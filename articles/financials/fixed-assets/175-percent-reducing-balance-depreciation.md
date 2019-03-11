---
title: 175 prósenta lækkandi afskrift
description: Þetta efnisatriði gefur yfirlit yfir 175 prósent afskriftaraðferðina bókfært virði.
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a63293dbf24c27733f8013947aeab5792fa0db9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "320168"
---
# <a name="175-percent-reducing-balance-depreciation"></a>175 prósenta lækkandi afskrift

[!include [banner](../includes/banner.md)]

Þetta efnisatriði gefur yfirlit yfir 175 prósent afskriftaraðferðina bókfært virði.

Þegar afskriftaregla fyrir eignir er sett upp og gildið **175% bókfært virði** í reitnum **Aðferð** reitnum á **Afskriftarreglur** síðunni eru eignir sem er úthlutað á þessa afskriftareglu afskrifaðar með sömu prósentu á hverju afskriftatímabili. 

Til að setja upp afskriftir fyrir 175% bókfært virði, verður einnig að velja valkosti í á **afskriftarár** svæði og **tímabilstíðni** á í **afskriftareglur** síðu. Valkostirnir sem eru tiltækir á svæðinu**tímabilstíðni** eru mismunandi eftir því sem valið er á svæðinu **afskriftarár**.

## <a name="select-a-depreciation-year"></a>Velja afskriftaár
Hægt er að velja annað hvort **Dagatal** eða **reikningsár** í svæðinu **afskriftarár** á **afskriftareglu** síðunni. Sjálfgefið gildi er **Dagatal**. 

Valið skilgreinir valmöguleikana sem í boði eru á svæðinu **tímabilstíðni**. Þetta svæði skilgreinir bókunardagsetningar uppsafnaðra afskrifta og magn þeirra yfir almanaksárið.

### <a name="calendar"></a>Dagatal

Það er hægt að velja að halda sjálfgefnum gildum í svæðinu **afskriftarár**,**dagatal**. 

**Dagatal** uppfærir afskriftargrundvöllinn 1. Janúar ár hvert. Yfirleitt er afskriftagrundvöllurinn bókað nettóvirði mínus hrakvirði. Í dæmunum hér að neðan er afskriftagrunnurinn deilistofninn í fyrstu segðinni í útreikningum í útreikningsdálkinum. 

Ef valið er **Dagatal** sem afskriftaár eru eftirfarandi valkostir tiltækir á svæðinu **tímabilstíðni**:

-   **Árleg** upphæð bókar 31. Desember.
-   **Mánaðarlega**bókar mánaðarlega upphæð við lok hvers almanaks mánaðar.
-   **Ársfjórðungslega**bókar upphæð ársfjórðungslega við lok hvers almanaksfjórðungs (31. mars, 30. júní, 30. september og 31. desember).
-   **Tvisvar á ári**bókar upphæð á hálfs árs fresti miðað við hálft almanaksár (30. júní og 31. desember).
-   Með **Daglega** er afskriftarupphæð fyrir afskriftaraðferðina daglega bókuð með einni færslu daglega.

### <a name="fiscal"></a>Fjárhagur

Ef valið er **Fjárhagsárs** á svæðinu **Afskriftarár** er 175% afskrift af bókfærðu virði reiknað á grundvelli fjárhagsárs fyrir fjárhagsdagatalið sem tilgreint er fyrir bókina eða fyrir fjárhagsdagatalið sem valin er á síðunni **Fjárhagur**. Fjárhagsdagatöl eru sett upp á síðunni **fjárhagsdagatöl**. Fyrir nánari upplýsingar, sjá [Fjárhagsdagatöl, fjárhagsár, og tímabil.](../budgeting/fiscal-calendars-fiscal-years-periods.md)

Fyrir fjárhagsárið 1. júlí til 30. júní, byrjar útreikningur afskrifta til dæmis þann 1. júlí. Fjárhagsár getur verið lengra eða styttra en 12 mánuðir. Afskriftirnar eru leiðréttar sjálfkrafa fyrir hvert tímabil og lengd næsta fjárhagsárs ákvarðast af uppsetningu tímabila á síðunni **Fjárhagsdagatöl**. 

Ef **reikningsár** er valið sem afskriftaár eru eftirfarandi valkostir tiltækir í svæðinu **tímabilstíðni**:

-   **Árlega** bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið sem eina upphæð á síðasta degi fjárhagsársins.
-   **Fjárhagstímabil** reiknar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið. Þessari upphæð er safnað upp í fjárhagstímabilin sem skilgreind eru á síðunni**fjárhagsdagatöl**.

## <a name="example-of-175-reducing-balance-depreciation"></a>Dæmi um afskriftir fyrir 175% bókfært virði

|                                |        |
|--------------------------------|--------|
| Kaupverð               | 11.000 |
| Hrakvirði                  | 1.000  |
| Afskriftargrundvöllur              | 10.000 |
| Líftími í árum             | 5      |
| Föst árleg afskriftaprósenta | 35%    |

Aðferðin afskriftir fyrir 175% bókfært virði stöðu deilir 175% með líftíma í árum. Það hlutfall af hundraði er margfaldað með bókuðu nettóvirði eignarinnar til að ákvarða afskriftarupphæð ársins.

| Tímabil | Reiknuð upphæð árlegra afskrifta | Bókfært verð                  | Nettó bókfært verð við lok árs |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| 1. ár | (11,000 – 1,000) × 35% = 3,500                | 11.000 – 3.500 = 7.500      | 11.000 – 1.000 – 3.500 = 6.500        |
| 2. ár | 6,500 × 35% = 2,275                           | 7,500 – 2,275 = 5,225       | 6,500 – 2,275 = 4,225                 |
| 3. ár | 4,225 × 35% = 1,478.75                        | 5.225 – 1.478,75 = 3.746,25 | 4,225 – 1,478.75 = 2,746.25           |

> [!NOTE] 
> Yfirleitt þegar upphæðin sem er reiknuð með því að nota 175% bókfært virði verður afskriftaraðferð lægri en upphæðin sem yrði reiknuð með því að nota línulega afskriftaaðferð er umbreyting yfir í línulega aðferð fyrir eftirstandandi líftíma.



