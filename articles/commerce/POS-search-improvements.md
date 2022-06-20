---
title: Leit að vöru og leit að viðskiptavinum í sölustað (POS)
description: Þessi grein veitir yfirlit yfir endurbætur sem gerðar hafa verið á vöru- og viðskiptavinaleitarvirkni í Dynamics 365 Commerce.
author: ShalabhjainMSFT
ms.date: 05/25/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: 141393
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: shajain
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: Retail April 2017 update
ms.openlocfilehash: 5f2d8162c810f63dc889a03d33fd111de69783de
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859001"
---
# <a name="product-search-and-customer-search-in-the-point-of-sale-pos"></a>Leit að vöru og leit að viðskiptavinum í sölustað (POS)

[!include [banner](includes/banner.md)]

Nútíma Point of Sale (MPOS) og Point of Sale (CPOS) í skýi bjóða upp á auðvelda leitaraðgerð á vörum og viðskiptavinum. Leitarstikan er alltaf til staðar efst í gluggum MPOS og CPOS, þannig að starfsmenn geti leitað að vörum og viðskiptavinum á fljótlegan hátt.

Starfsmenn geta leitað að vörum í vöruúrvali og vörulistum sem tengjast núverandi verslun. Þeir geta einnig leitað í vöruúrvali og vörubæklingum sem tengjast öðrum verslunum í fyrirtækinu. Þannig geta gjaldkerar selt og skilað vörum utan framboðs í vöruhúsi. Með svipuðum hætti geta starfsmenn leitað að viðskiptavinum sem tengjast núverandi verslun eða annarri verslun í fyrirtækinu. Auk þess geta starfsmenn leitað að viðskiptavinum sem tengjast öðru fyrirtæki í móðurfyrirtækinu.

## <a name="product-search"></a>Afurðaleit

Sjálfgefið er að vöruleitir séu gerðar á vöruúrvali verslunar. Þessi tegund leitar er þekktur sem *staðbundin vöruleit*. Hins vegar geta starfsmenn auðveldlega skipt yfir í hvaða verslun sem er í tengslum við núverandi verslun eða þeir geta leitað í annarri verslun. Þessi tegund leitar er þekktur sem *Fjartengd vöruleit*. Til að breyta vörulistanum velurðu hnappinn **Flokkar** til vinstri á síðunni. Efst í glugganum sem birtist skaltu velja hnappinn **Breyta vörulista** og velja síðan einn af tiltækum vörulistum til að skoða. Kerfið mun leita að vörum í valda vörulistanum.

Á síðunni **Breyta verslun** geta starfsmenn auðveldlega valið hvaða verslun sem er, eða þeir geta leitað að vörum í öllum verslunum.

![Vörulistanum breytt.](./media/Changecatalog.png "Vörulistanum breytt")

Staðbundin vöruleit leitar í eftirfarandi vörueiginleikum:

- Afurðarnúmer
- Afurðarnafn
- lýsing
- Víddir
- Strikamerki
- Leita að nafni

### <a name="additional-local-product-search-capabilities-conventional-sql-full-text-search"></a>Frekari leitareiginleikar staðbundinnar afurðar (hefðbundin SQL-leit með heildartexta) 

- Til að leita að mörg lykilorð í leit (það er fyrir leitir sem nota leitarorð) geta smásalar stillt hvort leitarniðurstöður innihaldi niðurstöður sem passa við *eitthvert* leitarorð eða aðeins niðurstöður sem passa við *öll* leitarorð. Stillingarnar fyrir þessa virkni er að finna í POS-virknisniðinu, undir nýjum hóp sem heitir **Afurðaleit**. Sjálfgefna stillingin er **Samsvara hvaða leitarorði sem er**. Þetta er einnig ráðlögðstilling. Þegar stillingin **Samsvara hvaða leitarorð sem er** er notuð, er öllum vörum sem passa að fullu eða hluta til við eitt eða fleiri leitarorð skilað sem niðurstöður. Þessar niðurstöður eru sjálfkrafa flokkaðar í hækkandi röð af vörum sem hafa mestu samsvörun við leitarorðin (að fullu eða að hluta).

    Stillingin **Samsvara hvaða leitarorði sem er** skilar aðeins vörum sem passa við öll leitarorð (að fullu eða hluta). Þessi stilling er gagnleg þegar vörunöfnin eru löng og starfsmenn vilja sjá aðeins takmarkaðar vörur í leitarniðurstöðum. Hins vegar er þessi leit með tveimur takmörkunum:

    - Leitin er gerð í einstökum vörueiginleikum. Til dæmis birtast aðeins vörur sem eru með öll leitarorð í að minnsta kosti einum eiginleika voru.
    - Ekki er leitað í víddum.
