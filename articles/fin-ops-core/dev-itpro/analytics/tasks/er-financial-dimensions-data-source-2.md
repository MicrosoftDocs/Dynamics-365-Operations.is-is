---
title: Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 2 - líkanavörpun)
description: Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 788564bfd7c3df146266976d8eef6621ff37ca2a
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550626"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="fc899-103">Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 2 - líkanavörpun)</span><span class="sxs-lookup"><span data-stu-id="fc899-103">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fc899-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="fc899-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="fc899-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="fc899-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="fc899-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á “Rafræn skýrslugerð notar fjárhagsvíddir sem gagnaveitu (Hluti 1: Hönnun gagnalíkans” ferli.</span><span class="sxs-lookup"><span data-stu-id="fc899-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="fc899-107">Bæta við nauðsynlegar gagnaveitur við líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="fc899-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="fc899-108">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="fc899-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="fc899-109">Veljið 'dæmi um líkan fyrir fjárhagsvíddir', í trénu.</span><span class="sxs-lookup"><span data-stu-id="fc899-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="fc899-110">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="fc899-110">Click Designer.</span></span>
4. <span data-ttu-id="fc899-111">Smellt er á Varpa líkani á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="fc899-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="fc899-112">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="fc899-112">Click New.</span></span>
6. <span data-ttu-id="fc899-113">Í reitnum Skilgreining er valið „færsla“.</span><span class="sxs-lookup"><span data-stu-id="fc899-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="fc899-114">Í reitnum Heiti skal færa inn 'gagnakortalagning vídda'.</span><span class="sxs-lookup"><span data-stu-id="fc899-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="fc899-115">Í reitnum lýsing skal færa inn 'gagnakortalagning vídda'.</span><span class="sxs-lookup"><span data-stu-id="fc899-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="fc899-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="fc899-116">Click Save.</span></span>
10. <span data-ttu-id="fc899-117">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="fc899-117">Click Designer.</span></span>
11. <span data-ttu-id="fc899-118">Í trénu skal velja „Dynamics 365 for Operations\Table“.</span><span class="sxs-lookup"><span data-stu-id="fc899-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="fc899-119">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="fc899-119">Click Add root.</span></span>
13. <span data-ttu-id="fc899-120">Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.</span><span class="sxs-lookup"><span data-stu-id="fc899-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="fc899-121">Í reitinn Tafla skal færa inn ‚CompanyInfo‘.</span><span class="sxs-lookup"><span data-stu-id="fc899-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="fc899-122">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="fc899-122">Click OK.</span></span>
16. <span data-ttu-id="fc899-123">Í trénu skal velja 'Functions\Financial dimensions details'.</span><span class="sxs-lookup"><span data-stu-id="fc899-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="fc899-124">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="fc899-124">Click Add root.</span></span>
    * <span data-ttu-id="fc899-125">Þennan gagnagjafa tilgreinir hvernig svið fjárhagsvídda er skilgreint fyrir allar skýrslur sem nota þetta líkan sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="fc899-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="fc899-126">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="fc899-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="fc899-127">Velja skal Já í reitnum Óska eftir víddum.</span><span class="sxs-lookup"><span data-stu-id="fc899-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="fc899-128">Velja skal Já til að leyfa notanda að velja víddir á keyrslutíma á skjámyndinni svargluggai Notanda.</span><span class="sxs-lookup"><span data-stu-id="fc899-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="fc899-129">Ef stillt á Nei verða allar fjárhagsvíddir núverandi tilviks notaðar sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="fc899-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="fc899-130">Í valreit fjárhagsvídda skal velja lögaðila</span><span class="sxs-lookup"><span data-stu-id="fc899-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="fc899-131">Veljið Allt til að leyfa notanda að velja víddir sem óskað er eftir fyrir núverandi tilvik í uppflettisvæðinu.</span><span class="sxs-lookup"><span data-stu-id="fc899-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="fc899-132">Veljið Lögaðila til að leyfa notanda að velja víddir sem óskað er eftir fyrir fyrirtæki í uppflettisvæðinu.</span><span class="sxs-lookup"><span data-stu-id="fc899-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="fc899-133">Velja skal Vídd til að leyfa notanda að velja víddir sem nota stakar víddarsamstæður.</span><span class="sxs-lookup"><span data-stu-id="fc899-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="fc899-134">Veljið Já í svæðinu Biðja um aðallykil.</span><span class="sxs-lookup"><span data-stu-id="fc899-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="fc899-135">Stilltu 'Biðja um aðallykil' á Já til að leyfa notendum að velja aðallykilinn sem hluta af listanum yfir víddir.</span><span class="sxs-lookup"><span data-stu-id="fc899-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="fc899-136">Ef stillt er á Nei, verður aðallykilinn ekki teknar með á lista yfir víddir og valkosturinn "Er aðallykill skylda" er virkjaður.</span><span class="sxs-lookup"><span data-stu-id="fc899-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="fc899-137">Ef "Er aðallykill áskilinn' er stilltur á já skal hafa aðallykillinn með í lista yfir víddir óháð vali notanda.</span><span class="sxs-lookup"><span data-stu-id="fc899-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="fc899-138">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="fc899-138">Click OK.</span></span>
