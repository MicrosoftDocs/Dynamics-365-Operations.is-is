--- 
title: "Stofna nafnakerfi afurðarnúmers fyrir skilgreind afurðarafbrigði"
description: "Þetta ferli sýnir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir skilgreind afurðarafbrigði og hvernig hægt er að tengja það við skilgreinanlegt afurðarsniðmát."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 800afdf075f0675185514158f3b712a0fe7675e3
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="58fef-103">Stofna nafnakerfi afurðarnúmers fyrir skilgreind afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="58fef-103">Create a product number nomenclature for configured product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="58fef-104">Þetta ferli sýnir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir skilgreind afurðarafbrigði og hvernig hægt er að tengja það við skilgreinanlegt afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="58fef-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="58fef-105">Þetta ferli sýnir einnig hvernig hægt er að byggja upp skilgreiningu nafnakerfis fyrir íhlut afbrigðalíkans afurðar.</span><span class="sxs-lookup"><span data-stu-id="58fef-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="58fef-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="58fef-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="58fef-107">Nýju afurðarnúmeri nafnakerfis er úthlutað á afurðarsniðmátið D0004.</span><span class="sxs-lookup"><span data-stu-id="58fef-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="58fef-108">Þetta verk myndi yfirleitt vera framkvæmt af hálfu vöruhönnuðar.</span><span class="sxs-lookup"><span data-stu-id="58fef-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="58fef-109">Stofnaðu Nafnakerfi afurðarnúmers</span><span class="sxs-lookup"><span data-stu-id="58fef-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="58fef-110">Smellið á Skilgreining afurðarafbrigðislíkans</span><span class="sxs-lookup"><span data-stu-id="58fef-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="58fef-111">Smelltu á Nafnakerfi afurðar.</span><span class="sxs-lookup"><span data-stu-id="58fef-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="58fef-112">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="58fef-112">Click New.</span></span>
4. <span data-ttu-id="58fef-113">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="58fef-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="58fef-114">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="58fef-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="58fef-115">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="58fef-115">Click Add.</span></span>
7. <span data-ttu-id="58fef-116">Smelltu á Númer afurðarsniðmáts.</span><span class="sxs-lookup"><span data-stu-id="58fef-116">Click Product master number.</span></span>
8. <span data-ttu-id="58fef-117">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="58fef-117">Click Add.</span></span>
9. <span data-ttu-id="58fef-118">Smelltu á Textafasta.</span><span class="sxs-lookup"><span data-stu-id="58fef-118">Click Text constant.</span></span>
10. <span data-ttu-id="58fef-119">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="58fef-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="58fef-120">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="58fef-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="58fef-121">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="58fef-121">Click Add.</span></span>
13. <span data-ttu-id="58fef-122">Smelltu á Skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="58fef-122">Click Configuration.</span></span>
14. <span data-ttu-id="58fef-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="58fef-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="58fef-124">Úthlutaðu nafnakerfi afurðarnúmers á afurðarsniðmát</span><span class="sxs-lookup"><span data-stu-id="58fef-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="58fef-125">Smelltu á Afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="58fef-125">Click Product masters.</span></span>
2. <span data-ttu-id="58fef-126">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="58fef-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="58fef-127">Til dæmis, sía reitinn Vörunúmer með gildið ‚D'.</span><span class="sxs-lookup"><span data-stu-id="58fef-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="58fef-128">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="58fef-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="58fef-129">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="58fef-129">Click Edit.</span></span>
5. <span data-ttu-id="58fef-130">Velja skal Já í reitnum Nota nafnakerfi.</span><span class="sxs-lookup"><span data-stu-id="58fef-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="58fef-131">Í reitnum Nafnakerfi afurðarafbrigðisnúmers skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="58fef-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="58fef-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="58fef-132">Close the page.</span></span>
8. <span data-ttu-id="58fef-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="58fef-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="58fef-134">Stofnaðu nafnakerfi fyrir íhlut afbrigðalíkans afurðar</span><span class="sxs-lookup"><span data-stu-id="58fef-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="58fef-135">Smella á Afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="58fef-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="58fef-136">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="58fef-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="58fef-137">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="58fef-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="58fef-138">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="58fef-138">Click Edit.</span></span>
5. <span data-ttu-id="58fef-139">Velja skal Já í reitnum Nota nafnakerfi skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="58fef-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="58fef-140">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="58fef-140">Click Add.</span></span>
7. <span data-ttu-id="58fef-141">Smelltu á Eigindargildi.</span><span class="sxs-lookup"><span data-stu-id="58fef-141">Click Attribute value.</span></span>
8. <span data-ttu-id="58fef-142">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="58fef-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="58fef-143">Sláið inn eða veldu gildi í reitnum Eigind.</span><span class="sxs-lookup"><span data-stu-id="58fef-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="58fef-144">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="58fef-144">Click Add.</span></span>
11. <span data-ttu-id="58fef-145">Smelltu á Textafasta.</span><span class="sxs-lookup"><span data-stu-id="58fef-145">Click Text constant.</span></span>
12. <span data-ttu-id="58fef-146">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="58fef-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="58fef-147">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="58fef-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="58fef-148">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="58fef-148">Click Add.</span></span>
15. <span data-ttu-id="58fef-149">Smelltu á Eigindargildi.</span><span class="sxs-lookup"><span data-stu-id="58fef-149">Click Attribute value.</span></span>
16. <span data-ttu-id="58fef-150">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="58fef-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="58fef-151">Sláið inn eða veldu gildi í reitnum Eigind.</span><span class="sxs-lookup"><span data-stu-id="58fef-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="58fef-152">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="58fef-152">Click Add.</span></span>
19. <span data-ttu-id="58fef-153">Smelltu á Textafasta.</span><span class="sxs-lookup"><span data-stu-id="58fef-153">Click Text constant.</span></span>
20. <span data-ttu-id="58fef-154">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="58fef-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="58fef-155">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="58fef-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="58fef-156">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="58fef-156">Click Add.</span></span>
23. <span data-ttu-id="58fef-157">Smelltu á Eigindargildi.</span><span class="sxs-lookup"><span data-stu-id="58fef-157">Click Attribute value.</span></span>
24. <span data-ttu-id="58fef-158">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="58fef-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="58fef-159">Sláið inn eða veldu gildi í reitnum Eigind.</span><span class="sxs-lookup"><span data-stu-id="58fef-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="58fef-160">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="58fef-160">Click Add.</span></span>
27. <span data-ttu-id="58fef-161">Smelltu á Textafasta.</span><span class="sxs-lookup"><span data-stu-id="58fef-161">Click Text constant.</span></span>
28. <span data-ttu-id="58fef-162">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="58fef-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="58fef-163">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="58fef-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="58fef-164">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="58fef-164">Click Add.</span></span>
31. <span data-ttu-id="58fef-165">Smelltu á Eigindargildi.</span><span class="sxs-lookup"><span data-stu-id="58fef-165">Click Attribute value.</span></span>
32. <span data-ttu-id="58fef-166">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="58fef-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="58fef-167">Sláið inn eða veldu gildi í reitnum Eigind.</span><span class="sxs-lookup"><span data-stu-id="58fef-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="58fef-168">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="58fef-168">Click Add.</span></span>
35. <span data-ttu-id="58fef-169">Smelltu á Textafasta.</span><span class="sxs-lookup"><span data-stu-id="58fef-169">Click Text constant.</span></span>
36. <span data-ttu-id="58fef-170">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="58fef-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="58fef-171">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="58fef-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="58fef-172">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="58fef-172">Click Add.</span></span>
39. <span data-ttu-id="58fef-173">Smelltu á Gildi númeraraðar.</span><span class="sxs-lookup"><span data-stu-id="58fef-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="58fef-174">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="58fef-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="58fef-175">Sláið inn eða veldu gildi í reitnum Númeraröð.</span><span class="sxs-lookup"><span data-stu-id="58fef-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="58fef-176">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="58fef-176">Close the page.</span></span>
43. <span data-ttu-id="58fef-177">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="58fef-177">Close the page.</span></span>
44. <span data-ttu-id="58fef-178">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="58fef-178">Close the page.</span></span>


