---
title: Vinna með leið fyrir framleiðslulíkan
description: Keyra þetta ferli krefst að afbrigðalíkan afurðar sé til staðar.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCRouteOperationDetails, WrkCtrCapabilityLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 45c6b1e6e75645bb17ce4defa0bca0e6d2131b6e
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921266"
---
# <a name="maintain-route-for-a-product-model"></a><span data-ttu-id="48443-103">Vinna með leið fyrir framleiðslulíkan</span><span class="sxs-lookup"><span data-stu-id="48443-103">Maintain route for a product model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="48443-104">Keyra þetta ferli krefst að afbrigðalíkan afurðar sé til staðar.</span><span class="sxs-lookup"><span data-stu-id="48443-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="48443-105">Þetta ferli notar hágæða hátalara líkanið USMF sýnigögn fyrirtæki til að fara í gegnum ferlið.</span><span class="sxs-lookup"><span data-stu-id="48443-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>

## <a name="add-a-route-operation"></a><span data-ttu-id="48443-106">Bæta við leiðaraðgerð</span><span class="sxs-lookup"><span data-stu-id="48443-106">Add a route operation</span></span>

1. <span data-ttu-id="48443-107">Farið í **Afurðarupplýsingastjórnun \> Afurðir \> Afbrigðalíkön afurða**.</span><span class="sxs-lookup"><span data-stu-id="48443-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="48443-108">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="48443-108">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="48443-109">Veljið lok hágæða hátalara líkan fyrir þetta æfingu.</span><span class="sxs-lookup"><span data-stu-id="48443-109">Select the High end speaker model for this exercise.</span></span>  
1. <span data-ttu-id="48443-110">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="48443-110">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="48443-111">Útvíkka hlutann **Leiðaraðgerð**.</span><span class="sxs-lookup"><span data-stu-id="48443-111">Expand the **Route operations** section.</span></span>
1. <span data-ttu-id="48443-112">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="48443-112">Select **Add**.</span></span>
1. <span data-ttu-id="48443-113">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="48443-113">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="48443-114">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="48443-114">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="48443-115">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="48443-115">Select **Save**.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="48443-116">Færa inn upplýsingar leiðaraðgerðar.</span><span class="sxs-lookup"><span data-stu-id="48443-116">Enter route operation details</span></span>

1. <span data-ttu-id="48443-117">Veljið **Upplýsingar um leiðaraðgerð**.</span><span class="sxs-lookup"><span data-stu-id="48443-117">Select **Route operation details**.</span></span>
1. <span data-ttu-id="48443-118">Færa inn eða veljið gildi í svæðinu **Aðgerð**.</span><span class="sxs-lookup"><span data-stu-id="48443-118">In the **Operation** field, enter or select a value.</span></span>
1. <span data-ttu-id="48443-119">Í **Aðg.nr**</span><span class="sxs-lookup"><span data-stu-id="48443-119">In the **Oper. No.**</span></span> <span data-ttu-id="48443-120">færðu inn númer</span><span class="sxs-lookup"><span data-stu-id="48443-120">field, enter a number.</span></span>
    * <span data-ttu-id="48443-121">Aðgerðarnúmer ákvarða the leiðarruna.</span><span class="sxs-lookup"><span data-stu-id="48443-121">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="48443-122">Hver eiginleiki á leiðaaðgerð hægt að sækja fast gildi eða varpað á eigind.</span><span class="sxs-lookup"><span data-stu-id="48443-122">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="48443-123">Vörpun eigind leiðir til þess að gildi er stillt sem hluti af skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="48443-123">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
1. <span data-ttu-id="48443-124">Í reitinn **Leiðaflokkur** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="48443-124">In the **Route group** field, enter or select a value.</span></span>
    * <span data-ttu-id="48443-125">Leiðarflokkur ákvarðar nauðsynlegar hegðun fyrir kostnaðarútreikning, notkun og uppsetningu.</span><span class="sxs-lookup"><span data-stu-id="48443-125">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
1. <span data-ttu-id="48443-126">Veljið flipann **Uppsetning**.</span><span class="sxs-lookup"><span data-stu-id="48443-126">Select the **Setup** tab.</span></span>
1. <span data-ttu-id="48443-127">Veljið flipann **Tímar**.</span><span class="sxs-lookup"><span data-stu-id="48443-127">Select the **Times** tab.</span></span>
1. <span data-ttu-id="48443-128">Færið inn númer í reitinn **Vinnslumagn**.</span><span class="sxs-lookup"><span data-stu-id="48443-128">In the **Process qty.** field, enter a number.</span></span>
    * <span data-ttu-id="48443-129">Ákvarðað hversu verður að vinna við einni aðgerð.</span><span class="sxs-lookup"><span data-stu-id="48443-129">Determine how many will be processed during one operation.</span></span>  
1. <span data-ttu-id="48443-130">Í reitinn **Klukkutímar/tími** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="48443-130">In the **Hours/time** field, enter a number.</span></span>
    * <span data-ttu-id="48443-131">Færið inn tímahlutfall.</span><span class="sxs-lookup"><span data-stu-id="48443-131">Enter the time ratio.</span></span>  
1. <span data-ttu-id="48443-132">Veljið gátreitinn **Stilla**.</span><span class="sxs-lookup"><span data-stu-id="48443-132">Select the **Set** check box.</span></span>
1. <span data-ttu-id="48443-133">Í reitinn **Keyrslutími** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="48443-133">In the **Run time** field, enter a number.</span></span>
    * <span data-ttu-id="48443-134">Ákvarða vinnslutíma fyrir það magn sem búið er að tilgreina.</span><span class="sxs-lookup"><span data-stu-id="48443-134">Determine the processing time for the quantity that you have specified.</span></span>  
1. <span data-ttu-id="48443-135">Veldu flipann **Tilfangaþarfir**.</span><span class="sxs-lookup"><span data-stu-id="48443-135">Select the **Resource requirements** tab.</span></span>
1. <span data-ttu-id="48443-136">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="48443-136">Select **Add**.</span></span>
1. <span data-ttu-id="48443-137">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="48443-137">In the list, mark the selected row.</span></span>
1. <span data-ttu-id="48443-138">Veljið valkost í svæðinu **Gerð kröfu**.</span><span class="sxs-lookup"><span data-stu-id="48443-138">In the **Requirement type** field, select an option.</span></span>
    * <span data-ttu-id="48443-139">Ákveða hvort eigi að tilgreina ákveðna tilföng eða getu sem búa verður yfir.</span><span class="sxs-lookup"><span data-stu-id="48443-139">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
1. <span data-ttu-id="48443-140">Sláið inn eða veljið gildi í reitnum **Krafa**.</span><span class="sxs-lookup"><span data-stu-id="48443-140">In the **Requirement** field, enter or select a value.</span></span>
1. <span data-ttu-id="48443-141">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="48443-141">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]