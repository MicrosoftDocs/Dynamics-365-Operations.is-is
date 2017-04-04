---
title: "Afskriftir fyrir 150% bókfært virði"
description: "Þessi grein gefur yfirlit yfir afskriftaraðferðina 150 prósent bókfært virði."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: d256feeadcf19550995c145f4e9a171acaeaeec3
ms.lasthandoff: 03/31/2017


---

# <a name="150-percent-reducing-balance-depreciation"></a>Afskriftir fyrir 150% bókfært virði

Þessi grein gefur yfirlit yfir afskriftaraðferðina 150 prósent bókfært virði.

Þegar afskriftaregla fyrir eignir er sett upp og gildið **150% af bókfærðu virði**er valið í svæðinu**aðferð** á skjámyndinni**afskriftaaðferðir** eru eignaafskriftir, sem eru tengdar þessari afskriftareglu, með sama hlutfall af hundraði á hverju afskriftatímabili. Þessi prósenta er reiknuð á grundvelli líftíma eignarinnar. Til dæmis, ef eign hefur líftíminn fimm ár, er prósenta reiknuð sem 30 prósent (150% ÷ 5). 

Til að setja upp afskriftir fyrir 150% bókfært virði, verður einnig að velja valkosti á svæðinu **afskriftarár** og **tímabilstíðni** á síðunni **afskriftareglur**. Valkostirnir sem eru tiltækir á svæðinu**tímabilstíðni** eru mismunandi eftir því sem valið er á svæðinu **afskriftarár**.

## <a name="selection-of-depreciation-year"></a>Val afskriftarárs
Hægt er að velja annað hvort **Dagatal** eða **reikningsár** í svæðinu **afskriftarár** á **afskriftareglu** síðunni. 

Sjálfgefið gildi er **Dagatal**. Valið skilgreinir valmöguleikana sem í boði eru á svæðinu **tímabilstíðni**. Þetta svæði skilgreinir bókunardagsetningar uppsafnaðra afskrifta og magn þeirra yfir almanaksárið.

### <a name="calendar"></a>Dagatal

Það er hægt að velja að halda sjálfgefnum gildum í svæðinu **afskriftarár, ****dagatal**. 

**Dagatal** uppfærir afskriftargrundvöllinn 1. Janúar ár hvert. Yfirleitt er afskriftagrundvöllurinn bókað nettóvirði mínus hrakvirði. Í dæmunum hér að neðan er afskriftagrunnurinn deilistofninn í fyrstu segðinni í útreikningum í útreikningsdálkinum. 

Ef valið er **Dagatal** sem afskriftaár eru eftirfarandi valkostir tiltækir á svæðinu **tímabilstíðni**:

-   **Árleg** upphæð bókar 31. Desember.
-   ** Mánaðarlega**bókar mánaðarlega upphæð við lok hvers almanaks mánaðar.
-   **Ársfjórðungslega**bókar upphæð ársfjórðungslega við lok hvers almanaksfjórðungs (31. mars, 30. júní, 30. september og 31. desember).
-   **Tvisvar á ári**bókar upphæð á hálfs árs fresti miðað við hálft almanaksár (30. júní og 31. desember).
-   Með ** Daglega** er afskriftarupphæð fyrir afskriftaraðferðina daglega bókuð með einni færslu daglega.

### <a name="fiscal"></a>Fjárhagur

Ef valið er **Fjárhagsárs** á svæðinu **Afskriftarár** er 150% afskrift af bókfærðu virði reiknað á grundvelli fjárhagsárs fyrir fjárhagsdagatalið sem tilgreint er fyrir bókina eða fyrir fjárhagsdagatalið sem valin er á síðunni **Fjárhagur**. Fjárhagsdagatöl eru sett upp á síðunni **fjárhagsdagatöl**. 

Til dæmis, fyrir fjárhagsárið 1. Júlí gegnum 30. Júní, byrjar útreikningur afskrifta þann 1. Júlí. Fjárhagsár getur verið lengra eða styttra en 12 mánuðir. Afskriftirnar eru leiðréttar fyrir hvert tímabil. Lengd næsta fjárhagsárs ákvarðast af uppsetning tímabila á síðunni**fjárhagsdagatöl**. 

Ef **reikningsár** er valið sem afskriftaár eru eftirfarandi valkostir tiltækir í svæðinu **tímabilstíðni**:

-   **Árlega** bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið sem eina upphæð á síðasta degi fjárhagsársins.
-   **Reikningstímabil** bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið. Þessari upphæð er safnað upp í fjárhagstímabilin sem skilgreind eru á síðunni**fjárhagsdagatöl**.

## <a name="example-of-150-reducing-balance-depreciation"></a>Dæmi um afskriftir fyrir 150% bókfært virði
|                                |        |
|--------------------------------|--------|
| Kaupverð               | 11.000 |
| Hrakvirði                  | 1.000  |
| Afskriftargrundvöllur              | 10.000 |
| Líftími í árum             | 5      |
| Föst árleg afskriftaprósenta | 30%    |

Aðferðin 150% bókfært virði stöðu deilir 150% með líftíma í árum. Það hlutfall af hundraði er margfaldað með bókuðu nettóvirði eignarinnar til að ákvarða afskriftarupphæð ársins.

| Tímabil | Reiknuð upphæð árlegra afskrifta | Bókfært verð             | Nettó bókfært verð við lok árs |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| 1. ár | (11,000 – 1,000) × 30% = 3,000                | 11.000 – 3.000 = 8.000 | 11.000 – 1.000 – 3.000 = 7.000        |
| 2. ár | 7,000 × 30% = 2,100                           | 8.000 – 2.100 = 5.900  | 7,000 – 2,100 = 4,900                 |
| 3. ár | 4,900 × 30% = 1,470                           | 5.900 – 1.470 = 4.430  | 4,900 – 1,470 = 3,430                 |

> [!NOTE]
> Venjulega er þegar upphæðin sem er reiknað með því að nota 150% bókfært virði afskriftaraðferð verður lægri en upphæðin sem á að reikna með því að nota línulega afskriftaaðferð er umbreyting yfir í línulega aðferð fyrir eftirstandandi líftíma.


