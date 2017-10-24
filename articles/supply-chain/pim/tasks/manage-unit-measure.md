--- 
title: "Stjórna mælieiningu"
description: "Þessi ferli sýnir hvernig á að skilgreina mælieiningu, veita þýðingar fyrir eininguna og lýsingu hennar, og skilgreina umreikningsreglur fyrir tengdar einingar."
author: sorenva
manager: AnnBe
ms.date: 02/12/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6bb7a5133e9412f4ed6fb74f0d3ee595c07a0c4b
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="manage-unit-of-measure"></a><span data-ttu-id="f558a-103">Stjórna mælieiningu</span><span class="sxs-lookup"><span data-stu-id="f558a-103">Manage unit of measure</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f558a-104">Þessi ferli sýnir hvernig á að skilgreina mælieiningu, veita þýðingar fyrir eininguna og lýsingu hennar, og skilgreina umreikningsreglur fyrir tengdar einingar.</span><span class="sxs-lookup"><span data-stu-id="f558a-104">This procedure shows how to define a unit of measure, provide translations for the unit and it's description, and define conversion rules for related units.</span></span> <span data-ttu-id="f558a-105">Hægt er að fara í gegnum þetta ferli með því að nota sýnigögn eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="f558a-105">You can walk through this procedure using demo data, or using your own data.</span></span>

1. <span data-ttu-id="f558a-106">Farðu í Viðhald útgefinnar afurðar.</span><span class="sxs-lookup"><span data-stu-id="f558a-106">Go to Released product maintenance.</span></span>
2. <span data-ttu-id="f558a-107">Smellt er á Einingum.</span><span class="sxs-lookup"><span data-stu-id="f558a-107">Click Units.</span></span>

## <a name="create-a-unit-of-measure"></a><span data-ttu-id="f558a-108">Stofna mælieiningu</span><span class="sxs-lookup"><span data-stu-id="f558a-108">Create a unit of measure</span></span>
1. <span data-ttu-id="f558a-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f558a-109">Click New.</span></span>
2. <span data-ttu-id="f558a-110">Í reitnum Eining skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f558a-110">In the Unit field, type a value.</span></span>
    * <span data-ttu-id="f558a-111">Færið inn Kenni eða tákn sem nota á þegar vísað er í mælieiningu.</span><span class="sxs-lookup"><span data-stu-id="f558a-111">Enter the ID or symbol to use when referring to the unit of measure.</span></span>  
3. <span data-ttu-id="f558a-112">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="f558a-112">In the Description field, type a value.</span></span>
    * <span data-ttu-id="f558a-113">Færið inn lýsandi heiti fyrir mælieiningu á tungumáli kerfisins.</span><span class="sxs-lookup"><span data-stu-id="f558a-113">Enter a descriptive name for the unit of measure in the system language.</span></span>  
4. <span data-ttu-id="f558a-114">Í reitnum Einingaflokkur skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="f558a-114">In the Unit class field, select an option.</span></span>
    * <span data-ttu-id="f558a-115">Mælieiningaflokkurinn skilgreinir hvaða röklegu flokkun, eins og svæði, fjöldi eða magni, mælieiningin er hluti af.</span><span class="sxs-lookup"><span data-stu-id="f558a-115">The unit class defines what logical grouping, such as area, mass, or quantity, the unit of measure is part of.</span></span>  
5. <span data-ttu-id="f558a-116">Í reitinn Nákvæmni aukastafa skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f558a-116">In the Decimal precision field, enter a number.</span></span>
    * <span data-ttu-id="f558a-117">Tilgreina fjölda aukastafa sem verður að slétta umreiknaðar mælieiningu í þegar útreikningi er lokið fyrir mælieiningu.</span><span class="sxs-lookup"><span data-stu-id="f558a-117">Specify the number of decimals that the converted unit of measure must be rounded to when a calculation is completed for the unit of measure.</span></span>  
6. <span data-ttu-id="f558a-118">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f558a-118">Click Save.</span></span>

