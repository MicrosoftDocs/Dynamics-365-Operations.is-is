---
title: Eiginleikar hnitanets
description: Þessi grein lýsir nokkrum öflugum eiginleikum riststýringarinnar. Virkja þarf nýjan eiginleika hnitanetsins til að hafa aðgang að þessum möguleikum.
author: jasongre
ms.date: 08/09/2022
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
ms.openlocfilehash: a8968a1263dfafd67b07b4beb78c51493e95756e
ms.sourcegitcommit: 47534a943f87a9931066e28f5d59323776e6ac65
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/11/2022
ms.locfileid: "9258948"
---
# <a name="grid-capabilities"></a>Eiginleikar hnitanets

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Nýja netstýringin veitir fjölda gagnlegra og öflugra eiginleika sem hægt er að nota til að auka framleiðni notenda, smíða áhugaverðari sýn á gögnin þín og fá þroskandi innsýn í gögnin þín. Þessi grein mun fjalla um eftirfarandi getu: 

- Sýnir reiknuð gildi 
- Vélritun á undan kerfinu
- Mat á stærðfræðisegðum 
- Flokkun gagna í töfluformi (virkjað sérstaklega með því að nota **Flokkun í rist** eiginleiki)
- Frysting dálka (virkjað sérstaklega með því að nota **Frysta súlur í ristum** eiginleiki)
- Aðlaga dálkbreidd sjálfkrafa
- Teygjanlegir dálkar

## <a name="showing-calculated-values"></a>Sýnir reiknuð gildi
Í fjármála- og rekstraröppum geta notendur skoðað útreiknað gildi fyrir hvern tölulegan dálk í töflu. Fóturhluti neðst á ristinni sýnir þessi reiknuðu gildi.

[![Sýnir reiknuð gildi í ristum.](./media/grids-aggregation.png)](./media/grids-aggregation.png)

Í útgáfum fyrir 10.0.29 er heildartalan eina studda reiknaða gildið. Hins vegar, frá og með útgáfu 10.0.29, eftir að þeir virkjaðu **Aukinn möguleiki til að safna neti** eiginleika, geta notendur valið á milli eftirfarandi fjögurra reiknaða gilda:

- Lágmark
- Hámark
- Samtals
- Meðaltal

Einn dálkur getur aðeins sýnt eina tegund af reiknuðu gildi. Hins vegar er hægt að stilla hvern dálk í hnitanetinu til að sýna aðra tegund af reiknuðu gildi.

### <a name="showing-the-grid-footer"></a>Sýni síðufót hnitanetsins
Það er fótsvæði neðst á hverju töfluneti í fjármála- og rekstraröppum. Neðanmálið getur sýnt mikilvægar upplýsingar sem tengjast gögnum sem birtast í reitunum. Hér eru nokkur dæmi um þessar upplýsingar:

- Fjöldi valdra lína í töflunni (þegar fleiri en ein skrá er valin)
- Reiknuð gildi neðst í stilltum, tölulegum dálkum (til dæmis heildartölur)
- Fjöldi raða í gagnasafninu 

Þessi fótur er sjálfgefið falinn en þú getur kveikt á honum. Til að sýna síðufót fyrir hnitanet skal velja hnappinn **Valkostir hnitanets** í haus hnitanetsins og síðan velja valkostinn **Sýna síðufót**. Eftir að kveikt er á síðufætinum fyrir tiltekið hnitanet verður stillingin geymd í minni þar til notandinn kýs að fela síðufótinn. Til að fela síðufótinn skal velja **Fela síðufót** á valmyndinni **Valkostir hnitanets**.

### <a name="specifying-columns-with-calculated-values"></a>Tilgreina dálka með reiknuðum gildum
Sem stendur sýna engir dálkar sjálfgefið reiknað gildi. Þess í stað er uppsetningin talin einskiptisaðgerð, eins og að stilla breidd dálka í ristum. Eftir að þú hefur tilgreint að þú viljir skoða reiknað gildi fyrir dálk, verður sú stilling minnst næst þegar þú heimsækir síðuna.

Það eru tvær leiðir til að stilla dálk til að sýna reiknað gildi:

