---
title: Dreifing á fjárhagsupphæð og færslur færslubókar undirfjárhags fyrir reikningur lánardrottins
description: Dreifingar á fjárhagsupphæð eru notaðar til að skilgreina hvernig gert verður grein fyrir upphæð, eins og hvernig kostnaður, skatta eða gjöld verður að teknir með á reikningi lánardrottins. Hvert upphæð sem verður að vera teknir með þegar reikningur lánardrottins er skráð mun hafa eina eða fleiri dreifingar á fjárhagsupphæð.
author: abruer
manager: AnnBe
ms.date: 08/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendEditInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 26891
ms.assetid: 93dc608a-b5b4-4ec3-83c2-618e3d80a583
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f8e38e6a571bb7f08b32548bcb4af823807a4340
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837567"
---
# <a name="accounting-distributions-and-subledger-journal-entries-for-vendor-invoices"></a><span data-ttu-id="3c9de-104">Dreifing á fjárhagsupphæð og færslur færslubókar undirfjárhags fyrir reikningur lánardrottins</span><span class="sxs-lookup"><span data-stu-id="3c9de-104">Accounting distributions and subledger journal entries for vendor invoices</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c9de-105">Dreifingar á fjárhagsupphæð eru notaðar til að skilgreina hvernig gert verður grein fyrir upphæð, eins og hvernig kostnaður, skatta eða gjöld verður að teknir með á reikningi lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-105">Accounting distributions are used to define how an amount will be accounted for, such as how the expense, tax, or charges will be accounted for on a vendor invoice.</span></span> <span data-ttu-id="3c9de-106">Hvert upphæð sem verður að vera teknir með þegar reikningur lánardrottins er skráð mun hafa eina eða fleiri dreifingar á fjárhagsupphæð.</span><span class="sxs-lookup"><span data-stu-id="3c9de-106">Every amount that must be accounted for when the vendor invoice is journalized will have one or more accounting distributions.</span></span> 

<a name="accounting-distributions"></a><span data-ttu-id="3c9de-107">Dreifing á fjárhagsupphæðum</span><span class="sxs-lookup"><span data-stu-id="3c9de-107">Accounting distributions</span></span> 
-------------------------

<span data-ttu-id="3c9de-108">Hægt er að nota eftirfarandi hnappanna í   síðunni reikningur lánardrottins til að skoða og mögulega breyta, dreifingar á fjárhagsupphæð síða fyrir hverja upphæð á reikningi lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-108">You can use the following buttons in the Vendor invoice page to view, and possibly modify, the accounting distributions for each amount on the vendor invoice.</span></span>
-   <span data-ttu-id="3c9de-109">**Dreifa upphæðum** – Skoða og breyta fjárhagsupphæðum fyrir einstakar línur og allar undirlínur, svo sem skatta eða gjöld.</span><span class="sxs-lookup"><span data-stu-id="3c9de-109">**Distribute amounts** – View and modify the accounting distributions for an individual line and any child lines, such as taxes or charges.</span></span> <span data-ttu-id="3c9de-110">Einnig er hægt að skoða og breyta dreifingar á fjárhagsupphæð fyrir línu undirstig beint í frá síðunni VSK-færsla eða síðunni Gjaldfærslur.</span><span class="sxs-lookup"><span data-stu-id="3c9de-110">You can also view and modify the accounting distributions for the child line directly from the Sales tax transactions page or the Charges transactions page.</span></span>
    -   <span data-ttu-id="3c9de-111">Breyta upphæðum í haus lánardrottnareiknings, svo sem gjöldum eða sléttuðum gjaldeyrisupphæðum.</span><span class="sxs-lookup"><span data-stu-id="3c9de-111">Modify vendor invoice header amounts, such as charges or currency rounding amounts.</span></span>
    -   <span data-ttu-id="3c9de-112">Breyta línuupphæðum lánardrottnareikninga.</span><span class="sxs-lookup"><span data-stu-id="3c9de-112">Modify vendor invoice line amounts.</span></span>
