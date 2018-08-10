---
title: "endurmat á erlendum gjaldmiðli fyrir fjárhag"
description: "Í þessu efnisatriði gefur yfirlit yfir eftirfarandi ferli endurmat á erlendum gjaldmiðli fjárhags: uppsetningu keyra ferlið útreikning fyrir ferli og hvernig á að bakfæra færslur endurmat, ef þörf krefur."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CurrencyLedgerGainLossAccount
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 62153
ms.assetid: 842e8561-560f-4cc6-8668-70cca60b1ba3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: f967854e9a39c7b2d76559744bbc1e16a53d7f6a
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="foreign-currency-revaluation-for-general-ledger"></a>endurmat á erlendum gjaldmiðli fyrir fjárhag

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði gefur yfirlit yfir eftirfarandi ferli endurmat á erlendum gjaldmiðli fjárhags: uppsetningu keyra ferlið útreikning fyrir ferli og hvernig á að bakfæra færslur endurmat, ef þörf krefur. 

Hluti af lok tímabils reikningsskilavenja krefjast stöður fjárhagslykils í erlendum gjaldmiðlum á að endurmetni nota annað gengi gerðir (gildandi, sögulegt,meðaltal o.s.frv.). Til dæmis, einn reikningsskilavenja krefst þess eignir og skuldir að endurmetni á gildandi gengi sem eignir á sögulegu gengi og rekstrarreikninga á mánaðarleg meðaltal. Endurmat á erlendum gjaldmiðli fjárhags má nota til að endurmeta efnahagsreikningur og rekstrarreikningur. 

> [!NOTE]
> Endurmat á erlendum gjaldmiðli er einnig tiltæk í (AR) viðskiptakröfur og viðskiptaskuldir (AP). Ef verið er að nota þessar einingar útistandandi færslur eiga að vera endurmetnar með endurmat á erlendum gjaldmiðli í þessum einingum. Viðskiptakröfur og viðskiptaskuldir endurmat á erlendum gjaldmiðli stofna bókhaldsfærsla í fjárhag til að endurspegla óinnleystur hagnaður eða tap, tryggja undirbók og fjárhag séu afstemmdar. Þar sem viðskiptakröfur og viðskiptaskuldir endurmat á erlendum gjaldmiðli stofna bókhaldsfærslur í fjárhag, viðskiptakröfur og viðskiptaskuldir aðallykla skuli undanskilin frá fjárhags endurmat á erlendum gjaldmiðli. 

Þegar keyrð er ferlið endurmat stöðu í hvern aðallykil sem bókaðar eru í erlendum gjaldmiðli endurmetinn. Óinnleystur hagnaður eða tap stofnaðar við endurmatsferli eru myndaðar af kerfinu. Tvær færslur hugsanlega stofnaðar, ein fyrir bókhaldsgjaldmiðli og aðra fyrir skráð verð ef það á við. Hver lykilfærslu verður bókuð í óinnleystur hagnaður eða tap og aðallykil endurmetinn.

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

Í **Frá dagsetningu** og **Til Dagsetningu** gildi skilgreina dagsetningabil til að reikna út stöðu erlendum gjaldmiðli sem verður endurmeta. Þegar þú endurmetur hagnaðar og taplykla, fjárhæð allar færslur sem eiga sér stað á dagsetningabili eru endurmetni. Þegar efnahagslykla, endurmeta hunsaðar Frá dags. Í staðinn staða til að endurmetni ákvarðast af tímann frá byrjun fjárhagsárs að Til-dagsetning. 

**Gengisdagsetning** hægt að nota til að skilgreina dagsetningin sem gengið setja á sjálfgildi. Til dæmis er hægt að endurmeta stöður milli dagsetning afmörkun fyrir Janúar 1 til 31. Janúar en nota gengi sem er skilgreind fyrir 1. Febrúar. 

Velja hvaða aðallykla til að endurmeta: Allt, efnahagsreikningur eða hagnaður og tap. Eingöngu aðallyklar merktar fyrir endurmat (á síðu lykil Aðal) er endurmetið. Ef óskað er að takmarka svið aðallykla frekar er hægt að nota Færslurnar **sem taka á með** flipa til að skilgreina afmörkun fyrir aðallykla eða einstaka aðallykla. 

