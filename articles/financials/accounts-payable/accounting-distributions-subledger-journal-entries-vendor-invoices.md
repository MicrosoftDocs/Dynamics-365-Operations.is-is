---
title: "Dreifing á fjárhagsupphæð og færslur færslubókar undirfjárhags fyrir reikningur lánardrottins"
description: "Dreifingar á fjárhagsupphæð eru notaðar til að skilgreina hvernig gert verður grein fyrir upphæð, eins og hvernig kostnaður, skatta eða gjöld verður að teknir með á reikningi lánardrottins. Hvert upphæð sem verður að vera teknir með þegar reikningur lánardrottins er skráð mun hafa eina eða fleiri dreifingar á fjárhagsupphæð."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 00550b4e3fa52108533c516d7ae1de0454c065ec
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a><span data-ttu-id="32803-104">Dreifing á fjárhagsupphæð og færslur færslubókar undirfjárhags fyrir reikningur lánardrottins</span><span class="sxs-lookup"><span data-stu-id="32803-104">Accounting distributions and subledger journal entries for vendor invoices</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="32803-105">Dreifingar á fjárhagsupphæð eru notaðar til að skilgreina hvernig gert verður grein fyrir upphæð, eins og hvernig kostnaður, skatta eða gjöld verður að teknir með á reikningi lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="32803-106">Hvert upphæð sem verður að vera teknir með þegar reikningur lánardrottins er skráð mun hafa eina eða fleiri dreifingar á fjárhagsupphæð.</span><span class="sxs-lookup"><span data-stu-id="32803-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

<a name="accounting-distributions"></a><span data-ttu-id="32803-107">Dreifing á fjárhagsupphæðum</span><span class="sxs-lookup"><span data-stu-id="32803-107">Accounting distributions</span></span> 
-------------------------

<span data-ttu-id="32803-108">Hægt er að nota eftirfarandi hnappanna í   síðunni reikningur lánardrottins til að skoða og mögulega breyta, dreifingar á fjárhagsupphæð síða fyrir hverja upphæð á reikningi lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="32803-109">**Dreifa fjárhæðir** - Skoða og breyta þeim dreifing á fjárhagsupphæð fyrir einstakar línur og allar  undirlínur, svo sem skatta eða gjöld.</span><span class="sxs-lookup"><span data-stu-id="32803-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="32803-110">Einnig er hægt að skoða og breyta dreifingar á fjárhagsupphæð fyrir línu undirstig beint í frá síðunni VSK-færsla eða síðunni Gjaldfærslur.</span><span class="sxs-lookup"><span data-stu-id="32803-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="32803-111">Breyta upphæðum í haus lánardrottnareiknings, svo sem gjöldum eða sléttuðum gjaldeyrisupphæðum.</span><span class="sxs-lookup"><span data-stu-id="32803-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="32803-112">Breyta línuupphæðum lánardrottnareikninga.</span><span class="sxs-lookup"><span data-stu-id="32803-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="32803-113">**Skoða dreifingu** - Skoða dreifingu á fjárhagsupphæð fyrir allar línur skjals.</span><span class="sxs-lookup"><span data-stu-id="32803-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="32803-114">Ekki er hægt að breyta dreifingu fjárhagsupphæða í þessu yfirliti.</span><span class="sxs-lookup"><span data-stu-id="32803-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="32803-115">Skoða hausupplýsingar og línuupphæðir.</span><span class="sxs-lookup"><span data-stu-id="32803-115">View header and line amounts.</span></span>

