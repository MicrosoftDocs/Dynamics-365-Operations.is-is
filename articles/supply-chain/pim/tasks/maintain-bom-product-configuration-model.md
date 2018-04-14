--- 
title: "Vinna með uppskrift fyrir afbrigðalíkan afurðar"
description: "Keyra þetta ferli krefst fyrirliggjandi skilgreiningu afbrigðalíkan afurðar."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: ef7fc230ea028ef790ad7989fe53f95c70c3b5b1
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="4e1c9-103">Vinna með uppskrift fyrir afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="4e1c9-103">Maintain BOM for a product configuration model</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4e1c9-104">Keyra þetta ferli krefst fyrirliggjandi skilgreiningu afbrigðalíkan afurðar.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="4e1c9-105">Hágæða hátalara líkan í fyrirtækinu sýnigögn USMF er notað til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="4e1c9-106">Bæta við uppskriftarlína</span><span class="sxs-lookup"><span data-stu-id="4e1c9-106">Add a BOM line</span></span>
1. <span data-ttu-id="4e1c9-107">Smellið á Skilgreining afurðarafbrigðislíkans</span><span class="sxs-lookup"><span data-stu-id="4e1c9-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="4e1c9-108">Smella á Afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="4e1c9-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="4e1c9-109">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4e1c9-110">Veljið hágæða hátalara fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="4e1c9-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4e1c9-112">Stækka hlutann uppskriftarlínunum.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="4e1c9-113">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-113">Click Add.</span></span>
7. <span data-ttu-id="4e1c9-114">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="4e1c9-115">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="4e1c9-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="4e1c9-117">Bæta við uppskriftarlínuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="4e1c9-117">Add BOM line details</span></span>
1. <span data-ttu-id="4e1c9-118">Smellt er á uppskriftarlínuupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-118">Click BOM line details.</span></span>
2. <span data-ttu-id="4e1c9-119">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="4e1c9-120">Til dæmis er hægt að velja M0055 vöru.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="4e1c9-121">Fyrir hvern línueiginleika Uppskriftar, er hægt að velja hvort hún tekur fast gildi eða er varpað á eigind.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="4e1c9-122">Veljið gátreitinn stilla.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-122">Select the Set check box.</span></span>
4. <span data-ttu-id="4e1c9-123">Velja skal Já í Útreiknings reitnum.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="4e1c9-124">Útreikningur eiginleika er stillt á Já tryggir uppskriftarlínunni er með í útreikningi kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="4e1c9-125">Smellið á flipann „Setja upp“.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="4e1c9-126">Veljið gátreitinn stilla.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-126">Select the Set check box.</span></span>
7. <span data-ttu-id="4e1c9-127">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="4e1c9-128">Magn svæðið ákvarðar hversu mikið vörunnar sem verða innifalin í Uppskriftinni.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="4e1c9-129">Þetta gæti verið að augljós umsækjanda fyrir eigindarvörpun.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="4e1c9-130">Smellt er á víddaflipann.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="4e1c9-131">Staðfesta ef einhver afurðarvíddum eru virk og þess vegna verður að hafa gildi eða eigind sem er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="4e1c9-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="4e1c9-132">Click OK.</span></span>


