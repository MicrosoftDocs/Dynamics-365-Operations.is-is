---
title: Stofna og úthluta ítarlegu regluskipulagi
description: Þetta efni útskýrir hvernig á að stofna og úthluta ítarlegri reglusamsetningu við reikningsskipulag.
author: aprilolson
manager: AnnBe
ms.date: 07/19/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountRuleStructure, DimensionCreateAccountRuleStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate, DimensionConfigureAccountStructure, DimensionConfigureAccountRule, DimensionCreateAccountRule, DimensionSelectAccountRuleStructure
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e6a3f7d174c91e357dce8a19ab50a5cd42a85561
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968601"
---
# <a name="create-and-assign-advanced-rule-structures"></a><span data-ttu-id="43e15-103">Stofna og úthluta ítarlegu regluskipulagi</span><span class="sxs-lookup"><span data-stu-id="43e15-103">Create and assign advanced rule structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="43e15-104">Þetta efni útskýrir hvernig á að stofna og úthluta ítarlegri reglusamsetningu við reikningsskipulag.</span><span class="sxs-lookup"><span data-stu-id="43e15-104">This topic explains how to create and assign an advanced rule structure to an account structure.</span></span> <span data-ttu-id="43e15-105">Þessi handbók notar sýnifyrirtækið USMF.</span><span class="sxs-lookup"><span data-stu-id="43e15-105">This guide uses the USMF demo company.</span></span>

## <a name="create-an-advanced-rule-structure"></a><span data-ttu-id="43e15-106">Stofna skipulag ítarlegrar reglu</span><span class="sxs-lookup"><span data-stu-id="43e15-106">Create an advanced rule structure</span></span>
1. <span data-ttu-id="43e15-107">Farðu í **Skoðunarrúðu > Kerfi > Fjárhagur > Bókhaldslykill > Skipulag > Ítarlegt regluskipulag**.</span><span class="sxs-lookup"><span data-stu-id="43e15-107">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Advanced rule structures**.</span></span>
2. <span data-ttu-id="43e15-108">Veldu **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="43e15-108">Select **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="43e15-109">Í reitnum **Ítarlegt regluskipulag** slærðu inn heiti til að lýsa regluskipulaginu.</span><span class="sxs-lookup"><span data-stu-id="43e15-109">In the **Advanced rule structure** field, type a name to describe the rule structure.</span></span>
4. <span data-ttu-id="43e15-110">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="43e15-110">Select **OK**.</span></span>
5. <span data-ttu-id="43e15-111">Veldu **Bæta við hluta**.</span><span class="sxs-lookup"><span data-stu-id="43e15-111">Select **Add segment**.</span></span>
6. <span data-ttu-id="43e15-112">Í lista yfir liði skal velja fjárhagsvídd.</span><span class="sxs-lookup"><span data-stu-id="43e15-112">In the list of segments, select a financial dimension.</span></span> <span data-ttu-id="43e15-113">Til dæmis **Verslun**.</span><span class="sxs-lookup"><span data-stu-id="43e15-113">For example, **Store**.</span></span>  
7. <span data-ttu-id="43e15-114">Veldu **Bæta við hluta**.</span><span class="sxs-lookup"><span data-stu-id="43e15-114">Select **Add segment**.</span></span>
8. <span data-ttu-id="43e15-115">Veldu **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="43e15-115">Select **Activate**.</span></span>

## <a name="apply-an-advanced-rule-structure-to-an-account-structure"></a><span data-ttu-id="43e15-116">Beita ítarlegu regluskipulagi á lykilskipulag</span><span class="sxs-lookup"><span data-stu-id="43e15-116">Apply an advanced rule structure to an account structure</span></span>
1. <span data-ttu-id="43e15-117">Farðu í **Skoðunarrúðu > Kerfi > Fjárhagur > Bókhaldslykill > Skipulag > Skilgreina lykilskipulög**.</span><span class="sxs-lookup"><span data-stu-id="43e15-117">Go to **navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="43e15-118">Í listanum skal finna og velja það lykilskipulag sem á að beita ítarlegri reglu á.</span><span class="sxs-lookup"><span data-stu-id="43e15-118">In the list, find and select the account structure you want to apply the advanced rule to.</span></span>
3. <span data-ttu-id="43e15-119">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="43e15-119">Select **Edit**.</span></span> <span data-ttu-id="43e15-120">Einnig er hægt að velja **Ítarlegar reglur** og notandi er beðinn um að setja lykilskipulag inn í **Drög**.</span><span class="sxs-lookup"><span data-stu-id="43e15-120">You can also select **Advanced rules** and you will be prompted to put the account structure in **Draft mode**.</span></span>  
4. <span data-ttu-id="43e15-121">Veldu **Ítarlegar reglur**.</span><span class="sxs-lookup"><span data-stu-id="43e15-121">Select **Advanced rules**.</span></span>
5. <span data-ttu-id="43e15-122">Veldu **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="43e15-122">Select **New** to open the drop dialog.</span></span>
6. <span data-ttu-id="43e15-123">Í reitinn **Ítarleg regla** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="43e15-123">In the **Advanced rule** field, type a value.</span></span>
7. <span data-ttu-id="43e15-124">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="43e15-124">In the **Name** field, type a value.</span></span>
8. <span data-ttu-id="43e15-125">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="43e15-125">Select **Create**.</span></span>
9. <span data-ttu-id="43e15-126">Veldu **Bæta við nýjum skilyrðum**.</span><span class="sxs-lookup"><span data-stu-id="43e15-126">Select **Add new criteria**.</span></span>
10. <span data-ttu-id="43e15-127">Í reitnum **Hvar** skal velja aðallykil eða fjárhagsvídd.</span><span class="sxs-lookup"><span data-stu-id="43e15-127">In the **Where** field, select main account or a financial dimension.</span></span>
11. <span data-ttu-id="43e15-128">Í reitnum **Virknitákn** skal velja valkost, eins og **er á milli** og **tekur með**.</span><span class="sxs-lookup"><span data-stu-id="43e15-128">In the **Operator** field, select an option, such as **is between** and **includes**.</span></span>
12. <span data-ttu-id="43e15-129">Í reitinn **Gildi** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="43e15-129">In the **Value** field, type a value.</span></span>
13. <span data-ttu-id="43e15-130">Í reitinn **Til og með** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="43e15-130">In the **through** field, type a value.</span></span>
14. <span data-ttu-id="43e15-131">Veldu **Bæta við** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="43e15-131">Select **Add** to open the drop dialog.</span></span>
15. <span data-ttu-id="43e15-132">Á listanum skal finna skipulag ítarlegrar reglu sem á að nota þegar þau skilyrði sem færð voru inn eru uppfyllt.</span><span class="sxs-lookup"><span data-stu-id="43e15-132">In the list, find the advanced rule structure you want to use when the criteria you entered is met.</span></span>
16. <span data-ttu-id="43e15-133">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="43e15-133">Select **Add**.</span></span>
17. <span data-ttu-id="43e15-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="43e15-134">Close the page.</span></span>
18. <span data-ttu-id="43e15-135">Veldu **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="43e15-135">Select **Activate**.</span></span>

