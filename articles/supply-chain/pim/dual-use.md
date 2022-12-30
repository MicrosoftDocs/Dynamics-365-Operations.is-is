---
title: Vörur með tvíþætt notagildi
description: Þessi grein útskýrir hvernig á að halda utan um vörur sem eru auðkenndar sem vörur með tvíþætt notagildi, geyma vottorðanúmer fyrir hverja viðeigandi afurð og land áfangastaðar, og prenta gild vottorðanúmer á viðeigandi reikninga, fylgiseðla og/eða sölupantanir.
author: t-benebo
ms.date: 07/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: COODualUseCerts, COORules, COODualUseCountries
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-07-15
ms.dyn365.ops.version: 10.0.9
ms.openlocfilehash: 5147a837be91aab519c373e624acc036f9293641
ms.sourcegitcommit: 555de844b8ba02fe095c28a2d447fc7c441ae549
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/09/2022
ms.locfileid: "9460549"
---
# <a name="dual-use-goods"></a>Vörur tvíþætts notagildis

[!include [banner](../includes/banner.md)]

Vörur með tvíþætt notagildi eru yfirleitt vörur sem bæði óbreyttir borgarar og hermenn geta notað. Til dæmis gæti efni verið notað sem áburður eða sprengiefni. Mörg lönd eru með sérstakar reglugerðir sem gilda um útflutning, innflutning og flutninga á vörum með tvíþætt notagildi. Því er mikilvægt að fyrirtæki sem eru að taka þátt í alþjóðlegum viðskiptum á vörum með tvíþætt notagildi haldi utan um hinar ýmsu reglur og vottorð.

Eiginleiki tvíþætts notagildis auðveldar fyrirtækjum að halda utan um afurðir sem eru auðkenndar sem vörur með tvíþætt notagildi, geyma vottorðanúmer fyrir hverja viðeigandi afurð og land áfangastaðar, og prenta gild vottorðanúmer á viðeigandi reikninga, fylgiseðla og/eða sölupantanir. Það hjálpar til við að tryggja að þegar vörur eru sendar séu þær alltaf með uppfærðar vottanir.

Íhugið eftirfarandi aðstæður:

1. Síðan **Uppsetning lands fyrir tvíþætt notagildi** í kerfinu þínu sýnir að sendingar til Frakklands þurfa á vottorði að halda.
2. Síðan **Upplýsingasíða um losaðar afurðir** fyrir afurð X-100 sýnir að hún er vara með tvíþætt notagildi. Saman sýna kóðinn, tegundin, flokkurinn og fyrirkomulagið flokkun útflutningseftirlits sem afurðin tilheyrir.
3. Síðan **Vottorð fyrir tvíþætt notagildi** inniheldur vottor fyrir afurð X-100 þegar hún er send til Frakklands. Þetta vottorð rennur út 1. janúar 2020.
4. 17. júní 2020, stofnar þú sölupöntun fyrir fyrirtæki viðskiptavinar sem er staðsett í Frakklandi og pöntunin inniheldur afurð X-100.
5. Þegar sölupöntunin er staðfest ákvarðar kerfið eftirfarandi upplýsingar:

    1. Inniheldur pöntunin afurðir sem eru vörur með tvíþætt notagildi?
    2. Ef pöntunin inniheldur vörur með tvíþætt notagildi, þarf land áfangastaðar á vottorði tvíþætts notagildis að halda?
    3. Ef landið gerir kröfu um vottorð vegna tvíþætts notagildis, er til gilt vottorð fyrir hverja vöru með tvíþætt notagildi fyrir land áfangastaðar?

6. Pöntunin inniheldur afurð X-100, afurðin er send til Frakklands og franskt vottorð er til fyrir afurðina. Vottorðið er hins vegar útrunnið. Þar af leiðandi birtast eftirfarandi viðvörunarskilaboð: „Vottorð fyrir tvíþætt notagildi fyrir eina eða fleiri vörur með tvíþætt notagildi í þessari sölupöntun eru ógildar. Á að halda áfram með staðfestinguna?“

