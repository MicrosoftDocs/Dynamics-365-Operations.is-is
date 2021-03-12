---
title: Innkaupabeiðnir
description: Þetta efnisatriði lýsir því hvernig innkaupabeiðnir eru studdar í fínstillingu skipulagningar.
author: ChristianRytt
manager: tfehr
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2021-01-04
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: 8075f8d7c3868c6d6012edbce17dbbb4749209ab
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992345"
---
# <a name="purchase-requisitions"></a><span data-ttu-id="cce21-103">Innkaupabeiðnir</span><span class="sxs-lookup"><span data-stu-id="cce21-103">Purchase requisitions</span></span>

<span data-ttu-id="cce21-104">Aðaláætlanagerð getur fyllt á samþykktar innkaupabeiðnir.</span><span class="sxs-lookup"><span data-stu-id="cce21-104">Master planning can replenish approved purchase requisitions.</span></span> <span data-ttu-id="cce21-105">Til að ná yfir innkaupabeiðnir þurfa notendur þar af leiðandi ekki að nota verkflæði til að stofna innkaupapantanir.</span><span class="sxs-lookup"><span data-stu-id="cce21-105">Therefore, to cover purchase requisitions, users don't have to use a workflow to create purchase orders.</span></span> <span data-ttu-id="cce21-106">Þess í stað er getur aðaláætlanagerð dekkað innkaupabeiðnir.</span><span class="sxs-lookup"><span data-stu-id="cce21-106">Instead, purchase requisitions can be covered by master planning.</span></span> <span data-ttu-id="cce21-107">Vegna þessarar virkni getur innkaupabeiðni framleitt innkaupapöntun, flutningspöntun eða framleiðslupöntun, allt eftir gildinu fyrir **Gerð áætlaðrar pöntunar** sem er stillt fyrir tengda afurðina.</span><span class="sxs-lookup"><span data-stu-id="cce21-107">Because of this functionality, a purchase requisition can produce a purchase order, a transfer order, or a production order, depending on the **Planned order type** value that is set for the related product.</span></span>

## <a name="enable-master-plans-to-include-requisitions"></a><span data-ttu-id="cce21-108">Virkja aðaláætlanir til að hafa með beiðnir</span><span class="sxs-lookup"><span data-stu-id="cce21-108">Enable master plans to include requisitions</span></span>

<span data-ttu-id="cce21-109">Til að hafa með beiðnir við þekjuútreikning fyrir aðaláætlun skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="cce21-109">To include requisitions during the coverage calculation for a master plan, follow these steps.</span></span>

1. <span data-ttu-id="cce21-110">Farið í **Aðaláætlanagerð** \> **Uppsetning** \> **Áætlanir** \> **Aðaláætlanir**.</span><span class="sxs-lookup"><span data-stu-id="cce21-110">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="cce21-111">Stofnið eða veljið aðaláætlun.</span><span class="sxs-lookup"><span data-stu-id="cce21-111">Create or select a master plan.</span></span>
1. <span data-ttu-id="cce21-112">Í flýtiflipanum **Almennt** skal stilla valkostinn **Hafa með beiðnir** á *Já*.</span><span class="sxs-lookup"><span data-stu-id="cce21-112">On the **General** FastTab, set the **Include requisitions** option to *Yes*.</span></span>
1. <span data-ttu-id="cce21-113">Endurtakið skref 2 og 3 fyrir hverja aðaláætlun til viðbótar þar sem á að hafa með beiðnir.</span><span class="sxs-lookup"><span data-stu-id="cce21-113">Repeat steps 2 and 3 for each additional master plan where you want to include requisitions.</span></span>

## <a name="approved-requisitions-time-fence"></a><span data-ttu-id="cce21-114">Samþykkt tímamörk beiðna (dagar)</span><span class="sxs-lookup"><span data-stu-id="cce21-114">Approved requisitions time fence</span></span>

