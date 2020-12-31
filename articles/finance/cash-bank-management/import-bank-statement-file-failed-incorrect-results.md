---
title: Úrræðaleit vegna innflutnings bankayfirlitsskrár
description: Það er mikilvægt að bankayfirlitsskránni frá bankanum samsvari útliti sem Microsoft Dynamics 365 Finance styður. Vegna strangar stöðlum fyrir bankayfirlit virka flestar samþættingar rétt. Hins vegar er skrá bankayfirlits stundum ekki hægt að flytja inn eða hefur rangar niðurstöður. Venjulega er þessi vandamál valdið af lítið mismun í bankayfirlitsskránni. Þessi skrá útskýrir hvernig má laga þennan mismun og leysa úr vandamálinu.
author: panolte
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankStatementFormat
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 09b24b88ee5f8104aabd11397d5bd2745e846cb0
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444261"
---
# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="5cfa3-107">Úrræðaleit vegna innflutnings bankayfirlitsskrár</span><span class="sxs-lookup"><span data-stu-id="5cfa3-107">Bank statement file import troubleshooting</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5cfa3-108">Það er mikilvægt að bankayfirlitsskránni frá bankanum samsvari útliti sem Microsoft Dynamics 365 Finance styður.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 Finance supports.</span></span> <span data-ttu-id="5cfa3-109">Vegna strangar stöðlum fyrir bankayfirlit virka flestar samþættingar rétt.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="5cfa3-110">Hins vegar er skrá bankayfirlits stundum ekki hægt að flytja inn eða hefur rangar niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="5cfa3-111">Venjulega er þessi vandamál valdið af lítið mismun í bankayfirlitsskránni.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="5cfa3-112">Þessi skrá útskýrir hvernig má laga þennan mismun og leysa úr vandamálinu.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="5cfa3-113">Hver er villan?</span><span class="sxs-lookup"><span data-stu-id="5cfa3-113">What is the error?</span></span>
------------------

<span data-ttu-id="5cfa3-114">Þegar þú hefur reynt að flytja inn bankayfirlitsskránni, skaltu fara í vinnslusögu gagnastjórnunar og í Gögn og upplýsingar um framkvæmd til að finna villuna.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="5cfa3-115">Villan getur hjálpað til með því vísa til yfirlits, stöðu eða uppgjörslínu.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="5cfa3-116">Hins vegar er ólíklegt að hún veiti nægar upplýsingar til að auðvelda að auðkenna svæði eða einingu sem veldur vandamálinu.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="5cfa3-117">Hver er munurinn?</span><span class="sxs-lookup"><span data-stu-id="5cfa3-117">What are the differences?</span></span>
<span data-ttu-id="5cfa3-118">Berðu saman skilgreiningu útlits bankaskrár við innflutningsskilgreiningu Finance og taktu eftir öllu misræmi í reitum og einingum.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-118">Compare the bank file layout definition to the Finance import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="5cfa3-119">Berðu saman bankayfirlitsskrána við tengda sýnisskrá Finance.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-119">Compare the bank statement file to the related sample Finance file.</span></span> <span data-ttu-id="5cfa3-120">Í ISO20022 skrárnar ætti að vera auðvelt að sjá mismun.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="time-zone-differences-on-imported-bank-statements"></a><span data-ttu-id="5cfa3-121">Munur á tímabelti á innfluttum bankayfirliti</span><span class="sxs-lookup"><span data-stu-id="5cfa3-121">Time zone differences on imported bank statements</span></span>
<span data-ttu-id="5cfa3-122">Gildin á dagsetningunni í innflutningsskránni geta verið önnur en gildistíminn sem birtist í Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-122">The date-time values in the import file can differ from the date-time values that are shown in Finance and Operations.</span></span> <span data-ttu-id="5cfa3-123">Til að koma í veg fyrir þetta misræmi, sláðu inn tímabelti sem valinn er á síðunni **Stilla gagnaveitur**.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-123">To prevent this discrepancy, enter a time zone preference on the **Configure data sources** page.</span></span> <span data-ttu-id="5cfa3-124">Sjáðu [Setja upp þróaða innflutningsferli banka](set-up-advanced-bank-reconciliation-import-process.md) til að fá frekari upplýsingar um að slá inn tímabeltisval.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-124">See [Set up the advanced bank reconciliation import process](set-up-advanced-bank-reconciliation-import-process.md) for more information about entering a time zone preference.</span></span>

## <a name="transformations"></a><span data-ttu-id="5cfa3-125">Umbreytingar</span><span class="sxs-lookup"><span data-stu-id="5cfa3-125">Transformations</span></span>
<span data-ttu-id="5cfa3-126">Yfirleitt, verður að framkvæma breytinguna í einni af þremur umbreytingum.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-126">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="5cfa3-127">Hver umbreyting er skrifuð fyrir tiltekna staðla.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-127">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="5cfa3-128">Nafn tilfangs</span><span class="sxs-lookup"><span data-stu-id="5cfa3-128">Resource name</span></span>                                         | <span data-ttu-id="5cfa3-129">Skrárnafn</span><span class="sxs-lookup"><span data-stu-id="5cfa3-129">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="5cfa3-130">BankStmtImport\_BAI2CSV\_í\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="5cfa3-130">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="5cfa3-131">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="5cfa3-131">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="5cfa3-132">BankStmtImport\_ISO20022XML\_í\_Afstemming\_xslt</span><span class="sxs-lookup"><span data-stu-id="5cfa3-132">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="5cfa3-133">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="5cfa3-133">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="5cfa3-134">BankStmtImport\_MT940TXT\_í\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="5cfa3-134">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="5cfa3-135">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="5cfa3-135">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="5cfa3-136">Kembing umbreytinga</span><span class="sxs-lookup"><span data-stu-id="5cfa3-136">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="5cfa3-137">Leiðrétta BAI2 og MT940 skrár</span><span class="sxs-lookup"><span data-stu-id="5cfa3-137">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="5cfa3-138">BAI2 og MT940 skrár eru skrár byggðar á texta og þarfnast leiðréttingar til að virkja kembingu Extensible Stylesheet Language-Umbreytinga (XSL-umbreyting).</span><span class="sxs-lookup"><span data-stu-id="5cfa3-138">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="5cfa3-139">Forritið gerir þessa leiðréttingu þegar skrá er innflutt.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-139">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="5cfa3-140">Stofna xml-skrá, og afrita eftirfarandi texta í það.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-140">Create an XML file, and copy the following text into it.</span></span>

    ```xml
    <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>
    ```
    
