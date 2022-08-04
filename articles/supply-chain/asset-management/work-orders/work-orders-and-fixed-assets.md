---
title: Verkbeiðnir og eignir
description: Þessi grein útskýrir verkbeiðnir og fastafjármuni í eignastýringu.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ed83450592d85205743c9ff1aefd0e66e5d2b90c
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111989"
---
# <a name="work-orders-and-fixed-assets"></a>Verkbeiðnir og eignir

[!include [banner](../../includes/banner.md)]


Í eignastýringu geta eignir verið tengdar fastafjármunum og þú getur búið til verkbeiðnir fyrir þessar eignir. Ef þú notar þessa virkni geturðu fengið heildaryfirlit yfir fastafjármuni, tengd fjárfestingarverkefni og þann kostnað sem skráður er á fjárfestingarverkefnin í **Verkefnastjórnun og bókhald** og **Fastafjármunir** einingar í fjármála- og rekstraröppunum.

>[!NOTE]
>Reiturinn **Númer eignar** í vinnslu verkbeiðni er aðeins stilltur ef **Fjárfesting** er valin sem verkgerð í verkbeiðnivinnslu.

Myndin hér að neðan sýnir tengsl fjárfestingarverkefnis í einingunni **Verkefnisstjórnun og bókhald** og vinnuverkefni vinnuverkefni.

![Mynd 1.](media/24-work-orders.png)

Eftirfarandi aðferð lýsir tengslum á milli eigna, verkbeiðna, verkbeiðniverka og fastafjármuna.

1. Þú býrð til eign sem þú tengir fastafjármunum.

![Mynd 2.](media/25-work-orders.png)

2. Þegar þú setur upp verkbeiðnigerðir á síðunni **Gerðir verkbeiðna** (**Eignastjórnun** > **Uppsetning** > **Verkbeiðnir** > **Verkbeiðnigerðir**) býrðu til verkbeiðnigerð til að meðhöndla fjárfestingar. Sjá einnig [Verkbeiðnigerðir](../setup-for-work-orders/work-order-types.md).

![Mynd 3.](media/26-work-orders.png)

3. Þegar þú setur upp verkflokka verkbeiðna á flipanum **Verkflokkur** á síðunni **Verkuppsetning verkbeiðni** (**Eignastýring** > **Uppsetning** > **Verkbeiðnir** > **Uppsetning verks**) býrðu til tengsl milli þeirrar verkbeiðnigerðar sem notuð er við fjárfestingar og verkefnahópsins sem stofnað var til vegna fjárfestinga á síðunni **Verkflokkar** í einingunni **Verkefnisstjórnun og bókhald** (**Verkefnisstjórnun og bókhald** > **Uppsetning** > **Bókun** > **Verkefnahópar**).

![Mynd 4.](media/27-work-orders.png)

4. Þegar þú býrð til verkbeiðni sem tengist fastri eign velur þú þá gerð verkbeiðni sem notuð er til að meðhöndla fjárfestingar, til dæmis **Fjárfesting**.

5. Þegar verkbeiðni er búin til, er tengd tegund verkbeiðni sýnd á síðunni **Allar verkbeiðnir**.

![Mynd 5.](media/28-work-orders.png)

6. Þegar verkbeiðnin er búin til er verkið sem tengist verkbeiðninni búið til á síðunni **Öll verk** í einingunn **Verkefnisstjórnun og bókhald** (**Verkefnisstjórnun og bókhald** > **Verk** > **Öll verk**). Til að skoða upplýsingar sem tengjast verkefninu, veldu tengilinn í reitnum **Kenni verks** á flipanum **Almennt** á flýtiflipanum **Línulýsing** á upplýsingasíðunni **Allar verkbeiðnir** í einingunni **Eignastýring** (**Eignastýring** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir**).

![Mynd 6.](media/29-work-orders.png)

7. Til að sjá yfirlit yfir verk sem eru tengd fastri eign skaltu velja **Fastar eignir** > **Fastar eignir** > **Fastar eignir** og síðan í reitnum **Númer fastrar eignar** velurðu tengilinn fyrir föstu eignina til að opna upplýsingaglugga. Stækkaðu gluggann **Tengdar upplýsingar** hægra megin á síðunni og veldu flýtiflipann **Tengd verk**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
