---
title: Innkaupabeiðnir
description: Þetta efnisatriði lýsir því hvernig innkaupabeiðnir eru studdar í fínstillingu skipulagningar.
author: ChristianRytt
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqPlanSched, ReqGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 564f87fe78e79107feb103f953ed4769e4734aa1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808041"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="0643b-103">Innkaupabeiðnir</span><span class="sxs-lookup"><span data-stu-id="0643b-103">Purchase requisitions</span></span>

<span data-ttu-id="0643b-104">Aðaláætlanagerð getur fyllt á samþykktar innkaupabeiðnir.</span><span class="sxs-lookup"><span data-stu-id="0643b-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="0643b-105">Til að ná yfir innkaupabeiðnir þurfa notendur þar af leiðandi ekki að nota verkflæði til að stofna innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="0643b-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="0643b-106">Þess í stað er getur aðaláætlanagerð dekkað innkaupabeiðnir.</span><span class="sxs-lookup"><span data-stu-id="0643b-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="0643b-107">Vegna þessarar virkni getur innkaupabeiðni framleitt innkaupapöntun, flutningspöntun eða framleiðslupöntun, allt eftir gildinu fyrir **Gerð áætlaðrar pöntunar** sem er stillt fyrir tengda afurðina.</span><span class="sxs-lookup"><span data-stu-id="0643b-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="0643b-108">Virkja aðaláætlanir til að hafa með beiðnir</span><span class="sxs-lookup"><span data-stu-id="0643b-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="0643b-109">Til að hafa með beiðnir við þekjuútreikning fyrir aðaláætlun skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="0643b-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="0643b-110">Farið í **Aðaláætlanagerð** \> **Uppsetning** \> **Áætlanir** \> **Aðaláætlanir**.</span><span class="sxs-lookup"><span data-stu-id="0643b-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="0643b-111">Stofnið eða veljið aðaláætlun.</span><span class="sxs-lookup"><span data-stu-id="0643b-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="0643b-112">Í flýtiflipanum **Almennt** skal stilla valkostinn **Hafa með beiðnir** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="0643b-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="0643b-113">Endurtakið skref 2 og 3 fyrir hverja aðaláætlun til viðbótar þar sem á að hafa með beiðnir.</span><span class="sxs-lookup"><span data-stu-id="0643b-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="0643b-114">Samþykkt tímamörk beiðna (dagar)</span><span class="sxs-lookup"><span data-stu-id="0643b-114">Approved requisitions time fence</span></span>

<span data-ttu-id="0643b-115">*Tímamörk samþykktra beiðna* ákveða hversu langt aftur (í dögum) aðaláætlun mun hafa með eftirspurn frá samþykktum áfyllingarbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="0643b-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="0643b-116">Hægt er að stilla tímamörk samþykktra beiðna á bæði þekjuflokksstigi og aðaláætlunarstigi.</span><span class="sxs-lookup"><span data-stu-id="0643b-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="0643b-117">Stilla tímamörk samþykktra beiðna fyrir þekjuflokk</span><span class="sxs-lookup"><span data-stu-id="0643b-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="0643b-118">Fara skal í **Aðaláætlanagerð** \> **Uppsetning** \> **Þekja** \> **Þekjuflokkar**.</span><span class="sxs-lookup"><span data-stu-id="0643b-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage groups**.</span></span>
1. <span data-ttu-id="0643b-119">Stofnið eða veljið þekjuflokk.</span><span class="sxs-lookup"><span data-stu-id="0643b-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="0643b-120">Í flýtiflipanum **Annað** skal stilla reitinn **Tímamörk samþykktra beiðna (dagar)** á fjölda daga sem hafa á með í tímamörkunum.</span><span class="sxs-lookup"><span data-stu-id="0643b-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="0643b-121">Endurtakið skref 2 og 3 fyrir hvern þekjuflokk til viðbótar þar sem á að stilla tímamörk samþykktra beiðna.</span><span class="sxs-lookup"><span data-stu-id="0643b-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="0643b-122">Stilla tímamörk samþykktra beiðna fyrir einstaka þekjuflokka</span><span class="sxs-lookup"><span data-stu-id="0643b-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="0643b-123">Þegar stillt eru tímamörk samþykktra beiðna fyrir staka aðaláætlun mun stillingin hnekkja stillingu tímamarka fyrir alla þekjuflokka sem eiga við.</span><span class="sxs-lookup"><span data-stu-id="0643b-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="0643b-124">Farið í **Aðaláætlanagerð** \> **Uppsetning** \> **Áætlanir** \> **Aðaláætlanir**.</span><span class="sxs-lookup"><span data-stu-id="0643b-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="0643b-125">Stofnið eða veljið aðaláætlun.</span><span class="sxs-lookup"><span data-stu-id="0643b-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="0643b-126">Í flýtiflipanum **Tímamörk í dögum** skal stilla reitinn **Tímamörk samþykktra beiðna (dagar)** á fjölda daga sem hafa á með í tímamörkunum.</span><span class="sxs-lookup"><span data-stu-id="0643b-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="0643b-127">Endurtakið skref 2 og 3 fyrir hverja aðaláætlun til viðbótar þar sem á að stilla tímamörk samþykktra beiðna.</span><span class="sxs-lookup"><span data-stu-id="0643b-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0643b-128">**Væntanlegt:** Tímamörk samþykktra beiðna eru ekki enn studd fyrir fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="0643b-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="0643b-129">Þar til þau eru studd verða öll gildin hunsuð sem færð eru inn í reitinn **Tímamörk samþykktra beiðna (dagar)**.</span><span class="sxs-lookup"><span data-stu-id="0643b-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="0643b-130">Sjálfstætt framboð, óháð þekjukóða</span><span class="sxs-lookup"><span data-stu-id="0643b-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="0643b-131">Innkaupabeiðnir eru alltaf dekkaðar af sjálfstæðum áætluðum pöntunum burtséð frá því hver þekjukóðinn er.</span><span class="sxs-lookup"><span data-stu-id="0643b-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="0643b-132">Þessi hegðun tryggir skýran rekjanleika og verkflæði á milli innkaupabeiðna og áfyllingarpantana.</span><span class="sxs-lookup"><span data-stu-id="0643b-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="0643b-133">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="0643b-133">Example 1</span></span>

