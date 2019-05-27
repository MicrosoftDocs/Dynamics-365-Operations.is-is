---
title: Sölu- og arðsemisframmistaða Power BI efni
description: Þetta efnisatriði lýsir því sem er innifalið í Sölu- og arðsemisframmistaða Power BI efni. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.
author: ShylaThompson
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: SalesProfitabilityPerformancePowerBI
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 260674
ms.assetid: ab457f02-929e-4d34-b813-335be3092287
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: cf4d3e12d33b67158ff4f96580b4ac2eb903bb93
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551438"
---
# <a name="sales-and-profitability-performance-power-bi-content"></a>Sölu- og arðsemisframmistaða Power BI efni

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvað er innifalið í **Sölu- og arðsemisframmistöðu** Microsoft Power BI efnis. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.

## <a name="overview"></a>Yfirlit

**Sölu- og arðsemisframmistaða** Power BI efnið var stofnað fyrir sölustjórnendur til að fylgjast með lykilmælikvörðum sölu yfir tekjur, brúttóhagnaði og hagnaðarhlutföllum. Hann notar færslugögn sölu og veitir bæði samanlagt yfirlit yfir sölutölur fyrirtækisins og sundurliðun söluafkomu fyrir viðskiptavini og afurðir.

Skýrslur merkið breytingar á tekjur og hagnað vöxtur tímanum. Þannig má nota skýrslurnar til að gera stjórnendum viðvart um jákvæða og neikvæða þróun fyrir einstaka viðskiptamenn og afurðir. Þar að auki gröf bera saman tekjur og arðsemi framleiðslulíkans mismunandi tegundir og þá viðskiptavinaflokka hvor við aðra. Þar af leiðandi tegund og svæðisbundnum stjórnendur geta auðkenna laggards og leaders. Að lokum setur ítarleg skýrsla upp tekjur viðskiptavinar á móti hagnaðarhlutfalli. Þess vegna hafa yfirmenn reikninga gagnaafritaðan grunn sem þeir geta notað til að fínstilla sölu- og markaðsstarf sitt fyrir hvern viðskiptavin fyrir sig.

Efnið **Sölu- og arðsemisafkoma** gerir sölustjórum kleift að greina söluafkomu á eftirfarandi hátt:

- Tekjur, á árinu (með viðskiptavinaflokk og einstaka viðskiptavini, sölutegundir, og stakar afurðir og landsvæði)
- Tekjubreytingar, ár frá ári (eftir svæði viðskiptavina og söluflokkum)

Hægt er að greina arðsemi á eftirfarandi hátt:

- Brúttóhagnaði og hagnaðarframlegð (með því að flokka viðskiptavina og afurðaflokka sölu)
- Breyting á brúttóframlegð, ár frá ári
- Arðsemi viðskiptavinar (eftir tekjum á móti brúttóframlegð)

## <a name="accessing-the-power-bi-content"></a>Aðgangur að Power BI efni
**Sölu- og arðsemisframmistaða** Power BI-efni er sýnt á **Sölu- og arðsemisframmistaða** síðunni (**Sölu- og markaðsstarf** \> **Fyrirspurnir og skýrslur** \> **Söluárangur** \> **Sölu- og arðsemisframmistaða**).

## <a name="metricsthat-are-included-in-the-power-bi-content"></a>Mælikvarðar sem eru hafðir með í Power BI efni
**Sölu- og arðsemisframmistaða** Power BI efnið inniheldur skýrslu sem samanstendur af safni mælikvarða. Þessir mælikvarðar eru birtir sem myndrit, reitir og töflur. Í eftirfarandi töflu er yfirlit yfir myndbirtingar í efninu.

| Skýrslusíða            | Gröf                                     | Reitir                                                   |
|------------------------|--------------------------------------------|---------------------------------------------------------|
| Tekjur eftir viðskiptavini    | Efstu tíu viðskiptamenn eftir tekjum                | Heildartekjur                                           |
|                        | Heildartekjur eftir viðskiptavinaflokki            | Vöxtur í tekjum ár frá ári                                      |
|                        | Heildartekjur viðskiptavina eftir viðskiptavinaflokki | Brúttóframlegð                                            |
|                        | Tekjur & brúttóframlegð eftir viðskiptavinaflokki   |                                                         |
| Tekjur eftir afurðum     | Tekjur & brúttóframlegð eftir söluflokki   | Samtala \# aukaafurða                                    |
|                        | Efstu tíu afurðir eftir tekjum                 | Heildarfjöldi virkra afurða og prósenta af samtölu |
|                        | Heildartekjur eftir söluflokki            | Fjöldi afurða fyrir 80% tekna           |
| Tekjur eftir tímabili\*    | Tekjur eftir mánuði                           | Vöxtur í tekjum ár frá ári                                      |
|                        | Eftirliggjandi tekjufrávik             | Vöxtur í tekjum ár frá ári %                                    |
|                        | Heildarfrávik sölu eftir landsvæði viðskiptavinar    |                                                         |
| Tekjur eftir staðsetningu    | Sölutekjur eftir borg                      |                                                         |
|                        | Vöxtur í tekjum ár frá ári %                       |                                                         |
|                        | Sölutekjur eftir svæðum                    |                                                         |
| Arðsemi viðskiptavinar | Brúttóframlegð á móti tekjum, viðskiptavinum   | Brúttóhagnaður, brúttóframlegð, vöxtur í tekjum ár frá ári          |
| Arðsemisgreining | Tekjur og brúttóhagnaður eftir mánuði          |                                                         |
|                        | Efstu 15 viðskiptamenn eftir brúttóframlegð           |                                                         |
|                        | Brúttóhagnaður eftir mánuði, ár frá ári                 |                                                         |

