---
title: Vinna með uppskrift fyrir afbrigðalíkan afurðar
description: Keyra þetta ferli krefst fyrirliggjandi skilgreiningu afbrigðalíkan afurðar.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 267ac5447d36f63094fdb57c0d450e4d79cf138b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4966856"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="04fd4-103">Vinna með uppskrift fyrir afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="04fd4-103">Maintain BOM for a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="04fd4-104">Keyra þetta ferli krefst fyrirliggjandi skilgreiningu afbrigðalíkan afurðar.</span><span class="sxs-lookup"><span data-stu-id="04fd4-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="04fd4-105">Hágæða hátalara líkan í fyrirtækinu sýnigögn USMF er notað til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="04fd4-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="04fd4-106">Bæta við uppskriftarlína</span><span class="sxs-lookup"><span data-stu-id="04fd4-106">Add a BOM line</span></span>
1. <span data-ttu-id="04fd4-107">Smellið á Skilgreining afurðarafbrigðislíkans</span><span class="sxs-lookup"><span data-stu-id="04fd4-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="04fd4-108">Smella á Afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="04fd4-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="04fd4-109">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="04fd4-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="04fd4-110">Veljið hágæða hátalara fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="04fd4-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="04fd4-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="04fd4-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="04fd4-112">Stækka hlutann uppskriftarlínunum.</span><span class="sxs-lookup"><span data-stu-id="04fd4-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="04fd4-113">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="04fd4-113">Click Add.</span></span>
7. <span data-ttu-id="04fd4-114">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="04fd4-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="04fd4-115">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="04fd4-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="04fd4-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="04fd4-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="04fd4-117">Bæta við uppskriftarlínuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="04fd4-117">Add BOM line details</span></span>
1. <span data-ttu-id="04fd4-118">Smellt er á uppskriftarlínuupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="04fd4-118">Click BOM line details.</span></span>
2. <span data-ttu-id="04fd4-119">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="04fd4-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="04fd4-120">Til dæmis er hægt að velja M0055 vöru.</span><span class="sxs-lookup"><span data-stu-id="04fd4-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="04fd4-121">Fyrir hvern línueiginleika Uppskriftar, er hægt að velja hvort hún tekur fast gildi eða er varpað á eigind.</span><span class="sxs-lookup"><span data-stu-id="04fd4-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="04fd4-122">Veljið gátreitinn stilla.</span><span class="sxs-lookup"><span data-stu-id="04fd4-122">Select the Set check box.</span></span>
4. <span data-ttu-id="04fd4-123">Velja skal Já í Útreiknings reitnum.</span><span class="sxs-lookup"><span data-stu-id="04fd4-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="04fd4-124">Útreikningur eiginleika er stillt á Já tryggir uppskriftarlínunni er með í útreikningi kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="04fd4-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="04fd4-125">Smellið á flipann „Setja upp“.</span><span class="sxs-lookup"><span data-stu-id="04fd4-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="04fd4-126">Veljið gátreitinn stilla.</span><span class="sxs-lookup"><span data-stu-id="04fd4-126">Select the Set check box.</span></span>
7. <span data-ttu-id="04fd4-127">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="04fd4-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="04fd4-128">Magn svæðið ákvarðar hversu mikið vörunnar sem verða innifalin í Uppskriftinni.</span><span class="sxs-lookup"><span data-stu-id="04fd4-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="04fd4-129">Þetta gæti verið að augljós umsækjanda fyrir eigindarvörpun.</span><span class="sxs-lookup"><span data-stu-id="04fd4-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="04fd4-130">Smellt er á víddaflipann.</span><span class="sxs-lookup"><span data-stu-id="04fd4-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="04fd4-131">Staðfesta ef einhver afurðarvíddum eru virk og þess vegna verður að hafa gildi eða eigind sem er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="04fd4-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="04fd4-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="04fd4-132">Click OK.</span></span>

