---
title: Setja upp íhluti verks
description: Þetta efnisatriði lýsir þeim hugtakaþáttum sem vinnsla getur haft með og gefur dæmi um hvernig hægt er að nota þessa þætti í fyrirtækinu.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle, HcmPersonnelManagementWorkspace, HCMJobFamily
audience: Application User
ms.author: twheeloc
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: de828bc1ab764a8a1bd084a508f38ff19a3947d5
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8693585"
---
# <a name="set-up-the-components-of-a-job"></a>Setja upp íhluti verks


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Þetta efnisatriði lýsir þeim hugtakaþáttum sem vinnsla getur haft með og gefur dæmi um hvernig hægt er að nota þessa þætti í fyrirtækinu. 

Áður en hægt er að stofna vinnslur verður þú að setja upp tilvísunarupplýsingar. Hægt er að stofna vinnslu sem hefur aðeins heiti. Hins vegar með því að hafa frekari upplýsingar með, t.d. titil vinnslu, veitirðu sjálfgildi fyrir þær stöður sem er úthlutað til vinnslu. Þar að auki er hægt að nota sumar þeirra upplýsinga sem voru færðar inn til að afmarka launafyrirkomulag við tilgreindar vinnslur. Ef ætlunin er að setja upp hæfni sem hægt er nota til að afmarka launafyrirkomulag við tilgreindar vinnslur ætti að setja upp starfshlutverk og vinnslugerð áður en vinnslur eru setter upp. Með því að hafa þessi sjálfgildi tiltæk spararðu tíma þegar stöðum er bætt við starfið. 

Sumar starfsupplýsingar, eins og starfsheiti, gerð og aðgerð, eru dagsetningarvirkar. Ef þú stofnar starf í dag en bætir þessum upplýsingum ekki við fyrr en seinna og skoðar síðan starfið frá og með stofndagsetningu munu þessar upplýsingar ekki birtast. Þess vegna ættirðu að stofna sumar þessara tilvísunarupplýsinga áður en þú þarft að nota þær. Á þann hátt er hægt að bæta við upplýsingum í ný störf þegar þau eru stofnuð.

## <a name="job-titles"></a>Starfsheiti
Áður en hægt er að stofna vinnslur verður að setja upp titla fyrir þær vinnslur. Stöður erfa starfsheiti úr vinnslum sem þær eru tengdar við. 

Viðhalda starfsheitum með því að nota síðuna **Titlar** sem þú getur opnað með því að nota leitaraðgerð. Á síðunni **Titlar** skal færa inn þá titla sem þú ætlar að nota fyrir störfin.

## <a name="job-types"></a>Starfsgerðir
Þú notar vinnslugerð til að flokka svipuð störf í flokka. Starfstegundir eru ekki áskildar. Hins vegar ef ætlunin er að nota vinnslugerðir þegar setja á upp hæfnireglur fyrir greiðsluáætlunarstjórnun ætti að setja upp vinnslugerðir áður en hægt er að setja upp störf. Sum dæmi um starfstegundir eru Fullt starf og Hlutastarf, eða Laun og Tímakaup. Starfstegundum er viðhaldið með því að nota síðuna **Vinnslugerð**. Á síðunni **Starfsgerðir** skal færa inn heiti og lýsingu á starfsgerðinni. Í reitnum **Staða undanþágu** velurðu einn af eftirfarandi valkostum til að tilgreina þá stöðu undanþágu Fair Labor Standards Act (FLSA) starfa sem hafa þessa starfsgerð:

-   **Undanþága** – Störf eru undanþegin yfirvinnu undir FLSA.
-   **Ekki undanþága** – Störf eru ekki undanþegin yfirvinnu undir FLSA.
-   **Á ekki við** – FLSA á ekki við.

## <a name="job-family"></a>Starfasafn
Starfasafn er hópur af störfum sem fela í sér svipaða vinnu og krefjast svipaðrar þjálfunar, hæfni, þekkingu og reynslu. Hægt er að tengja starfasafn við vinnu í flýtiflipanum **Flokkun starfs** á síðunni **Störf** og í flýtiflipanum **Almennt** á síðunni **Allar stöður**. Starfasöfn geta verið víðtæk eða sértæk eftir því hverjar kröfur fyrirtækis og skýrslugerðar er. Nokkur dæmi um víðtæk starfasöfn eru **Faglært vinnuafl** og **Ófaglært vinnuafl**. Nokkur dæmi um sértæk starfasöfn eru **Bókhald**, **Framleiðsla** og **Sala**.

