---
title: "Efni Power BI eyðslugreining innkaupa"
description: "Þetta efnisatriði lýsir því hvað er tekin með í eyðsla analysis innihaldi pakka fyrir Microsoft Power BI. Það útskýrt hvernig á að fá aðgang að skýrslunum sem eru innifaldar í innihald þjónustupakka og upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til innihald þjónustupakka."
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

Þetta efnisatriði lýsir því hvað er tekin með í eyðsla analysis innihaldi pakka fyrir Microsoft Power BI. Það útskýrt hvernig á að fá aðgang að skýrslunum sem eru innifaldar í innihald þjónustupakka og upplýsingar um gagnalíkan og einingar sem notaðar eru til að búa til innihald þjónustupakka.

<a name="overview"></a>Yfirlit
--------

Innkaup eyðslugreining innihaldi pakka fyrir Microsoft Power BI var stofnuð fyrir innkaup stjórnendur og stjórnendum sem bera ábyrgð áætlanir. Það hefur hannað til að auðvelda þær halda við eye í útgjöldum fyrir innkaup. Það notar færslugögn innkaupa frá Microsoft Dynamics 365 aðgerða og veitir both steypa saman yfirlit fyrirtækið innkaupa tölur og sundurliðun innkaupa eyðslu eftir lánardrottni og vöru. Skýrslur auðkenna breytingar í innkaup eyðsluþök yfir tíma. Þess vegna nota má þær viðvaranir stjórnenda um leitni jákvætt og neikvætt kostnaðar við vörumerki fyrir einstaka lánardrottna og vörur. Gröf sýna innkaupapöntun útgjöldum fyrir mismunandi innkaupategundir og lánardrottnaflokka. Tegund og svæðisbundið stjórnendur gæti finnur það gagnlegt að nota þessar línurit til að aðstoða við að auðkenna breytingar í útgjöldum hegðun. Innihald þjónustupakka let's stjórnendur innkaupa og stjórnendum sem bera ábyrgð áætlanir greina innkaupa eyðsluþök á eftirfarandi hátt:

-   Innkaupum á árinu (eftir lánardrottnaflokki og einstaka lánardrottna, innkaupategund og stakar afurðir og staðsetning lánardrottins)
-   Ár of ár breyting (eftir lánardrottni flokki og innkaupa tegund)

## <a name="accessing-the-content-pack"></a>Fara í hugbúnaðarhlutartréð innihaldi pakka
Innkaup eyðslugreining innihald þjónustupakka er birt sem innleiðingu eign í Microsoft Dynamics Lifecycle Services (LCS) og úr Microsoft Dynamics 365 aðgerða. Nánari upplýsingar um hvernig aðgangur og opna Power BI skýrslur í [Power BI efni í LCS frá Microsoft og for your viðskiptaaðila](power-bi-content-microsoft-partners.md).

## <a name="metrics-that-are-included-in-the-content-pack"></a>Einingar sem eru hafðar með í innihald þjónustupakka
Innkaup eyðslugreining sem inniheldur innihald þjónustupakka skýrsla sem samanstendur af safni mælikvörðum. Þessar einingar eru visualized sem gröf reitir og töflur. Eftirfarandi tafla veitir yfirlit yfir sjóngervingum í innihald þjónustupakka.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Skýrslan síðu</th>
<th>Gröf</th>
<th>Reitir</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Innkaup eftir lánardrottni</td>
<td><ul>
<li>10 efstu lánardrottna eftir innkaupum (staflað súlurit)</li>
<li>Samtals innkaup eftir lánardrottni flokki / lands / heiti (skífurit)</li>
<li>Innkaup eftir lánardrottni flokki / lands / heiti (stöplarit)</li>
<li>Meðaltal innkaup eftir lánardrottnum flokks / lands / heiti (stöplarit)</li>
</ul></td>
<td><ul>
<li>Heildarinnkaup</li>
<li>Vöxt sölu milli ÁRA innkaupa</li>
<li>Samtals # lánardrottna</li>
<li>Samtals # virka lánardrottnar</li>
</ul></td>
</tr>
<tr class="even">
<td>Innkaup eftir afurð</td>
<td><ul>
<li>Innkaupapöntun með því að innkaupategund / afurð heiti (stöplarit)</li>
<li>Samtala innkaup eftir innkaupategund / afurð heiti (skífurit)</li>
<li>10 efstu afurðir eftir innkaupa (staflað súlurit)</li>
</ul></td>
<td><ul>
<li>Samtals # afurðir</li>
<li>Afurðir alls virka hlutfall samtölu # afurðir</li>
<li>Fjöldi afurða fyrir 80% innkaupa</li>
</ul></td>
</tr>
<tr class="odd">
<td>Kaupa eftir tímabili *</td>
<td><ul>
<li>Innkaup eftir mánuði / degi (stöplarit)</li>
<li>Frávik á sölu milli ÁRA uppsöfnuð innkaup (waterfall línurit)</li>
<li>Heildarinnkaup sölu milli ÁRA vöxt (stöplarit)</li>
<li>Yfirlit innkaupa (fylki)</li>
</ul></td>
<td><ul>
<li>Vöxt sölu milli ÁRA innkaupa</li>
<li>% Fyrir vöxt sölu milli ÁRA innkaupa</li>
</ul></td>
</tr>
<tr class="even">
<td>Innkaup eftir staðsetningu lánardrottins</td>
<td><ul>
<li>Innkaupapöntun með borg</li>
<li>Innkaupapöntun % fyrir vöxt sölu milli ÁRA</li>
<li>Innkaup eftir landi</li>
</ul></td>
<td></td>
</tr>
<tr class="odd">
<td>Eyðslugreining innkaup eftir tíma</td>
<td><ul>
<li>Innkaup núverandi árs með mánuður / degi (línurit)</li>
<li>Núverandi og síðasta ári (lína og dálka línurit)</li>
</ul></td>
<td></td>
</tr>
<tr class="even">
<td>Eyðslugreining innkaup eftir lánardrottni</td>
<td><ul>
<li>Efstu 10 lánardrottins innkaupapöntun % innkaupa (trekt)</li>
<li>10 stærstu lánardrottnar með aukinn kostnaðar við vörumerki sölu milli ÁRA</li>
<li>10 stærstu lánardrottnar með minnkað kostnaðar við vörumerki sölu milli ÁRA</li>
</ul></td>
<td></td>
</tr>
</tbody>
</table>

