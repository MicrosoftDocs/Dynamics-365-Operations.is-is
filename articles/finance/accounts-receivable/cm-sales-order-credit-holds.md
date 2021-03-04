---
title: Lán í biðstöðu fyrir sölupantanir
description: Þetta efni lýsir uppsetningu reglna sem notaðar eru til að setja sölupöntun í kreditbið.
author: mikefalkner
manager: AnnBe
ms.date: 01/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 102ea4285407a4f4985cc8dd46ebc1ad21fc6f67
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444253"
---
# <a name="credit-holds-for-sales-orders"></a>Lán í biðstöðu fyrir sölupantanir
[!include [banner](../includes/banner.md)]

Þetta efni lýsir uppsetningu reglna sem notaðar eru til að setja sölupöntun í kreditbið. Reglur um útilokun á lánamálum geta átt við um einstaka viðskiptavini eða hóp viðskiptavina. Reglur um útilokun skilgreina svör við eftirfarandi kringumstæðum:

1. Fjöldi vanskiladaga
2. Bókhaldsstaða
3. Greiðsluskilmálar
4. Lánamark er útrunnið
5. Upphæð í vanskilum
6. Upphæð sölupöntunar
7. Hluti tiltækra lána notaður

Að auki eru tvær breytur sem stjórna viðbótar atburðarásum sem loka fyrir sölupöntun

1. Breyting á greiðsluskilmálum
2. Breyting á uppgjörsafslætti

## <a name="set-up-blocking-rules-and-exclusion-rules"></a>Settu upp hindrunarreglur og útilokunarreglur

Þegar viðskiptavinur hefst söluviðskipti eru upplýsingarnar um sölupöntunina skoðaðar á móti settum hindrunarreglum sem leiðbeina ákvörðun um hvort veita skuli lánstraust til viðskiptavinarins eða ekki og leyfa sölunni að halda áfram. Þú getur einnig skilgreint útilokanir sem munu hnekkja reglum um hindrun og leyfa vinnslu á sölupöntun. Þú getur sett upp hindrunarreglur og útilokunarreglur á síðunni **Lánastjórnun > Uppsetning > Uppsetning lánaumsýslu > Lokunarreglur**.

### <a name="days-overdue"></a>Dagar í vanskilum

Opnaðu flipann **Vanskiladagar** ef hindrunarreglan gildir um viðskiptavini með einn eða fleiri reikninga sem hafa verið í vanskilum í tiltekinn fjölda daga.
1. Veldu það svið viðskiptavina sem þessi regla er **Gildir fyrir**.
   - Veldu **Tafla** ef reglan gildir um tiltekinn viðskiptavin.
   - Veldu **Hópur** ef reglunni er beitt á vettvangi viðskiptavinahóps. 
   - Veldu **Allt** ef reglan á við alla viðskiptavini.
2. Þegar þú hefur tilgreint sviðið verður þú að tilgreina **Lykil/hópur** sem verður notað á sviðinu.
   - Fyrir sviðið **Tafla** mun uppflettingin bjóða upp á lista yfir viðskiptavini sem þú getur valið. 
   - Veldu **Hópur** ef reglan gildir um lánshóp viðskiptavina.
   - Veldu **Allt** ef reglan á við alla viðskiptavini. 
3. Veldu **Áhættuhóp** til að nota viðmið til að beita lánsfjárstýringu á viðskiptavini sem eru flokkaðir eftir sameiginlegum þáttum, svo sem lánshæfiseinkunn Dun og Bradstreet, fjölda ára sem þeir hafa verið í viðskiptum, þann tíma sem þeir hafa verið viðskiptavinur og svo framvegis.  
4. Velja gerð reglunnar sem verið er að setja upp. Valkosturinn **Lokun** mun búa til reglu sem lokar fyrir pöntun. Valkostur **Útilokun** mun búa til reglu sem útilokar aðra reglu frá að loka fyrir pöntun. 
5. Veljið **Gerð gildis**. Sjálfgefna færslan er fastur fjöldi daga. Ef þú ert að búa til útilokun geturðu tilgreint fastan fjölda daga eða upphæð í staðinn. 
6. Sláðu inn fjölda daga **Í vanskilum** sem verður leyft fyrir valda útilokunarreglu áður en pöntun er sett á lánstrauststjórn til endurskoðunar. Fjöldi vanskiladaga táknar viðbótarfjölda biðdaga sem bætast við fjölda daga umfram gjalddaga greiðslu sem reikningurinn getur haft áður en hann er talinn í vanskilum. Ef þú tilgreindir **Gildisgerð** sem upphæð fyrir útilokun, sláðu síðan inn fjárhæð og gjaldmiðil fyrir þá upphæð.

