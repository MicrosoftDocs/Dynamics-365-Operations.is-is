---
title: Vegið meðaltal dagsetningar
description: Dagsetning vegins meðaltals er birgðalíkan byggt á reglunni um vegið meðaltal þar sem innhreyfingar úr birgðum eru metnar á meðaltalsgildi vara sem tekið er á móti í birgðum fyrir hvern einstakan dag á birgðalokunartímabilinu.
author: AndersGirke
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventMarking, InventModelGroup, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28991
ms.assetid: 945d5088-a99d-4e54-bc42-d2bd61c61e22
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9990df3e57d65c77a75913efaf30675528d411b4
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 07/06/2021
ms.locfileid: "6343701"
---
# <a name="weighted-average-date"></a>Vegið meðaltal dagsetningar

[!include [banner](../includes/banner.md)]

Dagsetning vegins meðaltals er birgðalíkan sem byggist á reglunni um vegið meðaltal. Fyrir regluna um vegið meðaltal eru atriði úr birgðalíkani metin á meðaltalsvirði hlutanna sem tekið er á móti í birgðum fyrir hvern einstakan dag á birgðalokunartímabilinu. 

Þegar birgðalokun með dagsetningu vegins meðaltals er keyrð, eru allar daglegar úthreyfingar jafnaðar gagnvart sýndarúthreyfingu. Þessi sýndarúthreyfing geymir heildar móttekið magn og virði fyrir þann dag. Sýndarinnhreyfingin hefur samsvarandi sýndarúthreyfingu sem innhreyfingar verða jafnaðar við. Þannig fá allar úthreyfingar sama meðaltalskostnað. Sýndarúthreyfingu og -innhreyfingu er hægt að sjá sem sýndarflutning sem kallast *birgðalokunarfærsla með vegnu meðaltali*. 

Ef einungis ein úthreyfing hefur orðið á eða fyrir dagsetninguna, þarf ekki að meta meðaltal. Þar sem allar innhreyfingar eru jafnaðar út frá þeirri úthreyfingu þarf ekki að stofna sýndarflutning. Ef einungis innhreyfingar verða á dagsetningunni, eru að sama skapi engar úthreyfingar til að meta meðaltal út frá og þá verður sýndarflutningur ekki heldur stofnaður í því tilfelli. Þegar vegið meðaltal er notað geturðu valið að merkja birgðafærslur svo að tiltekin innhreyfing vöru sé jöfnuð gagnvart tiltekinni úthreyfingu í stað þess að nota regluna um vegið meðaltal. Í þessu tilfelli er ekki notuð reglan um dagsetningu vegins meðaltals. Mælt er með mánaðarlegri birgðalokun þegar birgðalíkanið dagsetning vegins meðaltals er notað. 

Eftirfarandi formúla er notuð til að reikna út kostnaðaraðferð vegins meðaltals dagsetningar: 

Vegið meðaltal = (\[Q1 × P1\] + \[Q2 × P2\] + \[Q *n* × P *n*\]) ÷ (Q1 + Q2 + Q *n*) 

Við birgðalokun er útreikningur framkvæmdur á hverjum degi í lokunartímabilinu, eins og sýnt er í eftirfarandi dæmi. 

![Daglegt útreikningalíkan dagsetningar vegins meðaltals.](./media/weightedaveragedatedailycalculationmodel.gif) 

Birgðafærslur sem fara úr birgðum, þar á meðal sölupantanir, birgðabækur og framleiðslupantanir, munu eiga sér stað á áætluðu kostnaðarverði á dagsetningu bókunarinnar. Þetta áætlaða kostnaðarverð kallast einnig meðalkostnaðarverð. Á degi birgðalokunar greinir kerfið birgðafærslur fyrir fyrri tímabil, fyrri daga og núverandi dag. Greiningin er notuð til að ákvarða hvaða eftirfarandi lokunaraðferð eigi að nota:

-   Bein jöfnun
-   Samantektarjöfnun

Jafnanir eru birgðalokunarbókanir sem leiðrétta úthreyfingar í rétt vegin meðaltöl frá og með lokadagsetningunni. 

**Ábending:** Fyrir frekari upplýsingar um jafnanir, sjá grein um birgðalokun. Eftirfarandi dæmi skýra áhrif þess að nota vegið meðaltal með fimm ólíkum skilgreiningum:

