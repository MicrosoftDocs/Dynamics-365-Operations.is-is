---
title: Kostnaðaráætlun framleiðslupöntunar
description: Þessi grein gefur upplýsingar um mat á framleiðslukostnaði. Mat á framleiðslukostnaði veitir upplýsingar um efnis- og afkastanotkunarkostnað við framleiðslu á vöru í áætluðu framleiðslupöntunarmagni.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93546fc170757ee2c39144842bae12d78400fd32
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547791"
---
# <a name="production-order-cost-estimation"></a><span data-ttu-id="ad819-104">Kostnaðaráætlun framleiðslupöntunar</span><span class="sxs-lookup"><span data-stu-id="ad819-104">Production order cost estimation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ad819-105">Þessi grein gefur upplýsingar um mat á framleiðslukostnaði.</span><span class="sxs-lookup"><span data-stu-id="ad819-105">This article provides information about production cost estimation.</span></span> <span data-ttu-id="ad819-106">Mat á framleiðslukostnaði veitir upplýsingar um efnis- og afkastanotkunarkostnað við framleiðslu á vöru í áætluðu framleiðslupöntunarmagni.</span><span class="sxs-lookup"><span data-stu-id="ad819-106">Production cost estimation provides the projected material and capacity consumption costs of producing an item in the planned production order quantity.</span></span> 

<span data-ttu-id="ad819-107">Eftir að þú stofnar framleiðslupöntun verður þú að meta framleiðslukostnað.</span><span class="sxs-lookup"><span data-stu-id="ad819-107">After you create a production order, you must estimate production costs.</span></span> <span data-ttu-id="ad819-108">Tilgangurinn er mat á vöru- og leiðanotkun fyrir framleiðsluferlið, því matið er notað sem grunnurinn að næstu röðunar- og framleiðsluferlum.</span><span class="sxs-lookup"><span data-stu-id="ad819-108">The purpose is to estimate item and route consumption for the production process, because these estimates are used as the basis for subsequent scheduling and production processes.</span></span>

## <a name="production-cost-estimation"></a><span data-ttu-id="ad819-109">Framleiðslukostnaðarmat</span><span class="sxs-lookup"><span data-stu-id="ad819-109">Production cost estimation</span></span>
<span data-ttu-id="ad819-110">Mat á framleiðslukostnaði er byggt á eftirfarandi upplýsingum:</span><span class="sxs-lookup"><span data-stu-id="ad819-110">Estimates of production costs are based on the following information:</span></span>

-   <span data-ttu-id="ad819-111">Magni í framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="ad819-111">The quantity on the production order</span></span>
-   <span data-ttu-id="ad819-112">Íhlutir í uppskriftum (BOMs) framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="ad819-112">The components on the production bills of materials (BOMs)</span></span>
-   <span data-ttu-id="ad819-113">Leiðaraðgerð í framleiðsluleið.</span><span class="sxs-lookup"><span data-stu-id="ad819-113">The routing operations in the production route</span></span>
-   <span data-ttu-id="ad819-114">Óbeinn kostnaður sem eiga við íhluti og aðgerðir</span><span class="sxs-lookup"><span data-stu-id="ad819-114">The indirect costs that apply to the components and operations</span></span>
-   <span data-ttu-id="ad819-115">Virk kostnaðargögn frá og með útreikningsdegi.</span><span class="sxs-lookup"><span data-stu-id="ad819-115">The active cost data as of the calculation date</span></span>

<span data-ttu-id="ad819-116">Ef til staðar er skuggalínuvara í framleiðsluuppskriftinni endurspegla útreikningarnir þætti skuggavörunnar og leiðaaðgerða.</span><span class="sxs-lookup"><span data-stu-id="ad819-116">If there is a phantom line item on the production BOMs, the calculations reflect the phantom’s components and route operations.</span></span> <span data-ttu-id="ad819-117">Hægt er að nota matsverkefnið til að endurreikna áætlaðan kostnað til að endurspegla uppfærðar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="ad819-117">You can use the estimation task to recalculate estimated costs so that they reflect updated information.</span></span> <span data-ttu-id="ad819-118">Til dæmis gætu uppfærðu upplýsingarnar verið breytingar á magni framleiðslupöntunarinnar, íhlutunum í framleiðsluuppskriftunum, leiðaraðgerðunum í framleiðsluleiðinni, óbeina kostnaðinum sem á við um þessa þætti og aðgerðir eða virk kostnaðargögn frá og með dagsetningu endurreikningsins.</span><span class="sxs-lookup"><span data-stu-id="ad819-118">For example, the updated information might be changes to the quantity on the production order, the components on the production BOMs, the routing operations in the production route, the indirect costs that apply to these components and operations, or the active cost data as of the recalculation date.</span></span> <span data-ttu-id="ad819-119">Útreikningarnir á áætluðum kostnaði gefa líka til kynna söluverð fyrir framleiðsluvöruna á grundvelli nálgunarinnar kostnaður-plús-álag.</span><span class="sxs-lookup"><span data-stu-id="ad819-119">The calculations of estimated cost also suggest a sales price for the production item, based on a cost-plus-markup approach.</span></span> <span data-ttu-id="ad819-120">Útreikningar á áætluðum kostnaði geta einnig gilt um tilvísunarpantanir sem endurspegla aðrar framleiðslupantanir sem eru tengdar við framleiðslupöntunina.</span><span class="sxs-lookup"><span data-stu-id="ad819-120">The calculations of estimated cost can optionally apply to reference orders that reflect other production orders that are linked to the production order.</span></span>

