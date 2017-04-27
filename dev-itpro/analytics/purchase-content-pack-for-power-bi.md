---
title: "Efni Power BI eyðslugreining innkaupa"
description: "Þetta efnisatriði lýsir því hvað er innifalið í efnispakka eyðslugreiningar fyrir Microsoft Power BI. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum, og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnispakka."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-12-30 09 - 40 - 51
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 8cb928cbf1316e63a8c7de833587168cd36a455c
ms.lasthandoff: 03/29/2017


---

# <a name="purchase-spend-analysis-power-bi-content"></a>Efni Power BI eyðslugreining innkaupa

Þetta efnisatriði lýsir því hvað er innifalið í efnispakka eyðslugreiningar fyrir Microsoft Power BI. Það lýsir einnig hvernig eigi að fara í skýrslur sem eru hafðar með í efnispakkanum, og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnispakka.

<a name="overview"></a>Yfirlit
--------

Efnispakki eyðslugreiningar innkaupa fyrir Microsoft Power BI var stofnaður fyrir innkaupastjóra og stjórnendur sem bera ábyrgð á áætlunum. Hann er hannaður til að auðvelda þeim fylgjast með útgjöldum fyrir innkaup. Hann notar færslugögn innkaupa frá Microsoft Dynamics 365 for Operations og veitir bæði samanlagt yfirlit yfir innkaupatölur fyrirtækisins og sundurliðun innkaupaeyðslu eftir lánardrottni og vöru. Skýrslur auðkenna breytingar í útgjöldum innkaupa yfir tíma. Þess vegna er hægt að nota þær til að vara stjórnendur við jákvæðri og neikvæðri kostnaðarþróun fyrir einstaka lánardrottna og vörur. Myndrit sýna útgjöld innkaupa fyrir mismunandi innkaupategundir og lánardrottnaflokka. Flokks- og svæðisbundnum stjórnendum gæti þótt gagnlegt að nota þessi myndrit til að finna breytingar á eyðsluhegðun. Efnispakkinn fyrir Microsoft Power BI var stofnaður fyrir innkaupastjóra og stjórnendur sem bera ábyrgð á greiningu fjárhagsáætlana innkaupaútgjalda á eftirfarandi hátt.

-   Innkaup á árinu (eftir lánardrottnaflokki og stökum lánardrottnum, innkaupategund og stökum afurðum og staðsetningu lánardrottins)
-   Breytingar á innkaupum ár frá ári (eftir lánardrottnaflokki og innkaupategund)

## <a name="accessing-the-content-pack"></a>Farið í efnispakkann
Efnispakki eyðslugreiningar innkaupa er gefinn út sem innleiðingu eign í Microsoft Dynamics Lifecycle Services (LCS) og úr Microsoft Dynamics 365 for Operations. Nánari upplýsingar um hvernig á að fara í og opna Power BI-skýrslur er að finna í [Power BI-efni í LCS frá Microsoft og viðskiptaaðilum þínum](power-bi-content-microsoft-partners.md).

## <a name="metrics-that-are-included-in-the-content-pack"></a>Mælikvarðar sem eru hafðir með í efnispakka
Efnispakki eyðslugreiningar innkaupa inniheldur skýrslu sem samanstendur af safni mælikvarða. Þessir mælikvarðar eru birtir sem myndrit, reitir og töflur. Í eftirfarandi töflu er yfirlit yfir myndbirtingar í efnispakkanum.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Skýrslusíða</th>
<th>Gröf</th>
<th>Reitir</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Innkaup eftir lánardrottni</td>
<td><ul>
<li>Efstu 10 lánardrottnar eftir innkaupum (staflað súlurit)</li>
<li>Samtals innkaup eftir lánardrottnaflokki / landi / heiti (skífurit)</li>
<li>Innkaup eftir lánardrottnaflokki / landi / heiti (stöplarit)</li>
<li>Meðaltal innkaupa eftir lánardrottnaflokki / landi / heiti (stöplarit)</li>
</ul></td>
<td><ul>
<li>Heildarinnkaup</li>
<li>Vöxtur í innkaupum ár frá ári</li>
<li>Samtala # lánardrottna</li>
<li>Samtala # virkra lánardrottna</li>
</ul></td>
</tr>
<tr class="even">
<td>Innkaup eftir afurðum</td>
<td><ul>
<li>Innkaup eftir innkaupategund / afurðarheiti (stöplarit)</li>
<li>Heildarinnkaup eftir innkaupategund / afurðarheiti (skífurit)</li>
<li>Efstu 10 afurðir eftir innkaupum (staflað súlurit)</li>
</ul></td>
<td><ul>
<li>Samtala # afurða</li>
<li>Samtala prósentu virkra afurða af samtölu # afurða</li>
<li>Fjöldi afurða fyrir 80% innkaupa</li>
</ul></td>
</tr>
<tr class="odd">
<td>Innkaup eftir tímabili*</td>
<td><ul>
<li>Innkaup eftir mánuði / degi (stöplarit)</li>
<li>Uppsöfnuð frávik á innkaupum ár frá ári (fossarit)</li>
<li>Vöxtur í heildarinnkaupum ár frá ári (stöplarit)</li>
<li>Innkaupayfirlit (fylki)</li>
</ul></td>
<td><ul>
<li>Vöxtur í innkaupum ár frá ári</li>
<li>Ár frá ári vöxtur í innkaupum</li>
</ul></td>
</tr>
<tr class="even">
<td>Innkaupaáætlun eftir staðsetningu lánardrottins</td>
<td><ul>
<li>Innkaup eftir borg</li>
<li>Vöxtur í innkaupum ár frá ári í %</li>
<li>Innkaup eftir landi</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Eyðslugreining innkaupa eftir tíma</td>
<td><ul>
<li>Innkaup núverandi árs eftir mánuðum / degi (línurit)</li>
<li>Innkaup núverandi og síðasta árs (línu- og stöplarit)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Eyðslugreining innkaupa eftir lánardrottni</td>
<td><ul>
<li>Efstu 10 innkaup lánardrottna % innkaupa (trekt)</li>
<li>Efstu 10 lánardrottnar með aukna eyðslu ár frá ári</li>
<li>Efstu 10 lánardrottnar með minnkaða eyðslu ár frá ári</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\*Innkaup þessa árs og síðasta árs og vöxtur eftir innkaupategund

