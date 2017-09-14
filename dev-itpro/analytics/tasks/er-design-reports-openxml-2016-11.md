--- 
title: "Hanna skilgreiningu fyrir myndun skýrslna á OpenXML-sniði fyrir rafræna skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi úthlutað á hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað nýja skilgreiningarveitu fyrir rafræna skýrslugerð (ER) sem inniheldur snið til að mynda rafræn skjöl í OPENXML-sniði."
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
ms.openlocfilehash: 51208cbc5118e95fd402cca3cbc228ef1b87a47f
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="design-a-configuration-for-generating-reports-in-openxml-format-for-electronic-reporting-er"></a><span data-ttu-id="23e19-103">Hanna skilgreiningu fyrir myndun skýrslna á OpenXML-sniði fyrir rafræna skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="23e19-103">Design a configuration for generating reports in OpenXML format for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="23e19-104">Eftirfarandi skref útskýra hvernig notandi úthlutað á hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað nýja skilgreiningarveitu fyrir rafræna skýrslugerð (ER) sem inniheldur snið til að mynda rafræn skjöl í OPENXML-sniði.</span><span class="sxs-lookup"><span data-stu-id="23e19-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="23e19-105">Þessi skilgreining verður notuð til að vinna greiðslur lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="23e19-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="23e19-106">Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í GBSI fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="23e19-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="23e19-107">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka".</span><span class="sxs-lookup"><span data-stu-id="23e19-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="23e19-108">Einnig verður að hafa Excel-skráin sem verður flutt inn þegar sniðmátið er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="23e19-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="23e19-109">Þessi skrá er hægt að fá aðgang að í: https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span><span class="sxs-lookup"><span data-stu-id="23e19-109">This file can be accessed from:  https://msdynamics.blob.core.windows.net/media/2016/04/SampleVendPaymWsReport.xlsx</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="23e19-110">Hlaða upp skilgreiningu greiðslugagnalíkans.</span><span class="sxs-lookup"><span data-stu-id="23e19-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="23e19-111">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="23e19-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="23e19-112">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="23e19-112">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="23e19-113">Veldu skilgreiningarveitu fyrir dæmi um fyrirtæki, veljið 'Litware, Inc.' Ef sést þessi skilgreiningarveita, verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka".</span><span class="sxs-lookup"><span data-stu-id="23e19-113">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="23e19-114">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="23e19-114">Click Set active.</span></span>
4. <span data-ttu-id="23e19-115">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="23e19-115">Click Repositories.</span></span>
    * <span data-ttu-id="23e19-116">Velja gagnasafn fyrir gerðina Rekstrartilföng, ef tiltækur.</span><span class="sxs-lookup"><span data-stu-id="23e19-116">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="23e19-117">Ef hennar er tiltæk, sleppa eftirfarandi skref um stofnun nýja gagnasafns.</span><span class="sxs-lookup"><span data-stu-id="23e19-117">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="23e19-118">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="23e19-118">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="23e19-119">Í reitnum gerð gagnasafns fyrir skilgreiningar, færðu inn "rekstrartilföng".</span><span class="sxs-lookup"><span data-stu-id="23e19-119">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="23e19-120">Smellið á Stofna gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="23e19-120">Click Create repository.</span></span>
8. <span data-ttu-id="23e19-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="23e19-121">Click OK.</span></span>
9. <span data-ttu-id="23e19-122">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="23e19-122">Click Open.</span></span>
10. <span data-ttu-id="23e19-123">Í trénu skal velja „Greiðslulíkan“.</span><span class="sxs-lookup"><span data-stu-id="23e19-123">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="23e19-124">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="23e19-124">Click Import.</span></span>
    * <span data-ttu-id="23e19-125">Flytja inn þetta gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="23e19-125">Import this data model.</span></span> <span data-ttu-id="23e19-126">Það verður notað sem gagnagjafi í nýja skilgreiningu sniðs.</span><span class="sxs-lookup"><span data-stu-id="23e19-126">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="23e19-127">Sleppa þessu þrepi ef skilgreiningin hefur þegar verið flutt.</span><span class="sxs-lookup"><span data-stu-id="23e19-127">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="23e19-128">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="23e19-128">Click Yes.</span></span>
