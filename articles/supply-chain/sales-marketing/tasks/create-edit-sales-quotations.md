--- 
title: "Stofna og breyta sölutilboðum"
description: "Þetta ferli sýnir hvernig á að stofna og uppfæra sölutilboð."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesQuotationListPage, SalesCreateQuotation, SalesQuotationTable, SalesQuotationTotals, SalesQuotationPriceSimulation, SalesQuotationEditLines, SrsReportViewerForm, smmSetNumSeqIfManual, CustTable, SalesTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 5b5618a815aaff12dd366523920ed275801b3b16
ms.contentlocale: is-is
ms.lasthandoff: 09/14/2018

---
# <a name="create-and-edit-sales-quotations"></a><span data-ttu-id="cabb5-103">Stofna og breyta sölutilboðum</span><span class="sxs-lookup"><span data-stu-id="cabb5-103">Create and edit sales quotations</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cabb5-104">Þetta ferli sýnir hvernig á að stofna og uppfæra sölutilboð.</span><span class="sxs-lookup"><span data-stu-id="cabb5-104">This procedure demonstrates how to create and update a sales quotation.</span></span> <span data-ttu-id="cabb5-105">Hægt er að keyra þetta ferli á eigin gögn eða í sýnigögn USMF fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="cabb5-105">You can run this procedure on your own data or in demo data company USMF.</span></span>


## <a name="create-a-sales-quotation"></a><span data-ttu-id="cabb5-106">Stofna sölutilboð</span><span class="sxs-lookup"><span data-stu-id="cabb5-106">Create a sales quotation</span></span>
1. <span data-ttu-id="cabb5-107">Fara í Sölu og markaðssetningu > Sölutilboð > Öll tilboð.</span><span class="sxs-lookup"><span data-stu-id="cabb5-107">Go to Sales and marketing > Sales quotations > All quotations.</span></span>
2. <span data-ttu-id="cabb5-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="cabb5-108">Click New.</span></span>
3. <span data-ttu-id="cabb5-109">Veljið 'Viðfang' í svæðinu gerð lykils.</span><span class="sxs-lookup"><span data-stu-id="cabb5-109">In the Account type field, select 'Prospect'.</span></span>
4. <span data-ttu-id="cabb5-110">Færa inn eða veljið gildi í svæðinu viðfang.</span><span class="sxs-lookup"><span data-stu-id="cabb5-110">In the Prospect field, enter or select a value.</span></span>
5. <span data-ttu-id="cabb5-111">Víkkið út almenna hlutann.</span><span class="sxs-lookup"><span data-stu-id="cabb5-111">Expand the General section.</span></span>
    * <span data-ttu-id="cabb5-112">Þar sem valið var að stofna tilboð frá Sölu og Markaðssetningar svæði, er gerð sjálfkrafa stillt á sölutilboð.</span><span class="sxs-lookup"><span data-stu-id="cabb5-112">Because you chose to create a quotation from the Sales and Marketing area, the type is automatically set to Sales quotation.</span></span> <span data-ttu-id="cabb5-113">Til að stofna tilboð fyrir verk verður opnuð hana úr verkefnastjórnunar- og bókhaldskerfi.</span><span class="sxs-lookup"><span data-stu-id="cabb5-113">To create a quotation for a project you must access it from the Project management and accounting module.</span></span>   
6. <span data-ttu-id="cabb5-114">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cabb5-114">Click OK.</span></span>
    * <span data-ttu-id="cabb5-115">Svæði og aðgerðir í tilboðslínunum er mjög svipuð þær á sölupöntunarlínum.</span><span class="sxs-lookup"><span data-stu-id="cabb5-115">The fields and actions on the quotation lines are very similar to the ones on the sales order lines.</span></span>   <span data-ttu-id="cabb5-116">Eins og sölupantanir er hægt að stofna tilboð fyrir tiltekna vöru eða þegar vörunúmerið er ekki þekkt eða er ekki til þegar tilboð var stofnað, hægt er að stofna tilboð fyrir söluflokk.</span><span class="sxs-lookup"><span data-stu-id="cabb5-116">Like sales orders, quotations can be created for a specific item or, when item number is not known or does not exist at the time of quotation creation, quotations can be created for a sales category.</span></span>  
