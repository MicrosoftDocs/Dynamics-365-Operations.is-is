---
title: Númeraplötustaða staðsetningar
description: Númeraplötustaða staðsetningar gerir þér kleift að sjá hvar tiltekin númeraplata er á staðsetningu með mörgum vörubrettum, eins og staðsetningu þar sem vörubrettum er raðað ofan á hvort annað.
author: Mirzaab
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlate, WHSLocationProfile, WHSLocDirTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: e52b313e0a00c04edf9003aa6292146936f837d4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8889429"
---
# <a name="location-license-plate-positioning"></a>Númeraplötustaða staðsetningar

[!include [banner](../includes/banner.md)]

Númeraplötustaða staðsetningar gerir þér kleift að sjá hvar tiltekin númeraplata er á staðsetningu með mörgum vörubrettum, eins og staðsetningu þar sem vörubrettum er raðað ofan á hvort annað.

Eiginleikinn bætir raðnúmeri við hverja númeraplötu sem er sett á geymslustað. Þetta raðnúmer er notað til að raða númeraplötunum á geymslustaðnum. Þar af leiðandir styður eiginleikinn á snjallan hátt aðstæður þar sem viðskiptavinir nota hallandi hillukerfi og þurfa að vita hvaða númeraplata snýr fram við tiltekt.

Þessi grein sýnir atburðarás sem sýnir hvernig á að setja upp og nota eiginleikann.

## <a name="turn-the-location-license-plate-positioning-feature-on-or-off"></a>Kveiktu eða slökktu á staðsetningareiginleikanum fyrir númeraplötustaðsetningu

Til að nota virknina sem lýst er í þessari grein, *Staðsetning númeraplötu* kveikt verður á eiginleikanum fyrir kerfið þitt. Frá og með Supply Chain Management 10.0.25 er þessi eiginleiki skylda og ekki hægt að slökkva á honum. Ef þú ert að keyra útgáfu eldri en 10.0.25 geta stjórnendur kveikt eða slökkt á þessari virkni með því að leita að *Staðsetning númeraplötu* eiginleiki í [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) vinnurými.

## <a name="example-scenario"></a>Dæmi

### <a name="make-sample-data-available"></a>Gera sýnigögn tiltæk

Til að vinna í gegnum þessar aðstæður með því að nota gildin sem hér koma fram, verður þú að nota kerfi þar sem sýnigögn eru sett upp. Þar að auki verður þú að velja **USMF**-lögaðila áður en þú byrjar.

### <a name="set-up-the-feature-for-this-scenario"></a>Setja upp eiginleikann fyrir þessar aðstæður

Ljúktu við eftirfarandi aðferðir til að setja upp *Staðsetning númeraplötu* eiginleiki fyrir atburðarásina sem er kynnt í þessari grein.

#### <a name="location-profiles"></a>Forstillingar staðsetningar

Kveikja verður á eiginleikanum í staðsetningarforstillingunni fyrir allar staðsetningar þar sem hann verður notaður.

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Vöruhús \> Forstillingar staðsetningar**.
1. Veldu **MAGN-06** í listanum yfir staðsetningarforstillingar á svæðinu vinstra megin.
1. Tveir nýir valkostir verið bætt við af eiginleikanum á flýtiflipanum **Almennt**. Stilla eftirfarandi gildi:

    - **Virkja númeraplötustöðu:** *Já*

        Þegar aðgerðin er stillt á *Já*, verður númeraplötustöðunni haldið við fyrir númeraplötur í staðsetningunni.

    - **Birta númeraplötustöðu í fartæki:** *Já*

        Þegar þessi valkostur er stilltur á *Já*, verður fartækjanotendum sýnd númeraplötustaðan við breytingar og talningu. Þú getur aðeins breytt stillingunni á þessum möguleika þegar kveikt er á eiginleikanum.

1. Veljið **Vista**.

#### <a name="location-directives"></a>Staðsetningarleiðbeiningar