-   Bein jöfnun vegins meðaltals dagsetningar án valkostarins **Taka efnislegt virði með**
-   Samantektarjöfnun vegins meðaltals dagsetningar án valkostarins **Taka efnislegt virði með**
-   Bein jöfnun vegins meðaltals dagsetningar með valkostinum **Taka efnislegt virði með**
-   Samantektarjöfnun vegins meðaltals dagsetningar með valkostinum **Taka efnislegt virði með**
-   Vegið meðaltal dagsetningar með merkingu

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-isnt-used"></a>Bein jöfnun vegins meðaltals dagsetningar án valkostarins Taka efnislegt virði með
Núverandi útgáfa nota sömu reglu um beina jöfnun og var notuð fyrir vegið meðaltal í fyrri útgáfum. Kerfið mun jafna beint á milli innhreyfinga og úthreyfinga. Kerfið notar þessa reglu beinnar jöfnunar í tilteknum aðstæðum:

-   Ein innhreyfing og ein eða margar úthreyfingar hafa verið bókaðar á þessu tímabili
-   Einungis úthreyfingar hafa verið bókaðar á tímabilinu og birgðir innihalda vörur á lager frá fyrri lokun.

Í aðstæðunum fyrir neðan hafa fjárhagslega uppfærðar innhreyfingar og úthreyfingar verið bókaðar. Á meðan á birgðalokun stendur mun kerfið gera upp innhreyfingu beint á móti úthreyfingu og ekki er nauðsynlegt að leiðrétta kostnaðarverð við úthreyfingu. 

Eftirfarandi skýringarmynd sýnir þessar færslur:

-   1a. Efnisleg innhreyfing birgða uppfærð fyrir magnið 5 með kostnaðinn 10,00 USD hver
-   1b. Fjárhagsleg innhreyfing birgða uppfærð fyrir magnið 5 á kostnaðinum 10,00 USD hver.
-   2a. Efnisleg úthreyfing birgða uppfærð fyrir magnið 2 með kostnaðinn 10,00 USD hver
-   2b. Fjárhagsleg úthreyfing birgða uppfærð fyrir magnið 2 með kostnaðinn USD 10,00 hver.
-   3. Birgðalokun var framkvæmd með því að nota beina jöfnun til að jafna fjárhagslega innhreyfingu birgða í fjárhagslega úthreyfingu birgða.

![Bein jöfnun vegins meðaltals dagsetningar án valkostarins Taka efnislegt virði með.](./media/weightedaveragedatedirectsettlementwithoutincludephysicalvalue.gif) 

**Lykill að skýringarmynd:**

-   Birgðafærslur eru táknaðar með lóðréttum örvum.
-   Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
-   Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
-   Verðgildi birgðafærslunnar er tilgreint fyrir ofan (eða neðan) hverja lóðrétta línu í skjámyndinni *Magn*@*Einingarverð*.
-   Birgðafærslugildi innan sviga bendir til þess að birgðafærslan sé efnislega bókuð í birgðir.
-   Birgðafærslugildi án sviga bendir til þess að birgðafærslan sé fjárhagslega bókuð í birgðir.
-   Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
-   Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur bókunarröð birgðafærslna á tímaásnum til kynna.
-   Birgðalokun eru sýndar með rauðri lóðréttri punktaðri línu og merkinu *birgðalokun*
-   Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-isnt-used"></a>Samantektarjöfnun vegins meðaltals dagsetningar án valkostarins Taka efnislegt virði með
Vegið meðaltal er byggt á þeirri reglu að allar innhreyfingar á lokunartímabili eru teknar saman í nýja birgðaflutningsfærslu. Þessi færsla kallast *vegið meðaltal birgðalokunar*. Öll innhreyfing  dagsins verður gerð upp gegn úthreyfingu nýrra birgðaflutningsfærslna. Öll úthreyfing dagsins verður gerð upp gegn innhreyfingu nýrra birgðaflutningsfærslna. Ef birgðir á lager eru jákvæðar eftir birgðalokunina eru þær birgðir og virði birgðanna tekið saman í nýja birgðaflutningsfærslu (innhreyfing). Ef birgðir á lager eru neikvæðar eftir birgðalokunina eru birgðir á lager og virði birgðanna summa einstakra úthreyfinga sem hafa ekki verið jafnaðar að fullu. 

Í aðstæðunum fyrir neðan hafa nokkrar fjárhagslega uppfærðar innhreyfingar og úthreyfingar verið bókaðar yfir tímabilið. Við birgðalokun metur kerfið hvern dag til að ákvarða hvað eigi að gera á hverjum þeirra við lokun. 

