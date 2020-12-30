---
title: Yfirlit yfir gæðastjórnun
description: Þessi grein lýsir því hvernig hægt er að nota gæðastjórnun í Dynamics 365 Supply Chain Management til að bæta gæði afurða innan aðfangakeðju þinnar.
author: perlynne
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTestAssociationTable, InventTestGroup, InventTestItemQualityGroup, InventTestTable, InventTestVariable, InventTestVariableOutcome
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1d7828e6bb9a3684c1d76e2cfac96174a8dfbf4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430405"
---
# <a name="quality-management-overview"></a><span data-ttu-id="66eb8-103">Yfirlit yfir gæðastjórnun</span><span class="sxs-lookup"><span data-stu-id="66eb8-103">Quality management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66eb8-104">Þessi grein lýsir því hvernig hægt er að nota gæðastjórnun í Dynamics 365 Supply Chain Management til að bæta gæði afurða innan aðfangakeðju þinnar.</span><span class="sxs-lookup"><span data-stu-id="66eb8-104">This topic describes how you can use quality management in Dynamics 365 Supply Chain Management to help improve product quality within your supply chain.</span></span>

<span data-ttu-id="66eb8-105">Gæðastjórnun getur hjálpað við að stjórna biðtíma þegar ósamkvæmar afurðir eru meðhöndlaðar, óháð uppruna þeirra.</span><span class="sxs-lookup"><span data-stu-id="66eb8-105">Quality management can help you manage turnaround times when you handle nonconforming products, regardless of their point of origin.</span></span> <span data-ttu-id="66eb8-106">Þar sem greiningargerðir eru tengdar leiðréttingaskýrslum getur Supply Chain Management raðað verki til að leiðrétta vandamál og komið í veg fyrir þau verði endurtekin.</span><span class="sxs-lookup"><span data-stu-id="66eb8-106">Because diagnostic types are linked to correction reporting, Supply Chain Management can schedule tasks to correct problems and prevent them from recurring.</span></span>

<span data-ttu-id="66eb8-107">Auk virkni fyrir stjórnun ósamkvæmni inniheldur gæðastjórnun virkni til að rekja úthreyfingar eftir gerð vanda (jafnvel innri vandamál) og til að auðkenna lausnir sem skammtíma- eða langtímalausnir.</span><span class="sxs-lookup"><span data-stu-id="66eb8-107">In addition to functionality for managing nonconformance, quality management includes functionality for tracking issues by problem type (even internal problems), and for identifying solutions as short-term or long-term.</span></span> <span data-ttu-id="66eb8-108">Upplýsingar um afkastavísi (KPI) veita innsýn í sögulegan feril fyrri vandamála með ósamkvæmi og þeirra lausna sem voru notuð til að leiðrétta þau.</span><span class="sxs-lookup"><span data-stu-id="66eb8-108">Statistics about key performance indicators (KPIs) provide insight into the history of previous nonconformance issues and the solutions that were used to correct them.</span></span> <span data-ttu-id="66eb8-109">Hægt er að nota söguleg gögn til að fara yfir skilvirkni fyrri gæðaráðstafana og ákvarða viðeigandi mælieiningar sem nota á í framtíðinni.</span><span class="sxs-lookup"><span data-stu-id="66eb8-109">You can use historical data to review the effectiveness of previous quality measures and determine appropriate measures to use in the future.</span></span>

<span data-ttu-id="66eb8-110">Þegar gæðatenging er sett upp getur Supply Chain Management myndað gæðapantanir fyrir ýmis viðskiptaferli, tilvik og skilyrði.</span><span class="sxs-lookup"><span data-stu-id="66eb8-110">When you set up a quality association, Supply Chain Management can generate quality orders for various business processes, events, and conditions.</span></span> <span data-ttu-id="66eb8-111">Gæðatengingin getur náð yfir ákveðna vöru, einstökan vöruflokk eða allar vörur.</span><span class="sxs-lookup"><span data-stu-id="66eb8-111">The quality association can cover a specific item, a specific group of items, or all items.</span></span>

## <a name="examples-of-the-use-of-quality-management"></a><span data-ttu-id="66eb8-112">Dæmi um notkun á gæðastjórnun</span><span class="sxs-lookup"><span data-stu-id="66eb8-112">Examples of the use of quality management</span></span>
<span data-ttu-id="66eb8-113">Gæðastjórnun er sveigjanleg og hægt er að innleiða hana á mismunandi vegu til að uppfylla kröfur um tiltekið stig í aðgerðum framboðskeðju.</span><span class="sxs-lookup"><span data-stu-id="66eb8-113">Quality management is flexible and can be implemented in various ways to meet the requirements of specific levels of supply chain operations.</span></span> <span data-ttu-id="66eb8-114">Eftirfarandi dæmi sýna hugsanlega notkun á þessum eiginleikum:</span><span class="sxs-lookup"><span data-stu-id="66eb8-114">The following examples illustrate possible uses of these features:</span></span>

-   <span data-ttu-id="66eb8-115">Hefja ferli gæðaeftirlits sjálfvirkt, byggt á fyrirfram skilgreindum skilyrðum (við vöruhússkráningu innkaupapöntunar frá tilteknum lánardrottni).</span><span class="sxs-lookup"><span data-stu-id="66eb8-115">Automatically start a quality control process, based on predefined criteria (upon warehouse registration of a purchase order from a specific vendor).</span></span>
-   <span data-ttu-id="66eb8-116">Læsa birgðum við skoðun til að koma í veg fyrir að ósamþykktar birgðir séu notaðar (alger stöðvun á pöntunarmagni innkaup).</span><span class="sxs-lookup"><span data-stu-id="66eb8-116">Block inventory during inspection to prevent non-approved inventory from being used (full blocking of purchase order quantities).</span></span>
-   <span data-ttu-id="66eb8-117">Vörusýnishorn eru notuð sem hluti af gæðatengingu til að skilgreina magn gildandi efnislegra birgða sem verður að skoða.</span><span class="sxs-lookup"><span data-stu-id="66eb8-117">Use item sampling as part of a quality association to define the amount of current physical inventory that must be inspected.</span></span> <span data-ttu-id="66eb8-118">Sýnataka getur verið byggð á föstu magni, prósentu eða fullri númeraplötu.</span><span class="sxs-lookup"><span data-stu-id="66eb8-118">Sampling can be based on fixed quantities, a percentage, or full license plate.</span></span>

> [!NOTE]
> <span data-ttu-id="66eb8-119">Eiginleikinn _Gæðastjórnun fyrir vöruhúsaferla_ eykur möguleika gæðastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="66eb8-119">The _Quality management for warehouse processes_ feature extends the capabilities of quality management.</span></span> <span data-ttu-id="66eb8-120">Ef þú ert að nota þennan eiginleika skaltu skoða [Gæðastjórnun fyrir vöruhúsaferli](quality-management-for-warehouses-processes.md) fyrir dæmi um hvernig gæðastjórnun virkar þegar hún er virkjuð.</span><span class="sxs-lookup"><span data-stu-id="66eb8-120">If you are using this feature, then see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md) for examples of how quality management works when it's enabled.</span></span>

-   <span data-ttu-id="66eb8-121">Stofna gæðapantanir fyrir hluta móttöku.</span><span class="sxs-lookup"><span data-stu-id="66eb8-121">Create quality orders for partial receipts.</span></span> <span data-ttu-id="66eb8-122">Til að stofna gæðapöntun sem byggir á magni sem tekið er við efnislega með pöntun verður að velja gátreitinn **Eftir uppfærðu magni** á skjámyndinni **Vörusýnishorn**.</span><span class="sxs-lookup"><span data-stu-id="66eb8-122">To create a quality order that is based on the quantity that is physically received with an order, you must select the **Per updated quantity** check box on the **Item sampling** form.</span></span>
-   <span data-ttu-id="66eb8-123">Stofna prófunargerðir sem innihalda lágmark, hámark og markprófunargildi og framkvæma eigindlega-samanborið við-eigindlega prófun sem hefur fyrirfram skilgreindar niðurstöður villuleitar.</span><span class="sxs-lookup"><span data-stu-id="66eb8-123">Create test types that include minimum, maximum, and target test values, and perform qualitative-versus-quantitative testing that has predefined validation results.</span></span>
-   <span data-ttu-id="66eb8-124">Tilgreina viðunandi gæðastig (AQL) til að stjórna vikmörkum gæðaráðstafana.</span><span class="sxs-lookup"><span data-stu-id="66eb8-124">Specify an acceptable quality level (AQL) to control quality measure tolerances.</span></span>
-   <span data-ttu-id="66eb8-125">Tilgreina tilföng sem skoðunaraðgerð krefst, eins og prófunarsvæði og prófunartæki.</span><span class="sxs-lookup"><span data-stu-id="66eb8-125">Specify the resources that an inspection operation requires, such as a test area and test instruments.</span></span>

## <a name="working-with-quality-associations"></a><span data-ttu-id="66eb8-126">Vinna með gæðatengingar</span><span class="sxs-lookup"><span data-stu-id="66eb8-126">Working with quality associations</span></span>
<span data-ttu-id="66eb8-127">Viðskiptaferli sem notar gæðatengingu getur verið tengt mismunandi upprunaskjölum, eins og innkaupapöntunum, sölupöntunum eða framleiðslupöntunum.</span><span class="sxs-lookup"><span data-stu-id="66eb8-127">The business process that uses a quality association can be related to various source documents, such as purchase orders, sales orders, or production orders.</span></span>

