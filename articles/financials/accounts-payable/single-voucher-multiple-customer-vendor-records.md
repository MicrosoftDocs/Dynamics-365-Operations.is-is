---
title: Eitt fylgiskjal með margar færslur viðskiptavinar eða lánardrottins
description: Þetta efnisatriði gefur yfirlit yfir hvað gerist þegar eitt fylgiskjal með margar færslur viðskiptavinar eða lánardrottins er bókuð. Þessar aðgerðir verður hætt að nota í síðari útgáfum Microsoft Microsoft Dynamics 365 for Finance and Operations, því ekki mælt með þessari aðferð við bókun vegna áhrifa bókhalds á vinnslu jöfnunar.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 222534
ms.assetid: d4df11ce-4d36-4c66-8230-f5fc58e021bc
ms.search.region: global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ded1763ce97ae751fce23cd460f99b3f3bfab7d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837085"
---
# <a name="single-voucher-with-multiple-customer-or-vendor-records"></a>Eitt fylgiskjal með margar færslur viðskiptavinar eða lánardrottins

[!include [banner](../includes/banner.md)]

Þetta efnisatriði gefur yfirlit yfir hvað gerist þegar eitt fylgiskjal með margar færslur viðskiptavinar eða lánardrottins er bókuð. Þessar aðgerðir verður hætt að nota í síðari útgáfum Microsoft Microsoft Dynamics 365 for Finance and Operations, því ekki mælt með þessari aðferð við bókun vegna áhrifa bókhalds á vinnslu jöfnunar. 

Sum algeng dæmi þar sem eitt fylgiskjal er notað fyrir marga viðskiptavini eða lánardrottna innihalda stöðufærslur á milli viðskiptavina, og stöður greiðslujöfnunar milli viðskiptavina og lánardrottna í sömu stofnun/fyrirtæki. 

Fylgiskjal sem inniheldur fleiri en einn viðskiptavin eða lánardrottinn er hægt að færa inn með því að nota eina af eftirfarandi aðferðum:

-   Með því að nota færslubók sem hefur **aðeins Eitt fylgiskjalsnúmer** valkostur valinn svo að hvert lína sem bætt er við færslubók er tekin með í sama fylgiskjali.
-   Nota fylgiskjal með mörgum línum, þar sem það er engin fjárhagsmótlykill til staðar, með fleiri en einn viðskiptavin eða lánardrottinn.
-   Færa inn fylgiskjal með lykil og mótlykill sem eru lánardrottins/lánardrottins, viðskiptavinar/viðskiptavinur, lánardrottins/viðskiptavina eða viðskiptavin/lánardrottinn.

Þetta efnisatriði sýnir hvernig jöfnun er unnin þegar eitt fylgiskjal með margar færslur viðskiptavinar eða lánardrottins er bókaður. Að auki veitir þetta efnisatriðis veitir hjáleiðir til aðstoðar við að átta sig á hvernig eigi að forðast að nota eitt fylgiskjal með fjölda viðskiptavina eða lánardrottna. Einkum eru dæmi sem lýsa tveimur algengum aðstæðum jöfnunar sem verða fyrir áhrifum af notkun eins fylgiskjals með mörgum viðskiptavini eða lánardrottna:

-   Bókhald staðgreiðsluafsláttar
-   Bókhald endurmats

