---
title: Reikna afhendingardaga sölupöntunar með CTP
description: Með CTP-afhendingargeta (Óhætt að lofa) getur þú gefið viðskiptavinum raunhæfar dagsetningar fyrir hvenær þú getur lofað tilteknum vörum. Í þessari grein er því lýst hvernig á að setja upp og nota CTP-afhendingargetu fyrir hverja áætlunarvél (Fínstilling áætlanagerðar og aðaláætlunarvél).
author: t-benebo
ms.date: 07/20/2022
ms.topic: article
ms.search.form: SalesAvailableDlvDates, SalesTable, CustParameters, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-07-20
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: 4a3b8ba89d9fb224026cf32cad89d7f28321ee79
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9741204"
---
# <a name="calculate-sales-order-delivery-dates-using-ctp"></a>Reikna afhendingardaga sölupöntunar með CTP

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->
<!-- KFN: Split into two topics, one for PO and one for classic. -->

Með CTP-afhendingargeta (Óhætt að lofa) getur þú gefið viðskiptavinum raunhæfar dagsetningar fyrir hvenær þú getur lofað tilteknum vörum. Fyrir hverja sölulínu getur þú gefið upp dagsetningu sem tekur mið af lagerbirgðum, framleiðslugetu og flutningstíma.

CTP endurbætir virkni ATP [(](../../sales-marketing/delivery-dates-available-promise-calculations.md)tiltækt-til-loforðs) með því að greina upplýsingar um afköst. Þar sem ATP tekur aðeins til greina efnislegt framboð og gerir ráð fyrir ótakmörkuðum afkastatilföngum tekur CTP tillit til bæði efnis og afkastagetu. Því gefur það raunhæfari mynd af því hvort hægt sé að fullnægja eftirspurn innan ákveðins tímaramma.

CTP-afhendingargeta virka aðeins öðruvísi, eftir því hvaða aðaláætlunarvél þú notar (Fínstilling áætlanagerðar eða úreltu aðaláætlunarvélina). Í þessari grein er því lýst hvernig á að setja það upp fyrir hverja vél. CTP-afhendingargeta fyrir fínstilling skipulagningar styður eins og er aðeins hluta af þeim aðstæðum CTP-afhendingargetu sem eru studdar af úreltu aðaláætlunarvélinni.

## <a name="turn-on-ctp-for-planning-optimization"></a>Kveikja á CTP-afhendingargeta fyrir fínstillingu áætlanagerðar

CTP-afhendingargeta fyrir úreltu aðaláætlunarvélina er alltaf tiltækt. Ef þú vilt hins vegar nota CTP fyrir fínstillingu áætlanagerðar verður að slökkva á því fyrir kerfið þitt. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Aðaláætlanagerð*
- **Heiti eiginleika:** *(Forútgáfa) CTP-afhendingargeta fyrir fínstillingu áætlanagerðar*

## <a name="how-ctp-compares-to-atp"></a>Hvernig CTP er borið saman við ATP

CTP og ATP eru svipuð, en CTP getur oft gefið nákvæmari niðurstöðu, eins og eftirfarandi dæmi sýnir.

Vara A er vara sem er samsettur úr vöru B og C og lagerbirgðir A-vöru eru 0 (núll). Ef þú gerir athugun á ATP sem tekur aðeins til efna verður magn ATP einnig 0 (núll). Ef þú hins vegar framkvæmir athugun CTP-afhendingargeta mun kerfið athuga hvort atriði B og C séu til staðar, athuga tilföngin sem þarf til að setja þau inn í vöru A og reikna út hversu mörg af vörum A er hægt að gera. Að auki getur útreikningur CTP-afhendingargetu athugað tilföng og efni sem þarf til að gera meira af vörum B og C, og til að nota þá til að gera meira af vöru A.

Útreikningur CTP-afhendingargetu sem telur að bæði efni og tilföng gætu sýnt stærra magn en útreikningur sem athugar aðeins efni, sérstaklega þegar varan sem er verið að athuga er vara sett saman í pöntun. Með öðrum orðum, er virkni CTP-afhendingargeta byggð á niðurbrotsaðgerðinni og hægt er að keyra fyrir valda sölupöntunarlínu til að reikna út væntanlegan afhendingardag.

