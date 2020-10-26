---
title: Hafist handa með eignarleigu
description: Í þessu efnisatriði er lýst möguleikum eignarleigu og farið í gegnum skrefin til að búa til leigusamning eignar og skoða upplýsingar fyrir þessa leigusamninga.
author: moaamer
manager: Ann Beebe
ms.date: 09/24/2020
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
ms.search.validFrom: 2020-09-24
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 5f8f86861f65f3da71843f6fd4a64e4199e86627
ms.sourcegitcommit: 9668af8d918faec37abe1881e550872cd6b73259
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/08/2020
ms.locfileid: "3970009"
---
# <a name="asset-leasing-get-started"></a>Hafist handa með eignarleigu

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Í þessu efnisatriði er lýst möguleikum eignarleigu og farið í gegnum skrefin til að búa til leigusamning eignar og skoða upplýsingar fyrir þessa leigusamninga. Í efnisatriðinu eru einnig skilgreind hugtökin sem notuð eru í notandaviðmóti og fylgigögnum. Eignarleiga er víðtæk lausn til að hafa umsjón með, rekja og virkja sjálfkrafa fjárhagsfærslur fyrir leigðar eignir í Microsoft Dynamics 365 Finance. Eignarleiga samræmist alþjóðlegum reikningsskilastöðlum (IFRS 16) og US GAAP-stöðlum (ASC 842). Eignarleiga nær í og vinnur úr upplýsingum um leigusamningana og hjálpar til við að búa til færslur í færslubók í gegnum gildistíma leigusamningsins, frá upphaflegri skráningu, mánaðarlegum færslum í færslubók, til virðisrýrnunar og lok leigusamningsins. Eignarleiga samþættist á einfaldan hátt við aðra hluta Dynamics 365 Finance, þ.m.t. Eignir, Viðskiptaskuldir og Fjárhag.

Frekari upplýsingar varðandi bókhaldsstaðla er að finna í stöðluðum fylgiskjölum fyrir IFRS 16 og US GAAP ASC 842.

## <a name="asset-leasing-elements"></a>Eignaleiguþættir
Eftirfarandi skýringarmynd sýnir helstu einingar viðskiptaferlis fyrir leigusamninga.

[![Eignaleiguþættir](./media/overview-01.png)](./media/overview-01.png)

Leigð eign inniheldur eftirfarandi meginþætti:

- **Leigusamningur** - Leigusalinn á eignina og gerir samkomulag við leigjandann um að leigja út eign á tilteknum tímabili í skiptum fyrir reglubundnar leigugreiðslur. Auk lagalegs samnings milli leigusala og leigjanda, nær leigusamningurinn yfir stjórnunarákvörðunum á borð við líkurnar á því að nýta sér valkost endurnýjunar og breytingu á eignarhaldi.

- **Útreikningur og flokkun leigusamnings eftir reikningsskilastaðli** - Útreikningur og flokkun leigusamnings segja til um reikningsskilastaðalinn sem verður notaður við upphaflegt mat og í framhaldinu, auk prófun flokksins sem ákvarðar hver gerð leigusamningsins verður. Leigusamningur getur verið fjármögnunarleigusamningur, rekstrarleigusamningur, skammtímaleigusamningur eða leigusamningur verðlítillar eignar. Kerfið reiknar einnig út núvirði á lágmarksgreiðslum á leigu í framtíðinni fyrir mat og flokkun.

