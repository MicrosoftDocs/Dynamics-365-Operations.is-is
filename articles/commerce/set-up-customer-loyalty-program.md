---
title: Yfirlit yfir vildarkerfi
description: Í þessu efni er fjallað um vildarkerfi í Dynamics 365 Commerce og samsvarandi uppsetningarþrepum til að hjálpa smásala auðveldlega að byrja með vildarkerfi sín.
author: scott-tucker
manager: AnnBe
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailLoyaltyPrograms, RetailPriceDiscGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16201
ms.assetid: f79559d2-bc2d-4f0b-a938-e7a61524ed80
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 337ede63cb9175f2674bae8f2caaac5f1ba5f5cb
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022948"
---
# <a name="loyalty-overview"></a>Yfirlit yfir vildarkerfi

[!include [banner](includes/banner.md)]

Vildarkerfi geta hjálpað til við að auka viðskiptavinar hollustu með því að umbuna viðskiptavinum fyrir samskipti þeirra við vörumerki smásala. Í Dynamics 365 Commerce er hægt að setja upp einfalda eða flókið vildarkerfi sem gilda á milli lögaðila í hvaða viðskiptarás sem er. Í þessu efni er fjallað um vildarkerfi í Commerce og samsvarandi uppsetningarþrepum til að hjálpa smásala auðveldlega að byrja með vildarkerfi sín.

Þú getur sett upp vildarkerfi þannig að það innihaldi eftirfarandi eiginleika.

- Setja upp margar gerðir umbunar í vildarkerfi sem á að bjóða í vildarkerfi og rekja þátttöku í vildarkerfi.
- Setja upp vildarkerfi sem tákna mismunandi vildarpunkts hvatningargreiðslur sem er að bjóða. Hægt er að hafa með vildarkerfalög til að bjóða hærri hvatningargreiðslur og umbun til viðskiptavina sem kaupa oftar eða eyða meiri peningum í verslununum.
- Skilgreina yfirvinnutaxta reglur til að auðkenna þá verkþætti sem viðskiptavinur verður að ljúka við ávinna umbun. Einnig er hægt að skilgreina innlausnarreglur til að auðkenna hvenær og hvernig viðskiptavinur getur innleyst umbun.
- Gefa út vildarkort frá hvaða rás sem tekur þátt í vildarkerfi og tengja vildarkort við eitt eða fleiri vildarkerfi sem viðskiptavinurinn getur tekið þátt í. Þú getur einnig tengt færslu viðskiptavinar við vildarkort til að auðvelda viðskiptavininum að safna vildarstigum af mörgum kortum og innleysa þau.
- Handvirkt stilla vildarkort eða flytja stöðu vildarumbunar af einu korti á annað til að koma til móts við eða umbuna viðskiptavinum.

## <a name="setting-up-loyalty-programs"></a>Uppsetning vildarkerfa

Setja verður upp nokkra þætti til að virkja eiginleikann vildarpunkta í Commerce. Eftirfarandi skýringarmynd sýnir eiginleika vildarkorts og hvernig þeir tengjast hvort öðru.

![vinnsluflæði kerfisuppsetningar](./media/loyaltyprocess.gif "Vildarþættir og hvernig þeir tengjast hver öðrum")

## <a name="loyalty-components"></a>Eiginleikar vildarkerfis

Eftirfarandi tafla lýsir hvert eiginleika og hvar það er notað í uppsetningu vildarkerfis.