13. <span data-ttu-id="23e19-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23e19-129">Close the page.</span></span>
14. <span data-ttu-id="23e19-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23e19-130">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="23e19-131">Stofna nýja skilgreiningu á sniði</span><span class="sxs-lookup"><span data-stu-id="23e19-131">Create a new format configuration</span></span>
1. <span data-ttu-id="23e19-132">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="23e19-132">Click Reporting configurations.</span></span>
2. <span data-ttu-id="23e19-133">Í trénu skal velja „Greiðslulíkan“.</span><span class="sxs-lookup"><span data-stu-id="23e19-133">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="23e19-134">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="23e19-134">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="23e19-135">Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkani PaymentModel“.</span><span class="sxs-lookup"><span data-stu-id="23e19-135">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="23e19-136">Stofna snið sem byggir á gagnalíkani PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="23e19-136">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="23e19-137">Í svæðið Heiti, Færðu inn 'dæmi um vinnublaðsskýrslu '.</span><span class="sxs-lookup"><span data-stu-id="23e19-137">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="23e19-138">Dæmi um vinnublaðsskýrslu</span><span class="sxs-lookup"><span data-stu-id="23e19-138">Sample worksheet report</span></span>  
6. <span data-ttu-id="23e19-139">ÆU reitnum Lýsing, færðu inn "Dæmi um vinnublaðsskýrslu fyrir greiðslur lánardrottna".</span><span class="sxs-lookup"><span data-stu-id="23e19-139">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="23e19-140">Dæmi um vinnublaðsskýrslu fyrir greiðslur lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="23e19-140">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="23e19-141">Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="23e19-141">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="23e19-142">Veljið skilgreininguna 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="23e19-142">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="23e19-143">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="23e19-143">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="23e19-144">Hanna nýtt skjal í sniði OPENXML vinnublaði</span><span class="sxs-lookup"><span data-stu-id="23e19-144">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="23e19-145">Í trénu skal velja „greiðslulíkan/dæmi um vinnublaðsskýrslu“.</span><span class="sxs-lookup"><span data-stu-id="23e19-145">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="23e19-146">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="23e19-146">Click Designer.</span></span>
3. <span data-ttu-id="23e19-147">Í aðgerðasvæðinu er smellt á innflutningur.</span><span class="sxs-lookup"><span data-stu-id="23e19-147">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="23e19-148">Smella á Flytja inn úr Excel</span><span class="sxs-lookup"><span data-stu-id="23e19-148">Click Import from Excel.</span></span>
5. <span data-ttu-id="23e19-149">Smellt er á viðhengi</span><span class="sxs-lookup"><span data-stu-id="23e19-149">Click Attachments.</span></span>
    * <span data-ttu-id="23e19-150">Tengja fyrirliggjandi Excel-skjalið sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="23e19-150">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="23e19-151">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="23e19-151">Click New.</span></span>
7. <span data-ttu-id="23e19-152">Smella á Skrá</span><span class="sxs-lookup"><span data-stu-id="23e19-152">Click File.</span></span>
    * <span data-ttu-id="23e19-153">Benda á fyrirliggjandi Excel-skrá.</span><span class="sxs-lookup"><span data-stu-id="23e19-153">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="23e19-154">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23e19-154">Close the page.</span></span>
9. <span data-ttu-id="23e19-155">Sláið inn eða veldu gildi í reitnum sniðmát.</span><span class="sxs-lookup"><span data-stu-id="23e19-155">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="23e19-156">Veljið viðhengda Excel-skráin sem nota á sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="23e19-156">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="23e19-157">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="23e19-157">Click OK.</span></span>
    * <span data-ttu-id="23e19-158">Athugið að sniðshlutar Rafræn skýrslugerð hafa verið stofnað í hönnunarsniði sem byggir á uppbygging MS Excel-skjals sem vísað er úr (nefnd svið).</span><span class="sxs-lookup"><span data-stu-id="23e19-158">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="23e19-159">Stofna nýja gagnagjafa til að reikna samtölur eftir gjaldmiðilskóða</span><span class="sxs-lookup"><span data-stu-id="23e19-159">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="23e19-160">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="23e19-160">Click the Mapping tab.</span></span>
