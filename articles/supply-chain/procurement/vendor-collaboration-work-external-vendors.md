---
title: Samstarf lánardrottna með ytri lánardrottnum
description: Þetta efnisatriði lýsir því hvernig innkaupastjórum geta unnið með ytri lánardrottinn til að skiptast á upplýsingar um innkaupapantanir og vörusendingabirgðir.
author: mkirknel
manager: AnnBe
ms.date: 11/02/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, VendVendorPortalInvoicePart
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 221264
ms.assetid: dde49743-1541-4353-a030-63ca3069cd7d
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 733ecc7cfb4fee325560f5a6fe11612bb8ba57ef
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815296"
---
# <a name="vendor-collaboration-with-external-vendors"></a>Samstarf lánardrottna með ytri lánardrottnum

[!include [banner](../includes/banner.md)]

Kerfiseiningin **Samstarf lánardrottna** er ætluð lánardrottnum sem eru ekki með samþættingu rafrænna gagnaskipta (EDI) við Microsoft Dynamics 365 Supply Chain Management. Það gerir söluaðilum kleift að vinna með innkaupapantanir (POs), reikninga, upplýsingar um vöruskiptabirgðir og beiðni um tilboð (RFQs) og leyfir þeim einnig að fá aðgang að hluta lánardrottinssniðmáts. Þetta efnisatriði útskýrir hvernig er hægt vinna með ytri lánardrottna sem eru að nota viðmótið samstarf lánardrottna til að vinna með innkaupapantanir, beiðnir um tilboð og vörusendingabirgðir. Það útskýrir einnig hvernig á að virkja tiltekinn lánardrottinn til að nota samstarf lánardrottna og hvernig á að skilgreina þær upplýsingar sem allir lánardrottnar sjá þegar þeir svara Innkaupapöntun.

Fyrir frekari upplýsingar um hvaða ytri lánardrottnum geta gert viðmót fyrir samstarf lánardrottna , sjá [samstarf lánardrottna við viðskiptavini](vendor-collaboration-work-customers-dynamics-365-operations.md).

> [!NOTE]
> Upplýsingarnar um samstarf lánardrottna í þessu efnisatriði gildir aðeins um núverandi útgáfu Supply Chain Management. Í Microsoft Dynamics AX 7.0 (febrúar 2016) og Microsoft Dynamics AX forritaútgáfu 7.0.1 (maí 2016) notarðu kerfiseininguna **Gátt lánardrottins** fyrir samskipti við lánardrottna. Upplýsingar um kerfiseininguna **Gátt lánardrottins** er að finna í [Samstarf með lánardrottnum í gegnum Gátt lánardrottins](collaborate-vendors-vendor-portal.md).

Sjá frekari upplýsingar um hvernig lánardrottnum geta notað samstarf lánardrottna í reikningsfærslu ferli, sjá [vinnusvæði reikningsfærslu fyrir samstarf lánardrottna](../../financials/accounts-payable/vendor-portal-invoicing-workspace.md). Fyrir upplýsingar um hvernig á að gera ráðstafanir fyrir nýja notendur samstarfs lánardrottna, sjá [Stjórna notendum samstarfs lánardrottna](manage-vendor-collaboration-users.md).

## <a name="defining-the-information-that-is-shown-to-vendors-when-they-respond-to-pos"></a>Tilgreina upplýsingarnar sem eru sýndar lánardrottnum þegar þeir svara innkaupapöntunum

Þegar lánardrottna svara Innkaupapöntun sem þú sendir þeim, sjá þeir eitt af þremur skilaboðagluggum, þar sem þau þurfa að staðfesta að þeir vilja samþykkja Innkaupapöntunina, hafna henni eða samþykkja með breytingum. Þar sem upplýsingarnar sem þarf að sýna lánardrottins á þeim tímapunkti getur verið sértæk fyrir þitt fyrirtækið, geturðu tilgreina textann sem birtist í hverjum staðfestingarboðum. Til dæmis, getur textinn upplýst lánardrottinn um næsta skref í ferlinu, eða um skilmála.