### <a name="accounts-status"></a>Bókhaldsstaða

Opnaðu flipann **Staða reiknings** ef hindrunarreglan á við um viðskiptavin með valinn stöðu reikningsins.
1. Velja gerð reglunnar sem verið er að setja upp.  **Lokun** mun búa til reglu sem lokar fyrir pöntun. **Útilokun** stofnar reglu sem útilokar reglu frá að loka fyrir pöntun. 
2. Veldu **Staða reiknings** sem mun valda því að reglan setur sölupöntun í bið eða útilokar það.

### <a name="terms-of-payment"></a>Greiðsluskilmálar

Veldu **Greiðsluskilmálar** ef hindrunarreglan gildir um valda greiðsluskilmála.
1. Velja gerð reglunnar sem verið er að setja upp.  **Lokun** mun búa til reglu sem lokar fyrir pöntun. **Útilokun** stofnar reglu sem útilokar reglu frá að loka fyrir pöntun. 
2. Veldu **Greiðsluskilmálar** sem mun valda því að reglan setur sölupöntun í bið eða útilokar það.

### <a name="credit-limit-expired"></a>Lánamark er útrunnið

Opnaðu flipann **Útlánamörkin runnu út** ef hindrunarreglan á við um viðskiptavini með lánamörk sem eru útrunnin.
1. Veldu það svið viðskiptavina sem þessi regla er **Gildir fyrir**.
   - Veldu **Tafla** ef reglan gildir um tiltekinn viðskiptavin.
   - Veldu **Hópur** ef reglunni er beitt á vettvangi viðskiptavinahóps. 
   - Veldu **Allt** ef reglan á við alla viðskiptavini.
2. Þegar þú hefur tilgreint sviðið verður þú að tilgreina **Lykil/hópur** sem verður notað á sviðinu.
   - Fyrir sviðið **Tafla** mun uppflettingin bjóða upp á lista yfir viðskiptavini til að velja af. 
   - Veldu **Hópur** ef reglan gildir um kreditstjórnunarhóp viðskiptavina.
   - Veldu **Allt** ef reglan á við alla viðskiptavini. 
3. Veldu **Áhættuhóp** til að takmarka enn frekar lista yfir viðskiptavini sem settir verða í kreditstjórnunarbið. 
4. Velja gerð reglunnar sem verið er að setja upp. 
   - Veldu **Lokun** til að stofna reglu sem lokar fyrir pöntun. 
   - Veldu **Útilokun** til að stofna reglu sem útilokar aðra reglu frá að loka fyrir pöntun. 
5. Sláðu inn **Útlánaviðmiðunardagur rann út** fyrir valda útilokunarreglu áður en pöntun er sett í bið lánastjórnunar. Fjöldi vanskiladaga táknar viðbótar biðdaga sem er bætt við þann fjölda daga sem lánsfjárhámarkið er útrunnið.

### <a name="overdue-amount"></a>Upphæð í vanskilum

Opnaðu flipann **Vanskilaupphæð** ef hindrunarreglan á við um viðskiptavini með vanskilaupphæðir.
1. Veldu það svið viðskiptavina sem þessi regla er **Gildir fyrir**.
   - Veldu **Tafla** ef reglan gildir um tiltekinn viðskiptavin.
   - Veldu **Hópur** ef reglunni er beitt á vettvangi viðskiptavinahóps. 
   - Veldu **Allt** ef reglan á við alla viðskiptavini.
2. Þegar þú hefur tilgreint sviðið verður þú að tilgreina **Lykil/hópur** sem verður notað á sviðinu.
   - Fyrir sviðið **Tafla** mun uppflettingin bjóða upp á uppflettingu á viðskiptavinum. 
   - Veldu **Hópur** ef reglan gildir um kreditstjórnunarhóp viðskiptavina.
   - Veldu **Allt** ef reglan á við alla viðskiptavini. 