<span data-ttu-id="0643b-134">Afurð er sett upp þannig að hún sé með gildi fyrir **Þekjukóða** sem er *Lágm/hám*. Hún er með eftirfarandi birgða-og beiðnistöður:</span><span class="sxs-lookup"><span data-stu-id="0643b-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="0643b-135">Birgðamagn á lager = 10.</span><span class="sxs-lookup"><span data-stu-id="0643b-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="0643b-136">Lágmarksmagn birgða = 15.</span><span class="sxs-lookup"><span data-stu-id="0643b-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="0643b-137">Hámarksmagn birgða = 20.</span><span class="sxs-lookup"><span data-stu-id="0643b-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="0643b-138">Innkaupabeiðni fyrir eitt stykki er til.</span><span class="sxs-lookup"><span data-stu-id="0643b-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="0643b-139">Hún er með umbeðna dagsetningu fyrir daginn í dag.</span><span class="sxs-lookup"><span data-stu-id="0643b-139">It has a requested date of today.</span></span>

<span data-ttu-id="0643b-140">Þegar aðaláætlanagerð er keyrð eru tvær áætlaðar pantanir stofnaðar: eina fyrir 10 stykki til að fylla á birgðir upp í hámarksmagn og eina fyrir eitt stykki til að fylla á innkaupabeiðnina.</span><span class="sxs-lookup"><span data-stu-id="0643b-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="0643b-141">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="0643b-141">Example 2</span></span>

<span data-ttu-id="0643b-142">Afurð er sett upp þannig að hún sé með gildi fyrir **Þekjukóða** sem er *Lágm/hám*. Hún er með eftirfarandi birgða-og beiðnistöður:</span><span class="sxs-lookup"><span data-stu-id="0643b-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="0643b-143">Birgðamagn á lager = 17.</span><span class="sxs-lookup"><span data-stu-id="0643b-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="0643b-144">Lágmarksmagn birgða = 15.</span><span class="sxs-lookup"><span data-stu-id="0643b-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="0643b-145">Hámarksmagn birgða = 20.</span><span class="sxs-lookup"><span data-stu-id="0643b-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="0643b-146">Innkaupabeiðni fyrir eitt stykki er til.</span><span class="sxs-lookup"><span data-stu-id="0643b-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="0643b-147">Hún er með umbeðna dagsetningu fyrir daginn í dag.</span><span class="sxs-lookup"><span data-stu-id="0643b-147">It has a requested date of today.</span></span>

<span data-ttu-id="0643b-148">Þegar aðaláætlanagerð er keyrð er ein áætluð pöntun fyrir eitt stykki stofnuð til að fylla á innkaupabeiðnina.</span><span class="sxs-lookup"><span data-stu-id="0643b-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="0643b-149">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="0643b-149">Example 3</span></span>

<span data-ttu-id="0643b-150">Afurð er sett upp þannig að hún sé með gildi fyrir **Þekjukóða** sem *Tímabil* og lengd tímabils upp á sjö daga.</span><span class="sxs-lookup"><span data-stu-id="0643b-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="0643b-151">Hún er með eftirfarandi stöður á birgðum, sölupöntun og beiðni:</span><span class="sxs-lookup"><span data-stu-id="0643b-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="0643b-152">Birgðamagn á lager = 0.</span><span class="sxs-lookup"><span data-stu-id="0643b-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="0643b-153">Sölupöntun fyrir fimm stykki er til.</span><span class="sxs-lookup"><span data-stu-id="0643b-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="0643b-154">Hún er með væntanlega sendingardagsetningu fyrir daginn í dag plús einn dagur.</span><span class="sxs-lookup"><span data-stu-id="0643b-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="0643b-155">Innkaupabeiðni fyrir þrjú stykki er til.</span><span class="sxs-lookup"><span data-stu-id="0643b-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="0643b-156">Hún er með umbeðna dagsetningu fyrir daginn í dag plús þrír dagar.</span><span class="sxs-lookup"><span data-stu-id="0643b-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="0643b-157">Þegar aðaláætlanagerð er keyrð eru tvær áætlaðar pantanir stofnaðar: ein fyrir þrjú stykki til að fylla á innkaupabeiðnina og eina fyrir fimm stykki til að fylla á eftirspurn sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="0643b-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="0643b-158">Þegar áætluð pöntun sem er fest við innkaupabeiðni er staðfest heldur áætlunarvélin þarfarakningunni á innkaupabeiðninni.</span><span class="sxs-lookup"><span data-stu-id="0643b-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="0643b-159">Ef kemur í ljós síðar að það vanti magn í staðfestu pöntunina sem þarf til að fylla á innkaupabeiðnina mun kerfið stofna nýja áætlaða pöntun sem nemur mismuninum.</span><span class="sxs-lookup"><span data-stu-id="0643b-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="0643b-160">Frekari upplýsingar um innkaupabeiðnir er að finna í [Yfirlit innkaupabeiðna](../../procurement/purchase-requisitions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0643b-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]