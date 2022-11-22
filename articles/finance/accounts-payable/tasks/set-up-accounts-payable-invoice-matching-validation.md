---
title: Setja upp villuleit fyrir reikningsjöfnun viðskiptaskulda
description: Þessi grein veitir upplýsingar um hvernig á að setja upp samsvörun reikninga viðskiptaskulda.
author: abruer
ms.date: 02/14/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5c93ba4a13dee32427f33fe9f33fda5d783501a7
ms.sourcegitcommit: 9740f9b41a7dcf1821c6baccb2e05b9865ac2966
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/15/2022
ms.locfileid: "9775327"
---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Setja upp sannprófun á Reikningsjöfnun viðskiptaskulda

[!include [banner](../../includes/banner.md)]

Áður en hafist er handa þarf að ganga úr skugga um að skilgreiningarlykill reikningsjöfnunar sé valinn. Ef þinn lögaðili rekur kostnað, eins og farm, með því að nota gjöld, skaltu tryggja að skilgreiningarlykillinn Gjöld sé valinn. Reikningsjöfnun viðskiptaskulda felst í því að bera saman reikning lánardrottins, innkaupapöntun og upplýsingar á fylgiseðli. Mismunur milli þessara skjala kallast misræmi í samsvörun. Misræmi er borinn saman við vikmörk sem tilgreind eru. Ef misræmi í samsvörun fer yfir vikmarkaprósentu eða upphæð, birtast tákn fyrir frávik samsvörunar á síðunni **Reikningur lánardrottins** og á síðunni **Samsvörunarupplýsingar reiknings**.

## <a name="determine-which-invoice-matching-validation-to-use"></a>Ákvarða hvaða staðfestingu á samsvörun reiknings skuli nota
Fjórar mismunandi gerðir staðfestingar á samsvörun eru tiltækar. 

- **Samsvörun á línustigi** – Algengasta gerð samsvörunar er línusamsvörun. Samsvörun á línustigi getur verið tvíhliða eða þríhliða samsvörun. Hægt er að tilgreina sjálfgefna samsvörun línustigs fyrir lögaðila á síðunni **Færibreyta viðskiptaskulda**. Tvíhliða samsvörun ber saman einingaverð á reikningi við einingaverð á innkaupapöntuninni. Þríhliða samsvörun ber að auki saman magn á reikningi við samsvarandi magn á vörukvittun.
- **Samtölur reiknings stemma** – Jafnaðu heildarupphæðir á reikningi við heildarupphæðir á innkaupapöntuninni. Þessi gerð af reikningsjöfnun inniheldur minnsta magn upplýsinga, svo hægt er að nota þennan valkost til að setja upp stýringar sem minnka tíma sem starfsmaður þarf til að skoða upplýsingar um reikningsjöfnun. Sex samtölur eru bornar saman, þ.m.t. Millisamtala, Heildarafsláttur, Gjöld, Söluskattur, Sléttun og Reikningsupphæð. Kerfið mun sannreyna hvort einhver þessara gilda á reikningnum víki frá áætluðu magni um meira en ásættanlegt frávik.
- **Gjöld stemma** – Jafnaðu upplýsingar um gjöld (upphæðir) á reikningi við upplýsingar um gjöld (upphæðir) á innkaupapöntun.
- **Verðsamtala fyrir samsvörun línuatriða** – Þessi gerð samsvörunar er gagnleg fyrir fyrirtæki sem venjulega fá marga reikninga fyrir eina línu innkaupapöntunar. Ef þú færð venjulega aðeins einn reikning á hverja línu innkaupapöntunar er þessi gerð samsvörunar ekki nauðsynleg. Þessi samsvörun krefst þess að tvíhliða eða þríhliða samsvörun sé virk og virkar sem staðfesting nettóupphæðar sem ekki má fara yfir, miðað við vikmörk og upphæðir. Þessi gerð samsvörunar ber saman upplýsingar um verð fyrir nettó upphæð á hverja línu á reikningi og öll í bið og áður bókaðar reikningslínur, með nettóupphæð samsvarandi innkaupapöntunarlínu. Nettóupphæðin ákvarðast af eftirfarandi formúlu: (einingarverð * línumagn) + línugjöld - línuafsláttur. Þegar verðsamtölur eru jafnaðar eftir prósentum verða gildin borin saman með því að nota viðskiptagjaldmiðilinn. Þegar samtölur verðs eru samsvaraðar eftir upphæð ber kerfið saman gildi með bókhaldsgjaldmiðlinum.

