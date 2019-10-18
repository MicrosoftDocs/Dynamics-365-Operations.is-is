---
title: Stuðulafskrift
description: Þessi grein veitir yfirlit yfir stuðulsafskriftaraðferð.
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
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5c36441e926cd5a82c802a350adf6b2ed6d6387
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178266"
---
# <a name="factor-depreciation"></a><span data-ttu-id="80dfb-103">Stuðulafskrift</span><span class="sxs-lookup"><span data-stu-id="80dfb-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80dfb-104">Þessi grein veitir yfirlit yfir stuðulsafskriftaraðferð.</span><span class="sxs-lookup"><span data-stu-id="80dfb-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="80dfb-105">Stuðlar eru prósenturnar sem eru notaðar til að afskrifa eignir.</span><span class="sxs-lookup"><span data-stu-id="80dfb-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="80dfb-106">Þegar afskriftaregla fyrir eignir hefur verið sett upp og velur **þáttur** í **aðferð** svæðinu í síðunni **afskriftarregla** er hægt að setja upp stighækkandi, stiglækkandi eða línulega afskrift:</span><span class="sxs-lookup"><span data-stu-id="80dfb-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="80dfb-107">Í stighækkandi afskrift hækkar afskriftarupphæðin með hverju afskriftartímabili.</span><span class="sxs-lookup"><span data-stu-id="80dfb-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="80dfb-108">Í stiglækkandi afskrift lækkar afskriftarupphæðin á tímabili með tímanum.</span><span class="sxs-lookup"><span data-stu-id="80dfb-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="80dfb-109">Í línuleg afskrift eru afskriftirnar eins á hverju tímabili.</span><span class="sxs-lookup"><span data-stu-id="80dfb-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="80dfb-110">Reglurnar og dæmin að sem fylgja gefa til kynna hvernig hægt er að setja upp stuðla fyrir hverja gerð afskriftar.</span><span class="sxs-lookup"><span data-stu-id="80dfb-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="80dfb-111">Þegar þú velur **stuðull** í **aðferð** svæði, eru **stuðull** svæði og **Tímabil** svæði birt.</span><span class="sxs-lookup"><span data-stu-id="80dfb-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="80dfb-112">Stighækkandi afskriftir</span><span class="sxs-lookup"><span data-stu-id="80dfb-112">Progressive depreciation</span></span>
<span data-ttu-id="80dfb-113">Gildið í reitnum **stuðull** er hærri en **50**.</span><span class="sxs-lookup"><span data-stu-id="80dfb-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="80dfb-114">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80dfb-114">Example</span></span>

