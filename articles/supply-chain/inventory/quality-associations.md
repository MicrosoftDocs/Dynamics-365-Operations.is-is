---
title: Gæðatengingar
description: Þetta efnisatriði lýsir því hvernig er hægt að nota gæðatengingar í Microsoft Dynamics 365 Supply Chain Management til að búa til gæðapantanir sjálfkrafa sem tengjast sölum þínum, innkaupum og framleiðsluferlum.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2020-06-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f46f09dc9b67cfb04d0320a071c2c739266af58
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956696"
---
# <a name="quality-associations"></a><span data-ttu-id="0786a-103">Gæðatengingar</span><span class="sxs-lookup"><span data-stu-id="0786a-103">Quality associations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0786a-104">Þetta efnisatriði lýsir því hvernig er hægt að nota gæðatengingar í Microsoft Dynamics 365 Supply Chain Management til að búa til gæðapantanir sjálfkrafa sem tengjast sölum þínum, innkaupum og framleiðsluferlum.</span><span class="sxs-lookup"><span data-stu-id="0786a-104">This topic describes how you can use quality associations in Microsoft Dynamics 365 Supply Chain Management to automatically generate quality orders that are related to your sales, purchase, and production processes.</span></span>

<span data-ttu-id="0786a-105">Gæðatenging skilgreinir allar eftirfarandi upplýsingar fyrir gæðapöntun sem er mynduð:</span><span class="sxs-lookup"><span data-stu-id="0786a-105">A quality association defines all the following information for a quality order that is generated:</span></span>

- <span data-ttu-id="0786a-106">Færslutilvikið</span><span class="sxs-lookup"><span data-stu-id="0786a-106">The transaction event</span></span>
- <span data-ttu-id="0786a-107">Safn prófana sem þarf að framkvæma á vörum</span><span class="sxs-lookup"><span data-stu-id="0786a-107">The set of tests that must be performed on the items</span></span>
- <span data-ttu-id="0786a-108">Viðunandi gæðastigi (AQL)</span><span class="sxs-lookup"><span data-stu-id="0786a-108">The acceptable quality level (AQL)</span></span>
- <span data-ttu-id="0786a-109">Úrtaksáætlunin</span><span class="sxs-lookup"><span data-stu-id="0786a-109">The sampling plan</span></span>

<span data-ttu-id="0786a-110">Gæðatengingu verður að skilgreina fyrir hvert afbrigði viðskiptaferlis sem krefst sjálfvirkrar myndunar gæðapöntunar.</span><span class="sxs-lookup"><span data-stu-id="0786a-110">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="0786a-111">Til dæmis er hægt að mynda gæðapöntun í viðskiptaferlum fyrir innkaupapantanir, biðgeymslupantanir, sölupantanir eða framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="0786a-111">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="0786a-112">Vinna með gæðatengingar</span><span class="sxs-lookup"><span data-stu-id="0786a-112">Working with quality associations</span></span>

<span data-ttu-id="0786a-113">Viðskiptaferli sem notar gæðatengingu getur verið tengt mismunandi upprunaskjölum, eins og innkaupapöntunum, sölupöntunum eða framleiðslupöntunum.</span><span class="sxs-lookup"><span data-stu-id="0786a-113">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="0786a-114">Hver gæðatengingafærsla skilgreinir einnig prófanir, viðunandi gæðastig og úrtaksáætlun sem eiga við myndaðar gæðapantanir.</span><span class="sxs-lookup"><span data-stu-id="0786a-114">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="0786a-115">Skilgreina verður gæðatengingafærslu fyrir hvert afbrigði viðskiptaferlis.</span><span class="sxs-lookup"><span data-stu-id="0786a-115">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="0786a-116">Til dæmis er hægt að setja upp gæðatengingu sem myndar gæðapöntun þegar innhreyfingarskjal afurða innkaupapöntun er uppfært.</span><span class="sxs-lookup"><span data-stu-id="0786a-116">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="0786a-117">Það fer eftir uppsetningu á keyrsluáætlun hvort hægt sé að stöðva kveikjuferlið sjálft á meðan gæðapöntun er opin.</span><span class="sxs-lookup"><span data-stu-id="0786a-117">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order.</span></span> <span data-ttu-id="0786a-118">Einnig er hægt að loka á síðari ferli, t.d. innkaupapantanir og reikninga.</span><span class="sxs-lookup"><span data-stu-id="0786a-118">Alternatively, subsequent processes, such as purchase order invoicing, can be blocked.</span></span>

