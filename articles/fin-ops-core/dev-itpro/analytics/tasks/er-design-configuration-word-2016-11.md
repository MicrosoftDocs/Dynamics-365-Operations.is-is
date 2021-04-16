---
title: Endurnýta stillingar rafrænnar skýrslugerðar með Excel-sniðmátum til að búa til skýrslur á Word-sniði
description: Þetta efnisatriði lýsir því hvernig skýrslusnið sem voru hönnuð til að mynda skýrslur sem Excel-vinnubækur geta verið skilgreind til að búa til skýrslur sem Word-skjöl.
author: NickSelin
ms.date: 01/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 728984678d78cf626e2b30222f1d1e603e05d117
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755059"
---
# <a name="reuse-er-configurations-with-excel-templates-to-generate-reports-in-word-format"></a><span data-ttu-id="56736-103">Endurnýta stillingar rafrænnar skýrslugerðar með Excel-sniðmátum til að búa til skýrslur á Word-sniði</span><span class="sxs-lookup"><span data-stu-id="56736-103">Reuse ER configurations with Excel templates to generate reports in Word format</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="56736-104">Til að búa til skýrslur sem Microsoft Word-skjöl er hægt að [skilgreina](../er-design-configuration-word.md) nýtt [rafrænt skýrslugerðar](../general-electronic-reporting.md)[snið](../general-electronic-reporting.md#FormatComponentOutbound).</span><span class="sxs-lookup"><span data-stu-id="56736-104">To generate reports as Microsoft Word documents, you can [configure](../er-design-configuration-word.md) a new [Electronic reporting (ER)](../general-electronic-reporting.md) [format](../general-electronic-reporting.md#FormatComponentOutbound).</span></span> <span data-ttu-id="56736-105">Að öðrum kosti er hægt að nota snið sem var upphaflega hannað til að mynda skýrslur sem Excel-vinnubækur.</span><span class="sxs-lookup"><span data-stu-id="56736-105">Alternatively, you can reuse an ER format that was originally designed to generate reports as Excel workbooks.</span></span> <span data-ttu-id="56736-106">Í þessu tilfelli þarf að skipta Excel-sniðmátinu út fyrir Word-sniðmát.</span><span class="sxs-lookup"><span data-stu-id="56736-106">In this case, you must replace the Excel template with a Word template.</span></span>

<span data-ttu-id="56736-107">Eftirfarandi ferli sýna hvernig notandi annaðhvort í hlutverki kerfisstjóra eða þróunaraðila rafrænnar skýrslugerðar getur skilgreint snið rafrænnar skýrslugerðar til að búa til skýrslur sem Word-skrár með því að endurnýta snið rafrænnar skýrslugerðar sem var hannað til að mynda skýrslur sem Excel-skrár.</span><span class="sxs-lookup"><span data-stu-id="56736-107">The following procedures show how a user in either the System administrator role or the Electronic reporting developer role can configure an ER format to generate reports as Word files by reusing an ER format that was designed to generate reports as Excel files.</span></span>

<span data-ttu-id="56736-108">Hægt er að ljúka við allar þessar aðgerðir í GBSI-fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="56736-108">These procedures can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="56736-109">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="56736-109">Prerequisites</span></span>

