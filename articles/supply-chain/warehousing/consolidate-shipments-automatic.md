---
title: Sameina sendingar þegar þær eru losaðar í vöruhús með því að nota sjálfvirka losun sölupantana
description: Þetta efnisatriði sýnir aðstæður þar sem margar pantanir eru losaðar í vöruhúsið í sama sjálfvirka ferli vöruhúsakerfis.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 74d4d9d8429095c3fac80db58f14ac2ef0776798
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/03/2022
ms.locfileid: "8677535"
---
# <a name="consolidate-shipments-released-to-the-warehouse-using-automatic-release-of-sales-orders"></a>Sameina sendingar þegar þær eru losaðar í vöruhús með því að nota sjálfvirka losun sölupantana

[!include [banner](../includes/banner.md)]

Þetta efnisatriði sýnir aðstæður þar sem margar pantanir eru losaðar í vöruhúsið í sama sjálfvirka ferli vöruhúsakerfis. Pantanirnar verða sameinaðar sjálfkrafa í sendingar, samkvæmt reglum sem eru skilgreindar sem samstæðureglur sendingar.

Meðan á atburðarásinni stendur verða söfn sölupantana stofnuð og hvert safn losað til vöruhússins. Þú munt síðan yfirfara sendingar sem eru stofnaðar eða uppfærðar meðan á sendingarsamstæðu stendur, með hliðsjón af skilgreindum stefnum.

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

#### <a name="sales-order-1-2"></a>Sölupöntun 1-2

1. Stofna sölupöntun sem er með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-001*
    - **Afhendingarmáti:** *Airwa-Air*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

#### <a name="sales-order-1-3"></a>Sölupöntun 1-3

1. Stofna sölupöntun sem er með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-001*
    - **Afhendingarmáti:** *10*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

1. Bæta við annarri pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0002* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*
    - **Afhendingarmáti:** *Airwa-Air*

### <a name="create-order-set-2"></a>Búa til pöntunarsett 2

#### <a name="sales-orders-2-1-and-2-2"></a>Sölupantanir 2-1 og 2-2

1. Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-002*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *M9200* (vara þar sem sía fyrir **kóða 4** er stillt á *eldfimt*)
    - **Magn:** *1.00*

1. Bæta við annarri pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *M9201* (vara þar sem sía fyrir **kóða 4** er stillt á *sprengifimt*)
    - **Magn:** *1.00*
    - **Afhendingarmáti:** *Airwa-Air*

### <a name="create-order-set-3"></a>Búa til pöntunarsett 3

#### <a name="sales-order-3-1"></a>Sölupöntun 3-1

1. Stofna sölupöntun sem er með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-002*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *M9200* (vara þar sem sía fyrir **kóða 4** er stillt á *eldfimt*)
    - **Magn:** *1.00*

1. Bæta við annarri pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *M9201* (vara þar sem sía fyrir **kóða 4** er stillt á *sprengifimt*)
    - **Magn:** *1.00*
    - **Afhendingarmáti:** *Airwa-Air*

> [!NOTE]
> Þessi pöntun er eins og pantanirnar tvær sem voru stofnaðar fyrir pantanasett 2. Það er hins vegar skráð sem eigin pantanasett vegna þess að það verður gefið út sérstaklega síðar í þessari atburðarás.

### <a name="create-order-set-4"></a>Búa til pöntunarsett 4

#### <a name="sales-order-4-1"></a>Sölupöntun 4-1

1. Stofna sölupöntun sem er með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-001*
    - **Innkaupabeiðni viðskiptavinar:** *1*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

### <a name="create-order-set-5"></a>Búa til pöntunarsett 5

#### <a name="sales-orders-5-1-and-5-2"></a>Sölupantanir 5-1 og 5-2

1. Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-001*
    - **Innkaupabeiðni viðskiptavinar:** *2*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

#### <a name="sales-order-5-3"></a>Sölupöntun 5-3

1. Stofna sölupöntun sem er með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-001*
    - **Innkaupabeiðni viðskiptavinar:** *1*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

