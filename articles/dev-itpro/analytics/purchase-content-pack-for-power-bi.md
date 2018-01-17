---
title: "Efni Power BI eyðslugreining innkaupa"
description: "Þetta efnisatriði lýsir því hvað er innifalið í Power BI efninu Greining á innkaupaútgjöldum Það lýsir einnig hvernig eigi að fara í skýrslur sem eru í efnispakkanum og veitir upplýsingar um gagnalíkan og einingar sem eru notaðar til að búa til efnið."
author: FrankDahl
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 265434
ms.assetid: 3cd9dfce-2687-4303-bc78-349e7cb5ea75
ms.search.region: global
ms.author: fdahl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: aac6439bb54b3b9cab066b06c01763e880efef8e
ms.openlocfilehash: 07b6f433a8355d7f9ed6dce8e26f78d38a86a713
ms.contentlocale: is-is
ms.lasthandoff: 12/18/2017

---

# <a name="purchase-spend-analysis-power-bi-content"></a>Efni Power BI eyðslugreining innkaupa

[!include[banner](../includes/banner.md)]

Þetta efnisatriði lýsir því hvað er innifalið í Power BI efninu **Greining á innkaupaútgjöldum**. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til efnið.

## <a name="overview"></a>Yfirlit

Power BI efnið **Greining á innkaupaútgjöldum** var hannað til að auðvelda innkaupastjórum og stjórnendum sem bera ábyrgð á fjárhagsáætlunum að fylgjast með innkaupaútgjöldum. Stjórnendur geta greint útgjöld við innkaup á eftirfarandi hátt:

-   Innkaup á árinu (eftir lánardrottnaflokki og stökum lánardrottnum, innkaupategund og stökum afurðum og staðsetningu lánardrottins)
-   Breytingar á innkaupum ár frá ári (eftir lánardrottnaflokki og innkaupategund)

Efnið notast við innkaupafærslugögn og gefur bæði samantekið yfirlit yfir innkaupatölur fyrirtækisins og sundurliðun á útgjöldum við innkaup eftir lánardrottnum og afurðum. Skýrslur auðkenna breytingar í útgjöldum innkaupa yfir tíma. Þannig má nota skýrslurnar til að gera stjórnendum viðvart um jákvæða og neikvæða útgjaldaþróun fyrir einstaka lánardrottna og afurðir. Ennfremur sýna gröf innkaupaútgjöld fyrir mismunandi innkaupaflokka og lánardrottnahópa. Því geta flokka- og svæðastjórnendur notað gröfin til að finna breytingar á útgjaldahegðun.

## <a name="accessing-the-power-bi-content"></a>Farið í Power BI-efni
**Eyðslugreining innkaupa** Power BI efni er sýnt á **Greining á innkaupum og eyðslu** síðunni (**Innkaup og aðföng** > **Fyrirspurnir og skýrslur** > **Greining á innkaupaárangri** > **Greining á innkaupum og eyðslu**). 

## <a name="metrics-that-are-included-in-the-power-bi-content"></a>Mælikvarðar sem eru hafðir með í Power BI-efni
Power BI efnið **Greining á innkaupaútgjöldum** inniheldur skýrslu sem samanstendur af safni mæligilda. Þessir mælikvarðar eru birtir sem myndrit, reitir og töflur. Eftirfarandi tafla sýnir myndræna framsetningu.

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
Eftirfarandi gögn eru notuð til að fylla út skýrslusíður í Power BI efninu **Greining á innkaupaútgjöldum**. Þessi gögn eru birt sem uppsafnaðar mælingar sem stigbundnar eru í einingaversluninni. Entity-verslunin er Microsoft SQL-gagnagrunnur sem er fínstilltur fyrir greiningu. Frekari upplýsingar eru í [Yfirlit yfir samþættingu Power BI við einingaverslun](power-bi-integration-entity-store.md)

Uppsafnaðar mælingar í þessum efnispakka eru undirflokkur uppsafnaðra mælinga sem voru tiltækar í Innkaupateningi í Microsoft Dynamics AX 2012 og Microsoft Dynamics AX 2012 R3. Til að stilla uppsafnaðar mælingar tenings í einingaverslun, verður að gera þær virkjanlegir. Sjá frekari upplýsingar um ferli fyrir millistigsvigtun uppsafnaðra mælinga í einingaverslun í [Yfirlit yfir Power BI samþættingu við einingaverslun](power-bi-integration-entity-store.md). Eftirfarandi uppsafnaðar lykilmælingar eru tiltækar beint úr reikningslínueiningunni og eru grunnur þessa efnispakka.

| Eining        | Lykiluppsafnaðar mælingar | Uppruni gagna                                 | Svæði              | lýsing                            |
|---------------|----------------------------|---------------------------------------------|--------------------|----------------------------------------|
| Reikningslínur | Innkaup                   | VendInvoiceTrans                            | SAMTALA(LineAmountMST) | Upphæðin í bókhaldsgjaldmiðli. |

Eftirfarandi tafla sýnir lykilmælingarnar í efnispakkanum sem eru reiknaðar úr reikningslínueiningunni.

| Mæla               | Útreikningur                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Innkaup núverandi árs | Innkaup núverandi árs = SAMTALA ('Reikningslínur'\[Innkaupa\])                                            |
| Innkaup síðasta árs    | Innkaup síðasta ár = REIKNA (SAMTALA ('Reikningslínur'\[Innkaupa\]), SAMEPERIODLASTYEAR (Dagsetningar\[Dagsetning\])) |
| Vöxtur í innkaupum ár frá ári   | Vöxtur í innkaupum ár frá ári = \[Innkaupa núverandi árs\] – \[Innkaupa síðasta árs\]                            |

Eftirfarandi lykilvíddir í efnispakkanum eru notaðar sem síur til að sneiða uppsafnaðar mælingar þannig að hægt sé að ná meiri uppskiptingu og öðlast dýpri greiningarinnsýn.

| Eining                 | Dæmi um eigindir                                |
|------------------------|-------------------------------------------------------|
| Lánardrottnar                | Lánardrottnaflokkar, Lánardrottnaland eða -svæði, nafn Lánardrottins |
| Afurðir               | Afurðarnúmer, afurðarheiti, heiti vöruflokka        |
| Innkaupaflokkar | Innkaupategund, nöfn innkaupategunda      |
| Lögaðilar         | Heiti lögaðila                                     |
| Dagsetningar                  | Dagsetningar, Mótbókun árs                                    |

Sjálfgefið er að efnispakkinn sýni gögn fyrir núgildandi almanaksár. Hins vegar er hægt að breyta dagsetningasíunni í síuhluta skýrslu. Einnig er hægt að breyta síu fyrirtækisins.

