---
title: Stofna rekstrartilföng
description: Rekstrartilföng framkvæmir verkþætti verks eða framleiðsluferli.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c4836b6f51f0be5afbdb55838dde27b3aaec5c1
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146975"
---
# <a name="create-an-operations-resource"></a><span data-ttu-id="751d3-103">Stofna rekstrartilföng</span><span class="sxs-lookup"><span data-stu-id="751d3-103">Create an operations resource</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="751d3-104">Rekstrartilföng framkvæmir verkþætti verks eða framleiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="751d3-104">An operations resource performs the activities of a project or a production process.</span></span> <span data-ttu-id="751d3-105">Þessi ferli sýnir hvernig á að skilgreina gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="751d3-105">This procedures shows you how to define an operations resource.</span></span> <span data-ttu-id="751d3-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="751d3-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="751d3-107">Fara á tilföng</span><span class="sxs-lookup"><span data-stu-id="751d3-107">Go to Resources.</span></span>
2. <span data-ttu-id="751d3-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="751d3-108">Click New.</span></span>
3. <span data-ttu-id="751d3-109">Í reitinn Tilfang skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="751d3-109">In the Resource field, type a value.</span></span>
4. <span data-ttu-id="751d3-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="751d3-110">In the Description field, type a value.</span></span>

## <a name="define-capacity-and-consumption-parameters"></a><span data-ttu-id="751d3-111">Skilgreina afkastageta og notkunarfæribreytur</span><span class="sxs-lookup"><span data-stu-id="751d3-111">Define capacity and consumption parameters</span></span>
1. <span data-ttu-id="751d3-112">Stækka hlutann aðgerð.</span><span class="sxs-lookup"><span data-stu-id="751d3-112">Expand the Operation section.</span></span>
2. <span data-ttu-id="751d3-113">Færið inn tölu í reitinn úrkastsprósenta.</span><span class="sxs-lookup"><span data-stu-id="751d3-113">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="751d3-114">Sláið inn eða veldu gildi í reitnum Setja upp flokkur.</span><span class="sxs-lookup"><span data-stu-id="751d3-114">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="751d3-115">Tilgreina kostnaðartegund sem skilgreinir hvernig á að gera grein fyrir kostnað við uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="751d3-115">Specify the cost category that defines how to account for the cost of setup.</span></span>  
4. <span data-ttu-id="751d3-116">Færa inn eða veljið gildi í reitinn flokkur keyrslutíma</span><span class="sxs-lookup"><span data-stu-id="751d3-116">In the Run time category field, enter or select a value.</span></span>
    * <span data-ttu-id="751d3-117">Tilgreina kostnaðartegund sem skilgreinir hvernig á að gera grein fyrir kostnað við keyrslutíma.</span><span class="sxs-lookup"><span data-stu-id="751d3-117">Specify the cost category that defines how to account for the cost of run time.</span></span>  
5. <span data-ttu-id="751d3-118">Sláið inn eða veldu gildi í reitnum magntegund.</span><span class="sxs-lookup"><span data-stu-id="751d3-118">In the Quantity category field, enter or select a value.</span></span>
    * <span data-ttu-id="751d3-119">Tilgreina kostnaðartegund sem skilgreinir hvernig á að gera grein kostnaði vegna tilfanga á grundvelli úttaksmagns.</span><span class="sxs-lookup"><span data-stu-id="751d3-119">Specify the cost category that defines how to account for the resource cost based on the output quantity.</span></span>  
6. <span data-ttu-id="751d3-120">Í reitnum Eining afkastagetu skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="751d3-120">In the Capacity unit field, select an option.</span></span>
    * <span data-ttu-id="751d3-121">Tilgreinið eininguna til að sýna afkastagetu rekstrartilfanga.</span><span class="sxs-lookup"><span data-stu-id="751d3-121">Specify the unit in which to express the capacity of the operations resource.</span></span>  
