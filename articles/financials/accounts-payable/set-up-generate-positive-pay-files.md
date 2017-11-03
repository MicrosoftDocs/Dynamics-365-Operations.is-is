---
title: "Setja upp og mynda jákvæða greiðsluskrá launa"
description: "Þessi skrá útskýrir hvernig á að setja upp jákvæða greiðslu og mynda jákvæðar greiðsluskrár."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 88433
ms.assetid: 73f3dcf6-040a-44ad-9512-7b3e0d17a571
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 28a8c7b739ecd991c6dc4934e379e3a2810f0240
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-and-generate-positive-pay-files"></a><span data-ttu-id="152df-103">Setja upp og mynda jákvæða greiðsluskrá launa</span><span class="sxs-lookup"><span data-stu-id="152df-103">Set up and generate positive pay files</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="152df-104">Þessi skrá útskýrir hvernig á að setja upp jákvæða greiðslu og mynda jákvæðar greiðsluskrár.</span><span class="sxs-lookup"><span data-stu-id="152df-104">This article explains how to set up positive pay and generate positive pay files.</span></span> 

<span data-ttu-id="152df-105">Setja upp jákvæða greiðslu til að búa til rafræna lista yfir ávísanir sem eru gefnar í banka.</span><span class="sxs-lookup"><span data-stu-id="152df-105">Set up positive pay to generate an electronic list of checks that is provided to the bank.</span></span> <span data-ttu-id="152df-106">Þegar ávísun er innleyst í bankanum ber bankinn ávísunina saman við lista yfir ávísanir.</span><span class="sxs-lookup"><span data-stu-id="152df-106">Then, when a check is presented to the bank, the bank compares it with the list of checks.</span></span> <span data-ttu-id="152df-107">Ef ávísunin stemmir við ávísun í listanum samþykkir bankinn ávísunina.</span><span class="sxs-lookup"><span data-stu-id="152df-107">If the check matches a check in the list, the bank clears it.</span></span> <span data-ttu-id="152df-108">Ef ávísunin stemmir ekki við ávísun í listanum heldur bankinn henni eftir til skoðunar.</span><span class="sxs-lookup"><span data-stu-id="152df-108">If the check doesn't match a check in the list, the bank holds it for review.</span></span>

