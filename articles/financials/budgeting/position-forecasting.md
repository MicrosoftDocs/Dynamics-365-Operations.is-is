---
title: "Stöðuspá"
description: "Útgjöld sem eru tengd starfsmönnum eru oft stórt hlutfall af kostnaði fyrirtækis. Stöðuspá leyfir þér að áætla þennan kostnað og hafa hann með í fjárhagsáætlunargerð."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 64413
ms.assetid: 35e791d2-1905-4808-a579-7f181ddddd91
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: fa11f1775017dd9bada61340b4bed70ea66a4137
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="position-forecasting"></a>Stöðuspá

[!include[banner](../includes/banner.md)]



Útgjöld sem eru tengd starfsmönnum eru oft stórt hlutfall af kostnaði fyrirtækis. Stöðuspá leyfir þér að áætla þennan kostnað og hafa hann með í fjárhagsáætlunargerð.

## <a name="position-forecasting-in-budget-planning"></a>Stöðuspá í fjárhagsáætlunargerð

[![Efstu myndrænt](./media/graphic-top.png)](./media/graphic-top.png) 

Stöðuspá notar þrjá aðalíhluti til að veita nákvæmar áætlunarupphæðir fyrir stöðukostnað. Síðan má færa þessar upphæðir inn í fjárhagsáætlunargerð fyrir útreikning á fjárhagsáætlunagsáætlun. 

Aðalíhluturinn er **spástaða** sem stendur fyrir öll kostnaðargögn sem eru tengd einni stöðu. Hægt er að stofna margar útgáfur spástöðu með því að úthluta öðrum aðstæðum fjárhagsáætlunargerðar á hverja útgáfu. Margar útgáfur leyfa á endurtekninganálgun að áætlun og hægt er að bera saman hvað-ef-aðstæður. Hver spástaða hefur samsvarandi stöðu í Mannauði.

**Kostnaðareining fjárhagsáætlunar** er uppsettur íhlutur sem stendur fyrir tiltekinn kostnað sem tengist stöðu, eins og grunnlaunum, sjúkratryggingum greiddum af vinnuveitanda, farsímastyrk og svo framvegis. Kostnaðareining fjárhagsáætlunar inniheldur aðallykilinn sem er notaður fyrir kostnað og valkosti fyrir útreikning. Hægt er að úthluta hverri kostnaðareiningu fjárhagsáætlunar á margar spástöður 

**Launaflokkur** er valfrjáls uppsetningaríhlutur sem er notaður til að jafna safn af kostnaðareiningum fjárhagsáætlunar og launaútreikning í stöður sem hafa svipuð launaeinkenni. Launaflokkur getur innihaldið launanet launataxta. Þegar flokknum er úthlutað á spástöðuna getur stig og þrep í hnitanetinu úthlutað tekjum á spástöðu. Safni kostnaðareininga er sjálfkrafa bætt við.

### <a name="position-forecasting-processes"></a>Ferli stöðuspár

[![graphic1b](./media/graphic1b.png)](./media/graphic1b.png) 

Í dæmigerðu ferli fyrir stöðuspár verður fyrst að stofna uppsetningaríhluti (kostnaðareiningar fjárhagsáætlunar og launaflokka). Spástöður eru síðan myndaðar, byggt á núverandi stöðum. Þá er hægt að gera breytingar. Til dæmis er hægt bæta við eða ljúka stöðum, breyta launatöxtum og kostnaði sem tengist fríðindium og bæta við launahækkunum. Hægt er að stofna margar útgáfur spástöðu til að auðvelda samanburð á ólíkum aðstæðum fjárhagsáætlunargerðar. Næst er hægt að taka spástöður inn í fjárhagsáætlunargerðir og færa inn kostnað úr spástöðunum sem línur fjárhagsáætlunargerðar.

Hægt er að stofna viðbótarútgáfur spástöðu þegar fjárhagsáætlanir eru endurskoðaðar. Þessar nýjar útgáfur skapa grundvöll fyrir endurskoðanir.

## <a name="position-forecasting-setup"></a>Uppsetning stöðuspár
[![graphic2](./media/graphic2-1024x327.png)](./media/graphic2.png)

### <a name="budget-cost-elements"></a>Kostnaðareiningar fyrir þessa fjárhagsáætlun

Kostnaðareiningar fjárhagsáætlunar eru notaðar til að skilgreina upplýsingar um kostnað fyrir spástöðu. Þessar upplýsingar innihalda gerð kostnaðar, hvernig kostnaður er reiknaður og hvort kostnaði er úthlutað á margar dagsetningar þegar spástaðan er innifalin í fjárhagsáætlun. 

