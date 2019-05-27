---
title: Stofna sölupantanareikninga
description: Þessi leiðarvísi fyrir verk lýsir reikningsfærslu sölupöntunar, þar á meðal sameiningu reikninga og runuvinnslu.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a57d204c0dcb44cbce7a0cc4d2f00b75b57e219
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1565207"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="f0e94-103">Stofna sölupantanareikninga</span><span class="sxs-lookup"><span data-stu-id="f0e94-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f0e94-104">Þessi leiðarvísi fyrir verk lýsir reikningsfærslu sölupöntunar, þar á meðal sameiningu reikninga og runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="f0e94-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="f0e94-105">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="f0e94-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="f0e94-106">Stofna reikning úr sölupöntun</span><span class="sxs-lookup"><span data-stu-id="f0e94-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="f0e94-107">Farið í Viðskiptakröfur > Pantanir > Sendar sölupantanir sem ekki er búið að reikningsfæra.</span><span class="sxs-lookup"><span data-stu-id="f0e94-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="f0e94-108">Veljið sölupöntun af listanum.</span><span class="sxs-lookup"><span data-stu-id="f0e94-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="f0e94-109">Smellið á „Reikningur“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="f0e94-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="f0e94-110">Smellið á „Reikningur“.</span><span class="sxs-lookup"><span data-stu-id="f0e94-110">Click Invoice.</span></span>
    * <span data-ttu-id="f0e94-111">Athugið að þessi sölupöntun hefur margir fylgiseðlar tengjast.</span><span class="sxs-lookup"><span data-stu-id="f0e94-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="f0e94-112">Það mun einungis sýna orðið <multiple> í stað númer fylgiseðils.</span><span class="sxs-lookup"><span data-stu-id="f0e94-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="f0e94-113">Víkkið út færibreytuhlutann.</span><span class="sxs-lookup"><span data-stu-id="f0e94-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="f0e94-114">Bókun verður að vera stillt á Já til að bóka reikninginn.</span><span class="sxs-lookup"><span data-stu-id="f0e94-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="f0e94-115">Einnig er hægt að slökkva á bókun og prenta bara reikning.</span><span class="sxs-lookup"><span data-stu-id="f0e94-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="f0e94-116">Hins vegar hægt að gera sömu niðurstöðu með því að stofna bráðabirgðareikninginn í stað reiknings.</span><span class="sxs-lookup"><span data-stu-id="f0e94-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="f0e94-117">Þessi valkostur er notaður fyrir runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="f0e94-117">This option is used for batch jobs.</span></span> <span data-ttu-id="f0e94-118">Fyrirspurnin er keyrð þegar runuvinnsla er keyrð.</span><span class="sxs-lookup"><span data-stu-id="f0e94-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="f0e94-119">Prenta svæði, velja 'Eftir'.</span><span class="sxs-lookup"><span data-stu-id="f0e94-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="f0e94-120">Velja skal Já til að Prenta reikninginn.</span><span class="sxs-lookup"><span data-stu-id="f0e94-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="f0e94-121">Prentstýring er hægt að prenta mörg afrit af reikningi og senda einnig reikninginn með tölvupósti sem pdf-skrá.</span><span class="sxs-lookup"><span data-stu-id="f0e94-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="f0e94-122">Veljið ‚taka saman' í svæði Prenta gjöld.</span><span class="sxs-lookup"><span data-stu-id="f0e94-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="f0e94-123">Í Athuga lánamarkasvæðið skal velja "Staða".</span><span class="sxs-lookup"><span data-stu-id="f0e94-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="f0e94-124">Smellið á Hætta við.</span><span class="sxs-lookup"><span data-stu-id="f0e94-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="f0e94-125">Sameina pantanir í einn reikning</span><span class="sxs-lookup"><span data-stu-id="f0e94-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="f0e94-126">Farið í Viðskiptakröfur > Pantanir > Allar sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="f0e94-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="f0e94-127">Finna viðskiptavin sem hefur opna marga reikninga.</span><span class="sxs-lookup"><span data-stu-id="f0e94-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="f0e94-128">Velja þarf opna sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="f0e94-128">Select an open sales order.</span></span>
4. <span data-ttu-id="f0e94-129">Veljið aðra opin sölupöntun fyrir sama viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="f0e94-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="f0e94-130">Smellið á „Reikningur“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="f0e94-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="f0e94-131">Smellt er á Reikningnum.</span><span class="sxs-lookup"><span data-stu-id="f0e94-131">Click Invoice.</span></span>
7. <span data-ttu-id="f0e94-132">Víkkið út færibreytuhlutann.</span><span class="sxs-lookup"><span data-stu-id="f0e94-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="f0e94-133">Veljið „Allt“ á svæðinu „Magn“.</span><span class="sxs-lookup"><span data-stu-id="f0e94-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="f0e94-134">Athugið að eru tvo reikninga eru skráðir í hlutanum yfirlit.</span><span class="sxs-lookup"><span data-stu-id="f0e94-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="f0e94-135">Látum okkur nú sameina þau í einn reikning.</span><span class="sxs-lookup"><span data-stu-id="f0e94-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="f0e94-136">í svæðið safnuppfærslu fyrir, Veljið 'Lykilnúmer Reiknings'.</span><span class="sxs-lookup"><span data-stu-id="f0e94-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="f0e94-137">Smellt er á Skipulag til að sameina sölupantanir í einn reikning.</span><span class="sxs-lookup"><span data-stu-id="f0e94-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="f0e94-138">Tvær sölupantanir eru nú sameinaðar einn reikning.</span><span class="sxs-lookup"><span data-stu-id="f0e94-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="f0e94-139">Smellið á Hætta við.</span><span class="sxs-lookup"><span data-stu-id="f0e94-139">Click Cancel.</span></span>
12. <span data-ttu-id="f0e94-140">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="f0e94-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="f0e94-141">Bóka reikninga í runu</span><span class="sxs-lookup"><span data-stu-id="f0e94-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="f0e94-142">Fara í Viðskiptakröfur > Reikningar > Runa reikningsfærsla > Reikningur.</span><span class="sxs-lookup"><span data-stu-id="f0e94-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="f0e94-143">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="f0e94-143">Click Select.</span></span>
3. <span data-ttu-id="f0e94-144">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f0e94-144">Click OK.</span></span>
4. <span data-ttu-id="f0e94-145">Smellt er á Runu.</span><span class="sxs-lookup"><span data-stu-id="f0e94-145">Click Batch.</span></span>
5. <span data-ttu-id="f0e94-146">Smellt er á Já til að kveikja á runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="f0e94-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="f0e94-147">Smellið á Endurtekning.</span><span class="sxs-lookup"><span data-stu-id="f0e94-147">Click Recurrence.</span></span>
7. <span data-ttu-id="f0e94-148">Velja daga</span><span class="sxs-lookup"><span data-stu-id="f0e94-148">Select Days</span></span>
8. <span data-ttu-id="f0e94-149">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f0e94-149">Click OK.</span></span>
9. <span data-ttu-id="f0e94-150">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f0e94-150">Click OK.</span></span>
10. <span data-ttu-id="f0e94-151">Smellið á Hætta við.</span><span class="sxs-lookup"><span data-stu-id="f0e94-151">Click Cancel.</span></span>
11. <span data-ttu-id="f0e94-152">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="f0e94-152">Click Yes.</span></span>

