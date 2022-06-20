---
title: Búa til reikningslínur þegar lánardrottnareikningar eru fluttir inn
description: Þessi grein lýsir virkni til að búa til reikningslínur sjálfkrafa á reikningum lánardrottins þegar reikningar eru fluttir inn.
author: sunfzam
ms.date: 09/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: e745ab1fb39edf69fabd147e46e1da8cc98ba6e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903508"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Búa til reikningslínur þegar lánardrottnareikningar eru fluttir inn

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þessi grein lýsir virkni til að búa til reikningslínur sjálfkrafa á reikningum lánardrottins þegar reikningar eru fluttir inn.

Stundum innihalda reikningar lánardrottins takmarkaðar upplýsingar á borð við upplýsingar um viðtakendur og millisamtölur. Hins vegar innihalda þeir engar upplýsingar fyrir línuatriði. Þegar þú flytur inn reikninga verða reikningslínurnar sjálfkrafa búnar til, byggt á upplýsingum um samsvarandi innkaupapöntun.

Til að virkja sjálfvirka stofnun reikningslína skal fylgja þessum skrefum.

1.  Farðu í **Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**.
2.  Í flipanum **Sjálfvirkni lánardrottnareiknings** undir **Sjálfvirk stofnun línu fyrir innflutta reikninga** skal stilla valkostinn **Stofna reikningslínur sjálfkrafa** á **Já**. 
4.  Í **Veldu sjálfgefið magn fyrir sjálfvirka gerð reikningslína** reit, veldu magnið sem á að nota til að búa til reikningslínur sjálfkrafa:

    - **Pantað magn** – Línur verða búnar til úr innkaupapöntunarlínum. Þetta gildi er sjálfgefið gildi.
    - **Magn vörukvittunar** – Innkaupapöntunarnúmerið verður notað til að finna viðeigandi vörukvittanir. Það mun síðan nota magn á innhreyfingarskjali afurðar til að búa til reikningslínur.

## <a name="data-entity-changes"></a>Breytingar á gagnaeiningu

Til að styðja við virknina sem lýst er í þessari grein, er **Fyrirsögn lánardrottins reiknings** gagnaeining hefur verið endurbætt. Þremur reitum hefur verið bætt við:

- **Header OnlyImport** – Þessi reitur verður að vera stilltur á **Já** til að búa til línur fyrir reikningshausa.
- **PurchIdRange** – Listi yfir innkaupapöntunarnúmer. Reikningsnúmerin geta verið á ákveðnu bili, t.d. **INV0001..INV0009** (þar sem tveir punktar aðskilja upphaf og endi bilsins) eða ákveðin gildi á borð við **INV0001, INV0003, INV0006**. Allar innkaupapantanir verða að tilheyra sama lánardrottnalykli í reikningshausnum. Annars koma upp eftirfarandi villuboð: „Ekki tókst að búa til reikningslínur. Innkaupapantanir eru með aðra lánardrottnalykla.“
- **PackingslipRange** – Listi yfir númer innhreyfingarskjala afurða. Hægt er að búa til línur lánardrottnareiknings úr innhreyfingarskjölum afurða. Númer innhreyfingarskjala afurða eru hins vegar yfirleitt á lánardrottnareikningum. Sláðu inn númer innhreyfingarskjals afurðar í þennan reit eingöngu ef þú getur augljóslega fundið út hvaða innhreyfingarskjöl afurða eru fyrir tiltekna reikninga. Hægt er að búa til reikningslínur út frá innhreyfingarskjölum afurða. Ef þessi reitur er notaður er stillingin á **Veldu sjálfgefið magn fyrir sjálfvirka gerð reikningslína** sviði á **Færibreytur viðskiptaskulda** síða er hunsuð. 

**Takmörkun**: Ef þú slærð inn mörg númer innhreyfingarskjala afurða verða nokkrir lánardrottnareikningar í bið stofnaðir með sama reikningsnúmerið. Sameina þarf þá handvirkt áður en unnið er frekar úr reikningnum. Í framtíðarútgáfum ætlum við að sameina reikningana sjálfkrafa, þannig að takmörkunin verður fjarlægð.

Öll innhreyfingarskjöl afurða verða að tilheyra sama lánardrottnalykli í reikningshausnum.

## <a name="result"></a>Niðurstaða

Ef línur eru búnar til eru eftirfarandi skilaboð skráð í sjálfvirknisögu lánardrottinsreiknings: "Búa til reikningslínur sjálfkrafa: tókst."

Ef línur myndast ekki eru eftirfarandi villuboð skráð: "Búa til reikningslínur sjálfkrafa: Mistókst."
