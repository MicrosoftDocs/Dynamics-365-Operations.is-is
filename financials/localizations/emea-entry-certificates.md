---
title: "Færsluvottorð ESB"
description: "Þessi grein veitir upplýsingar um færsluvottorð ESB."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 11464
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 415e8ec91f3968883cb4e7ece10d8a26782bac1b
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="eu-entry-certificates"></a>Færsluvottorð ESB

[!include[banner](../includes/banner.md)]


Þessi grein veitir upplýsingar um færsluvottorð ESB.

Hægt er að ljúka eftirfarandi verkum fyrir Evrópusambandið (ESB) færsluvottorð:

-   Búa til og gefa út færsluvottor ESB með fylgiseðli eða reikningur viðskiptavinar fyrir afhendingu á vörum eða þjónustu til esb-landa/svæða.
-   Taka á móti færsluskírteini Evrópusambandið sem er undirrituð af viðskiptavinur Evrópusambandið.
-   Senda á árituð EU færsluvottorð sem borist hefur frá viðskiptavini eða þriðja aðila sem er ábyrgur fyrir afhendingu vara til viðskiptavinar.
-   Tengja uppflutt ESB-inngönguvottorð við reikning viðskiptavinar.
-   Uppfæra stöðu skírteinis sem upphlaðins EU færsluvottorðs.

## <a name="prerequisites"></a>Skilyrði
Eftirfarandi tafla sýnir forkröfur sem verður að vera til staðar áður en byrjað er.

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
<td>Land/svæði</td>
<td>Aðalaðsetur lögaðilans verður að vera í aðildarlandi Evrópusambandsins.</td>
</tr>
<tr class="even">
<td>Tengd uppsetningarverk</td>
<td><ul>
<li>Á við <strong>Færibreytur viðskiptakrafna</strong> síðunni, veljið á <strong>Virkja færsluvottorðastjórnun</strong> og <strong>Virkja útgáfu færsluvottorða</strong> valkosti.</li>
<li>Á <strong>Viðskiptavini</strong> síðunni á <strong>Reikningur og afhending</strong> flýtiflipi, veljið <strong>færsluvottorð sem er krafist</strong> valkost til að gefa til kynna að ESB færsluvottorð er áskilin fyrir viðskiptavininn. Velja skal <strong> Færsluvottorð fyrir útgáfu</strong> gátreit til að gefa út færsluvottorð ESB fyrir lögaðila til viðskiptavinar.</li>
<li>Á <strong>Færibreytur viðskiptakrafna</strong> síðunni, veljið númeraraðarkóða fyrir tilvísun <strong>Færsluvottorðs</strong> .</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tengdar færslur</td>
<td><ul>
<li>Stofna viðskiptavinalykil.</li>
<li>Stofnið sölupöntun.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a>Myndun, skráningu og upphleðslu í EU færsluvottorðs
Hægt er að stofna ESB færsluskírteini sjálfvirkt eða handvirkt. ESB-færsluvottorð er stofnað og prentað sjálfkrafa þegar þú bókar fylgiseðil eða reikning fyrir viðskiptavin í síðunni **Bókun fylgiseðils** eða **Bókun reiknings**. Til að stofna handvirkt eða endurprenta færsluvottorð ESB fyrir reikning viðskiptavinar skal nota síðuna **Reikningabók**. Þar að auki er hægt að færa inn upplýsingar um færsluvottorð ESB sem er gefið út af þriðja aðila með því að nota **Færsluvottorðabók** síðuna.

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a>Stofna ESB færsluvottorð sjálfvirkt eða handvirkt

Hægt er að stofna færsluvottorð ESB sjálfkrafa með því að nota fylgiseðil á **Allar sölupantanir** síðuna eða með því að nota reikning á **sölupöntun** síðu. Til að stofna handvirkt færsluvottorð ESB er hægt að nota reikning á **reikningabók** síðu. Hinsvegar, Breyta verður stöðu vottunar á reikningi áður en stofnaðar handvirkt færsluvottorð ESB.

### <a name="registering-an-eu-entry-certificate"></a>Skráning færsluvottorðs ESB

Ef skráning er nauðsynleg er hægt að skrá færsluvottorð ESB sem er gefið út af þriðja aðila með því að nota **Færsluvottorðabók** síðuna.

### <a name="uploading-a-received-eu-entry-certificate"></a>Hleður upp mótteknu færsluvottorði ESB

Nota skal **viðhengi** síða til að hlaða upp móttekið færsluvottorð ESB sem er undirrituð af ESB-viðskiptavinur. Þegar vottorðið er hlaðið upp er hægt að tengja það við reikningi sem sönnun á afhendingu vörunnar. Þessi sönnun er nauðsynlegt ef gefa á út reikninga sem ekki virðisaukaskattsins (VSK) og hún er einnig notuð við endurskoðun.

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a>Valfrjálst: Uppfæra vottunarstöðu reiknings og prentunarstöðu reiknings

Hægt er að uppfæra stöðu færsluvottunar og prenta stöðu á reikningi viðskiptavinar með því að nota **reikningabók** síðu.

## <a name="technical-information-for-system-administrators"></a>Tæknilegar upplýsingar sem eru ætlaðar kerfisstjórum
Ef notandi ekki aðgang að síðum sem notaðar eru til að ljúka þessu verki, skal hafa samband við kerfisstjóra og veita upplýsingar sem er sýndar í eftirfarandi töflu.

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
<td>Öryggishlutverk og skyldur</td>
<td>Til að setja upp og stofna færsluvottorð EU fyrir vörur eða þjónustu, verður að vera meðlimur öryggishlutverk sem inniheldur skyldur á eftirfarandi:
<ul>
<li><strong>Starfsmaður viðskiptakrafa</strong> (CustInvoiceAccountsReceivableClerk)</li>
<li><strong>Fulltrúi þjónustudeildar</strong> (TradeCustomerServiceRepresentative)</li>
<li><strong>Sölumaður</strong> (TradeSalesClerk)</li>
<li><strong>Starfsmaður í flutningum</strong> (InventShippingClerk)</li>
</ul></td>
</tr>
</tbody>
</table>