## <a name="security-for-positive-pay-files"></a><span data-ttu-id="152df-109">Öryggi í jákvæðum greiðsluskrám</span><span class="sxs-lookup"><span data-stu-id="152df-109">Security for positive pay files</span></span>
<span data-ttu-id="152df-110">Jákvæðu greiðsluskránni geta innihaldið viðkvæmar upplýsingar um greiðsluþegar og upphæðir ávísunar.</span><span class="sxs-lookup"><span data-stu-id="152df-110">Positive pay files can contain sensitive information about payees and check amounts.</span></span> <span data-ttu-id="152df-111">Þess vegna skaltu vera viss um að nota viðeigandi öryggisráðstafanir frá þeim tíma sem skrárnar eru myndaðar og þar til þær eru mótteknar í bankanum.</span><span class="sxs-lookup"><span data-stu-id="152df-111">Therefore, make sure that you use appropriate security measures from the time that the files are generated until they are received by the bank.</span></span> <span data-ttu-id="152df-112">Jákvæðum greiðsluskrám er hlaðið niður í staðsetninguna sem tilgreind er af vafranum.</span><span class="sxs-lookup"><span data-stu-id="152df-112">Positive pay files are downloaded to the location that is specified by your web browser.</span></span> <span data-ttu-id="152df-113">Vegna þess að jákvæðar greiðsluskrár geta innihaldið viðkvæmar upplýsingar, er mikilvægt að aðeins heimilaðir notendur hafi aðgang til að mynda og skoða þessar upplýsingar í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="152df-113">Because positive pay files can contain sensitive information, it's important that only authorized users have access to generate and view this information in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="152df-114">Notið eftirfarandi töflu til að ákvarða heimildir sem krafist er.</span><span class="sxs-lookup"><span data-stu-id="152df-114">Use the following table to help you determine the privileges that are required.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="152df-115">Verkefni</span><span class="sxs-lookup"><span data-stu-id="152df-115">Task</span></span></th>
<th><span data-ttu-id="152df-116">Réttindi</span><span class="sxs-lookup"><span data-stu-id="152df-116">Privilege</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="152df-117">Mynda jákvæðar skrár úr listasíðunni <strong>Bankareikningar</strong> eða úr síðunni <strong>Bankareikningar</strong>.</span><span class="sxs-lookup"><span data-stu-id="152df-117">Generate positive pay files from the <strong>Bank accounts</strong> list page or the <strong>Bank accounts</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="152df-118"><strong>Viðhalda upplýsingum um jákvæða greiðslu banka</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="152df-118"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="152df-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="152df-119"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="152df-120">Mynda jákvæðar greiðsluskrár fyrir marga lögaðila og bankareikninga úr síðunni <strong>Mynda jákvæða greiðsluskrá </strong>.</span><span class="sxs-lookup"><span data-stu-id="152df-120">Generate positive pay files for multiple legal entities and bank accounts from the <strong>Generate a positive pay file</strong> page.</span></span></td>
<td><ul>
<li><span data-ttu-id="152df-121"><strong>Viðhalda upplýsingum um jákvæða greiðslu banka</strong> (BankPositivePayProcess)</span><span class="sxs-lookup"><span data-stu-id="152df-121"><strong>Maintain bank positive pay information</strong> (BankPositivePayProcess)</span></span></li>
<li><span data-ttu-id="152df-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span><span class="sxs-lookup"><span data-stu-id="152df-122"><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="152df-123">Skoða jákvæðar greiðsluskrár á síðunni <strong>Samantekt jákvæðra greiðsluskráa</strong>.</span><span class="sxs-lookup"><span data-stu-id="152df-123">View positive pay files on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="152df-124"><strong>Skoða jákvæðar greiðsluupplýsingar banka fyrir marga lögaðila</strong> (BankPositivePayView)</span><span class="sxs-lookup"><span data-stu-id="152df-124"><strong>View bank positive pay information for multiple legal entities</strong> (BankPositivePayView)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="152df-125">Staðfesta jákvæða greiðsluskrá banka á síðunni <strong>Samantekt jákvæðra greiðsluskráa</strong>.</span><span class="sxs-lookup"><span data-stu-id="152df-125">Confirm a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="152df-126"><strong>Staðfesta jákvæða greiðsluskrá</strong> (BankPositivePayConfirm)</span><span class="sxs-lookup"><span data-stu-id="152df-126"><strong>Confirm positive payment file</strong> (BankPositivePayConfirm)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="152df-127">Afturkalla jákvæða greiðsluskrá banka á síðunni <strong>Samantekt jákvæðra greiðsluskráa</strong>.</span><span class="sxs-lookup"><span data-stu-id="152df-127">Recall a bank positive pay file on the <strong>Positive pay file summary</strong> page.</span></span></td>
<td><span data-ttu-id="152df-128"><strong>Afturkalla jákvæða greiðsluskrá banka</strong> (BankPositivePayRecall)</span><span class="sxs-lookup"><span data-stu-id="152df-128"><strong>Recall positive pay file</strong> (BankPositivePayRecall)</span></span></td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a><span data-ttu-id="152df-129">Setja upp snið jákvæðra greiðslna</span><span class="sxs-lookup"><span data-stu-id="152df-129">Set up a positive pay format</span></span>
<span data-ttu-id="152df-130">Jákvæð greiðsluskrár eru stofnaðar með því að nota gagnaeiningar.</span><span class="sxs-lookup"><span data-stu-id="152df-130">Positive pay files are created by using data entities.</span></span> <span data-ttu-id="152df-131">Áður en hægt er að mynda jákvæða greiðsluskrá verður að setja upp umbreytingarílagssnið sem verður notað til að þýða upplýsingar um ávísunina í snið sem getur haft samskipti við bankann.</span><span class="sxs-lookup"><span data-stu-id="152df-131">Before you can generate a positive pay file, you must set up a transformation input format that will be used to translate the check information into a format that can communicate with the bank.</span></span> <span data-ttu-id="152df-132">Á síðunni **Jákvætt greiðslusnið** er hægt að stofna kennimerki skráarsniðs og lýsingu.</span><span class="sxs-lookup"><span data-stu-id="152df-132">On the **Positive pay format** page, you can create a file format identifier and a description.</span></span> <span data-ttu-id="152df-133">Umbreytingarílagssniðið verður að vera af gerðinni XML.</span><span class="sxs-lookup"><span data-stu-id="152df-133">The transformation input format must be of the XML type.</span></span> <span data-ttu-id="152df-134">Tilgreint snið fer eftir þeirri breytingaskrá sem verið er að nota.</span><span class="sxs-lookup"><span data-stu-id="152df-134">The specific format depends on the transformation file that you're using.</span></span> <span data-ttu-id="152df-135">Til dæmis notar sýniskráin Extensible Stylesheet Language Transformations (XSLT) sem fylgir sniðið **XML-Element**.</span><span class="sxs-lookup"><span data-stu-id="152df-135">For example, the sample Extensible Stylesheet Language Transformations (XSLT) file that is provided uses the **XML-Element** format.</span></span> <span data-ttu-id="152df-136">Nota skal aðgerðina **Hlaða upp skrá fyrir umbreytingu** til að tilgreina staðsetningu umbreytingaskrár fyrir snið sem bankinn krefst.</span><span class="sxs-lookup"><span data-stu-id="152df-136">Use the **Upload file used for transformation** action to specify the location of the transform file for the format that your bank requires.</span></span>

