---
title: Gámar
description: Þetta efnisatriði lýsir því hvernig eigi að setja upp gáma fyrir Heildarkostnaður eininguna.
author: sherry-zheng
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 2f7e9435aa3d0d06e1cc51457a6343b807d76dc7
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833714"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="251e3-103">Uppsetning gáms</span><span class="sxs-lookup"><span data-stu-id="251e3-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="251e3-104">Í þessu efnisatriði er lýst hvernig eigi að setja upp gáma fyrir **Heildarkostnaður** eininguna.</span><span class="sxs-lookup"><span data-stu-id="251e3-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a><span data-ttu-id="251e3-105">Setja upp gámagerðir</span><span class="sxs-lookup"><span data-stu-id="251e3-105">Set up shipping container types</span></span>

<span data-ttu-id="251e3-106">Gámagerðir skilgreina gerðir gáma sem er hægt að nota í sendingum og ferðum.</span><span class="sxs-lookup"><span data-stu-id="251e3-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="251e3-107">Til að vinna með gámagerðirnar skal fara í **Heildarkostnaður \> Gámauppsetning \> Gámagerðir**.</span><span class="sxs-lookup"><span data-stu-id="251e3-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="251e3-108">Þar er hægt að skoða, bæta við og fjarlægja færslur fyrir gámagerðirnar.</span><span class="sxs-lookup"><span data-stu-id="251e3-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="251e3-109">Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.</span><span class="sxs-lookup"><span data-stu-id="251e3-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="251e3-110">Svæði</span><span class="sxs-lookup"><span data-stu-id="251e3-110">Field</span></span> | <span data-ttu-id="251e3-111">lýsing</span><span class="sxs-lookup"><span data-stu-id="251e3-111">Description</span></span> |
|---|---|
| <span data-ttu-id="251e3-112">Gámagerð</span><span class="sxs-lookup"><span data-stu-id="251e3-112">Shipping container type</span></span> | <span data-ttu-id="251e3-113">Færið inn einkvæmt auðkennisheiti/númer fyrir gámagerðina.</span><span class="sxs-lookup"><span data-stu-id="251e3-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="251e3-114">lýsing</span><span class="sxs-lookup"><span data-stu-id="251e3-114">Description</span></span> | <span data-ttu-id="251e3-115">Færið inn lýsingu á gámagerðinni.</span><span class="sxs-lookup"><span data-stu-id="251e3-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="251e3-116">Magn</span><span class="sxs-lookup"><span data-stu-id="251e3-116">Volume</span></span> | <span data-ttu-id="251e3-117">Sláið inn hámarksmagn sem leyft er í gámum af þessari gerð.</span><span class="sxs-lookup"><span data-stu-id="251e3-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="251e3-118">Vægi</span><span class="sxs-lookup"><span data-stu-id="251e3-118">Weight</span></span> | <span data-ttu-id="251e3-119">Sláið inn hámarksþyngd sem leyfð er í gámum af þessari gerð.</span><span class="sxs-lookup"><span data-stu-id="251e3-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="251e3-120">Hægt að skila</span><span class="sxs-lookup"><span data-stu-id="251e3-120">Returnable</span></span> | <span data-ttu-id="251e3-121">Tilgreinið hvort hægt er að skila gámum af þessari gerð til lánardrottins þegar búið er að nota hann í ferð.</span><span class="sxs-lookup"><span data-stu-id="251e3-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="251e3-122">Ef þessi valkostur er stilltur á *Já* gæti aukalegur kostnaður átt við um skil á gámum af þessari gerð til upprunalegrar hafnar.</span><span class="sxs-lookup"><span data-stu-id="251e3-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="251e3-123">Setja upp gáma</span><span class="sxs-lookup"><span data-stu-id="251e3-123">Set up shipping containers</span></span>

