---
title: Stofna reikning með frjálsum texta
description: Í þessu efnisatriði er útskýrt hvernig á að stofna reikninga með frjálsum texta.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 7ccc652a407e9ed09c2ffffd3c86ff5070d6399b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217507"
---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="e5519-103">Stofna reikning með frjálsum texta</span><span class="sxs-lookup"><span data-stu-id="e5519-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5519-104">Í þessu efnisatriði er útskýrt hvernig á að stofna reikninga með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="e5519-104">This topic explains how to create free text invoices.</span></span> <span data-ttu-id="e5519-105">Fyrir ferlið skal nota **USMF** sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="e5519-105">For the procedure, use the **USMF** demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="e5519-106">Stofna textareikning</span><span class="sxs-lookup"><span data-stu-id="e5519-106">Create a free text invoice</span></span>

1. <span data-ttu-id="e5519-107">Fara í **Viðskiptakröfur (eða fjárhag) \> Reikningar \> Allir reikningar með frjálsum texta**.</span><span class="sxs-lookup"><span data-stu-id="e5519-107">Go to **Accounts receivable (or Sales Ledger) \> Invoices \> All free text invoices**.</span></span>
2. <span data-ttu-id="e5519-108">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e5519-108">Select **New**.</span></span>
3. <span data-ttu-id="e5519-109">Í reitnum **Viðskiptavinalykill** skal velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e5519-109">In the **Customer account** field, select a value.</span></span>

    * <span data-ttu-id="e5519-110">Sjálfgefið er að lykill sem valinn er sem viðskiptavinalykill er notaður sem reikningslykill.</span><span class="sxs-lookup"><span data-stu-id="e5519-110">By default, the account that is selected as the customer account is used as the invoice account.</span></span>
    * <span data-ttu-id="e5519-111">Ef reikningurinn er ekki bókaður byrjar bókhaldsstaðan á **Í vinnslu**.</span><span class="sxs-lookup"><span data-stu-id="e5519-111">If the invoice isn't posted, the accounting status starts with **In process**.</span></span>
    * <span data-ttu-id="e5519-112">Númeri reikningsins verður úthlutað þegar reikningurinn er bókaður.</span><span class="sxs-lookup"><span data-stu-id="e5519-112">The invoice number will be assigned when the invoice is posted.</span></span>
    * <span data-ttu-id="e5519-113">Ef verið er að nota umboð fyrir sameiginlegt evrópskt greiðslusvæði (SEPA) er umboðið fyrir beingreiðslu sjálfkrafa fært inn þegar viðskiptavinalykill er valinn.</span><span class="sxs-lookup"><span data-stu-id="e5519-113">If you're using Single Euro Payments Area (SEPA) mandates, the direct debit mandate is automatically entered when you select the customer account.</span></span>

4. <span data-ttu-id="e5519-114">Sláið inn gildi í reitnum **Lýsing**.</span><span class="sxs-lookup"><span data-stu-id="e5519-114">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="e5519-115">Í reitnum **Aðallykill** skal tilgreina lykilnúmer sem er ekki með víddir.</span><span class="sxs-lookup"><span data-stu-id="e5519-115">In the **Main account** field, specify an account number that doesn't have dimensions.</span></span> <span data-ttu-id="e5519-116">Víddir verða færðar inn síðar í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="e5519-116">You will enter dimensions later in this topic.</span></span>

    <span data-ttu-id="e5519-117">Einnig er hægt að færa inn einn eða fleiri stafi fyrir aðallykilinn og nota uppflettingu til að finna lykilinn.</span><span class="sxs-lookup"><span data-stu-id="e5519-117">You can also enter one or more characters for the main account, and use the lookup to find the account.</span></span>

