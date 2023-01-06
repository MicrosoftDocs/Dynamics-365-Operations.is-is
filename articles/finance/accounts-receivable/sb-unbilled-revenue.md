---
title: Óreikningsfærðar tekjur
description: Í þessari grein er útskýrt hvernig á að setja upp vörur og lykla til að nota eiginleika óreikningsfærðra tekna í áskriftargreiðslum.
author: JodiChristiansen
ms.date: 10/10/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: 539093
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2021-11-05
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: adf6f06ee454f368fa194315a87cfdec9e5e13da
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644169"
---
# <a name="unbilled-revenue"></a>Óreikningsfærðar tekjur

Þessi grein lýsir eiginleika óreikningsfærðra tekna sem gerir þér kleift að hafa með upphæðir fyrir heilar greiðsluáætlanir í efnahagsreikningnum. Þessar upphæðir eru teknar með í lyklum óreikningsfærðra tekna og í mótlykli óreikningsfærðra tekna og samningurinn er reikningsfærður í gegnum afborganir.

## <a name="set-up-unbilled-revenue"></a>Setja upp óreikningsfærðar tekjur

Fylgdu þessum skrefum til að setja upp óreikningsfærðar tekjur.

- Á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur** skal stilla reitina í hlutanum **Óreikningsfærðar tekjur**.
- Hægt er að nota eiginleika óreikningsfærðra tekna fyrir vörur þar sem reiturinn **Vörutegund** er stilltur á **Staðlað**. Einnig er hægt að nota þetta fyrir frestunarvörur. Til að nota óreikningsfærðar tekjur með skammtímavirkninni skal setja upp skammtímavalkosti á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur**.

Til að setja upp vörur til að nota óreikningsfærðar tekjur skal fylgja þessum skrefum.

1. Á síðunni **Uppsetning óreikningsfærðra tekna** í flipanum **Vörur** skal velja **Bæta við**.
2. Í nýju línunni í **Vörukóði** er vörukóðinn valinn.
3. Veldu vöruvenslin í reitnum **Vöruvensl**.
4. Endurtaka skal þessi skref að bæta fleiri línum.
5. Veldu **Vista**.

Til að setja upp vörur og lykla óreikningsfærðra tekna skal fylgja þessum skrefum.

1. Á síðunni **Uppsetning óreikningsfærðra tekna** í flipanum **Lyklar** skal velja **Bæta við**.
2. Í nýju línunni í **Vörukóði** er vörukóðinn valinn.
3. Veldu vöruvenslin í reitnum **Vöruvensl**.
4. Veldu lyklana fyrir óreikningsfærðar tekjur, óreikningsfærðan afslátt og jöfnun óreikningsfærðra tekna. Til að nota skammtímalykla þarf að stilla reitinn **Aðferð fyrir óreikningsfært til skamms tíma** á **Hlaupandi tímabil** eða **Fast ár** á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur**.
5. Endurtaka skal þessi skref að bæta fleiri línum.
6. Veldu **Vista**.

## <a name="use-unbilled-revenue"></a>Nota óreikningsfærðar tekjur

1. Á síðunni **Allar greiðsluáætlanir** skal stofna greiðsluáætlun.
2. Ef ekki er búið að setja upp vöruna til að nota óreikningsfærðar tekjur skal velja gátreitinn **Óreikningsfærðar tekjur** á greiðsluáætlunarlínunni.
3. Stillið valkostinn **Óreikningsfærðar tekjur** á **Já**. Farðu síðan yfir og breyttu óreikningsfærðum tekjum, afslætti og mótlyklum óreikningsfærðra tekna eftir þörfum.
4. Á greiðsluáætluninni, undir **Vinnsla óreikningsfærðra tekna**, skal velja **Stofna færslu í færslubók** til að stofna upprunalega færslu í færslubók fyrir óreikningsfærðar tekjur. Ljúka þarf þessu skrefi áður en greiðsluáætlunin er reikningsfærð.
5. Þegar upprunaleg færsla í færslubók hefur verið stofnuð skal velja **Búa til reikning** til að stofna sölupantanir og bóka reikningana fyrir greiðsluáætlanirnar.
6. Þegar reikningarnir hafa verið bókaðir geturðu farið yfir upplýsingar yfirferðar í flipanum **Endurnýjanir** á síðunni **Allar greiðsluáætlanir**.