7. <span data-ttu-id="cabb5-117">Í reitinn vara skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="cabb5-117">In the Item field, enter or select a value.</span></span>
8. <span data-ttu-id="cabb5-118">Í reitinn vara skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="cabb5-118">In the Item field, type a value.</span></span>
9. <span data-ttu-id="cabb5-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="cabb5-119">Close the page.</span></span>
10. <span data-ttu-id="cabb5-120">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="cabb5-120">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="cabb5-121">Ef gildir viðskiptasamningar fyrir vöruna sem valin er á línunni eru til, verð og afslátt sjálfkrafa afritaðir í tilboðslínunni.</span><span class="sxs-lookup"><span data-stu-id="cabb5-121">If there are valid trade agreements for the item selected on the line, the applicable price and discounts will be automatically copied to the quotation line.</span></span> <span data-ttu-id="cabb5-122">Gangið úr skugga um að svæði einnigs inniheldur gildi og hægt er einnig að færa afsláttargildi ef óskað er.</span><span class="sxs-lookup"><span data-stu-id="cabb5-122">Make sure that the Unit price field contains a value and you can also enter discount values if you want to.</span></span>  
11. <span data-ttu-id="cabb5-123">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="cabb5-123">Click Save.</span></span>
12. <span data-ttu-id="cabb5-124">Smellið á „Sölutilboð“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="cabb5-124">On the Action Pane, click Sales quotation.</span></span>
13. <span data-ttu-id="cabb5-125">Smellið á „Samtölur“.</span><span class="sxs-lookup"><span data-stu-id="cabb5-125">Click Totals.</span></span>
14. <span data-ttu-id="cabb5-126">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cabb5-126">Click OK.</span></span>
15. <span data-ttu-id="cabb5-127">Smellið á „Sölutilboðslína“.</span><span class="sxs-lookup"><span data-stu-id="cabb5-127">Click Sales quotation line.</span></span>
16. <span data-ttu-id="cabb5-128">Smellið á „Verð“.</span><span class="sxs-lookup"><span data-stu-id="cabb5-128">Click Prices.</span></span>
    * <span data-ttu-id="cabb5-129">Í síðunni Keyra verðhermingu er hægt að gera tilraunir með leiðrétta áætlaðar tekjur eða arðsemisgreiningu af tilboði byggt á viðkomandi einingarverð, afsláttarupphæð, afsláttarprósenta, heildarupphæð, framlegð, eða framlegðarhlutfall.</span><span class="sxs-lookup"><span data-stu-id="cabb5-129">In the Run price simulation page you can experiment with adjusting the expected revenue or profitability of your quotation based on the desired unit price, discount amount, discount percentage, total amount, margin, or contribution ratio.</span></span>   <span data-ttu-id="cabb5-130">Þegar þú ert ánægður með tölur, nota sem tillaga fyrir tilboðslínuna og verðtengd svæði verða uppfærðar samkvæmt því.</span><span class="sxs-lookup"><span data-stu-id="cabb5-130">When you are satisfied with the target figures, you apply the suggestion to the quotation line, and its price-related fields will be updated accordingly.</span></span>  
    * <span data-ttu-id="cabb5-131">Þú getur stofna eins margar verðherming sem óskað er.</span><span class="sxs-lookup"><span data-stu-id="cabb5-131">Y ou can create as many price simulations as you wish.</span></span> <span data-ttu-id="cabb5-132">Þegar smellt er á Nýtt, eru verðskilyrði úr núgildandi tilboðslínu afrituð á síðu.</span><span class="sxs-lookup"><span data-stu-id="cabb5-132">When you click New, the price conditions from the current quotation line are copied to the page.</span></span> <span data-ttu-id="cabb5-133">Síðan er hægt að breyta gildi í hvaða verð-tengdum svæðum í þau sem eru markmiðið.</span><span class="sxs-lookup"><span data-stu-id="cabb5-133">You can then modify values in any of the price-related fields to the target ones.</span></span> <span data-ttu-id="cabb5-134">Breyting á eitt af svæðunum kveikir endurútreikningur í öllum öðrum svæðum.</span><span class="sxs-lookup"><span data-stu-id="cabb5-134">A change in one of the fields will trigger recalculation in all the other fields.</span></span> <span data-ttu-id="cabb5-135">Til þess að reikna út framlegð sölu og framlegðarhlutfall, verður einingarkostnað afurðar að vera þekkt.</span><span class="sxs-lookup"><span data-stu-id="cabb5-135">In order for the system to calculate the sales margin and contribution ratio, the product's unit cost has to be known.</span></span> <span data-ttu-id="cabb5-136">Notið flipann hermunarverð fyrir ítarlegri yfirlit yfir upphaflegt verð, lögð til breytingar og áhrif þeirra á tilboðssamtölur.</span><span class="sxs-lookup"><span data-stu-id="cabb5-136">Use the Simulated prices tab for a detailed view of the original prices, proposed changes and their effect on the quotation totals.</span></span>   <span data-ttu-id="cabb5-137">Almenna reglan er að þegar hermun stillir nýja upphæð er notað í tilboðslínunni, endurreiknar kerfið og færir inn nýtt gildi í reitinn einingarverð.</span><span class="sxs-lookup"><span data-stu-id="cabb5-137">As a general rule, when a simulation that sets a new amount is applied to the quotation line, the system recalculates and enters a new value in the Unit price field.</span></span> <span data-ttu-id="cabb5-138">Ef hermunina er byggð á nýja framlegð eða nýtt framlegðarhlutfall, er aðeins nettóupphæð svæðið er uppfært og einingarverð er autt.</span><span class="sxs-lookup"><span data-stu-id="cabb5-138">If the simulation is based on a new margin or a new contribution ratio, only the Net amount field is updated, and the Unit price is blank.</span></span> <span data-ttu-id="cabb5-139">Í báðum tilvikum afsláttum sem voru í tilboðslínunni fyrir hermun verður eytt.</span><span class="sxs-lookup"><span data-stu-id="cabb5-139">In both cases, any discounts that were on the quotation line before simulation will be deleted.</span></span>  
