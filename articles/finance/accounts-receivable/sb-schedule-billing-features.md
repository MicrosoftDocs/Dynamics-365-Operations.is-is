---
title: Eiginleikar greiðsluáætlunar
description: Þessi grein útskýrir eiginleika greiðsluáætlana, t.d. verðlagningaraðferðir, hækkanir og afslætti, samræmingardagsetningar, hlutfallsskiptingu, bakfærða greiðslu og skiptingu vöruflokka.
author: JodiChristiansen
ms.date: 11/04/2021
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
ms.openlocfilehash: b6cfebc2bbfe06e118bfc96f9ae0df6323805e39
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853584"
---
# <a name="billing-schedule-features"></a>Eiginleikar greiðsluáætlunar

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir eiginleika greiðsluáætlana og greiðsluáætlunarlína. Hún lýsir mismunandi aðferðum sem notaðar eru við verðlagningu, hvernig á að nota hækkanir og afslætti og hvernig á að bakfæra greiðslutímabili. Þar er einnig að finna dæmi um útreikninga hlutfallsskiptingar og skiptingu vöruflokka.

## <a name="pricing-methods"></a>Verðlagningaraðferðir

Hægt er að nota eina af eftirfarandi verðlagningaraðferðum við að reikna einingarverð vöru:

* Flatt
* Staðlað
* Lag
* Flatt lag

### <a name="flat-pricing"></a>Flöt verðlagning

Þegar föst verðlagningaraðferð er notuð er hægt að breyta vörulínu greiðsluáætlunar á síðunni **Allar greiðsluáætlanir** í hvaða gildi sem er. Gildið **Verðeining** er alltaf **1**. Því eru gildin **Einingarverð** og **Nettóupphæð** fyrir vöru þau sömu.

### <a name="standard-pricing-without-a-trade-agreement"></a>Stöðluð verðlagning (án viðskiptasamnings)

Þegar hefðbundin verðlagningaraðferð er notuð án verðsamnings setur þú upp einingarverð fyrir vörulínur greiðsluáætlunar með því að velja **Afurðaupplýsingastjórnun** á síðunni **Upplýsingar um afurðar**. Einingarverðið er sýnt í hlutanum **Grunnsöluverð**. Það er reiknað sem *Verð* &divide; *Magn í verði*.

### <a name="standard-pricing-with-a-trade-agreement"></a>Stöðluð verðlagning (með viðskiptasamningi)

Eftirfarandi dæmi sýna hefðbundna verðútreikninga þegar viðskiptasamningur er til staðar. Hægt er að búa til viðskiptasamninga á síðunni **Upplýsingar um losun afurðar**.

Í báðum dæmunum er notuð vara sem hefur eftirfarandi verðflokka.

| Magn úr | Magn til | U af M | Verð | Verðeining |
|---|---|---|---|---|
| 0 | 10.000 | Hvert | 1.50 | 1 |
| 10.000 | 200 | Hvert | 1,25 | 1 |
| 200 | 999999 | Hvert | 1.00 | 1 |

**Dæmi 1**

Reikningsnúmerið er 250 og hefðbundin verðlagning er notuð. Vegna þess að magnið er á verðbilinu 200-999.999 er magntalan 1,00. 

Nettóupphæðin reiknuð á eftirfarandi hátt:

*Nettóupphæð* = (*Magn* &times; *Verð*) &divide; *Verðeining* = (250 &times; 1,00) &divide; 1 = 250

**Dæmi 2**

Reikningsnúmerið er 100 og hefðbundin verðlagning er notuð. Vegna þess að reikningsmagnið er á verðbilinu 0–100 er einingaverðið 1,50.

> [!NOTE]
> Reikningsmagnið er á bilinu 0–100 í stað 100-200 vegna þess að í hefðbundinni hegðun magnsamsvörunar er magn samsvarað ef það er *meira en eða jafnt og* „frá“ magnið og *minna en* „til“ magnið.

Nettóupphæðin reiknuð á eftirfarandi hátt:

*Nettóupphæð* = (100 &times; 1,50) &divide; 1 = 150

