---
title: Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 2 - líkanavörpun)
description: Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.
author: NickSelin
manager: AnnBe
ms.date: 05/27/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3214ddb1e077d889fb7b785bee2554b96c3907ed
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681686"
---
# <a name="er-use-financial-dimensions-as-a-data-source-part-2---model-mapping"></a><span data-ttu-id="11104-103">Rafræn skýrslugerð Nota Fjárhagsvíddir sem gagnaveita (Hluti 2 - líkanavörpun)</span><span class="sxs-lookup"><span data-stu-id="11104-103">ER Use financial dimensions as a data source (Part 2 - Model mapping)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11104-104">Eftirfarandi skref útskýra hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stillt líkan rafrænnar skýrslugerðar (ER) svo það noti fjárhagsvíddir sem gagnaveitu fyrir rafrænar skýrslur.</span><span class="sxs-lookup"><span data-stu-id="11104-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) model to use financial dimensions as a data source for ER reports.</span></span> <span data-ttu-id="11104-105">Hægt er að framkvæma þessum skrefum í Hvaða fyrirtæki sem er.</span><span class="sxs-lookup"><span data-stu-id="11104-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="11104-106">Til að ljúka þessum skrefum, verður fyrst að ljúka við skrefin í ferlinu „Rafræn skýrslugerð notar fjárhagsvíddir sem gagnaveitu (Hluti 1: Hönnun gagnalíkans”.</span><span class="sxs-lookup"><span data-stu-id="11104-106">To complete these steps, you must first complete the steps in the "ER Use financial dimensions as a data source (Part 1: Design data model" procedure.</span></span>


## <a name="add-required-data-sources-to-model-mapping"></a><span data-ttu-id="11104-107">Bæta við nauðsynlegar gagnaveitur við líkanavörpun</span><span class="sxs-lookup"><span data-stu-id="11104-107">Add required data sources to model mapping</span></span>
1. <span data-ttu-id="11104-108">Fara í Fyrirtækisstjórnun > Rafræn skýrslugerð > Grunnstillingar.</span><span class="sxs-lookup"><span data-stu-id="11104-108">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="11104-109">Veljið 'dæmi um líkan fyrir fjárhagsvíddir', í trénu.</span><span class="sxs-lookup"><span data-stu-id="11104-109">In the tree, select 'Financial dimensions sample model'.</span></span>
3. <span data-ttu-id="11104-110">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="11104-110">Click Designer.</span></span>
4. <span data-ttu-id="11104-111">Smellt er á Varpa líkani á gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="11104-111">Click Map model to datasource.</span></span>
5. <span data-ttu-id="11104-112">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="11104-112">Click New.</span></span>
6. <span data-ttu-id="11104-113">Í reitnum Skilgreining er valið „færsla“.</span><span class="sxs-lookup"><span data-stu-id="11104-113">In the Definition field, select Entry.</span></span>
7. <span data-ttu-id="11104-114">Í reitnum Heiti skal færa inn 'gagnakortalagning vídda'.</span><span class="sxs-lookup"><span data-stu-id="11104-114">In the Name field, type 'Dimensions data mapping'.</span></span>
8. <span data-ttu-id="11104-115">Í reitnum lýsing skal færa inn 'gagnakortalagning vídda'.</span><span class="sxs-lookup"><span data-stu-id="11104-115">In the Description field, type 'Dimensions data mapping'.</span></span>
9. <span data-ttu-id="11104-116">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="11104-116">Click Save.</span></span>
10. <span data-ttu-id="11104-117">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="11104-117">Click Designer.</span></span>
11. <span data-ttu-id="11104-118">Í trénu skal velja „Dynamics 365 for Operations\Table“.</span><span class="sxs-lookup"><span data-stu-id="11104-118">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
12. <span data-ttu-id="11104-119">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="11104-119">Click Add root.</span></span>
13. <span data-ttu-id="11104-120">Í reitnum Heiti skal færa inn ‚Fyrirtæki‘.</span><span class="sxs-lookup"><span data-stu-id="11104-120">In the Name field, type 'Company'.</span></span>
14. <span data-ttu-id="11104-121">Í reitinn Tafla skal færa inn ‚CompanyInfo‘.</span><span class="sxs-lookup"><span data-stu-id="11104-121">In the Table field, type 'CompanyInfo'.</span></span>
15. <span data-ttu-id="11104-122">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="11104-122">Click OK.</span></span>
16. <span data-ttu-id="11104-123">Í trénu skal velja 'Functions\Financial dimensions details'.</span><span class="sxs-lookup"><span data-stu-id="11104-123">In the tree, select 'Functions\Financial dimensions details'.</span></span>
17. <span data-ttu-id="11104-124">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="11104-124">Click Add root.</span></span>
    * <span data-ttu-id="11104-125">Þennan gagnagjafa tilgreinir hvernig svið fjárhagsvídda er skilgreint fyrir allar skýrslur sem nota þetta líkan sem gagnagjafa.</span><span class="sxs-lookup"><span data-stu-id="11104-125">This data source specifies how the scope of financial dimensions will be defined for any report that will use this model as a data source.</span></span>  
