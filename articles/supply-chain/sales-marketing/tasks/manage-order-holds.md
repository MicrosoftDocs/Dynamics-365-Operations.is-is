--- 
title: "Stjórna pöntunum í bið"
description: "Þetta ferli sýnir hvernig setja sölupantanir viðskiptavina í bið, hvernig vinna með biðstöðu greiðsluferlis og hvernig fjarlægja bið af pöntun."
author: omulvad
manager: AnnBe
ms.date: 01/09/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 7504411a840dd2daeb6fe6f47fd4387d6b011fba
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="manage-order-holds"></a><span data-ttu-id="606f7-103">Stjórna pöntunum í bið</span><span class="sxs-lookup"><span data-stu-id="606f7-103">Manage order holds</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="606f7-104">Þetta ferli sýnir hvernig setja sölupantanir viðskiptavina í bið, hvernig vinna með biðstöðu greiðsluferlis og hvernig fjarlægja bið af pöntun.</span><span class="sxs-lookup"><span data-stu-id="606f7-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="606f7-105">Pöntun kann að vera sett í bið af ýmsum ástæðum.</span><span class="sxs-lookup"><span data-stu-id="606f7-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="606f7-106">Til dæmis gætirðu verið með pöntun í bið þar til hægt er að staðfesta aðsetur  viðskiptavinar eða greiðsluhætti eða þar til stjórnandinn getur farið yfir lánamark viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="606f7-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer’s credit limit.</span></span> <span data-ttu-id="606f7-107">Þegar pöntun er í bið er ekki hægt að vinna af vörugeymslu til afhendingar.</span><span class="sxs-lookup"><span data-stu-id="606f7-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="606f7-108">Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.</span><span class="sxs-lookup"><span data-stu-id="606f7-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="606f7-109">Setja upp biðstöðu pöntunar</span><span class="sxs-lookup"><span data-stu-id="606f7-109">Set up order holds</span></span>
1. <span data-ttu-id="606f7-110">Fara í Sala og markaðssetning > Uppsetning > Sölupantanir > Biðkóðar pantana.</span><span class="sxs-lookup"><span data-stu-id="606f7-110">Go to Sales and marketing > Setup > Sales orders > Order hold codes.</span></span>
2. <span data-ttu-id="606f7-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="606f7-111">Click New.</span></span>
3. <span data-ttu-id="606f7-112">Í svæði Biðkóði skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="606f7-112">In the Hold code field, type a value.</span></span>
    * <span data-ttu-id="606f7-113">Til dæmis, skrifið Hringja aftur.</span><span class="sxs-lookup"><span data-stu-id="606f7-113">For example, type Call back.</span></span>  
4. <span data-ttu-id="606f7-114">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="606f7-114">In the Description field, type a value.</span></span>
    * <span data-ttu-id="606f7-115">Til dæmis, Pöntun haldið í bið eftir símtal frá viðskiptavinur.</span><span class="sxs-lookup"><span data-stu-id="606f7-115">For example, Order held waiting for customer callback.</span></span>  
    * <span data-ttu-id="606f7-116">Annars er hægt að velja gátreitur Fjarlægja frátekningu til að fjarlægja allar efnislegur frátekning úr pöntun þegar biðkóði er bætti við.</span><span class="sxs-lookup"><span data-stu-id="606f7-116">Optionally, select the Remove reservations check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="606f7-117">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="606f7-117">Click Save.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="606f7-118">Setja pöntun í bið</span><span class="sxs-lookup"><span data-stu-id="606f7-118">Place order on hold</span></span>
