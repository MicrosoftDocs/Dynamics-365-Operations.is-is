---
title: Skilgreina líkanavörpun rafrænnar skýrslugerðar og velja gagnagjafa
description: Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur valið gagnaveitur fyrir gagnalíkan rafrænnar skýrslugerðar.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 46dc13416aa094f33879c017c1a1815fc791409d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185107"
---
# <a name="define-er-model-mappings-and-select-data-sources-for-them"></a><span data-ttu-id="e330a-103">Skilgreina líkanavörpun rafrænnar skýrslugerðar og velja gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="e330a-103">Define ER model mappings and select data sources for them</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e330a-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur valið gagnaveitur fyrir Rafræna skýrslugerð (ER) gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="e330a-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can select data sources for an Electronic reporting (ER) data model.</span></span> <span data-ttu-id="e330a-105">Gagnaveita verður bundin vup einstaka íhluti fyrir valið gagnalíkan á þegar það var hannað og fylla viðskiptagögn á það gagnalíkan þegar það var keyrt.</span><span class="sxs-lookup"><span data-stu-id="e330a-105">The data sources will be bound to individual components of the selected data model at design time and populate business data to that data model at run-time.</span></span> <span data-ttu-id="e330a-106">Í þessu dæmi er valinn gagnagjafi fyrir fyrirliggjandi gagnalíkan sem hefur verið stofnað fyrir sýnisfyrirtæki, í þessu dæmi Litware, Inc. Til að ljúka þessum skrefum, þarf fyrst að ljúka við skrefin í ferlinu "Stofna nýtt gagnalíkan".</span><span class="sxs-lookup"><span data-stu-id="e330a-106">In this example, you will select data sources for an existing data model that has been created for sample company, Litware, Inc. To complete these steps, you must first complete the steps in the “Create a new data model” procedure.</span></span>


## <a name="open-the-electronic-reporting-configurations-tree"></a><span data-ttu-id="e330a-107">Opna grunnstillingatré Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="e330a-107">Open the Electronic Reporting configurations tree</span></span>
1. <span data-ttu-id="e330a-108">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="e330a-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e330a-109">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="e330a-109">Click Reporting configurations.</span></span>

## <a name="insert-a-new-model-mapping"></a><span data-ttu-id="e330a-110">Setja inn nýja líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="e330a-110">Insert a new model mapping</span></span>
1. <span data-ttu-id="e330a-111">Veljið 'Greiðslur (einfaldað líkan)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="e330a-111">In the tree, select 'Payments (simplified model)'.</span></span>
2. <span data-ttu-id="e330a-112">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="e330a-112">Click Designer.</span></span>
3. <span data-ttu-id="e330a-113">Smellt er á Varpa líkani á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="e330a-113">Click Map model to datasource.</span></span>
4. <span data-ttu-id="e330a-114">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e330a-114">Click New.</span></span>
    * <span data-ttu-id="e330a-115">Þetta stofnar nýja færslu sem mun varpa gagnalíkani á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="e330a-115">This will create a new record that will map the data model to data sources.</span></span> <span data-ttu-id="e330a-116">Í þessu dæmi, verður að varpa gagnalíkani í gagnagjafa fyrir viðkomandi greiðslugerð: kreditfærslu.</span><span class="sxs-lookup"><span data-stu-id="e330a-116">In this example, you will map the data model to data sources for the desired payment type: credit transfer.</span></span>     <span data-ttu-id="e330a-117">Mögulegt er að hanna fleiri en eina vörpun fyrir tiltekið gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="e330a-117">It is possible to design more than one mapping for a particular data model.</span></span> <span data-ttu-id="e330a-118">Til dæmis væri hægt að stofna vörpun fyrir mismunandi gerðir greiðslna, eins og fyrir beingreiðsla eða kreditfærsla.</span><span class="sxs-lookup"><span data-stu-id="e330a-118">For example, you could create a mapping for the different types of payments, such as for direct debit or for credit transfers.</span></span> <span data-ttu-id="e330a-119">Í þessu dæmi muntu stofna vörpun fyrir kreditfærslur.</span><span class="sxs-lookup"><span data-stu-id="e330a-119">In this example, you will create a mapping for credit transfers.</span></span>  
