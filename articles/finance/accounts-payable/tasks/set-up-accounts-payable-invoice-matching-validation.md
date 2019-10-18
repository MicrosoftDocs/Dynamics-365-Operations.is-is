---
title: Setja upp sannprófun á Reikningsjöfnun viðskiptaskulda
description: Þetta umræðuefni veitir upplýsingar um hvernig á að setja upp staðfestingu á reikningsjöfnun viðskiptaskulda.
author: abruer
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b048c49de7357ec1b5cbf36dd4f22a5d3efd443b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2189408"
---
# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Setja upp sannprófun á Reikningsjöfnun viðskiptaskulda

[!include [task guide banner](../../includes/task-guide-banner.md)]

Áður en hafist er handa þarf að ganga úr skugga um að skilgreiningarlykill reikningsjöfnunar sé valinn. Ef þinn lögaðili rekur kostnað, eins og farm, með því að nota gjöld, skaltu tryggja að skilgreiningarlykillinn Gjöld sé valinn.  Reikningsjöfnun viðskiptaskulda felst í því að bera saman reikning lánardrottins, innkaupapöntun og upplýsingar á fylgiseðli. Mismunur milli þessara skjala kallast misræmi í samsvörun. Misræmi er borinn saman við vikmörk sem tilgreind eru. Ef misræmi í samsvörun fer yfir vikmarkaprósentu eða upphæð, birtast tákn fyrir frávik samsvörunar á síðunni **Reikningur lánardrottins** og á síðunni **Samsvörunarupplýsingar reiknings**.

## <a name="determine-which-invoice-matching-validation-to-use"></a>Ákvarða hvaða staðfestingu á samsvörun reiknings skuli nota
Fjórar mismunandi gerðir staðfestingar á samsvörun eru tiltækar. 

- **Samsvörun á línustigi** – Algengasta gerð samsvörunar er línusamsvörun. Samsvörun á línustigi getur verið tvíhliða eða þríhliða samsvörun. Hægt er að tilgreina sjálfgefna samsvörun línustigs fyrir lögaðila á síðunni **Færibreyta viðskiptaskulda**. Tvíhliða samsvörun ber saman einingaverð á reikningi við einingaverð á innkaupapöntuninni. Þríhliða samsvörun ber að auki saman magn á reikningi við samsvarandi magn á vörukvittun.
- **Samtölur reiknings stemma** – Jafnaðu heildarupphæðir á reikningi við heildarupphæðir á innkaupapöntuninni. Þessi gerð af reikningsjöfnun inniheldur minnsta magn upplýsinga, svo hægt er að nota þennan valkost til að setja upp stýringar sem minnka tíma sem starfsmaður þarf til að skoða upplýsingar um reikningsjöfnun. Sex samtölur eru bornar saman, þ.m.t. Millisamtala, Heildarafsláttur, Gjöld, Söluskattur, Sléttun og Reikningsupphæð. Kerfið mun sannreyna hvort einhver þessara gilda á reikningnum víki frá áætluðu magni um meira en ásættanlegt frávik.
- **Gjöld stemma** – Jafnaðu upplýsingar um gjöld (upphæðir) á reikningi við upplýsingar um gjöld (upphæðir) á innkaupapöntun.
- **Verðsamtala fyrir samsvörun línuatriða** – Þessi gerð samsvörunar er gagnleg fyrir fyrirtæki sem venjulega fá marga reikninga fyrir eina línu innkaupapöntunar. Ef þú færð venjulega aðeins einn reikning á hverja línu innkaupapöntunar er þessi gerð samsvörunar ekki nauðsynleg. Þessi samsvörun krefst þess að tvíhliða eða þríhliða samsvörun sé virk og virkar sem staðfesting nettóupphæðar sem ekki má fara yfir, miðað við vikmörk og upphæðir.  Þessi gerð samsvörunar ber saman upplýsingar um verð fyrir nettó upphæð á hverja línu á reikningi og öll í bið og áður bókaðar reikningslínur, með nettóupphæð samsvarandi innkaupapöntunarlínu. Nettóupphæðin ákvarðast af eftirfarandi formúlu: (einingarverð * línumagn) + línugjöld - línuafsláttur. Þegar samtölur verðs eru samsvaraðar eftir prósentu ber kerfið saman gildi með færslugjaldmiðlinum. Þegar samtölur verðs eru samsvaraðar eftir upphæð ber kerfið saman gildi með bókhaldsgjaldmiðlinum.

