---
title: Hanna grunnstillingar rafrænnar skýrslugerðar til að búa til skýrslur á Word-sniði
description: Eftirfarandi skref útskýra hvernig notandi í annaðhvort hlutverk kerfisstjóri eða þróunaraðili rafræn skýrslugerð getur grunnstilla snið rafræn skýrslugerð til að mynda skýrslur sem skjöl í Microsoft Word.
author: NickSelin
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 327f03435ab55551953fd998dd89c831c76c4c26
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182601"
---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a><span data-ttu-id="b3c98-103">Hanna grunnstillingar rafrænnar skýrslugerðar til að búa til skýrslur á Word-sniði</span><span class="sxs-lookup"><span data-stu-id="b3c98-103">Design ER configurations to generate reports in Word format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b3c98-104">Eftirfarandi skref útskýra hvernig notandi í annaðhvort hlutverk kerfisstjóri eða þróunaraðili rafræn skýrslugerð getur grunnstilla snið rafræn skýrslugerð (ER) til að mynda skýrslur sem skjöl í Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="b3c98-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="b3c98-105">Hægt er að framkvæma þessum skrefum í GBSI fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="b3c98-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="b3c98-106">Til að ljúka þessum skrefum verður fyrst að ljúka við skref í verkefnaleiðbeiningar „Búa til grunnstilling Rafræn skýrslugerð til að mynda skýrslur í OPENXML-snið“.</span><span class="sxs-lookup"><span data-stu-id="b3c98-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="b3c98-107">Fyrirfram verður líka að hlaða niður og vista eftirfarandi sniðmát staðbundið fyrir sýnishorn skýrslu:</span><span class="sxs-lookup"><span data-stu-id="b3c98-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

- [<span data-ttu-id="b3c98-108">Sniðmát greiðsluskýrslu</span><span class="sxs-lookup"><span data-stu-id="b3c98-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="b3c98-109">Afmarkað sniðmát greiðsluskýrslu</span><span class="sxs-lookup"><span data-stu-id="b3c98-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)


<span data-ttu-id="b3c98-110">Þetta ferli er fyrir eiginleika sem var bætt við í Microsoft Dynamics 365 for Operations, útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="b3c98-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="b3c98-111">Velja fyrirliggjandi grunnstilling skýrsla í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="b3c98-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="b3c98-112">Í **Skoðunarrúðunni ferðu í Einingar > Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-112">In the **Navigation pane, go to Modules > Organization administration > Workspaces > Electronic reporting**.</span></span> <span data-ttu-id="b3c98-113">Gakktu úr skugga um að veitandi grunnstillingar „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="b3c98-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="b3c98-114">sé merkt sem virk.</span><span class="sxs-lookup"><span data-stu-id="b3c98-114">is selected as active.</span></span>  
2. <span data-ttu-id="b3c98-115">Smellið á **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-115">Click **Reporting configurations**.</span></span> <span data-ttu-id="b3c98-116">Við munum endurnota fyrirliggjandi grunnstillingu Rafræn skýrslugerð sem var fyrst hönnuð til að mynda skýrsluúttak í OPENXML-sniði.</span><span class="sxs-lookup"><span data-stu-id="b3c98-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="b3c98-117">Stækkið eða fellið saman „Greiðslulíka“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="b3c98-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="b3c98-118">Í trénu skal velja „greiðslulíkan/dæmi um vinnublaðsskýrslu“.</span><span class="sxs-lookup"><span data-stu-id="b3c98-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="b3c98-119">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="b3c98-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="b3c98-120">Skipta Excel-sniðmáti út fyrir Word-sniðmát</span><span class="sxs-lookup"><span data-stu-id="b3c98-120">Replace the Excel template with the Word template</span></span>

<span data-ttu-id="b3c98-121">Núna er Excel-skjal notað sem sniðmát til að mynda úttak í OPENXML-sniði.</span><span class="sxs-lookup"><span data-stu-id="b3c98-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="b3c98-122">Við munum flytja inn sniðmát skýrslunnar í Word-sniði.</span><span class="sxs-lookup"><span data-stu-id="b3c98-122">We will import the report’s template in Word format.</span></span>

