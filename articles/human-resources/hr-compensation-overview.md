---
title: Launafyrirkomulag
description: Þessi grein lýsir því hvernig á að nota launastjórnun til að stjórna og vinna úr launaáætlunum.
author: twheeloc
ms.date: 08/25/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCompensationLevel, HRCCompGrid, HRMCompFixedAction, HRMCompFixedBudget, HRMCompFixedPlanTable, HcmCompensationWorkspace
audience: Application User
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 39bb4419f18f2cc0da28b5527d261112b2ae74c5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859547"
---
# <a name="compensation-plans"></a>Launafyrirkomulag


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Stjórnendur launa og fríðinda geta notað **launastjórnun** til að viðhalda og vinna úr föstum og breytilegum launafyrirkomulögum fyrir starfsmenn fyrirtækisins.

### <a name="introduction"></a>Inngangur

Lausnastjórnun er notuð til að stýra afhendingu grunnlauna og umbunar. Föstum grunnlaunum starfsmanns og verðleikaaukning er stýrt með launafyrirkomulag fastra launa. Greiðsla hvatagreiðslu, svo sem kaupauka, afkastaumbun, hlutafjárkaupréttur og styrki, en einnig eins-skiptis umbun, er stýrt með breytilegu launafyrirkomulagi. 

Hægt er að tengja starfsmenn við eina eða fleiri áætlanir af báðum gerðum. Starfsmaður verður að uppfylla eftirfarandi skilyrði til að vera hæfur fyrir launafyrirkomulagið.
-   Starfsmaðurinn verður að hafa virka stöðuverkefni.
-   Starfsmaðurinn verður að uppfylla skilyrðin sem eru skilgreind af hæfnisreglum fyrir launafyrirkomulag.

## <a name="compensation-setup"></a>Uppsetning launa
Í eftirfarandi töflu er listi yfir þætti launaferlis sem geta verið sambyggt uppsetningu launafyrirkomulags fyrirtækisins.

