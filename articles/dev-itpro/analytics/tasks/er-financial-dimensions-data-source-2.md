--- 
title: "Varpa líkönum til að nota fjárhagsvíddir sem gagnaveitu í rafrænni skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur."
author: NickSelin
manager: AnnBe
ms.date: 10/14/2016
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
ms.sourcegitcommit: 7be3e9970e2599c159e7c9d414b54876d0116350
ms.openlocfilehash: a5fa6fb07fb2ba08812826acba748b38738bb468
ms.contentlocale: is-is
ms.lasthandoff: 03/09/2018

---
# <a name="map-models--to-use-financial-dimensions-as-a-data-source-for-electronic-reporting-er"></a><span data-ttu-id="f195f-103">Varpa líkönum til að nota fjárhagsvíddir sem gagnaveitu í rafrænni skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="f195f-103">Map models  to use financial dimensions as a data source for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f195f-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="f195f-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="f195f-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="f195f-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="f195f-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í á “Rafræn skýrslugerð notar fjárhagsvíddir sem gagnaveitu (Hluti 1: Hönnun gagnalíkans” ferli.</span><span class="sxs-lookup"><span data-stu-id="f195f-106">To complete these steps, you must first complete the steps in the “ER Use financial dimensions as a data source (Part 1: Design data model” procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="f195f-107">Bæta við nauðsynlegar gagnaveitur við líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="f195f-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="f195f-108">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="f195f-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="f195f-109">Veljið 'dæmi um líkan fyrir fjárhagsvíddir', í trénu.</span><span class="sxs-lookup"><span data-stu-id="f195f-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="f195f-110">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="f195f-110">Click Designer.</span></span>
4. <span data-ttu-id="f195f-111">Smellt er á Varpa líkani á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="f195f-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="f195f-112">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="f195f-112">Click New.</span></span>
6. <span data-ttu-id="f195f-113">Í reitnum Skilgreining er valið „færsla“.</span><span class="sxs-lookup"><span data-stu-id="f195f-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="f195f-114">Í reitnum Heiti skal færa inn 'gagnakortalagning vídda'.</span><span class="sxs-lookup"><span data-stu-id="f195f-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="f195f-115">Í reitnum lýsing skal færa inn 'gagnakortalagning vídda'.</span><span class="sxs-lookup"><span data-stu-id="f195f-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="f195f-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f195f-116">Click Save.</span></span>
10. <span data-ttu-id="f195f-117">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="f195f-117">Click Designer.</span></span>
11. <span data-ttu-id="f195f-118">Í trénu skal velja „Dynamics 365 for Operations\Tafla“.</span><span class="sxs-lookup"><span data-stu-id="f195f-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="f195f-119">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="f195f-119">Click Add root.</span></span>
13. <span data-ttu-id="f195f-120">Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.</span><span class="sxs-lookup"><span data-stu-id="f195f-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="f195f-121">Í reitinn Tafla skal færa inn ‚CompanyInfo‘.</span><span class="sxs-lookup"><span data-stu-id="f195f-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="f195f-122">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="f195f-122">Click OK.</span></span>
16. <span data-ttu-id="f195f-123">Í trénu skal velja 'Functions\Financial dimensions details'.</span><span class="sxs-lookup"><span data-stu-id="f195f-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="f195f-124">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="f195f-124">Click Add root.</span></span>
    * <span data-ttu-id="f195f-125">Þennan gagnagjafa tilgreinir hvernig svið fjárhagsvídda er skilgreint fyrir allar skýrslur sem nota þetta líkan sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="f195f-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="f195f-126">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="f195f-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="f195f-127">Velja skal Já í reitnum Óska eftir víddum.</span><span class="sxs-lookup"><span data-stu-id="f195f-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="f195f-128">Velja skal Já til að leyfa notanda að velja víddir á keyrslutíma á skjámyndinni svargluggai Notanda.</span><span class="sxs-lookup"><span data-stu-id="f195f-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="f195f-129">Ef stillt á Nei verða allar fjárhagsvíddir núverandi tilviks notaðar sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="f195f-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="f195f-130">Í valreit fjárhagsvídda skal velja lögaðila</span><span class="sxs-lookup"><span data-stu-id="f195f-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="f195f-131">Veljið Allt til að leyfa notanda að velja víddir sem óskað er eftir fyrir núverandi tilvik í uppflettisvæðinu.</span><span class="sxs-lookup"><span data-stu-id="f195f-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="f195f-132">Veljið Lögaðila til að leyfa notanda að velja víddir sem óskað er eftir fyrir fyrirtæki í uppflettisvæðinu.</span><span class="sxs-lookup"><span data-stu-id="f195f-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="f195f-133">Velja skal Vídd til að leyfa notanda að velja víddir sem nota stakar víddarsamstæður.</span><span class="sxs-lookup"><span data-stu-id="f195f-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="f195f-134">Veljið Já í svæðinu Biðja um aðallykil.</span><span class="sxs-lookup"><span data-stu-id="f195f-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="f195f-135">Stilltu 'Biðja um aðallykil' á Já til að leyfa notendum að velja aðallykilinn sem hluta af listanum yfir víddir.</span><span class="sxs-lookup"><span data-stu-id="f195f-135">Set ‘Ask for main account’ to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="f195f-136">Ef stillt er á Nei, verður aðallykilinn ekki teknar með á lista yfir víddir og valkosturinn "Er aðallykill skylda" er virkjaður.</span><span class="sxs-lookup"><span data-stu-id="f195f-136">If set to No, the main account will not be included to the list of dimensions and the ‘Is main account mandatory’ option is enabled.</span></span> <span data-ttu-id="f195f-137">Ef "Er aðallykill áskilinn' er stilltur á já skal hafa aðallykillinn með í lista yfir víddir óháð vali notanda.</span><span class="sxs-lookup"><span data-stu-id="f195f-137">If “Is main account mandatory’ is set to Yes, include the main account in the list of dimensions regardless of the user’s selection.</span></span>  