## <a name="how-does-settlement-impact-single-voucher-usage"></a>Hvernig hefur jöfnun áhrif á notkun eitt fylgiskjal
Þegar fylgiskjal sem inniheldur margar færslur á viðskiptavin eða lánardrottinn er bókað, er eitt fylgiskjal bókhalds stofnuð sem inniheldur mörg stöður fyrir viðskiptakröfur eða viðskiptaskuldir. Meðan á jöfnunarferlinu stendur, upphaflega bókhaldsfærslur eru notaðar til að stofna bókhaldsfærslur fyrir staðgreiðsluafslátt, óinnleystur hagnaður og tap, innleystur hagnaður og tap og lausn safnlykils fyrir upphaflega skjalið. Til dæmis, ef staðgreiðsluafsláttur er tekið við jöfnun lánadrottinsgreiðsla við reikning, verður bókhald staðgreiðsluafsláttar að vera bókaður í fjárhagslykil viðskiptaskulda úr upprunalega reikningnum. Ef upprunalegi reikningurinn var bókaður í fylgiskjal sem inniheldur margar færslur lánardrottna, er upphaflega bókhaldið tekið saman. Í þessu tilfelli þar sem það er engin leið til að nálgast ítarlegar bókhaldsfærslu fyrir hverja færslu lánardrottins í einni fylgiskjali, er engin leið til að ákvarða hvernig notandinn vildi láta gera grein fyrir staðgreiðsluafsláttur.

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-cash-discount-accounting"></a>Eitt fylgiskjal með mörgum lánardrottnum og áhrif á bókhald staðgreiðsluafsláttar

Í eftirfarandi dæmi eru margir reikningar lánardrottins skráðar í fjárhaginn í einni fylgiskjal í **almenn færslubók** síðu. Þessir reikningar eru dreift þvert yfir marga víddir lykils.

|             |                  |              |                 |           |            |
|-------------|------------------|--------------|-----------------|-----------|------------|
| **Fylgiskjal** | **Reikningsgerð** | **Lykill**  | **Lýsing** | **Debet** | **Kredit** |
| GNJL001     | Lánardrottinn           | 1001         | INV1            |           | 100,00     |
| GNJL001     | Lánardrottinn           | 1001         | INV2            |           | 200,00     |
| GNJL001     | Lánardrottinn           | 1001         | INV3            |           | 300.00     |
| GNJL001     | Fjárhagur           | 606300-001-- | INV1            |   50,00   |            |
| GNJL001     | Fjárhagur           | 606300-002-- | INV1            |   50,00   |            |
| GNJL001     | Fjárhagur           | 606300-003-- | INV2            | 200,00    |            |
| GNJL001     | Fjárhagur           | 606300-004-- | INV3            | 300.00    |            |

Eftir bókun er eitt fylgiskjal stofnuð.

|             |              |                  |                                    |
|-------------|--------------|------------------|------------------------------------|
| **Fylgiskjal** | **Lykill**  | **Bókunargerð** | **Upphæð í færslugjaldmiðli** |
| GNJL001     | 606300-001-- | Færslubók fjárhags   | 50,00                              |
| GNJL001     | 606300-002-- | Færslubók fjárhags   | 50,00                              |
| GNJL001     | 606300-003-- | Færslubók fjárhags   | 200,00                             |
| GNJL001     | 606300-004-- | Færslubók fjárhags   | 300.00                             |
| GNJL001     | 200110-001-  | Staða lánardrottins   | -100,00                            |
| GNJL001     | 200110-001-  | Staða lánardrottins   | -200.00                            |
| GNJL001     | 200110-001-  | Staða lánardrottins   | -300.00                            |

Athugið að fylgiskjalið inniheldur þrjár færslur fyrir bókunargerðina fyrir staða Lánardrottins í eitt fylgiskjal. Það er engin leið til að tilgreina að 50,00 debetfærsla fyrir 606300-001 og 50,00 debetfærsla fyrir 606300-002 er ætlað að mótbóka stöðufærslu lánardrottins fyrir 200110-001. Þetta er vegna þess að notandinn fært inn margar lánardrottinsfærslur í eitt fylgiskjal.

Með þessu dæmi er hægt að greina áhrif af því að nota eitt fylgiskjal hefur á uppgjörsreikning niður á við. Gera ráð fyrir að greiða 197,00 af reikningi uppá 200,00 og taka 3,00 staðgreiðsluafsláttur. Athugaðu lykilgildi staðgreiðsluafsláttar er úthlutað í allar víddir úr kostnaðarlykla fylgiskjals reiknings. Þetta er vegna þess að eitt fylgiskjal var notuð til að bóka reikning hér fyrir ofan án þess að gefa til kynna um hvernig notandi vildi að kostnaðardreifingin væri gagnvart stöðu lánardrottins í einni fylgiskjali.