1. Fara í **Vöruhúsakerfi \> Uppsetning \> Staðsetningarleiðbeiningar**.
1. Gakktu úr skugga um að svæðið **Gerð verkbeiðni** sé stillt á *Sölupantanir* í vinstri glugganum.
1. Veldu **61 Tiltektarpöntun sölupöntunar** á listanum yfir staðsetningarleiðbeiningar.
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Á flýtiflipanum **Línur** velur þú línuna sem hefur **raðnúmeragildið** *2*.
1. Á flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum**, velur þú línuna sem hefur **Nafngildi** *Taka til fyrir minna en bretti* (hún ætti að vera eina lína) og breytir **Raðnúmeragildi** hennar í *2*.
1. Veldu **Nýtt** fyrir ofan hnitanetið til að bæta við línu fyrir nýjar aðgerðir í staðsetningarleiðbeiningum.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Raðnúmer:** *1*
    - **Heiti:** *Staðsetning tiltektar 1*

1. Meðan nýja línan er enn valin skaltu velja **Breyta fyrirspurn** fyrir ofan hnitanetið.
1. Veldu flipann **Samtengingar** í fyrirspurnarritlinum.
1. Stækkaðu töfluna **Staðsetningar** til að birta tenginguna við töfluna **Birgðavíddir**.
1. Stækkaðu töfluna **Birgðavíddir** til að birta tenginguna við töfluna **Lagerbirgðir**.
1. Veldu **Birgðavíddir** og veldu síðan **Bæta við töflutengingu**.
1. Í listanum yfir töflur sem birtist í dálkinum **Tengsl** skaltu velja **Númeraplata (númeraplata)**. Veldu síðan **Velja** til að bæta **Númeraplötu** við töflutenginguna **Birgðavíddir**.
1. Veldu **Númeraplötu** og veldu svo **Bæta við töflutengingu**.
1. Í listanum yfir töflur sem birtist velur þú í dálknum **Tengsl** velur þú **Númeraplötustaða staðsetningar (númeraplata)**. Veldu síðan **Velja** til að bæta **Númeraplötustöðu staðsetningar** við töflutenginguna **Birgðavíddir**.

    ![Töflutengingar.](media/LpTableJoin.png "Töflutengingar")

1. Veldu **Í lagi** til að staðfesta uppfærðar töflutengingar og loka fyrirspurnarritlinum.
1. Í flýtiflipanum **Aðgerðir í staðsetningarleiðbeiningum** skal velja **Breyta fyrirspurn** til að opna fyrirspurnarritilinn að nýju.
1. Á flipanum **Svið** velur þú **Bæta við** til að bæta línu við hnitanetið.
1. Stilltu eftirfarandi gildi á nýju línunni:

    - **Tafla:** *Númeraplötustaða staðsetningar*
    - **Afleidd tafla:** *Númeraplötustaða staðsetningar*
    - **Svæði:** *Númeraplötustaða*
    - **Skilyrði:** *1*

    ![Nýtt svið.](media/LpPositionCriteria.png "Nýtt svið")

1. Smelltu á **Í lagi** til að vista breytingarnar og loka fyrirspurnarritlinum.

### <a name="set-up-sample-data-for-this-scenario"></a>Uppsetning sýnigagna fyrir þessar aðstæður

Fyrir þessar aðstæður verður notandinn að skrá sig inn í farsímaforrit vöruhússins með því að nota starfsmann sem er settur upp fyrir vöruhús *61* til að vinna verk. Notandinn verður einnig að ljúka við færslur.

Vegna þess að eiginleikinn *Númeraplötustaða staðsetningar* bætir við nýju kennimerki fyrir númeraplötustöðu staðsetningar, verður þú fyrst að búa til einhver gögn til að styðja við aðstæðurnar.

#### <a name="spot-count-the-first-location"></a>Teljið fyrstu staðsetninguna á staðnum

