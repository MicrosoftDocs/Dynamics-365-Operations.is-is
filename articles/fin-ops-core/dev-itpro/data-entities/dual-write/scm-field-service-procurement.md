---
title: Samstilling innkaupa milli Supply Chain Management og Field Service
description: Þetta efnisatriði lýsir því hvernig samþætting tvöfaldrar skráningar styður stofnun og uppfærslur innkaupapöntunar úr bæði Supply Chain Management og Field Service.
author: RamaKrishnamoorthy
ms.date: 11/11/2020
ms.topic: article
audience: Application User
ms.reviewer: rhaertle
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2020-11-11
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 4a2420981553957b6b234fe56747bc6f3568acf6b8ad77366c33caeae63b4faf
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716760"
---
# <a name="integrate-procurement-between-supply-chain-management-and-field-service"></a>Samstilling innkaupa milli Supply Chain Management og Field Service

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Microsoft Dynamics 365 Supply Chain Management býður upp á öfluga innkaupavirkni. Dynamics 365 Field Service býður upp á svipaða virkni sem styður innkaupaferlin sem tengjast þjónustuferlinu. Virknin í þessum tveimur forritum er samþætt í gegnum tvöfalda skráningu og víðtæk notkunartilfellin sem fylgja eru virkjuð í gegnum töfluvarpanir, lausnarreglu, yfirlit og skjámyndir.

Þessi samþætting styður stofnun innkaupapantana og í flestum tilfellum uppfærslur úr báðum forritum. Supply Chain Management styður hins vegar verðlagningu, aðsetrum og innhreyfingarskjali afurðar. Nokkur öflug víðtæk notkunartilfelli eru virkjuð fyrir fyrirtæki sem nota bæði Field Service og Supply Chain Management. Þessi notkunartilfelli gera kleift að hefja innkaup og rekja þau í báðum kerfunum.

Eftirfarandi mynd sýnir töflur í báðum kerfum og hvernig þeim er varpað hvort í annað. Innkaupapantanir í Field Service vísa í línu *reiknings* en innkaupapantanir í Supply Chain Management vísa aftur á móti í línu *lánardrottins*. Til að leysa úr samþættingu notar tvöföld skráning vísun til að tengja línur *lánardrottins* við línur *reiknings*. Frekari upplýsingar er að finna í [Samþætt lánardrottinssniðmát](vendor-mapping.md).

![Varpanir fyrir innkaup.](media/scm-field-service-tables.png)

## <a name="prerequisites"></a>Forkröfur

Til að samþætta Supply Chain Management við Field Service þarf að setja upp eftirfarandi þætti:

- Field Service, útgáfa 8.8.31.60 eða nýrri, fyrir alhliða samþættingu innkaupapöntunar
- Supply Chain Management útgáfa 10.0.14 eða nýrri
- Tvöföld skrif, til að keyra OneFSSCM-lausn

## <a name="installation-guidelines"></a>Uppsetningarleiðbeiningar

### <a name="prerequisites"></a>Forkröfur

