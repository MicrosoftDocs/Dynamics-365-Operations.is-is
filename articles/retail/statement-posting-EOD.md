---
title: "Endurbætur á virkni yfirlitsbókunar"
description: "Þetta efnisatriði lýsir endurbótum sem hafa verið gerðar á bókun uppgjörs eiginleikanum."
author: josaw1
manager: AnnBe
ms.date: 04/26/2016
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.search.region: Global
ms.search.industry: retail
ms.author: anpurush
ms.search.validFrom: 2018-04-30
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 190d0b59ad2e232b33b3c0d1700cbaf95c45aeca
ms.openlocfilehash: 3e8c5466a68fa87326c46a4e36bf7399be1279c6
ms.contentlocale: is-is
ms.lasthandoff: 01/04/2019

---

# <a name="improvements-to-statement-posting-functionality"></a>Endurbætur á virkni yfirlitsbókunar

[!include[banner](includes/banner.md)]

Þetta efnisatriði lýsir fyrsta safni endurbóta sem hafa verið gerðar á bókun uppgjörs eiginleikanum. Þessar endurbætur eru í boði í Microsoft Dynamics 365 for Finance and Operations 7.3.2.

## <a name="activation"></a>Virkjun

Sjálfgefið er, við uppsetningu á Finance and Operations 7.3.2, að forritið er sett upp til að nota eldri eiginleika á bókun uppgjörs. Til að virkja endurbættan eiginleika á bókun uppgjörs verður þú að kveikja á skilgreiningarlyklinum fyrir hann.

- Farðu í **Kerfisstjórnun** \> **Uppsetning** \> **Leyfisskilgreinin** og síðan undir hnútnum **Smásala** skal hreinsa gátreitinn **Smásöluyfirlit (eldra)** og velja gátreitinn **Smásöluyfirlit**.

Þegar kveikt er á nýja skilgreiningarlyklinum fyrir **Smásöluuppgjör** er nýtt valmyndaratriði sem heitir **Smásöluuppgjör** tiltækt. Þetta valmyndaratriði gerir þér kleift að búa til handvirkt, reikna og bóka uppgjör. Öll uppgjör sem valda villu þegar runubókunarferlið er notað verða einnig tiltæk í gegnum þetta valmyndaratriði. (Þegar kveikt er á skilgreiningarlyklinum fyrir **Smásöluuppgjör (eldra)** er valmyndaratriðið kallað **Opin yfirlit**.)

Finance and Operations felur í sér eftirfarandi staðfestingar sem tengjast þessum skilgreiningarlyklum:

- Ekki er hægt að kveikja á báðum skilgreiningarlyklunum á sama tíma.
- Það verður að nota sömu skilgreiningarlyklana fyrir allar þær aðgerðir sem eru framkvæmdar á tilteknu uppgjöri á meðan á líftíma þess stendur (stofna, reikna út, hreinsa, bóka, o.s.frv.). Til dæmis getur þú ekki búið til og reiknað út uppgjör á meðan kveikt er á skilgreiningarlyklinum fyrir **Smásöluuppgjör (eldra)** og síðan reyna að bóka sama uppgjör á meðan kveikt er á skilgreiningarlyklinum fyrir **Smásöluuppgjör**.

> [!NOTE]
> Við mælum með því að þú notir skilgreiningarlykilinn fyrir **Smásöluuppgjör** fyrir endurbættan eiginleika á bókun uppgjörs, nema þú hafir góðar ástæður fyrir því að nota í staðinn skilgreiningarlykilinn fyrir **Smásöluuppgjör (eldra)**. Microsoft mun halda áfram að fjárfesta í nýjum og bættum eiginleika fyrir bókun uppgjörs og það er mikilvægt að þú skiptir yfir í hann eins fljótt og auðið er til að njóta góðs af honum. Eldri eiginleiki fyrir bókun uppgjörs verður gerður úreltur í framtíðarútgáfu.