Til að skilgreina textann sem birtist í svari við Innkaupabeiðni skal fylgja þessum skrefum

1. Opnaðu **Upplýsingar fyrir lánardrottna sem svara IP** síðuna, veldu tegund svars og veldu svo **Breyta**.
2. Í glugganum **Upplýsingar skilaboð** færið inn upplýsingar sem óskað er eftir að lánardrottna sjái á skilaboðaglugganum.

Ef nauðsynlegt er að bæta við skilaboðum á fleiri en eitt tungumál, skal stofna aðskilin skilaboð og tilgreina viðeigandi tungumálakóða fyrir hvert þeirra. Sérhverjum lánardrottni birtast skilaboð á tungumálinu sem þeir nota.

## <a name="setting-the-vendor-collaboration-options-for-a-specific-vendor"></a>Stilla valkosti fyrir samstarf lánardrottins fyrir ákveðinn lánardrottinn

Stjórnandi skilgreinir almennar stillingar fyrir samstarf lánardrottins, svo sem öryggishlutverkum sem eru í boði fyrir alla lánardrottna sem þú starfar með. Hinsvegar eru líka stillingum sem geta verið mismunandi fyrir hvern lánadrottnalykil. Þú ættir að skilgreina þessar stillingar.

- Virkja samstarf lánardrottna
- Tilgreina hvort lánardrottinn eigi að sjá verðupplýsingar.

### <a name="enabling-vendor-collaboration"></a>Virkja samstarf lánardrottna

Áður en hægt er að stofna notendareikningar fyrir ytri lánardrottinn, þarf að skilgreina lánardrottnalykilinn sem leyfir þeim að nota samstarf lánardrottna. Á síðunni **Lánardrottnar** á **Almennt** flipanum skal stilla **Virkja samstarf** svæðið. Eftirtaldir valkostir eru í boði:

- **Virk (Innkaupapöntun er staðfest sjálfkrafa)** - Innkaupapantanir eru sjálfkrafa staðfestar ef lánardrottinn samþykkir þær án breytinga.
- **Virk (Innkaupapöntun er ekki staðfest sjálfkrafa)** - Innkaupapantanir þarf að vera handvirkt staðfest af fyrirtæki þitt eftir að lánardrottni hefur samþykkt þau.

### <a name="specifying-whether-the-vendor-should-see-price-information"></a>Tilgreina hvort lánardrottinn ætti að sjá verðupplýsingar

Til að deila upplýsingum um verð fyrir Innkaupatilboð gegnum viðmót samstarfsins, þarf að stilla **verð/upphæð innkaupapöntunar** valkostinn á **Sjálfgefið í innkaupapöntun** flipanum fyrir lánardrottnalykilinn á **Já**. Þessi verðupplýsingar innihalda einingaverð, afslætti og gjöld.

## <a name="working-with-pos-when-vendor-collaboration-is-used"></a>Unnið með Innkaupapöntun þegar notað er samstarf lánardrottna

### <a name="sending-a-po-to-a-vendor"></a>Senda Innkaupapöntun til lánardrottins

Innkaupapantanir eru stofnaðar í Supply Chain Management. Þegar Innkaupapöntun hefur stöðuna **Samþykkt**, er hún send til lánardrottins með því að nota **Senda til staðfestingar** á **Innkaupapöntun** síðunni. Staða Innkaupapöntunar er síðan breytt í **í Ytri Yfirferð**. Þegar Innkaupapöntunin hefur verið send lánardrottni getur hann séð hana á síðunni **Innkaupapantanir til skoðunar** í viðmóti lánardrottnasamvinnu. Lánardrottinn getur þá samþykkt Innkaupapöntun, hafnað henni eða lagt til breytingar á henni. Lánardrottinn getur líka bætt við athugasemdum til að gefa upplýsingar, eins og breytingar á Innkaupapöntun. Ef óskað er að beina athygli lánardrottins að nýrri innkaupapöntun er einnig hægt að senda Innkaupapöntunina með tölvupósti með því að nota prentstýringarkerfið.

