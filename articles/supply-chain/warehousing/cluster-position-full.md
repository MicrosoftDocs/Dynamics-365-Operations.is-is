---
title: Staðsetning klasa er full
description: Þetta efnisatriði veitir upplýsingar um eiginleikann fyrir fulla staðsetningu klasa. Þessi eiginleiki býður upp á aðra leið í stað ósveigjanlegar framkvæmdar á reglum um vinnuskiptingu þegar klasatiltekt er notuð, því að leyfð skekkjumörk rúmmálsins eru víðari fyrir gáma eða farm.
author: Mirzaab
ms.date: 08/25/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSClusterProfile
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 459c8fce892d9437c7466458b7e53743c71da38f
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102828"
---
# <a name="cluster-position-full"></a>Staðsetning klasa er full

[!include [banner](../includes/banner.md)]

Eiginleikinn *Staðsetning klasa er full* býður upp á aðra leið í stað ósveigjanlegar framkvæmdar á reglum um vinnuskiptingu þegar klasatiltekt er notuð, því að leyfð skekkjumörk rúmmálsins eru víðari fyrir gáma eða farm. Í algengum aðstæðum passa ekki öll atriði í verkbeiðni í valinn gám. Starfsmenn vöruhúss sem sjá um klasatiltekt hafa nokkra valmöguleika í þessum aðstæðum: þeir verða annaðhvort að breyta yfir í stærri gám eða vinna með yfirmanninum sínum til að finna út betri lausn.

Þessi eiginleiki kynnir möguleikann á því að keyra hnappinn **Fullur** í einni vinnueiningunni í klasa. Í eldri útgáfum var þessi valkostur aðeins tiltækur fyrir reglubundna tiltekt á pöntun, ekki fyrir klasatiltekt. Þessi eiginleiki er hins vegar frábrugðinn hefðbundna hnappnum **Fullur** að því leyti að hann hættir við eftirstandandi vinnu. Hann stingur ekki upp á að notandinn bæti öðru hólfi við sama klasann og hann stofnar ekki sjálfkrafa nýja vinnu.

## <a name="turn-the-cluster-position-full-feature-on-or-off"></a>Kveiktu eða slökktu á Cluster position fullri eiginleikanum

Til að nota virknina sem lýst er í þessu efni, er *Klasastaða full* kveikt verður á eiginleikanum fyrir kerfið þitt. Frá og með Supply Chain Management 10.0.25 er þessi eiginleiki skylda og ekki hægt að slökkva á honum. Ef þú ert að keyra útgáfu eldri en 10.0.25 geta stjórnendur kveikt eða slökkt á þessari virkni með því að leita að *Klasastaða full* eiginleiki í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnurými.

## <a name="setup"></a>Uppsetning

Þessi hluti býður upp á leiðarvísi og dæmi sem sýnir hvernig á að setja upp og nota eiginleikann *Staðsetning klasa er full*.

### <a name="make-sample-data-available"></a>Gera sýnigögn tiltæk

