---
title: "Gögn flutt út fyrir eftirspurnarspár"
description: "Til að fá nákvæmar spár um eftirspurn þarf að hafa söguleg eftirspurnargögn fyrir hverja vöru eða vöruúthlutunarlykil. Þetta efnisatriði útskýrir hvernig á að nota gagnaeiningar til að flytja inn söguleg eftirspurnargögn úr hvaða kerfi sem er þannig að notandi hafi lengri sögu yfir eftirspurnargögn."
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: c46b659a0ecffd6180fd0a76ff1b8d228f121571
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="import-historical-data-for-demand-forecasts"></a><span data-ttu-id="10abb-104">Gögn flutt út fyrir eftirspurnarspár</span><span class="sxs-lookup"><span data-stu-id="10abb-104">Import historical data for demand forecasts</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="10abb-105">Til að tryggja aukna nákvæmni spár um eftirspurn þarf að hafa eins mikið af sögulegum eftirspurnargögnum og hægt er að fá fyrir hverja vöru eða hvern vöruúthlutunarlykil.</span><span class="sxs-lookup"><span data-stu-id="10abb-105">To help guarantee the accuracy of demand forecasts, you must have as much historical demand data as you can get per item or item allocation key.</span></span> <span data-ttu-id="10abb-106">Ef söguleg eftirspurnargögn hafa ekki þegar verið flutt inn skal nota gagnaeininguna **Söguleg ytri eftirspurn** (ReqDemPlanHistoricalExternalDemandEntity) í Microsoft Dynamics 365 for Finance and Operations til að flytja þau inn.</span><span class="sxs-lookup"><span data-stu-id="10abb-106">If the historical demand data isn't already imported, use the **Historical external demand** (ReqDemPlanHistoricalExternalDemandEntity) data entity in Microsoft Dynamics 365 for Finance and Operations to import it.</span></span>

<span data-ttu-id="10abb-107">Á vinnusvæðinu **Gagnastjórnun** er hægt að sjá yfirlit yfir alla reiti í einingunni.</span><span class="sxs-lookup"><span data-stu-id="10abb-107">In the **Data management** workspace, you can see an overview of all the fields in the entity.</span></span>

1. <span data-ttu-id="10abb-108">Opnaðu vinnusvæðið **Gagnastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="10abb-108">Open the **Data management** workspace.</span></span>
2. <span data-ttu-id="10abb-109">Smellið á reitinn **Gagnaeiningar**.</span><span class="sxs-lookup"><span data-stu-id="10abb-109">Click the **Data entities** tile.</span></span>
3. <span data-ttu-id="10abb-110">Leitið í einingalistanum fyrir **Söguleg ytri eftirspurn**.</span><span class="sxs-lookup"><span data-stu-id="10abb-110">Search the entity list for **Historical external demand**.</span></span>
4. <span data-ttu-id="10abb-111">Smellið á **Markreitir**.</span><span class="sxs-lookup"><span data-stu-id="10abb-111">Click **Target fields**.</span></span> <span data-ttu-id="10abb-112">Eftirfarandi einingareitir eru áskildir: vefsvæði (**DeliveringSiteId**), dagsetning (**DemandDate**), magn (**DemandQuantity**) og annað hvort vörunúmer (**ItemNumber**) eða úthlutunarlykill vöru (**ProductAllocationKeyId**).</span><span class="sxs-lookup"><span data-stu-id="10abb-112">The following entity fields are mandatory: site (**DeliveringSiteId**), date (**DemandDate**), quantity (**DemandQuantity**), and either item number (**ItemNumber**) or item allocation key (**ProductAllocationKeyId**).</span></span>

<span data-ttu-id="10abb-113">Til að nota gagnaeininguna verður að hafa annað hvort Microsoft Excel-skrá eða skrá með gildum aðgreindum með kommum (CSV) sem inniheldur sögulegu eftirspurnargögnin.</span><span class="sxs-lookup"><span data-stu-id="10abb-113">To use the data entity, you must have a Microsoft Excel file or comma-separated values (CSV) file that contains the historical demand data.</span></span> <span data-ttu-id="10abb-114">Eftirfarandi dæmi sýnir hvernig á að flytja gögn úr CSV-skrá.</span><span class="sxs-lookup"><span data-stu-id="10abb-114">The following example shows how to import the data from a CSV file.</span></span>