- **Leigufærslur** - Eignarleiga styður upphaflega skráningu á afnotarétti af eign fyrir leigusamninga á efnahagsreikningnum, auk væntanlegu mati fyrir annaðhvort leigusamninga í eða fyrir utan efnahagsreikning. Upphaflegar skráningarfærslur reikna út núvirði á lágmarksgreiðslum á leigu í framtíðinni. Þessi gögn eru notuð til að ákvarða virði á upphaflegum afnotarétti eignar og leiguskuldbindingu, sem hefur áhrif á efnahagsreikning fyrirtækisins. Seinna mat á mánaðarlegum leigufærslum felur í sér uppsöfnun vaxta á leiguskuldbindinguna, sem hækkar leiguskuldbindinguna. Það mælir einnig uppsöfnun leigugreiðslna sem lækka leiguskuldbindingu og sem verður síðan greitt út til leigusala. Matið felur einnig í sér afskrift á afnotarétti eignar.

  Fyrir leigusamninga utan efnahagsreiknings, reiknar kerfið út línulegan leigukostnað fyrir annaðhvort af eftirfarandi sem felur í sér lægri kostnað: efnahagslegan líftíma eignarinnar eða leigutímann. Breytingar á leigu taka til greina breytingar á samningum á borð við framlengingu eða stækkun leigusamnings og færslu virðisrýrnunar sem notar afnotaréttinn af eign fyrir óendurheimtanlegan kostnað.

  Eignarleiga samþættist við Fjárhag til að tryggja að allar bókaðar leigufærslur uppfæri bókhaldslykilinn. Eignarleiga samþættist við Viðskiptaskuldir til að rekja reikninga leigusala í Viðskiptaskuldum og taka við framtíðargreiðslum þaðan. Samþætting við Eignir gerir þér kleift að rekja leigusamninga í skrá eignar og bóka færslur afnotaréttar af eign, þ.m.t. upphaflega skráningu, afskrift og virðisrýrnun eignar innan Eigna.   

## <a name="asset-leasing-components"></a>Þættir Eignarleigu 
Eignarleiga varpar upplýsingum um leigusamning, greiðsluáætlunum, upphafs- og lokadagsetningu og greiðslutíðninni. Hún gerir einnig útreikninga fyrir núvirði, mánaðarlegar leigugreiðslur, vexti og afskriftir leigusamnings sjálfvirka. Kerfið framkvæmir prófanir á flokkun leigusamnings, eftir því hver grunnstillingin er. Kerfið stofnar einnig og bókar samsvarandi leigufærslur sem eru byggðar á þeim ramma sem er skilgreindur af þeim reikningsskilastaðli sem þú ferð eftir.

Eftirfarandi skýringarmynd sýnir leigubók, leigusamning, reiknaða greiðsluáætlun, flokkunarprófanir fyrir leigusamninga og leigubækur og samsvarandi bókhaldsfærslur.

[![Leigusamningur, leigubók og greiðsluáætlun](./media/overview-02.png)](./media/overview-02.png)

- **Leigubók** - Leigubókin inniheldur allar upplýsingar um leigusamninginn, svo sem leiguskilmála, gangvirði og leigugreiðslur. Þar er einnig að finna reikningsskilastaðalinn sem þú fylgir, gerð leigusamningsins og mörkin sem eru tekin til greina í flokkunarprófun leigusamningsins. Leigubókin inniheldur einnig leigufærslurnar sem voru bókaðar í fjárhag. 
  
- **Leigusamningur** - Leigusamningurinn inniheldur upplýsingar um leigu eignar sem er grunnurinn að eignarleigunni, uppruni leiguupplýsinga er leigusamningur og stjórnunarákvarðanir eru gerðar utan við Dynamics 365 Finance. Gangvirði eignar er verðið sem á að greiða fyrir eign í færslu á degi verðmatsins. Þetta gildi gæti farið eftir eignagerðinni, markaðsskilyrðum og öðrum skilyrðum sem hægt er að taka til greina í matinu. Gangvirði eignar verður tekið til greina í jöfnu flokkunarprófunar.

- **Nýtingartími eignar** - Þetta táknar eftirstandandi tímabil fyrir nýtingartíma eignar, frá og með upphafsdagsetningu leigusamningsins. Nýtingartími eignar verður tekin til greina í jöfnun flokkunarprófunar. Hann er frábrugðinn nýtingartímanum sem er skilgreindur í Eignum.

- **Vextir á nýju lánsfé** - Þetta eru vextirnir sem verða notaðir til að reikna núvirðið. Kerfið mun nota óbeina vexti ef það er skilgreint í gögnum leigusamnings að reikna núvirði leigugreiðslnanna. Ef óbeinir vextir eru ekki skilgreindir, notar kerfið vexti á nýju lánsfé.

- **Tegund afborgunar** - Þetta er leigugreiðsla á gjalddaga annaðhvort við upphaf greiðslutímabilsins eða undir lok þess. Þetta gæti verið fyrirframgreiðsla eða framsett afborgun (við upphaf tímabils leigugreiðslunnar) eða venjuleg afborgun (undir lok tímabils leigugreiðslunnar).

  Fyrsti mánuður verður talinn sem tímabil númer núll fyrir fyrirframgreiðslu; fyrstu mánuður verður talinn tímabil eitt fyrir greiðslu eftirstöðva.

