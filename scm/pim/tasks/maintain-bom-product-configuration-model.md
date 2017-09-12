--- 
title: "Vinna með uppskrift fyrir afbrigðalíkan afurðar"
description: "Keyra þetta ferli krefst fyrirliggjandi skilgreiningu afbrigðalíkan afurðar."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 380e902f9c8266f583e44fa7ea643dc5d5ab52d3
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="maintain-bom-for-a-product-configuration-model"></a><span data-ttu-id="70090-103">Vinna með uppskrift fyrir afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="70090-103">Maintain BOM for a product configuration model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="70090-104">Keyra þetta ferli krefst fyrirliggjandi skilgreiningu afbrigðalíkan afurðar.</span><span class="sxs-lookup"><span data-stu-id="70090-104">Running this procedure requires an existing product configuration model.</span></span> <span data-ttu-id="70090-105">Hágæða hátalara líkan í fyrirtækinu sýnigögn USMF er notað til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="70090-105">The High end speaker model in the demo company USMF is used to create this procedure.</span></span>


## <a name="add-a-bom-line"></a><span data-ttu-id="70090-106">Bæta við uppskriftarlína</span><span class="sxs-lookup"><span data-stu-id="70090-106">Add a BOM line</span></span>
1. <span data-ttu-id="70090-107">Smellið á Skilgreining afurðarafbrigðislíkans</span><span class="sxs-lookup"><span data-stu-id="70090-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="70090-108">Smella á Afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="70090-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="70090-109">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="70090-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="70090-110">Veljið hágæða hátalara fyrir þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="70090-110">Select the High end speaker for this procedure.</span></span>  
4. <span data-ttu-id="70090-111">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="70090-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="70090-112">Stækka hlutann uppskriftarlínunum.</span><span class="sxs-lookup"><span data-stu-id="70090-112">Expand the BOM lines section.</span></span>
6. <span data-ttu-id="70090-113">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="70090-113">Click Add.</span></span>
7. <span data-ttu-id="70090-114">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="70090-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="70090-115">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="70090-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="70090-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="70090-116">Click Save.</span></span>

## <a name="add-bom-line-details"></a><span data-ttu-id="70090-117">Bæta við uppskriftarlínuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="70090-117">Add BOM line details</span></span>
1. <span data-ttu-id="70090-118">Smellt er á uppskriftarlínuupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="70090-118">Click BOM line details.</span></span>
2. <span data-ttu-id="70090-119">Í reitinn Vörunúmer skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="70090-119">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="70090-120">Til dæmis er hægt að velja M0055 vöru.</span><span class="sxs-lookup"><span data-stu-id="70090-120">For example, you can select the item M0055.</span></span>  
    * <span data-ttu-id="70090-121">Fyrir hvern línueiginleika Uppskriftar, er hægt að velja hvort hún tekur fast gildi eða er varpað á eigind.</span><span class="sxs-lookup"><span data-stu-id="70090-121">For each BOM line property, you can select if it takes a fixed value or is mapped to an attribute.</span></span>  
3. <span data-ttu-id="70090-122">Veljið gátreitinn stilla.</span><span class="sxs-lookup"><span data-stu-id="70090-122">Select the Set check box.</span></span>
4. <span data-ttu-id="70090-123">Velja skal Já í Útreiknings reitnum.</span><span class="sxs-lookup"><span data-stu-id="70090-123">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="70090-124">Útreikningur eiginleika er stillt á Já tryggir uppskriftarlínunni er með í útreikningi kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="70090-124">Setting the Calculation property to Yes ensures that the BOM line is included in cost calculations.</span></span>  
5. <span data-ttu-id="70090-125">Smellið á flipann „Setja upp“.</span><span class="sxs-lookup"><span data-stu-id="70090-125">Click the Setup tab.</span></span>
6. <span data-ttu-id="70090-126">Veljið gátreitinn stilla.</span><span class="sxs-lookup"><span data-stu-id="70090-126">Select the Set check box.</span></span>
7. <span data-ttu-id="70090-127">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="70090-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="70090-128">Magn svæðið ákvarðar hversu mikið vörunnar sem verða innifalin í Uppskriftinni.</span><span class="sxs-lookup"><span data-stu-id="70090-128">The quantity field determines how much of the item that will be included in the BOM.</span></span> <span data-ttu-id="70090-129">Þetta gæti verið að augljós umsækjanda fyrir eigindarvörpun.</span><span class="sxs-lookup"><span data-stu-id="70090-129">This could be an obvious candidate for an attribute mapping.</span></span>  
8. <span data-ttu-id="70090-130">Smellt er á víddaflipann.</span><span class="sxs-lookup"><span data-stu-id="70090-130">Click the Dimension tab.</span></span>
    * <span data-ttu-id="70090-131">Staðfesta ef einhver afurðarvíddum eru virk og þess vegna verður að hafa gildi eða eigind sem er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="70090-131">Verify if any of the product dimensions are active,  and therefore must have a value or attribute assigned.</span></span>  
9. <span data-ttu-id="70090-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="70090-132">Click OK.</span></span>


