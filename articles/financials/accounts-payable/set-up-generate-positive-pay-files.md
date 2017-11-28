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

# <a name="set-up-and-generate-positive-pay-files"></a>Setja upp og mynda jákvæða greiðsluskrá launa

[!include[banner](../includes/banner.md)]


Þessi skrá útskýrir hvernig á að setja upp jákvæða greiðslu og mynda jákvæðar greiðsluskrár. 

Setja upp jákvæða greiðslu til að búa til rafræna lista yfir ávísanir sem eru gefnar í banka. Þegar ávísun er innleyst í bankanum ber bankinn ávísunina saman við lista yfir ávísanir. Ef ávísunin stemmir við ávísun í listanum samþykkir bankinn ávísunina. Ef ávísunin stemmir ekki við ávísun í listanum heldur bankinn henni eftir til skoðunar.

## <a name="security-for-positive-pay-files"></a>Öryggi í jákvæðum greiðsluskrám
Jákvæðu greiðsluskránni geta innihaldið viðkvæmar upplýsingar um greiðsluþegar og upphæðir ávísunar. Þess vegna skaltu vera viss um að nota viðeigandi öryggisráðstafanir frá þeim tíma sem skrárnar eru myndaðar og þar til þær eru mótteknar í bankanum. Jákvæðum greiðsluskrám er hlaðið niður í staðsetninguna sem tilgreind er af vafranum. Vegna þess að jákvæðar greiðsluskrár geta innihaldið viðkvæmar upplýsingar, er mikilvægt að aðeins heimilaðir notendur hafi aðgang til að mynda og skoða þessar upplýsingar í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. Notið eftirfarandi töflu til að ákvarða heimildir sem krafist er.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Verkefni</th>
<th>Réttindi</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Mynda jákvæðar skrár úr listasíðunni <strong>Bankareikningar</strong> eða úr síðunni <strong>Bankareikningar</strong>.</td>
<td><ul>
<li><strong>Viðhalda upplýsingum um jákvæða greiðslu banka</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="even">
<td>Mynda jákvæðar greiðsluskrár fyrir marga lögaðila og bankareikninga úr síðunni <strong>Mynda jákvæða greiðsluskrá </strong>.</td>
<td><ul>
<li><strong>Viðhalda upplýsingum um jákvæða greiðslu banka</strong> (BankPositivePayProcess)</li>
<li><strong>BankPositivePayExportEntityView</strong> (BankPositivePayExportEntityView)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Skoða jákvæðar greiðsluskrár á síðunni <strong>Samantekt jákvæðra greiðsluskráa</strong>.</td>
<td><strong>Skoða jákvæðar greiðsluupplýsingar banka fyrir marga lögaðila</strong> (BankPositivePayView)</td>
</tr>
<tr class="even">
<td>Staðfesta jákvæða greiðsluskrá banka á síðunni <strong>Samantekt jákvæðra greiðsluskráa</strong>.</td>
<td><strong>Staðfesta jákvæða greiðsluskrá</strong> (BankPositivePayConfirm)</td>
</tr>
<tr class="odd">
<td>Afturkalla jákvæða greiðsluskrá banka á síðunni <strong>Samantekt jákvæðra greiðsluskráa</strong>.</td>
<td><strong>Afturkalla jákvæða greiðsluskrá banka</strong> (BankPositivePayRecall)</td>
</tr>
</tbody>
</table>

## <a name="set-up-a-positive-pay-format"></a>Setja upp snið jákvæðra greiðslna
Jákvæð greiðsluskrár eru stofnaðar með því að nota gagnaeiningar. Áður en hægt er að mynda jákvæða greiðsluskrá verður að setja upp umbreytingarílagssnið sem verður notað til að þýða upplýsingar um ávísunina í snið sem getur haft samskipti við bankann. Á síðunni **Jákvætt greiðslusnið** er hægt að stofna kennimerki skráarsniðs og lýsingu. Umbreytingarílagssniðið verður að vera af gerðinni XML. Tilgreint snið fer eftir þeirri breytingaskrá sem verið er að nota. Til dæmis notar sýniskráin Extensible Stylesheet Language Transformations (XSLT) sem fylgir sniðið **XML-Element**. Nota skal aðgerðina **Hlaða upp skrá fyrir umbreytingu** til að tilgreina staðsetningu umbreytingaskrár fyrir snið sem bankinn krefst.

## <a name="example-xslt-file-for-positive-pay-file"></a>Dæmi: XSLT-skrá fyrir jákvæða greiðsluskrá
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