## <a name="setup"></a>Setja upp

Sem hluti af endurbótum á eiginleikanum fyrir bókun uppgjörs hafa þrjár nýjar færibreytur verið kynntar til sögunnar á flýtiflipanum **Uppgjör** á flipanum **Bókun** á síðunni **Smásölufæribreytur**:

- **Slökkva á hreinsun upppgjörs** - Þessi valkostur er aðeins tiltækur í eldri eiginleika á bókun uppgjörs. Við mælum með að þú stillir þennan valkost á **Nei** til að koma í veg fyrir að notendur hreinsi uppgjör sem eru í hálfbókaðri stöðu. Ef yfirlýsingar, sem eru í hálfbókaðri stöðu, eru hreinsaðar skemmast gögn. Þú ættir að stilla þennan valkost á **Já** aðeins í undantekningartilvikum.
- **Frátekning birgða við útreikning** - Við mælum með því að þú notir runuvinnsluna **Bóka birgðir** fyrir birgðafrátekningu og að þú stillir þennan valkost á **Nei**. Þegar þessi valkostur er stilltur á **Nei** reynir endurbætti eiginleikinn á bókun uppgjörs ekki að búa til færslur birgðafrátekningar á meðan á útreikning stendur (ef færslur voru ekki þegar búnar til í gegnum runuvinnsluna **Bóka birgðir**). Í staðinn býr eiginleikinn til færslur birgðafrátekningar aðeins þegar bókun á sér stað. Þessi framkvæmd var hönnunarval og byggðist á þeirri staðreynd að tímaglugginn á milli útreikningsferlis og bókunarferlis er yfirleitt lítill. Ef þú vilt hins vegar taka frá birgðir á meðan á útreikningi stendur getur þú stillt þennan valkost á **Já**.

    Eldri eiginleikinn fyrir bókun uppgjörs tekur alltaf frá birgðir á meðan á útreikningsferli uppgjörs stendur yfir (ef frátekning var ekki þegar gerð í gegnum runuvinnsluna **Bóka birgðir**), án tillits til stillingar á þessum valkosti.

- **Gera þarf talningu óvirka** - Þegar þessi valkostur er stilltur á **Já** heldur bókunarferli á uppgjöri áfram, jafnvel þótt mismunurinn á talinni upphæð og færsluupphæð í uppgjörinu sé utan markanna sem eru skilgreind í flýtiflipanum **Uppgjör** fyrir smásöluverslun.

Þar að auki hefur reiturinn **Hámarksfjöldi samhliða uppgjörsbókana** verið kynntur til sögunnar á flýtiflipanum **Runuvinnsla**. Þessi reitur skilgreinir fjölda runuverka sem ætti að keyra á sama tíma. Eins og er þarftu að stilla gildið á þessum reit handvirkt.

Einnig, með nýja bókunarferlinu, er nauðsynlegt að skilgreina **Gjafakortsvara** í flýtiflipanum **Gjafakort** í flipanum **Bókun** á síðunni **Færibreytur smásölu**. Þetta á við, jafnvel þótt engin gjafakort séu notuð af fyrirtækinu.

Athugaðu að allar stillingar og færibreytur sem tengjast bókun uppgjörs og sem eru skilgreindar í smásöluverslun og á síðunni **Færibreytur smásöluverslana** eiga við í endurbættum eiginleika fyrir bókun uppgjörs.

## <a name="processing"></a>Í vinnslu

Hægt er að reikna út og bóka uppgjör í lotu með valmyndaratriðinu **Útreikningur uppgjörs í runu** og **Bóka uppgjör í runu**. Að öðrum kosti er hægt að reikna út og bóka uppgjör handvirkt með valmyndaratriðinu **Smásöluuppgjör** sem endurbætti eiginleikinn fyrir bókun uppgjörs veitir.

