---
title: Rafræn skýrslugerð Varpa gagnalíkani í valda gagnagjafa
description: Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur varpað rafræna skýrslugerð (ER) gagnalíkani á valda gagnaveitur Microsoft Dynamics 365 Finance.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cf19d69c498da32594e17e16fb83ed25e6747982
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142992"
---
# <a name="er-map-data-model-to-selected-data-sources"></a><span data-ttu-id="41f87-103">Rafræn skýrslugerð Varpa gagnalíkani í valda gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="41f87-103">ER Map data model to selected data sources</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="41f87-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur varpað rafræna skýrslugerð (ER) gagnalíkani á valda gagnaveitur.</span><span class="sxs-lookup"><span data-stu-id="41f87-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can map an Electronic reporting (ER) data model to selected data sources.</span></span> <span data-ttu-id="41f87-105">Þessi líkanavörpun verður síðar notuð sem gagnaveita í skilgreiningu sniðs sem verður notað til að stjórna skjölum rafrænna greiðsla.</span><span class="sxs-lookup"><span data-stu-id="41f87-105">This model mapping will later be used as a data source in a format configuration that will be used to manage electronic payment documents.</span></span> <span data-ttu-id="41f87-106">Í þessu dæmi er varpað gagnalíkani fyrir dæmi um fyrirtæki, Litware, Inc. til gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="41f87-106">In this example, you map a data model for sample company, Litware, Inc. to data sources.</span></span> <span data-ttu-id="41f87-107">Til að ljúka þessum skrefum, verður fyrst að ljúka skrefum í ferlinu „Velja gagnaveita fyrir líkanavörpun”.</span><span class="sxs-lookup"><span data-stu-id="41f87-107">To complete these steps, you must first complete the steps in the "Select data sources for model mapping" procedure.</span></span>


## <a name="open-er-configurations-tree"></a><span data-ttu-id="41f87-108">Opna grunnstillingatré rafrænnar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="41f87-108">Open ER configurations tree</span></span>
1. <span data-ttu-id="41f87-109">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="41f87-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="41f87-110">Smellt er á Skilgreiningum.</span><span class="sxs-lookup"><span data-stu-id="41f87-110">Click Configurations.</span></span>

## <a name="select-created-model-mapping"></a><span data-ttu-id="41f87-111">Veljið stofnuð líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="41f87-111">Select created model mapping</span></span>
1. <span data-ttu-id="41f87-112">Veljið 'Greiðslur (einfaldað líkan)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-112">In the tree, select 'Payments (simplified model)'.</span></span>
    * <span data-ttu-id="41f87-113">Gangið úr skugga um að skilgreiningarlíkanið „Greiðslur (einfaldað líkan)” hefur verið stofnuð fyrirfram.</span><span class="sxs-lookup"><span data-stu-id="41f87-113">Make sure that the model configuration "Payments (simplified model)" has been created in advance.</span></span> <span data-ttu-id="41f87-114">Að öðrum kosti skal stoppa núna og koma aftur eftir að lokið við verkefnaleiðbeiningar „Mynda nýja grunnstillingu með gagnalíkan af völdu léni“.</span><span class="sxs-lookup"><span data-stu-id="41f87-114">Otherwise, stop now and return after completion of the task guide 'Create a new configuration with data model of the selected domain'.</span></span>  
2. <span data-ttu-id="41f87-115">Smellt er á hönnuður Líkana.</span><span class="sxs-lookup"><span data-stu-id="41f87-115">Click Model designer.</span></span>
3. <span data-ttu-id="41f87-116">Smellt er á Varpa líkani á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="41f87-116">Click Map model to datasource.</span></span>
4. <span data-ttu-id="41f87-117">Veljið færsluna 'CT vörpun'.</span><span class="sxs-lookup"><span data-stu-id="41f87-117">Select the 'CT mapping' record.</span></span>
    * <span data-ttu-id="41f87-118">Vörpun CT</span><span class="sxs-lookup"><span data-stu-id="41f87-118">CT mapping</span></span>  

