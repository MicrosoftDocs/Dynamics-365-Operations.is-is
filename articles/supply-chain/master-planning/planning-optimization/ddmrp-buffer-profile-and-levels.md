---
title: Forstilling öryggisbirgða og gildi
description: Þessi grein veitir upplýsingar um snið öryggisbirgða og svið, sem ákvarða lágmarks- og hámarks birgðastöðu sem ætti að geyma fyrir hvern aftengingarpunkt.
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
ms.openlocfilehash: d254b949d31d0b15141646503c64760062b77fc7
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689147"
---
# <a name="buffer-profile-and-levels"></a>Forstilling öryggisbirgða og gildi

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Þegar þú hefur fundið aftengingarpunktana (mikilvægar vörur sem þú þarft að hafa á lager) verður þú að ákveða hve mikið magn af birgðum (öryggisbirgðum) þú þarft að hafa á hverjum þeirra. Þetta verk er annað skref DDMRP (Demand Driven Materials Resource Planning).

## <a name="buffer-levels-and-zones"></a>Stig og svæði biðminnis

Í DDMRP er hver öryggisbirgðir skilgreindur með því að nota þrjú gildi: lágmarksmagn, hámarksmagn og endurpöntunarmark. Þessi gildi ákvarða þrjú mismunasvæði, sem eru auðkennd með eftirfarandi litakóðum:

- **Rautt svæði** – Svæðið undir lágmarksmagni. Lágmarksmagnið er einnig kallað „efst í rauðu“ og skipulagning þín ætti að vera hönnuð til að tryggja að birgðastaða séu ávallt yfir þessu marki.
- **Gult svæði** – Svæðið á milli lágmarksmagns og endurpöntunarmarks. Endurpöntunarmark er einnig nefndur „efst í gulu“. Þegar þessu stigi er náð ætti kerfið að endurraða.
- **Grænt svæði** – Svæðið á milli endurpöntunarmarks og hámarksmagns. Hámarksmagnið er einnig kallað „efst í grænu“. Þessi punktur er hámarksstigið sem birgðir verður fylltur upp í að nýju.

Eftirfarandi skýringarmynd sýnir lituðu svæðin þrjú og hvernig þau tengjast lágmarksmagni, hámarksmagni og endurpöntunarmarki.

![DDMRP-biðminnissvæði og stig.](media/ddmrp-buffer-levels.png "DDMRP-biðminnissvæði og stig")

## <a name="calculating-the-buffer-zones"></a>Reiknar biðminnisstig

Þessi hluti útskýrir hvernig hæð hvers svæðis öryggisbirgðir er reiknuð.

Gula svæðið er yfirleitt reiknað fyrst. Þetta svæði táknar magnið sem þú notar frá því að þú pantar og þar til pöntunin berst. Með öðrum orðum er það notkunin sem búast má við á afhendingartíma áfyllingar. Það er reiknað út með því að nota eftirfarandi jöfnu:

- **Gula svæðið** = *Meðaltal daglegrar notkunar (ADU)* × *Aftengdur afhendingartími*

*Aftengdur afhendingartími* táknar tímann sem þarf til að framleiða eða taka á móti hlut ef aftengingarpunktar eru alltaf til á lager. Það er yfirleitt mun styttra en *uppsafnaður afhendingartími* sem hefðbundinn er í aðaláætlanagerð. Réttar stillingar öryggisbirgða eru lykilatriði til að tryggja að aftengingarpunktar séu í raun alltaf til á lager en ekki umframbirgðir.

Rautt svæði er reiknað út með því að nota eftirfarandi formúlu:

- **Rauður grunnur** = *ADU* × *Aftengdur afhendingartími* × *Stuðull afhendingartíma*
- **Rautt öryggi** = *Rauður grunnur* x *Breytileikaþáttur*
- **Rautt svæði** = *Rauður grunnur* + *Rautt öryggi*

Græna svæðið er reiknað sem hámarksniðurstaða af eftirfarandi þremur jöfnum:

- *Lágmarksmagn pöntunar*
- *ADU* × *Pöntunarferill*
- *ADU* × *Aftengdur afhendingartími* × *Stuðull afhendingartíma*