- **Samsett tímabil** - Þetta táknar fjölda tímabila sem vextir eru teknir saman á ári. Þetta gæti verið mánaðarlega (tólf tímabil á ári), ársfjórðungslega (fjögur tímabil á ári), hálfs árs fresti (tvö tímabil á ári), eða árlega (eitt tímabil á ári). Fjöldi tímabila verður talinn með í útreikningi núvirðis.

- **Upphafsdagsetning** - Þetta er dagsetningin þegar leigusali gerir leigjanda kleift að nota eignina. Allir útreikningar og færslur leigusamnings verða notuð samkvæmt upphafsdagsetningunni. Upphafsdagsetning á að vera í upphafi tímabils (fyrsta dag mánaðar) til að tryggja nákvæmni væntanlegra útreikninga. Hægt er að nota reitinn **Dagsetning undirritunar samnings** til að færa inn raundagsetninguna þegar samningurinn var undirritaður.

- **Leigutími** - Þetta er lengd leigutímans, í mánuðum.

> [!NOTE] 
> Skilgreining á leigutíma byggir á fjölda tímabila, eða bila, í greiðsluáætlunarlínum. Skilgreindum fjölda bila verður breytt í mánuði.

- **Greiðsluáætlunarlína** - Þetta heldur utan um leigugreiðslur eftir tímabili. Hún tilgreinir einnig hvort endurnýjunartímabil verður notað og tekið með í upphaflegu mati á afnotarétti af eign og leiguskuldbindingu. Hægt er að skilgreina upphafsdagsetningu fyrir gjaldfallnar greiðslur leigusamningsins og tímabilin sem tákna lengd leigusamningsins, sem getur verið í dögum, mánuðum eða árum.

- **Greiðslutíðni** - Þetta gefur til kynna hvort greiðslan er mánaðarleg, ársfjórðungsleg, hálfs árs fresti eða árlega. Lokadagsetningin er sjálfkrafa reiknuð út frá upphafsdegi og fjölda tímabila sem færð voru inn.

- **Greiðsluáætlun** - Þetta er reiknað núvirði, byggt á tímalengdinni sem leigugreiðslurnar ná yfir, greiðsluupphæðunum, samsettum tímabilum og tegund afborgunar.

- **Tímabilin** - Þetta eru leigutímabilin sem endurspegla innri samsetningu og tegund afborgunar. Samsett tímabil ákvarðar hvernig tímabilum verður skipt. Hægt er að stilla eftirfarandi samsett tímabil:

  - Mánaðarlega, 12 tímabil á ári
  - Ársfjórðungslega, 4 tímabil á ári
  - Hálfs árs fresti, 2 tímabil á ári
  - Árlega, 1 tímabil á ári

Fyrsta tímabilið hefst á tímabili núll, ef tegund afborgunar er framsett afborgun. Annars hefst fyrsta tímabilið á einum, ef tegund afborgunar er vangoldin greiðsla.

- **Mánuðir** - Þetta gefur til kynna fjölda almanaksmánaða yfir lengd leigutímans. Greiðsluupphæðin er gjaldfallin upphæð eins og hún er skilgreind í greiðslutíðninni. Útreiknað núvirði er leigugreiðsla á tímabili sem byggir á núvirði, samsett tímabil og vexti á nýju lánsfé.

> [!NOTE] 
> Núvirði er reiknað samkvæmt jöfnu afvaxtaðs sjóðstreymis.

- **Bækur** - Þetta er forskilgreind uppsetning sem tengist hverjum leigusamningi. Bókin skilgreinir þann reikningsskilastaðal sem er notaður, gerðir leigusamninga og mörkin sem eru notuð til grundvallar prófunar á flokkun. Flokkunarprófanir eru notaðar til að tilgreina gerð leigusamningsins sjálfkrafa.

- **Bókhaldsrammi** - Þetta sýnir valinn reikningsskilastaðal, annaðhvort IFRS 16 eða ASC 842, sem þú styður. Reikningsskilastaðallinn er tekinn fram á bókinni sem tengist leigusamningnum. Reikningsskilastaðallinn ákvarðar fjárhagslyklana sem eru tilgreindir í bókunarreglunni.

