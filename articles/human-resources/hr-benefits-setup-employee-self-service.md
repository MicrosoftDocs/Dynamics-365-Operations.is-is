---
title: Grunnstilla sjálfsafgreiðslu starfsmanns
description: Í Microsoft Dynamics 365 Human Resources, þú getur stillt flísar fyrir toppstig siglingar í sjálfsafgreiðslu starfsmanna.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
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
ms.openlocfilehash: dbbcb10f1d14088435248c3354ac153b23e5f8d7
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229810"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="09ed6-103">Grunnstilla sjálfsafgreiðslu starfsmanns</span><span class="sxs-lookup"><span data-stu-id="09ed6-103">Configure employee self service</span></span>

<span data-ttu-id="09ed6-104">Í Microsoft Dynamics 365 Human Resources, þú getur stillt flísar fyrir toppstig siglingar í sjálfsafgreiðslu starfsmanna.</span><span class="sxs-lookup"><span data-stu-id="09ed6-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="09ed6-105">Reitir fríðindaáætlunar beinir notendum að fríðindaáætlunum sem þeir eru hæfir fyrir.</span><span class="sxs-lookup"><span data-stu-id="09ed6-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="09ed6-106">Uppsetning reits fríðindaáætlana</span><span class="sxs-lookup"><span data-stu-id="09ed6-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="09ed6-107">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **sjálfsafgreiðslufæribreytur starfsmanns**.</span><span class="sxs-lookup"><span data-stu-id="09ed6-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="09ed6-108">Veldu **Uppsetning reits fríðindaáætlunar** flipanum og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="09ed6-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="09ed6-109">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="09ed6-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="09ed6-110">Svæði</span><span class="sxs-lookup"><span data-stu-id="09ed6-110">Field</span></span> | <span data-ttu-id="09ed6-111">Lýsing</span><span class="sxs-lookup"><span data-stu-id="09ed6-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="09ed6-112">**Auðkenni reits**</span><span class="sxs-lookup"><span data-stu-id="09ed6-112">**Tile ID**</span></span> | <span data-ttu-id="09ed6-113">Einkvæmt auðkenni fyrir reitinn.</span><span class="sxs-lookup"><span data-stu-id="09ed6-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="09ed6-114">**Texti merkis reits**</span><span class="sxs-lookup"><span data-stu-id="09ed6-114">**Tile label text**</span></span> | <span data-ttu-id="09ed6-115">Textinn sem birtist fyrir reitinn í sjálfsafgreiðslunni.</span><span class="sxs-lookup"><span data-stu-id="09ed6-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="09ed6-116">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="09ed6-116">**Description**</span></span> | <span data-ttu-id="09ed6-117">Lýsing á rietnum.</span><span class="sxs-lookup"><span data-stu-id="09ed6-117">A description of the tile.</span></span> |
   | <span data-ttu-id="09ed6-118">**Internet-fang**</span><span class="sxs-lookup"><span data-stu-id="09ed6-118">**Internet address**</span></span> | <span data-ttu-id="09ed6-119">Sláðu slóðina inn á sjálfsafgreiðslusíðuna fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="09ed6-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="09ed6-120">**Stærð reits**</span><span class="sxs-lookup"><span data-stu-id="09ed6-120">**Tile size**</span></span> | <span data-ttu-id="09ed6-121">Stærð flísanna: Lítil, meðalstór eða stór.</span><span class="sxs-lookup"><span data-stu-id="09ed6-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="09ed6-122">**Mark**</span><span class="sxs-lookup"><span data-stu-id="09ed6-122">**Target**</span></span> | <span data-ttu-id="09ed6-123">Tilgreinir hvort síðan eigi að opna í nýjum glugga eða núverandi glugga.</span><span class="sxs-lookup"><span data-stu-id="09ed6-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="09ed6-124">**Bakgrunnsmynd reits**</span><span class="sxs-lookup"><span data-stu-id="09ed6-124">**Tile background image**</span></span> | <span data-ttu-id="09ed6-125">Slóðin á myndina sem á að nota fyrir reitinn (valfrjálst).</span><span class="sxs-lookup"><span data-stu-id="09ed6-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="09ed6-126">**Hefst**</span><span class="sxs-lookup"><span data-stu-id="09ed6-126">**Start**</span></span> | <span data-ttu-id="09ed6-127">Upphafsdagsetning og tími sem reiturinn ætti að vera tiltækur.</span><span class="sxs-lookup"><span data-stu-id="09ed6-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="09ed6-128">**Lýkur**</span><span class="sxs-lookup"><span data-stu-id="09ed6-128">**End**</span></span> | <span data-ttu-id="09ed6-129">Lokasetning og tími sem reiturinn ætti að vera tiltækur.</span><span class="sxs-lookup"><span data-stu-id="09ed6-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="09ed6-130">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="09ed6-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="09ed6-131">Settu upp sveigjanlegt lánsféplan</span><span class="sxs-lookup"><span data-stu-id="09ed6-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="09ed6-132">Í vinnusvæðinu **Fríðindastjórnun**, undir **Skipulag**, veldu **sjálfsafgreiðslufæribreytur starfsmanns**.</span><span class="sxs-lookup"><span data-stu-id="09ed6-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="09ed6-133">Veldu **Uppsetning reits sveigjanlegrar útgjaldaáætlunar** flipanum og veldu síðan **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="09ed6-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="09ed6-134">Tilgreina gildi fyrir eftirfarandi reiti:</span><span class="sxs-lookup"><span data-stu-id="09ed6-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="09ed6-135">Svæði</span><span class="sxs-lookup"><span data-stu-id="09ed6-135">Field</span></span> | <span data-ttu-id="09ed6-136">Lýsing</span><span class="sxs-lookup"><span data-stu-id="09ed6-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="09ed6-137">**Auðkenni reits**</span><span class="sxs-lookup"><span data-stu-id="09ed6-137">**Tile ID**</span></span> | <span data-ttu-id="09ed6-138">Einkvæmt auðkenni fyrir reitinn.</span><span class="sxs-lookup"><span data-stu-id="09ed6-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="09ed6-139">**Texti merkis reits**</span><span class="sxs-lookup"><span data-stu-id="09ed6-139">**Tile label text**</span></span> | <span data-ttu-id="09ed6-140">Textinn sem birtist fyrir reitinn í sjálfsafgreiðslunni.</span><span class="sxs-lookup"><span data-stu-id="09ed6-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="09ed6-141">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="09ed6-141">**Description**</span></span> | <span data-ttu-id="09ed6-142">Lýsing á rietnum.</span><span class="sxs-lookup"><span data-stu-id="09ed6-142">A description of the tile.</span></span> |
   | <span data-ttu-id="09ed6-143">**Internet-fang**</span><span class="sxs-lookup"><span data-stu-id="09ed6-143">**Internet address**</span></span> | <span data-ttu-id="09ed6-144">Sláðu slóðina inn á sjálfsafgreiðslusíðuna fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="09ed6-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="09ed6-145">**Stærð reits**</span><span class="sxs-lookup"><span data-stu-id="09ed6-145">**Tile size**</span></span> | <span data-ttu-id="09ed6-146">Stærð flísanna: Lítil, meðalstór eða stór.</span><span class="sxs-lookup"><span data-stu-id="09ed6-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="09ed6-147">**Mark**</span><span class="sxs-lookup"><span data-stu-id="09ed6-147">**Target**</span></span> | <span data-ttu-id="09ed6-148">Tilgreinir hvort síðan eigi að opna í nýjum glugga eða núverandi glugga.</span><span class="sxs-lookup"><span data-stu-id="09ed6-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="09ed6-149">**Bakgrunnsmynd reits**</span><span class="sxs-lookup"><span data-stu-id="09ed6-149">**Tile background image**</span></span> | <span data-ttu-id="09ed6-150">Slóðin á myndina sem á að nota fyrir reitinn (valfrjálst).</span><span class="sxs-lookup"><span data-stu-id="09ed6-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="09ed6-151">**Hefst**</span><span class="sxs-lookup"><span data-stu-id="09ed6-151">**Start**</span></span> | <span data-ttu-id="09ed6-152">Upphafsdagsetning og tími sem reiturinn ætti að vera tiltækur.</span><span class="sxs-lookup"><span data-stu-id="09ed6-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="09ed6-153">**Lýkur**</span><span class="sxs-lookup"><span data-stu-id="09ed6-153">**End**</span></span> | <span data-ttu-id="09ed6-154">Lokasetning og tími sem reiturinn ætti að vera tiltækur.</span><span class="sxs-lookup"><span data-stu-id="09ed6-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="09ed6-155">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="09ed6-155">Select **Save**.</span></span>