### <a name="milestone-billing"></a>Útskrift samkvæmt þáttaskilum

Áfangagreiðsla virkar með óreikningsfærðum tekjum samkvæmt eftirfarandi skilyrðum:

- Ef yfirvara áfanga er óreikningsfærð (gátreiturinn **Óreikningsfærðar tekjur** er valinn) og undirvörur áfanga eru reikningsfærðar (gátreiturinn **Óreikingsfærðar tekjur** er hreinsaður) þarf að tilgreina upphafs- og lokadagsetningar fyrir yfirvöruna. Þessar dagsetningar eru notaðar til að stofna upphaflegu bókarfærsluna.
- Ef yfirvara áfanga er óreikningsfærð (gátreiturinn **Óreikningsfærðar tekjur** er hreinsaður) og undirvörur áfanga eru reikningsfærðar (gátreiturinn **Óreikningsfærðar tekjur** er valinn) þarf að tilgreina lokadagsetningu aðeins fyrir undirvörurnar sem á að búa til upprunalega færslu í færslubók fyrir.

Hægt er að vinna sérstaklega úr hverri undirvöru áfanga. Hægt er að tilgreina lokadagsetningarnar þegar á að stofna upprunalega færslu í færslubók.

> [!NOTE]
> Ef upphafleg færsla í færslubók fyrir yfirvöru eða undirvörur áfangans hefur þegar verið stofnuð eða reikningur hefur verið búinn til má ekki breyta upphafs- eða lokadagsetningum.

### <a name="unbilled-revenue-with-straight-line-deferrals"></a>Óreikningsfærðar tekjur með frestanir á beinni línu

Til að nota óreikningsfærðar tekjur með línulegum frestunaráætlunum skal fylgja þessum skrefum.

1. Á síðunni **Allar greiðsluáætlanir** skal stofna greiðsluáætlun.
2. Bæta vöru við greiðsluáætlunarlínur.
3. Velja **Frestanir** fyrir línuna.
4. Á síðunni **Færslufrestun** skal fylgja þessum skrefum:

    1. Stilltu valkostinn **Frestað** á **Já**.
    2. Breyttu lyklunum eftir þörfum.
    3. Í hlutanum **Áætlun** skal velja **Línulegt** og breyta öðrum gildum eftir þörfum.
    4. Veldu **Í lagi**.

5. Veldu **Óreikningsfærðar tekjur** fyrir línuna og fylgdu síðan þessum skrefum:

    1. Stillið valkostinn **Óreikningsfærðar tekjur** á **Já**.
    2. Veldu lyklana til að nota fyrir tekjur, afslátt og mótbókun tekna.

6. Í greiðsluáætluninni, undir **Vinnsla óreikningsfærðra tekna**, skal velja **Stofna færslu í færslubók**. Annars er hægt að nota síðuna **Fjöldavinnsla óreikningsfærðra tekna** til að stofna færsla í færslubók.
7. Frestunaráætlunin er búin til. Hægt er að fara yfir upplýsingarnar á síðunni **Allar frestunaráætlanir**. Eftir að frestunaráætlunin hefur verið búin til er hægt að breyta ýmsum gildum fyrir vörulínu greiðsluáætlunar. Til dæmis er hægt að breyta einingarverði, magni eða dagsetningum.

### <a name="unbilled-revenue-with-event-based-deferrals"></a>Óreikningsfærðar tekjur með frestanir byggðar á tilvikum

Til að nota óreikningsfærðar tekjur með tilvikstengdum frestunaráætlunum skal fylgja þessum skrefum.

