---
title: Stjórna pöntunum í bið
description: Þetta ferli sýnir hvernig setja sölupantanir viðskiptavina í bið, hvernig vinna með biðstöðu greiðsluferlis og hvernig fjarlægja bið af pöntun.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MCRHoldCodeTable, SalesTableListPage, SalesCreateOrder, SalesTable, MCRHoldCodeTrans, MCRHoldCheckOutOverride, MCRHoldCodeTable, MCRItemListCopying, MCRItemListTable, MCROMHoldList
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 27a5149812a8e478dae1d2385e6c139c9f635202
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010748"
---
# <a name="manage-order-holds"></a><span data-ttu-id="5b1a5-103">Stjórna pöntunum í bið</span><span class="sxs-lookup"><span data-stu-id="5b1a5-103">Manage order holds</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5b1a5-104">Þetta ferli sýnir hvernig setja sölupantanir viðskiptavina í bið, hvernig vinna með biðstöðu greiðsluferlis og hvernig fjarlægja bið af pöntun.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-104">This procedure demonstrates how to place customer sales orders on hold, how to work with order hold checkouts, and how to remove order holds.</span></span> <span data-ttu-id="5b1a5-105">Pöntun kann að vera sett í bið af ýmsum ástæðum.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-105">An order might be placed on hold for a variety of reasons.</span></span> <span data-ttu-id="5b1a5-106">Til dæmis gætirðu verið með pöntun í bið þar til hægt er að staðfesta aðsetur viðskiptavinar eða greiðsluhætti eða þar til stjórnandinn getur farið yfir lánamark viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-106">For example, you might hold an order until a customer address or payment method can be verified or until a manager can review the customer's credit limit.</span></span> <span data-ttu-id="5b1a5-107">Þegar pöntun er í bið er ekki hægt að vinna af vörugeymslu til afhendingar.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-107">While the order on hold, it cannot be processed by the warehouse for shipping.</span></span> 

<span data-ttu-id="5b1a5-108">Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-108">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-order-holds"></a><span data-ttu-id="5b1a5-109">Setja upp biðstöðu pöntunar</span><span class="sxs-lookup"><span data-stu-id="5b1a5-109">Set up order holds</span></span>
1. <span data-ttu-id="5b1a5-110">Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala og markaðssetning > Uppsetning > Sölupantanir > Biðkóðar pantana**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-110">Go to **Navigation pane > Modules > Sales and marketing > Setup > Sales orders > Order hold codes**.</span></span>
2. <span data-ttu-id="5b1a5-111">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-111">Click **New**.</span></span>
3. <span data-ttu-id="5b1a5-112">Í reitinn **Biðkóði** skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-112">In the **Hold code** field, type a value.</span></span> <span data-ttu-id="5b1a5-113">Til dæmis, skrifið Kalla aftur.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-113">For example, type 'Call back'.</span></span>  
4. <span data-ttu-id="5b1a5-114">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-114">In the **Description** field, type a value.</span></span>
    - <span data-ttu-id="5b1a5-115">Til dæmis, Pöntun haldið í bið eftir símtal frá viðskiptavinur.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-115">For example, Order held waiting for customer callback.</span></span>  
    - <span data-ttu-id="5b1a5-116">Annars er hægt að velja gátreitinn **Fjarlægja frátekningu** til að fjarlægja allar efnislegur frátekning úr pöntun þegar biðkóði er bætti við.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-116">Optionally, select the **Remove reservations** check box to remove any physical reservations from the order when this hold code is added.</span></span>  
5. <span data-ttu-id="5b1a5-117">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-117">Click **Save**.</span></span>

## <a name="place-order-on-hold"></a><span data-ttu-id="5b1a5-118">Setja pöntun í bið</span><span class="sxs-lookup"><span data-stu-id="5b1a5-118">Place order on hold</span></span>
1. <span data-ttu-id="5b1a5-119">Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala og markaðssetning > Sölupantanir > Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-119">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="5b1a5-120">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-120">Click **New**.</span></span>
3. <span data-ttu-id="5b1a5-121">Í reitnum **Viðskiptavinalykill** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-121">In the **Customer account** field, enter or select a value.</span></span>
4. <span data-ttu-id="5b1a5-122">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-122">Click **OK**.</span></span>
5. <span data-ttu-id="5b1a5-123">Í reitinn **Vörunúmer** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-123">In the **Item number** field, enter or select a value.</span></span>
6. <span data-ttu-id="5b1a5-124">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-124">In the **Quantity** field, enter a number.</span></span>
7. <span data-ttu-id="5b1a5-125">Á **Aðgerðasvæðinu** skal smellt á **Sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-125">On the **Action Pane**, click **Sales order**.</span></span>
8. <span data-ttu-id="5b1a5-126">Smellt er á **Biðstöður pantana**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-126">Click **Order holds**.</span></span>
9. <span data-ttu-id="5b1a5-127">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-127">Click **New**.</span></span>
10. <span data-ttu-id="5b1a5-128">Í svæði **Biðkóði** skal velja kóða sem stofnaður í fyrra undirverk.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-128">In the **Hold code** field, select the code you have created in the previous subtask.</span></span>
11. <span data-ttu-id="5b1a5-129">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-129">Click **Save**.</span></span>
12. <span data-ttu-id="5b1a5-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-130">Close the page.</span></span>
13. <span data-ttu-id="5b1a5-131">Farðu í **Sölu og markaðssetningu > sölupöntun > Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-131">Go to **Sales and marketing > Sales orders > All sales orders**.</span></span>
14. <span data-ttu-id="5b1a5-132">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-132">In the list, mark the selected row.</span></span> <span data-ttu-id="5b1a5-133">Pantanir sem núna í bið eru með merkt svæði „Ekki keyra“ og „Í biðstöðu“.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-133">Orders that are currently on hold have the "Do not process" and "Hold" fields marked.</span></span>
15. <span data-ttu-id="5b1a5-134">Á aðgerðasvæðinu er smellt á **Taka til og pakka**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-134">On the Action Pane, click **Pick and pack**.</span></span>

