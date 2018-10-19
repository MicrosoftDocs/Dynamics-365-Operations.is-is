--- 
title: "Rafræn skýrslugerð Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði (nóvember 2016)"
description: "Eftirfarandi skref útskýra hvernig notandi úthlutað á hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað nýja skilgreiningarveitu fyrir rafræna skýrslugerð (ER) sem inniheldur snið til að mynda rafræn skjöl í OPENXML-sniði."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 3e6b6b16f202af051ccff02051eb438ea49ff6da
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="e3fb3-103">Rafræn skýrslugerð Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði (nóvember 2016)</span><span class="sxs-lookup"><span data-stu-id="e3fb3-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e3fb3-104">Eftirfarandi skref útskýra hvernig notandi úthlutað á hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað nýja skilgreiningarveitu fyrir rafræna skýrslugerð (ER) sem inniheldur snið til að mynda rafræn skjöl í OPENXML-sniði.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="e3fb3-105">Þessi skilgreining verður notuð til að vinna greiðslur lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="e3fb3-106">Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í GBSI fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="e3fb3-107">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka".</span><span class="sxs-lookup"><span data-stu-id="e3fb3-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="e3fb3-108">Einnig verður að hafa Excel-skráin sem verður flutt inn þegar sniðmátið er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="e3fb3-109">Hægt er að fá aðgang að þessari skrá í [Sniðmát greiðsluskýrslu](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="e3fb3-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="e3fb3-110">Hlaða upp skilgreiningu greiðslugagnalíkans.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="e3fb3-111">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e3fb3-112">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e3fb3-113">Veldu skilgreiningarveitu fyrir dæmi um fyrirtæki, veljið 'Litware, Inc.' Ef sést þessi skilgreiningarveita, verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka".</span><span class="sxs-lookup"><span data-stu-id="e3fb3-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="e3fb3-114">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-114">Click Set active.</span></span>
4. <span data-ttu-id="e3fb3-115">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-115">Click Repositories.</span></span>
    * <span data-ttu-id="e3fb3-116">Velja gagnasafn fyrir gerðina Rekstrartilföng, ef tiltækur.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="e3fb3-117">Ef hennar er tiltæk, sleppa eftirfarandi skref um stofnun nýja gagnasafns.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="e3fb3-118">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="e3fb3-119">Í reitnum gerð gagnasafns fyrir skilgreiningar, færðu inn "rekstrartilföng".</span><span class="sxs-lookup"><span data-stu-id="e3fb3-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="e3fb3-120">Smellið á Stofna gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-120">Click Create repository.</span></span>
8. <span data-ttu-id="e3fb3-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-121">Click OK.</span></span>
9. <span data-ttu-id="e3fb3-122">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-122">Click Open.</span></span>
10. <span data-ttu-id="e3fb3-123">Í trénu skal velja „Greiðslulíkan“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="e3fb3-124">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-124">Click Import.</span></span>
    * <span data-ttu-id="e3fb3-125">Flytja inn þetta gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-125">Import this data model.</span></span> <span data-ttu-id="e3fb3-126">Það verður notað sem gagnagjafi í nýja skilgreiningu sniðs.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="e3fb3-127">Sleppa þessu þrepi ef skilgreiningin hefur þegar verið flutt.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="e3fb3-128">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-128">Click Yes.</span></span>
13. <span data-ttu-id="e3fb3-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-129">Close the page.</span></span>
14. <span data-ttu-id="e3fb3-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="e3fb3-131">Stofna nýja skilgreiningu á sniði</span><span class="sxs-lookup"><span data-stu-id="e3fb3-131">Create a new format configuration</span></span>
1. <span data-ttu-id="e3fb3-132">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="e3fb3-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="e3fb3-133">Í trénu skal velja „Greiðslulíkan“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="e3fb3-134">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="e3fb3-135">Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkani PaymentModel“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="e3fb3-136">Stofna snið sem byggir á gagnalíkani PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="e3fb3-137">Í svæðið Heiti, Færðu inn 'dæmi um vinnublaðsskýrslu '.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="e3fb3-138">Dæmi um vinnublaðsskýrslu</span><span class="sxs-lookup"><span data-stu-id="e3fb3-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="e3fb3-139">ÆU reitnum Lýsing, færðu inn "Dæmi um vinnublaðsskýrslu fyrir greiðslur lánardrottna".</span><span class="sxs-lookup"><span data-stu-id="e3fb3-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="e3fb3-140">Dæmi um vinnublaðsskýrslu fyrir greiðslur lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="e3fb3-141">Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="e3fb3-142">Veljið skilgreininguna 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="e3fb3-143">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="e3fb3-144">Hanna nýtt skjal í sniði OPENXML vinnublaði</span><span class="sxs-lookup"><span data-stu-id="e3fb3-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="e3fb3-145">Í trénu skal velja „greiðslulíkan/dæmi um vinnublaðsskýrslu“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="e3fb3-146">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-146">Click Designer.</span></span>
3. <span data-ttu-id="e3fb3-147">Í aðgerðasvæðinu er smellt á innflutningur.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="e3fb3-148">Smella á Flytja inn úr Excel</span><span class="sxs-lookup"><span data-stu-id="e3fb3-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="e3fb3-149">Smellt er á viðhengi</span><span class="sxs-lookup"><span data-stu-id="e3fb3-149">Click Attachments.</span></span>
    * <span data-ttu-id="e3fb3-150">Tengja fyrirliggjandi Excel-skjalið sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="e3fb3-151">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-151">Click New.</span></span>
7. <span data-ttu-id="e3fb3-152">Smella á Skrá</span><span class="sxs-lookup"><span data-stu-id="e3fb3-152">Click File.</span></span>
    * <span data-ttu-id="e3fb3-153">Benda á fyrirliggjandi Excel-skrá.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="e3fb3-154">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-154">Close the page.</span></span>
9. <span data-ttu-id="e3fb3-155">Sláið inn eða veldu gildi í reitnum sniðmát.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="e3fb3-156">Veljið viðhengda Excel-skráin sem nota á sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="e3fb3-157">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-157">Click OK.</span></span>
    * <span data-ttu-id="e3fb3-158">Athugið að sniðshlutar Rafræn skýrslugerð hafa verið stofnað í hönnunarsniði sem byggir á uppbygging MS Excel-skjals sem vísað er úr (nefnd svið).</span><span class="sxs-lookup"><span data-stu-id="e3fb3-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="e3fb3-159">Stofna nýja gagnagjafa til að reikna samtölur eftir gjaldmiðilskóða</span><span class="sxs-lookup"><span data-stu-id="e3fb3-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="e3fb3-160">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="e3fb3-161">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="e3fb3-162">Í trénu skal velja „virkni\Flokka eftir“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="e3fb3-163">Í reitnum Heiti skal færa inn 'PaymentByCurrency'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="e3fb3-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="e3fb3-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="e3fb3-165">Smella á Breyta hópi eftir</span><span class="sxs-lookup"><span data-stu-id="e3fb3-165">Click Edit group by.</span></span>
6. <span data-ttu-id="e3fb3-166">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="e3fb3-167">Veljið 'model\Payments', í trénu.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="e3fb3-168">Smellt er á Bæta reit við</span><span class="sxs-lookup"><span data-stu-id="e3fb3-168">Click Add field to.</span></span>
9. <span data-ttu-id="e3fb3-169">Veldu hvað skal flokka</span><span class="sxs-lookup"><span data-stu-id="e3fb3-169">Click What to group.</span></span>
10. <span data-ttu-id="e3fb3-170">Í trénu skal víkka út 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="e3fb3-171">Veljið 'líkan\greiðslur', í trénu.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="e3fb3-172">Smellt er á Bæta reit við</span><span class="sxs-lookup"><span data-stu-id="e3fb3-172">Click Add field to.</span></span>
13. <span data-ttu-id="e3fb3-173">Smellt er á Flokkaðir reitir</span><span class="sxs-lookup"><span data-stu-id="e3fb3-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="e3fb3-174">Í trénu veljið 'model\Payments\Instructed Amount(InstructedAmount)'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="e3fb3-175">Smellt er á Bæta reit við</span><span class="sxs-lookup"><span data-stu-id="e3fb3-175">Click Add field to.</span></span>
16. <span data-ttu-id="e3fb3-176">Smellt er á Uppsöfnunarreitir</span><span class="sxs-lookup"><span data-stu-id="e3fb3-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="e3fb3-177">Veljið valkost í svæðinu aðferð.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="e3fb3-178">Velja samsteypuaðgerðina SAMTÖLU.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="e3fb3-179">Í reitnum Heiti skal færa inn 'TotalInstructuredAmount'</span><span class="sxs-lookup"><span data-stu-id="e3fb3-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="e3fb3-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="e3fb3-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="e3fb3-181">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-181">Click Save.</span></span>
20. <span data-ttu-id="e3fb3-182">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-182">Close the page.</span></span>
21. <span data-ttu-id="e3fb3-183">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="e3fb3-184">Varpa sniðsíhlutum í gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="e3fb3-184">Map format components to data sources</span></span>
1. <span data-ttu-id="e3fb3-185">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="e3fb3-186">Í trénu skal víkka út 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="e3fb3-187">Í trénu skal útvíkka 'model\Payments\Initiating Party(InitiatingParty)'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="e3fb3-188">Í trénu skal útvíkka 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="e3fb3-189">Í tré skal víkka 'Excel\ReportHeader'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="e3fb3-190">Í tré skal velja 'Excel\ReportHeader\CompanyName'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="e3fb3-191">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-191">Click Bind.</span></span>
8. <span data-ttu-id="e3fb3-192">Útvíkka 'model\Payments\Creditor', í trénu.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="e3fb3-193">Í trénu skal útvíkka 'model\Payments\Creditor\Identification'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="e3fb3-194">Í trénu skal velja 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="e3fb3-195">Í tré skal víkka 'Excel\PaymLines'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="e3fb3-196">Í tré skal velja 'Excel\PaymLines\VendAccountName'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="e3fb3-197">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-197">Click Bind.</span></span>
14. <span data-ttu-id="e3fb3-198">Veljið 'model\Payments\Creditor\Name', í trénu.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="e3fb3-199">Í tré skal velja 'Excel\PaymLines\VendName'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="e3fb3-200">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-200">Click Bind.</span></span>
17. <span data-ttu-id="e3fb3-201">Í trénu skal víkka út 'model\Payments\Creditor Agent(CreditorAgent)'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="e3fb3-202">Í trénu skal velja 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="e3fb3-203">Í tré skal velja 'Excel\PaymLines\Bank'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="e3fb3-204">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-204">Click Bind.</span></span>
21. <span data-ttu-id="e3fb3-205">Í trénu skal velja 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="e3fb3-206">Í tré skal velja 'Excel\PaymLines\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="e3fb3-207">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-207">Click Bind.</span></span>
24. <span data-ttu-id="e3fb3-208">Í trénu skal víkka út 'model\Payments\Creditor Account(CreditorAccount)'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="e3fb3-209">Í trénu skal víkka út 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="e3fb3-210">Í trénu skal velja 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="e3fb3-211">Í tré skal velja 'Excel\PaymLines\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="e3fb3-212">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-212">Click Bind.</span></span>
29. <span data-ttu-id="e3fb3-213">Í trénu veljið 'model\Payments\Instructed Amount(InstructedAmount)'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="e3fb3-214">Í tré skal velja 'Excel\PaymLines\Debit'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="e3fb3-215">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-215">Click Bind.</span></span>
32. <span data-ttu-id="e3fb3-216">Útvíkka 'model\Payments\Creditor', í trénu.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="e3fb3-217">Í trénu skal víkka út 'model\Payments\Creditor Account(CreditorAccount)'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="e3fb3-218">Í trénu skal víkka út 'model\Payments\Creditor Agent(CreditorAgent)'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="e3fb3-219">Veljið 'líkan\greiðslur', í trénu.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="e3fb3-220">Í tré skal velja 'Excel\PaymLines\Currency'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="e3fb3-221">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-221">Click Bind.</span></span>
38. <span data-ttu-id="e3fb3-222">Í trénu skal víkka út 'PaymentByCurrency'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="e3fb3-223">Í trénu skal víkka út 'PaymentByCurrency\grouped'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="e3fb3-224">Í trénu skal velja 'PaymentByCurrency\grouped\Currency'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="e3fb3-225">Í tré skal víkka 'Excel\SummaryLines'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="e3fb3-226">Í tré skal velja 'Excel\SummaryLines\SummaryCurrency'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="e3fb3-227">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-227">Click Bind.</span></span>
44. <span data-ttu-id="e3fb3-228">Í trénu skal víkka út 'PaymentByCurrency\aggregated'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="e3fb3-229">Í trénu skal velja 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="e3fb3-230">Í tré skal velja 'Excel\SummaryLines\SummaryAmount'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="e3fb3-231">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-231">Click Bind.</span></span>
48. <span data-ttu-id="e3fb3-232">Í trénu skal velja 'PaymentByCurrency'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="e3fb3-233">Í tré skal velja 'Excel\SummaryLines'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="e3fb3-234">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-234">Click Bind.</span></span>
51. <span data-ttu-id="e3fb3-235">Veljið 'model\Payments', í trénu.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="e3fb3-236">Í tré skal velja 'Excel\PaymLines'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="e3fb3-237">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-237">Click Bind.</span></span>
54. <span data-ttu-id="e3fb3-238">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-238">Click Save.</span></span>
55. <span data-ttu-id="e3fb3-239">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="e3fb3-240">Nota stofnaða grunnstillingu fyrir greiðsluvinnslu</span><span class="sxs-lookup"><span data-stu-id="e3fb3-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="e3fb3-241">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-241">Click Change status.</span></span>
2. <span data-ttu-id="e3fb3-242">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-242">Click Complete.</span></span>
3. <span data-ttu-id="e3fb3-243">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-243">Click OK.</span></span>
4. <span data-ttu-id="e3fb3-244">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-244">Close the page.</span></span>
5. <span data-ttu-id="e3fb3-245">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-245">Close the page.</span></span>
6. <span data-ttu-id="e3fb3-246">Fara í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="e3fb3-247">Nota flýtiafmörkun til að sía í svæði Greiðsluháttur með gildinu „Rafrænt“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="e3fb3-248">Rafrænt</span><span class="sxs-lookup"><span data-stu-id="e3fb3-248">Electronic</span></span>  
8. <span data-ttu-id="e3fb3-249">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-249">Click Edit.</span></span>
9. <span data-ttu-id="e3fb3-250">Útvíkka hlutann Skráarsnið.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="e3fb3-251">Velja skal Já í Almennan rafræna skýrslugerð svæði.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="e3fb3-252">Færa inn eða velja gildi í reitnum skilgreiningu útflutningssniðs.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="e3fb3-253">Veljið skilgreininguna 'Dæmi um vinnublaðsskýrslu'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="e3fb3-254">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-254">Click Save.</span></span>
13. <span data-ttu-id="e3fb3-255">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="e3fb3-256">Nota stofnaða skilgreiningu fyrir prófun á vinnslu greiðslubóka</span><span class="sxs-lookup"><span data-stu-id="e3fb3-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="e3fb3-257">Fara í Viðskiptaskuldir > Greiðslur > Greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="e3fb3-258">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-258">Click New.</span></span>
    * <span data-ttu-id="e3fb3-259">Stofna nýja greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="e3fb3-260">Í svæðið Heiti skal slá inn ‚VendPay'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="e3fb3-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="e3fb3-261">VendPay</span></span>  
4. <span data-ttu-id="e3fb3-262">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-262">Click Lines.</span></span>
5. <span data-ttu-id="e3fb3-263">Í svæðinu lykill, skal tilgreina gildi 'GB_SI_000001'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="e3fb3-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="e3fb3-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="e3fb3-265">Stilla debet á '1000'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="e3fb3-266">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-266">Click New.</span></span>
8. <span data-ttu-id="e3fb3-267">Í svæðinu lykill, skal tilgreina gildi 'GB_SI_000005'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="e3fb3-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="e3fb3-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="e3fb3-269">Stilla debet á '2000'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="e3fb3-270">Í reitinn gjaldmiðill skal slá inn EUR.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="e3fb3-271">EUR</span><span class="sxs-lookup"><span data-stu-id="e3fb3-271">EUR</span></span>  
11. <span data-ttu-id="e3fb3-272">Í reitinn Mótlykill skal tilgreina gildin ''GBSI OPER'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="e3fb3-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="e3fb3-273">GBSI OPER</span></span>  
12. <span data-ttu-id="e3fb3-274">Í reitnum Greiðsluháttur skal slá inn 'Rafrænt'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="e3fb3-275">Rafrænt</span><span class="sxs-lookup"><span data-stu-id="e3fb3-275">Electronic</span></span>  
13. <span data-ttu-id="e3fb3-276">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-276">Click Save.</span></span>
14. <span data-ttu-id="e3fb3-277">Smelltu á Mynda greiðslur.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-277">Click Generate payments.</span></span>
15. <span data-ttu-id="e3fb3-278">Í reitnum Greiðsluháttur skal slá inn 'Rafrænt'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="e3fb3-279">Rafrænt</span><span class="sxs-lookup"><span data-stu-id="e3fb3-279">Electronic</span></span>  
16. <span data-ttu-id="e3fb3-280">Í svæði Skráarheiti skal slá inn „Greiðslur“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="e3fb3-281">Til dæmis, skráið greiðslur.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="e3fb3-282">Í reitinn Bankareikningar skal slá inn 'GBSI OPER'.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="e3fb3-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="e3fb3-283">GBSI OPER</span></span>  
18. <span data-ttu-id="e3fb3-284">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-284">Click OK.</span></span>
19. <span data-ttu-id="e3fb3-285">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-285">Click OK.</span></span>
    * <span data-ttu-id="e3fb3-286">Fara yfir stofnaðar vinnublað, þar á meðal upplýsingar um greiðslulínur ásamt samtölur fyrir hvern gjaldmiðilskóði sem notaður er í þessum greiðsluskilaboðum.</span><span class="sxs-lookup"><span data-stu-id="e3fb3-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


