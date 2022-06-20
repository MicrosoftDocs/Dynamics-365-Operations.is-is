---
title: Efni Power BI fyrir áskriftargreiðslu
description: Þessi grein lýsir því hvað er innifalið í áskriftarreikningnum Microsoft Power BI efni.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8849961"
---
# <a name="subscription-billing-power-bi-content"></a>Efni Power BI fyrir áskriftargreiðslu

[!include[banner](../includes/banner.md)]

Þessi grein lýsir því hvað er innifalið í áskriftarreikningnum Microsoft Power BI efni. Það lýsir einnig hvernig eigi að fara í Power BI-skýrslur og veitir upplýsingar um gagnalíkan og einingar sem notaðar voru til að búa til efnið. 

## <a name="overview"></a>Yfirlit

Áskriftarreikningurinn Power BI efni var búið til fyrir áskriftarreikninga og stjórnendur. Það veitir helstu innheimtumælingar fyrir áskrift, svo sem mánaðarlegar endurteknar tekjur (MRR) fyrir innheimtuáætlanir, og lækkandi stöðu og fossupplýsingar fyrir frestun áætlana. Það notar gögnin úr innheimtuáætlunum og frestun áætlana til að veita yfirsýn yfir endurteknar tekjur og tekjur.

The Power BI efni hefur eftirfarandi þrjá flipa sem veita samtals fjórar greiningarskýrslur: 

- **Greining - MRR** – Þessi flipi veitir **Mánaðarleg endurtekin innheimta** skýrslu og **Upplýsingar um innheimtuáætlun** skýrslu.
- **Greining - Foss** – Þessi flipi veitir **Tekjufoss** skýrslu.
- **Greining - Minnkandi staða** – Þessi flipi veitir **Minnkandi jafnvægi** skýrslu.

## <a name="view-data-on-the-analytical-reports"></a>Skoða gögn um greiningarskýrslur

Áður en þú getur skoðað gögn um greiningarskýrslurnar verður þú að keyra reglubundið ferli sem býr til skýrslugögn fyrir hverja skýrslu. Þessi gögn sem skýrslurnar krefjast verður að búa til vegna þess að þau eru ekki geymd beint í gagnagrunninum. 

1. Fara til **Innheimta áskriftar \> Endurtekinn samningsreikningur \> Reglubundin verkefni \> MRR greiningarskýrsla lotuvinnsla**, og fylgdu þessum skrefum:

    1. Sláðu inn dagsetningarbil sem er ekki meira en þrjú ár.
    2. Valfrjálst: Settu upp endurtekið runuferli til að endurnýja gögnin reglulega.
    3. Veldu **Í lagi**.

2. Eftir að runuvinnunni er lokið skaltu fara á **Kerfisstjórnun \> Uppsetning \> Entity Store**, og endurnýjaðu **Skýrsla MRR** heildarmæling. 
3. Fara til **Innheimta áskriftar \> Frestun tekna og gjalda \> Reglubundin verkefni \> Vatnsgreiningarskýrsla lotuvinnsla**, og fylgdu þessum skrefum:

    1. Sláðu inn upphafsdagsetningu og lokadagsetningu sem spanna ekki meira en 26 tímabil. 
    2. Ef þú vilt skoða spáð magn fyrri tímabila á núverandi tímabili skaltu stilla á **Spá fyrri upphæðir á núverandi tímabili** valmöguleika til **Já**.
    3. Valfrjálst: Settu upp endurtekið runuferli til að endurnýja gögnin reglulega.
    4. Veldu **Í lagi**. 

4. Eftir að runuvinnunni er lokið skaltu fara á **Kerfisstjórnun \> Uppsetning \> Entity Store**, og endurnýjaðu **Fossskýrsla** heildarmæling.
5. Fara til **Innheimta áskriftar \> Frestun tekna og gjalda \> Reglubundin verkefni \> Úrvinnsla á lækkandi jafnvægi greiningarskýrslu lotuvinnslu**, og fylgdu þessum skrefum:

    1. Sláðu inn upphafsdagsetningu og lokadagsetningu sem spanna ekki meira en 26 tímabil. 
    2. Ef þú vilt skoða spáð magn fyrri tímabila á núverandi tímabili skaltu stilla á **Spá fyrri upphæðir á núverandi tímabili** valmöguleika til **Já**.
    3. Valfrjálst: Settu upp endurtekið runuferli til að endurnýja gögnin reglulega.
    4. Veldu **Í lagi**.

6. Eftir að runuvinnunni er lokið skaltu fara á **Kerfisstjórnun \> Uppsetning \> Entity Store**, og endurnýjaðu **Skýrsla um lækkandi stöðu** heildarmæling.

## <a name="accessing-the-power-bi-content"></a>Aðgangur að Power BI efni

Áskriftarreikningurinn Power BI innihald er sýnt í **Innheimta áskriftar** vinnurými.
