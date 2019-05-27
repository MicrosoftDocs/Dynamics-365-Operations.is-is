---
title: Setja upp íhluti verks
description: Þetta efnisatriði lýsir þeim hugtakaþáttum sem vinnsla getur haft með og gefur dæmi um hvernig hægt er að nota þessa þætti í fyrirtækinu.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.author: anbichse
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 255a84c59a7041c80eb0a466c038d6f9885c5f63
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518252"
---
# <a name="set-up-the-components-of-a-job"></a>Setja upp íhluti verks

[!include [banner](includes/banner.md)]


Þetta efnisatriði lýsir þeim hugtakaþáttum sem vinnsla getur haft með og gefur dæmi um hvernig hægt er að nota þessa þætti í fyrirtækinu. 

Áður en hægt er að stofna vinnslur verður þú að setja upp tilvísunarupplýsingar. Hægt er að stofna vinnslu sem hefur aðeins heiti. Hins vegar með því að hafa frekari upplýsingar með, t.d. titil vinnslu, veitirðu sjálfgildi fyrir þær stöður sem er úthlutað til vinnslu. Þar að auki er hægt að nota sumar þeirra upplýsinga sem voru færðar inn til að afmarka launafyrirkomulag við tilgreindar vinnslur. Ef ætlunin er að setja upp hæfni sem hægt er nota til að afmarka launafyrirkomulag við tilgreindar vinnslur ætti að setja upp starfshlutverk og vinnslugerð áður en vinnslur eru setter upp. Með því að hafa þessi sjálfgildi tiltæk spararðu tíma þegar stöðum er bætt við starfið. 

Sumar starfsupplýsingar, eins og starfsheiti, gerð og aðgerð, eru dagsetningarvirkar. Ef þú stofnar starf í dag en bætir þessum upplýsingum ekki við fyrr en seinna og skoðar síðan starfið frá og með stofndagsetningu munu þessar upplýsingar ekki birtast. Þess vegna ættirðu að stofna sumar þessara tilvísunarupplýsinga áður en þú þarft að nota þær. Á þann hátt er hægt að bæta við upplýsingum í ný störf þegar þau eru stofnuð.

## <a name="job-titles"></a>Starfsheiti
Áður en hægt er að stofna vinnslur verður að setja upp titla fyrir þær vinnslur. Stöður erfa starfsheiti úr vinnslum sem þær eru tengdar við. 

Viðhalda starfsheitum með því að nota síðuna **Titlar** sem þú getur opnað með því að nota leitaraðgerð. Á síðunni **Titlar** skal færa inn þá titla sem þú ætlar að nota fyrir störfin.

## <a name="job-types"></a>Vinnslugerðir
Þú notar vinnslugerð til að flokka svipuð störf í flokka. Starfstegundir eru ekki áskildar. Hins vegar ef ætlunin er að nota vinnslugerðir þegar setja á upp hæfnireglur fyrir greiðsluáætlunarstjórnun ætti að setja upp vinnslugerðir áður en hægt er að setja upp störf. Sum dæmi um starfstegundir eru Fullt starf og Hlutastarf, eða Laun og Tímakaup. Starfstegundum er viðhaldið með því að nota síðuna **Vinnslugerð**. Á síðunni **Starfsgerðir** skal færa inn heiti og lýsingu á starfsgerðinni. Í reitnum **Staða undanþágu** velurðu einn af eftirfarandi valkostum til að tilgreina þá stöðu undanþágu Fair Labor Standards Act (FLSA) starfa sem hafa þessa starfsgerð:

-   **Undanþága** – Störf eru undanþegin yfirvinnu undir FLSA.
-   **Ekki undanþága** – Störf eru ekki undanþegin yfirvinnu undir FLSA.
-   **Á ekki við** – FLSA á ekki við.