## <a name="bind-created-data-sources-to-data-model-elements"></a><span data-ttu-id="41f87-119">Binda stofnaða gagnaveitur við þætti gagnalíkans</span><span class="sxs-lookup"><span data-stu-id="41f87-119">Bind created data sources to data model elements</span></span>
1. <span data-ttu-id="41f87-120">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="41f87-120">Click Designer.</span></span>
2. <span data-ttu-id="41f87-121">Í trénu, skal velja 'Processing date & time(ProcessingDateTime)'.</span><span class="sxs-lookup"><span data-stu-id="41f87-121">In the tree, select 'Processing date & time(ProcessingDateTime)'.</span></span>
3. <span data-ttu-id="41f87-122">Veljið ‚Processing date(ProcessingDateTime)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-122">In the tree, select 'Processing date(ProcessingDateTime)'.</span></span>
4. <span data-ttu-id="41f87-123">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-123">Click Bind.</span></span>
5. <span data-ttu-id="41f87-124">Veljið ‚Payment message identification(MessageIdentification)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-124">In the tree, select 'Payment message identification(MessageIdentification)'.</span></span>
6. <span data-ttu-id="41f87-125">Í trénu skal víkka út „Færslur“.</span><span class="sxs-lookup"><span data-stu-id="41f87-125">In the tree, expand 'Transactions'.</span></span>
7. <span data-ttu-id="41f87-126">Veljið ''Transactions\Journal batch number(JournalNum)'., í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-126">In the tree, select 'Transactions\Journal batch number(JournalNum)'.</span></span>
8. <span data-ttu-id="41f87-127">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-127">Click Bind.</span></span>
9. <span data-ttu-id="41f87-128">Í trénu skal velja „Greiðslur“.</span><span class="sxs-lookup"><span data-stu-id="41f87-128">In the tree, select 'Payments'.</span></span>
10. <span data-ttu-id="41f87-129">Í trénu skal velja „Færslur“.</span><span class="sxs-lookup"><span data-stu-id="41f87-129">In the tree, select 'Transactions'.</span></span>
11. <span data-ttu-id="41f87-130">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-130">Click Bind.</span></span>
12. <span data-ttu-id="41f87-131">Í trénu, útvíkka ' Greiðslur = Færslur.</span><span class="sxs-lookup"><span data-stu-id="41f87-131">In the tree, expand 'Payments= Transactions'.</span></span>
13. <span data-ttu-id="41f87-132">Í trénu, útvíkka ' Payments = Transactions\Creditor'.</span><span class="sxs-lookup"><span data-stu-id="41f87-132">In the tree, expand 'Payments= Transactions\Creditor'.</span></span>
14. <span data-ttu-id="41f87-133">Í trénu, útvíkka ' Payments = Transactions\Creditor\Account'.</span><span class="sxs-lookup"><span data-stu-id="41f87-133">In the tree, expand 'Payments= Transactions\Creditor\Account'.</span></span>
15. <span data-ttu-id="41f87-134">Í trénu, skal velja ' Payments = Transactions\Creditor\Account\Currency code(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="41f87-134">In the tree, select 'Payments= Transactions\Creditor\Account\Currency code(Currency)'.</span></span>
16. <span data-ttu-id="41f87-135">Útvíkka 'Transactions\vendBankAccountInTransactionCompany()', í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-135">In the tree, expand 'Transactions\vendBankAccountInTransactionCompany()'.</span></span>
17. <span data-ttu-id="41f87-136">Veljið 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-136">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Currency(CurrencyCode)'.</span></span>
18. <span data-ttu-id="41f87-137">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-137">Click Bind.</span></span>
19. <span data-ttu-id="41f87-138">Í trénu, skal velja ' Payments = Transactions\Creditor\Account\IBAN code(IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="41f87-138">In the tree, select 'Payments= Transactions\Creditor\Account\IBAN code(IBAN)'.</span></span>
20. <span data-ttu-id="41f87-139">Veljið 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-139">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\IBAN(BankIBAN)'.</span></span>
21. <span data-ttu-id="41f87-140">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-140">Click Bind.</span></span>
22. <span data-ttu-id="41f87-141">Í trénu, skal velja ' Payments = Transactions\Creditor\Account\Number'.</span><span class="sxs-lookup"><span data-stu-id="41f87-141">In the tree, select 'Payments= Transactions\Creditor\Account\Number'.</span></span>
23. <span data-ttu-id="41f87-142">Veljið 'Transactions\vendBankAccountInTransactionCompany () \Bank lykil number(AccountNum)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-142">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Bank account number(AccountNum)'.</span></span>
24. <span data-ttu-id="41f87-143">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-143">Click Bind.</span></span>
25. <span data-ttu-id="41f87-144">Í trénu, útvíkka ' Payments = Transactions\Creditor\Agent'.</span><span class="sxs-lookup"><span data-stu-id="41f87-144">In the tree, expand 'Payments= Transactions\Creditor\Agent'.</span></span>
26. <span data-ttu-id="41f87-145">Í trénu, skal velja ' Payments = Transactions\Creditor\Agent\Name'.</span><span class="sxs-lookup"><span data-stu-id="41f87-145">In the tree, select 'Payments= Transactions\Creditor\Agent\Name'.</span></span>
27. <span data-ttu-id="41f87-146">Veljið '\Name Transactions\vendBankAccountInTransactionCompany ()', í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-146">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Name'.</span></span>
28. <span data-ttu-id="41f87-147">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-147">Click Bind.</span></span>
29. <span data-ttu-id="41f87-148">Í trénu, skal velja ' Payments = Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span><span class="sxs-lookup"><span data-stu-id="41f87-148">In the tree, select 'Payments= Transactions\Creditor\Agent\Routing number(RoutingNumber)'.</span></span>
30. <span data-ttu-id="41f87-149">Veljið 'Transactions\vendBankAccountInTransactionCompany () \Routing number(RegistrationNum)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-149">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\Routing number(RegistrationNum)'.</span></span>
31. <span data-ttu-id="41f87-150">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-150">Click Bind.</span></span>
32. <span data-ttu-id="41f87-151">Í trénu, skal velja ' Payments = Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span><span class="sxs-lookup"><span data-stu-id="41f87-151">In the tree, select 'Payments= Transactions\Creditor\Agent\SWIFT code(SWIFT)'.</span></span>
33. <span data-ttu-id="41f87-152">Veljið 'Transactions\vendBankAccountInTransactionCompany () \SWIFT code(SWIFTNo)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-152">In the tree, select 'Transactions\vendBankAccountInTransactionCompany()\SWIFT code(SWIFTNo)'.</span></span>
34. <span data-ttu-id="41f87-153">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-153">Click Bind.</span></span>
35. <span data-ttu-id="41f87-154">Í trénu, skal velja ' Payments = Transactions\Creditor\Name'.</span><span class="sxs-lookup"><span data-stu-id="41f87-154">In the tree, select 'Payments= Transactions\Creditor\Name'.</span></span>
36. <span data-ttu-id="41f87-155">Útvíkka 'Transactions\findVendTable()', í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-155">In the tree, expand 'Transactions\findVendTable()'.</span></span>
37. <span data-ttu-id="41f87-156">Veljið ‚Transactions\findVendTable()\name()', í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-156">In the tree, select 'Transactions\findVendTable()\name()'.</span></span>
38. <span data-ttu-id="41f87-157">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-157">Click Bind.</span></span>
39. <span data-ttu-id="41f87-158">Í trénu, skal velja ' Payments = Transactions\Currency code(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="41f87-158">In the tree, select 'Payments= Transactions\Currency code(Currency)'.</span></span>
40. <span data-ttu-id="41f87-159">Í trénu skal víkka út „Færslur\>Tengsl“.</span><span class="sxs-lookup"><span data-stu-id="41f87-159">In the tree, expand 'Transactions\>Relations'.</span></span>
41. <span data-ttu-id="41f87-160">Í trénu skal víkka út „Færslur\>Tengsl\Gjaldmiðill tafla(Gjaldmiðill)“.</span><span class="sxs-lookup"><span data-stu-id="41f87-160">In the tree, expand 'Transactions\>Relations\Currency table(Currency)'.</span></span>
42. <span data-ttu-id="41f87-161">Í trénu skal velja „Færslur\>Tengsl\Gjaldmiðill tafla(Gjaldmiðill)\Gjaldmiðill kóði(CurrencyCodeISO)“.</span><span class="sxs-lookup"><span data-stu-id="41f87-161">In the tree, select 'Transactions\>Relations\Currency table(Currency)\Currency code(CurrencyCodeISO)'.</span></span>
43. <span data-ttu-id="41f87-162">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-162">Click Bind.</span></span>
44. <span data-ttu-id="41f87-163">Í trénu, útvíkka ' Payments= Transactions\Debtor'.</span><span class="sxs-lookup"><span data-stu-id="41f87-163">In the tree, expand 'Payments= Transactions\Debtor'.</span></span>
45. <span data-ttu-id="41f87-164">Í trénu, útvíkka 'Payments= Transactions\Debtor\Account'.</span><span class="sxs-lookup"><span data-stu-id="41f87-164">In the tree, expand 'Payments= Transactions\Debtor\Account'.</span></span>
46. <span data-ttu-id="41f87-165">Í trénu, skal velja ' Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span><span class="sxs-lookup"><span data-stu-id="41f87-165">In the tree, select 'Payments= Transactions\Debtor\Account\Currency code(Currency)'.</span></span>
47. <span data-ttu-id="41f87-166">Veljið 'Bank Account(BankAccount)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-166">In the tree, select 'Bank Account(BankAccount)'.</span></span>
48. <span data-ttu-id="41f87-167">Útvíkka 'Bank Account(BankAccount)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-167">In the tree, expand 'Bank Account(BankAccount)'.</span></span>
49. <span data-ttu-id="41f87-168">Veljið 'Bank Account(BankAccount)\Currency(CurrencyCode)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-168">In the tree, select 'Bank Account(BankAccount)\Currency(CurrencyCode)'.</span></span>
50. <span data-ttu-id="41f87-169">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-169">Click Bind.</span></span>
51. <span data-ttu-id="41f87-170">Í trénu, skal velja ' Bank Account(BankAccount) \IBAN'.</span><span class="sxs-lookup"><span data-stu-id="41f87-170">In the tree, select 'Bank Account(BankAccount)\IBAN'.</span></span>
52. <span data-ttu-id="41f87-171">Í trénu, skal velja ' Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span><span class="sxs-lookup"><span data-stu-id="41f87-171">In the tree, select 'Payments= Transactions\Debtor\Account\IBAN code(IBAN)'.</span></span>
53. <span data-ttu-id="41f87-172">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-172">Click Bind.</span></span>
54. <span data-ttu-id="41f87-173">Í trénu, skal velja ' Payments= Transactions\Debtor\Account\Number'.</span><span class="sxs-lookup"><span data-stu-id="41f87-173">In the tree, select 'Payments= Transactions\Debtor\Account\Number'.</span></span>
55. <span data-ttu-id="41f87-174">Veljið 'Bank Account(BankAccount)\Bank account number(AccountNum)‘, í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-174">In the tree, select 'Bank Account(BankAccount)\Bank account number(AccountNum)'.</span></span>
56. <span data-ttu-id="41f87-175">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-175">Click Bind.</span></span>
57. <span data-ttu-id="41f87-176">Í trénu, útvíkka ' Payments= Transactions\Debtor\Agent'.</span><span class="sxs-lookup"><span data-stu-id="41f87-176">In the tree, expand 'Payments= Transactions\Debtor\Agent'.</span></span>
58. <span data-ttu-id="41f87-177">Í trénu, skal velja ' Payments= Transactions\Debtor\Agent\Name'.</span><span class="sxs-lookup"><span data-stu-id="41f87-177">In the tree, select 'Payments= Transactions\Debtor\Agent\Name'.</span></span>
59. <span data-ttu-id="41f87-178">Í trénu skal velja 'Bank Account(BankAccount)\Name'.</span><span class="sxs-lookup"><span data-stu-id="41f87-178">In the tree, select 'Bank Account(BankAccount)\Name'.</span></span>
60. <span data-ttu-id="41f87-179">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-179">Click Bind.</span></span>
61. <span data-ttu-id="41f87-180">Í trénu, skal velja ' Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span><span class="sxs-lookup"><span data-stu-id="41f87-180">In the tree, select 'Payments= Transactions\Debtor\Agent\Routing number(RoutingNumber)'.</span></span>
62. <span data-ttu-id="41f87-181">Í trénu skal velja 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span><span class="sxs-lookup"><span data-stu-id="41f87-181">In the tree, select 'Bank Account(BankAccount)\Routing number(RegistrationNum)'.</span></span>
63. <span data-ttu-id="41f87-182">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-182">Click Bind.</span></span>
64. <span data-ttu-id="41f87-183">Í trénu, skal velja ' Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span><span class="sxs-lookup"><span data-stu-id="41f87-183">In the tree, select 'Payments= Transactions\Debtor\Agent\SWIFT code(SWIFT)'.</span></span>
65. <span data-ttu-id="41f87-184">Í trénu, skal velja 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span><span class="sxs-lookup"><span data-stu-id="41f87-184">In the tree, select 'Bank Account(BankAccount)\SWIFT code(SWIFTNo)'.</span></span>
66. <span data-ttu-id="41f87-185">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-185">Click Bind.</span></span>
67. <span data-ttu-id="41f87-186">Í trénu, skal velja ' Payments= Transactions\Debtor\Name'.</span><span class="sxs-lookup"><span data-stu-id="41f87-186">In the tree, select 'Payments= Transactions\Debtor\Name'.</span></span>
68. <span data-ttu-id="41f87-187">Í trénu skal velja 'Company information(Company)'.</span><span class="sxs-lookup"><span data-stu-id="41f87-187">In the tree, select 'Company information(Company)'.</span></span>
69. <span data-ttu-id="41f87-188">Útvíkka, í trénu 'Company information(Company)'.</span><span class="sxs-lookup"><span data-stu-id="41f87-188">In the tree, expand 'Company information(Company)'.</span></span>
70. <span data-ttu-id="41f87-189">Veljið 'Company information(Company)\Name‘, í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-189">In the tree, select 'Company information(Company)\Name'.</span></span>
71. <span data-ttu-id="41f87-190">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-190">Click Bind.</span></span>
72. <span data-ttu-id="41f87-191">Í trénu, skal velja ' Payments= Transactions\Description'.</span><span class="sxs-lookup"><span data-stu-id="41f87-191">In the tree, select 'Payments= Transactions\Description'.</span></span>
73. <span data-ttu-id="41f87-192">Veljið 'Transactions\Description(Txt)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-192">In the tree, select 'Transactions\Description(Txt)'.</span></span>
74. <span data-ttu-id="41f87-193">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-193">Click Bind.</span></span>
75. <span data-ttu-id="41f87-194">Í trénu, skal velja ''Payments= Transactions\End to end identification code(End2EndID)'.</span><span class="sxs-lookup"><span data-stu-id="41f87-194">In the tree, select 'Payments= Transactions\End to end identification code(End2EndID)'.</span></span>
76. <span data-ttu-id="41f87-195">Í trénu skal velja „Færslur\$EndToEndID“.</span><span class="sxs-lookup"><span data-stu-id="41f87-195">In the tree, select 'Transactions\$EndToEndID'.</span></span>
77. <span data-ttu-id="41f87-196">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-196">Click Bind.</span></span>
78. <span data-ttu-id="41f87-197">Í trénu, skal velja ''Payments= Transactions\Instructed amount(InstructedAmount)'.</span><span class="sxs-lookup"><span data-stu-id="41f87-197">In the tree, select 'Payments= Transactions\Instructed amount(InstructedAmount)'.</span></span>
79. <span data-ttu-id="41f87-198">Í trénu skal velja „Færslur\$Upphæð“.</span><span class="sxs-lookup"><span data-stu-id="41f87-198">In the tree, select 'Transactions\$Amount'.</span></span>
80. <span data-ttu-id="41f87-199">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-199">Click Bind.</span></span>
81. <span data-ttu-id="41f87-200">Í trénu skal velja 'Payments= Transactions\Transaction date(TransactionDate)'.</span><span class="sxs-lookup"><span data-stu-id="41f87-200">In the tree, select 'Payments= Transactions\Transaction date(TransactionDate)'.</span></span>
82. <span data-ttu-id="41f87-201">Veljið 'Transactions\Date(TransDate)', í trénu.</span><span class="sxs-lookup"><span data-stu-id="41f87-201">In the tree, select 'Transactions\Date(TransDate)'.</span></span>
83. <span data-ttu-id="41f87-202">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="41f87-202">Click Bind.</span></span>

