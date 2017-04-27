---
title: "Afskriftir fyrir 125% bókfært virði"
description: "Þessi grein gefur yfirlit yfir afskriftaraðferðina 125 prósent bókfært virði."
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
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 8e89a57dda8f2d392483ed13c686ea97b74926b0
ms.openlocfilehash: 1a4f07ce983271f36a58adaded1aec50d24d9e25
ms.lasthandoff: 03/31/2017


---

# <a name="125-percent-reducing-balance-depreciation"></a>Afskriftir fyrir 125% bókfært virði

[!include[banner](../includes/banner.md)]


Þessi grein gefur yfirlit yfir afskriftaraðferðina 125 prósent bókfært virði.

Þegar afskriftaregla fyrir eignir er sett upp og valið er ** 125% bókfært virði** í skjámyndinni **Aðferð** á síðunni **Afskriftarreglur**eru eignir sem eru tengdar þessari afskriftareglu, afskrifaðar með sama hlutfall af hundraði á hverju afskriftatímabili. Þessi prósenta er reiknuð á grundvelli líftíma eignarinnar. Til dæmis, ef eign hefur líftímann fimm ár, er prósentan reiknuð sem 25 prósent°(125% ÷ 5).

Til að setja upp afskriftir fyrir 125% bókfært virði, verður einnig að velja valkosti á svæðinu **Afskriftarár** og svæðið **Tímabilstíðni** á síðunni **Afskriftareglur**. Valkostirnir sem eru tiltækir á svæðinu**tímabilstíðni** eru mismunandi eftir því sem valið er á svæðinu **afskriftarár**.

## <a name="select-a-depreciation-year"></a>Velja afskriftaár
Hægt er að velja annað hvort **Dagatal** eða **reikningsár** í svæðinu **afskriftarár** á **afskriftareglu** síðunni. Sjálfgefið gildi er **Dagatal**. 

Valið skilgreinir valmöguleikana sem í boði eru á svæðinu **tímabilstíðni**. Þetta svæði skilgreinir bókunardagsetningar uppsafnaðra afskrifta og magn þeirra yfir almanaksárið.

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

Ef valið er **Fjárhagsárs** á svæðinu **Afskriftarár** er 125% afskrift af bókfærðu virði reiknað á grundvelli fjárhagsárs fyrir fjárhagsdagatalið sem tilgreint er fyrir bókina eða fyrir fjárhagsdagatalið sem valin er á síðunni **Fjárhagur**. Fjárhagsdagatöl eru sett upp á síðunni **fjárhagsdagatöl**. 

Fyrir fjárhagsárið 1. júlí til 30. júní, byrjar útreikningur afskrifta til dæmis þann 1. júlí. Fjárhagsár getur verið lengra eða styttra en 12 mánuðir. Afskriftirnar eru leiðréttar sjálfkrafa fyrir hvert tímabil og lengd næsta fjárhagsárs ákvarðast af uppsetningu tímabila á síðunni **Fjárhagsdagatöl**. 

Ef **reikningsár** er valið sem afskriftaár eru eftirfarandi valkostir tiltækir í svæðinu **tímabilstíðni**:

-   **Árlega**bókar heildarupphæð reiknaðra afskrifta°fyrir fjárhagsárið sem eina upphæð á síðasta degi fjárhagsársins.
-   **Reikningstímabil** bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið. Þessari upphæð er safnað upp í fjárhagstímabilin sem skilgreind eru á síðunni**fjárhagsdagatöl**.

## <a name="example-of-125-reducing-balance-depreciation"></a>Dæmi um afskriftir fyrir 125% bókfært virði
|                                |        |
|--------------------------------|--------|
| Kaupverð               | 11.000 |
| Hrakvirði                  | 1.000  |
| Afskriftargrundvöllur              | 10.000 |
| Líftími í árum             | 5      |
| Föst árleg afskriftaprósenta | 25%    |

Aðferðin afskriftir fyrir 125% bókfært virði deilir 125% með líftíma í árum. Það hlutfall af hundraði er margfaldað með bókuðu nettóvirði eignarinnar til að ákvarða afskriftarupphæð ársins.

| Tímabil | Reiknuð upphæð árlegra afskrifta | Bókfært verð                    | Nettó bókfært verð við lok árs |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| 1. ár | (11.000 – 1.000) × 25% = 2.500                | (11.000 – 2.500) = 8.500      | (11.000 – 1.000 – 2.500) = 7.500      |
| 2. ár | 7.500 × 25% = 1.875                           | (8.500 – 1.875) = 6.625       | (7.500 – 1.875) = 5.625               |
| 3. ár | 5.625 × 25% = 1.406,25                        | (6.625 – 1.406.25) = 5.218.75 | (5.625 – 1.406.25) = 4.218.75         |

> [!NOTE] 
> Yfirleitt þegar upphæðin sem er reiknuð með því að nota 125% bókfært virði verður afskriftaraðferð lægri en upphæðin sem yrði reiknuð með því að nota línulega afskriftaaðferð er umbreyting yfir í línulega aðferð fyrir eftirstandandi líftíma.




