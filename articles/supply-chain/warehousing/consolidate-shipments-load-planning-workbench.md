---
title: Sameina sendingar með því að nota „Losa í vöruhús“ á vinnusvæði farmáætlunar
description: Þetta efnisatriði sýnir aðstæður þar sem margar pantanir eru losaðar í vöruhúsið í sömu hleðslu og eru svo sameinaðar sjálfkrafa í sendingar.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 3d74a4171bc8d601d034afb9b7f12634a8f9dbed
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8672543"
---
# <a name="consolidate-shipments-by-releasing-to-warehouse-from-the-load-planning-workbench"></a>Sameina sendingar með því að nota „Losa í vöruhús“ á vinnusvæði farmáætlunar

[!include [banner](../includes/banner.md)]

Þetta efnisatriði sýnir aðstæður þar sem margar pantanir eru losaðar í vöruhúsið í sömu hleðslu og eru svo sameinaðar sjálfkrafa í sendingar.

## <a name="make-demo-data-available"></a>Bjóða upp á sýnigögn

Aðstæður í þessu efnisatriði vísa í gildi og færslur sem eru innifaldar í stöðluðum sýnigögnum fyrir Microsoft Dynamics 365 Supply Chain Management. Ef nota á gildin sem er boðið upp á hér eins og í æfingunum skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett og stilla lögaðilann á **USMF** áður en hafist er handa.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Setja upp samstæðureglur sendingar og afurðarsíur

Aðstæðurnar sem hér er lýst gera ráð fyrir að þegar hafi verið kveikt á eiginleikanum, farið hafi verið í gegnum æfingarnar í [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md) og reglur og aðrar færslur sem þar er lýst stofnaðar. Gætið þess að gera þessar æfingar áður en haldið er áfram með þessar aðstæður.

## <a name="create-the-sales-orders-for-this-scenario"></a>Búa til sölupantanir fyrir þessar aðstæður

Byrjaðu á því að stofna safn af sölupöntunum sem hægt er að vinna með. Vinna verður með vöruhús sem er virkt fyrir ítarlegt ferli vöruhúsakerfis. Nema annað vöruhús er tilgreint með skýrum hætti verður að nota sama vöruhúsið fyrir hvert eftirtalinna pöntunarsetta.

Opnaðu **Viðskiptakröfur \> Pantanir \> Allar sölupantanir** og búðu til safn sölupantana sem eru með stillingarnar sem lýst er í eftirfarandi undirhlutum.

### <a name="create-order-set-1"></a>Búa til pöntunarsett 1

#### <a name="sales-order-1-1"></a>Sölupöntun 1-1

1. Stofna sölupöntun sem er með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-001*
    - **Afhendingarmáti:** *Airwa-Air*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

1. Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.

#### <a name="sales-order-1-2"></a>Sölupöntun 1-2

1. Stofna sölupöntun sem er með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-001*
    - **Afhendingarmáti:** *Airwa-Air*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

1. Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.

#### <a name="sales-order-1-3"></a>Sölupöntun 1-3

1. Stofna sölupöntun sem er með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-001*
    - **Afhendingarmáti:** *10*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

1. Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.
1. Bæta við annarri pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0002* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*
    - **Afhendingarmáti:** *Airwa-Air*

1. Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá aðra pöntunarlínu.

### <a name="create-order-set-2"></a>Búa til pöntunarsett 2

#### <a name="sales-orders-2-1-and-2-2"></a>Sölupantanir 2-1 og 2-2

1. Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-002*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *M9200* (vara þar sem sía fyrir **kóða 4** er stillt á *eldfimt*)
    - **Magn:** *1.00*

1. Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.
1. Bæta við annarri pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *M9201* (vara þar sem sía fyrir **kóða 4** er stillt á *sprengifimt*)
    - **Magn:** *1.00*
    - **Afhendingarmáti:** *Airwa-Air*

1. Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá aðra pöntunarlínu.

### <a name="create-order-set-3"></a>Búa til pöntunarsett 3

#### <a name="sales-orders-3-1-and-3-2"></a>Sölupantanir 3-1 og 3-2

1. Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-001*
    - **Innkaupabeiðni viðskiptavinar:** *1*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

1. Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.

#### <a name="sales-orders-3-3-and-3-4"></a>Sölupantanir 3-3 og 3-4

1. Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-001*
    - **Innkaupabeiðni viðskiptavinar:** *2*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

1. Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.

### <a name="create-order-set-4"></a>Búa til pöntunarsett 4

#### <a name="sales-orders-4-1-and-4-2"></a>Sölupantanir 4-1 og 4-2

1. Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-003*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

1. Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.

#### <a name="sales-orders-4-3-and-4-4"></a>Sölupantanir 4-3 og 4-4

1. Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-004*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

1. Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.

