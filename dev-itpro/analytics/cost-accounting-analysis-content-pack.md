---
title: "Kostnaðarbókhaldsgreining Power BI-efni"
description: "Þetta efnisatriði lýsir því hvað er innifalið í Power BI-efni greiningar kostnaðarbókhalds. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 270274
ms.assetid: b74549df-35d5-4f2f-b3c7-405b0d38ea78
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 5ce75a6145bde4a8c33ed785c7d2a60a52416676
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="cost-accounting-analysis-power-bi-content"></a>Kostnaðarbókhaldsgreining Power BI-efni

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir því hvað er innifalið í Power BI-efni greiningar kostnaðarbókhalds. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið.

<a name="overview"></a>Yfirlit
--------

Microsoft Power BI-efnið **Greining kostnaðarbókhalds** er ætlað fyrir kostnaðarstýringu eða alla sem bera ábyrgð á framkvæmd kostnaðarstýring af fyrirtæki. Það inniheldur lykilmælikvarða, eins og kostnaður, Mæligildi, og kostnaðarhlutfall eftir raunverulegur kostnaður, kostnað fjárhagsáætlunar og sveigjanleg áætlun kostnaður. Það notar færslugögn frá Kostnaðarbókhald í Microsoft Dynamics 365 for Operations og veitir samanlagt yfirlit yfir kostnaður fyrir allt fyrirtæki í einum skýrslugjaldmiðill. Stjórnendur getur síað gögnin eftir kostnaðarhlutur til að framkvæma kostnaðarstýringu á skipulagseiningum þess, jafnvel þó að fyrirtæki geti haft nokkra lögaðilar. Þar sem Power BI-efni **Kostnaðarbókhald greining** auðkenni frávik milli raunverulegs kostnaður og fjárhagsáætlun kostnaður er hægt að tilkynna stjórnendum um jákvæða og neikvæða þróun fyrir skipulagseiningarnar. Stjórnendur geta kafa niður í stigveldi kostnaðareiningar eða stakar kostnaðareining til að fá sundurliðaða innsýn í hvernig kostnaðarfrávik hafa komið upp og síðan tekið skilvirka aðgerð. Power BI-efnið **Kostnaðarbókhald greining** gerir kostnaðarbókurum kleift að greina hvernig kostnaður flæðir í gegnum kostnaðarhluti alls fyrirtæki. Í frekari upplýsingar um Kostnaðarbókhald, sjá [Kostnaðarbókhald heimasíða](/dynamics365/operations/financials/cost-accounting/cost-accounting-home-page). Með því að skilgreina öryggi á aðgangsstigi í Kostnaðarbókhaldi og sameina það við öryggi á línustigi í Power BI, er hægt að veita öllum eigendum kostnaðarhluta aðgang í Power BI-efni **Kostnaðarbókhald greining**. Öll gögn í myndbirtingar verða síðan afmörkuð á grunni þess aðgangsstig sem er stjórnað í Kostnaðarbókhald. Frekari upplýsingar um öryggi á aðgangsstigi og öryggi línutstigi, sjá [Öryggi sett upp fyrir Power BI-efni kostnaðarbókhalds](setup-security-cost-accounting-content-pack.md).

## <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni
Hægt er að finna Power BI-efnið **Greining kostnaðarbókhalds** í safninu Samnýttar eignar í Microsoft Dynamics Lifecycle Services (LCS). Upplýsingar um hvernig á að sækja efnið og tengja það við gögn Dynamics 365 for Operations er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](power-bi-content-microsoft-partners.md). 

> ATHUGIÐ - **KB4011327** er forskilyrði fyrir þetta Power BI efni. Eftir að þú skrá inn á Lifecycle Services, hefurðu aðgang að KB hér: <https://fix.lcs.dynamics.com/issue/results/?q=kb4011327>.

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
Gögn Dynamics 365 for Operations eru notuð til að fylla út skýrslusíður í Power BI-efni **Greiningar kostnaðarbókhalds**. Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni sem Microsoft SQL-gagnagrunnur sem er fínstilltur fyrir greiningu. Frekari upplýsingar eru í [Yfirlit yfir samþættingu Power BI við einingaverslun](power-bi-integration-entity-store.md) Eftirfarandi lykiluppsafnaðar mælingar eru notaðar sem grunnur að efninu.

| Eining                  | Lykiluppsafnaðar mælingar | Gagnaveita fyrir Dynamics 365 for Operations | Svæði     | lýsing                                   |
|-------------------------|---------------------------|---------------------------------------------|-----------|-----------------------------------------------|
| Færslur kostnaðarbókhaldsgreiningar | SUM(uppphæð)               | CAMDATAAggregatedCostEntry                  | Upphæð    | Upphæð í gjaldmiðði fjárhagur kostnaðarbókhalds |
| Tölfræðilegar færslur     | SUM(Mæligildi)            | CAMDATAAggregatedStatisctialEntry           | Mæligildi |                                               |

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

## <a name="additional-resources"></a>Frekari upplýsingar
Hér eru gagnlegir tenglar sem tengjast einingar og að búa til Power BI-efni:

-   [Gagnaeiningar](..\data-entities\data-entities.md)
-   [Stofnun efnispakka fyrirtækis ](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gera gagnalíkön með því að nota Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Bæta Power BI-reitum við vinnusvæði](configure-power-bi-integration.md)
-   [Uppsetning öryggis fyrir Power BI-efni kostnaðarbókhalds](setup-security-cost-accounting-content-pack.md)




