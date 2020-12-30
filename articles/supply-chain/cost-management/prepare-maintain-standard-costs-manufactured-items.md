---
title: Undirbúa viðhald staðalkostnaðar fyrir framleiddar vörur
description: Þetta efnisatriði fjallar um skrefin til að undirbúa viðhald kostnaðar fyrir framleiddar vörur.
author: AndersGirke
manager: tfehr
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 866da2ce58e33676c2fa4bb2d6abfde891a5d021
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430370"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a><span data-ttu-id="1dc89-103">Undirbúa viðhald staðalkostnaðar fyrir framleiddar vörur</span><span class="sxs-lookup"><span data-stu-id="1dc89-103">Prepare to maintain standard costs for manufactured items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1dc89-104">Þetta efnisatriði fjallar um skrefin til að undirbúa viðhald kostnaðar fyrir framleiddar vörur.</span><span class="sxs-lookup"><span data-stu-id="1dc89-104">This topic describes the steps for preparing to maintain costs for manufactured items.</span></span> <span data-ttu-id="1dc89-105">Skrefin fyrir framleiddar vörur eru örlítið frábrugðin skrefunum fyrir keyptar vörur.</span><span class="sxs-lookup"><span data-stu-id="1dc89-105">The steps for manufactured items differ slightly from the steps for purchased items.</span></span>

<span data-ttu-id="1dc89-106">Reglur sem eru úthlutaðar framleiddum vörum geta haft áhrif á kostnaðarútreikninga fyrir framleiddu móðurvörurnar.</span><span class="sxs-lookup"><span data-stu-id="1dc89-106">Policies that are assigned to manufactured items can affect the cost calculations for the parent manufactured items.</span></span> <span data-ttu-id="1dc89-107">Til að undirbúa viðhald kostnaðar fyrir framleiddar vörur skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="1dc89-107">To prepare to maintain costs for manufactured items, follow these steps.</span></span>

1. <span data-ttu-id="1dc89-108">Úthlutaðu framleiddu vörunni vörulíkanaflokki.</span><span class="sxs-lookup"><span data-stu-id="1dc89-108">Assign an item model group to the manufactured item.</span></span> 

   <span data-ttu-id="1dc89-109">Vörulíkanaflokkurinn staðfestir að staðlaðar kostnaður verði notaður.</span><span class="sxs-lookup"><span data-stu-id="1dc89-109">The item model group identifies that standard costs will be used.</span></span>

2. <span data-ttu-id="1dc89-110">Úthlutið framleiddu vörunni vöruflokk.</span><span class="sxs-lookup"><span data-stu-id="1dc89-110">Assign an item group to the manufactured item.</span></span> 

   <span data-ttu-id="1dc89-111">Vöruflokkurinn inniheldur fjárhagslykla sem eiga við um framleiddu vöruna.</span><span class="sxs-lookup"><span data-stu-id="1dc89-111">The item group contains ledger accounts that apply to the manufactured item.</span></span> <span data-ttu-id="1dc89-112">Fjárhagslyklarnir fyrir framleidda vöru sem hafa birgðalíkan staðalkostnaðar innihalda nokkur framleiðslufrávik, frávik kostnaðarbreytingar og endurmat birgðakostnaðarins.</span><span class="sxs-lookup"><span data-stu-id="1dc89-112">The ledger accounts for a manufactured item that has a standard cost inventory model include several production variances, the cost change variance, and the inventory cost revaluation.</span></span>

3. <span data-ttu-id="1dc89-113">Úthluta vörunni birgðamælieiningu.</span><span class="sxs-lookup"><span data-stu-id="1dc89-113">Assign the inventory unit of measure to the item.</span></span> 

   <span data-ttu-id="1dc89-114">Kostnaður vörunnar er alltaf gefinn upp í birgðamælieiningu vörunnar.</span><span class="sxs-lookup"><span data-stu-id="1dc89-114">The item's costs are always expressed in the item's inventory unit of measure.</span></span>

4. <span data-ttu-id="1dc89-115">Ekki úthluta framleiddu vörunni kostnaðarflokki nema farið verði með vöruna sem keypta vöru.</span><span class="sxs-lookup"><span data-stu-id="1dc89-115">Don't assign a cost group to the manufactured item unless the item will be treated as a purchased item.</span></span>

5. <span data-ttu-id="1dc89-116">Úthlutaðu framleiddu vörunni útreikningsflokki uppskriftar (BOM).</span><span class="sxs-lookup"><span data-stu-id="1dc89-116">Assign a bill of materials (BOM) calculation group to the manufactured item.</span></span> 

   <span data-ttu-id="1dc89-117">Flokkur uppskriftarútreiknings vörunnar skilgreinir viðvörunarskilyrði sem eiga við.</span><span class="sxs-lookup"><span data-stu-id="1dc89-117">The item's BOM calculation group defines warning conditions that apply.</span></span> <span data-ttu-id="1dc89-118">Þannig er hægt að búa til viðvörunarboð um mögulegar ástæður útreikningsskekkja þegar útreikningur uppskrifta er gerður.</span><span class="sxs-lookup"><span data-stu-id="1dc89-118">In that way, when a BOM calculation is done, warning messages can be generated about possible sources of calculation errors.</span></span> <span data-ttu-id="1dc89-119">Til dæmis getur viðvörunarboð borið kennsl á virka uppskrift eða leið sem er ekki til.</span><span class="sxs-lookup"><span data-stu-id="1dc89-119">For example, a warning message can identify when an active BOM or route doesn't exist.</span></span> <span data-ttu-id="1dc89-120">Flokkur uppskriftarútreikninga inniheldur reglu um stöðvun niðurbrots sem gefur til kynna hvenær framleidd vara skuli meðhöndluð sem keypt vara.</span><span class="sxs-lookup"><span data-stu-id="1dc89-120">The BOM calculation group contains a stop explosion policy that indicates when a manufactured item should be treated as a purchased item.</span></span>