### <a name="tier-pricing"></a>Verðlagning lags

Í eftirfarandi dæmi er vara með eftirfarandi verðflokka.

| Magn úr | Magn til | U af M | Verð | Verðeining |
|---|---|---|---|---|
| 0 | 10.000 | Hvert | 1.50 | 10 |
| 10.000 | 200 | Hvert | 1,25 | 10 |
| 200 | 999999 | Hvert | 1.00 | 10 |

Ef reikningsmagnið er 250 og verðlagningaraðferð þreps er notað eru verð varanna reiknuð út á eftirfarandi hátt, samkvæmt verðþrepunum:

- **Fyrstu 100 vörurnar:** 100 &times; 1,50 = 150,00
- **Aðrar 100 vörurnar:** 100 &times; 1,25 = 125,00
- **Eftirstandandi vörur:** 50 &times; 1,00 = 50,00

Nettóupphæðin reiknuð á eftirfarandi hátt:

*Nettóupphæð* = (150,00 &divide; 10) + (125,00 &divide; 10) + (50,00 &divide; 10) = 15,00 + 12,50 + 5,00 = 32,50

Eftir að nettóupphæðin er reiknuð er einingarverðið reiknað með því að deila nettóupphæðinni með magninu:

*Einingaverð* = 32,50 &divide; 250 = 0,13

### <a name="flat-tier-pricing"></a>Flöt verðlagning lags

Í eftirfarandi dæmi er vara með eftirfarandi verðflokka.

| Magn úr | Magn til | U af M | Flöt upphæð lags | Verðeining |
|---|---|---|---|---|
| 0 | 50 | Hvert | 100.00 | 50 |
| 50 | 200 | Hvert | 150.00 | 200 |

Eftirfarandi tafla sýnir reikninga og einingarverð fyrir mismunandi magn sem keypt er. Nettóupphæðin er reiknuð fyrst og síðan er einingarverðið reiknað.

| Reikningur | Magn innkeypt | Einingarverð | Nettóupphæð |
|---|---|---|---|
| 1 | 25 | 2,00 &divide; 25 = 0,08 | 100 &divide; 50 = 2,00 |
| 2 | 20 | 2,00 &divide; 20 = 0,10 | 100 &divide; 50 = 2,00 |
| 3 | 50 | 2,00 &divide; 50 = 0,04 | 100 &divide; 50 = 2,00 |
| 4 | 60 | 0,75 &divide; 60 = 0,0125 = 0,01 | 150 &divide; 200 = 0,75 |

## <a name="escalations-and-discounts"></a>Hækkanir og afslættir

*Hækkun* er verðhækkun fyrir komandi greiðslutímabil sem reikningurinn hefur ekki enn verið búinn til fyrir. *Afsláttur* er verðlækkun fyrir komandi greiðslutímabil sem reikningurinn hefur ekki enn verið búinn til fyrir.

Í áskriftargreiðslum er ekki hægt að nota hækkanir og afslætti afturvirkt í greiðsluáætlun. Til dæmis er ekki hægt að nota hækkun á greiðsluáætlun þrjá mánuði aftur í tímann og vinna úr henni. Með öðrum orðum er ekki hægt að beita verðhækkun sem átti sér stað fyrir þremur mánuðum.

Hægt er að nota hækkun eða afslátt á greiðsluáætlun eða greiðsluáætlunarlínu á einum af eftirfarandi stöðum:

- Listasíðan **Allar/Virkar greiðsluáætlanir**
- Tiltekin greiðsluáætlun
- Tiltekin greiðsluáætlunarlína

### <a name="apply-an-escalation-or-discount"></a>Nota hækkun eða afslátt

Til að nota hækkun eða afslátt á greiðsluáætlun skaltu fylgja þessum skrefum.

