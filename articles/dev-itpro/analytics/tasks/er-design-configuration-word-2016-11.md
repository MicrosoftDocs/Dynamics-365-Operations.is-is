--- 
title: "Hanna skilgreiningu fyrir myndun skýrslna á Microsoft Word-sniði fyrir rafræna skýrslugerð (ER)"
description: "Eftirfarandi skref útskýra hvernig notandi í annaðhvort hlutverk kerfisstjóri eða þróunaraðili rafræn skýrslugerð getur grunnstilla snið rafræn skýrslugerð til að mynda skýrslur sem skjöl í Microsoft Word."
author: NickSelin
manager: AnnBe
ms.date: 12/21/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 21eb35e7713ce856b7c6d364e2ad4dfc1b30e5fd
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---
# <a name="design-a-configuration-for-generating-reports-in-microsoft-word-format-for-electronic-reporting-er"></a><span data-ttu-id="e38ac-103">Hanna skilgreiningu fyrir myndun skýrslna á Microsoft Word-sniði fyrir rafræna skýrslugerð (ER)</span><span class="sxs-lookup"><span data-stu-id="e38ac-103">Design a configuration for generating reports in Microsoft Word format for electronic reporting (ER)</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e38ac-104">Eftirfarandi skref útskýra hvernig notandi í annaðhvort hlutverk kerfisstjóri eða þróunaraðili rafræn skýrslugerð getur grunnstilla snið rafræn skýrslugerð til að mynda skýrslur sem skjöl í Microsoft Word.</span><span class="sxs-lookup"><span data-stu-id="e38ac-104">The following steps explain how a user in either the System administrator or Electronic reporting developer role can configure an Electronic reporting (ER) formats to generate reports as Microsoft Word files.</span></span> <span data-ttu-id="e38ac-105">Hægt er að framkvæma þessum skrefum í GBSI fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="e38ac-105">These steps can be performed in the GBSI company.</span></span>

<span data-ttu-id="e38ac-106">Til að ljúka þessum skrefum verður fyrst að ljúka við skref í verkefnaleiðbeiningar „Búa til grunnstilling Rafræn skýrslugerð til að mynda skýrslur í OPENXML-snið“.</span><span class="sxs-lookup"><span data-stu-id="e38ac-106">To complete these steps, you must first complete the steps in the “Create an ER configuration for generating reports in OPENXML format” task guide.</span></span> <span data-ttu-id="e38ac-107">Fyrirfram verður líka að hlaða niður og vista eftirfarandi sniðmát staðbundið fyrir sýnishorn skýrslu:</span><span class="sxs-lookup"><span data-stu-id="e38ac-107">In advance, you must also download and save the following templates locally for the sample report:</span></span>

