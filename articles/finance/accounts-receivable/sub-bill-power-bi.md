---
title: Efni Power BI fyrir áskriftargreiðslu
description: Þessi grein lýsir því hvað er innifalið í Microsoft Power BI efni áskriftargreiðslunnar.
author: JodiChristiansen
ms.date: 04/13/2022
ms.topic: article
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-04-13
ms.openlocfilehash: 6cee01eb5b8bb8296b6e7f638b565c999ccc023e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849961"
---
# <a name="subscription-billing-power-bi-content"></a>Efni Power BI fyrir áskriftargreiðslu

[!include[banner](../includes/banner.md)]

Þessi grein lýsir því hvað er innifalið í Microsoft Power BI efni áskriftargreiðslunnar. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið. 

## <a name="overview"></a>Yfirlit

Power BI efni áskriftargreiðslunnar var búið til fyrir bókara og stjórnendur áskriftargreiðslu. Þar er að finna helstu mælingar á áskriftargreiðslu, t.d. mánaðarlegar endurteknar tekjur (MRR) fyrir greiðsluáætlanir og hlutfallsstöðu og dreifingarupplýsingar fyrir frestunaráætlanir. Það notar gögn úr greiðsluáætlunum og frestunaráætlunum til að gefa yfirlit yfir endurtekið innstreymi og tekjur.

Power BI efnið hefur eftirfarandi þrjá flipa sem gefa samtals fjórar greiningarskýrslur: 

- **Greiningar - MRR** – Þessi flipi býður upp á skýrsluna **Mánaðarlega endurtekin greiðsla** og skýrsluna **Upplýsingar um greiðsluáætlun**.
- **Greiningar - Dreifing** – Þessi flipi býður upp á skýrsluna **Tekjudreifing**.
- **Greiningar - Hlutfallsstaða** – Þessi flipi býður upp á skýrsluna **Hlutfallsstaða**.

## <a name="view-data-on-the-analytical-reports"></a>Skoða gögn í greiningarskýrslum

Áður en hægt er að skoða gögn í greiningarskýrslum þarf að keyra reglubundið ferli sem býr til skýrslugögnin fyrir hverja skýrslu. Þessi gögn sem skýrslurnar krefjast verða að vera búin til vegna þess að þau eru ekki vistuð beint í gagnagrunninum. 

1. Farðu í **Áskriftargreiðslur \> Endurteknar samningsgreiðslur \> Reglubundin verk \> Runuvinnsla MRR-greiningarskýrslu** og fylgdu þessum skrefum:

    1. Sláðu inn tímabil sem er ekki lengra en þrjú ár.
    2. Valfrjálst: Settu upp endurtekna runuvinnslu til að uppfæra gögnin reglulega.
    3. Veldu **Í lagi**.

2. Eftir að runuvinnslunni er lokið skal fara í **Kerfisstjórnun \> Uppsetning \> Einingaverslun** og uppfæra uppsafnaðar mælingar **MRR-skýrslu**. 
3. Farðu í **Áskriftargreiðslur \> Tekju- og kostnaðarfrestanir \> Reglubundin verk \> Runuvinnsla fyrir greiningarskýrslu dreifingar** og fylgdu þessum skrefum:

    1. Færðu inn upphafsdagsetningu og lokadagsetningu sem ná yfir ekki meira en 26 tímabil. 
    2. Ef þú vilt skoða áætlað magn síðustu tímabila á yfirstandandi tímabili skaltu stilla valkostinn **Spá fyrri upphæða á núverandi tímabili** á **Já**.
    3. Valfrjálst: Settu upp endurtekna runuvinnslu til að uppfæra gögnin reglulega.
    4. Veldu **Í lagi**. 

4. Eftir að runuvinnslunni lýkur skal fara í **Kerfisstjórnun \> Uppsetning \> Einingaverslun** og uppfæra uppsafnað mælingu **Dreifingarskýrslu**.
5. Farðu í **Áskriftargreiðslur \> Tekju- og kostnaðarfrestanir \> Reglubundin verk \> Runuvinnsla fyrir greiningarskýrslu hlutfallsstöðu** og fylgdu þessum skrefum:

    1. Færðu inn upphafsdagsetningu og lokadagsetningu sem ná yfir ekki meira en 26 tímabil. 
    2. Ef þú vilt skoða áætlað magn síðustu tímabila á yfirstandandi tímabili skaltu stilla valkostinn **Spá fyrri upphæða á núverandi tímabili** á **Já**.
    3. Valfrjálst: Settu upp endurtekna runuvinnslu til að uppfæra gögnin reglulega.
    4. Veldu **Í lagi**.

6. Eftir að runuvinnslunni lýkur skal fara í **Kerfisstjórnun \> Uppsetning \> Einingaverslun** og uppfæra uppsafnaða mælingu **Skýrsla um hlutfallsstöðu**.

## <a name="accessing-the-power-bi-content"></a>Aðgangur að Power BI efni

Power BI efni áskriftargreiðslunnar er sýnt á vinnusvæðinu **Áskriftargreiðslur**.
