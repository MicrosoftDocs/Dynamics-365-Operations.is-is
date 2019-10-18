---
title: Yfirlit yfir vinnureglur vöruhúss
description: Vöruhús vinnu reglur stýra hvort vöruhúsavinna sé stofnuð af ferli vöruhúsa í framleiðsluumhverfi, samkvæmt gerð verks, staðsetningu birgða og vöru.
author: johanhoffmann
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 196561
ms.assetid: cbf48ec6-1836-48d5-ad66-a9b534af1786
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 7476cf797685feb4c50e3cefef4c53ca37b82dff
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251409"
---
# <a name="warehouse-work-policies-overview"></a><span data-ttu-id="d41bd-103">Yfirlit yfir vinnureglur vöruhúss</span><span class="sxs-lookup"><span data-stu-id="d41bd-103">Warehouse work policies overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d41bd-104">Vöruhús vinnu reglur stýra hvort vöruhúsavinna sé stofnuð af ferli vöruhúsa í framleiðsluumhverfi, samkvæmt gerð verks, staðsetningu birgða og vöru.</span><span class="sxs-lookup"><span data-stu-id="d41bd-104">Warehouse work policies control whether warehouse work is created by warehouse processes in manufacturing, based on work order type, inventory location, and product.</span></span>

<span data-ttu-id="d41bd-105">Þessi regla vinnu stýrir því hvort vöruhúsavinnu er stofnað fyrir ferli vöruhúsa í framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="d41bd-105">This work policy controls whether warehouse work is created for warehouse processes in manufacturing.</span></span> <span data-ttu-id="d41bd-106">Setja upp stefnu vinnu með samsetningu **vinnupantanagerðir**, **staðsetningu birgða**, og **afurð**.</span><span class="sxs-lookup"><span data-stu-id="d41bd-106">You can set up the work policy by using a combination of **work order types**, an **inventory location**, and a **product**.</span></span> <span data-ttu-id="d41bd-107">Til dæmis er afurð L0101 skráð sem lokið á staðsetningu framleiðslufrálags 001.</span><span class="sxs-lookup"><span data-stu-id="d41bd-107">For example, product L0101 is reported as finished to output location 001.</span></span> <span data-ttu-id="d41bd-108">Fullbúin framleiðsluvara er síðar notuð í aðra framleiðslupöntun á staðsetningu frálags 001.</span><span class="sxs-lookup"><span data-stu-id="d41bd-108">The finished good is later consumed in another production order at output location 001.</span></span> <span data-ttu-id="d41bd-109">Í þessu tilfelli er hægt að setja upp reglu vinnu til að koma í veg fyrir að vinna fyrir fullbúnar vörur frágangur stofnað þegar afurð L0101 tilbúið að staðsetningu framleiðslufrálags 001.</span><span class="sxs-lookup"><span data-stu-id="d41bd-109">In this case, you can set up a work policy to prevent the work for finished goods put-away from being created when you report product L0101 as finished to output location 001.</span></span> <span data-ttu-id="d41bd-110">Regla vinnu er einstök eining sem lýst hægt að með eftirfarandi upplýsingum:</span><span class="sxs-lookup"><span data-stu-id="d41bd-110">The work policy is an individual entity that can be described through the following information:</span></span>

-   <span data-ttu-id="d41bd-111">**Vinnuregluheiti** (einkvæmt kenni reglunnar vinna)</span><span class="sxs-lookup"><span data-stu-id="d41bd-111">**Work policy name** (the unique identifier of the work policy)</span></span>
-   <span data-ttu-id="d41bd-112">**Vinnupantanagerðir** og **aðferð fyrir stofnun Vinnu**</span><span class="sxs-lookup"><span data-stu-id="d41bd-112">**Work order types** and **Work creation method**</span></span>
-   <span data-ttu-id="d41bd-113">**Birgðastaðsetningar**</span><span class="sxs-lookup"><span data-stu-id="d41bd-113">**Inventory locations**</span></span>
-   <span data-ttu-id="d41bd-114">**Afurðir**</span><span class="sxs-lookup"><span data-stu-id="d41bd-114">**Products**</span></span>