<span data-ttu-id="cce21-115">*Tímamörk samþykktra beiðna* ákveða hversu langt aftur (í dögum) aðaláætlun mun hafa með eftirspurn frá samþykktum áfyllingarbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="cce21-115">The *approved requisitions time fence* establishes how far back (in days) a master plan will include demand from approved replenishment requisitions.</span></span> <span data-ttu-id="cce21-116">Hægt er að stilla tímamörk samþykktra beiðna á bæði þekjuflokksstigi og aðaláætlunarstigi.</span><span class="sxs-lookup"><span data-stu-id="cce21-116">You can set an approved requisitions time fence at both the coverage group level and the master plan level.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-a-coverage-group"></a><span data-ttu-id="cce21-117">Stilla tímamörk samþykktra beiðna fyrir þekjuflokk</span><span class="sxs-lookup"><span data-stu-id="cce21-117">Set the approved requisitions time fence for a coverage group</span></span>

1. <span data-ttu-id="cce21-118">Fara skal í **Aðaláætlanagerð** \> **Uppsetning** \> **Þekja** \> **Þekjuflokkur**.</span><span class="sxs-lookup"><span data-stu-id="cce21-118">Go to **Master planning** \> **Setup** \> **Coverage** \> **Coverage group**.</span></span>
1. <span data-ttu-id="cce21-119">Stofnið eða veljið þekjuflokk.</span><span class="sxs-lookup"><span data-stu-id="cce21-119">Create or select a coverage group.</span></span>
1. <span data-ttu-id="cce21-120">Í flýtiflipanum **Annað** skal stilla reitinn **Tímamörk samþykktra beiðna (dagar)** á fjölda daga sem hafa á með í tímamörkunum.</span><span class="sxs-lookup"><span data-stu-id="cce21-120">On the **Other** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="cce21-121">Endurtakið skref 2 og 3 fyrir hvern þekjuflokk til viðbótar þar sem á að stilla tímamörk samþykktra beiðna.</span><span class="sxs-lookup"><span data-stu-id="cce21-121">Repeat steps 2 and 3 for each additional coverage group where you want to set an approved requisitions time fence.</span></span>

### <a name="set-the-approved-requisitions-time-fence-for-individual-master-plans"></a><span data-ttu-id="cce21-122">Stilla tímamörk samþykktra beiðna fyrir einstaka þekjuflokka</span><span class="sxs-lookup"><span data-stu-id="cce21-122">Set the approved requisitions time fence for individual master plans</span></span>

<span data-ttu-id="cce21-123">Þegar stillt eru tímamörk samþykktra beiðna fyrir staka aðaláætlun mun stillingin hnekkja stillingu tímamarka fyrir alla þekjuflokka sem eiga við.</span><span class="sxs-lookup"><span data-stu-id="cce21-123">When you set an approved requisitions time fence for an individual master plan, the setting overrides the time fence setting for any applicable coverage group.</span></span>

1. <span data-ttu-id="cce21-124">Farið í **Aðaláætlanagerð** \> **Uppsetning** \> **Áætlanir** \> **Aðaláætlanir**.</span><span class="sxs-lookup"><span data-stu-id="cce21-124">Go to **Master planning** \> **Setup** \> **Plans** \> **Master plans**.</span></span>
1. <span data-ttu-id="cce21-125">Stofnið eða veljið aðaláætlun.</span><span class="sxs-lookup"><span data-stu-id="cce21-125">Create or select a master plan.</span></span>
1. <span data-ttu-id="cce21-126">Í flýtiflipanum **Tímamörk í dögum** skal stilla reitinn **Tímamörk samþykktra beiðna (dagar)** á fjölda daga sem hafa á með í tímamörkunum.</span><span class="sxs-lookup"><span data-stu-id="cce21-126">On the **TIme fences in days** FastTab, set the **Approved requisitions time fence (days)** field to the number of days to include in the time fence.</span></span>
1. <span data-ttu-id="cce21-127">Endurtakið skref 2 og 3 fyrir hverja aðaláætlun til viðbótar þar sem á að stilla tímamörk samþykktra beiðna.</span><span class="sxs-lookup"><span data-stu-id="cce21-127">Repeat steps 2 and 3 for each additional master plan where you want to set an approved requisitions time fence.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cce21-128">**Væntanlegt:** Tímamörk samþykktra beiðna eru ekki enn studd fyrir fínstillingu skipulagningar.</span><span class="sxs-lookup"><span data-stu-id="cce21-128">**Coming soon:** Approved requisitions time fences aren't yet supported for Planning Optimization.</span></span> <span data-ttu-id="cce21-129">Þar til þau eru studd verða öll gildin hunsuð sem færð eru inn í reitinn **Tímamörk samþykktra beiðna (dagar)**.</span><span class="sxs-lookup"><span data-stu-id="cce21-129">Until they are supported, all values that you enter in the **Approved requisitions time fence (days)** field will be ignored.</span></span>

