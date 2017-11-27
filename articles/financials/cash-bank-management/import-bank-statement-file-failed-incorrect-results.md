---
title: "Úrræðaleit vegna innflutnings bankayfirlitsskrár"
description: "Það er mikilvægt að bankayfirlitsskráin frá bankanum samsvari útliti sem Microsoft Dynamics 365 for Finance and Operations, Enterprise edition styður. Vegna strangar stöðlum fyrir bankayfirlit virka flestar samþættingar rétt. Hins vegar er skrá bankayfirlits stundum ekki hægt að flytja inn eða hefur rangar niðurstöður. Venjulega er þessi vandamál valdið af lítið mismun í bankayfirlitsskránni. Þessi skrá útskýrir hvernig má laga þennan mismun og leysa úr vandamálinu."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 141273
ms.assetid: 3ee2f32b-02aa-420b-8990-e6aa5fc6bda3
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4feb77bf0031494dfd456c23c632a264c96f0e43
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="bank-statement-file-import-troubleshooting"></a><span data-ttu-id="3f7f4-107">Úrræðaleit vegna innflutnings bankayfirlitsskrár</span><span class="sxs-lookup"><span data-stu-id="3f7f4-107">Bank statement file import troubleshooting</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3f7f4-108">Það er mikilvægt að bankayfirlitsskráin frá bankanum samsvari útliti sem Microsoft Dynamics 365 for Finance and Operations, Enterprise edition styður.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-108">It's important that the bank statement file from the bank match the layout that Microsoft Dynamics 365 for Finance and Operations, Enterprise edition supports.</span></span> <span data-ttu-id="3f7f4-109">Vegna strangar stöðlum fyrir bankayfirlit virka flestar samþættingar rétt.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-109">Because of strict standards for bank statements, most integrations will work correctly.</span></span> <span data-ttu-id="3f7f4-110">Hins vegar er skrá bankayfirlits stundum ekki hægt að flytja inn eða hefur rangar niðurstöður.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-110">However, sometimes the statement file can't be imported or has incorrect results.</span></span> <span data-ttu-id="3f7f4-111">Venjulega er þessi vandamál valdið af lítið mismun í bankayfirlitsskránni.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-111">Typically, these issues are caused by small differences in the bank statement file.</span></span> <span data-ttu-id="3f7f4-112">Þessi skrá útskýrir hvernig má laga þennan mismun og leysa úr vandamálinu.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-112">This article explains how to fix these differences and resolve the issues.</span></span>

<a name="what-is-the-error"></a><span data-ttu-id="3f7f4-113">Hver er villan?</span><span class="sxs-lookup"><span data-stu-id="3f7f4-113">What is the error?</span></span>
------------------

<span data-ttu-id="3f7f4-114">Þegar þú hefur reynt að flytja inn bankayfirlitsskránni, skaltu fara í vinnslusögu gagnastjórnunar og í Gögn og upplýsingar um framkvæmd til að finna villuna.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-114">After you try to import a bank statement file, go to the Data management job history and its execution details to find the error.</span></span> <span data-ttu-id="3f7f4-115">Villan getur hjálpað til með því vísa til yfirlits, stöðu eða uppgjörslínu.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-115">The error can help by pointing to the statement, balance, or statement line.</span></span> <span data-ttu-id="3f7f4-116">Hins vegar er ólíklegt að hún veiti nægar upplýsingar til að auðvelda að auðkenna svæði eða einingu sem veldur vandamálinu.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-116">However, it's unlikely to provide enough information to help you identify the field or element that is causing the issue.</span></span>

## <a name="what-are-the-differences"></a><span data-ttu-id="3f7f4-117">Hver er munurinn?</span><span class="sxs-lookup"><span data-stu-id="3f7f4-117">What are the differences?</span></span>
<span data-ttu-id="3f7f4-118">Berðu saman skilgreiningu útlits bankaskrár við innflutningsskilgreiningu Finance and Operations og taktu eftir öllu misræmi í reitum og einingum.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-118">Compare the bank file layout definition to the Finance and Operations import definition, and note any differences in the fields and elements.</span></span> <span data-ttu-id="3f7f4-119">Berðu saman bankayfirlitsskrána við tengda sýnisskrá Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-119">Compare the bank statement file to the related sample Finance and Operations file.</span></span> <span data-ttu-id="3f7f4-120">Í ISO20022 skrárnar ætti að vera auðvelt að sjá mismun.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-120">In the ISO20022 files, any differences should be easy to see.</span></span>