1. Opnaðu farsímaforritið vöruhússins og skráðu þig inn á vöruhús *61*.
1. Opnaðu **Birgðir \> Telja á staðnum**.
1. Opnaðu síðuna **Telja á staðnum** og stilltu svæðið **Staðsetning** á *01A01R1S1B*.
1. Veljið **Í lagi**.

    Síðan birtir staðsetninguna sem þú slóst inn. Einnig birtast eftirfarandi skilaboð: „Staðsetningu lokið, bæta við nýrri númeraplötu eða vöru?“

1. Smelltu á **Uppfæra** til að bæta við talningu á staðsetningu.
1. Á síðunni **Regluleg talning: Bæta við nýrri númeraplötu eða vöru** skaltu velja svæðið **Vara** og síðan slá inn gildið *A0001*.
1. Veljið **Í lagi**.
1. Á síðunni **Regluleg talning: Bæta við nýrri númeraplötu eða vöru** skaltu velja svæðið **Númeraplata** og síðan slá inn gildið *LP1001* (eða annað númeraplötunúmer að eigin vali).

    Síðan **Regluleg talning: Bæta við nýrri númeraplötu eða vöru** sýnir **Númeraplötustöðu 1**.

1. Veljið **Í lagi**.

    Nú verður þú að tilgreina magn vörunnar sem talin er á númeraplötunni.

1. Stilltu svæðið **Magn** á *10*.
1. Veljið **Í lagi**.

    Síðan birtir staðsetninguna sem þú slóst inn. Einnig birtast eftirfarandi skilaboð: „Staðsetningu lokið, bæta við nýrri númeraplötu eða vöru?“

1. Smelltu á **Uppfæra** til að bæta við annarri talningu á staðsetningu.
1. Á síðunni **Regluleg talning: Bæta við nýrri númeraplötu eða vöru** skaltu velja svæðið **Vara** og síðan slá inn gildið *A0002*.
1. Veljið **Í lagi**.
1. Á síðunni **Regluleg talning: Bæta við nýrri númeraplötu eða vöru** skaltu velja svæðið **Númeraplata** og síðan slá inn gildið *LP1002* (eða annað númeraplötunúmer að eigin vali, að því tilskyldu að númerið sé annað en númeraplötunúmerið sem þú tilgreindir áður).
1. Breyttu stöðu númeraplötunnar með því að stilla reitinn **Númeraplötustaða** á *2*.
1. Veljið **Í lagi**.
1. Tilgreindu magn vörunnar sem talin er á númeraplötunni með því að stilla svæðið **Magn** á *10*.
1. Veljið **Í lagi**.

    Síðan birtir staðsetninguna sem þú slóst inn. Einnig birtast eftirfarandi skilaboð: „Staðsetningu lokið, bæta við nýrri númeraplötu eða vöru?“

1. Veljið **Í lagi**.

Vinnu er nú lokið.

#### <a name="spot-count-the-second-location"></a>Telja aðra staðsetningu á staðnum

1. Opnaðu síðuna **Telja á staðnum** og stilltu svæðið **Staðsetning** á *01A01R1S2B*.
1. Veljið **Í lagi**.

    Síðan birtir staðsetninguna sem þú slóst inn. Einnig birtast eftirfarandi skilaboð: „Staðsetningu lokið, bæta við nýrri númeraplötu eða vöru?“

1. Smelltu á **Uppfæra** til að bæta við talningu á staðsetningu.
1. Á síðunni **Regluleg talning: Bæta við nýrri númeraplötu eða vöru** skaltu velja svæðið **Vara** og síðan slá inn gildið *A0002*.
1. Veljið **Í lagi**.
1. Á síðunni **Regluleg talning: Bæta við nýrri númeraplötu eða vöru** skaltu velja svæðið **Númeraplata** og síðan slá inn gildið *LP1003* (eða annað númeraplötunúmer að eigin vali, að því tilskyldu að númerið sé annað en bæði númeraplötunúmerin sem þú tilgreindir í ferlinu hér á undan).

    Síðan **Regluleg talning: Bæta við nýrri númeraplötu eða vöru** sýnir **Númeraplötustöðu 1**.

