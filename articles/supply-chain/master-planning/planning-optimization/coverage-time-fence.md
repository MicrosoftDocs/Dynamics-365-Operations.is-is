---
title: Þekjutímamörk
description: Þessi grein lýsir því hvernig á að setja upp þekjutímagirðingar þegar þú ert að nota áætlanagerð fínstillingu. Þekjutímamörk gefa til kynna áætlunartímabilið og mörkin.
author: t-benebo
ms.date: 01/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqGroup, ReqItemTable, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2021-01-18
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ebd59e05d2ae227f24e7dae6fae3634aab026c5a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8847934"
---
# <a name="coverage-time-fences"></a>Þekjutímamörk

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir því hvernig á að setja upp *umfjöllunartíma girðingar* þegar þú ert að nota áætlanagerð fínstillingu. Skipuleggjendur geta skilgreint áætlunartímabilið (þekjutímamörkin í dögum) og sleppt framboði og eftirspurn sem fellur utan tímabilsins. Þekjutímamörk hjálpa þar af leiðandi til við að koma í veg fyrir „hávaða“ af völdum tillagna um framboð sem þarf ekki að bregðast við næstu mánuðina. Sem dæmi má nefna spá næsta ár og pantanir viðskiptavina sem eru settar langt umfram venjulegs afhendingartíma.

Þekjutímamörk er fjöldi daga eftir daginn í dag (m.ö.o. dagsetningin þegar áætlunarkeyrslan er sett í gang) sem framboði og eftirspurn er sleppt. Til að koma í veg fyrir tafir þarf að ganga úr skugga um að tímamörk fyrir umfang séu lengri en afhendingartími alls. Sjálfgefna kerfisgildið er 100 dagar.

Hægt er að tilgreina þekjutímamörk á hverju eftirfarandi stigi:

- **Þekjuflokkur** – Hægt er að stilla sjálfgefin þekjutímamörk fyrir hvern þekjuflokk.
- **Vöruþekja** – Hægt er að hnekkja þekjutímamörkum sem eru fengin frá þekjuflokknum sem vöru er úthlutað.
- **Aðaláætlun** – Hægt er að hnekkja þekjutímamörkum sem eru fengin frá stillingum þekjuflokks og vöruþekju.

Eftirfarandi hlutar útskýra hvernig á að tilgreina þekjuflokk á hverju stigi.

## <a name="set-a-coverage-time-fence-for-a-coverage-group"></a>Setja upp þekjutímamörk fyrir þekjuflokk

Þegar þekjutímamörk eru tilgreind fyrir þekjuflokk gildir stillingin fyrir allar vörur (afurðir) sem tilheyra þeim flokki. Hins vegar er hægt að hnekkja stillingunum fyrir tilteknar vörur eða tilteknar aðaláætlanir.

Til að tilgreina þekjutímamörk fyrir þekjuflokk skal fylgja þessum skrefum.

1. Fara skal í **Aðaláætlanagerð \> Uppsetning \> Þekja \> þekjuflokkar**.
1. Veljið fyrirliggjandi þekjuflokk á listanum eða búið til nýjan þekjuflokk.
1. Í flýtiflipanum **Almennt** skal stilla reitinn **Þekjutímamörk (dagar)** á þann fjölda daga sem á að nota þekjutímamörkin fyrir þekjuflokkinn.

## <a name="set-a-coverage-time-fence-for-a-specific-item"></a>Velja þekjutímamörk fyrir tiltekna vöru

Sérhver vara (afurð) tilheyrir þekjuflokki. Ef engum þekjuflokki er úthlutað beint á vöru gildir sjálfgefinn þekjuflokkur. Sérhver vara erfir þekjutímamörk úr þekjuflokki sínum. Hins vegar er hægt að hnekkja þessum tímamörkum fyrir tilteknar vörur eftir þörfum.

Til að tilgreina þekjutímamörk fyrir tiltekna vöru skal fylgja þessum skrefum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veldu afurð úr hnitanetinu.
1. Á aðgerðasvæðinu, í flipanum **Áætlun**, í flokknum **Þekja**, skal velja **Vöruþekja**.
1. Á síðunni **Vöruþekja**, í flipanum **Yfirlit**, skal velja eða stofna línu fyrir svæðið þar sem á að stilla þekjutímamörk.
1. Veljið flipann **Almennt** til að opna stillingarnar fyrir valið svæði.
1. Veljið gátreitinn **Hnekkja stillingum þekjuflokks**.
1. Stillið reitinn **Þekjutímamörk (dagar)** á þann fjölda daga sem á að nota sem þekjutímamörk fyrir vöruna.

