---
title: "Setja upp íhluti í vinnslu"
description: "Þetta efnisatriði lýsir almennar einingar í vinnslu geta verið og gefur dæmi um hvernig hægt er að nota þessar einingar í þínu fyrirtæki."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: d96b1f01a5cb4370436888deae8fd4835a0dbb80
ms.openlocfilehash: b8143db5b133337603a7f2f46028d91bb81cd947
ms.lasthandoff: 03/31/2017


---

# <a name="setting-up-the-components-of-a-job"></a>Setja upp íhluti í vinnslu

Þetta efnisatriði lýsir almennar einingar í vinnslu geta verið og gefur dæmi um hvernig hægt er að nota þessar einingar í þínu fyrirtæki. 

Áður en hægt er að stofna störf, verður að setja upp sumar tilvísunarupplýsingum. Hægt er að stofna vinnslu sem er aðeins með heiti. Hins vegar með þar á meðal viðbótarupplýsingar, eins og starfsheiti, er að veita sjálfgildi fyrir stöður sem tengjast vinnslu. Þar að auki er sumar upplýsingar sem eru færðar inn má nota til að sía launafyrirkomulag fyrir ákveðin störf. Ef óskað er að setja upp hæfni sem hægt er að nota til að sía launafyrirkomulag fyrir tiltekin verk ætti að setja upp starfshlutverk og starfsgerðir áður en að setja upp vinnslur. Eftir að hafa þessi sjálfgefnu gildi tiltæk, verður að spara tíma þegar stöðum bætt við runuvinnsluna. 

Sumar upplýsingar um verk, eins og starfsheiti, gerð og aðgerð, er dagsetningin virk. Ef stofna vinnslu í dag en ekki að bæta við þessar upplýsingar síðar fram, og síðan athugaðir vinnslan dagsetningar stofnunar, ekki þessar upplýsingar birtast. Þess vegna er á að stofna einhverjum af þessum upplýsingum tilvísun áður en krefjast þess. Þannig er hægt að bæta upplýsingar í ný störf þegar þær eru stofnaðar.

## <a name="job-titles"></a>Starfsheiti
Áður en hægt er að stofna vinnslur verður að setja upp titla fyrir þær vinnslur. Stöður erfa starfsheiti úr vinnslum sem þær eru tengdar við. 

Vinna með starfsheiti með því að nota í **Titla** síðu sem hægt er að opna með því að nota aðgerð Leit. Á við ** Titla ** síðunni skal færa inn titla sem á að nota fyrir vinnslur.

## <a name="job-types"></a>Vinnslugerðir
Notið gerðir starfa til að flokka tegundir svipuð störf. Vinnslugerðir ekki eru kostnaðarjafnaðar krafist. Hins vegar ef ætlunin er að nota vinnslugerðir þegar setja á upp hæfnireglur fyrir greiðsluáætlunarstjórnun ætti að setja upp vinnslugerðir áður en hægt er að setja upp störf. Nokkur dæmi um vinnslugerðir eru fullt og hlutastarf eða greiða launum og tímakaup. Viðhalda starfsgerðum með því að nota í **Vinnslugerðir** síðu. Á við **Vinnslugerðir** síðunni, færið inn nafn og stutt lýsing fyrir vinnslugerðina. Í því **Skattfrjálsa stöðu** skal velja einn af eftirfarandi valkostum til að tilgreina Sanngjarnt Vinnu Stöðlum Act (FLSA) undanþágustaða vinnsla sem hafa þessa vinnslugerð:

-   **Skattundanþágunúmer** – Vinnslur sem eru undanþegnir yfirvinnu undir FLSA á.
-   **Ekki undanþegið** – Vinnslur sem ekki eru kostnaðarjafnaðar undanþegin yfirvinnu undir á FLSA.
-   **Ekki nota** – FLSA þekju er ekki tiltækt.

