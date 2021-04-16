---
title: Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 2 - líkanavörpun)
description: Þetta efni útskýrir hvernig á að skilgreina líkan rafrænnar skýrslugerðar til að nota fjárhagsvíddir sem gagnagjafa fyrir skýrslur rafrænnar skýrslugerðar. (Hluti 2)
author: NickSelin
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e6f5ffbebdfcd9f945e6237904d80e8734b0220
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752437"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="19310-104">Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 2 - líkanavörpun)</span><span class="sxs-lookup"><span data-stu-id="19310-104">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="19310-105">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="19310-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="19310-106">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="19310-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="19310-107">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð notar fjárhagsvíddir sem gagnaveitu (Hluti 1: Hönnun gagnalíkans”.</span><span class="sxs-lookup"><span data-stu-id="19310-107">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="19310-108">Bæta við nauðsynlegar gagnaveitur við líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="19310-108">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="19310-109">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="19310-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="19310-110">Veljið 'dæmi um líkan fyrir fjárhagsvíddir', í trénu.</span><span class="sxs-lookup"><span data-stu-id="19310-110">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="19310-111">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="19310-111">Click Designer.</span></span>
4. <span data-ttu-id="19310-112">Smellt er á Varpa líkani á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="19310-112">Click Map model to datasource.</span></span>
5. <span data-ttu-id="19310-113">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="19310-113">Click New.</span></span>
6. <span data-ttu-id="19310-114">Í reitnum Skilgreining er valið „færsla“.</span><span class="sxs-lookup"><span data-stu-id="19310-114">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="19310-115">Í reitnum Heiti skal færa inn 'gagnakortalagning vídda'.</span><span class="sxs-lookup"><span data-stu-id="19310-115">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="19310-116">Í reitnum lýsing skal færa inn 'gagnakortalagning vídda'.</span><span class="sxs-lookup"><span data-stu-id="19310-116">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="19310-117">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="19310-117">Click Save.</span></span>
10. <span data-ttu-id="19310-118">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="19310-118">Click Designer.</span></span>
11. <span data-ttu-id="19310-119">Í trénu skal velja „Dynamics 365 for Operations\Table“.</span><span class="sxs-lookup"><span data-stu-id="19310-119">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="19310-120">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="19310-120">Click Add root.</span></span>
13. <span data-ttu-id="19310-121">Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.</span><span class="sxs-lookup"><span data-stu-id="19310-121">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="19310-122">Í reitinn Tafla skal færa inn ‚CompanyInfo‘.</span><span class="sxs-lookup"><span data-stu-id="19310-122">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="19310-123">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="19310-123">Click OK.</span></span>
16. <span data-ttu-id="19310-124">Í trénu skal velja 'Functions\Financial dimensions details'.</span><span class="sxs-lookup"><span data-stu-id="19310-124">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="19310-125">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="19310-125">Click Add root.</span></span>
    * <span data-ttu-id="19310-126">Þennan gagnagjafa tilgreinir hvernig svið fjárhagsvídda er skilgreint fyrir allar skýrslur sem nota þetta líkan sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="19310-126">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="19310-127">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="19310-127">In the Name field, type a value.</span></span>
