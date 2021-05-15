---
title: Stofna nýja verðsamning
description: Þetta ferli sýnir hvernig á að stofna viðskiptasamningur þar sem þú skráir inn nýtt söluverð afurðar sem þú hefur ákvarðað með tilteknum viðskiptavin.
author: omulvad
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TradeNonStockedConversion, TradeNonStockedConversionChangeWizard, TradeNonStockedConversionCheckWorksheet, TradeNonStockedConversionWizard, TradeNonStockedRegister
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 592b3d0265a3be92a5a823c6aabdd40b4e3f0a27
ms.sourcegitcommit: 890a0b3eb3c1f48d786b0789e5bb8641e0b8455e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5919942"
---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="55c7f-103">Stofna nýja verðsamning</span><span class="sxs-lookup"><span data-stu-id="55c7f-103">Create a new trade agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="55c7f-104">Þetta ferli sýnir hvernig á að stofna viðskiptasamningur þar sem þú skráir inn nýtt söluverð afurðar sem þú hefur ákvarðað með tilteknum viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="55c7f-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="55c7f-105">Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.</span><span class="sxs-lookup"><span data-stu-id="55c7f-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="55c7f-106">Ef þú ert að nota eigin gögn, þarftu áður en byrjað er að þessari handbók að ganga úr skugga um að heiti færslubókar fyrir Verðsamningur er til staðar þar sem Sjálfgefinn tengsl er stillt á "Verð (sala)".</span><span class="sxs-lookup"><span data-stu-id="55c7f-106">If you're using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to "Price (sales)".</span></span>

## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="55c7f-107">Stofna og bóka nýja færslubók verðsamnings</span><span class="sxs-lookup"><span data-stu-id="55c7f-107">Create and post a new trade agreement journal</span></span>

1. <span data-ttu-id="55c7f-108">Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala og markaðsstarf > Verð og afslættir > Færslubækur verðsamninga**.</span><span class="sxs-lookup"><span data-stu-id="55c7f-108">Go to **Navigation pane > Modules > Sales and marketing > Prices and discounts > Trade agreement journals**.</span></span>
2. <span data-ttu-id="55c7f-109">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="55c7f-109">Click **New**.</span></span>
3. <span data-ttu-id="55c7f-110">Í reitnum **Heiti** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="55c7f-110">In the **Name** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="55c7f-111">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="55c7f-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="55c7f-112">Á **Aðgerðasvæði** er smellt á **Línur**.</span><span class="sxs-lookup"><span data-stu-id="55c7f-112">On **Action Pane**, click **Lines**.</span></span>
6. <span data-ttu-id="55c7f-113">Í reitnum **Reikningskóði** velurðu „Tafla“.</span><span class="sxs-lookup"><span data-stu-id="55c7f-113">In the **Account code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="55c7f-114">Í þessu dæmi er verið að uppfæra verð fyrir tiltekinn viðskiptavin, sem þýðir að þarf að velja Töflu.</span><span class="sxs-lookup"><span data-stu-id="55c7f-114">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="55c7f-115">Ef verið var að uppfæra listaverð afurðar, myndirðu velja „Allt“, þannig að nýtt verð myndi gilda fyrir alla viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="55c7f-115">If you were updating the product's list price, you would select 'All', so that the new price is valid for all customers.</span></span> <span data-ttu-id="55c7f-116">Ef þú værir að sundurgreina verð milli ólíkra hluta viðskiptavinar þá myndiðu velja Flokk.</span><span class="sxs-lookup"><span data-stu-id="55c7f-116">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="55c7f-117">Til að velja Flokk, verður að hafa að sett upp verðflokka viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="55c7f-117">To select Group, you must have set up Customer price groups.</span></span>  

7. <span data-ttu-id="55c7f-118">Í reitnum **Val á lykli** skal smella á fellilistahnappinn til að opna uppflettinguna.</span><span class="sxs-lookup"><span data-stu-id="55c7f-118">In the **Account selection** field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="55c7f-119">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="55c7f-119">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="55c7f-120">Í reitnum **Vörukóði** velurðu „Tafla“.</span><span class="sxs-lookup"><span data-stu-id="55c7f-120">In the **Item code** field, select 'Table'.</span></span>
    
    <span data-ttu-id="55c7f-121">Þegar þú færir inn viðskiptasamning af gerðinni „Verð (sala)“ verðurðu að velja einungis „Tafla“ í reitnum **Vörukóði**.</span><span class="sxs-lookup"><span data-stu-id="55c7f-121">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the **Item code** field.</span></span> <span data-ttu-id="55c7f-122">Þetta er vegna þess að verð með raungildi og má ekki vera það sama fyrir allar afurðir eða flokka afurða.</span><span class="sxs-lookup"><span data-stu-id="55c7f-122">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>
    
