---
title: Búa til reikningslínur þegar lánardrottnareikningar eru fluttir inn
description: Þessi grein lýsir virkninni við að búa sjálfkrafa til reikningslínur í reikningum lánardrottins þegar reikningar eru fluttir inn.
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
ms.openlocfilehash: 5cb2c1234de03e9777921c18e4cbb81eec7feef9
ms.sourcegitcommit: 9c637bcf4e2eb8f711290a861492f038feaf1568
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2022
ms.locfileid: "9462275"
---
# <a name="generate-invoice-lines-when-you-import-vendor-invoices"></a>Búa til reikningslínur þegar lánardrottnareikningar eru fluttir inn

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Þessi grein lýsir virkninni við að búa sjálfkrafa til reikningslínur í reikningum lánardrottins þegar reikningar eru fluttir inn.

Stundum innihalda reikningar lánardrottins takmarkaðar upplýsingar á borð við upplýsingar um viðtakendur og millisamtölur. Hins vegar innihalda þeir engar upplýsingar fyrir línuatriði. Þegar þú flytur inn reikninga verða reikningslínur sjálfkrafa búnar til byggðar á upplýsingum í samsvarandi innkaupapöntun.

Til að virkja sjálfvirka stofnun reikningslína skal fylgja þessum skrefum.

1.  Farðu í **Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**.
2.  Í flipanum **Sjálfvirkni lánardrottnareiknings** undir **Sjálfvirk stofnun línu fyrir innflutta reikninga** skal stilla valkostinn **Stofna reikningslínur sjálfkrafa** á **Já**. 
4.  Í reitnum **Velja sjálfgefið magn fyrir sjálfvirka stofnun reikningslína** skal velja magnið sem á að nota til að búa til reikningslínur sjálfkrafa:

    - **Pantað magn** – Línur verða til úr innkaupapöntunarlínum. Þetta gildi er sjálfgefið gildi.
    - **Magn á innhreyfingarskjali afurðar** – Innkaupapöntunarnúmerið verður notað til að finna viðeigandi innhreyfingarskjöl afurða. Það mun síðan nota magn á innhreyfingarskjali afurðar til að búa til reikningslínur.

## <a name="data-entity-changes"></a>Breytingar á gagnaeiningu

Til að styðja við virknina sem er lýst í þessari grein hefur gagnaeiningin **Reikningshaus lánardrottins** verið bætt. Þremur reitum hefur verið bætt við:

- **HeaderOnlyImport** – Þessi reitur verður að vera stilltur á **Já** til að búa til línur fyrir reikningshausa.
- **PurchIdRange** – Listi yfir innkaupapöntunarnúmer. Reikningsnúmerin geta verið á ákveðnu bili, t.d. **PO0001..PO0009** (þar sem tveir punktar aðskilja upphaf og endi bilsins) eða ákveðin gildi á borð við **PO0001, PO0003, PO0006**. Allar innkaupapantanir verða að tilheyra sama lánardrottnalykli í reikningshausnum. Annars koma upp eftirfarandi villuboð: „Ekki tókst að búa til reikningslínur. Innkaupapantanir eru með aðra lánardrottnalykla.“
- **PackingslipRange** – Listi yfir númer innhreyfingarskjala afurða. Hægt er að búa til línur lánardrottnareiknings úr innhreyfingarskjölum afurða. Númer innhreyfingarskjala afurða eru hins vegar yfirleitt á lánardrottnareikningum. Sláðu inn númer innhreyfingarskjals afurðar í þennan reit eingöngu ef þú getur augljóslega fundið út hvaða innhreyfingarskjöl afurða eru fyrir tiltekna reikninga. Hægt er að búa til reikningslínur út frá innhreyfingarskjölum afurða. Ef þessi reitur er notaður er stillingin á reitnum **Velja sjálfgefið magn fyrir sjálfvirka stofnun reikningslína** á síðunni **Færibreytur viðskiptaskulda** hunsuð. 

**Takmörkun**: Ef þú slærð inn mörg númer innhreyfingarskjala afurða verða nokkrir lánardrottnareikningar í bið stofnaðir með sama reikningsnúmerið. Sameina þarf þá handvirkt áður en unnið er frekar úr reikningnum. Í næstu útgáfum er ráðgert að gera það kleift að sameina reikninga sjálfkrafa þannig að takmörkunin verður fjarlægð.

Öll innhreyfingarskjöl afurða verða að tilheyra sama lánardrottnalykli í reikningshausnum.

## <a name="result"></a>Niðurstaða

Ef línur takast eru eftirfarandi skilaboð skráð í sjálfvirkniferil lánardrottnareiknings: „Stofna reikningslínur sjálfkrafa: Tókst.“

Ef ekki tekst að búa til línur eru eftirfarandi villuboð skráð: „Stofna reikningslínur sjálfkrafa: Mistókst.“
