---
title: Skilgreina líkanavörpun rafrænnar skýrslugerðar og velja gagnagjafa
description: Í þessu efnisatriði er útskýrt hvernig kerfisstjóri eða þróunaraðili rafrænnar skýrslugerðar getur valið gagnagjafa fyrir gagnalíkan rafrænnar skýrslugerðar.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fccdda3ac441630836a0d33f78eb04e9cd26d4a
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092111"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a><span data-ttu-id="52e6b-103">Skilgreina líkanavörpun rafrænnar skýrslugerðar og velja gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="52e6b-103">Define ER model mappings and select data sources for them</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="52e6b-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur valið gagnaveitur fyrir Rafræna skýrslugerð (ER) gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="52e6b-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="52e6b-105">Gagnaveita verður bundin vup einstaka íhluti fyrir valið gagnalíkan á þegar það var hannað og fylla viðskiptagögn á það gagnalíkan þegar það var keyrt.</span><span class="sxs-lookup"><span data-stu-id="52e6b-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="52e6b-106">Í þessu dæmi er valinn gagnagjafi fyrir fyrirliggjandi gagnalíkan sem hefur verið stofnað fyrir sýnisfyrirtæki, í þessu dæmi Litware, Inc. Til að ljúka þessum skrefum, þarf fyrst að ljúka við skrefin í ferlinu "Stofna nýtt gagnalíkan".</span><span class="sxs-lookup"><span data-stu-id="52e6b-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the "Create a new data model" procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="52e6b-107">Opna grunnstillingatré Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="52e6b-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="52e6b-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="52e6b-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="52e6b-109">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="52e6b-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="52e6b-110">Setja inn nýja líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="52e6b-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="52e6b-111">Veljið 'Greiðslur (einfaldað líkan)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="52e6b-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="52e6b-112">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="52e6b-112">Click Designer.</span></span>
3. <span data-ttu-id="52e6b-113">Smellt er á Varpa líkani á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="52e6b-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="52e6b-114">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-114">Click New.</span></span>
    * <span data-ttu-id="52e6b-115">Þetta stofnar nýja færslu sem mun varpa gagnalíkani á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="52e6b-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="52e6b-116">Í þessu dæmi, verður að varpa gagnalíkani í gagnagjafa fyrir viðkomandi greiðslugerð: kreditfærslu.</span><span class="sxs-lookup"><span data-stu-id="52e6b-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="52e6b-117">Mögulegt er að hanna fleiri en eina vörpun fyrir tiltekið gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="52e6b-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="52e6b-118">Til dæmis væri hægt að stofna vörpun fyrir mismunandi gerðir greiðslna, eins og fyrir beingreiðsla eða kreditfærsla.</span><span class="sxs-lookup"><span data-stu-id="52e6b-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="52e6b-119">Í þessu dæmi muntu stofna vörpun fyrir kreditfærslur.</span><span class="sxs-lookup"><span data-stu-id="52e6b-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="52e6b-120">Í reitinn Heiti skal slá inn 'CT vörpun'.</span><span class="sxs-lookup"><span data-stu-id="52e6b-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="52e6b-121">Vörpun CT</span><span class="sxs-lookup"><span data-stu-id="52e6b-121">CT mapping</span></span>  
6. <span data-ttu-id="52e6b-122">Í reitinn Lýsing skal slá inn ‚CT vörpun greiðslulíkans'.</span><span class="sxs-lookup"><span data-stu-id="52e6b-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="52e6b-123">CT vörpun greiðslulíkans</span><span class="sxs-lookup"><span data-stu-id="52e6b-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="52e6b-124">Í svæði Skilgreining skal slá inn 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="52e6b-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="52e6b-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="52e6b-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="52e6b-126">„Leysa úr“ breytir skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="52e6b-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="52e6b-127">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="52e6b-128">Skilgreina nauðsynlega gagnaveitur fyrir gildandi líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="52e6b-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="52e6b-129">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="52e6b-129">Click Designer.</span></span>
2. <span data-ttu-id="52e6b-130">Í trénu skal velja 'Dynamics 365 for Operations\Table records'.</span><span class="sxs-lookup"><span data-stu-id="52e6b-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="52e6b-131">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="52e6b-131">Click Add root.</span></span>
    * <span data-ttu-id="52e6b-132">Færið inn gagnagjafa til að hafa aðgang að greiðslufærslum.</span><span class="sxs-lookup"><span data-stu-id="52e6b-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="52e6b-133">Í reitnum Heiti skal færa inn ‚færslur'.</span><span class="sxs-lookup"><span data-stu-id="52e6b-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="52e6b-134">Færslur</span><span class="sxs-lookup"><span data-stu-id="52e6b-134">Transactions</span></span>  