## <a name="calculating-average-daily-usage"></a>Útreikningur daglegrar meðaltalsnotkunar

Kerfið notar eina af þremur aðferðum til að reikna út magnið sem þú notar á dag:

- **Meðaltal daglegrar notkunar (fyrri notkun)** – Þessi aðferð er byggð á raunverulegri fyrri neyslu.
- **Dagleg meðalnotkun (framvirk)** – Þessi nálgun er byggð á spá um notkun í framtíðinni.
- **Meðaltal daglegrar notkunar (blönduð)** – Þessi aðferð byggir á veginni blöndu af fyrri og áætlaðri neyslu.

### <a name="average-daily-usage-past"></a>Dagleg meðalnotkun (í fortíðinni)

Fyrri meðaltal daglegrar notkunar er reiknað sem meðaltal með því að bæta við magni sem er notað á hverjum degi í tiltekinn fjölda undangenginna daga og deila síðan heildinni með fjölda daga. Eftirfarandi mynd sýnir hvernig þessi aðferð virkar þegar útreikningurinn er skoðaður þrjá daga aftur í tímann.

![Myndrit yfir meðaltal daglegrar notkunar (í fortíðinni).](media/ddmrp-adu-past.png "Myndrit yfir meðaltal daglegrar notkunar (í fortíðinni)")

Á fyrri skýringarmynd, ef þetta er að morgni 11. júní, er meðaltal daglegrar notkunar síðustu þrjá daga (8., 9. og 10. júní) 21.

- **ADU (fyrra tímabil)** = (29 + 11 + 23) ÷ 3 = 21

Tekið er tillit til eftirfarandi færslna við útreikning á meðaltal daglegrar notkunar (fyrri færslur):

- Færslur sem minnka magn vörunnar (í `inventtrans` töflunni þar sem magn er minna en núll)
- Færslur með stöðu við *Í pöntun*, *Frátekið pantað*, *Frátekið efnislegt magn*, *Tekið til*, *Frádregið* eða *Selt*
- Færslur dagsettar á völdu tímabili aftur á bak (meðaltal daglegrar notkunar á liðnu tímabili)
- Aðrar færslur en vöruhúsavinna, biðgeymsla, sölutilboð eða uppgjör (`WHSWork`, `WHSQuarantine`, `SalesQuotation` eða `Statement`)
- Aðrar færslur en færslubækur sem eru innan sömu þekjuvíddar

### <a name="average-daily-usage-forward"></a>Dagleg meðalnotkun (framvirk)

Ef um nýja vöru er að ræða er ekki víst að eldri notkunargögn séu fyrir hendi. Því gætir þú í staðinn notað áætlaðan meðaltal daglegrar notkunar í framhaldinu (til dæmis miðað við áætlaða eftirspurn). Eftirfarandi mynd sýnir hvernig þessi aðferð virkar þegar útreikningurinn er skoðaður þrjá daga fram í tímann (þar á meðal í dag).

![Myndrit yfir daglega meðalnotkun (framvirk).](media/ddmrp-adu-forward.png "Myndrit yfir daglega meðalnotkun (framvirk)")

Á fyrri myndinni, ef dagurinn í dag er að morgni 11. júní, er meðaltal daglegrar notkunar næstu þrjá daga (11., 12., og 13. júní) 21,66.

- **ADU (framvirkt)** = (18 + 18 + 29) ÷ 3 = 21,66

Tekið er tillit til eftirfarandi færslna við útreikning á meðaltali daglegrar notkunar (framvirkt):

- Spá um færslur fyrir vöruna þar sem spáin er valin á aðaláætlun
- Færslur dagsettar á völdu framtalstímabili (meðaltal daglegrar notkunar framvirka tímabilsins)

### <a name="average-daily-usage-blended"></a>Dagleg meðalnotkun (blönduð notkun)

Blandað meðaltal daglegrar notkunar sameinar meðaltal fyrri notkunar og meðaltal framvirkrar notkunar, eins og sýnt er á eftirfarandi skýringarmynd.

