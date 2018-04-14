---
title: "Forsendur fyrir staðalkostnaði"
description: "Þetta efnisatriði fjallar um grundvallarskref við notkun staðalkostnaðar."
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventStdCostConv, CostingVersion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f7f1cef3198462eab15c1c7d2de4c5d4a5576919
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="prerequisites-for-standard-costs"></a><span data-ttu-id="c304f-103">Forsendur fyrir staðalkostnaði</span><span class="sxs-lookup"><span data-stu-id="c304f-103">Prerequisites for standard costs</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="c304f-104">Þetta efnisatriði fjallar um grundvallarskref við notkun staðalkostnaðar.</span><span class="sxs-lookup"><span data-stu-id="c304f-104">This topic describes the basic steps for using standard costs.</span></span> <span data-ttu-id="c304f-105">Eftirfarandi skref fara eftir starfsemi fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="c304f-105">Subsequent steps depend on the company's operations.</span></span> <span data-ttu-id="c304f-106">Til dæmis eru skrefin mismunandi fyrir umhverfi sem er ekki með framleiðslu, framleiðsluumhverfi sem notar ekki leiðir og framleiðsluumhverfi sem notar leiðir.</span><span class="sxs-lookup"><span data-stu-id="c304f-106">For example, the steps differ for a nonmanufacturing environment, a manufacturing environment that doesn't use routings, and a manufacturing environment that uses routings.</span></span> 

<span data-ttu-id="c304f-107">Til að setja upp staðalkostnað skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="c304f-107">To set up standard costs, follow these steps.</span></span>

<span data-ttu-id="c304f-108">**1. Búa til vörulíkanaflokk fyrir staðalkostnað.**</span><span class="sxs-lookup"><span data-stu-id="c304f-108">**1. Create an item model group for standard costs.**</span></span>

<span data-ttu-id="c304f-109">Notaðu síðu **Vörulíkanaflokks** til að stofna nýjan flokk fyrir staðalkostnað og úthlutaðu birgðalíkani af **Staðalkostnaði**.</span><span class="sxs-lookup"><span data-stu-id="c304f-109">Use the **Item model groups** page to create a new group for standard costs, and assign an inventory model of **Standard cost**.</span></span> <span data-ttu-id="c304f-110">Kennimerki vörulíkanaflokksins ætti að hafa einhverja þýðingu, eins og **St.kostn.**.</span><span class="sxs-lookup"><span data-stu-id="c304f-110">The identifier for the item model group should be meaningful, such as **Std Cost**.</span></span> <span data-ttu-id="c304f-111">Veldu gátreitina til að gefa til kynna að flokkurinn eigi að leyfa fjárhagslegar neikvæðar birgðir og að hann eigi að bóka efnislegar birgðir og fjárhagslegar birgðir.</span><span class="sxs-lookup"><span data-stu-id="c304f-111">Select the check boxes to indicate that the group should allow financial negative inventory, and that it should post physical inventory and financial inventory.</span></span> <span data-ttu-id="c304f-112">Þessi flokkur staðalkostnaðar verður úthlutaður vörum.</span><span class="sxs-lookup"><span data-stu-id="c304f-112">This standard cost group will be assigned to items.</span></span>

<span data-ttu-id="c304f-113">**2. Skilgreina fjárhagslykla sem tengjast frávikum í staðalkostnaði.**</span><span class="sxs-lookup"><span data-stu-id="c304f-113">**2. Define ledger accounts that are related to standard cost variances.**</span></span> 

<span data-ttu-id="c304f-114">Notaðu síðuna **Bókhaldslyklar** til að skilgreina fjárhagslykla sem tengjast frávikum í staðalkostnaði.</span><span class="sxs-lookup"><span data-stu-id="c304f-114">Use the **Chart of accounts** page to define ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="c304f-115">Skilgreina þarf þessa fjárhagslykla áður en hægt er að úthluta þeim á síðu **Bókunar**.</span><span class="sxs-lookup"><span data-stu-id="c304f-115">These ledger accounts must be defined before they can be assigned on the **Posting** page.</span></span> <span data-ttu-id="c304f-116">Fjárhagslyklarnir geta endurspeglað vöruflokka og kostnaðarflokka.</span><span class="sxs-lookup"><span data-stu-id="c304f-116">The ledger accounts can reflect item groups and cost groups.</span></span>

<span data-ttu-id="c304f-117">**3. Úthluta fjárhagslyklum á vörubókanir sem tengjast frávikum í staðalkostnaði.**</span><span class="sxs-lookup"><span data-stu-id="c304f-117">**3. Assign ledger accounts to item postings that are related to standard cost variances.**</span></span> 

