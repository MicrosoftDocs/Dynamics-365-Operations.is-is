---
title: Festing
description: Þessi grein lýsir hvernig á að kveikja á og nota festingu.
author: GalynaFedorova
ms.date: 07/29/2021
ms.topic: article
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2021-07-29
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 8a0fa849f07f0cc0a41a663fc97b5aba927700b1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903812"
---
# <a name="anchoring"></a>Festing

[!include [banner](../includes/banner.md)]

Þessi grein veitir upplýsingar um ferli festingar. Það útskýrir uppsetningu sem krafist er og rökin sem eru keyrð þegar starfsmaður í vöruhúsi breytir annaðhvort bráðabirgðarstaðsetningu eða hleðslustaðsetningu.

Eiginleiki festingar gerir þér kleift að hnekkja bráðabirgðar- eða hleðslustaðsetningu. Öllum opnum frágangi verður þá vísað á nýja bráðabirgðar- eða hleðslustaðsetningu sem þú tilgreinir.

Þessi eiginleiki getur auðveldað starfsmönnum skilvirkari vinnubrögð þegar þeir senda varning. Hér eru nokkur dæmi:

- Starfsmaður sem verður að setja vörur í pöntun 1 í bráðabirgðarstaðsetningu við dreifingarstöð 1 getur ekki lokið þessari aðgerð þar sem fyrri farmur hefur ekki verið færður úr staðsetningunni. Frekar en að bíða eftir að sviðsetningarstaðsetning á dreifingarstöð 1 verði tiltæk ákveður starfsmaðurinn að nota staðsetningu sviðsetningar fyrir dreifingarstöð 2. Þess vegna hnekkir starfsmaðurinn ráðlagðri staðsetningu sviðsetningar. Frágangsstaðsetning fyrir allar eftirstandandi vörur er síðan uppfærð í staðsetningu sviðsetningar á dreifingarstöð 2.
- Starfsmaður sem verður að framkvæma margar tiltektir fyrir sömu afhendingu getur verið viss um að öllum frágangsvörum sé safnað á sama staðinn. Þess vegna þarf minni tíma til að hlaða vörunum í flutningabílinn.

Þú stillir festingu fyrir valmyndaratriði fartækis með því að nota valkostinn **Festing**. Ef þú stillir valkostinn á *Já* getur þú notað reitinn **Festa við** til að tilgreina hvort þú viljir festa við sendingu eða farm. Ef þú stillir reitinn **Festa við** á *Sending* verður næstu opnum frágöngum breytt í nýju staðsetninguna fyrir þá sendingu. Ef þú stillir hann á *Farm* verður næstu opnum frágöngum breytt í nýju staðsetninguna fyrir þann farm.

> [!IMPORTANT]
> Staðsetningunni fyrir opinn frágang sem fylgir í kjölfarið verður breytt í vinnulínurnar sem eru búnar til úr sömu vinnusniðmátslínunni. Með öðrum orðum mun kerfið festa frágangslínurnar sem koma upprunalega úr sömu vinnusniðmátslínunni.

Í þessari grein er að finna aðstæður sem sýna hvernig festing virkar. Í aðstæðunum verða söfn sölupantana stofnuð og þau losuð til vöruhússins. Þú hnekkir síðan ráðlagðri bráðabirgðarstaðsetningu og staðfestir að allri eftirstandandi frágangsvinnu er beint á nýju staðsetninguna.

## <a name="scenario-prerequisite-make-demo-data-available"></a>Skilyrði fyrir aðstæðurnar: Bjóða upp á sýnigögn

Aðstæður í þessari grein vísa í gildi og færslur sem eru innifaldar í stöðluðum sýnigögnum fyrir Microsoft Dynamics 365 Supply Chain Management. Ef nota á gildin sem er boðið upp á hér eins og í æfingunum skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett og stilla lögaðilann á *USMF* áður en hafist er handa.

## <a name="scenario-setup"></a>Uppsetning sviðsmyndar

Áður en unnið er í gegnum sýnidæmið þarf að virkja festingu fyrir viðeigandi valmyndaratriði fartækis.

### <a name="set-up-a-mobile-device-menu-item-to-enable-anchoring"></a>Setja upp valmyndaratriði fartækis til að virkja festingu

