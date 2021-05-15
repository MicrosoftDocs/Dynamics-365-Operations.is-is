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
ms.openlocfilehash: ed1981b7c1427c902f237f0aa95f63e89bc345ab
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920930"
---
# <a name="create-working-time-templates"></a><span data-ttu-id="7798a-103">Vinnutímasniðmát stofnuð</span><span class="sxs-lookup"><span data-stu-id="7798a-103">Create working time templates</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7798a-104">Sniðmát vinnutíma skilgreina vinnustundir yfir vikuna og eru notaðir til að mynda vinnutíma fyrir tímabil.</span><span class="sxs-lookup"><span data-stu-id="7798a-104">Working time templates define the working hours throughout a week and are used to generate working times for a period of time.</span></span> <span data-ttu-id="7798a-105">Þessi verklýsing sýnir hvernig á að skilgreina sniðmát vinnutíma með því að nota eiginleikar vinnutímaröðunar til flokkunar á vinnutímabilum.</span><span class="sxs-lookup"><span data-stu-id="7798a-105">This procedure shows you how to define a working time template using working time scheduling properties for categorizing working time intervals.</span></span> <span data-ttu-id="7798a-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="7798a-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="7798a-107">Farið í **Vinnusvæði > Líftímastjórnun tilfanga**.</span><span class="sxs-lookup"><span data-stu-id="7798a-107">Go to **Workspaces > Resource lifecycle management**.</span></span>
1. <span data-ttu-id="7798a-108">Veljið **Sniðmát vinnutíma**.</span><span class="sxs-lookup"><span data-stu-id="7798a-108">Select **Working time templates**.</span></span>

## <a name="create-working-time-template"></a><span data-ttu-id="7798a-109">Stofna sniðmát vinnutíma.</span><span class="sxs-lookup"><span data-stu-id="7798a-109">Create working time template</span></span>

1. <span data-ttu-id="7798a-110">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="7798a-110">Select **New**.</span></span>
1. <span data-ttu-id="7798a-111">Færa inn gildi í reitnum **Sniðmát vinnutíma**.</span><span class="sxs-lookup"><span data-stu-id="7798a-111">In the **Working time template** field, type a value.</span></span>
1. <span data-ttu-id="7798a-112">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7798a-112">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="7798a-113">Stækka **Mánudagur** hlutann.</span><span class="sxs-lookup"><span data-stu-id="7798a-113">Expand the **Monday** section.</span></span>
1. <span data-ttu-id="7798a-114">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="7798a-114">Select **Add**.</span></span>
1. <span data-ttu-id="7798a-115">Í reitinn **Frá** skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="7798a-115">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="7798a-116">Tilgreina tímasetningu þegar verk hefst á morgnana.</span><span class="sxs-lookup"><span data-stu-id="7798a-116">Specify the time when work begins in the morning.</span></span>  
1. <span data-ttu-id="7798a-117">Í reitinn **Til** í skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="7798a-117">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="7798a-118">Tilgreina tímasetningu þegar starfsmenn taka hlé fyrir hádegisverð.</span><span class="sxs-lookup"><span data-stu-id="7798a-118">Specify the time when workers break for lunch.</span></span>  
1. <span data-ttu-id="7798a-119">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="7798a-119">Select **Add**.</span></span>
1. <span data-ttu-id="7798a-120">Í reitinn **Frá** skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="7798a-120">In the **From** field, enter a time.</span></span>
    * <span data-ttu-id="7798a-121">Tilgreina tímasetningu þegar vinna hefst aftur eftir hádegisverð.</span><span class="sxs-lookup"><span data-stu-id="7798a-121">Specify the time when work resumes after lunch.</span></span>  
1. <span data-ttu-id="7798a-122">Í reitinn **Til** í skal slá inn tíma.</span><span class="sxs-lookup"><span data-stu-id="7798a-122">In the **To** field, enter a time.</span></span>
    * <span data-ttu-id="7798a-123">Tilgreina lok vinnudagur.</span><span class="sxs-lookup"><span data-stu-id="7798a-123">Specify the end of the work day.</span></span>  

## <a name="replicate-working-times-to-all-week-days"></a><span data-ttu-id="7798a-124">Afrita vinnutíma á allir dagar í viku</span><span class="sxs-lookup"><span data-stu-id="7798a-124">Replicate working times to all week days</span></span>

