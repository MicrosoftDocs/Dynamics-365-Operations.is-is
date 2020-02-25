---
title: Grunnstilla sjálfsafgreiðslu starfsmanns
description: ''
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
ms.openlocfilehash: e44a35071b8d0987e6c949fb11312204317b44a1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/03/2020
ms.locfileid: "3009421"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="ee77e-102">Grunnstilla sjálfsafgreiðslu starfsmanns</span><span class="sxs-lookup"><span data-stu-id="ee77e-102">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="ee77e-103">Í Microsoft Dynamics 365 Human Resources, þú getur stillt flísar fyrir toppstig siglingar í sjálfsafgreiðslu starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="ee77e-103">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="ee77e-104">Ávinningur áætlunarflísar beinir notendum að hagnaði áætlunum sem þeir eru gjaldgengir í.</span><span class="sxs-lookup"><span data-stu-id="ee77e-104">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="ee77e-105">Uppsetning á reit hlutverkamiðstöðvar</span><span class="sxs-lookup"><span data-stu-id="ee77e-105">Set up a role center tile</span></span>

1. <span data-ttu-id="ee77e-106">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **sjálfsafgreiðslufæribreytur starfsmanns**.</span><span class="sxs-lookup"><span data-stu-id="ee77e-106">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="ee77e-107">Veldu **Skipulag hlutverks miðflísar** flipanum og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="ee77e-107">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="ee77e-108">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="ee77e-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="ee77e-109">Svæði</span><span class="sxs-lookup"><span data-stu-id="ee77e-109">Field</span></span> | <span data-ttu-id="ee77e-110">Lýsing</span><span class="sxs-lookup"><span data-stu-id="ee77e-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ee77e-111">Auðkenni reits</span><span class="sxs-lookup"><span data-stu-id="ee77e-111">Tile ID</span></span> | <span data-ttu-id="ee77e-112">Einkvæmt auðkenni fyrir reitinn.</span><span class="sxs-lookup"><span data-stu-id="ee77e-112">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="ee77e-113">Texti merkis reits</span><span class="sxs-lookup"><span data-stu-id="ee77e-113">Tile label text</span></span> | <span data-ttu-id="ee77e-114">Textinn sem birtist fyrir reitinn í sjálfsafgreiðslunni.</span><span class="sxs-lookup"><span data-stu-id="ee77e-114">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="ee77e-115">Lýsing</span><span class="sxs-lookup"><span data-stu-id="ee77e-115">Description</span></span> | <span data-ttu-id="ee77e-116">Lýsing á rietnum.</span><span class="sxs-lookup"><span data-stu-id="ee77e-116">A description of the tile.</span></span> |
   | <span data-ttu-id="ee77e-117">Internet-fang</span><span class="sxs-lookup"><span data-stu-id="ee77e-117">Internet address</span></span> | <span data-ttu-id="ee77e-118">Sláðu slóðina inn á sjálfsafgreiðslusíðuna fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="ee77e-118">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="ee77e-119">Stærð reits</span><span class="sxs-lookup"><span data-stu-id="ee77e-119">Tile size</span></span> | <span data-ttu-id="ee77e-120">Stærð flísanna: Lítil, meðalstór eða stór.</span><span class="sxs-lookup"><span data-stu-id="ee77e-120">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="ee77e-121">Mark</span><span class="sxs-lookup"><span data-stu-id="ee77e-121">Target</span></span> | <span data-ttu-id="ee77e-122">Tilgreinir hvort síðan eigi að opna í nýjum glugga eða núverandi glugga.</span><span class="sxs-lookup"><span data-stu-id="ee77e-122">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="ee77e-123">Bakgrunnsmynd reits</span><span class="sxs-lookup"><span data-stu-id="ee77e-123">Tile background image</span></span> | <span data-ttu-id="ee77e-124">Slóðin á myndina sem á að nota fyrir reitinn (valfrjálst).</span><span class="sxs-lookup"><span data-stu-id="ee77e-124">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="ee77e-125">Hefst</span><span class="sxs-lookup"><span data-stu-id="ee77e-125">Start</span></span> | <span data-ttu-id="ee77e-126">Upphafsdagsetning og tími sem reiturinn ætti að vera tiltækur.</span><span class="sxs-lookup"><span data-stu-id="ee77e-126">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="ee77e-127">Lýkur</span><span class="sxs-lookup"><span data-stu-id="ee77e-127">End</span></span> | <span data-ttu-id="ee77e-128">Lokasetning og tími sem reiturinn ætti að vera tiltækur.</span><span class="sxs-lookup"><span data-stu-id="ee77e-128">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="ee77e-129">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="ee77e-129">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="ee77e-130">Uppsetning reits fríðindaáætlana</span><span class="sxs-lookup"><span data-stu-id="ee77e-130">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="ee77e-131">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **sjálfsafgreiðslufæribreytur starfsmanns**.</span><span class="sxs-lookup"><span data-stu-id="ee77e-131">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="ee77e-132">Veldu **Uppsetning reits fríðindaáætlunar** flipanum og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="ee77e-132">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="ee77e-133">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="ee77e-133">Specify values for the following fields:</span></span>

   | <span data-ttu-id="ee77e-134">Svæði</span><span class="sxs-lookup"><span data-stu-id="ee77e-134">Field</span></span> | <span data-ttu-id="ee77e-135">Lýsing</span><span class="sxs-lookup"><span data-stu-id="ee77e-135">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ee77e-136">Auðkenni reits</span><span class="sxs-lookup"><span data-stu-id="ee77e-136">Tile ID</span></span> | <span data-ttu-id="ee77e-137">Einkvæmt auðkenni fyrir reitinn.</span><span class="sxs-lookup"><span data-stu-id="ee77e-137">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="ee77e-138">Texti merkis reits</span><span class="sxs-lookup"><span data-stu-id="ee77e-138">Tile label text</span></span> | <span data-ttu-id="ee77e-139">Textinn sem birtist fyrir reitinn í sjálfsafgreiðslunni.</span><span class="sxs-lookup"><span data-stu-id="ee77e-139">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="ee77e-140">Lýsing</span><span class="sxs-lookup"><span data-stu-id="ee77e-140">Description</span></span> | <span data-ttu-id="ee77e-141">Lýsing á rietnum.</span><span class="sxs-lookup"><span data-stu-id="ee77e-141">A description of the tile.</span></span> |
   | <span data-ttu-id="ee77e-142">Internet-fang</span><span class="sxs-lookup"><span data-stu-id="ee77e-142">Internet address</span></span> | <span data-ttu-id="ee77e-143">Sláðu slóðina inn á sjálfsafgreiðslusíðuna fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="ee77e-143">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="ee77e-144">Stærð reits</span><span class="sxs-lookup"><span data-stu-id="ee77e-144">Tile size</span></span> | <span data-ttu-id="ee77e-145">Stærð flísanna: Lítil, meðalstór eða stór.</span><span class="sxs-lookup"><span data-stu-id="ee77e-145">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="ee77e-146">Mark</span><span class="sxs-lookup"><span data-stu-id="ee77e-146">Target</span></span> | <span data-ttu-id="ee77e-147">Tilgreinir hvort síðan eigi að opna í nýjum glugga eða núverandi glugga.</span><span class="sxs-lookup"><span data-stu-id="ee77e-147">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="ee77e-148">Bakgrunnsmynd reits</span><span class="sxs-lookup"><span data-stu-id="ee77e-148">Tile background image</span></span> | <span data-ttu-id="ee77e-149">Slóðin á myndina sem á að nota fyrir reitinn (valfrjálst).</span><span class="sxs-lookup"><span data-stu-id="ee77e-149">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="ee77e-150">Hefst</span><span class="sxs-lookup"><span data-stu-id="ee77e-150">Start</span></span> | <span data-ttu-id="ee77e-151">Upphafsdagsetning og tími sem reiturinn ætti að vera tiltækur.</span><span class="sxs-lookup"><span data-stu-id="ee77e-151">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="ee77e-152">Lýkur</span><span class="sxs-lookup"><span data-stu-id="ee77e-152">End</span></span> | <span data-ttu-id="ee77e-153">Lokasetning og tími sem reiturinn ætti að vera tiltækur.</span><span class="sxs-lookup"><span data-stu-id="ee77e-153">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="ee77e-154">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="ee77e-154">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="ee77e-155">Settu upp sveigjanlegt lánsféplan</span><span class="sxs-lookup"><span data-stu-id="ee77e-155">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="ee77e-156">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **sjálfsafgreiðslufæribreytur starfsmanns**.</span><span class="sxs-lookup"><span data-stu-id="ee77e-156">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="ee77e-157">Veldu **Uppsetning reits sveigjanlegrar útgjaldaáætlunar** flipanum og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="ee77e-157">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="ee77e-158">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="ee77e-158">Specify values for the following fields:</span></span>

   | <span data-ttu-id="ee77e-159">Svæði</span><span class="sxs-lookup"><span data-stu-id="ee77e-159">Field</span></span> | <span data-ttu-id="ee77e-160">Lýsing</span><span class="sxs-lookup"><span data-stu-id="ee77e-160">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="ee77e-161">Auðkenni reits</span><span class="sxs-lookup"><span data-stu-id="ee77e-161">Tile ID</span></span> | <span data-ttu-id="ee77e-162">Einkvæmt auðkenni fyrir reitinn.</span><span class="sxs-lookup"><span data-stu-id="ee77e-162">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="ee77e-163">Texti merkis reits</span><span class="sxs-lookup"><span data-stu-id="ee77e-163">Tile label text</span></span> | <span data-ttu-id="ee77e-164">Textinn sem birtist fyrir reitinn í sjálfsafgreiðslunni.</span><span class="sxs-lookup"><span data-stu-id="ee77e-164">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="ee77e-165">Lýsing</span><span class="sxs-lookup"><span data-stu-id="ee77e-165">Description</span></span> | <span data-ttu-id="ee77e-166">Lýsing á rietnum.</span><span class="sxs-lookup"><span data-stu-id="ee77e-166">A description of the tile.</span></span> |
   | <span data-ttu-id="ee77e-167">Internet-fang</span><span class="sxs-lookup"><span data-stu-id="ee77e-167">Internet address</span></span> | <span data-ttu-id="ee77e-168">Sláðu slóðina inn á sjálfsafgreiðslusíðuna fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="ee77e-168">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="ee77e-169">Stærð reits</span><span class="sxs-lookup"><span data-stu-id="ee77e-169">Tile size</span></span> | <span data-ttu-id="ee77e-170">Stærð flísanna: Lítil, meðalstór eða stór.</span><span class="sxs-lookup"><span data-stu-id="ee77e-170">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="ee77e-171">Mark</span><span class="sxs-lookup"><span data-stu-id="ee77e-171">Target</span></span> | <span data-ttu-id="ee77e-172">Tilgreinir hvort síðan eigi að opna í nýjum glugga eða núverandi glugga.</span><span class="sxs-lookup"><span data-stu-id="ee77e-172">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="ee77e-173">Bakgrunnsmynd reits</span><span class="sxs-lookup"><span data-stu-id="ee77e-173">Tile background image</span></span> | <span data-ttu-id="ee77e-174">Slóðin á myndina sem á að nota fyrir reitinn (valfrjálst).</span><span class="sxs-lookup"><span data-stu-id="ee77e-174">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="ee77e-175">Hefst</span><span class="sxs-lookup"><span data-stu-id="ee77e-175">Start</span></span> | <span data-ttu-id="ee77e-176">Upphafsdagsetning og tími sem reiturinn ætti að vera tiltækur.</span><span class="sxs-lookup"><span data-stu-id="ee77e-176">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="ee77e-177">Lýkur</span><span class="sxs-lookup"><span data-stu-id="ee77e-177">End</span></span> | <span data-ttu-id="ee77e-178">Lokasetning og tími sem reiturinn ætti að vera tiltækur.</span><span class="sxs-lookup"><span data-stu-id="ee77e-178">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="ee77e-179">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="ee77e-179">Select **Save**.</span></span>
