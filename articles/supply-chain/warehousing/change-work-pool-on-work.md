---
title: Breyta vinnuhópi á vinnu
description: Þetta efnisatriði útskýrir hvernig hægt er að nota hnappinn „Breyta vinnuhópi“ fyrir vinnuliði til að breyta vinnuhópi fyrirliggjandi vinnu.
author: mirzaab
manager: tfehr
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPool,WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: global
ms.author: mirzaab
ms.search.validFrom: 2020-07-16
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 66d110c3235e8a87b64bf160bdad8524fad6abe5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001150"
---
# <a name="change-work-pool-on-work"></a>Breyta vinnuhópi á vinnu

[!include [banner](../includes/banner.md)]

Hægt er að nota vinnuhópa til að skipuleggja vinnu í flokka. Til dæmis er hægt að stofna vinnuhóp til að flokka vinnu sem fer í staðsetningu tiltekins vöruhúss.

Eiginleikinn *Breyta vinnuhópi á vinnu* bætir hnappnum **Breyta vinnuhópi** við aðgerðasvæðið fyrir vinnuliði. Stjórnendur vöruhúss geta þar af leiðandi auðveldlega breytt vinnuhópi fyrirliggjandi vinnu. Þessi eiginleiki gerir stjórnendum kleift að bregðast hratt við breytingum í vinnusal vöruhúss og hann eykur getu þeirra til að aðlagast breyttum aðstæðum og þörfinni til að flytja vinnu á annan vinnuhóp.

## <a name="turn-on-the-change-work-pool-on-work-feature"></a>Kveikja á eiginleikanum „Breyta vinnuhópi á vinnu“

Áður en hafist er handa við að setja upp eða nota þennan eiginleika þarf að ganga úr skugga um að hann sé í boði í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikt á honum ef þörf krefur. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Breyta vinnuhópi á vinnu*

## <a name="set-up-the-change-work-pool-on-work-feature"></a>Setja upp eiginleikann „Breyta vinnuhópi á vinnu“

Til að nota þennan eiginleika þarf að hafa einhverja vinnuhópa uppsetta. Einnig er hægt að setja upp vinnusniðmátin til að þau úthluti hópi sjálfkrafa. Ef á að vinna í gegnum sýniaðstæðurnar sem boðið er upp á seinna í þessu efnisatriði, skal setja kerfið eins og lýst er í þessum hluta.

### <a name="set-up-work-pools"></a>Setja upp vinnuhópa

Vinnuhópar gera þér kleift að skipuleggja vinnuliði eftir gerð. Til að vinna með eiginleikann *Breyta vinnuhópi á vinnu* þarf að hafa a.m.k. tvo vinnuhópa tiltæka. Til að skoða og bæta við vinnuhópum skal fylgja þessum skrefum.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnuhópar**.
1. Ef unnið er með sýnigögn úr fyrirtækinu **USMF** og farið verður í gegnum atburðarásina seinna í þessu efnisatriði, skal bæta við tveimur vinnuhópum sem eru með eftirfarandi stillingum:

    - Vinnuhópur 1:

        - **Auðkenni vinnuhóps:** *Vefverslun*
        - **Lýsing:** *Vefverslun*

    - Vinnuhópur 2:

        - **Auðkenni vinnuhóps:** *Símaver*
        - **Lýsing:** *Símaver*

1. Í aðgerðarúðunni skal velja **Vista**.

### <a name="set-up-work-templates"></a>Setja upp vinnusniðmát

Fyrir hvert vinnusniðmát er hægt að stilla sjálfgefinn vinnuhóp eftir þörfum. Fyrir hvert viðeigandi sniðmát er vinnuhópi úthlutað í dálknum **Auðkenni vinnuhóps**. Í þessu tilviki erfa sjálfkrafa allir vinnuliðir sem búnir eru til með því að nota uppgefið sniðmát úthlutaðan vinnuhóp. Ef unnið er með sýnigögn úr fyrirtækinu **USMF** og farið verður í gegnum atburðarásina seinna í þessu efnisatriði, skal fylgja þessum skrefum.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.
1. Á aðgerðasvæðinu skal velja **Breyta** til að færa síðuna yfir í breytingastillingu.
1. Breytið sniðmátinu með því að stilla eftirfarandi gildi:

    - **Vinnusniðmát:** *62 Tína til að pakka*
    - **Auðkenni vinnuhóps:** *Vefverslun*

1. Veljið **Vista**.

## <a name="example-scenario"></a>Dæmi

Þessi atburðarás sýnir hvernig á að breyta flæði úrvinnslunnar fyrir fyrirliggjandi vinnulið með því að breyta vinnuhóp hans. Hún notar sýnigögn úr fyrirtækinu **USMF** og stillingarnar sem mælt var með fyrr í þessu efnisatriði.

### <a name="create-a-sales-order-and-release-it-to-the-warehouse"></a>Stofna sölupöntun og losa hana í vöruhúsið.

