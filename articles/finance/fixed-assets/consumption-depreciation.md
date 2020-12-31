---
title: Notkunarafskriftir
description: Þessi grein gefur yfirlit yfir notkunaraðferð afskriftar.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2c9d95a7a45ed99c63516749285126c786685c87
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444259"
---
# <a name="consumption-depreciation"></a><span data-ttu-id="bdf7b-103">Notkunarafskriftir</span><span class="sxs-lookup"><span data-stu-id="bdf7b-103">Consumption depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bdf7b-104">Þessi grein gefur yfirlit yfir notkunaraðferð afskriftar.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-104">This article gives an overview of the Consumption method of depreciation.</span></span>

<span data-ttu-id="bdf7b-105">Ef afskriftaregla fyrir eignir er sett upp og valið er **notkun** í reitnum **Aðferð** á skjámyndinni **Afskriftaaðferðir** eru eignir tengdar þessari afskriftareglu og samkvæmt notkun þeirra.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-105">If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage.</span></span> <span data-ttu-id="bdf7b-106">Ekki þarf að setja upp prósentur og tímabil í á **afskriftareglur** síðu.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-106">You don't have to set up percentages and intervals on the **Depreciation profiles** page.</span></span> <span data-ttu-id="bdf7b-107">Eftir að þú stofnar afskriftarregla sem notar notkunaraðferð, er hægt að setja aðferðina upp á nokkra vegu.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-107">After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.</span></span>

## <a name="set-up-and-use-consumption-depreciation"></a><span data-ttu-id="bdf7b-108">Setja upp og nota notkunarafskrift.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-108">Set up and use consumption depreciation</span></span>
1.  <span data-ttu-id="bdf7b-109">Á síðunni **afskriftarregla** skal stofna afskriftarreglu.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-109">On the **Depreciation profiles** page, create the depreciation profile.</span></span> <span data-ttu-id="bdf7b-110">Fyrir notkunarútreikninga verður afskriftareglan að innihalda kenni, heiti og **notkun** verður að vera valin í reitnum **aðferð**.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-110">For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.</span></span>
2.  <span data-ttu-id="bdf7b-111">Á **Notkunarstuðull** síða, setja upp notkunarstuðull.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-111">On the **Consumption factors** page, set up consumption factors.</span></span> <span data-ttu-id="bdf7b-112">Hvern notkunarstuðul verður að hafa Kenni og heiti, og notkunarstuðul sem er tilgreindur sem magn eða prósenta.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-112">Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.</span></span>
3.  <span data-ttu-id="bdf7b-113">Á **notkunareining** síðuna setja upp notkunareiningar.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-113">On the **Consumption units** page, set up consumption units.</span></span> <span data-ttu-id="bdf7b-114">Hver notkunareining verður að hafa Kenni og heiti</span><span class="sxs-lookup"><span data-stu-id="bdf7b-114">Each consumption unit must have an ID and a name.</span></span> <span data-ttu-id="bdf7b-115">Afskriftareiningar eru notaðar til að reikna notkunarafskrift á **notkunarafskrift** síðu.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-115">Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page.</span></span> <span data-ttu-id="bdf7b-116">Dæmi um einingar eru kílómetrar (km), kílógrömm (kg) og klukkustund.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-116">Examples of units are kilometer (km), kilogram (kg), and hour.</span></span>
4.  <span data-ttu-id="bdf7b-117">Á **Eignir** síðu setja upp einstaka eignir.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-117">On the **Fixed assets** page, set up individual fixed assets.</span></span> <span data-ttu-id="bdf7b-118">Fyrir hverja eign, veldu Virðislíkön og afskriftarbækur sem eru með afskriftarreglur.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-118">For each fixed asset, select value models and depreciation books that have depreciation profiles.</span></span> <span data-ttu-id="bdf7b-119">Setja verður upp virðislíkan eða afskriftarbók fyrir notkunarafskrift ef einhver af eignum þínum notar afskriftarregla sem byggist á notkunaraðferðinni.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-119">You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method.</span></span> <span data-ttu-id="bdf7b-120">Þessari uppsetningu er að gera annaðhvort á í **Afskriftir** flipanum á **Virðislíkön** síðu eða á í **Almennt** flýtiflipi af **afskriftareglu** síðu.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-120">This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page.</span></span> <span data-ttu-id="bdf7b-121">Hægt er að nota sama virðislíkan fyrir margar eignir.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-121">You can use the same value model for multiple fixed assets.</span></span> <span data-ttu-id="bdf7b-122">Afskriftareglur eru hluti af virðislíkani eða afskriftarbók sem valin er fyrir hverja eign.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-122">Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset.</span></span> <span data-ttu-id="bdf7b-123">Ekki er hægt að bæta við eða breyta afskriftareglur beint á í **Eignir** síðu.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-123">You can't add or modify depreciation profiles directly on the **Fixed assets** page.</span></span> <span data-ttu-id="bdf7b-124">Hægt er að breyta afskriftarreglum aðeins á **afskriftabækur** síðu.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-124">You can modify depreciation profiles only on the **Depreciation books** page.</span></span>
5.  <span data-ttu-id="bdf7b-125">Á síðunni **Virðislíkan** eða síðunni **Afskriftarbók** í reitahópnum **Notkunarafskrift** skal færa upplýsingar í eftirtalin svæði:</span><span class="sxs-lookup"><span data-stu-id="bdf7b-125">On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:</span></span>
    -   <span data-ttu-id="bdf7b-126">Notkunarstuðull</span><span class="sxs-lookup"><span data-stu-id="bdf7b-126">Consumption factor</span></span>
    -   <span data-ttu-id="bdf7b-127">Eining</span><span class="sxs-lookup"><span data-stu-id="bdf7b-127">Unit</span></span>
    -   <span data-ttu-id="bdf7b-128">Einingaafskriftir</span><span class="sxs-lookup"><span data-stu-id="bdf7b-128">Unit depreciation</span></span>
    -   <span data-ttu-id="bdf7b-129">Metin notkun</span><span class="sxs-lookup"><span data-stu-id="bdf7b-129">Estimated consumption</span></span>

    <span data-ttu-id="bdf7b-130">Svæðið **bókun notkun** sýnir notkunarafskriftareiningar, sem hafa þegar verið bókaðar annað hvort blöndu af eign og virðislíkan, eða fyrir afskriftarbók</span><span class="sxs-lookup"><span data-stu-id="bdf7b-130">The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book.</span></span> <span data-ttu-id="bdf7b-131">Handvirkt er ekki hægt að uppfæra gildið í þessu svæði.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-131">You can't manually update the value in this field.</span></span>

