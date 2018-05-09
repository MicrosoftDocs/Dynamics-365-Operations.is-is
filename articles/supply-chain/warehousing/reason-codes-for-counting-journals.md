---
title: "Ástæðukóðar fyrir birgðatalningu"
description: "Í þessu efnisatriði er því lýst hvernig eigi að setja upp og innleiða ástæðukóðum fyrir talningarverk."
author: Mirzaab
manager: AnnBe
ms.date: 03/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventCountingReasonCodePolicy
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0d787dac50374af11d878652103145c9ae9b6877
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="reason-codes-for-inventory-counting"></a><span data-ttu-id="2a02f-103">Ástæðukóðar fyrir birgðatalningu</span><span class="sxs-lookup"><span data-stu-id="2a02f-103">Reason codes for inventory counting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a02f-104">Ástæðukóðar gera þér kleift að greina niðurstöður talningarferlis og hvers kyns misræmi sem á sér stað í því ferli.</span><span class="sxs-lookup"><span data-stu-id="2a02f-104">Reason codes let you analyze the results of a counting process and any discrepancies that occur during that process.</span></span> <span data-ttu-id="2a02f-105">Hægt er að tilgreina ástæðuna fyrir því að gera talningu, t.d. brotið bretti eða lagerleiðrétting sem byggist á sýnishornum birgða.</span><span class="sxs-lookup"><span data-stu-id="2a02f-105">You can specify the reason for doing the count, such as a broken pallet or a stock adjustment that is based on inventory samples.</span></span>

## <a name="recommendation"></a><span data-ttu-id="2a02f-106">Ráðleggingar</span><span class="sxs-lookup"><span data-stu-id="2a02f-106">Recommendation</span></span>

<span data-ttu-id="2a02f-107">Áður en kerfið er sett upp er mælt með því að skilgreina áætlun til að vinna með ástæðukóðum.</span><span class="sxs-lookup"><span data-stu-id="2a02f-107">Before you set up the system, we recommend that you define a strategy for working with reason codes.</span></span> <span data-ttu-id="2a02f-108">Reyndu til dæmis að svara eftirfarandi spurningum:</span><span class="sxs-lookup"><span data-stu-id="2a02f-108">For example, try to answer the following questions:</span></span>

- <span data-ttu-id="2a02f-109">Eiga ástæðukóðar að vera áskildir í vöruhúsum?</span><span class="sxs-lookup"><span data-stu-id="2a02f-109">Should reason codes be mandatory on warehouses?</span></span>
- <span data-ttu-id="2a02f-110">Eiga ástæðukóðar að vera áskildir eða valfrjálsir á sumum vörum?</span><span class="sxs-lookup"><span data-stu-id="2a02f-110">Should reason codes be mandatory or optional on some items?</span></span>
- <span data-ttu-id="2a02f-111">Hversu marga ástæðukóða þarftu á að halda?</span><span class="sxs-lookup"><span data-stu-id="2a02f-111">How many reason codes do you require?</span></span>
- <span data-ttu-id="2a02f-112">Hvernig eiga notendur strikamerkjaskanna að nota ástæðukóða?</span><span class="sxs-lookup"><span data-stu-id="2a02f-112">How should users of barcode scanners use reason codes?</span></span> <span data-ttu-id="2a02f-113">Eiga ástæðukóðarnir að vera forvaldir, áskildir eða óbreytanlegir?</span><span class="sxs-lookup"><span data-stu-id="2a02f-113">Should the reason codes be preselected, mandatory, or not editable?</span></span>
- <span data-ttu-id="2a02f-114">Þurfa starfskraftar í vöruhúsi öðruvísi tilhögun á ástæðukóðum fyrir farsímaskanna?</span><span class="sxs-lookup"><span data-stu-id="2a02f-114">Do warehouse workers require different reason code behavior on mobile scanners?</span></span> <span data-ttu-id="2a02f-115">Ef svarið er já, er hægt að búa til fleiri valmyndaratriði og úthluta þeim á mismunandi fólk.</span><span class="sxs-lookup"><span data-stu-id="2a02f-115">If the answer is yes, you can create more menu items and assign them to different people.</span></span>

## <a name="where-reason-codes-apply"></a><span data-ttu-id="2a02f-116">Þar sem ástæðukóðar eiga við</span><span class="sxs-lookup"><span data-stu-id="2a02f-116">Where reason codes apply</span></span>