Hægt er að keyra ferlið endurmat fyrir einn eða fleiri lögaðila. Uppfletting mun birta aðeins lögaðila sem þú hafa aðgang að. Velja lögaðila sem á að keyra vinnslu endurmats. 

Hægt að keyra endurmatsins fyrir einn eða fleiri erlendum gjaldmiðlum. Uppfletting mun innihalda alla gjaldmiðla sem voru bókaðir innan dagsetningabilsins fyrir tegund aðallykils (efnahagsreikningur eða rekstur) lögaðila sem valinn til að endurmeta. Bókhaldsgjaldmiðill hafðar með í listanum en ekkert mun vera endurmetið ef valinn er bókhaldsgjaldmiðli. 

Setja **Forskoðun fyrir bókun** á **Já** ef óskað er að endurskoða niðurstöður endurmats fjárhags. Forskoðun í fjárhag er annað en hermun í Viðskiptakröfur og viðskiptaskuldir endurmat á erlendum gjaldmiðli. Hermun í Viðskiptakröfur og viðskiptaskuldir er skýrslu, en fjárhagur hefur forskoðun sem er hægt að bóka, án þess að þurfa til þess að keyra endurmat ferlið aftur. Hægt er að flytja út niðurstöður forskoðun í Microsoft Excel til að geyma sögu hvernig upphæðir voru reiknaðar. Hægt er að nota runuvinnslu ef á að forskoða niðurstöður á endurmati. Úr forskoðun notandi hefur valkost að bóka niðurstöður fyrir alla lögaðila með **Bóka** hnappinn. Ef vandamál með niðurstöðum fyrir lögaðili notandi hefur einnig valkostinn til að bóka hlutmengi lögaðila með **Veldu lögaðila til að bóka** hnappinn. 

Eftir að ferli endurmat á erlendum gjaldmiðli er lokið færsla stofnuð að rekja sögu hverja keyrslu.  Sérstök færsla verður stofnuð fyrir hvern lögaðila og bókunarlag.

## <a name="calculate-unrealized-gainloss"></a>Reikna óinnleystur hagnaður/tap
Óinnleystur hagnaður/tap færslur eru stofnaðar mismunandi milli fjárhags endurmat og Viðskiptakröfur og viðskiptaskuldir endurmat ferlið. Viðskiptakröfur og viðskiptaskuldir fyrri endurmats er alveg bakfærð (gert er ráð fyrir færslan ekki enn jafna) og nýja endurmatsfærsla stofnuð sem óinnleystur hagnaður/tap byggðar á nýju gengi fyrir. Þetta er vegna þess að hverrar einstakrar færslu í Viðskiptakröfur og viðskiptaskuldir endurmeta. Í Fjárhagur er fyrra endurmat ekki snúið við. Í staðinn er færsla stofnuð fyrir delta milli stöðu aðallykils, þar á meðal allar fyrri endurmat upphæðum og nýtt gildi byggt á gengi fyrir Dagsetningu gengis. 

**Dæmi** Eftirfarandi stöður eru til fyrir aðallykilinn 110110.

|            |                    |                        |                       |
|------------|--------------------|------------------------|-----------------------|
| **Dagsetning**   | **Fjárhagslykill** | **Færsluupphæð** | **Upphæð á lykil** |
| 20. janúar | 110110 (reiðufé)      | 500 EUR (Debet)        | 1000 USD (Debet)      |

Aðallykill er endurmetinn 31. Janúar.  Óinnleystur hagnaður/tap er reiknuð á eftirfarandi hátt.

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

Engar nýjar færslur eru bókaðar fyrir Febrúar.  Aðallykill er endurmetinn á 28. Febrúar.

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

Hægt er að bakfæra Niðurstöður endurmat í rangri dagsetningaröð, en það gæti þurft að bakfæra einnig nýrra endurmat til að tryggja rétta stöðu fyrir hvern endurmetinn aðallykil. Bakfærslur geta orðið í rangri dagsetningaröð þar sem það er engin leið til að stjórna hvaða aðallyklar eru endurmetni og tíðni þegar endurmetnað. Til dæmis fyrirtæki gæti ákveðið að endurmeta þeirra reiðufé aðallykla ársfjórðungslega, en allar aðrar aðallykla mánaðarlega.