7. <span data-ttu-id="751d3-122">Í reitinn Afkastageta skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="751d3-122">In the Capacity field, enter a number.</span></span>
8. <span data-ttu-id="751d3-123">Færið inn tölu í reitinn Skilvirkniprósenta.</span><span class="sxs-lookup"><span data-stu-id="751d3-123">In the Efficiency percentage field, enter a number.</span></span>
    * <span data-ttu-id="751d3-124">Tilgreina skilvirkni sem búist er við frá rekstrartilföng.</span><span class="sxs-lookup"><span data-stu-id="751d3-124">Specify the efficiency that you expect from the operations resource.</span></span> <span data-ttu-id="751d3-125">Skilvirkniprósenta leiðréttir gegnumstreymi rekstrartilfanga og hefur áhrif á tíma sem er frátekin fyrir tilfang.</span><span class="sxs-lookup"><span data-stu-id="751d3-125">The efficiency percentage adjusts the throughput of the operations resource and affects the time that is reserved for the resource.</span></span>  
9. <span data-ttu-id="751d3-126">Færið inn tölu í Aðgerðaröðun prósentusvæðinu.</span><span class="sxs-lookup"><span data-stu-id="751d3-126">In the Operations scheduling percentage field, enter a number.</span></span>
    * <span data-ttu-id="751d3-127">Tilgreinið hámarkshlutfall afkastagetu rekstrartilfanga sem á að nota í aðgerðaröðun.</span><span class="sxs-lookup"><span data-stu-id="751d3-127">Specify the maximum percentage of capacity of the operations resource that you want to use in operations scheduling.</span></span>  
10. <span data-ttu-id="751d3-128">Veljið Já í svæðinu takmörkuð Afkastageta.</span><span class="sxs-lookup"><span data-stu-id="751d3-128">Select Yes in the Finite capacity field.</span></span>
    * <span data-ttu-id="751d3-129">Þessi valkostur stilltur á Já ef rekstrartilföng skuli raðað á grundvelli raunverulega afkastagetu sem er tiltækt, og ef taka skal tillit til fyrirliggjandi frátekningar á afkastagetu.</span><span class="sxs-lookup"><span data-stu-id="751d3-129">Set this option to Yes if the operations resource should be scheduled based on the actual capacity that is available, and if existing capacity reservations should be considered.</span></span> <span data-ttu-id="751d3-130">Ef þessi valkostur er stilltur á Nei, er gert ráð fyrir að rekstrartilföng hafa ótakmarkaða afköst, og gæti tilföngin gætu verið yfirbókaður.</span><span class="sxs-lookup"><span data-stu-id="751d3-130">If this option is set to No, the operations resource is assumed to have infinite capacity, and the resource might be overbooked.</span></span>  
11. <span data-ttu-id="751d3-131">Velja skal Já í svæðinu Flöskuhálstilfang.</span><span class="sxs-lookup"><span data-stu-id="751d3-131">Select Yes in the Bottleneck resource field.</span></span>

## <a name="define-working-times"></a><span data-ttu-id="751d3-132">Skilgreina vinnutíma</span><span class="sxs-lookup"><span data-stu-id="751d3-132">Define working times</span></span>
1. <span data-ttu-id="751d3-133">Stækka Dagatals hluta.</span><span class="sxs-lookup"><span data-stu-id="751d3-133">Expand the Calendars section.</span></span>
2. <span data-ttu-id="751d3-134">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="751d3-134">Click Add.</span></span>
3. <span data-ttu-id="751d3-135">Sláið inn eða veldu gildi í reitnum dagatal.</span><span class="sxs-lookup"><span data-stu-id="751d3-135">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="751d3-136">Tilgreina vinnutímadagatal sem skilgreinir afkastagetu (í klukkustundum) tilfanganna.</span><span class="sxs-lookup"><span data-stu-id="751d3-136">Specify the working time calendar that defines the capacity (in hours) of the resource.</span></span>  
4. <span data-ttu-id="751d3-137">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="751d3-137">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="751d3-138">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="751d3-138">In the list, click the link in the selected row.</span></span>

