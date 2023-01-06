---
title: Áætlun um vísitölu neysluverðs
description: Í þessari grein er útskýrt hvernig á að búa til lista yfir áætlanir um vísitölu neysluverðs (CPI) sem þú færð af internetinu til að ákvarða hækkað gjald í áskriftarinnheimtu.
author: JodiChristiansen
ms.date: 11/04/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: f08b79ee00baab3713d9ccc24a7595b1de7a7768
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904874"
---
# <a name="consumer-price-index-schedule"></a>Áætlun um vísitölu neysluverðs

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að búa til, eyða, yfirfara og vinna úr áætlunum um vísitölu neysluverðs (CPI). Hægt er að nota CPI-áætlun til að ákvarða verð á neysluvörum og þjónustu sem þú setur inn sem greiðsluáætlunarlínur. Hægt er að nota CPI-áætlunina með hækkun og afsláttarverði á greiðsluáætlun eða vinna handvirkt úr henni til að uppfæra greiðsluupphæðir á greiðsluáætlunum. Hægt er að færa handvirkt inn CPI-áætlanir eða flytja þær inn með því að nota samsettar CPI-áætlunareiningar.

Til að bæta við CPI-áætlun skal fylgja þessum skrefum.

1. Á síðunni **Áætlun um vísitölu neysluverðs** skal velja **Ný**.
2. Í reitnum **Áætlun um vísitölu neysluverðs** er fært inn einkvæmt heiti.
3. Í reitnum **Lýsing** skal færa inn lýsingu.
4. Á flipanum **Áætlun um vísitölu neysluverðs** skal velja **Bæta við**.
5. Í reitnum **Dagsetning á vísitölu neysluverðs** skal tilgreina dagsetninguna þegar ný CPI-áætlun verður virk.
6. Í reitnum **Áætlun um vísitölu neysluverðs** er fært inn heitið sem var fært inn í skrefi 2.
7. Veldu **Vista**.

Til að eyða dagsetningu CPI-áætlunar skal fylgja þessum skrefum.

1. Á síðunni **Áætlun um vísitölu neysluverðs** er valin ein eða fleiri línur sem á að eyða og síðan er valið **Fjarlægja**.
2. Á aðgerðasvæðinu skal velja **Eyða** til að eyða allir CPI-áætluninni. Ekki er hægt að eyða völdu CPI-áætluninni ef hún tengist einhverri greiðsluáætlun.
3. Í aðgerðarúðunni velur þú **Ferli** til að uppfæra greiðsluáætlanir sem nota valda CPI-áætlun. Nýjustu CPI-dagsetningar og áætlunarupphæðir verða notaðar til að uppfæra verð á greiðsluáætlun.
4. Í flýtiflipanum **Úrvinnsla vísitölu neysluverðs** skaltu skoða uppfærða reiti **Númer greiðsluáætlunar**, **Vörunúmer**, **Upphafsdagsetning innheimtu**, **Lokadagsetning innheimtu**, **Dagsetning hækkunar**, og **Tíðni hækkunar** .

Eftir að CPI-áætlanir hafa verið settar upp er hægt að nota þær til hækkunar og breytinga á afsláttarverði á greiðsluáætlunum.

## <a name="cpi-calculation"></a>CPI-útreikningur

Í þessum dæmum er tímabilið frá 1. janúar 2020 til og með 31. desember 2022. Grunnhlutfall CPI (CPI-gildið þegar samningurinn hefst) er 105,65. Þann 1. janúar 2021 er CPI gildi 110,5. Þann 1. janúar 2022 er núverandi CPI 114,25. Upphafleg upphæð er $1.000.

**Dæmi 1**

Á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur** stillirðu reitinn **Útreikningur á vísitölu neysluverðs** á **Grunnvísitölu neysluverðs**.

Á tímabilinu 1. janúar 2021 er fyrsta hækkunarupphæðin reiknuð á eftirfarandi hátt miðað við upphaflega upphæð:

