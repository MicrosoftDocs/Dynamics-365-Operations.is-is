---
title: Notkunarafskriftir
description: "Þessi grein gefur yfirlit yfir notkunaraðferð afskriftar."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13751
ms.assetid: d25a681f-49a5-4bfc-aa76-1c6373e35dd8
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 653c7de18d8227d639d0138201a9ec395b484d2f
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="consumption-depreciation"></a><span data-ttu-id="f51d1-103">Notkunarafskriftir</span><span class="sxs-lookup"><span data-stu-id="f51d1-103">Consumption depreciation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="f51d1-104">Þessi grein gefur yfirlit yfir notkunaraðferð afskriftar.</span><span class="sxs-lookup"><span data-stu-id="f51d1-104">This article gives an overview of the Consumption method of depreciation.</span></span>

<span data-ttu-id="f51d1-105">Ef afskriftaregla fyrir eignir er sett upp og valið er **notkun** í svæðinu**aðferð** á skjámyndinni**afskriftaaðferðir** eru eignir, tengdar þessari afskriftareglu sem eru byggðar á notkun þeirra.</span><span class="sxs-lookup"><span data-stu-id="f51d1-105">If you set up a depreciation profile for fixed assets and select **Consumption** in the **Method** field on the **Depreciation profiles** page, fixed assets are assigned to the depreciation profile based on their usage.</span></span> <span data-ttu-id="f51d1-106">Ekki þarf að setja upp prósentur og tímabil í á **afskriftareglur** síðu.</span><span class="sxs-lookup"><span data-stu-id="f51d1-106">You don't have to set up percentages and intervals on the **Depreciation profiles** page.</span></span> <span data-ttu-id="f51d1-107">Eftir að þú stofnar afskriftarregla sem notar notkunaraðferð, er hægt að setja aðferðina upp á nokkra vegu.</span><span class="sxs-lookup"><span data-stu-id="f51d1-107">After you create a depreciation profile that uses the Consumption method, you can set up the method in various ways.</span></span>

