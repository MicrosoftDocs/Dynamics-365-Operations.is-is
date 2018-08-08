---
title: "Kostnaðarverð skilavöru og lotukenni skila"
description: "Þú gætir viljað að kostnaður skilavaranna jafngildi kostnaði varanna á þeim tíma þegar þú seldir vörurnar til viðskiptavinarins. Þú getur gert þetta með því að nota **Lotukenni skila**."
author: ShylaThompson
manager: AnnBe
ms.date: 04/30/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReturnTableListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 33cd3d50fe342ba12a17419f4e759c243a60b3e0
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---

# <a name="return-cost-price-and-return-lot-id"></a><span data-ttu-id="88137-104">Kostnaðarverð skilavöru og lotukenni skila</span><span class="sxs-lookup"><span data-stu-id="88137-104">Return cost price and return lot ID</span></span>        

[!include [banner](../includes/banner.md)]



<span data-ttu-id="88137-105">Kostnaður við vörur sem er skilað til birgða er reiknaður með því að nota núverandi kostnað vörunnar.</span><span class="sxs-lookup"><span data-stu-id="88137-105">The cost of products that are returned to inventory is calculated by using the current cost of the products.</span></span> <span data-ttu-id="88137-106">Hins vegar gætir þú viljað að kostnaður skilavaranna jafngildi kostnaði varanna á þeim tíma þegar þú seldir vörurnar til viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="88137-106">However, you might want the cost of the returned products to equal the cost of the products at the time when you sold the products to the customer.</span></span> <span data-ttu-id="88137-107">Þú getur gert þetta með því að nota reitinn **Lotukenni skila** á flýtiflipanum **Línuupplýsingar** í skjámyndinni **Sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="88137-107">You can do this by using the **Return lot ID** field on the **Line details** FastTab in the **Sales order** form.</span></span>

<span data-ttu-id="88137-108">Íhugaðu til dæmis eftirfarandi atburðarás.</span><span class="sxs-lookup"><span data-stu-id="88137-108">For example, consider the following scenario.</span></span> <span data-ttu-id="88137-109">Þú sendir viðskiptavini reikning.</span><span class="sxs-lookup"><span data-stu-id="88137-109">You invoice a customer.</span></span> <span data-ttu-id="88137-110">Síðan skilar viðskiptavinurinn afgreiddum vörum til þín.</span><span class="sxs-lookup"><span data-stu-id="88137-110">Then, the customer returns the delivered products to you.</span></span> <span data-ttu-id="88137-111">Þú skilar vörunum á lager.</span><span class="sxs-lookup"><span data-stu-id="88137-111">You return the products to stock.</span></span> <span data-ttu-id="88137-112">Í þessu tilviki, þegar þú kreditfærir viðskiptavininn vegna skilavaranna, er kostnaður þessara vara reiknaður út með því að nota núverandi kostnað varanna.</span><span class="sxs-lookup"><span data-stu-id="88137-112">In this case, when you credit the customer for the returned products, the cost of those products is calculated by using the current cost of the products.</span></span> <span data-ttu-id="88137-113">Hins vegar, ef þú notar reitinn **Lotukenni skila**, er kostnaðurinn á skilavörunum reiknaður út með því að nota kostnað á reikningi upprunalegu sölunnar til viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="88137-113">However, if you use the **Return lot ID** field, the cost of the returned products is calculated by using the cost on the invoice of the original sale to the customer.</span></span>

<span data-ttu-id="88137-114">Til að nota annan kostnað en núverandi kostnað vegna skila viðskiptavinar skaltu nota eina af eftirfarandi aðferðum.</span><span class="sxs-lookup"><span data-stu-id="88137-114">To use a cost other than the current cost for returns from a customer, use one of the following methods.</span></span>

## <a name="method-1-manually-enter-the-return-cost-price"></a><span data-ttu-id="88137-115">Aðferð 1: Sláðu inn handvirkt kostnaðarverð skila</span><span class="sxs-lookup"><span data-stu-id="88137-115">Method 1: Manually enter the return cost price</span></span>

