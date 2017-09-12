--- 
title: "Varpa gagnalíkani á valdar gagnaveitur fyrir rafræna skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur varpað rafræna skýrslugerð (ER) gagnalíkani á valdar Dynamics 365 for Finance and Operations, Enterprise edition gagnaveitur."
author: NickSelin
manager: AnnBe
ms.date: 01/16/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 96974d7c1597db4ac31168be40cecbc7e12d6edd
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="map-a-data-model-to-selected-data-sources-for-electronic-reporting-er"></a><span data-ttu-id="bbf76-103">Varpa gagnalíkani á valdar gagnaveitur fyrir rafræna skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="bbf76-103">Map a data model to selected data sources for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bbf76-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur varpað rafræna skýrslugerð (ER) gagnalíkani á valdar Dynamics 365 for Finance and Operations, Enterprise edition gagnaveitur.</span><span class="sxs-lookup"><span data-stu-id="bbf76-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected Dynamics 365 for Finance and Operations, Enterprise edition data sources.</span></span> <span data-ttu-id="bbf76-105">Þessi líkanavörpun verður síðar notuð sem gagnaveita í skilgreiningu sniðs sem verður notað til að stjórna skjölum rafrænna greiðsla.</span><span class="sxs-lookup"><span data-stu-id="bbf76-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="bbf76-106">Í þessu dæmi er varpað gagnalíkani fyrir dæmi um fyrirtæki, Litware, Inc. til gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="bbf76-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="bbf76-107">Til að ljúka þessum skrefum, verður fyrst að ljúka skrefum í ferlinu "Velja gagnaveita fyrir líkanavörpun".</span><span class="sxs-lookup"><span data-stu-id="bbf76-107">To complete these steps, you must first complete the steps in the “Select data sources for model mapping” procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="bbf76-108">Opna grunnstillingatré rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="bbf76-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="bbf76-109">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="bbf76-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="bbf76-110">Smellt er á Skilgreiningum.</span><span class="sxs-lookup"><span data-stu-id="bbf76-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="bbf76-111">Veljið stofnuð líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="bbf76-111">Select created model mapping</span></span>
1. <span data-ttu-id="bbf76-112">Veljið 'Greiðslur (einfaldað líkan)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="bbf76-113">Gangið úr skugga um að skilgreiningarlíkanið "Greiðslur (einfaldað líkan)" hefur verið stofnuð fyrirfram.</span><span class="sxs-lookup"><span data-stu-id="bbf76-113">Make sure that the model configuration “Payments (simplified model)” has been created in advance.</span></span> <span data-ttu-id="bbf76-114">Að öðrum kosti skal stoppa núna og koma aftur eftir að lokið við verkefnaleiðbeiningar „Mynda nýja grunnstillingu með gagnalíkan af völdu léni“.</span><span class="sxs-lookup"><span data-stu-id="bbf76-114">Otherwise, stop now and return after completion of the task guide ‘Create a new configuration with data model of the selected domain’.</span></span>  
2. <span data-ttu-id="bbf76-115">Smellt er á hönnuður Líkana.</span><span class="sxs-lookup"><span data-stu-id="bbf76-115">Click Model designer.</span></span>
3. <span data-ttu-id="bbf76-116">Smellt er á Varpa líkani á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="bbf76-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="bbf76-117">Veljið færsluna 'CT vörpun'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="bbf76-118">Vörpun CT</span><span class="sxs-lookup"><span data-stu-id="bbf76-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="bbf76-119">Binda stofnaða gagnaveitur við þætti gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="bbf76-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="bbf76-120">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="bbf76-120">Click Designer.</span></span>
2. <span data-ttu-id="bbf76-121">Í trénu, skal velja 'Processing date & time(ProcessingDateTime)'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="bbf76-122">Veljið ‚Processing date(ProcessingDateTime)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="bbf76-123">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-123">Click Bind.</span></span>
5. <span data-ttu-id="bbf76-124">Veljið ‚Payment message identification(MessageIdentification)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="bbf76-125">Í trénu skal víkka út „Færslur“.</span><span class="sxs-lookup"><span data-stu-id="bbf76-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="bbf76-126">Veljið ''Transactions\Journal batch number(JournalNum)'., í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="bbf76-127">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-127">Click Bind.</span></span>
9. <span data-ttu-id="bbf76-128">Í trénu skal velja „Greiðslur“.</span><span class="sxs-lookup"><span data-stu-id="bbf76-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="bbf76-129">Í trénu skal velja „Færslur“.</span><span class="sxs-lookup"><span data-stu-id="bbf76-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="bbf76-130">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-130">Click Bind.</span></span>
12. <span data-ttu-id="bbf76-131">Í trénu, útvíkka ' Greiðslur = Færslur.</span><span class="sxs-lookup"><span data-stu-id="bbf76-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="bbf76-132">Í trénu, útvíkka ' Payments = Transactions\Creditor'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="bbf76-133">Í trénu, útvíkka ' Payments = Transactions\Creditor\Account'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="bbf76-134">Í trénu, skal velja ' Payments = Transactions\Creditor\Account\Currency code(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="bbf76-135">Útvíkka 'Transactions\vendBankAccountInTransactionCompany()', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="bbf76-136">Veljið 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="bbf76-137">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-137">Click Bind.</span></span>
19. <span data-ttu-id="bbf76-138">Í trénu, skal velja ' Payments = Transactions\Creditor\Account\IBAN code(IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="bbf76-139">Veljið 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="bbf76-140">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-140">Click Bind.</span></span>
22. <span data-ttu-id="bbf76-141">Í trénu, skal velja ' Payments = Transactions\Creditor\Account\Number'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="bbf76-142">Veljið 'Transactions\vendBankAccountInTransactionCompany () \Bank lykil number(AccountNum)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="bbf76-143">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-143">Click Bind.</span></span>
25. <span data-ttu-id="bbf76-144">Í trénu, útvíkka ' Payments = Transactions\Creditor\Agent'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="bbf76-145">Í trénu, skal velja ' Payments = Transactions\Creditor\Agent\Name'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="bbf76-146">Veljið '\Name Transactions\vendBankAccountInTransactionCompany ()', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="bbf76-147">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-147">Click Bind.</span></span>
29. <span data-ttu-id="bbf76-148">Í trénu, skal velja ' Payments = Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="bbf76-149">Veljið 'Transactions\vendBankAccountInTransactionCompany () \Routing number(RegistrationNum)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="bbf76-150">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-150">Click Bind.</span></span>
32. <span data-ttu-id="bbf76-151">Í trénu, skal velja ' Payments = Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="bbf76-152">Veljið 'Transactions\vendBankAccountInTransactionCompany () \SWIFT code(SWIFTNo)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="bbf76-153">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-153">Click Bind.</span></span>
35. <span data-ttu-id="bbf76-154">Í trénu, skal velja ' Payments = Transactions\Creditor\Name'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="bbf76-155">Útvíkka 'Transactions\findVendTable()', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="bbf76-156">Veljið ‚Transactions\findVendTable()\name()', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="bbf76-157">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-157">Click Bind.</span></span>
39. <span data-ttu-id="bbf76-158">Í trénu, skal velja ' Payments = Transactions\Currency code(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="bbf76-159">Í trénu skal víkka út „Færslur\>Tengsl“.</span><span class="sxs-lookup"><span data-stu-id="bbf76-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="bbf76-160">Í trénu skal víkka út „Færslur\>Tengsl\Gjaldmiðill tafla(Gjaldmiðill)“.</span><span class="sxs-lookup"><span data-stu-id="bbf76-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="bbf76-161">Í trénu skal velja „Færslur\>Tengsl\Gjaldmiðill tafla(Gjaldmiðill)\Gjaldmiðill kóði(CurrencyCodeISO)“.</span><span class="sxs-lookup"><span data-stu-id="bbf76-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="bbf76-162">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-162">Click Bind.</span></span>
44. <span data-ttu-id="bbf76-163">Í trénu, útvíkka ' Payments= Transactions\Debtor'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="bbf76-164">Í trénu, útvíkka 'Payments= Transactions\Debtor\Account'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="bbf76-165">Í trénu, skal velja ' Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="bbf76-166">Veljið 'Bank Account(BankAccount)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="bbf76-167">Útvíkka 'Bank Account(BankAccount)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="bbf76-168">Veljið 'Bank Account(BankAccount)\Currency(CurrencyCode)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="bbf76-169">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-169">Click Bind.</span></span>
51. <span data-ttu-id="bbf76-170">Í trénu, skal velja ' Bank Account(BankAccount) \IBAN'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="bbf76-171">Í trénu, skal velja ' Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="bbf76-172">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-172">Click Bind.</span></span>
54. <span data-ttu-id="bbf76-173">Í trénu, skal velja ' Payments= Transactions\Debtor\Account\Number'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="bbf76-174">Veljið 'Bank Account(BankAccount)\Bank account number(AccountNum)‘, í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="bbf76-175">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-175">Click Bind.</span></span>
57. <span data-ttu-id="bbf76-176">Í trénu, útvíkka ' Payments= Transactions\Debtor\Agent'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="bbf76-177">Í trénu, skal velja ' Payments= Transactions\Debtor\Agent\Name'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="bbf76-178">Í trénu skal velja 'Bank Account(BankAccount)\Name'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="bbf76-179">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-179">Click Bind.</span></span>
61. <span data-ttu-id="bbf76-180">Í trénu, skal velja ' Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="bbf76-181">Í trénu skal velja 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="bbf76-182">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-182">Click Bind.</span></span>
64. <span data-ttu-id="bbf76-183">Í trénu, skal velja ' Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="bbf76-184">Í trénu, skal velja 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="bbf76-185">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-185">Click Bind.</span></span>
67. <span data-ttu-id="bbf76-186">Í trénu, skal velja ' Payments= Transactions\Debtor\Name'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="bbf76-187">Í trénu skal velja 'Company information(Company)'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="bbf76-188">Útvíkka, í trénu 'Company information(Company)'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="bbf76-189">Veljið 'Company information(Company)\Name‘, í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="bbf76-190">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-190">Click Bind.</span></span>
72. <span data-ttu-id="bbf76-191">Í trénu, skal velja ' Payments= Transactions\Description'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="bbf76-192">Veljið 'Transactions\Description(Txt)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="bbf76-193">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-193">Click Bind.</span></span>
75. <span data-ttu-id="bbf76-194">Í trénu, skal velja ''Payments= Transactions\End to end identification code(End2EndID)'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="bbf76-195">Í trénu skal velja „Færslur\$EndToEndID“.</span><span class="sxs-lookup"><span data-stu-id="bbf76-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="bbf76-196">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-196">Click Bind.</span></span>
78. <span data-ttu-id="bbf76-197">Í trénu, skal velja ''Payments= Transactions\Instructed amount(InstructedAmount)'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="bbf76-198">Í trénu skal velja „Færslur\$Upphæð“.</span><span class="sxs-lookup"><span data-stu-id="bbf76-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="bbf76-199">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-199">Click Bind.</span></span>
81. <span data-ttu-id="bbf76-200">Í trénu skal velja 'Payments= Transactions\Transaction date(TransactionDate)'.</span><span class="sxs-lookup"><span data-stu-id="bbf76-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="bbf76-201">Veljið 'Transactions\Date(TransDate)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="bbf76-202">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="bbf76-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="bbf76-203">Villuleita stofnaða vörpun</span><span class="sxs-lookup"><span data-stu-id="bbf76-203">Validate created mapping</span></span>
1. <span data-ttu-id="bbf76-204">Smella á Villuleita.</span><span class="sxs-lookup"><span data-stu-id="bbf76-204">Click Validate.</span></span>
    * <span data-ttu-id="bbf76-205">Sannprófa nýja vörpun til að tryggja að allar bindingar séu í lagi.</span><span class="sxs-lookup"><span data-stu-id="bbf76-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="bbf76-206">Með því að smella á örina má stækka eða fella saman hlutann Villulisti.</span><span class="sxs-lookup"><span data-stu-id="bbf76-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="bbf76-207">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="bbf76-207">Click Save.</span></span>
4. <span data-ttu-id="bbf76-208">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bbf76-208">Close the page.</span></span>
5. <span data-ttu-id="bbf76-209">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bbf76-209">Close the page.</span></span>
6. <span data-ttu-id="bbf76-210">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="bbf76-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="bbf76-211">Breyta stöðu gildandi útgáfu skilgreiningar líkans</span><span class="sxs-lookup"><span data-stu-id="bbf76-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="bbf76-212">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="bbf76-212">Click Change status.</span></span>
    * <span data-ttu-id="bbf76-213">Breyta stöðu hannaðrar grunnstillingar líkans - úr Drög í Lokið til að gera tiltækur fyrir hönnun greiðslusniðs.</span><span class="sxs-lookup"><span data-stu-id="bbf76-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="bbf76-214">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="bbf76-214">Click Complete.</span></span>
    * <span data-ttu-id="bbf76-215">Velja Lokið.</span><span class="sxs-lookup"><span data-stu-id="bbf76-215">Select Complete.</span></span>  
3. <span data-ttu-id="bbf76-216">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="bbf76-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="bbf76-217">Til dæmis „Útgáfa 1“.</span><span class="sxs-lookup"><span data-stu-id="bbf76-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="bbf76-218">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="bbf76-218">Click OK.</span></span>
5. <span data-ttu-id="bbf76-219">Velja lokna útgáfu af núgildandi skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="bbf76-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="bbf76-220">Athugið að stofnuð skilgreining er vistuð sem lokin útgáfa 1.</span><span class="sxs-lookup"><span data-stu-id="bbf76-220">Note that the created configuration is saved as completed version 1.</span></span>  


