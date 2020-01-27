---
title: Flokkun tiltektarlínu
description: Þetta efnisatriði veitir yfirlit yfir flokkun tiltektarlínu.
author: Mirzaab
manager: AnnBe
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2019-12-31
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1b1d0135d450bc9be7b1303240a9ca70f95ae38e
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906269"
---
# <a name="pick-line-grouping"></a>Flokkun tiltektarlínu

[!include [banner](../includes/banner.md)]

Við flokkun tiltektarlínu er hægt að sameina margar vinnulínur sem hafa sama hlut og staðsetningu í staka tínslu sem er kynnt notandanum í fartæki. Þess vegna geta starfsmenn vörugeymslu fengið skilvirkustu fyrirmælin sem mögulegt er, en nauðsynlegum aðskilnaði vinnulína í kerfinu er einnig haldið (til dæmis fyrir mismunandi gáma og pantanir).

## <a name="set-up-pick-line-grouping"></a>Setja upp flokkun tiltektarlínu

### <a name="create-a-mobile-device-menu-item"></a>Stofna valmyndaratriði fartækis

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækja** og búðu til nýtt valmyndaratriði sem heitir **Línutiltekt söluhópa - Stýrt af notanda**.
2. Undir **Valmyndaratriði fyrirtækis** stillirðu eftirfarandi gildi:

    - Í reitinn **Heiti valmyndaratriðis** slærðu inn **Sölutiltekt - Flokkalína**.
    - Í reitinn **Titill** slærðu inn **Sölutiltekt - Flokkalína**.
    - Í reitnum **Stilling** velurðu **Vinna**.
    - Stilltu valkostinn **Nota fyrirliggjandi vinnu** á **Já**.

3. Á flýtiflipanum **Almennt** geturðu stillt eftirfarandi gildi:

    - Í reitnum **Stýrt af** velurðu **Stýrt af notanda**.
    - Stilltu valkostinn **Mynda númeraplötu** á **Já**.
    - Stilltu valkostinn **Flokkatiltekt** á **Já**.

4. Á flýtiflipanum **Vinnuklasar** skaltu fylgja þessum skrefum til að stilla gilda vinnuflokka fyrir valmyndaratriðið í fartækinu:

    1. Veljið **Nýtt**.
    2. Í reitnum **Auðkenni vinnuklasa** velurðu **Sala** eða **Tiltekt sölupöntunar**, eftir því vöruhúsi sem þú ætlar að nota.
    3. Í reitnum **Gerð verkbeiðni** velurðu **Sölupantanir**.

### <a name="set-up-a-mobile-device-menu"></a>Setja upp valmynd fartækja

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmynd fartækis**. 
1. Bættu valmyndaratriðinu sem þú bjóst til við valmyndina.

### <a name="set-up-a-work-template"></a>Setja upp vinnusniðmát

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.
1. Finndu vinnusniðmátið sem ætti að nota með þessari aðgerð. Fyrir þetta dæmi skaltu velja staðalinn **51 tiltekt á stig** Contoso-vinnusniðmát.
1. Í valmyndinni velurðu **Breyta fyrirspurn**.
1. Á flipanum **Röðun** velurðu **Bæta við** og stillir síðan eftirfarandi gildi:

    - Í reitnum **Tafla** velurðu **Tímabundnar vinnufærslur**.
    - Í reitnum **Afleidd tafla** velurðu **Tímabundnar vinnufærslur**.
    - Í reitinn **Reitur** velurðu **Vörunúmer**.
    - Í reitnum **Leitarstefna** velurðu **Hækkandi**.

> [!NOTE]
> Til að flokkunarvirkni tiltektarlínu virki verður að flokka vinnulínurnar eftir auðkenni hlutar. Ef línum sem eru með sömu hlutina er ekki skipt í röð hver á eftir annarri verða þær ekki flokkaðar.

## <a name="example"></a>Dæmi

### <a name="create-picking-work"></a>Stofna tiltektarvinnu