| Hluti                                        | lýsing | Þar sem það er notað |
|--------------------------------------------------|-------------|-----------------|
| Setja upp afslætti (skilyrði)                  | Setja upp afslætti sem bjóða á viðskiptavinum vildarkerfis. Til dæmis má bjóða 5 prósent af öllum fatnaði. | Afslættir verður að bæta við verðflokka áður en hægt er að taka þá með í vildarkerfi. Verðflokkar eru úthlutaðar á vildarkerfi og vildarlög. |
| Setja upp verðflokka (skilyrði)               | Verðflokkar eru notaðir til að stofna og stjórna verð og afslætti afurða. Setja upp verðflokka sem inniheldur afslætti sem eiga við vildarkerfi. | Verðflokkar eru tengdir við vildarkerfi og vildarkerfalögum. |
| Setja upp rásir (skilyrði)                   | Viðskiptarásir eru verslanir sem taka þátt í þínu vildarkerfi, s.s. hefðbundnar verslanir eða netverslun, eða símaver. Setja verður upp rásir áður en hægt er að úthluta vildarkerfi þeim. | Þú úthlutar rás til vildarkerfis ef rásin tekur þátt í vildarkerfinu. |
| Setja upp Vildargreiðsluháttur (frumskilyrði) | Setða verður upp greiðslumáta áður en hægt er að nota vildarkort við afgreiðslukassann og innleysa vildarpunkta sem hluta af vildarkerfi. Þarf einnig að bæta við vildargreiðsluháttur við rásar áður en viðskiptavini geta innleysa vildarpunkta þeirra sem greiðslu fyrir afurðir. | Setja upp greiðslumáta vildarkerfis gerð og úthluta á vildargreiðsluháttur rása sem tekur þátt í vildarkerfinu. |
| Setja upp dagsetningabil                            | Dagsetningabil gefa upp á sveigjanlega leið til að setja tímabil sem á við vildarlög. Tímabil eru notuð til að tilgreina lengd þess tíma sem viðskiptavinur getur verið í lagi eða til hversu mikinn tíma viðskiptavinurinn hefur til að klára aðgerð til að geta fengið lag. | Dagsetningabil eiga einungis ef lög erum notuð í vildarkerfum. Velja dagsetningabilið sem á við kerfislög og tímabil sem á við reglur vildarlags forritið. |
| Setja upp umbunarstig                             | Vildarpunktar eru gerðir umbunar sem er að bjóða viðskiptavinum. Umbunarpunktar getur verið innleysanlegur eða ekki innleysanlegur. Hægt er að skipta innleysanlega vildarpunkta fyrir afurðir. Óinnleysanlegir vildarpunktar eru notaðir til rakningar eða fyrirframgreiðslu til viðskiptavinar í næsta lagi í vildaráætluninni. | Vildarpunktar eru tilvísað í reglum vildarlags og eru notaðir til að viðurkenna viðskiptavinar fyrir tiltekið lag. Vildarpunktar eru einnig vísað í vildarkerfi í reglur tekna og innlausn. Í tekjureglur, tilgreina umbun sem viðskiptavinur getur unnið inn fyrir tiltekinn verkþátt. Í innlausnarreglur, tilgreinir þú umbun sem er viðskiptavinur getur innleyst. |
| Setja upp vildarkerfi                          | Vildarkerfi eru kjarnavildareining sem þú býður upp á. Hvert vildarkerfi má einnig hafa vildarlögum sem er úthlutað á það. Afslættir og verðflokka eru úthlutaðir á vildarkerfi annaðhvort á forritsstigi eða í lagi stigi lagsins. | Stofna vildarkerfi fyrir við vildarkerfi. Þú tengir vildarkort við vildarkerfið, og hægt er að úthluta vildarkortum til viðskiptavinar. Viðskiptarásir taka þátt í vildarkerfi sem eru tengdir við vildarkerfi. Viðskiptavinir sem eru með vildarkort geta tekið þátt í vildarkerfum sem er úthlutað á kortið. |
| Setja upp vildarlög og vildarlagsreglur              | Vildarlög eru valfrjáls stig sem þú getur tilgreint fyrir vildarkerfi þín. Þú getur sett upp grunnafslætti og umbun fyrir alla viðskiptavini sem taka þátt í hollustuáætlun, og þú getur sett upp fleiri afslætti og umbun fyrir viðskiptavini sem náð í mismunandi stig í áætluninni. Hægt er að setja upp reglur sem viðurkenna viðskiptavin fyrir hvert lag fyrir hverja vildarlag sem þú skilgreinir. Einnig er hægt að skilgreina hversu lengi viðskiptavinir geta verið í lagi eftir að þeir hafa náð því. | Vildarlög og vildarlagareglur eru skilgreind í vildarkerfum. Ef ekki eru skilgreind nein vildarlög, fá allir viðskiptavinir sem taka þátt í vildarkerfinu afslætti sem þú úthlutar í verðflokki vildarkerfisins. Ef vildarlög eru skilgreind, er hægt að setja upp tekjukóða reglur og innlausnarreglur fyrir vildarlög í vildarkerfinu. |
| Uppsetning vildarkerfa                           | Vildarskemu tilgreina ávinningsreglur og innlausnarreglur sem gilda í ákveðnum vildarkerfi. Þú úthlutar rás til vildarkerfis til að auðkenna hvaða vildarkerfi, tekjureglur og innlausnarreglur eiga við verslun. | Vildarskema er úthlutað á vildarkerfi og til rása. Hægt er að úthluta mörgum vildarkerfum til sama vildarkerfis og hægt er að úthluta mörgum vildarkerfum til margra rása. |
| Uppsetning vildarkorta                             | Vildarkort veitir handhafa kortsins rétt til að taka þátt í vildarkerfi sem er úthlutað á kort. Vildarkort má gefa út nafnlaust eða hægt er að úthluta þeim til ákveðins viðskiptavinar. Hægt er að skoða færslur vildarpunkta fyrir tilteknu korti og hægt er að skoða yfirlit yfir vildarpunkta sem hafa verið á kortinu. Hægt er að gefa út vildarkort frá hvaða rás sem er. Hægt er að leiðrétta einnig handvirkt vildarkort til að uppfæra viðskiptavini í annað lag, bæta við vildarpunktum eða flytja vildarpunktastöðu af einu korti til annars. | Þú úthlutar vildarkerfi á vildarkort. |