Fylgdu þessum skrefum til að virkja festingu fyrir valmyndaratriði fartækis.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Á listasvæðinu skal velja færsluna sem heitir *Tiltekt sölu*. Ef engin fyrirliggjandi færsla er með það heiti skal búa hana til. Staðfestið eða stillið eftirfarandi gildi fyrir færsluna:

    - **Heiti valmyndaratriðis:** *Tiltekt sölu*
    - **Tiltekt:** *Tiltekt sölu*
    - **Máti:** *Vinna*
    - **Nota fyrirliggjandi vinnu:** *Já*
    - **Stýrt af:** *Notandastýrt*
    - **Festing:** *Já*

        Þessi stilling veldur því að kerfið festir margar verkbeiðnilínur saman meðan á tiltekt sölu stendur.

    - **Fest eftir:** *Farmur*

        Þessi stilling veldur því að kerfið festir eftir farmi.

    - **Hnekkja yfirnúmeraplötu:** *Já*
    - **Hnekkja númeraplötu við frágang:** *Já*
    - **Láta notanda halda vinnu læstri:** *Já*
    - **Leyfa umframtiltekt:** *Já*

### <a name="set-up-a-work-template-to-enable-staging"></a>Setja upp vinnusniðmát til að virkja flutning á biðsvæði

Fylgdu þessum skrefum til að skilgreina vinnusniðmát til að virkja flutning á biðsvæði. Þessi stilling mun styðja við aðstæður þar sem starfsmaður setur vörur pöntunar á bráðabirgðarstaðsetningu.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Vinna \> Vinnusniðmát**.
1. Í reitnum **Gerð verkbeiðni** velurðu *Sölupantanir*.
1. Í hnitanetinu skal velja vinnusniðmátið **61 Biðsvæði sölupöntunar**.
1. Í hlutanum **Upplýsingar vinnusniðmáts** skal ganga úr skugga um að eftirfarandi línur séu til staðar og skilgreindar eins og hér er sýnt:

    - Lína 1:

        - **Verkgerð:** *Tiltekt*
        - **Áskilið:** Valið (= *Já*)
        - **Auðkenni vinnuklasa:** *Tiltekt sölupöntunar*

    - Lína 2:

        - **Tegund vinnu:** *Frágangur*
        - **Áskilið:** Valið (= *Já*)
        - **Leiðbeiningarkóði:** *Stig*
        - **Auðkenni vinnuklasa:** *Tiltekt sölupöntunar*

    - Lína 3:

        - **Verkgerð:** *Tiltekt*
        - **Áskilið:** Valið (= *Já*)
        - **Stöðva vinnu:** *Já*
        - **Auðkenni vinnuklasa:** *Sölupöntunarálag*

    - Lína 4:

        - **Tegund vinnu:** *Frágangur*
        - **Áskilið:** Valið (= *Já*)
        - **Leiðbeiningarkóði:** *Útskot*
        - **Auðkenni vinnuklasa:** *Sölupöntunarálag*

1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn** til að opna fyrirspurnarritil.
1. Gakktu úr skugga um að eftirfarandi lína sé til staðar í flipanum **Svið**:

    - **Tafla:** *Tímabundnar vinnufærslur*
    - **Afleidd tafla:** *Tímabundnar vinnufærslur*
    - **Svæði:** *Vöruhús*
    - **Skilyrði:** *61*

1. Gakktu úr skugga um að eftirfarandi lína sé til staðar í flipanum **Röðun**:

    - **Tafla:** *Tímabundnar vinnufærslur*
    - **Afleidd tafla:** *Tímabundnar vinnufærslur*
    - **Reitur:** *Auðkenni sendingar*
    - **Leitarstefna:** *Hækkandi*

1. Veldu **Í lagi** til að nota stillingarnar þínar og loka fyrirspurnarritilinum. Samþykktu breytingarnar ef beðið er um það.
1. Á aðgerðasvæðinu skal velja **Vinnuhausaskil**.
1. Í línunni þar sem reiturinn **Heiti svæðis** er stillt á *Auðkenni sendingar* skal ganga úr skugga um að gátreiturinn **Flokka eftir þessum reit** sé valinn.

### <a name="set-up-license-plates-locations-and-inventory"></a>Setja upp númeraplötur, staðsetningar og birgðir

Áður en þú útbýrð sölupantanir og sendingar þarftu að tryggja að til séu nauðsynlegar staðsetningar, númeraplötur og birgðir.

1. Farið í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Númeraplötur** og búið til tvær númeraplötur:

    - MyLP1
    - MyLP2