> [!NOTE]
> Eftirfarandi stillingar á **Samsvara hvaða leitarorði sem er**/**Samsvara öllum leitarorðum** í POS-virknireglum eiga aðeins við fyrir **staðbundnar** upplifanir afurðarleitar (hefðbundin SQL-leit með heildartexta). Þessi stilling hefur engin áhrif á skýjavæddar leitarupplifanir. Nýja leitarvélin er með eigið háþróað reiknirit sem knýr leitarsamsvörun fyrir leitarniðurstöður afurðar. 

- Smásöluaðilar geta skilgreint vöruleit til að sýna leitartillögur þegar notendur slá inn vöruheiti. Ný stilling fyrir þessa virkni er að finna í POS-virknisniðinu, undir hópi sem heitir **Vöruleit**. Stillingin heitir **Sýna leitaruppástungur meðan þú skrifa**. Þessi virkni getur hjálpað starfsmönnum að finna fljótt vöruna sem þeir leita að, vegna þess að þeir þurfa ekki að slá inn heitið handvirkt.
- Vöruleit reikniritin leitar nú einnig að leitarorðum í eiginleikanum **Leita í heiti** fyrir vöruna.

![Afurðatillögur.](./media/Productsuggestions.png "Afurðatillögur")

## <a name="customer-search"></a>Viðskiptavinaleit

Viðskiptavinaleit er notuð til að finna viðskiptavini í ýmsum tilgangi. Til dæmis gætu gjaldkerar viljað sjá óskalista viðskiptavina eða kaupferil eða bæta við viðskiptavininum við viðskipti. Reitnirit leitar parar saman leitarskilmála og þau gildi sem eru til staðar í eftirfarandi eiginleikum viðskiptavina:

- Nafn
- Netfang
- Símanúmer
- Vildarkortsnúmer
- Aðsetur
- Reikningsnúmer

Meðal þessara eiginleika gefur heitið mestan sveigjanleika fyrir leitir með mörgum leitarorðum, vegna þess að reikniritið skilar öllum viðskiptavinum sem passa við leitarniðurstöður. Viðskiptavinirnir sem samsvara flestum leitarorðum birtast efst í niðurstöðunum. Þessi aðferð hjálpar gjaldkerum í kringumstæðum þar sem þeir leita með því að slá inn fullt nafn, en eftirnafni og fornafni var víxlað við upphaflega gagnaskráningu. Hins vegar, til að skila betri afköstum, varðveita allir aðrir eiginleikar röð leitarorða. Ef röðin af leitarorðum passa ekki við pöntunina sem gögnin eru geymd í verður þess vegna engum niðurstöðum skilað.

Sjálfgefið er að leita viðskiptavina í aðsetursbókum viðskiptavina sem tengjast versluninni. Þessi tegund leitar er þekkt sem *Staðbundin viðskiptavinarleit* Einnig má leita að að viðskiptavinum altækt. Með öðrum orðum geta þeir leitað yfir verslanir félagsins og yfir alla aðra lögaðila. Þessi tegund leitar er þekktur sem *Fjartengd viðskiptavinarleit*

Til að leita altækt geta starfsmenn valið hnappinn **Sía niðurstöður** neðst á síðunni og síðan valið valkostinn **Leita í öllum verslunum**, eins og sýnt er á myndinni á eftir. Í þessu tilviki eru ekki aðeins viðskiptavinir sýndir. Allar tegundir aðila sem eru hluti af hverri aðsetursbók í höfuðstöðvum eru einnig sýndir. Þessir aðilar eru starfsmenn, seljendur, tengiliðir og samkeppnisaðilar.

> [!NOTE]
> Færa þarf inn minnst fjóra stafi til að leit að fjartengdum viðskiptavinum skili niðurstöðum.

Kenni viðskiptavinar er ekki sýnt fyrir viðskiptavini sem aðrir lögaðilar spyrjast fyrir um vegna þess að ekkert kenni viðskiptavinar hefur verið stofnað fyrir þá aðila í núverandi fyrirtæki. Hins vegar, ef starfsmaður opnar síðuna með viðskiptavinarupplýsingum, býr kerfið sjálfkrafa til viðskiptavinarkenni fyrir aðila og tengir einnig aðsetursbækur viðskiptavina verslunar við viðskiptavininn. Þess vegna verður viðskiptavinurinn sýnilegur í staðbundnum leitum sem eru gerðar síðar.

![Altæk viðskiptavinaleit.](./media/Globalcustomersearch.png "Altæk viðskiptavinaleit")

### <a name="additional-local-customer-search-capabilities"></a>Frekari leitareiginleikar staðbundins viðskiptavinar

Þegar notendur leita að símanúmeri hunsar kerfið sérstafi (t.d. bil, bandstrik og sviga) sem kann að hafa verið bætt við þegar viðskiptavinurinn var búinn til. Þess vegna þurfa gjaldkerar ekki að hafa áhyggjur af símanúmersniðinu þegar þeir leita. Til dæmis, ef símanúmer viðskiptavinar var slegið inn sem **123-456-7890**, getur gjaldkeri leitað að viðskiptavinum með því að slá inn **1234567890** eða með því að slá inn fyrstu tölur símanúmersins.

> [!NOTE]
> Viðskiptavinur getur haft mörg símanúmer og netföng. Reiknirit viðskiptavinaleitar leitar einnig í gegnum þessi aukalegu netföng og símanúmer, en síðan með leitarniðurstöðum um viðskiptavin sýnir aðeins aðalnetfang og aðalsímanúmer. Þetta getur valdið ruglingi því að niðurstöður um viðskiptavin sýna ekki netfangið eða símanúmerið sem leitað var að. Í síðari útgáfu er ætlunin að bæta skjámyndina fyrir leitarniðurstöður um viðskiptavin þannig að hún sýni þessar upplýsingar.

Hefðbundna viðskiptaleitin getur verið tímafrek vegna þess að hún leitar yfir mörg svæði. Þess í stað geta gjaldkerar leitað í einum eiginleika viðskiptavinar, eins og nafni, netfangi eða símanúmeri. Eiginleikarnir sem reiknirit viðskiptavinaleitar notar eru sameiginlega þekktir sem *leitarskilyrði viðskiptavinar*. Kerfisstjórinn getur auðveldlega stillt eitt eða fleiri skilyrði sem flýtileiðir sem birtast í POS. Vegna þess að leitin er takmörkuð við eitt skilyrði, eru aðeins viðeigandi leitarniðurstöður sýndar og afköstin er mun betri en afköst staðlaðrar viðskiptavinaleitar. Eftirfarandi skýringarmynd sýnir flýtileiðir viðskiptavinaleitar í POS.

![Flýtileiðir viðskiptavinaleitar.](./media/SearchShortcutsPOS.png "Flýtileiðir viðskiptavinaleitar")

Til að stilla leitarskilyrði sem flýtileiðir verður stjórnandinn að opna síðuna **Færibreytur Commerce** í Commerce og síðan á flipanum **POS leitarskilyrði** eru öll skilyrði valin sem eiga að birtast sem flýtileiðir.

![Skilgreina flýtileiðir leitar.](./media/ConfigureShortcutsAX.png "Skilgreina flýtileiðir leitar")

> [!NOTE]
> Ef þú bætir við of mörgum flýtileiðum verður fellivalmyndin á leitarstikunni í POS ofhlaðin og það getur haft áhrif á reynslu starfsmanns af leitinni. Við mælum með að þú bætir aðeins við eins mörgum flýtileiðum og nauðsynlegt er.

Reiturinn **Birta röð** ákvarðar röðina sem flýtileiðir eru sýndar í POS. Skilyrðin sem eru sýnd eru innbyggðir eiginleikar sem reiknirit viðskiptavinaleitar notar til að leita að viðskiptavinum. Hins vegar geta samstarfsaðilar bætt við sérsniðnum eiginleikum sem flýtivísunum. Til að bæta við sérsniðnum eiginleikum sem flýtivísunum þarf kerfisstjórinn að lengja framlengjanlega upptalningu (fasttexti) sem er notuð við leitarskilyrði viðskiptavinar og síðan merkja sérsniðna eiginleika samstarfsaðila sem flýtileiðir. Samstarfsaðilar bera ábyrgð á að skrifa kóðann til að finna niðurstöður þegar sérsniðnar flýtileiðir eru notaðar við leitir.

Þýðingar fyrir flýtileiðir eru nauðsynlegar ef þú vilt að flýtileiðir séu birtar á POS. Ef tungumál rásarinnar er annað en sjálfgefið tungumál kerfisins verður þú að skilgreina þýðinguna fyrir hverja flýtileið á væntanlegu tungumáli. Þú getur skilgreint þýðingar með því að velja **Þýða** fyrir hverja flýtileið. 

> [!NOTE]
> Sérsniðnum eiginleika sem er bætt við fasttextann hefur ekki áhrif á staðlað reiknirit viðskiptavinaleitar. Með öðrum orðum mun reiknirit viðskiptavinaleitar ekki leita í sérsniðnum eiginleikum. Notendur geta aðeins notað sérsniðna eiginleika fyrir leitir ef þessum sérsniðna eiginleika er bætt við sem flýtileið eða ef sjálfgefnu reikniriti leitar er hnekkt.

Smásöluaðilar geta einnig stillt sjálfgefna leitarstillingu viðskiptavinar á sölustað á **Leita í öllum verslunum**. Þessar skilgreiningar geta verið gagnlegar í aðstæðum þar sem leita verður strax í viðskiptavinum sem voru stofnaðir utan POS (til dæmis, jafnvel áður en dreifingarvinnslan er keyrð). Til að gera það þarf smásöluaðili að kveikja á valkostinum **Sjálfgefið leitarsnið viðskiptavinar** í virknireglu sölustaðar. Þegar hann er stilltur á **Já** munu allar leitartilraunir að viðskiptavini senda rauntímakall til höfuðstöðva.

Til að koma í veg fyrir óvænt afkastavandamál eru þessar stillingar faldar á bak við tilraunaútgáfuflagg sem heitir **CUSTOMERSEARCH_ENABLE_DEFAULTSEARCH_FLIGHTING**. Þess vegna, til að sýna stillinguna **Sjálfgefnar leitarstillingar viðskiptavina** í notandaviðmótinu (UI) ætti smásalinn að stofna stuðningsmiða fyrir samþykkisprófun notanda (UAT) og framleiðsluumhverfi. Þegar miðinn hefur verið móttekinn munu tæknimennirnir vinna með söluaðila til að ganga úr skugga um að smásalinn framkvæmi prófanir í umhverfi utan framleiðslu til að meta árangur og framkvæma allar fínstillingar sem krafist er.

## <a name="cloud-powered-customer-search"></a>Viðskiptavinaleit í skýinu

Opin forútgáfa af leitareiginleika viðskiptavinar með þjónustu Azure Cognitive Search hefur verið gefin út sem hluti af Commerce-útgáfu 10.0.18. Auk endurbóta á afköstum njóta notendur þjónustunnar góðs af mörgum lagfæringum og endurbótum tengdra möguleika. Afkastaendurbæturnar koma berlega í ljós þegar altækur leitareiginleiki („Leita í öllum verslunum“) sölustaðar er notaður. Það er vegna þess að leitarniðurstöður eru sóttar úr leitaratriðaskrá Azure í staðinn fyrir að vera fengnar úr gögnum í Commerce Headquarters. 

### <a name="enable-the-cloud-powered-search-feature"></a>Virkja leitareiginleika í skýinu

> [!NOTE]
> Þess er krafist að bæði Commerce Headquarters og Commerce Scale Unit séu uppfærð í útgáfu 10.0.18. Ekki er nauðsynlegt að uppfæra sölustaðinn.

Til að virkja leitareiginleika í skýinu í Commerce Headquarters skal fylgja þessum skrefum.

1. Opna skal **Kerfisstjórnun \> Vinnusvæði \> Eiginleikastjórnun**.
1. Leitið að og veljið eiginleikann **(Forútgáfa) Viðskiptavinaleit í skýinu** og veljið síðan **Virkja núna**.
1. Farið í **Smásala og viðskipti > Uppsetning höfuðstöðva > Viðskiptaverkraðari > Frumstilla verkraðara viðskipta** og veljið **Í lagi** til að sýna nýju vinnsluna **1010_CustomerSearch** á sniðinu **Dreifingaráætlun**.
1. Farið í **Smásala og viðskipti > Upplýsingatækni smásölu og viðskipta > Dreifingaráætlun**.
1. Keyrið vinnsluna **1010_CustomerSearch**. Þessi vinnsla gefur upp dagsetningu leitaratriðaskráar Azure. Þegar atriðaskráin hefur verið birt verður staða vinnslunnar stillt á **Notuð**.
1. Þegar vinnslustaðan **1010_CustomerSearch** er stillt á **Notuð** skal keyra vinnsluna **1110 - Global configuration** til að uppfæra rásir sölustaðar á nýlega virkjaða eiginleikanum í **Eiginleikastjórnun**.
1. Síðan skal keyra vinnsluna **1010_CustomerSearch** með reglulegu millibili til að senda uppfærslur viðskiptavina til leitaratriðaskráarinnar.

> [!NOTE]
> Fyrir fyrstu birtingu atriðaskráar gæti vinnslan **1010_CustomerSearch** tekið nokkrar klukkustundir því hún þarf að senda allar viðskiptavinafærslur til leitaratriðaskráar Azure. Næstu uppfærslur ættu að taka nokkrar mínútur. Á tímabilinu þegar leitareiginleikinn í skýinu er virkjaður en birtingu atriðaskráar er ekki lokið mun viðskiptavinaleitin úr sölustað fara sjálfgefið í fyrirliggjandi SQL-leit. Þetta tryggir að aðgerðir verslunar verði ekki fyrir truflunum.

### <a name="functional-differences-from-the-existing-search"></a>Munir á virkni miðað við núverandi leit

Eftirfarandi listi sýnir hvernig virkni viðskiptavinaleitar í skýinu er frábrugðin núverandi leitarvirkni. 

- Viðskiptavinir sem eru stofnaðir og breytt í Commerce Headquarters eru sendir í leitaratriðaskrá Azure þegar vinnslan **1010_CustomerSearch** er keyrð. Þessar uppfærslur taka að lágmarki 15 til 20 mínútur til að uppfæra atriðaskrána. Notendur sölustaðar geta leitað að nýjum viðskiptavinum (eða leitað út frá uppfærðum upplýsingum) um 15 til 20 mínútum eftir að uppfærslurnar eiga sér stað í Commerce Headquarters. Ef viðskiptaferlið krefst þess að strax verði hægt að leita á sölustað að viðskiptavinum sem stofnaðir eru í Commerce Headquarters, þá er þetta mögulega ekki rétta þjónustan fyrir þig.
- Nýir viðskiptavinir sem stofnaðir eru á sölustað eru sendir í leitaratriðaskrá Azure úr Commerce Scale Unit og verður hægt að leita að þeim strax í öllum verslunum. Ef hins vegar er kveikt á eiginleika fyrir stofnun ósamstillts viðskiptavinar verða nýjar færslur viðskiptavinar ekki sendar til leitaratriðaskráar Azure úr Commerce Scale Unit og verður ekki hægt að leita að þeim úr sölustað fyrr en upplýsingar um viðskiptavin eru samstilltar við Commerce Headquarters og kenni viðskiptavina eru búin til fyrir ósamstillta viðskiptavini. Vinnslan **1010_CustomerSearch** mun þá geta sent færslur ósamstilltra viðskiptavina til leitaratriðaskráar Azure. Það tekur að meðaltali um 30 mínútur áður en hægt verður að leita að nýlega stofnuðum, ósamstilltum viðskiptavinum á sölustað. Þetta mat gerir ráð fyrir að vinnslurnar **1010_CustomerSearch**, **P-vinnsla** og **Samstilla viðskiptavini og viðskiptafélaga úr async-stillingu** verði keyrðar á 15 mínútna fresti.
- Leit í skýinu leitar einnig að aukalegum netföngum og símanúmerum viðskiptavina, en sem stendur sýna niðurstöður viðskiptavinaleitar aðeins aðalsímanúmer og aðalnetfang viðskiptavina. Við fyrstu sýn kann að virðast að óviðkomandi leitarniðurstöðum hafi verið skilað, en athugun á aukalegu netfangi og símanúmeri viðskiptavinar í leitarniðurstöðum getur gengið úr skugga um hvort leitarorðin hafi skilað samsvörun viðskiptavinar. Til að forðast slíkan rugling eru uppi áform um að bæta síðu leitarniðurstaðna til að gera notendum auðveldara um vik að skilja hvers vegna leitarniðurstöðu var skilað.
- Krafan um að leita með því að nota a.m.k. 4 stafi í altækri leit („Leita í öllum verslunum“) á ekki við um þessa þjónustu.

> [!NOTE]
> Eiginleiki viðskiptavinaleitar sem notar þjónustu Azure Cognitive Search er tiltæk í forútgáfu á takmörkuðum svæðum. Eiginleiki viðskiptavinaleitar er *ekki* fyrir hendi í eftirfarandi löndum:
> - Brasilía
> - Indland

[!INCLUDE[footer-include](../includes/footer-banner.md)]