## <a name="loyalty-processes"></a>Vildarferli

Eftirfarandi tafla lýsir ferla sem þarf að keyra til að senda vildarskilgreiningum og gögnin í verslununum og til að sækja vildarfærslur frá verslununum þínum.

| Heiti ferlis                         | Lýsing | Heiti síðu |
|--------------------------------------|-------------|-----------|
| 1050 (vildarupplýsingar)           | Keyra þetta ferli til að senda vildargögn úr Commerce í smásöluverslun. Það er góð hugmynd að skipuleggja þetta ferli til að keyra oft, þannig að vildargögn séu sendar til allra verslana. | Dreifingaráætlun |
| Vinna úr vildarkerfi              | Keyra þetta ferli til að tengja vildarkerfi með rásir sem eru tengdar við vildarkerfi. Hægt er að raða þetta ferli til að keyra sem runuvinnslu. Keyra þarf þetta ferli ef skilgreiningargögn vildarpunkta er breytt, eins og vildarkerfi, vildaráætlanir, eða vildarpunktar vildarkerfis. | Vinna úr vildarkerfi |
| Bóka áunna vildarpunkta í runuvinnslu | Keyra þetta ferli til að uppfæra vildarkort til að taka með færslur sem var unnin án tengingar. Þetta ferli gildir aðeins ef gátreiturinn **Bóka áunna punkta í runuvinnslu** er valinn á **Samnýttar færibreytur Commerce** síðu, svo hægt er að fá umbun án nettengingar. | Bóka áunna vildarpunkta í runuvinnslu |
| Uppfæra vildarkortalög            | Keyra þetta ferli til að meta tekjuaðgerðir viðskiptavinar gagnvart vildarlagsreglum fyrir vildarkerfi og til að uppfæra stöðu lags viðskiptavinar. Þetta ferli er þarft eingöngu ef reglum vildarkerfis er breytt og uppfærðar reglur eiga að vera beitt afturvirkt fyrir vildarkort sem hefur þegar verið gefið út. Þetta ferli er hægt að keyra sem runuvinnslu eða fyrir einstaka spjöld. | Uppfæra vildarkortalög |