### <a name="create-order-set-6"></a>Búa til pöntunarsett 6

#### <a name="sales-orders-6-1-and-6-2"></a>Sölupantanir 6-1 og 6-2

1. Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-003*
    - **Innkaupabeiðni viðskiptavinar:** *2*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

#### <a name="sales-orders-6-3-and-6-4"></a>Sölupantanir 6-3 og 6-4

1. Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-004*
    - **Innkaupabeiðni viðskiptavinar:** *1*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

#### <a name="sales-orders-6-5-and-6-6"></a>Sölupantanir 6-5 og 6-6

1. Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-007*
    - **Svæði:** *6*
    - **Vöruhús:** *61*
    - **Hópur:** *ShipCons*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

#### <a name="sales-orders-6-7-and-6-8"></a>Sölupantanir 6-7 og 6-8

1. Stofnaðu tvær eins sölupantanirnar sem eru með eftirfarandi stillingar:

    - **Viðskiptavinalykill:** *US-007*
    - **Svæði:** *6*
    - **Vöruhús:** *61*
    - **Hópur:** – Hafa þennan reit auðan.

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a>Sjálfvirk losun á sölupöntunum í vöruhúsið

Fyrir hvert safn af sölupöntunum sem voru stofnaðar áður skal ljúka ferli fyrir sjálfvirka losun í vöruhúsið. Í hverju tilviki verður unnið í gegnum [grunnlosunarferli í vöruhús](#release-procedure) sem er gefið upp hér.

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a>Grunnlosunarferli í vöruhús

Fyrir hvert safn af sölupöntunum sem voru stofnuð áður skal ljúka við ferlin þrjú sem er sagt frá í eftirfarandi undirköflum.

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a>Uppfæra bylgjusniðmátið sem verður notað við losun

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Bylgjur \> Bylgjusniðmát**.
1. Stillið svæðið **gerð bylgjusniðmáts** á *afhendingu*.
1. Finnið og veljið bylgjusniðmátið sem tengist vöruhúsinu sem var notað í pöntunarsettunum sem voru stofnuð fyrir þessa atburðarás. Til dæmis, ef notað er vöruhús *24*, skal velja bylgjusniðmátið **sjálfgefin afhending 24**. Ef notað var vöruhús *61* skal velja bylgjusniðmátið **afhending 61.**
1. Á aðgerðarúðunni skal velja **Breyta**.
1. Stilla valkostinn fyrir **Vinna úr bylgju við losun í vörugeymslu** á *Nei*.

#### <a name="release-to-the-warehouse"></a>Losa í vöruhús

1. Farið í **Vöruhúsakerfi \> Losa í vöruhús \> Sjálfvirk losun sölupantana**.
1. Stillið svæðið **Magn til að losa** á *Allt*.
1. Á flýtiflipanum **Færslur til að taka með** skal velja **Sía** til að opna svargluggann „fyrirspurn“.
1. Veldu **Bæta við** til að bæta við röð á flipanum **Svið** til að bæta við línu sem er með eftirfarandi stillingar á hnitanetinu:

    - **tafla:** *Sölupöntun*
    - **Afleidd tafla:** *Sölupöntun*
    - **Svæði:** *Sölupöntun*
    - **Skilyrði:** Færa skal inn kommuaðgreinda lista yfir sölupöntunarnúmer úr æskilegu pantanamengi.

1. Veljið **Í lagi** til að vista fyrirspurnina.
1. Veljið **Í lagi** til að ræsa ferlið *Sjálfvirk losun í vöruhús*.

#### <a name="review-the-shipment-that-is-created-or-updated"></a>Yfirfara sendinguna sem er búin til eða uppfærð

1. Opnið **Vöruhúsakerfi \> Sendingar \> Allar sendingar**.
1. Finnið og veljið þá sendingu sem um ræðir.
1. Ef samstæðuregla var notuð þegar sendingin var stofnuð eða hún var uppfærð ætti hún að koma fram í reitnum **Samstæðuregla sendingar**.

### <a name="release-sales-orders-from-order-set-1"></a>Losa sölupantanir úr pöntunarsetti 1

Farið eftir [Grunnlosunarferli í vöruhús](#release-procedure) til að losa sölupantanir úr pantanasetti 1.

Þegar því er lokið ættirðu að sjá að tvær sendingar voru búnar til:

- Fyrsta sendingin inniheldur þrjár línur og var búin til með því að nota samstæðureglu sendingar *CustomerMode*.
- Önnur sendingin, sem notar ekki flutningsmátann *Flugfélög*, var stofnuð með því að nota samstæðureglu sendingar *CustomerOrderNo*.

### <a name="release-sales-orders-from-order-set-2"></a>Losa sölupantanir úr pöntunarsetti 2

Farið eftir [Grunnlosunarferli í vöruhús](#release-procedure) til að losa sölupantanir úr pantanasetti 2.

Þegar því er lokið ættirðu að sjá að þrjár sendingar voru búnar til:

- Fyrsta sendingin inniheldur vörur sem eru *eldfimar*.
- Hvor hinna sendinganna tveggja inniheldur eina línu með vöru sem er *sprengifim*.

### <a name="release-sales-orders-from-order-set-3"></a>Losa sölupantanir úr pöntunarsetti 3

Farið eftir [Grunnlosunarferli í vöruhús](#release-procedure) til að losa sölupantanir úr pantanasetti 3.

Þegar því er lokið ætti að koma í ljós að eftirfarandi aðgerðir áttu sér stað:

- Ein fyrirliggjandi sending (sendingin sem var stofnuð þegar pöntunarsett 2 var losað í vöruhúsið) var uppfærð. Línu sem er með vöru sem er *eldfim* var bætt við.
- Ein ný sending var búin til sem inniheldur vöruna sem er *sprengifim*.

### <a name="release-sales-orders-from-order-set-4"></a>Losa sölupantanir úr pöntunarsetti 4

Farið eftir [Grunnlosunarferli í vöruhús](#release-procedure) til að losa sölupantanir úr pantanasetti 4.

Þegar því er lokið ætti að koma fram að ein fyrirliggjandi sending (þar sem svæðið **Innkaupabeiðni viðskiptavinar** er stillt á *1*) var uppfærð. Einni nýrri línu var bætt við hana.

### <a name="release-sales-orders-from-order-set-5"></a>Losa sölupantanir úr pöntunarsetti 5

Farið eftir [Grunnlosunarferli í vöruhús](#release-procedure) til að losa sölupantanir úr pantanasetti 5.

Þegar því er lokið ætti að koma í ljós að eftirfarandi aðgerðir áttu sér stað:

- Ein fyrirliggjandi sending (þar sem svæðið **Innkaupabeiðni viðskiptavinar** er stillt á *1*) var uppfærð. Línu úr sölupöntun 5-3 (þar sem reiturinn **Innkaupabeiðni viðskiptavinar** er stilltur á *1*) var bætt við hana.
- Ein ný sending var stofnuð, þar sem línur úr sölupöntunum 5-1 og 5-2 eru flokkaðar í eina sendingu.

### <a name="release-sales-orders-from-order-set-6"></a>Losa sölupantanir úr pöntunarsetti 6

Farið eftir [Grunnlosunarferli í vöruhús](#release-procedure) til að losa sölupantanir úr pantanasetti 6.

Þegar því er lokið ættirðu að sjá að fjórar sendingar voru búnar til:

- Línur úr tveimur pöntunum fyrir viðskiptavin *US-003* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.
- Línur úr tveimur pöntunum fyrir viðskiptavin *US-004* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.
- Línur úr sölupöntun 6-5 og 6-6 fyrir viðskiptavin *US-007* voru settar saman í sendingu með því að nota *Pöntunarsett* úr samstæðureglu sendingar.
- Línur úr sölupöntun 6-7 og 6-8 fyrir viðskiptavin *US-007* voru settar saman í sendingu með því að nota *CrossOrder* úr samstæðureglu sendingar.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Samstæðureglur sendingar](about-shipment-consolidation-policies.md)
- [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]