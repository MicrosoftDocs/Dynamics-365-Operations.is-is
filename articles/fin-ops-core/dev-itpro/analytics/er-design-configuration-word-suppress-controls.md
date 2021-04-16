---
title: Fela Word-efnisstýringar í mynduðum skýrslum
description: Í þessu efni er útskýrt hvernig á að skilgreina snið rafrænnar skýrslugerðar til að mynda skýrslur sem Microsoft Word-skrár þar sem efnisstýringar eru faldar.
author: NickSelin
ms.date: 02/11/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner,  LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-01-01
ms.dyn365.ops.version: Version 10.0.6
ms.openlocfilehash: 8c99203110cfdc7f8123c30488611d55f48e8f67
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753602"
---
# <a name="suppress-word-content-controls-in-generated-reports"></a><span data-ttu-id="45313-103">Fela Word-efnisstýringar í mynduðum skýrslum</span><span class="sxs-lookup"><span data-stu-id="45313-103">Suppress Word content controls in generated reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="45313-104">Til að búa til skýrslur sem Microsoft Word-skjöl þarf að hanna sniðmát fyrir skýrslurnar sem Word-skjal.</span><span class="sxs-lookup"><span data-stu-id="45313-104">To generate reports as Microsoft Word documents, you must design a template for the reports as a Word document.</span></span> <span data-ttu-id="45313-105">Þetta sniðmát verður að innihalda Word-efnisstýringar sem staðgengla fyrir gögn sem verður fyllt út í við keyrslu.</span><span class="sxs-lookup"><span data-stu-id="45313-105">This template must contain Word content controls as placeholders for data that will be filled in at runtime.</span></span> <span data-ttu-id="45313-106">Til að nota Word-skjalið sem sniðmát sem er búið til sem sniðmát fyrir skýrslurnar er hægt að [skilgreina](er-design-configuration-word.md) nýja [rafræna skýrslugerðar](general-electronic-reporting.md) [lausn](er-quick-start1-new-solution.md).</span><span class="sxs-lookup"><span data-stu-id="45313-106">To use the Word document that is created as a template for your reports, you can [configure](er-design-configuration-word.md) a new [Electronic reporting (ER)](general-electronic-reporting.md) [solution](er-quick-start1-new-solution.md).</span></span> <span data-ttu-id="45313-107">Lausnin verður að fela í sér [skilgreiningu](general-electronic-reporting.md#Configuration) rafrænnar skýrslugerðar sem inniheldur [sniðshlut](general-electronic-reporting.md#FormatComponentOutbound) rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="45313-107">The solution must include an ER [configuration](general-electronic-reporting.md#Configuration) that contains an ER [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="45313-108">Þetta snið rafrænnar skýrslugerðar verður að vera skilgreint til að nota hannaða sniðmátið fyrir myndun skýrslu.</span><span class="sxs-lookup"><span data-stu-id="45313-108">This ER format must be configured to use the designed template for report generation.</span></span>

<span data-ttu-id="45313-109">Í útgáfu 10.0.6 og nýrri af Dynamics 365 Finance er hægt að skilgreina formúlur í snið rafrænnar skýrslugerðar til að fela sumar Word-efnisstýringar í mynduðum skjölum.</span><span class="sxs-lookup"><span data-stu-id="45313-109">In version 10.0.6 and later of Dynamics 365 Finance, you can configure formulas in your ER format to suppress some Word content controls in generated documents.</span></span>

<span data-ttu-id="45313-110">Eftirfarandi skref útskýra hvernig notandi sem er úthlutað hlutverki kerfisstjóra eða hagnýts ráðgjafa rafrænnar skýrslugerðar getur skilgreint snið rafrænnar skýrslugerðar sem myndar skýrslur sem Word-skrár og felur sumar efnisstýringarnar í mynduðum skýrslum sem hafa verið skilgreindar með því að nota Word-sniðmát.</span><span class="sxs-lookup"><span data-stu-id="45313-110">The following steps explain how a user who is assigned to the System administrator or Electronic reporting functional consultant role can configure an ER format that generates reports as Word files and suppresses some of the content controls in the generated reports that have been configured by using a Word template.</span></span>