<span data-ttu-id="66eb8-128">Hver gæðatengingafærsla skilgreinir einnig prófanir, viðunandi gæðastig og úrtaksáætlun sem eiga við myndaðar gæðapantanir.</span><span class="sxs-lookup"><span data-stu-id="66eb8-128">Each quality association record defines the set of tests, the AQL, and the sampling plan that applies to the quality orders that are generated.</span></span> <span data-ttu-id="66eb8-129">Skilgreina verður gæðatengingafærslu fyrir hvert afbrigði viðskiptaferlis.</span><span class="sxs-lookup"><span data-stu-id="66eb8-129">You must define a quality association record for each variation in a business process.</span></span> <span data-ttu-id="66eb8-130">Til dæmis er hægt að setja upp gæðatengingu sem myndar gæðapöntun þegar innhreyfingarskjal afurða innkaupapöntun er uppfært.</span><span class="sxs-lookup"><span data-stu-id="66eb8-130">For example, you can set up a quality association that generates a quality order when a purchase order product receipt is updated.</span></span> <span data-ttu-id="66eb8-131">Það fer eftir uppsetningu á keyrsluáætlun hvort hægt sé að stöðva kveikjuferlið sjálft á meðan gæðapöntun er opin eða hvort hægt sé að stöðva næstu ferli, eins og reikningsfærslu á innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="66eb8-131">Depending on the setup of the execution plan, the triggering process itself can be blocked while there is an open quality order, or the next processes, such as purchase order invoicing, can be blocked.</span></span>

<span data-ttu-id="66eb8-132">**Ábending:** Meðan gæðapantanir eru opnar er birgðamagn sjálfkrafa stöðvað til útgáfu.</span><span class="sxs-lookup"><span data-stu-id="66eb8-132">**Note:** While there are open quality orders, inventory quantities are automatically blocked from being issued.</span></span> <span data-ttu-id="66eb8-133">Það fer eftir **Alger stöðvun** stillingunni á síðunni **Vörusýnishorn** hvort magn sé annaðhvort magn í gæðapöntun eða magn í upprunaskjalslínu.</span><span class="sxs-lookup"><span data-stu-id="66eb8-133">Depending on the **Full blocking** setting on the **Item samplings** page, the quantity is either the quantity on the quality order or the quantity on the source document line.</span></span>

<span data-ttu-id="66eb8-134">Fyrir tiltekið viðskiptaferli auðkennir gæðatengingarfærslan tilvik og skilyrði sem mynda skal gæðapöntun fyrir.</span><span class="sxs-lookup"><span data-stu-id="66eb8-134">For a given business process, the quality association record identifies the event and the conditions that a quality order is generated for.</span></span> <span data-ttu-id="66eb8-135">Skilyrðin geta átt sérstaklega við svæði eða lögaðila.</span><span class="sxs-lookup"><span data-stu-id="66eb8-135">The conditions can be specific to either a site or a legal entity.</span></span> <span data-ttu-id="66eb8-136">Aðeins er hægt að mynda gæðapöntun sem felur í sér eyðileggingarprófun þegar lagerbirgðir eru til staðar fyrir tilvikið.</span><span class="sxs-lookup"><span data-stu-id="66eb8-136">A quality order that involves destructive tests can be generated only when on-hand inventory exists for the event.</span></span>