> [!NOTE]
> <span data-ttu-id="0786a-119">Meðan gæðapantanir eru opnar er birgðamagn sjálfkrafa stöðvað til útgáfu.</span><span class="sxs-lookup"><span data-stu-id="0786a-119">While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="0786a-120">Það fer eftir **Alger stöðvun** stillingunni á síðunni **Vörusýnishorn** hvort magn sé annaðhvort magn í gæðapöntun eða magn í upprunaskjalslínu.</span><span class="sxs-lookup"><span data-stu-id="0786a-120">Depending on the setting of the **Full blocking** field on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span> <span data-ttu-id="0786a-121">Frekari upplýsingar er að finna í [Vörusýnataka gæðastjórnunar](quality-item-sampling.md).</span><span class="sxs-lookup"><span data-stu-id="0786a-121">For more information, see [Quality management item sampling](quality-item-sampling.md).</span></span>

<span data-ttu-id="0786a-122">Fyrir tiltekið viðskiptaferli auðkennir gæðatengingarfærslan tilvik og skilyrði sem mynda skal gæðapöntun fyrir.</span><span class="sxs-lookup"><span data-stu-id="0786a-122">For a given business process, the quality association record identifies the event and conditions that a quality order is generated for.</span></span> <span data-ttu-id="0786a-123">Skilyrðin geta átt sérstaklega við svæði eða lögaðila.</span><span class="sxs-lookup"><span data-stu-id="0786a-123">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="0786a-124">Aðeins er hægt að mynda gæðapöntun sem felur í sér eyðileggingarprófun þegar lagerbirgðir eru til staðar fyrir tilvikið.</span><span class="sxs-lookup"><span data-stu-id="0786a-124">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="0786a-125">Til að vinna með gæðatengingar skal fara í **Birgðastjórnun \> Uppsetning \> Gæðastjórnun \> Gæðatengingar**.</span><span class="sxs-lookup"><span data-stu-id="0786a-125">To work with quality associations, go to **Inventory management \> Setup \> Quality control \> Quality associations**.</span></span> <span data-ttu-id="0786a-126">Eftirfarandi dæmi sýna hvernig gæðatengingafærsla er skilgreind fyrir afbrigði hvers viðskiptaferlis.</span><span class="sxs-lookup"><span data-stu-id="0786a-126">The following examples show how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="0786a-127">Í eftirfarandi töflu eru dæmin tekin saman eftir tilviki og skilyrðum sem skilgreind eru af gæðatengingarfærslu.</span><span class="sxs-lookup"><span data-stu-id="0786a-127">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0786a-128">Gerð tilvísunar</span><span class="sxs-lookup"><span data-stu-id="0786a-128">Reference type</span></span></th>
<th><span data-ttu-id="0786a-129">Gerð tilviks</span><span class="sxs-lookup"><span data-stu-id="0786a-129">Event type</span></span></th>
<th><span data-ttu-id="0786a-130">Framkvæmd</span><span class="sxs-lookup"><span data-stu-id="0786a-130">Execution</span></span></th>
<th><span data-ttu-id="0786a-131">Lokun tilviks</span><span class="sxs-lookup"><span data-stu-id="0786a-131">Event blocking</span></span></th>
<th><span data-ttu-id="0786a-132">Tilvísun skjals</span><span class="sxs-lookup"><span data-stu-id="0786a-132">Document reference</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0786a-133">Birgðir</span><span class="sxs-lookup"><span data-stu-id="0786a-133">Inventory</span></span></td>
<td><span data-ttu-id="0786a-134">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="0786a-134">Not applicable</span></span></td>
<td><span data-ttu-id="0786a-135">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="0786a-135">Not applicable</span></span></td>
<td><span data-ttu-id="0786a-136">Ekkert</span><span class="sxs-lookup"><span data-stu-id="0786a-136">None</span></span></td>
<td><span data-ttu-id="0786a-137">Allt</span><span class="sxs-lookup"><span data-stu-id="0786a-137">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="0786a-138">Sala</span><span class="sxs-lookup"><span data-stu-id="0786a-138">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="0786a-139">Tiltektarferli er áætlað</span><span class="sxs-lookup"><span data-stu-id="0786a-139">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="0786a-140">Fyrir</span><span class="sxs-lookup"><span data-stu-id="0786a-140">Before</span></span></td>
<td><span data-ttu-id="0786a-141">Ekkert</span><span class="sxs-lookup"><span data-stu-id="0786a-141">None</span></span></td>
<td rowspan="22"><span data-ttu-id="0786a-142">Tilgreint kenni, Flokkur eða Allir aðeins</span><span class="sxs-lookup"><span data-stu-id="0786a-142">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-143">Tiltektarferli</span><span class="sxs-lookup"><span data-stu-id="0786a-143">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-144">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="0786a-144">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-145">Reikningur</span><span class="sxs-lookup"><span data-stu-id="0786a-145">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0786a-146">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="0786a-146">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="0786a-147">Fyrir</span><span class="sxs-lookup"><span data-stu-id="0786a-147">Before</span></span></td>
<td><span data-ttu-id="0786a-148">Ekkert</span><span class="sxs-lookup"><span data-stu-id="0786a-148">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-149">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="0786a-149">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-150">Reikningur</span><span class="sxs-lookup"><span data-stu-id="0786a-150">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="0786a-151">Innkaup</span><span class="sxs-lookup"><span data-stu-id="0786a-151">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="0786a-152">Innhreyfingaskjal</span><span class="sxs-lookup"><span data-stu-id="0786a-152">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="0786a-153">Fyrir</span><span class="sxs-lookup"><span data-stu-id="0786a-153">Before</span></span></td>
<td><span data-ttu-id="0786a-154">Ekkert</span><span class="sxs-lookup"><span data-stu-id="0786a-154">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-155">Innhreyfingaskjal</span><span class="sxs-lookup"><span data-stu-id="0786a-155">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-156">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="0786a-156">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-157">Reikningur</span><span class="sxs-lookup"><span data-stu-id="0786a-157">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0786a-158">Eftir</span><span class="sxs-lookup"><span data-stu-id="0786a-158">After</span></span></td>
<td><span data-ttu-id="0786a-159">Ekkert</span><span class="sxs-lookup"><span data-stu-id="0786a-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-160">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="0786a-160">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-161">Reikningur</span><span class="sxs-lookup"><span data-stu-id="0786a-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0786a-162">Skráning</span><span class="sxs-lookup"><span data-stu-id="0786a-162">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="0786a-163">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="0786a-163">Not applicable</span></span></td>
<td><span data-ttu-id="0786a-164">Ekkert</span><span class="sxs-lookup"><span data-stu-id="0786a-164">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-165">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="0786a-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-166">Reikningur</span><span class="sxs-lookup"><span data-stu-id="0786a-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="0786a-167">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="0786a-167">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="0786a-168">Fyrir</span><span class="sxs-lookup"><span data-stu-id="0786a-168">Before</span></span></td>
<td><span data-ttu-id="0786a-169">Ekkert</span><span class="sxs-lookup"><span data-stu-id="0786a-169">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-170">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="0786a-170">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-171">Reikningur</span><span class="sxs-lookup"><span data-stu-id="0786a-171">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0786a-172">Eftir</span><span class="sxs-lookup"><span data-stu-id="0786a-172">After</span></span></td>
<td><span data-ttu-id="0786a-173">Ekkert</span><span class="sxs-lookup"><span data-stu-id="0786a-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-174">Reikningur</span><span class="sxs-lookup"><span data-stu-id="0786a-174">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="0786a-175">Framleiðsla</span><span class="sxs-lookup"><span data-stu-id="0786a-175">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="0786a-176">Skráning</span><span class="sxs-lookup"><span data-stu-id="0786a-176">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="0786a-177">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="0786a-177">Not applicable</span></span></td>
<td><span data-ttu-id="0786a-178">Ekkert</span><span class="sxs-lookup"><span data-stu-id="0786a-178">None</span></span></td>
<td rowspan="12"><span data-ttu-id="0786a-179">Allt</span><span class="sxs-lookup"><span data-stu-id="0786a-179">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-180">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="0786a-180">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-181">Við skil</span><span class="sxs-lookup"><span data-stu-id="0786a-181">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="0786a-182">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="0786a-182">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="0786a-183">Fyrir</span><span class="sxs-lookup"><span data-stu-id="0786a-183">Before</span></span></td>
<td><span data-ttu-id="0786a-184">Ekkert</span><span class="sxs-lookup"><span data-stu-id="0786a-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-185">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="0786a-185">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-186">Við skil</span><span class="sxs-lookup"><span data-stu-id="0786a-186">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0786a-187">Eftir</span><span class="sxs-lookup"><span data-stu-id="0786a-187">After</span></span></td>
<td><span data-ttu-id="0786a-188">Ekkert</span><span class="sxs-lookup"><span data-stu-id="0786a-188">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-189">Við skil</span><span class="sxs-lookup"><span data-stu-id="0786a-189">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="0786a-190">Biðgeymsla</span><span class="sxs-lookup"><span data-stu-id="0786a-190">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="0786a-191">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="0786a-191">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="0786a-192">Fyrir</span><span class="sxs-lookup"><span data-stu-id="0786a-192">Before</span></span></td>
<td><span data-ttu-id="0786a-193">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="0786a-193">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-194">Við skil</span><span class="sxs-lookup"><span data-stu-id="0786a-194">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-195">Eftir</span><span class="sxs-lookup"><span data-stu-id="0786a-195">After</span></span></td>
<td><span data-ttu-id="0786a-196">Við skil</span><span class="sxs-lookup"><span data-stu-id="0786a-196">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-197">Við skil</span><span class="sxs-lookup"><span data-stu-id="0786a-197">End</span></span></td>
<td><span data-ttu-id="0786a-198">Fyrir</span><span class="sxs-lookup"><span data-stu-id="0786a-198">Before</span></span></td>
<td><span data-ttu-id="0786a-199">Við skil</span><span class="sxs-lookup"><span data-stu-id="0786a-199">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0786a-200">Leiðaraðgerð</span><span class="sxs-lookup"><span data-stu-id="0786a-200">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="0786a-201">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="0786a-201">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="0786a-202">Fyrir</span><span class="sxs-lookup"><span data-stu-id="0786a-202">Before</span></span></td>
<td><span data-ttu-id="0786a-203">Engum</span><span class="sxs-lookup"><span data-stu-id="0786a-203">None</span></span></td>
<td rowspan="3"><span data-ttu-id="0786a-204">Tiltekið kenni, flokkur eða allt og tiltekið tilfang, flokkur eða allt</span><span class="sxs-lookup"><span data-stu-id="0786a-204">Specific ID, Group, or All, and specific Resource, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-205">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="0786a-205">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-206">Eftir</span><span class="sxs-lookup"><span data-stu-id="0786a-206">After</span></span></td>
<td><span data-ttu-id="0786a-207">Engum</span><span class="sxs-lookup"><span data-stu-id="0786a-207">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="0786a-208">Framleiðsla aukaafurðar</span><span class="sxs-lookup"><span data-stu-id="0786a-208">Co-product production</span></span></td>
<td><span data-ttu-id="0786a-209">Skráning</span><span class="sxs-lookup"><span data-stu-id="0786a-209">Registration</span></span></td>
<td><span data-ttu-id="0786a-210">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="0786a-210">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="0786a-211">Engum</span><span class="sxs-lookup"><span data-stu-id="0786a-211">None</span></span></td>
<td rowspan="3"><span data-ttu-id="0786a-212">Allir</span><span class="sxs-lookup"><span data-stu-id="0786a-212">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="0786a-213">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="0786a-213">Report as finished</span></span></td>
<td><span data-ttu-id="0786a-214">Fyrir</span><span class="sxs-lookup"><span data-stu-id="0786a-214">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-215">Eftir</span><span class="sxs-lookup"><span data-stu-id="0786a-215">After</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="0786a-216">Eiginleikinn *Gæðastjórnun fyrir vöruhúsaferli* bætir við möguleikum fyrir úrvinnslu gæðapantana fyrir framleiðslu þar sem **Gerð tilviks** er stillt á *Tilkynna sem lokið* og reiturinn **Framkvæmd** er stilltur á *Eftir á* og fyrir innkaup þar sem reiturinn **Gerð tilviks** er stilltur á *Skráning*.</span><span class="sxs-lookup"><span data-stu-id="0786a-216">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production where the **Event type** field is set to *Report as finished* and the **Execution** field is set to *After*, and for purchases where the **Event type** field is set to *Registration*.</span></span> <span data-ttu-id="0786a-217">Frekari upplýsingar er að finna í [Gæðastjórnun fyrir vöruhúsaferli](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="0786a-217">For more information, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

