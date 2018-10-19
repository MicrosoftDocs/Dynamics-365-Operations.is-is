--- 
title: "Rafræn skýrslugerð Varpa gagnalíkani í valda gagnagjafa"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur varpað rafræna skýrslugerð (ER) gagnalíkani á valdar Dynamics 365 for Finance and Operations, Enterprise edition gagnaveitur."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 249bf3f3806ed43eccf39086bdf9697a3e879c27
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="64cc2-103">Rafræn skýrslugerð Varpa gagnalíkani í valda gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="64cc2-103">ER Map data model to selected data sources</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="64cc2-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur varpað rafræna skýrslugerð (ER) gagnalíkani á valdar Dynamics 365 for Finance and Operations, Enterprise edition gagnaveitur.</span><span class="sxs-lookup"><span data-stu-id="64cc2-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected Dynamics 365 for Finance and Operations, Enterprise edition data sources.</span></span> <span data-ttu-id="64cc2-105">Þessi líkanavörpun verður síðar notuð sem gagnaveita í skilgreiningu sniðs sem verður notað til að stjórna skjölum rafrænna greiðsla.</span><span class="sxs-lookup"><span data-stu-id="64cc2-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="64cc2-106">Í þessu dæmi er varpað gagnalíkani fyrir dæmi um fyrirtæki, Litware, Inc. til gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="64cc2-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="64cc2-107">Til að ljúka þessum skrefum, verður fyrst að ljúka skrefum í ferlinu "Velja gagnaveita fyrir líkanavörpun".</span><span class="sxs-lookup"><span data-stu-id="64cc2-107">To complete these steps, you must first complete the steps in the “Select data sources for model mapping” procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="64cc2-108">Opna grunnstillingatré rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="64cc2-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="64cc2-109">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="64cc2-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="64cc2-110">Smellt er á Skilgreiningum.</span><span class="sxs-lookup"><span data-stu-id="64cc2-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="64cc2-111">Veljið stofnuð líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="64cc2-111">Select created model mapping</span></span>
1. <span data-ttu-id="64cc2-112">Veljið 'Greiðslur (einfaldað líkan)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="64cc2-113">Gangið úr skugga um að skilgreiningarlíkanið "Greiðslur (einfaldað líkan)" hefur verið stofnuð fyrirfram.</span><span class="sxs-lookup"><span data-stu-id="64cc2-113">Make sure that the model configuration “Payments (simplified model)” has been created in advance.</span></span> <span data-ttu-id="64cc2-114">Að öðrum kosti skal stoppa núna og koma aftur eftir að lokið við verkefnaleiðbeiningar „Mynda nýja grunnstillingu með gagnalíkan af völdu léni“.</span><span class="sxs-lookup"><span data-stu-id="64cc2-114">Otherwise, stop now and return after completion of the task guide ‘Create a new configuration with data model of the selected domain’.</span></span>  
2. <span data-ttu-id="64cc2-115">Smellt er á hönnuður Líkana.</span><span class="sxs-lookup"><span data-stu-id="64cc2-115">Click Model designer.</span></span>
3. <span data-ttu-id="64cc2-116">Smellt er á Varpa líkani á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="64cc2-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="64cc2-117">Veljið færsluna 'CT vörpun'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="64cc2-118">Vörpun CT</span><span class="sxs-lookup"><span data-stu-id="64cc2-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="64cc2-119">Binda stofnaða gagnaveitur við þætti gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="64cc2-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="64cc2-120">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="64cc2-120">Click Designer.</span></span>
2. <span data-ttu-id="64cc2-121">Í trénu, skal velja 'Processing date & time(ProcessingDateTime)'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="64cc2-122">Veljið ‚Processing date(ProcessingDateTime)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="64cc2-123">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-123">Click Bind.</span></span>
5. <span data-ttu-id="64cc2-124">Veljið ‚Payment message identification(MessageIdentification)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="64cc2-125">Í trénu skal víkka út „Færslur“.</span><span class="sxs-lookup"><span data-stu-id="64cc2-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="64cc2-126">Veljið ''Transactions\Journal batch number(JournalNum)'., í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="64cc2-127">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-127">Click Bind.</span></span>
9. <span data-ttu-id="64cc2-128">Í trénu skal velja „Greiðslur“.</span><span class="sxs-lookup"><span data-stu-id="64cc2-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="64cc2-129">Í trénu skal velja „Færslur“.</span><span class="sxs-lookup"><span data-stu-id="64cc2-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="64cc2-130">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-130">Click Bind.</span></span>
12. <span data-ttu-id="64cc2-131">Í trénu, útvíkka ' Greiðslur = Færslur.</span><span class="sxs-lookup"><span data-stu-id="64cc2-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="64cc2-132">Í trénu, útvíkka ' Payments = Transactions\Creditor'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="64cc2-133">Í trénu, útvíkka ' Payments = Transactions\Creditor\Account'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="64cc2-134">Í trénu, skal velja ' Payments = Transactions\Creditor\Account\Currency code(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="64cc2-135">Útvíkka 'Transactions\vendBankAccountInTransactionCompany()', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="64cc2-136">Veljið 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="64cc2-137">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-137">Click Bind.</span></span>
19. <span data-ttu-id="64cc2-138">Í trénu, skal velja ' Payments = Transactions\Creditor\Account\IBAN code(IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="64cc2-139">Veljið 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="64cc2-140">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-140">Click Bind.</span></span>
22. <span data-ttu-id="64cc2-141">Í trénu, skal velja ' Payments = Transactions\Creditor\Account\Number'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="64cc2-142">Veljið 'Transactions\vendBankAccountInTransactionCompany () \Bank lykil number(AccountNum)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="64cc2-143">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-143">Click Bind.</span></span>
25. <span data-ttu-id="64cc2-144">Í trénu, útvíkka ' Payments = Transactions\Creditor\Agent'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="64cc2-145">Í trénu, skal velja ' Payments = Transactions\Creditor\Agent\Name'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="64cc2-146">Veljið '\Name Transactions\vendBankAccountInTransactionCompany ()', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="64cc2-147">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-147">Click Bind.</span></span>
29. <span data-ttu-id="64cc2-148">Í trénu, skal velja ' Payments = Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="64cc2-149">Veljið 'Transactions\vendBankAccountInTransactionCompany () \Routing number(RegistrationNum)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="64cc2-150">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-150">Click Bind.</span></span>
32. <span data-ttu-id="64cc2-151">Í trénu, skal velja ' Payments = Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="64cc2-152">Veljið 'Transactions\vendBankAccountInTransactionCompany () \SWIFT code(SWIFTNo)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="64cc2-153">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-153">Click Bind.</span></span>
35. <span data-ttu-id="64cc2-154">Í trénu, skal velja ' Payments = Transactions\Creditor\Name'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="64cc2-155">Útvíkka 'Transactions\findVendTable()', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="64cc2-156">Veljið ‚Transactions\findVendTable()\name()', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="64cc2-157">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-157">Click Bind.</span></span>
39. <span data-ttu-id="64cc2-158">Í trénu, skal velja ' Payments = Transactions\Currency code(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="64cc2-159">Í trénu skal víkka út „Færslur\>Tengsl“.</span><span class="sxs-lookup"><span data-stu-id="64cc2-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="64cc2-160">Í trénu skal víkka út „Færslur\>Tengsl\Gjaldmiðill tafla(Gjaldmiðill)“.</span><span class="sxs-lookup"><span data-stu-id="64cc2-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="64cc2-161">Í trénu skal velja „Færslur\>Tengsl\Gjaldmiðill tafla(Gjaldmiðill)\Gjaldmiðill kóði(CurrencyCodeISO)“.</span><span class="sxs-lookup"><span data-stu-id="64cc2-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="64cc2-162">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-162">Click Bind.</span></span>
44. <span data-ttu-id="64cc2-163">Í trénu, útvíkka ' Payments= Transactions\Debtor'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="64cc2-164">Í trénu, útvíkka 'Payments= Transactions\Debtor\Account'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="64cc2-165">Í trénu, skal velja ' Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="64cc2-166">Veljið 'Bank Account(BankAccount)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="64cc2-167">Útvíkka 'Bank Account(BankAccount)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="64cc2-168">Veljið 'Bank Account(BankAccount)\Currency(CurrencyCode)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="64cc2-169">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-169">Click Bind.</span></span>
51. <span data-ttu-id="64cc2-170">Í trénu, skal velja ' Bank Account(BankAccount) \IBAN'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="64cc2-171">Í trénu, skal velja ' Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="64cc2-172">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-172">Click Bind.</span></span>
54. <span data-ttu-id="64cc2-173">Í trénu, skal velja ' Payments= Transactions\Debtor\Account\Number'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="64cc2-174">Veljið 'Bank Account(BankAccount)\Bank account number(AccountNum)‘, í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="64cc2-175">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-175">Click Bind.</span></span>
57. <span data-ttu-id="64cc2-176">Í trénu, útvíkka ' Payments= Transactions\Debtor\Agent'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="64cc2-177">Í trénu, skal velja ' Payments= Transactions\Debtor\Agent\Name'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="64cc2-178">Í trénu skal velja 'Bank Account(BankAccount)\Name'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="64cc2-179">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-179">Click Bind.</span></span>
61. <span data-ttu-id="64cc2-180">Í trénu, skal velja ' Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="64cc2-181">Í trénu skal velja 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="64cc2-182">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-182">Click Bind.</span></span>
64. <span data-ttu-id="64cc2-183">Í trénu, skal velja ' Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="64cc2-184">Í trénu, skal velja 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="64cc2-185">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-185">Click Bind.</span></span>
67. <span data-ttu-id="64cc2-186">Í trénu, skal velja ' Payments= Transactions\Debtor\Name'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="64cc2-187">Í trénu skal velja 'Company information(Company)'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="64cc2-188">Útvíkka, í trénu 'Company information(Company)'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="64cc2-189">Veljið 'Company information(Company)\Name‘, í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="64cc2-190">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-190">Click Bind.</span></span>
72. <span data-ttu-id="64cc2-191">Í trénu, skal velja ' Payments= Transactions\Description'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="64cc2-192">Veljið 'Transactions\Description(Txt)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="64cc2-193">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-193">Click Bind.</span></span>
75. <span data-ttu-id="64cc2-194">Í trénu, skal velja ''Payments= Transactions\End to end identification code(End2EndID)'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="64cc2-195">Í trénu skal velja „Færslur\$EndToEndID“.</span><span class="sxs-lookup"><span data-stu-id="64cc2-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="64cc2-196">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-196">Click Bind.</span></span>
78. <span data-ttu-id="64cc2-197">Í trénu, skal velja ''Payments= Transactions\Instructed amount(InstructedAmount)'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="64cc2-198">Í trénu skal velja „Færslur\$Upphæð“.</span><span class="sxs-lookup"><span data-stu-id="64cc2-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="64cc2-199">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-199">Click Bind.</span></span>
81. <span data-ttu-id="64cc2-200">Í trénu skal velja 'Payments= Transactions\Transaction date(TransactionDate)'.</span><span class="sxs-lookup"><span data-stu-id="64cc2-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="64cc2-201">Veljið 'Transactions\Date(TransDate)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="64cc2-202">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="64cc2-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="64cc2-203">Villuleita stofnaða vörpun</span><span class="sxs-lookup"><span data-stu-id="64cc2-203">Validate created mapping</span></span>
1. <span data-ttu-id="64cc2-204">Smella á Villuleita.</span><span class="sxs-lookup"><span data-stu-id="64cc2-204">Click Validate.</span></span>
    * <span data-ttu-id="64cc2-205">Sannprófa nýja vörpun til að tryggja að allar bindingar séu í lagi.</span><span class="sxs-lookup"><span data-stu-id="64cc2-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="64cc2-206">Með því að smella á örina má stækka eða fella saman hlutann Villulisti.</span><span class="sxs-lookup"><span data-stu-id="64cc2-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="64cc2-207">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="64cc2-207">Click Save.</span></span>
4. <span data-ttu-id="64cc2-208">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="64cc2-208">Close the page.</span></span>
5. <span data-ttu-id="64cc2-209">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="64cc2-209">Close the page.</span></span>
6. <span data-ttu-id="64cc2-210">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="64cc2-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="64cc2-211">Breyta stöðu gildandi útgáfu skilgreiningar líkans</span><span class="sxs-lookup"><span data-stu-id="64cc2-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="64cc2-212">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="64cc2-212">Click Change status.</span></span>
    * <span data-ttu-id="64cc2-213">Breyta stöðu hannaðrar grunnstillingar líkans - úr Drög í Lokið til að gera tiltækur fyrir hönnun greiðslusniðs.</span><span class="sxs-lookup"><span data-stu-id="64cc2-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="64cc2-214">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="64cc2-214">Click Complete.</span></span>
    * <span data-ttu-id="64cc2-215">Velja Lokið.</span><span class="sxs-lookup"><span data-stu-id="64cc2-215">Select Complete.</span></span>  
3. <span data-ttu-id="64cc2-216">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="64cc2-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="64cc2-217">Til dæmis „Útgáfa 1“.</span><span class="sxs-lookup"><span data-stu-id="64cc2-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="64cc2-218">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="64cc2-218">Click OK.</span></span>
5. <span data-ttu-id="64cc2-219">Velja lokna útgáfu af núgildandi skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="64cc2-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="64cc2-220">Athugið að stofnuð skilgreining er vistuð sem lokin útgáfa 1.</span><span class="sxs-lookup"><span data-stu-id="64cc2-220">Note that the created configuration is saved as completed version 1.</span></span>  


