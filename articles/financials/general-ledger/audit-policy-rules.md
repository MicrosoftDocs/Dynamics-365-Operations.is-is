---
title: "Reglur endurskoðunarstefnu"
description: "Hægt er að nota endurskoðunarreglur til að meta kostnaðarskýrslur, reikninga lánardrottna og innkaupapantanir til að tryggja að þeir samræmast stefnureglur sem eru stofnaðar. Allar reglur sem eru tengd við endurskoðunarstefnu eru rekin í runuham, samkvæmt áætlun sem þú tilgreinir.  Hver stefnuregla er tilvik af stefnureglugerð. Fyrir hverja stefnureglugerð aðeins einn stefnureglu getur verið virk í einu."
author: ryansandness
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AuditPolicyAdditionalOption, AuditPolicyRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12991
ms.assetid: 8d787017-71dc-418f-b8c2-4ea9763d9978
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 04217e162090720d2a48c96aa9356cea2dbfa230
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="audit-policy-rules"></a>Reglur endurskoðunarstefnu

[!INCLUDE [banner](../includes/banner.md)]

Hægt er að nota endurskoðunarreglur til að meta kostnaðarskýrslur, reikninga lánardrottna og innkaupapantanir til að tryggja að þeir samræmast stefnureglur sem eru stofnaðar. Allar reglur sem eru tengd við endurskoðunarstefnu eru rekin í runuham, samkvæmt áætlun sem þú tilgreinir.  Hver stefnuregla er tilvik af stefnureglugerð. Fyrir hverja stefnureglugerð aðeins einn stefnureglu getur verið virk í einu. 

<a name="queries-and-query-types"></a>Fyrirspurnir og gerðir fyrirspurna
-----------------------

Þegar regla endurskoðunarstefnu er stofnuð þarf fyrst að velja stefnureglugerð. Gerð reglu tilgreinir fyrirspurn Hugbúnaðarhlutatrénu (AOT) til að nota sem upphafspunkt fyrir þá reglu. Það skilgreinir einnig fyrirspurn ferðar til nota fyrir stefnureglu. Fyrirspurnin ákvarðar upprunaskjalið sem metur síðan til stefnuregluna. Það skilgreinir einnig reiti í upprunaskjali sem auðkenna bæði lögaðila og dagsetningu til að nota þegar skjöl eru valin til endurskoðunar. Gerð fyrirspurnar stýrir sjálfgefið svæði í fyrirspurnarskjámynd og í síðunni regla endurskoðunarstefnu. Eftirfarandi tafla sýnir gerðir fyrirspurn sem er tiltækt fyrir reglur endurskoðunarstefnu.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Gerð fyrirspurnar</th>
<th>Tilgangur</th>
<th>Frekari upplýsingar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Skilyrðisbundið</td>
<td>Meta uppruna eigindir skjals gagnvart tilgreindum gildum.</td>
<td></td>
</tr>
<tr class="even">
<td>Samanlagt</td>
<td>Meta margar upprunaskjöl eða línur upprunaskjals gagnvart stefnureglu með söfnun tölulegt gildi.</td>
<td></td>
</tr>
<tr class="odd">
<td>Sýnishorn</td>
<td>Veljið handahófi tilgreindri prósentu af upprunaskjöl til að meta brot á reglum.</td>
<td>Þegar þessi valkostur er valinn, skaltu nota síðuna regla endurskoðunarstefnu til að tilgreina hlutfall skjala til að velja af handahófi fyrir endurskoðun.</td>
</tr>
<tr class="even">
<td>Afrita</td>
<td>Meta upprunaskjöl til að ákvarða hvort þau innihalda tvíteknar færslur í tilgreindu svæðin.</td>
<td>Þegar þessi valkostur er valinn, skaltu nota síðuna regla endurskoðunarstefnu til að tilgreina fjölda daga til að bæta við upphaf dagsetningabils skjalavals þegar skjöl eru metin fyrir tvíteknar færslur.</td>
</tr>
<tr class="odd">
<td>Listaleit</td>
<td>Meta upprunaskjöl fyrir tilteknar einingar.</td>
<td>Rót skjalið fyrirspurnarinnar tilgreinir skjalið sem er endurskoðuð. Fyrirspurnin verður að vera listafyrirspurn sem inniheldur tilvísun í the dirpartytable-töflu. Hægt er að nota þennan valkost aðeins með eftirfarandi fyrirspurnir AOT:
<ul>
<li><span class="ui">AuditPolicyExpenseList</span> (Kostnaðarskýrsla vaktaðra starfsmanna)</li>
<li><span class="ui">AuditPolicyPurchList</span> (Innkaupapöntun vaktaðra lánardrottna)</li>
<li><span class="ui">AuditPolicyVendInvoiceList</span> (reikningur vaktaðra lánardrottna)</li>
</ul>
Þegar þessi valkostur er valinn skal tilgreina vaktaðar einingar í síðunni regla endurskoðunarstefnu.</td>
</tr>
<tr class="even">
<td>Lykilorðaleit</td>
<td>Meta upprunaskjöl til að ákvarða hvort þau innihalda tiltekin orð.</td>
<td>Þegar þessi valkostur er valinn skal færa inn orð til að leita að í regla endurskoðunarstefnu síða. regla endurskoðunarstefnu síða  inniheldur einnig valkosti sem leyfa þér að tilgreina töflur og reiti til að meta fyrir orð sem þú slóst inn.</td>
</tr>
</tbody>
</table>

## <a name="common-parameters"></a>Algengar færibreytur
Allar stefnureglur um tiltekna endurskoðunarstefnu deila sömu runufæribreytur og sama dagsetningarbil skjalavals. Þessar færibreytur eru tilgreindar fyrir reglu í á Aukavalkostir síða.



<a name="see-also"></a>Sjá einnig
--------

[Brot á endurskoðunarstefnu og tilvik](audit-policy-violations-cases.md)
[Skilgreina endurskoðunarstefnu fyrir upprunaskjöl](tasks/define-audit-policies-source-documents.md)