5. <span data-ttu-id="52e6b-135">Í reitnum Merki skal færa inn ‚Færslur‘.</span><span class="sxs-lookup"><span data-stu-id="52e6b-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="52e6b-136">Færslur</span><span class="sxs-lookup"><span data-stu-id="52e6b-136">Transactions</span></span>  
6. <span data-ttu-id="52e6b-137">Færið inn 'Fjárhagsbókarlínur' í svæðinu Hjálp.</span><span class="sxs-lookup"><span data-stu-id="52e6b-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="52e6b-138">Fjárhagsfærslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="52e6b-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="52e6b-139">Velja skal Já í reitnum Óska eftir fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="52e6b-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="52e6b-140">Velja skal Já.</span><span class="sxs-lookup"><span data-stu-id="52e6b-140">Select Yes.</span></span>  
8. <span data-ttu-id="52e6b-141">Í reitnum Tafla skal færa inn ‚LedgerJournalTrans‘.</span><span class="sxs-lookup"><span data-stu-id="52e6b-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="52e6b-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="52e6b-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="52e6b-143">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-143">Click OK.</span></span>
    * <span data-ttu-id="52e6b-144">Veljið töflunni LedgerJournalTrans sem gagnaveita fyrir gildandi gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="52e6b-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="52e6b-145">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="52e6b-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="52e6b-146">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="52e6b-146">Click Add.</span></span>
    * <span data-ttu-id="52e6b-147">Smella á bæta Við til að bæta við nýju reiknuðu svæði.</span><span class="sxs-lookup"><span data-stu-id="52e6b-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="52e6b-148">Í reitnum Heiti skal færa inn '$EndToEndID'.</span><span class="sxs-lookup"><span data-stu-id="52e6b-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="52e6b-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="52e6b-149">$EndToEndID</span></span>  
13. <span data-ttu-id="52e6b-150">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="52e6b-150">Click Edit formula.</span></span>
14. <span data-ttu-id="52e6b-151">Veljið 'String\CONCATENATE', í trénu.</span><span class="sxs-lookup"><span data-stu-id="52e6b-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="52e6b-152">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="52e6b-152">Click Add function.</span></span>
16. <span data-ttu-id="52e6b-153">Í trénu skal víkka út „Færslur“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="52e6b-154">Veljið 'Transactions\Voucher', í trénu.</span><span class="sxs-lookup"><span data-stu-id="52e6b-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="52e6b-155">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="52e6b-155">Click Add data source.</span></span>
19. <span data-ttu-id="52e6b-156">Í svæði Formúla slá inn 'CONCATENATE(Transactions.Voucher, "-", '.</span><span class="sxs-lookup"><span data-stu-id="52e6b-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="52e6b-157">Sláðu inn [ , "-", ] aftast í formúlu.</span><span class="sxs-lookup"><span data-stu-id="52e6b-157">Type [ , "-", ] at the end of the formula.</span></span>  
20. <span data-ttu-id="52e6b-158">Í trénu skal velja „String/TEXT“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="52e6b-159">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="52e6b-159">Click Add function.</span></span>
22. <span data-ttu-id="52e6b-160">Veljið 'Transactions\Record-ID(RecId)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="52e6b-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="52e6b-161">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="52e6b-161">Click Add data source.</span></span>
24. <span data-ttu-id="52e6b-162">Í svæði Formúla slá inn 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span><span class="sxs-lookup"><span data-stu-id="52e6b-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="52e6b-163">Sláðu inn [))] aftast í formúlu.</span><span class="sxs-lookup"><span data-stu-id="52e6b-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="52e6b-164">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-164">Click Save.</span></span>
    * <span data-ttu-id="52e6b-165">Gangið úr skugga um að engar villur hafi fundist fyrir formúluna sem er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="52e6b-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="52e6b-166">Sjá flipann VILLUR undir ritilstýringu formúlu.</span><span class="sxs-lookup"><span data-stu-id="52e6b-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="52e6b-167">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="52e6b-167">Close the page.</span></span>
