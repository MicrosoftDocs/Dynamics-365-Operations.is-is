---
title: Telja birgðir í vöruhúsi
description: Þetta efni lýsir ferlinu við stofnun og bókun birgðatalningabók til að telja tiltekna vöru á staðsetningu í vöruhúsinu.
author: MarkusFogelberg
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 452822eaf26c26e4c9e00f909dbd18127f6fc781
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230105"
---
# <a name="count-inventory-in-a-warehouse"></a>Telja birgðir í vöruhúsi

[!include [banner](../../includes/banner.md)]

Þetta efni lýsir ferlinu við stofnun og bókun birgðatalningabók til að telja tiltekna vöru á staðsetningu í vöruhúsinu. Ferlið á við virkni „grunnvöruhúss”, sem er tiltækt í birgðastjórnunareiningunni, ekki við vöruhúsavirknina sem er tiltæk í kerfiseiningunni vöruhúsakerfi. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn. Ef verið er að nota eigin gögn, tryggja þarf afurðir og staðsetningar eru uppsettar og að hefur verið stofnað heiti birgðabókar fyrir talningarbækur. Birgðatalning er yfirleitt framkvæmd af starfsmanni í vöruhúsi.


## <a name="create-an-inventory-counting-journal"></a>Stofna færslubóka fyrir birgðatalningu
1. Farðu í **Skoðunarrúða > Kerfi > Birgðastjórnun > Bókarfærslur > Vörutalning > Talning**.
2. Veljið **Nýtt**.
3. Í reitnum **Heiti** skaltu velja það dagbókarheiti birgðatalningar sem þú vilt nota af fellivalmyndinni. Sum svæði er fyllt út samkvæmt uppsetningu heitis birgðatalningabókar sem er valin.  
4. Í reitnum **Starfskraftur** skaltu smella á fellilistahnappinn til að opna leitina.
5. Í listanum skaltu **Velja** starfskraftinn sem þú vilt nota.
6. Veljið **Í lagi**.

## <a name="create-journal-lines"></a>Stofna færslubókarlínur
1. Veljið **Nýtt**.
2. Í reitnum **Vörunúmer** velurðu skrána sem óskað er eftir af fellilistanum. Ef verið er að nota sýnigögn fyrirtækisins USMF velja **A0001**.  
3. Í reitnum **Svæði** velurðu skrána sem óskað er eftir af fellilistanum. Ef verið er að nota sýnigögn fyrirtækisins USMF, veljið svæði **2**.
4. Í reitnum **Vöruhús** velurðu skrána sem óskað er eftir af fellilistanum. Ef verið er að nota sýnigögn fyrirtækisins USMF, skal velja vöruhúsið **24**.  
5. Í reitnum **Staðsetning** velurðu skrána sem óskað er eftir af fellilistanum. Ef verið er að nota sýnigögn fyrirtækisins USMF, velja staðsetningu **BULK-001**.  
6. Í reitinn Talið skal slá inn númer. Ef fært er inn talið númer sem er annað númer en er sýnt í reitnum **Á lager**, er reiturinn **Magn** uppfærður til að sýna misræmið.  
7. Veljið **Vista**.

## <a name="post-the-inventory-counting-journal"></a>Bóka færslubók fyrir birgðatalningu
1. Veldu **Bóka**. Þegar birgðatalningabók er bókuð, ef talin upphæð er önnur en upphæð sem skráð er í reitnum **Á lager** er innhreyfing eða úthreyfing birgða bókuð, birgðastigi og birgðagildi breytt og fjárhagsfærslur stofnaðar.
2. Veljið **Í lagi**.

## <a name="view-inventory-transactions"></a>Skoða birgðafærslur
1. Veldu **Birgðir**.
2. Veldu **Færslur**. Hér er hægt að sjá tengdar færslur sem stofnast þegar talningarbók birgða er bókuð.   



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]