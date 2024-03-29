---
title: Minnka bókfært virði
description: Þessi grein gefur yfirlit yfir afskriftaraðferðina bókfært virði.
author: moaamer
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52bf9d4e9cbc9cabda5d5ab17c1a00ecea0d0348
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883272"
---
# <a name="reduce-balance-depreciation"></a>Minnka bókfært virði

[!include [banner](../includes/banner.md)]

Þessi grein gefur yfirlit yfir afskriftaraðferðina bókfært virði.

Þegar afskriftaregla fyrir eignir er sett upp og bókfært virði er valið í á svæðinu **Aðferð** á skjámyndinni **afskriftarregla** verða eignir sem hafa þessa afskriftareglu afskrifaðar um sama hlutfall af hundraði á hverju afskriftatímabili.

Til að setja upp afskriftir fyrir bókfært virði verður einnig að velja í svæðunum á flýtiflipanum **almennt** í skjámyndinni fyrir **afskriftarregluna**. Fyrst skal velja ár í svæðinu **afskriftarár**. Mismunandi valmöguleikar birtast á svæðinu **tímabilstíðni** eftir því hvað valið er, svo sem útskýrt er í eftirfarandi köflum. 

Einnig verður að færa gildi í svæðið **Prósentuhlutfall** fyrir afskriftarregluna. Ef kosturinn **Full afskrift** er valinn er eftirstandandi afskriftagrunnur tekinn á síðasta afskriftatímabili, sem gæti verið há upphæð. Sum lönd/svæði nota ekki umskipti yfir í línulega afskriftaaðferð. Umskipti eiga sér stað þegar upphæð auka afskriftaraðferðar er hærri eða jöfn og upphæð aðalafskriftarreglunnar, þá verður afskriftarupphæðin sem er tekin upphæðin sem fengin er með aukaaðferðinni. 

Af því að eign afskrifast aldrei að fullu ef prósentureikningur er notaður verður að velja kostinn **Full afskrift** til að afskrifa eign að fullu.

## <a name="select-a-depreciation-year"></a>Velja afskriftaár
Hægt er að velja annað hvort **Dagatal** eða **reikningsár** í svæðinu **afskriftarár** á **afskriftareglu** síðunni. Valið skilgreinir valmöguleikana sem í boði eru á svæðinu **tímabilstíðni**. Sjálfgefinn kostur er **dagatal**.

### <a name="calendar"></a>Dagatal

Valmöguleikinn **dagatal** uppfærir afskriftagrunninn (vanalega bókað nettóverð að frádregnu hrakvirði) þann 1. janúar ár hvert. Í dæminu um afskriftir fyrir bókfært virði hér síðar í þessari grein er afskriftargrunnurinn deilistofninn í fyrstu segðinni í útreikningsdálkinum. 

Ef **dagatal** er valið eru eftirfarandi valkostir á svæðinu **tímabilstíðni**, sem skilgreinir bókunardagsetningar uppsafnaðra afskrifta og upphæðir yfir allt almanaksárið:

- Valkosturinn árlega bókar 31. desember.
- Valkosturinn mánaðarlega bókar mánaðarlega upphæð við lok hvers almanaksmánaðar
- Valkosturinn ársfjórðungslega bókar upphæð ársfjórðungslega við lok hvers almanaksfjórðungs (31. mars, 30. júní, 30. september og 31. desember).
- Valkosturinn tvisvar á ári bókar upphæð á hálfs árs fresti miðað við hálft almanaksár (30. júní og 31. desember).
- Með valkostinum daglega er afskriftarupphæð fyrir afskriftaraðferðina daglega bókuð með einni færslu daglega.

Til dæmis, ef valið er **Árlega**, eru árlegar afskriftir bókaðar aðeins einu sinni, 31. Desember ár hvert. Ef valið er **mánaðarlega** bókast afskriftirnar sem 1/12 árlegrar afskriftaupphæðar mánaðarlega.

### <a name="fiscal"></a>Fjárhagur

Ef valið er **reikningsár** á svæðinu **afskriftarár** er línulega afskriftaraðferðin notuð. Það er reiknað á grundvelli fjárhagsársins sem er sett upp á síðunni **Fjárhagsdagatöl** fyrir fjárhagsdagatalið sem valið er á síðunni **Fjárhagur**. Fyrir fjárhagsárið 1. júlí til 30. júní, byrjar útreikningur afskrifta til dæmis þann 1. júlí. Fjárhagsár getur verið lengra eða styttra en 12 mánuðir. Afskriftirnar eru leiðréttar fyrir hvert fjárhagstímabil. Lengd næsta fjárhagsárs er byggt á fjárhagstímabilum sem sett eru upp þegar nýtt fjárhagsár er stofnað á síðunni **fjárhagsdagatöl**.


Ef **fjárhagsár** er valið eru eftirfarandi valkostir tiltækir á svæðinu **tímabilstíðni**:

- Árlega bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið sem eina upphæð á síðasta degi fjárhagsársins.
- Fjárhagstímabil bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið, sem er safnað upp í fjárhagstímabilin sem skilgreind eru fyrir fjárhagsdagatalið sem valið er á síðunni **höfuðbók**, eða fyrir fjárhagsdagatalið sem valið er fyrir bók fyrir eign.

## <a name="example-of-reducing-balance-depreciation"></a>Dæmi um afskriftir fyrir bókfært virði

Segjum að kaupverð eignarinnar sé 11.000, rýrnunarvirðið sé 1.000 og prósentustuðull afskriftanna sé 30. 

Með því að nota aðferðina lækkandi afskrift eru 30 prósent af afskriftagrunninum (nettóvirði mínus rýrnunarvirði) reiknuð í lok fyrra afskriftatímabils. Afskriftir fyrstu þriggja áranna eru sýndar í eftirfarandi töflu:

| Tímabil | Reiknuð upphæð árlegra afskrifta | Nettó bókfært verð við lok árs |
|--------|-------------------------------------------|---------------------------------------|
| 1. ár | (11.000 - 1.000) \* 30% = 3.000           | (11,000 - 1,000) - 3,000 = 7,000      |
| 2. ár | (7.000 - 1.000) \* 30% = 1.800            | (7,000 -1,800) = 5,200                |
| 3. ár | (5.200 - 1.000) \* 30% = 1.260            | (5,200 - 1,260) = 3,940               |










[!INCLUDE[footer-include](../../includes/footer-banner.md)]
