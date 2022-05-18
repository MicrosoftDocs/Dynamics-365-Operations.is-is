---
title: Eiginleikar greiðsluáætlunar
description: Þetta efnisatriði útskýrir eiginleika innheimtuáætlana, eins og verðlagningaraðferðir, stighækkanir og afslætti, jöfnunardagsetningar, hlutfall, öfuga innheimtu og skiptan vöruflokka.
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
ms.openlocfilehash: 0ce323565a94e8e70d90a65b7a3143e984a1c159
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/04/2022
ms.locfileid: "8696647"
---
# <a name="billing-schedule-features"></a>Eiginleikar greiðsluáætlunar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði útskýrir eiginleika innheimtuáætlana og innheimtuáætlunarlína. Það lýsir mismunandi aðferðum sem eru notaðar við verðlagningu, hvernig á að nota stighækkanir og afslætti og hvernig á að bakfæra innheimtutímabili. Það inniheldur einnig dæmi um hlutfallsútreikninga og skiptan vöruflokka.

## <a name="pricing-methods"></a>Verðlagningaraðferðir

Þú getur notað eina af eftirfarandi verðlagningaraðferðum til að reikna út einingarverð vöru:

* Flatt
* Staðlað
* Lag
* Flatt lag

### <a name="flat-pricing"></a>Flat verð

Þegar aðferðin við flata verðlagningu er notuð er einingarverð fyrir línu greiðsluáætlunar á **Allar innheimtuáætlanir** síðu er hægt að breyta í hvaða gildi sem þú vilt. The **Verðeining** gildi er alltaf **1**. Þess vegna er **Einingaverð** og **Virði** gildi fyrir hlut eru þau sömu.

### <a name="standard-pricing-without-a-trade-agreement"></a>Hefðbundin verðlagning (án viðskiptasamnings)

Þegar staðlað verðlagningaraðferð er notuð án viðskiptasamnings, seturðu upp einingarverð fyrir greiðsluáætlunarlínu með því að velja **Vöruupplýsingastjórnun** á **Slepptu vöruupplýsingum** síðu. Einingaverðið er sýnt í **Grunnsöluverð** kafla. Það er reiknað sem *Verð*&divide;*Verð magn*.

### <a name="standard-pricing-with-a-trade-agreement"></a>Hefðbundin verðlagning (með viðskiptasamningi)

Eftirfarandi dæmi sýna staðlaða verðútreikninga þegar viðskiptasamningur er fyrir hendi. Þú getur búið til viðskiptasamninga frá **Slepptu vöruupplýsingum** síðu.

Bæði dæmin nota vöru sem hefur eftirfarandi verðflokka.

| Magn frá | Magn til | U af M | Verð | Verðeining |
|---|---|---|---|---|
| 0 | 10.000 | Hvert | 1.50 | 1 |
| 10.000 | 200 | Hvert | 1.25 | 1 |
| 200 | 999999 | Hvert | 1.00 | 1 |

**Dæmi 1**

Reikningsmagnið er 250 og venjuleg verðlagningaraðferð er notuð. Þar sem magnið er á bilinu 200–999.999 verðmagn, er einingarverðið 1,00. 

Nettóupphæðin er reiknuð á eftirfarandi hátt:

*Virði* = (*Magn*&times;*Verð*)&divide;*Verðeining* = (250&times; 1.00)&divide; 1 = 250

**Dæmi 2**

Reikningsmagnið er 100 og venjuleg verðlagningaraðferð er notuð. Þar sem reikningsmagnið er á bilinu 0–100 verðmagn, er einingarverðið 1,50.

> [!NOTE]
> Reikningsmagnið er á bilinu 0–100 í stað 100–200 bilsins vegna þess að í venjulegu magnjöfnunarhegðun passar magn ef það er *meira en eða jafnt og* „frá“ magninu og *minna en* "til" magnið.

Nettóupphæðin er reiknuð á eftirfarandi hátt:

*Virði* = (100&times; 1,50)&divide; 1 = 150

### <a name="tier-pricing"></a>Tier verðlagning

