---
title: Minnkunarregla eftirágreidds afsláttar
description: Í þessu efnisatriði er lýst hvernig á að setja upp minnkunarreglur. Minnkunarreglur stjórna hegðuninni þegar margir eftirágreiddir afslættir gilda um sömu vöruna eða færsluna.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateCategory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: e6b178704fde18036d526e7a645cb9b4f8bd66c7
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579065"
---
# <a name="rebate-reduction-principles"></a>Minnkunarregla eftirágreidds afsláttar

[!include [banner](../includes/banner.md)]

Hægt er að flokka tilboð fyrir stjórnun eftirágreidds afsláttar í *minnkunarreglur* til að draga úr öðrum úthlutunum sem tengjast vöru og/eða draga úr gildunum sem koma út úr útreikningum eftirágreidds afsláttar. Þegar búið er að setja upp minnkunarreglur er hægt að úthluta þeim valfrjálst eftir þörfum á línurnar í tilboðum fyrir stjórnun eftirágreidds afsláttar.

Minnkunarreglur eftirágreidds afsláttar eiga aðeins við þegar tilboð eftirágreidds afsláttar skarast. Þar af leiðandi gætu þeir veitt marga eftirágreidda afslætti í kringumstæðum þar sem margir eftirágreiddir afslættir eru ekki skuld.

## <a name="manage-rebate-reduction-principles"></a>Stjórna minnkunarreglu eftirágreidds afsláttar

Til að vinna með minnkunarreglur eftirágreidds afsláttar skal fara í **Stjórnun eftirágreidds afsláttar \> Uppsetning \> Minnkunarregla eftirágreidds afsláttar**. Notið því næst hnappana á aðgerðasvæðinu til að bæta við og fjarlægja minnkunarreglur eftir þörfum. Fyrir hverja reglu skal stilla reitina eins og því er lýst í eftirfarandi töflu.

| Svæði | lýsing |
|---|---|
| Minnkunarregla eftirágreidds afsláttar | Sláið inn einkvæmt heiti fyrir minnkunarreglu eftirágreidds afsláttar. |
| lýsing | Færið inn lýsingu á minnkunarreglu eftirágreidds afsláttar. |
| Nota lækkun | Veljið þennan gátreit til að nota lækkunargrunn á eftirágreidda afslætti sem tilheyra þessari minnkunarreglu eftirágreidds afsláttar. |
| Lækkunargrunnur | Ef gátreiturinn **Nota lækkun** er valinn, þá skal velja lækkunargrunninn (*Úthlutun*, *Eftirágreiddir afslættir* eða *Bæði*). Ef *Bæði* er valið og bæði úthlutun og eftirágreiddur afsláttur hafa verið bókuð fyrir eldra tilboð, verður aðeins eftirágreiddur afsláttur notaður. |
| Útiloka frá lækkun | Ef þessi gátreitur er valinn verða úthlutanir og eftirágreiddir afslættir sem tilheyra þessari minnkunarreglu eftirágreidds afsláttar ekki hafið með í næstu lækkunum. Stillingin á reitnum **Lækkunargrunnur** á ekki við um þessa stillingu. |

## <a name="examples-of-rebate-reduction-principle-setups"></a>Dæmi um uppsetningar minnkunarreglu eftirágreidds afsláttar

Eftirfarandi tafla sýnir nokkur dæmigerð dæmi um uppsetningar á minnkunarreglu eftirágreidds afsláttar. Fyrir hverja minnkunarreglu eftirágreidds afsláttar útskýrir gildið í reitnum **Lýsing** tilgangi minnkunarreglu eftirágreidds afsláttar.

| Minnkunarregla eftirágreidds afsláttar | lýsing | Nota lækkun | Lækkunargrunnur | Útiloka frá lækkun |
|---|---|---|---|---|
| Frestað | Lækka eftirágreiddan afslátt | Já | Hvort tveggja | Nei |
| Exclreb | Sleppa eftirágreiddum afslætti | Já | Eftirágreiddur afsláttur | Já |
| Margfeldi | Margir eftirágreiddir afslættir | Já | Hvort tveggja | Já |
| Engum | Úthlutun og eftirágreiddur afsláttur eingöngu | Nei | Hvort tveggja | Já |
| Úthlutun | Eingöngu úthlutun | Já | Úthlutun | Nei |
| Eftirágreiddur afsláttur | Aðeins eftirágreiddur afsláttur | Já | Eftirágreiddur afsláttur | Já |

## <a name="examples-of-rebate-reduction-principle-calculations"></a>Dæmi um útreikning á minnkunarreglu eftirágreidds afsláttar

Sölupöntun er til staðar með einni sölupöntunarlínu. Þessi lína er með gildið $1.000. Eftirfarandi tilboð gilda um pöntunina:

