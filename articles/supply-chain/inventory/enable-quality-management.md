---
title: Yfirlit yfir gæðastjórnun
description: Þessi grein lýsir því hvernig hægt er að nota gæðastjórnun í Dynamics 365 Supply Chain Management til að bæta gæði afurða innan aðfangakeðju þinnar.
author: perlynne
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2d51c659d9d06f075458359d81de978e7a6d14b
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814399"
---
# <a name="quality-management-overview"></a><span data-ttu-id="1c227-103">Yfirlit yfir gæðastjórnun</span><span class="sxs-lookup"><span data-stu-id="1c227-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c227-104">Þessi grein lýsir því hvernig hægt er að nota gæðastjórnun í Dynamics 365 Supply Chain Management til að bæta gæði afurða innan aðfangakeðju þinnar.</span><span class="sxs-lookup"><span data-stu-id="1c227-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="1c227-105">Gæðastjórnun getur hjálpað við að stjórna biðtíma þegar ósamkvæmar afurðir eru meðhöndlaðar, óháð uppruna þeirra.</span><span class="sxs-lookup"><span data-stu-id="1c227-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="1c227-106">Þar sem greiningargerðir eru tengdar leiðréttingaskýrslum getur Supply Chain Management raðað verki til að leiðrétta vandamál og komið í veg fyrir þau verði endurtekin.</span><span class="sxs-lookup"><span data-stu-id="1c227-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="1c227-107">Auk virkni fyrir stjórnun ósamkvæmni inniheldur gæðastjórnun virkni til að rekja úthreyfingar eftir gerð vanda (jafnvel innri vandamál) og til að auðkenna lausnir sem skammtíma- eða langtímalausnir.</span><span class="sxs-lookup"><span data-stu-id="1c227-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="1c227-108">Upplýsingar um afkastavísi (KPI) veita innsýn í sögulegan feril fyrri vandamála með ósamkvæmi og þeirra lausna sem voru notuð til að leiðrétta þau.</span><span class="sxs-lookup"><span data-stu-id="1c227-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="1c227-109">Hægt er að nota söguleg gögn til að fara yfir skilvirkni fyrri gæðaráðstafana og ákvarða viðeigandi mælieiningar sem nota á í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="1c227-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="1c227-110">Þegar gæðatenging er sett upp getur Supply Chain Management myndað gæðapantanir fyrir ýmis viðskiptaferli, tilvik og skilyrði.</span><span class="sxs-lookup"><span data-stu-id="1c227-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="1c227-111">Gæðatengingin getur náð yfir ákveðna vöru, einstökan vöruflokk eða allar vörur.</span><span class="sxs-lookup"><span data-stu-id="1c227-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="1c227-112">Dæmi um notkun á gæðastjórnun</span><span class="sxs-lookup"><span data-stu-id="1c227-112">Examples of the use of quality management</span></span>
<span data-ttu-id="1c227-113">Gæðastjórnun er sveigjanleg og hægt er að innleiða hana á mismunandi vegu til að uppfylla kröfur um tiltekið stig í aðgerðum framboðskeðju.</span><span class="sxs-lookup"><span data-stu-id="1c227-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="1c227-114">Eftirfarandi dæmi sýna hugsanlega notkun á þessum eiginleikum:</span><span class="sxs-lookup"><span data-stu-id="1c227-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="1c227-115">Hefja ferli gæðaeftirlits sjálfvirkt, byggt á fyrirfram skilgreindum skilyrðum (við vöruhússkráningu innkaupapöntunar frá tilteknum lánardrottni).</span><span class="sxs-lookup"><span data-stu-id="1c227-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="1c227-116">Læsa birgðum við skoðun til að koma í veg fyrir að ósamþykktar birgðir séu notaðar (alger stöðvun á pöntunarmagni innkaup).</span><span class="sxs-lookup"><span data-stu-id="1c227-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="1c227-117">Vörusýnishorn eru notuð sem hluti af gæðatengingu til að skilgreina magn gildandi efnislegra birgða sem verður að skoða.</span><span class="sxs-lookup"><span data-stu-id="1c227-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="1c227-118">Sýnishorn geta verið byggð á föstu magni eða hlutfalli.</span><span class="sxs-lookup"><span data-stu-id="1c227-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="1c227-119">Stofna gæðapantanir fyrir hluta móttöku.</span><span class="sxs-lookup"><span data-stu-id="1c227-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="1c227-120">Til að stofna gæðapöntun sem byggir á magni sem tekið er við efnislega með pöntun verður að velja gátreitinn **Eftir uppfærðu magni** á skjámyndinni **Vörusýnishorn**.</span><span class="sxs-lookup"><span data-stu-id="1c227-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="1c227-121">Stofna prófunargerðir sem innihalda lágmark, hámark og markprófunargildi og framkvæma eigindlega-samanborið við-eigindlega prófun sem hefur fyrirfram skilgreindar niðurstöður villuleitar.</span><span class="sxs-lookup"><span data-stu-id="1c227-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="1c227-122">Tilgreina viðunandi gæðastig (AQL) til að stjórna vikmörkum gæðaráðstafana.</span><span class="sxs-lookup"><span data-stu-id="1c227-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="1c227-123">Tilgreina tilföng sem skoðunaraðgerð krefst, eins og prófunarsvæði og prófunartæki.</span><span class="sxs-lookup"><span data-stu-id="1c227-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="1c227-124">Vinna með gæðatengingar</span><span class="sxs-lookup"><span data-stu-id="1c227-124">Working with quality associations</span></span>
<span data-ttu-id="1c227-125">Viðskiptaferli sem notar gæðatengingu getur verið tengt mismunandi upprunaskjölum, eins og innkaupapöntunum, sölupöntunum eða framleiðslupöntunum.</span><span class="sxs-lookup"><span data-stu-id="1c227-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="1c227-126">Hver gæðatengingafærsla skilgreinir einnig prófanir, viðunandi gæðastig og úrtaksáætlun sem eiga við myndaðar gæðapantanir.</span><span class="sxs-lookup"><span data-stu-id="1c227-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="1c227-127">Skilgreina verður gæðatengingafærslu fyrir hvert afbrigði viðskiptaferlis.</span><span class="sxs-lookup"><span data-stu-id="1c227-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="1c227-128">Til dæmis er hægt að setja upp gæðatengingu sem myndar gæðapöntun þegar innhreyfingarskjal afurða innkaupapöntun er uppfært.</span><span class="sxs-lookup"><span data-stu-id="1c227-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="1c227-129">Það fer eftir uppsetningu á keyrsluáætlun hvort hægt sé að stöðva kveikjuferlið sjálft á meðan gæðapöntun er opin eða hvort hægt sé að stöðva næstu ferli, eins og reikningsfærslu á innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="1c227-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="1c227-130">**Ábending:** Meðan gæðapantanir eru opnar er birgðamagn sjálfkrafa stöðvað til útgáfu.</span><span class="sxs-lookup"><span data-stu-id="1c227-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="1c227-131">Það fer eftir **Alger stöðvun** stillingunni á síðunni **Vörusýnishorn** hvort magn sé annaðhvort magn í gæðapöntun eða magn í upprunaskjalslínu.</span><span class="sxs-lookup"><span data-stu-id="1c227-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="1c227-132">Fyrir tiltekið viðskiptaferli auðkennir gæðatengingarfærslan tilvik og skilyrði sem mynda skal gæðapöntun fyrir.</span><span class="sxs-lookup"><span data-stu-id="1c227-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="1c227-133">Skilyrðin geta átt sérstaklega við svæði eða lögaðila.</span><span class="sxs-lookup"><span data-stu-id="1c227-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="1c227-134">Aðeins er hægt að mynda gæðapöntun sem felur í sér eyðileggingarprófun þegar lagerbirgðir eru til staðar fyrir tilvikið.</span><span class="sxs-lookup"><span data-stu-id="1c227-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="1c227-135">Eftirfarandi dæmi sýna hvernig gæðatengingafærsla er skilgreind fyrir afbrigði hvers viðskiptaferlis.</span><span class="sxs-lookup"><span data-stu-id="1c227-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="1c227-136">Í eftirfarandi töflu eru dæmin tekin saman eftir tilviki og skilyrðum sem skilgreind eru af gæðatengingarfærslu.</span><span class="sxs-lookup"><span data-stu-id="1c227-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="1c227-137">Gerð tilvísunar</span><span class="sxs-lookup"><span data-stu-id="1c227-137">Reference type</span></span></th>
<th><span data-ttu-id="1c227-138">Gerð tilviks</span><span class="sxs-lookup"><span data-stu-id="1c227-138">Event type</span></span></th>
<th><span data-ttu-id="1c227-139">Framkvæmd</span><span class="sxs-lookup"><span data-stu-id="1c227-139">Execution</span></span></th>
<th><span data-ttu-id="1c227-140">Lokun tilviks</span><span class="sxs-lookup"><span data-stu-id="1c227-140">Event blocking</span></span></th>
<th><span data-ttu-id="1c227-141">Tilvísun skjals</span><span class="sxs-lookup"><span data-stu-id="1c227-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="1c227-142">Birgðir</span><span class="sxs-lookup"><span data-stu-id="1c227-142">Inventory</span></span></td>
<td><span data-ttu-id="1c227-143">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="1c227-143">Not applicable</span></span></td>
<td><span data-ttu-id="1c227-144">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="1c227-144">Not applicable</span></span></td>
<td><span data-ttu-id="1c227-145">Ekkert</span><span class="sxs-lookup"><span data-stu-id="1c227-145">None</span></span></td>
<td><span data-ttu-id="1c227-146">Allt</span><span class="sxs-lookup"><span data-stu-id="1c227-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="1c227-147">Sala</span><span class="sxs-lookup"><span data-stu-id="1c227-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="1c227-148">Tiltektarferli er áætlað</span><span class="sxs-lookup"><span data-stu-id="1c227-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="1c227-149">Fyrir</span><span class="sxs-lookup"><span data-stu-id="1c227-149">Before</span></span></td>
<td><span data-ttu-id="1c227-150">Ekkert</span><span class="sxs-lookup"><span data-stu-id="1c227-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="1c227-151">Tilgreint kenni, Flokkur eða Allir aðeins</span><span class="sxs-lookup"><span data-stu-id="1c227-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-152">Tiltektarferli</span><span class="sxs-lookup"><span data-stu-id="1c227-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-153">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="1c227-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-154">Reikningur</span><span class="sxs-lookup"><span data-stu-id="1c227-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1c227-155">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="1c227-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="1c227-156">Fyrir</span><span class="sxs-lookup"><span data-stu-id="1c227-156">Before</span></span></td>
<td><span data-ttu-id="1c227-157">Ekkert</span><span class="sxs-lookup"><span data-stu-id="1c227-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-158">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="1c227-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-159">Reikningur</span><span class="sxs-lookup"><span data-stu-id="1c227-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="1c227-160">Innkaup</span><span class="sxs-lookup"><span data-stu-id="1c227-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="1c227-161">Innhreyfingaskjal</span><span class="sxs-lookup"><span data-stu-id="1c227-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="1c227-162">Fyrir</span><span class="sxs-lookup"><span data-stu-id="1c227-162">Before</span></span></td>
<td><span data-ttu-id="1c227-163">Ekkert</span><span class="sxs-lookup"><span data-stu-id="1c227-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-164">Innhreyfingaskjal</span><span class="sxs-lookup"><span data-stu-id="1c227-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-165">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="1c227-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-166">Reikningur</span><span class="sxs-lookup"><span data-stu-id="1c227-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1c227-167">Eftir</span><span class="sxs-lookup"><span data-stu-id="1c227-167">After</span></span></td>
<td><span data-ttu-id="1c227-168">Ekkert</span><span class="sxs-lookup"><span data-stu-id="1c227-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-169">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="1c227-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-170">Reikningur</span><span class="sxs-lookup"><span data-stu-id="1c227-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1c227-171">Skráning</span><span class="sxs-lookup"><span data-stu-id="1c227-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="1c227-172">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="1c227-172">Not applicable</span></span></td>
<td><span data-ttu-id="1c227-173">Ekkert</span><span class="sxs-lookup"><span data-stu-id="1c227-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-174">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="1c227-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-175">Reikningur</span><span class="sxs-lookup"><span data-stu-id="1c227-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="1c227-176">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="1c227-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="1c227-177">Fyrir</span><span class="sxs-lookup"><span data-stu-id="1c227-177">Before</span></span></td>
<td><span data-ttu-id="1c227-178">Ekkert</span><span class="sxs-lookup"><span data-stu-id="1c227-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-179">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="1c227-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-180">Reikningur</span><span class="sxs-lookup"><span data-stu-id="1c227-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1c227-181">Eftir</span><span class="sxs-lookup"><span data-stu-id="1c227-181">After</span></span></td>
<td><span data-ttu-id="1c227-182">Ekkert</span><span class="sxs-lookup"><span data-stu-id="1c227-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-183">Reikningur</span><span class="sxs-lookup"><span data-stu-id="1c227-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="1c227-184">Framleiðsla</span><span class="sxs-lookup"><span data-stu-id="1c227-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="1c227-185">Skráning</span><span class="sxs-lookup"><span data-stu-id="1c227-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="1c227-186">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="1c227-186">Not applicable</span></span></td>
<td><span data-ttu-id="1c227-187">Ekkert</span><span class="sxs-lookup"><span data-stu-id="1c227-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="1c227-188">Allt</span><span class="sxs-lookup"><span data-stu-id="1c227-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-189">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="1c227-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-190">Við skil</span><span class="sxs-lookup"><span data-stu-id="1c227-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="1c227-191">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="1c227-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="1c227-192">Fyrir</span><span class="sxs-lookup"><span data-stu-id="1c227-192">Before</span></span></td>
<td><span data-ttu-id="1c227-193">Ekkert</span><span class="sxs-lookup"><span data-stu-id="1c227-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-194">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="1c227-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-195">Við skil</span><span class="sxs-lookup"><span data-stu-id="1c227-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1c227-196">Eftir</span><span class="sxs-lookup"><span data-stu-id="1c227-196">After</span></span></td>
<td><span data-ttu-id="1c227-197">Ekkert</span><span class="sxs-lookup"><span data-stu-id="1c227-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-198">Við skil</span><span class="sxs-lookup"><span data-stu-id="1c227-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="1c227-199">Biðgeymsla</span><span class="sxs-lookup"><span data-stu-id="1c227-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="1c227-200">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="1c227-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="1c227-201">Fyrir</span><span class="sxs-lookup"><span data-stu-id="1c227-201">Before</span></span></td>
<td><span data-ttu-id="1c227-202">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="1c227-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-203">Við skil</span><span class="sxs-lookup"><span data-stu-id="1c227-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-204">Eftir</span><span class="sxs-lookup"><span data-stu-id="1c227-204">After</span></span></td>
<td><span data-ttu-id="1c227-205">Við skil</span><span class="sxs-lookup"><span data-stu-id="1c227-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-206">Við skil</span><span class="sxs-lookup"><span data-stu-id="1c227-206">End</span></span></td>
<td><span data-ttu-id="1c227-207">Fyrir</span><span class="sxs-lookup"><span data-stu-id="1c227-207">Before</span></span></td>
<td><span data-ttu-id="1c227-208">Við skil</span><span class="sxs-lookup"><span data-stu-id="1c227-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1c227-209">Leiðaraðgerð</span><span class="sxs-lookup"><span data-stu-id="1c227-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="1c227-210">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="1c227-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="1c227-211">Fyrir</span><span class="sxs-lookup"><span data-stu-id="1c227-211">Before</span></span></td>
<td><span data-ttu-id="1c227-212">Ekkert</span><span class="sxs-lookup"><span data-stu-id="1c227-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="1c227-213">Tilgreitn kenni, Flokkur eða Allt, og Tilfangasértækt, Flokkur eða Allt</span><span class="sxs-lookup"><span data-stu-id="1c227-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-214">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="1c227-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-215">Eftir</span><span class="sxs-lookup"><span data-stu-id="1c227-215">After</span></span></td>
<td><span data-ttu-id="1c227-216">Ekkert</span><span class="sxs-lookup"><span data-stu-id="1c227-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="1c227-217">Framleiðsla aukaafurðar</span><span class="sxs-lookup"><span data-stu-id="1c227-217">Co-product production</span></span></td>
<td><span data-ttu-id="1c227-218">Skráning</span><span class="sxs-lookup"><span data-stu-id="1c227-218">Registration</span></span></td>
<td><span data-ttu-id="1c227-219">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="1c227-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="1c227-220">Ekkert</span><span class="sxs-lookup"><span data-stu-id="1c227-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="1c227-221">Allt</span><span class="sxs-lookup"><span data-stu-id="1c227-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="1c227-222">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="1c227-222">Report as finished</span></span></td>
<td><span data-ttu-id="1c227-223">Fyrir</span><span class="sxs-lookup"><span data-stu-id="1c227-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-224">Eftir</span><span class="sxs-lookup"><span data-stu-id="1c227-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="1c227-225">Eftirfarandi tafla veitir frekari upplýsingar um hvernig hægt er að mynda gæðapantanir fyrir tilgreindar gerðir ferla.</span><span class="sxs-lookup"><span data-stu-id="1c227-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="1c227-226">Gerð ferlis</span><span class="sxs-lookup"><span data-stu-id="1c227-226">Type of process</span></span></th>
<th><span data-ttu-id="1c227-227">Þegar hægt er að mynda gæðapantanir sjálfvirkt</span><span class="sxs-lookup"><span data-stu-id="1c227-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="1c227-228">Þegar hægt er að mynda gæðapantanir ef eyðileggingarprófun er áskilin</span><span class="sxs-lookup"><span data-stu-id="1c227-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="1c227-229">Upplýsingar um skilyrði</span><span class="sxs-lookup"><span data-stu-id="1c227-229">Condition information</span></span></th>
<th><span data-ttu-id="1c227-230">Upplýsingar um handvirka myndun</span><span class="sxs-lookup"><span data-stu-id="1c227-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="1c227-231">Innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="1c227-231">Purchase order</span></span></td>
<td><span data-ttu-id="1c227-232">Á undan eða eftir komulista eða innhreyfingarskjal afurða fyrir efni sem er móttekið er bókuð</span><span class="sxs-lookup"><span data-stu-id="1c227-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="1c227-233">Eftir innhreyfingarskjal afurða fyrir efni sem er móttekið er bókað, þar sem efnið verður að vera tiltækt fyrir eyðileggingarprófun</span><span class="sxs-lookup"><span data-stu-id="1c227-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="1c227-234">Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða lánardrottins eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="1c227-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1c227-235">Gæðapöntun sem er stofnuð handvirkt og vísar í innkaupapöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="1c227-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-236">Biðgeymslupöntun</span><span class="sxs-lookup"><span data-stu-id="1c227-236">Quarantine order</span></span></td>
<td><span data-ttu-id="1c227-237">Á undan eða eftir biðgeymslupöntunin er skráð sem lokið eða lokið</span><span class="sxs-lookup"><span data-stu-id="1c227-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="1c227-238">Ekki er hægt að mynda gæðapantanir sem krefjast eyðileggingarprófana.&#39;</span><span class="sxs-lookup"><span data-stu-id="1c227-238">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="1c227-239">Gert er ráð fyrir að virkni biðgeymslupöntunar annist ráðstöfun á efni sem er eyðilagt.&#39;</span><span class="sxs-lookup"><span data-stu-id="1c227-239">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="1c227-240">Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða lánardrottins eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="1c227-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1c227-241">Gæðapöntun sem er stofnuð handvirkt og vísar í biðgeymslupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="1c227-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-242">Sölupöntun</span><span class="sxs-lookup"><span data-stu-id="1c227-242">Sales order</span></span></td>
<td><span data-ttu-id="1c227-243">Á undan á áætluðu tiltektarferli eða fylgiseðilsuppfærslu fyrir vörur sem verið er að senda</span><span class="sxs-lookup"><span data-stu-id="1c227-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="1c227-244">Á hvaða þrepi sem er</span><span class="sxs-lookup"><span data-stu-id="1c227-244">At any step</span></span></td>
<td><span data-ttu-id="1c227-245">Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða viðskiptavinar eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="1c227-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1c227-246">Gæðapöntun sem er stofnuð handvirkt og vísar í sölupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="1c227-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-247">Framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="1c227-247">Production order</span></span></td>
<td><span data-ttu-id="1c227-248">Á undan eða eftir að tilbúið magn fyrir framleiðslupöntun er skráð</span><span class="sxs-lookup"><span data-stu-id="1c227-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="1c227-249">Eftir að tilbúið magn fyrir framleiðslupöntun er skráð</span><span class="sxs-lookup"><span data-stu-id="1c227-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="1c227-250">Þörf á gæðapöntun getur verið vegna tiltekins svæðis eða vöru eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="1c227-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1c227-251">Gæðapöntun sem er stofnuð handvirkt og vísar í framleiðslupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="1c227-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-252">Framleiðslupöntun sem er með leiðaraðgerð</span><span class="sxs-lookup"><span data-stu-id="1c227-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="1c227-253">Á undan eða eftir að skýrslu er lokið fyrir aðgerð</span><span class="sxs-lookup"><span data-stu-id="1c227-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="1c227-254">Á undan eða eftir að skýrsluframleiðslu er lokið fyrir síðustu aðgerð</span><span class="sxs-lookup"><span data-stu-id="1c227-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="1c227-255">Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða rekstrartilfanga eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="1c227-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="1c227-256">Gæðapöntun sem er stofnuð handvirkt og vísar í leiðaraðgerð getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="1c227-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="1c227-257">Birgðir</span><span class="sxs-lookup"><span data-stu-id="1c227-257">Inventory</span></span></td>
<td><span data-ttu-id="1c227-258">Ekki er hægt að mynda gæðapöntun sjálfkrafa fyrir færslu í birgðabók eða fyrir flutningspantanafærslur.</span><span class="sxs-lookup"><span data-stu-id="1c227-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="1c227-259">Gæðapöntun verður að vera stofnuð handvirkt fyrir birgðamagn vöru.&#39;</span><span class="sxs-lookup"><span data-stu-id="1c227-259">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="1c227-260">Efnislegra lagerbirgða er krafist.</span><span class="sxs-lookup"><span data-stu-id="1c227-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="1c227-261">Dæmi um sjálfvirka myndun á gæðapöntun</span><span class="sxs-lookup"><span data-stu-id="1c227-261">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="1c227-262">Innkaup</span><span class="sxs-lookup"><span data-stu-id="1c227-262">Purchasing</span></span>

