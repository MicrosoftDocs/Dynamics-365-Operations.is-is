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
ms.openlocfilehash: de380113fe951f75c15f9e5526ad2f1f5cc84334
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908881"
---
# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="65ede-104">Gögn flutt út fyrir eftirspurnarspár</span><span class="sxs-lookup"><span data-stu-id="65ede-104">Import historical data for demand forecasts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="65ede-105">Til að tryggja aukna nákvæmni spár um eftirspurn þarf að hafa eins mikið af sögulegum eftirspurnargögnum og hægt er að fá fyrir hverja vöru eða hvern vöruúthlutunarlykil.</span><span class="sxs-lookup"><span data-stu-id="65ede-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="65ede-106">Ef söguleg eftirspurnargögn hafa ekki þegar verið flutt inn skal nota gagnaeininguna **Söguleg ytri eftirspurn** (ReqDemPlanHistoricalExternalDemandEntity) í Dynamics 365 Supply Chain Management til að flytja þau inn.</span><span class="sxs-lookup"><span data-stu-id="65ede-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Dynamics 365 Supply Chain Management to import it.</span></span>

<span data-ttu-id="65ede-107">Á vinnusvæðinu **Gagnastjórnun** er hægt að sjá yfirlit yfir alla reiti í einingunni.</span><span class="sxs-lookup"><span data-stu-id="65ede-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="65ede-108">Opnaðu vinnusvæðið **Gagnastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="65ede-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="65ede-109">Veljið reitinn **Gagnaeiningar**.</span><span class="sxs-lookup"><span data-stu-id="65ede-109">Select the **Data entities** tile.</span></span>
3. <span data-ttu-id="65ede-110">Leitið í einingalistanum fyrir **Söguleg ytri eftirspurn**.</span><span class="sxs-lookup"><span data-stu-id="65ede-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="65ede-111">Veljið **Markreitir**.</span><span class="sxs-lookup"><span data-stu-id="65ede-111">Select **Target fields**.</span></span> <span data-ttu-id="65ede-112">Eftirfarandi einingareitir eru áskildir: vefsvæði (**DeliveringSiteId**), dagsetning (**DemandDate**), magn (**DemandQuantity**) og annað hvort vörunúmer (**ItemNumber**) eða úthlutunarlykill vöru (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="65ede-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="65ede-113">Til að nota gagnaeininguna verður að hafa annað hvort Microsoft Excel-skrá eða skrá með gildum aðgreindum með kommum (CSV) sem inniheldur sögulegu eftirspurnargögnin.</span><span class="sxs-lookup"><span data-stu-id="65ede-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="65ede-114">Eftirfarandi dæmi sýnir hvernig á að flytja gögn úr CSV-skrá.</span><span class="sxs-lookup"><span data-stu-id="65ede-114">The following example shows how to import the data from a CSV file.</span></span>

<span data-ttu-id="65ede-115">Frekari upplýsingar um hvernig á að flytja inn gögn, þar á meðal hvernig á að hreinsa gögn eftir innflutning, má finna í [Yfirlit yfir inn- og útflutningsvinnslu gagna](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) og tengd efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="65ede-115">For more information about how to import data, including how to clean up data after an import, see [Data import and export jobs overview](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md) and its related topics.</span></span>

## <a name="example"></a><span data-ttu-id="65ede-116">Dæmi</span><span class="sxs-lookup"><span data-stu-id="65ede-116">Example</span></span>

<span data-ttu-id="65ede-117">Hægt er að nota eftirfarandi skrá sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="65ede-117">You can use the following file as an example.</span></span> <span data-ttu-id="65ede-118">Sæktu [HistoricalDemandData](/dynamics/s-e/).</span><span class="sxs-lookup"><span data-stu-id="65ede-118">Download the [HistoricalDemandData](/dynamics/s-e/).</span></span> <span data-ttu-id="65ede-119">Þessi skrá inniheldur gögn sögulegar eftirspurnar vöru D0001.</span><span class="sxs-lookup"><span data-stu-id="65ede-119">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="65ede-120">Hún inniheldur aðeins fyrir eftirfarandi skyldusvæði: svæði, magn og dagsetningu eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="65ede-120">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="65ede-121">Velja fyrirtæki til að flytja söguleg eftirspurnargögn inn í.</span><span class="sxs-lookup"><span data-stu-id="65ede-121">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="65ede-122">Opnaðu vinnusvæðið **Gagnastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="65ede-122">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="65ede-123">Veljið reitinn **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="65ede-123">Select the **Import** tile.</span></span>
4. <span data-ttu-id="65ede-124">Færið inn heiti fyrir innflutningsverkið, t.d. **Flytja inn sögulega eftirspurn fyrir vöruna D0001**.</span><span class="sxs-lookup"><span data-stu-id="65ede-124">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="65ede-125">Í reitinn **Snið upprunagagna** skal velja skráarsnið skráarinnar sem þú ert að flytja inn.</span><span class="sxs-lookup"><span data-stu-id="65ede-125">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="65ede-126">Til þess að flytja inn skrána HistoricalDemandData í þessu dæmi skal velja **CSV**.</span><span class="sxs-lookup"><span data-stu-id="65ede-126">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="65ede-127">Í reitinn **Heiti Einingar** skal velja **Söguleg ytri eftirspurn**.</span><span class="sxs-lookup"><span data-stu-id="65ede-127">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="65ede-128">Vistaðu skrána í tölvunni og hladdu henni svo upp.</span><span class="sxs-lookup"><span data-stu-id="65ede-128">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="65ede-129">Velja **Innflutningur**.</span><span class="sxs-lookup"><span data-stu-id="65ede-129">Select **Import**.</span></span>
9. <span data-ttu-id="65ede-130">Síðan **Samantekt framkvæmdar** opnast sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="65ede-130">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="65ede-131">Sannprófaðu innfluttu gögnin á síðunni.</span><span class="sxs-lookup"><span data-stu-id="65ede-131">Verify the imported data on the page.</span></span>

<span data-ttu-id="65ede-132">Eftir að söguleg eftirspurnargögn hafa verið flutt inn er hægt að mynda eftirspurnarspá.</span><span class="sxs-lookup"><span data-stu-id="65ede-132">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="65ede-133">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="65ede-133">Additional resources</span></span>

[<span data-ttu-id="65ede-134">Myndun tölfræðilegrar grunnlínuspár</span><span class="sxs-lookup"><span data-stu-id="65ede-134">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)  
[<span data-ttu-id="65ede-135">Yfirlit yfir inn- og útflutningsvinnslu gagna</span><span class="sxs-lookup"><span data-stu-id="65ede-135">Data import and export jobs overview</span></span>](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]