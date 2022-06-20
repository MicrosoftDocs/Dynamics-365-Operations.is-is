---
title: Eiginleikar greiðsluáætlunar
description: Þessi grein útskýrir eiginleika innheimtuáætlana, eins og verðlagningaraðferðir, stighækkanir og afslætti, jöfnunardagsetningar, hlutfall, öfuga innheimtu og skiptan vöruflokka.
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
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853584"
---
# <a name="billing-schedule-features"></a>Eiginleikar greiðsluáætlunar

[!include [banner](../includes/banner.md)]

Þessi grein útskýrir eiginleika innheimtuáætlana og innheimtuáætlunarlína. Það lýsir mismunandi aðferðum sem eru notaðar við verðlagningu, hvernig á að nota stighækkanir og afslætti og hvernig á að bakfæra innheimtutímabili. Það inniheldur einnig dæmi um hlutfallsútreikninga og skiptan vöruflokka.

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
| 10.000 | 200 | Hvert | 1,25 | 1 |
| 200 | 999999 | Hvert | 1.00 | 1 |

**Dæmi 1**

Reikningsmagnið er 250 og venjuleg verðlagningaraðferð er notuð. Þar sem magnið er á bilinu 200–999.999 verðmagnsbili er einingarverðið 1,00. 

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
| 10.000 | 200 | Hvert | 1,25 | 10 |
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
2. Veldu **Stækkun og afsláttur** annað hvort á **Stækkun og afsláttur** flipanum eða á innheimtuáætlunarlínunni.
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
    - *Lok mánaðarhluti* = 22&divide; 31
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
    - *Hlutfallsleg upphæð* = (12.000 &times; 5) &divide; 12 = 5.000

## <a name="reversing-a-period-billing"></a>Bakfærsla tímabilsreiknings

Í þessu dæmi hefur innheimtuáætlun aðeins eina línu:

- Innheimta fer fram mánaðarlega í 12 mánuði frá janúar til desember.
- Reikningar hafa verið stofnaðir fyrir öll tímabil fram í apríl.

Á að bakfæra reikninginn fyrir reikningstímabilið apríl.

Ef sölureikningur hefði ekki enn verið stofnaður fyrir reikningstímabilið apríl er hægt að eyða sölupöntuninni. Í þessu tilfelli **yrði gjaldfærð** staða fyrir smáatriðin fjarlægð. En þar sem reikningur hefur verið stofnaður fyrir reikningstímabilið **er ekki hægt að hreinsa stöðu reikningsfærðra** upplýsinga fyrir smáatriðin. Þess vegna, til að bakfæra aprílreikninginn, verður að stofna mótkreditnótu fyrir línuna.

1. **Á síðunni Allar reikningsáætlanir** skal stofna áætlunarlínu fyrir sömu vöru.
2. Breyta gildinu **Magn** fyrir vöruna í neikvætt fyrir upprunalega magnið.
3. Reiturinn **Reikningstíðni er** stilltur á **Einu sinni**.
4. Uppfæra upphafs- og lokadagsetningar þannig að þær samsvari dagsetningum reikningsupplýsingalínu sem á að stofna kreditnótu fyrir. Til að setja sem dæmi upphafsdagsetninguna á 1. apríl 2019 og lokadagsetninguna til 30. apríl 2019.
5. Vista breytingarnar.
6. **Opna síðuna Mynda reikning** og stofna sölupöntunina sem er með kreditnótuna fyrir tilgreint tímabil.
7. Valfrjálst: Bóka reikninginn.

Þegar línurnar fyrir innheimtuáætlunina eru skoðaðar kemur í ljós að nýja línan er með tengil á kreditnótuna. Upprunalega línan verður enn með tengil á upphaflega aprílreikninginn.

## <a name="split-item-group-examples"></a>Skipta dæmum um vöruflokka

Í þessu dæmi er eftirfarandi uppsetning til staðar:

- **Á síðunni** Færibreytur ítrekunarsamnings **er skipt eftir vöruflokki** valið og reiturinn **Gerð einkvæmrar áætlunar** er stilltur á **Viðskiptamaður**.
- Þrír vöruflokkar hafa verið stofnaðir: **FORSKEYTI**, **DATAHUB** og **SPP**.
- US-001 viðskiptavinar er með margar reikningsáætlanir þar sem vöruflokkurinn er FORSKEYTI EÐA DATAHUB.
- US-002 viðskiptavinar er með margar reikningsáætlanir þar sem vöruflokkurinn er FORSKEYTI EÐA SPP.

| Númer greiðsluáætlunar | Viðskiptamaður | Vöruflokkur |
|---|---|---|
| SCH001 | US-001 | FORSKEYTI |
| SCH002 | US-001 | DATAHUB |
| SCH003 | US-002 | FORSKEYTI |
| SCH004 | US-002 | SPP (staðlað greiðslutímabil) |

Viðskiptavinur US-001 kaupir endurnýjunarvöru sem tilheyrir FORSKEYTISvöruflokknum. Þessi færsla er ný sölupöntun.

