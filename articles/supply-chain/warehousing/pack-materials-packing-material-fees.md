---
title: Umbúðaefni og gjöld
description: Þetta efni veitir upplýsingar um pökkunarefnisgjöld sem eru greidd til endurvinnslufyrirtækja með ákveðnu millibili.
author: MarkusFogelberg
manager: tfehr
ms.date: 02/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventPackagingGroup, InventPackagingMaterialCode, InventPackagingMaterialFee, InventPackagingMaterialTrans, InventPackagingMaterialTransPurch, InventPackagingUnit
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2194
ms.assetid: 040b65dc-43c9-4256-b69f-b2d6e736fbe9
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2020-02-19
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b9ca8653bb3dc00285774d4ead9a8c14c606f24
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234730"
---
# <a name="packing-materials-and-fees"></a>Umbúðaefni og gjöld

[!include [banner](../includes/banner.md)]

Umbúðaefnisgjald er greitt með ákveðnu millibili til endurvinnslufyrirtækis. Upphæð byggð á þyngdareiningu er greidd fyrir hvern þann efnivið sem umbúðaeining samanstendur af. Þó að umbúðaefnisgjald sé reiknað út og tilkynnt eru engar fjárhagsfærslur bókaðar þar sem gjöldin eru ekki reiknuð sem skattur sem greiða skal yfirvöldum.

Þyngd umbúðaefnis og gjöld eru reiknuð bæði fyrir sölu- og innkaupapantanalínur.

Þú getur skilgreint eina eða fleiri umbúðaeiningar fyrir staka vöru, fyrir vöruflokk (pökkunarflokk) eða fyrir allar vörur. Umbúðaeining samanstendur af ýmsum umbúðaefnum, þyngd þess, og vörufjölda sem tilheyrir umbúðaeiningu. Umbúðaefniskóða er úthlutað á hverja gerð umbúðaefnis sem  er skilgreint. Byggt á umbúðaefniskóðanum, er hægt að tilgreina verð fyrir tiltekið tímabil. Umbúðaefnisgjald er reiknað á grundvelli þessara upplýsinga.

> [!NOTE]
> Jafnvel þótt fyrirtækið greiði ekki umbúðaefnisgjald er hægt að nota aðgerðina til að reikna talnagögn fyrir umbúðaþyngd.

## <a name="set-up-packing-material-allocation"></a><a name="allocations"></a>Setja upp úthlutun á umbúðaefni

Áður en þú getur reiknað út þyngd pökkunarefnis, efnisgjald, eða hvort tveggja, verður þú að kveikja á útreikningnum og skilgreina hvaða efni og gjöld gilda um hvaða vörur.

1. Farðu í **Birgðastjórnun \> Uppsetning \> Færibreytur birgða- og vöruhúsakerfis**.
1. Á flipanum **Almennt**, í hlutanum **Umbúðaefni**, stillirðu valkostinn **Reikna umbúðaefnisgjöld** á **Já**.
1. Farðu í **Birgðastjórnun \> Uppsetning \> Umbúðaefni \> Umbúðaflokkar**, og búðu til alla umbúðahópa sem þú notar. Allir hlutir í umbúðahópi nota sömu úthlutun umbúðaefna. Ef þú notar ekki umbúðahópa geturðu sleppt þessu skrefi.

    > [!TIP]
    > Eftir að þú hefur búið til umbúðahópana geturðu úthlutað hóp á hverja afurð eins og þú þarft. Farðu í **Afurðaupplýsingastjórnun \> Afurðir \> Útgefnar afurðir**, veldu afurð og síðan á flýtiflipanum **Stjórna birgðum**, í reitnum **Umbúðaflokkur** velurðu viðeigandi umbúðaflokk.

