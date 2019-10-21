---
title: Verkbeiðnir og eignir
description: Þetta efni útskýrir verkbeiðnir og eignir í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250830"
---
# <a name="work-orders-and-fixed-assets"></a>Verkbeiðnir og eignir


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Í eignastýringu geta eignir verið tengdar fastafjármunum og þú getur búið til verkbeiðnir fyrir þessar eignir. Ef þú notar þessa virkni geturðu fengið fullkomið yfirlit yfir fastafjármuni, tengd fjárfestingarverkefni og kostnaðinn sem skráður er á fjárfestingarverkefnin í einingunni **Verkefnisstjórnun og bókhald** og eininguna **Fastafjármunir**.

>[!NOTE]
>Reiturinn **Númer eignar** er aðeins fylltur út í vinnslugerð verkbeiðni ef gerðin „Fjárfesting“ er valin sem verkgerð í verkbeiðniverki.

![Mynd 1](media/24-work-orders.png)

Eftirfarandi aðferð lýsir tengslum á milli eigna, verkbeiðna, verkbeiðniverka og fastafjármuna.

1. Þú býrð til eign sem þú tengir fastafjármunum eins og sýnt er á myndinni hér að neðan.

![Mynd 2](media/25-work-orders.png)

2. Þegar þú setur upp verkbeiðnigerðir (**Eignastjórnun** > **Uppsetning** > **Verkbeiðnir** > **Verkbeiðnigerðir**), þú býrð til verkbeiðnigerð til að meðhöndla fjárfestingar. Sjá einnig [Verkbeiðnigerðir](../setup-for-work-orders/work-order-types.md).

![Mynd 3](media/26-work-orders.png)

3. Þegar þú setur upp verkhópa verkbeiðna (tengillinn **Eignastýring** > **Uppsetning** > **Verkbeiðnir** > **Uppsetning verks** > **Verkefnahópur**), þú býrð til tengsl milli þeirrar verkbeiðnigerðar sem notuð er við fjárfestingar og verkefnahópsins sem stofnað var til vegna fjárfestinga í einingunni **Verkefnisstjórnun og bókhald** (**Verkefnisstjórnun og bókhald** > **Uppsetning** > **Bókun** > **Verkefnahópar**).

![Mynd 4](media/27-work-orders.png)

4. Þegar þú býrð til verkbeiðni sem snýr að varanlegum eignum velur þú þá gerð verkbeiðni sem notuð er til að meðhöndla fjárfestingar, til dæmis „Fjárfesting“.

5. Þegar verkbeiðni er búin til, er tengd tegund verkbeiðni sýnd í **Öllum verkbeiðnum**.

![Mynd 5](media/28-work-orders.png)

6. Þegar verkbeiðni er stofnuð er verkefnið sem tengist verkbeiðninni stofnað í **Verkefnisstjórnun og bókhald** > **Öll verkefni**. Þú getur séð upplýsingar sem tengjast verkefninu með því að smella á tengilinn **Verkkenni** á verkbeiðninni (í **Eignastjórnun** opnarðu verkbeiðnina í smáatriðum > flýtiflipann **Línuupplýsingar** > flipann **Almennt** > reitnum **Verkkenni**).

![Mynd 6](media/29-work-orders.png)

7. Í **Fastafjármunir**, þú getur séð yfirlit yfir verkefnin sem tengjast fastafjármunum (**Fastafjármunir** > **Fastafjármunir** > **Fastafjármunir** > smelltu á eignina í reitnum **Númer eignar** > skoða innihaldið í glugganum **Tengdar upplýsingar** > hlutanum **Tilheyrandi verkefni**).

