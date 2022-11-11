---
title: Forgangsröðuð áætlun
description: Þessi grein lýsir forgangsbundinni áætlanagerð Microsoft Dynamics 365 Supply Chain Management.
author: t-benebo
ms.date: 10/15/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-10-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 1a952fe5734f01325842a8a130b9322eadc67951
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740593"
---
# <a name="priority-based-planning"></a>Forgangsröðuð áætlun

[!include [banner](../../includes/banner.md)]

Þessi grein lýsir forgangsbundinni áætlanagerð Microsoft Dynamics 365 Supply Chain Management. Eiginleikinn bætir við stuðningi við eftirspurnardrifna áætlanagerð, sem er eitt skref í [Eftirspurnardrifin efnisþörf áætlanagerð (DDMRP)](ddmrp-overview.md). Forgangsmiðuð áætlanagerð gerir kerfinu kleift að búa til skipulagðar pantanir sem eru knúnar áfram af forgangsröðun áætlana í stað kröfudagsetninga.

Forgangsmiðuð áætlanagerð gerir þér kleift að forgangsraða áfyllingarpöntunum til að tryggja að brýnni eftirspurn sé forgangsraðað fram yfir minna mikilvæga eftirspurn. Til dæmis verður áfyllingarpöntun á lager sett í forgang fram yfir venjulega áfyllingarpöntun. Kerfið getur sjálfkrafa skipt stærri pöntunum í aðskildar smærri pantanir þar sem pöntunarlínur eru flokkaðar eftir forgangi. Það getur þá afgreitt allar forgangspantanir fyrst.