Ferlið og skrefin til að reikna út og bóka uppgjör í runu eru þau sömu og þau voru í eldri bókun uppgjörs. Hins vegar hafa verulegar endurbætur átt sér stað í kjarnastarfsemi á vinnslu uppgjaranna. Þessar endurbætur gera ferlið sterkara og veita betri sýnileika í upplýsingar um stöður og villur. Þess vegna geta notendur tekist á við orsök villanna og síðan haldið áfram með bókunarferlið án þess að gögnin skemmist og án þess að þurfa á lagfæringu gagna að halda.

Eftirfarandi kaflar lýsa nokkrum af helstu endurbótunum á eiginleikanum fyrir bókun uppgjörs sem birtast í notendaviðmótinu fyrir smásöluuppgjör og bókuð uppgjör.

### <a name="status-details"></a>Stöðuupplýsingar

Nýtt stöðulíkan hefur verið kynnt í reglubundinni bókun uppgjörs yfir ferli útreikninga og bókunar.

Eftirfarandi tafla lýsir hinum ýmsu stöðum og röð þeirra í útreikningsferlinu.

| Röðun á stöðu | Ríki      | lýsing |
|-------------|------------|-------------|
| 1           | Hafið    | Uppgjörið var búið til og er tilbúið til útreiknings. |
| 2           | Merkt     | Færslurnar sem falla undir uppgjörið eru auðkenndar á grundvelli færibreyta uppgjörs og þær eru merktar með auðkenni uppgjörs. |
| 3           | Reiknað | Uppgjörslínurnar eru reiknaðar og sýndar. |

Eftirfarandi tafla lýsir hinum ýmsu stöðum og röð þeirra í bókunarferlinu.

| Röðun á stöðu | Ríki                   | lýsing |
|-------------|-------------------------|-------------|
| 1           | Merkt                 | Margar villuleitir eru gerðar sem tengjast færibreytum (til dæmis ráðstöfunargjaldi) og uppgjöri og uppgjörslínum (til dæmis munurinn á milli talinnar upphæðar og færsluupphæðar). |
| 2           | Uppsafnað              | Sölufærslum fyrir nefnda og ónefnda viðskiptavini er safnað saman á grundvelli skilgreiningarinnar. Öllum uppsöfnuðum færslum er að lokum breytt í sölupöntun. |
| 3           | Pöntun viðskiptavinar stofnuð  | Sölupantanir eru stofnaðar í kerfinu á grundvelli uppsafnaðra færslna. |
| 4           | Pöntun viðskiptavinar reikningsfærð | Sölupantanir eru reikningsfærðar. |
| 5           | Bókaðir afslættir        | Færslubækur tímabundins afsláttar eru bókaðar á grundvelli skilgreiningarinnar. |
| 6           | Bókaðar tekjur/útgjöld   | Færslur tekja/gjalda eru bókaðar sem fylgiskjöl. |
| 7           | Fylgiskjöl tengd         | Greiðslubækur eru búnar til og tengdar samsvarandi reikningi. |
| 8           | Bókaðar greiðslur         | Greiðslubækur eru bókaðar. |
| 9           | Bókuð gjafakort       | Gjafakortsfærslur eru bókaðar sem fylgiskjöl. |
| 10          | Birt                  | Uppgjörið er merkt sem bókað. |

Sérhver staða í töflunni hér að framan er sjálfstæð í eðli sínu, og háð stigveldi er byggt á milli staðanna. Þessi háðu tengsl færast frá toppi til botns. Ef kerfið lendir í einhverjum villum meðan það vinnur með stöðu, er staða uppgjörsins fært aftur í fyrri stöðu. Allar síðari endurtekningar á ferlinum halda áfram frá þeirri stöðu sem mistókst og heldur áfram þaðan. Þessi aðferð hefur eftirfarandi kosti:

- Notandinn hefur fullan sýnileika á stöðunni þar sem villan átti sér stað.
- Komið er í veg fyrir skemmdir á gögnum. Til dæmis, í eiginleikanum fyrir bókun uppgjörs, voru tilvik þar sem sumar sölupantanir voru reikningsfærðar en aðrar skildar eftir opnar. Það voru líka tilvik þar sem sumar greiðslubækur höfðu ekki samsvarandi reikninga til að gera upp vegna þess að villa kom upp við bókun á reikningi.
- Notendur geta séð núverandi stöðu á uppgjöri með því að nota hnappinn **Upplýsingar um stöðu** í flokknum **Upplýsingar um framkvæmd** í uppgjöri. Upplýsingasíða stöðu hefur þrjá hluta:

    - Fyrsti hluti sýnir núverandi stöðu á uppgjöri ásamt villukóða og ítarlegum villuboðum ef villa kom upp.
    - Annar hluti sýnir ýmsar stöður á útreikningsferlinu. Sjónmerki gefa til kynna stöður sem hefur tekist að keyra, stöður sem ekki var hægt að keyra út af villum og stöður sem hafa ekki enn verið keyrðar.
    - Þriðja hluti sýnir ýmsar stöður á bókunarferlinu. Sjónmerki gefa til kynna stöður sem hefur tekist að keyra, stöður sem ekki var hægt að keyra út af villum og stöður sem hafa ekki enn verið keyrðar.

Að auki sýnir hausinn í öðrum og þriðja hluta heildarstöðu viðkomandi ferils.

### <a name="event-logs"></a>Tilvikaannálar

Uppgjör fer í gegnum ýmsar aðgerðir (til dæmis, stofna, reikna út, hreinsa og bóka) og hugsanlega verður kallað á mörg tilvik af sömu aðgerðinni á líftíma uppgjörsins. Til dæmis, eftir að uppgjör er stofnað og reiknað út getur notandi hreinsað uppgjörið og reiknað það út aftur. Hnappurinn **Tilvikaannáll** í **Upplýsingar um framkvæmd** flokki uppgjörsins veitir fulla endurskoðunarslóð af ýmsum aðgerðum sem var kallað á fyrir uppgjör, ásamt upplýsingum um hvenær var kallað eftir þessum aðgerðum.

### <a name="aggregated-transactions"></a>Uppsafnaðar færslur

Í bókunarferlinu er sölufærslunum safnað saman á grundvelli skilgreiningarinnar. Þessar uppsöfnuðu færslur eru geymdar í kerfinu og notaðar til að stofna sölupantanir. Sérhver uppsöfnuð færsla stofnar eina samsvarandi sölupöntun í kerfinu. Þú getur skoðað uppsafnaðar færslur með hnappnum **Uppsafnaðar færslur** í **Upplýsingar um framkvæmd** flokki uppgjörsins.

Flipinn **Upplýsingar um sölupöntun** á uppsafnaðri færslu sýnir eftirfarandi upplýsingar:

- **Færslukenni** - Kenni uppsöfnuðu færslunnar.
- **Uppgjörsnúmer** - Uppgjörið sem uppsafnaða færslan tilheyrir.
- **Dagsetning** - Dagsetningin þegar uppsafnaða færslan var stofnuð.
- **Sölukenni** - Sölupöntunarkennið þegar sölupöntun er stofnuð út frá uppsafnaðri færslu. Ef þessi reitur er auður hefur samsvarandi sölupöntun ekki verið stofnuð.
- **Fjöldi uppsafnaðra lína** - Heildarfjöldi lína fyrir uppsafnaða færslu og sölupöntun.
- **Staða** - Síðasti staða uppsöfnuðu færslunnar.
- **Reikningskenni** - Kenni sölureiknings þegar sölupöntun fyrir uppsafnaða færslu er stofnuð. Ef þessi reitur er auður hefur reikningurinn fyrir sölupöntunina ekki verið bókaður.