Fyrir eftirfarandi dæmi hefur vara eftirfarandi verðflokka.

| Magn frá | Magn til | U af M | Verð | Verðeining |
|---|---|---|---|---|
| 0 | 10.000 | Hvert | 1.50 | 10 |
| 10.000 | 200 | Hvert | 1.25 | 10 |
| 200 | 999999 | Hvert | 1.00 | 10 |

Ef reikningsmagnið er 250, og flokkaverðlagningaraðferðin er notuð, eru verð vörunnar reiknuð út á eftirfarandi hátt miðað við verðflokka:

- **Fyrstu 100 atriðin:** 100&times; 1,50 = 150,00
- **Önnur 100 atriði:** 100&times; 1,25 = 125,00
- **Eftirstöðvar:** 50&times; 1,00 = 50,00

Nettóupphæðin er reiknuð á eftirfarandi hátt:

*Virði* = (150,00&divide; 10) + (125,00&divide; 10) + (50,00&divide; 10) = 15,00 + 12,50 + 5,00 = 32,50

Eftir að nettóupphæðin hefur verið reiknuð er einingarverðið reiknað með því að deila nettóupphæðinni með magninu:

*Einingaverð* = 32,50&divide; 250 = 0,13

### <a name="flat-tier-pricing"></a>Fljótt verðlag

Fyrir eftirfarandi dæmi hefur vara eftirfarandi verðflokka.

| Magn frá | Magn til | U af M | Flöt upphæð lags | Verðeining |
|---|---|---|---|---|
| 0 | 50 | Hvert | 100.00 | 50 |
| 50 | 200 | Hvert | 150.00 | 200 |

Eftirfarandi tafla sýnir reikninga og einingaverð fyrir mismunandi magn sem eru keypt. Nettóupphæðin er reiknuð fyrst og síðan einingarverðið.

| Reikningur | Magn innkeypt | Einingarverð | Nettóupphæð |
|---|---|---|---|
| 1 | 25 | 2.00&divide; 25 = 0,08 | 100&divide; 50 = 2,00 |
| 2 | 20 | 2.00&divide; 20 = 0,10 | 100&divide; 50 = 2,00 |
| 3 | 50 | 2.00&divide; 50 = 0,04 | 100&divide; 50 = 2,00 |
| 4 | 60 | 0,75&divide; 60 = 0,0125 = 0,01 | 150&divide; 200 = 0,75 |

## <a name="escalations-and-discounts"></a>Hækkanir og afslættir

An *stigmögnun* er verðhækkun fyrir framtíðarreikningstímabil sem reikningurinn hefur ekki enn verið búinn til fyrir. A *afsláttur* er verðlækkun fyrir framtíðarreikningstímabil sem reikningurinn hefur ekki enn verið búinn til fyrir.

Í innheimtu áskriftar er ekki hægt að beita hækkunum og afslætti afturvirkt á innheimtuáætlun. Til dæmis er ekki hægt að beita stigmögnun á innheimtuáætlun þremur mánuðum í fortíðinni og vinna úr henni. Með öðrum orðum, þú getur ekki beitt verðhækkun sem varð fyrir þremur mánuðum.

Þú getur beitt hækkun eða afslátt á innheimtuáætlun eða innheimtuáætlunarlínu á einum af eftirfarandi stöðum:

- The **Allar/virkar innheimtuáætlanir** listasíðu
- Sérstök innheimtuáætlun
- Sérstök innheimtuáætlunarlína

### <a name="apply-an-escalation-or-discount"></a>Notaðu hækkun eða afslátt

Fylgdu þessum skrefum til að nota hækkun eða afslátt á innheimtuáætlun.