2. <span data-ttu-id="23e19-161">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="23e19-161">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="23e19-162">Í trénu skal velja „virkni\Flokka eftir“.</span><span class="sxs-lookup"><span data-stu-id="23e19-162">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="23e19-163">Í reitnum Heiti skal færa inn 'PaymentByCurrency'.</span><span class="sxs-lookup"><span data-stu-id="23e19-163">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="23e19-164">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="23e19-164">PaymentByCurrency</span></span>  
5. <span data-ttu-id="23e19-165">Smella á Breyta hópi eftir</span><span class="sxs-lookup"><span data-stu-id="23e19-165">Click Edit group by.</span></span>
6. <span data-ttu-id="23e19-166">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="23e19-166">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="23e19-167">Veljið 'model\Payments', í trénu.</span><span class="sxs-lookup"><span data-stu-id="23e19-167">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="23e19-168">Smellt er á Bæta reit við</span><span class="sxs-lookup"><span data-stu-id="23e19-168">Click Add field to.</span></span>
9. <span data-ttu-id="23e19-169">Veldu hvað skal flokka</span><span class="sxs-lookup"><span data-stu-id="23e19-169">Click What to group.</span></span>
10. <span data-ttu-id="23e19-170">Í trénu skal víkka út 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="23e19-170">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="23e19-171">Veljið 'líkan\greiðslur', í trénu.</span><span class="sxs-lookup"><span data-stu-id="23e19-171">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="23e19-172">Smellt er á Bæta reit við</span><span class="sxs-lookup"><span data-stu-id="23e19-172">Click Add field to.</span></span>
13. <span data-ttu-id="23e19-173">Smellt er á Flokkaðir reitir</span><span class="sxs-lookup"><span data-stu-id="23e19-173">Click Grouped fields.</span></span>
14. <span data-ttu-id="23e19-174">Í trénu veljið 'model\Payments\Instructed Amount(InstructedAmount)'.</span><span class="sxs-lookup"><span data-stu-id="23e19-174">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="23e19-175">Smellt er á Bæta reit við</span><span class="sxs-lookup"><span data-stu-id="23e19-175">Click Add field to.</span></span>
16. <span data-ttu-id="23e19-176">Smellt er á Uppsöfnunarreitir</span><span class="sxs-lookup"><span data-stu-id="23e19-176">Click Aggregation fields.</span></span>
17. <span data-ttu-id="23e19-177">Veljið valkost í svæðinu aðferð.</span><span class="sxs-lookup"><span data-stu-id="23e19-177">In the Method field, select an option.</span></span>
    * <span data-ttu-id="23e19-178">Velja samsteypuaðgerðina SAMTÖLU.</span><span class="sxs-lookup"><span data-stu-id="23e19-178">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="23e19-179">Í reitnum Heiti skal færa inn 'TotalInstructuredAmount'</span><span class="sxs-lookup"><span data-stu-id="23e19-179">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="23e19-180">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="23e19-180">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="23e19-181">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="23e19-181">Click Save.</span></span>