## <a name="job-functions"></a>Starfshlutverk
Starfshlutverk lýsa hástigs virkt flokkar og tengdum hástigs skyldur. Starfshlutverk eru ekki áskilin. Þú getur notað starfshlutverk ásamt vinnslugerð til að afmarka launafyrirkomulag við tilteknar vinnslur. Þú tengir starfshlutverk og vinnslugerð við launafyrirkomulag með því að setja upp hæfnisreglur á síðunni **Hæfnisreglur**. Síðan er hægt að festa hóp stiga við launafyrirkomulag sem eiga við um tilgreinda samsetningu vinnslugerðar og starfshlutverka sem þú hefur skilgreint til og með hæfniregla. (Þessir eiginleikar eiga við um bæði launafyrirkomulagi fastra launa og breytileg uppbót áætlun.) Hins vegar ef þú ætlar að nota starfshlutverk þegar hæfnisreglur eru settar upp fyrir launafyrirkomulag þarf að setja upp starfshlutverk áður en þú setur upp störf. Eftirfarandi tafla sýnir dæmi um starfshlutverk.

| Starf           | Starfshlutverk         |
|---------------|----------------------|
| Sölustjóri | Stjórnandi á miðsstigi    |
| Bókhaldari    | Sérfræðingar        |

Starfstegundum er viðhaldið með því að nota síðuna **Starfshlutverk**. Á síðunni **Starfshlutverk** skal færa inn staðfestingarkóða og stutta lýsingu á starfshlutverk.

## <a name="job-tasks"></a>Verkefni starfs
Verkhlutar sem lýsa grunnatriðum verkefnis sem starfskraftur sem er í stöðu fyrir vinnsla verður að ljúka. Sama verkefni starfs er hægt að bæta við mörg störf og í stöður fyrir þau störf sem nota þau verkefni. Eftirfarandi tafla sýnir dæmi um verkefni starfs.

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
<li><strong>Perf yfirferð</strong> – fara yfir afköst hvers sölumanns&#39;.</li>
<li><strong>Abs yfirferð</strong> – Samþykkja eða hafna fjarvistabeiðnir&#39; hvers sölumanns eða skráningar.</li>
</ul></td>
</tr>
<tr class="even">
<td>Bókhaldari</td>
<td><strong>FIN Skýrslu</strong> – Birta vikulegt fjárhagsskýrslur til fjármálastjórnanda.</td>
</tr>
</tbody>
</table>

Verkefnum starfs er viðhaldið með því að nota síðuna **Verkefni starfs**. Á síðunni **Verkefni starfs** skal færa inn heiti og lýsingu á verkefni starfs. Í svæðinu **athugasemd** er valfrjálst hægt að færa inn viðbótarupplýsingar. Hægt er að uppfæra athugasemdirnar fyrir tilgreint starf án þess að breyta athugasemdunum sem voru færðar inn hérna.

## <a name="areas-of-responsibility"></a>Ábyrgðarsvið
Þú notar Ábyrgðarsvið til að gefa til kynna starfshlutverk, ferli, afurðir og aðgerðir sem starfsmaður sem er í stöðu er ábyrgur fyrir í vinnslu. Til dæmis fyrir starf sem heitir "Bókari" gæti eitt svæði ábyrgðar verið "Fjárhagsleg skýrslugerð fyrir Afurð A". Ábyrgðarsviði er viðhaldið með því að nota síðuna **Ábyrgðarsvið** sem þú getur opnað með því að nota leitaraðgerð. Á síðunni **Ábyrgðarsvið** skal færa inn heiti og lýsingu á ábyrgðinni. Í svæðinu **athugasemd** er valfrjálst hægt að færa inn viðbótarupplýsingar. Hægt er að uppfæra athugasemdirnar fyrir tilgreint starf án þess að breyta athugasemdunum sem voru færðar inn hérna.

## <a name="steps-for-creating-a-job"></a>Skref til að stofna starf
Sjá efnisatriðið [Skilgreina ný störf](../fin-and-ops/hr/tasks/define-new-jobs.md) fyrir skref fyrir skref aðferð til að stofna til nýtt starf. 