- **Gerðir leigusamninga** Þetta gefur til kynna hvor gerðin af leigusamningi verður notuð, annaðhvort fjármögnunarleigusamningur eða rekstrarleigusamningur. Undir fjármögnunarleigusamningi eru áhætta og ávinningur sem tengjast leigðri eign fluttar á leigjandann. Undir rekstrarleigusamningi helst áhætta og ávinningur sem tengjast leigðri eign áfram hjá leigusalanum. Þriðji valkosturinn er sjálfvirk auðkenning á gerð leigusamnings, annaðhvort fjármögnunar- eða rekstrarleiga, sem byggir á skilgreindum mörkum í bókinni. Þessi sjálfvirka auðkenning er framkvæmd meðan endurflokkunarprófun er í gangi.

- **Mörk** - Þetta er notað í prófunum á flokkun leigusamnings til að ákvarða hvort eignin er flokkuð samkvæmt einhverju af eftirfarandi:

  - **Leigutími** - Þetta er prósenta nýtingartímans sem nota á í flokkunarprófuninni. Kerfið mun flokka leigusamninginn sem fjármögnunarleigusamning ef gerð leigusamnings er stillt á sjálfvirkni, og ef leigutíminn yfir nýtingartíma eignarinnar er meiri en eða jafnt og prósentan sem gefin er upp hér.

  - **Núvirði** - Þetta er prósentan af gangvirði eignar sem nota á í flokkunarprófuninni. Kerfið mun flokka leigusamninginn sem fjármögnunarleigusamning ef gerð leigusamnings er stillt á sjálfvirkni og ef núvirði á leigugreiðslum í framtíðinni yfir gangvirði eignarinnar er meira en eða jafnt og prósentan sem gefin er upp hér.

  - **Skammtímaleigusamningur** - Ef leigutíminn er minni en eða jafn skilgreindu virði, verður leigusamningurinn flokkaður sem skammtímaleigusamningur.

  - **Verðlítið** - Ef gangvirði eignar er minna en eða jafnt og skilgreindu virði, verður eignin flokkuð sem leiga verðlítillar eignar.

  - **Flokkun og færslur leigusamnings** Flokkun leigusamnings er sjálfvirkt ferli til að flokka leigusamninga samkvæmt skilgreindum mörkum í bókum fyrir utan önnur skilyrði prófunarflokkunar til að greina leigusamninginn sem fjármögnunarleigusamning, rekstrarleigusamning, skammtímaleigusamning eða leigusamning verðlítillar eignar. Þetta er einnig notað til að auðkenna hvort ferli frestaðra leigugreiðslna er fylgt eftir.

Flokkunarprófanir fela í sér flutning á eignarhaldi, kaupmöguleika, leigutíma, núvirði og einstaka eign. Eftirfarandi skýringarmynd sýnir prófun leigusamningsflokkunar.

[![Prófun leigusamningsflokkunar](./media/overview-03.png)](./media/overview-03.png)

Hver gerð leigusamnings meðhöndlar bókhaldið á ólíkan hátt fyrir mismunandi leigufærslur. Færslurnar fela í sér upphaflega skráningu, vaxtakostnað, gjaldfallna greiðslu á leigu og afskrift leigusamnings og þær fylgja reikningsskilastöðlum sem þú fylgir (IFRS 16 eða ASC 842). Fjárhagslyklar eru skilgreindir samkvæmt bókunarreglu leigusamningsins fyrir hverja færslugerð og bókhaldsramma.

## <a name="asset-leasing-transactions"></a>Færslur eignarleigu

#### <a name="initial-recognition"></a>Upphafleg skráning 
Upphafleg skráning á leigðri eign notar reiknað núvirði svo hægt sé að gefa það upp í efnahagsreikningnum. Bókhaldsfærslan fyrir þetta er búin til sjálfkrafa. Þessi færsla debetfærir lykilinn fyrir afnotarétt af eign og kreditfærir skuldbindingalykil rekstrarleigusamnings eins og hér segir. Ef eign er tengd leigusamningnum, mun upphafleg skráningarfærsla endurspegla eignakaup. Í þessu tilfelli þarf að skilgreina bókunarreglu eigna til að bóka lykil fyrir afnotarétt af eign. 