18. <span data-ttu-id="11104-126">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="11104-126">In the Name field, type a value.</span></span>
19. <span data-ttu-id="11104-127">Velja skal Já í reitnum Óska eftir víddum.</span><span class="sxs-lookup"><span data-stu-id="11104-127">Select Yes in the Ask for dimensions field.</span></span>
    * <span data-ttu-id="11104-128">Velja skal Já til að leyfa notanda að velja víddir á keyrslutíma á skjámyndinni svargluggai Notanda.</span><span class="sxs-lookup"><span data-stu-id="11104-128">Select Yes to allow the user to select dimensions at run-time on the User dialog form.</span></span> <span data-ttu-id="11104-129">Ef stillt á Nei verða allar fjárhagsvíddir núverandi tilviks notaðar sjálfgefið.</span><span class="sxs-lookup"><span data-stu-id="11104-129">If set to No, all financial dimensions of the current instance will be used by default.</span></span>  
20. <span data-ttu-id="11104-130">Í valreit fjárhagsvídda skal velja lögaðila</span><span class="sxs-lookup"><span data-stu-id="11104-130">In the Financial dimensions selection field, select 'Legal entity'.</span></span>
    * <span data-ttu-id="11104-131">Veljið Allt til að leyfa notanda að velja víddir sem óskað er eftir fyrir núverandi tilvik í uppflettisvæðinu.</span><span class="sxs-lookup"><span data-stu-id="11104-131">Select All to allow the user to select desire dimensions for the current  instance in the Lookup field.</span></span>  <span data-ttu-id="11104-132">Veljið Lögaðila til að leyfa notanda að velja víddir sem óskað er eftir fyrir fyrirtæki í uppflettisvæðinu.</span><span class="sxs-lookup"><span data-stu-id="11104-132">Select Legal entity to allow the user to select dimensions for the company in the Lookup field.</span></span>  <span data-ttu-id="11104-133">Velja skal Vídd til að leyfa notanda að velja víddir sem nota stakar víddarsamstæður.</span><span class="sxs-lookup"><span data-stu-id="11104-133">Select Dimension to allow the user to select dimensions using a single dimension set.</span></span>  
21. <span data-ttu-id="11104-134">Veljið Já í svæðinu Biðja um aðallykil.</span><span class="sxs-lookup"><span data-stu-id="11104-134">Select Yes in the Ask for main account field.</span></span>
    * <span data-ttu-id="11104-135">Stilltu „Biðja um aðallykil” á Já til að leyfa notendum að velja aðallykilinn sem hluta af listanum yfir víddir.</span><span class="sxs-lookup"><span data-stu-id="11104-135">Set 'Ask for main account' to Yes to allow users to select the main account as part of the list of dimensions.</span></span>   <span data-ttu-id="11104-136">Ef stillt er á Nei, verður aðallykilinn ekki teknar með á lista yfir víddir og valkosturinn „Er skylda fyrir aðallykil” er virkjaður.</span><span class="sxs-lookup"><span data-stu-id="11104-136">If set to No, the main account will not be included to the list of dimensions and the 'Is main account mandatory' option is enabled.</span></span> <span data-ttu-id="11104-137">Ef „Er skylda fyrir aðallykil” er stillt á já skal hafa aðallykillinn með í lista yfir víddir óháð vali notanda.</span><span class="sxs-lookup"><span data-stu-id="11104-137">If "Is main account mandatory' is set to Yes, include the main account in the list of dimensions regardless of the user's selection.</span></span>  