## <a name="work-order-types"></a><span data-ttu-id="d41bd-115">Gerðir vinnupöntunar</span><span class="sxs-lookup"><span data-stu-id="d41bd-115">Work order types</span></span>
<span data-ttu-id="d41bd-116">Hægt er að velja um eftirfarandi gerðir vinnupöntunar:</span><span class="sxs-lookup"><span data-stu-id="d41bd-116">You can select the following work order types:</span></span>

-   <span data-ttu-id="d41bd-117">Frágangur á fullunnum vörum</span><span class="sxs-lookup"><span data-stu-id="d41bd-117">Finished goods put away</span></span>
-   <span data-ttu-id="d41bd-118">Frágangur aukaafurða og hliðarafurða</span><span class="sxs-lookup"><span data-stu-id="d41bd-118">Co-product and by-product put away</span></span>
-   <span data-ttu-id="d41bd-119">Tiltekt hráefnis</span><span class="sxs-lookup"><span data-stu-id="d41bd-119">Raw material picking</span></span>

<span data-ttu-id="d41bd-120">Í **aðferð fyrir stofnun Vinnu** svæðið hefur gildið **Aldrei**.</span><span class="sxs-lookup"><span data-stu-id="d41bd-120">The **Work creation method** field has the value **Never**.</span></span> <span data-ttu-id="d41bd-121">Þetta gildi gefur til kynna að vinnu regla kemur í veg fyrir vöruhúsavinnu verið stofnuð fyrir valda vinnupöntunargerð.</span><span class="sxs-lookup"><span data-stu-id="d41bd-121">This value indicates that the work policy will prevent warehouse work from being created for the selected work order type.</span></span>

## <a name="inventory-locations"></a><span data-ttu-id="d41bd-122">Birgðastaðsetningar</span><span class="sxs-lookup"><span data-stu-id="d41bd-122">Inventory locations</span></span>
<span data-ttu-id="d41bd-123">Velja má á staðsetningu sem reglan vinna á við um.</span><span class="sxs-lookup"><span data-stu-id="d41bd-123">You can select a location that the work policy applies to.</span></span> <span data-ttu-id="d41bd-124">Ef engin staðsetning er tengd vinnureglu vinnureglu ekki eiga við um ferli.</span><span class="sxs-lookup"><span data-stu-id="d41bd-124">If no location is associated with a work policy, the work policy doesn’t apply to any processes.</span></span> <span data-ttu-id="d41bd-125">Á **Staðsetningar** síðu er einnig er hægt að velja eða hætta við val á vinnu reglu fyrir ákveðna staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="d41bd-125">On the **Locations** page, you can also select or cancel the selection of the work policy for a specific location.</span></span>

## <a name="products"></a><span data-ttu-id="d41bd-126">Afurðir</span><span class="sxs-lookup"><span data-stu-id="d41bd-126">Products</span></span>
<span data-ttu-id="d41bd-127">Velja má á vöru sem reglan vinna á við um.</span><span class="sxs-lookup"><span data-stu-id="d41bd-127">You can select a product that the work policy applies to.</span></span> <span data-ttu-id="d41bd-128">Hægt er að nota regluna vinnu allar afurðir eða valdar afurðir.</span><span class="sxs-lookup"><span data-stu-id="d41bd-128">You can apply the work policy to either all products or selected products.</span></span>