Eftirfarandi skýringarmynd sýnir þessar færslur: 

**Dagur 1:**

-   1a. Efnisleg innhreyfing uppfærð með magninu 3 á 15,00 USD hver
-   1b. Fjárhagsleg innhreyfing uppfærð með magninu 3 á 15,00 USD hver
-   2a. Efnisleg úthreyfing birgða í magninu 1 með meðalkostnaðinum 15,00 USD.
-   2b. Fjárhagsleg úthreyfing birgða í magninu 1 með meðalkostnaðinum 15,00 USD.

Kerfið notar beina jöfnun fyrir dag 1. 

**Dagur 2:**

-   3a. Efnisleg úthreyfing birgða í magninu 1 með meðalkostnaðinum 15,00 USD.
-   3b. Fjárhagsleg úthreyfing birgða í magninu 1 með meðalkostnaðinum 15,00 USD.

Kerfið notar beina jöfnun fyrir dag 2. 

**Dagur 3:**

-   4a. Efnisleg úthreyfing birgða í magninu 1 með meðalkostnaðinum 15,00 USD.
-   4b. Fjárhagsleg úthreyfing birgða í magninu 1 með meðalkostnaðinum 15,00 USD.
-   5a. Efnisleg innhreyfing í magninu 1 á 17,00 USD hver
-   5b. Fjárhagsleg innhreyfing í magninu 1 á 17,00 USD hver

Birgðalokun er framkvæmd. Nota þarf beina jöfnun þar sem margar innhreyfingar eru á mörgum dögum.

-   7a. Fjárhagsleg úthreyfing birgðalokunarfærslu með vegnu meðaltali er stofnuð með magninu 2 á 32,00 USD til að draga saman allar jafnanir fjárhagslegra innhreyfinga birgða sem hafa ekki verið lokaðar.
-   7b. Fjárhagsleg innhreyfing birgðalokunarfærslu vegins meðaltals er stofnuð sem mótvægi við 7a.

Kerfið myndar og bókar samanteknu birgðaflutningafærsluna. Einnig jafnar kerfið allar innhreyfingar fyrir daginn og birgðir á lager fyrir fyrri daga á móti samantekinni úthreyfingarfærslu birgðaflutningsins. Allar úthreyfingar dagsins eru jafnaðar á móti samanteknu innhreyfingarfærslu birgðaflutningsins. Vegið meðaltal kostnaðarverðsins reiknast sem 16,00 USD. Úthreyfingin hefur leiðréttingu upp á 1,00 USD til að leiðrétta veginn meðalkostnað. Nýja meðalkostnaðarverðið er 16,00 USD. 

Eftirfarandi skýringarmynd sýnir þessar raðir af færslum með áhrifunum af því að velja birgðalíkan vegins meðaltals og regluna um beina jöfnun án valkostarins **Taka efnislegt virði með**. 

![Samantektarjöfnun vegins meðaltals dagsetningar án valkostarins Taka efnislegt virði með.](./media/weightedaveragedatesummarizedsettlementwithoutincludephysicalvalue.gif) 

**Lykill að skýringarmynd**

-   Birgðafærslur eru táknaðar með lóðréttum örvum.
-   Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
-   Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
-   Verðgildi birgðafærslunnar er tilgreint fyrir ofan (eða neðan) hverja lóðrétta línu í skjámyndinni *Magn*@*Einingarverð*.
-   Birgðafærslugildi innan sviga bendir til þess að birgðafærslan sé efnislega bókuð í birgðir.
-   Birgðafærslugildi án sviga bendir til þess að birgðafærslan sé fjárhagslega bókuð í birgðir.
-   Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
-   Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur bókunarröð birgðafærslna á tímaásnum til kynna.
-   Birgðalokun eru sýndar með rauðri lóðréttri punktaðri línu og merkinu *birgðalokun*
-   Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.
-   Rauðar skáliggjandi örvar lýsa innhreyfingarfærslum sem verið er að jafna í úthreyfingarfærslu sem stofnuð er af kerfinu.
-   Græna skáliggjandi örin táknar mótfærslu kerfismyndaðrar innhreyfingarfærslu þar sem upprunalega bókaða úthreyfingafærslan er jöfnuð.