<span data-ttu-id="45313-111">Hægt er að ljúka þessum skrefum í GBSI-fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="45313-111">These steps can be completed in the GBSI company.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="45313-112">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="45313-112">Prerequisites</span></span>

<span data-ttu-id="45313-113">Til að ljúka þessum skrefum þarf fyrst að ljúka skrefunum í eftirfarandi verkleiðbeiningum:</span><span class="sxs-lookup"><span data-stu-id="45313-113">To complete these steps, you must first complete the steps in the following task guides:</span></span>

- [<span data-ttu-id="45313-114">Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði</span><span class="sxs-lookup"><span data-stu-id="45313-114">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="45313-115">Endurnýta stillingar rafrænnar skýrslugerðar með Excel-sniðmátum til að búa til skýrslur á Word-sniði</span><span class="sxs-lookup"><span data-stu-id="45313-115">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)

<span data-ttu-id="45313-116">Þegar skrefum þessara verkleiðbeininga er lokið eru eftirfarandi atriði undirbúin:</span><span class="sxs-lookup"><span data-stu-id="45313-116">When you complete the steps of these task guides, the following items are prepared:</span></span>

- <span data-ttu-id="45313-117">Rafrænt skýrslugerðarsnið fyrir **Dæmi um vinnublaðsskýrslu** sem er skilgreint til að búa til skjal á Word-sniði</span><span class="sxs-lookup"><span data-stu-id="45313-117">A **Sample worksheet report** ER format that is configured to generate a document in Word format</span></span>
- <span data-ttu-id="45313-118">Útgáfa [draga](general-electronic-reporting.md#component-versioning) fyrir rafrænt skýrslugerðarsnið fyrir **Dæmi um vinnublaðsskýrslu** sem er merkt sem **Keyranlegt**</span><span class="sxs-lookup"><span data-stu-id="45313-118">A [draft](general-electronic-reporting.md#component-versioning) version of the **Sample worksheet report** ER format that is marked as **Runnable**</span></span>
- <span data-ttu-id="45313-119">**Rafræn** greiðslumáti sem er skilgreindur til að nota **Dæmi um vinnublaðsskýrslu** rafræns skýrslugerðarsniðs fyrir afgreiðslu lánardrottnagreiðslu</span><span class="sxs-lookup"><span data-stu-id="45313-119">An **Electronic** method of payments that is configured to use the **Sample worksheet report** ER format for vendor payment processing</span></span>

<span data-ttu-id="45313-120">Einnig þarf að hlaða niður og vista eftirfarandi sniðmát fyrir sýnishorn skýrslu:</span><span class="sxs-lookup"><span data-stu-id="45313-120">You must also download and save the following template for the sample report:</span></span>

- [<span data-ttu-id="45313-121">Afmarkað sniðmát 2 af greiðsluskýrslu (SampleVendPaymDocReportBounded2.docx)</span><span class="sxs-lookup"><span data-stu-id="45313-121">Bounded Template 2 of Payment Report (SampleVendPaymDocReportBounded2.docx)</span></span>](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded2.docx)

## <a name="review-the-downloaded-word-template"></a><a id="tag-control"></a><span data-ttu-id="45313-122">Fara yfir sótt Word-sniðmát</span><span class="sxs-lookup"><span data-stu-id="45313-122">Review the downloaded Word template</span></span>

1. <span data-ttu-id="45313-123">Í Word-skjáborðsforritinu skal opna sniðmátsskrána **SampleVendPaymDocReportBounded2.docx** sem var sótt hér áður.</span><span class="sxs-lookup"><span data-stu-id="45313-123">In the Word desktop application, open the **SampleVendPaymDocReportBounded2.docx** template file that you downloaded earlier.</span></span>
2. <span data-ttu-id="45313-124">Gangið úr skugga um að sniðmátsskráin innihaldi yfirlitshluta sem sýnir samtals greiðsluupphæðir fyrir hvern gjaldmiðilskóða sem hefur verið uppfylltur í afgreiddum greiðslum.</span><span class="sxs-lookup"><span data-stu-id="45313-124">Verify that the template file contains a summary section that shows the total payment amounts for every currency code that has been met in the processed payments.</span></span>

    - <span data-ttu-id="45313-125">Samantektarhlutann er að finna í aðskildri töflu Word-skjalsins.</span><span class="sxs-lookup"><span data-stu-id="45313-125">The summary section resides in a separate table of the Word document.</span></span>
    - <span data-ttu-id="45313-126">Fyrsta lína töflunnar inniheldur fyrirsagnir töfludálka sem haus hlutans.</span><span class="sxs-lookup"><span data-stu-id="45313-126">The first row of this table holds the table columns headings as the section header.</span></span>
    - <span data-ttu-id="45313-127">Önnur lína töflunnar inniheldur endurtekna efnisstýringu sem upplýsingar um hluta.</span><span class="sxs-lookup"><span data-stu-id="45313-127">The second row of this table holds the repeating content control as the section details.</span></span>
    - <span data-ttu-id="45313-128">Þessari efnisstýringu er varpað í reitinn **SummaryLines** í sérsniðna XML-hlutanum **Skýrsla**.</span><span class="sxs-lookup"><span data-stu-id="45313-128">This content control is mapped to the **SummaryLines** field of the **Report** custom XML part.</span></span>
    - <span data-ttu-id="45313-129">Á grundvelli þessarar vörpunar tengist efnisstýringin einingunni **SummaryLines** í breytanlegu sniði rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="45313-129">Based on this mapping, the content control is associated with the **SummaryLines** element of the editable ER format.</span></span>

    > [!NOTE]
    > <span data-ttu-id="45313-130">Endurtekna efnisstýringin er merkt af lyklinum **SummaryLines** sem passar við reit sérsniðna XML-hlutans sem hefur verið varpað í.</span><span class="sxs-lookup"><span data-stu-id="45313-130">The repeating content control is tagged by the **SummaryLines** key that matches the field of the custom XML part that it has been mapped to.</span></span>

    ![Útlit Word-sniðmáts](./media/er-design-configuration-word-suppress-controls-image1.gif)

## <a name="select-the-existing-er-report-configuration"></a><span data-ttu-id="45313-132">Velja fyrirliggjandi grunnstilling skýrsla í Rafræn skýrslugerð</span><span class="sxs-lookup"><span data-stu-id="45313-132">Select the existing ER report configuration</span></span>

<span data-ttu-id="45313-133">Fyrir eftirfarandi skref verður fyrirliggjandi skilgreining rafrænnar skýrslugerðar notuð aftur sem var skilgreind þegar lokið var við skrefin í áðurnefndum verkleiðbeiningum.</span><span class="sxs-lookup"><span data-stu-id="45313-133">For the following steps, you will reuse the existing ER configuration that you configured when you completed the steps in the previously mentioned task guides.</span></span>

1. <span data-ttu-id="45313-134">Farðu í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð**.</span><span class="sxs-lookup"><span data-stu-id="45313-134">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="45313-135">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="45313-135">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="45313-136">Á síðunni **Skilgreiningar**, í skilgreiningatrénu, skal stækka **Greiðslulíkan** og velja **Dæmi um vinnublaðsskýrslu**.</span><span class="sxs-lookup"><span data-stu-id="45313-136">On the **Configurations** page, in the configuration tree, expand **Payment model**, and select **Sample worksheet report**.</span></span>
4. <span data-ttu-id="45313-137">Veljið **Hönnuður** til að breyta útgáfudrögum valins sniðs rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="45313-137">Select **Designer** to edit the draft version of the selected ER format.</span></span>

## <a name="replace-the-current-template-with-the-new-template"></a><span data-ttu-id="45313-138">Skipta út núgildandi sniðmáti fyrir nýja sniðmátið</span><span class="sxs-lookup"><span data-stu-id="45313-138">Replace the current template with the new template</span></span>

<span data-ttu-id="45313-139">Núna er skráin SampleVendPaymDocReportBounded.docx notuð sem sniðmát til að búa til úttakið á Word-sniði.</span><span class="sxs-lookup"><span data-stu-id="45313-139">Currently, the SampleVendPaymDocReportBounded.docx file is used as a template to generate the output in Word format.</span></span> <span data-ttu-id="45313-140">Í eftirfarandi skrefum verður þessu Word-sniðmáti skipt út fyrir nýja Word-sniðmátið, SampleVendPaymDocReportBounded2.docx, sem var sótt hér áður.</span><span class="sxs-lookup"><span data-stu-id="45313-140">In the following steps, you will replace this Word template with the new Word template, SampleVendPaymDocReportBounded2.docx, that you downloaded earlier.</span></span>

1. <span data-ttu-id="45313-141">Á síðunni **Sniðshönnuður** skal velja **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="45313-141">On the **Format designer** page, select **Attachments**.</span></span>
2. <span data-ttu-id="45313-142">Á síðunni **Viðhengi** skal velja **Eyða** til að fjarlægja fyrirliggjandi sniðmát.</span><span class="sxs-lookup"><span data-stu-id="45313-142">On the **Attachments** page, select **Delete** to remove the existing template.</span></span>
3. <span data-ttu-id="45313-143">Veljið **Já** til að staðfesta eyðinguna.</span><span class="sxs-lookup"><span data-stu-id="45313-143">Select **Yes** to confirm the deletion.</span></span>
4. <span data-ttu-id="45313-144">Veljið **Ný** \> **Skrá**.</span><span class="sxs-lookup"><span data-stu-id="45313-144">Select **New** \> **File**.</span></span>
5. <span data-ttu-id="45313-145">Veljið **Fletta** og flettið síðan og veljið skrána **SampleVendPaymDocReportBounded2.docx** sem var sótt áður.</span><span class="sxs-lookup"><span data-stu-id="45313-145">Select **Browse**, and browse to and select the **SampleVendPaymDocReportBounded2.docx** file that you downloaded earlier.</span></span>
6. <span data-ttu-id="45313-146">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="45313-146">Select **OK**.</span></span>
7. <span data-ttu-id="45313-147">Lokaðu síðunni **Viðhengi**.</span><span class="sxs-lookup"><span data-stu-id="45313-147">Close the **Attachments** page.</span></span>
8. <span data-ttu-id="45313-148">Á síðunni **Sniðshönnuður**, í reitinn **Sniðmát**, skal færa inn eða velja skrána **SampleVendPaymDocReportBounded2.docx**.</span><span class="sxs-lookup"><span data-stu-id="45313-148">On the **Format designer** page, in the **Template** field, enter or select the **SampleVendPaymDocReportBounded2.docx** file.</span></span>

## <a name="run-the-format-to-create-word-output"></a><span data-ttu-id="45313-149">Keyra sniðið til að búa til Word-úttak</span><span class="sxs-lookup"><span data-stu-id="45313-149">Run the format to create Word output</span></span>

1. <span data-ttu-id="45313-150">Farðu í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók**.</span><span class="sxs-lookup"><span data-stu-id="45313-150">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="45313-151">Á síðunni **Greiðslur lánardrottna**, í flipanum **Listi**, skal velja allar greiðslurnar.</span><span class="sxs-lookup"><span data-stu-id="45313-151">On the **Vendor payments** page, on the **List** tab, select all the payments.</span></span>
3. <span data-ttu-id="45313-152">Veljið **Greiðslustaða** \> **Engin**.</span><span class="sxs-lookup"><span data-stu-id="45313-152">Select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="45313-153">Veldu **Búa til greiðslur**.</span><span class="sxs-lookup"><span data-stu-id="45313-153">Select **Generate payments**.</span></span>
5. <span data-ttu-id="45313-154">Í reitnum **Greiðslumáti** skal velja **Rafrænn**.</span><span class="sxs-lookup"><span data-stu-id="45313-154">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="45313-155">Í reitnum **Bankareikningur** skal velja **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="45313-155">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="45313-156">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="45313-156">Select **OK**.</span></span>
8. <span data-ttu-id="45313-157">Í svargluggann **Rafrænar skýrslufæribreytur** skal velja **Í lagi** og greina myndað úttak.</span><span class="sxs-lookup"><span data-stu-id="45313-157">In the **Electronic report parameters** dialog box, select **OK**, and analyze the generated output.</span></span>

    ![Greiðslur til úrvinnslu á greiðslusíðu lánardrottins](./media/er-design-configuration-word-suppress-controls-image2.gif)

    <span data-ttu-id="45313-159">Úttakið er sýnt á Word-sniði og inniheldur samantektarhlutann.</span><span class="sxs-lookup"><span data-stu-id="45313-159">The output is presented in Word format and contains the summary section.</span></span>

## <a name="configure-the-editable-format-to-suppress-the-summary-section"></a><a id="configure-to-suppress-control"></a><span data-ttu-id="45313-160">Skilgreina breytanlegt snið til að fela samantektarhlutann</span><span class="sxs-lookup"><span data-stu-id="45313-160">Configure the editable format to suppress the summary section</span></span>

<span data-ttu-id="45313-161">Ef ætlunin er að fela samantektarhlutann í mynduðu skjali, samkvæmt beiðni notanda sem keyrir þetta rafræna skýrslugerðarsnið, þarf að lagfæra breytanlegt snið rafrænnar skýrslugerðar.</span><span class="sxs-lookup"><span data-stu-id="45313-161">If you want to suppress the summary section in a generated document, based on the request of a user who runs this ER format, you must modify the editable ER format.</span></span>

1. <span data-ttu-id="45313-162">Farið í **Fyrirtækisstjórnun** \> **Vinnusvæði** \> **Rafræn skýrslugerð** og opnið útgáfudrög rafræns skýrslugerðarsniðs til að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="45313-162">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**, and open the draft version of the ER format for editing.</span></span>
2. <span data-ttu-id="45313-163">Veldu **Skilgreiningar skýrslugerðar**.</span><span class="sxs-lookup"><span data-stu-id="45313-163">Select **Reporting configurations**.</span></span> 
3. <span data-ttu-id="45313-164">Á síðunni **Skilgreiningar**, í skilgreiningatrénu, skal stækka **Greiðslulíkan** \> **Dæmi um vinnublaðsskýrslu**.</span><span class="sxs-lookup"><span data-stu-id="45313-164">On the **Configurations** page, in the configuration tree, expand **Payment model** \> **Sample worksheet report**.</span></span>
4. <span data-ttu-id="45313-165">Veljið **Hönnuður**.</span><span class="sxs-lookup"><span data-stu-id="45313-165">Select **Designer**.</span></span>
5. <span data-ttu-id="45313-166">Á síðunni **Sniðshönnuður** skal stækka **Word** og velja **SummaryLines**.</span><span class="sxs-lookup"><span data-stu-id="45313-166">On the **Format designer** page, expand **Word**, and select **SummaryLines**.</span></span>
6. <span data-ttu-id="45313-167">Í flipanum **Vörpun** skal bæta við nýjum gagngjafa til að spyrja notendur á keyrslutíma hvort fela eigi samantektarhlutann:</span><span class="sxs-lookup"><span data-stu-id="45313-167">On the **Mapping** tab, add a new data source to ask the user, at runtime, whether the summary section should be suppressed:</span></span>

    1. <span data-ttu-id="45313-168">Veljið **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="45313-168">Select **Add root**.</span></span>
    2. <span data-ttu-id="45313-169">Í svarglugganum **Bæta við gagnagjafa** skal velja **Færibreyta slegin inn almennt\af notanda** til að opna svargluggann **Eiginleikar gagnagjafa „Innsláttarfæribreyta notanda“**.</span><span class="sxs-lookup"><span data-stu-id="45313-169">In the **Add data source** dialog box, select **General\User input parameter** to open the **'User input parameter' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="45313-170">Í reitinn **Heiti** skal færa inn **uipSuppress**.</span><span class="sxs-lookup"><span data-stu-id="45313-170">In the **Name** field, enter **uipSuppress**.</span></span>
    4. <span data-ttu-id="45313-171">Í reitinn **Merki** skal færa inn **Fela samantektarhluta**.</span><span class="sxs-lookup"><span data-stu-id="45313-171">In the **Label** field, enter **Suppress summary section**.</span></span>
    5. <span data-ttu-id="45313-172">Í reitnum **Heiti gagnaaðgerðar**, velja eða slá inn **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="45313-172">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="45313-173">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="45313-173">Select **OK**.</span></span>

7. <span data-ttu-id="45313-174">Bætið við nýjum gagnagjafa af **NoYes** upptalningargerðinni:</span><span class="sxs-lookup"><span data-stu-id="45313-174">Add a new data source of the **NoYes** application enumeration type:</span></span>

    1. <span data-ttu-id="45313-175">Veljið **Bæta við rót**.</span><span class="sxs-lookup"><span data-stu-id="45313-175">Select **Add root**.</span></span>
    2. <span data-ttu-id="45313-176">Í svarglugganum **Bæta við gagnagjafa** skal velja **Dynamics 365 for Operations\Enumeration** til að opna svargluggann **Eiginleikar gagnagjafa „upptalningar“**.</span><span class="sxs-lookup"><span data-stu-id="45313-176">In the **Add data source** dialog box, select **Dynamics 365 for Operations\Enumeration** to open the **'Enumeration' data source properties** dialog box.</span></span>
    3. <span data-ttu-id="45313-177">Í reitinn **Heiti** skal færa inn **enumNoYes**.</span><span class="sxs-lookup"><span data-stu-id="45313-177">In the **Name** field, enter **enumNoYes**.</span></span>
    4. <span data-ttu-id="45313-178">Í reitinn **Merki** skal færa inn **Fela valkosti**.</span><span class="sxs-lookup"><span data-stu-id="45313-178">In the **Label** field, enter **Suppress options**.</span></span>
    5. <span data-ttu-id="45313-179">Í reitnum **Heiti gagnaaðgerðar**, velja eða slá inn **NoYes**.</span><span class="sxs-lookup"><span data-stu-id="45313-179">In the **Operations data type name** field, select or enter **NoYes**.</span></span>
    6. <span data-ttu-id="45313-180">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="45313-180">Select **OK**.</span></span>

8. <span data-ttu-id="45313-181">Fyrir völdu sniðseininguna **SummaryLines** skal skilgreina formúluna til að tilgreina hvenær eigi að fela Word-efnisstýringuna sem tengist valdri sniðseiningu:</span><span class="sxs-lookup"><span data-stu-id="45313-181">For the selected **SummaryLines** format element, configure the formula to specify when the Word content control that is associated with the selected format element should be suppressed:</span></span>

    1. <span data-ttu-id="45313-182">Í flipanum **Vörpun**, í hlutanum **Fjarlægt**, skal velja **Breyta** til að opna síðuna **[Formúluhönnuður](general-electronic-reporting-formula-designer.md)**.</span><span class="sxs-lookup"><span data-stu-id="45313-182">On the **Mapping** tab, in the **Removed** section, select **Edit** to open the **[Formula designer](general-electronic-reporting-formula-designer.md)** page.</span></span>
    2. <span data-ttu-id="45313-183">Í reitnum **Formúla** skal færa inn formúluna `uipSuppress = enumNoYes.Yes`.</span><span class="sxs-lookup"><span data-stu-id="45313-183">In the **Formula** field, enter the formula `uipSuppress = enumNoYes.Yes`.</span></span>
    3. <span data-ttu-id="45313-184">Veljið **Vista** og lokið síðunni **Formúluhönnuður**.</span><span class="sxs-lookup"><span data-stu-id="45313-184">Select **Save**, and close the **Formula designer** page.</span></span>

        > [!NOTE]
        > <span data-ttu-id="45313-185">Þessari formúlu verður beitt á myndað skjal **þegar búið er að keyra allar aðrar sniðseiningar**.</span><span class="sxs-lookup"><span data-stu-id="45313-185">This formula will be applied to a generated document **after all other format elements are run**.</span></span> <span data-ttu-id="45313-186">Til að nota þessa formúlu finnst Word-efnisstýring sem er merkt sem sniðseining sem formúlan er skilgreind fyrir (**SummaryLines** í þessu tilfelli) í mynduðu skjali.</span><span class="sxs-lookup"><span data-stu-id="45313-186">To apply this formula, a Word content control that is tagged as a format element that the formula is configured for (**SummaryLines** in this case) is found in a generated document.</span></span> <span data-ttu-id="45313-187">Þessi efnisstýring er síðan fjarlægð að fullu ásamt línunni í Word-töflunni sem geymir hana.</span><span class="sxs-lookup"><span data-stu-id="45313-187">That content control is then completely removed, together with the row in the Word table that holds it.</span></span> <span data-ttu-id="45313-188">Upplýsingalína samantektarhlutans er fjarlægð úr mynduðu skjali.</span><span class="sxs-lookup"><span data-stu-id="45313-188">The details row of the summary section is removed from the generated document.</span></span>
        >
        > <span data-ttu-id="45313-189">Á hönnunartíma mætti skilgreina formúluna **Fjarlægt** fyrir sniðseiningu, jafnvel þótt engin efnisstýring í Word-sniðmátinu sem verið er að nota sé með merki sem passar við heiti sniðseiningarinnar sem eiginleikinn **Fjarlægt** er skilgreindur fyrir.</span><span class="sxs-lookup"><span data-stu-id="45313-189">At design time, you might configure the **Removed** formula for a format element, even though no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span> <span data-ttu-id="45313-190">Þegar sniðið er villuleitað á hönnunartíma kemur upp [viðvörun](er-components-inspections.md#i14) um þetta ósamræmi.</span><span class="sxs-lookup"><span data-stu-id="45313-190">When you validate the format at design time, you receive a [warning](er-components-inspections.md#i14) about this inconsistency.</span></span>
        >
        > <span data-ttu-id="45313-191">Við keyrslu er undantekning notuð ef engin efnisstýring í Word-sniðmátinu sem verið er að nota er með merki sem passar við heiti sniðseiningarinnar sem eiginleikinn **Fjarlægt** er skilgreindur fyrir.</span><span class="sxs-lookup"><span data-stu-id="45313-191">At runtime, an exception is thrown if no content control in the Word template that you're using has a tag that matches the name of a format element that the **Removed** property is configured for.</span></span>

    4. <span data-ttu-id="45313-192">Í flipanum **Vörpun**, í hlutanum **Fjarlægt**, skal stilla valkostinn **Með yfireiningu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="45313-192">On the **Mapping** tab, in the **Removed** section, set the **With parent** option to **Yes**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="45313-193">Stilla þarf þennan valkost á **Já** til að fjarlægja alla Word-töfluna sem hluti yfireiningar línunnar sem geymir upplýsingar um samantektarhlutann.</span><span class="sxs-lookup"><span data-stu-id="45313-193">You must set this option to **Yes** to remove the whole Word table as the parent object of the row that holds the summary section details.</span></span> <span data-ttu-id="45313-194">Ef þessi valkostur er stilltur á **Nei** verður hauslína hlutans áfram í myndaða skjalinu.</span><span class="sxs-lookup"><span data-stu-id="45313-194">If you set this option to **No**, the section header row remains in the generated document.</span></span>

9. <span data-ttu-id="45313-195">Smellið á **Vista** til að vista breytingarnar á breytanlega sniðinu.</span><span class="sxs-lookup"><span data-stu-id="45313-195">Select **Save** to save your changes to the editable format.</span></span>

    ![Myndað úttak á Word-sniði](./media/er-design-configuration-word-suppress-controls-image3.gif)

## <a name="run-the-modified-format-to-create-word-output"></a><span data-ttu-id="45313-197">Keyra breytta sniðið til að búa til Word-úttak</span><span class="sxs-lookup"><span data-stu-id="45313-197">Run the modified format to create Word output</span></span>

1. <span data-ttu-id="45313-198">Farðu í **Viðskiptaskuldir** \> **Greiðslur** \> **Greiðslubók**.</span><span class="sxs-lookup"><span data-stu-id="45313-198">Go to **Accounts payable** \> **Payments** \> **Payment journal**.</span></span>
2. <span data-ttu-id="45313-199">Veljið greiðslubókina sem var búin til og veljið síðan **Línur**.</span><span class="sxs-lookup"><span data-stu-id="45313-199">Select the payment journal that you created, and then select **Lines**.</span></span>
3. <span data-ttu-id="45313-200">Á síðunni **Greiðslur lánardrottna** skal velja allar línurnar og síðan velja **Greiðslustaða** \> **Engin**.</span><span class="sxs-lookup"><span data-stu-id="45313-200">On the **Vendor payments** page, select all the rows, and then select **Payment status** \> **None**.</span></span>
4. <span data-ttu-id="45313-201">Veldu **Búa til greiðslur**.</span><span class="sxs-lookup"><span data-stu-id="45313-201">Select **Generate payments**.</span></span>
5. <span data-ttu-id="45313-202">Í reitnum **Greiðslumáti** skal velja **Rafrænn**.</span><span class="sxs-lookup"><span data-stu-id="45313-202">In the **Method of payment** field, select **Electronic**.</span></span>
6. <span data-ttu-id="45313-203">Í reitnum **Bankareikningur** skal velja **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="45313-203">In the **Bank account** field, select **GBSI OPER**.</span></span>
7. <span data-ttu-id="45313-204">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="45313-204">Select **OK**.</span></span>
8. <span data-ttu-id="45313-205">Í svarglugganum **Rafrænar skýrslufæribreytur**, í reitnum **Fela samantektarhluta**, skal velja **Já**.</span><span class="sxs-lookup"><span data-stu-id="45313-205">In the **Electronic report parameters** dialog box, in the **Suppress summary section** field, select **Yes**.</span></span>
9. <span data-ttu-id="45313-206">Veljið **Í lagi** og skoðið myndað úttak.</span><span class="sxs-lookup"><span data-stu-id="45313-206">Select **OK**, and analyze the generated output.</span></span>

    ![Myndað úttak á Word-sniði](./media/er-design-configuration-word-suppress-controls-image4.gif)

    <span data-ttu-id="45313-208">Takið eftir að úttakið inniheldur ekki samantektarhlutann vegna þess að hann hefur verið falinn.</span><span class="sxs-lookup"><span data-stu-id="45313-208">Notice that the output doesn't contain the summary section, because it has been suppressed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="45313-209">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="45313-209">Additional resources</span></span>

- [<span data-ttu-id="45313-210">Hanna skilgreiningu til að mynda skýrslur á OPENXML-sniði</span><span class="sxs-lookup"><span data-stu-id="45313-210">Design a configuration for generating reports in OPENXML format</span></span>](./tasks/er-design-reports-openxml-2016-11.md)
- [<span data-ttu-id="45313-211">Hanna nýja skilgreiningu rafrænnar skýrslugerðar til að búa til skýrslur á Word-sniði</span><span class="sxs-lookup"><span data-stu-id="45313-211">Design a new ER configuration to generate reports in Word format</span></span>](er-design-configuration-word.md)
- [<span data-ttu-id="45313-212">Endurnýta stillingar rafrænnar skýrslugerðar með Excel-sniðmátum til að búa til skýrslur á Word-sniði</span><span class="sxs-lookup"><span data-stu-id="45313-212">Re-use ER configurations with Excel templates to generate reports in Word format</span></span>](./tasks/er-design-configuration-word-2016-11.md)
- [<span data-ttu-id="45313-213">Skoða grunnstilltan hlut rafrænnar skýrslugerðar til að koma í veg fyrir vandamál varðandi keyrslu</span><span class="sxs-lookup"><span data-stu-id="45313-213">Inspect the configured ER component to prevent runtime issues</span></span>](er-components-inspections.md#i14)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]