-   <span data-ttu-id="3c9de-113">**Skoða dreifingu** - Skoða dreifingu á fjárhagsupphæð fyrir allar línur skjals.</span><span class="sxs-lookup"><span data-stu-id="3c9de-113">**View distributions** – View the accounting distributions for all lines on the document.</span></span> <span data-ttu-id="3c9de-114">Ekki er hægt að breyta dreifingu fjárhagsupphæða í þessu yfirliti.</span><span class="sxs-lookup"><span data-stu-id="3c9de-114">You cannot modify the accounting distributions from this view.</span></span>
    -   <span data-ttu-id="3c9de-115">Skoða hausupplýsingar og línuupphæðir.</span><span class="sxs-lookup"><span data-stu-id="3c9de-115">View header and line amounts.</span></span>

<span data-ttu-id="3c9de-116">Ef lánardrottinsreikningnum vísar til innkaupapöntunar, er hægt að skipta og breyta dreifingar á fjárhagsupphæð fyrir línur sem innihalda vörur sem ekki eru í birgðum.</span><span class="sxs-lookup"><span data-stu-id="3c9de-116">If the vendor invoice references a purchase order, you can split and modify the accounting distributions for lines that contain an item that is not stocked.</span></span> <span data-ttu-id="3c9de-117">Ef reikningslínu lánardrottinsins tilvísun til innkaupapöntunarlínu, er einnig hægt að eyða fjárhagsupphæð.</span><span class="sxs-lookup"><span data-stu-id="3c9de-117">If the vendor invoice line does not reference a purchase order line, you can also delete an accounting distribution.</span></span> <span data-ttu-id="3c9de-118">Ekki er hægt að skipta eða eyða línum fyrir gjöld, skatt, og línuafslætti.</span><span class="sxs-lookup"><span data-stu-id="3c9de-118">You cannot split or delete lines for charges, taxes, and line discounts.</span></span> <span data-ttu-id="3c9de-119">Hægt er að breyta fjárhagslyklinum, en ekki er hægt að breyta upphæðum eða prósentum.</span><span class="sxs-lookup"><span data-stu-id="3c9de-119">You can modify the ledger account, but you cannot change the amounts or percentages.</span></span>
> [!NOTE]                                                                                                                                 
> <span data-ttu-id="3c9de-120">Ef yfirlínu inniheldur vöru sem er ekki í birgðum og fjárhagsupphæð skipt, undirstig verður að skipta línunni sjálfkrafa til að jafna fjárhagsvíddir yfirlínu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-120">If the parent line contains an item that is not stocked and the accounting distributions are split, the child line will be split automatically to match the financial dimensions of the parent line.</span></span> <span data-ttu-id="3c9de-121">Dreifingar á fjárhagsupphæð fyrir línu undirstig getur ekki auk skipta eða eytt, en eftir uppsetningu á undirstig línu, gæti verið hægt að breyta fjárhagslykil fyrir fjárhagsupphæð undirstig línu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-121">The accounting distributions for the child line cannot be additionally split or deleted, but depending on the setup of the child line, you might be able to modify the ledger account for the accounting distributions of the child line.</span></span>

