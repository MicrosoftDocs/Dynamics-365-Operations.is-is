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
ms.custom: 13831
ms.assetid: 2b6c4fe4-02ff-4191-bcad-32f1f34c15f2
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87cca8b3472f572cd1c4ba3d894269f7ba0f248a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241075"
---
# <a name="factor-depreciation"></a><span data-ttu-id="c5b8d-103">Stuðulafskrift</span><span class="sxs-lookup"><span data-stu-id="c5b8d-103">Factor depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5b8d-104">Þessi grein veitir yfirlit yfir stuðulsafskriftaraðferð.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-104">This article gives an overview of the factor depreciation method.</span></span>

<span data-ttu-id="c5b8d-105">Stuðlar eru prósenturnar sem eru notaðar til að afskrifa eignir.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-105">Factors are the percentages that are used to depreciate assets.</span></span> <span data-ttu-id="c5b8d-106">Þegar afskriftaregla fyrir eignir hefur verið sett upp og velur **þáttur** í **aðferð** svæðinu í síðunni **afskriftarregla** er hægt að setja upp stighækkandi, stiglækkandi eða línulega afskrift:</span><span class="sxs-lookup"><span data-stu-id="c5b8d-106">When you set up a fixed asset depreciation profile and select **Factor** in the **Method** field on the **Depreciation profiles** page, you can set up progressive, digressive, or straight line depreciation:</span></span>

-   <span data-ttu-id="c5b8d-107">Í stighækkandi afskrift hækkar afskriftarupphæðin með hverju afskriftartímabili.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-107">In progressive depreciation, the amount of depreciation increases each depreciation period.</span></span>
-   <span data-ttu-id="c5b8d-108">Í stiglækkandi afskrift lækkar afskriftarupphæðin á tímabili með tímanum.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-108">In digressive depreciation, the amount of depreciation per period decreases over time.</span></span>
-   <span data-ttu-id="c5b8d-109">Í línuleg afskrift eru afskriftirnar eins á hverju tímabili.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-109">In straight line depreciation, the depreciation is the same in each period.</span></span>

<span data-ttu-id="c5b8d-110">Reglurnar og dæmin að sem fylgja gefa til kynna hvernig hægt er að setja upp stuðla fyrir hverja gerð afskriftar.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-110">The rules and examples that follow indicate how you can set up factors for each type of depreciation.</span></span> 

> [!NOTE] 
> <span data-ttu-id="c5b8d-111">Þegar þú velur **stuðull** í **aðferð** svæði, eru **stuðull** svæði og **Tímabil** svæði birt.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-111">When you select **Factor** in the **Method** field, the **Factor** field and the **Interval** field are displayed.</span></span>

## <a name="progressive-depreciation"></a><span data-ttu-id="c5b8d-112">Stighækkandi afskriftir</span><span class="sxs-lookup"><span data-stu-id="c5b8d-112">Progressive depreciation</span></span>
<span data-ttu-id="c5b8d-113">Gildið í reitnum **stuðull** er hærri en **50**.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-113">The value in the **Factor** field is more than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="c5b8d-114">Dæmi</span><span class="sxs-lookup"><span data-stu-id="c5b8d-114">Example</span></span>