- Veldu og haltu inni (eða hægrismelltu) í dálknum sem þú vilt skoða reiknað gildi fyrir. Ef **Aukinn möguleiki til að safna neti** eiginleiki er virkur, veldu **Skoða heildartölur dálka**, og veldu síðan viðeigandi reiknaða gildi. Ef þessi eiginleiki er ekki virkur skaltu velja **Samtals þennan dálk**. Þessi aðgerð veldur því að þrír atburðir eiga sér stað:

    1. Ratnarfóturinn verður sýnilegur. 
    2. Val þitt fyrir að skoða reiknað gildi fyrir dálkinn er vistað. 
    3. Æskilegur útreikningur er hafinn fyrir dálkinn og aðra dálka sem þú hefur áður stillt til að sýna reiknað gildi. Tíminn sem þarf til að sýna reiknuð gildi fer eftir stærð gagnasafnsins.

- Eftir að fóturinn er sýnilegur skaltu velja **Sýna samtals** (eða **Veldu reiknað gildi** ef **Aukinn möguleiki til að safna neti** eiginleiki er virkur) í fótsvæðinu neðst í dálknum sem þú vilt skoða reiknað gildi fyrir. Ef það eru engir stilltir dálkar mun sá hnappur vera tiltækur í síðufæti í öllum töludálkum.

    Eftir að að minnsta kosti einn dálkur hefur verið stilltur til að sýna reiknað gildi, **Sýna samtals** (eða **Veldu reiknað gildi**) hnappurinn verður aðeins tiltækur á sveimi eða fókus. Aðgerðin með því að velja hnappinn vistar bara val þitt fyrir að skoða reiknað gildi í dálknum, svo að valið sé notað við framtíðarheimsóknir á síðuna. Í neðanmálinu er þessi staða gefin til kynna með bandstriki sem birtist í dálkinum. (Athugaðu að reiknað gildi birtist strax ef gagnasafnið er nógu lítið.)

Ef þú gerir mistök og vilt ekki lengur skoða reiknað gildi í tilteknum dálki skaltu velja og halda inni (eða hægrismella) í dálknum og velja síðan **Fela samtals** (eða **Skoða heildartölur dálka \> Enginn** ef **Aukinn möguleiki til að safna neti** eiginleiki er virkur). Að öðrum kosti skaltu velja **Fela samtals** (eða **Fela reiknað gildi**) í síðufæti í þeim dálki. Þessi valkostur verður einnig vistaður fyrir framtíðarheimsóknir á síðunni. 

### <a name="calculating-aggregate-values"></a>Útreikningur á heildargildum
Þegar þú ferð á síðu þar sem fóturinn er sýnilegur og dálkar eru nú þegar stilltir til að sýna reiknuð gildi, gætu þessi gildi ekki verið sýnd í fótinn. Hegðunin fer eftir stærð gagnasafnsins á síðunni. Ef gagnasafnið er nógu lítið birtast útreiknuð gildi sjálfkrafa ásamt fjölda lína í gagnasafninu. Ef það eru strik í síðufæti undir dálkunum sem þú stilltir er gagnasafnið of stórt til að kerfið geti sýnt reiknuð gildi strax. Í þessu tilviki þarf skýrar aðgerðir til að reikna út gildin. Til að reikna út gildin skaltu velja **Reikna** hnappinn í síðufæti. Að öðrum kosti skaltu velja og halda inni (eða hægrismella) í dálki sem þú vilt skoða heildarfjöldann fyrir og velja síðan **Samtals þennan dálk** (eða **Skoða heildartölur dálka** og síðan æskilegt reiknað gildi ef **Aukinn möguleiki til að safna neti** eiginleiki er virkur).

Ef það tekur langan tíma að klára útreikninginn er hægt að hætta við aðgerðina hvenær sem er með því að velja **Hætta við**. Stundum verður gagnasafnið of stórt til að reikna út heildargildi (takmörk sem stofnunin þín setur). Í þessu tilviki færðu í staðinn tilkynningu um að sía gögnin þín meira.

