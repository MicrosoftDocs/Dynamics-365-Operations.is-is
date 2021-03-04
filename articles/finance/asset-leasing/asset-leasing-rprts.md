---
title: Eignarleiguskýrsla
description: Þetta efnisatriði sýnir og lýsir stuttlega þeim skýrslum sem eru í boði í eignarleigu.
author: moaamer
manager: Ann Beebe
ms.date: 10/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-27
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: bab2b0b2b021266e50d6f4a1fad1cc4a1c1ae56e
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4444584"
---
# <a name="asset-leasing-reports"></a>Eignarleiguskýrsla

[!include [banner](../includes/banner.md)]

Þetta efnisatriði sýnir og lýsir stuttlega þeim skýrslum sem eru í boði í eignarleigu. Flestar skýrslur birtast með því að klára þessi skref eða önnur svipuð skref eins og tekið er fram). 

- Til að skoða flestar eignarleiguskýrslur skal fara í **Eignarleiga > Fyrirspurnir og skýrslur > Leiguskýrslur** og síðan velja skýrslu til að skoða. Fyrir skýrslurnar sem þurfa annars konar valslóð, eru leiðbeiningarnar til að opna skýrsluna í lýsingu á þeirri skýrslu. 
- Þegar valin er skýrsla til að prenta opnast færibreytusíðu sem gerir þér kleift að sía upplýsingarnar sem hafðar eru með í skýrslunni. Sláið inn síuskilyrði og veljið svo **Í lagi** til að búa til skýrslu. Mynduð skýrsla mun sýna upplýsingar sem falla undir síurnar sem voru tilgreindar.

## <a name="asset-movement"></a>Eignahreyfingar
Eignahreyfingarskýrslan þjónar sem framlengingarskýrsla fyrir stöðu afnotaréttar af eign fyrir hvern leigusamning. Þessi skýrsla gerir þér kleift að skoða eignafærslur leigu yfir tiltekið tímabil. Skýrslan inniheldur eftirfarandi reiti. 

|     Skýrslureitir                  |     lýsing                                                                |
|------------------------------------|--------------------------------------------------------------------------------|
|     Upphafsdagsetning              |     Upphafsdagsetning á fyrstu útgáfu leigusamningsins.                     |   
|     Leigutími                     |     Leigutími fyrstu útgáfu leigusamningsins.                            |
|     Skammtímaleiga               |     Ef leigan er flokkuð sem skammtímaleiga verður það sýnt sem **Já**.         |
|     Lágvirðiseign                |     Ef leigan er flokkuð sem leiga verðlítillar eignar verður það sýnt sem **Já**.          |
|     Upphaflegur afnotaréttur af eign     |     Upprunalegt virði afnotaréttar af eign úr upphaflegri skráningu í færslubókina.      |
|     Upphafsstaða              |     Bókað nettóvirði fyrir afnotarétt af eign frá og með **Frá dagsetningu**.                         |
|     Tímabil afskriftakostnaðar    |     Upphæð afskriftakostnaðar innan dagabilsins sem er skilgreint fyrir skýrsluna.        |
|     Uppsöfnuð afskrift       |     Upphæð uppsafnaðra afskrifta frá og með **Frá dagsetningu**.                               |
|     Virðisrýrnun                     |     Upphæðin sem eignin rýrnaði í virði innan dagabilsins sem er skilgreint fyrir skýrsluna.               |
|     Breytingar                  |     Upphæð leiðréttinga á afnotarétti eignar milli færibreyta dagsetningar.                            |
|     Bókað nettóvirði                 |     Bókað lokanettóvirði á afnotarétti eignar, sem er nettó uppsafnaðra afskrifta frá og með **Til dagsetningar**.    |

## <a name="differences-report"></a>Mismunarskýrsla
Mismunarskýrslan sýnir mismuninn milli upplýsinga sem hlaðið er inn í innflutningsramma leigusamningsins og upplýsinga sem eru í kerfinu á þessari stundu. Þetta gerir þér kleift að bera saman það sem var lagað, uppfært eða bætt við í gegnum innflutningsramma leigusamningsins.  