<span data-ttu-id="c5b8d-115">Kaupverð er 100.000, stuðull er 70, líftími er 10 ár, og afskrift hefst á 1. janúar.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-115">The acquisition price is 100,000, the factor is 70, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="c5b8d-116">Afskriftarupphæð og upphæð bókaðs nettóvirði eru sýnd aðeins fyrir fyrstu sex ári líftímans.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-116">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="c5b8d-117">Ár</span><span class="sxs-lookup"><span data-stu-id="c5b8d-117">Year</span></span> | <span data-ttu-id="c5b8d-118">Tímabil</span><span class="sxs-lookup"><span data-stu-id="c5b8d-118">Period</span></span>      | <span data-ttu-id="c5b8d-119">Afskriftarupphæð</span><span class="sxs-lookup"><span data-stu-id="c5b8d-119">Depreciation amount</span></span> | <span data-ttu-id="c5b8d-120">Upphæð bókaðs nettóvirðis</span><span class="sxs-lookup"><span data-stu-id="c5b8d-120">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="c5b8d-121">1</span><span class="sxs-lookup"><span data-stu-id="c5b8d-121">1</span></span>    | <span data-ttu-id="c5b8d-122">31. desember</span><span class="sxs-lookup"><span data-stu-id="c5b8d-122">December 31</span></span> | <span data-ttu-id="c5b8d-123">307,69</span><span class="sxs-lookup"><span data-stu-id="c5b8d-123">307.69</span></span>              | <span data-ttu-id="c5b8d-124">99.692,31</span><span class="sxs-lookup"><span data-stu-id="c5b8d-124">99,692.31</span></span>             |
| <span data-ttu-id="c5b8d-125">2</span><span class="sxs-lookup"><span data-stu-id="c5b8d-125">2</span></span>    | <span data-ttu-id="c5b8d-126">31. desember</span><span class="sxs-lookup"><span data-stu-id="c5b8d-126">December 31</span></span> | <span data-ttu-id="c5b8d-127">1.447,21</span><span class="sxs-lookup"><span data-stu-id="c5b8d-127">1,447.21</span></span>            | <span data-ttu-id="c5b8d-128">98.245,10</span><span class="sxs-lookup"><span data-stu-id="c5b8d-128">98,245.10</span></span>             |
| <span data-ttu-id="c5b8d-129">3</span><span class="sxs-lookup"><span data-stu-id="c5b8d-129">3</span></span>    | <span data-ttu-id="c5b8d-130">31. desember</span><span class="sxs-lookup"><span data-stu-id="c5b8d-130">December 31</span></span> | <span data-ttu-id="c5b8d-131">3.104,50</span><span class="sxs-lookup"><span data-stu-id="c5b8d-131">3,104.50</span></span>            | <span data-ttu-id="c5b8d-132">95.140,60</span><span class="sxs-lookup"><span data-stu-id="c5b8d-132">95,140.60</span></span>             |
| <span data-ttu-id="c5b8d-133">4</span><span class="sxs-lookup"><span data-stu-id="c5b8d-133">4</span></span>    | <span data-ttu-id="c5b8d-134">31. desember</span><span class="sxs-lookup"><span data-stu-id="c5b8d-134">December 31</span></span> | <span data-ttu-id="c5b8d-135">5.150,21</span><span class="sxs-lookup"><span data-stu-id="c5b8d-135">5,150.21</span></span>            | <span data-ttu-id="c5b8d-136">89.990,39</span><span class="sxs-lookup"><span data-stu-id="c5b8d-136">89,990.39</span></span>             |
| <span data-ttu-id="c5b8d-137">5</span><span class="sxs-lookup"><span data-stu-id="c5b8d-137">5</span></span>    | <span data-ttu-id="c5b8d-138">31. desember</span><span class="sxs-lookup"><span data-stu-id="c5b8d-138">December 31</span></span> | <span data-ttu-id="c5b8d-139">7.522,95</span><span class="sxs-lookup"><span data-stu-id="c5b8d-139">7,522.95</span></span>            | <span data-ttu-id="c5b8d-140">82.467,44</span><span class="sxs-lookup"><span data-stu-id="c5b8d-140">82,467.44</span></span>             |
| <span data-ttu-id="c5b8d-141">6</span><span class="sxs-lookup"><span data-stu-id="c5b8d-141">6</span></span>    | <span data-ttu-id="c5b8d-142">31. desember</span><span class="sxs-lookup"><span data-stu-id="c5b8d-142">December 31</span></span> | <span data-ttu-id="c5b8d-143">10.184,06</span><span class="sxs-lookup"><span data-stu-id="c5b8d-143">10,184.06</span></span>           | <span data-ttu-id="c5b8d-144">72.283,38</span><span class="sxs-lookup"><span data-stu-id="c5b8d-144">72,283.38</span></span>             |

## <a name="digressive-depreciation"></a><span data-ttu-id="c5b8d-145">Stiglækkandi afskriftir</span><span class="sxs-lookup"><span data-stu-id="c5b8d-145">Digressive depreciation</span></span>
<span data-ttu-id="c5b8d-146">Gildið í reitnum **stuðull** er lægri en **50**.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-146">The value in the **Factor** field is less than **50**.</span></span>

### <a name="example"></a><span data-ttu-id="c5b8d-147">Dæmi</span><span class="sxs-lookup"><span data-stu-id="c5b8d-147">Example</span></span>

<span data-ttu-id="c5b8d-148">Kaupverð er 100.000, stuðull er 20, líftími er 10 ár, og afskrift hefst á 1. janúar.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-148">The acquisition price is 100,000, the factor is 20, the service life is 10 years, and depreciation starts on January 1.</span></span> <span data-ttu-id="c5b8d-149">Afskriftarupphæð og upphæð bókaðs nettóvirði eru sýnd aðeins fyrir fyrstu sex ári líftímans.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-149">The depreciation amounts and net book value amounts are shown only for the first six years of service life.</span></span>