|             |              |                      |           |            |
|-------------|--------------|----------------------|-----------|------------|
| **Fylgiskjal** | **Lykill**  | **Bókunargerð**     | **Debet** | **Kredit** |
| APPAYM001   | 200110-001-  | Staða lánardrottins       | 197.00    |            |
| APPAYM001   | 110110-001-  | Banki                 |           | 197.00     |
| 14000056    | 520200-001-- | Staðgreiðsluafsláttur lánardrottins |           | 0.25       |
| 14000056    | 520200-002-- | Staðgreiðsluafsláttur lánardrottins |           | 0.25       |
| 14000056    | 520200-003-- | Staðgreiðsluafsláttur lánardrottins |           | 1,00       |
| 14000056    | 520200-004-- | Staðgreiðsluafsláttur lánardrottins |           | 1.50       |
| 14000056    | 200110-001-  | Staða lánardrottins       | 3,00      |            |

Ef notandinn er óánægður með staðgreiðsluafslátt sem verið er að úthluta þvert á allar kostnaðardreifingar úr upprunalega reikningnum, í stað þess að nota eitt fylgiskjal ætti að nota mörg fylgiskjöl til að skrá reikninga. Hér er dæmi um hvernig tókst að færa inn mörg fylgiskjöl í fjárhag í stað þess að nota eitt fylgiskjal, eins og sýnt er á þessu dæmi.

|             |                  |              |                 |           |            |                 |                    |
|-------------|------------------|--------------|-----------------|-----------|------------|-----------------|--------------------|
| **Fylgiskjal** | **Reikningsgerð** | **Lykill**  | **Lýsing** | **Debet** | **Kredit** | **Mótbókunargerð** | **Mótlykill** |
| GNJL001     | Lánardrottinn           | 1001         | INV1            |           | 100,00     | Fjárhagur          | &lt;autt&gt;      |
| GNJL001     | Fjárhagur           | 606300-001-- | INV1            |   50,00   |            | Fjárhagur          | &lt;autt&gt;      |
| GNJL001     | Fjárhagur           | 606300-002-- | INV1            |   50,00   |            | Fjárhagur          | &lt;autt&gt;      |
| GNJL002     | Lánardrottinn           | 1001         | INV2            |           | 200,00     | Fjárhagur          | 606300-003--       |
| GNJL003     | Lánardrottinn           | 1001         | INV3            |           | 300.00     | Fjárhagur          | 606300-004--       |

Núna, þegar INV2 er greidd verður eftirfarandi færslu gerð. Athugið fjárhagsvíddir staðgreiðsluafsláttar fylgja tengdum fjárhagsvíddum kostnaðar.

|             |              |                      |           |            |
|-------------|--------------|----------------------|-----------|------------|
| **Fylgiskjal** | **Lykill**  | **Bókunargerð**     | **Debet** | **Kredit** |
| APPAYM001   | 200110-001-  | Staða lánardrottins       | 197.00    |            |
| APPAYM001   | 110110-001-  | Banki                 |           | 197.00     |
| 14000056    | 520200-003-- | Staðgreiðsluafsláttur lánardrottins |           | 3,00       |
| 14000056    | 200110-001-  | Staða lánardrottins       | 3,00      |            |

### <a name="one-voucher-with-multiple-vendors-and-the-impact-on-realized-gainloss-accounting"></a>Eitt fylgiskjal með mörgum lánardrottnum og áhrif á bókhald innleysts hagnaður/taps

|             |                  |             |                 |           |            |                  |              |
|-------------|------------------|-------------|-----------------|-----------|------------|------------------|--------------|
| **Fylgiskjal** | **Reikningsgerð** | **Lykill** | **Lýsing** | **Debet** | **Kredit** | **Reikningsgerð** | **Lykill**  |
| GNJL001     | Lánardrottinn           | 1001        | INV1            |           | 100,00     | Fjárhagur           | 606300-001-- |
| GNJL001     | Lánardrottinn           | 1001        | INV2            |           | 200,00     | Fjárhagur           | 606300-002-- |

