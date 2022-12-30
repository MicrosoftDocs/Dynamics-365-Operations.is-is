---
title: Birgðafærsluupplýsingar
description: Í þessari grein er að finna yfirlit yfir upplýsingasíðu Færslur sem sýnir upplýsingar um valda birgðafærslu.
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
ms.openlocfilehash: 55e29d5804f57cd86fb5ddac5d6c5576b7ea5f61
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859388"
---
# <a name="inventory-transaction-details"></a>Birgðafærsluupplýsingar

Notaðu síðuna **Færsluupplýsingar** til að skoða upplýsingar um allar valdar birgðafærslur.

## <a name="open-the-transaction-details-page"></a>Opnaðu síðuna Færsluupplýsingar

Til að opna síðuna **Færsluupplýsingar** skaltu fylgja þessum skrefum.

1. Farið í **Birgðastjórnun \> Fyrirspurnir og skýrslur \> Færslur**.
1. Veldu færslurnar sem á að skoða.
1. Veldu **Færsluupplýsingar** á aðgerðasvæðinu.

## <a name="fasttabs-overview"></a>Yfirlit flýtiflipa

Síðunni **Upplýsingar um færslur** er skipt niður í nokkra flýtiflipa. Eftirfarandi tafla lýsir tilgangi hvers flýtiflipa.

| Flýtiflipi | Lýsing |
|---|---|
| Almennt | Þessi flýtiflipi sýnir grunnupplýsingar um valda birgðafærslu. Auk reitanna sem birtast á síðunni **Birgðafærslur** inniheldur hann viðbótarreitina sem lýst er síðar í þessari grein. |
| Uppfærslur | Þessi flýtiflipi sýnir upplýsingar sem tengjast efnislegum, fjárhagslegum, jöfnunar þáttum valinnar birgðafærslu. Sumir reitir gætu verið auðir en það fer eftir núverandi stöðu færslunnar. Þeir reitir verða þó sjálfkrafa stilltir þegar færslur eru bókaðar. Auk reitanna sem birtast á síðunni **Birgðafærslur** inniheldur þessi flýtiflipi viðbótarreitina sem lýst er síðar í þessari grein. |
| Fjárhagsbókanir | Þessi flýtiflipi sýnir bókunargerð og fjárhagslykil sem eru notuð fyrir efnuslega uppfærslu, fjárhagslega uppfærslu, efnislegar tekjur, efnisleg gjöld, fjárhagslegar tekjur og fjárhagsleg gjöld sem eru tengd valinni birgðafærslu. |
| Tilvísanir | Þessi flýtiflipi sýnir viðbótarupplýsingar um upprunafærsluna sem bjó til valda birgðafærslu. Til dæmis gætu þessar upplýsingar innihaldið upplýsingar úr innkaupapöntuninni eða sölupöntuninni. |
| Tengdar upplýsingar | Þessi flýtiflipi sýnir viðbótarupplýsingar um valda birgðafærslu. Þessir reitir gætu ekki verið stilltir ef þú ert ekki að nota suma eiginleika, til dæmis innkaupaflokka eða verkefni. |
| Fjárhagsvíddir - efnislegt | Þessi flýtiflipi sýnir fjárhagsvíddargildin sem voru notuð þegar efnislega uppfærslan var bókuð. Reitirnir eru auðir ef ekki er búið að birta efnislega uppfærslu. |
| Fjárhagsvíddir - fjárhagslegt | Þessi flýtiflipi sýnir fjárhagsvíddargildin sem voru notuð þegar fjárhagslega uppfærslan var bókuð. Reitirnir eru auðir ef fjárhagsuppfærslan hefur ekki verið bókuð. |
| Birgðavíddir | Þessi flýtiflipi sýnir birgðavíddargildin sem er úthlutað á valda birgðafærslu. Þessi gildi eru m.a. svæðið, vöruhúsið, stærð, litur, stilling, staðsetning, rununúmer, raðnúmer, birgðastaða, númeraplata og eigandi. |

## <a name="fields-on-the-general-fasttab"></a>Reitir á flýtiflipanum Almennt

Eftirfarandi tafla lýsir reitunum á flýtiflipanum **Almennt** sem birtast ekki einnig á síðunni **Birgðafærslur**.