## <a name="independent-supply-regardless-of-coverage-code"></a><span data-ttu-id="cce21-130">Sjálfstætt framboð, óháð þekjukóða</span><span class="sxs-lookup"><span data-stu-id="cce21-130">Independent supply, regardless of coverage code</span></span>

<span data-ttu-id="cce21-131">Innkaupabeiðnir eru alltaf dekkaðar af sjálfstæðum áætluðum pöntunum burtséð frá því hver þekjukóðinn er.</span><span class="sxs-lookup"><span data-stu-id="cce21-131">Purchase requisitions are always covered by independent planned orders, regardless of the coverage code.</span></span> <span data-ttu-id="cce21-132">Þessi hegðun tryggir skýran rekjanleika og verkflæði á milli innkaupabeiðna og áfyllingarpantana.</span><span class="sxs-lookup"><span data-stu-id="cce21-132">This behavior ensures clear traceability and workflows between purchase requisitions and replenishment orders.</span></span>

### <a name="example-1"></a><span data-ttu-id="cce21-133">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="cce21-133">Example 1</span></span>

<span data-ttu-id="cce21-134">Afurð er sett upp þannig að hún sé með gildi fyrir **Þekjukóða** sem er *Lágm/hám*. Hún er með eftirfarandi birgða-og beiðnistöður:</span><span class="sxs-lookup"><span data-stu-id="cce21-134">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="cce21-135">Birgðamagn á lager = 10.</span><span class="sxs-lookup"><span data-stu-id="cce21-135">Inventory on-hand quantity = 10.</span></span>
- <span data-ttu-id="cce21-136">Lágmarksmagn birgða = 15.</span><span class="sxs-lookup"><span data-stu-id="cce21-136">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="cce21-137">Hámarksmagn birgða = 20.</span><span class="sxs-lookup"><span data-stu-id="cce21-137">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="cce21-138">Innkaupabeiðni fyrir eitt stykki er til.</span><span class="sxs-lookup"><span data-stu-id="cce21-138">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="cce21-139">Hún er með umbeðna dagsetningu fyrir daginn í dag.</span><span class="sxs-lookup"><span data-stu-id="cce21-139">It has a requested date of today.</span></span>

<span data-ttu-id="cce21-140">Þegar aðaláætlanagerð er keyrð eru tvær áætlaðar pantanir stofnaðar: eina fyrir 10 stykki til að fylla á birgðir upp í hámarksmagn og eina fyrir eitt stykki til að fylla á innkaupabeiðnina.</span><span class="sxs-lookup"><span data-stu-id="cce21-140">When master planning runs, two planned orders are created: one for 10 pieces to replenish inventory to the maximum quantity, and one for one piece to replenish the purchase requisition.</span></span>

### <a name="example-2"></a><span data-ttu-id="cce21-141">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="cce21-141">Example 2</span></span>

<span data-ttu-id="cce21-142">Afurð er sett upp þannig að hún sé með gildi fyrir **Þekjukóða** sem er *Lágm/hám*. Hún er með eftirfarandi birgða-og beiðnistöður:</span><span class="sxs-lookup"><span data-stu-id="cce21-142">A product is set up so that it has a **Coverage code** value of *Min/max*. It has the following inventory and requisition statuses:</span></span>

- <span data-ttu-id="cce21-143">Birgðamagn á lager = 17.</span><span class="sxs-lookup"><span data-stu-id="cce21-143">Inventory on-hand quantity = 17.</span></span>
- <span data-ttu-id="cce21-144">Lágmarksmagn birgða = 15.</span><span class="sxs-lookup"><span data-stu-id="cce21-144">Minimum inventory quantity = 15.</span></span>
- <span data-ttu-id="cce21-145">Hámarksmagn birgða = 20.</span><span class="sxs-lookup"><span data-stu-id="cce21-145">Maximum inventory quantity = 20.</span></span>
- <span data-ttu-id="cce21-146">Innkaupabeiðni fyrir eitt stykki er til.</span><span class="sxs-lookup"><span data-stu-id="cce21-146">A purchase requisition for one piece exists.</span></span> <span data-ttu-id="cce21-147">Hún er með umbeðna dagsetningu fyrir daginn í dag.</span><span class="sxs-lookup"><span data-stu-id="cce21-147">It has a requested date of today.</span></span>