[<span data-ttu-id="e38ac-108">Sniðmát greiðsluskýrslu</span><span class="sxs-lookup"><span data-stu-id="e38ac-108">Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

[<span data-ttu-id="e38ac-109">Afmarkað sniðmát greiðsluskýrslu</span><span class="sxs-lookup"><span data-stu-id="e38ac-109">Bounded Template of Payment Report</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="e38ac-110">Þetta ferli er fyrir eiginleika sem var bætt við í Microsoft Dynamics 365 for Operations útgáfu 1611.</span><span class="sxs-lookup"><span data-stu-id="e38ac-110">This procedure is for a feature that was added in Microsoft Dynamics 365 for Operations version 1611.</span></span>


## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="e38ac-111">Velja fyrirliggjandi grunnstilling skýrsla í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="e38ac-111">Select the existing ER report configuration</span></span>
1. <span data-ttu-id="e38ac-112">Fara í Fyrirtækisstjórnun > Vinnusvæði > Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="e38ac-112">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="e38ac-113">Gakktu úr skugga um að veitandi grunnstillingar „Litware, Inc.“</span><span class="sxs-lookup"><span data-stu-id="e38ac-113">Make sure that the configuration provider ‘Litware, Inc.’</span></span> <span data-ttu-id="e38ac-114">sé merkt sem virk.</span><span class="sxs-lookup"><span data-stu-id="e38ac-114">is selected as active.</span></span>  
2. <span data-ttu-id="e38ac-115">Smelltu á Grunnstillingar skýrslugerðar</span><span class="sxs-lookup"><span data-stu-id="e38ac-115">Click Reporting configurations.</span></span>
    * <span data-ttu-id="e38ac-116">Við munum endurnota fyrirliggjandi grunnstillingu Rafræn skýrslugerð sem var fyrst hönnuð til að mynda skýrsluúttak í OPENXML-sniði.</span><span class="sxs-lookup"><span data-stu-id="e38ac-116">We will re-use the existing ER configuration that has been originally designed to generate the report output in OPENXML format.</span></span>  
3. <span data-ttu-id="e38ac-117">Stækkið eða fellið saman „Greiðslulíka“ í trénu.</span><span class="sxs-lookup"><span data-stu-id="e38ac-117">In the tree, expand 'Payment model'.</span></span>
4. <span data-ttu-id="e38ac-118">Í trénu skal velja „greiðslulíkan/dæmi um vinnublaðsskýrslu“.</span><span class="sxs-lookup"><span data-stu-id="e38ac-118">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
5. <span data-ttu-id="e38ac-119">Smellið á Hönnuður.</span><span class="sxs-lookup"><span data-stu-id="e38ac-119">Click Designer.</span></span>

## <a name="replace-the-excel-template-with-the-word-template"></a><span data-ttu-id="e38ac-120">Skipta Excel-sniðmáti út fyrir Word-sniðmát</span><span class="sxs-lookup"><span data-stu-id="e38ac-120">Replace the Excel template with the Word template</span></span>
    * <span data-ttu-id="e38ac-121">Núna er Excel-skjal notað sem sniðmát til að mynda úttak í OPENXML-sniði.</span><span class="sxs-lookup"><span data-stu-id="e38ac-121">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="e38ac-122">Við munum flytja inn sniðmát skýrslunnar í Word-sniði.</span><span class="sxs-lookup"><span data-stu-id="e38ac-122">We will import the report’s template in Word format.</span></span>  
1. <span data-ttu-id="e38ac-123">Smellt er á viðhengi</span><span class="sxs-lookup"><span data-stu-id="e38ac-123">Click Attachments.</span></span>
    * <span data-ttu-id="e38ac-124">Skipta út fyrirliggjandi Excel-sniðmát fyrir Word-sniðmát sem áður var sótt, sniðmát greiðsluskýrslu.</span><span class="sxs-lookup"><span data-stu-id="e38ac-124">Replace the existing Excel template with the Word template that you downloaded earlier, Template of Payment Report.</span></span> <span data-ttu-id="e38ac-125">Athugaðu að þetta sniðmát inniheldur aðeins útlit skjals sem á að mynda sem úttak í Rafræn skýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="e38ac-125">Note, this template only contains the layout of the document we want to generate as ER output.</span></span>  
2. <span data-ttu-id="e38ac-126">Smellið á Eyða.</span><span class="sxs-lookup"><span data-stu-id="e38ac-126">Click Delete.</span></span>
3. <span data-ttu-id="e38ac-127">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="e38ac-127">Click Yes.</span></span>
4. <span data-ttu-id="e38ac-128">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e38ac-128">Click New.</span></span>
5. <span data-ttu-id="e38ac-129">Smella á Skrá</span><span class="sxs-lookup"><span data-stu-id="e38ac-129">Click File.</span></span>
6. <span data-ttu-id="e38ac-130">Smellið á Fletta.</span><span class="sxs-lookup"><span data-stu-id="e38ac-130">Click Browse.</span></span> <span data-ttu-id="e38ac-131">Fletta á og velja SampleVendPaymDocReport.docx sem áður var sótt.</span><span class="sxs-lookup"><span data-stu-id="e38ac-131">Navigate to and select SampleVendPaymDocReport.docx that you previously downloaded.</span></span> <span data-ttu-id="e38ac-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e38ac-132">Click OK.</span></span>
    * <span data-ttu-id="e38ac-133">Velja sniðmát sem sótt í fyrra skref.</span><span class="sxs-lookup"><span data-stu-id="e38ac-133">Select the template that you downloaded in the previous step.</span></span>  
7. <span data-ttu-id="e38ac-134">Sláið inn eða veldu gildi í reitnum sniðmát.</span><span class="sxs-lookup"><span data-stu-id="e38ac-134">In the Template field, enter or select a value.</span></span>

## <a name="extend-the-word-template-by-adding-a-custom-xml-part"></a><span data-ttu-id="e38ac-135">Víkka Word-sniðmát út með því bæta við sérstilltum XML-hluta</span><span class="sxs-lookup"><span data-stu-id="e38ac-135">Extend the Word template by adding a custom XML part</span></span>
1. <span data-ttu-id="e38ac-136">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e38ac-136">Click Save.</span></span>
    * <span data-ttu-id="e38ac-137">Auk þess að vista breyting á grunnstilling, aðgerðin Vista uppfærir viðhengt Word-sniðmát.</span><span class="sxs-lookup"><span data-stu-id="e38ac-137">In addition to storing configuration changes, the Save action also updates the attached Word template.</span></span> <span data-ttu-id="e38ac-138">Uppbygging hannaða sniðsins er flutt í viðhengt Word-skjal sem nýr sérstilltur XML-hluti með heitinu „Skýrsla“.</span><span class="sxs-lookup"><span data-stu-id="e38ac-138">The structure of the designed format is ported to the attached Word document as a new custom XML part with the name ‘Report’.</span></span> <span data-ttu-id="e38ac-139">Athugaðu að viðhengda Word-sniðmát inniheldur ekki aðeins útlit skjalsins sem á að mynda sem úttak Rafræn skýrslugerð, heldur líka inniheldur uppbygging gagna sem Rafræn skýrslugerð setur inn í sniðmát í þessari keyrslu.</span><span class="sxs-lookup"><span data-stu-id="e38ac-139">Note that the attached Word template contains not only the layout of the document we want to generate as ER output, it also contains the structure of data that ER will populate into this template at runtime.</span></span>  
2. <span data-ttu-id="e38ac-140">Smellt er á viðhengi</span><span class="sxs-lookup"><span data-stu-id="e38ac-140">Click Attachments.</span></span>
    * <span data-ttu-id="e38ac-141">Nú þarf að binda einingar sérstillta XML-hlutans „Skýrsla“ við hluta í Word-skjal.</span><span class="sxs-lookup"><span data-stu-id="e38ac-141">Now you need to bind the elements of the custom XML part ‘Report’ to the Word document parts.</span></span>  
    * <span data-ttu-id="e38ac-142">Ef þú þekkir Word-skjöl sem hægt er að hanna sem skjámynd sem innihalda efnisstjórnun sem eru bundin af einingum af sérstillt XML-hlutar, skal spila öll skref næsta undirverkefnis til að mynda slíkt skjal.</span><span class="sxs-lookup"><span data-stu-id="e38ac-142">If you're familiar with Word documents that can be designed as forms containing content controls that are bounded with elements of custom XML parts – play all steps of the next sub-task to create such a document.</span></span> <span data-ttu-id="e38ac-143">Nánari upplýsingar á þessum tengli https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span><span class="sxs-lookup"><span data-stu-id="e38ac-143">For more details, see this link https://support.office.com/en-us/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b?ui=en-US&rs=en-US&ad=US.</span></span> <span data-ttu-id="e38ac-144">Annars skal sleppa öllum skrefum í næsta undirverkefni.</span><span class="sxs-lookup"><span data-stu-id="e38ac-144">Otherwise, skip all the steps in the next sub-task.</span></span>  

## <a name="get-word-with-custom-xml-part-to-do-data-bindings"></a><span data-ttu-id="e38ac-145">Fá Word með sérstillt XML-hluta til að framkvæma gagnatengsl</span><span class="sxs-lookup"><span data-stu-id="e38ac-145">Get Word with custom XML part to do data bindings</span></span>
    * <span data-ttu-id="e38ac-146">Opna þetta skjal í Word og gera eftirfarandi: - Opna flipann Word Developer (sérstilltu borðann ef hann er ekki virkur).</span><span class="sxs-lookup"><span data-stu-id="e38ac-146">Open this document in Word and do the following:  - Open the Word Developer tab (customize the ribbon if it is not enabled yet).</span></span>  <span data-ttu-id="e38ac-147">- Velja XML vörpunargluggi.</span><span class="sxs-lookup"><span data-stu-id="e38ac-147">- Select XML mapping pane.</span></span>  <span data-ttu-id="e38ac-148">- Velja sérstillta XML-hlutann „Skýrsla“ í uppflettingu.</span><span class="sxs-lookup"><span data-stu-id="e38ac-148">- Select the ‘Report’ custom XML part in the lookup.</span></span>  <span data-ttu-id="e38ac-149">- Framkvæma vörpun eininga í völdum sérstilltum XML-hluta og efnisstjórnun í Word-skjal.</span><span class="sxs-lookup"><span data-stu-id="e38ac-149">- Do mapping of the elements of the selected custom XML part and content controls of the Word document.</span></span>  <span data-ttu-id="e38ac-150">- Vista uppfærður Word-skjal í staðbundið drif.</span><span class="sxs-lookup"><span data-stu-id="e38ac-150">- Save the updated Word document on a local drive.</span></span>  

## <a name="upload-the-word-template-with-custom-xml-part-bounded-to-content-controls"></a><span data-ttu-id="e38ac-151">Hlaða upp Word-sniðmát með sérstillt XML-hluta sem er bundinn við efnisstjórnun</span><span class="sxs-lookup"><span data-stu-id="e38ac-151">Upload the Word template with custom XML part bounded to content controls</span></span>
1. <span data-ttu-id="e38ac-152">Smellið á Eyða.</span><span class="sxs-lookup"><span data-stu-id="e38ac-152">Click Delete.</span></span>
2. <span data-ttu-id="e38ac-153">Smella á Já.</span><span class="sxs-lookup"><span data-stu-id="e38ac-153">Click Yes.</span></span>
    * <span data-ttu-id="e38ac-154">Bæta við nýju sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="e38ac-154">Add a new template.</span></span> <span data-ttu-id="e38ac-155">Ef þú laukst við skrefin í fyrra undirverk skal velja Word-skjal sem var undirbúið og vista staðbundinn.</span><span class="sxs-lookup"><span data-stu-id="e38ac-155">If you competed the steps in the previous subtask, select the Word document that you prepared and saved locally.</span></span> <span data-ttu-id="e38ac-156">Annars skal velja MS Word-sniðmátið SampleVendPaymDocReportBounded.docx sem áður var sótt.</span><span class="sxs-lookup"><span data-stu-id="e38ac-156">Otherwise, select the SampleVendPaymDocReportBounded.docx MS Word template that you downloaded earlier.</span></span>  
3. <span data-ttu-id="e38ac-157">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="e38ac-157">Click New.</span></span>
4. <span data-ttu-id="e38ac-158">Smella á Skrá</span><span class="sxs-lookup"><span data-stu-id="e38ac-158">Click File.</span></span>
5. <span data-ttu-id="e38ac-159">Smellið á Fletta.</span><span class="sxs-lookup"><span data-stu-id="e38ac-159">Click Browse.</span></span> <span data-ttu-id="e38ac-160">Fletta á og velja SampleVendPaymDocReportBounded.docx sem áður var sótt.</span><span class="sxs-lookup"><span data-stu-id="e38ac-160">Navigate to and select SampleVendPaymDocReportBounded.docx that you previously downloaded.</span></span> <span data-ttu-id="e38ac-161">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="e38ac-161">Click OK.</span></span>
6. <span data-ttu-id="e38ac-162">Í svæði Sniðmát skal velja skjal sem sótt í fyrra skref.</span><span class="sxs-lookup"><span data-stu-id="e38ac-162">In the Template field, select the document that you downloaded in the previous step.</span></span>
7. <span data-ttu-id="e38ac-163">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e38ac-163">Click Save.</span></span>
8. <span data-ttu-id="e38ac-164">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e38ac-164">Close the page.</span></span>

## <a name="execute-the-format-to-create-word-output"></a><span data-ttu-id="e38ac-165">Framkvæma snið til að mynda Word-úttak</span><span class="sxs-lookup"><span data-stu-id="e38ac-165">Execute the format to create Word output</span></span>
1. <span data-ttu-id="e38ac-166">Í Aðgerðarrúðunni er smellt á skilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="e38ac-166">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="e38ac-167">Smelltu á Færibreytur notanda</span><span class="sxs-lookup"><span data-stu-id="e38ac-167">Click User parameters.</span></span>
3. <span data-ttu-id="e38ac-168">Veljið Já í svæðinu Stillingar keyrslu.</span><span class="sxs-lookup"><span data-stu-id="e38ac-168">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="e38ac-169">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e38ac-169">Click OK.</span></span>
5. <span data-ttu-id="e38ac-170">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="e38ac-170">Click Edit.</span></span>
6. <span data-ttu-id="e38ac-171">Veljið Já í svæðinu drög keyrslu.</span><span class="sxs-lookup"><span data-stu-id="e38ac-171">Select Yes in the Run Draft field.</span></span>
7. <span data-ttu-id="e38ac-172">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="e38ac-172">Click Save.</span></span>
8. <span data-ttu-id="e38ac-173">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e38ac-173">Close the page.</span></span>
9. <span data-ttu-id="e38ac-174">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="e38ac-174">Close the page.</span></span>
10. <span data-ttu-id="e38ac-175">Fara í Viðskiptaskuldir > Greiðslur > Greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="e38ac-175">Go to Accounts payable > Payments > Payment journal.</span></span>
11. <span data-ttu-id="e38ac-176">Smellið á „Línur“.</span><span class="sxs-lookup"><span data-stu-id="e38ac-176">Click Lines.</span></span>
12. <span data-ttu-id="e38ac-177">Merkið eða afmerkið allar línur í listanum.</span><span class="sxs-lookup"><span data-stu-id="e38ac-177">In the list, mark or unmark all rows.</span></span>
13. <span data-ttu-id="e38ac-178">Smellt er á greiðslustöðu.</span><span class="sxs-lookup"><span data-stu-id="e38ac-178">Click Payment status.</span></span>
14. <span data-ttu-id="e38ac-179">Smellt á Ekkert.</span><span class="sxs-lookup"><span data-stu-id="e38ac-179">Click None.</span></span>
15. <span data-ttu-id="e38ac-180">Smelltu á Mynda greiðslur.</span><span class="sxs-lookup"><span data-stu-id="e38ac-180">Click Generate payments.</span></span>
16. <span data-ttu-id="e38ac-181">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e38ac-181">Click OK.</span></span>
17. <span data-ttu-id="e38ac-182">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="e38ac-182">Click OK.</span></span>
    * <span data-ttu-id="e38ac-183">Greina myndað úttak.</span><span class="sxs-lookup"><span data-stu-id="e38ac-183">Analyze the generated output.</span></span> <span data-ttu-id="e38ac-184">Athuga að myndað úttak er sett fram í Word-snið og inniheldur upplýsingar um unnar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="e38ac-184">Note that the created output is presented in Word format and contains the details of the processed payments.</span></span>  


