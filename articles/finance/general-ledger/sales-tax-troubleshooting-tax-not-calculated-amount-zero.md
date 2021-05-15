---
title: Skatturinn er ekki reiknaður eða skattupphæðin er núll
description: Þetta efnisatriði inniheldur villuleitarupplýsingar sem geta hjálpað þegar skattaupphæðin er 0 (núll) eða skatturinn er ekki reiknaður.
author: shtao
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: ead979081692d4dcee9812c89f5f10c7879d3f7e
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947656"
---
# <a name="tax-isnt-calculated-or-the-tax-amount-is-zero"></a><span data-ttu-id="5e662-103">Skatturinn er ekki reiknaður eða skattupphæðin er núll</span><span class="sxs-lookup"><span data-stu-id="5e662-103">Tax isn't calculated or the tax amount is zero</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e662-104">Færsla gæti verið með línuupphæð sem er ekki 0 (núll) en annaðhvort er skatturinn ekki reiknaður eða reiknaður skattupphæð er 0.</span><span class="sxs-lookup"><span data-stu-id="5e662-104">A transaction might have a line amount that isn't 0 (zero), but either tax isn't calculated or the calculated tax amount is 0.</span></span> <span data-ttu-id="5e662-105">Til að leysa úr vandamálinu skal fylgja skrefunum í eftirfarandi hlutum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="5e662-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span>

## <a name="verify-that-tax-codes-are-correctly-selected-by-the-transaction"></a><span data-ttu-id="5e662-106">Staðfestu að skattkóðar séu rétt valdir af færslunni</span><span class="sxs-lookup"><span data-stu-id="5e662-106">Verify that tax codes are correctly selected by the transaction</span></span>

<span data-ttu-id="5e662-107">Ef færslan velur ekki rétta skattkóða eða, ef hún velur enga skattkóða, verða skattar ekki reiknaðir út af henni.</span><span class="sxs-lookup"><span data-stu-id="5e662-107">If the transaction doesn't select the correct tax codes, or if it doesn't select any tax codes, taxes won't be calculated on it.</span></span> <span data-ttu-id="5e662-108">Fylgið eftirfarandi skrefum til að staðfesta að skattkóðar séu rétt valdir af færslunni.</span><span class="sxs-lookup"><span data-stu-id="5e662-108">Follow these steps to verify that tax codes are correctly selected by the transaction.</span></span> 

