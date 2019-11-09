---
title: Áhrif afskrifta með bakfærslum
description: Þessi grein fjallar hugsanlega afleiðingar af því að bakfæra eignafærslu.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 2961
ms.assetid: 63a3ac92-c321-4379-a86a-b1b14915f340
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd4c4a9e7e89b34b1311b38310877b45e4d95b22
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187361"
---
# <a name="depreciation-effects-with-reversals"></a><span data-ttu-id="d2d95-103">Áhrif afskrifta með bakfærslum</span><span class="sxs-lookup"><span data-stu-id="d2d95-103">Depreciation effects with reversals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2d95-104">Þessi grein fjallar hugsanlega afleiðingar af því að bakfæra eignafærslu.</span><span class="sxs-lookup"><span data-stu-id="d2d95-104">This article discusses potential implications of reversing a fixed asset transaction.</span></span> 

<span data-ttu-id="d2d95-105">Hægt er að bakfæra eignafærslur og færslur sem tengjast eign.</span><span class="sxs-lookup"><span data-stu-id="d2d95-105">You can reverse fixed asset transactions, and the transactions that are associated with a fixed asset.</span></span> <span data-ttu-id="d2d95-106">Einnig er hægt að afturkalla bakfærða færslu.</span><span class="sxs-lookup"><span data-stu-id="d2d95-106">You can also revoke a reversed transaction.</span></span> 

<span data-ttu-id="d2d95-107">Hægt er að bakfæra eða afturkalla færslu sem var ekki nýjasta færslan bókuð í bókina fyrir eignina.</span><span class="sxs-lookup"><span data-stu-id="d2d95-107">You can reverse or revoke a transaction that was not the most recent transaction posted to the book for the asset.</span></span> <span data-ttu-id="d2d95-108">Fyrst að athuga hvort einhverjar afskriftafærslur voru bókaðar eftir færsluna sem á að bakfæra.</span><span class="sxs-lookup"><span data-stu-id="d2d95-108">You should first determine whether any depreciation transactions were posted after the transaction that you are reversing.</span></span> <span data-ttu-id="d2d95-109">Þetta er vegna þess að afskriftir eru ekki endurreiknaðar þegar færsla er bakfærð.</span><span class="sxs-lookup"><span data-stu-id="d2d95-109">This is because depreciation is not recalculated when you reverse a transaction.</span></span> <span data-ttu-id="d2d95-110">Þess vegna verða afskriftir oft ýktar eða verða of litlar eftir bakfærsluna eins og sýnt er í dæmunum.</span><span class="sxs-lookup"><span data-stu-id="d2d95-110">Therefore, depreciation often is overstated or understated after the reversal, as shown in the examples.</span></span> 

<span data-ttu-id="d2d95-111">Svo að tryggja megi að afskriftir séu réttar þegar færsla er bakfærð skal ekki halda áfram með bakfærsluna ef boð berast í ferlinu sem segja að afskriftir verði ekki endurreiknaðar.</span><span class="sxs-lookup"><span data-stu-id="d2d95-111">To make sure that depreciation is correct when you reverse a transaction, do not continue with the reversal if you receive a message that states that depreciation will not be recalculated.</span></span> <span data-ttu-id="d2d95-112">Í staðinn skal fyrst bakfæra afskriftarfærsluna sem var bókuð eftir færsluna sem reynt var að bakfæra og halda svo áfram með bakfærsluna.</span><span class="sxs-lookup"><span data-stu-id="d2d95-112">Instead, first reverse the depreciation transaction that was posted after the transaction you tried to reverse, and then continue with the reversal.</span></span> <span data-ttu-id="d2d95-113">Þú verður ekki varaður við afskriftarútreikningum, og hægt er að halda áfram að bakfæra.</span><span class="sxs-lookup"><span data-stu-id="d2d95-113">You will not be warned about depreciation recalculations, and you can continue with the reversal.</span></span> 