1.000 + (110,5 – 105,65) &divide; 105,65 &times; 1.000 = 1.045,91

Á tímabilinu 1. janúar 2022 er hækkunin reiknuð út á eftirfarandi hátt:

1.000 + (114,25 – 105,65) &divide; 105,65 &times; 1000 = 1.081,40

**Dæmi 2**

Á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur** stillir þú reitinn **Útreikningur á vísitölu neysluverðs** á **Fyrri vísitala neysluverðs**.

Á tímabilinu 1. janúar 2021 er fyrsta hækkunarupphæðin reiknuð á eftirfarandi hátt miðað við upphaflega upphæð:

1.000 + (110,5 – 105,65) &divide; 105,65 &times; 1.000 = 1.045,91

Á tímabilinu 1. janúar 2022 er hækkunarupphæðin reiknuð á eftirfarandi hátt miðað við upphaflega hækkunarupphæð:

1.045,91 + (114,25 – 110,5) &divide; 110,5 &times; 1.045,91 = 1.081,40

> [!NOTE]
> Hækkunarferlið notar alltaf nýjasta CPI-gildið, óháð dagsetningu vísitölunnar. Ef hækkunin er til dæmis í september en nýjasta gildi CPI er fyrir júlí er júlístuðullinn notaður. Engar leiðréttingar eru gerðar eftir að septembervísitalan er slegin inn.

## <a name="prorated-escalation"></a>Hlutfallsleg hækkun

Ef hækkun á sér stað á miðju reikningstímabili er upphæðin hlutfallsleg. Til dæmis er greiðslutímabilið frá 1. ágúst 2020 til og með 31. júlí 2021. Á CPI-deginum 1. september 2019 er CPI-gildið 244. Á CPI-deginum 1. september 2020 er þetta CPI-gildi 250. Ef fyrra verð er 1.000 eru eftirfarandi formúlur notaðar til að reikna út greiðsluupphæð tímabilsins:

* *CPI-breytingar* = (250 – 244) &divide; 244 = 2,459%
* *Núverandi hlutfall* = (1.000 &times; 2,459%) = 1.024,59
* *Fjöldi daga á núverandi gengi* = 31. júlí 2021 – 1. september 2020 = 334
* *Fyrra hlutfall* = 1.000
* *Fjöldi daga á fyrra gengi* = 31. ágúst 2020 – 1. ágúst 2020 = 31
* *Heildarfjöldi daga á reikningstímabilinu* = 31. júlí 2021 – 1. ágúst 2020 + 1 = 365
* *Greiðsluupphæð fyrir þetta tímabil* = (1.000 &times; 31 &divide; 365) + (1.024,59 &times; 334 &divide; 365) = 1.022,50

## <a name="escalation-that-uses-the-cpi-and-percentage"></a>Hækkun sem notar CPI og prósentu

Hækkanir má framkvæma með því að nota CPI. CPI plús þriggja prósenta hækkun hefst 1. janúar 2020 og er árlegt.

- Upphæðin sem er skuldfærð fyrir 1. janúar 2019 til og með 31. desember 2020 er 4.000 kr.
- Greiðslutímabil hækkunar er frá 1. janúar 2020 til og með 31. desember 2020.
- Á CPI-deginum 1. desember 2018 er CPI-gildið 205,3. Á CPI-deginum 1. desember 2019 er CPI-gildið 219,6.

Ef fyrra verð er 4.000 er greiðsluupphæðin fyrir þetta tímabil reiknuð á eftirfarandi hátt:

- *CPI-breytingar* = (219,6 – 205,3) &divide; 205,3 = 6,965%
- *Núverandi hlutfall* = (4.000 &times;6,965%) – 4000 = 278,60
- *Prósentubreytingar* = (4.000 = &times; 1,03) – 4,000 = 120
- *Upphæð reiknings* = 4.000 + 278,6 + 120 = 4.398,6