#### <a name="sales-orders-4-5-and-4-6"></a>Sölupantanir 4-5 og 4-6

1. Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-007*
    - **Svæði:** *6*
    - **Vöruhús:** *61*
    - **Hópur:** *ShipCons*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

1. Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.

#### <a name="sales-orders-4-7-and-4-8"></a>Sölupantanir 4-7 og 4-8

1. Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-007*
    - **Svæði:** *6*
    - **Vöruhús:** *61*
    - **Hópur:** – Hafa þennan reit auðan.

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

1. Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a>Nota vinnusvæði hleðsluáætlunar til að búa til hleðslur og losa þær í vöruhúsið

Fylgið eftirfarandi skrefum til að búa til hleðslu fyrir hvert pöntunarsett sem stofnað var fyrir þessar aðstæður og losið hana síðan í vöruhúsið.

1. Farið í **Vöruhúsakerfi \> Hleðsla \> Vinnusvæði hleðsluáætlunar**.
1. Á flipanum **Sölulínur** skal finna og velja allar sölupöntunarlínur úr einni af pöntunarsettunum sem voru stofnuð fyrir þessar aðstæður.
1. Í aðgerðasvæði, á flipanum **Framboð og eftirspurn** skal velja **Bæta við \> Við nýja hleðslu** til að bæta völdum pöntunarlínum við nýja hleðslu.
1. Í svarglugganum **Úthlutun hleðslusniðmáts** í reitnum **Kenni hleðslusniðmáts** skal velja hleðslusniðmát, svo sem *Stnd hleðslusniðmát*.
1. Veldu **Í lagi** til að loka svarglugganum. 
1. Í hlutanum **Hleðsla** er hægt að finna og velja hleðsluna sem var verið að stofna.
1. Veljið **Losa \> Losa í vöruhús** til að losa valda hleðslu í vöruhúsið.
1. Endurtakið þetta ferli fyrir hin þrjú pantanamengi sem voru stofnuð fyrir þessar aðstæður.

## <a name="verify-the-shipments"></a>Staðfesta sendingar

Eftirfarandi ferli gerir kleift að staðfesta sendingarnar sem hafa verið stofnaðar eða uppfærðar í kjölfar sendingarsameiningar. Notið það til að yfirfara hvert pöntunarsett sem var stofnað fyrir þessar aðstæður og skoðið síðan undirhlutana sem fylgja til að ganga úr skugga um réttar niðurstöður.

1. Opnið **Vöruhúsakerfi \> Sendingar \> Allar sendingar**.
1. Finnið og veljið þá sendingu sem um ræðir.
1. Ef samstæðuregla var notuð þegar sendingin var stofnuð eða hún var uppfærð ætti hún að koma fram í reitnum **Samstæðuregla sendingar**.

### <a name="release-order-set-1-in-one-load"></a>Losunarpantanasett 1 í einum farmi

Tvær sendingar ættu að hafa verið stofnaðar:

- Fyrsta sendingin inniheldur þrjár línur og var búin til með því að nota samstæðureglu sendingar *CustomerMode*.
- Önnur sendingin, sem notar ekki flutningsmátann *Flugfélög*, var stofnuð með því að nota samstæðureglu sendingar *CustomerOrderNo*.

### <a name="release-order-set-2-in-one-load"></a>Losunarpantanasett 2 í einum farmi

Þrjár sendingar ættu að hafa verið stofnaðar:

- Fyrsta sendingin inniheldur *eldfimu* vörurnar.
- Hvor hinna sendinganna tveggja inniheldur eina línu með vöru sem er *sprengifim*.

### <a name="release-order-set-3-in-one-load"></a>Losunarpantanasett 3 í einum farmi

Tvær sendingar ættu að hafa verið stofnaðar:

- Fyrsta sendingin inniheldur pöntunarlínur úr sölupöntuninni þar sem reiturinn **Innkaupabeiðni viðskiptavinar** er stilltur á *1*.
- Önnur sendingin inniheldur pöntunarlínur úr sölupöntun þar sem reiturinn **Innkaupabeiðni viðskiptavinar** er stilltur á *2*.

### <a name="release-order-set-4-in-one-load"></a>Losunarpantanasett 4 í einum farmi

Fjórar sendingar ættu að hafa verið stofnaðar:

- Línur úr tveimur pöntunum fyrir viðskiptavinalykil *US-003* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.
- Línur úr tveimur pöntunum fyrir viðskiptavinalykil *US-004* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.
- Línur úr sölupöntun 4-5 og 4-6 fyrir viðskiptavinalykil *US-007* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.
- Línur úr sölupöntun 4-7 og 4-8 fyrir viðskiptavinlykil *US-007* voru settar saman í sendingu með því að nota *CrossOrder* úr samstæðureglu sendingar.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Samstæðureglur sendingar](about-shipment-consolidation-policies.md)
- [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]