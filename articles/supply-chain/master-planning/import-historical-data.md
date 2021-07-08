---
title: Gögn flutt út fyrir eftirspurnarspár
description: Til að fá nákvæmar spár um eftirspurn þarf að hafa söguleg eftirspurnargögn fyrir hverja vöru eða vöruúthlutunarlykil. Þetta efnisatriði útskýrir hvernig á að nota gagnaeiningar til að flytja inn söguleg eftirspurnargögn úr hvaða kerfi sem er þannig að notandi hafi lengri sögu yfir eftirspurnargögn.
author: roxanadiaconu
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: kamaybac
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0b04ee246d4c28e934407ccb92d792692cc4347d
ms.sourcegitcommit: cbbb35c71ab4ff1ae08fa4f7cc97019b207246be
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/23/2021
ms.locfileid: "6301651"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="fe395-104">Gögn flutt út fyrir eftirspurnarspár</span><span class="sxs-lookup"><span data-stu-id="fe395-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fe395-105">Til að tryggja aukna nákvæmni spár um eftirspurn þarf að hafa eins mikið af sögulegum eftirspurnargögnum og hægt er að fá fyrir hverja vöru eða hvern vöruúthlutunarlykil.</span><span class="sxs-lookup"><span data-stu-id="fe395-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="fe395-106">Ef söguleg eftirspurnargögn hafa ekki þegar verið flutt inn skal nota gagnaeininguna **Söguleg ytri eftirspurn** (ReqDemPlanHistoricalExternalDemandEntity) í Dynamics 365 Supply Chain Management til að flytja þau inn.</span><span class="sxs-lookup"><span data-stu-id="fe395-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="fe395-107">Á vinnusvæðinu **Gagnastjórnun** er hægt að sjá yfirlit yfir alla reiti í einingunni.</span><span class="sxs-lookup"><span data-stu-id="fe395-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="fe395-108">Opnaðu vinnusvæðið **Gagnastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="fe395-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="fe395-109">Veljið reitinn **Gagnaeiningar**.</span><span class="sxs-lookup"><span data-stu-id="fe395-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="fe395-110">Leitið í einingalistanum fyrir **Söguleg ytri eftirspurn**.</span><span class="sxs-lookup"><span data-stu-id="fe395-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="fe395-111">Veljið **Markreitir**.</span><span class="sxs-lookup"><span data-stu-id="fe395-111">Select **Target fields**.</span></span> <span data-ttu-id="fe395-112">Eftirfarandi einingareitir eru áskildir: vefsvæði (**DeliveringSiteId**), dagsetning (**DemandDate**), magn (**DemandQuantity**) og annað hvort vörunúmer (**ItemNumber**) eða úthlutunarlykill vöru (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="fe395-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="fe395-113">Til að nota gagnaeininguna verður að hafa annað hvort Microsoft Excel-skrá eða skrá með gildum aðgreindum með kommum (CSV) sem inniheldur sögulegu eftirspurnargögnin.</span><span class="sxs-lookup"><span data-stu-id="fe395-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="fe395-114">Eftirfarandi dæmi sýnir hvernig á að flytja gögn úr CSV-skrá.</span><span class="sxs-lookup"><span data-stu-id="fe395-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="fe395-115">Frekari upplýsingar um hvernig á að flytja inn gögn, þar á meðal hvernig á að hreinsa gögn eftir innflutning, má finna í [Yfirlit yfir inn- og útflutningsvinnslu gagna](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) og tengd efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="fe395-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

<span data-ttu-id="fe395-116">Sjá einnig [Myndun tölfræðilegrar grunnlínuspár](generate-statistical-baseline-forecast.md).</span><span class="sxs-lookup"><span data-stu-id="fe395-116">See also [Generate a statistical baseline forecast](generate-statistical-baseline-forecast.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]