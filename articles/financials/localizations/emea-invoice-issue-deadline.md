---
title: Tímamörk útgáfu reiknings
description: Þessi grein útskýrir hvernig á að setja upp færibreytur til að reikna út gjalddaga fyrir útgáfu reikninga viðskiptavina og reikninga lánardrottins innan Evrópusambandsins (ESB).
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, LedgerInvoiceIssueDueDateSetup_W
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 10923
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Iceland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 701519dcc2cf27b73fd6861a21e49cef5a80f50c
ms.sourcegitcommit: 16bfa0fd08feec1647829630401ce62ce2ffa1a4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/02/2019
ms.locfileid: "1852227"
---
# <a name="invoice-issue-deadline"></a>Tímamörk útgáfu reiknings

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að setja upp færibreytur til að reikna út gjalddaga fyrir útgáfu reikninga viðskiptavina og reikninga lánardrottins innan Evrópusambandsins (ESB).

Tilskipun Evrópusambandsins (ESB) nr. 45/2010 og aðrar tilskipanir krefjast þess að sendingar innan Evrópusambandsins verður að reikningsfæra fimmtánda dags mánaðarins eftir að afhending er gerð, eða á undan þeim degi. Á sama tíma getur hvert land innan ESB haft mismunandi tímamörk reikningsfærlsu fyrir innlendar afhendingar. Gjalddagavirkni útgáfu reiknings gera kleift að jafna dagsetningabil við gerð lands/svæðis. Síðan, fyrir allar sendingar til og frá landi/svæði af tiltekinni gerð, er gjalddagi útgáfu reiknings reiknuð með því að nota reglur sem eru settar á tilteknu dagsetningabili. Þar að auki er hægt að fá alla fylgiseðla sem hafa tiltekinn gjalddaga útgáfu reiknings, sía eftir gjalddaga útgáfu reiknings við reglubundna sölureikninga og stýra útgáfudagsetningu sölureikninga við bókun reiknings. Þú getur sett upp kóða dagsetningabils, og síðan sett upp útreikningsreglu fyrir útgáfudag reiknings með því að úthluta kóða dagsetningabils til lands-/ svæðistegundar. Útreikningur regla er notuð til að reikna út gjalddaga til að gefa út reikninga fyrir eftirfarandi færslur:

-   Sendingar innan ESB
-   Innlendar sendingar innan aðildarríkis ESB

Einnig er hægt að setja upp dagsetningarstýringar til að tryggja að reikningar viðskiptavina og kreditnótur fyrir færslur viðskiptavinar séu mynduð innan tilgreinds tímabils eftir að afhending fer fram.

## <a name="prerequisites"></a>Skilyrði
Eftirfarandi tafla sýnir forkröfur sem verður að vera til staðar áður en hægt er að nota gjalddagavirkni útgáfu reiknings.

| Tegund            | Skilyrði                                                                                                                                                                                                                                                                                                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Land/svæði      | Aðalaðsetur lögaðilans verður að vera í aðildarlandi Evrópusambandsins.                                                                                                                                                                                                                                                                                                                    |
| Tengd uppsetningarverk | Á síðunni **Dagsetningabil** seturðu upp dagsetningabil sem eru notuð til að reikna út gjalddaga útgáfu reiknings. (Smellt er á **Fjárhagur** &gt; **Uppsetning fjárhags** &gt; **Dagsetningabil**.) Á síðunni **Færibreytur erlendra viðskipta** seturðu upp eiginleika erlendra viðskipta fyrir ýmis lönd/svæði. (Smellt er á **Skattur** &gt; **Uppsetning** &gt; **Erlend viðskipti** &gt; **Færibreytur erlendra viðskipta**.) |

## <a name="invoice-issue-due-date-calculation-rule"></a>Reikna gjalddaga fyrir útgáfu reiknings
Nota skal **Setja upp útreikning á útgáfu reiknings gjalddaga** til að setja upp útreikningsreglu fyrir útgáfudag reiknings með því að úthluta kóða dagsetningabils til lands-/ svæðistegundar.

## <a name="date-control-parameters-for-customer-invoices-and-credit-notes"></a>Færibreytur til að stjórna dagsetningum fyrir reikninga viðskiptavina og inneignarnótur
Hægt er að setja upp færibreytur dagsetningarstýringar til að tryggja að reikningar viðskiptavina og kreditnótur fyrir færslur viðskiptavinar séu mynduð innan tilgreinds tímabils eftir að afhending fer fram. Hægt er að finna þessar færibreytur á svæðinu **Stýring reikningsdagsetninga** á síðunni **Færibreytur viðskiptakrafna**.

## <a name="example"></a>Dæmi
Til að setja upp Microsoft Dynamics 365 for Finance and Operations til að reikna út gjalddaga reikningsútgáfu fyrir sendingar innan ESB fimmtánda dag næsta mánaðar eftir að framboðið er afhent, skal stofna dagsetningarbilskóða og útreikning reglu við eftirfarandi stillingar.

### <a name="date-interval-code"></a>Kóði dagsetningabils

| Reitur                                                           | Gildi                           |
|-----------------------------------------------------------------|---------------------------------|
| Kóði dagsetningabils                                              | 15 NM                           |
| Lýsing                                                     | Fimmtándi dagur næsta mánaðar |
| Á undan (í reitahópnum **Til dagsetningar**)                         | Mánuður                           |
| Byrjun/Lok (í reitahópunum **Til dagsetningar**)                      | Við skil                             |
| +/- (í reitahópnum **Til dagsetningar**)                            | 15                              |
| Dagar, mánuðir, ár eða tímabil (í reitahópnum **Til dagsetningar**) | Dagar                            |