## <a name="distributing-amounts"></a><span data-ttu-id="3c9de-122">Dreifing upphæða</span><span class="sxs-lookup"><span data-stu-id="3c9de-122">Distributing amounts</span></span>
<span data-ttu-id="3c9de-123">Þegar reikningur lánardrottins verður hverri upphæð dreift á eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="3c9de-123">When you enter a vendor invoice, each amount will be distributed as follows.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3c9de-124">Gerð reikningslínu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="3c9de-124">Type of vendor invoice line</span></span></th>
<th><span data-ttu-id="3c9de-125">Forgangsröð sem ákvarðar hvaðan aðallykill er birtur</span><span class="sxs-lookup"><span data-stu-id="3c9de-125">Order of priority that determines where the main account is displayed from</span></span></th>
<th><span data-ttu-id="3c9de-126">Forgangsröð sem ákvarðar hvaða fjárhagsvídd sjálfgefna er birt</span><span class="sxs-lookup"><span data-stu-id="3c9de-126">Order of priority that determines which default financial dimension is displayed</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3c9de-127">Afurð í birgðum</span><span class="sxs-lookup"><span data-stu-id="3c9de-127">Stocked product</span></span></td>
<td><ol>
<li><span data-ttu-id="3c9de-128">Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="3c9de-128">The accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-129">Svæði aðallykils þegar útgjöld Innkaupa fyrir afurð er valinn í Bókunarsíðu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-129">The Main account field when Purchase expenditure for product is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3c9de-130">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="3c9de-130">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-131">Nota sjálfgefin gildi fjárhagsvídda á reikningi lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-131">Use the default financial dimension values on the vendor invoice.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c9de-132">Innkaupategund eða afurð sem er ekki í birgðum</span><span class="sxs-lookup"><span data-stu-id="3c9de-132">A procurement category or a product that is not stocked</span></span></td>
<td><ol>
<li><span data-ttu-id="3c9de-133">Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínu lánardrottinsins vísar í innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-133">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-134">Svæði aðallykils þegar útgjöld Innkaupa fyrir kostnaður er valinn í Bókunarsíðu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-134">The Main account field when Purchase expenditure for expense is selected in the Posting page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3c9de-135">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="3c9de-135">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-136">Ef aðallykils er úthlutunarlykill er að nota sjálfgefna gildið úr skilgreiningu úthlutunar lykil.</span><span class="sxs-lookup"><span data-stu-id="3c9de-136">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="3c9de-137">Nota sjálfgefin gildi fjárhagsvídda á reikningi lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-137">Use the default financial dimension values on the vendor invoice.</span></span></li>
<li><span data-ttu-id="3c9de-138">Nota fjárhagsvíddargildi reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-138">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3c9de-139">Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-139">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c9de-140">Eign</span><span class="sxs-lookup"><span data-stu-id="3c9de-140">Fixed asset</span></span></td>
<td><ol>
<li><span data-ttu-id="3c9de-141">Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínu lánardrottinsins vísar í innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-141">The accounting distribution for the purchase order line, if the vendor invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-142">Ef Kaup er valinn í svæðinu gerð Færslu í skjámyndinni reikningur Lánardrottins, er svæði aðallykils þegar Kaup eru valdar merktur í síðan bókunarregla eigna.</span><span class="sxs-lookup"><span data-stu-id="3c9de-142">If Acquisition is selected in the Transaction type field in the Vendor invoice form, the Main account field when Acquisition is selected in the Fixed asset posting profiles page.</span></span></li>
<li><span data-ttu-id="3c9de-143">Ef leiðrétting kaupa er valinn í svæðinu gerð Færslu í skjámyndinni reikningur Lánardrottins, er svæði aðallykils þegar leiðrétting kaupa eru valdar merktur í síðan bókunarregla eigna.</span><span class="sxs-lookup"><span data-stu-id="3c9de-143">If Acquisition adjustment is selected in the Transaction type field, the Main account field when Acquisition adjustment is selected in the Fixed asset posting profiles page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3c9de-144">Nota lykilsdreifingar fyrir innkaupapöntunarlínu, ef reikningslínan vísar í innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-144">Use the account distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-145">Nota fjárhagsvíddargildi reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-145">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3c9de-146">Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-146">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c9de-147">Verk sem eru skilgreind í reikningslínu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="3c9de-147">Project defined on the vendor invoice line</span></span></td>
<td><ol>
<li><span data-ttu-id="3c9de-148">Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínan vísar í innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-148">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-149">Ef Staða er valin í Bókunarkostnað - vörusvæði í síðunni verkflokkur, er svæðið aðallykill þegar Kostnaður er valinn í síðunni uppsetning fjárhagsbókunar.</span><span class="sxs-lookup"><span data-stu-id="3c9de-149">If Balance is selected in the Post costs - item field in the Project groups page, the Main account field when Cost is selected in the Ledger posting setup page.</span></span></li>
<li><span data-ttu-id="3c9de-150">Ef hagnaður og tap er valin í Bókunarkostnað - vörusvæði í síðunni verkflokkur, er svæðið aðallykill þegar kostnaður - afurð er valinn í síðunni uppsetning fjárhagsbókunar.</span><span class="sxs-lookup"><span data-stu-id="3c9de-150">If Profit and loss is selected in the Post costs - item field in the Project groups page, the Main account field when Cost - item is selected in the Ledger posting setup page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3c9de-151">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="3c9de-151">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c9de-152">Línuafsláttur</span><span class="sxs-lookup"><span data-stu-id="3c9de-152">Line discount</span></span></td>
<td><ol>
<li><span data-ttu-id="3c9de-153">Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínan vísar í innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-153">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-154">Svæði aðallykils þegar afsláttur er valinn í Bókunarsíðu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-154">The Main account field when Discount is selected in the Posting page.</span></span></li>
<li><span data-ttu-id="3c9de-155">Ef aðallykill fyrir afslátt er ekki skilgreint í bókunarreglu, dreifing á fjárhagsupphæð heildarverðs á innkaupapöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="3c9de-155">If a main account for a discount is not defined on the posting profile, the accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3c9de-156">Ef reikningslínan vísar innkaupapöntunarlínu, nota dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="3c9de-156">If the invoice line references a purchase order line, use the accounting distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-157">Nota fjárhagsvíddir úr dreifingar á fjárhagsupphæð fyrir heildarverð á reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-157">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3c9de-158">Nota gildi fjárhagsvídda fyrir reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-158">Use the financial dimension values for the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3c9de-159">Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-159">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c9de-160">Innkaup, gjald fært inn í verð og afsláttur flipi innkaupapöntunarlínunnar</span><span class="sxs-lookup"><span data-stu-id="3c9de-160">Purchase charge, which is entered on the Price and discount tab of the purchase order line</span></span></td>
<td><ol>
<li><span data-ttu-id="3c9de-161">Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínan vísar í innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-161">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-162">Dreifing á fjárhagsupphæð útvíkkað verð á innkaupapöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="3c9de-162">The accounting distribution of the extended price on the purchase order line.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3c9de-163">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="3c9de-163">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-164">Nota fjárhagsvíddir úr dreifingar á fjárhagsupphæð fyrir heildarverð á reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-164">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c9de-165">Línugjald</span><span class="sxs-lookup"><span data-stu-id="3c9de-165">Line charge</span></span></td>
<td><ol>
<li><span data-ttu-id="3c9de-166">Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínan vísar í innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-166">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-167">Ef fjárhagslykillinn er valinn í svæðinu gerð debets í skjámynd gjaldakóði, svæði debet Lykils í síðunni gjaldakóðar.</span><span class="sxs-lookup"><span data-stu-id="3c9de-167">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="3c9de-168">Ef afurð er valin í reitnum gerð debets í    skjámyndina gjaldakóðar, dreifing á fjárhagsupphæð fyrir heildarverð á innkaupapöntunarlínunni.</span><span class="sxs-lookup"><span data-stu-id="3c9de-168">If Item is selected in the debit Type field in the Charges code form, the accounting distribution for the extended price on the purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-169">Ef viðskiptavinur/lánardrottinn er valinn í svæðinu gerð debets í skjámynd gjaldakóði, svæði kredit Lykils í síðunni gjaldakóðar.</span><span class="sxs-lookup"><span data-stu-id="3c9de-169">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3c9de-170">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="3c9de-170">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-171">Nota fjárhagsvíddir úr dreifingar á fjárhagsupphæð fyrir heildarverð á reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-171">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3c9de-172">Nota fjárhagsvíddargildi reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-172">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3c9de-173">Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-173">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c9de-174">Skattur, með eftirfarandi skilyrði:</span><span class="sxs-lookup"><span data-stu-id="3c9de-174">Tax, with the following condition:</span></span>
<ul>
<li><span data-ttu-id="3c9de-175">valkosturinn beita BNA skattlagningarreglum er valinn á síðunni færibreytur fjárhags.</span><span class="sxs-lookup"><span data-stu-id="3c9de-175">The Apply U.S. taxation rules option is selected in the General ledger parameters page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="3c9de-176">Dreifing á fjárhagsupphæð fyrir innkaupapöntunarlínuna, ef reikningslínan vísar í innkaupapöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-176">The accounting distribution for the purchase order line, if the invoice line references a purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-177">Dreifing á fjárhagsupphæð heildarverð eða gjöldum.</span><span class="sxs-lookup"><span data-stu-id="3c9de-177">The accounting distribution of the extended price or charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3c9de-178">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="3c9de-178">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-179">Nota fjárhagsvíddir úr dreifingar á fjárhagsupphæð fyrir heildarverð á reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-179">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3c9de-180">Nota fjárhagsvíddargildi reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-180">Use the financial dimension values from the vendor invoice line.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c9de-181">Skattur, með eftirfarandi skilyrðum:</span><span class="sxs-lookup"><span data-stu-id="3c9de-181">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="3c9de-182">Valkosturinn beita BNA skattlagningarreglum er hreinsaður á síðunni færibreytur fjárhags.</span><span class="sxs-lookup"><span data-stu-id="3c9de-182">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="3c9de-183">svæðið neysluskattur fyrir VSK-flokkur er hreinsaður á síðunni vsk-flokka.</span><span class="sxs-lookup"><span data-stu-id="3c9de-183">The Use tax field for the sales tax group is cleared in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="3c9de-184">Ef skattupphæðin er endurkræf, svæðið VSK-kröfur í í síðunni fjárhagsbókunarflokkar.</span><span class="sxs-lookup"><span data-stu-id="3c9de-184">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="3c9de-185">Ef skattupphæðin er endurkræf, útvíkkað verð eða dreifing á fjárhagsupphæð fyrir gjald.</span><span class="sxs-lookup"><span data-stu-id="3c9de-185">If the tax amount is not recoverable, the extended price or the accounting distribution for the charge.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3c9de-186">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="3c9de-186">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-187">Nota fjárhagsvíddir úr útvíkkað verð eða dreifingar á fjárhagsupphæð fyrir gjald á reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-187">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3c9de-188">Nota fjárhagsvíddargildi reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-188">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3c9de-189">Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-189">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c9de-190">Skattur, með eftirfarandi skilyrðum:</span><span class="sxs-lookup"><span data-stu-id="3c9de-190">Tax, with the following conditions:</span></span>
<ul>
<li><span data-ttu-id="3c9de-191">Valkosturinn beita BNA skattlagningarreglum er hreinsaður á síðunni færibreytur fjárhags.</span><span class="sxs-lookup"><span data-stu-id="3c9de-191">The Apply U.S. taxation rules option is cleared in the General ledger parameters page.</span></span></li>
<li><span data-ttu-id="3c9de-192">neysluskattur svæði fyrir VSK-flokkur er valið í síðu VSK-flokkur.</span><span class="sxs-lookup"><span data-stu-id="3c9de-192">The Use tax field for the sales tax group is selected in the Sales tax groups page.</span></span></li>
</ul></td>
<td><ol>
<li><span data-ttu-id="3c9de-193">Ef skattupphæðin er endurkræf, svæðið VSK-kröfur í í síðunni fjárhagsbókunarflokkar.</span><span class="sxs-lookup"><span data-stu-id="3c9de-193">If the tax amount is recoverable, the Sales tax receivable field in the Ledger posting groups page.</span></span></li>
<li><span data-ttu-id="3c9de-194">Ef skattupphæðin er ekki endurkræf, svæði útgjöld neysluskatts í síðunni fjárhagsbókunarflokkar.</span><span class="sxs-lookup"><span data-stu-id="3c9de-194">If the tax amount is not recoverable, the Use tax expense field in the Ledger posting groups page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3c9de-195">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="3c9de-195">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-196">Nota fjárhagsvíddir úr útvíkkað verð eða dreifingar á fjárhagsupphæð fyrir gjald á reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-196">Use the financial dimensions from the extended price or the accounting distributions for the charge on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3c9de-197">Nota fjárhagsvíddargildi reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-197">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3c9de-198">Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-198">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3c9de-199">Gjald hauss</span><span class="sxs-lookup"><span data-stu-id="3c9de-199">Header charge</span></span></td>
<td><ol>
<li><span data-ttu-id="3c9de-200">Ef fjárhagslykillinn er valinn í svæðinu gerð debets í skjámynd gjaldakóði, svæði debet Lykils í síðunni gjaldakóðar.</span><span class="sxs-lookup"><span data-stu-id="3c9de-200">If Ledger account is selected in the debit Type field in the Charges code form, the debit Account field in the Charges code page.</span></span></li>
<li><span data-ttu-id="3c9de-201">Ef viðskiptavinur/lánardrottinn er valinn í svæðinu gerð debets í skjámynd gjaldakóði, svæði kredit Lykils í síðunni gjaldakóðar.</span><span class="sxs-lookup"><span data-stu-id="3c9de-201">If Customer/Vendor is selected in the debit Type field in the Charges code form, the credit Account field in the Charges code page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3c9de-202">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="3c9de-202">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-203">Ef aðallykils er úthlutunarlykill er að nota sjálfgefna gildið úr skilgreiningu úthlutunar lykil.</span><span class="sxs-lookup"><span data-stu-id="3c9de-203">If the main account is an allocation account, use the default value from the allocation account definition.</span></span></li>
<li><span data-ttu-id="3c9de-204">Nota sjálfgefin sniðmátsgildi fjárhagsvídda úr reikningshaus lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-204">Use the financial dimension default template values from the vendor invoice header.</span></span></li>
<li><span data-ttu-id="3c9de-205">Nota fjárhagsvíddargildi reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-205">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3c9de-206">Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-206">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3c9de-207">Haus afsláttur</span><span class="sxs-lookup"><span data-stu-id="3c9de-207">Header discount</span></span></td>
<td><ol>
<li><span data-ttu-id="3c9de-208">Svæði aðallykils fyrir bókunargerð fyrir afslátt reikningur lánardrottins í lyklar fyrir síðuna sjálfvirk færsla.</span><span class="sxs-lookup"><span data-stu-id="3c9de-208">The Main account field for the Vendor invoice discount posting type in the Accounts for automatic transactions page.</span></span></li>
</ol></td>
<td><ol>
<li><span data-ttu-id="3c9de-209">Ef reikningslínan vísar innkaupapöntunarlínu, nota lykilsdreifingar fyrir innkaupapöntunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="3c9de-209">If the invoice line references a purchase order line, use the account distribution for the purchase order line.</span></span></li>
<li><span data-ttu-id="3c9de-210">Nota fjárhagsvíddir úr dreifingar á fjárhagsupphæð fyrir heildarverð á reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-210">Use the financial dimensions from the accounting distributions for the extended price on the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3c9de-211">Nota fjárhagsvíddargildi reikningslínu lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-211">Use the financial dimension values from the vendor invoice line.</span></span></li>
<li><span data-ttu-id="3c9de-212">Nota sjálfgefin gildi fjárhagsvídda frá aðallykli í bókhaldslykill síðu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-212">Use the default financial dimension values from the main account in the Chart of Accounts page.</span></span></li>
</ol></td>
</tr>
</tbody>
</table>