1. Veldu innheimtuáætlun eða innheimtuáætlunarlínu.
2. Veldu **Stækkun og afsláttur** annað hvort á **Stækkun og afsláttur** flipa eða á innheimtuáætlunarlínunni.
3. Ef vísitala neysluverðs er notuð til að reikna út hækkun eða afslátt skal velja gildi í **Útreikningur vísitölu neysluverðs** sviði.
4. Veldu **Nýtt** til að bæta við stigmögnunar- eða afsláttarlínu.
5. Til að fá afslátt skaltu velja **Afsláttur** gátreit. Fyrir stigmögnun, farðu frá **Afsláttur** gátreiturinn hreinsaður.
6. Stilltu **Upphafsdagur** og **Tíðni** sviðum.
7. Fyrir frestunaratriði sem nota óinnheimta tekjur eiginleiki, stilltu **Loka dagsetning** sviði.
8. Stilltu **Hlutfall**, **·**, eða **Áætlun um vísitölu neysluverðs** sviði.
9. Stilltu **Loka dagsetning** sviði.
10. Veldu **Í lagi**.
11. Endurtaktu skref 4 til 10 fyrir hverja viðbótarhækkunar- eða afsláttarlínu sem þú þarfnast.

### <a name="fields-on-the-billing-schedule-lines-page"></a>Reitir á síðunni Innheimtuáætlunarlínur

The **Innheimtuáætlunarlínur** síða inniheldur eftirfarandi reiti.

| Reitur | Lýsing |
|---|---|
| Vörunúmer | Vörunúmerið fyrir innheimtuáætlunarlínuna. Þessi reitur er aðeins tiltækur þegar síðan er opnuð úr greiðsluáætlunarlínu. |
| Útreikningur á vísitölu neysluverðs | <p>Veldu aðferðina sem er notuð til að reikna út hækkun vísitölu neysluverðs:</p><ul><li>**Fyrri vísitala neysluverðs** – Notaðu fyrra gildi vísitölu neysluverðs fyrir stighækkunarútreikning.</li><li>**Grunnvísitala neysluverðs** – Notaðu grunngildi vísitölu neysluverðs fyrir stigmögnunarútreikninginn.</li></ul> |
| **Lína** rist | |
| Afsláttur | <p>Stilltu gátreitinn til að tilgreina hvort breytingin á upphæðinni sé hækkun eða afsláttur:</p><ul><li>**Valið** – Breytingin tekur afslátt á innheimtuáætlun eða innheimtuáætlunarlínu.</li><li>**Hreinsað** – Breytingin beitir stigmögnun á innheimtuáætlun eða áætlunarlínu.</li></ul><p>Ekki er hægt að breyta stillingum þessa gátreits fyrir vörur sem nota óinnheimt tekjur. Að auki er ekki hægt að nota afslætti á vörur sem nota tekjuskiptingu.</p> |
| Upphafsdagsetning | Veldu upphafsdag hækkunar eða afsláttar. |
| Tíðni | Veldu tíðni hækkunar eða afsláttar: **Enginn**, **·**, **·**, **·**, eða **Árlega**. |
| Prósenta | Tilgreindu hlutfall hækkunar eða afsláttar. |
| Upphæð | Tilgreindu upphæð hækkunar eða afsláttar. |
| Áætlun um vísitölu neysluverðs | Veldu áætlun vísitölu neysluverðs sem notuð er við útreikninga. |
| Lokadagsetning | <p>Veldu lokadag hækkunar eða afsláttar.</p><p>**Athugið:** Þessi reitur er nauðsynlegur fyrir vörur sem nota óinnheimt tekjur eiginleiki.</p> |
| Áætlunarnúmer frestunar | <p>Númer frestunaráætlunar.</p><p>Þessi reitur er aðeins tiltækur þegar síðan er opnuð úr innheimtuáætlunarlínu.</p> |
| Rununúmer færslubókar | <p>Dagbókarlotunúmerið.</p><p>Þessi reitur er aðeins tiltækur þegar síðan er opnuð úr innheimtuáætlunarlínu.</p> |
| Heildarafsláttarupphæð | <p>Summa afsláttarupphæða fyrir allar línur í hnitanetinu.</p><p>Þessi reitur er aðeins tiltækur þegar síðan er opnuð úr innheimtuáætlunarlínu.</p> |
| Núverandi skammtíma óinnheimt tekjuupphæð | <p>Núverandi skammtíma óinnheimt tekjuupphæð.</p><p>Þessi upphæð birtist þegar skammtíma frestun aðferð er valin á **Endurteknar innheimtufæribreytur samnings** síðu og reikningar fyrir línuliðinn eru settir upp á **Uppsetning óinnheimtutekna** síðu.</p> |
| Núverandi langtíma óinnheimt tekjuupphæð | <p>Núverandi langtíma óinnheimt tekjuupphæð.</p><p>Þessi upphæð birtist þegar skammtíma frestun aðferð er valin á **Endurteknar innheimtufæribreytur samnings** síðu og reikningar fyrir línuliðinn eru settir upp á **Uppsetning óinnheimtutekna** síðu.</p> |

