---
title: Áætlun um vísitölu neysluverðs
description: Þessi grein útskýrir hvernig á að búa til lista yfir vísitölu neysluverðs (VPI) áætlanir sem þú færð af internetinu til að hjálpa til við að ákvarða hækkunargjaldið í áskriftarreikningi.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904874"
---
# <a name="consumer-price-index-schedule"></a>Áætlun um vísitölu neysluverðs

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir hvernig á að búa til, eyða, endurskoða og vinna úr vísitölu neysluverðs (VNV). Hægt er að nota VNV áætlun til að ákvarða verð fyrir neysluvörur og þjónustu sem þú bætir við sem innheimtuáætlunarlínur. Þá er hægt að nota neysluverðsáætlunina með hækkun og afsláttarverðlagningu á innheimtuáætlun, eða hægt er að vinna hana handvirkt til að uppfæra innheimtuupphæðir á innheimtuáætlunum. Þú getur slegið inn kostnaðarverðsáætlanir handvirkt, eða þú getur flutt þær inn með því að nota samsetta eininguna VNV.

Fylgdu þessum skrefum til að bæta við VNV áætlun.

1. Á **Áætlun um vísitölu neysluverðs** síðu, veldu **Nýtt**.
2. Í **Áætlun um vísitölu neysluverðs** reit, sláðu inn einstakt nafn.
3. Í reitnum **Lýsing** skal færa inn lýsingu.
4. Á **Áætlun um vísitölu neysluverðs** flipa, veldu **Bæta við**.
5. Í **Vísitala neysluverðs dags** reit, tilgreindu dagsetninguna þegar nýja VNV áætlunin verður virk.
6. Í **Áætlun um vísitölu neysluverðs** reit, sláðu inn nafnið sem þú slóst inn í skrefi 2.
7. Veldu **Vista**.

Fylgdu þessum skrefum til að eyða áætlunardagsetningu VNV.

1. Á **Áætlun um vísitölu neysluverðs** síðu, veldu eina eða fleiri línur sem þú vilt eyða og veldu síðan **Fjarlægja**.
2. Til að eyða allri VNV áætluninni skaltu velja á Aðgerðarrúðunni **Eyða**. Þú getur ekki eytt völdum kostnaðarverðsáætlun ef hún er tengd einhverri innheimtuáætlun.
3. Á aðgerðarrúðunni velurðu **Ferli** til að uppfæra innheimtuáætlanir sem nota valda VNV áætlun. Nýjustu dagsetningar neysluverðs og áætlunarupphæðir verða notaðar til að uppfæra innheimtuáætlunarverð.
4. Á **Ferli vísitölu neysluverðs** Flýtiflipi, skoðaðu uppfærða **Númer innheimtuáætlunar**, **·**, **innheimtu**, **innheimtu**, **·**, og **Stækkunartíðni** sviðum.

Eftir að VNV áætlanir hafa verið settar upp er hægt að nota þær til að hækka og afslætti verðbreytingar á innheimtuáætlunum.

## <a name="cpi-calculation"></a>VNV útreikningur

Fyrir þessi dæmi er tímabilið frá 1. janúar 2020 til 31. desember 2022. Grunngengi neysluverðs (VNV gildi þegar samningur hefst) er 105,65. Þann 1. janúar 2021 er núverandi neysluverðsvísitala 110,5. Þann 1. janúar 2022 er núverandi neysluverðsvísitala 114,25. Upphafsupphæðin er $1,000.

**Dæmi 1**

Á **Endurteknar innheimtufæribreytur samnings** síðu, þú stillir **Útreikningur vísitölu neysluverðs** sviði til **Grunnvísitala neysluverðs**.

Fyrir tímabilið 1. janúar 2021 er fyrsta stigvaxandi upphæð reiknuð á eftirfarandi hátt miðað við upphaflega upphæð:

1.000 + (110,5 – 105,65)&divide; 105,65&times; 1.000 = 1.045,91