![Myndrit yfir daglega meðalnotkun (blönduð notkun).](media/ddmrp-adu-blended.png "Myndrit yfir daglega meðalnotkun (blönduð notkun)")

Á fyrri skýringarmynd er blandað meðaltal daglegrar notkunar fyrir fyrri þrjá dagana (8. til 13. júní) 21,33 ef dagurinn í dag er að morgni 11. júní.

- **ADU-blandað** = (*ADU afturvirkt* + *ADU framvirkt*) ÷ 2<br>= (21 + 21,66) ÷ 2<br>= 21,33

## <a name="buffer-calculation-factors"></a>Reiknistuðlar biðminnis

Fyrir hverjar vöru er hægt að skilgreina tvo þætti til að stilla hversu stór rauðu og grænu svæðin eiga að vera. Á þennan hátt er hægt að bæta upp fyrir áætlaðan afhendingartíma sem búist er við og krefjast breytileika.

![Afhendingartími og breytileikaþættir.](media/ddmrp-zone-factors.png "Afhendingartími og breytileikaþættir")

Fyrsti þátturinn er *þáttur afhendingartíma*. Gildið er tugagildi frá 0 til 1. Því lengri sem afhendingartími er, því lægra ætti gildið að vera. Eftirspurnardrifið fyrirtæki mælir með eftirfarandi sviðum:

- **Langur afhendingartími:** 0,20–0,40
- **Miðlungs afhendingartími:** 0,41-0,60
- **Stuttur afhendingartími:** 0,61-1,00

Annar þátturinn er *Breytileikastuðullinn*. Gildið er tugagildi frá 0 til 1. Því meiri sem eftirspurnarbreytileikinn er, þeim mun lægra ætti gildið að vera. Eftirspurnardrifið fyrirtæki mælir með eftirfarandi sviðum:

- **Lítill breytileiki:** 0,20-0,40
- **Miðlungs breytileiki:** 0,41-0,60
- **Mikill breytileiki:** 0,61-1,00

## <a name="buffer-calculation-examples"></a>Dæmi um útreikning biðminnis

Þetta dæmi heldur áfram dæmi um framleiðslu kodda sem er gefið upp í [Staðsetning birgða](ddmrp-inventory-positioning.md). Í því dæmi valdir þú aftengingarpunkta sem minnkuðu afhendingartímann úr 21 degi í fimm daga, eins og sýnt er á eftirfarandi skýringarmynd.

![Dæmi um aftengdan afhendingartíma.](media/ddmrp-bom-decoupled-lead-time-example.png "Dæmi um aftengdan afhendingartíma")

Í þessu dæmi gerðu ráð fyrir að meðaltal daglegrar notkunar hafi verið reiknað sem 23 stykki og, eins og sýnt er á fyrri myndinni, er aftengdur afhendingartími fimm dagar. Með því að nota þessi gildi er hægt að reikna gula svæðið með því að nota eftirfarandi jöfnu:

- **Gult svæði** = *ADU* × *Aftengdur afhendingartímie* = 115

![Dæmi um útreikning á gulu svæði.](media/ddmrp-example-calc-yellow.png "Dæmi um útreikning á gulu svæði")

Útreikningur rauða svæðisins líkist útreikningi gula svæðisins, en það er fyllt með breytileika og afhendingartíma. Í þessu dæmi skaltu gera ráð fyrir að þú hafir fylgst með miðlungs afhendingartíma (þáttur = 0,50) og miklum breytileika eftirspurnar (þáttur = 0,8). Með því að nota þessi gildi ásamt íhlutum úr jöfnu gulu svæðis er hægt að reikna rauða svæðið með því að nota eftirfarandi jöfnur:

- **Rauður grunnur** = *ADU* × *Aftengdur afhendingartími* × *Stuðull afhendingartíma* = 57,5
- **Rautt öryggi** = *Rauður grunnur* × *Breytileikaþáttur* = 46
- **Rautt svæði** = *Rauður grunnur* + *Rautt öryggi* = 103,5

