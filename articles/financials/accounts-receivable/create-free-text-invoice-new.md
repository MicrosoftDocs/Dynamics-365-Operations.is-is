--- 
title: "Stofna reikning með frjálsum texta"
description: "Þessi grein sýnir hvernig skal stofna reikning með frjálsum texta."
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f69505f0c6137121cae92d42d052b244326c8436
ms.openlocfilehash: 2a611bdd4dd97109709ed355eb80471e27413744
ms.contentlocale: is-is
ms.lasthandoff: 06/28/2018

---

# <a name="create-a-free-text-invoice"></a><span data-ttu-id="ddca9-103">Stofna reikning með frjálsum texta</span><span class="sxs-lookup"><span data-stu-id="ddca9-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ddca9-104">Þessi grein sýnir hvernig skal stofna reikning með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="ddca9-104">This article demonstrates how to create a free text invoice.</span></span> <span data-ttu-id="ddca9-105">Fyrir þetta ferli skal nota USMF sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="ddca9-105">For this procedure, use the USMF demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="ddca9-106">Stofna reikning með frjálsum texta</span><span class="sxs-lookup"><span data-stu-id="ddca9-106">Create a free text invoice</span></span>

1. <span data-ttu-id="ddca9-107">Fara í Viðskiptakröfur > Reikningar > Allir reikningar með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="ddca9-107">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="ddca9-108">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="ddca9-108">Click New.</span></span>
3. <span data-ttu-id="ddca9-109">Í reitnum Viðskiptavinalykill skal velja gildi.</span><span class="sxs-lookup"><span data-stu-id="ddca9-109">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="ddca9-110">Reikningslykillinn verður sjálfgefið að sama lykli og notaður var fyrir viðskiptavinalykilinn.</span><span class="sxs-lookup"><span data-stu-id="ddca9-110">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="ddca9-111">Lykilstaðan byrjar á Í vinnslu ef reikningurinn hefur ekki verið bókaður.</span><span class="sxs-lookup"><span data-stu-id="ddca9-111">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="ddca9-112">Númeri reikningsins verður úthlutað þegar reikningurinn er bókaður.</span><span class="sxs-lookup"><span data-stu-id="ddca9-112">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="ddca9-113">Ef SEPA-umboð er notað verður umboð fyrir beingreiðslu sjálfkrafa fyllt út með umboði þegar viðskiptavinalykillinn er valinn.</span><span class="sxs-lookup"><span data-stu-id="ddca9-113">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="ddca9-114">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="ddca9-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ddca9-115">Í svæðinu aðallykill, skal tilgreina lykilnúmer án víddir.</span><span class="sxs-lookup"><span data-stu-id="ddca9-115">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="ddca9-116">Einnig er hægt að slá inn einn eða fleiri stafi fyrir aðallykilinn og nota uppflettingu til að finna lykilinn.</span><span class="sxs-lookup"><span data-stu-id="ddca9-116">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="ddca9-117">Þú munt færa inn víddirnar síðar í þessari handbók.</span><span class="sxs-lookup"><span data-stu-id="ddca9-117">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="ddca9-118">Stækkið flýtiflipann fyrir línuupplýsingar til að geta bætt víddum við aðallykilinn.</span><span class="sxs-lookup"><span data-stu-id="ddca9-118">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="ddca9-119">Smellið á flipann fyrir línu „Fjárhagsvíddar“.</span><span class="sxs-lookup"><span data-stu-id="ddca9-119">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="ddca9-120">Víddirnar eru aðeins ætlaðar fyrir valda línu.</span><span class="sxs-lookup"><span data-stu-id="ddca9-120">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="ddca9-121">Vsk-flokkur er fylltur út frá viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="ddca9-121">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="ddca9-122">Vsk-flokk frá aðallykli er notað ef viðskiptavinur hefur ekki vsk-flokk.</span><span class="sxs-lookup"><span data-stu-id="ddca9-122">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="ddca9-123">VSK-flokkur varanna er fylltur út sjálfgefið úr aðallykli.</span><span class="sxs-lookup"><span data-stu-id="ddca9-123">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="ddca9-124">Ef aðallykillinn hefur ekki VSK-flokk vöru verður VSK-flokkur vöru úr virðisaukaskattsfæribreytum fjárhags notaður.</span><span class="sxs-lookup"><span data-stu-id="ddca9-124">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="ddca9-125">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="ddca9-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="ddca9-126">Magnið er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="ddca9-126">The quantity is optional.</span></span>  
9. <span data-ttu-id="ddca9-127">Færið inn númer í reitnum „Einingarverð“.</span><span class="sxs-lookup"><span data-stu-id="ddca9-127">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="ddca9-128">Einingarverðið er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="ddca9-128">The unit price is optional.</span></span>  
    * <span data-ttu-id="ddca9-129">Upphæðin er reiknuð út sem magnið margfaldað með einingarverðinu.</span><span class="sxs-lookup"><span data-stu-id="ddca9-129">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="ddca9-130">Þó er hægt að hnekkja útreikningnum og slá inn aðra upphæð.</span><span class="sxs-lookup"><span data-stu-id="ddca9-130">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="ddca9-131">Smellið á „Virðisaukaskatt“ til að skoða útreiknaðan virðisaukaskatt fyrir reikninginn.</span><span class="sxs-lookup"><span data-stu-id="ddca9-131">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="ddca9-132">Á þessari síðu er hægt að skoða upphæðir virðisaukaskattsins eða hnekkja þeim á leiðréttingarflipanum.</span><span class="sxs-lookup"><span data-stu-id="ddca9-132">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="ddca9-133">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ddca9-133">Click OK.</span></span>
