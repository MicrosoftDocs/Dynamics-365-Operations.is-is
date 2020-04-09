---
title: Samþætt vinna með lánardrottinssniðmát
description: Þetta efni lýsir samþættingu lánardrottnagagna milli forrita Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 8d531ed4e46d8ee5d2b0937b6efc480e051fe708
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3173109"
---
# <a name="integrated-vendor-master"></a>Samþætt lánardrottinssniðmát

[!include [banner](../../includes/banner.md)]



Hugtakið *lánardrottinn* vísar til fyrirtækis birgja eða í einkaeigu sem veitir fyrirtæki eða þjónustu vöru eða þjónustu. Þó að *Lánardrottinn* sé rótgróið hugtak í Microsoft Dynamics 365 Supply Chain Management er ekkert lánadrottinshugtakið til í líkanadrifnum forritum í Dynamics 365. Hins vegar geturðu ofhlaðið eininguna **Lykill/tengiliður** til að geyma lánardrottnaupplýsingar. Samþætt lánardrottinssniðmát kynnir skýrt lánardrottnahugtak í líkanadrifnum forritum í Dynamics 365. Þú getur annaðhvort notað nýju lánardrottnahönnunina eða geymt lánardrottnagögn í einingunni **Lykill/tengiliður**. Tvöföld skrifa styður báðar leiðir.

Í báðum aðferðum eru gögn lánardrottins samþætt á milli gátta Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service og Power Apps. Í Supply Chain Management eru gögnin tiltæk fyrir verkflæði eins og innkaupabeiðnir og innkaupapantanir.

## <a name="vendor-data-flow"></a>Gagnaflæði lánardrottins

Ef þú vilt ekki geyma lánardrottnagögn í einingunni **Lykill/tengiliður** í Common Data Service geturðu notað nýju lánardrottnahönnunina.

![Gagnaflæði lánardrottins](media/dual-write-vendor-data-flow.png)

Ef þú vilt halda áfram að geyma lánardrottnagögn í einingunni **Lykill/tengiliður** geturðu notað auknu lánardrottnahönnunina. Til að nota aukna lánardrottnahönnun verður þú að stilla verkflæði lánardrottins í tvískiptu lausnarpakkanum. Fyrir frekari upplýsingar, sjá [Skipta á milli lánardrottnahönnunar](vendor-switch.md).

![Útvíkkað gagnaflæði lánardrottins](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Ef þú ert að nota Power Apps-gáttir fyrir lánardrottna með sjálfsafgreiðslu geta lánardrottnaupplýsingar streymt beint í forrit Finance and Operations.

## <a name="templates"></a>Sniðmát

Lánardrottnagögn innihalda allar upplýsingar um lánardrottinn, svo sem lánardrottnahópinn, heimilisföng, tengiliðaupplýsingar, greiðslusnið og reikningssnið. Safn af einingakortum virka saman á meðan samskipti við lánardrottna eru í gangi, eins og sýnt er í eftirfarandi töflu.

Finance and Operations-smáforrit | Önnur Dynamics 365 forrit     | Lýsing
----------------------------|-----------------------------|------------
Lánardrottinn V2                   | Reikningur                     | Fyrirtæki sem nota lyklaeininguna til að geyma upplýsingar um lánardrottna geta haldið áfram að nota hana á sama hátt. Þau geta einnig nýtt sér yfirlýsta virkni lánardrottins sem kemur vegna samþættingar forrita Finance and Operations.
Lánardrottinn V2                   | Msdyn\_vendors              | Fyrirtæki sem nota sérsniðna lausn fyrir lánardrottna geta nýtt sér hugtakið tilbúinn lánardrottinn sem er kynntur til sögunnar í Common Data Service vegna samþættingar forrita Finance and Operations. 
Lánardrottnaflokkar               | msdyn\_vendorgroups         | Þetta sniðmát samstillir upplýsingar um hóp lánardrottna.
Greiðsluháttur lánardrottins       | msdyn\_vendorpaymentmethods | Þetta sniðmát samstillir upplýsingar um greiðslumáta lánardrottna.
Tengiliðir fyrir skuldatryggingu V2             | tengiliðir                    | [Tengiliða](customer-mapping.md#cds-contacts-v2-to-contacts)-sniðmátið samstillir allar aðal-, aðrar og þriðju tengiliðaupplýsingar, bæði fyrir viðskiptavini og framleiðendur.
Greiðsluáætlunarlínur      | msdyn\_paymentschedulelines | [Greiðsluáætlunarlínu](customer-mapping.md#payment-schedule-lines-to-msdyn_paymentschedulelines)-sniðmátið samstillir tilvísunargögn greiðsluáætlunar, bæði fyrir viðskiptavini og lánardrottna.
Greiðsluáætlun            | msdyn\_paymentschedules     | [Greiðsluáætlana](customer-mapping.md#payment-schedule-to-msdyn_paymentschedules)-sniðmátið samstillir tilvísunargögn greiðsluáætlunar, bæði fyrir viðskiptavini og lánardrottna.
Greiðsludagalínur CDS V2    | msdyn\_paymentdaylines      | [Greiðsludagalínu](customer-mapping.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines)-sniðmátið samstillir tilvísunargögn greiðsludagalína fyrir viðskiptavini og lánardrottna.
Greiðsludagar CDS            | msdyn\_paymentdays          | [Greiðsludagar](customer-mapping.md#payment-days-cds-to-msdyn_paymentdays)-sniðmátið samstillir tilvísunargögn greiðsludaga, bæði fyrir viðskiptavini og lánardrottna.
Greiðsluskilmálar            | msdyn\_paymentterms         | [Greiðsluskilmála](customer-mapping.md#terms-of-payment-to-msdyn_paymentterms)-sniðmátið samstillir tilvísunargögn greiðsluskilmála (skilmála greiðslu), bæði fyrir viðskiptavini og lánardrottna.
Viðskeyti nafna                | msdyn\_nameaffixes          | [Heitisviðskeytis](customer-mapping.md#name-affixes-to-msdyn_nameaffixes)-sniðmátið samstillir tilvísunargögn nafnaviðskeyta, bæði fyrir viðskiptavini og lánardrottna.

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [Vendors](includes/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](includes/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](includes/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