<span data-ttu-id="c304f-118">Notaðu síðu **Bókunar** til að úthluta fjárhagslyklum sem tengjast frávikum í staðalkostnaði.</span><span class="sxs-lookup"><span data-stu-id="c304f-118">Use the **Posting** page to assign the ledger accounts that are related to standard cost variances.</span></span> <span data-ttu-id="c304f-119">Þú getur tilgreint fjárhagslykil fráviks eftir vöru (eða vöruflokki) og eftir kostnaðarflokki (eða gerð kostnaðarflokks) eða þú getur tilgreint að fjárhagslykillinn eigi við um allar vörur og alla kostnaðarflokka.</span><span class="sxs-lookup"><span data-stu-id="c304f-119">You can specify a variance's ledger account by item (or item group) and by cost group (or cost group type), or you can specify that the ledger account applies to all items and all cost groups.</span></span> <span data-ttu-id="c304f-120">Þessir valkostir samsvara kostnaðartengslum fyrir töflur, flokka og allt.</span><span class="sxs-lookup"><span data-stu-id="c304f-120">These options correspond to cost relations for tables, groups, and all.</span></span> 

<span data-ttu-id="c304f-121">Áður en þú skilgreinir bókunarreglur á vörum skaltu nota síðuna **Færslusamsetningar** til að virkja kostnaðartengsl (fyrir töflur, flokka og allt).</span><span class="sxs-lookup"><span data-stu-id="c304f-121">Before you define the item posting rules, use the **Transaction combinations** page to enable cost relations (for tables, groups, and all).</span></span>

<span data-ttu-id="c304f-122">**4. Skilgreina birgðafæribreytur sem tengjast staðalkostnaði.**</span><span class="sxs-lookup"><span data-stu-id="c304f-122">**4. Define inventory parameters that are related to standard costs.**</span></span> 

-  <span data-ttu-id="c304f-123">Notaðu flipann **Uppskriftir** á síðunni **Birgðafæribreytur** til að skilgreina tvær kostnaðarstýrðar færibreytur sem tengjast staðalkostnaði.</span><span class="sxs-lookup"><span data-stu-id="c304f-123">Use the **Bills of materials** tab on the **Inventory parameters** page to define two cost control parameters that are related to standard costs.</span></span> 

    -  <span data-ttu-id="c304f-124">Í reitnum **Sundurliðun kostnaðar** veldu **Ekkert** eða **Undirfjárhag**.</span><span class="sxs-lookup"><span data-stu-id="c304f-124">In the **Cost breakdown** field, select **None** or **Sub ledger**.</span></span> <span data-ttu-id="c304f-125">Ef þú velur **Undirfjárhag** er sundurliðun kostnaðar *virk* sundurliðun kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="c304f-125">If you select **Sub ledger**, the cost breakdown is an *active* cost breakdown.</span></span> <span data-ttu-id="c304f-126">Virk sundurliðun kostnaðar er mikilvæg við útreikning, viðhald og yfirlit yfir sundurliðun kostnaðarflokka í margstiga uppbyggingu vöru fyrir staðalkostnaðarvörur.</span><span class="sxs-lookup"><span data-stu-id="c304f-126">An active cost breakdown is critical for calculating, retaining, and viewing cost group segmentation across a multilevel product structure for standard cost items.</span></span> <span data-ttu-id="c304f-127">Þegar sundurliðun kostnaðar er virk getur þú skráð og greint birgðir, verk í vinnslu (WIP) og kostnaður seldra vara (COGS) fyrir hvern kostnaðarflokk í einstiga, margstiga eða heildarsniði.</span><span class="sxs-lookup"><span data-stu-id="c304f-127">When the cost breakdown is active, you can report and analyze inventory, work in process (WIP), and cost of goods sold (COGS) per cost group in a single-level, multilevel, or total format.</span></span> <span data-ttu-id="c304f-128">Þegar sundurliðun kostnaðar er virk, ef þú virkjar kostnað framleiddra vara, verður sundurliðun kostnaðarflokka geymd í kostnaðarfærslu vörunnar.</span><span class="sxs-lookup"><span data-stu-id="c304f-128">When the cost breakdown is active, if you activate a manufactured item's cost, the cost group segmentation will be stored in the item's cost record.</span></span> 

    -  <span data-ttu-id="c304f-129">Ef þú velur **Ekkert** verður sundurliðun kostnaðarflokks ekki viðhaldið fyrir staðalkostnaðarvörur.</span><span class="sxs-lookup"><span data-stu-id="c304f-129">If you select **None**, cost group segmentation won't be maintained for standard cost items.</span></span> <span data-ttu-id="c304f-130">Með öðrum orðum, staðalkostnaður framleiddrar vöru verður reiknaður og honum viðhaldið sem einni upphæð, án sundurliðunar kostnaðarflokka.</span><span class="sxs-lookup"><span data-stu-id="c304f-130">In other words, a manufactured item's standard cost will be calculated and maintained as a single amount, without cost group segmentation.</span></span> <span data-ttu-id="c304f-131">Kostnaðarframlegð framleiddra hluta verður safnað saman í eina upphæð.</span><span class="sxs-lookup"><span data-stu-id="c304f-131">The cost contributions of manufactured components will be aggregated into the single amount.</span></span>