## <a name="examples"></a><span data-ttu-id="bdf7b-132">Dæmi</span><span class="sxs-lookup"><span data-stu-id="bdf7b-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="bdf7b-133">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="bdf7b-133">Example 1</span></span>

<span data-ttu-id="bdf7b-134">Eftirfarandi notkunarstuðull er settur upp fyrir 31. janúar:</span><span class="sxs-lookup"><span data-stu-id="bdf7b-134">The following consumption factor is set up for January 31:</span></span>

-   <span data-ttu-id="bdf7b-135">Magnið 1,000.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-135">The quantity is 1,000.</span></span>
-   <span data-ttu-id="bdf7b-136">Afskriftarverð einingar sem er tilgreint fyrir eignarinnar er 1,5.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-136">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>

<span data-ttu-id="bdf7b-137">Afskriftatillagan þann 31. Janúar er á eftirfarandi: Magn × einingarafskrift 1.000 × 1,5 = 1,500 Ef stuðullinn sem er tilgreint fyrir eignina er prósentustuðull er magnið sem metið er í **Metin notkun** reit fyrir virðislíkan eignarinnar er margfaldað með prósentunni sem sett er upp fyrir valda lokadagsetningu.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-137">The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date.</span></span> <span data-ttu-id="bdf7b-138">Meðfylgjandi magnið er svo lagt til sem afskriftarmagn fyrir tímabilið.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-138">The resulting quantity is then suggested as the depreciation quantity for the period.</span></span>

### <a name="example-2"></a><span data-ttu-id="bdf7b-139">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="bdf7b-139">Example 2</span></span>

<span data-ttu-id="bdf7b-140">Eftirfarandi stuðull fyrir notkunarafskrift er setja upp fyrir janúar 31:</span><span class="sxs-lookup"><span data-stu-id="bdf7b-140">The following factor for consumption depreciation is set up for January 31:</span></span>

-   <span data-ttu-id="bdf7b-141">Prósenta er 10 prósent.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-141">The percentage is 10 percent.</span></span>
-   <span data-ttu-id="bdf7b-142">Afskriftarverð einingar sem er tilgreint fyrir eignarinnar er 1,5.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-142">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>
-   <span data-ttu-id="bdf7b-143">Metið magn eignarinnar er 2.000.</span><span class="sxs-lookup"><span data-stu-id="bdf7b-143">The estimated quantity of the fixed asset is 2,000.</span></span>

<span data-ttu-id="bdf7b-144">Afskriftatillagan þann 31. Janúar er á eftirfarandi hátt: áætlað magn × Prósentu × einingarafskrift 2.000 ×.10 × 1,5 = 300</span><span class="sxs-lookup"><span data-stu-id="bdf7b-144">The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300</span></span>



