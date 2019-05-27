---
title: " Grunnverð og verðsamningar"
description: Þetta ferli fer í gegnum stofnun söluverð bundnum við rás viðskiptasamninga.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PriceDiscGroup, RetailStoreTable, RetailChannelPriceGroup, EcoResProductDetailsExtended, PriceDiscAdmTable, PriceDiscAdm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4830ac553318cfbb3cb74395d1662e74dff75290
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548532"
---
# <a name="base-price-and-trade-agreements"></a><span data-ttu-id="9520a-103"> Grunnverð og verðsamningar</span><span class="sxs-lookup"><span data-stu-id="9520a-103">Base price and trade agreements</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9520a-104">Þetta ferli fer í gegnum stofnun söluverð bundnum við rás viðskiptasamninga.</span><span class="sxs-lookup"><span data-stu-id="9520a-104">This procedure walks through creating channel-specific sales price trade agreements.</span></span> <span data-ttu-id="9520a-105">Þessi aðferð notar USRT sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="9520a-105">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="9520a-106">Fara í Smásölu og viðskipti > Verðlagning og afslættir > Verðflokkar > Allir verðflokkar.</span><span class="sxs-lookup"><span data-stu-id="9520a-106">Go to Retail and commerce > Pricing and discounts > Price groups > All price groups.</span></span>
    * <span data-ttu-id="9520a-107">Verðflokkar eru hvernig verðsamninga er úthlutað á tiltekinn rásir.</span><span class="sxs-lookup"><span data-stu-id="9520a-107">Price groups are how trade agreements are assigned to specific channels.</span></span> <span data-ttu-id="9520a-108">Notkun verðflokka til að tengja viðskiptasamninga við rás gerir virkjar verðlagningu eftir rásum.</span><span class="sxs-lookup"><span data-stu-id="9520a-108">Using price groups to assign trade agreements to a channel enables channel-specific pricing.</span></span>  
2. <span data-ttu-id="9520a-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9520a-109">Click New.</span></span>
3. <span data-ttu-id="9520a-110">Í reitinn verðflokkur skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9520a-110">In the Price groups field, type a value.</span></span>
4. <span data-ttu-id="9520a-111">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9520a-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="9520a-112">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9520a-112">Click Save.</span></span>
6. <span data-ttu-id="9520a-113">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9520a-113">Close the page.</span></span>
7. <span data-ttu-id="9520a-114">Fara í Smásölu og viðskipti > rásir > smásöluverslanir > allar smásöluverslanir.</span><span class="sxs-lookup"><span data-stu-id="9520a-114">Go to Retail and commerce > Channels > Retail stores > All retail stores.</span></span>
8. <span data-ttu-id="9520a-115">Á listanum, veljið 'New York'</span><span class="sxs-lookup"><span data-stu-id="9520a-115">In the list, select 'New York'</span></span>
9. <span data-ttu-id="9520a-116">Í aðgerðasvæðinu er smellt á verslun.</span><span class="sxs-lookup"><span data-stu-id="9520a-116">On the Action Pane, click Store.</span></span>
10. <span data-ttu-id="9520a-117">Smellt er á verðflokkur.</span><span class="sxs-lookup"><span data-stu-id="9520a-117">Click Price groups.</span></span>
11. <span data-ttu-id="9520a-118">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9520a-118">Click New.</span></span>
12. <span data-ttu-id="9520a-119">Í reitnum verðflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9520a-119">In the Price groups field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="9520a-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="9520a-120">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="9520a-121">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9520a-121">Click Save.</span></span>
15. <span data-ttu-id="9520a-122">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9520a-122">Close the page.</span></span>
16. <span data-ttu-id="9520a-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9520a-123">Close the page.</span></span>
17. <span data-ttu-id="9520a-124">Fara í Smásölu og viðskipti > Afurðir og tegundir > Losaðar afurðir eftir flokki.</span><span class="sxs-lookup"><span data-stu-id="9520a-124">Go to Retail and commerce > Products and categories > Released products by category.</span></span>
18. <span data-ttu-id="9520a-125">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9520a-125">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="9520a-126">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="9520a-126">Click Edit.</span></span>
20. <span data-ttu-id="9520a-127">Víxla útvíkkun á liðnum Selja.</span><span class="sxs-lookup"><span data-stu-id="9520a-127">Toggle the expansion of the Sell section.</span></span>
21. <span data-ttu-id="9520a-128">Í reitinn Verð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="9520a-128">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="9520a-129">Þetta verð er notaður ef engin viðeigandi verðsamningar fundust.</span><span class="sxs-lookup"><span data-stu-id="9520a-129">This price is used if no applicable trade agreements are found.</span></span>  
22. <span data-ttu-id="9520a-130">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9520a-130">Click Save.</span></span>
23. <span data-ttu-id="9520a-131">Í aðgerðasvæðinu er smellt á selja.</span><span class="sxs-lookup"><span data-stu-id="9520a-131">On the Action Pane, click Sell.</span></span>
24. <span data-ttu-id="9520a-132">Smelltu á Stofna verðsamninga</span><span class="sxs-lookup"><span data-stu-id="9520a-132">Click Create trade agreements.</span></span>
25. <span data-ttu-id="9520a-133">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="9520a-133">Click New.</span></span>
26. <span data-ttu-id="9520a-134">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9520a-134">In the Name field, click the drop-down button to open the lookup.</span></span>
27. <span data-ttu-id="9520a-135">Farið í listann og veljið smásala.</span><span class="sxs-lookup"><span data-stu-id="9520a-135">In the list, select 'Retail'.</span></span>
    * <span data-ttu-id="9520a-136">Færslubókarheitið ‚Smásala' er notað í sýnigögn sem sjálfgefin tengsl „Verðs (sala)".</span><span class="sxs-lookup"><span data-stu-id="9520a-136">In the demo data, the 'Retail' journal name has the default relation of 'Price (sales)'.</span></span> <span data-ttu-id="9520a-137">Þetta þýðir að allar nýjar línur sem stofnaðar eru verða sjálfgefnar fyrir söluverð viðskiptasamninga.</span><span class="sxs-lookup"><span data-stu-id="9520a-137">That means all new lines created will default to sales price trade agreements.</span></span>  