Kerfið mun rúnna rauða svæðið í 104 stykki (ea), því stykkin eru talin í heilum tölum.

![Dæmi um útreikning á rauðu svæði.](media/ddmrp-example-calc-red.png "Dæmi um útreikning á rauðu svæði")

Útreikningur græna svæðis felur einnig í sér þætti úr útreikningi gulu svæðis, en hann gerir kleift að reikna lágmarksstærð pöntunar, pöntunarlotu og afhendingartímastuðul. Til dæmis skaltu gera ráð fyrir að það sé engin pöntunarlota (því eru engar tímatakmarkanir á því hversu oft þú pantar) og lágmarks pöntunarmagn er 10 stykki. Græna svæðið er síðan reiknað sem hámarksniðurstaða eftirfarandi þriggja jafna:

- *Lágmarksmagn pöntunar* = 10
- *ADU* × *Pöntunarlota* = 0
- *ADU* × *Aftengdur afhendingartími* × *Stuðull afhendingartíma* = 57,5

Kerfið mun rúnna græna svæðið í 58 stykki (ea), því stykkin eru talin í heilum tölum.

![Dæmi um rauðgrænan útreikning.](media/ddmrp-example-calc-green.png "Dæmi um útreikning á grænu svæði")

Eftirfarandi skýringarmynd tekur saman þessar niðurstöður um útreikning svæðis með því að nota trektargraf sem er oft notaður í DDMRP.

![Samantekt á niðurstöðum svæðisútreiknings.](media/ddmrp-example-calc-summary.png "Samantekt á niðurstöður útreikninga staðs")

## <a name="dynamic-adjustments"></a><a name="dynamic-adjustments"></a>Breytilegar Leiðréttingar

Breytilegar leiðréttingar getur þú notað *leiðréttingarstuðull eftirspurnar* á tímum mikillar eða lítillar eftirspurnar. Þessi þáttur margfaldar ADU í öllum útreikningum fyrir valið tímabil. Öryggisbirgðasvæðum er svo breytt í kjölfarið. Venjulega er þessi þáttur notaður eftir að upphafsgildi öryggisbirgða eru búin til, þannig að hægt sé að fínstilla þau með tímanum og sem viðbrögð við breyttum aðstæðum. Þetta verk er þriðja skrefið DDMRP.

Til dæmis gæti verið meiri eftirspurn eftir koddavörum í ágúst þegar fólk fer í frí. Þar af leiðir er búist við að salan verði meiri. Í þessu tilfelli er hægt að breyta gildinu **Leiðréttingarstuðull eftirspurnar** fyrir vöruna í *1,5* fyrir allar vikurnar í ágúst.

Á þennan hátt er hægt að reikna gildi öryggisbirgða og breyta þeim síðan miðað við fleiri en bara þær upplýsingar sem kerfið hefur. Í fullri DDMRP útfærslu reiknar þú út ný gildi öryggisbirgða á hverjum degi í gegnum runuvinnslu og samþykkir gildin sjálfkrafa. Síðan er áætlunargerð keyrt sem runuvinnsla og farið yfir fyrirhugaðar pantanir á hverjum degi til að fylla á öryggisbirgðir.

## <a name="implement-buffers-in-supply-chain-management"></a>Innleiða öryggisbirgðir í Supply Chain Management

Í þessum kafla er lýst hvernig best er að framkvæma áætlun svæði öryggisbirgða í Microsoft Dynamics 365 Supply Chain Management. Það gerir ráð fyrir að þú hafir þegar gert þær greiningar og útreikninga sem lýst er í fyrri hluta þessarar greinar.

### <a name="set-up-buffers-for-a-decoupling-point-item"></a><a name="set-up-buffers"></a>Setja upp öryggisbirgðir fyrir vöru aftengingarpunkts

