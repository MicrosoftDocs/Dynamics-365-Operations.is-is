---
title: Vinna með uppskrift fyrir afbrigðalíkan afurðar
description: Keyra þetta ferli krefst fyrirliggjandi skilgreiningu afbrigðalíkan afurðar.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, PCBOMLineDetails, InventItemIdLookupSimple
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 457aa5720919d8455a3099b200980bb36f60577f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "342386"
---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="a2936-103">Vinna með uppskrift fyrir afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="a2936-103">Maintain BOM for a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a2936-104">Keyra þetta ferli krefst fyrirliggjandi skilgreiningu afbrigðalíkan afurðar.</span><span class="sxs-lookup"><span data-stu-id="a2936-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="a2936-105">Hágæða hátalara líkan í fyrirtækinu sýnigögn USMF er notað til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="a2936-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="a2936-106">Bæta við uppskriftarlína</span><span class="sxs-lookup"><span data-stu-id="a2936-106">Add a BOM line</span></span>
1. <span data-ttu-id="a2936-107">Smellið á Skilgreining afurðarafbrigðislíkans</span><span class="sxs-lookup"><span data-stu-id="a2936-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="a2936-108">Smella á Afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="a2936-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="a2936-109">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a2936-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="a2936-110">Veljið hágæða hátalara fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="a2936-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="a2936-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a2936-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="a2936-112">Stækka hlutann uppskriftarlínunum.</span><span class="sxs-lookup"><span data-stu-id="a2936-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="a2936-113">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="a2936-113">Click Add.</span></span>
7. <span data-ttu-id="a2936-114">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a2936-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="a2936-115">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="a2936-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="a2936-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a2936-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="a2936-117">Bæta við uppskriftarlínuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="a2936-117">Add BOM line details</span></span>
1. <span data-ttu-id="a2936-118">Smellt er á uppskriftarlínuupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="a2936-118">Click BOM line details.</span></span>
2. <span data-ttu-id="a2936-119">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="a2936-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="a2936-120">Til dæmis er hægt að velja M0055 vöru.</span><span class="sxs-lookup"><span data-stu-id="a2936-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="a2936-121">Fyrir hvern línueiginleika Uppskriftar, er hægt að velja hvort hún tekur fast gildi eða er varpað á eigind.</span><span class="sxs-lookup"><span data-stu-id="a2936-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="a2936-122">Veljið gátreitinn stilla.</span><span class="sxs-lookup"><span data-stu-id="a2936-122">Select the Set check box.</span></span>
4. <span data-ttu-id="a2936-123">Velja skal Já í Útreiknings reitnum.</span><span class="sxs-lookup"><span data-stu-id="a2936-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="a2936-124">Útreikningur eiginleika er stillt á Já tryggir uppskriftarlínunni er með í útreikningi kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="a2936-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="a2936-125">Smellið á flipann „Setja upp“.</span><span class="sxs-lookup"><span data-stu-id="a2936-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="a2936-126">Veljið gátreitinn stilla.</span><span class="sxs-lookup"><span data-stu-id="a2936-126">Select the Set check box.</span></span>
7. <span data-ttu-id="a2936-127">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="a2936-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="a2936-128">Magn svæðið ákvarðar hversu mikið vörunnar sem verða innifalin í Uppskriftinni.</span><span class="sxs-lookup"><span data-stu-id="a2936-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="a2936-129">Þetta gæti verið að augljós umsækjanda fyrir eigindarvörpun.</span><span class="sxs-lookup"><span data-stu-id="a2936-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="a2936-130">Smellt er á víddaflipann.</span><span class="sxs-lookup"><span data-stu-id="a2936-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="a2936-131">Staðfesta ef einhver afurðarvíddum eru virk og þess vegna verður að hafa gildi eða eigind sem er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="a2936-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="a2936-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a2936-132">Click OK.</span></span>

