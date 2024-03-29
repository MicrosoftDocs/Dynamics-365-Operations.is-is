---
title: Endurbætur á virkni uppgjörsbókunar
description: Þessi grein lýsir endurbótum sem hafa verið gerðar á aðgerðinni til að birta yfirlýsingar.
author: analpert
ms.date: 05/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2018-04-30
ms.openlocfilehash: 33b4f17cd46338b62bed96f0a285e7b9634cc87a
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067820"
---
# <a name="improvements-to-statement-posting-functionality"></a>Endurbætur á virkni uppgjörsbókunar

[!include [banner](includes/banner.md)]

Þessi grein lýsir fyrsta settinu af endurbótum sem hafa verið gerðar á færslueiginleika yfirlýsingar. Þessar endurbætur eru fáanlegar í Microsoft Dynamics 365 Fjármál 7.3.2.

## <a name="activation"></a>Virkjun

Sjálfgefið er, við uppsetningu á fjármálum og rekstri 7.3.2, forritið er sett upp til að nota eldri eiginleikann fyrir yfirlitsfærslur. Til að virkja endurbættan eiginleika á bókun uppgjörs verður þú að kveikja á skilgreiningarlyklinum fyrir hann.

- Farðu í **Kerfisstjórnun** \> **Uppsetning** \> **Leyfisskilgreinin** og síðan undir hnútnum **Retail og Commerce** skal hreinsa gátreitinn **Yfirlit (eldra)** og velja gátreitinn **Yfirlit**.

Þegar kveikt er á nýja skilgreiningarlyklinum fyrir **Yfirlit** er nýtt valmyndaratriði sem heitir **Yfirlit** tiltækt. Þetta valmyndaratriði gerir þér kleift að búa til handvirkt, reikna og bóka uppgjör. Öll uppgjör sem valda villu þegar runubókunarferlið er notað verða einnig tiltæk í gegnum þetta valmyndaratriði. (Þegar kveikt er á skilgreiningarlyklinum fyrir **Yfirlit (eldra)** er valmyndaratriðið kallað **Opin yfirlit**.)

Commerce felur í sér eftirfarandi staðfestingar sem tengjast þessum skilgreiningarlyklum:

- Ekki er hægt að kveikja á báðum skilgreiningarlyklunum á sama tíma.
- Það verður að nota sömu skilgreiningarlyklana fyrir allar þær aðgerðir sem eru framkvæmdar á tilteknu uppgjöri á meðan á líftíma þess stendur (stofna, reikna út, hreinsa, bóka, o.s.frv.). Til dæmis getur þú ekki búið til og reiknað út uppgjör á meðan kveikt er á skilgreiningarlyklinum fyrir **Yfirlit (eldra)** og síðan reyna að bóka sama uppgjör á meðan kveikt er á skilgreiningarlyklinum fyrir **Yfirlit**.

> [!NOTE]
> Við mælum með því að þú notir skilgreiningarlykilinn fyrir **Yfirlit** fyrir endurbættan eiginleika á bókun uppgjörs, nema þú hafir góðar ástæður fyrir því að nota í staðinn skilgreiningarlykilinn fyrir **Yfirlit (eldra)**. Microsoft mun halda áfram að fjárfesta í nýjum og bættum eiginleika fyrir bókun uppgjörs og það er mikilvægt að þú skiptir yfir í hann eins fljótt og auðið er til að njóta góðs af honum. Eiginleikinn fyrir bókun á eldra uppgjöri er úreltur frá og með útgáfu 8.0.

## <a name="setup"></a>Setja upp

Sem hluti af endurbótum á eiginleikanum fyrir bókun uppgjörs hafa þrjár nýjar færibreytur verið kynntar til sögunnar á flýtiflipanum **Uppgjör** á flipanum **Bókun** á síðunni **Færibreytur Commerce**:

- **Slökkva á hreinsun upppgjörs** - Þessi valkostur er aðeins tiltækur í eldri eiginleika á bókun uppgjörs. Við mælum með að þú stillir þennan valkost á **Nei** til að koma í veg fyrir að notendur hreinsi uppgjör sem eru í hálfbókaðri stöðu. Ef yfirlýsingar, sem eru í hálfbókaðri stöðu, eru hreinsaðar skemmast gögn. Þú ættir að stilla þennan valkost á **Já** aðeins í undantekningartilvikum.
- **Frátekning birgða við útreikning** - Við mælum með því að þú notir runuvinnsluna **Bóka birgðir** fyrir birgðafrátekningu og að þú stillir þennan valkost á **Nei**. Þegar þessi valkostur er stilltur á **Nei** reynir endurbætti eiginleikinn á bókun uppgjörs ekki að búa til færslur birgðafrátekningar á meðan á útreikning stendur (ef færslur voru ekki þegar búnar til í gegnum runuvinnsluna **Bóka birgðir**). Í staðinn býr eiginleikinn til færslur birgðafrátekningar aðeins þegar bókun á sér stað. Þessi framkvæmd var hönnunarval og byggðist á þeirri staðreynd að tímaglugginn á milli útreikningsferlis og bókunarferlis er yfirleitt lítill. Ef þú vilt hins vegar taka frá birgðir á meðan á útreikningi stendur getur þú stillt þennan valkost á **Já**.

    Eldri eiginleikinn fyrir bókun uppgjörs tekur alltaf frá birgðir á meðan á útreikningsferli uppgjörs stendur yfir (ef frátekning var ekki þegar gerð í gegnum runuvinnsluna **Bóka birgðir**), án tillits til stillingar á þessum valkosti.

- **Gera þarf talningu óvirka** - Þegar þessi valkostur er stilltur á **Já** heldur bókunarferli á uppgjöri áfram, jafnvel þótt mismunurinn á talinni upphæð og færsluupphæð í uppgjörinu sé utan markanna sem eru skilgreind í flýtiflipanum **Uppgjör** fyrir verslanir.

> [!NOTE]
> Frá og með útgáfu Commerce útgáfu 10.0.14, þegar **Smásöluyfirlit - Trickle feed** eiginleiki er virkur, the **Settu inn birgðahald** runuvinna á ekki lengur við og ekki hægt að keyra hana.

## <a name="processing"></a>Í vinnslu

Hægt er að reikna út og bóka uppgjör í lotu með valmyndaratriðinu **Útreikningur uppgjörs í runu** og **Bóka uppgjör í runu**. Að öðrum kosti er hægt að reikna út og bóka uppgjör handvirkt með valmyndaratriðinu **Yfirlit** sem endurbætti eiginleikinn fyrir bókun uppgjörs veitir.

Ferlið og skrefin til að reikna út og bóka uppgjör í runu eru þau sömu og þau voru í eldri bókun uppgjörs. Hins vegar hafa verulegar endurbætur átt sér stað í kjarnastarfsemi á vinnslu uppgjaranna. Þessar endurbætur gera ferlið sterkara og veita betri sýnileika í upplýsingar um stöður og villur. Þess vegna geta notendur tekist á við orsök villanna og síðan haldið áfram með bókunarferlið án þess að gögnin skemmist og án þess að þurfa á lagfæringu gagna að halda.

Eftirfarandi kaflar lýsa nokkrum af helstu endurbótunum á eiginleikanum fyrir bókun uppgjörs sem birtast í notendaviðmótinu fyrir yfirlit og bókuð uppgjör.

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

Meðan á bókunarferlinu stendur eru staðgreiðslufærslur teknar saman eftir viðskiptavinum og vöru. Þess vegna er fjöldi sölupantana og lína sem eru búnar til minnkaðar. Safnaðar færslur eru geymdar í kerfinu og notaðar til að búa til sölupantanir. Sérhver uppsöfnuð færsla stofnar eina samsvarandi sölupöntun í kerfinu. 

Ef yfirlit er ekki að fullu bókað er hægt að skoða samanlagðar færslur í yfirlitinu. Á aðgerðarrúðunni, á **Yfirlýsing** flipa, í **Upplýsingar um framkvæmd** hópur, veldu **Samanlögð viðskipti**.

![Hnappur fyrir samansafnaðar færslur fyrir yfirlit sem er ekki að fullu bókað.](media/aggregated-transactions.png)