### <a name="confirmation-and-acceptance-of-a-po-by-a-vendor"></a>Staðfesting og samþykki Innkaupapöntunar af lánardrottinn

Þegar lánardrottinn hefur samþykkt innkaupapöntun má staðfesta hana sjálfvirkt eða það gæti þurft að staðfesta hana handvirkt. Hegðunin veltur á hvort reiturinn **Virkjun samstarfs** er stilltur á **Virkt (Innkaupapöntun er staðfest sjálfkrafa)** eða á **Virkt (Innkaupapöntun er ekki staðfest sjálfkrafa)** fyrir lánardrottinn.

Taflan hér að neðan sýnir dæmigerð upplýsingaskipti, eftir því hvernig lánardrottinn svarar þegar þú sendir innkaupapöntun til staðfestingar.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr>
<th>Svar lánardrottins</th>
<th>Niðurstaða</th>
</tr>
</thead>
<tbody>
<tr class="even">
<td>Lánardrottinn <strong>samþykkir</strong> pöntunina, og Supply Chain Management er stillt á að staðfesta sjálfvirkt Innkaupapöntun sem lánardrottinn staðfestir.</td>
<td>Staða pöntunar er uppfærð í <strong>Staðfest</strong>. Ef ekki er hægt að uppfæra pöntunina af einhverjum ástæðum er svar lánardrottins enn skráð sem <strong>Samþykkt</strong> en staða innkaupapöntunarinnar er áfram <strong>Í ytri yfirferð</strong>.&#39; 

Innkaupabeiðnin sem var sendur til lánardrottins og sem hefur stöðu <strong>Í ytri yfirferð</strong> er uppfærð með staðfestum afhendingardögum á línunum. Þessi uppfærsla hrindir af stað nýja útgáfu sem er sjálfkrafa stillt á <strong>Staðfest</strong> staða. Þegar innkaupapöntun er staðfest, birtist það í samstarfsviðmóti lánardrottna.</td>
</tr>
<tr class="odd">
<td>Lánardrottinn <strong>samþykkir</strong> pöntunina, en Supply Chain Management er ekki stillt á að staðfesta sjálfvirkt Innkaupapöntun sem lánardrottinn staðfestir.</td>
<td>Svar lánardrottins er skráð sem <strong>samþykkt</strong> en innkaupapöntunin er áfram í stöðunni <strong>Í ytri yfirferð</strong>.

Innkaupabeiðnin sem var sendur til lánardrottins og sem hefur stöðu <strong>Í ytri yfirferð</strong> er uppfærð með staðfestum afhendingardögum á línunum. Þessi uppfærsla hrindir af stað nýjan útgáfu sem er sjálfkrafa stillt á <strong>Í ytri yfirferð</strong> staða. Þú getur síðan samþykkt innkaupapöntunina handvirkt.</td>
</tr>
<tr class="even">
<td>Lánardrottinn <strong>hafnar</strong> pöntuninni.</td>
<td>Svar lánardrottins er skráð sem <strong>Hafnað</strong> og innkaupapöntunin er áfram í stöðunni <strong>Í ytri yfirferð</strong>. Höfnunin er móttekin með athugasemd lánardrottna.&#39;</td>
</tr>
<tr class="odd">
<td>Lánardrottinn <strong>samþykkir</strong> pöntunina <strong>með breytingum</strong>. Stungið er upp á breytingum á stigi línunnar. Lánardrottinn getur samþykkja eða hafna einstakar línur. Hér eru nokkrar aðrar breytingar sem lánardrottinn getur lagt til:
<ul>
<li>Breyta dagsetningum eða magn.</li>
<li>Skipta línum fyrir mismunandi afhendingardagsetningar eða magn.</li>
<li>Nota staðgengilsvöru.</li>
</ul>
Upplýsingar um verð og gjöld geta ekki verið breytt af lánardrottinn.&#39; Hins vegar getur lánardrottinn lagt til þessar breytingar með því að nota athugasemdir.</td>
<td>Svar lánardrottins er skráð sem <strong>Samþykkt með breytingum</strong> og innkaupapöntunin er áfram í stöðunni <strong>Í ytri yfirferð</strong>. Stöðurnar sýnir hvaða tegundir breytinga lánardrottinn hefur lagt til. Nánari upplýsingar um sjálfvirka notkun breytinga er að finna í &quot;Uppfæra Innkaupapöntunina þegar lánardrottinn leggur til breytingar&quot; kafla seinna í þessu efnisatriði. </td>
</tr>
</tbody>
</table>