Þessi grein útskýrir hvernig á að skilgreina allar stillingar sem þarf til að setja upp vörur með tvíþætt notagildi og styðja þessa atburðarás.

## <a name="define-dual-use-requirements-for-each-relevant-country"></a>Skilgreina kröfur um tvíþætt notagildi fyrir hvert land sem á við

Mismunandi lönd eru með mismunandi kröfur fyrir vörur með tvíþætt notagildi. Síðan **Uppsetning lands fyrir tvíþætt notagildi** er notuð til að halda utan um löndin sem þurfa og þurfa ekki vottorð. Upplýsingarnar sem hér eru tilgreindar eru athugaðar þegar sölupantanir eru stofnaðar og minnt verður á að útvega nauðsynleg vottorð.

Til að setja upp upplýsingar um kröfur vegna tvíþætts notagildis fyrir mismunandi lönd, skal fylgja þessum skrefum.

1. Farið í **Afurðaupplýsingastjórnun \> Uppsetning \> Afurðarsamræmi \> Afurðir með tvíþættu notagildi \> Uppsetning lands fyrir tvíþætt notagildi**.
2. Veldu fyrirliggjandi uppsetningu lands til að breyta henni, eða **Ný** á aðgerðasvæðinu til að búa til nýja uppsetning lands.
3. Stilltu eftirfarandi gildi fyrir valda landið eða nýja uppsetningu á landi.

    | Svæði | lýsing |
    |---|---|
    | Land/svæði | Veldu landið sem þú ert að rekja þarfir fyrir. |
    | Vottorð áskilið | Veljið þennan gátreit fyrir lönd sem þurfa vottun fyrir vörur með tvíþætt notagildi. Hreinsið það fyrir lönd sem þurfa ekki þessa vottun. |

## <a name="create-dual-use-categories"></a>Stofna flokka tvíþætts notagildis

Oft þarf að flokka vörur með tvíþætt notagildi samkvæmt flokkunarnúmeri útflutningseftirlitsins (ECCN). ECCN er kóði í bók- eða tölustöfum sem flokkar vörur eftir þáttum á borð við vörutegund eða tækni. Síðan **Flokkar tvíþætts notagildis** auðveldar þér að búa til lista yfir flokkana sem eru notaðir til að greina frá tilgangi.

Til að setja upp flokka tvíþætts notagildis skal fylgja þessum skrefum.

1. Farið í **Afurðaupplýsingastjórnun \> Uppsetning \> Afurðarsamræmi \> Afurðir með tvíþættu notagildi \> Flokkar tvíþætts notagildis**.
2. Veljið fyrirliggjandi flokk til að breyta honum, eða veljið **Nýr** á aðgerðasvæðinu til að búa til nýjan flokk.
3. Stillið eftirfarandi gildi fyrir valdan eða nýjan flokk.

    | Svæði | lýsing |
    |---|---|
    | Kóði tvíþætts notagildis | Sláið inn fullan ECCN-kóða (til dæmis, *3A001*).|
    | Flokkur tvíþætts notagildis | Færið inn flokkshlutann af eftirlitslista söluvarnings (CCL) fyrir ECCN-kóðann. Til dæmis fyrir ECCN-kóðann *3A001* er þetta gildi *3*. |
    | Hópur tvíþætts notagildis | Færið inn hluta afurðaflokks fyrir ECCN-kóðann. Til dæmis, fyrir ECCN-kóðann *3A001*, er þetta gildi *A*. |
    | Fyrirkomulag tvíþætts notagildis | Sláið inn fyrirkomulagskóða vörunnar. Þessi kóði auðkennir ástæðuna fyrir því að varan er flokkuð sem vara með tvíþætt notagildi. Til dæmis, fyrir ECCN-kóðann *3A001*, er þetta gildi *001*. |

## <a name="apply-dual-use-categories-to-products"></a>Nota flokka tvíþætts notagildis á afurðir

Til að auðkenna afurð sem vara með tvíþætt notagildi og nota flokk tvíþætts notagildis, skal fylgja þessum skrefum.

