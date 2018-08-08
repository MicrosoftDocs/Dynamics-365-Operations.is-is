---
title: "Tengsl þjónustuhluta"
description: "Hægt er að stofna þjónustuhlutatengsl á milli þjónustuhlutar og þjónustusamnings eða þjónustupöntunar."
author: ShylaThompson
manager: AnnBe
ms.date: 02/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceObjectRelation
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 03047b3eccf3c90d4cf7426ddaec83f10dbea1b0
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---

# <a name="service-object-relations"></a><span data-ttu-id="a1c57-103">Tengsl þjónustuhluta</span><span class="sxs-lookup"><span data-stu-id="a1c57-103">Service object relations</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a1c57-104">Hægt er að stofna þjónustuhlutatengsl á milli þjónustuhlutar og þjónustusamnings eða þjónustupöntunar.</span><span class="sxs-lookup"><span data-stu-id="a1c57-104">You can create service object relations between a service object and a service agreement or service order.</span></span> <span data-ttu-id="a1c57-105">Þegar tengsl eru stofnuð er þjónustuhluturinn tengdur við þjónustusamning eða þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="a1c57-105">When you create a relation, you attach the service object to the service agreement or service order.</span></span>

<span data-ttu-id="a1c57-106">Eftir að tengslin hafa verið stofnuð er hægt að tengja þjónustuhlutinn við allar línur á þjónustusamningnum eða þjónustupöntun.</span><span class="sxs-lookup"><span data-stu-id="a1c57-106">After the relation is created, you can attach the service object to any lines on the service agreement or service order.</span></span>

## <a name="template-boms"></a><span data-ttu-id="a1c57-107">Uppskriftir sniðmáts</span><span class="sxs-lookup"><span data-stu-id="a1c57-107">Template BOMs</span></span>

<span data-ttu-id="a1c57-108">Einnig er hægt að tilgreina sniðmátsuppskrift fyrir hlutatengslin.</span><span class="sxs-lookup"><span data-stu-id="a1c57-108">You can also specify a template BOM for the object relation.</span></span> <span data-ttu-id="a1c57-109">Sniðmátsuppskriftin er uppskrift fyrir hluti þar sem þjónusta fer fram.</span><span class="sxs-lookup"><span data-stu-id="a1c57-109">The template BOM is a bill of materials for the object on which you perform service.</span></span> <span data-ttu-id="a1c57-110">Ef hluti af þjónustuhlut þáttarins er skiptur út í þjónustuheimsókn er hægt að skrá breytinguna í þjónustuuppskrift með því að nota skjámyndina Þjónustuhlutir.</span><span class="sxs-lookup"><span data-stu-id="a1c57-110">If you replace a component part of the service object during a service visit, you can register this change in the service BOM by using the Service objects form.</span></span>

## <a name="example"></a><span data-ttu-id="a1c57-111">Dæmi</span><span class="sxs-lookup"><span data-stu-id="a1c57-111">Example</span></span>

<span data-ttu-id="a1c57-112">Í viðskiptavinasetri er stofnaður þjónustusamningur til að þjóna tveimur lyftum.</span><span class="sxs-lookup"><span data-stu-id="a1c57-112">You create a service agreement for servicing two elevators at a customer site.</span></span>
<span data-ttu-id="a1c57-113">Þjónustusamningurinn hefur auðkennið SAL-001.</span><span class="sxs-lookup"><span data-stu-id="a1c57-113">The service agreement has the identifier ID SAL-001.</span></span>

<span data-ttu-id="a1c57-114">Lyfturnar eru settar upp sem hlutir í skjámyndinni Þjónustuhlutir sem EL-S/1000 og EL-L/1000.</span><span class="sxs-lookup"><span data-stu-id="a1c57-114">The elevators are set up in the Service objects form as objects, EL-S/1000 and EL-L/1000.</span></span>

<span data-ttu-id="a1c57-115">Tengja skal þjónustuhlutina, EL-S/1000 og EL-L/1000, við þjónustusamninginn.</span><span class="sxs-lookup"><span data-stu-id="a1c57-115">You attach the service objects, EL-S/1000 and EL-L/1000, to the service agreement.</span></span>

