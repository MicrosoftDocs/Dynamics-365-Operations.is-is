---
title: Flokkun bylgjusniðmáts
description: Flokkun bylgjusniðmáts gerir kerfinu kleift að nota uppsetningar bylgjusniðmáts til að ákvarða, byggt á skilyrðum sem skilgreind eru, hvernig skipta á losaðar línur og úthluta þeim á nýjar eða fyrirliggjandi bylgjur. Þessi eiginleiki getur verið gagnlegur í vöruhúsum þar sem bylgjur eru stofnaðar út frá tilteknum skilyrðum, en þar sem stjórnendur kjósa að stofna bylgjur sjálfkrafa í stað þess að gera það handvirkt.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWaveTableListPage, WHSWaveTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 5eb18ce29cbd1434b2a766c2ba5d78ed1be4e72b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851247"
---
# <a name="wave-template-grouping"></a>Flokkun bylgjusniðmáts

[!include [banner](../includes/banner.md)]

Flokkun bylgjusniðmáts gerir kerfinu kleift að nota uppsetningar [bylgjusniðmáts](tasks/configure-wave-processing.md) til að ákvarða, byggt á skilyrðum sem skilgreind eru, hvernig skipta á losaðar línur og úthluta þeim á nýjar eða fyrirliggjandi bylgjur. Þessi eiginleiki getur verið gagnlegur í vöruhúsum þar sem bylgjur eru stofnaðar út frá tilteknum skilyrðum, en þar sem stjórnendur kjósa að stofna bylgjur sjálfkrafa í stað þess að gera það handvirkt. Hann gerir kerfunum kleift að bæta sérhverri nýlega losaðri sendingu við fyrstu bylgjuna sem það finnur sem er með samsvarandi reitargildi flokkunar. Ef engin samsvörun finnst stofnar kerfið nýja bylgju fyrir nýju sendinguna.

> [!IMPORTANT]
> Flokkun bylgjusniðmáts er ekki studd fyrir vinnugerðirnar *hráefnistiltekt framleiðslu* eða *Kanban-tiltekt*. Þetta er vegna þess að bylgjuflokkun er byggð á sendingum og þessar vinnugerðir nota ekki sendingar.

## <a name="turn-on-the-wave-template-grouping-feature"></a>Kveikja á eiginleika bylgjusniðmátsflokkunar

Áður en hægt er að nota eiginleikann *Flokkun bylgjusniðmáts* verður að vera kveikt á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Flokkun bylgjusniðmáts*

## <a name="set-a-wave-template-to-use-wave-template-grouping"></a><a name="set-up-template"></a>Stilla bylgjusniðmát til að nota flokkun bylgjusniðmáts

Til að gera bylgjusniðmátsflokkun tiltæka skal fylgja þessum skrefum til að setja upp [bylgjusniðmát](tasks/configure-wave-processing.md).

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.
1. Vinstra megin á svæðinu skal velja bylgjusniðmátið sem á að setja upp. Ef þú ert að undirbúa að vinna í gegnum atburðarásina síðar í þessari grein með því að nota kynningargögn skaltu velja **62 Sendingar sjálfgefið** sniðmát.
1. Veldu **Breyta** til að setja síðuna í breytingastillingu.
1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Gera stofnun bylgju sjálfvirka:** *Já*
    - **Úthluta á opnar bylgjur:** *Já*
    - **Vinna úr bylgju við losun í vörugeymslu:** *Nei*

1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn** til að opna fyrirspurnargluggann.
1. Í fyrirspurnarglugganum, í flipanum **Röðun**, skal fara yfir skilyrði röðunar og ganga úr skugga um að til sé regla sem tekur með reitinn sem ætlunin er að nota til að flokka bylgjurnar.

    Ef verið er að undirbúa vinnu í gegnum atburðarásina með því að nota sýnigögn, skal bæta við línu sem er með eftirfarandi gildum:

    - **Tafla:** *Sendingar*
    - **Afleidd tafla:** *Sendingar*
    - **Reitur:** *Flutningsþjónusta*

        > [!NOTE]
        > Þegar þetta gildi er valið gætu komið upp eftirfarandi skilaboð: „Reiturinn Flutningsþjónusta er ekki vísisreitur. Á að bæta við röðun á þetta?“ Veljið **Já** til að bæta við röðun.

    - **Leitarstefna:** *Hækkandi*