1. Veljið greiðsluáætlun eða línu í greiðsluáætlun.
2. Veldu **Hækkun og afsláttur** annaðhvort í flipanum **Hækkun og afsláttur** eða í greiðsluáætlunarlínunni.
3. Ef notuð er vísitala neysluverðs til að reikna út hækkun eða afslátt skal velja gildi í reitnum **Útreikningur á vísitölu neysluverðs**.
4. Veldu **Nýtt** til að bæta við hækkunar- eða afsláttarlínu.
5. Fyrir afslátt, veljið gátreitinn **Afsláttur**. Til að hækka skal hafa gátreitinn **Afsláttur** auðan.
6. Stillið reitina **Upphafsdagsetning** og **Tíðni**.
7. Fyrir frestunarvörur sem nota eiginleika óreikningsfærðra tekna skal stilla stilla reitinn **Lokadagur**.
8. Veldu reitinn **Prósent**, **Upphæð** eða **Áætlun um vísitölu neysluverðs**.
9. Stillið svæðið **Lokadagsetning**.
10. Veldu **Í lagi**.
11. Endurtakið skref 4 til 10 fyrir hverja hækkunar- eða afsláttarlínu í viðbót sem þörf er á.

### <a name="fields-on-the-billing-schedule-lines-page"></a>Reitir á síðunni Greiðsluáætlunarlínur

Síðan **Greiðsluáætlunarlínur** inniheldur eftirfarandi reiti.

| Svæði | Lýsing |
|---|---|
| Vörunúmer | Vörunúmerið fyrir greiðsluáætlunarlínuna. Þetta svæði er aðeins tiltækt þegar síðan er opnuð frá vöru greiðsluáætlunarlínu. |
| Útreikningur á vísitölu neysluverðs | <p>Veljið aðferðina sem er notuð til að reikna út hækkun vísitölu neysluverð:</p><ul><li>**Fyrri vísitala neysluverðs** – Notaðu fyrra gildi vísitölu neysluverðs fyrir útreikning hækkunar.</li><li>**Grunnvísitala neysluverðs** – Notaðu grunnvísitölu neysluverðs fyrir útreikning hækkunar.</li></ul> |
| **Línunet** | |
| Afsláttur | <p>Veljið gátreitinn til að tilgreina hvort breytingin á upphæðinni er hækkun eða afsláttur:</p><ul><li>**Valið** – Breytingin úthlutar afslætti á greiðsluáætlunina eða greiðsluáætlunarlínuna.</li><li>**Hreinsað** – Breytingin á við um hækkun á greiðsluáætlun eða áætlunarlínu.</li></ul><p>Ekki er hægt að breyta stillingu þessa gátreits fyrir vörur sem nota eiginleikann fyrir óreikningsfærðar tekjur. Þar að auki er ekki hægt að nota afslætti fyrir vörur sem nota tekjuskiptingu.</p> |
| Upphafsdagsetning | Velja upphafsdag hækkunar eða afsláttar. |
| Tíðni | Veldu tíðni hækkunar eða afsláttar: **Ekkert**, **Mánaðarlega**, **Ársfjórðungslega**, **Hálfs árs fresti** eða **Árlega**. |
| Prósenta | Tilgreinið prósentutölu hækkunarinnar eða afsláttarins. |
| Upphæð | Tilgreinið upphæð hækkunar eða afsláttar. |
| Áætlun um vísitölu neysluverðs | Veljið áætlun vísitölu neysluverðs sem notuð er við útreikningana. |
| Lokadagsetning | <p>Veljið lokadag hækkunar eða afsláttar.</p><p>**Til athugunar:** Þessi reitur er nauðsynlegur fyrir vörur sem nota eiginleikann fyrir óreikningsfærðar tekjur.</p> |
| Áætlunarnúmer frestunar | <p>Áætlunarnúmer frestunarinnar.</p><p>Þetta svæði er aðeins tiltækt þegar síðan er opnuð frá línu greiðsluáætlunar.</p> |
| Rununúmer færslubókar | <p>Rununúmer færslubókar.</p><p>Þetta svæði er aðeins tiltækt þegar síðan er opnuð frá línu greiðsluáætlunar.</p> |
| Heildarafsláttarupphæð | <p>Samtala afsláttarfjárhæða fyrir allar línur í töflunni.</p><p>Þetta svæði er aðeins tiltækt þegar síðan er opnuð frá línu greiðsluáætlunar.</p> |
| Núgildandi skammtíma óreikningsfærð tekjuupphæð | <p>Núgildandi skammtíma óreikningsfærð tekjuupphæð.</p><p>Þessi upphæð birtist þegar skammtíma frestunarleið er valin á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur** á lyklarnir fyrir vörulínuna eru uppsettir á síðunni **Uppsetning óreikningsfærðra tekna**.</p> |
| Núgildandi langtíma óreikningsfærð tekjuupphæð | <p>Núgildandi langtíma óreikningsfærð tekjuupphæð.</p><p>Þessi upphæð birtist þegar skammtíma frestunarleið er valin á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur** á lyklarnir fyrir vörulínuna eru uppsettir á síðunni **Uppsetning óreikningsfærðra tekna**.</p> |