20. <span data-ttu-id="23e19-182">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23e19-182">Close the page.</span></span>
21. <span data-ttu-id="23e19-183">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="23e19-183">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="23e19-184">Varpa sniðsíhlutum í gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="23e19-184">Map format components to data sources</span></span>
1. <span data-ttu-id="23e19-185">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="23e19-185">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="23e19-186">Í trénu skal víkka út 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="23e19-186">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="23e19-187">Í trénu skal útvíkka 'model\Payments\Initiating Party(InitiatingParty)'.</span><span class="sxs-lookup"><span data-stu-id="23e19-187">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="23e19-188">Í trénu skal útvíkka 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span><span class="sxs-lookup"><span data-stu-id="23e19-188">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="23e19-189">Í tré skal víkka 'Excel\ReportHeader'.</span><span class="sxs-lookup"><span data-stu-id="23e19-189">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="23e19-190">Í tré skal velja 'Excel\ReportHeader\CompanyName'.</span><span class="sxs-lookup"><span data-stu-id="23e19-190">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="23e19-191">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="23e19-191">Click Bind.</span></span>
8. <span data-ttu-id="23e19-192">Útvíkka 'model\Payments\Creditor', í trénu.</span><span class="sxs-lookup"><span data-stu-id="23e19-192">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="23e19-193">Í trénu skal útvíkka 'model\Payments\Creditor\Identification'.</span><span class="sxs-lookup"><span data-stu-id="23e19-193">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="23e19-194">Í trénu skal velja 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span><span class="sxs-lookup"><span data-stu-id="23e19-194">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="23e19-195">Í tré skal víkka 'Excel\PaymLines'.</span><span class="sxs-lookup"><span data-stu-id="23e19-195">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="23e19-196">Í tré skal velja 'Excel\PaymLines\VendAccountName'.</span><span class="sxs-lookup"><span data-stu-id="23e19-196">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="23e19-197">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="23e19-197">Click Bind.</span></span>
14. <span data-ttu-id="23e19-198">Veljið 'model\Payments\Creditor\Name', í trénu.</span><span class="sxs-lookup"><span data-stu-id="23e19-198">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="23e19-199">Í tré skal velja 'Excel\PaymLines\VendName'.</span><span class="sxs-lookup"><span data-stu-id="23e19-199">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="23e19-200">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="23e19-200">Click Bind.</span></span>
17. <span data-ttu-id="23e19-201">Í trénu skal víkka út 'model\Payments\Creditor Agent(CreditorAgent)'.</span><span class="sxs-lookup"><span data-stu-id="23e19-201">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="23e19-202">Í trénu skal velja 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span><span class="sxs-lookup"><span data-stu-id="23e19-202">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="23e19-203">Í tré skal velja 'Excel\PaymLines\Bank'.</span><span class="sxs-lookup"><span data-stu-id="23e19-203">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="23e19-204">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="23e19-204">Click Bind.</span></span>
21. <span data-ttu-id="23e19-205">Í trénu skal velja 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span><span class="sxs-lookup"><span data-stu-id="23e19-205">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="23e19-206">Í tré skal velja 'Excel\PaymLines\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="23e19-206">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="23e19-207">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="23e19-207">Click Bind.</span></span>
24. <span data-ttu-id="23e19-208">Í trénu skal víkka út 'model\Payments\Creditor Account(CreditorAccount)'.</span><span class="sxs-lookup"><span data-stu-id="23e19-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="23e19-209">Í trénu skal víkka út 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span><span class="sxs-lookup"><span data-stu-id="23e19-209">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="23e19-210">Í trénu skal velja 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span><span class="sxs-lookup"><span data-stu-id="23e19-210">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="23e19-211">Í tré skal velja 'Excel\PaymLines\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="23e19-211">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="23e19-212">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="23e19-212">Click Bind.</span></span>
29. <span data-ttu-id="23e19-213">Í trénu veljið 'model\Payments\Instructed Amount(InstructedAmount)'.</span><span class="sxs-lookup"><span data-stu-id="23e19-213">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="23e19-214">Í tré skal velja 'Excel\PaymLines\Debit'.</span><span class="sxs-lookup"><span data-stu-id="23e19-214">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="23e19-215">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="23e19-215">Click Bind.</span></span>
32. <span data-ttu-id="23e19-216">Útvíkka 'model\Payments\Creditor', í trénu.</span><span class="sxs-lookup"><span data-stu-id="23e19-216">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="23e19-217">Í trénu skal víkka út 'model\Payments\Creditor Account(CreditorAccount)'.</span><span class="sxs-lookup"><span data-stu-id="23e19-217">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="23e19-218">Í trénu skal víkka út 'model\Payments\Creditor Agent(CreditorAgent)'.</span><span class="sxs-lookup"><span data-stu-id="23e19-218">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="23e19-219">Veljið 'líkan\greiðslur', í trénu.</span><span class="sxs-lookup"><span data-stu-id="23e19-219">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="23e19-220">Í tré skal velja 'Excel\PaymLines\Currency'.</span><span class="sxs-lookup"><span data-stu-id="23e19-220">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="23e19-221">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="23e19-221">Click Bind.</span></span>
38. <span data-ttu-id="23e19-222">Í trénu skal víkka út 'PaymentByCurrency'.</span><span class="sxs-lookup"><span data-stu-id="23e19-222">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="23e19-223">Í trénu skal víkka út 'PaymentByCurrency\grouped'.</span><span class="sxs-lookup"><span data-stu-id="23e19-223">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="23e19-224">Í trénu skal velja 'PaymentByCurrency\grouped\Currency'.</span><span class="sxs-lookup"><span data-stu-id="23e19-224">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="23e19-225">Í tré skal víkka 'Excel\SummaryLines'.</span><span class="sxs-lookup"><span data-stu-id="23e19-225">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="23e19-226">Í tré skal velja 'Excel\SummaryLines\SummaryCurrency'.</span><span class="sxs-lookup"><span data-stu-id="23e19-226">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="23e19-227">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="23e19-227">Click Bind.</span></span>
44. <span data-ttu-id="23e19-228">Í trénu skal víkka út 'PaymentByCurrency\aggregated'.</span><span class="sxs-lookup"><span data-stu-id="23e19-228">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="23e19-229">Í trénu skal velja 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span><span class="sxs-lookup"><span data-stu-id="23e19-229">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="23e19-230">Í tré skal velja 'Excel\SummaryLines\SummaryAmount'.</span><span class="sxs-lookup"><span data-stu-id="23e19-230">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="23e19-231">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="23e19-231">Click Bind.</span></span>
48. <span data-ttu-id="23e19-232">Í trénu skal velja 'PaymentByCurrency'.</span><span class="sxs-lookup"><span data-stu-id="23e19-232">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="23e19-233">Í tré skal velja 'Excel\SummaryLines'.</span><span class="sxs-lookup"><span data-stu-id="23e19-233">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="23e19-234">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="23e19-234">Click Bind.</span></span>
51. <span data-ttu-id="23e19-235">Veljið 'model\Payments', í trénu.</span><span class="sxs-lookup"><span data-stu-id="23e19-235">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="23e19-236">Í tré skal velja 'Excel\PaymLines'.</span><span class="sxs-lookup"><span data-stu-id="23e19-236">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="23e19-237">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="23e19-237">Click Bind.</span></span>
54. <span data-ttu-id="23e19-238">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="23e19-238">Click Save.</span></span>
55. <span data-ttu-id="23e19-239">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23e19-239">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="23e19-240">Nota stofnaða grunnstillingu fyrir greiðsluvinnslu</span><span class="sxs-lookup"><span data-stu-id="23e19-240">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="23e19-241">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="23e19-241">Click Change status.</span></span>
2. <span data-ttu-id="23e19-242">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="23e19-242">Click Complete.</span></span>
3. <span data-ttu-id="23e19-243">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="23e19-243">Click OK.</span></span>
4. <span data-ttu-id="23e19-244">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23e19-244">Close the page.</span></span>
5. <span data-ttu-id="23e19-245">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23e19-245">Close the page.</span></span>
6. <span data-ttu-id="23e19-246">Fara í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.</span><span class="sxs-lookup"><span data-stu-id="23e19-246">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="23e19-247">Nota flýtiafmörkun til að sía í svæði Greiðsluháttur með gildinu „Rafrænt“.</span><span class="sxs-lookup"><span data-stu-id="23e19-247">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="23e19-248">Rafrænt</span><span class="sxs-lookup"><span data-stu-id="23e19-248">Electronic</span></span>  
8. <span data-ttu-id="23e19-249">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="23e19-249">Click Edit.</span></span>
9. <span data-ttu-id="23e19-250">Útvíkka hlutann Skráarsnið.</span><span class="sxs-lookup"><span data-stu-id="23e19-250">Expand the File formats section.</span></span>
10. <span data-ttu-id="23e19-251">Velja skal Já í Almennan rafræna skýrslugerð svæði.</span><span class="sxs-lookup"><span data-stu-id="23e19-251">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="23e19-252">Færa inn eða velja gildi í reitnum skilgreiningu útflutningssniðs.</span><span class="sxs-lookup"><span data-stu-id="23e19-252">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="23e19-253">Veljið skilgreininguna 'Dæmi um vinnublaðsskýrslu'.</span><span class="sxs-lookup"><span data-stu-id="23e19-253">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="23e19-254">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="23e19-254">Click Save.</span></span>
13. <span data-ttu-id="23e19-255">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="23e19-255">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="23e19-256">Nota stofnaða skilgreiningu fyrir prófun á vinnslu greiðslubóka</span><span class="sxs-lookup"><span data-stu-id="23e19-256">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="23e19-257">Fara í Viðskiptaskuldir > Greiðslur > Greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="23e19-257">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="23e19-258">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="23e19-258">Click New.</span></span>
    * <span data-ttu-id="23e19-259">Stofna nýja greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="23e19-259">Create a new payment journal.</span></span>  