> [!NOTE]
> Kerfisstjórar geta breytt takmörkunum fyrir fjölda færslur sem eru tiltækar til að reikna út samanlagðan hlut með því að breyta **Hámarksfjöldi staðbundinna gagna fyrir hvert rist** breytu á **Frammistöðuvalkostir viðskiptavina** síðu. Sjálfgefið gildi er 25.000 færslur. Stjórnendur ættu að vera varkár þegar þeir stilla þetta gildi, vegna þess að gildi sem er of stórt getur tæmt tiltækt minni á vél notandans. Við mælum með að gildið sé ekki hærra en 50.000 færslur.

Reiknuð gildi verða sjálfkrafa uppfærð þegar þú uppfærir, eyðir eða býrð til línur í gagnasafninu.

## <a name="typing-ahead-of-the-system"></a>Vélritun á undan kerfinu
Í mörgum atburðarásum í viðskiptum er möguleikinn til að færa gögn fljótt inn í kerfið mjög mikilvægur. Fyrir kynningu á nýju netstýringunni gátu notendur aðeins breytt gögnum í núverandi röð. Þess vegna, eftir að þeir gerðu breytingar í röð, gátu notendur ekki skipt yfir í aðra röð eða búið til nýja línu fyrr en kerfið hefur staðfest breytingarnar í núverandi röð og (ef um er að ræða línugerð) keyrt alla rökfræði sem tengist með stofnun nýrrar röðar. Til að hjálpa til við að draga úr þeim tíma sem notendur eyða í að bíða eftir að þessum aðgerðum ljúki, og til að bæta framleiðni notenda, lagar nýja netið þessar aðgerðir þannig að þær séu ósamstilltar. Notendur geta búið til nýjar raðir eða farið í aðrar raðir til að gera breytingar á meðan fyrri raðir sannprófanir og raðir búa til rökfræði eru í bið. 

[![Að slá á undan kerfinu.](./media/gridFastEntry-07-25-2022.gif)](./media/gridFastEntry-07-25-2022.gif)

Til að styðja við þessa nýju hegðun hefur nýjum dálki fyrir línustöðuna verið bætt við hægra megin við dálk línuvals þegar hnitanetið er í breytingastillingu. Þessari dálkur sýnir eina af eftirfarandi stöðum:

- **Autt** - Engin stöðumynd gefur til kynna að kerfið hafi náð að vista línuna.
- **Vinnsla í bið** - Þessi staða gefur til kynna að netþjónninn hafi enn ekki vistað breytingar í línunni en að þær séu í biðröð breytinga sem þarf að vinna úr. Áður en gripið er til aðgerða utan hnitanetsins þarf að bíða eftir að unnið er úr öllum breytingum. Að auki er textinn í þessum línum skáletraður til að gefa til kynna óvistaða stöðu á línum. 
- **Ógild staða** - Þessi staða sýnir að viðvörun eða skilaboð hafi verið ræst við úrvinnslu á línunni og að það hafi hugsanlega komið í veg fyrir að kerfið vistaði breytingarnar í þessari línu. Í gamla hnitanetinu, ef vistunaraðgerðin tókst ekki, var notandi þvingaður til baka í línuna til að laga vandamálið strax. Í nýja hnitanetinu er notandi hinsvegar látinn vita að vandamál við staðfestingu hafi komið upp, en að notandi geti ákveðið hvenær hann vilji laga vandann í línunni. Þegar þú ert tilbúinn til að laga vandamál geturðu fært áhersluna handvirkt til baka í línuna. Einnig er hægt að velja aðgerðina **Lagfæra þetta vandamál**. Þessi aðgerð færir áhersluna strax til baka á línuna þar sem vandinn kom upp og leyfir notanda að gera breytingar innan og utan hnitanetsins. Athugið að vinnsla á síðari línum í bið er stöðvuð þar til leyst hefur verið úr þessari staðfestingarviðvörun. 
- **Gert hlé** - Þessi staða gefur til kynna að hlé hafi verið gert á vinnslu netþjónsins því að staðfesting línunnar hafi ræst sprettiglugga sem krefst innslátt notanda. Vegna þess að notandinn gæti verið að slá inn gögn í einhverri annarri línu, er honum ekki birtur sprettiglugginn strax. Í staðinn verður glugginn birtur þegar notandinn kýs að halda áfram vinnslu. Þessari stöðu fylgir tilkynning sem upplýsir notandann um ástandið. Tilkynningin felur í sér aðgerðina **Halda vinnslu áfram** sem ræsir sprettigluggann.

