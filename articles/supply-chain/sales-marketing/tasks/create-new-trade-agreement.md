--- 
title: "Stofna nýja verðsamning"
description: "Þetta ferli sýnir hvernig á að stofna viðskiptasamningur þar sem þú skráir inn nýtt söluverð afurðar sem þú hefur ákvarðað með tilteknum viðskiptavin."
author: omulvad
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1eb7a945243387f85ec5f38cc3b969d8d030ff25
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-new-trade-agreement"></a><span data-ttu-id="c44f2-103">Stofna nýja verðsamning</span><span class="sxs-lookup"><span data-stu-id="c44f2-103">Create a new trade agreement</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c44f2-104">Þetta ferli sýnir hvernig á að stofna viðskiptasamningur þar sem þú skráir inn nýtt söluverð afurðar sem þú hefur ákvarðað með tilteknum viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="c44f2-104">This procedure shows you how to create a trade agreement where you register a new product sales price that you've agreed with a specific customer.</span></span> <span data-ttu-id="c44f2-105">Hægt er að keyra þessa ferli í sýnifyrirtækinu USMF eða í eigin gögnum.</span><span class="sxs-lookup"><span data-stu-id="c44f2-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="c44f2-106">Ef verið er að nota eigin gögn, þarftu að ganga úr skugga um áður en byrjað er að þessari handbók að á heiti færslubókar fyrir Verðsamningur er til staðar þar sem Sjálfgefinn tengsl er stillt á "Verð (sala)".</span><span class="sxs-lookup"><span data-stu-id="c44f2-106">If you’re using your own data, before you start this guide you need to make sure that a Trade agreement journal name exists where the Default relation is set to “Price (sales)”.</span></span>


## <a name="create-and-post-a-new-trade-agreement-journal"></a><span data-ttu-id="c44f2-107">Stofna og bóka nýja færslubók verðsamnings</span><span class="sxs-lookup"><span data-stu-id="c44f2-107">Create and post a new trade agreement journal</span></span>
1. <span data-ttu-id="c44f2-108">Fara í Sölu og markaðssetningu > Verð og afslætti > Færslubækur viðskiptasamninga.</span><span class="sxs-lookup"><span data-stu-id="c44f2-108">Go to Sales and marketing > Prices and discounts > Trade agreement journals.</span></span>
2. <span data-ttu-id="c44f2-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="c44f2-109">Click New.</span></span>
3. <span data-ttu-id="c44f2-110">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c44f2-110">In the Name field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="c44f2-111">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="c44f2-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="c44f2-112">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="c44f2-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="c44f2-113">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="c44f2-113">Click Lines.</span></span>
7. <span data-ttu-id="c44f2-114">Í reitnum kóði lykils er valið 'tafla'.</span><span class="sxs-lookup"><span data-stu-id="c44f2-114">In the Account code field, select 'Table'.</span></span>
    * <span data-ttu-id="c44f2-115">Í þessu dæmi er verið að uppfæra verð fyrir tiltekinn viðskiptavin, sem þýðir að þarf að velja Töflu.</span><span class="sxs-lookup"><span data-stu-id="c44f2-115">In this example, you're updating the price for a specific customer, which means you need to choose Table.</span></span> <span data-ttu-id="c44f2-116">Ef verið var að uppfæra listaverð afurðar, myndirðu velja Allt, þannig að ný verði gildir fyrir alla viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="c44f2-116">If you were updating the product's list price, you would select All, so that the new price is valid for all customers.</span></span> <span data-ttu-id="c44f2-117">Ef þú værir að sundurgreina verð milli ólíkra hluta viðskiptavinar þá myndiðu velja Flokk.</span><span class="sxs-lookup"><span data-stu-id="c44f2-117">If you were differentiating prices among different customer segments, then you would select Group.</span></span> <span data-ttu-id="c44f2-118">Til að velja Flokk, verður að hafa að sett upp verðflokka viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="c44f2-118">To select Group, you must have set up Customer price groups.</span></span>  
8. <span data-ttu-id="c44f2-119">Í reitnum Val á lykli skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c44f2-119">In the Account selection field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="c44f2-120">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="c44f2-120">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="c44f2-121">Í reitnum vörukóði er valið ‚Tafla‘.</span><span class="sxs-lookup"><span data-stu-id="c44f2-121">In the Item code field, select 'Table'.</span></span>
    * <span data-ttu-id="c44f2-122">Þegar þú færir inn viðskiptasamningur af gerðinni 'Verð (sala) verður einungis að velja Tafla í vörukóðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="c44f2-122">When you are entering a trade agreement of type 'Price (sales)', you must only select 'Table' in the Item code field.</span></span> <span data-ttu-id="c44f2-123">Þetta er vegna þess að verð með raungildi og má ekki vera það sama fyrir allar afurðir eða flokka afurða.</span><span class="sxs-lookup"><span data-stu-id="c44f2-123">This is because a price is an absolute value and cannot be same for all products or a group of products.</span></span>  