Tilgreindir reitir skilgreina hegðun kostnaðareiningar fjárhagsáætlunar. Hverri kostnaðareiningu fjárhagsáætlunar er úthlutað kostnaðargerð fjárhagsáætlunar **Tekjur**, **Fríðindi**, **Skattar** eða **Annað**. Kostnaðargerðir fjárhagsáætlunar er aðallega notaðar til að reikna samtölur. Gildið **Hnekking spástöðu** tilgreinir hvort hægt sé að breyta upphæð á einingu í spástöðunni. Reiturinn **Úthlutunaraðferð** er notaður þegar spástöðu er bætt við fjárhagsáætlun. Hægt er að skipta kostnaðarupphæð upp í aðskildar fjárhagsáætlunarlínur sem hafa mismunandi dagsetningar, á mánaðarlegum, ársfjórðungslegum, vikulegum eða hálfsmánaðarlegum grundvelli. Með því að velja upphafsdagsetningu úthlutarðu kostnaði sem einni upphæð á upphafsdagsetningu sem er stillt á spástöðuna. 

Útreikningur á kostnaðarupphæð kostnaðareiningar fjárhagsáætlunar notar gildisdagsetningar til að virkja sömu kostnaðareininguna sem á að nota á mismunandi tímabilum. Stökum aðallykli er úthlutað á hvert tímabil, ásamt prósentu eða árlegri upphæð sem tilgreinir kostnaðarupphæð. Kostnaðareining fjárhagsáætlunar getur notað prósentu annarrar kostnaðareiningar eða árleg upphæð, en ekki hvort tveggja. Einnig er hægt að tilgreina árleg mörk. 

Ef kostnaðareiningin er byggð á prósentu, verður að tilgreina kostnaðareiningar fjárhagsáætlunar sem eru notaðar sem grunnur fyrir útreikning.

**Dæmi** 

Fyrirtæki Jodi veitir þjálfunarafslátt upp á 5% af grunnlaunum starfsmanns. Jodi þarf að stofna kostnaðareiningu fjárhagsáætlunar fyrir þennan kostnað. Hún stofnar nýja kostnaðareiningu fjárhagsáætlunar og úthlutar **Fríðindai** kostnaðargerð fjárhagsáætlunar.

Jodi vill ekki að stjórnendur breyti upphæð fríðinda. Þess vegna velur hún **Ekki heimila kostnaðarbreytingar** í reitnum **Hnekking spástöðu**. Fyrirtækið vill að þessum kostnaðuri sé úthlutað jafnt í hverjum mánuði. Þess vegna velur Jodi **Ársfjórðungslega** í reitnum **Úthlutunaraðferð**. 

Næst bætir Jodi við línu kostnaðarútreikningsins, stillir dagsetningar og aðallykil og færir inn **5,00** í prósentum. Fyrirtækið hennar er með þak upp á 5,000 USD ári fyrir þessi fríðindi. Þess vegna færir Jodi upphæðina inn sem árleg mörk. 

Loks bætir Jodi við öllum kostnaðareiningum tekna sem eru notaðar fyrir grunnlaun og sem grundvöllur útreiknings. Núna er kostnaðareining fjárhagsáætlunar hennar tilbúin til notkunar.

### <a name="compensation-groups"></a>Launaflokkar

Hægt er að nota launaflokka til að flokka spástöður sem hafa svipaða eiginleika launa. Einnig er hægt að nota þá til að skilgreina tekjur og árlega aukningu spástöðu og til að úthluta safni algengra eininga fjárhagsáætlunar. 

Grunnaðgerðir launaflokka eru að úthluta safni af kostnaðareiningum fjárhagsáætlunar á spástöðu. Þess vegna er hægt að nota launaflokka til að bæta við almennum kostnaði, eins og fríðindaáætlunum og sköttum. Stjórnandi sem stofnar spástöðu þarf ekki að þekkja allar kostnaðareiningarnar sem verður að bæta við. Í staðinn er hægt að bæta kostnaðareiningum við þegar launaflokkur er valinn. Einingunum er bætt við uppsetningu launaflokkurs á flipanum **Kostnaðareiningar fyrir þessa fjárhagsáætlun**. 