27. <span data-ttu-id="52e6b-168">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-168">Click OK.</span></span>
    * <span data-ttu-id="52e6b-169">Bættu reiknuð svæði við þennan gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="52e6b-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="52e6b-170">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="52e6b-170">Click Add.</span></span>
    * <span data-ttu-id="52e6b-171">Smella á bæta Við til að bæta við nýju reiknuðu svæði.</span><span class="sxs-lookup"><span data-stu-id="52e6b-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="52e6b-172">Í reitnum Heiti skal færa inn ‚$Amount'.</span><span class="sxs-lookup"><span data-stu-id="52e6b-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="52e6b-173">$Amount</span><span class="sxs-lookup"><span data-stu-id="52e6b-173">$Amount</span></span>  
30. <span data-ttu-id="52e6b-174">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="52e6b-174">Click Edit formula.</span></span>
31. <span data-ttu-id="52e6b-175">Í trénu skal víkka út „Færslur“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="52e6b-176">Veljið 'Transactions\Debit(AmountCurDebit)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="52e6b-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="52e6b-177">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="52e6b-177">Click Add data source.</span></span>
34. <span data-ttu-id="52e6b-178">Í svæði Formúla slá inn 'Transactions.AmountCurDebit - '.</span><span class="sxs-lookup"><span data-stu-id="52e6b-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="52e6b-179">Sláðu inn [ - ] aftast í formúlu.</span><span class="sxs-lookup"><span data-stu-id="52e6b-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="52e6b-180">Í trénu, veljið 'Transactions\Credit(AmountCurCredit)'.</span><span class="sxs-lookup"><span data-stu-id="52e6b-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="52e6b-181">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="52e6b-181">Click Add data source.</span></span>
37. <span data-ttu-id="52e6b-182">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-182">Click Save.</span></span>
38. <span data-ttu-id="52e6b-183">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="52e6b-183">Close the page.</span></span>
39. <span data-ttu-id="52e6b-184">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-184">Click OK.</span></span>
    * <span data-ttu-id="52e6b-185">Þetta bætir $Amount reiknaða svæðið við vilda gagnaveitu fyrir núverandi gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="52e6b-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="52e6b-186">Í trénu skal velja „Færslur\$Upphæð“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="52e6b-187">Í trénu skal víkka út „Færslur“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="52e6b-188">Í tré skal víkka eða draga saman „Færslur\$Upphæð“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="52e6b-189">Í tré skal víkka eða draga saman 'Transactions'.</span><span class="sxs-lookup"><span data-stu-id="52e6b-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="52e6b-190">Í trénu skal velja 'Dynamics 365 for Operations\Table records'.</span><span class="sxs-lookup"><span data-stu-id="52e6b-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="52e6b-191">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="52e6b-191">Click Add root.</span></span>
    * <span data-ttu-id="52e6b-192">Færið inn gagnaveitu til að hafa aðgang að upplýsingar bankareiknings fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="52e6b-192">Enter this data source to access the company's bank account details.</span></span>  
46. <span data-ttu-id="52e6b-193">Í reitnum Heiti skal færa inn 'BankAccount'.</span><span class="sxs-lookup"><span data-stu-id="52e6b-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="52e6b-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="52e6b-194">BankAccount</span></span>  
47. <span data-ttu-id="52e6b-195">Færið inn 'Bankareikning' í svæðinu Merki.</span><span class="sxs-lookup"><span data-stu-id="52e6b-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="52e6b-196">Bankareikningur</span><span class="sxs-lookup"><span data-stu-id="52e6b-196">Bank Account</span></span>  
48. <span data-ttu-id="52e6b-197">Færið inn 'Bankareikning' í svæðinu Hjálp.</span><span class="sxs-lookup"><span data-stu-id="52e6b-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="52e6b-198">Bankareikningur</span><span class="sxs-lookup"><span data-stu-id="52e6b-198">Bank Account</span></span>  
49. <span data-ttu-id="52e6b-199">Velja skal Já í reitnum Óska eftir fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="52e6b-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="52e6b-200">Velja skal Já.</span><span class="sxs-lookup"><span data-stu-id="52e6b-200">Select Yes.</span></span>  
50. <span data-ttu-id="52e6b-201">Í reitnum Tafla skal færa inn 'BankAccountTable'.</span><span class="sxs-lookup"><span data-stu-id="52e6b-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="52e6b-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="52e6b-202">BankAccountTable</span></span>  
51. <span data-ttu-id="52e6b-203">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-203">Click OK.</span></span>
    * <span data-ttu-id="52e6b-204">Veljið BankAccountTable töfluna sem gagnaveita fyrir gildandi gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="52e6b-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="52e6b-205">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="52e6b-205">Click Add root.</span></span>
    * <span data-ttu-id="52e6b-206">Færið inn gagnaveitu til að hafa aðgang að upplýsingar um fyrirmæli fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="52e6b-206">Enter this data source to access the company's requisites.</span></span>  
