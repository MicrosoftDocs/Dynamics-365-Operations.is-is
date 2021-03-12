---
title: Stofna sölupantanareikninga
description: Þessi leiðarvísi fyrir verk lýsir reikningsfærslu sölupöntunar, þar á meðal sameiningu reikninga og runuvinnslu.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0076e838ad4eac687dc7db1bc0a94891f0ee6d9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991018"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="ac2a7-103">Stofna sölupantanareikninga</span><span class="sxs-lookup"><span data-stu-id="ac2a7-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ac2a7-104">Þessi leiðarvísi fyrir verk lýsir reikningsfærslu sölupöntunar, þar á meðal sameiningu reikninga og runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="ac2a7-105">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="ac2a7-106">Stofna reikning úr sölupöntun</span><span class="sxs-lookup"><span data-stu-id="ac2a7-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="ac2a7-107">Farðu í **Sloðunarrúða > Kerfiseiningar > viðskiptakröfur > Pantanir > Sendar en óreikningsfærðar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="ac2a7-108">Veljið sölupöntun af listanum.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="ac2a7-109">Í **aðgerðasvæðinu** er smellt á **Reikningur > Mynda > Reikningur**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="ac2a7-110">Athugið að þessi sölupöntun hefur margir fylgiseðlar tengjast.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="ac2a7-111">Það mun einungis sýna orðið <multiple> í stað númer fylgiseðils.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="ac2a7-112">Útvíkkaðu hlutann **Færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="ac2a7-113">Bókun verður að vera stillt á Já til að bóka reikninginn.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="ac2a7-114">Einnig er hægt að slökkva á bókun og prenta bara reikning.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="ac2a7-115">Hins vegar hægt að gera sömu niðurstöðu með því að stofna bráðabirgðareikninginn í stað reiknings.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="ac2a7-116">Þessi valkostur er notaður fyrir runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-116">This option is used for batch jobs.</span></span> <span data-ttu-id="ac2a7-117">Fyrirspurnin er keyrð þegar runuvinnsla er keyrð.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="ac2a7-118">Í reitnum **Prenta** skal velja 'Eftir'.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="ac2a7-119">Velja skal **Já** til að **Prenta reikninginn**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="ac2a7-120">Prentstýring er hægt að prenta mörg afrit af reikningi og senda einnig reikninginn með tölvupósti sem pdf-skrá.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="ac2a7-121">Í reitnum **Prenta gjöld** skaltu velja Taka saman.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="ac2a7-122">Í reitnum **Athuga lánamark** skal velja Staða.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="ac2a7-123">Smelltu á **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="ac2a7-124">Sameina pantanir í einn reikning</span><span class="sxs-lookup"><span data-stu-id="ac2a7-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="ac2a7-125">Farðu í **Sloðunarrúða > Kerfiseiningar > viðskiptakröfur > Pantanir > Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="ac2a7-126">Finna viðskiptavin sem hefur opna marga reikninga.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="ac2a7-127">Veldu margar opnar sölupantanir frá sama viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="ac2a7-128">Í **aðgerðasvæðinu** er smellt á **Reikningur > Mynda > Reikningur**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="ac2a7-129">Útvíkkaðu hlutann **Færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="ac2a7-130">Í reitnum **Magn** velurðu Allt.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="ac2a7-131">Athugið að eru tvo reikninga eru skráðir í hlutanum yfirlit.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="ac2a7-132">Látum okkur nú sameina þau í einn reikning.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="ac2a7-133">í reitnum **Safnuppfærsla fyrir** skal velja Lykilnúmer Reiknings.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="ac2a7-134">Smelltu á **Raða** til að sameina sölupantanir í einn reikning.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="ac2a7-135">Tvær sölupantanir eru nú sameinaðar einn reikning.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="ac2a7-136">Smelltu á **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="ac2a7-137">Smellið á **Já**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="ac2a7-138">Bóka reikninga í runu</span><span class="sxs-lookup"><span data-stu-id="ac2a7-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="ac2a7-139">Farðu í **Skoðunarrúðu > Einingar > Viðskiptakröfur > Reikningar > Runureikningsfærsla > Reikningur**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="ac2a7-140">Smellið á **Velja**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-140">Click **Select**.</span></span>
3. <span data-ttu-id="ac2a7-141">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-141">Click **OK**.</span></span>
4. <span data-ttu-id="ac2a7-142">Smelltu á **Runa**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-142">Click **Batch**.</span></span>
5. <span data-ttu-id="ac2a7-143">Veldu **Já** í **Runuvinnslu**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="ac2a7-144">Smelltu á **Endurtekning**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="ac2a7-145">Veldu **Dagar**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-145">Select **Days**.</span></span>
8. <span data-ttu-id="ac2a7-146">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-146">Click **OK**.</span></span>
9. <span data-ttu-id="ac2a7-147">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-147">Click **OK**.</span></span>
10. <span data-ttu-id="ac2a7-148">Smelltu á **Hætta við**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="ac2a7-149">Smellið á **Já**.</span><span class="sxs-lookup"><span data-stu-id="ac2a7-149">Click **Yes**.</span></span>