3. Veldu **Áhættuhóp** ef þú vilt takmarka enn frekar lista yfir viðskiptavini sem fara í kreditstjórnunarbið. 
4. Velja gerð reglunnar sem verið er að setja upp. 
   - Veldu **Lokun** til að stofna reglu sem lokar fyrir pöntun. 
   - Veldu **Útilokun** til að stofna reglu sem útilokar aðra reglu frá að loka fyrir pöntun. 
5. Sláðu inn **Vanskilaupphæð** fyrir valda útilokunarreglu áður en pöntun er sett í bið lánastjórnunar til endurskoðunar. 
6. Veldu **Gildisgerð** sem skilgreinir þá tegund verðmæta sem verður notuð til að prófa einnig hversu mikið af lánamörkum hefur verið notað. Lokunarreglur krefjast prósentu en útilokun getur verið með fasta fjárhæð eða prósentu. Þröskuldurinn tengist lánamörkum.
7. Sláðu inn gildið fyrir **Viðmiðunarmörk lána** fyrir valda reglu áður en viðskiptavinur heldur úti lánstrausti. Þetta getur verið upphæð eða prósentutala byggð á gildistegundinni sem valin er í gildistegundinni.
8. Reglan athugar að farið hafi verið fram yfir **Vanskilaupphæð** og **Viðmiðunarmörk lána**. 

### <a name="sales-order"></a>Sölupöntun 

Veldu **Sölupöntun** ef hindrunarreglan á við um verðmæti sölupöntunarinnar.
1. Veldu það svið viðskiptavina sem þessi regla er **Gildir fyrir**.
   - Veldu **Tafla** ef reglan gildir um tiltekinn viðskiptavin.
   - Veldu **Hópur** ef reglunni er beitt á vettvangi viðskiptavinahóps. 
   - Veldu **Allt** ef reglan á við alla viðskiptavini.
2. Þegar þú hefur tilgreint sviðið verður þú að tilgreina **Lykil/hópur** sem verður notað á sviðinu.
   - Fyrir sviðið **Tafla** mun uppflettingin bjóða upp á uppflettingu á viðskiptavinum. 
   - Veldu **Hópur** ef reglan gildir um kreditstjórnunarhóp viðskiptavina.
   - Veldu **Allt** ef reglan á við alla viðskiptavini. 
3. Veldu **Áhættuhóp** ef þú vilt takmarka enn frekar lista yfir viðskiptavini sem fara í kreditstjórnunarbið. 
4. Velja gerð reglunnar sem verið er að setja upp.  
   - Veldu **Lokun** til að stofna reglu sem lokar fyrir pöntun. 
   - Veldu **Útilokun** til að stofna reglu sem útilokar aðra reglu frá að loka fyrir pöntun. 
5. Sláðu inn **Sölupöntunarupphæð** fyrir valda útilokunarreglu áður en pöntun er sett í bið lánastjórnunar. 

Reglan um sölupöntun felur í sér viðbótarstillingu sem gengur framhjá öllum öðrum reglum. Til að búa til útilokun sem sleppir sölupöntuninni án þess að taka gildi aðrar reglur, veldu gátreitinn **Losa sölupöntun** á útilokunarlínu.

### <a name="credit-limit-used"></a>Lánamark notað

Veldu **Útlánamörk notuð** ef hindrunarreglan gildir um lánsfjárhæð viðskiptavinanna sem notuð er.
1. Veldu það svið viðskiptavina sem þessi regla er **Gildir fyrir**.
   - Veldu **Tafla** ef reglan gildir um tiltekinn viðskiptavin.
   - Veldu **Hópur** ef reglunni er beitt á vettvangi viðskiptavinahóps. 
   - Veldu **Allt** ef reglan á við alla viðskiptavini.
2. Þegar þú hefur tilgreint sviðið verður þú að tilgreina **Lykil/hópur** sem verður notað á sviðinu.
   - Fyrir sviðið **Tafla** mun uppflettingin bjóða upp á uppflettingu á viðskiptavinum. 
   - Veldu **Hópur** ef reglan gildir um kreditstjórnunarhóp viðskiptavina.
   - Veldu **Allt** ef reglan á við alla viðskiptavini. 
3. Veldu **Áhættuhóp** ef þú vilt takmarka enn frekar lista yfir viðskiptavini sem fara í kreditstjórnunarbið. 
4. Velja gerð reglunnar sem verið er að setja upp.
   - Veldu **Lokun** til að stofna reglu sem lokar fyrir pöntun. 
   - Veldu **Útilokun** til að stofna reglu sem útilokar aðra reglu frá að loka fyrir pöntun. 