1. Veljið **Í lagi**.
1. Tilgreindu magn vörunnar sem talin er á númeraplötunni með því að stilla svæðið **Magn** á *10*.
1. Veljið **Í lagi**.

    Síðan birtir staðsetninguna sem þú slóst inn. Einnig birtast eftirfarandi skilaboð: „Staðsetningu lokið, bæta við nýrri númeraplötu eða vöru?“

1. Veljið **Í lagi**.

Vinnu er nú lokið.

#### <a name="work-details"></a>Upplýsingar um vinnu

> [!NOTE]
> Talningar á staðnum í farsímaforritinu stofna reglulegar talningar í Microsoft Dynamics 365. Vinnan krefst þess að talningar séu samþykktar áður en þær eru bókaðar í birgðir.

1. Innskráning í Dynamics 365 Supply Chain Management.
1. Opnaðu **Vöruhúsastjórnun \> Vinna \> Upplýsingar um vinnu**.
1. Finndu línur með eftirfarandi gildi á flipanum **Yfirlit**:

    - **Gerð verkpöntunar:** *Regluleg talning*
    - **Vöruhús:** *61*
    - **Vinnustaða:** *Bíður yfirferðar*

    Stofna ætti tvö vinnuauðkenni fyrir þessar línur. Staðfesta verður talningar fyrir bæði þessi vinnuauðkenni.

1. Veldu fyrsta vinnuauðkennið fyrir gerð verkbeiðni *Reglulegrar talningar*.
1. Á Aðgerðasvæðinu á flipanum **Vinna** í hópnum **Vinna** velur þú **Regluleg talning**.

    Tvær línur birtast, ein fyrir hverja vöru fyrir sig og númeraplata. Gildin í svæðunum **Talið magn**, **Staðsetning**, **Númeraplata** og **Vara** ættu að passa við talningarfærslurnar sem þú bjóst til í fartækinu. Ef einhver af þessum reitum er ekki sýnilegur skaltu smella á **Sýna víddir** á aðgerðasvæðinu til að bæta þeim við hnitanetið.

1. Veldu báðar línurnar.
1. Veldu **Samþykkja talningu** á aðgerðasvæðinu.
1. Skilaboðin „Bókar - Færslubók“ birtast. Smelltu á **Upplýsingar um skilaboð** til að skoða færslubókarnúmerið.
1. Lokaðu upplýsingunum um skilaboð.
1. Endurhladdu síðuna **Vinna**.

    Fyrsta vinnuauðkenninu hefur verið lokað og er ekki lengur sýnt.

    > [!TIP]
    > Smelltu í gátreitinn **Sýna lokna** fyrir ofan hnitanetið til að skoða vinnu sem er lokið.

    Þú verður nú að samþykkja vinnuna fyrir númeraplötuna í staðsetningu *01A01R1S2B*.

1. Smelltu á flipann **Yfirlit** og veldu annað vinnuauðkenni fyrir gerð verkbeiðni *Reglulegrar talningar*.
1. Á Aðgerðasvæðinu á flipanum **Vinna** í hópnum **Vinna** velur þú **Regluleg talning**.

    Ein lína birtist fyrir vöruna og númeraplötuna. Gildin í svæðunum **Talið magn**, **Staðsetning**, **Númeraplata** og **Vara** ættu að passa við talningarfærslurnar sem þú bjóst til í fartækinu.

1. Veldu línuna.
1. Veldu **Samþykkja talningu** á aðgerðasvæðinu.
1. Skilaboðin „Bókar - Færslubók“ birtast. Smelltu á **Upplýsingar um skilaboð** til að skoða færslubókarnúmerið.
1. Lokaðu upplýsingunum um skilaboð.
1. Endurhladdu síðuna **Vinna**.

    Öðru vinnuauðkenninu hefur verið lokað og er ekki lengur sýnt.

    > [!TIP]
    > Smelltu í gátreitinn **Sýna lokna** fyrir ofan hnitanetið til að skoða vinnu sem er lokið.

