---
title: Búa til leyfis- og fjarvistaáætlun
description: Þetta efni lýsir því hvernig á að búa til orlofsáætlanir í Dynamics 365 Human Resources fyrir mismunandi tegundir orlofs.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 253ca72b14c2460f8f0aaad687992b873eb11518
ms.sourcegitcommit: e91a1797192fd9bc4048b445bb5c1ad5d333d87d
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/01/2021
ms.locfileid: "7728980"
---
# <a name="create-a-leave-and-absence-plan"></a>Búa til leyfis- og fjarvistaáætlun

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Skilgreindu orlofs- og fjarveruáætlanir í Dynamics 365 Human Resources fyrir hverja tegund orlofs sem þú býður. Orlofs- og fjarveruáætlanir geta safnast á mismunandi tíðni, svo sem árlega, mánaðarlega eða hálfsmánaðarlega. Einnig er hægt að skilgreina áætlun sem styrk, þar sem stök uppsöfnun á sér stað við ákveðna dagsetningu. Til dæmis gætirðu búið til áætlun sem veitir fljótandi frí árlega.

Skipulögð orlofsáætlun gerir starfsmönnum kleift að fá bætur miðað við þann tíma sem þeir hafa eytt með stofnun. Skipulagðar áætlanir gera kleift að gera sjálfvirka skráningu í viðbótar bótatíma.

Þú getur tilgreint hámarks yfirfærslufjárhæðir eða lágmarksjafnvægi til að tryggja að starfsmenn noti aðeins bótatímana sem þeir hafa safnað.

Til dæmis, með skipulagðri áætlun, geturðu veitt nýjum starfsmönnum 80 tíma greiddan fríafslátt (PTO). Þá geturðu veitt 120 klukkustundir af 60 mánaða þjónustu.

Þú getur einnig búið til stöðutengda orlofskostnað, svo sem starfstíma eingöngu framkvæmdastjóra.

## <a name="create-a-leave-plan"></a>Stofna oflofsáætlun

1. Á síðunni **Áætlanir leyfis og fjarvista** skal velja **Stofna nýja áætlun**.

2. Undir **Upplýsingar**, sláðu inn **Nafn**, **Upphafsdagur**, **Lýsing**, og **Skildu eftir tegund** fyrir áætlun þína.

Ef aðgerðin **Stilla margar leyfisgerðir fyrir eina orlofs- og fjarveruáætlun** er virkjuð eru leyfisgerðir stilltar í **Uppsöfnunaráætlun** í stað undir **Upplýsingar**. Fyrir hverja færslu í uppsöfnunartöflu töflunni er hægt að skilgreina leyfisgerð. Þegar þessi eiginleiki er virkur þarf einnig að nota nýja gagnaeiningar fyrir samþættingu eða aðrar aðstæður þar sem nota þarf einingar. 

Nýju einingarnar eru:

- Bankafærsla yfir leyfi og fjarvistir V2
- Skráning leyfis og fjarvista V2
- Áætlunarskil leyfis og fjarvista V2
- Áætlun leyfis og fjarvista V2
- Beiðni um frí V2

 > [!IMPORTANT]
   > Eftir að þessi eiginleiki hefur verið virkjaður er ekki hægt að slökkva á honum.

