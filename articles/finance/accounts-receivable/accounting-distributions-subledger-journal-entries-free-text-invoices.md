---
title: Um bókhaldsfærslur dreifingar og færslur í færslubók fyrir reikningur með frjálsum texta
description: Dreifingar á fjárhagsupphæð eru notaðar til að skilgreina hvernig gert verður grein fyrir upphæð, eins og hvernig gert verður grein fyrir tekjur, skatta eða gjöld á reikningi með frjálsum texta Hver upphæð sem verður að gera grein fyrir þegar reikningur með frjálsum texta er skráður mun hafa eina eða fleiri dreifingar á fjárhagsupphæð.
author: ShivamPandey-msft
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 3141
ms.assetid: fecd17a2-d7b4-4a20-ac81-eb71abbfa9d1
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7e3e1e0a757dcd51edcd38bb348e52b756e57334
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188759"
---
# <a name="accounting-distributions-and-subledger-entries-for-free-text-invoices"></a>Um bókhaldsfærslur dreifingar og undirbókar færslna fyrir reikninga með frjálsum texta

[!include [banner](../includes/banner.md)]

Dreifingar á fjárhagsupphæð eru notaðar til að skilgreina hvernig gert verður grein fyrir upphæð, eins og hvernig gert verður grein fyrir tekjur, skatta eða gjöld á reikningi með frjálsum texta Hver upphæð sem verður að gera grein fyrir þegar reikningur með frjálsum texta er skráður mun hafa eina eða fleiri dreifingar á fjárhagsupphæð.

## <a name="accounting-distributions"></a>Dreifing á fjárhagsupphæðum

Hægt er að nota eftirfarandi hnappanna í reikningur með frjálsum texta síðunni reikningur lánardrottins til að skoða og mögulega breyta, dreifingar á fjárhagsupphæð síða fyrir hverja upphæð á reikningur með frjálsum texta.

-   **Dreifa fjárhæðir**— Skoða og breyta dreifingum á fjárhagsupphæð fyrir einstakar línur og allar undirlínur, svo sem skatta eða gjöld. Einnig er hægt að skoða og breyta dreifingar á fjárhagsupphæð fyrir línu undirstig beint í frá síðunni VSK-færsla eða síðunni Gjaldfærslur.
    -   Breyta upphæðum í haus reikningur með frjálsum texta, svo sem gjöldum eða sléttuðum gjaldeyrisupphæðum.
    -   Breyta upphæðum í reikningi með frjálsum texta.
-   **Skoða dreifingu** - Skoða dreifingu á fjárhagsupphæð fyrir allar línur skjals. Ekki er hægt að breyta dreifingu fjárhagsupphæða í þessu yfirliti.
    -   Skoða hausupplýsingar og línuupphæðir.