-  <span data-ttu-id="c304f-132">Í svæðinu **Frávik frá staðli** skaltu velja **Samantekt** eða **Fyrir hvern kostnaðarflokk**.</span><span class="sxs-lookup"><span data-stu-id="c304f-132">In the **Variances to standard** field, select **Summarized** or **Per cost group**.</span></span> <span data-ttu-id="c304f-133">Ef þú velur **Fyrir hvern kostnaðarflokk** getur þú greint frávik á innkaupaverði og frávik á framleiðslu eftir kostnaðarflokki.</span><span class="sxs-lookup"><span data-stu-id="c304f-133">If you select **Per cost group**, you can identify purchase price variances and production variances by cost group.</span></span> <span data-ttu-id="c304f-134">Þú getur einnig greint fjórar gerðir frávika á framleiðslu: lotustærð, magn, verð og staðgengilsfrávik.</span><span class="sxs-lookup"><span data-stu-id="c304f-134">You can also identify the four types of production variances: the lot size, quantity, price, and substitution variances.</span></span> <span data-ttu-id="c304f-135">Ef þú velur **Samantekt** getur þú ekki greint frávik eftir kostnaðarflokki og þú getur ekki greint fjórar gerðir frávika á framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="c304f-135">If you select **Summarized**, you can't identify variances by cost group, and you can't identify the four types of production variances.</span></span> <span data-ttu-id="c304f-136">Þú getur bara skoðað samantekt á frávikum framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="c304f-136">You can just view a summarized production variance.</span></span>

-  <span data-ttu-id="c304f-137">Reglan um frávik frá staðli virkar óháð reglunni um sundurliðun kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="c304f-137">The policy about variance to standard works independently of the cost breakdown policy.</span></span> <span data-ttu-id="c304f-138">Með öðrum orðum er hægt að velja **Ekkert** sem reglu fyrir sundurliðun kostnaðar og velja frávik fyrir hvern kostnaðarhóp, þannig að frávik framleiðslu eftir kostnaðarflokki verður áfram greint.</span><span class="sxs-lookup"><span data-stu-id="c304f-138">In other words, you can select a cost breakdown policy of **None** and select variances per cost group, so that production variances by cost group will still be captured.</span></span>

<span data-ttu-id="c304f-139">**5. Stofna kostnaðarútgáfur fyrir staðlalkostnað.**</span><span class="sxs-lookup"><span data-stu-id="c304f-139">**5. Create costing versions for standard costs.**</span></span> 

<span data-ttu-id="c304f-140">Notaðu síðuna **Uppsetningu kostnaðarútgáfu** til að stofna eina eða fleiri kostnaðarútgáfur fyrir staðalkostnað.</span><span class="sxs-lookup"><span data-stu-id="c304f-140">Use the **Costing version setup** page to create one or more costing versions for standard costs.</span></span> <span data-ttu-id="c304f-141">Úthluta þarf hverri kostnaðarútgáfu gerð kostnaðar sem **Staðalkostnað** og verður að leyfa efni að innihalda kostnaðargögn.</span><span class="sxs-lookup"><span data-stu-id="c304f-141">Each costing version must be designated by a costing type of **Standard cost** and must allow content to include cost data.</span></span>

<span data-ttu-id="c304f-142">**6. Undirbúa núverandi viðskiptavin til að nota staðalkostnað.**</span><span class="sxs-lookup"><span data-stu-id="c304f-142">**6. Prepare an existing customer to use standard costs.**</span></span> 

<span data-ttu-id="c304f-143">Viðskiptavinir sem vilja til að breyta núverandi vörum sínum yfir í birgðalíkan staðalkostnaðar verða að nota síðuna **Umreikningur á staðalkostnaði**.</span><span class="sxs-lookup"><span data-stu-id="c304f-143">Customers who want to change their existing items to a standard cost inventory model must use the **Standard cost conversions** page.</span></span>


<a name="related-topics"></a><span data-ttu-id="c304f-144">Tengd efnisatriði</span><span class="sxs-lookup"><span data-stu-id="c304f-144">Related topics</span></span>
--------

[<span data-ttu-id="c304f-145">Yfirlit yfir umreikning staðalkostnaðar</span><span class="sxs-lookup"><span data-stu-id="c304f-145">Standard cost conversion overview</span></span>](standard-cost-conversion-overview.md)