## <a name="loyalty-enhancements"></a>Vildarkerfisviðbætur

Commerce hefur nýja vildarkerfisvirkni sem hluti af útgáfu október 2018. Hvert af nýju viðbótunum er lýst hér að neðan.

- Sem hluti af vildarkerfi í fyrri útgáfum gætu smásalar búið til mismunandi reglur um tekjur og innlausn með vildarlögum til að greina á milli umbunarfyrir viðskiptavini í mismunandi lögum. Söluaðilar geta nú með "tengingar" verið hluti af reglum um tekjur og innlausn þannig að ákveðinn hópur viðskiptavina geti verið hluti af núverandi lögum, en samt verðlaunaður á annan hátt. Þetta kemur í veg fyrir þörfina á að búa til fleiri lög.
    
    > [!NOTE]
    > Tekjureglur innan vildarkerfis eru viðbótar. Til dæmis, ef þú býrð til reglu til að umbuna meðlimi í gulllagi 10 stig fyrir hvern Bandaríkjadal og þú stofnar einnig reglu fyrir viðskiptavin með „uppgjafahermannstengsl“til að umbuna 5 stig fyrir hvert Bandaríkjadal, þá er uppgjafahermaður sem er líka meðlimur í gulllagi myndi vinna sér inn 15 stig fyrir 1 Bandaríkjadal, þar sem viðskiptavinurinn uppfyllir skilyrði fyrir báðar línur. Hins vegar, ef viðskiptavinurinn sem er uppgjafahermaður var ekki meðlimur í gulllagi, þá myndi hann vinna sér inn 5 stig fyrir hvern dollar. Til að endurspegla breytingar á rásum skaltu keyra **Vinnslu vildarkerfis** og **1050** (upplýsingar um vildarkerfi) störf.
    
    ![Tengslamiðaðar tekjur](./media/Affiliation-based-earning.png "Tengslamiðaðar tekjur")

- Smásalar hafa oft sérstakt verð fyrir ákveðna hóp viðskiptavina að þeir vilja ekki að vildarkerfi eigi við um. Til dæmis, heildsalar eða starfsmenn sem fá sérstakt verð og enga vildarpunkta. Venjulega eru „tengingar“ notaðir til að veita sérstökum verðlagningu til slíkra viðskiptavinahópa. Til að takmarka tiltekna viðskiptavinahópa viðskiptavina frá því að vinna sér inn vildarpunkta, getur smásalinn tilgreint eitt eða fleiri tengsl við **Útilokuð tengsl** hlutann í vildarkerfinu. Þannig að þegar viðskiptavinir sem tilheyra útilokaðir tengingar eru núverandi meðlimir vildarkerfis, munu þeir ekki geta fengið vildarpunkta fyrir kaup sín. Til að endurspegla breytingar á rásum skaltu keyra **Vinnslu vildarkerfis** og **1050** (upplýsingar um vildarkerfi) störf.

    ![Útilokuð tengsl](./media/Excluded-affiliations.png "Útiloka tengsl frá því að vinna sér inn vildarpunkta")
    
- Smásalar geta búið til vildarkortsnúmer í rásunum. Fyrir uppfærslu október 2018 gætu smásalar notað efnisleg vildarkort eða búið til vildarkort með því að nota einstakar upplýsingar um viðskiptavin eins og símanúmer. Til að virkja sjálfvirka framleiðslu á vildarkortum í verslunum skaltu kveikja á **Búa til vildarkortsnúmer** í virknireglunni sem tengist versluninni. Fyrir netrásir geta smásalar notað IssueLoyaltyCard API til að gefa út vildarkort til viðskiptavina. Smásalar geta annaðhvort veitt vildarkortsnúmer til þessa API, sem verður notaður til að búa til vildarkortið, eða kerfið mun nota vildarkortsnúmeraröðina sem er sett í Commerce. Hins vegar, ef númeraröðin er ekki til staðar, og smásalinn gefur ekki upp vildarkortsnúmer meðan þú hringir í API, þá birtist villa.

    ![Búa til vildarkort](./media/Generate-loyalty-card.png "Búðu til sjálfkrafa vildarkortanúmer")