12. <span data-ttu-id="ddca9-134">Smellt er á Gjöld til að bæta gjaldi við reikning.</span><span class="sxs-lookup"><span data-stu-id="ddca9-134">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="ddca9-135">Í reitnum Gjaldakóði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="ddca9-135">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="ddca9-136">Í reitinn Gjöld skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="ddca9-136">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="ddca9-137">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="ddca9-137">Close the page.</span></span>
16. <span data-ttu-id="ddca9-138">Smellið á „Samtölur“ til að skoða samantekt yfir reikninga og samtölur.</span><span class="sxs-lookup"><span data-stu-id="ddca9-138">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="ddca9-139">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="ddca9-139">Click Close.</span></span>
18. <span data-ttu-id="ddca9-140">Smellið á „Bóka“ til að bóka reikninginn.</span><span class="sxs-lookup"><span data-stu-id="ddca9-140">Click Post to post the invoice.</span></span> <span data-ttu-id="ddca9-141">Hægt er að hætta við áður en bókun er framkvæmd.</span><span class="sxs-lookup"><span data-stu-id="ddca9-141">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="ddca9-142">Til að breyta tímasetningu prentunar reiknings: Velja Gildandi til að prenta hvern reikning þegar hann er uppfærður eða Velja Eftir að prenta eftir að allir reikningar hafa verið uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="ddca9-142">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="ddca9-143">Ef óskað er að breyta hvernig gerð lánamarks viðskiptavinarins er athuguð fyrir bókun, þarf að breyta gerð lánamarks.</span><span class="sxs-lookup"><span data-stu-id="ddca9-143">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="ddca9-144">Ef það á að prenta reikninginn skal velja Já.</span><span class="sxs-lookup"><span data-stu-id="ddca9-144">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="ddca9-145">Ef það á að bóka reikninginn skal velja Já.</span><span class="sxs-lookup"><span data-stu-id="ddca9-145">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="ddca9-146">Hægt er að prenta reikninga án bókunar.</span><span class="sxs-lookup"><span data-stu-id="ddca9-146">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="ddca9-147">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="ddca9-147">Click OK.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="ddca9-148">Afrita línur</span><span class="sxs-lookup"><span data-stu-id="ddca9-148">Copy lines</span></span>
<span data-ttu-id="ddca9-149">Til að afrita línur á reikningi með frjálsum texta skal velja eina eða fleiri línur og smella síðan á Afrita valdar línur.</span><span class="sxs-lookup"><span data-stu-id="ddca9-149">To copy lines on the free text invoice, select one or more lines and then click Copy selected lines.</span></span> <span data-ttu-id="ddca9-150">Þú getur tilgreint fjölda eintaka sem þú vilt gera og þú getur líka afritað athugasemdir og viðhengi.</span><span class="sxs-lookup"><span data-stu-id="ddca9-150">You can specify the number of copies that you want to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="ddca9-151">Þú getur afritað dreifingarnar eða heimilað endursköpun þeirra þegar þú bókar.</span><span class="sxs-lookup"><span data-stu-id="ddca9-151">You can copy the distributions or allow them to be recreated when you post.</span></span> <span data-ttu-id="ddca9-152">Um leið og þú afritar línurnar geturðu breytt upplýsingum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="ddca9-152">Once you copy the lines, you can edit the information as needed.</span></span> 

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="ddca9-153">Búa til reikning með frjálsum texta út frá sniðmáti</span><span class="sxs-lookup"><span data-stu-id="ddca9-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="ddca9-154">Þú getur búið til reikning með frjálsum texta út frá sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="ddca9-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="ddca9-155">Þegar þú velur Nýtt úr sniðmáti úr flipanum Reikningur getur þú valið sniðmátsnafn og viðskiptavinarlykilinn fyrir nýja reikninginn með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="ddca9-155">When you select New from template from the Invoice tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="ddca9-156">Þú getur einnig valið að gera gildi sjálfgefin, svo sem greiðsluskilmála og greiðsluaðferð frá viðskiptavininum eða notaðu gildin sem voru vistuð með sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="ddca9-156">You can also choose to default values such as the terms of payment and method of payment from the customer or use the values that were saved with the template.</span></span> <span data-ttu-id="ddca9-157">Nýr reikningur með frjálsum texta verður búinn til og þú getur breytt gildunum í þeirri reikningi.</span><span class="sxs-lookup"><span data-stu-id="ddca9-157">A new free text invoice will be created and you can edit the values in that invoice.</span></span> 


