---
title: Notkun Samfelldniáætlana
description: Þetta ferli fer í gegnum að selja samfelldniáætlanir og vinna úr tengdar sölupantanir.
author: scott-tucker
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRCustomerService, MCRCustSearch, SalesTable, MCRContinuityCustInfo, MCRCustPaymLookup, CreditCardTokenization, CreditCardLookup, MCRSalesOrderRecap
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45bd4a3cc9f9b03c713d33638d6dc93aa696c581
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1564908"
---
# <a name="using-continuity-program"></a><span data-ttu-id="761a2-103">Notkun Samfelldniáætlana</span><span class="sxs-lookup"><span data-stu-id="761a2-103">Using continuity program</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="761a2-104">Þetta ferli fer í gegnum að selja samfelldniáætlanir og vinna úr tengdar sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="761a2-104">This procedure walks through selling a continuity program and processing related sales orders.</span></span> <span data-ttu-id="761a2-105">Til að ljúka við þetta ferli, þarf notandi að vera settur upp sem notandi símavers.</span><span class="sxs-lookup"><span data-stu-id="761a2-105">To complete this procedure, the user has to be set up as a call center user.</span></span> <span data-ttu-id="761a2-106">Þessi aðferð notar USRT sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="761a2-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="761a2-107">Fara í Smásölu og viðskipti > viðskiptavinur > viðskiptavinur þjónusta.</span><span class="sxs-lookup"><span data-stu-id="761a2-107">Go to Retail and commerce > Customers > Customer service.</span></span>
2. <span data-ttu-id="761a2-108">Í svæðinu SearchText, færðu inn 'Karen' og styðja á Tab-lykil.</span><span class="sxs-lookup"><span data-stu-id="761a2-108">In the SearchText field, type 'Karen' and then press the Tab key.</span></span>
    * <span data-ttu-id="761a2-109">Svargluggi Ítarleg leit ætti að birtast.</span><span class="sxs-lookup"><span data-stu-id="761a2-109">The advanced search dialog should pop up.</span></span> <span data-ttu-id="761a2-110">Ef það gerist ekki skal smella á Leit hægra megin við þetta svæði.</span><span class="sxs-lookup"><span data-stu-id="761a2-110">If it doesn't, click Search to the right of this field.</span></span>  
3. <span data-ttu-id="761a2-111">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="761a2-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="761a2-112">Aðeins ætti að birtast ein línan með Karen Berg.</span><span class="sxs-lookup"><span data-stu-id="761a2-112">There should be only one row with Karen Berg showing.</span></span> <span data-ttu-id="761a2-113">Velja línuna með því að smella á gátmerki-dálknum lengst til vinstri í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="761a2-113">Select the row by clicking on the checkmark column on the far left of the grid.</span></span>  
4. <span data-ttu-id="761a2-114">Smellið á Velja.</span><span class="sxs-lookup"><span data-stu-id="761a2-114">Click Select.</span></span>
5. <span data-ttu-id="761a2-115">Smelltu á Ný sölupöntun</span><span class="sxs-lookup"><span data-stu-id="761a2-115">Click New sales order.</span></span>
    * <span data-ttu-id="761a2-116">Gott er að taka niður númer sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="761a2-116">It's a good idea to note the sales order number.</span></span> <span data-ttu-id="761a2-117">Þarf hana síðar í þessu ferli.</span><span class="sxs-lookup"><span data-stu-id="761a2-117">You'll need it later in this procedure.</span></span>  
6. <span data-ttu-id="761a2-118">Í svæðinu vörunúmer, færðu inn '88000' og styðja á Tab-lykil.</span><span class="sxs-lookup"><span data-stu-id="761a2-118">In the Item number field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="761a2-119">Þetta er Samfelldnivara í sýnigögn USRT.</span><span class="sxs-lookup"><span data-stu-id="761a2-119">This is a continuity item in the USRT demo data.</span></span>  
7. <span data-ttu-id="761a2-120">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="761a2-120">Click Complete.</span></span>
8. <span data-ttu-id="761a2-121">Færa inn "Visa" í svæðinu greiðslumáti.</span><span class="sxs-lookup"><span data-stu-id="761a2-121">In the Payment method field, enter 'Visa'.</span></span>
9. <span data-ttu-id="761a2-122">Smelltu á Bæta við kreditkorti</span><span class="sxs-lookup"><span data-stu-id="761a2-122">Click Add credit card.</span></span>
    * <span data-ttu-id="761a2-123">Færðu inn nauðsynlegt upplýsingar um kreditkort á þessari síðu.</span><span class="sxs-lookup"><span data-stu-id="761a2-123">Enter the required credit card information on this page.</span></span>  