## <a name="transformations"></a><span data-ttu-id="3f7f4-121">Umbreytingar</span><span class="sxs-lookup"><span data-stu-id="3f7f4-121">Transformations</span></span>
<span data-ttu-id="3f7f4-122">Yfirleitt, verður að framkvæma breytinguna í einni af þremur umbreytingum.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-122">Typically, the change must be made in one of three transformations.</span></span> <span data-ttu-id="3f7f4-123">Hver umbreyting er skrifuð fyrir tiltekna staðla.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-123">Each transformation is written for a specific standard.</span></span>

| <span data-ttu-id="3f7f4-124">Nafn tilfangs</span><span class="sxs-lookup"><span data-stu-id="3f7f4-124">Resource name</span></span>                                         | <span data-ttu-id="3f7f4-125">Skrárnafn</span><span class="sxs-lookup"><span data-stu-id="3f7f4-125">File name</span></span>                          |
|-------------------------------------------------------|------------------------------------|
| <span data-ttu-id="3f7f4-126">BankStmtImport\_BAI2CSV\_í\_BAI2XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="3f7f4-126">BankStmtImport\_BAI2CSV\_to\_BAI2XML\_xslt</span></span>            | <span data-ttu-id="3f7f4-127">BAI2CSV-to-BAI2XML.xslt</span><span class="sxs-lookup"><span data-stu-id="3f7f4-127">BAI2CSV-to-BAI2XML.xslt</span></span>            |
| <span data-ttu-id="3f7f4-128">BankStmtImport\_ISO20022XML\_í\_Afstemming\_xslt</span><span class="sxs-lookup"><span data-stu-id="3f7f4-128">BankStmtImport\_ISO20022XML\_to\_Reconciliation\_xslt</span></span> | <span data-ttu-id="3f7f4-129">ISO20022XML-to-Reconciliation.xslt</span><span class="sxs-lookup"><span data-stu-id="3f7f4-129">ISO20022XML-to-Reconciliation.xslt</span></span> |
| <span data-ttu-id="3f7f4-130">BankStmtImport\_MT940TXT\_í\_MT940XML\_xslt</span><span class="sxs-lookup"><span data-stu-id="3f7f4-130">BankStmtImport\_MT940TXT\_to\_MT940XML\_xslt</span></span>          | <span data-ttu-id="3f7f4-131">MT940TXT-to-MT940XML.xslt</span><span class="sxs-lookup"><span data-stu-id="3f7f4-131">MT940TXT-to-MT940XML.xslt</span></span>          |

## <a name="debugging-transformations"></a><span data-ttu-id="3f7f4-132">Kembing umbreytinga</span><span class="sxs-lookup"><span data-stu-id="3f7f4-132">Debugging transformations</span></span>
### <a name="adjust-the-bai2-and-mt940-files"></a><span data-ttu-id="3f7f4-133">Leiðrétta BAI2 og MT940 skrár</span><span class="sxs-lookup"><span data-stu-id="3f7f4-133">Adjust the BAI2 and MT940 files</span></span>

<span data-ttu-id="3f7f4-134">BAI2 og MT940 skrár eru skrár byggðar á texta og þarfnast leiðréttingar til að virkja kembingu Extensible Stylesheet Language-Umbreytinga (XSL-umbreyting).</span><span class="sxs-lookup"><span data-stu-id="3f7f4-134">The BAI2 and MT940 files are text-based files and require an adjustment to enable Extensible Stylesheet Language Transformations (XSLT) debugging.</span></span> <span data-ttu-id="3f7f4-135">Forritið gerir þessa leiðréttingu þegar skrá er innflutt.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-135">The program makes this adjustment when a file is imported.</span></span>

