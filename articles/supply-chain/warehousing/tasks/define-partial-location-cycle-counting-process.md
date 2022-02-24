---
title: 'Skilgreina hlutastaðsetning reglulegrar talningar '
description: Þegar þú notar áætlun um reglulega talningu til að stofna talningarvinnu, geturðu stýrt hinum raunverulegu talningaraðgerðum með því að fara fram á að aðeins sérstakar vörur og vöruafbrigði verði talin í staðinn fyrir allar lagerbirgðir á staðsetningunni.
author: ShylaThompson
manager: tfehr
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItemCycleCount, WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSWorkTemplateTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 39a256a5a88a6d70373d6e23f1f380da6791f418
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/16/2020
ms.locfileid: "4430666"
---
# <a name="define-partial-location-cycle-counting-process"></a>Skilgreina hlutastaðsetning reglulegrar talningar  

[!include [banner](../../includes/banner.md)]

Þegar þú notar áætlun um reglulega talningu til að stofna talningarvinnu, geturðu stýrt hinum raunverulegu talningaraðgerðum með því að fara fram á að aðeins sérstakar vörur og vöruafbrigði verði talin í staðinn fyrir allar lagerbirgðir á staðsetningunni. Með því að afmarka sérstakar vörur, getur stjórnandi vöruhússins minnkað fastan kostnað við endurmat, minnkað líkur á samstæðumistökum og sparað tíma. Stjórnandi vöruhúss framkvæmir yfirleitt verkin sem tengjast uppsetningu. Hægt er að fara í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða þín eigin gögn.


## <a name="create-a-cycle-counting-work-template"></a>Stofna Vinnusniðmát reglulegrar talningar
1. Fara í vöruhúsakerfi  > Uppsetning  > Vinna  > Vinnusniðmát.
2. Í svæðinu gerð vinnupöntunar, skal velja „Regluleg talning“.
3. Smellið á „Nýtt“.
4. Í reitinn raðnúmer skal slá inn númer.
    * Röðunarpöntunin er frá lægsta númerinu til hæsta númersins. Gildið verður að vera meira en 0 (núll).  
5. Í listanum skal merkja valda línu.
6. Færa inn gildi í reitnum Vinnusniðmát.
7. Færa inn gildi í reitnum lýsingu Vinnusniðmáts.
8. Færa inn eða velja gildi í reitnum Kenni Vinnuklasa.
9. Í reitinn Vinnuforgangur skal slá inn númer.
10. Smellið á „Vista“.
11. Smellið á „Nýtt“.
12. Í listanum skal merkja valda línu.
13. Veljið „Talning“ í svæðinu vinnutegund.
14. Færa inn eða velja gildi í reitnum Kenni Vinnuklasa.
15. Smellið á „Vista“.
16. Smella á Vinnulínuskil.
17. Smellið á „Nýtt“.
18. Í reitinn raðnúmer skal slá inn númer.
    * Röðunarpöntunin er frá lægsta númerinu til hæsta númersins. Gildið verður að vera meira en 0 (núll).  
19. Smellið á „Vista“.
20. Lokið síðunni.
21. Lokið síðunni.

## <a name="create-a-cycle-counting-plan"></a>Stofna áætlun um reglulega talningu
1. Fara í vöruhúsakerfi > Uppsetning > Reglulega talningu > Áætlanir um reglulega talningu.
2. Smellið á „Nýtt“.
3. Í reitnum Auðkenni fyrir áætlun um reglulega talningu skal færa inn gildi.
4. Í reitinn Lýsing skal slá inn gildi.
5. Í reitnum Hámarksfjöldi reglulegrar talningar skal færa inn tölu.
6. Sláið inn eða veldu gildi í reitnum vinnusniðmát.
7. Smellið á „Nýtt“.
8. Í reitinn raðnúmer skal slá inn númer.
    * Röðunarpöntunin er frá lægsta númerinu til hæsta númersins. Gildið verður að vera meira en 0 (núll).  
9. Sláið inn gildi í reitnum „Lýsing“.
10. Smellið á „Vista“.
11. Smella á Skilgreina fyrirspurn um afurð
12. Í listanum skal merkja valda línu.
13. Í reitinn Skilyrði skal slá inn eða veldu gildi.
14. Smellið á „Í lagi“.
15. Lokið síðunni.

