--- 
title: "Fara yfir innheimtuupplýsingar"
description: "Þetta ferli fer í gegnum hvernig á að fara yfir upplýsingar um innheimtu auk ýmsar uppsetningar valkostir og innheimtu færslur."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: b28d41d5ecf63b22cb84aff0c12a36cb0d728945
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="review-collections-information"></a>Fara yfir innheimtuupplýsingar

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli fer í gegnum hvernig á að fara yfir upplýsingar um innheimtu auk ýmsar uppsetningar valkostir og innheimtu færslur. Þessi aðferð notar sýnigögn USMF fyrirtækisins.


## <a name="create-customer-pools"></a>Stofna viðskiptavinahópa
1. Fara í Skuldir og innheimta > Uppsetning > Hópur viðskiptavina.
    * Notaðu þessa síðu til að Setja upp viðskiptavinaflokka, sem eru fyrirspurnir sem skilgreina flokk af viðskiptavinalykill sem hægt er að birtast og stjórnað fyrir innheimtu eða aldursgreiningu ferli. Nota viðskiptavinahópa til að sía upplýsingar á listasíðu innheimta og tengdar listasíður. Einnig er hægt að nota viðskiptavinahópa til að sía viðskiptavinalykla sem eru teknar með þegar skyndimynd aldurstímabils eru stofnaðar.  
    * Hægt er að nota viðskiptavinahópa til að sía viðskiptavinalykla sem eru teknar með þegar skyndimynd aldurstímabils eru stofnaðar.  
2. Smellið á „Nýtt“.
3. Færa inn gildi í reitnum kenni hóps.
4. Í reitinn Lýsing hóps skal slá inn gildi.
5. Smellt er á velja skilyrði hóps.
6. Í reitinn Skilyrði skal slá inn gildi.
7. Smellið á „Í lagi“.
8. Smellt er á Forskoðun hópur viðskiptavina.

## <a name="create-collections-agents"></a>Stofna innheimtufulltrúa
1. Fara í Skuldir og innheimta > Uppsetning > Innheimtufulltrúar.
    * Notið þessa síðu til að setja upp starfsmenn sem innheimtufulltrúa og úthlutið viðskiptavinahópa þeim. Innheimtufulltrúi með er sá einstaklingur sem vinnur með viðskiptavini til að tryggja að greiðslurnar eru innheimtar í tæka tíð.  
    * Innheimtufulltrúa sem eru settir upp í þessari síðu er sjálfkrafa bætt við innheimtuhópnum. Ef teymi er valinn í svæðinu Hóps á síðunni færibreytur viðskiptakrafna, er  innheimtufulltrúa bætt við þann hóp. Ef hópur er ekki valið, er nýr hópur með heitinu innheimtur er stofna sjálfvirkt og innheimtufulltrúi eru bætt við þann hópur.  
2. Smellið á „Nýtt“.
3. Smelltu á Bæta við.
4. Smellið á „Loka“.
5. Smelltu á Bæta við.
6. Í listanum skal merkja valda línu.
7. Í reitnum kenni hóps skal smella á fellilistahnappinn til að opna leitina.
8. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
9. Veldu eða hreinsaðu gátreitinn sjálfgefinn hópur.
    * Veljið þennan valkost til taka með alla viðskiptavinahópa í síulista fyrir valda innheimtufulltrúi. Ef þessi valkostur er ekki valinn eru aðeins viðskiptavinahópar sem eru úthlutaðar á innheimtufulltrúi tiltækir í síulistum.  

## <a name="create-aging-period-definition"></a>Stofna Skilgreiningar aldurstímabila
1. Fara í Skuldir og innheimta > Uppsetning > Skilgreiningar aldurstímabila.
    * Hægt er að nota skilgreiningu aldurstímabils til að greina binditíma viðskiptavinalykla og lánardrottnalykla á grundvelli dagsetningar sem er færð inn. Hverju aldurstímabili sem settur er upp fyrir skilgreiningu aldurstímabils samsvarar dálki á listasíðunni eða í skjámyndinni eða skýrslunni þegar greining er framkvæmd.  