## <a name="how-ctp-differs-depending-on-the-master-planning-engine-that-you-use"></a>Hvernig CTP-afhendingargeta er mismunandi eftir því hvaða aðaláætlunarvél þú notar

Eftirfarandi tafla dregur saman muninn á CTP-afhendingargeta fyrir áætlanagerð og CTP-afhendingargeta fyrir úreltu aðaláætlunarvélina.

| Eining | Fínstilling áætlanagerðar | Úrelt aðaláætlunarvél |
|---|---|---|
| Stilling **Stýring afhendingardagsetninga** fyrir pantanir, pöntunarlínur og vörur | *CTP fyrir fínstillingu áætlanagerðar* | *CTP-afhendingargeta* |
| Tími útreiknings | Útreikningurinn er settur af stað með því að keyra sveigjanlega áætlun sem áætlað verk. | Útreikningurinn er strax virkjaður í hvert sinn sem þú slærð inn eða uppfærir sölupöntunarlínu. |
| Reitargildi **Staða CTP fyrir fínstillingu áætlanagerðar** | <p>Gildi *Ekki tilbúið* er sýnt fyrir pantanir og pöntunarlínur þar sem breytileg áætlun hefur ekki verið keyrð síðan pantanir og línur voru búnar til eða uppfærðar síðast.</p><p>Gildið *Tilbúið* er sýnt fyrir pantanir og línur þar sem CTP-afhendingargeta hefur verið notað til að reikna út staðfesta afhendingardaga með því að keyra breytilegu áætlunina.</p> | Gildið *Tilbúið* er alltaf sýnt. |

## <a name="set-default-delivery-date-control-methods"></a><a name="default-methods"></a>Velja sjálfgefna stýring afhendingardagsetninga

Kerfið getur notað hvaða af nokkrum aðferðum sem er til að reikna út áætlanir um afhendingardag fyrir hverja pöntun og pöntunarlínu. Þú ættir að velja stjórnunaraðferð afhendingardags sem oftast er notuð sem altæk sjálfgefin aðferð. Einnig er hægt að stilla einstakar hnekkingar fyrir hverja vöru. Seinna verður hægt að hnekkja sjálfgefnar aðferðir fyrir hverja pöntun og/eða pöntunarlínu eins og þú krefst.

### <a name="set-the-global-default-delivery-date-control"></a><a name="global-default"></a>Stilla altæka, sjálfgefna stýringu afhendingardagsetninga

Sjálfgefin stjórnunaraðferð fyrir afhendingardag verða notuð fyrir allar nýjar pöntunarlínur þar sem hnekking á ekki við. Til að velja einn skaltu fylgja þessum skrefum.

1. Opnið **Viðskiptakröfur \> Setja upp \> Færibreytur viðskiptakrafna**.
1. Á flipanum **Sendingar** á flýtiflipanum **Afhendingarstýring**, í reitnum **Stýring afhendingardags** er valin sú aðferð sem á að nota sem sjálfgefna aðferð fyrir fyrirtækið þitt:

    - *Ekkert* – Ekki reikna afhendingardaga.
    - *Afhendingartími sölu* – afhendingartími sölu er tíminn milli stofnunar sölupöntunarinnar og sendingu vara. Útreikningur afhendingardags er á grundvelli sjálfgefinn fjölda daga, og tekur ekki tillit til birgðastöðu, , þekktrar eftirspurnar eða áætlað framboð.
    - *ATP* – ATP er magn vöru sem er tiltækur og hægt er að lofa viðskiptavini á tiltekinni dagsetningu. ATP útreikningur felur í sér óstaðfestar birgðir, afhendingartími , áætlaðar innhreyfingar og úthreyfingar.
    - *ATP + mörk úthreyfinga*, sendingardagsetning er sú sama og dagsetning sem er tiltækt-til-loforðs (ATP) auk marka úthreyfinga fyrir vöruna. Mörk úthreyfinga er sá tími sem þarf að undirbúa þær vörur sem á að senda.
    - *CTP* – Notaðu CTP útreikninginn sem er gefinn upp af úreltu aðaláætlunarvélinni. Ef þú ert að nota fínstilling áætlanagerðar er ekki heimilt að nota *CTP-afhendingargetu* sem stýringaraðferð afhendingardags og ef hún er valin mun það valda villu þegar útreikningur er keyrður.
    - *CTP fyrir fínstillingu skipulagningar -* Notaðu CTP útreikninginn sem er gefinn upp með fínstillingu skipulagningar. Þessi valkostur hefur engin áhrif ef þú notar úreltu aðaláætlunarvélina.