Hægt er að nota vinnusvæðið **Undirbúningur innkaupapöntunar** til að fylgjast með hvaða innkaupapöntun lánardrottinn hefur svarað. Þetta vinnusvæði inniheldur tvo lista sem innihalda innkaupapantanir með stöðuna **í Ytri Yfirferð**:

- Í ytri yfirferð krefst aðgerða
- Í ytri yfirferð og bíður svars lánardrottins

### <a name="changing-a-po"></a>Breyta Innkaupapöntun

Til að breyta Innkaupapöntun sem lánardrottinn er þegar búið að svara, þarf að senda nýja útgáfu Innkaupapöntunar til lánardrottins. Ný Innkaupapöntunin verður með útgáfuviðskeyti til að gefa til kynna að það sé breytt útgáfa af Innkaupapöntun sem var send áður. Síðan **Staðfestingarsaga innkaupapantana lánardrottins** gerir þér og lánardrottnum kleift að rekja sögu hverja pöntun. Áður staðfest útgáfa Innkaupapöntunarinnar mun vera í lista yfir staðfestar Innkaupapantanir þar til ný Innkaupapöntun hefur verið staðfest.

### <a name="canceling-a-po"></a>Hætta við Innkaupapöntun

Þegar hætt er við Innkaupapöntun er stöðu breytt í **Samþykkt**. Þú þarft að senda Innkaupapöntunina aftur til lánardrottins þannig að lánardrottinn get staðfest eða hafnað ógildingunni. Eftir að ógildingin er staðfest birtist Innkaupapöntunin í lista lánardrottins yfir staðfestar Innkaupapantanir sem **Hætt við**.

### <a name="adding-attachments-to-a-po"></a>Bætir viðhengjum við IP

Hægt að bæta við viðhengjum eins og skrám, myndum og athugasemdum við Innkaupapöntun með því að nota skjalastjórnunarkerfið. Viðhengi við gerðina **Ytri** verða sýnileg lánardrottni þegar Innkaupapöntunin er send til þeirra.

## <a name="updating-a-po-when-a-vendor-suggests-changes"></a>Uppfærsla á Innkaupapöntun þegar lánardrottinn leggur til breytingar

Ef seljandi hefur svarað Innkaupapöntun og lagt til breytingum er næsta skref að vinna úr svarinu.

Í vinnusvæðinu **Undirbúningur fyrir innkaupapöntun**, í **Í ytri yfirferð krefst aðgerða** listanum, getur þú borið kennsl á innkaupapöntun sem lánardrottinn hefur samþykkt með breytingum. Frá þessum lista geturðu einnig farið yfir á svar lánardrottins.

Á svari getur lánardrottinn breytt eftirfarandi upplýsingar á hausnum:
 
- Tilvísun lánardrottnaskjals
- Afhendingarmáti
- Afhendingarskilmálar
- Staðfest dagsetning afhendingar

Lánardrottinn getur einnig bætt við athugasemd eða viðhengi.

