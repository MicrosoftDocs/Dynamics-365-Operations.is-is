---
title: Reikna afhendingardaga sölupöntunar með CTP
description: Capable-to-promise (CTP) virkni gerir þér kleift að gefa viðskiptavinum raunhæfar dagsetningar fyrir hvenær þú getur lofað tilteknum vörum. Þessi grein lýsir því hvernig á að setja upp og nota CTP fyrir hverja skipulagsvél (Planning Optimization og innbyggða vélin).
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
ms.openlocfilehash: 3b8e3dc9f0e7aaf019aa4d7284458206e7daadb2
ms.sourcegitcommit: 86c0562ce1ecdf7937125c0f5a6771f178b459e7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/24/2022
ms.locfileid: "9714861"
---
# <a name="calculate-sales-order-delivery-dates-using-ctp"></a>Reikna afhendingardaga sölupöntunar með CTP

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Capable-to-promise (CTP) virkni gerir þér kleift að gefa viðskiptavinum raunhæfar dagsetningar fyrir hvenær þú getur lofað tilteknum vörum. Fyrir hverja sölulínu er hægt að gefa upp dagsetningu sem tekur mið af fyrirliggjandi lagerbirgðum, framleiðslugetu og flutningstíma.

CTP framlengir [í boði að lofa](../../sales-marketing/delivery-dates-available-promise-calculations.md) (ATP) virkni með því að huga að getuupplýsingum. Á meðan ATP lítur aðeins á efnisframboð og gerir ráð fyrir óendanlegum getuauðlindum, þá lítur CTP á framboð á bæði efni og getu. Þess vegna gefur það raunsærri mynd af því hvort hægt sé að fullnægja eftirspurn innan ákveðins tímaramma.

CTP virkar örlítið öðruvísi, allt eftir aðalskipulagsvélinni sem þú ert að nota (Planning Optimization eða innbyggða vélin). Þessi grein lýsir því hvernig á að setja það upp fyrir hverja vél. CTP fyrir fínstillingu áætlanagerðar styður sem stendur aðeins undirmengi af CTP-sviðsmyndum sem eru studdar af innbyggðu vélinni.

## <a name="turn-on-ctp-for-planning-optimization"></a>Kveiktu á CTP fyrir áætlanagerð fínstillingu

CTP fyrir innbyggðu aðalskipulagsvélina er alltaf til staðar. Hins vegar, ef þú vilt nota CTP fyrir áætlanagerð fínstillingu, verður að snúa því fyrir kerfið þitt. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Aðaláætlanagerð*
- **Eiginleikaheiti:** *(Forskoðun) CTP fyrir hagræðingu áætlanagerðar*

## <a name="how-ctp-compares-to-atp"></a>Hvernig CTP er í samanburði við ATP

CTP og ATP eru svipaðar, en CTP getur oft gefið nákvæmari niðurstöðu eins og eftirfarandi dæmi sýnir.

Atriði A er hlutur sem er samsettur úr liðum B og C, og birgðamagn vöru A er 0 (núll). Ef þú gerir ATP athugun sem tekur aðeins til efnis verður ATP magnið einnig 0 (núll). Hins vegar, ef þú gerir CTP-athugun, mun kerfið athuga hvort atriði B og C séu tiltæk, athuga tilföngin sem þarf til að gera þau að lið A og reikna út hversu mörg atriði A er hægt að búa til. Að auki getur CTP útreikningurinn athugað tilföng og efni sem þarf til að gera meira úr hlutum B og C, og til að nota þau til að gera meira úr hlut A.

CTP útreikningur sem tekur bæði til efnis og tilföngs gæti sýnt meira magn en útreikningur sem athugar eingöngu efni, sérstaklega þegar varan sem verið er að athuga er samsett eftir pöntun. Með öðrum orðum, CTP virkni er byggð á sprengiaðgerðinni og hægt er að keyra hana fyrir valda sölupöntunarlínu til að reikna út áætlaðan afhendingardag.

## <a name="how-ctp-differs-depending-on-the-master-planning-engine-that-you-use"></a>Hvernig CTP er mismunandi eftir aðalskipulagsvélinni sem þú notar