## <a name="set-up-parameters-to-enable-invoice-matching-validation"></a>Setja upp færibreytur til að virkja staðfestingu reikningsjöfnunar
1. Farðu í **Viðskiptaskuldir > Uppsetning > Færibreytur fyrir viðskiptaskuldir.**
2. Veldu flipann **Staðfesting reiknings**.
3. Merktu eða hreinsaðu gátreitinn **Virkja staðfestingu reikningsjöfnunar**.
    * Veldu hvort samþykkis er þörf áður en reikningur sem inniheldur misræmi fyrir reikningsjöfnun geti verið bókaður. Ef þetta er stillt á **Leyfa með viðvörun** mun birtast sjónræn lýsing þegar misræmi í reikningsjöfnun fer yfir vikmörk. Hins vegar muntu geta bóka reikninginn. Til að nota verkflæði með villuprófun á reikningsjöfnun skal tryggja að reiturinn **Bóka reikning með misræmi** sé stilltur á **Leyfa með viðvörun** til að komast hjá því að samþykkja mörgum sinnum.  
    * Í **Uppfærðu sjálfkrafa stöðu samsvörunar reikningshaus** reit, veldu hvort samsvörun verði framkvæmd sjálfkrafa við innslátt reikningsgagna. Ráðlögð stilling er **Já**, nema eru þú rekist á vandamál með innfærslu gagna. Með því að gera sjálfvirkar uppfærslur óvirkar má gera hraðar afköst kerfisins því villuprófun reikningsjöfnunar verður að sleppt við innfærslu gagna. Starfsmaður gagnainnfærslu þarf að uppfæra handvirkt jöfnunarstaða á reikningi til að sjá niðurstöður villuleitar fyrir reikningsjöfnun þegar þetta er stillt á **Nei**.  
4. Stilla **Samtölur reiknings stemma**.
5. Veldu eða hreinsaðu gátreitinn **Jafna samtölur reiknings** til að jafna raunverulegra samtölur reiknings með áætlaðar samtölur.
    * Veldu hvort tákn birtist ef ósamræmi í reikningsjöfnun fer yfir vikmörk. Þú getur valið að birta táknið þegar jákvætt misræmi fer yfir vikmörk, eða þegar annað hvort jákvætt eða neikvætt misræmi fer yfir vikmörk.  
    * Til dæmis vikmörkin er 5 prósent og heildarreikningsupphæð innkaupapöntunar er 100,00. Þess vegna jöfnunartákn verð birtist ef upp á 105,00 er hærri en upphæð heildarupphæð reiknings á reikningnum. Ef valið er **Ef meira en eða minna en vikmörk** birtist táknið einnig ef reikningsupphæð er lægra en 95,00.  
