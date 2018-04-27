---
title: "Formúluhönnuður"
description: "Þetta efnisatriði útskýrir hvernig á að nota reikniformúluhönnuð til að greina og viðhalda formúlum í trjáyfirliti."
author: cvocph
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PlanActivity, ReqSupplyDemandSchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.search.industry: 
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a4cfd017fe10bbda6eda0e3a9a045e0832b08753
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="formula-designer"></a>Formúluhönnuður

[!INCLUDE [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir hvernig á að nota reikniformúluhönnuð til að greina og viðhalda formúlum í trjáyfirliti.

Þegar síðan **Reikniformúluhönnuður** er opnup af síðunni **Losaðar vörur** sýnir tréð á vinstri rúðunni lista yfir samafurðir og stigveldi innihaldsefna fyrir losaðar vörur. Skipanin er fengin úr stigveldi formúla sem eru virkar og samþykktar fyrir valda vöru og innihaldsefni hennar, sjálfgefið röðunarsvæði vörunnar og raunverulega dagsetningu.

Smelltu á **Uppsetningu** til að velja ólíkar skilgreiningar og tilgreina hvaða upplýsingar á að sýna í línum trésins.

Smellið á **Síu** til að breyta upphaflega valinu í yfirlitinu. Með því að stilla skoðunarreglu á **Valið/virkt** eða **Valið**, er hægt að velja einstakar formúlur eða leiðarútgáfur til að nota í yfirliti. Hægt er að velja ósamþykkt og óvirkar formúluútgáfur til að birta eða viðhalda formúluhönnuði.  

> [!NOTE]
> Ef síðan **Formúluhönnuður** af listasíðunni **Uppskriftir** er opnuð birtir hún ekki upplýsingar um leið. Núna er valinu á formúlu eða útgáfu leiðar beitt á öll tilvik hönnuðarins útreikningsformúlu.  

Í eftirfarandi köflum er lýst virkni sem er tiltæk í uppskriftahönnuði.

## <a name="analyze-a-formula-structure-by-using-the-formula-designer"></a>Greina skipulag reikniformúlu með því að nota reikniformúluhönnuð
Formúluhönnuður hefur tvo hluta:

-   Trjáyfirlit yfir formúluskipulagið.
-   Upplýsingahluta sem sýnir upplýsingar valinna gagna. Þegar þú velja hnút í trjáyfirlitinu, eru flýtiflipar í hlutanum upplýsingar uppfærast byggt á þeim hnút:
    -   **Formúlulínuupplýsingar** – Skoða upplýsingar um fomúlulínu sem er valin í trjáyfirlitinu.
    -   **Afurðargögn** – Skoða upplýsingar um aðalafurð eða afurð sem er notuð í valinn hnút. Hægt er að smella á **Breyta útgefin afurð** til að viðhalda valinnar vöru.
    -   **Formúla** – Skoða haus formúlu sem er tengd við valinn hnút.
    -   **Leið** – Skoða haus leiðar sem er tengd við valinn hnút.
    -   **Leiðaraðgerðir** – Skoða forskoðun á aðgerðum leiðarinnar. Þegar uppskriftarlína sem er tengdur við tiltekna aðgerð er valið, er aðgerðin merkt sem **Íhlutur nauðsynlegur við aðgerðir**.

## <a name="select-a-formula-and-route"></a>Veljið formúlu og leið
Síunni sem er beitt fyrir formúlu og leið er sýnd í haus formúluhönnuðar. Hægt er að breyta síu með því að nota í **Síu** svarglugga. Eftirfarandi tafla lýsir reitunum í svarglugganum.

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
<td>Ef valin endanleg vara er afurðarsniðmát er hægt að skilgreina virka afurðavídd fyrir aðalvalið. Athugið að ef formúluhönnuðurinn er opnaður fyrir afurð sem er ekki afurðarsniðmát verður ekki hægt að velja neinar afurðarvíddir í svarglugganum <strong>Sía</strong>.</p></td>
</tr>
<tr class="even">
<td>Svæði</td>
<td>Breyta svæði sem innihaldstréð er sýnt fyrir. Sjálfgefið svæði er sjálfgefið birgðasvæði afurðar.</td>
</tr>
<tr class="odd">
<td>Skoðunarregla</td>
<td><p>Velja skoðunarregluútgáfuna sem á við gildandi formúluskipulag og gildandi leið:</p>
<ul>
<li>Ef reglan er stillt á <strong>Virk</strong> eða <strong>Valinn/virk</strong> er gildandi formúluútgáfa eða leiðarútgáfa fyrir þessa dagsetningu fundin.</li>
<li>Þegar regla er stillt á <strong>Valið/virkt</strong> eða <strong>Valið</strong>, geturðu valið formúluútgáfu eða leiðarútgáfu með því að smella á <strong>Formúlu</strong> &gt; <strong>Formúluútgáfur</strong> eða <strong>Leið</strong> &gt; <strong>Leiðarútgáfur</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>Útgáfudagsetning</td>
<td>Færið inn útgáfudagsetningu fyrir formúlu og leið. Útgáfan tilgreinir hvaða formúluútgáfu á að nota á tilteknum degi, byggt á útgáfudagsetningum í uppsetningu formúluútgáfu.</td>
</tr>
<tr class="odd">
<td>Frá-magn</td>
<td>Sía útgáfur með því að velja tiltekin &quot;frá&quot;-magn. Ef þú stillir gildi gætu mismunandi útgáfur formúlu og leiða verið valdar.</td>
</tr>
<tr class="even">
<td>Sýna aðeins gild</td>
<td>Ef gátreiturinn er valinn eru einungis formúlulínur með gildum dagsetningum sýndar í tréskipulaginu. Hægt er að hægrismella eða tvísmella á formúlulínuna til þess að opna síðuna <strong>Breyta fornúlulínu</strong> þar sem má skoða gildisdagsetningar fyrir formúlulínuna.</td>
</tr>
</tbody>
</table>

Þegar formúluhönnuður er notaður til að endurskoða eða breyta formúlum sem samanstanda af einni eða fleiri stigum af skuggum, nær leið sem er tengt við hæstu vöruna yfirleitt yfir allt stigveldi formúlunnar. Til að einfalda yfirlit er hægt er að læsa efstastigs leið á skjánum með því að smella **Skoða** &gt; **Læsa leið**. Til að aflæsa leiðinni er smellt á **Skoða** &gt; **Aflæsa leið**.

## <a name="add-and-edit-formulas-and-formula-lines"></a>Bæta við og breyta formúlum og reikniformúlulínum
Nota skal aðgerðirnar **Uppskriftarlínur** eða **Formúlur** til að breyta formúlulínum eða formúlu. Þegar þú velur hnút í trénu ákvarðar gerð hnúts þá eiginleika sem eru tiltækir.

| Aðgerð                            | lýsing                                                                                               | Hnútagerð og skilyrði |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|--------------------------|
| Uppskriftarlína &gt; Breyta                 | Opnar svarglugga þar sem hægt er að breyta eigindum formúlulínu.                                         | Þessi aðgerð er tiltæk þegar hnútur formúlulínu er valinn. |
| Uppskriftarlína &gt; Eyða               | Eyða formúlulínu úr valinni formúlu.                                                          | Þessi aðgerð er tiltæk þegar hnútur formúlulínu er valinn og formúlan er ekki læst fyrir breytingum. |
| Uppskriftarlínur &gt; Bæta við á undan línu      | Opna svarglugga þar sem hægt er að velja afurðarafbrigði til að taka með á undan valinni formúlulínu.     | Þessi aðgerð er tiltæk þegar hnútur formúlulínu er valinn. |
| Uppskriftarlínur &gt; Bæta við íhlut uppskriftar | Opna svarglugga þar sem hægt er að velja afurðarafbrigði til að taka með í lok valinnar formúlu.   | Þessi aðgerð er tiltæk þegar valinn hnútur er með valda formúlu. Ef þessi aðgerð er ekki tiltæk, er vantar hugsanlega formúluútgáfu fyrir valið afurðarafbrigði. Í þessu tilfelli er hægt að smella á **Formúlu** &gt; **Stofna útgáfu** til að stofna útgáfa sem vantar fyrir valinn hnút. |
| Uppskriftarlínur &gt; Bæta við eftir línu       | Opna svarglugga þar sem hægt er að velja afurðarafbrigði til að taka með á eftir valinni formúlulínu.      | Þessi aðgerð er tiltæk þegar hnútur formúlulínu er valinn. |
| Formúla &gt; Stofna útgáfu         | Stofna nýja formúluútgáfu eða formúlu fyrir afurðarafbrigði á valinn hnút.                     | Þessi aðgerð er tiltæk þegar hnútur formúlulínu sem er valin er tengd við vöru sem er með gerð framleiðslu **Uppskrift** eða **Formúlu**. |
| Formúla &gt; Útreikningur            | Opnar svarglugga þar sem hægt er að keyra útreikning kostnaðar eða söluverðs fyrir valda afurðarafbrigði. | Þessi aðgerð er tiltæk þegar valinn hnútur er tengdur við formúluútgáfu. |
| Formúla &gt; Athugun                  | Villuleita og athuga valda formúlu.                                                                  | Þessi aðgerð er tiltæk þegar valinn hnútur er tengdur við formúluútgáfu. |

## <a name="configuring-the-tree-view"></a>Skilgreina trjáyfirlitið.
Smellið á **Uppsetningu** til að sérsníða upplýsingarnar sem birtast í trjáyfirlitinu í formúluhönnuði.


| Svæðaflokkur |                                                                          lýsing                                                                          |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
|     Uppskrift     | Notið þessa gátreiti til að velja skilyrðin sem eru sýndar í trjáskipulagi. Formúluhönnuðurinn sýnir valin skilyrði neðst í báðum flipum. |
|    Leið    |                                           Notið þessa gátreiti til að velja skilyrðin sem eru sýndar fyrir leiðirnar.                                           |


