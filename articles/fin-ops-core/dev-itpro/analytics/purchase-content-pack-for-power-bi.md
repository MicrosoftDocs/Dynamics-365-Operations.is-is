---
title: Eyðslugreining innkaupa Power BI efni
description: Þessi grein lýsir því sem er innifalið í innkaupaútgjaldagreiningunni Power BI efni.
author: FrankDahl
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchaseSpendAnalysisPowerBI
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 08937d36be27f7b21ab50473715cc155e4fd0c9e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892741"
---
# <a name="purchase-spend-analysis-power-bi-content"></a>Eyðslugreining innkaupa Power BI efni

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því sem er innifalið í **Greining kaupkostnaðar** Microsoft Power BI efni. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.

## <a name="overview"></a>Yfirlit

**Efnispakki eyðslugreiningar innkaupa** Power BI-efni var stofnaður fyrir innkaupastjóra og stjórnendur sem bera ábyrgð á áætlunum. Stjórnendur geta greint útgjöld við innkaup á eftirfarandi hátt:

- Innkaup á árinu (eftir lánardrottnaflokki og stökum lánardrottnum, innkaupategund og stökum afurðum og staðsetningu lánardrottins)
- Breytingar á innkaupum ár frá ári (eftir lánardrottnaflokki og innkaupategund)

Efnið notast við innkaupafærslugögn og gefur bæði samantekið yfirlit yfir innkaupatölur fyrirtækisins og sundurliðun á útgjöldum við innkaup eftir lánardrottnum og afurðum. Skýrslur auðkenna breytingar í útgjöldum innkaupa yfir tíma. Þannig má nota skýrslurnar til að gera stjórnendum viðvart um jákvæða og neikvæða útgjaldaþróun fyrir einstaka lánardrottna og afurðir. Ennfremur sýna gröf innkaupaútgjöld fyrir mismunandi innkaupaflokka og lánardrottnahópa. Því geta flokka- og svæðastjórnendur notað gröfin til að finna breytingar á útgjaldahegðun.

## <a name="accessing-the-power-bi-content"></a>Aðgangur að Power BI efni
**Eyðslugreining innkaupa** Power BI-efni er sýnt á **Greining á innkaupum og eyðslu** síðunni (**Innkaup og aðföng** \> **Fyrirspurnir og skýrslur** \> **Greining á innkaupaárangri** \> **Greining á innkaupum og eyðslu**).

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mælikvarðar sem eru hafðir með í Power BI efni
**Eyðslugreining innkaupa** Power BI efni inniheldur skýrslu sem samanstendur af safni mælikvarða. Þessir mælikvarðar eru birtir sem myndrit, reitir og töflur. 

Eftirfarandi hlutar veita yfirlit yfir myndrænar framsetningar.

### <a name="purchase-by-vendor-report-page"></a>Skýrslusíða fyrir innkaup eftir lánardrottni
**Gröf**
- Efstu 10 lánardrottnar eftir innkaupum (staflað súlurit)
- Samtals innkaup eftir lánardrottnaflokki / landi / heiti (skífurit)
- Innkaup eftir lánardrottnaflokki / landi / heiti (stöplarit)
- Meðaltal innkaupa eftir lánardrottnaflokki / landi / heiti (stöplarit)

**Reitir**
- Heildarinnkaup
- Vöxtur í innkaupum ár frá ári
- Samtala # lánardrottna
- Samtala # virkra lánardrottna

**Dæmi**
<img src="media/spend1.png" alt="Purchase by vendor">

### <a name="purchase-by-product-report-page"></a>Skýrslusíða fyrir innkaup eftir afurðum

**Gröf**
- Innkaup eftir innkaupategund / afurðarheiti (stöplarit)
- Heildarinnkaup eftir innkaupategund / afurðarheiti (skífurit)
- Efstu 10 afurðir eftir innkaupum (staflað súlurit)

**Reitir**
- Samtala # afurða</li>
- Samtala prósentu virkra afurða af samtölu # afurða
- Fjöldi afurða fyrir 80% innkaupa

**Dæmi**


<img src="media/purchaseByProduct.png" alt="Purchase by Product">

### <a name="purchase-by-period-report-page"></a>Skýrslusíða fyrir innkaup eftir tímabili
Þessi síða sýnir innkaup þessa árs og síðasta árs og vöxtur eftir innkaupategund.

**Gröf** 
- Innkaup eftir mánuði / degi (stöplarit)
- Uppsöfnuð frávik á innkaupum ár frá ári (fossarit)
- Vöxtur í heildarinnkaupum ár frá ári (stöplarit)
- Innkaupayfirlit (fylki)

