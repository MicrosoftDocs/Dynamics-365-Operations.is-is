--- 
title: "Mynda áætlun með skorðum"
description: "Þessi verklýsing sýnir hvernig á að stofna áætlun sen tekur tillit bæði til efnis- og afkastahamla."
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
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9deb615d05b90865ea6a050599bf91879b5688d0
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="f79ac-103">Mynda áætlun með skorðum</span><span class="sxs-lookup"><span data-stu-id="f79ac-103">Generate a constrained plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f79ac-104">Þessi verklýsing sýnir hvernig á að stofna áætlun sen tekur tillit bæði til efnis- og afkastahamla.</span><span class="sxs-lookup"><span data-stu-id="f79ac-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="f79ac-105">Áætlunin tryggir að framleiðslu hefst ekki fyrr en efni sé tiltækt og tilföng eru ekki yfirbókaður.</span><span class="sxs-lookup"><span data-stu-id="f79ac-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="f79ac-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="f79ac-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="f79ac-107">Þetta ferli er ætluð fyrir framleiðslustjóri</span><span class="sxs-lookup"><span data-stu-id="f79ac-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="f79ac-108">Setja upp áætlun með skorðum</span><span class="sxs-lookup"><span data-stu-id="f79ac-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="f79ac-109">Smellt er á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="f79ac-109">Click Master planning.</span></span>
2. <span data-ttu-id="f79ac-110">Smellt er á aðaláætlanir.</span><span class="sxs-lookup"><span data-stu-id="f79ac-110">Click Master plans.</span></span>
3. <span data-ttu-id="f79ac-111">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="f79ac-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="f79ac-112">Dæmi: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="f79ac-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="f79ac-113">Veljið Já í svæðinu takmörkuð Afkastageta.</span><span class="sxs-lookup"><span data-stu-id="f79ac-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="f79ac-114">Í reitnum Tímamörk takmarkað afkastaveita skal slá inn ‚30‘.</span><span class="sxs-lookup"><span data-stu-id="f79ac-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="f79ac-115">Víkka út hlutann tímamörk í dögum.</span><span class="sxs-lookup"><span data-stu-id="f79ac-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="f79ac-116">Veljið Já í svæðinu Afkastageta.</span><span class="sxs-lookup"><span data-stu-id="f79ac-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="f79ac-117">Í reitinn Tímamörk áætlaðrar afkastagetu slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f79ac-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="f79ac-118">Dæmi: 60</span><span class="sxs-lookup"><span data-stu-id="f79ac-118">Example: 60</span></span>  
9. <span data-ttu-id="f79ac-119">Veljið Já í Reiknaðar seinkanir reitnum.</span><span class="sxs-lookup"><span data-stu-id="f79ac-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="f79ac-120">Í reitinn Tímamörk útreiknaðra seinkana (dagar) skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f79ac-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="f79ac-121">Dæmi: 60</span><span class="sxs-lookup"><span data-stu-id="f79ac-121">Example: 60</span></span>  
11. <span data-ttu-id="f79ac-122">Útvíkka hlutann Reiknuð seinkanir.</span><span class="sxs-lookup"><span data-stu-id="f79ac-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="f79ac-123">Veldu Já í reitnum Bæta við reiknaðri seinkun á dagsetningu þarfa</span><span class="sxs-lookup"><span data-stu-id="f79ac-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="f79ac-124">Veldu Já í reitnum Bæta við reiknaðri seinkun á dagsetningu þarfa</span><span class="sxs-lookup"><span data-stu-id="f79ac-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="f79ac-125">Veldu Já í reitnum Bæta við reiknaðri seinkun á dagsetningu þarfa</span><span class="sxs-lookup"><span data-stu-id="f79ac-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="f79ac-126">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f79ac-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="f79ac-127">Stofna áætlun með skorðum</span><span class="sxs-lookup"><span data-stu-id="f79ac-127">Create a constrained plan</span></span>
1. <span data-ttu-id="f79ac-128">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="f79ac-128">Click Run.</span></span>
2. <span data-ttu-id="f79ac-129">Færa inn eða veljið gildi í svæðinu Aðaláætlun.</span><span class="sxs-lookup"><span data-stu-id="f79ac-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="f79ac-130">Velja áætlunina sem settar voru upp skorður fyrir.</span><span class="sxs-lookup"><span data-stu-id="f79ac-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="f79ac-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f79ac-131">Click OK.</span></span>
    * <span data-ttu-id="f79ac-132">Þetta gæti tekið nokkra stund.</span><span class="sxs-lookup"><span data-stu-id="f79ac-132">This may take a while.</span></span>  
4. <span data-ttu-id="f79ac-133">Smellt er á Áætlaðar pantanir.</span><span class="sxs-lookup"><span data-stu-id="f79ac-133">Click Planned orders.</span></span>