<span data-ttu-id="d2d95-114">Eftirfarandi dæmi sýna útreikninga sem eru gerðir ef valið er að halda áfram eftir viðvörunarboðin í stað þess að bakfæra fyrst afskriftarfærslurnar.</span><span class="sxs-lookup"><span data-stu-id="d2d95-114">The following examples show the calculations that occur if you continue beyond the message without first reversing the depreciation transactions.</span></span>

## <a name="example-1-depreciation-is-overstated"></a><span data-ttu-id="d2d95-115">Dæmi 1: Afskriftir eru ýktar</span><span class="sxs-lookup"><span data-stu-id="d2d95-115">Example 1: Depreciation is overstated</span></span>
<span data-ttu-id="d2d95-116">Eign er sett upp með 5 ára líftíma og línuleg afskrift (60 afskriftartímabil).</span><span class="sxs-lookup"><span data-stu-id="d2d95-116">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="d2d95-117">Í þessu dæmi eru afskriftir ýktar.</span><span class="sxs-lookup"><span data-stu-id="d2d95-117">In this example, depreciation is overstated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="d2d95-118">Færslusaga eignar</span><span class="sxs-lookup"><span data-stu-id="d2d95-118">Asset transaction history</span></span>

| <span data-ttu-id="d2d95-119">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="d2d95-119">Date</span></span>       | <span data-ttu-id="d2d95-120">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="d2d95-120">Transaction type</span></span>                                                          | <span data-ttu-id="d2d95-121">Upphæð</span><span class="sxs-lookup"><span data-stu-id="d2d95-121">Amount</span></span>                                    |
|------------|---------------------------------------------------------------------------|-------------------------------------------|
| <span data-ttu-id="d2d95-122">1. janúar</span><span class="sxs-lookup"><span data-stu-id="d2d95-122">January 1</span></span>  | <span data-ttu-id="d2d95-123">Kaup</span><span class="sxs-lookup"><span data-stu-id="d2d95-123">Acquisition</span></span>                                                               | <span data-ttu-id="d2d95-124">59.000,00</span><span class="sxs-lookup"><span data-stu-id="d2d95-124">59,000.00</span></span>                                 |
| <span data-ttu-id="d2d95-125">1. janúar</span><span class="sxs-lookup"><span data-stu-id="d2d95-125">January 1</span></span>  | <span data-ttu-id="d2d95-126">Leiðrétting kaupa</span><span class="sxs-lookup"><span data-stu-id="d2d95-126">Acquisition adjustment</span></span>                                                    | <span data-ttu-id="d2d95-127">1.000,00</span><span class="sxs-lookup"><span data-stu-id="d2d95-127">1,000.00</span></span>                                  |
| <span data-ttu-id="d2d95-128">31. janúar</span><span class="sxs-lookup"><span data-stu-id="d2d95-128">January 31</span></span> | <span data-ttu-id="d2d95-129">Afskrift (stofnuð með því að nota tillögu fyrir eitt afskriftartímabil)</span><span class="sxs-lookup"><span data-stu-id="d2d95-129">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="d2d95-130">1,000.00Útreikningur: bókað virði (59.000 + 1.000) / Fjöldi afskriftartímabila sem er eftir (60)</span><span class="sxs-lookup"><span data-stu-id="d2d95-130">1,000.00Calculation: Book value (59,000 + 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="d2d95-131">Bakfærsluaðgerð</span><span class="sxs-lookup"><span data-stu-id="d2d95-131">Reversal action</span></span>

| <span data-ttu-id="d2d95-132">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="d2d95-132">Date</span></span>      | <span data-ttu-id="d2d95-133">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="d2d95-133">Transaction type</span></span>                | <span data-ttu-id="d2d95-134">Upphæð</span><span class="sxs-lookup"><span data-stu-id="d2d95-134">Amount</span></span>    |
|-----------|---------------------------------|-----------|
| <span data-ttu-id="d2d95-135">1. janúar</span><span class="sxs-lookup"><span data-stu-id="d2d95-135">January 1</span></span> | <span data-ttu-id="d2d95-136">Bakfærsla leiðréttingar á eign</span><span class="sxs-lookup"><span data-stu-id="d2d95-136">Acquisition adjustment reversal</span></span> | <span data-ttu-id="d2d95-137">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="d2d95-137">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="d2d95-138">Áhrif afskriftar</span><span class="sxs-lookup"><span data-stu-id="d2d95-138">Depreciation effect</span></span>

| <span data-ttu-id="d2d95-139">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="d2d95-139">Date</span></span>        | <span data-ttu-id="d2d95-140">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="d2d95-140">Transaction type</span></span>        | <span data-ttu-id="d2d95-141">Upphæð</span><span class="sxs-lookup"><span data-stu-id="d2d95-141">Amount</span></span>                                                                                |
|-------------|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d95-142">28. febrúar</span><span class="sxs-lookup"><span data-stu-id="d2d95-142">February 28</span></span> | <span data-ttu-id="d2d95-143">Afskrift (tillaga)</span><span class="sxs-lookup"><span data-stu-id="d2d95-143">Depreciation (proposal)</span></span> | <span data-ttu-id="d2d95-144">983.05Útreikningur: bókað virði (59.000 - 1.000 afskrift) / Fjöldi afskriftartímabila sem er eftir (59)</span><span class="sxs-lookup"><span data-stu-id="d2d95-144">983.05Calculation: Book value (59,000 - 1,000 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="d2d95-145">Afskrift er ýkt um 16,95 (1000 - 983,.05).</span><span class="sxs-lookup"><span data-stu-id="d2d95-145">Depreciation is overstated by 16.95 (1,000 - 983.05).</span></span>

## <a name="example-2-depreciation-is-understated"></a><span data-ttu-id="d2d95-146">Dæmi 2: Afskrift verður of lítil</span><span class="sxs-lookup"><span data-stu-id="d2d95-146">Example 2: Depreciation is understated</span></span>
<span data-ttu-id="d2d95-147">Eign er sett upp með 5 ára líftíma og línuleg afskrift (60 afskriftartímabil).</span><span class="sxs-lookup"><span data-stu-id="d2d95-147">An asset is set up with a 5-year useful life and straight line depreciation (60 depreciation periods).</span></span> <span data-ttu-id="d2d95-148">Í þessu dæmi eru afskriftir of litlar.</span><span class="sxs-lookup"><span data-stu-id="d2d95-148">In this example, depreciation is understated.</span></span>
#### <a name="asset-transaction-history"></a><span data-ttu-id="d2d95-149">Færslusaga eigna</span><span class="sxs-lookup"><span data-stu-id="d2d95-149">Asset transaction history</span></span>

| <span data-ttu-id="d2d95-150">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="d2d95-150">Date</span></span>       | <span data-ttu-id="d2d95-151">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="d2d95-151">Transaction type</span></span>                                                          | <span data-ttu-id="d2d95-152">Upphæð</span><span class="sxs-lookup"><span data-stu-id="d2d95-152">Amount</span></span>                                      |
|------------|---------------------------------------------------------------------------|---------------------------------------------|
| <span data-ttu-id="d2d95-153">1. janúar</span><span class="sxs-lookup"><span data-stu-id="d2d95-153">January 1</span></span>  | <span data-ttu-id="d2d95-154">Kaup</span><span class="sxs-lookup"><span data-stu-id="d2d95-154">Acquisition</span></span>                                                               | <span data-ttu-id="d2d95-155">59.000,00</span><span class="sxs-lookup"><span data-stu-id="d2d95-155">59,000.00</span></span>                                   |
| <span data-ttu-id="d2d95-156">1. janúar</span><span class="sxs-lookup"><span data-stu-id="d2d95-156">January 1</span></span>  | <span data-ttu-id="d2d95-157">Leiðrétting niðurfærslu</span><span class="sxs-lookup"><span data-stu-id="d2d95-157">Write-down adjustment</span></span>                                                     | <span data-ttu-id="d2d95-158">1.000,00</span><span class="sxs-lookup"><span data-stu-id="d2d95-158">1,000.00</span></span>                                    |
| <span data-ttu-id="d2d95-159">31. janúar</span><span class="sxs-lookup"><span data-stu-id="d2d95-159">January 31</span></span> | <span data-ttu-id="d2d95-160">Afskrift (stofnuð með því að nota tillögu fyrir eitt afskriftartímabil)</span><span class="sxs-lookup"><span data-stu-id="d2d95-160">Depreciation (created by using a proposal for one period of depreciation)</span></span> | <span data-ttu-id="d2d95-161">966.67Útreikningur: bókað virði (59.000 + 1.000) / Fjöldi afskriftartímabila sem er eftir (60)</span><span class="sxs-lookup"><span data-stu-id="d2d95-161">966.67Calculation: Book value (59,000 - 1,000) / Number of depreciation periods remaining (60)</span></span> |

#### <a name="reversal-action"></a><span data-ttu-id="d2d95-162">Bakfærsluaðgerð</span><span class="sxs-lookup"><span data-stu-id="d2d95-162">Reversal action</span></span>

| <span data-ttu-id="d2d95-163">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="d2d95-163">Date</span></span>      | <span data-ttu-id="d2d95-164">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="d2d95-164">Transaction type</span></span>               | <span data-ttu-id="d2d95-165">Upphæð</span><span class="sxs-lookup"><span data-stu-id="d2d95-165">Amount</span></span>    |
|-----------|--------------------------------|-----------|
| <span data-ttu-id="d2d95-166">1. janúar</span><span class="sxs-lookup"><span data-stu-id="d2d95-166">January 1</span></span> | <span data-ttu-id="d2d95-167">Leiðrétting Niðurfærslu bakfærð</span><span class="sxs-lookup"><span data-stu-id="d2d95-167">Write-down adjustment reversal</span></span> | <span data-ttu-id="d2d95-168">-1.000,00</span><span class="sxs-lookup"><span data-stu-id="d2d95-168">–1,000.00</span></span> |

#### <a name="depreciation-effect"></a><span data-ttu-id="d2d95-169">Áhrif afskriftar</span><span class="sxs-lookup"><span data-stu-id="d2d95-169">Depreciation effect</span></span>

| <span data-ttu-id="d2d95-170">Dagsetning</span><span class="sxs-lookup"><span data-stu-id="d2d95-170">Date</span></span>        | <span data-ttu-id="d2d95-171">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="d2d95-171">Transaction type</span></span>        | <span data-ttu-id="d2d95-172">Upphæð</span><span class="sxs-lookup"><span data-stu-id="d2d95-172">Amount</span></span>                                                                                       |
|-------------|-------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d95-173">28. febrúar</span><span class="sxs-lookup"><span data-stu-id="d2d95-173">February 28</span></span> | <span data-ttu-id="d2d95-174">Afskrift (tillaga)</span><span class="sxs-lookup"><span data-stu-id="d2d95-174">Depreciation (proposal)</span></span> | <span data-ttu-id="d2d95-175">983.62Útreikningur: bókað virði (59.000 + 966,67 afskrift) / Fjöldi afskriftartímabila sem er eftir (59)</span><span class="sxs-lookup"><span data-stu-id="d2d95-175">983.62Calculation: Book value (59,000 - 966.67 depreciation) / Number of depreciation periods remaining (59)</span></span> |

<span data-ttu-id="d2d95-176">Afskrift er er höfð of lítil sem nemur 16,95 (983,62 - 966,67).</span><span class="sxs-lookup"><span data-stu-id="d2d95-176">Depreciation is understated by 16.95 (983.62 - 966.67).</span></span>



<a name="additional-resources"></a><span data-ttu-id="d2d95-177">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="d2d95-177">Additional resources</span></span>
--------

[<span data-ttu-id="d2d95-178">Afskriftir eigna</span><span class="sxs-lookup"><span data-stu-id="d2d95-178">Fixed asset depreciation</span></span>](fixed-asset-depreciation.md)


