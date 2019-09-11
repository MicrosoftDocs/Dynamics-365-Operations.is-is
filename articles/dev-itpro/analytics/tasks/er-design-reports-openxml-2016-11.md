---
title: Rafræn skýrslugerð Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði (nóvember 2016)
description: Þetta efni útskýrir hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað nýja skilgreiningarveitu fyrir rafræna skýrslugerð (ER) sem inniheldur snið til að mynda rafræn skjöl í OPENXML-sniði.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport,  ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERModelGroupByFunctionEditor, VendPaymMode, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1229c89f43f9ded955dadf2f4d87825c9ab4e71
ms.sourcegitcommit: e552111e148a80544a3468da60ea0464f02a658d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/15/2019
ms.locfileid: "1875273"
---
# <a name="er-design-a-configuration-for-generating-reports-in-openxml-format-november-2016"></a><span data-ttu-id="03dd5-103">Rafræn skýrslugerð Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði (nóvember 2016)</span><span class="sxs-lookup"><span data-stu-id="03dd5-103">ER Design a configuration for generating reports in OPENXML format (November 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="03dd5-104">Þetta efni útskýrir hvernig notandi í hlutverki Kerfisstjóra eða Þróunaraðila rafrænnar skýrslulausnar getur stofnað nýja skilgreiningarveitu fyrir rafræna skýrslugerð (ER) sem inniheldur snið til að mynda rafræn skjöl í OPENXML-sniði.</span><span class="sxs-lookup"><span data-stu-id="03dd5-104">This topic explains how a user in the System Administrator or Electronic Reporting Developer role can create a new Electronic reporting (ER) configuration that contains a template for generating electronic documents in OPENXML format.</span></span> <span data-ttu-id="03dd5-105">Þessi skilgreining verður notuð til að vinna greiðslur lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="03dd5-105">This configuration will be used for processing vendor payments.</span></span>

<span data-ttu-id="03dd5-106">Í þessu dæmi, verður að stofna skilgreiningu fyrir dæmi um fyrirtæki, Litware, Inc. Þessi skref má framkvæma í GBSI fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="03dd5-106">In this example, you will create a configuration for sample company, Litware, Inc. These steps can be performed in GBSI company.</span></span>