<a name="distributing-taxes"></a><span data-ttu-id="3c9de-213">Dreifing skatta</span><span class="sxs-lookup"><span data-stu-id="3c9de-213">Distributing taxes</span></span>
------------------

<span data-ttu-id="3c9de-214">Ekki er hægt að stofna dreifingu á fjárhagsupphæð fyrr en skattar hafa verið reiknaðir.</span><span class="sxs-lookup"><span data-stu-id="3c9de-214">Accounting distributions for taxes cannot be created until taxes are calculated.</span></span> <span data-ttu-id="3c9de-215">Til að reikna virðisaukaskatt, verður að ljúka eitt af eftirtöldum verkefnum í síðunni reikningur lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-215">To calculate sales taxes, you must complete one of the following tasks in the Vendor invoice page:</span></span>
-   <span data-ttu-id="3c9de-216">Skoða samtölu reiknings.</span><span class="sxs-lookup"><span data-stu-id="3c9de-216">View the invoice total.</span></span>
-   <span data-ttu-id="3c9de-217">Skoða VSK.</span><span class="sxs-lookup"><span data-stu-id="3c9de-217">View the sales tax.</span></span>
-   <span data-ttu-id="3c9de-218">Skoða færslubók undirfjárhags.</span><span class="sxs-lookup"><span data-stu-id="3c9de-218">View the subledger journal.</span></span>
-   <span data-ttu-id="3c9de-219">Skoða dreifingar á fjárhagsupphæð fyrir reikning lánardrottins sem er lokið.</span><span class="sxs-lookup"><span data-stu-id="3c9de-219">View accounting distributions for the complete vendor invoice.</span></span>
-   <span data-ttu-id="3c9de-220">Setja reikningur lánardrottins í bið.</span><span class="sxs-lookup"><span data-stu-id="3c9de-220">Place the vendor invoice on hold.</span></span>
-   <span data-ttu-id="3c9de-221">Bóka reikning lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="3c9de-221">Post the vendor invoice.</span></span>