Til að vinna í gegnum [sýniaðstæðurnar](#example-scenario) með því að nota sýnskrárnar og sýnigildin sem eru kynnt í þessu efnisatriði verður þú að vinna á kerfi þar sem venjulegu [sýnigögnin](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) eru sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

Einnig er hægt að nota þetta sýnidæmi sem leiðsögn ef unnið er með þennan eiginleika í framleiðslukerfi. Í því tilfelli verður hinsvegar að skipta út eigin gildum fyrir stillingarnar sem er lýst hér.

### <a name="cluster-profiles"></a>Klasanotandaupplýsingar

Tilgreina verður hvort klasaauðkenni eru sjálfkrafa mynduð, hversu margar stöður eru notaðar, hvenær klösum er skipt og hvernig tiltekt er raðað og staðfest.

1. Farðu á **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Klasaforstillingar**.
1. Í listasvæðinu skal velja færsluna **Stofna klasa**.
1. Í flýtiflipanum **Almennt** skal staðfesta eftirfarandi gildi:

    - **Mynda klasaauðkenni:** *Já*
    - **Virkja stöður:** *Já*
    - **Fjöldi staða:** *2*
    - **Heiti stöðu:** *Tölustafur*
    - **Skipta klasaeiningu við:** *Frágang*
    - **Gerð röðunarstaðfestingar:** *Skönnun stöðu*

1. Í flýtiflipanum **Klasaröðun**. Hnitanetið ætti að vera autt (það ætti ekki að innihalda neinar línur).

### <a name="work-templates"></a>Vinnusniðmát

Tilgreina verður hvernig tiltekt fyrir klasatiltekt er búin til.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.
1. Efst á síðunni skal stilla reitinn **Gerð verkbeiðni** á *Sölupantanir*.
1. Gangið úr skugga um að eftirfarandi vinnusniðmát úr sýnigögnunum séu skráð. Ef þau eru ekki tiltæk verður ekki hægt að ljúka atburðarásinni.

    - 61 Stig sölupöntunar
    - 61 Klasatiltekt sölupöntunar

### <a name="location-directives"></a>Staðsetningarleiðbeiningar

Tilgreina verður hvar vörur eru tíndar og hvar þær eru settar.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.
1. Efst í listanum skal stilla reitinn **Gerð verkbeiðni** á *Innkaupapantanir*.
1. Ganga skal úr skugga um að eftirfarandi leiðbeiningar sölupöntunar úr sýnigögnunum séu skráðar. Ef þau eru ekki tiltæk verður ekki hægt að ljúka atburðarásinni.

    - 61 Klasatiltekt
    - 61 Tiltektarröð sölupöntunar

### <a name="mobile-device-menu-items"></a>Valmyndaratriði fartækis

Þú verður að stilla valmynd fartækis til að nota fyrirliggjandi vertk sem er stjórnað af klasatínslu. Í valmyndaratriði fartækis fyrir klasatiltekt þarf að kveikja á færibreytunni **Leyfa skiptingu vinnu** og bæta verður við vinnuklasanum *Tiltekt sölupöntunar*.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Í listasvæðinu skal velja færsluna **Stofnun klasatiltektar**.
1. Veljið **Breyta** á aðgerðasvæðinu.
1. Stilltu eftirfarandi gildi á flýtiflipanum **Almennt**:

    - **Stjórnað af:** *Klasatiltekt*
    - **Mynda númeraplötu:** *Já*
    - **Leyfa skiptingu vinnu:** *Já*
    - **Prófílkenni klasa:** *Stofna klasa*

    Samþykktu sjálfgildin fyrir öll önnur svæði.

1. Í flýtiflipanum **Vinnuklasar** skal bæta við eftirfarandi tveimur línum eftir þörfum:

    - Lína 1 (oftast til staðar í sýnigögnum):

        - **Auðkenni vinnuklasa:***Sala* 
        - **Gerð verkpöntunar:** *Sölupantanir*

    - Lína 2 (líklega ekki til staðar í sýnigögnum):

        - **Auðkenni vinnuklasa:** *Tiltekt sölupöntunar*
        - **Gerð verkpöntunar:** *Sölupantanir*

1. Farið í **Uppsetning verkstaðfestingar** á aðgerðasvæðinu.
1. Veljið **Breyta**.
1. Sláið inn eftirfarandi gildi í línunni í hnitaneti.
    - **Verkgerð** - *Tiltekt*
    - **Staðfesting afurðar** - *Velja gátreitinn*

1. Veljið **Vista** í aðgerðarúðunni og lokið síðunni.

## <a name="create-picking-work"></a>Stofna tiltektarvinnu

Áður en hægt er að ræsa klasatiltekt þarf að stofna einhverja vinnu á útleið. Klasaforstillingin sem þú bjóst til áður tilgreinir tvær klasastöður. Þess vegna þarf að stofna að minnsta kosti tvö vinnukenni fyrir tiltekt sölupöntunar. Fyrir þessa atburðarás eiga færslur sér stað í vöruhúsi *61* og þær nota vörur *L0101* og *T0100*. Sýnigögnin ættu að vera með nægar birgðir á lager af þessum vörum. Gangið úr skugga um að nægilegar birgðir séu til staðar til að ljúka við færslurnar.

### <a name="create-sales-order-1"></a>Stofna sölupöntun 1

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Veljið **Nýtt** til að búa til sölupöntun 1.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - **Viðskiptavinalykill:** *US-010*
    - **Vöruhús:** *61*

1. Veljið **Í lagi**.
1. Ný sölupöntun opnast. Í flýtiflipanum **Sölupöntunarlínur** skal bæta við línu sem er með eftirfarandi stillingum:

    - **Vörunúmer:** *T0100*
    - **Magn:** *5*

1. Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Afhending**, skal stilla reitinn **Staðfest sendingardagsetning** á daginn í dag.
1. Í flýtiflipanum **Sölupöntunarlínur** skal bæta við annarri línu sem er með eftirfarandi stillingum:

    - **Vörunúmer:** *L0101*
    - **Magn:** *20*

1. Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Afhending**, skal stilla reitinn **Staðfest sendingardagsetning** á daginn í dag.
1. Fyrir hverja línu sem bætt var við, skal fylgja þessum skrefum til að taka frá birgðir:

    1. Velja skal línur sem á að taka frá.
    2. Í flýtiflipanum **Sölupöntunarlínur** skal velja **Birgðir \> Frátekning**.
    3. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá birgðir.
    4. Lokaðu síðunni **Frátekning**.

1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.

    Þegar losuninni er lokið birtast upplýsingaboð sem sýna auðkenni bylgju og sendingar sem voru búin til.

### <a name="create-sales-order-2"></a>Stofna sölupöntun 2

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Veljið **Nýtt** til að búa til sölupöntun 2.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - **Viðskiptavinalykill:** *US-011*
    - **Vöruhús:** *61*

1. Veljið **Í lagi**.
1. Ný sölupöntun opnast. Í flýtiflipanum **Sölupöntunarlínur** skal bæta við línu sem er með eftirfarandi stillingum:

    - **Vörunúmer:** *L0101*
    - **Magn:** *20*

1. Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Afhending**, skal stilla reitinn **Staðfest sendingardagsetning** á daginn í dag.
1. Í flýtiflipanum **Sölupöntunarlínur** skal bæta við annarri línu sem er með eftirfarandi stillingum:

    - **Vörunúmer:** *T0100*
    - **Magn:** *2*

1. Í flýtiflipanum **Upplýsingar um línu**, í flipanum **Afhending**, skal stilla reitinn **Staðfest sendingardagsetning** á daginn í dag.
1. Fyrir hverja línu sem bætt var við, skal fylgja þessum skrefum til að taka frá birgðir:

    1. Velja skal línur sem á að taka frá.
    2. Í flýtiflipanum **Sölupöntunarlínur** skal velja **Birgðir \> Frátekning**.
    3. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá birgðir.
    4. Lokaðu síðunni **Frátekning**.

1. Á aðgerðasvæðinu, í flipanum **Vöruhús**, skal velja **Losa í vöruhús**.

    Þegar losuninni er lokið birtast upplýsingaboð sem sýna auðkenni bylgju og sendingar sem voru búin til.

### <a name="get-work-ids-and-license-plate-numbers"></a>Sækja vinnukenni og númer númeraplötu

Tvö vinnukenni ættu að hafa verið stofnuð, hvert þeirra með tveimur tiltektarlínum. Fylgið eftirfarandi skrefum til að finna vinnukenni og úthlutanir númeraplötu.

1. Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnu**.
1. Í hnitanetinu **Yfirlit**, skal leita í dálknum **Pöntunarnúmer** að sölupöntununum tveimur sem voru stofnaðar rétt í þessu. Skráið niður vinnuauðkenni hverrar sölupöntunar fyrir sig.
1. Veljið línuna fyrir hvora sölupöntun fyrir sig til að sýna tengdar upplýsingar í hnitanetinu **Línur**. Skráið niður staðsetninguna þar sem hvor vara verður tínd úr.
1. Farið í **Birgðastjórnun \> Fyrirspurnir og skýrslur \> Lagerlisti**.
1. Í aðgerðasvæðinu skal velja **Víddir** til að opna svargluggann **Birting víddar**.
1. Gangið úr skugga um að svargluggarnir **Númeraplata**, **Vöruhús** og **Vörunúmer** séu valdir og veljið síðan **Í lagi**.
1. Í glugganum **Sía** skal stilla eftirfarandi síur:

    - **Vörunúmer** – **er eitt af** – *L0101* og *T100*
    - **Vöruhús** – **hefst á** – *61*

1. Skráið niður gildi **Númeraplötu** sem birtist.

## <a name="example-scenario"></a><a name="example-scenario"></a>Dæmi

### <a name="mobile-device-flow-execution--work-confirmation-setup-for-the-product"></a>Framkvæmd flæðis í fartæki - Uppsetning verkstaðfestingar fyrir afurðina

1. Skráðu þig inn í farsímaforrit vöruhúsakerfis sem notandi í vöruhúsi *61*.
1. Farið í **Á útleið \> stofnun klasatiltektar**.

    Síðan **VERK: Úthluta vinnu á klasa** birtist.

1. Færið inn vinnukennið fyrir sölupöntun 1 til að úthluta henni á klasastöðu 1.
1. Veljið **Í lagi** (gátmerkistákn).
1. Færið inn vinnukennið fyrir sölupöntun 2 til að úthluta henni á klasastöðu 2.
1. Veljið **Í lagi** (gátmerkistákn).

    Síðan **VERK: Stofnun klasatiltektar: Tiltekt** birtist og sýnir *Vara L0101 2 PL*.

Vegna þess að klasaprófíllinn stillti fjölda staðsetninga á 2, beinir kerfið þér sjálfkrafa á fyrstu sameinuðu tiltektina: tvö bretti af vöru *L0101*.

Hvenær sem er í eftirfarandi skrefum er hægt að velja flipann **Upplýsingar** til að skoða viðbótarupplýsingar um verkið, t.d. tiltektarstaðsetningu.

1. Stillið reitinn **VARA** á *L0101*. Þetta staðfestir vörunúmerið, sem er krafist fyrir þetta valmyndaratriði (þetta var skilgreint áður með því að velja **Uppsetning verkstaðfestingar** á síðunni **Valmyndaratriði fartækis** þegar þetta valmyndaratriði var stofnað).
1. Sláið inn númeri númeraplötunnar sem tengist vörunni á staðsetningunni sem tínt er úr. Þú munt velja tvö bretti.
1. Stillið reitinn **NP** á *NP\_TILTEKT\_01*.
1. Veljið **Í lagi** (gátmerkistákn).

    Síðan **VERK: Raða: Stofnun klasatiltektar** birtist. Hér raðar þú völdu brettunum tveimur á tiltektarstaðsetningu. Þessi staðsetning gæti verið tankur eða gámur sem er notaður til að aðskilja tíndar birgðar eftir sölupöntun.

1. Skoðið upplýsingarnar sem eru sýndar fyrir vöruna (*L0101*) og magn (*20* ea) sem verður raðað í stöðu 1 (fyrir sölupöntun 1).
1. Stillið reitinn **STAÐA NA** á *1*.
1. Veljið **Í lagi** (gátmerkistákn).
1. Skoðið upplýsingarnar sem eru sýndar fyrir vöruna (*L0101*) og magn (*20* ea) sem verður raðað í stöðu 2 (fyrir sölupöntun 2).
1. Stillið reitinn **STAÐA NA** á *2*.
1. Veljið **Í lagi** (gátmerkistákn).

    Síðan **VERK: Stofnun klasatiltektar: Tiltekt** birtist og sýnir *Vara T0100 7 ea*.

Í þessari atburðarás getur staðsetning 1 ekki samþykkt fullt magn af vörum sem þarf að tína til að uppfylla sölupöntun 1. Staðan verður að vera merkt sem full. Í þessu dæmi er hægt að gera hlutatínslu úr annarri vöru. Önnur varan verður tínd að hluta til fyrir staðsetningu 1 og ný vinna verður stofnuð til að tína eftirstandandi magn til að uppfylla pöntunina.

1. Veljið valmyndarhnappinn (stundum kallaður hamborgari eða hamborgarahnappur) og veljið síðan **Staðsetningin er full**.
1. Auðkennið stöðuna sem er full og veljið *1*.
1. Veljið **Í lagi** (gátmerkistákn).
1. Færa skal inn magn tiltektar sem enn er hægt að tína í staðsetningu 1. Kerfið getur ákveðið hvaða vörunúmer er verið að tína.
1. Færðu inn *2*.
1. Veljið **Í lagi** (gátmerkistákn).
1. Staðfestið vörunúmerið til að ljúka við tínslu eftirstandandi vöru í stöðu 2.
1. Stillið reitinn **VARA** á *T0100*.
1. Veljið **Í lagi** (gátmerkistákn).
1. Færið inn númeraplötuna sem varan er tínd úr með því að stilla reitinn **NP** á *LPREPL04*.
1. Veljið **Í lagi** (gátmerkistákn).
1. Skoðið upplýsingarnar sem eru sýndar fyrir vöruna (*T0100*) og magn (*2* ea) sem verður raðað í stöðu 2 (fyrir sölupöntun 2).
1. Stillið reitinn **STAÐA NA** á *2*.
1. Veljið **Í lagi** (gátmerkistákn).
1. Skoðið upplýsingarnar sem eru sýndar fyrir vöruna (*T0100*) og magn (*2* ea) sem verður raðað í stöðu 1 (fyrir sölupöntun 1).
1. Stillið reitinn **STAÐA NA** á *1*.
1. Veljið **Í lagi** (gátmerkistákn).

    Síðan **VERK: Stofnun klasatiltektar: Frágangur** birtist.

Í þessari atburðarás hefur klasatiltekinni verið lokið og notandanum er sagt að ganga frá tíndum vörum úr staðsetningu 1 og staðsetningu 2 á geymslustaðsetningu *STAGE01*.

1. Fara skal yfir upplýsingarnar á síðunni. Hún sýnir að heildarmagnið *44* verður sett á geymslustaðsetninguna.
1. Veljið **Í lagi** (gátmerkistákn).

    Skilaboðin „Klasa er lokið“ birtast.

Nú er hægt að nota valmyndaratriðið **Tiltekt sölu** til að tína eftirstandandi magn. Síðan er hægt að nota valmyndaratriðið **Hleðsla sölu** til að færa vörurnar úr geymslustaðsetningu yfir á dreifingarstað.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]