1. <span data-ttu-id="b3c98-123">Smelltu á **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-123">Click **Attachments**.</span></span> <span data-ttu-id="b3c98-124">Skipta út fyrirliggjandi Excel-sniðmát fyrir Word-sniðmát sem áður var sótt, SampleVendPaymDocReport.docx.</span><span class="sxs-lookup"><span data-stu-id="b3c98-124">Replace the existing Excel template with the Word template that you downloaded earlier, SampleVendPaymDocReport.docx.</span></span> <span data-ttu-id="b3c98-125">Athugaðu að þetta sniðmát inniheldur aðeins útlit skjals sem á að mynda sem úttak í Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="b3c98-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="b3c98-126">Smellið á **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-126">Click **Delete**.</span></span>
3. <span data-ttu-id="b3c98-127">Smellið á **Já**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-127">Click **Yes**.</span></span>
4. <span data-ttu-id="b3c98-128">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-128">Click **New**.</span></span>
5. <span data-ttu-id="b3c98-129">Smelltu á **Skrá**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-129">Click **File**.</span></span>
6. <span data-ttu-id="b3c98-130">Smellið á **Fletta**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-130">Click **Browse**.</span></span> <span data-ttu-id="b3c98-131">Fletta á og velja SampleVendPaymDocReport.docx sem áður var sótt.</span><span class="sxs-lookup"><span data-stu-id="b3c98-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="b3c98-132">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-132">Click **OK**.</span></span> <span data-ttu-id="b3c98-133">Velja sniðmát sem sótt í fyrra skref.</span><span class="sxs-lookup"><span data-stu-id="b3c98-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="b3c98-134">Sláið inn eða veldu gildi í reitnum **sniðmát**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-134">In the **Template** field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="b3c98-135">Víkka Word-sniðmát út með því bæta við sérstilltum XML-hluta</span><span class="sxs-lookup"><span data-stu-id="b3c98-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="b3c98-136">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-136">Click **Save**.</span></span> <span data-ttu-id="b3c98-137">Auk þess að vista breyting á grunnstilling, aðgerðin Vista uppfærir viðhengt Word-sniðmát.</span><span class="sxs-lookup"><span data-stu-id="b3c98-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="b3c98-138">Uppbygging hannaða sniðsins er flutt í viðhengt Word-skjal sem nýr sérstilltur XML-hluti með heitinu „Skýrsla“.</span><span class="sxs-lookup"><span data-stu-id="b3c98-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="b3c98-139">Athugaðu að viðhengda Word-sniðmát inniheldur ekki aðeins útlit skjalsins sem á að mynda sem úttak Rafræn skýrslugerð, heldur líka inniheldur uppbygging gagna sem Rafræn skýrslugerð setur inn í sniðmát í þessari keyrslu.</span><span class="sxs-lookup"><span data-stu-id="b3c98-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="b3c98-140">Smelltu á **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-140">Click **Attachments**.</span></span>
    + <span data-ttu-id="b3c98-141">Nú þarf að binda einingar sérstillta XML-hlutans „Skýrsla“ við hluta í Word-skjal.</span><span class="sxs-lookup"><span data-stu-id="b3c98-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    + <span data-ttu-id="b3c98-142">Ef þú þekkir Word-skjöl sem hægt er að hanna sem skjámynd sem innihalda efnisstjórnun sem eru bundin af einingum af sérstillt XML-hlutar, skal spila öll skref næsta undirverkefnis til að mynda slíkt skjal.</span><span class="sxs-lookup"><span data-stu-id="b3c98-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="b3c98-143">Sjá frekari upplýsingar í [Stofna eyðublöð sem notendur fylla út eða prenta í Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US).</span><span class="sxs-lookup"><span data-stu-id="b3c98-143">For more details, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US).</span></span> <span data-ttu-id="b3c98-144">Annars skal sleppa öllum skrefum í næsta undirverkefni.</span><span class="sxs-lookup"><span data-stu-id="b3c98-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="b3c98-145">Fá Word með sérstillt XML-hluta til að framkvæma gagnatengsl</span><span class="sxs-lookup"><span data-stu-id="b3c98-145">Get Word with custom XML part to do data bindings</span></span>

