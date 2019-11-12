---
title: Dreifingarstjórnun pöntunar (DOM)
description: Þetta efnisatriði lýsir virkni dreifingarstjórnunar pöntunar (DOM) í Dynamics 365 Retail.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0ebac1c3f9f79ee49ae11a121a4a0dd3bd456c8f
ms.sourcegitcommit: bdbca89bd9b328c282ebfb681f75b8f1ed96e7a8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578485"
---
# <a name="distributed-order-management-dom"></a>Dreifingarstjórnun pöntunar (DOM)

[!include [banner](includes/banner.md)]

Í nýjum viðmiðum smásöluaðgerða leggja smásöluaðilar áherslu á að bjóða upp á sérsniðin tengsl við viðskiptavini, alhliða upplifun og hnökralaus samskipti. Svo margir valkostir eru í boði og munu viðskiptavinir því versla þar sem þeir njóta bestu upplifunarinnar. Í mörgum tilfellum hafa verð og afurðir ekki lengur úrslitaáhrif á ákvarðanatökur viðskiptavina.

Til að bæta upplifun viðskiptavina verða smásöluaðilar að geta séð birgðir í rauntíma í öllum rásum. Eitt, heildrænt yfirlit yfir allar birgðir getur hjálpað til við að hámarka uppfyllingu, úthlutun og dreifingu pöntunar. Þess vegna er upptaka og innleiðing á kerfi dreifingarstjórnunar pöntunar (DOM) að verða meira aðkallandi fyrir smásöluaðila.

DOM hámarkar uppfyllingu pöntunar yfir mörg flókin kerfi og ferla. DOM reiðir sig á eitt, heildaryfirlit birgða yfir allt fyrirtækið til að stjórna pöntunum á snjallan hátt, svo þær verði rétt uppfylltar og með hagkvæmari hætti. DOM auðveldar smásöluaðilum að uppfylla væntingar viðskiptavina með því að auka skilvirkni aðfangakeðju smásölu.

Eftirfarandi skýringarmynd sýnir ferli sölupöntunar í DOM-kerfi.

![Ferli sölupöntunar í samhengi við DOM](./media/flow.png "Ferli sölupöntunar í samhengi við DOM")

## <a name="set-up-dom"></a>Setja upp DOM

1. Opnið **Kerfisstjórnun \> Setja upp \> Skilgreining leyfis**.
2. Á flipanum **Skilgreiningarlykill** skal stækka hnútinn **Retail** og síðan velja gátreitinn **Dreifingarstjórnun pöntunar**.
3. Opnið **Retail \> Dreifingarstjórnun pöntunar \> Setja upp \> DOM færibreytur**.
4. Á flipanum **Almennt** skal stilla eftirfarandi gildi:

    - **Virkja dreifingarstjórnun pöntunar** – Stillið þennan valkost á **Já**.
    - **Staðfesta notkun á Bing-kortum fyrir DOM** – Stillið þennan valkost á **Já**.

        > [!NOTE]
        > Aðeins er hægt að stilla þennan valkost á **Já** ef valkosturinn **Virkja Bing-kort** á flipanum **Bing-kort** á síðunni **Samnýttar færibreytur Retail** (**Retail \> Uppsetning höfuðstöðva\> Færibreytur \> Samnýttar færibreytur Retail**) er einnig stilltur á **Já**, og ef gildur lykill er sleginn inn í reitinn **Lykill Bing-korts**.

    - **Varðveislutími í dögum** – Tilgreinið hversu lengi á að geyma uppfyllingaráætlanir í kerfinu, sem DOM-keyrslur búa til. Runuvinnslan **Uppsetning á eyðingarvinnslu DOM-uppfyllingargagna** eyðir öllum uppfyllingaráætlunum sem eru eldri en dagafjöldinn sem tilgreindur er hér.
    - **Höfnunartímabil (í dögum)** – Tilgreinið tímann sem þarf að líða áður en hægt er að úthluta hafnaðri pöntunarlínu á sömu staðsetninguna.

