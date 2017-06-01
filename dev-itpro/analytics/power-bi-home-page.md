---
title: "Heimasíða Power BI"
description: "Þetta efnisatriði telur upp tilföng til aðstoðar við að nota Power BI með Dynamics 365 for Operations."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations
ms.custom: 265694
ms.assetid: 0095a7cf-8cc9-41f6-bf00-b59868fa6ea2
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 711a2e18a692d7f4d048109fdd97497483ce05e8
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="power-bi-home-page"></a>Heimasíða Power BI

[!include[banner](../includes/banner.md)]


Þetta efnisatriði telur upp tilföng til aðstoðar við að nota Power BI með Dynamics 365 for Operations.

<a name="power-bi-content-for-dynamics-365-for-operations"></a>Power BI efni fyrir Dynamics 365 for Operations
------------------------------------------------

| **Eiginleikasvæði**                  | **Power BI-efni**                          | **Hvar á að finna Power BI efni**                                                                                                                                                                                         | **Frekari upplýsingar**                                                                                                                                                               |
|-----------------------------------|-----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fjármálastjórnun              | Fjárhagsleg frammistaða                         | Microsoft Dynamics Lifecycle Services (LCS) (Þessi útgáfa af efnispakka styður Dynamics 365 for Operations útgáfu 1611.) PowerBI.com (Þessi útgáfa af efnispakka styður Microsoft Dynamics 365 for Operations 7.0 og 7.0.1.) | [Power BI-efni fjárhagslegrar frammistöðu](financial-performance-power-bi-content-pack.md)                                               |
|                                   | Skulda- og innheimtuumsjón             | LCS                                                                                                                                                                                                                            |                                                                                                                                                                              |
| Mannauðsstjórnun          | Ráðningarskýrslur                            | LCS                                                                                                                                                                                                                            | [Ráða Power BI-efni](recruiting-analysis-power-bi-content-pack.md)                                                       |
|                                   | Hæfni starfsmanna og þróunarskýrslur | LCS                                                                                                                                                                                                                            | [Hæfni starfsmanna og þróun Power BI-efnis](employee-competencies-and-development-analysis-power-bi-content-pack.md) |
|                                   | Þjálfunarskýrslur fyrirtækis               | LCS                                                                                                                                                                                                                            | [Þjálfun fyrirtækis Power BI efni](organizational-training-analysis-power-bi-content-pack.md)                             |
|                                   | Mælikvarðar vinnuafls                             | LCS                                                                                                                                                                                                                            | [Mælikvarðar vinnuafls Power BI-efni](workforce-analysis-power-bi-content-pack.md)                                                 |
|                                   | Launa- og fríðindaskýrslur             | LCS                                                                                                                                                                                                                            | [Laun og fríðindi Power BI efni](compensation-and-benefits-analysis-power-bi-content-pack.md)                         |
| Verkefnastjórnun og bókhald | Aðferðastjóri                              | LCS                                                                                                                                                                                                                            |                                                                                                                                                                              |
| Smásala og viðskipti               | Afköst smásölurásar                    | PowerBI.com                                                                                                                                                                                                                    | [Power BI-efni afkasta smásölurásar](retail-channel-performance-dashboard-power-bi-data.md)                 |
| Afgreiðslustjórnun           | Kostnaðarstýring                               | PowerBI.com                                                                                                                                                                                                                    |  [Kostnaðarstjórnun Power BI efni](cost-management-content-pack.md)                                                          |
|                                   | Sölu- og arðsemisframmistaða           | LCS                                                                                                                                                                                                                            | [Sölu- og afköst arðsemisgreiningar Power BI-efni](sales-profitability-performance-content-pack.md)          |
|                                   | Eyðslugreining innkaupa                       | LCS                                                                                                                                                                                                                            | [Eyðslugreining innkaupa Power BI efni](purchase-content-pack-for-power-bi.md)                                                 |
|                                   | Kostnaðarbókhaldsgreining                      | LCS                                                                                                                                                                                                                            | [Kostnaðarbókhaldsgreining Power BI-efni](cost-accounting-analysis-content-pack.md)                                         |
|                                   | Afköst vöruhúss                         | LCS                                                                                                                                                                                                                            |                                                                                                                                                                              |
|                                   | Framleiðsluafköst                        | LCS                                                                                                                                                                                                                            |                                                                                                                                                                              |

## <a name="access-power-bi-content-from-lcs"></a>Aðgangur Power BI efnis úr LCS
Upplýsingar um hvernig á að sækja Power BI efni og tengja það við gögn fyrirtækisins er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](power-bi-content-microsoft-partners.md).

## <a name="access-power-bi-content-from-powerbicom"></a>Aðgangur Power BI efni úr PowerBI.com
1.  Innskráning á [PowerBI.com](https://www.powerbi.com/).
2.  Smellið á **Sækja gögn**.
3.  Í **Þjónusta** reitnum smellirðu á **Sækja**.
4.  Breytið þeim eiginleikum sem á að breyta og smellið svo á **Sækja**.
5.  Færa skal inn vefslóð Dynamics 365 for Operations umhverfis. Slóðin verður að vera á sniðinu **https://&lt;YourAOSTenant&gt;.cloudax.dynamics.com**. Smelltu á **Næsta**.
6.  Veldu **oAuth2** sem sannvottunaraðferð og smelltu svo á **innskráning**.
7.  Þegar beðið er u m það skal færa inn Microsoft Office 365 lykil sem hefur leyfi til að fá aðgang að Dynamics 365 for Operations umhverfi.
8.  Eftir að notandi hefur verið skráður inn hefst innflutningsferlið sjálfkrafa. Þegar innflutningi er lokið birtast skýrslur sem eru hafðar með í efnispakka í yfirlitssvæðinu. Veljið skýrslu til að skoða innflutt gögn.

## <a name="learn-more-about-the-power-bi-integration"></a>Frekari upplýsingar um samþættingu Power BI
-   [Power BI-samþætting](power-bi-integration.md)
-   [Yfirlit yfir samþættingu Power BI við einingaverslun](power-bi-integration-entity-store.md)
-   [Semja og dreifa Power BI skýrslum með einingaverslun](author-distribute-power-bi-reports.md)
-   [Festa Power BI skýrslur á vinnusvæði](pin-power-bi-reports.md)
-   [BI power efni í LCS frá Microsoft og viðskiptaaðilum þínum](power-bi-content-microsoft-partners.md)
-   [Nota skilgreiningu Rafræna skýrslugerð til að gefa Power BI gögnum úr Dynamics 365 for Operations](general-electronic-reporting-report-configuration-get-data-powerbi.md)