<span data-ttu-id="0786a-218">Eftirfarandi tafla veitir frekari upplýsingar um hvernig hægt er að mynda gæðapantanir fyrir tilgreindar gerðir ferla.</span><span class="sxs-lookup"><span data-stu-id="0786a-218">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>

<div class="tableSection">
<table>
<thead>
<tr>
<th><span data-ttu-id="0786a-219">Gerð ferlis</span><span class="sxs-lookup"><span data-stu-id="0786a-219">Type of process</span></span></th>
<th><span data-ttu-id="0786a-220">Þegar hægt er að mynda gæðapantanir sjálfvirkt</span><span class="sxs-lookup"><span data-stu-id="0786a-220">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="0786a-221">Þegar hægt er að mynda gæðapantanir ef eyðileggingarprófun er áskilin</span><span class="sxs-lookup"><span data-stu-id="0786a-221">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="0786a-222">Upplýsingar um skilyrði</span><span class="sxs-lookup"><span data-stu-id="0786a-222">Condition information</span></span></th>
<th><span data-ttu-id="0786a-223">Upplýsingar um handvirka myndun</span><span class="sxs-lookup"><span data-stu-id="0786a-223">Manual generation information</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0786a-224">Innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="0786a-224">Purchase order</span></span></td>
<td><span data-ttu-id="0786a-225">Á undan eða eftir komulista eða innhreyfingarskjal afurða fyrir efni sem er móttekið er bókuð</span><span class="sxs-lookup"><span data-stu-id="0786a-225">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="0786a-226">Eftir innhreyfingarskjal afurða fyrir efni sem er móttekið er bókað, þar sem efnið verður að vera tiltækt fyrir eyðileggingarprófun</span><span class="sxs-lookup"><span data-stu-id="0786a-226">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="0786a-227">Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða lánardrottins eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="0786a-227">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="0786a-228">Gæðapöntun sem er stofnuð handvirkt og vísar í innkaupapöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="0786a-228">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-229">Biðgeymslupöntun</span><span class="sxs-lookup"><span data-stu-id="0786a-229">Quarantine order</span></span></td>
<td><span data-ttu-id="0786a-230">Á undan eða eftir biðgeymslupöntunin er skráð sem lokið eða lokið</span><span class="sxs-lookup"><span data-stu-id="0786a-230">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="0786a-231">Ekki er hægt að mynda gæðapantanir sem krefjast eyðileggingarprófana.</span><span class="sxs-lookup"><span data-stu-id="0786a-231">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="0786a-232">Gert er ráð fyrir að virkni biðgeymslupöntunar annist ráðstöfun á efni sem er eyðilagt.</span><span class="sxs-lookup"><span data-stu-id="0786a-232">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="0786a-233">Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða lánardrottins eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="0786a-233">The requirement for a quality order can reflect a specific site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="0786a-234">Gæðapöntun sem er stofnuð handvirkt og vísar í biðgeymslupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="0786a-234">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-235">Sölupöntun</span><span class="sxs-lookup"><span data-stu-id="0786a-235">Sales order</span></span></td>
<td><span data-ttu-id="0786a-236">Á undan á áætluðu tiltektarferli eða fylgiseðilsuppfærslu fyrir vörur sem verið er að senda</span><span class="sxs-lookup"><span data-stu-id="0786a-236">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="0786a-237">Á hvaða þrepi sem er</span><span class="sxs-lookup"><span data-stu-id="0786a-237">At any step</span></span></td>
<td><span data-ttu-id="0786a-238">Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða viðskiptavinar eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="0786a-238">The requirement for a quality order can reflect a specific site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="0786a-239">Gæðapöntun sem er stofnuð handvirkt og vísar í sölupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="0786a-239">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-240">Framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="0786a-240">Production order</span></span></td>
<td><span data-ttu-id="0786a-241">Á undan eða eftir að tilbúið magn fyrir framleiðslupöntun er skráð</span><span class="sxs-lookup"><span data-stu-id="0786a-241">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="0786a-242">Eftir að tilbúið magn fyrir framleiðslupöntun er skráð</span><span class="sxs-lookup"><span data-stu-id="0786a-242">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="0786a-243">Þörf á gæðapöntun getur verið vegna tiltekins svæðis eða vöru eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="0786a-243">The requirement for a quality order can reflect a specific site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="0786a-244">Gæðapöntun sem er stofnuð handvirkt og vísar í framleiðslupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="0786a-244">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-245">Framleiðslupöntun sem er með leiðaraðgerð</span><span class="sxs-lookup"><span data-stu-id="0786a-245">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="0786a-246">Á undan eða eftir að skýrslu er lokið fyrir aðgerð</span><span class="sxs-lookup"><span data-stu-id="0786a-246">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="0786a-247">Á undan eða eftir að skýrsluframleiðslu er lokið fyrir síðustu aðgerð</span><span class="sxs-lookup"><span data-stu-id="0786a-247">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="0786a-248">Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða rekstrartilfanga eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="0786a-248">The requirement for a quality order can reflect a specific site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="0786a-249">Gæðapöntun sem er stofnuð handvirkt og vísar í leiðaraðgerð getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="0786a-249">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="0786a-250">Birgðir</span><span class="sxs-lookup"><span data-stu-id="0786a-250">Inventory</span></span></td>
<td><span data-ttu-id="0786a-251">Ekki er hægt að mynda gæðapöntun sjálfkrafa fyrir færslu í birgðabók eða fyrir flutningspantanafærslur.</span><span class="sxs-lookup"><span data-stu-id="0786a-251">A quality order can't be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="0786a-252">Stofna verður gæðapöntun handvirkt fyrir birgðamagn vöru.</span><span class="sxs-lookup"><span data-stu-id="0786a-252">A quality order must be manually created for an item's inventory quantity.</span></span> <span data-ttu-id="0786a-253">Efnislegra lagerbirgða er krafist.</span><span class="sxs-lookup"><span data-stu-id="0786a-253">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>
</div>