5. Á flipanum **Leysari** skal stilla eftirfarandi gildi:

    - **Hámarksfjöldi sjálfvirkra uppfyllingatilrauna** – Tilgreinið hversu oft DOM-vélin reynir að miðla pöntunarlínu á staðsetningu. DOM-vélin flaggar pöntunarlínu sem undantekningu ef hún getur ekki miðlað pöntunarlínunni á staðsetningu í tilgreindum fjölda tilrauna. Hún mun þá sleppa þeirri línu í framtíðarkeyrslum þar til staðan er endurstillt handvirkt.
    - **Nærliggjandi landsvæði svæðisbundinnar verslunar** – Færið inn gildi. Þessi reitur auðveldar að ákvarða hvernig staðsetningar eru flokkaðar saman og litið á sem jafnar hvað varðar fjarlægð. Ef til að mynda fært er inn **100** verður litið á allar verslanir eða dreifingarstöðvar innan 100 mílna radíuss frá aðsetri uppfyllingar sem jafnar hvað varðar fjarlægð.
    - **Gerð leysara** – Veljið gildi. Tvær gerðir af leysara eru gefnar út með Retail: **Leysari framleiðslu** og **Einfaldaður leysari**. Velja þarf **Leysari framleiðslu** fyrir allar vélar sem munu keyra DOM (sem sagt allir þjónar sem eru hluti af DOMBatch-flokknum). Leysari framleiðslu krefst tiltekins leyfislykils sem er að sjálfgefnu leyfður og uppsettur í vinnsluumhverfi. Þennan leyfislykil þarf að setja upp handvirkt fyrir umhverfi sem er ekki vinnsluumhverfi. Til að setja upp leyfislykilinn handvirkt skal fylgja þessum skrefum:

        1. Opnið samnýtta eignasafnið í Microsoft Dynamics Lifecycle Services og veljið **Líkan** sem eignagerð og sækið skrána **DOM-leyfi**.
        2. Ræsið Microsoft Internet Information Services (IIS), hægrismellið á **Vefsvæði AOSService** og veljið síðan **Skoða**. Windows Explorer-gluggi opnast á **\<AOS service rooy\>\\webroot**. Skrifa skal niður slóðina fyrir \<AOS Service root\> vegna þess að hún verður notuð í næsta skrefi.
        3. Afritið skilgreiningarskrána í skráasafninu **\<Rót AOS Service\>\\PackagesLocalDirectory\\DOM\\hólf**.
        4. Opnaðu biðlara Retail Headquarters og opnaðu svo síðuna **DOM-færibreytur**. Á flipanum **Leysari**, í reitnum **Gerð leysara** skal velja **Leysari framleiðslu** og staðfesta að engin villuboð birtist.

        > [!NOTE]
        > Einfaldaður leysari er útvegaður svo smásöluaðilar geti prófað DOM-eiginleikann án þess að þurfa að setja upp tiltekið leyfi. Fyrirtæki eiga ekki að nota einfaldaðan leysara í vinnsluumhverfi.
        >
        > Einfaldaði leysarinn býður upp á sömu eiginleika og leysari framleiðslu, en þó eru takmarkanir hvað varðar frammistöðu (fjöldi pantana og pöntunarlína sem hægt er að vinna með í keyrslu) og samleitni niðurstaðna (runa pantana kemur ekki endilega með bestu niðurstöðuna í sumum tilfellum).
     
6. Farið aftur í **Retail \> Dreifingarstjórnun pöntunar \> Setja upp \> DOM-færibreytur**.
7. Á flipanum **Númeraraðir** skal úthluta áskildum númeraröðum á hinar ýmsu DOM-einingar.

    > [!NOTE]
    > Áður en hægt er að úthluta númeraröðum á einingarnar verða þær að vera skilgreindar á síðunni **Númeraraðir** (**Fyrirtækisstjórnun \> Númeraraðir \> Númeraraðir**).

8. DOM-eiginleikinn styður skilgreininguna á ýmsum gerðum DOM-reglna, og fyrirtæki geta skilgreint margar reglur, allt eftir rekstrarþörfum þeirra. Hægt er að skilgreina DOM-reglur fyrir flokk af staðsetningum eða einkvæmar staðsetningar, og fyrir tilgreinda afurðategund, afurð eða vöruvíddasamsetningu. Til að stofna flokkun á staðsetningum sem verður að nota fyrir DOM-reglurnar skal fylgja þessum skrefum:

    1. Opnið **Retail \> Uppsetning rásar \> Uppfyllingarflokkar**.
    2. Veljið **Nýr** og færið inn heiti og lýsingu á nýja flokknum.
    3. Veljið **Vista**.
    4. Veljið **Bæta við línu** til að bæta einni staðsetningu við flokkinn. Að öðrum kosti skal velja **Bæta við línum** til að bæta við mörgum staðsetningum.