## <a name="example-xslt-file-for-positive-pay-file"></a><span data-ttu-id="152df-137">Dæmi: XSLT-skrá fyrir jákvæða greiðsluskrá</span><span class="sxs-lookup"><span data-stu-id="152df-137">Example: XSLT file for positive pay file</span></span>
    <xsl:stylesheet version="1.0" xmlns:xsl="http://www.w3.org/1999/XSL/Transform" xmlns:msxsl="urn:schemas-microsoft-com:xslt" exclude-result-prefixes="msxsl xslthelper" xmlns="urn:iso:std:iso:20022:tech:xsd:pain.001.001.02" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xslthelper="http://schemas.microsoft.com/BizTalk/2003/xslthelper">
      <xsl:output method="xml" omit-xml-declaration="no" version="1.0" encoding="utf-8"/>
      <xsl:template match="/">
        <xsl:value-of select="'
    '" />
        <Document>
          <xsl:value-of select="'
    '" />
          <!--Header Begin-->
          <xsl:value-of select='string("Vendor ID,Vendor Name,Voided,Document Type,Check Date,Check Number,Check Amount,Checkbook ID,Vendor Class ID,Posted Date")'/>
          <xsl:value-of select="'
    '" />
          <!--Header End-->
          <xsl:for-each select="Document/BankPositivePayExportEntity">
            <!--Cheque Detail begin-->
            <xsl:value-of select='RECIPIENTACCOUNTNUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='BANKNEGINSTRECIPIENTNAME/text()'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Void") or CHEQUESTATUS/text()=normalize-space("Rejected") or CHEQUESTATUS/text()=normalize-space("Cancelled")'>
                <xsl:value-of select='string("Yes")'/>
              </xsl:when>
              <xsl:when test='CHEQUESTATUS/text()=normalize-space("Payment")'>
                <xsl:value-of select='string("No")'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='string(" ")'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("Payment")'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='CHEQUENUM/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='AMOUNTCUR/text()'/>
            <xsl:value-of select="','" />
            <xsl:value-of select='string("BOA-#1812")'/>
            <xsl:value-of select="','" />
            <xsl:choose>
              <xsl:when test='RECIPIENTTYPE/text()=normalize-space("Vend")'>
                <xsl:value-of select='VENDGROUP/text()'/>
              </xsl:when>
              <xsl:otherwise>
                <xsl:value-of select='CUSTGROUP/text()'/>
              </xsl:otherwise>
            </xsl:choose>
            <xsl:value-of select="','" />
            <xsl:value-of select='TRANSDATE/text()'/>
            <xsl:value-of select="'
    '" />
          </xsl:for-each>
        </Document>
      </xsl:template>
    </xsl:stylesheet>

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a><span data-ttu-id="152df-138">Úthluta jákvæðum greiðslusniðum á bankareikning</span><span class="sxs-lookup"><span data-stu-id="152df-138">Assign the positive pay format to a bank account</span></span>
<span data-ttu-id="152df-139">Fyrir hvern bankareikning sem á að mynda upplýsingar um jákvæða greiðslu til, verður að úthluta jákvæða greiðslusniðinu sem tilgreint var í fyrra ferli.</span><span class="sxs-lookup"><span data-stu-id="152df-139">For each bank account that you want to generate positive pay information for, you must assign the positive pay format that you specified in the previous section.</span></span> <span data-ttu-id="152df-140">Á síðunni **Bankareikningar**, veljið jákvæða greiðslusniðið sem samsvarar bankareikningnum.</span><span class="sxs-lookup"><span data-stu-id="152df-140">On the **Bank accounts** page, select the positive pay format that corresponds to the bank account.</span></span> <span data-ttu-id="152df-141">Í svæðinu **Upphafsdagur jákvæðrar greiðslu** þarf að færa inn fyrstu dagsetningu til að mynda jákvæðar greiðsluskrár.</span><span class="sxs-lookup"><span data-stu-id="152df-141">In the **Positive pay start date** field, enter the first date to generate positive pay files.</span></span> <span data-ttu-id="152df-142">Það er mikilvægt að dagsetning sé slegin inn í þetta svæði.</span><span class="sxs-lookup"><span data-stu-id="152df-142">It's important that you enter a date in this field.</span></span> <span data-ttu-id="152df-143">Annars mun fyrsta jákvæða greiðsluskrá sem mynduð er innihalda allar ávísanir sem hafa verið stofnaðar fyrir þennan bankareikning.</span><span class="sxs-lookup"><span data-stu-id="152df-143">Otherwise, the first positive pay file that you generate will include all checks that have ever been created for this bank account.</span></span>

