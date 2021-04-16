---
title: Stofna stigveldi fyrirtækis fyrir skýrslur
description: Nota þetta ferli til að stofna skýrslustigveldi fyrir skýrslugerð fyrirtækis.
author: ShylaThompson
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 727a77b5a3a64bd4b679103e24d8c4c384a113e2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815741"
---
# <a name="create-an-organization-report-hierarchy"></a><span data-ttu-id="33a58-103">Stofna stigveldi fyrirtækis fyrir skýrslur</span><span class="sxs-lookup"><span data-stu-id="33a58-103">Create an organization report hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33a58-104">Nota þetta ferli til að stofna skýrslustigveldi fyrir skýrslugerð fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="33a58-104">Use this procedure to create a report hierarchy for organization reporting.</span></span> <span data-ttu-id="33a58-105">Tilgangur þessarar skráningar er að leiða þig í gegnum víddarstigveldið svo þú getir haldið áfram þar til öll skipan skýrslugerðar fyrirtækisins hefur verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="33a58-105">The purpose of this recording is to guide you through the dimension hierarchy so that you can continue until the whole organization reporting structure is created.</span></span> <span data-ttu-id="33a58-106">Þessi skráning notar USP2-sýnigagnafyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="33a58-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="33a58-107">Fara í kostnaðarbókhald > Víddir > Stigveldi vídda.</span><span class="sxs-lookup"><span data-stu-id="33a58-107">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="33a58-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="33a58-108">Click New.</span></span>
3. <span data-ttu-id="33a58-109">Velja „Stigveldi víddarflokkunar“ í reitnum HierarchyTypeComboBox.</span><span class="sxs-lookup"><span data-stu-id="33a58-109">In the HierarchyTypeComboBox field, select 'Dimension classification hierarchy'.</span></span>
    * <span data-ttu-id="33a58-110">Velja Stigveldi víddaflokkunar.</span><span class="sxs-lookup"><span data-stu-id="33a58-110">Select Dimension classification hierarchy.</span></span> <span data-ttu-id="33a58-111">Gerðin Flokkunarstigveldi víddar er notuð til að skilgreina reglur og til skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="33a58-111">The Dimension classification hierarchy type is used to define rules and for reporting purposes.</span></span> <span data-ttu-id="33a58-112">Hún styður allar víddir á borð við kostnaðarhluti, kostnaðareiningar og tölfræðilegar víddir.</span><span class="sxs-lookup"><span data-stu-id="33a58-112">It supports all dimensions, such as cost objects, cost elements, and statistical dimensions.</span></span>  