2.  <span data-ttu-id="5cfa3-141">Afrita innihald bankayfirlitsskrár og líma þau í xml-skrána þannig að þær skipta út **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-141">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="5cfa3-142">Kemba XSL-umbreytingu</span><span class="sxs-lookup"><span data-stu-id="5cfa3-142">Debug the XSLT</span></span>

<span data-ttu-id="5cfa3-143">Frekari upplýsingar er að finna í <https://msdn.microsoft.com/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-143">For more information, see <https://msdn.microsoft.com/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="5cfa3-144">Ræsa Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-144">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="5cfa3-145">Stofnið nýtt stjórnborðsforrit.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-145">Create a console application.</span></span>
3.  <span data-ttu-id="5cfa3-146">Opnið viðeigandi XSL-umbreytingu.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-146">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="5cfa3-147">Smellt er á XLS-umbreytingu og skilgreiningarsíðu hennar.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-147">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="5cfa3-148">Stilltu ílagið á staðsetningu bankayfirlitsskrár.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-148">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="5cfa3-149">Skilgreina staðsetningu og skrárnafn fyrir úttak.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-149">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="5cfa3-150">Stilltu nauðsynlega rofpunkta.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-150">Set the required break points.</span></span>
8.  <span data-ttu-id="5cfa3-151">Á valmyndinni, smelltu á **XML** &gt; **Byrja XSLT kembingu**.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-151">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="5cfa3-152">Sníða XLST-úttak</span><span class="sxs-lookup"><span data-stu-id="5cfa3-152">Format the XSLT output</span></span>

<span data-ttu-id="5cfa3-153">Þegar umbreytingin er keyrð, stofnar hún úttaksskrá sem hægt er að skoða í Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-153">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="5cfa3-154">Notið Ctrl + A, Ctrl + K og Ctrl + D til að sníða til úttaksskránni á fjótlegan hátt.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-154">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="5cfa3-155">Stilla umbreytingu</span><span class="sxs-lookup"><span data-stu-id="5cfa3-155">Adjust the transformation</span></span>

<span data-ttu-id="5cfa3-156">Stilla umbreytingu til að fá viðeigandi svæði eða einingu í bankayfirlitsskránni.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-156">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="5cfa3-157">Varpaðu svo þeim reit eða einingu á viðeigandi einingu Finance.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-157">Then map that field or element to the appropriate Finance element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="5cfa3-158">Vísir fyrir debet/kredit</span><span class="sxs-lookup"><span data-stu-id="5cfa3-158">Debit/credit indicator</span></span>

<span data-ttu-id="5cfa3-159">Stundum gætu debet verið flutt inn sem kredit og kredit verið flutt inn sem debet.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-159">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="5cfa3-160">Til að leysa þetta vandamál verður að breyta viðkomandi XSL-umbreytingu.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-160">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="5cfa3-161">Ef bankayfirlit koma úr mörgum bönkum, skal tryggja að þau noti allir sama nálgun fyrir debet/kredit, eða stofna aðskilinn umbreytingar.</span><span class="sxs-lookup"><span data-stu-id="5cfa3-161">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="5cfa3-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator-sniðmát</span><span class="sxs-lookup"><span data-stu-id="5cfa3-162">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="5cfa3-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit-sniðmát</span><span class="sxs-lookup"><span data-stu-id="5cfa3-163">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="5cfa3-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator-sniðmát</span><span class="sxs-lookup"><span data-stu-id="5cfa3-164">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="5cfa3-165">Dæmi um bankayfirlitssnið og tæknilegar útlit</span><span class="sxs-lookup"><span data-stu-id="5cfa3-165">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="5cfa3-166">Hér að neðan eru dæmi um skilgreiningar tæknilegs útlits fyrir innflutningsskrár ítarlegrar bankaafstemmingar og þriggja tengdum skrám bankayfirlits:</span><span class="sxs-lookup"><span data-stu-id="5cfa3-166">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="5cfa3-167">Þú getur hlaðið niður skáardæmum og tæknilegum útlitum hér: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="5cfa3-167">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="5cfa3-168">Skilgreining tæknilegs útlits</span><span class="sxs-lookup"><span data-stu-id="5cfa3-168">Technical layout definition</span></span>                             | <span data-ttu-id="5cfa3-169">Dæmi bankayfirlitsskránni</span><span class="sxs-lookup"><span data-stu-id="5cfa3-169">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="5cfa3-170">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="5cfa3-170">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="5cfa3-171">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="5cfa3-171">MT940StatementExample</span></span>                |
| <span data-ttu-id="5cfa3-172">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="5cfa3-172">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="5cfa3-173">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="5cfa3-173">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="5cfa3-174">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="5cfa3-174">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="5cfa3-175">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="5cfa3-175">BAI2StatementExample</span></span>                 |