5. <span data-ttu-id="e330a-120">Í reitinn Heiti skal slá inn 'CT vörpun'.</span><span class="sxs-lookup"><span data-stu-id="e330a-120">In the Name field, type 'CT mapping'.</span></span>
    * <span data-ttu-id="e330a-121">Vörpun CT</span><span class="sxs-lookup"><span data-stu-id="e330a-121">CT mapping</span></span>  
6. <span data-ttu-id="e330a-122">Í reitinn Lýsing skal slá inn ‚CT vörpun greiðslulíkans'.</span><span class="sxs-lookup"><span data-stu-id="e330a-122">In the Description field, type 'Payment model mapping CT'.</span></span>
    * <span data-ttu-id="e330a-123">CT vörpun greiðslulíkans</span><span class="sxs-lookup"><span data-stu-id="e330a-123">Payment model mapping CT</span></span>  
7. <span data-ttu-id="e330a-124">Í svæði Skilgreining skal slá inn 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="e330a-124">In the Definition field, type 'CustomerCreditTransferInitiation'.</span></span>
    * <span data-ttu-id="e330a-125">CustomerCreditTransferInitiation</span><span class="sxs-lookup"><span data-stu-id="e330a-125">CustomerCreditTransferInitiation</span></span>  
8. <span data-ttu-id="e330a-126">„Leysa úr“ breytir skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="e330a-126">ResolveChanges the Definition.</span></span>
9. <span data-ttu-id="e330a-127">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e330a-127">Click Save.</span></span>

## <a name="define-required-data-sources-for-the-current-model-mapping"></a><span data-ttu-id="e330a-128">Skilgreina nauðsynlega gagnaveitur fyrir gildandi líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="e330a-128">Define required data sources for the current model mapping</span></span>
1. <span data-ttu-id="e330a-129">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="e330a-129">Click Designer.</span></span>
2. <span data-ttu-id="e330a-130">Í trénu skal velja 'Dynamics 365 for Operations\Table records'.</span><span class="sxs-lookup"><span data-stu-id="e330a-130">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
3. <span data-ttu-id="e330a-131">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="e330a-131">Click Add root.</span></span>
    * <span data-ttu-id="e330a-132">Færið inn gagnagjafa til að hafa aðgang að greiðslufærslum.</span><span class="sxs-lookup"><span data-stu-id="e330a-132">Enter this data source to access payment transactions.</span></span>  
4. <span data-ttu-id="e330a-133">Í reitnum Heiti skal færa inn ‚færslur'.</span><span class="sxs-lookup"><span data-stu-id="e330a-133">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="e330a-134">Færslur</span><span class="sxs-lookup"><span data-stu-id="e330a-134">Transactions</span></span>  
5. <span data-ttu-id="e330a-135">Í reitnum Merki skal færa inn ‚Færslur‘.</span><span class="sxs-lookup"><span data-stu-id="e330a-135">In the Label field, enter 'Transactions'.</span></span>
    * <span data-ttu-id="e330a-136">Færslur</span><span class="sxs-lookup"><span data-stu-id="e330a-136">Transactions</span></span>  
6. <span data-ttu-id="e330a-137">Færið inn 'Fjárhagsbókarlínur' í svæðinu Hjálp.</span><span class="sxs-lookup"><span data-stu-id="e330a-137">In the Help field, enter 'Ledger journal lines'.</span></span>
    * <span data-ttu-id="e330a-138">Fjárhagsfærslubókarlínur</span><span class="sxs-lookup"><span data-stu-id="e330a-138">Ledger journal lines</span></span>  
