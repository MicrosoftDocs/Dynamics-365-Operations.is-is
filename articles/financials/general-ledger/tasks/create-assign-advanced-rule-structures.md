---
title: Stofna og úthluta ítarlegu regluskipulagi
description: Þessar verkefnaleiðbeiningar fara í gegnum stofnun og úthlutun ítarlegs regluskipulags á lykilskipulag.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: dd62254c20cf5d77677d03c7d7335fb793d7f5f2
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558907"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="9f707-103">Stofna og úthluta ítarlegu regluskipulagi</span><span class="sxs-lookup"><span data-stu-id="9f707-103">Create and assign advanced rule structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9f707-104">Þessar verkefnaleiðbeiningar fara í gegnum stofnun og úthlutun ítarlegs regluskipulags á lykilskipulag.</span><span class="sxs-lookup"><span data-stu-id="9f707-104">This task guide steps through creating and assigning an advanced rule structure to an account structure.</span></span> <span data-ttu-id="9f707-105">Þessi handbók notar sýnifyrirtækið USMF.</span><span class="sxs-lookup"><span data-stu-id="9f707-105">This guide uses the USMF demo company.</span></span>


## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="9f707-106">Stofna skipulag ítarlegrar reglu</span><span class="sxs-lookup"><span data-stu-id="9f707-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="9f707-107">Fara í Fjárhagur > Bókhaldslyklar > Skipulag > Ítarlegt regluskipulag.</span><span class="sxs-lookup"><span data-stu-id="9f707-107">Go to General ledger > Chart of accounts > Structures > Advanced rule structures.</span></span>
2. <span data-ttu-id="9f707-108">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9f707-108">Click New to open the drop dialog.</span></span>
3. <span data-ttu-id="9f707-109">Í svæðinu skipulag Ítarlegrar reglu, sláið inn nafn til að lýsa skipulagi reglu.</span><span class="sxs-lookup"><span data-stu-id="9f707-109">In the Advanced rule structure field, type a name to descritbe the rule structure.</span></span>
4. <span data-ttu-id="9f707-110">Í Í reitinn Lýsing skal slá inn gildi til að lýsa skipulaginu.</span><span class="sxs-lookup"><span data-stu-id="9f707-110">In the Description field, type a value to describe the structure.</span></span>
5. <span data-ttu-id="9f707-111">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="9f707-111">Click OK.</span></span>
6. <span data-ttu-id="9f707-112">Smellt er á Bæta við hluta.</span><span class="sxs-lookup"><span data-stu-id="9f707-112">Click Add segment.</span></span>
7. <span data-ttu-id="9f707-113">Í lista yfir liði skal velja fjárhagsvídd.</span><span class="sxs-lookup"><span data-stu-id="9f707-113">In the list of segments, select a financial dimension.</span></span>
    * <span data-ttu-id="9f707-114">Til dæmis Verslun.</span><span class="sxs-lookup"><span data-stu-id="9f707-114">For example, Store.</span></span>  
8. <span data-ttu-id="9f707-115">Smellt er á Bæta við hluta.</span><span class="sxs-lookup"><span data-stu-id="9f707-115">Click Add segment.</span></span>
9. <span data-ttu-id="9f707-116">Á listanum smellirðu á tengilinn í skipulagi ítarlegrar reglu til að skoða það.</span><span class="sxs-lookup"><span data-stu-id="9f707-116">In the list, click the link of the advanced rule structure to view it.</span></span>
10. <span data-ttu-id="9f707-117">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="9f707-117">Click Activate.</span></span>
11. <span data-ttu-id="9f707-118">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="9f707-118">Click Activate.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="9f707-119">Beita ítarlegu regluskipulagi á lykilskipulag</span><span class="sxs-lookup"><span data-stu-id="9f707-119">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="9f707-120">Lokaðu skjámyndinni.</span><span class="sxs-lookup"><span data-stu-id="9f707-120">Close the form.</span></span>
2. <span data-ttu-id="9f707-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9f707-121">Close the page.</span></span>
3. <span data-ttu-id="9f707-122">Fara í Fjárhagur > Bókhaldslyklar > Skipulag > Skilgreina lykilskipulag.</span><span class="sxs-lookup"><span data-stu-id="9f707-122">Go to General ledger > Chart of accounts > Structures > Configure account structures.</span></span>
4. <span data-ttu-id="9f707-123">Í listanum skal finna og velja það lykilskipulag sem á að beita ítarlegri reglu á.</span><span class="sxs-lookup"><span data-stu-id="9f707-123">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
5. <span data-ttu-id="9f707-124">Smellt er á heiti lykilskipulags til að opna það.</span><span class="sxs-lookup"><span data-stu-id="9f707-124">Click the name of the account structure to open it.</span></span>
6. <span data-ttu-id="9f707-125">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="9f707-125">Click Edit.</span></span>
    * <span data-ttu-id="9f707-126">Einnig er hægt að smella á Ítarlegar reglur og notandi er beðinn um að setja lykilskipulag í ham fyrir Drög.</span><span class="sxs-lookup"><span data-stu-id="9f707-126">You can also click Advanced rules and you will be prompted to put the account structure in Draft mode.</span></span>  
7. <span data-ttu-id="9f707-127">Smellt er á Ítarlegar reglur.</span><span class="sxs-lookup"><span data-stu-id="9f707-127">Click Advanced rules.</span></span>
8. <span data-ttu-id="9f707-128">Smellt er á Nýtt til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9f707-128">Click New to open the drop dialog.</span></span>
9. <span data-ttu-id="9f707-129">Í reitinn Ítarleg regla skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9f707-129">In the Advanced rule field, type a value.</span></span>
10. <span data-ttu-id="9f707-130">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9f707-130">In the Name field, type a value.</span></span>
11. <span data-ttu-id="9f707-131">Smellið á Stofna.</span><span class="sxs-lookup"><span data-stu-id="9f707-131">Click Create.</span></span>
12. <span data-ttu-id="9f707-132">Smelltu á Bæta við nýjum skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="9f707-132">Click Add new criteria.</span></span>
13. <span data-ttu-id="9f707-133">Í reitnum Hvar skal velja aðallykil eða fjárhagsvídd.</span><span class="sxs-lookup"><span data-stu-id="9f707-133">In the Where field, select main account or a financial dimension.</span></span>
14. <span data-ttu-id="9f707-134">Í reitnum Virknitákn skal velja valkost, eins og er á milli og tekur með.</span><span class="sxs-lookup"><span data-stu-id="9f707-134">In the Operator field, select an option, such as is between and includes.</span></span>
15. <span data-ttu-id="9f707-135">Í reitinn Gildi skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9f707-135">In the Value field, type a value.</span></span>
16. <span data-ttu-id="9f707-136">Í reitinn Til og með skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9f707-136">In the through field, type a value.</span></span>
17. <span data-ttu-id="9f707-137">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9f707-137">Click Add to open the drop dialog.</span></span>
18. <span data-ttu-id="9f707-138">Á listanum skal finna skipulag ítarlegrar reglu sem á að nota þegar þau skilyrði sem færð voru inn eru uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="9f707-138">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
19. <span data-ttu-id="9f707-139">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="9f707-139">Click Add.</span></span>
20. <span data-ttu-id="9f707-140">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9f707-140">Close the page.</span></span>
21. <span data-ttu-id="9f707-141">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="9f707-141">Click Activate.</span></span>
22. <span data-ttu-id="9f707-142">Smellið á Virkja.</span><span class="sxs-lookup"><span data-stu-id="9f707-142">Click Activate.</span></span>