## <a name="set-up-parameters-to-enable-invoice-matching-validation"></a>Setja upp færibreytur til að virkja staðfestingu reikningsjöfnunar
1. Farðu í **Viðskiptaskuldir > Uppsetning > Færibreytur fyrir viðskiptaskuldir.**
2. Veldu flipann **Staðfesting reiknings**.
3. Merktu eða hreinsaðu gátreitinn **Virkja staðfestingu reikningsjöfnunar**.
    * Veldu hvort samþykkis er þörf áður en reikningur sem inniheldur misræmi fyrir reikningsjöfnun geti verið bókaður. Ef þetta er stillt á **Leyfa með viðvörun** mun birtast sjónræn lýsing þegar misræmi í reikningsjöfnun fer yfir vikmörk. Hins vegar muntu geta bóka reikninginn. Til að nota verkflæði með villuprófun á reikningsjöfnun skal tryggja að reiturinn **Bóka reikning með misræmi** sé stilltur á **Leyfa með viðvörun** til að komast hjá því að samþykkja mörgum sinnum.  
    * Í reitnum **Uppfæra sjálfvirkt samsvörunarstöðu reikningshauss** skaltu velja hvort samsvörun verður framkvæmd sjálfvirkt við gagnafærslu á reikningum í kerfinu. Ráðlögð stilling er **Já**, nema eru þú rekist á vandamál með innfærslu gagna. Með því að gera sjálfvirkar uppfærslur óvirkar má gera hraðar afköst kerfisins því villuprófun reikningsjöfnunar verður að sleppt við innfærslu gagna. Starfsmaður gagnainnfærslu þarf að uppfæra handvirkt jöfnunarstaða á reikningi til að sjá niðurstöður villuleitar fyrir reikningsjöfnun þegar þetta er stillt á **Nei**.  
4. Stilla **Samtölur reiknings stemma**.
5. Veldu eða hreinsaðu gátreitinn **Jafna samtölur reiknings** til að jafna raunverulegra samtölur reiknings með áætlaðar samtölur.
    * Veldu hvort tákn birtist ef ósamræmi í reikningsjöfnun fer yfir vikmörk. Þú getur valið að birta táknið þegar jákvætt misræmi fer yfir vikmörk, eða þegar annað hvort jákvætt eða neikvætt misræmi fer yfir vikmörk.  
    * Til dæmis vikmörkin er 5 prósent og heildarreikningsupphæð innkaupapöntunar er 100,00. Þess vegna jöfnunartákn verð birtist ef upp á 105,00 er hærri en upphæð heildarupphæð reiknings á reikningnum. Ef valið er **Ef meira en eða minna en vikmörk** birtist táknið einnig ef reikningsupphæð er lægra en 95,00.  