6. <span data-ttu-id="1dc89-121">Úthlutaðu stöðluðu pöntunarmagni ef framleiddur hlutur hefur fastan kostnað.</span><span class="sxs-lookup"><span data-stu-id="1dc89-121">If the manufactured item has constant costs, assign a standard order quantity to it.</span></span> 

   <span data-ttu-id="1dc89-122">Staðlaða pöntunarmagnið er lotustærð bókhalds fyrir afskriftir á föstum kostnaði.</span><span class="sxs-lookup"><span data-stu-id="1dc89-122">The standard order quantity is an accounting lot size for amortizing constant costs.</span></span> <span data-ttu-id="1dc89-123">Dæmi um fastan kostnað eru uppsetningartími í leiðaraðgerðum og fast magn íhlutar í uppskrift (BOM).</span><span class="sxs-lookup"><span data-stu-id="1dc89-123">Examples of constant costs include setup times in routing operations and a constant component quantity in the BOM.</span></span>

7. <span data-ttu-id="1dc89-124">Skilgreinið uppskriftina fyrir framleiddu vöruna.</span><span class="sxs-lookup"><span data-stu-id="1dc89-124">Define the BOM for the manufactured item.</span></span> 

   <span data-ttu-id="1dc89-125">Hægt er að skilgreina eina eða fleiri uppskriftarútgáfur fyrir framleiddu vöruna.</span><span class="sxs-lookup"><span data-stu-id="1dc89-125">One or more BOM versions can be defined for the manufactured item.</span></span> <span data-ttu-id="1dc89-126">Staðfestu að útgáfurnar sem þú hefur áhuga á hafi verið merktar sem samþykktar og virkar og að þær hafi þær virku dagsetningar sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="1dc89-126">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="1dc89-127">Hægt er að láta uppskriftarútgáfuna eiga við um allt fyrirtækið eða eitt vefsetur.</span><span class="sxs-lookup"><span data-stu-id="1dc89-127">The BOM version can be company-wide or site-specific.</span></span>

8. <span data-ttu-id="1dc89-128">Skilgreinið leiðina fyrir framleiddu vöruna.</span><span class="sxs-lookup"><span data-stu-id="1dc89-128">Define the routing for the manufactured item.</span></span> 

   <span data-ttu-id="1dc89-129">Hægt er að skilgreina eina eða fleiri leiðarútgáfur fyrir framleiddu vöruna.</span><span class="sxs-lookup"><span data-stu-id="1dc89-129">One or more route versions can be defined for the manufactured item.</span></span> <span data-ttu-id="1dc89-130">Staðfestu að útgáfurnar sem þú hefur áhuga á hafi verið merktar sem samþykktar og virkar og að þær hafi þær virku dagsetningar sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="1dc89-130">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="1dc89-131">Leiðarútgáfan má ekki eiga við um nema eitt vefsetur.</span><span class="sxs-lookup"><span data-stu-id="1dc89-131">The route version must be site-specific.</span></span>

<span data-ttu-id="1dc89-132">Ef þú vilt nota leiðarlýsingar í kostnaðartilgangi er nauðsynlegt að frekari undirbúningur nauðsynlegur.</span><span class="sxs-lookup"><span data-stu-id="1dc89-132">If you want to use routing information for costing purposes, additional preparation steps are required.</span></span> <span data-ttu-id="1dc89-133">Til dæmis verða kostnaðarflokkarnir sem eru úthlutaðir til leiðaraðgerða að vera réttir og þeim lokið.</span><span class="sxs-lookup"><span data-stu-id="1dc89-133">For example, the cost categories that are assigned to routing operations must be correct and completed.</span></span>

<a name="related-topics"></a><span data-ttu-id="1dc89-134">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="1dc89-134">Related topics</span></span>
--------

[<span data-ttu-id="1dc89-135">Afskrifa fastan kostnað fyrir framleidda vöru</span><span class="sxs-lookup"><span data-stu-id="1dc89-135">Amortize constant costs for a manufactured item</span></span>](amortize-constant-costs-manufactured-item.md)

[<span data-ttu-id="1dc89-136">Uppsetning afurða sem hægt er að framleiða eða kaupa</span><span class="sxs-lookup"><span data-stu-id="1dc89-136">Set up products that can be produced or procured</span></span>](manufactured-items-treated-as-purchased-items.md)

