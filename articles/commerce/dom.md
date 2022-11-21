---
title: Dreifingarstjórnun pöntunar (DOM)
description: Þessi grein lýsir virkni dreifingarstjórnunar pöntunar (DOM) í Dynamics 365 Commerce.
author: josaw1
ms.date: 02/08/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: a18441c44869e0e95cf79e35045dd7eacca7e43d
ms.sourcegitcommit: 4f987aad3ff65fe021057ac9d7d6922fb74f980e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/14/2022
ms.locfileid: "9764180"
---
# <a name="distributed-order-management-dom"></a>Dreifingarstjórnun pöntunar (DOM)

[!include [banner](includes/banner.md)]

Þessi grein lýsir virkni dreifingarstjórnunar pöntunar (DOM) í Microsoft Dynamics 365 Commerce.

DOM er alhliða fínstillingalausn fyrir uppfyllingar sem hjálpar til við að hámarka skilvirkni við uppfyllingu pantana í aðfangakeðjuneti. DOM hjálpar til við að tryggja að vörur séu afhentar viðskiptavinum í réttu magni, frá réttum upprunastað og á réttum tíma. DOM getur einnig hjálpað til við að hámarka hagnað, lágmarka kostnað og uppfylla kröfur um þjónustustig.

DOM notar MIP-forritun (blandaða heiltöluforritun) og forspárgreiningarlíkön til að fínstilla á runustigi og á stigi hverrar pöntunar fyrir sig. Þessi eiginleiki gerir söluaðilum kleift að nota skilgreindar reglur til að koma jafnvægi á margar uppfyllingarþarfir sem stangast á. Í afhendingarneti nútímans, þar sem uppfylling pantana getur farið fram í gegnum margar miðlunarleiðir, þurfa fyrirtæki að geta brugðist skjótt við breytingum á pöntunum, framboðsvandamálum birgja og aukinni eftirspurn. DOM hjálpar til við að hámarka skilvirkni við uppfyllingu pantana og við að finna rétta upprunastaði fyrir vöruafhendingar í takt við viðskiptaskorður og markmið á borð við að lágmarka kostnað og uppfylla pantanir á þeim upprunastað sem er næstur. Til að fínstilla uppfyllingu pantana notar DOM fjarlægðina á milli upprunastaða vörunnar og sendingarstaða, kostnaðarliði sem eru skilgreindir í fínstillingarmarkmiðum og reglur sem eru skilgreindar sem skorður, t.d. birgða- og uppfyllingarhnúta. Með DOM er hægt að skilgreina margar forstillingar sem gera fyrirtækjum kleift að keyra mismunandi fínstillingaáætlanir í samræmi við gerð fyrirtækisins eða markhóp þess. 

Eftirfarandi skýringarmynd sýnir ferli sölupöntunar í DOM-kerfi.

![Ferli sölupöntunar í samhengi við DOM-staðalinn.](./media/flow.png "Ferli sölupöntunar í samhengi við DOM-staðalinn")

## <a name="set-up-dom"></a>Setja upp DOM