## <a name="assign-a-number-sequence-for-positive-pay-files"></a><span data-ttu-id="152df-144">Setja upp númeraröð fyrir jákvæðar greiðsluskrár</span><span class="sxs-lookup"><span data-stu-id="152df-144">Assign a number sequence for positive pay files</span></span>
<span data-ttu-id="152df-145">Hver jákvæða greiðsluskrá verður að hafa einkvæmt númer.</span><span class="sxs-lookup"><span data-stu-id="152df-145">Each positive pay file must have a unique number.</span></span> <span data-ttu-id="152df-146">Notið flipann **Númeraraðir** á síðunni **Færibreytur reiðufjár- og bankastjórnunar** til að stofna númeraröð fyrir jákvæðar greiðsluskrár.</span><span class="sxs-lookup"><span data-stu-id="152df-146">Use the **Number sequences** tab on the **Cash and bank management parameters** page to create a number sequence for positive pay files.</span></span>

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a><span data-ttu-id="152df-147">Mynda jákvæða greiðsluskrá fyrir stakan bankareikning</span><span class="sxs-lookup"><span data-stu-id="152df-147">Generate a positive pay file for a single bank account</span></span>
<span data-ttu-id="152df-148">Hægt er að mynda jákvæða greiðsluskrá fyrir einn lögaðila og einn bankareikning.</span><span class="sxs-lookup"><span data-stu-id="152df-148">You can generate a positive pay file for a single legal entity and a single bank account.</span></span> <span data-ttu-id="152df-149">Til upplýsinga um hvernig á að mynda jákvæðar greiðsluskrár fyrir marga lögaðila og bankareikninga á sama tíma er vísað í næsta hluta.</span><span class="sxs-lookup"><span data-stu-id="152df-149">For information about how to generate positive pay files for multiple legal entities and bank accounts at the same time, see the next section.</span></span> <span data-ttu-id="152df-150">Til að mynda jákvæða greiðsluskrá fyrir einn lögaðila og einn bankareikning, opnið svargluggann **Mynda jákvæða greiðsluskrá** á síðunni **Bankareikningar**.</span><span class="sxs-lookup"><span data-stu-id="152df-150">To generate a positive pay file for a single legal entity and a single bank account, open the **Generate a positive pay file** dialog box from the **Bank accounts** page.</span></span> <span data-ttu-id="152df-151">Í svæðinu **Lokadagsetning**, færið inn síðustu dagsetningu ávísunar til að taka með í jákvæðri greiðsluskrá.</span><span class="sxs-lookup"><span data-stu-id="152df-151">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="152df-152">Allar ávísanir sem ekki hafa verið með í jákvæðri greiðsluskrá fyrir þessa dagsetningu ávísunar eru í skránni.</span><span class="sxs-lookup"><span data-stu-id="152df-152">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a><span data-ttu-id="152df-153">Mynda jákvæða greiðsluskrá fyrir marga bankareikninga</span><span class="sxs-lookup"><span data-stu-id="152df-153">Generate a positive pay file for multiple bank accounts</span></span>
<span data-ttu-id="152df-154">Til að mynda jákvæðar greiðsluskrár fyrir marga bankareikninga notið reglubundna verkið **Mynda jákvæða greiðsluskrá**.</span><span class="sxs-lookup"><span data-stu-id="152df-154">To generate a positive pay file for multiple bank accounts, use the **Generate a positive pay file** periodic task.</span></span> <span data-ttu-id="152df-155">Veljið snið jákvæðrar greiðslu fyrir skrána og tilgreinið hvort eigi að mynda skrá fyrir alla lögaðila eða fyrir valinn lögaðila.</span><span class="sxs-lookup"><span data-stu-id="152df-155">Select the positive pay format for the file, and specify whether to generate the file for all legal entities or for a selected legal entity.</span></span> <span data-ttu-id="152df-156">Einnig er hægt að mynda jákvæða greiðsluskrá fyrir alla bankareikninga sem nota tilgreinda sniðið fyrir jákvæða greiðslu eða fyrir valinn bankareikning.</span><span class="sxs-lookup"><span data-stu-id="152df-156">You can also generate the positive pay file for all bank accounts that use the specified positive pay format or for a selected bank account.</span></span> <span data-ttu-id="152df-157">Í svæðinu **Lokadagsetning**, færið inn síðustu dagsetningu ávísunar til að taka með í jákvæðri greiðsluskrá.</span><span class="sxs-lookup"><span data-stu-id="152df-157">In the **Cut-off date** field, enter the last check date to include in the positive pay file.</span></span> <span data-ttu-id="152df-158">Allar ávísanir sem ekki hafa verið með í jákvæðri greiðsluskrá fyrir þessa dagsetningu ávísunar eru í skránni.</span><span class="sxs-lookup"><span data-stu-id="152df-158">All checks that haven’t been included in a positive pay file by the end of this check date are included in the file.</span></span>