## <a name="set-up-and-use-consumption-depreciation"></a><span data-ttu-id="f51d1-108">Setja upp og nota notkunarafskrift.</span><span class="sxs-lookup"><span data-stu-id="f51d1-108">Set up and use consumption depreciation</span></span>
1.  <span data-ttu-id="f51d1-109">Á síðunni **afskriftarregla** skal stofna afskriftarreglu.</span><span class="sxs-lookup"><span data-stu-id="f51d1-109">On the **Depreciation profiles** page, create the depreciation profile.</span></span> <span data-ttu-id="f51d1-110">Fyrir notkunarútreikninga verður afskriftareglan að innihalda kenni, heiti og **notkun** verður að vera valin í reitnum **aðferð**.</span><span class="sxs-lookup"><span data-stu-id="f51d1-110">For consumption calculations, the depreciation profile must have an ID and a name, and **Consumption** must be selected in the **Method** field.</span></span>
2.  <span data-ttu-id="f51d1-111">Á **Notkunarstuðull** síða, setja upp notkunarstuðull.</span><span class="sxs-lookup"><span data-stu-id="f51d1-111">On the **Consumption factors** page, set up consumption factors.</span></span> <span data-ttu-id="f51d1-112">Hvern notkunarstuðul verður að hafa Kenni og heiti, og notkunarstuðul sem er tilgreindur sem magn eða prósenta.</span><span class="sxs-lookup"><span data-stu-id="f51d1-112">Each consumption factor must have an ID and a name, and a consumption factor that is specified as either a quantity or a percentage.</span></span>
3.  <span data-ttu-id="f51d1-113">Á **notkunareining** síðuna setja upp notkunareiningar.</span><span class="sxs-lookup"><span data-stu-id="f51d1-113">On the **Consumption units** page, set up consumption units.</span></span> <span data-ttu-id="f51d1-114">Hver notkunareining verður að hafa Kenni og heiti</span><span class="sxs-lookup"><span data-stu-id="f51d1-114">Each consumption unit must have an ID and a name.</span></span> <span data-ttu-id="f51d1-115">Afskriftareiningar eru notaðar til að reikna notkunarafskrift á **notkunarafskrift** síðu.</span><span class="sxs-lookup"><span data-stu-id="f51d1-115">Depreciation units are used to calculate consumption depreciation on the **Consumption depreciation** page.</span></span> <span data-ttu-id="f51d1-116">Dæmi um einingar eru kílómetrar (km), kílógrömm (kg) og klukkustund.</span><span class="sxs-lookup"><span data-stu-id="f51d1-116">Examples of units are kilometer (km), kilogram (kg), and hour.</span></span>
4.  <span data-ttu-id="f51d1-117">Á **Eignir** síðu setja upp einstaka eignir.</span><span class="sxs-lookup"><span data-stu-id="f51d1-117">On the **Fixed assets** page, set up individual fixed assets.</span></span> <span data-ttu-id="f51d1-118">Fyrir hverja eign, veldu Virðislíkön og afskriftarbækur sem eru með afskriftarreglur.</span><span class="sxs-lookup"><span data-stu-id="f51d1-118">For each fixed asset, select value models and depreciation books that have depreciation profiles.</span></span> <span data-ttu-id="f51d1-119">Setja verður upp virðislíkan eða afskriftarbók fyrir notkunarafskrift ef einhver af eignum þínum notar afskriftarregla sem byggist á notkunaraðferðinni.</span><span class="sxs-lookup"><span data-stu-id="f51d1-119">You must set up value models or depreciation books for consumption depreciation if any of your fixed assets use depreciation profiles that are based on the Consumption method.</span></span> <span data-ttu-id="f51d1-120">Þessari uppsetningu er að gera annaðhvort á í **Afskriftir** flipanum á **Virðislíkön** síðu eða á í **Almennt** flýtiflipi af **afskriftareglu** síðu.</span><span class="sxs-lookup"><span data-stu-id="f51d1-120">This setup is done either on the **Depreciation** tab of the **Value models** page or on the **General** FastTab of the **Depreciation profile** page.</span></span> <span data-ttu-id="f51d1-121">Hægt er að nota sama virðislíkan fyrir margar eignir.</span><span class="sxs-lookup"><span data-stu-id="f51d1-121">You can use the same value model for multiple fixed assets.</span></span> <span data-ttu-id="f51d1-122">Afskriftareglur eru hluti af virðislíkani eða afskriftarbók sem valin er fyrir hverja eign.</span><span class="sxs-lookup"><span data-stu-id="f51d1-122">Depreciation profiles are part of the value model or depreciation book that you select for each fixed asset.</span></span> <span data-ttu-id="f51d1-123">Ekki er hægt að bæta við eða breyta afskriftareglur beint á í **Eignir** síðu.</span><span class="sxs-lookup"><span data-stu-id="f51d1-123">You can't add or modify depreciation profiles directly on the **Fixed assets** page.</span></span> <span data-ttu-id="f51d1-124">Hægt er að breyta afskriftarreglum aðeins á **afskriftabækur** síðu.</span><span class="sxs-lookup"><span data-stu-id="f51d1-124">You can modify depreciation profiles only on the **Depreciation books** page.</span></span>
5.  <span data-ttu-id="f51d1-125">Í **virðislíkani** síðu eða **afskriftarbók**síðu, í **notkunarafskrift** reitahópur, skal færa upplýsingar í eftirtalin svæði :</span><span class="sxs-lookup"><span data-stu-id="f51d1-125">On the **Value models** page or the **Depreciation books** page, in the **Consumption depreciation** field group, enter information in the following fields:</span></span>
    -   <span data-ttu-id="f51d1-126">Notkunarstuðull</span><span class="sxs-lookup"><span data-stu-id="f51d1-126">Consumption factor</span></span>
    -   <span data-ttu-id="f51d1-127">Eining</span><span class="sxs-lookup"><span data-stu-id="f51d1-127">Unit</span></span>
    -   <span data-ttu-id="f51d1-128">Einingaafskriftir</span><span class="sxs-lookup"><span data-stu-id="f51d1-128">Unit depreciation</span></span>
    -   <span data-ttu-id="f51d1-129">Metin notkun</span><span class="sxs-lookup"><span data-stu-id="f51d1-129">Estimated consumption</span></span>

    <span data-ttu-id="f51d1-130">Svæðið **bókun notkun** sýnir notkunarafskriftareiningar, sem hafa þegar verið bókaðar annað hvort blöndu af eign og virðislíkan, eða fyrir afskriftarbók</span><span class="sxs-lookup"><span data-stu-id="f51d1-130">The **Posted consumption** field shows the consumption depreciation, in units, that has already been posted either for the combination of the fixed asset and value model, or for the depreciation book.</span></span> <span data-ttu-id="f51d1-131">Handvirkt er ekki hægt að uppfæra gildið í þessu svæði.</span><span class="sxs-lookup"><span data-stu-id="f51d1-131">You can't manually update the value in this field.</span></span>