3. Skilgreina uppsafnanir í **Uppsagnir** flipann. Uppsöfnun ákvarðar hvenær og hversu oft starfsmanni er veittur frí. Í þessu skrefi skilgreinir þú stefnu um það hvenær verðlaunin eiga að fá úthlutun og stefnu um hagnað orlofsuppbótar.

   1. Veldu gildi úr **Uppsöfnunartíðni** fellilisti:

      - Daglega
      - Vikulega
      - Aðra hverja viku
      - Annan hvern mánuð
      - Mánaðarlega
      - Ársfjórðungslega
      - Annað hvert ár
      - Árlega
      - Enginn

   2. Veldu valkost úr **Uppsöfnunartími** fellivalmynd til að ákvarða upphafsdagsetningu sem notaður er við útreikning á rekstrartímabilum:

      | Tímabilsgrunnur uppsöfnunar | Lýsing |
      | --- | --- |
      | **Upphafsdagsetning áætlunar** | Upphafsdagur uppsöfnunarstímabilsins er dagsetningin sem áætlunin liggur fyrir. |
      | **Starfsmannasértæk dagsetning** | Upphafsdagur uppsöfnunartímabils fer eftir atburði starfsmanns:</br><ul><li>Sérsniðin (þú verður að tilgreina uppsöfnunargrundvöll fyrir hverja einstaka skráningu)</li><li>Dagsetning starfsafmælis</li><li>Upprunaleg ráðningardagsetning</li><li>Starfsaldursdagsetning</li><li>Breyttur fyrsti starfsdagur starfskrafts</li><li>Fyrsti starfsdagur starfskrafts</li></ul> |

   3. Veldu valkost úr **Uppsöfnun verðlaunadags** fellilisti:

      - **Lokadagsetning uppsöfnunartímabils** - Starfsmanni er úthlutaður frítími á síðasta degi úthlutunartímabilsins. Til að safna upp réttri upphæð verður uppsöfnunarferlið að fela í sér allt tímabilið. Til dæmis, ef uppsöfnunartímabilið er 1. janúar 2020 til og með 31. janúar 2020, verður þú að keyra uppsöfnunina fyrir 1. febrúar 2020 til að taka með janúar.

      - **Upphafsdagur uppsöfnunartímabils** - Starfsmanni er úthlutaður frítími á fyrsta degi úthlutunartímabilsins.

   4. Veldu valkost úr **Uppsöfnunarstefna við skráningu** fellilisti. Þetta gildi skilgreinir hvernig reikna skuli uppsöfnun þegar starfsmaður skráir sig á miðju rekstrartímabili.

      - **Hlutfallslega skipt** - Dagsetningabilið milli skráningardags og upphafsdags er notað til að ákvarða dagamuninn. Þessi mismunur er notaður þegar unnið er úr uppsöfnunum.

      - **Full uppsöfnun** - Upphæð fullrar uppsöfnunar, sem byggist á laginu, er úthlutað við fyrstu úrvinnslu uppsöfnunar.

      - **Engin uppsöfnun** - Engri uppsöfnun er úthlutað fyrr en við næsta uppsöfnunartímabil.

   5. Veldu valkost úr **Uppsöfnunarstefna við afskráningu** fellilisti. Þetta gildi skilgreinir hvernig reikna skuli uppsöfnun þegar starfsmaður afskráir sig á miðju rekstrartímabili.

      - **Hlutfallslega skipt** - Dagsetningabilið milli skráningardags og upphafsdags er notað til að ákvarða dagamuninn. Þessi mismunur er notaður þegar unnið er úr uppsöfnunum.

      - **Full uppsöfnun** - Upphæð fullrar uppsöfnunar, sem byggist á laginu, er úthlutað við fyrstu úrvinnslu uppsöfnunar.

      - **Engin uppsöfnun** - Engri uppsöfnun er úthlutað fyrr en við næsta uppsöfnunartímabil.

4. Skilgreindu uppsöfnunaráætlunina í **Uppsöfnunaráætlun** flipann. Uppsöfnunaráætlun ákvarðar:

   - Hvernig starfsmaður safnar frí
   - Hvaða upphæðir starfsmaður mun safna
   - Hvaða upphæð verða yfirfærðar

   Hægt er að stofna lög til að veita frítíma á grunni mismunandi stiga.

   Ef þú ert með starfsmenn í tímavinnu er hægt að veita frí sem byggist á vinnustundum í stað ráðningartíma hjá fyrirtækinu. Upplýsingar um vinnustundir eru venjulega geymdar tíma- og viðverukerfi. Þú getur flutt inn venjulega og yfirvinnutíma sem unnið er úr tíma- og mætingarkerfinu og notað þær sem grunn fyrir verðlaun starfsmanns.
   
    1. Veldu valkost úr **Uppsöfnunargerð** fellilisti:

      - **Mánaðarlega þjónusta** - Byggðu uppsöfnunaráætlunina á mánaða þjónustu.

      - **Vinnutímar** - Byggðu uppsöfnunaráætlunina á vinnustundum. Nánari upplýsingar um áfallningu í vinnustundir, sjá [Rennur upp frestur byggður á vinnustundum](hr-leave-and-absence-plans.md?accrue-time-off-based-on-hours-worked).

      Nánari upplýsingar um uppsöfnunarstöður, sjá [Uppsöfnunarfrí byggt á vinnustundum](hr-leave-and-absence-plans.md?enrollments-and-balances).

    2. Sláðu inn gildi í uppsöfnunaráætlunartöflu:

      - **Starfsaldur í mánuðum** - Lágmarksfjölda mánaða sem starfsmaður verður að vinna til að eiga rétt á uppsöfnunum. Ef þú þarft ekki lágmark skaltu stilla gildið á 0.

      - **Unnar vinnustundir** - Lágmarksfjölda vinnustunda sem starfsmaður verður að vinna á hverju uppsöfnunartímabili til að eiga rétt á uppsöfnunum. Ef þú þarft ekki lágmark skaltu stilla gildið á 0.

      - **Uppsöfnunarupphæð** - Fjöldi vinnustunda eða daga sem starfsmenn safna upp á hverju tímabili. Tímabilið byggir á uppsöfnunartíðni.

      - **Lágmarksstaða** - Hægt er að nota neikvætt gildi fyrir lágmarksstöðu ef starfsmenn geta óskað eftir lengra leyfi en það sem þeir eru með.

      - **Hámarksyfirfærsla** - Uppsöfnunarferlið mun jafna stöðu leyfa sem fara yfir stöðu hámarksyfirfærslu á árlegri upphafsdagsetningu.

      - **Styrksupphæð** - Upprunalegur fjöldi vinnustunda eða daga sem starfsmenn fá þegar þeir skrá sig í fyrsta sinn í leyfisáætlunina. Upphæðin safnast ekki upp fyrir hvert uppsöfnunartímabil.
      