7. <span data-ttu-id="e330a-139">Velja skal Já í reitnum Óska eftir fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="e330a-139">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="e330a-140">Velja skal Já.</span><span class="sxs-lookup"><span data-stu-id="e330a-140">Select Yes.</span></span>  
8. <span data-ttu-id="e330a-141">Í reitnum Tafla skal færa inn ‚LedgerJournalTrans‘.</span><span class="sxs-lookup"><span data-stu-id="e330a-141">In the Table field, type 'LedgerJournalTrans'.</span></span>
    * <span data-ttu-id="e330a-142">LedgerJournalTrans</span><span class="sxs-lookup"><span data-stu-id="e330a-142">LedgerJournalTrans</span></span>  
9. <span data-ttu-id="e330a-143">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e330a-143">Click OK.</span></span>
    * <span data-ttu-id="e330a-144">Veljið töflunni LedgerJournalTrans sem gagnaveita fyrir gildandi gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="e330a-144">Select the LedgerJournalTrans table as a data source for the current data model.</span></span>  
10. <span data-ttu-id="e330a-145">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="e330a-145">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="e330a-146">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e330a-146">Click Add.</span></span>
    * <span data-ttu-id="e330a-147">Smella á bæta Við til að bæta við nýju reiknuðu svæði.</span><span class="sxs-lookup"><span data-stu-id="e330a-147">Click Add to add a new calculated field.</span></span>  
12. <span data-ttu-id="e330a-148">Í reitnum Heiti skal færa inn '$EndToEndID'.</span><span class="sxs-lookup"><span data-stu-id="e330a-148">In the Name field, type '$EndToEndID'.</span></span>
    * <span data-ttu-id="e330a-149">$EndToEndID</span><span class="sxs-lookup"><span data-stu-id="e330a-149">$EndToEndID</span></span>  
13. <span data-ttu-id="e330a-150">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="e330a-150">Click Edit formula.</span></span>
14. <span data-ttu-id="e330a-151">Veljið 'String\CONCATENATE', í trénu.</span><span class="sxs-lookup"><span data-stu-id="e330a-151">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="e330a-152">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="e330a-152">Click Add function.</span></span>
16. <span data-ttu-id="e330a-153">Í trénu skal víkka út „Færslur“.</span><span class="sxs-lookup"><span data-stu-id="e330a-153">In the tree, expand 'Transactions'.</span></span>
17. <span data-ttu-id="e330a-154">Veljið 'Transactions\Voucher', í trénu.</span><span class="sxs-lookup"><span data-stu-id="e330a-154">In the tree, select 'Transactions\Voucher'.</span></span>
18. <span data-ttu-id="e330a-155">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="e330a-155">Click Add data source.</span></span>
19. <span data-ttu-id="e330a-156">Í svæði Formúla slá inn 'CONCATENATE(Transactions.Voucher, "-", '.</span><span class="sxs-lookup"><span data-stu-id="e330a-156">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", '.</span></span>
    * <span data-ttu-id="e330a-157">Sláðu inn [ , “-“, ] aftast í formúlu.</span><span class="sxs-lookup"><span data-stu-id="e330a-157">Type [ , “-“, ] at the end of the formula.</span></span>  
20. <span data-ttu-id="e330a-158">Í trénu skal velja „String/TEXT“.</span><span class="sxs-lookup"><span data-stu-id="e330a-158">In the tree, select 'String\TEXT'.</span></span>
21. <span data-ttu-id="e330a-159">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="e330a-159">Click Add function.</span></span>
22. <span data-ttu-id="e330a-160">Veljið 'Transactions\Record-ID(RecId)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="e330a-160">In the tree, select 'Transactions\Record-ID(RecId)'.</span></span>
23. <span data-ttu-id="e330a-161">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="e330a-161">Click Add data source.</span></span>
24. <span data-ttu-id="e330a-162">Í svæði Formúla slá inn 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span><span class="sxs-lookup"><span data-stu-id="e330a-162">In the Formula field, enter 'CONCATENATE(Transactions.Voucher, "-", TEXT(Transactions.RecId))'.</span></span>
    * <span data-ttu-id="e330a-163">Sláðu inn [))] aftast í formúlu.</span><span class="sxs-lookup"><span data-stu-id="e330a-163">Type [))] at the end of the formula.</span></span>  
