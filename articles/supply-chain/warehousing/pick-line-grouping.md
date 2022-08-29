---
title: Flokkun tiltektarlínu
description: Þessi grein veitir yfirlit yfir flokkun vallínu.
author: Mirzaab
ms.date: 12/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFMenuItem,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 00a4e07ac38a83cd4569006f3b6e2bdd59ed1a42
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2022
ms.locfileid: "9334536"
---
# <a name="pick-line-grouping"></a>Flokkun tiltektarlínu

[!include [banner](../includes/banner.md)]

Flokkun tiltektarlínu gerir kleift að sameina margar vinnulínur sem eru með sömu vöru og staðsetningu í eina tiltekt sem birtist notanda í fartæki. Starfsmenn í vöruhúsi geta þar af leiðandi fengið gagnlegustu leiðbeiningarnar, en nauðsynlegur aðskilnaður vinnulínu (fyrir mismunandi umbúðir, pantanir og svo framvegis) er enn hægt að vinna með í kerfinu.

## <a name="turn-on-the-pick-line-grouping-feature"></a>Kveikja á eiginleika fyrir flokkun tiltektarlínu

Áður en þú getur notað þennan eiginleika verður að kveikja á honum fyrir kerfið þitt. Stjórnendur geta notað vinnusvæðið [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum ef þörf krefur. Þar er eiginleikinn sýndur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Flokkun tiltektarlínu*

## <a name="set-up-pick-line-grouping"></a>Setja upp flokkun tiltektarlínu

### <a name="create-a-mobile-device-menu-item"></a>Stofna valmyndaratriði fartækis

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Í reitinn **Heiti valmyndaratriðis** skal færa inn *Tiltekt söluflokkslínu*.
1. Í reitinn **Titill** skal slá inn *Tiltekt söluflokkslínu*. Þessi titill birtist í valmynd fartækis.
1. Í reitnum **Stilling** velurðu *Vinna*.
1. Stilltu valkostinn **Nota fyrirliggjandi vinnu** á *Já*.
1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - Í reitnum **Stýrt af** velurðu *Stýrt af notanda*.
    - Stilltu valkostinn **Mynda númeraplötu** á *Já*.
    - Stilltu valkostinn **Flokkatiltekt** á *Já*.
    - Samþykkið sjálfgefin gildi fyrir valkostina sem eftir eru.

1. Fylgið þessum skrefum til að skilgreina gilda vinnuklasa fyrir valmyndaratriði fartækis:

    1. Í flýtiflipanum **Vinnuklasar** skal velja **Nýr**.
    2. Í reitnum **Auðkenni vinnuklasa** er hægt að velja annaðhvort *Sala* eða *Tiltekt sölupöntunar*, en það fer eftir vöruhúsinu sem verður notað. Fyrir þessar aðstæður skal velja *Tiltekt sölupöntunar*.

        Reiturinn **Gerð verkbeiðni** er sjálfkrafa stilltur á *Sölupantanir*.

### <a name="set-up-a-mobile-device-menu"></a>Setja upp valmynd fartækja

Fylgið þessum skrefum til að bæta við valmyndaratriðinu sem var stofnað í valmyndinni **Á útleið**.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Listasvæðið sýnir allar fyrirliggjandi valmyndir fartækis. Veljið *Á útleið* í listanum.
1. Í listanum **Tiltækar valmyndir og valmyndaratriði** skal finna og velja valmyndaratriðið *Tiltekt söluflokkslínu* sem var stofnað.
1. Veljið hægri örvarhnappinn til að flytja valmyndaratriðið *Tiltekt söluflokkslínu* yfir í listann **Valmyndaskipan**.
1. Notið örvarhnappana upp og niður til að færa valmyndaratriðið á æskilegan stað í valmyndaskipanina.
1. Í aðgerðarúðunni skal velja **Vista**.

### <a name="set-up-a-work-template"></a>Setja upp vinnusniðmát

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.
1. Í reitnum **Gerð verkbeiðni** velurðu *Sölupantanir*.
1. Í hnitanetinu **Yfirlit** skal finna og velja vinnusniðmátið sem á að nota með þessari aðgerð. Fyrir þessar aðstæður skal velja sniðmátið *51 Tína fyrir geymslustað*.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.
1. Í svarglugga fyrirspurnarritils, í flipanum **Röðun**, skal velja **Bæta við** og síðan stilla eftirfarandi gildi fyrir nýju línuna:

    - Í dálkinum **Tafla** skal velja *Tímabundnar vinnufærslur*.
    - Í dálkinum **Afleidd tafla** skal velja *Tímabundnar vinnufærslur*.
    - Í dálkinum **Reitur** skal velja *Vörunúmer*.
    - Í dálkinum **Leitarstefna** skal velja *Hækkandi*.

1. Veljið **Í lagi** til að loka svarglugganum og vista breytingarnar.
1. Eftirfarandi skilaboð birtast: „Flokkun verður endurstillt, á að halda áfram?" Veldu **Já** til að halda áfram.

> [!IMPORTANT]
> Til að flokkunarvirkni tiltektarlínu virki verður að flokka vinnulínurnar eftir auðkenni hlutar. Ef línum sem eru með sömu hlutina er ekki skipt í röð hver á eftir annarri verða þær ekki flokkaðar.

## <a name="example"></a>Dæmi

### <a name="create-picking-work"></a>Stofna tiltektarvinnu

Áður en þú getur sett upp flokkun tiltektarlína verður þú að búa til einhverja hæfa vinnu á útleið.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Smellið á **Nýtt** til að stofna nýja sölupöntun.
1. Í reitnum **Viðskiptavinalykill** skal velja *US-004*.
1. Á flýtiflipanum **Almennt**, í reitnum **Vöruhús**, er valið *51*.
1. Veljið **Í lagi**.
1. Í flýtiflipanum **Sölupöntunarlínur** skal bæta við eftirfarandi sex línum:

    - **Lína 1:** Í reitnum **Vörunúmer** velurðu *M9200*. Í **Magn** reitinn er fært inn *3*.
    - **Lína 2:** Í reitnum **Vörunúmer** velurðu *M9201*. Í **Magn** reitinn er fært inn *3*.
    - **Lína 3:** Í reitnum **Vörunúmer** velurðu *M9202*. Í **Magn** reitinn er fært inn *2*.
    - **Lína 4:** Í reitnum **Vörunúmer** velurðu *M9200*. Í **Magn** reitinn er fært inn *1*.
    - **Lína 5:** Í reitnum **Vörunúmer** velurðu *M9200*. Í **Magn** reitinn er fært inn *3*.
    - **Lína 6:** Í reitnum **Vörunúmer** velurðu *M9202*. Í **Magn** reitinn er fært inn *7*.

    Hér er yfirlit yfir heildarmagn fyrir hverja vöru:

    - **Vara M9200:** *7* hver
    - **Vara M9201:** *3* hver
    - **Vara M9202:** *9* hver

1. Áður en þú losar pantanir í vöruhúsið verður þú að ganga úr skugga um að tiltektarstaðirnir séu með nægar birgðir fyrir allar vörur í öllum pöntunum. Farðu yfir stillinguna **Staðsetningartilskipun** til að ákvarða hvaða tínslustaðir eru notaðir við tínslu sölupöntunum. Ef verið er að nota umhverfi contoso-sýnigagna fyrir vöruhús *51* skal staðfesta að til séu lausar birgðir.

    Nú þarf að taka frá birgðirnar fyrir hverja línu.

1. Í flýtiflipanum **Sölupöntunarlínur** skal velja eina af línunum sem þarf að taka frá.
1. Á valmyndinni **Birgðir** fyrir ofan hnitanetið smellir þú á **Frátekning**.
1. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að nota frátekninguna. Því næst skal loka síðunni.
1. Endurtakið skref 8 til 10 fyrir eftirstandandi línur sem þarf að taka frá.

    Nú þarf að losa sölupöntunina í vöruhúsið.

1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.

    Skilaboð birtast sem segja að sending og bylgja hafi verið stofnuð og að bylgjan hafi verið send inn til að keyra í runu.

    Þegar bylgjunni og öllum seinni verkum er lokið er vinnunkenni stofnað fyrir vinnuna sem er með sex línur. Línunum er raðað eftir vörunúmeri.

1. Farið í **Vöruhúsakerfi \> Vinna \> Öll vinna** til að skoða vinnuna sem var stofnuð. Skráið hjá ykkur gildið fyrir **Vinnukennið** því það þarf að nota það í næsta skrefi.

### <a name="initiate-picking-from-the-mobile-device"></a>Tiltekt hafin í fartæki

1. Skráðu þig inn í fartækið sem notandi sem er settur upp fyrir í vöruhús *51*.
1. Í fartækinu velurðu valmynd sem inniheldur nýtt valmyndaratriði fartækis. Fyrir þessar aðstæður skal velja **Á útleið**.
1. Veljið valmyndaratriðið **Tiltekt söluflokkslínu** til að hefja tiltektina.
1. Færið inn gildið fyrir **Vinnukenni** sem skráð var niður í skrefinu hér á undan.

    Tiltektarskref ætti að sjást þar sem öllum tiltektarlínum fyrir vöru *M9200* er safnað saman og skipun um að tína *7* af vöru *M9200*.

    > [!IMPORTANT]
    > Í fartækinu hefur tiltektarvinnunni fyrir þessar þrjár tiltektarlínur verið safnað saman í eitt tiltektarskref fyrir notandann.

1. Staðfestu tiltektarskrefið.
1. Farið á vinnusíðu fyrir vinnunkennið og takið eftir að öllum þremur tiltektarlínunum fyrir vöru *M9200* var lokað samtímis.
1. Farið aftur í fartækið og haldið áfram með tiltektina. Vinnulína 4 fyrir vöru *M9201* ætti að koma upp. Þar sem aðeins ein vinnulína var í pöntuninni er ekkert til að safna saman.
1. Staðfestu tiltektarskrefið.
1. Síðasta tiltektarstigið í fartækinu safnar saman síðustu tveimur tiltektarlínunum úr vinnupöntuninni.
1. Ljúkið við tiltektarskrefið fyrir *9* af vöru *M9202*.
1. Staðfestu frágangsskrefið og öll viðbótartiltektar-/frágangspör til að klára vinnuna.

> [!IMPORTANT]
>
> - Aðeins er hægt að flokka vinnu línur ef þær eru í röð.
> - Eftirfarandi aðgerðir eru ekki studdar:
>
>   - Vörur með framleiðsluþyngd
>
>    Ef það eru einhverjar framleiðsluþyngdir í vvinnunni færðu villuboð áður en þú byrjar tiltekt.
>
>   - Stykkjatínsla
>   - Vinnulínur sem eru með óuppgerða áfyllingarvinnu
>   - Umframtiltekt
>   - Endurúthlutun með fyrir vöru


[!INCLUDE[footer-include](../../includes/footer-banner.md)]