## <a name="validate-created-mapping"></a><span data-ttu-id="41f87-203">Villuleita stofnaða vörpun</span><span class="sxs-lookup"><span data-stu-id="41f87-203">Validate created mapping</span></span>
1. <span data-ttu-id="41f87-204">Smella á Villuleita.</span><span class="sxs-lookup"><span data-stu-id="41f87-204">Click Validate.</span></span>
    * <span data-ttu-id="41f87-205">Sannprófa nýja vörpun til að tryggja að allar bindingar séu í lagi.</span><span class="sxs-lookup"><span data-stu-id="41f87-205">Validate the new mapping to ensure that all bindings are okay.</span></span>  
2. <span data-ttu-id="41f87-206">Með því að smella á örina má stækka eða fella saman hlutann Villulisti.</span><span class="sxs-lookup"><span data-stu-id="41f87-206">Click the arrow to expand or collapse the Error List section.</span></span>
3. <span data-ttu-id="41f87-207">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="41f87-207">Click Save.</span></span>
4. <span data-ttu-id="41f87-208">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="41f87-208">Close the page.</span></span>
5. <span data-ttu-id="41f87-209">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="41f87-209">Close the page.</span></span>
6. <span data-ttu-id="41f87-210">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="41f87-210">Close the page.</span></span>