## <a name="weighted-average-date-direct-settlement-when-the-include-physical-value-option-is-used"></a>Bein jöfnun vegins meðaltals dagsetningar með valkostinum Taka efnislegt virði með
Reglan um beina jöfnun sem notuð er í þessari útgáfu er sú sama og notuð er fyrir vegið meðaltal í fyrri útgáfum. Kerfið mun jafna beint á milli innhreyfinga og úthreyfinga. Kerfið notar þessa reglu beinnar jöfnunar í tilteknum aðstæðum:

-   Ein innhreyfing og ein eða margar úthreyfingar hafa verið bókaðar á þessu tímabili
-   Aðeins úthreyfingar hafa verið bókaðar á tímabilinu og í birgðum eru birgðir á lager frá fyrri lokun.

Ef gátreiturinn **Efnislegt virði tekið með** er valinn fyrir vöru á síðunni **Vörulíkanaflokkur** notar kerfið efnislega uppfærðar innhreyfingar þegar það reiknar út áætlað kostnaðarverð eða meðaltal. Úthreyfingar eru bókaðar samkvæmt þessu áætlaða kostnaðarverði á tímabilinu. Við birgðalokun eru aðeins innhreyfingar sem hafa verið fjárhagslega uppfærðar teknar með í útreikning á vegnu meðaltali.

## <a name="weighted-average-date-summarized-settlement-when-the-include-physical-value-option-is-used"></a>Samantektarjöfnun vegins meðaltals dagsetningar án valkostarins Taka efnislegt virði með
Ef gátreiturinn **Efnislegt virði tekið með** er valinn fyrir vöru á síðunni **Vörulíkanaflokkur** notar kerfið efnislega uppfærðar innhreyfingar þegar það reiknar út áætlað kostnaðarverð eða meðaltal. Úthreyfingar eru bókaðar samkvæmt þessu áætlaða kostnaðarverði á tímabilinu. Við birgðalokun eru aðeins innhreyfingar sem hafa verið fjárhagslega uppfærðar teknar með í útreikning á vegnu meðaltali. Jöfnunarregla fyrir vegið meðaltal byggist á því að öll innhreyfing innan lokunartímabils er tekin saman í nýja birgðaflutningsfærslu sem kallast  *Birgðalokun með vegnu meðaltali*. Öll innhreyfing  dagsins verður gerð upp gegn úthreyfingu nýrra birgðaflutningsfærslna. Öll úthreyfing dagsins verður gerð upp gegn innhreyfingu nýrra birgðaflutningsfærslna. Ef birgðir á lager eru jákvæðar eftir birgðalokunina eru þær birgðir og virði birgðanna tekið saman í nýja birgðaflutningsfærslu (innhreyfing). Ef birgðir á lager eru neikvæðar eftir birgðalokunina eru birgðir á lager og virði birgðanna summa einstakra úthreyfinga sem hafa ekki verið jafnaðar að fullu.

## <a name="weighted-average-date-when-marking-is-used"></a>Vegið meðaltal dagsetningar með merkingu
Merking er aðferð sem gerir mögulegt að tengja úthreyfingarfærslu við innhreyfingarfærslu. Merking getur farið fram annað hvort áður eða eftir að færsla er bókuð. Hægt er að nota merkingu þegar ætlunin er að ganga úr skugga um nákvæman kostnað við birgðir þegar færsla er bókuð eða þegar birgðalokun er framkvæmd. 

Þjónustudeild fyrir viðskiptavini, hefur til dæmis fengið flýtipöntun frá mikilvægum viðskiptavini. Þar sem um flýtipöntun er að ræða þarf að greiða meira fyrir vöruna til þess að geta mætt beiðni viðskiptavinarins. Þá er nauðsynlegt að vera viss um að kostnaðurinn við þessa birgðavöru endurspeglist í framlegð, eða kostnaði seldra vara (COGS) á þessum sölupöntunarreikningi. Þegar innkaupapöntunin er bókuð, eru birgðir mótteknar með kostnaðinum 120,00 USD. þetta sölupöntunarskjal er merkt við innkaupapöntunina áður en fylgiseðillinn eða reikningurinn er bókaður. Kostnaður seldra vara mun þá vera 120,00 USD í staðinn fyrir núverandi meðaltal kostnaðar vörunnar. Ef að fylgiseðill sölupöntunarinnar eða reikningur er bókaður áður en merking á sér stað, mun kostnaður seldra vara verða bókaður á meðalkostnaðarverði. Áður en birgðalokun er framkvæmd er hægt að merkja þessar tvær færslur, hvora fyrir aðra. Þegar innhreyfingarfærsla er merkt við úthreyfingarfærslu er ekki tekið tillit til villuleitaraðferðarinnar sem var skilgreind í vörulíkanaflokknum. Í staðinn jafnar kerfið færslurnar hverja við aðra. 