| Sölupöntun # | Viðskiptamaður | Aðalvara | Vara endurnýjunar | Endurnýjunarvöruflokkur | Númer greiðsluáætlunar |
|---|---|---|---|---|---|
| SO0001 | US-001 | D0001 | D0002 | FORSKEYTI | SCH001 |

Þegar reikningurinn fyrir sölupöntunina er bókaður er endurnýjunarvörunni bætt við fyrirliggjandi innheimtuáætlun (SCH001) fyrir viðskiptavininn. Þessi reikningsáætlun notar forskeytisvöruflokkinn. Allar endurnýjunarvörur sem tilheyra sama vöruflokki eru settar í sömu innheimtuáætlun.

**Haus**
 
| Númer greiðsluáætlunar | Viðskiptamaður | Vöruflokkur |
|---|---|---| 
| SCH001 | US-001 | FORSKEYTI |

**Lína**

| Númer greiðsluáætlunar | Viðskiptamaður | Vöruflokkur |
|---|---|---|
| SCH001 | US-001 | D0002 |

Viðskiptavinur US-001 kaupir nú endurnýjunarvöru sem tilheyrir SPP vöruflokknum. Þessi færsla er ný sölupöntun.

| Sölupöntun # | Viðskiptamaður | Aðalvara | Vara endurnýjunar | Endurnýjunarvöruflokkur | Númer greiðsluáætlunar |
|---|---|---|---|---|---|
| SO0002 | US-001 | D0003 | D0004 | SPP (staðlað greiðslutímabil) | |

Eins og er er US-001 viðskiptavinar ekki með innheimtuáætlun sem notar SPP-vöruflokkinn. Þess vegna er ný innheimtuáætlun stofnuð.

**Haus**

| Númer greiðsluáætlunar| Viðskiptamaður | Vöruflokkur |
|---|---|---|
| SCH005 | US-001 | SPP (staðlað greiðslutímabil) |

**Lína**

| Númer greiðsluáætlunar | Viðskiptamaður | Vöruflokkur |
|---|---|---|
| SCH005 | US-001 | D0004 |

### <a name="multiple-billing-schedules-for-the-same-end-user-and-customer"></a>Margar reikningsáætlanir fyrir sama notanda og viðskiptavin

Í þessu dæmi er eftirfarandi uppsetning til staðar:

- **Á síðunni** Færibreytur ítrekunarsamnings **er skipt eftir vöruflokki** valið og reiturinn **Gerð einkvæmrar áætlunar** er stilltur á **Notanda**.
- **Á síðunni Notendur eru** eftirfarandi tengsl viðskiptavinar og notanda sett upp.

    | Viðskiptavinalykill | Notandareikningur |
    |---|---|
    | US-001 | US-221 |

Margar reikningsáætlanir eru stofnaðar fyrir samsetningu viðskiptavinar og notanda. Þar sem **Skipt eftir vöruflokki** er valið á síðunni Færibreytur endurtekinna **samningsreikninga** er hægt að stofna margar reikningsáætlanir fyrir sömu tengsl viðskiptavinar og notanda.

| Númer greiðsluáætlunar | Viðskiptamaður | Notandareikningur | Vöruflokkur hauss |
|---|---|---|---|
| SCH005 | US-001 | US-221 | IG1 |
| SCH006 | US-001 | US-221 | IG2 |
| SCH007 | US-001 | US-221 | IG3 |

**Á síðunni Uppsetning** vöru eru stofnuð tengsl stuðnings- og endurnýjunarvöru.

| Vörukóði | Vöruvensl | Þjónustuvara | Vara endurnýjunar | Endurnýjunarvöruflokkur |
|---|---|---|---|---|
| Tafla | D001 | ATRIÐI27 | D007 | IG1 |
| Tafla | D002 | ATRIÐI28 | D005 | IG2 |
| Tafla | D003 | ATRIÐI29 | D006 | IG3 |

Nú er sölupöntun stofnuð fyrir viðskiptamanninn US-001. Þessi sölupöntun er með vörur af **síðunni Uppsetning** vöru. Þegar sölupöntunin er stofnuð skal opna **síðuna Stuðningur og endurnýjunarferli** og stilla **reitinn Reikningur** notanda og aðrar nauðsynlegar upplýsingar fyrir endurnýjunarvöruna.

Þegar reikningurinn fyrir færsluna er stofnaður og bókaður eru mismunandi reikningsáætlanir stofnaðar fyrir samsetningu viðskiptavinar/notanda og vöruflokks. Hægt er að úthluta fleiri en einni línu í sömu sölupöntun á sömu reikningsáætlun.

| Sölupöntun # | Viðskiptamaður | Notandareikningur | Aðalvara | Þjónustuvara | Vara endurnýjunar | Númer greiðsluáætlunar |
|---|---|---|---|---|---|---|
| SO0001 | US-001 | US-221 | D001 | ATRIÐI27 | D007 | SCH005 |
| SO0001 | US-001 | US-221 | D002 | ATRIÐI28 | D005 | SCH006 |
| SO0001 | US-001 | US-221 | D003 | ATRIÐI29 | D006 | SCH005 |
