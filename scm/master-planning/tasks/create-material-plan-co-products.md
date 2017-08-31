--- 
title: "Búa til efnisáætlun fyrir aukaafurðir"
description: "Framleiðslustjóri áætlar efnisþarfir fyrir vörur sem eru aukaafurðir formúlu."
author: YuyuScheller
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 4eb36b0de53f40f882950628d55d6ac08ac5fdde
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-material-plan-for-co-products"></a>Búa til efnisáætlun fyrir aukaafurðir

[!include[task guide banner](../../includes/task-guide-banner.md)]

Framleiðslustjóri áætlar efnisþarfir fyrir vörur sem eru aukaafurðir formúlu. Sýnigögn fyrirtækisins til að stofna þetta ferli er USP2.


## <a name="create-requirement-for-a-co-product"></a>Stofna þörf fyrir aukaafurð
1. Farðu í Sjálfgefið mælaborð.
2. Smellt er á Vinnsla og fyrirspurnir sölupantana.
3. Smellt er á Nýtt.
4. Smellt er á sölupöntun.
5. Í reitinn Reikningur viðskiptavinar skal slá inn gildi.
    * Dæmi: US-001  
6. Smellið á „Í lagi“.
7. Í reitnum Vörunúmer skal slá inn gildi.
    * Til dæmis: P6003  
8. Færið inn númer í reitnum „Magn“.
    * Til dæmis: 50000.  
9. Smellið á „Vista“.

## <a name="create-a-material-plan-for-co-products"></a>Búa til efnisáætlun fyrir aukaafurðir
1. Smellt er á aðaláætlanagerð.
2. Í reitnum Áætlun skal smella á fellilistahnappinn til að opna leitina.
3. Í listanum skal smella á tengilinn í valinni línu.
    * Dæmi: MasterPlan  
4. Smellið á „Keyra“.
5. Útvíkka eða draga saman Færslur sem á að taka með hluta.
6. Smellt er á Síu.
7. Á listanum, Velja línuna fyrir svæðið = vörunúmer
8. Í reitinn Skilyrði skal slá inn gildi.
    * Til dæmis: P6003  
9. Smellið á „Í lagi“.
10. Smellið á „Í lagi“.
11. Smellt er á Áætlaðar pantanir.
12. Nota flýtiafmörkun til að finna færslur Til dæmis, sía svæðið vörunúmer með gildið 'P6000'.
    * Sía eftir formúluvöru sem hefur aukaafurð vöru sem stofnuð var sölupöntun fyrir.  
13. Í listanum skal merkja valda línu.
    * Velja allar línur sem sían skilaði.  
14. Í listanum skal smella á tengilinn í valinni línu.
15. Útvíkka eða draga saman hlutann Þarfarakning.
16. Í listanum skal smella á tengilinn í valinni línu.
    * Áætluð pöntun er fest við sölupöntun fyrir aukaafurðina.  
17. Lokið síðunni.


