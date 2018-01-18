---
title: "Kostnaðarbókhaldsgreining Power BI-efni"
description: "Þetta efnisatriði lýsir því hvað er innifalið í Power BI-efni greiningar kostnaðarbókhalds. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið."
author: AndersGirke
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: aac6439bb54b3b9cab066b06c01763e880efef8e
ms.openlocfilehash: 2d0fb4de84838f1778625d977bdd2ceeaac61f8c
ms.contentlocale: is-is
ms.lasthandoff: 12/18/2017

---

# <a name="cost-accounting-analysis-power-bi-content"></a>Kostnaðarbókhaldsgreining Power BI-efni

[!include[banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvað er innifalið í **Greining kostnaðarbókhalds** í efni Microsoft Power BI. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.

## <a name="overview"></a>Yfirlit

**Greining kostnaðarbókhalds** í Power BI er ætlað fyrir kostnaðarstýringu eða alla sem bera ábyrgð á framkvæmd kostnaðarstýringar fyrirtækis. Það inniheldur lykilmælikvarða, eins og kostnaður, Mæligildi, og kostnaðarhlutfall eftir raunverulegur kostnaður, kostnað fjárhagsáætlunar og sveigjanleg áætlun kostnaður. Það notar færslugögn úr einingunni **Kostnaðarbókhald** og veitir samanlagt yfirlit yfir kostnað fyrir allt fyrirtækið í einum skýrslugjaldmiðli. Stjórnendur getur síað gögnin eftir kostnaðarhlutur til að framkvæma kostnaðarstýringu á skipulagseiningum þess, jafnvel þó að fyrirtæki geti haft nokkra lögaðilar. 

Þar sem **Greining kostnaðarbókhalds** sýnir muninn milli raunverulegs og áætlaðs kostnaðar, geta stjórnendur verið upplýstir um jákvæða og neikvæða þróun innan sinnar rekstrareiningar. Stjórnendur geta kafað niður í stigveldi kostnaðareininga eða stakar kostnaðareiningar. Þannig geta stjórnendur öðlast mikið innsæi í hvernig kostnaðarfrávik eru tilkomin og gripið svo til viðeigandi ráðstafana. 

**Greining kostnaðarbókhalds** gerir kostnaðarbókurum kleift að greina hvernig kostnaður flæðir í gegnum kostnaðarhluti alls fyrirtækisins. 

Í frekari upplýsingar um Kostnaðarbókhald, sjá [Kostnaðarbókhald heimasíða](../../financials/cost-accounting/cost-accounting-home-page.md). 

Með því að skilgreina öryggi á aðgangsstigi í Kostnaðarbókhaldi og sameina það við öryggi á línustigi í Power BI, er hægt að veita öllum eigendum kostnaðarhluta aðgang í Power BI-efni **Kostnaðarbókhald greining**. Öll gögn í myndbirtingar verða síðan afmörkuð á grunni þess aðgangsstig sem er stjórnað í Kostnaðarbókhald. Frekari upplýsingar um öryggi á aðgangsstigi og öryggi línutstigi, sjá [Öryggi sett upp fyrir Power BI-efni kostnaðarbókhalds](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni
Hægt er að finna Power BI-efnið **Greining kostnaðarbókhalds** í safninu Samnýttar eignar í Microsoft Dynamics Lifecycle Services (LCS). Upplýsingar um hvernig á að sækja efnið og innleiða það í fyrirtæki er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/12/12/power-bi-content-from-microsoft-and-your-partners/). Til að sjá sýningarmyndband um hvernig innleiða á Power BI-efnið, sjá [Power BI-efni frá Microsoft og samstarfsaðilum þínum í Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w) í Office Mix.

Hlaða skal niður efninu **Greining kostnaðarbókhalds** sem á við um þá útgáfu Microsoft Dynamics 365 sem verið er að nota.

> [!NOTE]
> KB 4011327 er forskilyrði fyrir þetta Power BI-efni. Eftir að þú hefur skráð þig inn í LCS, hefurðu aðgang að KB hér: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mælikvarðar sem eru hafðir með í Power BI-efni
Innihaldið inniheldur hóp af skýrslusíðum. Hver síða samanstendur af safni mælikvarða sem eru sýndir sem myndrit, reitir og töflur. Í eftirfarandi töflu er yfirlit yfir myndbirtingar í Power BI-efni **kostnaðarbókhalds**.

| Skýrslusíða                      | Graf                                                                                                                         | Reitur                                          |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| Kostnaðarstýring eftir fjárhagstímabili    | Raunverulegur kostnaður og Fjárhagsáætlun kostnaður eftir stigveldisstigi Kostnaðareiningar                                                                   | Raunkostnaður á móti kostnað á fjárhagsáætlun                    |
|                                  | Frávik fjárhagsáætlunar eftir stigveldistigi kostnaðareiningar                                                                               | Hlutfall raunkostnaðar á móti hlutfalli kostnaðar fjárhagsáætlunar          |
|                                  | Efstu 10 frávik fjárhagsáætlunar í prósentum eftir kostnaðareiningum                                                                          | Raunmæligildi á móti Fjárhagsáætlun mæligildi          |
| Kostnaðarstýring það sem af er árinu     | Raunverulegur kostnaður og Fjárhagsáætlun kostnaður eftir tímabili almanaksárs                                                                           | Raunkostnaður á móti kostnað á fjárhagsáætlun                    |
|                                  | Frávik fjárhagsáætlunar eftir tímabili almanaksárs                                                                                       | Hlutfall raunkostnaðar á móti hlutfalli kostnaðar fjárhagsáætlunar          |
|                                  | Efstu 10 frávik fjárhagsáætlunar í prósentum eftir kostnaðareiningum                                                                          | Raunmæligildi á móti Fjárhagsáætlun mæligildi          |
| Kostnaðarhlutfall eftir fjárhagsári         | Hlutfall raunkostnaður eftir kostnaðarhegðun                                                                                             | Hlutfall raunkostnaðar á móti hlutfalli kostnaðar fjárhagsáætlunar          |
|                                  | Hlutfall raunkostnaðar, frávik hlutfalls áætlaðs kostnaðar, prósenta hlutfalls áætlaðs kostnaðar eftir stigveldisstigi Kostnaðareiningar | Raunmæligildi á móti Fjárhagsáætlun mæligildi          |
|                                  | Frávik fjárhagsáætlunar eftir stigveldistigi kostnaðareiningar                                                                               |                                               |
|                                  | Efstu 10 frávik fjárhagsáætlunar í prósentum eftir kostnaðareiningum                                                                          |                                               |
| Sveigjanleg áætlun eftir fjárhagstímabili | Raunkostnaður, Fjárhagsáætlun kostnaður og sveigjanleg áætlun eftir stigveldisstigi Kostnaðareiningar                                             | Raunmæligildi á móti Fjárhagsáætlun mæligildi          |
|                                  | Frávik fjárhagsáætlunar og frávik sveigjanleg áætlun eftir stigveldistigi kostnaðareiningar                                                  | Raunkostnaður á móti kostnaði sveigjanleg áætlun           |
|                                  | Raunkostnaður, Fjárhagsáætlun kostnaður og sveigjanlegur kostnaður eftir kostnaðarhegðun og stigveldisstigi Kostnaðareiningar                                  | Hlutfall raunkostnaðar á móti hlutfalli kostnaðar sveigjanleg áætlunar |
| Kostnaðaryfirlit eftir fjárhagstímabili  | Raunverulegur kostnaður eftir stigveldisstigi Kostnaðareiningar og heiti víddarstaks kostnaðarhlutar                                             |                                               |
|                                  | Raunverulegur kostnaður eftir heiti víddarstaks kostnaðarhlutar og heiti víddarstaks kostnaðareiningar                                       |                                               |

## <a name="understanding-the-data-model-and-entities"></a>Skilja gagnalíkan og einingar
Eftirfarandi gögn eru notuð til að fylla út skýrslusíður í **Greining kostnaðarbókhalds** í Power BI. Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni. Entity-verslunin er Microsoft SQL-gagnagrunnur sem er fínstilltur fyrir greiningu. Frekari upplýsingar eru í [Yfirlit yfir samþættingu Power BI við einingaverslun](power-bi-integration-entity-store.md) 

Eftirfarandi lykiluppsafnaðar mælingar eru notaðar sem grunnur að efninu.

| Eining                  | Lykiluppsafnaðar mælingar | Gagnagjafar fyrir Dynamics 365      | Svæði     | lýsing                                        |
|-------------------------|---------------------------|-----------------------------------|-----------|----------------------------------------------------|
| Færslur kostnaðarbókhaldsgreiningar | SUM(uppphæð)               | CAMDATAAggregatedCostEntry        | Upphæð    | Upphæð í fjárhagsgjaldmiðli kostnaðarbókhalds. |
| Tölfræðilegar færslur     | SUM(Mæligildi)            | CAMDATAAggregatedStatisctialEntry | Mæligildi |                                                    |

Eftirfarandi tafla sýnir hvernig lykiluppsafnaðar mælingar eru notaðar til að stofna nokkrar útreikningsmælingar í gagnamengi efnisins.

| Mæla                                       | Hvernig mælieining er reiknuð                                                                                          |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Raunkostnaður                                   | CALCULATE('Cost bókhald færslur'\[Mælieining\], 'Færsla útgáfa'\[ISSOURCEVERSIONBUDGET\_VIRÐI\] = 0)            |
| Áætlaður kostnaður                                   | CALCULATE('Cost bókhald færslur'\[Mælieining\], 'Færsla útgáfa'\[ISSOURCEVERSIONBUDGET\_VIRÐI\] = 1)            |
| Kostnaðarfrávik fjárhagsáætlunar                          | \[Áætlaður kostnaður\] - \[Raunkostnaður\]                                                                                      |
| Prósenta áætlaðs kostnaðar                    | IF(\[Fjárhagsáætlun kostnaður\] = 0, blank(), \[Fjárhagsáætlun frávik\] / \[Fjárhagsáætlun kostnaður\])                                                |
| Raunveruleg mæligildi                              | CALCULATE('Tölfræðilegar færslur'\[Mælieining\], 'Færsla útgáfa'\[ISSOURCEVERSIONBUDGET\_VIRÐI\] = 0)          |
| Áætluð mæligildi                              | CALCULATE(\[Mælieining\], 'Færsla útgáfa'\[ISSOURCEVERSIONBUDGET\_VIRÐI\] = 1)                               |
| Tölfræðileg frávik fjárhagsáætlunar                   | \[Mæligildi fjárhagsáætlunar\] - \[Raunmæligildi\]                                                                            |
| Prósenta tölfræðilegra frávik fjárhagsáætlunar        | IF(\[Mæligildi fjárhagsáætlunar\] = 0, blank(), \[Tölfræðileg frávik fjárhagsáætlunar\] / \[Mæligildi fjárhagsáætlunar\])                          |
| Raunverulegt kostnaðarhlutfall                              | IF(\[Raunmæligildi\] = 0, BLANK(), \[Raunverulegur kostnaður\] / \[Raunmæligildi\])                                          |
| Kostnaðarhlutfall áætlunar                              | IF(\[Mæligildi fjárhagsáætlunar\] = 0, blank(), \[Kostnaður fjárhagsáætlunar\] / \[Mæligildi fjárhagsáætlunar\])                                          |
| Frávik markaðsvaxta kostnaðar fjárhagsáætlunar                     | \[Markaðsvextir kostnaðar fjárhagsáætlunar\] - \[Markaðsvextir raunkostnaðar\]                                                                            |
| Prósenta frávika markaðsvaxta kostnaðar fjárhagsáætlunar          | IF(\[Kostnaður fjárhagsáætlunar\] = 0, blank(), \[frávik markaðsvaxta áætlaðs kostnaðar\] / \[Markaðsvextir kostnaðar fjárhagsáætlunar\])                                 |
| Fastur kostnaður áætlunar                             | CALCULATE(\[Kostnaður fjárhagsáætlunar\], 'Færslur kostnaðarbókhaldsgreiningar'\[COSTBEHAVIOR\] = 1)                                              |
| Breytilegur áætlaður kostnaður                          | CALCULATE(\[Kostnaður fjárhagsáætlunar\], 'Færslur kostnaðarbókhaldsgreiningar'\[COSTBEHAVIOR\] = 2)                                              |
| Fastur kostnaður sveigjanlegrar áætlunar                    | \[Fastur kostnaður fjárhagsáætlunar\]                                                                                                  |
| Breytilegur kostnaður sveigjanlegrar áætlunar                 | IF(\[Mæligildi fjárhagsáætlunar\] = 0, BLANK(), (\[Breytilegur áætlaður kostnaður\] / \[Mæligildi fjárhagsáætlunar\]) \* \[Raunmæligildi\])       |
| Kostnaður sveigjanlegrar áætlunar                          | \[Fastur kostnaður sveigjanlegrar áætlunar\] + \[Breytilegur kostnaður sveigjanlegrar áætlunar\]                                                     |
| Frávik sveigjanlegrar áætlunar                      | \[Kostnaður sveigjanlegrar áætlunar\] - \[Raunkostnaður\]                                                                             |
| Prósenta frávika sveigjanleg áætlunar           | IF(\[Kostnaður sveigjanlegrar áætlunar\] = 0, BLANK(), \[Frávik sveigjanlegrar áætlunar\] / \[Kostnaður sveigjanlegrar áætlunar\])                     |
| Markaðsvextir kostnaðar sveigjanlegrar áætlunar                     | IF(\[Raunveruleg mæligildi\] = 0, BLANK(), \[Kostnaður sveigjanlegrar áætlunar\] / \[Raunveruleg mæligildi\])                                 |
| Frávik markaðsvaxta kostnaðar sveigjanlegrar áætlunar            | \[Markaðsvextir kostnaðar sveigjanlegrar áætlunar\] - \[Markaðsvextir raunkostnaðar\]                                                                   |
| Frávikaprósenta markaðsvaxta kostnaðar sveigjanlegrar áætlunar | IF(\[Markaðsvextir kostnaðar sveigjanlegrar áætlunar\] = 0, BLANK(), \[Frávik markaðsvaxta kostnaðar sveigjanlegrar áætlunar\] / \[Markaðsvextir kostnaðar sveigjanlegrar áætlunar\]) |

Eftirfarandi lykilvíddir eru notaðar sem síur til að sneiða uppsafnaðar mælingar þannig að hægt sé að veita meiri uppskiptingu og dýpri greiningarinnsýn.

| Eining                             | Dæmi um eigindir                                                                                               |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Fjárhagir kostnaðarbókhalds            | Fjárhagur kostnaðarbókhalds                                                                                               |
| Stýrieiningar kostnaðar                 | Heiti stýrieiningar kostnaðar                                                                                               |
| Víddir kostnaðareiningar            | Heiti víddar kostnaðareiningar, Heiti víddarstaks kostnaðareiningar, lýsing víddarstaka kostnaðareiningar.          |
| Víddir kostnaðarhluta             | Heiti víddar kostnaðarhlutar, Heiti víddarstaks kostnaðarhlutar, lýsing víddarstaka kostnaðarhlutar.              |
| Tölfræðilegar víddir             | Heiti tölfræðivíddar, Heiti tölfræðilegs víddarstaks, lýsing Tölfræðilegt víddarstaks              |
| Víddarstigveldi kostnaðarhlutar  | Heiti stigveldis víddar kostnaðarhlutar, stigveldisstig víddar kostnaðarhlutar, lýsing stigveldistrés víddar kostnaðarhlutar.    |
| Víddarstigveldi kostnaðareiningar | Heiti stigveldis víddar kostnaðareiningar, stigveldisstig víddar kostnaðareiningar, lýsing stigveldistrés víddar kostnaðareiningar. |
| Tölfræðileg víddarstigveldi  | Heiti stigveldis tölfræðivíddar, stigveldisstig tölfræðivíddar, lýsing stigveldistrés tölfræðivíddar.    |
| Færsluútgáfur               | Útgáfunafn                                                                                                         |
| Fjárhagsdagatöl                   | Almanak, lýsing almanaks                                                                                       |
| Fjárhagsár                       | Almanaksár                                                                                                        |
| Fjárhagstímabil                     | Tímabil almanaksárs                                                                                                 |