2. Smellið á „Nýtt“.
3. Í reitnum Skilgreining aldurstímabils skal slá inn gildi.
4. Sláið inn gildi í reitnum „Lýsing“.
    * Tilgreina heiti tímabils, einingu og bil fyrir hverja aldurstímabil til að taka með í skilgreiningu aldurstímabils. Lína sem er með 0 (núll) í svæðinu Eining stendur fyrir dagsetning sem greining er keyrð. Línur fyrir núll munu hafa -1, og línur eftir núll munu hafa 1 sem sjálfgefin lok í svæðinu Eining, en má breyta.  Smella á Upp- og Niðurörvarnar til að endurraða línunum. Ekki er hægt að færa 0 (núll)-ínuna.  
    * Staðsettu bendil þar sem þú vilt setja inn nýja línu og svo Smellið á Bæta við.  
    * Skal velja vísbending til að standa fyrir aldurstímabil í innheimta skjámynd og listasíða. Til dæmis væri að velja grænt vísi fyrir gildandi tímabil, gult vísi fyrir 30 dögum fram tímabil og rautt vísi fyrir 90 daga fram tímabil.  
    * Veljið prentstefnuna fyrir skilgreiningu aldurstímabils. Þetta val ákvarðar röðinni sem dálkarnir birtast á aldursgreindur aldursgreining Viðskiptavina skýrsla eða aldursgreining Lánardrottna skýrsla.  Framvirk – Prenta dálkur í sömu röð og hausar birtast í tafla, byrjað á efstu lína.  Afturvirk – Prenta dálkur í öfugri röð og hausar birtast í tafla, byrjað á lægstu lína.    

## <a name="setup-collections-parameters"></a>Setja upp færibreytur fyrir innheimtu
1. Farið í Skuldir og innheimta > Uppsetning > Færibreytur viðskiptakrafna.
2. Smellt er á flipanum innheimta.
3. Útvíkka eða draga saman hluta sjálfgildi Innheimtu.
    * Skal velja skilgreining aldurstímabils fyrir sjálfgefið aldursgreiningarmynd sem verður notað í skjámynd innheimtu.  
    * Veljið hópur sem innheimtuaðilar eru úthlutað á í skjámyndinni innheimtufulltrúi. Einungis þá hópa sem hafa hópgerð innheimtu birtast á listanum.  
4. Stækka eða fella saman afskriftarhlutann.
    * Veljið færslubókarheitið sem er sett upp fyrir daglega færslubók fjárhags, til að nota þegar færslu er afskrifuð með innheimtuskjámyndinni eða tengdar listasíður.  
    * Veljið sjálfgefinn ástæðukóði, til að nota þegar afskriftarfærsla er stofnað með innheimtuskjámyndinni eða tengdar listasíður.  
    * Veljið þennan valkost til að stofna aðskildar færslubókarlínu fyrir vsk-upphæðir þegar afskriftarfærslur eru stofnaðar með því að nota síðuna Söfn eða tengdar listasíður. Ef þú velur þennan valkostur, geturðu auðveldlega rakið upphæð virðisaukaskatts sem koma við sögu í afskriftafærsla. Hægt er að rekja upphæðir virðisaukaskatts sérstaklega til að auðvelda þér að leiðrétta VSK-skuld þína fyrir viðkomandi tímabil.  
5. Útvíkka eða draga saman sniðmátshluti Tölvupóst.
    * Veljið sniðmát fyrir tölvupóst sem nota á til að senda tölvupóst með því að nota Tölvupóstur > Færslur sem tengjast aðgerð tengiliðs í Innheimtuskjámyndinni.  
    * Veljið sniðmát fyrir tölvupóst sem nota á til að senda yfirlit viðskiptavinar sem viðhengi við tölvupóstskilaboð með því að nota Tölvupóstur > Yfirlit sem tengist aðgerð tengiliðs í innheimtuskjámyndinni.  
    * Veljið sniðmát fyrir tölvupóst sem nota á til að senda tölvupóst með því að nota Tölvupóstur > Færslur sem tengjast aðgerð söluaðila í Innheimtuskjámyndinni.  