Í eftirfarandi dæmi eru margir reikningar lánardrottins skráðar í fjárhaginn í einni fylgiskjal í **almenn færslubók** síðu. Þessir reikningar eru dreift þvert yfir marga víddir lykils. Eftir bókun er eitt fylgiskjal stofnuð.

|             |              |                  |                                          |                                         |
|-------------|--------------|------------------|------------------------------------------|-----------------------------------------|
| **Fylgiskjal** | **Lykill**  | **Bókunargerð** | **Upphæð í færslugjaldmiðli (EUR)** | **Upphæð í bókhaldsgjaldmiðli (USD)** |
| GNJL001     | 606300-001-- | Færslubók fjárhags   | 100,00                                   | 114.00                                  |
| GNJL001     | 606300-002-- | Færslubók fjárhags   | 200,00                                   | 228.00                                  |
| GNJL001     | 200110-001-  | Staða lánardrottins   | -100,00                                  | -114.00                                 |
| GNJL001     | 200110-001-  | Staða lánardrottins   | -200.00                                  | -228.00                                 |

Athugið að fylgiskjalið inniheldur tvær færslur fyrir bókunargerðina fyrir staða Lánardrottins í eitt fylgiskjal. Það er engin leið til að tilgreina að debetfærsla fyrir 606300-001 er ætlað að mótbóka stöðufærslu lánardrottins uppá 100.00 til 200110-001. Þetta er vegna þess að notandinn fært inn margar lánardrottinsfærslur í eitt fylgiskjal. 

Með þessu dæmi er hægt að greina áhrif af því að nota eitt fylgiskjal hefur á uppgjörsreikning niður á við. Gefum okkur að bókhaldsgjaldmiðli fyrirtækisins er USD og færslur fyrir ofan voru bókaðar í færslugjaldmiðli EUR. Gefum okkur að þú greiðir að fullu reikninginn 200,00 EUR en þú uppgötvar innleyst tap vegna munur á genginu á milli þess sem þú bókaðir reikninginn og tíma greiðslunnar. Athugaðu lykilgildi innleyst taps er úthlutað í allar víddir úr kostnaðarlykla fylgiskjals reiknings. Í þessu tilfelli bæði víddin 001 og 002 var úthlutað, jafnvel þótt upplifun notanda getur verið að aðeins 002 tilheyrir kostnaðarlykil úr reikningnum sem er verið er að jafna. Þetta er vegna þess að eitt fylgiskjal var notuð til að bóka reikning hér fyrir ofan og engin leið að vita hvernig notandi vildi að kostnaðardreifingin væri gagnvart stöðu lánardrottins í einni fylgiskjali.

|             |             |                    |                                          |                                         |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| **Fylgiskjal** | **Lykill** | **Bókunargerð**   | **Upphæð í færslugjaldmiðli (EUR)** | **Upphæð í bókhaldsgjaldmiðli (USD)** |
| APPAYM001   | 200110-001- | Staða lánardrottins     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Banki               | -200.00                                  | -230.00                                 |
| 14000056    | 801300-001- | Gengistap | 0,00                                     | 0.67                                    |
| 14000056    | 801300-002- | Gengistap | 0,00                                     | 1.33                                    |
| 14000056    | 200110-001- | Staða lánardrottins     |                                          | -2.00                                   |

Ef notandinn er óánægður með tap vegna gengistaps sem verið er að úthluta þvert á allar kostnaðardreifingar úr upprunalega reikningnum, í stað þess að nota eitt fylgiskjal ætti að nota mörg fylgiskjöl til að skrá reikninga. Hér er dæmi um hvernig tókst að færa inn mörg fylgiskjöl í fjárhag í stað þess að nota eitt fylgiskjal, eins og sýnt er á þessu dæmi.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Fylgiskjal** | **Reikningsgerð** | **Lykill** | **Lýsing** | **Debet** | **Kredit** | **Mótbókunargerð** | **Mótlykill** |
| GNJL002     | Lánardrottinn           | 1001        | INV1            |           | 100,00     | Fjárhagur          | 606300-001--       |
| GNJL003     | Lánardrottinn           | 1001        | INV2            |           | 200,00     | Fjárhagur          | 606300-002--       |