1. Á síðunni **Allar greiðsluáætlanir** skal stofna greiðsluáætlun.
2. Bæta vöru við greiðsluáætlunarlínur.
3. Velja **Frestanir** fyrir línuna.
4. Á síðunni **Færslufrestun** skal fylgja þessum skrefum:

    1. Stilltu valkostinn **Frestað** á **Já**.
    2. Breyttu lyklunum eftir þörfum.
    3. Í hlutanum **Áætlun** skal velja **Tengt tilviki**, **Sniðmát**, **Úthlutunargerð** og **Gildistímalykil**.
    4. Veldu **Í lagi**.

5. Veldu **Óreikningsfærðar tekjur** fyrir línuna og fylgdu síðan þessum skrefum:

    - Stillið valkostinn **Óreikningsfærðar tekjur** á **Já**.
    - Veldu lyklana til að nota fyrir tekjur, afslátt og mótbókun tekna.

6. Í greiðsluáætluninni, undir **Vinnsla óreikningsfærðra tekna**, skal velja **Stofna færslu í færslubók**. Annars er hægt að nota síðuna **Fjöldavinnsla óreikningsfærðra tekna** til að stofna færsla í færslubók.
7. Frestunaráætlunin er búin til. Hægt er að fara yfir upplýsingarnar á síðunni **Allar frestunaráætlanir**. Eftir að frestunaráætlunin hefur verið búin til er hægt að breyta ýmsum gildum fyrir vörulínu greiðsluáætlunar. Til dæmis er hægt að breyta einingarverði, magni eða dagsetningum. Frestunaráætlunin er endurreiknuð út frá nýju gildunum.

Dreifingarnar eru endurreiknaðar út frá úthlutunargerðinni sem er valin (**Prósenta**, **Prósentu lokið** eða **Jafnar upphæðir**). Fyrir úthlutunargerðina **Breytilegar upphæðir** er dreifingin endurreiknuð samkvæmt prósentu sem jafngildir upphaflegu virði fyrir tilvikið. Sem dæmi er upprunalegt einingarverð $100,00 og prósenta upphaflegs virðis er $55,00 (55 prósent). Ef einingarverði er breytt í $200,00 verður breytileg upphæð tilviksins $110,00 (ennþá 55 prósent).

> [!NOTE]
> Ef línur frestunaráætlunar hafa verið skráðar verður ekki hægt að breyta vörulínu greiðsluáætlunar. Til að breyta vörulínunni þarf fyrst að bakfæra skráðar línur. Þá er hægt að uppfæra greiðsluáætlunarlínuna.

### <a name="unbilled-revenue-and-top-billing"></a>Óreikningsfærðar tekjur og mest reikningsfært

Greiðsluáætlun er færð inn til þriggja ára og reikningarnir eru reikningsfærðir árlega á þriggja ára tímabili. Öll upphæð samningsins er skráð á lykil óreikningsfærðra tekna sem árlegir reikningar eru búnir til úr. Mótlykillinn er tekjulykill eða frestaður tekjulykill.

Mest reikningsfært og óreikningsfærðar tekjur vinna ekki saman því að vandamál með afstemmingu geta komið upp í fjárhagnum. Til dæmis er vöruflokkur A settur upp á síðunni **Uppsetning vöruflokks** þannig að reiturinn **Fjöldi efstu lína** er stilltur á **2**. Á síðunni **Greiðsluáætlanir** er þremur vörum bætt við. Allar þrjár vörurnar tillheyra vöruflokki A. Þegar upphafleg færsla í færslubók er stofnuð fyrir eiginleika óreikningsfærðra tekna er upphæð allra þriggja varanna afgreidd á óreikningsfærðan lykil. Þegar reikningur greiðsluáætlunar er búin til eru aðeins upphæðir fyrir tvær efstu vörurnar hafðar með. Reikningsupphæðin stemmir því ekki við upphæðina sem var afgreidd á lykil óreikningsfærðra tekna og vandamál með afstemmingu geta komið upp í fjárhagnum.