## <a name="proration-examples"></a>Dæmi um hlutfall

Útreikningar á hlutfalli geta byggst á fjölda daga eða mánaðarfjölda. Aðferðin sem notuð er við hlutfallsútreikninginn er stillt á **Endurteknar innheimtufæribreytur samnings** síðu. Hlutfallsaðferðin hefur áhrif á hvernig upphæðir eru reiknaðar út fyrir innheimtuáætlun í eftirfarandi tilvikum:

- Upphafleg sköpun
- Beiting hækkunar eða afsláttar
- Lok
- Staðsetning eða fjarlæging bið
- Viðbót á stuðningi eða endurnýjun

Hlutfallsaðferðin hefur einnig áhrif á útreikninga á mánaðarlegum endurteknum tekjum (MRR) skýrslu.

### <a name="example-1"></a>Dæmi 1

Árleg upphæð innheimtuáætlunar er $5,000. Upphafsdagur er 12. ágúst 2019 og lokadagur er 22. desember 2019. Innheimtutíðni er árleg. Hlutfallsleg upphæð er reiknuð út á eftirfarandi hátt, eftir því hvort notuð er dagleg eða mánaðarleg útreikningsaðferð:

- **Daglega**

    - *Fjöldi daga* = *Loka dagsetning* –*Upphafsdagur* + 1 = 133 dagar
    - *Fjöldi daga á árinu* = 11. ágúst 2020 – 12. ágúst 2019 + 1 = 366 dagar
    - *Hlutfallsleg upphæð* = 5.000&times; (133&divide; 366) = 1816,94

- **Mánaðarlega**

    - *Upphafsmánaðarhluti* = (31 – 12 + 1)&divide; 31 = 20&divide; 31
    - *Miðmánuðir* = 3
    - *Loka mánaðarhluti* = 22&divide; 31
    - Hlutfallsleg upphæð = 5.000&divide; 12&times;\[ (20&divide; 31) + 3 + (22&divide; 31)\] = 1814,52

### <a name="example-2"></a>Dæmi 2

Árleg upphæð innheimtuáætlunar er $12,000. Upphafsdagur er 1. ágúst 2019 og lokadagur er 31. desember 2019. Innheimtutíðni er árleg. Hlutfallsleg upphæð er reiknuð út á eftirfarandi hátt, allt eftir útreikningsaðferð:

- **Daglega**

    - *Fjöldi daga* = *Loka dagsetning* –*Upphafsdagur* + 1 = 153 dagar
    - *Fjöldi daga á árinu* = 31. júlí 2020 – 1. ágúst 2019 + 1 = 366 dagar
    - *Hlutfallsleg upphæð* = 12.000&times; (153&divide; 366) = 5016,39

- **Mánaðarlega (heill mánuður)**

    - *Fjöldi mánaða* = 5
    - *Samtals mánuðir* = 12
    - *Hlutfallsleg upphæð* = (12.000&times; 5)&divide; 12 = 5.000

## <a name="reversing-a-period-billing"></a>Innheimtu tímabils

Fyrir þetta dæmi hefur innheimtuáætlun aðeins eina línu:

- Innheimta fer fram mánaðarlega í 12 mánuði frá janúar til desember.
- Reikningar hafa verið búnir til fyrir öll tímabil fram í apríl.

Þú vilt bakfæra reikninginn fyrir reikningstímabilið í apríl.

