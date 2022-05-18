---
title: Upplýsingar um birgðafærslur
description: Þetta efnisatriði veitir yfirlit yfir síðu Færsluupplýsingar sem sýnir upplýsingar um valda birgðafærslu.
author: rachel-profitt
ms.date: 04/25/2022
ms.topic: article
ms.search.form: InventTrans, InventTransDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2022-04-25
ms.dyn365.ops.version: 10.0.27
ms.openlocfilehash: fd1416f21ce15dc832dd41ea4110c93bf5bb41a2
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735878"
---
# <a name="inventory-transaction-details"></a>Upplýsingar um birgðafærslur

Nota **Upplýsingar um viðskipti** síðu til að skoða upplýsingar um valin birgðafærslu.

## <a name="open-the-transaction-details-page"></a>Opnaðu síðuna Færsluupplýsingar

Til að opna **Upplýsingar um viðskipti** síðu, fylgdu þessum skrefum.

1. Fara til **Vörustjórnun \> Fyrirspurnir og skýrslur \> Viðskipti**.
1. Veldu færsluna sem þú vilt skoða.
1. Á aðgerðarrúðunni velurðu **Upplýsingar um viðskipti**.

## <a name="fasttabs-overview"></a>Yfirlit yfir flýtiflipana

The **Upplýsingar um viðskipti** síðunni er skipt í nokkra flýtiflipa. Eftirfarandi tafla lýsir tilgangi hvers flýtiflipa.

| Flýtiflipi | Lýsing |
|---|---|
| Almennt | Þessi flýtiflipi sýnir grunnupplýsingar um valda birgðafærslu. Til viðbótar við reitina sem birtast á **Birgðaviðskipti** síðu, inniheldur það viðbótarreitina sem lýst er síðar í þessu efni. |
| Uppsetningar eiginleika | Þessi flýtiflipi sýnir upplýsingar sem tengjast efnislegum, fjárhagslegum og uppgjörsþáttum valinnar birgðafærslu. Það fer eftir núverandi stöðu færslunnar, sumir reitir gætu verið auðir. Hins vegar verða þeir reitir sjálfkrafa stilltir þegar færslur eru bókaðar. Til viðbótar við reitina sem birtast á **Birgðaviðskipti** síðu, inniheldur þessi flýtiflipi viðbótarreitin sem lýst er síðar í þessu efni. |
| Fjárhagsbókanir | Þessi flýtiflipi sýnir bókunartegund og fjárhagsreikning sem eru notaðir fyrir efnislega uppfærslu, fjárhagsuppfærslu, efnistekjur, efnisgjöld, fjárhagstekjur og fjárhagsgjöld sem tengjast völdum birgðafærslu. |
| Tilvísanir | Þessi flýtiflipi sýnir viðbótarupplýsingar um upprunafærsluna sem bjó til valda birgðafærslu. Til dæmis gætu þessar upplýsingar innihaldið upplýsingar úr innkaupapöntun eða sölupöntun. |
| Tengdar upplýsingar | Þessi flýtiflipi sýnir viðbótarupplýsingar um valda birgðafærslu. Þessir reitir gætu ekki verið stilltir ef þú ert ekki að nota suma eiginleika, eins og innkaupaflokka eða verkefni. |
| Fjárhagsvíddir - líkamlegar | Þessi flýtiflipi sýnir fjárhagsvíddargildin sem voru notuð þegar líkamlega uppfærslan var birt. Ef líkamleg uppfærsla hefur ekki verið birt verða reitirnir auðir. |
| Fjárhagsvíddir – fjárhagslegar | Þessi flýtiflipi sýnir fjárhagsvíddargildin sem voru notuð þegar fjárhagsuppfærslan var bókuð. Ef fjárhagsuppfærslan hefur ekki verið birt verða reitirnir auðir. |
| Birgðavíddir | Þessi flýtiflipi sýnir birgðavíddargildin sem eru úthlutað á valda birgðafærslu. Þessi gildi innihalda vefsvæði, vöruhús, stærð, lit, uppsetningu, staðsetningu, lotunúmer, raðnúmer, birgðastöðu, númeraplötu og eiganda. |