9. Til að skilgreina reglur skal opna **Retail \> Dreifingarstjórnun pöntunar \> Setja upp \> Stjórna reglum**. Eftirfarandi DOM-reglur eru studdar eins og er:

    - **Regla lágmarksbirgða** – Þessi gerð af reglu gerir fyrirtækjum kleift að aðgreina tilgreint magn afurðar í öðrum tilgangi en fyrir uppfyllingu pöntunar. Sem dæmi er hugsanlegt að fyrirtæki vilji ekki að DOM taki allar tiltækar birgðir í verslun til greina við uppfyllingu pöntunar. Í staðinn gætu þau viljað taka frá einhverjar birgðir fyrir viðskiptavini á staðnum. Þegar þessi gerð af reglu er notuð er hægt að skilgreina lágmarksbirgðir sem á að geyma fyrir flokk af afurðum, staka afurð eða afurðarafbrigði fyrir hverja staðsetningu eða flokk staðsetninga.
    - **Forgangsregla uppfyllingarstaðsetningar** – Þessi gerð af reglu gerir fyrirtækjum kleift að skilgreina stigveldi staðsetninga til að koma á forgangi sem DOM-vélin hefur í huga þegar hún reynir að bera kennsl á uppfyllingarstaðsetningar fyrir tilgreindar afurðir. Gilt svið forgangs er frá 1 til 10, þar sem 1 er efst í forgangi og 10 er neðst í forgangi. Staðsetningar sem eru ofar í forgangsröðinni eru teknar til greina á undan staðsetningum sem eru neðar í forgangsröðinni. Pöntunum er aðeins miðlað á staðsetningar þar sem forgangur er skilgreindur, ef reglan er skilgreind sem ströng takmarkandi regla.
    - **Regla fyrir hlutapantanir** – Þessi regla gerir fyrirtækjum kleift að skilgreina hvort hægt sé að uppfylla pöntun eða pöntunarlínur að hluta til. Eftirfarandi færibreytur eru tiltækar:

        - **Uppfylla hlutapantanir?** – Ef þessi valkostur er stilltur á **Já** getur DOM aðeins uppfyllt hluta af magni pöntunarlínu. Þessi uppfylling að hluta til er gerð með því að skipta pöntunarlínunni.
        - **Uppfylla hlutalínur?** – Ef þessi valkostur er stilltur á **Já** getur DOM aðeins uppfyllt hluta af magni pöntunarlína. Þessi uppfylling að hluta til er gerð með því að skipta pöntunarlínunni.
        - **Uppfylla pöntun aðeins frá einni staðsetningu** – Ef þessi valkostur er stilltur á **Já** gengur DOM úr skugga um að allar línur pöntunar séu uppfylltar frá einni staðsetningu.


        Eftirfarandi tafla útskýrir hegðunina þegar samsetning þessara færibreyta er skilgreind.

        |      | Uppfylla hlutapantanir | Uppfylla hlutalínur | Uppfylla pöntun aðeins frá einni staðsetningu | Lýsing |
        |------|------------------------|-----------------------|--------------------------------------|-------------|
        | 1    | Já                    | Já                   | Já                                  | Hægt er að uppfylla nokkrar línur pöntunarinnar og hægt er að uppfylla stakar línur að hluta til, en allar línurnar verða að koma frá sömu staðsetningunni í tilviki DOM-keyrslu. (Þessi samsetning er ekki studd eins og er.) |
        | 2    | Já                    | Nei                    | Já                                  | Hægt er að uppfylla nokkrar línur pöntunarinnar en ekki er hægt að uppfylla stakar línur að hluta til, og allar uppfylltu línurnar verða að koma frá sömu staðsetningunni í tilviki DOM-keyrslu. (Þessi samsetning er ekki studd eins og er.) |
        | 3    | Já                    | Já                   | Nei                                   | Hægt er að uppfylla nokkrar línur pöntunarinnar, hægt er að uppfylla stakar línur að hluta til, og hægt er að uppfylla hverja línu frá fleiri en einni staðsetningu í tilviki DOM-keyrslu. |
        | 4\*  | Nei                     | Á ekki við        | Nei                                   | Uppfylla þarf allar pöntunarlínur, ekki er hægt að uppfylla stakar línur að hluta til, og hægt er að uppfylla hverja pöntunarlínu frá mismunandi staðsetningum. |
        | 5\*  | Nei                     | Á ekki við        | Já                                  | Uppfylla þarf allar pöntunarlínur, ekki er hægt að uppfylla stakar línur að hluta til, og aðeins er hægt að afhenda allar pöntunarlínur frá einni staðsetningu. |
        | 6\*  | Nei                     | Á ekki við        | Nei                                   | Þessi samsetning virkar eins og samsetning 4 vegna þess að ekki er hægt að stilla **Uppfylla hlutalínur** á **Já** þegar **Uppfylla hlutapantanir** er stillt á **Nei**. |
        | 7\*  | Nei                     | Á ekki við        | Já                                  | Þessi samsetning virkar eins og samsetning 5 vegna þess að **Uppfylla hlutalínur** getur ekki verið **Já** þegar **Uppfylla hlutapantanir** er **Nei**. |
        | 8    | Já                    | Nei                    | Nei                                   | Hægt er að uppfylla nokkrar línur pöntunarinnar, en ekki er hægt að uppfylla stakar línur að hluta til, og hægt er að uppfylla hinar ýmsu pöntunarlínur frá fleiri en einni staðsetningu í tilviki DOM-keyrslu. |
        | 9\*  | Nei                     | Á ekki við        | Já                                  | Uppfylla þarf allar pöntunarlínur og það frá aðeins einni staðsetningu. |

        \* Ef **Uppfylla hlutapantanir** er stillt á **Nei** er alltaf litið svo á að **Uppfylla hlutalínur** sé stillt á **Nei**, óháð því hver stillingin er í raun og veru.