Ef aðgerðin **Stilla margar leyfisgerðir fyrir eina orlofs- og fjarveruáætlun** er virkjuð velurðu valkost úr **Leyfisgerð**. 

   > [!IMPORTANT]
   > Eftir að þessi eiginleiki hefur verið virkjaður er ekki hægt að slökkva á honum.

Ef eiginleikinn **Nota fullt stöðugildi** er virkur notar Human Resources fullt stöðugildi (FTE) sem er skilgreint fyrir stöðuna til að hlutfallsskipta uppsöfnun starfsmanns. Til dæmis, ef FTE er .5 og uppsöfnunarfjárhæðin er 10, þá mun starfsmaðurinn safna 5. Þú getur aðeins notað þennan möguleika ef þú gerir kleift að nota margar leyfisgerðir.  

5. Veljið **Vista**.

## <a name="accrue-time-off-based-on-hours-worked"></a>Uppsöfnun frís sem byggist á vinnustundum

Ef þú ert með starfsmenn í tímavinnu er hægt að veita frí sem byggist á vinnustundum í stað ráðningartíma hjá fyrirtækinu. Gögn um vinnustundagögn eru venjulega geymdar tíma- og viðverukerfi. Þú getur flutt inn venjulega og yfirvinnutíma sem unnið er úr tíma- og mætingarkerfinu og notað þær sem grunn fyrir verðlaun starfsmanns.

Þegar þú velur vinnustundir sem uppsöfnunargerð geturðu nota eru tvær gerðir af tímum fyrir uppsöfnunina: reglulegar og yfirvinna. Uppsöfnunarferli fyrir vinnustundaáætlanir notar tíðni uppsöfnunar, ásamt tímabilsgrunn uppsöfnunar, til að ákvarða vinnustundirnar sem safna á upp.

### <a name="annual-accrual-frequency"></a>Árleg tíðni uppsöfnunar

| Dagsetning uppsafnaðrar umbunar    | Vinnustundalag    | Uppsöfnunarupphæð        | Unnar klukkustundir, dagsetningar   | Unnar klukkustundir, raun| Umbun               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 12/31/2018            | 2080                 | 144                   | 1/1/2018-31/12/2018  | 2085                | 144                 |        
| 12/31/2018            | 2080                 | 144                   | 1/1/2018-31/12/2018  | 2000                | 0                 |


### <a name="monthly-accrual-frequency"></a>Mánaðarleg tíðni uppsöfnunar

| Dagsetning uppsafnaðrar umbunar    | Vinnustundalag    | Uppsöfnunarupphæð        | Unnar klukkustundir, dagsetningar   | Unnar klukkustundir, raun| Umbun               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 160                  | 12                    | 1/8/2018-31/8/2018   | 184                 | 12                  |        
| 8/31/2018             | 160                  | 3                     | 1/8/2018-31/8/2018   | 184                 | 3                   |

### <a name="semi-monthly-accrual-frequency"></a>Hálfsmánaðarleg tíðni uppsöfnunar

| Dagsetning uppsafnaðrar umbunar    | Vinnustundalag    | Uppsöfnunarupphæð        | Unnar klukkustundir, dagsetningar   | Unnar klukkustundir, raun| Umbun               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 80                   | 6                     | 16/8/2018-31/8/2018  | 81                  | 6                  |        
| 8/31/2018             | 80                   | 6                     | 16/8/2018-31/8/2018  | 75                  | 0                   |

### <a name="weekly-accrual-frequency"></a>Vikuleg tíðni uppsöfnunar

| Dagsetning uppsafnaðrar umbunar    | Vinnustundalag    | Uppsöfnunarupphæð        | Unnar klukkustundir, dagsetningar   | Unnar klukkustundir, raun| Umbun               |
| --------------------- | -------------------- | --------------------- | -------------------- |-------------------- |-------------------- |
| 8/31/2018             | 40                   | 3                     | 27/8/2018-31/8/2018  | 42                  | 3                  |        
| 8/31/2018             | 40                   | 3                     | 27/8/2018-31/8/2018  | 35                  | 0                   |