## <a name="proration-examples"></a>Dæmi um skiptingu

Útreikningar fyrir skiptingu geta verið byggðir á fjölda daga eða fjölda mánaða. Aðferðin sem er notuð við útreikning hlutfallsskiptingar er stillt á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur**. Aðferð hlutfallsskiptingar hefur áhrif á hvernig upphæðir eru reiknaðar fyrir greiðsluáætlun í eftirfarandi aðstæðum:

- Upprunaleg stofnun
- Notkun hækkunar eða afsláttar
- Lok
- Staðsetning eða fjarlæging biðstöðu
- Viðbót við stuðning eða endurnýjun

Aðferð hlutfallsskiptingar hefur einnig áhrif á útreikninga í skýrslu um mánaðarlegar endurteknar tekjur.

### <a name="example-1"></a>Dæmi 1

Árleg upphæð greiðsluáætlunar er $5000. Upphafsdagurinn er 12. ágúst 2019 og lokadagurinn er 22. desember 2019. Greiðslur eru árlegar. Hlutfallsleg upphæð er reiknuð á eftirfarandi hátt, eftir því hvort notuð er dagleg eða mánaðarleg reikniaðferð:

- **Daglega**

    - *Dagafjöldi* = *Lokadagur* – *Upphafsdagur* + 1 = 133 dagar
    - *Fjöldi daga á árinu* = 11. ágúst 2020 – 12. ágúst 2019 + 1 = 366 dagar
    - *Hlutfallsleg upphæð* = 5000 &times; (133 &divide; 366) = 1816,94

- **Mánaðarlega**

    - *Upphafsmánaðarhluti* = (31 – 12 + 1) &divide; 31 = 20 &divide; 31
    - *Miðmánuðir* = 3
    - *Hlutur loka mánaðar* = 22 &divide; 31
    - Hlutfallsleg upphæð= 5000 &divide; 12 &times; \[(20 &divide; 31) + 3 + (22 &divide; 31)\] = 1814,52

### <a name="example-2"></a>Dæmi 2

Árleg upphæð greiðsluáætlunar er 12.000 dollarar. Upphafsdagurinn er 1. ágúst 2019 og lokadagurinn er 31. desember 2019. Greiðslur eru árlegar. Hlutfallsleg upphæð er reiknuð út á eftirfarandi hátt, eftir því hvaða reikniaðferð er notuð:

- **Daglega**

    - *Dagafjöldi* = *Lokadagur* – *Upphafsdagur* + 1 = 153 dagar
    - *Fjöldi daga á árinu* = 31. júlí 2020 – 1. ágúst 2019 + 1 = 366 dagar
    - *Hlutfallsleg upphæð* = 12.000 &times; (153 &divide; 366) = 5016,39

- **Mánaðarlega (heill mánuður)**

    - *Fjöldi mánaða* = 5
    - *Heildarfjöldi mánaða* = 12
    - *Hlutfallsleg upphæð* = (12.000 &times; 5) &divide; 12 = 5000

## <a name="reversing-a-period-billing"></a>Bakfærsla reikningstímabils

Í þessu dæmi hefur greiðsluáætlun aðeins eina línu:

- Greitt er mánaðarlega í 12 mánuði frá janúar til og með desember.
- Reikningar hafa verið stofnaðir fyrir öll tímabil fram í apríl.

