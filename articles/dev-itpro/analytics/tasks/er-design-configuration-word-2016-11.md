--- 
title: "Hanna grunnstillingar rafrænnar skýrslugerðar til að búa til skýrslur á Word-sniði"
description: "Eftirfarandi skref útskýra hvernig notandi í annaðhvort hlutverk kerfisstjóri eða þróunaraðili rafræn skýrslugerð getur grunnstilla snið rafræn skýrslugerð til að mynda skýrslur sem skjöl í Microsoft Word."
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: dc47d44285af4c720d2f450d11fb1004ef461d0f
ms.contentlocale: is-is
ms.lasthandoff: 10/16/2018

---
# <a name="design-er-configurations-to-generate-reports-in-word-format"></a><span data-ttu-id="9e856-103">Hanna grunnstillingar rafrænnar skýrslugerðar til að búa til skýrslur á Word-sniði</span><span class="sxs-lookup"><span data-stu-id="9e856-103">Design ER configurations to generate reports in Word format</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e856-104">Eftirfarandi skref útskýra hvernig notandi í annaðhvort hlutverk kerfisstjóri eða þróunaraðili rafræn skýrslugerð getur grunnstilla snið rafræn skýrslugerð til að mynda skýrslur sem skjöl í Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="9e856-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="9e856-105">Hægt er að framkvæma þessum skrefum í GBSI fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="9e856-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="9e856-106">Til að ljúka þessum skrefum verður fyrst að ljúka við skref í verkefnaleiðbeiningar „Búa til grunnstilling Rafræn skýrslugerð til að mynda skýrslur í OPENXML-snið“.</span><span class="sxs-lookup"><span data-stu-id="9e856-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="9e856-107">Fyrirfram verður líka að hlaða niður og vista eftirfarandi sniðmát staðbundið fyrir sýnishorn skýrslu:</span><span class="sxs-lookup"><span data-stu-id="9e856-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

- [<span data-ttu-id="9e856-108">Sniðmát greiðsluskýrslu</span><span class="sxs-lookup"><span data-stu-id="9e856-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="9e856-109">Afmarkað sniðmát greiðsluskýrslu</span><span class="sxs-lookup"><span data-stu-id="9e856-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)


<span data-ttu-id="9e856-110">Þetta ferli er fyrir eiginleika sem var bætt við í Microsoft Dynamics 365 for Operations útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="9e856-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="9e856-111">Velja fyrirliggjandi grunnstilling skýrsla í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="9e856-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="9e856-112">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="9e856-112">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="9e856-113">Gakktu úr skugga um að veitandi grunnstillingar „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="9e856-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="9e856-114">sé merkt sem virk.</span><span class="sxs-lookup"><span data-stu-id="9e856-114">is selected as active.</span></span>  
2. <span data-ttu-id="9e856-115">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="9e856-115">Click Reporting configurations.</span></span>
    * <span data-ttu-id="9e856-116">Við munum endurnota fyrirliggjandi grunnstillingu Rafræn skýrslugerð sem var fyrst hönnuð til að mynda skýrsluúttak í OPENXML-sniði.</span><span class="sxs-lookup"><span data-stu-id="9e856-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="9e856-117">Stækkið eða fellið saman „Greiðslulíka“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="9e856-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="9e856-118">Í trénu skal velja „greiðslulíkan/dæmi um vinnublaðsskýrslu“.</span><span class="sxs-lookup"><span data-stu-id="9e856-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="9e856-119">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="9e856-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="9e856-120">Skipta Excel-sniðmáti út fyrir Word-sniðmát</span><span class="sxs-lookup"><span data-stu-id="9e856-120">Replace the Excel template with the Word template</span></span>
    * <span data-ttu-id="9e856-121">Núna er Excel-skjal notað sem sniðmát til að mynda úttak í OPENXML-sniði.</span><span class="sxs-lookup"><span data-stu-id="9e856-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="9e856-122">Við munum flytja inn sniðmát skýrslunnar í Word-sniði.</span><span class="sxs-lookup"><span data-stu-id="9e856-122">We will import the report’s template in Word format.</span></span>  
1. <span data-ttu-id="9e856-123">Smellt er á viðhengi</span><span class="sxs-lookup"><span data-stu-id="9e856-123">Click Attachments.</span></span>
    * <span data-ttu-id="9e856-124">Skipta út fyrirliggjandi Excel-sniðmát fyrir Word-sniðmát sem áður var sótt, SampleVendPaymDocReport.docx.</span><span class="sxs-lookup"><span data-stu-id="9e856-124">Replace the existing Excel template with the Word template that you downloaded earlier, SampleVendPaymDocReport.docx.</span></span> <span data-ttu-id="9e856-125">Athugaðu að þetta sniðmát inniheldur aðeins útlit skjals sem á að mynda sem úttak í Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="9e856-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="9e856-126">Smellið á Eyða.</span><span class="sxs-lookup"><span data-stu-id="9e856-126">Click Delete.</span></span>