Áður en þú getur sett upp flokkun tiltektarlína verður þú að búa til einhverja hæfa vinnu á útleið.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
2. Smellið á **Nýtt** til að stofna nýja sölupöntun. 
3. Í reitnum **Viðskiptavinalykill** velurðu einhvern viðskiptavin. 
4. Á flýtiflipanum **Almennt**, í reitnum **Vöruhús**, er valið **51**. Veljið síðan **Í lagi**.
5. Undir **Sölupöntunarlínur** skaltu bæta við eftirfarandi sex línum:

    - **Lína 1:** Í reitnum **Vörunúmer** velurðu **M9200**. Í **Magn** reitinn er fært inn **3**.
    - **Lína 2:** Í reitnum **Vörunúmer** velurðu **M9201**. Í **Magn** reitinn er fært inn **3**. 
    - **Lína 3:** Í reitnum **Vörunúmer** velurðu **M9202**. Í **Magn** reitinn er fært inn **2**. 
    - **Lína 4:** Í reitnum **Vörunúmer** velurðu **M9200**. Í **Magn** reitinn er fært inn **1**. 
    - **Lína 5:** Í reitnum **Vörunúmer** velurðu **M9200**. Í **Magn** reitinn er fært inn **3**.
    - **Lína 6:** Í reitnum **Vörunúmer** velurðu **M9202**. Í **Magn** reitinn er fært inn **7**. 

    Hér er yfirlit yfir heildarmagn fyrir hverja vöru:

    - **Vara M9200:** 7 stykki
    - **Vara M9201:** 3 stykki
    - **Vara M9202:** 9 stykki

6. Áður en þú losar pantanir í vöruhúsið verður þú að ganga úr skugga um að tiltektarstaðirnir séu með nægar birgðir fyrir allar vörur í öllum pöntunum. Farðu yfir stillinguna **Staðsetningartilskipun** til að ákvarða hvaða tínslustaðir eru notaðir við tínslu sölupöntunum.
7. Bókaðu birgðirnar og slepptu þeim í vöruhúsið. Vinnukenni sem hefur sex línur er búið til. Línunum er raðað eftir vörunúmeri.

### <a name="run-the-mobile-device-flow"></a>Keyrðu fartækjaflæðið

1. Í fartækinu velurðu valmynd sem inniheldur nýtt valmyndaratriði fartækis.
1. Veldu valmyndaratriðið **Sölutiltekt - Flokkalína** og hefðu tiltektina.

    Eftir að þú hefur valið valmyndina og slegið inn vinnukenið sérðu tiltektarskrefið þar sem allar tiltektarlínur fyrir vöruna M9200 eru flokkaðar. Þú færð leiðbeiningar um að velja 7 stykki af vöru M9200.

1. Staðfestu tiltektarskrefið. 
1. Farðu á biðlaraskjáinn í vinnunni sem er í gangi og taktu eftir því að öllum þremur tiltektarlínum fyrir vöruna M9200 var lokað samtímis.

    Vinnulína 4 er kynnt.

1. Staðfestu tiltektarskrefið.

    Síðasta tiltektarstigið í fartækinu safnar saman síðustu tveimur tiltektarlínunum úr vinnupöntuninni.

1. Ljúktu við tiltektarskrefið fyrir 9 stykki af vöru M9202.
1. Staðfestu frágangsskrefið og öll viðbótartiltektar-/frágangspör til að klára vinnuna.

> [!NOTE]
> - Aðeins er hægt að flokka vinnu línur ef þær eru í röð.
> - Eftirfarandi aðgerðir eru ekki studdar:
>
>    - Vörur framleiðsluþyngdar. Ef það eru einhverjar framleiðsluþyngdir í vvinnunni færðu villuboð áður en þú byrjar tiltekt.
>    - Einingatiltekt.
>    - Vinnulínur sem hafa óunna endurnýjunarvinnu.
>    - Umframtiltekt.
