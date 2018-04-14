--- 
title: "Setja upp greiðsluþóknanir viðskiptavina"
description: "Stofna greiðsluþóknanir fyrir greiðsluar viðskiptavinar."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
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
ms.openlocfilehash: d740ea3f9aeef9ae302fbf3f03e9ecebff24aa5d
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="establish-customer-payment-fees"></a><span data-ttu-id="2c43a-103">Setja upp greiðsluþóknanir viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="2c43a-103">Establish customer payment fees</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2c43a-104">Stofna greiðsluþóknanir fyrir greiðsluar viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="2c43a-104">Create payment fees for customer payments.</span></span>

<span data-ttu-id="2c43a-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="2c43a-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="2c43a-106">Fara í Viðskiptakröfur > Uppsetningar greiðslu > Greiðsluþóknun.</span><span class="sxs-lookup"><span data-stu-id="2c43a-106">Go to Accounts receivable > Payments setup > Payment fee.</span></span>
2. <span data-ttu-id="2c43a-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="2c43a-107">Click New.</span></span>
3. <span data-ttu-id="2c43a-108">Í svæðið Kenni Þóknunar að færa inn kenni Þóknunar.</span><span class="sxs-lookup"><span data-stu-id="2c43a-108">In the Fee ID field, enter a Fee ID.</span></span>
    * <span data-ttu-id="2c43a-109">Kenni Þóknunar Birtist í greiðslubókum, þannig að hafðu það lýsandi til að skilja er hvaða þóknun er metin.</span><span class="sxs-lookup"><span data-stu-id="2c43a-109">The Fee ID displays on payment journals, so make it descriptive to understand what fee is being assessed.</span></span>  
4. <span data-ttu-id="2c43a-110">Færa skal inn heiti þóknunar í reitinn Heiti.</span><span class="sxs-lookup"><span data-stu-id="2c43a-110">In the Name field, enter a fee Name.</span></span>
5. <span data-ttu-id="2c43a-111">Færið inn lýsingu fyrir þóknun í lýsingarsvæði Þóknunar.</span><span class="sxs-lookup"><span data-stu-id="2c43a-111">In the Fee description field, enter a description for the fee.</span></span>
6. <span data-ttu-id="2c43a-112">Velja hvort gjaldið verður skuldfærð á Viðskiptavin eða fjárhagslykil.</span><span class="sxs-lookup"><span data-stu-id="2c43a-112">Select whether the fee will be charged to the Customer or a Ledger account.</span></span>
    * <span data-ttu-id="2c43a-113">Ef viðskiptavinur er metin þóknun, veljið Viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="2c43a-113">If the customer is assessed the fee, select Customer.</span></span> <span data-ttu-id="2c43a-114">Ef þóknunin verður meta sem útgjöld á fyrirtækið , velja Fjárhag.</span><span class="sxs-lookup"><span data-stu-id="2c43a-114">If the fee will be assess to your organization as an expense, select Ledger.</span></span> <span data-ttu-id="2c43a-115">Veljið Viðskiptavin fyrir þetta verk.</span><span class="sxs-lookup"><span data-stu-id="2c43a-115">For this task, select Customer.</span></span>  
7. <span data-ttu-id="2c43a-116">Veljið gerð færslubókar sem getur notað þessa greiðsluþóknun.</span><span class="sxs-lookup"><span data-stu-id="2c43a-116">Select the type of  journal that can use this payment fee.</span></span>
    * <span data-ttu-id="2c43a-117">Ef þessi gjöld eru notaðar fyrir greiðslur viðskiptavina, færslubókargerð líklega verður greiðslu Viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="2c43a-117">If these fees are used for customer payments, the journal type will likely be Customer payment.</span></span>  
8. <span data-ttu-id="2c43a-118">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="2c43a-118">Click Save.</span></span>
9. <span data-ttu-id="2c43a-119">Smellt er á uppsetning Greiðsluþóknunar.</span><span class="sxs-lookup"><span data-stu-id="2c43a-119">Click Payment fee setup.</span></span>
    * <span data-ttu-id="2c43a-120">Uppsetning greiðsluþóknunar er notuð til að skilgreina skilyrði fyrir það hvenær greiðsluþóknun verður metin.</span><span class="sxs-lookup"><span data-stu-id="2c43a-120">The Payment fee setup is used to define the criteria for when the payment fee will be assessed.</span></span>  <span data-ttu-id="2c43a-121">Til dæmis er hægt að skilgreina þóknunin verður reiknuð ef bankareikningurinn er USMF OPER og greiðsluháttur er ávísun.</span><span class="sxs-lookup"><span data-stu-id="2c43a-121">For example, you can define that the fee will be calculated if the bank account is USMF OPER, and the method of payment is check.</span></span>  
