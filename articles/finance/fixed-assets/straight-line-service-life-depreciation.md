---
title: Línulegar líftímaafskriftir
description: Þessi grein gefur yfirlit yfir afskriftaaðferðina Línulegar líftímaafskriftir.
author: ShylaThompson
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
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7b7b9b240156263b4dc1bc308a7f4457380a27f3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444413"
---
# <a name="straight-line-service-life-depreciation"></a>Línulegar líftímaafskriftir

[!include [banner](../includes/banner.md)]

Þessi grein gefur yfirlit yfir afskriftaaðferðina Línulegar líftímaafskriftir.

Þegar afskriftaregla fyrir eignir er sett upp og velur og línulegur líftími í reitnum Aðferð í síðunni afskriftareglu, eru eignirnar sem hafa þessa afskriftarreglu úthlutaða á sig afskrifaðar byggt á heildar líftíma eignar. Þetta er að öllu jöfnu sama afskriftarupphæðin á hverju afskriftatímabili. 

munurinn á afskriftarupphæðinni sem er reiknuð milli eftirstöðva beinlínulíftíma og beinlínu líftíma er þegar leiðrétting er bókuð á eignina. 

Til að setja upp afskriftir fyrir beinlínu líftíma, verður einnig að velja valkosti á svæðinu afskriftarár og reitum tímabilstíðni á síðunni afskriftareglur.

## <a name="select-a-depreciation-year"></a>Velja afskriftaár
Hægt er að velja annað hvort Dagatal eða Fjárhagsár á svæði fyrir afskriftarár á síðunni afskriftareglur. Valið skilgreinir valmöguleikana sem í boði eru á svæðinu tímabilstíðni. Sjálfgefinn kostur er dagatal.

### <a name="calendar"></a>Dagatal

Ef Dagatal er valið er gert ráð fyrir ári sem er 1. Janúar til 31. Desember , jafnvel ef fjárhagsdagatalið hefur verið skilgreint annan hátt. 

Valmöguleikinn dagatal uppfærir afskriftagrunninn (vanalega bókað nettóverð að frádregnu hrakvirði) þann 1. janúar ár hvert. Í dæmunum hér að neðan er afskriftagrunnurinn deilistofninn í fyrstu segðinni í útreikningum í útreikningsdálkinum. 

Ef dagatal er valið eru eftirfarandi valkostir á svæðinu tímabilstíðni, sem skilgreinir bókunardagsetningar uppsafnaðra afskrifta og upphæðir yfir allt almanaksárið:
-   Árleg upphæð bókar 31. Desember.
-   Valkosturinn mánaðarlega bókar mánaðarlega upphæð við lok hvers almanaksmánaðar
-   Valkosturinn ársfjórðungslega bókar upphæð ársfjórðungslega við lok hvers almanaksfjórðungs (31. mars, 30. júní, 30. september og 31. desember).
-   Valkosturinn tvisvar á ári bókar upphæð á hálfs árs fresti miðað við hálft almanaksár (30. júní og 31. desember).
-   Með valkostinum daglega er afskriftarupphæð fyrir afskriftaraðferðina daglega bókuð með einni færslu daglega.

Til dæmis, ef valið er Árlega, eru árlegar afskriftir bókaðar aðeins einu sinni, 31. Desember ár hvert. Ef valið er mánaðarlega bókast afskriftirnar sem 1/12 árlegrar afskriftaupphæðar mánaðarlega.

### <a name="fiscal"></a>Fjárhagur

Ef valið er reikningsár á svæðinu afskriftarár er afskrift línulegs líftíma notuð. Það reiknuð á grundvelli fjárhagsársins sem er skilgreindur eftir fjárhagsdagatalið sem tilgreindur er fyrir bók eða fjárhagsdagatal sem valinn er í Fjárhagssíðu. Fjárhagsdagatöl eru sett upp á síðunni fjárhagsdagatöl.

Fyrir fjárhagsárið 1. júlí til 30. júní, byrjar útreikningur afskrifta til dæmis þann 1. júlí. Fjárhagsár getur verið lengra eða styttra en 12 mánuðir. Afskriftirnar eru leiðréttar sjálfkrafa fyrir hvert fjárhagstímabil. Lengd næsta fjárhagsárs er byggt á fjárhagstímabilum sem sett eru upp þegar nýtt fjárhagsár er stofnað á skjámyndinni fjárhagsdagatöl. 

Ef fjárhagsár er valið eru eftirfarandi valkostir tiltækir á svæðinu tímabilstíðni:
-   Árlega bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið sem eina upphæð á síðasta degi fjárhagsársins.
-   Fjárhagstímabil reiknar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið sem er safnað upp í tímabilin sem eru skilgreind í skjámynd fjárhagsdagatals fyrir fjárhagsdagatal.

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a>Dæmi: Línuleg afskrift af óbreytt eign
Segjum sem svo að eignin hafi eftirfarandi eiginleika:

|                     |        |
|---------------------|--------|
| Kaupverð    | 11.000 |
| Hrakvirði       | 1.000  |
| Afskriftargrundvöllur   | 10.000 |
| Líftími í árum  | 5      |
| Árleg afskrift | 2.000  |

Sama afskriftarupphæð á hverju ári. (Kaupverð - Hrakvirði) / Líftími í árum

| Tímabil | Reiknuð árleg upphæð afskrifta | Nettó bókfært verð við lok árs |
|--------|-------------------------------------------|---------------------------------------|
| 1. ár | (11,000 - 1,000) / 5 = 2,000              | 9.000                                 |
| 2. ár | (11,000 - 1,000) / 5 = 2,000              | 7.000                                 |
| 3. ár | (11,000 - 1,000) / 5 = 2,000              | 5.000                                 |
| 4. ár | (11,000 - 1,000) / 5 = 2,000              | 3.000                                 |
| 5. ár | (11,000 - 1,000) / 5 = 2,000              | 1.000                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a>Dæmi: Línuleg afskrift af breyttri eign

Segjum sem svo að bætt sé við leiðrétting kaupa upp á 4,000 á 2. ári við sömu eignina. 

Líftími leiðréttingar kaupa er sú sama og eignarinnar og hefst við kaup þess. Nettó bókfært verð stendur eftir við lok 5. árs, sem samsvarar nettó bókfært verð kaupverðsbreytingarinnar. Afskriftirnar eftir tímabilum eru reiknaðar eins og sýnt er í eftirfarandi töflu.

| Tímabil | Reiknuð upphæð árlegra afskrifta | Nettó bókfært verð við lok árs |
|--------|-------------------------------------------|---------------------------------------|
| 1. ár | 10,000 / 5 = 2,000                        | 11.000 - 2.000 = 9.000                |
| 2. ár | 4.000 ( – Leiðrétting kaupa)            | 9,000 + 4,000 =13,000                 |
| 2. ár | 14,000 / 5 = 2,800                        | 13.000 - 2.800 = 10.200               |
| 3. ár | 14,000 / 5 = 2,800                        | 10,200 - 2,800 = 7,400                |
| 4. ár | 14,000 / 5 = 2,800                        | 7,400 - 2,800 = 4,600                 |
| 5. ár | 14,000 / 5 = 2,800                        | 4,600 - 2,800 = 1,800                 |
| 6. ár | Eftirstöðvar 800\*                           | 1,800 – 800 = 1,000                   |

\*Þar sem eftirstandandi upphæð eru lægri en afskriftarupphæðin eru aðeins eftirstöðvarnar, að frádregnu hrakvirði, teknar.