6. Í reitnum **Vikmarkaprósenta fyrir samtölur reiknings** skaltu slá inn þau hlutfallsfrávik sem eru viðunandi. Þetta gildi er sjálfgefið gildi fyrirtækisins. Þessu gildi er hægt að hnekkja fyrir tiltekna lánardrottna með því að nota síðuna **Vikmörk samtalna reiknings**. Fyrir upplýsingar um hvernig á að hnekkja vikmörkunarprósentu reikningsheilda fyrir tiltekinn lánardrottinn, sjá [Setja upp heildartölur reikninga sem passa við vikmörk fyrir lánardrottna](set-up-accounts-payable-invoice-matching-validation.md#set-up-invoice-totals-matching-tolerance-for-vendors) kafla síðar í þessari grein.
7. Stilltu **Samsvörun verðs og magns**.
8. Í reitnum **Línujöfnunarregla** skal velja gildi sem nota á sem sjálfgefna reglu fyrir lögaðilann sem unnið er með. **Ekki áskilið** þýðir að það er engin þörf á sannprófun fyrir einstaka verð reikningslínu við verð innkaupapöntunar eða magn reiknings við magn á fylgiseðlum. **Tvíhliða Jöfnun** þýðir að sannprófun reikningslína er áskilin en aðeins í innkaupapöntun og reikningsskjöl birgis eru höfð með í sannprófun. Innhreyfingarskjal afurða er ekki þáttur í samsvarandi villuleit. **Þríhliða Jöfnun** þýðir að nettó einingarverð reiknings verður borið saman við nettó einingaverð í innkaupapöntun og á samsvarandi magn á innhreyfingarskjali afurða verður borið saman við magn á reikningi.
9. Til að leyfa að mismunandi stig samsvörunar séu fyrir samsetninguna vöru, lánardrottinn, lánardrottinn og vöru eða innkaupapöntunarlínu, skaltu velja gildi í reitnum **Leyfa hnekkingu jöfnunarreglu**. Hægt er að hnekkja lögaðila línujöfnunarreglu fyrir tiltekinn lánardrottin, vöru eða lánardrottins og vörusamsetninguna á síðunni **Jöfnunarregla**.
    * Ef þú notar línusamsvörun stefnu um **Tvíhliða samsvörun** eða **Þríhliða samsvörun**, getur þú sett upp verðvikunarprósentur fyrir lögaðila þína, vörur og söluaðila á **Verðþol vöru** síðu. Sjálfgefin verðvikmörk lögaðila verða stillt á núll prósent fyrir tvíhliða og þríhliða samsvörun. Þegar lánardrottnareikningar eru bornir saman við upplýsingar á innkaupapöntun, er leitað að viðeigandi verðvikmarkaprósentum.   
10. Til að jafna samtölur verðs fyrir línuatriði á reikninga, veljið gildi í svæðinu **Jafna samtölur verðs**. Þessi gerð af samsvörun er gagnlegt ef lánardrottinn sendir marga reikninga fyrir sömu innkaupapöntunarlínunni. Hægt er að bera saman upplýsingar um verð fyrir nettó upphæð á hverja línu á reikningi og öll í bið og áður bókaðar reikningslínur, með nettóupphæð samsvarandi innkaupapöntunarlínu. Valkostir eru meðal annars **Ekkert**, **Hlutfall**, **Prósenta** eða **Prósenta og upphæð**.
11. Í reitnum **Vikmarkaprósenta samtölu innkaupaverðs** skaltu slá inn hlutfall af þeirra vikmarka sem þú getur samþykkt. Þessi reitur býðst þegar **Jafna samtölur verðs** er stillt á **Prósenta** eða **Prósenta og upphæð**.
12. Í reitnum **Vikmörk samtölu innkaupaverðs** skaltu slá inn upphæð í bókhaldsgjaldmiðlinum. Þessi reitur býðst þegar **Jafna samtölur verðs** er stillt á **Upphæð** eða **Prósenta og upphæð**.
13. Í reitnum **Birta jöfnunartákn fyrir samtölu verðs** skal velja þegar tákn birtist ef ósamræmi í reikningsjöfnun fer yfir vikmörk fyrir nettó einingaverð. Hægt er að birta á tákn jákvætt misræmi fer vikmörk, eða þegar jákvæð eða neikvæð misræmi fer vikmörk.
Til dæmis vikmörkin er 5 prósent og sem samtala innkaupapöntunar er 10,00. Þess vegna er jöfnunartákn birtist ef línu verð samtala reikningsins er yfir 10,50. Ef valið er **Ef meira en eða minna en vikmörk** birtist táknið einnig ef heildarverð línu á reikningi er lægri en 9,50.
13. Stilltu **Gjöld passa**.
14. Til að jafna raunveruleg gjöld við áætlu gjöld, á grundvelli upplýsinga á innkaupapöntun, veljið gátreitinn **Jafna gjöld**.

## <a name="set-up-unit-price-tolerance-percentages"></a>Vikmarkaprósentur einingaverðs settar upp
Farðu í **Viðskiptaskuldir > Uppsetning > Uppsetning reikningsjöfnunar > Verðvikmörk** til að skilgreina leyfilega prósentu verðvikmarka. Ef þú notar línusamsvörun stefnu um **Tvíhliða samsvörun** eða **Þríhliða samsvörun**, þú getur sett upp verðvikunarprósentur fyrir lögaðila, vörur og söluaðila. Þegar lánardrottnareikningar eru bornir saman við upplýsingar á innkaupapöntun, er leitað að viðeigandi verðvikmarkaprósentum. Eftirfarandi er sjálfgefin leitarröð:
* Tafla/Tafla
* Tafla/Hópur
* Tafla/Allt
* Hópur/Tafla
* Hópur/Hópur
* Hópur/Allt
* Allt/Tafla
* Allt/Hópur
* Allt/Allt

Sjálfgefin vikmörk verðs í lögaðilanum eru 0 prósent og þetta verðvikmörk eiga við allar vörur og lykla (Allt, Allt). Þú getur ekki eytt færslunni fyrir sjálfgefna verðvikmörk lögaðila.

Sjálfgefið er að neikvæð verðmisræmi eru leyfilegur. Hins vegar er ekki hægt að slá inn neikvæða tölu sem vikmörk verðprósentu. Til að rekja neikvæðar prósentur verðvikmarka skaltu velja **Ef hærra eða lægra en vikmörk** í reitnum **Birta jöfnunartákn fyrir einingarverð** á síðunni **Færibreytur viðskiptaskulda**. Sláðu síðan inn prósentu verðvikmarka á síðuna **Verðvikmörk**.

## <a name="set-up-matching-policy-override"></a>Sejt upp hnekkingu jöfnunarreglu

Fara til **Viðskiptaskuldir > Uppsetning > Uppsetning samsvörunar reikninga > Samsvörunarstefna** til að skilgreina sjálfgefna færslu fyrir **Samsvörunarstefna** reit fyrir línur í **Pöntun** síðu. Þetta er valfrjáls uppsetning. Notaðu þessa síðu til að setja upp tvíhliða samsvörun eða þríhliða samsvörun fyrir vörur, lánardrottna eða samsetningar vöru og lánardrottna. Þessar færslur gera þér kleift að skilgreina grófari jöfnunarreglur en jöfnunarregla lögaðila sem þú skilgreindir á síðunni **Færibreytur viðskiptaskulda**. Sjálfgefin jöfnunarregla línu lögaðila gildir um allar vörur og lánardrottna nema þau sem önnur jöfnunarregla línu er tilgreind fyrir á þessari síðu.

Á þessari síðu velurðu **Stig jöfnunarreglu**. Veldu stigið í stigveldi jöfnunarreglu sem stilla á jöfnunarreglur línu fyrir.

- **Vara og lánardrottinn** – Tilgreindu jöfnunarreglu fyrir tilteknar vörur sem eru keyptar af tilteknum lánardrottnum.
- **Vara** – Tilgreindu jöfnunarregla fyrir tilteknar vörur sem eru keyptar af hvaða lánardrottni sem er, nema þau sem tilgreind eru stigi vöru og lánardrottins.
- **Lánardrottinn** – Tilgreindu jöfnunarregla fyrir allar vörur sem eru keyptar af tilgreindum lánardrottnum sem er, nema þau sem tilgreind eru stigi vöru og lánardrottins.
  
Eftirfarandi stigveldi er notað til að ákvarða jöfnunarreglu sem er notuð:
  *  Vara og lánardrottinn
  *  vara
  *  Lánardrottinn
  *  Lögaðili
  
## <a name="set-up-invoice-totals-matching-tolerance-for-vendors"></a>Skilgreindu vikmörk fyrir samtölur reikningsjöfnunar fyrir lánardrottna

Farðu í **Viðskiptaskuldir > Uppsetning > Uppsetning reikningsjöfnunar > Vikmörk samtalna reiknings** til að tilgreina lánardrottnavikmörk fyrir jöfnun samtalna reiknings. Samsvarandi útreikningur notar prósentu vikmarka samtalna reiknings af reikningi lánardrottins sem er skilgreindur sem pöntunarreikningur á reikningi lánardrottins. Ef lánardrottinn reikningur hefur ekki tilgreint vikmarkaprósenta fyrir heildarreikninga, þá er vikmörk reikningsheilda sem er tilgreint fyrir lögaðilann í **Færibreytur viðskiptaskulda** síða er notuð.

1. Til að tilgreina vikmörk fyrir einstaka lánardrottna sem hnekkja sjálfgefnum vikmörkum skaltu velja **Lánardrottnalykill**.
2. Færa skal inn fráviksprósentu sem telst viðunandi fyrir þennan lánardrottinn.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