19. <span data-ttu-id="19310-128">Velja skal Já í reitnum Óska eftir víddum.</span><span class="sxs-lookup"><span data-stu-id="19310-128">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="19310-129">Velja skal Já til að leyfa notanda að velja víddir á keyrslutíma á skjámyndinni svargluggai Notanda.</span><span class="sxs-lookup"><span data-stu-id="19310-129">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="19310-130">Ef stillt á Nei verða allar fjárhagsvíddir núverandi tilviks notaðar sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="19310-130">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="19310-131">Í valreit fjárhagsvídda skal velja lögaðila</span><span class="sxs-lookup"><span data-stu-id="19310-131">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="19310-132">Veljið Allt til að leyfa notanda að velja víddir sem óskað er eftir fyrir núverandi tilvik í uppflettisvæðinu.</span><span class="sxs-lookup"><span data-stu-id="19310-132">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="19310-133">Veljið Lögaðila til að leyfa notanda að velja víddir sem óskað er eftir fyrir fyrirtæki í uppflettisvæðinu.</span><span class="sxs-lookup"><span data-stu-id="19310-133">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="19310-134">Velja skal Vídd til að leyfa notanda að velja víddir sem nota stakar víddarsamstæður.</span><span class="sxs-lookup"><span data-stu-id="19310-134">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="19310-135">Veljið Já í svæðinu Biðja um aðallykil.</span><span class="sxs-lookup"><span data-stu-id="19310-135">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="19310-136">Stilltu „Biðja um aðallykil” á Já til að leyfa notendum að velja aðallykilinn sem hluta af listanum yfir víddir.</span><span class="sxs-lookup"><span data-stu-id="19310-136">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="19310-137">Ef stillt er á Nei, verður aðallykilinn ekki teknar með á lista yfir víddir og valkosturinn „Er skylda fyrir aðallykil” er virkjaður.</span><span class="sxs-lookup"><span data-stu-id="19310-137">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="19310-138">Ef „Er skylda fyrir aðallykil” er stillt á já skal hafa aðallykillinn með í lista yfir víddir óháð vali notanda.</span><span class="sxs-lookup"><span data-stu-id="19310-138">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="19310-139">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="19310-139">Click OK.</span></span>
<span data-ttu-id="19310-140">![Hönnuðarsíðan ER-líkanavörpun](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="19310-140">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="19310-141">Í trénu skal velja 'Dynamics 365 for Operations\Table records'.</span><span class="sxs-lookup"><span data-stu-id="19310-141">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="19310-142">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="19310-142">Click Add root.</span></span>
25. <span data-ttu-id="19310-143">Í svæðið Heiti, færðu inn 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="19310-143">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="19310-144">Velja skal Já í reitnum Óska eftir fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="19310-144">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="19310-145">Í reitnum Tafla skal færa inn ‚LedgerJournalTable‘.</span><span class="sxs-lookup"><span data-stu-id="19310-145">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="19310-146">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="19310-146">Click OK.</span></span>
<span data-ttu-id="19310-147">![Hönnuðarsíðan ER-líkanavörpun](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="19310-147">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="19310-148">Varpa einingum gagnalíkans við gagnaveitur sem bætt var við.</span><span class="sxs-lookup"><span data-stu-id="19310-148">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="19310-149">Stækkið „færslubók“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="19310-149">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="19310-150">Í trénu skal víkka út 'Journal\Transaction'.</span><span class="sxs-lookup"><span data-stu-id="19310-150">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="19310-151">Í trénu skal víkka út 'Journal\Transaction\Dimensions data'.</span><span class="sxs-lookup"><span data-stu-id="19310-151">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="19310-152">Í trénu skal víkka út 'Dimensions setting'.</span><span class="sxs-lookup"><span data-stu-id="19310-152">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="19310-153">Í trénu skal víkka út 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="19310-153">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="19310-154">Í trénu, útvíkka „LedgerJournal\<Relations“.</span><span class="sxs-lookup"><span data-stu-id="19310-154">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="19310-155">Í trénu, útvíkka expand „LedgerJournal\<Relations\LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="19310-155">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="19310-156">Í trénu, útvíkka „LedgerJournal\<Relations\LedgerJournalTrans\Voucher“.</span><span class="sxs-lookup"><span data-stu-id="19310-156">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="19310-157">Í trénu skal velja 'Journal\Transaction\Voucher'.</span><span class="sxs-lookup"><span data-stu-id="19310-157">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="19310-158">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="19310-158">Click Bind.</span></span>
11. <span data-ttu-id="19310-159">Í trénu, skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.</span><span class="sxs-lookup"><span data-stu-id="19310-159">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="19310-160">Athugið að fyrir allar tilvísanir í fjárhagsvíddir sem eru stilltar á, til dæmis LedgerDimension, er samsvarandi vara gagnaveitu tiltæk (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="19310-160">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="19310-161">Þessi gagnagjafaliður býður upp á fjárhagsvíddir þessara vídda sem eru stilltar sem listi færslunnar.</span><span class="sxs-lookup"><span data-stu-id="19310-161">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="19310-162">Í trénu, skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.</span><span class="sxs-lookup"><span data-stu-id="19310-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="19310-163">Í trénu skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions“.</span><span class="sxs-lookup"><span data-stu-id="19310-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="19310-164">Í trénu skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value“.</span><span class="sxs-lookup"><span data-stu-id="19310-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="19310-165">Í trénu skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition“.</span><span class="sxs-lookup"><span data-stu-id="19310-165">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="19310-166">Í trénu, skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name“.</span><span class="sxs-lookup"><span data-stu-id="19310-166">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="19310-167">Í trénu, skal velja 'Journal\Transaction\Dimensions data\Name'.</span><span class="sxs-lookup"><span data-stu-id="19310-167">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="19310-168">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="19310-168">Click Bind.</span></span>
19. <span data-ttu-id="19310-169">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description“.</span><span class="sxs-lookup"><span data-stu-id="19310-169">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="19310-170">Í trénu, skal velja 'Journal\Transaction\Dimensions data\Description'.</span><span class="sxs-lookup"><span data-stu-id="19310-170">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="19310-171">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="19310-171">Click Bind.</span></span>
22. <span data-ttu-id="19310-172">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code“.</span><span class="sxs-lookup"><span data-stu-id="19310-172">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="19310-173">Í trénu, skal velja 'Journal\Transaction\Dimensions data\Code'.</span><span class="sxs-lookup"><span data-stu-id="19310-173">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="19310-174">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="19310-174">Click Bind.</span></span>
25. <span data-ttu-id="19310-175">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions“.</span><span class="sxs-lookup"><span data-stu-id="19310-175">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="19310-176">Í trénu, skal velja 'Journal\Transaction\Dimensions data'.</span><span class="sxs-lookup"><span data-stu-id="19310-176">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="19310-177">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="19310-177">Click Bind.</span></span>
<span data-ttu-id="19310-178">![Hönnuðarsíðan ER-líkanavörpun](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="19310-178">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="19310-179">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)“.</span><span class="sxs-lookup"><span data-stu-id="19310-179">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="19310-180">Í trénu, skal velja 'Journal\Transaction\Debit'.</span><span class="sxs-lookup"><span data-stu-id="19310-180">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="19310-181">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="19310-181">Click Bind.</span></span>
31. <span data-ttu-id="19310-182">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)“.</span><span class="sxs-lookup"><span data-stu-id="19310-182">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="19310-183">Í trénu, skal velja 'Journal\Transaction\Date'.</span><span class="sxs-lookup"><span data-stu-id="19310-183">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="19310-184">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="19310-184">Click Bind.</span></span>
34. <span data-ttu-id="19310-185">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)“.</span><span class="sxs-lookup"><span data-stu-id="19310-185">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="19310-186">Í trénu, skal velja 'Journal\Transaction\Currency'.</span><span class="sxs-lookup"><span data-stu-id="19310-186">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="19310-187">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="19310-187">Click Bind.</span></span>
37. <span data-ttu-id="19310-188">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)“.</span><span class="sxs-lookup"><span data-stu-id="19310-188">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="19310-189">Í trénu, skal velja 'Journal\Transaction\Credit'.</span><span class="sxs-lookup"><span data-stu-id="19310-189">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="19310-190">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="19310-190">Click Bind.</span></span>
40. <span data-ttu-id="19310-191">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="19310-191">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="19310-192">Í trénu, skal velja 'Journal\Transaction'.</span><span class="sxs-lookup"><span data-stu-id="19310-192">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="19310-193">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="19310-193">Click Bind.</span></span>
43. <span data-ttu-id="19310-194">Í trénu, skal velja 'LedgerJournal\Journal batch number(JournalNum)'.</span><span class="sxs-lookup"><span data-stu-id="19310-194">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="19310-195">Í trénu, skal velja 'Journal\Batch'.</span><span class="sxs-lookup"><span data-stu-id="19310-195">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="19310-196">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="19310-196">Click Bind.</span></span>
46. <span data-ttu-id="19310-197">Í trénu, skal velja 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="19310-197">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="19310-198">Í trénu, skal velja 'Journal'.</span><span class="sxs-lookup"><span data-stu-id="19310-198">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="19310-199">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="19310-199">Click Bind.</span></span>
49. <span data-ttu-id="19310-200">Í trénu, skal víkka út 'Dimensions'.</span><span class="sxs-lookup"><span data-stu-id="19310-200">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="19310-201">Í trénu, skal víkka út 'Dimensions\Main account and dimensions'.</span><span class="sxs-lookup"><span data-stu-id="19310-201">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="19310-202">Í trénu, skal víkka út 'Dimensions\Main account and dimensions\Definition'.</span><span class="sxs-lookup"><span data-stu-id="19310-202">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="19310-203">Í trénu, skal velja 'Dimensions\Main account and dimensions\Definition\Name'.</span><span class="sxs-lookup"><span data-stu-id="19310-203">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="19310-204">Í trénu, skal velja 'Dimensions setting\Code'.</span><span class="sxs-lookup"><span data-stu-id="19310-204">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="19310-205">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="19310-205">Click Bind.</span></span>
55. <span data-ttu-id="19310-206">Í trénu, skal velja 'Dimensions\Main account and dimensions\Definition\Report column name'.</span><span class="sxs-lookup"><span data-stu-id="19310-206">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="19310-207">Í trénu, skal velja 'Dimensions setting\Name'.</span><span class="sxs-lookup"><span data-stu-id="19310-207">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="19310-208">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="19310-208">Click Bind.</span></span>
58. <span data-ttu-id="19310-209">Í trénu, skal velja 'Dimensions\Main account and dimensions'.</span><span class="sxs-lookup"><span data-stu-id="19310-209">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="19310-210">Í trénu, skal velja 'Dimensions setting'.</span><span class="sxs-lookup"><span data-stu-id="19310-210">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="19310-211">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="19310-211">Click Bind.</span></span>
61. <span data-ttu-id="19310-212">Í trénu, skal velja 'Company'.</span><span class="sxs-lookup"><span data-stu-id="19310-212">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="19310-213">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="19310-213">Click Edit.</span></span>
63. <span data-ttu-id="19310-214">Í svæðinu expressionAsStringText skal færa inn 'Company.'find()'.'name()''.</span><span class="sxs-lookup"><span data-stu-id="19310-214">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="19310-215">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="19310-215">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="19310-216">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="19310-216">Click Save.</span></span>
<span data-ttu-id="19310-217">![Hönnuðarsíðan ER-líkanavörpun](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="19310-217">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="19310-218">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="19310-218">Close the page.</span></span>
66. <span data-ttu-id="19310-219">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="19310-219">Click Save.</span></span>
67. <span data-ttu-id="19310-220">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="19310-220">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="19310-221">Ljúktu við þessa útgáfu af drögum að líkani.</span><span class="sxs-lookup"><span data-stu-id="19310-221">Complete this draft model's version</span></span>
1. <span data-ttu-id="19310-222">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="19310-222">Close the page.</span></span>
2. <span data-ttu-id="19310-223">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="19310-223">Close the page.</span></span>
3. <span data-ttu-id="19310-224">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="19310-224">Click Change status.</span></span>
4. <span data-ttu-id="19310-225">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="19310-225">Click Complete.</span></span>
5. <span data-ttu-id="19310-226">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="19310-226">Click OK.</span></span>
<span data-ttu-id="19310-227">![Hönnuðarsíðan ER-líkanavörpun](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="19310-227">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]