<span data-ttu-id="a1c57-116">Ef óskað er eftir að skrá breytingar í uppskriftinni fyrir þjónustuhlutinn um leið og skipt er út hluta hlutarins, er þjónustuuppskrift tengd við þjónustuhlutatengsl, eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="a1c57-116">You want to register changes in the BOM for the service object as you replace component parts of the object, so you attach a service BOM to the service object relation, as described in the following table.</span></span>

| <span data-ttu-id="a1c57-117">Þjónustuhlutur</span><span class="sxs-lookup"><span data-stu-id="a1c57-117">Service object</span></span> | <span data-ttu-id="a1c57-118">Tengsl – Þjónustusamningur</span><span class="sxs-lookup"><span data-stu-id="a1c57-118">Relation – Service agreement</span></span> | <span data-ttu-id="a1c57-119">Þjónustuuppskrift</span><span class="sxs-lookup"><span data-stu-id="a1c57-119">Service BOM</span></span>   |
|----------------|------------------------------|---------------|
| <span data-ttu-id="a1c57-120">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="a1c57-120">EL-S/1000</span></span>      | <span data-ttu-id="a1c57-121">Kenni SAL-001</span><span class="sxs-lookup"><span data-stu-id="a1c57-121">ID SAL-001</span></span>                   | <span data-ttu-id="a1c57-122">EL-S/1000-uppskrift</span><span class="sxs-lookup"><span data-stu-id="a1c57-122">BOM-EL-S/1000</span></span> |
| <span data-ttu-id="a1c57-123">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="a1c57-123">EL-L/1000</span></span>      | <span data-ttu-id="a1c57-124">Kenni SAL-001</span><span class="sxs-lookup"><span data-stu-id="a1c57-124">ID SAL-001</span></span>                   | <span data-ttu-id="a1c57-125">BOM-EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="a1c57-125">BOM-EL-L/1000</span></span> |

<span data-ttu-id="a1c57-126">Nú er hægt að stofna þjónustusamningslínur með þessum hlutum vegna þess að komin eru á þjónustuhlutatengsl eins og lýst er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="a1c57-126">Because there are service object relations for the agreement, you can now create service agreement lines with these objects, as shown in the following table.</span></span>

| <span data-ttu-id="a1c57-127">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="a1c57-127">Transaction type</span></span> | <span data-ttu-id="a1c57-128">Tegund</span><span class="sxs-lookup"><span data-stu-id="a1c57-128">Category</span></span>           | <span data-ttu-id="a1c57-129">Þjónustuhlutur</span><span class="sxs-lookup"><span data-stu-id="a1c57-129">Service object</span></span> |
|------------------|--------------------|----------------|
| <span data-ttu-id="a1c57-130">Tími</span><span class="sxs-lookup"><span data-stu-id="a1c57-130">Hour</span></span>             | <span data-ttu-id="a1c57-131">Eftirlit</span><span class="sxs-lookup"><span data-stu-id="a1c57-131">Inspection</span></span>         | <span data-ttu-id="a1c57-132">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="a1c57-132">EL-S/1000</span></span>      |
| <span data-ttu-id="a1c57-133">Tími</span><span class="sxs-lookup"><span data-stu-id="a1c57-133">Hour</span></span>             | <span data-ttu-id="a1c57-134">Gírkassi hreinsaður</span><span class="sxs-lookup"><span data-stu-id="a1c57-134">Gear box cleaning</span></span>  | <span data-ttu-id="a1c57-135">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="a1c57-135">EL-S/1000</span></span>      |
| <span data-ttu-id="a1c57-136">Vara</span><span class="sxs-lookup"><span data-stu-id="a1c57-136">Item</span></span>             | <span data-ttu-id="a1c57-137">Hreinsun efnis</span><span class="sxs-lookup"><span data-stu-id="a1c57-137">Cleaning materials</span></span> | <span data-ttu-id="a1c57-138">EL-S/1000</span><span class="sxs-lookup"><span data-stu-id="a1c57-138">EL-S/1000</span></span>      |
| <span data-ttu-id="a1c57-139">Tími</span><span class="sxs-lookup"><span data-stu-id="a1c57-139">Hour</span></span>             | <span data-ttu-id="a1c57-140">Eftirlit</span><span class="sxs-lookup"><span data-stu-id="a1c57-140">Inspection</span></span>         | <span data-ttu-id="a1c57-141">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="a1c57-141">EL-L/1000</span></span>      |
| <span data-ttu-id="a1c57-142">Tími</span><span class="sxs-lookup"><span data-stu-id="a1c57-142">Hour</span></span>             | <span data-ttu-id="a1c57-143">Gírkassi hreinsaður</span><span class="sxs-lookup"><span data-stu-id="a1c57-143">Gearbox cleaning</span></span>   | <span data-ttu-id="a1c57-144">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="a1c57-144">EL-L/1000</span></span>      |
| <span data-ttu-id="a1c57-145">Vara</span><span class="sxs-lookup"><span data-stu-id="a1c57-145">Item</span></span>             | <span data-ttu-id="a1c57-146">Hreinsun efnis</span><span class="sxs-lookup"><span data-stu-id="a1c57-146">Cleaning materials</span></span> | <span data-ttu-id="a1c57-147">EL-L/1000</span><span class="sxs-lookup"><span data-stu-id="a1c57-147">EL-L/1000</span></span>      |

