---
title: Skrá vörumóttöku í innkaupapöntun
description: Þetta efni útskýrir hvernig á að skrá móttöku á vörum beint á innkaupapöntun.
author: mkirknel
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1aa4043aca2e53eae32256a98d556c25b4ec1957
ms.sourcegitcommit: ac47e8679fb104515f7dcca509294264bd05d2b1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2020
ms.locfileid: "3454788"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a><span data-ttu-id="35568-103">Skrá vörumóttöku í innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="35568-103">Record the receipt of goods on the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="35568-104">Þetta efni útskýrir hvernig á að skrá móttöku á vörum beint á innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="35568-104">This topic explains how to record receipt of goods directly on a purchase order.</span></span> <span data-ttu-id="35568-105">Einnig er hægt að skrá innhreyfingu afurða í vöruhúsinu og síðan síðar skrá hana í innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="35568-105">It's also possible to register product receipt in the warehouse, and then later record it on the purchase order.</span></span> <span data-ttu-id="35568-106">Þetta verk er yfirleitt gert af innkaupaaðila eða af samræmingaraðila viðskiptaskulda.</span><span class="sxs-lookup"><span data-stu-id="35568-106">This task is typically done by a purchasing agent or an accounts payable coordinator.</span></span> <span data-ttu-id="35568-107">Dæmi sem eru sýnd í þessari handbók er hægt að nota sýnigögn USMF-fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="35568-107">The example shown in this guide can be used in the USMF demo data company.</span></span> <span data-ttu-id="35568-108">Dæmin inniheldur skref til að stofna einfalda innkaupapöntun, þannig að hægt er að spila ferlið sem leiðarvísi fyrir verk.</span><span class="sxs-lookup"><span data-stu-id="35568-108">The example includes steps to create a simple purchase order so that you can play the procedure as a task guide.</span></span> <span data-ttu-id="35568-109">Ef þú værir að nota ferlið á þín eigin gögn, myndirðu byrgja á undirverkinu **Færsla innhreyfingar á vörum**.</span><span class="sxs-lookup"><span data-stu-id="35568-109">If you were using the procedure on your own data, you would start at the **Record receipt of goods** subtask.</span></span>


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a><span data-ttu-id="35568-110">Undirbúa nýja innkaupapöntun vegna móttöku afurða.</span><span class="sxs-lookup"><span data-stu-id="35568-110">Prepare a new purchase order for receipt of goods</span></span>
1. <span data-ttu-id="35568-111">Farðu í **Skoðunarrúðu > Kerfiseiningar > Innkaup og aðföng > Innkaupapantanir > Allar innkaupapantanir**.</span><span class="sxs-lookup"><span data-stu-id="35568-111">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase orders > All purchase orders**.</span></span>
2. <span data-ttu-id="35568-112">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="35568-112">Select **New**.</span></span>
3. <span data-ttu-id="35568-113">Í svæðinu **Lánardrottnalykill** skal slá inn `US-101`.</span><span class="sxs-lookup"><span data-stu-id="35568-113">In the **Vendor account** field, enter `US-101`.</span></span>
4. <span data-ttu-id="35568-114">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="35568-114">Select **OK**.</span></span>
5. <span data-ttu-id="35568-115">Í reitinn **Vörunúmer** slærðu inn `M0001`.</span><span class="sxs-lookup"><span data-stu-id="35568-115">In the **Item number** field, enter `M0001`.</span></span>
6. <span data-ttu-id="35568-116">Í reitinn **Magn** skal slá inn `5`.</span><span class="sxs-lookup"><span data-stu-id="35568-116">In the **Quantity** field, enter `5`.</span></span>
7. <span data-ttu-id="35568-117">Í aðgerðasvæðinu velurðu **Innkaup**.</span><span class="sxs-lookup"><span data-stu-id="35568-117">On the Action Pane, select **Purchase**.</span></span>
8. <span data-ttu-id="35568-118">Veldu **Staðfesta**.</span><span class="sxs-lookup"><span data-stu-id="35568-118">Select **Confirm**.</span></span>

