---
title: Stofna nafnakerfi afurðarnúmers fyrir skilgreind afurðarafbrigði
description: Þetta ferli sýnir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir skilgreind afurðarafbrigði og hvernig hægt er að tengja það við skilgreinanlegt afurðarsniðmát.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22aa4823fbf43b29a8fd9661645e8563c07e437d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844658"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="31479-103">Stofna nafnakerfi afurðarnúmers fyrir skilgreind afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="31479-103">Create a product number nomenclature for configured product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="31479-104">Þetta ferli sýnir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir skilgreind afurðarafbrigði og hvernig hægt er að tengja það við skilgreinanlegt afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="31479-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="31479-105">Þetta ferli sýnir einnig hvernig hægt er að byggja upp skilgreiningu nafnakerfis fyrir íhlut afbrigðalíkans afurðar.</span><span class="sxs-lookup"><span data-stu-id="31479-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="31479-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="31479-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="31479-107">Nýju afurðarnúmeri nafnakerfis er úthlutað á afurðarsniðmátið D0004.</span><span class="sxs-lookup"><span data-stu-id="31479-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="31479-108">Þetta verk myndi yfirleitt vera framkvæmt af hálfu vöruhönnuðar.</span><span class="sxs-lookup"><span data-stu-id="31479-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="31479-109">Stofnaðu Nafnakerfi afurðarnúmers</span><span class="sxs-lookup"><span data-stu-id="31479-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="31479-110">Smellið á Skilgreining afurðarafbrigðislíkans</span><span class="sxs-lookup"><span data-stu-id="31479-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="31479-111">Smelltu á Nafnakerfi afurðar.</span><span class="sxs-lookup"><span data-stu-id="31479-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="31479-112">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="31479-112">Click New.</span></span>
4. <span data-ttu-id="31479-113">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="31479-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="31479-114">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="31479-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="31479-115">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="31479-115">Click Add.</span></span>
7. <span data-ttu-id="31479-116">Smelltu á Númer afurðarsniðmáts.</span><span class="sxs-lookup"><span data-stu-id="31479-116">Click Product master number.</span></span>
8. <span data-ttu-id="31479-117">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="31479-117">Click Add.</span></span>
9. <span data-ttu-id="31479-118">Smelltu á Textafasta.</span><span class="sxs-lookup"><span data-stu-id="31479-118">Click Text constant.</span></span>
10. <span data-ttu-id="31479-119">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="31479-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="31479-120">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="31479-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="31479-121">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="31479-121">Click Add.</span></span>
13. <span data-ttu-id="31479-122">Smelltu á Skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="31479-122">Click Configuration.</span></span>
14. <span data-ttu-id="31479-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="31479-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="31479-124">Úthlutaðu nafnakerfi afurðarnúmers á afurðarsniðmát</span><span class="sxs-lookup"><span data-stu-id="31479-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="31479-125">Smelltu á Afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="31479-125">Click Product masters.</span></span>
2. <span data-ttu-id="31479-126">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="31479-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="31479-127">Til dæmis, sía reitinn Vörunúmer með gildið ‚D'.</span><span class="sxs-lookup"><span data-stu-id="31479-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="31479-128">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="31479-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="31479-129">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="31479-129">Click Edit.</span></span>
5. <span data-ttu-id="31479-130">Velja skal Já í reitnum Nota nafnakerfi.</span><span class="sxs-lookup"><span data-stu-id="31479-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="31479-131">Í reitnum Nafnakerfi afurðarafbrigðisnúmers skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="31479-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="31479-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="31479-132">Close the page.</span></span>
8. <span data-ttu-id="31479-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="31479-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="31479-134">Stofnaðu nafnakerfi fyrir íhlut afbrigðalíkans afurðar</span><span class="sxs-lookup"><span data-stu-id="31479-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="31479-135">Smella á Afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="31479-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="31479-136">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="31479-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="31479-137">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="31479-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="31479-138">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="31479-138">Click Edit.</span></span>
5. <span data-ttu-id="31479-139">Velja skal Já í reitnum Nota nafnakerfi skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="31479-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="31479-140">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="31479-140">Click Add.</span></span>
7. <span data-ttu-id="31479-141">Smelltu á Eigindargildi.</span><span class="sxs-lookup"><span data-stu-id="31479-141">Click Attribute value.</span></span>
8. <span data-ttu-id="31479-142">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="31479-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="31479-143">Sláið inn eða veldu gildi í reitnum Eigind.</span><span class="sxs-lookup"><span data-stu-id="31479-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="31479-144">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="31479-144">Click Add.</span></span>
11. <span data-ttu-id="31479-145">Smelltu á Textafasta.</span><span class="sxs-lookup"><span data-stu-id="31479-145">Click Text constant.</span></span>
12. <span data-ttu-id="31479-146">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="31479-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="31479-147">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="31479-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="31479-148">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="31479-148">Click Add.</span></span>
15. <span data-ttu-id="31479-149">Smelltu á Eigindargildi.</span><span class="sxs-lookup"><span data-stu-id="31479-149">Click Attribute value.</span></span>
16. <span data-ttu-id="31479-150">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="31479-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="31479-151">Sláið inn eða veldu gildi í reitnum Eigind.</span><span class="sxs-lookup"><span data-stu-id="31479-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="31479-152">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="31479-152">Click Add.</span></span>
19. <span data-ttu-id="31479-153">Smelltu á Textafasta.</span><span class="sxs-lookup"><span data-stu-id="31479-153">Click Text constant.</span></span>
20. <span data-ttu-id="31479-154">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="31479-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="31479-155">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="31479-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="31479-156">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="31479-156">Click Add.</span></span>
23. <span data-ttu-id="31479-157">Smelltu á Eigindargildi.</span><span class="sxs-lookup"><span data-stu-id="31479-157">Click Attribute value.</span></span>
24. <span data-ttu-id="31479-158">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="31479-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="31479-159">Sláið inn eða veldu gildi í reitnum Eigind.</span><span class="sxs-lookup"><span data-stu-id="31479-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="31479-160">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="31479-160">Click Add.</span></span>
27. <span data-ttu-id="31479-161">Smelltu á Textafasta.</span><span class="sxs-lookup"><span data-stu-id="31479-161">Click Text constant.</span></span>
28. <span data-ttu-id="31479-162">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="31479-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="31479-163">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="31479-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="31479-164">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="31479-164">Click Add.</span></span>
31. <span data-ttu-id="31479-165">Smelltu á Eigindargildi.</span><span class="sxs-lookup"><span data-stu-id="31479-165">Click Attribute value.</span></span>
32. <span data-ttu-id="31479-166">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="31479-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="31479-167">Sláið inn eða veldu gildi í reitnum Eigind.</span><span class="sxs-lookup"><span data-stu-id="31479-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="31479-168">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="31479-168">Click Add.</span></span>
35. <span data-ttu-id="31479-169">Smelltu á Textafasta.</span><span class="sxs-lookup"><span data-stu-id="31479-169">Click Text constant.</span></span>
36. <span data-ttu-id="31479-170">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="31479-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="31479-171">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="31479-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="31479-172">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="31479-172">Click Add.</span></span>
39. <span data-ttu-id="31479-173">Smelltu á Gildi númeraraðar.</span><span class="sxs-lookup"><span data-stu-id="31479-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="31479-174">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="31479-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="31479-175">Sláið inn eða veldu gildi í reitnum Númeraröð.</span><span class="sxs-lookup"><span data-stu-id="31479-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="31479-176">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="31479-176">Close the page.</span></span>
43. <span data-ttu-id="31479-177">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="31479-177">Close the page.</span></span>
44. <span data-ttu-id="31479-178">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="31479-178">Close the page.</span></span>