<span data-ttu-id="88137-116">Að sjálfgefnu, þegar þú bætir vörum við skilapöntun, er vörunum skilað til birgða á núverandi kostnaðarverði.</span><span class="sxs-lookup"><span data-stu-id="88137-116">By default, when you add items to a return order, the items are returned to inventory at the current cost price.</span></span> <span data-ttu-id="88137-117">Til að tilgreina annað kostnaðarverð skila skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="88137-117">To specify a different return cost price, follow these steps.</span></span>

1.  <span data-ttu-id="88137-118">Smelltu á **Sala og markaðssetning** \> **Almennt** \> **Skilapantanir** \> **Allar skilapantanir**.</span><span class="sxs-lookup"><span data-stu-id="88137-118">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="88137-119">Í **Aðgerðarsvæði**, í flokknum **Nýtt**, skaltu smella á **Skilapöntun**.</span><span class="sxs-lookup"><span data-stu-id="88137-119">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="88137-120">Í skjámyndinni **Stofna skilapöntun** skaltu velja viðskiptavinalykil og smella síðan á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="88137-120">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="88137-121">Í skjámyndinni **Skilapöntun - RMA-númer: %1, %2** skaltu velja vöru og síðan færa inn neikvætt magn í reitinn **Magn**.</span><span class="sxs-lookup"><span data-stu-id="88137-121">In the **Return order - RMA number: %1, %2** form, select an item, and then enter a negative quantity in the **Quantity** field.</span></span>

5.  <span data-ttu-id="88137-122">Smellið á flýtiflipa **Upplýsingar um línur**.</span><span class="sxs-lookup"><span data-stu-id="88137-122">Click the **Line details** FastTab.</span></span>

6.  <span data-ttu-id="88137-123">Á flipanum **Almennt** skaltu færa inn gildi í reitinn **Kostnaðarverð skila**.</span><span class="sxs-lookup"><span data-stu-id="88137-123">On the **General** tab, enter a value in the **Return cost price** field.</span></span> <span data-ttu-id="88137-124">Þetta gildi er notað þegar vörunum er skilað til birgða.</span><span class="sxs-lookup"><span data-stu-id="88137-124">This value is used when the goods are returned to inventory.</span></span> <span data-ttu-id="88137-125">Ef þú færir ekki inn gildi er núverandi kostnaðarverð notað þegar vörunum er skilað til birgða.</span><span class="sxs-lookup"><span data-stu-id="88137-125">If you do not enter a value, the current cost price is used when the goods are returned to inventory.</span></span>

## <a name="method-2-automatically-generate-the-cost-price-based-on-the-customer-invoice-line"></a><span data-ttu-id="88137-126">Aðferð 2: Búa til kostnaðarverð sjálfkrafa byggt á reikningslínu viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="88137-126">Method 2: Automatically generate the cost price based on the customer invoice line</span></span>

<span data-ttu-id="88137-127">Þetta er æskilega aðferðin til að búa til skilalínur.</span><span class="sxs-lookup"><span data-stu-id="88137-127">This is the preferred method to use to create return lines.</span></span> <span data-ttu-id="88137-128">Til að nota kostnað vörunnar á þeim tíma sem þú seldir vörurnar til viðskiptavinarins skaltu búa til skilapöntun og tilgreina sölulínu til að skila.</span><span class="sxs-lookup"><span data-stu-id="88137-128">To use the cost of the products at the time when you sold the products to the customer, create a return order and specify a sales line to return.</span></span>

1.  <span data-ttu-id="88137-129">Smelltu á **Sala og markaðssetning** \> **Almennt** \> **Skilapantanir** \> **Allar skilapantanir**.</span><span class="sxs-lookup"><span data-stu-id="88137-129">Click **Sales and marketing** \> **Common** \> **Return orders** \> **All return orders**.</span></span>

2.  <span data-ttu-id="88137-130">Í **Aðgerðarsvæði**, í flokknum **Nýtt**, skaltu smella á **Skilapöntun**.</span><span class="sxs-lookup"><span data-stu-id="88137-130">On the **Action Pane**, in the **New** group, click **Return order**.</span></span>