## <a name="record-receipt-of-goods"></a><span data-ttu-id="35568-119">Skrásetja viðtöku varnings</span><span class="sxs-lookup"><span data-stu-id="35568-119">Record receipt of goods</span></span>
1. <span data-ttu-id="35568-120">Í aðgerðasvæðinu velurðu **Móttaka**.</span><span class="sxs-lookup"><span data-stu-id="35568-120">On the Action Pane, select **Receive**.</span></span>
2. <span data-ttu-id="35568-121">Velja **Innhreyfingarskjal afurða**.</span><span class="sxs-lookup"><span data-stu-id="35568-121">Select **Product receipt**.</span></span> <span data-ttu-id="35568-122">Reiturinn **Magn** leyfir þér að velja mismunandi valkosti fyrir það magn sem á að taka á móti.</span><span class="sxs-lookup"><span data-stu-id="35568-122">The **Quantity** field allows you to select different options for the quantity that you want to receive.</span></span> <span data-ttu-id="35568-123">Til dæmis, ef áður hefur verið skráð magn í vöruhúsi, er hægt að velja **Skráð magn**.</span><span class="sxs-lookup"><span data-stu-id="35568-123">For example, if a quantity has previously been registered in the warehouse, you can select **Registered quantity**.</span></span> <span data-ttu-id="35568-124">Í þessu dæmis, notaðu gildið **Pantað magn**.</span><span class="sxs-lookup"><span data-stu-id="35568-124">For this example, use the value **Ordered quantity**.</span></span>
3. <span data-ttu-id="35568-125">Víkkið út hlutann **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="35568-125">Expand the **Overview** section.</span></span>
4. <span data-ttu-id="35568-126">Í reitinn **Móttaka afurða** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="35568-126">In the **Product receipt** field, type any value.</span></span> <span data-ttu-id="35568-127">Þetta svæði er notað til að færa inn tilvísun sem verður notað sem fylgiskjal fyrir færslubók innhreyfingarskjala afurða.</span><span class="sxs-lookup"><span data-stu-id="35568-127">This field is used to enter a reference that will be used as voucher for the product receipt journal.</span></span>  
5. <span data-ttu-id="35568-128">Stækka hlutann **Línur**.</span><span class="sxs-lookup"><span data-stu-id="35568-128">Expand the **Lines** section.</span></span>
6. <span data-ttu-id="35568-129">Stillið **Magn** á „4“.</span><span class="sxs-lookup"><span data-stu-id="35568-129">Set **Quantity** to '4'.</span></span> <span data-ttu-id="35568-130">Hér er hægt að tilgreina handvirkt magn sem fæst fyrir hverja línu í pöntun.</span><span class="sxs-lookup"><span data-stu-id="35568-130">Here you are able to manually specify the quantity that is being received for each line on the order.</span></span>  
7. <span data-ttu-id="35568-131">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="35568-131">Select **OK**.</span></span> <span data-ttu-id="35568-132">Vörurnar hafa nú verið skráð sem móttekið á innkaupapöntuninni og búið er að stofna færslubók fyrir innhreyfingarskjal afurða sem endurspegla þetta.</span><span class="sxs-lookup"><span data-stu-id="35568-132">The goods have now been recorded as received on the purchase order, and a product receipt journal has been created as document to reflect this.</span></span> <span data-ttu-id="35568-133">Hægt er að nota aðgerðina innhreyfing afurðar til að fara yfir færslubækur sem stofnaðar eru með innkaupapöntuninni og sjá hvað var móttekið og hvenær.</span><span class="sxs-lookup"><span data-stu-id="35568-133">You can use the Product receipt action to review the journals created with the purchase order, and see what was received, and when.</span></span>  

