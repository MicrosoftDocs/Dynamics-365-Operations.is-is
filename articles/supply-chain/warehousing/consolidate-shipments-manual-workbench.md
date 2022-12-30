---
title: Sameina sendingar með því að nota samstæðuvinnusvæði sendinga
description: Þessi grein sýnir aðstæður þar sem margar pantanir eru losaðar í vöruhúsið og síðan sameinaðar í sendingar síðar með því að nota samstæðuvinnusvæði sendingar.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: eed484cd37b02e58831e0041c3e0625091283b65
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428118"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a>Sameina sendingar með því að nota samstæðuvinnusvæði sendinga

[!include [banner](../includes/banner.md)]

Þessi grein sýnir aðstæður þar sem margar pantanir eru losaðar í vöruhúsið og síðan sameinaðar í sendingar síðar með því að nota samstæðuvinnusvæði sendingar.

## <a name="make-demo-data-available"></a>Bjóða upp á sýnigögn

Aðstæður í þessari grein vísa í gildi og færslur sem eru innifaldar í stöðluðum sýnigögnum fyrir Microsoft Dynamics 365 Supply Chain Management. Ef nota á gildin sem er boðið upp á hér eins og í æfingunum skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett og stilla lögaðilann á **USMF** áður en hafist er handa.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Setja upp samstæðureglur sendingar og afurðarsíur

Aðstæðurnar sem hér er lýst gera ráð fyrir að þegar hafi verið kveikt á eiginleikanum, farið hafi verið í gegnum æfingarnar í [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md) og reglur og aðrar færslur sem þar er lýst stofnaðar. Gætið þess að gera þessar æfingar áður en haldið er áfram með þessar aðstæður.

## <a name="turn-the-manual-shipment-consolidation-feature-on-or-off"></a>Kveikja eða slökkva á eiginleika handvirkrar sameiningar á sendingu