Gildin í skýrslunni verða breytileg eftir völdum leigutaka. Skýrslan sýnir aðeins þá reiti sem eru öðruvísi en þeir sem eru núna í kerfinu og í millistigsvistunartöflunum. Gamla gildið er það sem er annaðhvort í kerfinu núna eða það sem var áður í kerfinu, eftir því hvort búið sé að keyra innflutningsferlið. Nýja gildið sýnir gildið sem er í millistigsvistunartöflunni sem kemur í stað gamla gildisins.

## <a name="five-years-undiscounted-payment-forecast"></a>Fimm ára óafvöxtuð greiðsluspá
Skýrslan um fimm ára óafvaxtaða greiðsluspá sýnir áætlaðar óafvaxtaðar leigugreiðslur sem á að greiða á næstu fimm árum frá deginum sem er tilgreindur í skýrslufæribreytunum. Skýrslan inniheldur eftirfarandi reiti. 

|     Skýrslureitir         |     lýsing                                                                                       |
|-------------------------- |---------------------------------------------------------------------------------------------------    |
|     Lýsing á leigusamningi     |     Lýsing á leigusamningi í haus leigusamningsins.                                                      |
|     Leigukenni              |     Einkvæma leigukennið.                                                                              |
|     Bóka                  |     Leigubókin sem tengist bókarkenninu.                                                         |
|     Flokkun        |     Flokkun leigusamningsins.                                                                  |
|     Bókunarlag         |     Lagið sem þessi leiga er bókuð á.                                                         |
|     Gjaldmiðill              |     Gjaldmiðll leigu.                                                                        |
|     Núverandi               |     Samtala allra leigugreiðslna til greiðslu innan næstu 12 mánaða frá dagsetningu skýrslugerðar.          |
|     13–24 mánuðir          |     Samtala allra leigugreiðslna til greiðslu milli 13 og 24 mánuðum frá dagsetningu skýrslugerðar.           |
|     25–36 mánuðir          |     Samtala allra leigugreiðslna til greiðslu milli 25 og 36 mánuðum frá dagsetningu skýrslugerðar.           |
|     37–48 mánuðir          |     Samtala allra leigugreiðslna til greiðslu milli 37 og 48 mánuðum frá dagsetningu skýrslugerðar.           |
|     49–60 mánuðir          |     Samtala allra leigugreiðslna til greiðslu milli 49 og 60 mánuðum frá dagsetningu skýrslugerðar.           |
|     Þar á eftir            |     Samtala allra leigugreiðslna til greiðslu 61 mánuði eða síðar frá dagsetningu skýrslugerðar.              |

## <a name="gaap-cash-flows-report"></a>Sjóðstreymisskýrsla GAAP
Skýrsla með upplýsingum um GAAP uppfyllir US GAAP upplýsingakröfur sem tilgreindar eru í 842-20-50-4(g)(1). Til að skoða þessa skýrslu er farið á **Eignarleiga > Fyrirspurnir og skýrslur > Upplýsingar > GAAP - sjóðstreymi**. 

