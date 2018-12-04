---
title: "Endurmat á erlendum gjaldmiðli fyrir viðskiptakröfur og viðskiptaskuldir"
description: "Gengissveiflur valda því að fræðilegt gildi (bókfært verð) opinna færsla í erlendum gjaldmiðli eru mismunandi frá tíma til tíma. Þessi grein gefur upplýsingar um ferlið endurmat á erlendum gjaldmiðli sem keyrt er til að uppfæra virði opinna færslna í Viðskiptaskuldum og Viðskiptakröfum."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustExchRateAdjustment, VendExchRateAdjustment
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14211
ms.assetid: defb1ea5-1f3e-4859-87d8-3f9954d3f388
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 259b487b0f11b19af9609d63f12114dcaa61be52
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="foreign-currency-revaluation-for-accounts-payable-and-accounts-receivable"></a>Endurmat á erlendum gjaldmiðli fyrir viðskiptakröfur og viðskiptaskuldir

[!include [banner](../includes/banner.md)]

Gengissveiflur valda því að fræðilegt gildi (bókfært verð) opinna færsla í erlendum gjaldmiðli eru mismunandi frá tíma til tíma. Þessi grein gefur upplýsingar um ferlið endurmat á erlendum gjaldmiðli sem keyrt er til að uppfæra virði opinna færslna í Viðskiptaskuldum og Viðskiptakröfum. 

Fræðilegt gildi, eða bókað virði, opinnar færslu í erlendum gjaldmiðlum breytist með tímanum vegna gengisbreytinga. Til uppfæra gildi opinna færslna viðskiptaskuldir og viðskiptakröfur, skal keyra ferlið endurmat á erlendum gjaldmiðli. Endurmat á erlendum gjaldmiðli er hægt að keyra bæði fyrir viðskiptakröfur og viðskiptaskuldir Ferlið notar á nýtt gengi til að endurmeta opnar upphæðir, eða ójafnaðar upphæðir, á tiltekinni dagsetningu. Mismunur á milli upphaflegu bókaðar upphæðir og endurmetnu upphæðir veldur óinnleystum hagnaði eða tapi fyrir hverja opna færslu. Undirbækur viðskiptaskulda og viðskiptakrafa er síðan uppfærð til að endurspegla óinnleystan hagnaður eða tap, og bókhaldsfærsla er bókuð í fjárhag.

## <a name="simulate-a-foreign-currency-revaluation"></a>Líkja eftir endurmati á erlendum gjaldmiðli
Áður en þú endurmeta upphæðir í erlendum gjaldmiðli í opnum færslum, er hægt að keyra skýrsluhermun fyrir endurmat á erlendum gjaldmiðli fyrir sömu dagsetningu og aðferð. Til að keyra á skýrslunahermun, í **endurmat á Erlendum gjaldmiðli** síðunni er smellt á **Hermun** hnappinn. Skýrslan veitir forskoðun á upphæð óinnleysts hagnaðar eða taps, samkvæmt færibreytum sem eru skilgreindar fyrir hermunina.

## <a name="process-a-foreign-currency-revaluation"></a>Vinna endurmat á erlendum gjaldmiðli
Notið **Endurmat á erlendum gjaldmiðli** síðuna undir **Reglubundin verkefni** til að endurmat opnar færslur. Hægt er að keyra ferlið í rauntíma eða raða til þess að keyra með því að nota runuvinnslu. Hægt er að keyra ferlið í rauntíma eða áætla keyrslu með því að nota runuvinnslu. Þegar þú Skilgreina stillingar fyrir endurmatsferlið, þarf að vera viss um hvort eigi að prenta skýrslu um niðurstöður. Ekki er hægt að endurprenta endurmatsskýrslu eftir að ferlinu er lokið. Ef þú myndar skýrslu um endurmat á erlendum gjaldmiðli sýnir hún mismunandi stöður í stigi viðskiptavinar/lánardrottins og á stigi gjaldmiðils:

-   Stöður viðskiptavina eða lánardrottna sem hafa færslur í erlendum gjaldmiðli sem hafa verið endurmetnar. Eftirfarandi stöður eru sýndar:
    -   Upphafleg heildarstaða í erlendum gjaldmiðli.
    -   Heildarupphæð í erlendum gjaldmiðli í bókhaldsgjaldmiðli, frá og með fyrra endurmati.
    -   Heildarupphæð í erlendum gjaldmiðli í bókhaldsgjaldmiðli, frá og með núverandi endurmati.
    -   Mismunurinn milli núverandi og fyrri endurmats. Þessi mismunurinn er viðbótar óinnleystur hagnaður eða tap.
-   Samtals óinnleystur hagnaður eða tap fyrir hvern gjaldmiðil.

