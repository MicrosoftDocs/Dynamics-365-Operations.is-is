---
title: Stofna stigveldi fyrirtækis fyrir skýrslur
description: Nota þetta ferli til að stofna skýrslustigveldi fyrir skýrslugerð fyrirtækis.
author: ShylaThompson
manager: AnnBe
ms.date: 10/30/2017
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
ms.openlocfilehash: 5684c710b8e167a4a39f106eb3c0fd77e3011dbd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841346"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="28956-103">Stofna stigveldi fyrirtækis fyrir skýrslur</span><span class="sxs-lookup"><span data-stu-id="28956-103">Create an organization report hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="28956-104">Nota þetta ferli til að stofna skýrslustigveldi fyrir skýrslugerð fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="28956-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="28956-105">Tilgangur þessarar skráningar er að leiða þig í gegnum víddarstigveldið svo þú getir haldið áfram þar til öll skipan skýrslugerðar fyrirtækisins hefur verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="28956-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="28956-106">Þessi skráning notar USP2-sýnigagnafyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="28956-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="28956-107">Fara í kostnaðarbókhald > Víddir > Stigveldi vídda.</span><span class="sxs-lookup"><span data-stu-id="28956-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="28956-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="28956-108">Click New.</span></span>
3. <span data-ttu-id="28956-109">Velja „Stigveldi víddarflokkunar“ í reitnum HierarchyTypeComboBox.</span><span class="sxs-lookup"><span data-stu-id="28956-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="28956-110">Velja Stigveldi víddaflokkunar.</span><span class="sxs-lookup"><span data-stu-id="28956-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="28956-111">Gerðin Flokkunarstigveldi víddar er notuð til að skilgreina reglur og til skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="28956-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="28956-112">Hún styður allar víddir á borð við kostnaðarhluti, kostnaðareiningar og tölfræðilegar víddir.</span><span class="sxs-lookup"><span data-stu-id="28956-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="28956-113">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="28956-113">Click Create.</span></span>
5. <span data-ttu-id="28956-114">Í reitinn Heiti stigveldi víddar skal slá inn „Fyrirtæki USP2“.</span><span class="sxs-lookup"><span data-stu-id="28956-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="28956-115">Sláið inn eða veljið gildi í reitnum Vídd.</span><span class="sxs-lookup"><span data-stu-id="28956-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="28956-116">Velja kostnaðarstaði.</span><span class="sxs-lookup"><span data-stu-id="28956-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="28956-117">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="28956-117">Click Save.</span></span>
8. <span data-ttu-id="28956-118">Smella á Skoða stigveldi</span><span class="sxs-lookup"><span data-stu-id="28956-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="28956-119">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="28956-119">Click New.</span></span>
10. <span data-ttu-id="28956-120">Í svæðið Heiti hnútar, færðu inn „Framkvæmdastjóri“.</span><span class="sxs-lookup"><span data-stu-id="28956-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="28956-121">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="28956-121">Click Save.</span></span>
12. <span data-ttu-id="28956-122">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="28956-122">Click New.</span></span>
13. <span data-ttu-id="28956-123">Í svæðið Heiti hnútar, færðu inn „Kostnaðarstaðir Framkvæmdastjóri“.</span><span class="sxs-lookup"><span data-stu-id="28956-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="28956-124">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="28956-124">Click Save.</span></span>
15. <span data-ttu-id="28956-125">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="28956-125">Click New.</span></span>
16. <span data-ttu-id="28956-126">Í svæðið Heiti hnútar, færðu inn „Svæði Austur“.</span><span class="sxs-lookup"><span data-stu-id="28956-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="28956-127">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="28956-127">Click Save.</span></span>
18. <span data-ttu-id="28956-128">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="28956-128">Click New.</span></span>
19. <span data-ttu-id="28956-129">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="28956-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="28956-130">Sláið inn eða veldu gildi í reitnum Frá víddarstak.</span><span class="sxs-lookup"><span data-stu-id="28956-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="28956-131">Velja víddarstakið sem samsvarar hnútinum.</span><span class="sxs-lookup"><span data-stu-id="28956-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="28956-132">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="28956-132">Click Save.</span></span>
22. <span data-ttu-id="28956-133">Í trénu skal velja „Fyrirtæki USP2\CEO\CEO Kostnaðarstaðir“.</span><span class="sxs-lookup"><span data-stu-id="28956-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="28956-134">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="28956-134">Click New.</span></span>
24. <span data-ttu-id="28956-135">Í svæðið Heiti hnútar, færðu inn „Svæði Vestur“.</span><span class="sxs-lookup"><span data-stu-id="28956-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="28956-136">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="28956-136">Click Save.</span></span>
26. <span data-ttu-id="28956-137">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="28956-137">Click New.</span></span>
27. <span data-ttu-id="28956-138">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="28956-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="28956-139">Sláið inn eða veldu gildi í reitnum Frá víddarstak.</span><span class="sxs-lookup"><span data-stu-id="28956-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="28956-140">Velja víddarstakið sem samsvarar hnútinum.</span><span class="sxs-lookup"><span data-stu-id="28956-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="28956-141">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="28956-141">Click Save.</span></span>
30. <span data-ttu-id="28956-142">Í trénu skal velja „Fyrirtæki USP2\CEO“.</span><span class="sxs-lookup"><span data-stu-id="28956-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="28956-143">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="28956-143">Click New.</span></span>
32. <span data-ttu-id="28956-144">Í svæðið Heiti hnútar, færðu inn „Kostnaðarstaðir Framkvæmdastjóri“.</span><span class="sxs-lookup"><span data-stu-id="28956-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="28956-145">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="28956-145">Click Save.</span></span>
34. <span data-ttu-id="28956-146">Smellið á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="28956-146">Click New.</span></span>
35. <span data-ttu-id="28956-147">Í svæðið Heiti hnútar, færðu inn „Markaðsherf“.</span><span class="sxs-lookup"><span data-stu-id="28956-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="28956-148">Í svæðið Heiti hnútar, færðu inn „Markaðsherferð“.</span><span class="sxs-lookup"><span data-stu-id="28956-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="28956-149">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="28956-149">Click Save.</span></span>
38. <span data-ttu-id="28956-150">Smellið á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="28956-150">Click New.</span></span>
39. <span data-ttu-id="28956-151">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="28956-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="28956-152">Sláið inn eða veldu gildi í reitnum Frá víddarstak.</span><span class="sxs-lookup"><span data-stu-id="28956-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="28956-153">Velja víddarstakið sem samsvarar hnútinum.</span><span class="sxs-lookup"><span data-stu-id="28956-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="28956-154">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="28956-154">Click Save.</span></span>
42. <span data-ttu-id="28956-155">Í trénu skal velja „Fyrirtæki USP2\CEO\CFO Kostnaðarstaðir“.</span><span class="sxs-lookup"><span data-stu-id="28956-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="28956-156">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="28956-156">Click New.</span></span>
44. <span data-ttu-id="28956-157">Í svæðið Heiti hnútar, færðu inn „Vörusýningar“.</span><span class="sxs-lookup"><span data-stu-id="28956-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="28956-158">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="28956-158">Click Save.</span></span>
46. <span data-ttu-id="28956-159">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="28956-159">Click New.</span></span>
47. <span data-ttu-id="28956-160">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="28956-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="28956-161">Sláið inn eða veldu gildi í reitnum Frá víddarstak.</span><span class="sxs-lookup"><span data-stu-id="28956-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="28956-162">Velja víddarstakið sem samsvarar hnútinum.</span><span class="sxs-lookup"><span data-stu-id="28956-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="28956-163">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="28956-163">Click Save.</span></span>
50. <span data-ttu-id="28956-164">Í trénu skal velja „Fyrirtæki USP2\CEO“.</span><span class="sxs-lookup"><span data-stu-id="28956-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="28956-165">Í svæðið Heiti hnútar, færðu inn „Kostnaðarstaðir Framkvæmdastjóri“.</span><span class="sxs-lookup"><span data-stu-id="28956-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="28956-166">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="28956-166">Click Save.</span></span>
53. <span data-ttu-id="28956-167">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="28956-167">Click New.</span></span>
54. <span data-ttu-id="28956-168">Í svæðið Heiti hnútar, færðu inn „Símaver“.</span><span class="sxs-lookup"><span data-stu-id="28956-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="28956-169">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="28956-169">Click Save.</span></span>
56. <span data-ttu-id="28956-170">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="28956-170">Click New.</span></span>
57. <span data-ttu-id="28956-171">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="28956-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="28956-172">Sláið inn eða veldu gildi í reitnum Frá víddarstak.</span><span class="sxs-lookup"><span data-stu-id="28956-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="28956-173">Velja víddarstakið sem samsvarar hnútinum.</span><span class="sxs-lookup"><span data-stu-id="28956-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="28956-174">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="28956-174">Click Save.</span></span>