## <a name="set-a-coverage-time-fence-for-a-specific-master-plan"></a>Velja þekjutímamörk fyrir tiltekna vöru

Hægt er að tilgreina þekjutímamörk á hverju stigi aðaláætlunar. Á þennan hátt er hægt að skilgreina fjölda daga sem útreikningur aðaláætlanagerðar nær yfir fyrir aðaláætlun. Þessi stilling hnekkir öllum stillingum þekjutíma sem hafa verið skilgreindar fyrir hverja viðeigandi vöru og þekjuflokk.

Til að tilgreina Þekjutímamörk fyrir tiltekna aðaláætlun skal fylgja þessum skrefum.

1. Farið í **Aðaláætlanagerð \> Uppsetning \> Áætlanir \> Aðaláætlanir**.
1. Veljið fyrirliggjandi aðaláætlun í listanum eða stofnið nýja aðaláætlun.
1. Í flýtiflipanum **Tímamörk í dögum** skal stilla valkostinn **Þekja** á *Já*. Í svæðið undir valkostinum skal síðan færa inn fjölda daga sem á að nota sem þekjutímamörk fyrir aðaláætlunina.

## <a name="considerations-for-coverage-time-fences"></a>Til athugunar varðandi þekjutímamörk

Þegar verið er að setja upp þekjutímamörk skal íhuga eftirfarandi atriði:

- Þekjutímamörk hafa aðeins áhrif á innsláttargögn fyrir aðaláætlanagerð. Ef tafir koma upp gætu áætlaðar pantanir verið með dagsetningu sem kemur á eftir deginum í dag plús þekjutímamörkin.
- Þekjutímamörk eru tilgreind í almanaksdögum. Dagatöl sem nota virka daga hafa ekki áhrif á útreikning tímamarka. Til dæmis er alltaf litið á viku sem sjö daga jafnvel þótt helgar séu settar upp sem lokaðir dagar í vinnutímadagatalinu.
- Þarfafærslur verða ekki myndaðar fyrir neitt framboð og eftirspurn sem fellur utan við þekjutímamörk.
- Ef samþykkt framboð og eftirspurn fellur utan þekjutímamörkin verður því ekki hlaðið inn í vélina. Því kveikir það ekki á neinni áfyllingu og tafir verða ekki reiknaðar. Engu að síður ætti þessu framboði og eftirspurn ekki að vera eytt úr kerfinu.
- Frávik á magni öryggisbirgða (úr lágmarkslyklum) verður hunsað ef það fellur utan þekjutímamarka.
- Eftirspurn innan samstæðu verður hunsuð ef umbeðin sendingardagsetning sem er reiknuð er ekki innan þekjutímamarka. Athugið að fyrir innbyggða aðaláætlanagerð takmarkast eftirspurn innan samstæðu ekki við þekjutímamörk.
- Eftirspurnarspár verða hunsaðar ef dagsetning fjárhagsáætlunar er ekki innan þekjutímamarka. Athugið að fyrir innbyggða aðaláætlanagerð takmarkast eftirspurnarspár innan samstæðu ekki við þekjutímamörk.
- Fínstilling skipulagningar tekur tillit til tímabeltis. Hún tekur tillit til tímabeltis á svæðum framboðs og eftirspurn og tíma áætlunarkeyrslu. Til dæmis er aðaláætlanagerð ræst klukkan 11:00 þann 15. október frá svæði í Danmörku (tímabelti GMT+1) og Þekjutímamörk upp á tíu daga eru notuð. Í slíku tilfelli er framboð og eftirspurn frá svæði í Seattle (tímabelti GMT-8) haft með þangað til kl. 02:00 þann 25. október (= tíu sólarhringa eftir að aðaláætlanagerð var ræst mínus tímamismunur upp á níu klukkustundir). Athugið að innbyggð aðaláætlunarvél tekur aðeins tillit til dagsetningu tímamarkanna. Þess vegna getur útkoman verið önnur.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]