23. <span data-ttu-id="fc899-139">Í trénu skal velja 'Dynamics 365 for Operations\Table records'.</span><span class="sxs-lookup"><span data-stu-id="fc899-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="fc899-140">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="fc899-140">Click Add root.</span></span>
25. <span data-ttu-id="fc899-141">Í svæðið Heiti, færðu inn 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="fc899-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="fc899-142">Velja skal Já í reitnum Óska eftir fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="fc899-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="fc899-143">Í reitnum Tafla skal færa inn ‚LedgerJournalTable‘.</span><span class="sxs-lookup"><span data-stu-id="fc899-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="fc899-144">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="fc899-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="fc899-145">Varpa einingum gagnalíkans við gagnaveitur sem bætt var við.</span><span class="sxs-lookup"><span data-stu-id="fc899-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="fc899-146">Stækkið „færslubók“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="fc899-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="fc899-147">Í trénu skal víkka út 'Journal\Transaction'.</span><span class="sxs-lookup"><span data-stu-id="fc899-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="fc899-148">Í trénu skal víkka út 'Journal\Transaction\Dimensions data'.</span><span class="sxs-lookup"><span data-stu-id="fc899-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="fc899-149">Í trénu skal víkka út 'Dimensions setting'.</span><span class="sxs-lookup"><span data-stu-id="fc899-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="fc899-150">Í trénu skal víkka út 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="fc899-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="fc899-151">Í trénu, útvíkka „LedgerJournal\<Relations“.</span><span class="sxs-lookup"><span data-stu-id="fc899-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="fc899-152">Í trénu, útvíkka expand „LedgerJournal\<Relations\LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="fc899-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="fc899-153">Í trénu, útvíkka „LedgerJournal\<Relations\LedgerJournalTrans\Voucher“.</span><span class="sxs-lookup"><span data-stu-id="fc899-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="fc899-154">Í trénu skal velja 'Journal\Transaction\Voucher'.</span><span class="sxs-lookup"><span data-stu-id="fc899-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="fc899-155">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="fc899-155">Click Bind.</span></span>
11. <span data-ttu-id="fc899-156">Í trénu, skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.</span><span class="sxs-lookup"><span data-stu-id="fc899-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="fc899-157">Athugið að fyrir allar tilvísanir í fjárhagsvíddir sem eru stilltar á, til dæmis LedgerDimension, er samsvarandi vara gagnaveitu tiltæk (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="fc899-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="fc899-158">Þessi gagnaveituvara býður upp á fjárhagsvíddir þessara vídda sem eru stilltar sem listi færslunnar.</span><span class="sxs-lookup"><span data-stu-id="fc899-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="fc899-159">Í trénu, skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.</span><span class="sxs-lookup"><span data-stu-id="fc899-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="fc899-160">Í trénu skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions“.</span><span class="sxs-lookup"><span data-stu-id="fc899-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="fc899-161">Í trénu skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value“.</span><span class="sxs-lookup"><span data-stu-id="fc899-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="fc899-162">Í trénu skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition“.</span><span class="sxs-lookup"><span data-stu-id="fc899-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="fc899-163">Í trénu, skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name“.</span><span class="sxs-lookup"><span data-stu-id="fc899-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="fc899-164">Í trénu, skal velja 'Journal\Transaction\Dimensions data\Name'.</span><span class="sxs-lookup"><span data-stu-id="fc899-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="fc899-165">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="fc899-165">Click Bind.</span></span>
19. <span data-ttu-id="fc899-166">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description“.</span><span class="sxs-lookup"><span data-stu-id="fc899-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="fc899-167">Í trénu, skal velja 'Journal\Transaction\Dimensions data\Description'.</span><span class="sxs-lookup"><span data-stu-id="fc899-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="fc899-168">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="fc899-168">Click Bind.</span></span>
22. <span data-ttu-id="fc899-169">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code“.</span><span class="sxs-lookup"><span data-stu-id="fc899-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="fc899-170">Í trénu, skal velja 'Journal\Transaction\Dimensions data\Code'.</span><span class="sxs-lookup"><span data-stu-id="fc899-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="fc899-171">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="fc899-171">Click Bind.</span></span>
25. <span data-ttu-id="fc899-172">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions“.</span><span class="sxs-lookup"><span data-stu-id="fc899-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="fc899-173">Í trénu, skal velja 'Journal\Transaction\Dimensions data'.</span><span class="sxs-lookup"><span data-stu-id="fc899-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="fc899-174">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="fc899-174">Click Bind.</span></span>
28. <span data-ttu-id="fc899-175">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)“.</span><span class="sxs-lookup"><span data-stu-id="fc899-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="fc899-176">Í trénu, skal velja 'Journal\Transaction\Debit'.</span><span class="sxs-lookup"><span data-stu-id="fc899-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="fc899-177">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="fc899-177">Click Bind.</span></span>
31. <span data-ttu-id="fc899-178">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)“.</span><span class="sxs-lookup"><span data-stu-id="fc899-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="fc899-179">Í trénu, skal velja 'Journal\Transaction\Date'.</span><span class="sxs-lookup"><span data-stu-id="fc899-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="fc899-180">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="fc899-180">Click Bind.</span></span>
34. <span data-ttu-id="fc899-181">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)“.</span><span class="sxs-lookup"><span data-stu-id="fc899-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="fc899-182">Í trénu, skal velja 'Journal\Transaction\Currency'.</span><span class="sxs-lookup"><span data-stu-id="fc899-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="fc899-183">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="fc899-183">Click Bind.</span></span>
37. <span data-ttu-id="fc899-184">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)“.</span><span class="sxs-lookup"><span data-stu-id="fc899-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="fc899-185">Í trénu, skal velja 'Journal\Transaction\Credit'.</span><span class="sxs-lookup"><span data-stu-id="fc899-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="fc899-186">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="fc899-186">Click Bind.</span></span>
40. <span data-ttu-id="fc899-187">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="fc899-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="fc899-188">Í trénu, skal velja 'Journal\Transaction'.</span><span class="sxs-lookup"><span data-stu-id="fc899-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="fc899-189">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="fc899-189">Click Bind.</span></span>
43. <span data-ttu-id="fc899-190">Í trénu, skal velja 'LedgerJournal\Journal batch number(JournalNum)'.</span><span class="sxs-lookup"><span data-stu-id="fc899-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="fc899-191">Í trénu, skal velja 'Journal\Batch'.</span><span class="sxs-lookup"><span data-stu-id="fc899-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="fc899-192">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="fc899-192">Click Bind.</span></span>
46. <span data-ttu-id="fc899-193">Í trénu, skal velja 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="fc899-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="fc899-194">Í trénu, skal velja 'Journal'.</span><span class="sxs-lookup"><span data-stu-id="fc899-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="fc899-195">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="fc899-195">Click Bind.</span></span>
49. <span data-ttu-id="fc899-196">Í trénu, skal víkka út 'Dimensions'.</span><span class="sxs-lookup"><span data-stu-id="fc899-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="fc899-197">Í trénu, skal víkka út 'Dimensions\Main account and dimensions'.</span><span class="sxs-lookup"><span data-stu-id="fc899-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="fc899-198">Í trénu, skal víkka út 'Dimensions\Main account and dimensions\Definition'.</span><span class="sxs-lookup"><span data-stu-id="fc899-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="fc899-199">Í trénu, skal velja 'Dimensions\Main account and dimensions\Definition\Name'.</span><span class="sxs-lookup"><span data-stu-id="fc899-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="fc899-200">Í trénu, skal velja 'Dimensions setting\Code'.</span><span class="sxs-lookup"><span data-stu-id="fc899-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="fc899-201">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="fc899-201">Click Bind.</span></span>
55. <span data-ttu-id="fc899-202">Í trénu, skal velja 'Dimensions\Main account and dimensions\Definition\Report column name'.</span><span class="sxs-lookup"><span data-stu-id="fc899-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="fc899-203">Í trénu, skal velja 'Dimensions setting\Name'.</span><span class="sxs-lookup"><span data-stu-id="fc899-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="fc899-204">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="fc899-204">Click Bind.</span></span>
58. <span data-ttu-id="fc899-205">Í trénu, skal velja 'Dimensions\Main account and dimensions'.</span><span class="sxs-lookup"><span data-stu-id="fc899-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="fc899-206">Í trénu, skal velja 'Dimensions setting'.</span><span class="sxs-lookup"><span data-stu-id="fc899-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="fc899-207">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="fc899-207">Click Bind.</span></span>
61. <span data-ttu-id="fc899-208">Í trénu, skal velja 'Company'.</span><span class="sxs-lookup"><span data-stu-id="fc899-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="fc899-209">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="fc899-209">Click Edit.</span></span>
63. <span data-ttu-id="fc899-210">Í svæðinu expressionAsStringText skal færa inn 'Company.'find()'.'name()''.</span><span class="sxs-lookup"><span data-stu-id="fc899-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="fc899-211">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="fc899-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="fc899-212">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="fc899-212">Click Save.</span></span>
65. <span data-ttu-id="fc899-213">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="fc899-213">Close the page.</span></span>
66. <span data-ttu-id="fc899-214">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="fc899-214">Click Save.</span></span>
67. <span data-ttu-id="fc899-215">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="fc899-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="fc899-216">Ljúktu við þessa útgáfu af drögum að líkani.</span><span class="sxs-lookup"><span data-stu-id="fc899-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="fc899-217">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="fc899-217">Close the page.</span></span>
2. <span data-ttu-id="fc899-218">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="fc899-218">Close the page.</span></span>
3. <span data-ttu-id="fc899-219">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="fc899-219">Click Change status.</span></span>
4. <span data-ttu-id="fc899-220">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="fc899-220">Click Complete.</span></span>
5. <span data-ttu-id="fc899-221">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="fc899-221">Click OK.</span></span>