<span data-ttu-id="66eb8-137">Eftirfarandi dæmi sýna hvernig gæðatengingafærsla er skilgreind fyrir afbrigði hvers viðskiptaferlis.</span><span class="sxs-lookup"><span data-stu-id="66eb8-137">The following examples illustrate how a quality association record is defined for the variations in each business process.</span></span> <span data-ttu-id="66eb8-138">Í eftirfarandi töflu eru dæmin tekin saman eftir tilviki og skilyrðum sem skilgreind eru af gæðatengingarfærslu.</span><span class="sxs-lookup"><span data-stu-id="66eb8-138">For each example, the following table summarizes the events and conditions that are defined by a quality association record.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="66eb8-139">Gerð tilvísunar</span><span class="sxs-lookup"><span data-stu-id="66eb8-139">Reference type</span></span></th>
<th><span data-ttu-id="66eb8-140">Gerð tilviks</span><span class="sxs-lookup"><span data-stu-id="66eb8-140">Event type</span></span></th>
<th><span data-ttu-id="66eb8-141">Framkvæmd</span><span class="sxs-lookup"><span data-stu-id="66eb8-141">Execution</span></span></th>
<th><span data-ttu-id="66eb8-142">Lokun tilviks</span><span class="sxs-lookup"><span data-stu-id="66eb8-142">Event blocking</span></span></th>
<th><span data-ttu-id="66eb8-143">Tilvísun skjals</span><span class="sxs-lookup"><span data-stu-id="66eb8-143">Document reference</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="66eb8-144">Birgðir</span><span class="sxs-lookup"><span data-stu-id="66eb8-144">Inventory</span></span></td>
<td><span data-ttu-id="66eb8-145">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="66eb8-145">Not applicable</span></span></td>
<td><span data-ttu-id="66eb8-146">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="66eb8-146">Not applicable</span></span></td>
<td><span data-ttu-id="66eb8-147">Ekkert</span><span class="sxs-lookup"><span data-stu-id="66eb8-147">None</span></span></td>
<td><span data-ttu-id="66eb8-148">Allt</span><span class="sxs-lookup"><span data-stu-id="66eb8-148">All</span></span></td>
</tr>
<tr>
<td rowspan="7"><span data-ttu-id="66eb8-149">Sala</span><span class="sxs-lookup"><span data-stu-id="66eb8-149">Sales</span></span></td>
<td rowspan="4"><span data-ttu-id="66eb8-150">Tiltektarferli er áætlað</span><span class="sxs-lookup"><span data-stu-id="66eb8-150">Picking process is scheduled</span></span></td>
<td rowspan="4"><span data-ttu-id="66eb8-151">Fyrir</span><span class="sxs-lookup"><span data-stu-id="66eb8-151">Before</span></span></td>
<td><span data-ttu-id="66eb8-152">Ekkert</span><span class="sxs-lookup"><span data-stu-id="66eb8-152">None</span></span></td>
<td rowspan="22"><span data-ttu-id="66eb8-153">Tilgreint kenni, Flokkur eða Allir aðeins</span><span class="sxs-lookup"><span data-stu-id="66eb8-153">Specific ID, Group, or All only</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-154">Tiltektarferli</span><span class="sxs-lookup"><span data-stu-id="66eb8-154">Picking process</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-155">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="66eb8-155">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-156">Reikningur</span><span class="sxs-lookup"><span data-stu-id="66eb8-156">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="66eb8-157">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="66eb8-157">Packing slip</span></span></td>
<td rowspan="3"><span data-ttu-id="66eb8-158">Fyrir</span><span class="sxs-lookup"><span data-stu-id="66eb8-158">Before</span></span></td>
<td><span data-ttu-id="66eb8-159">Ekkert</span><span class="sxs-lookup"><span data-stu-id="66eb8-159">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-160">Fylgiseðill</span><span class="sxs-lookup"><span data-stu-id="66eb8-160">Packing slip</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-161">Reikningur</span><span class="sxs-lookup"><span data-stu-id="66eb8-161">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="15"><span data-ttu-id="66eb8-162">Innkaup</span><span class="sxs-lookup"><span data-stu-id="66eb8-162">Purchase</span></span></td>
<td rowspan="7"><span data-ttu-id="66eb8-163">Innhreyfingaskjal</span><span class="sxs-lookup"><span data-stu-id="66eb8-163">Receipt list</span></span></td>
<td rowspan="4"><span data-ttu-id="66eb8-164">Fyrir</span><span class="sxs-lookup"><span data-stu-id="66eb8-164">Before</span></span></td>
<td><span data-ttu-id="66eb8-165">Ekkert</span><span class="sxs-lookup"><span data-stu-id="66eb8-165">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-166">Innhreyfingaskjal</span><span class="sxs-lookup"><span data-stu-id="66eb8-166">Receipt list</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-167">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="66eb8-167">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-168">Reikningur</span><span class="sxs-lookup"><span data-stu-id="66eb8-168">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="66eb8-169">Eftir</span><span class="sxs-lookup"><span data-stu-id="66eb8-169">After</span></span></td>
<td><span data-ttu-id="66eb8-170">Ekkert</span><span class="sxs-lookup"><span data-stu-id="66eb8-170">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-171">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="66eb8-171">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-172">Reikningur</span><span class="sxs-lookup"><span data-stu-id="66eb8-172">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="66eb8-173">Skráning</span><span class="sxs-lookup"><span data-stu-id="66eb8-173">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="66eb8-174">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="66eb8-174">Not applicable</span></span></td>
<td><span data-ttu-id="66eb8-175">Ekkert</span><span class="sxs-lookup"><span data-stu-id="66eb8-175">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-176">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="66eb8-176">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-177">Reikningur</span><span class="sxs-lookup"><span data-stu-id="66eb8-177">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="66eb8-178">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="66eb8-178">Product receipt</span></span></td>
<td rowspan="3"><span data-ttu-id="66eb8-179">Fyrir</span><span class="sxs-lookup"><span data-stu-id="66eb8-179">Before</span></span></td>
<td><span data-ttu-id="66eb8-180">Ekkert</span><span class="sxs-lookup"><span data-stu-id="66eb8-180">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-181">Innhreyfingarskjal afurðar</span><span class="sxs-lookup"><span data-stu-id="66eb8-181">Product receipt</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-182">Reikningur</span><span class="sxs-lookup"><span data-stu-id="66eb8-182">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="66eb8-183">Eftir</span><span class="sxs-lookup"><span data-stu-id="66eb8-183">After</span></span></td>
<td><span data-ttu-id="66eb8-184">Ekkert</span><span class="sxs-lookup"><span data-stu-id="66eb8-184">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-185">Reikningur</span><span class="sxs-lookup"><span data-stu-id="66eb8-185">Invoice</span></span></td>
</tr>
<tr>
<td rowspan="8"><span data-ttu-id="66eb8-186">Framleiðsla</span><span class="sxs-lookup"><span data-stu-id="66eb8-186">Production</span></span></td>
<td rowspan="3"><span data-ttu-id="66eb8-187">Skráning</span><span class="sxs-lookup"><span data-stu-id="66eb8-187">Registration</span></span></td>
<td rowspan="3"><span data-ttu-id="66eb8-188">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="66eb8-188">Not applicable</span></span></td>
<td><span data-ttu-id="66eb8-189">Ekkert</span><span class="sxs-lookup"><span data-stu-id="66eb8-189">None</span></span></td>
<td rowspan="12"><span data-ttu-id="66eb8-190">Allt</span><span class="sxs-lookup"><span data-stu-id="66eb8-190">All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-191">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="66eb8-191">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-192">Við skil</span><span class="sxs-lookup"><span data-stu-id="66eb8-192">End</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="66eb8-193">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="66eb8-193">Report as finished</span></span></td>
<td rowspan="3"><span data-ttu-id="66eb8-194">Fyrir</span><span class="sxs-lookup"><span data-stu-id="66eb8-194">Before</span></span></td>
<td><span data-ttu-id="66eb8-195">Ekkert</span><span class="sxs-lookup"><span data-stu-id="66eb8-195">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-196">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="66eb8-196">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-197">Við skil</span><span class="sxs-lookup"><span data-stu-id="66eb8-197">End</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="66eb8-198">Eftir</span><span class="sxs-lookup"><span data-stu-id="66eb8-198">After</span></span></td>
<td><span data-ttu-id="66eb8-199">Ekkert</span><span class="sxs-lookup"><span data-stu-id="66eb8-199">None</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-200">Við skil</span><span class="sxs-lookup"><span data-stu-id="66eb8-200">End</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="66eb8-201">Biðgeymsla</span><span class="sxs-lookup"><span data-stu-id="66eb8-201">Quarantine</span></span></td>
<td rowspan="3"><span data-ttu-id="66eb8-202">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="66eb8-202">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="66eb8-203">Fyrir</span><span class="sxs-lookup"><span data-stu-id="66eb8-203">Before</span></span></td>
<td><span data-ttu-id="66eb8-204">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="66eb8-204">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-205">Við skil</span><span class="sxs-lookup"><span data-stu-id="66eb8-205">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-206">Eftir</span><span class="sxs-lookup"><span data-stu-id="66eb8-206">After</span></span></td>
<td><span data-ttu-id="66eb8-207">Við skil</span><span class="sxs-lookup"><span data-stu-id="66eb8-207">End</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-208">Við skil</span><span class="sxs-lookup"><span data-stu-id="66eb8-208">End</span></span></td>
<td><span data-ttu-id="66eb8-209">Fyrir</span><span class="sxs-lookup"><span data-stu-id="66eb8-209">Before</span></span></td>
<td><span data-ttu-id="66eb8-210">Við skil</span><span class="sxs-lookup"><span data-stu-id="66eb8-210">End</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="66eb8-211">Leiðaraðgerð</span><span class="sxs-lookup"><span data-stu-id="66eb8-211">Route operation</span></span></td>
<td rowspan="3"><span data-ttu-id="66eb8-212">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="66eb8-212">Report as finished</span></span></td>
<td rowspan="2"><span data-ttu-id="66eb8-213">Fyrir</span><span class="sxs-lookup"><span data-stu-id="66eb8-213">Before</span></span></td>
<td><span data-ttu-id="66eb8-214">Ekkert</span><span class="sxs-lookup"><span data-stu-id="66eb8-214">None</span></span></td>
<td rowspan="3"><span data-ttu-id="66eb8-215">Tilgreitn kenni, Flokkur eða Allt, og Tilfangasértækt, Flokkur eða Allt</span><span class="sxs-lookup"><span data-stu-id="66eb8-215">Specific ID, Group, or All, and Resource specific, Group, or All</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-216">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="66eb8-216">Report as finished</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-217">Eftir</span><span class="sxs-lookup"><span data-stu-id="66eb8-217">After</span></span></td>
<td><span data-ttu-id="66eb8-218">Ekkert</span><span class="sxs-lookup"><span data-stu-id="66eb8-218">None</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="66eb8-219">Framleiðsla aukaafurðar</span><span class="sxs-lookup"><span data-stu-id="66eb8-219">Co-product production</span></span></td>
<td><span data-ttu-id="66eb8-220">Skráning</span><span class="sxs-lookup"><span data-stu-id="66eb8-220">Registration</span></span></td>
<td><span data-ttu-id="66eb8-221">Ekki tiltækt</span><span class="sxs-lookup"><span data-stu-id="66eb8-221">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="66eb8-222">Ekkert</span><span class="sxs-lookup"><span data-stu-id="66eb8-222">None</span></span></td>
<td rowspan="3"><span data-ttu-id="66eb8-223">Allt</span><span class="sxs-lookup"><span data-stu-id="66eb8-223">All</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="66eb8-224">Bóka tilbúið</span><span class="sxs-lookup"><span data-stu-id="66eb8-224">Report as finished</span></span></td>
<td><span data-ttu-id="66eb8-225">Fyrir</span><span class="sxs-lookup"><span data-stu-id="66eb8-225">Before</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-226">Eftir</span><span class="sxs-lookup"><span data-stu-id="66eb8-226">After</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="66eb8-227">Eftirfarandi tafla veitir frekari upplýsingar um hvernig hægt er að mynda gæðapantanir fyrir tilgreindar gerðir ferla.</span><span class="sxs-lookup"><span data-stu-id="66eb8-227">The following table provides more information about how quality orders can be generated for specific types of processes.</span></span>
<div class="tableSection">

