---
title: "Leiðir og aðgerðir"
description: "Þetta efni veitir upplýsingar um leiðir og aðgerðir. Leið tilgreinir ferli fyrir framleiðslu á afurð eða afurðarafbrigði. Það lýsir hverju skrefi (aðgerð) í framleiðsluferlinu og pöntunin verður að framkvæma eftirfarandi skrefum í. Fyrir hvert skref er leiðin einnig skilgreinir nauðsynlegar aðgerðir tilfanga þarf uppsetningartíma og keyrslutíma, og hvernig kostnaður er reiknaður."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 556b9859d0b162b11f0bcbfc6552f6fd9a900596
ms.lasthandoff: 03/31/2017


---

# <a name="routes-and-operations"></a>Leiðir og aðgerðir

Þetta efni veitir upplýsingar um leiðir og aðgerðir. Leið tilgreinir ferli fyrir framleiðslu á afurð eða afurðarafbrigði. Það lýsir hverju skrefi (aðgerð) í framleiðsluferlinu og pöntunin verður að framkvæma eftirfarandi skrefum í. Fyrir hvert skref er leiðin einnig skilgreinir nauðsynlegar aðgerðir tilfanga þarf uppsetningartíma og keyrslutíma, og hvernig kostnaður er reiknaður.

<a name="overview"></a>Yfirlit
--------

Í framleiðsluleið lýsir þeirri röð aðgerða sem er krafist til að framleiða á afurð eða afurðarafbrigði. Fyrir hverja aðgerð á leiðinni einnig skilgreinir rekstrartilföngum sem krafist er, tímanum sem er krafist til að setja upp og framkvæma aðgerðina og hvernig kostnaður er reiknaður. Hægt er að nota sömu leið til að útbúa margar afurðir eða hægt er að skilgreina einkvæmt leið fyrir hverja afurð eða afurðarafbrigði. Enn er hægt að hafa margar leiðir til á sömu afurð. Í þessu tilfelli leið sem notuð er breytileg eftir þáttum eins og magn sem framleiða þarf. Skilgreining á leið í Microsoft Dynamics 365 aðgerða samanstendur af fjórum aðskildar einingar sem lýsa framleiðsluferlið saman:

-   **Leið** – leið skilgreinir skipulag framleiðsluferlið. Með öðrum orðum, það tilgreinir röð aðgerða.
-   **Aðgerð** – aðgerð auðkennir nefnd skref í leiðinni, eins og **Samsetningu**. Sama aðgerð getur átt sér stað í mörgum leiðum og geta haft mismunandi aðgerðanúmer.
-   **Aðgerðavensl** – aðgerðavensla skilgreinir aðgerð, eins og uppsetningartíma og keyrslutíma, kostnaðartegundir, færibreytur notkun og tilfangaþarfir aðgerðar eiginleikum. Aðgerðavenslin gerir rekstraráætlanagerðar eiginleikum eru breytilegir, eftir afurðir sem eru í framleiðslu eða leið sem aðgerðin er notað í aðgerð.
-   **Leiðarútgáfa** – leiðarútgáfu tilgreinir þá leið sem er notuð til að framleiða á afurð eða afurðarafbrigði. Leiðarútgáfur að virkja leiðir til að endurnota milli afurðir eða breyta tímanum. Þær gera einnig mismunandi leiðir til að nota til að framleiða á sömu afurð. Í þessu tilfelli, leið sem er notaður fer eftir þáttum staðsetningu eða magn sem framleiða þarf.

## <a name="routes"></a>Leiðir
Leið lýsir röð aðgerða sem er notuð til að framleiða á afurð eða afurðarafbrigði. Hver aðgerð er úthlutað aðgerðanúmer og þáttur aðgerð. Röð aðgerða skjámyndir leiðanet má tákna með beina línurit sem hefur eitt eða fleiri upphafsdagsetning punkta og eina endastöð. Í Dynamics 365 fyrir Aðgerðir, leiðir eru háttvirt samkvæmt skipulagsgerð. Tvær gerðir af leiðir eru einföldum leiðir og leiðarútgáfur net. Í færibreytum Framleiðslu stýringu hægt er að tilgreina hvort hægt er að nota aðeins einföld leiðir eða hvort hægt er að nota flóknari leiðanet.

### <a name="simple-routes"></a>Einföld leiðir