## <a name="change-the-status-of-the-current-version-of-model-configuration"></a><span data-ttu-id="41f87-211">Breyta stöðu gildandi útgáfu skilgreiningar líkans</span><span class="sxs-lookup"><span data-stu-id="41f87-211">Change the status of the current version of model configuration</span></span>
1. <span data-ttu-id="41f87-212">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="41f87-212">Click Change status.</span></span>
    * <span data-ttu-id="41f87-213">Breyta stöðu hannaðrar grunnstillingar líkans - úr Drög í Lokið til að gera tiltækur fyrir hönnun greiðslusniðs.</span><span class="sxs-lookup"><span data-stu-id="41f87-213">Change the status of designed model configuration – from Draft to Completed to make it available for payment format design.</span></span>  
2. <span data-ttu-id="41f87-214">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="41f87-214">Click Complete.</span></span>
    * <span data-ttu-id="41f87-215">Velja Lokið.</span><span class="sxs-lookup"><span data-stu-id="41f87-215">Select Complete.</span></span>  
3. <span data-ttu-id="41f87-216">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="41f87-216">In the Description field, type a value.</span></span>
    * <span data-ttu-id="41f87-217">Til dæmis „Útgáfa 1“.</span><span class="sxs-lookup"><span data-stu-id="41f87-217">For example, 'version 1'.</span></span>  
4. <span data-ttu-id="41f87-218">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="41f87-218">Click OK.</span></span>
5. <span data-ttu-id="41f87-219">Velja lokna útgáfu af núgildandi skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="41f87-219">Select the completed version of the current configuration.</span></span>
    * <span data-ttu-id="41f87-220">Athugið að stofnuð skilgreining er vistuð sem lokin útgáfa 1.</span><span class="sxs-lookup"><span data-stu-id="41f87-220">Note that the created configuration is saved as completed version 1.</span></span>  