53. <span data-ttu-id="52e6b-207">Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.</span><span class="sxs-lookup"><span data-stu-id="52e6b-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="52e6b-208">Fyrirt.  </span><span class="sxs-lookup"><span data-stu-id="52e6b-208">Company</span></span>  
54. <span data-ttu-id="52e6b-209">Í reitinn Merki skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="52e6b-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="52e6b-210">Fyrirtækið</span><span class="sxs-lookup"><span data-stu-id="52e6b-210">Company information</span></span>  
55. <span data-ttu-id="52e6b-211">Í reitinn Hjálp skal færa inn ‚Fyrirtækjaupplýsingar‘.</span><span class="sxs-lookup"><span data-stu-id="52e6b-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="52e6b-212">Fyrirtækið</span><span class="sxs-lookup"><span data-stu-id="52e6b-212">Company information</span></span>  
56. <span data-ttu-id="52e6b-213">Velja skal Já í reitnum Óska eftir fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="52e6b-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="52e6b-214">Velja skal Já.</span><span class="sxs-lookup"><span data-stu-id="52e6b-214">Select Yes.</span></span>  
57. <span data-ttu-id="52e6b-215">Í reitinn Tafla skal færa inn ‚CompanyInfo‘.</span><span class="sxs-lookup"><span data-stu-id="52e6b-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="52e6b-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="52e6b-216">CompanyInfo</span></span>  
58. <span data-ttu-id="52e6b-217">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-217">Click OK.</span></span>
    * <span data-ttu-id="52e6b-218">Veljið CompanyInfo töfluna sem gagnaveita fyrir gildandi gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="52e6b-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="52e6b-219">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="52e6b-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="52e6b-220">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="52e6b-220">Click Add root.</span></span>
    * <span data-ttu-id="52e6b-221">Setja inn reiknuð svæði sem nýja gagnaveita.</span><span class="sxs-lookup"><span data-stu-id="52e6b-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="52e6b-222">Í svæðið Heiti, færðu in 'ProcessingDateTime'.</span><span class="sxs-lookup"><span data-stu-id="52e6b-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="52e6b-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="52e6b-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="52e6b-224">Í svæðið Merki skal færa inn ' Vinnsludagsetning & tími '.</span><span class="sxs-lookup"><span data-stu-id="52e6b-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="52e6b-225">Vinnsludagsetning & tími</span><span class="sxs-lookup"><span data-stu-id="52e6b-225">Processing date & time</span></span>  
63. <span data-ttu-id="52e6b-226">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="52e6b-226">Click Edit formula.</span></span>
64. <span data-ttu-id="52e6b-227">Í tré skal velja 'Date/time\SESSIONNOW'.</span><span class="sxs-lookup"><span data-stu-id="52e6b-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="52e6b-228">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="52e6b-228">Click Add function.</span></span>
66. <span data-ttu-id="52e6b-229">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-229">Click Save.</span></span>
67. <span data-ttu-id="52e6b-230">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="52e6b-230">Close the page.</span></span>
68. <span data-ttu-id="52e6b-231">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-231">Click OK.</span></span>
    * <span data-ttu-id="52e6b-232">Bæta ProcessingDateTime reiknaða svæðisins við sem gagnaveita fyrir gildandi gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="52e6b-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="52e6b-233">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="52e6b-233">Click Save.</span></span>
70. <span data-ttu-id="52e6b-234">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="52e6b-234">Close the page.</span></span>
71. <span data-ttu-id="52e6b-235">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="52e6b-235">Close the page.</span></span>
72. <span data-ttu-id="52e6b-236">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="52e6b-236">Close the page.</span></span>