Vinnið með starfasöfnum með því að nota síðuna **Starfasafn** sem þú getur opnað með því að nota leitaraðgerðina. Á síðunni **Starfasafn** skal færa inn einkvæmt heiti fyrir safnið og færa inn nákvæma lýsingu á því starfinu.

## <a name="job-functions"></a>Starfshlutverk
Starfshlutverk lýsa hástigs virkt flokkar og tengdum hástigs skyldur. Starfshlutverk eru ekki áskilin. Þú getur notað starfshlutverk ásamt vinnslugerð til að afmarka launafyrirkomulag við tilteknar vinnslur. Þú tengir starfshlutverk og vinnslugerð við launafyrirkomulag með því að setja upp hæfnisreglur á síðunni **Hæfnisreglur**. Síðan er hægt að festa hóp stiga við launafyrirkomulag sem eiga við um tilgreinda samsetningu vinnslugerðar og starfshlutverka sem þú hefur skilgreint til og með hæfniregla. (Þessir eiginleikar eiga við um bæði launafyrirkomulagi fastra launa og breytileg uppbót áætlun.) Hins vegar ef þú ætlar að nota starfshlutverk þegar hæfnisreglur eru settar upp fyrir launafyrirkomulag þarf að setja upp starfshlutverk áður en þú setur upp störf. Eftirfarandi tafla sýnir dæmi um starfshlutverk.

| Starf           | Starfshlutverk         |
|---------------|----------------------|
| Sölustjóri | Stjórnandi á miðsstigi    |
| Bókhaldari    | Sérfræðingar        |

Starfstegundum er viðhaldið með því að nota síðuna **Starfshlutverk**. Á síðunni **Starfshlutverk** skal færa inn staðfestingarkóða og stutta lýsingu á starfshlutverk.

## <a name="compensation"></a>Laun
Til að úthluta launafyrirkomulagi fastra launa á starfsmann sem er með stöðu í starfi þarf að stilla launastig starfsins. The **Bótastig** er notað þegar lágmarks-, miðpunkts- og hámarksupphæðir eru settar í uppbótaruppbyggingu (bótanet). Þegar fyrirkomulag fastra launa er stofnað er launaskipulagið valið. Launaskipulagið inniheldur einnig launastigið. Þegar þú velur launafyrirkomulag fastra launa fyrir starfsmann, á eru launastigin sem eru í boði háð starfinu sem staða starfsmanns tengist. Frekari upplýsingar um hvernig á að setja upp laun er að finna í [Launafyrirkomulag](hr-compensation-overview.md).

## <a name="job-skills"></a>Hæfni fyrir starf
Starfshæfni lýsir þeirri hæfni sem er nauðsynleg til að gegna starfi. Hæfnistig verður að tengjast hverri starfshæfni. Hæfnistigin eru skilgreind af notendum. Þau gefa til kynna stig þekkingar eða reynslu sem þarf fyrir hæfnina. Til dæmis gætu fyrirtæki sett upp tölugildi, til dæmis 1 til 5, þar sem **1** gefur til kynna byrjanda og **5** gefur til kynna sérfræðing. Einnig gætu fyrirtæki sett upp stig sem eru merkt **Byrjandi**, **Miðlungs** eða **Sérfræðingur**. Eftir að hæfnisstigið er stillt er einnig hægt að stilla mikilvægi hæfninnar. Ef t.d. er gerð krafa um að endurskoðandi hafi góða þekkingu á Microsoft Excel er hægt að búa til hæfni sem kallast **Þekking á Excel**. Hæfnisstigið er svo hægt að stilla á **Miðlungs** og mikilvægið er hægt að stilla á **Mest**.

Hægt er að nota hæfnina í starfi í hæfnisskrá. Hæfnisskrá getur borið saman hæfnigrunn sem þarf fyrir starfið og hæfnina sem tengist starfskrafti. Hún getur þá ákvarðað samsvörunarprósentu sem byggir á skörun á hæfni. Frekari upplýsingar um hæfnisskrá er að finna í [Skilgreina hæfni](hr-develop-skills.md). 

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
Sjá greinina [Skilgreina ný störf](./hr-personnel-define-jobs.md) fyrir skref fyrir skref aðferð til að stofna til nýtt starf. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
