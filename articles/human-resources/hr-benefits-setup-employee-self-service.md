---
title: Grunnstilla sjálfsafgreiðslu starfsmanns
description: Í Microsoft Dynamics 365 Human Resources, þú getur stillt flísar fyrir toppstig siglingar í sjálfsafgreiðslu starfsmanna.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 17918fc7b894929c92c54b59b7440ab8aef980bd
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092661"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="d43e7-103">Grunnstilla sjálfsafgreiðslu starfsmanns</span><span class="sxs-lookup"><span data-stu-id="d43e7-103">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="d43e7-104">Í Microsoft Dynamics 365 Human Resources, þú getur stillt flísar fyrir toppstig siglingar í sjálfsafgreiðslu starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="d43e7-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="d43e7-105">Ávinningur áætlunarflísar beinir notendum að hagnaði áætlunum sem þeir eru gjaldgengir í.</span><span class="sxs-lookup"><span data-stu-id="d43e7-105">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="d43e7-106">Uppsetning á reit hlutverkamiðstöðvar</span><span class="sxs-lookup"><span data-stu-id="d43e7-106">Set up a role center tile</span></span>

1. <span data-ttu-id="d43e7-107">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **sjálfsafgreiðslufæribreytur starfsmanns**.</span><span class="sxs-lookup"><span data-stu-id="d43e7-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="d43e7-108">Veldu **Skipulag hlutverks miðflísar** flipanum og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d43e7-108">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="d43e7-109">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="d43e7-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="d43e7-110">Svæði</span><span class="sxs-lookup"><span data-stu-id="d43e7-110">Field</span></span> | <span data-ttu-id="d43e7-111">Lýsing</span><span class="sxs-lookup"><span data-stu-id="d43e7-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d43e7-112">Auðkenni reits</span><span class="sxs-lookup"><span data-stu-id="d43e7-112">Tile ID</span></span> | <span data-ttu-id="d43e7-113">Einkvæmt auðkenni fyrir reitinn.</span><span class="sxs-lookup"><span data-stu-id="d43e7-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="d43e7-114">Texti merkis reits</span><span class="sxs-lookup"><span data-stu-id="d43e7-114">Tile label text</span></span> | <span data-ttu-id="d43e7-115">Textinn sem birtist fyrir reitinn í sjálfsafgreiðslunni.</span><span class="sxs-lookup"><span data-stu-id="d43e7-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="d43e7-116">Lýsing</span><span class="sxs-lookup"><span data-stu-id="d43e7-116">Description</span></span> | <span data-ttu-id="d43e7-117">Lýsing á rietnum.</span><span class="sxs-lookup"><span data-stu-id="d43e7-117">A description of the tile.</span></span> |
   | <span data-ttu-id="d43e7-118">Internet-fang</span><span class="sxs-lookup"><span data-stu-id="d43e7-118">Internet address</span></span> | <span data-ttu-id="d43e7-119">Sláðu slóðina inn á sjálfsafgreiðslusíðuna fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="d43e7-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="d43e7-120">Stærð reits</span><span class="sxs-lookup"><span data-stu-id="d43e7-120">Tile size</span></span> | <span data-ttu-id="d43e7-121">Stærð flísanna: Lítil, meðalstór eða stór.</span><span class="sxs-lookup"><span data-stu-id="d43e7-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="d43e7-122">Mark</span><span class="sxs-lookup"><span data-stu-id="d43e7-122">Target</span></span> | <span data-ttu-id="d43e7-123">Tilgreinir hvort síðan eigi að opna í nýjum glugga eða núverandi glugga.</span><span class="sxs-lookup"><span data-stu-id="d43e7-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="d43e7-124">Bakgrunnsmynd reits</span><span class="sxs-lookup"><span data-stu-id="d43e7-124">Tile background image</span></span> | <span data-ttu-id="d43e7-125">Slóðin á myndina sem á að nota fyrir reitinn (valfrjálst).</span><span class="sxs-lookup"><span data-stu-id="d43e7-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="d43e7-126">Hefst</span><span class="sxs-lookup"><span data-stu-id="d43e7-126">Start</span></span> | <span data-ttu-id="d43e7-127">Upphafsdagsetning og tími sem reiturinn ætti að vera tiltækur.</span><span class="sxs-lookup"><span data-stu-id="d43e7-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="d43e7-128">Lýkur</span><span class="sxs-lookup"><span data-stu-id="d43e7-128">End</span></span> | <span data-ttu-id="d43e7-129">Lokasetning og tími sem reiturinn ætti að vera tiltækur.</span><span class="sxs-lookup"><span data-stu-id="d43e7-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="d43e7-130">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d43e7-130">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="d43e7-131">Uppsetning reits fríðindaáætlana</span><span class="sxs-lookup"><span data-stu-id="d43e7-131">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="d43e7-132">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **sjálfsafgreiðslufæribreytur starfsmanns**.</span><span class="sxs-lookup"><span data-stu-id="d43e7-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="d43e7-133">Veldu **Uppsetning reits fríðindaáætlunar** flipanum og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d43e7-133">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="d43e7-134">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="d43e7-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="d43e7-135">Svæði</span><span class="sxs-lookup"><span data-stu-id="d43e7-135">Field</span></span> | <span data-ttu-id="d43e7-136">Lýsing</span><span class="sxs-lookup"><span data-stu-id="d43e7-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d43e7-137">Auðkenni reits</span><span class="sxs-lookup"><span data-stu-id="d43e7-137">Tile ID</span></span> | <span data-ttu-id="d43e7-138">Einkvæmt auðkenni fyrir reitinn.</span><span class="sxs-lookup"><span data-stu-id="d43e7-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="d43e7-139">Texti merkis reits</span><span class="sxs-lookup"><span data-stu-id="d43e7-139">Tile label text</span></span> | <span data-ttu-id="d43e7-140">Textinn sem birtist fyrir reitinn í sjálfsafgreiðslunni.</span><span class="sxs-lookup"><span data-stu-id="d43e7-140">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="d43e7-141">Lýsing</span><span class="sxs-lookup"><span data-stu-id="d43e7-141">Description</span></span> | <span data-ttu-id="d43e7-142">Lýsing á rietnum.</span><span class="sxs-lookup"><span data-stu-id="d43e7-142">A description of the tile.</span></span> |
   | <span data-ttu-id="d43e7-143">Internet-fang</span><span class="sxs-lookup"><span data-stu-id="d43e7-143">Internet address</span></span> | <span data-ttu-id="d43e7-144">Sláðu slóðina inn á sjálfsafgreiðslusíðuna fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="d43e7-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="d43e7-145">Stærð reits</span><span class="sxs-lookup"><span data-stu-id="d43e7-145">Tile size</span></span> | <span data-ttu-id="d43e7-146">Stærð flísanna: Lítil, meðalstór eða stór.</span><span class="sxs-lookup"><span data-stu-id="d43e7-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="d43e7-147">Mark</span><span class="sxs-lookup"><span data-stu-id="d43e7-147">Target</span></span> | <span data-ttu-id="d43e7-148">Tilgreinir hvort síðan eigi að opna í nýjum glugga eða núverandi glugga.</span><span class="sxs-lookup"><span data-stu-id="d43e7-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="d43e7-149">Bakgrunnsmynd reits</span><span class="sxs-lookup"><span data-stu-id="d43e7-149">Tile background image</span></span> | <span data-ttu-id="d43e7-150">Slóðin á myndina sem á að nota fyrir reitinn (valfrjálst).</span><span class="sxs-lookup"><span data-stu-id="d43e7-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="d43e7-151">Hefst</span><span class="sxs-lookup"><span data-stu-id="d43e7-151">Start</span></span> | <span data-ttu-id="d43e7-152">Upphafsdagsetning og tími sem reiturinn ætti að vera tiltækur.</span><span class="sxs-lookup"><span data-stu-id="d43e7-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="d43e7-153">Lýkur</span><span class="sxs-lookup"><span data-stu-id="d43e7-153">End</span></span> | <span data-ttu-id="d43e7-154">Lokasetning og tími sem reiturinn ætti að vera tiltækur.</span><span class="sxs-lookup"><span data-stu-id="d43e7-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="d43e7-155">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d43e7-155">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="d43e7-156">Settu upp sveigjanlegt lánsféplan</span><span class="sxs-lookup"><span data-stu-id="d43e7-156">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="d43e7-157">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **sjálfsafgreiðslufæribreytur starfsmanns**.</span><span class="sxs-lookup"><span data-stu-id="d43e7-157">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="d43e7-158">Veldu **Uppsetning reits sveigjanlegrar útgjaldaáætlunar** flipanum og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d43e7-158">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="d43e7-159">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="d43e7-159">Specify values for the following fields:</span></span>

   | <span data-ttu-id="d43e7-160">Svæði</span><span class="sxs-lookup"><span data-stu-id="d43e7-160">Field</span></span> | <span data-ttu-id="d43e7-161">Lýsing</span><span class="sxs-lookup"><span data-stu-id="d43e7-161">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d43e7-162">Auðkenni reits</span><span class="sxs-lookup"><span data-stu-id="d43e7-162">Tile ID</span></span> | <span data-ttu-id="d43e7-163">Einkvæmt auðkenni fyrir reitinn.</span><span class="sxs-lookup"><span data-stu-id="d43e7-163">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="d43e7-164">Texti merkis reits</span><span class="sxs-lookup"><span data-stu-id="d43e7-164">Tile label text</span></span> | <span data-ttu-id="d43e7-165">Textinn sem birtist fyrir reitinn í sjálfsafgreiðslunni.</span><span class="sxs-lookup"><span data-stu-id="d43e7-165">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="d43e7-166">Lýsing</span><span class="sxs-lookup"><span data-stu-id="d43e7-166">Description</span></span> | <span data-ttu-id="d43e7-167">Lýsing á rietnum.</span><span class="sxs-lookup"><span data-stu-id="d43e7-167">A description of the tile.</span></span> |
   | <span data-ttu-id="d43e7-168">Internet-fang</span><span class="sxs-lookup"><span data-stu-id="d43e7-168">Internet address</span></span> | <span data-ttu-id="d43e7-169">Sláðu slóðina inn á sjálfsafgreiðslusíðuna fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="d43e7-169">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="d43e7-170">Stærð reits</span><span class="sxs-lookup"><span data-stu-id="d43e7-170">Tile size</span></span> | <span data-ttu-id="d43e7-171">Stærð flísanna: Lítil, meðalstór eða stór.</span><span class="sxs-lookup"><span data-stu-id="d43e7-171">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="d43e7-172">Mark</span><span class="sxs-lookup"><span data-stu-id="d43e7-172">Target</span></span> | <span data-ttu-id="d43e7-173">Tilgreinir hvort síðan eigi að opna í nýjum glugga eða núverandi glugga.</span><span class="sxs-lookup"><span data-stu-id="d43e7-173">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="d43e7-174">Bakgrunnsmynd reits</span><span class="sxs-lookup"><span data-stu-id="d43e7-174">Tile background image</span></span> | <span data-ttu-id="d43e7-175">Slóðin á myndina sem á að nota fyrir reitinn (valfrjálst).</span><span class="sxs-lookup"><span data-stu-id="d43e7-175">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="d43e7-176">Hefst</span><span class="sxs-lookup"><span data-stu-id="d43e7-176">Start</span></span> | <span data-ttu-id="d43e7-177">Upphafsdagsetning og tími sem reiturinn ætti að vera tiltækur.</span><span class="sxs-lookup"><span data-stu-id="d43e7-177">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="d43e7-178">Lýkur</span><span class="sxs-lookup"><span data-stu-id="d43e7-178">End</span></span> | <span data-ttu-id="d43e7-179">Lokasetning og tími sem reiturinn ætti að vera tiltækur.</span><span class="sxs-lookup"><span data-stu-id="d43e7-179">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="d43e7-180">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d43e7-180">Select **Save**.</span></span>