Núna, þegar INV2 er greidd verður eftirfarandi færslu gerð. Athugið fjárhagsvíddir gengistaps fylgja tengdum fjárhagsvíddum kostnaðar.

|             |             |                    |                                          |                                         |
|-------------|-------------|--------------------|------------------------------------------|-----------------------------------------|
| **Fylgiskjal** | **Lykill** | **Bókunargerð**   | **Upphæð í færslugjaldmiðli (EUR)** | **Upphæð í bókhaldsgjaldmiðli (USD)** |
| APPAYM001   | 200110-001- | Staða lánardrottins     | 200,00                                   | 230.00                                  |
| APPAYM001   | 110110-001- | Banki               | -200.00                                  | -230.00                                 |
| 14000056    | 801300-002- | Gengistap | 0,00                                     | 2.00                                    |
| 14000056    | 200110-001- | Staða lánardrottins     |                                          | -2.00                                   |

## <a name="one-voucher-for-balance-transfers-and-netting-scenarios"></a>Eitt fylgiskjal fyrir stöðufærslum og aðstæður greiðslujöfnunar
Tvær aðstæður sem eru oft notaðar og nota eitt fylgiskjal sem inniheldur marga viðskiptavini eða lánardrottna innihalda stöðufærslur frá einn viðskiptavinur/lánardrottinn til annars viðskiptavinur/lánardrottinn og greiðslujöfnun viðskiptavinar og lánardrottna sem eru sama fyrirtæki. Eftirfarandi tvö dæmi lýsa æskileg aðferð til að færa þessar aðstæður inn í Finance and Operations, í stað þess að færa þær inn í eitt fylgiskjal. 

*Stöðufærsla* er eitt fylgiskjal með marga viðskiptavini fært inn til að flytja stöðu frá einum viðskiptavini á annan viðskiptavin (sama lánardrottna). Þessar aðstæður geta orðið þegar ábyrgð á að greiða reikninginn færist yfir á annar aðili, svo sem undirfyrirtæki sem færir ábyrgð í móðurfyrirtæki. 

Þetta dæmi gerir ráð fyrir sölu þar sem viðskiptavinurinn er hæfur fyrir staðgreiðsluafslátt ef greiðslan er innt af hendi innan 10 daga. Í þessu dæmi er notast viðskiptavinur við vátryggingafélagið sem ber ábyrgð á greiðslu reikningsins. Vátryggingafélagið er sett upp sem annar viðskiptavinur í kerfinu. Upphafleg staða viðskiptavinar er flutt á vátryggingafélagið sem greiðir reikninginn, og tekur 2% staðgreiðsluafslátt fyrir greiðslu innan afsláttartímabils. 

Til að sýna, skal gera ráð fyrir að eftirfarandi sölu er gerður á viðskiptavin ACME. Eftirfarandi bókhaldsfærslur tákna sölu.

|                    |                  |           |            |
|--------------------|------------------|-----------|------------|
| **Fjárhagslykill** | **Bókunargerð** | **Debet** | **Kredit** |
| 401100-002-023-    | Tekjur          |           | 100        |
| 130100-002-        | Staða viðskiptavinar | 100       |            |

Næst skal notanda flytja gjaldfallin staða frá ACME til vátryggingafélagið, í eitt fylgiskjal í greiðslubók viðskiptakrafa. Í Finance and Operations, er vátryggingafélagið sett upp sem trygging viðskiptavinar.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Fylgiskjal** | **Reikningsgerð** | **Lykill** | **Lýsing** | **Debet** | **Kredit** | **Mótbókunargerð** | **Mótlykill** |
| ARPAYM001   | Viðskiptavinur         | ACME        | Flutningur        |           | 100,00     | Viðskiptavinur        | Trygging          |

