---
title: Hugtök leyfis og fjarvista
description: Þetta efnisatriði lýsir hugtökum leyfis og fjarvista og hvernig stöður frítíma eru ákvarðaðar.
author: andreabichsel
manager: AnnBe
ms.date: 01/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application user
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: ''
ms.openlocfilehash: 96e3aa74e513a2421b04bac049400cf71042e2c8
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/19/2019
ms.locfileid: "857293"
---
# <a name="leave-and-absence-concepts"></a>Hugtök leyfis og fjarvista

[!include[banner](../includes/banner.md)]

Hugtökum sem er lýst í þessu efnisatriði geta auðveldað þér að ákvarða hvernig starfsmanni er veittur frítími og hvernig tímastöður starfsmannsins eru reiknaðar út. Frekari upplýsingar um stjórnun leyfa og fjarvista er að finna í [Stjórnun leyfis og fjarvista](https://docs.microsoft.com/dynamics365/unified-operations/talent/leave-absence-overview).

## <a name="leave-plan-details"></a>Upplýsingar um leyfisáætlanir

### <a name="start-date"></a>Upphafsdagur

Upphafsdagsetningin er dagurinn þegar uppsöfnunarferli byrjar. Upphafsdagurinn þjónar einnig sem árleg dagsetning sem er notuð til að reikna út yfirfærðar upphæðir.

## <a name="accruals"></a>Uppsafnanir

Uppsafnanir ákvarða hvenær og hversu oft starfsmanni er veittur frítími. Reglur um það hvenær eigi að úthluta uppsöfnunum og reglur um hlutfallsskipti eru skilgreind í hlutanum **Uppsafnanir** við uppsetningu á áætlun leyfis og fjarvista.

### <a name="accrual-frequency"></a>Uppsöfnunartíðni

Uppsöfnunartíðnin skilgreinir hversu oft leyfi er safnað upp eða úthlutað. Eftirtaldir valkostir eru í boði:

- Daglega
- Vikulega
- Aðra hverja viku
- Annan hvern mánuð
- Mánaðarlega
- Ársfjórðungslega
- Annað hvert ár
- Árlega
- Enginn

### <a name="accrual-period-basis"></a>Tímabilsgrunnur uppsöfnunar

Tímabilsgrunnur uppsöfnunar ákvarðar dagsetninguna sem er notuð til að reikna út uppsöfnunartímabil. Eftirtaldir valkostir eru í boði:

- **Upphafsdagsetning áætlunar**
- **Tiltekin dagsetning starfsmanns** - Þegar þessi valkostur er valinn ákvarðar gildið uppruna gildisins fyrir upphaflegu dagsetninguna sem er notuð til að reikna út uppsöfnunartímabil. Eftirtaldir valkostir eru í boði:

    - Sérsniðinn
    - Árleg dagsetning
    - Upprunaleg ráðningardagsetning
    - Starfsaldursdagsetning
    - Breyttur fyrsti starfsdagur starfskrafts
    - Fyrsti starfsdagur starfskrafts

### <a name="accrual-award-date"></a>Úthlutunardagsetning uppsöfunar

Úthlutunardagsetning uppsöfnunar ákvarðar hvenær starfsmanni er úthlutaður frítími. Eftirtaldir valkostir eru í boði:

- **Lokadagsetning uppsöfnunartímabils** - Starfsmanni verður úthlutaður frítími á síðasta degi úthlutunartímabilsins.

    Til að safna upp réttri upphæð verður uppsöfnunarferlið að fela í sér allt tímabilið. Til dæmis er uppsöfnunartímabilið frá 1. janúar til og með 31. janúar 2018. Í þessu tilfelli, svo janúar verði tekin með, verður uppsöfnunin að keyra fyrir 1. febrúar 2018.

- **Upphafsdagur uppsöfnunartímabils** - Starfsmanni verður úthlutaður frítími á fyrsta degi úthlutunartímabilsins.

### <a name="accrual-policy-on-enrollment"></a>Uppsöfnunarregla við skráningu

Þessi uppsöfnunarregla fyrir skráningu skilgreinir hvernig uppsöfnun er reiknuð út þegar starfsmaður er skráður á miðju uppsöfnunartímabili. Eftirtaldir valkostir eru í boði:

- **Hlutfallslega skipt** - Dagsetningabilið milli skráningardags og upphafsdags er notað til að ákvarða dagamuninn. Þessi mismunur er notaður þegar unnið er úr uppsöfnunum.
- **Full uppsöfnun** - Upphæð fullrar uppsöfnunar, sem byggist á laginu, er úthlutað við fyrstu úrvinnslu uppsöfnunar.
- **Engin uppsöfnun** - Engri uppsöfnun er úthlutað fyrr en við næsta uppsöfnunartímabil.

### <a name="accrual-policy-on-unenrollment"></a>Uppsöfnunarregla við afskráningu

Þessi uppsöfnunarregla fyrir afskráningu skilgreinir hvernig uppsöfnun er reiknuð út þegar starfsmaður er afskráður á miðju uppsöfnunartímabili. Eftirtaldir valkostir eru í boði:

- **Hlutfallslega skipt** - Dagsetningabilið milli skráningardags og upphafsdags er notað til að ákvarða dagamuninn. Þessi mismunur er notaður þegar unnið er úr uppsöfnunum.
- **Full uppsöfnun** - Upphæð fullrar uppsöfnunar, sem byggist á laginu, er úthlutað við fyrstu úrvinnslu uppsöfnunar.
- **Engin uppsöfnun** - Engri uppsöfnun er úthlutað fyrr en við næsta uppsöfnunartímabil.

## <a name="accrual-schedule"></a>Uppsöfnunaráætlun

Uppsöfnunaráætlun ákvarðar hvernig starfsmaður safnar upp frítíma og hvaða upphæðum þessi starfsmaður safnar upp og yfirfærir. Hægt er að búa til lög þannig að frítíma sé úthlutað á grunni mismunandi stiga.

### <a name="months-of-service"></a>Starfsaldur í mánuðum

Gildið fyrir **Starfsaldur í mánuðum** skilgreinir lágmarksfjölda mánaða sem starfsmaður verður að vinna til að eiga rétt á uppsöfnunum. Ef ekki er þörf á lágmarki fyrir starfsmenn skal stilla gildið á **0**.

### <a name="hours-worked"></a>Unnar vinnustundir

Gildið fyrir **Unnar vinnustundir** skilgreinir lágmarksfjölda vinnustunda sem starfsmaður verður að vinna á hverju uppsöfnunartímabili til að eiga rétt á uppsöfnunum. Ef ekki er þörf á lágmarki fyrir starfsmenn skal stilla gildið á **0**.

### <a name="accrual-amount"></a>Uppsöfnunarupphæð

Uppsöfnunarupphæðin er fjöldi vinnustunda eða daga sem starfsmenn safna upp á hverju tímabili. Tímabilið byggir á uppsöfnunartíðni.

### <a name="minimum-balance"></a>Lágmarksstaða

Hægt er að nota neikvætt gildi fyrir lágmarksstöðu ef starfsmenn geta óskað eftir lengra leyfi en það sem þeir eru með.

### <a name="maximum-carry-forward"></a>Hámark yfirfærslu

Uppsöfnunarferlið mun jafna stöðu leyfa sem fara yfir stöðu hámarksyfirfærslu á árlegri upphafsdagsetningu.

### <a name="grant-amount"></a>Styrksupphæð

Styrksupphæðin er upprunalegur fjöldi vinnustunda eða daga sem starfsmenn fá þegar þeir skrá sig í fyrsta sinn í leyfisáætlunina. Upphæðin safnast ekki upp fyrir hvert uppsöfnunartímabil.

## <a name="enrollments-and-balances"></a>Skráningar og stöður

### <a name="enrollment-date"></a>Skráningardagur

Skráningardagurinn ákvarðar hvenær starfsmaður getur byrjað að safna frítíma. Til dæmis, ef starfsmaður er skráður í frí 15. júní 2018 getur hún safnað upp frítíma fyrir 15. júní 2018.

### <a name="current-balance"></a>Gildandi staða

Núgildandi staða er upphæð leyfis sem er í boði fyrir frítímabeiðnir. Þessi upphæð inniheldur uppsafnanir, samþykktar beiðnir og breytingar á núgildandi degi.

### <a name="current-balance-examples"></a>Dæmi um núverandi stöðu

#### <a name="annual-plan"></a>Árleg áætlun

**Uppsetning áætlunar**

| Upphafsdagsetning áætlunar | Skráningardagur | Uppsöfnunartíðni | Tímabilsgrunnur uppsöfnunar | Úthlutunardagsetning uppsöfunar    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Árlegur            | Upphafsdagsetning áætlunar      | Lok uppsöfnunartímabils |

Unnið er úr uppsöfnunum 1. janúar 2019 (1/1/2019) þannig að þetta heildartímabil er tekið með.

**Niðurstöður**

| Uppsöfnunarupphæð | Lágmarksstaða | Hámark yfirfærslu | Upphæð beiðni | Núgildandi staða (frá og með 1/1/2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 200            | 0               | 120                   | 40             | 160                              |

Núgildandi staða (160) = Uppsöfnunarupphæð (200) - Upphæð beiðni (40)

#### <a name="semimonthly-plan"></a>Áætlun annan hvern mánuð

**Uppsetning áætlunar**

| Upphafsdagsetning áætlunar | Skráningardagur | Uppsöfnunartíðni | Tímabilsgrunnur uppsöfnunar | Úthlutunardagsetning uppsöfunar    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Annan hvern mánuð       | Upphafsdagsetning áætlunar      | Lok uppsöfnunartímabils |

Unnið er úr uppsöfnunum 1. maí 2018 (1/5/2018) þannig að þetta heildartímabil er tekið með.

**Niðurstöður**

| Uppsöfnunarupphæð | Lágmarksstaða | Hámark yfirfærslu | Upphæð beiðni | Núgildandi staða (frá og með 1/1/2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 22                               |

Núgildandi staða (22) = Uppsöfnunarupphæð (5 x 6) - Upphæð beiðni (8)

#### <a name="monthly-plan"></a>Mánaðarleg áætlun

**Uppsetning áætlunar**

| Upphafsdagsetning áætlunar | Skráningardagur | Uppsöfnunartíðni | Tímabilsgrunnur uppsöfnunar | Úthlutunardagsetning uppsöfunar    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Annan hvern mánuð       | Upphafsdagsetning áætlunar      | Lok uppsöfnunartímabils |

Unnið er úr uppsöfnunum 1. maí 2018 (1/5/2018) þannig að þetta heildartímabil er tekið með.

**Niðurstöður**

| Uppsöfnunarupphæð | Lágmarksstaða | Hámark yfirfærslu | Upphæð beiðni | Núgildandi staða (frá og með 1/1/2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Núgildandi staða (7) = Uppsöfnunarupphæð (5 x 3) - Upphæð beiðni (8)

### <a name="forecasted-balance"></a>Spáð staða

*Spáð staða* er upphæð leyfis sem er í boði fyrir ókomna dagsetningu. Spáð er fyrir um breytingar á uppsöfnunum og yfirfærslum upp að þeim degi.

Eftirfarandi formúla er notuð:

Spáð staða mánudags = Núgildandi staða – Beiðnir + Uppsafnanir – breytingar á yfirfærslu

### <a name="forecasted-balance-examples"></a>Dæmi um spáða stöðu

#### <a name="annual-plan"></a>Árleg áætlun

**Uppsetning áætlunar**

| Upphafsdagsetning áætlunar | Skráningardagur | Uppsöfnunartíðni | Tímabilsgrunnur uppsöfnunar | Úthlutunardagsetning uppsöfunar    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Árlegur            | Upphafsdagsetning áætlunar      | Lok uppsöfnunartímabils |

Unnið er úr uppsöfnunum 15. febrúar 2019 (15/2/2019) þannig að þetta heildartímabil er tekið með.

**Niðurstöður**

| Uppsöfnunarupphæð | Lágmarksstaða | Hámark yfirfærslu | Gildandi staða | Spáð staða (frá og með 15/2/2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 20             | 0               | 20                    | 40              | 40                                   |

Spáð staða (40) = Uppsöfnunarupphæð (20) + Núgildandi staða (40) – breytingar á yfirfærslu (20)

#### <a name="semimonthly-plan"></a>Áætlun annan hvern mánuð

**Uppsetning áætlunar**

| Upphafsdagsetning áætlunar | Skráningardagur | Uppsöfnunartíðni | Tímabilsgrunnur uppsöfnunar | Úthlutunardagsetning uppsöfunar    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Annan hvern mánuð       | Upphafsdagsetning áætlunar      | Lok uppsöfnunartímabils |

Unnið er úr uppsöfnunum 15. febrúar 2019 (15/2/2019) þannig að þetta heildartímabil er tekið með.

**Niðurstöður**

| Uppsöfnunarupphæð | Lágmarksstaða | Hámark yfirfærslu | Gildandi staða | Spáð staða (frá og með 15/2/2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 5              | 0               | 20                    | 40              | 35                                   |

Spáð staða (35) = Uppsöfnunarupphæð (5 x 3) + Núgildandi staða (40) – breytingar á yfirfærslu (20)

#### <a name="monthly-plan"></a>Mánaðarleg áætlun

**Uppsetning áætlunar**

| Upphafsdagsetning áætlunar | Skráningardagur | Uppsöfnunartíðni | Tímabilsgrunnur uppsöfnunar | Úthlutunardagsetning uppsöfunar    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 2/1/2018        | Annan hvern mánuð       | Upphafsdagsetning áætlunar      | Lok uppsöfnunartímabils |

Unnið er úr uppsöfnunum 15. febrúar 2019 (15/2/2019) þannig að þetta heildartímabil er tekið með.

**Niðurstöður**

| Uppsöfnunarupphæð | Lágmarksstaða | Hámark yfirfærslu | Gildandi staða | Spáð staða (frá og með 15/2/2019) |
|----------------|-----------------|-----------------------|-----------------|--------------------------------------|
| 10             | 0               | 20                    | 40              | 30                                   |

Spáð staða (30) = Uppsöfnunarupphæð (10 x 1) + Núgildandi staða (40) – breytingar á yfirfærslu (20)

### <a name="proration-balance-examples"></a>Dæmi um hlutfallsskipti stöðu

#### <a name="prorated-monthly-plan"></a>Skipt mánaðarleg áætlun

**Uppsetning áætlunar**

| Upphafsdagsetning áætlunar | Uppsöfnunartíðni | Tímabilsgrunnur uppsöfnunar |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Mánaðarlega           | Upphafsdagsetning áætlunar      |

**Niðurstöður**

| Starfsmaður            | Starfsaldur í mánuðum | Skráningardagur | Upphafsdagur | Uppsöfnunarupphæð | Vinna úr uppsöfnun | Efnahagur |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2,53    |

#### <a name="full-accrual-monthly-plan"></a>Full uppsöfnun mánaðarlegrar áætlunar

**Uppsetning áætlunar**

| Upphafsdagsetning áætlunar | Uppsöfnunartíðni | Tímabilsgrunnur uppsöfnunar |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Mánaðarlega           | Upphafsdagsetning áætlunar      |

**Niðurstöður**

| Starfsmaður            | Starfsaldur í mánuðum | Skráningardagur | Upphafsdagur | Uppsöfnunarupphæð | Vinna úr uppsöfnun | Efnahagur |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 3,00    |

#### <a name="no-accrual-monthly-plan"></a>Engin uppsöfnun mánaðarlegrar áætlunar

**Uppsetning áætlunar**

| Upphafsdagsetning áætlunar | Uppsöfnunartíðni | Tímabilsgrunnur uppsöfnunar |
|-----------------|-------------------|----------------------|
| 1/1/2018        | Mánaðarlega           | Upphafsdagsetning áætlunar      |

**Niðurstöður**

| Starfsmaður            | Starfsaldur í mánuðum | Skráningardagur | Upphafsdagur | Uppsöfnunarupphæð | Vinna úr uppsöfnun | Efnahagur |
|---------------------|-------------------|-----------------|------------|----------------|-----------------|---------|
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3,00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1,00           | 9/1/2018        | 2.00    |