<span data-ttu-id="80dfb-115">Kaupverð er 100.000, stuðull er 70, líftími er 10 ár, og afskrift hefst á 1. janúar.</span><span class="sxs-lookup"><span data-stu-id="80dfb-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="80dfb-116">Afskriftarupphæð og upphæð bókaðs nettóvirði eru sýnd aðeins fyrir fyrstu sex ári líftímans.</span><span class="sxs-lookup"><span data-stu-id="80dfb-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="80dfb-117">Ár</span><span class="sxs-lookup"><span data-stu-id="80dfb-117">Year</span></span> | <span data-ttu-id="80dfb-118">Tímabil</span><span class="sxs-lookup"><span data-stu-id="80dfb-118">Period</span></span>      | <span data-ttu-id="80dfb-119">Afskriftarupphæð</span><span class="sxs-lookup"><span data-stu-id="80dfb-119">Depreciation amount</span></span> | <span data-ttu-id="80dfb-120">Upphæð bókaðs nettóvirðis</span><span class="sxs-lookup"><span data-stu-id="80dfb-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="80dfb-121">1</span><span class="sxs-lookup"><span data-stu-id="80dfb-121">1</span></span>    | <span data-ttu-id="80dfb-122">31. desember</span><span class="sxs-lookup"><span data-stu-id="80dfb-122">December 31</span></span> | <span data-ttu-id="80dfb-123">307,69</span><span class="sxs-lookup"><span data-stu-id="80dfb-123">307.69</span></span>              | <span data-ttu-id="80dfb-124">99.692,31</span><span class="sxs-lookup"><span data-stu-id="80dfb-124">99,692.31</span></span>             |
| <span data-ttu-id="80dfb-125">2</span><span class="sxs-lookup"><span data-stu-id="80dfb-125">2</span></span>    | <span data-ttu-id="80dfb-126">31. desember</span><span class="sxs-lookup"><span data-stu-id="80dfb-126">December 31</span></span> | <span data-ttu-id="80dfb-127">1.447,21</span><span class="sxs-lookup"><span data-stu-id="80dfb-127">1,447.21</span></span>            | <span data-ttu-id="80dfb-128">98.245,10</span><span class="sxs-lookup"><span data-stu-id="80dfb-128">98,245.10</span></span>             |
| <span data-ttu-id="80dfb-129">3</span><span class="sxs-lookup"><span data-stu-id="80dfb-129">3</span></span>    | <span data-ttu-id="80dfb-130">31. desember</span><span class="sxs-lookup"><span data-stu-id="80dfb-130">December 31</span></span> | <span data-ttu-id="80dfb-131">3.104,50</span><span class="sxs-lookup"><span data-stu-id="80dfb-131">3,104.50</span></span>            | <span data-ttu-id="80dfb-132">95.140,60</span><span class="sxs-lookup"><span data-stu-id="80dfb-132">95,140.60</span></span>             |
| <span data-ttu-id="80dfb-133">4</span><span class="sxs-lookup"><span data-stu-id="80dfb-133">4</span></span>    | <span data-ttu-id="80dfb-134">31. desember</span><span class="sxs-lookup"><span data-stu-id="80dfb-134">December 31</span></span> | <span data-ttu-id="80dfb-135">5.150,21</span><span class="sxs-lookup"><span data-stu-id="80dfb-135">5,150.21</span></span>            | <span data-ttu-id="80dfb-136">89.990,39</span><span class="sxs-lookup"><span data-stu-id="80dfb-136">89,990.39</span></span>             |
| <span data-ttu-id="80dfb-137">5</span><span class="sxs-lookup"><span data-stu-id="80dfb-137">5</span></span>    | <span data-ttu-id="80dfb-138">31. desember</span><span class="sxs-lookup"><span data-stu-id="80dfb-138">December 31</span></span> | <span data-ttu-id="80dfb-139">7.522,95</span><span class="sxs-lookup"><span data-stu-id="80dfb-139">7,522.95</span></span>            | <span data-ttu-id="80dfb-140">82.467,44</span><span class="sxs-lookup"><span data-stu-id="80dfb-140">82,467.44</span></span>             |
| <span data-ttu-id="80dfb-141">6</span><span class="sxs-lookup"><span data-stu-id="80dfb-141">6</span></span>    | <span data-ttu-id="80dfb-142">31. desember</span><span class="sxs-lookup"><span data-stu-id="80dfb-142">December 31</span></span> | <span data-ttu-id="80dfb-143">10.184,06</span><span class="sxs-lookup"><span data-stu-id="80dfb-143">10,184.06</span></span>           | <span data-ttu-id="80dfb-144">72.283,38</span><span class="sxs-lookup"><span data-stu-id="80dfb-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="80dfb-145">Stiglækkandi afskriftir</span><span class="sxs-lookup"><span data-stu-id="80dfb-145">Digressive depreciation</span></span>
<span data-ttu-id="80dfb-146">Gildið í reitnum **stuðull** er lægri en **50**.</span><span class="sxs-lookup"><span data-stu-id="80dfb-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="80dfb-147">Dæmi</span><span class="sxs-lookup"><span data-stu-id="80dfb-147">Example</span></span>

