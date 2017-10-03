---
title: "virkni uppskriftahönnuðar"
description: "Þessi grein lýsir því hvernig þú getur notað hönnuð uppskriftar til að hanna og vinna með uppskriftatréskipulag (BOM). Hægt er smella á uppsetningu til að velja ólíkar skilgreiningar og tilgreina hvaða upplýsingar á að sýna í línum trésins."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMDesigner
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 20981
ms.assetid: 2b92eec1-d28c-4965-9086-939c77b3c62b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: c871cf4e5ee7f359010aac1fa0fef81e0e0df564
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017

---

# <a name="bom-designer-functionality"></a>virkni uppskriftahönnuðar

[!include[banner](../includes/banner.md)]


Þessi grein lýsir því hvernig þú getur notað hönnuð uppskriftar til að hanna og vinna með uppskriftatréskipulag (BOM). Hægt er smella á uppsetningu til að velja ólíkar skilgreiningar og tilgreina hvaða upplýsingar á að sýna í línum trésins.

Þegar þú opna **uppskriftarhönnuði** síðu frá **Útgefnum afurðum** síðu, birtir hún stigveldi uppskrifta (BOMs) sem eru virk og samþykkt fyrir völdu vöruna, fyrir sjálfgefið pöntunarsvæði eða vöru, og raunverulega dagsetningu.  

Smellið á **Síu** til að breyta upphaflega valinu í yfirlitinu. Með því að stilla skoðunarreglu á **Valið/virkt eða Valið**, er hægt að velja einstakar Uppskriftir eða leiðarútgáfur til að nota í yfirliti. Hægt er að velja ósamþykkt og óvirkar uppskriftaútgáfur til að birta eða viðhalda uppskriftarhönnuði.  

**Ábending:** Ef uppskriftarhönnuði er opnuð í **Uppskriftir** listasíðuna, birtir það ekki upplýsingar um leið. Sem stendur er val á Uppskrift eða leiðarútgáfu eiginleiki fyrir útgáfur Uppskriftar og leiðarútgáfa og á við öll tilvik uppskriftarhönnuðar.  

Í eftirfarandi köflum er lýst virkni sem er tiltæk á mismunandi flipum í uppskriftahönnuði.

## <a name="analyzing-a-bom-structure-by-using-the-bom-designer"></a>Greina skipulag Uppskriftarinnar með uppskriftahönnuði
Uppskriftahönnuður hefur tvo hluta:

-   Trjáyfirlit yfir uppskriftarskipulagið.
-   Upplýsingahluta sem sýnir upplýsingar valinna gagna. Þegar þú velja hnút í trjáyfirlitinu, eru flýtiflipar í hlutanum upplýsingar uppfærast byggt á þeim hnút:
    -   **Uppskriftarlínuupplýsingar** – Sýnir upplýsingar um uppskriftarlínu sem er valin í trjáyfirlitinu.
    -   **Afurðargögn** – Sýnir upplýsingar um aðalafurð eða afurð sem er notuð í valinn hnút. Hægt er að smella á **Breyta útgefin afurð** til að viðhalda valinnar vöru.
    -   **Uppskrift** – Sýnir haus uppskriftar sem er tengd við valinn hnút.
    -   **Uppskrift** – Sýnir haus leiðar sem er tengd við valinn hnút.
    -   **leiðaraðgerð** – Sýnir forskoðun á aðgerðum leiðarinnar. Þegar uppskriftarlína sem er tengdur við tiltekna aðgerð er valið, er aðgerðin merkt sem **Íhlutur nauðsynlegur við aðgerðir**.

## <a name="selecting-a-bom-and-route"></a>Velja Uppskrift og leið
Síunni sem er beitt fyrir Uppskrift og leið er birt í haus uppskriftarhönnuðar. Hægt er að breyta síu með því að nota í **Síu** svarglugga. Eftirfarandi tafla lýsir reitunum í svarglugganum.

<table>
<thead>
<tr class="header">
<th>Reitur</th>
<th>Lýsing</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Afurðarvíddir</td>
<td>Ef fullkláraða varan er afurðarsniðmát er hægt að skilgreina virkar afurðarvíddir fyrir aðalval. <strong>Ábending:</strong> Ef uppskriftarhönnuði fyrir afurðir sem ekki afurðarsniðmát er opnuð, er ekki hægt að velja neinar afurðavíddir á <strong>Síu</strong> svarglugga.</td>
</tr>
<tr class="even">
<td>Svæði</td>
<td>Breyta svæði sem uppskriftatrénu er birt fyrir. Sjálfgefið svæði er sjálfgefið birgðasvæði afurðar.</td>
</tr>
<tr class="odd">
<td>Skoðunarregla</td>
<td>Velja skoðunarregluútgáfuna sem á við gildandi uppskriftarskipulag og gildandi leið.
<ul>
<li>Ef reglan er stillt á <strong> virk eða valinn/virk</strong> er gildandi uppskriftarútgáfa eða leiðarútgáfa fyrir þessa dagsetningu fundin.</li>
<li>Þegar regla er stillt á <strong>Valið/virkt eða valið</strong>, geturðu valið uppskriftarútgáfu eða leiðarútgáfu með því að smella á <strong>Uppskrift</strong> &gt; <strong>uppskriftaútgáfur</strong> eða <strong>Leið</strong> &gt; <strong>Leiðarútgáfur</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Útgáfudagsetning</td>
<td>Færið inn útgáfudagsetningu fyrir uppskrift og leið. Útgáfan tilgreinir hvaða uppskriftarútgáfa á að nota á tilteknum degi eins og ákvarðað er af útgáfudagsetningu í uppsetningu uppskriftarútgáfu.</td>
</tr>
<tr class="odd">
<td>Frá-magn</td>
<td>Sía útgáfur með því að velja tiltekin frá-magn. Ef þú stillir á gildi, gæti verið valdar mismunandi Uppskriftir og leiðarútgáfur.</td>
</tr>
<tr class="even">
<td>Sýna aðeins gild</td>
<td>Ef gátreiturinn er valinn eru einungis uppskriftarlínur með gildum dagsetningum sýndar í tréskipulaginu. Hægt er að hægrismella eða tvísmella á uppskriftarlínuna til þess að opna síðuna <strong>Breyta uppskriftarlínu</strong> þar sem má skoða gildisdagsetningar fyrir uppskriftarlínuna.</td>
</tr>
</tbody>
</table>