> [!NOTE]
> Í Retail, útgáfu 10.0.5, var færibreytunni **Uppfylla pöntun aðeins frá einni staðsetningu** breytt í **Hámarksstaðsetning uppfyllingar**. Í stað þess að leyfa notanda að skilgreina hvort aðeins sé hægt að uppfylla pantanir á einum stað eða uppfylla á eins mörgum stöðum og mögulegt er geta notendur nú tilgreint hvort hægt sé að uppfylla þær á ákveðnum fjölda staðsetninga (allt að fimm), eða frá eins mörgum stöðum og mögulegt er. Þetta veitir meiri sveigjanleika í fjölda staðsetninga sem hægt er að uppfylla pöntunina á.

   - **Staðsetningarregla uppfyllingar utan nets** – Þessi regla gerir fyrirtækjum kleift að tilgreina staðsetningu eða flokk staðsetninga sem utan nets eða ekki tiltæka fyrir DOM, svo ekki sé hægt að úthluta pöntunum á þessar staðsetningar til uppfyllingar.
    - **Regla um hámark hafnana** – Þessi regla gerir fyrirtækjum kleift að skilgreina mörk fyrir hafnanir. DOM-vinnslan mun merkja pöntun eða pöntunarlínu sem undantekningu þegar mörkum er náð og útiloka hana frá frekari úrvinnslu.

        Eftir að pöntunarlínum er úthlutað á staðsetningu getur staðsetningin hafnað úthlutaðri pöntunarlínu vegna þess að hún getur mögulega ekki uppfyllt þessa línu af einhverjum ástæðum. Hafnaðar línur eru merktar sem undantekning og settar aftur í safnið til vinnslu í næstu keyrslu. Við næstu keyrslu reynir DOM að úthluta höfnuðum línum á aðra staðsetningu. Nýja staðsetningin getur einnig hafnað úthlutaðri pöntunarlínu. Þessi hringrás úthlutunar og höfnunar getur átt sér stað mörgum sinnum. Þegar talning höfnunar nær skilgreindum mörkum merkir DOM pöntunarlínuna sem varanlega undantekningu og kemur ekki til með að velja þessa línu til úthlutunar aftur. DOM tekur pöntunarlínuna eingöngu aftur til greina fyrir endurúthlutun ef notandi endurstillir stöðu pöntunarlínunnar handvirkt.

   - **Regla um hámarksfjarlægð** – Þessi regla gerir fyrirtækjum kleift að skilgreina hámarksfjarlægð sem staðsetning eða flokkur staðsetninga getur verið í til að uppfylla pöntun. Ef skilgreindar reglur um hámarksfjarlægð fyrir staðsetningu skarast, notar DOM lægstu hámarksfjarlægð sem er skilgreind fyrir þá staðsetningu.
    - **Regla um hámarkspantanir** – Þessi regla gerir fyrirtækjum kleift að skilgreina hámarksfjölda pantana sem staðsetning eða flokkur staðsetninga getur unnið úr á almanaksdegi. Ef hámarksfjölda pantana er úthlutað á staðsetningu á einum degi úthlutar DOM ekki fleiri pöntunum á þessa staðsetningu það sem eftir lifir almanaksdagsins.

   Hér eru nokkrar algengar eigindir sem hægt er að skilgreina fyrir allar undanfarandi gerðir af reglum:

   - **Upphafsdagur** og **Lokadagur** – Hægt er að gera allar reglur dagsetningamiðaðar með þessum reitum.
   - **Gera óvirkar** – Einungis reglur sem hafa gildið **Nei** fyrir þennan reit eru teknar til greina í DOM-keyrslu.
   - **Ströng takmarkandi** – Regla getur verið skilgreind sem annaðhvort ströng takmarkandi eða ekki ströng takmarkandi. Allar DOM-keyrslur fara í gegnum tvær ítrekanir. Í fyrri ítrekuninni er hver regla meðhöndluð sem ströng takmarkandi regla, óháð því hver stilling reitsins er. Það er að segja, allar reglur eru í gildi. Eina undantekningin er reglan **Forgangur staðsetningar**. Í seinni ítrekuninni eru reglurnar, sem ekki voru skilgreindar sem strangar takmarkandi reglur, fjarlægðar og pöntunum eða pöntunarlínum, sem ekki var úthlutað á staðsetningu þegar allar reglurnar voru í gildi, er úthlutað á staðsetningar.