| Svæði | Lýsing |
|---|---|
| Aðili | Heiti viðkomandi aðila fyrir valda birgðafærslu. Í innkaupapöntunarfærslu kemur til dæmis fram nafn lánardrottins á innkaupapöntuninni og í sölupöntunarfærslu kemur fram nafn viðskiptavinarins. Þessi reitur er ekki í boði fyrir allar gerðir af birgðafærslum. |
| Birgðatilvísun | Ef önnur birgðafærsla tengist valinni birgðafærslu skal tilgreina tegund hinnar færslunnar. Ef innkaupapöntun er til dæmis merkt gegn sölupöntun verður reiturinn **Birgðatilvísun** í innkaupapöntunarfærslunni stilltur á *Sölupöntun*. Merking fer sjálfkrafa fram fyrir beinar afhendingarpantanir og pantanir innan samstæðu. Þegar merking er notuð með öðrum kostnaðaraðferðum en *staðalkostnaði* g *hlaupandi meðaltali* mun kerfið búa til jafnanir og leiðréttingar á nákvæmum færslum sem eru merktar. Þannig getur þú náð „raunverulegum“ kostnaði sem hnekkir rök fyrir fyrsta inn, fyrsta út (FIFO), síðasta inn, fyrsta út (LIFO), eða vegið meðaltal. |
| Birgðanúmer | Sérstaka færslan sem tengist völdu birgðafærslunni. Ef innkaupapöntun er til dæmis merkt gegn sölupöntun verður reiturinn **Birgðanúmer** í innkaupapöntunarfærslunni stilltur á sölupöntunarnúmerið. |
| Verkkenni | Ef valin birgðafærsla er tengd verki er þessi reitur stilltur á númer verkefnis. |
| Lotukenni | Einkvæmu lotukennin sem kerfið hefur úthlutað valda birgðafærslunni. |
| Tilvísunarlota | Ef önnur birgðafærsla tengist völdu birgðafærslunni er runukenni hinnar færslunnar. Ef innkaupapöntun er til dæmis merkt gegn sölupöntun verður reiturinn **Tilvísunarruna** í innkaupapöntunarfærslunni stilltur á gildið **Runukenni** í sölupöntunarlínu birgðafærslunnar. |
| Víddarnúmer | Einkvæmt auðkenni sem táknar samsetningu allra birgðarvídda sem eru tengd við valda birgðafærslu. |
| Opið gildi | Gildi sem tilgreinir hvort valin birgðafærsla hafi verið jöfnuð með birgðalokunarferlinu. Ef þessi reitur er stilltur á *Já* hefur færslan ekki verið jöfnuð. |
| Væntanleg dagsetning | Fyrir innhreyfingarfærslur, dagsetninguna þegar búist er við því að innhreyfing birgða komi fram. Til dæmis gæti þessi reitur sýnt væntanlega móttökudagsetningu á pöntun birgðalæsingar eða afhendingardag á innkaupapöntunarlínu. |
| Birgðadagsetning | Þessi reitur er stilltur þegar skráningarfærsla var gerð á innhreyfingarpöntun áður en efnisleg innhreyfing var birt. |
| Ófjárhagslegur flutningur | Gildi sem gefur til kynna hvort valin birgðafærsla sé ekki fjárhagsleg færsla. Færsla sem er ekki fjárhagsleg á sér stað þegar ekki er hægt að rekja fjárhagslega breytingar á birgðavíddum á síðunni **Vörulíkanaflokkur**. |
| Flytja lotukenni | Ef valin birgðafærsla er ekki fjárhagsleg færsla er þessi reitur stilltur á **llotukenni** hinnar birgðafærslunnar sem valin færsla er gerð upp á móti. |

## <a name="fields-on-the-updates-fasttab"></a>Reitir á flýtiflipanum Uppfærslur

Eftirfarandi tafla lýsir reitunum á flýtiflipanum **Uppfærslur** sem birtast ekki einnig á síðunni **Birgðarfærslur**.

| Svæði | Lýsing |
|---|---|
| Efnislegt fylgiskjal | Reikningsnúmerið úr fjárhag þar sem efnisleg bókun fyrir valda birgðafærslu var búin til. |
| Leið | Leiðin sem er tengd við valda birgðafærslu. Þessi reitur er aðeins stilltur fyrir færslur tiltektarlista framleiðslu þar sem uppskriftin (BOM) eða formúlulínan er tengd tiltekinni vöru. |
| Fylgiseðill | Fylgiseðilsnúmer sem var fært inn vegna innhreyfingarfærslu innkaupapöntunar. |
| Efnisleg kostnaðarupphæð | Upphæðin sem var bókuð í fjárhaginn fyrir efnislegu uppfærsluna. Þessi upphæð er staðalkostnaður fyrir staðlaða kostnaðarvöru. Fyrir aðrar kostnaðaraðferðir táknar það vegið meðaltal vörunnar við bókun. |
| Efnistekjur | Upphæð frestaðar tekjur sem var bókuð í fjárhaginn fyrir efnislegu uppfærsluna. |
| Hleðsluauðkenni | Ef núverandi færsla tengist farmi í flutningsstjórnun, sýnir þessi reitur einkvæmt númer farmsins sem innihélt vöruna. |
| Efnislega bókað | Gildi sem gefur til kynna hvort valin birgðafærsla hafi verið efnislega bókuð. Ef núverandi færsla er bókuð í fjárhag verður einnig um að ræða efnislegan afsláttarmiða. |
| Fjárhagslega bókað | Gildi sem tilgreinir hvort valin birgðafærsla hafi verið bókuð fjárhagslega. Ef núverandi færsla er bókuð í fjárhag, verður einnig um að ræða afsláttarmiða. |
| Efnislegt gjald bókað | Gildi sem segir til um hvort efnisleg gjöld sem eru tengd valinni birgðafærslu hafi verið bókuð. |
| Fjárhagsgjald bókað | Gildi sem segir til um hvort fjárhagsleg gjöld sem eru tengd valinni birgðafærslu hafi verið bókuð. |
| Fjárhagsfylgiskjal | Númer fylgiskjals í fjárhagnum þar sem fjárhagsbókunin var búin til. |
| Reikningur | Reikningsnúmerið sem var búið til, til dæmis fyrir innkaupapöntun eða sölupöntun. |
| Leiðrétting | Upphæðin sem var leiðrétt í völdu birgðafærslunni úr birgðalokunar- og leiðréttingarferlinu. |
| Rekstur, bókuð upphæð | Upphæð valdrar birgðafærslu sem var bókuð á rekstraryfirlit. |
| Óbókaður reikningur | Reikningsnúmer tengdrar innkaupapöntunar sem birtist á síðunni **Reikningur frá lánardrottni í bið**. |
| Fjárhagslega lokað | Dagsetningin þegar færslan var fyllilega jöfnuð. |
| Afgreitt magn framleiðsluþyngdar | Magn framleiðsluþyngdar sem uppgjörið nær til. |
| Jafnað magn | Magnið sem hefur verið jafnað fyrir valda birgðafærslu. |
| Jöfnuð upphæð | Gildið sem hefur verið jafnað fyrir valda birgðafærslu. |
