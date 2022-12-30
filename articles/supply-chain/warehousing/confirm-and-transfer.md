---
title: Staðfesta og flytja
description: Í þessari grein útskýrt hvernig á að nota eiginleikann „Staðfesta og flytja“, sem gerir notendum kleift að senda farma úr vöruhúsinu áður en allri vinnu er lokið sem tengist þessum förmum.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLoadTemplate,WHSWorkTemplateTable,WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 9257d8f9e6ed62ac0b19b0cdc8fd858e8b2f97a3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900565"
---
# <a name="confirm-and-transfer"></a>Staðfesta og flytja

[!include [banner](../includes/banner.md)]

Eiginleikann *Staðfesta og flytja* gerir notendum kleift að senda farma úr vöruhúsinu áður en allri vinnu er lokið sem tengist þessum förmum. Þegar sending sem inniheldur farmlínur sem voru ekki teknar til að fullu er móttekin, er notandinn sem á að staðfesta beðinn um annaðhvort að skipta eftirstandandi magni niður á nýjan farm eða að hætta við óklárað magn.

Kerfi sem eru sett upp til að heimila að skipta upp farmi styðja aðstæður þar sem aðlaga þarf hleðslur, sem hafa verið áætlaðar eða hlaðnar að hluta til, út af nýjum eða breyttum kringumstæðum.

Biðlarinn inniheldur rök sem gerir kleift að loka og staðfesta hlutahleðslur sem sendar. Allar eftirstandandi sendingar og farmlínur (þar með talið fullt magn og hlutamagn) eru þá færðar yfir í nýlega stofnaðan farm og sendingu, ef þessi yfirfærsla er nauðsynleg og uppsetningin heimilar hana. Nýjar sendingar og farmar eru stofnuð sjálfkrafa samkvæmt upprunalegu skilyrði sendingar og stofnunar farms og aðaleigindir þeirra haldast óbreyttar. Einnig er hægt að sjálfkrafa hætta við eftirstandandi magn ef verkbeiðni hefur ekki enn verið stofnuð og notandi telur þessa afturköllun óhjákvæmilega.

Þessi virkni styður aðstæður þar sem heildarfarmurinn passar ekki í einn flutningabíl, eða þar sem hluti farmsins á að fara úr vöruhúsinu áður en afgangur farmsins er tilbúinn undir sendingu. Í þessum aðstæðum er hægt að flytja eftirstandandi afurðir á nýjan farm og þar af leiðandi í nýjan flutningabíl. Vegna þess að hægt er að nota þennan eiginleika með förmum sem alla jafna krefst sendingar á heilum farmi, veitir hann aukinn sveigjanleika þannig að umsjónaraðilar flutninga geta leyst úr óhefðbundnum og ófyrirsjáanlegum aðstæðum.

Þegar farmi er skipt framkvæmir eiginleikinn *Staðfesta og flytja* eftirfarandi aðgerðir:

- Nýir farmar og sendingar eru stofnaðar þegar á þarf að halda. Hver farmur eða sending verður að mestu með sömu eigindir og upprunalegi farmurinn eða sendingin. Að undanskilinni farmstöðunni, sem verður endurreiknuð út frá verkstöðunni.
- Notandi er látinn vita að nýr farmur hafi verið búinn til. Notanda er einnig tilkynnt um auðkenni nýja farmsins.
- Farmlínurnar, verkhausarnir og vinnulínurnar sem skipt var upp eru uppfærð með nýju farm- og sendingarupplýsingunum.
- Ef verið er að skipta upp heilli sendingu er sendingunni viðhaldið og aðeins farmtilvísanir eru uppfærðar. Ef skipta þarf sendingunni er ný sending stofnuð.

Þegar hætt er við eftirstandandi magn er allt magn farmlínu, sem ekki hefur verið tínt og er ekki með óafturkallanlega vinnu tengda, fjarlægt úr farminum. Ef eitthvað verk er í vinnslu, getur notandinn aðeins skipt farminum. Ekki er hægt að hætta við eftirstandandi magn.

Aðeins er hægt að skipta upp farmi sem uppfyllir öll eftirfarandi skilyrði:

