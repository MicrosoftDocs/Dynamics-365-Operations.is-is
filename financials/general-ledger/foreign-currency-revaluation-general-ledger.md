---
title: "endurmat á erlendum gjaldmiðli fyrir fjárhag"
description: "Þetta efnisatriði gefur yfirlit yfir eftirfarandi fyrir erlendan gjaldmiðil endurmat fjárhagsferlið - uppsetning keyra ferlið útreikning fyrir ferli og hvernig á að bakfæra færslur endurmat, ef þörf krefur."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ef99caf4570969d2b920cec8b53669ce2094965
ms.openlocfilehash: 5d6d13fe44eef7766b4dcaf274c3522bce3da816
ms.lasthandoff: 03/31/2017


---

# <a name="foreign-currency-revaluation-for-general-ledger"></a>endurmat á erlendum gjaldmiðli fyrir fjárhag

Þetta efnisatriði gefur yfirlit yfir eftirfarandi fyrir erlendan gjaldmiðil endurmat fjárhagsferlið - uppsetning keyra ferlið útreikning fyrir ferli og hvernig á að bakfæra færslur endurmat, ef þörf krefur. 

Hluti af lok tímabils reikningsskilavenja krefjast stöður fjárhagslykils í erlendum gjaldmiðlum á að endurmetni nota annað gengi gerðir (gildandi, sögulegt,meðaltal o.s.frv.). Til dæmis, einn reikningsskilavenja krefst þess eignir og skuldir að endurmetni á gildandi gengi sem eignir á sögulegu gengi og rekstrarreikninga á mánaðarleg meðaltal. Endurmat á erlendum gjaldmiðli fjárhags má nota til að endurmeta efnahagsreikningur og rekstrarreikningur. 

> [!NOTE]
> Endurmat á erlendum gjaldmiðli er einnig tiltæk í (AR) viðskiptakröfur og viðskiptaskuldir (AP). Ef verið er að nota þessar einingar útistandandi færslur eiga að vera revalued með endurmat á erlendum gjaldmiðli í þessum kerfum. Viðskiptakröfur og viðskiptaskuldir endurmat á erlendum gjaldmiðli stofna bókhaldsfærsla í fjárhag til að endurspegla óinnleystur hagnaður eða tap, tryggja undirbók og fjárhag séu afstemmdar. Þar sem viðskiptakröfur og viðskiptaskuldir endurmat á erlendum gjaldmiðli stofna bókhaldsfærslur í fjárhag, viðskiptakröfur og viðskiptaskuldir aðallykla skuli undanskilin frá fjárhags endurmat á erlendum gjaldmiðli. 

Þegar keyrð er ferlið endurmat stöðu í hvern aðallykil sem bókaðar eru í erlendum gjaldmiðli endurmetinn. Óinnleystur hagnaður eða tap stofnaðar við endurmatsferli eru myndaðar af kerfinu. Tvær færslur hugsanlega stofnaðar, ein fyrir bókhaldsgjaldmiðli og aðra fyrir skýrslugjaldmiðill, ef við á. Hver lykilfærslu verður bókuð í óinnleystur hagnaður eða tap og aðallykil verið endurmetni.

## <a name="prepare-to-run-foreign-currency-revaluation"></a>Undirbúa keyrslu á endurmati á erlendum gjaldmiðli
eftirfarandi uppsetningar er krafist áður en endurmatsferlið er keyrt.

-   Á síðunni **Aðallykill**:
-   Fyrir hvern aðallykil sem ætti að vera endurmetið, veljið **endurmat á Erlendum gjaldmiðli**. Ef aðallykli ættu ekki að endurmetinn (eins og Viðskiptakröfur og viðskiptaskuldir ef endurmetin í undirbókum), hreinsa þennan valkost.
-   Ef aðallykils er merkt fyrir endurmat, færa inn **gengisgerð**. Verður nota þessa gerð gengis fyrir endurmat á aðallykilinn. Aðskilin svæði **Fjárhagslegar skýrslugerð gengisgerð**, er tiltækt fyrir fjárhagsskýrslugerð. Tvö svæði eru ekki haldið í samræmi, heimiluð fyrir mismunandi gengisgerðir sem nota á fyrir endurmat og fjárhagsskýrslugerð.

-   Á síðunni **fjárhagur**:
-   Tilgreinið **gengisgerð**. Ef gengisgerð er ekki tilgreind á aðallykilinn, þessa gerð gengis notað við endurmat á erlendum gjaldmiðli.
-   Tilgreinið innleystan hagnaður, innleyst tap, óinnleystur hagnaður og óinnleyst tap lyklar fyrir endurmat gjaldmiðils. Innleystur hagnaður og innleyst tap lyklar eru notaðir fyrir jafnaðar viðskiptakröfur og viðskiptaskuldir færslur og óinnleystur hagnaður og óinnleyst tap lyklar eru notaðir fyrir endurmat opnar færslur og aðallykla fjárhags.