5. Veldu **Eftirstandandi þröskuldur** sem skilgreinir hlutfall lánsfjárhámarks sem lokar fyrir sölupöntunina. Ef verðmæti pöntunar eykur lánsfjárhæðina sem notuð er yfir prósentunni verður pöntunin sett í bið. 

## <a name="put-a-sales-order-on-hold-based-on-other-criteria"></a>Settu sölupöntun í bið samkvæmt öðrum forsendum
  
### <a name="rank-payment-terms"></a>Flokka greiðsluskilmála  

Þú getur þvingað útfærslureglurnar þegar greiðsluskilmálum er breytt. Þú verður að raða greiðsluskilmálum og úthluta þeim röðunargildi. Ef þú breytir greiðsluskilmálum pöntunarinnar í greiðsluskilmála sem eru hærri en gömlu greiðsluskilmálarnir, verður pöntunin send til lánastjórnunar og þarfnast samþykkis.

Þú getur sett upp röðun greiðsluskilmála á síðunni **Lánastjórnun > Uppsetning > Uppsetning lánamála > Raða greiðsluskilmálum**.

1. Veldu greiðsluskilmála í reitnum **Greiðsluskilmálar** til að raða; þegar þú velur hugtak birtist lýsingin í reitnum **Lýsing**.
2. Veldu röð hugtaksins í reitnum **Raða**. Gildin eru öll miðað hvert við annað svo að þú getur notað 1,2,3 eða 10,20,30. Þú getur líka notað sama gildi fyrir flesta greiðsluskilmála þannig að aðeins einn eða tveir greiðsluskilmálar koma af stað lánstraustsins.

### <a name="rank-settlement-discounts"></a>Flokka uppgjörsafslætti   

Þú getur þvingað útfærslureglurnar þegar uppgjörsafslætti er breytt. Þú verður að raða uppgjörsafsláttum og úthluta þeim röðunargildi. Ef þú breytir uppgjörsafsláttum pöntunarinnar í uppgjörsafslætti sem eru hærri en gömlu uppgjörsafslættirnr, verður pöntunin send til lánastjórnunar og þarfnast samþykkis.

Þú getur sett upp röðun greiðsluskilmála á síðunni **Lánastjórnun > Uppsetning > Uppsetning lánamála > Raða uppgjörsafsláttum**.

1. Veldu **Staðgreiðsluafsláttinn** sem á að raða. **Lýsing** á uppgjörsafslættinum verður sýnd.
2. Veldu gildið **Raða**. Gildin eru öll miðað hvert við annað svo að þú getur notað 1,2,3 eða 10,20,30. Þú getur líka notað sama gildi fyrir flesta uppgjörsafslætti þannig að aðeins einn eða tveir uppgjörsafslættir kveikja á mati á greiðslugetu.

## <a name="sequence-the-application-of-rules"></a>Fylgdu reglunum beitt

Reglur eru keyrðar í tiltekinni röð sem þú breytir í samræmi við þarfir fyrirtækisins. 

- Eitt dæmi af útilokunarreglum sölupöntunar gerir þér kleift að hnekkja öllum reglum sem gætu hindrað sölupöntun. Búðu til útilokunarreglu fyrir sölupöntun og merktu við valkostinn **Losa sölupöntun**. Pöntunin verður ekki sett í bið ef sú útilokunarregla er sönn og engar aðrar reglur verða skoðaðar.
- Reglur um útilokun geta sett pöntunina í bið.
- Útilokunarreglur eru keyrðar á eftir hindrunarreglum. Útilokunarreglur hafa aðeins áhrif á regluna sem þær eru skilgreindar á. 
- Reglur um lokun og útilokun eru keyrðar í töflu, síðan Hópur, síðan Öll röð. Vegna þessarar vinnsluraðar er mögulegt að hafa hindrunarreglu á öllu stigi sem ekki verður keyrt vegna þess að útilokunarregla á töflu- eða hópastigi er keyrð.
- Útilokanir hnekkja ekki lokunarreglunni ef þær eru á sama stigi. Til dæmis mun útilokunarregla á hópsstigi ekki hnekkja lokunarreglunni á hópsstigi. Þú þarft ekki að setja upp undantekningar á öllu stiginu nema eins og getið er hér að ofan með einu tilvikinu um útilokunarreglu sölupöntunar. 