11. <span data-ttu-id="c44f2-124">Í reitnum Vöruvensl skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c44f2-124">In the Item relation field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="c44f2-125">Á listanum, veljið afurð sem á að taka með í samningnum.</span><span class="sxs-lookup"><span data-stu-id="c44f2-125">In the list, select the product you want to include in the agreement.</span></span>
    * <span data-ttu-id="c44f2-126">Skrifaðu athugasemd um hvaða vöru sem var valin.</span><span class="sxs-lookup"><span data-stu-id="c44f2-126">Make a note of which product you've selected.</span></span>  
13. <span data-ttu-id="c44f2-127">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="c44f2-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="c44f2-128">Í reitinn Frá skal slá inn lágmarksmagn.</span><span class="sxs-lookup"><span data-stu-id="c44f2-128">In the From field, enter a minimum quantity.</span></span>
    * <span data-ttu-id="c44f2-129">Ef viðskiptavinur þarf að panta lágmarksmagn áður en þeir verða gjaldgengir fyrir nýtt verð, þá þarf að tilgreina það magn hér.</span><span class="sxs-lookup"><span data-stu-id="c44f2-129">If the customer has to order a minimum quantity  before they can qualify for the new price, then you need to specify that quantity here.</span></span>  
    * <span data-ttu-id="c44f2-130">Færið inn gildi í svæðinu Til, til að tilgreina hámarksmagn og ef farið er umfram það mun verðið á samningnum ekki vera gilt.</span><span class="sxs-lookup"><span data-stu-id="c44f2-130">Enter a value in the To field to specify the maximum quantity above which the agreement's price will not be valid.</span></span> <span data-ttu-id="c44f2-131">Ef þú ert að bjóða verð og afslætti sem byggir á mörgum hléum í magni, þá skaltu tilgreina hvern magnsvina sem par af lágmarks- og hámarksmagni í 'Frá' og '‘Til svæði, í þessari röð.</span><span class="sxs-lookup"><span data-stu-id="c44f2-131">If you offer prices and discounts based on multiple quantity breaks, then specify each quantity bracket as a pair of minimum and maximum quantity in the 'From' and 'To' fields respectively.</span></span>  
15. <span data-ttu-id="c44f2-132">Færa inn verð í svæðinu Upphæð í gjaldmiðli</span><span class="sxs-lookup"><span data-stu-id="c44f2-132">In the Amount in currency field, enter a price.</span></span>
16. <span data-ttu-id="c44f2-133">Í dagsetningarsvæði Frá, færið inn dagsetningu sem þessi samningur gildir uppfrá.</span><span class="sxs-lookup"><span data-stu-id="c44f2-133">In the From date field, enter a date from which this agreement will be valid.</span></span>
17. <span data-ttu-id="c44f2-134">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="c44f2-134">Click Save.</span></span>
18. <span data-ttu-id="c44f2-135">Smella á Villuleita.</span><span class="sxs-lookup"><span data-stu-id="c44f2-135">Click Validate.</span></span>
19. <span data-ttu-id="c44f2-136">Smella á Villuleita valdar línur.</span><span class="sxs-lookup"><span data-stu-id="c44f2-136">Click Validate selected lines.</span></span>
20. <span data-ttu-id="c44f2-137">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c44f2-137">Click OK.</span></span>
21. <span data-ttu-id="c44f2-138">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="c44f2-138">Click Post.</span></span>
22. <span data-ttu-id="c44f2-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c44f2-139">Click OK.</span></span>

## <a name="view-trade-agreements-for-a-product"></a><span data-ttu-id="c44f2-140">Skoða viðskiptasamninga fyrir afurð</span><span class="sxs-lookup"><span data-stu-id="c44f2-140">View trade agreements for a product</span></span>
1. <span data-ttu-id="c44f2-141">Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.</span><span class="sxs-lookup"><span data-stu-id="c44f2-141">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="c44f2-142">Finna og velja vöru sem verð hefur nýlega verið uppfært verð, á listanum.</span><span class="sxs-lookup"><span data-stu-id="c44f2-142">In the list, find and select the product whose price you have just updated.</span></span>
3. <span data-ttu-id="c44f2-143">Í aðgerðasvæðinu er smellt á selja.</span><span class="sxs-lookup"><span data-stu-id="c44f2-143">On the Action Pane, click Sell.</span></span>
4. <span data-ttu-id="c44f2-144">Smellt er á Skoða viðskiptasamninga.</span><span class="sxs-lookup"><span data-stu-id="c44f2-144">Click View trade agreements.</span></span>
    * <span data-ttu-id="c44f2-145">Fara yfir nákvæmar upplýsingar um verð viðskiptasamnings sem var nýverið stofnaður.</span><span class="sxs-lookup"><span data-stu-id="c44f2-145">Review the details of the price trade agreement you have just created.</span></span>    
5. <span data-ttu-id="c44f2-146">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c44f2-146">Close the page.</span></span>