10. <span data-ttu-id="2c43a-122">Veljið annað hvort Töflu, Flokk eða Allt til að skilgreina hvaða bankareikninga verða metnar þessu gjaldi.</span><span class="sxs-lookup"><span data-stu-id="2c43a-122">Select either Table, Group or All to define which bank accounts will be assessed this fee.</span></span>
    * <span data-ttu-id="2c43a-123">Ef Allt er valið, gæti allar bankareikningar verið metnar fyrir þessu gjaldi.</span><span class="sxs-lookup"><span data-stu-id="2c43a-123">If you select All, all bank accounts could be assessed this fee.</span></span>  <span data-ttu-id="2c43a-124">Ef Tafla er valinn er aðeins bankareikningur sem þú valdir verið metnar gjaldi.</span><span class="sxs-lookup"><span data-stu-id="2c43a-124">If you select Table, only the bank account you select could be assessed this fee.</span></span> <span data-ttu-id="2c43a-125">Ef þú velur Flokk, einungis bankareikningur í valda bankaflokkinn gæti verið metnar þessu gjaldi.</span><span class="sxs-lookup"><span data-stu-id="2c43a-125">If you select Group, only the bank accounts in the selected bank group could be assessed this fee.</span></span>  
11. <span data-ttu-id="2c43a-126">Veljið bankaflokk eða bankareikningi.</span><span class="sxs-lookup"><span data-stu-id="2c43a-126">Select either a bank group or a bank account.</span></span>
    * <span data-ttu-id="2c43a-127">Ef Tafla er valin, birtir leitin bankareikninga.</span><span class="sxs-lookup"><span data-stu-id="2c43a-127">If you selected Table, the lookup will display bank accounts.</span></span> <span data-ttu-id="2c43a-128">Ef flokkur er valin, birtir leitin bankaflokka.</span><span class="sxs-lookup"><span data-stu-id="2c43a-128">If you selected Group, the lookup will display bank groups.</span></span>  
12. <span data-ttu-id="2c43a-129">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="2c43a-129">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="2c43a-130">Velja Greiðsluhátt sem verður metið þessu gjaldi.</span><span class="sxs-lookup"><span data-stu-id="2c43a-130">Select the Method of payment for which this fee will be assessed.</span></span>
    * <span data-ttu-id="2c43a-131">Til dæmis er hægt að meta þóknun viðskiptavinum ef þeir senda greiðslur sem ávísun, frekar en sem rafræna greiðslu.</span><span class="sxs-lookup"><span data-stu-id="2c43a-131">For example, you may assess a fee to your customers if they send payments as a check, rather than as an electronic payment.</span></span>  
14. <span data-ttu-id="2c43a-132">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="2c43a-132">In the list, find and select the desired record.</span></span>
15. <span data-ttu-id="2c43a-133">Ef við á, færið inn gjaldmiðil greiðslunnar.</span><span class="sxs-lookup"><span data-stu-id="2c43a-133">If relevant, enter a payment currency.</span></span>
    * <span data-ttu-id="2c43a-134">Greiðslugjaldmiðli er notað sem aukaleg skilyrði fyrir hvort þóknunin verður metin.</span><span class="sxs-lookup"><span data-stu-id="2c43a-134">The payment currency is used as an additional criteria for whether the fee will be assessed.</span></span>  <span data-ttu-id="2c43a-135">Til dæmis bankanum gæti gjaldfærð aukalegar þóknun fyrir greiðslur mótteknar í USD-gjaldmiðli, þar sem þær vanalega aðeins færðar í gjaldmiðli EUR.</span><span class="sxs-lookup"><span data-stu-id="2c43a-135">For example, your bank may charge an extra fee for payments received in USD currency, since they normally only transact in EUR currency.</span></span>  
16. <span data-ttu-id="2c43a-136">Velja hvort gjaldið verður prósentu, upphæð eða bil.</span><span class="sxs-lookup"><span data-stu-id="2c43a-136">Select whether the fee will be a percent, amount or interval.</span></span>
17. <span data-ttu-id="2c43a-137">Færa inn prósentu eða upphæð þóknunar.</span><span class="sxs-lookup"><span data-stu-id="2c43a-137">Enter either percentage or amount of the fee.</span></span>
    * <span data-ttu-id="2c43a-138">Sé svæðið Prósenta/Upphæð Prósenta, þá mun gildi fært inn hér verða prósenta.</span><span class="sxs-lookup"><span data-stu-id="2c43a-138">If the Percentage/Amount field is Percent, then the value enter here will be a percentage.</span></span> <span data-ttu-id="2c43a-139">Ef svæðið Prósenta/Upphæð er Upphæð, þá er gildi sem færð er inn hér vera upphæð.</span><span class="sxs-lookup"><span data-stu-id="2c43a-139">If the Percentage/Amount field is Amount, then the value you enter here will be an amount.</span></span> <span data-ttu-id="2c43a-140">Sé svæðið Prósenta/Upphæð er tímabil, nota tímabils flipann til að skilgreina lög.</span><span class="sxs-lookup"><span data-stu-id="2c43a-140">If the Percentage/Amount field is Interval, use the Interval tab to define the tiers.</span></span>  
18. <span data-ttu-id="2c43a-141">Veljið gjaldmiðil fyrir gjöldin í svæðinu gjaldmiðill Þóknunar.</span><span class="sxs-lookup"><span data-stu-id="2c43a-141">In the Fee currency field, select the currency of the fee.</span></span>
    * <span data-ttu-id="2c43a-142">Þetta er gjaldmiðill sem þóknunin verður stofnuð í.</span><span class="sxs-lookup"><span data-stu-id="2c43a-142">This is the currency in which the fee will be created.</span></span>  
19. <span data-ttu-id="2c43a-143">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="2c43a-143">Click Save.</span></span>