25. <span data-ttu-id="e330a-164">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e330a-164">Click Save.</span></span>
    * <span data-ttu-id="e330a-165">Gangið úr skugga um að engar villur hafi fundist fyrir formúluna sem er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="e330a-165">Make sure that no errors have been discovered for the created formula.</span></span> <span data-ttu-id="e330a-166">Sjá flipann VILLUR undir ritilstýringu formúlu.</span><span class="sxs-lookup"><span data-stu-id="e330a-166">See the ERRORS tab below the formula editor control.</span></span>  
26. <span data-ttu-id="e330a-167">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e330a-167">Close the page.</span></span>
27. <span data-ttu-id="e330a-168">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e330a-168">Click OK.</span></span>
    * <span data-ttu-id="e330a-169">Bættu reiknuð svæði við þennan gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="e330a-169">Add the calculated field to this data source.</span></span>  
28. <span data-ttu-id="e330a-170">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="e330a-170">Click Add.</span></span>
    * <span data-ttu-id="e330a-171">Smella á bæta Við til að bæta við nýju reiknuðu svæði.</span><span class="sxs-lookup"><span data-stu-id="e330a-171">Click Add to add a new calculated field.</span></span>  
29. <span data-ttu-id="e330a-172">Í reitnum Heiti skal færa inn ‚$Amount'.</span><span class="sxs-lookup"><span data-stu-id="e330a-172">In the Name field, type '$Amount'.</span></span>
    * <span data-ttu-id="e330a-173">$Amount</span><span class="sxs-lookup"><span data-stu-id="e330a-173">$Amount</span></span>  
30. <span data-ttu-id="e330a-174">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="e330a-174">Click Edit formula.</span></span>
31. <span data-ttu-id="e330a-175">Í trénu skal víkka út „Færslur“.</span><span class="sxs-lookup"><span data-stu-id="e330a-175">In the tree, expand 'Transactions'.</span></span>
32. <span data-ttu-id="e330a-176">Veljið 'Transactions\Debit(AmountCurDebit)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="e330a-176">In the tree, select 'Transactions\Debit(AmountCurDebit)'.</span></span>
33. <span data-ttu-id="e330a-177">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="e330a-177">Click Add data source.</span></span>
34. <span data-ttu-id="e330a-178">Í svæði Formúla slá inn 'Transactions.AmountCurDebit - '.</span><span class="sxs-lookup"><span data-stu-id="e330a-178">In the Formula field, enter 'Transactions.AmountCurDebit - '.</span></span>
    * <span data-ttu-id="e330a-179">Sláðu inn [ - ] aftast í formúlu.</span><span class="sxs-lookup"><span data-stu-id="e330a-179">Type [ - ] at the end of the formula.</span></span>  
35. <span data-ttu-id="e330a-180">Í trénu, veljið 'Transactions\Credit(AmountCurCredit)'.</span><span class="sxs-lookup"><span data-stu-id="e330a-180">In the tree, select 'Transactions\Credit(AmountCurCredit)'.</span></span>
36. <span data-ttu-id="e330a-181">Smellt er á Bæta við gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="e330a-181">Click Add data source.</span></span>
37. <span data-ttu-id="e330a-182">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e330a-182">Click Save.</span></span>
38. <span data-ttu-id="e330a-183">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e330a-183">Close the page.</span></span>
39. <span data-ttu-id="e330a-184">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e330a-184">Click OK.</span></span>
    * <span data-ttu-id="e330a-185">Þetta bætir $Amount reiknaða svæðið við vilda gagnaveitu fyrir núverandi gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="e330a-185">This will add the $Amount calculated field to the selected data source for the current data model.</span></span>  