<span data-ttu-id="a1c57-148">Í þjónustuheimsókn verður að skipta út gírkassanum fyrir EL-S/1000 lyftuna.</span><span class="sxs-lookup"><span data-stu-id="a1c57-148">On a service visit, you have to replace the gearbox for elevator EL-S/1000.</span></span> <span data-ttu-id="a1c57-149">Til að skipta um þáttahluta hlutarins er hægt að fá aðgang að uppskriftarhönnuði með því að nota þjónustuhlutatengslin sem sett voru upp fyrir gildandi þjónustusamning.</span><span class="sxs-lookup"><span data-stu-id="a1c57-149">To replace a component part of the object, you can access the BOM Designer by using the service object relation that you set up for the current service agreement.</span></span>

<span data-ttu-id="a1c57-150">Aðgangur að uppskriftarhönnuði með því að nota þjónustuhlutatengsl</span><span class="sxs-lookup"><span data-stu-id="a1c57-150">Access the BOM Designer by using a service object relation</span></span>

1. <span data-ttu-id="a1c57-151">Þjónustusamningar</span><span class="sxs-lookup"><span data-stu-id="a1c57-151">Service agreements</span></span>
2. <span data-ttu-id="a1c57-152">Tvísmellið á þjónustusamning eða smellið á Þjónustusamning til að stofna þjónustusamning.</span><span class="sxs-lookup"><span data-stu-id="a1c57-152">Double-click a service agreement, or click Service agreement to create a service agreement.</span></span>
3. <span data-ttu-id="a1c57-153">Smellið á flipann „Setja upp“.</span><span class="sxs-lookup"><span data-stu-id="a1c57-153">Click the Setup tab.</span></span>
4. <span data-ttu-id="a1c57-154">Smellið á Þjónustuhluti til að tengja sniðmátsuppskrift við þjónustusamninginn.</span><span class="sxs-lookup"><span data-stu-id="a1c57-154">Click Service objects to attach a template BOM to the service agreement.</span></span>
5. <span data-ttu-id="a1c57-155">Í skjámyndinni Þjónustuhlutir skal smella á Hönnuð til að opna skjámyndina Hönnuður til að breyta sniðmátsuppskriftinni.</span><span class="sxs-lookup"><span data-stu-id="a1c57-155">In the Service objects form, click Designer to open the Designer form to modify the template BOM.</span></span>

## <a name="automatically-created-service-orders"></a><span data-ttu-id="a1c57-156">Stofna þjónustupantanir sjálfvirkt</span><span class="sxs-lookup"><span data-stu-id="a1c57-156">Automatically created service orders</span></span>

<span data-ttu-id="a1c57-157">Ef þjónustupantanir eru stofnaðar sjálfkrafa fyrir þjónustusamning verða þjónustuhlutatengslin í samningnum einnig stofnuð í þjónustupöntunum.</span><span class="sxs-lookup"><span data-stu-id="a1c57-157">If you automatically create service orders for a service agreement, the service object relations in the agreement are also created in the service orders.</span></span>