### <a name="invoice-issue-due-date-calculation-rule"></a>Reikna gjalddaga fyrir útgáfu reiknings

| Reitur               | Gildi                                                     |
|---------------------|-----------------------------------------------------------|
| Gerð lands/svæðis | **ESB**                                                    |
| Upphafsdagsetning          | Færið inn dagsetninguna þegar núgildandi uppsetning línu tekur gildi. |
| Kóði dagsetningabils  | **15 NM**                                                 |

## <a name="next-steps"></a>Næstu skref
Eftir að þú hefur lokið við að setja upp færibreytur til að reikna gjalddaga útgáfu reikninga getur þú stofnað og bókað eftirfarandi færslur til að sjálfkrafa reikna og uppfæra gjalddaga fyrir útgáfu reikninga:

-   **sölupöntun** - Þegar þú býrð til sölupantanir og senda fylgiseðill, gjalddagi á útgáfu reiknings er reiknað og uppfærð á fylgiseðill. Gjalddagi er reiknaður á grundvelli dagsetningabilsins sem er tengt því landi/svæði sem er tilgreint í afhendingaraðsetri sölupöntunar. Eftir að fylgiseðill er bókaður er hægt að staðfesta gjalddaga útgáfu reiknings í reitnum **Gjalddagi útgáfu reiknings** á síðunni **Færslubók fylgiseðla**. (Smellt er á **Sala og markaðssetning** &gt; **Sölupöntun** &gt; **Afhending pöntunar** &gt; **Fylgiseðill**.) Hægt er að skoða alla fylgiseðla sem eru ekki reikningsfærðir og gjalddaga útgáfu reiknings þeirra á síðunni **Fylgiseðlar ekki reikningsfærðir**. (Smellt er á **Sala og markaðssetning** &gt; **Sölupöntun** &gt; **Afhending pöntunar** &gt; **Fylgiseðlar ekki reikningsfærðir**.)
-   **innkaupapöntun** - Þegar þú býrð til innkaupapöntun og senda innhreyfingarskjal afurða, er gjalddagi á útgáfu reiknings er reiknað og uppfærð á innhreyfingarskjal afurða. Gjalddagi er reiknaður á grundvelli tímabilsins sem er tengt því landi/svæði sem er tilgreint í aðalaðsetri lánardrottins. Eftir að innhreyfingarskjal afurða er bókað er hægt að staðfesta gjalddaga útgáfu reiknings í reitnum **Gjalddagi útgáfu reiknings** á síðunni **Færslubók innhreyfingarskjals afurða**. (Smellt er á **Innkaup og aðföng** &gt; **Innkaupapantanir** &gt; **Móttaka afurða** &gt; **Innhreyfingarskjal afurða**.) Hægt er að skoða öll innhreyfingarskjöl afurða sem eru ekki reikningsfærð og gjalddaga útgáfu reiknings þeirra á síðunni **Innhreyfingarskjöl afurða ekki reikningsfærð**. (Smellt er á **Innkaup og aðföng** &gt; **Innkaupapantanir** &gt; **Móttaka afurða** &gt; **Innhreyfingarskjöl afurða ekki reikningsfærð**.)

## <a name="technical-information-for-system-administrators"></a>Tæknilegar upplýsingar sem eru ætlaðar kerfisstjórum
Ef notandi hefur ekki aðgang að síðum sem notaðar eru til að ljúka verkum sem eru nefnd í þessari grein skal hafa samband við kerfisstjóra og veita þær upplýsingar sem er sýndar í eftirfarandi töflu.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tegund</th>
<th>Skilyrði</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Skilgreiningarlyklar</td>
<td>Smellt er á <strong>Kerfisstjórnun</strong> &gt; <strong>Uppsetning</strong> &gt; <strong>Leyfi</strong> &gt; <strong>Skilgreining leyfis</strong>. Smelltu á skilgreiningarlykilinn <strong>Fjárhagur</strong>.</td>
</tr>
<tr class="even">
<td>Öryggishlutverk og skyldur</td>
<td>Til að framkvæma þetta verk, verður að vera meðlimur öryggishlutverk sem inniheldur skyldur á eftirfarandi:
<ul>
<li><strong>CustInvoiceInvoiceAndCashProcessEnable</strong> (Virkja Reikningar og aðgerðir reiðufés)</li>
<li><strong>VendInvoiceInvoicePaymentProcessEnable</strong> (Virkja reiknings- og greiðsluferlið)</li>
</ul></td>
</tr>
<tr class="odd">
<td>öryggishlutverk og réttindi</td>
<td>Til að framkvæma þetta verk, verður að vera meðlimur öryggishlutverk sem felur í sér réttindi sem eftirfarandi:
<ul>
<li><strong>CustPackingSlipJournalView</strong> (Skoða sölufylgiseðla)</li>
<li><strong>VendPackingSlipJournalView</strong> (Skoða færslubók innhreyfingarskjala afurða úr innkaupapöntun)</li>
<li><strong>LedgerInvoiceIssueDueDateSetupMaintain_W</strong> (eikna gjalddaga fyrir útgáfu reiknings)</li>
</ul></td>
</tr>
</tbody>
</table>





