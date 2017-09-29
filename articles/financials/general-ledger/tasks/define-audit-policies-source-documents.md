--- 
title: "Skilgreina endurskoðunarstefnur fyrir upprunaskjöl"
description: "Þessi verklýsing sýnir hvernig á að setja upp og keyra reglu endurskoðunarstefnu."
author: ryansandness
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 4b05f744120e940bfea3e92b8aac3e41fc8151d9
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="fbed3-103">Skilgreina endurskoðunarstefnur fyrir upprunaskjöl</span><span class="sxs-lookup"><span data-stu-id="fbed3-103">Define audit policies for source documents</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fbed3-104">Þessi verklýsing sýnir hvernig á að setja upp og keyra reglu endurskoðunarstefnu.</span><span class="sxs-lookup"><span data-stu-id="fbed3-104">This procedure shows how to set up and run audit policy rules.</span></span> <span data-ttu-id="fbed3-105">Dæmi notar kostnaðarskýrslur með hótel kostnaðargerð.</span><span class="sxs-lookup"><span data-stu-id="fbed3-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="fbed3-106">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="fbed3-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="fbed3-107">Endurskoðandahlutverkið inniheldur réttar heimildir til að framkvæma þessi verk.</span><span class="sxs-lookup"><span data-stu-id="fbed3-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="fbed3-108">Fara á vinnusvæði Endurskoðunar > Uppsetning > Stefnureglugerð.</span><span class="sxs-lookup"><span data-stu-id="fbed3-108">Go to Audit workbench > Setup > Policy rule type.</span></span>
2. <span data-ttu-id="fbed3-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="fbed3-109">Click New.</span></span>
3. <span data-ttu-id="fbed3-110">Í reitinn Nafn reglu skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="fbed3-110">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="fbed3-111">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="fbed3-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fbed3-112">Í svæðið heiti Fyrirspurnar, veljið línu Kostnaðarskýrslu</span><span class="sxs-lookup"><span data-stu-id="fbed3-112">In the Query name field, select Expense report line</span></span>
6. <span data-ttu-id="fbed3-113">Veljið í svæðinu fyrirspurn skal velja samanlagt</span><span class="sxs-lookup"><span data-stu-id="fbed3-113">In the query type field, select Aggregate</span></span>
7. <span data-ttu-id="fbed3-114">Í reitnum Lögaðili skal velja lögaðila</span><span class="sxs-lookup"><span data-stu-id="fbed3-114">In the Legal entity field, select Legal entity</span></span>
8. <span data-ttu-id="fbed3-115">Í svæðinu tilvísun dagsetningar Skjals, veljið breytt dagsetning og tími</span><span class="sxs-lookup"><span data-stu-id="fbed3-115">In the Document date reference field, select Modified date and time</span></span>
9. <span data-ttu-id="fbed3-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="fbed3-116">Click Save.</span></span>
10. <span data-ttu-id="fbed3-117">Fara á vinnusvæði Endurskoðunar > Uppsetning > endurskoðunarstefnur.</span><span class="sxs-lookup"><span data-stu-id="fbed3-117">Go to Audit workbench > Setup > Audit policies.</span></span>
11. <span data-ttu-id="fbed3-118">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="fbed3-118">Click New.</span></span>
12. <span data-ttu-id="fbed3-119">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="fbed3-119">In the Name field, type a value.</span></span>
13. <span data-ttu-id="fbed3-120">Útvíkka hlutann Fyrirtækjaregla.</span><span class="sxs-lookup"><span data-stu-id="fbed3-120">Expand the Policy organizations section.</span></span>
14. <span data-ttu-id="fbed3-121">Veljið 'Contoso Entertainment System USA', í trénu.</span><span class="sxs-lookup"><span data-stu-id="fbed3-121">In the tree, select 'Contoso Entertainment System USA'.</span></span>
15. <span data-ttu-id="fbed3-122">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="fbed3-122">Click Add.</span></span>
16. <span data-ttu-id="fbed3-123">Veljið "Contoso Consulting USA", í trénu.</span><span class="sxs-lookup"><span data-stu-id="fbed3-123">In the tree, select 'Contoso Consulting USA'.</span></span>
17. <span data-ttu-id="fbed3-124">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="fbed3-124">Click Add.</span></span>
18. <span data-ttu-id="fbed3-125">Veljið "Contoso Retail USA", í trénu.</span><span class="sxs-lookup"><span data-stu-id="fbed3-125">In the tree, select 'Contoso Retail USA'.</span></span>
19. <span data-ttu-id="fbed3-126">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="fbed3-126">Click Add.</span></span>
20. <span data-ttu-id="fbed3-127">Minnka hlutann Reglufyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="fbed3-127">Collapse the Policy organizations section.</span></span>
21. <span data-ttu-id="fbed3-128">Stækka liðnum stefnuregla.</span><span class="sxs-lookup"><span data-stu-id="fbed3-128">Expand the Policy rules section.</span></span>
22. <span data-ttu-id="fbed3-129">Finna og velja síðan Stefnuregluna sem var stofnuð áður, á listanum.</span><span class="sxs-lookup"><span data-stu-id="fbed3-129">In the list, find and select the Policy Rule that was created previously.</span></span>
23. <span data-ttu-id="fbed3-130">Smellt er á Stofna stefnureglu.</span><span class="sxs-lookup"><span data-stu-id="fbed3-130">Click Create policy rule.</span></span>
24. <span data-ttu-id="fbed3-131">Færa inn dagsetningu og tíma í svæðinu gildisdagsetningu.</span><span class="sxs-lookup"><span data-stu-id="fbed3-131">In the Effective date field, enter a date and time.</span></span>
25. <span data-ttu-id="fbed3-132">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="fbed3-132">Click Filter.</span></span>
26. <span data-ttu-id="fbed3-133">Á listanum, Velja línuna fyrir kostnaðartegund, og stillið upplýsing á Hótel.</span><span class="sxs-lookup"><span data-stu-id="fbed3-133">In the list, select the row for Expense category, and set the details to Hotel</span></span>
27. <span data-ttu-id="fbed3-134">Í reitinn Skilyrði skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="fbed3-134">In the Criteria field, enter or select a value.</span></span>
28. <span data-ttu-id="fbed3-135">Smellt er á flipann Samanlagt.</span><span class="sxs-lookup"><span data-stu-id="fbed3-135">Click the Aggregate tab.</span></span>
29. <span data-ttu-id="fbed3-136">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="fbed3-136">Click Add.</span></span>
30. <span data-ttu-id="fbed3-137">Á listanum, veljið gildi fyrir svæðið sem er færsluupphæð.</span><span class="sxs-lookup"><span data-stu-id="fbed3-137">In the list, select a field value of Transaction amount</span></span>
31. <span data-ttu-id="fbed3-138">Í reitinn Svæði skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="fbed3-138">In the Field field, enter or select a value.</span></span>
32. <span data-ttu-id="fbed3-139">Velja í svæðinu AggregateFunction, velja 'Samtölu'.</span><span class="sxs-lookup"><span data-stu-id="fbed3-139">In the AggregateFunction field, select 'Sum'.</span></span>
33. <span data-ttu-id="fbed3-140">Smellt er á flipa Flokka eftir.</span><span class="sxs-lookup"><span data-stu-id="fbed3-140">Click the Group by tab.</span></span>
34. <span data-ttu-id="fbed3-141">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="fbed3-141">Click Add.</span></span>
35. <span data-ttu-id="fbed3-142">Á listanum, veljið gildi fyrir Starfsmann </span><span class="sxs-lookup"><span data-stu-id="fbed3-142">In the list, select a value of Employee</span></span> 
36. <span data-ttu-id="fbed3-143">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="fbed3-143">Click Add.</span></span>
37. <span data-ttu-id="fbed3-144">Á listanum, veljið gildi fyrir kostnaðartegund</span><span class="sxs-lookup"><span data-stu-id="fbed3-144">In the list, select a value of Expense category</span></span>
38. <span data-ttu-id="fbed3-145">Í reitinn Svæði skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="fbed3-145">In the Field field, enter or select a value.</span></span>
39. <span data-ttu-id="fbed3-146">Smellt er á flipann Inniheldur.</span><span class="sxs-lookup"><span data-stu-id="fbed3-146">Click the Having tab.</span></span>
40. <span data-ttu-id="fbed3-147">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="fbed3-147">Click Add.</span></span>
41. <span data-ttu-id="fbed3-148">Veldu færsluupphæð</span><span class="sxs-lookup"><span data-stu-id="fbed3-148">Select Transaction amount</span></span>
42. <span data-ttu-id="fbed3-149">Í reitinn Svæði skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="fbed3-149">In the Field field, enter or select a value.</span></span>
43. <span data-ttu-id="fbed3-150">Velja í svæðinu AggregateFunction, velja 'Samtölu'.</span><span class="sxs-lookup"><span data-stu-id="fbed3-150">In the AggregateFunction field, select 'Sum'.</span></span>
44. <span data-ttu-id="fbed3-151">Í svæðinu Skilyrði, færðu inn'> 2000'.</span><span class="sxs-lookup"><span data-stu-id="fbed3-151">In the Criteria field, type '>2000'.</span></span>
45. <span data-ttu-id="fbed3-152">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="fbed3-152">Click OK.</span></span>
46. <span data-ttu-id="fbed3-153">Smellið á Prófun.</span><span class="sxs-lookup"><span data-stu-id="fbed3-153">Click Test.</span></span>
47. <span data-ttu-id="fbed3-154">Í reitnum upphafsdagur valins skjals, færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="fbed3-154">In the Document selection starting date field, enter a date and time.</span></span>
48. <span data-ttu-id="fbed3-155">Í reitnum lokadagsetning valins skjals, færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="fbed3-155">In the Document selection ending date field, enter a date and time.</span></span>
49. <span data-ttu-id="fbed3-156">Smella á Keyra prófun.</span><span class="sxs-lookup"><span data-stu-id="fbed3-156">Click Run test.</span></span>
50. <span data-ttu-id="fbed3-157">Á Aðgerðasvæðinu skal smellt á endurskoðunarreglu.</span><span class="sxs-lookup"><span data-stu-id="fbed3-157">On the Action Pane, click Audit policy.</span></span>
51. <span data-ttu-id="fbed3-158">Smellt er á Aukavalkosti.</span><span class="sxs-lookup"><span data-stu-id="fbed3-158">Click Additional options.</span></span>
52. <span data-ttu-id="fbed3-159">Í reitnum Upphafsdagsetning skal færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="fbed3-159">In the Starting date field, enter a date and time.</span></span>
53. <span data-ttu-id="fbed3-160">Í reitnum Lokadagsetning skal færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="fbed3-160">In the Ending date field, enter a date and time.</span></span>
54. <span data-ttu-id="fbed3-161">Smellt er á Runu.</span><span class="sxs-lookup"><span data-stu-id="fbed3-161">Click Batch.</span></span>
55. <span data-ttu-id="fbed3-162">Stækka útvíkkun á liðnum Keyra í bakgrunni.</span><span class="sxs-lookup"><span data-stu-id="fbed3-162">Expand the Run in the background section.</span></span>
56. <span data-ttu-id="fbed3-163">Veljið Já í svæðinu runuvinnsla.</span><span class="sxs-lookup"><span data-stu-id="fbed3-163">Select Yes in the Batch processing field.</span></span>
57. <span data-ttu-id="fbed3-164">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="fbed3-164">Click OK.</span></span>
58. <span data-ttu-id="fbed3-165">Fara á vinnusvæði Endurskoðunar > endurskoða mál</span><span class="sxs-lookup"><span data-stu-id="fbed3-165">Go to Audit workbench > Audit cases.</span></span>
59. <span data-ttu-id="fbed3-166">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="fbed3-166">In the list, find and select the desired record.</span></span>
60. <span data-ttu-id="fbed3-167">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="fbed3-167">In the list, click the link in the selected row.</span></span>
61. <span data-ttu-id="fbed3-168">Útvíkka hlutann Tengingar.</span><span class="sxs-lookup"><span data-stu-id="fbed3-168">Expand the Associations section.</span></span>
62. <span data-ttu-id="fbed3-169">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="fbed3-169">In the list, find and select the desired record.</span></span>
63. <span data-ttu-id="fbed3-170">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="fbed3-170">In the list, click the link in the selected row.</span></span>


