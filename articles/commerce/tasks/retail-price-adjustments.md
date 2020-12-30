---
title: Leiðréttingar á smásöluverði
description: Þetta ferli mun fara í gegnum stofnun verðleiðrétting Commerce.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, RetailDiscountPricingWorkspace, RetailPeriodicDiscount, RetailDiscountPriceGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83498fa0a0432cb182106d6d273cb6117ed0b094
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413194"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="d76b9-103">Leiðréttingar á smásöluverði</span><span class="sxs-lookup"><span data-stu-id="d76b9-103">Retail price adjustments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d76b9-104">Þetta ferli mun fara í gegnum stofnun verðleiðrétting Commerce.</span><span class="sxs-lookup"><span data-stu-id="d76b9-104">This procedure will walk through creating a commerce price adjustment.</span></span> <span data-ttu-id="d76b9-105">Verðleiðrétting getur stillt söluverð vöru beint eða breyta hennar grunn söluverði eða söluverði verðsamnings.</span><span class="sxs-lookup"><span data-stu-id="d76b9-105">A price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="d76b9-106">Þessi aðferð notar USRT sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="d76b9-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="d76b9-107">Smella á Stjórnun verðlagningar og afslátta.</span><span class="sxs-lookup"><span data-stu-id="d76b9-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="d76b9-108">Smellt er á flipanum verðleiðrétting.</span><span class="sxs-lookup"><span data-stu-id="d76b9-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="d76b9-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d76b9-109">Click New.</span></span>
    * <span data-ttu-id="d76b9-110">Héðan er hægt að stofna allar algengustu notuð verð- og reglum, þar á meðal afslætti verðleiðréttingar, verðsamningabækur og tegund verðlagningu reglur.</span><span class="sxs-lookup"><span data-stu-id="d76b9-110">From here you can create all of the most commonly used price and discount rules, including discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="d76b9-111">Smelltu á Verðleiðrétting.</span><span class="sxs-lookup"><span data-stu-id="d76b9-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="d76b9-112">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d76b9-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="d76b9-113">Stækka línuhlutann.</span><span class="sxs-lookup"><span data-stu-id="d76b9-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="d76b9-114">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d76b9-114">Click Add.</span></span>
    * <span data-ttu-id="d76b9-115">Til dæmis, færa inn´ '81126' inn í svæðið Afurð.</span><span class="sxs-lookup"><span data-stu-id="d76b9-115">For this example, enter '81126' in the Product field.</span></span> <span data-ttu-id="d76b9-116">Svo fært inn '10.0' í svæðinu prósenta Línuafsláttar.</span><span class="sxs-lookup"><span data-stu-id="d76b9-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="d76b9-117">verðleiðréttingu með Afsláttarprósenta minnkar grunnsöluverð eða söluverð verðsamnings.</span><span class="sxs-lookup"><span data-stu-id="d76b9-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="d76b9-118">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d76b9-118">Click Add.</span></span>
    * <span data-ttu-id="d76b9-119">Til dæmis, færa inn '81125' inn í svæðið Afurð.</span><span class="sxs-lookup"><span data-stu-id="d76b9-119">For this example, enter '81125' in the Product field.</span></span> <span data-ttu-id="d76b9-120">Síðan skal velja 'upphæð staðgreiðsluafsláttar ‚ í Afsláttur aðferð svæði.</span><span class="sxs-lookup"><span data-stu-id="d76b9-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="d76b9-121">Að lokum, færið inn '5.0' í svæðinu upphæð staðgreiðsluafsláttar.</span><span class="sxs-lookup"><span data-stu-id="d76b9-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="d76b9-122">Afsláttargerð upphæð staðgreiðsluafsláttar er tekin af grunnverði eða verð innkaupasamnings viðskipti upphæð.</span><span class="sxs-lookup"><span data-stu-id="d76b9-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="d76b9-123">Smellt er á verðflokkur.</span><span class="sxs-lookup"><span data-stu-id="d76b9-123">Click Price groups.</span></span>
    * <span data-ttu-id="d76b9-124">Veljið 'RP-Houston' í svæðinu Verð.</span><span class="sxs-lookup"><span data-stu-id="d76b9-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="d76b9-125">Þetta verður að tengja verðleiðrétting Houston verslun.</span><span class="sxs-lookup"><span data-stu-id="d76b9-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="d76b9-126">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d76b9-126">Click Save.</span></span>
11. <span data-ttu-id="d76b9-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d76b9-127">Close the page.</span></span>
12. <span data-ttu-id="d76b9-128">Í reitinn Staða er valið virkja.</span><span class="sxs-lookup"><span data-stu-id="d76b9-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="d76b9-129">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d76b9-129">Click Save.</span></span>
14. <span data-ttu-id="d76b9-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d76b9-130">Close the page.</span></span>
15. <span data-ttu-id="d76b9-131">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="d76b9-131">Refresh the page.</span></span>