Hegðun reglunnar **Útlánamörk notuð** mun breytast á grundvelli stillinga fyrir færibreytuna **Athuga lánamörk fyrir sölupöntun** sem er að finna í glugganum Skuldir og innheimta.
- Ef færibreytan er stillt á Nei, þá verður ekki keyrð reglan um lánsfjármagn sem notuð er.
- Ef færibreytan er stillt á Já og **Skilaboð þegar farið er yfir lánamörk** er stillt á viðvörun, þá færðu viðvörun þegar lánsfjárhámarkið er farið yfir. Reglurnar **Útlánamörk notuð** verða keyrðar til að sjá hvort þú ert með reglur sem þú vilt keyra. Hins vegar, fyrir þessa atburðarás, myndirðu venjulega ekki bæta við neinum reglum.
- Ef færibreytan er stillt á Já og **Skilaboð þegar farið er yfir lánamörk** er stillt á villu, þá verður lánamörkin athuguð og pöntunin sett í bið ef farið er yfir lánamörk. Þar að auki verða reglurnar **Útlánamörk notuð** keyrðar til að sjá hvort það eru viðbótarreglur sem á að keyra. Villuboð birtast ekki en lokunarástæðan **Fór yfir lánamörk** verður sýnd. 

## <a name="settings-that-will-change-the-way-an-order-is-placed-on-hold"></a>Stillingar sem munu breyta því hvernig pöntun er sett í bið

Hægt er að útiloka pantanir frá lánamálum jafnvel þó að það séu reglur. 

- Ef þú breytir stillingum **Útiloka viðskiptavini frá lánsfjárstýringu** í **Allir viðskiptavinir > Velja viðskiptavin > Flýtiflipin skulda og innheimtu** í **Já**, þá verða engar pantanir hjá þeim viðskiptavini afgreiddar
- Ef þú breytir gildi **Útiloka frá lánamálum** á **sölupöntunarhaus** á **Flýtiflipi fyrir lánastjórnun** í **Já**, þá verður ekki unnið úr reglum um lánamál. Þessa stillingu er aðeins hægt að gera með lánamálum eða lánastjóra.

## <a name="processing-orders-on-hold-using-the-credit-management-hold-list"></a>Að vinna úr pöntunum í bið með biðlista yfir lánastjórnun

Í biðlista yfir lánamálastjórnun skulum við sjá yfirumsjón með öllum sölupöntunum sem hafa verið settar í bið og láta þá fjarlægja vörurnar þegar dregið hefur verið úr lánamálunum. Síðan **Biðlisti yfir lánastjórnun** sýnir allar sölupantanir sem hafa verið settar í bið. Þú getur skoðað biðlistann á síðunni **Allar kreditbiðir** (**Lánastjórnun > Listi yfir lánaumsýslu > Allar kreditbiðir**).
Sölupantanir frá öllum lögaðilum eru sendar á sama biðlista yfir lánastjórnun, sem gefur miðlæga yfirsýn yfir allar færslur sem þarfnast athygli. Notendur munu aðeins sjá upplýsingar fyrir lögaðila sem þeir hafa aðgang að.

Hægt er að setja sölupöntun á biðlista af eftirfarandi ástæðum:
1. Viðskiptavinurinn er með reikning sem er tímabært í tiltekinn fjölda daga. 
2. Pöntunin hefur sérstaka reikningsstöðu.
3. Pöntunin hefur sérstaka greiðsluskilmála.
4. Viðskiptavinurinn hefur útrunnið lánsheimild.
5. Viðskiptavinurinn er með tímabundna upphæð og hefur notað tiltekið hlutfall af lánamörkum
6. Sölupöntunin er meiri en ákveðin upphæð.
7. Viðskiptavinurinn hefur farið yfir ákveðið hlutfall af lánsheimildum.
8. Greiðsluskilmálar eru frábrugðnir sjálfgefnum greiðsluskilmálum viðskiptavinarins.
9. Uppgjörsafslátturinn er frábrugðinn sjálfgefnum uppgjörsafslætti fyrir viðskiptavininn.

Lokunarástæðan birtist fyrir hverja sölupöntun á biðlistanum. Ef það eru fleiri en ein ástæða fyrir bið, mun ástæðan birtast **Margfeldi**. Þú getur notað valmyndina **Lokunarástæður** í aðgerðarglugganum til að skoða allar ástæður þess að sölupöntunin var sett í bið. Þú getur líka skoðað **Lokunarástæður** í upplýsingareit.