1. Opnið **Kerfisstjórnun \> Setja upp \> Skilgreining leyfis**.
2. Á flipanum **Skilgreiningarlykill** skal stækka hnútinn **Commerce** og síðan velja gátreitinn **Dreifingarstjórnun pöntunar**.
3. Opnið **Retail and Commerce \> Dreifingarstjórnun pöntunar \> Setja upp \> DOM færibreytur**.
4. Á flipanum **Almennt** skal stilla eftirfarandi gildi:

    - **Virkja dreifingarstjórnun pöntunar** – Stillið þennan valkost á **Já**.
    - **Staðfesta notkun á Bing-kortum fyrir DOM** – Stillið þennan valkost á **Já**.

        > [!NOTE]
        > Aðeins er hægt að stilla þennan valkost á **Já** ef valkosturinn **Virkja Bing-kort** á flipanum **Bing-kort** á síðunni **Samnýttar viðskiptafæribreytur** (**Retail and Commerce \> Uppsetning höfuðstöðva\> Færibreytur \> Samnýttar viðskiptafæribreytur**) er einnig stilltur á **Já**, og ef gildur lykill er sleginn inn í reitinn **Lykill Bing-korts**.
        >
        > Gáttin [Þróunarmiðstöð Bing-korta](https://www.bingmapsportal.com/) gerir notanda kleift að takmarka aðgang á API-lyklum Bing-korta niður í lénasafn sem notandi tilgreinir. Með þessum eiginleika geta viðskiptavinir skilgreint afmarkað safn tilvísanagilda eða svið IP-talna sem lykillinn verður sannprófaður gagnvart. Beiðnir úr heimildarlistanum verða unnar á venjulegan hátt, á meðan beiðnir utan listans skila svari um að aðgangur sé óheimill. Lénöryggi sem viðbót við API-lykil er valfrjáls og lyklar sem ekki er breytt halda áfram að virka. Heimildarlisti fyrir lykil er óháður öllum öðrum lyklunum og gerir notanda kleift að hafa aðskildar reglur fyrir hvern lykil. Dreifingarstjórnun pöntunar styður ekki uppsetningu eiginleika sem lén vísa í.

    - **Varðveislutími í dögum** – Tilgreinið hversu lengi á að geyma uppfyllingaráætlanir í kerfinu, sem DOM-keyrslur búa til. Runuvinnslan **Uppsetning á eyðingarvinnslu DOM-uppfyllingargagna** eyðir öllum uppfyllingaráætlunum sem eru eldri en dagafjöldinn sem tilgreindur er hér.
    - **Höfnunartímabil (í dögum)** – Tilgreinið tímann sem þarf að líða áður en hægt er að úthluta hafnaðri pöntunarlínu á sömu staðsetninguna.

5. Á flipanum **Leysari** skal stilla eftirfarandi gildi:

    - **Hámarksfjöldi sjálfvirkra uppfyllingatilrauna** – Tilgreinið hversu oft DOM-vélin reynir að miðla pöntunarlínu á staðsetningu. DOM-vélin flaggar pöntunarlínu sem undantekningu ef hún getur ekki miðlað pöntunarlínunni á staðsetningu í tilgreindum fjölda tilrauna. Hún mun þá sleppa þeirri línu í framtíðarkeyrslum þar til staðan er endurstillt handvirkt.
    - **Nærliggjandi landsvæði svæðisbundinnar verslunar** – Færið inn gildi. Þessi reitur auðveldar að ákvarða hvernig staðsetningar eru flokkaðar saman og litið á sem jafnar hvað varðar fjarlægð. Ef til að mynda fært er inn **100** verður litið á allar verslanir eða dreifingarstöðvar innan 100 mílna radíuss frá aðsetri uppfyllingar sem jafnar hvað varðar fjarlægð.
    - **Gerð leysara** – Veljið gildi. Tvær gerðir af leysara eru gefnar út með Commerce: **Leysari framleiðslu** og **Einfaldaður leysari**. Velja þarf **Leysari framleiðslu** fyrir allar vélar sem munu keyra DOM (sem sagt allir þjónar sem eru hluti af DOMBatch-flokknum). Leysari framleiðslu krefst tiltekins leyfislykils sem er að sjálfgefnu leyfður og uppsettur í vinnsluumhverfi. Í nýrri umhverfum í þrepi 2+ er Leysari framleiðslu þegar virkur. Þennan leyfislykil þarf að setja upp handvirkt fyrir umhverfi sem er ekki vinnsluumhverfi. Til að setja upp leyfislykilinn handvirkt skal fylgja þessum skrefum:

        1. Opnið samnýtta eignasafnið í Microsoft Dynamics Lifecycle Services og veljið **Líkan** sem eignagerð og sækið skrána **DOM-leyfi**.
        1. Ræsið Microsoft Internet Information Services (IIS), hægrismellið á **Vefsvæði AOSService** og veljið síðan **Skoða**. Windows Explorer-gluggi opnast á **\<AOS service root\>\\webroot**. Skrifa skal niður slóðina fyrir \<AOS Service root\> vegna þess að hún verður notuð í næsta skrefi.
        1. Afritið skilgreiningarskrána í skráasafninu **\<AOS Service root\>\\PackagesLocalDirectory\\DOM\\hólf**.
        1. Opnaðu biðlara Höfuðstöðva og opnaðu svo síðuna **DOM-færibreytur**. Á flipanum **Leysari**, í reitnum **Gerð leysara** skal velja **Leysari framleiðslu** og staðfesta að engin villuboð birtist.

        > [!NOTE]
        > Einfaldaður leysari er útvegaður svo smásöluaðilar geti prófað DOM-eiginleikann án þess að þurfa að setja upp tiltekið leyfi. Fyrirtæki eiga ekki að nota einfaldaðan leysara í vinnsluumhverfi.
        >
        > Leysari framleiðslu bætir frammistöðu, (svo sem fjölda pantana og pöntunarlína sem hægt er að vinna með í keyrslu) og samleitni niðurstaðna (runa pantana kemur ekki endilega með bestu niðurstöðuna í sumum tilfellum). Reglan um **Hlutapantanir** krefst Leysara framleiðslu.

6. Farið aftur í **Smásala og viðskipti \> Dreifingarstjórnun pöntunar \> Setja upp \> DOM-færibreytur**.
7. Á flipanum **Númeraraðir** skal úthluta áskildum númeraröðum á hinar ýmsu DOM-einingar.

    > [!NOTE]
    > Áður en hægt er að úthluta númeraröðum á einingarnar verða þær að vera skilgreindar á síðunni **Númeraraðir** (**Fyrirtækisstjórnun \> Númeraraðir \> Númeraraðir**).

8. DOM-eiginleikinn styður skilgreininguna á ýmsum gerðum DOM-reglna, og fyrirtæki geta skilgreint margar reglur, allt eftir rekstrarþörfum þeirra. Hægt er að skilgreina DOM-reglur fyrir flokk af staðsetningum eða einkvæmar staðsetningar, og fyrir tilgreinda afurðategund, afurð eða vöruvíddasamsetningu. Til að stofna flokkun á staðsetningum sem verður að nota fyrir DOM-reglurnar skal fylgja þessum skrefum:

    1. Opnið **Retail and Commerce \> Uppsetning rásar \> Uppfyllingarflokkar**.
    2. Veljið **Nýr** og færið inn heiti og lýsingu á nýja flokknum.
    3. Veljið **Vista**.
    4. Veljið **Bæta við línu** til að bæta einni staðsetningu við flokkinn. Að öðrum kosti skal velja **Bæta við línum** til að bæta við mörgum staðsetningum.

    > [!NOTE]
    > Í Commerce-útgáfu 10.0.12 og nýrri verður að virkja **Getu til að tilgreina staðsetningar sem „Sending“ eða „Afhending“ í uppfyllingarflokki** á vinnusvæði **eiginleikastjórnunar**.
    >
    > Þessi eiginleiki bætir við nýjum grunnstillingum á síðu **uppfyllingarflokks** svo að hægt sé að skilgreina hvort hægt sé að nota vöruhúsið fyrir sendingu eða hvort hægt sé að nota samsetninguna vöruhús/verslun fyrir sendingu, afhendingu eða hvort tveggja. 
    >
    > Ef þessi eiginleiki er virkur mun það uppfæra valkosti fyrir staðsetningarval þegar verið er að stofna afhendingar- eða sendingarpantanir á sölustað.
    >
    > Ef eiginleikinn er virkur uppfærast einnig síður á sölustað þegar aðgerðirnar „senda allt“ eða „senda valið“ eru valdar.

9. Til að skilgreina reglur skal opna **Retail and Commerce \> Dreifingarstjórnun pöntunar \> Setja upp \> Stjórna reglum**. Eftirfarandi DOM-reglur eru studdar eins og er:

    - **Regla lágmarksbirgða** – Þessi gerð af reglu gerir fyrirtækjum kleift að aðgreina tilgreint magn afurðar í öðrum tilgangi en fyrir uppfyllingu pöntunar. Sem dæmi er hugsanlegt að fyrirtæki vilji ekki að DOM taki allar tiltækar birgðir í verslun til greina við uppfyllingu pöntunar. Í staðinn gætu þau viljað taka frá einhverjar birgðir fyrir viðskiptavini á staðnum. Þegar þessi gerð af reglu er notuð er hægt að skilgreina lágmarksbirgðir sem á að geyma fyrir flokk af afurðum, staka afurð eða afurðarafbrigði fyrir hverja staðsetningu eða flokk staðsetninga. Einnig er hægt að skilgreina lágmarksbirgðir með því að nota viðbótartegundastigveldi. Ef vara tilheyrir mörgum flokkum fær viðbótarflokkur hæsta vægi fyrir allar reglur þar sem hægt er að nota flokka.
    - **Forgangsregla uppfyllingarstaðsetningar** – Þessi gerð af reglu gerir fyrirtækjum kleift að skilgreina stigveldi staðsetninga til að koma á forgangi sem DOM-vélin hefur í huga þegar hún reynir að bera kennsl á uppfyllingarstaðsetningar fyrir tilgreindar afurðir. Gilt svið forgangs er frá 1 til 10, þar sem 1 er efst í forgangi og 10 er neðst í forgangi. Staðsetningar sem eru ofar í forgangsröðinni eru teknar til greina á undan staðsetningum sem eru neðar í forgangsröðinni. Pöntunum er aðeins miðlað á staðsetningar þar sem forgangur er skilgreindur, ef reglan er skilgreind sem ströng takmarkandi regla. Kjörstillingar DOM eru að senda heilar pantanir frá einni staðsetningu. Þetta þýðir að ef ekki er hægt að afgreiða heila pöntun og allar línur í henni frá einni staðsetningu sem er í 1. forgangi mun DOM reyna að uppfylla hana frá staðsetningu sem er með 2. forgang.
    - **Regla hlutapantana** – Í Retail útgáfu 10.0.5 var færibreytunni **Uppfylla pöntun aðeins frá einni staðsetningu** breytt í **Hámarksstaðsetningar uppfyllingar**. Gamla færibreytan gerði notendum kleift að skilgreina hvort aðeins sé hægt að uppfylla pantanir frá einum stað eða frá eins mörgum stöðum og mögulegt er. Nýja færibreytan gerir notendum kleift að tilgreina hvort hægt sé að uppfylla pantanir frá ákveðnum fjölda staðsetninga (allt að fimm) eða frá eins mörgum staðsetningum og mögulegt er. DOM mun skipta línunni fyrir alla valkosti nema fyrir uppfyllingu frá einum stað vegna þess að úrvinnsla pantana fer eftir línum. Þessi regla virkar aðeins með Leysara framleiðslu.
    - **Staðsetningarregla uppfyllingar utan nets** – Þessi regla gerir fyrirtækjum kleift að tilgreina staðsetningu eða flokk staðsetninga sem utan nets eða ekki tiltæka fyrir DOM, svo ekki sé hægt að úthluta pöntunum á þessar staðsetningar til uppfyllingar.
    - **Regla um hámark hafnana** – Þessi regla gerir fyrirtækjum kleift að skilgreina mörk fyrir hafnanir. DOM-vinnslan mun merkja pöntun eða pöntunarlínu sem undantekningu þegar mörkum er náð og útiloka hana frá frekari úrvinnslu. Til að tryggja afköst skoðar DOM ekki sögu allra hafnana. 

        Eftir að pöntunarlínum er úthlutað á staðsetningu getur staðsetningin hafnað úthlutaðri pöntunarlínu vegna þess að hún getur mögulega ekki uppfyllt þessa línu af einhverjum ástæðum. Hafnaðar línur eru merktar sem undantekning og settar aftur í safnið til vinnslu í næstu keyrslu. Við næstu keyrslu reynir DOM að úthluta höfnuðum línum á aðra staðsetningu. Nýja staðsetningin getur einnig hafnað úthlutaðri pöntunarlínu. Þessi hringrás úthlutunar og höfnunar getur átt sér stað mörgum sinnum. Þegar talning höfnunar nær skilgreindum mörkum merkir DOM pöntunarlínuna sem varanlega undantekningu og kemur ekki til með að velja þessa línu til úthlutunar aftur. DOM tekur pöntunarlínuna eingöngu aftur til greina fyrir endurúthlutun ef notandi endurstillir stöðu pöntunarlínunnar handvirkt.

    - **Regla um hámarksfjarlægð** – Þessi regla gerir fyrirtækjum kleift að skilgreina hámarksfjarlægð sem staðsetning eða flokkur staðsetninga getur verið í til að uppfylla pöntun. Ef skilgreindar reglur um hámarksfjarlægð fyrir staðsetningu skarast, notar DOM lægstu hámarksfjarlægð sem er skilgreind fyrir þá staðsetningu.
    - **Regla um hámarkspantanir** – Þessi regla gerir fyrirtækjum kleift að skilgreina hámarksfjölda pantana sem staðsetning eða flokkur staðsetninga getur unnið úr. Í fínstillingaferlinu tekur kerfið tillit til pantana sem hafa ekki verið sendar frá þessum stöðum. Þessi athugun er gerð þvert á forstillingar. Þetta þýðir að ef hámarksfjöldi pantana sem skarast er skilgreindur þvert á forstillingar fyrir sömu staðsetningu tekur kerfið tillit til hámarksfjölda pantana sem er skilgreindur í öllum forstillingum. 

    Hér eru nokkrar algengar eigindir sem hægt er að skilgreina fyrir allar undanfarandi gerðir af reglum:

    - **Upphafsdagur** og **Lokadagur** – Hægt er að nota þessa reiti til að stilla hverja reglu á gildisdagsetningar.
    - **Óvirkar** – Einungis reglur sem hafa gildið **Nei** fyrir þennan reit eru teknar til greina í DOM-keyrslu.
    - **Ströng takmarkandi** – Regla getur verið skilgreind sem annaðhvort ströng takmarkandi eða ekki ströng takmarkandi. Allar DOM-keyrslur fara í gegnum tvær ítrekanir. Í fyrri ítrekuninni er hver regla meðhöndluð sem ströng takmarkandi regla, óháð því hver stilling reitsins er. Það er að segja, allar reglur eru í gildi. Eina undantekningin er reglan **Forgangur staðsetningar**. Í seinni ítrekuninni eru reglurnar, sem ekki voru skilgreindar sem strangar takmarkandi reglur, fjarlægðar og pöntunum eða pöntunarlínum, sem ekki var úthlutað á staðsetningu þegar allar reglurnar voru í gildi, er úthlutað á staðsetningar.

10. Uppfyllingarsnið eru notuð til að flokka safn af reglum, lögaðilum, söluuppruna pantana og afhendingarmátum. Hver DOM-keyrsla er fyrir tiltekið uppfyllingarsnið. Á þennan hátt geta fyrirtæki skilgreint og keyrt safn af reglum fyrir safn af lögaðilum á pöntunum sem eru með tiltekinn söluuppruna pantana og tiltekinn afhendingarmáta. Því er hægt að skilgreina uppfyllingarsnið eins og við á ef keyra þarf ólík reglusöfn fyrir ólík söfn af söluuppruna pantana eða afhendingarmáta. Til að setja upp uppfyllingarsnið skal fylgja þessum skrefum:  

    1. Opnið **Retail and Commerce \> Dreifingarstjórnun pöntunar \> Setja upp \> Uppfyllingarsnið**.
    2. Veljið **Nýtt**.
    3. Færið inn gildi í reitina **Snið** og **Lýsing**.
    4. Stillið valkostinn **Nota niðurstöðu sjálfkrafa**. Ef þessi valkostur er stilltur á **Já** verða niðurstöður DOM-keyrslu fyrir sniðið sjálfkrafa notaðar í sölupöntunarlínum. Ef hann er stilltur á **Nei** verður eingöngu hægt að skoða niðurstöðurnar í uppfyllingaráætlun. Þær verða ekki notaðar í sölupöntunarlínum.
    5. Ef keyra á DOM-sniðið fyrir pantanir sem eru með söluuppruna allra pantana, þ.m.t. þeirra þar sem uppruninn er óskilgreindur, skal stilla valkostinn **Vinna úr pöntunum með auðan söluuppruna** á **Já**. Til að keyra forstillinguna fyrir aðeins nokkra söluuppruna pantana er hægt að skilgreina þá á síðunni **Söluupprunar** líkt og verður útskýrt síðar.

        > [!NOTE]
        > Í Commerce-útgáfu 10.0.12 og nýrri verður að virkja eiginleika **Getu til að úthluta uppfyllingarflokki á uppfyllingarforstillingu** á vinnusvæði **eiginleikastjórnunar**. Með þessum eiginleika er hægt að tilgreina lista yfir vöruhús sem DOM á að taka tillit til þegar fínstilling er keyrð með uppfyllingarforstillingu. Ef listi yfir vöruhús er ekki tilgreindur skoðar DOM öll vöruhús og lögaðila sem eru skilgreindir í forstillingunni.
        >
        > Þessi eiginleiki bætir við nýrri grunnstillingu á síðu **uppfyllingarforstillingar** sem hægt er að tengja við einn uppfyllingarflokk. 
        >
        > Ef uppfyllingarflokkurinn er valinn er hægt að keyra DOM-reglur fyrir viðkomandi uppfyllingarforstillingu á móti sendingarvöruhúsum innan þess uppfyllingarflokks. 
        > 
        > Til að fullnýta þennan eiginleika þarf að tryggja að til staðar sé einn uppfyllingarflokkur sem inniheldur öll sendingarvöruhúsin og tengja þann uppfyllingarflokk við uppfyllingarforstillinguna.

    6. Á flýtiflipanum **Lögaðilar** skal velja **Bæta við** og síðan lögaðila.
    7. Á flýtiflipanum **Reglur** skal velja **Bæta við** og síðan regluna sem tengja á við sniðið.
    8. Endurtakið þessi tvö skref þar til allar nauðsynlegar reglur eru tengdar við sniðið.
    9. Veljið **Vista**.
    10. Á flipanum **Setja upp**, á aðgerðasvæðinu, skal velja **Afhendingarmátar**.
    11. Á síðunni **Afhendingarmátar** skal velja **Nýr**.
    12. Í reitnum **Fyrirtæki** skal velja lögaðilann. Listinn yfir fyrirtæki takmarkast við lögaðilana sem bætt var við hér á undan.
    13. Í reitnum **Afhendingarmáti** skal velja afhendingarmátann sem tengja á við þetta snið. Ekki er hægt að tengja afhendingarmáta við mörg virk snið.
    14. Endurtakið þessi tvö skref þar til allir nauðsynlegir afhendingarmátar eru tengdir við sniðið.
    15. Lokið síðunni **Afhendingarmátar**.
    16. Á flipanum **Setja upp**, á aðgerðasvæðinu, skal velja **Söluuppruni pantana**.
    17. Á síðunni **Söluupprunar** skal velja **Nýr**.
    18. Í reitnum **Fyrirtæki** skal velja lögaðilann. Listinn yfir fyrirtæki takmarkast við lögaðilana sem bætt var við hér á undan.
    19. Í reitnum **Söluuppruni** skal velja söluuppruna sem tengja á við þetta snið. Ekki er hægt að tengja söluuppruna við mörg virk snið.
    20. Endurtakið þessi tvö skref þar til allir nauðsynlegir söluupprunar eru tengdir við sniðið.
    21. Lokið síðunni **Söluupprunar**.
    22. Stillið valkostinn **Virkja snið** á **Já**. Villuboð kemur upp ef einhverjar villur eru í uppsetningu.

## <a name="dom-processing"></a>DOM-vinnsla

DOM keyrir aðeins í runuvinnslu. Til að skilgreina runuvinnslu fyrir DOM-keyrslur skal fylgja þessum skrefum.

1. Opnið **Retail and Commerce \> Dreifingarstjórnun pöntunar \> Runuvinnsla \> Verkuppsetning DOM-vinnslu**.
1. Á flýtiflipanum **Færibreytur**, í reitnum **Uppfyllingarsnið** skal velja snið sem DOM þarf að keyra fyrir.
1. Á flýtiflipanum **Keyra í bakgrunni**, í reitnum **Runuflokkur** skal velja grunnstilltan runuflokk.
1. Í reitinn **Verklýsing** skal færa inn heiti á runuvinnslunni.
1. Veljið **Endurtekning** og skilgreinið endurtekningu runuvinnslunnar.
1. Veljið **Í lagi**.

Við vinnslu tekur DOM tillit til pöntunar og pöntunarlína eins og hér er lýst:

- Pöntunarlínur sem uppfylla skilyrði fyrir söluuppruna pöntunar, afhendingarmáta og lögaðila eins og það er skilgreint í DOM-sniðinu, og sem uppfylla einhver þessara skilyrða:

    - Þær eru stofnaðar úr viðskiptarásum.
    - Þeim hefur aldrei verið miðlað af hálfu DOM.
    - Þeim hefur aldrei verið miðlað af hálfu DOM áður, en þær eru merktar sem undantekningar og eru undir mörkum hámarkstilrauna.
    - Afhendingarmátinn er ekki að sækja eða afhenda rafrænt.
    - Þær eru ekki merktar til afhendingar.
    - Þær eru ekki útilokaðar handvirkt.

- Pantanir sem eru ekki í bið

DOM velur staðsetningu sem er næst afhendingaraðsetri viðskiptavinar eftir að það beitir reglum, birgðatakmörkunum og hámörkun. DOM umbreytir aðsetrum af gerðinni **Afhending** í breiddar- og lengdargráðugildi. Það umbreytir síðan afhendingaraðsetri sölupöntunar í breiddar- og lengdargráðugildi og uppfærir breiddar- og lengdargráðugildi aðsetursins til síðari nota. DOM fer eftir Bing-kortum til að ákvarða nákvæm breiddar- og lengdargráðugildi í samræmi við upplýsingar um aðsetur, borg og póstnúmer.

DOM notar API Bing-korta til að reikna úr fjarlægð í lofti eða akstursvegalengd, allt eftir stillingunum. Síðan notar það þessar upplýsingar til að ákvarða sendingarkostnað. Fínstillingalíkanið forgangsraðar uppfyllingu heildarpantana frá einum stað. Jafnvel þótt hluti pöntunar sé tiltækur í sömu borg eða innan sama póstnúmers er líkanið fínstillt til að draga úr fjölda sendinga. 

DOM flettir upp tiltækum birgðum með því að skoða lagerbirgðir hjá vöruhúsum V2-aðila. Í hverri runuvinnslu skiptir DOM pöntunum upp í runur í samræmi við færibreytugildi **DOM-vinnslu** í verkum sem eru skilgreind í forstillingunni. Sjálfgefið gildi færibreytunnar er **2000**. Dæmi: Ef 10.000 pöntunarlínur eru fínstilltar í vinnslu og færibreyta **DOM-vinnslu** er stillt á sjálfgildið **2000** býr DOM til fimm runur sem unnið úr samtímis. Uppfyllingaráætlanir eru síðan sóttar úr fínstillingunni og notaðar í línunni. Ef skipta þarf pöntunarlínunni á milli tveggja staða tryggir DOM að verð og skattar dreifist á viðeigandi hátt á línurnar.

![Skilyrði sölupöntunar.](./media/ordercriteria.png "Skilyrði sölupöntunar")

## <a name="results-of-dom-runs"></a>Niðurstöður DOM-vinnsla

Ef uppfyllingarforstilling er stillt á **Nota sjálfkrafa** verða niðurstöður vinnslunnar notaðar sjálfkrafa í sölupöntunarlínum, og hægt verður að sjá uppfyllingaráætlun sérstaklega. Ef uppfyllingarsnið er hins vegar ekki stillt á **Nota sjálfkrafa** verður aðeins hægt að sjá niðurstöður keyrslunnar í yfirliti uppfyllingaráætlunar. 

Til að skoða allar uppfyllingaráætlanir sem eru búnar til skal fylgja þessum skrefum.

1. Opnið **Retail and Commerce \> Dreifingarstjórnun pöntunar \> Dreifingarstjórnun pöntunar**.
2. Á vinnusvæðinu **Dreifingarstjórnun pöntunar** skal velja reitinn **Uppfyllingaráætlanir**.
3. Veljið kennið fyrir viðeigandi uppfyllingaráætlun pöntunar til að skoða uppfyllingaráætlunina.

    Upplýsingahluti pöntunar í uppfyllingaráætlun sýnir upprunalegar sölupöntunarlínur sem voru hluti af keyrslunni. Fyrir utan hefðbundna reiti sölupöntunarlínu inniheldur upplýsingahluti pöntunar einnig eftirfarandi þrjá reiti sem tengjast DOM:

    - **Uppfyllingargerð** – Þessi reitur sýnir hvort sölupöntunarlína sé miðluð að fullu, miðluð að hluta til eða ekki miðluð á staðsetningu.
    - **Skipta** – Þessi reitur sýnir hvort einni sölupöntunarlínu hafi verið skipt og henni miðlað á mismunandi staðsetningar.
    - **Fjöldi uppfyllingarstaðsetninga** – Þessi reitur sýnir hversu margar uppfyllingarlínur voru stofnaðar fyrir eina sölupöntunarlínu (byggt á fjölda staðsetninga sem upprunalegri sölupöntunarlínu var miðlað á).

    Upplýsingahlutinn um uppfyllingu pöntunar sýnir úthlutun upprunalegra sölupöntunarlína á mismunandi staðsetningar, ásamt magni þeirra.

## <a name="order-line-actions-and-statuses"></a>Aðgerðir og stöður pöntunarlínu

Eftirfarandi lýsir stillingum á pöntunarlínum. Til að opna pöntunarlínu skal opna **Retail and Commerce \> Viðskiptavinir \> Allar sölupantanir**.

- Ef valkosturinn **Útiloka frá DOM-vinnslu** á flipanum **Almennt** í sölupöntunarlínu er stilltur á **Já** verður pöntun eða pöntunarlína útilokuð frá DOM-vinnslu.
- Hægt er að stilla reitinn **DOM-staða** á flipanum **Almennt** í sölupöntunarlínu á eitt af eftirfarandi gildum:

    - **Ekkert** – Pöntunarlínunni hefur aldrei verið miðlað.
    - **Að fullu** – Pöntunarlínunni hefur verið miðlað og úthlutað á staðsetningu.
    - **Undantekning** – Pöntunarlínunni hefur verið miðlað en ekki er hægt að úthluta henni á staðsetningu. Undantekningar eru með margar undirgerðir sem hægt er að skoða á DOM-vinnusvæðinu:

        - **Ekkert magn er tiltækt** – Engar tiltækar birgðir eru til sem hægt er að úthluta pöntun á í staðsetningum.
        - **Hámarksfjöldi hafnana** – Pöntunarlína hefur náð hámarksfjölda hafnana.
        - **Árekstrar við breytingu á gögnum** – Sölupöntunarlínu hefur verið breytt síðan pöntun var miðluð. Þess vegna er ekki hægt að nota uppfyllingaráætlunina fyrir pöntunina.
        - **Sérstök undantekning pöntunarlínu** – Margar undantekningar eru á pöntunarlínu.

- Hægt er að keyra DOM í gagnvirku sniði meðan á færslu sölupöntunar stendur. Við innslátt pöntunarlínu, eftir að afurð og magn hefur verið tilgreint, er hægt að velja **Uppfæra línu** og síðan, undir **DOM**, skal velja **Stinga upp á uppfyllingarstaðsetningu**. Þá sést listi yfir staðsetningar sem byggjast á DOM-reglum sem geta uppfyllt magnið á pöntunarlínunni. Á þennan lista er raðað eftir fjarlægð. Veljið staðsetningu til að setja viðeigandi svæði og vöruhús á sölupöntunarlínuna. Til að þessi virkni virki sem skyldi þarf að vera til staðar virkt uppfyllingarsnið sem passar við söluuppruna og afhendingarmáta á sölulínunni.
- Til að skoða skrár DOM-keyrslu fyrir sölupöntunarlínu skal velja **Sölupöntunarlína** og síðan, undir **DOM**, velja **Skoða DOM-skrár**. DOM-skrárnar sýna öll tilvik og skrár sem DOM-keyrslan bjó til. Skrárnar hjálpa til við að skilja hvers vegna tilgreindri staðsetningu var úthlutað á pöntunarlínu og hvaða reglur og takmarkanir voru íhugaðar sem hluti af úthlutuninni. DOM-skrárnar eru einnig tiltækar á stigi sölupöntunarhauss á flipanum **Stjórna**.

## <a name="run-a-clean-up-job-for-dom-fulfillment-plans"></a>Keyrið hreinsunarverk fyrir uppfyllingaráætlanir DOM

Uppfyllingaráætlanir eru stofnaðar á meðan DOM-vinnsla keyrir. Með tímanum mun kerfið geyma fjöldann allan af uppfyllingaráætlunum. Til að stjórna fjölda uppfyllingaráætlana sem kerfið geymir er hægt að skilgreina runuvinnslu sem eyðir eldri uppfyllingaráætlunum, sem byggir á gildinu **Varðveislutími í dögum**.

1. Opnið **Retail and Commerce \> Dreifingarstjórnun pöntunar \> Runuvinnsla \> Uppsetning á eyðingarvinnslu DOM-uppfyllingargagna**. 
1. Í reitnum **Runuflokkur** skal velja grunnstilltan runuflokk.
1. Veljið **Endurtekning** og skilgreinið endurtekningu runuvinnslunnar.
1. Veljið **Í lagi**.

## <a name="more-information"></a>Frekari upplýsingar

Hér eru nokkur atriði til að hafa í huga þegar DOM-eiginleikinn er notaður:

- Sem stendur skoðar DOM aðeins pantanir sem eru stofnaðar úr viðskiptarásum. Litið er á sölupantanir sem sölupantanir þegar valkosturinn **Commerce-sala** er stilltur á **Já**.
- Microsoft hefur ekki prófað DOM með ítarlegum eiginleikum vöruhúsakerfis. Viðskiptavinir og samstarfsaðilar verða því að fara varlega í að ákvarða hvort DOM sé samhæft við ítarlegar aðgerðir og ferla vöruhúsakerfisins sem eiga við þá. Ítarlegar vöruhúsaaðgerðir virkja stillanlegar víddir, eins og birgðastöðu, sem veita ekki nákvæman skilning á tiltækum birgðum. DOM býður upp á sveigjanlega aðferð við að stilla tiltækar birgðir við innleiðingar sem nota ítarlegar vöruhúsaaðgerðir. Hægt er að nota það til að vinna með sérsniðin gildi birgðastöðu og annarra vídda.

    Sveigjanleiki DOM er takmarkaður vegna þess að fínstilling fer fram í forsmíðuðu MIP-líkani sem tekur tillit til fínstillingarinnar og takmarkana hennar. Nokkrir sveigjanleikapunktar eru þegar í boði til að stilla fínstillingu birgða og eftirvinnslu. DOM-forstillingar geta verið mismunandi eftir uppruna sölu og afhendingarmáta. Hægt er að stilla uppruna sölupöntunar við móttöku pantana og hægt er að nota mismunandi fínstillingaáætlanir í samræmi við þessi gildi. DOM styður einnig að búa til sérsniðnar runuvinnslur sem geta tekið við verki DOM-vinnslu sem inntaki og láta samþykkja forstillingu sem færibreytu. Þannig er hægt að keyra fínstillingar hverja á fætur annarri til að styðja við ólík viðskiptaferli.

- DOM er aðeins í boði í skýjaútgáfu Commerce. Það er ekki stutt fyrir uppsetningar á staðnum.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