## <a name="manage-order-holds"></a><span data-ttu-id="5b1a5-135">Stjórna pöntunum í bið</span><span class="sxs-lookup"><span data-stu-id="5b1a5-135">Manage order holds</span></span>
1. <span data-ttu-id="5b1a5-136">Farðu í **Sala og markaðssetning > Sölupöntun > Opnar pantanir > Pantanir í bið**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-136">Go to **Sales and marketing > Sales orders > Open orders > Order holds**.</span></span> <span data-ttu-id="5b1a5-137">Síðan **Pantanir í bið** virkar sem vinnubekkur þar sem fá yfirlit yfir allar núgildandi og unnar biðstöður, vinna með þær og tengdar sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-137">**Order holds** page functions as a workbench where you can get an overview of all the current and processed holds, and handle them and associated sales orders.</span></span>     
2. <span data-ttu-id="5b1a5-138">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-138">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="5b1a5-139">Á **aðgerðarúðunni** skal smella á **Setja greiðsluferli í bið**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-139">On the **Action Pane**, click **Hold checkout**.</span></span>
4. <span data-ttu-id="5b1a5-140">Smella skal á **Greiðsluferli**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-140">Click **Check out**.</span></span>
5. <span data-ttu-id="5b1a5-141">Í listanum skal afmerkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-141">In the list, unmark the selected row.</span></span> <span data-ttu-id="5b1a5-142">Reiturinn **Greiðsluferli** birtir núna notandakenni þitt.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-142">The **Checkout out to** field now shows your user ID.</span></span>   
6. <span data-ttu-id="5b1a5-143">Smelltu á **Hreinsa greiðsluferli**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-143">Click **Clear checkout**.</span></span>
7. <span data-ttu-id="5b1a5-144">Í **aðgerðaglugganum** smellirðu á **Hreinsa biðstöðu**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-144">On the **Action Pane**, click **Clear hold**.</span></span>
    - <span data-ttu-id="5b1a5-145">Þegar þú tilbúið að fjarlægja í bið og leyfa pöntun halda áfram í næsta útskráningarskref verður að hreinsa í bið.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-145">When you are ready to remove the hold and allow the order to proceed to the next fulfilment step, you must clear the hold.</span></span> <span data-ttu-id="5b1a5-146">Ef ekki þarf að breyta pöntun má keyra aðgerð Hreinsa bið.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-146">If the order requires no changes, you can run the Clear holds action.</span></span> <span data-ttu-id="5b1a5-147">Þegar bið er hreinsa er hægt að nota aðgerð Hreinsa og breyta ef uppfæra þarf pöntun.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-147">However, you can use the Clear and modify action if, when clearing a hold, the order has to be updated.</span></span>      
    - <span data-ttu-id="5b1a5-148">Aðgerðin **Hreinsa og senda** á aðeins við þegar aðgerðin Símaver er notað.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-148">The **Clear and submit** action is only applicable when you use Call center functionality.</span></span>  
8. <span data-ttu-id="5b1a5-149">Smelltu á **Hreinsa biðstöðu**.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-149">Click **Clear holds**.</span></span> <span data-ttu-id="5b1a5-150">Biðstaða hefur verið fjarlægja af pöntun og fjarlægt af lista yfir virkar biðstöður.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-150">The hold has now been cleared from the order and removed from the list of Active holds.</span></span> <span data-ttu-id="5b1a5-151">Til að sjá allar biðstöður eða hlutmengi þeirra samkvæmt tiltekinni stöðu skal breyta gildi í svæði Sýna.</span><span class="sxs-lookup"><span data-stu-id="5b1a5-151">To see all the holds or their subset according to a specific status, change the value in the Show field.</span></span>     