\*Þetta ár og síðasta ári innkaupa- og vöxt samkvæmt innkaupategund

## <a name="data-model-and-entities"></a>Gagnalíkan og einingar
Dynamics 365 fyrir Aðgerðir sem gögnin eru notuð fyrir skýrsluna í eyðslu analysis innihald þjónustupakka. Þessum gögnum er birtur sem uppsöfnuðum mælingum sem stig eru í versluninni Einingar sem er Microsoft SQL-gagnagrunnur sem er fínstillt fyrir greiningu. Sjá frekari upplýsingar um verslun Einingar í [Power BI samþættingu við Verslunina Einingar í Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blog bóka. Uppsafnaðar mælingar í þessa innihald þjónustupakka eru undirsamstæðunni uppsöfnuðum mælingum sem voru tiltæk í Innkaupateningur í Microsoft Dynamics AX 2012 og Microsoft Dynamics 365 fyrir Aðgerðir 2012 R3. Að áfangi uppsafnaðar mælingar tenings í versluninni Einingu, verður að gera þær virkjanlegir. Nánari upplýsingar, sjá ferli fyrir sviðsetningar uppsafnaðar mælingar í verslun í Einingu sem [Power BI samþættingu við Verslunina Einingar í Dynamics](https://blogs.msdn.microsoft.com/dynamicsaxbi/2016/06/09/power-bi-integration-with-entity-store-in-dynamics-ax-7-may-update/) blog bóka. Eftirfarandi lykli uppsöfnuðum mælingum tiltækar beint úr línunum einingunni Reiknings og eru notaðar sem grunnur innihald þjónustupakka.

| Eining        | Uppsafnaðar mælingar lykli | Gagnagjafi fyrir Dynamics 365 fyrir Aðgerðir | Svæði              | lýsing                           |
|---------------|----------------------------|---------------------------------------------|--------------------|---------------------------------------|
| Línur á reikningi | Innkaup                   | VendInvoiceTrans                            | SUM(LineAmountMST) | Upphæð í bókhaldsgjaldmiðli |

Eftirfarandi tafla sýnir lykill mælingarnar sem eru reiknaðar í innihald þjónustupakka úr einingunni línur Reikningsins.

| Mæla               | Útreikningur                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Innkaup núverandi ár | Innkaup ár = SAMTALA ('Reikningslínur'\[Innkaupa\])                                            |
| Innkaup síðasta árs    | Innkaup síðasta ár = REIKNA (SAMTALA ('Reikningslínur'\[Innkaupa\]), SAMEPERIODLASTYEAR (Dagsetningar\[Dagsetning\])) |
| Vöxt sölu milli ÁRA innkaupa   | Sölu milli ÁRA innkaupa vöxt = \[Innkaupa ár\] – \[Innkaupa síðasta árs\]                            |

Eftirfarandi lykils í innihald þjónustupakka eru notaðar þær víddir sem síur að sneiða uppsöfnuðum mælingum þannig að ná fleiri uppskiptingin og hærra insights greiningar.

| Eining                 | Dæmi um eigindir                                |
|------------------------|-------------------------------------------------------|
| Lánardrottnar                | Lánardrottnaflokka, Lánardrottna land eða svæði, nafn Lánardrottins |
| Afurðir               | Afurðarnúmer, afurðarheiti, vöruheiti flokka        |
| Innkaupaflokkar | Innkaupategund nöfn tegund Innkaupategund      |
| Lögaðilar         | Heiti lögaðila                                     |
| Dagsetningar                  | Dagsetningar, mótbókun Árs                                    |

Að sjálfgefnu sýnir innihald þjónustupakka gögnum fyrir núgildandi almanaksár. Hins vegar hægt að breyta dagsetningasía í hlutanum síur skýrslu. Einnig er hægt að breyta síu fyrirtækisins.

## <a name="additional-resources"></a>Frekari upplýsingar
Hér eru gagnlegir tenglar sem tengjast einingar og að búa til Power BI-efni:

-   [Gagnaeiningar](..\data-entities\data-entities.md)
-   [Stofnun efnispakka fyrirtækis ](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
-   [Gera gagnalíkön með því að nota Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
-   [Bæta Power BI-reitum við vinnusvæði](configure-power-bi-integration.md)