1.  <span data-ttu-id="3f7f4-136">Stofna xml-skrá, og afrita eftirfarandi texta í það.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-136">Create an XML file, and copy the following text into it.</span></span>

        <Batch><![CDATA[PASTESTATEMENTFILEHERE
        ]]></Batch>

2.  <span data-ttu-id="3f7f4-137">Afrita innihald bankayfirlitsskrár og líma þau í xml-skrána þannig að þær skipta út **PASTESTATEMENTFILEHERE**.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-137">Copy the contents of the bank statement file, and paste them into the XML file so that they replace **PASTESTATEMENTFILEHERE**.</span></span>

### <a name="debug-the-xslt"></a><span data-ttu-id="3f7f4-138">Kemba XSL-umbreytingu</span><span class="sxs-lookup"><span data-stu-id="3f7f4-138">Debug the XSLT</span></span>

<span data-ttu-id="3f7f4-139">Nánari upplýsingar, sjá <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-139">For more information, see <https://msdn.microsoft.com/en-us/library/ms255605.aspx>.</span></span>

1.  <span data-ttu-id="3f7f4-140">Ræsa Microsoft Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-140">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="3f7f4-141">Stofnið nýtt stjórnborðsforrit.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-141">Create a console application.</span></span>
3.  <span data-ttu-id="3f7f4-142">Opnið viðeigandi XSL-umbreytingu.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-142">Open the appropriate XSLT.</span></span>
4.  <span data-ttu-id="3f7f4-143">Smellt er á XLS-umbreytingu og skilgreiningarsíðu hennar.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-143">Click the XLST and its properties page.</span></span>
5.  <span data-ttu-id="3f7f4-144">Stilltu ílagið á staðsetningu bankayfirlitsskrár.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-144">Set the input to the location of the bank statement file.</span></span>
6.  <span data-ttu-id="3f7f4-145">Skilgreina staðsetningu og skrárnafn fyrir úttak.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-145">Define a location and file name for the output.</span></span>
7.  <span data-ttu-id="3f7f4-146">Stilltu nauðsynlega rofpunkta.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-146">Set the required break points.</span></span>
8.  <span data-ttu-id="3f7f4-147">Á valmyndinni, smelltu á **XML** &gt; **Byrja XSLT kembingu**.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-147">On the menu, click **XML** &gt; **Start XSLT Debugging**.</span></span>

### <a name="format-the-xslt-output"></a><span data-ttu-id="3f7f4-148">Sníða XLST-úttak</span><span class="sxs-lookup"><span data-stu-id="3f7f4-148">Format the XSLT output</span></span>

<span data-ttu-id="3f7f4-149">Þegar umbreytingin er keyrð, stofnar hún úttaksskrá sem hægt er að skoða í Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-149">When the transformation runs, it creates an output file that you can view in Visual Studio.</span></span> <span data-ttu-id="3f7f4-150">Notið Ctrl + A, Ctrl + K og Ctrl + D til að sníða til úttaksskránni á fjótlegan hátt.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-150">Use Ctrl+A, Ctrl+K, and Ctrl+D to quickly format the output file.</span></span>

### <a name="adjust-the-transformation"></a><span data-ttu-id="3f7f4-151">Stilla umbreytingu</span><span class="sxs-lookup"><span data-stu-id="3f7f4-151">Adjust the transformation</span></span>

<span data-ttu-id="3f7f4-152">Stilla umbreytingu til að fá viðeigandi svæði eða einingu í bankayfirlitsskránni.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-152">Adjust the transformation to get the appropriate field or element in the bank statement file.</span></span> <span data-ttu-id="3f7f4-153">Varpaðu svo þeim reit eða einingu á viðeigandi einingu Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-153">Then map that field or element to the appropriate Finance and Operations element.</span></span>

### <a name="debitcredit-indicator"></a><span data-ttu-id="3f7f4-154">Vísir fyrir debet/kredit</span><span class="sxs-lookup"><span data-stu-id="3f7f4-154">Debit/credit indicator</span></span>