## <a name="age-customer-balance"></a>Aldursgreina stöður viðskiptavinar
1. Fara í Skuldir og innheimta > Reglubundin verk > Aldursgreina stöður viðskiptavinar.
    * Velja skal skilgreiningu aldurstímabils Ferli skyndimynd aldurstímabils aldursgreinir færslur samkvæmt aldurstímabil sem eru skilgreind í völdu skilgreining aldurstímabils.  
    * Velja skal hóp viðskiptavina eða skiljið reit eftir auðan til að stofna aldursgreiningarmyndir fyrir alla viðskiptavini. Ef viðskiptavinahópur er valinn er ferli aldursgreiningarmyndar notað aðeins fyrir viðskiptamannalykla sem eru hluti af viðskiptavinahópnum. Valinn viðskiptavinahópur verður að vera af gerðinni Aldursgreningarmynd.  
    * Velja dagsetningu til að byggja útreikninga aldursgreiningarmyndar á.    Færsludagsetning – aldursgreina hverja færslu á grundvelli færsludagsetningar.    Gjalddagi – aldursgreina hverja færslu á grundvelli gjalddaga hennar.    Dagsetning skjals - aldursgreina hverja færslu á grundvelli dagsetningar skjalsins.  
    * Veljið dagsetninguna sem á að nota sem gildandi dagsetningu aldursgreiningarmyndar. Aldurstímabil eru reiknaðar út frá þessari dagsetningu.    Dagurinn í dag (nota kerfisdagsetningu). Notið þennan valkost ef vinnsla er sett upp til að koma í endurtekna runuvinnslu. Ef þessi dagsetning er notuð er hægt að keyra endurtekna runuvinnslu með reglulegu millibili og kerfisdagsetningin á sama tíma er notuð.    Valinn dagsetning – nota dagsetning sem þú tilgreinir. Ef þessi valkostur er valinn skal færa inn dagsetningu aldursgreiningar.  
2. Smellið á „Í lagi“.

## <a name="view-aged-customer-balances"></a>Skoða aldursgreindar stöður viðskiptavinar
1. Fara í skuldir og innheimta > Innheimta > Aldursgreindar stöður.
    * Nota þessa listasíðu til að skoða stöðu viðskiptavinar og aldursgreind upphæðir með aldursgreiningu tímabil. Þessar upplýsingar eru geymdar í aldursgreiningarmynd. Aldurstímabil ákvarðast af skilgreiningu aldurstímabils sem er notuð. Skilgreining aldurstímabils er fengið úr viðskiptavinahópnum ef það var tilgreint fyrir fyrirspurnarhópinn. Ef viðskiptavinahópnum hefur ekki skilgreining aldurstímabils, er notað sjálfgefna skilgreining aldurstímabils sem er tilgreint í skjámyndinni færibreytur viðskiptakrafna.  
2. Víkkið út upplýsingareitinn „Tengiliður“.
    * Sjálfgefinn tengiliður fyrir viðskiptavinur  
    * sjálfgefið Sölumaður fyrir viðskiptavininn.  
3. Víkkið út upplýsingareitinn „Lánamark“.
    * Notið lánaupplýsingar Upplýsingakassi til að skoða lánamark og upplýsingum um núverandi staða fyrir viðskiptavin.  