6. <span data-ttu-id="e5519-118">Veljið flýtiflipann **Línuupplýsingar** til að bæta víddum við aðallykilinn.</span><span class="sxs-lookup"><span data-stu-id="e5519-118">Select the **Line details** FastTab to add dimensions to the main account.</span></span>
7. <span data-ttu-id="e5519-119">Veljið flipann **Fjárhagsvíddalína**.</span><span class="sxs-lookup"><span data-stu-id="e5519-119">Select the **Financial dimensions line** tab.</span></span>

    * <span data-ttu-id="e5519-120">Víddirnar eru aðeins ætlaðar fyrir valda línu.</span><span class="sxs-lookup"><span data-stu-id="e5519-120">The dimensions are for the selected line only.</span></span>
    * <span data-ttu-id="e5519-121">VSK-flokkurinn er fylltur út frá viðskiptavininum.</span><span class="sxs-lookup"><span data-stu-id="e5519-121">The sales tax group is filled in from the customer.</span></span> <span data-ttu-id="e5519-122">Ef viðskiptavinurinn er ekki með VSK-flokk er VSK-flokkur aðallykils notaður.</span><span class="sxs-lookup"><span data-stu-id="e5519-122">If the customer doesn't have a sales tax group, the sales tax group from the main account is used.</span></span>
    * <span data-ttu-id="e5519-123">VSK-flokkur vöru er fylltur út frá aðallyklinum.</span><span class="sxs-lookup"><span data-stu-id="e5519-123">The items sales tax group is filled in from the main account.</span></span> <span data-ttu-id="e5519-124">Ef aðallykill er ekki með VSK-flokk vöru, þá er VSK-flokkur vörunnar sem tilgreindur er í færibreytum virðisaukaskatts í fjárhag notaður.</span><span class="sxs-lookup"><span data-stu-id="e5519-124">If the main account doesn't have an item sales tax group, the item sales tax group that is specified in the sales tax parameters in General ledger is used.</span></span>

8. <span data-ttu-id="e5519-125">Valfrjálst: Sláið inn númer í reitinn **Magn**.</span><span class="sxs-lookup"><span data-stu-id="e5519-125">Optional: In the **Quantity** field, enter a number.</span></span>
9. <span data-ttu-id="e5519-126">Valfrjálst: Sláið inn númer í reitinn **Einingarverð**.</span><span class="sxs-lookup"><span data-stu-id="e5519-126">Optional: In the **Unit price** field, enter a number.</span></span>

    <span data-ttu-id="e5519-127">Upphæðin er reiknuð út sem magnið margfaldað með einingarverðinu.</span><span class="sxs-lookup"><span data-stu-id="e5519-127">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="e5519-128">Hins vegar er hægt að hnekkja útreikningnum með því að færa inn upphæð.</span><span class="sxs-lookup"><span data-stu-id="e5519-128">However, you can override that calculation by entering an amount.</span></span>

10. <span data-ttu-id="e5519-129">Veljið **Virðisaukaskattur** til að skoða reiknaðan virðisaukaskatt fyrir reikninginn.</span><span class="sxs-lookup"><span data-stu-id="e5519-129">Select **Sales tax** to view the sales tax that is calculated for the invoice.</span></span>

    <span data-ttu-id="e5519-130">Hægt er að skoða upphæðir virðisaukaskatts á þessari síðu, eða hnekkja upphæðunum á flipanum **Leiðrétting**.</span><span class="sxs-lookup"><span data-stu-id="e5519-130">You can view the sales tax amounts on this page, or you can override the amounts on the **Adjustment** tab.</span></span>