<span data-ttu-id="cce21-148">Þegar aðaláætlanagerð er keyrð er ein áætluð pöntun fyrir eitt stykki stofnuð til að fylla á innkaupabeiðnina.</span><span class="sxs-lookup"><span data-stu-id="cce21-148">When master planning runs, one planned order for one piece is created to replenish the purchase requisition.</span></span>

### <a name="example-3"></a><span data-ttu-id="cce21-149">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="cce21-149">Example 3</span></span>

<span data-ttu-id="cce21-150">Afurð er sett upp þannig að hún sé með gildi fyrir **Þekjukóða** sem *Tímabil* og lengd tímabils upp á sjö daga.</span><span class="sxs-lookup"><span data-stu-id="cce21-150">A product is set up so that it has a **Coverage code** value of *Period* and a period length of seven days.</span></span> <span data-ttu-id="cce21-151">Hún er með eftirfarandi stöður á birgðum, sölupöntun og beiðni:</span><span class="sxs-lookup"><span data-stu-id="cce21-151">It has the following inventory, sales order, and requisition statuses:</span></span>

- <span data-ttu-id="cce21-152">Birgðamagn á lager = 0.</span><span class="sxs-lookup"><span data-stu-id="cce21-152">Inventory on-hand quantity = 0.</span></span>
- <span data-ttu-id="cce21-153">Sölupöntun fyrir fimm stykki er til.</span><span class="sxs-lookup"><span data-stu-id="cce21-153">A sales order for five pieces exists.</span></span> <span data-ttu-id="cce21-154">Hún er með væntanlega sendingardagsetningu fyrir daginn í dag plús einn dagur.</span><span class="sxs-lookup"><span data-stu-id="cce21-154">It has an expected ship date of today plus one day.</span></span>
- <span data-ttu-id="cce21-155">Innkaupabeiðni fyrir þrjú stykki er til.</span><span class="sxs-lookup"><span data-stu-id="cce21-155">A purchase requisition for three pieces exists.</span></span> <span data-ttu-id="cce21-156">Hún er með umbeðna dagsetningu fyrir daginn í dag plús þrír dagar.</span><span class="sxs-lookup"><span data-stu-id="cce21-156">It has a requested date of today plus three days.</span></span>

<span data-ttu-id="cce21-157">Þegar aðaláætlanagerð er keyrð eru tvær áætlaðar pantanir stofnaðar: ein fyrir þrjú stykki til að fylla á innkaupabeiðnina og eina fyrir fimm stykki til að fylla á eftirspurn sölupöntunar.</span><span class="sxs-lookup"><span data-stu-id="cce21-157">When master planning runs, two planned orders are created: one for three pieces to replenish the purchase requisition and one for five pieces to replenish sales order demand.</span></span>

> [!NOTE]
> <span data-ttu-id="cce21-158">Þegar áætluð pöntun sem er fest við innkaupabeiðni er staðfest heldur áætlunarvélin þarfarakningunni á innkaupabeiðninni.</span><span class="sxs-lookup"><span data-stu-id="cce21-158">After a planned order that is pegged to a purchase requisition is firmed, the planning engine keeps the pegging to the purchase requisition.</span></span> <span data-ttu-id="cce21-159">Ef kemur í ljós síðar að það vanti magn í staðfestu pöntunina sem þarf til að fylla á innkaupabeiðnina mun kerfið stofna nýja áætlaða pöntun sem nemur mismuninum.</span><span class="sxs-lookup"><span data-stu-id="cce21-159">If the firmed order is later found to be missing some quantity that is required to fulfill the purchase requisition, the system will create a new planned order for the difference.</span></span>

<span data-ttu-id="cce21-160">Frekari upplýsingar um innkaupabeiðnir er að finna í [Yfirlit innkaupabeiðna](../../procurement/purchase-requisitions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cce21-160">For more information about purchase requisitions, see [Purchase requisition overview](../../procurement/purchase-requisitions-overview.md).</span></span>