28. <span data-ttu-id="9520a-138">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="9520a-138">Click Lines.</span></span>
29. <span data-ttu-id="9520a-139">Í reitnum kóði lykils er valið 'flokkur'.</span><span class="sxs-lookup"><span data-stu-id="9520a-139">In the Account code field, select 'Group'.</span></span>
30. <span data-ttu-id="9520a-140">Í reitnum Val á lykli skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9520a-140">In the Account selection field, click the drop-down button to open the lookup.</span></span>
31. <span data-ttu-id="9520a-141">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="9520a-141">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9520a-142">Þetta Ljúka við tengil úr Rásar til vöruverðs til viðskiptasamningi.</span><span class="sxs-lookup"><span data-stu-id="9520a-142">This will complete the link from Channel to Price group to Trade agreement.</span></span>  
32. <span data-ttu-id="9520a-143">Í reitinn vöruvensl skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9520a-143">In the Item relation field, type a value.</span></span>
33. <span data-ttu-id="9520a-144">Í Upphæð í gjaldmiðli svæðinu, færið inn tölu.</span><span class="sxs-lookup"><span data-stu-id="9520a-144">In the Amount in currency field, enter a number.</span></span>
34. <span data-ttu-id="9520a-145">Kanna eða afmerkja Finna næsta gátreit.</span><span class="sxs-lookup"><span data-stu-id="9520a-145">Check or uncheck the Find next checkbox.</span></span>
    * <span data-ttu-id="9520a-146">Þegar Finna næsta hefur verið stillt á 'Já', verðlagningarvélar munu halda áfram að leita að viðeigandi verðsamninga með lægri söluverði.</span><span class="sxs-lookup"><span data-stu-id="9520a-146">When Find next is set to 'Yes', the pricing engine will continue to search for applicable trade agreements with a lower sale price.</span></span> <span data-ttu-id="9520a-147">Þegar Finna næsta hefur verið stillt á 'Nei', verðvél stöðvar leit og notar viðskiptasamningsins.</span><span class="sxs-lookup"><span data-stu-id="9520a-147">When Find next is set to 'No', the price engine stops searching and uses the trade agreement.</span></span>  
35. <span data-ttu-id="9520a-148">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="9520a-148">Click Post.</span></span>
36. <span data-ttu-id="9520a-149">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9520a-149">Click OK.</span></span>
37. <span data-ttu-id="9520a-150">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9520a-150">Close the page.</span></span>
38. <span data-ttu-id="9520a-151">Í aðgerðasvæðinu er smellt á selja.</span><span class="sxs-lookup"><span data-stu-id="9520a-151">On the Action Pane, click Sell.</span></span>
39. <span data-ttu-id="9520a-152">Smelltu á söluverð</span><span class="sxs-lookup"><span data-stu-id="9520a-152">Click Sales price.</span></span>