## <a name="view-the-results-of-positive-pay-file-generation"></a><span data-ttu-id="152df-159">Skoða niðurstöður myndunar jákvæðrar greiðsluskrár</span><span class="sxs-lookup"><span data-stu-id="152df-159">View the results of positive pay file generation</span></span>
<span data-ttu-id="152df-160">Eftir að jákvæð greiðsluskrá er mynduð, er hægt að skoða niðurstöðurnar á síðunni **Samantekt jákvæðrar greiðsluskrár**.</span><span class="sxs-lookup"><span data-stu-id="152df-160">After the positive pay file is generated, you can view the results on the **Positive pay file summary** page.</span></span> <span data-ttu-id="152df-161">Til að skoða upplýsingar um einstakar ávísanir skal nota upplýsingasíðuna **Jákvæð greiðsluskrá**.</span><span class="sxs-lookup"><span data-stu-id="152df-161">To view the details of the individual checks, use the **Positive pay file** details page.</span></span>

## <a name="confirm-a-positive-pay-file"></a><span data-ttu-id="152df-162">Staðfesta jákvæða greiðsluskrá</span><span class="sxs-lookup"><span data-stu-id="152df-162">Confirm a positive pay file</span></span>
<span data-ttu-id="152df-163">Eftir að búið er að greiða ávísanir sem eru talin upp í jákvæðu greiðsluskránni berst staðfestingarnúmer frá bankanum.</span><span class="sxs-lookup"><span data-stu-id="152df-163">After the checks that are listed in a positive pay file have been paid, you receive a confirmation number from your bank.</span></span> <span data-ttu-id="152df-164">Síðan er hægt að staðfesta jákvæðu greiðsluskrána.</span><span class="sxs-lookup"><span data-stu-id="152df-164">You can then confirm the positive pay file.</span></span> <span data-ttu-id="152df-165">Á síðunni **Samantekt jákvæðrar greiðsluskrár**, veljið jákvæða greiðsluskrá sem hefur stöðuna **Stofnuð**, og veljið síðan aðgerðina **Slá inn staðfestingu**.</span><span class="sxs-lookup"><span data-stu-id="152df-165">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Enter confirmation** action.</span></span> <span data-ttu-id="152df-166">Þegar jákvæð greiðsluskrá er staðfest er staðfestingarnúmerið sem berst frá bankanum skráð.</span><span class="sxs-lookup"><span data-stu-id="152df-166">When you confirm a positive pay file, the confirmation number that you received from the bank is recorded.</span></span>

