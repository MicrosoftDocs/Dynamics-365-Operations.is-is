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
ms.openlocfilehash: 8b100d5da6ec26dc386c0c6cb0793245531eb0d8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186257"
---
# <a name="create-account-structures"></a><span data-ttu-id="9ef86-103">Stofna lykilskipulög</span><span class="sxs-lookup"><span data-stu-id="9ef86-103">Create account structures</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9ef86-104">Þessi leiðarvísir fyrir verk fer í gegnum stofnun lykilskipulags.</span><span class="sxs-lookup"><span data-stu-id="9ef86-104">This task guide steps through creating an account structure.</span></span> <span data-ttu-id="9ef86-105">Skrefin nota sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="9ef86-105">The steps use demo data company USMF.</span></span>

1. <span data-ttu-id="9ef86-106">Farðu í **Skoðunarrúðu > Kerfi > Fjárhagur > Bókhaldslykill > Skipulag > Skilgreina lykilskipulög**.</span><span class="sxs-lookup"><span data-stu-id="9ef86-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Structures > Configure account structures**.</span></span>
2. <span data-ttu-id="9ef86-107">Í **aðgerðarsvæðinu** smellirðu á **Nýtt** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="9ef86-107">On the **Action pane**, click **New** to open the drop dialog.</span></span>
3. <span data-ttu-id="9ef86-108">Í reitnum **Lykilskipulag** skal slá inn heiti sem lýsir tilgangi lykilskipulags.</span><span class="sxs-lookup"><span data-stu-id="9ef86-108">In the **Account structure** field, type a name to describe the purpose of the account structure.</span></span>
4. <span data-ttu-id="9ef86-109">Í reitnum **Lýsing** skal slá inn heiti sem lýsir tilgangi lykilskipulags.</span><span class="sxs-lookup"><span data-stu-id="9ef86-109">In the **Description** field, type a description to specify the purpose of the account structure.</span></span>
5. <span data-ttu-id="9ef86-110">Smellið á **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="9ef86-110">Click **Create**.</span></span>
6. <span data-ttu-id="9ef86-111">Í **Hlutum og leyfilegum gildum** smellirðu á **Bæta við hluta**.</span><span class="sxs-lookup"><span data-stu-id="9ef86-111">In the **Segments and allowed values**, click **Add segment**.</span></span>
7. <span data-ttu-id="9ef86-112">Í víddalistanum velurðu vídd til að bæta við lykilskipulagið.</span><span class="sxs-lookup"><span data-stu-id="9ef86-112">In the dimensions list, select the dimension to add to the account structure.</span></span>
8. <span data-ttu-id="9ef86-113">Í lok listans smellirðu á **Bæta við hluta**.</span><span class="sxs-lookup"><span data-stu-id="9ef86-113">At the end of the list, click **Add segment**.</span></span>
9. <span data-ttu-id="9ef86-114">Endurtaktu skref 6 til 9 eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="9ef86-114">Repeat step 6 to 9 as needed.</span></span>
10. <span data-ttu-id="9ef86-115">Í hlutanum **Upplýsingar um leyfð gildi** velurðu hluta til að breyta leyfðum gildum.</span><span class="sxs-lookup"><span data-stu-id="9ef86-115">In the **Allowed value details** section, select the segment to edit the allowed values.</span></span>
    <span data-ttu-id="9ef86-116">Smelltu til dæmis á reitinn **Aðallykill**.</span><span class="sxs-lookup"><span data-stu-id="9ef86-116">For example, click the **Main Account** field.</span></span>  