6. Í reitnum **Vikmarkaprósenta fyrir samtölur reiknings** skaltu slá inn þau hlutfallsfrávik sem eru viðunandi. Þetta gildi er sjálfgefið gildi fyrirtækisins. Þessu gildi er hægt að hnekkja fyrir tiltekna lánardrottna með því að nota síðuna **Vikmörk samtalna reiknings**. Til að fá upplýsingar um hvernig á að hnekkja vikmörkum samtalna reiknings fyrir heildarvikmarkaprósentan fyrir tiltekinn lánardrottinn skaltu sjá hlutann „Setja upp vikmörk samtalna reiknings fyrir lánardrottna“ seinna í þessu efni.
7. Stilltu **Samsvörun verðs og magns**.
8. Í reitnum **Línujöfnunarregla** skal velja gildi sem nota á sem sjálfgefna reglu fyrir lögaðilann sem unnið er með. **Ekki áskilið** þýðir að það er engin þörf á sannprófun fyrir einstaka verð reikningslínu við verð innkaupapöntunar eða magn reiknings við magn á fylgiseðlum. **Tvíhliða Jöfnun** þýðir að sannprófun reikningslína er áskilin en aðeins í innkaupapöntun og reikningsskjöl birgis eru höfð með í sannprófun. Innhreyfingarskjal afurða er ekki þáttur í samsvarandi villuleit. **Þríhliða Jöfnun** þýðir að nettó einingarverð reiknings verður borið saman við nettó einingaverð í innkaupapöntun og á samsvarandi magn á innhreyfingarskjali afurða verður borið saman við magn á reikningi.
9. Til að leyfa að mismunandi stig samsvörunar séu fyrir samsetninguna vöru, lánardrottinn, lánardrottinn og vöru eða innkaupapöntunarlínu, skaltu velja gildi í reitnum **Leyfa hnekkingu jöfnunarreglu**. Hægt er að hnekkja lögaðila línujöfnunarreglu fyrir tiltekinn lánardrottin, vöru eða lánardrottins og vörusamsetninguna á síðunni **Jöfnunarregla**.
    * Ef þú notar línujöfnunarreglu tvíhliða samsvörunar eða þríhliða samsvörunar geturðu sett upp vikmarkaprósentur verðs fyrir lögaðila, vörur og lánardrottna á síðunni **Verðvikmörk vöru**. Sjálfgefin verðvikmörk lögaðila verða stillt á núll prósent fyrir tvíhliða og þríhliða samsvörun. Þegar lánardrottnareikningar eru bornir saman við upplýsingar á innkaupapöntun, er leitað að viðeigandi verðvikmarkaprósentum.   
10. Til að jafna samtölur verðs fyrir línuatriði á reikninga, veljið gildi í svæðinu **Jafna samtölur verðs**. Þessi gerð af samsvörun er gagnlegt ef lánardrottinn sendir marga reikninga fyrir sömu innkaupapöntunarlínunni. Hægt er að bera saman upplýsingar um verð fyrir nettó upphæð á hverja línu á reikningi og öll í bið og áður bókaðar reikningslínur, með nettóupphæð samsvarandi innkaupapöntunarlínu.  Valkostir eru meðal annars **Ekkert**, **Hlutfall**, **Prósenta** eða **Prósenta og upphæð**.
11. Í reitnum **Vikmarkaprósenta samtölu innkaupaverðs** skaltu slá inn hlutfall af þeirra vikmarka sem þú getur samþykkt. Þessi reitur býðst þegar **Jafna samtölur verðs** er stillt á **Prósenta** eða **Prósenta og upphæð**.
12. Í reitnum **Vikmörk samtölu innkaupaverðs** skaltu slá inn upphæð í bókhaldsgjaldmiðlinum. Þessi reitur býðst þegar **Jafna samtölur verðs** er stillt á **Upphæð** eða **Prósenta og upphæð**.
13. Í reitnum **Birta jöfnunartákn fyrir samtölu verðs** skal velja þegar tákn birtist ef ósamræmi í reikningsjöfnun fer yfir vikmörk fyrir nettó einingaverð. Hægt er að birta á tákn jákvætt misræmi fer vikmörk, eða þegar jákvæð eða neikvæð misræmi fer vikmörk.
Til dæmis vikmörkin er 5 prósent og sem samtala innkaupapöntunar er 10,00. Þess vegna er jöfnunartákn birtist ef línu verð samtala reikningsins er yfir 10,50. Ef valið er **Ef meira en eða minna en vikmörk** birtist táknið einnig ef heildarverð línu á reikningi er lægri en 9,50.
13. Stilla Gjöld stemma.
14. Til að jafna raunveruleg gjöld við áætlu gjöld, á grundvelli upplýsinga á innkaupapöntun, veljið gátreitinn **Jafna gjöld**.