-   Á síðunni **gjaldmiðilsendurmatslyklum**:
-   Veljið aðra gjaldmiðilsendurmatslykla fyrir hvern gjaldmiðil og fyrirtæki. Ef engin lyklar eru skilgreindir, eru lykla úr **Fjárhag** síðu notaðar.

## <a name="process-foreign-currency-revaluation"></a>Vinna endurmat á erlendum gjaldmiðli
Eftir uppsetningu er lokið er notuð **endurmat á Erlendum gjaldmiðli** síðu til að endurmeta stöður aðallykla. Hægt er að keyra ferlið í rauntíma eða raða til þess að keyra með því að nota runuvinnslu. 

Í **endurmat á Erlendum gjaldmiðli** síðu birtir sögu hverju ferli endurmat, þar á meðal þegar ferlið var keyrt hvaða skilyrðum var skilgreind tengil fylgiskjal stofnuð fyrir endurmatsins og færsla ef fyrri endurmat var bakfærð. Til að keyra endurmatsferlið , veljið **endurmat á Erlendum gjaldmiðli** hnappinn. 

Í **Frá dagsetningu** og ** Til Dagsetningu** gildi skilgreina dagsetningabil til að reikna út stöðu erlendum gjaldmiðli sem verður endurmeta. Þegar þú endurmetur hagnaðar og taplykla, fjárhæð allar færslur sem eiga sér stað á dagsetningabili eru endurmetni. Þegar efnahagslykla, endurmeta hunsaðar Frá dags. Í staðinn staða til að endurmetni ákvarðast af tímann frá byrjun fjárhagsárs að Til-dagsetning. 

Í **Gengisdagsetning** til að skilgreina dagsetningin sem gengið á sjálfgildi. Til dæmis er hægt að endurmeta stöður milli á dag afmörkun á Janúar 1 til 31. Janúar en nota gengi sem er skilgreind fyrir 1. Febrúar. 

Velja hvaða aðallykla til að endurmeta: Allt, efnahagsreikningur eða hagnaður og tap. Revalued mun eingöngu aðallyklar merkt fyrir endurmat (á síðu lykil Aðal). Ef óskað er að takmarka frekar þá aðallyklabil nota Færslurnar **til að taka með** flipa til að skilgreina afmörkun fyrir aðallykla eða einstaka aðallykla. 

Hægt er að keyra ferlið endurmat fyrir eina eða fleiri lögaðila. Uppfletting verður að birta aðeins lögaðila sem hafa aðgang. Velja lögaðila sem á að keyra vinnslu endurmats. 

Hægt að keyra endurmatsins fyrir einn eða fleiri erlendum gjaldmiðlum. Uppfletting felur í sér alla gjaldmiðla sem voru bókaðar í dagsetningarbili við tegund aðallykils (efnahagsreikningur eða rekstur) lögaðila sem valinn til að endurmeta. Bókhaldsgjaldmiðill verða teknar með í listanum en ekkert verður revalued ef valinn er í bókhaldsgjaldmiðli. 

Setja **Forskoðun fyrir bókun** að **Já** ef óskað er að endurskoða niðurstöður endurmat fjárhagsins. Forskoðun í fjárhag er annað en hermun í Viðskiptakröfur og AP endurmat á erlendum gjaldmiðli. Hermun í Viðskiptakröfur og AP er skýrsla en fjárhagsins hefur forskoðun sem hægt er að bóka, án þess að þurfa að keyra endurmat ferlið aftur. Hægt er að flytja út niðurstöður forskoðun í Microsoft Excel til að geyma sögu hvernig upphæðir voru reiknaðar. Hægt er að nota runuvinnslu ef á að forskoða niðurstöður á endurmati. Úr forskoðun notandi hefur valkost að bóka niðurstöður fyrir alla lögaðila með **Bóka** hnappinn. Ef vandamál með niðurstöðum fyrir lögaðili notandi hefur einnig valkostinn til að bóka hlutmengi lögaðila með **Veldu lögaðila til að bóka** hnappinn. 

Eftir að ferli endurmat á erlendum gjaldmiðli er lokið er færsla stofnuð til að rekja sögu hverri keyrslu.  Sérstök færsla verður stofnuð fyrir hvern lögaðila og bókunarlag.