<span data-ttu-id="2a02f-117">Hægt er að búa til margar reglur ástæðukóða og hver regla ástæðukóða getur haft tvær reglur fyrir ástæðukóða talningar.</span><span class="sxs-lookup"><span data-stu-id="2a02f-117">You can create multiple reason code policies, and each reason code policy can have two counting reason code policies.</span></span> <span data-ttu-id="2a02f-118">Reglur ástæðukóða talningar er hægt að nota á stigi vöruhúss eða stigi vöru.</span><span class="sxs-lookup"><span data-stu-id="2a02f-118">The counting reason code policies can be used at the warehouse level or the item level.</span></span>

## <a name="set-up-reason-code-policies"></a><span data-ttu-id="2a02f-119">Setja upp reglur ástæðukóða</span><span class="sxs-lookup"><span data-stu-id="2a02f-119">Set up reason code policies</span></span>

1. <span data-ttu-id="2a02f-120">Veldu **Birgðastjórnun** \> **Uppsetning** \> **Birgðir** \> **Reglur ástæðukóða talningar** og búðu til nýja reglu ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="2a02f-120">Select **Inventory management** \> **Setup** \> **Inventory** \> **Counting reason code policies**, and create a new reason code policy.</span></span>
2. <span data-ttu-id="2a02f-121">Í reitnum **Gerð ástæðukóða talningar** skal velja annaðhvort **Áskilið** eða **Valfrjálst** til að tilgreina hvort val á ástæðukóða eigi að vera valfrjáls eða áskilin aðgerð í einni af eftirfarandi talningarbókum:</span><span class="sxs-lookup"><span data-stu-id="2a02f-121">In the **Counting reason code type** field, select either **Mandatory** or **Optional** to specify whether selection of a reason code should be an optional or mandatory action in one of the following counting journals:</span></span>

    - <span data-ttu-id="2a02f-122">Regluleg talning (fartæki)</span><span class="sxs-lookup"><span data-stu-id="2a02f-122">Cycle Count (mobile device)</span></span>
    - <span data-ttu-id="2a02f-123">Stundartalning (fartæki)</span><span class="sxs-lookup"><span data-stu-id="2a02f-123">Spot Count (mobile device)</span></span>
    - <span data-ttu-id="2a02f-124">Þröskuldstalning (fartæki)</span><span class="sxs-lookup"><span data-stu-id="2a02f-124">Threshold Count (mobile device)</span></span>
    - <span data-ttu-id="2a02f-125">Leiðrétting inn (fartæki)</span><span class="sxs-lookup"><span data-stu-id="2a02f-125">Adjustment In (mobile device)</span></span>
    - <span data-ttu-id="2a02f-126">Leiðrétting út (fartæki)</span><span class="sxs-lookup"><span data-stu-id="2a02f-126">Adjustment Out (mobile device)</span></span>
    - <span data-ttu-id="2a02f-127">Talningarbók (þungbiðlari)</span><span class="sxs-lookup"><span data-stu-id="2a02f-127">Counting Journal (rich client)</span></span>

<span data-ttu-id="2a02f-128">Einnig er hægt að setja upp ástæðukóða fyrir einstök vöruhús og afurðir.</span><span class="sxs-lookup"><span data-stu-id="2a02f-128">You can also set up reason codes for individual warehouses and for products.</span></span> <span data-ttu-id="2a02f-129">Uppsetning ástæðukóða fyrir afurðir getur hunsað uppsetningu fyrir vöruhús.</span><span class="sxs-lookup"><span data-stu-id="2a02f-129">The reason code setup for products can disregard the setup for warehouses.</span></span>

## <a name="mandatory-reason-codes"></a><span data-ttu-id="2a02f-130">Áskildir ástæðukóðar</span><span class="sxs-lookup"><span data-stu-id="2a02f-130">Mandatory reason codes</span></span>

<span data-ttu-id="2a02f-131">Ef færibreytan **Áskilið** er stillt í skilgreiningu ástæðukóða fyrir vöruhús eða vörur, er ekki hægt að ljúka og loka talningarbókinni fyrr en ástæðukóði hefur verið útvegaður.</span><span class="sxs-lookup"><span data-stu-id="2a02f-131">If the **Mandatory** parameter is set in the configuration of reason codes for warehouses or items, the counting journal can't be completed and closed until a reason code is provided.</span></span>

