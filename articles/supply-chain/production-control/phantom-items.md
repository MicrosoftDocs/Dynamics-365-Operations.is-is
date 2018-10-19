---
title: "Skuggavörur"
description: "Þetta efnisatriði lýsir í smáatriðum hvernig hægt er að nota línugerð skuggavöru fyrir línurnar í uppskriftum og formúlu í Microsoft Dynamics 365 for Finance and Operations."
author: ShylaThompson
manager: AnnBe
ms.date: 06/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: shylaw
ms.search.validfrom: 
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: c5d4fb53939d88fcb1bd83d70bc361ed9879f298
ms.openlocfilehash: a92dd82f309867586f047e0dfc36e452a44a0f9c
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---

# <a name="phantom-items"></a><span data-ttu-id="bc685-103">Skuggavörur</span><span class="sxs-lookup"><span data-stu-id="bc685-103">Phantom items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc685-104">Þetta efnisatriði lýsir í smáatriðum hvernig hægt er að nota línugerð skuggavöru fyrir línurnar í uppskriftum og formúlu.</span><span class="sxs-lookup"><span data-stu-id="bc685-104">This topic describes, in detail, how the Phantom line type can be used for the lines of a bill of materials (BOM) and a formula.</span></span> <span data-ttu-id="bc685-105">Í eftirfarandi skýringarmynd er (a) uppskrift fyrir afurð H og hluta F og G og (b) leiðarskjalið fyrir afurðir H og hluta F.</span><span class="sxs-lookup"><span data-stu-id="bc685-105">In the following illustration, (a) is the BOM for product H and parts F and G, and (b) is the route sheet for products H and part F.</span></span>

![Afurð H og hluti F](media/product-H-part-F.png)


<span data-ttu-id="bc685-107">Þessi skýringarmynd sýnir dæmi um skipulag uppskriftar á tveimur stigum.</span><span class="sxs-lookup"><span data-stu-id="bc685-107">This illustration shows an example of a BOM structure in two levels.</span></span> <span data-ttu-id="bc685-108">Lokaafurð H táknar afurð fyrir samsetningu tækis.</span><span class="sxs-lookup"><span data-stu-id="bc685-108">Finished product H represents a product for a machine assembly.</span></span> <span data-ttu-id="bc685-109">Samsetning tækis samanstendur af tveimur hlutum, rafeiningu (F) sem er með tvo efnisþætti (A og B) og hópur umbúða (G) sem einnig er með tvo efnisþætti (C og D).</span><span class="sxs-lookup"><span data-stu-id="bc685-109">The machine assembly consists of two parts, an electrical unit (F) that has two materials (A and B) and a group of packaging materials (G) that also has two materials (C and D).</span></span> <span data-ttu-id="bc685-110">Annað efni (E) er notað við almenna samsetningu tækis.</span><span class="sxs-lookup"><span data-stu-id="bc685-110">Another material (E) is used during the general assembly of the machine.</span></span>

![Afurð H og hluti F](media/product-H-part-B.png)

<span data-ttu-id="bc685-112">Framangreind skýringarmynd sýnir hönnunaruppskrift fyrir afurð H. Þessi uppbygging veitir góða yfirsýn yfir hluta og íhluti fyrir heildarsamsetningu tækis.</span><span class="sxs-lookup"><span data-stu-id="bc685-112">The preceding illustration represents the Engineering BOM for product H. This structure provides a good overview of the parts and components of the overall machine assembly.</span></span> <span data-ttu-id="bc685-113">Þótt hönnuðir afurða gætu viljað sjá uppskriftina með þessum hætti, getur hins vegar verið að þessi uppbygging sýni ekki á réttan hátt hvernig tækið er sett upp í vinnusal.</span><span class="sxs-lookup"><span data-stu-id="bc685-113">However, although product designers might prefer to see the BOM represented in this way, this structure might not correctly represent the way that the machine is built on the shop floor.</span></span> 

<span data-ttu-id="bc685-114">Til dæmis bendir hönnunaruppskriftin í framagreindri skýringamynd til þess að rafeining F sé sett saman sem aðskilinn hluti á aðskildum vinnufyrirmælum.</span><span class="sxs-lookup"><span data-stu-id="bc685-114">For example, the Engineering BOM in the preceding illustration indicates that electrical unit F is assembled as a separate part on a separate work order.</span></span> <span data-ttu-id="bc685-115">Í vinnusal getur hins vegar verið að samsetning á rafeiningunni sem hluti af heildarsamsetningu tækisins sé talin æskilegri, en ekki sem aðskilin vinnufyrirmæli.</span><span class="sxs-lookup"><span data-stu-id="bc685-115">However, on the shop floor, it might be judged more optimal to assemble the electrical unit as part of the overall machine assembly, not as a separate work order.</span></span>