## <a name="assign-the-positive-pay-format-to-a-bank-account"></a>Úthluta jákvæðum greiðslusniðum á bankareikning
Fyrir hvern bankareikning sem á að mynda upplýsingar um jákvæða greiðslu til, verður að úthluta jákvæða greiðslusniðinu sem tilgreint var í fyrra ferli. Á síðunni **Bankareikningar**, veljið jákvæða greiðslusniðið sem samsvarar bankareikningnum. Í svæðinu **Upphafsdagur jákvæðrar greiðslu** þarf að færa inn fyrstu dagsetningu til að mynda jákvæðar greiðsluskrár. Það er mikilvægt að dagsetning sé slegin inn í þetta svæði. Annars mun fyrsta jákvæða greiðsluskrá sem mynduð er innihalda allar ávísanir sem hafa verið stofnaðar fyrir þennan bankareikning.

## <a name="assign-a-number-sequence-for-positive-pay-files"></a>Setja upp númeraröð fyrir jákvæðar greiðsluskrár
Hver jákvæða greiðsluskrá verður að hafa einkvæmt númer. Notið flipann **Númeraraðir** á síðunni **Færibreytur reiðufjár- og bankastjórnunar** til að stofna númeraröð fyrir jákvæðar greiðsluskrár.

## <a name="generate-a-positive-pay-file-for-a-single-bank-account"></a>Mynda jákvæða greiðsluskrá fyrir stakan bankareikning
Hægt er að mynda jákvæða greiðsluskrá fyrir einn lögaðila og einn bankareikning. Til upplýsinga um hvernig á að mynda jákvæðar greiðsluskrár fyrir marga lögaðila og bankareikninga á sama tíma er vísað í næsta hluta. Til að mynda jákvæða greiðsluskrá fyrir einn lögaðila og einn bankareikning, opnið svargluggann **Mynda jákvæða greiðsluskrá** á síðunni **Bankareikningar**. Í svæðinu **Lokadagsetning**, færið inn síðustu dagsetningu ávísunar til að taka með í jákvæðri greiðsluskrá. Allar ávísanir sem ekki hafa verið með í jákvæðri greiðsluskrá fyrir þessa dagsetningu ávísunar eru í skránni.

## <a name="generate-a-positive-pay-file-for-multiple-bank-accounts"></a>Mynda jákvæða greiðsluskrá fyrir marga bankareikninga
Til að mynda jákvæðar greiðsluskrár fyrir marga bankareikninga notið reglubundna verkið **Mynda jákvæða greiðsluskrá**. Veljið snið jákvæðrar greiðslu fyrir skrána og tilgreinið hvort eigi að mynda skrá fyrir alla lögaðila eða fyrir valinn lögaðila. Einnig er hægt að mynda jákvæða greiðsluskrá fyrir alla bankareikninga sem nota tilgreinda sniðið fyrir jákvæða greiðslu eða fyrir valinn bankareikning. Í svæðinu **Lokadagsetning**, færið inn síðustu dagsetningu ávísunar til að taka með í jákvæðri greiðsluskrá. Allar ávísanir sem ekki hafa verið með í jákvæðri greiðsluskrá fyrir þessa dagsetningu ávísunar eru í skránni.

## <a name="view-the-results-of-positive-pay-file-generation"></a>Skoða niðurstöður myndunar jákvæðrar greiðsluskrár
Eftir að jákvæð greiðsluskrá er mynduð, er hægt að skoða niðurstöðurnar á síðunni **Samantekt jákvæðrar greiðsluskrár**. Til að skoða upplýsingar um einstakar ávísanir skal nota upplýsingasíðuna **Jákvæð greiðsluskrá**.

## <a name="confirm-a-positive-pay-file"></a>Staðfesta jákvæða greiðsluskrá
Eftir að búið er að greiða ávísanir sem eru talin upp í jákvæðu greiðsluskránni berst staðfestingarnúmer frá bankanum. Síðan er hægt að staðfesta jákvæðu greiðsluskrána. Á síðunni **Samantekt jákvæðrar greiðsluskrár**, veljið jákvæða greiðsluskrá sem hefur stöðuna **Stofnuð**, og veljið síðan aðgerðina **Slá inn staðfestingu**. Þegar jákvæð greiðsluskrá er staðfest er staðfestingarnúmerið sem berst frá bankanum skráð.

## <a name="recall-a-positive-pay-file"></a>Afturkalla jákvæða greiðsluskrá
Ef nauðsynlegt er að breyta jákvæðri greiðsluskrá er hægt að afturkalla hana. Á síðunni **Samantekt jákvæðrar greiðsluskrár** veljið jákvæða greiðsluskrá sem hefur stöðuna **Stofnuð**, og veljið síðan aðgerðina **Aturkalla**. Svæðið sem gefur til kynna hvort ávísun hefur verið tekin með í jákvæðri greiðsluskrá er endurstillt fyrir hverja ávísun í jákvæðu greiðsluskránni. Síðan er hægt að stofna nýja jákvæða greiðsluskrá sem inniheldur ávísunina sem var afturkölluð.