10. <span data-ttu-id="55c7f-123">Í reitnum **Vöruvensl** skal smella á fellilistahnappinn til að opna uppflettinguna.</span><span class="sxs-lookup"><span data-stu-id="55c7f-123">In the **Item relation** field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="55c7f-124">Á listanum, veljið afurð sem á að taka með í samningnum.</span><span class="sxs-lookup"><span data-stu-id="55c7f-124">In the list, select the product you want to include in the agreement.</span></span> <span data-ttu-id="55c7f-125">Skrifaðu athugasemd um hvaða vöru sem var valin.</span><span class="sxs-lookup"><span data-stu-id="55c7f-125">Make a note of which product you've selected.</span></span>  
12. <span data-ttu-id="55c7f-126">Í reitinn **Frá** slærðu inn lágmarksmagn.</span><span class="sxs-lookup"><span data-stu-id="55c7f-126">In the **From** field, enter a minimum quantity.</span></span>
    - <span data-ttu-id="55c7f-127">Ef viðskiptavinur þarf að panta lágmarksmagn áður en þeir verða gjaldgengir fyrir nýtt verð, þá þarf að tilgreina það magn hér.</span><span class="sxs-lookup"><span data-stu-id="55c7f-127">If the customer has to order a minimum quantity before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    - <span data-ttu-id="55c7f-128">Færið inn gildi í svæðinu **Til** til að tilgreina hámarksmagn og ef farið er umfram það mun verð í samningnum ekki vera gilt.</span><span class="sxs-lookup"><span data-stu-id="55c7f-128">Enter a value in the **To** field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="55c7f-129">Ef þú ert að bjóða verð og afslætti sem byggja á mörgum skilum í magni, þá skaltu tilgreina öll skil í magni sem par af lágmarks- og hámarksmagni í reitunum **Frá** og **Til**, í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="55c7f-129">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the **From** and **To** fields respectively.</span></span>
13. <span data-ttu-id="55c7f-130">Í reitinn **Upphæð í gjaldmiðli** skaltu færa inn verð.</span><span class="sxs-lookup"><span data-stu-id="55c7f-130">In the **Amount in currency field**, enter a price.</span></span>
14. <span data-ttu-id="55c7f-131">Undir hlutanum **Upplýsingar**, í reitnum **Frá dags.**, skaltu skrá dags. sem þessi samningur verður ekki gildur frá.</span><span class="sxs-lookup"><span data-stu-id="55c7f-131">Under the **Details** section, in the **From date** field, enter a date from which this agreement will be valid.</span></span>
15. <span data-ttu-id="55c7f-132">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="55c7f-132">Click **Save**.</span></span>
16. <span data-ttu-id="55c7f-133">Smelltu á **Villuleita**.</span><span class="sxs-lookup"><span data-stu-id="55c7f-133">Click **Validate**.</span></span>
17. <span data-ttu-id="55c7f-134">Smelltu á **Villuleita valdar línur**.</span><span class="sxs-lookup"><span data-stu-id="55c7f-134">Click **Validate selected lines**.</span></span>
18. <span data-ttu-id="55c7f-135">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="55c7f-135">Click **OK**.</span></span>
19. <span data-ttu-id="55c7f-136">Smelltu á **Bóka.**</span><span class="sxs-lookup"><span data-stu-id="55c7f-136">Click **Post**.</span></span>
20. <span data-ttu-id="55c7f-137">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="55c7f-137">Click **OK**.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="55c7f-138">Skoða viðskiptasamninga fyrir afurð</span><span class="sxs-lookup"><span data-stu-id="55c7f-138">View trade agreements for a product</span></span>

1. <span data-ttu-id="55c7f-139">Farðu í **Skoðunarrúða > Kerfiseiningar > Afurðaupplýsingastjórnun > Afurðir > Útgefnar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="55c7f-139">Go to **Navigation pane > Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="55c7f-140">Finna og velja vöru sem verð hefur nýlega verið uppfært verð, á listanum.</span><span class="sxs-lookup"><span data-stu-id="55c7f-140">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="55c7f-141">Í **Aðgerðasvæðinu** smellirðu á **Selja**.</span><span class="sxs-lookup"><span data-stu-id="55c7f-141">On the **Action Pane**, click **Sell**.</span></span>
4. <span data-ttu-id="55c7f-142">Smelltu á **Skoða viðskiptasamninga**.</span><span class="sxs-lookup"><span data-stu-id="55c7f-142">Click **View trade agreements**.</span></span>
    
    <span data-ttu-id="55c7f-143">Fara yfir nákvæmar upplýsingar um verð viðskiptasamnings sem var nýverið stofnaður.</span><span class="sxs-lookup"><span data-stu-id="55c7f-143">Review the details of the price trade agreement you have just created.</span></span>

5. <span data-ttu-id="55c7f-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="55c7f-144">Close the page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="55c7f-145">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="55c7f-145">Additional resources</span></span>

### <a name="whitepaper"></a><span data-ttu-id="55c7f-146">Hvítbók</span><span class="sxs-lookup"><span data-stu-id="55c7f-146">Whitepaper</span></span>

<span data-ttu-id="55c7f-147">Frekari upplýsingar er að hlaða niður eftirfarandi hvítbók (skrifuð til að styðja AX2012, en gildir einnig fyrir Dynamics 365 Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="55c7f-147">For more information, download the following white paper (written to support AX2012, but still applies for Dynamics 365 Supply Chain Management)</span></span>

- [<span data-ttu-id="55c7f-148">Viðskiptasamningar</span><span class="sxs-lookup"><span data-stu-id="55c7f-148">Trade agreements</span></span>](https://download.microsoft.com/download/0/2/9/02972c8b-0159-4936-a3ef-1e64252b2d2f/TradeAgreementsInAX.pdf)

### <a name="community-blogs"></a><span data-ttu-id="55c7f-149">Samfélagsblogg</span><span class="sxs-lookup"><span data-stu-id="55c7f-149">Community blogs</span></span>

- [<span data-ttu-id="55c7f-150">Söluverð í Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="55c7f-150">Sales prices in Dynamics 365 for Finance and Operations</span></span>](https://financefunction.tech/2018/11/14/sales-prices-in-dynamics-365-for-finance-and-operations/#sales_price_in_trade_agreements)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]