<span data-ttu-id="32803-116">Ef lánardrottinsreikningnum vísar til innkaupapöntunar, er hægt að skipta og breyta dreifingar á fjárhagsupphæð fyrir línur sem innihalda vörur sem ekki eru í birgðum.</span><span class="sxs-lookup"><span data-stu-id="32803-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="32803-117">Ef reikningslínu lánardrottinsins tilvísun til innkaupapöntunarlínu, er einnig hægt að eyða fjárhagsupphæð.</span><span class="sxs-lookup"><span data-stu-id="32803-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="32803-118">Ekki er hægt að skipta eða eyða línum fyrir gjöld, skatt, og línuafslætti.</span><span class="sxs-lookup"><span data-stu-id="32803-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="32803-119">Hægt er að breyta fjárhagslyklinum, en ekki er hægt að breyta upphæðum eða prósentum.</span><span class="sxs-lookup"><span data-stu-id="32803-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="32803-120">Ef yfirlínu inniheldur vöru sem er ekki í birgðum og fjárhagsupphæð skipt, undirstig verður að skipta línunni sjálfkrafa til að jafna fjárhagsvíddir yfirlínu.</span><span class="sxs-lookup"><span data-stu-id="32803-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="32803-121">Dreifingar á fjárhagsupphæð fyrir línu undirstig getur ekki auk skipta eða eytt, en eftir uppsetningu á undirstig línu, gæti verið hægt að breyta fjárhagslykil fyrir fjárhagsupphæð undirstig línu.</span><span class="sxs-lookup"><span data-stu-id="32803-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="32803-122">Dreifing upphæða</span><span class="sxs-lookup"><span data-stu-id="32803-122">Distributing amounts</span></span>
<span data-ttu-id="32803-123">Þegar reikningur lánardrottins verður hverri upphæð dreift á eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="32803-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="32803-124">Gerð reikningslínu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="32803-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="32803-125">Forgangsröð sem ákvarðar hvaðan aðallykill er birtur</span><span class="sxs-lookup"><span data-stu-id="32803-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="32803-126">Forgangsröð sem ákvarðar hvaða fjárhagsvídd sjálfgefna er birt</span><span class="sxs-lookup"><span data-stu-id="32803-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="32803-127">Afurð í birgðum</span><span class="sxs-lookup"><span data-stu-id="32803-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="32803-128">Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="32803-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="32803-129">Svæði aðallykils þegar útgjöld Innkaupa fyrir afurð er valinn í Bókunarsíðu.</span><span class="sxs-lookup"><span data-stu-id="32803-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="32803-130">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="32803-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="32803-131">Nota sjálfgefin gildi fjárhagsvídda á reikningi lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32803-132">Innkaupategund eða afurð sem er ekki í birgðum</span><span class="sxs-lookup"><span data-stu-id="32803-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="32803-133">Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínu lánardrottinsins vísar í innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="32803-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="32803-134">Svæði aðallykils þegar útgjöld Innkaupa fyrir kostnaður er valinn í Bókunarsíðu.</span><span class="sxs-lookup"><span data-stu-id="32803-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="32803-135">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="32803-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="32803-136">Ef aðallykils er úthlutunarlykill er að nota sjálfgefna gildið úr skilgreiningu úthlutunar lykil.</span><span class="sxs-lookup"><span data-stu-id="32803-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="32803-137">Nota sjálfgefin gildi fjárhagsvídda á reikningi lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="32803-138">Nota fjárhagsvíddargildi reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="32803-139">Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</span><span class="sxs-lookup"><span data-stu-id="32803-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="32803-140">Eign</span><span class="sxs-lookup"><span data-stu-id="32803-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="32803-141">Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínu lánardrottinsins vísar í innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="32803-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="32803-142">Ef Kaup er valinn í svæðinu gerð Færslu í skjámyndinni reikningur Lánardrottins, er svæði aðallykils þegar Kaup eru valdar merktur í síðan bókunarregla eigna.</span><span class="sxs-lookup"><span data-stu-id="32803-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="32803-143">Ef leiðrétting kaupa er valinn í svæðinu gerð Færslu í skjámyndinni reikningur Lánardrottins, er svæði aðallykils þegar leiðrétting kaupa eru valdar merktur í síðan bókunarregla eigna.</span><span class="sxs-lookup"><span data-stu-id="32803-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="32803-144">Nota lykilsdreifingar fyrir innkaupapöntunarlínu, ef reikningslínan vísar í innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="32803-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="32803-145">Nota fjárhagsvíddargildi reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="32803-146">Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</span><span class="sxs-lookup"><span data-stu-id="32803-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32803-147">Verk sem eru skilgreind í reikningslínu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="32803-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="32803-148">Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínan vísar í innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="32803-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="32803-149">Ef Staða er valin í Bókunarkostnað - vörusvæði í síðunni verkflokkur, er svæðið aðallykill þegar Kostnaður er valinn í síðunni uppsetning fjárhagsbókunar.</span><span class="sxs-lookup"><span data-stu-id="32803-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="32803-150">Ef hagnaður og tap er valin í Bókunarkostnað - vörusvæði í síðunni verkflokkur, er svæðið aðallykill þegar kostnaður - afurð er valinn í síðunni uppsetning fjárhagsbókunar.</span><span class="sxs-lookup"><span data-stu-id="32803-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="32803-151">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="32803-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="32803-152">Línuafsláttur</span><span class="sxs-lookup"><span data-stu-id="32803-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="32803-153">Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínan vísar í innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="32803-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="32803-154">Svæði aðallykils þegar afsláttur er valinn í Bókunarsíðu.</span><span class="sxs-lookup"><span data-stu-id="32803-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="32803-155">Ef aðallykill fyrir afslátt er ekki skilgreint í bókunarreglu, dreifing á fjárhagsupphæð heildarverðs á innkaupapöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="32803-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="32803-156">Ef reikningslínan vísar innkaupapöntunarlínu, nota dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="32803-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="32803-157">Nota fjárhagsvíddir úr dreifingar á fjárhagsupphæð fyrir heildarverð á reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="32803-158">Nota gildi fjárhagsvídda fyrir reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="32803-159">Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</span><span class="sxs-lookup"><span data-stu-id="32803-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32803-160">Innkaup, gjald fært inn í verð og afsláttur flipi innkaupapöntunarlínunnar</span><span class="sxs-lookup"><span data-stu-id="32803-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="32803-161">Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínan vísar í innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="32803-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="32803-162">Dreifing á fjárhagsupphæð útvíkkað verð á innkaupapöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="32803-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="32803-163">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="32803-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="32803-164">Nota fjárhagsvíddir úr dreifingar á fjárhagsupphæð fyrir heildarverð á reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="32803-165">Línugjald</span><span class="sxs-lookup"><span data-stu-id="32803-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="32803-166">Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínan vísar í innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="32803-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="32803-167">Ef fjárhagslykillinn er valinn í svæðinu gerð debets í skjámynd gjaldakóði, svæði debet Lykils í síðunni gjaldakóðar.</span><span class="sxs-lookup"><span data-stu-id="32803-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="32803-168">Ef afurð er valin í reitnum gerð debets í    skjámyndina gjaldakóðar, dreifing á fjárhagsupphæð fyrir heildarverð á innkaupapöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="32803-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="32803-169">Ef viðskiptavinur/lánardrottinn er valinn í svæðinu gerð debets í skjámynd gjaldakóði, svæði kredit Lykils í síðunni gjaldakóðar.</span><span class="sxs-lookup"><span data-stu-id="32803-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="32803-170">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="32803-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="32803-171">Nota fjárhagsvíddir úr dreifingar á fjárhagsupphæð fyrir heildarverð á reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="32803-172">Nota fjárhagsvíddargildi reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="32803-173">Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</span><span class="sxs-lookup"><span data-stu-id="32803-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32803-174">Skattur, með eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="32803-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="32803-175">valkosturinn beita BNA skattlagningarreglum er valinn á síðunni færibreytur fjárhags.</span><span class="sxs-lookup"><span data-stu-id="32803-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="32803-176">Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínan vísar í innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="32803-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="32803-177">Dreifing á fjárhagsupphæð heildarverð eða gjöldum.</span><span class="sxs-lookup"><span data-stu-id="32803-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="32803-178">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="32803-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="32803-179">Nota fjárhagsvíddir úr dreifingar á fjárhagsupphæð fyrir heildarverð á reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="32803-180">Nota fjárhagsvíddargildi reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="32803-181">Skattur, með eftirfarandi skilyrðum:</span><span class="sxs-lookup"><span data-stu-id="32803-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="32803-182">Valkosturinn beita BNA skattlagningarreglum er hreinsaður á síðunni færibreytur fjárhags.</span><span class="sxs-lookup"><span data-stu-id="32803-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="32803-183">svæðið neysluskattur fyrir VSK-flokkur er hreinsaður á síðunni vsk-flokka.</span><span class="sxs-lookup"><span data-stu-id="32803-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="32803-184">Ef skattupphæðin er endurkræf, svæðið VSK-kröfur í í síðunni fjárhagsbókunarflokkar.</span><span class="sxs-lookup"><span data-stu-id="32803-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="32803-185">Ef skattupphæðin er endurkræf, útvíkkað verð eða dreifing á fjárhagsupphæð fyrir gjald.</span><span class="sxs-lookup"><span data-stu-id="32803-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="32803-186">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="32803-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="32803-187">Nota fjárhagsvíddir úr útvíkkað verð eða dreifingar á fjárhagsupphæð fyrir gjald á reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="32803-188">Nota fjárhagsvíddargildi reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="32803-189">Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</span><span class="sxs-lookup"><span data-stu-id="32803-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32803-190">Skattur, með eftirfarandi skilyrðum:</span><span class="sxs-lookup"><span data-stu-id="32803-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="32803-191">Valkosturinn beita BNA skattlagningarreglum er hreinsaður á síðunni færibreytur fjárhags.</span><span class="sxs-lookup"><span data-stu-id="32803-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="32803-192">neysluskattur svæði fyrir VSK-flokkur er valið í síðu VSK-flokkur.</span><span class="sxs-lookup"><span data-stu-id="32803-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="32803-193">Ef skattupphæðin er endurkræf, svæðið VSK-kröfur í í síðunni fjárhagsbókunarflokkar.</span><span class="sxs-lookup"><span data-stu-id="32803-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="32803-194">Ef skattupphæðin er ekki endurkræf, svæði útgjöld neysluskatts í síðunni fjárhagsbókunarflokkar.</span><span class="sxs-lookup"><span data-stu-id="32803-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="32803-195">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="32803-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="32803-196">Nota fjárhagsvíddir úr útvíkkað verð eða dreifingar á fjárhagsupphæð fyrir gjald á reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="32803-197">Nota fjárhagsvíddargildi reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="32803-198">Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</span><span class="sxs-lookup"><span data-stu-id="32803-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="32803-199">Gjald hauss</span><span class="sxs-lookup"><span data-stu-id="32803-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="32803-200">Ef fjárhagslykillinn er valinn í svæðinu gerð debets í skjámynd gjaldakóði, svæði debet Lykils í síðunni gjaldakóðar.</span><span class="sxs-lookup"><span data-stu-id="32803-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="32803-201">Ef viðskiptavinur/lánardrottinn er valinn í svæðinu gerð debets í skjámynd gjaldakóði, svæði kredit Lykils í síðunni gjaldakóðar.</span><span class="sxs-lookup"><span data-stu-id="32803-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="32803-202">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="32803-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="32803-203">Ef aðallykils er úthlutunarlykill er að nota sjálfgefna gildið úr skilgreiningu úthlutunar lykil.</span><span class="sxs-lookup"><span data-stu-id="32803-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="32803-204">Nota sjálfgefin sniðmátsgildi fjárhagsvídda úr reikningshaus lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="32803-205">Nota fjárhagsvíddargildi reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="32803-206">Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</span><span class="sxs-lookup"><span data-stu-id="32803-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32803-207">Haus afsláttur</span><span class="sxs-lookup"><span data-stu-id="32803-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="32803-208">Svæði aðallykils fyrir bókunargerð fyrir afslátt reikningur lánardrottins í lyklar fyrir síðuna sjálfvirk færsla.</span><span class="sxs-lookup"><span data-stu-id="32803-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="32803-209">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="32803-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="32803-210">Nota fjárhagsvíddir úr dreifingar á fjárhagsupphæð fyrir heildarverð á reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="32803-211">Nota fjárhagsvíddargildi reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="32803-212">Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</span><span class="sxs-lookup"><span data-stu-id="32803-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>

 
<a name="distributing-taxes"></a><span data-ttu-id="32803-213">Dreifing skatta</span><span class="sxs-lookup"><span data-stu-id="32803-213">Distributing taxes</span></span>
------------------