<span data-ttu-id="56736-110">Til að ljúka þessum ferlum þarf fyrst að fylgja skrefunum í verkleiðbeiningunni [Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði](er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="56736-110">To complete these procedures, you must first follow the steps in the [Design a configuration for generating reports in OPENXML format](er-design-reports-openxml-2016-11.md) task guide.</span></span>

<span data-ttu-id="56736-111">Einnig þarf að hlaða niður og vista eftirfarandi sniðmát staðbundið fyrir sýnishorn skýrslu:</span><span class="sxs-lookup"><span data-stu-id="56736-111">You must also download and locally save the following templates for the sample report:</span></span>

- [<span data-ttu-id="56736-112">Sniðmát greiðsluskýrslu (SampleVendPaymDocReport.docx)</span><span class="sxs-lookup"><span data-stu-id="56736-112">Template of Payment Report (SampleVendPaymDocReport.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)
- [<span data-ttu-id="56736-113">Bundið sniðmát greiðsluskýrslu (SampleVendPaymDocReportBounded.docx)</span><span class="sxs-lookup"><span data-stu-id="56736-113">Bounded Template of Payment Report (SampleVendPaymDocReportBounded.docx)</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)

<span data-ttu-id="56736-114">Þetta ferli er fyrir eiginleika sem var bætt við í Dynamics 365 for Operations, útgáfu 1611 (nóvember 2016).</span><span class="sxs-lookup"><span data-stu-id="56736-114">These procedures are for a feature that was added in Dynamics 365 for Operations version 1611 (November 2016).</span></span>

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="56736-115">Velja fyrirliggjandi grunnstilling skýrsla í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="56736-115">Select the existing ER report configuration</span></span>

1. <span data-ttu-id="56736-116">Í Dynamics 365 Finance skal fara í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="56736-116">In Dynamics 365 Finance, go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="56736-117">Gangið úr skugga um að skilgreiningarveitan **Litware, Inc** sé valin sem **Virk**.</span><span class="sxs-lookup"><span data-stu-id="56736-117">Make sure that the **Litware, Inc.** configuration provider is selected as **Active**.</span></span> <span data-ttu-id="56736-118">Ef svo er ekki skal fylgja skrefunum í verkleiðbeiningunni [Stofna skilgreiningarveitendur og merkja þá sem virka](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="56736-118">If it isn't, follow the steps in the [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) task guide.</span></span>
3. <span data-ttu-id="56736-119">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="56736-119">Select **Reporting configurations**.</span></span> <span data-ttu-id="56736-120">Endurnota skal fyrirliggjandi skilgreiningu rafrænnar skýrslugerðar sem var fyrst hönnuð til að mynda skýrsluúttak á OPENXML-sniði.</span><span class="sxs-lookup"><span data-stu-id="56736-120">You will reuse the existing ER configuration that was designed to generate the report output in OPENXML format.</span></span>
4. <span data-ttu-id="56736-121">Á síðunni **Skilgreiningar**, í skilgreiningatrénu á svæðinu til vinstri, skal stækka **Greiðslulíkan** og velja **Dæmi um vinnublaðsskýrslu**.</span><span class="sxs-lookup"><span data-stu-id="56736-121">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and select **Sample worksheet report**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="56736-122">Útgáfudrögum valins sniðs rafrænnar skýrslugerðar er hægt að breyta í flýtiflipanum **Útgáfur**.</span><span class="sxs-lookup"><span data-stu-id="56736-122">The draft version of the selected ER format can be edited on the **Versions** FastTab.</span></span>

5. <span data-ttu-id="56736-123">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="56736-123">Select **Designer**.</span></span>
6. <span data-ttu-id="56736-124">Athugið að á síðunni **Sniðshönnuður** gefur titill á einingu rótarsniðs til kynna að Excel-sniðmátið sé í notkun sem stendur.</span><span class="sxs-lookup"><span data-stu-id="56736-124">On the **Format designer** page, notice that the title of the root format element indicates that an Excel template is currently used.</span></span>

![Núverandi skilgreining valin](../media/er-design-configuration-word-2016-11-image01.gif)

## <a name="review-the-downloaded-word-template"></a><span data-ttu-id="56736-126">Fara yfir sótt Word-sniðmát</span><span class="sxs-lookup"><span data-stu-id="56736-126">Review the downloaded Word template</span></span>

1. <span data-ttu-id="56736-127">Í Word-skjáborðsforritinu skal opna sniðmátsskrána **SampleVendPaymDocReport.docx** sem var sótt hér áður.</span><span class="sxs-lookup"><span data-stu-id="56736-127">In the Word desktop application, open the **SampleVendPaymDocReport.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="56736-128">Gangið úr skugga um að sniðmátið innihaldi aðeins útlit skjalsins sem á að mynda sem úttak rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="56736-128">Verify that the template contains only the layout of the document that you want to generate as ER output.</span></span>

![Útlit Word-sniðmátsins í skjáborðsforritinu](../media/er-design-configuration-word-2016-11-image02.png)

## <a name="replace-the-excel-template-with-the-word-template-and-add-a-custom-xml-part"></a><span data-ttu-id="56736-130">Skipta Excel-sniðmáti út fyrir Word-sniðmát og bæta við sérsniðnum XML-hluta</span><span class="sxs-lookup"><span data-stu-id="56736-130">Replace the Excel template with the Word template and add a custom XML part</span></span>

<span data-ttu-id="56736-131">Núna er Excel-skjal notað sem sniðmát til að mynda úttak í OPENXML-sniði.</span><span class="sxs-lookup"><span data-stu-id="56736-131">Currently, the Excel document is used as a template to generate the output in OPENXML format.</span></span> <span data-ttu-id="56736-132">Þessu sniðmáti verður skipt út fyrir Word-sniðmátskránni SampleVendPaymDocReport.docx sem var sótt hér á undan.</span><span class="sxs-lookup"><span data-stu-id="56736-132">You will replace this template with the SampleVendPaymDocReport.docx Word template file that you downloaded earlier.</span></span> <span data-ttu-id="56736-133">Þú munt einnig víkka Word-sniðmát út með því bæta við sérstilltum XML-hluta.</span><span class="sxs-lookup"><span data-stu-id="56736-133">You will also extend the Word template by adding a custom XML part.</span></span>

1. <span data-ttu-id="56736-134">Í Finance, á síðunni **Sniðshönnuður**, í flipanum **Snið**, skal velja **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="56736-134">In Finance, on the **Format designer** page, on the **Format** tab, select **Attachments**.</span></span>
2. <span data-ttu-id="56736-135">Á síðunni **Viðhengi** skal velja **Eyða** til að fjarlægja fyrirliggjandi Excel-sniðmát.</span><span class="sxs-lookup"><span data-stu-id="56736-135">On the **Attachments** page, select **Delete** to remove the existing Excel template.</span></span> <span data-ttu-id="56736-136">Veljið **Já** til að staðfesta breytinguna.</span><span class="sxs-lookup"><span data-stu-id="56736-136">Select **Yes** to confirm the change.</span></span>
3. <span data-ttu-id="56736-137">Veljið **Ný** \> **Skrá**.</span><span class="sxs-lookup"><span data-stu-id="56736-137">Select **New** \> **File**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="56736-138">Velja verður gerð skjals sem var [skilgreint](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) í færibreytum rafrænnar skýrslugerðar til að vista sniðmát rafrænna skýrslugerðarsniða.</span><span class="sxs-lookup"><span data-stu-id="56736-138">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

4. <span data-ttu-id="56736-139">Veljið **Fletta** og flettið síðan og veljið skrána **SampleVendPaymDocReport.docx** sem var sótt áður.</span><span class="sxs-lookup"><span data-stu-id="56736-139">Select **Browse**, and then browse to and select the **SampleVendPaymDocReport.docx** file that you downloaded earlier.</span></span>
5. <span data-ttu-id="56736-140">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="56736-140">Select **OK**.</span></span>
6. <span data-ttu-id="56736-141">Lokaðu síðunni **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="56736-141">Close the **Attachments** page.</span></span>
7. <span data-ttu-id="56736-142">Á síðunni **Sniðshönnuður**, í reitinn **Sniðmát**, skal færa inn eða velja skrána **SampleVendPaymDocReport.docx** til að nota Word-sniðmátið í staðinn fyrir Excel-sniðmátið sem var valið hér áður.</span><span class="sxs-lookup"><span data-stu-id="56736-142">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReport.docx** file to use that Word template instead of the Excel template that was previously used.</span></span>
8. <span data-ttu-id="56736-143">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="56736-143">Select **Save**.</span></span>

    <span data-ttu-id="56736-144">Auk þess að vista breyting á grunnstilling uppfærir aðgerðin **Vista** viðhengt Word-sniðmát.</span><span class="sxs-lookup"><span data-stu-id="56736-144">In addition to storing configuration changes, the **Save** action updates the attached Word template.</span></span> <span data-ttu-id="56736-145">Stigveldisskipulagi hannaða sniðsins er bætt við viðhengt Word-skjal sem nýr sérstilltur XML-hluti sem heitir **Skýrsla**.</span><span class="sxs-lookup"><span data-stu-id="56736-145">The hierarchical structure of the designed format is added to the attached Word document as a new custom XML part that is named **Report**.</span></span> <span data-ttu-id="56736-146">Viðhengt Word-sniðmát inniheldur útlit skjalsins sem verður myndað sem úttak rafrænnar skýrslugerðar og skipulag gagna sem rafræn skýrslugerð færir inn í sniðmátið við keyrslu.</span><span class="sxs-lookup"><span data-stu-id="56736-146">The attached Word template contains the layout of the document that will be generated as ER output and the structure of data that ER will enter in that template at runtime.</span></span>

9. <span data-ttu-id="56736-147">Athugið að titill á einingu rótarsniðs gefur til kynna að Word-sniðmátið sé í notkun sem stendur.</span><span class="sxs-lookup"><span data-stu-id="56736-147">Notice that the title of the root format element indicates that a Word template is currently used.</span></span>

    ![Excel-sniðmáti skipt út fyrir Word-sniðmát og sérsniðnum XML-hluta bætt við](../media/er-design-configuration-word-2016-11-image03.gif)

10. <span data-ttu-id="56736-149">Í flipanum **Snið** skal velja **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="56736-149">On the **Format** tab, select **Attachments**.</span></span>

<span data-ttu-id="56736-150">Nú er hægt að varpa einingum sérsniðna XML-hlutans **Skýrslur** í efnisstýringar Word-skjalsins.</span><span class="sxs-lookup"><span data-stu-id="56736-150">You can now map the elements of the **Report** custom XML part to the content controls of the Word document.</span></span>

<span data-ttu-id="56736-151">Ef þú kannast við ferlið við hönnun Word-skjala sem snið sem innihalda [efnisstýringar](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) sem er varpað í einingar [sérsniðinna XML-hluta](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019) skal ljúka öllum skrefum í næsta ferli til að búa til skjalið.</span><span class="sxs-lookup"><span data-stu-id="56736-151">If you're familiar with the process of designing Word documents as forms that contain [content controls](https://docs.microsoft.com/office/client-developer/word/content-controls-in-word) that are mapped to elements of [custom XML parts](https://docs.microsoft.com/visualstudio/vsto/custom-xml-parts-overview?view=vs-2019), complete all steps in the next procedure to create the document.</span></span> <span data-ttu-id="56736-152">Frekari upplýsingar er að finna [Búa til snið sem notendur ljúka við eða prenta í Word](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span><span class="sxs-lookup"><span data-stu-id="56736-152">For more information, see [Create forms that users complete or print in Words](https://support.office.com/article/Create-forms-that-users-complete-or-print-in-Word-040c5cc1-e309-445b-94ac-542f732c8c8b).</span></span> <span data-ttu-id="56736-153">Annars skal sleppa næsta ferli.</span><span class="sxs-lookup"><span data-stu-id="56736-153">Otherwise, skip the next procedure.</span></span>

## <a name="get-a-word-document-that-has-a-custom-xml-part-and-do-data-mapping"></a><a id='get-word-doc'></a><span data-ttu-id="56736-154">Sækja Word-skjal sem er með sérsniðinn XML-hluta og varpa gögnum</span><span class="sxs-lookup"><span data-stu-id="56736-154">Get a Word document that has a custom XML part and do data mapping</span></span>

1. <span data-ttu-id="56736-155">Í Finance, á síðunni **Viðhengi**, skal **Opna** til að sækja valið sniðmát úr Finance og vista það staðbundið sem Word-skjal.</span><span class="sxs-lookup"><span data-stu-id="56736-155">In Finance, on the **Attachments** page, select **Open** to download the selected template from Finance and store it locally as a Word document.</span></span>
3. <span data-ttu-id="56736-156">Í Word-skjáborðsforritinu skal opna skjalið sem var sótt.</span><span class="sxs-lookup"><span data-stu-id="56736-156">In the Word desktop application, open the document that you just downloaded.</span></span>
4. <span data-ttu-id="56736-157">Í flipanum **Þróunaraðili** skal velja **XML-vörpunarsvæði**.</span><span class="sxs-lookup"><span data-stu-id="56736-157">On the **Developer** tab, select **XML Mapping Pane**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="56736-158">Ef flipinn **Þróunaraðili** birtist ekki í borðanum skal sérsníða borðann til að bæta honum við.</span><span class="sxs-lookup"><span data-stu-id="56736-158">If the **Developer** tab doesn't appear on the ribbon, customize the ribbon to add it.</span></span>

5. <span data-ttu-id="56736-159">Á svæðinu **XML-vörpun**, í reitnum **Sérsniðinn XML-hluti**, skal velja sérsniðna XML-hlutann **Skýrsla**.</span><span class="sxs-lookup"><span data-stu-id="56736-159">In the **XML Mapping** pane, in the **Custom XML Part** field, select the **Report** custom XML part.</span></span>
6. <span data-ttu-id="56736-160">Varpið einingum valda sérsniðna XML-hlutans **Skýrsla** og efnisstýringum Word-skjalsins.</span><span class="sxs-lookup"><span data-stu-id="56736-160">Map the elements of the selected **Report** custom XML part and the content controls of the Word document.</span></span>
7. <span data-ttu-id="56736-161">Vistið uppfært Word-skjal staðbundið sem **SampleVendPaymDocReportBounded.docx**.</span><span class="sxs-lookup"><span data-stu-id="56736-161">Save the updated Word document locally as **SampleVendPaymDocReportBounded.docx**.</span></span>

## <a name="review-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="56736-162">Fara yfir Word-sniðmátið þar sem sérsniðnum XML-hluta er varpað í efnisstýringar</span><span class="sxs-lookup"><span data-stu-id="56736-162">Review the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="56736-163">Í Word-skjáborðsforritinu skal opna sniðmátsskrána **SampleVendPaymDocReportBounded.docx**.</span><span class="sxs-lookup"><span data-stu-id="56736-163">In the Word desktop application, open the **SampleVendPaymDocReportBounded.docx** template file.</span></span>
2. <span data-ttu-id="56736-164">Gangið úr skugga um að sniðmátið innihaldi útlit skjalsins sem á að mynda sem úttak rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="56736-164">Verify that the template contains the layout of the document that you want to generate as ER output.</span></span> <span data-ttu-id="56736-165">Efnisstýringarnar sem eru notaðar sem staðgenglar fyrir gögn sem rafræn skýrslugerð færir inn í þetta sniðmát við keyrslu byggjast á vörpunum sem eru skilgreindar milli eininga sérsniðna XML-hlutans **Skýrsla** og efnisstýringar Word-skjalsins.</span><span class="sxs-lookup"><span data-stu-id="56736-165">The content controls that are used as placeholders for data that ER will enter in this template at runtime are based on the mappings that are configured between elements of the **Report** custom XML part and the content controls of the Word document.</span></span>

![Forskoða Word-sniðmát í skjáborðsforritinu](../media/er-design-configuration-word-2016-11-image04.png)

## <a name="upload-the-word-template-where-the-custom-xml-part-is-mapped-to-content-controls"></a><span data-ttu-id="56736-167">Hlaða upp Word-sniðmáti þar sem sérsniðnum XML-hluta er varpað í efnisstýringar</span><span class="sxs-lookup"><span data-stu-id="56736-167">Upload the Word template where the custom XML part is mapped to content controls</span></span>

1. <span data-ttu-id="56736-168">Í Finance, á síðunni **Viðhengi**, skal velja **Eyða** til að fjarlægja Word-sniðmátið sem er með engar varpanir milli eininga sérsniðna XML-hlutans **Skýrsla** og efnisstýringar.</span><span class="sxs-lookup"><span data-stu-id="56736-168">In Finance, on the **Attachments** page, select **Delete** to remove the Word template that has no mappings between elements of the **Report** custom XML part and content controls.</span></span> <span data-ttu-id="56736-169">Veljið **Já** til að staðfesta breytinguna.</span><span class="sxs-lookup"><span data-stu-id="56736-169">Select **Yes** to confirm the change.</span></span>
2. <span data-ttu-id="56736-170">Veljið **Ný** \> **Skrá** til að bæta við nýrri sniðmátsskrá sem inniheldur varpanir milli eininga sérsniðna XML-hlutans **Skýrsla** og efnisstýringar.</span><span class="sxs-lookup"><span data-stu-id="56736-170">Select **New** \> **File** to add a new template file that contains mappings between elements of the **Report** custom XML part and content controls.</span></span>

    > [!NOTE]
    > <span data-ttu-id="56736-171">Velja verður gerð skjals sem var [skilgreint](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) í færibreytum rafrænnar skýrslugerðar til að vista sniðmát rafrænna skýrslugerðarsniða.</span><span class="sxs-lookup"><span data-stu-id="56736-171">You must select a document type that has been [configured](../electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) in the ER parameters to store templates of ER formats.</span></span>

3. <span data-ttu-id="56736-172">Veljið **Fletta** og flettið síðan að og veljið skrána **SampleVendPaymDocReportBounded.docx** sem var sótt eða undirbúin með því að ljúka ferlinu í hlutanum [Ná í Word sem er með sérsniðinn XML-hluta til að gera gagnavörpun](#get-word-doc).</span><span class="sxs-lookup"><span data-stu-id="56736-172">Select **Browse**, and then browse to and select the **SampleVendPaymDocReportBounded.docx** file that you downloaded or prepared by completing the procedure in the [Get a Word that has a custom XML part to do data mapping](#get-word-doc) section.</span></span>
4. <span data-ttu-id="56736-173">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="56736-173">Select **OK**.</span></span>
5. <span data-ttu-id="56736-174">Lokaðu síðunni **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="56736-174">Close the **Attachments** page.</span></span>
6. <span data-ttu-id="56736-175">Á síðunni **Sniðshönnuður**, í reitnum **Sniðmát**, skal velja skjalið sem var sótt.</span><span class="sxs-lookup"><span data-stu-id="56736-175">On the **Format designer** page, in the **Template** field, select the document that you just downloaded.</span></span>
7. <span data-ttu-id="56736-176">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="56736-176">Select **Save**.</span></span>
8. <span data-ttu-id="56736-177">Lokaðu síðunni **Sniðshönnuður**.</span><span class="sxs-lookup"><span data-stu-id="56736-177">Close the **Format designer** page.</span></span>

## <a name="mark-the-configured-format-as-runnable"></a><span data-ttu-id="56736-178">Merkja skilgreint snið sem keyranlegt</span><span class="sxs-lookup"><span data-stu-id="56736-178">Mark the configured format as runnable</span></span>

<span data-ttu-id="56736-179">Til að keyra útgáfudrög breytanlega sniðsins þarf að gera það [keyranlegt](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span><span class="sxs-lookup"><span data-stu-id="56736-179">To run the draft version of the editable format, you must make it [runnable](../er-quick-start2-customize-report.md#MarkFormatRunnable).</span></span>

1. <span data-ttu-id="56736-180">Í Finance, á síðunni **Skilgreiningar**, í aðgerðarúðunni, í flipanum **Skilgreiningar**, í flokknum **Ítarlegar stillingar**, skal velja **Færibreytur notanda**.</span><span class="sxs-lookup"><span data-stu-id="56736-180">In Finance, on the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
2. <span data-ttu-id="56736-181">Í glugganum **Færibreytur notanda** skal stilla valkostinn **Keyra stillingar** á **Já** og síðan velja **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="56736-181">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
3. <span data-ttu-id="56736-182">Veljið **Breyta** til að gera núverandi síðu breytanlega ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="56736-182">Select **Edit** to make the current page editable, as required.</span></span>
4. <span data-ttu-id="56736-183">Fyrir þegar völdu skilgreininguna **Dæmi um vinnublaðsskýrslu** skal stilla valkostinn **Keyra drög** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="56736-183">For the currently selected **Sample worksheet report** configuration, set the **Run Draft** option to **Yes**.</span></span>
5. <span data-ttu-id="56736-184">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="56736-184">Select **Save**.</span></span>

## <a name="run-the-format-to-create-output-in-word-format"></a><span data-ttu-id="56736-185">Keyra snið til að búa til úttak á Word-sniði</span><span class="sxs-lookup"><span data-stu-id="56736-185">Run the format to create output in Word format</span></span>

1. <span data-ttu-id="56736-186">Í Finance skal fara í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók**.</span><span class="sxs-lookup"><span data-stu-id="56736-186">In Finance, go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="56736-187">Í greiðslubók sem var færð inn áður skal velja **Línur**.</span><span class="sxs-lookup"><span data-stu-id="56736-187">In a payment journal that you entered earlier, select **Lines**.</span></span>
3. <span data-ttu-id="56736-188">Á síðunni **Greiðslur lánardrottna** skal velja allar línur í hnitanetinu.</span><span class="sxs-lookup"><span data-stu-id="56736-188">On the **Vendor payments** page, select all rows in the grid.</span></span>
4. <span data-ttu-id="56736-189">Veljið **Greiðslustaða** \> **Engin**.</span><span class="sxs-lookup"><span data-stu-id="56736-189">Select **Payment status** \> **None**.</span></span>

    ![Greiðslur til úrvinnslu á greiðslusíðu lánardrottins](../media/er-design-configuration-word-2016-11-image05.png)

5. <span data-ttu-id="56736-191">Á aðgerðasvæðinu skal velja **Búa til greiðslur**.</span><span class="sxs-lookup"><span data-stu-id="56736-191">On the Action Pane, select **Generate payments**.</span></span>
6. <span data-ttu-id="56736-192">Í svarglugganum sem kemur upp skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="56736-192">In the dialog box that appears, follow these steps:</span></span>

    1. <span data-ttu-id="56736-193">Í reitnum **Greiðslumáti** skal velja **Rafrænn**.</span><span class="sxs-lookup"><span data-stu-id="56736-193">In the **Method of payment** field, select **Electronic**.</span></span>
    2. <span data-ttu-id="56736-194">Í reitnum **Bankareikningur** skal velja **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="56736-194">In the **Bank account** field, select **GBSI OPER**.</span></span>
    3. <span data-ttu-id="56736-195">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="56736-195">Select **OK**.</span></span>

7. <span data-ttu-id="56736-196">Í **Svargluggi rafrænna skýrslufæribreyta** velurðu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="56736-196">In the **Electronic report parameters** dialog box, select **OK**.</span></span>
8. <span data-ttu-id="56736-197">Myndað úttak er sett fram í Word-snið og inniheldur upplýsingar um unnar greiðslur.</span><span class="sxs-lookup"><span data-stu-id="56736-197">The generated output is presented in Word format and contains the details of the processed payments.</span></span> <span data-ttu-id="56736-198">Greina myndað úttak.</span><span class="sxs-lookup"><span data-stu-id="56736-198">Analyze the generated output.</span></span>

    ![Myndað úttak á Word-sniði](../media/er-design-configuration-word-2016-11-image06.png)

## <a name="additional-resources"></a><span data-ttu-id="56736-200">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="56736-200">Additional resources</span></span>

- [<span data-ttu-id="56736-201">Hanna nýja skilgreiningu rafrænnar skýrslugerðar til að búa til skýrslur á Word-sniði</span><span class="sxs-lookup"><span data-stu-id="56736-201">Design a new ER configuration to generate reports in Word format</span></span>](../er-design-configuration-word.md)
- [<span data-ttu-id="56736-202">Felldu inn myndir og form í skjöl sem þú myndar með því að nota ER</span><span class="sxs-lookup"><span data-stu-id="56736-202">Embed images and shapes in documents that you generate by using ER</span></span>](../electronic-reporting-embed-images-shapes.md#embed-an-image-in-a-word-document)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]