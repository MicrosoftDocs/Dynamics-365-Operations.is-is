---
title: Búa til staðsetningarleiðbeiningar
description: Í þessu efnisatriði er útskýrt hvernig á að stofna staðsetningarleiðbeiningar. Staðsetningarleiðbeiningar eru notandaskilgreindar reglur sem hjálpa við auðkenningu tiltektar- og frágangsstaðsetninga fyrir birgðahreyfingar.
author: Mirzaab
manager: tfehr
ms.date: 07/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocDirTable, WHSLocDirHint, WHSLocDirTableUOM, WHSLocDirFailure
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-28
ms.dyn365.ops.version: Release 10.0.9
ms.openlocfilehash: 4f634b7f526fd198b394af6d3870c43ee560813e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016771"
---
# <a name="create-location-directives"></a>Búa til staðsetningarleiðbeiningar

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er útskýrt hvernig á að stofna staðsetningarleiðbeiningar. Staðsetningarleiðbeiningar eru notandaskilgreindar reglur sem hjálpa við auðkenningu tiltektar- og frágangsstaðsetninga fyrir birgðahreyfingar. Til dæmis, fyrir sölupöntunarfærslu, ákvarða staðsetningarleiðbeiningar hvar vörurnar verða tíndar og hvar tíndar vörur verða settar.

> [!NOTE]
> Athugasemd: Þetta efni á við aðgerðir í **Vöruhúsakerfi**. Það á ekki við um eiginleika í einingunni [Birgðastjórnun](../inventory/inventory-home-page.md).

Hægt er að nota staðsetningarleiðbeiningar til að framkvæma eftirfarandi verk:

- Frágangur varanna á innleið.
- Taka til og geyma vörur fyrri færslur á útleið.
- Sækja og setja hráefni fyrir framleiðslu.
- Fylla á staðsetningar.

## <a name="prerequisites"></a>Forkröfur

