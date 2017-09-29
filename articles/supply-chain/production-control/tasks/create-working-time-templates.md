--- 
title: "Vinnutímasniðmát stofnuð"
description: "Sniðmát vinnutíma skilgreina vinnustundir yfir vikuna og eru notaðir til að mynda vinnutíma fyrir tímabil."
author: sorenva
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2df37747601618fc3d45734152a05aedd39500a6
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="create-working-time-templates"></a><span data-ttu-id="cab83-103">Vinnutímasniðmát stofnuð</span><span class="sxs-lookup"><span data-stu-id="cab83-103">Create working time templates</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cab83-104">Sniðmát vinnutíma skilgreina vinnustundir yfir vikuna og eru notaðir til að mynda vinnutíma fyrir tímabil.</span><span class="sxs-lookup"><span data-stu-id="cab83-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="cab83-105">Þessi verklýsing sýnir hvernig á að skilgreina sniðmát vinnutíma með því að nota eiginleikar vinnutímaröðunar til flokkunar á vinnutímabilum.</span><span class="sxs-lookup"><span data-stu-id="cab83-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="cab83-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="cab83-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="cab83-107">Farið í Öll vinnusvæði > Líftímastjórnun tilfanga.</span><span class="sxs-lookup"><span data-stu-id="cab83-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="cab83-108">Smellt er á sniðmát vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="cab83-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="cab83-109">Stofna sniðmát vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="cab83-109">Create working time template</span></span>
1. <span data-ttu-id="cab83-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="cab83-110">Click New.</span></span>
2. <span data-ttu-id="cab83-111">Færa inn gildi í reitnum sniðmát vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="cab83-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="cab83-112">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="cab83-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="cab83-113">Stækka Mánudagur hluti.</span><span class="sxs-lookup"><span data-stu-id="cab83-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="cab83-114">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="cab83-114">Click Add.</span></span>
6. <span data-ttu-id="cab83-115">Í reitinn Frá skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="cab83-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="cab83-116">Tilgreina tímasetningu þegar verk hefst á morgnana.</span><span class="sxs-lookup"><span data-stu-id="cab83-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="cab83-117">Í reitinn Til í skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="cab83-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="cab83-118">Tilgreina tímasetningu þegar starfsmenn taka hlé fyrir hádegisverð.</span><span class="sxs-lookup"><span data-stu-id="cab83-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="cab83-119">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="cab83-119">Click Add.</span></span>
9. <span data-ttu-id="cab83-120">Í reitinn Frá skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="cab83-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="cab83-121">Tilgreina tímasetningu þegar vinna hefst aftur eftir hádegisverð.</span><span class="sxs-lookup"><span data-stu-id="cab83-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="cab83-122">Í reitinn Til í skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="cab83-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="cab83-123">Tilgreina lok vinnudagur.</span><span class="sxs-lookup"><span data-stu-id="cab83-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="cab83-124">Afrita vinnutíma á allir dagar í viku</span><span class="sxs-lookup"><span data-stu-id="cab83-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="cab83-125">Smellt er á afrita dag.</span><span class="sxs-lookup"><span data-stu-id="cab83-125">Click Copy day.</span></span>
    * <span data-ttu-id="cab83-126">Afrita skilgreiningar vinnutíma frá Mánudegi yfir á Þriðjudag.</span><span class="sxs-lookup"><span data-stu-id="cab83-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="cab83-127">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cab83-127">Click OK.</span></span>
3. <span data-ttu-id="cab83-128">Smellt er á afrita dag.</span><span class="sxs-lookup"><span data-stu-id="cab83-128">Click Copy day.</span></span>
    * <span data-ttu-id="cab83-129">Afrita skilgreiningar vinnutíma frá Mánudegi til Miðvikudegi.</span><span class="sxs-lookup"><span data-stu-id="cab83-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="cab83-130">Í reitnum til vikudags skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="cab83-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="cab83-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cab83-131">Click OK.</span></span>
6. <span data-ttu-id="cab83-132">Smellt er á afrita dag.</span><span class="sxs-lookup"><span data-stu-id="cab83-132">Click Copy day.</span></span>
    * <span data-ttu-id="cab83-133">Afrita skilgreiningar vinnutíma frá Mánudegi til Fimmtudag.</span><span class="sxs-lookup"><span data-stu-id="cab83-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="cab83-134">Í reitnum til vikudags skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="cab83-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="cab83-135">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cab83-135">Click OK.</span></span>
9. <span data-ttu-id="cab83-136">Smellt er á afrita dag.</span><span class="sxs-lookup"><span data-stu-id="cab83-136">Click Copy day.</span></span>
    * <span data-ttu-id="cab83-137">Afrita skilgreiningar vinnutíma frá Mánudegi til Föstudags.</span><span class="sxs-lookup"><span data-stu-id="cab83-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="cab83-138">Í reitnum til vikudags skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="cab83-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="cab83-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cab83-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="cab83-140">Skilgreina tímahólf fyrir sérstakar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="cab83-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="cab83-141">Stækka Föstudagur hluti.</span><span class="sxs-lookup"><span data-stu-id="cab83-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="cab83-142">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="cab83-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="cab83-143">Í reitinn eiginleiki skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="cab83-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="cab83-144">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="cab83-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="cab83-145">Í reitinn eiginleiki skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="cab83-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="cab83-146">Merkja helgardagar ekki hægt að sækja</span><span class="sxs-lookup"><span data-stu-id="cab83-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="cab83-147">Stækka Laugardagur hluti.</span><span class="sxs-lookup"><span data-stu-id="cab83-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="cab83-148">Velja skal Já í svæði Lokað fyrir afhendingu.</span><span class="sxs-lookup"><span data-stu-id="cab83-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="cab83-149">Stækka Sunnudagur hluti.</span><span class="sxs-lookup"><span data-stu-id="cab83-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="cab83-150">Velja skal Já í svæði Lokað fyrir afhendingu.</span><span class="sxs-lookup"><span data-stu-id="cab83-150">Select Yes in the Closed for pickup field.</span></span>