11. <span data-ttu-id="e5519-131">Veldu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e5519-131">Select **OK**.</span></span>
12. <span data-ttu-id="e5519-132">Veljið **Gjöld** til að bæta gjaldi við reikninginn.</span><span class="sxs-lookup"><span data-stu-id="e5519-132">Select **Charges** to add a charge to the invoice.</span></span>
13. <span data-ttu-id="e5519-133">Sláið inn gildi í reitinn **Gjaldakóði**.</span><span class="sxs-lookup"><span data-stu-id="e5519-133">In the **Charges code** field, enter a value.</span></span>
14. <span data-ttu-id="e5519-134">Sláið inn númer í reitinn **Virði gjalda**.</span><span class="sxs-lookup"><span data-stu-id="e5519-134">In the **Charges value** field, enter a number.</span></span>
15. <span data-ttu-id="e5519-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e5519-135">Close the page.</span></span>
16. <span data-ttu-id="e5519-136">Veljið **Samtölur** til að skoða samantekt á reikningsupplýsingum og heildarupplýsingum.</span><span class="sxs-lookup"><span data-stu-id="e5519-136">Select **Totals** to view a summary of the invoice details and totals.</span></span>
17. <span data-ttu-id="e5519-137">Veljið **Loka**.</span><span class="sxs-lookup"><span data-stu-id="e5519-137">Select **Close**.</span></span>
18. <span data-ttu-id="e5519-138">Veljið **Bóka** til að bóka reikninginn.</span><span class="sxs-lookup"><span data-stu-id="e5519-138">Select **Post** to post the invoice.</span></span> <span data-ttu-id="e5519-139">Enn er tækifæri til að hætta við áður en bókunin er gerð.</span><span class="sxs-lookup"><span data-stu-id="e5519-139">You will still have an opportunity to cancel before you actually post.</span></span>

    * <span data-ttu-id="e5519-140">Hægt er að breyta tímasetningu á útprentun reiknings.</span><span class="sxs-lookup"><span data-stu-id="e5519-140">You can change the timing of invoice printing.</span></span> <span data-ttu-id="e5519-141">Veljið **Núgildandi** til að prenta hvern reikning þegar hann er uppfærður.</span><span class="sxs-lookup"><span data-stu-id="e5519-141">Select **Current** to print each invoice as it's updated.</span></span> <span data-ttu-id="e5519-142">Veljið **Á eftir** til að prenta þegar allir reikningar hafa verið uppfærðir.</span><span class="sxs-lookup"><span data-stu-id="e5519-142">Select **After** to print after all invoices have been updated.</span></span>
    * <span data-ttu-id="e5519-143">Til að breyta því hvernig lánamark viðskiptavinar er staðfest áður en reikningur er bókaður skal breyta gildinu í reitnum **Gerð lánamarks**.</span><span class="sxs-lookup"><span data-stu-id="e5519-143">To change how the customer's credit limit is verified before the invoice is posted, change the value in the **Credit limit type** field.</span></span>
    * <span data-ttu-id="e5519-144">Til að prenta reikninginn skal stilla valkostinn á **Já**.</span><span class="sxs-lookup"><span data-stu-id="e5519-144">To print the invoice, set the option to **Yes**.</span></span>
    * <span data-ttu-id="e5519-145">Til að bóka reikninginn skal stilla valkostinn á **Já**.</span><span class="sxs-lookup"><span data-stu-id="e5519-145">To post the invoice, set the option to **Yes**.</span></span> <span data-ttu-id="e5519-146">Hægt er að prenta reikninginn án þess að bóka hann.</span><span class="sxs-lookup"><span data-stu-id="e5519-146">You can print the invoice without posting it.</span></span>

19. <span data-ttu-id="e5519-147">Veldu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e5519-147">Select **OK**.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="e5519-148">Afrita línur</span><span class="sxs-lookup"><span data-stu-id="e5519-148">Copy lines</span></span>
<span data-ttu-id="e5519-149">Til að afrita línur á reikningi með frjálsum texta skal velja eina eða fleiri línur og velja síðan **Afrita valdar línur**.</span><span class="sxs-lookup"><span data-stu-id="e5519-149">To copy lines on a free text invoice, select one or more lines, and then select **Copy selected lines**.</span></span> <span data-ttu-id="e5519-150">Hægt er að tilgreina fjölda eintaka sem á að gera og einnig er hægt að afrita athugasemdir og viðhengi.</span><span class="sxs-lookup"><span data-stu-id="e5519-150">You can specify the number of copies to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="e5519-151">Annaðhvort er hægt að afrita dreifingarnar eða leyfa endursköpun þeirra við bókun.</span><span class="sxs-lookup"><span data-stu-id="e5519-151">You can either copy the distributions or let them be re-created when you post.</span></span>

<span data-ttu-id="e5519-152">Eftir afritun á línum er hægt að breyta upplýsingum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e5519-152">After you copy lines, you can edit the information as you require.</span></span>

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="e5519-153">Búa til reikning með frjálsum texta út frá sniðmáti</span><span class="sxs-lookup"><span data-stu-id="e5519-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="e5519-154">Þú getur búið til reikning með frjálsum texta út frá sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="e5519-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="e5519-155">Þegar **Nýtt úr sniðmáti** er valið úr flipanum **Reikningur** er hægt að velja sniðmátsheiti og viðskiptavinalykilinn fyrir nýja reikninginn með frjálsum texta.</span><span class="sxs-lookup"><span data-stu-id="e5519-155">When you select **New from template** on the **Invoice** tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="e5519-156">Sjálfgefin gildi, svo sem greiðsluskilmálar og greiðslumáti, geta sjálfkrafa verið fyllt út af viðskiptavininum, eða hægt er að nota gildin sem voru vistuð í sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="e5519-156">Default values, such as the terms of payment and method of payment, can be automatically filled in from the customer, or you can use the values that were saved in the template.</span></span>

<span data-ttu-id="e5519-157">Nýr reikningur með frjálsum texta verður búinn til og hægt er að breyta gildunum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="e5519-157">A new free text invoice is created, and you can edit the values as you require.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]