Á línunum getur lánardrottinn breytt magninu og afhendingardögum, bætt við athugasemdum og viðhengjum, hafnað línu, skipt út fyrir línu fyrir aðra vöru sem er slegin inn sem texti og skipt línu í margar sendingar. Staða lína er breytileg eftir því hvaða breytingar lánardrottinn hefur lagt til:
    
- **Samþykkt með breytingum**
- **Hafnað**
- **Skipt út** - Í þessu tilviki er bætt við viðbótarlínu sem hefur stöðu **Skipting**.
- **Staðfest**
- **Skipt í áætlun** - Í þessu tilfelli er bætt við auka línur sem hafa stöðu **Áætlunarlínur**.

Hafi lína engar breytingar er línustaðan **Samþykkt**.

Á svöruninni sýna stöður línanna þér þær tegundir breytingar sem lánardrottinn gerði. Að auki birtast öll svæði sem voru breytt sem feitletruð til að hjálpa þér að bera kennsl á breytingarnar.

Þú getur uppfært Innkaupapöntun með því að velja **Vinna uppfærslu innkaupapöntunar** á svarinu eða á einum línu í einu. **Er uppfærsla Innkaupapöntunar unnin?** reitur á hausnum og línunum sýna hvort kerfið hefur unnið hausinn eða línurnar til að uppfæra Innkaupapöntunina með breytingum sem koma frá svarinu. Þú getur keyrt **Vinna uppfærslu Innkaupapöntunar** aðgerðina aðeins einu sinni á hvern haus eða línu.

Ekki er hægt að uppfæra allar ráðlagðar breytingar í innkaupapöntun. Aðeins uppfærslur á hausnum og uppfærslur á dagsetningum og magni á línum geta sjálfkrafa verið uppfærðar á Innkaupapöntuninni. Fyrir aðrar breytingar verður að uppfæra innkaupapöntunina handvirkt. Í þessu tilviki er gildi **Er Innkaupapöntun uppfærslan unnin?** reitsins **Handvirk uppfærsla**. Til dæmis, ef lánardrottinn leggur til að lína sé skipt inn í áætlun, verður þessi breyting að vera gerðar handvirkt.

Sérhver lína sem hefur stöðu **Samþykkt** mun hafa staðfestan afhendingardag. Þegar þú keyrir **Vinna uppfærslu Innkaupapöntunar** aðgerðina, er þessi dagsetning uppfærður á Innkaupapöntuninni. Athugasemdir og viðhengi eru ekki sjálfkrafa fluttar í núverandi Innkaupapöntun. Að auki eru viðskiptasamningar ekki endurmetnar á Innkaupapöntunarlínum þegar þú uppfærir núverandi Innkaupapöntun í gegnum **Vinna uppfærslu Innkaupapöntunar** aðgerðina.

## <a name="po-statuses-and-versions"></a>Staða og útgáfur innkaupapöntunar

Þessi kafli lýsir mismunandi stöðum sem Innkaupapöntun getur haft fram að þeim tíma sem hún er staðfest. Það lýsir einnig hvenær nýjar útgáfur af Innkaupapöntun eru tiltækar lánardrottni. Hegðunin er breytileg eftir því hvort notuð eru breytingarstjórnun fyrir innkaupapantanir. 

### <a name="versions-and-statuses-if-you-dont-use-change-management"></a>Útgáfur og stöður ef þú notar ekki breytingastjórnun

Taflan hér að neðan sýnir dæmi um breytingar á stöðu og útgáfum sem Innkaupapöntun gæti farið í gegnum.

