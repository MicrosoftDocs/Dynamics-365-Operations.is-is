---
title: Eiginleikar hnitanets
description: Þessi grein lýsir nokkrum kröftugum eiginleikum netstýringar. Virkja þarf nýjan eiginleika hnitanetsins til að hafa aðgang að þessum möguleikum.
author: jasongre
ms.date: 08/29/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 096f441d39dde0f322ed117ab35a6a4641a38a93
ms.sourcegitcommit: 1d5cebea3e05b6d758cd01225ae7f566e05698d2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/02/2022
ms.locfileid: "9405466"
---
# <a name="grid-capabilities"></a>Eiginleikar hnitanets

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Nýja netstýringin veitir fjölda gagnlegra og öflugra eiginleika sem hægt er að nota til að auka framleiðni notenda, smíða áhugaverðari sýn á gögnin þín og fá þroskandi innsýn í gögnin þín. Þessi grein mun fjalla um eftirfarandi getu: 

- Sýnir reiknuð gildi 
- Vélritun á undan kerfinu
- Mat á stærðfræðisegðum 
- Flokkun töflugagna (virkjuð sérstaklega með því að nota eiginleikann **Flokkun í hnitanetum**)
- Festa dálka (virkjað á aðskilinn hátt með því að nota eiginleikann **Festa dálka í hnitanetum**)
- Aðlaga dálkbreidd sjálfkrafa
- Teygjanlegir dálkar

## <a name="showing-calculated-values"></a>Sýnir reiknuð gildi
Í forritum fjármála- og reksturs geta notendur skoðað reiknað gildi fyrir hvern talnadálk í hnitaneti. Neðanmálshluti neðst í hnitanetinu sýnir þessi útreiknuðu gildi.

[![Sýnir reiknuð gildi í hnitanetum.](./media/grids-aggregation.png)](./media/grids-aggregation.png)

Í eldri útgáfum en 10.0.29 er samtala eina studda reiknaða gildið. Hins vegar, frá og með útgáfu 10.0.29, eftir að notendur virkja eiginleikann **Auknir möguleikar í uppsöfnun hnitanets** geta þeir valið úr eftirfarandi fjórum reiknuðum gildum:

- Lágmark
- Hámark
- Samtals
- Meðaltal

Einn dálkur getur aðeins sýnt eina gerð af reiknuðu gildi. Hins vegar er hægt að stilla hvern dálk í grindinni þannig að hann sýni mismunandi gerð af reiknuðu gildi.

### <a name="showing-the-grid-footer"></a>Sýni síðufót hnitanetsins
Það er neðanmálssvæði neðst í hverju töflukerfi í forritum fjármála- og reksturs. Neðanmálið getur sýnt mikilvægar upplýsingar sem tengjast gögnum sem birtast í reitunum. Hér eru nokkur dæmi um þessar upplýsingar:

- Fjöldi valdra lína í töflunni (þegar fleiri en ein skrá er valin)
- Reiknuð gildi neðst í samstilltu töludálkunum (t.d. samtölur)
- Fjöldi raða í gagnasafninu 

Þessi síðufótur er sjálfgefið falinn en hægt er að kveikja á honum. Til að sýna síðufót fyrir hnitanet skal velja hnappinn **Valkostir hnitanets** í haus hnitanetsins og síðan velja valkostinn **Sýna síðufót**. Eftir að kveikt er á síðufætinum fyrir tiltekið hnitanet verður stillingin geymd í minni þar til notandinn kýs að fela síðufótinn. Til að fela síðufótinn skal velja **Fela síðufót** á valmyndinni **Valkostir hnitanets**.

### <a name="specifying-columns-with-calculated-values"></a>Tilgreina dálka með reiknuðum gildum
Sem stendur sýna engir dálkar sjálfgefið reiknuð gildi. Í staðinn er uppsetningin talin aðgerð sem er framkvæmd einu sinni, eins og að breyta breidd dálka í hnitanetum. Þegar þú hefur tilgreint að þú viljir sjá reiknað gildi fyrir dálk, verður munað eftir stillingunni þegar þú heimsækir síðuna næst.

Það eru tvær leiðir til að stilla dálk til að sýna útreiknað gildi