10. Uppfyllingarsnið eru notuð til að flokka safn af reglum, lögaðilum, söluuppruna pantana og afhendingarmátum. Hver DOM-keyrsla er fyrir tiltekið uppfyllingarsnið. Á þennan hátt geta fyrirtæki skilgreint og keyrt safn af reglum fyrir safn af lögaðilum á pöntunum sem eru með tiltekinn söluuppruna pantana og tiltekinn afhendingarmáta. Því er hægt að skilgreina uppfyllingarsnið eins og við á ef keyra þarf ólík reglusöfn fyrir ólík söfn af söluuppruna pantana eða afhendingarmáta. Til að setja upp uppfyllingarsnið skal fylgja þessum skrefum:  

    1. Opnið **Retail \> Dreifingarstjórnun pöntunar \> Setja upp \> Uppfyllingarsnið**.
    2. Veljið **Nýtt**.
    3. Færið inn gildi í reitina **Snið** og **Lýsing**.
    4. Stillið valkostinn **Nota niðurstöðu sjálfkrafa**. Ef þessi valkostur er stilltur á **Já** verða niðurstöður DOM-keyrslu fyrir sniðið sjálfkrafa notaðar í sölupöntunarlínum. Ef hann er stilltur á **Nei** verður eingöngu hægt að skoða niðurstöðurnar í uppfyllingaráætlun. Þær verða ekki notaðar í sölupöntunarlínum.
    5. Ef keyra á DOM-sniðið fyrir pantanir sem eru með söluuppruna allra pantana, jafnvel þeirra þar sem uppruninn er óskilgreindur, skal stilla valkostinn **Vinna úr pöntunum með auðan söluuppruna** á **Já**. Til að keyra sniðið fyrir aðeins nokkra söluuppruna pantana er hægt að skilgreina þá á síðunni **Söluupprunar** líkt og verður útskýrt síðar.
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

1. Opnið **Retail \> Dreifingarstjórnun pöntunar \> Runuvinnsla \> Verkuppsetning DOM-vinnslu**.
1. Á flýtiflipanum **Færibreytur**, í reitnum **Uppfyllingarsnið** skal velja snið sem DOM þarf að keyra fyrir.
1. Á flýtiflipanum **Keyra í bakgrunni**, í reitnum **Runuflokkur** skal velja grunnstilltan runuflokk.
1. Í reitinn **Verklýsing** skal færa inn heiti á runuvinnslunni.
1. Veljið **Endurtekning** og skilgreinið endurtekningu runuvinnslunnar.
1. Veljið **Í lagi**.

