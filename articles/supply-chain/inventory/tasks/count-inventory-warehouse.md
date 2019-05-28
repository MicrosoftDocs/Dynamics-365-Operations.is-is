---
title: Telja birgðir í vöruhúsi
description: Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun birgðatalningabók til að telja tiltekinnar vöru á staðsetningu í vöruhúsinu.
author: MarkusFogelberg
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalCount, InventJournalCreate, HcmWorkerLookUp, InventItemIdLookupSimple, InventLocationIdLookup, WMSLocationIdLookup, InventTrans
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8c0bbfe8f86d27f81b0d577ed89dfa34ebcf3f18
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549906"
---
# <a name="count-inventory-in-a-warehouse"></a>Telja birgðir í vöruhúsi

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli fer í gegnum ferlið fyrir stofnun og bókun birgðatalningabók til að telja tiltekinnar vöru á staðsetningu í vöruhúsinu. Ferlið á við "grunn vöruhús" aðgerðir, sem tiltækar eru í kerfinu birgðastjórnun, ekki á vöruhúsaaðgerð sem tiltæk er í kerfiseiningunni vöruhúsakerfi. Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn. Ef verið er að nota eigin gögn, tryggja þarf afurðir og staðsetningar eru uppsettar og að hefur verið stofnað heiti birgðabókar fyrir talningarbækur. Birgðatalning er yfirleitt framkvæmd af starfsmanni í vöruhúsi.


## <a name="create-an-inventory-counting-journal"></a>Stofna færslubóka fyrir birgðatalningu
1. Fara í Birgðastjórnun > Færslubókarfærslur > Vörutalning > Talning.
2. Smellið á „Nýtt“.
3. Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.
4. Á listanum, smella á að nota nafn birgðatalningabókar
    * Sum svæði er fyllt út samkvæmt uppsetningu heitis birgðatalningabókar sem er valin.  
5. Í reitnum starfskraftur skal smella á fellilistahnappinn til að opna leitina.
6. Veljið starfsmanninn sem á að nota í listanum.
7. Smellið á Velja.
8. Smellið á „Í lagi“.

## <a name="create-journal-lines"></a>Stofna færslubókarlínur
1. Smellið á „Nýtt“.
2. Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Ef verið er að nota sýnigögn fyrirtækisins USMF velja 'A0001'.  
4. Í reitnum svæði skal smella á fellilistahnappinn til að opna leitina.
5. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Ef verið er að nota sýnigögn fyrirtækisins USMF, veljið svæði '2'.  
6. Í reitnum vöruhús skal smella á fellilistahnappinn til að opna leitina.
7. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Ef verið er að nota sýnigögn fyrirtækisins USMF, skal velja vöruhúsið '24'.  
8. Í reitnum staðsetning skal smella á fellilistahnappinn til að opna leitina.
9. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Ef verið er að nota sýnigögn fyrirtækisins USMF, velja staðsetningu ‚BULK-001'  
10. Í reitinn Talið skal slá inn númer.
    * Ef fært er inn talið númer sem er annað númer en er sýnd í svæðinu á lager, er magnsvæðið uppfærð til að sýna misræmið.  
11. Smellið á „Vista“.

## <a name="post-the-inventory-counting-journal"></a>Bóka færslubók fyrir birgðatalningu
1. Smellið á „Bóka“.
    * Þegar bókað er birgðatalningabók, ef talin upphæð er önnur en upphæð sem skráð er í svæðinu á lager er innhreyfing eða úthreyfing birgða bókuð, birgðastigi og birgðagildi breytt og fjárhagsfærslur stofnaðar.  
2. Smellið á „Í lagi“.

## <a name="view-inventory-transactions"></a>Skoða birgðafærslur
1. Smellið á birgðir.
2. Smella á Færslur.
    * Hér er hægt að sjá tengdar færslur sem stofnast þegar talningarbók birgða er bókuð.   

