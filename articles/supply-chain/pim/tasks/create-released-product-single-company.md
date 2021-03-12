---
title: Stofna útgefna afurð fyrir stakt fyrirtæki
description: Þetta ferli fer í gegnum hvernig skal stofna eina losaða afurð í einni einingu lögaðila.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, UnitOfMeasureLookup, DimensionLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 79d5252d950cd83dfd1307ffb661948405102593
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4999682"
---
# <a name="create-a-released-product-for-a-single-company"></a><span data-ttu-id="821f8-103">Stofna útgefna afurð fyrir stakt fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="821f8-103">Create a released product for a single company</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="821f8-104">Þetta ferli fer í gegnum hvernig skal stofna eina losaða afurð í einni einingu lögaðila.</span><span class="sxs-lookup"><span data-stu-id="821f8-104">This procedure walks through how to create a single released product in the context of a single legal unit.</span></span> <span data-ttu-id="821f8-105">Eftir að útgefin afurð er stofnuð er hún strax tiltæk í þessari einingu aðeins.</span><span class="sxs-lookup"><span data-stu-id="821f8-105">After the released product is created,  it's immediately available in this unit only.</span></span> <span data-ttu-id="821f8-106">Þú getur farið í gegnum þetta ferli í sýnifyrirtækinu USMF.</span><span class="sxs-lookup"><span data-stu-id="821f8-106">You can walk through this procedure in demo data company USMF.</span></span> <span data-ttu-id="821f8-107">Þetta verk er yfirleitt framkvæmd af vöruhönnuður.</span><span class="sxs-lookup"><span data-stu-id="821f8-107">This task is usually performed by a product designer.</span></span>