Flipinn **Færsluupplýsingar** á uppsafnaðri færslu sýnir allar smásölufærslur sem hafa verið dregnar inn í uppsafnaða færslu. Uppsafnaðar línur í uppsafnaðri færslu sýna allar uppsafnaðar skrár frá smásölufærslum. Uppsafnaðar línur sýna einnig upplýsingar eins og vöru, afbrigði, magn, verð, nettóupphæð, einingu og vöruhús. Í grundvallaratriðum samsvarar hver uppsöfnuð lína einni sölupöntunarlínu.

Frá síðunni **Uppsafnaðar færslur** er hægt að hlaða niður XML-skrá fyrir tiltekna uppsafnaða færslu með því að nota hnappinn **Flytja út XML-skrá sölupantana**. Þú getur notað XML-skrá til að kemba vandamál sem hafa með stofnun sölupantana og bókanir að gera. Sæktu einfaldlega XML-skrána, svo skaltu hlaða hana upp í prófunarumhverfi og kemba vandamálið í prófunarumhverfinu. Virknin til að hlaða niður XML-skránni fyrir uppsafnaða færslu er ekki í boði fyrir uppgjör sem hafa verið bókuð.

Yfirlit uppsafnaðrar færslu veitir eftirfarandi kosti:

- Notandinn hefur sýnileika í uppsafnaðar færslur sem mistókust við stofnun sölupöntunar og sölupantanir sem mistókust við reikningsfærslu.
- Notandinn hefur sýnileika í hvernig færslum er safnað saman.
- Notandinn hefur fulla endurskoðunarslóð, frá smásölufærslum, til sölupantana, til sölureikninga. Þessi endurskoðunarslóð var ekki tiltæk í eldri eiginleikanum fyrir bókun uppgjörs.
- Uppsafnaðar XML-skrá gera það auðveldara að bera kennsl á vandamál við stofnun sölupöntunar og reikningsfærslu.

### <a name="journal-vouchers"></a>Færslubókarfylgiskjöl

Hnappurinn **Færslubókarfylgiskjöl** í **Upplýsingar um framkvæmd** flokki uppgjörs sýnir hinar ýmsu fylgiskjalafærslur sem eru stofnaðar fyrir uppgjör og sem tengjast afsláttum, tekju-/gjaldareikningum, gjafakortum og svo framvegis.

Eins og er sýnir forritið aðeins þessar upplýsingar fyrir bókuð uppgjör.

### <a name="payment-journals"></a>Greiðslubækur

Hnappurinn **Greiðslubækur** í **Upplýsingar um framkvæmd** flokki uppgjörs sýnir hinar ýmsu greiðslubækur sem eru stofnaðar fyrir uppgjör.

Eins og er sýnir forritið aðeins þessar upplýsingar fyrir bókuð uppgjör.

## <a name="other-improvements"></a>Aðrar endurbætur

Aðrar endurbætur sem notendur geta séð hafa verið gerðar á eiginleikanum fyrir bókun uppgjörs. Hér eru nokkur dæmi:

- Uppsöfnunin tekur ekki tillit til eininga starfsmanna, afgreiðslustöðvar og vaktar. Vegna þess að það eru færri uppsafnaðar færibreytur þarf að vinna úr færri sölupöntunarlínum.
- Dregið er úr sjálfheldutilvikum á töflum smásölufærslu með því að kynna aukalega viðbótartöflu og með því að gera innsetningaraðgerðir í stað uppfærsluaðgerða á töflum smásölufærslu.
- Fjöldi runuverka í gangi hefur verið settur í færibreytur og takmarkaður. Þess vegna má fínstilla þessa tölu sérstaklega fyrir umhverfi viðskiptavinarins. Í eldri eiginleika fyrir bókun uppgjörs var stofnaður ótakmarkaður fjöldi runuverka á sama tíma. Niðurstöðurnar voru óviðráðanlegt álag, kostnaður og flöskuhálsar á runuþjóninum.
- Uppgjör eru sett í biðröð fyrir úrvinnslu með skilvirkni að leiðarljósi þannig að uppgjör sem hafa flestar færslur fá forgang.
- Runuvinnslur eins og **Reikna út uppgjör í runu** og **Bóka uppgjör í runu** eru eingöngu keyrðar í runustillingu. Í eldri eiginleikanum fyrir bókun uppgjörs gátu notendur valið að keyra þessar runuvinnslur í gagnvirkri stillingu sem er einþráða aðgerð ólíkt runuvinnslum sem eru margþráða.
- Í eldri eiginleikanum fyrir bókun uppgjörs setti sérhver bilun á runuverki alla runuvinnsluna í villustöðu. Í endurbætta eiginleikanum leiða bilanir á runuverki ekki til þess að runuvinnsla fari í villustöðu ef önnur runuverk klárast. Þú ættir að meta bókunarstöðuna fyrir runuframkvæmd með því að nota síðuna **Uppgjör smásölu** þar sem þú getur séð allar þær yfirlýsingar sem ekki voru bókaðar vegna villna.
- Í eldri eiginleikanum fyrir bókun uppgjörs leiðir fyrsta tilvik á bilun á uppgjöri til þess að öll runan mistakist. Ekki er unnið úr uppgjörum sem eftir eru. Í endurbætta eiginleikanum heldur runuvinnslan áfram vinna úr öllum uppgjörum, jafnvel þó að sum uppgjörin mistakist. Einn kostur er að notendur fá innsýn í nákvæman fjölda uppgjara sem hafa villur. Þess vegna þurfa notendur ekki að vera fastir í endurtekinni lykkju þar sem villur eru lagaðar og bókun uppgjörsferlis er keyrt þar til öll uppgjör hafa verið bókuð.

## <a name="general-guidance-about-the-statement-posting-process"></a>Almennar leiðbeiningar um bókunarferli uppgjörs

- Við mælum með því að þú keyrir bókunarferli uppgjörs í runu vegna þess að runukeyrslur nýta sér styrkleika runurammans hvað varðar margþræðingu. Margþræðing er nauðsynleg tili þess að takast á við gríðarmikið magn færslna sem venjulega koma fyrir í bókunum uppgjörs.
- Við mælum með því að þú kveikir á neikvæðum efnislegum birgðum í vörulíkanaflokknum, þannig að þú fáir hnökralausa upplifun. Í sumum tilfellum gæti ekki verið hægt að bóka neikvæð uppgjör nema það séu neikvæðar efnislegar birgðir. Til dæmis, ef aðeins er til ein eining af vöru í birgðum og það hefur átt sér stað sölufærsla og skilafærsla fyrir vöruna, þá ætti að vera hægt að bóka færsluna jafnvel þótt ekki sé kveikt á neikvæðum birgðum. Hins vegar, vegna þess að bókunarferli uppgjörs dregur bæði sölufærslu og skilafærslu inn í staka viðskiptamannapöntun, er engin trygging fyrir því að sölulínan verði bókuð fyrst og skilalínan í kjölfarið. Þess vegna geta villur komið upp. Ef kveikt er á neikvæðum birgðum í þessari atburðarás verður bókun færslunnar ekki fyrir neikvæðum áhrifum og kerfið mun endurspegla birgðirnar á réttan hátt.
- Við mælum með að þú notir uppsöfnun á meðan þú reiknar út og bókar uppgjör. Þess vegna er mælt með eftirfarandi stillingum fyrir sumar af uppsöfnuðu færibreytunum:

    - Farðu í **Smásala** \> **Uppsetning höfuðstöðva** \> **Færibreytur** \> **Smásölufæribreytur**. Síðan á flipanum **Bókun**, á flýtiflipanum **Birgðauppfærsla**, í reitnum **Upplýsingastig** skal velja **Samantekt**.
    - Farðu í **Smásala** \> **Uppsetning höfuðstöðva** \> **Færibreytur** \> **Smásölufæribreytur**. Síðan á flipanum **Bókun**, á flýtiflipanum **Uppsöfnun** skal stilla valkostinn **Fylgiskjalafærslur** á **Já**.