### <a name="releasing-orders-from-the-hold-list-for-processing"></a>Slepptu pöntunum af biðlistanum til vinnslu

Þegar þú hefur kannað ástæður biðstöðvarinnar og dregið úr þeim geturðu sleppt sölupöntunum til frekari vinnslu.

1) Veldu línu í biðlistanum. Þú getur sleppt mörgum pöntunum með því að velja fleiri en eina línu.
2) Veldu **Losunarástæðu** fyrir pöntunina sem hefur verið valin til losunar.  
3) Sláðu inn **Ednurskoðunardagsetningu** fyrir hverja pöntun sem hefur verið valin til losunar.  
4) Veldu valmyndina **Losa** í aðgerðarrúðunni til að gefa út pöntun. Þessi valmynd verður aðeins tiltæk eftir að færslur hafa verið valdar. Notandanum er boðið upp á tvo möguleika:
   - Veldu **Með bókun** til að fjarlægja biðina og bóka skjalið með sama bókunarferli og var notað þegar það var sett í bið. Til dæmis, ef staðfesting sölupöntunar var sett í bið, verður staðfestingu sölupöntunarinnar lokið eftir útgáfuna. Sölupöntunarformið með sölupöntun verður birt þannig að notandinn getur sent staðfestinguna.
   - Veldu **Án bókunar** til að fjarlægja biðina án þess að gera frekari úrvinnslu. Nú er hægt að bóka sölupöntunina handvirkt.

### <a name="rejecting-orders-in-the-hold-list"></a>Hafna pöntunum í biðlistanum
Þú getur notað valmyndina **Hafna** í aðgerðaglugganum til að hafna sölupöntun
1. Veldu línu í biðlistanum. Þú getur sleppt mörgum pöntunum með því að velja fleiri en eina línu.
2. Pöntunin verður fjarlægð af biðlistanum og sölupöntunarhausinn verður uppfærður til að sýna að pöntuninni var hafnað.

### <a name="automatically-releasing-credit-management-holds"></a>Losar sjálfkrafa kreditstjórnunarbið
Sölupantanir eru settar á biðlista byggðar á útilokunarreglunum. Sumar ástæður fyrir bið geta þó breyst með tímanum ef sölupöntunin er á biðlistanum í nokkurn tíma. Til dæmis getur viðskiptavinur greitt reikninginn sinn og losað við lánsheimildina. 

Þú getur notað valmyndina **Metið til losunar** til að fara yfir sölupantanir á biðlista og sleppa þeim sjálfkrafa ef ástæðan fyrir biðinni hefur verið milduð.
1.  Veldu valmyndina **Meta til losunar**
2.  Veldu **Reglur um að hindra ferli** til að fara yfir allar sölupantanir. Veldu **Vinndu útilokunarreglur fyrir valdar línur** til að fara aðeins yfir línurnar sem þú valdir.
3. Renna mun birtast þannig að þú getur valið einn viðskiptavin. Láttu viðskiptavini falla niður fyrir alla viðskiptavini. 
4. Þegar þú smellir á í lagi er ferlið keyrt í bakgrunni og þú getur haldið áfram að vinna að öðrum verkefnum. Ef þú velur runuvinnslu áður en þú smellir á Í lagi mun ferlið keyra í runu þegar þú smellir á Í lagi. Það getur tekið nokkurn tíma að vinna úr pöntunum í bið á listanum svo notaðu Endurnýja til að uppfæra stöðu pantana. 
5.  Ef hindrunarástæða á ekki lengur við um pöntun verður lokunarástæðan talin ekki lengur gild og þú munt ekki lengur sjá gátmerki við hliðina á ástæðunni þegar þú skoðar hindrunarástæðurnar.
6.  Ef allar ástæður fyrir lokun eru hreinsaðar, þá er nýrri ástæðu **Tilbúinn til losunar** bætt við listann yfir hindrunarástæður. Hægt er að losa sölupöntunina sjálfvirkt.
7.  Ef færibreytan **Losa sjálfkrafa** á flipanum **Skuldir og innhheimta > Uppsetning > Færibreytur skulda og innheimtu > Kredit > Sjálfvirk losun** er stilltur á **Með bókun**, þá færðu beiðni um að bóka með bókunarglugganum fyrir skjalið sem var lokað.
8.  Ef færibreytan **Losa sjálfkrafa** á flipanum **Skuldir og innhheimta > Uppsetning > Færibreytur skulda og innheimtu > Kredit > Sjálfvirk losun** er stilltur á **Án bókunar**, þá verður að bóka pöntunina á handvirkan hátt.