- Áunnir og innleystir vildarpunktar eru nú vistaðar fyrir hverja færslu og sölupöntun gegn sölulínunni þannig að sama upphæð geti verið endurgreitt eða tekið til baka þegar um er að ræða heil vöruskil eða vöruskil að hluta. Þar að auki, með því að hafa sýnileika á sölulínu er möguleiki fyrir notendur símavers að svara spurningum viðskiptavina um hversu mörg stig voru áunnin eða innleyst fyrir hverja línu. Áður en þessar breytingar voru gerðar voru vildarpunktar alltaf endurreiknar við vöruskil, sem leiddi til annars upphæð en upphaflega ef ávinnings- eða innlausnarreglur voru breytilegar og notendur símavers höfðu ekki sýnileika á sundurliðun vildarpunkta. Hægt er að skoða vildarpunktana undir **Kortafærslur** eyðublaðinu fyrir hvert vildarkort. Til að virkja þennan eiginleika skal kveikja á skilgreiningunni **Bóka vildarpunkta á hverja sölulínu** undir flipanum **Samnýttar færibreytur Commerce** \> **Almennt**.

    > [!NOTE]
    > Við mælum eindregið með því að kveikja á þessum eiginleika til að tryggja að hægt sé að endurgreiða réttan fjölda punkta eða taka frá viðskiptavininum ef skilað er.

- Smásalar geta nú skilgreint ávinnslutímabilið fyrir hvern vildarpunkt. Ávinnslutímabilið mun skilgreina lengdina frá ávinningsdegi, en eftir það verður vildarpunktarnir tiltæk fyrir viðskiptavini. Punktar sem ekki eru áunnir má skoða í **Punktar sem ekki eru áunnir** dálki á **Vildarkort** síðu. Auk þess geta smásalar skilgreint hámark vildarpunkta á hverju vildarkorti. Þetta svæði er hægt að nota til að draga úr áhrifum svika í vildarkerfi. Þegar hámarksvildarpunktum hafa verið náð, getur notandinn ekki áunnið sér fleiri stig. Smásalinn getur ákveðið að útiloka slík kort þar til þeir hafa rannsakað um hugsanlega svik. Ef smásali ákveður svik, getur smásalinn ekki aðeins lokað vildarkortinu fyrir viðskiptavininn heldur einnig merkt viðskiptavininn sem útilokaðan. Til að gera það skaltu stilla **Útiloka viðskiptavin frá skráningu í vildarkerfi** eiginleikann á **Já** undir **Allir viðskiptavinir** á **Commerce** flýtiflipanum. Útilokaðir viðskiptavinir geta ekki fengið útgefin vildarkort í neinum rásum.

    ![Ávinnsla og hámark vildarpunkta](./media/Vesting-and-maximum-reward-points.png "Skilgreina ávinnslu og hámark vildarpunkta")

- Tengsl er til að veita sérstakt verð og afslætti, en það eru nokkur tengsl sem smásalar vilja ekki að viðskiptavinir þeirra sjái. Til dæmis gæti tengsl sem heitir „viðskiptavinur sem eyðir miklu“ ekki verið vel tekið af sumum viðskiptavinum. Þar að auki eru nokkur tengsl sem ekki ætti að stjórna í versluninni, til dæmis starfsmenn, vegna þess að þú vilt ekki að gjaldkerar ákveði hverjir séu starfsmenn og fá þannig starfsmannabundna afslætti. Smásalar geta nú valið tengsl sem ætti að vera falið í rásum. Tengsl merkt sem **Fela í rásum** er ekki hægt að skoða, bæta við eða fjarlægja á sölustað. Hins vegar verður verðlagning og afsláttur sem tengist tengslunum ennþá beitt á vörurnar.

    ![Fela tengsl](./media/Hide-affiliations.png "Fela tengsl í rásum")
    