### <a name="set-up-reason-codes-for-warehouses"></a><span data-ttu-id="2a02f-132">Setja upp ástæðukóða fyrir vöruhús</span><span class="sxs-lookup"><span data-stu-id="2a02f-132">Set up reason codes for warehouses</span></span>

1. <span data-ttu-id="2a02f-133">Veldu **Birgðastjórnun** \> **Uppsetning** \> **Birgðasundurliðun** \> **Vöruhús**.</span><span class="sxs-lookup"><span data-stu-id="2a02f-133">Select **Inventory Management** \> **Setup** \> **Inventory breakdown** \> **Warehouses**.</span></span>
2. <span data-ttu-id="2a02f-134">Í flipanum **Vöruhús**, í reitnum **Regla ástæðukóða talningar** skal velja einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="2a02f-134">On the **Warehouse** tab, in the **Counting reason code policy** field, select one of the following options:</span></span>

    - <span data-ttu-id="2a02f-135">**Autt** - Færibreyta sem er sett upp fyrir vöru er notuð til að ákvarða hvort talningarbækur séu áskildar fyrir afurðina.</span><span class="sxs-lookup"><span data-stu-id="2a02f-135">**Blank** – The parameter that is set up for the item is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="2a02f-136">**Áskilið** - Ástæðukóða er alltaf krafist fyrir talningarbækur vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="2a02f-136">**Mandatory** – A reason code is always required on counting journals for the warehouse.</span></span>
    - <span data-ttu-id="2a02f-137">**Valfrjálst** - Ástæðukóða er ekki krafist fyrir talningarbækur vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="2a02f-137">**Optional** – A reason code isn't required on counting journals for the warehouse.</span></span>

### <a name="set-up-reason-codes-for-products"></a><span data-ttu-id="2a02f-138">Setja upp ástæðukóða fyrir afurðir</span><span class="sxs-lookup"><span data-stu-id="2a02f-138">Set up reason codes for products</span></span>

1. <span data-ttu-id="2a02f-139">Veldu **Upplýsingastjórnun afurða** \> **Afurðir** \> **Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="2a02f-139">Select **Product information management** \> **Products** \> **Released products**.</span></span>
2. <span data-ttu-id="2a02f-140">Á flipanum **Afurðir** skal velja **Regla ástæðukóða talningar** og síðan velja einn af eftirfarandi valkostum:</span><span class="sxs-lookup"><span data-stu-id="2a02f-140">On the **Product** tab, select **Counting reason code policy**, and then select one of the following options:</span></span>

    - <span data-ttu-id="2a02f-141">**Autt** - Færibreyta sem er sett upp fyrir vöruhús er notuð til að ákvarða hvort talningarbækur séu áskildar fyrir afurðina.</span><span class="sxs-lookup"><span data-stu-id="2a02f-141">**Blank** – The parameter that is set up for the warehouse is used to determine whether counting journals are mandatory for the product.</span></span>
    - <span data-ttu-id="2a02f-142">**Áskilið** - Ástæðukóða er alltaf krafist fyrir talningarbækur afurðar.</span><span class="sxs-lookup"><span data-stu-id="2a02f-142">**Mandatory** – A reason code is always required on counting journals for the product.</span></span> <span data-ttu-id="2a02f-143">Þessi stilling hnekkir öllum stillingum ástæðukóða á stigi vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="2a02f-143">This setting overrides any reason code setting at the warehouse level.</span></span>
    - <span data-ttu-id="2a02f-144">**Valfrjálst** - Ástæðukóða er ekki krafist fyrir talningarbækur afurðar.</span><span class="sxs-lookup"><span data-stu-id="2a02f-144">**Optional** – A reason code isn't required on counting journals for the product.</span></span> <span data-ttu-id="2a02f-145">Þessi stilling hnekkir öllum stillingum ástæðukóða á stigi vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="2a02f-145">This setting overrides any reason code setting at the warehouse level.</span></span>

### <a name="use-reason-codes-in-counting-journals"></a><span data-ttu-id="2a02f-146">Nota ástæðukóða í talningarbókum</span><span class="sxs-lookup"><span data-stu-id="2a02f-146">Use reason codes in counting journals</span></span>