<span data-ttu-id="bc685-116">Hönnunaruppskrfitin gefur einnig til kynna að hluti G sé aðskilinn hluti.</span><span class="sxs-lookup"><span data-stu-id="bc685-116">This Engineering BOM also indicates that part G is a separate part.</span></span> <span data-ttu-id="bc685-117">Í þessari uppbyggingu táknar hluti G þó ekki efnislegan hluta, heldur safn af umbúðum.</span><span class="sxs-lookup"><span data-stu-id="bc685-117">However, in this structure, part G doesn’t represent a physical part but a collection of packaging materials.</span></span> 

<span data-ttu-id="bc685-118">Þess vegna, þrátt fyrir að hönnunaruppskrift sé hagkvæm fyrir hönnun afurðar og viðhaldi á þeirri hönnun, gæti verið að hún sé ekki rökréttasta leiðin til að styðja við framkvæmdarferli á framleiðslu afurðarinnar.</span><span class="sxs-lookup"><span data-stu-id="bc685-118">Therefore, although an Engineering BOM provides great value for the design of a product and maintenance of that design, it might not be the most logical way to support the manufacturing execution process of the product.</span></span> <span data-ttu-id="bc685-119">Aftur á móti sýnir hönnunaruppskrift bestu leiðina til að búa til afurð.</span><span class="sxs-lookup"><span data-stu-id="bc685-119">By contrast, a Manufacturing BOM represents the best way to build a product.</span></span>

<span data-ttu-id="bc685-120">Eftirfarandi skýringarmynd sýnir hvernig framangreind uppskrift er umbreytt í framleiðsluuppskrift.</span><span class="sxs-lookup"><span data-stu-id="bc685-120">The following illustration shows how the preceding Engineering BOM is transitioned into a Manufacturing BOM.</span></span> <span data-ttu-id="bc685-121">Í þessari skýringarmynd er (a) uppskrift fyrir afurð H, og (b) er leiðarskjalið fyrir afurð H.</span><span class="sxs-lookup"><span data-stu-id="bc685-121">In this illustration, (a) is the BOM for product H, and b is the route sheet for product H.</span></span>

<span data-ttu-id="bc685-122">Í þessari uppbyggingu er hægt að sjá að ekki er minnst á hluta F og G og efnin sem þessir hlutar samanstanda af hefur verið fært upp á næsta stig uppskriftar.</span><span class="sxs-lookup"><span data-stu-id="bc685-122">In this structure, you can see that there is no notion of parts F and G, and the materials that these parts consist of have been elevated to the next BOM level.</span></span> 

<span data-ttu-id="bc685-123">Ólíkt hönnunaruppskriftinni, sem var með tvö aðgerðarskjöl, hefur framleiðsluuppskriftin aðeins eitt aðgerðarskjal.</span><span class="sxs-lookup"><span data-stu-id="bc685-123">Unlike the Engineering BOM, which had two operations sheets, the Manufacturing BOM has only one operations sheet.</span></span> <span data-ttu-id="bc685-124">Umbúðaraðgerðin sem tengdist við hluta G, hefur einnig verið færður upp og er nú hluti af aðgerðarskjali fyrir afurð H. Samsetning rafeiningarinnar er fyrsta aðgerðin.</span><span class="sxs-lookup"><span data-stu-id="bc685-124">The packaging operation that was linked to part G has also been elevated and is now part of the operations sheet for product H. The assembly of the electrical unit is the first operation.</span></span> <span data-ttu-id="bc685-125">Þessi röð er skynsamleg, því að þessi eining er notuð í næstu aðgerð, sem er samsetning tækisins.</span><span class="sxs-lookup"><span data-stu-id="bc685-125">This order makes good sense, because this unit is used in the next operation, which is the machine assembly.</span></span> <span data-ttu-id="bc685-126">Síðasta aðgerðin er umbúðaraðgerðin, sem notar tvö umbúðaefni (C og D).</span><span class="sxs-lookup"><span data-stu-id="bc685-126">The last operation is the packaging operation, which consumes two packing materials (C and D).</span></span>

