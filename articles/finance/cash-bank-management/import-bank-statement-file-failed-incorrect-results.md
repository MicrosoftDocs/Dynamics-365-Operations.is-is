---
title: Úrræðaleit vegna innflutnings bankayfirlitsskrár
description: Það er mikilvægt að bankayfirlitsskránni frá bankanum samsvari útliti sem Microsoft Dynamics 365 Finance styður. Vegna strangar stöðlum fyrir bankayfirlit virka flestar samþættingar rétt. Hins vegar er skrá bankayfirlits stundum ekki hægt að flytja inn eða hefur rangar niðurstöður. Venjulega er þessi vandamál valdið af lítið mismun í bankayfirlitsskránni. Þessi skrá útskýrir hvernig má laga þennan mismun og leysa úr vandamálinu.
author: panolte
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 14f0e480b93e663f81db5a1edb2ae71b559bb05e
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188561"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="9aa84-107">Úrræðaleit vegna innflutnings bankayfirlitsskrár</span><span class="sxs-lookup"><span data-stu-id="9aa84-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9aa84-108">Það er mikilvægt að bankayfirlitsskránni frá bankanum samsvari útliti sem Microsoft Dynamics 365 Finance styður.</span><span class="sxs-lookup"><span data-stu-id="9aa84-108">It's important that the bank statement file from the bank matches the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="9aa84-109">Vegna strangar stöðlum fyrir bankayfirlit virka flestar samþættingar rétt.</span><span class="sxs-lookup"><span data-stu-id="9aa84-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="9aa84-110">Hins vegar er skrá bankayfirlits stundum ekki hægt að flytja inn eða hefur rangar niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="9aa84-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="9aa84-111">Venjulega er þessi vandamál valdið af lítið mismun í bankayfirlitsskránni.</span><span class="sxs-lookup"><span data-stu-id="9aa84-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="9aa84-112">Þessi skrá útskýrir hvernig má laga þennan mismun og leysa úr vandamálinu.</span><span class="sxs-lookup"><span data-stu-id="9aa84-112">This article explains how to fix these differences and resolve the issues.</span></span>

## <a name="what-is-the-error"></a><span data-ttu-id="9aa84-113">Hver er villan?</span><span class="sxs-lookup"><span data-stu-id="9aa84-113">What is the error?</span></span>

<span data-ttu-id="9aa84-114">Þegar þú hefur reynt að flytja inn bankayfirlitsskránni, skaltu fara í vinnslusögu gagnastjórnunar og í Gögn og upplýsingar um framkvæmd til að finna villuna.</span><span class="sxs-lookup"><span data-stu-id="9aa84-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="9aa84-115">Villan getur hjálpað til með því vísa til yfirlits, stöðu eða uppgjörslínu.</span><span class="sxs-lookup"><span data-stu-id="9aa84-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="9aa84-116">Hins vegar er ólíklegt að hún veiti nægar upplýsingar til að auðvelda að auðkenna svæði eða einingu sem veldur vandamálinu.</span><span class="sxs-lookup"><span data-stu-id="9aa84-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

> [!NOTE]
> <span data-ttu-id="9aa84-117">Innflutt bankayfirlit geta aðeins skarast fyrir einn tímapunkt.</span><span class="sxs-lookup"><span data-stu-id="9aa84-117">Imported bank statements can overlap only for single a point in time.</span></span>  <span data-ttu-id="9aa84-118">Ef uppgjöri lýkur til dæmis klukkan 12:00 þann 1. janúar, 2021 þá er upphafsdagsetningin fyrir næsta uppgjör kl. 12:00 þann 1. janúar, 2021 12:00:00.</span><span class="sxs-lookup"><span data-stu-id="9aa84-118">For example, if a statement ends at 12:00 AM on January 1, 2021, then beginning date for the next statement can be 12:00 AM on Jarnuary 1, 2021 12:00:00 AM.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="9aa84-119">Hver er munurinn?</span><span class="sxs-lookup"><span data-stu-id="9aa84-119">What are the differences?</span></span>
<span data-ttu-id="9aa84-120">Berðu saman skilgreiningu útlits bankaskrár við innflutningsskilgreiningu Finance og taktu eftir öllu misræmi í reitum og einingum.</span><span class="sxs-lookup"><span data-stu-id="9aa84-120">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="9aa84-121">Berðu saman bankayfirlitsskrána við tengda sýnisskrá Finance.</span><span class="sxs-lookup"><span data-stu-id="9aa84-121">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="9aa84-122">Í ISO20022 skrárnar ætti að vera auðvelt að sjá mismun.</span><span class="sxs-lookup"><span data-stu-id="9aa84-122">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="9aa84-123">Munur á tímabelti á innfluttum bankayfirliti</span><span class="sxs-lookup"><span data-stu-id="9aa84-123">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="9aa84-124">Gildin á dagsetningunni í innflutningsskránni geta verið önnur en gildistíminn sem birtist í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9aa84-124">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="9aa84-125">Til að koma í veg fyrir þetta misræmi, sláðu inn tímabelti sem valinn er á síðunni **Stilla gagnaveitur**.</span><span class="sxs-lookup"><span data-stu-id="9aa84-125">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="9aa84-126">Frekari upplýsingar um að slá inn tímabeltisval má finna á [Setja upp þróaða innflutningsferli banka](set-up-advanced-bank-reconciliation-import-process.md).</span><span class="sxs-lookup"><span data-stu-id="9aa84-126">For more information about entering a time zone preference, see [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md).</span></span>