<span data-ttu-id="2a02f-147">Í talningarbókum er hægt að bæta við ástæðukóðum fyrir talningar af eftirfarandi gerðum:</span><span class="sxs-lookup"><span data-stu-id="2a02f-147">In a counting journal, you can add reason codes for counts of the following types:</span></span>

- <span data-ttu-id="2a02f-148">Regluleg talning</span><span class="sxs-lookup"><span data-stu-id="2a02f-148">Cycle Count</span></span>
- <span data-ttu-id="2a02f-149">Stundartalning</span><span class="sxs-lookup"><span data-stu-id="2a02f-149">Spot Count</span></span>
- <span data-ttu-id="2a02f-150">Þröskuldstalning</span><span class="sxs-lookup"><span data-stu-id="2a02f-150">Threshold Count</span></span>
- <span data-ttu-id="2a02f-151">Leiðrétting inn</span><span class="sxs-lookup"><span data-stu-id="2a02f-151">Adjustment In</span></span>
- <span data-ttu-id="2a02f-152">Leiðrétting út</span><span class="sxs-lookup"><span data-stu-id="2a02f-152">Adjustment Out</span></span>

<span data-ttu-id="2a02f-153">Ástæðukóðum er bætt við færslubókarlínur í talningarbókum af gerðinni **Talningarbók**.</span><span class="sxs-lookup"><span data-stu-id="2a02f-153">Reason codes are added to the journal lines in counting journals of the **Counting journal** type.</span></span>

1. <span data-ttu-id="2a02f-154">Veldu **Birgðastjórnun** \> **Færslubókarfærslur** \> **Vörutalning** \> **Talning**.</span><span class="sxs-lookup"><span data-stu-id="2a02f-154">Select **Inventory management** \> **Journal entries** \> **Item counting** \> **Counting**.</span></span>
2. <span data-ttu-id="2a02f-155">Í línuupplýsingum talningarbókar, í reitnum **Ástæðukóði talningar** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="2a02f-155">In the line details of the counting journal, in the **Counting reason code** field, select an option.</span></span>

### <a name="view-the-counting-history-as-its-recorded-by-reason-codes"></a><span data-ttu-id="2a02f-156">Skoðaðu talningarferilinn eins og hann er skráður af ástæðukóðum</span><span class="sxs-lookup"><span data-stu-id="2a02f-156">View the counting history as it's recorded by reason codes</span></span>

- <span data-ttu-id="2a02f-157">Veldu **Birgðastjórnun** \> **Fyrirspurnir og skýrslur** \> **Talningarferill** og síðan í reitnum **Ástæðukóði talningar** skaltu skoða talningarferilinn sem hefur verið skráður í gegnum ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="2a02f-157">Select **Inventory management** \> **Inquiries and reports** \> **Counting history**, and then, in the **Counting reason code** field, view the counting history that has been recorded through a reason code.</span></span>

### <a name="use-a-reason-code-for-a-quantity-adjustment"></a><span data-ttu-id="2a02f-158">Notaðu ástæðukóða fyrir magnleiðréttingu</span><span class="sxs-lookup"><span data-stu-id="2a02f-158">Use a reason code for a quantity adjustment</span></span>

1. <span data-ttu-id="2a02f-159">Á síðunni **Lagerbirgðir** skal velja **Leiðrétta magn**.</span><span class="sxs-lookup"><span data-stu-id="2a02f-159">On the **On-hand inventory** page, select **Adjust quantity**.</span></span> <span data-ttu-id="2a02f-160">Hægt er að opna síðuna **Lagerbirgðir** á nokkra vegu.</span><span class="sxs-lookup"><span data-stu-id="2a02f-160">You can open the **On-hand inventory** page in several ways.</span></span> <span data-ttu-id="2a02f-161">Veldu til dæmis **Birgðastjórnun** \> **Fyrirspurnir og skýrslur** \> **Lagerbirgðir**.</span><span class="sxs-lookup"><span data-stu-id="2a02f-161">For example, select **Inventory management** \> **Inquiries and reports** \> **On-hand inventory**.</span></span>
2. <span data-ttu-id="2a02f-162">Veldu **Leiðrétta magn** og síðan í reitnum **Ástæðukóði talningar** skal velja ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="2a02f-162">Select **Adjust quantity**, and then, in the **Counting reason code** field, select a reason code.</span></span>