<span data-ttu-id="03dd5-107">Til að ljúka þessum skrefum verður fyrst að ljúka við skrefin í ferlinu "Stofna skilgreiningarveitu og merkja hana sem virka".</span><span class="sxs-lookup"><span data-stu-id="03dd5-107">To complete these steps, you must first complete the steps in the “Create a configuration provider and mark it as active” procedure.</span></span> <span data-ttu-id="03dd5-108">Einnig verður að hafa Excel-skráin sem verður flutt inn þegar sniðmátið er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="03dd5-108">You must also have an Excel file which will be imported when creating the template.</span></span> <span data-ttu-id="03dd5-109">Hægt er að fá aðgang að þessari skrá í [Sniðmát greiðsluskýrslu](https://go.microsoft.com/fwlink/?linkid=862266).</span><span class="sxs-lookup"><span data-stu-id="03dd5-109">This file can be accessed from the [Template of Payment Report](https://go.microsoft.com/fwlink/?linkid=862266).</span></span>


## <a name="upload-the-payments-data-model-configuration"></a><span data-ttu-id="03dd5-110">Hlaða upp skilgreiningu greiðslugagnalíkans.</span><span class="sxs-lookup"><span data-stu-id="03dd5-110">Upload the Payments data model configuration</span></span>
1. <span data-ttu-id="03dd5-111">Farðu í **Einingar > Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-111">In the navigation pane, go to **Modules > Organization administration > Workspaces > Electronic reporting**.</span></span>
2. <span data-ttu-id="03dd5-112">Í listanum merkirðu skilgreiningarveitu fyrir dæmi um fyrirtæki, veljið Litware, Inc. Ef þessi skilgreiningarveita sést ekki verður fyrst að ljúka við skrefin í [Stofna skilgreiningarveitu og merkja hana sem virka](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="03dd5-112">In the list, mark the configuration provider for sample company, Litware, Inc. If you don’t see this configuration provider, you must first complete the steps in [Create a configuration provider and mark it as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="03dd5-113">Veldu **Stilla sem virkt**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-113">Select **Set active**.</span></span>
4. <span data-ttu-id="03dd5-114">Veldu **Geymslur**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-114">Select **Repositories**.</span></span> <span data-ttu-id="03dd5-115">Velja gagnasafn fyrir gerðina Rekstrartilföng, ef tiltækur.</span><span class="sxs-lookup"><span data-stu-id="03dd5-115">Select a repository for the Operations Resources type, if available.</span></span> <span data-ttu-id="03dd5-116">Ef hennar er tiltæk, sleppa eftirfarandi skref um stofnun nýja gagnasafns.</span><span class="sxs-lookup"><span data-stu-id="03dd5-116">If its available, skip the following steps about creating a new repository.</span></span>  
5. <span data-ttu-id="03dd5-117">Veldu **Bæta við** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="03dd5-117">Select **Add** to open the drop dialog.</span></span>
6. <span data-ttu-id="03dd5-118">Í reitnum **Gerð geymslu fyrir grunnstillingar**, færirðu inn `Operations resourcesdd`.</span><span class="sxs-lookup"><span data-stu-id="03dd5-118">In the **Configuration repository type** field, enter `Operations resourcesdd`.</span></span>
7. <span data-ttu-id="03dd5-119">Veljið **Stofna geymslu**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-119">Select **Create repository**.</span></span>
8. <span data-ttu-id="03dd5-120">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-120">Select **OK**.</span></span>
9. <span data-ttu-id="03dd5-121">Veljið **Opna**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-121">Select **Open**.</span></span>
10. <span data-ttu-id="03dd5-122">Í trénu skal velja **Greiðslulíkan**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-122">In the tree, select **Payment model**.</span></span>
11. <span data-ttu-id="03dd5-123">Velja **Innflutningur**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-123">Select **Import**.</span></span> <span data-ttu-id="03dd5-124">Flytja inn þetta gagnalíkan.</span><span class="sxs-lookup"><span data-stu-id="03dd5-124">Import this data model.</span></span> <span data-ttu-id="03dd5-125">Það verður notað sem gagnagjafi í nýja skilgreiningu sniðs.</span><span class="sxs-lookup"><span data-stu-id="03dd5-125">It will be used as a data source in a new format configuration.</span></span> <span data-ttu-id="03dd5-126">Sleppa þessu þrepi ef skilgreiningin hefur þegar verið flutt.</span><span class="sxs-lookup"><span data-stu-id="03dd5-126">Skip this step if this configuration has been already imported.</span></span>  
12. <span data-ttu-id="03dd5-127">Velja skal **Já**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-127">Select **Yes**.</span></span>
13. <span data-ttu-id="03dd5-128">Lokaðu síðunum þar til þú kemur aftur á rafrænu skýrslusíðuna.</span><span class="sxs-lookup"><span data-stu-id="03dd5-128">Close the pages until you return to the Electronic reporting page.</span></span>

## <a name="create-a-new-format-configuration"></a><span data-ttu-id="03dd5-129">Stofna nýja skilgreiningu á sniði</span><span class="sxs-lookup"><span data-stu-id="03dd5-129">Create a new format configuration</span></span>
1. <span data-ttu-id="03dd5-130">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-130">Select **Reporting configurations**.</span></span>
2. <span data-ttu-id="03dd5-131">Í trénu skal velja **Greiðslulíkan**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-131">In the tree, select **Payment model**.</span></span>
3. <span data-ttu-id="03dd5-132">Veldu **Stofna skilgreiningu** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="03dd5-132">Select **Create configuration** to open the drop dialog.</span></span>
4. <span data-ttu-id="03dd5-133">Í reitinn **Nýtt** skal slá inn `Format based on data model PaymentModel`.</span><span class="sxs-lookup"><span data-stu-id="03dd5-133">In the **New** field, enter `Format based on data model PaymentModel`.</span></span> <span data-ttu-id="03dd5-134">Stofna snið sem byggir á gagnalíkani PaymentModel.</span><span class="sxs-lookup"><span data-stu-id="03dd5-134">Create a format that is based on the PaymentModel data model.</span></span>
5. <span data-ttu-id="03dd5-135">Í reitinn **Heiti** skaltu færa inn `Sample worksheet report`.</span><span class="sxs-lookup"><span data-stu-id="03dd5-135">In the **Name** field, type `Sample worksheet report`.</span></span> <span data-ttu-id="03dd5-136">Dæmi um vinnublaðsskýrslu</span><span class="sxs-lookup"><span data-stu-id="03dd5-136">Sample worksheet report</span></span>  
6. <span data-ttu-id="03dd5-137">Á svæðinu **Lýsing** skal færa inn `Sample worksheet report for vendors’ payments`.</span><span class="sxs-lookup"><span data-stu-id="03dd5-137">In the **Description** field, type `Sample worksheet report for vendors’ payments`.</span></span> <span data-ttu-id="03dd5-138">Dæmi um vinnublaðsskýrslu fyrir greiðslur lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="03dd5-138">Sample worksheet report for vendors’ payments.</span></span>  
7. <span data-ttu-id="03dd5-139">Í svæðinu **Skilgreining gagnalíkans** skal færa inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="03dd5-139">In the **Data model definition** field, enter or select a value.</span></span> <span data-ttu-id="03dd5-140">Veljið skilgreininguna **CustomerCreditTransferInitiation**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-140">Select the **CustomerCreditTransferInitiation** definition.</span></span>  
8. <span data-ttu-id="03dd5-141">Veljið **Stofna skilgreiningu**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-141">Select **Create configuration**.</span></span>

## <a name="design-a-new-document-in-openxml-worksheet-format"></a><span data-ttu-id="03dd5-142">Hanna nýtt skjal í sniði OPENXML vinnublaði</span><span class="sxs-lookup"><span data-stu-id="03dd5-142">Design a new document in OPENXML worksheet format</span></span>
1. <span data-ttu-id="03dd5-143">Í trénu skal velja **greiðslulíkan\dæmi um vinnublaðsskýrslu**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-143">In the tree, select **Payment model\Sample worksheet report**.</span></span>
2. <span data-ttu-id="03dd5-144">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-144">Select **Designer**.</span></span>
3. <span data-ttu-id="03dd5-145">Á Aðgerðasvæðinu skal velja **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-145">On the Action Pane, select **Import**.</span></span>
4. <span data-ttu-id="03dd5-146">Veldu **Flytja inn úr Excel**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-146">Select **Import from Excel**.</span></span>
5. <span data-ttu-id="03dd5-147">Veldu **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-147">Select **Attachments**.</span></span> <span data-ttu-id="03dd5-148">Tengja fyrirliggjandi Excel-skjalið sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="03dd5-148">Attach the existing Excel document as a template.</span></span>  
6. <span data-ttu-id="03dd5-149">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-149">Select **New**.</span></span>
7. <span data-ttu-id="03dd5-150">Veldu **Skrá**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-150">Select **File**.</span></span> <span data-ttu-id="03dd5-151">Benda á fyrirliggjandi Excel-skrá.</span><span class="sxs-lookup"><span data-stu-id="03dd5-151">Point to the existing Excel file.</span></span>  
8. <span data-ttu-id="03dd5-152">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="03dd5-152">Close the page.</span></span>
9. <span data-ttu-id="03dd5-153">Sláið inn eða veldu gildi í reitnum **sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-153">In the **Template** field, enter or select a value.</span></span> <span data-ttu-id="03dd5-154">Veljið viðhengda Excel-skráin sem nota á sem sniðmát.</span><span class="sxs-lookup"><span data-stu-id="03dd5-154">Select the attached Excel file to be used as a template.</span></span>  
10. <span data-ttu-id="03dd5-155">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-155">Select **OK**.</span></span> <span data-ttu-id="03dd5-156">Athugið að sniðshlutar Rafræn skýrslugerð hafa verið stofnað í hönnunarsniði sem byggir á uppbygging MS Excel-skjals sem vísað er úr (nefnd svið).</span><span class="sxs-lookup"><span data-stu-id="03dd5-156">Note that ER format components have been created in the designing format based on the structure of the referring MS Excel document (named ranges).</span></span>  

## <a name="create-a-new-data-source-to-calculate-totals-by-currency-codes"></a><span data-ttu-id="03dd5-157">Stofna nýja gagnagjafa til að reikna samtölur eftir gjaldmiðilskóða</span><span class="sxs-lookup"><span data-stu-id="03dd5-157">Create a new data source to calculate totals by currency codes</span></span>
1. <span data-ttu-id="03dd5-158">Veldu flipann **Vörpun**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-158">Select the **Mapping** tab.</span></span>
2. <span data-ttu-id="03dd5-159">Veldu **Bæta við rót** til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="03dd5-159">Select **Add root** to open the drop dialog.</span></span>
3. <span data-ttu-id="03dd5-160">Í trénu skal velja **virkni\Flokka eftir**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-160">In the tree, select **Functions\Group by**.</span></span>
4. <span data-ttu-id="03dd5-161">Í reitinn **Heiti** skaltu færa inn `PaymentByCurrency`.</span><span class="sxs-lookup"><span data-stu-id="03dd5-161">In the **Name** field, type `PaymentByCurrency`.</span></span>
5. <span data-ttu-id="03dd5-162">Veldu **Breyta hópi eftir**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-162">Select **Edit group by**.</span></span>
6. <span data-ttu-id="03dd5-163">Stækkaðu í trénu **tegund**, veldu síðan **líkan\Greiðslur**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-163">In the tree, expand **model**, then select **model\Payments**.</span></span>
7. <span data-ttu-id="03dd5-164">Veldu **Bæta reit við**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-164">Select **Add field to**.</span></span>
8. <span data-ttu-id="03dd5-165">Veldu **Hvað skal flokka**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-165">Select **What to group**.</span></span>
9. <span data-ttu-id="03dd5-166">Stækkaðu í trénu **líkan\Greiðslur**, veldu síðan **líkan\Greiðslur\Gjaldmiðill**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-166">In the tree, expand **model\Payments**, then select **model\Payments\Currency**.</span></span>
10. <span data-ttu-id="03dd5-167">Veldu **Bæta reit við**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-167">Select **Add field to**.</span></span>
11. <span data-ttu-id="03dd5-168">Veldu **Flokkaðir reitir**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-168">Select **Grouped fields**.</span></span>
12. <span data-ttu-id="03dd5-169">Í trénu veljið **model\Payments\Instructed Amount(InstructedAmount)**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-169">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)**.</span></span>
13. <span data-ttu-id="03dd5-170">Veldu **Bæta reit við**, veldu síðan **Uppsöfnunarsvið**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-170">Select **Add field to**, then select **Aggregation fields**.</span></span>
14. <span data-ttu-id="03dd5-171">Veljið valkost í retinum **aðferð**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-171">In the **Method** field, select an option.</span></span> <span data-ttu-id="03dd5-172">Velja aðgerðina **Uppsöfnuð SAMTALA**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-172">Select the **SUM aggregation** function.</span></span>  
15. <span data-ttu-id="03dd5-173">Í reitinn **Heiti** skaltu færa inn `TotalInstructuredAmount`.</span><span class="sxs-lookup"><span data-stu-id="03dd5-173">In the **Name** field, type `TotalInstructuredAmount`.</span></span>
16. <span data-ttu-id="03dd5-174">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-174">Select **Save**.</span></span>
17. <span data-ttu-id="03dd5-175">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="03dd5-175">Close the page.</span></span>
18. <span data-ttu-id="03dd5-176">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-176">Select **OK**.</span></span>

## <a name="map-format-components-to-data-sources"></a><span data-ttu-id="03dd5-177">Varpa sniðsíhlutum í gagnagjafa</span><span class="sxs-lookup"><span data-stu-id="03dd5-177">Map format components to data sources</span></span>
1. <span data-ttu-id="03dd5-178">Í trénu skal útvíkka **model\Payments\Initiating Party(InitiatingParty)\Name** og **Excel\ReportHeader\CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-178">In the tree, select **model\Payments\Initiating Party(InitiatingParty)\Name** and **Excel\ReportHeader\CompanyName**.</span></span>
2. <span data-ttu-id="03dd5-179">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-179">Select **Bind**.</span></span>
3. <span data-ttu-id="03dd5-180">Í trénu skal velja **model\Payments\Creditor\Identification\Source ID(SourceID)** og **Excel\PaymLines\VendAccountName**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-180">In the tree, select **model\Payments\Creditor\Identification\Source ID(SourceID)** and **Excel\PaymLines\VendAccountName**.</span></span>
4. <span data-ttu-id="03dd5-181">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-181">Select **Bind**.</span></span>
5. <span data-ttu-id="03dd5-182">Veldu í trénu **model\Payments\Creditor\Name** og **Excel\PaymLines\VendName**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-182">In the tree, select **model\Payments\Creditor\Name** and **Excel\PaymLines\VendName**.</span></span>
6. <span data-ttu-id="03dd5-183">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-183">Select **Bind**.</span></span>
7. <span data-ttu-id="03dd5-184">Veldu í trénu **model\Payments\Creditor Agent(CreditorAgent)\Name** og **Excel\PaymLines\Bank**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-184">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Name** and **Excel\PaymLines\Bank**.</span></span>
8. <span data-ttu-id="03dd5-185">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-185">Select **Bind**.</span></span>
9. <span data-ttu-id="03dd5-186">Veldu í trénu **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** og **Excel\PaymLines\RoutingNumber**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-186">In the tree, select **model\Payments\Creditor Agent(CreditorAgent)\Routing Number(RoutingNumber)** and **Excel\PaymLines\RoutingNumber**.</span></span>
10. <span data-ttu-id="03dd5-187">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-187">Select **Bind**.</span></span>
11. <span data-ttu-id="03dd5-188">Veldu í trénu **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** og **Excel\PaymLines\AccountNumber**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-188">In the tree, select **model\Payments\Creditor Account(CreditorAccount)\Identification\Number** and **Excel\PaymLines\AccountNumber**.</span></span>
12. <span data-ttu-id="03dd5-189">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-189">Select **Bind**.</span></span>
13. <span data-ttu-id="03dd5-190">Veldu í trénu **model\Payments\Instructed Amount(InstructedAmount)** og **Excel\PaymLines\Debit**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-190">In the tree, select **model\Payments\Instructed Amount(InstructedAmount)** and **Excel\PaymLines\Debit**.</span></span>
14. <span data-ttu-id="03dd5-191">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-191">Select **Bind**.</span></span>
15. <span data-ttu-id="03dd5-192">Veldu í trénu **model\Payments\Currency** og **Excel\PaymLines\Currency**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-192">In the tree, select **model\Payments\Currency** and **Excel\PaymLines\Currency**.</span></span>
16. <span data-ttu-id="03dd5-193">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-193">Select **Bind**.</span></span>
17. <span data-ttu-id="03dd5-194">Veldu í trénu **PaymentByCurrency\grouped\Currency** og **Excel\SummaryLines\SummaryCurrency**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-194">In the tree, select **PaymentByCurrency\grouped\Currency** and **Excel\SummaryLines\SummaryCurrency**.</span></span>
18. <span data-ttu-id="03dd5-195">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-195">Select **Bind**.</span></span>
19. <span data-ttu-id="03dd5-196">Veldu í trénu **PaymentByCurrency\aggregated\TotalInstructuredAmount** og **Excel\SummaryLines\SummaryAmount**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-196">In the tree, select **PaymentByCurrency\aggregated\TotalInstructuredAmount** and **Excel\SummaryLines\SummaryAmount**.</span></span>
20. <span data-ttu-id="03dd5-197">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-197">Select **Bind**.</span></span>
21. <span data-ttu-id="03dd5-198">Í trénu velurðu **PaymentByCurrency** og **Excel\SummaryLines**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-198">In the tree, select **PaymentByCurrency** and **Excel\SummaryLines**.</span></span>
22. <span data-ttu-id="03dd5-199">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-199">Select **Bind**.</span></span>
23. <span data-ttu-id="03dd5-200">Í trénu velurðu **model\Payments** og **Excel\PaymLines**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-200">In the tree, select **model\Payments** and **Excel\PaymLines**.</span></span>
24. <span data-ttu-id="03dd5-201">Veldu **Binda**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-201">Select **Bind**.</span></span>
25. <span data-ttu-id="03dd5-202">Veljið **Vista** og lokið síðan síðunni.</span><span class="sxs-lookup"><span data-stu-id="03dd5-202">Select **Save**, then close the page.</span></span>

## <a name="use-the-created-configuration-for-payments-processing"></a><span data-ttu-id="03dd5-203">Nota stofnaða grunnstillingu fyrir greiðsluvinnslu</span><span class="sxs-lookup"><span data-stu-id="03dd5-203">Use the created configuration for payments processing</span></span>
1. <span data-ttu-id="03dd5-204">Veljið **Breyta stöðu**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-204">Select **Change status**.</span></span>
2. <span data-ttu-id="03dd5-205">Velja **Lokið**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-205">Select **Complete**.</span></span>
3. <span data-ttu-id="03dd5-206">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-206">Select **OK**.</span></span>
4. <span data-ttu-id="03dd5-207">Í skoðunarrúðunni ferðu í **Kerfi > Viðskiptaskuldir > Greiðsluuppsetning > Greiðsluhættir**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-207">In the navigation pane, go to **Modules > Accounts payable > Payment setup > Methods of payment**.</span></span>
5. <span data-ttu-id="03dd5-208">Nota flýtiafmörkun til að sía í svæði **Greiðsluháttur** með gildinu **Rafrænt**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-208">Use the Quick Filter to filter on the **Method of payment** field with a value of **Electronic**.</span></span>
6. <span data-ttu-id="03dd5-209">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-209">Select **Edit**.</span></span>
7. <span data-ttu-id="03dd5-210">Útvíkkaðu hlutann **Skráarsnið**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-210">Expand the **File formats** section.</span></span>
8. <span data-ttu-id="03dd5-211">Velja skal **Já** í reitnum **Almenn rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-211">Select **Yes** in the **Generic electronic reporting** field.</span></span>
9. <span data-ttu-id="03dd5-212">Færa inn eða velja gildi í reitnum **Skilgreining útflutningssniðs**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-212">In the **Export format configuration** field, enter or select a value.</span></span> <span data-ttu-id="03dd5-213">Veljið skilgreininguna **Dæmi um vinnublaðsskýrslu**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-213">Select the **Sample worksheet report** configuration.</span></span>  
10. <span data-ttu-id="03dd5-214">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-214">Select **Save**.</span></span>
11. <span data-ttu-id="03dd5-215">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="03dd5-215">Close the page.</span></span>

## <a name="use-the-created-configuration-for-testing-of-payment-journals-processing"></a><span data-ttu-id="03dd5-216">Nota stofnaða skilgreiningu fyrir prófun á vinnslu greiðslubóka</span><span class="sxs-lookup"><span data-stu-id="03dd5-216">Use the created configuration for testing of payment journals processing</span></span>
1. <span data-ttu-id="03dd5-217">Í skoðunarrúðunni ferðu í **Einingar > Viðskiptaskuldir > Greiðslur > Greiðslubók**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-217">In the navigation pane, go to **Modules > Accounts payable > Payments > Payment journal**.</span></span>
2. <span data-ttu-id="03dd5-218">Veldu **Nýr** til að stofna nýja greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="03dd5-218">Select **New** to create a new payment journal.</span></span>
3. <span data-ttu-id="03dd5-219">Í svæðið **Heiti** skal slá inn **VendPay**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-219">In the **Name** field, type **VendPay**.</span></span>
4. <span data-ttu-id="03dd5-220">Veldu **Línur**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-220">Select **Lines**.</span></span>
5. <span data-ttu-id="03dd5-221">Í reitnum **Lykill** skal færa inn gildin `GB_SI_000001`.</span><span class="sxs-lookup"><span data-stu-id="03dd5-221">In the **Account** field, specify the values `GB_SI_000001`.</span></span>
6. <span data-ttu-id="03dd5-222">Stilltu **Debet** á `1000`.</span><span class="sxs-lookup"><span data-stu-id="03dd5-222">Set **Debit** to `1000`.</span></span>
7. <span data-ttu-id="03dd5-223">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-223">Select **New**.</span></span>
8. <span data-ttu-id="03dd5-224">Í reitnum **Lykill** skal færa inn gildin `GB_SI_000005`.</span><span class="sxs-lookup"><span data-stu-id="03dd5-224">In the **Account** field, specify the values `GB_SI_000005`.</span></span>
9. <span data-ttu-id="03dd5-225">Stilltu **Debet** á `2000`.</span><span class="sxs-lookup"><span data-stu-id="03dd5-225">Set **Debit** to `2000`.</span></span>
10. <span data-ttu-id="03dd5-226">Í reitinn **Gjaldmiðill** skal slá inn `EUR`.</span><span class="sxs-lookup"><span data-stu-id="03dd5-226">In the **Currency** field, type `EUR`.</span></span>
11. <span data-ttu-id="03dd5-227">Í reitinn **Mótlykill** skal tilgreina gildin `GBSI OPER`.</span><span class="sxs-lookup"><span data-stu-id="03dd5-227">In the **Offset account** field, specify the values `GBSI OPER`.</span></span>
12. <span data-ttu-id="03dd5-228">Í reitnum **Greiðsluháttur** skal slá inn `Electronic`.</span><span class="sxs-lookup"><span data-stu-id="03dd5-228">In the **Method of payment** field, type `Electronic`.</span></span>
13. <span data-ttu-id="03dd5-229">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-229">Select **Save**.</span></span>
14. <span data-ttu-id="03dd5-230">Veldu **Búa til greiðslur**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-230">Select **Generate payments**.</span></span>
15. <span data-ttu-id="03dd5-231">Í reitnum **Greiðsluháttur** skal slá inn `Electronic`.</span><span class="sxs-lookup"><span data-stu-id="03dd5-231">In the **Method of payment** field, type `Electronic`.</span></span>
16. <span data-ttu-id="03dd5-232">Í reitnum **Heiti skrár** færðu inn `Payments`.</span><span class="sxs-lookup"><span data-stu-id="03dd5-232">In the **File name** field, type `Payments`.</span></span>
17. <span data-ttu-id="03dd5-233">Í reitinn **Bankareikningar** skal slá inn `GBSI OPER`.</span><span class="sxs-lookup"><span data-stu-id="03dd5-233">In the **Bank account** field, type `GBSI OPER`.</span></span>
18. <span data-ttu-id="03dd5-234">Veldu **Í lagi** og síðan aftur **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="03dd5-234">Select **OK**, then select **OK** again.</span></span> <span data-ttu-id="03dd5-235">Fara yfir stofnaðar vinnublað, þar á meðal upplýsingar um greiðslulínur ásamt samtölur fyrir hvern gjaldmiðilskóði sem notaður er í þessum greiðsluskilaboðum.</span><span class="sxs-lookup"><span data-stu-id="03dd5-235">Review the created worksheet, including details of payment lines as well as totals for each currency code used in this payment message.</span></span>  