## <a name="fields-on-the-general-fasttab"></a>Reitir á Almennt flýtiflipanum

Eftirfarandi tafla lýsir reitunum á **Almennt** Flýtiflipi sem birtist ekki líka á **Birgðaviðskipti** síðu.

| Reitur | Lýsing |
|---|---|
| Aðili | Nafn viðkomandi aðila fyrir valda birgðafærslu. Til dæmis sýnir innkaupapöntunarfærsla nafn lánardrottins á innkaupapöntuninni og sölupöntunarfærsla sýnir nafn viðskiptavinar. Þessi reitur er ekki tiltækur fyrir allar tegundir birgðafærslur. |
| Birgðatilvísun | Ef önnur birgðafærsla er tengd völdum birgðafærslu, gerð þessarar annarrar færslu. Til dæmis, ef innkaupapöntun er merkt við sölupöntun, er **Birgðatilvísun** reit innkaupapöntunarfærslunnar verður stilltur á *Sölupöntun*. Merking á sér stað sjálfkrafa fyrir pantanir fyrir beinar afhendingar og millipantanir. Þegar þú notar merkingu með öðrum kostnaðaraðferðum en *staðalkostnaður* og *hlaupandi meðaltal*, mun kerfið búa til uppgjör og leiðréttingar á nákvæmlega þeim færslum sem eru merktar. Þannig er hægt að ná fram „raunverulegum“ kostnaði sem hnekkir rökfræðinni fyrir fyrstur inn, fyrst út (FIFO); síðastur inn, fyrst út (LIFO); eða vegið meðaltal. |
| Birgðanúmer | Tiltekna færslan sem er tengd völdum birgðafærslu. Til dæmis, ef innkaupapöntun er merkt við sölupöntun, er **Birgðanúmer** reitinn í innkaupapöntunarfærslunni verður stilltur á sölupöntunarnúmerið. |
| Verkkenni | Ef valin birgðafærsla er tengd verki er þessi reitur stilltur á verknúmerið. |
| Lotukenni | Einkvæma lotuauðkenni sem kerfið hefur úthlutað valinni birgðafærslu. |
| Tilvísunarlota | Ef önnur birgðafærsla er tengd völdum birgðafærslu, lotuauðkenni þeirrar annarrar færslu. Til dæmis, ef innkaupapöntun er merkt við sölupöntun, er **Viðmiðunarlóð** reitur innkaupapöntunarfærslunnar verður **Lot ID** gildi birgðafærslu sölupöntunarlínunnar. |
| Víddarnúmer | Einstakt auðkenni sem táknar samsetningu allra birgðavíddargilda sem eru úthlutað til valda birgðafærslu. |
| Opið gildi | Gildi sem gefur til kynna hvort valin birgðafærsla hafi verið jöfnuð með birgðalokunarferlinu. Ef þessi reitur er stilltur á *Já*, viðskiptin hafa ekki verið gerð upp. |
| Væntanleg dagsetning | Fyrir innhreyfingarfærslur, dagsetningin þegar búist er við að birgðamóttaka eigi sér stað. Til dæmis gæti þessi reitur sýnt væntanlega móttökudagsetningu á birgðalokunarpöntun eða afhendingardagsetningu á innkaupapöntunarlínu. |
| Birgðadagsetning | Þessi reitur er stilltur þegar skráningarfærsla var gerð á móttökupöntuninni áður en efnisleg kvittun var bókuð. |
| Ófjárhagslegur flutningur | Gildi sem gefur til kynna hvort valin birgðafærsla sé ófjárhagsleg millifærsla. Ófjárhagsleg millifærsla á sér stað þegar breyting á birgðavíddum er ekki rakin fjárhagslega á **Vörulíkanahópur** síðu. |
| Flytja lotukenni | Ef valin birgðafærsla er ófjárhagsleg millifærsla er þessi reitur stilltur á **Lot ID** verðmæti hinnar birgðafærslunnar sem valin færsla er gerð upp á móti. |