<table>
<tbody>
<tr>
<th><span data-ttu-id="66eb8-228">Gerð ferlis</span><span class="sxs-lookup"><span data-stu-id="66eb8-228">Type of process</span></span></th>
<th><span data-ttu-id="66eb8-229">Þegar hægt er að mynda gæðapantanir sjálfvirkt</span><span class="sxs-lookup"><span data-stu-id="66eb8-229">When quality orders can be automatically generated</span></span></th>
<th><span data-ttu-id="66eb8-230">Þegar hægt er að mynda gæðapantanir ef eyðileggingarprófun er áskilin</span><span class="sxs-lookup"><span data-stu-id="66eb8-230">When quality orders can be generated if destructive testing is required</span></span></th>
<th><span data-ttu-id="66eb8-231">Upplýsingar um skilyrði</span><span class="sxs-lookup"><span data-stu-id="66eb8-231">Condition information</span></span></th>
<th><span data-ttu-id="66eb8-232">Upplýsingar um handvirka myndun</span><span class="sxs-lookup"><span data-stu-id="66eb8-232">Manual generation information</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="66eb8-233">Innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="66eb8-233">Purchase order</span></span></td>
<td><span data-ttu-id="66eb8-234">Á undan eða eftir komulista eða innhreyfingarskjal afurða fyrir efni sem er móttekið er bókuð</span><span class="sxs-lookup"><span data-stu-id="66eb8-234">Before or after a receipts list or product receipt for the material that is received is posted</span></span></td>
<td><span data-ttu-id="66eb8-235">Eftir innhreyfingarskjal afurða fyrir efni sem er móttekið er bókað, þar sem efnið verður að vera tiltækt fyrir eyðileggingarprófun</span><span class="sxs-lookup"><span data-stu-id="66eb8-235">After the product receipt for the material that is received is posted, because the material must be available for destructive testing</span></span></td>
<td><span data-ttu-id="66eb8-236">Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða lánardrottins eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="66eb8-236">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="66eb8-237">Gæðapöntun sem er stofnuð handvirkt og vísar í innkaupapöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="66eb8-237">A manually generated quality order that refers to a purchase order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-238">Biðgeymslupöntun</span><span class="sxs-lookup"><span data-stu-id="66eb8-238">Quarantine order</span></span></td>
<td><span data-ttu-id="66eb8-239">Á undan eða eftir biðgeymslupöntunin er skráð sem lokið eða lokið</span><span class="sxs-lookup"><span data-stu-id="66eb8-239">Before or after the quarantine order is reported as finished or ended</span></span></td>
<td><span data-ttu-id="66eb8-240">Ekki er hægt að mynda gæðapantanir sem krefjast eyðileggingarprófana.&#39;</span><span class="sxs-lookup"><span data-stu-id="66eb8-240">Quality orders that require destructive tests can&#39;t be generated.</span></span> <span data-ttu-id="66eb8-241">Gert er ráð fyrir að virkni biðgeymslupöntunar annist ráðstöfun á efni sem er eyðilagt.&#39;</span><span class="sxs-lookup"><span data-stu-id="66eb8-241">It&#39;s assumed that the quarantine order functionality handles the disposition of the material that is destroyed.</span></span></td>
<td><span data-ttu-id="66eb8-242">Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða lánardrottins eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="66eb8-242">The requirement for a quality order can reflect a particular site, item, or vendor, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="66eb8-243">Gæðapöntun sem er stofnuð handvirkt og vísar í biðgeymslupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="66eb8-243">A manually generated quality order that refers to a quarantine order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-244">Sölupöntun</span><span class="sxs-lookup"><span data-stu-id="66eb8-244">Sales order</span></span></td>
<td><span data-ttu-id="66eb8-245">Á undan á áætluðu tiltektarferli eða fylgiseðilsuppfærslu fyrir vörur sem verið er að senda</span><span class="sxs-lookup"><span data-stu-id="66eb8-245">Before a scheduled picking process or packing slip update for the items that are being shipped</span></span></td>
<td><span data-ttu-id="66eb8-246">Á hvaða þrepi sem er</span><span class="sxs-lookup"><span data-stu-id="66eb8-246">At any step</span></span></td>
<td><span data-ttu-id="66eb8-247">Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða viðskiptavinar eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="66eb8-247">The requirement for a quality order can reflect a particular site, item, or customer, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="66eb8-248">Gæðapöntun sem er stofnuð handvirkt og vísar í sölupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="66eb8-248">A manually generated quality order that refers to a sales order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-249">Framleiðslupöntun</span><span class="sxs-lookup"><span data-stu-id="66eb8-249">Production order</span></span></td>
<td><span data-ttu-id="66eb8-250">Á undan eða eftir að tilbúið magn fyrir framleiðslupöntun er skráð</span><span class="sxs-lookup"><span data-stu-id="66eb8-250">Before or after the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="66eb8-251">Eftir að tilbúið magn fyrir framleiðslupöntun er skráð</span><span class="sxs-lookup"><span data-stu-id="66eb8-251">After the finished quantity for the production order is reported</span></span></td>
<td><span data-ttu-id="66eb8-252">Þörf á gæðapöntun getur verið vegna tiltekins svæðis eða vöru eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="66eb8-252">The requirement for a quality order can reflect a particular site or item, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="66eb8-253">Gæðapöntun sem er stofnuð handvirkt og vísar í framleiðslupöntun getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="66eb8-253">A manually generated quality order that refers to a production order can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-254">Framleiðslupöntun sem er með leiðaraðgerð</span><span class="sxs-lookup"><span data-stu-id="66eb8-254">Production order that has a route operation</span></span></td>
<td><span data-ttu-id="66eb8-255">Á undan eða eftir að skýrslu er lokið fyrir aðgerð</span><span class="sxs-lookup"><span data-stu-id="66eb8-255">Before or after the report is finished for an operation</span></span></td>
<td><span data-ttu-id="66eb8-256">Á undan eða eftir að skýrsluframleiðslu er lokið fyrir síðustu aðgerð</span><span class="sxs-lookup"><span data-stu-id="66eb8-256">After the reporting production is finished for the last operation</span></span></td>
<td><span data-ttu-id="66eb8-257">Þörf á gæðapöntun getur verið vegna tiltekins svæðis, vöru eða rekstrartilfanga eða samsetningu þessara skilyrða.</span><span class="sxs-lookup"><span data-stu-id="66eb8-257">The requirement for a quality order can reflect a particular, site, item, or operations resource, or a combination of these conditions.</span></span></td>
<td><span data-ttu-id="66eb8-258">Gæðapöntun sem er stofnuð handvirkt og vísar í leiðaraðgerð getur notað upplýsingar úr gæðatengingafærslu, til dæmis úrtaksáætlun til prófunar.</span><span class="sxs-lookup"><span data-stu-id="66eb8-258">A manually generated quality order that refers to a route operation can use information in a quality association record, such as the test sampling plan.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-259">Birgðir</span><span class="sxs-lookup"><span data-stu-id="66eb8-259">Inventory</span></span></td>
<td><span data-ttu-id="66eb8-260">Ekki er hægt að mynda gæðapöntun sjálfkrafa fyrir færslu í birgðabók eða fyrir flutningspantanafærslur.</span><span class="sxs-lookup"><span data-stu-id="66eb8-260">A quality order cannot be automatically generated for a transaction in an inventory journal or for transfer order transactions.</span></span></td>
<td></td>
<td></td>
<td><span data-ttu-id="66eb8-261">Gæðapöntun verður að vera stofnuð handvirkt fyrir birgðamagn vöru.&#39;</span><span class="sxs-lookup"><span data-stu-id="66eb8-261">A quality order must be created manually for an item&#39;s inventory quantity.</span></span> <span data-ttu-id="66eb8-262">Efnislegra lagerbirgða er krafist.</span><span class="sxs-lookup"><span data-stu-id="66eb8-262">Physical on-hand inventory is required.</span></span></td>
</tr>
</tbody>
</table>

## <a name="quality-order-auto-generation-examples"></a><span data-ttu-id="66eb8-263">Dæmi um sjálfvirka myndun á gæðapöntun</span><span class="sxs-lookup"><span data-stu-id="66eb8-263">Quality order auto-generation examples</span></span>

### <a name="purchasing"></a><span data-ttu-id="66eb8-264">Innkaup</span><span class="sxs-lookup"><span data-stu-id="66eb8-264">Purchasing</span></span>

<span data-ttu-id="66eb8-265">Í innkaupum, ef þú stillir reitinn **Gerð tilviks** á **Innhreyfingarskjal afurðar** og reitinn **Framkvæmd** á **Eftir** á síðunni **Gæðatengingar** færðu eftirfarandi niðurstöður:</span><span class="sxs-lookup"><span data-stu-id="66eb8-265">In purchasing, if you set the **Event type** field to **Product receipt** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span> 

- <span data-ttu-id="66eb8-266">Ef valkosturinn **Eftir uppfærðu magni** er stilltur á **Já** myndast gæðapöntun fyrir hverja innhreyfingu gegn innkaupapöntuninni, byggð á mótteknu magni og stillingum í vörusýni.</span><span class="sxs-lookup"><span data-stu-id="66eb8-266">If the **Per updated quantity** option is set to **Yes**, a quality order is generated for every receipt against the purchase order, based on the received quantity and settings in the item sampling.</span></span> <span data-ttu-id="66eb8-267">Í hvert skipti sem magn er móttekið gegn innkaupapöntuninni myndast nýjar gæðapantanir miðað við nýlega fengið magn.</span><span class="sxs-lookup"><span data-stu-id="66eb8-267">Every time that a quantity is received against the purchase order, new quality orders are generated based on the newly received quantity.</span></span>
- <span data-ttu-id="66eb8-268">Ef valkosturinn **Eftir uppfærðu magni** er stilltur á **Nei** myndast gæðapöntun fyrir fyrstu innhreyfinguna gegn innkaupapöntuninni, byggð á mótteknu magni.</span><span class="sxs-lookup"><span data-stu-id="66eb8-268">If the **Per updated quantity** option is set to **No**, a quality order is generated for the first receipt against the purchase order, based on the received quantity.</span></span> <span data-ttu-id="66eb8-269">Að auki eru ein eða fleiri gæðapantanir búnar til miðað við eftirstandandi magn, eftir því hverjar rakningarvíddirnar eru.</span><span class="sxs-lookup"><span data-stu-id="66eb8-269">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions.</span></span> <span data-ttu-id="66eb8-270">Gæðapantanir eru ekki myndaðar fyrir síðari innhreyfingar gegn innkaupapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="66eb8-270">Quality orders aren't generated for subsequent receipts against the purchase order.</span></span>

### <a name="production"></a><span data-ttu-id="66eb8-271">Vinnsla</span><span class="sxs-lookup"><span data-stu-id="66eb8-271">Production</span></span>

<span data-ttu-id="66eb8-272">Í framleiðslu, ef þú stillir reitinn **Gerð tilviks** á **Tilkynna sem lokið** og reitinn **Framkvæmd** á **Eftir** á síðunni **Gæðatengingar** færðu eftirfarandi niðurstöður:</span><span class="sxs-lookup"><span data-stu-id="66eb8-272">In production, if you set the **Event type** field to **Report as finished** and the **Execution** field to **After** on the **Quality associations** page, you get the following results:</span></span>