1. Farðu **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Staðsetningar** og búðu til eftirfarandi staðsetningar ef þær eru ekki þegar til staðar.

    | Vöruhús | Staður   | Auðkenni forstillingar staðsetningar | Svæðisauðkenni   |
    |-----------|------------|---------------------|-----------|
    | 61        | 06A01R2S1B | PICK-06             | Hæð     |
    | 61        | 06A01R3S1B | PICK-06             | Hæð     |
    | 61        | STAGE01    | ÞREP               | *(Autt)* |
    | 61        | STAGE02    | ÞREP               | *(Autt)* |
    | 61        | STAGE03    | ÞREP               | *(Autt)* |
    | 61        | STAGE04    | ÞREP               | *(Autt)* |

1. Gakktu úr skugga um að eftirfarandi birgðir séu tiltækar. Ef þú verður að breyta birgðum geturðu búið til handvirkar birgðahreyfingar, notað áfyllingu eða notað hvaða annað flæði sem er.

    | Vörunúmer | Magn | Vöruhús | Staður   | Númeraplata |
    |-------------|----------|-----------|------------|---------------|
    | A0001       | 100      | 61        | 06A01R2S1B | MyLP1         |
    | A0002       | 100      | 61        | 06A01R3S1B | MyLP2         |

### <a name="create-demand"></a>Búa til eftirspurn

Áður en þú getur prófað virkni festingar þarftu að búa til eftirspurn. Fyrir þessar aðstæður býrðu til þrjár sölupantanir fyrir sama viðskiptavininn.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Veldu **Ný** til að stofna fyrstu sölupöntunina.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - **Viðskiptavinalykill:** *US-001*
    - **Vöruhús:** *61*

1. Veldu **Í lagi**.
1. Ný sölupöntun opnast. Hún inniheldur auða línu í flýtiflipanum **Sölupöntunarlína**. Stilltu eftirfarandi gildi fyrir þessa línu:

    - **Vörunúmer:** *A0001*
    - **Magn:** *1*

1. Á tækjastikunni skal velja **Bæta við línu** til að bæta við annarri sölupöntunarlínu og stilla eftirfarandi gildi fyrir hana:

    - **Vörunúmer:** *A0002*
    - **Magn:** *1*

1. Fylgið þessum skrefum fyrir hverja sölulínu í pöntuninni til að taka frá birgðir fyrir hana:

    1. Í flýtiflipanum **Sölupöntunarlínur** skal velja sölupöntunarlínu.
    1. Á tækjastikunni skal velja **Birgðir \> Frátekning**.
    1. Á síðunni **Frátekning** skal velja **Frátektarlota** og loka svo síðunni.
    1. Í aðgerðarúðunni skal velja **Vista**.

1. Endurtakið skref 2 til 6 til að stofna aðra sölupöntun. Stillið eftirfarandi gildi fyrir hana:

    - Í svarglugganum **Stofna sölupöntun**:

        - **Viðskiptavinalykill:** *US-001*
        - **Vöruhús:** *61*

    - Á sölupöntunarlínu 1:

        - **Vörunúmer:** *A0001*
        - **Magn:** *2*

    - Á sölupöntunarlínu 2:

        - **Vörunúmer:** *A0002*
        - **Magn:** *2*

1. Endurtakið skref 7 til að taka frá hverja línu í sölupöntun 2.
1. Endurtakið skref 2 til 6 til að stofna þriðju sölupöntun. Stillið eftirfarandi gildi fyrir hana:

    - Í svarglugganum **Stofna sölupöntun**:

        - **Viðskiptavinalykill:** *US-001*
        - **Vöruhús:** *61*

    - Á sölupöntunarlínu 1:

        - **Vörunúmer:** *A0001*
        - **Magn:** *3*

    - Á sölupöntunarlínu 2:

        - **Vörunúmer:** *A0002*
        - **Magn:** *3*

1. Endurtakið skref 7 til að taka frá hverja línu í sölupöntun 3.

### <a name="use-the-load-planning-workbench-to-create-a-load-and-release-it-to-the-warehouse"></a>Notið vinnusvæði hleðsluáætlunar til að búa til hleðslu og losa hana í vöruhúsið

Fylgið þessum skrefum til að búa til hleðslu fyrir pantanir sem stofnaðar voru fyrir þessar aðstæður og losa þær síðan í vöruhúsið.