3.  <span data-ttu-id="88137-131">Í skjámyndinni **Stofna skilapöntun** skaltu velja viðskiptavinalykil og smella síðan á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="88137-131">In the **Create return order** form, select a customer account, and then click **OK**.</span></span>

4.  <span data-ttu-id="88137-132">Í skjámyndinni **Skilapöntun - RMA-númer: %1, %2** í **Aðgerðasvæði** skal smella á **Finna sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="88137-132">In the **Return order - RMA number: %1, %2** form, on the **Action Pane**, click **Find sales order**.</span></span>

5.  <span data-ttu-id="88137-133">Í skjámyndinni **Finna sölupöntun** skaltu velja reikningslínuna sem á að skila og smella síðan á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="88137-133">In the **Find sales order** form, select the invoice line to return, and then click **OK**.</span></span>
    
    <span data-ttu-id="88137-134">Á flýtiflipanum **Línuupplýsingar**, á flipanum **Almennt**, sýnir reiturinn **Lotukenni skila** gildið á upprunalegu sölulínunni.</span><span class="sxs-lookup"><span data-stu-id="88137-134">On the **Line details** FastTab, on the **General** tab, the **Return lot ID** field displays the value from the original sales line.</span></span> <span data-ttu-id="88137-135">Að auki sýnir reiturinn **Kostnaðarverð skila** kostnaðargildi upphaflegu sölulínunnar.</span><span class="sxs-lookup"><span data-stu-id="88137-135">Additionally, the **Return cost price** field displays the cost value from the original sales line.</span></span>

## <a name="cost-calculation-example"></a><span data-ttu-id="88137-136">Dæmi um kostnaðarreikning</span><span class="sxs-lookup"><span data-stu-id="88137-136">Cost calculation example</span></span>

<span data-ttu-id="88137-137">Þegar þú notar reitinn **Lotukenni skila** á skilapöntunarlínu til að tilgreina kostnaðarverð skila er kostnaðurinn á skilapöntunarlínunni notaður.</span><span class="sxs-lookup"><span data-stu-id="88137-137">When you use the **Return lot ID** field on a return order line to specify the return cost price, the cost on the return order line is used.</span></span> <span data-ttu-id="88137-138">Ef þú keyrir virkni lokunar eða endurreikning birgða er kostnaðurinn stilltur á upprunalegu sölulínunni.</span><span class="sxs-lookup"><span data-stu-id="88137-138">If you run the inventory close or recalculation functionality, the cost is adjusted on the original sales line.</span></span> <span data-ttu-id="88137-139">Kostnaðurinn á skilapöntunarlínunni er sjálfkrafa stilltur til að endurspegla sama kostnað á hvert stykki.</span><span class="sxs-lookup"><span data-stu-id="88137-139">The cost on the return order line is automatically adjusted to reflect the same cost per piece.</span></span>

1.  <span data-ttu-id="88137-140">Stofna og losa vöru sem heitir Próf.</span><span class="sxs-lookup"><span data-stu-id="88137-140">Create and release a product that is named Test.</span></span> <span data-ttu-id="88137-141">Í skjámyndinni **Upplýsingar um losaðar afurðir** eru eftirfarandi upplýsingar tilgreindar:</span><span class="sxs-lookup"><span data-stu-id="88137-141">In the **Released product details** form, specify the following information:</span></span>
    
    1.  <span data-ttu-id="88137-142">Á flýtiflipanum **Stjórna kostnaði**, í reitnum **Vöruflokkur** skal velja flokkinn **Hlutar**.</span><span class="sxs-lookup"><span data-stu-id="88137-142">On the **Manage costs** FastTab, in the **Item group** field, select the **Parts** group.</span></span>
    
    2.  <span data-ttu-id="88137-143">Á flýtiflipanum **Almennt**, í reitnum **Vörulíkanaflokkur** skal velja **DEF**.</span><span class="sxs-lookup"><span data-stu-id="88137-143">On the **General** FastTab, in the **Item model group** field, select **DEF**.</span></span>
    
    3.  <span data-ttu-id="88137-144">Á flýtiflipanum **Innkaup**, í reitnum **Verð** skal slá inn 10,00 sem kostnaðarverð vörunnar.</span><span class="sxs-lookup"><span data-stu-id="88137-144">On the **Purchase** FastTab, in the **Price** field, type 10.00 as the cost price of the item.</span></span>
    
    4.  <span data-ttu-id="88137-145">Í **Aðgerðasvæði** er smellt á **Víddarflokkar**.</span><span class="sxs-lookup"><span data-stu-id="88137-145">On the **Action Pane**, click **Dimension groups**.</span></span> <span data-ttu-id="88137-146">Í reitnum **Geymsluvíddarflokkur** skal velja **Svæði og vöruhús eingöngu**.</span><span class="sxs-lookup"><span data-stu-id="88137-146">In the **Storage dimension group** field, select **Site and Warehouse only**.</span></span> <span data-ttu-id="88137-147">Í reitnum **Rakningarvíddarflokkur** skal velja **Engar virkar rakningarvíddir**.</span><span class="sxs-lookup"><span data-stu-id="88137-147">In the **Tracking dimension group** field, select **No active tracking dimensions**.</span></span>