## <a name="job-functions"></a>Starfshlutverk
Junctions Vinnslu lýsa flókna virkni tegundir og tengja gjöld á háu stigi. Starfshlutverk ekki eru kostnaðarjafnaðar krafist. Hægt er að nota starfshlutverk með vinnslugerðir, til að sía launafyrirkomulag fyrir ákveðin störf. Hægt er að tengja starfshlutverk og starfsgerðir við launafyrirkomulag með því að setja upp hæfnisreglur í í **hæfnisreglur** síðu. Svo er hægt að tengja hóp stiga við launafyrirkomulag sem á við tiltekna samsetningu vinnslugerð og starfshlutverk sem hefur verið skilgreind í hæfnisreglunum. (Þessar aðgerðir eiga bæði launafyrirkomulög fastra launa og breytilegrar uppbótar.) Hins vegar ef ætlunin er að nota starfshlutverk þegar verið er að setja upp hæfnisreglur fyrir greiðsluáætlunarstjórnun ætti að setja upp starfshlutverk áður en að setja upp vinnslur. Eftirfarandi tafla sýnir nokkur dæmi um starfshlutverk.

| Starf           | Starfshlutverk         |
|---------------|----------------------|
| Sölustjóri | Stjórnandi miðjum stig    |
| Bókhaldari    | Tölvusérfræðinga        |

Viðhalda starfshlutverkum með því að nota í **Vinnsluraðgerðum** síðu. Á við **Vinnsluraðgerðum** síðunni skal færa inn kennikóða og stutt lýsing fyrir starfshlutverkið.

## <a name="job-tasks"></a>Verkefni starfs
Verkefni lýsa grunnatriðin sem starfsmaðurinn sem er í stöðu fyrir vinnslu verður að ljúka. Hægt er að bæta sama verksvið mörg störf og stöður fyrir vinnslur sem nota þessi verkefni. Eftirfarandi tafla sýnir nokkur dæmi um verk í vinnslu.

<table>
<thead>
<tr class="header">
<th>Starf</th>
<th>Verkefni starfs</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Sölustjóri</td>
<td><ul>
<li><strong>Perf yfirferð</strong> – fara Yfir afköst vinnslu fyrir hverja sölumanns.</li>
<li><strong>Abs yfirferð</strong> – Samþykkja eða hafna fjarvistabeiðnir hverja sölumanns eða skráningar.</li>
</ul></td>
</tr>
<tr class="even">
<td>Bókhaldari</td>
<td><strong>FIN Skýrslu</strong> – Birta yfirmaður fjármála vikulegt fjárhagsskýrslur.</td>
</tr>
</tbody>
</table>

Viðhalda starfsverkum með því að nota í **Vinnslu verka** síðu. Á við **Vinnslu verka** síðunni, færið inn heiti og lýsingu fyrir verk í vinnslu. Í því **Athugasemd** svæðið er einnig hægt að færa inn viðbótarupplýsingar. Hægt er að uppfæra athugasemdir fyrir tiltekna vinnslu án þess að breyta athugasemdir sem var færð inn hér.

## <a name="areas-of-responsibility"></a>Ábyrgðarsvið
Ábyrgðarsvið eru notuð til að tilgreina vinnu hlutverk, ferli og afurðir sem starfsmaður í stöðu fyrir starf er ber ábyrgð á. Til dæmis fyrir vinnslu sem kallast "Bókari", ein ábyrgðarsvið gæti verið "Fjárhagsleg skýrslugerð fyrir afurð A." Viðhalda ábyrgðarsviðum með því að nota í **Ábyrgðarsvið** síðu sem hægt er að finna með því að nota aðgerð Leit. Í því **Ábyrgðarsvið** síðunni, færið inn heiti og lýsingu fyrir ábyrgðarsvið. Í því **Athugasemd** svæðið er einnig hægt að færa inn viðbótarupplýsingar. Hægt er að uppfæra athugasemdir fyrir tiltekna vinnslu án þess að breyta athugasemdir sem var færð inn hér.