| Aðgerð | Staða og útgáfa |
|--------|--------------------|
| Upprunaleg útgáfa af Innkaupapöntuninni er stofnuð í Supply Chain Management. | Staðan er **Samþykkt**. |
| Innkaupapöntunin er send á lánardrottins. | Útgáfa er skráð í viðmót samstarfs lánardrottna og stöðunni er breytt í **Í Ytri Yfirferð**. |
| Lánardrottinn sendir inn **Samþykkt með breytingum** svarið. | Staðan er enn **í Ytri yfirferð**. |
| Þú gerir einhverjar breytingar sem lánardrottinn biður um. | Stöðu breytt í **Samþykkt**. |
| Þú sendir nýja útgáfu af Innkaupapöntuninni lánardrottins. | Ný útgáfa er skráð í viðmót samstarfs lánardrottna og stöðunni er breytt í **Í Ytri Yfirferð**. |
| Lánardrottinn samþykkir nýju útgáfuna af IP. | Staðan er enn **í Ytri Yfirferð** nema lánardrottnalykill er skilgreindur til að stilla sjálfkrafa Innkaupapantanir á stöðuna **Staðfest** þegar lánardrottinn samþykkja þær. |

Lánardrottnar þurfa ekki að staðfesta Innkaupapöntun með því að nota viðmóti fyrir samstarf lánardrottna. Þeir geta einnig sent skilaboð í tölvupósti eða tilkynnt samþykki Innkaupapöntunarinnar gegnum aðrar rásir. Þú getur síðan samþykkt pöntunina handvirkt. Í þessu tilfelli berst þér viðvörun sem tilkynnir að verið sé að staðfesta pöntun jafnvel þótt að það er ekkert svar frá lánardrottni. Innkaupapöntunin birtist síðan í staðfestingarferli sem opin staðfest pöntun sem hefur ekki svör. Lánardrottinn hefur á þessu stigi ekki lengur valkost til að staðfesta eða hafna innkaupapöntun.

> [!NOTE]
> Sú útgáfa Innkaupapöntunar sem er tiltæk öðrum vinnslum í Supply Chain Management er alltaf síðasta útgáfa, jafnvel þó að sú útgáfa hafi ekki enn verið skráð í viðmóti fyrir samstarf lánardrottna.

### <a name="versions-and-statuses-if-you-use-change-management"></a>Útgáfur og stöður ef þú notar breytingastjórnun

Ef breytingastjórnun er virkjuð fyrir Innkaupapöntun, fer Innkaupapöntunin í gegnum samþykktarverkflæði til að komast í stöðuna **Samþykkt**. Þetta ferli er ekki sýnilegt lánardrottni.

Taflan hér að neðan sýnir dæmi um breytingar á stöðu og útgáfu sem Innkaupapöntun gæti farið í gegnum þegar breytingastjórnun er virkjuð. Útgáfa er skráð þegar Innkaupapöntunin er samþykkt, ekki þegar Innkaupapöntunin er send til lánardrottins eða staðfest.

| Aðgerð | Staða og útgáfa |
|--------|--------------------|
| Upprunaleg útgáfa af Innkaupapöntuninni er stofnuð í Supply Chain Management. | Staðan er **Drög**. |
| Innkaupapöntunin er send í samþykktarferli. (Samþykktarferlið er innra ferli sem lánardrottinn er ekki hluti af.) | Stöðunni er breytt úr **Drög** til **Í Yfirferð** til **Samþykki** ef Innkaupapöntuninni er ekki hafnað meðan á samþykktarferlinu stendur. Samþykkt innkaupapöntun er skráð sem útgáfa. | 
| Innkaupapöntunin er send á lánardrottins. | Útgáfa er skráð í viðmót samstarfs lánardrottna og stöðunni er breytt í **Í Ytri Yfirferð**. |
| Þú gerir nokkrar breytingar sem lánardrottinn óskar eftir, annaðhvort handvirkt eða með því að nota **Vinna uppfærslu Innkaupapöntunar** aðgerðina á svarið til að uppfæra Innkaupapöntunina. | Stöðu er breytt aftur í **Drög**. |
| Innkaupapöntunin er send aftur í samþykktarferlið. | Stöðunni er breytt úr **Drög** til **í Yfirferð** til **Samþykki** ef Innkaupapöntuninni er ekki hafnað meðan á samþykktarferlinu stendur. Einnig er hægt að skilgreina kerfið þannig að breytingar krefjast ekki endursamþykktar. Í þessu tilfelli fer staðan fyrst í **Drög** og er sjálfkrafa uppfærð í **Samþykkt**. Samþykkta Innkaupapöntunin er skráð sem ný útgáfa. |
| Þú sendir nýja útgáfu af Innkaupapöntuninni lánardrottins. | Ný útgáfa er skráð í viðmót samstarfs lánardrottna og stöðunni er breytt í **Í Ytri Yfirferð**. |
| Lánardrottinn samþykkir nýju útgáfuna. | Stöðu er breytt í **Staðfest**, annað hvort sjálfvirkt eða þegar svarið kemur frá lánardrottni og síðan er Innkaupapöntunin staðfest. |