- Í dálkinum sem á að skoða reiknað gildi fyrir skaltu velja og halda inni (eða hægrismella). Ef búið er að virkja eiginleikann **Auknir möguleikar í uppsöfnun hnitanets** skal velja **Sýna samtölur dálka** og velja síðan reiknað gildi sem óskað er eftir. Ef sá eiginleiki er ekki virkur skaltu velja **Samtala þessa dálks**. Þessi aðgerð veldur því að þrír atburðir eiga sér stað:

    1. Síðufótur hnitanetsins verður sýnilegur. 
    2. Stilling þín til að skoða reiknað gildi fyrir dálkinn er vistuð. 
    3. Útreikningurinn sem óskað er eftir er hafinn fyrir þennan dálk og alla aðra dálka sem þú hefur áður stillt til að sjá reiknað gildi fyrir. Tíminn sem þarf til að sýna reiknuð gildi fer eftir stærð gagnasafnsins.

- Þegar fóturinn er sýnilegur velurðu **Sýna samtölu** (eða **Velja reiknað gildi** ef eiginleikinn **Auknir möguleikar í uppsöfnun hnitanets** er virkur) á svæði fótar neðst í dálkinum þar sem á að skoða reiknað gildi fyrir. Ef það eru engar stilltir dálkar verður sá hnappur tiltækur fyrir alla töludálka.

    Þegar að minnsta kosti einn dálkur er stilltur til að birta reiknað gildi verður hnappurinn **Sýna samtölu** (eða hnappurinn **Velja reiknað gildi**) þegar haldið er yfir eða í fókus. Aðgerðin við að velja hnappinn vistar einungis stillingu þína um að sjá reiknað gildi í dálkinum, þannig að stillingin er notuð þegar síðan er opnuð síðar. Í neðanmálinu er þessi staða gefin til kynna með bandstriki sem birtist í dálkinum. (Athugaðu að reiknað gildi birtist strax ef gagnasafnið er nógu lítið).

Ef þú gerir mistök og vilt ekki lengur skoða reiknað gildi í tilteknum dálki skaltu velja og halda inni (eða hægrismella) í dálkinum og velja svo **Fela samtölu** (eða **Skoða samtölur dálks \> Ekkert** ef eiginleikinn **Auknir möguleikar í uppsöfnun hnitanets** er virkjaður). Einnig getur þú valið **Fela samtölu** (eða **Fela reiknað gildi**) í fæti umrædds dálks. Þessi valkostur verður einnig vistaður fyrir framtíðarheimsóknir á síðunni. 

### <a name="calculating-aggregate-values"></a>Reiknar samanlögð gildi
Þegar þú ferð á síðu þar sem fótur er sýnilegur og dálkar eru þegar stilltir til að sýna reiknuð gildi er ekki víst að þau gildi séu sýnd í fætinum. Hegðunin fer eftir stærð gagnasafnsins á síðunni. Ef gagnasafnið er nægjanlega lítill, birtast reiknuð gildi sjálfkrafa ásamt fjölda lína í gagnasafninu. Ef það eru bandstrik í fót undir dálkunum sem þú stilltir, þá er gagnasafnið of stórt til að kerfið geti sýnt reiknaðar tölur strax. Í þessu tilviki þarf að grípa til sérstakra aðgerða til að reikna gildin. Til að reikna út gildin skaltu velja hnappinn **Reikna** í fætinum. Einnig getur þú valið og haldið inni (eða hægrismellt) dálki sem þú vilt skoða heildarupphæðina fyrir og síðan valið **Samtala þessa dálks** (eða **Skoða samtölur dálks** og síðan reiknaða gildið sem óskað er eftir ef eiginleikinn **Auknir möguleikar í uppsöfnun hnitanets** er virkjaður).

Þú getur hætt við aðgerðina hvenær sem er með því að velja **Hætta við** ef útreikningurinn tekur langan tíma. Stundum verður gagnasafnið of stórt til að reikna samanlögð gildi (mörk sem eru ákvörðuð af fyrirtækinu þínu). Í því tilviki færðu þess í stað tilkynningu um að sía gögnin þín betur.

> [!NOTE]
> Kerfisstjórar geta breytt hámarksfjölda skráa sem eru tiltækar til að reikna samanlögð gildi með því að breyta færibreytunni **Hámarksfjöldi staðbundinna færsla fyrir hvert hnitanet** á síðunni **Valkostir afkastagetu biðlara**. Sjálfgefið gildi er 25.000 færslur. Stjórnendur ættu að gæta varúðar þegar þeir stilla þetta gildi, vegna þess að gildi sem er of stórt getur fyllt allt tiltækt minni í tölvu notandans. Mælt er með því að gildið sé ekki stærra en 50.000 færslur.