40. <span data-ttu-id="e330a-186">Í trénu skal velja „Færslur\$Upphæð“.</span><span class="sxs-lookup"><span data-stu-id="e330a-186">In the tree, select 'Transactions\$Amount'.</span></span>
41. <span data-ttu-id="e330a-187">Í trénu skal víkka út „Færslur“.</span><span class="sxs-lookup"><span data-stu-id="e330a-187">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="e330a-188">Í tré skal víkka eða draga saman „Færslur\$Upphæð“.</span><span class="sxs-lookup"><span data-stu-id="e330a-188">In the tree, expand or collapse 'Transactions\$Amount'.</span></span>
43. <span data-ttu-id="e330a-189">Í tré skal víkka eða draga saman 'Transactions'.</span><span class="sxs-lookup"><span data-stu-id="e330a-189">In the tree, expand or collapse 'Transactions'.</span></span>
44. <span data-ttu-id="e330a-190">Í trénu skal velja 'Dynamics 365 for Operations\Table records'.</span><span class="sxs-lookup"><span data-stu-id="e330a-190">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
45. <span data-ttu-id="e330a-191">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="e330a-191">Click Add root.</span></span>
    * <span data-ttu-id="e330a-192">Færið inn gagnaveitu til að hafa aðgang að upplýsingar bankareiknings fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="e330a-192">Enter this data source to access the company’s bank account details.</span></span>  
46. <span data-ttu-id="e330a-193">Í reitnum Heiti skal færa inn 'BankAccount'.</span><span class="sxs-lookup"><span data-stu-id="e330a-193">In the Name field, type 'BankAccount'.</span></span>
    * <span data-ttu-id="e330a-194">BankAccount</span><span class="sxs-lookup"><span data-stu-id="e330a-194">BankAccount</span></span>  
47. <span data-ttu-id="e330a-195">Færið inn 'Bankareikning' í svæðinu Merki.</span><span class="sxs-lookup"><span data-stu-id="e330a-195">In the Label field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="e330a-196">Bankareikningur</span><span class="sxs-lookup"><span data-stu-id="e330a-196">Bank Account</span></span>  
48. <span data-ttu-id="e330a-197">Færið inn 'Bankareikning' í svæðinu Hjálp.</span><span class="sxs-lookup"><span data-stu-id="e330a-197">In the Help field, enter 'Bank Account'.</span></span>
    * <span data-ttu-id="e330a-198">Bankareikningur</span><span class="sxs-lookup"><span data-stu-id="e330a-198">Bank Account</span></span>  
49. <span data-ttu-id="e330a-199">Velja skal Já í reitnum Óska eftir fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="e330a-199">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="e330a-200">Velja skal Já.</span><span class="sxs-lookup"><span data-stu-id="e330a-200">Select Yes.</span></span>  
50. <span data-ttu-id="e330a-201">Í reitnum Tafla skal færa inn 'BankAccountTable'.</span><span class="sxs-lookup"><span data-stu-id="e330a-201">In the Table field, type 'BankAccountTable'.</span></span>
    * <span data-ttu-id="e330a-202">BankAccountTable</span><span class="sxs-lookup"><span data-stu-id="e330a-202">BankAccountTable</span></span>  
51. <span data-ttu-id="e330a-203">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e330a-203">Click OK.</span></span>
    * <span data-ttu-id="e330a-204">Veljið BankAccountTable töfluna sem gagnaveita fyrir gildandi gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="e330a-204">Select the BankAccountTable table as a data source for the current data model.</span></span>  
52. <span data-ttu-id="e330a-205">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="e330a-205">Click Add root.</span></span>
    * <span data-ttu-id="e330a-206">Færið inn gagnaveitu til að hafa aðgang að upplýsingar um fyrirmæli fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="e330a-206">Enter this data source to access the company’s requisites.</span></span>  
53. <span data-ttu-id="e330a-207">Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.</span><span class="sxs-lookup"><span data-stu-id="e330a-207">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="e330a-208">Fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="e330a-208">Company</span></span>  
54. <span data-ttu-id="e330a-209">Í reitinn Merki skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="e330a-209">In the Label field, type a value.</span></span>
    * <span data-ttu-id="e330a-210">Fyrirtækið</span><span class="sxs-lookup"><span data-stu-id="e330a-210">Company information</span></span>  
55. <span data-ttu-id="e330a-211">Í reitinn Hjálp skal færa inn ‚Fyrirtækjaupplýsingar‘.</span><span class="sxs-lookup"><span data-stu-id="e330a-211">In the Help field, enter 'Company information'.</span></span>
    * <span data-ttu-id="e330a-212">Fyrirtækið</span><span class="sxs-lookup"><span data-stu-id="e330a-212">Company information</span></span>  