11. <span data-ttu-id="9ef86-117">Í reitnum **Virknitákn** skal velja valkost, eins og er á milli og tekur með.</span><span class="sxs-lookup"><span data-stu-id="9ef86-117">In the **Operator** field, select an option, such as is between and includes.</span></span>
12. <span data-ttu-id="9ef86-118">Í reitinn **Gildi** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9ef86-118">In the **Value** field, type a value.</span></span> <span data-ttu-id="9ef86-119">Til dæmis 600000.</span><span class="sxs-lookup"><span data-stu-id="9ef86-119">For example, 600000.</span></span>  
13. <span data-ttu-id="9ef86-120">Í reitinn **Til og með** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9ef86-120">In the **through** field, type a value.</span></span> <span data-ttu-id="9ef86-121">Til dæmis 699999.</span><span class="sxs-lookup"><span data-stu-id="9ef86-121">For example, 699999.</span></span>  
14. <span data-ttu-id="9ef86-122">Í kaflanum **Upplýsingar um leyfð gildi** smellirðu á **Nota**.</span><span class="sxs-lookup"><span data-stu-id="9ef86-122">In the **Allowed value details** section, click **Apply**.</span></span>
15. <span data-ttu-id="9ef86-123">Endurtaktu skref 10 til 15 eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="9ef86-123">Repeat step 10 to 15 as needed.</span></span>  
16. <span data-ttu-id="9ef86-124">Í kaflanum **Upplýsingar um leyfð gildi** smellirðu á **Bæta við nýjum skilyrðum**.</span><span class="sxs-lookup"><span data-stu-id="9ef86-124">In the **Allowed value details** section, click **Add new criteria**.</span></span>
17. <span data-ttu-id="9ef86-125">Í reitnum Virknitákn skal velja valkost, eins og er á milli og tekur með.</span><span class="sxs-lookup"><span data-stu-id="9ef86-125">In the Operator field, select an option, such as is between and includes.</span></span>
18. <span data-ttu-id="9ef86-126">Í reitinn **Gildi** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9ef86-126">In the **Value** field, type a value.</span></span> <span data-ttu-id="9ef86-127">Til dæmis 033.</span><span class="sxs-lookup"><span data-stu-id="9ef86-127">For example, 033.</span></span>  
19. <span data-ttu-id="9ef86-128">Í reitinn **Til og með** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9ef86-128">In the **through** field, type a value.</span></span> <span data-ttu-id="9ef86-129">Til dæmis 034.</span><span class="sxs-lookup"><span data-stu-id="9ef86-129">For example, 034.</span></span>  
20. <span data-ttu-id="9ef86-130">Smellið á **Nota**.</span><span class="sxs-lookup"><span data-stu-id="9ef86-130">Click **Apply**.</span></span>
21. <span data-ttu-id="9ef86-131">Í hnitanetinu velurðu hluta til að breyta leyfðum gildum.</span><span class="sxs-lookup"><span data-stu-id="9ef86-131">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="9ef86-132">Til dæmis Kostnaðarstað.</span><span class="sxs-lookup"><span data-stu-id="9ef86-132">For example, Cost Center.</span></span>  
22. <span data-ttu-id="9ef86-133">Í reitinn **CostCenter** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9ef86-133">In the **CostCenter field**, type a value.</span></span> <span data-ttu-id="9ef86-134">Til dæmis 007..021.</span><span class="sxs-lookup"><span data-stu-id="9ef86-134">For example, 007..021.</span></span>  
23. <span data-ttu-id="9ef86-135">Í **Hlutum og leyfilegum gildum** smellirðu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="9ef86-135">In the **Segments and allowed values**, click **Add**.</span></span>
24. <span data-ttu-id="9ef86-136">Í reitinn **MainAccount** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9ef86-136">In the **MainAccount** field, type a value.</span></span> <span data-ttu-id="9ef86-137">Til dæmis 600000..699999</span><span class="sxs-lookup"><span data-stu-id="9ef86-137">For example, 600000..699999</span></span>  
25. <span data-ttu-id="9ef86-138">Í hnitanetinu velurðu hluta til að breyta leyfðum gildum.</span><span class="sxs-lookup"><span data-stu-id="9ef86-138">In the grid, select the segment to edit the allowed values.</span></span> <span data-ttu-id="9ef86-139">Til dæmis Deild.</span><span class="sxs-lookup"><span data-stu-id="9ef86-139">For example, Department.</span></span>  
26. <span data-ttu-id="9ef86-140">Í reitinn Deild skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9ef86-140">In the Department field, type a value.</span></span> <span data-ttu-id="9ef86-141">Til dæmis 032.</span><span class="sxs-lookup"><span data-stu-id="9ef86-141">For example, 032.</span></span>  
27. <span data-ttu-id="9ef86-142">Í reitinn CostCenter skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9ef86-142">In the CostCenter field, type a value.</span></span> <span data-ttu-id="9ef86-143">Til dæmis 086.</span><span class="sxs-lookup"><span data-stu-id="9ef86-143">For example, 086.</span></span>  
28. <span data-ttu-id="9ef86-144">Í **aðgerðarúðunni** skaltu smella á **Villuleita**.</span><span class="sxs-lookup"><span data-stu-id="9ef86-144">On the **Action pane**, click **Validate**.</span></span>
29. <span data-ttu-id="9ef86-145">Í **aðgerðarúðunni** skal smella á **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="9ef86-145">On the **Action pane**, click **Activate**.</span></span>
30. <span data-ttu-id="9ef86-146">Smellið á **Virkja**.</span><span class="sxs-lookup"><span data-stu-id="9ef86-146">Click **Activate**.</span></span>