### <a name="set-delivery-date-control-overrides-for-individual-products"></a>Stilla stýringu afhendingardags fyrir einstakar vörur

Þú getur úthlutað hnekkingum fyrir tilteknar vörur þar sem þú vilt nota aðra stýringaraðferð fyrir afhendingardag en þá sem er skilgreind sem altæk sjálfgefin aðferð.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veljið vöruna sem á að setja upp.
1. Á aðgerðasvæðinu, í flipanum **Stjórna birgðum**, í flokknum **Pöntunarstillingar**, skal velja **Sjálfgefnar pöntunarstillingar**.
1. Á síðunni **Stillingar hefðbundinnar pöntunar**, á flýtiflipanum **Sölupöntun** stillir þú valkostinn **Hnekkja afhendingarstýringu** á *Já*.
1. Í reitnum **Stýring afhendingardagsetningar** er valin sú aðferð sem nota á fyrir valda vöru. Sömu valkostir og lýst er í hlutanum [Stilla altæka, sjálfgefna stýringu afhendingardagsetninga](#global-default) eru tiltækir.

## <a name="schedule-ctp-for-planning-optimization-calculations"></a><a name="batch-job"></a>Áætlun CTP-afhendingargeta fyrir fínstillingu áætlanagerðar

Þegar þú notar CTP-afhendingargeta til fínstillingar skipulagningar verður þú að keyra breytilega áætlun til að ræsa kerfið til að gera útreikninga CTP-afhendingargeta og stilla síðan staðfesta sendingar- og móttökudaga fyrir allar viðeigandi pantanir. Áætlunin verður að innihalda allar vörur sem staðfestar sendingar- og móttökudagsetningar eru nauðsynlegar fyrir. (Þegar þú notar CTP-afhendingargeta fyrir úrelta aðaláætlunarvél eru CTP-afhendingargeta útreikningarnir gerðir strax á staðnum. Þar af leiðandi þarftu ekki að keyra sveigjanlega áætlun til að sjá CTP-afhendingargeta niðurstöðurnar.)

Til að tryggja að dagsetningarnar séu tiltækar í tæka tíð fyrir alla notendur mælum við með því að þú setjir upp runuvinnsla til að framkvæma endurteknar áætlanir. Til dæmis, runuvinnsla sem er sett upp til að keyra breytilega áætlun á 30 mínútna fresti mun stilla staðfesta sendingar- og móttökudagsetningar á 30 mínútna fresti. Notendur sem slá inn og flytja inn pantanir þurfa því að bíða í að hámarki 30 mínútur til að fá staðfestar sendingar- og móttökudagsetningar.

Til að setja upp runuvinnslu til að keyra breytilega áætlun á venjulegri áætlun skal fylgja þessum skrefum.

1. Farið í **Aðaláætlanagerð \> Aðaláætlanagerð \> Keyra \> Aðaláætlanagerð**.
1. Í svarglugganum **Aðaláætlanagerð**, í flýtiflipanum **Færibreytur** stillirðu reitinn **Aðaláætlun** á breytilegu áætlunina sem á að keyra.
1. Á flýtiflipanum **Keyra í bakgrunni** skal stilla valkostinn **Runuvinnsla** á *Já*.
1. Veldu **Endurtekning** og settu upp áætlun eftir þörfum.
1. Veldu **Í lagi** til að vista áætlunina.
1. Veljið **Í lagi** til að stofna runuvinnsla og loka svarglugganum.

## <a name="use-ctp-for-the-deprecated-master-planning-engine"></a>Nota CTP-afhendingargetu fyrir úrelta aðaláætlunarvél

### <a name="create-a-new-order-by-using-ctp-for-the-deprecated-master-planning-engine"></a>Stofna nýja pöntun með því að nota CTP fyrir úreltu aðaláætlunarvélina

Í hvert sinn sem nýrri sölupöntun eða pöntunarlínu er bætt við úthlutar kerfið sjálfgefna stýringaraðferð fyrir afhendingardag. Pöntunarhausinn byrjar alltaf á altæku sjálfgefnu aðferðinni. Ef hnekkingu er úthlutað á pantaða vöru mun nýja pöntunarlínan nota þessa hnekkingu. Annars mun nýja pöntunarlínan einnig nota altæku sjálfgefnu aðferðina. Þess vegna ættir þú að stilla sjálfgefnu aðferðirnar þannig að þær passi við stýringaraðferð afhendingardags sem þú notar oftast. Eftir að pöntun er stofnuð er hægt að hnekkja sjálfgefinni aðferð í haus pöntunar og/eða pöntunarlínustigi eins og krafist er. Frekari upplýsingar eru í [Velja sjálfgefna stýring afhendingardagsetninga](#default-methods) og [Breyta núverandi sölupöntunum til að nota CTP-afhendingargetu](#change-orders).

### <a name="view-confirmed-delivery-dates-when-you-use-ctp-for-the-deprecated-master-planning-engine"></a>Skoða staðfestar afhendingardaga þegar CTP-afhendingargeta er notað fyrir aðaláætlunarvélina

Ef þú notar úreltu aðaláætlunarvélina eru útreikningar CTP-afhendingargeta notaðir á pantanir og/eða pöntunarlínur þar sem reiturinn **Stýring afhendingardagsetninga** er stilltur á *CTP-afhendingargeta*.

Fyrir sölulínur sem nota CTP-afhendingargeta fyrir úreltu aðaláætlunarvélina, stillir kerfið sjálfkrafa reitina **Staðfest sendingardagsetning** og **Staðfest móttökudagsetning** í hvert skipti sem þú vistar sölulínu. Ef þú gerir síðar viðeigandi breytingu á sölulínu (til dæmis með því að breyta magni hennar eða svæði) verða dagsetningarnar samstundis endurreiknaðar.

- Til að skoða staðfesta afhendingardaga sölupöntunarlínu skaltu opna sölupöntunina og velja sölulínuna. Síðan í flýtiflipanum **Upplýsingar um línu**, í flipanum **Afhending**, skal stilla gildin **Staðfest sendingardagsetning** og **Staðfest móttökudagsetning**.
- Til að skoða staðfesta afhendingardaga fyrir heila pöntun skaltu opna sölupöntunina og velja yfirlitið **Haus**. Í flýtiflipanum **Afhending** skal stilla gildin **Staðfest sendingardagsetning** og **Staðfest móttökudagsetning**.

## <a name="use-ctp-for-planning-optimization"></a>Nota CTP fyrir fínstillingu áætlanagerðar

### <a name="create-a-new-order-by-using-ctp-for-planning-optimization"></a>Stofna nýja pöntun með því að nota CTP fyrir fínstillingu áætlanagerðar

Í hvert sinn sem nýrri sölupöntun eða pöntunarlínu er bætt við úthlutar kerfið sjálfgefna stýringaraðferð fyrir afhendingardag. Pöntunarhausinn byrjar alltaf á altæku sjálfgefnu aðferðinni. Ef hnekkingu er úthlutað á pantaða vöru mun nýja pöntunarlínan nota þessa hnekkingu. Annars mun nýja pöntunarlínan einnig nota altæku sjálfgefnu aðferðina. Þess vegna ættir þú að stilla sjálfgefnu aðferðirnar þannig að þær passi við stýringaraðferð afhendingardags sem þú notar oftast. Eftir að pöntun er stofnuð er hægt að hnekkja sjálfgefinni aðferð í haus pöntunar og/eða pöntunarlínustigi eins og krafist er. Frekari upplýsingar eru í [Velja sjálfgefna stýring afhendingardagsetninga](#default-methods) og [Breyta núverandi sölupöntunum til að nota CTP-afhendingargetu](#change-orders).

### <a name="view-confirmed-delivery-dates-when-using-ctp-for-planning-optimization"></a>Skoða staðfesta afhendingardaga þegar CTP-afhendingargeta er notað til að fínstilla skipulagningu

Ef þú notar fínstilling skipulagningar eru útreikningar CTP-afhendingargeta notaðir á pantanir og/eða pöntunarlínur þar sem reiturinn **Stýring afhendingardagsetninga** er stilltur á *CTP-afhendingargeta fyrir fínstilling skipulagningar*.

Fyrir sölulínur sem nota CTP-afhendingargeta til fínstillingar skipulagningar eru reitirnir **Staðfest sendingardagsetning** og **Staðfest móttökudagsetning** auðir þar til keyrð er viðeigandi breytileg áætlun (yfirleitt með því að nota venjulega runuvinnslu). Þær eru þá sjálfkrafa stilltar. Frekari upplýsingar er að finna í [Áætlun CTP-afhendingargeta fyrir fínstillingu áætlanagerðar](#batch-job).

**CTP-afhendingargeta fyrir fínstilling skipulagningar** segir til um hvort staðfestar dagsetningar hafi enn verið reiknaðar fyrir hverja línu sem notar CTP-afhendingargetu fyrir fínstillingu skipulagningar. Reiturinn sýnir gildi *Ekki tilbúið* fyrir línur og pantanir þar sem staðfestar afhendingardagsetningar hafa annað hvort ekki enn verið reiknaðar út eða eru ekki lengur í gildi vegna annarra breytinga. Það sýnir gildið *Tilbúið* fyrir línur og pantanir sem hafa verið reiknaðar. Hægt er að skoða stöðuna fyrir hverja línu og fyrir alla pöntunina.

- Til að skoða stöðuna fyrir sölupöntunarlínu skaltu opna sölupöntunina og velja sölulínuna. Síðan, á flýtiflipanum **Upplýsingar um línu** á flipanum **Afhending** skaltu fara yfir gildið **CTP-afhendingargeta fyrir fínstilling skipulagningar**. Reitirnir **Staðfest sendingardagsetning** og **Staðfest móttökudagsetning** fyrir línuna eru einnig sýndir á þessum flipa eftir að þeir hafa verið reiknaðir út.
- Til að skoða stöðuna fyrir alla pöntunina skaltu opna sölupöntunina og velja yfirlitið **Haus**. Síðan, á flýtiflipanum **Afhending** skaltu fara yfir gildið **CTP-afhendingargeta fyrir fínstilling skipulagningar**. Reitirnir **Staðfest sendingardagsetning** og **Staðfest móttökudagsetning** fyrir pöntunina eru einnig sýndir á þessum flipa eftir að þeir hafa verið reiknaðir út.

<!-- KFM: The following text may be untrue and needs to be reviewed with the PM for next revision:

The sales orders that are *Ready* or *Not ready* are shown in the **All sales orders** list page. You can check the sales order that are *Ready* or *Not ready* from the sales order list page by filtering on this new status field.

-->

> [!NOTE]
> - Ef þú uppfærir sölupöntunarlínu eftir að CTP-afhendingargeta fyrir fínstilling skipulagningar hefur reiknað út staðfestar dagsetningar fyrir hana hreinsar kerfið dagsetningar þar til næst þegar viðeigandi breytileg áætlun er keyrð.
> - Ef þú breytir tengdri stillingu sem gæti haft áhrif á núverandi staðfestar dagsetningar (til dæmis með því að breyta afhendingartími, bókunum eða merkingum) ættir þú að hreinsa staðfestar dagsetningar fyrir núverandi pantanir. Þessi aðgerð verður til þess að stöðu hverrar línu verður breytt í *Ekki tilbúin*. Þessi breyting mun síðan valda því að kerfið getur endurreiknað staðfestar dagsetningar næst þegar það keyrir breytilegu áætlunina.

## <a name="change-existing-sales-orders-so-that-they-use-ctp"></a><a name="change-orders"></a>Breyta núverandi sölupöntunum þannig að þær noti CTP-afhendingargetu

Hægt er að breyta **Stýringu afhendingardagsetningar** fyrir hvaða opna pöntun sem er hvenær sem er. Hægt er að breyta gildi í hausstigi og/eða fyrir hverja línu eins og þú krefst.

### <a name="change-to-ctp-at-the-order-header-level"></a>Breyta í CTP-afhendingargeta á stigi pöntunarhaussins

<!-- KFM: Would be nice to mention how changing this setting on the header affects the individual lines. -->

Til að breyta pöntun þannig að hún noti CTP-afhendingargeta á hausstigi pöntunar skal fylgja þessum skrefum.

1. Opna **Viðskiptakröfur \> Pantanir \> Allar sölupantanir**.
1. Opnaðu sölupöntunina sem þú vilt setja upp eða stofnaðu nýja.
1. Veldu **Haus** til að opna upplýsingar um haus á síðunni **Upplýsingar um sölupöntun**.
1. Í flýtiflipi **Afhending** skal stilla reitinn **Stýring afhendingardagsetninga** á eitt af eftirfarandi gildum, eftir því hvaða áætlunarvél þú ætlar að nota:

    - *CTP* – Notaðu CTP útreikninginn sem er gefinn upp af úreltu aðaláætlunarvélinni. Ef þú ert að nota fínstilling skipulagningar er ekki heimilt að stjórna *CTP-afhendingargeta* afhendingardegi. Ef þetta gildi er valið kemur því upp villa þegar útreikningurinn er keyrður.
    - *CTP fyrir fínstillingu skipulagningar -* Notaðu CTP útreikninginn sem er gefinn upp með fínstillingu skipulagningar. Þessi stilling hefur engin áhrif ef þú notar úreltu aðaláætlunarvélina.

<!-- KFM: Additional dialogs are shown here. Review these with the PM and expand this procedure at next revision. -->
1. Veldu **Í lagi** til að gera breytinguna.

### <a name="change-to-ctp-at-the-order-line-level"></a>Skipta yfir í CTP-afhendingargetu á stigi pöntunarlínu

Ef þú bjóst til pöntunarlínu með því að nota aðra stýriaðferð fyrir afhendingardag getur þú breytt í CTP-afhendingargeta hvenær sem er. Breytingar sem gerðar eru á línustigi hafa ekki áhrif á aðrar línur. Hins vegar gætu þær valdið því að heildar afhendingardagur pöntunar færast fram eða til baka, eftir því hvernig hver uppfærður línuútreikningur breytist. <!-- KFM: Confirm this intro at next revision -->

Fylgið eftirfarandi skrefum til að breyta pöntun þannig að hún noti CTP-afhendingargeta fyrir úrelta aðaláætlunarvél á línustigi.

1. Opna **Viðskiptakröfur \> Pantanir \> Allar sölupantanir**.
1. Opnaðu sölupöntunina sem þú vilt setja upp eða stofnaðu nýja.
1. Á síðunni **Upplýsingar um sölupöntun**, í flýtiflipanum **Sölupöntunarlínur**, skal velja sölupöntunarlínurnar sem á að setja upp.
1. Í flýtiflipa **Upplýsingar um línu** á flipanum **Afhending** skal stilla reitinn **Stýring afhendingardagsetninga** á eitt af eftirfarandi gildum, eftir því hvaða áætlunarvél þú ætlar að nota:

    - *CTP* – Notaðu CTP útreikninginn sem er gefinn upp af úreltu aðaláætlunarvélinni. Ef þú ert að nota fínstilling skipulagningar er ekki heimilt að stjórna *CTP-afhendingargeta* afhendingardegi. Ef þetta gildi er valið kemur því upp villa þegar útreikningurinn er keyrður.
    - *CTP fyrir fínstillingu skipulagningar -* Notaðu CTP útreikninginn sem er gefinn upp með fínstillingu skipulagningar. Þessi stilling hefur engin áhrif ef þú notar úreltu aðaláætlunarvélina.

    Svarglugginn **Tiltækar sendingar- og móttökudagsetningar sendingar- og** birtist og sýnir Tiltækar sendingar- og móttökudagsetningar. Þessi svargluggi virkar á sama hátt fyrir pöntunarlínur og fyrir haus pöntunar, eins og lýst er í fyrri hluta.

1. Í aðgerðarúðunni skal velja **Vista**.