Til að nota handvirka sameiningu sendingar þarf að kveikja á því fyrir kerfið. Sem hluti af Supply Chain Management, útgáfa 10.0.29, er sjálfgefið kveikt á þessum eiginleika. Stjórnendur geta kveikt eða slökkt á þessari virkni með því að leita að eiginleikanum *Handvirk sameining sendingar* á vinnusvæðinu [Eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Einnig þarf að kveikja á eiginleikanum *Sameina sendingar* áður en hægt er að búa til reglur (frá og með útgáfu 10.0.29 af Supply Chain Management er þessi eiginleiki áskilinn og ekki er hægt að slökkva á honum.) Frekari upplýsingar er að finna í [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md).

## <a name="create-the-sales-orders-for-this-scenario"></a>Búa til sölupantanir fyrir þessar aðstæður

Byrjaðu á því að stofna safn af sölupöntunum sem hægt er að vinna með. Vinna verður með vöruhús sem er virkt fyrir ítarlegt ferli vöruhúsakerfis. Nema annað vöruhús er tilgreint með skýrum hætti verður að nota sama vöruhúsið fyrir hvert eftirtalinna pöntunarsetta.

Opnaðu **Viðskiptakröfur \> Pantanir \> Allar sölupantanir** og búðu til safn sölupantana sem eru með stillingarnar sem lýst er í eftirfarandi undirhlutum.

### <a name="create-order-set-1"></a>Búa til pöntunarsett 1

#### <a name="sales-orders-1-1-and-1-2"></a>Sölupantanir 1-1 og 1-2

1. Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:

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
    - **Afhendingarmáti:** *Airwa-Air*

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

## <a name="release-the-orders-to-the-warehouse"></a>Losa pantanirnar í vöruhúsið

Fylgdu þessum skrefum til að losa hverja sölupöntun sem þú bjóst til fyrir þessar aðstæður í vöruhúsið.

1. Opna **Viðskiptakröfur \> Pantanir \> Allar sölupantanir**.
1. Finnið og veljið sölupöntun sem á að losa.
1. Á aðgerðasvæðinu, á flipanum **Vöruhús**, skal velja **Aðgerðir \> Losa í vöruhús** til að losa valda sölupöntun.
1. Endurtakið þetta ferli fyrir hverja sölupöntun sem var stofnuð fyrir þessar aðstæður.

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a>Sameina sendingarnar með því að nota samstæðuvinnusvæði sendinga

1. Opnaðu **Vöruhúsakerfi \> Losa í vöruhús \> Samstæðuvinnusvæði sendinga**.
1. Á aðgerðasvæðinu skal velja **Breyta fyrirspurn**.
1. Í svarglugga fyrirspurnarritils á flipanum **Svið** skal velja **Bæta við** til að bæta við línu sem er með eftirfarandi stillingar á hnitanetinu:

    - **Tafla:** *Sölupantanir*
    - **Svæði:** *Sölupöntun*
    - **Skilyrði:** Færa skal inn kommuaðgreinda lista yfir sölupöntunarnúmer fyrir hvert pöntunarsett sem var búið til fyrir aðstæðurnar.

1. Velja skal **Í lagi** til að vista fyrirspurnina og loka glugganum.
1. Á aðgerðasvæðinu skal velja **Sameina sendingar**.
1. Veljið allar sendingar og síðan, á aðgerðasvæðinu, veljið **Sameina**.

## <a name="verify-the-shipments"></a>Staðfesta sendingar

Eftirfarandi ferli gerir kleift að staðfesta sendingarnar sem hafa verið stofnaðar eða uppfærðar í kjölfar sendingarsameiningar. Notið það til að yfirfara hvert pöntunarsett sem var stofnað fyrir þessar aðstæður og skoðið síðan undirhlutana sem fylgja til að ganga úr skugga um réttar niðurstöður.

1. Opnið **Vöruhúsakerfi \> Sendingar \> Allar sendingar**.
1. Finnið og veljið þá sendingu sem um ræðir.
1. Ef samstæðuregla var notuð þegar sendingin var stofnuð eða hún var uppfærð ætti hún að koma fram í reitnum **Samstæðuregla sendingar**.

### <a name="related-shipments-for-order-set-1"></a>Tengdar sendingar fyrir pöntunarsett 1

Tvær sendingar ættu að hafa verið stofnaðar:

- Fyrsta sendingin inniheldur þrjár línur og var búin til með því að nota samstæðureglu sendingar *CustomerMode*.
- Önnur sendingin, sem notar ekki flutningsmátann *Flugfélög*, var stofnuð með því að nota samstæðureglu sendingar *CustomerOrderNo*.

### <a name="related-shipments-for-order-set-2"></a>Tengdar sendingar fyrir pöntunarsett 2

Þrjár sendingar ættu að hafa verið stofnaðar:

- Fyrsta sendingin inniheldur vörur sem eru *eldfimar*.
- Hvor hinna sendinganna tveggja inniheldur eina línu með vöru sem er *sprengifim*.

### <a name="related-shipments-for-order-set-3"></a>Tengdar sendingar fyrir pöntunarsett 3

Tvær sendingar ættu að hafa verið stofnaðar:

- Fyrsta sendingin inniheldur pöntunarlínur úr sölupöntuninni þar sem reiturinn **Innkaupabeiðni viðskiptavinar** er stilltur á *1*.
- Önnur sendingin inniheldur pöntunarlínur úr sölupöntun þar sem reiturinn **Innkaupabeiðni viðskiptavinar** er stilltur á *2*.

### <a name="related-shipments-for-order-set-4"></a>Tengdar sendingar fyrir pöntunarsett 4

Fjórar sendingar ættu að hafa verið stofnaðar:

- Línur úr tveimur pöntunum fyrir viðskiptavin *US-003* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.
- Línur úr tveimur pöntunum fyrir viðskiptavin *US-004* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.
- Línur úr sölupöntun 4-5 og 4-6 fyrir viðskiptavin *US-007* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.
- Línur úr sölupöntun 4-7 og 4-8 fyrir viðskiptavin *US-007* voru settar saman í sendingu með því að nota *CrossOrder* úr samstæðureglu sendingar.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir samstæðureglur sendingar](about-shipment-consolidation-policies.md)
- [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]