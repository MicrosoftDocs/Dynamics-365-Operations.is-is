---
title: Stofna leiðir (febrúar 2016)
description: Þetta verk einblínir á að búa til framleiðsluleiðir fyrir fullunnin vara og hálfunnin vara.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a68b28c0e0ee14429a23d3241cabdae948d706d2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "354093"
---
# <a name="create-routes-february-2016"></a>Stofna leiðir (febrúar 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta verk einblínir á að búa til framleiðsluleiðir fyrir fullunnin vara og hálfunnin vara. Þetta er fimmta verkið í línunni Útreikningur uppskrifta. Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.


## <a name="create-a-route-for-a-semi-finished-product"></a>Búa til leið fyrir hálfunnin vara
1. Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.
2. Í listanum skal smella á tengilinn í valinni línu.
    * Veljið vörunúmer BOM_2.  
3. Smellið á tæknifræðingur á aðgerðarúðunni.
4. Smellt er á Leiðinni.
5. Smellið á „Nýtt“.
6. Smellt er á Leið og leiðarútgáfa.
7. Sláið inn gildi í reitnum „Lýsing“.
    * Til dæmis, slá inn ROUTE_2.  
8. Sláið inn eða veldu gildi í reitnum svæði.
    * Í þessu dæmi, slá inn eða velja Svæði 1.  
9. Smellið á „Í lagi“.
10. Smellið á „Nýtt“.
11. Færa inn eða veljið gildi í svæðinu aðgerð.
    * Í þessu dæmi, velja Samsetning.  
12. Í reitinn keyrslutími skal slá inn númer.
    * Til dæmis, skrifið 1. Uppsetningartímar eru að öllu jöfnu hluti af verðinu sem reiknað er fyrir vöruna.  
13. Í reitinn leiðaflokkur skal slá inn eða velja gildi.
    * Í þessu dæmi, velja Std.  
14. Smellið á flipann „Setja upp“.
15. Sláið inn eða veldu gildi í reitnum Setja upp flokkur.
    * Í þessu dæmi, velja Samsetning.  
16. Smellt er á tímaflipann.
17. Í svæði Uppsetningartími, slá inn tölu.
    * Í þessu dæmi, slá inn 1. Uppsetningartímar eru að öllu jöfnu hluti af verðinu sem reiknað er fyrir vöruna.  
18. Í aðgerðasvæði, smella á Leiðarútgáfa.
19. Smellið á Samþykkja.
20. Velja skal Já í „Á einnig að samþykkja leiðina?“ reit.
21. Smellið á „Í lagi“.
22. Í aðgerðasvæði, smella á Leiðarútgáfa.
23. Smellið á Virkja.
24. Lokið síðunni.
25. Lokið síðunni.

## <a name="create-a-route-for-a-finished-product"></a>Búa til leið fyrir fullunnin vara
1. Í listanum skal smella á tengilinn í valinni línu.
    * Veljið vörunúmer BOM_1.  
2. Smellið á tæknifræðingur á aðgerðarúðunni.
3. Smellt er á Leiðinni.
4. Smellið á „Nýtt“.
5. Smellt er á Leið og leiðarútgáfa.
6. Sláið inn gildi í reitnum „Lýsing“.
    * Í þessu dæmi, slá inn ROUTE_1.  
7. Sláið inn eða veldu gildi í reitnum svæði.
    * Í þessu dæmi, slá inn eða velja Svæði 1.  
8. Smellið á „Í lagi“.
9. Smellið á „Nýtt“.
10. Færa inn eða veljið gildi í svæðinu aðgerð.
    * Í þessu dæmi, velja Umbúðir.  
11. Í reitinn keyrslutími skal slá inn númer.
    * Í þessu dæmi, slá inn 1.  
12. Í reitinn leiðaflokkur skal slá inn eða velja gildi.
    * Í þessu dæmi, velja Std.  
13. Smellið á flipann „Setja upp“.
14. Sláið inn eða veldu gildi í reitnum Setja upp flokkur.
    * Í þessu dæmi, velja Umbúðir.  
15. Smellt er á tímaflipann.
16. Í svæði Uppsetningartími, slá inn tölu.
    * Í þessu dæmi, slá inn 1.  
17. Í aðgerðasvæði, smella á Leiðarútgáfa.
18. Smellið á Samþykkja.
19. Smellið á „Í lagi“.
20. Í aðgerðasvæði, smella á Leiðarútgáfa.
21. Smellið á Virkja.
22. Lokið síðunni.
23. Lokið síðunni.

## <a name="enable-automatic-consumption-of-setup-time"></a>Kveikja á sjálfvirkt notkun á uppsetningartími
1. Smella skal á Framleiðslustýring > Uppsetningu > Leiðir > Leiðaflokkar.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Velja Std á listanum.  
3. Smellið á „Breyta“.
4. Velja Já í svæði Uppsetningartími.
    * Uppsetningartímar eru að öllu jöfnu hluti af verðinu sem reiknað er fyrir vöruna.  
5. Smellið á „Vista“.
6. Lokið síðunni.