## <a name="examples-of-automatic-generation-of-quality-orders"></a><span data-ttu-id="0786a-254">Dæmi um sjálfvirka myndun þjónustupantana</span><span class="sxs-lookup"><span data-stu-id="0786a-254">Examples of automatic generation of quality orders</span></span>

### <a name="purchasing"></a><span data-ttu-id="0786a-255">Innkaup</span><span class="sxs-lookup"><span data-stu-id="0786a-255">Purchasing</span></span>

<span data-ttu-id="0786a-256">Í innkaupum, ef þú stillir reitinn **Gerð tilviks** á *Innhreyfingarskjal afurðar* og reitinn **Framkvæmd** á *Eftir* á síðunni **Gæðatengingar** færðu eftirfarandi niðurstöður:</span><span class="sxs-lookup"><span data-stu-id="0786a-256">In purchasing, if you set the **Event type** field to *Product receipt* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="0786a-257">Ef valkosturinn **Eftir uppfærðu magni** er stilltur á *Já* myndast gæðapöntun fyrir hverja innhreyfingu gegn innkaupapöntuninni, byggð á mótteknu magni og stillingum í vörusýni.</span><span class="sxs-lookup"><span data-stu-id="0786a-257">If the **Per updated quantity** option is set to *Yes*, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="0786a-258">Í hvert skipti sem magn er móttekið gegn innkaupapöntuninni myndast nýjar gæðapantanir miðað við nýlega fengið magn.</span><span class="sxs-lookup"><span data-stu-id="0786a-258">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="0786a-259">Ef valkosturinn **Eftir uppfærðu magni** er stilltur á *Nei* myndast gæðapöntun fyrir fyrstu innhreyfinguna gegn innkaupapöntuninni, byggð á mótteknu magni.</span><span class="sxs-lookup"><span data-stu-id="0786a-259">If the **Per updated quantity** option is set to *No*, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="0786a-260">Að auki eru ein eða fleiri gæðapantanir búnar til miðað við eftirstandandi magn, eftir því hverjar rakningarvíddirnar eru.</span><span class="sxs-lookup"><span data-stu-id="0786a-260">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="0786a-261">Gæðapantanir eru ekki myndaðar fyrir síðari innhreyfingar gegn innkaupapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="0786a-261">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="0786a-262">Vinnsla</span><span class="sxs-lookup"><span data-stu-id="0786a-262">Production</span></span>