## <a name="set-up-unit-price-tolerance-percentages"></a>Vikmarkaprósentur einingaverðs settar upp
Farðu í **Viðskiptaskuldir > Uppsetning > Uppsetning reikningsjöfnunar > Verðvikmörk** til að skilgreina leyfilega prósentu verðvikmarka. Ef þú notar línujöfnunarregla tvíhliða jöfnun eða þríhliða jöfnun, er hægt að setja vikmarkaprósentur verðs fyrir lögaðila, vörur og lánardrottna. Þegar lánardrottnareikningar eru bornir saman við upplýsingar á innkaupapöntun, er leitað að viðeigandi verðvikmarkaprósentum. Eftirfarandi er sjálfgefin leitarröð:
* Tafla/Tafla
* Tafla/Hópur
* Tafla/Allt
* Hópur/Tafla
* Hópur/Hópur
* Hópur/Allt
* Allt/Tafla
* Allt/Hópur
* Allt/Allt

Sjálfgefin vikmörk verðs í lögaðilanum eru 0 prósent og þetta verðvikmörk eiga við allar vörur og lykla (Allt, Allt). Ekki er hægt að eyða sjálfgefnum verðvikmörkum lögaðila fyrir færsluna.

Sjálfgefið er að neikvæð verðmisræmi eru leyfilegur. Hins vegar er hægt að færa inn neikvæða tölu sem prósentu verðumburðarlyndis. Til að rekja neikvæðar prósentur verðvikmarka skaltu velja **Ef hærra eða lægra en vikmörk** í reitnum **Birta jöfnunartákn fyrir einingarverð** á síðunni **Færibreytur viðskiptaskulda**. Sláðu síðan inn prósentu verðvikmarka á síðuna **Verðvikmörk**.

## <a name="set-up-matching-policy-override"></a>Sejt upp hnekkingu jöfnunarreglu

Farðu í **Viðskiptaskuldir > Uppsetning > Uppsetning reikningsjöfnunar > Jöfnunarregla** til að skilgreina sjálfgefna færslu fyrir reitinn Jöfnunarregla fyrir línur í innkaupapöntunarsniðinu. Þetta er valfrjáls uppsetning. Notaðu þetta eyðublað til að setja upp samsetningar á tvíhliða samsvörun eða þríhliða samsvörun fyrir vörur, lánardrottna eða vörur og birgja. Þessar færslur gera þér kleift að skilgreina grófari jöfnunarreglur en jöfnunarregla lögaðila sem þú skilgreindir á síðunni **Færibreytur viðskiptaskulda**. Sjálfgefin jöfnunarregla línu lögaðila gildir um allar vörur og lánardrottna nema þau sem önnur jöfnunarregla línu er tilgreind fyrir á þessari síðu.

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

Farðu í **Viðskiptaskuldir > Uppsetning > Uppsetning reikningsjöfnunar > Vikmörk samtalna reiknings** til að tilgreina lánardrottnavikmörk fyrir jöfnun samtalna reiknings. Samsvarandi útreikningur notar prósentu vikmarka samtalna reiknings af reikningi lánardrottins sem er skilgreindur sem pöntunarreikningur á reikningi lánardrottins. Ef reikningur lánardrottins hefur ekki tilgreint vikmarkaprósentu fyrir samtölu reiknings er vikmarkaprósenta samtalna reiknings sem tilgreind er fyrir lögaðilann á síðunni **Færibreytur viðskiptaskulda** notuð.

1. Til að tilgreina vikmörk fyrir einstaka lánardrottna sem hnekkja sjálfgefnum vikmörkum skaltu velja **Lánardrottnalykill**.
2. Færa skal inn fráviksprósentu sem telst viðunandi fyrir þennan lánardrottinn.
