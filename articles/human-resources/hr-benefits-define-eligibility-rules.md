---
title: Skilgreina reglur og stefnur um hæfi til fríðinda
description: Þessi grein sýnir hvernig hægt er að stofna hæfnisreglur fríðinda og stefnur og síðan tengja reglur við Fríðindi.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: f46437fef342ab1a4e368063d8b74205ca8e8c05
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2020
ms.locfileid: "3430878"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="ceb20-103">Skilgreina reglur og stefnur um hæfi til fríðinda</span><span class="sxs-lookup"><span data-stu-id="ceb20-103">Define benefit eligibility rules and policies</span></span>

<span data-ttu-id="ceb20-104">Þessi grein sýnir hvernig hægt er að stofna hæfnisreglur fríðinda og stefnur og síðan tengja reglur við Fríðindi.</span><span class="sxs-lookup"><span data-stu-id="ceb20-104">This article shows you how you can create benefit eligibility rules and policies and then assign rules to Benefits.</span></span>  

<span data-ttu-id="ceb20-105">Gögn sýniútgáfu fyrirtækis sem er notað til að stofna þessa skráningu í USMF.</span><span class="sxs-lookup"><span data-stu-id="ceb20-105">The demo data company used to create this recording is USMF.</span></span>


## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="ceb20-106">Stofna Stefnureglugerðir um hæfni til fríðinda</span><span class="sxs-lookup"><span data-stu-id="ceb20-106">Create benefit eligibility policy rule type</span></span>
1. <span data-ttu-id="ceb20-107">Farið í Mannauður > Fríðindi > Hæfi > Fríðindi hæfi stefnureglugerðir.</span><span class="sxs-lookup"><span data-stu-id="ceb20-107">Go to Human resources > Benefits > Eligibility > Benefit eligibility policy rule types.</span></span>
2. <span data-ttu-id="ceb20-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="ceb20-108">Click New.</span></span>
3. <span data-ttu-id="ceb20-109">Í reitinn Nafn reglu skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ceb20-109">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="ceb20-110">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="ceb20-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ceb20-111">Í reitnum Heiti fyrirspurnar skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="ceb20-111">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="ceb20-112">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ceb20-112">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="ceb20-113">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="ceb20-113">Click Save.</span></span>
8. <span data-ttu-id="ceb20-114">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ceb20-114">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="ceb20-115">Regla um hæfni til fríðinda</span><span class="sxs-lookup"><span data-stu-id="ceb20-115">Benefit eligibility policy</span></span>
1. <span data-ttu-id="ceb20-116">Farið í Mannauður > Fríðindi > Hæfi > Fríðindi hæfi stefnur.</span><span class="sxs-lookup"><span data-stu-id="ceb20-116">Go to Human resources > Benefits > Eligibility > Benefit eligibility policies.</span></span>
2. <span data-ttu-id="ceb20-117">Veljið fyrirliggjandi stefmireglu fríðinda.</span><span class="sxs-lookup"><span data-stu-id="ceb20-117">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="ceb20-118">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ceb20-118">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ceb20-119">Víxla útvíkkun hluta fyrirtækisreglu.</span><span class="sxs-lookup"><span data-stu-id="ceb20-119">Toggle the expansion of the Policy organizations sections.</span></span>  <span data-ttu-id="ceb20-120">Hér er hægt að bæta við eða fjarlægja hvaða fyrirtæki sem á að taka með í reglunni.</span><span class="sxs-lookup"><span data-stu-id="ceb20-120">Here you can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="ceb20-121">Útvíkka eða draga saman hlutann stefnuregla.</span><span class="sxs-lookup"><span data-stu-id="ceb20-121">Expand or collapse the Policy rules section.</span></span>
6. <span data-ttu-id="ceb20-122">Finna reglu sem áður hafa verið stofnaðar í listanum.</span><span class="sxs-lookup"><span data-stu-id="ceb20-122">In the list find the policy rule previously created.</span></span>
7. <span data-ttu-id="ceb20-123">Smellt er á Stofna stefnureglu.</span><span class="sxs-lookup"><span data-stu-id="ceb20-123">Click Create policy rule.</span></span>
8. <span data-ttu-id="ceb20-124">Færið inn dagsetninguna sem reglan á að taka gildi í svæðinu gildisdagsetningu.</span><span class="sxs-lookup"><span data-stu-id="ceb20-124">In the Effective date field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="ceb20-125">Stilla virkar og lokadagsetningar gerir kleift að gera breytingar síðar á stefnureglur og fjarlægja þörfina á að koma aftur að þessari reglu þegar óskað er eftir að þessar breytingar taki gildi.</span><span class="sxs-lookup"><span data-stu-id="ceb20-125">Setting effective and end dates allows you to make future changes to policy rules and removing the need to come back to the policy when you want those changes to take effect.</span></span>  
9. 
    * <span data-ttu-id="ceb20-126">Til dæmi ef reglan eiga aðeins við sölustjóra er hægt að stofna Hvar klausunni til að segja: þar sem stöðulýsing jafngildir Sölustjóri .</span><span class="sxs-lookup"><span data-stu-id="ceb20-126">For example if you wanted the rule to only apply to Sales Managers you could create the Where clause to say: Where position description equals Sales Manager.</span></span>  <span data-ttu-id="ceb20-127">Hægt er að marfalda með Og Eða yrðingar saman í reglunni.</span><span class="sxs-lookup"><span data-stu-id="ceb20-127">You can And or Or multiple Where statements together in the rule.</span></span>  
10. <span data-ttu-id="ceb20-128">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ceb20-128">Click OK.</span></span>
11. <span data-ttu-id="ceb20-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ceb20-129">Close the page.</span></span>
12. <span data-ttu-id="ceb20-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ceb20-130">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="ceb20-131">Úthluta regla fríðinda</span><span class="sxs-lookup"><span data-stu-id="ceb20-131">Assign rule to benefit</span></span>
1. <span data-ttu-id="ceb20-132">Farið í Mannauður > Fríðindi > Fríðindi.</span><span class="sxs-lookup"><span data-stu-id="ceb20-132">Go to Human resources > Benefits > Benefits.</span></span>
2. <span data-ttu-id="ceb20-133">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="ceb20-133">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="ceb20-134">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ceb20-134">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="ceb20-135">Útvíkka eða draga saman hlutann hæfnisreglur.</span><span class="sxs-lookup"><span data-stu-id="ceb20-135">Expand or collapse the Eligibility rules section.</span></span>
5. <span data-ttu-id="ceb20-136">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="ceb20-136">Click Edit.</span></span>
6. <span data-ttu-id="ceb20-137">Velja Reglu sem byggð er á listanum í svæðinu Hæfni.</span><span class="sxs-lookup"><span data-stu-id="ceb20-137">In the Eligibility field, select Rule based from the list.</span></span>
7. <span data-ttu-id="ceb20-138">Í reitnum gerð reglu skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="ceb20-138">In the Rule type field, click the drop down button to open the lookup.</span></span>
8. <span data-ttu-id="ceb20-139">Finna og velja reglu sem áður hafa verið stofnaðar í listanum.</span><span class="sxs-lookup"><span data-stu-id="ceb20-139">In the list find and select the rule you previously created.</span></span>
9. <span data-ttu-id="ceb20-140">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="ceb20-140">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="ceb20-141">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="ceb20-141">Click Save.</span></span>
11. <span data-ttu-id="ceb20-142">Lokaðu skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="ceb20-142">Close the form.</span></span>