2.  <span data-ttu-id="88137-148">Stofnaðu innkaupapöntun fyrir 10 stykkjum af prufuvörunni á 6,00 fyrir hvert stykki og bókaðu síðan reikning fyrir innkaupapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="88137-148">Create a purchase order for 10 pieces of the Test item at 6.00 per piece, and then post an invoice for the purchase order.</span></span>
    
    <span data-ttu-id="88137-149">Stofnaðu aðra innkaupapöntun fyrir 10 stykkjum af prufuvörunni á 8,00 fyrir hvert stykki og bókaðu síðan reikning fyrir innkaupapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="88137-149">Create a second purchase order for 10 pieces of the Test item at 8.00 per piece, and then post an invoice for the purchase order.</span></span>

3.  <span data-ttu-id="88137-150">Bókaðu reikning fyrir sölupöntun til að selja fimm stykki af prufuvörunni.</span><span class="sxs-lookup"><span data-stu-id="88137-150">Post an invoice for a sales order to sell five pieces of the Test item.</span></span>
    
    <span data-ttu-id="88137-151">Í þessu tilviki er sölupöntunarlínan kostuð á 35,00 (5 stykki \* 7,00 meðalkostnaður á stykki).</span><span class="sxs-lookup"><span data-stu-id="88137-151">In this case, the sales order line is costed at 35.00 (5 pieces \* 7.00 average cost per piece).</span></span>

4.  <span data-ttu-id="88137-152">Stofnaðu skilapöntun fyrir viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="88137-152">Create a return order for the customer.</span></span> <span data-ttu-id="88137-153">Í skjámyndinni **Finna sölupöntun** skaltu velja reikningslínuna og smella síðan á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="88137-153">In the **Find sales order** form, select the invoice line, and then click **OK**.</span></span>

5.  <span data-ttu-id="88137-154">Í skjámyndinni **Skilapöntun - RMA-númer: %1, %2** skaltu staðfesta að skilapöntun sé gerð til að skila prufuvörunni.</span><span class="sxs-lookup"><span data-stu-id="88137-154">In the **Return order - RMA number: %1, %2** form, verify that a return order is generated to return the Test item.</span></span> <span data-ttu-id="88137-155">Magn skilapöntunarinnar er stillt á -5,00.</span><span class="sxs-lookup"><span data-stu-id="88137-155">The quantity of the return order is set to -5.00.</span></span>
    
    <span data-ttu-id="88137-156">Reiturinn **Lotukenni skila** sýnir lotukenni.</span><span class="sxs-lookup"><span data-stu-id="88137-156">The **Return lot ID** field displays a lot ID.</span></span> <span data-ttu-id="88137-157">Þetta lotukenni er tekið frá upprunalegu sölupöntuninni á vörunni sem seld var viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="88137-157">This lot ID is taken from the original sales order of the item that was sold to the customer.</span></span> <span data-ttu-id="88137-158">Reiturinn **Kostnaðarverð skila** sýnir kostnaðarverð upprunalegu sölulínunnar.</span><span class="sxs-lookup"><span data-stu-id="88137-158">The **Return cost price** field displays the cost price from the original sales line.</span></span>

