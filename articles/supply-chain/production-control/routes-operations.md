---
title: Leiðir og aðgerðir
description: Þessi efnisatriði gefur upplýsingar um leiðir og aðgerðir.
author: sorenva
manager: tfehr
ms.date: 03/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesigner, BOMDesignerRouteVersion, Route, RouteInventProd, RouteOpr, RouteOprTable, ProdRouteJob, ProdRouteTrans, ProdRouteOverview, ProdRouteJobOverview, ProdRouteJobListPagePreviewPane, RouteTable, RouteVersionFeasibility, ProdRouteJobCurrent, RouteGroup, RouteProductionOrder, EngChgCaseRouteTablePart, EcoResProductProdTypeFormulaNoActiveRouteFormPart,
ms.author: sorenand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 268124
ms.assetid: f78d5836-3e71-42b7-a5d1-41f19228d9d2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adf890f5305f4e6a62c2d7527ff3b593ed61eff3
ms.sourcegitcommit: c55fecae96b4bb27bc313ba10a97eddb9c91350a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/12/2020
ms.locfileid: "3989242"
---
# <a name="routes-and-operations"></a>Leiðir og virkni

[!include [banner](../includes/banner.md)]

Þessi efnisatriði gefur upplýsingar um leiðir og aðgerðir. Leið tilgreinir ferli fyrir framleiðslu á afurð eða afurðarafbrigði. Hún lýsir hverju skrefi (aðgerð) í framleiðsluferlinu og röðina sem framkvæma verður þessi skref í. Fyrir hvert skref skilgreinir leiðin einnig nauðsynlegar aðgerðir tilfanga, áskilinn uppsetningartíma og keyrslutíma og hvernig kostnaður er reiknaður.

<a name="overview"></a>Yfirlit
--------

Leið lýsir þeirri röð aðgerða sem er krafist til að framleiða afurð eða afurðarafbrigði. Fyrir hverja aðgerð skilgreinir leiðin einnig rekstrartilföng sem krafist er, tímann sem er krafist til að setja upp og framkvæma aðgerðina og hvernig kostnaður er reiknaður. Hægt er að nota sömu leið til að útbúa margar afurðir eða hægt er að skilgreina einkvæma leið fyrir hverja afurð eða afurðarafbrigði. Jafnvel er hægt að hafa margar leiðir fyrir sömu afurð. Í þessu tilfelli er leiðin sem notuð er breytileg eftir þáttum eins og því magni sem framleiða þarf. Skilgreining á leið í Supply Chain Management samanstendur af fjórum aðskildum einingum sem lýsa framleiðsluferlinu saman:

- **Leið** – leið skilgreinir skipulag framleiðsluferlis. Með öðrum orðum, hún tilgreinir röð aðgerða.
- **Aðgerð** – aðgerð auðkennir nefnd skref í leiðinni, eins og **Samsetningu**. Sama aðgerð getur átt sér stað í mörgum leiðum og getur haft mismunandi aðgerðanúmer.
- **Aðgerðavensl** – aðgerðavensl skilgreina aðgerðareiginleika, eins og uppsetningartíma og keyrslutíma, kostnaðartegundir, notkunarfæribreytur og tilfangaþarfir. Aðgerðavenslin virkja að aðgerðareiginleikar rekstraráætlanagerðar eru breytilegir, eftir leið sem aðgerðin er notuð í eða þeim afurðum sem verið er að framleiða.
- **Leiðarútgáfa** – Leið lýsir þeirri röð aðgerða sem er krafist til að framleiða afurð eða afurðarafbrigði. Leiðarútgáfur virkja leiðir til að endurnota milli afurðir eða breytast með tímanum. Þær gera einnig mismunandi leiðir virkar til að nota til að framleiða sömu afurð. Í þessu tilfelli fer leið sem notuð er eftir þáttum eins og staðsetningu eða magn sem framleiða þarf.

## <a name="routes"></a>Leiðir
Leið lýsir þeirri röð aðgerða sem er notuð til að framleiða afurð eða afurðarafbrigði. Hverri aðgerð er úthlutað aðgerðanúmeri og arftakaaðgerð. Röð aðgerða mynda leiðanet sem hægt er að tákna með stýrðu línuriti sem hefur einn eða fleiri upphafsdagsetningarpunkta og eina endastöð. Í Supply Chain Management eru leiðir aðgreindar samkvæmt skipulagsgerð. Tvær gerðir af leiðum eru einfaldar leiðir og leiðanet. Í færibreytum Framleiðslustýringar er hægt að tilgreina hvort aðeins er hægt að nota einfaldar leiðir eða hvort hægt er að nota flóknari leiðanet.