22. <span data-ttu-id="11104-138">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="11104-138">Click OK.</span></span>
<span data-ttu-id="11104-139">![Hönnuðarsíðan ER-líkanavörpun](../media/er-financial-dimensions-guides-model-mapping1.png)</span><span class="sxs-lookup"><span data-stu-id="11104-139">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping1.png)</span></span>
23. <span data-ttu-id="11104-140">Í trénu skal velja 'Dynamics 365 for Operations\Table records'.</span><span class="sxs-lookup"><span data-stu-id="11104-140">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
24. <span data-ttu-id="11104-141">Smella á bæta Við rót.</span><span class="sxs-lookup"><span data-stu-id="11104-141">Click Add root.</span></span>
25. <span data-ttu-id="11104-142">Í svæðið Heiti, færðu inn 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="11104-142">In the Name field, type 'LedgerJournal'.</span></span>
26. <span data-ttu-id="11104-143">Velja skal Já í reitnum Óska eftir fyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="11104-143">Select Yes in the Ask for query field.</span></span>
27. <span data-ttu-id="11104-144">Í reitnum Tafla skal færa inn ‚LedgerJournalTable‘.</span><span class="sxs-lookup"><span data-stu-id="11104-144">In the Table field, type 'LedgerJournalTable'.</span></span>
28. <span data-ttu-id="11104-145">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="11104-145">Click OK.</span></span>
<span data-ttu-id="11104-146">![Hönnuðarsíðan ER-líkanavörpun](../media/er-financial-dimensions-guides-model-mapping2.png)</span><span class="sxs-lookup"><span data-stu-id="11104-146">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping2.png)</span></span>

## <a name="map-data-model-elements-to-added-data-sources"></a><span data-ttu-id="11104-147">Varpa einingum gagnalíkans við gagnaveitur sem bætt var við.</span><span class="sxs-lookup"><span data-stu-id="11104-147">Map data model elements to added data sources</span></span>
1. <span data-ttu-id="11104-148">Stækkið „færslubók“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="11104-148">In the tree, expand 'Journal'.</span></span>
2. <span data-ttu-id="11104-149">Í trénu skal víkka út 'Journal\Transaction'.</span><span class="sxs-lookup"><span data-stu-id="11104-149">In the tree, expand 'Journal\Transaction'.</span></span>
3. <span data-ttu-id="11104-150">Í trénu skal víkka út 'Journal\Transaction\Dimensions data'.</span><span class="sxs-lookup"><span data-stu-id="11104-150">In the tree, expand 'Journal\Transaction\Dimensions data'.</span></span>
4. <span data-ttu-id="11104-151">Í trénu skal víkka út 'Dimensions setting'.</span><span class="sxs-lookup"><span data-stu-id="11104-151">In the tree, expand 'Dimensions setting'.</span></span>
5. <span data-ttu-id="11104-152">Í trénu skal víkka út 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="11104-152">In the tree, expand 'LedgerJournal'.</span></span>
6. <span data-ttu-id="11104-153">Í trénu, útvíkka „LedgerJournal\<Relations“.</span><span class="sxs-lookup"><span data-stu-id="11104-153">In the tree, expand 'LedgerJournal\<Relations'.</span></span>
7. <span data-ttu-id="11104-154">Í trénu, útvíkka expand „LedgerJournal\<Relations\LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="11104-154">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
8. <span data-ttu-id="11104-155">Í trénu, útvíkka „LedgerJournal\<Relations\LedgerJournalTrans\Voucher“.</span><span class="sxs-lookup"><span data-stu-id="11104-155">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Voucher'.</span></span>
9. <span data-ttu-id="11104-156">Í trénu skal velja 'Journal\Transaction\Voucher'.</span><span class="sxs-lookup"><span data-stu-id="11104-156">In the tree, select 'Journal\Transaction\Voucher'.</span></span>
10. <span data-ttu-id="11104-157">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="11104-157">Click Bind.</span></span>
11. <span data-ttu-id="11104-158">Í trénu, skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.</span><span class="sxs-lookup"><span data-stu-id="11104-158">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
    * <span data-ttu-id="11104-159">Athugið að fyrir allar tilvísanir í fjárhagsvíddir sem eru stilltar á, til dæmis LedgerDimension, er samsvarandi vara gagnaveitu tiltæk (LedgerDimension.Dimension).</span><span class="sxs-lookup"><span data-stu-id="11104-159">Note that for any reference to financial dimensions that is set to, for instance, LedgerDimension, a corresponding data source item is available (LedgerDimension.Dimension).</span></span> <span data-ttu-id="11104-160">Þessi gagnagjafaliður býður upp á fjárhagsvíddir þessara vídda sem eru stilltar sem listi færslunnar.</span><span class="sxs-lookup"><span data-stu-id="11104-160">This data source item offers the financial dimensions of that dimensions set as the record's list.</span></span>  