Þú vilt afturkalla reikninginn fyrir reikningstímabilið í apríl.

Ef sölureikningur hefur ekki enn verið stofnaður fyrir greiðslutímabilið í apríl geturðu eytt sölupöntuninni. Í þessu tilfelli væri staðan **Greitt** fyrir upplýsingarnar fjarlægð. Þar sem reikningur hefur verið stofnaður fyrir greiðslutímabilið er hins vegar ekki hægt að hreinsa stöðuna **Reikningsfært** fyrir upplýsingarnar. Til að afturkalla greiðsluna í apríl þarf því að stofna kreditnótu mótbókunar fyrir línuna.

1. Á síðunni **Allar greiðsluáætlanir** skal búa til áætlunarlínu fyrir sömu vöruna.
2. Breytið gildi **Magn** fyrir vörun í neikvætt gildi af upphaflegu magni.
3. Stillið reitinn **Greiðslutíðni** á **Einu sinni**.
4. Uppfærðu upphafs- og lokadagsetningarnar svo að þær stemmi við dagsetningar í línu greiðsluupplýsinga sem á að búa til kreditnótu fyrir. Til dæmis skaltu stilla upphafsdagsetningu á 1. apríl 2019 og lokadagsetningu á 30. apríl 2019.
5. Vista breytingarnar.
6. Opnaðu síðuna **Búa til reikning** og stofnaðu sölupöntunina sem er með kreditnótuna fyrir tiltekið tímabil.
7. Valkvæmt: Bóka reikninginn.

Þegar þú ferð yfir línurnar fyrir greiðsluáætlunina tekurðu eftir að nýja línan er með tengil á kreditnótuna. Upprunalega línan verður áfram með tengil á upprunalega aprílreikninginn.

## <a name="split-item-group-examples"></a>Dæmi um skiptan vöruflokk

Í þessu dæmi er eftirfarandi uppsetning til staðar:

- Á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur** er **Skipta eftir vöruflokki** valið og reiturinn **Gerð einkvæmrar áætlunar** er stilltur á **Viðskiptavinur**.
- Þrír vöruflokkar hafa verið stofnaðir: **PREFIX**, **DATAHUB** og **SPP**.
- Viðskiptavinur US-001 er með margar greiðsluáætlanir þar sem vöruflokkurinn er PREFIX eða DATAHUB.
- Viðskiptavinur US-002 er með margar greiðsluáætlanir þar sem vöruflokkurinn er PREFIX eða SPP.

| Númer greiðsluáætlunar | Viðskiptamaður | Vöruflokkur |
|---|---|---|
| SCH001 | US-001 | FORSKEYTI |
| SCH002 | US-001 | DATAHUBNAME |
| SCH003 | US-002 | FORSKEYTI |
| SCH004 | US-002 | SPP (staðlað greiðslutímabil) |

Viðskiptavinur US-001 kaupir endurnýjunarvöru sem tilheyrir vöruflokknum PREFIX. Þessi færsla er ný sölupöntun.

| Sölupöntun # | Viðskiptamaður | Aðalvara | Vara endurnýjunar | Endurnýjunarvöruflokkur endurnýjunar | Númer greiðsluáætlunar |
|---|---|---|---|---|---|
| SO0001 | US-001 | D0001 | D0002 | FORSKEYTI | SCH001 |

Þegar reikningurinn fyrir sölupöntunina er bókaður er endurnýjunarvörunni bætt við fyrirliggjandi greiðsluáætlun (SCH001) fyrir viðskiptavininn. Þessi greiðsluáætlun notar vöruflokkinn PREFIX. Allar endurnýjunarvörur sem tilheyra sama vöruflokki eru settar í sömu greiðsluáætlun.

**Haus**
 
| Númer greiðsluáætlunar | Viðskiptamaður | Vöruflokkur |
|---|---|---| 
| SCH001 | US-001 | FORSKEYTI |

**Lína**

| Númer greiðsluáætlunar | Viðskiptamaður | Vöruflokkur |
|---|---|---|
| SCH001 | US-001 | D0002 |