Fylgdu þessum skrefum til að setja upp gildi öryggisbirgða fyrir aftengingarpunkt.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veldu losaða vöru sem er sett upp sem aftengingarpunktur. (Frekari upplýsingar eru í [Birgðastaðsetning](ddmrp-inventory-positioning.md)).
1. Á aðgerðasvæðinu, í flipanum **Áætlun** skal velja **Vöruþekja**.
1. Á síðunni **Vöruþekja** skal velja færslu vöruþekju sem býr til aftengingarpunkt. (Þessi færsla mun sýna nafn þekjuflokks sem er settur upp til að búa til aftengingarpunkta).
1. Veldu flipann **Almennt**.
1. Ef þú vilt að kerfið endurreikni gildi öryggisbirgða á hverjum degi eða í hverri viku, byggt á söluferil þinni, spám og stillingum þekjuflokka, skaltu fylgja eftirfarandi skrefum:

    1. Stilltu valkostinn **Gildi öryggisbirgða yfir tíma** á *Já*.
    1. Skilaboðagluggi birtist og tilkynnir um að handvirkar stillingar öryggisbirgða verði endurstilltar ef þú heldur áfram (**Lágmark**, **Endurpöntunarmark** og **Hámark**). Veljið **Já** til að halda nýju stillingunni.

    Ef þú kýst hins vegar að reikna út eða færa inn stillingarnar öryggisbirgða í einu lagi skaltu fylgja þessum leiðbeiningum:

    1. Stilltu valkostinn **Gildi öryggisbirgða yfir tíma** á *Nei*.
    1. Stilltu reitina **Lágmark**, **Endurpöntunarmark** og **Hámark** á gildi öryggisbirgða sem þú hefur reiknað fyrir vöruna, eins og lýst var fyrr í þessari grein.

1. Stilltu eftirfarandi reiti til að ljúka við að setja upp DDMRP útreikninga fyrir vöruna:

    - **Pöntunarlota** – Tilgreinið fjölda daga sem þurfa að líða á milli innkaupapantana á hlutnum. Stilltu gildið á *0* (núll) ef engar takmarkanir eru á pöntun. Þessi reitur hefur áhrif á hámarksmagn öryggisbirgða eins og áður hefur verið fjallað um í þessari grein.
    - **Meðaltal daglegrar notkunar** – Hægt er að færa inn áætlaðan ADU fyrir vöruna. Þetta svæði er eingöngu ætlað til upplýsinga. Vanalega er gildið sjálfkrafa reiknað sem hluti af útreikningi öryggisbirgða.
    - **Mörk mikillar pantanaaukningar** – Tilgreinið lágmarksfjölda daglegra sala á vörunni sem telst vera söluaukning (óvenju mikil eftirspurn). Kerfið notar þennan reit til að endurraða magni áætluðra pantana á tímum mikillar eftirspurnar. Frekari upplýsingar eru í [Áætlanagerð miðað við framboð](ddmrp-planning.md).

### <a name="calculate-or-enter-decoupled-lead-times"></a><a name="calc-lead-time"></a>Reiknaðu eða sláðu inn aftengda afhendingartíma