Áður en hægt er að stofna staðsetningarleiðbeiningu þarf að fylgja þessum skrefum til að ganga úr skugga um að forkröfur séu til staðar.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Vöruhús**.
1. Stofna vöruhús.
1. Í flýtiflipanum **Vöruhús** skal stilla valkostinn **Nota ferli vöruhúsastjórnunar** á *Já*.
1. Stofna staðsetningar, staðsetningargerðir, staðsetningarforstillingar og staðsetningarsnið. Frekari upplýsingar er að finna í [Skilgreina staðsetningar í vöruhúsi með vöruhúsakerfi](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).
1. Stofna svæði og svæðisflokka. Frekari upplýsingar er að finna í [Uppsetning vöruhúss](https://docs.microsoft.com/dynamics365/commerce/channels-setup-warehouse) og [Skilgreina staðsetningar í vöruhúsi með vöruhúsakerfi](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/tasks/configure-locations-wms-enabled-warehouse).

## <a name="setup"></a>Setja upp

### <a name="create-location-directives"></a>Búa til staðsetningarleiðbeiningar

Til að stofna staðsetningartilskipun, skal fylgja eftirfarandi skrefum.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.
1. Á listasvæðinu skal stilla reitinn **Gerð verkbeiðni** á þá gerð birgðafærslu sem verið að stofna staðsetningarleiðbeiningu fyrir.
1. Veldu **Ný** á aðgerðasvæðinu til að búa til staðsetningarleiðbeiningu.
1. Fyrir nýju staðsetningarleiðbeininguna skal stilla reitina eins og lýst er í eftirfarandi töflu.

    | Svæði | lýsing |
    |---|---|
    | Raðnúmer | Færið inn heiltölu sem gefur til kynna hvar í röðinni staðsetningarleiðbeiningin er. Hvar í röðinni segir til um hvenær unnið er úr hverri staðsetningarleiðbeiningu fyrir sig fyrir valda gerð verkbeiðni. |
    | Nafn | Færðu inn nafn á staðsetningarleiðbeiningunni. | 
    | Vinnugerð | Veldu gerð vinnunnar sem á að framkvæma. Listi yfir gildi fer eftir gerð birgðafærslu sem valin er í reitnum **Gerð verkbeiðni**. Eftirfarandi gildi gætu verið tiltæk:<ul><li>**Frágangur** – Staðsetningarleiðbeiningin reynir að finna bestu staðsetninguna til að staðsetja eða finna birgðir sem koma inn í kerfið við móttöku, framleiðslu eða leiðréttingu birgða. Staðsetningarleiðbeiningin er einnig notuð til að skilgreina afhendingarstaðsetningu fyrir geymslu eða útskot í verkflæði á útleið.</li><li>**Taka til** – Staðsetningarleiðbeiningin reynir að finna bestu staðsetningar til að taka frá efnislegar birgðir (stofna vinnu). Hægt er að ljúka tiltekt (þ.e. hægt er að losa vinnulínu tiltektar), jafnvel þótt vinnunni sé ekki lokið. Notandinn getur lokið efnislegri tiltekt. Í kerfinu er þessi aðgerð tiltektarskref. Notandinn getur síðan hætt við í fartækinu og lokið vinnunni (t.d. frágangi) seinna. Hins vegar er vinnuhausnum fyrst lokað þegar lokafrágangi er lokið.</li><li>**Talning** , **Leiðréttingar** , **Sérsnið** , **Breyting á birgðastöðu** , **Röðun númeraplötu** , **Prenta** , **Stöðubreyting** og **Pakka í faldaðar númeraplötur** - Hægt er að nota þessi gildi í hvaða uppsetningu staðsetningarleiðbeiningar sem er.</li></ul> |
    | Svæði | Veljið svæðið Þar sem ætti að ljúka við vinnuna. |
    | Vöruhús | Veljið vöruhúsastaðsetninguna þar sem á að klára vinnuna. |
    | Leiðbeiningarkóði | Veljið leiðbeiningarkóða til að leiða val á staðsetningarleiðbeiningum sem tengjast frágangslínum vinnusniðmáts þar sem þessum kóða er úthlutað. Á síðunni **Leiðbeiningarkóði** er hægt að búa til nýja kóða sem má nota til að tengja vinnusniðmát við staðsetningarleiðbeiningu. Einnig er hægt að nota þessa síðu til að koma á tengingu milli hvaða vinnusniðmátslínu sem er og staðsetningarleiðbeiningar (t.d. útskot eða geymslustað). Frekari upplýsingar um hvernig á að skilgreina leiðbeiningarkóða með vinnusniðmáti er að finna í [Stýra vöruhúsavinnu með vinnusniðmátum og staðsetningarleiðbeiningum](control-warehouse-location-directives.md).<p>Ef leiðbeiningarkóði er stilltur, þegar búa þarf til vinnu, leitar kerfið í staðsetningarleiðbeiningum eftir leiðbeiningarkóða í stað þess að leita eftir röð. Á þennan hátt er hægt að vera nákvæmari í sniðmáti staðsetningar sem er notað fyrir tiltekið skref í vinnusniðmáti, eins og skrefið fyrir geymslu á efni.</p> |
    | Ráðstöfunarkóði | Veljið ráðstöfunarkóða til að framsenda frágang móttekinna vara á staðsetningu. (Frekari upplýsingar er að finna í [Setja upp ráðstöfunarkóða](tasks/set-up-dispositions-codes.md).) Þessi reitur er aðeins í boði þegar reiturinn **Gerð verkbeiðni** er stilltur á *Innkaupapantanir* , *Vöruskilapantanir* eða *Frágangur á fullunnum vörum*. |
    | Margar birgðahaldseiningar | Stillið þennan valkost á *Já* til að nota margar birgðahaldseiningar á staðsetningu. Til dæmis verður þessi valkostur að vera stilltur á *Já* fyrir útskotið.<p>Ef valkosturinn **Margar birgðahaldseiningar** er stilltur á *Já* verður frágangsstaðsetningin tilgreind í vinnu (eins og búist er við). Hins vegar getur frágangsstaðsetningin aðeins höndlað frágang á mörgum vörum ef vinnan inniheldur margar birgðahaldseiningar sem þarf að taka til og ganga frá, ekki ef vinnan felur í sér aðeins eina birgðahaldseiningu sem þarf að ganga frá.</p><p>Ef valkosturinn **Margar birgðahaldseiningar** er stilltur á *Nei* , verður frágangsstaðsetningin eingöngu tilgreind ef frágangurinn er aðeins með eina gerð af birgðahaldseiningu.</p><p>Til að nota báðar aðferðirnar þarf að tilgreina tvær línur sem eru með sama skipulag og uppsetningu, en stilla valkostinn **Margar birgðahaldseiningar** á *Já* fyrir eina af línunum og *Nei* fyrir hinar. Með öðrum orðum, krafist er tveggja eins staðsetningarleiðbeininga fyrir frágangsaðgerðir, jafnvel þó að notandi þurfi ekki að greina á milli stakrar og margra birgðahaldseininga í vinnukenninu. Einnig þarf að setja upp staðsetningarleiðbeiningu fyrir tínslu, ef um er að ræða pöntun sem er með fleiri en eina vöru.</p><p>**Athugið:** Ef valkosturinn **Margar birgðahaldseiningar** er stilltur á *Já* fyrir staðsetningarleiðbeiningu af vinnugerðinni *Frágangur* , velur kerfið alltaf fyrstu línu staðsetningarleiðbeiningarinnar, óháð öðrum takmörkunum sem eru búnar til í línunum.</p> |

1. Valfrjálst: Á aðgerðasvæðinu skal velja **Breyta fyrirspurn** til að velja staði eða tilgreina allar takmarkanir sem gilda þegar þú velur ákveðna staðsetningarleiðbeiningu.
1. Í flýtiflipanum **Línur** skal stofna eina eða fleiri línur til að tilgreina einingar og til að finna eða taka frá magn í vöruhúsi.
1. Fyrir allar nýjar línur skal stilla reitina eins og lýst er í eftirfarandi töflu.

    | Svæði | lýsing |
    |---|---|
    | Raðnúmer | Færið inn heiltölu sem gefur til kynna hvar í röðinni staðsetningarleiðbeiningin er. Hvar í röðinni segir til um hvenær unnið er úr hverri staðsetningarleiðbeiningu fyrir sig fyrir valda vinnugerð. |
    | Frá-magn | Tilgreinið neðri mörk magnbilsins þegar á að velja röðina í miðjunni á hnitanetinu. Tilgreinið magnið í mælieiningunni sem er valin í reitnum **Eining**. |
    | Til magn | Tilgreinið efri mörk magnbilsins þegar á að velja röðina í miðjunni á hnitanetinu. Tilgreinið magnið í mælieiningunni sem er valin í reitnum **Eining**. |
    | Eining | Velja mælieiningu fyrir vörurnar.<p>Hægt er að tilgreina lágmarksmagn og hámarksmagn sem á að gilda fyrir leiðbeininguna. Einnig er hægt að tilgreina að nota eigi leiðbeininguna fyrir tiltekna birgðaeiningu. Reiturinn **Eining** er aðeins notaður fyrir magnáætlun.</p><p>Til að ákvarða hvort lína staðsetningarleiðbeiningar eigi við, mun kerfið meta magn með því að nota gildið **Eining** sem er tekið fram í línunni. Í hvert sinn sem farið er í línu staðsetningarleiðbeiningar mun kerfið reyna að umbreyta eftirspurnareiningunni í einingu sem er tilgreind í línunni. Ef umreikningur eininga er ekki til staðar, fer kerfið yfir í næstu línu.</p> |
    | Finna magn | Þessi reitur gildir aðeins þegar reynt er að ganga frá eða finna magn í vöruhúsinu. Með öðrum orðum gildir hann aðeins fyrir *Frágangsvinnu*. Veljið aðferðina sem er notuð til að meta hvort magnið er innan marka sem stillt er í reitunum **Frá magn** og **Til magn**. Ef staðsetningarleiðbeiningin er fyrir færslu á innleið skal velja einn af eftirfarandi valkostum:<ul><li>**Magn númeraplötu** ─ Til að meta hvort magn sé innan bilsins sem sóst er eftir, skal nota magnið í númeraplötunni sem verið er að taka á móti.</li><li>**Einingamælt magn** ─ Til að meta hvort magn sé innan bilsins sem sóst er eftir, skal nota magnið sem verið er að einingamæla við flutninginn. Til dæmis, í vöruhúsi, ef hægt er að taka á móti magni sem nemur 1000 og skipta því niður á 10 númeraplötur, sem hver fyrir sig er með magn sem nemur 100, er hægt að nota magn sem nemur 1000 vörum í stað númeraplötumagns upp á 100.</li><li>**Eftirstöðvar magns** ─ Til að meta hvort magn sé innan bilsins sem sóst er eftir, skal nota magnið sem á eftir að taka á móti í innkaupapöntunarlínunni sem er verið að athuga.</li><li>**Væntanlegt magn** ─ Til að meta hvort magn sé innan bilsins sem sóst er eftir, skal nota heildarmagnið í innkaupapöntunarlínunni, óháð magninu sem er þegar verið að taka á móti.</li></ul> |

1. Valfrjálst: Í flýtiflipanum **Línur** er hægt að stilla eftirfarandi viðbótarreiti.

    | Svæði | lýsing |
    |---|---|
    | Takmarka eftir einingu | Veljið þennan gátreit til að takmarka mælieiningar sem teljast gild valskilyrði fyrir línur staðsetningarleiðbeiningar. Þegar mælieiningar hafa verið tilgreindar, verða aðeins vörur, þar sem einingin samsvarar a.m.k. einni einingu sem er skilgreind fyrir röðunarflokk einingar, taldar gildar fyrir línuvalið.<p>Til dæmis takmarkast einingin við bretti og varan tengist röðunarflokk einingar sem inniheldur eininguna *bretti*. Í þessu tilviki verður litið á vörurnar sem gildan valkost fyrir staðsetningarleiðbeininguna.</p><p>Hins vegar stjórnar gátreiturinn **Takmarka eftir einingu** ekki einingunni eða einingunum sem eru notaðar í vinnulínum. Takmörkun einingar gildir aðeins um einingarnar sem eru gerðar tiltækar í gegnum röðunarflokk einingarinnar.</p><p>Til dæmis tengist vara röðunarflokki einingar sem inniheldur báðar einingarnar *bretti* og *stk*. Mælieining hefur verið skilgreind þar sem 1 bretti = 100 stk, og staðsetningarleiðbeiningin notar virknina **Takmarka eftir einingu** aðeins fyrir bretti. Ennfremur hefur vinnusniðmát verið skilgreint sem takmarkar stofnun vinnuhauss við 50 stk. Í slíku tilfelli verða vinnulínur með 50 stk. stofnaðar.</p><p>Til að tilgreina mælieiningu fyrir takmarkanir skal fylgja þessum skrefum</p><ol><li>Í flýtiflipanum **Línur** skal velja **Takmarka eftir einingu**. Þessi hnappur verður aðeins tiltækur eftir að gátreiturinn **Takmarka eftir einingu** er valinn í línunni og síðan velja **Vista**.</li><li>Í reitnum **Eining** skal velja mælieininguna til að takmarka eftir fyrir tiltektar- og frágangsferlin.</li></ol> |
    | Slétta upp í einingu | Veljið þennan valkost til að tilgreina hvort tiltekt á hráefni eigi að vera sléttuð upp í heila afgreiðslueiningu sem er tilgreind í reitnum **Takmarka eftir einingu**. Þetta reitur á aðeins við um tiltekt á hráefni og staðsetningarleiðbeiningar af gerðinni *Tiltekt*. |
    | Staðsetja umbúðamagn | Veljið þennan gátreit ef magn umbúðaeiningar er tilgreint á síðunni **Sölupöntun**. Ef þessi gátreitur er valinn, eru aðeins staðsetningarnar sem eru með þetta magn umbúðaeiningar valdar. |
    | Leyfa að skipta | Veljið þennan gátreit til að skipta magninu á mörgum stöðum. |
    | Sniðmát fyrir tafarlausa áfyllingu | Stofnið tengingu við áfyllingarsniðmát þannig að áfylling hefjist strax ef vörum er ekki úthlutað. Ef reiturinn er skilinn eftir auður, hefst vöruáfylling ekki fyrr en unnið hefur verið úr öllum línum staðsetningarleiðbeiningarinnar.<p>Þetta reitur er aðeins í boði fyrir valdar gerðir verkbeiðni þar sem áfylling er leyfð, eins og *Sölupantanir* og *Tiltekt hráefnis*.</p> |

1. Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Ný** til að velja staðsetninguna eða staðsetningarbil.
1. Reiturinn **Raðnúmer** sýnir röðina sem unnið verður úr staðsetningarleiðbeiningunni fyrir valda vinnugerð. Hægt er að breyta röðinni. Hins vegar skal fara varlega með raðnúmer fyrir aðgerðir í staðsetningarleiðbeiningum, því að aðgerðir í staðsetningarleiðbeiningum keyra alltaf í þessari röð.
1. Í reitinn **Heiti** skal slá inn heiti á aðgerð staðsetningarleiðbeiningar. Verið nákvæm svo það sé á hreinu hver aðgerðin er.
1. Valfrjálst: Smellið á **Breyta fyrirspurn** til að breyta staðsetningum vöruhúss og öðrum skilyrðum.
1. Valfrjálst: Hægt er að stilla eftirfarandi viðbótarreiti fyrir staðsetningarleiðbeiningu.

    | Svæði | lýsing |
    |---|---|
    | Notkun fastrar staðsetningar | Veljið hvaða staðsetningar staðsetningarleiðbeiningin á að taka til greina:<ul><li>**Fastar og lausar staðsetningar** - staðsetningarleiðbeiningin tekur tillit til allra staðsetninga.</li><li>**Aðeins fastar staðsetningar fyrir afurðina** - staðsetningarleiðbeiningin tekur aðeins tillit til fastra staðsetninga fyrir afurðir.</li><li>**Aðeins fastar staðsetningar fyrir afurðarafbrigðið** - staðsetningarleiðbeiningin tekur aðeins tillit til fastra staðsetninga fyrir afurðarafbrigði.</li></ul> |
    | Heimila neikvæðar birgðir | Veljið þennan gátreit til að heimila neikvæðar birgðir á staðsetningu tilgreint vöruhús. |
    | Runa virk | Veljið þennan gátreit til að nota runuvinnslustefnu fyrir vörur sem nota runur. Ef þessi gátreitur er valinn og reiturinn **Stefna** er stilltur á *Engin* fer kerfið yfir í næstu aðgerðarlínuna. |
    | Stjórnunarstefna | Veljið stefnuna sem staðsetningarleiðbeiningin á að nota:<ul><li>**Engin** – Engin stefna verður notuð.</li><li>**Jafna umbúðamagn** - Þessi aðferð athugar hvort staðsetning tiltektar hafi tilgreint umbúðamagn. Þessi aðferð gildir aðeins þegar reiturinn **Vinnugerð** er stilltur á *Tiltekt*.</li><li>**Sameina** - Þessi aðferð sameinar vörur í tiltekinni staðsetningu þegar líkar vörur eru þegar fyrir hendi. Þessi aðferð gildir aðeins þegar reiturinn **Vinnugerð** er stilltur á *Frágangur*. Í dæmigerðri uppsetningu fyrir frágang reynir kerfið að sameina fyrstu aðgerðarlínuna og síðan í annarri aðgerðarlínunni reynir það að ganga frá án sameiningar. Sameining á vörum gerir seinni tiltektir skilvirkari.</li><li>**Frátekt á FEFO-runu** - Þessi aðferð er notuð þegar birgðir eru staðsettar með lokadag runu og er úthlutað fyrir frátekningu á runu. Fyrst útrunnið - fyrst út (FEFO) frátektaraðferðin er einnig notuð þegar birgðir eru staðsettar með því að nota fyrningardagsetningu runu til viðbótar við lokadagsetningu. Aðeins er hægt að nota þessa aðferð fyrir vörur sem nota runu. Þessi aðferð gildir aðeins þegar reiturinn **Vinnugerð** er stilltur á *Tiltekt*. Þegar þessi aðferð er valin er öllum röðunum fyrirspurna fyrir rununúmer hnekkt sem eru notuð.</li><li>**Slétta upp í heila númeraplötu** - Þessi aðferð sléttar upp birgðamagnið þannig að það samsvari númeraplötumagninu sem er úthlutað á vörurnar sem þarf að taka til. Aðeins er hægt að nota þessa aðferð fyrir áfyllingargerð staðsetningarleiðbeininga og aðeins þegar reiturinn **Vinnugerð** er stilltur á *Tiltekt*.</li><li>**Tóm staðsetning með engin verk á innleið** - Þessi aðferð er notuð til að finna tómar staðsetningar. Staðsetning er talin tóm ef hún hefur engar efnislegar birgðir og enga væntanlega vinnu á innleið. Þessi aðferð gildir aðeins þegar reiturinn **Vinnugerð** er stilltur á *Frágangur*.</li></ul> |

## <a name="example-of-the-use-of-location-directives"></a>Dæmi um notkun staðsetningarleiðbeiningar

Í þessu dæmi skal íhuga innkaupapöntunarferli þar sem staðsetningarleiðbeiningar verða að finna lausa afkastagetu í vöruhúsi fyrir birgðavara sem hafa einungis verið skráð í móttökusvæðinu. Fyrst þarftu að finna laust pláss innan vöruhússins með því að sameina við fyrirliggjandi lagerbirgðir. Ef sameining er ekki möguleg, þarftu að finna tóma staðsetningu.

Fyrir þessa atburðarás verður þú að skilgreina tvær aðgerðir staðsetningarleiðbeiningar. Fyrsta aðgerð í röðinni verður að nota í **Sameina** stjórnunarstefnu og annar ætti að nota í **Autt staðsetning með engu verki á innleið** stjórnunarstefnu. Nema þú skilgreinir þriðju aðgerð til að meðhöndla aðstæður yfirflæðis eru tvær niðurstöður mögulegar þegar engin afkastageta er í vöruhúsinu: hægt er að stofna vinnu jafnvel þótt engin staðsetningar eru skilgreindar eða ferli verkstofnunar getur mistekist. Niðurstaðan er ákvarðaður með uppsetningu á **staðsetningarleiðbeiningum** síðuna, þar sem hægt er að ákveða hvort að velja **Stöðva vinnu á misheppnuðum staðsetningarleiðbeiningum** valkost fyrir hverja gerð vinnupöntunar.

## <a name="next-step"></a>Næsta skref

Eftir að þú stofnar staðsetningarleiðbeiningar getur þú tengir hvert tilskipunarkóða með vinnusniðmátskóða fyrir vinnusköpun. Frekari upplýsingar er að finna í [Stýra vöruhúsavinnu með vinnusniðmátum og staðsetningarleiðbeiningum](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/control-warehouse-location-directives).

## <a name="technical-information-for-system-admins"></a>Tæknilegar upplýsingar sem eru ætlaðar kerfisstjórum

Ef notandi ekki aðgang að síðum sem notaðar eru til að ljúka þessu verki, skal hafa samband við kerfisstjóra og veita upplýsingar sem er sýndar í eftirfarandi töflu.

| Tegund | Skilyrði |
|---|---|
| Skilgreiningarlyklar | Opnið **Kerfisstjórnun \> Setja upp \> Skilgreining leyfis**. Útvíkkið leyfislykillinn **Viðskipti** og veljið síðan skilgreinarlykilinn **Vöruhúsakerfi og flutningsstjórnun**. |