1. Staðfestið að nóg af lagerbirgðum séu til fyrir vörur *A0001* og *A0002* í vöruhúsi *62*. Farið í **Vöruhúsakerfi \> Fyrirspurnir og skýrslur \> Listi á lager** og breytið síunum eins og sýnt er hér:

    - Gildið **Vöruhús** byrjar á *62*.
    - Gildið **Vörunúmer** er annaðhvort *A001* eða *A002*.

    Sýnigögn eiga hvort um sig að vera með magn upp á 10.

    Næst þarftu að stofna sölupöntun.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - **Viðskiptavinalykill:** *US-007*
    - **Vöruhús:** *62*

1. Veljið **Í lagi** til að stofna sölupöntunina og loka svarglugganum.
1. Ný sölupöntun opnast. Hún ætti að innihalda nýja, auða línu í hnitanetinu í flýtiflipanum **Sölupöntunarlínur**. Stilltu eftirfarandi gildi á þessari línu:

    - **Vörunúmer:** *A0001*
    - **Magn:** *2*

1. Á valmyndinni **Birgðir** fyrir ofan hnitanetið smellir þú á **Frátekning**.
1. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá birgðir.
1. Lokið síðunni.
1. Í sölupöntuninni sem var nýverið stofnuð, í flýtiflipanum **Sölupöntunarlínur**, skal velja **Bæta við línu** til að bæta annarri línu við sölupöntunina. Stilltu eftirfarandi gildi á þessari línu:

    - **Vörunúmer:** *A0002*
    - **Magn:** *2*

1. Á valmyndinni **Birgðir** fyrir ofan hnitanetið smellir þú á **Frátekning**.
1. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá birgðir.
1. Lokið síðunni.
1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.
1. Þú færð skilaboð með upplýsingum um bylgjuauðkenni og sendingarkenni sem voru búin til frá útgáfunni. Skráðu niður bylgjuauðkennið.

### <a name="review-the-outbound-wave"></a>Fara yfir bylgju á útleið

1. Farðu í **Vöruhúsastjórnun \> Bylgjur á útleið \> Sendingarbylgjur \> Allar bylgjur**.
1. Í hnitanetinu skaltu velja bylgjuauðkennið sem var búið til úr losuninni á sölupöntuninni.
1. Veljið bylgjukennið til að skoða upplýsingarnar.
1. Í flýtiflipanum **Bylgjulínur** skal ganga úr skugga um að auðkenni sendingar sé sýnt fyrir sölupöntunina.

    > [!TIP]
    > Ef valkosturinn **Vinna úr bylgju við losun í vörugeymslu** er stilltur á *Nei* í uppsetningunni fyrir bylgjusniðmát sendingar, þarf að vinna handvirkt úr bylgjunni með því að velja **Vinna úr** í flipanum **Bylgja** á aðgerðasvæðinu til að búa til vinnu.

1. Gakktu úr skugga um að bylgjan hafi verið meðhöndluð. Þessi meðhöndlun býr til nauðsynlega vinnu.

### <a name="view-work-details-and-change-the-work-pool"></a>Skoða upplýsingar um vinnu og breyta vinnuhópnum

Hægt er að nota síðuna **Upplýsingar um vinnu** til að skoða vinnuna sem búin var til og til að stjórna vinnuhópnum.

1. Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnu**.
1. Veljið línuna fyrir vinnuna sem var verið að búa til. Dálkurinn **Pöntunarnúmer** sýnir sölupöntunarnúmerið.

    Reiturinn **Auðkenni vinnuhóps** verður stilltur á auðkenni vinnuhópsins sem settur var upp í vinnusniðmátinu.

    > [!TIP]
    > Ef reiturinn **Auðkenni vinnuhóps** sést ekki, skal bæta dálknum við hnitanetið og síðan endurhlaða síðunni.

1. Til að breyta vinnuhópnum sem tengist vinnukenni, á aðgerðasvæðinu, í flipanum **Vinna**, skal velja **Breyta auðkenni vinnuhóps**.
1. Í svarglugganum **Breyta vinnuhópi**, í flýtiflipanum **Færibreytur**, í reitnum **Auðkenni vinnuhóps**, skal velja *Símaver*.
1. Veldu **Í lagi** til að gera breytinguna.
1. Takið eftir að gildið í reitnum **Auðkenni vinnuhóps** hefur nú verið breytt í *Símaver*.

> [!IMPORTANT]
> Þegar svarglugginn **Breyta vinnuhópi** birtist, gæti reiturinn **Auðkenni vinnuhóps** verið sjálfgefið auður. Ef reiturinn er auður þegar valið er **Í lagi** til að koma breytingum á, verður vinnuhópurinn fjarlægður að fullu úr vinnunni.
>
> Ásamt því að skipta um vinnuhópa, er hægt að nota þetta ferli til að bæta vinnuhópi við hvaða vinnulið sem er sem er ekki með slíkan, eða til að fjarlægja vinnuhóp úr vinnulið sem er með einn slíkan.