- Notendur símavers geta nú auðveldlega leita fyrir viðskiptavini með þeirra vildarkortsupplýsingar og fletta að vildarkorts- og vildarkortsfærslusíðum viðskiptavinarins frá **Þjónustudeild** síðu.

    ![Þjónusta við viðskiptavini](./media/Customer-service.png "Leita að vildarupplýsingum fyrir viðskiptavininn")
    
- Ef vildarkortið er í hættu þarf að búa til annað kort í staðinn og núverandi punktar flutt á nýtt kort. Flæði á nýjum kortum hefur verið einfaldað í þessari útgáfu. Auk þess geta viðskiptavinir gefið sumum eða öllum vildarpunkta sínum til vina og fjölskyldu. Þegar punktar eru flutt eru færslur til stillingar á punktum búnar til fyrir hvert vildarkort. Nýja kortið og stöðuvirkni er hægt að nálgast frá **Vildarkort** síðu.

    ![Skipta um og flytja punkta](./media/Replace-and-transfer-points.png "Skiptu um vildarkort eða millifærðu jafnvægi")
    
- Smásalar gætu viljað fanga árangur tiltekinnar rásar til að skrá viðskiptavini inn í vildarkerfi. Uppruni skráningar fyrir vildarkortin er nú vistuð þannig að smásalar geta keyrt skýrslur um þessi gögn. Uppruni skráningar er sjálfkrafa fangaður fyrir öll útgefnu vildarkort frá MPOS/CPOS eða e-Commerce rásum. Fyrir vildarkortin sem eru gefin út af bakvinnsluforritinu getur notandi símavers valið viðeigandi rás.
- Í fyrri útgáfum gætu smásalar notað MPOS / CPOS til að innleysa vildarpunkta fyrir viðskiptavini í verslun. Hins vegar, í þessum útgáfum, vegna þess að vildarstaða er sýnd í vildarpunktum, gat gjaldkeri ekki séð gjaldmiðilsupphæðina sem hægt væri að beita við núverandi færslu. Gjaldkerinn þurfti að breyta punktum í gjaldmiðilinn áður en hann greiddi með vildarpunktum. Í núverandi útgáfu, eftir að línur hafa verið bætt við færsluna, getur gjaldkerinn séð þá upphæð sem vildarpunktar geta náð til við núverandi færslu, sem gerir það auðvelt að beita sumum eða öllum vildarpunktunum við viðskiptin. Þar að auki getur gjaldkeri séð punktana sem munu renna út á næstu 30 dögum svo að þeir geta beitt viðbótarsölu eða krosssölu til að hvetja viðskiptavininn til að eyða punktunum sem eru að renna út í þeirri færslu.

    ![Punktar sem staða vildarpunkta nær yfir](./media/Points-covered-by-loyalty-balance.png "Sýna stöðu sem vildarpunktar ná yfir")

    ![Punktar sem eru að renna út](./media/Expiring-points.png "Skoða punkta sem eru að renna út")

- Með útgáfunni 8.1.3 höfum við virkjað valkostinn „greiða með vildarpunktum“ í rás símavers. Til að virkja þennan möguleika skaltu búa til greiðslumáta fyrir vildarpunkta og tengja hana við símaverið. 

    > [!NOTE]
    > Vegna þess að vildargreiðslurnar eru settar upp sem kortagreiðslur verður þú að velja kort á síðunni **Kortauppsetning**. 

    ![Uppsetning á vildarkorti](./media/LoyaltyCardSetup.png "Uppsetning á vildarkorti")

    Eftir að þetta er komið upp geta viðskiptavinir innleyst vildarpunktana í símaverinu. Að auki erum við að efla upplifun notenda enn frekar til að sýna „Upphæð sem fellur undir vildarpunkta", svo að notendur símaversins þurfi ekki að fletta á milli skjáa til að skoða vildarinneignina.

