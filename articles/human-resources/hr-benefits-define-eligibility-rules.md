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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Version 7.0.0, Human Resources
ms.openlocfilehash: df517e1ab72634cb434411fab3bd92bf34c7e609
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5805947"
---
# <a name="define-benefit-eligibility-rules-and-policies"></a><span data-ttu-id="88633-103">Skilgreina reglur og stefnur um hæfi til fríðinda</span><span class="sxs-lookup"><span data-stu-id="88633-103">Define benefit eligibility rules and policies</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="88633-104">Þetta efnisatriði sýnir hvernig hægt er að stofna hæfnisreglur fríðinda og stefnur og síðan úthluta reglum á fríðindi.</span><span class="sxs-lookup"><span data-stu-id="88633-104">This topic shows you how you can create benefit eligibility rules and policies and then assign rules to benefits.</span></span>  

## <a name="create-benefit-eligibility-policy-rule-type"></a><span data-ttu-id="88633-105">Stofna Stefnureglugerðir um hæfni til fríðinda</span><span class="sxs-lookup"><span data-stu-id="88633-105">Create benefit eligibility policy rule type</span></span>

1. <span data-ttu-id="88633-106">Farið í **Mannauður > Fríðindi > Hæfi > Fríðindi hæfi stefnureglugerðir**.</span><span class="sxs-lookup"><span data-stu-id="88633-106">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policy rule types**.</span></span>
2. <span data-ttu-id="88633-107">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="88633-107">Select **New**.</span></span>
3. <span data-ttu-id="88633-108">Í reitinn **Heiti reglu** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="88633-108">In the **Rule name** field, enter a value.</span></span>
4. <span data-ttu-id="88633-109">Sláið inn gildi í reitnum **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="88633-109">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="88633-110">Í reitnum **Heiti fyrirspurnar** skal velja fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="88633-110">In the **Query name** field, select the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="88633-111">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="88633-111">In the list, select the link in the selected row.</span></span>
7. <span data-ttu-id="88633-112">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="88633-112">Select **Save**.</span></span>
8. <span data-ttu-id="88633-113">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="88633-113">Close the page.</span></span>

## <a name="benefit-eligibility-policy"></a><span data-ttu-id="88633-114">Regla um hæfni til fríðinda</span><span class="sxs-lookup"><span data-stu-id="88633-114">Benefit eligibility policy</span></span>

1. <span data-ttu-id="88633-115">Farið í **Mannauður > Fríðindi > Hæfi > Fríðindi hæfi stefnur**.</span><span class="sxs-lookup"><span data-stu-id="88633-115">Go to **Human resources > Benefits > Eligibility > Benefit eligibility policies**.</span></span>
2. <span data-ttu-id="88633-116">Veljið fyrirliggjandi stefmireglu fríðinda.</span><span class="sxs-lookup"><span data-stu-id="88633-116">Select an existing benefit policy.</span></span>
3. <span data-ttu-id="88633-117">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="88633-117">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="88633-118">Víxla útvíkkun hluta **fyrirtækisreglu**.</span><span class="sxs-lookup"><span data-stu-id="88633-118">Toggle the expansion of the **Policy organizations** sections.</span></span> <span data-ttu-id="88633-119">Hægt er að bæta við eða fjarlægja hvaða fyrirtæki sem á að taka með í reglunni.</span><span class="sxs-lookup"><span data-stu-id="88633-119">You can add or remove any organizations you want to include in the policy.</span></span>
5. <span data-ttu-id="88633-120">Útvíkka eða draga saman hlutann **stefnuregla**.</span><span class="sxs-lookup"><span data-stu-id="88633-120">Expand or collapse the **Policy rules** section.</span></span>
6. <span data-ttu-id="88633-121">Finna reglu sem áður hafa verið stofnaðar í listanum.</span><span class="sxs-lookup"><span data-stu-id="88633-121">In the list, find the policy rule previously created.</span></span>
7. <span data-ttu-id="88633-122">Veldu **stefnureglu**.</span><span class="sxs-lookup"><span data-stu-id="88633-122">Select **Create policy rule**.</span></span>
8. <span data-ttu-id="88633-123">Færið inn dagsetninguna sem reglan á að taka gildi í svæðinu **gildisdagsetningu**.</span><span class="sxs-lookup"><span data-stu-id="88633-123">In the **Effective date** field, enter the date in which you want the policy to become effective.</span></span>
    * <span data-ttu-id="88633-124">Að stilla virkar lokadagsetningar gerir kleift að gera breytingar síðar á stefnureglum þannig að ekki þurfi að fara aftur í regluna þegar ætlunin er að þessar breytingar taki gildi.</span><span class="sxs-lookup"><span data-stu-id="88633-124">Setting effective end dates allows you to make future changes to policy rules so you don't need to come back to the policy when you want those changes to take effect.</span></span>  
9. <span data-ttu-id="88633-125">Ef þörf krefur skal bæta where-klausu við reitinn **Bæta við skilyrði**.</span><span class="sxs-lookup"><span data-stu-id="88633-125">If needed, add a where clause to the **Add condition** field.</span></span>
    * <span data-ttu-id="88633-126">Til dæmi ef reglan eiga aðeins við sölustjóra er hægt að stofna Hvar klausunni til að segja: þar sem stöðulýsing jafngildir Sölustjóri.</span><span class="sxs-lookup"><span data-stu-id="88633-126">For example if you wanted the rule to only apply to Sales Managers you could create the where clause to say: Where position description equals Sales Manager.</span></span> <span data-ttu-id="88633-127">Hægt er að bæta mörgum where-skipunum saman í reglunni.</span><span class="sxs-lookup"><span data-stu-id="88633-127">You can add multiple where statements together in the rule.</span></span>  
10. <span data-ttu-id="88633-128">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="88633-128">Select **OK**.</span></span>
11. <span data-ttu-id="88633-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="88633-129">Close the page.</span></span>

## <a name="assign-rule-to-benefit"></a><span data-ttu-id="88633-130">Úthluta regla fríðinda</span><span class="sxs-lookup"><span data-stu-id="88633-130">Assign rule to benefit</span></span>

1. <span data-ttu-id="88633-131">Farið í **Mannauður > Fríðindi > Fríðindi**.</span><span class="sxs-lookup"><span data-stu-id="88633-131">Go to **Human resources > Benefits > Benefits**.</span></span>
2. <span data-ttu-id="88633-132">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="88633-132">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="88633-133">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="88633-133">In the list, select the link in the selected row.</span></span>
4. <span data-ttu-id="88633-134">Útvíkka eða draga saman hlutann **hæfnisreglu** r.</span><span class="sxs-lookup"><span data-stu-id="88633-134">Expand or collapse the **Eligibility rules** section.</span></span>
5. <span data-ttu-id="88633-135">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="88633-135">Select **Edit**.</span></span>
6. <span data-ttu-id="88633-136">Í reitnum **Hæfi** skal velja reglu.</span><span class="sxs-lookup"><span data-stu-id="88633-136">In the **Eligibility** field, select the rule.</span></span>
7. <span data-ttu-id="88633-137">Í reitnum **Gerð reglu** skal velja regluna sem var verið að búa til.</span><span class="sxs-lookup"><span data-stu-id="88633-137">In the **Rule type** field, select the rule you previously created.</span></span>
9. <span data-ttu-id="88633-138">Í listanum skal velja tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="88633-138">In the list, select the link in the selected row.</span></span>
10. <span data-ttu-id="88633-139">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="88633-139">Select **Save**.</span></span>
11. <span data-ttu-id="88633-140">Lokaðu skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="88633-140">Close the form.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]