Eftirfarandi tafla dregur saman muninn á CTP fyrir hagræðingu áætlanagerðar og CTP fyrir innbyggðu aðalskipulagsvélina.

| Eining | Fínstilling áætlanagerðar | Innbyggð aðalskipulagsvél |
|---|---|---|
| **Stýring á afhendingardagsetningu** stilling fyrir pantanir, pöntunarlínur og vörur | *CTP fyrir fínstillingu áætlanagerðar* | *CTP* |
| Tími útreiknings | Útreikningurinn er settur af stað með því að keyra kraftmikla áætlun sem áætlað verkefni. | Útreikningurinn fer strax í gang í hvert skipti sem þú slærð inn eða uppfærir sölupöntunarlínu. |
| **CTP fyrir áætlanagerð hagræðingu stöðu** reit gildi | <p>Verðmæti á *Ekki tilbúinn* er sýnt fyrir pantanir og pöntunarlínur þar sem kvika áætlunin hefur ekki keyrt síðan pantanir og línur voru búnar til eða síðast uppfærðar.</p><p>Verðmæti á *Tilbúið* er sýnd fyrir pantanir og línur þar sem CTP hefur verið notað til að reikna út staðfestar afhendingardagsetningar með því að keyra kraftmiklu áætlunina.</p> | Verðmæti á *Tilbúið* er alltaf sýndur. |

## <a name="set-default-delivery-date-control-methods"></a><a name="default-methods"></a> Stilltu sjálfgefna afhendingardagsetningaraðferðir

Kerfið getur notað einhverja af nokkrum aðferðum til að reikna út afhendingardagsetningaráætlun fyrir hverja pöntun og pöntunarlínu. Þú ættir að stilla afhendingardagsetningaraðferðina sem þú vilt nota oftast sem alþjóðlega sjálfgefna aðferð. Þú getur líka stillt einstakar hnekkjanir fyrir hverja vöru. Síðar muntu geta hnekið sjálfgefnum aðferðum fyrir hverja pöntun og/eða pöntunarlínu eftir þörfum.

### <a name="set-the-global-default-delivery-date-control"></a><a name="global-default"></a> Stilltu alþjóðlega sjálfgefna afhendingardagsetningarstýringu

Sjálfgefin aðferð til að stjórna afhendingardagsetningu verður notuð á allar nýjar pöntunarlínur þar sem hnekking á ekki við. Til að velja einn skaltu fylgja þessum skrefum.

1. Opnið **Viðskiptakröfur \> Setja upp \> Færibreytur viðskiptakrafna**.
1. Á **Sendingar** flipa, á **Afhendingareftirlit** Flýtiflipi, í **Stýring á afhendingardagsetningu** reit, veldu aðferðina sem þú vilt nota sem sjálfgefna aðferð fyrir fyrirtæki þitt:

    - *Enginn* – Ekki reikna út afhendingardaga.
    - *Afhendingartími sölu* – afhendingartími sölu er tíminn milli stofnunar sölupöntunarinnar og sendingu vara. Útreikningur á afhendingardagsetningu byggir á sjálfgefnum fjölda daga og tekur ekki tillit til lagerframboðs, þekktrar eftirspurnar eða fyrirhugaðs framboðs.
    - *ATP* – ATP er magn vöru sem er tiltækt og hægt er að lofa viðskiptavinum á tilteknum degi. ATP útreikningur felur í sér óstaðfestar birgðir, afhendingartími , áætlaðar innhreyfingar og úthreyfingar.
    - *ATP + Útgáfubil* – Sendingardagsetningin jafngildir ATP dagsetningunni auk útgáfuframlegðar vörunnar. Mörk úthreyfinga er sá tími sem þarf að undirbúa þær vörur sem á að senda.
    - *CTP* – Notaðu CTP-útreikninginn sem innbyggða aðalskipulagsvélin veitir. Ef þú ert að nota áætlanagerð hagræðingu, the *CTP* aðferð til að stjórna afhendingardagsetningu er ekki leyfð og ef hún er valin mun hún valda villu þegar útreikningurinn keyrir.
    - *CTP fyrir hagræðingu áætlanagerðar* – Notaðu CTP-útreikninginn sem er veittur af Planning Optimization. Þessi valkostur hefur engin áhrif ef þú ert að nota innbyggðu aðalskipulagsvélina.