Ef nota á óreikningsfærðar tekjur skal skilja síðuna **Uppsetning vöruflokks** eftir auða eða setja upp alla vöruflokka þannig að reiturinn **Fjöldi efstu lína** er stilltur á **0** (núll). Ef nota á mest reikningsfært eru engar aðgerðir óreikningsfærðra tekna í boði.

### <a name="examples"></a>Dæmi

Frá og með útgáfu 10.0.29 er nýrri færibreytu bætt við færibreytur endurtekinnar samningsgreiðslu. Þegar stillt er á „Já“ virkjar færibreytan **Nota óreikningsfærða mótlykla** tvo nýja lykla í **Uppsetning óreikningsfærðra tekna**. Mótlyklar óreikningsfærðra tekna og óreikningsfærðs afsláttar verða í boði og eru best notaðir þegar greiðsluáætlanir eru búnar til í öðrum gjaldmiðli en bókhaldsgjaldmiðli. Að nota mótlyklana tryggir að lyklar óreikningsfærðra tekna og óreikningsfærðs afsláttar séu bakfærðir með sama genginu og í upphaflegum færslum. Upphaflega ferlið **Stofna færslu í færslubók** er það sama með debetfærslu í óreikningsfærðar tekjur og kreditfærslu í tekjur. Ef afsláttur er notaður er upphafleg færslan í færslubók sú sama með debet í afslætti og kredit í óreikningsfærðum afslætti. 

Þetta dæmi sýnir hvernig á að nota óreikningsfærðar tekjur til að skrá alla upphæð samningsins á efnahagsreikning sem óreikningsfærðar tekjur. Hin hliðin á færslunni eru tekjur eða frestaðar tekjur. Þegar viðskiptavinur er reikningsfærður eru óreikningsfærðar tekjur bakfærðar. Tekjuskráning mun gerast annaðhvort við reikningsfærslu eða samkvæmt áætlun frestaðrar skráningar sem var sett upp.

#### <a name="assumptions"></a>Forsendur

- Þann 1. janúar á yfirstandandi ári skrifar viðskiptavinur undir þriggja ára samning að upphæð $390.
- Samningurinn felur í sér tvo hluta: leyfi og viðhaldssamning.
- Söluverð leyfisgjaldsins er $300 og viðskiptavinurinn verður reikningsfærður fyrir $100 1. janúar á hverju samningsári. Leyfisgjaldið að upphæð $300 verður tekið sem tekjur þegar samningurinn er undirritaður.
- Söluverð viðhaldsgjaldsins er $90 og viðskiptavinurinn fær reikningsfærslu upp á $30 þann 1. janúar á hverju samningsári. $90 viðhaldsgjaldinu verður frestað og $2,50 verður skráð í hverjum mánuði á samningstímanum.
- Viðskiptavinur verður reikningsfærður um $130 í upphafi (1. janúar) hvers árs af samningnum.

#### <a name="steps"></a>Skref

