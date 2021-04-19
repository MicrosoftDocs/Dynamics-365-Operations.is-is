---
title: Vinnutímasniðmát stofnuð
description: Sniðmát vinnutíma skilgreina vinnustundir yfir vikuna og eru notaðir til að mynda vinnutíma fyrir tímabil.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkTimeTable, WorkTimeCopyDayDialog, WorkPeriodTemplate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1885aba11b5c6878cc9dca615cea98b77b4df63f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811583"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="cd5b0-103">Vinnutímasniðmát stofnuð</span><span class="sxs-lookup"><span data-stu-id="cd5b0-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cd5b0-104">Sniðmát vinnutíma skilgreina vinnustundir yfir vikuna og eru notaðir til að mynda vinnutíma fyrir tímabil.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="cd5b0-105">Þessi verklýsing sýnir hvernig á að skilgreina sniðmát vinnutíma með því að nota eiginleikar vinnutímaröðunar til flokkunar á vinnutímabilum.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="cd5b0-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="cd5b0-107">Farið í Öll vinnusvæði > Líftímastjórnun tilfanga.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="cd5b0-108">Smellt er á sniðmát vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-108">Click Working time templates.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="cd5b0-109">Stofna sniðmát vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-109">Create working time template</span></span>
1. <span data-ttu-id="cd5b0-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-110">Click New.</span></span>
2. <span data-ttu-id="cd5b0-111">Færa inn gildi í reitnum sniðmát vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-111">In the Working time template field, type a value.</span></span>
3. <span data-ttu-id="cd5b0-112">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="cd5b0-113">Stækka Mánudagur hluti.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-113">Expand the Monday section.</span></span>
5. <span data-ttu-id="cd5b0-114">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-114">Click Add.</span></span>
6. <span data-ttu-id="cd5b0-115">Í reitinn Frá skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-115">In the From field, enter a time.</span></span>
    * <span data-ttu-id="cd5b0-116">Tilgreina tímasetningu þegar verk hefst á morgnana.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-116">Specify the time when work begins in the morning.</span></span>  
7. <span data-ttu-id="cd5b0-117">Í reitinn Til í skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-117">In the To field, enter a time.</span></span>
    * <span data-ttu-id="cd5b0-118">Tilgreina tímasetningu þegar starfsmenn taka hlé fyrir hádegisverð.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-118">Specify the time when workers break for lunch.</span></span>  
8. <span data-ttu-id="cd5b0-119">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-119">Click Add.</span></span>
9. <span data-ttu-id="cd5b0-120">Í reitinn Frá skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-120">In the From field, enter a time.</span></span>
    * <span data-ttu-id="cd5b0-121">Tilgreina tímasetningu þegar vinna hefst aftur eftir hádegisverð.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-121">Specify the time when work resumes after lunch.</span></span>  
10. <span data-ttu-id="cd5b0-122">Í reitinn Til í skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-122">In the To field, enter a time.</span></span>
    * <span data-ttu-id="cd5b0-123">Tilgreina lok vinnudagur.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="cd5b0-124">Afrita vinnutíma á allir dagar í viku</span><span class="sxs-lookup"><span data-stu-id="cd5b0-124">Replicate working times to all week days</span></span>
1. <span data-ttu-id="cd5b0-125">Smellt er á afrita dag.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-125">Click Copy day.</span></span>
    * <span data-ttu-id="cd5b0-126">Afrita skilgreiningar vinnutíma frá Mánudegi yfir á Þriðjudag.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
2. <span data-ttu-id="cd5b0-127">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-127">Click OK.</span></span>
3. <span data-ttu-id="cd5b0-128">Smellt er á afrita dag.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-128">Click Copy day.</span></span>
    * <span data-ttu-id="cd5b0-129">Afrita skilgreiningar vinnutíma frá Mánudegi til Miðvikudegi.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
4. <span data-ttu-id="cd5b0-130">Í reitnum til vikudags skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-130">In the To weekday field, select an option.</span></span>
5. <span data-ttu-id="cd5b0-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-131">Click OK.</span></span>
6. <span data-ttu-id="cd5b0-132">Smellt er á afrita dag.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-132">Click Copy day.</span></span>
    * <span data-ttu-id="cd5b0-133">Afrita skilgreiningar vinnutíma frá Mánudegi til Fimmtudag.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-133">Copy the working times definitions from Monday to Thursday.</span></span>  
7. <span data-ttu-id="cd5b0-134">Í reitnum til vikudags skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-134">In the To weekday field, select an option.</span></span>
8. <span data-ttu-id="cd5b0-135">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-135">Click OK.</span></span>
9. <span data-ttu-id="cd5b0-136">Smellt er á afrita dag.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-136">Click Copy day.</span></span>
    * <span data-ttu-id="cd5b0-137">Afrita skilgreiningar vinnutíma frá Mánudegi til Föstudags.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-137">Copy the working times definitions from Monday to Friday.</span></span>  
10. <span data-ttu-id="cd5b0-138">Í reitnum til vikudags skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-138">In the To weekday field, select an option.</span></span>
11. <span data-ttu-id="cd5b0-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-139">Click OK.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="cd5b0-140">Skilgreina tímahólf fyrir sérstakar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="cd5b0-140">Define time slots for special operations</span></span>
1. <span data-ttu-id="cd5b0-141">Stækka Föstudagur hluti.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-141">Expand the Friday section.</span></span>
2. <span data-ttu-id="cd5b0-142">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-142">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="cd5b0-143">Í reitinn eiginleiki skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-143">In the Property field, enter or select a value.</span></span>
4. <span data-ttu-id="cd5b0-144">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-144">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="cd5b0-145">Í reitinn eiginleiki skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-145">In the Property field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="cd5b0-146">Merkja helgardagar ekki hægt að sækja</span><span class="sxs-lookup"><span data-stu-id="cd5b0-146">Mark weekend days as closed for pickup</span></span>
1. <span data-ttu-id="cd5b0-147">Stækka Laugardagur hluti.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-147">Expand the Saturday section.</span></span>
2. <span data-ttu-id="cd5b0-148">Velja skal Já í svæði Lokað fyrir afhendingu.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-148">Select Yes in the Closed for pickup field.</span></span>
3. <span data-ttu-id="cd5b0-149">Stækka Sunnudagur hluti.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-149">Expand the Sunday section.</span></span>
4. <span data-ttu-id="cd5b0-150">Velja skal Já í svæði Lokað fyrir afhendingu.</span><span class="sxs-lookup"><span data-stu-id="cd5b0-150">Select Yes in the Closed for pickup field.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]