4. <span data-ttu-id="33a58-113">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="33a58-113">Click Create.</span></span>
5. <span data-ttu-id="33a58-114">Í reitinn Heiti stigveldi víddar skal slá inn „Fyrirtæki USP2“.</span><span class="sxs-lookup"><span data-stu-id="33a58-114">In the Dimension hierarchy name field, type 'Oganization USP2'.</span></span>
6. <span data-ttu-id="33a58-115">Sláið inn eða veljið gildi í reitnum Vídd.</span><span class="sxs-lookup"><span data-stu-id="33a58-115">In the Dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="33a58-116">Velja kostnaðarstaði.</span><span class="sxs-lookup"><span data-stu-id="33a58-116">Select Cost centers.</span></span>  
7. <span data-ttu-id="33a58-117">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="33a58-117">Click Save.</span></span>
8. <span data-ttu-id="33a58-118">Smella á Skoða stigveldi</span><span class="sxs-lookup"><span data-stu-id="33a58-118">Click View hierarchy.</span></span>
9. <span data-ttu-id="33a58-119">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="33a58-119">Click New.</span></span>
10. <span data-ttu-id="33a58-120">Í svæðið Heiti hnútar, færðu inn „Framkvæmdastjóri“.</span><span class="sxs-lookup"><span data-stu-id="33a58-120">In the Node name field, type 'CEO'.</span></span>
11. <span data-ttu-id="33a58-121">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="33a58-121">Click Save.</span></span>
12. <span data-ttu-id="33a58-122">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="33a58-122">Click New.</span></span>
13. <span data-ttu-id="33a58-123">Í svæðið Heiti hnútar, færðu inn „Kostnaðarstaðir Framkvæmdastjóri“.</span><span class="sxs-lookup"><span data-stu-id="33a58-123">In the Node name field, type 'CEO cost centers'.</span></span>
14. <span data-ttu-id="33a58-124">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="33a58-124">Click Save.</span></span>
15. <span data-ttu-id="33a58-125">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="33a58-125">Click New.</span></span>
16. <span data-ttu-id="33a58-126">Í svæðið Heiti hnútar, færðu inn „Svæði Austur“.</span><span class="sxs-lookup"><span data-stu-id="33a58-126">In the Node name field, type 'Region East'.</span></span>
17. <span data-ttu-id="33a58-127">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="33a58-127">Click Save.</span></span>
18. <span data-ttu-id="33a58-128">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="33a58-128">Click New.</span></span>
19. <span data-ttu-id="33a58-129">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="33a58-129">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="33a58-130">Sláið inn eða veldu gildi í reitnum Frá víddarstak.</span><span class="sxs-lookup"><span data-stu-id="33a58-130">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="33a58-131">Velja víddarstakið sem samsvarar hnútinum.</span><span class="sxs-lookup"><span data-stu-id="33a58-131">Select the dimension member that corresponds to the node.</span></span>  
21. <span data-ttu-id="33a58-132">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="33a58-132">Click Save.</span></span>
22. <span data-ttu-id="33a58-133">Í trénu skal velja „Fyrirtæki USP2\CEO\CEO Kostnaðarstaðir“.</span><span class="sxs-lookup"><span data-stu-id="33a58-133">In the tree, select 'Oganization USP2\CEO\CEO cost centers'.</span></span>
23. <span data-ttu-id="33a58-134">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="33a58-134">Click New.</span></span>
24. <span data-ttu-id="33a58-135">Í svæðið Heiti hnútar, færðu inn „Svæði Vestur“.</span><span class="sxs-lookup"><span data-stu-id="33a58-135">In the Node name field, type 'Region West'.</span></span>
25. <span data-ttu-id="33a58-136">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="33a58-136">Click Save.</span></span>
26. <span data-ttu-id="33a58-137">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="33a58-137">Click New.</span></span>
27. <span data-ttu-id="33a58-138">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="33a58-138">In the list, mark the selected row.</span></span>
28. <span data-ttu-id="33a58-139">Sláið inn eða veldu gildi í reitnum Frá víddarstak.</span><span class="sxs-lookup"><span data-stu-id="33a58-139">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="33a58-140">Velja víddarstakið sem samsvarar hnútinum.</span><span class="sxs-lookup"><span data-stu-id="33a58-140">Select the dimension member that corresponds to the node.</span></span>  
29. <span data-ttu-id="33a58-141">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="33a58-141">Click Save.</span></span>
30. <span data-ttu-id="33a58-142">Í trénu skal velja „Fyrirtæki USP2\CEO“.</span><span class="sxs-lookup"><span data-stu-id="33a58-142">In the tree, select 'Oganization USP2\CEO'.</span></span>
31. <span data-ttu-id="33a58-143">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="33a58-143">Click New.</span></span>
32. <span data-ttu-id="33a58-144">Í svæðið Heiti hnútar, færðu inn „Kostnaðarstaðir Framkvæmdastjóri“.</span><span class="sxs-lookup"><span data-stu-id="33a58-144">In the Node name field, type 'CFO cost centers'.</span></span>
33. <span data-ttu-id="33a58-145">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="33a58-145">Click Save.</span></span>
34. <span data-ttu-id="33a58-146">Smellið á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="33a58-146">Click New.</span></span>
35. <span data-ttu-id="33a58-147">Í svæðið Heiti hnútar, færðu inn „Markaðsherf“.</span><span class="sxs-lookup"><span data-stu-id="33a58-147">In the Node name field, type 'Marketing campa'.</span></span>
36. <span data-ttu-id="33a58-148">Í svæðið Heiti hnútar, færðu inn „Markaðsherferð“.</span><span class="sxs-lookup"><span data-stu-id="33a58-148">In the Node name field, type 'Marketing campaign'.</span></span>
37. <span data-ttu-id="33a58-149">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="33a58-149">Click Save.</span></span>
38. <span data-ttu-id="33a58-150">Smellið á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="33a58-150">Click New.</span></span>
39. <span data-ttu-id="33a58-151">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="33a58-151">In the list, mark the selected row.</span></span>
40. <span data-ttu-id="33a58-152">Sláið inn eða veldu gildi í reitnum Frá víddarstak.</span><span class="sxs-lookup"><span data-stu-id="33a58-152">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="33a58-153">Velja víddarstakið sem samsvarar hnútinum.</span><span class="sxs-lookup"><span data-stu-id="33a58-153">Select the dimension member that corresponds to the node.</span></span>  
41. <span data-ttu-id="33a58-154">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="33a58-154">Click Save.</span></span>
42. <span data-ttu-id="33a58-155">Í trénu skal velja „Fyrirtæki USP2\CEO\CFO Kostnaðarstaðir“.</span><span class="sxs-lookup"><span data-stu-id="33a58-155">In the tree, select 'Organization USP2\CEO\CFO cost centers'.</span></span>
43. <span data-ttu-id="33a58-156">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="33a58-156">Click New.</span></span>
44. <span data-ttu-id="33a58-157">Í svæðið Heiti hnútar, færðu inn „Vörusýningar“.</span><span class="sxs-lookup"><span data-stu-id="33a58-157">In the Node name field, type 'Trade shows'.</span></span>
45. <span data-ttu-id="33a58-158">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="33a58-158">Click Save.</span></span>
46. <span data-ttu-id="33a58-159">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="33a58-159">Click New.</span></span>
47. <span data-ttu-id="33a58-160">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="33a58-160">In the list, mark the selected row.</span></span>
48. <span data-ttu-id="33a58-161">Sláið inn eða veldu gildi í reitnum Frá víddarstak.</span><span class="sxs-lookup"><span data-stu-id="33a58-161">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="33a58-162">Velja víddarstakið sem samsvarar hnútinum.</span><span class="sxs-lookup"><span data-stu-id="33a58-162">Select the dimension member that corresponds to the node.</span></span>  
49. <span data-ttu-id="33a58-163">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="33a58-163">Click Save.</span></span>
50. <span data-ttu-id="33a58-164">Í trénu skal velja „Fyrirtæki USP2\CEO“.</span><span class="sxs-lookup"><span data-stu-id="33a58-164">In the tree, select 'Oganization USP2\CEO'.</span></span>
51. <span data-ttu-id="33a58-165">Í svæðið Heiti hnútar, færðu inn „Kostnaðarstaðir Framkvæmdastjóri“.</span><span class="sxs-lookup"><span data-stu-id="33a58-165">In the Node name field, type 'CIO cost centers'.</span></span>
52. <span data-ttu-id="33a58-166">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="33a58-166">Click Save.</span></span>
53. <span data-ttu-id="33a58-167">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="33a58-167">Click New.</span></span>
54. <span data-ttu-id="33a58-168">Í svæðið Heiti hnútar, færðu inn „Símaver“.</span><span class="sxs-lookup"><span data-stu-id="33a58-168">In the Node name field, type 'Call centers'.</span></span>
55. <span data-ttu-id="33a58-169">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="33a58-169">Click Save.</span></span>
56. <span data-ttu-id="33a58-170">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="33a58-170">Click New.</span></span>
57. <span data-ttu-id="33a58-171">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="33a58-171">In the list, mark the selected row.</span></span>
58. <span data-ttu-id="33a58-172">Sláið inn eða veldu gildi í reitnum Frá víddarstak.</span><span class="sxs-lookup"><span data-stu-id="33a58-172">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="33a58-173">Velja víddarstakið sem samsvarar hnútinum.</span><span class="sxs-lookup"><span data-stu-id="33a58-173">Select the dimension member that corresponds to the node.</span></span>  
59. <span data-ttu-id="33a58-174">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="33a58-174">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]