- Ein eða fleiri farmlínur eru með tínt magn.
- Hleðslustaðan er minni en það sem hlaðið er.
- Engin farmlínugögn eru til. (Þessi gögn eru stofnuð í gegnum sameiningu númeraplötu á geymslustaðsetningu og eiginleikinn Staðfesta og flytja styður ekki sameiningu númeraplötu.)
- Engar birgðir bíða pökkunar á pökkunarstaðsetningu sem stendur. (Eiginleikinn *Staðfesta og flytja* styður ekki birgðir sem hafa verið tíndar yfir á pökkunarstöðina en hefur ekki verið pakkað ennþá nema ef gámar sem hafa verið pakkaðir eru staðsettir á geymslustaðsetningum með hleðsluvinnu stofnaða.)

> [!NOTE]
> Þessi virkni er frábrugðin virkni farmflutnings, sem ætti að nota í vöruhúsum sem geta aldrei áætlað og búið til farm á undan tiltekt, en í staðinn hlaða tiltækt flutningspláss eftir að tiltekt lýkur.
>
> Notið eiginleikann *Staðfesta og flytja* í aðstæðum þar sem farmar eru venjulega áætlaðir og búnir til fyrir tíma, en þar sem undantekningar koma stundum fyrir þar sem farmurinn passar ekki í tiltækan flutning (t.d. í flutningabíl).

## <a name="turn-the-confirm-and-transfer-feature-on-or-off"></a>Kveikir eða slekkur á staðfestingar- og flutningseiginleikanum

Til að nota virknina sem lýst er í þessari grein þarf að kveikja á eiginleikanum *Staðfesta og flytja* fyrir kerfið. Frá og með útgáfu 10.0.25 af Supply Chain Management er þessi eiginleiki skylda og ekki er hægt að slökkva á henni. Ef þú ert að keyra útgáfu sem er eldri en 10.0.25, þá geta stjórnendur kveikt eða slökkt á þessum eiginleika með því að leita að eiginleikanum *Staðfesta og flytja* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

## <a name="set-up-confirm-and-transfer"></a>Setja upp staðfesta og flytja

Til að nota eiginleikann *Staðfesta og flytja* þarf að kveikja á honum í öllum hleðslusniðmátum sem eiga við. Það fer eftir þörfum, en að auki gæti verið gott að undirbúa vinnusniðmátin til að styðja við eiginleikann. Ef á að vinna í gegnum sýniaðstæðurnar sem boðið er upp á seinna í þessari grein, skal setja kerfið eins og lýst er í þessum hluta. (Þessar aðstæður byggja á **USMF** sýnigögnum.)

### <a name="prepare-your-load-templates"></a>Undirbúið hleðslusniðmátin

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Farmur \> Hleðslusniðmát**.
1. Á aðgerðasvæðinu skal velja **Breyta** til að færa síðuna yfir í breytingastillingu.
1. Veljið gátreitinn **Leyfa skiptingu farmlínu við staðfestingu sendingar** fyrir hvert sniðmát sem til er þar sem á að kveikja á eiginleikanum. Önnur leið er að velja **Nýtt** til að stofna nýtt sniðmát og skilgreina það eftir þörfum. Sérhver farmur sem er stofnaður með því að nota þetta sniðmát mun erfa þessa virkni. (Ef unnið er með **USMF** sýnigögnin, skal kveikja á eiginleikanum fyrir hleðslusniðmátið **20 feta gámur**.)

### <a name="prepare-your-work-templates"></a>Undirbúið vinnusniðmátið

Þessi uppsetning er ekki nauðsynleg í öllum aðstæðum. Dæmið sem hér er sýnt tryggir að hægt sé að skipta verki eftir sendingu til að styðja sýniaðstæðurnar sem boðið er upp á seinna í þessari grein. Einnig eru aðrar leiðir til að ná þessari útkomu.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.
1. Í hnitanetinu í efri hluta síðunnar skal velja fyrirliggjandi vinnusniðmát þar sem á að setja upp eiginleikann *Staðfesta og flytja*. (Ef unnið er með **USMF** sýnigögnin skal velja vinnusniðmátið **51 Tína fyrir geymslustað**.) Annars skal stofna nýtt vinnusniðmát.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn** til að opna svargluggann **Sala**.
1. Í svarglugganum **Sala**, í flipanum **Röðun**, skal velja **Bæta við** til að bæta línu við hnitanetið.
1. Í nýju línunni skal stilla eftirfarandi gildi:

    - **Tafla:** *Tímabundnar vinnufærslur*
    - **Afleidd tafla:** *Tímabundnar vinnufærslur*
    - **Reitur:** *Auðkenni sendingar*
    - **Leitarstefna:** *Hækkandi*