## <a name="view-customer-collections-details"></a>Skoða innheimtuupplýsingar viðskiptavinar
1. Í listanum skal smella á tengilinn í valinni línu.
2. Stækka Aðsetur upplýsingareitur.
3. Stækka Tengiliður upplýsingareitur.
4. Víkkið út upplýsingareitinn „Aldursgreining“.
5. Víkkið út upplýsingareitinn „Lánamark“.
6. Í aðgerðasvæðinu er smellt á innheimta.
    * Uppfæra aldursgreiningarmynd fyrir viðskiptavin, með gildandi dagsetningu sem dagsetningu aldursgreiningar sem færsludagsetningar er borinn saman við. Ef aldursgreiningarmynd inniheldur upplýsingar fyrir marga lögaðila, inniheldur uppfærðar aldursgreiningarmynd upplýsingar fyrir sama lögaðila. Upphæðir eru geymdar í bókhaldsgjaldmiðli lögaðilans sem notandinn er skráður á þegar aldursgreiningarmynd er uppfærð.  
    * Velja skal skilgreiningu aldurstímabils Að sjálfgefnu er aldurstímabil sem tengist aldursgreiningarmynd fyrir viðskiptavin birt. Skilgreining aldurstímabils stjórnar aldurstímabili og upphæðum sem eru sýndar í upplýsingareitunum Aldursgreindar stöður og Lánaupplýsingar.  
    * Opna valmynd sem inniheldur eftirfarandi atriði: Fyrirtæki – Birta upphæðir í Aldursgreindar stöður og lánaupplýsingar Upplýsingakassa í bókhaldsgjaldmiðli lögaðila.    Viðskiptavinur – Birta upphæðir í Aldursgreindar stöður og lánaupplýsingar upplýsingareitunum í gjaldmiðli viðskiptavinar.  
    * Veljið eina eða fleiri lögaðila í aldursgreiningarmynd viðskiptavinar sem á að skoða upplýsingar um. Lögaðilar sem eru sýndar á lista var valinn þegar aldursgreiningarmynd var stofnuð.  
    * Skoða yfirlit viðskiptavinar í Microsoft Excel-sniði. Hægt er að velja upphafsdagsetningu fyrir dagsetningasviðið færsla til að hafa með í uppgjörinu og ákveða hvort hafa eigi aðeins opnar færslur með eða bæði opnar og jöfnuðum færslum. Ef aldursgreiningarmynd inniheldur upplýsingar fyrir marga lögaðila, færslur eru hafðar með fyrir alla lögaðila.  
    * Opna skjámyndina Skjöl, þar sem hægt er að stofna eða breyta skjöl eða athugasemdir.  