Ef sölureikningur hafði ekki enn verið stofnaður fyrir reikningstímabilið í apríl gætirðu eytt sölupöntuninni. Í þessu tilviki er **Innheimt** staða fyrir smáatriðin yrði fjarlægð. Hins vegar, vegna þess að reikningur hefur verið búinn til fyrir reikningstímabilið, er **Innheimt** Ekki er hægt að hreinsa stöðu fyrir smáatriðin. Þess vegna, til að bakfæra innheimtu í apríl, verður þú að búa til jöfnunarkreditnótu fyrir línuna.

1. Á **Allar innheimtuáætlanir** síðu, búðu til áætlunarlínu fyrir sama hlut.
2. Breyttu **Magn** verðmæti vörunnar að mínus upprunalega magns.
3. Stilltu **Innheimtutíðni** sviði til **Einu sinni**.
4. Uppfærðu upphafs- og lokadagsetningar þannig að þær passi við dagsetningar reikningsupplýsingalínunnar sem þú vilt búa til kreditnótu fyrir. Fyrir þetta dæmi skaltu stilla upphafsdagsetningu á 1. apríl 2019 og lokadagsetningu á 30. apríl 2019.
5. Vista breytingarnar.
6. Opnaðu **Búðu til reikning** síðu og stofnaðu sölupöntunina sem hefur kreditnótu fyrir tilgreint tímabil.
7. Valfrjálst: Bókaðu reikninginn.

Þegar þú skoðar línurnar fyrir innheimtuáætlun muntu taka eftir því að nýja línan hefur tengil á inneignarnótu. Upprunalega línan mun enn hafa tengil á upprunalega apríl reikninginn.

## <a name="split-item-group-examples"></a>Dæmi um skiptan vöruhóp

Í þessu dæmi er eftirfarandi uppsetning til staðar:

- Á **Endurteknar innheimtufæribreytur samnings** síða, **Skipt eftir vöruflokki** er valið, og **Einstök áætlunargerð** reiturinn er stilltur á **Viðskiptavinur**.
- Þrír vöruflokkar hafa verið búnir til: **FORSKIPTI**, **·**, og **SPP**.
- Viðskiptavinur US-001 hefur margar innheimtuáætlanir þar sem vöruflokkurinn er PREFIX eða DATAHUB.
- Viðskiptavinur US-002 er með margar innheimtuáætlanir þar sem vöruflokkurinn er PREFIX eða SPP.

| Númer greiðsluáætlunar | Viðskiptavinur | Vöruflokkur |
|---|---|---|
| SCH001 | US-001 | FORSKIPTI |
| SCH002 | US-001 | DATAHUB |
| SCH003 | US-002 | FORSKIPTI |
| SCH004 | US-002 | SPP (staðlað greiðslutímabil) |

Viðskiptavinur US-001 kaupir endurnýjunarvöru sem tilheyrir PREFIX vöruflokknum. Þessi færsla er ný sölupöntun.

| Sölupöntun # | Viðskiptavinur | Aðalatriði | Vara endurnýjunar | Endurnýjunarvöruflokkur | Númer greiðsluáætlunar |
|---|---|---|---|---|---|
| SO0001 | US-001 | D0001 | D0002 | FORSKIPTI | SCH001 |

Þegar reikningur fyrir sölupöntun er bókaður er endurnýjunarliðnum bætt við núverandi greiðsluáætlun (SCH001) fyrir viðskiptamann. Þessi innheimtuáætlun notar PREFIX vöruflokkinn. Allir endurnýjunarliðir sem tilheyra sama vöruflokki eru settir í sömu innheimtuáætlun.

**Haus**
 
| Númer greiðsluáætlunar | Viðskiptavinur | Vöruflokkur |
|---|---|---| 
| SCH001 | US-001 | FORSKIPTI |

**Lína**

| Númer greiðsluáætlunar | Viðskiptavinur | Vöruflokkur |
|---|---|---|
| SCH001 | US-001 | D0002 |