## <a name="create-a-released-product"></a><span data-ttu-id="821f8-108">Stofna útgefna afurð</span><span class="sxs-lookup"><span data-stu-id="821f8-108">Create a released product</span></span>
1. <span data-ttu-id="821f8-109">Farðu í Losaðar afurðir.</span><span class="sxs-lookup"><span data-stu-id="821f8-109">Go to Released products.</span></span>
2. <span data-ttu-id="821f8-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="821f8-110">Click New.</span></span>
3. <span data-ttu-id="821f8-111">Í reitinn Afurðarnúmer skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="821f8-111">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="821f8-112">Ef afurðarnúmer er ekki sjálfkrafa slegið inn í reitur Afurðarnúmer skal slá inn einkvæmt afurðarnúmer.</span><span class="sxs-lookup"><span data-stu-id="821f8-112">If a product number is not automatically entered in the Product number field, type a unique product number.</span></span> <span data-ttu-id="821f8-113">Þetta skref er aðeins áskilið ef engin númeraröð hefur verið sett upp fyrir afurðarnúmer.</span><span class="sxs-lookup"><span data-stu-id="821f8-113">This step is only  required if no number sequence has been set up for product numbers.</span></span>  
4. <span data-ttu-id="821f8-114">Sláið inn gildi í reitinn Afurðarheiti.</span><span class="sxs-lookup"><span data-stu-id="821f8-114">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="821f8-115">Afurðarheiti er sjálfgefið á leitarnafn.</span><span class="sxs-lookup"><span data-stu-id="821f8-115">The Product name is defaulted to the search name.</span></span> <span data-ttu-id="821f8-116">Ef þörf krefur, er hægt að velja að breyta leitarnafninu.</span><span class="sxs-lookup"><span data-stu-id="821f8-116">If needed, you can select to change the search name.</span></span>  
5. <span data-ttu-id="821f8-117">Í reitnum Vörulíkanaflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="821f8-117">In the Item model group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="821f8-118">Vörulíkanaflokkar innihalda stillingar sem ákvarða hvernig vörum er stýrt og þær meðhöndlaðar á inn- og úthreyfingum.</span><span class="sxs-lookup"><span data-stu-id="821f8-118">The item model groups contain settings that determine how items are controlled and handled on item receipts and issues.</span></span> <span data-ttu-id="821f8-119">Stillingarnar ákvarða einnig hvernig notkun á vörum er reikna út.</span><span class="sxs-lookup"><span data-stu-id="821f8-119">The settings also determine how the consumption of items are calculated.</span></span>  
6. <span data-ttu-id="821f8-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="821f8-120">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="821f8-121">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="821f8-121">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="821f8-122">Í reitnum Vöruflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="821f8-122">In the Item group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="821f8-123">Notið þessa skjámynd til að stjórna birgðum með því að deila vörum í birgðum í flokka sem byggðir eru á vörueinkennum.</span><span class="sxs-lookup"><span data-stu-id="821f8-123">Item groups are used to manage inventory by dividing inventory items into groups based on item characteristics.</span></span> <span data-ttu-id="821f8-124">Til að stjórna hvernig upplýsingar eru bókaðar í aðallykla, er t.d. hægt að stofna röð af mismunandi vöruflokkum sem eru tengdar við tiltekna aðallykla.</span><span class="sxs-lookup"><span data-stu-id="821f8-124">For example, to manage how information is posted to main accounts, you can create a series of different item groups that are associated with specific main accounts.</span></span> <span data-ttu-id="821f8-125">Þetta gerir kleift að rekja birgðavirði fyrir vörur á mismunandi stigum.</span><span class="sxs-lookup"><span data-stu-id="821f8-125">This lets you track the inventory value of items at different stages.</span></span>  
9. <span data-ttu-id="821f8-126">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="821f8-126">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="821f8-127">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="821f8-127">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="821f8-128">Í reitnum Geymsluvíddarflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="821f8-128">In the Storage dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="821f8-129">Geymsluvíddir stjórna því hvernig vörur eru geymdar og teknar út af lager.</span><span class="sxs-lookup"><span data-stu-id="821f8-129">The storage dimensions help you control how items are stored and taken from inventory.</span></span> <span data-ttu-id="821f8-130">Til dæmis getur geymsluvídd verið Svæði og vöruhús</span><span class="sxs-lookup"><span data-stu-id="821f8-130">For example, a storage dimension can be Site and Warehouse.</span></span>  
12. <span data-ttu-id="821f8-131">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="821f8-131">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="821f8-132">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="821f8-132">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="821f8-133">Í reitnum Rakningarvíddarflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="821f8-133">In the Tracking dimension group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="821f8-134">Rakningarvíddarflokkur ákvarðar hvaða víddaflokkar er hægt að bæta við afurð.</span><span class="sxs-lookup"><span data-stu-id="821f8-134">The tracking dimension group determines which tracking dimensions you can add to a product.</span></span> <span data-ttu-id="821f8-135">Til dæmis má nota rununúmer og raðnúmer til að rekja birgðavörur.</span><span class="sxs-lookup"><span data-stu-id="821f8-135">For example, the batch number and serial number are used to track inventory items.</span></span>  
15. <span data-ttu-id="821f8-136">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="821f8-136">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="821f8-137">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="821f8-137">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="821f8-138">Í reitnum Birgðaeining skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="821f8-138">In the Inventory unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="821f8-139">Birgðaeining ákvarðar hvernig afurð er magnbundin þegar hún er geymd á lager.</span><span class="sxs-lookup"><span data-stu-id="821f8-139">The inventory unit determines how the product is quantified when it's stored in inventory.</span></span>  
18. <span data-ttu-id="821f8-140">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="821f8-140">In the list, find and select the desired record.</span></span>
19. <span data-ttu-id="821f8-141">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="821f8-141">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="821f8-142">Í reitnum Innkaupaeining skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="821f8-142">In the Purchase unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="821f8-143">Innkaupaeining ákvarðar hvernig afurð er magnbundin þegar hún er keypt af lánardrottni.</span><span class="sxs-lookup"><span data-stu-id="821f8-143">The purchase unit determines how the product is quantified when it's purchased from a vendor.</span></span>  
21. <span data-ttu-id="821f8-144">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="821f8-144">In the list, find and select the desired record.</span></span>
22. <span data-ttu-id="821f8-145">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="821f8-145">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="821f8-146">Í reitnum Sölueining skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="821f8-146">In the Sales unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="821f8-147">Innkaupaeining ákvarðar hvernig afurð er magnbundin þegar hún er seld til viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="821f8-147">The sales unit determines how the product is quantified when it's sold to a customer.</span></span>  
24. <span data-ttu-id="821f8-148">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="821f8-148">In the list, find and select the desired record.</span></span>
25. <span data-ttu-id="821f8-149">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="821f8-149">In the list, click the link in the selected row.</span></span>
26. <span data-ttu-id="821f8-150">Í reitnum Uppskriftaeining skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="821f8-150">In the BOM unit field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="821f8-151">Uppskriftareining ákvarðar hvernig afurð er magnbundin þegar hún er höfð með í uppskrift.</span><span class="sxs-lookup"><span data-stu-id="821f8-151">The BOM unit determines how the product is quantified when including it in a bill of materials (BOM).</span></span>  
27. <span data-ttu-id="821f8-152">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="821f8-152">In the list, find and select the desired record.</span></span>
28. <span data-ttu-id="821f8-153">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="821f8-153">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="821f8-154">Í reitnum VSK-flokkur vöru skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="821f8-154">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="821f8-155">VSK-flokkur vöru í VSK-flokknum ákvarðar hvernig virðisaukaskattur er reikna út hverja vöru.</span><span class="sxs-lookup"><span data-stu-id="821f8-155">The item sales tax group in the Sales taxation group determines how sales tax is calculated for each item.</span></span>  
30. <span data-ttu-id="821f8-156">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="821f8-156">In the list, find and select the desired record.</span></span>
31. <span data-ttu-id="821f8-157">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="821f8-157">In the list, click the link in the selected row.</span></span>
32. <span data-ttu-id="821f8-158">Í reitnum VSK-flokkur vöru skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="821f8-158">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="821f8-159">VSK-flokkur vöru í innkaupasköttunarflokknum ákvarðar hvernig innkaupaskattur er reikna út fyrir hverja vöru.</span><span class="sxs-lookup"><span data-stu-id="821f8-159">The item sales tax group in the Purchase taxation group determines how purchase tax is calculated for each item.</span></span>  
33. <span data-ttu-id="821f8-160">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="821f8-160">In the list, find and select the desired record.</span></span>
34. <span data-ttu-id="821f8-161">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="821f8-161">In the list, click the link in the selected row.</span></span>
35. <span data-ttu-id="821f8-162">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="821f8-162">Click OK.</span></span>