### <a name="employee-assigned-leave-plans"></a>Úthlutaðar leyfisáætlanir starfsmanns

Í úthlutuðum leyfisáætlunum starfsmanns er grunnlag og gerð vinnustunda birt fyrir vinnustundaáætlanir. Raunverulegar vinnustundir fyrir uppsöfnunartímabilin frá og með núverandi dagsetningu birast einnig fyrir virkar áætlanir.

### <a name="loading-data"></a>Innlestur gagna

Hægt er að flytja inn raunverulegar vinnustundir með einingunni **unnar leyfis- og fjarvistarstundir** í gagnastjórnun. Ef þú ert að nota vinnutímadagatal sannprófar innflutningur að reglulegar vinnustundir fari ekki yfir áætlaðar vinnustundir á dag sem er skilgreint af dagatalinu. Innflutningurinn sannprófar einnig að vinnustundir fyrir tiltekinn dag fari ekki yfir 24. 

Þú þarft eftirfarandi upplýsingar til að flytja inn raunverulegar vinnustundir til að nota í uppsöfnunarferli á leyfi:

- Númer starfsmanns 
- Dagsetning sem var unnið
- Gerð
- Tímar

Ein dagsetning getur aðeins haft eina af hverri gerð sem tengist henni.

| Númer starfsmanns       | Dagsetning sem var unnið           | Gerð                  | Vinnustundir                |
| --------------------- | -------------------- | --------------------- | -------------------- |
| 000337                | 8/6/2018             | Regluleg               | 8                    |       
| 000337                | 8/7/2018             | Regluleg               | 8                    |
| 000337                | 8/7/2018             | Yfirvinna              | 3                    |
| 000337                | 8/8/2018             | Regluleg               | 8                    |
| 000337                | 8/7/2018             | Regluleg               | 8                    |
| 000337                | 8/9/2018             | Regluleg               | 8                    |

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

Unnið er úr uppsöfnunum 1. maí 2018 (5/1/2018) þannig að þetta heildartímabil er tekið með.

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

Unnið er úr uppsöfnunum 1. maí 2018 (5/1/2018) þannig að þetta heildartímabil er tekið með.

**Niðurstöður**

| Uppsöfnunarupphæð | Lágmarksstaða | Hámark yfirfærslu | Upphæð beiðni | Núgildandi staða (frá og með 1/1/2019) |
|----------------|-----------------|-----------------------|----------------|----------------------------------|
| 5              | 0               | 120                   | 8              | 7                                |

Núgildandi staða (7) = Uppsöfnunarupphæð (5 x 3) - Upphæð beiðni (8)

### <a name="forecasted-balance"></a>Spástaða

*Spáð staða* er upphæð leyfis sem er í boði fyrir ókomna dagsetningu. Spáð er fyrir um breytingar á uppsöfnunum og yfirfærslum upp að þeim degi.

Human Resources notar eftirfarandi formúlu:

Spáð staða mánudags = Núgildandi staða – Beiðnir + Uppsafnanir – breytingar á yfirfærslu

### <a name="forecasted-balance-examples"></a>Dæmi um spáða stöðu

#### <a name="annual-plan"></a>Árleg áætlun

**Uppsetning áætlunar**

| Upphafsdagsetning áætlunar | Skráningardagur | Uppsöfnunartíðni | Tímabilsgrunnur uppsöfnunar | Úthlutunardagsetning uppsöfunar    |
|-----------------|-----------------|-------------------|----------------------|-----------------------|
| 1/1/2018        | 1/1/2018        | Árlegur            | Upphafsdagsetning áætlunar      | Lok uppsöfnunartímabils |

Unnið er úr uppsöfnunum 15. febrúar 2019 (2/15/2019) þannig að þetta heildartímabil er tekið með.

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

Unnið er úr uppsöfnunum 15. febrúar 2019 (2/15/2019) þannig að þetta heildartímabil er tekið með.

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

Unnið er úr uppsöfnunum 15. febrúar 2019 (2/15/2019) þannig að þetta heildartímabil er tekið með.

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
| Jeannette Nicholson | 0,00              | 6/1/2018        | 6/1/2018   | 1,00           | 9/1/2018        | 3.00    |
| Jay Norman          | 0,00              | 6/15/2018       | 6/15/2018  | 1.00           | 9/1/2018        | 2.00    |

## <a name="see-also"></a>Sjá einnig

- [Yfirlit yfir leyfi og fjarvistir](hr-leave-and-absence-overview.md)
- [Grunnstilla gerðir leyfis og fjarvista](hr-leave-and-absence-types.md)
- [Uppsöfnunaráætlanir fyrir leyfi og fjarvistir](hr-leave-and-absence-accrue.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