56. <span data-ttu-id="e330a-213">Velja skal Já í reitnum Óska eftir fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="e330a-213">Select Yes in the Ask for query field.</span></span>
    * <span data-ttu-id="e330a-214">Velja skal Já.</span><span class="sxs-lookup"><span data-stu-id="e330a-214">Select Yes.</span></span>  
57. <span data-ttu-id="e330a-215">Í reitinn Tafla skal færa inn ‚CompanyInfo‘.</span><span class="sxs-lookup"><span data-stu-id="e330a-215">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="e330a-216">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="e330a-216">CompanyInfo</span></span>  
58. <span data-ttu-id="e330a-217">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e330a-217">Click OK.</span></span>
    * <span data-ttu-id="e330a-218">Veljið CompanyInfo töfluna sem gagnaveita fyrir gildandi gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="e330a-218">Select the CompanyInfo table as a data source for the current data model.</span></span>  
59. <span data-ttu-id="e330a-219">Veljið 'Functions\Calculated svæðið', í trénu.</span><span class="sxs-lookup"><span data-stu-id="e330a-219">In the tree, select 'Functions\Calculated field'.</span></span>
60. <span data-ttu-id="e330a-220">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="e330a-220">Click Add root.</span></span>
    * <span data-ttu-id="e330a-221">Setja inn reiknuð svæði sem nýja gagnaveita.</span><span class="sxs-lookup"><span data-stu-id="e330a-221">Insert a calculated field as a new data source.</span></span>  
61. <span data-ttu-id="e330a-222">Í svæðið Heiti, færðu in 'ProcessingDateTime'.</span><span class="sxs-lookup"><span data-stu-id="e330a-222">In the Name field, type 'ProcessingDateTime'.</span></span>
    * <span data-ttu-id="e330a-223">ProcessingDateTime</span><span class="sxs-lookup"><span data-stu-id="e330a-223">ProcessingDateTime</span></span>  
62. <span data-ttu-id="e330a-224">Í svæðið Merki skal færa inn ' Vinnsludagsetning & tími '.</span><span class="sxs-lookup"><span data-stu-id="e330a-224">In the Label field, enter 'Processing date & time'.</span></span>
    * <span data-ttu-id="e330a-225">Vinnsludagsetning & tími</span><span class="sxs-lookup"><span data-stu-id="e330a-225">Processing date & time</span></span>  
63. <span data-ttu-id="e330a-226">Smellt er á Breyta formúla.</span><span class="sxs-lookup"><span data-stu-id="e330a-226">Click Edit formula.</span></span>
64. <span data-ttu-id="e330a-227">Í tré skal velja 'Date/time\SESSIONNOW'.</span><span class="sxs-lookup"><span data-stu-id="e330a-227">In the tree, select 'Date/time\SESSIONNOW'.</span></span>
65. <span data-ttu-id="e330a-228">Smelltu á Bæta við Aðgerð.</span><span class="sxs-lookup"><span data-stu-id="e330a-228">Click Add function.</span></span>
66. <span data-ttu-id="e330a-229">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e330a-229">Click Save.</span></span>
67. <span data-ttu-id="e330a-230">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e330a-230">Close the page.</span></span>
68. <span data-ttu-id="e330a-231">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e330a-231">Click OK.</span></span>
    * <span data-ttu-id="e330a-232">Bæta ProcessingDateTime reiknaða svæðisins við sem gagnaveita fyrir gildandi gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="e330a-232">Add the ProcessingDateTime calculated field as a data source for the current data model.</span></span>  
69. <span data-ttu-id="e330a-233">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e330a-233">Click Save.</span></span>
70. <span data-ttu-id="e330a-234">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e330a-234">Close the page.</span></span>
71. <span data-ttu-id="e330a-235">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e330a-235">Close the page.</span></span>
72. <span data-ttu-id="e330a-236">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e330a-236">Close the page.</span></span>