## <a name="sharing-information-about-consignment-inventory"></a>Deila upplýsingum um vörusendingabirgðir

Ef verið er að nota vörusendingabirgðir, geta lánardrottna notað viðmót fyrir samstarf lánardrottna til að skoða upplýsingar um eftirfarandi síður:

- **Innkaupapantanir sem notar vörusendingabirgðir** - Innkaupapantanir fyrir vörusendingabirgðir eru myndaðar þegar eignarhaldi á birgðum er breytt frá lánardrottninum til fyrirtækis þíns. Innhreyfingarskjal afurða er bókaðar samtímis. Þessum innkaupapantanir vörusendinga birtast aðeins á **Innkaupapantanir sem nota vörusendingabirgðir** síðuna. Þær eru ekki teknar með í **Allar staðfestar innkaupapantanir** síðuna í **samstarf lánardrottna** kerfiseiningunni.
- **Afurðir sem er tekið við úr vörusendingabirgðum** - Þessi síða inniheldur lista yfir allar færslur þar sem eignarhald afurða hefur verið flutt frá lánardrottni til fyrirtækis þíns. Lánardrottnar geta nota þessar upplýsingar til að reikningsfæra á viðskiptavininn.
- **Vörusendingarbirgðir á lager** - Þessi síða sýnir vörusendingabirgðir á lager í eigu lánardrottins sem hefur verið móttekið í vöruhúsi þínu.

## <a name="working-with-rfqs-when-you-use-vendor-collaboration"></a>Vinna með tilboðsbeiðni þegar þú notar samstarf lánardrottna

Þessi kafli lýsir samskiptum á milli viðskiptavina og lánardrottna meðan á tilboðsbeiðnaferli stendur. Það útskýrir einnig hvernig upplýsingar eru sendar til lánardrottna. Fyrir grunn yfirlit yfir stuðning við tilboðsbeiðnaferlið, sjá [Yfirlit yfir beiðnir um tilboð (RFQs)](request-quotations.md).

### <a name="alternates-attachments-amendments-and-returns"></a>Staðgenglar, viðhengi, lagfæringar og skil

- **Staðgenglar** - Á hausnum í tilboðsbeiðnatilfelli getur þú tilgreint að staðgenglar séu leyfðir fyrir vörulínur utan vörulista. Þegar staðgenglar eru virkjaðir geta lánardrottnar bætt við staðgenglalínum fyrir hverja línu sem beðið er um.
- **Viðhengi** - Viðhengjum er hægt að bæta við bæði á síðuhaussstigi og línustigi í tilboðsbeiðnatilfelli. Viðhengi er hægt að flokka annað hvort sem innri eða ytri. Innri viðhengi er aðeins hægt að skoða á viðskiptavinarhliðinni, en lánardrottnar geta skoðað ytri viðhengi eftir að þau eru send.

    Lánardrottnar geta einnig bætt við viðhengjum á svartilboðinu sínu. Þessar viðhengi má skoða á viðskiptavinarhliðinni eftir að lánardrottinn leggur fram tilboðssvarið. Viðhengi sem lánardrottnar bæta við eru alltaf flokkaðir sem ytri. Til að fá aðgang að viðhengi sem lánardrottinn hefur sent saman með tilboð skaltu velja **Tilboðsviðhengi** eða **Tilboðslínuviðhengi**.
    
    Til að opna viðhengi sem voru send saman með tilboðsbeiðnatilfellinu, skaltu nota bréfaklemmutákn skjalastjórnunar á svarinu.