1. Farðu í **Birgðastjórnun \> Uppsetning \> Umbúðaefni \> Umbúðefnakóðar**, skilgreindu sérhverja gerð umbúðaefnis sem þú notar og tilgreindu eininguna þar sem umbúðaefnið er notað þegar þú undirbýr sendingar.
1. Fara til **Birgðastjórnun \> Uppsetning \> Umbúðaefni \> Umbúðaefnisgjöld**, og stilltu gjald fyrir sérhverja gerð af umbúðaefni sem þú varst að skilgreina. Gjöld eru reiknuð út frá verðinu á hverja einingu sem neytt er.
1. Til að úthluta umbúðaefni á vörur skaltu fara í **Birgðastjórnun \> Uppsetning \> Umbúðaefni \> Úthlutun umbúða** og stofna úthlutanir. Hægt er að stofna eins margar úthlutanir og þarf. Þú getur úthlutað umbúðaefni fyrir stakar vörur, vöruflokka (pökkunarflokka) eða allar vörur, allt eftir því hversu nákvæmar úthlutanir þínar ættu að vera.

    Fyrir hverja úthlutun sem þú stofnar skal fylgja þessum skrefum.

    1. Á flýtiflipanum **Almennt** stillirðu eftirfarandi reiti:

        - **Vörukóði** - Veldu umfang úthlutunar:

            - **Tafla** - Búðu til úthlutun fyrir eina tiltekna vöru.
            - **Hópur** - Búðu til úthlutun fyrir allar þær vörur sem tilheyra pökkunarflokki sem er skilgreindur á síðunni **Pökkunarflokkar**.
            - **Allt** - Búðu til úthlutun fyrir allar vörur.

            > [!NOTE]
            > Venjulega ættir þú að gera allar úthlutanir þínar á sama stigi (**Tafla**, **Hópur** eða **Allt**). Ef þú notar fleiri en eitt stig verður sérstök samsvörunarúthlutun notuð fyrir hverja vöru. (Stigið **Tafla** hefur forgang fram yfir stigið **Hópur** og bæði þessi stig hafa forgang fram yfir stigið **Allt**.)

        - **Vöruvensl** - Ef þú ert að úthluta fyrir eina vöru skaltu velja vöruna. Ef þú ert að úthluta fyrir hóp af vörum skaltu velja pökkunarflokkinn. Ef þú ert að úthluta fyrir allar vörur skaltu skilja þennan reit eftir.
        - **Stillingar**, **Stærð**, **Litur** og **Stíll** - Sláðu inn gildi fyrir þessar víddir eftir þörfum til að skilgreina nánar vöruna sem þú ert að úthluta fyrir.
        - **Umbúðaeining** - Veldu eininguna þar sem vörunni er pakkað í þegar umbúðaefnið er notað. Þessi eining gæti verið frábrugðin einingunni sem varan er keypt og geymd í.
        - **Stuðull umbúðaeiningar** - Sláðu inn umreikningsstuðulinn sem er notaður til að umreikna úr birgðaeiningunni í umbúðaeininguna. (Umbreytingin notar formúluna *Umbúðaeiningar* = *Vörueiningar* × *Stuðull umbúðaeiningar*.)

    1. Á flýtiflipanum **Umbúðaefni** bætirðu við línu fyrir hvert stykki af umbúðaefni sem þarf til núverandi úthlutunar. Tilgreindu á hverja línu tegund efnisins (eins og skilgreint er á síðunni **Umbúðefnakóðar**) og magn þess sem er neytt fyrir hverja senda einingu núverandi vöru.

## <a name="packing-units-on-sales-order-lines"></a>Umbúðaeiningar í sölupöntunarlínum