Hægt er að merkja úthreyfingarfærslu við innhreyfingu áður en færsla er bókuð. Hægt er að gera þetta frá sölupöntunarlínu á síðunni **Ítarupplýsingar sölupöntunar**. Hægt er að skoða opnar innhreyfingarfærslur á síðunni **Merking**. Hægt er að merkja úthreyfingarfærslu við innhreyfingu eftir að færslan er bókuð. Hægt er að stemma eða merkja úthreyfingarfærslu fyrir opna innhreyfingarfærslu fyrir skráðan hlut úr bókaðri birgðaleiðréttingabók. Eftirfarandi skýringarmynd sýnir þessar færslur:

-   1a. Efnisleg innhreyfing birgða í magninu 1 á kostnaðarverðinu USD 10,00 hver.
-   1b. Fjárhagsleg innhreyfing birgða í magninu 1 á kostnaðarverðinu USD 10,00 hver.
-   2a. Efnisleg innhreyfing birgða í magninu 1 á kostnaðarverðinu USD 20,00 hver.
-   2b. Fjárhagsleg innhreyfing birgða í magninu 1 á kostnaðarverðinu USD 20,00 hver.
-   3a. Efnisleg innhreyfing birgða í magninu 1 á kostnaðarverðinu USD 25,00 hver.
-   4a. Efnisleg innhreyfing birgða í magninu 1 á kostnaðarverðinu USD 30,00 hver.
-   4b. Fjárhagsleg innhreyfing birgða í magninu 1 á kostnaðarverðinu USD 30,00 hver.
-   5a. Efnisleg úthreyfing birgða í magninu 1 á kostnaðarverðinu 21,25 USD (meðalverð fjárhagslega og efnislegra uppfærðra færslna).
-   5b. Fjárhagsleg úthreyfing birgða í magninu 1 er merkt við birgðainnhreyfingu 2b áður en færslan er bókuð. Þessi færsla er bókuð á kostnaðarverðinu 20,00 USD.
-   6a. Efnisleg úthreyfing birgða í magninu 1 á kostnaðarverðinu USD 21,25.
-   7. Birgðalokun er framkvæmd. Þar sem fjárhagslega uppfærða færslan er merkt við innhreyfingu sem er til, eru færslurnar jafnaðar hvor á aðra og engin leiðrétting gerð.

Nýtt meðaltal kostnaðarverðs endurspeglar meðaltal færslna sem hafa verið uppfærðar fjárhagslega og efnislega á 27,50 USD. Eftirfarandi skýringarmynd sýnir þessar raðir af færslum og áhrifum þess að merkja við birgðalíkan vegins meðaltals.

![Vegið meðaltal dagsetningar með merkingu.](./media/weightedaveragedatewithmarking.gif) 

**Lykill að skýringarmynd:**

-   Birgðafærslur eru táknaðar með lóðréttum örvum.
-   Innhreyfing í birgðir er táknuð með lóðréttum örvum fyrir ofan tímaásinn.
-   Úthreyfing úr birgðum er táknuð með lóðréttum örvum fyrir neðan tímaásinn.
-   Verðgildi birgðafærslunnar er tilgreint fyrir ofan (eða neðan) hverja lóðrétta línu í skjámyndinni *Magn*@*Einingarverð*.
-   Birgðafærslugildi innan sviga bendir til þess að birgðafærslan sé efnislega bókuð í birgðir.
-   Birgðafærslugildi án sviga bendir til þess að birgðafærslan sé fjárhagslega bókuð í birgðir.
-   Hver ný innhreyfingar eða úthreyfingarfærsla er merkt með nýju merki.
-   Hver lóðrétt ör er merkt með raðkenni t.d. *1a*. Kennið gefur bókunarröð birgðafærslna á tímaásnum til kynna.
-   Birgðalokun eru sýndar með rauðri lóðréttri punktaðri línu og merkinu *birgðalokun*
-   Jöfnun sem er gerð af birgðalokun er táknuð með brotinni rauðri línu sem liggur skáhallt frá innhreyfingu til úthreyfingar.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]