6.  <span data-ttu-id="88137-159">Skráðu móttöku á skilavörum.</span><span class="sxs-lookup"><span data-stu-id="88137-159">Register the receipt of the returned items.</span></span>

7.  <span data-ttu-id="88137-160">Bókaðu fylgiseðil fyrir skilavörum.</span><span class="sxs-lookup"><span data-stu-id="88137-160">Post a packing slip for the returned items.</span></span>

8.  <span data-ttu-id="88137-161">Bókaðu reikning fyrir skilapöntuninni.</span><span class="sxs-lookup"><span data-stu-id="88137-161">Post an invoice for the return order.</span></span> <span data-ttu-id="88137-162">Á listasíðunni **Allar sölupantanir** skaltu velja sölupöntun þar sem **Skilapöntun** er pöntunargerðin.</span><span class="sxs-lookup"><span data-stu-id="88137-162">On the **All sales orders** list page, select a sales order for which **Returned order** is the order type.</span></span>

9.  <span data-ttu-id="88137-163">Opnaðu skjámyndina **Birgðafærslur**.</span><span class="sxs-lookup"><span data-stu-id="88137-163">Open the **Inventory transactions** form.</span></span> <span data-ttu-id="88137-164">Staðfestu að skilin eru kostuð á 7,00 á stykki með því að nota gildið í reitnum **Kostnaðarverð skila** fyrir samtals 35,00 í reitnum **Kostnaðarupphæð**.</span><span class="sxs-lookup"><span data-stu-id="88137-164">Verify that the return is costed at 7.00 per piece by using the value in the **Return cost price** field, for a total of 35.00 in the **Cost amount** field.</span></span> <span data-ttu-id="88137-165">Þú getur opnað skjámyndina **Birgðafærslur** í skjámyndinni **Skilapöntun - RMA-númer: %1, %2**.</span><span class="sxs-lookup"><span data-stu-id="88137-165">You can open the **Inventory transactions** form from the **Return order - RMA number: %1, %2** form.</span></span> <span data-ttu-id="88137-166">Í hnitanetinu **Línur** skaltu smella á **Birgðir** \> **Færslur**.</span><span class="sxs-lookup"><span data-stu-id="88137-166">In the **Lines** grid, click **Inventory** \> **Transactions**.</span></span>

10. <span data-ttu-id="88137-167">Í „Birgða- og vöruhúsakerfi“ skaltu nota skjámyndina **Lokun og leiðrétting** til að keyra ferlið **3. Loka**.</span><span class="sxs-lookup"><span data-stu-id="88137-167">In Inventory and warehouse management, use the **Closing and adjustment** form to run the **3. Close** procedure.</span></span>
    
    <span data-ttu-id="88137-168">Þessi aðgerð leiðréttir kostnaðinn á upprunalegu sölulínunni sem var verðlagður á -35,00 (5 stykki \* 7,00) í -30,00 (5 stykki \* 6,00).</span><span class="sxs-lookup"><span data-stu-id="88137-168">This action adjusts the cost on the original sales line that was costed at -35.00 (5 pieces \* 7.00) to -30.00 (5 pieces \* 6.00).</span></span> <span data-ttu-id="88137-169">Þetta er vegna þess að birgðalíkanaflokkurinn notar fyrst inn, fyrst út (FIFO) og 6,00 á stykki er FIFO-kostnaðurinn frá fyrstu innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="88137-169">This is because the inventory model group uses First in, First out (FIFO), and 6.00 per piece is the FIFO cost from the first purchase order.</span></span> <span data-ttu-id="88137-170">Að auki leiðréttir aðgerðin kostnaðinn á sölulínu skila til að passa við kostnaðinn á stykki á upprunalegu sölulínunni.</span><span class="sxs-lookup"><span data-stu-id="88137-170">Additionally, the action adjusts the cost on the return sales line to match the cost per piece on the original sales line.</span></span> <span data-ttu-id="88137-171">Þess vegna er kostnaður á skilalínu leiðréttur úr 35,00 í 30,00.</span><span class="sxs-lookup"><span data-stu-id="88137-171">Therefore, the cost of the return line is adjusted from 35.00 to 30.00.</span></span>