<span data-ttu-id="251e3-124">Gámafærslur eru notaðar til að bera kennsl á hvern gám sem notaður er í ferðum.</span><span class="sxs-lookup"><span data-stu-id="251e3-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="251e3-125">Þegar ferð er stofnuð er hægt að velja tilgreindan gám fyrir hana í listanum yfir allar gámafærslur sem búið er að skilgreina hér.</span><span class="sxs-lookup"><span data-stu-id="251e3-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="251e3-126">Þessi eiginleiki er mjög gagnlegur ef fyrirtækið á eigin gáma.</span><span class="sxs-lookup"><span data-stu-id="251e3-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="251e3-127">Ekki þarf að slá inn gámanúmerin fyrir gáma sem verða aðeins notaðir einu sinni.</span><span class="sxs-lookup"><span data-stu-id="251e3-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="251e3-128">Í staðinn er hægt að bæta við gámanúmerinu þegar ferðin er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="251e3-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="251e3-129">Gámafærslur eru aðeins notaðar í heildarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="251e3-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="251e3-130">Þær eru ekki í boði í staðlaðri **Flutningsstjórnun** einingu (TMS).</span><span class="sxs-lookup"><span data-stu-id="251e3-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="251e3-131">Til að vinna gáma skal fara í **Heildarkostnaður \> Gámauppsetning \> Gámar**.</span><span class="sxs-lookup"><span data-stu-id="251e3-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="251e3-132">Þar er hægt að skoða, bæta við og fjarlægja færslur gámanna.</span><span class="sxs-lookup"><span data-stu-id="251e3-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="251e3-133">Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.</span><span class="sxs-lookup"><span data-stu-id="251e3-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="251e3-134">Svæði</span><span class="sxs-lookup"><span data-stu-id="251e3-134">Field</span></span> | <span data-ttu-id="251e3-135">lýsing</span><span class="sxs-lookup"><span data-stu-id="251e3-135">Description</span></span> |
|---|---|
| <span data-ttu-id="251e3-136">Gámur</span><span class="sxs-lookup"><span data-stu-id="251e3-136">Shipping container</span></span> | <span data-ttu-id="251e3-137">Færið inn einkvæmt auðkennisheiti/númer fyrir gám.</span><span class="sxs-lookup"><span data-stu-id="251e3-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="251e3-138">Gámagerð</span><span class="sxs-lookup"><span data-stu-id="251e3-138">Shipping container type</span></span> | <span data-ttu-id="251e3-139">Velja gerð gáms.</span><span class="sxs-lookup"><span data-stu-id="251e3-139">Select the type of shipping container.</span></span> <span data-ttu-id="251e3-140">Frekari upplýsingar er að finna í hlutanum [Setja upp gámagerðir](#shipping-container-types) fyrr í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="251e3-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="251e3-141">Uppsetning gáms er valfrjáls.</span><span class="sxs-lookup"><span data-stu-id="251e3-141">The shipping container setup is optional.</span></span> <span data-ttu-id="251e3-142">Yfirleitt verður hún aðeins notuð ef fyrirtækið á eigin gáma eða notar oft sömu gámana.</span><span class="sxs-lookup"><span data-stu-id="251e3-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="251e3-143">Engar vartölur eru reiknaðar fyrir gámanúmer.</span><span class="sxs-lookup"><span data-stu-id="251e3-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a><span data-ttu-id="251e3-144">Setja upp einingagerðir</span><span class="sxs-lookup"><span data-stu-id="251e3-144">Set up unit types</span></span>

<span data-ttu-id="251e3-145">Einingagerðir setja á frekari flokkanir og auðkenningaraðferðir fyrir gáma.</span><span class="sxs-lookup"><span data-stu-id="251e3-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="251e3-146">Einingagerðin er yfirleitt notuð til að auðkenna gerð gámsins sem vörum er pakkað í, t.d. bretti eða tunnur.</span><span class="sxs-lookup"><span data-stu-id="251e3-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="251e3-147">Hægt er að velja einingagerð þegar gámur er settur upp á **Allir gámar** síðunni.</span><span class="sxs-lookup"><span data-stu-id="251e3-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="251e3-148">Einingargerðir eru aðeins notaðar í heildarkostnaði.</span><span class="sxs-lookup"><span data-stu-id="251e3-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="251e3-149">Þetta er ekki í boði í TMS.</span><span class="sxs-lookup"><span data-stu-id="251e3-149">They aren't available in TMS.</span></span>

