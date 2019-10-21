---
title: Afskriftir fyrir 200% bókfært virði
description: Þessi grein gefur yfirlit yfir afskriftaraðferðina 200 prósent bókfært virði.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0474a8cecccaf1e23874458c27e0bea991140b6c
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187430"
---
# <a name="200-percent-reducing-balance-depreciation"></a>Afskriftir fyrir 200% bókfært virði

[!include [banner](../includes/banner.md)]

Þessi grein gefur yfirlit yfir afskriftaraðferðina 200 prósent bókfært virði.

Þegar afskriftarregla fyrir eignir er sett upp og gildið **200% bókfært virði** er valið í reitnum **Aðferð** á **Afskriftarreglur** eru eignaafskriftir, sem eru tengdar þessari afskriftareglu, með sama hlutfall af hundraði á hverju afskriftatímabili. Þessi prósenta er byggist á líftíma eignarinnar. Til dæmis, ef eign er með líftíma fimm ár, er prósenta reiknuð sem 40 prósent (200% ÷ 5). 

Þessi aðferð er einnig þekkt sem stiglækkandi afskrift .

Til að setja upp afskriftir fyrir 200% bókfært virði, verður einnig að velja valkosti á svæðinu **Afskriftarár** og á svæðinu **Tímabilstíðni** á síðunni **Afskriftareglur** síðu. Valkostirnir sem eru tiltækar á svæðinu **Tímabilstíðni** eru mismunandi eftir því gildi sem valið er á svæðinu **Afskriftarár**.

## <a name="select-a-depreciation-year"></a>Velja afskriftaár
Hægt er að velja annað hvort **Dagatal** eða **reikningsár** í svæðinu **afskriftarár** á **afskriftareglu** síðunni. Sjálfgefið gildi er **Dagatal**. 

Valið skilgreinir valmöguleikana sem í boði eru á svæðinu **tímabilstíðni**. Þetta svæði skilgreinir bókunardagsetningar uppsafnaðra afskrifta og magn þeirra yfir almanaksárið.

### <a name="calendar"></a>Dagatal

Hægt er að velja að halda sjálfgefnum gildum í reitnum **Afskriftarár**, **Dagatal**. 

**Dagatal** uppfærir afskriftargrundvöllinn 1. Janúar ár hvert. Yfirleitt eru afskriftir bókað nettóvirði mínus hrakvirði. Í dæmunum hér að neðan er afskriftagrunnurinn deilistofninn í fyrstu segðinni í útreikningum í útreikningsdálkinum. 

Ef valið er **Dagatal** sem afskriftaár eru eftirfarandi valkostir tiltækir á svæðinu **tímabilstíðni**:

-   **Árleg** upphæð bókar 31. Desember.
-   **Mánaðarlega** bókar mánaðarlega upphæð við lok hvers almanaks mánaðar.
-   **Ársfjórðungslega** bókar upphæð ársfjórðungslega við lok hvers almanaksfjórðungs (31. mars, 30. júní, 30. september og 31. desember).
-   **Tvisvar á ári** bókar upphæð á hálfs árs fresti miðað við hálft almanaksár (30. júní og 31. desember).
-   Með **Daglega** er afskriftarupphæð fyrir afskriftaraðferðina daglega bókuð með einni færslu daglega.

### <a name="fiscal"></a>Fjárhagur

Ef valið er **Fjárhagsárs** á svæðinu **Afskriftarár** er 200% afskrift af bókfærðu virði reiknað á grundvelli fjárhagsárs fyrir fjárhagsdagatalið sem tilgreint er fyrir bókina eða fyrir fjárhagsdagatalið sem valin er á síðunni **Fjárhagur**. Fjárhagsdagatöl eru sett upp á síðunni **fjárhagsdagatöl**. 

Fyrir fjárhagsárið 1. júlí til 30. júní, byrjar útreikningur afskrifta til dæmis þann 1. júlí. Fjárhagsár getur verið lengra eða styttra en 12 mánuðir. Afskriftirnar eru leiðréttar fyrir hvert tímabil. Lengd næsta fjárhagsárs ákvarðast af uppsetning tímabila á síðunni **Fjárhagsdagatöl**. 

Ef **Fjárhags** er valið sem afskriftaár eru eftirfarandi valkostir tiltækir á svæðinu **Tímabilstíðni**:

-   **Árlega** bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið sem eina upphæð á síðasta degi fjárhagsársins.
-   **Reikningstímabil** bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið. Þessari upphæð er safnað upp í fjárhagstímabilin sem skilgreind eru á síðunni **Fjárhagsdagatöl**.

## <a name="example-of-200-reducing-balance-depreciation"></a>Dæmi um afskriftir fyrir 200% bókfært virði

|                                |        |
|--------------------------------|--------|
| Kaupverð               | 11.000 |
| Hrakvirði                  | 1, 000 |
| Afskriftargrundvöllur              | 10.000 |
| Líftími í árum             | 5      |
| Föst árleg afskriftaprósenta | 40%    |

Afskriftir fyrir 200% bókfært virði stöðu aðferð deilir 200% með líftíma í árum. Það hlutfall af hundraði er margfaldað með bókuðu nettóvirði eignarinnar til að ákvarða afskriftarupphæð ársins.

| Tímabil | Reiknuð upphæð árlegra afskrifta | Bókfært verð             | Nettó bókfært verð við lok árs |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| 1. ár | (11.000 – 1.000) × 40% = 4.000                | 11.000 – 4.000 = 7.000 | 11.000 – 1.000 – 4.000 = 6.000        |
| 2. ár | 6.000 × 40% = 2.,400                           | 7.000 – 2.400 = 4.600  | 6.000 – 2.400 = 3.600                 |
| 3. ár | 3.600 × 40% = 1.440                           | 4.600 – 1.440 = 3.160  | 3.600 – 1.440 = 2.160                 |

> [!NOTE] 
> Yfirleitt þegar upphæðin sem er reiknuð með því að nota 200% bókfært virði verður afskriftaraðferð lægri en upphæðin sem yrði reiknuð með því að nota línulega afskriftaaðferð er umbreyting yfir í línulega aðferð fyrir°eftirstandandi líftíma.