3. <span data-ttu-id="9e856-127">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="9e856-127">Click Yes.</span></span>
4. <span data-ttu-id="9e856-128">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9e856-128">Click New.</span></span>
5. <span data-ttu-id="9e856-129">Smella á Skrá</span><span class="sxs-lookup"><span data-stu-id="9e856-129">Click File.</span></span>
6. <span data-ttu-id="9e856-130">Smellið á Fletta.</span><span class="sxs-lookup"><span data-stu-id="9e856-130">Click Browse.</span></span> <span data-ttu-id="9e856-131">Fletta á og velja SampleVendPaymDocReport.docx sem áður var sótt.</span><span class="sxs-lookup"><span data-stu-id="9e856-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="9e856-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9e856-132">Click OK.</span></span>
    * <span data-ttu-id="9e856-133">Velja sniðmát sem sótt í fyrra skref.</span><span class="sxs-lookup"><span data-stu-id="9e856-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="9e856-134">Sláið inn eða veldu gildi í reitnum sniðmát.</span><span class="sxs-lookup"><span data-stu-id="9e856-134">In the Template field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="9e856-135">Víkka Word-sniðmát út með því bæta við sérstilltum XML-hluta</span><span class="sxs-lookup"><span data-stu-id="9e856-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="9e856-136">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9e856-136">Click Save.</span></span>
    * <span data-ttu-id="9e856-137">Auk þess að vista breyting á grunnstilling, aðgerðin Vista uppfærir viðhengt Word-sniðmát.</span><span class="sxs-lookup"><span data-stu-id="9e856-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="9e856-138">Uppbygging hannaða sniðsins er flutt í viðhengt Word-skjal sem nýr sérstilltur XML-hluti með heitinu „Skýrsla“.</span><span class="sxs-lookup"><span data-stu-id="9e856-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="9e856-139">Athugaðu að viðhengda Word-sniðmát inniheldur ekki aðeins útlit skjalsins sem á að mynda sem úttak Rafræn skýrslugerð, heldur líka inniheldur uppbygging gagna sem Rafræn skýrslugerð setur inn í sniðmát í þessari keyrslu.</span><span class="sxs-lookup"><span data-stu-id="9e856-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="9e856-140">Smellt er á viðhengi</span><span class="sxs-lookup"><span data-stu-id="9e856-140">Click Attachments.</span></span>
    * <span data-ttu-id="9e856-141">Nú þarf að binda einingar sérstillta XML-hlutans „Skýrsla“ við hluta í Word-skjal.</span><span class="sxs-lookup"><span data-stu-id="9e856-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    * <span data-ttu-id="9e856-142">Ef þú þekkir Word-skjöl sem hægt er að hanna sem skjámynd sem innihalda efnisstjórnun sem eru bundin af einingum af sérstillt XML-hlutar, skal spila öll skref næsta undirverkefnis til að mynda slíkt skjal.</span><span class="sxs-lookup"><span data-stu-id="9e856-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="9e856-143">Nánari upplýsingar er að finna á https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span><span class="sxs-lookup"><span data-stu-id="9e856-143">For more details, see this link https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span></span> <span data-ttu-id="9e856-144">Annars skal sleppa öllum skrefum í næsta undirverkefni.</span><span class="sxs-lookup"><span data-stu-id="9e856-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="9e856-145">Fá Word með sérstillt XML-hluta til að framkvæma gagnatengsl</span><span class="sxs-lookup"><span data-stu-id="9e856-145">Get Word with custom XML part to do data bindings</span></span>
    * <span data-ttu-id="9e856-146">Opna þetta skjal í Word og gera eftirfarandi: - Opna flipann Word Developer (sérstilltu borðann ef hann er ekki virkur).</span><span class="sxs-lookup"><span data-stu-id="9e856-146">Open this document in Word and do the following:  - Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>  <span data-ttu-id="9e856-147">- Velja XML vörpunargluggi.</span><span class="sxs-lookup"><span data-stu-id="9e856-147">- Select XML mapping pane.</span></span>  <span data-ttu-id="9e856-148">- Velja sérstillta XML-hlutann „Skýrsla“ í uppflettingu.</span><span class="sxs-lookup"><span data-stu-id="9e856-148">- Select the ‘Report’ custom XML part in the lookup.</span></span>  <span data-ttu-id="9e856-149">- Framkvæma vörpun eininga í völdum sérstilltum XML-hluta og efnisstjórnun í Word-skjal.</span><span class="sxs-lookup"><span data-stu-id="9e856-149">- Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="9e856-150">- Vista uppfærður Word-skjal í staðbundið drif.</span><span class="sxs-lookup"><span data-stu-id="9e856-150">- Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="9e856-151">Hlaða upp Word-sniðmát með sérstillt XML-hluta sem er bundinn við efnisstjórnun</span><span class="sxs-lookup"><span data-stu-id="9e856-151">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="9e856-152">Smellið á Eyða.</span><span class="sxs-lookup"><span data-stu-id="9e856-152">Click Delete.</span></span>