|     Skýrslureitir                                 |     lýsing                                                                                                                                               |
|------------------------------------------------   |-----------------------------------------------------------------------------  |
|     Frá dagsetning <br> Til dags.                        |     Skilgreinir dagsetningabil sem er notað til að takmarka upplýsingarnar sem hafðar eru með í skýrslunni.      |
|     Lögaðili                                  |     Lögaðili sem bundinn er við leigusamninga.                                      |
|     Gerð leigu                                    |     Flokkun leigusamningsins sem annaðhvort fjármögnunarleigusamningur eða rekstrarleigusamningur.           |
|     Leigukenni                                      |     Einkvæma leigukennið.                                                      |
|     Lýsing á leigusamningi                             |     Lýsing á leigusamningi í haus leigusamningsins.                              |
|     Leigubók                                    |     Leigubókin sem línan vísar í.                        |
|     Bókunarlag                                 |     Hvert bók sem er tengt eign er uppsett fyrir ákveðið bókunarlag sem hefur heildarafskriftarviðfang.                          |
|     Leigusamningsflokkur                                   |     Flokkurinn sem leigan er bundin við.                                     |
|     Gjaldmiðill                                      |     Skammstöfun fyrir færslugjaldmiðilinn sem er notaður. Í öllum skýrslum verður færslugjaldmiðlinum breytt í skýrslugjaldmiðilinn.                      |
|     Fjármögnunarleigusamningar - Rekstrarsjóðstreymi         |     Samtala allra bókaðra breytilegra greiðslna og heildarvaxtagreiðslna sem bókaðar eru úr afskriftaráætlun á milli dagsetningarfæribreytanna.        |
|     Fjármögnunarleigusamningar - Sjóðstreymi fjármögnunar           |     Samtala allra höfuðstólsgreiðslna úr afskriftaráætlun milli dagsetningarfæribreytanna.       |
|     Rekstrarleigusamningar - Rekstrarsjóðstreymi       |     Samtala allra bókaðra leigugreiðslna og bókaðra breytilegra greiðslna á milli dagsetningarfæribreytanna.            |

## <a name="lease-balances-forecast"></a>Spá um stöðu leigusamninga
Spá um stöðu leigusamninga sýnir upplýsingar beint frá afskriftaráætlun skuldbindinga og afskriftaráætlun eigna. Skýrslan sýnir upphæðir sem spáð er fyrir um í áætlaðri leiguskuldbindingu og afnotarétti af eign yfir tímabil, þ.m.t. allan áætlaðan kostnað fyrir þessa leigusamninga. Skýrslan inniheldur eftirfarandi reiti.

|     Skýrslureitir                 |     lýsing                                                                                                                                                                               |
|---------------------------------  |--------------------------------------------------------------------------------------------------------------------   |
|     Upphafsstaða             |     Upphafsstaða í afskriftaráætlun leigusamningsins fyrir tímabilið sem inniheldur upphafsdagsetningu skýrslunnar.            |
|     Upphafleg skráning           |     Ef upphafsdagsetning leigusamningsins fellur innan dagsetningabilsins sem skilgreint er í skýrslunni mun þessi dálkur sýna gildið fyrir skuldbindingu á upphaflegri skráningu í færslubókinni.      |
|     Greiðslur                      |     Samtala leigugreiðslna sem falla innan dagsetningabilsins sem er skilgreint fyrir skýrsluna.                               |
|     Áhugasvið                      |     Samtala vaxtakostnaðar fyrir leiguna sem fellur innan dagsetningabilsins sem er skilgreint fyrir skýrsluna.                    |
|     Lokastaða                |     Skuldastaða leigunnar frá og með **Til dagsetningar**.                                                             |
|     Skammtímaskuldir          |     Upphæð skammtímaskulda í afskriftaráætlun leigusamningsins frá og með **Til dagsetningar**.                           |
|     Langtímaskuld           |     Upphæð langtímaskulda í afskriftaráætlun leigusamningsins frá og með **Til dagsetningar**.                            |
|     Upphaflegt bókað nettóvirði      |     „Bókað nettóvirði í upphafi“ í afskriftaráætlun eignar í leigusamningi fyrir tímabilið sem inniheldur upphafsdagsetningu skýrslunnar      |
|     Upphafleg skráning           |     Ef upphafsdagsetning leigusamningsins fellur innan dagsetningarfæribreyta skýrslunnar mun þessi dálkur sýna gildið fyrir skuldbindingu á upphaflegri skráningu í færslubókinni.            |
|     Afskriftakostnaður          |     Samtala afskriftakostnaðar fyrir leiguna sem fellur innan dagsetningabilsins sem er skilgreint fyrir skýrsluna.                  |
|     Lokastaða                |     Eignastaða leigunnar frá og með **Til dagsetningar**.                                                              |
|     Leiðrétting á eigin fé             |     Upphafsstaða að frádregnu bókuðu nettóvirði í upphafi.                                                             |

