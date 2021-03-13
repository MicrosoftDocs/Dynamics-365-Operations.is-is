---
title: Skilgreina endurskoðunarstefnur fyrir upprunaskjöl
description: Þetta efni útskýrir hvernig á að setja upp og keyra reglur endurskoðunarstefnu.
author: panolte
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e020a9e82ff18055e40e3e0ddc7bbed1068c886c
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5021430"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="82e0e-103">Skilgreina endurskoðunarstefnur fyrir upprunaskjöl</span><span class="sxs-lookup"><span data-stu-id="82e0e-103">Define audit policies for source documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="82e0e-104">Þetta efni útskýrir hvernig á að setja upp og keyra reglur endurskoðunarstefnu.</span><span class="sxs-lookup"><span data-stu-id="82e0e-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="82e0e-105">Dæmi notar kostnaðarskýrslur með hótel kostnaðargerð.</span><span class="sxs-lookup"><span data-stu-id="82e0e-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="82e0e-106">Þessi aðferð notar sýnigögn USMF fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="82e0e-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="82e0e-107">Endurskoðandahlutverkið inniheldur réttar heimildir til að framkvæma þessi verk.</span><span class="sxs-lookup"><span data-stu-id="82e0e-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="82e0e-108">Í skoðunarrúðunni ferðu í **Einingar > Vinnusvæði endurskoðunar > Uppsetning > Stefnureglugerð**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="82e0e-109">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-109">Select **New**.</span></span>
3. <span data-ttu-id="82e0e-110">Í reitinn **Heiti reglu** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="82e0e-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="82e0e-111">Í reitinn **Lýsing** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="82e0e-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="82e0e-112">Í reitnum **Heiti fyrirspurnar** velurðu **Kostnaðarskýrslulínu**</span><span class="sxs-lookup"><span data-stu-id="82e0e-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="82e0e-113">í reitnum **Gerð fyrirspurnar** skal velja **Samanlagt**</span><span class="sxs-lookup"><span data-stu-id="82e0e-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="82e0e-114">Í reitnum **Lögaðili** skal velja **Lögaðila**</span><span class="sxs-lookup"><span data-stu-id="82e0e-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="82e0e-115">Í reitnum **Tilvísun í dagsetningu skjals** velurðu **Breytt dagsetning og tími**</span><span class="sxs-lookup"><span data-stu-id="82e0e-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="82e0e-116">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-116">Select **Save**.</span></span>
10. <span data-ttu-id="82e0e-117">Í skoðunarrúðunni ferðu í **Einingar > Vinnusvæði endurskoðunar > Uppsetning > Endurskoðunarstefnur**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="82e0e-118">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-118">Select **New**.</span></span>
12. <span data-ttu-id="82e0e-119">Í reitinn **Heiti** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="82e0e-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="82e0e-120">Útvíkkaðu kaflann **Fyrirtækjaregla**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="82e0e-121">Veljið **Contoso Entertainment System USA** í trénu og síðan **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="82e0e-122">Veljið **Contoso Consulting USA** í trénu og síðan **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="82e0e-123">Veljið **Contoso Retail USA** í trénu og síðan **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="82e0e-124">Minnkaðu hlutann **Fyrirtækjaregla**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="82e0e-125">Útvíkkaðu hlutann **Stefnuregla**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="82e0e-126">Finna og velja síðan Stefnuregluna sem var stofnuð áður, á listanum.</span><span class="sxs-lookup"><span data-stu-id="82e0e-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="82e0e-127">Veldu **stefnureglu**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="82e0e-128">Í retinum **Gildisdagsetningu** færirðu inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="82e0e-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="82e0e-129">Velja **Síu**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-129">Select **Filter**.</span></span>
23. <span data-ttu-id="82e0e-130">Á listanum skal velja línuna fyrir **Kostnaðartegund** og stilla upplýsingarnar á **Hótel**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="82e0e-131">Í reitinn **Skilyrði** skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="82e0e-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="82e0e-132">Veldu flipann **Samanlagt**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="82e0e-133">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-133">Select **Add**.</span></span>
27. <span data-ttu-id="82e0e-134">Á listanum velurðu reitagildi sem er **Færsluupphæð**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="82e0e-135">Í reitinn **Reitur** skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="82e0e-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="82e0e-136">Í reitnum **AggregateFunction** velurðu **Samtölu**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="82e0e-137">Veldu flipann **Flokka eftir**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="82e0e-138">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-138">Select **Add**.</span></span>
32. <span data-ttu-id="82e0e-139">Á listanum velurðu gildi fyrir **Starfsmann**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="82e0e-140">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-140">Select **Add**.</span></span>
34. <span data-ttu-id="82e0e-141">Á listanum velurðu gildi fyrir **Kostnaðartegund**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="82e0e-142">Í reitinn **Reitur** skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="82e0e-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="82e0e-143">Velja flipann **Með**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="82e0e-144">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-144">Select **Add**.</span></span>
38. <span data-ttu-id="82e0e-145">Veldu **Færsluupphæð**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="82e0e-146">Í reitinn **Reitur** skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="82e0e-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="82e0e-147">Í reitnum **AggregateFunction** velurðu **Samtölu**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="82e0e-148">Í svæðinu **Skilyrði** skaltu færa inn `>2000`.</span><span class="sxs-lookup"><span data-stu-id="82e0e-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="82e0e-149">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-149">Select **OK**.</span></span>
43. <span data-ttu-id="82e0e-150">Veldu **Prófa**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-150">Select **Test**.</span></span>
44. <span data-ttu-id="82e0e-151">Í reitnum **Upphafsdagsetning skjalavals** skaltu færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="82e0e-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="82e0e-152">Í reitnum **Lokadagsetning skjalavals** skal færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="82e0e-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="82e0e-153">Veldu **Keyra prófun**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-153">Select **Run test**.</span></span>
47. <span data-ttu-id="82e0e-154">Á Aðgerðasvæðinu skal velja **Endurskoðunarstefnu**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="82e0e-155">Veldu **Aukavalkosti**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="82e0e-156">Í reitinn **Upphafsdagsetning** skal færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="82e0e-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="82e0e-157">Í reitinn **Lokadagsetning** skal færa inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="82e0e-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="82e0e-158">Veldu **Runu**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-158">Select **Batch**.</span></span>
52. <span data-ttu-id="82e0e-159">Stækkaðu hlutann **Keyra í bakgrunni**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="82e0e-160">Veldu **Já** í reitnum **Runuvinnsla**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="82e0e-161">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-161">Select **OK**.</span></span>
55. <span data-ttu-id="82e0e-162">Í skoðunarrúðunni ferðu í **Einingar > Vinnusvæði endurskoðunar > Endurskoða mál**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="82e0e-163">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="82e0e-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="82e0e-164">Útvíkkaður hlutann **Tengingar**.</span><span class="sxs-lookup"><span data-stu-id="82e0e-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="82e0e-165">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="82e0e-165">In the list, find and select the desired record.</span></span>