## <a name="data-model-and-entities"></a>Gagnalíkan og einingar
Gögn Dynamics 365 for Operations eru notuð fyrir skýrsluna í efnispakka eyðslugreiningar innkaupa. Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni sem Microsoft SQL-gagnagrunnur sem er fínstilltur fyrir greiningu. Sjá frekari upplýsingar um verslun Einingar í bloggfærslunni [Power BI samþættingu við einingaverslun í Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) fyrir nánari upplýsingar. Uppsafnaðar mælingar í þessum efnispakka eru undirflokkur uppsöfnaðra mælinga sem voru tiltækar í Innkaupateningur í Microsoft Dynamics AX 2012 og Microsoft Dynamics 365 for Operations 2012 R3. Til að stilla uppsafnaðar mælingar tenings í einingaverslun, verður að gera þær virkjanlegir. Sjá frekari upplýsingar um ferli fyrir sviðsetningu uppsafnaðra mælinga í verslun Einingar í bloggfærslunni [Power BI samþættingu við einingaverslun í Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) fyrir nánari upplýsingar. Eftirfarandi lykiluppsafnaðar mælingar eru tiltækar beint úr reikningslínueiningunni og eru notaðar sem grunnur að efnispakka.

| Eining        | Lykiluppsafnaðar mælingar | Gagnaveita fyrir Dynamics 365 for Operations | Svæði              | lýsing                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Línur á reikningi | Innkaup                   | VendInvoiceTrans                            | SAMTALA(LineAmountMST) | Upphæð í bókhaldsgjaldmiðli |

Eftirfarandi tafla sýnir lykilmælingarnar sem eru reiknaðar í efnispakkanum úr reikningslínueiningunni.

| Mæla               | Útreikningur                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Innkaup núverandi árs | Innkaup núverandi árs = SAMTALA ('Reikningslínur'\[Innkaupa\])                                            |
| Innkaup síðasta árs    | Innkaup síðasta ár = REIKNA (SAMTALA ('Reikningslínur'\[Innkaupa\]), SAMEPERIODLASTYEAR (Dagsetningar\[Dagsetning\])) |
| Vöxtur í innkaupum ár frá ári   | Vöxtur í innkaupum ár frá ári = \[Innkaupa núverandi árs\] – \[Innkaupa síðasta árs\]                            |

Eftirfarandi lykilvíddir í efnispakka eru notaðar sem síur til að sneiða uppsafnaðar mælingar þannig að hægt sé að ná meiri uppskiptingu og dýpri greiningarinnsýn.

| Eining                 | Dæmi um eigindir                                |
|------------------------|-------------------------------------------------------|
| Lánardrottnar                | Lánardrottnaflokkar, Lánardrottnaland eða -svæði, nafn Lánardrottins |
| Afurðir               | Afurðarnúmer, afurðarheiti, heiti vöruflokka        |
| Innkaupaflokkar | Innkaupategund, nöfn innkaupategunda      |
| Lögaðilar         | Heiti lögaðila                                     |
| Dagsetningar                  | Dagsetningar, Mótbókun árs                                    |

Sjálfgefið er að efnispakki sýni gögn fyrir núgildandi almanaksár. Hins vegar er hægt að breyta dagsetningasíunni í síuhluta skýrslu. Einnig er hægt að breyta síu fyrirtækisins.

## <a name="additional-resources"></a>Frekari upplýsingar
Hér eru gagnlegir tenglar sem tengjast einingar og að búa til Power BI-efni:

-   [Gagnaeiningar](..\data-entities\data-entities.md)
-   [Stofnun efnispakka fyrirtækis ](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gera gagnalíkön með því að nota Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Bæta Power BI-reitum við vinnusvæði](configure-power-bi-integration.md)



