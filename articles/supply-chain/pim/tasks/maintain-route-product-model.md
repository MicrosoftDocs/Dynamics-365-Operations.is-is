---
title: Vinna með leið fyrir framleiðslulíkan
description: Keyra þetta ferli krefst að afbrigðalíkan afurðar sé til staðar.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 24419cb9bad4b4344fe23789750387de6cca3796
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203521"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="65315-103">Vinna með leið fyrir framleiðslulíkan</span><span class="sxs-lookup"><span data-stu-id="65315-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="65315-104">Keyra þetta ferli krefst að afbrigðalíkan afurðar sé til staðar.</span><span class="sxs-lookup"><span data-stu-id="65315-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="65315-105">Þetta ferli notar hágæða hátalara líkanið USMF sýnigögn fyrirtæki til að fara í gegnum ferlið.</span><span class="sxs-lookup"><span data-stu-id="65315-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="65315-106">Bæta við leiðaraðgerð</span><span class="sxs-lookup"><span data-stu-id="65315-106">Add a route operation</span></span>
1. <span data-ttu-id="65315-107">Smellið á Skilgreining afurðarafbrigðislíkans</span><span class="sxs-lookup"><span data-stu-id="65315-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="65315-108">Smella á Afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="65315-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="65315-109">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="65315-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="65315-110">Veljið lok hágæða hátalara líkan fyrir þetta æfingu.</span><span class="sxs-lookup"><span data-stu-id="65315-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="65315-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="65315-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="65315-112">Útvíkka hlutann leiðaraðgerð.</span><span class="sxs-lookup"><span data-stu-id="65315-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="65315-113">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="65315-113">Click Add.</span></span>
7. <span data-ttu-id="65315-114">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="65315-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="65315-115">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="65315-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="65315-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="65315-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="65315-117">Færa inn upplýsingar leiðaraðgerðar.</span><span class="sxs-lookup"><span data-stu-id="65315-117">Enter route operation details</span></span>
1. <span data-ttu-id="65315-118">Smellt er á leiðaraðgerð.</span><span class="sxs-lookup"><span data-stu-id="65315-118">Click Route operation details.</span></span>
2. <span data-ttu-id="65315-119">Færa inn eða veljið gildi í svæðinu aðgerð.</span><span class="sxs-lookup"><span data-stu-id="65315-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="65315-120">Í Aðg.</span><span class="sxs-lookup"><span data-stu-id="65315-120">In the Oper.</span></span> <span data-ttu-id="65315-121">Nei.</span><span class="sxs-lookup"><span data-stu-id="65315-121">No.</span></span> <span data-ttu-id="65315-122">færðu inn númer</span><span class="sxs-lookup"><span data-stu-id="65315-122">field, enter a number.</span></span>
    * <span data-ttu-id="65315-123">Aðgerðarnúmer ákvarða the leiðarruna.</span><span class="sxs-lookup"><span data-stu-id="65315-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="65315-124">Hver eiginleiki á leiðaaðgerð hægt að sækja fast gildi eða varpað á eigind.</span><span class="sxs-lookup"><span data-stu-id="65315-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="65315-125">Vörpun eigind leiðir til þess að gildi er stillt sem hluti af skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="65315-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="65315-126">Í reitinn leiðaflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="65315-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="65315-127">Leiðarflokkur ákvarðar nauðsynlegar hegðun fyrir kostnaðarútreikning, notkun og uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="65315-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="65315-128">Smellið á flipann „Setja upp“.</span><span class="sxs-lookup"><span data-stu-id="65315-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="65315-129">Smellt er á tímaflipann.</span><span class="sxs-lookup"><span data-stu-id="65315-129">Click the Times tab.</span></span>
7. <span data-ttu-id="65315-130">Í svæðinu framleiðslumagn færðu inn númer</span><span class="sxs-lookup"><span data-stu-id="65315-130">In the Process qty. field, enter a number.</span></span>
    * <span data-ttu-id="65315-131">Ákvarðað hversu verður að vinna við einni aðgerð.</span><span class="sxs-lookup"><span data-stu-id="65315-131">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="65315-132">Í reitinn klukkutímar/tími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="65315-132">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="65315-133">Færið inn tímahlutfall.</span><span class="sxs-lookup"><span data-stu-id="65315-133">Enter the time ratio.</span></span>  
9. <span data-ttu-id="65315-134">Veljið gátreitinn stilla.</span><span class="sxs-lookup"><span data-stu-id="65315-134">Select the Set check box.</span></span>
10. <span data-ttu-id="65315-135">Í reitinn keyrslutími skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="65315-135">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="65315-136">Ákvarða vinnslutíma fyrir það magn sem búið er að tilgreina.</span><span class="sxs-lookup"><span data-stu-id="65315-136">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="65315-137">Smellið á flipann tilfangaþörf.</span><span class="sxs-lookup"><span data-stu-id="65315-137">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="65315-138">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="65315-138">Click Add.</span></span>
13. <span data-ttu-id="65315-139">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="65315-139">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="65315-140">Veljið valkost í svæðinu gerð krafna.</span><span class="sxs-lookup"><span data-stu-id="65315-140">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="65315-141">Ákveða hvort eigi að tilgreina ákveðna tilföng eða getu sem búa verður yfir.</span><span class="sxs-lookup"><span data-stu-id="65315-141">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="65315-142">Sláið inn eða veldu gildi í reitnum kröfur.</span><span class="sxs-lookup"><span data-stu-id="65315-142">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="65315-143">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="65315-143">Click OK.</span></span>

