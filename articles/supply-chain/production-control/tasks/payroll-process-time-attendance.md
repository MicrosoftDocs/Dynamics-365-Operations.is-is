---
title: "Virkja launaferli fyrir tíma og mætingu"
description: "Þessi verklýsing sýnir hvernig á að virkja launavinnslu í tími og mæting."
author: johanhoffmann
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 020bcb71d9b8495e61f3cf83c073771d6f2b2f26
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="7b29c-103">Virkja launaferli fyrir tíma og mætingu</span><span class="sxs-lookup"><span data-stu-id="7b29c-103">Enable the payroll process for time and attendance</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b29c-104">Þessi verklýsing sýnir hvernig á að virkja launavinnslu í tími og mæting.</span><span class="sxs-lookup"><span data-stu-id="7b29c-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="7b29c-105">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="7b29c-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="7b29c-106">Stofna launagerð með tengdum launataxta</span><span class="sxs-lookup"><span data-stu-id="7b29c-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="7b29c-107">Tími og viðvera > Setja upp > Laun > Launagerð</span><span class="sxs-lookup"><span data-stu-id="7b29c-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="7b29c-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7b29c-108">Click New.</span></span>
3. <span data-ttu-id="7b29c-109">Í reitinn launagerð skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7b29c-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="7b29c-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="7b29c-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7b29c-111">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="7b29c-111">Click Save.</span></span>
6. <span data-ttu-id="7b29c-112">Smellt er á Taxta.</span><span class="sxs-lookup"><span data-stu-id="7b29c-112">Click Rates.</span></span>
    * <span data-ttu-id="7b29c-113">Taxtar fyrir launagerðir eru settar upp fyrir tiltekin tímabil, og einstakir taxtar má stofna fyrir starfsmenn</span><span class="sxs-lookup"><span data-stu-id="7b29c-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="7b29c-114">Það er ekki alltaf nauðsynlegt að stofna taxta fyrir launagerðir fyrir tími og mæting.</span><span class="sxs-lookup"><span data-stu-id="7b29c-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="7b29c-115">Þessar upplýsingar gætu þegar verið til staðar í launakerfi sem notað til að mynda laun.</span><span class="sxs-lookup"><span data-stu-id="7b29c-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="7b29c-116">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7b29c-116">Click New.</span></span>
8. <span data-ttu-id="7b29c-117">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="7b29c-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="7b29c-118">Í reitinn taxtar skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="7b29c-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="7b29c-119">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="7b29c-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="7b29c-120">Stofna launasamning</span><span class="sxs-lookup"><span data-stu-id="7b29c-120">Create a pay agreement</span></span>
1. <span data-ttu-id="7b29c-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7b29c-121">Close the page.</span></span>
2. <span data-ttu-id="7b29c-122">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7b29c-122">Close the page.</span></span>
3. <span data-ttu-id="7b29c-123">Fara á launasamninga.</span><span class="sxs-lookup"><span data-stu-id="7b29c-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="7b29c-124">Tími og viðvera > Setja upp > Launagerð</span><span class="sxs-lookup"><span data-stu-id="7b29c-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="7b29c-125">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7b29c-125">Click New.</span></span>
5. <span data-ttu-id="7b29c-126">Færa inn gildi í svæðinu launasamningur.</span><span class="sxs-lookup"><span data-stu-id="7b29c-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="7b29c-127">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="7b29c-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="7b29c-128">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="7b29c-128">Click Save.</span></span>
8. <span data-ttu-id="7b29c-129">Smellið á samningslínur.</span><span class="sxs-lookup"><span data-stu-id="7b29c-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="7b29c-130">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7b29c-130">Click New.</span></span>
10. <span data-ttu-id="7b29c-131">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="7b29c-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="7b29c-132">Færa inn eða veljið gildi í svæðinu gerð forstillingar.</span><span class="sxs-lookup"><span data-stu-id="7b29c-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="7b29c-133">Færa inn eða veljið gildi í svæðinu launagerð.</span><span class="sxs-lookup"><span data-stu-id="7b29c-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="7b29c-134">Setja upp launasamning fyrir tíma og skráningu starfsmann</span><span class="sxs-lookup"><span data-stu-id="7b29c-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="7b29c-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7b29c-135">Close the page.</span></span>
2. <span data-ttu-id="7b29c-136">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7b29c-136">Close the page.</span></span>
3. <span data-ttu-id="7b29c-137">Fara í starfsmaður sem sinnir tímaskráningu</span><span class="sxs-lookup"><span data-stu-id="7b29c-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="7b29c-138">Tími og viðvera > Setja upp > Starfsmaður sem sinnir tímaskráningu</span><span class="sxs-lookup"><span data-stu-id="7b29c-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="7b29c-139">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7b29c-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="7b29c-140">Smellið á flipann Ráðningar.</span><span class="sxs-lookup"><span data-stu-id="7b29c-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="7b29c-141">Útvíkka hlutann tímaskráning.</span><span class="sxs-lookup"><span data-stu-id="7b29c-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="7b29c-142">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="7b29c-142">Click Edit.</span></span>
8. <span data-ttu-id="7b29c-143">Sláðu inn eða veldu gildi í reitnum launasamningur.</span><span class="sxs-lookup"><span data-stu-id="7b29c-143">In the Pay agreement field, enter or select a value.</span></span>