## <a name="define-resource-capabilities"></a><span data-ttu-id="751d3-139">Skilgreina möguleika tilfanga</span><span class="sxs-lookup"><span data-stu-id="751d3-139">Define resource capabilities</span></span>
1. <span data-ttu-id="751d3-140">Útvíkka hlutann Getu.</span><span class="sxs-lookup"><span data-stu-id="751d3-140">Expand the Capabilities section.</span></span>
2. <span data-ttu-id="751d3-141">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="751d3-141">Click Add.</span></span>
    * <span data-ttu-id="751d3-142">Geta er hæfni rekstrartilfanga til að framkvæma tiltekinn verkþátt.</span><span class="sxs-lookup"><span data-stu-id="751d3-142">A capability is the ability of an operations resource to perform a particular activity.</span></span> <span data-ttu-id="751d3-143">Röðunarvél úthlutar tilföng með því að láta tilfangaþörfum á hvern verkþátt samsvara getu tiltækar rekstrartilföng.</span><span class="sxs-lookup"><span data-stu-id="751d3-143">The scheduling engine allocates resources by matching the resource requirements of each activity to the capabilities of the available operations resources.</span></span>  
3. <span data-ttu-id="751d3-144">Í reitinn Geta skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="751d3-144">In the Capability field, enter or select a value.</span></span>
4. <span data-ttu-id="751d3-145">Í reitinn Stig skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="751d3-145">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="751d3-146">Tilgreinið þá færni sem vinnur tilfang á getu.</span><span class="sxs-lookup"><span data-stu-id="751d3-146">Specify the level of proficiency by which the resource processes the capability.</span></span>  
5. <span data-ttu-id="751d3-147">Í reitinn forgangur skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="751d3-147">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="751d3-148">Tilgreinið forgang rekstrartilföng með tilliti til getu.</span><span class="sxs-lookup"><span data-stu-id="751d3-148">Specify the priority of the operations resource with respect to the capability.</span></span> <span data-ttu-id="751d3-149">Þegar er raðað eftir forgangi, rekstrartilföng með mesta forgang (lægsta tölugildi) er valið fyrst.</span><span class="sxs-lookup"><span data-stu-id="751d3-149">When scheduling by priority, the operations resource with the highest priority (lowest numeric value) is selected first.</span></span>  

## <a name="assign-resource-to-resource-group"></a><span data-ttu-id="751d3-150">Úthluta tilföngum á tilfangaflokk</span><span class="sxs-lookup"><span data-stu-id="751d3-150">Assign resource to resource group</span></span>
1. <span data-ttu-id="751d3-151">Útvíkka hlutann tilfangaflokkur.</span><span class="sxs-lookup"><span data-stu-id="751d3-151">Expand the Resource groups section.</span></span>
2. <span data-ttu-id="751d3-152">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="751d3-152">Click Add.</span></span>
    * <span data-ttu-id="751d3-153">Tilfangaflokkurinn skilgreinir svæði, framleiðslueiningu og samhengi vöruhúss fyrir rekstrartilföngum.</span><span class="sxs-lookup"><span data-stu-id="751d3-153">The resource group defines the site, production unit, and warehouse context for operations resources.</span></span> <span data-ttu-id="751d3-154">Aðeins er hægt að raða rekstrartilföng þegar þeim er úthlutað á tilfangaflokk , og aðeins á svæði þar sem tilfangaflokkurinn er staðsettur.</span><span class="sxs-lookup"><span data-stu-id="751d3-154">The operations resource can only be scheduled when assigned to a resource group, and only on the site where the resource group is located.</span></span>  
3. <span data-ttu-id="751d3-155">Í reitinn tilfangaflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="751d3-155">In the Resource group field, enter or select a value.</span></span>
4. <span data-ttu-id="751d3-156">Sláðu inn eða veldu gildi Innsláttur reitnum Staðsetning inntaks.</span><span class="sxs-lookup"><span data-stu-id="751d3-156">In the Input location field, enter or select a value.</span></span>
    * <span data-ttu-id="751d3-157">Tilgreina staðsetningu vöruhúss þar sem rekstrartilföng er að nota efni.</span><span class="sxs-lookup"><span data-stu-id="751d3-157">Specify the warehouse location from where the operations resource is consuming materials.</span></span>  

