---
title: Færa reikningsgögn inn í viðskiptaskuldakerfi með reikningasafni
description: Þetta efni lýsir því hvernig nota á komubókina til að búa til reikninga.
author: abruer
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4768ee6ddbaba8ae5bab5e2f9f7df9239efeb90
ms.sourcegitcommit: 9cbff8a2cdeaf606488fb0044b3de4ab4409c9dc
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 02/26/2022
ms.locfileid: "8358290"
---
# <a name="key-invoice-data-into-the-ap-system-using-invoice-pool"></a>Færa reikningsgögn inn í viðskiptaskuldakerfi með reikningasafni

[!include [banner](../../includes/banner.md)]

Þetta efni lýsir því hvernig nota á komubókina til að búa til reikninga. Nota síðan reikningasafninu til að jafna reikninginn við innkaupapöntun og ljúka kostnað á síðunni reikningur lánardrottins.


## <a name="create-a-purchase-order"></a>Stofna innkaupapöntun
1. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Viðskiptaskuldir > Innkaupapantanir > Innkaupapantanir**.
2. Smellið á **Nýtt** til að stofna nýja innkaupapöntun.
3. Í reitnum **Lánardrottnalykill** skal velja lánardrottinn fyrir fellilistann. Til dæmis, veljið lánardrottinn **1001**.
4. Veljið **Í lagi**.
5. Í reitnum **Vörunúmer** velurðu vörnúmer þjónustu af fellilistanum. Veljið til dæmis **S0001**. Nettóupphæðin er 75,00.  Þetta er Upphæð sem við búumst við á reikningnum.  
6. Í aðgerðasvæðinu velurðu **Innkaup**.
7. Veldu **Staðfesta**.

## <a name="create-and-post-and-invoice"></a>Stofna og bóka og reikningsfæra
1. Í skoðunarrúðunni ferðu í **Einingar > Viðskiptaskuldir > Reikningar > Komubók**.
2. Veljið **Nýtt**.
3. Opna uppflettingu til að velja heiti komubókar sem á að nota.
4. Veldu heiti komubókarinnar sem þú vilt nota.
5. Veldu **Línur** til að opna skrána og færa inn kostnaðarlínur.
6. Í Uppfletting skal velja lánardrottinn. Til dæmis, veljið lánardrottinn **1001**.
7. Í reitnum **Reikningur** færirðu inn númer reiknings.
8. Í reitinn **Lýsing** skal slá inn gildi.
9. Í reitnum **Kredit** skal slá inn tölu.
10. Í reitnum **Innkaupapöntun** opnarðu fellivalmyndina til að velja innkaupapöntunina sem þú bjóst til áður.
11. Í reitnum **Samþykkt af** skal auðkenna samþykktaraðila á fellilistanum og smella á **Velja** til að velja þann samþykktaraðila.
12. Veldu **Bóka**.

## <a name="open-an-invoice-from-the-pool-and-match-it-to-a-purchase-order-to-complete-the-invoice-process"></a>Opna reikning úr safninu og stemma hann við innkaupapöntun til að ljúka reikningsferlinu.
1. Í skoðunarrúðunni ferðu í **Einingar > Viðskiptaskuldir > Reikningar > Reikningasafn**.
2. Veldu **Innkaupapöntun** til að búa til reikning lánardrottins úr reikningi í safninu.
3. Veljið reikninginn sem á að skoða.
4. Veldu **Uppfæra samsvörunarstöðu** til að ljúka við samsvörun.
5. Í aðgerðasvæðinu velurðu **Valkostir**.
6. Veldu **Breyta skjámynd**.
7. Veldu **Hnitalínuyfirlit**.
8. Veldu **Bóka**.
9. Lokið síðunni.
10. Í skoðunarrúðunni ferðu í **Kerfiseiningar > Viðskiptaskuldir > Lánardrottnar > Lánardrottnar**.
11. Veljið þann lánardrottinn sem var á innkaupapöntuninni. Til dæmis, veljið lánardrottinn **1001**.
12. Á aðgerðasvæðinu velurðu **Lánardrottinn**.
13. Veldu **Færslur**.
14. Velja reikninginn sem þú stofnaðir. uppsöfnun komubókar var bakfærð og bókaðar á viðeigandi kostnaðarlykil.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