1. Veljið **Í lagi** til að vista stillingarnar og loka svarglugganum **Sala**.
1. Ef skilaboð birtast sem segja að flokkunin verði endurstillt, skal velja **Já** til að halda áfram.
1. Í hnitanetinu í efri hluta síðunnar **Vinnusniðmát** skal velja sniðmátið sem var breytt og síðan á aðgerðasvæðinu skal velja **Vinnuhausaskil**.
1. Á aðgerðasvæðinu skal velja **Breyta** til að færa síðuna yfir í breytingastillingu.
1. Í hnitanetinu skal stilla eftirfarandi gildi:

    - **Heiti töflu:** *Tímabundnar vinnufærslur*
    - **Heiti reits:** *Auðkenni sendingar*
    - **Flokka eftir þessum reit:** Veljið þennan gátreit.

1. Í aðgerðarúðunni skal velja **Vista**.
1. Lokið síðunni.

## <a name="scenario"></a>Aðstæður

Þessar aðstæður sýna dæmi þar sem tiltektarferlinu er ekki enn lokið, en þrátt fyrir það verður að hlaða vörunum sem hafa verið tíndar hingað til í flutningabíl og senda þær. Þar af leiðandi getur notandinn skipt upp framlínum sem ekki hafa verið tíndar á nýjan farm. Öll gagnatengsl verða þá sjálfkrafa uppfærð.

> [!NOTE]
> Tiltekin gildi sem lýst er í þessum aðstæðum byggja á **USMF** sýnigögnunum. Mælt er með því að nota þessi sýnigögn þegar sýna á öðrum eða verið er að kynna sér hvernig nota eigi eiginleikana. Ef **USMF** sýnigögnin eru ekki notuð skal setja inn eigin gildi eins og þörf krefur.

### <a name="step-1-create-a-load-that-has-multiple-load-lines"></a>Skref 1: Búa til farm sem er með mörgum farmlínum

Áður en hægt er að nota þessa virkni þarf að hafa farm sem inniheldur margar farmlínur. Einnig þarf að ganga úr skugga um að tiltektarstaðsetningar séu með nægar birgðir fyrir allar vörurnar í sölupöntunum sem verða stofnaðar. Farið yfir uppsetningu staðsetningarleiðbeininga (**Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**) og punktið hjá ykkur tiltektarstaðsetningarnar sem notaðar eru fyrir tiltekt sölupöntunar. Ef leiðrétta þarf birgðirnar skal stofna handvirkar hreyfingar, nota áfyllingu eða nota önnur flæði eftir þörfum.

Til að búa til nothæfan farm skal fyrst stofna þrjár sölupantanir með því að fylgja þessum skrefum.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Á aðgerðasvæðinu skal velja **Ný** til að opna svargluggann **Stofna sölupöntun**.
1. Í svarglugganum **Stofna sölupöntun** skal stilla eftirfarandi gildi (að lágmarki):

    - Í flýtiflipanum **Viðskiptavinur** skal stilla reitinn **Viðskiptavinalykill** á *US-004* (*Cave Wholesales*).
    - Í flýtiflipanum **Almennt** skal stilla reitinn **Vöruhús** á *51*.

1. Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum **Stofna sölupöntun**.
1. Nýja sölupöntunin þín opnast. Í hnitanetinu **Sölupöntunarlínur** skal bæta við línu sem er með eftirfarandi gildum:

    - **Vörunúmer:** *M9200*
    - **Magn:** *40*
    - **Prófhópur:** *ea*