2. <span data-ttu-id="9e856-153">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="9e856-153">Click Yes.</span></span>
    * <span data-ttu-id="9e856-154">Bæta við nýju sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="9e856-154">Add a new template.</span></span> <span data-ttu-id="9e856-155">Ef þú laukst við skrefin í fyrra undirverk skal velja Word-skjal sem var undirbúið og vista staðbundinn.</span><span class="sxs-lookup"><span data-stu-id="9e856-155">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="9e856-156">Annars skal velja MS Word-sniðmátið SampleVendPaymDocReportBounded.docx sem áður var sótt.</span><span class="sxs-lookup"><span data-stu-id="9e856-156">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="9e856-157">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9e856-157">Click New.</span></span>
4. <span data-ttu-id="9e856-158">Smella á Skrá</span><span class="sxs-lookup"><span data-stu-id="9e856-158">Click File.</span></span>
5. <span data-ttu-id="9e856-159">Smellið á Fletta.</span><span class="sxs-lookup"><span data-stu-id="9e856-159">Click Browse.</span></span> <span data-ttu-id="9e856-160">Fletta á og velja SampleVendPaymDocReportBounded.docx sem áður var sótt.</span><span class="sxs-lookup"><span data-stu-id="9e856-160">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="9e856-161">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="9e856-161">Click OK.</span></span>
6. <span data-ttu-id="9e856-162">Í svæði Sniðmát skal velja skjal sem sótt í fyrra skref.</span><span class="sxs-lookup"><span data-stu-id="9e856-162">In the Template field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="9e856-163">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9e856-163">Click Save.</span></span>
8. <span data-ttu-id="9e856-164">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9e856-164">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="9e856-165">Framkvæma snið til að mynda Word-úttak</span><span class="sxs-lookup"><span data-stu-id="9e856-165">Execute the format to create Word output</span></span>
1. <span data-ttu-id="9e856-166">Í Aðgerðarrúðunni er smellt á skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="9e856-166">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="9e856-167">Smelltu á Færibreytur notanda</span><span class="sxs-lookup"><span data-stu-id="9e856-167">Click User parameters.</span></span>
3. <span data-ttu-id="9e856-168">Veljið Já í svæðinu Stillingar keyrslu.</span><span class="sxs-lookup"><span data-stu-id="9e856-168">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="9e856-169">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9e856-169">Click OK.</span></span>
5. <span data-ttu-id="9e856-170">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="9e856-170">Click Edit.</span></span>
6. <span data-ttu-id="9e856-171">Veljið Já í svæðinu drög keyrslu.</span><span class="sxs-lookup"><span data-stu-id="9e856-171">Select Yes in the Run Draft field.</span></span>
7. <span data-ttu-id="9e856-172">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9e856-172">Click Save.</span></span>
8. <span data-ttu-id="9e856-173">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9e856-173">Close the page.</span></span>
9. <span data-ttu-id="9e856-174">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="9e856-174">Close the page.</span></span>
10. <span data-ttu-id="9e856-175">Fara í Viðskiptaskuldir > Greiðslur > Greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="9e856-175">Go to Accounts payable > Payments > Payment journal.</span></span>
11. <span data-ttu-id="9e856-176">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="9e856-176">Click Lines.</span></span>
12. <span data-ttu-id="9e856-177">Merkið eða afmerkið allar línur í listanum.</span><span class="sxs-lookup"><span data-stu-id="9e856-177">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="9e856-178">Smellt er á greiðslustöðu.</span><span class="sxs-lookup"><span data-stu-id="9e856-178">Click Payment status.</span></span>
14. <span data-ttu-id="9e856-179">Smellt á Ekkert.</span><span class="sxs-lookup"><span data-stu-id="9e856-179">Click None.</span></span>
15. <span data-ttu-id="9e856-180">Smelltu á Mynda greiðslur.</span><span class="sxs-lookup"><span data-stu-id="9e856-180">Click Generate payments.</span></span>
16. <span data-ttu-id="9e856-181">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9e856-181">Click OK.</span></span>
17. <span data-ttu-id="9e856-182">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9e856-182">Click OK.</span></span>
    * <span data-ttu-id="9e856-183">Greina myndað úttak.</span><span class="sxs-lookup"><span data-stu-id="9e856-183">Analyze the generated output.</span></span> <span data-ttu-id="9e856-184">Athuga að myndað úttak er sett fram í Word-snið og inniheldur upplýsingar um unnar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="9e856-184">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  


