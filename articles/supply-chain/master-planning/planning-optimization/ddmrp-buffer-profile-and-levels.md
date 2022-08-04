---
title: Stuðpúðarsnið og stig
description: Þessi grein veitir upplýsingar um stuðpúðasnið og magn, sem ákvarða lágmarks- og hámarksbirgðamagn sem ætti að halda fyrir hvern aftengingarpunkt.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: dd72332abefd31fd391ff66931a5abae0efb08de
ms.sourcegitcommit: 529fc10074b06f4c4dc52f2b4dc1f159c36e8dbc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/22/2022
ms.locfileid: "9186574"
---
# <a name="buffer-profile-and-levels"></a>Stuðpúðarsnið og stig

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Eftir að þú hefur greint aftengingarpunktana þína (lykilatriði sem þú munt geyma á lager), verður þú að ákveða hversu mikið af lager (buffer) þú ætlar að geyma á hverjum þeirra. Þetta verkefni er annað skref í Demand Driven Materials Resource Planning (DDMRP).

## <a name="buffer-levels-and-zones"></a>Stuðpúðastig og svæði

Í DDMRP er hver lagerbuffi skilgreindur með því að nota þrjú gildi: lágmarksmagn, hámarksmagn og endurpöntunarpunkt. Þessi gildi koma á þremur mismunasvæðum, sem auðkennd eru með eftirfarandi litakóðum:

- **Rautt svæði** – Svæðið undir lágmarksmagni. Lágmarksmagnið er einnig nefnt „topp af rauðu“ og skipulagsáætlun þín ætti að vera hönnuð til að tryggja að birgðir séu alltaf yfir þessum punkti.
- **Gult svæði** – Svæðið á milli lágmarksmagns og endurpöntunarpunkts. Endurröðunarpunkturinn er einnig nefndur „toppur af gulum“. Þegar þessum tímapunkti er náð ætti kerfið að endurraða.
- **Grænt svæði** – Svæðið á milli endurpöntunarpunkts og hámarksmagns. Hámarksmagnið er einnig nefnt „toppur af grænu“. Þessi punktur er hámarksstigið sem birgðirnar verða endurnýjaðar í.

Eftirfarandi mynd sýnir lituðu svæðin þrjú og hvernig þau tengjast lágmarksmagni, hámarksmagni og endurpöntunarpunkti.

![DDMRP biðminni svæði og stig.](media/ddmrp-buffer-levels.png "DDMRP biðminni svæði og stig")

## <a name="calculating-the-buffer-zones"></a>Útreikningur á biðminni

Þessi hluti útskýrir hvernig hæð hvers biðminni er reiknuð út.

Gula svæðið er venjulega reiknað fyrst. Þetta svæði táknar magnið sem þú neytir frá því augnabliki þegar þú pantar þar til pöntunin berst. Með öðrum orðum, það er væntanleg neysla á áfyllingartímanum. Það er reiknað með því að nota eftirfarandi jöfnu:

- **Gult svæði** = *Dagleg meðalnotkun (ADU)* ×*Aftengdur leiðtími*

The *aftengdur leiðtími* táknar þann tíma sem þarf til að framleiða eða taka á móti vöru ef aftengingarpunktarnir eru alltaf til á lager. Það er venjulega miklu styttra en *uppsafnaður leiðtími* sem jafnan er notað í aðalskipulagi. Réttar biðminnistillingar eru lykillinn að því að tryggja að aftengingarpunktar séu alltaf til á lager en ekki of mikið.

Rauða svæðið er reiknað út með því að nota eftirfarandi jöfnur:

- **Rauður grunnur** = *ADU* ×*Aftengdur leiðtími* ×*Leiðslutími þáttur*
- **Rautt öryggi** = *Rauður grunnur* ×*Breytileikastuðull*
- **Rautt svæði** = *Rauður grunnur* + *Rautt öryggi*

Græna svæðið er reiknað sem hámarksniðurstaða af eftirfarandi þremur jöfnum:

- *Lágmarksmagn pöntunar*
- *ADU* ×*Panta hringrás*
- *ADU* ×*Aftengdur leiðtími* ×*Leiðslutími þáttur*

## <a name="calculating-average-daily-usage"></a>Að reikna út meðaltal daglegrar notkunar

Kerfið notar eina af þremur aðferðum til að reikna út magnið sem þú neytir á dag:

- **Dagleg meðalnotkun (fyrri)** – Þessi nálgun byggir á raunverulegri fyrri neyslu.
- **Dagleg meðalnotkun (áfram)** – Þessi nálgun byggir á spáðri neyslu í framtíðinni.
- **Dagleg meðalnotkun (blandað)** – Þessi nálgun byggir á veginni blöndu fyrri og spáðrar neyslu.

### <a name="average-daily-usage-past"></a>Dagleg meðalnotkun (fyrri)

Fyrri ADU er reiknað sem meðaltal með því að leggja saman magnið sem er notað á hverjum degi í tiltekinn fjölda liðinna daga og deila síðan heildarfjöldanum með fjölda daga. Eftirfarandi mynd sýnir hvernig þessi aðferð virkar þegar útreikningurinn lítur þrjá daga í fortíðina.

![Dagleg meðalnotkun (fyrri) graf.](media/ddmrp-adu-past.png "Dagleg meðalnotkun (fyrri) graf")

Í fyrri myndinni, ef dagurinn í dag er að morgni 11. júní, er ADU fyrir síðustu þrjá daga (8., 9. og 10. júní) 21.

- **ADU (fortíð)** = (29 + 11 + 23) ÷ 3 = 21

### <a name="average-daily-usage-forward"></a>Dagleg meðalnotkun (áfram)

Fyrir nýja vöru gætir þú ekki haft nein fyrri notkunargögn. Þess vegna gætirðu í staðinn notað áætlaða ADU framvegis (til dæmis byggt á spáð eftirspurn). Eftirfarandi mynd sýnir hvernig þessi nálgun virkar þegar útreikningurinn lítur þrjá daga fram í tímann (þar á meðal í dag).

![Meðaltal daglegrar notkunar (áfram).](media/ddmrp-adu-forward.png "Meðaltal daglegrar notkunar (áfram).")

Í fyrri myndinni, ef dagurinn í dag er að morgni 11. júní, er ADU næstu þrjá daga (11., 12. og 13. júní) 21,66.

- **ADU (áfram)** = (18 + 18 + 29) ÷ 3 = 21,66

### <a name="average-daily-usage-blended"></a>Dagleg meðalnotkun (blandað)

Blandað ADU sameinar meðaltal fyrri notkunar og meðalframvirkrar notkunar, eins og sýnt er á eftirfarandi mynd.

![Meðaltal daglegrar notkunar (blandað) graf.](media/ddmrp-adu-blended.png "Meðaltal daglegrar notkunar (blandað) graf")

Í fyrri myndinni, ef dagurinn í dag er að morgni 11. júní, er blandað ADU fyrir fyrri og næstu þrjá daga (8. til 13. júní) 21.33.

- **ADU blandað** = (*ADU fortíð* + *ADU áfram*) ÷ 2<br>= (21 + 21,66) ÷ 2<br>= 21.33

## <a name="buffer-calculation-factors"></a>Stuðlar að reikna stuðpúða

Fyrir hvern hlut er hægt að skilgreina tvo þætti til að stilla hversu stórt rauða og græna svæðið eiga að vera. Þannig er hægt að jafna upp áætluðum afgreiðslutíma og eftirspurnarbreytileika.

![Leiðslutími og breytileikaþættir.](media/ddmrp-zone-factors.png "Leiðslutími og breytileikaþættir")

Fyrsti þátturinn er *leiðtímastuðull*. Gildið er aukastaf frá 0 til 1. Því lengri leiðslutími er, því lægra ætti gildið að vera. The Demand Driven Institute mælir með eftirfarandi sviðum:

- **Langur leiðtími:** 0,20–0,40
- **Miðlungs leiðtími:** 0,41–0,60
- **Stuttur leiðtími:** 0,61–1,00

Annar þátturinn er *breytileikastuðull*. Gildið er aukastaf frá 0 til 1. Því meiri sem eftirspurnarbreytileiki er, því lægra ætti gildið að vera. The Demand Driven Institute mælir með eftirfarandi sviðum:

- **Lítill breytileiki:** 0,20–0,40
- **Miðlungs breytileiki:** 0,41–0,60
- **Mikill breytileiki:** 0,61–1,00

## <a name="buffer-calculation-examples"></a>Dæmi um reikningsstuðla

