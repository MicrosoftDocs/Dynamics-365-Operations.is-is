---
title: "Yfirlit yfir gæðastjórnun"
description: "Þessi grein lýsir því hvernig hægt er að nota gæðastjórnun í Microsoft Dynamics 365 for Finance and Operations til að bæta gæði afurða innan aðfangakeðju þinnar."
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 28ef47e2dc1f9c7e1c0b262c58332dcfea1f7495
ms.contentlocale: is-is
ms.lasthandoff: 09/12/2017

---

# <a name="quality-management-overview"></a><span data-ttu-id="4a998-103">Yfirlit yfir gæðastjórnun</span><span class="sxs-lookup"><span data-stu-id="4a998-103">Quality management overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4a998-104">Þessi grein lýsir því hvernig hægt er að nota gæðastjórnun í Microsoft Dynamics 365 for Finance and Operations til að bæta gæði afurða innan aðfangakeðju þinnar.</span><span class="sxs-lookup"><span data-stu-id="4a998-104">This article describes how you can use quality management in Microsoft Dynamics 365 for Finance and Operations to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="4a998-105">Gæðastjórnun getur hjálpað við að stjórna biðtíma þegar ósamkvæmar afurðir eru meðhöndlaðar, óháð uppruna þeirra.</span><span class="sxs-lookup"><span data-stu-id="4a998-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="4a998-106">Þar sem greiningargerðir eru tengdar leiðréttingaskýrslum getur Microsoft Dynamics 365 for Finance and Operations raðað verk til að leiðrétta vandamál og komið í veg fyrir þau verði endurtekin.</span><span class="sxs-lookup"><span data-stu-id="4a998-106">Because diagnostic types are linked to correction reporting, Microsoft Dynamics 365 for Finance and Operations can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="4a998-107">Auk virkni fyrir stjórnun ósamkvæmni inniheldur gæðastjórnun virkni til að rekja úthreyfingar eftir gerð vanda (jafnvel innri vandamál) og til að auðkenna lausnir sem skammtíma- eða langtímalausnir.</span><span class="sxs-lookup"><span data-stu-id="4a998-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="4a998-108">Upplýsingar um afkastavísi (KPI) veita innsýn í sögulegan feril fyrri vandamála með ósamkvæmi og þeirra lausna sem voru notuð til að leiðrétta þau.</span><span class="sxs-lookup"><span data-stu-id="4a998-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="4a998-109">Hægt er að nota söguleg gögn til að fara yfir skilvirkni fyrri gæðaráðstafana og ákvarða viðeigandi mælieiningar sem nota á í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="4a998-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="4a998-110">Þegar gæðatenging er sett upp getur Finance and Operations myndað gæðapantanir fyrir ýmis viðskiptaferli, tilvik og skilyrði.</span><span class="sxs-lookup"><span data-stu-id="4a998-110">When you set up a quality association, Finance and Operations can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="4a998-111">Gæðatengingin getur náð yfir ákveðna vöru, einstökan vöruflokk eða allar vörur.</span><span class="sxs-lookup"><span data-stu-id="4a998-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="4a998-112">Dæmi um notkun á gæðastjórnun</span><span class="sxs-lookup"><span data-stu-id="4a998-112">Examples of the use of quality management</span></span>
<span data-ttu-id="4a998-113">Gæðastjórnun er sveigjanleg og hægt er að innleiða hana á mismunandi vegu til að uppfylla kröfur um tiltekið stig í aðgerðum framboðskeðju.</span><span class="sxs-lookup"><span data-stu-id="4a998-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="4a998-114">Eftirfarandi dæmi sýna hugsanlega notkun á þessum eiginleikum:</span><span class="sxs-lookup"><span data-stu-id="4a998-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="4a998-115">Hefja ferli gæðaeftirlits sjálfvirkt, byggt á fyrirfram skilgreindum skilyrðum (við vöruhússkráningu innkaupapöntunar frá tilteknum lánardrottni).</span><span class="sxs-lookup"><span data-stu-id="4a998-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="4a998-116">Læsa birgðum við skoðun til að koma í veg fyrir að ósamþykktar birgðir séu notaðar (alger stöðvun á pöntunarmagni innkaup).</span><span class="sxs-lookup"><span data-stu-id="4a998-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="4a998-117">Vörusýnishorn eru notuð sem hluti af gæðatengingu til að skilgreina magn gildandi efnislegra birgða sem verður að skoða.</span><span class="sxs-lookup"><span data-stu-id="4a998-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="4a998-118">Sýnishorn geta verið byggð á föstu magni eða hlutfalli.</span><span class="sxs-lookup"><span data-stu-id="4a998-118">Sampling can be based on fixed quantities or a percentage.</span></span>
-   <span data-ttu-id="4a998-119">Stofna gæðapantanir fyrir hluta móttöku.</span><span class="sxs-lookup"><span data-stu-id="4a998-119">Create quality orders for partial receipts.</span></span> <span data-ttu-id="4a998-120">Til að stofna gæðapöntun sem byggir á magni sem tekið er við efnislega með pöntun verður að velja gátreitinn **Eftir uppfærðu magni** á skjámyndinni **Vörusýnishorn**.</span><span class="sxs-lookup"><span data-stu-id="4a998-120">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="4a998-121">Stofna prófunargerðir sem innihalda lágmark, hámark og markprófunargildi og framkvæma eigindlega-samanborið við-eigindlega prófun sem hefur fyrirfram skilgreindar niðurstöður villuleitar.</span><span class="sxs-lookup"><span data-stu-id="4a998-121">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="4a998-122">Tilgreina viðunandi gæðastig (AQL) til að stjórna vikmörkum gæðaráðstafana.</span><span class="sxs-lookup"><span data-stu-id="4a998-122">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="4a998-123">Tilgreina tilföng sem skoðunaraðgerð krefst, eins og prófunarsvæði og prófunartæki.</span><span class="sxs-lookup"><span data-stu-id="4a998-123">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="4a998-124">Vinna með gæðatengingar</span><span class="sxs-lookup"><span data-stu-id="4a998-124">Working with quality associations</span></span>
<span data-ttu-id="4a998-125">Viðskiptaferli sem notar gæðatengingu getur verið tengt mismunandi upprunaskjölum, eins og innkaupapöntunum, sölupöntunum eða framleiðslupöntunum.</span><span class="sxs-lookup"><span data-stu-id="4a998-125">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="4a998-126">Hver gæðatengingafærsla skilgreinir einnig prófanir, viðunandi gæðastig og úrtaksáætlun sem eiga við myndaðar gæðapantanir.</span><span class="sxs-lookup"><span data-stu-id="4a998-126">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="4a998-127">Skilgreina verður gæðatengingafærslu fyrir hvert afbrigði viðskiptaferlis.</span><span class="sxs-lookup"><span data-stu-id="4a998-127">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="4a998-128">Til dæmis er hægt að setja upp gæðatengingu sem myndar gæðapöntun þegar innhreyfingarskjal afurða innkaupapöntun er uppfært.</span><span class="sxs-lookup"><span data-stu-id="4a998-128">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="4a998-129">Það fer eftir uppsetningu á keyrsluáætlun hvort hægt sé að stöðva kveikjuferlið sjálft á meðan gæðapöntun er opin eða hvort hægt sé að stöðva næstu ferli, eins og reikningsfærslu á innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="4a998-129">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="4a998-130">**Ábending:** Meðan gæðapantanir eru opnar er birgðamagn sjálfkrafa stöðvað til útgáfu.</span><span class="sxs-lookup"><span data-stu-id="4a998-130">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="4a998-131">Það fer eftir **Alger stöðvun** stillingunni á síðunni **Vörusýnishorn** hvort magn sé annaðhvort magn í gæðapöntun eða magn í upprunaskjalslínu.</span><span class="sxs-lookup"><span data-stu-id="4a998-131">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="4a998-132">Fyrir tiltekið viðskiptaferli auðkennir gæðatengingarfærslan tilvik og skilyrði sem mynda skal gæðapöntun fyrir.</span><span class="sxs-lookup"><span data-stu-id="4a998-132">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="4a998-133">Skilyrðin geta átt sérstaklega við svæði eða lögaðila.</span><span class="sxs-lookup"><span data-stu-id="4a998-133">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="4a998-134">Aðeins er hægt að mynda gæðapöntun sem felur í sér eyðileggingarprófun þegar lagerbirgðir eru til staðar fyrir tilvikið.</span><span class="sxs-lookup"><span data-stu-id="4a998-134">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="4a998-135">Eftirfarandi dæmi sýna hvernig gæðatengingafærsla er skilgreind fyrir afbrigði hvers viðskiptaferlis.</span><span class="sxs-lookup"><span data-stu-id="4a998-135">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="4a998-136">Í eftirfarandi töflu eru dæmin tekin saman eftir tilviki og skilyrðum sem skilgreind eru af gæðatengingarfærslu.</span><span class="sxs-lookup"><span data-stu-id="4a998-136">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="4a998-137">Gerð tilvísunar</span><span class="sxs-lookup"><span data-stu-id="4a998-137">Reference type</span></span></th>
<th><span data-ttu-id="4a998-138">Gerð tilviks</span><span class="sxs-lookup"><span data-stu-id="4a998-138">Event type</span></span></th>
<th><span data-ttu-id="4a998-139">Framkvæmd</span><span class="sxs-lookup"><span data-stu-id="4a998-139">Execution</span></span></th>
<th><span data-ttu-id="4a998-140">Lokun tilviks</span><span class="sxs-lookup"><span data-stu-id="4a998-140">Event blocking</span></span></th>
<th><span data-ttu-id="4a998-141">Tilvísun skjals</span><span class="sxs-lookup"><span data-stu-id="4a998-141">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="4a998-142">Birgðir</span><span class="sxs-lookup"><span data-stu-id="4a998-142">Inventory</span></span></td>
<td><span data-ttu-id="4a998-143">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="4a998-143">Not applicable</span></span></td>
<td><span data-ttu-id="4a998-144">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="4a998-144">Not applicable</span></span></td>
<td><span data-ttu-id="4a998-145">Ekkert</span><span class="sxs-lookup"><span data-stu-id="4a998-145">None</span></span></td>
<td><span data-ttu-id="4a998-146">Allt</span><span class="sxs-lookup"><span data-stu-id="4a998-146">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="4a998-147">Sala</span><span class="sxs-lookup"><span data-stu-id="4a998-147">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="4a998-148">Tiltektarferli er áætlað</span><span class="sxs-lookup"><span data-stu-id="4a998-148">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="4a998-149">Fyrir</span><span class="sxs-lookup"><span data-stu-id="4a998-149">Before</span></span></td>
<td><span data-ttu-id="4a998-150">Ekkert</span><span class="sxs-lookup"><span data-stu-id="4a998-150">None</span></span></td>
<td rowspan="22"><span data-ttu-id="4a998-151">Tilgreint kenni, Flokkur eða Allir aðeins</span><span class="sxs-lookup"><span data-stu-id="4a998-151">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-152">Tiltektarferli</span><span class="sxs-lookup"><span data-stu-id="4a998-152">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-153">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="4a998-153">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-154">Reikningur</span><span class="sxs-lookup"><span data-stu-id="4a998-154">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4a998-155">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="4a998-155">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="4a998-156">Fyrir</span><span class="sxs-lookup"><span data-stu-id="4a998-156">Before</span></span></td>
<td><span data-ttu-id="4a998-157">Ekkert</span><span class="sxs-lookup"><span data-stu-id="4a998-157">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-158">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="4a998-158">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-159">Reikningur</span><span class="sxs-lookup"><span data-stu-id="4a998-159">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="4a998-160">Innkaup</span><span class="sxs-lookup"><span data-stu-id="4a998-160">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="4a998-161">Innhreyfingaskjal</span><span class="sxs-lookup"><span data-stu-id="4a998-161">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="4a998-162">Fyrir</span><span class="sxs-lookup"><span data-stu-id="4a998-162">Before</span></span></td>
<td><span data-ttu-id="4a998-163">Ekkert</span><span class="sxs-lookup"><span data-stu-id="4a998-163">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-164">Innhreyfingaskjal</span><span class="sxs-lookup"><span data-stu-id="4a998-164">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-165">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="4a998-165">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-166">Reikningur</span><span class="sxs-lookup"><span data-stu-id="4a998-166">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4a998-167">Eftir</span><span class="sxs-lookup"><span data-stu-id="4a998-167">After</span></span></td>
<td><span data-ttu-id="4a998-168">Ekkert</span><span class="sxs-lookup"><span data-stu-id="4a998-168">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-169">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="4a998-169">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-170">Reikningur</span><span class="sxs-lookup"><span data-stu-id="4a998-170">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4a998-171">Skráning</span><span class="sxs-lookup"><span data-stu-id="4a998-171">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="4a998-172">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="4a998-172">Not applicable</span></span></td>
<td><span data-ttu-id="4a998-173">Ekkert</span><span class="sxs-lookup"><span data-stu-id="4a998-173">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-174">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="4a998-174">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-175">Reikningur</span><span class="sxs-lookup"><span data-stu-id="4a998-175">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="4a998-176">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="4a998-176">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="4a998-177">Fyrir</span><span class="sxs-lookup"><span data-stu-id="4a998-177">Before</span></span></td>
<td><span data-ttu-id="4a998-178">Ekkert</span><span class="sxs-lookup"><span data-stu-id="4a998-178">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-179">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="4a998-179">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-180">Reikningur</span><span class="sxs-lookup"><span data-stu-id="4a998-180">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4a998-181">Eftir</span><span class="sxs-lookup"><span data-stu-id="4a998-181">After</span></span></td>
<td><span data-ttu-id="4a998-182">Ekkert</span><span class="sxs-lookup"><span data-stu-id="4a998-182">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-183">Reikningur</span><span class="sxs-lookup"><span data-stu-id="4a998-183">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="4a998-184">Framleiðsla</span><span class="sxs-lookup"><span data-stu-id="4a998-184">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="4a998-185">Skráning</span><span class="sxs-lookup"><span data-stu-id="4a998-185">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="4a998-186">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="4a998-186">Not applicable</span></span></td>
<td><span data-ttu-id="4a998-187">Ekkert</span><span class="sxs-lookup"><span data-stu-id="4a998-187">None</span></span></td>
<td rowspan="12"><span data-ttu-id="4a998-188">Allt</span><span class="sxs-lookup"><span data-stu-id="4a998-188">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-189">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="4a998-189">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-190">Við skil</span><span class="sxs-lookup"><span data-stu-id="4a998-190">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="4a998-191">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="4a998-191">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="4a998-192">Fyrir</span><span class="sxs-lookup"><span data-stu-id="4a998-192">Before</span></span></td>
<td><span data-ttu-id="4a998-193">Ekkert</span><span class="sxs-lookup"><span data-stu-id="4a998-193">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-194">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="4a998-194">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-195">Við skil</span><span class="sxs-lookup"><span data-stu-id="4a998-195">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4a998-196">Eftir</span><span class="sxs-lookup"><span data-stu-id="4a998-196">After</span></span></td>
<td><span data-ttu-id="4a998-197">Ekkert</span><span class="sxs-lookup"><span data-stu-id="4a998-197">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-198">Við skil</span><span class="sxs-lookup"><span data-stu-id="4a998-198">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="4a998-199">Biðgeymsla</span><span class="sxs-lookup"><span data-stu-id="4a998-199">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="4a998-200">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="4a998-200">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="4a998-201">Fyrir</span><span class="sxs-lookup"><span data-stu-id="4a998-201">Before</span></span></td>
<td><span data-ttu-id="4a998-202">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="4a998-202">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-203">Við skil</span><span class="sxs-lookup"><span data-stu-id="4a998-203">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-204">Eftir</span><span class="sxs-lookup"><span data-stu-id="4a998-204">After</span></span></td>
<td><span data-ttu-id="4a998-205">Við skil</span><span class="sxs-lookup"><span data-stu-id="4a998-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-206">Við skil</span><span class="sxs-lookup"><span data-stu-id="4a998-206">End</span></span></td>
<td><span data-ttu-id="4a998-207">Fyrir</span><span class="sxs-lookup"><span data-stu-id="4a998-207">Before</span></span></td>
<td><span data-ttu-id="4a998-208">Við skil</span><span class="sxs-lookup"><span data-stu-id="4a998-208">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4a998-209">Leiðaraðgerð</span><span class="sxs-lookup"><span data-stu-id="4a998-209">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="4a998-210">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="4a998-210">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="4a998-211">Fyrir</span><span class="sxs-lookup"><span data-stu-id="4a998-211">Before</span></span></td>
<td><span data-ttu-id="4a998-212">Ekkert</span><span class="sxs-lookup"><span data-stu-id="4a998-212">None</span></span></td>
<td rowspan="3"><span data-ttu-id="4a998-213">Tilgreitn kenni, Flokkur eða Allt, og Tilfangasértækt, Flokkur eða Allt</span><span class="sxs-lookup"><span data-stu-id="4a998-213">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-214">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="4a998-214">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-215">Eftir</span><span class="sxs-lookup"><span data-stu-id="4a998-215">After</span></span></td>
<td><span data-ttu-id="4a998-216">Ekkert</span><span class="sxs-lookup"><span data-stu-id="4a998-216">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="4a998-217">Framleiðsla aukaafurðar</span><span class="sxs-lookup"><span data-stu-id="4a998-217">Co-product production</span></span></td>
<td><span data-ttu-id="4a998-218">Skráning</span><span class="sxs-lookup"><span data-stu-id="4a998-218">Registration</span></span></td>
<td><span data-ttu-id="4a998-219">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="4a998-219">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="4a998-220">Ekkert</span><span class="sxs-lookup"><span data-stu-id="4a998-220">None</span></span></td>
<td rowspan="3"><span data-ttu-id="4a998-221">Allt</span><span class="sxs-lookup"><span data-stu-id="4a998-221">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="4a998-222">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="4a998-222">Report as finished</span></span></td>
<td><span data-ttu-id="4a998-223">Fyrir</span><span class="sxs-lookup"><span data-stu-id="4a998-223">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-224">Eftir</span><span class="sxs-lookup"><span data-stu-id="4a998-224">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="4a998-225">Eftirfarandi tafla veitir frekari upplýsingar um hvernig hægt er að mynda gæðapantanir fyrir tilgreindar gerðir ferla.</span><span class="sxs-lookup"><span data-stu-id="4a998-225">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="4a998-226">Gerð ferlis</span><span class="sxs-lookup"><span data-stu-id="4a998-226">Type of process</span></span></th>
<th><span data-ttu-id="4a998-227">Þegar hægt er að mynda gæðapantanir sjálfvirkt</span><span class="sxs-lookup"><span data-stu-id="4a998-227">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="4a998-228">Þegar hægt er að mynda gæðapantanir ef eyðileggingarprófun er áskilin</span><span class="sxs-lookup"><span data-stu-id="4a998-228">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="4a998-229">Upplýsingar um skilyrði</span><span class="sxs-lookup"><span data-stu-id="4a998-229">Condition information</span></span></th>
<th><span data-ttu-id="4a998-230">Upplýsingar um handvirka myndun</span><span class="sxs-lookup"><span data-stu-id="4a998-230">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="4a998-231">Innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="4a998-231">Purchase order</span></span></td>
<td><span data-ttu-id="4a998-232">Á undan eða eftir komulista eða innhreyfingarskjal afurða fyrir efni sem er móttekið er bókuð</span><span class="sxs-lookup"><span data-stu-id="4a998-232">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="4a998-233">Eftir innhreyfingarskjal afurða fyrir efni sem er móttekið er bókað, þar sem efnið verður að vera tiltækt fyrir eyðileggingarprófun</span><span class="sxs-lookup"><span data-stu-id="4a998-233">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="4a998-234">Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða lánardrottins eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="4a998-234">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="4a998-235">Gæðapöntun sem er stofnuð handvirkt og vísar í innkaupapöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="4a998-235">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-236">Biðgeymslupöntun</span><span class="sxs-lookup"><span data-stu-id="4a998-236">Quarantine order</span></span></td>
<td><span data-ttu-id="4a998-237">Á undan eða eftir biðgeymslupöntunin er skráð sem lokið eða lokið</span><span class="sxs-lookup"><span data-stu-id="4a998-237">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="4a998-238">Ekki er hægt að mynda gæðapantanir sem krefjast eyðileggingarprófana.</span><span class="sxs-lookup"><span data-stu-id="4a998-238">Quality orders that require destructive tests can't be generated.</span></span> <span data-ttu-id="4a998-239">Gert er ráð fyrir að virkni biðgeymslupöntunar annist ráðstöfun á efni sem er eyðilagt.</span><span class="sxs-lookup"><span data-stu-id="4a998-239">It's assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="4a998-240">Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða lánardrottins eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="4a998-240">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="4a998-241">Gæðapöntun sem er stofnuð handvirkt og vísar í biðgeymslupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="4a998-241">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-242">Sölupöntun</span><span class="sxs-lookup"><span data-stu-id="4a998-242">Sales order</span></span></td>
<td><span data-ttu-id="4a998-243">Á undan á áætluðu tiltektarferli eða fylgiseðilsuppfærslu fyrir vörur sem verið er að senda</span><span class="sxs-lookup"><span data-stu-id="4a998-243">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="4a998-244">Á hvaða þrepi sem er</span><span class="sxs-lookup"><span data-stu-id="4a998-244">At any step</span></span></td>
<td><span data-ttu-id="4a998-245">Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða viðskiptavinar eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="4a998-245">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="4a998-246">Gæðapöntun sem er stofnuð handvirkt og vísar í sölupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="4a998-246">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-247">Framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="4a998-247">Production order</span></span></td>
<td><span data-ttu-id="4a998-248">Á undan eða eftir að tilbúið magn fyrir framleiðslupöntun er skráð</span><span class="sxs-lookup"><span data-stu-id="4a998-248">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="4a998-249">Eftir að tilbúið magn fyrir framleiðslupöntun er skráð</span><span class="sxs-lookup"><span data-stu-id="4a998-249">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="4a998-250">Þörf á gæðapöntun getur verið vegna tiltekins svæðis eða vöru eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="4a998-250">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="4a998-251">Gæðapöntun sem er stofnuð handvirkt og vísar í framleiðslupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="4a998-251">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-252">Framleiðslupöntun sem er með leiðaraðgerð</span><span class="sxs-lookup"><span data-stu-id="4a998-252">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="4a998-253">Á undan eða eftir að skýrslu er lokið fyrir aðgerð</span><span class="sxs-lookup"><span data-stu-id="4a998-253">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="4a998-254">Á undan eða eftir að skýrsluframleiðslu er lokið fyrir síðustu aðgerð</span><span class="sxs-lookup"><span data-stu-id="4a998-254">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="4a998-255">Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða rekstrartilfanga eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="4a998-255">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="4a998-256">Gæðapöntun sem er stofnuð handvirkt og vísar í leiðaraðgerð getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="4a998-256">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="4a998-257">Birgðir</span><span class="sxs-lookup"><span data-stu-id="4a998-257">Inventory</span></span></td>
<td><span data-ttu-id="4a998-258">Ekki er hægt að mynda gæðapöntun sjálfkrafa fyrir færslu í birgðabók eða fyrir flutningspantanafærslur.</span><span class="sxs-lookup"><span data-stu-id="4a998-258">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="4a998-259">Gæðapöntun verður að vera stofnuð handvirkt fyrir birgðamagn vöru.</span><span class="sxs-lookup"><span data-stu-id="4a998-259">A quality order must be created manually for an item's inventory quantity.</span></span> <span data-ttu-id="4a998-260">Efnislegra lagerbirgða er krafist.</span><span class="sxs-lookup"><span data-stu-id="4a998-260">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-management-pages"></a><span data-ttu-id="4a998-261">Gæðastjórnunarsíður</span><span class="sxs-lookup"><span data-stu-id="4a998-261">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4a998-262">Síða</span><span class="sxs-lookup"><span data-stu-id="4a998-262">Page</span></span></th>
<th><span data-ttu-id="4a998-263">Lýsing</span><span class="sxs-lookup"><span data-stu-id="4a998-263">Description</span></span></th>
<th><span data-ttu-id="4a998-264">Dæmi</span><span class="sxs-lookup"><span data-stu-id="4a998-264">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4a998-265">Gæðatengingar</span><span class="sxs-lookup"><span data-stu-id="4a998-265">Quality associations</span></span></td>
<td><span data-ttu-id="4a998-266">Sjá fyrri hluta í þessari grein.</span><span class="sxs-lookup"><span data-stu-id="4a998-266">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="4a998-267">Gæðatenging skilgreinir allar eftirfarandi upplýsingar fyrir gæðapöntun sem er mynduð:</span><span class="sxs-lookup"><span data-stu-id="4a998-267">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="4a998-268">Færslutilvikið</span><span class="sxs-lookup"><span data-stu-id="4a998-268">The transaction event</span></span></li>
<li><span data-ttu-id="4a998-269">Safn prófana sem þarf að framkvæma á vörum</span><span class="sxs-lookup"><span data-stu-id="4a998-269">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="4a998-270">Viðunandi gæðastig</span><span class="sxs-lookup"><span data-stu-id="4a998-270">The AQL</span></span></li>
<li><span data-ttu-id="4a998-271">Úrtaksáætlunin</span><span class="sxs-lookup"><span data-stu-id="4a998-271">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="4a998-272">Gæðatengingu verður að skilgreina fyrir hvert afbrigði viðskiptaferlis sem krefst sjálfvirkrar myndunar gæðapöntunar.</span><span class="sxs-lookup"><span data-stu-id="4a998-272">You must define a quality associationfor each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="4a998-273">Til dæmis er hægt að mynda gæðapöntun í viðskiptaferlum fyrir innkaupapantanir, biðgeymslupantanir, sölupantanir eða framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="4a998-273">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a998-274">Prófanir</span><span class="sxs-lookup"><span data-stu-id="4a998-274">Tests</span></span></td>
<td><span data-ttu-id="4a998-275">Notið þessa skjámynd til að skilgreina og skoða einstök próf sem ákvarða hvort framleiðsluvara fyrirtækisins uppfylli gæðakröfur.</span><span class="sxs-lookup"><span data-stu-id="4a998-275">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="4a998-276">Hægt er að úthluta einu eða fleiri einstökum prófum á prófunarflokk.</span><span class="sxs-lookup"><span data-stu-id="4a998-276">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="4a998-277">Í þessu tilviki þarf einnig að tilgreina prófunarsértækar upplýsingar, eins og viðunandi mælingargildi.</span><span class="sxs-lookup"><span data-stu-id="4a998-277">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="4a998-278">Mælingargildi eru notuð fyrir magnbundnar prófanir og prófunarbreytur eru notaðar fyrir eðlisbundin próf.</span><span class="sxs-lookup"><span data-stu-id="4a998-278">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="4a998-279">Magnbundið próf hefur prófunargerð fyrir <strong>Heiltala</strong> eða <strong>Brot</strong> og er einnig með skilgreinda mælieiningu.</span><span class="sxs-lookup"><span data-stu-id="4a998-279">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="4a998-280">Gæðaskilyrði og prófunarniðurstöður sem eru sýnd sem tölur.</span><span class="sxs-lookup"><span data-stu-id="4a998-280">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="4a998-281">Eðlisbundið próf hefur prófunargerðina <strong>Valkostir</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a998-281">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="4a998-282">Eigindlegar prófanir krefjast viðbótarupplýsingar um prófunarbreytuna sem verið er að mæla og tölusetta valkosti hennar.</span><span class="sxs-lookup"><span data-stu-id="4a998-282">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="4a998-283">Gæðaforskriftir og prófunarniðurstöður sem eru sýnd eftir útkomu.</span><span class="sxs-lookup"><span data-stu-id="4a998-283">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="4a998-284">Framleiðslufyrirtæki framkvæmir tvær prófanir á innkeypt efni: magnbundið prófun á gæðum efnis og eigindlega prófun á umbúðaskemmdum.</span><span class="sxs-lookup"><span data-stu-id="4a998-284">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="4a998-285">Fyrirtækið skilgreinir viðbótarupplýsingar um eðlisbundið próf til að auðkenna prófunarbreytu (skemmdar umbúðir) og niðurstöður hennar.</span><span class="sxs-lookup"><span data-stu-id="4a998-285">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="4a998-286">Fyrirtæki notar síðuna <strong>Prófunarflokkar</strong> til að úthluta tveimur prófunum á prófunarflokk og tilgreina prófunarsértækar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="4a998-286">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="4a998-287">Prófunarflokknum er úthlutað á gæðapöntun svo að fyrirtækið getur tilkynnt niðurstöður prófana fyrir bæði prófin.</span><span class="sxs-lookup"><span data-stu-id="4a998-287">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4a998-288">Prófunarflokkar</span><span class="sxs-lookup"><span data-stu-id="4a998-288">Test groups</span></span></td>
<td><span data-ttu-id="4a998-289">Notaðu þessa síðu til að setja upp, breyta og skoða prófunarflokka og einstakar prófanir sem er úthlutað á prófunarflokk.</span><span class="sxs-lookup"><span data-stu-id="4a998-289">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="4a998-290">Efri rúðan birtir prófunarflokka og neðri rúðan birtir prófanir sem er úthlutað á valinn prófunarflokk.</span><span class="sxs-lookup"><span data-stu-id="4a998-290">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="4a998-291">Nokkrum reglum er úthlutað á prófunarflokk, eins og úrtaksáætlun, viðunandi gæðastigi og þörf fyrir eyðileggingarprófun.</span><span class="sxs-lookup"><span data-stu-id="4a998-291">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="4a998-292">Þegar þú úthlutar stöku prófi á prófunarflokk, skilgreinirðu viðbótarupplýsingar, eins og röðina, skjölin og gildisdagsetningarnar.</span><span class="sxs-lookup"><span data-stu-id="4a998-292">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="4a998-293">Fyrir magnbundna prófun innihalda upplýsingar sem eru skilgreindar einnig viðunandi mælingargildi.</span><span class="sxs-lookup"><span data-stu-id="4a998-293">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="4a998-294">Upplýsingarnar eru prófunarfæribreytur og sjálfgefin útkoma fyrir eigindlega prófun.</span><span class="sxs-lookup"><span data-stu-id="4a998-294">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="4a998-295">Prófunarflokkur sem er úthlutað á gæðapöntun skilgreinir sjálfgefið safn prófana sem verður að framkvæma á tiltekinni vöru.</span><span class="sxs-lookup"><span data-stu-id="4a998-295">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="4a998-296">Hins vegar er hægt að bæta við, breyta, eða eyða prófunum innan gæðapöntunar.</span><span class="sxs-lookup"><span data-stu-id="4a998-296">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="4a998-297">Niðurstöður prófana eru tilkynntar fyrir hvert próf á gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="4a998-297">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="4a998-298">Framleiðslufyrirtæki skilgreinir prófunarflokk fyrir hvert afbrigði af gæðareglum sínum.</span><span class="sxs-lookup"><span data-stu-id="4a998-298">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="4a998-299">Mismunandi prófunarflokkar endurspegla mismun á úrtaksáætlunum, safn prófana sem þarf að framkvæma samtímis, viðunandi gæðastigi og öðrum stuðlum.</span><span class="sxs-lookup"><span data-stu-id="4a998-299">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="4a998-300">Fyrir magnbundnar prófanir er einnig mismunur í viðunandi mælingargildum.</span><span class="sxs-lookup"><span data-stu-id="4a998-300">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="4a998-301">Til að framfylgja gæðareglum úthlutar fyrirtækið prófunarflokki á hverja reglu fyrir sjálfvirka myndun gæðapantana á síðunni <strong>Gæðatengingar</strong> og einnig prófunarflokki á gæðapantanir sem eru stofnaðar handvirkt.</span><span class="sxs-lookup"><span data-stu-id="4a998-301">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a998-302">Vörugæðaflokkar</span><span class="sxs-lookup"><span data-stu-id="4a998-302">Item quality groups</span></span></td>
<td><span data-ttu-id="4a998-303">Notaðu þessa síðu til að setja upp, breyta og skoða vörur sem er úthlutað á gæðaflokk eða gæðaflokka sem eru tengdir vöru.</span><span class="sxs-lookup"><span data-stu-id="4a998-303">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="4a998-304">Gæðaflokkur stendur fyrir sameiginlegar prófunarkröfur fyrir vörur.</span><span class="sxs-lookup"><span data-stu-id="4a998-304">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="4a998-305">Þegar búið er að skilgreina kröfur fyrir prófun á síðunni <strong>Prófunarflokkar</strong> er hægt að skilgreina reglur fyrir sjálfvirka myndun gæðapantana.</span><span class="sxs-lookup"><span data-stu-id="4a998-305">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="4a998-306">Til að einfalda ferlið eru ekki skilgreindar reglur fyrir stakar vörur.</span><span class="sxs-lookup"><span data-stu-id="4a998-306">To simplify the process, you don't define rules for individual items.</span></span> <span data-ttu-id="4a998-307">Þess í stað eru skilgreindar reglur fyrir gæðaflokk, með því að nota síðuna <strong>Gæðatengingar</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a998-307">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="4a998-308">Einnig er hægt að nota síðuna <strong>Vörur gæðaflokka</strong> fyrir valinn gæðaflokk til að úthluta viðeigandi vörum á þeim flokki.</span><span class="sxs-lookup"><span data-stu-id="4a998-308">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="4a998-309">Einnig er hægt að nota síðuna <strong>Vörur gæðaflokka</strong> fyrir valda vöru til að úthluta viðeigandi gæðaflokkum á vöruna.</span><span class="sxs-lookup"><span data-stu-id="4a998-309">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="4a998-310">Framleiðslufyrirtæki kaupir ýmislegt hráefni sem eru með sömu prófunarkröfur fyrir væntanlegt eftirlit.</span><span class="sxs-lookup"><span data-stu-id="4a998-310">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="4a998-311">Fyrirtækið skilgreinir gæðaflokk og úthlutar síðan vörunúmerum sem eru tengd hráefnum á þann flokk.</span><span class="sxs-lookup"><span data-stu-id="4a998-311">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="4a998-312">Síðar kaupir fyrirtækið nýja gerð hráefnis sem er með sömu prófunarkröfur.</span><span class="sxs-lookup"><span data-stu-id="4a998-312">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="4a998-313">Í stað þess að setja upp ný skilyrði um prófanir fyrir nýtt efni bætir við fyrirtækið vörunúmeri fyrir nýtt efni fyrirliggjandi gæðaflokk.</span><span class="sxs-lookup"><span data-stu-id="4a998-313">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="4a998-314">Sama framleiðslufyrirtæki framleiðir einnig vörur sem eru með sömu prófunarkröfur í framleiðslu og sendir vörur með sömu kröfur fyrir framkvæmd prófana fyrir sendingu.</span><span class="sxs-lookup"><span data-stu-id="4a998-314">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="4a998-315">Fyrirtækið skilgreinir tvo viðbótargæðaflokka og úthlutar síðan viðeigandi vörunúmerum í hvern gæðaflokk.</span><span class="sxs-lookup"><span data-stu-id="4a998-315">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4a998-316">Prófunarbreytur</span><span class="sxs-lookup"><span data-stu-id="4a998-316">Test variables</span></span></td>
<td><span data-ttu-id="4a998-317">Notaðu síðuna til þess að skilgreina og skoða breyturnar sem eru tengdar við eigindlega prófun.</span><span class="sxs-lookup"><span data-stu-id="4a998-317">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="4a998-318">Fyrir hverja færibreytu eru skilgreindar númeraðar niðurstöður sem sýna mögulega valkosti.</span><span class="sxs-lookup"><span data-stu-id="4a998-318">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="4a998-319">Skilgreina prófanir á <strong>Prófanir</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="4a998-319">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="4a998-320">Fyrir eðlisbundið próf verður að stilla prófunargerðina á <strong>Valkost</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a998-320">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="4a998-321">Notaðu síðuna <strong>Prófunarflokkar</strong> til að úthluta breytu á prófun.</span><span class="sxs-lookup"><span data-stu-id="4a998-321">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="4a998-322">Framleiðslufyrirtæki sem framleiðir kexkökur notar skoðunarpróf sem nær til nokkurra gerða af hinni framleiddu vöru.</span><span class="sxs-lookup"><span data-stu-id="4a998-322">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="4a998-323">Þessi prófun hefur nokkur breytur.</span><span class="sxs-lookup"><span data-stu-id="4a998-323">This inspection test has several variables.</span></span> <span data-ttu-id="4a998-324">Ein færibreyta er bragð, með valkostunum gott eða vont.</span><span class="sxs-lookup"><span data-stu-id="4a998-324">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="4a998-325">Önnur færibreyta er litur, með mögulega niðurstöðu of dökkur, of ljós, og í lagi.</span><span class="sxs-lookup"><span data-stu-id="4a998-325">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4a998-326">Útkomur úr prófunarbreytum</span><span class="sxs-lookup"><span data-stu-id="4a998-326">Test variable outcomes</span></span></td>
<td><span data-ttu-id="4a998-327">Notið þessa síðu til að setja upp, breyta og skoða mögulegar niðurstöður prófana fyrir prófunarbreytu sem tengist gæðaprófi.</span><span class="sxs-lookup"><span data-stu-id="4a998-327">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="4a998-328">Hægt er að gefa hverri niðurstöðu einkunnina <strong>staðist</strong> eða <strong>fallið</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a998-328">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="4a998-329">Skilgreina verður breytuna og niðurstöður hennar fyrir hverja eigindlega prófun sem er skilgreind á síðunni <strong>Prófanir</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a998-329">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="4a998-330">(Fyrir gæðaprófanir er prófunargerðin stillt á <strong>Valkostur</strong> á síðunni <strong>Prófanir</strong>.) Notaðu síðuna <strong>Prófunarflokkar</strong> til að úthluta prófunarbreytu og sjálfgefinni niðurstöðu á staka gæðaprófun.</span><span class="sxs-lookup"><span data-stu-id="4a998-330">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="4a998-331">Framleiðslufyrirtæki sem framleiðir kexkökur notar skoðunarpróf sem nær til nokkurra gerða af hinni framleiddu vöru.</span><span class="sxs-lookup"><span data-stu-id="4a998-331">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="4a998-332">Þessi eftirlitsprófun hefur nokkur breytur.</span><span class="sxs-lookup"><span data-stu-id="4a998-332">This inspection test has of several variables.</span></span> <span data-ttu-id="4a998-333">Ein færibreyta er bragð, með valkostum gott eða vont.</span><span class="sxs-lookup"><span data-stu-id="4a998-333">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="4a998-334">Önnur færibreyta er litur, með mögulega niðurstöðu of dökkur, of ljós, og í lagi.</span><span class="sxs-lookup"><span data-stu-id="4a998-334">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="4a998-335">Hver einasta niðurstaða hefur stöðuna <strong>staðist</strong> eða <strong>fallið</strong>.</span><span class="sxs-lookup"><span data-stu-id="4a998-335">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="4a998-336">Á meðan á gæðaprófi stendur fyrir hverja færibreytu, skráir prófunaraðili niðurstöður prófsins með því að velja eina af mögulegu niðurstöðunum.</span><span class="sxs-lookup"><span data-stu-id="4a998-336">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="4a998-337">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="4a998-337">See also</span></span>
--------

[<span data-ttu-id="4a998-338">Ferli gæðastjórnunar</span><span class="sxs-lookup"><span data-stu-id="4a998-338">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="4a998-339">Virkja stjórnun ósamkvæmni</span><span class="sxs-lookup"><span data-stu-id="4a998-339">Enabling nonconformance management</span></span>](enable-nonconformance-management.md)