<span data-ttu-id="b3c98-146">Opnaðu þetta skjal í Word og gerðu eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="b3c98-146">Open this document in Word and do the following:</span></span>  
1. <span data-ttu-id="b3c98-147">Opnaðu flipann Word Developer (sérstilltu borðann ef hann er ekki virkur enn).</span><span class="sxs-lookup"><span data-stu-id="b3c98-147">Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>
2. <span data-ttu-id="b3c98-148">Veldu XML vörpunarglugga.</span><span class="sxs-lookup"><span data-stu-id="b3c98-148">Select XML mapping pane.</span></span>
3. <span data-ttu-id="b3c98-149">Veldu sérstillta XML-hlutann „Skýrsla“ í uppflettingu.</span><span class="sxs-lookup"><span data-stu-id="b3c98-149">Select the ‘Report’ custom XML part in the lookup.</span></span>
4. <span data-ttu-id="b3c98-150">Framkvæmdu vörpun eininga í völdum sérstilltum XML-hluta og efnisstjórnun í Word-skjal.</span><span class="sxs-lookup"><span data-stu-id="b3c98-150">Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="b3c98-151">5.</span><span class="sxs-lookup"><span data-stu-id="b3c98-151">5.</span></span> <span data-ttu-id="b3c98-152">Vistaðu uppfært Word-skjal á staðbundið drif.</span><span class="sxs-lookup"><span data-stu-id="b3c98-152">Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="b3c98-153">Hlaða upp Word-sniðmát með sérstillt XML-hluta sem er bundinn við efnisstjórnun</span><span class="sxs-lookup"><span data-stu-id="b3c98-153">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="b3c98-154">Smellið á **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-154">Click **Delete**.</span></span>
2. <span data-ttu-id="b3c98-155">Smellið á **Já**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-155">Click **Yes**.</span></span> <span data-ttu-id="b3c98-156">Bæta við nýju sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="b3c98-156">Add a new template.</span></span> <span data-ttu-id="b3c98-157">Ef þú laukst við skrefin í fyrra undirverk skal velja Word-skjal sem var undirbúið og vista staðbundinn.</span><span class="sxs-lookup"><span data-stu-id="b3c98-157">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="b3c98-158">Annars skal velja MS Word-sniðmátið SampleVendPaymDocReportBounded.docx sem áður var sótt.</span><span class="sxs-lookup"><span data-stu-id="b3c98-158">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="b3c98-159">Smellt er á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-159">Click **New**.</span></span>
4. <span data-ttu-id="b3c98-160">Smelltu á **Skrá**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-160">Click **File**.</span></span>
5. <span data-ttu-id="b3c98-161">Smellið á **Fletta**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-161">Click **Browse**.</span></span> <span data-ttu-id="b3c98-162">Fletta á og velja SampleVendPaymDocReportBounded.docx sem áður var sótt.</span><span class="sxs-lookup"><span data-stu-id="b3c98-162">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="b3c98-163">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-163">Click **OK**.</span></span>
6. <span data-ttu-id="b3c98-164">Í svæði **Sniðmát** skal velja skjal sem var hlaðið niður í fyrra skrefi.</span><span class="sxs-lookup"><span data-stu-id="b3c98-164">In the **Template** field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="b3c98-165">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-165">Click **Save**.</span></span>
8. <span data-ttu-id="b3c98-166">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b3c98-166">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="b3c98-167">Framkvæma snið til að mynda Word-úttak</span><span class="sxs-lookup"><span data-stu-id="b3c98-167">Execute the format to create Word output</span></span>
1. <span data-ttu-id="b3c98-168">Í **Aðgerðarrúðunni** smellirðu á **Skilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-168">On the **Action Pane**, click **Configurations**.</span></span>
2. <span data-ttu-id="b3c98-169">Smelltu á **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-169">Click **User parameters**.</span></span>
3. <span data-ttu-id="b3c98-170">Veljið Já í reitnum **Stillingar keyrslu**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-170">Select Yes in the **Run settings** field.</span></span>
4. <span data-ttu-id="b3c98-171">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-171">Click **OK**.</span></span>
5. <span data-ttu-id="b3c98-172">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-172">Click **Edit**.</span></span>
6. <span data-ttu-id="b3c98-173">Veljið Já í reitnum **Drög keyrslu**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-173">Select Yes in the **Run Draft** field.</span></span>
7. <span data-ttu-id="b3c98-174">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-174">Click **Save**.</span></span>
8. <span data-ttu-id="b3c98-175">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b3c98-175">Close the page.</span></span>
9. <span data-ttu-id="b3c98-176">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b3c98-176">Close the page.</span></span>
10. <span data-ttu-id="b3c98-177">Í **skoðunarrúðunni** ferðu í **Einingar > Viðskiptaskuldir > Greiðslur > Greiðslubók**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-177">In the **Navigation pane**, go to **Modules > Accounts payable > Payments > Payment journal**.</span></span>
11. <span data-ttu-id="b3c98-178">Smellið á **Línur**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-178">Click **Lines**.</span></span>
12. <span data-ttu-id="b3c98-179">Merkið eða afmerkið allar línur í listanum.</span><span class="sxs-lookup"><span data-stu-id="b3c98-179">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="b3c98-180">Smelltu á **Greiðslustöðu**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-180">Click **Payment status**.</span></span>
14. <span data-ttu-id="b3c98-181">Smelltu á **Ekkert**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-181">Click **None**.</span></span>
15. <span data-ttu-id="b3c98-182">Smelltu á **Mynda greiðslur**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-182">Click **Generate payments**.</span></span>
16. <span data-ttu-id="b3c98-183">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-183">Click **OK**.</span></span>
17. <span data-ttu-id="b3c98-184">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="b3c98-184">Click **OK**.</span></span> <span data-ttu-id="b3c98-185">Greina myndað úttak.</span><span class="sxs-lookup"><span data-stu-id="b3c98-185">Analyze the generated output.</span></span> <span data-ttu-id="b3c98-186">Athuga að myndað úttak er sett fram í Word-snið og inniheldur upplýsingar um unnar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="b3c98-186">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  