<span data-ttu-id="1c227-263">Í innkaupum, ef þú stillir reitinn **Gerð tilviks** á **Innhreyfingarskjal afurðar** og reitinn **Framkvæmd** á **Eftir** á síðunni **Gæðatengingar** færðu eftirfarandi niðurstöður:</span><span class="sxs-lookup"><span data-stu-id="1c227-263">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="1c227-264">Ef valkosturinn **Eftir uppfærðu magni** er stilltur á **Já** myndast gæðapöntun fyrir hverja innhreyfingu gegn innkaupapöntuninni, byggð á mótteknu magni og stillingum í vörusýni.</span><span class="sxs-lookup"><span data-stu-id="1c227-264">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="1c227-265">Í hvert skipti sem magn er móttekið gegn innkaupapöntuninni myndast nýjar gæðapantanir miðað við nýlega fengið magn.</span><span class="sxs-lookup"><span data-stu-id="1c227-265">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="1c227-266">Ef valkosturinn **Eftir uppfærðu magni** er stilltur á **Nei** myndast gæðapöntun fyrir fyrstu innhreyfinguna gegn innkaupapöntuninni, byggð á mótteknu magni.</span><span class="sxs-lookup"><span data-stu-id="1c227-266">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="1c227-267">Að auki eru ein eða fleiri gæðapantanir búnar til miðað við eftirstandandi magn, eftir því hverjar rakningarvíddirnar eru.</span><span class="sxs-lookup"><span data-stu-id="1c227-267">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="1c227-268">Gæðapantanir eru ekki myndaðar fyrir síðari innhreyfingar gegn innkaupapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="1c227-268">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="1c227-269">Gæðaforskriftir</span><span class="sxs-lookup"><span data-stu-id="1c227-269">Quality specification</span></span></th>
<th><span data-ttu-id="1c227-270">Uppfært magn á</span><span class="sxs-lookup"><span data-stu-id="1c227-270">Per updated quantity</span></span></th>
<th><span data-ttu-id="1c227-271">Á rakningarvídd</span><span class="sxs-lookup"><span data-stu-id="1c227-271">Per tracking dimension</span></span></th>
<th><span data-ttu-id="1c227-272">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="1c227-272">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="1c227-273">Prósenta: 10%</span><span class="sxs-lookup"><span data-stu-id="1c227-273">Percentage: 10%</span></span></td>
<td><span data-ttu-id="1c227-274">Já</span><span class="sxs-lookup"><span data-stu-id="1c227-274">Yes</span></span></td>
<td>
<p><span data-ttu-id="1c227-275">Rununúmer: Nr.</span><span class="sxs-lookup"><span data-stu-id="1c227-275">Batch number: No</span></span></p>
<p><span data-ttu-id="1c227-276">Raðnúmer: Nr.</span><span class="sxs-lookup"><span data-stu-id="1c227-276">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="1c227-277">Pöntunarmagn: 100</span><span class="sxs-lookup"><span data-stu-id="1c227-277">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="1c227-278">Tilkynna sem lokið fyrir 30</span><span class="sxs-lookup"><span data-stu-id="1c227-278">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="1c227-279">Gæðapöntun #1 fyrir 3 (10% af 30)</span><span class="sxs-lookup"><span data-stu-id="1c227-279">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1c227-280">Tilkynna sem lokið fyrir 70</span><span class="sxs-lookup"><span data-stu-id="1c227-280">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="1c227-281">Gæðapöntun # 2 fyrir 7 (10% af pöntunarmagni sem eftir er, sem jafngildir 70 í þessu tilfelli)</span><span class="sxs-lookup"><span data-stu-id="1c227-281">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="1c227-282">Fast magn: 1</span><span class="sxs-lookup"><span data-stu-id="1c227-282">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="1c227-283">Nr</span><span class="sxs-lookup"><span data-stu-id="1c227-283">No</span></span></td>
<td>
<p><span data-ttu-id="1c227-284">Rununúmer: Nr.</span><span class="sxs-lookup"><span data-stu-id="1c227-284">Batch number: No</span></span></p>
<p><span data-ttu-id="1c227-285">Raðnúmer: Nr.</span><span class="sxs-lookup"><span data-stu-id="1c227-285">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="1c227-286">Pöntunarmagn: 100</span><span class="sxs-lookup"><span data-stu-id="1c227-286">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="1c227-287">Tilkynna sem lokið fyrir 30</span><span class="sxs-lookup"><span data-stu-id="1c227-287">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="1c227-288">Gæðapöntun #1 er búin til fyrir 1 (fyrir fyrsta magn sem var tilkynnt sem lokið, sem hefur fast gildi 1).</span><span class="sxs-lookup"><span data-stu-id="1c227-288">Quality order #1 is created for 1 (for the first reported-as-finished quantity, which has a fixed value of 1).</span></span></li>
<li><span data-ttu-id="1c227-289">Fleiri gæðapantanir eru ekki myndaðar á móti eftirstandandi magni.</span><span class="sxs-lookup"><span data-stu-id="1c227-289">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1c227-290">Tilkynna sem lokið fyrir 10</span><span class="sxs-lookup"><span data-stu-id="1c227-290">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="1c227-291">Engar gæðapantanir eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="1c227-291">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1c227-292">Tilkynna sem lokið fyrir 60</span><span class="sxs-lookup"><span data-stu-id="1c227-292">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="1c227-293">Engar gæðapantanir eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="1c227-293">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="1c227-294">Fast magn: 1</span><span class="sxs-lookup"><span data-stu-id="1c227-294">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="1c227-295">Já</span><span class="sxs-lookup"><span data-stu-id="1c227-295">Yes</span></span></td>
<td>
<p><span data-ttu-id="1c227-296">Rununúmer: Já</span><span class="sxs-lookup"><span data-stu-id="1c227-296">Batch number: Yes</span></span></p>
<p><span data-ttu-id="1c227-297">Raðnúmer: Já</span><span class="sxs-lookup"><span data-stu-id="1c227-297">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="1c227-298">Pöntunarmagn: 10</span><span class="sxs-lookup"><span data-stu-id="1c227-298">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="1c227-299">Tilkynna sem lokið fyrir 3</span><span class="sxs-lookup"><span data-stu-id="1c227-299">Report as finished for 3</span></span>
<ul>
<li><span data-ttu-id="1c227-300">Gæðapöntun #1 fyrir 1 í lotu #b1, raðnúmer #s1</span><span class="sxs-lookup"><span data-stu-id="1c227-300">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="1c227-301">Gæðapöntun #2 fyrir 1 í lotu #b2, raðnúmer #s2</span><span class="sxs-lookup"><span data-stu-id="1c227-301">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="1c227-302">Gæðapöntun #3 fyrir 1 í lotu #b3, raðnúmer #s3</span><span class="sxs-lookup"><span data-stu-id="1c227-302">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1c227-303">Tilkynna sem lokið fyrir 2</span><span class="sxs-lookup"><span data-stu-id="1c227-303">Report as finished for 2</span></span>
<ul>
<li><span data-ttu-id="1c227-304">Gæðapöntun #4 fyrir 1 í lotu #b4, raðnúmer #s4</span><span class="sxs-lookup"><span data-stu-id="1c227-304">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="1c227-305">Gæðapöntun #5 fyrir 1 í lotu #b5, raðnúmer #s5</span><span class="sxs-lookup"><span data-stu-id="1c227-305">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="1c227-306"><strong>Ath.:</strong> Hægt er að endurnýta rununa.</span><span class="sxs-lookup"><span data-stu-id="1c227-306"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="1c227-307">Fast magn: 2</span><span class="sxs-lookup"><span data-stu-id="1c227-307">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="1c227-308">Nr</span><span class="sxs-lookup"><span data-stu-id="1c227-308">No</span></span></td>
<td>
<p><span data-ttu-id="1c227-309">Rununúmer: Já</span><span class="sxs-lookup"><span data-stu-id="1c227-309">Batch number: Yes</span></span></p>
<p><span data-ttu-id="1c227-310">Raðnúmer: Já</span><span class="sxs-lookup"><span data-stu-id="1c227-310">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="1c227-311">Pöntunarmagn: 10</span><span class="sxs-lookup"><span data-stu-id="1c227-311">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="1c227-312">Tilkynna sem lokið fyrir 4</span><span class="sxs-lookup"><span data-stu-id="1c227-312">Report as finished for 4</span></span>
<ul>
<li><span data-ttu-id="1c227-313">Gæðapöntun #1 fyrir 1 í lotu #b1, raðnúmer #s1.</span><span class="sxs-lookup"><span data-stu-id="1c227-313">Quality order #1 for 1 of batch #b1, serial #s1.</span></span></li>
<li><span data-ttu-id="1c227-314">Gæðapöntun #2 fyrir 1 í lotu #b2, raðnúmer #s2.</span><span class="sxs-lookup"><span data-stu-id="1c227-314">Quality order #2 for 1 of batch #b2, serial #s2.</span></span></li>
<li><span data-ttu-id="1c227-315">Gæðapöntun #3 fyrir 1 í lotu #b3, raðnúmer #s3.</span><span class="sxs-lookup"><span data-stu-id="1c227-315">Quality order #3 for 1 of batch #b3, serial #s3.</span></span></li>
<li><span data-ttu-id="1c227-316">Gæðapöntun #4 fyrir 1 í lotu #b4, raðnúmer #s4.</span><span class="sxs-lookup"><span data-stu-id="1c227-316">Quality order #4 for 1 of batch #b4, serial #s4.</span></span></li>
<li><span data-ttu-id="1c227-317">Fleiri gæðapantanir eru ekki myndaðar á móti eftirstandandi magni.</span><span class="sxs-lookup"><span data-stu-id="1c227-317">No more quality orders are created against the remaining quantity.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1c227-318">Tilkynna sem lokið fyrir 6</span><span class="sxs-lookup"><span data-stu-id="1c227-318">Report as finished for 6</span></span>
<ul>
<li><span data-ttu-id="1c227-319">Engar gæðapantanir eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="1c227-319">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="production"></a><span data-ttu-id="1c227-320">Framleiðsla</span><span class="sxs-lookup"><span data-stu-id="1c227-320">Production</span></span>

