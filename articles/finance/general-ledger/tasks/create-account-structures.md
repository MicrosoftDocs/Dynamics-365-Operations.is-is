---
title: Stofna lykilskipulög
description: Þessi leiðarvísir fyrir verk fer í gegnum stofnun lykilskipulags.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DimensionConfigureAccountStructure, DimensionCreateAccountStructure, DimensionHierarchyAddLevel, DimensionHierarchyConstraintActivate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b75ee76a1fb874652415a2174441f629955d763a
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145156"
---
# <a name="create-account-structures"></a><span data-ttu-id="c9cb7-103">Stofna lykilskipulög</span><span class="sxs-lookup"><span data-stu-id="c9cb7-103">Create account structures</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c9cb7-104">Þessi leiðarvísir fyrir verk fer í gegnum stofnun lykilskipulags.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="c9cb7-105">Skrefin nota sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="c9cb7-106">Farðu í **Skoðunarrúðu > Kerfi > Fjárhagur > Bókhaldslykill > Skipulag > Skilgreina lykilskipulög**.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="c9cb7-107">Í **aðgerðarsvæðinu** smellirðu á **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="c9cb7-108">Í reitnum **Lykilskipulag** skal slá inn heiti sem lýsir tilgangi lykilskipulags.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="c9cb7-109">Í reitnum **Lýsing** skal slá inn heiti sem lýsir tilgangi lykilskipulags.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="c9cb7-110">Smellið á **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-110">Click **Create**.</span></span>
6. <span data-ttu-id="c9cb7-111">Í **Hlutum og leyfilegum gildum** smellirðu á **Bæta við hluta**.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="c9cb7-112">Í víddalistanum velurðu vídd til að bæta við lykilskipulagið.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="c9cb7-113">Í lok listans smellirðu á **Bæta við hluta**.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="c9cb7-114">Endurtaktu skref 6 til 9 eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="c9cb7-115">Í hlutanum **Upplýsingar um leyfð gildi** velurðu hluta til að breyta leyfðum gildum.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="c9cb7-116">Smelltu til dæmis á reitinn **Aðallykill**.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="c9cb7-117">Í reitnum **Virknitákn** skal velja valkost, eins og er á milli og tekur með.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="c9cb7-118">Í reitinn **Gildi** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="c9cb7-119">Til dæmis 600000.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-119">For example, 600000.</span></span>  
13. <span data-ttu-id="c9cb7-120">Í reitinn **Til og með** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-120">In the **through** field, type a value.</span></span> <span data-ttu-id="c9cb7-121">Til dæmis 699999.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-121">For example, 699999.</span></span>  
14. <span data-ttu-id="c9cb7-122">Í kaflanum **Upplýsingar um leyfð gildi** smellirðu á **Nota**.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="c9cb7-123">Endurtaktu skref 10 til 15 eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="c9cb7-124">Í kaflanum **Upplýsingar um leyfð gildi** smellirðu á **Bæta við nýjum skilyrðum**.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="c9cb7-125">Í reitnum Virknitákn skal velja valkost, eins og er á milli og tekur með.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="c9cb7-126">Í reitinn **Gildi** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="c9cb7-127">Til dæmis 033.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-127">For example, 033.</span></span>  
19. <span data-ttu-id="c9cb7-128">Í reitinn **Til og með** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-128">In the **through** field, type a value.</span></span> <span data-ttu-id="c9cb7-129">Til dæmis 034.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-129">For example, 034.</span></span>  
20. <span data-ttu-id="c9cb7-130">Smellið á **Nota**.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-130">Click **Apply**.</span></span>
21. <span data-ttu-id="c9cb7-131">Í hnitanetinu velurðu hluta til að breyta leyfðum gildum.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="c9cb7-132">Til dæmis Kostnaðarstað.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="c9cb7-133">Í reitinn **CostCenter** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="c9cb7-134">Til dæmis 007..021.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="c9cb7-135">Í **Hlutum og leyfilegum gildum** smellirðu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="c9cb7-136">Í reitinn **MainAccount** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="c9cb7-137">Til dæmis 600000..699999</span><span class="sxs-lookup"><span data-stu-id="c9cb7-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="c9cb7-138">Í hnitanetinu velurðu hluta til að breyta leyfðum gildum.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="c9cb7-139">Til dæmis Deild.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-139">For example, Department.</span></span>  
26. <span data-ttu-id="c9cb7-140">Í reitinn Deild skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-140">In the Department field, type a value.</span></span> <span data-ttu-id="c9cb7-141">Til dæmis 032.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-141">For example, 032.</span></span>  
27. <span data-ttu-id="c9cb7-142">Í reitinn CostCenter skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="c9cb7-143">Til dæmis 086.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-143">For example, 086.</span></span>  
28. <span data-ttu-id="c9cb7-144">Í **aðgerðarúðunni** skaltu smella á **Villuleita**.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="c9cb7-145">Í **aðgerðarúðunni** skal smella á **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="c9cb7-146">Smellið á **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="c9cb7-146">Click **Activate**.</span></span>