## <a name="transformations"></a><span data-ttu-id="9aa84-127">Umbreytingar</span><span class="sxs-lookup"><span data-stu-id="9aa84-127">Transformations</span></span>
<span data-ttu-id="9aa84-128">Yfirleitt, verður að framkvæma breytinguna í einni af þremur umbreytingum.</span><span class="sxs-lookup"><span data-stu-id="9aa84-128">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="9aa84-129">Hver umbreyting er skrifuð fyrir tiltekna staðla.</span><span class="sxs-lookup"><span data-stu-id="9aa84-129">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="9aa84-130">Nafn tilfangs</span><span class="sxs-lookup"><span data-stu-id="9aa84-130">Resource name</span></span>                                         | <span data-ttu-id="9aa84-131">Skrárnafn</span><span class="sxs-lookup"><span data-stu-id="9aa84-131">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="9aa84-132">BankStmtImport\_BAI2CSV\_í\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="9aa84-132">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="9aa84-133">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="9aa84-133">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="9aa84-134">BankStmtImport\_ISO20022XML\_í\_Afstemming\_xslt</span><span class="sxs-lookup"><span data-stu-id="9aa84-134">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="9aa84-135">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="9aa84-135">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="9aa84-136">BankStmtImport\_MT940TXT\_í\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="9aa84-136">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="9aa84-137">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="9aa84-137">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="9aa84-138">Kembing umbreytinga</span><span class="sxs-lookup"><span data-stu-id="9aa84-138">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="9aa84-139">Leiðrétta BAI2 og MT940 skrár</span><span class="sxs-lookup"><span data-stu-id="9aa84-139">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="9aa84-140">BAI2 og MT940 skrár eru skrár byggðar á texta og þarfnast leiðréttingar til að virkja kembingu Extensible Stylesheet Language-Umbreytinga (XSL-umbreyting).</span><span class="sxs-lookup"><span data-stu-id="9aa84-140">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="9aa84-141">Forritið gerir þessa leiðréttingu þegar skrá er innflutt.</span><span class="sxs-lookup"><span data-stu-id="9aa84-141">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="9aa84-142">Stofna xml-skrá, og afrita eftirfarandi texta í það.</span><span class="sxs-lookup"><span data-stu-id="9aa84-142">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="9aa84-143">Afrita innihald bankayfirlitsskrár og líma þau í xml-skrána þannig að þær skipta út **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="9aa84-143">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="9aa84-144">Kemba XSL-umbreytingu</span><span class="sxs-lookup"><span data-stu-id="9aa84-144">Debug the XSLT</span></span>

<span data-ttu-id="9aa84-145">Frekari upplýsingar er að finna í <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="9aa84-145">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="9aa84-146">Ræsa Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9aa84-146">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="9aa84-147">Stofnið nýtt stjórnborðsforrit.</span><span class="sxs-lookup"><span data-stu-id="9aa84-147">Create a console application.</span></span>
3.  <span data-ttu-id="9aa84-148">Opnið viðeigandi XSL-umbreytingu.</span><span class="sxs-lookup"><span data-stu-id="9aa84-148">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="9aa84-149">Smellt er á XLS-umbreytingu og skilgreiningarsíðu hennar.</span><span class="sxs-lookup"><span data-stu-id="9aa84-149">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="9aa84-150">Stilltu ílagið á staðsetningu bankayfirlitsskrár.</span><span class="sxs-lookup"><span data-stu-id="9aa84-150">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="9aa84-151">Skilgreina staðsetningu og skrárnafn fyrir úttak.</span><span class="sxs-lookup"><span data-stu-id="9aa84-151">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="9aa84-152">Stilltu nauðsynlega rofpunkta.</span><span class="sxs-lookup"><span data-stu-id="9aa84-152">Set the required break points.</span></span>
8.  <span data-ttu-id="9aa84-153">Á valmyndinni, smelltu á **XML** &gt; **Byrja XSLT kembingu**.</span><span class="sxs-lookup"><span data-stu-id="9aa84-153">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="9aa84-154">Sníða XLST-úttak</span><span class="sxs-lookup"><span data-stu-id="9aa84-154">Format the XSLT output</span></span>