<span data-ttu-id="3f7f4-155">Stundum gætu debet verið flutt inn sem kredit og kredit verið flutt inn sem debet.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-155">Sometimes, debits might be imported as credits, and credits might be imported as debits.</span></span> <span data-ttu-id="3f7f4-156">Til að leysa þetta vandamál verður að breyta viðkomandi XSL-umbreytingu.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-156">To resolve this issue, you must change the appropriate XSLT.</span></span> <span data-ttu-id="3f7f4-157">Ef bankayfirlit koma úr mörgum bönkum, skal tryggja að þau noti allir sama nálgun fyrir debet/kredit, eða stofna aðskilinn umbreytingar.</span><span class="sxs-lookup"><span data-stu-id="3f7f4-157">If bank statements come from multiple banks, make sure that they all use the same debit/credit approach, or create separate transformations.</span></span>

-   <span data-ttu-id="3f7f4-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator-sniðmát</span><span class="sxs-lookup"><span data-stu-id="3f7f4-158">BAI2XML-to-Reconciliation.xlst GetAmountCreditDebitIndicator template</span></span>
-   <span data-ttu-id="3f7f4-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit-sniðmát</span><span class="sxs-lookup"><span data-stu-id="3f7f4-159">ISO20022XML-to-Reconcilation.xslt GetCreditDebit template</span></span>
-   <span data-ttu-id="3f7f4-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator-sniðmát</span><span class="sxs-lookup"><span data-stu-id="3f7f4-160">MT940XML-to-Reconcilation.xslt GetCreditDebitIndicator template</span></span>

## <a name="examples-of-bank-statement-formats-and-technical-layouts"></a><span data-ttu-id="3f7f4-161">Dæmi um bankayfirlitssnið og tæknilegar útlit</span><span class="sxs-lookup"><span data-stu-id="3f7f4-161">Examples of bank statement formats and technical layouts</span></span>
<span data-ttu-id="3f7f4-162">Hér að neðan eru dæmi um skilgreiningar tæknilegs útlits fyrir innflutningsskrár ítarlegrar bankaafstemmingar og þriggja tengdum skrám bankayfirlits:</span><span class="sxs-lookup"><span data-stu-id="3f7f4-162">The following table lists examples of the technical layout definitions for advanced bank reconciliation import files and three related bank statement example files.</span></span> <span data-ttu-id="3f7f4-163">Þú getur sótt dæmi um skrár og tæknilegar lýsingar hingað: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span><span class="sxs-lookup"><span data-stu-id="3f7f4-163">You can download the example files and technical layouts here: https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/exofbankstfotechlayouts</span></span>  


| <span data-ttu-id="3f7f4-164">Skilgreining tæknilegs útlits</span><span class="sxs-lookup"><span data-stu-id="3f7f4-164">Technical layout definition</span></span>                             | <span data-ttu-id="3f7f4-165">Dæmi bankayfirlitsskránni</span><span class="sxs-lookup"><span data-stu-id="3f7f4-165">Bank statement example file</span></span>          |
|---------------------------------------------------------|--------------------------------------|
| <span data-ttu-id="3f7f4-166">DynamicsAXMT940Layout</span><span class="sxs-lookup"><span data-stu-id="3f7f4-166">DynamicsAXMT940Layout</span></span>                                   | <span data-ttu-id="3f7f4-167">MT940StatementExample</span><span class="sxs-lookup"><span data-stu-id="3f7f4-167">MT940StatementExample</span></span>                |
| <span data-ttu-id="3f7f4-168">DynamicsAXISO20022Layout</span><span class="sxs-lookup"><span data-stu-id="3f7f4-168">DynamicsAXISO20022Layout</span></span>                                | <span data-ttu-id="3f7f4-169">ISO20022StatementExample</span><span class="sxs-lookup"><span data-stu-id="3f7f4-169">ISO20022StatementExample</span></span>             |
| <span data-ttu-id="3f7f4-170">DynamicsAXBAI2Layout</span><span class="sxs-lookup"><span data-stu-id="3f7f4-170">DynamicsAXBAI2Layout</span></span>                                    | <span data-ttu-id="3f7f4-171">BAI2StatementExample</span><span class="sxs-lookup"><span data-stu-id="3f7f4-171">BAI2StatementExample</span></span>                 |