Einföld leið er röð og er aðeins ein byrjunarreit fyrir leiðina.  

[![Einföld leið](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Ef aðeins einföld leiðir í færibreytum Framleiðslu, virkja myndar Dynamics 365 fyrir Aðgerðir sjálfkrafa í aðgerðanúmer (10, 20, 30, o.s.frv) þegar skilgreina leið.

### <a name="route-networks"></a>Leiðanet

Ef flóknari leiðanet í færibreytur framleiðslustýringar, hægt er að skilgreina leiðum sem hafa mörg hafinn punkta og aðgerðir sem hægt er að keyra samhliða.  

[![Route network](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

**Athugasemdir :**

-   Hver aðgerð getur haft eina þáttur aðgerð og alla leið þarf að ljúka í einni aðgerð.
-   Það er engin ábyrgðarbréfs sem margar aðgerðir sem hafa sömu þáttur aðgerð (t.d., aðgerðir 40 í fyrrgreint sýnidæmi og 30) verður að keyra raunverulega samhliða. Framboð og getu á tilföng væri að setja hömlur á því hvernig aðgerðum er raðað.
-   Hægt er að nota 0 (núll) sem aðgerðarnúmer. Númerið er frátekið og er notað til að tilgreina síðasta aðgerðin í leiðinni hefur engin aðgerð næsta þáttar.

### <a name="parallel-operations"></a>Samhliða aðgerðir

Stundum samsetningu margra rekstrartilföngum sem hafa mismunandi eiginleika er krafist til að framkvæma aðgerð. Til dæmis samsetningu aðgerð útheimt vél, verkfæri og einn starfsmann fyrir hvern tveggja véla til að hafa umsjón aðgerðina. Þessu dæmi er miðuð með því að nota samhliða aðgerðum þar sem ein aðgerð er skráður sem aðalaðgerðin og hin eru aukaáherslu.  

[![Leið sem aðal-og aukaaðgerð](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Yfirleitt, aðalaðgerðin stendur fyrir tilfang flöskuháls og ákvarðar hverng keyrslutíma fyrir aukaaðgerðir. Hins vegar við röðun sem felur í sér takmarkaðrar, tilföng sem eru áætlaðar fyrir aðalaðgerðin og á aukaaðgerðir verður tiltækur og hafa frjálsum afkastagetu á sama tíma.  

Aðalaðgerðin og í aukaaðgerðum verða að hafa sama aðgerðarnúmer (30 í fyrrgreint sýnidæmi).  

Dæmið, tilfangaþörfina fyrir aðalaðgerðin (30) er á vél meðan tilfangaþarfirnar fyrir aukaaðgerðir (30' og 30'') eru forritið og starfsmanns. Fimmtíu - prósenta álags hjálpar til við að tryggja samræmda sem röðun starfsmanna geta hafa umsjón tveggja véla á sama tíma.

### <a name="approval-of-routes"></a>Samþykki á leiðum

Leið verður að vera samþykkt áður en hægt er að nota í ferli fjárhagsáætlunargerðar eða framleiðslufyrirtæki. Samþykki gefur til kynna hönnun leið hefur verið lokið. Sama losuð afurð eða útgefin afurðarafbrigði getur haft margar samþykktar leiðir. Yfirleitt, samþykki á leið á sér stað þegar fyrsta viðeigandi leiðaútgáfa samþykkt. Hins vegar í sumum business aðstæður, samþykki leiðina og leiðarútgáfuna eru aðskildar verkþætti sem snerta gætu mismunandi ferli eigendur.  

Hverrar leiðar getur samþykkt eða ósamþykkt sérstaklega. Athugið hins vegar, þegar leið er ósamþykkt eru allar tengdar leiðarútgáfur eru einnig ósamþykktar. Í færibreytum Framleiðslu stýringu hægt er að tilgreina hvort leiðir getur verið ósamþykkt og hvort hægt er að breyta leiðum.  

Ef um er að halda kladda sem færslur sem samþykkir hverrar leiðar er hægt að krefjast rafrænna undirskrifta fyrir samþykki á leiðinni. Notendur fái til að staðfesta auðkenni þeirra með því að nota við [rafrænna undirskrifta](/dynamics365/operations/organization-administration/electronic-signature-overview).

## <a name="operations"></a>Rekstur
Aðgerð er skref í framleiðsluferlinu. Hver aðgerð hefur Kenni og lýsingu á einföldum í Dynamics 365 fyrir Aðgerðir. Eftirfarandi töflur sýnir gott dæmi um aðgerðir úr vél verslunar.

| Aðgerð  | lýsing        |
|------------|--------------------|
| PipeCut    | Pipe klipping       |
| TIGweld    | TIG welding        |
| JigAssy    | Samsetning jig       |
| Eftirlit | Gæðaeftirlit |

Aðgerð, eins og uppsetningartíma og keyrslutíma, tilfangaþarfir, upplýsingar kostnaðarútreiknings og útreikningur notkunar aðgerðar eiginleika eru tilgreind í aðgerðavenslin. (Frekari upplýsingar um aðgerðavensl sjá hlutann næstu.)

## <a name="operation-relations"></a>Aðgerðavensl
Eftirfarandi eiginleikar rekstraráætlanagerðar aðgerðar er haldið við í aðgerðavenslin:

-   Kostnaðartegundir
-   Færibreytur fyrir notkun
-   Vinnslutíma
-   Magn í vinnslu
-   Tilfangaþörf
-   Athugasemdir og leiðbeiningar

Hægt er að skilgreina margar aðgerðavensl fyrir sömu aðgerð. Hins vegar hver aðgerðavensl við eina aðgerð og vistar eiginleika sem tengjast leið, losaðar afurðir eða safn útgefnar afurðir sem eru tengdar við flokk vöru. Þess vegna er hægt að nota sömu aðgerð í mörgum leiðum sem hafa mismunandi rekstraráætlanagerðar eiginleika. Þar að auki er hægt auðveldara að viðhalda skal aðalgögn ef um er að nota staðlaðar aðgerðir sem hafa sömu eiginleika rekstraráætlanagerðar, óháð leið sem er notuð og vara sem er framleidd. Svið aðgerðavenslin er skilgreind í gegnum í **Vörukóði**, **Vöruvensl**, **Leið kóða** og **Leið vensl** eiginleika, eins og sýnt er í eftirfarandi töflu.

| Vörukóði | Vöruvensl         | Leiðarkóði | Leiðarvensl   | Svið aðgerðavenslin                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tafla     | &lt;Vörukenni&gt;       | Leið      | &lt;Auðkenni leiðar&gt; | Um eiginleikum aðgerð þegar hann er notaður í leiðinni þar sem **Leiðarnúmer**=&lt;leiðarkenni&gt; til að framleiða útgefin afurð þar sem **Vörunúmer**=&lt;vörukenni&gt;.                                                                                                                        |
| Tafla     | &lt;Vörukenni&gt;       | Allir lyklar        |                  | Sjálfgefin rekstraráætlanagerðar eiginleikum aðgerð þegar hún er notuð til að framleiða útgefin afurð þar sem **Vörunúmer**=&lt;vörukenni&gt;. Með öðrum orðum þessir eiginleikar rekstraráætlanagerðar eiga við þegar engin tengsl eru sérstaklega leið aðgerð fyrir losaða afurð.                                     |
| Hópur     | &lt;Kenni vöru&gt; | Leið      | &lt;Auðkenni leiðar&gt; | Rekstraráætlanagerðar eiginleikum aðgerð þegar hann er notaður í leiðinni þar sem **Leiðarnúmer**=&lt;leiðarkenni&gt; til að framleiða útgefnu afurðanna sem tengjast vöruflokkum &lt;vörukenni flokk&gt;, nema það sé tiltekin leið aðgerðavensl fyrir losaða afurð.                         |
| Hópur     | &lt;Kenni vöru&gt; | Allir lyklar        |                  | Sjálfgefin rekstraráætlanagerðar eiginleikum aðgerð þegar hún er notuð til að framleiða útgefnu afurðanna sem tengjast vöruflokkum &lt;vörukenni flokkur&gt;, nema nákvæmari aðgerðavensl til.                                                                                                  |
| Allir lyklar       |                       | Leið      | &lt;Auðkenni leiðar&gt; | Sjálfgefin rekstraráætlanagerðar eiginleikum aðgerðina þegar hann er notaður í leiðinni þar sem **Leiðarnúmer**=&lt;leiðarkenni&gt;. Með öðrum orðum þessir eiginleikar rekstraráætlanagerðar eiga við þegar það er engin aðgerðavensl fyrir þessa leið sem tilheyra annaðhvort útgefin afurð eða hún er með tengda vöruflokk. |
| Allir lyklar       |                       | Allir lyklar        |                  | Sjálfgefin rekstraráætlanagerðar eiginleikum aðgerð. Þessir eiginleikar rekstraráætlanagerðar gilda þegar nákvæmari aðgerðavensl er ekki til.                                                                                                                                                                |

Einnig er hægt að tilgreina aðgerðavensla er bundinn við svæði. Á þennan hátt er rekstraráætlanagerðar eiginleikum aðgerð geta verið mismunandi, eftir staðsetningu (sem er í svæði) þar sem aðgerðin er framkvæmd. Fyrir skilgreindar vörur má einnig að tilgreina mismunandi um eiginleika fyrir hvert afurðarafbrigði.  

Aðgerðavensl gefið lotur sveigjanleika þegar skilgreina skal leiðir. Þar að auki er kleift að skilgreina sjálfgefna eiginleika hjálpar til við að draga úr fjölda aðalgögn sem þarf að vinna með. Hins vegar sveigjanleika þetta þýðir líka að sem verður að hafa í huga samhengi sem aðgerðavensla í að breyta.  

**Athugasemd:** Því rekstraráætlanagerðar eiginleikar eru geymd í aðgerðavensl fyrir hverja aðgerð á leiðinni, öll tilvik af sömu aðgerð (t.d. Samsetningu) hafa sama uppsetningartíma, keyrslutíma, tilfangaþarfir og svo framvegis. Þess vegna ef tveggja tilvika aðgerðar verður koma í sömu leið en hafa mismunandi keyrðar oft þarf að stofna einkvæmrar aðgerðir, eins og Assembly1 og Assembly2.

### <a name="modifying-product-specific-routes"></a>Breyta afurðabundnar leiðir

Þegar opna í **Leið** frá síðunni á **Losuð afurðarupplýsingar** síðu leiðarútgáfur sem eru tengdar við valda afurð losuð eru sýndar. Í þessu samhengi fyrir hverja aðgerð Dynamics 365 aðgerða sýnir rekstraráætlanagerðar eiginleikum úr aðgerðavenslin sem samsvarar best leiðarútgáfuna. Álagsritsins verður að innihalda lista yfir aðgerðir í **Vörukóði** og **Leið kóða** eiginleikar úr aðgerðavenslin. Þess vegna er hægt að ákvarða hvaða aðgerðavensl er sýnd.  

Í í **Leið** síðu er hægt að breyta eiginleikum rekstraráætlanagerðar aðgerð keyrslutíma eða kostnaðartegundir. Breytingarnar eru vistaðar í aðgerðavensl við leiðina og útgefin afurð sem vísað er í gildandi leiðarútgáfu. Ef aðgerðavensl sem sýndur er ekki við leiðina og útgefin afurð áður en breytingar eru vistaðar, sem kerfið býr til afrit af aðgerðavenslin. Þessi afrit *er* sérstaklega við um leið og útgefin afurð. Því eru breytingarnar ekki áhrif á aðrar leiðir eða útgefnum afurðum. Til að staðfesta venslin sem aðgerðin hefur verið breytt á í **Leið** síðunni, þvínæst á **Vörukóði** og **Leið kóða** svæði.  

Einnig handvirkt er hægt að stofna aðgerð sem er sérstaklega við um leið og útgefin afurð með því að nota í **Afrita og breyta venslum** aðgerð.  

**Athugasemd:** Ef bæta við nýrri aðgerð í leið á í **Leið** síðu aðgerðavensla er stofnað aðeins fyrir gildandi útgefin afurð. Þess vegna ef leið er einnig notuð til að útbúa aðra útgefnar afurðir, engin tengsl við aðgerð verða til fyrir þær útgefnar afurðir og ekki lengur hægt að nota leið fyrir þær útgefnar afurðir.

### <a name="maintaining-operation-relations-per-route"></a>Viðhald aðgerðavensl fyrir leið

Þegar opna í **Leiðarupplýsingar** frá síðunni á **Leiðir** listasíðu, birtist listi yfir allar aðgerðavensl sem eiga við valda leið. Þess vegna er auðveldlega hægt að staðfesta hvaða aðgerðar eiginleikar eru notaðir fyrir hvaða afurðir. Hægt er að breyta eiginleika sjálfgildi og gildi eiginleika afurðabundnar.  

Ný aðgerðavensl er bætt við á á **Leiðarupplýsingar** síðu í **Leið kóða** er sjálfkrafa stillt á **Leið**, og **Leið vensl** er stillt á leið númer gildandi leið.

### <a name="maintaining-operation-relations-per-operation"></a>Umsjón með aðgerðavensl fyrir hverja aðgerð

Úr í **Aðgerðir** síðu er hægt að opna í **aðgerðavensl** síðu. Á þessari síðu er hægt að breyta öllum aðgerðavensl fyrir tilgreindu aðgerðina. Hægt er að breyta jafnvel aðgerðavensl sem innihalda sjálfgefin gildi.  

Ef fyrirtækið notar staðlaðar aðgerðir og ef um færibreytur eru þau sömu fyrir allar afurðir og ferli, sem **aðgerðavensl** síða gefur þægileg leið til að viðhalda sjálfgefnum rekstraráætlanagerðar eiginleikum þær aðgerðir.

### <a name="applying-operation-relations"></a>Beita aðgerðavensl

Í sumum tilfellum Dynamics 365 fyrir Aðgerðir verður að finna rekstraráætlanagerðar eiginleika fyrir aðgerð. Til dæmis þegar innkaupapöntun er stofnuð um eiginleikum hverri aðgerð verður að afrita úr vensl aðgerða í framleiðsluleiðinni. Í þessum kringumstæðum er leitar Dynamics 365 fyrir Aðgerðir í viðeigandi aðgerðavensl úr sérstakasta samsetningu að samsetningin.  

Þegar Dynamics 365 fyrir Aðgerðir leitar viðeigandi aðgerðavensl fyrir losaða afurð aðgerðavensla sem samsvarar Vörukenni útgefin afurð er forgangs yfir aðgerðavensla sem samsvarar vöruflokk kenni. Upphafspunkti aðgerðavensla sem samsvarar Flokkskenni vöru er æskilegur yfir aðgerðavensl sjálfgefið. Leitin er gert í eftirfarandi röð:

1.  **Vörukóði**=**Töfluna** og **Vöruvensl**=&lt;vörukenni&gt;
2.  **Vörukóði**=**Flokkur** og **Vöruvensl**=&lt;Auðkenni vöru&gt;
3.  **Vörukóði**=**Allar**
4.  **Leið kóða**=**Leið** og **Leið vensl**=&lt;Kenni leiðar&gt;
5.  **Leið kóða**=**Allar**
6.  **Skilgreining**=&lt;Skilgreiningarkenni&gt;
7.  **Configuration**=
8.  **Svæði**=&lt;setri Kenni&gt;
9.  **Site**=

Þess vegna aðgerð á að nota aðeins einu sinni fyrir hverja leið. Ef aðgerðin margsinnis í sömu leið er öllum tilvika sem aðgerðin mun hafa sama aðgerðavensl og er ekki hægt að hafa aðra eiginleika (til dæmis keyrslu) fyrir hvert tilvik.

## <a name="route-versions"></a>Leiðarútgáfur
Útgáfur leiða eru notaðar til að hýsa tilbrigði í framleiðslunni afurðir eða veita meiri stjórn yfir framleiðsluferlinu. Þeir skilgreina leið sem á að nota þegar tiltekin afurð losuð eða losuð afurðarafbrigði er framleidd. Hægt er að nota eftirfarandi skorður til að skilgreina leið sem er notað fyrir losaða afurð:

-   Afurðavíddir (stærð, lit, stílum eða afbrigði)
-   Framleiðslumagn
-   Framleiðslusvæði
-   Dagsetning framleiðslu

Þegar verið er að framleiða vöru á ákveðnu svæði í ákveðið magn eða á tilteknu tímabili, er hægt að úthluta ákveðinni leiðarútgáfu viðkomandi útgáfu sem sjálfgefna leið. Athugið hins vegar að aðeins ein virk leið er leyfð fyrir tiltekið útgefin afurð og tiltekið safn skorður.  

Í færibreytum Framleiðslu stýring má krefjast gildistíma leiðarútgáfu alltaf að vera tilgreint.

### <a name="approval-of-route-versions"></a>Samþykkja útgáfur leiða

Áður en hægt er að nota leiðarútgáfu í áætlun eða framleiðslu í vinnslu, það verður að vera samþykkt. Þegar leiðaútgáfa er samþykkt, einnig er hægt að samþykkja tengdar leið. Athugið hins vegar hægt að samþykkja útgáfu leiðar ef sem tengd er einnig leiðina.

### <a name="activating-the-default-route-version"></a>Virkja sjálfgefna leiðarútgáfu

Þegar leiðaútgáfa er virkjuð er að tilgreina hann sem nota sjálfgefna leiðarútgáfan sem sniðmát fjárhagsáætlunargerðar, eða sem verður notað til að stofna framleiðslupantanir. Hægt er að hafa aðeins ein virk leiðarútgáfa fyrir tiltekið safn skorður (til dæmis, tímabil, svæði eða magn). Ef útgáfan sem verið er að reyna að virkja rekst á við útgáfu sem er þegar virk berast villuskilaboð. Til að koma í veg fyrir að tvíræðrar virkjun, síðan annaðhvort verður rákust útgáfa gera eða breyta skorðum (yfirleitt tímabilið) í leiðarútgáfu.

### <a name="electronic-signatures"></a>Rafrænar undirskriftir

Ef þarf er að halda kladda sem færslur sem samþykkir og virkjar hverja leiðarútgáfa er hægt að krefjast rafrænna undirskrifta fyrir þessi verk. Notendur sem samþykkja og virkja leiðaútgáfur svo þarf að staðfesta auðkenni þeirra með því að nota við [rafrænna undirskrifta](/dynamics365/operations/organization-administration/electronic-signature-overview).

### <a name="product-change-that-uses-case-management"></a>Breyting á afurð sem notar málastjórnunar

Afurðin afurðarbreytingamál fyrir samþykki og virkjun nýir eða breyttir leiðir og leiðarútgáfur gefur auðveld leið til að sjá yfirlit yfir skorður útgáfu leiðar. Einnig er hægt að samþykkja og virkja allar leiðir sem eru tengdar við tiltekinn breytt í einni aðgerð og niðurstöðum í afurðarbreytingamálið skjals.

## <a name="maintaining-routes"></a>Umsjón með leiðum
Eftir ykkar, gæti verið hægt að minnka framlag sem er krafist til að vinna með skilgreiningar á vinnslu.

### <a name="making-routes-independent-of-resources"></a>Gera leiðir óháð tilföng

Í mörgum kerfum aðgerðir tilfang eða tilfangaflokkur sem á að framkvæma aðgerð að vera tilgreint í leiðinni. Hins vegar í Dynamics 365 fyrir Aðgerðir sem hægt er að skilgreina safn þarfir aðgerðir tilfanga verður að uppfylla sem við á fyrir aðgerðina. Þess vegna tiltekinna aðgerða tilfang eða tilfangaflokkur sem á að nota er ekki með til að ákvarða fyrr en er aðgerðinni raðað raun. Þessi virkni er sérlega gagnleg þegar mörgum starfsmönnum eða vélum sem getur unnið sömu aðgerð.  

Til dæmis tilgreina aðgerð krefst inn rekstrartilföng af á **Vélar** sem hefur í **Stamping** getu 20 tonnum. Áætlunarkerfið verður geta síðan leyst úr þessar þarfir til tiltekinna aðgerða tilfang eða tilfangaflokkur þegar aðgerðin er áætluð. Þar sem einungis er hægt að tilgreina þessar þarfir bindingaraðgerð á vél á tilteknum stað, hafa mikið sveigjanlegri. Þar að auki, viðhald er auðveldara þegar tilföng eru fluttar eða ný tilföng er bætt við.  

Nánari upplýsingar um mismunandi gerðir af tilfangaþarfir og hvernig á að nota þær í tilfangaþarfir Aðgerða og [tilfangagetu](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Samnýta leiðir á milli setra

Ef að framleiða á sömu afurð á fleiri en einu svæði framleiðslu og ef skrefin fyrir framleiðslu á vöru eru þau sömu í öllum sites oft er hægt að hanna samnýtta leið sem notuð er á milli allra framleiðslusvæði. Til að stofna samnýtt leið er ekki að tilgreina svæði á leiðinni sjálfri. Hins vegar þarf samt að stofna leiðarútgáfu sem tengir samnýtta leið við afurð á hverju svæði.  

Verður einnig að tryggja tilfangaþarfir fyrir hverja aðgerð í leiðinni ekki hringja fyrir tilföng sérstakar aðgerðir eða tilfangaflokka, en í staðinn er tilgreindur í einkenni þarf tilföng. Áætlunarkerfið síðan verður að úthluta viðeigandi rekstrartilföngum úr því svæði sem framleiðslu er raðað. Til dæmis ef eru örlítið mismunandi í keyrslutíma eða ef uppsetningartíma fyrir tiltekna aðgerð er ekki svæðisbundið er hægt að tilgreina þessar upplýsingar með því að bæta fleiri aðgerðavensl fyrir þá svæði.  

Til fulls fríðindi samnýtta leiðir, ætti einnig nota tilfanganotkun á samsvarandi uppskrift (BOM). Þegar þú flaggið fyrir tilfanganotkun í uppskriftarlínunni, vöruhús og staðsetning sem á að nota hráefni frá er inferred úr rekstrartilföng sem er aðgerðinni raðað á. Þess vegna vöruhús og staðsetning vinnukortaheimild ekki til að ákvarða þar til framleiðslunni er raðað raun. Á þennan hátt er hægt að gera Uppskrift og leið óháð efnisleg staðsetning þar sem varan er framleidd.

### <a name="standard-operation-relations"></a>Stöðluð aðgerðavensl

Ef fyrirtækið notar staðlaðar aðgerðir í gegnum framleiðslu sé minnstu eða engin afbrigði uppsetningartíma, keyrslutíma útreikningur notkunar kostnaðarútreikning, og svo á, gæti borgað stofnun sjálfgefna aðgerðavensl fyrir allar aðgerðir. Í þessu tilfelli koma í veg fyrir stofnun aðgerðavensl sem eiga við allar leið eða losuð afurð.  

Ef einnig express tilfangaþarfir hæfni og getu, og gera notanda leiðir óháð svæði, sem geta hjálpað til við halda áframhaldandi viðhald viðskiptaferlunum að lágmarki.  

Þegar þessi aðferð er notuð í **aðgerðavensl** síðu verður skal aðal áfangastaður viðhald keyrslutíma og öðrum eiginleikum.

### <a name="resource-specific-process-times"></a>Vinnslutímar tiltekin tilföng

Ef ekki er aðgerðir tilfang eða tilfangaflokkur sem hluti af tilfangaþarfir fyrir aðgerð, gæti verið viðeigandi tilföng vinna á mismunandi kerfishraða. Þess vegna tíma sem þarf til að vinna úr aðgerð sérð. Til að leysa þetta vandamál er hægt að nota í **Formúlu** á aðgerðavensl til að tilgreina hvernig vinnslutími er reiknaður. Eftirtaldir valkostir eru í boði:

-   **Stöðluð** – (Sjálfgefinn valkostur) útreikningurinn notar aðeins svæði úr aðgerðavenslin og multiplies tilgreinda keyrslutíma með pöntunarmagn.
-   **Afkastageta** – útreikningurinn inniheldur á **Afkastagetu** úr aðgerðir tilfanga. Þess vegna er tíma tilfanga-háð. Gildið sem tilgreint er á aðgerðum tilfanga er afkastageta á klukkustund. Þetta gildi er margfaldað með pöntunarmagn og **Stuðull** gildi úr aðgerðavenslin.
-   **Runa** – afkastagetu í runu er reiknað með því að nota upplýsingar úr aðgerðavenslin. Fjöldi runur og vinnslutími síðan reiknast út á pöntunarmagninu.
-   **Tilfangaruna** – Þessi valkostur er nokkurn vegin eins og í **Runu** valkost. Hins vegar útreikningurinn inniheldur á **Runu afkastagetu** úr aðgerðir tilfanga. Þess vegna er tíma tilfanga-háð.


<a name="see-also"></a>Sjá einnig
--------

[Bills of materials and formulas](bill-of-material-bom.md)

[Cost categories used in production routing](../cost-management/cost-categories-used-production-routings.md)

[Resource capabilities](resource-capabilities.md)

[Electronic signature overview](/dynamics365/operations/organization-administration/electronic-signature-overview)