Fyrir atriði þar sem þú velur að leyfa kerfinu að [reikna út svæði öryggisbirgða sjálfkrafa](#set-up-buffers) skaltu fylgja eftirfarandi skrefum til að reikna eða slá inn aftengda afhendingartíma fyrir vöru aftengingarpunkt.

1. Opnaðu síðuna **Vöruþekja** fyrir aftengingarpunktinn þinn. (Nánari upplýsingar eru í [Setja upp öryggisbirgðir fyrir vöru aftengingarpunkts](#set-up-buffers)).
1. Veljið þekjufærsla vörurá sem býr til aftengingarpunkt.
1. Veljið flipann **Biðminnisgildi**.
1. Ef engin tímabil eru sýnd á hnitanetinu, á aðgerðasvæði, á flipanum **Gildi öryggisbirgða**, skal velja **Bæta við tímabilum**. Kerfið fyllir hnitanetið með línum fyrir hvert daglegt eða vikulegt tímabil, eftir því hvort reiturinn **Lágmark, hámark og endurröðunarmark** fyrir [þekjuflokkinn](ddmrp-inventory-positioning.md) er stilltur á *Daglegt* eða *Vikulega*. Kerfið mun bæta við nógu mörgum línum til að ná tímamörkum sem tilgreind eru fyrir þekjuflokkinn sem úthlutað er til vörunnar.
1. Velja tímabilið þar sem reikna á út aftengda afhendingartíma. (Venjulega er þetta tímabil tímabilið sem inniheldur daginn í dag.)
1. Á aðgerðarsvæðinu, á flipanum **Gildi öryggisbirgða**, skal velja **Reikna aftengdur afhendingartími**.
1. Í svarglugganum **Reikna út aftengdan afhendingartíma** skal stilla eftirfarandi reiti:

    - **Uppskriftir** – Veldu uppskriftina sem þú vilt keyra útreikninginn á.
    - **Dagsetning** – Veldu dagsetninguna sem á að keyra útreikninginn á. Sett tiltækra uppskrifta verður síað þannig að aðeins uppskriftir sem eru virkir fyrir valda dagsetningu verði sýndir.
    - **Magn** – Færðu inn magnið sem á að keyra útreikning fyrir. Sett tiltækra uppskrifta verður síað þannig að aðeins birtist uppskrift sem á við um tilgreint magn.

1. Veldu **Í lagi** til að keyra útreikninginn og lokaðu svarglugganum **Reikna út aftengdan afhendingartíma**. Dálkurinn **Aftengdur afhendingartími** á völdu tímabili sýnir nú útreiknað gildi.

### <a name="calculate-or-enter-average-daily-usage"></a><a name="calc-adu"></a>Reiknaðu eða sláðu inn meðalnotkun á dag

Fyrir atriði þar sem þú velur að leyfa kerfinu að [reikna út svæði öryggisbirgða sjálfkrafa](#set-up-buffers) skaltu fylgja eftirfarandi skrefum til að reikna eða slá inn meðaltal daglegrar notkunar fyrir aftengingarpunkt vöru.

1. Opnaðu síðuna **Vöruþekja** fyrir aftengingarpunktinn þinn. (Nánari upplýsingar eru í [Setja upp öryggisbirgðir fyrir vöru aftengingarpunkts](#set-up-buffers)).
1. Veljið þekjufærsla vörurá sem býr til aftengingarpunkt.
1. Veljið flipann **Biðminnisgildi**.
1. Ef engin tímabil eru sýnd á hnitanetinu, á aðgerðasvæði, á flipanum **Gildi öryggisbirgða**, skal velja **Bæta við tímabilum**. Kerfið fyllir hnitanetið með línum fyrir hvert daglegt eða vikulegt tímabil, eftir því hvort reiturinn **Lágmark, hámark og endurröðunarmark** fyrir [þekjuflokkinn](ddmrp-inventory-positioning.md) er stilltur á *Daglegt* eða *Vikulega*. Að auki eru sjálfgefin gildi fyrir reitina **Afhendingartímastuðull** og **Breytileikastuðull** tekin úr þekjuflokknum. Þú getur breytt þessum gildum fyrir hverja línu eftir þörfum.
1. Velja tímabil þar sem reikna á út ADU.
1. Á aðgerðarsvæðinu, á flipanum **Gildi öryggisbirgða**, skal velja **Reikna meðalnotkun á dag**. Kerfið reynir að safna gögnum sem eru nauðsynleg fyrir útreikning meðaltal daglegrar notkunar, eins og skilgreint er fyrir [þekjuflokkinn](ddmrp-inventory-positioning.md).
1. Fylgið einu af eftirfarandi skrefum:

    - Ef nauðsynleg gögn eru tiltæk er niðurstöðum útreiknings bætt við dálkinn **Meðaltal daglegrar notkunar**. Engra aðgerða er krafist í þessu tilviki.
    - Ef tilskilin gögn eru ekki tiltæk er engum gildum sjálfkrafa bætt við. Í þessu tilviki skaltu slá inn áætluð gildi fyrir hverja línu þar sem þú ætlar að reikna gildi öryggisbirgða.

### <a name="calculate-and-apply-buffer-values"></a>Reikna út og nota biðminnisgildi

Fyrir vörur þar sem þú velur að leyfa kerfinu að [reikna út svæði öryggisbirgða sjálfkrafa](#set-up-buffers), getur þú sett handvirkt af stað útreikning á gildum öryggisbirgða með því að fylgja þessum skrefum.

1. Fyrir viðkomandi vöru aftengingarpunkt [stilltu útreikning öryggisbirgða](#set-up-buffers), [reiknaðu út eða sláðu inn aftengda afhendingartíma](#calc-lead-time) og [reiknaðu út eða sláðu inn meðaltal daglegrar notkunar](#calc-adu) fyrir öll viðeigandi tímabil, eins og áður hefur verið lýst í þessari grein.
1. Opnaðu síðuna **Vöruþekja** fyrir aftengingarpunktinn þinn.
1. Veldu flipann **Gildi öryggisbirgða**, sem ætti þegar að sýna lista yfir tímabil.
1. Veljið tímabilið sem á að reikna öryggisbirgðir fyrir. (Yfirleitt verður þetta tímabil það tímabil sem felur í sér daginn í dag). Röðin sem þú velur verður þegar að hafa gildi sem eru ekki núll í dálkunum **Meðaltal daglegrar notkunar** og dálkanna **Aftengdur afhendingartími**.
1. Breyta reitnum **Leiðréttingarstuðull eftirspurnar** fyrir eina eða fleiri línur eftir þörfum. Kerfið mun beita þessum stuðli á gildi **Meðaltal daglegrar notkunar** í öllum útreikningum öryggisbirgða þar sem það gildi er notað. Þessi stuðull gerir þér kleift að aðlagað þig að því hvernig eftirspurnin sveiflast eftir dagsetningum (til dæmis fyrir frídaga eða árstíðabundnar vörur).
1. Á aðgerðarsvæðinu, á flipanum **Gildi öryggisbirgða**, skal velja **Reikna út magn lágm., hám. og endurpöntunarmarks**. Kerfið reiknar út og fyllir út dálkana **Reiknað lágmark**, **Reiknað endurpöntunarmark** og **Reiknað hámark** í hnitanetinu á síðunni **Vöruþekja**.
1. Þegar þú hefur lokið við að fara yfir reiknuðu gildin verður þú að nota þau. Annars hafa þær engin áhrif. Þegar þú beitir útreikningi fyrir eina eða fleiri línur eru gildi úr dálkunum **Reiknað lágmark**, **Reiknuð endurpöntun** og **Reiknað hámark** afrituð í dálkana **Lágmark**, **Endurpöntunarmark** og **Hámark** í hverju tilviki fyrir sig. Á aðgerðasvæðinu, í flipanum **Gildi öryggisbirgða**, í flokknum **Grípa til aðgerðar**, skal velja einn af eftirfarandi hnöppum:

    - **Samþykkja alla útreikninga** – Nota öll reiknuð gildi í hnitaneti.
    - **Samþykkja útreikninga fyrir valdar línur** – Nota eingöngu reiknuð gildi fyrir valdar línur.
    - **Fleygja öllum útreikningum** – Fleygja öllu reiknuðum gildum fyrir lágmarksmagn, hámarksmagn og endurröðunarmark í hnitanetinu.
    - **Fleygja öllum útreikningum fyrir valdar línur** – Fleygðu öllum reiknuðum gildum fyrir lágmarksmagn, hámarksmagn og endurpöntunarmark fyrir valdar raðir.

### <a name="schedule-automatic-buffer-value-calculations"></a>Áætla sjálfvirka útreikninga gilda öryggisbirgða

Eftir að þú hefur að fullu sett upp DDMRP stillingarnar og staðfest að þær virki eins og til er ætlast, viltu líklega setja upp lotuverk til að endurreikna meðaltal daglegrar notkunar og tengd gildi öryggisbirgða reglulega eftir þörfum, byggt á gögnum um raunverulega notkun og/eða uppfærðum spám. Þessi aðferð á aðeins við um vörur þar sem þú velur að leyfa kerfinu að [reikna sjálfkrafa svæði öryggisbirgða](#set-up-buffers).

Fylgið eftirfarandi skrefum til að tímasetja sjálfvirka útreikninga á öryggisbirgðum.

1. Fara í **Áætlanagerð \> Aðaláætlanagerð \> DDMRP \> Reikna gildi öryggisbirgða**.
1. Í svarglugganum **Reikna gildi öryggisbirgða** skal stilla eftirfarandi reiti:

    - **Reikna meðaltal daglegrar notkunar** – Stillið þennan valkost á *Já* til að endurreikna meðaltal daglegrar notkunar aftengingarpunktur vara í hvert skipti sem verkið er keyrt. Stillið á *Nei* til að sleppa þessum útreikningi. Venjulega á að stilla þennan valkost á *Já*.
    - **Reikna út aftengdan afhendingartíma** – Stillið þennan valkost á *Já* til að endurreikna aftengdan afhendingartíma í hvert sinn sem verkið er keyrt. Stillið á *Nei* til að sleppa þessum útreikningi. Venjulega á að stilla þennan valkost á *Já*.
    - **Reikna gildi öryggisbirgða** – Stillið þennan valkost á *Já* til að endurreikna gildi öryggisbirgða í hvert skipti sem verkið er keyrt. Stillið á *Nei* til að sleppa þessum útreikningi. Venjulega á að stilla þennan valkost á *Já*.
    - **Samþykkja útreikning á lágmarki, hámarki og endurpöntunarmarki** – Stilltu þennan valkost á *Já* til að samþykkja sjálfkrafa og beita endurreiknuðum gildum öryggisbirgða í hvert skipti sem verkið er keyrt. Stilla á *Nei* til að láta endurreiknuð gildi standa ójöfnuð. Í þessu tilviki taka umreiknuðu gildin ekki gildi nema einhver beiti þeim handvirkt síðar á síðu **Vöruþekja** fyrir hverja vöru. Venjulega á að stilla þennan valkost á *Já*.
    - **Aðaláætlun** – Veldu aðaláætlun sem inniheldur vörurnar sem verða fyrir áhrifum af útreikningnum. Útreikningurinn mun gilda um allar vörur áætlunarsíunnar sem stillingarnar **sía** í þessum svarglugga takmarka.

1. Til að takmarka þann fjölda færslna sem þessi runuvinnsla ætti að keyra á skal velja á flýtiflipanum **Færslur til að taka með** valkostinn **Sía** til að opna svargluggann **Fyrirspurn**. Svargluggi virka rétt eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.
1. Á flýtiflipanum **Keyra í bakgrunni** skaltu tilgreina hvernig, hvenær og hversu oft á að reikna valda útreikninga fyrir valdar vörur. Reitirnir virka eins og þeir virka fyrir aðrar gerðir [bakgrunnsvinnsla](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) í Supply Chain Management.
1. Veljið **Í lagi** til að bæta nýja verkinu við runubiðröð fyrir keyrslu.

### <a name="review-and-recalculate-decoupled-lead-times-for-all-items"></a>Yfirfara og endurreikna aftengdan afhendingartíma fyrir allar vörur

Fylgdu þessum skrefum til að yfirfara og endurreikna alla aftengda afhendingartíma sem eru tiltækir hjá lögaðila þínum (fyrirtæki).

1. Fara í **Áætlanagerð \> Aðaláætlanagerð \> DDMRP \> Aftengdur afhendingartími**.
1. Á síðunni **Aftengdur afhendingartími** skaltu fletta og sía listann eftir þörfum til að finna upplýsingarnar sem þú ert að leita að. Til að skoða enn frekari upplýsingar fyrir vöru skal velja tengil hennar í dálknum **Vörunúmer**.
1. Ef þú vilt endurreikna aftengdur afhendingartíma fyrir einhverja vöru skaltu velja vöruna og velja síðan **Reikna út aftengdan afhendingartíma** á aðgerðasvæði. Svarglugginn **Reikna út aftengdan afhendingartíma** opnast. Þessi svargluggi virkar alveg eins og hann gerir þegar [þú reiknar út aftengda afhendingartíma](#calc-lead-time) fyrir sömu vöru á síðunni **Vöruþekja**.
