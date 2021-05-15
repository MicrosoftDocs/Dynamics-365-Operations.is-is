---
title: Stofna efnisáætlun fyrir aukaafurðir.
description: Framleiðslustjóri áætlar efnisþarfir fyrir vörur sem eru aukaafurðir formúlu.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920730"
---
# <a name="create-a-material-plan-for-co-products"></a>Stofna efnisáætlun fyrir aukaafurðir.

[!include [banner](../../includes/banner.md)]

Framleiðslustjóri áætlar efnisþarfir fyrir vörur sem eru aukaafurðir formúlu. Sýnigögn fyrirtækisins til að stofna þetta ferli er USP2.

## <a name="create-requirement-for-a-co-product"></a>Stofna þörf fyrir aukaafurð

1. Farið í **Sala og markaðssetning \> Vinnusvæði \> Vinnsla og fyrirspurnir sölupantana**.
1. Veljið **Nýtt**.
1. Veldu **Velja sölupöntun**.
1. Í reitinn **Viðskiptavinalykill** skal slá inn gildi.
    * Dæmi: US-001  
1. Veljið **Í lagi**.
1. Í reitnum **Vörunúmer** skal slá inn gildi.
    * Til dæmis: P6003  
1. Í reitnum **Magn** slærðu inn tölu.
    * Til dæmis: 50000.  
1. Veljið **Vista**.

## <a name="create-a-material-plan-for-co-products"></a>Búa til efnisáætlun fyrir aukaafurðir

1. Lokið síðunni.
1. Lokið síðunni.
1. Veljið **Aðaláætlanagerð**.
1. Í reitnum **Áætlun** velurðu fellilistahnappinn til að opna uppflettinguna.
1. Í listanum skal velja tengilinn í valinni línu.
    * Dæmi: MasterPlan  
1. Veljið **Keyra**.
1. Útvíkka eða draga saman **Færslur sem á að taka með** hlutann.
1. Velja **Síu**.
1. Í listanum skal velja línuna fyrir **Reitur** = *Vörunúmer*.
1. Í reitnum **Skilyrði** skal slá inn gildi.
    * Til dæmis: P6003  
1. Veljið **Í lagi**.
1. Veljið **Í lagi**.
1. Veldu **Tillögur**.
1. Nota flýtiafmörkun til að finna færslur Til dæmis, sía svæðið **Vörunúmer** með gildið 'P6000'.
    * Sía eftir formúluvöru sem hefur aukaafurð vöru sem stofnuð var sölupöntun fyrir.  
1. Í listanum skal merkja valda línu.
    * Velja allar línur sem sían skilaði.  
1. Í listanum skal velja tengilinn í valinni línu.
1. Víkkið út hlutann **Þarfarakning**.
1. Í listanum skal velja tengilinn í valinni línu.
    * Áætluð pöntun er fest við sölupöntun fyrir aukaafurðina.  
1. Lokið síðunni.

## <a name="create-a-second-requirement-for-a-co-product"></a>Stofna aðra þörf fyrir aukaafurð

1. Farið í **Sala og markaðssetning \> Vinnusvæði \> Vinnsla og fyrirspurnir sölupantana**.
1. Veljið **Nýtt**.
1. Veldu **Velja sölupöntun**.
1. Í reitinn **Viðskiptavinalykill** skal slá inn gildi.
    * Dæmi: US-001  
1. Veljið **Í lagi**.
1. Í reitnum **Vörunúmer** skal slá inn gildi.
    * Til dæmis: P6003  
1. Í reitnum **Magn** slærðu inn tölu.
    * Til dæmis: 50000.  
1. Veljið **Vista**.

## <a name="create-a-second-material-plan-for-co-products"></a>Stofna aðra efnisáætlun fyrir aukaafurðir

1. Í reitnum **Áætlun** velurðu fellilistahnappinn til að opna uppflettinguna.
2. Í listanum skal velja tengilinn í valinni línu.
    * Dæmi: MasterPlan  
3. Veljið **Keyra**.
4. Útvíkka eða draga saman **Færslur sem á að taka með** hlutann.
5. Velja **Síu**.
6. Í listanum skal velja línuna fyrir **Reitur** = *Vörunúmer*.
7. Í reitnum *Skilyrði* skal slá inn gildi.
    * Til dæmis: P6003  
8. Veljið **Í lagi**.
9. Veljið **Í lagi**.
10. Veldu **Tillögur**.
11. Nota flýtiafmörkun til að finna færslur Til dæmis, sía svæðið **Vörunúmer** með gildið 'P6000'.
    * Sía eftir formúluvöru sem hefur aukaafurð vöru sem stofnuð var sölupöntun fyrir.  
12. Í listanum skal merkja valda línu.
    * Velja allar línur sem sían skilaði.  
13. Í listanum skal velja tengilinn í valinni línu.
14. Útvíkka eða draga saman hlutann **Þarfarakning**.
15. Í listanum skal velja tengilinn í valinni línu.
    * Áætluð pöntun er fest við sölupöntun fyrir aukaafurðina.  
16. Lokið síðunni.
17. Veljið **Aðaláætlanagerð**.
18. Farið í **Aðaláætlanagerð \> Uppsetning \> Færibreytur aðaláætlanagerðar**.
19. Veljið *Nei* í reitnum **Slökkva á öllum ferlum áætlanagerðar**.
20. Lokið síðunni.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]