---
title: " Leiðréttingar á smásöluverði"
description: Þetta ferli mun fara í gegnum stofnun verðleiðrétting smásölu.
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
ms.openlocfilehash: 9427d3955e5442e301c416e2960e071ca5d85a3c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1550019"
---
# <a name="retail-price-adjustments"></a><span data-ttu-id="76615-103"> Leiðréttingar á smásöluverði</span><span class="sxs-lookup"><span data-stu-id="76615-103">Retail price adjustments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="76615-104">Þetta ferli mun fara í gegnum stofnun verðleiðrétting smásölu.</span><span class="sxs-lookup"><span data-stu-id="76615-104">This procedure will walk through creating a retail price adjustment.</span></span> <span data-ttu-id="76615-105">Verðleiðrétting smásölu getur setja söluverði vöru beint eða breyta hennar grunn söluverði eða söluverði verðsamnings.</span><span class="sxs-lookup"><span data-stu-id="76615-105">A retail price adjustment can set an item's sale price directly, or modify its base sale price or trade agreement sale price.</span></span> <span data-ttu-id="76615-106">Þessi aðferð notar USRT sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="76615-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="76615-107">Smella á Stjórnun verðlagningar og afslátta.</span><span class="sxs-lookup"><span data-stu-id="76615-107">Click Pricing and discount management.</span></span>
2. <span data-ttu-id="76615-108">Smellt er á flipanum verðleiðrétting.</span><span class="sxs-lookup"><span data-stu-id="76615-108">Click the Price adjustments tab.</span></span>
3. <span data-ttu-id="76615-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="76615-109">Click New.</span></span>
    * <span data-ttu-id="76615-110">Héðan er hægt að stofna allar algengustu notuð verð- og reglum, þar á meðal smásöluafslætti verðleiðréttingar, verðsamningabækur og tegund verðlagningu reglur.</span><span class="sxs-lookup"><span data-stu-id="76615-110">From here you can create all of the most commonly used price and discount rules, including retail discounts, price adjustments, trade agreement journals, and category pricing rules.</span></span>  
4. <span data-ttu-id="76615-111">Smelltu á Verðleiðrétting.</span><span class="sxs-lookup"><span data-stu-id="76615-111">Click Price adjustment.</span></span>
5. <span data-ttu-id="76615-112">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="76615-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="76615-113">Stækka línuhlutann.</span><span class="sxs-lookup"><span data-stu-id="76615-113">Expand the Lines section.</span></span>
7. <span data-ttu-id="76615-114">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="76615-114">Click Add.</span></span>
    * <span data-ttu-id="76615-115">Til dæmis, færa inn´ '81126' inn í svæðið Afurð.</span><span class="sxs-lookup"><span data-stu-id="76615-115">For this example, enter '81126' in the Product field.</span></span>    <span data-ttu-id="76615-116">Svo fært inn '10.0' í svæðinu prósenta Línuafsláttar.</span><span class="sxs-lookup"><span data-stu-id="76615-116">Then, enter '10.0' in the Discount percentage field.</span></span>  
    * <span data-ttu-id="76615-117">verðleiðréttingu með Afsláttarprósenta minnkar grunnsöluverð eða söluverð verðsamnings.</span><span class="sxs-lookup"><span data-stu-id="76615-117">A discount percentage type price adjustment will reduce a base sales price or trade agreement sales price.</span></span>  
8. <span data-ttu-id="76615-118">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="76615-118">Click Add.</span></span>
    * <span data-ttu-id="76615-119">Til dæmis, færa inn '81125' inn í svæðið Afurð.</span><span class="sxs-lookup"><span data-stu-id="76615-119">For this example, enter '81125' in the Product field.</span></span>    <span data-ttu-id="76615-120">Síðan skal velja 'upphæð staðgreiðsluafsláttar ‚ í Afsláttur aðferð svæði.</span><span class="sxs-lookup"><span data-stu-id="76615-120">Then, select 'Cash discount amount' in the Discount method field.</span></span>    <span data-ttu-id="76615-121">Að lokum, færið inn '5.0' í svæðinu upphæð staðgreiðsluafsláttar.</span><span class="sxs-lookup"><span data-stu-id="76615-121">Finally, enter '5.0' in the Cash discount amount field.</span></span>  
    * <span data-ttu-id="76615-122">Afsláttargerð upphæð staðgreiðsluafsláttar er tekin af grunnverði eða verð innkaupasamnings viðskipti upphæð.</span><span class="sxs-lookup"><span data-stu-id="76615-122">A Cash discount amount discount type is an amount taken off from a base price or a trade agreement price.</span></span>  
9. <span data-ttu-id="76615-123">Smellt er á verðflokkur.</span><span class="sxs-lookup"><span data-stu-id="76615-123">Click Price groups.</span></span>
    * <span data-ttu-id="76615-124">Veljið 'RP-Houston' í svæðinu Verð.</span><span class="sxs-lookup"><span data-stu-id="76615-124">Select 'RP-Houston' in the Price group field.</span></span>  
    * <span data-ttu-id="76615-125">Þetta verður að tengja verðleiðrétting Houston verslun.</span><span class="sxs-lookup"><span data-stu-id="76615-125">This will associate the Price adjustment to the Houston store.</span></span>  
10. <span data-ttu-id="76615-126">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="76615-126">Click Save.</span></span>
11. <span data-ttu-id="76615-127">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="76615-127">Close the page.</span></span>
12. <span data-ttu-id="76615-128">Í reitinn Staða er valið virkja.</span><span class="sxs-lookup"><span data-stu-id="76615-128">In the Status field, select 'Enabled'.</span></span>
13. <span data-ttu-id="76615-129">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="76615-129">Click Save.</span></span>
14. <span data-ttu-id="76615-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="76615-130">Close the page.</span></span>
15. <span data-ttu-id="76615-131">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="76615-131">Refresh the page.</span></span>