<span data-ttu-id="9aa84-155">Þegar umbreytingin er keyrð, stofnar hún úttaksskrá sem hægt er að skoða í Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="9aa84-155">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="9aa84-156">Notið Ctrl + A, Ctrl + K og Ctrl + D til að sníða til úttaksskránni á fjótlegan hátt.</span><span class="sxs-lookup"><span data-stu-id="9aa84-156">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="9aa84-157">Stilla umbreytingu</span><span class="sxs-lookup"><span data-stu-id="9aa84-157">Adjust the transformation</span></span>

<span data-ttu-id="9aa84-158">Stilla umbreytingu til að fá viðeigandi svæði eða einingu í bankayfirlitsskránni.</span><span class="sxs-lookup"><span data-stu-id="9aa84-158">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="9aa84-159">Varpaðu svo þeim reit eða einingu á viðeigandi einingu Finance.</span><span class="sxs-lookup"><span data-stu-id="9aa84-159">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="9aa84-160">Vísir fyrir debet/kredit</span><span class="sxs-lookup"><span data-stu-id="9aa84-160">Debit/credit indicator</span></span>

<span data-ttu-id="9aa84-161">Stundum gætu debet verið flutt inn sem kredit og kredit verið flutt inn sem debet.</span><span class="sxs-lookup"><span data-stu-id="9aa84-161">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="9aa84-162">Til að leysa þetta vandamál verður að breyta viðkomandi XSL-umbreytingu.</span><span class="sxs-lookup"><span data-stu-id="9aa84-162">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="9aa84-163">Ef bankayfirlit koma úr mörgum bönkum, skal tryggja að þau noti allir sama nálgun fyrir debet/kredit, eða stofna aðskilinn umbreytingar.</span><span class="sxs-lookup"><span data-stu-id="9aa84-163">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="9aa84-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator-sniðmát</span><span class="sxs-lookup"><span data-stu-id="9aa84-164">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="9aa84-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit-sniðmát</span><span class="sxs-lookup"><span data-stu-id="9aa84-165">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="9aa84-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator-sniðmát</span><span class="sxs-lookup"><span data-stu-id="9aa84-166">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="9aa84-167">Dæmi um bankayfirlitssnið og tæknilegar útlit</span><span class="sxs-lookup"><span data-stu-id="9aa84-167">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="9aa84-168">Hér að neðan eru dæmi um skilgreiningar tæknilegs útlits fyrir innflutningsskrár ítarlegrar bankaafstemmingar og þriggja tengdum skrám bankayfirlits:</span><span class="sxs-lookup"><span data-stu-id="9aa84-168">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="9aa84-169">Þú getur hlaðið niður skáardæmum og tæknilegum útlitum hér: [Flytja inn skráardæmi](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span><span class="sxs-lookup"><span data-stu-id="9aa84-169">You can download the example files and technical layouts here: [Import file examples](//download.microsoft.com/download/8/e/c/8ec8d2d0-eb8c-41fb-ad8c-f01a4d670a44/Dynamics365FinanceAdvancedBankStatementLayouts.xlsx)</span></span>  

| <span data-ttu-id="9aa84-170">Skilgreining tæknilegs útlits</span><span class="sxs-lookup"><span data-stu-id="9aa84-170">Technical layout definition</span></span>                             | <span data-ttu-id="9aa84-171">Dæmi bankayfirlitsskránni</span><span class="sxs-lookup"><span data-stu-id="9aa84-171">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="9aa84-172">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="9aa84-172">DynamicsAXMT940Layout</span></span>                                   | [<span data-ttu-id="9aa84-173">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="9aa84-173">MT940StatementExample</span></span>](//download.microsoft.com/download/2/d/c/2dcc4e55-ddc8-4a74-b79c-250fae201c3c/mt940StatementExample.txt)                |
| <span data-ttu-id="9aa84-174">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="9aa84-174">DynamicsAXISO20022Layout</span></span>                                | [<span data-ttu-id="9aa84-175">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="9aa84-175">ISO20022StatementExample</span></span>](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdownload.microsoft.com%2Fdownload%2F1%2F5%2F5%2F155d84ed-c250-48f3-b0b1-c5a431e7855b%2FISO20022-MultipleStatements.xml&data=04%7C01%7CRobert.Schlomann%40microsoft.com%7C30d0c233cb6546547d0a08d8f4965edc%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637528273956712775%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&sdata=3VzvLZK%2BO8PjuI7XVdC6rD2j3nUJfteo7zFp%2B1s9BwM%3D&reserved=0)             |
| <span data-ttu-id="9aa84-176">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="9aa84-176">DynamicsAXBAI2Layout</span></span>                                    | [<span data-ttu-id="9aa84-177">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="9aa84-177">BAI2StatementExample</span></span>](//download.microsoft.com/download/1/1/6/11693f57-bfc1-4993-a274-5fb978be70fa/BAI2StatementExample.txt)                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