## <a name="examples"></a><span data-ttu-id="f51d1-132">Dæmi</span><span class="sxs-lookup"><span data-stu-id="f51d1-132">Examples</span></span>
### <a name="example-1"></a><span data-ttu-id="f51d1-133">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="f51d1-133">Example 1</span></span>

<span data-ttu-id="f51d1-134">Eftirfarandi notkunarstuðull er settur upp fyrir 31. janúar:</span><span class="sxs-lookup"><span data-stu-id="f51d1-134">The following consumption factor is set up for January 31:</span></span>

-   <span data-ttu-id="f51d1-135">Magnið 1,000.</span><span class="sxs-lookup"><span data-stu-id="f51d1-135">The quantity is 1,000.</span></span>
-   <span data-ttu-id="f51d1-136">Afskriftarverð einingar sem er tilgreint fyrir eignarinnar er 1,5.</span><span class="sxs-lookup"><span data-stu-id="f51d1-136">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>

<span data-ttu-id="f51d1-137">Afskriftatillagan þann 31. Janúar er á eftirfarandi: Magn × einingarafskrift 1.000 × 1,5 = 1,500 Ef stuðullinn sem er tilgreint fyrir eignina er prósentustuðull er magnið sem metið er í **Metin notkun** reit fyrir virðislíkan eignarinnar er margfaldað með prósentunni sem sett er upp fyrir valda lokadagsetningu.</span><span class="sxs-lookup"><span data-stu-id="f51d1-137">The depreciation proposal on January 31 is as follows: Quantity × Unit depreciation 1,000 × 1.5 = 1,500 If the factor that is specified for the fixed asset is a percentage factor, the quantity that is estimated in the **Estimated consumption** field for the value model of the fixed asset is multiplied by the percentage that is set up for the selected end date.</span></span> <span data-ttu-id="f51d1-138">Meðfylgjandi magnið er svo lagt til sem afskriftarmagn fyrir tímabilið.</span><span class="sxs-lookup"><span data-stu-id="f51d1-138">The resulting quantity is then suggested as the depreciation quantity for the period.</span></span>

### <a name="example-2"></a><span data-ttu-id="f51d1-139">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="f51d1-139">Example 2</span></span>

<span data-ttu-id="f51d1-140">Eftirfarandi stuðull fyrir notkunarafskrift er setja upp fyrir janúar 31:</span><span class="sxs-lookup"><span data-stu-id="f51d1-140">The following factor for consumption depreciation is set up for January 31:</span></span>

-   <span data-ttu-id="f51d1-141">Prósenta er 10 prósent.</span><span class="sxs-lookup"><span data-stu-id="f51d1-141">The percentage is 10 percent.</span></span>
-   <span data-ttu-id="f51d1-142">Afskriftarverð einingar sem er tilgreint fyrir eignarinnar er 1,5.</span><span class="sxs-lookup"><span data-stu-id="f51d1-142">The unit depreciation price that is specified for the fixed asset is 1.5.</span></span>
-   <span data-ttu-id="f51d1-143">Metið magn eignarinnar er 2.000.</span><span class="sxs-lookup"><span data-stu-id="f51d1-143">The estimated quantity of the fixed asset is 2,000.</span></span>

<span data-ttu-id="f51d1-144">Afskriftatillagan þann 31. Janúar er á eftirfarandi hátt: áætlað magn × Prósentu × einingarafskrift 2.000 ×.10 × 1,5 = 300</span><span class="sxs-lookup"><span data-stu-id="f51d1-144">The depreciation proposal on January 31 is as follows: Estimated quantity × Percentage × Unit depreciation 2,000 × .10 × 1.5 = 300</span></span>