Þetta dæmi heldur áfram koddaframleiðsludæminu sem er að finna í [Staðsetning birgða](ddmrp-inventory-positioning.md). Í því dæmi valdir þú aftengingarpunkta sem styttu afgreiðslutíma úr 21 degi í fimm daga, eins og sýnt er á eftirfarandi mynd.

![Dæmi um ótengdan leiðtíma.](media/ddmrp-bom-decoupled-lead-time-example.png "Dæmi um ótengdan leiðtíma")

Í þessu dæmi, gerðu ráð fyrir að ADU hafi verið reiknaður sem 23 stykki og eins og sýnt er á fyrri myndinni er aftengdur leiðtími fimm dagar. Með því að nota þessi gildi geturðu reiknað út gula svæðið með því að nota eftirfarandi jöfnu:

- **Gult svæði** = *ADU* ×*Aftengdur leiðtími* = 115

![Dæmi um útreikning á gulu svæði.](media/ddmrp-example-calc-yellow.png "Dæmi um útreikning á gulu svæði")

Rauða svæðisútreikningurinn líkist gula svæðisútreikningnum, en hann er bólstraður fyrir breytileika og leiðtíma. Í þessu dæmi, gerðu ráð fyrir að þú hafir séð miðlungs afgreiðslutíma (stuðull = 0,50) og mikla eftirspurnarbreytileika (stuðull = 0,8). Með því að nota þessi gildi ásamt hlutunum úr gula svæðisjöfnunni er hægt að reikna út rauða svæðið með því að nota eftirfarandi jöfnur:

- **Rauður grunnur** = *ADU* ×*Aftengdur leiðtími* ×*Leiðslutími þáttur* = 57,5
- **Rautt öryggi** = *Rauður grunnur* ×*Breytileikastuðull* = 46
- **Rautt svæði** = *Rauður grunnur* + *Rautt öryggi* = 103,5

Kerfið mun hringlaga rauða svæðið í 104 stykki (ea), vegna þess að stykki eru talin í heilum tölum.

![Dæmi um útreikning á rauðu svæði.](media/ddmrp-example-calc-red.png "Dæmi um útreikning á rauðu svæði")

Græna svæðisútreikningurinn inniheldur einnig íhlutina úr gula svæðisjöfnunni, en hann gerir ráð fyrir lágmarkspöntunarstærð, pöntunarlotu og afgreiðslutímastuðli. Í þessu dæmi, gerðu ráð fyrir að það sé engin pöntunarlota (þess vegna hefur þú engar tímatakmarkanir á því hversu oft þú pantar), og lágmarkspöntunarmagn er 10 stykki. Græna svæðið er síðan reiknað út sem hámarksniðurstaða af eftirfarandi þremur jöfnum:

- *Lágmarks magn pöntunar* = 10
- *ADU* ×*Panta hringrás* = 0
- *ADU* ×*Aftengdur leiðtími* ×*Leiðslutími þáttur* = 57,5

Kerfið mun umferð græna svæðið í 58 stykki (ea), því stykki eru talin í heilum tölum.

![Dæmi um rautt grænt útreikning.](media/ddmrp-example-calc-green.png "Dæmi um útreikning á grænu svæði")

Eftirfarandi mynd dregur saman þessar svæðisútreikningsniðurstöður með því að nota trektgrafíkina sem oft er notuð í DDMRP.

![Samantekt á niðurstöðum svæðisreiknings.](media/ddmrp-example-calc-summary.png "Samantekt á niðurstöðum svæðisreiknings")

## <a name="dynamic-adjustments"></a><a name="dynamic-adjustments"></a> Dýnamískar stillingar

Dynamic stillingar gera þér kleift að beita a *eftirspurnarleiðréttingarstuðull* á tímum mikillar eða lítillar eftirspurnar. Þessi þáttur margfaldar ADU í öllum útreikningum fyrir valið tímabil. Stuðpúðasvæðum er síðan breytt í röð. Þú notar venjulega þennan þátt eftir að þú hefur búið til upphafleg biðminni, svo þú getir fínstillt þau með tímanum og til að bregðast við breyttum aðstæðum. Þetta verkefni er þriðja skref DDMRP.

Til dæmis gæti verið meiri eftirspurn eftir koddavöru í ágúst þegar fólk fer í frí. Því er búist við að salan verði meiri. Í þessu tilviki geturðu breytt **Eftirspurnarleiðréttingarstuðull** gildi fyrir vöruna til *1.5* fyrir allar vikurnar í ágúst.