## <a name="lease-commencements-report"></a>Skýrsla um upphaf leigusamnings
Skýrsla um upphaf leigusamnings sýnir alla leigusamninga sem hafa byrjað innan tiltekins dagsetningabils, þ.m.t. stöðu upphaflegrar skuldbindingar og afnotaréttar af eign. Skýrslan inniheldur eftirfarandi reiti. 

|     Skýrslureitir                 |     lýsing                                                                                       |
|---------------------------------  |---------------------------------------------------------------------------------------------------    |
|     Upphafsdagsetning             |     Dagsetning upphaflegrar skráningar í færslubók sem var bókuð fyrir þá útgáfu leigusamnings.         |
|     Upphafleg upphæð skuldar      |     Upphæð skuldar fyrir upphaflega skráningu í færslubók.                                  |
|     Stofnupphæð eignar          |     Upphæð eignar fyrir upphaflega skráningu í færslubók.                                      |

## <a name="lease-modification-report"></a>Skýrsla um breytingar á leigusamningi
Skýrsla um breytingar á leigusamningi sýnir alla leigusamninga sem hefur verið breytt innan tiltekins dagsetningabils. Skýrslan sýnir líka notandann sem leiðrétti leigusamninginn og heildarupphæð leiðréttrar skuldar. Skýrslan inniheldur eftirfarandi reiti. 

|     Skýrslureitir                 |     lýsing           |
|---------------------------------  |-------------------------  |
|     Leiðrétt af                   |     Notandanafn þess sem breytti leigusamningnum.                                |
|     Dagsetning leiðréttingar               |     Dagsetningin sem leiðréttingarfærsla var bókuð í færslubók.                        |
|     Leiðréttingar                   |     Upphæðin fyrir allar leiðréttingarfærslur í færslubók sem voru bókaðar á skuldareikning leigusamningsins á milli færibreytudagsetninganna. Kreditfærslur verða sýndar sem jákvæðar og debetfærslur sem neikvæðar.       |
|     Upphæð hagnaðar (taps)            |     Upphæðin fyrir allar leiðréttingarfærslur í færslubók sem voru bókaðar á hagnaðar-/tapreikning leigusamningsins á milli færibreytudagsetninganna. Kreditfærslur verða sýndar sem jákvæðar og debetfærslur sem neikvæðar.       |
|     Óráðstafað eigið fé             |     Upphæðin fyrir allar leiðréttingarfærslur í færslubók sem voru bókaðar á framlegðarreikning leigusamningsins á milli færibreytudagsetninganna.      |
|     Lokastaða skuldar      |     Skuldastaðan sem kemur upp frá og með leiðréttingardagsetningu leigunnar.           |

## <a name="lease-movement-report"></a>Hreyfingarskýrsla leigunnar
Hreyfingarskýrsla leigunnar þjónar sem framlengingarskýrsla fyrir skuldastöðu eignar fyrir hvern leigusamning. Þessi skýrsla gerir notanda kleift að skoða skuldafærslur leigu yfir tiltekið tímabil.