Skrá er haldin yfir hvert skipti sem endurmat á erlendum gjaldmiðli er keyrð. Úr færslunni á **mat á Erlendum gjaldmiðli** síðu, skal velja **Færslur** til að skoða nákvæman lista yfir færslur sem voru stofnaðar vegna endurmatsins. Hvert fylgiskjal færslu stendur fyrir opna færslu sem var endurmetin. Ef opinni færslu var endurmetin oftar en einu sinni, sjást tvær færslur sem nota sama fylgiskjal. Ein færsla verður fyrir bakfærslu fyrri óinnleysts hagnaður eða taps, og önnur færsla verður fyrir nýja óinnleysta hagnaðinn eða tapið. Til að keyra endurmatsferlið , smellið á **endurmat á Erlendum gjaldmiðli** hnappinn. Skilgreina viðeigandi stillingar fyrir eftirfarandi færibreytur:

-   **Aðferð** - Aðferðin sem notuð var í vinnslu á völdu endurmats á erlendum gjaldmiðli .
    -   **Staðlað** - vinnslur endurmats á erlendum gjaldmiðli eru bókaðar óháð því hvort niðurstaðan er hagnaður eða tap.
    -   **Lágmarks** vinnslur endurmats á erlendum gjaldmiðli eru eingöngu bókaðar ef niðurstaðan er tap.
    -   **Reiknigsdagsetning**vinnsla endurmats á erlendum gjaldmiðli notar upprunalegt gengi færslnanna, sem eru endurmetnar samkvæmt upprunalegu gildi þeirra í bókhaldsgjaldmiðli. Áhrif allra fyrri endurmat á erlendum gjaldmiðli er hætt við.
-   **Viðmiðunardagsetning** - Dagsetning þegar allar færslur sem hafa opnar (ekki jafnaðar) upphæðir á þeirri dagsetningu eru fundnar. Upphæðir í erlendum gjaldmiðli er endurmetnar með því gengi sem ert fært inn á síðunni **gengi Gjaldmiðils** fyrir viðmiðunardagsetninguna. Þegar upphæðir í erlendum gjaldmiðli er endurmetnar á viðmiðunardagsetningu, verður þessi dagsetning síðasta dagsetning endurmats á erlendum gjaldmiðli fyrir færslur sem eru lagfærðar. Ef ákveðið er að keyra endurmat á erlendum gjaldmiðli fyrir viðmiðunardagsetninguna sem er á undan síðustu dagsetningu endurmats á erlendum gjaldmiðli á færslum sem þegar hafa verið leiðréttar, eru færslur sem voru opnar á fyrri skoðunardagsetningunni en sem hafa nýrri síðustu dagsetningu endurmats á erlendum gjaldmiðli ekki leiðréttar með reglubundnu vinnslunni.
-   **Dagsetning gengis** - Dagsetning sem ákvarðar það gengi sem notað er við færslu endurmats á erlendum gjaldmiðli.
-   **Nota bókunarreglu úr** – bókunarregla sem er notuð til að færa inn sjálfgefinn aðallykil fyrir viðskiptakröfur eða Viðskiptaskuldir fyrir bókhaldsfærslur fyrir færslur endurmats á erlendum gjaldmiðli:
    -   **Bókun** – Bókunarregla viðskiptavinafærslunnar er notuð.
    -   **Velja** – færið inn bókunarregluna á svæðinu **bókunarregla**.
-   **Bókunarregla** - **velja** er valið í svæðinu **Nota bókunarreglu úr** ákvarðar bókunarreglan sem þú færir inn í þessum reit bókunarreglu færslu fyrir endurmat á erlendum gjaldmiðli.
-   **Fjárhagsvíddir** - fjárhagsvíddarinnar sem eru bókaðar á bókhaldsfærslur fyrir færslur fyrir endurmat á erlendum gjaldmiðli.
    -   **Ekkert** – Engar fjárhagsvíddir eru bókaðar. Ef þú ert með áskilda fjárhagsvídd í lykilskipulagi þínu, er endumatsferlið samt keyrt og stofnar bókhaldsfærslur sem hafa engar fjárhagsvíddir. Þér mun berast viðvörunarskilaboð fyrst, þannig að hægt er að hætta við endurmatið.
    -   **Tafla** fjárhagsvíddir viðskiptavinalykils eða lánardrottnalykils eru bókaðar á færslur fyrir endurmat á erlendum gjaldmiðli.
    -   **Bókun** fjárhagsvíddir færslunnar sem er verið að endurmeta eru bókaðar á færslur fyrir endurmat á erlendum gjaldmiðli. Sjálfgefið er að fjárhagsvíddir úr fjárhagslykli AR/AP upprunalegra færsla verða notaðar fyrir AR/AP aðallykil fyrir endurmatsfærsluna, og fjárhagsvíddir úr fjárhagslykli eigna/kostnaðar/tekna fyrir upprunalegu færsluna verða notaðar fyrir óinnleystan aðallykil hagnaðar/taps/ fyrir  endurmatsfærsluna.