- **Tvöföld skrif** – Frekari upplýsingar eru í [Tvöföld skrif – heimasíða](dual-write-home-page.md#dual-write-setup).
- **Dynamics 365 Field Service** – Frekari upplýsingar eru [Hvernig á að setja upp Dynamics 365 Field Service](/dynamics365/field-service/install-field-service#step-1-install-dynamics-365-field-service).

Þegar það er virkjað í Microsoft Dataverse kynna tvöföld skráning og Field Service ýmsar lagskiptar lausnir til sögunnar sem stækka umhverfið með nýjum lýsigögnum, skjámyndum, yfirlitum og reglu. Hægt er að virkja þessar lausnir í hvaða röð sem er, þó oftast sé sett upp í þeirri röð sem gefin er upp hér:

1. **Field Service Common** – Field Service Common er sett upp þegar Field Service er sett upp í umhverfinu.
2. **Field Service (Anchor)** – Field Service (Anchor) er sett upp þegar Field Service er sett upp í umhverfinu. 
3. **Supply Chain Management Extended** – Supply Chain Management Extended er sjálfkrafa sett upp þegar tvöföld skráning er virkjuð í umhverfi. 
4. **OneFSSCM-lausn** – OneFSSCM er sjálfkrafa sett upp af annarri hvorri lausninni (Field Service eða Supply Chain Management) sem var síðast sett upp.

    - Ef Field Service er þegar uppsett í umhverfinu og tvöföld skráning er virkjuð sem setur upp Supply Chain Management Extended, verður OneFSSCM sett upp.
    - Ef Supply Chain Management Extended er þegar uppsett í umhverfinu og Field Service er sett upp, verður OneFSSCM sett upp.

## <a name="initial-synchronization"></a>Upphafleg samstilling

Til að stofna nýjar innkaupapantanir og vinna með fyrirliggjandi innkaupapantanir þarf að samstilla tilvísunargögnin á milli Supply Chain Management og Dataverse. Upphafsskrifvirknin er notuð til að greina töflutengslin og finna töflurnar sem þarf að virkja fyrir tiltekið kort.

Þú verður að samstilla eftirfarandi töflur:

- Afurðasniðmát

    Þegar upphafleg skrif eru keyrð kemur upp heildarlisti yfir nauðsynlegar töflur. Hér eru nokkur dæmi um þessi sniðmát:

    - Allar afurðir
    - Útgefnar afurðir V2
    - Dataverse útgefnar einkvæmar afurðir

- Svæði
- Vöruhús
- Innkaupaflokkasniðmát

    Hér eru nokkur dæmi um þessi sniðmát:

    - Innkaupaflokkar
    - Handvirk stilling
    - Tegundastigveldi afurðar
    - Úthlutanir afurðategundar

- Sniðmát lánardrottna, t.d. lánardrottinn V2
- Sniðmát tengiliðaa, t.d. Dataverse-tengiliðir V2
- Sniðmát starfskrafts, t.d. Starfskraftur

Samstilling taflanna tryggir að öll skjöl (innkaupapantanir og innhreyfingarskjöl) í Supply Chain Management verði tiltæk í Dataverse.

### <a name="account-and-vendor-tables"></a>Lykla -og lánardrottnatöflur

Innkaupapantanir í Field Service treysta á að reikningstaflan reki lánardrottna. Þess vegna nota Dataverse-töflurnar fyrir innkaupapantanir lykla til að rekja lánardrottna. Til að brúa þennan mikilvæga mun þarf að virkja eftirfarandi fjögur verkflæði til að halda lyklum og lánardrottnum samstilltum: 

- Stofna lánardrottna í reikningstöflu
- Stofna lánardrottna í lánardrottnatöflu
- Uppfæra lánardrottna í reikningstöflu
- Uppfæra lánardrottna í lánardrottnatöflu

Ef eitt OneFSSCM er uppsett, vegna þess að bæði Field Service og Supply Chain Management Extended eru uppsett, eru þessi verkflæði sjálfkrafa virkjuð. Ef Field Service er ekki uppsett, en ætlunin er að samþætta töflur innkaupapantana við Dataverse, þarf að virkja þessi verkflæði. Í báðum tilvikum, nema byrjað sé frá grunni, gæti þurft að ganga úr skugga um að allir lánardrottnar séu stofnaðir sem lyklar í Dataverse áður en innkaupapantanir eru stofnaðar. Að öðrum kosti gætu villur komið upp.

### <a name="initial-synchronization"></a>Upphafleg samstilling

Þegar öll skilyrði eru á sínum stað, ef ætlunin er að fyrirliggjandi innkaupapantanir og innhreyfingarskjöl afurða verði tiætk í báðum kerfum, þarf að gera upphaflega samstillingu á eftirfarandi sniðmátum:

- Haus innkaupapöntunar V2
- CDS Innkaupapantanalína
- CDS-innkaupapantanalína með mjúkeyðingu
- Móttaka innkaupapöntunar
- Afurð í móttöku innkaupapöntunar

## <a name="mappings-with-logic"></a>Varpanir með reglu

Samþætting innkaupa stækkar afurðavörpunina með eftirfarandi reglu til að ganga úr skugga um að dálkurinn **Afurðargerð Field Service** sé rétt stilltur í afurðatöflunni í Dataverse:

- Ef **Afurðargerð** er stillt á *Afurð* og **Vörulíkanaflokkur, afurð í birgðum** er stillt á *Satt*, er **Afurðargerð Field Service** stillt á *Birgðir*.
- Ef **Afurðargerð** er stillt á *Afurð* og **Vörulíkanaflokkur, afurð í birgðum** er stillt á *Ósatt*, er **Afurðargerð Field Service** stillt á *Ekki birgðir*.
- Ef **Afurðargerð** er stillt á *Þjónusta*, er **Afurðargerð Field Service** stillt á *Þjónusta*.

Auk þess inniheldur Dataverse reglu sem varpar lánardrottnum með tilheyrandi lyklum þeirra. Þessi regla stillir sjálfgefinn lánardrottnalykil reiknings. Þegar stofnuð, stillir viðbótarregla þjónustumegin sjálfgefinn lánardrottnalykil reiknings úr lánardrottninum sem tengist lyklinum. Lánardrottinn er með tilvísun í reikningslykilinn sem er notaður til að stilla þetta gildi.

## <a name="supported-scenarios"></a>Studdar aðstæður

- Dataverse notendur geta búið til og uppfært innkaupapantanir. Ferlinu og gögnum er hins vegar stjórnað af Supply Chain Management. Takmarkanir á uppfærslum á dálkum innkaupapöntunar í Supply Chain Management eiga við þegar uppfærslur koma frá Field Service. Til dæmis er ekki hægt að uppfæra innkaupapöntun ef hún er frágengin. 
- Ef innkaupapöntun er stjórnað af breytingastjórnun í Supply Chain Management getur notandi Field Service aðeins uppfært innkaupapöntunina þegar samþykktarstaða Supply Chain Management er *Drög*.
- Nokkrir dálkar eru aðeins stýrðir af Supply Chain Management og er ekki hægt að uppfæra í Field Service. Til að fá upplýsingar um hvaða dálka er ekki hægt að uppfæra skal skoða vörpunartöflur í afurðinni. Til einföldunar eru flestir þessara dálka stilltir sem skrifvarðir á Dataverse-síðum. 

    Til dæmis er dálkum fyrir verðupplýsingar stýrt með Supply Chain Management. Supply Chain Management er með viðskiptasamninga sem Field Service getur notið góðs af. dálkar á borð við **Einingarverð**, **Afsláttur** og **Nettóupphæð** koma aðeins úr Supply Chain Management. Til að tryggja að verðið sé samstillt við Field Service ætti að nota eiginleikann **Samstilla** á síðunum **Innkaupapöntun** og **Afurð innkaupapöntunar** í Dataverse þegar gögn innkaupapöntunar hafa verið slegin inn. Frekari upplýsingar er að finna í [Samstilla við innkaupagögn Dynamics 365 Supply Chain Management samkvæmt eftirspurn](#sync-procurement).

- Dálkurinn **Samtölur** er aðeins í boði í Field Service vegna þess að engar uppfærðar samtölur innkaupapöntunarinnar eru til staðar í Supply Chain Management. Samtölur í Supply Chain Management eru reiknaðar út frá mörgum færibreytum sem eru ekki í boði í Field Service.
- Innkaupapöntunarlínur þar sem aðeins innkaupategund er tilgreind, eða þar sem tilgreind afurð er vara af afurðargerðinni *Þjónusta* eða afurðargerðinni Field Service, er aðeins hægt að hefja í Supply Chain Management. Línurnar eru síðan samstilltar við Dataverse og eru sýnilegar í Field Service.
- Ef aðeins Field Service er uppsett, ekki Supply Chain Management, er dálkurinn **Vöruhús** áskilinn í innkaupapöntun. Ef Supply Chain Management er hins vegar uppsett, er slakað á þessari kröfu vegna þess að Supply Chain Management leyfir innkaupapöntunarlínur þar sem ekkert vöruhús er tilgreint við ákveðnar kringumstæður.
- Innhreyfingarskjölum afurða (móttökum innkaupapantana í Dataverse) er stjórnað af Supply Chain Management og er ekki hægt að stofna úr Dataverse ef Supply Chain Management er uppsett. Innhreyfingarskjöl afurða úr Supply Chain Management eru samstillt úr Supply Chain Management við Dataverse.
- Undirafhending er leyfð í Supply Chain Management. OneFSSCM-lausnin bætir við reglu þannig að þegar innhreyfingarlína afurðar (eða innhreyfingarafurð innkaupapöntunar í Dataverse) er stofnuð eða uppfærð er lína birgðabókar stofnuð í Dataverse til að leiðrétta eftirstandandi magn sem er í pöntun fyrir aðstæður undirafhendingar.

## <a name="unsupported-scenarios"></a>Óstuddar aðstæður

- Field Service kemur í veg fyrir að línum sé bætt við afturkallaða innkaupapöntun í Supply Chain Management. Sem hjáleið er hægt að breyta kerfisstöðu innkaupapöntunar í Field Service og síðan bæta nýju línunni við annaðhvort Field Service eða Supply Chain Management.
- Þótt innkaupalínur hafi áhrif á birgðastöður í báðum kerfum, þá tryggir þessi samþætting ekki jafnar birgðir á milli Supply Chain Management og Field Service. Bæði Field Service og Supply Chain Management eru með aðra ferla sem uppfæra birgðastöður. Þessi ferli eru utan umfangs innkaupa.

## <a name="status-management"></a>Stöðustjórnun

Stöður innkaupapantana í Field Service eru frábrugðnar stöðunum í Supply Chain Management.

### <a name="field-service-purchase-order-and-purchase-order-product-statuses"></a>Innkaupapöntun Field Service og afurðarstöður innkaupapöntunar

| Haus – kerfisstaða | Haus - samþykktarstaða | Vörustaða |
|---|---|---|
| <ul><li>Drög</li><li>Sent inn</li><li>Hætt við</li><li>Móttekin afurð</li><li>Reikningsfært</li></ul> | <ul><li>Núll</li><li>Samþ.</li><li>Hafnað</li></ul> | <ul><li>Í biðstöðu</li><li>Móttekið</li><li>Hætt við</li></ul> |

### <a name="supply-chain-management-purchase-order-and-purchase-order-line-statuses"></a>Stöður innkaupa og innkaupapöntunarlína Supply Chain Management.

Samþykktarstöður lína eru aðeins virkar þegar verkflæði línu er til staðar.

| Haus – skjalastaða | Haus - samþykktarstaða | Staða línu | Samþykktarstaða línu |
|---|---|---|---|
| <ul><li>Opin pöntun (biðpöntun)</li><li>Móttekið</li><li>Reikningsfært</li><li>Hætt við</li></ul> | <ul><li>Drög</li><li>Í endurskoðun</li><li>Samþ.</li><li>Hafnað</li><li>Í ytri yfirferð</li><li>Staðfest</li><li>Lokið</li></ul> | <ul><li>Opin pöntun (biðpöntun)</li><li>Móttekið</li><li>Reikningsfært</li><li>Hætt við</li></ul> | <ul><li>Ekki sent</li><li>Í endurskoðun</li><li>Samþ.</li><li>Hafnað</li></ul> |

Eftirfarandi reglur eru notaðar fyrir stöðudálka:

- Ekki er hægt að uppfæra stöðu í Supply Chain Management úr Field Service. Hins vegar verður staðan í Field Service í sumum tilfellum uppfærð þegar staða innkaupapöntunar í Supply Chain Management er breytt.
- Ef innkaupapöntun í Supply Chain Management er undir breytingastjórnun og verið er að vinna úr breytingu, er samþykktarstaðan *Drög* eða *Í yfirferð*. Í slíku tilfelli verður samþykktarstaða Field Service stillt á *Núll*.
- Ef samþykktarstaða innkaupapöntunar í Supply Chain Management er stillt á *Samþykkt*, *Í ytri yfirferð*, *Staðfest* eða *Lokið*, verður samþykktarstaða innkaupapöntunar Field Service stillt á *Samþykkt*.
- Ef samþykktarstaða innkaupapöntunar í Supply Chain Management er stillt á *Hafnað* verður samþykktarstaða innkaupapöntunar Field Service stillt á *Hafnað*.
- Ef staðan í haus skjals í Supply Chain Management er breytt í *Opin pöntun (biðpöntun)* og staða innkaupapöntunar Field Service er *Drög* eða *Hætt við*, verður stöðu innkaupapöntunar Field Service breytt í *Sent inn*.
- Ef staðan í haus skjals í Staða í Supply Chain Management er breytt í *Hætt við* og engar innhreyfingarafurðir innkaupapöntunar í Field Service tengjast innkaupapöntuninni (í gegnum afurðir innkaupapöntunar), er kerfisstaða Field Service stillt á *Hætt við*.
- Ef staða innkaupapöntunarlínu í Supply Chain Management er *Hætt við*, er afurðarstaða innkaupapöntunar í Field Service stillt á *Hætt við*. Að auki, ef staða innkaupapöntunarlínu í Supply Chain Management er breytt úr *Hætt við* í *Biðpöntun*, staða afurðavöru innkaupapöntunar í Field Service stillt á *Í bið*.

## <a name="sync-with-the-supply-chain-management-procurement-data-on-demand"></a><a id="sync-procurement"></a>Samstilla við innkaupagögn Supply Chain Management samkvæmt eftirspurn

Supply Chain Management inniheldur innkaupagögn fyrir viðskiptasamninga, afslætti og aðrar aðstæður sem reiða sig á aðra ferla í Supply Chain Management. Innkaupavélin notar flóknar reglur til að finna út besta verðið fyrir tiltekna innkaupapöntun. Þegar tvöföld skráning er notuð er gögnum ekki alltaf haldið samstilltum milli beggja umhverfa, sérstaklega í aðstæðum þar sem línur eru stofnaðar eða uppfærðar úr Dataverse og gætu sett í gang frekari ferla í Supply Chain Management.

## <a name="sync-the-procurement-data-from-supply-chain-management"></a>Samstilla innkaupagögn úr Supply Chain Management

1. Í Dataverse skal fara í **Birgðir \> Innkaupapöntun**.
2. Veljið **Ný** til að stofna nýja innkaupapöntun eða veljið línu í fyrirliggjandi innkaupapöntun.
3. Úr innkaupapöntun eða innkaupapöntunarlínu.
4. Á aðgerðasvæðinu skal velja **Samstilla**.

Allir dálkar úr Dataverse og Field Service sem er deilt með Supply Chain Management eru samstilltir.

Hér eru aðstæður þar sem þarf hugsanlega að nota aðgerðina **Samstilla**:

- Ef margar breytingar eru gerðar á sömu línunni úr Dataverse skal keyra aðgerðina **Samstilla**.
- Ef ekki er víst hvort breyting kann að vera önnur breytingin í röð úr Dataverse gæti reynst sniðugt að keyra aðgerðina **Samstilla**.
- Ef villuboð birtast um uppfærslu á gildi úr Supply Chain Management skal keyra aðgerðina **Samstilla** og síðan reyna uppfærsluna aftur í Dataverse.

## <a name="cancelling-the-posting-process"></a>Hætt við bókunarferlið

Ef hætt er við bókunarferli innhreyfingarskjals afurðar í úrvinnslunni, þá gæti tvöföld skráning stofnað innhreyfingarskjalslínu afurðar í Dataverse, en ekki stofnað innhreyfingarskjalslínu afurðar í Supply Chain Management. Þessi staða kemur upp vegna þess að tvöföld skráning styður ekki dreifðar færslur.

## <a name="templates"></a>Sniðmát

Eftirfarandi sniðmát eru í boði fyrir samþættingu á fylgiskjölum sem tengjast innkaupum.

| Birgðakeðjustjórnun | Field Service | lýsing |
|---|---|---|
| [Haus innkaupapöntunar V2](mapping-reference.md#183) | msdyn\_Purchaseorders | Þessi tafla inniheldur dálka sem tákna haus innkaupapöntunarinnar. |
| [Eining innkaupapöntunarlínu](mapping-reference.md#181) | msdyn\_PurchaseOrderProducts | Þessi tafla inniheldur línur sem tákna línur í innkaupapöntun. Afurðarnúmerið er notað fyrir samstillingu. Þetta auðkennir afurðina sem birgðahaldseiningu, þ.m.t. afurðarvíddir. Frekari upplýsingar um samþættingu afurðar Dataverse má finna í [Samræmd afurðaupplifun](product-mapping.md). |
| [Haus afurðarkvittunar](mapping-reference.md#185) | msdyn\_purchaseorderreceipts | Þessi tafla inniheldur hausa innhreyfingarskjals afurða sem eru stofnaðir þegar innhreyfingarskjöl afurða eru bókuð í Supply Chain Management. |
| [Lína innhreyfingarskjals](mapping-reference.md#184) | msdyn\_purchaseorderreceiptproducts | Þessi tafla inniheldur innhreyfingarskjalslínur afurðar sem eru stofnaðar þegar innhreyfingarskjal afurðar er bókað í Supply Chain Management. |
| [Eining mjúkeyðingar innkaupapöntunarlínu](mapping-reference.md#182) | msdyn\_purchaseorderproducts | Þessi tafla inniheldur upplýsingar um innkaupapöntunarlínur sem eru mjúkeyddar. Aðeins er hægt að mjúkeyða innkaupapöntunarlínu í Supply Chain Management þegar innkaupapöntunin hefur verið staðfest eða samþykkt ef kveikt er á breytingastjórnun. Línan er til í gagnagrunni Supply Chain Management og er merkt sem **IsDeleted**. Fyrst að Dataverse er ekki með mjúkeyðingu skilgreinda, er mikilvægt að þessar upplýsingar séu samstilltar við Dataverse. Á þennan hátt er hægt að eyða línum, sem eru mjúkeyddar í Supply Chain Management, sjálfkrafa úr Dataverse. Í slíku tilfelli er reglan til að eyða línu í Dataverse staðsett í Supply Chain Management Extended. |

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
