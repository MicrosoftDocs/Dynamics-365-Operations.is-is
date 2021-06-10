---
title: Skilgreina reglur og stefnur um hæfi til fríðinda
description: Þessi grein sýnir hvernig hægt er að stofna hæfnisreglur fríðinda og stefnur og síðan tengja reglur við Fríðindi.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysPolicyListPage, SysPolicy, HcmBenefitEligibilityPolicy, HcmBenefit, BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: 046b045fbdda125c5a2259783c0347f687453528
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053154"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="7fbaa-103">Skilgreina reglur og stefnur um hæfi til fríðinda</span><span class="sxs-lookup"><span data-stu-id="7fbaa-103">Define benefit eligibility rules and policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7fbaa-104">Þetta efnisatriði sýnir hvernig hægt er að stofna hæfnisreglur fríðinda og stefnur og síðan úthluta reglum á fríðindi.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="7fbaa-105">Stofna Stefnureglugerðir um hæfni til fríðinda</span><span class="sxs-lookup"><span data-stu-id="7fbaa-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="7fbaa-106">Farið í **Mannauður > Fríðindi > Hæfi > Fríðindi hæfi stefnureglugerðir**.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="7fbaa-107">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-107">Select **New**.</span></span>
3. <span data-ttu-id="7fbaa-108">Í reitinn **Heiti reglu** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="7fbaa-109">Sláið inn gildi í reitnum **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="7fbaa-110">Í reitnum **Heiti fyrirspurnar** skal velja fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="7fbaa-111">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="7fbaa-112">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-112">Select **Save**.</span></span>
8. <span data-ttu-id="7fbaa-113">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="7fbaa-114">Regla um hæfni til fríðinda</span><span class="sxs-lookup"><span data-stu-id="7fbaa-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="7fbaa-115">Farið í **Mannauður > Fríðindi > Hæfi > Fríðindi hæfi stefnur**.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="7fbaa-116">Veljið fyrirliggjandi stefmireglu fríðinda.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="7fbaa-117">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="7fbaa-118">Víxla útvíkkun hluta **fyrirtækisreglu**.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="7fbaa-119">Hægt er að bæta við eða fjarlægja hvaða fyrirtæki sem á að taka með í reglunni.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="7fbaa-120">Útvíkka eða draga saman hlutann **stefnuregla**.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="7fbaa-121">Finna reglu sem áður hafa verið stofnaðar í listanum.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="7fbaa-122">Veldu **stefnureglu**.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="7fbaa-123">Færið inn dagsetninguna sem reglan á að taka gildi í svæðinu **gildisdagsetningu**.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="7fbaa-124">Að stilla virkar lokadagsetningar gerir kleift að gera breytingar síðar á stefnureglum þannig að ekki þurfi að fara aftur í regluna þegar ætlunin er að þessar breytingar taki gildi.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="7fbaa-125">Ef þörf krefur skal bæta where-klausu við reitinn **Bæta við skilyrði**.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="7fbaa-126">Til dæmi ef reglan eiga aðeins við sölustjóra er hægt að stofna Hvar klausunni til að segja: þar sem stöðulýsing jafngildir Sölustjóri.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="7fbaa-127">Hægt er að bæta mörgum where-skipunum saman í reglunni.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="7fbaa-128">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-128">Select **OK**.</span></span>
11. <span data-ttu-id="7fbaa-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="7fbaa-130">Úthluta regla fríðinda</span><span class="sxs-lookup"><span data-stu-id="7fbaa-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="7fbaa-131">Farið í **Mannauður > Fríðindi > Fríðindi**.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="7fbaa-132">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="7fbaa-133">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="7fbaa-134">Útvíkka eða draga saman hlutann **hæfnisreglur**.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="7fbaa-135">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-135">Select **Edit**.</span></span>
6. <span data-ttu-id="7fbaa-136">Í reitnum **Hæfi** skal velja reglu.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="7fbaa-137">Í reitnum **Gerð reglu** skal velja regluna sem var verið að búa til.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="7fbaa-138">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="7fbaa-139">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-139">Select **Save**.</span></span>
11. <span data-ttu-id="7fbaa-140">Lokaðu skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="7fbaa-140">Close the form.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]