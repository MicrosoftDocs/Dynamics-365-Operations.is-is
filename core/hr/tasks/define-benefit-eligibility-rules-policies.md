--- 
# required metadata 
title: Skilgreina reglur og stefnur um hæfi til fríðinda
description: Þessi skráning sýnir hvernig hægt er að stofna hæfnisreglur fríðinda og stefnur og síðan tengja reglur við Fríðindi.
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: null
ms.service: dynamics-ax-applications
ms.technology: null
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: '2016-06-30'
ms.dyn365.ops.version: AX 7.0.0
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="22fe5-103">Skilgreina reglur og stefnur um hæfi til fríðinda</span><span class="sxs-lookup"><span data-stu-id="22fe5-103">Define benefit eligibility rules and policies</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22fe5-104">Þessi skráning sýnir hvernig hægt er að stofna hæfnisreglur fríðinda og stefnur og síðan tengja reglur við Fríðindi.</span><span class="sxs-lookup"><span data-stu-id="22fe5-104">This recording will show you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="22fe5-105">Gögn sýniútgáfu fyrirtækis sem er notað til að stofna þessa skráningu í USMF.</span><span class="sxs-lookup"><span data-stu-id="22fe5-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="22fe5-106">Stofna Stefnureglugerðir um hæfni til fríðinda</span><span class="sxs-lookup"><span data-stu-id="22fe5-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="22fe5-107">Farið í Mannauður > Fríðindi > Hæfi > Fríðindi hæfi stefnureglugerðir.</span><span class="sxs-lookup"><span data-stu-id="22fe5-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="22fe5-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="22fe5-108">Click New.</span></span>
3. <span data-ttu-id="22fe5-109">Í reitinn Nafn reglu skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="22fe5-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="22fe5-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="22fe5-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="22fe5-111">Í reitnum Heiti fyrirspurnar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="22fe5-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="22fe5-112">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="22fe5-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="22fe5-113">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="22fe5-113">Click Save.</span></span>
8. <span data-ttu-id="22fe5-114">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="22fe5-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="22fe5-115">Regla um hæfni til fríðinda</span><span class="sxs-lookup"><span data-stu-id="22fe5-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="22fe5-116">Farið í Mannauður > Fríðindi > Hæfi > Fríðindi hæfi stefnur.</span><span class="sxs-lookup"><span data-stu-id="22fe5-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="22fe5-117">Veljið fyrirliggjandi stefmireglu fríðinda.</span><span class="sxs-lookup"><span data-stu-id="22fe5-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="22fe5-118">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="22fe5-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="22fe5-119">Víxla útvíkkun hluta fyrirtækisreglu.</span><span class="sxs-lookup"><span data-stu-id="22fe5-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="22fe5-120">Hér er hægt að bæta við eða fjarlægja hvaða fyrirtæki sem á að taka með í reglunni.</span><span class="sxs-lookup"><span data-stu-id="22fe5-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="22fe5-121">Útvíkka eða draga saman hlutann stefnuregla.</span><span class="sxs-lookup"><span data-stu-id="22fe5-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="22fe5-122">Finna reglu sem áður hafa verið stofnaðar í listanum.</span><span class="sxs-lookup"><span data-stu-id="22fe5-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="22fe5-123">Smellt er á Stofna stefnureglu.</span><span class="sxs-lookup"><span data-stu-id="22fe5-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="22fe5-124">Færið inn dagsetninguna sem reglan á að taka gildi í svæðinu gildisdagsetningu.</span><span class="sxs-lookup"><span data-stu-id="22fe5-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="22fe5-125">Stilla virkar og lokadagsetningar gerir kleift að gera breytingar síðar á stefnureglur og fjarlægja þörfina á að koma aftur að þessari reglu þegar óskað er eftir að þessar breytingar taki gildi.</span><span class="sxs-lookup"><span data-stu-id="22fe5-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="22fe5-126">Til dæmi ef reglan eiga aðeins við sölustjóra er hægt að stofna Hvar klausunni til að segja: þar sem stöðulýsing jafngildir Sölustjóri .</span><span class="sxs-lookup"><span data-stu-id="22fe5-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="22fe5-127">Hægt er að marfalda með Og Eða yrðingar saman í reglunni.</span><span class="sxs-lookup"><span data-stu-id="22fe5-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="22fe5-128">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="22fe5-128">Click OK.</span></span>
11. <span data-ttu-id="22fe5-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="22fe5-129">Close the page.</span></span>
12. <span data-ttu-id="22fe5-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="22fe5-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="22fe5-131">Úthluta regla fríðinda</span><span class="sxs-lookup"><span data-stu-id="22fe5-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="22fe5-132">Farið í Mannauður > Fríðindi > Fríðindi.</span><span class="sxs-lookup"><span data-stu-id="22fe5-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="22fe5-133">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="22fe5-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="22fe5-134">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="22fe5-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="22fe5-135">Útvíkka eða draga saman hlutann hæfnisreglur.</span><span class="sxs-lookup"><span data-stu-id="22fe5-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="22fe5-136">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="22fe5-136">Click Edit.</span></span>
6. <span data-ttu-id="22fe5-137">Velja Reglu sem byggð er á listanum í svæðinu Hæfni.</span><span class="sxs-lookup"><span data-stu-id="22fe5-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="22fe5-138">Í reitnum gerð reglu skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="22fe5-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="22fe5-139">Finna og velja reglu sem áður hafa verið stofnaðar í listanum.</span><span class="sxs-lookup"><span data-stu-id="22fe5-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="22fe5-140">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="22fe5-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="22fe5-141">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="22fe5-141">Click Save.</span></span>
11. <span data-ttu-id="22fe5-142">Lokaðu skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="22fe5-142">Close the form.</span></span>