Launaflokkar geta einnig ákvarðað launataxta fyrir spástöðu. Hægt er að setja upp flokk sem notar annaðhvort klukkutíma eða árslaun sem grunn til að reikna út tekjur spástöðu. Á flipanum **Töflur yfir launahlutfall** ákvarðar launanet launataxta þær tekjur sem bætt er við spástöðu, byggt á úthlutuðu stigi og þrepi. Þessar hnitanet geta byggt á fyrirliggjandi launanetum í mannauði. Einnig er hægt að stofna nýtt launanet fyrir fjárhagsáætlunargerð. 

Gildisdagsetningar og lokadagar í töflum launahlutfalls leyfa alltaf breytingar á launataxta. Þessi eiginleiki er gagnlegur þegar launaviðræðueining hefur samið um aðhliða hækkun í miðju ferli fjárhagsáætlunar. Í þessu tilfelli breytirðu lokadegi fyrirliggjandi töflu í daginn á undan dagsetningu taxtabreytingarinnar og bætir við nýrri taxtatöflu sem hefst á nýju dagsetningunni. Þegar ný taxtatafla er stofnuð og valið er **Búa til nýtt launanet úr núverandi neti** er hægt að velja fyrirliggjandi taxtatöflu úr mannauði. Í taxtatöflunni sem er stofnuð gerir valkosturinn **Fjöldabreyting** það mögulegt að nota prósentu eða flata upphæð fyrir aukningu eða lækkun á alla taxta í hnitanetinu. 

Reitirnir **Bæta við áætlun** og **Dagsetning aukningar** í launaflokknum eru notaðir þegar stofna þarf launahækkanir, þar sem stöður fara úr einu þrepi á það næsta. Árleg launahækkun er dæmigerðar aðstæður. Bæta við áætlun ákvarðar hvort starfsafmæli stöðu eða ein almenn dagsetning er notuð fyrir hækkun þreps. Bæta við áætlun gildir um allar spástöður í launaflokki. 

Kostnaðareining tekna sem er valin í launaflokknum er notuð þegar tekjur eru stofnaðar fyrir spástöður í flokknum, þar með talið grunnlaun og allar þrepaaukningar. Reiturinn **Fyrirkomulag fastra Launa** tengir launaflokk við fyrirkomulag fastra launa í mannauði. Þessi tengill getur úthlutað upplýsingum um föst laun starfsmanns á spástöðu og getur þess vegna gert fjárhagsáætlunargerð nákvæmari. Munið að skipan launanets (stig og þrep) fyrir launaflokk ætti að samsvara skipan launafyrirkomulags fastra launa. Annars getur kerfið ekki tengt launaflokk og launafyrirkomulag fastra launa á réttan hátt.

## <a name="creating-forecast-positions"></a>Stofnar nýja stöðuspá
[![graphic3](./media/graphic3-1024x327.png)](./media/graphic3.png)

### <a name="creating-forecast-positions-for-existing-positions"></a>Stofna spástöður fyrir fyrirliggjandi stöður

Fyrir sem nákvæmasta fjárhagsáætlunargerð er hægt að stofna spástöður með því að nota upplýsingar úr fyrirliggjandi stöðum í Dynamics 365 for Finance and Operations, Enterprise Edition, óháð því hvort staða hefur verið fyllt eða ekki. 

Aðgerðin **Bæta við stöðum sem til eru** birtir allar stöður fyrir fyrirtæki. Með því að stilla dagsetninguna **Frá og með** er hægt að breyta lista yfir stöður þannig að það innihaldi staði sem voru til á dagsetningu í fortíðinni eða, sem er algengara, í framtíðinni (til dæmis upphaf næsta ferlis fjárhagsáætlunar). Veljið ferli fjárhagsáætlunargerðar og aðstæður fjárhagsáætlunargerðar, veljið stöður í listanum og smellið síðan á **Í lagi** til að stofna spástöðu fyrir valdar stöður. Athugið að aðeins er hægt að stofna eina spástöðu fyrir hverja fyrirliggjandi stöðu í ferli og aðstæðumar fjárhagsáætlunargerðar. Hins vegar er hægt að stofna frekari útgáfur með því að úthluta mismunandi aðstæðum fjárhagsáætlunargerðar. 

Ef kostnaðareiningum fjárhagsáætlunar hefur verið úthlutað á stöðu í mannauði er þessum kostnaðareiningum fjárhagsáætlunar einnig úthlutað á spástöðu og þær nota sjálfgefnar upphæðir. Reiturinn **Úthlutaður starfsmaður** í spástöðunni er stilltur á nafn starfsmanns sem er úthlutað á stöðuna, ef starfsmanni er úthlutað. Þessi reitur er einfaldur textareitur. Engin beinn tengill er stofnaður. 