### <a name="configure-reason-codes-for-mobile-device-menu-items"></a><span data-ttu-id="2a02f-163">Skilgreina ástæðukóða fyrir valmyndaratriði fartækis</span><span class="sxs-lookup"><span data-stu-id="2a02f-163">Configure reason codes for mobile device menu items</span></span>

<span data-ttu-id="2a02f-164">Hægt er að skilgreina ástæðukóða fyrir hvaða talningargerð sem er í valmyndaratriði fartækis.</span><span class="sxs-lookup"><span data-stu-id="2a02f-164">You can configure reason codes for any type of count on a mobile device menu item.</span></span> <span data-ttu-id="2a02f-165">Uppsetning valmyndaratriðis fartækis inniheldur eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="2a02f-165">The configuration of the mobile device menu item includes the following information:</span></span>

- <span data-ttu-id="2a02f-166">Hvort ástæðukóðinn sjáist fyrir starfskraft fartækis meðan á talningu stendur.</span><span class="sxs-lookup"><span data-stu-id="2a02f-166">Whether the reason code is shown to the mobile device worker during counting.</span></span>
- <span data-ttu-id="2a02f-167">Sjálfgefni ástæðukóðinn sem er sýndur í valmyndaratriði fartækis.</span><span class="sxs-lookup"><span data-stu-id="2a02f-167">The default reason code that is shown on a mobile device menu item.</span></span>
- <span data-ttu-id="2a02f-168">Hvort notandi geti breytt ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="2a02f-168">Whether the user can edit the reason code.</span></span>

### <a name="set-up-reason-codes-on-a-mobile-device"></a><span data-ttu-id="2a02f-169">Setja upp ástæðukóða á fartæki</span><span class="sxs-lookup"><span data-stu-id="2a02f-169">Set up reason codes on a mobile device</span></span>

1. <span data-ttu-id="2a02f-170">Veldu **Vöruhúsakerfi** \> **Uppsetning** \> **Fartæki** \> **Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="2a02f-170">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="2a02f-171">Í flipanum **Regluleg talning** skal velja **Regluleg talning**.</span><span class="sxs-lookup"><span data-stu-id="2a02f-171">On the **Cycle count** tab, select **Cycle counting**.</span></span>
3. <span data-ttu-id="2a02f-172">Í reitnum **Sjálfgefinn ástæðukóði talningar** skal stilla sjálfgefinn ástæðukóða sem á að skrá þegar talning er gerð með því að nota valmyndaratriði fartækis.</span><span class="sxs-lookup"><span data-stu-id="2a02f-172">In the **Default counting reason code** field, set the default reason code that should be recorded when counting is done by using the mobile device menu item.</span></span>
4. <span data-ttu-id="2a02f-173">Í reitnum **Birta ástæðukóða talningar** skal velja **Lína** til að sýna ástæðukóða eftir að hvert frávik er skráð.</span><span class="sxs-lookup"><span data-stu-id="2a02f-173">In the **Display counting reason code** field, select **Line** to show the reason code after each variance is recorded.</span></span> <span data-ttu-id="2a02f-174">Að öðrum kosti skal velja **Fela** ef ekki á að sýna ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="2a02f-174">Alternatively, select **Hide** if the reason code shouldn't be shown.</span></span>
5. <span data-ttu-id="2a02f-175">Stilltu valkostinn **Breyta ástæðukóða talningar** á annaðhvort **Já** eða **Nei**.</span><span class="sxs-lookup"><span data-stu-id="2a02f-175">Set the **Edit counting reason code** option to either **Yes** or **No**.</span></span> <span data-ttu-id="2a02f-176">Ef þú stillir valkostinn á **Já** getur starfskraftur breytt ástæðukóða þegar hann er sýndur á fartækinu meðan á talningu stendur.</span><span class="sxs-lookup"><span data-stu-id="2a02f-176">If you set this option to **Yes**, the worker can edit the reason code when it's shown on the mobile device during counting.</span></span>

> [!NOTE]
> <span data-ttu-id="2a02f-177">Hægt er að virkja hnappinn **Regluleg talning** á valmyndaratriði hvaða fartækis sem er þar sem talning getur farið fram.</span><span class="sxs-lookup"><span data-stu-id="2a02f-177">The **Cycle counting** button can be enabled on any mobile device menu item where counting can be done.</span></span> <span data-ttu-id="2a02f-178">Dæmi um það eru valmyndaratriðin fyrir stundartalningar, notendastýrð verk og kerfisstýrð verk.</span><span class="sxs-lookup"><span data-stu-id="2a02f-178">Example include the menu items for spot counts, user-directed work, and system-directed work.</span></span>