1. Farið í **Vöruhúsakerfi \> Hleðsla \> Vinnusvæði hleðsluáætlunar**.
1. Í flipanum **Sölulínur** skal finna og velja allar sölupöntunarlínur fyrir sölupöntun 1 og sölupöntun 2.
1. Á aðgerðasvæðinu, í flipanum **Framboð og eftirspurn**, í flokknum **Bæta við**, skal velja **Við nýjan farm**.
1. Í svarglugganum **Úthlutun hleðslusniðmáts** í reitnum **Kenni hleðslusniðmáts** skal velja hleðslusniðmát, svo sem *Stnd hleðslusniðmát*.
1. Veldu **Í lagi** til að loka svarglugganum.
1. Í hlutanum **Hleðsla** er hægt að finna og velja hleðsluna sem var stofnuð.
1. Á tækjastikunni skal velja **Losa \> Losa í vöruhús**.
1. Í svarglugganum **Losa farm í vöruhús** skal velja **Í lagi** til að losa valda hleðslu í vöruhúsið.
1. Farið í **Vöruhúsakerfi \> Vinna \> Öll vinna** til að skoða vinnuna sem var stofnuð. Þú ættir að finna tvö ný vinnukenni, eitt fyrir hverja sendingu. Hvert vinnukenni er með tiltektar- og frágangslínur sem færa birgðir úr tiltektarstaðsetningum í bráðabirgðastaðsetningu og úr bráðabirgðastaðsetningu í útskot. Skráið hjá ykkur gildið fyrir **Vinnukennið** fyrir fyrstu afhendingu því það þarf að nota það í næsta skrefi.

### <a name="sales-order-picking-to-the-staging-location-for-the-first-shipment"></a>Tiltekt sölupöntunar yfir í bráðabirgðastaðsetningu fyrir fyrstu sendinguna

1. Skráðu þig inn í farsímaforrit vöruhúsakerfis sem starfsmaður í vöruhúsi *61*. (Í stöðluðum sýnigögnum getur þú skráð þig inn með því að nota _61_ sem notandakenni og _1_ sem aðgangsorð.)
1. Í aðalvalmyndinni skal velja **Á útleið**.
1. Í valmyndinni **Á útleið** skal velja **Sölutiltekt**.
1. Veldu reitinn **Auðkenni** og færðu síðan inn vinnukennið fyrir fyrstu sendinguna.
1. Staðfestu færsluna.
1. Í reitinn **Númeraplata** skal færa inn númer númeraplötu fyrir fyrstu vöruna (*MyLP1*).
1. Staðfestu færsluna.
1. Í reitinn **Marknúmeraplata** skal færa inn hvaða númer sem er (marknúmeraplatan þarf ekki að vera þegar til staðar).

    Velja skal allar línur sem búnar voru til í bylgjunni sem unnið var úr og yfir í sömu marknúmeraplötuna.

1. Staðfestu færsluna.
1. Í reitinn **Númeraplata** skal færa inn númer númeraplötu fyrir aðra vöruna (*MyLP2*).
1. Staðfestu færsluna.

    Ímyndaðu þér að starfsmaðurinn hafi safnað saman pöntuninni en þegar hann fer á bráðabirgðastaðsetninguna sem tilgreind er í vinnunni, tekur hann eftir að bilið er þegar í notkun. Starfsmaðurinn sér þó að önnur nálæg staðsetning (*STAGE03*) er tiltæk. Hann óskar þar af leiðandi eftir því að breyta bráðabirgðastaðsetningunni. Þar sem eiginleiki festingar er virkjaður mun kerfið þá sjálfkrafa uppfæra bráðabirgðastaðsetninguna fyrir þessa og allar tengdar vinnur.

1. Veldu **Hnekkja staðsetningu** til að hnekkja bráðabirgðastaðsetningu sem stungið er upp á.
1. Í reitnum **Undantekningar verks** skal tilgreina *Bráðabirgðastað breytt*.
1. Í reitinn **Staðsetning** skal færa inn nýja bráðabirgðastaðsetningu (*STAGE03*).
1. Staðfestu færsluna. Skilaboðin „Vinnu er lokið“ birtast.
1. Farið í **Vöruhúsakerfi \> Vinna \> Öll vinna**.
1. Opnaðu vinnukennið fyrir fyrstu sendinguna. Staðfestu að bráðabirgðastaðsetningin hafi verið uppfærð yfir á nýju staðsetninguna (*STAGE03*) sem var skilgreind með því að nota fartækið.
1. Opnaðu vinnukennið fyrir aðra sendinguna. Gakktu úr skugga um að bráðabirgðastaðsetningin hafi verið uppfærð í nýja bráðabirgðastaðsetningu (*STAGE03*) vegna uppsetningar festingar.

> [!NOTE]
> Staðsetningin fyrir allar eftirstandandi opnar vinnulínur frágangs sem eru með sömu bráðabirgðastaðsetningu og var búin til úr sömu vinnusniðmátslínunni verður uppfærð í nýju staðsetninguna.

