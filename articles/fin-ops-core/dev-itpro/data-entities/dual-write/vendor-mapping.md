---
title: Samþætt lánardrottinssniðmát
description: Þessi grein lýsir samþættingu söluaðilagagna milli fjármála- og rekstrarforrita og Dataverse.
author: RamaKrishnamoorthy
ms.date: 07/15/2019
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: a2c32ef546a5bc74e090591c0ac9d51529299041
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/02/2022
ms.locfileid: "9112197"
---
# <a name="integrated-vendor-master"></a>Samþætt lánardrottinssniðmát

[!include [banner](../../includes/banner.md)]



Hugtakið *lánardrottinn* vísar til fyrirtækis birgja eða í einkaeigu sem veitir fyrirtæki eða þjónustu vöru eða þjónustu. Þó að *lánardrottinn* sé rótgróið hugtak í Microsoft Dynamics 365 Supply Chain Management er ekkert lánadrottnahugtak til í forritum viðskiptavinar. Hins vegar er hægt að ofhlaða töfluna **Lykill/tengiliður** til að geyma lánardrottnaupplýsingar. Samþætt lánardrottnasniðmát kynnir skýrt lánardrottnahugtak í forritum viðskiptavina. Annaðhvort er hægt að nota nýju lánardrottnahönnunina eða geyma lánardrottnagögn í töflunni **Lykill/tengiliður**. Tvöföld skrifa styður báðar leiðir.

Í báðum aðferðum eru gögn lánardrottins samþætt á milli gátta Dynamics 365 Supply Chain Management, Dynamics 365 Sales, Dynamics 365 Field Service og Power Apps. Í Supply Chain Management eru gögnin tiltæk fyrir verkflæði eins og innkaupabeiðnir og innkaupapantanir.

## <a name="vendor-data-flow"></a>Gagnaflæði lánardrottins

Ef ekki á að geyma lánardrottnagögn í tölfunni **Lykill/tengiliður** í Dataverse geturðu notað nýju lánardrottnahönnunina.

![Gagnaflæði lánardrottins.](media/dual-write-vendor-data-flow.png)

Ef halda á áfram að geyma lánardrottnagögn í töflunni **Lykill/tengiliður** geturðu notað auknu lánardrottnahönnunina. Til að nota aukna lánardrottnahönnun verður þú að stilla verkflæði lánardrottins í tvískiptu lausnarpakkanum. Fyrir frekari upplýsingar, sjá [Skipta á milli lánardrottnahönnunar](vendor-switch.md).

![Útvíkkað gagnaflæði lánardrottins.](media/dual-write-vendor-detail.jpg)

> [!TIP]
> Ef þú ert að nota Power Apps gáttir fyrir sjálfsafgreiðsluseljendur, geta upplýsingar um söluaðila streymt beint í fjármála- og rekstraröpp.

## <a name="templates"></a>Sniðmát

Lánardrottnagögn innihalda allar upplýsingar um lánardrottinn, svo sem lánardrottnahópinn, heimilisföng, tengiliðaupplýsingar, greiðslusnið og reikningssnið. Safn af töflukortum vinna saman í gagnasamskiptum lánardrottins, eins og sýnt er í eftirfarandi töflu.

Forrit fyrir Finance and Operations | Forrit viðskiptavinatengsla     | lýsing
----------------------------|-----------------------------|------------
[Tengiliðir fyrir skuldatryggingu V2](mapping-reference.md#115) | tengiliðir | Þetta sniðmát samstillir allar aðal-, aðrar og þriðju tengiliðaupplýsingar, bæði fyrir viðskiptavini og framleiðendur.
[Viðskeyti nafna](mapping-reference.md#155) | msdyn_nameaffixes | Þetta sniðmát samstillir tilvísunargögn nafnaviðskeyta, bæði fyrir viðskiptavini og lánardrottna.
[Greiðsludagalínur CDS V2](mapping-reference.md#157) | msdyn_paymentdaylines | Þetta sniðmát samstillir tilvísunargögn greiðsludagalína, bæði fyrir viðskiptavini og lánardrottna.
[Greiðsludagar CDS](mapping-reference.md#158) | msdyn_paymentdays | Þetta sniðmát samstillir tilvísunargögn greiðsludaga, bæði fyrir viðskiptavini og lánardrottna.
[Greiðsluáætlunarlínur](mapping-reference.md#159) | msdyn_paymentschedulelines | Samstillir tilvísunargögn greiðsluáætlunarlína, bæði fyrir viðskiptavini og lánardrottna.
[Greiðsluáætlun](mapping-reference.md#160) | msdyn_paymentschedules | Þetta sniðmát samstillir tilvísunargögn greiðsluáætlunar, bæði fyrir viðskiptavini og lánardrottna.
[Greiðsluskilmálar](mapping-reference.md#161) | msdyn_paymentterms | Þetta sniðmát samstillir tilvísunargögn greiðsluskilmála (skilmála greiðslu), bæði fyrir viðskiptavini og lánardrottna.
[Lánardrottnar V2](mapping-reference.md#202) | msdyn_vendors | Fyrirtæki sem nota sérsniðna lausn fyrir söluaðila geta nýtt sér hugmyndina um söluaðila sem er út úr kassanum sem verið er að kynna í Dataverse vegna samþættingar fjármála- og rekstrarforrita.
[Lánardrottnaflokkar](mapping-reference.md#200) | msdyn_vendorgroups | Þetta sniðmát samstillir upplýsingar um hóp lánardrottna.
[Greiðsluháttur lánardrottins](mapping-reference.md#201) | msdyn_vendorpaymentmethods | Þetta sniðmát samstillir upplýsingar um greiðslumáta lánardrottna.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