<span data-ttu-id="251e3-150">Til að vinna með einingargerðir skal fara í **Heildarkostnaður \> Gámauppsetning \> Einingagerðir**.</span><span class="sxs-lookup"><span data-stu-id="251e3-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="251e3-151">Þar er hægt að skoða, bæta við og fjarlægja færslur fyrir einingagerðirnar.</span><span class="sxs-lookup"><span data-stu-id="251e3-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="251e3-152">Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.</span><span class="sxs-lookup"><span data-stu-id="251e3-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="251e3-153">Svæði</span><span class="sxs-lookup"><span data-stu-id="251e3-153">Field</span></span> | <span data-ttu-id="251e3-154">lýsing</span><span class="sxs-lookup"><span data-stu-id="251e3-154">Description</span></span> |
|---|---|
| <span data-ttu-id="251e3-155">Einingargerð</span><span class="sxs-lookup"><span data-stu-id="251e3-155">Unit type</span></span> | <span data-ttu-id="251e3-156">Færið inn einkvæmt auðkennisheiti/númer fyrir einingagerðina.</span><span class="sxs-lookup"><span data-stu-id="251e3-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="251e3-157">lýsing</span><span class="sxs-lookup"><span data-stu-id="251e3-157">Description</span></span> | <span data-ttu-id="251e3-158">Færa inn lýsingu á einingagerðinni.</span><span class="sxs-lookup"><span data-stu-id="251e3-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a><span data-ttu-id="251e3-159">Setja upp kæligerðir</span><span class="sxs-lookup"><span data-stu-id="251e3-159">Set up refrigeration types</span></span>

<span data-ttu-id="251e3-160">Kæligerðir setja á frekari flokkanir og auðkenningaraðferðir fyrir gáma (yfirleitt kæligáma).</span><span class="sxs-lookup"><span data-stu-id="251e3-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="251e3-161">Hægt er að velja kæligerð þegar gámur er settur upp á síðunni **Allir gámar**.</span><span class="sxs-lookup"><span data-stu-id="251e3-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="251e3-162">Til að vinna með gerðir kælingar skal fara í **Heildarkostnaður \> Gámauppsetning \> Gerðir kælinga**.</span><span class="sxs-lookup"><span data-stu-id="251e3-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="251e3-163">Þar er hægt að skoða, bæta við og fjarlægja færslur fyrir kæligerðirnar.</span><span class="sxs-lookup"><span data-stu-id="251e3-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="251e3-164">Eftirfarandi tafla lýsir eritinum sem eru tiltækir fyrir hverja færslu.</span><span class="sxs-lookup"><span data-stu-id="251e3-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="251e3-165">Svæði</span><span class="sxs-lookup"><span data-stu-id="251e3-165">Field</span></span> | <span data-ttu-id="251e3-166">lýsing</span><span class="sxs-lookup"><span data-stu-id="251e3-166">Description</span></span> |
|---|---|
| <span data-ttu-id="251e3-167">Gerð kælingar</span><span class="sxs-lookup"><span data-stu-id="251e3-167">Refrigeration type</span></span> | <span data-ttu-id="251e3-168">Færið inn einkvæmt auðkennisheiti/númer fyrir kæligerðina.</span><span class="sxs-lookup"><span data-stu-id="251e3-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="251e3-169">lýsing</span><span class="sxs-lookup"><span data-stu-id="251e3-169">Description</span></span> | <span data-ttu-id="251e3-170">Færið inn lýsingu á kæligerðinni.</span><span class="sxs-lookup"><span data-stu-id="251e3-170">Enter a description of the refrigeration type.</span></span> |