Til að fá fljótt yfirlit yfir þennan eiginleika skaltu skoða eftirfarandi myndband: [Stuðningur við skipulagshagræðingu fyrir forgangsmiðaða áætlanagerð í Dynamics 365 Supply Chain Management](https://youtu.be/GmMHzFETTQc).

## <a name="turn-on-priority-based-planning-in-your-system"></a>Kveiktu á forgangsbundinni áætlanagerð í kerfinu þínu

Áður en þú getur notað þennan eiginleika verður að kveikja á honum fyrir kerfið þitt. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Aðaláætlanagerð*
- **Eiginleikaheiti:** *Forgangsdrifinn MRP stuðningur fyrir hagræðingu áætlanagerðar*

## <a name="where-and-how-planning-priorities-are-assigned"></a>Hvar og hvernig forgangsröðun í skipulagsmálum er úthlutað

*Skipulagsforgangur* upplýsingar um framboð og eftirspurn eru burðarás forgangsmiðaðrar áætlanagerðar. Skipulagsforgangur skilgreinir mikilvægi eftirspurnar- eða framboðslínu. Aðalskipulag notar það þegar **Umfjöllunarkóði** reiturinn er stilltur á *Forgangur*.

Skipulagsforgangur er venjulega tala á milli 0 (núll) og 100, þar sem 0 táknar mesta mikilvægi. Það er sýnt og sett í **Skipulagsforgangur** sviði. Þú getur fundið þennan reit á eftirfarandi síðum: **Eftirspurnarspálínur**, **um sölupöntun**, **um innkaupapöntun**, **pöntunarupplýsingar**, og **Fyrirhugaðar pöntunarupplýsingar**.

Þegar **Umfjöllunarkóði** reiturinn fyrir viðkomandi vöru eða þekjuhóp er stilltur á *Forgangur*, aðalskipulag jafnvægir framboð og eftirspurn með því að nota eftirspurnardrifna nálgun þar sem hún reiknar út áætlunarforgang og, fyrir hverja útgefna vöru, tekur tillit til gilda sem eru sett fyrir **Lágmark**, **punkt**, og **Hámark** sviðum á **Vöruumfjöllun** síðu.

> [!NOTE]
> The *Forgangur* gildi er í boði fyrir **Umfjöllunarkóði** reit aðeins þegar áætlanagerð fínstilling er virkjuð.

Hið tengda *áætlanagerð forgangslíkön* stjórna áætlunarforganginum og skipta skipulögðum pöntunum eftir forgangssviði. Þeir leyfa þér einnig að stilla sjálfgefin áætlanagerð forgangsgildi fyrir hverja framboðs- eða eftirspurnartegund og skilgreina forgangsútreikningsaðferðina.

## <a name="types-of-priority-calculation-methods"></a>Tegundir forgangsútreikningsaðferða

Hvert áætlanagerð forgangslíkan hefur a **Forgangsreikningsaðferð** stilling sem stjórnar því hvernig aðalskipulag beitir forgangi á áætlaðar pantanir. Tiltæk gildi eru *Hlutfall af hámarks birgðamagni* og *Forgangssvið*. *Forgangssvið* táknar fullkomnari útgáfu af *Hlutfall af hámarks birgðamagni* aðferð.

### <a name="percent-of-maximum-inventory-quantity"></a>Hlutfall af hámarks birgðamagni

Í *Hlutfall af hámarks birgðamagni* útreikningsaðferð finnur forgangsútreikningur framboðsins strauminn *heildar tiltækar birgðir* (nettóflæði) sem hlutfall af **Hámarks birgðamagn** gildi sem er stillt fyrir hlut. Ein skipulögð pöntun er síðan búin til fyrir hverja vöru og lánardrottna (nema hámarks pöntunarmagn sé notað til að knýja fram skiptingu). Skipulagsforgangur pöntunarinnar er reiknaður sem hlutfall af hámarki.

Eftirfarandi formúla er notuð:

*Hlutfall af hámarki* = (*Nettóflæðisstaða* × 100) ÷*Hámarksverðmæti birgðamagns frá vöruþekju*

Í þessari formúlu, *Nettóflæðisstaða* er reiknað á eftirfarandi hátt:

*Nettóflæðisstaða* = *Á hendi* + *Á pöntun* –*Hæfð eftirspurn*

- *Á pöntun* er væntanlegt framboð.
- *Hæfð eftirspurn* táknar nettóþarfir sem hafa kröfudagsetninguna innan skipulagstímagirðingar.

Meðan á aðalskipulagskeyrslunni stendur eru nýjar áætlaðar pantanir búnar til þegar nettóflæðisstaða er minni en endurpöntunarpunktamagn vöru. Fyrirhugað pöntunarmagn er munurinn á milli **Hámarks birgðamagn** gildi sem er stillt á vörustigi og nettóflæðisstöðu. Fyrirhugaður pöntunarforgangur er reiknaður sem a *nettó flæðisstaða* hlutfall af **Hámarks birgðamagn** gildi.

> [!NOTE]
> Reiknaður forgangur getur ekki verið neikvæður, jafnvel þótt eftirspurn sé meiri en heildarframboð. Ef eftirspurn er meiri en heildarframboð er reiknaður forgangur stilltur á 0 (núll).

### <a name="priority-ranges"></a>Forgangssvið

The *Forgangssvið* reikningsaðferðin er fullkomnari en *Hlutfall af hámarks birgðamagni* aðferð og er stillt á stigi forgangslíkans áætlanagerðar. Hægt er að búa til nokkrar nýjar fyrirhugaðar framboðspantanir til að uppfylla eftirspurn á hverja vöru. Forgangsröðun fyrirhugaðs framboðs fylgir þeim gildum sem eru skilgreind í **Skipuleggja forgangssvið** rist á **Skipulags forgangslíkön** síðu.

Eftirfarandi viðbótarreglur taka gildi þegar **Forgangsreikningsaðferð** reiturinn er stilltur á *Forgangssvið*:

- Ef **Íhugaðu forgang eftirspurnar** valkostur fyrir fyrirhugað forgangslíkan er stillt á *Já*, forgangur sem er stilltur á hverja eftirspurnarlínu mun takmarka forgangssviðssviðið. Forgangur nýrrar fyrirhugaðrar pöntunar á framboði verður ekki lægri en forgangur eftirspurnar. Efri gildi bilsins er talið vera þröskuldur sem forgangsgildi eftirspurnar er borið saman við. Ef forgangur eftirspurnar er nákvæmlega í miðjunni á milli efri þröskuldsgilda tveggja sviða, verður það svið sem hefur hæsta forgang (þ.e. lægsta forgangsgildi) valið.
- Ef **Fyrirhuguð pöntunargerð** reit fyrir fyrirhugað forgangslíkan er stillt á *Eitt framboð með mikilvægasta forgang*, aðeins eitt framboð verður til til að uppfylla alla leið upp að hámarki. Forgangurinn verður stilltur á forgang fyrsta sviðsins sem mun kalla á framboð.
- Ef það er engin á lager, ekkert framboð og engin eftirspurn, línan í **Skipuleggja forgangssvið** rist þar sem **Frá magni** reiturinn er stilltur á *Núll* verður notað.
- Ef það er eftirspurn, en það er engin á-hönd birgðir eða væntanlegt framboð, línan í **Skipuleggja forgangssvið** rist þar sem **Frá magni** reiturinn er stilltur á *Núll eða minna* verður notað.
- Þegar bilið sem eftirspurnin er hluti af er metið mun stillingin á **Íhugaðu forgang eftirspurnar** valkosturinn mun samt hafa áhrif.

## <a name="differences-between-traditional-timeline-calculations-and-priority-based-planning"></a>Munur á hefðbundnum tímalínuútreikningum og forgangsmiðaðri áætlanagerð

Forgangsmiðuð áætlanagerð er frábrugðin hefðbundnum tímalínuútreikningum á eftirfarandi hátt:

- Allir venjulegir forskipulagningarvinnslur eru enn í gildi. Þessir forvinnsluaðilar fela í sér tengingu samþykktra fyrirhugaðra pantana við sölueftirspurn, kortlagningu innkaupabeiðni og pöntunarrökfræði. Aðeins er unnið úr eftirspurn sem ekki er uppfyllt af þessum forvinnslum.
- Við tengingu er tekið tillit til allt framboðs, óháð forgangi þess. Þetta framboð inniheldur birgðahald á lager, losað framboð og ótengda hluta samþykktra fyrirhugaðra pantana.
- Enga „neikvæða daga“ eftirspurn er hægt að tengja við framboð á öllum umfjöllunartímanum.
- Þegar framboð er tengt við eftirspurn er framboðið sem hefur mestan forgang (þ.e. lægsta forgangsgildið) notað fyrst. Framboð er talið hafa forgangsgildi 0 (núll). Þess vegna verður það neytt sem fyrsta uppspretta.
- Nýjar fyrirhugaðar framboðslínur verða búnar til samkvæmt venjulegum reglum um lágmarkspöntunarstærð, hámarkspöntunarstærð, magnmargfalda og svo framvegis.

## <a name="planning-priority-models"></a>Forgangslíkön fyrir áætlanagerð

*Skipulags forgangslíkön* er úthlutað til umfjöllunarhópa og stjórna skipulagsforgangi fyrir áætlaðar pantanir. Þeir skilgreina rökfræðina sem ákvarðar hvernig áætlunarforgangsgildi er reiknað út fyrir hverja áætlaða pöntun og hvernig forgangi er úthlutað á áætlaðar pantanir, framboðslínur og eftirspurnarlínur.

Til að vinna með forgangslíkön áætlanagerðar skaltu fara á **Aðalskipulag \> Uppsetning \> Skipulags forgangslíkön**. Eins og áður hefur verið fjallað um er ein mikilvægasta stilling líkans **Forgangsreikningsaðferð** gildi. Þessi stilling stjórnar útreikningsaðferðinni sem er notuð þegar aðaláætlanagerð úthlutar forgangsgildi á áætlaðar pantanir.

> [!NOTE]
> Forgangslíkön áætlanagerðar gilda um allt skipulag, fyrir alla lögaðila.

### <a name="coverage-group"></a>Þekjuflokkur

Settu upp nýjan umfjöllunarhóp sem þú ætlar að nota fyrir forgangsmiðaða áætlanagerð, eins og lýst er í [Skilgreina umfangsreglur fyrir hluti](../tasks/define-coverage-rules-items.md). Eftir að þú hefur búið til umfjöllunarhópinn skaltu stilla eftirfarandi viðbótarreiti:

- **Umfjöllunarkóði** – Veldu *Forgangur* ef umfjöllunarhópurinn mun nota forgangsmiðaða áætlanagerð.
- **Skipulagsforgangslíkan** – Veldu hvaða forgangslíkan sem er fyrir alla skipulagningu.

### <a name="item-coverage"></a>Vöruþekja

Settu upp stillingar fyrir vöruþekju eins og lýst er í [Þekjustillingar](../coverage-settings.md). Sjálfgefið er **Umfjöllunarkóði** gildi sem er valið fyrir þekjuhópinn er afritað í vöruþekjustillingar. Hins vegar geturðu hnekkt sjálfgefna gildinu eftir þörfum. Í sumum tilfellum er **Umfjöllunarkóði** reit fyrir vöruþekjuskrá er stillt á *Skipulag*, en ekkert áætlunarforgangslíkan er skilgreint fyrir tengda þekjuhópinn. Í þessum tilvikum, hvaða líkan sem er þar sem **Forgangsreikningsaðferð** reiturinn er stilltur á *Hlutfall af hámarks birgðamagni* og **Fyrirhuguð pöntunargerð** reiturinn er stilltur á *Eitt framboð með mikilvægasta forgang* verður beitt sjálfgefið.

Stilltu **Umfjöllunarkóði** sviði til *Forgangur* að gera **Endurraða punkt** reitinn í tiltækum vöruþekjustillingum. Í þessum reit skal slá inn endurpöntunarpunktamagnið sem kerfið á að nota á meðan það er að ákvarða hvenær á að leggja inn fyrirhugaðar pantanir sem hafa **Umfjöllunarkóði** verðmæti á *Forgangur*.

Magn endurpöntunarpunkta er oft reiknað út sem eftirspurn á afgreiðslutíma auk lágmarksgildis (öryggisbirgða). Það verður að vera gildi á milli **Lágmark** og **Hámark** gildi.

Til dæmis gætirðu stillt reitina á eftirfarandi hátt:

- **Lágmark:** *10*
- **Endurraða punktur:** *45*
- **Hámark:** *60*

Fyrir þetta dæmi er magn endurpöntunarpunkta byggt á sjö daga afgreiðslutíma og 5 að meðaltali daglega notkun. Þess vegna er eftirspurnin á afgreiðslutíma 35. Lágmarksgildið 10 (öryggisbirgðir) er síðan bætt við til að fá endurpöntunarpunkt upp á 45. Þegar þessi uppsetning er notuð verður stungið upp á framboði þegar áætluð áreiti er undir 45. Pöntunarforgangurinn mun byggjast á uppsetningu skipulagsforgangs.

### <a name="manage-planning-priority-models"></a>Stjórna áætlanagerð forgangslíkön

Til að vinna með forgangslíkönin þín áætlanagerð. Fylgdu þessum skrefum.

1. Fara til **Aðalskipulag \> Uppsetning \> Skipulags forgangslíkön**.
1. Veldu annað hvort fyrirliggjandi líkan í listaglugganum eða veldu **Nýtt** á aðgerðarrúðunni til að búa til nýtt líkan.
1. Í haus færslunnar skal stilla eftirfarandi reiti:

    - **Nafn** – Sláðu inn heiti fyrir líkanið. Nafnið verður að vera einstakt fyrir alla lögaðila í fyrirtækinu þínu.
    - **Lýsing** – Sláðu inn lýsingu á líkaninu.
    - **Forgangsreikningsaðferð** – Veldu eitt af eftirfarandi gildum:

        - *Forgangssvið* – Þegar þú velur þetta gildi mun **Skipuleggja forgangssvið** rist verður tiltækt. Þar verður þú að setja upp nokkur forgangssvið til að skilgreina áætlunarforgangsgildi.
        - *Prósenta af hámarks birgðamagni* – Reiknaðu áætlunarforgangsgildi sem prósentu, byggt á áætluðu birgðastigi yfir hámarks birgðamagn.

    - **Fyrirhuguð pöntunargerð** – Þessi reitur er tiltækur þegar **Forgangsreikningsaðferð** reiturinn er stilltur á *Forgangssvið*. Veljið eitt af eftirfarandi gildum:

        - *Eitt framboð með mikilvægasta forgang* – Ekki skipta skipulögðum pöntunum út frá forgangssviðinu. Skipulagsforgangur fyrir áætlaða pöntun er byggður á mikilvægasta forgangssviðinu (þ.e. lægsta áætlunarforgangsgildi).
        - *Skiptu í samræmi við forgangssvið* – Skiptu eftirspurninni í margar skipulagðar pantanir, byggt á forgangssviðum áætlanagerðar. Skipulagsforgangur fyrir einstakar áætlaðar pantanir er skilgreindur af áætlunarforgangi tengda áætlunarforgangssviðsins.

    - **Íhugaðu forgang eftirspurnar** – Stilltu þennan valkost á *Já* að takmarka forgang nýrrar fyrirhugaðrar pöntunar sem er búin til fyrir framboð. (Forgangurinn verður ekki lægri en forgangur tengdrar eftirspurnar.) Ef þú stillir þennan valkost á *Nei*, forgangur eftirspurnarpöntunarinnar verður ekki tekinn til greina þegar forgangur framboðspöntunarinnar er reiknaður.

1. Ef þú stillir **Forgangsútreikningsaðferð** sviði til *Forgangssvið*, nota **Bæta við** og **Fjarlægja** hnappar á tækjastikunni á **Skipuleggja forgangssvið** Flýtiflipa til að bæta við eða fjarlægja forgangssviðslínur eftir þörfum. Ef margar línur eru til, og þú setur inn nýja línu, verður áætlunarforgangur sjálfkrafa stilltur á meðaltal völdu línunnar og línunnar fyrir ofan hana. Fyrir hverja línu skal stilla eftirfarandi reiti:

    - **Skipulagsforgangur** – Sláðu inn hvaða gildi sem er á milli 0,00 og 100,00. Þetta gildi táknar áætlunarforganginn sem er notaður fyrir línuna. Lægsta forgangsgildið táknar hæsta forganginn. Sjálfgefnu gildi er úthlutað en þú getur breytt því eftir þörfum. Það sama **Skipulagsforgangur** gildi er ekki hægt að nota fyrir fleiri en eitt áætlunarforgangssvið í sama áætlunarforgangslíkani.
    - **Lýsing** – Sláðu inn lýsingu á forgangssviði áætlanagerðar (svo sem *Endurraðaðu punkt í hámark*).
    - **Frá magni** – Neðri mörk forgangssviðs skipulags. Þetta gildi er skrifvarið og er byggt á **Að magni** og **Hlutfall af til magns** gildi fyrir fyrra forgangssvið áætlanagerðar.
    - **Að magni** – Veldu reitinn úr vöruþekju sem ætti að nota til að skilgreina efri mörk sviðsins. Eftirfarandi gildi eru studd og munu hafa áhrif á **Frá magni** gildi næsta bils:

        - *Núll* – Þetta gildi táknar neikvætt til núllsvið (*Núll eða minna* til *Núll*). Fyrir línur þar sem þetta gildi er valið er **Prósenta af til magns** reiturinn er skrifvarinn og er alltaf stilltur á *100* prósent.
        - *Lágmarks birgðamagn* – Þetta gildi táknar **Lágmark** gildi fyrir hlut á **Vöruumfjöllun** síðu. Fyrir línur þar sem þetta gildi er valið er **Prósenta af til magns** reiturinn er breytanlegur og er notaður til að stilla **Frá magni** gildi næsta bils (til dæmis til *80% af Lágmarks birgðamagni*).
        - *Endurraða punkt* – Þetta gildi táknar **Endurraða punkt** gildi fyrir hlut á **Vöruumfjöllun** síðu. Fyrir línur þar sem þetta gildi er valið er **Prósenta af til magns** reiturinn er breytanlegur og er notaður til að stilla **Frá magni** gildi fyrir næsta svið (til dæmis til *80% af endurpöntunarpunkti*).
        - *Hámarks birgðamagn* – Þetta gildi táknar **Hámark** gildi fyrir hlut á **Vöruumfjöllun** síðu. Fyrir línur þar sem þetta gildi er valið er **Prósenta af til magns** reiturinn er breytanlegur og er notaður til að stilla **Frá magni** af næsta bili (til dæmis til *80% af Lágmarks birgðamagni*).
        - *Óendanlegt* – Þetta gildi táknar óendanlega efri stig á bilinu (*Óendanlegt eða minna* til *Óendanlegt*). Fyrir línur þar sem þetta gildi er valið er **Prósenta af til magns** reiturinn er skrifvarinn og er alltaf stilltur á *100* prósent.

    - **Prósenta af til magns** – Sláðu inn prósentugildi sem er notað til að reikna út efri mörk áætlunarforgangssviðsins, byggt á gildinu sem er valið í **Að magni** sviði. Til dæmis, ef **Að magni** reiturinn er stilltur á *Lágmarks birgðamagn*, og **Prósenta af til magns** reiturinn er stilltur á *50*, verða efri mörkin 50 prósent af lágmarks birgðamagni frá tengdum vöruþekju.

1. Á **Vanskil áætlanagerðarforgangs** Flýtiflipi, stilltu reitina eins og þú þarft til að skilgreina sjálfgefna áætlunarforgangsröðun fyrir hverja tegund framboðs- eða eftirspurnarlínu (sölupöntun, innkaupapöntun, millifærslupöntun eða eftirspurnarspá). Aðeins er hægt að slá inn jákvæð gildi.

## <a name="view-and-maintain-planning-priority"></a>Skoða og viðhalda forgangi áætlanagerðar

Skipulagsforgangur er sýndur og settur í **Skipulagsforgangur** sviði. Þú getur fundið þennan reit á síðunum sem eru taldar upp í eftirfarandi töflu. Forgangurinn er stilltur sem tala á milli 0 (núll) og 100, þar sem 0 táknar mesta mikilvægi.

| Síða | Staðsetning vallarins | Gildisuppspretta |
|---|---|---|
| Eftirspurnarspárlínur | <p>**Atriði** flipa</p><p>(Veldu línu í efri hlutanum og veldu síðan **Atriði** flipa.)</p> | Sjálfgefið gildi eða gildi sem er stillt handvirkt |
| Upplýsingar um sölupöntun | <p>**Afhending** flipann á **Upplýsingar um línu** Hraðflipi</p><p>(Veldu línu á **Sölupöntunarlínur** flýtiflipann og síðan á **Upplýsingar um línu** flýtiflipann, veldu **Afhending** flipa.)</p> | Sjálfgefið gildi, gildi frá millifyrirtækja eða gildi sem er stillt handvirkt |
| Upplýsingar um innkaupapöntun | <p>**Afhending** flipann á **Upplýsingar um línu** Hraðflipi</p><p>(Veldu línu á **Innkaupapöntunarlínur** flýtiflipann og síðan á **Upplýsingar um línu** flýtiflipann, veldu **Afhending** flipa.)</p> | Gildi sem er stillt við staðfestingu frá fyrirhuguðum pöntunum, gildi frá millifyrirtækja eða gildi sem er stillt handvirkt |
| Flytja pöntunarupplýsingar | <p>**Afhending** flipann á **Upplýsingar um línu** Hraðflipi</p><p>(Veldu línu á **Flytja pöntunarlínur** flýtiflipann og síðan á **Upplýsingar um línu** flýtiflipann, veldu **Afhending** flipa.)</p> | Gildi sem er stillt við staðfestingu úr áætluðum pöntunum eða gildi sem er stillt handvirkt |
| Upplýsingar tillögu | **Almennt** Hraðflipi | Gildi sem er reiknað við aðalskipulagningu eða gildi sem er stillt handvirkt |

### <a name="intercompany-trade"></a>Samstæðuviðskipti

The **Skipulagsforgangur** verðmæti á framboðs- og eftirspurnarlínum milli fyrirtækja er deilt á milli tengdra aðila. Breytingar á hvorri hlið munu endurspeglast á tengdu pöntunarlínunni.

Hér eru nokkur dæmi:

- Notandi breytir áætlunarforgangi fyrir samstæðusölupöntunarlínu úr 20 í 30. Þessi breyting endurspeglast á tengdri innkaupapöntunarlínu milli fyrirtækja.
- Notandi breytir áætlunarforgangi fyrir innkaupapöntunarlínu innan samstæðu úr 40 í 50. Þessi breyting endurspeglast á tengdri sölupöntunarlínu milli fyrirtækja.
