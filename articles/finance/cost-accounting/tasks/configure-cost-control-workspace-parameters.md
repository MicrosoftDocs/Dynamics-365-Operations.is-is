---
title: Skilgreina færibreytur vinnusvæðis kostnaðarstýringar
description: Nota þetta ferli til að grunnstilla Vinnusvæði kostnaðarstýringar svo stjórnendur á ýmsum stigum í fyrirtæki geti fengið innsýn inn í kostnaðarhluta þess, eins og og kostnaðarstaði og vöruflokka.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 867bfd2f2d1ff486e683cb11c38906dd0efe8c14
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187867"
---
# <a name="configure-cost-control-workspace-parameters"></a><span data-ttu-id="d9c3d-103">Skilgreina færibreytur vinnusvæðis kostnaðarstýringar</span><span class="sxs-lookup"><span data-stu-id="d9c3d-103">Configure cost control workspace parameters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d9c3d-104">Nota þetta ferli til að grunnstilla Vinnusvæði kostnaðarstýringar svo stjórnendur á ýmsum stigum í fyrirtæki geti fengið innsýn inn í kostnaðarhluta þess, eins og og kostnaðarstaði og vöruflokka.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-104">Use this procedure to configure the Cost control workspace so that managers at various levels in an organization can gain insight into their cost objects, such as cost centers and product groups.</span></span> <span data-ttu-id="d9c3d-105">USP2 sýnifyrirtækið var notað til að stofna þessa skráningu.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-105">The USP2 demo company was used to create this recording.</span></span>

1. <span data-ttu-id="d9c3d-106">Fara í kostnaðarbókhald > Uppsetning > kostnaðarstýring vinnusvæði skilgreining.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-106">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
2. <span data-ttu-id="d9c3d-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-107">Click New.</span></span>
3. <span data-ttu-id="d9c3d-108">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-108">In the Name field, type a value.</span></span>
4. <span data-ttu-id="d9c3d-109">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="d9c3d-110">Veljið Já í svæðinu Útgefið.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-110">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="d9c3d-111">Ef þú velur Já, geta notendur sem er úthlutað einu af eftirfarandi hlutverkum séð skýrsluna í Vinnusvæði kostnaðarstýringar: Stjórnandi kostnaðarbókhalds, endurskoðandi kostnaðar, afgreiðslustarfsmaður endurskoðanda kostnaðar, og eftirlitsmaður kostnaðarhluta.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-111">If you set this option to Yes, users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, or cost object controller.</span></span> <span data-ttu-id="d9c3d-112">Ef þú velur Nei, geta aðeins notendur sem er úthlutað einu af eftirfarandi hlutverkum séð skýrsluna í Vinnusvæði kostnaðarstýringar: Stjórnandi kostnaðarbókhalds, endurskoðandi kostnaðar, eða afgreiðslustarfsmaður endurskoðanda kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-112">If you set this option to No, only users who are assigned one of these roles can see the report in the Cost control workspace: cost accounting manager, cost accountant, or cost accountant clerk.</span></span>  
6. <span data-ttu-id="d9c3d-113">Útvíkka Afmörkun gagna svæðið.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-113">Expand the Data filtering section.</span></span>
7. <span data-ttu-id="d9c3d-114">Í reitinn Kostnaðarstýringareining skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-114">In the Cost control unit field, enter or select a value.</span></span>
8. <span data-ttu-id="d9c3d-115">Í svæði Upphafleg útgáfa kostnaðaráætlunar slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-115">In the Budget original version field, enter or select a value.</span></span>
9. <span data-ttu-id="d9c3d-116">Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðareiningar.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-116">In the Cost element dimension hierarchy field, enter or select a value.</span></span>
10. <span data-ttu-id="d9c3d-117">Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-117">In the Cost object dimension hierarchy field, enter or select a value.</span></span>
11. <span data-ttu-id="d9c3d-118">Útvíkka hlutann Úthluta útreikningsfærslum.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-118">Expand the Assign calculation records section.</span></span>
12. <span data-ttu-id="d9c3d-119">Smellið á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-119">Click New.</span></span>
13. <span data-ttu-id="d9c3d-120">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="d9c3d-121">Sláið inn eða veldu gildi í reitnum Fjárhagsdagatal tímabil.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-121">In the Fiscal calendar period field, enter or select a value.</span></span>
15. <span data-ttu-id="d9c3d-122">Í svæði Raunveruleg útgáfa, slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-122">In the Actual version field, enter or select a value.</span></span>
16. <span data-ttu-id="d9c3d-123">Útvíkka hlutann Fjárhagstímabil fyrir dálk.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-123">Expand the Fiscal periods per column section.</span></span>
17. <span data-ttu-id="d9c3d-124">Veljið Já í reitnum Núgildandi tímabil.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-124">Select Yes in the Current period field.</span></span>
18. <span data-ttu-id="d9c3d-125">Útvíkka hlutann Dálkar til sýna fyrir kostnað.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-125">Expand the Columns to display for costs section.</span></span>
19. <span data-ttu-id="d9c3d-126">Veljið Já í reitnum Fastur kostnaður.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-126">Select Yes in the Fixed cost field.</span></span>
20. <span data-ttu-id="d9c3d-127">Veljið Já í reitnum Breytilegur kostnaður.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-127">Select Yes in the Variable cost field.</span></span>
21. <span data-ttu-id="d9c3d-128">Veljið Já í reitnum heildarkostnaður.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-128">Select Yes in the Total cost field.</span></span>
22. <span data-ttu-id="d9c3d-129">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-129">Click Save.</span></span>
23. <span data-ttu-id="d9c3d-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-130">Close the page.</span></span>
24. <span data-ttu-id="d9c3d-131">Fara í kostnaðarbókhald > Vinnusvæði > kostnaðarstýring.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-131">Go to Cost accounting > Workspaces > Cost control.</span></span>
25. <span data-ttu-id="d9c3d-132">Veljið stöðu til að sjá fastan, breytilegan, heildar og óflokkaðan kostnað fyrir valin fjárhagstímabil.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-132">Select a statement to see fixed, variable, total, and unclassified costs for the selected fiscal periods.</span></span>
26. <span data-ttu-id="d9c3d-133">Sláið inn eða veldu gildi í reitnum Fjárhagsdagatal tímabil.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-133">In the Fiscal calendar period field, enter or select a value.</span></span>
27. <span data-ttu-id="d9c3d-134">Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-134">In the Cost object dimension hierarchy node field, enter or select a value.</span></span>
    * <span data-ttu-id="d9c3d-135">Eftir að þú hefur valið Stigveldi víddar fyrir kostnaðarhluta skal útvíkka Stigveldi víddar fyrir kostnaðarhluta til að sjá það kostnaðarvirði sem þú vilt.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-135">After you've selected a Cost object dimension hierarchy, expand the Cost element dimension hierarchy to see the desired cost values.</span></span> <span data-ttu-id="d9c3d-136">Þú getur t.d. útvíkkað stigveldið í Framleiðslurekstrarkostnaður til að sjá virðið.</span><span class="sxs-lookup"><span data-stu-id="d9c3d-136">For example, you can expand the hierarchy to Manufacturing overhead to see the value.</span></span>  