<table>
<thead>
<tr class="header">
<th>Hlutur</th>
<th>Meiri upplýsingar</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Aðgerðir fastra launa</td>
<td>Aðgerðir fastra launa hafa tvennan tilgang:
<ul>
<li>Aðgerðir getur tilgreint gerðir upplýsingar sem verður að skrá þegar laun starfsmanns breytist. Til dæmis er hægt að krefjast ástæðu breytinga, eins og stöðuhækkun eða stöðulækkun verður skráð.</li>
<li>Aðgerðir geta tryggt að útreikningur er notað þegar launafyrirkomulag fastra launa eru unnið.  Til dæmis, aðgerðir af gerðinni eigið fé bera saman laun fyrir starfsmenn við lágmarks tilvísunarpunkt fyrir stig starfsmanns og tryggja að starfsmaðurinn fái greidd að minnsta kosti lágmarkið.&#39;</li>
</ul></td>
</tr>
<tr class="even">
<td>Stig</td>
<td>Stigum er úthlutað á störf, og allar stöður sem eru tengdar við starfstilvísun. Hægt er að stofna afmarkaðar gerðir launafyrirkomulaga: Gráða, braut og skref.</td>
</tr>
<tr class="odd">
<td>Fylki nýtingar launabils</td>
<td>Nýtingarfylki sviðs hjálpar þér að flytja starfsmenn í stýripunktinn fyrir starf þeirra. Einnig er hægt að nota nýtingarmörk til að stýra launataxta eigin fjár innan fyrirtækisins óháð frammistöðu starfsmanns eða heildarframmistöðu fyrirtækisins.&#39; Til dæmis Starfsmenn sem fá minna greitt í sínu sviði fá hærri prósentuaukning en þeir starfsmenn sem eru fá greitt meira innan sviðsins. Á þennan hátt er hægt kerfisbundið hægt að mótbóka muninn á eigin fé. Notkunarmörkin eru reiknuð út á eftirfarandi hátt: (Fastur launataxti - Lágmark sviðs) / (Hámark sviðs - Lágmark sviðs).</td>
</tr>
<tr class="even">
<td>Uppsetning tilvísunarpunkta</td>
<td>Uppsetningar tilvísunarpunkta innihalda hóp tilvísunarpunkta sem sýna svið í fylki. Hverju sviði má tengja launataxta. Til dæmis hafa gráðuáætlanir oft tilvísunarpunkta fyrir Lágmark, Miðpunktur og Hámark.</td>
</tr>
<tr class="odd">
<td>Launafylki</td>
<td>Launafylki er safn tilvísunarpunkta og stiga sem þú notar til að stofna launafyrirkomulag.</td>
</tr>
<tr class="even">
<td>Launaskipulag</td>
<td>Launaskipulag er launafylki sem er með launataxta sem tengist tilvísunarpunkta fyrir hvert stig.</td>
</tr>
<tr class="odd">
<td>Hæfnisreglur</td>
<td>Hægt er að nota hæfnisreglur til að bera kennsl á starfsmenn í tilteknum vinnslur, vinnsluaðgerðir, vinnslugerðir, deildum, verkalýðsfélögum, eða launasvæðum sem tilteknar launafyrirkomulag eiga við um. Stofna verður hæfnireglur fyrir bæði launafyrirkomulag fastra og breytilegra launa til að skrá starfsmenn í áætlun. Eftir að hafa tilgreint hæfnisreglur fyrir greiðsluáætlun, skal skilgreina stiga munu eiga við vinnslur sem áætlunin á við um.</td>
</tr>
<tr class="even">
<td>Greiðslutíðni</td>
<td>Greiðslutíðni er notuð til að skilgreina tímabilið sem laun eru greidd fyrir.  Til dæmis auðveldar greiðslutíðni að skilja hvort launaupphæðin er tilgreindur sem árleg laun eða launataxti á klukkustund. Greiðslutíðni eru einnig notaðar til að setja upp umreiknistuðla til að umbreyta upphæðir launa úr  greiðslutíðni fyrir mánaðarlega, vikulega, hálfsmánaðarlegrar og tímakaups yfir í árleg greiðslutíðni.</td>
</tr>
<tr class="odd">
<td>Launasvæði</td>
<td>Launasvæði eru notuð til þess að tilgreina laun starfsmanns samkvæmt staðsetningu vinnustaðar.</td>
</tr>
<tr class="even">
<td>Stýripunktur</td>
<td>Stýripunkturinn skilgreinir hvað þú telur vera besta launataxta fyrir alla starfsmenn í launastigi. Fyrir áætlunarskipulag gráðu eru stýripunktar yfirleitt miðpunktur sviðsins. Brautarskipulag notast sjaldan við stýripunkta. Hægt er að tilgreina stýripunktur fyrir launafyrirkomulag fastra launa í launafyrirkomulagssíðunni **Föst laun**.</td>
</tr>
<tr class="odd">
<td>Starfshlutverk</td>
<td>Starfshlutverk eru notaðar til að flokka og sía launafyrirkomulag fyrir tiltekin störf.</td>
</tr>
<tr class="even">
<td>Vinnslugerðir</td>
<td>Vinnslugerðir eru notaðar til að flokka og sía launafyrirkomulag fyrir tiltekin störf.</td>
</tr>
<tr class="odd">
<td>Gerðir breytilegra uppbóta</td>
<td>Breytileg launagerð, eins og hlutabréfaumbun eða umbun í reiðufé, er sett upp í breytilegu launafyrirkomulagi.</td>
</tr>
<tr class="even">
<td>Launanet</td>
<td>Launanet innihalda launaskipulagið.  Eitt eða fleiri launafyrirkomulag geta notað hnitanet launa.</td>
</tr>
<tr class="odd">
<td>Afkastaáætlanir</td>
<td>Afkastaáætlanir eru notaðar til að tengja afköst við úthlutunarfylki, til að nota áætlun fyrir árangurstengingu launa.</td>
</tr>
<tr class="even">
<td>Afkastaeinkunnir</td>
<td>Afkastaeinkunnir eru notaðar í afkastaáætlunum til að ákvarða upphæð umbunar vegna verðleika eða afkasta.</td>
</tr>
</tbody>
</table>

## <a name="process-events"></a>Vinnslutilvik
Vinnslutilvik reiknar út launaupplýsingar fyrir tilgreint tímabil handa öllum starfsmönnum sem eru skráðir í eina eða fleiri fastar eða breytilegar launafyrirkomulag. Hægt er að keyra vinnslutilvik endurtekið, til að prófa eða uppfæra útreiknaðar launaniðurstöður.

## <a name="compensation-events"></a>Launatilvik

Í hvert sinn vinnslutilvik er keyrt er launatilvik stofnað.  Launatilvik innihalda niðurstöðu launavinnslu fyrir hvern starfsmann sem hafður var með í vinnslutilvikinu.  Þegar útreikningar eru réttir er hægt að hlaða launatilvikinu til að uppfæra launafærslur fyrir starfsmenn sem verða fyrir áhrifum af vinnslutilvikið.

## <a name="recommendations"></a>Ráðleggingar
Þegar vinnslutilvik hefur verið keyrt, geturðu stungið uppá leiðréttingar á verðleikahækkun starfsmanns eða umbunarupphæð út frá reiknuðum leiðbeiningar á vinnslutilvikinu. Til að gera tillögur fyrir starfsmenn, verður að virkja tillögur þegar launafyrirkomulag eru sett upp eða þegar sett er upp vinnslutilvikið.





[!INCLUDE[footer-include](../includes/footer-banner.md)]