\* Tekjur þessa árs og síðasta árs og vöxtur eftir söluflokki.

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Eftirfarandi gögn eru notuð til að fylla út skýrsluna í **Sölu- og arðsemisframmistaða** Power BI efnið. Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni. Einingaverslunin er Microsoft SQL Server gagnagrunnur sem er fínstillt fyrir greiningar. Frekari upplýsingar eru í [Yfirlit yfir samþættingu Power BI við einingaverslun](power-bi-integration-entity-store.md)

Uppsafnaðar mælingar í þessum efnispakka eru undirflokkur uppsafnaðra mælinga sem voru tiltækar í söluteningi í Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3. Til að stilla uppsafnaðar mælingar tenings í einingaverslun verður að gera þær virkjanlegir. Sjá frekari upplýsingar um ferli fyrir sviðsetningu uppsafnaðra mælinga í verslun Einingar í bloggfærslunni [Power BI-samþætting við einingaverslun í Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) fyrir nánari upplýsingar.

Eftirfarandi lykiluppsafnaðar mælingar á reikningslínueiningunni eru notaðar sem grunnur að efninu.

| Eining        | Lykiluppsafnaðar mælingar                   | Gagnagjafar fyrir Dynamics 365 | Svæði                                        | lýsing                                       |
|---------------|----------------------------------------------|------------------------------|----------------------------------------------|---------------------------------------------------|
| Reikningslínur | Tekjur                                      | CustInvoiceTrans             | SAMTALA(LineAmountMST)                           | Upphæðin í bókhaldsgjaldmiðli.            |
|               | Kostnaður seldra vara                           | InventTrans                  | SAMTALA(CostAmountPosted + CostAmountAdjustment) | Samtala kostnaðarupphæð og leiðréttingar.    |
|               | Línuupphæð þóknunar – bókhaldsgjaldmiðill | CustInvoiceTrans             | SUM(CommissAmountMST)                        | Þóknunarupphæð í bókhaldsgjaldmiðlinum. |

Eftirfarandi tafla sýnir lykiluppsafnaðar mælingar reikningslínueiningarinnar sem eru notaðar til að stofna nokkrar útreikningsmælingar í gagnasafni efnis.

| Mæla           | Útreikningur                                                                                      |
|-------------------|--------------------------------------------------------------------------------------------------|
| Brúttóframlegð      | SUM(Tekjur – COGS – Þóknun – Virðisaukaskattur (talinn með í línuupphæð viðskiptavinareiknings))          |
| Brúttóframlegð      | SUM(Brúttóhagnaður/ (Tekjur – Virðisaukaskattur (talinn með í línuupphæð viðskiptavinareiknings)))             |
| Tekjur síðasta árs | Tekjur síðasta árs = REIKNA (SAMTALA ('Reikningslínur'\[Tekjur\]), SAMEPERIODLASTYEAR (Dagsetningar\[Dagsetning\])) |

Eftirfarandi lykilvíddir í söluteningnum eru notaðar sem síur til að sneiða uppsafnaðar mælingar þannig að hægt sé að ná meiri uppskiptingu og öðlast betri innsýn í greiningu.

| Eining           | Dæmi um eigindir                               |
|------------------|------------------------------------------------------|
| Viðskiptavinir        | Viðskiptavinaflokkar, Viðskiptavin svæða, Heimilisfang, Atvinnugrein |
| Afurðir         | Afurðarnúmer, afurðarheiti, heiti vöruflokka       |
| Sölutegundir | Heiti söluflokka                                 |
| Lögaðilar   | Heiti lögaðila                                   |
| Dagsetningar            | Dagsetningar                                                |

Sjálfgefið er að efnispakkinn sýni gögn fyrir núgildandi almanaksár. Hins vegar er hægt að breyta dagsetningasíunni í síuhluta skýrslu. Einnig er hægt að breyta síu fyrirtækisins.
