--- 
# required metadata 
title: Stofna textareikning
description: Þessi leiðarvísir fyrir verk sýnir stofnun textareiknings.
author: mikefalkner
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: null
ms.service: dynamics-ax-applications
ms.technology: null
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: '2016-06-30'
ms.dyn365.ops.version: AX 7.0.0
---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="99f06-103">Stofna textareikning</span><span class="sxs-lookup"><span data-stu-id="99f06-103">Create a free text invoice</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="99f06-104">Þessi leiðarvísir fyrir verk sýnir stofnun textareiknings.</span><span class="sxs-lookup"><span data-stu-id="99f06-104">This task guide demonstrates creating a free text invoice.</span></span> <span data-ttu-id="99f06-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="99f06-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="99f06-106">Fara í Viðskiptakröfur > Reikningar > Allir reikningar með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="99f06-106">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="99f06-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="99f06-107">Click New.</span></span>
3. <span data-ttu-id="99f06-108">Í reitnum Viðskiptavinalykill skal velja gildi.</span><span class="sxs-lookup"><span data-stu-id="99f06-108">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="99f06-109">Reikningslykillinn verður sjálfgefið að sama lykli og notaður var fyrir viðskiptavinalykilinn.</span><span class="sxs-lookup"><span data-stu-id="99f06-109">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="99f06-110">Lykilstaðan byrjar á Í vinnslu ef reikningurinn hefur ekki verið bókaður.</span><span class="sxs-lookup"><span data-stu-id="99f06-110">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="99f06-111">Númeri reikningsins verður úthlutað þegar reikningurinn er bókaður.</span><span class="sxs-lookup"><span data-stu-id="99f06-111">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="99f06-112">Ef SEPA-umboð er notað verður umboð fyrir beingreiðslu sjálfkrafa fyllt út með umboði þegar viðskiptavinalykillinn er valinn.</span><span class="sxs-lookup"><span data-stu-id="99f06-112">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="99f06-113">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="99f06-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="99f06-114">Í svæðinu aðallykill, skal tilgreina lykilnúmer án víddir.</span><span class="sxs-lookup"><span data-stu-id="99f06-114">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="99f06-115">Einnig er hægt að slá inn einn eða fleiri stafi fyrir aðallykilinn og nota uppflettingu til að finna lykilinn.</span><span class="sxs-lookup"><span data-stu-id="99f06-115">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="99f06-116">Þú munt færa inn víddirnar síðar í þessari handbók.</span><span class="sxs-lookup"><span data-stu-id="99f06-116">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="99f06-117">Stækkið flýtiflipann fyrir línuupplýsingar til að geta bætt víddum við aðallykilinn.</span><span class="sxs-lookup"><span data-stu-id="99f06-117">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="99f06-118">Smellið á flipann fyrir línu „Fjárhagsvíddar“.</span><span class="sxs-lookup"><span data-stu-id="99f06-118">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="99f06-119">Víddirnar eru aðeins ætlaðar fyrir valda línu.</span><span class="sxs-lookup"><span data-stu-id="99f06-119">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="99f06-120">Vsk-flokkur er fylltur út frá viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="99f06-120">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="99f06-121">Vsk-flokk frá aðallykli er notað ef viðskiptavinur hefur ekki vsk-flokk.</span><span class="sxs-lookup"><span data-stu-id="99f06-121">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="99f06-122">VSK-flokkur varanna er fylltur út sjálfgefið úr aðallykli.</span><span class="sxs-lookup"><span data-stu-id="99f06-122">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="99f06-123">Ef aðallykillinn hefur ekki VSK-flokk vöru verður VSK-flokkur vöru úr virðisaukaskattsfæribreytum fjárhags notaður.</span><span class="sxs-lookup"><span data-stu-id="99f06-123">If the main account does not have a item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="99f06-124">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="99f06-124">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="99f06-125">Magnið er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="99f06-125">The quantity is optional.</span></span>  
9. <span data-ttu-id="99f06-126">Færið inn númer í reitnum „Einingarverð“.</span><span class="sxs-lookup"><span data-stu-id="99f06-126">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="99f06-127">Einingarverðið er valfrjálst.</span><span class="sxs-lookup"><span data-stu-id="99f06-127">The unit price is optional.</span></span>  
    * <span data-ttu-id="99f06-128">Upphæðin er reiknuð út sem magnið margfaldað með einingarverðinu.</span><span class="sxs-lookup"><span data-stu-id="99f06-128">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="99f06-129">Þó er hægt að hnekkja útreikningnum og slá inn aðra upphæð.</span><span class="sxs-lookup"><span data-stu-id="99f06-129">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="99f06-130">Smellið á „Virðisaukaskatt“ til að skoða útreiknaðan virðisaukaskatt fyrir reikninginn.</span><span class="sxs-lookup"><span data-stu-id="99f06-130">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="99f06-131">Á þessari síðu er hægt að skoða upphæðir virðisaukaskattsins eða hnekkja þeim á leiðréttingarflipanum.</span><span class="sxs-lookup"><span data-stu-id="99f06-131">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="99f06-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="99f06-132">Click OK.</span></span>
12. <span data-ttu-id="99f06-133">Smellt er á Gjöld til að bæta gjaldi við reikning.</span><span class="sxs-lookup"><span data-stu-id="99f06-133">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="99f06-134">Í reitnum Gjaldakóði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="99f06-134">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="99f06-135">Í reitinn Gjöld skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="99f06-135">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="99f06-136">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="99f06-136">Close the page.</span></span>
16. <span data-ttu-id="99f06-137">Smellið á „Samtölur“ til að skoða samantekt yfir reikninga og samtölur.</span><span class="sxs-lookup"><span data-stu-id="99f06-137">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="99f06-138">Smellið á „Loka“.</span><span class="sxs-lookup"><span data-stu-id="99f06-138">Click Close.</span></span>
18. <span data-ttu-id="99f06-139">Smellið á „Bóka“ til að bóka reikninginn.</span><span class="sxs-lookup"><span data-stu-id="99f06-139">Click Post to post the invoice.</span></span> <span data-ttu-id="99f06-140">Hægt er að hætta við áður en bókun er framkvæmd.</span><span class="sxs-lookup"><span data-stu-id="99f06-140">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="99f06-141">Til að breyta tímasetningu prentunar reiknings: Velja Gildandi til að prenta hvern reikning þegar hann er uppfærður eða Velja Eftir að prenta eftir að allir reikningar hafa verið uppfærðar.</span><span class="sxs-lookup"><span data-stu-id="99f06-141">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="99f06-142">Ef óskað er að breyta hvernig gerð lánamarks viðskiptavinarins er athuguð fyrir bókun, þarf að breyta gerð lánamarks.</span><span class="sxs-lookup"><span data-stu-id="99f06-142">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="99f06-143">Ef það á að prenta reikninginn skal velja Já.</span><span class="sxs-lookup"><span data-stu-id="99f06-143">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="99f06-144">Ef það á að bóka reikninginn skal velja Já.</span><span class="sxs-lookup"><span data-stu-id="99f06-144">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="99f06-145">Hægt er að prenta reikninga án bókunar.</span><span class="sxs-lookup"><span data-stu-id="99f06-145">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="99f06-146">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="99f06-146">Click OK.</span></span>