## <a name="distributing-amounts"></a>Dreifing upphæða
Þegar reikningur með frjálsum texta verður hverri upphæð dreift á eftirfarandi hátt.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Gerð peningaupphæðar</th>
<th>Hvaðan aðallykill er birtur</th>
<th>Forgangsröð sem ákvarðar hvaða fjárhagsvídd sjálfgefna er birt</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Lína Reiknings með frjálsum texta</td>
<td>Fjárhagslykill á reikningur með frjálsum texta.</td>
<td><ol>
<li>Ef aðallykils er úthlutunarlykill er að nota sjálfgefna gildið úr skilgreiningu úthlutunar lykil.</li>
<li>Ef aðallykils er ekki úthlutunarlykill, notið sjálfgefin sniðmát fjárhagsvídda á línu í reikningur með frjálsum texta.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda á reikningur með frjálsum texta.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda frá fjárhagslykill í síðu bókhaldslykils.</li>
</ol></td>
</tr>
<tr class="even">
<td>Lína Reiknings með frjálsum texta fyrir eignarnúmer og samsetningu virðislíkans
<div class="alert">
<table>
<thead>
<tr class="header">
<th><strong>Ábending</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Aðallykillinn í línu reiknings með frjálsum texta verður afskráningarlykill eigna.</td>
</tr>
</tbody>
</table>
</div></td>
<td>Fjárhagslykill á reikningur með frjálsum texta.</td>
<td><ol>
<li>Nota sjálfgefin gildi fjárhagsvídda á reikningur með frjálsum texta.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda frá fjárhagslykill í síðu bókhaldslykils.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Afsláttarupphæð Reiknings með frjálsum texta</td>
<td>Aðallykill fyrir svæði afsláttar viðskiptavina í síðunni staðgreiðsluafslættir.</td>
<td><ol>
<li>Ef aðallykils er úthlutunarlykill er að nota sjálfgefna gildið úr skilgreiningu úthlutunar lykil.</li>
<li>Ef aðallykils er ekki úthlutunarlykill, notið sjálfgefin sniðmát fjárhagsvídda á línu í reikningur með frjálsum texta.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda á reikningur með frjálsum texta.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda frá fjárhagslykill í síðu bókhaldslykils.</li>
</ol></td>
</tr>
<tr class="even">
<td>Upphæð virðisaukaskatts á reikningur með frjálsum texta</td>
<td>Reiturinn VSK-til greiðslu í fjárhagsbókunarflokki síðu.</td>
<td><ol>
<li>Nota fjárhagsvíddiir sem eru skilgreindar á upphæð reiknings með frjálsum texta eða dreifingum fyrir upphæð gjaldlínunnar.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda á reikningur með frjálsum texta.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda frá fjárhagslykill í síðu bókhaldslykils.</li>
</ol></td>
</tr>
<tr class="odd">
<td>Upphæð gjaldlínu á reikningur með frjálsum texta</td>
<td>Svæði kreditlykils á síðunni Gjaldakóðar.</td>
<td><ol>
<li>Ef aðallykils er úthlutunarlykill er að nota sjálfgefna gildið úr skilgreiningu úthlutunar lykil.</li>
<li>Ef aðallykils er ekki úthlutunarlykill, notið sjálfgefin sniðmát fjárhagsvídda á línu í reikningur með frjálsum texta.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda á reikningur með frjálsum texta.</li>
<li>Nota sjálfgefin gildi fjárhagsvídda frá fjárhagslykill í síðu bókhaldslykils.</li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="distributing-taxes"></a>Dreifing skatta
Ekki er hægt að stofna dreifingu á fjárhagsupphæð fyrr en skattar hafa verið reiknaðir. Til að reikna virðisaukaskatt, verður að ljúka einu af eftirtöldum verkefnum í skjámyndinni reikningur með frjálsum texta:
-   Skoða VSK.
-   Skoða samtölu reiknings.
-   Skoða sjóðstreymi.
-   Skoða dreifingu á fjárhagsupphæðum fyrir allan reikning með frjálsum texta.
-   Skoða færslubók undirfjárhags.

## <a name="subledger-journals-for-free-text-invoices"></a>Færslubækur undirfjárhags fyrir reikninga með frjálsum texta
Áður en þú bóka reikningur með frjálsum texta, er hægt að skoða fulla bókhaldsfærslu, sem felur í sér skuldfærslu og inneignir, til að staðfesta að reikningurinn sé sendur til réttra reikninga. Þetta yfirlit yfir alla lykilfærslu kallast færslubók undirfjárhags. Ef færsla í undirbók er röng þegar hún er forskoðuð áður en reikningur með frjálsum texta eru skráðar, er hægt að breyta færslu í undirbók. Þess í stað verður þú að breyta dreifingu á fjárhagsupphæð eða bókunarreglu. Fjárhagsupphæðum er notuð til að skilgreina einni hlið lykilfærslu, debet eða kredit. Mótfærsla lykilfærslu í undirbókarlykil er stofnuð með því að nota bókunarreglur, eins og úr viðskiptavinalykli eða skatti.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]