## <a name="subledger-journals-for-vendor-invoices"></a><span data-ttu-id="3c9de-222">Færslubækur undirfjárhags fyrir reikninga lánardrottins</span><span class="sxs-lookup"><span data-stu-id="3c9de-222">Subledger journals for vendor invoices</span></span>
<span data-ttu-id="3c9de-223">Áður en reikningur lánardrottins er bókaður, er hægt að skoða alla lykilfærslu reiknings, þar á meðal debet- og kreditsniði, til að staðfesta sem reikningurinn er bókuð á rétta lykla.</span><span class="sxs-lookup"><span data-stu-id="3c9de-223">Before you post a vendor invoice, you can view the full accounting entry of the invoice, which includes debits and credits, to verify that the invoice is being posted to the correct accounts.</span></span> <span data-ttu-id="3c9de-224">Þetta yfirlit yfir alla lykilfærslu kallast færslubók undirfjárhags.</span><span class="sxs-lookup"><span data-stu-id="3c9de-224">This view of the full accounting entry is called a subledger journal.</span></span> 

<span data-ttu-id="3c9de-225">Ef færsla í undirbók er röng þegar hún er forskoðuð áður en reikningur lánardrottins eru skráðar, er hægt að breyta færslu í undirbók.</span><span class="sxs-lookup"><span data-stu-id="3c9de-225">If the subledger journal entry is incorrect when you preview it before you journalize the vendor invoice, you cannot modify the subledger journal entry.</span></span> <span data-ttu-id="3c9de-226">Þess í stað verður þú að breyta dreifingu á fjárhagsupphæð eða bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="3c9de-226">Instead, you must modify the accounting distributions or the posting profile.</span></span> <span data-ttu-id="3c9de-227">Fjárhagsupphæðum er notuð til að skilgreina einni hlið lykilfærslu, debet eða kredit.</span><span class="sxs-lookup"><span data-stu-id="3c9de-227">The accounting distributions are used to define one side of the accounting entry, the debit or the credit.</span></span> <span data-ttu-id="3c9de-228">Mótfærslu lykilfærslu undirbókarlykils er stofnuð með því að nota bókunarreglur, eins og úr lykli lánardrottins eða skatts.</span><span class="sxs-lookup"><span data-stu-id="3c9de-228">The offsetting subledger journal account entry is created by using the posting profiles, such as from the vendor account or tax.</span></span>