1. Veljið **Í lagi** til að vista breytingarnar og loka fyrirspurnarglugganum.
1. Á aðgerðasvæðinu skal velja **Flokkun bylgjusniðmáts**.
1. Á síðunni **Flokkun bylgjusniðmáts** skal velja gátreitinn **Flokka eftir** fyrir hverja línu sem nota á til að flokka pöntunarlínurnar í bylgjur, eftir þörfum. Ef verið er að undirbúa vinnu í gegnum aðstæðurnar með því að nota sýnigögn skal velja gátreitinn **Flokka eftir** fyrir línuna *Flutningsþjónusta*.
1. Veljið **Vista**.
1. Lokið síðunni **Flokkun bylgjusniðmáts**.
1. Veljið **Vista** til að vista sniðmátið.

## <a name="scenario"></a>Aðstæður

Þessi hluti býður upp á forskrift sem hægt er að vinna með til að fá upplýsingar um hvað þessi eiginleiki gerir og hvernig á að vinna með hann.

### <a name="make-sample-data-available"></a>Gera sýnigögn tiltæk

Til að vinna í gegnum þessar aðstæður með því að nota sýnigögnin og gildin sem eru tilgreind hér verður þú að vera á kerfi þar sem venjuleg [sýnigögn](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

Einnig er hægt að nota þessar aðstæður sem leiðsögn um notkun á eiginleikanum þegar unnið er í framleiðslukerfi. Í slíku tilfelli þarf hinsvegar að skipta út eigin gildum og einhverjar nauðsynlegar færslugerðir gæti vantað sem stöðluðu sýnigögnin bjóða upp á.

### <a name="scenario-wave-template-grouping"></a>Aðstæður: Flokkun bylgjusniðmáts

Þessar aðstæður sýna hvernig nota má flokkun bylgjusniðmáts til að stofna sjálfkrafa margar bylgjur, byggðar á flokkunarskilyrðum sem eru skilgreind í bylgjusniðmáti. Í þessum aðstæðum er bylgjusniðmátið sett upp í kerfinu til að búa til eina bylgju á flutningsþjónustu.

Áður en þú byrjar skaltu undirbúa bylgjusniðmátið eins og lýst er í [Stilltu bylgjusniðmát til að nota bylgjusniðmátflokkun](#set-up-template) kafla fyrr í þessari grein. Ef unnið verður með sýnigögn fyrir þetta dæmi skal gæta þess að nota gildi sýnigagnanna sem stungið er upp á í því ferli. Þessi uppsetning mun flokka bylgjurnar samkvæmt flutningsþjónustunni sem er stillt fyrir hverja sölupöntun.

#### <a name="create-sales-order-1"></a>Stofna sölupöntun 1

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Smellið á **Nýtt** til að stofna nýja sölupöntun.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - Í flipanum **Viðskiptavinur** skaltu stilla reitinn **Reikningur viðskiptavinar** á *US-004*.
    - Í flýtiflipanum **Almennt** skal stilla reitinn **Vöruhús** á *62*.

1. Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum **Stofna sölupöntun**.
1. Nýja sölupöntunin er opnuð í **Línur**. Skráið hjá ykkur sölupöntunarnúmerið.
1. Skiptið yfir í **Hausa** yfirlitið.
1. Í flýtiflipanum **Afhending**, í hlutanum **Flutningur**, skal stilla eftirfarandi gildi:

    - **Farmflytjandi:** *Flugfarmur*
    - **Flutningsþjónusta:** *flug*

1. Skiptið aftur yfir í yfirlitið **Línur**.
1. Í hlutanum **Sölupöntunarlínur** skal velja **Bæta við línu** til að bæta línu við hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Vörunúmer:** *A0002*
    - **Magn:** *2*

1. Veljið nýju pöntunarlínuna og síðan í valmyndinni **Birgðir** fyrir ofan hnitanetið skal smella á **Frátekning**.
1. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá heildarmagn valdrar línu í vöruhúsinu.
1. Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.
1. Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Aðgerðir**, velurðu **Losa í vöruhús**.
1. Þú færð upplýsingaboð sem sýna sendinguna og bylgjuna fyrir þessa pöntun. Skráið hjá ykkur bylgjukennið og sendingarkenni.

#### <a name="view-the-wave-that-was-created-from-sales-order-1"></a>Skoða bylgjuna sem var búin til úr sölupöntun 1

1. Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.
1. Veljið bylgjukennið sem stofnað var í sölupöntuninni.
1. Veljið tengil bylgjukennis til að opna upplýsingasíðu bylgjunnar.
1. Takið eftir að sendingunni hefur verið bætt við flýtiflipann **Bylgjulínur**.

#### <a name="create-sales-order-2"></a>Stofna sölupöntun 2

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Smellið á **Nýtt** til að stofna nýja sölupöntun.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - Í flipanum **Viðskiptavinur** skaltu stilla reitinn **Reikningur viðskiptavinar** á *US-005*.
    - Í flýtiflipanum **Almennt** skal stilla reitinn **Vöruhús** á *62*.

1. Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum **Stofna sölupöntun**.
1. Nýja sölupöntunin er opnuð í **Línur**. Skráið hjá ykkur sölupöntunarnúmerið.
1. Skiptið yfir í **Hausa** yfirlitið.
1. Í flýtiflipanum **Afhending**, í hlutanum **Flutningur**, skal stilla eftirfarandi gildi:

    - **Farmflytjandi:** *Blómaflytjandi*
    - **Flutningsþjónusta:** *Std*

1. Skiptið aftur yfir í yfirlitið **Línur**.
1. Í hlutanum **Sölupöntunarlínur** skal velja **Bæta við línu** til að bæta línu við hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Vörunúmer:** *A0001*
    - **Magn:** *1*

1. Veljið nýju pöntunarlínuna og síðan í valmyndinni **Birgðir** fyrir ofan hnitanetið skal smella á **Frátekning**.
1. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá heildarmagn valdrar línu í vöruhúsinu.
1. Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.
1. Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Aðgerðir**, velurðu **Losa í vöruhús**.
1. Þú færð upplýsingaboð sem sýna sendinguna og bylgjuna fyrir þessa pöntun. Skráið hjá ykkur bylgjukennið og sendingarkenni. Takið eftir því að bylgjukennið er ólíkt bylgjukenni fyrstu sölupöntunarinnar.

#### <a name="view-the-wave-that-was-created-from-sales-order-2"></a>Skoða bylgjuna sem var búin til úr sölupöntun 2

1. Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.
1. Veljið bylgjukennið sem stofnað var í sölupöntun tvö.
1. Veljið tengil bylgjukennis til að opna upplýsingasíðu bylgjunnar.
1. Takið eftir að sendingunni hefur verið bætt við flýtiflipann **Bylgjulínur**.

Ný bylgja var stofnuð fyrir þessa sendingu vegna þess að hún notar aðra flutningsþjónustu en fyrsta sölupöntunin.

#### <a name="create-sales-order-3"></a>Stofna sölupöntun 3

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Smellið á **Nýtt** til að stofna nýja sölupöntun.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - Í flipanum **Viðskiptavinur** skaltu stilla reitinn **Reikningur viðskiptavinar** á *US-006*.
    - Í flýtiflipanum **Almennt** skal stilla reitinn **Vöruhús** á *62*.

1. Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum **Stofna sölupöntun**.
1. Nýja sölupöntunin er opnuð í **Línur**. Skráið hjá ykkur sölupöntunarnúmerið.
1. Skiptið yfir í **Hausa** yfirlitið.
1. Í flýtiflipanum **Afhending**, í hlutanum **Flutningur**, skal stilla eftirfarandi gildi:

    - **Farmflytjandi:** *Flugfarmur*
    - **Flutningsþjónusta:** *flug*

1. Skiptið aftur yfir í yfirlitið **Línur**.
1. Í hlutanum **Sölupöntunarlínur** skal velja **Bæta við línu** til að bæta línu við hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Vörunúmer:** *A0001*
    - **Magn:** *1*

1. Veljið nýju pöntunarlínuna og síðan í valmyndinni **Birgðir** fyrir ofan hnitanetið skal smella á **Frátekning**.
1. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá heildarmagn valdrar línu í vöruhúsinu.
1. Lokið síðunni **Frátekning** til að fara aftur í sölupöntunina.
1. Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Aðgerðir**, velurðu **Losa í vöruhús**.
1. Þú færð upplýsingaboð sem sýna sendinguna og bylgjuna fyrir þessa pöntun. Skráið hjá ykkur bylgjukennið og sendingarkenni. Sendingunni hefur verið úthlutað á fyrirliggjandi bylgju úr fyrstu sölupöntuninni.

#### <a name="view-the-wave-for-sales-orders-1-and-3"></a>Skoða bylgjuna fyrir sölupantanir 1 og 3

1. Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.
1. Veljið bylgjukennið sem stofnað var í þriðju sölupöntuninni.
1. Veljið tengil bylgjukennis til að opna upplýsingasíðu bylgjunnar.
1. Takið eftir að sendingunni hefur verið bætt við flýtiflipann **Bylgjulínur**, ásamt sendingunni fyrir fyrstu sölupöntunina.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]