Viðskiptavinur US-001 kaupir nú endurnýjunarvöru sem tilheyrir SPP-vöruflokknum. Þessi færsla er ný sölupöntun.

| Sölupöntun # | Viðskiptamaður | Aðalvara | Vara endurnýjunar | Endurnýjunarvöruflokkur endurnýjunar | Númer greiðsluáætlunar |
|---|---|---|---|---|---|
| SO0002 | US-001 | D0003 | D0004 | SPP (staðlað greiðslutímabil) | |

Sem stendur er viðskiptavinur US-001 ekki með greiðsluáætlun sem notar SPP-vöruflokkinn. Því er ný greiðsluáætlun stofnuð.

**Haus**

| Númer greiðsluáætlunar| Viðskiptamaður | Vöruflokkur |
|---|---|---|
| SCH005 | US-001 | SPP (staðlað greiðslutímabil) |

**Lína**

| Númer greiðsluáætlunar | Viðskiptamaður | Vöruflokkur |
|---|---|---|
| SCH005 | US-001 | D0004 |

### <a name="multiple-billing-schedules-for-the-same-end-user-and-customer"></a>Margar greiðsluáætlanir fyrir sama notanda og viðskiptavin

Í þessu dæmi er eftirfarandi uppsetning til staðar:

- Á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur** er **Skipta eftir vöruflokki** valið og reiturinn **Gerð einkvæmrar áætlunar** er stilltur á **Notandi**.
- Á síðunni **Notendur** er eftirfarandi samsetning viðskiptavinar og notanda sett upp.

    | Viðskiptavinalykill | Notandareikningur |
    |---|---|
    | US-001 | US-221 |

Fjölmargar greiðsluáætlanir eru stofnaðar fyrir samsetningu viðskiptavinar og notanda. Vegna þess að **Skipta eftir vöruflokki** er valið á síðunni **Færibreytur fyrir endurteknar samningsgreiðslur** er hægt að búa til margar greiðsluáætlanir fyrir sömu tengsl viðskiptavinar og notanda.

| Númer greiðsluáætlunar | Viðskiptamaður | Notandareikningur | Vöruflokkur hauss |
|---|---|---|---|
| SCH005 | US-001 | US-221 | IG1 |
| SCH006 | US-001 | US-221 | IG2 |
| SCH007 | US-001 | US-221 | IG3 |

Á síðunni **Vöruuppsetning** er hægt að búa til stuðnings- og endurnýjunarvöruvensl.

| Vörukóði | Vöruvensl | Þjónustuvara | Vara endurnýjunar | Endurnýjunarvöruflokkur endurnýjunar |
|---|---|---|---|---|
| Tafla | D001 | ITEM27 | D007 | IG1 |
| Tafla | D002 | ITEM28 | D005 | IG2 |
| Tafla | D003 | ITEM29 | D006 | IG3 |

Nú er hægt að stofna sölupöntun fyrir viðskiptavin US-001. Þessi sölupöntun er með hluti af síðunni **Vöruuppsetning**. Þegar sölupöntunin er stofnuð skaltu opna síðuna **Þjónustu- og endurnýjunarferli** og stilla reitinn **Notandareikningur** og aðrar nauðsynlegar upplýsingar fyrir endurnýjunarvöruna.

Þegar reikningurinn fyrir færsluna er búinn til og bókaður eru mismunandi greiðsluáætlanir búnar til fyrir samsetningu viðskiptavinar/notanda og vöruflokks. Hægt er að úthluta fleiri en einni línu á sömu sölupöntun á sömu greiðsluáætlun.

| Sölupöntun # | Viðskiptamaður | Notandareikningur | Aðalvara | Þjónustuvara | Vara endurnýjunar | Númer greiðsluáætlunar |
|---|---|---|---|---|---|---|
| SO0001 | US-001 | US-221 | D001 | ITEM27 | D007 | SCH005 |
| SO0001 | US-001 | US-221 | D002 | ITEM28 | D005 | SCH006 |
| SO0001 | US-001 | US-221 | D003 | ITEM29 | D006 | SCH005 |