Þannig er hægt að reikna út biðminni með tímanum og stilla þau svo út frá fleiru en þeim upplýsingum sem kerfið hefur. Í fullri DDMRP útfærslu muntu reikna út ný biðminnigildi á hverjum degi í gegnum runuvinnu og samþykkja sjálfkrafa gildin. Þú munt síðan keyra áætlanagerð sem runuvinnu og fara yfir fyrirhugaðar pantanir á hverjum degi til að fylla á biðminni.

## <a name="implement-buffers-in-supply-chain-management"></a>Innleiða biðminni í Supply Chain Management

Þessi hluti lýsir því hvernig á að innleiða biðminnisstefnu þína í Microsoft Dynamics 365 Supply Chain Management. Það gerir ráð fyrir að þú hafir þegar gert greiningar og útreikninga sem lýst er í fyrri hluta þessarar greinar.

### <a name="set-up-buffers-for-a-decoupling-point-item"></a><a name="set-up-buffers"></a> Settu upp biðminni fyrir hlut aftengingarpunkts

Fylgdu þessum skrefum til að setja upp biðminnigildi fyrir aftengingarpunkt.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veldu útgefinn hlut sem er settur upp sem aftengingarpunktur. (Nánari upplýsingar er að finna í [Staðsetning birgða](ddmrp-inventory-positioning.md) .)
1. Á aðgerðarrúðunni, á **Áætlun** flipa, veldu **Vöruumfjöllun**.
1. Á **Vöruumfjöllun** síðu, veldu vöruþekjuskrá sem býr til aftengingarpunkt. (Þessi skrá mun sýna nafn umfjöllunarhóps sem er settur upp til að búa til aftengingarpunkta.)
1. Veldu flipann **Almennt**.
1. Ef þú vilt að kerfið endurreikna biðminni á hverjum degi eða í hverri viku, byggt á sölusögu þinni, spám og stillingum þekjuhóps skaltu fylgja þessum skrefum:

    1. Sett **Buffer gildi með tímanum** valmöguleika til *Já*.
    1. Skilaboðabox lætur þig vita að handvirkar biðminni stillingar (**Lágmark**, **punkt**, og **Hámark**) verður endurstillt ef þú heldur áfram. Veldu **Já** að halda nýju stillingunni.

    Að öðrum kosti, ef þú vilt frekar reikna út eða slá inn biðminni stillingar þínar bara einu sinni, fylgdu þessum skrefum:

    1. Sett **Buffer gildi með tímanum** valmöguleika til *Nei*.
    1. Stilltu **Lágmark**, **punkt**, og **Hámark** reiti til biðminnigildanna sem þú hefur reiknað út fyrir hlutinn, eins og lýst er fyrr í þessari grein.

1. Stilltu eftirfarandi reiti til að klára að setja upp DDMRP útreikninga fyrir vöruna:

    - **Panta hringrás** – Tilgreindu fjölda daga sem líða þarf á milli innkaupapantana fyrir vöruna. Stilltu gildið á *0* (núll) ef engar pöntunartakmarkanir eru fyrir hendi. Þessi reitur hefur áhrif á hámarksmagn biðminni, eins og áður hefur verið fjallað um í þessari grein.
    - **Dagleg meðalnotkun** – Þú getur valið að slá inn áætlað ADU fyrir hlutinn. Þetta svæði er eingöngu ætlað til upplýsinga. Venjulega er gildið sjálfkrafa reiknað sem hluti af biðminniútreikningum.
    - **Pöntunarhámarksþröskuldur** – Tilgreindu lágmarksfjölda daglegra sölu á vörunni sem flokkast sem söluauki (óvenju mikil eftirspurn). Kerfið notar þennan reit til að auka endurpöntunarmagn fyrirhugaðra pantana á tímabilum með mikilli eftirspurn. Fyrir frekari upplýsingar, sjá [Eftirspurnarstýrð áætlanagerð](ddmrp-planning.md).

### <a name="calculate-or-enter-decoupled-lead-times"></a><a name="calc-lead-time"></a> Reiknaðu eða sláðu inn aftengdan afgreiðslutíma