1. Setjið upp tvær losaðar vörur sem óreikningsfærðar vörur. Notaðu síðuna **Uppsetning óreikningsfærðra tekna** til að setja upp vörur og lykla sem nota óreikningsfærðar tekjur.
2. Í þessu dæmi er viðhaldsgjaldi frestað. Varan krefst frestunarsniðmáts sem er sett upp á síðunni **Sniðmát frestunar**. Sniðmátið er með tímabilstíðnina **Mánaðarlega** og skráningartímabil sem er 36 mánuðir á lengd. Því eru tekjurnar á mánuði $2,50.
3. Á síðunni **Vörum frestað sjálfgefið** skal stilla reitinn **Viðhaldsgjald** á **Frestanleg vara**. Þetta skref og næsta munu valda því að vara viðhaldsgjaldsins verður frestað þegar hún er seld eða höfð með í greiðsluáætlun.
4. Veldu **Sjálfgefnar frestanir** \> **Sniðmát** og bættu við vörunni fyrir viðhaldsgjaldið og línulegt sniðmát úr skrefi 2. Vara viðhaldsgjaldsins verður tengd við 36 mánaða frestunaráætlun.
5. Búðu til greiðsluáætlun sem inniheldur báðar óreikningsfærðu vörurnar. Greiðsluáætlunin fyrir samninginn er sett upp með eftirfarandi vörum.

    | Atriði | Upphafsdagsetning | Lokadagsetning | Upphæð | Greiðslutíðni | Frestunarvara | Óreikningsfærðar tekjur | Lýsing |
    |---|---|---|---|---|---|---|---|
    | Leyfi | 01. janúar 2022 | 31. desember 2024 | $100,00 | Árlega | Nr. | Já | Viðskiptavinur fær reikning upp á $100,00 á hverju ári. Samtals $300,00 verður skráð fyrirfram sem óreikningsfærðar tekjur á efnahagsreikninginn og sem tekjur á rekstrarreikninginn. Hver reikningur lækkar óreikningsfærðu upphæðina. |
    | Viðhald | 01. janúar 2022 | 31. desember 2024 | $30,00 | Árlega | Já | Já | Viðskiptavinur fær reikning upp á $30,00 á hverju ári. Samtals $90,00 verður skráð fyrirfram sem óreikningsfærðar tekjur og frestaðar tekjur á efnahagsreikninginn. Hver reikningur lækkar óreikningsfærðu upphæðina. Frestaðar tekjur verða skráðar mánaðarlega yfir 36 mánuði. |

6. Á síðunni **Allar greiðsluáætlanir** skaltu nota ferlið **Stofna færslu í færslubók** til að bóka samningsvirðið á efnahagsreikninginn sem óreikningsfærðar tekjur.

Tvær færslur færslubókar eru stofnaðar, ein fyrir hvora línu í greiðsluáætluninni.

| Lykill | Debetupphæð | Kreditupphæð |
|---|---|---|
| Lykill óreikningsfærðra tekna | $300,00 | |
| Tekjulykill | | $300,00 |

| Lykill | Debetupphæð | Kreditupphæð |
|---|---|---|
| Lykill óreikningsfærðra tekna | $90,00 | |
| Frestaðar tekjur | | $90,00 |

Samningurinn krefst þess að reikningur fyrir viðskiptavininn verði búinn til við upphaf hvers árs. Nota ferlið **Mynda reikning** til að búa til reikning. Þegar reikningurinn er búinn til er eftirfarandi fylgiskjal reikningsins bókað.

| Lykill| Debetupphæð | Kreditupphæð |
|---|---|---|
| Lykill óreikningsfærðra tekna | | $130,00 |
| Viðskiptakröfur | $130,00 | |

Þessi sama færsla í færslubók verður stofnuð af reikningum sem eru bókaðir við upphaf næstu tveggja ára. Lykill óreikningsfærðra tekna er minnkaður á hverju ári í ferlinu **Búa til reikning**. Mótlykill óreikningsfærðra tekna er notaður til að jafna lykil óreikningsfærðra tekna þegar mismunandi gengi er notað. 

Í síðasta skrefinu er færsla í skráningarbók stofnuð í hverjum mánuði til að skrá frestaðar tekjur úr viðhaldsgjaldinu. Hægt er að stofna færslu færslubókar með því að nota síðuna **Úrvinnsla skráningar**. Einnig er hægt að stofna hana með því að velja **Skráning** fyrir línurnar á síðunum **Frestunaráætlun**.

| Aðallykill | Debetupphæð | Kreditupphæð |
|---|---|---|
| Frestaðar tekjur | $2,50 | |
| Tekjur | | $2,50 |

Þessi færsla í færslubók verður stofnuð í hvert skipti sem úrvinnsla skráningar er keyrð fyrir þessa frestuðu vöru (samtals 36 sinnum).

#### <a name="short-term-fixed-year"></a>Skammtíma: Fast ár

Hægt er að nota óreikningsfærðar tekjur saman með skammtímavirkni með því að stilla reitinn **Óreikningsfært til skammtíma** á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur**. Eftirfarandi dæmi sýnir útreikninga sem eru gerðir þegar óreikningsfærðar tekjur eru notaðar saman með aðferðinni **Fast ár** fyrir óreikningsfært til skammtíma.