12. <span data-ttu-id="11104-161">Í trénu, skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)“.</span><span class="sxs-lookup"><span data-stu-id="11104-161">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)'.</span></span>
13. <span data-ttu-id="11104-162">Í trénu skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions“.</span><span class="sxs-lookup"><span data-stu-id="11104-162">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
14. <span data-ttu-id="11104-163">Í trénu skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value“.</span><span class="sxs-lookup"><span data-stu-id="11104-163">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value'.</span></span>
15. <span data-ttu-id="11104-164">Í trénu skal víkka út „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition“.</span><span class="sxs-lookup"><span data-stu-id="11104-164">In the tree, expand 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition'.</span></span>
16. <span data-ttu-id="11104-165">Í trénu, skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name“.</span><span class="sxs-lookup"><span data-stu-id="11104-165">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Definition\Name'.</span></span>
17. <span data-ttu-id="11104-166">Í trénu, skal velja 'Journal\Transaction\Dimensions data\Name'.</span><span class="sxs-lookup"><span data-stu-id="11104-166">In the tree, select 'Journal\Transaction\Dimensions data\Name'.</span></span>
18. <span data-ttu-id="11104-167">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="11104-167">Click Bind.</span></span>
19. <span data-ttu-id="11104-168">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description“.</span><span class="sxs-lookup"><span data-stu-id="11104-168">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Description'.</span></span>
20. <span data-ttu-id="11104-169">Í trénu, skal velja 'Journal\Transaction\Dimensions data\Description'.</span><span class="sxs-lookup"><span data-stu-id="11104-169">In the tree, select 'Journal\Transaction\Dimensions data\Description'.</span></span>
21. <span data-ttu-id="11104-170">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="11104-170">Click Bind.</span></span>
22. <span data-ttu-id="11104-171">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code“.</span><span class="sxs-lookup"><span data-stu-id="11104-171">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions\Value\Code'.</span></span>
23. <span data-ttu-id="11104-172">Í trénu, skal velja 'Journal\Transaction\Dimensions data\Code'.</span><span class="sxs-lookup"><span data-stu-id="11104-172">In the tree, select 'Journal\Transaction\Dimensions data\Code'.</span></span>
24. <span data-ttu-id="11104-173">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="11104-173">Click Bind.</span></span>
25. <span data-ttu-id="11104-174">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions“.</span><span class="sxs-lookup"><span data-stu-id="11104-174">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Account.Dimension(LedgerDimension.Dimension)\Main account and dimensions'.</span></span>
26. <span data-ttu-id="11104-175">Í trénu, skal velja 'Journal\Transaction\Dimensions data'.</span><span class="sxs-lookup"><span data-stu-id="11104-175">In the tree, select 'Journal\Transaction\Dimensions data'.</span></span>
27. <span data-ttu-id="11104-176">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="11104-176">Click Bind.</span></span>
<span data-ttu-id="11104-177">![Hönnuðarsíðan ER-líkanavörpun](../media/er-financial-dimensions-guides-model-mapping3.png)</span><span class="sxs-lookup"><span data-stu-id="11104-177">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping3.png)</span></span>
28. <span data-ttu-id="11104-178">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)“.</span><span class="sxs-lookup"><span data-stu-id="11104-178">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Debit(AmountCurDebit)'.</span></span>
29. <span data-ttu-id="11104-179">Í trénu, skal velja 'Journal\Transaction\Debit'.</span><span class="sxs-lookup"><span data-stu-id="11104-179">In the tree, select 'Journal\Transaction\Debit'.</span></span>
30. <span data-ttu-id="11104-180">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="11104-180">Click Bind.</span></span>
31. <span data-ttu-id="11104-181">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)“.</span><span class="sxs-lookup"><span data-stu-id="11104-181">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Date(TransDate)'.</span></span>
32. <span data-ttu-id="11104-182">Í trénu, skal velja 'Journal\Transaction\Date'.</span><span class="sxs-lookup"><span data-stu-id="11104-182">In the tree, select 'Journal\Transaction\Date'.</span></span>
33. <span data-ttu-id="11104-183">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="11104-183">Click Bind.</span></span>
34. <span data-ttu-id="11104-184">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)“.</span><span class="sxs-lookup"><span data-stu-id="11104-184">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Currency(CurrencyCode)'.</span></span>
35. <span data-ttu-id="11104-185">Í trénu, skal velja 'Journal\Transaction\Currency'.</span><span class="sxs-lookup"><span data-stu-id="11104-185">In the tree, select 'Journal\Transaction\Currency'.</span></span>
36. <span data-ttu-id="11104-186">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="11104-186">Click Bind.</span></span>
37. <span data-ttu-id="11104-187">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)“.</span><span class="sxs-lookup"><span data-stu-id="11104-187">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans\Credit(AmountCurCredit)'.</span></span>
38. <span data-ttu-id="11104-188">Í trénu, skal velja 'Journal\Transaction\Credit'.</span><span class="sxs-lookup"><span data-stu-id="11104-188">In the tree, select 'Journal\Transaction\Credit'.</span></span>
39. <span data-ttu-id="11104-189">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="11104-189">Click Bind.</span></span>
40. <span data-ttu-id="11104-190">Í trénu skal velja „LedgerJournal\<Relations\LedgerJournalTrans“.</span><span class="sxs-lookup"><span data-stu-id="11104-190">In the tree, select 'LedgerJournal\<Relations\LedgerJournalTrans'.</span></span>
41. <span data-ttu-id="11104-191">Í trénu, skal velja 'Journal\Transaction'.</span><span class="sxs-lookup"><span data-stu-id="11104-191">In the tree, select 'Journal\Transaction'.</span></span>
42. <span data-ttu-id="11104-192">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="11104-192">Click Bind.</span></span>
43. <span data-ttu-id="11104-193">Í trénu, skal velja 'LedgerJournal\Journal batch number(JournalNum)'.</span><span class="sxs-lookup"><span data-stu-id="11104-193">In the tree, select 'LedgerJournal\Journal batch number(JournalNum)'.</span></span>
44. <span data-ttu-id="11104-194">Í trénu, skal velja 'Journal\Batch'.</span><span class="sxs-lookup"><span data-stu-id="11104-194">In the tree, select 'Journal\Batch'.</span></span>
45. <span data-ttu-id="11104-195">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="11104-195">Click Bind.</span></span>
46. <span data-ttu-id="11104-196">Í trénu, skal velja 'LedgerJournal'.</span><span class="sxs-lookup"><span data-stu-id="11104-196">In the tree, select 'LedgerJournal'.</span></span>
47. <span data-ttu-id="11104-197">Í trénu, skal velja 'Journal'.</span><span class="sxs-lookup"><span data-stu-id="11104-197">In the tree, select 'Journal'.</span></span>
48. <span data-ttu-id="11104-198">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="11104-198">Click Bind.</span></span>
49. <span data-ttu-id="11104-199">Í trénu, skal víkka út 'Dimensions'.</span><span class="sxs-lookup"><span data-stu-id="11104-199">In the tree, expand 'Dimensions'.</span></span>
50. <span data-ttu-id="11104-200">Í trénu, skal víkka út 'Dimensions\Main account and dimensions'.</span><span class="sxs-lookup"><span data-stu-id="11104-200">In the tree, expand 'Dimensions\Main account and dimensions'.</span></span>
51. <span data-ttu-id="11104-201">Í trénu, skal víkka út 'Dimensions\Main account and dimensions\Definition'.</span><span class="sxs-lookup"><span data-stu-id="11104-201">In the tree, expand 'Dimensions\Main account and dimensions\Definition'.</span></span>
52. <span data-ttu-id="11104-202">Í trénu, skal velja 'Dimensions\Main account and dimensions\Definition\Name'.</span><span class="sxs-lookup"><span data-stu-id="11104-202">In the tree, select 'Dimensions\Main account and dimensions\Definition\Name'.</span></span>
53. <span data-ttu-id="11104-203">Í trénu, skal velja 'Dimensions setting\Code'.</span><span class="sxs-lookup"><span data-stu-id="11104-203">In the tree, select 'Dimensions setting\Code'.</span></span>
54. <span data-ttu-id="11104-204">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="11104-204">Click Bind.</span></span>
55. <span data-ttu-id="11104-205">Í trénu, skal velja 'Dimensions\Main account and dimensions\Definition\Report column name'.</span><span class="sxs-lookup"><span data-stu-id="11104-205">In the tree, select 'Dimensions\Main account and dimensions\Definition\Report column name'.</span></span>
56. <span data-ttu-id="11104-206">Í trénu, skal velja 'Dimensions setting\Name'.</span><span class="sxs-lookup"><span data-stu-id="11104-206">In the tree, select 'Dimensions setting\Name'.</span></span>
57. <span data-ttu-id="11104-207">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="11104-207">Click Bind.</span></span>
58. <span data-ttu-id="11104-208">Í trénu, skal velja 'Dimensions\Main account and dimensions'.</span><span class="sxs-lookup"><span data-stu-id="11104-208">In the tree, select 'Dimensions\Main account and dimensions'.</span></span>
59. <span data-ttu-id="11104-209">Í trénu, skal velja 'Dimensions setting'.</span><span class="sxs-lookup"><span data-stu-id="11104-209">In the tree, select 'Dimensions setting'.</span></span>
60. <span data-ttu-id="11104-210">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="11104-210">Click Bind.</span></span>
61. <span data-ttu-id="11104-211">Í trénu, skal velja 'Company'.</span><span class="sxs-lookup"><span data-stu-id="11104-211">In the tree, select 'Company'.</span></span>
62. <span data-ttu-id="11104-212">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="11104-212">Click Edit.</span></span>
63. <span data-ttu-id="11104-213">Í svæðinu expressionAsStringText skal færa inn 'Company.'find()'.'name()''.</span><span class="sxs-lookup"><span data-stu-id="11104-213">In the expressionAsStringText field, enter 'Company.'find()'.'name()''.</span></span>
    * <span data-ttu-id="11104-214">Company.'find()'.'name()'</span><span class="sxs-lookup"><span data-stu-id="11104-214">Company.'find()'.'name()'</span></span>  