#### <a name="on-hand-by-location"></a>Á lager eftir birgðageymslu

1. Opnaðu **Vöruhúsakerfi \> Fyrirpurnir og skýrslur \> Á lager eftir staðsetningu**.
1. Stilla eftirfarandi gildi:

    - **Svæði:** *6*
    - **Vöruhús:** *61*
    - **Uppfæra á öllum staðsetningum:** *Já*

1. Taktu eftir að tvær númeraplötur eru fyrir staðsetningu *01A01R1S1B*:

    - **A0001**, þar sem svæðið **Númeraplötustaður** er stilltur á *1*
    - **A0002**, þar sem svæðið **Númeraplötustaður** er stilltur á *2*

1. Taktu eftir því að ein númeraplata er fyrir staðsetningu *01A01R1S2B*:

    - **A0002**, þar sem svæðið **Númeraplötustaður** er stilltur á *1*

### <a name="sales-order-scenario"></a>Aðstæður sölupöntunar

Nú þegar lokið er við að setja upp eiginleikann *Númeraplötustaða staðsetningar* og birgðunum hefur verið sett á svið verður þú að búa til sölupöntun til að búa til tiltekt sem mun beina vöruhússtarfsmanni að taka til vöru *A0002* úr birgðastaðsetningunni þar sem auðkenni vörubrettis er í stöðu *1*.

1. Farðu í **Sölu og markaðssetningu \> Sölupöntun \> Allar sölupantanir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Sláið inn eftirfarandi gildi í svarglugganum **Stofna sölupöntun**:

    - **Viðskiptavinalykill:** *US-004*
    - **Vöruhús:** *61*

1. Veljið **Í lagi**.
1. Nýrri línu er bætt við hnitanetið á flýtiflipanum **Sölupöntunarlínur**. Stilltu eftirfarandi gildi á þessari nýju línu:

    - **Vörunúmer:** *A0002*
    - **Magn:** *1*

1. Á valmyndinni **Birgðir** fyrir ofan hnitanetið smellir þú á **Frátekning**.
1. Á síðunni **Frátekning**, á aðgerðasvæðinu, skal velja **Frátektarlota** til að taka frá birgðir fyrir pöntunarlínuna.
1. Lokaðu síðunni **Frátekning**.
1. Á aðgerðarrúðunni, á flipanum **Vöruhús**, í hópnum **Aðgerðir**, velurðu **Losa í vöruhús**.

    Þú færð upplýsingaboð sem tilgreina bylgjuauðkenni og sendingarkenni sem voru búin til fyrir pöntunina.

1. Á flýtiflipanum **Sölupöntunarlínur** á valmyndinni **Vöruhús** fyrir ofan hnitanetið smellir þú á **Upplýsingar um vinnu**.
1. Síðan opnast síðan **Vinna** og sýnir vinnuna sem stofnuð var fyrir sölulínuna. Skráið niður vinnuauðkennið sem birtist.

### <a name="sales-picking-scenario"></a>Aðstæður sölutiltektar

1. Opnaðu farsímaforritið og skráðu þig inn á vöruhús *61*.
1. Opnaðu **Á útleið \> Sölutiltekt**.
1. Á síðunni **Skanna vinnuauðkenni / kenni númeraplötu** skaltu smella á svæðið **Auðkenni** og síðan slá inn auðkenni sölulínunnar.
1. Taktu eftir að tiltektin segir þér til að taka til vöru *A0002* úr staðsetningu *01A01R1S2B*. Þú færð þessar leiðbeiningar vegna þess að vara *A0002* er á númeraplötunni sem er í stöðu *1* á þeirri staðsetningu.

    ![Staðsetning á stöðu 1.](media/LocationLicensePlatePositioning.png "Staðsetning stöðu 1")

1. Sláðu inn auðkenni númeraplötunnar sem þú bjóst til fyrir staðsetningu og fylgdu síðan leiðbeiningunum til að velja sölupöntunina.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]