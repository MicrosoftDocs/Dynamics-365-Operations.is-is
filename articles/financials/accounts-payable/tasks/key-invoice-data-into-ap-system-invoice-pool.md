--- 
title: "Færa reikningsgögn inn í viðskiptaskuldakerfi með reikningasafni"
description: "Þessi leiðarvísi fyrir verk sýnir hvernig á að nota komubók til að stofna reikninga."
author: abruer
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 96040b1c1ba130f773ba0defbf7bf1dcebedfc13
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Færa reikningsgögn inn í viðskiptaskuldakerfi með reikningasafni

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísi fyrir verk sýnir hvernig á að nota komubók til að stofna reikninga.  Nota síðan reikningasafninu til að jafna reikninginn við innkaupapöntun og ljúka kostnað á síðunni reikningur lánardrottins.


## <a name="create-a-purchase-order"></a>Stofna innkaupapöntun
1. Fara í Viðskiptaskuldir > Innkaupapantanir > Innkaupapantanir.
2. Smellið á Nýtt til að stofna innkaupapöntun.
3. Í reitnum lánardrottnalykill skal smella á fellilistahnappinn til að opna leitina.
4. Veljið lánardrottinn úr listanum. Til dæmis lánardrottins 1001.
5. Smellt er á Í lagi.
6. Í reitnum vörunúmer skal smella á fellilistahnappinn til að opna leitina.
7. Finna vörunúmer þjónustu af listanum. Veljið til dæmis S0001.
8. Smellið á vörunúmer og veljið það.
    * Nettóupphæðin er 75,00.  Þetta er Upphæð sem við búumst við á reikningnum.  
9. Í aðgerðasvæðinu er smellt á Innkaup.
10. Smellið á „Staðfesta“.

## <a name="create-and-post-and-invoice"></a>Stofna og bóka og reikningsfæra
1. Fara í Viðskiptaskuldir > Reikningar > Komubók.
2. Smellið á „Nýtt“.
3. Opna uppflettingu til að velja heiti komubókar sem á að nota.
4. Veldu heiti komubókarinnar sem þú vilt nota.
5. Smellið á Línur til að opna afgreiðslukassann og færa inn kostnaðarlínur.
6. Í Uppfletting skal velja lánardrottinn. Til dæmis má smella á lánardrottni 1001.
7. Í reitnum Reikningur færirðu inn númer reiknings.
8. Í reitinn Lýsing skal slá inn gildi.
9. Í reitnum Kredit skal slá inn tölu.
10. Í reitnum innkaupapöntun skal smella á fellilistahnappinn til að opna leitina.
11. Velja innkaupapöntun sem búið var til áður.
12. Í reitnum Samþykkt af skal smella á fellilistahnappinn til að opna leitina.
13. Merkið samþykkjanda og smelltu á Velja til að velja þann samþykkjanda.
14. Smellið á „Bóka“.
15. Lokaðu skjámyndinni.
16. Lokaðu skjámyndinni.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Opna reikning úr safninu og stemma hann við innkaupapöntun til að ljúka reikningsferlinu.
1. Fara í Viðskiptaskuldir > Reikningar > Reikningasafn.
2. Smellt er á innkaupapöntun til að búa til reikning lánardrottins úr reikningi í safninu.
3. Veljið reikninginn sem á að skoða.
4. Smellið á Uppfæra samsvörunarstöðu til að ljúka við samsvörun.
5. Í aðgerðasvæðinu er smellt á valkostir.
6. Smellið á skoða Breytingu.
7. Smellið á skoða Hnitanet.
8. Smellið á „Bóka“.
9. Lokaðu skjámyndinni.
10. Farið í Viðskiptaskuldir > Lánardrottnar > Lánardrottnar.
11. Veljið þann lánardrottinn sem var á innkaupapöntuninni. Til dæmis, veljið lánardrottinn 1001.
12. Í listanum skal smella á tengilinn í valinni línu.
13. Í aðgerðasvæðinu er smellt á lánardrottinn.
14. Smella á Færslur.
15. Velja reikninginn sem þú stofnaðir.
    * uppsöfnun komubókar var bakfærð og bókaðar á viðeigandi kostnaðarlykil.  