- <span data-ttu-id="66eb8-273">Ef valkosturinn **Eftir uppfærðu magni** er stilltur á **Já** myndast gæðapöntun fyrir hvert lokið magn og stillingar í vörusýni.</span><span class="sxs-lookup"><span data-stu-id="66eb8-273">If the **Per updated quantity** option is set to **Yes**, a quality order is generated based on every finished quantity and settings in the item sampling.</span></span> <span data-ttu-id="66eb8-274">Í hvert skipti sem magn er tilkynnt sem lokið gegn framleiðslupöntuninni myndast nýjar gæðapantanir miðað við nýlega lokið magn.</span><span class="sxs-lookup"><span data-stu-id="66eb8-274">Every time that a quantity is reported as finished against the production order, new quality orders are generated based on newly finished quantity.</span></span> <span data-ttu-id="66eb8-275">Þessi myndunarrök eru í samræmi við innkaup.</span><span class="sxs-lookup"><span data-stu-id="66eb8-275">This generation logic is consistent with purchasing.</span></span>
- <span data-ttu-id="66eb8-276">Ef valkosturinn **Eftir uppfærðu magni** er stilltur á **Nei** myndast gæðapöntun fyrir fyrsta skiptið sem magn er tilkynnt sem lokið, byggt á loknu magni.</span><span class="sxs-lookup"><span data-stu-id="66eb8-276">If the **Per updated quantity** option is set to **No**, a quality order is generated the first time that a quantity is reported as finished, based on the finished quantity.</span></span> <span data-ttu-id="66eb8-277">Að auki eru ein eða fleiri gæðapantanir búnar til miðað við eftirstandandi magn, eftir því hverjar rakningarvíddirnar eru í vörusýninu.</span><span class="sxs-lookup"><span data-stu-id="66eb8-277">Additionally, one or more quality orders are created based on the remaining quantity, depending on the tracking dimensions of the item sampling.</span></span> <span data-ttu-id="66eb8-278">Gæðapantanir eru ekki búnar til fyrir seinna lokið magn.</span><span class="sxs-lookup"><span data-stu-id="66eb8-278">Quality orders aren't generated for subsequent finished quantities.</span></span>

<table>
<tbody>
<tr>
<th><span data-ttu-id="66eb8-279">Gæðaforskriftir</span><span class="sxs-lookup"><span data-stu-id="66eb8-279">Quality specification</span></span></th>
<th><span data-ttu-id="66eb8-280">Uppfært magn á</span><span class="sxs-lookup"><span data-stu-id="66eb8-280">Per updated quantity</span></span></th>
<th><span data-ttu-id="66eb8-281">Á rakningarvídd</span><span class="sxs-lookup"><span data-stu-id="66eb8-281">Per tracking dimension</span></span></th>
<th><span data-ttu-id="66eb8-282">Niðurstaða</span><span class="sxs-lookup"><span data-stu-id="66eb8-282">Result</span></span></th>
</tr>
<tr>
<td><span data-ttu-id="66eb8-283">Prósenta: 10%</span><span class="sxs-lookup"><span data-stu-id="66eb8-283">Percentage: 10%</span></span></td>
<td><span data-ttu-id="66eb8-284">Já</span><span class="sxs-lookup"><span data-stu-id="66eb8-284">Yes</span></span></td>
<td>
<p><span data-ttu-id="66eb8-285">Rununúmer: Nr.</span><span class="sxs-lookup"><span data-stu-id="66eb8-285">Batch number: No</span></span></p>
<p><span data-ttu-id="66eb8-286">Raðnúmer: Nr.</span><span class="sxs-lookup"><span data-stu-id="66eb8-286">Serial number: No</span></span></p>
</td>
<td>
<p><span data-ttu-id="66eb8-287">Pöntunarmagn: 100</span><span class="sxs-lookup"><span data-stu-id="66eb8-287">Order quantity: 100</span></span></p>
<ol>
<li><span data-ttu-id="66eb8-288">Tilkynna sem lokið fyrir 30</span><span class="sxs-lookup"><span data-stu-id="66eb8-288">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="66eb8-289">Gæðapöntun #1 fyrir 3 (10% af 30)</span><span class="sxs-lookup"><span data-stu-id="66eb8-289">Quality order #1 for 3 (10% of 30)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="66eb8-290">Tilkynna sem lokið fyrir 70</span><span class="sxs-lookup"><span data-stu-id="66eb8-290">Report as finished for 70</span></span>
<ul>
<li><span data-ttu-id="66eb8-291">Gæðapöntun # 2 fyrir 7 (10% af pöntunarmagni sem eftir er, sem jafngildir 70 í þessu tilfelli)</span><span class="sxs-lookup"><span data-stu-id="66eb8-291">Quality order #2 for 7 (10% of the remaining order quantity, which equals 70 in this case)</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-292">Fast magn: 1</span><span class="sxs-lookup"><span data-stu-id="66eb8-292">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="66eb8-293">Nr</span><span class="sxs-lookup"><span data-stu-id="66eb8-293">No</span></span></td>
<td>
<p><span data-ttu-id="66eb8-294">Rununúmer: Nr.</span><span class="sxs-lookup"><span data-stu-id="66eb8-294">Batch number: No</span></span></p>
<p><span data-ttu-id="66eb8-295">Raðnúmer: Nr.</span><span class="sxs-lookup"><span data-stu-id="66eb8-295">Serial number: No</span></span></p>
</td>
<td><span data-ttu-id="66eb8-296">Pöntunarmagn: 100</span><span class="sxs-lookup"><span data-stu-id="66eb8-296">Order quantity: 100</span></span>
<ol>
<li><span data-ttu-id="66eb8-297">Tilkynna sem lokið fyrir 30</span><span class="sxs-lookup"><span data-stu-id="66eb8-297">Report as finished for 30</span></span>
<ul>
<li><span data-ttu-id="66eb8-298">Gæðapöntun #1 er stofnuð fyrir 1 (fyrir fyrsta magn sem var tilkynnt sem lokið, sem hefur fast gildi 1)</span><span class="sxs-lookup"><span data-stu-id="66eb8-298">Quality order #1 for 1 (for the first reported-as-finished quantity, which has a fixed value of 1)</span></span></li>
<li><span data-ttu-id="66eb8-299">Gæðapöntun #2 er stofnuð fyrir 1 (fyrir eftirstandandi magn, sem er samt með fast gildi 1)</span><span class="sxs-lookup"><span data-stu-id="66eb8-299">Quality order #2 for 1 (for the remaining quantity, which still has a fixed value of 1)</span></span></li>
</ul>
</li>
<li><span data-ttu-id="66eb8-300">Tilkynna sem lokið fyrir 10</span><span class="sxs-lookup"><span data-stu-id="66eb8-300">Report as finished for 10</span></span>
<ul>
<li><span data-ttu-id="66eb8-301">Engar gæðapantanir eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="66eb8-301">No quality orders are created.</span></span></li>
</ul>
</li>
<li><span data-ttu-id="66eb8-302">Tilkynna sem lokið fyrir 60</span><span class="sxs-lookup"><span data-stu-id="66eb8-302">Report as finished for 60</span></span>
<ul>
<li><span data-ttu-id="66eb8-303">Engar gæðapantanir eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="66eb8-303">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-304">Fast magn: 1</span><span class="sxs-lookup"><span data-stu-id="66eb8-304">Fixed quantity: 1</span></span></td>
<td><span data-ttu-id="66eb8-305">Já</span><span class="sxs-lookup"><span data-stu-id="66eb8-305">Yes</span></span></td>
<td>
<p><span data-ttu-id="66eb8-306">Rununúmer: Já</span><span class="sxs-lookup"><span data-stu-id="66eb8-306">Batch number: Yes</span></span></p>
<p><span data-ttu-id="66eb8-307">Raðnúmer: Já</span><span class="sxs-lookup"><span data-stu-id="66eb8-307">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="66eb8-308">Pöntunarmagn: 10</span><span class="sxs-lookup"><span data-stu-id="66eb8-308">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="66eb8-309">Tilkynna sem lokið fyrir 3: 1 fyrir #b1, #s1; 1 fyrir #b2, #s2; og 1 fyrir #b3, #s3</span><span class="sxs-lookup"><span data-stu-id="66eb8-309">Report as finished for 3: 1 for #b1, #s1; 1 for #b2, #s2; and 1 for #b3, #s3</span></span>
<ul>
<li><span data-ttu-id="66eb8-310">Gæðapöntun #1 fyrir 1 í lotu #b1, raðnúmer #s1</span><span class="sxs-lookup"><span data-stu-id="66eb8-310">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="66eb8-311">Gæðapöntun #2 fyrir 1 í lotu #b2, raðnúmer #s2</span><span class="sxs-lookup"><span data-stu-id="66eb8-311">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="66eb8-312">Gæðapöntun #3 fyrir 1 í lotu #b3, raðnúmer #s3</span><span class="sxs-lookup"><span data-stu-id="66eb8-312">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
</ul>
</li>
<li><span data-ttu-id="66eb8-313">Tilkynna sem lokið fyrir 2: 1 fyrir #b4, #s4; og 1 fyrir #b5, #s5</span><span class="sxs-lookup"><span data-stu-id="66eb8-313">Report as finished for 2: 1 for #b4, #s4; and 1 for #b5, #s5</span></span>
<ul>
<li><span data-ttu-id="66eb8-314">Gæðapöntun #4 fyrir 1 í lotu #b4, raðnúmer #s4</span><span class="sxs-lookup"><span data-stu-id="66eb8-314">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
<li><span data-ttu-id="66eb8-315">Gæðapöntun #5 fyrir 1 í lotu #b5, raðnúmer #s5</span><span class="sxs-lookup"><span data-stu-id="66eb8-315">Quality order #5 for 1 of batch #b5, serial #s5</span></span></li>
</ul>
</li>
</ol>
<p><span data-ttu-id="66eb8-316"><strong>Ath.:</strong> Hægt er að endurnýta rununa.</span><span class="sxs-lookup"><span data-stu-id="66eb8-316"><strong>Note:</strong> The batch can be reused.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="66eb8-317">Fast magn: 2</span><span class="sxs-lookup"><span data-stu-id="66eb8-317">Fixed quantity: 2</span></span></td>
<td><span data-ttu-id="66eb8-318">Nr</span><span class="sxs-lookup"><span data-stu-id="66eb8-318">No</span></span></td>
<td>
<p><span data-ttu-id="66eb8-319">Rununúmer: Já</span><span class="sxs-lookup"><span data-stu-id="66eb8-319">Batch number: Yes</span></span></p>
<p><span data-ttu-id="66eb8-320">Raðnúmer: Já</span><span class="sxs-lookup"><span data-stu-id="66eb8-320">Serial number: Yes</span></span></p>
</td>
<td>
<p><span data-ttu-id="66eb8-321">Pöntunarmagn: 10</span><span class="sxs-lookup"><span data-stu-id="66eb8-321">Order quantity: 10</span></span></p>
<ol>
<li><span data-ttu-id="66eb8-322">Tilkynna sem lokið fyrir 4: 1 fyrir #b1, #s1; 1 fyrir #b2, #s2; og 1 fyrir #b3, #s3; og 1 fyrir #b4, #s4</span><span class="sxs-lookup"><span data-stu-id="66eb8-322">Report as finished for 4: 1 for #b1, #s1; 1 for #b2, #s2; 1 for #b3, #s3; and 1 for #b4, #s4</span></span>
<ul>
<li><span data-ttu-id="66eb8-323">Gæðapöntun #1 fyrir 1 í lotu #b1, raðnúmer #s1</span><span class="sxs-lookup"><span data-stu-id="66eb8-323">Quality order #1 for 1 of batch #b1, serial #s1</span></span></li>
<li><span data-ttu-id="66eb8-324">Gæðapöntun #2 fyrir 1 í lotu #b2, raðnúmer #s2</span><span class="sxs-lookup"><span data-stu-id="66eb8-324">Quality order #2 for 1 of batch #b2, serial #s2</span></span></li>
<li><span data-ttu-id="66eb8-325">Gæðapöntun #3 fyrir 1 í lotu #b3, raðnúmer #s3</span><span class="sxs-lookup"><span data-stu-id="66eb8-325">Quality order #3 for 1 of batch #b3, serial #s3</span></span></li>
<li><span data-ttu-id="66eb8-326">Gæðapöntun #4 fyrir 1 í lotu #b4, raðnúmer #s4</span><span class="sxs-lookup"><span data-stu-id="66eb8-326">Quality order #4 for 1 of batch #b4, serial #s4</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="66eb8-327">Gæðapöntun #5 fyrir 2, án tilvísunar í runu og raðnúmer</span><span class="sxs-lookup"><span data-stu-id="66eb8-327">Quality order #5 for 2, without a reference to a batch and a serial number</span></span></li>
</ul>
</li>
<li><span data-ttu-id="66eb8-328">Tilkynna sem lokið fyrir 6: 1 fyrir #b5, #s5; 1 fyrir #b6, #s6; 1 fyrir #b7, #s7; 1 fyrir #b8, #s8; 1 fyrir #b9, #s9; og 1 fyrir #b10, #s10</span><span class="sxs-lookup"><span data-stu-id="66eb8-328">Report as finished for 6: 1 for #b5, #s5; 1 for #b6, #s6; 1 for #b7, #s7; 1 for #b8, #s8; 1 for #b9, #s9; and 1 for #b10, #s10</span></span>
<ul>
<li><span data-ttu-id="66eb8-329">Engar gæðapantanir eru búnar til.</span><span class="sxs-lookup"><span data-stu-id="66eb8-329">No quality orders are created.</span></span></li>
</ul>
</li>
</ol>
</td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="66eb8-330">Eiginleikinn *Gæðastjórnun fyrir vöruhúsaferli* bætir við möguleikum fyrir úrvinnslu gæðapantana fyrir framleiðslu með **Gerð tilviks** stillt á *Tilkynna sem lokið* og **Framkvæmd** stillt á *Eftir* og fyrir innkaup með **Gerð tilviks** stillt á *Skráning*.</span><span class="sxs-lookup"><span data-stu-id="66eb8-330">The *Quality management for warehouse processes* feature adds capabilities for quality order processing for production with **Event type** set to *Report as finished* and **Execution** set to *After*, and for purchases with **Event type** set to *Registration*.</span></span> <span data-ttu-id="66eb8-331">Frekari upplýsingar er að finna í [Gæðastjórnun fyrir vöruhúsaferli](quality-management-for-warehouses-processes.md).</span><span class="sxs-lookup"><span data-stu-id="66eb8-331">For details, see [Quality management for warehouse processes](quality-management-for-warehouses-processes.md).</span></span>