<span data-ttu-id="80dfb-148">Kaupverð er 100.000, stuðull er 20, líftími er 10 ár, og afskrift hefst á 1. janúar.</span><span class="sxs-lookup"><span data-stu-id="80dfb-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="80dfb-149">Afskriftarupphæð og upphæð bókaðs nettóvirði eru sýnd aðeins fyrir fyrstu sex ári líftímans.</span><span class="sxs-lookup"><span data-stu-id="80dfb-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="80dfb-150">Ár</span><span class="sxs-lookup"><span data-stu-id="80dfb-150">Year</span></span> | <span data-ttu-id="80dfb-151">Tímabil</span><span class="sxs-lookup"><span data-stu-id="80dfb-151">Period</span></span>      | <span data-ttu-id="80dfb-152">Afskriftarupphæð</span><span class="sxs-lookup"><span data-stu-id="80dfb-152">Depreciation amount</span></span> | <span data-ttu-id="80dfb-153">Upphæð bókaðs nettóvirðis</span><span class="sxs-lookup"><span data-stu-id="80dfb-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="80dfb-154">1</span><span class="sxs-lookup"><span data-stu-id="80dfb-154">1</span></span>    | <span data-ttu-id="80dfb-155">31. desember</span><span class="sxs-lookup"><span data-stu-id="80dfb-155">December 31</span></span> | <span data-ttu-id="80dfb-156">56.080,43</span><span class="sxs-lookup"><span data-stu-id="80dfb-156">56,080.43</span></span>           | <span data-ttu-id="80dfb-157">43.919,57</span><span class="sxs-lookup"><span data-stu-id="80dfb-157">43,919.57</span></span>             |
| <span data-ttu-id="80dfb-158">2</span><span class="sxs-lookup"><span data-stu-id="80dfb-158">2</span></span>    | <span data-ttu-id="80dfb-159">31. desember</span><span class="sxs-lookup"><span data-stu-id="80dfb-159">December 31</span></span> | <span data-ttu-id="80dfb-160">10.665,70</span><span class="sxs-lookup"><span data-stu-id="80dfb-160">10,665.70</span></span>           | <span data-ttu-id="80dfb-161">33.253,87</span><span class="sxs-lookup"><span data-stu-id="80dfb-161">33,253.87</span></span>             |
| <span data-ttu-id="80dfb-162">3</span><span class="sxs-lookup"><span data-stu-id="80dfb-162">3</span></span>    | <span data-ttu-id="80dfb-163">31. desember</span><span class="sxs-lookup"><span data-stu-id="80dfb-163">December 31</span></span> | <span data-ttu-id="80dfb-164">7.156,22</span><span class="sxs-lookup"><span data-stu-id="80dfb-164">7,156.22</span></span>            | <span data-ttu-id="80dfb-165">26,097.65</span><span class="sxs-lookup"><span data-stu-id="80dfb-165">26,097.65</span></span>             |
| <span data-ttu-id="80dfb-166">4</span><span class="sxs-lookup"><span data-stu-id="80dfb-166">4</span></span>    | <span data-ttu-id="80dfb-167">31. desember</span><span class="sxs-lookup"><span data-stu-id="80dfb-167">December 31</span></span> | <span data-ttu-id="80dfb-168">5.538,06</span><span class="sxs-lookup"><span data-stu-id="80dfb-168">5,538.06</span></span>            | <span data-ttu-id="80dfb-169">20.559,59</span><span class="sxs-lookup"><span data-stu-id="80dfb-169">20,559.59</span></span>             |
| <span data-ttu-id="80dfb-170">5</span><span class="sxs-lookup"><span data-stu-id="80dfb-170">5</span></span>    | <span data-ttu-id="80dfb-171">31. desember</span><span class="sxs-lookup"><span data-stu-id="80dfb-171">December 31</span></span> | <span data-ttu-id="80dfb-172">4.579,89</span><span class="sxs-lookup"><span data-stu-id="80dfb-172">4,579.89</span></span>            | <span data-ttu-id="80dfb-173">15.979,70</span><span class="sxs-lookup"><span data-stu-id="80dfb-173">15,979.70</span></span>             |
| <span data-ttu-id="80dfb-174">6</span><span class="sxs-lookup"><span data-stu-id="80dfb-174">6</span></span>    | <span data-ttu-id="80dfb-175">31. desember</span><span class="sxs-lookup"><span data-stu-id="80dfb-175">December 31</span></span> | <span data-ttu-id="80dfb-176">3.937,36</span><span class="sxs-lookup"><span data-stu-id="80dfb-176">3,937.36</span></span>            | <span data-ttu-id="80dfb-177">12.042,34</span><span class="sxs-lookup"><span data-stu-id="80dfb-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="80dfb-178">Línuleg afskrift</span><span class="sxs-lookup"><span data-stu-id="80dfb-178">Straight line depreciation</span></span>
<span data-ttu-id="80dfb-179">Gildið í reitnum **stuðull** er jafn **50**.</span><span class="sxs-lookup"><span data-stu-id="80dfb-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="80dfb-180">Í þessu tilfelli eru afskriftirnar þær sömu á hverju tímabili og þú ættir að hugsa um áhrif þeirra gilda sem voru tilgreind í öðrum reitum, eins og lýst er í [línulegur líftími afskriftar](straight-line-service-life-depreciation.md)</span><span class="sxs-lookup"><span data-stu-id="80dfb-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>