1. Á valmyndinni **Birgðir** fyrir ofan hnitanetið smellir þú á **Frátekning**.
1. Á aðgerðasvæðinu skal velja **Frátektarlota** til að opna síðuna **Frátekning**.
1. Takið frá birgðirnar í sölulínunum og lokið því næst síðunni **Frátekning**.
1. Endurtakið skref 1 til 4 til að bæta við annarri sölupöntun fyrir sama viðskiptavin og vöruhús.
1. Bætið við tveimur sölulínum sem eru með eftirfarandi gildum. Þegar búið er að bæta við hvorri línunni fyrir sig skal taka frá birgðir eins og lýst er í skrefum 6 til 8.

    - **Lína 1:** Stillið reitinn **Vörunúmer** á *M9200*, reitinn **Magn** á *30* og reitinn **Eining** á *ea*.
    - **Lína 2:** Stillið reitinn **Vörunúmer** á *M9201*, reitinn **Magn** á *20* og reitinn **Eining** á *ea*.

1. Endurtakið skref 1 til 4 til að bæta við þriðju sölupöntuninni fyrir sama viðskiptavin og vöruhús.
1. Bætið við tveimur sölulínum sem eru með eftirfarandi gildum. Þegar búið er að bæta við hvorri línunni fyrir sig skal taka frá birgðir eins og lýst er í skrefum 6 til 8.

    - **Lína 1:** Stillið reitinn **Vörunúmer** á *M9201*, reitinn **Magn** á *20* og reitinn **Eining** á *ea*.
    - **Lína 2:** Stillið reitinn **Vörunúmer** á *M9202*, reitinn **Magn** á *60* og reitinn **Eining** á *ea*.

#### <a name="load-planning-workbench"></a>Vinnusvæði hleðsluáætlunar

Vinnusvæði hleðsluáætlunar mun nota kenni hleðslusniðmátsins til að búa til sendingarnar losa sölupöntunarlínurnar í vöruhúsið.

1. Farið í **Vöruhúsakerfi \> Hleðsla \> Vinnusvæði hleðsluáætlunar**.
1. Í reitnum **Vöruhús** skal velja *51*.

    Nú verður farmurinn gerður fyrir sölupantanirnar sem voru stofnaðar.

1. Í flýtiflipanum **Sölulínur**, í hnitanetinu, skal velja sölulínurnar fyrir nýju sölupantanirnar.
1. Á aðgerðasvæðinu, í flipanum **Framboð og eftirspurn**, í flokknum **Bæta við**, skal velja **Við nýjan farm**.
1. Í svarglugganum **Úthlutun hleðslusniðmáts**, í reitnum **Kenni hleðslusniðmáts**, skal velja *20 feta gámur*.
1. Veljið **Í lagi**.
1. Í hlutanum **Farmar** á síðunni **Vinnusvæði hleðsluáætlunar**, í hnitanetinu, skal finna nýlega stofnað auðkenni farms fyrir vöruhús *51*. Flettið þangað til komið er að dálknum **Leyfa skiptingu farmlínu við staðfestingu sendingar**. Velja ætti gátreitinn fyrir farminn.
1. Veljið farminn.
1. Í valmyndinni **Losa** fyrir ofan hnitanetið skal velja **Losa í vöruhús** til að stofna vinnu.
1. Í svarglugganum **Losa farm í vöruhús** skal ganga úr skugga um að flýtiflipinn **Færslur til að taka með** sýni auðkenni farmsins.
1. Veljið **Í lagi**.

    Hugsanlega koma upp skilaboðin „Aðgerð í gangi“ á meðan kerfið stofnar sendingarnar og vinnuna.

1. Í hlutanum **Farmar** á síðunni **Vinnusvæði hleðsluáætlunar** ætti farmurinn nú að vera með hleðslustöðuna *Í bylgju*. Veljið farminn og síðan, í valmyndinni **Tengdar upplýsingar** fyrir ofan hnitanetið, skal velja **Upplýsingar um bylgju** til að skoða auðkenni sendinganna sem voru stofnaðar. Þegar því er lokið skal loka síðunni **Bylgjur**.
1. Í hlutanum **Farmar** á síðunni **Vinnusvæði hleðsluáætlunar** skal velja farminn og síðan, í valmyndinni **Tengdar upplýsingar** fyrir ofan hnitanetið, skal velja **Upplýsingar um verk** til að skoða vinnuna sem var stofnuð fyrir sölupantanirnar.
1. Punktið hjá ykkur auðkenni stofnaðra verka. Hugsanlega þarf að fletta til hægri til að sjá sölupöntunarnúmer og auðkenni sendingar sem tengjast verkkenninu.