**Reitir**
- Vöxtur í innkaupum ár frá ári
- Ár frá ári vöxtur í innkaupum

**Dæmi**
<img src="media/purchaseByPeriod.png" alt="Purchase by Period">

### <a name="purchase-by-vendor-location-report-page"></a>Skýrslusíða fyrir innkaup eftir staðsetningu lánardrottins

**Gröf**
- Innkaup eftir borg
- Vöxtur í innkaupum ár frá ári í %
- Innkaup eftir landi

**Dæmi**
<img src="media/purchByVendorLocation.png" alt="Purchase by Vendor Location">

### <a name="purchase-spend-analysis-by-time-report-page"></a>Skýrslusíða fyrir eyðslugreiningu innkaupa eftir tíma

**Gröf** 
- Innkaup núverandi árs eftir mánuðum / degi (línurit)
- Innkaup núverandi og síðasta árs (línu- og stöplarit)

**Dæmi**
<img src="media/PurchByTIme.png" alt="Purchase by Time">

### <a name="purchase-spend-analysis-by-vendor-report-page"></a>Skýrslusíða fyrir eyðslugreiningu innkaupa eftir lánardrottni

**Gröf** 
- Efstu 10 innkaup lánardrottna % innkaupa (trekt)
- Efstu 10 lánardrottnar með aukna eyðslu ár frá ári
- Efstu 10 lánardrottnar með minnkaða eyðslu ár frá ári

**Dæmi** 
<img src="media/PurchSpendAnalysisByVendor.png" alt="Purchase spend by vendor">


## <a name="data-model-and-entities"></a>Gagnalíkan og einingar
Eftirfarandi gögn eru notuð til að fylla út skýrslusíður í **Eyðslugreining innkaupa** Power BI efni. Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni. Einingaverslunin er Microsoft SQL Server gagnagrunnur sem er fínstillt fyrir greiningar. Nánari upplýsingar er að finna í [Power BI samþætting við einingaverslun](power-bi-integration-entity-store.md).

Uppsafnaðar mælingar í þessum efnispakka eru undirflokkur uppsafnaðra mælinga sem voru tiltækar í Innkaupateningur í Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3. Til að stilla uppsafnaðar mælingar tenings í einingaverslun verður að gera þær virkjanlegir. Sjá frekari upplýsingar um ferli fyrir sviðsetningu uppsafnaðra mælinga í einingarverlsun í [Power BI-samþættingu við einingaverslun](power-bi-integration-entity-store.md). Eftirfarandi uppsafnaðar lykilmælingar eru tiltækar beint úr reikningslínueiningunni og eru grunnur þessa efnispakka.

| Eining        | Lykiluppsafnaðar mælingar | Uppruni gagna                                 | Svæði              | lýsing                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| Reikningslínur | Innkaup                   | VendInvoiceTrans                            | SAMTALA(LineAmountMST) | Upphæðin í bókhaldsgjaldmiðli. |

Eftirfarandi tafla sýnir lykilmælingarnar í efnispakkanum sem eru reiknaðar úr reikningslínueiningunni.

| Mæla               | Útreikningur                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Innkaup núverandi árs | Innkaup núverandi árs = SAMTALA ('Reikningslínur'\[Innkaupa\])                                            |
| Innkaup síðasta árs    | Innkaup síðasta ár = REIKNA (SAMTALA ('Reikningslínur'\[Innkaupa\]), SAMEPERIODLASTYEAR (Dagsetningar\[Dagsetning\])) |
| Vöxtur í innkaupum ár frá ári   | Vöxtur í innkaupum ár frá ári = \[Innkaupa núverandi árs\] – \[Innkaupa síðasta árs\]                            |

Eftirfarandi lykilvíddir í efnispakkanum eru notaðar sem síur til að sneiða uppsafnaðar mælingar þannig að hægt sé að ná meiri uppskiptingu og öðlast dýpri greiningarinnsýn.

| Eining                 | Dæmi um eigindir                                |
|------------------------|-------------------------------------------------------|
| Lánardrottnar                | Lánardrottnaflokkar, Lánardrottnaland eða -svæði, nafn Lánardrottins |
| Afurðir               | Afurðarnúmer, afurðarheiti, heiti vöruflokka        |
| Innkaupaflokkar | Innkaupategund, nöfn innkaupategunda      |
| Lögaðilar         | Heiti lögaðila                                     |
| Dagsetningar                  | Dagsetningar, Mótbókun árs                                    |

Sjálfgefið er að efnispakkinn sýni gögn fyrir núgildandi almanaksár. Hins vegar er hægt að breyta dagsetningasíunni í síuhluta skýrslu. Einnig er hægt að breyta síu fyrirtækisins.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]