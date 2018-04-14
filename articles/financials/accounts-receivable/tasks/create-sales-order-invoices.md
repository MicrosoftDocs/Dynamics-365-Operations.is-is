--- 
title: "Stofna sölupantanareikninga"
description: "Þessi leiðarvísi fyrir verk lýsir reikningsfærslu sölupöntunar, þar á meðal sameiningu reikninga og runuvinnslu."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: b32a6627a14821be600b4fa49e4a5988d3801cf9
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="2b3de-103">Stofna sölupantanareikninga</span><span class="sxs-lookup"><span data-stu-id="2b3de-103">Create sales order invoices</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2b3de-104">Þessi leiðarvísi fyrir verk lýsir reikningsfærslu sölupöntunar, þar á meðal sameiningu reikninga og runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="2b3de-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="2b3de-105">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="2b3de-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="2b3de-106">Stofna reikning úr sölupöntun</span><span class="sxs-lookup"><span data-stu-id="2b3de-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="2b3de-107">Farið í Viðskiptakröfur > Pantanir > Sendar sölupantanir sem ekki er búið að reikningsfæra.</span><span class="sxs-lookup"><span data-stu-id="2b3de-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="2b3de-108">Veljið sölupöntun af listanum.</span><span class="sxs-lookup"><span data-stu-id="2b3de-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="2b3de-109">Smellið á „Reikningur“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="2b3de-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="2b3de-110">Smellið á „Reikningur“.</span><span class="sxs-lookup"><span data-stu-id="2b3de-110">Click Invoice.</span></span>
    * <span data-ttu-id="2b3de-111">Athugið að þessi sölupöntun hefur margir fylgiseðlar tengjast.</span><span class="sxs-lookup"><span data-stu-id="2b3de-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="2b3de-112">Það mun einungis sýna orðið <multiple> í stað númer fylgiseðils.</span><span class="sxs-lookup"><span data-stu-id="2b3de-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="2b3de-113">Víkkið út færibreytuhlutann.</span><span class="sxs-lookup"><span data-stu-id="2b3de-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="2b3de-114">Bókun verður að vera stillt á Já til að bóka reikninginn.</span><span class="sxs-lookup"><span data-stu-id="2b3de-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="2b3de-115">Einnig er hægt að slökkva á bókun og prenta bara reikning.</span><span class="sxs-lookup"><span data-stu-id="2b3de-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="2b3de-116">Hins vegar hægt að gera sömu niðurstöðu með því að stofna bráðabirgðareikninginn í stað reiknings.</span><span class="sxs-lookup"><span data-stu-id="2b3de-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="2b3de-117">Þessi valkostur er notaður fyrir runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="2b3de-117">This option is used for batch jobs.</span></span> <span data-ttu-id="2b3de-118">Fyrirspurnin er keyrð þegar runuvinnsla er keyrð.</span><span class="sxs-lookup"><span data-stu-id="2b3de-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="2b3de-119">Prenta svæði, velja 'Eftir'.</span><span class="sxs-lookup"><span data-stu-id="2b3de-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="2b3de-120">Velja skal Já til að Prenta reikninginn.</span><span class="sxs-lookup"><span data-stu-id="2b3de-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="2b3de-121">Prentstýring er hægt að prenta mörg afrit af reikningi og senda einnig reikninginn með tölvupósti sem pdf-skrá.</span><span class="sxs-lookup"><span data-stu-id="2b3de-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="2b3de-122">Veljið ‚taka saman' í svæði Prenta gjöld.</span><span class="sxs-lookup"><span data-stu-id="2b3de-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="2b3de-123">Í Athuga lánamarkasvæðið skal velja "Staða".</span><span class="sxs-lookup"><span data-stu-id="2b3de-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="2b3de-124">Smellið á Hætta við.</span><span class="sxs-lookup"><span data-stu-id="2b3de-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="2b3de-125">Sameina pantanir í einn reikning</span><span class="sxs-lookup"><span data-stu-id="2b3de-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="2b3de-126">Farið í Viðskiptakröfur > Pantanir > Allar sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="2b3de-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="2b3de-127">Finna viðskiptavin sem hefur opna marga reikninga.</span><span class="sxs-lookup"><span data-stu-id="2b3de-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="2b3de-128">Velja þarf opna sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="2b3de-128">Select an open sales order.</span></span>
4. <span data-ttu-id="2b3de-129">Veljið aðra opin sölupöntun fyrir sama viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="2b3de-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="2b3de-130">Smellið á „Reikningur“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="2b3de-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="2b3de-131">Smellt er á Reikningnum.</span><span class="sxs-lookup"><span data-stu-id="2b3de-131">Click Invoice.</span></span>
7. <span data-ttu-id="2b3de-132">Víkkið út færibreytuhlutann.</span><span class="sxs-lookup"><span data-stu-id="2b3de-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="2b3de-133">Veljið „Allt“ á svæðinu „Magn“.</span><span class="sxs-lookup"><span data-stu-id="2b3de-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="2b3de-134">Athugið að eru tvo reikninga eru skráðir í hlutanum yfirlit.</span><span class="sxs-lookup"><span data-stu-id="2b3de-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="2b3de-135">Látum okkur nú sameina þau í einn reikning.</span><span class="sxs-lookup"><span data-stu-id="2b3de-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="2b3de-136">í svæðið safnuppfærslu fyrir, Veljið 'Lykilnúmer Reiknings'.</span><span class="sxs-lookup"><span data-stu-id="2b3de-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="2b3de-137">Smellt er á Skipulag til að sameina sölupantanir í einn reikning.</span><span class="sxs-lookup"><span data-stu-id="2b3de-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="2b3de-138">Tvær sölupantanir eru nú sameinaðar einn reikning.</span><span class="sxs-lookup"><span data-stu-id="2b3de-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="2b3de-139">Smellið á Hætta við.</span><span class="sxs-lookup"><span data-stu-id="2b3de-139">Click Cancel.</span></span>
12. <span data-ttu-id="2b3de-140">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="2b3de-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="2b3de-141">Bóka reikninga í runu</span><span class="sxs-lookup"><span data-stu-id="2b3de-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="2b3de-142">Fara í Viðskiptakröfur > Reikningar > Runa reikningsfærsla > Reikningur.</span><span class="sxs-lookup"><span data-stu-id="2b3de-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="2b3de-143">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="2b3de-143">Click Select.</span></span>
3. <span data-ttu-id="2b3de-144">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="2b3de-144">Click OK.</span></span>
4. <span data-ttu-id="2b3de-145">Smellt er á Runu.</span><span class="sxs-lookup"><span data-stu-id="2b3de-145">Click Batch.</span></span>
5. <span data-ttu-id="2b3de-146">Smellt er á Já til að kveikja á runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="2b3de-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="2b3de-147">Smellið á Endurtekning.</span><span class="sxs-lookup"><span data-stu-id="2b3de-147">Click Recurrence.</span></span>
7. <span data-ttu-id="2b3de-148">Velja daga</span><span class="sxs-lookup"><span data-stu-id="2b3de-148">Select Days</span></span>
8. <span data-ttu-id="2b3de-149">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="2b3de-149">Click OK.</span></span>
9. <span data-ttu-id="2b3de-150">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="2b3de-150">Click OK.</span></span>
10. <span data-ttu-id="2b3de-151">Smellið á Hætta við.</span><span class="sxs-lookup"><span data-stu-id="2b3de-151">Click Cancel.</span></span>
11. <span data-ttu-id="2b3de-152">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="2b3de-152">Click Yes.</span></span>