|     Skýrslureitir             |     lýsing                                               |
|----------------------------   |-------------------------------------------------------------- |
|     Upphafsdagsetning         |     Upphafsdagsetning á fyrstu útgáfu leigusamningsins.    |
|     Leigutími                |     Leigutími fyrstu útgáfu leigusamningsins.           |
|     Eftirstandandi greiðslur        |     Fjöldi greiðslna sem enn hefur ekki verið bókaðar fyrir leiguna.                       |
|     Upphafsstaða         |     Samtala allra færslna sem hafa áhrif á leiguskuldina sem átti sér stað á undan upphafsdegi skýrslunnar.             |
|     Upphafleg skráning       |     Upphæð allra upphaflegra skráningarfærslna fyrir leigusamninginn sem var bókuð innan dagsetningabilsins sem er skilgreint fyrir skýrsluna.     |
|     Greiðslur                  |     Samtala fyrir greiðslufærslur leigu sem hafa verið bókaðar innan dagsetningabilsins sem er skilgreint fyrir skýrsluna. Gildin í þessum dálki birtast sem neikvæðar upphæðir þar sem greiðslurnar minnka skuldastöðu leigusamningsins.  |
|     Áhugasvið                  |     Samtala uppsafnaðra vaxta sem hafa verið bókaðir á móti leigusamningnum innan dagsetningabilsins sem er skilgreint fyrir skýrsluna.            |
|     Leiðréttingar               |     Samtala bókaðra leiðréttingafærslna leigusamningsins innan dagsetningabilsins sem er skilgreint fyrir skýrsluna.                               |
|     Lokastaða            |     Staða allra skuldafærslna leigusamningsins sem hafa verið bókaðar frá og með **Til dagsetningar** í skýrslunni.                  |

## <a name="lease-transactions-report"></a>Leigufærsluskýrsla
Fyrirspurn um leigufærslur sýnir allar færslur í færslubók sem eignarleigan hefur myndað. Hver færsla í færslubók er tengd við bókarkennið sem hún á uppruna sinn í. Þetta gerir þér kleift að tengja á auðveldan hátt færslu í færslubók við samsvarandi leigusamning. Fyrirspurn um leigufærslur virkar á svipaðan hátt og á síðunni **Fylgiskjalafærslur** í fjárhag.

## <a name="weighted-average-discount-rate-report"></a>Skýrsla um vegið meðaltal forvaxta
Skýrslan um vegið meðaltal forvaxta fullnægir kröfum US GAAP um upplýsingamiðlun sem tilgreindar eru í ASC 842-20-50-4(g)(4) fyrir vegið meðaltal forvaxta. Til að skoða þessa skýrslu er farið í **Eignarleiga > Fyrirspurnir og skýrslur > Upplýsingar > Vegið meðaltal forvaxta**. Skýrslan inniheldur eftirfarandi reiti. 

|     Skýrslureitir                     |     lýsing                                                           |
|------------------------------------   |------------------------------------------------------------------------   |
|     Frá og með dagsetningu                        |     Þessi skýrsla inniheldur alla leigusamninga sem byrjuðu á eða fyrir **Frá og með** dagsetningarfæribreytunni. Þessa skýrslu á að keyra á síðasta degi tímabilsins sem á að gefa upp.      |
|     Lögaðili                      |     Lögaðilinn sem er bundinn leigusamningnum.                           |
|     Leigukenni                          |     Einkvæma leigukennið.                                                  |
|     Lýsing á leigusamningi                 |     Lýsing á leigusamningi í haus leigusamningsins.                          |
|     Bóka                              |     Ákveðin gerð bókar fyrir birtan leigusamning.                                                                                                                                            |
|     Bókunarlag                     |     Hvert bók sem er tengt eign er uppsett fyrir ákveðið bókunarlag sem hefur heildarafskriftarviðfang.      |
|     Leigusamningsflokkur                       |     Flokkurinn sem leigusamningurinn tilheyrir.                                 |
|     Forvextir                     |     Taxtinn sem er notaður fyrir afslátt leigugreiðslu.                             |
|     Gjaldmiðill                          |     Skammstöfun fyrir færslugjaldmiðilinn sem er notaður. Í öllum skýrslum verður færslugjaldmiðlinum breytt í skýrslugjaldmiðilinn.  |
|     Eftirstandandi leigugreiðslur          |     Heildarupphæð ógreiddra leigugreiðslna úr greiðsluáætlun sem eftir stendur frá dagsetningunni **Frá og með**.            |
|     Eftirstandandi vegnar greiðslur       |     Leigugreiðslur sem eftir eru margfaldaðar með notuðum forvöxtum.   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]