1. <span data-ttu-id="7798a-125">Veljið **Afrita dag**.</span><span class="sxs-lookup"><span data-stu-id="7798a-125">Select **Copy day**.</span></span>
    * <span data-ttu-id="7798a-126">Afrita skilgreiningar vinnutíma frá Mánudegi yfir á Þriðjudag.</span><span class="sxs-lookup"><span data-stu-id="7798a-126">Copy the working times definitions from Monday to Tuesday.</span></span>  
1. <span data-ttu-id="7798a-127">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7798a-127">Select **OK**.</span></span>
1. <span data-ttu-id="7798a-128">Veljið **Afrita dag**.</span><span class="sxs-lookup"><span data-stu-id="7798a-128">Select **Copy day**.</span></span>
    * <span data-ttu-id="7798a-129">Afrita skilgreiningar vinnutíma frá Mánudegi til Miðvikudegi.</span><span class="sxs-lookup"><span data-stu-id="7798a-129">Copy the working times definitions from Monday to Wednesday.</span></span>  
1. <span data-ttu-id="7798a-130">Í reitnum **Til vikudags** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="7798a-130">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="7798a-131">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7798a-131">Select **OK**.</span></span>
1. <span data-ttu-id="7798a-132">Veljið **Afrita dag**.</span><span class="sxs-lookup"><span data-stu-id="7798a-132">Select **Copy day**.</span></span>
    * <span data-ttu-id="7798a-133">Afrita skilgreiningar vinnutíma frá Mánudegi til Fimmtudag.</span><span class="sxs-lookup"><span data-stu-id="7798a-133">Copy the working times definitions from Monday to Thursday.</span></span>  
1. <span data-ttu-id="7798a-134">Í reitnum **Til vikudags** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="7798a-134">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="7798a-135">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7798a-135">Select **OK**.</span></span>
1. <span data-ttu-id="7798a-136">Veljið **Afrita dag**.</span><span class="sxs-lookup"><span data-stu-id="7798a-136">Select **Copy day**.</span></span>
    * <span data-ttu-id="7798a-137">Afrita skilgreiningar vinnutíma frá Mánudegi til Föstudags.</span><span class="sxs-lookup"><span data-stu-id="7798a-137">Copy the working times definitions from Monday to Friday.</span></span>  
1. <span data-ttu-id="7798a-138">Í reitnum **Til vikudags** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="7798a-138">In the **To weekday** field, select an option.</span></span>
1. <span data-ttu-id="7798a-139">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7798a-139">Select **OK**.</span></span>

## <a name="define-time-slots-for-special-operations"></a><span data-ttu-id="7798a-140">Skilgreina tímahólf fyrir sérstakar aðgerðir</span><span class="sxs-lookup"><span data-stu-id="7798a-140">Define time slots for special operations</span></span>

1. <span data-ttu-id="7798a-141">Stækka **Föstudagur** hlutann.</span><span class="sxs-lookup"><span data-stu-id="7798a-141">Expand the **Friday** section.</span></span>
1. <span data-ttu-id="7798a-142">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="7798a-142">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="7798a-143">Í reitinn **Eiginleiki** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7798a-143">In the **Property** field, enter or select a value.</span></span>
1. <span data-ttu-id="7798a-144">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="7798a-144">In the list, find and select the desired record.</span></span>
1. <span data-ttu-id="7798a-145">Í reitinn **Eiginleiki** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="7798a-145">In the **Property** field, enter or select a value.</span></span>

## <a name="mark-weekend-days-as-closed-for-pickup"></a><span data-ttu-id="7798a-146">Merkja helgardagar ekki hægt að sækja</span><span class="sxs-lookup"><span data-stu-id="7798a-146">Mark weekend days as closed for pickup</span></span>

1. <span data-ttu-id="7798a-147">Stækka **Laugardagur** hlutann.</span><span class="sxs-lookup"><span data-stu-id="7798a-147">Expand the **Saturday** section.</span></span>
1. <span data-ttu-id="7798a-148">Velja skal *Já* í reitnum **Lokað fyrir afhendingu**.</span><span class="sxs-lookup"><span data-stu-id="7798a-148">Select *Yes* in the **Closed for pickup** field.</span></span>
1. <span data-ttu-id="7798a-149">Stækka **Sunnudagur** hlutann.</span><span class="sxs-lookup"><span data-stu-id="7798a-149">Expand the **Sunday** section.</span></span>
1. <span data-ttu-id="7798a-150">Velja skal *Já* í reitnum **Lokað fyrir afhendingu**.</span><span class="sxs-lookup"><span data-stu-id="7798a-150">Select *Yes* in the **Closed for pickup** field.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]