7. Í aðgerðasvæðinu er smellt á miðla.
    * Opna Outlook, þar sem hægt er að senda tölvupóst skilaboð tengilið sem er tilgreint í svæðinu Tengilið. Ef tengiliður fyrir innheimtu er ekki tilgreint, er aðalaðsetur fyrir viðskiptamanninn notað. Ef aðaltengiliður er ekki tilgreint, tölvupóstskilaboð verður sent í fyrsta aðsetur skráð í Tengiliður skjámynd. Færslur sem eru valin eru hafðar með sem viðhengi. Viðhengið í Excel-sniði og inniheldur þrjár vinnublöðunum. Hægt er að tilgreina sem sniðmát fyrir tölvupóst fyrir skilaboð á tengiliðum viðskiptavinar í skjámyndinni færibreytur viðskiptakrafna.  
    * Þessi hnappur er ekki tiltækur ef tengilið sem er valin í þessari skjámynd hafa ekki tölvupóstfang sett upp.  
    * Undirbúa yfirlit og til að opna Outlook, þar sem hægt er að senda tölvupóst skilaboð sem hefur yfirliti í viðhengi til aðsetur sem er tilgreint í svæðinu Tengilið. Ef tengiliður fyrir innheimtu er ekki tilgreint, er aðalaðsetur fyrir viðskiptamanninn notað. Ef aðaltengiliður er ekki tilgreint, tölvupóstskilaboð verður sent í fyrsta aðsetur skráð í Tengiliður skjámynd.  
    * Þessi hnappur er ekki tiltækur ef tengilið sem er valin í þessari skjámynd hafa ekki tölvupóstfang sett upp.  
    * Opna Outlook, þar sem hægt er að senda tölvupóst skilaboð fyrir starfsmanninn sem er tilgreindur sem sölufulltrúa fyrir söluflokkur sem er úthlutaður viðskiptavininum. Ef færslur eru valdar þær eru teknar með sem viðhengi. Viðhengið í Excel-sniði og inniheldur tvo vinnublöðunum. Hægt er að tilgreina sem sniðmát fyrir tölvupóst fyrir skilaboð á sölumenn í skjámyndinni færibreytur viðskiptakrafna.  
    * Þessi hnappur er ekki tiltækur ef sölumanneskju sem er birt í þessari skjámynd hafa ekki tölvupóstfang sett upp.  
    * Hægt er að skoða og framkvæma aðgerðir á færslum fyrir viðskiptavininn. Ef verið er að nota miðstýrðar greiðslur er með upplýsingar fyrir alla lögaðila sem eru innifaldar í aldursgreiningarmynd viðskiptavinar. Hægt er að takmarka upplýsingarnar um lögaðili með því að nota hnappinn Fyrirtækis í Velja flokk í Aðgerðarúðunni.  
    * Breyta stöðu innheimtu fyrir völdu færslurnar.    Enginn ágreiningur – engar innheimtuaðgerðir hafa farið fram fyrir færsluna.    Ágreiningur – viðskiptamaðurinn hefur tilkynnt að eitthvað sé athugavert við færsluna.    Loforð um greiðslu - viðskiptavinur hefur samþykkt að greiða upphæð færslunnar.    Leyst – Öll vandamál með færsluna hafa verið leyst og engir viðbótarinnheimtuverkþættir eru nauðsynlegir.  
    * Opna valmynd og veljið einn af eftirfarandi atriði til að tilgreina hvaða færslur á að birta í þessari skjámynd: Opna – Birta aðeins færslur sem hafa ekki verið jafnaðar.    Opnar og lokaðar – Birta allar færslur bæði jöfnuð og ekki jöfnuð.  
    * Vinna úr völdu greiðsluna sem greiðslu af gerðinni ónógir sjóðir (FSF-greiðsla).    Þessi hnappur býðst aðeins ef valda færslan er greiðsla (kreditstaða án reiknings) sem hefur verið færð inn í greiðslubók, bankareikningur er tengdur við færsluna og ekki hefur verið hætt við greiðsluna áður.  
    * Afskrifa valdar færslur.  
    * Merkja valdar færslur fyrir jöfnun með hver annarri.  
    * Opna Upprunalega skjámynd skjals, þar sem hægt er að skoða og prenta skjal fyrir valda færslu.  
    * Opna valmynd sem inniheldur eftirfarandi atriði: Innheimta – Birta aðeins verkþætti sem voru stofnaðar í innheimtuskjámyndinni.    Allt – Birta alla verkþætti fyrir viðskiptavininn, þar sem stofnaðar voru við verkþætti.  
    * Opna valmynd sem inniheldur eftirfarandi atriði: Opna – Birta aðeins verkþætti sem eru ekki lokað.    Opnar og lokaðar – Birta allar aðgerðir, burtséð frá stöðu þeirra.  
    * Velja innheimtumál sem úthlutað er til viðskiptavinar eða skiljið eftir autt. Ef máls er valinn eru aðeins færslur og verkþætti sem eru tengdar við málið birtast í þessari skjámynd.  
8. Smellið á listann Sýna.
    * Veljið viðskiptavinalykil eða samþykkið sjálfgefnu færsluna. Að sjálfgefnu er í valinn reikning viðskiptavinar á síðu viðskiptavinalista eða í skjámyndinni sem þessi skjámynd var opnuð. Ef skjámyndin er opnuð úr listasíðunni eru viðskiptavinum í lista viðskiptavina sem eru teknar með í hópnum innheimtu sem er notuð á listasíðunni.  