## <a name="quality-management-pages"></a><span data-ttu-id="66eb8-332">Gæðastjórnunarsíður</span><span class="sxs-lookup"><span data-stu-id="66eb8-332">Quality management pages</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66eb8-333">Síða</span><span class="sxs-lookup"><span data-stu-id="66eb8-333">Page</span></span></th>
<th><span data-ttu-id="66eb8-334">lýsing</span><span class="sxs-lookup"><span data-stu-id="66eb8-334">Description</span></span></th>
<th><span data-ttu-id="66eb8-335">Dæmi</span><span class="sxs-lookup"><span data-stu-id="66eb8-335">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="66eb8-336">Gæðatengingar</span><span class="sxs-lookup"><span data-stu-id="66eb8-336">Quality associations</span></span></td>
<td><span data-ttu-id="66eb8-337">Sjá fyrri hluta í þessari grein.</span><span class="sxs-lookup"><span data-stu-id="66eb8-337">See the previous sections of this article.</span></span></td>
<td><span data-ttu-id="66eb8-338">Gæðatenging skilgreinir allar eftirfarandi upplýsingar fyrir gæðapöntun sem er mynduð:</span><span class="sxs-lookup"><span data-stu-id="66eb8-338">A quality association defines all the following information for a quality order that is generated:</span></span>
<ul>
<li><span data-ttu-id="66eb8-339">Færslutilvikið</span><span class="sxs-lookup"><span data-stu-id="66eb8-339">The transaction event</span></span></li>
<li><span data-ttu-id="66eb8-340">Safn prófana sem þarf að framkvæma á vörum</span><span class="sxs-lookup"><span data-stu-id="66eb8-340">The set of tests that must be performed on the items</span></span></li>
<li><span data-ttu-id="66eb8-341">Viðunandi gæðastig</span><span class="sxs-lookup"><span data-stu-id="66eb8-341">The AQL</span></span></li>
<li><span data-ttu-id="66eb8-342">Úrtaksáætlunin</span><span class="sxs-lookup"><span data-stu-id="66eb8-342">The sampling plan</span></span></li>
</ul>
<span data-ttu-id="66eb8-343">Gæðatengingu verður að skilgreina fyrir hvert afbrigði viðskiptaferlis sem krefst sjálfvirkrar myndunar gæðapöntunar.</span><span class="sxs-lookup"><span data-stu-id="66eb8-343">You must define a quality association for each variation in a business process that requires automatic generation of quality orders.</span></span> <span data-ttu-id="66eb8-344">Til dæmis er hægt að mynda gæðapöntun í viðskiptaferlum fyrir innkaupapantanir, biðgeymslupantanir, sölupantanir eða framleiðslupantanir.</span><span class="sxs-lookup"><span data-stu-id="66eb8-344">For example, a quality order can be generated in the business processes for purchase orders, quarantine orders, sales orders, and production orders.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66eb8-345">Prófanir</span><span class="sxs-lookup"><span data-stu-id="66eb8-345">Tests</span></span></td>
<td><span data-ttu-id="66eb8-346">Notið þessa skjámynd til að skilgreina og skoða einstök próf sem ákvarða hvort framleiðsluvara fyrirtækisins uppfylli gæðakröfur.</span><span class="sxs-lookup"><span data-stu-id="66eb8-346">Use this page to define and view the individual tests that determine whether your products meet quality specifications.</span></span> <span data-ttu-id="66eb8-347">Hægt er að úthluta einu eða fleiri einstökum prófum á prófunarflokk.</span><span class="sxs-lookup"><span data-stu-id="66eb8-347">You can assign one or more individual tests to a test group.</span></span> <span data-ttu-id="66eb8-348">Í þessu tilviki þarf einnig að tilgreina prófunarsértækar upplýsingar, eins og viðunandi mælingargildi.</span><span class="sxs-lookup"><span data-stu-id="66eb8-348">In this case, you also specify test-specific information, such as the acceptable measurement values.</span></span> <span data-ttu-id="66eb8-349">Mælingargildi eru notuð fyrir magnbundnar prófanir og prófunarbreytur eru notaðar fyrir eðlisbundin próf.</span><span class="sxs-lookup"><span data-stu-id="66eb8-349">Measurement values are used for quantitative tests, and test variables are used for qualitative tests.</span></span>
<ul>
<li><span data-ttu-id="66eb8-350">Magnbundið próf hefur prófunargerð fyrir <strong>Heiltala</strong> eða <strong>Brot</strong> og er einnig með skilgreinda mælieiningu.</span><span class="sxs-lookup"><span data-stu-id="66eb8-350">A quantitative test has a test type of <strong>Integer</strong> or <strong>Fraction</strong>, and also has a designated unit of measure.</span></span> <span data-ttu-id="66eb8-351">Gæðaskilyrði og prófunarniðurstöður sem eru sýnd sem tölur.</span><span class="sxs-lookup"><span data-stu-id="66eb8-351">Quality specifications and test results are expressed as numbers.</span></span></li>
<li><span data-ttu-id="66eb8-352">Eðlisbundið próf hefur prófunargerðina <strong>Valkostir</strong>.</span><span class="sxs-lookup"><span data-stu-id="66eb8-352">A qualitative test has a test type of <strong>Option</strong>.</span></span> <span data-ttu-id="66eb8-353">Eigindlegar prófanir krefjast viðbótarupplýsingar um prófunarbreytuna sem verið er að mæla og tölusetta valkosti hennar.</span><span class="sxs-lookup"><span data-stu-id="66eb8-353">Qualitative tests require additional information about the test variable that is being measured and its enumerated options.</span></span> <span data-ttu-id="66eb8-354">Gæðaforskriftir og prófunarniðurstöður sem eru sýnd eftir útkomu.</span><span class="sxs-lookup"><span data-stu-id="66eb8-354">Quality specifications and test results are expressed according to an outcome.</span></span></li>
</ul></td>
<td><span data-ttu-id="66eb8-355">Framleiðslufyrirtæki framkvæmir tvær prófanir á innkeypt efni: magnbundið prófun á gæðum efnis og eigindlega prófun á umbúðaskemmdum.</span><span class="sxs-lookup"><span data-stu-id="66eb8-355">A manufacturing company performs two tests on purchased material: a quantitative test about material quality and a qualitative test about packaging damage.</span></span> <span data-ttu-id="66eb8-356">Fyrirtækið skilgreinir viðbótarupplýsingar um eðlisbundið próf til að auðkenna prófunarbreytu (skemmdar umbúðir) og niðurstöður hennar.</span><span class="sxs-lookup"><span data-stu-id="66eb8-356">The company defines additional information about the qualitative test to identify the test variable (damaged packaging) and its outcomes.</span></span> <span data-ttu-id="66eb8-357">Fyrirtæki notar síðuna <strong>Prófunarflokkar</strong> til að úthluta tveimur prófunum á prófunarflokk og tilgreina prófunarsértækar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="66eb8-357">The company uses the <strong>Test groups</strong> page to assign the two tests to a test group and to specify the test-specific information.</span></span> <span data-ttu-id="66eb8-358">Prófunarflokknum er úthlutað á gæðapöntun svo að fyrirtækið getur tilkynnt niðurstöður prófana fyrir bæði prófin.</span><span class="sxs-lookup"><span data-stu-id="66eb8-358">The test group is assigned to a quality order, so that the company can report test results for the two tests.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66eb8-359">Prófunarflokkar</span><span class="sxs-lookup"><span data-stu-id="66eb8-359">Test groups</span></span></td>
<td><span data-ttu-id="66eb8-360">Notaðu þessa síðu til að setja upp, breyta og skoða prófunarflokka og einstakar prófanir sem er úthlutað á prófunarflokk.</span><span class="sxs-lookup"><span data-stu-id="66eb8-360">Use this page to set up, edit, and view test groups and the individual tests that are assigned to a test group.</span></span> <span data-ttu-id="66eb8-361">Efri rúðan birtir prófunarflokka og neðri rúðan birtir prófanir sem er úthlutað á valinn prófunarflokk.</span><span class="sxs-lookup"><span data-stu-id="66eb8-361">The upper pane displays test groups, and the lower pane displays the tests that are assigned to a selected test group.</span></span> <span data-ttu-id="66eb8-362">Nokkrum reglum er úthlutað á prófunarflokk, eins og úrtaksáætlun, viðunandi gæðastigi og þörf fyrir eyðileggingarprófun.</span><span class="sxs-lookup"><span data-stu-id="66eb8-362">You assign several policies to a test group, such as a sampling plan, an AQL, and the requirement for destructive testing.</span></span> <span data-ttu-id="66eb8-363">Þegar þú úthlutar stöku prófi á prófunarflokk, skilgreinirðu viðbótarupplýsingar, eins og röðina, skjölin og gildisdagsetningarnar.</span><span class="sxs-lookup"><span data-stu-id="66eb8-363">When you assign an individual test to a test group, you define additional information, such as the sequence, documents, and validity dates.</span></span> <span data-ttu-id="66eb8-364">Fyrir magnbundna prófun innihalda upplýsingar sem eru skilgreindar einnig viðunandi mælingargildi.</span><span class="sxs-lookup"><span data-stu-id="66eb8-364">For a quantitative test, the information that you define also includes the acceptable measurement values.</span></span> <span data-ttu-id="66eb8-365">Upplýsingarnar eru prófunarfæribreytur og sjálfgefin útkoma fyrir eigindlega prófun.</span><span class="sxs-lookup"><span data-stu-id="66eb8-365">For a qualitative test, the information includes the test variable and default outcome.</span></span> <span data-ttu-id="66eb8-366">Prófunarflokkur sem er úthlutað á gæðapöntun skilgreinir sjálfgefið safn prófana sem verður að framkvæma á tiltekinni vöru.</span><span class="sxs-lookup"><span data-stu-id="66eb8-366">The test group that is assigned to a quality order defines the default set of tests that must be performed on the specified item.</span></span> <span data-ttu-id="66eb8-367">Hins vegar er hægt að bæta við, breyta, eða eyða prófunum innan gæðapöntunar.</span><span class="sxs-lookup"><span data-stu-id="66eb8-367">However, you can add, delete, or change tests on the quality order.</span></span> <span data-ttu-id="66eb8-368">Niðurstöður prófana eru tilkynntar fyrir hvert próf á gæðapöntun.</span><span class="sxs-lookup"><span data-stu-id="66eb8-368">Test results are reported for each test on a quality order.</span></span></td>
<td><span data-ttu-id="66eb8-369">Framleiðslufyrirtæki skilgreinir prófunarflokk fyrir hvert afbrigði af gæðareglum sínum.</span><span class="sxs-lookup"><span data-stu-id="66eb8-369">A manufacturing company defines a test group for each variation of its quality guidelines.</span></span> <span data-ttu-id="66eb8-370">Mismunandi prófunarflokkar endurspegla mismun á úrtaksáætlunum, safn prófana sem þarf að framkvæma samtímis, viðunandi gæðastigi og öðrum stuðlum.</span><span class="sxs-lookup"><span data-stu-id="66eb8-370">The various test groups reflect differences in the sampling plans, the sets of tests that must be performed together, the AQL, and other factors.</span></span> <span data-ttu-id="66eb8-371">Fyrir magnbundnar prófanir er einnig mismunur í viðunandi mælingargildum.</span><span class="sxs-lookup"><span data-stu-id="66eb8-371">For quantitative tests, there are also differences in the acceptable measurement values.</span></span> <span data-ttu-id="66eb8-372">Til að framfylgja gæðareglum úthlutar fyrirtækið prófunarflokki á hverja reglu fyrir sjálfvirka myndun gæðapantana á síðunni <strong>Gæðatengingar</strong> og einnig prófunarflokki á gæðapantanir sem eru stofnaðar handvirkt.</span><span class="sxs-lookup"><span data-stu-id="66eb8-372">To enforce its quality guidelines, the company assigns a test group to each rule for automatically generating quality orders on the <strong>Quality associations</strong> page, and also assigns a test group to quality orders that are manually created.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66eb8-373">Vörugæðaflokkar</span><span class="sxs-lookup"><span data-stu-id="66eb8-373">Item quality groups</span></span></td>
<td><span data-ttu-id="66eb8-374">Notaðu þessa síðu til að setja upp, breyta og skoða vörur sem er úthlutað á gæðaflokk eða gæðaflokka sem eru tengdir vöru.</span><span class="sxs-lookup"><span data-stu-id="66eb8-374">Use this page to set up, edit, and view the items that are assigned to a quality group or the quality groups that are assigned to an item.</span></span> <span data-ttu-id="66eb8-375">Gæðaflokkur stendur fyrir sameiginlegar prófunarkröfur fyrir vörur.</span><span class="sxs-lookup"><span data-stu-id="66eb8-375">A quality group represents common testing requirements for items.</span></span> <span data-ttu-id="66eb8-376">Þegar búið er að skilgreina kröfur fyrir prófun á síðunni <strong>Prófunarflokkar</strong> er hægt að skilgreina reglur fyrir sjálfvirka myndun gæðapantana.</span><span class="sxs-lookup"><span data-stu-id="66eb8-376">After you define the test requirements on the <strong>Test groups</strong> page, you can define the rules for automatically generating quality orders.</span></span> <span data-ttu-id="66eb8-377">Til að einfalda ferlið eru ekki skilgreindar reglur fyrir stakar vörur.&#39;</span><span class="sxs-lookup"><span data-stu-id="66eb8-377">To simplify the process, you don&#39;t define rules for individual items.</span></span> <span data-ttu-id="66eb8-378">Þess í stað eru skilgreindar reglur fyrir gæðaflokk, með því að nota síðuna <strong>Gæðatengingar</strong>.</span><span class="sxs-lookup"><span data-stu-id="66eb8-378">Instead, you define rules for a quality group, by using the <strong>Quality associations</strong> page.</span></span> <span data-ttu-id="66eb8-379">Einnig er hægt að nota síðuna <strong>Vörur gæðaflokka</strong> fyrir valinn gæðaflokk til að úthluta viðeigandi vörum á þeim flokki.</span><span class="sxs-lookup"><span data-stu-id="66eb8-379">You can also use the <strong>Item quality groups</strong> page for a selected quality group to assign relevant items to that group.</span></span> <span data-ttu-id="66eb8-380">Einnig er hægt að nota síðuna <strong>Vörur gæðaflokka</strong> fyrir valda vöru til að úthluta viðeigandi gæðaflokkum á vöruna.</span><span class="sxs-lookup"><span data-stu-id="66eb8-380">You can also use the <strong>Item quality groups</strong> page for a selected item to assign relevant quality groups to that item.</span></span></td>
<td><span data-ttu-id="66eb8-381">Framleiðslufyrirtæki kaupir ýmislegt hráefni sem eru með sömu prófunarkröfur fyrir væntanlegt eftirlit.</span><span class="sxs-lookup"><span data-stu-id="66eb8-381">A manufacturing company purchases various raw materials that have the same testing requirements for incoming inspection.</span></span> <span data-ttu-id="66eb8-382">Fyrirtækið skilgreinir gæðaflokk og úthlutar síðan vörunúmerum sem eru tengd hráefnum á þann flokk.</span><span class="sxs-lookup"><span data-stu-id="66eb8-382">The company defines a quality group and then assigns the item numbers that are associated with the raw materials to that group.</span></span> <span data-ttu-id="66eb8-383">Síðar kaupir fyrirtækið nýja gerð hráefnis sem er með sömu prófunarkröfur.</span><span class="sxs-lookup"><span data-stu-id="66eb8-383">Later, the company purchases a new type of raw material that has the same testing requirements.</span></span> <span data-ttu-id="66eb8-384">Í stað þess að setja upp ný skilyrði um prófanir fyrir nýtt efni bætir við fyrirtækið vörunúmeri fyrir nýtt efni fyrirliggjandi gæðaflokk.</span><span class="sxs-lookup"><span data-stu-id="66eb8-384">Instead of setting up new testing requirements for the new material, the company adds the item number for the new material to the existing quality group.</span></span> <span data-ttu-id="66eb8-385">Sama framleiðslufyrirtæki framleiðir einnig vörur sem eru með sömu prófunarkröfur í framleiðslu og sendir vörur með sömu kröfur fyrir framkvæmd prófana fyrir sendingu.</span><span class="sxs-lookup"><span data-stu-id="66eb8-385">The same manufacturing company also produces items that have the same production testing requirements and ships items that have the same requirement for pre-shipment testing.</span></span> <span data-ttu-id="66eb8-386">Fyrirtækið skilgreinir tvo viðbótargæðaflokka og úthlutar síðan viðeigandi vörunúmerum í hvern gæðaflokk.</span><span class="sxs-lookup"><span data-stu-id="66eb8-386">The company defines two additional quality groups and then assigns the relevant item numbers to each group.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66eb8-387">Prófunarbreytur</span><span class="sxs-lookup"><span data-stu-id="66eb8-387">Test variables</span></span></td>
<td><span data-ttu-id="66eb8-388">Notaðu síðuna til þess að skilgreina og skoða breyturnar sem eru tengdar við eigindlega prófun.</span><span class="sxs-lookup"><span data-stu-id="66eb8-388">Use this page to define and view the variables that are associated with a qualitative test.</span></span> <span data-ttu-id="66eb8-389">Fyrir hverja færibreytu eru skilgreindar númeraðar niðurstöður sem sýna mögulega valkosti.</span><span class="sxs-lookup"><span data-stu-id="66eb8-389">For each variable, you define enumerated outcomes that represent the possible options.</span></span> <span data-ttu-id="66eb8-390">Skilgreina prófanir á <strong>Prófanir</strong> síðu.</span><span class="sxs-lookup"><span data-stu-id="66eb8-390">You define tests on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="66eb8-391">Fyrir eðlisbundið próf verður að stilla prófunargerðina á <strong>Valkost</strong>.</span><span class="sxs-lookup"><span data-stu-id="66eb8-391">For qualitative tests, you must set the test type to <strong>Option</strong>.</span></span> <span data-ttu-id="66eb8-392">Notaðu síðuna <strong>Prófunarflokkar</strong> til að úthluta breytu á prófun.</span><span class="sxs-lookup"><span data-stu-id="66eb8-392">Use the <strong>Test groups</strong> page to assign a test variable to an individual test.</span></span></td>
<td><span data-ttu-id="66eb8-393">Framleiðslufyrirtæki sem framleiðir kexkökur notar skoðunarpróf sem nær til nokkurra gerða af hinni framleiddu vöru.</span><span class="sxs-lookup"><span data-stu-id="66eb8-393">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="66eb8-394">Þessi prófun hefur nokkur breytur.</span><span class="sxs-lookup"><span data-stu-id="66eb8-394">This inspection test has several variables.</span></span> <span data-ttu-id="66eb8-395">Ein færibreyta er bragð, með valkostunum gott eða vont.</span><span class="sxs-lookup"><span data-stu-id="66eb8-395">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="66eb8-396">Önnur færibreyta er litur, með mögulega niðurstöðu of dökkur, of ljós, og í lagi.</span><span class="sxs-lookup"><span data-stu-id="66eb8-396">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66eb8-397">Útkomur úr prófunarbreytum</span><span class="sxs-lookup"><span data-stu-id="66eb8-397">Test variable outcomes</span></span></td>
<td><span data-ttu-id="66eb8-398">Notið þessa síðu til að setja upp, breyta og skoða mögulegar niðurstöður prófana fyrir prófunarbreytu sem tengist gæðaprófi.</span><span class="sxs-lookup"><span data-stu-id="66eb8-398">Use this page to set up, edit, and to view the possible test results for a test variable that is associated with a qualitative test.</span></span> <span data-ttu-id="66eb8-399">Hægt er að gefa hverri niðurstöðu einkunnina <strong>staðist</strong> eða <strong>fallið</strong>.</span><span class="sxs-lookup"><span data-stu-id="66eb8-399">For each outcome, you assign a <strong>pass</strong> or <strong>fail</strong> status.</span></span> <span data-ttu-id="66eb8-400">Skilgreina verður breytuna og niðurstöður hennar fyrir hverja eigindlega prófun sem er skilgreind á síðunni <strong>Prófanir</strong>.</span><span class="sxs-lookup"><span data-stu-id="66eb8-400">You must define a variable and its outcomes for each qualitative test that is defined on the <strong>Tests</strong> page.</span></span> <span data-ttu-id="66eb8-401">(Fyrir gæðaprófanir er prófunargerðin stillt á <strong>Valkostur</strong> á síðunni <strong>Prófanir</strong>.) Notaðu síðuna <strong>Prófunarflokkar</strong> til að úthluta prófunarbreytu og sjálfgefinni niðurstöðu á staka gæðaprófun.</span><span class="sxs-lookup"><span data-stu-id="66eb8-401">(For qualitative tests, the test type is set to <strong>Option</strong> on the <strong>Tests</strong> page.) Use the <strong>Test groups</strong> page to assign a test variable and the default outcome to an individual qualitative test.</span></span></td>
<td><span data-ttu-id="66eb8-402">Framleiðslufyrirtæki sem framleiðir kexkökur notar skoðunarpróf sem nær til nokkurra gerða af hinni framleiddu vöru.</span><span class="sxs-lookup"><span data-stu-id="66eb8-402">A manufacturing company that produces cookies uses an inspection test for the finished product.</span></span> <span data-ttu-id="66eb8-403">Þessi eftirlitsprófun hefur nokkur breytur.</span><span class="sxs-lookup"><span data-stu-id="66eb8-403">This inspection test has of several variables.</span></span> <span data-ttu-id="66eb8-404">Ein færibreyta er bragð, með valkostum gott eða vont.</span><span class="sxs-lookup"><span data-stu-id="66eb8-404">One variable is taste, and the possible outcomes for this variable are good and bad.</span></span> <span data-ttu-id="66eb8-405">Önnur færibreyta er litur, með mögulega niðurstöðu of dökkur, of ljós, og í lagi.</span><span class="sxs-lookup"><span data-stu-id="66eb8-405">A second variable is color, and the possible outcomes are too dark, too light, and correct.</span></span> <span data-ttu-id="66eb8-406">Hver einasta niðurstaða hefur stöðuna <strong>staðist</strong> eða <strong>fallið</strong>.</span><span class="sxs-lookup"><span data-stu-id="66eb8-406">A status of <strong>pass</strong> or <strong>fail</strong> is assigned to each outcome.</span></span> <span data-ttu-id="66eb8-407">Á meðan á gæðaprófi stendur fyrir hverja færibreytu, skráir prófunaraðili niðurstöður prófsins með því að velja eina af mögulegu niðurstöðunum.</span><span class="sxs-lookup"><span data-stu-id="66eb8-407">During the inspection test for each variable, the inspector reports the test result by selecting one of the outcomes.</span></span></td>
</tr>
</tbody>
</table>



<a name="additional-resources"></a><span data-ttu-id="66eb8-408">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="66eb8-408">Additional resources</span></span>
--------

[<span data-ttu-id="66eb8-409">Gæðastjórnunarferli</span><span class="sxs-lookup"><span data-stu-id="66eb8-409">Quality management processes</span></span>](quality-management-processes.md)

[<span data-ttu-id="66eb8-410">Stjórnun ósamkvæmi</span><span class="sxs-lookup"><span data-stu-id="66eb8-410">Nonconformance management</span></span>](enable-nonconformance-management.md)

[<span data-ttu-id="66eb8-411">Gæðastjórnun fyrir vöruhúsaferli</span><span class="sxs-lookup"><span data-stu-id="66eb8-411">Quality management for warehouse processes</span></span>](quality-management-for-warehouses-processes.md)