Fyrir hluti þar sem þú velur að leyfa kerfinu að [reiknaðu biðminni þín sjálfkrafa](#set-up-buffers), fylgdu þessum skrefum til að reikna út eða slá inn aftengdan leiðtíma fyrir aftengingarpunktsvöru.

1. Opnaðu **Vöruumfjöllun** síðu fyrir aftengingarpunktinn þinn. (Nánari upplýsingar er að finna í [Settu upp biðminni fyrir hlut aftengingarpunkts](#set-up-buffers) .)
1. Veldu vöruþekjuskrá sem býr til aftengingarpunkt.
1. Veldu **Buffer gildi** flipa.
1. Ef engin tímabil eru sýnd í hnitanetinu, á aðgerðarrúðunni, á **Buffer gildi** flipa, veldu **Bættu við tímabilum**. Kerfið fyllir ristina af línum fyrir hvert daglegt eða vikulegt tímabil, allt eftir því hvort **Lágm., hámark og endurpöntunarpunktatímabil** sviði fyrir [umfjöllunarhópur](ddmrp-inventory-positioning.md) er stillt á *Daglega* eða *Vikulega*. Kerfið mun bæta við nógu mörgum línum til að ná tímagirðingunni sem er tilgreind fyrir þekjuhópinn sem er úthlutað til vörunnar.
1. Veldu tímabilið þar sem þú vilt reikna aftengdan leiðtíma. (Venjulega er þetta tímabil tímabilið sem inniheldur dagsetninguna í dag.)
1. Á aðgerðarrúðunni, á **Buffer gildi** flipa, veldu **Reiknaðu aftengdan leiðtíma**.
1. Í **Reiknaðu aftengdan leiðtíma** valmynd, stilltu eftirfarandi reiti:

    - **BOM** – Veldu efnisskrána (BOM) sem þú vilt keyra útreikninginn á.
    - **Dagsetning** – Veldu dagsetninguna sem þú vilt keyra útreikninginn á. Safnið af tiltækum uppskriftum verður síað þannig að aðeins uppskriftir sem eru virkar fyrir valda dagsetningu eru sýndar.
    - **Magn** – Sláðu inn magnið sem þú vilt keyra útreikninginn fyrir. Safnið af tiltækum uppskriftum verður síað þannig að aðeins birtast uppskriftir sem eiga við tilgreint magn.

1. Veldu **Allt í lagi** til að keyra útreikninginn og loka **Reiknaðu aftengdan leiðtíma** valmynd. The **Aftengdur leiðtími** dálkurinn fyrir valið tímabil sýnir nú reiknað gildi.

### <a name="calculate-or-enter-average-daily-usage"></a><a name="calc-adu"></a> Reiknaðu eða sláðu inn meðaltal daglegrar notkunar

Fyrir hluti þar sem þú velur að leyfa kerfinu að [reiknaðu biðminni þín sjálfkrafa](#set-up-buffers), fylgdu þessum skrefum til að reikna út eða slá inn ADU fyrir aftengingarpunktsvöru.

1. Opnaðu **Vöruumfjöllun** síðu fyrir aftengingarpunktinn þinn. (Nánari upplýsingar er að finna í [Settu upp biðminni fyrir hlut aftengingarpunkts](#set-up-buffers) .)
1. Veldu vöruþekjuskrá sem býr til aftengingarpunkt.
1. Veldu **Buffer gildi** flipa.
1. Ef engin tímabil eru sýnd í hnitanetinu, á aðgerðarrúðunni, á **Buffer gildi** flipa, veldu **Bættu við tímabilum**. Kerfið fyllir ristina af línum fyrir hvert daglegt eða vikulegt tímabil, allt eftir því hvort **Lágm., hámark og endurpöntunarpunktatímabil** sviði fyrir [umfjöllunarhópur](ddmrp-inventory-positioning.md) er stillt á *Daglega* eða *Vikulega*. Að auki eru sjálfgefin gildi fyrir **Leiðslutími þáttur** og **Breytileikastuðull** reitir eru teknir úr umfjöllunarhópnum. Þú getur breytt þessum gildum fyrir hverja línu eftir þörfum.
1. Veldu tímabil þar sem þú vilt reikna út ADU.
1. Á aðgerðarrúðunni, á **Buffer gildi** flipa, veldu **Reiknaðu meðaltal daglegrar notkunar**. Kerfið reynir að safna gögnum sem eru nauðsynleg fyrir ADU útreikninginn, eins og skilgreint er fyrir [umfjöllunarhópur](ddmrp-inventory-positioning.md).
1. Fylgið einu af eftirfarandi skrefum:

    - Ef nauðsynleg gögn eru tiltæk, er útreikningsniðurstöðum bætt við **Dagleg meðalnotkun** dálki. Í þessu tilviki er ekki þörf á neinum aðgerðum.
    - Ef nauðsynleg gögn eru ekki tiltæk er engum gildum sjálfkrafa bætt við. Í þessu tilviki skaltu slá inn áætluð gildi handvirkt fyrir hverja línu þar sem þú ætlar að reikna út biðminni.

### <a name="calculate-and-apply-buffer-values"></a>Reiknaðu og notaðu biðminni gildi

Fyrir hluti þar sem þú velur að leyfa kerfinu að [reiknaðu biðminni þín sjálfkrafa](#set-up-buffers), þú getur kveikt handvirkt á útreikningi biðminnigilda með því að fylgja þessum skrefum.

1. Fyrir viðkomandi lið aftengingarpunkts, [stilla biðminni útreikninginn](#set-up-buffers),[reikna út eða slá inn aftengdan afgreiðslutíma](#calc-lead-time), og [reikna eða slá inn meðaltal daglegrar notkunar](#calc-adu) fyrir öll viðeigandi tímabil, eins og áður hefur verið lýst í þessari grein.
1. Opnaðu **Vöruumfjöllun** síðu fyrir aftengingarpunktinn þinn.
1. Veldu **Buffer gildi** flipa, sem ætti nú þegar að sýna lista yfir tímabil.
1. Veldu tímabilið þar sem þú vilt reikna biðminni gildi. (Venjulega mun þetta tímabil vera tímabilið sem nær til dagsins í dag.) Línan sem þú velur verður nú þegar að hafa gildi sem eru ekki núll í **Dagleg meðalnotkun** og **Aftengdur leiðtími** dálkum.
1. Breyttu **Eftirspurnarleiðréttingarstuðull** reit fyrir eina eða fleiri línur eftir þörfum. Kerfið mun beita þessum þætti á **Dagleg meðalnotkun** gildi í öllum biðminniútreikningum þar sem það gildi er notað. Þessi þáttur gerir þér kleift að stilla eftir því hvernig eftirspurn sveiflast eftir dagsetningu (til dæmis fyrir hátíðir eða árstíðabundnar vörur).
1. Á aðgerðarrúðunni, á **Buffer gildi** flipa, veldu **Reiknaðu lágmarks-, hámarks- og endurraða punktamagn**. Kerfið reiknar út og fyllir út **Reiknuð mín**, **endurpöntunarpunktur**, og **Reiknað max** dálkar í ristinni á **Vöruumfjöllun** síðu.
1. Þegar þú hefur lokið við að skoða útreiknuð gildi verður þú að nota þau. Annars hafa þær engin áhrif. Þegar þú notar útreikning fyrir eina eða fleiri línur, gildi frá **Reiknuð mín**, **endurröðun**, og **Reiknað max** reitirnir eru afritaðir í **Min**, **punkt**, og **Hámark** dálkum, í sömu röð. Á aðgerðarrúðunni, á **Buffer gildi** flipa, í **Grípa til aðgerða** hóp, veldu einn af eftirfarandi hnöppum:

    - **Samþykkja alla útreikninga** – Notaðu öll reiknuð gildi í ristinni.
    - **Samþykkja útreikninga fyrir valdar línur** – Notaðu útreiknuð gildi eingöngu fyrir valdar línur.
    - **Henda öllum útreikningum** – Fleygðu öllum reiknuðum gildum fyrir lágmarksmagn, hámarksmagn og endurröðunarpunkta í ristinni.
    - **Fleygðu útreikningum fyrir valdar línur** – Fleygðu öllum reiknuðum gildum fyrir lágmarksmagn, hámarksmagn og endurraða punkta fyrir valdar línur.

### <a name="schedule-automatic-buffer-value-calculations"></a>Tímasettu sjálfvirka útreikninga á biðminni

Eftir að þú hefur stillt upp DDMRP stillingarnar þínar að fullu og staðfest að þær virki eins og búist var við, muntu líklega vilja setja upp runuvinnu til að endurreikna ADU og tengd biðminni gildi reglulega eftir þörfum, byggt á raunverulegum neyslugögnum og/eða uppfærðum spám. Þessi aðferð á aðeins við um hluti þar sem þú velur að leyfa kerfinu að gera það [reikna sjálfkrafa biðminni svæði](#set-up-buffers).

Fylgdu þessum skrefum til að skipuleggja sjálfvirka útreikninga á biðminni.

1. Fara til **Aðalskipulag \> Aðalskipulag \> DDMRP \> Reiknaðu biðminni gildi**.
1. Í **Reiknaðu biðminni gildi** valmynd, stilltu eftirfarandi reiti:

    - **Reiknaðu meðaltal daglegrar notkunar** – Stilltu þennan valkost á *Já* að endurreikna ADU aftengingarpunkta í hvert sinn sem verkið keyrir. Stilltu það á *Nei* að sleppa þessum útreikningi. Venjulega ættir þú að stilla þennan valkost á *Já*.
    - **Reiknaðu aftengdan leiðtíma** – Stilltu þennan valkost á *Já* að endurreikna aftengda afgreiðslutíma í hvert sinn sem verkið keyrir. Stilltu það á *Nei* að sleppa þessum útreikningi. Venjulega ættir þú að stilla þennan valkost á *Já*.
    - **Reiknaðu biðminni gildi** – Stilltu þennan valkost á *Já* til að endurreikna biðminni gildi í hvert sinn sem verkið keyrir. Stilltu það á *Nei* að sleppa þessum útreikningi. Venjulega ættir þú að stilla þennan valkost á *Já*.
    - **Samþykkja útreikning fyrir lágmark, max og endurpöntunarpunkt** – Stilltu þennan valkost á *Já* til að samþykkja og beita endurreiknuðu biðminnigildunum sjálfkrafa í hvert sinn sem verkið keyrir. Stilltu það á *Nei* að láta endurreiknuð gildi óbeitt. Í þessu tilviki munu endurreiknuðu gildin ekki taka gildi nema einhver noti þau handvirkt síðar úr hverri vöru **Vöruumfjöllun** síðu. Venjulega ættir þú að stilla þennan valkost á *Já*.
    - **Snilldaráætlun** – Veldu aðalskipulag sem inniheldur þá hluti sem verða fyrir áhrifum af útreikningnum. Útreikningurinn mun eiga við um alla hluti í áætlunarsíunni, sem takmarkast enn frekar af **Sía** stillingar í þessum glugga.

1. Til að takmarka safnið af færslum sem þetta runuverk ætti að keyra á, á **Skrár til að hafa með** Flýtiflipi, veldu **Sía** að opna **Fyrirspurn** valmynd. Þessi gluggi virkar alveg eins og hann gerir fyrir aðrar gerðir af [bakgrunnsstörf](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í birgðakeðjustjórnun.
1. Á **Hlaupa í bakgrunni** Flýtiflipi, tilgreinið hvernig, hvenær og hversu oft skal gera valda útreikninga fyrir valda atriði. Reitirnir virka eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.
1. Veldu **Allt í lagi** til að bæta nýja verkinu við hópröð fyrir framkvæmd.

### <a name="review-and-recalculate-decoupled-lead-times-for-all-items"></a>Skoðaðu og endurreiknaðu aftengdan afgreiðslutíma fyrir alla hluti

Fylgdu þessum skrefum til að fara yfir og endurreikna alla aftengda afgreiðslutíma sem eru í boði hjá lögaðilanum þínum (fyrirtæki).

1. Fara til **Aðalskipulag \> Aðalskipulag \> DDMRP \> Aftengdur leiðtími**.
1. Á **Aftengdur leiðtími** síðu, flettu og síaðu listann eftir þörfum til að finna upplýsingarnar sem þú ert að leita að. Til að skoða enn frekari upplýsingar um hlut skaltu velja tengil þess í **Vörunúmer** dálki.
1. Ef þú vilt endurreikna aftengdan afgreiðslutíma fyrir einhverja vöru skaltu velja vöruna og síðan velja **Reiknaðu aftengdan leiðtíma** á aðgerðasvæðinu. The **Reiknaðu aftengdan leiðtíma** svarglugginn birtist. Þessi valmynd virkar alveg eins og þegar þú ert [reikna út ótengdan leiðtíma](#calc-lead-time) fyrir sama hlut á **Vöruumfjöllun** síðu.