### <a name="differences-when-entering-data-ahead-of-the-system"></a>Mismunur þegar gögn eru slegin inn á undan kerfinu
Þegar þú slærð inn gögn á undan þeim stað þar sem kerfið er að vinna, geturðu búist við nokkrum breytingum á gagnafærsluupplifuninni:

- Þú munt taka eftir því að það eru engir fellilistar fyrir uppfletti, svæðisgildi eru ekki staðfest eftir að þú færð í annan dálk í sömu röð og dálkar sýna upphaflega ekki sjálfgefin gildi. Þessi hegðun á sér stað þegar þú býrð til eða uppfærir á undan kerfinu. Hins vegar, eftir að kerfið nær þeim stað þar sem þú ert að breyta, mun staðlað upplifun halda áfram. Ef þú gerðir breytingar á reit sem venjulega fær sjálfgefið gildi, hnekkja breytingarnar þínar sjálfgefna svæðisgildi þegar þjónninn byrjar að vinna úr röðinni.
- Ef þú býrð til nýja línu með því að nota **Ör niður** takka, allir dálkar í ristinni munu birtast sem breytanlegar. Sjálfgefið er að fókusinn verði settur í fyrsta dálkinn í nýju línunni. Þessi dálkur gæti ekki verið sami dálkur og fékk upphaflega fókusinn í eldri töflunni, eða sami dálkur sem fær fókus eftir að þú hefur valið **Nýtt** takki. Stofnunin þín getur sérsniðið kerfið og breytt dálknum sem fær upphafsfókus þegar **Ör niður** lykill er valinn. Fyrir frekari upplýsingar, sjá [Tilgreinir dálkinn sem fær upphafsfókus þegar nýjar línur eru búnar til með því að nota örvatakkann niður](#developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key) kafla. Burtséð frá því geturðu notað sérstillingar til að fínstilla hvert rist fyrir innslátt gagna. Nánar tiltekið geturðu endurraðað reitum þannig að fyrsti dálkurinn sé dálkurinn sem þú vilt byrja að slá inn gögn í. Þú gætir líka viljað endurraða reitum almennt fyrir gagnafærslu, til að draga úr flipastoppum og fela alla reiti sem eru ekki nauðsynlegir fyrir gagnafærslu í þessari tilteknu sýn.

### <a name="pasting-from-excel"></a>Líma úr Excel
Notendur hafa alltaf getað flutt gögn úr netum í fjármála- og rekstraröppum til Microsoft Excel með því að nota **Flytja út í Excel** vélbúnaður. Hins vegar, möguleikinn á að slá inn gögn á undan kerfinu gerir nýja ristinni kleift að styðja afritun töflur úr Excel og líma þær beint inn í töflur í fjármála- og rekstraröppum. Hólfið í hnitanetinu þar sem límingaraðgerðin hefst ákvarðar hvar líming á afritaðri töflu hefst. Efni afrituðu töflunnar skrifar yfir efni hnitanetsins, fyrir utan tvö tilfelli:

- Ef fjöldi dálka í afrituðu töflunni er meiri en fjöldi dálka sem eru eftir í hnitanetinu, þar sem staðsetning límingar hefst, er notandanum tilkynnt að aukadálkarnir hafi verið hunsaðir. 
- Ef fjöldi lína í afrituðu töflunni er meiri en fjöldi lína í hnitanetinu, þar sem staðsetning límingar hefst, skrifar límda efnið yfir núverandi hólf, og allar aukalínur í afrituðu töflunni eru settar inn sem nýjar línur neðst í hnitanetinu. 

## <a name="evaluating-math-expressions"></a>Mat á stærðfræðisegðum
Sem framleiðniörvun geta notendur slegið inn stærðfræðiformúlur í tölureiti í töflu. Þeir þurfa ekki að gera útreikninginn í forriti utan kerfisins. Til dæmis ef þú slærð inn **=15\*4** og ýttu síðan á lykilinn **Flipi** til að fara út úr reitnum, mun kerfið meta segðina og vista gildi upp á **60** fyrir reitinn.

[![Að meta stærðfræðiorð.](./media/gridMathExpression-07-25-2022.gif)](./media/gridMathExpression-07-25-2022.gif)

Til að gera kerfið að viðurkenna gildi sem tjáningu, byrjaðu gildið með jöfnu merki (**=**). Nánari upplýsingar um rekstraraðila sem studd er og setningafræði, sjá [Studd stærðfræðitákn](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).

Frá og með útgáfu 10.0.29 hefur hæfileikinn til að meta stærðfræðilega tjáningu í talnastýringum verið útvíkkuð og er nú einnig fáanleg utan hnitanetsins.

## <a name="grouping-tabular-data"></a>Flokkun töflugagna
Viðskiptanotendur þurfa oft að framkvæma sérstaka greiningu á gögnum. Þó að hægt sé að gera þessa greiningu með því að flytja út gögn til Microsoft Excel og með því að nota pivot töflur, the **Flokkun í rist** eiginleiki, sem er háður nýju netstýringareiginleikanum, gerir notendum kleift að skipuleggja töflugögn sín á áhugaverðan hátt innan fjármála- og rekstrarforrita. Vegna þess að þessi eiginleiki framlengir **Reiknuð gildi** eiginleiki, **Flokkun** gerir þér kleift að öðlast þýðingarmikla innsýn í gögnin með því að gefa upp reiknuð gildi (til dæmis undirsamtölur) á hópstigi.

[![Samsetning gagna í rist.](./media/grids-groupingWithTotals.png)](./media/grids-groupingWithTotals.png)

Til að nota þennan eiginleika skal hægrismella á dálkinn sem á að flokka eftir, og velja **Flokka eftir þessum dálki**. Þessi aðgerð mun raða gögnum eftir völdum dálki, bæta við nýjum **Flokki eftir** dálki við upphaf hnitanetsins og setja inn „hauslínur“ í upphafi hvers hóps. Þessar hausraðir veita eftirfarandi upplýsingar um hvern hóp:

- Gagnagildi fyrir hópinn 
- Dálkheiti (þessar upplýsingar eru sérstaklega gagnlegar þegar mörg flokkunarstig eru til staðar)
- Fjöldi gagnalína í þessum hópi
- Reiknuð gildi fyrir hvaða stillta dálk sem er (til dæmis undirsamtölur ef dálkurinn er stilltur til að sýna heildartölu)

Með [Vistaðar skoðanir](saved-views.md) virkt geturðu vistað flokkun sem hluta af yfirliti á síðum sem gera kleift að vista fyrirspurnir á skoðanir. Til dæmis þeir sem eru með stóra útsýnisvalara. Sjáðu [Skipt á milli skoðana](saved-views.md#switching-between-views) kafla fyrir frekari upplýsingar. 

### <a name="multiple-levels-of-grouping"></a>Mörg stig flokkunar
Eftir að gögn hafa verið flokkuð eftir einum dálki er hægt að flokka gögnin eftir öðrum dálki með því að velja **Flokka eftir þessum dálki** í viðkomandi dálki. Hægt er að endurtaka þetta ferli þar til fimm faldaðar stigaflokkanir eru til staðar, sem er studd hámarksdýpt. Á þessu stigi er ekki lengur hægt að flokka eftir viðbótardálkum.

Hvenær sem er er hægt að fjarlægja flokkun í hvaða dálki sem er með því að hægrismella á dálkinn og velja **Sundra hópi**. Einnig er hægt að fjarlægja flokkun úr öllum dálkum með því að velja **Valkostir hnitanets** og síðan **Sundra öllum hópi**.

### <a name="sorting-grouped-data"></a>Röðun flokkaðra gagna
Eftir að þú flokkar gögn eftir einum eða fleiri dálkum geturðu breytt röðunarstefnu fyrir hvaða flokkunardálk sem er í gegnum samsvarandi dálkhaus. 

Ef þú flokkar á óflokkaðan dálk helst flokkunin ósnortin. Gögnin eru flokkuð innan hvers hóps, byggt á völdum dálki.

### <a name="expanding-and-collapsing-groups"></a>Stækka og fella saman hópa
Fyrsta flokkun gagna verður með alla hópa útvíkkaða. Hægt er að búa til samandregin yfirlit yfir gögnin með því að fella saman einstaka flokka eða nota hóp til að stækka og draga saman til að aðstoða við að fletta í gegnum gögn. Til að víkka út hóp eða draga hann saman skal velja tvíoddatákn (>) hnappinn í samsvarandi flokkshauslínu. Athugið að staða fyrir víkkun/samanfellingu einstakra flokka er **ekki** vistuð í sérstillingum.

### <a name="selecting-and-unselecting-rows-at-the-group-level"></a>Velja og afvelja línur á hópstigi
Á sama hátt og hægt er að velja (eða afvelja) allar línur í hnitanetinu með því að velja gátreitinn efst í fyrsta dálkinum í hnitanetinu, einnig er hægt að velja (eða afvelja) allar línur í hópi með því að velja gátreitinn í samsvarandi hauslínu hóps. Gátreiturinn í hauslínu hóps endurspeglar alltaf núverandi valstöðu lína í þeim hópi, burtséð frá því hvort allar línur séu valdar, engar línur séu valdar eða aðeins nokkrar línur séu valdar.

### <a name="hiding-column-names"></a>Fela dálkaheiti
Við flokkun gagna er sjálfgefið að hegðun sýni dálkheiti í hauslínu hóps. Hægt er að fela dálkheitið í hauslínu hóps með því að velja **Valkostir hnitanets** > **Fela dálkheiti hóps**.

### <a name="grouping-on-date-and-time-columns"></a>Flokkun á dálkum dagsetningar og tíma
Þegar þú flokkar á Date eða DateTime reiti hefurðu möguleika á að flokka eftir ári, mánuði eða degi. Hópurinn „gildi“ í samsvarandi hauslínu mun passa við sniðið úr þeim reit. Að auki, fyrir DateTime og Time reiti, geturðu flokkað eftir klukkustund, mínútu eða sekúndu.

> [!IMPORTANT]
> Notendur geta ekki bætt við flokkunardálki eins og er eftir að þeir flokka á hluta dagsetningar- eða tímadálks.

## <a name="freezing-columns"></a>Dálkar frystir
Sumir dálkar í hnitaneti gætu reynst það mikilvægir fyrir samhengi þannig að þú vilt ekki að þeir hverfi úr augsýn við flettingu. Þess í stað gætirðu viljað að gildin í þessum dálkum séu alltaf sýnileg. The **Frysting dálka í rist** eiginleiki veitir notendum þennan sveigjanleika. 

[![Frysta súlur í rist.](./media/gridFreezingColumns-07-25-2022.gif)](./media/gridFreezingColumns-07-25-2022.gif)

Til að festa dálk skal hægrismella í haus dálksins og síðan velja **Festa dálk**. Í fyrsta skipti sem þetta skref er gert verður valinn dálkur að fyrsta dálkinum og mun ekki lengur hverfa úr augsýn við flettingu. Næstu dálkum sem eru festir verður bætt hægra megin við síðasta festa dálkinn. Hægt er að nota venjulegu færsluaðgerðina til að endurraða festum dálkum eftir þörfum. Hins vegar er ekki hægt að færa festa dálka þannig að þeir birtist á meðal ófestra dálka. Að sama skapi er ekki hægt að færa ófesta dálka þannig að þeir birtist á meðal festra dálka.

Til að losa dálk skal hægrismella í haus fests dálks og síðan velja **Losa dálk**. 

Athugið að dálkval og línustaða dálka í nýja hnitanetinu eru alltaf fest sem fyrstu tveir dálkarnir. Þess vegna, þegar þessir dálkar eru teknir með í hnitaneti, verða þeir alltaf sýnilegir notanda, óháð láréttri flettistöðu í hnitanetinu. Ekki er hægt að endurraða þessum tveimur dálkum.

## <a name="autofit-column-width"></a>Aðlaga dálkbreidd sjálfkrafa
Eins og í Excel geta notendur þvingað dálk til að breyta stærð sjálfkrafa miðað við innihaldið sem er nú sýnt í honum. Tvísmelltu bara (eða tvísmelltu) á stærðarhandföngin í dálknum. Að öðrum kosti skaltu setja fókusinn í dálkhausinn og velja síðan **A** lykill (fyrir sjálfvirkt).

## <a name="frequently-asked-questions"></a>Algengar spurningar
### <a name="how-do-i-enable-the-new-grid-control-in-my-environment"></a>Hvernig virkja ég nýja netstýringu í umhverfi mínu? 

Eiginleikinn **Ný hnitanetsstýring** er í boði í eiginleikastjórnun í hvaða umhverfi sem er. Eftir að eiginleikinn í eiginleikastjórnun hefur verið virkjaður munu allar síðari notandalotur nýta sér nýju netstýringuna. 

Þessi eiginleiki byrjaði að vera virkur sjálfgefið í útgáfu 10.0.21. Stefnt er að því að verða lögboðin í október 2022.

## <a name="developer-opting-out-individual-pages-from-using-the-new-grid"></a>[Þróunaraðili] Afskrá einstaka síður frá því að nota nýja hnitanetið 
Ef fyrirtækið uppgötvar síðu sem á í vandræðum með að nota nýja hnitanetið, er API tiltækt til að leyfa einstökum skjámyndum að nota eldri netstýringu og leyfa á sama tíma öðrum hlutum kerfisins að nota nýju netstýringuna. Til að afskrá einstaka síður frá því að nota nýja hnitanetið, skal bæta við eftirfarandi kallskilaboðum `super()` í `run()` aðferð skjámyndarinnar.

```this.forceLegacyGrid();```

Þetta API verður að lokum úrelt til að gera kleift að fjarlægja eldri netstýringu. Hins vegar verður það tiltækt í að minnsta kosti 12 mánuði eftir að tilkynnt er um afskrift þess. Ef einhver vandamál krefjast þess að þetta API sé notað skal tilkynna um þau til Microsoft.

### <a name="forcing-a-page-to-use-the-new-grid-after-previously-opting-out-the-grid"></a>Að þvinga síðu til að nota nýja netið eftir að hafa áður afþakkað netið
Ef þú hefur valið að nota ekki einstaka síðu á nýja netinu gætirðu viljað virkja nýja netið aftur síðar eftir að undirliggjandi vandamál hafa verið leyst. Til að gera þetta þarftu einfaldlega að fjarlægja kallið við `forceLegacyGrid()`. Breytingin tekur ekki gildi fyrr en eitt af eftirfarandi gerist:

- **Endurvirkjun umhverfis**: Þegar umhverfi er uppfært og virkað að nýju er taflan sem geymir síðurnar sem hafa verið valdar úr nýja netinu sjálfkrafa hreinsuð út (FormControlReactGridState).
- **Handvirk hreinsun töflunnar**: Fyrir þróunaraðstæður þarftu að nota SQL til að hreinsa FormControlReactGridState töfluna og endurræsa síðan AOS. Þessi samsetning aðgerða mun endurstilla skyndiminni síðna sem hafa afþakkað nýja hnitið.

## <a name="developer-opting-individual-grids-out-of-the-typing-ahead-of-the-system-capability"></a>[Hönnuður] Að taka einstök rist út úr vélritun á undan kerfisgetu
Sumar aðstæður hafa komið upp sem henta ekki til að vinna vel með *Að slá á undan kerfinu* getu netsins. (Til dæmis, einhver kóði sem er ræstur þegar röð er staðfest veldur því að gagnauppspretturannsókn fer af stað og rannsóknin getur síðan spillt óbundnum breytingum á núverandi línum.) Ef fyrirtækið þitt uppgötvar slíka atburðarás er API tiltækt sem gerir þróunaraðili afþakkar einstaka töflu úr ósamstilltri röðarstaðfestingu og snýr aftur til eldri hegðunar.

Þegar ósamstilltur röð sannprófun er óvirkur í hnitaneti geta notendur ekki búið til nýja línu eða fært í aðra núverandi línu í hnitanetinu á meðan það eru löggildingarvandamál í núverandi línu. Sem fylgifiskur þessarar aðgerðar er ekki hægt að líma töflur úr Excel inn í fjármála- og rekstrarnet.

Til að afþakka einstaka töflu úr ósamstilltri röð staðfestingu skaltu bæta við eftirfarandi símtali á eftir`super()` í`run()` aðferð formsins.

```<gridControl>.allowPreemptiveClient(false);```

> [!NOTE]
> - Þetta símtal ætti aðeins að kalla fram í undantekningartilvikum og ætti ekki að vera viðmið fyrir öll net.
> - Við mælum ekki með því að þú breytir þessu API á keyrslutíma eftir að eyðublaðið er hlaðið.

## <a name="developer-size-to-available-width-columns"></a>[Þróunaraðili] Stækka breidd dálka eins og hægt er
Ef þróunaraðili stillir eiginleikann **WidthMode** á **SizeToAvailable** fyrir dálka innan nýja hnitanetsins, fá þessir dálkar upphaflega sömu breidd og þeir myndu fá ef eiginleikinn væri stilltur á **SizeToContent**. Hins vegar teygist á þeim þannig að þeir noti þá breidd sem í boði er innan hnitanetsins. Ef eiginleikinn er stilltur á **SizeToAvailable** fyrir marga dálka, deila allir þessir dálkar á milli sín aukalegri breidd sem er í boði innan hnitanetsins. Hins vegar, ef notandi breytir stærð einhverra þessara dálka, verður sá dálkur fastur. Hann heldur þeirri breidd og breikkar ekki lengur til að fylla upp í tiltæka breidd hnitanetsins.

## <a name="developer-specifying-the-column-that-receives-the-initial-focus-when-new-rows-are-created-by-using-the-down-arrow-key"></a>[Hönnuður] Tilgreinir dálkinn sem fær upphafsfókus þegar nýjar línur eru búnar til með því að nota örvatakkann niður
Eins og fjallað var um í [Mismunur þegar gögn eru slegin inn á undan kerfinu](#differences-when-entering-data-ahead-of-the-system) kafla, ef „Slá á undan kerfinu“ möguleikinn er virkur og notandi býr til nýja línu með því að nota **Ör niður** lykill, sjálfgefin hegðun er að setja fókusinn í fyrsta dálkinn í nýju röðinni. Þessi reynsla gæti verið frábrugðin upplifuninni í eldri töflunni eða þegar a **Nýtt** hnappur er valinn.

Notendur og stofnanir geta búið til vistaðar skoðanir sem eru fínstilltar fyrir gagnafærslu. (Til dæmis geturðu endurraðað dálkum þannig að fyrsti dálkurinn sé sá sem þú vilt byrja að slá inn gögn í.) Að auki, frá og með útgáfu 10.0.29, geta stofnanir breytt þessari hegðun með því að nota **selectedControlOnCreate()** aðferð. Þessi aðferð gerir forritara kleift að tilgreina dálkinn sem ætti að fá upphafsfókus þegar ný röð er búin til með því að nota **Ör niður** lykill. Sem inntak tekur þetta API stjórnauðkennið sem samsvarar dálknum sem ætti að fá upphafsfókusinn.

## <a name="known-issues"></a>Þekkt vandamál
Þessi hluti heldur lista yfir þekkt vandamál fyrir nýju hnitanetsstýringuna.

### <a name="open-issues"></a>Opin vandamál
- Þegar búið er að virkja eiginleikann **Ný hnitanetsstýring**, halda sumar síður áfram að nota núverandi netstýringu. Þetta gerist við eftirfarandi aðstæður:
 
    - Spjaldlisti er til á síðunni sem gefinn er upp í mörgum dálkum.
    - Flokkaður spjaldlisti er til á síðunni.
    - Dálkur hnitanets sem bregst ekki við stækkanlegri stýringu.

    Þegar notandi stendur í fyrsta skipti frammi fyrir þessum aðstæðum birtast skilaboð um að uppfæra skuli síðuna. Eftir að þessi skilaboð birtast mun síðan halda áfram að nýta núverandi hnitanet fyrir alla notendur fram að næstu uppfærslu afurðar. Betri meðhöndlun á þessum aðstæðum, svo hægt sé að nýta nýja hnitanetið, verður höfð í huga í framtíðaruppfærslu.

- [KB 4582758] Færslur eru óskýrar þegar verið er að breyta aðdrætti úr 100 í einhverja aðra prósentutölu

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