Við vinnslu tekur DOM tillit til pöntunar og pöntunarlína eins og hér er lýst:

- Pöntunarlínur sem uppfylla skilyrði fyrir söluuppruna pöntunar, afhendingarmáta og lögaðila eins og það er skilgreint í DOM-sniðinu, og sem uppfylla einhver þessara skilyrða:

    - Þær eru stofnaðar úr smásölurásum.
    - Þeim hefur aldrei verið miðlað af hálfu DOM.
    - Þeim hefur aldrei verið miðlað af hálfu DOM áður, en þær eru merktar sem undantekningar og eru undir mörkum hámarkstilrauna.
    - Afhendingarmátinn er ekki að sækja eða afhenda rafrænt.
    - Þær eru ekki merktar til afhendingar.
    - Þær eru ekki útilokaðar handvirkt.

- Pantanir sem eru ekki í bið

DOM velur staðsetningu sem er næst afhendingaraðsetri viðskiptavinar eftir að það setur á reglur, birgðatakmarkanir og hámörkun.

![Skilyrði sölupöntunar](./media/ordercriteria.png "Skilyrði sölupöntunar")

## <a name="results-of-dom-runs"></a>Niðurstöður DOM-keyrslna

Ef uppfyllingarsnið er stillt á **Nota sjálfkrafa** verða niðurstöður keyrslunnar notaðar sjálfkrafa í sölupöntunarlínum, og hægt verður að sjá uppfyllingaráætlun sérstaklega. Ef uppfyllingarsnið er hins vegar ekki stillt á **Nota sjálfkrafa** verður aðeins hægt að sjá niðurstöður keyrslunnar í yfirliti uppfyllingaráætlunar. 

Til að skoða allar uppfyllingaráætlanir sem eru búnar til skal fylgja þessum skrefum.

1. Opnið **Retail \> Dreifingarstjórnun pöntunar \> Dreifingarstjórnun pöntunar**.
2. Á vinnusvæðinu **Dreifingarstjórnun pöntunar** skal velja reitinn **Uppfyllingaráætlanir**.
3. Veljið kennið fyrir viðeigandi uppfyllingaráætlun pöntunar til að skoða uppfyllingaráætlunina.

    Upplýsingahluti pöntunar í uppfyllingaráætlun sýnir upprunalegar sölupöntunarlínur sem voru hluti af keyrslunni. Fyrir utan hefðbundna reiti sölupöntunarlínu inniheldur upplýsingahluti pöntunar einnig eftirfarandi þrjá reiti sem tengjast DOM:

    - **Uppfyllingargerð** – Þessi reitur sýnir hvort sölupöntunarlína sé miðluð að fullu, miðluð að hluta til eða ekki miðluð á staðsetningu.
    - **Skipta** – Þessi reitur sýnir hvort einni sölupöntunarlínu hafi verið skipt og henni miðlað á mismunandi staðsetningar.
    - **Fjöldi uppfyllingarstaðsetninga** – Þessi reitur sýnir hversu margar uppfyllingarlínur voru stofnaðar fyrir eina sölupöntunarlínu (byggt á fjölda staðsetninga sem upprunalegri sölupöntunarlínu var miðlað á).

    Upplýsingahlutinn um uppfyllingu pöntunar sýnir úthlutun upprunalegra sölupöntunarlína á mismunandi staðsetningar, ásamt magni þeirra.

## <a name="order-line-actions-and-statuses"></a>Aðgerðir og stöður pöntunarlínu