Fyrir tímabilið 1. janúar 2022 er hækkunarfjárhæð reiknuð á eftirfarandi hátt:

1.000 + (114,25 – 105,65)&divide; 105,65&times; 1.000 = 1.081,40

**Dæmi 2**

Á **Endurteknar innheimtufæribreytur samnings** síðu, þú stillir **Útreikningur vísitölu neysluverðs** sviði til **Fyrri vísitala neysluverðs**.

Fyrir tímabilið 1. janúar 2021 er fyrsta stigvaxandi upphæð reiknuð á eftirfarandi hátt miðað við upphaflega upphæð:

1.000 + (110,5 – 105,65)&divide; 105,65&times; 1.000 = 1.045,91

Fyrir tímabilið 1. janúar 2022 er hækkunarfjárhæð reiknuð á eftirfarandi hátt, miðað við fyrstu hækkunarfjárhæð:

1.045,91 + (114,25 – 110,5)&divide; 110,5&times; 1.045,91 = 1.081,40

> [!NOTE]
> Stækkunarferlið notar alltaf nýjasta VNV gildið, óháð vísitöludagsetningu. Til dæmis, ef hækkunin er í september, en nýjasta VNV gildið er fyrir júlí, er júlívísitalan notuð. Engar leiðréttingar eru gerðar eftir að septembervísitalan er færð inn.

## <a name="prorated-escalation"></a>Hlutfallsleg stigmögnun

Ef hækkunin á sér stað á miðju innheimtutímabili er upphæðin hlutfallsleg. Til dæmis er innheimtutímabilið frá 1. ágúst 2020 til 31. júlí 2021. Á VNV dagsetningunni 1. september 2019 er VNV gildið 244. Á VNV dagsetningunni 1. september 2020 er þetta VNV gildi 250. Ef fyrri taxti er 1.000 eru eftirfarandi formúlur notaðar til að reikna út reikningsupphæð tímabilsins:

* *Breytingar á VNV* = (250 – 244)&divide; 244 = 2,459%
* *Núverandi gengi* = 1.000&times; 2,459% = 1.024,59
* *Fjöldi daga á núverandi gengi* = 31. júlí 2021 – 1. september 2020 = 334
* *Fyrra gengi* = 1.000
* *Fjöldi daga á fyrra gengi* = 31. ágúst 2020 – 1. ágúst 2020 = 31. ágúst
* *Heildarfjöldi daga á reikningstímabilinu* = 31. júlí 2021 – 1. ágúst 2020 + 1 = 365
* *Innheimtuupphæð fyrir þetta tímabil* = (1.000&times; 31&divide; 365) + (1.024,59&times; 334&divide; 365) = 1.022,50

## <a name="escalation-that-uses-the-cpi-and-percentage"></a>Stækkun sem notar VNV og prósentu

Hækkanir er hægt að gera með því að nota VNV. Vísitala neysluverðs auk 3 prósenta hækkunar hefst 1. janúar 2020 og hefur árlega tíðni.

- Upphæðin sem er innheimt fyrir 1. janúar 2019, til og með 31. desember 2020, er 4.000.
- Innheimtutímabilið sem verður aukið er 1. janúar 2020, til og með 31. desember 2020.
- Á vísitölu neysluverðs 1. desember 2018 er vísitala neysluverðs 205,3. Á vísitölu neysluverðs 1. desember 2019 er vísitala neysluverðs 219,6.

Ef fyrri taxti er 4.000, er reikningsupphæð þessa tímabils reiknuð á eftirfarandi hátt:

- *Breytingar á VNV* = (219,6 – 205,3)&divide; 205,3 = 6,965%
- *Núverandi gengi* = (4.000&times; 6,965%) – 4000 = 278,60
- *Hlutfallsbreytingar* = (4.000&times; 1,03) – 4.000 = 120
- *Upphæð innheimtu* = 4.000 + 278,6 + 120 = 4.398,6