## <a name="example"></a><span data-ttu-id="d41bd-129">Dæmi</span><span class="sxs-lookup"><span data-stu-id="d41bd-129">Example</span></span>
<span data-ttu-id="d41bd-130">Í eftirfarandi dæmi eru tvær framleiðslupantanir, PRD 001 og PRD 00*2*.</span><span class="sxs-lookup"><span data-stu-id="d41bd-130">In the following example, there are two production orders, PRD-001 and PRD-00*2*.</span></span> <span data-ttu-id="d41bd-131">Framleiðslupöntunin PRD 001 hefur aðgerðar sem nefnist **Samsetningu**, þar sem afurð SC1 verið skráð sem lokið á staðsetningu O1.</span><span class="sxs-lookup"><span data-stu-id="d41bd-131">Production order PRD-001 has an operation that is named **Assembly**, where product SC1 is being reported as finished to location O1.</span></span> <span data-ttu-id="d41bd-132">Framleiðslupöntunin PRD 002 hefur aðgerðar sem nefnist **Málun** og notar afurð SC1 frá staðsetningu O1.</span><span class="sxs-lookup"><span data-stu-id="d41bd-132">Production order PRD-002 has an operation that is named **Painting** and consumes product SC1 from location O1.</span></span> <span data-ttu-id="d41bd-133">Framleiðslupöntunin PRD 002 notar einnig RM1 hráefni úr staðsetningunni O1.</span><span class="sxs-lookup"><span data-stu-id="d41bd-133">Production order PRD-002 also consumes raw material RM1 from location O1.</span></span> <span data-ttu-id="d41bd-134">RM1 er geymd á staðsetningu vöruhúss BULK-001 og verður tekið til staðsetningu O1 eftir vöruhúsi vinnu fyrir tiltekt hráefnis.</span><span class="sxs-lookup"><span data-stu-id="d41bd-134">RM1 is stored in warehouse location BULK-001 and will be picked to location O1 by warehouse work for raw material picking.</span></span> <span data-ttu-id="d41bd-135">Vinna tiltektar er myndað þegar PRD 002 framleiðsla er losuð.</span><span class="sxs-lookup"><span data-stu-id="d41bd-135">The picking work is generated when production PRD-002 is released.</span></span> 