<span data-ttu-id="32803-214">Ekki er hægt að stofna dreifingu á fjárhagsupphæð fyrr en skattar hafa verið reiknaðir.</span><span class="sxs-lookup"><span data-stu-id="32803-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="32803-215">Til að reikna virðisaukaskatt, verður að ljúka eitt af eftirtöldum verkefnum í síðunni reikningur lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="32803-216">Skoða samtölu reiknings.</span><span class="sxs-lookup"><span data-stu-id="32803-216">View the invoice total.</span></span>
-   <span data-ttu-id="32803-217">Skoða VSK.</span><span class="sxs-lookup"><span data-stu-id="32803-217">View the sales tax.</span></span>
-   <span data-ttu-id="32803-218">Skoða færslubók undirfjárhags.</span><span class="sxs-lookup"><span data-stu-id="32803-218">View the subledger journal.</span></span>
-   <span data-ttu-id="32803-219">Skoða dreifingar á fjárhagsupphæð fyrir reikning lánardrottins sem er lokið.</span><span class="sxs-lookup"><span data-stu-id="32803-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="32803-220">Setja reikningur lánardrottins í bið.</span><span class="sxs-lookup"><span data-stu-id="32803-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="32803-221">Bóka reikning lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="32803-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="32803-222">Færslubækur undirfjárhags fyrir reikninga lánardrottins</span><span class="sxs-lookup"><span data-stu-id="32803-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="32803-223">Áður en reikningur lánardrottins er bókaður, er hægt að skoða alla lykilfærslu reiknings, þar á meðal debet- og kreditsniði, til að staðfesta sem reikningurinn er bókuð á rétta lykla.</span><span class="sxs-lookup"><span data-stu-id="32803-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="32803-224">Þetta yfirlit yfir alla lykilfærslu kallast færslubók undirfjárhags.</span><span class="sxs-lookup"><span data-stu-id="32803-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="32803-225">Ef færsla í undirbók er röng þegar hún er forskoðuð áður en reikningur lánardrottins eru skráðar, er hægt að breyta færslu í undirbók.</span><span class="sxs-lookup"><span data-stu-id="32803-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="32803-226">Þess í stað verður þú að breyta dreifingu á fjárhagsupphæð eða bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="32803-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="32803-227">Fjárhagsupphæðum er notuð til að skilgreina einni hlið lykilfærslu, debet eða kredit.</span><span class="sxs-lookup"><span data-stu-id="32803-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="32803-228">Mótfærslu lykilfærslu undirbókarlykils er stofnuð með því að nota bókunarreglur, eins og úr lykli lánardrottins eða skatts.</span><span class="sxs-lookup"><span data-stu-id="32803-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>