Ef kostnaðareining fjárhagsáætlunar er valin er árlegri upphæð fastra launa úthlutað á spástöðuna með því að nota valda kostnaðareiningu, að því tilskildu að úthlutaður starfsmaður hafi launafyrirkomulagi fastra launa. Ef starfsmaðurinn er ekki með fyrirkomulag fastra launa eða ef engum starfsmanni er úthlutað er sjálfgefin upphæð notuð fyrir kostnaðareiningu fjárhagsáætlunar. 

Þegar valkosturinn **Úthluta launaflokki** er stilltur á **Já**, ef starfsmaðurinn sem er úthlutað á stöðuna er með þrepaskipt fyrirkomulag fastra launa sem er tengt launaflokki (eins og lýst var áður), er stigi og þrepi frá starfsmanni úthlutað á spástöðuna ásamt launaflokknum. Kostnaðareiningu tekna úr launaflokki er bætt við spástöðuna og úr launaflokki er bætt við spástöðu og launataxta á stigi og þrepi úr launaflokki er notaður. 

Stillingin á valkostinum **Úthluta launaflokki** hefur forgang fram yfir stillinguna **Úthlutun kostnaðareiningar fjárhagsáætlunar**. Hægt er að nota stillingarnar tvær á sama tíma. 

[![graphic4](./media/graphic4.png)](./media/graphic4.png) 

Annar valkostur er að úthluta árlegri dagsetningu. Valin dagsetning (leiðréttur upphafsdagur, upphafsdagur starfsmanns, upphafsdagur starfs eða starfsaldursdagsetning) úthlutaðs starfsmanns er síðan stillt sem árleg dagsetning spástöðu og er notuð til upplýsinga og þegar launahækkanir eru myndaðar.

### <a name="creating-new-forecast-positions"></a>Stofnun nýrrar stöðuspá

Hægt er að stofna nýja spástöður á tvo vegu: með afritun á fyrirliggjandi spástöðu og með því að stofna algerlega nýja spástöðu. 

Þegar spástaða er valin skal velja **Afrita valda spástöðu** til að stofna nýja spástöðu sem er með spána **Fyrirhugað**. Þessi spástaða er með öll sömu gögn og spástaðan sem var afrituð, fyrir utan úthlutaðan starfsmann og athugasemdir um kostnaðareiningar fjárhagsáætlunar. Athugið að samsvarandi ný staða er einnig stofnuð í mannauði. Þessi staða er með lýsinguna **Stofnað af spá**. 

Einnig er hægt að búa til alveg nýja spástöðu. Veldu fyrirliggjandi starf og veldu einnig ferli fjárhagsáætlunargerðar og aðstæður fjárhagsáætlunargerðar. Síðan er hægt að bæta við öðrum upplýsingum sem óskað er eftir. Enn aftur, ný staða stofnuð er um leið í mannauði.

## <a name="working-with-forecast-positions"></a>Unnið með spástöður
[![graphic5](./media/graphic5-1024x327.png)](./media/graphic5.png)

### <a name="multiple-versions-of-a-forecast-position"></a>Margar útgáfur spástöðu

Hægt er að breyta spástöðum til að beita annaðhvort þekktum breytingum fyrir ferli fjárhagsáætlunar eða til að móta fyrirhugaðar breytingar. Algengur háttur er að stofna grunnlínusafn af spástöðum, stofna afrit af þeim spástöðum og nota svo afritin til að móta mismunandi söfn af breytingum. Afritunum er úthlutað á aðrar aðstæður fjárhagsáætlunargerðar en, í það minnsta þar til breytingar eru gerðar, eru annars samsvarandi spástöðunum sem þær eru afritaðar frá. Frumrit og afrit deila sömu stöðu í mannauði. 

Virknin **Afrita í aðstæður** veitir þessa virkni. Athugið að hver mannauðsstaða getur aðeins haft eina spástöðu í hverjum aðstæðum fjárhagsáætlunargerðar.

### <a name="modifying-forecast-positions"></a>Spástöðum breytt