> [!NOTE]
> Rekstrarleigusamningar eru aðeins studdir af US GAAP ASC 842.

|     Gerð                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Rekstrarleigusamningur samkvæmt US GAAP              |     Afnotaréttur af eign      |     Skuldbinding rekstrarleigusamnings       |
|     Fjármögnunarleigusamningur samkvæmt IFRS og US GAAP        |     Afnotaréttur af eign      |     Skuldbinding rekstrarleigusamnings       |

#### <a name="lease-liability-amortization-interest-expense"></a>Afskrift leiguskuldbindingar (vaxtakostnaður) 
Vextir fyrir leigusamning eru skráðir með því að reikna út vexti fyrir upphafsstöðu leigusamningsins, leigugreiðslu tímabils, vexti á lánsfé og samsett tímabil á ári. Vaxtaupphæðin eykur skuldbindingu á lykli rekstrarleigusamnings með því að kreditfæra hann, sem kemur fram í efnahagsreikningi fyrirtækisins. Færslan felur einnig í sér debetfærslu á lykli vaxtakostnaðar sem kemur fram á rekstraryfirlitinu fyrir fjármagnsleigusamninga og á kostnaðarlykli leigusamnings fyrir rekstrarleigusamninga.

|     Gerð                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Færsla skuldbindingar rekstrarleigusamnings samkvæmt US GAAP ASC 842    |     Vaxtakostnaður          |     Skuldbinding rekstrarleigusamnings         |
|     Færsla skuldbindingar fjármögnunarleigusamnings samkvæmt IFRS og US GAAP      |     Vaxtakostnaður          |     Skuldbinding fjármögnunarleigusamnings           |

#### <a name="accrued-lease-payment"></a>Uppsöfnuð leigugreiðsla
Uppsöfnuð leigugreiðsla er viðurkennd sem framtíðargreiðsla leigutaka sem unnið verður úr sem greiðslufærsla úr banka- eða sjóðsreikningum. Gjaldfallin leigugreiðsla minnkar leiguskuldbindingu með því að debetfæra lykil leiguskuldbindingar á móti hvort undirbók lánardrottins, í því tilfelli þegar leigutaki er skilgreindur sem lánardrottinn, eða bókun kredithluta á fjárhagslykil víxilskuldar, þá verður greiðslan framkvæmd á móti annaðhvort lánardrottni eða víxilskuld.

|     Gerð                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Rekstrarleigusamningur samkvæmt US GAAP              |  Skuldbinding rekstrarleigusamnings    |   Skuldbinding lánardrottins (undirbók)/Víxilskuld  |
|     Fjármögnunarleigusamningur samkvæmt IFRS og US GAAP        |  Skuldbinding fjármögnunarleigusamnings      |   Skuldbinding lánardrottins (undirbók)/Víxilskuld  |

#### <a name="asset-depreciation"></a>Afskrift eigna
Afnotaréttur af eign er afskrifaður á þeim tíma sem er styttri - nýtingartíma eignar eða leigusamning. Aðferðin til að reikna afskriftir fyrir GAAP (ASC 842) byggist á mismun á línulegum leigukostnaði og vaxtaupphæð. Vextir á fjármagnsleigusamningi eru reiknaðir með því að nota hefðbundna línulega aðferð. Leiguafskriftir hafa áhrif á rekstraryfirlitið með því að debetfæra vaxtakostnað. Efnahagsreikningurinn verður fyrir áhrifum vegna kreditfærslu á lykli fyrir afnotarétt af eign fyrir fjármögnunarleigusamninga. Fyrir rekstrarleigusamninga er afskriftin að kreditfæra kostnaðarlykil leigusamningsins. Ef leigusamningurinn er tengdur við eign verða afskriftarfærslurnar keyrðar úr eignaeiningunni eingöngu. 

|     Gerð                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Rekstrarleigusamningur samkvæmt US GAAP              |  Leigukostnaður                |   Uppsafnaðar afskriftir afnotaréttar eignar     |
|     Fjármögnunarleigusamningur samkvæmt IFRS og US GAAP        |   Afskrift af kostnaði vegna afnotaréttar af eign   |   Uppsafnaðar afskriftir afnotaréttar eignar    |