- Margir smásalar umbuna aðeins vildarpunktum miðað við sölufærslur en fleiri viðskiptavinamiðaðir smásalar vilja umbuna viðskiptavinum sínum fyrir hvers konar virk samskipti þeirra við vörumerkið. Til dæmis vilja þeir umbuna fyrir að fylla út könnun á netinu, heimsækja verslun, líka við smásala á Facebook, tvíta um smásalann og fleira. Til að gera það getur smásalinn skilgreint hvaða fjölda sem er af „Önnur verkþáttargerð“ og skilgreint samsvarandi tekjureglur fyrir þessar aðgerðir. Einnig er til staðar API Commerce Scale Unit „PostNonTransactionalActivityLoyaltyPoints“ sem hægt er að hringja í þegar aðgerð er fundin sem ætti að umbuna viðskiptavinum með vildarpunktum. Þetta API gerir ráð fyrir auðkenni vildarkorts, auðkenni rásar og auðkenni annarrar verkþáttargerðar svo hægt sé að staðsetja viðskiptavininn sem ætti að fá umbun og til að finna út tekjuregluna fyrir verkþáttinn. 

    Úthlutun punkta fyrir verkþætti sem tilheyra ekki færslum felur venjulega í sér tvö stór skref:

    - Verkþáttur finnst sem ætti að umbuna.
    - Úthlutun á viðeigandi punktum.

    Fyrsta skrefið er utan við Commerce, t.d. tvít um vörumerkið eða líka við vörumerkið á Facebook. Eftir að borið hefur verið kennsl á verkþáttinn geta smásalarnir hringt í ofangreindan API Commerce Scale Unit og úthlutað vildarpunktum í rauntíma. Í slíkum tilvikum er engin þörf á yfirferð vegna þess að verkþáttur hefur átt sér stað og samsvarandi punktum á að úthluta. Hins vegar eru aðstæður þar sem smásali myndi vilja endurskoða skrárnar áður en punktum er úthlutað. Til dæmis hefur smásalinn sett upp vinnusmiðju í versluninni sem viðskiptavinirnir skrá sig í á vefsvæðinu eða öðrum forritum sem bjóða upp á viðburðarskráningu. Hins vegar eiga aðeins viðskiptavinir sem mæta að vinna sér inn vildarpunkta. Fyrir slíkar aðstæður, í 10.0 útgáfunni kynntum við gagnaeiningu sem heitir **Línur fyrir aðrar verkþáttargerðir vildarpunkta í smásölu**. Þessi gagnaeining gerir smásölum kleift að nota annaðhvort Ramma fyrir inn- og útflutning gagna (DIXF) eða OData API til að skrá verkþættina sem eiga að veita viðskiptavinum vildarpunkta. Gagnaeiningin geymir verkþættina í færslubók sem heitir **Vildarlínur fyrir aðra verkþætti** sem hægt er að nota til þess að yfirfara og breyta. Eftir að gögnin hafa verið yfirfarin getur tæknimaður annaðhvort bókað verkþáttarlínurnar handvirkt eða keyrt verk sem heitir **Vinna úr öðrum verkþáttargerðum fyrir vildarlínur** sem mun bóka allar óbókuðu verkþáttarlínurnar og úthluta punktunum til viðskiptavina samkvæmt tekjureglunum. Í ofangreindri atburðarás myndi forrit viðburðarskráningar hringja í Odata API til að senda upplýsingar um viðskiptavin til Commerce. Hins vegar getur tæknimaðurinn bókað verkþáttarlínurnar fyrir aðeins þessa viðskiptavini sem tóku þátt í vinnusmiðjunni og eytt verkþáttarlínunum hjá hinum viðskiptavinunum. 

    > [!NOTE]
    > Eins og er neyðir kerfið notendur til að setja upp númeraröð fyrir „aðrar verkþáttargerðir“, en það skref reynist ekki nauðsynlegt í framtíðarútgáfum. Til að setja upp númeraröð skal fara í **Samnýttar færibreytur Commerce** \> **Númeraraðir** og velja númeraröð fyrir **Auðkenni fyrir vildarpunkta annarra verkþáttargerða**.