22. <span data-ttu-id="f195f-138">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f195f-138">Click OK.</span></span>
23. <span data-ttu-id="f195f-139">Í trénu skal velja „Dynamics 365 for Operations\Tafla færslur“.</span><span class="sxs-lookup"><span data-stu-id="f195f-139">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="f195f-140">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="f195f-140">Click Add root.</span></span>
25. <span data-ttu-id="f195f-141">Í svæðið Heiti, færðu inn 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="f195f-141">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="f195f-142">Velja skal Já í reitnum Óska eftir fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="f195f-142">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="f195f-143">Í reitnum Tafla skal færa inn ‚LedgerJournalTable‘.</span><span class="sxs-lookup"><span data-stu-id="f195f-143">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="f195f-144">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f195f-144">Click OK.</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="f195f-145">Varpa einingum gagnalíkans við gagnaveitur sem bætt var við.</span><span class="sxs-lookup"><span data-stu-id="f195f-145">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="f195f-146">Stækkið „færslubók“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="f195f-146">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="f195f-147">Í trénu skal víkka út 'Journal\Transaction'.</span><span class="sxs-lookup"><span data-stu-id="f195f-147">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="f195f-148">Í trénu skal víkka út 'Journal\Transaction\Dimensions data'.</span><span class="sxs-lookup"><span data-stu-id="f195f-148">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="f195f-149">Í trénu skal víkka út 'Dimensions setting'.</span><span class="sxs-lookup"><span data-stu-id="f195f-149">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="f195f-150">Í trénu skal víkka út 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="f195f-150">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="f195f-151">Í trénu, útvíkka „LedgerJournal\<Relations“.</span><span class="sxs-lookup"><span data-stu-id="f195f-151">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="f195f-152">Í trénu, útvíkka expand „LedgerJournal\<Relations\LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="f195f-152">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="f195f-153">Í trénu, útvíkka „LedgerJournal\<Relations\LedgerJournalTrans\Voucher“.</span><span class="sxs-lookup"><span data-stu-id="f195f-153">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="f195f-154">Í trénu skal velja 'Journal\Transaction\Voucher'.</span><span class="sxs-lookup"><span data-stu-id="f195f-154">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="f195f-155">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="f195f-155">Click Bind.</span></span>
11. <span data-ttu-id="f195f-156">Í trénu, skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.</span><span class="sxs-lookup"><span data-stu-id="f195f-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="f195f-157">Athugið að fyrir allar tilvísanir í fjárhagsvíddir sem eru stilltar á, til dæmis LedgerDimension, er samsvarandi vara gagnaveitu tiltæk (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="f195f-157">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="f195f-158">Þessi gagnaveituvara býður upp á fjárhagsvíddir þessara vídda sem eru stilltar sem listi færslunnar.</span><span class="sxs-lookup"><span data-stu-id="f195f-158">This data source item offers the financial dimensions of that dimensions set as the record’s list.</span></span>  
12. <span data-ttu-id="f195f-159">Í trénu, skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.</span><span class="sxs-lookup"><span data-stu-id="f195f-159">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="f195f-160">Í trénu skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions“.</span><span class="sxs-lookup"><span data-stu-id="f195f-160">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="f195f-161">Í trénu skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value“.</span><span class="sxs-lookup"><span data-stu-id="f195f-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="f195f-162">Í trénu skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition“.</span><span class="sxs-lookup"><span data-stu-id="f195f-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="f195f-163">Í trénu, skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name“.</span><span class="sxs-lookup"><span data-stu-id="f195f-163">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="f195f-164">Í trénu, skal velja 'Journal\Transaction\Dimensions data\Name'.</span><span class="sxs-lookup"><span data-stu-id="f195f-164">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="f195f-165">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="f195f-165">Click Bind.</span></span>
19. <span data-ttu-id="f195f-166">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description“.</span><span class="sxs-lookup"><span data-stu-id="f195f-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="f195f-167">Í trénu, skal velja 'Journal\Transaction\Dimensions data\Description'.</span><span class="sxs-lookup"><span data-stu-id="f195f-167">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="f195f-168">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="f195f-168">Click Bind.</span></span>
22. <span data-ttu-id="f195f-169">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code“.</span><span class="sxs-lookup"><span data-stu-id="f195f-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="f195f-170">Í trénu, skal velja 'Journal\Transaction\Dimensions data\Code'.</span><span class="sxs-lookup"><span data-stu-id="f195f-170">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="f195f-171">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="f195f-171">Click Bind.</span></span>
25. <span data-ttu-id="f195f-172">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions“.</span><span class="sxs-lookup"><span data-stu-id="f195f-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="f195f-173">Í trénu, skal velja 'Journal\Transaction\Dimensions data'.</span><span class="sxs-lookup"><span data-stu-id="f195f-173">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="f195f-174">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="f195f-174">Click Bind.</span></span>
28. <span data-ttu-id="f195f-175">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)“.</span><span class="sxs-lookup"><span data-stu-id="f195f-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="f195f-176">Í trénu, skal velja 'Journal\Transaction\Debit'.</span><span class="sxs-lookup"><span data-stu-id="f195f-176">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="f195f-177">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="f195f-177">Click Bind.</span></span>
31. <span data-ttu-id="f195f-178">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)“.</span><span class="sxs-lookup"><span data-stu-id="f195f-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="f195f-179">Í trénu, skal velja 'Journal\Transaction\Date'.</span><span class="sxs-lookup"><span data-stu-id="f195f-179">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="f195f-180">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="f195f-180">Click Bind.</span></span>
34. <span data-ttu-id="f195f-181">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)“.</span><span class="sxs-lookup"><span data-stu-id="f195f-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="f195f-182">Í trénu, skal velja 'Journal\Transaction\Currency'.</span><span class="sxs-lookup"><span data-stu-id="f195f-182">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="f195f-183">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="f195f-183">Click Bind.</span></span>
37. <span data-ttu-id="f195f-184">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)“.</span><span class="sxs-lookup"><span data-stu-id="f195f-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="f195f-185">Í trénu, skal velja 'Journal\Transaction\Credit'.</span><span class="sxs-lookup"><span data-stu-id="f195f-185">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="f195f-186">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="f195f-186">Click Bind.</span></span>
40. <span data-ttu-id="f195f-187">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="f195f-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="f195f-188">Í trénu, skal velja 'Journal\Transaction'.</span><span class="sxs-lookup"><span data-stu-id="f195f-188">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="f195f-189">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="f195f-189">Click Bind.</span></span>
43. <span data-ttu-id="f195f-190">Í trénu, skal velja 'LedgerJournal\Journal batch number(JournalNum)'.</span><span class="sxs-lookup"><span data-stu-id="f195f-190">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="f195f-191">Í trénu, skal velja 'Journal\Batch'.</span><span class="sxs-lookup"><span data-stu-id="f195f-191">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="f195f-192">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="f195f-192">Click Bind.</span></span>
46. <span data-ttu-id="f195f-193">Í trénu, skal velja 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="f195f-193">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="f195f-194">Í trénu, skal velja 'Journal'.</span><span class="sxs-lookup"><span data-stu-id="f195f-194">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="f195f-195">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="f195f-195">Click Bind.</span></span>
49. <span data-ttu-id="f195f-196">Í trénu, skal víkka út 'Dimensions'.</span><span class="sxs-lookup"><span data-stu-id="f195f-196">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="f195f-197">Í trénu, skal víkka út 'Dimensions\Main account and dimensions'.</span><span class="sxs-lookup"><span data-stu-id="f195f-197">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="f195f-198">Í trénu, skal víkka út 'Dimensions\Main account and dimensions\Definition'.</span><span class="sxs-lookup"><span data-stu-id="f195f-198">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="f195f-199">Í trénu, skal velja 'Dimensions\Main account and dimensions\Definition\Name'.</span><span class="sxs-lookup"><span data-stu-id="f195f-199">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="f195f-200">Í trénu, skal velja 'Dimensions setting\Code'.</span><span class="sxs-lookup"><span data-stu-id="f195f-200">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="f195f-201">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="f195f-201">Click Bind.</span></span>
55. <span data-ttu-id="f195f-202">Í trénu, skal velja 'Dimensions\Main account and dimensions\Definition\Report column name'.</span><span class="sxs-lookup"><span data-stu-id="f195f-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="f195f-203">Í trénu, skal velja 'Dimensions setting\Name'.</span><span class="sxs-lookup"><span data-stu-id="f195f-203">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="f195f-204">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="f195f-204">Click Bind.</span></span>
58. <span data-ttu-id="f195f-205">Í trénu, skal velja 'Dimensions\Main account and dimensions'.</span><span class="sxs-lookup"><span data-stu-id="f195f-205">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="f195f-206">Í trénu, skal velja 'Dimensions setting'.</span><span class="sxs-lookup"><span data-stu-id="f195f-206">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="f195f-207">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="f195f-207">Click Bind.</span></span>
61. <span data-ttu-id="f195f-208">Í trénu, skal velja 'Company'.</span><span class="sxs-lookup"><span data-stu-id="f195f-208">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="f195f-209">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="f195f-209">Click Edit.</span></span>
63. <span data-ttu-id="f195f-210">Í svæðinu expressionAsStringText skal færa inn 'Company.'find()'.'name()''.</span><span class="sxs-lookup"><span data-stu-id="f195f-210">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="f195f-211">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="f195f-211">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="f195f-212">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f195f-212">Click Save.</span></span>
65. <span data-ttu-id="f195f-213">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f195f-213">Close the page.</span></span>
66. <span data-ttu-id="f195f-214">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="f195f-214">Click Save.</span></span>
67. <span data-ttu-id="f195f-215">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f195f-215">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="f195f-216">Ljúktu við þessa útgáfu af drögum að líkani.</span><span class="sxs-lookup"><span data-stu-id="f195f-216">Complete this draft model’s version</span></span>
1. <span data-ttu-id="f195f-217">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f195f-217">Close the page.</span></span>
2. <span data-ttu-id="f195f-218">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f195f-218">Close the page.</span></span>
3. <span data-ttu-id="f195f-219">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="f195f-219">Click Change status.</span></span>
4. <span data-ttu-id="f195f-220">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="f195f-220">Click Complete.</span></span>
5. <span data-ttu-id="f195f-221">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="f195f-221">Click OK.</span></span>