## <a name="fields-on-the-updates-fasttab"></a>Reitir á flýtiflipanum Uppfærslur

Eftirfarandi tafla lýsir reitunum á **Uppfærslur** Flýtiflipi sem birtist ekki líka á **Birgðaviðskipti** síðu.

| Reitur | Lýsing |
|---|---|
| Efnislegt fylgiskjal | Skírteinisnúmerið úr fjárhag þar sem efnisleg bókun fyrir valda birgðafærslu var mynduð. |
| Leið | Leiðin sem er tengd völdum birgðafærslu. Þessi reitur er aðeins stilltur fyrir framleiðslutínslulistafærslur þar sem efnisskrá (BOM) eða formúlulína tengist tiltekinni vöru. |
| Fylgiseðill | Fylgiseðilsnúmerið sem var slegið inn fyrir innkaupapöntun vörukvittunarfærslu. |
| Efnisleg kostnaðarupphæð | Upphæðin sem var bókuð í fjárhag fyrir líkamlega uppfærslu. Fyrir staðlaða kostnaðarvöru táknar þessi upphæð staðalkostnaðinn. Fyrir aðrar kostnaðaraðferðir táknar það vegið meðaltal vörunnar við færslu. |
| Efnistekjur | Upphæð frestaðra tekna sem var bókuð í fjárhag fyrir líkamlega uppfærslu. |
| Hleðsluauðkenni | Ef núverandi færsla er tengd hleðslu í Flutningsstjórnun sýnir þessi reitur einkvæmt númer farmsins sem innihélt vöruna. |
| Efnislega bókað | Gildi sem gefur til kynna hvort valin birgðafærsla hafi verið bókuð líkamlega. Ef núverandi færsla er bókuð í fjárhag, verður einnig efnislegt fylgiskjal. |
| Fjárhagslega bókað | Gildi sem gefur til kynna hvort valin birgðafærsla hafi verið fjárhagslega bókuð. Ef núverandi færsla er bókuð í fjárhag mun einnig fylgja fjárhagsskírteini. |
| Efnislegt gjald bókað | Gildi sem gefur til kynna hvort efnisleg gjöld sem tengjast völdum birgðafærslu hafi verið bókuð. |
| Fjárhagsgjald bókað | Gildi sem gefur til kynna hvort fjármagnsgjöld sem tengjast völdum birgðafærslu hafi verið bókuð. |
| Fjárhagsfylgiskjal | Skírteinisnúmerið í aðalbókinni þar sem fjárhagsbókunin var mynduð. |
| Reikningur | Reikningsnúmerið sem var búið til, til dæmis fyrir innkaupapöntun eða sölupöntun. |
| Leiðrétting | Upphæðin sem var leiðrétt á valinni birgðafærslu úr birgðalokun og leiðréttingarferli. |
| Rekstur, bókuð upphæð | Upphæð valinnar birgðafærslu sem var bókuð á rekstrarreikning. |
| Óbókaður reikningur | Reikningsnúmer tengdrar innkaupapöntunar sem birtist á **Reikningur seljanda í bið** síðu. |
| Fjárhagslega lokað | Dagsetningin þegar viðskiptin voru að fullu gerð upp. |
| Afgreitt magn framleiðsluþyngdar | Aflaþyngdarmagn sem fellur undir uppgjörið. |
| Jafnað magn | Magnið sem hefur verið jafnað fyrir valda birgðafærslu. |
| Jöfnuð upphæð | Gildið sem hefur verið jafnað fyrir valda birgðafærslu. |