#### <a name="short-term-lease"></a>Skammtímaleiga
Litið er á skammtímaleigu sem kostnað, sem mun hafa áhrif á rekstrarreikning fyrirtækis. Myndaðar leigugreiðslur á gjalddaga munu debetfæra kostnaðarlykil leigusamnings og kreditfæra víxilskuldir eða fjárhagslykil undirbókar.

|     Gerð                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Færsla skammtímaleiga samkvæmt IFRS og US GAAP     |  Leigukostnaður                |   Skuldbinding lánardrottins (undirbók)/Víxilskuld  |

#### <a name="low-value-lease"></a>Lágvirðiseign
Litið er á leigu verðlítillar eignar sem kostnað sem mun hafa áhrif á rekstrarreikning fyrirtækisins. Myndaðar leigugreiðslur á gjalddaga munu debetfæra kostnað leigusamnings og kreditfæra víxilskuldir eða undirbók lánardrottins.

|     Gerð                                          |     Debet                     |     Kredit                            |
|-----------------------------------------------    |-----------------------------  |------------------------------------   |
|     Færsla lágvirðiseignar samkvæmt IFRS og US GAAP      |  Leigukostnaður                |   Skuldbinding lánardrottins (undirbók)/Víxilskuld  |


#### <a name="index-revaluation"></a>Endurmat vísitölu
Þetta er lykill eignarleigunnar fyrir breytilegar leigugreiðslur reiknaðar samkvæmt vaxtavísitölu. Breytingar á leigugreiðslum vegna breytinga á vaxtavísitölu teljast leiðrétting á leigusamningi samkvæmt IFRS 16. Leiguskuldbinding og afnotaréttur af eignum verða lagaðar til að taka nýju greiðslunar með í reikninginn. 

|     Gerð                                          |     Debet                             |     Kredit                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Færsla vegna endurmats á vísitölu samkvæmt IFRS við hækkun  |  Afnotaréttur af eign       |   Skuldbinding rekstrarleigusamnings |
|   Færsla vegna endurmats á vísitölu samkvæmt IFRS við lækkun  |  Skuldbinding rekstrarleigusamnings  |   Afnotaréttur af eign      |

Þegar greiðslur breytast vegna breytinga á vaxtavísitölunni, breytast aðeins breytilegar greiðslur nema frekari breytingar eru gerðar á sjóðstreymi, t.d. breyting á leigutíma sem tengist vöxtum samkvæmt US GAAP ASC 842.

#### <a name="lease-adjustment"></a>Leiðrétting leigusamnings
Eignarleiga leyfir breytingar á leigusamningum ef leigutímanum er breytt, leigusamningurinn er framlengdur eða ef aðrar kringumstæður koma upp þar sem leigusamningur þarfnast leiðréttingar. Leiðréttingar á leigusamningi eru bókaðar til að auka eða draga úr afnotarétti af eign og leiguskuldbindingu. Leiðréttingarferlið tekur á móti yfirfærðum lokastöðum á afskriftum skuldbindingar og eignastöðu á leiðréttingardeginum. Þegar leigusamningur er tengdur við eign verður leiðrétting á afnotarétti af eign bókuð með því að nota auðkennið sem úthlutað er í Eignum. 

|     Gerð                                          |     Debet                             |     Kredit                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Leiðréttingarfærsla leigusamnings fyrir IFRS og US GAAP vegna hækkunar     |  Afnotaréttur af eign       |   Skuldbinding rekstrarleigusamnings |
|   Leiðréttingarfærsla leigusamnings fyrir IFRS og US GAAP vegna lækkunar     |  Skuldbinding rekstrarleigusamnings  |   Afnotaréttur af eign      |


#### <a name="lease-impairment"></a>Virðisrýrnun leigusamnings
Þetta táknar minnkun á yfirfærðri stöðu á afnotarétti eignar. Auðkennið upphæð virðisrýrnunar, færsludagsetningu og eftirstandandi tímabil. Eftirstandandi afnotaréttur af eign verður afskrifaður samkvæmt línulegri aðferð. Reiknireglan um virðisrýrnun leigusamnings tekur til greina yfirfært virði eignar í afskriftaráætlun eignar.  