## <a name="define-unit-translations"></a><span data-ttu-id="f558a-119">Skilgreina þýðingar eininga</span><span class="sxs-lookup"><span data-stu-id="f558a-119">Define unit translations</span></span>
1. <span data-ttu-id="f558a-120">Smellt er á einingatexti.</span><span class="sxs-lookup"><span data-stu-id="f558a-120">Click Unit texts.</span></span>
2. <span data-ttu-id="f558a-121">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f558a-121">Click New.</span></span>
    * <span data-ttu-id="f558a-122">Einingatexti skal nota til að stofna þýðing fyrir Kenni eða tákn sem standa fyrir mælieiningu sem nota á á ytri skjöl í tungumálum fyrir viðskiptavin eða lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="f558a-122">Use unit text to create a translation of the ID or a symbol representing the unit of measure for use on external documents in customer- or vendor-specific languages.</span></span>  
3. <span data-ttu-id="f558a-123">Í reitnum Tungumál skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="f558a-123">In the Language field, enter or select a value.</span></span>
4. <span data-ttu-id="f558a-124">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f558a-124">In the Text field, type a value.</span></span>
5. <span data-ttu-id="f558a-125">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f558a-125">Click Save.</span></span>
6. <span data-ttu-id="f558a-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f558a-126">Close the page.</span></span>
7. <span data-ttu-id="f558a-127">Smellt er á Þýddar einingalýsingar.</span><span class="sxs-lookup"><span data-stu-id="f558a-127">Click Translated unit descriptions.</span></span>
8. <span data-ttu-id="f558a-128">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f558a-128">Click New.</span></span>
    * <span data-ttu-id="f558a-129">Skilgreina lýsingar fyrir tiltekin tungumál fyrir mælieiningu.</span><span class="sxs-lookup"><span data-stu-id="f558a-129">Define language-specific descriptions for the unit of measure.</span></span>  
9. <span data-ttu-id="f558a-130">Í reitnum Tungumál skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="f558a-130">In the Language field, enter or select a value.</span></span>
10. <span data-ttu-id="f558a-131">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="f558a-131">In the Description field, type a value.</span></span>
11. <span data-ttu-id="f558a-132">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f558a-132">Click Save.</span></span>
12. <span data-ttu-id="f558a-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f558a-133">Close the page.</span></span>

## <a name="define-unit-conversion-rules"></a><span data-ttu-id="f558a-134">Skilgreina umreikningsreglur eininga</span><span class="sxs-lookup"><span data-stu-id="f558a-134">Define unit conversion rules</span></span>
1. <span data-ttu-id="f558a-135">Smellt er á Umreikningur eininga.</span><span class="sxs-lookup"><span data-stu-id="f558a-135">Click Unit conversions.</span></span>
    * <span data-ttu-id="f558a-136">Skilgreina reglur til að umreikna mælieininguna í og frá öðrum mælieiningar í völdu einingaflokknum.</span><span class="sxs-lookup"><span data-stu-id="f558a-136">Define rules for converting the unit of measure to and from other units of measure in the selected unit class.</span></span>  
2. <span data-ttu-id="f558a-137">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="f558a-137">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="f558a-138">Í reitnum Stuðull skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="f558a-138">In the Factor field, enter a number.</span></span>
    * <span data-ttu-id="f558a-139">Umreiknistuðull milli Frá einingu og Til einingar.</span><span class="sxs-lookup"><span data-stu-id="f558a-139">Conversion factor between the From unit and the To unit.</span></span> <span data-ttu-id="f558a-140">til dæmis er umreiknistuðullinn úr sentímetrum í metra 100 þar sem 100 sentímetrar eru í einum metra.</span><span class="sxs-lookup"><span data-stu-id="f558a-140">For example, the conversion factor from centimeter to meter is 100 because there are 100 centimeters in one meter.</span></span>  
4. <span data-ttu-id="f558a-141">Í reitnum Til einingar skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="f558a-141">In the To unit field, enter or select a value.</span></span>
5. <span data-ttu-id="f558a-142">Í reitnum Sléttun skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="f558a-142">In the Rounding field, select an option.</span></span>
    * <span data-ttu-id="f558a-143">Skilgreina hvernig slétta skal umbreytt gildi.</span><span class="sxs-lookup"><span data-stu-id="f558a-143">Define how the converted value should be rounded.</span></span>  
6. <span data-ttu-id="f558a-144">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f558a-144">Click OK.</span></span>
7. <span data-ttu-id="f558a-145">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f558a-145">Close the page.</span></span>