1. Opna **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**.
1. Veljið eða stofnið afurð til að opna síðuna **Upplýsingar um losaðar afurðir**.
1. Í flýtiflipanum **Erlend viðskipti** skal stilla valkostinn **Afurðir með tvíþættu notagildi** á **Já** til að auðkenna núverandi afurð sem vöru með tvíþætt notagildi.
1. Stillið reitinn **Kóði tvíþætts notagildis** á kóðann sem gildir um núverandi afurð. (Þú skilgreindir þennan kóða á síðunni **Flokkar tvíþætts notagildis**.)

> [!NOTE]
>
> Kerfið gerir eftirfarandi athuganir á tvíþættri notkun þegar það býr til sölustaðfestingu:
>
> 1. Inniheldur pöntunin einhverjar tvíþættar vörur?
> 1. Þarf land áfangastaðar á vottorði með tvíþætt notagildi að halda?
> 1. Ef svo er, eru til vottorð fyrir hverja tvíþætta vöru fyrir ákvörðunarlandið, og gilda þau skírteini fyrir staðfestar endadagsetningar?
> 1. Ef svörin við spurningum 1 og 2 eru „Já“ og svarið við spurningu 3 er „Nei“, þá sýnir kerfið viðvörun til að láta notandann vita að það vanti tvíþætt vottorð fyrir eina eða fleiri tvíþættar vörur í sölupöntuninni. Notandinn ætti líklega að fá tilskilin vottorð og reyna aftur, en gæti þess í stað hunsað viðvörunina og haldið áfram með sölustaðfestinguna ef hann vill.

## <a name="set-up-dual-use-certificates"></a>Setja upp vottorð fyrir tvíþætt notagildi

Síðan **Vottorð fyrir tvíþætt notagildi** er notuð til að setja upp og stjórna nauðsynlegum vottorðum fyrir tvíþætt notagildi fyrir hverja afurð og land. Hægt er að rekja upplýsingar um hvert vottorð, svo sem land og gildistíma. Einnig er hægt að stilla valkosti til að tilgreina hvar eigi að prenta þessar upplýsingar. Til dæmis er hægt að prenta upplýsingarnar á reikninginn, fylgiseðilinn og/eða sölupöntunina. Þessi uppsetning er merkt þegar sölupöntun er stofnuð.

1. Farið í **Afurðaupplýsingastjórnun \> Uppsetning \> Afurðarsamræmi \> Afurðir með tvíþættu notagildi \> Vottorð fyrir tvíþætt notagildi**.
2. Veljið fyrirliggjandi vottorð til að breyta því, eða veljið **Nýtt** á aðgerðasvæðinu til að búa til nýtt vottorð.
3. Stilltu eftirfarandi gildi fyrir valda vottorðið eða nýtt vottorði.

    | Svæði | lýsing |
    |---|---|
    | Vörunúmer | Veljið vörunúmer fyrir vöru með tvíþætt notagildi sem þetta vottorð gildir um. |
    | Land/svæði | Viðtökuland eða svæði þar sem þú verður að nota þetta vottorð. |
    | Númer vottorðs | Númerið sem birtist á votorðinu sem er gefið út til lánardrottins eða viðskiptavinar. |
    | Virkt | Veljið fyrstu dagsetningu þegar núgildandi vottorð er gilt.|
    | Lok gildistíma | Veljið síðustu dagsetningu þegar núgildandi vottorð er gilt. |
    | Prenta á reikning | Veljið þennan gátreit til að prenta númer vottorðs á reikningunum sem eru stílaðir á tiltekið land innan tiltekins dagsetningabils. |
    | Prenta á fylgiseðil | Veljið þennan gátreit til að prenta númer vottorðs á fylgiseðlum sem eru stílaðir á tiltekið land innan tiltekins dagsetningabils. |
    | Prenta á sölupöntun | Veljið þennan gátreit til að prenta númer vottorðs á sölupöntunum sem eru stílaðar á tiltekið land innan tiltekins dagsetningabils. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