Fyrir bókaðar yfirlit er hægt að skoða samanlagðar færslur á **Settar yfirlýsingar** síðu. Á aðgerðarrúðunni velurðu **Fyrirspurnir**, og veldu síðan **Samanlögð viðskipti**.

![Skipun um samansafnaðar færslur fyrir bókaðar yfirlit.](media/aggregated-transactions-posted-statements.png)

The **Upplýsingar um sölupöntun** Flýtiflipi uppsafnaðrar færslu sýnir eftirfarandi upplýsingar:

- **Færslukenni** - Kenni uppsöfnuðu færslunnar.
- **Uppgjörsnúmer** - Uppgjörið sem uppsafnaða færslan tilheyrir.
- **Dagsetning** - Dagsetningin þegar uppsafnaða færslan var stofnuð.
- **Sölukenni** - Sölupöntunarkennið þegar sölupöntun er stofnuð út frá uppsafnaðri færslu. Ef þessi reitur er auður hefur samsvarandi sölupöntun ekki verið stofnuð.
- **Fjöldi uppsafnaðra lína** - Heildarfjöldi lína fyrir uppsafnaða færslu og sölupöntun.
- **Staða** - Síðasti staða uppsöfnuðu færslunnar.
- **Reikningskenni** - Kenni sölureiknings þegar sölupöntun fyrir uppsafnaða færslu er stofnuð. Ef þessi reitur er auður hefur reikningurinn fyrir sölupöntunina ekki verið bókaður.
- **Villumelding** – Þessi reitur er stilltur ef samsöfnunin er í villuástandi.
- **Villu skilaboð** – Þessi reitur er stilltur ef samsöfnunin er í villuástandi. Það sýnir upplýsingar um hvað olli því að ferlið mistókst. Þú getur notað upplýsingarnar í villukóðanum til að laga málið og síðan endurræsa ferlið handvirkt. Það fer eftir tegund upplausnar, gæti þurft að eyða uppsöfnuðum sölu og vinna úr henni á nýrri yfirlýsingu.

![Reitir á flýtiflipanum Sölupöntunarupplýsingar fyrir uppsafnaða færslu.](media/aggregated-transactions-error-message-view.png)

The **Upplýsingar um viðskipti** Flýtiflipi uppsafnaðrar færslu sýnir allar færslur sem hafa verið dregnar inn í samansafnaða færslu. Uppsafnaðar línur í uppsafnaðri færslu sýna allar uppsafnaðar skrár frá færslum. Uppsafnaðar línur sýna einnig upplýsingar eins og vöru, afbrigði, magn, verð, nettóupphæð, einingu og vöruhús. Í grundvallaratriðum samsvarar hver uppsöfnuð lína einni sölupöntunarlínu.

![Færsluupplýsingar flýtiflipi uppsafnaðrar færslu.](media/aggregated-transactions-sales-details.png)

Í sumum tilfellum gætu uppsafnaðar færslur mistekst að bóka samantekna sölupöntun þeirra. Í þessum aðstæðum verður villukóði tengdur yfirlýsingastöðunni. Til að skoða aðeins uppsafnaðar færslur sem innihalda villur geturðu virkjað **Sýndu aðeins mistök** sía í uppsafnaðar færsluskjánum með því að velja gátreitinn. Með því að virkja þessa síu takmarkar þú niðurstöðurnar við samanlagðar færslur sem hafa villur sem krefjast úrlausnar. Fyrir upplýsingar um hvernig á að laga þessar villur, sjá [Breyta og endurskoða netpöntun og ósamstilltar pöntunarfærslur viðskiptavina](edit-order-trans.md).

![Gátreitur fyrir síuna Sýna aðeins bilanir í uppsafnaðar færsluskjánum.](media/aggregated-transactions-failure-view.png)

Á **Samanlögð viðskipti** síðu geturðu hlaðið niður XML fyrir tiltekna uppsafnaða færslu með því að velja **Flytja út safngögn**. Þú getur skoðað XML í hvaða XML sniði sem er til að sjá raunverulegar upplýsingar um gögn sem fela í sér stofnun og bókun sölupöntunar. Virknin til að hlaða niður XML-skránni fyrir uppsafnaða færslu er ekki í boði fyrir uppgjör sem hafa verið bókuð.