Athugið að færslu hér að ofan eru geymdar í eitt fylgiskjal. Þessu fylgiskjali inniheldur tvær færslur viðskiptavinar. Eftirfarandi fylgiskjalið er stofnuð þegar ofantalið fjárhagsfærslu er bókuð.

|             |             |                  |                                    |
|-------------|-------------|------------------|------------------------------------|
| **Fylgiskjal** | **Lykill** | **Bókunargerð** | **Upphæð í færslugjaldmiðli** |
| ARPAYM001   | 130100-002- | Staða viðskiptavinar | 100,00                             |
| ARPAYM001   | 130100-002- | Staða viðskiptavinar | -100,00                            |

Næst, gefum okkur að greiðsla berst frá viðskiptavini tryggingar fyrir 98,00 og valið er að jafna greiðsluna við reikninginn sem var stofnaður af stöðufærslunni. Þetta leiðir til að eftirfarandi fylgiskjalið er bókað. Hugsanlega er ætlast til að jöfnunin noti fjárhagsvíddir úr upprunalegum reikningi, en það er ekki mögulegt þar sem það sem ekki er reikningsskjal fyrir viðskiptavin tryggingar. Athugið að sjálfgefnu koma víddir dreifingar á staðgreiðsluafslátt úr viðskiptavinafærslu sem stofnaðar eru úr flutningnum, ekki úr upprunalega tekjulykli reiknings. Sjálfgefna er afleiðing af því að nota eitt fylgiskjal til að flytja stöðurnar.

|             |             |                  |           |            |
|-------------|-------------|------------------|-----------|------------|
| **Fylgiskjal** | **Lykill** | **Bókunargerð** | **Debet** | **Kredit** |
| ARPAYM002   | 110110-002- | Banki             | 98.00     |            |
| ARPAYM002   | 130100-002- | Staða viðskiptavinar |           | 98.00      |

Á tengt fylgiskjal fyrir staðgreiðsluafslátt, er hið sjálfgefna fyrir fjárhagsvídd komið úr færslu viðskiptavinar sem var stofnaðar úr flutninginn, þar sem flutningurinn er með fleiri en einn viðskiptavinur.

|             |             |                        |           |            |
|-------------|-------------|------------------------|-----------|------------|
| **Fylgiskjal** | **Lykill** | **Bókunargerð**       | **Debet** | **Kredit** |
| ARP-00001   | 403300-002- | Staðgreiðsluafsláttur viðskiptavinar | 2.00      |            |
| ARP-00001   | 130100-002- | Staða viðskiptavinar       |           | 2.00       |

Ef notandinn er ósáttur með hið sjálfgefna fyrir fjárhagsvíddirnar fyrir staðgreiðsluafslátt, í stað þess að nota eitt fylgiskjal ætti að nota mörg fylgiskjöl til að skrá stöðufærslu. Aðstæður ættu að nást með því að stofna kreditreikning fyrir viðskiptavin sem staðan er flutt ÚR og debet-minnisblað eða reikningur stofnaður fyrir viðskiptavininn sem staðan er flutt til. Eftirfarandi dæmi sýnir hvernig mörg fylgiskjöl er hægt að færa í greiðslubók viðskiptakröfur sem flytja stöðu, í stað þess að nota eitt fylgiskjal, eins og lýst er í þessu dæmi.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Fylgiskjal** | **Reikningsgerð** | **Lykill** | **Lýsing** | **Debet** | **Kredit** | **Mótbókunargerð** | **Mótlykill** |
| ARPAYM001   | Viðskiptavinur         | ACME        |                 |           | 100,00     | Fjárhagur          | 401100-002-023-    |
| ARPAYM002   | Viðskiptavinur         | Trygging   |                 | 100,00    |            | Fjárhagur          | 401100-002-023-    |