## <a name="cycle-count-approvals"></a><span data-ttu-id="2a02f-179">Samþykki reglulegrar talningar</span><span class="sxs-lookup"><span data-stu-id="2a02f-179">Cycle count approvals</span></span>

<span data-ttu-id="2a02f-180">Áður en talning er samþykkt getur notandi breytt ástæðukóðanum sem tengist talningunni.</span><span class="sxs-lookup"><span data-stu-id="2a02f-180">Before a count is approved, the user can change the reason code that is associated with the count.</span></span> <span data-ttu-id="2a02f-181">Þegar talning er samþykkt er ástæðukóði sleginn inn í línu talningarbókar.</span><span class="sxs-lookup"><span data-stu-id="2a02f-181">When the count is approved, the reason code is entered on the counting journal lines.</span></span>

### <a name="modify-cycle-count-approvals"></a><span data-ttu-id="2a02f-182">Breyta samþykki reglulegrar talningar</span><span class="sxs-lookup"><span data-stu-id="2a02f-182">Modify cycle count approvals</span></span>

1. <span data-ttu-id="2a02f-183">Veldu **Vöruhúsakerfi** \> **Regluleg talning** \> **Verk reglulegrar talningar bíður yfirferðar**.</span><span class="sxs-lookup"><span data-stu-id="2a02f-183">Select **Warehouse management** \> **Cycle counting** \> **Cycle count work pending review**.</span></span>
2. <span data-ttu-id="2a02f-184">Veldu **Regluleg talning** og síðan í reitnum **Ástæðukóði** skal velja nýjan ástæðukóða.</span><span class="sxs-lookup"><span data-stu-id="2a02f-184">Select **Cycle counting**, and then, in the **Reason code** field, select a new reason code.</span></span>

### <a name="modify-the-mobile-device-menu-item-for-adjustment-in-and-adjustment-out"></a><span data-ttu-id="2a02f-185">Breyttu valmyndaratriði fartækis fyrir Leiðréttingu inn og Leiðréttingu út</span><span class="sxs-lookup"><span data-stu-id="2a02f-185">Modify the mobile device menu item for Adjustment in and Adjustment out</span></span>

1. <span data-ttu-id="2a02f-186">Veldu **Vöruhúsakerfi** \> **Uppsetning** \> **Fartæki** \> **Valmyndaratriði fartækis** og veldu síðan **Leiðrétting inn og út**.</span><span class="sxs-lookup"><span data-stu-id="2a02f-186">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**, and then select **Adjustment in and out**.</span></span>
2. <span data-ttu-id="2a02f-187">Stilltu valkostinn **Nota núverandi verk** á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="2a02f-187">Set the **Use existing work** option to **No**.</span></span>
3. <span data-ttu-id="2a02f-188">Í reitnum **Ferli verkstofnunar** skal velja **Leiðrétting inn**.</span><span class="sxs-lookup"><span data-stu-id="2a02f-188">In the **Work creation process** field, select **Adjustment in**.</span></span>

<span data-ttu-id="2a02f-189">Eftirfarandi reitum verður bætt við valmyndaratriði fartækis þegar **Leiðrétting inn** eða **Leiðrétting út** er valin á meðan ferli verkstofnunar stendur yfir:</span><span class="sxs-lookup"><span data-stu-id="2a02f-189">The following fields will be added to the mobile device menu item when **Adjustment in** or **Adjustment out** is selected during the work creation process:</span></span>

- <span data-ttu-id="2a02f-190">Sjálfgefinn ástæðukóði talningar</span><span class="sxs-lookup"><span data-stu-id="2a02f-190">Default counting reason code</span></span>
- <span data-ttu-id="2a02f-191">Birta ástæðukóða talningar</span><span class="sxs-lookup"><span data-stu-id="2a02f-191">Display counting reason code</span></span>
- <span data-ttu-id="2a02f-192">Breyta ástæðukóða talningar</span><span class="sxs-lookup"><span data-stu-id="2a02f-192">Edit counting reason code</span></span>