## <a name="view-the-estimated-costs"></a><span data-ttu-id="ad819-121">Skoða áætlaður kostnaður.</span><span class="sxs-lookup"><span data-stu-id="ad819-121">View the estimated costs</span></span>
<span data-ttu-id="ad819-122">Þegar mat hefur verið keyrt er hægt að skoða niðurstöður á **Verðútreikning** síðu.</span><span class="sxs-lookup"><span data-stu-id="ad819-122">After you run estimation, you can view the results on the **Price calculation** page.</span></span> <span data-ttu-id="ad819-123">Matið reiknar eftirfarandi gildi:</span><span class="sxs-lookup"><span data-stu-id="ad819-123">The estimation calculates the following values:</span></span>

-   <span data-ttu-id="ad819-124">**Framleiðslukostnaður** – Framleiðslukostnaður er efsta lína matsins.</span><span class="sxs-lookup"><span data-stu-id="ad819-124">**Production cost** – The production cost is the top line of the estimate.</span></span> <span data-ttu-id="ad819-125">Hún sýnir heildarkostnað við keyrslu framleiðslupöntunar og heildar söluverð framleiðslunnar.</span><span class="sxs-lookup"><span data-stu-id="ad819-125">It shows the complete cost of running the production order and the total sales price for the production.</span></span> <span data-ttu-id="ad819-126">Hún er samtala allra kostnaðarlína í matinu.</span><span class="sxs-lookup"><span data-stu-id="ad819-126">It's the sum of all the cost lines on the estimate.</span></span>
-   <span data-ttu-id="ad819-127">**Leið eða kostnaður tilfanga** – Leið eða tilfangakostnaður er kostnaður fyrir framleiðsluaðgerðir.</span><span class="sxs-lookup"><span data-stu-id="ad819-127">**Route or resource costs** – Route or resource costs are the costs for the production operations.</span></span> <span data-ttu-id="ad819-128">Þau taka með kostnað fyrir einingar eins og uppsetningartíma, keyrslutíma og umstang.</span><span class="sxs-lookup"><span data-stu-id="ad819-128">They include the cost of elements such as setup time, run time, and overhead.</span></span>
-   <span data-ttu-id="ad819-129">**Efniskostnaður** – Efniskostnaður er kostnaður og verð uppskriftaíhluta sem eru nauðsynlegir til þess að framleiða vöruna.</span><span class="sxs-lookup"><span data-stu-id="ad819-129">**Material costs** – Material costs are the costs and prices of the BOM components that are required in order to produce the item.</span></span> <span data-ttu-id="ad819-130">Þessi kostnaður hefur áður verið fastsettur og færa inn í kerfið.</span><span class="sxs-lookup"><span data-stu-id="ad819-130">These costs have previously been established and entered into the system.</span></span>

## <a name="other-uses-of-cost-estimation"></a><span data-ttu-id="ad819-131">Önnur not kostnaðarmats</span><span class="sxs-lookup"><span data-stu-id="ad819-131">Other uses of cost estimation</span></span>
<span data-ttu-id="ad819-132">Kostnaðarmat felur líka í sér eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="ad819-132">A cost estimate also provides the following information:</span></span>

-   <span data-ttu-id="ad819-133">Auðskilin verðtilboð</span><span class="sxs-lookup"><span data-stu-id="ad819-133">Meaningful price quotations</span></span>
-   <span data-ttu-id="ad819-134">Mat á arðsemi pöntunarinnar</span><span class="sxs-lookup"><span data-stu-id="ad819-134">Estimates of the profitability of the order</span></span>
-   <span data-ttu-id="ad819-135">Mat á hráefnisnotkun</span><span class="sxs-lookup"><span data-stu-id="ad819-135">Estimates of raw material usage</span></span>
-   <span data-ttu-id="ad819-136">Samanburð á kostnaðarupplýsingum úr fyrri framleiðslum</span><span class="sxs-lookup"><span data-stu-id="ad819-136">Comparisons of cost information from previous productions</span></span>
-   <span data-ttu-id="ad819-137">Áætlunar- og spáupplýsingar</span><span class="sxs-lookup"><span data-stu-id="ad819-137">Budget and forecasting information</span></span>
-   <span data-ttu-id="ad819-138">Mat á nauðsynlegri framleiðslustærð til þess að geta viðhaldið tilteknum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="ad819-138">Estimates of the production size that is required in order to maintain a particular cost</span></span>