### <a name="credit-management-approval-workflow"></a>Vinnuflæði fyrir samþykki lánaumsýslu

Þú getur líka búið til **Verkflæði kreditstjórnunar** til að stjórna losun á kreditbiðum. Þegar þú hefur sett upp verkflæðið með síðunni **Lánastjórnun > Uppsetning > Verkflæði fyrir lánamál** verða pantanir merktar til losunar eða höfnunar sendar í verkflæði þar sem þær verður að samþykkja fyrst áður en þær verða losaðar eða hafnað. 

Ef þú hefur með verk til losunar með bókun eða losun án bókunar í verkflæðinu mun verkflæðissamþykkið einnig einnig losa sölupöntunina. Ef bilun er í losunarferlinu vegna vantar uppsetningarupplýsinga eða annarra orsaka þarftu að muna sölupöntunina frá verkflæðinu, laga málið sem olli biluninni og senda síðan pöntunina til vinnuflæðis aftur.

Ef þú setur verkefnin sem gefin eru út ekki í pósti eða sleppir án þess að setja það inn í verkflæðið þitt mun aðferðin við að samþykkja verkflæðið einfaldlega gera þér kleift að sleppa sölupöntuninni handvirkt þegar samþykki er lokið.

### <a name="forced-credit-hold"></a>Þvinguð kreditbið  
  
Stundum gæti þurft að loka fyrir sölupantanir, jafnvel þó að pöntunin uppfylli ekki skilyrði hindrunarreglnanna. Til dæmis er heimilt að láta lánastjóra vita um vandamál sem ekki eru tengd lánsfé við viðskiptavininn og ákveða að setja pantanir handvirkt strax í bið þar til málið er búið að hreinsa. Þú getur þvingað sölupöntun handvirkt í bið ef þetta ástand kemur upp.

1. Opnaðu sölupöntunina sem þú vilt setja í bið.  
2. Veldu **Þvinga kreditbið** á flipanum **Lánastjórnun** í aðgerðaglugganum **Lánastjórnun**.
3. Veldu **Þvingaða biðástæðu**.
4. Smellið á **Í lagi.** Sölupöntuninni verður skilað á lista kreditstjórnunarbiðar.

Þú getur einnig þvingað margar pantanir til að vera í bið með því að nota **Lánastjórnun > Reglubundin verk > Þvinga kreditbið**. Til dæmis er hægt að setja allar sölupantanir í bið fyrir tiltekinn viðskiptavin.
1. Veldu **Þvingaða biðástæðu**. 
2. Smelltu á **Færslur til að fela í sér** til að velja sölupantanir sem á að setja í bið. 
3. Smelltu á **Í lagi** til að keyra valdar sölupantanir.

Ekki er hægt að vinna með sölupantanir sem hafa verið þvingaðar í bið með vinnuflæði.

#### <a name="releasing-orders-that-were-added-to-the-credit-management-hold-list-with-a-forced-credit-hold"></a>Slepptu pöntunum sem bættust við lánalistastjórnina með neyddri lánsheimild
Ekki er hægt að gefa út sölupantanir sem eru með nauðungarástæður sjálfkrafa. Ef sölupöntuninni var þvingað í bið og þú hefur notað ferli sem sleppir sjálfkrafa sölupöntunum birtist sölupöntunin sem **Tilbúin til losunar** og vera áfram á biðlistanum. Þú verður að nota valmyndina **Losa** til að losa pöntunina.
 
## <a name="free-text-invoices-orders-and-project-invoice-support-in-credit-management"></a>Reikningar með frjálsum texta, pantanir og stuðningur við reikninga vegna verkefna í lánastýringu 
Lánastjórnun er aðeins hægt að nota sem stendur við sölupantanir. Frítextareikningar, sölupunktur sölupantana og pantanir í símaþjónustuverum nota tímabundin lánamörk og tryggingar/ábyrgðir sem þú bætir við til að laga lánsheimildina. Þeir munu ekki nota hindrunarreglurnar og þær verða ekki settar á biðlista ef það er vandamál með lánsfjárhæðina.

Það er enginn stuðningur við reikninga verkefna í lánamálum.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]