- **Lagfæringar** - Þegar lagfæringu er lokið verða fyrirliggjandi tilboðssvör fjarlægð þannig að hægt sé að skipta þeim út fyrir uppfærð gildi. Upplýsingar eins og línaverð og magn frá fyrri tilboðssvörum má skoða í gegnum færslubækur á tilboðsbeiðnatilfellinu.

    Til að knýja fram lagfæringarferli skal á síðunni **Innkaup og aðföng færibreytur**, á **Beiðni um tilboð** flýtiflipanum, stilla **Læsa tilboðsbeiðnum þegar þau eru send** á **Já**. (Þessi valkostur er stilltur og áskilinn fyrir opinbera aðila.)

- **Skil** - Ef lánardrottinn hefur sent inn tilboð, en meiri eða breyttar upplýsingar eru nauðsynlegar fyrir tilboðsbeiðna tilvikið, getur viðskiptavinurinn skilað tilboðinu til lánardrottins. Gögnin frá tilboðinu, sem áður var lagt fram, er haldið eftir og lánardrottinn getur framkvæmt breytingarnar sem farið var fram á án þess að þurfa að endurræsa tilboðsferlið.

## <a name="public-sector-extensions"></a>Viðbót fyrir hið opinbera

Fyrir opinbera geiranum, útvíkkuð virkni gerir tilboðsbeiðnatilfelli kleift að vera sent til lánardrottna og birt. Þegar þú birtir tilboðsbeiðni getur allir sem óska eftir upplýsingunum skoðað verkið sem samræmist flestum opinberum reglum. Öll tiltæk vinna endurspeglast í **Opnar birtar beiðnir um tilboð** listasíðu, og þær tilboðsbeiðnir sem hætt er við, eru í bið eða veittar má skoða á **Lokaðar birtar beiðnir um tilboð** listasíðu. Þessar skjöl eru einnig hægt að skoða á vefsvæði utan Supply Chain Management gegnum samþættingu við eftirfarandi gagnaeiningar:

- Útgefnar tilboðsbeiðnir
- Lína útgefinna tilboðsbeiðna
- Viðhengi hausa útgefinna tilboðsbeiðna

Þessar einingar leyfa fólki sem ekki eru forsjárnotendur í Supply Chain Management, en sem hafa nafnlausan aðgang að ytri síðunni, að skoða tiltæka og lokaða vinnu. Að auki leyfir útvíkkuð virkni í **Senda og birta** notanda sem setur upp færibreytur fyrir vinnslu tilboðsbeiðni að skilgreina tölvupóstsnið. Svo þegar innkaupastjóri stofnar tilfelli tilboðsbeiðni verður hann eða hún að velja tölvupóstsniðið til að senda nauðsynlegar upplýsingar til lánardrottna í tilboðsbeiðnatilfellinu. 

Notandinn sem setur upp færibreytur fyrir tilboðsbeiðniferlið getur búið til margar tölvupóstsniðmát. Þessar tölvupóstsniðmát geta innihaldið bæði fastan texta og eftirfarandi skiptitákn. Táknunum verður skipt út fyrir samhengisháð gildi þegar tölvupóstur er búinn til.

- %RFQCase%
- %RFQCaseName%
- %bidType%
- nviteOnly%%i
- %expiryDateTime%
- %requester%
- %requestingDepartment%
- %accountnum%
- %todaysdate%
- %createddate%

Ef lagfæringar er krafist og er send eftir að tilboðsbeiðni er send, þá mun tilboðsbeiðnin verða endursend til allra boðinna lánardrottna. Útgefið skjalið verður líka uppfært á síðunni **Opna útgefnar tilboðsbeiðnir**.