17. <span data-ttu-id="cabb5-140">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="cabb5-140">Close the page.</span></span>
18. <span data-ttu-id="cabb5-141">Smellið á „Tilboð“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="cabb5-141">On the Action Pane, click Quotation.</span></span>
19. <span data-ttu-id="cabb5-142">Smellið á „Senda tilboð“.</span><span class="sxs-lookup"><span data-stu-id="cabb5-142">Click Send quotation.</span></span>
20. <span data-ttu-id="cabb5-143">Velja skal Já í svæðinu Prenta tilboðið.</span><span class="sxs-lookup"><span data-stu-id="cabb5-143">Select Yes in the Print quotation field.</span></span>
21. <span data-ttu-id="cabb5-144">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cabb5-144">Click OK.</span></span>
    * <span data-ttu-id="cabb5-145">Skýrslan getur tekið mínútu til að mynda.</span><span class="sxs-lookup"><span data-stu-id="cabb5-145">The report may take a minute to generate.</span></span> <span data-ttu-id="cabb5-146">Ekki að loka síðunni fyrr en það hefur verið gert.</span><span class="sxs-lookup"><span data-stu-id="cabb5-146">Don’t close the page until it does so.</span></span>  
22. <span data-ttu-id="cabb5-147">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="cabb5-147">Close the page.</span></span>

## <a name="update-a-sales-quotation"></a><span data-ttu-id="cabb5-148">Uppfæra sölutilboð</span><span class="sxs-lookup"><span data-stu-id="cabb5-148">Update a sales quotation</span></span>
1. <span data-ttu-id="cabb5-149">Smellið á „Fylgja eftir“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="cabb5-149">On the Action Pane, click Follow up.</span></span>
2. <span data-ttu-id="cabb5-150">Smellt er á umbreyta í viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="cabb5-150">Click Convert to customer.</span></span>
3. <span data-ttu-id="cabb5-151">Í reitinn Reikningur viðskiptavinar skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="cabb5-151">In the Customer account field, type a value.</span></span>
4. <span data-ttu-id="cabb5-152">Smella skal á athuga.</span><span class="sxs-lookup"><span data-stu-id="cabb5-152">Click Check.</span></span>
    * <span data-ttu-id="cabb5-153">Gangið úr skugga um að þú sjáir skilaboð um að fært inn í lykilnúmerið er frjálst til notkunar.</span><span class="sxs-lookup"><span data-stu-id="cabb5-153">Make sure you see a message that the account number you typed in is free to use.</span></span>  
5. <span data-ttu-id="cabb5-154">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cabb5-154">Click OK.</span></span>
    * <span data-ttu-id="cabb5-155">Kerfið hefur nú stofnað nýjan viðskiptavinalykil fyrir viðfang á tilboðinu.</span><span class="sxs-lookup"><span data-stu-id="cabb5-155">The system has now created a new customer account for the prospect on the quotation.</span></span>  
6. <span data-ttu-id="cabb5-156">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="cabb5-156">Close the page.</span></span>
7. <span data-ttu-id="cabb5-157">Smellið á „Fylgja eftir“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="cabb5-157">On the Action Pane, click Follow up.</span></span>
8. <span data-ttu-id="cabb5-158">Smellið á „Staðfesta“.</span><span class="sxs-lookup"><span data-stu-id="cabb5-158">Click Confirm.</span></span>
9. <span data-ttu-id="cabb5-159">Í reitinn Ástæða skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="cabb5-159">In the Reason field, enter or select a value.</span></span>
10. <span data-ttu-id="cabb5-160">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="cabb5-160">Click OK.</span></span>
11. <span data-ttu-id="cabb5-161">Smellið á „Almennt“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="cabb5-161">On the Action Pane, click General.</span></span>
12. <span data-ttu-id="cabb5-162">Smellið á „Sölupantanir“.</span><span class="sxs-lookup"><span data-stu-id="cabb5-162">Click Sales orders.</span></span>
13. <span data-ttu-id="cabb5-163">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="cabb5-163">Close the page.</span></span>