### <a name="simple-routes"></a>Einfaldar leiðir

Einföld leið er raðbundin og er aðeins einn byrjunarreitur fyrir leiðina.  

[![Einföld leið](./media/routes-and-operations-1-simple-route.png)](./media/routes-and-operations-1-simple-route.png)  

Ef aðeins einfaldar leiðir eru virkjaðar í færibreytum Framleiðslustýringar, myndar Supply Chain Management sjálfkrafa aðgerðanúmer (10, 20, 30, o.s.frv) þegar þú skilgreinir leið.

### <a name="route-networks"></a>Leiðanet

Ef flóknari leiðanet eru virkjuð í færibreytum framleiðslustýringar, er hægt að skilgreina leiðir sem hafa marga upphafspunkta og aðgerðir sem hægt er að keyra samhliða.  

[![Leiðanet](./media/routes-and-operations-2-route-network.png)](./media/routes-and-operations-2-route-network.png)  

> [!NOTE]
> - Hver aðgerð getur aðeins haft eina arftakaaðgerð og allri leiðinni þarf að ljúka í einni aðgerð.
> - Þetta tryggir ekki að margar aðgerðir sem hafa sömu arftakaaðgerð (t.d. aðgerðir 30 og 40 í fyrrgreint sýnidæmi) verði í raun keyrðar samhliða. Framboð og geta tilfanga geta sett hömlur á það hvernig aðgerðum er raðað.
> - Ekki er hægt að nota 0 (núll) sem aðgerðarnúmer. Númerið er frátekið og er notað til að tilgreina að síðasta aðgerðin í leiðinni hefur engin aðgerð næsta þáttar.

### <a name="parallel-operations"></a>Samhliða aðgerðir

Stundum er samsetningar margra rekstrartilfönga sem hafa mismunandi eiginleika krafist til að framkvæma aðgerð. Til dæmis getur samsetning aðgerða útheimt vél, verkfæri og einn starfsmann fyrir hverjar tvær vélar til að hafa umsjón með aðgerðinni. Þetta dæmi er hægt að setja upp í líkan með því að nota samhliða aðgerðir þar sem ein aðgerð er skráð sem aðalaðgerðin og hinar eru aukaáherslu.  

[![Leið sem hefur aðal-og aukaaðgerðir](./media/routes-and-operations-3-parallel-operations.png)](./media/routes-and-operations-3-parallel-operations.png)  

Yfirleitt stendur aðalaðgerðin fyrir tilfangaflöskuháls og ákvarðar keyrslutíma fyrir aukaaðgerðir. Hins vegar við röðun sem felur í sér takmarkaðra getu, verða tilföng sem eru áætluð fyrir bæði aðalaðgerðina og aukaaðgerðir að vera tiltæk og hafa frjálsa afkastagetu á sama tíma.  

Aðalaðgerðin og aukaaðgerðir verða að hafa sama aðgerðarnúmer (30 í fyrrgreindu sýnidæmi).  