1. <span data-ttu-id="5e662-109">Í færslulínunni, í flýtiflipanum **Upplýsingar um línu**, í flipanum **Uppsetning**, í hlutanum **Virðisaukaskattur**, skal staðfesta réttur skattflokkur hafi verið valinn í reitunum **VSK-flokkur vöru** og **VSK-flokkur**.</span><span class="sxs-lookup"><span data-stu-id="5e662-109">On the transaction line, on the **Line details** FastTab, on the **Setup** tab, in the **Sales tax** section, verify that the correct tax groups are selected in the **Item sales tax group** and **Sales tax group** fields.</span></span> <span data-ttu-id="5e662-110">Ef réttir skattflokkar eru ekki valdir skaltu velja þá.</span><span class="sxs-lookup"><span data-stu-id="5e662-110">If the correct tax groups aren't selected, select them.</span></span>

    <span data-ttu-id="5e662-111">[![Reitir VSK-flokks vöru og VSK-flokks](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="5e662-111">[![Item sales tax group and Sales tax group fields](./media/tax-not-calculated-tax-amount-zero-Picture1.png)](./media/tax-not-calculated-tax-amount-zero-Picture1.png)</span></span>

2. <span data-ttu-id="5e662-112">Farið í **Skattur** \> **Óbeinir skattar** \> **Söluskattur** \> **Söluskattflokkar**.</span><span class="sxs-lookup"><span data-stu-id="5e662-112">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
3. <span data-ttu-id="5e662-113">Veljið viðeigandi VSK-flokk og síðan í flýtiflipanum **Uppsetning** skal hafa í huga skattkóðann í reitnum **VSK-kóði**.</span><span class="sxs-lookup"><span data-stu-id="5e662-113">Select the appropriate sales tax group, and then, on the **Setup** FastTab, make a note of the tax code in the **Sales tax code** field.</span></span>

    <span data-ttu-id="5e662-114">[![Síða VSK-flokks](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="5e662-114">[![Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture2.png)](./media/tax-not-calculated-tax-amount-zero-Picture2.png)</span></span>

4. <span data-ttu-id="5e662-115">Farið í **Skattur** \> **Óbeinir skattar** \> **Söluskattur** \> **VSK-flokkur vöru**.</span><span class="sxs-lookup"><span data-stu-id="5e662-115">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Item sales tax groups**.</span></span>
5. <span data-ttu-id="5e662-116">Veljið viðeigandi VSK-flokk vöru og síðan í flýtiflipanum **Uppsetning** skal staðfesta að skattkóðinn í reitnum **VSK-kóði** passi við skattkóða VSK-flokksins.</span><span class="sxs-lookup"><span data-stu-id="5e662-116">Select the appropriate item sales tax group, and then, on the **Setup** FastTab, verify that the tax code in the **Sales tax code** field matches the tax code of the sales tax group.</span></span>

    <span data-ttu-id="5e662-117">[![Síðan VSK-flokkur vöru](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="5e662-117">[![Item sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture3.png)](./media/tax-not-calculated-tax-amount-zero-Picture3.png)</span></span>

6. <span data-ttu-id="5e662-118">Ef VSK-kóðarnir passa ekki saman skaltu uppfæra VSK-kóðann fyrir einn af hópunum.</span><span class="sxs-lookup"><span data-stu-id="5e662-118">If the tax codes don't match, update the sales tax code for one of the groups.</span></span>

## <a name="verify-that-the-selected-tax-codes-arent-exempt-and-that-they-have-the-correct-tax-rate-value"></a><span data-ttu-id="5e662-119">Staðfestið að vödlu skattkóðarnir séu ekki undanþegnir og að þeir hafi rétt skatthlutfallsgildi</span><span class="sxs-lookup"><span data-stu-id="5e662-119">Verify that the selected tax codes aren't exempt and that they have the correct tax rate value</span></span>

<span data-ttu-id="5e662-120">Ef skattkóðarnir eru undanþegnir, eða ef skatthlutfallið er 0 (núll), verður útreikningsniðurstaða skatts 0.</span><span class="sxs-lookup"><span data-stu-id="5e662-120">If the tax codes are exempt, or if the tax rate is 0 (zero), the tax calculation result will be 0.</span></span> <span data-ttu-id="5e662-121">Fylgið eftirfarandi skrefum til að ákvarða hvort valdir skattkóðar séu undanþegnir og til að staðfesta að rétt skatthlutfall sé notað fyrir þá.</span><span class="sxs-lookup"><span data-stu-id="5e662-121">Follow these steps to determine whether the selected tax codes are exempt and to verify that the correct tax rate is applied to them.</span></span>

1. <span data-ttu-id="5e662-122">Farið í **Skattur** \> **Óbeinir skattar** \> **Söluskattur** \> **Söluskattflokkar**.</span><span class="sxs-lookup"><span data-stu-id="5e662-122">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax groups**.</span></span>
2. <span data-ttu-id="5e662-123">Veljið viðeigandi VSK-flokk og síðan í flýtiflipanum **Uppsetning** skal staðfesta að gátreiturinn **Undanþegið** sé hreinsaður.</span><span class="sxs-lookup"><span data-stu-id="5e662-123">Select the appropriate sales tax group, and then, on the **Setup** FastTab, verify that the **Exempt** check box is cleared.</span></span> <span data-ttu-id="5e662-124">Ef hann er valinn skal hreinsa hann.</span><span class="sxs-lookup"><span data-stu-id="5e662-124">If it's selected, clear it.</span></span>

    <span data-ttu-id="5e662-125">[![Gátreitur undanþágu á síðu VSK-flokka](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="5e662-125">[![Exempt check box on the Sales tax groups page](./media/tax-not-calculated-tax-amount-zero-Picture4.png)](./media/tax-not-calculated-tax-amount-zero-Picture4.png)</span></span>

3. <span data-ttu-id="5e662-126">Farið í **Skattur** \> **Óbeinir skattar** \> **Söluskattur** \> **Söluskattflokkur**.</span><span class="sxs-lookup"><span data-stu-id="5e662-126">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="5e662-127">Veljið viðeigandi VSK-kóða og staðfestið síðan að skatthlutfallsgildi í reitnum **Gildi** sé ekki 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="5e662-127">Select the appropriate sales tax code, and then verify that the tax rate value in the **Value** field isn't 0 (zero).</span></span> <span data-ttu-id="5e662-128">Ef það er 0 skal uppfæra reitinn þannig að hann sé stilltur á rétt skatthlutfall.</span><span class="sxs-lookup"><span data-stu-id="5e662-128">If it's 0, update the field so that it's set to the correct tax rate.</span></span>

    <span data-ttu-id="5e662-129">[![Reitur gildis á síðu fyrir gildi VSK-kóða](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="5e662-129">[![Value field on the Sales tax code values page](./media/tax-not-calculated-tax-amount-zero-Picture5.png)](./media/tax-not-calculated-tax-amount-zero-Picture5.png)</span></span>

## <a name="determine-whether-zero-is-the-correct-tax-amount"></a><span data-ttu-id="5e662-130">Ákvarðið hvort núll sé rétt skattupphæð</span><span class="sxs-lookup"><span data-stu-id="5e662-130">Determine whether zero is the correct tax amount</span></span>

<span data-ttu-id="5e662-131">Í sumum tilvikum er skattfjárhæðin 0 (núll) rétt.</span><span class="sxs-lookup"><span data-stu-id="5e662-131">In some scenarios, a tax amount of 0 (zero) is correct.</span></span> <span data-ttu-id="5e662-132">Fylgið eftirfarandi skrefum til að ákvarða hvort 0 sé rétt skattfjárhæð fyrir færsluna.</span><span class="sxs-lookup"><span data-stu-id="5e662-132">Follow these steps to determine whether 0 is the correct tax amount for your transaction.</span></span>

1. <span data-ttu-id="5e662-133">Opnið **Fjárhagur** \> **Fjárhagsuppsetning** \> **Færibreytur fyrir fjárhag**.</span><span class="sxs-lookup"><span data-stu-id="5e662-133">Go to **General ledger** \> **Ledger setup** \> **General ledger parameters**.</span></span>
2. <span data-ttu-id="5e662-134">Á flipanum **Söluskattur** í reitnum **Útreikningsaðferð** skal staðfesta að **Alls** sé valin.</span><span class="sxs-lookup"><span data-stu-id="5e662-134">On the **Sales tax** tab, in the **Calculation method** field, verify that **Total** is selected.</span></span>

    <span data-ttu-id="5e662-135">[![Reitur reikningsaðferðar á færibreytusíðu fjárhags](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="5e662-135">[![Calculation method field on the General ledger parameters page](./media/tax-not-calculated-tax-amount-zero-Picture6.png)](./media/tax-not-calculated-tax-amount-zero-Picture6.png)</span></span>

3. <span data-ttu-id="5e662-136">Farið í **Skattur** \> **Óbeinir skattar** \> **Söluskattur** \> **Söluskattflokkur**.</span><span class="sxs-lookup"><span data-stu-id="5e662-136">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
4. <span data-ttu-id="5e662-137">Veljið viðeigandi VSK-kóða, veljið **Útreikningur** \> **Jaðargrunnur** og staðfestið að jaðargrunnurinn sé stilltur á **Nettóupphæð af reikningsstöðu** eða **Samtala reiknings að meðtöldum öðrum VSK-upphæðum**.</span><span class="sxs-lookup"><span data-stu-id="5e662-137">Select the appropriate sales tax code, select **Calculation** \> **Marginal base**, and verify that the marginal base is set to **Net amount of invoice balance** or **Invoice total incl. other sales tax amounts**.</span></span> <span data-ttu-id="5e662-138">Frekari upplýsingar eru í [Samtala reiknings að meðtöldum öðrum VSK-upphæðum](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span><span class="sxs-lookup"><span data-stu-id="5e662-138">For more information, see the [Invoice total incl. other sales tax amounts](marginal-base-field.md#invoice-total-incl-other-sales-tax-amounts).</span></span>
5. <span data-ttu-id="5e662-139">Ef rétt gildi eru stillt í skrefum 2 og 4 skal ákvarða hvort heildarupphæð færslunnar sé 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="5e662-139">If the correct values are set in steps 2 and 4, determine whether the total amount of the transaction is 0 (zero).</span></span> <span data-ttu-id="5e662-140">Ef heildarupphæðin er 0 er skattupphæð 0 væntanleg niðurstaða.</span><span class="sxs-lookup"><span data-stu-id="5e662-140">If the total amount is 0, a tax amount of 0 is the expected result.</span></span> <span data-ttu-id="5e662-141">Þar sem skattaútreikningurinn er byggður á heildarupphæð reikningsupphæðarinnar, og upphæðin er ekki lína fyrir línu, verður skattupphæðinni 0 úthlutað á hverja línu eftir skattaútreikninginn.</span><span class="sxs-lookup"><span data-stu-id="5e662-141">Because the tax calculation is based on the total amount of the invoice balance, and that amount isn't line by line, the tax amount of 0 will be allocated to each line after the tax calculation.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="5e662-142">Ákvarða hvort sérstilling sé til staðar</span><span class="sxs-lookup"><span data-stu-id="5e662-142">Determine whether customization exists</span></span>

<span data-ttu-id="5e662-143">Ef þú hefur lokið við skrefin í fyrri hlutum en hefur ekki getað leyst vandamálið skaltu komast að því hvort sérstillingar séu til staðar.</span><span class="sxs-lookup"><span data-stu-id="5e662-143">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="5e662-144">Ef engin sérstilling er til skal stofna þjónustubeiðni frá Microsoft til að fá frekari aðstoð.</span><span class="sxs-lookup"><span data-stu-id="5e662-144">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