Greiðsluáætlun sem er með eftirfarandi skilyrði er búin til:

- **Upphafsdagsetning:** 1. júní 2020
- **Lokadagsetning:** 31. desember 2021
- **Einingarverð**: $100
- **Tíðni:** Mánaðarlega

Á síðunni **Allar greiðsluáætlanir** er upphafleg færsla í færslubók stofnuð með ferlinu **Stofna færslu í færslubók**. Núverandi upphæðir til skammtíma og langtíma eru reiknaðar á eftirfarandi hátt:

- **Upphæð núverandi óreikningsfærðra tekna til skamms tíma:** $700
- **Upphæð núverandi óreikningsfærðra tekna til langs tíma:** $1200

Reikningurinn er búinn til fyrir greiðslutímabilið frá 1. júní 2020 til og með 30. nóvember 2020. Núverandi upphæðir til skammtíma og langtíma eru reiknaðar á eftirfarandi hátt:

- **Upphæð núverandi óreikningsfærðra tekna til skamms tíma:** $100
- **Upphæð núverandi óreikningsfærðra tekna til langs tíma:** $1200

Reikningurinn er búinn til fyrir reikningstímabilið frá 1. desember 2020 til og með 31. desember 2020. Núverandi upphæðir til skammtíma og langtíma eru reiknaðar á eftirfarandi hátt:

- **Upphæð núverandi óreikningsfærðra tekna til skamms tíma:** $1200
- **Upphæð núverandi óreikningsfærðra tekna til langs tíma:** $0

#### <a name="short-term-rolling-periods"></a>Skammtíma: Veltutímabil

Hægt er að nota óreikningsfærðar tekjur saman með skammtímavirkni með því að stilla aðferð óreikningsfærðs til skammtíma á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur**, Eftirfarandi dæmi sýnir útreikninga sem eru gerðir þegar óreikningsfærðar tekjur eru notaðar saman með aðferðinni **Hlaupandi tímabil** fyrir óreikningsfært til skammtíma.

Greiðsluáætlun sem er með eftirfarandi skilyrði er búin til:

- **Upphafsdagsetning:** 1. júní 2020
- **Lokadagsetning:** 31. desember 2021
- **Einingarverð**: $100
- **Tíðni:** Mánaðarlega

Á síðunni **Allar greiðsluáætlanir** er upphafleg færsla í færslubók stofnuð með ferlinu **Stofna færslu í færslubók**. Núverandi upphæðir til skammtíma og langtíma eru reiknaðar á eftirfarandi hátt:

- **Upphæð núverandi óreikningsfærðra tekna til skamms tíma:** $1200
- **Upphæð núverandi óreikningsfærðra tekna til langs tíma:** $700

Reikningurinn er búinn til fyrir greiðslutímabilið frá 1. júní 2020 til og með 30. nóvember 2020. Núverandi upphæðir til skammtíma og langtíma eru reiknaðar á eftirfarandi hátt:

- **Upphæð núverandi óreikningsfærðra tekna til skamms tíma:** $1200
- **Upphæð núverandi óreikningsfærðra tekna til langs tíma:** $100

Reikningurinn er búinn til fyrir reikningstímabilið frá 1. desember 2020 til og með 31. desember 2020. Núverandi upphæðir til skammtíma og langtíma eru reiknaðar á eftirfarandi hátt:

- **Upphæð núverandi óreikningsfærðra tekna til skamms tíma:** $1200
- **Upphæð núverandi óreikningsfærðra tekna til langs tíma:** $0

### <a name="items-with-revenue-allocation"></a>Vörur með tekjuúthlutun

Tveimur vörum sem eru með mismunandi greiðslutíðni er bætt við greiðsluáætlunina. Bæði nota óreikningsfærðar tekjur og eru vörur sem hægt er að fresta.