### <a name="use-the-load-planning-workbench-to-add-the-new-sales-order-to-the-existing-load"></a>Nota vinnusvæði hleðsluáætlunar til að bæta nýju sölupöntuninni við fyrirliggjandi hleðslu

Fylgdu þessum skrefum til að bæta pöntun við hleðsluna og losaðu hana síðan í vöruhúsið.

1. Farið í **Vöruhúsakerfi \> Hleðsla \> Vinnusvæði hleðsluáætlunar**.
1. Í flipanum **Sölulínur** skal finna og velja allar sölupöntunarlínur fyrir sölupöntun 3.
1. Á aðgerðasvæðinu, í flipanum **Framboð og eftirspurn**, í flokknum **Bæta við**, skal velja **Við fyrirliggjandi farm** til að bæta völdum pöntunarlínum við fyrirliggjandi farm.
1. Veldu **Í lagi** til að loka svarglugganum.
1. Í hlutanum **Farmar** skal finna og velja farminn úr fyrri skrefum.
1. Veljið **Losa \> Losa í vöruhús**.
1. Í svarglugganum **Losa farm í vöruhús** skal velja **Í lagi** til að losa valda hleðslu í vöruhúsið.
1. Farið í **Vöruhúsakerfi \> Vinna \> Öll vinna** til að skoða vinnuna sem var stofnuð. Skráið hjá ykkur gildið fyrir **Vinnukennið** því það þarf að nota það í næsta skrefi.

### <a name="sales-order-picking-to-the-staging-location-for-the-third-shipment"></a>Tiltekt sölupöntunar yfir í bráðabirgðastaðsetningu fyrir þriðju sendinguna

1. Skráðu þig inn í forrit fartækisins sem starfsmaður í vöruhúsi *61*.
1. Í aðalvalmyndinni skal velja **Á útleið**.
1. Í valmyndinni **Á útleið** skal velja **Sölutiltekt**.
1. Veldu reitinn **Auðkenni** og færðu síðan inn vinnukennið fyrir þriðju sendinguna.
1. Staðfestu færsluna.
1. Í reitinn **Númeraplata** skal færa inn númer númeraplötu fyrir fyrstu vöruna (*MyLP1*).
1. Staðfestu færsluna.
1. Í reitinn **Marknúmeraplata** skal færa inn hvaða númer sem er (marknúmeraplatan þarf ekki að vera þegar til staðar).
1. Staðfestu færsluna.
1. Í reitinn **Númeraplata** skal færa inn númer númeraplötu fyrir aðra vöruna (*MyLP2*).
1. Staðfestu færsluna.

    Hvað varðar fyrsta farminn skaltu ímynda þér að starfsmaðurinn komist að því að tilgreind bráðabirgðastaðsetning sé ekki tiltæk. Af þeim sökum vill hann nota aðra bráðabirgðastaðsetningu (*STAGE04*).

1. Veldu **Hnekkja staðsetningu** til að hnekkja bráðabirgðastaðsetningu sem stungið er upp á.
1. Í reitnum **Undantekningar verks** skal tilgreina *Bráðabirgðastað breytt*.
1. Í reitinn **Staðsetning** skal færa inn nýja bráðabirgðastaðsetningu (*STAGE04*).
1. Staðfestu færsluna. Skilaboðin „Vinnu er lokið“ birtast.
1. Farið í **Vöruhúsakerfi \> Vinna \> Öll vinna**.
1. Opnaðu vinnukennið fyrir fyrstu sendinguna. Gakktu úr skugga um að bráðabirgðastaðsetningin hafi ekki verið uppfærð í nýju bráðabirgðastaðsetninguna (*STAGE04*) vegna þess að eftirstandandi opin frágangslína samsvarar ekki vinnusniðmátslínu lokinnar frágangslínu.
1. Opnaðu vinnukennið fyrir aðra sendinguna. Gakktu úr skugga um að bráðabirgðastaðsetningin hafi ekki verið uppfærð í nýju bráðabirgðastaðsetninguna (*STAGE04*) vegna þess að bráðabirgðastaðsetningin samsvarar ekki bráðabirgðastaðsetningu lokinnar frágangslínu. Með öðrum orðum eru fullkláruð lína og eftirstandandi opin vinnulína með mismunandi bráðabirgðastaðsetningar og í þessu tilfelli eru aðeins línur sem eru með sömu bráðabirgðastaðsetningarnar uppfærðar.
1. Opnaðu vinnukennið fyrir þriðju sendinguna. Gakktu úr skugga um að bráðabirgðastaðsetningin hafi verið uppfærð í nýja bráðabirgðastaðsetningu (*STAGE04*).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