10. <span data-ttu-id="761a2-124">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="761a2-124">Click OK.</span></span>
11. <span data-ttu-id="761a2-125">Stækkið hlutann Greiðslur.</span><span class="sxs-lookup"><span data-stu-id="761a2-125">Expand the Payment section.</span></span>
    * <span data-ttu-id="761a2-126">Til að senda pöntun símavers, þarf að færa inn greiðslur fyrir pöntuninni.</span><span class="sxs-lookup"><span data-stu-id="761a2-126">To submit a call center order, payments have to be entered for the order.</span></span>  
12. <span data-ttu-id="761a2-127">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="761a2-127">Click OK.</span></span>
13. <span data-ttu-id="761a2-128">Smelltu á Senda.</span><span class="sxs-lookup"><span data-stu-id="761a2-128">Click Submit.</span></span>
    * <span data-ttu-id="761a2-129">Þú ert búinn að stofna nýja samfelldnipöntun.</span><span class="sxs-lookup"><span data-stu-id="761a2-129">You're done creating a new continuity order.</span></span> <span data-ttu-id="761a2-130">Næst, muntu keyra tvær runuvinnslur sem eru notuð við vinnslu á samfelldnipöntunum.</span><span class="sxs-lookup"><span data-stu-id="761a2-130">Next, you'll run two batch processes that are used to process the continuity orders.</span></span>  
14. <span data-ttu-id="761a2-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="761a2-131">Close the page.</span></span>
15. <span data-ttu-id="761a2-132">Fara í Smásölu og viðskipti > Samfelldni > Vinnsla samfelldnigreiðslna.</span><span class="sxs-lookup"><span data-stu-id="761a2-132">Go to Retail and commerce > Continuity > Process continuity payments.</span></span>
16. <span data-ttu-id="761a2-133">Í svæðinu Samfelldnivara, færðu inn '88000' og styðja á Tab-lykil.</span><span class="sxs-lookup"><span data-stu-id="761a2-133">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
17. <span data-ttu-id="761a2-134">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="761a2-134">Click OK.</span></span>
18. <span data-ttu-id="761a2-135">Fara í Smásölu og viðskipti > Samfelldni > Stofna samfelldni undirpantanir.</span><span class="sxs-lookup"><span data-stu-id="761a2-135">Go to Retail and commerce > Continuity > Create continuity child orders.</span></span>
    * <span data-ttu-id="761a2-136">Þetta ferli mun stofna nýjar sölupantanir byggt á stillingum samfelldniáætlanir.</span><span class="sxs-lookup"><span data-stu-id="761a2-136">This process will create new sales orders based on the settings of your continuity programs.</span></span>  
19. <span data-ttu-id="761a2-137">Í svæðinu Samfelldnivara, færðu inn '88000' og styðja á Tab-lykil.</span><span class="sxs-lookup"><span data-stu-id="761a2-137">In the Continuity item field, type '88000' and then press the Tab key.</span></span>
    * <span data-ttu-id="761a2-138">Vara "88000" er Samfelldnivara í sýnigögn USRT.</span><span class="sxs-lookup"><span data-stu-id="761a2-138">Item '88000' is a continuity item in the USRT demo data.</span></span>  
20. <span data-ttu-id="761a2-139">Í reitinn sölupöntun skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="761a2-139">In the Sales order field, enter or select a value.</span></span>
    * <span data-ttu-id="761a2-140">Færið inn númer sölupöntunar sem var tekið niður fyrr í ferlinu.</span><span class="sxs-lookup"><span data-stu-id="761a2-140">Enter the sales order number that you noted earlier in the procedure.</span></span> <span data-ttu-id="761a2-141">Þetta mun halda vinnslutíma í lágmarki fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="761a2-141">This will keep the processing time to a minimal for this procedure.</span></span> <span data-ttu-id="761a2-142">Svæðið sölupöntun er valfrjáls - hægt er að vinna allar pantanir fyrir hverja staka áætlun.</span><span class="sxs-lookup"><span data-stu-id="761a2-142">The Sales order field field is optional--you could process all orders for any one program.</span></span>  
21. <span data-ttu-id="761a2-143">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="761a2-143">Click OK.</span></span>

