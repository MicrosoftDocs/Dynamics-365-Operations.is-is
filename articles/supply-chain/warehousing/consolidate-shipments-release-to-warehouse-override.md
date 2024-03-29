---
title: Sameina sendingar þegar samstæðureglu sendingar hefur verið hnekkt
description: Þessi grein sýnir aðstæður þar sem losa þarf handvirkt eina eða fleiri sölulínur í vöruhúsið af síðunni Losa í vöruhús og hnekkja þarf kerfisskilgreindri samstæðureglu sendingar áður en hún er losuð.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: e2c4fed880c423790b979f27511d8d5697bd244c
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/08/2022
ms.locfileid: "9427956"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden"></a>Sameina sendingar þegar samstæðureglu sendingar hefur verið hnekkt

[!include [banner](../includes/banner.md)]

Þessi grein sýnir aðstæður þar sem losa þarf handvirkt eina eða fleiri sölulínur í vöruhúsið af síðunni **Losa í vöruhús** og hnekkja þarf kerfisskilgreindri samstæðureglu sendingar áður en hún er losuð. Hugsanlega þarf að hnekkja samstæðureglu sendingar, t.d. ef sameina þarf pöntun sem er ekki vanalega sameinuð með opnum sendingum við opnar sendingar.

Við aðstæðurnar er stofnarðu sölupantanir og hnekkir svo sjálfgefinni samstæðureglu sendingar áður en pöntunum er sleppt í vöruhúsið.

## <a name="make-demo-data-available"></a>Bjóða upp á sýnigögn

Aðstæður í þessari grein vísa í gildi og færslur sem eru innifaldar í stöðluðum sýnigögnum fyrir Microsoft Dynamics 365 Supply Chain Management. Ef nota á gildin sem er boðið upp á hér eins og í æfingunum skal gæta þess að vinna í umhverfi þar sem sýnigögnin eru uppsett og stilla lögaðilann á **USMF** áður en hafist er handa.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Setja upp samstæðureglur sendingar og afurðarsíur

Aðstæðurnar sem hér er lýst gera ráð fyrir að þegar hafi verið kveikt á eiginleikanum, farið hafi verið í gegnum æfingarnar í [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md) og reglur og aðrar færslur sem þar er lýst stofnaðar. Gætið þess að gera þessar æfingar áður en haldið er áfram með þessar aðstæður.

## <a name="create-the-sales-orders-for-this-scenario"></a>Búa til sölupantanir fyrir þessar aðstæður

1. Opnaðu **Viðskiptakröfur \> Pantanir \> Allar sölupantanir** og búðu til þrjár eins sölupantanir með eftirfarandi stillingum:

    - **Viðskiptavinalykill:** *US-002*

1. Bættu við pöntunarlínu sem er með eftirfarandi stillingar:

    - **Vörunúmer:** *A0001* (vara sem engin sía fyrir **kóða 4** er úthlutað á)
    - **Magn:** *1.00*

1. Veljið **Birgðir \> Frátekning** og síðan, á aðgerðasvæðinu, veljið **Frátektarlota** til að taka frá pöntunarlínu.

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a>Losa sölupantanir af síðunni Losa í vöruhús

Fylgið eftirfarandi skrefum til að hnekkja samstæðureglu sendingar við losun í vöruhúsið.

1. Opnaðu **Vöruhúsakerfi \> Losa í vöruhús \> Losa í vöruhús**.
1. Í efri rúðu skal velja fyrstu sölupöntunina sem var stofnuð fyrir þessar aðstæður.
1. Veljið **Bæta við** til að bæta línunni við losun í vöruhúsið. Takið eftir að *Sjálfgefið* samstæðureglu sendingar er beitt í neðstu rúðu.
1. Á neðsta svæðinu skal velja **Velja nýja samstæðureglu sendingar**.
1. Veljið reglu sem leyfir samstæðu við aðrar opnar sendingar sömu reglu. Veljið til dæmis regluna *CustomerOrderNo*.
1. Velja **Losa í vöruhús**.
1. Velja skal aðra og þriðju sölupöntun sem voru stofnaðar fyrir þessar aðstæður.
1. Veljið **Bæta við** til að bæta línunum við losunina í vöruhúsið. Takið eftir að *Sjálfgefið* reglunni er beitt í neðstu rúðu.
1. Velja skal aðra línuna og síðan, í **Velja nýja samstæðureglu sendingar**, velja *CustomerOrderNo* regluna.
1. Veljið **Losa í vöruhús** fyrir báðar línurnar.

## <a name="verify-the-shipments"></a>Staðfesta skal sendingarnar

Tvær sendingar ættu að hafa verið stofnaðar:

- Fyrsta sendingin inniheldur tvær línur og var búin til með því að nota samstæðureglu sendingar *CustomerOrderNo*.
- Önnur sendingin inniheldur eina línu og var búin til með því að nota samstæðuregluna *Sjálfgefið*.

Fylgdu þessum skrefum til að yfirfara sendingar sem voru stofnaðar.

1. Opnið **Vöruhúsakerfi \> Sendingar \> Allar sendingar**.
1. Finnið og veljið þá sendingu sem um ræðir.
1. Í svæðið **Samstæðuregla sendingar** skal fara yfir samstæðuregluna sem var notuð þegar sendingin var stofnuð.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Yfirlit yfir samstæðureglur sendingar](about-shipment-consolidation-policies.md)
- [Skilgreina samstæðureglur sendingar](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]