![Hnappurinn Flytja út samansafn gagna á síðunni Safnaðar færslur.](media/aggregated-transactions-export.png)

Ef þú getur ekki lagað villuna með því að leiðrétta gögn á sölupöntuninni eða gögnum sem styðja sölupöntunina, **Eyða pöntun viðskiptavina** hnappur er í boði. Til að eyða pöntun velurðu samansafnaða færsluna sem mistókst og veldu síðan **Eyða pöntun viðskiptavina**. Bæði samanlagðri færslu og samsvarandi sölupöntun verður eytt. Þú getur nú skoðað færslurnar með því að nota breytinga- og endurskoðunaraðgerðina. Að öðrum kosti er hægt að endurvinna þau með nýrri yfirlýsingu. Eftir að allar bilanir hafa verið lagfærðar er hægt að halda áfram færslu yfirlits með því að keyra post statement fallið fyrir viðkomandi yfirlit.

![Eyða pöntunarhnappi viðskiptavinar í uppsafnaðar færsluskjánum.](media/aggregated-transactions-delete-cust-order.png)

Uppsöfnuð færsluyfirlit veitir eftirfarandi kosti:

- Notandinn hefur sýnileika í uppsafnaðar færslur sem mistókust við stofnun sölupöntunar og sölupantanir sem mistókust við reikningsfærslu.
- Notandinn hefur sýnileika í hvernig færslum er safnað saman.
- Notandinn hefur fulla endurskoðunarslóð, frá færslum, til sölupantana, til sölureikninga. Þessi endurskoðunarslóð var ekki tiltæk í eldri eiginleikanum fyrir bókun uppgjörs.
- Samanlögð XML skrá gerir það auðveldara að bera kennsl á vandamál við stofnun sölupöntunar og reikningagerð.

> [!NOTE]
> Þegar færslur eru teknar saman er starfsmaðurinn sem úthlutað er færslunni ekki lengur tiltækur fyrir **Helstu söluskýrsla starfsmanna**, sem þýðir að **Helstu söluskýrsla starfsmanna** mun ekki sýna allar færslur. Við mælum með að þú notir ekki **Helstu söluskýrsla starfsmanna** með samanlögðum viðskiptum.

### <a name="journal-vouchers"></a>Færslubókarfylgiskjöl

Hnappurinn **Færslubókarfylgiskjöl** í **Upplýsingar um framkvæmd** flokki uppgjörs sýnir hinar ýmsu fylgiskjalafærslur sem eru stofnaðar fyrir uppgjör og sem tengjast afsláttum, tekju-/gjaldareikningum, gjafakortum og svo framvegis.

Eins og er sýnir forritið aðeins þessar upplýsingar fyrir bókuð uppgjör.

### <a name="payment-journals"></a>Greiðslubækur

Hnappurinn **Greiðslubækur** í **Upplýsingar um framkvæmd** flokki uppgjörs sýnir hinar ýmsu greiðslubækur sem eru stofnaðar fyrir uppgjör.

Eins og er sýnir forritið aðeins þessar upplýsingar fyrir bókuð uppgjör.

## <a name="other-improvements"></a>Aðrar endurbætur

Aðrar endurbætur sem notendur geta séð hafa verið gerðar á eiginleikanum fyrir bókun uppgjörs. Hér eru nokkur dæmi:

- Uppsöfnunin tekur ekki tillit til eininga starfsmanna, afgreiðslustöðvar og vaktar. Vegna þess að það eru færri uppsafnaðar færibreytur þarf að vinna úr færri sölupöntunarlínum.
- Dregið er úr sjálfheldutilvikum á töflum færslu með því að kynna aukalega viðbótartöflu og með því að gera innsetningaraðgerðir í stað uppfærsluaðgerða á töflum færslu.
- Fjöldi runuverka í gangi hefur verið settur í færibreytur og takmarkaður. Þess vegna má fínstilla þessa tölu sérstaklega fyrir umhverfi viðskiptavinarins. Í eldri eiginleika fyrir bókun uppgjörs var stofnaður ótakmarkaður fjöldi runuverka á sama tíma. Niðurstöðurnar voru óviðráðanlegt álag, kostnaður og flöskuhálsar á runuþjóninum.
- Uppgjör eru sett í biðröð fyrir úrvinnslu með skilvirkni að leiðarljósi þannig að uppgjör sem hafa flestar færslur fá forgang.
- Runuvinnslur eins og **Reikna út uppgjör í runu** og **Bóka uppgjör í runu** eru eingöngu keyrðar í runustillingu. Í eldri eiginleikanum fyrir bókun uppgjörs gátu notendur valið að keyra þessar runuvinnslur í gagnvirkri stillingu sem er einþráða aðgerð ólíkt runuvinnslum sem eru margþráða.
- Í eldri eiginleikanum fyrir bókun uppgjörs setti sérhver bilun á runuverki alla runuvinnsluna í villustöðu. Í endurbætta eiginleikanum leiða bilanir á runuverki ekki til þess að runuvinnsla fari í villustöðu ef önnur runuverk klárast. Þú ættir að meta bókunarstöðuna fyrir runuframkvæmd með því að nota síðuna **Yfirlit** þar sem þú getur séð allar þær yfirlýsingar sem ekki voru bókaðar vegna villna.
- Í eldri eiginleikanum fyrir bókun uppgjörs leiðir fyrsta tilvik á bilun á uppgjöri til þess að öll runan mistakist. Ekki er unnið úr uppgjörum sem eftir eru. Í endurbætta eiginleikanum heldur runuvinnslan áfram vinna úr öllum uppgjörum, jafnvel þó að sum uppgjörin mistakist. Einn kostur er að notendur fá innsýn í nákvæman fjölda uppgjara sem hafa villur. Þess vegna þurfa notendur ekki að vera fastir í endurtekinni lykkju þar sem villur eru lagaðar og bókun uppgjörsferlis er keyrt þar til öll uppgjör hafa verið bókuð.

## <a name="general-guidance-about-the-statement-posting-process"></a>Almennar leiðbeiningar um bókunarferli uppgjörs

- Við mælum með því að þú keyrir bókunarferli uppgjörs í runu vegna þess að runukeyrslur nýta sér styrkleika runurammans hvað varðar margþræðingu. Margþræðing er nauðsynleg tili þess að takast á við gríðarmikið magn færslna sem venjulega koma fyrir í bókunum uppgjörs.
- Við mælum með því að þú kveikir á neikvæðum efnislegum birgðum í vörulíkanaflokknum, þannig að þú fáir hnökralausa upplifun. Í sumum tilfellum gæti ekki verið hægt að bóka neikvæð uppgjör nema það séu neikvæðar efnislegar birgðir. Til dæmis, ef aðeins er til ein eining af vöru í birgðum og það hefur átt sér stað sölufærsla og skilafærsla fyrir vöruna, þá ætti að vera hægt að bóka færsluna jafnvel þótt ekki sé kveikt á neikvæðum birgðum. Hins vegar, vegna þess að bókunarferli uppgjörs dregur bæði sölufærslu og skilafærslu inn í staka viðskiptamannapöntun, er engin trygging fyrir því að sölulínan verði bókuð fyrst og skilalínan í kjölfarið. Þess vegna geta villur komið upp. Ef kveikt er á neikvæðum birgðum í þessari atburðarás verður bókun færslunnar ekki fyrir neikvæðum áhrifum og kerfið mun endurspegla birgðirnar á réttan hátt.
- Við mælum með að þú notir uppsöfnun á meðan þú reiknar út og bókar uppgjör. Þess vegna er mælt með eftirfarandi stillingum fyrir sumar af uppsöfnuðu færibreytunum:

    - Opnið **Retail og Commerce** \> **Uppsetning höfuðstöðva** \> **Færibreytur** \> **Færibreytur Commerce**. Síðan á flipanum **Bókun**, á flýtiflipanum **Birgðauppfærsla**, í reitnum **Upplýsingastig** skal velja **Samantekt**.
    - Opnið **Retail og Commerce** \> **Uppsetning höfuðstöðva** \> **Færibreytur** \> **Færibreytur Commerce**. Síðan á flipanum **Bókun**, á flýtiflipanum **Uppsöfnun** skal stilla valkostinn **Fylgiskjalafærslur** á **Já**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