| <span data-ttu-id="c5b8d-150">Ár</span><span class="sxs-lookup"><span data-stu-id="c5b8d-150">Year</span></span> | <span data-ttu-id="c5b8d-151">Tímabil</span><span class="sxs-lookup"><span data-stu-id="c5b8d-151">Period</span></span>      | <span data-ttu-id="c5b8d-152">Afskriftarupphæð</span><span class="sxs-lookup"><span data-stu-id="c5b8d-152">Depreciation amount</span></span> | <span data-ttu-id="c5b8d-153">Upphæð bókaðs nettóvirðis</span><span class="sxs-lookup"><span data-stu-id="c5b8d-153">Net book value amount</span></span> |
|------|-------------|---------------------|-----------------------|
| <span data-ttu-id="c5b8d-154">1</span><span class="sxs-lookup"><span data-stu-id="c5b8d-154">1</span></span>    | <span data-ttu-id="c5b8d-155">31. desember</span><span class="sxs-lookup"><span data-stu-id="c5b8d-155">December 31</span></span> | <span data-ttu-id="c5b8d-156">56.080,43</span><span class="sxs-lookup"><span data-stu-id="c5b8d-156">56,080.43</span></span>           | <span data-ttu-id="c5b8d-157">43.919,57</span><span class="sxs-lookup"><span data-stu-id="c5b8d-157">43,919.57</span></span>             |
| <span data-ttu-id="c5b8d-158">2</span><span class="sxs-lookup"><span data-stu-id="c5b8d-158">2</span></span>    | <span data-ttu-id="c5b8d-159">31. desember</span><span class="sxs-lookup"><span data-stu-id="c5b8d-159">December 31</span></span> | <span data-ttu-id="c5b8d-160">10.665,70</span><span class="sxs-lookup"><span data-stu-id="c5b8d-160">10,665.70</span></span>           | <span data-ttu-id="c5b8d-161">33.253,87</span><span class="sxs-lookup"><span data-stu-id="c5b8d-161">33,253.87</span></span>             |
| <span data-ttu-id="c5b8d-162">3</span><span class="sxs-lookup"><span data-stu-id="c5b8d-162">3</span></span>    | <span data-ttu-id="c5b8d-163">31. desember</span><span class="sxs-lookup"><span data-stu-id="c5b8d-163">December 31</span></span> | <span data-ttu-id="c5b8d-164">7.156,22</span><span class="sxs-lookup"><span data-stu-id="c5b8d-164">7,156.22</span></span>            | <span data-ttu-id="c5b8d-165">26,097.65</span><span class="sxs-lookup"><span data-stu-id="c5b8d-165">26,097.65</span></span>             |
| <span data-ttu-id="c5b8d-166">4</span><span class="sxs-lookup"><span data-stu-id="c5b8d-166">4</span></span>    | <span data-ttu-id="c5b8d-167">31. desember</span><span class="sxs-lookup"><span data-stu-id="c5b8d-167">December 31</span></span> | <span data-ttu-id="c5b8d-168">5.538,06</span><span class="sxs-lookup"><span data-stu-id="c5b8d-168">5,538.06</span></span>            | <span data-ttu-id="c5b8d-169">20.559,59</span><span class="sxs-lookup"><span data-stu-id="c5b8d-169">20,559.59</span></span>             |
| <span data-ttu-id="c5b8d-170">5</span><span class="sxs-lookup"><span data-stu-id="c5b8d-170">5</span></span>    | <span data-ttu-id="c5b8d-171">31. desember</span><span class="sxs-lookup"><span data-stu-id="c5b8d-171">December 31</span></span> | <span data-ttu-id="c5b8d-172">4.579,89</span><span class="sxs-lookup"><span data-stu-id="c5b8d-172">4,579.89</span></span>            | <span data-ttu-id="c5b8d-173">15.979,70</span><span class="sxs-lookup"><span data-stu-id="c5b8d-173">15,979.70</span></span>             |
| <span data-ttu-id="c5b8d-174">6</span><span class="sxs-lookup"><span data-stu-id="c5b8d-174">6</span></span>    | <span data-ttu-id="c5b8d-175">31. desember</span><span class="sxs-lookup"><span data-stu-id="c5b8d-175">December 31</span></span> | <span data-ttu-id="c5b8d-176">3.937,36</span><span class="sxs-lookup"><span data-stu-id="c5b8d-176">3,937.36</span></span>            | <span data-ttu-id="c5b8d-177">12.042,34</span><span class="sxs-lookup"><span data-stu-id="c5b8d-177">12,042.34</span></span>             |

## <a name="straight-line-depreciation"></a><span data-ttu-id="c5b8d-178">Línuleg afskrift</span><span class="sxs-lookup"><span data-stu-id="c5b8d-178">Straight line depreciation</span></span>
<span data-ttu-id="c5b8d-179">Gildið í reitnum **stuðull** er jafn **50**.</span><span class="sxs-lookup"><span data-stu-id="c5b8d-179">The value in the **Factor** field is equal to **50**.</span></span> <span data-ttu-id="c5b8d-180">Í þessu tilfelli eru afskriftirnar þær sömu á hverju tímabili og þú ættir að hugsa um áhrif þeirra gilda sem voru tilgreind í öðrum reitum, eins og lýst er í [línulegur líftími afskriftar](straight-line-service-life-depreciation.md)</span><span class="sxs-lookup"><span data-stu-id="c5b8d-180">In this case, the depreciation is the same in each period, and you should consider the implications of the values that you have specified in other fields, as described in [Straight line service life depreciation](straight-line-service-life-depreciation.md).</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]