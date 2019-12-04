---
title: Samþættur aðallánardrottinn
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
ms.openlocfilehash: da451c63c23444da564307505d38699faf9df19a
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770987"
---
# <a name="integrated-vendor-master"></a>Samþættur aðallánardrottinn

[!include [banner](../includes/banner.md)]

Hugtakið *Lánardrottinn* á við birgðasamtök eða einkaeigu sem er hluti af aðfangakeðjuferlinu og veitir vörur fyrir fyrirtækið. Þó að *Lánardrottinn* sé rótgróið hugtak í forritum Finance and Operations er hugtakið lánardrottinn ekki til í öðrum forritum Dynamics 365. Þess í stað, yfirhlaða sum fyrirtæki lykileininguna til að geyma bæði viðskiptavinaupplýsingar og upplýsingar um lánardrottna. Önnur fyrirtæki nota sérsniðið lánardrottinshugtak. Common Data Service samþætting styður bæði þessa hönnun. Þess vegna geturðu virkjað aðra hvora hönnunina, allt eftir aðstæðum fyrirtækisins.

Sameining gagna lánardrottins milli forrita Finance and Operations og annarra forrita Dynamics 365 gerir þér kleift að ná góðum tökum á gögnunum. Óháð því hvaðan lánardrottnagögnin eru upprunnin, þá eru þau samþætt bak við tjöldin þvert á forritamörk og mismun á innviðum. 

### <a name="vendor-data-flow"></a>Gagnaflæði lánardrottins

Ef þú vilt nota önnur forrit Dynamics 365 við stjórnun lánardrottins og þú vilt einangra upplýsingar seljanda frá upplýsingum viðskiptavinarins, geturðu notað nýja lánardrottinshönnunina.

![Gagnaflæði lánardrottins](media/dual-write-vendor-data-flow.png)

Ef þú vilt nota önnur forrit Dynamics 365 við stjórnun lánardrottins og þú vilt halda áfram að nota lyklaeininguna til að geyma upplýsingar lánardrottins geturðu notað nýju útvíkkuðu lánardrottinshönnunina. Í þessari hönnun eru útvíkkaðar upplýsingar um lánardrottinn, svo sem lánardrottnahópinn og bókunarforstillingar lánardrottins, geymdar í smáatriðum lánardrottins.

![Útvíkkað gagnaflæði lánardrottins](media/dual-write-vendor-detail.jpg)

Tengiliðsupplýsingar lánardrottins líkjast tengiliðsupplýsingum viðskiptavina. Bak við tjöldin eru upplýsingar tengiliðar vistaðar og sóttar frá sömu einingum.

## <a name="templates"></a>Sniðmát

Lánardrottnagögn innihalda allar upplýsingar um lánardrottinn, svo sem lánardrottnahópinn, heimilisföng, tengiliðaupplýsingar, greiðslusnið og reikningssnið. Safn af einingakortum virka saman á meðan samskipti við lánardrottna eru í gangi, eins og sýnt er í eftirfarandi töflu.

Forrit Finance and Operations | Önnur Dynamics 365 forrit         | Lýsing
----------------------------|---------------------------------|------------
Lánardrottinn V2               | Reikningur | Fyrirtæki sem nota lyklaeininguna til að geyma upplýsingar um lánardrottna geta haldið áfram að nota hana á sama hátt. Þau geta einnig nýtt sér yfirlýsta virkni lánardrottins sem kemur vegna samþættingar forrita Finance and Operations.
Lánardrottinn V2               | Msdyn\_vendors | Fyrirtæki sem nota sérsniðna lausn fyrir lánardrottna geta nýtt sér hugtakið tilbúinn lánardrottinn sem er kynntur til sögunnar í Common Data Service vegna samþættingar forrita Finance and Operations. 
Lánardrottnaflokkar | msdyn_vendorgroups | Þetta sniðmát samstillir upplýsingar um hóp lánardrottna.
Greiðsluháttur lánardrottins | msdyn_vendorpaymentmethods | Þetta sniðmát samstillir upplýsingar um greiðslumáta lánardrottna.
Tengiliðir fyrir skuldatryggingu V2             | tengiliðir                        | [Tengiliða](dual-write-customer.md#cds-contacts-v2-to-contacts)-sniðmátið samstillir allar aðal-, aðrar og þriðju tengiliðaupplýsingar, bæði fyrir viðskiptavini og framleiðendur.
Greiðsluáætlunarlínur      | msdyn_paymentschedulelines      | [Greiðsluáætlunarlínu](dual-write-customer.md#payment-schedule-lines-to-msdyn_paymentschedulelines)-sniðmátið samstillir tilvísunargögn greiðsluáætlunar, bæði fyrir viðskiptavini og lánardrottna.
Greiðsluáætlun            | msdyn_paymentschedules          | [Greiðsluáætlana](dual-write-customer.md#payment-schedule-to-msdyn_paymentschedules)-sniðmátið samstillir tilvísunargögn greiðsluáætlunar, bæði fyrir viðskiptavini og lánardrottna.
Greiðsludagalínur CDS V2    | msdyn_paymentdaylines           | [Greiðsludagalínu](dual-write-customer.md#payment-day-lines-cds-v2-to-msdyn_paymentdaylines)-sniðmátið samstillir tilvísunargögn greiðsludagalína fyrir viðskiptavini og lánardrottna.
Greiðsludagar CDS            | msdyn_paymentdays               | [Greiðsludagar](dual-write-customer.md#payment-days-cds-to-msdyn_paymentdays)-sniðmátið samstillir tilvísunargögn greiðsludaga, bæði fyrir viðskiptavini og lánardrottna.
Greiðsluskilmálar            | msdyn_paymentterms              | [Greiðsluskilmála](dual-write-customer.md#terms-of-payment-to-msdyn_paymentterms)-sniðmátið samstillir tilvísunargögn greiðsluskilmála (skilmála greiðslu), bæði fyrir viðskiptavini og lánardrottna.
Viðskeyti nafna                | msdyn_nameaffixes               | [Heitisviðskeytis](dual-write-customer.md#name-affixes-to-msdyn_nameaffixes)-sniðmátið samstillir tilvísunargögn nafnaviðskeyta, bæði fyrir viðskiptavini og lánardrottna.

[!include [symbols](../includes/dual-write-symbols.md)]

[!include [Vendors](dual-write/VendorsV2-msdyn-vendors.md)]

[!include [Vendor groups](dual-write/VendVendorGroup-msdyn-vendorgroups.md)]

[!include [Vendor payment methods](dual-write/VendorPaymentMethod-msdyn-vendorpaymentmethods.md)]