### <a name="set-delivery-date-control-overrides-for-individual-products"></a>Stilltu afhendingardagsetningarstýringar fyrir einstakar vörur

Þú getur úthlutað hnekkingum fyrir tilteknar vörur þar sem þú vilt nota aðra afhendingardagastýringaraðferð en þá sem er stillt sem alhliða sjálfgefna aðferðin þín.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veldu vöruna sem þú vilt setja upp.
1. Á aðgerðasvæðinu, í flipanum **Stjórna birgðum**, í flokknum **Pöntunarstillingar**, skal velja **Sjálfgefnar pöntunarstillingar**.
1. Á **Sjálfgefnar pöntunarstillingar** síðu, á **Sölupöntun** flýtiflipann, stilltu **Hneka afhendingarstýringu** valmöguleika til *Já*.
1. Í **Stýring á afhendingardagsetningu** reit, veldu aðferðina sem á að nota fyrir valda vöru. Sömu valkostir og lýst er í [Stilltu alþjóðlega sjálfgefna afhendingardagsetningarstýringu](#global-default) kafla eru í boði.

## <a name="schedule-ctp-for-planning-optimization-calculations"></a><a name="batch-job"></a> Tímasettu CTP fyrir útreikninga á hagræðingu áætlanagerðar

Þegar þú notar CTP fyrir áætlanagerð fínstillingu verður þú að keyra kraftmikla áætlun til að kveikja á kerfinu til að gera CTP útreikninga og stilla síðan staðfestar sendingar og móttökudagsetningar fyrir allar viðeigandi pantanir. Áætlunin verður að innihalda alla hluti sem staðfestar sendingar og móttökudagsetningar eru nauðsynlegar fyrir. (Þegar þú notar CTP fyrir innbyggðu áætlunarvélina, eru CTP útreikningar strax gerðir á staðnum. Þess vegna þarftu ekki að keyra kraftmikla áætlun til að sjá CTP niðurstöðurnar.)

Til að tryggja að dagsetningar séu tiltækar tímanlega fyrir alla notendur mælum við með að þú setjir upp runuvinnu til að keyra viðeigandi áætlanir reglulega. Til dæmis, runuvinna sem er sett upp til að keyra kraftmikla áætlun á 30 mínútna fresti mun setja staðfesta skipið og fá dagsetningar á 30 mínútna fresti. Þess vegna þurfa notendur sem setja inn og flytja inn pantanir að hámarki að bíða í 30 mínútur til að fá staðfesta skipið og fá dagsetningar.

Fylgdu þessum skrefum til að setja upp runuvinnu til að keyra kraftmikla áætlun á reglulegri áætlun.

1. Fara til **Aðalskipulag \> Aðalskipulag \> Hlaupa \> Aðalskipulag**.
1. Í **Aðalskipulag** valmynd, á **Færibreytur** flýtiflipann, stilltu **Snilldaráætlun** reit í kraftmiklu áætlunina sem þú vilt keyra.
1. Á **Hlaupa í bakgrunni** flýtiflipann, stilltu **Lotuvinnsla** valmöguleika til *Já*.
1. Veldu **Endurkoma**, og settu upp áætlunina eftir þörfum.
1. Veldu **Allt í lagi** til að vista áætlunina.
1. Veldu **Allt í lagi** til að búa til runuvinnuna og loka glugganum.

## <a name="use-ctp-for-built-in-master-planning"></a>Notaðu CTP fyrir innbyggða aðalskipulagningu

### <a name="create-a-new-order-by-using-ctp-for-built-in-master-planning"></a>Búðu til nýja pöntun með því að nota CTP fyrir innbyggða aðalskipulagningu

Í hvert skipti sem þú bætir við nýrri sölupöntun eða pöntunarlínu, úthlutar kerfið sjálfgefna afhendingardagsetningaraðferð til þess. Pöntunarhausinn byrjar alltaf á alþjóðlegu sjálfgefna aðferðinni. Ef hnekkja er úthlutað á pantaða vöru mun nýja pöntunarlínan nota þá hnekun. Annars mun nýja pöntunarlínan einnig nota alþjóðlegu sjálfgefna aðferðina. Þess vegna ættir þú að stilla sjálfgefnar aðferðir þannig að þær passi við afhendingardagsetningaraðferðina sem þú notar oftast. Eftir að þú hefur búið til pöntun geturðu hnekkt sjálfgefna aðferð á pöntunarhaus og/eða pöntunarlínustigi eins og þú þarfnast. Fyrir frekari upplýsingar, sjá [Stilltu sjálfgefna afhendingardagsetningaraðferðir](#default-methods) og [Breyttu núverandi sölupöntunum til að nota CTP](#change-orders).

### <a name="view-confirmed-delivery-dates-when-you-use-ctp-for-built-in-master-planning"></a>Skoðaðu staðfesta afhendingardagsetningar þegar þú notar CTP fyrir innbyggða aðalskipulagningu

Ef þú ert að nota innbyggðu aðalskipulagsvélina er CTP útreikningum beitt á pantanir og/eða pöntunarlínur þar sem **Stýring á afhendingardagsetningu** reiturinn er stilltur á *CTP*.

Fyrir sölulínur sem nota CTP fyrir innbyggða aðalskipulagningu, stillir kerfið sjálfkrafa **Staðfest sendingardagsetning** og **Staðfest móttökudagsetning** reiti í hvert skipti sem þú vistar sölulínu. Ef þú gerir síðar viðeigandi breytingu á sölulínu (til dæmis með því að breyta magni hennar eða síðu) verða dagsetningarnar strax endurreiknaðar.

- Til að skoða staðfestar afhendingardagsetningar fyrir sölupöntunarlínu, opnaðu sölupöntunina og veldu sölulínuna. Síðan, á **Upplýsingar um línu** flýtiflipann, á **Afhending** flipann, skoðaðu **Staðfest sendingardagsetning** og **Staðfest móttökudagsetning** gildi.
- Til að skoða staðfestar afhendingardagsetningar fyrir heila pöntun skaltu opna sölupöntunina og velja **Fyrirsögn** útsýni. Síðan, á **Afhending** Flýtiflipi, skoðaðu **Staðfest sendingardagsetning** og **Staðfest móttökudagsetning** gildi.

## <a name="use-ctp-for-planning-optimization"></a>Notaðu CTP til að hagræða skipulagningu

### <a name="create-a-new-order-by-using-ctp-for-planning-optimization"></a>Búðu til nýja pöntun með því að nota CTP fyrir áætlanagerð fínstillingu

Í hvert skipti sem þú bætir við nýrri sölupöntun eða pöntunarlínu, úthlutar kerfið sjálfgefna afhendingardagsetningaraðferð til þess. Pöntunarhausinn byrjar alltaf á alþjóðlegu sjálfgefna aðferðinni. Ef hnekkja er úthlutað á pantaða vöru mun nýja pöntunarlínan nota þá hnekun. Annars mun nýja pöntunarlínan einnig nota alþjóðlegu sjálfgefna aðferðina. Þess vegna ættir þú að stilla sjálfgefnar aðferðir þannig að þær passi við afhendingardagsetningaraðferðina sem þú notar oftast. Eftir að þú hefur búið til pöntun geturðu hnekkt sjálfgefna aðferð á pöntunarhaus og/eða pöntunarlínustigi eins og þú þarfnast. Fyrir frekari upplýsingar, sjá [Stilltu sjálfgefna afhendingardagsetningaraðferðir](#default-methods) og [Breyttu núverandi sölupöntunum til að nota CTP](#change-orders).

### <a name="view-confirmed-delivery-dates-when-using-ctp-for-planning-optimization"></a>Skoðaðu staðfesta afhendingardagsetningar þegar þú notar CTP fyrir áætlanagerð fínstillingu

Ef þú ert að nota hagræðingu áætlanagerðar, eru CTP útreikningar notaðir á pantanir og/eða pöntunarlínur þar sem **Stýring á afhendingardagsetningu** reiturinn er stilltur á *CTP fyrir hagræðingu áætlanagerðar*.

Fyrir sölulínur sem nota CTP fyrir hagræðingu áætlanagerðar, **Staðfest sendingardagsetning** og **Staðfest móttökudagsetning** reitirnir verða auðir þar til þú keyrir viðeigandi kraftmikla áætlun (venjulega með því að nota reglubundið runuverk). Þeir eru þá sjálfkrafa stilltir. Fyrir frekari upplýsingar sjá [Tímasettu CTP fyrir útreikninga á hagræðingu áætlanagerðar](#batch-job).

The **CTP fyrir áætlanagerð hagræðingu stöðu** reiturinn gefur til kynna hvort staðfestar dagsetningar hafi verið reiknaðar út fyrir hverja línu sem notar CTP fyrir áætlanagerð fínstillingu. Reiturinn sýnir gildi fyrir *Ekki tilbúinn* fyrir línur og pantanir þar sem staðfestir afhendingardagar hafa annaðhvort ekki verið reiknaðir út eða eru ekki lengur í gildi vegna annarra breytinga. Það sýnir gildi á *Tilbúið* fyrir línur og pantanir sem hafa verið reiknaðar. Hægt er að skoða stöðuna fyrir hverja línu og fyrir alla pöntunina.

- Til að skoða stöðu sölupöntunarlínu, opnaðu sölupöntunina og veldu sölulínuna. Síðan, á **Upplýsingar um línu** flýtiflipann, á **Afhending** flipann, skoðaðu **CTP fyrir áætlanagerð hagræðingu stöðu** gildi. The **Staðfest sendingardagsetning** og **Staðfest móttökudagsetning** reitir fyrir línuna eru einnig sýndir á þessum flipa eftir að þeir hafa verið reiknaðir út.
- Til að skoða stöðu fyrir heila pöntun skaltu opna sölupöntunina og velja **Fyrirsögn** útsýni. Síðan, á **Afhending** Flýtiflipi, skoðaðu **CTP fyrir áætlanagerð hagræðingu stöðu** gildi. The **Staðfest sendingardagsetning** og **Staðfest móttökudagsetning** fyrir röð eru einnig sýndar á þessum flipa eftir að þær hafa verið reiknaðar.

<!-- KFM: The following text may be untrue and needs to be reviewed with the PM for next revision:

The sales orders that are *Ready* or *Not ready* are shown in the **All sales orders** list page. You can check the sales order that are *Ready* or *Not ready* from the sales order list page by filtering on this new status field.

-->

> [!NOTE]
> - Ef þú uppfærir sölupöntunarlínu eftir að CTP for Planning Optimization hefur reiknað út staðfestar dagsetningar fyrir hana, mun kerfið hreinsa þessar dagsetningar þar til næst þegar viðeigandi kraftmikil áætlun er keyrð.
> - Ef þú breytir tengdri stillingu sem gæti haft áhrif á núverandi staðfestar dagsetningar (til dæmis með því að breyta afgreiðslutíma, pöntunum eða merkingum), ættir þú að hreinsa staðfestar dagsetningar fyrir viðeigandi fyrirliggjandi pantanir. Þessi aðgerð mun valda því að stöðu hverrar viðeigandi línu verður breytt í *Ekki tilbúinn*. Þessi breyting mun aftur á móti valda því að kerfið endurreikur staðfestar dagsetningar næst þegar það keyrir kraftmiklu áætlunina.

## <a name="change-existing-sales-orders-so-that-they-use-ctp"></a><a name="change-orders"></a> Breyta núverandi sölupöntunum þannig að þær noti CTP

Þú getur breytt **Stýring á afhendingardagsetningu** gildi fyrir hvaða opna pöntun hvenær sem er. Þú getur breytt gildinu á hausstigi og/eða fyrir hverja línu eftir þörfum.

### <a name="change-to-ctp-at-the-order-header-level"></a>Breyttu í CTP á pöntunarhausstigi

<!-- KFM: Would be nice to mention how changing this setting on the header affects the individual lines. -->

Til að breyta pöntun þannig að hún noti CTP á pöntunarhausstigi skaltu fylgja þessum skrefum.

1. Opna **Viðskiptakröfur \> Pantanir \> Allar sölupantanir**.
1. Opnaðu sölupöntunina sem þú vilt setja upp eða búðu til nýja.
1. Veldu **Fyrirsögn** til að opna hausupplýsingarnar á **Upplýsingar um sölupöntun** síðu.
1. Á **Afhending** flýtiflipann, stilltu **Stýring á afhendingardagsetningu** reit í eitt af eftirfarandi gildum, allt eftir skipulagsvélinni sem þú ert að nota:

    - *CTP* – Notaðu CTP-útreikninginn sem innbyggða aðalskipulagsvélin veitir. Ef þú ert að nota áætlanagerð hagræðingu, the *CTP* aðferð til að stjórna afhendingardagsetningu er ekki leyfð. Þess vegna, ef þú velur þetta gildi, mun villa koma upp þegar útreikningurinn keyrir.
    - *CTP fyrir hagræðingu áætlanagerðar* – Notaðu CTP-útreikninginn sem er veittur af Planning Optimization. Þessi stilling hefur engin áhrif ef þú ert að nota innbyggðu aðalskipulagsvélina.

<!-- KFM: Additional dialogs are shown here. Review these with the PM and expand this procedure at next revision. -->
1. Veldu **Í lagi** til að gera breytinguna.

### <a name="change-to-ctp-at-the-order-line-level"></a>Breyta í CTP á pöntunarlínustigi

Ef þú bjóst til pöntunarlínu með því að nota aðra afhendingardagastýringaraðferð geturðu breytt í CTP hvenær sem er. Breytingar sem þú gerir á línustigi hafa ekki áhrif á neinar aðrar línur. Hins vegar gætu þær valdið því að heildarafhendingardagsetningar pöntunar færast fram eða aftur, allt eftir því hvernig hver uppfærður línuútreikningur breytist. <!-- KFM: Confirm this intro at next revision -->

Til að breyta pöntun þannig að hún noti CTP fyrir innbyggða aðalskipulagningu á línustigi skal fylgja þessum skrefum.

1. Opna **Viðskiptakröfur \> Pantanir \> Allar sölupantanir**.
1. Opnaðu sölupöntunina sem þú vilt setja upp eða búðu til nýja.
1. Á **Upplýsingar um sölupöntun** síðu, á **Sölupöntunarlína** Flýtiflipi, veldu sölupöntunarlínuna sem þú vilt setja upp.
1. Á **Upplýsingar um línu** flýtiflipann, á **Afhending** flipann, stilltu **Stýring á afhendingardagsetningu** reit í eitt af eftirfarandi gildum, allt eftir skipulagsvélinni sem þú ert að nota:

    - *CTP* – Notaðu CTP-útreikninginn sem innbyggða aðalskipulagsvélin veitir. Ef þú ert að nota áætlanagerð hagræðingu, the *CTP* aðferð til að stjórna afhendingardagsetningu er ekki leyfð. Þess vegna, ef þú velur þetta gildi, mun villa koma upp þegar útreikningurinn keyrir.
    - *CTP fyrir hagræðingu áætlanagerðar* – Notaðu CTP-útreikninginn sem er veittur af Planning Optimization. Þessi stilling hefur engin áhrif ef þú ert að nota innbyggðu aðalskipulagsvélina.

    The **Tiltækar sendingar- og kvittunardagsetningar** svarglugginn birtist og sýnir tiltækar skips- og kvittunardagsetningar. Þessi svargluggi virkar á sama hátt fyrir pöntunarlínur og hann gerir fyrir pöntunarhaus, eins og lýst er í fyrri hlutanum.

1. Í aðgerðarúðunni skal velja **Vista**.