1. <span data-ttu-id="606f7-119">Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir</span><span class="sxs-lookup"><span data-stu-id="606f7-119">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="606f7-120">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="606f7-120">Click New.</span></span>
3. <span data-ttu-id="606f7-121">Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="606f7-121">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="606f7-122">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="606f7-122">Click OK.</span></span>
5. <span data-ttu-id="606f7-123">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="606f7-123">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="606f7-124">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="606f7-124">In the Quantity field, enter a number.</span></span>
7. <span data-ttu-id="606f7-125">Smellið á „Sölupöntun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="606f7-125">On the Action Pane, click Sales order.</span></span>
8. <span data-ttu-id="606f7-126">Smellt er á Biðstöður pantana.</span><span class="sxs-lookup"><span data-stu-id="606f7-126">Click Order holds.</span></span>
9. <span data-ttu-id="606f7-127">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="606f7-127">Click New.</span></span>
10. <span data-ttu-id="606f7-128">Í svæði Biðkóði skal velja kóða sem stofnaður í fyrra undirverk.</span><span class="sxs-lookup"><span data-stu-id="606f7-128">In the Hold code field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="606f7-129">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="606f7-129">Click Save.</span></span>
12. <span data-ttu-id="606f7-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="606f7-130">Close the page.</span></span>
13. <span data-ttu-id="606f7-131">Fara í Sölu og markaðssetningu > sölupöntun > Allar sölupantanir</span><span class="sxs-lookup"><span data-stu-id="606f7-131">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
14. <span data-ttu-id="606f7-132">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="606f7-132">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="606f7-133">Pantanir sem núna í bið eru með merkt svæði „Ekki keyra“ og „Í biðstöðu“.</span><span class="sxs-lookup"><span data-stu-id="606f7-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>    
15. <span data-ttu-id="606f7-134">Smellið á „Tiltekt og pökkun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="606f7-134">On the Action Pane, click Pick and pack.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="606f7-135">Stjórna pöntunum í bið</span><span class="sxs-lookup"><span data-stu-id="606f7-135">Manage order holds</span></span>
1. <span data-ttu-id="606f7-136">Fara í Sala og markaðssetning > Sölupöntun > Opnar pantanir > Pantanir í bið.</span><span class="sxs-lookup"><span data-stu-id="606f7-136">Go to Sales and marketing > Sales orders > Open orders > Order holds.</span></span>
    * <span data-ttu-id="606f7-137">Síðan Pantanir í bið virkar sem vinnubekkur þar sem fá yfirlit yfir allar núgildandi og unnar biðstöður, vinna með þær og tengdar sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="606f7-137">Order holds page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>      
2. <span data-ttu-id="606f7-138">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="606f7-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="606f7-139">Á aðgerðarúða skal smella á Setja greiðsluferli í bið.</span><span class="sxs-lookup"><span data-stu-id="606f7-139">On the Action Pane, click Hold checkout.</span></span>
4. <span data-ttu-id="606f7-140">Smella skal á Greiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="606f7-140">Click Check out.</span></span>
5. <span data-ttu-id="606f7-141">Í listanum skal afmerkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="606f7-141">In the list, unmark the selected row.</span></span>
    * <span data-ttu-id="606f7-142">Svæði Greiðsluferli í birtir núna notandakenni þitt.</span><span class="sxs-lookup"><span data-stu-id="606f7-142">The Checkout out to field now shows your user ID.</span></span>   
6. <span data-ttu-id="606f7-143">Smella á Hreinsa greiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="606f7-143">Click Clear checkout.</span></span>
7. <span data-ttu-id="606f7-144">Í að smella á Hreinsa biðstöðu.</span><span class="sxs-lookup"><span data-stu-id="606f7-144">On the Action Pane, click Clear hold.</span></span>
    * <span data-ttu-id="606f7-145">Þegar þú tilbúið að fjarlægja í bið og leyfa pöntun halda áfram í næsta útskráningarskref verður að hreinsa í bið.</span><span class="sxs-lookup"><span data-stu-id="606f7-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="606f7-146">Ef ekki þarf að breyta pöntun má keyra aðgerð Hreinsa bið.</span><span class="sxs-lookup"><span data-stu-id="606f7-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="606f7-147">Þegar bið er hreinsa er hægt að nota aðgerð Hreinsa og breyta ef uppfæra þarf pöntun.</span><span class="sxs-lookup"><span data-stu-id="606f7-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    * <span data-ttu-id="606f7-148">Aðgerðin Hreinsa og senda á aðeins við þegar aðgerðin Símaver er notað.</span><span class="sxs-lookup"><span data-stu-id="606f7-148">The Clear and submit action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="606f7-149">Smella á Hreinsa biðstöðu.</span><span class="sxs-lookup"><span data-stu-id="606f7-149">Click Clear holds.</span></span>
    * <span data-ttu-id="606f7-150">Biðstaða hefur verið fjarlægja af pöntun og fjarlægt af lista yfir virkar biðstöður.</span><span class="sxs-lookup"><span data-stu-id="606f7-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="606f7-151">Til að sjá allar biðstöður eða hlutmengi þeirra samkvæmt tiltekinni stöðu skal breyta gildi í svæði Sýna.</span><span class="sxs-lookup"><span data-stu-id="606f7-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     