<span data-ttu-id="d41bd-136">[![Reglur vöruhúsavinnu](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="d41bd-136">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span> 

<span data-ttu-id="d41bd-137">Þegar ætlunin er að skilgreina vöruhús regla vinnu á þessu dæmi ætti að íhuga að eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="d41bd-137">When you plan to configure a warehouse work policy for this scenario, you should consider the following information:</span></span>

-   <span data-ttu-id="d41bd-138">Vöruhúsavinnu fyrir fullbúnar vörur frágangur er ekki áskilin þegar afurð SC1 tilbúið úr framleiðslunni pöntun PRD-001 til staðsetningu O1 er tilkynnt.</span><span class="sxs-lookup"><span data-stu-id="d41bd-138">Warehouse work for finished goods put-away isn’t required when you report product SC1 as finished from production order PRD-001 to location O1.</span></span> <span data-ttu-id="d41bd-139">Þetta er vegna þess að í **Málun** aðgerð fyrir framleiðslupöntun PRD 002 notar SC1 á sama stað.</span><span class="sxs-lookup"><span data-stu-id="d41bd-139">This is because the **Painting** operation for production order PRD-002 consumes SC1 at the same location.</span></span>
-   <span data-ttu-id="d41bd-140">Vinna vöruhús fyrir tiltekt hráefnis er krafist til að flytja RM1 hráefni frá staðsetningu vöruhúss BULK-001 á staðsetningu O1.</span><span class="sxs-lookup"><span data-stu-id="d41bd-140">Warehouse work for raw material picking is required in order to move raw material RM1 from warehouse location BULK-001 to location O1.</span></span>

<span data-ttu-id="d41bd-141">Hér er dæmi um vinnu regluna sem hægt er að setja upp, byggðar á þessum atriðum.</span><span class="sxs-lookup"><span data-stu-id="d41bd-141">Here is an example of the work policy that you can set up, based on these considerations.</span></span>


|                                       |                                       |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="d41bd-142"><strong>Heiti vinnureglu</strong></span><span class="sxs-lookup"><span data-stu-id="d41bd-142"><strong>Work policy name</strong></span></span><br> | <span data-ttu-id="d41bd-143"><strong>Gerðir vinnupöntunar</strong></span><span class="sxs-lookup"><span data-stu-id="d41bd-143"><strong>Work order types</strong></span></span><br> |
|         <span data-ttu-id="d41bd-144">Enginn frágangur 01</span><span class="sxs-lookup"><span data-stu-id="d41bd-144">No put away 01     \`</span></span>          |     <span data-ttu-id="d41bd-145">- Frágangur á fullunnum vörum</span><span class="sxs-lookup"><span data-stu-id="d41bd-145">- Finished good put away</span></span><br>      |
|                                       |    <span data-ttu-id="d41bd-146"><strong>Staðsetningar</strong></span><span class="sxs-lookup"><span data-stu-id="d41bd-146"><strong>Locations</strong></span></span><br>     |
|                                       |                 <span data-ttu-id="d41bd-147">- O1</span><span class="sxs-lookup"><span data-stu-id="d41bd-147">- O1</span></span>                  |
|                                       |    <span data-ttu-id="d41bd-148"><strong>Afurðir</strong></span><span class="sxs-lookup"><span data-stu-id="d41bd-148"><strong>Products</strong></span></span> <br>     |
|                                       |                 <span data-ttu-id="d41bd-149">- SC1</span><span class="sxs-lookup"><span data-stu-id="d41bd-149">- SC1</span></span>                 |

<span data-ttu-id="d41bd-150">Eftirfarandi ferli lýsa nákvæmar leiðbeiningar um hvernig setja á upp reglu vinnu vöruhús fyrir þetta dæmi.</span><span class="sxs-lookup"><span data-stu-id="d41bd-150">The following procedures provide step-by-step instructions about how to set up the warehouse work policy for this scenario.</span></span> <span data-ttu-id="d41bd-151">Sýnishorn uppsetningar sýnir hvernig tilkynnt framleiðslupöntun sem lokið á staðsetningu sem er ekki númeraplötustýrð eru einnig lýst.</span><span class="sxs-lookup"><span data-stu-id="d41bd-151">A sample setup showing how to report a production order as finished to a location that isn’t license plate–controlled is also described.</span></span>

## <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="d41bd-152">Setja upp reglur vöruhúsavinnu</span><span class="sxs-lookup"><span data-stu-id="d41bd-152">Set up a warehouse work policy</span></span>
<span data-ttu-id="d41bd-153">Ferli vöruhúsa ekki alltaf hafa vöruhús vinnu.</span><span class="sxs-lookup"><span data-stu-id="d41bd-153">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="d41bd-154">Með því að skilgreina vinnustefnu, sem getur komið í veg fyrir stofnun vinnu fyrir tiltekt hráefnis og frágangur fullbúinna vara fyrir safn af afurðum á tiltekna staði.</span><span class="sxs-lookup"><span data-stu-id="d41bd-154">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="d41bd-155">USMF sýniútgáfu fyrirtækis notað til að stofna þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="d41bd-155">The USMF demo data company was used to create this procedure.</span></span> 

<span data-ttu-id="d41bd-156">SKREF (21)</span><span class="sxs-lookup"><span data-stu-id="d41bd-156">STEPS (21)</span></span>

|     |                                                                            |
|-----|----------------------------------------------------------------------------|
| <span data-ttu-id="d41bd-157">1.</span><span class="sxs-lookup"><span data-stu-id="d41bd-157">1.</span></span>  | <span data-ttu-id="d41bd-158">Fara í vöruhúsakerfi &gt; Uppsetning &gt; Vinna &gt; Vinnureglur.</span><span class="sxs-lookup"><span data-stu-id="d41bd-158">Go to Warehouse management &gt; Setup &gt; Work &gt; Work policies.</span></span>        |
| <span data-ttu-id="d41bd-159">2.</span><span class="sxs-lookup"><span data-stu-id="d41bd-159">2.</span></span>  | <span data-ttu-id="d41bd-160">Smellið á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="d41bd-160">Click New.</span></span>                                                                 |
| <span data-ttu-id="d41bd-161">3.</span><span class="sxs-lookup"><span data-stu-id="d41bd-161">3.</span></span>  | <span data-ttu-id="d41bd-162">Í svæðið Vinnu reglu heiti, skrifa 'Engin frágangsvinna‘</span><span class="sxs-lookup"><span data-stu-id="d41bd-162">In the Work policy name field, type 'No put-away work'.</span></span>                    |
| <span data-ttu-id="d41bd-163">4.</span><span class="sxs-lookup"><span data-stu-id="d41bd-163">4.</span></span>  | <span data-ttu-id="d41bd-164">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="d41bd-164">Click Save.</span></span>                                                                |
| <span data-ttu-id="d41bd-165">5.</span><span class="sxs-lookup"><span data-stu-id="d41bd-165">5.</span></span>  | <span data-ttu-id="d41bd-166">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d41bd-166">Click Add.</span></span>                                                                 |
| <span data-ttu-id="d41bd-167">6.</span><span class="sxs-lookup"><span data-stu-id="d41bd-167">6.</span></span>  | <span data-ttu-id="d41bd-168">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d41bd-168">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="d41bd-169">7.</span><span class="sxs-lookup"><span data-stu-id="d41bd-169">7.</span></span>  | <span data-ttu-id="d41bd-170">Í Gerð vinnupöntun svæðinu, veljið 'Fullunninna vöru frágangur'.</span><span class="sxs-lookup"><span data-stu-id="d41bd-170">In the Work order type field, select 'Finished goods put away'.</span></span>            |
| <span data-ttu-id="d41bd-171">8.</span><span class="sxs-lookup"><span data-stu-id="d41bd-171">8.</span></span>  | <span data-ttu-id="d41bd-172">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d41bd-172">Click Add.</span></span>                                                                 |
| <span data-ttu-id="d41bd-173">9.</span><span class="sxs-lookup"><span data-stu-id="d41bd-173">9.</span></span>  | <span data-ttu-id="d41bd-174">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d41bd-174">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="d41bd-175">10.</span><span class="sxs-lookup"><span data-stu-id="d41bd-175">10.</span></span> | <span data-ttu-id="d41bd-176">Í Gerð vinnupöntun svæðinu, veljið 'Aukaafurða og hliðarafurða frágangur'.</span><span class="sxs-lookup"><span data-stu-id="d41bd-176">In the Work order type field, select 'Co-product and by-product put away'.</span></span> |
| <span data-ttu-id="d41bd-177">11.</span><span class="sxs-lookup"><span data-stu-id="d41bd-177">11.</span></span> | <span data-ttu-id="d41bd-178">Útvíkka hlutann birgðastaðsetning.</span><span class="sxs-lookup"><span data-stu-id="d41bd-178">Expand the Inventory locations section.</span></span>                                    |
| <span data-ttu-id="d41bd-179">12.</span><span class="sxs-lookup"><span data-stu-id="d41bd-179">12.</span></span> | <span data-ttu-id="d41bd-180">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d41bd-180">Click Add.</span></span>                                                                 |
| <span data-ttu-id="d41bd-181">13.</span><span class="sxs-lookup"><span data-stu-id="d41bd-181">13.</span></span> | <span data-ttu-id="d41bd-182">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d41bd-182">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="d41bd-183">14.</span><span class="sxs-lookup"><span data-stu-id="d41bd-183">14.</span></span> | <span data-ttu-id="d41bd-184">Í vöruhúsalistanum, sláðu inn "51"</span><span class="sxs-lookup"><span data-stu-id="d41bd-184">In the Warehouse list, enter '51'.</span></span>                                         |
| <span data-ttu-id="d41bd-185">15.</span><span class="sxs-lookup"><span data-stu-id="d41bd-185">15.</span></span> | <span data-ttu-id="d41bd-186">Sláið inn eða veldu '001‘ í staðsetning reitnum.</span><span class="sxs-lookup"><span data-stu-id="d41bd-186">In the Location field, enter or select '001'.</span></span>                              |
| <span data-ttu-id="d41bd-187">16.</span><span class="sxs-lookup"><span data-stu-id="d41bd-187">16.</span></span> | <span data-ttu-id="d41bd-188">Víkka út hlutann Afurðir.</span><span class="sxs-lookup"><span data-stu-id="d41bd-188">Expand the Products section.</span></span>                                               |
| <span data-ttu-id="d41bd-189">17.</span><span class="sxs-lookup"><span data-stu-id="d41bd-189">17.</span></span> | <span data-ttu-id="d41bd-190">Í reitnum afurðaval skal velja valið.</span><span class="sxs-lookup"><span data-stu-id="d41bd-190">In the Product selection field, select 'Selected'.</span></span>                         |
| <span data-ttu-id="d41bd-191">18.</span><span class="sxs-lookup"><span data-stu-id="d41bd-191">18.</span></span> | <span data-ttu-id="d41bd-192">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d41bd-192">Click Add.</span></span>                                                                 |
| <span data-ttu-id="d41bd-193">19.</span><span class="sxs-lookup"><span data-stu-id="d41bd-193">19.</span></span> | <span data-ttu-id="d41bd-194">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d41bd-194">In the list, mark the selected row.</span></span>                                        |
| <span data-ttu-id="d41bd-195">20.</span><span class="sxs-lookup"><span data-stu-id="d41bd-195">20.</span></span> | <span data-ttu-id="d41bd-196">Í reitinn Vörunúmer skal slá inn eða veldu L0101.</span><span class="sxs-lookup"><span data-stu-id="d41bd-196">In the Item number field, enter or select 'L0101'.</span></span>                         |
| <span data-ttu-id="d41bd-197">21.</span><span class="sxs-lookup"><span data-stu-id="d41bd-197">21.</span></span> | <span data-ttu-id="d41bd-198">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="d41bd-198">Click Save.</span></span>                                                                |

## <a name="report-a-production-order-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="d41bd-199">Tilkynna framleiðslupöntun sem lokið er á staðsetningu sem ekki númeraplötustýrð</span><span class="sxs-lookup"><span data-stu-id="d41bd-199">Report a production order as finished to a location that isn’t license plate–controlled</span></span>
<span data-ttu-id="d41bd-200">Þessi ferli sýnir dæmi um skýrslugerð sem lokið á staðsetningu sem ekki númeraplötustýrð.</span><span class="sxs-lookup"><span data-stu-id="d41bd-200">This procedure shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="d41bd-201">Gildandi vinnureglu er skilyrði fyrir þetta verk.</span><span class="sxs-lookup"><span data-stu-id="d41bd-201">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="d41bd-202">Fyrri ferli sýna uppsetningu vinnureglu.</span><span class="sxs-lookup"><span data-stu-id="d41bd-202">The previous procedure shows the setup of the work policy.</span></span> 

<span data-ttu-id="d41bd-203">SKREF (25)</span><span class="sxs-lookup"><span data-stu-id="d41bd-203">STEPS (25)</span></span>

<table>
<tbody>
<tr>
<td colspan="3"><span data-ttu-id="d41bd-204"><strong>Undirverk: Setja upp staðsetningu úttaks</strong></span><span class="sxs-lookup"><span data-stu-id="d41bd-204"><strong>Sub-task: Set up an output location.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="d41bd-205">Fara á fyrirtækisstjórnun &gt; Tilföng &gt; Tilfangaflokka.</span><span class="sxs-lookup"><span data-stu-id="d41bd-205">Go to Organization administration &gt; Resources &gt; Resource groups.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="d41bd-206">Á listanum skal velja tilfangaflokk &#39;5102&#39;.</span><span class="sxs-lookup"><span data-stu-id="d41bd-206">In the list, select resource group &#39;5102&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="d41bd-207">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="d41bd-207">Click Edit.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="d41bd-208">Í úttaksvöruhúsreitnum skal velja &#39;51&#39;.</span><span class="sxs-lookup"><span data-stu-id="d41bd-208">In the Output warehouse field, enter &#39;51&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="d41bd-209">Í reit úttakssvæðis skal slá inn &#39;001&#39;.</span><span class="sxs-lookup"><span data-stu-id="d41bd-209">In the Output location field, enter &#39;001&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="d41bd-210">Staðsetning 001 er ekki &#39; númeraplötustýrð stjórnun.</span><span class="sxs-lookup"><span data-stu-id="d41bd-210">Location 001 isn&#39;t a license plate–controlled location.</span></span> <span data-ttu-id="d41bd-211">Hægt er að setja upp staðsetningu úttaks ekki númeraplötu aðeins ef gildandi vinnureglu er til fyrir staðsetningarinnar.</span><span class="sxs-lookup"><span data-stu-id="d41bd-211">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span></td>
</tr>
<tr>
<td colspan="3"><span data-ttu-id="d41bd-212"><strong>Undirverk: Stofna framleiðslupöntun og skrá sem lokið.</strong></span><span class="sxs-lookup"><span data-stu-id="d41bd-212"><strong>Sub-task: Create a production order and report it as finished.</strong></span></span></td>
</tr>
<tr>
<td></td>
<td>1.</td>
<td><span data-ttu-id="d41bd-213">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d41bd-213">Close the page.</span></span></td>
</tr>
<tr>
<td></td>
<td>2.</td>
<td><span data-ttu-id="d41bd-214">Fara í framleiðslustýringar &gt; Framleiðslupantanir &gt; Allar framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="d41bd-214">Go to Production control &gt; Production orders &gt; All production orders.</span></span></td>
</tr>
<tr>
<td></td>
<td>3.</td>
<td><span data-ttu-id="d41bd-215">Smella á Ný framleiðslupöntun.</span><span class="sxs-lookup"><span data-stu-id="d41bd-215">Click New production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>4.</td>
<td><span data-ttu-id="d41bd-216">Í vörunúmerasvæðið skal slá inn &#39;L0101&#39;.</span><span class="sxs-lookup"><span data-stu-id="d41bd-216">In the Item number field, enter &#39;L0101&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>5.</td>
<td><span data-ttu-id="d41bd-217">Smellið á „Stofna“.</span><span class="sxs-lookup"><span data-stu-id="d41bd-217">Click Create.</span></span></td>
</tr>
<tr>
<td></td>
<td>6.</td>
<td><span data-ttu-id="d41bd-218">Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="d41bd-218">On the Action Pane, click Production order.</span></span></td>
</tr>
<tr>
<td></td>
<td>7.</td>
<td><span data-ttu-id="d41bd-219">Smellt er á Mat.</span><span class="sxs-lookup"><span data-stu-id="d41bd-219">Click Estimate.</span></span></td>
</tr>
<tr>
<td></td>
<td>8.</td>
<td><span data-ttu-id="d41bd-220">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="d41bd-220">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>9.</td>
<td><span data-ttu-id="d41bd-221">Smellt er á Byrja.</span><span class="sxs-lookup"><span data-stu-id="d41bd-221">Click Start.</span></span></td>
</tr>
<tr>
<td></td>
<td>10.</td>
<td><span data-ttu-id="d41bd-222">Smellið á flipann „Almennt“.</span><span class="sxs-lookup"><span data-stu-id="d41bd-222">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>11.</td>
<td><span data-ttu-id="d41bd-223">Veljið &#39;Aldrei&#39; í reitnum Sjálfvirk uppskriftarnotkun.</span><span class="sxs-lookup"><span data-stu-id="d41bd-223">In the Automatic BOM consumption field, select &#39;Never&#39;.</span></span></td>
</tr>
<tr>
<td></td>
<td>12.</td>
<td><span data-ttu-id="d41bd-224">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d41bd-224">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>13.</td>
<td><span data-ttu-id="d41bd-225">Smellið á „Bóka sem tilbúið“.</span><span class="sxs-lookup"><span data-stu-id="d41bd-225">Click Report as finished.</span></span></td>
</tr>
<tr>
<td></td>
<td>14.</td>
<td><span data-ttu-id="d41bd-226">Smellið á flipann „Almennt“.</span><span class="sxs-lookup"><span data-stu-id="d41bd-226">Click the General tab.</span></span></td>
</tr>
<tr>
<td></td>
<td>15.</td>
<td><span data-ttu-id="d41bd-227">Velja skal Já í reitnum leyfa villu.</span><span class="sxs-lookup"><span data-stu-id="d41bd-227">Select Yes in the Accept error field.</span></span></td>
</tr>
<tr>
<td></td>
<td>16.</td>
<td><span data-ttu-id="d41bd-228">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="d41bd-228">Click OK.</span></span></td>
</tr>
<tr>
<td></td>
<td>17.</td>
<td><span data-ttu-id="d41bd-229">Í aðgerðasvæðinu er smellt á vöruhús.</span><span class="sxs-lookup"><span data-stu-id="d41bd-229">On the Action Pane, click Warehouse.</span></span></td>
</tr>
<tr>
<td></td>
<td>18.</td>
<td><span data-ttu-id="d41bd-230">Smellt er á Upplýsingar um vinnu</span><span class="sxs-lookup"><span data-stu-id="d41bd-230">Click Work details.</span></span></td>
</tr>
<tr>
<td></td>
<td>19.</td>
<td><span data-ttu-id="d41bd-231">Þegar framleiðslupöntunin var skráð sem lokið, engin vinna var mynduð fyrir frágangur.</span><span class="sxs-lookup"><span data-stu-id="d41bd-231">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="d41bd-232">Þetta gerist vegna þess að vinna regla er skilgreind sem kemur í veg fyrir vinnu búnar til þegar afurð L0101 er skráð sem lokið á staðsetningu 001.</span><span class="sxs-lookup"><span data-stu-id="d41bd-232">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span></td>
</tr>
</tbody>
</table>