Breytingar sem gerðar eru á spástöðum eru takmarkaðar við þær spástöður. Breytingarnar hafa ekki áhrif á stöðufærslur í mannauði. Flestar breytingar takmarkast einnig við spástöðuna sem verið er að breyta. Með öðrum orðum eru breytingarnar sértækar fyrir það ferli og aðstæður fjárhagsáætlunargerðar sem er úthlutað. Undantekningar eru breytingar á reitum sem eru samnýttir fyrir stöðu fyrir ferli og aðstæður. Þessir reitir eru reitirnir á flipanum **Almennt** og flipanum **Fjárhagsvíddir**. Þegar þessum reitum er breytt eiga nýju gildin við stöðuna í öllum aðstæðum fjárhagsáætlunargerðar. Þar af leiðandi leyfa þessir reitir að allar útgáfur séu uppfærðar á skjótan hátt.

#### <a name="budget-cost-elements"></a>Kostnaðareiningar fyrir þessa fjárhagsáætlun

Kostnaðareiningar fjárhagsáætlunar veita aðalupplýsingar fyrir fjárhagsáætlunargerðir: upphæð fjárhagsáætlunar og aðallykilinn. Áætlunarupphæðin er sú upphæð sem er send á fjárhagsáætlun þegar spástaða er höfð með í áætlun. Fjárhagsáætlun er reiknuð út og ekki er hægt að breyta henni beint. Þessi upphæð er annaðhvort árleg upphæð eða útreikningur á prósentu grunneininga árlegrar upphæðar (eins og skilgreint er í uppsetningu á kostnaðareiningu fjárhagsáætlunar). Upphæðin er síðan þáttur í þeim fjölda daga sem er í dagsetningabili einnigarinnar (upphafsdagsetningu til lokadags) og einnig með gildinu **Jafngildi fulls starfs** (FTE) fyrir spástöðuna. 

Til dæmis er fjárhagsáætlun kostnaðarlínu einingar frá 1. janúar 2017 til 30. júní 2017, sem er með árlega upphæð 100.000 og FTE gildi upp á **0,50** reiknuð sem 100.000 × (181 dagar ÷ 365 dagar) × 0,50 = 24.794,52. 

Línur kostnaðareiningar fjárhagsáætlunar verður einnig að endurreikna þegar FTE-gildinu er breytt í spástöðunni. Einnig verður að endurreikna línurnar þegar virkjunardagsetningum eða starfslokadagsetningum er breytt. Breytingar á dagsetningum geta valdið uppfærslu á upphafs- og lokadagsetningum kostnaðareiningar fjárhagsáætlunar, sem verða að vera innan dagsetninga spástöðunnar. Þegar endurútreiknings er þörf verður hnappurinn **Endurreikna** tiltækur og skilaboðin „Þarnast útreiknings“ birtast. Endurútreikningur er einnig áskilinn ef hægt er að bæta við eða fjarlægja kostnaðareiningu fjárhagsáætlunar.

**Dæmi** 

Fyrirtækið íhugar tvo valkosti til að draga úr kostnaði við stöðu endurskoðanda. Einn valkostur er að ljúka stöðunni hluta ársins. Annar valkostur er að breyta stöðunni í hálfan vinnudag fyrir allt árið. Brad hefur stofnað spástöðu fyrir núverandi stöðu bókhaldara í grunnlínuaðstæðum. Hann afritar þessa grunnlínuspá í aðstæður A, stillir dagsetningu starfsloka á 31. maí og endurreiknar. Síðan afritar Brad grunnlínuspána í aðstæður B, breytir FTE-gildinu í **0,50** og endurreiknar. Brad hefur nú þrjár útgáfur sem hvert um sig hefur kostnaðarsamtölur sem hafa verið samstilltar við valkosti hans.

#### <a name="assigning-a-compensation-group"></a>Úthlutun launaflokks

Þegar þú fyrst úthlutar launaflokki á spástöðu er sjálfgefnum kostnaðareiningum fjárhagsáætlunar bætt við úr launaflokknum. Ef kostnaðareiningunum hefur þegar verið úthlutað á spástöðuna, haldast þessar kostnaðareiningar. Ef launaflokk hefur þegar verið úthlutað og verið er að breyta honum eru núgildandi kostnaðareiningar fjárhagsáætlunar fjarlægðar og þeim skipt út með safni úr launaflokki. 

Þegar launastig og -þrep eru valin er tekjum kostnaðareiningar fjárhagsáætlunar (eins og skilgreint er í launaflokki) bætt við. Árleg upphæð er reiknuð með því að nota taxta í völdu stigi og þrepi og árlegar vinnustundir í launaflokknum (eða, fyrir árslaun, heildarupphæð í stigi og þrepi). Enn aftur, þessi upphæð er þáttur í dagsetningabili í línu kostnaðareiningarinnar og FTE-gildi spástöðunnar.