Eftir að þú hefur gert það [kveiktu á útreikningnum fyrir umbúðaefnisgjöld og settu upp úthlutanir þínar](#allocations), kerfið staðfestir að umbúðaeiningar eru tilgreindar fyrir hverja vöru sem er bætt við sölupöntun. Það reiknar síðan út öll gjöld sem þarf. Þegar hlut er bætt við sölupöntun á sér stað eitt af eftirfarandi skrefum:

- **Ef umbúðaúthlutun á við um vöruna:** Kerfið uppfærir sölupöntunarlínuna með tilgreindri umbúðaeiningu og magni umbúðaeiningar. (Magn fyrir umbúðaeiningu er reiknað með því að nota formúluna *Magn í umbúðaeiningu* = *Pantað magn* ÷ *Fjöldi vara í valinni pökkunareiningu*.)
- **Ef engin umbúðaúthlutun á við um vöruna:** Hægt er að færa inn umbúðaeiningu og magn handvirkt á sölupöntunarlínu.

Einnig er mögulegt að breyta pökkunareiningu og magni hennar þegar sölupöntunarlína er bókuð. Þessi geta á við ef sölupöntunarlína er aðeins afhent eða reikningsfærð að hluta.

Þegar þú reikningsfærir sölupöntun stofnar kerfið nýjar umbúðaefnisfærslur. Umbúðaefnisfærslur innihalda þyngd umbúðaefnis fyrir sölulínuna. Þú getur breytt færslunum eftir að þú hefur reikningsfært þær. Síðan er hægt að stofna nýjar færslur.

## <a name="packing-units-on-purchase-order-lines"></a>Umbúðaeiningar í innkaupapöntunarlínum

Kerfið stofnar ekki umbúðaefnisfærslur fyrir innkaupapöntunarlínur. Þess í stað stofnar þú færslur fyrir reikningsfærðar innkaupapöntunarlínur á síðunni **Umbúðaefnisfærslur**.

## <a name="set-up-license-numbers-for-customers-that-are-charged-packing-material-fees"></a>Settu upp leyfisnúmer fyrir viðskiptavini sem eru rukkaðir um umbúðaefnisgjöld

Ef sölupantanir tiltekins viðskiptavinar eiga að innihalda gjöld fyrir umbúðaefnið sem er notað fyrir hverja pöntun, fylgdu þessum skrefum.

1. Farðu í **Viðskiptakröfur \> Viðskiptavinir \> Alla viðskiptavini**.
1. Veldu viðskiptavininn sem á að rukka fyrir umbúðaefni.
1. Á flýtiflipanum **Reikningur og afhending** stillirðu eftirfarandi reiti:

    - Í hlutanum **Virðisaukaskattur**, í reitnum **Leyfisnúmer fyrir umbúðagjald**, slærðu inn leyfisnúmer fyrirtækisins.
    - Í hlutanum **Umbúðaefnisgjald**, í reitnum **Leyfisnúmer**, slærðu inn leyfisnúmer fyrirtækisins.

Þegar þú býrð til og reikningsfærir sölupöntun sem inniheldur eina eða fleiri vörur sem nota umbúðaefni mun reikningurinn sýna umbúðaefnisgjöldin.

Fylgdu þessum sömu skrefum fyrir viðskiptavini sem ættu ekki að greiða umbúðaefnisgjöld en hreinsaðu leyfisnúmerin úr reitunum **Leyfisnúmer fyrir umbúðagjald** og **Leyfisnúmer**. Reikningar fyrir viðskiptavini sem ekki greiða umbúðaefnisgjald sýna þyngd umbúðaefnanna, en þeir sýna ekki gjöldin.

Til að búa til skýrslu sem sýnir öll umbúðaefnisgjöld sem fyrirtæki þitt skuldar fyrir tiltekið tímabil ferðu á **Birgðastjórnun \> Fyrirspurnir og skýrslur \> Skýrslur um umbúðaefni \> Útreikningur umbúðaefnisgjalds**, tilgreinir dagsetningarsvið og velur síðan **Í lagi**.

## <a name="print-packing-material-weights-on-invoices"></a>Prenta þyngd umbúðaefnis á reikninga

Mögulegt er að prenta þyngd umbúða og gefa til kynna á reikningnum hver greiðir tengd gjöld. Þyngd er dregin saman fyrir hvern pökkunarkóða.

1. Opnið **Viðskiptakröfur \> Setja upp \> Færibreytur viðskiptakrafna**.
1. Á flipanum **Uppfærslur**, á flýtflipanum **Reikningur**, stillirðu valkostinn **Prenta þyngd umbúðaefnis** á **Já**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]