3. <span data-ttu-id="23e19-260">Í svæðið Heiti skal slá inn ‚VendPay'.</span><span class="sxs-lookup"><span data-stu-id="23e19-260">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="23e19-261">VendPay</span><span class="sxs-lookup"><span data-stu-id="23e19-261">VendPay</span></span>  
4. <span data-ttu-id="23e19-262">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="23e19-262">Click Lines.</span></span>
5. <span data-ttu-id="23e19-263">Í svæðinu lykill, skal tilgreina gildi 'GB_SI_000001'.</span><span class="sxs-lookup"><span data-stu-id="23e19-263">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="23e19-264">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="23e19-264">GB_SI_000001</span></span>  
6. <span data-ttu-id="23e19-265">Stilla debet á '1000'.</span><span class="sxs-lookup"><span data-stu-id="23e19-265">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="23e19-266">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="23e19-266">Click New.</span></span>
8. <span data-ttu-id="23e19-267">Í svæðinu lykill, skal tilgreina gildi 'GB_SI_000005'.</span><span class="sxs-lookup"><span data-stu-id="23e19-267">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="23e19-268">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="23e19-268">GB_SI_000005</span></span>  
9. <span data-ttu-id="23e19-269">Stilla debet á '2000'.</span><span class="sxs-lookup"><span data-stu-id="23e19-269">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="23e19-270">Í reitinn gjaldmiðill skal slá inn EUR.</span><span class="sxs-lookup"><span data-stu-id="23e19-270">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="23e19-271">EUR</span><span class="sxs-lookup"><span data-stu-id="23e19-271">EUR</span></span>  
11. <span data-ttu-id="23e19-272">Í reitinn Mótlykill skal tilgreina gildin ''GBSI OPER'.</span><span class="sxs-lookup"><span data-stu-id="23e19-272">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="23e19-273">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="23e19-273">GBSI OPER</span></span>  
12. <span data-ttu-id="23e19-274">Í reitnum Greiðsluháttur skal slá inn 'Rafrænt'.</span><span class="sxs-lookup"><span data-stu-id="23e19-274">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="23e19-275">Rafrænt</span><span class="sxs-lookup"><span data-stu-id="23e19-275">Electronic</span></span>  
13. <span data-ttu-id="23e19-276">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="23e19-276">Click Save.</span></span>
14. <span data-ttu-id="23e19-277">Smelltu á Mynda greiðslur.</span><span class="sxs-lookup"><span data-stu-id="23e19-277">Click Generate payments.</span></span>
15. <span data-ttu-id="23e19-278">Í reitnum Greiðsluháttur skal slá inn 'Rafrænt'.</span><span class="sxs-lookup"><span data-stu-id="23e19-278">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="23e19-279">Rafrænt</span><span class="sxs-lookup"><span data-stu-id="23e19-279">Electronic</span></span>  
16. <span data-ttu-id="23e19-280">Í svæði Skráarheiti skal slá inn „Greiðslur“.</span><span class="sxs-lookup"><span data-stu-id="23e19-280">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="23e19-281">Til dæmis, skráið greiðslur.</span><span class="sxs-lookup"><span data-stu-id="23e19-281">For example, type Payments.</span></span>  
17. <span data-ttu-id="23e19-282">Í reitinn Bankareikningar skal slá inn 'GBSI OPER'.</span><span class="sxs-lookup"><span data-stu-id="23e19-282">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="23e19-283">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="23e19-283">GBSI OPER</span></span>  
18. <span data-ttu-id="23e19-284">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="23e19-284">Click OK.</span></span>
19. <span data-ttu-id="23e19-285">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="23e19-285">Click OK.</span></span>
    * <span data-ttu-id="23e19-286">Fara yfir stofnaðar vinnublað, þar á meðal upplýsingar um greiðslulínur ásamt samtölur fyrir hvern gjaldmiðilskóði sem notaður er í þessum greiðsluskilaboðum.</span><span class="sxs-lookup"><span data-stu-id="23e19-286">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