Viðskiptavinur US-001 kaupir nú endurnýjunarvöru sem tilheyrir SPP vöruhópnum. Þessi færsla er ný sölupöntun.

| Sölupöntun # | Viðskiptavinur | Aðalatriði | Vara endurnýjunar | Endurnýjunarvöruflokkur | Númer greiðsluáætlunar |
|---|---|---|---|---|---|
| SO0002 | US-001 | D0003 | D0004 | SPP (staðlað greiðslutímabil) | |

Eins og er, hefur viðskiptavinur US-001 ekki innheimtuáætlun sem notar SPP vöruhópinn. Þess vegna er ný innheimtuáætlun búin til.

**Haus**

| Númer greiðsluáætlunar| Viðskiptavinur | Vöruflokkur |
|---|---|---|
| SCH005 | US-001 | SPP (staðlað greiðslutímabil) |

**Lína**

| Númer greiðsluáætlunar | Viðskiptavinur | Vöruflokkur |
|---|---|---|
| SCH005 | US-001 | D0004 |

### <a name="multiple-billing-schedules-for-the-same-end-user-and-customer"></a>Margar innheimtuáætlanir fyrir sama notanda og viðskiptavin

Í þessu dæmi er eftirfarandi uppsetning til staðar:

- Á **Endurteknar innheimtufæribreytur samnings** síða, **Skipt eftir vöruflokki** er valið, og **Einstök áætlunargerð** reiturinn er stilltur á **Endanotandi**.
- Á **Endir notendur** síðu er eftirfarandi viðskiptavinur og notendasamband sett upp.

    | Viðskiptavinalykill | Notandareikningur |
    |---|---|
    | US-001 | US-221 |

Margar innheimtuáætlanir eru búnar til fyrir samsetningu viðskiptavinar og endanotanda. Vegna þess að **Skipt eftir vöruflokki** er valið á **Endurteknar innheimtufæribreytur samnings** síðu er hægt að búa til margar innheimtuáætlanir fyrir sama viðskiptavin og endanotendasamband.

| Númer greiðsluáætlunar | Viðskiptavinur | Notandareikningur | Hlutaflokkur fyrir haus |
|---|---|---|---|
| SCH005 | US-001 | US-221 | IG1 |
| SCH006 | US-001 | US-221 | IG2 |
| SCH007 | US-001 | US-221 | IG3 |

Á **Uppsetning hlutar** síðu býrðu til stuðnings- og endurnýjunarsambönd.

| Vörukóði | Vöruvensl | Þjónustuvara | Vara endurnýjunar | Endurnýjunarvöruflokkur |
|---|---|---|---|---|
| Tafla | D001 | LIÐUR 27 | D007 | IG1 |
| Tafla | D002 | LIÐUR 28 | D005 | IG2 |
| Tafla | D003 | LIÐUR 29 | D006 | IG3 |

Þú stofnar nú sölupöntun fyrir viðskiptavin US-001. Þessi sölupöntun hefur vörur frá **Uppsetning hlutar** síðu. Þegar þú stofnar sölupöntunina skaltu opna **Stuðnings- og endurnýjunarferli** síðu og stilltu **Notendareikningur** reitinn og allar aðrar nauðsynlegar upplýsingar fyrir endurnýjunaratriðið.

Þegar reikningur fyrir færsluna er stofnaður og bókaður, eru mismunandi innheimtuáætlanir búnar til fyrir samsetningu viðskiptavinar/endanotanda og vöruflokks. Hægt er að úthluta fleiri en einni línu í sömu sölupöntun á sömu innheimtuáætlun.

| Sölupöntun # | Viðskiptavinur | Notandareikningur | Aðalatriði | Þjónustuvara | Vara endurnýjunar | Númer greiðsluáætlunar |
|---|---|---|---|---|---|---|
| SO0001 | US-001 | US-221 | D001 | LIÐUR 27 | D007 | SCH005 |
| SO0001 | US-001 | US-221 | D002 | LIÐUR 28 | D005 | SCH006 |
| SO0001 | US-001 | US-221 | D003 | LIÐUR 29 | D006 | SCH005 |
