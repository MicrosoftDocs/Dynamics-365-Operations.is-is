---
title: Stofna nafnakerfi afurðarnúmers fyrir skilgreind afurðarafbrigði
description: Þetta ferli sýnir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir skilgreind afurðarafbrigði og hvernig hægt er að tengja það við skilgreinanlegt afurðarsniðmát.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e52b7a5aff3e86e845484e1e84b4003cc4a52c95
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992371"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="1f9e9-103">Stofna nafnakerfi afurðarnúmers fyrir skilgreind afurðarafbrigði</span><span class="sxs-lookup"><span data-stu-id="1f9e9-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1f9e9-104">Þetta ferli sýnir hvernig á að setja inn nafnakerfi afurðarnúmers fyrir skilgreind afurðarafbrigði og hvernig hægt er að tengja það við skilgreinanlegt afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="1f9e9-105">Þetta ferli sýnir einnig hvernig hægt er að byggja upp skilgreiningu nafnakerfis fyrir íhlut afbrigðalíkans afurðar.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="1f9e9-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="1f9e9-107">Nýju afurðarnúmeri nafnakerfis er úthlutað á afurðarsniðmátið D0004.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="1f9e9-108">Þetta verk myndi yfirleitt vera framkvæmt af hálfu vöruhönnuðar.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="1f9e9-109">Stofnaðu Nafnakerfi afurðarnúmers</span><span class="sxs-lookup"><span data-stu-id="1f9e9-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="1f9e9-110">Smellið á Skilgreining afurðarafbrigðislíkans</span><span class="sxs-lookup"><span data-stu-id="1f9e9-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="1f9e9-111">Smelltu á Nafnakerfi afurðar.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="1f9e9-112">Smellt er á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-112">Click New.</span></span>
4. <span data-ttu-id="1f9e9-113">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="1f9e9-114">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="1f9e9-115">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-115">Click Add.</span></span>
7. <span data-ttu-id="1f9e9-116">Smelltu á Númer afurðarsniðmáts.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-116">Click Product master number.</span></span>
8. <span data-ttu-id="1f9e9-117">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-117">Click Add.</span></span>
9. <span data-ttu-id="1f9e9-118">Smelltu á Textafasta.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-118">Click Text constant.</span></span>
10. <span data-ttu-id="1f9e9-119">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="1f9e9-120">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="1f9e9-121">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-121">Click Add.</span></span>
13. <span data-ttu-id="1f9e9-122">Smelltu á Skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-122">Click Configuration.</span></span>
14. <span data-ttu-id="1f9e9-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="1f9e9-124">Úthlutaðu nafnakerfi afurðarnúmers á afurðarsniðmát</span><span class="sxs-lookup"><span data-stu-id="1f9e9-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="1f9e9-125">Smelltu á Afurðarsniðmát.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-125">Click Product masters.</span></span>
2. <span data-ttu-id="1f9e9-126">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="1f9e9-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="1f9e9-127">Til dæmis, sía reitinn Vörunúmer með gildið ‚D'.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="1f9e9-128">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1f9e9-129">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-129">Click Edit.</span></span>
5. <span data-ttu-id="1f9e9-130">Velja skal Já í reitnum Nota nafnakerfi.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="1f9e9-131">Í reitnum Nafnakerfi afurðarafbrigðisnúmers skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="1f9e9-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-132">Close the page.</span></span>
8. <span data-ttu-id="1f9e9-133">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="1f9e9-134">Stofnaðu nafnakerfi fyrir íhlut afbrigðalíkans afurðar</span><span class="sxs-lookup"><span data-stu-id="1f9e9-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="1f9e9-135">Smella á Afbrigðalíkan afurðar</span><span class="sxs-lookup"><span data-stu-id="1f9e9-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="1f9e9-136">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="1f9e9-137">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="1f9e9-138">Smella á Breyta.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-138">Click Edit.</span></span>
5. <span data-ttu-id="1f9e9-139">Velja skal Já í reitnum Nota nafnakerfi skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="1f9e9-140">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-140">Click Add.</span></span>
7. <span data-ttu-id="1f9e9-141">Smelltu á Eigindargildi.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-141">Click Attribute value.</span></span>
8. <span data-ttu-id="1f9e9-142">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="1f9e9-143">Sláið inn eða veldu gildi í reitnum Eigind.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="1f9e9-144">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-144">Click Add.</span></span>
11. <span data-ttu-id="1f9e9-145">Smelltu á Textafasta.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-145">Click Text constant.</span></span>
12. <span data-ttu-id="1f9e9-146">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="1f9e9-147">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="1f9e9-148">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-148">Click Add.</span></span>
15. <span data-ttu-id="1f9e9-149">Smelltu á Eigindargildi.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-149">Click Attribute value.</span></span>
16. <span data-ttu-id="1f9e9-150">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="1f9e9-151">Sláið inn eða veldu gildi í reitnum Eigind.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="1f9e9-152">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-152">Click Add.</span></span>
19. <span data-ttu-id="1f9e9-153">Smelltu á Textafasta.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-153">Click Text constant.</span></span>
20. <span data-ttu-id="1f9e9-154">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="1f9e9-155">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="1f9e9-156">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-156">Click Add.</span></span>
23. <span data-ttu-id="1f9e9-157">Smelltu á Eigindargildi.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-157">Click Attribute value.</span></span>
24. <span data-ttu-id="1f9e9-158">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="1f9e9-159">Sláið inn eða veldu gildi í reitnum Eigind.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="1f9e9-160">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-160">Click Add.</span></span>
27. <span data-ttu-id="1f9e9-161">Smelltu á Textafasta.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-161">Click Text constant.</span></span>
28. <span data-ttu-id="1f9e9-162">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="1f9e9-163">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="1f9e9-164">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-164">Click Add.</span></span>
31. <span data-ttu-id="1f9e9-165">Smelltu á Eigindargildi.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-165">Click Attribute value.</span></span>
32. <span data-ttu-id="1f9e9-166">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="1f9e9-167">Sláið inn eða veldu gildi í reitnum Eigind.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="1f9e9-168">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-168">Click Add.</span></span>
35. <span data-ttu-id="1f9e9-169">Smelltu á Textafasta.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-169">Click Text constant.</span></span>
36. <span data-ttu-id="1f9e9-170">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="1f9e9-171">Í reitinn Texti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="1f9e9-172">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-172">Click Add.</span></span>
39. <span data-ttu-id="1f9e9-173">Smelltu á Gildi númeraraðar.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="1f9e9-174">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="1f9e9-175">Sláið inn eða veldu gildi í reitnum Númeraröð.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="1f9e9-176">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-176">Close the page.</span></span>
43. <span data-ttu-id="1f9e9-177">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-177">Close the page.</span></span>
44. <span data-ttu-id="1f9e9-178">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1f9e9-178">Close the page.</span></span>