Reiknuð gildi munu uppfærast sjálfkrafa þegar þú uppfærir, eyðir eða býrð til línur í gagnasafninu.

## <a name="typing-ahead-of-the-system"></a>Vélritun á undan kerfinu
Í mörgum atburðarásum í viðskiptum er möguleikinn til að færa gögn fljótt inn í kerfið mjög mikilvægur. Áður en nýja hnitanetsstýringin var kynnt gátu notendur aðeins breytt gögnum í núverandi línu. Eftir að breytingarnar voru gerðar í línu gátu notendur því ekki skipt yfir í aðra línu eða búið til nýja línu fyrr en kerfið hafði staðfest breytingarnar í núverandi línu og (og í tilvikum þegar lína var stofnuð) keyrði öll rök sem eru tengd stofnun nýrrar línu. Til að reyna að draga úr þeim tíma sem notendur bíða eftir að þessum aðgerðum ljúki, og til að bæta afköst notanda, aðlagar nýja hnitanetið þessar aðgerðir svo þær séu ósamstilltar. Þess vegna getur notandinn fært sig yfir í aðrar línur til að gera breytingar á meðan beðið er eftir fyrri staðfestingum á línum og rök stofnunar línu eru í bið. 

[![Innsláttur á undan kerfinu](./media/gridFastEntry-07-25-2022.gif)](./media/gridFastEntry-07-25-2022.gif)

Til að styðja við þessa nýju hegðun hefur nýjum dálki fyrir línustöðuna verið bætt við hægra megin við dálk línuvals þegar hnitanetið er í breytingastillingu. Þessari dálkur sýnir eina af eftirfarandi stöðum:

- **Autt** - Engin stöðumynd gefur til kynna að kerfið hafi náð að vista línuna.
- **Vinnsla í bið** - Þessi staða gefur til kynna að netþjónninn hafi enn ekki vistað breytingar í línunni en að þær séu í biðröð breytinga sem þarf að vinna úr. Áður en gripið er til aðgerða utan hnitanetsins þarf að bíða eftir að unnið er úr öllum breytingum. Að auki er textinn í þessum línum skáletraður til að gefa til kynna óvistaða stöðu á línum. 
- **Ógild staða** - Þessi staða sýnir að viðvörun eða skilaboð hafi verið ræst við úrvinnslu á línunni og að það hafi hugsanlega komið í veg fyrir að kerfið vistaði breytingarnar í þessari línu. Í gamla hnitanetinu, ef vistunaraðgerðin tókst ekki, var notandi þvingaður til baka í línuna til að laga vandamálið strax. Í nýja hnitanetinu er notandi hinsvegar látinn vita að vandamál við staðfestingu hafi komið upp, en að notandi geti ákveðið hvenær hann vilji laga vandann í línunni. Þegar þú ert tilbúinn til að laga vandamál geturðu fært áhersluna handvirkt til baka í línuna. Einnig er hægt að velja aðgerðina **Lagfæra þetta vandamál**. Þessi aðgerð færir áhersluna strax til baka á línuna þar sem vandinn kom upp og leyfir notanda að gera breytingar innan og utan hnitanetsins. Athugið að vinnsla á síðari línum í bið er stöðvuð þar til leyst hefur verið úr þessari staðfestingarviðvörun. 
- **Gert hlé** - Þessi staða gefur til kynna að hlé hafi verið gert á vinnslu netþjónsins því að staðfesting línunnar hafi ræst sprettiglugga sem krefst innslátt notanda. Vegna þess að notandinn gæti verið að slá inn gögn í einhverri annarri línu, er honum ekki birtur sprettiglugginn strax. Í staðinn verður glugginn birtur þegar notandinn kýs að halda áfram vinnslu. Þessari stöðu fylgir tilkynning sem upplýsir notandann um ástandið. Tilkynningin felur í sér aðgerðina **Halda vinnslu áfram** sem ræsir sprettigluggann.

### <a name="differences-when-entering-data-ahead-of-the-system"></a>Mismunur þegar gögn eru slegin inn á undan kerfinu
Þegar þú slærð inn gögn á undan þeim stað þar sem kerfið er í vinnslu kunna nokkrar breytingar verða á upplifun gagnaskráningar:

- Þú munt taka eftir því að það eru engir fellilistar fyrir uppflettingu, gildi reita eru ekki staðfest eftir að þú færir þig í aðra dálk í sömu línu og dálkar sýna ekki sjálfgefin gildi í upphafi. Þessi hegðun á sér stað þegar þú stofnar eða uppfærir á undan kerfinu. Þegar kerfið er komið á þann stað sem þú ert að breyta, verður upplifunin hins vegar eins og venjulega. Ef þú hefur gert breytingar á reit sem venjulega fær sjálfgefið gildi, þá hnekkja breytingar þínar sjálfgefna gildi reitsins þegar netþjónninn byrjar að vinna úr línunni.
- Ef ný lína er búin til með því að nota **Niðurörvarhnappinn** birtast allir dálkar í hnitanetinu sem hægt er að breyta. Sjálfgefið er að leggja áherslu á fyrsta dálkinn í nýju línunni. Þessi dálkur er hugsanlega ekki sami dálkur og var lögð áhersla á í eldri hnitanetinu, eða sami dálkur og var lögð áhersla á eftir að þú hefur valið **Nýjan** hnapp. Fyrirtækið þitt getur sérsniðið kerfið og breytt dálkinum sem er lögð áhersla á í upphafi þegar **Niðurörvarhnappurinn** er valinn. Nánari upplýsingar er að finna í hlutanum [Tilgreina dálk sem lögð er áhersla á í upphafi þegar nýjar línur eru stofnaðar með niðurörvarhnappinum](#developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key). Óháð því er hægt að nota sérstillingu til að fínstilla hvert hnitanet fyrir gagnaskráningu. Nánar tiltekið er hægt að endurraða reitum þannig að fyrsti dálkurinn er dálkurinn sem á að byrja að færa inn gögn. Þú gætir einnig viljað endurraða reitum fyrir gagnaskráningu, til að fækka dálkhökum og fela alla reiti sem eru ekki nauðsynlegir fyrir gagnaskráningu í yfirlitinu sem um ræðir.

### <a name="pasting-from-excel"></a>Líma úr Excel
Notendur hafa alltaf getað flutt gögn úr hnitanetum í forritum fjármála- og reksturs í Microsoft Excel með því að nota aðferðina **Flytja inn í Excel**. Getan til að slá inn gögn á undan kerfinu gerir hinsvegar nýja hnitanetinu kleift að styðja afritun á töflum úr Excel og líma þær beint í hnitanet í forritum fjármála- og reksturs. Hólfið í hnitanetinu þar sem límingaraðgerðin hefst ákvarðar hvar líming á afritaðri töflu hefst. Efni afrituðu töflunnar skrifar yfir efni hnitanetsins, fyrir utan tvö tilfelli:

- Ef fjöldi dálka í afrituðu töflunni er meiri en fjöldi dálka sem eru eftir í hnitanetinu, þar sem staðsetning límingar hefst, er notandanum tilkynnt að aukadálkarnir hafi verið hunsaðir. 
- Ef fjöldi lína í afrituðu töflunni er meiri en fjöldi lína í hnitanetinu, þar sem staðsetning límingar hefst, skrifar límda efnið yfir núverandi hólf, og allar aukalínur í afrituðu töflunni eru settar inn sem nýjar línur neðst í hnitanetinu. 

## <a name="evaluating-math-expressions"></a>Mat á stærðfræðisegðum
Sem framleiðniörvun geta notendur slegið inn stærðfræðiformúlur í tölureiti í töflu. Þeir þurfa ekki að gera útreikninginn í forriti utan kerfisins. Til dæmis ef þú slærð inn **=15\*4** og ýttu síðan á lykilinn **Flipi** til að fara út úr reitnum, mun kerfið meta segðina og vista gildi upp á **60** fyrir reitinn.

[![Mat á stærðfræðisegðum.](./media/gridMathExpression-07-25-2022.gif)](./media/gridMathExpression-07-25-2022.gif)

Til að gera kerfið að viðurkenna gildi sem tjáningu, byrjaðu gildið með jöfnu merki (**=**). Nánari upplýsingar um rekstraraðila sem studd er og setningafræði, sjá [Studd stærðfræðitákn](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

Frá og með útgáfu 10.0.29 hefur getan til að meta stærðfræðisegðir með tölustjórnun stærðfræðitjáningu í talnastýringum verið framlengd og er nú einnig aðgengileg utan hnitanetsins.

## <a name="grouping-tabular-data"></a>Flokkun töflugagna
Fyrirtækjanotendur þurfa oft að framkvæma sértækar greiningar á gögnum. Þó að hægt sé að framkvæma greiningu með því að flytja út gögn á Microsoft Excel og nota Pivot-töflur gerir **flokkun í hnitaneti** eiginleikinn, sem er háður nýjum eiginleika hnitastýringar, notendum kleift að skipuleggja töflugögn á áhugaverðan hátt innan forrita fjármála- og reksturs. Vegna þess að þessi eiginleiki stækkar eiginleikann **Reiknuð gildi** gerir **Flokkun** þér kleift að fá gagnlegri innsýn í gögnin með því að gefa upp reiknuð gildi (t.d. millisamtölur) á hópstigi.

[![Flokkar gögn í hnitaneti.](./media/grids-groupingWithTotals.png)](./media/grids-groupingWithTotals.png)

Til að nota þennan eiginleika skal hægrismella á dálkinn sem á að flokka eftir, og velja **Flokka eftir þessum dálki**. Þessi aðgerð mun raða gögnum eftir völdum dálki, bæta við nýjum **Flokki eftir** dálki við upphaf hnitanetsins og setja inn „hauslínur“ í upphafi hvers hóps. Þessar hausraðir veita eftirfarandi upplýsingar um hvern hóp:

- Gagnagildi fyrir hópinn 
- Dálkheiti (þessar upplýsingar eru sérstaklega gagnlegar þegar mörg flokkunarstig eru til staðar)
- Fjöldi gagnalína í þessum hópi
- Reiknuð gildi fyrir hvaða skilgreinda dálk sem er (til dæmis millisamtölur ef dálkurinn er stilltur til að sýna samtölu)

Þegar [Vistuð yfirlit](saved-views.md) eru virkjuð er hægt að vista flokkun sem hluta af yfirliti á síðum sem leyfa að vista fyrirspurnir í yfirlitum. Til dæmis þeir sem eru með stórt yfirlitsval. Sjá hlutann [Skipta á milli yfirlita](saved-views.md#switching-between-views) fyrir frekari upplýsingar. 

### <a name="multiple-levels-of-grouping"></a>Mörg stig flokkunar
Eftir að gögn hafa verið flokkuð eftir einum dálki er hægt að flokka gögnin eftir öðrum dálki með því að velja **Flokka eftir þessum dálki** í viðkomandi dálki. Hægt er að endurtaka þetta ferli þar til fimm faldaðar stigaflokkanir eru til staðar, sem er studd hámarksdýpt. Á þessu stigi er ekki lengur hægt að flokka eftir viðbótardálkum.

Hvenær sem er er hægt að fjarlægja flokkun í hvaða dálki sem er með því að hægrismella á dálkinn og velja **Sundra hópi**. Einnig er hægt að fjarlægja flokkun úr öllum dálkum með því að velja **Valkostir hnitanets** og síðan **Sundra öllum hópi**.

### <a name="sorting-grouped-data"></a>Raða flokkuðum gögnum
Eftir að gögn hafa verið flokkuð í einn eða fleiri dálka er hægt að breyta röðunarstefnu hvers flokkunardálks með samsvarandi dálkahaus. 

Ef þú raðar í óflokkaðan dálk helst flokkunin óbreytt. Gögnunum er raðað innan hvers flokks, miðað við valda dálkinn.

### <a name="expanding-and-collapsing-groups"></a>Stækka og fella saman hópa
Fyrsta flokkun gagna verður með alla hópa útvíkkaða. Hægt er að búa til samandregin yfirlit yfir gögnin með því að fella saman einstaka flokka eða nota hóp til að stækka og draga saman til að aðstoða við að fletta í gegnum gögn. Til að víkka út hóp eða draga hann saman skal velja tvíoddatákn (>) hnappinn í samsvarandi flokkshauslínu. Athugið að staða fyrir víkkun/samanfellingu einstakra flokka er **ekki** vistuð í sérstillingum.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Velja og afvelja línur á hópstigi
Á sama hátt og hægt er að velja (eða afvelja) allar línur í hnitanetinu með því að velja gátreitinn efst í fyrsta dálkinum í hnitanetinu, einnig er hægt að velja (eða afvelja) allar línur í hópi með því að velja gátreitinn í samsvarandi hauslínu hóps. Gátreiturinn í hauslínu hóps endurspeglar alltaf núverandi valstöðu lína í þeim hópi, burtséð frá því hvort allar línur séu valdar, engar línur séu valdar eða aðeins nokkrar línur séu valdar.

### <a name="hiding-column-names"></a>Fela dálkaheiti
Við flokkun gagna er sjálfgefið að hegðun sýni dálkheiti í hauslínu hóps. Hægt er að fela dálkheitið í hauslínu hóps með því að velja **Valkostir hnitanets** > **Fela dálkheiti hóps**.

### <a name="grouping-on-date-and-time-columns"></a>Flokkun dálka dagsetninga og tíma
Þegar þú flokkar reitina Dagsetning eða Dagsetning og tími getur þú valið um að flokka eftir ári, mánuði eða degi. Flokkurinn „gildi“ í samsvarandi hauslínu mun samsvara sniðinu úr þeim reit. Að auki er hægt að flokkar reitina Dagsetning eða Dagsetning og tími eftir klukkustund, mínútu eða sekúndu.

> [!IMPORTANT]
> Notendur geta ekki bætt við flokkunardálki eftir að þeir hafa sett hóp í hluta af dagsetningu eða tímadálki.

## <a name="freezing-columns"></a>Dálkar frystir
Sumir dálkar í hnitaneti gætu reynst það mikilvægir fyrir samhengi þannig að þú vilt ekki að þeir hverfi úr augsýn við flettingu. Þess í stað gætirðu viljað að gildin í þessum dálkum séu alltaf sýnileg. Eiginleikinn **Festa dálka í hnitaneti** býður notendum upp á þennan sveigjanleika. 

[![Frystir dálka í hnitaneti.](./media/gridFreezingColumns-07-25-2022.gif)](./media/gridFreezingColumns-07-25-2022.gif)

Til að festa dálk skal hægrismella í haus dálksins og síðan velja **Festa dálk**. Í fyrsta skipti sem þetta skref er gert verður valinn dálkur að fyrsta dálkinum og mun ekki lengur hverfa úr augsýn við flettingu. Næstu dálkum sem eru festir verður bætt hægra megin við síðasta festa dálkinn. Hægt er að nota venjulegu færsluaðgerðina til að endurraða festum dálkum eftir þörfum. Hins vegar er ekki hægt að færa festa dálka þannig að þeir birtist á meðal ófestra dálka. Að sama skapi er ekki hægt að færa ófesta dálka þannig að þeir birtist á meðal festra dálka.

Til að losa dálk skal hægrismella í haus fests dálks og síðan velja **Losa dálk**. 

Athugið að dálkval og línustaða dálka í nýja hnitanetinu eru alltaf fest sem fyrstu tveir dálkarnir. Þess vegna, þegar þessir dálkar eru teknir með í hnitaneti, verða þeir alltaf sýnilegir notanda, óháð láréttri flettistöðu í hnitanetinu. Ekki er hægt að endurraða þessum tveimur dálkum.

## <a name="autofit-column-width"></a>Aðlaga dálkbreidd sjálfkrafa
Eins og í Excel geta notendur þvingað dálk til að breyta stærðinni sjálfkrafa miðað við efnið sem verið er að sýna í honum. Einungis þarf að tvísmella (eða tvísmella) á gripsvæðin í dálknum. Einnig er hægt að leggja áherslu á dálkahausinn og velja svo lykilinn **A** (fyrir sjálfvirka aðlögun).

## <a name="frequently-asked-questions"></a>Algengar spurningar
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Hvernig virkja ég nýja netstýringu í umhverfi mínu? 

Eiginleikinn **Ný hnitanetsstýring** er í boði í eiginleikastjórnun í hvaða umhverfi sem er. Eftir að eiginleikinn í eiginleikastjórnun hefur verið virkjaður munu allar síðari notandalotur nýta sér nýju netstýringuna. 

Þessi eiginleiki byrjaði fyrst að vera sjálfgefinn í útgáfu 10.0.21. Stefnt er að því að slíkt verði áskilið í október 2022.

## <a name="developer-topics"></a>Umfjöllunarefni forritara

### <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Þróunaraðili] Afskrá einstaka síður frá því að nota nýja hnitanetið 
Ef fyrirtækið uppgötvar síðu sem á í vandræðum með að nota nýja hnitanetið, er API tiltækt til að leyfa einstökum skjámyndum að nota eldri netstýringu og leyfa á sama tíma öðrum hlutum kerfisins að nota nýju netstýringuna. Til að afskrá einstaka síður frá því að nota nýja hnitanetið, skal bæta við eftirfarandi kallskilaboðum `super()` í `run()` aðferð skjámyndarinnar.

```this.forceLegacyGrid();```

Þetta forritaskil (API) verður að lokum gert úrelt til að hægt sé að fjarlægja eldri hnitanetsstýringar. Hún verður þó tiltæk í að minnsta kosti 12 mánuði eftir að úrelding hennar er tilkynnt. Ef einhver vandamál krefjast þess að þetta API sé notað skal tilkynna um þau til Microsoft.

#### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Að þvinga síðu til að nota nýja netið eftir að hafa áður afþakkað netið
Ef þú hefur valið að nota ekki einstaka síðu á nýja netinu gætirðu viljað virkja nýja netið aftur síðar eftir að undirliggjandi vandamál hafa verið leyst. Til að gera þetta þarftu einfaldlega að fjarlægja kallið við `forceLegacyGrid()`. Breytingin tekur ekki gildi fyrr en eitt af eftirfarandi gerist:

- **Endurvirkjun umhverfis**: Þegar umhverfi er uppfært og virkað að nýju er taflan sem geymir síðurnar sem hafa verið valdar úr nýja netinu sjálfkrafa hreinsuð út (FormControlReactGridState).
- **Handvirk hreinsun töflunnar**: Fyrir þróunaraðstæður þarftu að nota SQL til að hreinsa FormControlReactGridState töfluna og endurræsa síðan AOS. Þessi samsetning aðgerða mun endurstilla skyndiminni síðna sem hafa afþakkað nýja hnitið.

### <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Forritari] Að stilla tiltekin hnitanet með innslætti á undan getu kerfisins
Nokkrar sviðsmyndir hafa komið upp sem hafa ekki reynst vel við *Innsláttargetu hnitanetsins á undan kerfinu*. (Til dæmis, einhver kóði sem er ræstur þegar lína er staðfest veldur því að rannsókn gagnagjafa fer í gang, og rannsóknin getur síðan skemmt óstaðfestar breytingar á núverandi línum). Ef fyrirtækið þitt upplifir slíka sviðsmynd eru forritaskil (API) í boði sem gerir forritara kleift að taka stakt hnitanet úr ósamstilltri staðfestingu línu og skipta aftur yfir í eldri hegðun.

Þegar ósamstillt staðfesting línu er gerð óvirk í hnitaneti geta notendur ekki búið til nýja línu eða fært sig yfir í aðra línu í hnitanetinu á meðan vandamál varðandi staðfestingu eru til staðar í núverandi línu. Önnur áhrif sem þessi aðgerð hefur er að ekki verður hægt að líma töflur úr Excel inn í hnitanet fjármála- og reksturs.

Til að taka staka línu úr ósamstilltri staðfestingu línu skal bæta við eftirfarandi kalli eftir að búið er að fylla `super()` inn í `run()` aðferðina á eyðublaðinu.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Aðeins ætti að nota þetta kall í undantekningartilvikum og ætti ekki að vera hefðbundið verklag fyrir öll hnitanet.
> - Ekki er mælt með því að virkja þessi forritaskil (API) á keyrslutíma eftir að eyðublaðinu er hlaðið inn.

### <a name="developer-size-to-available-width-columns"></a>[Þróunaraðili] Stækka breidd dálka eins og hægt er
Ef þróunaraðili stillir eiginleikann **WidthMode** á **SizeToAvailable** fyrir dálka innan nýja hnitanetsins, fá þessir dálkar upphaflega sömu breidd og þeir myndu fá ef eiginleikinn væri stilltur á **SizeToContent**. Hins vegar teygist á þeim þannig að þeir noti þá breidd sem í boði er innan hnitanetsins. Ef eiginleikinn er stilltur á **SizeToAvailable** fyrir marga dálka, deila allir þessir dálkar á milli sín aukalegri breidd sem er í boði innan hnitanetsins. Hins vegar, ef notandi breytir stærð einhverra þessara dálka, verður sá dálkur fastur. Hann heldur þeirri breidd og breikkar ekki lengur til að fylla upp í tiltæka breidd hnitanetsins.

### <a name="developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key"></a>[Forritari] Tilgreinir dálkinn sem upphaflega er áhersla á þegar nýjar línur eru búnar til með því að nota niðurörvarhnappinn
Eins og fjallað var um í hlutanum [Mismunur þegar gögn eru slegin inn á undan kerfinu](#differences-when-entering-data-ahead-of-the-system) ef eiginleikinn „Innsláttur á undan kerfinu“ er virkur, og notandi stofnar nýja línu með því að nota **Niðurörvahnappinn**, er sjálfgefna hegðunin sú að leggja áherslu á fyrsta dálkinn í nýju línunni. Þessi upplifun gæti verið frábrugðin upplifuninni í eldra hnitanetinu eða þegar **Nýr** hnappur er valinn.

Notendur og fyrirtæki geta búið til vistuð yfirlit sem eru sérstillt fyrir gagnaskráningu. (Til dæmis er hægt að endurraða dálkum þannig að fyrsti dálkurinn sé sá sem á að byrja að slá inn gögn í). Þar að auki, frá og með útgáfu 10.0.29, geta fyrirtæki breytt þessari hegðun með því að nota aðferðina **selectedControlOnCreate()**. Þessi aðferð gerir forritara kleift að tilgreina dálkinn sem ætti að leggja áherslu á í upphafi þegar ný lína er stofnuð með því að nota **Niðurörvahnappinn**. Sem innslátt taka þessi forritaskil (API) stjórnkenni sem samsvarar dálknum sem ætti að leggja áherslu á í upphafi.

### <a name="developer-handling-grids-with-non-react-extensible-controls"></a>[Forritari] Meðhöndlun hnitaneta með stækkanlegum stýringum sem eru ekki React
Þegar hnitanet er að hlaðast, ef kerfið finnur stækkanlega stýringu sem er ekki byggt á React, mun kerfið þvinga eldra hnitanetið til að gera það virkt í staðinn. Þegar notandi lendir í þessum aðstæðum birtast skilaboð sem gefa til kynna að uppfæra þurfi síðuna. Eftir það hleður þessi síða eldra hnitanetinu sjálfkrafa inn án frekari tilkynninga til notenda þar til næsta kerfisuppfærsla á sér stað. 

Til að lagfæra þetta ástand varanlega, geta höfundar stækkanlegra stýringa búið til React-útgáfu af stýringunni til notkunar í hnitanetinu.  Þegar forritun er lokið er hægt að bæta eigindinni **FormReactControlAttribute** við X++ flokk stýringarinnar til að tilgreina staðsetningu React- eiginleikanum til að tilgreina staðsetningu React-búntsins sem á að hlaða fyrir umrædda stýringu. Sjá `SegmentedEntryControl`-flokkinn sem dæmi.  

## <a name="known-issues"></a>Þekkt vandamál
Þessi hluti heldur lista yfir þekkt vandamál fyrir nýju hnitanetsstýringuna.

### <a name="open-issues"></a>Opin vandamál
- Þegar búið er að virkja eiginleikann **Ný hnitanetsstýring**, halda sumar síður áfram að nota núverandi netstýringu. Þetta gerist við eftirfarandi aðstæður:
 
    - [Leyst] Spjaldlisti er til á síðunni sem gefinn er upp í mörgum dálkum.
        - Þessi gerð spjaldlista er studd af **Ný hnitanetsstýring** sem hefst í útgáfu 10.0.30. Hægt er að fjarlægja alla notkun á forceLegacyGrid() í þessu skyni. 
    - [Leyst] Flokkaður spjaldlisti er til á síðunni.
        - Hópaðir spjaldlistar eru studdir af **Nýju hnitanetsstýringunni** sem hefst í útgáfu 10.0.30. Hægt er að fjarlægja alla notkun á forceLegacyGrid() í þessu skyni. 
    - [Leyst] Dálkur hnitanets sem bregst ekki við stækkanlegri stýringu.
        - Stækkanlegar stýringar geta veitt React-útgáfu af stýringunni sem verður hlaðið inn þegar hún er sett í hnitanetið og lagað skilgreiningu stýringar til að hlaða þessari stýringu þegar hún er notuð í hnitanetinu. Frekari upplýsingar er að finna í hluta viðkomandi þróunaraðila. 

    Þegar notandi stendur í fyrsta skipti frammi fyrir þessum aðstæðum birtast skilaboð um að uppfæra skuli síðuna. Eftir að þessi skilaboð birtast mun síðan halda áfram að nýta núverandi hnitanet fyrir alla notendur fram að næstu uppfærslu afurðar. Betri meðhöndlun á þessum aðstæðum, svo hægt sé að nýta nýja hnitanetið, verður höfð í huga í framtíðaruppfærslu.

- [KB 4582758] Færslur eru óskýrar þegar verið er að breyta aðdrætti úr 100 í einhverja aðra prósentutölu

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