|     Gerð                                          |     Debet                             |     Kredit                    |
|-----------------------------------------------    |-------------------------------------  |----------------------------   |
|   Virðisrýrnunarfærsla fyrir IFRS og US GAAP           |  Kostnaður virðisrýrnunar                   |    Afnotaréttur af eign     |

>[!NOTE]
> Ef leigusamningurinn er tengdur við eign, verður virðisrýrnun leigusamningsins bókuð í Eignum vegna þess að afskrift eignar er keyrð í Eignakerfiseiningunni.

**Tvöfaldur gjaldmiðill** Leigufærslur er hægt að bóka í öðrum gjaldmiðli en bókhalds- og skýrslugjaldmiðli. Gengi gjaldmiðils er skilgreint í Fjárhagskerfinu á upphafsdeginum. Hægt er að breyta genginu með því að stilla reitinn **Fast gengi** á **Já** þegar leigusamningurinn er búinn til. Þegar leigufærslur eru færðar inn notar upphafleg skráning og væntanlegar afskriftarfærslur gengið frá upphafsdeginum. Síðari greiðslur og vaxtafærslur munu nota núverandi virkt gengi. 

## <a name="create-an-asset-lease"></a>Búa til leigusamning eignar
Ljúkið eftirfarandi skrefum til að stofna nýja leigu. 

1. Til að nota **Eignarleigu** þarf að virkja hana á vinnusvæðinu **Eiginleikastjórnun**. Á vinnusvæðinu **Eiginleikastjórnun** skal velja **Allir** þannig að allir eiginleikar koma fram á síðunni. Veljið **Eignarleiga** og síðan **Virkja núna**.
2. Farið í **Eignarleiga > Almennt > Samantekt leigu**. Fylltið út nauðsynlega reiti í flýtiflipanum **Almennt**. 
   - **Upplýsingar um leigu**
   - **Nýtingartími eignar (mánuðir)**
   - **Leigusamningsflokkur**
   - **Vextir á nýju lánsfé (%)**
   - **Samsett tímabil**
   - **Tegund afborgunar**
   - **Gjaldmiðill**
   - **Upphafsdagsetning**

3. Farið í flýtiflipann **Greiðsluáætlunarlínur** og færið inn greiðslulínu og veljið síðan **Stofna áætlanir**.

4. Veldu **Bækur**. 

5. Skiptið yfir í flýtiflipann **Almennt**. **Upphaflegur afnotaréttur af eign** og **leiguskuldbinding** eru reiknaðir út. 

6. Farið í flýtiflipann **Prófun leigusamningsflokkunar** til athuga gildið í reitnum **Gerð leigusamnings**. 

   Sjálfvirk **Gerð leigusamnings** er flokkuð samkvæmt skilyrðinu sem er skilgreint á síðunni **Bækur**.

7.  Farið í **Greiðsluáætlun** undir hlutanum **Virkni**.  

   Síðan **Greiðsluáætlun** sýnir greiðsluáætlanir í framtíðinni fyrir leigukenni. Veljið **Staðfesta áætlun** til að geta birt færslurnar **Upphafleg skráning**. 

[![Aðgerð upphaflegrar skráningar](./media/overview-13.png)](./media/overview-13.png)

8. Veljið **Upphafleg skráning** til að stofna fyrstu skráningarbók. 

9. Veljið **Eignarleigubækur** til að bóka fyrstu skráningarfærsluna. 

   Í greiðsluáætluninni er hægt að opna ítarlega síðu sem sýnir færslur afnotaréttar af eign. 
 
   **Afskriftaráætlun leiguskuldbindingar** sýnir vaxtaupphæðina sem er reiknuð fyrir hvert tímabil.
   
10. Stofnið færslubókina og farið svo í **Eignarleigubækur**. **Afskriftaráætlun leiguskuldbindingar** sýnir einnig vaxtafærslurnar.

   Síðan **Afskriftaráætlun eignar** sýnir afskriftarfærslurnar fyrir valið leigukenni. 

   [![Færslusíða afnotaréttar af eign](./media/overview-20.png)](./media/overview-20.png)

   Síðan **Færslur afnotaréttar af eign** sýnir upphaflega skráningu, uppsafnaðar afskriftir og eignastöðuna. 

   Síðan **Færslur leiguskuldbindingar** sýnir upphaflega skráningu, vaxtagreiðslur leigu, leigugreiðslur og stöðu leiguskuldbindingar. 