#### <a name="generating-increases"></a>Mynda hækkanir

Árlegar hækkanir (ein á almanaksárinu) er hægt að stofna sjálfkrafa fyrir spástöður sem eru með úthlutaðan flokk þrepaskiptra launa. Smellið á **Mynda hækkun** til að bæta við kostnaðareiningu fjárhagsáætlunar tekna við næsta hæsta skref. Upphafsdagur nýrrar kostnaðareiningar tekna er dagsetning áætlaðrar hækkunar sem er birt í spástöðunni. Þessi dagsetning er valin úr launaflokki á einn af tveimur háttum. Ef áætlun um hækkun í launaflokki er stillt á **Sameiginleg dagsetning** er dagsetning hækkunar tilgreind í launaflokki. Ef áætlun um hækkun er stillt á **Árleg dagsetning** er reiturinn Árleg dagsetning í spástöðunni notaður og ferli fjárhagsáætlunar setur inn árið. Ef margar almanaksár eru í ferli fjárhagsáætlunar er mörgum hækkunum bætt við. 

Lokadagur núverandi kostnaðareiningar tekna er uppfærður með deginum á undan dagsetningu hækkunar. Endurútreikningsferlið er sjálfkrafa notað þegar hækkanir eru myndaðar. Þess vegna er þarf ekki að endurreikna handvirkt. 

Ef smellt er aftur á **Mynda aukningu** er vinnslan aftur keyrð en bætir ekki við fleiri færslum. Aðeins ein hækkun er stofnuð á almanaksárinu.

#### <a name="changes-from-other-pages"></a>Breytingar af öðrum síðum

Uppfærslur á spástöðum koma einnig úr öðrum svæðum, eins og uppsetningarsíðum kostnaðareiningar fjárhagsáætlunar og launaflokks. Einnig er hægt að breyta spástöðum með því að nota fjöldauppfærsluferlið. 

Tveir valkostir eru í boði á uppsetningarsíðunni **Kostnaðareining fjárhagsáætlunar**: **Bæta við stöður** og **Uppfæra stöður**. Valkosturinn **Bætið við stöður** bætir kostnaðareiningu fjárhagsáætlunar við valdar spástöður. Ef einingunni hefur þegar verið úthlutað á spástöðu er þeirri spástöðu sleppt. Valkosturinn **Uppfæra stöður** á við um núverandi gildi (aðallykill, prósenta, árleg upphæð og svo framvegis) í völdum spástöðum. 

Hver vinnsla hefur svipaða síðu þar sem hægt er að velja spástöður. Síðan **Bætið við stöður** sýnir allar spástöður sem eru tiltækar til vals, en síðan **Uppfæra stöður** sýnir einungis þær spástöður sem hefur þegar verið úthlutað kostnaðareiningum fjárhagsáætlunar. (Þess vegna veitir síðan **Uppfæra stöður** leið til að komast að því hvaða spástöður hafa þegar verið tengdar kostnaðareiningu.) Spástöður eru fluttar úr efra hnitaneti í neðra hnitaneti til að hafa þær með í uppfærslu. 

Athugið að aðgerðin **Breyta dagsetningum** á flipanum **Kostnaðarútreikningur** breytist strax upphafs- og lokadagsetningum kostnaðareiningar fjárhagsáætlunnar í spástöðunum. Valkostir um ekkert val eru tiltækir. 

Á síðunni **Launaflokkur** beitir aðgerðin **Uppfæra stöðutaxta** núgildandi töflu launataxta á spástöður sem eru úthlutaðar á flokkinn. Taxtarnir eru uppfærðir og viðbótarlínum kostnaðareiningar er bætt við fyrir allar nýjar línur taxtatöflu (sem byggja á dagsetningum). Hins vegar eru kostnaðareiningar fjárhagsáætlunar og dagsetningar hækkunar ekki uppfærðar. Hægt er að velja hvaða ferli fjárhagsáætlunargerðar og aðstæður fjárhagsáætlunargerðar á að uppfæra. Þess vegna er hægt að uppfæra einar aðstæður en hafa aðrar aðstæður óbreyttar fyrir samanburð. 

