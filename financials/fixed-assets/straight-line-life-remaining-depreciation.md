---
title: "Línuleg afskrift eftirstandandi líftíma"
description: "Þessi grein gefur yfirlit yfir afskriftaaðferðina Línuleg afskrift eftirstandandi líftíma."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 765825ba43cad44b076ea6628d2787011e97fc57
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="straight-line-life-remaining-depreciation"></a>Línuleg afskrift eftirstandandi líftíma

[!include[banner](../includes/banner.md)]


Þessi grein gefur yfirlit yfir afskriftaaðferðina Línuleg afskrift eftirstandandi líftíma.

Þegar afskriftarregla fyrir eignir er sett upp og valið er **Línuleg á eftirstöðvum líftíma** í svæðinu **aðferð** í síðunni **afskriftarregla** ráðast afskriftir eignasem heyra undir þá afskriftarreglu er byggð á eftirstandandi líftíma eignarinnar. Þetta er að öllu jöfnu sama afskriftarupphæðin á hverju afskriftatímabili. Til að setja upp afskriftir fyrir Línuleg á eftirstöðvum líftíma, verður einnig að velja valkosti á svæðinu **afskriftarár** og **tímabilstíðni** á síðunni **afskriftareglur**. Valkostirnir sem eru tiltækir á svæðinu**tímabilstíðni** eru mismunandi eftir því sem valið er á svæðinu **afskriftarár**.

## <a name="select-a-depreciation-year"></a>Velja afskriftaár
Hægt er að velja annað hvort **Dagatal** eða **reikningsár** í svæðinu **afskriftarár** á **afskriftareglu** síðunni. Sjálfgefið gildi er **Dagatal**. Valið skilgreinir valmöguleikana sem í boði eru á svæðinu **tímabilstíðni**. Þetta svæði skilgreinir bókunardagsetningar uppsafnaðra afskrifta og magn þeirra yfir almanaksárið.

### <a name="calendar"></a>Dagatal

Ef **Dagatal** er valið í ***Afskriftarár*** reitnum, er gert ráðyrir ári sem er 1. Janúar til og með  31. Desember , jafnvel ef fjárhagsdagatalið hefur verið skilgreint annan hátt. **Dagatal** uppfærir afskriftargrundvöllinn 1. Janúar ár hvert. Yfirleitt er afskriftagrundvöllurinn bókað nettóvirði mínus hrakvirði. Í dæmunum hér að neðan er afskriftagrunnurinn deilistofninn í fyrstu segðinni í útreikningum í útreikningsdálkinum. Ef valið er **Dagatal** sem afskriftaár eru eftirfarandi valkostir tiltækir á svæðinu **tímabilstíðni**:

-   **Árleg** upphæð bókar 31. Desember.
-   **Mánaðarlega**bókar mánaðarlega upphæð við lok hvers almanaks mánaðar.
-   **Ársfjórðungslega**bókar upphæð ársfjórðungslega við lok hvers almanaksfjórðungs (31. mars, 30. júní, 30. september og 31. desember).
-   Valkosturinn **tvisvar á ári** bókar upphæð á hálfs árs fresti miðað við hálft almanaksár (30. júní og 31. desember).
-   Með **daglega** er afskriftarupphæð fyrir afskriftaraðferðina daglega bókuð með einni færslu daglega.

Til dæmis, ef valið er **Árlega**, eru árlegar afskriftir bókaðar aðeins einu sinni, 31. Desember ár hvert. Ef valið er **mánaðarlega** bókast afskriftirnar sem einn tólfta árlegrar afskriftaupphæðar mánaðarlega.

### <a name="fiscal"></a>Fjárhagur

Ef valið er **reikningsár**á svæðinu **afskriftarár** er línuleg afskrift eftirstandandi líftíma notuð. Afskrift er reiknuð á grundvelli fjárhagsára sem eftir eru. Til dæmis, fyrir fjárhagsárið 1. Júlí 2015 gegnum 30. Júní, 2016 byrjar útreikningur afskrifta þann 1. Júlí. Fjárhagsár getur verið lengra eða styttra en 12 mánuðir. Afskriftirnar eru leiðréttar fyrir hvert fjárhagstímabil. Lengd næsta fjárhagsárs ákvarðast af uppsetning fjárhagstímabila á síðunni**fjárhagsdagatöl**. Ef **reikningsár** er valið sem afskriftaár eru eftirfarandi valkostir tiltækir í svæðinu **tímabilstíðni**:

-   **Árlega** bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið sem eina upphæð á síðasta degi fjárhagsársins.
-   **Fjárhagstímabil** reiknar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið. Þessari upphæð er safnað upp í fjárhagstímabilin sem skilgreind eru á síðunni**fjárhagsdagatöl** fyrir fjárhagstímabilin sem eru skilgreind í fyrir bókina.

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Dæmi um Línuleg afskrift af óbreytt eign
eignin hefur eftirfarandi eiginleika:

|                     |        |
|---------------------|--------|
| Kaupverð    | 11.000 |
| Hrakvirði       | 1.000  |
| Afskriftargrundvöllur   | 10.000 |
| Líftími í árum  | 5      |
| Árleg afskrift | 2.000  |

Afskriftarupphæðin er sama ár hvert: (Kaupverð - hrakvirði) ÷ líftíma í árum

| Tímabil | Reiknuð upphæð árlegra afskrifta | Nettó bókfært verð við lok árs |
|--------|-----------------------------------------------|---------------------------------------|
| 1. ár | (11.000 – 1.000) ÷ 5 = 2.000                  | 9.000                                 |
| 2. ár | (9.000 – 1.000) ÷ 4 = 2.000                   | 7.000                                 |
| 3. ár | (7.000 – 1.000) ÷ 3 = 2.000                   | 5.000                                 |
| 4. ár | (5.000 – 1.000) ÷ 2 = 2.000                   | 3.000                                 |
| 5. ár | (3.000 – 1.000) ÷ 1 = 2.000                   | 1.000                                 |