- **Vörunúmer 1000:** Surface Pro 128GB

    - **Innheimtutíðni:** Einu sinni
    - **Einingarverð**:$1500
    - **Sjálfstætt söluverð:** $1600
    - **Samningstekjur:** $1465,26

- **Vörunúmer: S0021** Trygging sem er seld með vörunúmeri 1000.

    - **Greiðslutíðni:** Mánaðarleg í 12 mánuði
    - **Einingarverð:** $20 á mánuði
    - **Sjálfstætt söluverð:** $25
    - **Samningstekjur:** $264,74

Þar sem báðar vörurnar nota óreikningsfærðar tekjur og tekjuúthlutun verður heildarupphæð samningsins í endurnýjunarlínunni 0 (núll). Dálknum **Samningstekjur** er bætt við og hann sýnir upphæð samningstekna.

Eftirfarandi tafla sýnir upphaflega færslu í færslubók fyrir vörurnar og reikninginn.

| Aðallykill | Debetupphæð | Kreditupphæð |
|---|---|---|
| **Bókarfærsla vöru 1000** | | | 
| Lykill óreikningsfærðra tekna (401250) | $1465,26 | |
| Lykill tekjufrestunar (250600) | | $1465,26 |
| **Bókarfærsla vöru 0021** | | | 
| Lykill óreikningsfærðra tekna (401250) | $274,74 | |
| Lykill tekjufrestunar (250600) | | $274,74 |
| **Reikningur** | | |
| Lykill óreikningsfærðra tekna | | $1465,26 |
| Lykill óreikningsfærðra tekna | | $274,74 |
| Viðskiptakröfulykill (130100) | $1488,16 | |

#### <a name="changes-to-the-billing-schedule-line-billing-detail-line-or-revenue-allocation"></a>Breytingar á greiðsluáætlunarlínu, línu greiðsluupplýsinga eða tekjuúthlutun

Þegar einingarverði eða magni er breytt þarf að uppfæra upphæð samningstekna fyrir hverja vöru sem er hluti af tekjuúthlutuninni. Því er bókarfærslan endurreiknuð.

Til dæmis er einingarverði fyrir vöru 1000 breytt úr $1.500 í $1.600. Í þessu tilviki er upphæð samningstekna sjálfkrafa endurreiknað sem $1.549,47. Samningstekjur fyrir vöru S0021 eru endurreiknaðar sem $290,53.

Þegar breyting er staðfest og skráð eru upphaflegar færslur í færslubók fyrir báðar vörurnar bakfærðar og nýjar færslur í færslubók stofnaðar:

- **Vara 1000:** Upprunaleg færsla í færslubók að upphæð $1.465,26 er bakfærð. Ný bókarfærsla fyrir $1549,47 er stofnuð.
- **Vara S0021:** Upphafleg færsla í færslubók að upphæð $274,74 er bakfærð. Ný bókarfærsla fyrir $290,53 er stofnuð.

#### <a name="termination"></a>Lok

Vara S0021 er með upphafsdagsetningu í janúar 2020 og lokadagsetningu í desember 2020 en er sagt upp í júní 2020. Endurreikna þarf upphæð samningstekna fyrir báðar vörurnar:

- **Vara 1000:** Samningstekjurnar eru endurreiknaðar sem $1.567,67.
- **Vara S0021:** Samningstekjurnar eru endurreiknaðar sem $124,00.

Færsla í leiðréttingabók er stofnuð fyrir línuna sem er sagt upp. Færslan í færslubókinni fyrir línuna sem tilheyrir sama númeri margþátta ráðstöfunar er bakfærð og ný færsla í færslubók er stofnuð:

- **Vara 1000:** Upprunaleg færsla í færslubók að upphæð $1.465,26 er bakfærð. Færsla í leiðréttingarbók fyrir $1549,47 er stofnuð.
- **Vara S0021:** Upphafleg færsla í færslubók að upphæð $274,74 er bakfærð. Ný bókarfærsla fyrir $124,00 er stofnuð.
