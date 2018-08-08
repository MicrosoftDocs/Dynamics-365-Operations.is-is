--- 
title: "Setja upp villuleit fyrir reikningsjöfnun viðskiptaskulda"
description: "Þessi skráning notar sýnigögn USMF fyrirtækis"
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e9bf83269c34133509734691fd018ee703c40626
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="set-up-accounts-payable-invoice-matching-validation"></a>Setja upp villuleit fyrir reikningsjöfnun viðskiptaskulda

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi skráning notar sýnigögn USMF fyrirtækis hlutverk viðskiptaskuldastjóri eða aðalbókari myndi framkvæma þessi skrefum. Áður en hafist er handa þarf að ganga úr skugga um að skilgreiningarlykill reikningsjöfnunar sé valinn. Ef þinn lögaðili rekur kostnað, eins og farm, með því að nota gjöld, skaltu tryggja að skilgreiningarlykillinn Gjöld sé valinn.  Reikningsjöfnun viðskiptaskulda felst í því að bera saman reikning lánardrottins, innkaupapöntun og upplýsingar á fylgiseðli. Mismunur milli þessara skjala kallast misræmi í samsvörun. Misræmi er borinn saman við vikmörk sem tilgreind eru. Ef jöfnunarmisræmi fer yfir vikmarkaprósenta eða upphæð, birtast stemma frávikstákn í skjámyndinni reikningur Lánardrottins og skjámynd upplýsingar reikningsjöfnunar.

1. Fara í Viðskiptaskuldir > Uppsetning > Færibreytur viðskiptaskulda.
2. Smellið á flipann Staðfesting reiknings.
3. Merkja eða afmerkja gátreitinn Virkja villuleit reikningsjöfnunar.
    * Veldu hvort samþykkis er þörf áður en reikningur sem inniheldur misræmi fyrir reikningsjöfnun geti verið bókaður. Ef þetta er stillt til að Leyfa með viðvörun, mun birtast sjónræn lýsing þegar misræmi í reikningsjöfnun fer yfir vikmörk. Hins vegar muntu geta bóka reikninginn. Til að nota verkflæði með villuprófun á reikningsjöfnun skal tryggja að Bóka reikning með misræmi svæðið er stillt til að Leyfa með viðvörun til að komast hjá því að samþykkja mörgum sinnum.  
    * Í svæðinu uppfæra Sjálfvirkt stöðusvæði samsvörunar fyrir fyrirsögn reiknings skal velja hvort samsvörun verður framkvæmd sjálfvirkt við gagnafærslu á reikningum í kerfinu. Ráðlögð stilling er Já, nema eru þú rekist á vandamál með innfærslu gagna. Með því að gera sjálfvirkar uppfærslur óvirkar má gera hraðar afköst kerfisins því villuprófun reikningsjöfnunar verður að sleppt við innfærslu gagna. Starfsmaður gagnainnfærslu þarf að uppfæra handvirkt jöfnunarstaða á reikningi til að sjá niðurstöður villuleitar fyrir reikningsjöfnun þegar þetta er stillt á nei.  
4. Víxla útvíkkun á liðnum samtölur reiknings stemma.
5. Merkja eða afmerkja gátreit Jafna samtölur reiknings til að jafna raunverulegra samtölur reiknings með áætlaðar samtölur.
    * Veldu hvort tákn birtist ef ósamræmi í reikningsjöfnun fer yfir vikmörk. Þú getur valið að birta táknið þegar jákvætt misræmi fer yfir vikmörk, eða þegar annað hvort jákvætt eða neikvætt misræmi fer yfir vikmörk.  
    * Til dæmis vikmörkin er 5 prósent og heildarreikningsupphæð innkaupapöntunar er 100,00. Þess vegna jöfnunartákn verð birtist ef upp á 105,00 er hærri en upphæð heildarupphæð reiknings á reikningnum. Ef valið er Ef meira en eða minna en vikmörk, birtist táknið einnig ef reikningsupphæð er lægra en 95,00.  
6. Í reitnum vikmarkaprósenta samtölu Reiknings, færið inn númer.
7. Víxla útvíkkun á við jöfnun Verðs og magns hluta.
    * Í línujöfnunarregla skal velja gildi sem nota á sem sjálfgefna reglu fyrir lögaðilann sem unnið er með. "Ekki áskilið" þýðir að það er engin þörf á sannprófun fyrir einstaka verð reikningslínu við verð innkaupapöntunar eða magn reiknings við magn á fylgiseðlum. "Tvíhliða Jöfnun" þýðir að sannprófun reikningslína er áskilin en aðeins í innkaupapöntun og reikningsskjöl birgis eru höfð með í sannprófun. Innhreyfingarskjal afurða er ekki þáttur í samsvarandi villuleit. "Þríhliða Jöfnun" þýðir að nettó einingarverð reiknings verður borið saman við nettó einingaverð í innkaupapöntun og á samsvarandi magn á innhreyfingarskjali afurða verður borið saman við magn á reikningi.  
    * Ef þú notar línujöfnunarregla tvíhliða jöfnun eða þríhliða jöfnun, er hægt að setja vikmarkaprósentur verðs fyrir lögaðila, vörur og lánardrottna á síðu verðvikmörk Vöru. Þegar lánardrottnareikningar eru bornir saman við upplýsingar á innkaupapöntun, er leitað að viðeigandi verðvikmarkaprósentum.  
8. Veljið valkost í reitnum línujöfnunarregla
    * Til að leyfa mismunandi stig samsvörunar að vera notuð fyrir vöru, lánardrottinn, samsetningu lánardrottins og vöru eða innkaupapöntunarlínu, veljið gildi í svæðinu Leyfa hnekkingu jöfnunarreglu. Hægt er að hnekkja lögaðila línujöfnunarreglu fyrir tiltekinn lánardrottin, vöru eða lánardrottins og vörusamsetninguna á síðunni jöfnunarregla.  
    * Til að jafna samtölur verðs fyrir línuatriði á reikninga, veljið gildi í svæðinu samtala verðsamsvörunar. Þessi gerð af samsvörun er gagnlegt ef lánardrottinn sendir marga reikninga fyrir sömu innkaupapöntunarlínunni. Hægt er að bera saman upplýsingar um verð fyrir nettó upphæð á hverja línu á reikningi og öll í bið og áður bókaðar reikningslínur, með nettóupphæð samsvarandi innkaupapöntunarlínu.  
9. Veljið valkost í samtölur verðsamræmis svæðið.
10. Færið inn tölu í svæðið samtala innkaupaverðs.
11. Víxla útvíkkun á liðnum gjöld stemma.
12. Til að jafna raunveruleg gjöld við áætlu gjöld, á grundvelli upplýsinga á innkaupapöntun, veljið gátreitinn jafna gjöld.
13. Lokið síðunni.