## <a name="add-product-characteristics"></a><span data-ttu-id="821f8-163">Bæta við eiginleika afurðar</span><span class="sxs-lookup"><span data-stu-id="821f8-163">Add product characteristics</span></span>
1. <span data-ttu-id="821f8-164">Stækka eða fella saman hlutann Stjórna birgðum.</span><span class="sxs-lookup"><span data-stu-id="821f8-164">Expand or collapse the Manage inventory section.</span></span>
2. <span data-ttu-id="821f8-165">Í reitinn Nettóþyngd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="821f8-165">In the Net weight field, enter a number.</span></span>
3. <span data-ttu-id="821f8-166">Í reitinn Umbúðaþyngd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="821f8-166">In the Tare weight field, enter a number.</span></span>
4. <span data-ttu-id="821f8-167">Í reitinn Brúttódýpt skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="821f8-167">In the Gross depth field, enter a number.</span></span>
5. <span data-ttu-id="821f8-168">Í reitinn Brúttólengd skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="821f8-168">In the Gross width field, enter a number.</span></span>
6. <span data-ttu-id="821f8-169">Í reitinn Brúttóhæð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="821f8-169">In the Gross height field, enter a number.</span></span>
7. <span data-ttu-id="821f8-170">Í reitinn Magn skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="821f8-170">In the Volume field, enter a number.</span></span>

## <a name="add-financial-dimensions"></a><span data-ttu-id="821f8-171">Bæta við fjárhagsvíddum</span><span class="sxs-lookup"><span data-stu-id="821f8-171">Add financial dimensions</span></span>
1. <span data-ttu-id="821f8-172">Útvíkka eða draga saman hluta fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="821f8-172">Expand or collapse the Financial dimensions section.</span></span>
2. <span data-ttu-id="821f8-173">Í reitnum BusinessUnit skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="821f8-173">In the BusinessUnit field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="821f8-174">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="821f8-174">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="821f8-175">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="821f8-175">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="821f8-176">Í reitnum CostCenter skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="821f8-176">In the CostCenter field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="821f8-177">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="821f8-177">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="821f8-178">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="821f8-178">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="821f8-179">Í reitnum Deild skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="821f8-179">In the Department field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="821f8-180">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="821f8-180">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="821f8-181">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="821f8-181">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="821f8-182">Í reitnum ItemGroup skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="821f8-182">In the ItemGroup field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="821f8-183">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="821f8-183">In the list, find and select the desired record.</span></span>
13. <span data-ttu-id="821f8-184">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="821f8-184">In the list, click the link in the selected row.</span></span>