## <a name="example"></a><span data-ttu-id="10abb-115">Dæmi</span><span class="sxs-lookup"><span data-stu-id="10abb-115">Example</span></span>

<span data-ttu-id="10abb-116">Hægt er að nota eftirfarandi skrá sem dæmi.</span><span class="sxs-lookup"><span data-stu-id="10abb-116">You can use the following file as an example.</span></span> <span data-ttu-id="10abb-117">Sæktu [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span><span class="sxs-lookup"><span data-stu-id="10abb-117">Download the [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast).</span></span> <span data-ttu-id="10abb-118">Þessi skrá inniheldur gögn sögulegar eftirspurnar vöru D0001.</span><span class="sxs-lookup"><span data-stu-id="10abb-118">This file contains the historical demand data for item D0001.</span></span> <span data-ttu-id="10abb-119">Hún inniheldur aðeins fyrir eftirfarandi skyldusvæði: svæði, magn og dagsetningu eftirspurnar.</span><span class="sxs-lookup"><span data-stu-id="10abb-119">It contains only the following mandatory fields: site, quantity, and the demand date.</span></span>

1. <span data-ttu-id="10abb-120">Velja fyrirtæki til að flytja söguleg eftirspurnargögn inn í.</span><span class="sxs-lookup"><span data-stu-id="10abb-120">Select the company to import the historical demand data into.</span></span>
2. <span data-ttu-id="10abb-121">Opnaðu vinnusvæðið **Gagnastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="10abb-121">Open the **Data management** workspace.</span></span>
3. <span data-ttu-id="10abb-122">Smellið á reitinn **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="10abb-122">Click the **Import** tile.</span></span>
4. <span data-ttu-id="10abb-123">Færið inn heiti fyrir innflutningsverkið, t.d. **Flytja inn sögulega eftirspurn fyrir vöruna D0001**.</span><span class="sxs-lookup"><span data-stu-id="10abb-123">Enter a name for the import project, such as **Import historical demand for item D0001**.</span></span>
5. <span data-ttu-id="10abb-124">Í reitinn **Snið upprunagagna** skal velja skráarsnið skráarinnar sem þú ert að flytja inn.</span><span class="sxs-lookup"><span data-stu-id="10abb-124">In the **Source data format** field, select the file format of the file that you're importing.</span></span> <span data-ttu-id="10abb-125">Til þess að flytja inn skrána HistoricalDemandData í þessu dæmi skal velja **CSV**.</span><span class="sxs-lookup"><span data-stu-id="10abb-125">To import the HistoricalDemandData file for this example, select **CSV**.</span></span>
6. <span data-ttu-id="10abb-126">Í reitinn **Heiti Einingar** skal velja **Söguleg ytri eftirspurn**.</span><span class="sxs-lookup"><span data-stu-id="10abb-126">In the **Entity name** field, select **Historical external demand**.</span></span>
7. <span data-ttu-id="10abb-127">Vistaðu skrána í tölvunni og hladdu henni svo upp.</span><span class="sxs-lookup"><span data-stu-id="10abb-127">Save the file to your computer, and then upload it.</span></span>
8. <span data-ttu-id="10abb-128">Smelltu á **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="10abb-128">Click **Import**.</span></span>
9. <span data-ttu-id="10abb-129">Síðan **Samantekt framkvæmdar** opnast sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="10abb-129">The **Execution summary** page is opened automatically.</span></span> <span data-ttu-id="10abb-130">Sannprófaðu innfluttu gögnin á síðunni.</span><span class="sxs-lookup"><span data-stu-id="10abb-130">Verify the imported data on the page.</span></span>

<span data-ttu-id="10abb-131">Eftir að söguleg eftirspurnargögn hafa verið flutt inn er hægt að mynda eftirspurnarspá.</span><span class="sxs-lookup"><span data-stu-id="10abb-131">After you've imported the historical demand data, you can generate a demand forecast.</span></span>

## <a name="see-also"></a><span data-ttu-id="10abb-132">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="10abb-132">See also</span></span>

[<span data-ttu-id="10abb-133">Myndun tölfræðilegrar grunnlínuspár</span><span class="sxs-lookup"><span data-stu-id="10abb-133">Generate a statistical baseline forecast</span></span>](generate-statistical-baseline-forecast.md)