### <a name="step-2-set-up-the-execution-flow-for-mobile-devices"></a>Skref 2: Setja upp framkvæmdaflæði fyrir fartæki

Verk fartækis þurfa á upplýsingum sem notandi slær inn, t.d. verkkenni eða kenni númeraplötu. Í reitunum eru þessar upplýsingar yfirleitt veittar notendum vöruhúss í gegnum strikamerki sem er að finna í fylgiskjölum, pakkningum eða rekkum. Til að ljúka skrefum fartækis fyrir aðstæður skal ganga úr skugga um að hafa borið kennsl á verkkennið fyrir færslurnar og kenni númeraplatna fyrir vöruna og staðsetninguna í færslunum.

1. Skráið ykkur inn í fartækið með því að nota notandakenni og aðgangsorð fyrir vöruhús *51*.
1. Veljið **Á útleið**.
1. Veljið **Tiltekt sölu**.
1. Möguleiki er á því að slá inn verkkennið eða kenni númeraplötunnar. Sláið inn verkkenni fyrstu sölupöntunarinnar og veljið síðan **Færa inn**.
1. Í reitinn **Loc** skal slá inn staðsetninguna sem sýnd er til að staðfesta tiltektarstaðsetningu. Veljið síðan **Færa inn**.
1. Í reitnum **Númeraplata** skal færa inn kenni númeraplötu. Kenni númeraplötu verður að stemma við vöruna, vöruhús og staðsetningu vörunnar sem er tínd úr valdri staðsetningu. Þegar því er lokið skal velja **Færa inn**.
1. Í reitinn **Vara** skal færa inn vörunúmerið til að staðfesta vöruna sem er tínd og síðan velja **Færa inn**.
1. Í reitinn **Magn** skal færa inn magnið til að staðfesta vöruna sem er tínd og síðan velja **Færa inn**.
1. Í reitinn **Marknúmeraplata** skal færa inn kenni marknúmeraplötu. Marknúmeraplötur eru skilgreindar af notanda. Gætið þess að slá inn kenni númeraplötu sem hægt er að muna. Mælt er með því að nota núverandi dagsetningu plús tveggja stafa röð (ÁÁMMDD\#\#) sem snið, t.d. *19112301*. Þegar því er lokið skal velja **Færa inn**.
1. Farið yfir upplýsingar sem eru sýndar. Þessar upplýsingar eru upplýsingar um *Tiltekt* sem verður nú að gögnum *Frágangs* fyrir frágangsaðgerðina. Þegar því er lokið skal velja **Færa inn**.

    - Skilaboðin **Vinnu lokið** birtast.

1. Endurtakið skref 4 til 10 fyrir verkkenni annarrar sölupöntunarinnar.

Næsta skref er að hlaða tíndu númeraplötunum tveimur í flutningabílinn.

1. Skráið ykkur inn í fartækið með því að nota notandakenni og aðgangsorð fyrir vöruhús *51*.
1. Veljið **Á útleið**.
1. Veljið **Hleðsla sölu**.
1. Færið inn notandaskilgreint kenni marknúmeraplötu sem stofnað var fyrir fyrsta verkkennið í ferlinu á undan. Síðan skal velja **Færa inn** til að setja númeraplötuna á staðsetninguna **STIG**.
1. Færið aftur inn kenni marknúmeraplötu og veljið síðan **Færa inn** til að ganga frá númeraplötunni á staðsetninguna **AFGREIÐSLUHURÐ**.
1. Endurtakið skref 4 til 5 fyrir kenni marknúmeraplötu sem stofnað var fyrir annað verkkennið.

Verkkennunum tveimur verður nú lokað (hlaðin).

### <a name="step-3-confirm-the-outbound-shipment"></a>Skref 3: Staðfesta sendingu á útleið

Í þessu skrefi verða staðfestar sölupantanirnar tvær og vinnan sem hefur verið lokið fyrir farminn til að senda tíndar vörur farmsins og búa til nýjan farm fyrir vörurnar sem hafa ekki verið tíndar. Staðfesting á sendingu á útleið verður að gera á síðunni **Upplýsingar um hleðslu**.

1. Farið í **Vöruhúsakerfi \> Hleðsla \> Vinnusvæði hleðsluáætlunar**.
1. Í hlutanum **Hleðslur**, í hnitanetinu, skal velja línuna fyrir hleðslukennið sem var stofnað.
1. Veljið tengil hleðslukennis til að opna síðuna **Upplýsingar um hleðslu**.
1. Á síðunni **Upplýsingar um hleðslu**, á aðgerðasvæðinu, í flipanum **Afhenda og taka á móti**, í flokknum **Staðfesta**, skal velja **Sending á útleið** til að hefja staðfestinguna.
1. Í svarglugganum **Staðfesta sendingu**, í reitnum **Aðferð við skiptingu farms við staðfestingu afgreiðslu**, skal velja *Skipta magni á nýjan farm*.
1. Veljið **Í lagi**.

    Hugsanlega koma upp skilaboðin „Aðgerð í gangi“.

    Upplýsandi skilaboð birtast sem sýna að sending farmsins hafi verið staðfest og að nýr farmur hafi verið búinn til úr skiptu magni.

Uppfærið síðuna **Vinnusvæði hleðsluáætlunar** til að nýlega stofnaðan farm.

Einnig er hægt að staðfesta að tengsl milli færslna hafi verið uppfærð á eftirfarandi hátt:

- Eftirstandandi (óunnar) sendingar og línur sendingar eru uppfærðar með nýja hleðslukenninu.
- Sölupöntunin er tengd við nýja hleðslukennið.
- Upprunalegi farmurinn inniheldur ekki eftirstandandi farmlínur.
- Eftirstandandi vinna hefur verið uppfærð með nýja hleðslukenninu.
- Bylgjan helst óbreytt.
- Staða nýja farmsins er uppfærð á réttan hátt. (Ef verkstaðan er _Í vinnslu_ á hleðslustaðan að vera _Í vinnslu_.)

## <a name="notes-and-tips"></a>Athugasemdir og ábendingar

- Einnig er hægt að kveikja á færibreytunni **Leyfa skiptingu farmlínu við staðfestingu sendingar** þegar farmurinn hefur verið búinn til með slökkt á færibreytunni **Hleðslusniðmát** en áður en hleðsluferlið hefst. Farið í æskilegan farm og síðan, í hausyfirlitinu, skal kveikja á færibreytunni.
- Valkosturinn **Skipta magni á nýjan farm** virkar einnig þegar einhverjir af eftirstandandi verkhausum eru með stöðuna *Í vinnslu*. Þess vegna er enn hægt að nota virknina jafnvel þótt starfsmenn séu þegar byrjaðir að keyra tiltektarpantanirnar.
- Ef valið er **Hætta við óuppfyllt magn** á meðan til er verk með stöðuna *Opið* eða *Í vinnslu*, birtast eftirfarandi villuboð: „Ekki er hægt að hætta við eftirstandandi magn fyrir farm. Vinna er til fyrir farm.“
- Ef valið er **Hætta við óuppfyllt magn** þegar ekkert verk er eftir, en ólosaðar farmlínur eru til fyrir farminn, birtast eftirfarandi villuboð: „Ekki var hægt að staðfesta sendinguna fyrir farm vegna þess að magnið fyrir vöru fer yfir þá prósentu sem skilgreind er fyrir undirafhendingu.“ Til að koma í veg fyrir villuna er hægt að stilla prósentu fyrir **Undir afhendingu** í ólosaðri farmlínu á 100 prósent. Ólosaðar línur verða ekki fluttar á nýjan farm, en núverandi farmur verður staðfestur með undirafhendingu. Í þessu tilfelli verður ekki hægt að endurlosa upprunalega pöntun. Því verður að meðhöndla hana á annan hátt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]