64. <span data-ttu-id="11104-215">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="11104-215">Click Save.</span></span>
<span data-ttu-id="11104-216">![Hönnuðarsíðan ER-líkanavörpun](../media/er-financial-dimensions-guides-model-mapping4.png)</span><span class="sxs-lookup"><span data-stu-id="11104-216">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping4.png)</span></span>
65. <span data-ttu-id="11104-217">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="11104-217">Close the page.</span></span>
66. <span data-ttu-id="11104-218">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="11104-218">Click Save.</span></span>
67. <span data-ttu-id="11104-219">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="11104-219">Close the page.</span></span>

## <a name="complete-this-draft-models-version"></a><span data-ttu-id="11104-220">Ljúktu við þessa útgáfu af drögum að líkani.</span><span class="sxs-lookup"><span data-stu-id="11104-220">Complete this draft model's version</span></span>
1. <span data-ttu-id="11104-221">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="11104-221">Close the page.</span></span>
2. <span data-ttu-id="11104-222">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="11104-222">Close the page.</span></span>
3. <span data-ttu-id="11104-223">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="11104-223">Click Change status.</span></span>
4. <span data-ttu-id="11104-224">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="11104-224">Click Complete.</span></span>
5. <span data-ttu-id="11104-225">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="11104-225">Click OK.</span></span>
<span data-ttu-id="11104-226">![Hönnuðarsíðan ER-líkanavörpun](../media/er-financial-dimensions-guides-model-mapping5.png)</span><span class="sxs-lookup"><span data-stu-id="11104-226">![ER model mapping designer page](../media/er-financial-dimensions-guides-model-mapping5.png)</span></span>