Þetta þýðir að þegar viðskiptavinur Tryggingar 98,00 með fylgiskjali ARPAYM02, rétta fjárhagsvíddir úr fylgiskjali ARPAYM002 fjárhagsfærslu verður notuð.

|             |             |                  |           |            |
|-------------|-------------|------------------|-----------|------------|
| **Fylgiskjal** | **Lykill** | **Bókunargerð** | **Debet** | **Kredit** |
| ARPAYM003   | 110110-002- | Banki             | 98.00     |            |
| ARPAYM003   | 130100-002  | Staða viðskiptavinar |           | 98.00      |

Á tengt fylgiskjal fyrir staðgreiðsluafslátt, fjárhagsvíddir verður notuð úr mótfærslu tekjulykils á fylgiskjali ARPAYM002.

|             |                 |                        |           |            |
|-------------|-----------------|------------------------|-----------|------------|
| **Fylgiskjal** | **Lykill**     | **Bókunargerð**       | **Debet** | **Kredit** |
| ARP-00001   | 403300-002-023- | Staðgreiðsluafsláttur viðskiptavinar | 2.00      |            |
| ARP-00001   | 130100-002-     | Staða viðskiptavinar       |           | 2.00       |

### 

## <a name="one-voucher-with-a-netting-for-multiple-customers-and-vendors"></a>Eitt fylgiskjal með skuldajöfnun fyrir margar viðskiptavina og lánardrottna
Skuldjöfnun koma að gagni þegar fyrirtæki sem kaupir og selur til sama fyrirtækis. Frekar en að greiða reikninga lánardrottins og bíða eftir að taka við greiðslu fyrir reikninga viðskiptavina, eru reikninga lánardrottna og viðskiptavina skuldajöfnuð. Færsla skuldajöfnunar er jöfnuð á móti útistandandi stöðu. 

Til að sýna, gefum okkur að lánardrottna 1001 og viðskiptavini US-008 eru sömu einingu, svo fyrirtækið vill skuldajafna stöður viðskiptaskuldir og viðskiptakrafa áður en greiddar eru/tekið við greiðslum eftirstöðvar. Gerum ráð fyrir að færslu viðskiptavinar skuldar 75,00 EUR og færslu lánardrottins skuldar 100,00 EUR, sem þýðir að þú myndir frekar kjósa nettó stöður og aðeins greiða lánardrottins 25,00 EUR. Ennfremur er gert ráð fyrir að bókhaldsgjaldmiðill sé USD. Í þessu tilfelli er færsla skuldajöfnunar færð inn í eitt fylgiskjal í greiðslubók viðskiptaskulda.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Fylgiskjal** | **Reikningsgerð** | **Lykill** | **Lýsing** | **Debet** | **Kredit** | **Mótbókunargerð** | **Mótlykill** |
| APPAYM001   | Lánardrottinn           | 1001        | Greiðslujöfnun         |  75,00    |            | Viðskiptavinur        | US-008             |

Til að forðast óæskilegar vandamál við síðari jafnanir fyrir þessa færslu, í stað þess að nota eitt fylgiskjal, ætti að færa inn mörg fylgiskjöl í færslubókina sem til að skrá færslu skuldajöfnunar. Athugið að stöður viðskiptavinar og lánardrottins eru jafnaðar með einni millireikning að forðast að nota eitt fylgiskjal sem inniheldur margar stöður viðskiptavina og lánardrottna.

|             |                  |             |                 |           |            |                 |                    |
|-------------|------------------|-------------|-----------------|-----------|------------|-----------------|--------------------|
| **Fylgiskjal** | **Reikningsgerð** | **Lykill** | **Lýsing** | **Debet** | **Kredit** | **Mótbókunargerð** | **Mótlykill** |
| 001         | Viðskiptavinur         | US-008      |                 |           |  75,00     | Fjárhagur          | 999999---          |
| 002         | Lánardrottinn           | 1001        |                 |  75,00    |            | Fjárhagur          | 999999---          |





