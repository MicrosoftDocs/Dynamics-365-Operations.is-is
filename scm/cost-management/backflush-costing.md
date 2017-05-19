---
title: "Bakfærslukostnaðaraðferð"
description: "Þetta efnisatriði kynnir til sögunnar hugtakið bakfærslukostnaðaraðferð sem er notað fyrir lean-framleiðslu."
author: YuyuScheller
manager: AnnBe
ms.date: 04/10/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LeanCosting, LeanCostingTimeBucket
audience: Application User
ms.reviewer: annbe
ms.search.scope: Operations, Core
ms.custom: 272063
ms.assetid: 62a2a7da-ff79-49bf-a6e8-29460ba5252f
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: conradv
ms.dyn365.ops.intro: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 35e202db8042eaed2cfab200cc43810bba14cc87
ms.contentlocale: is-is
ms.lasthandoff: 04/25/2017


---

# <a name="backflush-costing"></a>Bakfærslukostnaðaraðferð

[!include[banner](../includes/banner.md)]


Þetta efnisatriði kynnir til sögunnar hugtakið bakfærslukostnaðaraðferð sem er notað fyrir lean-framleiðslu. 

Kostnaður fyrir Lean-framleiðslu gerir framleiðsluflæðinu aðferð fyrirtækjasamstæðum sem er lagt til backflush kostnaðarútreikning. Í bakfærslukostnaðaraðferð er beinum efnum sem notuð eru safnað upp í kostnaðarlykil verks í vinnslu (VÍV) í framleiðsluflæðinu. Birgðalíkanaflokkur staðalkostnaðar er notaður. Vörur sem eru fengnar úr framleiðsluflæðinu eru dregnar frá VÍV á staðalkostnaðarverði þeirra. Meginmunur á bakfærslukostnaðaraðferð og staðalkostnaði er að fyrir bakfærslukostnaðaraðferð eru frávik ekki reiknuð fyrir hvert kanban eða tilbúna afurð. Þess í stað eru frávik reiknuð eftir framleiðsluflæði yfir tímabil. Þessi aðferð kynnir sannarlega lean-hugtak til að skrá efnisnotkun. Sérnýtt tiltekið magn efnisins er ekki skráð í kanban- eða framleiðslupöntun. Þess í stað eru fullar runur eða afgreiðslueiningar stigskiptar í framleiðsluflæðinu. Eftir að runur eða afgreiðslueiningar eru skráðar sem auðar eru þær skilgreindar sem notaðar. Hugsanlegt er að nota ítarlega notkun notuð eftir því hver [skilgreining framleiðsluflæðisins er](http://ax.help.dynamics.com/en/wiki/lean-manufacturing-modeling-the-lean-organization/). Áður en hægt er að nota ítarlega notkun verða fyrirtæki að leyfa sjálfumsér að láta efni hverfa í VÍV-framleiðsluflæðinu. Reglubundin bakfærslukostnaðaraðferð ákvarðar virk gildi VÍV til loka tímabils. Þessi ákvörðun byggist á kanban-afgreiðslueiningum og stöðu kanban-vinnslu. Frávik milli virkra gilda og raungilda VÍV eftir kostnaðarflokki og vöru eru gjaldfærð og sýnd sem frávik.

## <a name="configuring-backflush-costing"></a>Grunnstilling bakfærslukostnaðaraðferðar
Til að virkja kostnaðarútreikning verður að ljúka eftirfarandi uppsetningu:

-   **Setja upp VÍV-reikningar fyrir framleiðsluflokk og framleiðsluflæði.** Vív-lyklar fyrir framleiðsluflæði eru tilgreindir í framleiðsluflokknum. Framleiðsluflæði bakfærslukostnaðaraðferðar reiknar frávik sem mismun á VÍV-gildi fyrir og eftir að bakfærslukostnaðaraðferð er framkvæmd fyrir hvert framleiðsluflæði. Þess vegna er mælt með að VÍV-reikningur sé stofnaður fyrir hvert framleiðsluflæði.
-   **Úthlutun kostnaðartegundar á tilfangaflokk.** Úthluta verður kostnaðartegund á tegund keyrslutíma fyrir vinnureitinn. Til að ákvarða frávik eftir verkþætti þarf að stofna kostnaðartegund fyrir hvern vinnureit. Kostnaðartegundir fyrir uppsetningu og magn eru ekki teknar með í kostnaðarútreikningi fyrir lean-framleiðslu. VÍV-reikningar fyrir hvern flokk tilfanga eru hunsaðir í bakfærslukostnaðaraðferði. Fyrir útselda verkþætti er engin kostnaðartegund nauðsynleg. Kostnaðarflokkur sem er úthlutað á virka þjónustu er notaður í staðinn.
-   **Úthluta kostnaðarflokkum.** Til að leyfa sundurliðun kostnaðarframlegðar í framleiðsluflæði, verður að úthluta kostnaðarflokkum eftir kostnaðarflokksgerð:
    -   **Kostnaðarflokkur beins efnis** - Beint efni krefst kostnaðarflokks sem auðkennir efnistegund fyrir kostnað. Kostnaðarflokkurinn virkjar uppsafnað yfirlit yfir kostnað, VÍV og frávik eftir beinu efni.
    -   **Kostnaðarflokkur beinnar framleiðslu** - Kostnaðarflokkur beinnar framleiðslu nær yfir framlag beins kostnaðar rekstrartilfanga í framleiðsluflæðinu. Þessi kostnaðarflokkur gerir kleift uppsafnað yfirlit yfir kostnað, VÍV og frávik eftir kostnaði beinnar framleiðslu.
    -   **Óbeinn kostnaðarflokkur** - Óbeinn kostnaðarflokkur er nauðsynlegur til þess að reikna út framlag óbeins kostnaðar til framleiðsluflæðisins. Þessi kostnaðarflokkur virkjar uppsafnað yfirlit yfir kostnað, VÍV og frávik eftir óbeinum kostnaði.
    -   **Kostnaðarflokkur beinnar útvistunar** - Kostnaðarflokkur fyrir þjónustur virkjar uppsafnað yfirlit yfir úthlutuðan kostnað og VÍV og ákvarðar kostnaðarfrávik útseldrar þjónustu.
    -   **Kostnaðarflokkur fyrir endanlega vöru** - Fullunnar vörur þarfnast kostnaðarflokks sem auðkennir afurðategund fyrir kostnað. Þessi kostnaðarflokkur virkjar uppsafnað yfirlit yfir kostnað, VÍV og frávik eftir afurðategund. Staðlaður kostnaður fyrir vörur er reiknaður með því að nota kostnaðarútreikning sem er byggður á uppskrift (BOM) og annaðhvort framleiðsluflæði og kanban-reglum eða leið.

### <a name="costing-sheet"></a>Kostnaðarskjöl

Kostnaðarskjalið virðislíkön skipulag kostnaðar fyrir fyrirtækið og er byggt upp af kostnaðarflokkum til að flokka kostnað. Kostnaðarskjalið hefur mismunandi skjámyndir. Hún sýnir kostnaðarupplýsingar eftir því skipulagi sem er hannað í því. Í kostnaðarskjalinu er einnig skilgreind formúla sem er notuð til að reikna út óbeinan kostnað. Útreikningsjafna getur byggst á magni, þyngd, rúmmáli eða gildi.

-   **Skilgreina kostnaðarútgáfu.** Í kostnaðarútgáfunni skilgreinir fyrirtækið hvernig viðhalda eigi kostnaði. Kostnaðarútgáfa getur innihaldið færslur staðalkostnaðar eða áætlaðs kostnaðar sem eru byggðar á kostnaðargerðinni sem er úthlutað á kostnaðarútgáfuna. Sú kostnaðarútgáfa sem er notuð fyrir kostnað fyrir lean-framleiðslu verður að byggja á staðalkostnaði.
-   **Úthluta birgðalíkanaflokki á losaðar vörur.** Allar vörur sem eru tengdar framleiðsluflæðinu verður að úthluta í birgðalíkanaflokk sem notar birgðalíkanaflokkinn **Staðalkostnað**. Staðalkostnaði er viðhaldið fyrir hvert svæði og virkjunardagsetningu. Fyrir afurðarsniðmát er hægt að velja birgðalíkanaflokk ef kostnaði er viðhaldið á hverja vöruvíddasamsetningu eða afurðarsniðmát.
-   **Samkvæmt skilgreiningu er útseld þjónusta ekki birgðaþjónusta.** Útseldir verkþættir hafa engan birgðalíkanaflokk. Til að kostnaðarfæra útseldan verkþátt rétt verður að passa að þjónustuverkþátturinn tilheyri birgðalíkanaflokki þar sem birgðastefnan er stillt á **Vara í birgðum = Rangt**.

Fyrir úttaksvörur krefst kostnaðarútreikningur sem er byggður á framleiðsluflæðinu að staðalkostnaði sé viðhaldið fyrir þjónustu sem er tengd útseldum verkþáttum. Kostnaðarflokkur sem er úthlutað til þjónustu er notaður til að ákvarða kostnaðarfrávik útselds verkþáttar.

## <a name="cost-calculation-for-lean-manufacturing"></a>Kostnaðarútreikningur fyrir lean-framleiðslu
Fyrir vörur sem eru gefnar upp utan framleiðsluflæðis verður að byggja uppskriftarútreikninginn á leiðarútgáfu eða framleiðsluflæði. Uppskriftarútreikningurinn reiknar út kostnað vöru og tengda sundurliðun tilfanga og efnis sem nauðsynleg eru til að búa til vöru. Frádráttur frá VÍV-reikningi fyrir framleiðsluflæðið er gerður með því að nota niðurbrot afurðar eftir vöru- og kostnaðarflokki.

### <a name="calculation-that-is-based-on-the-production-flow"></a>Útreikningur sem er byggður á framleiðsluflæðinu

Lean-framleiðsla fyrir Microsoft Dynamics 365 for Operations er óháð leiðum. Kostnaðarútreikningur fyrir vörur sem eru gefnar úr framleiðsluflæðinu getur verið byggður á sjálfu framleiðsluflæðinu. Áður en hægt er að framkvæma útreikning verður að stofna kanban-reglu sem sér fyrir afurðinni utan framleiðsluflæðis. Ef hægt er að veita vöru úr mörgum framleiðsluflæðum á sama svæði á dagsetningu útreiknings er hægt að velja framleiðsluflæði fyrir útreikning Uppskriftar. Á síðunni **Sjálfgefið framleiðsluflæði** er hægt að skilgreina sjálfgefið framleiðsluflæði fyrir hverja vöru. Ef margar kanban-reglur eru til fyrir sömu afurð í sama framleiðsluflæðinu sem er virkt á dagsetningu útreiknings velur útreikningurinn fyrstu kanban-regluna sem er virk fyrir útreikninginn.

### <a name="calculation-that-is-based-on-the-route"></a>Útreikningur sem er byggður á leiðinni

Útreikningur sem er byggður á leið gildir sem útreikningur sem byggist á framleiðsluflæðinu. Hins vegar notar útreikningur sem er byggður á leið ekki kostnaðarútreikning fyrir virkni lean-framleiðslu. Leiðin á að nota tilfangaþörf fyrir tilfangaflokka. Til að forðast kerfisbundin frávik ætti hún einnig að nota sömu vinnureiti eða a.m.k. sömu kostnaðartegundir. Aftur ætti að forðast kostnaðartegundir fyrir uppsetningu og magn. Þær hjálpa ekki til við að reikna út kostnaðinn í grófara niðurbrot en bakfærslukostnaðaraðferð lean-framleiðslu. Til að ákvarða hvaða valmöguleika (framleiðsluflæði eða leið) ætti að nota til að reikna út kostnað, skal hafa í huga niðurstöður sundurliðunar kostnaðar. Útgáfan sem er nær stöðu og framleiðir færri frávik í heildina er betri valkosturinn. Í umhverfi lean-framleiðslu þar sem vara er úr einu framleiðsluflæði og einni kanban-reglu er útreikningur sem er byggður á framleiðsluflæðinu sennilega nákvæmari. Fyrir vöru sem er til hjá lean-framleiðslu og sölupantanir á sama svæði, eða sem getur haft mörg framleiðsluflæði eða margar kanban-reglur í sama flæði, gæti útreikningur verið nákvæmari ef hann er byggður á leiðarútgáfu sem er sérstaklega byggð upp fyrir útreikning kostnaðar, ekki fyrir framleiðsluna. Framleiðsluflæði verður að vera notað við útreikning vara sem eru tengdar undirverktaka. Í Microsoft Dynamics 365 for Operations nota kostnaðarlíkön fyrir undirverktaka í framleiðslupöntun og úthýsing í lean-framleiðslu tvær mismunandi nálganir. Lean-framleiðsla kynnir nýjan gerð kostnaðarflokks, **Beina úthýsingu**, til að reikna út útselda þjónustu.

## <a name="material-consumption"></a>Efnisnotkun
Þegar efni er notað úr birgðum í VÍV er kostnaði við efni bætt við VÍV á raunverulegum staðalkostnaði fyrir kostnaðarflokk. Þessi aðgerð á sér stað við eftirfarandi kringumstæður:

-   Kanban-úthreyfingar eru bókaðar fyrir kanban-tiltektarlínur sem uppfæra birgðir.
-   Flutningsvinnslum er lokið sem uppfæra birgðir við tínslu en ekki móttöku (Flutningur efnis úr birgðum í VÍV).

## <a name="receiving-products-from-the-production-flow"></a>Taka á móti vörum frá framleiðsluflæðinu
Vörur eru mótteknar úr framleiðsluflæðinu við eftirfarandi kringumstæður:

-   Ferlisvinnslum er lokið sem hafa **Uppfærslu birgða við móttöku** stillt **Já**.
-   Ferlisvinnslum er lokið sem uppfæra birgðir við móttöku, en sem hafa **Uppfærsla birgða við tiltekt stillta** á **Nei** (Færa úr VÍV í birgðir). Þessi valkostur gerir kleift að móttaka allar vörur utan framleiðsluflæðis óháð skilgreiningu Uppskriftar og leiðar. Ferlið fylgir aðeins efnislegu flæði. Þessi valkostur hentar sérstaklega fyrir móttöku hliðarafurða, aukaafurða eða rýrnunar utan framleiðsluflæðis og til að leiðrétta kostnaðarstöðu VÍV framleiðsluflæðis samkvæmt því.

Vörur sem eru fengnar úr framleiðsluflæðinu eru dregnar frá VÍV.

## <a name="products-in-wip"></a>Afurðir í VÍV
VÍV líkan fyrir lean-framleiðslu í Microsoft Dynamics 365 for Operations gerir kleift að nota stöðu efnismeðhöndlunareiningar kanbans til að stýra hráefni, hálfkláruðum afurðum og tilbúnum afurðum sem eru hluti af VÍV.

-   **Úthlutað** - Kanban getur haft notað efni sem er gjaldfært í VÍV.
-   **Móttekið** - Ef kanban sem vísar til síðasta verkþáttar þar sem **Uppfærsla birgða á kvittun** er stillt á **Nei**, sýnir hún fulla afgreiðslueiningu afurðar eða hálfkláraðrar afurðar sem eru ekki skráð í birgðir.

Athugið að efnið í VÍV er ekki sýnilegt í yfirliti yfir birgðir á lager. Það er hins vegar er sýnilegt í yfirlitum yfir kanban-magn.

## <a name="consuming-products-in-wip"></a>Notkun afurða í VÍV
Afurðir í VÍV eru notaðar þegar samsvarandi kanban-afgreiðslueiningar eru tæmdar. Autt kanban-merki framleiðir ekki virka kostnaðarfærslu en tekur gildi þegar næsta bakfærslukostnaðaraðferð er keyrð. Tæmdar kanban-afgreiðslueiningar eru ekki lengur gjaldfærðar sem á lager og þess vegna reiknaðar sem notaðar innan þess tímabils.

### <a name="automatic-empty-registration"></a>Sjálfvirk auð skráning

Áætluð eða tilvikskanban er hægt að stilla á sjálfvirka auða skráningu í kanban-reglunni:

-   **Þegar tekið er á móti afgreiðslueiningum** - Sjálfgefið er að fyrir áætluð kanban er efnið skilgreint sem nota á þegar síðustu vinnslu fyrir kanban er lokið. Fyrir kanban í föstu magni er aðeins mælt með þessum valkosti fyrir kanban í stakri körfu kanbans þar sem það skilkar kortinu í uppruna eftirspurnar í hvert sinn sem kanban er móttekið á síðasta áfangastað.
-   **Þegar upprunaþörfn er skráð** - Þessi valkostur er aðeins tiltækur fyrir tilvikskanban og er sjálfgefin stilling fyrir þau. Þessi valkostur er gagnlegur í tengslum við VÍV til að halda VÍV hreinu, þar sem kanban fyrir íhluti í VÍV eru sjálfkrafa tæmd og þar af leiðandi notuð af VÍV, þegar yfirkanbanið er útbúið.

Að lokum er hægt að úthluta kanban-afgreiðslueiningum (= í vinnslu,) móttekið (= allur), eða tæmd. Það er engin hlutfallsleg tæming. Þar af leiðandi til að virkja nákvæman skráningu notkun, er mikilvægt að takmarka magn vöru í kanban þannig að þær séu lægri en notkun á hvert tímabil. Vörur sem eru færðar yfir í vinnslusalinn í stórum runum sem ná yfir dagar eða vikur eftirspurnar ætti ekki að nota í VÍV. Í staðinn ætti að geyma þessar afurðir í birgðum.

## <a name="backflush-costing"></a>Bakfærslukostnaðaraðferð
Það ætti að keyra bakfærslukostnaðaraðferð til að meta VÍV reglubundið VÍV og framleiða stöðu við lok tímabils sem reiknar frávik á efni, vinnu og óbeinan kostnað. Útreiknuð frávik eru bókuð í frávikalykla. Í ferli bakfærslukostnaðaraðferðar eru öll framleiðsluflæði lögaðilans notuð í sömu runukeyrslu. Þegar bakfærslukostnaðaraðferð er keyrð í runuvinnslu gæti vinnsla verið margþrædd með framleiðsluflæðinu. Tímabil bakfærslu er skilgreint með lokadagsetningu. Ekki er hægt að bóka færslur á dagsetningu þegar útreikningur bakfærslukostnaðaraðferðar hefur verið keyrður. Aldrei skal keyra bakfærslukostnaðaraðferð á gildandi dagsetningu áður en dagurinn er raunverulega liðinn. Bakfærslukostnaðaraðferð framkvæmir eftirfarandi skref.

1.  Ákvarðar ónotaðað magn í framleiðsluflæðinu frá lokadagsetningu tímabils. Eftir að bakfærslukostnaðaraðferð hefur verið keyrð er hægt að skoða ónotað magn á keyrsludagsetningu kostnaðarútreiknings í svarglugganum **Ónotað magn**.
2.  Reikna út nettó raunverulega notkun á framleiðsluflæðinu yfir tímabil.
3.  Hreinsa VÍV úr raunverulegri notkun og vörum.
4.  Reikna út framleiðslufrávik í staðlaðan kostnað fyrir tímabilið. **Fyrir notaða íhluti fyrir tímabilið:**
    -   Uppfæra fjárhagslega nettó raunverulegt magn efnis sem framleiðsluflæðið notaði yfir tímabil. Kerfið vinnur í fyrstu í, fyrst út (FIFO) röð á færslunum einstaka birgðirnar til að uppfæra fjárhagslega efnislega uppfærðar færslur fyrir framleiðsluflæðið, þar til að nettó innleystu magni fyrir tímabil er náð.
    -   Færslum er fjárhagslega skipt til að varpa nákvæmu notuðu magni.
    -   Ónotað magn í VÍV framleiðsluflæðis er áfram í efnislega uppfærðri stöðu.

    **Fyrir lokið magn framleiðslu fyrir tímabil:**
    -   Uppfæra fjárhagslega birgðahreyfingar fyrir lokið magn fyrir tímabil.

    **Fyrir umbreytingarkostnað:**
    -   Notaðar umreikningskostnaðarfærslur (leiðarfærslur) sem voru skráðar fyrir tímabilið eru fjárhagslega uppfærðar.
    -   Allur beinn framleiðslukostnaður er fjárhagslega uppfærður. Öllum kanban-ferlisvinnslum sem er lokið á tímabilinu er safnað upp.
    -   Allur óbeinn kostnaður sem er reiknaður fyrir notað efni innan tímabilsins er reiknaður út og dreginn frá VÍV. Eftirstandandi óbeinn kostnaður er bókaður sem frávik.

5.  Reikna út framleiðslufrávik í staðlaðan kostnað. Frávikið er reiknað fyrir hvern kostnaðarflokk.