Í dæminu hér á undan er tilfangaþörfin fyrir aðalaðgerðina (30) vélin á meðan tilfangaþarfir fyrir aukaaðgerðir (30' og 30'') eru forritið og starfsmaðurinn. Fimmtíu prósenta álag hjálpar til við að tryggja að áætlaður starfsmaður getur haft umsjón með tveimur vélum í einu.

### <a name="approval-of-routes"></a>Samþykki á leiðum

Áður en hægt er að nota leið í áætlun eða framleiðsluferli, verður hún að vera samþykkt. Samþykki gefur til kynna leiðahönnun hefur verið lokið. Sama losuð afurð eða útgefin afurðarafbrigði geta haft margar samþykktar leiðir. Venjulega er samþykkt leiðar gerð þegar fyrsta viðeigandi leiðaútgáfa er samþykkt. Hins vegar í sumum viðskiptaaðstæðum, eru samþykkt leiðarinnar og leiðarútgáfunnar aðskildir verkþættir sem snert gætu mismunandi eigendur ferla.  

Hver leið getur verið sérstaklega samþykkt eða ósamþykkt. Athugið hins vegar að þegar leið er ósamþykkt, eru allar tengdar leiðarútgáfur einnig ósamþykktar. Í færibreytum Framleiðslustýringar er hægt að tilgreina hvort hæg t sé að hætta við samþykkt leiða og hvort hægt sé að breyta samþykktum leiðum.  

Ef þú verður að halda kladda sem skráir hver samþykkir hverja leið er hægt að krefjast rafrænna undirskrifta fyrir samþykki á leiðinni. Notendur þurfa þá að staðfesta auðkenni þeirra með því að nota [rafrænar undirskriftir](../../fin-and-ops/organization-administration/electronic-signature-overview.md).

## <a name="operations"></a>Operations
Aðgerðirnar eru þrep í framleiðsluferlinu. Hver aðgerð hefur kenni og einfalda lýsingu. Eftirfarandi töflur sýna góð dæmi um aðgerðir úr vél verslunar.

| Aðgerð  | lýsing        |
|------------|--------------------|
| PipeCut    | Klippa       |
| TIGweld    | TIG suða        |
| JigAssy    | Jig-samsetning       |
| Eftirlit | Gæðaeftirlit |

Aðgerðareiginleikar aðgerðar, eins og uppsetningartími og keyrslutími, tilfangaþörf, kostnaðarútreikningar og notkunarútreikningar, eru tilgreindir í aðgerðarvenslum. (Frekari upplýsingar um aðgerðavensl eru í næsta hluta.)

## <a name="operation-relations"></a>Aðgerðavensl
Eftirfarandi eiginleikum rekstraráætlanagerðar aðgerðar er haldið við í aðgerðavenslum:

- Kostnaðartegundir
- Notkunarfæribreytur
- Vinnslutímar
- Magn í vinnslu
- Tilfangaþörf
- Athugasemdir og leiðbeiningar

Hægt er að skilgreina mörg aðgerðavensl fyrir sömu aðgerð. Hins vegar eru hver aðgerðavensl sértæk við eina aðgerð og geyma eiginleika sem tengjast leið, losuðum afurðum eða safni útgefinna afurða sem eru tengdar við flokk vöru. Þess vegna er hægt að nota sömu aðgerð í mörgum leiðum sem hafa mismunandi aðgerðareiginleika. Þar að auki er auðveldlega hægt að viðhalda aðalgögnum ef notaðar eru staðlaðar aðgerðir sem hafa sömu aðgerðareiginleika, óháð leið sem er notuð og vöru sem er framleidd. Svið aðgerðavensla er skilgreint í gegnum eiginleikana **Vörukóði**, **Vöruvensl**, **Leið kóða** og **Leið vensl** eins og sýnt er í eftirfarandi töflu.

| Vörukóði | Vöruvensl         | Leiðarkóði | Leiðarvensl   | Umfang aðgerðavensla                                                                                                                                                                                                                                                                              |
|-----------|-----------------------|------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Tafla     | &lt;Vörukenni&gt;       | Leið      | &lt;Auðkenni leiðar&gt; | Aðgerðaeiginleikar aðgerðar þegar hún er notuð í leiðinni þar sem **Leiðarnúmer**=&lt;leiðarkenni&gt; til að framleiða útgefin afurð þar sem **Vörunúmer**=&lt;vörukenni&gt;.                                                                                                                        |
| Tafla     | &lt;Vörukenni&gt;       | Allir lyklar        |                  | Sjálfgefnir aðgerðareiginleikar aðgerðar þegar hún er notuð til að framleiða útgefna afurð þar sem **Vörunúmer**=&lt;vörukenni&gt;. Með öðrum orðum eiga þessir eiginleikar rekstraráætlanagerðar við þegar engin leiðarsértæk tengsl eru til fyrir losaða afurð.                                     |
| Hópur     | &lt;Kenni vöruflokka&gt; | Leið      | &lt;Auðkenni leiðar&gt; | Aðgerðareiginleikar aðgerðar þegar hún er notuð í leiðinni þar sem **Leiðarnúmer**=&lt;leiðarkenni&gt; til að framleiða útgefnar afurðir sem tengjast vöruflokkum &lt;vörukenni flokk&gt;, nema það sé tiltekin leið aðgerðavensl fyrir losaða afurð.                         |
| Hópur     | &lt;Kenni vöruflokka&gt; | Allir lyklar        |                  | Sjálfgefnir aðgerðareigileikar aðgerðar þegar hún er notuð til að framleiða útgefnu afurðanna sem tengjast vöruflokkum &lt;vörukenni flokkur&gt;, nema nákvæmari aðgerðavensl séu til.                                                                                                  |
| Allir lyklar       |                       | Leið      | &lt;Auðkenni leiðar&gt; | Sjálfgefnir aðgerðaeiginleikar aðgerðar þegar hún er notuð í leiðinni þar sem **Leiðarnúmer**=&lt;leiðarkenni&gt;. Með öðrum orðum eiga þessir aðgerðareiginleikar við þegar engin aðgerðartengsl eiga sérstaklega við um annaðhvort útgefna afurð eða tengdan vöruflokk. |
| Allir lyklar       |                       | Allir lyklar        |                  | Sjálfgefnir aðgerðareiginleikar aðgerðar. Þessir aðgerðareiginleikar gilda þegar nákvæmari aðgerðavensl eru ekki til.                                                                                                                                                                |

Einnig er hægt að tilgreina að aðgerðavensl séu bundin við svæði. Á þennan hátt geta aðgerðaeiginleikar aðgerðar verið mismunandi, eftir staðsetningu (það er að segja, svæðinu) þar sem aðgerðin er framkvæmd. Fyrir skilgreindar vörur má einnig að tilgreina mismunandi aðgerðareiginleika fyrir hverja afurðargrunnstillingu.  

Aðgerðavensl veita mikinn sveigjanleika þegar skilgreina skal leiðir. Þar að auki hjálpar getan að skilgreina sjálfgefna eiginleika til við að draga úr fjölda aðalgagna sem þarf að vinna með. Hins vegar þýðir þessi sveigjanleika líka að það verður að hafa í huga samhengið sem aðgerðavenslum er breytt innan.  

> [!NOTE]
> Þar sem aðgerðaeiginleikar eru geymdir í aðgerðavenslum fyrir hverja aðgerð á hverri leið, hafa öll tilvik af sömu aðgerð (t.d. Samsetningu) sama uppsetningartíma, keyrslutíma og tilfangaþarfir. Þess vegna ef tvö tilvik aðgerðar verða að koma á sömu leið en hafa mismunandi keyrslutíma þarf að stofna tvær aðskildar aðgerðir, eins og Assembly1 og Assembly2.

### <a name="modifying-product-specific-routes"></a>Breyti afurðabundnum leiðum

Þegar þú opnar síðuna **Leið** á síðunni **Losuð afurðarupplýsingar** eru leiðarútgáfur sem eru tengdar við valda afurð losuð sýndar. Í þessu samhengi sýnir Supply Chain Management aðgerðaeiginleika fyrir hverja aðgerð úr aðgerðavenslum sem samsvara bestu leiðarútgáfunni. Þú munt taka eftir að listinn yfir aðgerðir inniheldur eiginleikana **Vörukóði** og **Leið kóða** úr aðgerðavenslunum. Þess vegna er hægt að ákvarða hvaða aðgerðavensl er sýnd.  

Á síðunni **Leið** er hægt að breyta aðgerðareiginleikum aðgerðar, eins og keyrslutíma eða kostnaðartegundum. Breytingarnar eru vistaðar í aðgerðavensl sem eiga sérstaklega við um leiðina og útgefna afurð sem vísað er í gildandi leiðarútgáfu. Ef aðgerðavensl sem eru sýnd eiga ekki sérstaklega við um leiðina og útgefna afurð áður en breytingar eru vistaðar, býr kerfið til afrit af aðgerðavenslunum. Þetta afrit *er* sértækt fyrir leiðina og útgefna afurð. Þess vegna hafa breytingarnar ekki áhrif á aðrar leiðir eða útgefnar afurðir. Til að staðfesta hvaða aðgerðavenslum er breytt á síðunni **Leið** síðunni, skal skoða svæðin **Vörukóði** og **Leiðarkóða**.  

Einnig er hægt að stofna handvirkt aðgerð sem á sérstaklega við um leið og útgefna afurð með því að nota aðgerðina **Afrita og breyta venslum**.  

> [!NOTE]
> Ef bætt er við nýrri aðgerð í leið á síðunni **Leið** eru aðgerðavensl aðeins stofnuð fyrir gildandi útgefna afurð. Þess vegna ef leið er einnig notuð til að útbúa aðrar útgefnar afurðir, munu engin aðgerðatengsl verða til fyrir þær útgefnar afurðir og ekki verður lengur hægt að nota leið fyrir þessar útgefnu afurðir.

### <a name="maintaining-operation-relations-per-route"></a>Vinna með aðgerðavensl á hverja leið

Þegar þú opnar síðuna **Leiðarupplýsingar** á listasíðunni **Leiðir** birtist listi yfir öll aðgerðavensl sem eiga við valda leið. Þess vegna er auðveldlega hægt að staðfesta hvaða aðgerðareiginleikar eru notaðir fyrir hvaða afurðir. Hægt er að breyta sjálfgefnum eiginleikagildum og afurðabundnum eiginleikagildum.  

Ef nýjum aðgerðavenslum er bætt við á síðunni **Leiðarupplýsingar** er **Leið kóða** sjálfkrafa stillt á **Leið**, og svæðið **Leiðarvensl** er stillt á leiðarnúmer gildandi leiðar.

### <a name="maintaining-operation-relations-per-operation"></a>Vinna með aðgerðavensl á hverja aðgerð

Af síðunni **Aðgerðir** er hægt að opna síðuna **aðgerðavensl**. Á þessari síðu er hægt að breyta öllum aðgerðavenslum fyrir tilgreindu aðgerðina. Hægt er að breyta jafnvel aðgerðavenslum sem innihalda sjálfgefin gildi.  

Ef fyrirtækið notar staðlaðar aðgerðir og ef rekstrarfæribreytur eru þær sömu fyrir allar afurðir og ferli, gefur síðan **Aðgerðavensl** þægilega leið til að viðhalda sjálfgefnum aðgerðareiginleikum þeirra aðgerða.

### <a name="applying-operation-relations"></a>Beiting aðgerðavensla

Í sumum tilfellum verður Supply Chain Management að finna aðgerðareiginleika fyrir aðgerð. Til dæmis þegar innkaupapöntun er stofnuð verður að afrita aðgerðareiginleika hverrar aðgerðar úr aðgerðavenslum yfir í framleiðsluleiðina. Í þessum kringumstæðum leitar Supply Chain Management að viðeigandi aðgerðavenslum frá sértækustu samsetningunni að minnst sértæku samsetningunni.  

Þegar Supply Chain Management leitar að mest viðeigandi aðgerðavenslum fyrir losaða afurð eru aðgerðavensl sem samsvara vörukenni útgefinnar afurðar tekin fram fyrir aðgerðavensl sem samsvara vöruflokkskenni. Á móti eru aðgerðavensl sem samsvarar Flokkskenni vöru æskilegri en sjálfgefin aðgerðavensl. Leitin er gerð í eftirfarandi röð:

1.  **Vörukóði**=**Tafla** og **Vöruvensl**=&lt;vörukenni&gt;
2.  **Vörukóði**=**Hópur** og **Vöruvensl**=&lt;vörukenni&gt;
3.  **Vörukóði**=**Allt**
4.  **Leiðakóði**=**Leið** og **Leið tengsl**=&lt;leið kenni&gt;
5.  **Leiðarkóði**=**Allt**
6.  **Skilgreining**=&lt;Skilgreiningarkenni&gt;
7.  **Skilgreining**=
8.  **Svæði**=&lt;Svæðiskenni&gt;
9.  **Svæði**=

Þess vegna á aðeins að nota aðgerð einu sinni fyrir hverja leið. Ef aðgerðin kemur margsinnis fyrir í sömu leið munu öll tilvik þeirrar aðgerðar hafa sömu aðgerðavensl og ekki er hægt að hafa aðra eiginleika (til dæmis keyrslutíma) fyrir hvert tilvik.

## <a name="route-versions"></a>Leiðarútgáfur

Útgáfur leiða eru notaðar til að hýsa tilbrigði í framleiðslu á afurðum eða veita meiri stjórn yfir framleiðsluferlinu. Þær skilgreina þá leið sem á að nota þegar tiltekin útgefin afurð eða losuð afurðarafbrigði er framleidd. Hægt er að nota eftirfarandi skorður til að skilgreina hvaða leið er notuð fyrir losaða afurð:

- Vöruvíddir (stærð, litur, stíll eða skilgreining)
- Framleiðslumagn
- Framleiðslusvæði
- Framleiðsludagsetning

Þegar verið er að framleiða vöru á ákveðnu svæði í ákveðnu magni eða á tilteknu tímabili, er hægt að úthluta ákveðinni leiðarútgáfu viðkomandi útgáfu sem sjálfgefinni leiðarútgáfu. Athugið hins vegar að aðeins ein virk leið er leyfð fyrir tiltekna útgefna afurð og tiltekið safn skorður.  

Í færibreytum Framleiðslustýringar er hægt að krefjast að gildistími leiðarútgáfu verði alltaf að vera tilgreintdur

### <a name="approval-of-route-versions"></a>Samþykkt á leiðarútgáfum

Áður en hægt er að nota leiðarútgáfu í áætlun eða framleiðsluferli verður að samþykkja hana. Þegar leiðaútgáfa samþykkt er einnig hægt að samþykkja tengda leið. Athugið að hægt er að samþykkja leiðarútgáfu eingöngu ef tengd leið er einnig samþykkt.

### <a name="activating-the-default-route-version"></a>Virkja sjálfgefna leiðarútgáfu

Þegar leiðaútgáfa er virkjuð er hún tilgreind sem sjálfgefin leiðarútgáfa sem aðaláætlanagerð notar eða sem verður notuð til að stofna framleiðslupantanir. Hægt er að hafa aðeins eina virka leiðarútgáfu fyrir tiltekið safn skorður (til dæmis, tímabil, svæði eða magn). Ef útgáfan sem verið er að reyna að virkja rekst á við útgáfu sem er þegar virk berast villuskilaboð. Það verður annaðhvort að afvirkja útgáfu sem rekst á eða breyta skorðum útgáfu (yfirleitt tímabils) til að koma í veg fyrir tvíræða virkjun.

### <a name="electronic-signatures"></a>Rafrænar undirskriftir

Ef þú verður að halda kladda sem skráir hver samþykkir og virkjar hverja leiðaútgáfu er hægt að krefjast rafrænna undirskrifta fyrir þessi verkefni. Notendur sem samþykkja og virkja leiðarútgáfur verða síðan að staðfesta auðkenni þeirra með því að nota [rafræna undirskrift](../../fin-and-ops/organization-administration/electronic-signature-overview.md).

### <a name="product-change-that-uses-case-management"></a>Vörubreyting sem notar málastjórnun

Afurðarbreytingamál fyrir samþykkt og virkjun nýrra eða breyttra leiða og leiðarútgáfa veitir auðvelda leið til að sjá yfirlit yfir skorður leiðarútgáfu. Einnig er hægt að samþykkja og virkja allar leiðir sem tengjast ákveðinni breytingu í einni aðgerð og skjalfesta niðurstöður í breytingarmáli afurðar.

## <a name="maintaining-routes"></a>Viðhalda leiðum

Eftir viðskiptaþörfum ykkar, gæti verið hægt að minnka það framlag sem er krafist til að viðhalda skilgreiningum á vinnslu.

### <a name="making-routes-independent-of-resources"></a>Gera leiðir óháðar tilföngum

Í mörgum kerfum verður að tilgreina aðgerðatilföng eða tilfangaflokk sem á að framkvæma aðgerð í leiðinni. Hins vegar er í Supply Chain Management hægt að skilgreina safn krafna sem rekstrartilföng verða að uppfylla til að vera viðeigandi fyrir aðgerðina. Þess vegna þarf ekki að ákvarða tiltekin rekstrartilföng eða tilfangaflokk sem á að nota fyrr en aðgerðinni er í raðað raun. Þessi virkni er sérlega gagnleg þegar þú ert með marga starfsmenn eða vélar sem geta unnið sömu aðgerð.  

Til dæmis tilgreinir þú að aðgerð krefst aðgerða af gerðinni **Vélar** sem hefur **Stimplunar** getu upp á 20 tonn. Röðunarvélin mun síðan leysa þessar þarfir til tiltekinna aðgerðatilfanga eða tilfangaflokks þegar aðgerðin er áætluð. Þar sem hægt er að tilgreina einungis þessar þarfir í stað þess að binda aðgerð við tiltekna vél, hefurðu miklu meiri sveigjanleika. Þar að auki, verður viðhald auðveldara þegar tilföng eru flutt eða nýjum tilföngum er bætt við.  

Nánari upplýsingar um mismunandi gerðir af tilfangaþörfum og hvernig á að nota þær er að finna í tilfangaþarfir Aðgerða og [tilfangagetu](resource-capabilities.md).

### <a name="sharing-routes-across-sites"></a>Samnýting leiða á milli svæða

Ef framleiða á sömu afurð á fleiri en einu svæði framleiðslu og ef skrefin fyrir framleiðslu á vöru eru þau sömu í öllum svæðum er oft hægt að hanna samnýtta leið sem notuð er á milli allra framleiðslusvæða. Til að stofna samnýtta leið skal ekki tilgreina svæði á leiðinni sjálfri. Hins vegar þarf samt að stofna leiðarútgáfu sem tengir samnýtta leið við afurð á hverju svæði.  

Einnig verður að tryggja að tilfangaþarfir fyrir hverja aðgerð í leiðinni kalli ekki eftir sértækum rekstrartilföngum eða tilfangaflokkum, en séu þess í stað tilgreind hvað varðar einkenni áskilinna tilfanga. Röðunarvélin mun síðan geta úthlutað viðeigandi rekstrartilföngum úr því svæði sem framleiðslu er raðað á. Til dæmis ef það er örlítill mismunur í keyrslutíma eða ef uppsetningartími fyrir tiltekna aðgerð er svæðisbundinn er hægt að tilgreina þessar upplýsingar með því að bæta við fleiri aðgerðavenslum fyrir það svæði.  

Til að nýta fríðindi samnýttra leiða til fulls ætti einnig nota tilfanganotkun á samsvarandi uppskrift (BOM). Þegar þú stillir flaggið fyrir tilfanganotkun í uppskriftarlínunni, er vöruhús og staðsetning sem á að nota hráefni frá afleitt úr rekstrartilföngum sem aðgerðinni er raðað á. Þess vegna þarf ekki að ákvarða vöruhús og staðsetningu fyrr en framleiðslan er í rauninni áætluð. Á þennan hátt er hægt að gera bæði Uppskrift og leið óháðar efnislegri staðsetningu þar sem varan er framleidd.

### <a name="standard-operation-relations"></a>Stöðluð aðgerðavensl

Ef fyrirtækið notar staðlaðar aðgerðir í gegnum framleiðslu og ef það er lítill sem enginn breytileiki á uppsetningartíma, keyrslutíma, notkunarútreikningi, kostnaðarútreikningi og svo framvegis, gæti borgað sig að stofna sjálfgefin aðgerðavensl fyrir allar aðgerðir. Í þessu tilfelli skal forðast að stofna aðgerðavensl sem eiga við allar leiðir eða losaðar afurðir.  

Ef þú tilgreinir einnig tilfangaþarfir hvað varðar hæfni og getu og gerir notandaleiðirnar óháðar svæði, er hægt að hjálpa til við að halda áframhaldandi viðhaldi viðskiptaferlanna í lágmarki.  

Þegar þessi aðferð er notuð verður síðan **Aðgerðavensl** aðaláfangastaður fyrir viðhald keyrslutíma og annarra eiginleika.

### <a name="resource-specific-process-times"></a>Tilfangatilgreindir keyrslutímar

Ef þú tilgreininr ekki rekstrartilfang eða tilfangaflokkur sem hluta af tilfangaþörfum fyrir aðgerð, gætu viðeigandi tilföng unnið á mismunandi kerfishraða. Þess vegna er tíminn sem þarf til að vinna úr aðgerð mismunandi. Til að leysa þetta vandamál er hægt að nota svæðið **Formúlu** í aðgerðavenslum til að tilgreina hvernig vinnslutími er reiknaður. Eftirtaldir valkostir eru í boði:

- **Stöðluð** – (Sjálfgefinn valkostur) útreikningurinn notar aðeins svæði úr aðgerðavenslum og margfaldar tilgreinda keyrslutíma með pöntunarmagni.
- **Afkastageta** – útreikningurinn inniheldur svæðið **Afkastagetu** úr rekstrartilföngum. Þess vegna er tíminn tilfanga-háður. Gildið sem tilgreint er á aðgerðum tilfanga er afkastageta á klukkustund. **Vinnslutíminn** er reiknaður sem **Pöntunarmagn** deilt með **Afkastageta**.
- **Runa** – afkastagetu í runu er reiknað með því að nota upplýsingar úr aðgerðavenslum. Fjöldi runa og vinnslutími má síðan reikna út frá pöntunarmagninu.
- **Tilfangaruna** – Þessi valkostur er nokkurn veginn eins og í **Runu** valkost. Hins vegar inniheldur útreikningurinn svæðið **Afkastagetu** úr rekstrartilföngum. Þess vegna er tíminn háður tilföngum.

### <a name="set-up-route-groups"></a>Setja upp leiðarflokka

Hægt er að skilgreina leiðaflokkinn og uppsetningu leiðarinnar eða vinnslugerðar undir **Framleiðslustýring > Uppsetning > Leið > Leiðaflokkar**. Fyrir hverja gerð leiðar/vinnslu í leiðaflokknum er hægt að velja eða hreinsa eftirfarandi valkosti:

- **Virkjun** - Veljið þennan valkost til að virkja útreikninga og áætlanagerð fyrir valda vinnslugerð, og til að fá endurgjöf um vinnslu þegar þú keyrir vinnsluröðun. Þú þarft að velja þennan möguleika til að virkja vinnslugerðina og síðan velja afganginn af valkostunum fyrir þessa vinnslugerð. Ef virkjunin er ekki valin mun þessi vinnslugerð ekki vera virkjuð, óháð valinu á öðrum valkostum. 
- **Vinnslustýring** - Veldu þennan valkost til að hafa með vinnslugerðina í vinnslustýringu þegar þú keyrir vinnsluröðun. 
- **Vinnutími** Veljið þennan valkost til að raða vinnslugerð skv. vinnutímadagatalinu sem er skilgreint fyrir rekstrartilföng, annars er gregorískt dagatal nota. Vinnutími getur annað hvort verið áætlaður með gregorísku tímatali eða með skilgreindu verkdagatali. Ef valið er þessi valkostur, mun röðun byggjast á skilgreindum vinnutíma. Enn fremur, mun vinnsla af umræddri vinnslugerð vera röðuð frá miðnætti á tilgreindri dagsetningu sem upphafsdagsetning vinnslunnar.
- **Afkastageta** - Veljið þennan valkost til að taka frá afkastagetu fyrir vinnslugerðina þegar þú keyrir vinnsluröðun. Ef þetta er valið, afkastagetu frátekin röðun er keyrð fyrir valin vinnslugerð. Þetta gefur yfirlit sem vinnslugerðir í hverjum flokki leið er notuð í rekstrartilföngum. Til dæmis, í þeim tilvikum þar sem þurrkunartilföng eru flöskuhálstilföng, verða þessi tilföng að vera tilgreind sem flöskuhálsar. Þurrkunar aðgerðir sem er úthlutað á biðröð vinnslugerðir tíma þurfa þurrkunar tilföng. 

Fyrir hverja vinnslugerð þarf fyrst að gera hana virka eða óvirka. Þegar slökkt er á verða engar hinna uppsetninganna (vinnslustýring, vinnutími og afkastageta) teknar til greina, þar sem vinnslugerðin verður ekki virk. 

Meðal vinnslugerðanna er hægt að finna skörun. Skörun gerir mismunandi vinnslum kleift að vera framkvæmdar á sama tímanum. Þegar vinnslur skarast er hægt að nota tilföngin en ekki er hægt að taka þau frá fyrir tilteknar vinnslur.
Þess vegna, þegar virkjun er valin fyrir skörun, hafa aðrar stillingar (vinnslustýring, vinnutími og afkastageta) engin áhrif á leiðaflokkinn. 

> [!NOTE]
> Þegar útgáfur eru uppfærðar gætu eftirfarandi villur komið upp á: **„CRL villa kom upp þegar röðunarvél var sótt“**. Ef þessi villa kemur upp skal fara á síðuna **Leiðaflokkar** og fyrir allar leiðir þar sem þú hefur virkjar **Skörun** skal hreina valkostina **Vinnslustjórnun**, **Vinnutími** og **Afkastageta**. 

## <a name="additional-resources"></a>Frekari upplýsingar

- [Uppskriftir og formúlur](bill-of-material-bom.md)

- [Kostnaðartegundir notaðar í framleiðslubeiningu](../cost-management/cost-categories-used-production-routings.md)

- [Tilfangageta](resource-capabilities.md)

- [Yfirlit yfir rafræna undirskrift](../../fin-and-ops/organization-administration/electronic-signature-overview.md)