<span data-ttu-id="1c227-321">Í framleiðslu, ef þú stillir reitinn **Gerð tilviks** á **Tilkynna sem lokið** og reitinn **Framkvæmd** á **Eftir** á síðunni **Gæðatengingar** færðu eftirfarandi niðurstöður:</span><span class="sxs-lookup"><span data-stu-id="1c227-321">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="1c227-322">Ef valkosturinn **Eftir uppfærðu magni** er stilltur á **Já** myndast gæðapöntun fyrir hvert lokið magn og stillingar í vörusýni.</span><span class="sxs-lookup"><span data-stu-id="1c227-322">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="1c227-323">Í hvert skipti sem magn er tilkynnt sem lokið gegn framleiðslupöntuninni myndast nýjar gæðapantanir miðað við nýlega lokið magn.</span><span class="sxs-lookup"><span data-stu-id="1c227-323">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="1c227-324">Þessi myndunarrök eru í samræmi við innkaup.</span><span class="sxs-lookup"><span data-stu-id="1c227-324">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="1c227-325">Ef valkosturinn **Eftir uppfærðu magni** er stilltur á **Nei** myndast gæðapöntun fyrir fyrsta skiptið sem magn er tilkynnt sem lokið, byggt á loknu magni.</span><span class="sxs-lookup"><span data-stu-id="1c227-325">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="1c227-326">Að auki eru ein eða fleiri gæðapantanir búnar til miðað við eftirstandandi magn, eftir því hverjar rakningarvíddirnar eru í vörusýninu.</span><span class="sxs-lookup"><span data-stu-id="1c227-326">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="1c227-327">Gæðapantanir eru ekki búnar til fyrir seinna lokið magn.</span><span class="sxs-lookup"><span data-stu-id="1c227-327">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="1c227-328">Gæðaforskriftir</span><span class="sxs-lookup"><span data-stu-id="1c227-328">Quality specification</span></span></th>
<th><span data-ttu-id="1c227-329">Uppfært magn á</span><span class="sxs-lookup"><span data-stu-id="1c227-329">Per updated quantity</span></span></th>
<th><span data-ttu-id="1c227-330">Á rakningarvídd</span><span class="sxs-lookup"><span data-stu-id="1c227-330">Per tracking dimension</span></span></th>
<th><span data-ttu-id="1c227-331">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="1c227-331">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="1c227-332">Prósenta: 10%</span><span class="sxs-lookup"><span data-stu-id="1c227-332">Percentage: 10%</span></span></td>
<td><span data-ttu-id="1c227-333">Já</span><span class="sxs-lookup"><span data-stu-id="1c227-333">Yes</span></span></td>
<td>
<p><span data-ttu-id="1c227-334">Rununúmer: Nr.</span><span class="sxs-lookup"><span data-stu-id="1c227-334">Batch number: No</span></span></p>
<p><span data-ttu-id="1c227-335">Raðnúmer: Nr.</span><span class="sxs-lookup"><span data-stu-id="1c227-335">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="1c227-336">Pöntunarmagn: 100</span><span class="sxs-lookup"><span data-stu-id="1c227-336">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="1c227-337">Tilkynna sem lokið fyrir 30</span><span class="sxs-lookup"><span data-stu-id="1c227-337">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="1c227-338">Gæðapöntun #1 fyrir 3 (10% af 30)</span><span class="sxs-lookup"><span data-stu-id="1c227-338">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1c227-339">Tilkynna sem lokið fyrir 70</span><span class="sxs-lookup"><span data-stu-id="1c227-339">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="1c227-340">Gæðapöntun # 2 fyrir 7 (10% af pöntunarmagni sem eftir er, sem jafngildir 70 í þessu tilfelli)</span><span class="sxs-lookup"><span data-stu-id="1c227-340">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="1c227-341">Fast magn: 1</span><span class="sxs-lookup"><span data-stu-id="1c227-341">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="1c227-342">Nr</span><span class="sxs-lookup"><span data-stu-id="1c227-342">No</span></span></td>
<td>
<p><span data-ttu-id="1c227-343">Rununúmer: Nr.</span><span class="sxs-lookup"><span data-stu-id="1c227-343">Batch number: No</span></span></p>
<p><span data-ttu-id="1c227-344">Raðnúmer: Nr.</span><span class="sxs-lookup"><span data-stu-id="1c227-344">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="1c227-345">Pöntunarmagn: 100</span><span class="sxs-lookup"><span data-stu-id="1c227-345">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="1c227-346">Tilkynna sem lokið fyrir 30</span><span class="sxs-lookup"><span data-stu-id="1c227-346">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="1c227-347">Gæðapöntun #1 er stofnuð fyrir 1 (fyrir fyrsta magn sem var tilkynnt sem lokið, sem hefur fast gildi 1)</span><span class="sxs-lookup"><span data-stu-id="1c227-347">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="1c227-348">Gæðapöntun #2 er stofnuð fyrir 1 (fyrir eftirstandandi magn, sem er samt með fast gildi 1)</span><span class="sxs-lookup"><span data-stu-id="1c227-348">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1c227-349">Tilkynna sem lokið fyrir 10</span><span class="sxs-lookup"><span data-stu-id="1c227-349">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="1c227-350">Engar gæðapantanir eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="1c227-350">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1c227-351">Tilkynna sem lokið fyrir 60</span><span class="sxs-lookup"><span data-stu-id="1c227-351">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="1c227-352">Engar gæðapantanir eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="1c227-352">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="1c227-353">Fast magn: 1</span><span class="sxs-lookup"><span data-stu-id="1c227-353">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="1c227-354">Já</span><span class="sxs-lookup"><span data-stu-id="1c227-354">Yes</span></span></td>
<td>
<p><span data-ttu-id="1c227-355">Rununúmer: Já</span><span class="sxs-lookup"><span data-stu-id="1c227-355">Batch number: Yes</span></span></p>
<p><span data-ttu-id="1c227-356">Raðnúmer: Já</span><span class="sxs-lookup"><span data-stu-id="1c227-356">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="1c227-357">Pöntunarmagn: 10</span><span class="sxs-lookup"><span data-stu-id="1c227-357">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="1c227-358">Tilkynna sem lokið fyrir 3: 1 fyrir #b1, #s1; 1 fyrir #b2, #s2; og 1 fyrir #b3, #s3</span><span class="sxs-lookup"><span data-stu-id="1c227-358">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="1c227-359">Gæðapöntun #1 fyrir 1 í lotu #b1, raðnúmer #s1</span><span class="sxs-lookup"><span data-stu-id="1c227-359">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="1c227-360">Gæðapöntun #2 fyrir 1 í lotu #b2, raðnúmer #s2</span><span class="sxs-lookup"><span data-stu-id="1c227-360">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="1c227-361">Gæðapöntun #3 fyrir 1 í lotu #b3, raðnúmer #s3</span><span class="sxs-lookup"><span data-stu-id="1c227-361">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1c227-362">Tilkynna sem lokið fyrir 2: 1 fyrir #b4, #s4; og 1 fyrir #b5, #s5</span><span class="sxs-lookup"><span data-stu-id="1c227-362">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="1c227-363">Gæðapöntun #4 fyrir 1 í lotu #b4, raðnúmer #s4</span><span class="sxs-lookup"><span data-stu-id="1c227-363">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="1c227-364">Gæðapöntun #5 fyrir 1 í lotu #b5, raðnúmer #s5</span><span class="sxs-lookup"><span data-stu-id="1c227-364">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="1c227-365"><strong>Ath.:</strong> Hægt er að endurnýta rununa.</span><span class="sxs-lookup"><span data-stu-id="1c227-365"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="1c227-366">Fast magn: 2</span><span class="sxs-lookup"><span data-stu-id="1c227-366">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="1c227-367">Nr</span><span class="sxs-lookup"><span data-stu-id="1c227-367">No</span></span></td>
<td>
<p><span data-ttu-id="1c227-368">Rununúmer: Já</span><span class="sxs-lookup"><span data-stu-id="1c227-368">Batch number: Yes</span></span></p>
<p><span data-ttu-id="1c227-369">Raðnúmer: Já</span><span class="sxs-lookup"><span data-stu-id="1c227-369">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="1c227-370">Pöntunarmagn: 10</span><span class="sxs-lookup"><span data-stu-id="1c227-370">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="1c227-371">Tilkynna sem lokið fyrir 4: 1 fyrir #b1, #s1; 1 fyrir #b2, #s2; og 1 fyrir #b3, #s3; og 1 fyrir #b4, #s4</span><span class="sxs-lookup"><span data-stu-id="1c227-371">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="1c227-372">Gæðapöntun #1 fyrir 1 í lotu #b1, raðnúmer #s1</span><span class="sxs-lookup"><span data-stu-id="1c227-372">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="1c227-373">Gæðapöntun #2 fyrir 1 í lotu #b2, raðnúmer #s2</span><span class="sxs-lookup"><span data-stu-id="1c227-373">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="1c227-374">Gæðapöntun #3 fyrir 1 í lotu #b3, raðnúmer #s3</span><span class="sxs-lookup"><span data-stu-id="1c227-374">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="1c227-375">Gæðapöntun #4 fyrir 1 í lotu #b4, raðnúmer #s4</span><span class="sxs-lookup"><span data-stu-id="1c227-375">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="1c227-376">Gæðapöntun #5 fyrir 2, án tilvísunar í runu og raðnúmer</span><span class="sxs-lookup"><span data-stu-id="1c227-376">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="1c227-377">Tilkynna sem lokið fyrir 6: 1 fyrir #b5, #s5; 1 fyrir #b6, #s6; 1 fyrir #b7, #s7; 1 fyrir #b8, #s8; 1 fyrir #b9, #s9; og 1 fyrir #b10, #s10</span><span class="sxs-lookup"><span data-stu-id="1c227-377">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="1c227-378">Engar gæðapantanir eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="1c227-378">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="1c227-379">Gæðastjórnunarsíður</span><span class="sxs-lookup"><span data-stu-id="1c227-379">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1c227-380">Síða</span><span class="sxs-lookup"><span data-stu-id="1c227-380">Page</span></span></th>
<th><span data-ttu-id="1c227-381">Lýsing</span><span class="sxs-lookup"><span data-stu-id="1c227-381">Description</span></span></th>
<th><span data-ttu-id="1c227-382">Dæmi</span><span class="sxs-lookup"><span data-stu-id="1c227-382">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1c227-383">Gæðatengingar</span><span class="sxs-lookup"><span data-stu-id="1c227-383">Quality associations</span></span></td>
<td><span data-ttu-id="1c227-384">Sjá fyrri hluta í þessari grein.</span><span class="sxs-lookup"><span data-stu-id="1c227-384">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="1c227-385">Gæðatenging skilgreinir allar eftirfarandi upplýsingar fyrir gæðapöntun sem er mynduð:</span><span class="sxs-lookup"><span data-stu-id="1c227-385">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="1c227-386">Færslutilvikið</span><span class="sxs-lookup"><span data-stu-id="1c227-386">The transaction event</span></span></li>
<li><span data-ttu-id="1c227-387">Safn prófana sem þarf að framkvæma á vörum</span><span class="sxs-lookup"><span data-stu-id="1c227-387">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="1c227-388">Viðunandi gæðastig</span><span class="sxs-lookup"><span data-stu-id="1c227-388">The AQL</span></span></li>
<li><span data-ttu-id="1c227-389">Úrtaksáætlunin</span><span class="sxs-lookup"><span data-stu-id="1c227-389">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="1c227-390">Gæðatengingu verður að skilgreina fyrir hvert afbrigði viðskiptaferlis sem krefst sjálfvirkrar myndunar gæðapöntunar.</span><span class="sxs-lookup"><span data-stu-id="1c227-390">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="1c227-391">Til dæmis er hægt að mynda gæðapöntun í viðskiptaferlum fyrir innkaupapantanir, biðgeymslupantanir, sölupantanir eða framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="1c227-391">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c227-392">Prófanir</span><span class="sxs-lookup"><span data-stu-id="1c227-392">Tests</span></span></td>
<td><span data-ttu-id="1c227-393">Notið þessa skjámynd til að skilgreina og skoða einstök próf sem ákvarða hvort framleiðsluvara fyrirtækisins uppfylli gæðakröfur.</span><span class="sxs-lookup"><span data-stu-id="1c227-393">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="1c227-394">Hægt er að úthluta einu eða fleiri einstökum prófum á prófunarflokk.</span><span class="sxs-lookup"><span data-stu-id="1c227-394">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="1c227-395">Í þessu tilviki þarf einnig að tilgreina prófunarsértækar upplýsingar, eins og viðunandi mælingargildi.</span><span class="sxs-lookup"><span data-stu-id="1c227-395">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="1c227-396">Mælingargildi eru notuð fyrir magnbundnar prófanir og prófunarbreytur eru notaðar fyrir eðlisbundin próf.</span><span class="sxs-lookup"><span data-stu-id="1c227-396">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="1c227-397">Magnbundið próf hefur prófunargerð fyrir <strong>Heiltala</strong> eða <strong>Brot</strong> og er einnig með skilgreinda mælieiningu.</span><span class="sxs-lookup"><span data-stu-id="1c227-397">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="1c227-398">Gæðaskilyrði og prófunarniðurstöður sem eru sýnd sem tölur.</span><span class="sxs-lookup"><span data-stu-id="1c227-398">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="1c227-399">Eðlisbundið próf hefur prófunargerðina <strong>Valkostir</strong>.</span><span class="sxs-lookup"><span data-stu-id="1c227-399">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="1c227-400">Eigindlegar prófanir krefjast viðbótarupplýsingar um prófunarbreytuna sem verið er að mæla og tölusetta valkosti hennar.</span><span class="sxs-lookup"><span data-stu-id="1c227-400">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="1c227-401">Gæðaforskriftir og prófunarniðurstöður sem eru sýnd eftir útkomu.</span><span class="sxs-lookup"><span data-stu-id="1c227-401">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="1c227-402">Framleiðslufyrirtæki framkvæmir tvær prófanir á innkeypt efni: magnbundið prófun á gæðum efnis og eigindlega prófun á umbúðaskemmdum.</span><span class="sxs-lookup"><span data-stu-id="1c227-402">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="1c227-403">Fyrirtækið skilgreinir viðbótarupplýsingar um eðlisbundið próf til að auðkenna prófunarbreytu (skemmdar umbúðir) og niðurstöður hennar.</span><span class="sxs-lookup"><span data-stu-id="1c227-403">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="1c227-404">Fyrirtæki notar síðuna <strong>Prófunarflokkar</strong> til að úthluta tveimur prófunum á prófunarflokk og tilgreina prófunarsértækar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="1c227-404">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="1c227-405">Prófunarflokknum er úthlutað á gæðapöntun svo að fyrirtækið getur tilkynnt niðurstöður prófana fyrir bæði prófin.</span><span class="sxs-lookup"><span data-stu-id="1c227-405">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c227-406">Prófunarflokkar</span><span class="sxs-lookup"><span data-stu-id="1c227-406">Test groups</span></span></td>
<td><span data-ttu-id="1c227-407">Notaðu þessa síðu til að setja upp, breyta og skoða prófunarflokka og einstakar prófanir sem er úthlutað á prófunarflokk.</span><span class="sxs-lookup"><span data-stu-id="1c227-407">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="1c227-408">Efri rúðan birtir prófunarflokka og neðri rúðan birtir prófanir sem er úthlutað á valinn prófunarflokk.</span><span class="sxs-lookup"><span data-stu-id="1c227-408">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="1c227-409">Nokkrum reglum er úthlutað á prófunarflokk, eins og úrtaksáætlun, viðunandi gæðastigi og þörf fyrir eyðileggingarprófun.</span><span class="sxs-lookup"><span data-stu-id="1c227-409">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="1c227-410">Þegar þú úthlutar stöku prófi á prófunarflokk, skilgreinirðu viðbótarupplýsingar, eins og röðina, skjölin og gildisdagsetningarnar.</span><span class="sxs-lookup"><span data-stu-id="1c227-410">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="1c227-411">Fyrir magnbundna prófun innihalda upplýsingar sem eru skilgreindar einnig viðunandi mælingargildi.</span><span class="sxs-lookup"><span data-stu-id="1c227-411">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="1c227-412">Upplýsingarnar eru prófunarfæribreytur og sjálfgefin útkoma fyrir eigindlega prófun.</span><span class="sxs-lookup"><span data-stu-id="1c227-412">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="1c227-413">Prófunarflokkur sem er úthlutað á gæðapöntun skilgreinir sjálfgefið safn prófana sem verður að framkvæma á tiltekinni vöru.</span><span class="sxs-lookup"><span data-stu-id="1c227-413">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="1c227-414">Hins vegar er hægt að bæta við, breyta, eða eyða prófunum innan gæðapöntunar.</span><span class="sxs-lookup"><span data-stu-id="1c227-414">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="1c227-415">Niðurstöður prófana eru tilkynntar fyrir hvert próf á gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="1c227-415">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="1c227-416">Framleiðslufyrirtæki skilgreinir prófunarflokk fyrir hvert afbrigði af gæðareglum sínum.</span><span class="sxs-lookup"><span data-stu-id="1c227-416">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="1c227-417">Mismunandi prófunarflokkar endurspegla mismun á úrtaksáætlunum, safn prófana sem þarf að framkvæma samtímis, viðunandi gæðastigi og öðrum stuðlum.</span><span class="sxs-lookup"><span data-stu-id="1c227-417">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="1c227-418">Fyrir magnbundnar prófanir er einnig mismunur í viðunandi mælingargildum.</span><span class="sxs-lookup"><span data-stu-id="1c227-418">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="1c227-419">Til að framfylgja gæðareglum úthlutar fyrirtækið prófunarflokki á hverja reglu fyrir sjálfvirka myndun gæðapantana á síðunni <strong>Gæðatengingar</strong> og einnig prófunarflokki á gæðapantanir sem eru stofnaðar handvirkt.</span><span class="sxs-lookup"><span data-stu-id="1c227-419">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c227-420">Vörugæðaflokkar</span><span class="sxs-lookup"><span data-stu-id="1c227-420">Item quality groups</span></span></td>
<td><span data-ttu-id="1c227-421">Notaðu þessa síðu til að setja upp, breyta og skoða vörur sem er úthlutað á gæðaflokk eða gæðaflokka sem eru tengdir vöru.</span><span class="sxs-lookup"><span data-stu-id="1c227-421">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="1c227-422">Gæðaflokkur stendur fyrir sameiginlegar prófunarkröfur fyrir vörur.</span><span class="sxs-lookup"><span data-stu-id="1c227-422">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="1c227-423">Þegar búið er að skilgreina kröfur fyrir prófun á síðunni <strong>Prófunarflokkar</strong> er hægt að skilgreina reglur fyrir sjálfvirka myndun gæðapantana.</span><span class="sxs-lookup"><span data-stu-id="1c227-423">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="1c227-424">Til að einfalda ferlið eru ekki skilgreindar reglur fyrir stakar vörur.&#39;</span><span class="sxs-lookup"><span data-stu-id="1c227-424">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="1c227-425">Þess í stað eru skilgreindar reglur fyrir gæðaflokk, með því að nota síðuna <strong>Gæðatengingar</strong>.</span><span class="sxs-lookup"><span data-stu-id="1c227-425">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="1c227-426">Einnig er hægt að nota síðuna <strong>Vörur gæðaflokka</strong> fyrir valinn gæðaflokk til að úthluta viðeigandi vörum á þeim flokki.</span><span class="sxs-lookup"><span data-stu-id="1c227-426">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="1c227-427">Einnig er hægt að nota síðuna <strong>Vörur gæðaflokka</strong> fyrir valda vöru til að úthluta viðeigandi gæðaflokkum á vöruna.</span><span class="sxs-lookup"><span data-stu-id="1c227-427">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="1c227-428">Framleiðslufyrirtæki kaupir ýmislegt hráefni sem eru með sömu prófunarkröfur fyrir væntanlegt eftirlit.</span><span class="sxs-lookup"><span data-stu-id="1c227-428">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="1c227-429">Fyrirtækið skilgreinir gæðaflokk og úthlutar síðan vörunúmerum sem eru tengd hráefnum á þann flokk.</span><span class="sxs-lookup"><span data-stu-id="1c227-429">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="1c227-430">Síðar kaupir fyrirtækið nýja gerð hráefnis sem er með sömu prófunarkröfur.</span><span class="sxs-lookup"><span data-stu-id="1c227-430">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="1c227-431">Í stað þess að setja upp ný skilyrði um prófanir fyrir nýtt efni bætir við fyrirtækið vörunúmeri fyrir nýtt efni fyrirliggjandi gæðaflokk.</span><span class="sxs-lookup"><span data-stu-id="1c227-431">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="1c227-432">Sama framleiðslufyrirtæki framleiðir einnig vörur sem eru með sömu prófunarkröfur í framleiðslu og sendir vörur með sömu kröfur fyrir framkvæmd prófana fyrir sendingu.</span><span class="sxs-lookup"><span data-stu-id="1c227-432">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="1c227-433">Fyrirtækið skilgreinir tvo viðbótargæðaflokka og úthlutar síðan viðeigandi vörunúmerum í hvern gæðaflokk.</span><span class="sxs-lookup"><span data-stu-id="1c227-433">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1c227-434">Prófunarbreytur</span><span class="sxs-lookup"><span data-stu-id="1c227-434">Test variables</span></span></td>
<td><span data-ttu-id="1c227-435">Notaðu síðuna til þess að skilgreina og skoða breyturnar sem eru tengdar við eigindlega prófun.</span><span class="sxs-lookup"><span data-stu-id="1c227-435">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="1c227-436">Fyrir hverja færibreytu eru skilgreindar númeraðar niðurstöður sem sýna mögulega valkosti.</span><span class="sxs-lookup"><span data-stu-id="1c227-436">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="1c227-437">Skilgreina prófanir á <strong>Prófanir</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="1c227-437">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="1c227-438">Fyrir eðlisbundið próf verður að stilla prófunargerðina á <strong>Valkost</strong>.</span><span class="sxs-lookup"><span data-stu-id="1c227-438">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="1c227-439">Notaðu síðuna <strong>Prófunarflokkar</strong> til að úthluta breytu á prófun.</span><span class="sxs-lookup"><span data-stu-id="1c227-439">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="1c227-440">Framleiðslufyrirtæki sem framleiðir kexkökur notar skoðunarpróf sem nær til nokkurra gerða af hinni framleiddu vöru.</span><span class="sxs-lookup"><span data-stu-id="1c227-440">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="1c227-441">Þessi prófun hefur nokkur breytur.</span><span class="sxs-lookup"><span data-stu-id="1c227-441">This inspection test has several variables.</span></span> <span data-ttu-id="1c227-442">Ein færibreyta er bragð, með valkostunum gott eða vont.</span><span class="sxs-lookup"><span data-stu-id="1c227-442">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="1c227-443">Önnur færibreyta er litur, með mögulega niðurstöðu of dökkur, of ljós, og í lagi.</span><span class="sxs-lookup"><span data-stu-id="1c227-443">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1c227-444">Útkomur úr prófunarbreytum</span><span class="sxs-lookup"><span data-stu-id="1c227-444">Test variable outcomes</span></span></td>
<td><span data-ttu-id="1c227-445">Notið þessa síðu til að setja upp, breyta og skoða mögulegar niðurstöður prófana fyrir prófunarbreytu sem tengist gæðaprófi.</span><span class="sxs-lookup"><span data-stu-id="1c227-445">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="1c227-446">Hægt er að gefa hverri niðurstöðu einkunnina <strong>staðist</strong> eða <strong>fallið</strong>.</span><span class="sxs-lookup"><span data-stu-id="1c227-446">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="1c227-447">Skilgreina verður breytuna og niðurstöður hennar fyrir hverja eigindlega prófun sem er skilgreind á síðunni <strong>Prófanir</strong>.</span><span class="sxs-lookup"><span data-stu-id="1c227-447">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="1c227-448">(Fyrir gæðaprófanir er prófunargerðin stillt á <strong>Valkostur</strong> á síðunni <strong>Prófanir</strong>.) Notaðu síðuna <strong>Prófunarflokkar</strong> til að úthluta prófunarbreytu og sjálfgefinni niðurstöðu á staka gæðaprófun.</span><span class="sxs-lookup"><span data-stu-id="1c227-448">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="1c227-449">Framleiðslufyrirtæki sem framleiðir kexkökur notar skoðunarpróf sem nær til nokkurra gerða af hinni framleiddu vöru.</span><span class="sxs-lookup"><span data-stu-id="1c227-449">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="1c227-450">Þessi eftirlitsprófun hefur nokkur breytur.</span><span class="sxs-lookup"><span data-stu-id="1c227-450">This inspection test has of several variables.</span></span> <span data-ttu-id="1c227-451">Ein færibreyta er bragð, með valkostum gott eða vont.</span><span class="sxs-lookup"><span data-stu-id="1c227-451">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="1c227-452">Önnur færibreyta er litur, með mögulega niðurstöðu of dökkur, of ljós, og í lagi.</span><span class="sxs-lookup"><span data-stu-id="1c227-452">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="1c227-453">Hver einasta niðurstaða hefur stöðuna <strong>staðist</strong> eða <strong>fallið</strong>.</span><span class="sxs-lookup"><span data-stu-id="1c227-453">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="1c227-454">Á meðan á gæðaprófi stendur fyrir hverja færibreytu, skráir prófunaraðili niðurstöður prófsins með því að velja eina af mögulegu niðurstöðunum.</span><span class="sxs-lookup"><span data-stu-id="1c227-454">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="1c227-455">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="1c227-455">Additional resources</span></span>
--------

[<span data-ttu-id="1c227-456">Gæðastjórnunarferli</span><span class="sxs-lookup"><span data-stu-id="1c227-456">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="1c227-457">Stjórnun ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="1c227-457">Nonconformance management</span></span>](enable-nonconformance-management.md)