<span data-ttu-id="0786a-263">Í framleiðslu, ef þú stillir reitinn **Gerð tilviks** á *Tilkynna sem lokið* og reitinn **Framkvæmd** á *Eftir* á síðunni **Gæðatengingar** færðu eftirfarandi niðurstöður:</span><span class="sxs-lookup"><span data-stu-id="0786a-263">In production, if you set the **Event type** field to *Report as finished* and the **Execution** field to *After* on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="0786a-264">Ef valkosturinn **Eftir uppfærðu magni** er stilltur á *Já* myndast gæðapöntun fyrir hvert lokið magn og stillingar í vörusýni.</span><span class="sxs-lookup"><span data-stu-id="0786a-264">If the **Per updated quantity** option is set to *Yes*, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="0786a-265">Í hvert sinn sem magn er skráð sem lokið gagnvart framleiðslupöntuninni eru nýjar gæðapantanir búnar til út frá nýlega loknu magni.</span><span class="sxs-lookup"><span data-stu-id="0786a-265">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on the newly finished quantity.</span></span> <span data-ttu-id="0786a-266">Þessi myndunarrök eru í samræmi við innkaup.</span><span class="sxs-lookup"><span data-stu-id="0786a-266">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="0786a-267">Ef valkosturinn **Eftir uppfærðu magni** er stilltur á *Nei* myndast gæðapöntun fyrir fyrsta skiptið sem magn er tilkynnt sem lokið, byggt á loknu magni.</span><span class="sxs-lookup"><span data-stu-id="0786a-267">If the **Per updated quantity** option is set to *No*, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="0786a-268">Að auki eru ein eða fleiri gæðapantanir búnar til miðað við eftirstandandi magn, eftir því hverjar rakningarvíddirnar eru í vörusýninu.</span><span class="sxs-lookup"><span data-stu-id="0786a-268">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="0786a-269">Gæðapantanir eru ekki búnar til fyrir seinna lokið magn.</span><span class="sxs-lookup"><span data-stu-id="0786a-269">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="0786a-270">Gæðaforskriftir</span><span class="sxs-lookup"><span data-stu-id="0786a-270">Quality specification</span></span></th>
<th><span data-ttu-id="0786a-271">Uppfært magn á</span><span class="sxs-lookup"><span data-stu-id="0786a-271">Per updated quantity</span></span></th>
<th><span data-ttu-id="0786a-272">Á rakningarvídd</span><span class="sxs-lookup"><span data-stu-id="0786a-272">Per tracking dimension</span></span></th>
<th><span data-ttu-id="0786a-273">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="0786a-273">Result</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="0786a-274">Prósenta: 10%</span><span class="sxs-lookup"><span data-stu-id="0786a-274">Percentage: 10%</span></span></td>
<td><span data-ttu-id="0786a-275">Já</span><span class="sxs-lookup"><span data-stu-id="0786a-275">Yes</span></span></td>
<td>
<p><span data-ttu-id="0786a-276">Rununúmer: Nr.</span><span class="sxs-lookup"><span data-stu-id="0786a-276">Batch number: No</span></span></p>
<p><span data-ttu-id="0786a-277">Raðnúmer: Nr.</span><span class="sxs-lookup"><span data-stu-id="0786a-277">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="0786a-278">Pöntunarmagn: 100</span><span class="sxs-lookup"><span data-stu-id="0786a-278">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="0786a-279">Tilkynna sem lokið fyrir 30</span><span class="sxs-lookup"><span data-stu-id="0786a-279">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="0786a-280">Gæðapöntun 1 fyrir 3 (10% af 30)</span><span class="sxs-lookup"><span data-stu-id="0786a-280">Quality order 1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="0786a-281">Tilkynna sem lokið fyrir 70</span><span class="sxs-lookup"><span data-stu-id="0786a-281">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="0786a-282">Gæðapöntun 2 fyrir 7 (10% eftirstandandi pöntunarmagn, sem er 70 í þessu tilviki)</span><span class="sxs-lookup"><span data-stu-id="0786a-282">Quality order 2 for 7 (10% of the remaining order quantity, which is 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="0786a-283">Fast magn: 1</span><span class="sxs-lookup"><span data-stu-id="0786a-283">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="0786a-284">Ekkert</span><span class="sxs-lookup"><span data-stu-id="0786a-284">No</span></span></td>
<td>
<p><span data-ttu-id="0786a-285">Rununúmer: Nr.</span><span class="sxs-lookup"><span data-stu-id="0786a-285">Batch number: No</span></span></p>
<p><span data-ttu-id="0786a-286">Raðnúmer: Nr.</span><span class="sxs-lookup"><span data-stu-id="0786a-286">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="0786a-287">Pöntunarmagn: 100</span><span class="sxs-lookup"><span data-stu-id="0786a-287">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="0786a-288">Tilkynna sem lokið fyrir 30</span><span class="sxs-lookup"><span data-stu-id="0786a-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="0786a-289">Gæðapöntun 1 fyrir 1 (fyrir fyrsta tilkynnta sem lokið magn, sem hefur föst gildi 1)</span><span class="sxs-lookup"><span data-stu-id="0786a-289">Quality order 1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="0786a-290">Gæðapöntun 2 fyrir 1 (fyrir eftirstandandi magn, sem er enn með fast gildi 1)</span><span class="sxs-lookup"><span data-stu-id="0786a-290">Quality order 2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="0786a-291">Tilkynna sem lokið fyrir 10</span><span class="sxs-lookup"><span data-stu-id="0786a-291">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="0786a-292">Engar gæðapantanir eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="0786a-292">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="0786a-293">Tilkynna sem lokið fyrir 60</span><span class="sxs-lookup"><span data-stu-id="0786a-293">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="0786a-294">Engar gæðapantanir eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="0786a-294">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="0786a-295">Fast magn: 1</span><span class="sxs-lookup"><span data-stu-id="0786a-295">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="0786a-296">Já</span><span class="sxs-lookup"><span data-stu-id="0786a-296">Yes</span></span></td>
<td>
<p><span data-ttu-id="0786a-297">Rununúmer: Já</span><span class="sxs-lookup"><span data-stu-id="0786a-297">Batch number: Yes</span></span></p>
<p><span data-ttu-id="0786a-298">Raðnúmer: Já</span><span class="sxs-lookup"><span data-stu-id="0786a-298">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="0786a-299">Pöntunarmagn: 10</span><span class="sxs-lookup"><span data-stu-id="0786a-299">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="0786a-300">Tilkynna sem lokið fyrir 3: 1 fyrir rununúmer b1, raðnúmer s1; 1 fyrir rununúmer b2, raðnúmer s2; og 1 fyrir rununúmer b3, raðnúmer s3</span><span class="sxs-lookup"><span data-stu-id="0786a-300">Report as finished for 3: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; and 1 for batch number b3, serial number s3</span></span>
<ul>
<li><span data-ttu-id="0786a-301">Gæðapöntun 1 fyrir 1 af lotunúmeri b1, raðnúmer s1</span><span class="sxs-lookup"><span data-stu-id="0786a-301">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="0786a-302">Gæðapöntun 2 fyrir 1 lotunúmer b2, raðnúmer s2</span><span class="sxs-lookup"><span data-stu-id="0786a-302">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="0786a-303">Gæðapöntun 3 fyrir 1 lotunúmer b3, raðnúmer s3</span><span class="sxs-lookup"><span data-stu-id="0786a-303">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="0786a-304">Tilkynna sem lokið fyrir 2: 1 fyrir rununúmer b4, raðnúmer s4; og 1 fyrir rununúmer b5, raðnúmer s5</span><span class="sxs-lookup"><span data-stu-id="0786a-304">Report as finished for 2: 1 for batch number b4, serial number s4; and 1 for batch number b5, serial number s5</span></span>
<ul>
<li><span data-ttu-id="0786a-305">Gæðapöntun 4 fyrir 1 lotunúmer b4, raðnúmer s4</span><span class="sxs-lookup"><span data-stu-id="0786a-305">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
<li><span data-ttu-id="0786a-306">Gæðapöntun 5 fyrir 1 lotunúmer b5, raðnúmer s5</span><span class="sxs-lookup"><span data-stu-id="0786a-306">Quality order 5 for 1 of batch number b5, serial number s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="0786a-307"><strong>Ath.:</strong> Hægt er að endurnýta rununa.</span><span class="sxs-lookup"><span data-stu-id="0786a-307"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="0786a-308">Fast magn: 2</span><span class="sxs-lookup"><span data-stu-id="0786a-308">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="0786a-309">Ekkert</span><span class="sxs-lookup"><span data-stu-id="0786a-309">No</span></span></td>
<td>
<p><span data-ttu-id="0786a-310">Rununúmer: Já</span><span class="sxs-lookup"><span data-stu-id="0786a-310">Batch number: Yes</span></span></p>
<p><span data-ttu-id="0786a-311">Raðnúmer: Já</span><span class="sxs-lookup"><span data-stu-id="0786a-311">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="0786a-312">Pöntunarmagn: 10</span><span class="sxs-lookup"><span data-stu-id="0786a-312">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="0786a-313">Tilkynna sem lokið fyrir 4: 1 fyrir rununúmer b1, raðnúmer s1; 1 fyrir rununúmer b2, raðnúmer s2; 1 fyrir rununúmer b3, raðnúmer s3; og 1 fyrir rununúmer b4, raðnúmer s4</span><span class="sxs-lookup"><span data-stu-id="0786a-313">Report as finished for 4: 1 for batch number b1, serial number s1; 1 for batch number b2, serial number s2; 1 for batch number b3, serial number s3; and 1 for batch number b4, serial number s4</span></span>
<ul>
<li><span data-ttu-id="0786a-314">Gæðapöntun 1 fyrir 1 af lotunúmeri b1, raðnúmer s1</span><span class="sxs-lookup"><span data-stu-id="0786a-314">Quality order 1 for 1 of batch number b1, serial number s1</span></span></li>
<li><span data-ttu-id="0786a-315">Gæðapöntun 2 fyrir 1 lotunúmer b2, raðnúmer s2</span><span class="sxs-lookup"><span data-stu-id="0786a-315">Quality order 2 for 1 of batch number b2, serial number s2</span></span></li>
<li><span data-ttu-id="0786a-316">Gæðapöntun 3 fyrir 1 lotunúmer b3, raðnúmer s3</span><span class="sxs-lookup"><span data-stu-id="0786a-316">Quality order 3 for 1 of batch number b3, serial number s3</span></span></li>
<li><span data-ttu-id="0786a-317">Gæðapöntun 4 fyrir 1 lotunúmer b4, raðnúmer s4</span><span class="sxs-lookup"><span data-stu-id="0786a-317">Quality order 4 for 1 of batch number b4, serial number s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="0786a-318">Gæðapöntun 5 fyrir 2, án tilvísunar í lotunúmer og raðnúmer</span><span class="sxs-lookup"><span data-stu-id="0786a-318">Quality order 5 for 2, without a reference to a batch number and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="0786a-319">Tilkynna sem lokið fyrir 6: 1 fyrir rununúmer b5, raðnúmer s5; 1 fyrir rununúmer b6, raðnúmer s6; 1 fyrir rununúmer b7, raðnúmer s7; 1 fyrir rununúmer b8, raðnúmer s8; 1 fyrir rununúmer b9, raðnúmer s9; og 1 fyrir rununúmer b10, raðnúmer s10</span><span class="sxs-lookup"><span data-stu-id="0786a-319">Report as finished for 6: 1 for batch number b5, serial number s5; 1 for batch number b6, serial number s6; 1 for batch number b7, serial number s7; 1 for batch number b8, serial number s8; 1 for batch number b9, serial number s9; and 1 for batch number b10, serial number s10</span></span>
<ul>
<li><span data-ttu-id="0786a-320">Engar gæðapantanir eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="0786a-320">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="0786a-321">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="0786a-321">Additional resources</span></span>

- [<span data-ttu-id="0786a-322">Gæðastjórnunarferli</span><span class="sxs-lookup"><span data-stu-id="0786a-322">Quality management processes</span></span>](quality-management-processes.md)
- [<span data-ttu-id="0786a-323">Virkja stjórnun gæða og ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="0786a-323">Enable quality and nonconformance management</span></span>](enable-quality-management.md)
- [<span data-ttu-id="0786a-324">Gæðastjórnun fyrir vöruhúsaferli</span><span class="sxs-lookup"><span data-stu-id="0786a-324">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