- Til að bjóða upp á góða þjónustu við viðskiptavini og á áhrifaríkan hátt leysa fyrirspurnir viðskiptavina er mikilvægt að gjaldkerar hafi aðgang að öllum notandaupplýsingum viðskiptavinar. Með útgáfu 10.0 geta gjaldkerar séð upplýsingar um vildarpunktaferil ásamt tengdu vildarkerfi lagskiptar upplýsingar í POS.
- Ókeypis eða afhending með afslætti er einn af mjög hvetjandi þáttum viðskiptavina til að kaupa á netinu. Til að gera smásala kleift að setja upp kynningartilboð á afhendingum með útgáfu 10.0, höfum við kynna nýja tegund kynningar þar sem ber heitið „Þröskuldarafsláttur afhendingar“ þar sem smásalinn getur skilgreint viðmiðunarmörk sem, þegar þeim er náð, munu gera viðskiptavinum kleift að fá afslátt á eða ókeypis sendingarkostnað. Til dæmis, eyða $35 fyrir ókeypis „Tveggja daga sendingu“ eða ókeypis „Tveggja daga sendingu“ fyrir alla vildarviðskiptavini. Þessi eiginleiki nýtir nýjan ítarlegan möguleika sjálfvirkra gjalda. Vísa í [fylgiskjöl í ítarlegum sjálfvirkum greiðslum](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges). Þessi ítarlegu sjálfvirku gjöld verða að vera virkjuð svo afhendingartilboð virki. Hægt er að virkja þau í flipanum **Pantanir viðskiptavinar** á síðunni **Færibreytur Commerce** og kveikja á skilgreiningunni „Nota ítarleg sjálfvirk gjöld“. Vegna þess að söluaðili getur sett upp margar tegundir gjalda, t.d. meðhöndlun eða uppsetningu, þarf söluaðili einnig að tilgreina hvaða gjald er litið á sem sendingargjald. Þessir flutningsafslættir eru einungis notaðir fyrir sendingargjöld. Til að tilgreina gjald sem sendingargjald skal fara í skjámyndina **Gjaldakóðar** sem má finna undir **Retail og Commerce** \> **Upplýsingatækni Retail og Commerce** \> **Uppsetning rásar** \> **Gjöld** og kveikja á gátreitnum „Sendingargjald“ fyrir æskileg gjöld. Nú getur þú farið í skjámyndina **Þröskuldarafsláttur fyrir afhendingu** og sett upp afsláttinn.

    Líkt og með vöruafslætti virðir þessi afsláttur alla núverandi staðlaða afsláttarmöguleika, t.d. að leyfa söluaðilum að takmarka þessa afslætti með afsláttarmiðum þannig að aðeins viðskiptavinir með afsláttarmiða geta fengið þessa afslætti. Einnig nýta þessir afslættir möguleika verðflokka til að ákvarða hæfi slíkra afslátta. Til dæmis getur smásali valið að keyra þessi kynningartilboð aðeins í netrásum og/eða yfir rásir fyrir tiltekna hópa viðskiptavinahópa, svo sem vildarvina. Eftir að pöntunarlínur með tilgreindan afhendingarmáta standast skilgreindan þröskuld, þá verður sendingarafsláttur notaður og dregur úr sendingargjaldi miðað við uppsetningu afsláttar. 

    > [!NOTE]
    > Ólíkt öðrum reglubundnum afsláttum, t.d. magni, einfalt, blanda og samsvara og þröskuldarafslættir, þá býr sendingarafsláttur ekki til afsláttarlínur, heldur breytir sendingargjaldinu með beinum hætti og bætir heiti afsláttarins við lýsingu gjaldsins.