<span data-ttu-id="bc685-127">Í Microsoft Dynamics 365 for Finance and Operations er umbreytingin milli hönnunaruppskriftar og framleiðsluuppskriftar virkjuð með línugerð skuggauppskriftarinnar.</span><span class="sxs-lookup"><span data-stu-id="bc685-127">In Microsoft Dynamics 365 for Finance and Operations, the transition between the Engineering BOM and the Manufacturing BOM is enabled through the Phantom BOM line type.</span></span> <span data-ttu-id="bc685-128">Eins og hugtakið „skuggi“ bendir til hafa hlutar F og G horfið við umbreytingu á milli uppskriftargerðanna tveggja.</span><span class="sxs-lookup"><span data-stu-id="bc685-128">As the term “phantom” indicates, parts F and G have disappeared during the transition between the two BOM types.</span></span> <span data-ttu-id="bc685-129">Í þessu dæmi er skuggalínugerðin notuð á uppskriftarlínurnar fyrir hluta F og G í hönnunaruppskriftinni.</span><span class="sxs-lookup"><span data-stu-id="bc685-129">In this example, the Phantom line type is applied to the BOM lines for parts F and G in the Engineering BOM.</span></span> <span data-ttu-id="bc685-130">Þegar framleiðslu- eða runupöntun er stofnuð er hönnunaruppskriftin afrituð í framleiðslu- eða runupöntunina.</span><span class="sxs-lookup"><span data-stu-id="bc685-130">When a production or batch order is created, the Engineering BOM is copied to the production or batch order.</span></span> <span data-ttu-id="bc685-131">Þá, þegar pöntunin er áætluð, á sér stað umbreyting frá hönnunaruppskrift til framleiðsluuppskriftar, eins og sýnt er á framangreindri skýringarmynd.</span><span class="sxs-lookup"><span data-stu-id="bc685-131">Then, when the order is estimated, the transition from the Engineering BOM to the Manufacturing BOM occurs, as shown in the preceding illustrations.</span></span> <span data-ttu-id="bc685-132">Í aðgerðarskjalinu í annarri skýringarmyndinni er umbúðaefni C og D aðföng fyrir aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="bc685-132">From the operations sheet in the second illustration, packaging materials C and D are input for the operation.</span></span> 

## <a name="multilevel-phantom-bom-structures"></a><span data-ttu-id="bc685-133">Uppbygging skuggauppskriftar á mörgum stigum</span><span class="sxs-lookup"><span data-stu-id="bc685-133">Multilevel phantom BOM structures</span></span>
<span data-ttu-id="bc685-134">Hægt er að nota skuggalínugerð í marglaga hönnunaruppskrift eins og sýnt er á eftirfarandi skýringarmynd.</span><span class="sxs-lookup"><span data-stu-id="bc685-134">The Phantom line type can be used in multilevel BOM structures, as shown in the following illustration.</span></span> <span data-ttu-id="bc685-135">Í þessari skýringarmynd er (a) uppskrift fyrir afurð G, og (b) leiðarskjalið fyrir hluta E og F og afurð G.</span><span class="sxs-lookup"><span data-stu-id="bc685-135">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for parts E and F and product G.</span></span> 

![Afurð G og hluti F með leiðarskjölum](media/product-G-route-sheet-G.png)


<span data-ttu-id="bc685-137">Eftirfarandi skýringarmynd sýnir framleiðsluuppskriftina og leiðarskjalið ef uppskriftarlínur fyrir hluta E og F eru stilltar þannig að línugerðin sé skuggalínugerð.</span><span class="sxs-lookup"><span data-stu-id="bc685-137">The following illustration shows the resulting Manufacturing BOM and route sheet if the BOM lines for parts E and F are configured so that the line type is Phantom.</span></span> <span data-ttu-id="bc685-138">Í þessari skýringarmynd er (a) uppskrift fyrir afurð G, og (b) leiðarskjalið fyrir afurð G.</span><span class="sxs-lookup"><span data-stu-id="bc685-138">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for product G.</span></span>

![Afurð G](media/product-G.png)


## <a name="phantom-and-route-network"></a><span data-ttu-id="bc685-140">Skugga- og leiðanet</span><span class="sxs-lookup"><span data-stu-id="bc685-140">Phantom and route network</span></span>
<span data-ttu-id="bc685-141">Einnig er hægt að nota skuggauppskriftir fyrir uppskrift sem hefur leiðanet.</span><span class="sxs-lookup"><span data-stu-id="bc685-141">Phantom BOMs can also be used for a BOM that has a route network.</span></span> <span data-ttu-id="bc685-142">Í leiðaneti eru ein eða fleiri aðgerðir keyrðar samhliða.</span><span class="sxs-lookup"><span data-stu-id="bc685-142">In a route network, one or more operations run in parallel.</span></span> <span data-ttu-id="bc685-143">Eftirfarandi skýringarmynd sýnir dæmi um leiðanet sem er notað í uppskrift á mörgum stigum.</span><span class="sxs-lookup"><span data-stu-id="bc685-143">The following illustration shows an example of a route network that is used in a multilevel BOM.</span></span> <span data-ttu-id="bc685-144">Í þessari skýringarmynd er (a) uppskrift fyrir afurð G og hluta F, og (b) leiðarskjalið fyrir afurð G og hluta F, sem er með leiðanet.</span><span class="sxs-lookup"><span data-stu-id="bc685-144">In this illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F, which has a route network.</span></span>

![Afurð G og hluti F](media/product-G-part-F.png)


<span data-ttu-id="bc685-146">Í eftirfarandi skýringarmynd er (a) uppskrift fyrir afurð G og hluta F og (b) leiðarskjalið fyrir afurð G og hluta F.</span><span class="sxs-lookup"><span data-stu-id="bc685-146">In the following illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F.</span></span>

![Afurð G og hluti F með leiðarskjölum](media/product-G-part-F-with-route-sheet.png)

