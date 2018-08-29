--- 
title: "Hanna skilgreiningar rafrænnar skýrslugerðar til að mynda skýrslur á OpenXML-sniði"
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
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b42cfe36c57a9526e585bbad0fcd31ff60b90397
ms.contentlocale: is-is
ms.lasthandoff: 08/09/2018

---
# <a name="design-er-configurations-to-generate-reports-in-openxml-format"></a><span data-ttu-id="6eda2-103">Hanna skilgreiningar rafrænnar skýrslugerðar til að mynda skýrslur á OpenXML-sniði</span><span class="sxs-lookup"><span data-stu-id="6eda2-103">Design ER configurations to generate reports in OpenXML format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6eda2-104">Eftirfarandi skref útskýra hvernig notandi úthlutað á hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað nýja skilgreiningarveitu fyrir rafræna skýrslugerð (ER) sem inniheldur snið til að mynda rafræn skjöl í OPENXML-sniði.</span><span class="sxs-lookup"><span data-stu-id="6eda2-104">The following steps explain how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="6eda2-105">Þessi skilgreining verður notuð til að vinna greiðslur lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="6eda2-105">This configuration will be used for processing vendor payments.</span></span>



<span data-ttu-id="6eda2-106">Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í GBSI fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="6eda2-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>



<span data-ttu-id="6eda2-107">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka".</span><span class="sxs-lookup"><span data-stu-id="6eda2-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="6eda2-108">Þú verður einnig að sækja og vista Microsoft Excel skrána, [Sniðmát greiðsluskýrslu](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="6eda2-108">You must also download and save the Microsoft Excel file, [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span> 

## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="6eda2-109">Hlaða upp skilgreiningu greiðslugagnalíkans.</span><span class="sxs-lookup"><span data-stu-id="6eda2-109">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="6eda2-110">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="6eda2-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="6eda2-111">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="6eda2-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6eda2-112">Veldu skilgreiningarveitu fyrir dæmi um fyrirtæki, veljið 'Litware, Inc.' Ef sést þessi skilgreiningarveita, verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka".</span><span class="sxs-lookup"><span data-stu-id="6eda2-112">Select the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span>  
3. <span data-ttu-id="6eda2-113">Smellt á Stilla sem virkt.</span><span class="sxs-lookup"><span data-stu-id="6eda2-113">Click Set active.</span></span>
4. <span data-ttu-id="6eda2-114">Smella á Geymslur.</span><span class="sxs-lookup"><span data-stu-id="6eda2-114">Click Repositories.</span></span>
    * <span data-ttu-id="6eda2-115">Velja gagnasafn fyrir gerðina Rekstrartilföng, ef tiltækur.</span><span class="sxs-lookup"><span data-stu-id="6eda2-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="6eda2-116">Ef hennar er tiltæk, sleppa eftirfarandi skref um stofnun nýja gagnasafns.</span><span class="sxs-lookup"><span data-stu-id="6eda2-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="6eda2-117">Smelltu á Bæta við til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="6eda2-117">Click Add to open the drop dialog.</span></span>
6. <span data-ttu-id="6eda2-118">Í reitnum gerð gagnasafns fyrir skilgreiningar, færðu inn "rekstrartilföng".</span><span class="sxs-lookup"><span data-stu-id="6eda2-118">In the Configuration repository type field, enter 'Operations resources'.</span></span>
7. <span data-ttu-id="6eda2-119">Smellið á Stofna gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="6eda2-119">Click Create repository.</span></span>
8. <span data-ttu-id="6eda2-120">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-120">Click OK.</span></span>
9. <span data-ttu-id="6eda2-121">Smellt er á Opin.</span><span class="sxs-lookup"><span data-stu-id="6eda2-121">Click Open.</span></span>
10. <span data-ttu-id="6eda2-122">Í trénu skal velja „Greiðslulíkan“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-122">In the tree, select 'Payment model'.</span></span>
11. <span data-ttu-id="6eda2-123">Smelltu á Flytja inn.</span><span class="sxs-lookup"><span data-stu-id="6eda2-123">Click Import.</span></span>
    * <span data-ttu-id="6eda2-124">Flytja inn þetta gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="6eda2-124">Import this data model.</span></span> <span data-ttu-id="6eda2-125">Það verður notað sem gagnagjafi í nýja skilgreiningu sniðs.</span><span class="sxs-lookup"><span data-stu-id="6eda2-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="6eda2-126">Sleppa þessu þrepi ef skilgreiningin hefur þegar verið flutt.</span><span class="sxs-lookup"><span data-stu-id="6eda2-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="6eda2-127">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="6eda2-127">Click Yes.</span></span>
13. <span data-ttu-id="6eda2-128">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6eda2-128">Close the page.</span></span>
14. <span data-ttu-id="6eda2-129">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6eda2-129">Close the page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="6eda2-130">Stofna nýja skilgreiningu á sniði</span><span class="sxs-lookup"><span data-stu-id="6eda2-130">Create a new format configuration</span></span>
1. <span data-ttu-id="6eda2-131">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="6eda2-131">Click Reporting configurations.</span></span>
2. <span data-ttu-id="6eda2-132">Í trénu skal velja „Greiðslulíkan“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-132">In the tree, select 'Payment model'.</span></span>
3. <span data-ttu-id="6eda2-133">Smellt er á stofna skilgreiningu til að opna fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="6eda2-133">Click Create configuration to open the drop dialog.</span></span>
4. <span data-ttu-id="6eda2-134">Í nýja svæðinu, færðu inn „Snið byggir á gagnalíkani PaymentModel“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-134">In the New field, enter 'Format based on data model PaymentModel'.</span></span>
    * <span data-ttu-id="6eda2-135">Stofna snið sem byggir á gagnalíkani PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="6eda2-135">Create a format that is based on the PaymentModel data model.</span></span>  
5. <span data-ttu-id="6eda2-136">Í svæðið Heiti, Færðu inn 'dæmi um vinnublaðsskýrslu '.</span><span class="sxs-lookup"><span data-stu-id="6eda2-136">In the Name field, type 'Sample worksheet report'.</span></span>
    * <span data-ttu-id="6eda2-137">Dæmi um vinnublaðsskýrslu</span><span class="sxs-lookup"><span data-stu-id="6eda2-137">Sample worksheet report</span></span>  
6. <span data-ttu-id="6eda2-138">ÆU reitnum Lýsing, færðu inn "Dæmi um vinnublaðsskýrslu fyrir greiðslur lánardrottna".</span><span class="sxs-lookup"><span data-stu-id="6eda2-138">In the Description field, type 'Sample worksheet report for vendors’ payments'.</span></span>
    * <span data-ttu-id="6eda2-139">Dæmi um vinnublaðsskýrslu fyrir greiðslur lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="6eda2-139">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="6eda2-140">Í reitinn Skilgreining Gagnalíkans skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="6eda2-140">In the Data model definition field, enter or select a value.</span></span>
    * <span data-ttu-id="6eda2-141">Veljið skilgreininguna 'CustomerCreditTransferInitiation'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-141">Select the 'CustomerCreditTransferInitiation' definition.</span></span>  
8. <span data-ttu-id="6eda2-142">Smelltu á Stofna skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="6eda2-142">Click Create configuration.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="6eda2-143">Hanna nýtt skjal í sniði OPENXML vinnublaði</span><span class="sxs-lookup"><span data-stu-id="6eda2-143">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="6eda2-144">Í trénu skal velja „greiðslulíkan/dæmi um vinnublaðsskýrslu“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-144">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
2. <span data-ttu-id="6eda2-145">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="6eda2-145">Click Designer.</span></span>
3. <span data-ttu-id="6eda2-146">Í aðgerðasvæðinu er smellt á innflutningur.</span><span class="sxs-lookup"><span data-stu-id="6eda2-146">On the Action Pane, click Import.</span></span>
4. <span data-ttu-id="6eda2-147">Smella á Flytja inn úr Excel</span><span class="sxs-lookup"><span data-stu-id="6eda2-147">Click Import from Excel.</span></span>
5. <span data-ttu-id="6eda2-148">Smellt er á viðhengi</span><span class="sxs-lookup"><span data-stu-id="6eda2-148">Click Attachments.</span></span>
    * <span data-ttu-id="6eda2-149">Tengja fyrirliggjandi Excel-skjalið sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="6eda2-149">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="6eda2-150">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-150">Click New.</span></span>
7. <span data-ttu-id="6eda2-151">Smella á Skrá</span><span class="sxs-lookup"><span data-stu-id="6eda2-151">Click File.</span></span>
    * <span data-ttu-id="6eda2-152">Benda á fyrirliggjandi Excel-skrá.</span><span class="sxs-lookup"><span data-stu-id="6eda2-152">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="6eda2-153">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6eda2-153">Close the page.</span></span>
9. <span data-ttu-id="6eda2-154">Sláið inn eða veldu gildi í reitnum sniðmát.</span><span class="sxs-lookup"><span data-stu-id="6eda2-154">In the Template field, enter or select a value.</span></span>
    * <span data-ttu-id="6eda2-155">Veljið viðhengda Excel-skráin sem nota á sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="6eda2-155">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="6eda2-156">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-156">Click OK.</span></span>
    * <span data-ttu-id="6eda2-157">Athugið að sniðshlutar Rafræn skýrslugerð hafa verið stofnað í hönnunarsniði sem byggir á uppbygging MS Excel-skjals sem vísað er úr (nefnd svið).</span><span class="sxs-lookup"><span data-stu-id="6eda2-157">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="6eda2-158">Stofna nýja gagnagjafa til að reikna samtölur eftir gjaldmiðilskóða</span><span class="sxs-lookup"><span data-stu-id="6eda2-158">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="6eda2-159">Smelltu á flipann Vörpun.</span><span class="sxs-lookup"><span data-stu-id="6eda2-159">Click the Mapping tab.</span></span>
2. <span data-ttu-id="6eda2-160">Smelltu á Bæta við rót til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="6eda2-160">Click Add root to open the drop dialog.</span></span>
3. <span data-ttu-id="6eda2-161">Í trénu skal velja „virkni\Flokka eftir“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-161">In the tree, select 'Functions\Group by'.</span></span>
4. <span data-ttu-id="6eda2-162">Í reitnum Heiti skal færa inn 'PaymentByCurrency'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-162">In the Name field, type 'PaymentByCurrency'.</span></span>
    * <span data-ttu-id="6eda2-163">PaymentByCurrency</span><span class="sxs-lookup"><span data-stu-id="6eda2-163">PaymentByCurrency</span></span>  
5. <span data-ttu-id="6eda2-164">Smella á Breyta hópi eftir</span><span class="sxs-lookup"><span data-stu-id="6eda2-164">Click Edit group by.</span></span>
6. <span data-ttu-id="6eda2-165">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-165">In the tree, expand 'model'.</span></span>
7. <span data-ttu-id="6eda2-166">Veljið 'model\Payments', í trénu.</span><span class="sxs-lookup"><span data-stu-id="6eda2-166">In the tree, select 'model\Payments'.</span></span>
8. <span data-ttu-id="6eda2-167">Smellt er á Bæta reit við</span><span class="sxs-lookup"><span data-stu-id="6eda2-167">Click Add field to.</span></span>
9. <span data-ttu-id="6eda2-168">Veldu hvað skal flokka</span><span class="sxs-lookup"><span data-stu-id="6eda2-168">Click What to group.</span></span>
10. <span data-ttu-id="6eda2-169">Í trénu skal víkka út 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-169">In the tree, expand 'model\Payments'.</span></span>
11. <span data-ttu-id="6eda2-170">Veljið 'líkan\greiðslur', í trénu.</span><span class="sxs-lookup"><span data-stu-id="6eda2-170">In the tree, select 'model\Payments\Currency'.</span></span>
12. <span data-ttu-id="6eda2-171">Smellt er á Bæta reit við</span><span class="sxs-lookup"><span data-stu-id="6eda2-171">Click Add field to.</span></span>
13. <span data-ttu-id="6eda2-172">Smellt er á Flokkaðir reitir</span><span class="sxs-lookup"><span data-stu-id="6eda2-172">Click Grouped fields.</span></span>
14. <span data-ttu-id="6eda2-173">Í trénu veljið 'model\Payments\Instructed Amount(InstructedAmount)'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-173">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
15. <span data-ttu-id="6eda2-174">Smellt er á Bæta reit við</span><span class="sxs-lookup"><span data-stu-id="6eda2-174">Click Add field to.</span></span>
16. <span data-ttu-id="6eda2-175">Smellt er á Uppsöfnunarreitir</span><span class="sxs-lookup"><span data-stu-id="6eda2-175">Click Aggregation fields.</span></span>
17. <span data-ttu-id="6eda2-176">Veljið valkost í svæðinu aðferð.</span><span class="sxs-lookup"><span data-stu-id="6eda2-176">In the Method field, select an option.</span></span>
    * <span data-ttu-id="6eda2-177">Velja samsteypuaðgerðina SAMTÖLU.</span><span class="sxs-lookup"><span data-stu-id="6eda2-177">Select the SUM aggregation function.</span></span>  
18. <span data-ttu-id="6eda2-178">Í reitnum Heiti skal færa inn 'TotalInstructuredAmount'</span><span class="sxs-lookup"><span data-stu-id="6eda2-178">In the Name field, type 'TotalInstructuredAmount'.</span></span>
    * <span data-ttu-id="6eda2-179">TotalInstructuredAmount</span><span class="sxs-lookup"><span data-stu-id="6eda2-179">TotalInstructuredAmount</span></span>  
19. <span data-ttu-id="6eda2-180">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-180">Click Save.</span></span>
20. <span data-ttu-id="6eda2-181">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6eda2-181">Close the page.</span></span>
21. <span data-ttu-id="6eda2-182">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-182">Click OK.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="6eda2-183">Varpa sniðsíhlutum í gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="6eda2-183">Map format components to data sources</span></span>
1. <span data-ttu-id="6eda2-184">Í trénu skal víkka út 'model'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-184">In the tree, expand 'model'.</span></span>
2. <span data-ttu-id="6eda2-185">Í trénu skal víkka út 'model\Payments'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-185">In the tree, expand 'model\Payments'.</span></span>
3. <span data-ttu-id="6eda2-186">Í trénu skal útvíkka 'model\Payments\Initiating Party(InitiatingParty)'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-186">In the tree, expand 'model\Payments\Initiating Party(InitiatingParty)'.</span></span>
4. <span data-ttu-id="6eda2-187">Í trénu skal útvíkka 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-187">In the tree, select 'model\Payments\Initiating Party(InitiatingParty)\Name'.</span></span>
5. <span data-ttu-id="6eda2-188">Í tré skal víkka 'Excel\ReportHeader'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-188">In the tree, expand 'Excel\ReportHeader'.</span></span>
6. <span data-ttu-id="6eda2-189">Í tré skal velja 'Excel\ReportHeader\CompanyName'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-189">In the tree, select 'Excel\ReportHeader\CompanyName'.</span></span>
7. <span data-ttu-id="6eda2-190">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6eda2-190">Click Bind.</span></span>
8. <span data-ttu-id="6eda2-191">Útvíkka 'model\Payments\Creditor', í trénu.</span><span class="sxs-lookup"><span data-stu-id="6eda2-191">In the tree, expand 'model\Payments\Creditor'.</span></span>
9. <span data-ttu-id="6eda2-192">Í trénu skal útvíkka 'model\Payments\Creditor\Identification'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-192">In the tree, expand 'model\Payments\Creditor\Identification'.</span></span>
10. <span data-ttu-id="6eda2-193">Í trénu skal velja 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-193">In the tree, select 'model\Payments\Creditor\Identification\Source ID(SourceID)'.</span></span>
11. <span data-ttu-id="6eda2-194">Í tré skal víkka 'Excel\PaymLines'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-194">In the tree, expand 'Excel\PaymLines'.</span></span>
12. <span data-ttu-id="6eda2-195">Í tré skal velja 'Excel\PaymLines\VendAccountName'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-195">In the tree, select 'Excel\PaymLines\VendAccountName'.</span></span>
13. <span data-ttu-id="6eda2-196">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6eda2-196">Click Bind.</span></span>
14. <span data-ttu-id="6eda2-197">Veljið 'model\Payments\Creditor\Name', í trénu.</span><span class="sxs-lookup"><span data-stu-id="6eda2-197">In the tree, select 'model\Payments\Creditor\Name'.</span></span>
15. <span data-ttu-id="6eda2-198">Í tré skal velja 'Excel\PaymLines\VendName'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-198">In the tree, select 'Excel\PaymLines\VendName'.</span></span>
16. <span data-ttu-id="6eda2-199">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6eda2-199">Click Bind.</span></span>
17. <span data-ttu-id="6eda2-200">Í trénu skal víkka út 'model\Payments\Creditor Agent(CreditorAgent)'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-200">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
18. <span data-ttu-id="6eda2-201">Í trénu skal velja 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-201">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Name'.</span></span>
19. <span data-ttu-id="6eda2-202">Í tré skal velja 'Excel\PaymLines\Bank'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-202">In the tree, select 'Excel\PaymLines\Bank'.</span></span>
20. <span data-ttu-id="6eda2-203">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6eda2-203">Click Bind.</span></span>
21. <span data-ttu-id="6eda2-204">Í trénu skal velja 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-204">In the tree, select 'model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)'.</span></span>
22. <span data-ttu-id="6eda2-205">Í tré skal velja 'Excel\PaymLines\RoutingNumber'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-205">In the tree, select 'Excel\PaymLines\RoutingNumber'.</span></span>
23. <span data-ttu-id="6eda2-206">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6eda2-206">Click Bind.</span></span>
24. <span data-ttu-id="6eda2-207">Í trénu skal víkka út 'model\Payments\Creditor Account(CreditorAccount)'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-207">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
25. <span data-ttu-id="6eda2-208">Í trénu skal víkka út 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-208">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)\Identification'.</span></span>
26. <span data-ttu-id="6eda2-209">Í trénu skal velja 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-209">In the tree, select 'model\Payments\Creditor Account(CreditorAccount)\Identification\Number'.</span></span>
27. <span data-ttu-id="6eda2-210">Í tré skal velja 'Excel\PaymLines\AccountNumber'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-210">In the tree, select 'Excel\PaymLines\AccountNumber'.</span></span>
28. <span data-ttu-id="6eda2-211">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6eda2-211">Click Bind.</span></span>
29. <span data-ttu-id="6eda2-212">Í trénu veljið 'model\Payments\Instructed Amount(InstructedAmount)'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-212">In the tree, select 'model\Payments\Instructed Amount(InstructedAmount)'.</span></span>
30. <span data-ttu-id="6eda2-213">Í tré skal velja 'Excel\PaymLines\Debit'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-213">In the tree, select 'Excel\PaymLines\Debit'.</span></span>
31. <span data-ttu-id="6eda2-214">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6eda2-214">Click Bind.</span></span>
32. <span data-ttu-id="6eda2-215">Útvíkka 'model\Payments\Creditor', í trénu.</span><span class="sxs-lookup"><span data-stu-id="6eda2-215">In the tree, expand 'model\Payments\Creditor'.</span></span>
33. <span data-ttu-id="6eda2-216">Í trénu skal víkka út 'model\Payments\Creditor Account(CreditorAccount)'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-216">In the tree, expand 'model\Payments\Creditor Account(CreditorAccount)'.</span></span>
34. <span data-ttu-id="6eda2-217">Í trénu skal víkka út 'model\Payments\Creditor Agent(CreditorAgent)'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-217">In the tree, expand 'model\Payments\Creditor Agent(CreditorAgent)'.</span></span>
35. <span data-ttu-id="6eda2-218">Veljið 'líkan\greiðslur', í trénu.</span><span class="sxs-lookup"><span data-stu-id="6eda2-218">In the tree, select 'model\Payments\Currency'.</span></span>
36. <span data-ttu-id="6eda2-219">Í tré skal velja 'Excel\PaymLines\Currency'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-219">In the tree, select 'Excel\PaymLines\Currency'.</span></span>
37. <span data-ttu-id="6eda2-220">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6eda2-220">Click Bind.</span></span>
38. <span data-ttu-id="6eda2-221">Í trénu skal víkka út 'PaymentByCurrency'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-221">In the tree, expand 'PaymentByCurrency'.</span></span>
39. <span data-ttu-id="6eda2-222">Í trénu skal víkka út 'PaymentByCurrency\grouped'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-222">In the tree, expand 'PaymentByCurrency\grouped'.</span></span>
40. <span data-ttu-id="6eda2-223">Í trénu skal velja 'PaymentByCurrency\grouped\Currency'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-223">In the tree, select 'PaymentByCurrency\grouped\Currency'.</span></span>
41. <span data-ttu-id="6eda2-224">Í tré skal víkka 'Excel\SummaryLines'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-224">In the tree, expand 'Excel\SummaryLines'.</span></span>
42. <span data-ttu-id="6eda2-225">Í tré skal velja 'Excel\SummaryLines\SummaryCurrency'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-225">In the tree, select 'Excel\SummaryLines\SummaryCurrency'.</span></span>
43. <span data-ttu-id="6eda2-226">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6eda2-226">Click Bind.</span></span>
44. <span data-ttu-id="6eda2-227">Í trénu skal víkka út 'PaymentByCurrency\aggregated'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-227">In the tree, expand 'PaymentByCurrency\aggregated'.</span></span>
45. <span data-ttu-id="6eda2-228">Í trénu skal velja 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-228">In the tree, select 'PaymentByCurrency\aggregated\TotalInstructuredAmount'.</span></span>
46. <span data-ttu-id="6eda2-229">Í tré skal velja 'Excel\SummaryLines\SummaryAmount'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-229">In the tree, select 'Excel\SummaryLines\SummaryAmount'.</span></span>
47. <span data-ttu-id="6eda2-230">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6eda2-230">Click Bind.</span></span>
48. <span data-ttu-id="6eda2-231">Í trénu skal velja 'PaymentByCurrency'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-231">In the tree, select 'PaymentByCurrency'.</span></span>
49. <span data-ttu-id="6eda2-232">Í tré skal velja 'Excel\SummaryLines'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-232">In the tree, select 'Excel\SummaryLines'.</span></span>
50. <span data-ttu-id="6eda2-233">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6eda2-233">Click Bind.</span></span>
51. <span data-ttu-id="6eda2-234">Veljið 'model\Payments', í trénu.</span><span class="sxs-lookup"><span data-stu-id="6eda2-234">In the tree, select 'model\Payments'.</span></span>
52. <span data-ttu-id="6eda2-235">Í tré skal velja 'Excel\PaymLines'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-235">In the tree, select 'Excel\PaymLines'.</span></span>
53. <span data-ttu-id="6eda2-236">Smelltu á Binda.</span><span class="sxs-lookup"><span data-stu-id="6eda2-236">Click Bind.</span></span>
54. <span data-ttu-id="6eda2-237">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-237">Click Save.</span></span>
55. <span data-ttu-id="6eda2-238">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6eda2-238">Close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="6eda2-239">Nota stofnaða grunnstillingu fyrir greiðsluvinnslu</span><span class="sxs-lookup"><span data-stu-id="6eda2-239">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="6eda2-240">Smellið á „Breyta stöðu“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-240">Click Change status.</span></span>
2. <span data-ttu-id="6eda2-241">Smelltu á Ljúka.</span><span class="sxs-lookup"><span data-stu-id="6eda2-241">Click Complete.</span></span>
3. <span data-ttu-id="6eda2-242">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-242">Click OK.</span></span>
4. <span data-ttu-id="6eda2-243">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6eda2-243">Close the page.</span></span>
5. <span data-ttu-id="6eda2-244">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6eda2-244">Close the page.</span></span>
6. <span data-ttu-id="6eda2-245">Fara í Viðskiptakröfur > Greiðsluuppsetning > Greiðsluhættir.</span><span class="sxs-lookup"><span data-stu-id="6eda2-245">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
7. <span data-ttu-id="6eda2-246">Nota flýtiafmörkun til að sía í svæði Greiðsluháttur með gildinu „Rafrænt“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-246">Use the Quick Filter to filter on the Method of payment field with a value of 'Electronic'.</span></span>
    * <span data-ttu-id="6eda2-247">Rafrænt</span><span class="sxs-lookup"><span data-stu-id="6eda2-247">Electronic</span></span>  
8. <span data-ttu-id="6eda2-248">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-248">Click Edit.</span></span>
9. <span data-ttu-id="6eda2-249">Útvíkka hlutann Skráarsnið.</span><span class="sxs-lookup"><span data-stu-id="6eda2-249">Expand the File formats section.</span></span>
10. <span data-ttu-id="6eda2-250">Velja skal Já í Almennan rafræna skýrslugerð svæði.</span><span class="sxs-lookup"><span data-stu-id="6eda2-250">Select Yes in the Generic electronic reporting field.</span></span>
11. <span data-ttu-id="6eda2-251">Færa inn eða velja gildi í reitnum skilgreiningu útflutningssniðs.</span><span class="sxs-lookup"><span data-stu-id="6eda2-251">In the Export format configuration field, enter or select a value.</span></span>
    * <span data-ttu-id="6eda2-252">Veljið skilgreininguna 'Dæmi um vinnublaðsskýrslu'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-252">Select the ‘Sample worksheet report’ configuration.</span></span>  
12. <span data-ttu-id="6eda2-253">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-253">Click Save.</span></span>
13. <span data-ttu-id="6eda2-254">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="6eda2-254">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="6eda2-255">Nota stofnaða skilgreiningu fyrir prófun á vinnslu greiðslubóka</span><span class="sxs-lookup"><span data-stu-id="6eda2-255">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="6eda2-256">Fara í Viðskiptaskuldir > Greiðslur > Greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="6eda2-256">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="6eda2-257">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-257">Click New.</span></span>
    * <span data-ttu-id="6eda2-258">Stofna nýja greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="6eda2-258">Create a new payment journal.</span></span>  
3. <span data-ttu-id="6eda2-259">Í svæðið Heiti skal slá inn ‚VendPay'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-259">In the Name field, type 'VendPay'.</span></span>
    * <span data-ttu-id="6eda2-260">VendPay</span><span class="sxs-lookup"><span data-stu-id="6eda2-260">VendPay</span></span>  
4. <span data-ttu-id="6eda2-261">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-261">Click Lines.</span></span>
5. <span data-ttu-id="6eda2-262">Í svæðinu lykill, skal tilgreina gildi 'GB_SI_000001'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-262">In the Account field, specify the values 'GB_SI_000001'.</span></span>
    * <span data-ttu-id="6eda2-263">GB_SI_000001</span><span class="sxs-lookup"><span data-stu-id="6eda2-263">GB_SI_000001</span></span>  
6. <span data-ttu-id="6eda2-264">Stilla debet á '1000'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-264">Set Debit to '1000'.</span></span>
7. <span data-ttu-id="6eda2-265">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-265">Click New.</span></span>
8. <span data-ttu-id="6eda2-266">Í svæðinu lykill, skal tilgreina gildi 'GB_SI_000005'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-266">In the Account field, specify the values 'GB_SI_000005'.</span></span>
    * <span data-ttu-id="6eda2-267">GB_SI_000005</span><span class="sxs-lookup"><span data-stu-id="6eda2-267">GB_SI_000005</span></span>  
9. <span data-ttu-id="6eda2-268">Stilla debet á '2000'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-268">Set Debit to '2000'.</span></span>
10. <span data-ttu-id="6eda2-269">Í reitinn gjaldmiðill skal slá inn EUR.</span><span class="sxs-lookup"><span data-stu-id="6eda2-269">In the Currency field, type 'EUR'.</span></span>
    * <span data-ttu-id="6eda2-270">EUR</span><span class="sxs-lookup"><span data-stu-id="6eda2-270">EUR</span></span>  
11. <span data-ttu-id="6eda2-271">Í reitinn Mótlykill skal tilgreina gildin ''GBSI OPER'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-271">In the Offset account field, specify the values 'GBSI OPER'.</span></span>
    * <span data-ttu-id="6eda2-272">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="6eda2-272">GBSI OPER</span></span>  
12. <span data-ttu-id="6eda2-273">Í reitnum Greiðsluháttur skal slá inn 'Rafrænt'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-273">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="6eda2-274">Rafrænt</span><span class="sxs-lookup"><span data-stu-id="6eda2-274">Electronic</span></span>  
13. <span data-ttu-id="6eda2-275">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-275">Click Save.</span></span>
14. <span data-ttu-id="6eda2-276">Smelltu á Mynda greiðslur.</span><span class="sxs-lookup"><span data-stu-id="6eda2-276">Click Generate payments.</span></span>
15. <span data-ttu-id="6eda2-277">Í reitnum Greiðsluháttur skal slá inn 'Rafrænt'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-277">In the Method of payment field, type 'Electronic'.</span></span>
    * <span data-ttu-id="6eda2-278">Rafrænt</span><span class="sxs-lookup"><span data-stu-id="6eda2-278">Electronic</span></span>  
16. <span data-ttu-id="6eda2-279">Í svæði Skráarheiti skal slá inn „Greiðslur“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-279">In the File name field, type 'Payments'.</span></span>
    * <span data-ttu-id="6eda2-280">Til dæmis, skráið greiðslur.</span><span class="sxs-lookup"><span data-stu-id="6eda2-280">For example, type Payments.</span></span>  
17. <span data-ttu-id="6eda2-281">Í reitinn Bankareikningar skal slá inn 'GBSI OPER'.</span><span class="sxs-lookup"><span data-stu-id="6eda2-281">In the Bank account field, type 'GBSI OPER'.</span></span>
    * <span data-ttu-id="6eda2-282">GBSI OPER</span><span class="sxs-lookup"><span data-stu-id="6eda2-282">GBSI OPER</span></span>  
18. <span data-ttu-id="6eda2-283">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-283">Click OK.</span></span>
19. <span data-ttu-id="6eda2-284">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="6eda2-284">Click OK.</span></span>
    * <span data-ttu-id="6eda2-285">Fara yfir stofnaðar vinnublað, þar á meðal upplýsingar um greiðslulínur ásamt samtölur fyrir hvern gjaldmiðilskóði sem notaður er í þessum greiðsluskilaboðum.</span><span class="sxs-lookup"><span data-stu-id="6eda2-285">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  