Þegar uppskriftarhönnuði er notuð til að endurskoða eða breyta Uppskriftir sem samanstanda af einni eða fleiri stig af skuggum, nær leið sem er tengt við hæstu vöruna yfirleitt yfir allt stigveldi Uppskriftalínunnar. Til að einfalda yfirlit er hægt er að læsa efstastigs leið á skjánum með því að smella **Skoða** &gt; **Læsa leið**. Til að aflæsa leiðinni er smellt á **Skoða** &gt; **Aflæsa leið**.

## <a name="adding-and-editing-boms-and-bom-lines"></a>Bæta við og breyta Uppskriftir og uppskriftarlínum
Nota skal **uppskriftarlínur** eða **eiginleika** til að breyta uppskriftarlínum eða Uppskrift. Þegar þú velja hnút í trénu ákvarðar gerð hnúts þá eiginleika sem eru tiltækir.

| Aðgerð                            | lýsing                                                                                               | Hnútagerð og skilyrði                                                                                                                                                                                                                                                                       |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Uppskriftarlína &gt; Breyta                 | Opnar svarglugga þar sem hægt er að breyta eigindir uppskriftarlínu.                                             | Þessi aðgerð er tiltæk þegar hnútur uppskriftarlínu er valin.                                                                                                                                                                                                                                   |
| Uppskriftarlína &gt; Eyða               | Eyða uppskriftarlínu úr valinni uppskrift                                                                  | Þessi aðgerð er tiltækt þegar hnútir uppskriftarlínu er valinn, og Uppskrift er ekki læst fyrir breytingum.                                                                                                                                                                                             |
| Uppskriftarlínur &gt; Bæta við á undan línu      | Opna svarglugga þar sem hægt er að velja afurðarafbrigði til að taka með á undan valda uppskriftarlínu.         | Þessi aðgerð er tiltæk þegar hnútur uppskriftarlínu er valin.                                                                                                                                                                                                                                   |
| Uppskriftarlínur &gt; Bæta við íhlut uppskriftar | Opna svarglugga þar sem hægt er að velja afurðarafbrigði til að taka með í lok valda uppskriftar.       | Þessi aðgerð er tiltæk þegar valinn hnútur er með valda uppskrift. Ef þessi aðgerð er ekki tiltæk, er vantar hugsanlega uppskriftarútgáfu fyrir valinnar afurðarafbrigði. Í þessu tilfelli er hægt að smella á **Uppskrift** &gt; **Stofna útgáfu** til að stofna útgáfa sem vantar fyrir valinn hnút. |
| Uppskriftarlínur &gt; Bæta við eftir línu       | Opna svarglugga þar sem hægt er að velja afurðarafbrigði til að taka með á eftir valda uppskriftarlínu.          | Þessi aðgerð er tiltæk þegar hnútur uppskriftarlínu er valin.                                                                                                                                                                                                                                   |
| Uppskrift &gt; Stofna útgáfu             | Stofna nýja uppskriftarútgáfu eða Uppskrift fyrir afurðarafbrigði á valinn hnút.                             | Þessi aðgerð er tiltæk þegar hnútur uppskriftarlínu sem er valin er tengd við vöru sem er með gerð framleiðslu **Uppskrift** eða **Formúlu**.                                                                                                                                                  |
| Uppskrift &gt; Útreikningur                | Opnar svarglugga þar sem hægt er að keyra útreikning kostnaðar eða söluverðs fyrir valda afurðarafbrigði. | Þessi aðgerð er tiltæk þegar valinn hnútur er tengdur við uppskriftarútgáfu.                                                                                                                                                                                                         |
| Uppskrift &gt; Tékki                      | Villuleita og athuga valda Uppskrift.                                                                      | Þessi aðgerð er tiltæk þegar valinn hnútur er tengdur við uppskriftarútgáfu.                                                                                                                                                                                                         |

## <a name="configuring-the-tree-view"></a>Skilgreina trjáyfirlitið.
Smellið á **Uppsetningu** til að sérsníða upplýsingarnar sem birtast í trjáyfirlitinu í uppskriftarhönnuði.

| Svæðaflokkur | Lýsing                                                                                                                                                  |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Uppskrift         | Notið þessa gátreiti til að velja skilyrðin sem eru sýndar í trjáskipulagi. Uppskriftahönnuður sýnir valin skilyrði neðst í báðum flipum. |
| Leið       | Notið þessa gátreiti til að velja skilyrðin sem eru sýndar fyrir leiðirnar.                                                                                    |