## <a name="calculate-unrealized-gainloss"></a>Reikna óinnleystur hagnaður/tap
Óinnleystur hagnaður/tap færslur eru stofnaðar mismunandi milli fjárhags endurmat og Viðskiptakröfur og viðskiptaskuldir endurmat ferlið. Viðskiptakröfur og viðskiptaskuldir fyrri endurmats er alveg bakfærð (gert er ráð fyrir færslan ekki enn jafna) og nýja endurmatsfærsla stofnuð sem óinnleystur hagnaður/tap byggðar á nýju gengi fyrir. Þetta er vegna þess að hverrar einstakrar færslu í Viðskiptakröfur og viðskiptaskuldir endurmeta. Í fjárhag, fyrri endurmat er ekki bakfærðar. Í staðinn er færsla stofnuð fyrir delta milli stöðu aðallykils, þ.m.t. allar fyrri endurmatsupphæða og byggt á gengi fyrir Dagsetningu á Gengi í nýja gildið. 

**Dæmi** eftirfarandi stöður eru til fyrir aðallykilinn 110110.

|            |                    |                        |                       |
|------------|--------------------|------------------------|-----------------------|
| **Dagsetning**   | **Fjárhagslykill** | **Færsluupphæð** | **Upphæð á lykil** |
| 20. janúar | 110110 (reiðufé)      | 500 EUR (Debet)        | 1000 USD (Debet)      |

Aðallykils er endurmetni 31. Janúar.  Óinnleystur hagnaður/tap er reiknuð á eftirfarandi hátt.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Núverandi staða í færslugjaldmiðli** | **Núverandi staða í bókhaldsgjaldmiðli** | **Gengi við endurmati** | **ný Upphæð í bókhaldsgjaldmiðli** | **Óinnleystur hagnaður/tap**    |
| 500 EUR                                     | 1000 USD                                   | 166.6667                         | 833.33 EUR (500 x 1.666667)        | 166.67 tap (833.33 – 1000) |

Eftirfarandi lykilfærslu er stofnuð.

|            |                          |           |            |
|------------|--------------------------|-----------|------------|
| **Dagsetning**   | **Fjárhagslykill**       | **Debet** | **Kredit** |
| 31. janúar | 110110 (reiðufé)            |           | 166.67     |
| 31. janúar | 801400 (óinnleyst tap) | 166.67    |            |

Engar nýjar færslur eru bókaðar fyrir Febrúar.  Aðallykils er endurmetni á 28. Febrúar.

|                                             |                                            |                                  |                                    |                             |
|---------------------------------------------|--------------------------------------------|----------------------------------|------------------------------------|-----------------------------|
| **Núverandi staða í færslugjaldmiðli** | **Núverandi staða í bókhaldsgjaldmiðli** | **Gengi við endurmati** | **ný Upphæð í bókhaldsgjaldmiðli** | **Óinnleystur hagnaður/tap**    |
| 500 EUR                                     | 833.33 USD (1000 - 166.67)                 | 250.0000                         | 1250 USD (500 x 2,5)               | 416.67 hagnaður (1250 – 833.33) |

Eftirfarandi lykilfærslu er stofnuð.

|             |                          |           |            |
|-------------|--------------------------|-----------|------------|
| **Dagsetning**    | **Fjárhagslykill**       | **Debet** | **Kredit** |
| 28. febrúar | 110110 (reiðufé)            | 416.67    |            |
| 28. febrúar | 801600 (óinnleystur hagnaður) |           | 416.67     |

## <a name="reverse-foreign-currency-revaluation"></a>Bakfæra endurmats á erlendum gjaldmiðli
Ef nauðsynlegt er að bakfæra endurmatsfærsluna velja **Bakfæra færslu** hnappinn á **endurmat á Erlendum gjaldmiðli** síðu. Ný Erlendum gjaldmiðli endurmat söguleg færsla stofnuð til að viðhalda sögulegum endurskoðunarslóð þegar endurmatsins átti sér stað eða var bakfærð. 

Hægt er að bakfæra niðurstöður endurmat dagsetning innkaupapöntunar utan, en gæti þurft að bakfæra meira gildandi endurmat til að tryggja að rétt stöður fyrir hvern aðallykil endurmetni einnig. Fyrir bakfærslur getur átt sér stað útrunnin pöntun þar sem það er engin leið til að stjórna hvaða aðallyklar eru endurmetni og tíðni þegar endurmetnað. Til dæmis gæti fyrirtæki valið til að endurmeta þeirra reiðufé aðallykla ársfjórðungslega, en allar aðrar aðallykla mánaðarlega.