- **Tilboð 1:** 10 prósent á $1.000
- **Tilboð 2:** 15 prósent á $1.000
- **Tilboð 3:** 20 prósent á $1.000
- **Tilboð 4:** 25 prósent á $1.000

Röð úrvinnslunnar er mjög mikilvæg. Röð úrvinnslunnar byggir á því hvernig er unnið eins og lýst er í [Vinna úr, yfirfara og bóka eftirágreidda afslætti](process-review-post.md).

Til dæmis dregur eftirfarandi tafla saman niðurstöðuna ef notað er *1, 2, 3, 4* og ef aðeins er unnið úr úthlutunum.

| Tilboð | Áskriftir og stillingar | Niðurstaða úthlutunar |
|---|---|---|
| 1 | <p>Flokkunin athugar ekki lækkanir í öðrum tilboðum. Gerð er athugun á bæði úthlutunum og eftirágreiddum afsláttum.</p><ul><li>**Draga frá:** *Nei*</li><li>**Lækkunardráttargrunnur:** *Bæði*</li><li>**Útiloka frá lækkun:** *Nei*</li></ul> | $1.000 × 10% = $100 |
| 2 | <p>Flokkunin athugar lækkanir í öðrum tilboðum en er flögguð þannig að hún er sjálf hunsuð. Athugun fer aðeins fram fyrir eftirágreiddan afslátt.</p><ul><li>**Draga frá:** *Já*</li><li>**Lækkunardráttargrunnur:** *Bæði*</li><li>**Útiloka frá lækkun:** *Já*</li></ul> | $1.000 × 15% = $150 |
| 3 | <p>Flokkunin athugar lækkanir í öðrum tilboðum. Gerð er athugun á bæði úthlutunum og eftirágreiddum afsláttum.</p><ul><li>**Draga frá:** *Já*</li><li>**Lækkunardráttargrunnur:** *Bæði*</li><li>**Útiloka frá lækkun:** *Nei*</li></ul> | ($1.000 – tilboð 1) × 20% = $180 |
| 4 | <p>Flokkunin athugar lækkanir í öðrum tilboðum. Gerð er athugun á bæði úthlutunum og eftirágreiddum afsláttum.</p><ul><li>**Draga frá:** *Já*</li><li>**Lækkunardráttargrunnur:** *Bæði*</li><li>**Útiloka frá lækkun:** *Nei*</li></ul> | ($1.000 – Tilboð 1 – Tilboð 3) × 25% = $180 |

Eftirfarandi tafla sýnir nokkur dæmi þar sem unnið er úr úthlutun í ólíkum röðum og þar sem mismunandi samtölur koma út fyrir vikið. Frávikið í úthlutunum fer eftir röðinni sem kerfið vinnur úr tilboðum. Mikilvægt er að átta sig á því hvernig röð úrvinnslu hefur áhrif á lokaupphæð eftirágreidds afsláttar.

| Röð | Útreikningur |
|---|---|
| 1<br>(1, 2, 3, 4) | <ul><li>**Tilboð 1:** $1.000 × 10% = $100</li><li>**Tilboð 2:** $1.000 × 15% = $150</li><li>**Tilboð 3:** ($1.000 – tilboð 1) × 20% = $180</li><li>**Tilboð 4:** ($1.000 – Tilboð 1 – Tilboð 2) × 25% = $180</li><li>**Heildarúthlutun:** $610</li></ul> |
| 2<br>(4, 3, 2, 1) | <ul><li>**Tilboð 4:** $1.000 x 25% = $250</li><li>**Tilboð 3:** ($1.000 – tilboð 4) × 20% = $150</li><li>**Tilboð 2:** $1.000 x 15% = $150</li><li>**Tilboð 1:** $1.000 x 10% = $100</li><li>**Heildarúthlutun:** $650</li></ul> |
| 3<br>(3, 2, 1, 4) | <ul><li>**Tilboð 3:** $1.000 x 20% = $200</li><li>**Tilboð 2:** $1.000 x 15% = $150</li><li>**Tilboð 1:** $1.000 x 10% = $100</li><li>**Tilboð 4:** ($1.000 – Tilboð 3 – Tilboð 1) × 25% = $175</li><li>**Heildarúthlutun:** $625</li></ul> |
| 4<br>(2, 4, 1, 3) | <ul><li>**Tilboð 2:** $1.000 × 15% = $150</li><li>**Tilboð 4:** $1.000 × 25% = $250</li><li>**Tilboð 1:** $1.000 × 10% = $100</li><li>**Tilboð 3:** ($1.000 – Tilboð 4 – Tilboð 1) × 20% = $130</li><li>**Heildarúthlutun:** $630</li></ul> |
