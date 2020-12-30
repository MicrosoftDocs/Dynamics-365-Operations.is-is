---
title: Verkbeiðnir og eignir
description: Þetta efni útskýrir verkbeiðnir og eignir í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ca7a5d88de4308d7be9c1bc749b9dbf1da027c2c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4430542"
---
# <a name="work-orders-and-fixed-assets"></a>Verkbeiðnir og eignir

[!include [banner](../../includes/banner.md)]


Í eignastýringu geta eignir verið tengdar fastafjármunum og þú getur búið til verkbeiðnir fyrir þessar eignir. Ef þú notar þessa virkni geturðu fengið fullkomið yfirlit yfir fastafjármuni, tengd fjárfestingarverkefni og kostnaðinn sem skráður er á fjárfestingarverkefnin í einingunum **Verkefnisstjórnun og bókhald** og **Fastafjármunir** í Microsoft Dynamics 365 for Finance and Operations.

>[!NOTE]
>Reiturinn **Númer eignar** í vinnslu verkbeiðni er aðeins stilltur ef **Fjárfesting** er valin sem verkgerð í verkbeiðnivinnslu.

Myndin hér að neðan sýnir tengsl fjárfestingarverkefnis í einingunni **Verkefnisstjórnun og bókhald** og vinnuverkefni vinnuverkefni.

![Mynd 1](media/24-work-orders.png)

Eftirfarandi aðferð lýsir tengslum á milli eigna, verkbeiðna, verkbeiðniverka og fastafjármuna.

1. Þú býrð til eign sem þú tengir fastafjármunum.

![Mynd 2](media/25-work-orders.png)

2. Þegar þú setur upp verkbeiðnigerðir á síðunni **Gerðir verkbeiðna** (**Eignastjórnun** > **Uppsetning** > **Verkbeiðnir** > **Verkbeiðnigerðir**) býrðu til verkbeiðnigerð til að meðhöndla fjárfestingar. Sjá einnig [Verkbeiðnigerðir](../setup-for-work-orders/work-order-types.md).

![Mynd 3](media/26-work-orders.png)

3. Þegar þú setur upp verkflokka verkbeiðna á flipanum **Verkflokkur** á síðunni **Verkuppsetning verkbeiðni** (**Eignastýring** > **Uppsetning** > **Verkbeiðnir** > **Uppsetning verks**) býrðu til tengsl milli þeirrar verkbeiðnigerðar sem notuð er við fjárfestingar og verkefnahópsins sem stofnað var til vegna fjárfestinga á síðunni **Verkflokkar** í einingunni **Verkefnisstjórnun og bókhald** (**Verkefnisstjórnun og bókhald** > **Uppsetning** > **Bókun** > **Verkefnahópar**).

![Mynd 4](media/27-work-orders.png)

4. Þegar þú býrð til verkbeiðni sem tengist fastri eign velur þú þá gerð verkbeiðni sem notuð er til að meðhöndla fjárfestingar, til dæmis **Fjárfesting**.

5. Þegar verkbeiðni er búin til, er tengd tegund verkbeiðni sýnd á síðunni **Allar verkbeiðnir**.

![Mynd 5](media/28-work-orders.png)

6. Þegar verkbeiðnin er búin til er verkið sem tengist verkbeiðninni búið til á síðunni **Öll verk** í einingunn **Verkefnisstjórnun og bókhald** (**Verkefnisstjórnun og bókhald** > **Verk** > **Öll verk**). Til að skoða upplýsingar sem tengjast verkefninu, veldu tengilinn í reitnum **Kenni verks** á flipanum **Almennt** á flýtiflipanum **Línulýsing** á upplýsingasíðunni **Allar verkbeiðnir** í einingunni **Eignastýring** (**Eignastýring** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir**).

![Mynd 6](media/29-work-orders.png)

7. Til að sjá yfirlit yfir verk sem eru tengd fastri eign skaltu velja **Fastar eignir** > **Fastar eignir** > **Fastar eignir** og síðan í reitnum **Númer fastrar eignar** velurðu tengilinn fyrir föstu eignina til að opna upplýsingaglugga. Stækkaðu gluggann **Tengdar upplýsingar** hægra megin á síðunni og veldu flýtiflipann **Tengd verk**.