## <a name="recall-a-positive-pay-file"></a><span data-ttu-id="152df-167">Afturkalla jákvæða greiðsluskrá</span><span class="sxs-lookup"><span data-stu-id="152df-167">Recall a positive pay file</span></span>
<span data-ttu-id="152df-168">Ef nauðsynlegt er að breyta jákvæðri greiðsluskrá er hægt að afturkalla hana.</span><span class="sxs-lookup"><span data-stu-id="152df-168">If you must change a positive pay file, you can recall it.</span></span> <span data-ttu-id="152df-169">Á síðunni **Samantekt jákvæðrar greiðsluskrár** veljið jákvæða greiðsluskrá sem hefur stöðuna **Stofnuð**, og veljið síðan aðgerðina **Aturkalla**.</span><span class="sxs-lookup"><span data-stu-id="152df-169">On the **Positive pay file summary** page, select a positive pay file that has a status of **Created**, and then select the **Recall** action.</span></span> <span data-ttu-id="152df-170">Svæðið sem gefur til kynna hvort ávísun hefur verið tekin með í jákvæðri greiðsluskrá er endurstillt fyrir hverja ávísun í jákvæðu greiðsluskránni.</span><span class="sxs-lookup"><span data-stu-id="152df-170">For each check in the positive pay file, the field that indicates whether that check has been included in a positive pay file is reset.</span></span> <span data-ttu-id="152df-171">Síðan er hægt að stofna nýja jákvæða greiðsluskrá sem inniheldur ávísunina sem var afturkölluð.</span><span class="sxs-lookup"><span data-stu-id="152df-171">You can then create a new positive pay file that includes the check that was recalled.</span></span>




