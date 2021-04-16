---
title: Stofna og úthluta ítarlegu regluskipulagi
description: Þetta efni útskýrir hvernig á að stofna og úthluta ítarlegri reglusamsetningu við reikningsskipulag.
author: aprilolson
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b81e3cc169bf0164af0b9c4de4faeb936df6784
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837058"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="b0f11-103">Stofna og úthluta ítarlegu regluskipulagi</span><span class="sxs-lookup"><span data-stu-id="b0f11-103">Create and assign advanced rule structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b0f11-104">Þetta efni útskýrir hvernig á að stofna og úthluta ítarlegri reglusamsetningu við reikningsskipulag.</span><span class="sxs-lookup"><span data-stu-id="b0f11-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="b0f11-105">Þessi handbók notar sýnifyrirtækið USMF.</span><span class="sxs-lookup"><span data-stu-id="b0f11-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="b0f11-106">Stofna skipulag ítarlegrar reglu</span><span class="sxs-lookup"><span data-stu-id="b0f11-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="b0f11-107">Farðu í **Skoðunarrúðu > Kerfi > Fjárhagur > Bókhaldslykill > Skipulag > Ítarlegt regluskipulag**.</span><span class="sxs-lookup"><span data-stu-id="b0f11-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="b0f11-108">Veldu **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b0f11-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="b0f11-109">Í reitnum **Ítarlegt regluskipulag** slærðu inn heiti til að lýsa regluskipulaginu.</span><span class="sxs-lookup"><span data-stu-id="b0f11-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="b0f11-110">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b0f11-110">Select **OK**.</span></span>
5. <span data-ttu-id="b0f11-111">Veldu **Bæta við hluta**.</span><span class="sxs-lookup"><span data-stu-id="b0f11-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="b0f11-112">Í lista yfir liði skal velja fjárhagsvídd.</span><span class="sxs-lookup"><span data-stu-id="b0f11-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="b0f11-113">Til dæmis **Verslun**.</span><span class="sxs-lookup"><span data-stu-id="b0f11-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="b0f11-114">Veldu **Bæta við hluta**.</span><span class="sxs-lookup"><span data-stu-id="b0f11-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="b0f11-115">Veldu **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="b0f11-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="b0f11-116">Beita ítarlegu regluskipulagi á lykilskipulag</span><span class="sxs-lookup"><span data-stu-id="b0f11-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="b0f11-117">Farðu í **Skoðunarrúðu > Kerfi > Fjárhagur > Bókhaldslykill > Skipulag > Skilgreina lykilskipulög**.</span><span class="sxs-lookup"><span data-stu-id="b0f11-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="b0f11-118">Í listanum skal finna og velja það lykilskipulag sem á að beita ítarlegri reglu á.</span><span class="sxs-lookup"><span data-stu-id="b0f11-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="b0f11-119">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="b0f11-119">Select **Edit**.</span></span> <span data-ttu-id="b0f11-120">Einnig er hægt að velja **Ítarlegar reglur** og notandi er beðinn um að setja lykilskipulag inn í **Drög**.</span><span class="sxs-lookup"><span data-stu-id="b0f11-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="b0f11-121">Veldu **Ítarlegar reglur**.</span><span class="sxs-lookup"><span data-stu-id="b0f11-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="b0f11-122">Veldu **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b0f11-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="b0f11-123">Í reitinn **Ítarleg regla** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b0f11-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="b0f11-124">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b0f11-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="b0f11-125">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="b0f11-125">Select **Create**.</span></span>
9. <span data-ttu-id="b0f11-126">Veldu **Bæta við nýjum skilyrðum**.</span><span class="sxs-lookup"><span data-stu-id="b0f11-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="b0f11-127">Í reitnum **Hvar** skal velja aðallykil eða fjárhagsvídd.</span><span class="sxs-lookup"><span data-stu-id="b0f11-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="b0f11-128">Í reitnum **Virknitákn** skal velja valkost, eins og **er á milli** og **tekur með**.</span><span class="sxs-lookup"><span data-stu-id="b0f11-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="b0f11-129">Í reitinn **Gildi** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b0f11-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="b0f11-130">Í reitinn **Til og með** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="b0f11-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="b0f11-131">Veldu **Bæta við** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="b0f11-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="b0f11-132">Á listanum skal finna skipulag ítarlegrar reglu sem á að nota þegar þau skilyrði sem færð voru inn eru uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="b0f11-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="b0f11-133">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="b0f11-133">Select **Add**.</span></span>
17. <span data-ttu-id="b0f11-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b0f11-134">Close the page.</span></span>
18. <span data-ttu-id="b0f11-135">Veldu **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="b0f11-135">Select **Activate**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]