Eftirfarandi lýsir stillingum á pöntunarlínum. Til að opna pöntunarlínu skal opna **Retail \> Viðskiptavinir \> Allar sölupantanir**.
- Ef valkosturinn **Útiloka frá DOM-vinnslu** á flipanum **Almennt** í sölupöntunarlínu er stilltur á **Já** verður pöntun eða pöntunarlína útilokuð frá DOM-vinnslu.
- Hægt er að stilla reitinn **DOM-staða** á flipanum **Almennt** í sölupöntunarlínu á eitt af eftirfarandi gildum:

    - **Ekkert** – Pöntunarlínunni hefur aldrei verið miðlað.
    - **Að fullu** – Pöntunarlínunni hefur verið miðlað og úthlutað á staðsetningu.
    - **Undantekning** – Pöntunarlínunni hefur verið miðlað en ekki er hægt að úthluta henni á staðsetningu. Undantekningar eru með margar undirgerðir sem hægt er að skoða á vinnusvæðinu:

        - **Ekkert magn er tiltækt** – Engar tiltækar birgðir eru til sem hægt er að úthluta pöntun á í staðsetningum.
        - **Hámarksfjöldi hafnana** – Pöntunarlína hefur náð hámarksfjölda hafnana.
        - **Árekstrar við breytingu á gögnum** – Sölupöntunarlínu hefur verið breytt síðan pöntun var miðluð. Þess vegna er ekki hægt að nota uppfyllingaráætlunina fyrir pöntunina.
        - **Sérstök undantekning pöntunarlínu** – Margar undantekningar eru á pöntunarlínu.

- Hægt er að keyra DOM í gagnvirku sniði meðan á færslu sölupöntunar stendur. Við innslátt pöntunarlínu, eftir að afurð og magn hefur verið tilgreint, er hægt að velja **Uppfæra línu** og síðan, undir **DOM**, skal velja **Stinga upp á uppfyllingarstaðsetningu**. Þá sést listi yfir staðsetningar sem byggjast á DOM-reglum sem geta uppfyllt magnið á pöntunarlínunni. Á þennan lista er raðað eftir fjarlægð. Veljið staðsetningu til að setja viðeigandi svæði og vöruhús á sölupöntunarlínuna. Til að þessi virkni virki sem skyldi þarf að vera til staðar virkt uppfyllingarsnið sem passar við söluuppruna og afhendingarmáta á sölulínunni.
- Til að skoða skrár DOM-keyrslu fyrir sölupöntunarlínu skal velja **Sölupöntunarlína** og síðan, undir **DOM**, velja **Skoða DOM-skrár**. DOM-skrárnar sýna öll tilvik og skrár sem DOM-keyrslan bjó til. Skrárnar hjálpa til við að skilja hvers vegna tilgreindri staðsetningu var úthlutað á pöntunarlínu og hvaða reglur og takmarkanir voru íhugaðar sem hluti af úthlutuninni. DOM-skrárnar eru einnig tiltækar á stigi sölupöntunarhauss á flipanum **Stjórna**.

## <a name="run-a-clean-up-job-for-dom-fulfillment-plans"></a>Keyrið hreinsunarverk fyrir uppfyllingaráætlanir DOM

Uppfyllingaráætlanir eru stofnaðar á meðan DOM-vinnsla keyrir. Með tímanum mun kerfið geyma fjöldann allan af uppfyllingaráætlunum. Til að stjórna fjölda uppfyllingaráætlana sem kerfið geymir er hægt að skilgreina runuvinnslu sem eyðir eldri uppfyllingaráætlunum, sem byggir á gildinu **Varðveislutími í dögum**.

1. Opnið **Retail \> Dreifingarstjórnun pöntunar \> Runuvinnsla \> Uppsetning á eyðingarvinnslu DOM-uppfyllingargagna**. 
1. Í reitnum **Runuflokkur** skal velja grunnstilltan runuflokk.
1. Veljið **Endurtekning** og skilgreinið endurtekningu runuvinnslunnar.
1. Veljið **Í lagi**.

## <a name="more-information"></a>Frekari upplýsingar

Hér eru nokkur atriði til að hafa í huga þegar DOM-eiginleikinn er notaður:

- Sem stendur skoðar DOM aðeins pantanir sem eru stofnaðar úr smásölurásum. Litið er á sölupantanir sem smásölupantanir þegar valkosturinn **Retail-sala** er stilltur á **Já**.
- Microsoft hefur ekki prófað DOM með ítarlegum eiginleikum vöruhúsakerfis. Viðskiptavinir og samstarfsaðilar verða að fara varlega í að ákvarða hvort DOM sé samhæft við ítarlegar aðgerðir og ferla vöruhúsakerfisins sem eiga við þá.
- DOM er aðeins í boði í skýjaútgáfu Retail. Það er ekki stutt fyrir uppsetningar á staðnum.