Með því að velja spástöður og smella síðan á **Fjöldauppfærsla** er hægt að bæta við eða breyta fleiri en einni spástöðu í einu. Margir valkostir eru í boði. Einn valkostur á flipanum **Fjárhagsvíddir** er eilítið öðruvísi en hinir og tengist kostnaðareiningum fjárhagsáætlunar. Hægt er að bæta við kostnaðareiningum fjárhagsáætlunar með því að stilla valkostinn **Sjálfgildi fjárhagsáætlunar** á **Já**. Ef engar kostnaðareiningar fjárhagsáætlunar eru valdar en **Sjálfgildi fjárhagsáætlunar** eru stillt á **Já** eru allar kostnaðareiningar fjárhagsáætlunar sem hefur verið úthlutað fjarlægðar. 

Endurútreikningsferlið er sjálfkrafa notað á allar spástöður sem hafa breyst.

## <a name="bringing-forecast-positions-into-budget-plans"></a>Spástöður settar inn í fjárhagsáætlanir

[![graphic6](./media/graphic6-1024x327.png)](./media/graphic6.png)

Tilgangur stofnunar og breytinga á spástöðum er að bæta þeim við fjárhagsáætlanir, svo að fjárhagsáætlanirnar innihaldi sem nákvæmastar upphæðir fjárhagsáætlunar. Það eru tvær aðferðir til að bæta spástöðum við fjárhagsáætlanir. Hægt er að nota myndunarferli eða valferli á fjárhagsáætlunargerðina.

### <a name="generating-a-budget-plan-from-forecast-positions"></a>Myndun fjárhagsáætlunar úr spástöðum

Aðgerðin **Mynda fjárhagsáætlun úr spástöðum** stofnar eða uppfærir fjárhagsáætlunargerðir svo að þær hafi áætlunarupphæðir og FTE-talningar úr spástöðum. Upphæðir fjárhagsáætlunar úr spástöðunni verða línuupphæðir fjárhagsáætlunar og eru því teknar saman eftir fjárhagsvíddargildum og gildisdagsetningu. Myndunarferlið úthlutar upprunaspástöðu á línu fjárhagsáætlunargerðar. Til að skoða stöðu er annaðhvort hægt að bæta spástöðu við sem línu í fjárhagsáætlunarútlit eða nota fyrirspurnina **Fjárhagsáætlunarlínur**. Til að sleppa þessari úthlutun, skal stilla valkostinn **Hafa stöðu í línu fjárhagsáætlunargerðar** á **Nei**. 

Hægt er að velja FTE aðstæður fjárhagsáætlunargerðar til að taka með fjölda FTE í fjárhagsáætlunina. Hægt er að velja einungis áætlanir af gerðinni magn sem eru innifaldar í útliti markfjárhagsáætlunar. Þegar FTE-aðstæður eru valdar verður einnig að tilgreina aðallykil FTE. Þessi lykill er notaður til að stofna fjárhagsáætlunarlínur fyrir magn. 

Ferli og aðstæður fjárhagsáætlunargerðar sem eru valdar í uppruna ákvarða ferli og aðstæður fjárhagsáætlunargerðar markaðstæðna. Þar sem eigindunum er úthlutað á spástöður verða þau að vera samstillt við fjárhagsáætlunina. Þess vegna er ekki hægt að breyta eigindum á markinu. 

Fyrir önnur myndunarferli eru þrír valkostir í boði:

-   **Stofna nýja fjárhagsáætlun** – Stofna nýja áætlun sem hefur eigindir sem eru valdar í hlutanum **Mark**.
-   **Skipta út fyrirliggjandi aðstæðum fjárhagsáætlunargerðar** – Eyða öllum gögnum í fjárhagsáætlun marks í völdum aðstæðum fjárhagsáætlunargerðar og stofna nýjar línur sem hafa gögn valinnar spástöðu.
-   **Uppfæra fyrirliggjandi aðstæður fjárhagsáætlunargerðar og bæta nýjum gögnum við** – Uppfæra fyrirliggjandi línur í markáætlun sem samsvarar upprunalínum og bæta einnig við nýjum línum fyrir ný gögn. Samsvörunin er byggð á fjárhagslykli, dagsetningu, fjárhagsáætlunarklasa og öðrum gildum, eins og spástöðu. Allar línur sem hafa staðsetningarnúmer sem samsvarar stöðu uppruna er skipt út fyrir nýjar línur úr frumkóða.

### <a name="selecting-forecast-positions"></a>Val á spástöðum

Einnig er hægt að bæta upphæðum fjárhagsáætlunar spástöðu beint við fjárhagsáætlunargerð. Nota skal aðgerðina **Bæta við stöðum** fyrir ofan línur fjárhagsáætlunargerðar til að velja spástöður til að taka með. 

Þær aðstæður fjárhagsáætlunargerðar sem eru valdar sem uppruni takmarkast við aðstæður sem eru innifaldar í útlit áætlunar. Einn valkostur á flipanum **Mark** gerir kleift að tilgreina að FTE-aðstæður og aðallykil séu tiltæk til að taka með í FTE-talningum, en þeirra sé ekki krafist. 

Þetta valferli hegðar sér eins og valkosturinn **Uppfæra fyrirliggjandi aðstæður fjárhagsáætlunargerðar og bæta nýjum gögnum við** fyrir myndunarferli. Allar fyrirliggjandi línur fjárhagsáætlunargerðarinnar þar sem spástöðu er bætt við eru fjarlægðar og skipt út fyrir nýju línurnar sem eru byggðar á núverandi stöðu spástöðunnar.

#### <a name="date-options"></a>Dagsetningarvalkostir

Upphafsdagsetning á fjárhagsáætlun kostnaðarlínu einingu ákvarðar gildisdagsetningu samsvarandi línu fjárhagsáætlunargerðar fyrir bæði myndunarferlið og ferlið sem valið er. Reiturinn **Úthlutunaraðferð** á uppsetningasíðu kostnaðareininga fjárhagsáætlunar tilgreinir úthlutunaraðferðina:

-   **Upphafsdagsetning** – Upphafsdagsetning kostnaðareiningar fjárhagsáætlunar er notuð sem gildisdagsetning fjárhagsáætlunarlínu.
-   **Mánaðarleg** – Upphæð fjárhagsáætlunar er deilt jafnt með fjölda mánaða á dagsetningabilinu til að framleiða dæmigerða mánaðarlega upphæð sem er úthlutað á fyrsta degi hvers mánaðar. Ef fyrsta tímabilið er hluti mánaðar er upphæðin fyrir þann mánuð þáttuð með fjölda daga sem kostnaðurinn er virkur í þeim mánuði og niðurstöðunum er úthlutað á upphafsdagsetningu. Upphæð fyrir síðasta mánuð er mismunurinn á milli heildarupphæðar áætlunar og samtölu allra annarra mánaða. Þess vegna getur sléttun haft áhrif á upphæð fyrir síðasta mánuð.
-   **Ársfjórðungslega** – Þessi aðferð er sú sama og **Mánaðarleg** en útreikningar eru gerðir fyrir þriggja mánaða tímabil.
-   **Vikulegt** – Rökunum svipar til rakanna í aðferðunum **Mánaðarleg** og **Ársfjórðungsleg**. Upphæð fjárhagsáætlunar er jafnt deilt með fjölda vikna á dagsetningabili til að framleiða dæmigerða vikulega upphæð sem er úthlutað á fyrsta dag hvers mánaðar. Ef fyrsta tímabilið er hluti viku er upphæðin fyrir þá viku þáttuð með fjölda daga sem kostnaðurinn er virkur í þeirri viku og niðurstöðunum er úthlutað á upphafsdagsetningu. Upphæð fyrir síðustu viku er mismunurinn á milli heildarupphæðar áætlunar og samtölu allra annarra vikna. Þess vegna getur sléttun haft áhrif á upphæð fyrir síðustu viku.
-   **Aðra hverja viku** – Þessi aðferð er sú sama og **Vikuleg** en útreikningar eru gerðir fyrir tveggja vikna tímabil.

#### <a name="changing-budget-plan-lines-that-have-forecast-positions"></a>Breyting fjárhagsáætlunarlínum sem hafa spástöður

Fjárhagsáætlunarlínur sýna uppruna áætlunarupphæða (númer spástöðunnar) en eru ekki tengdar. Þess vegna eru breytingar á spástöðunni ekki sýndar í línu fjárhagsáætlunar og breytingar á línu fjárhagsáætlunar eru sýndar í spástöðu. Ef þú breytir spástöðu og vilt að uppfærslurnar séu hafðar með í fjárhagsáætlun þarf að færa spástöðuna aftur inn í áætlunina. Mundu hins vegar að ferlið fjarlægir allar línur þar sem þeirri spástöðu er úthlutað. Þess vegna eru allar breytingar sem gerðar hafa verið á þessum línum fjarlægðar. 

Til að sjá hvaða fjárhagsáætlanir spástaða hefur verið höfð með í er hægt að mynda skýrsluna **Spástöður eftir fjárhagsáætlun**. Einnig er hægt að opna upplýsingareitinn **Tengdar fjárhagsáætlanir** til að skoða áætlanir í spástöðunni.




