---
title: Finna úrelt afurðarafbrigði
description: Þetta ferli sýnir hvernig á að finna úreltar afurðir eða afurðaafbrigði og hvernig á að tengja lífferilsstöðu afurðar við úreltar afurðir.
author: cvocph
manager: AnnBe
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4641d24cfa24722f5411da8943bfe4095a9546a4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "360188"
---
# <a name="find-obsolete-product-variants"></a>Finna úrelt afurðarafbrigði 

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli sýnir hvernig á að finna úreltar afurðir eða afurðaafbrigði og hvernig á að tengja lífferilsstöðu afurðar við úreltar afurðir. Forkröfur: Skilgreina þarf að minnsta kosti eina lífferlisstöðu afurðar sem er óvirk fyrir áætlanagerð áður en hægt er að spila þessar verkefnaleiðbeiningar.


## <a name="run-a-simulation"></a>Keyra hermingu
1. Fara í Afurðaupplýsingastjórnun > Reglubundin verk > Breyta lífferilsstöðu fyrir úreltar vörur.
2. Sláið inn eða veljið gildi í reitnum Ný lífferilsstaða afurðar.
3. Velja skal Já í Keyra hermun án þess að uppfæra afurðagagnareit.
4. Í reitinum Útiloka vörur sem voru búnar til innan þessa dagafjölda skal slá inn númer.
5. Í reitinum Útiloka vörur sem hafa verið notaðar í færslum (í dagafjölda) skal slá inn númer.
6. Útvíkka Færslur til að taka hluta.
7. Smellt er á Síu.
8. Í listanum skal merkja valda línu.
9. Í reitinn Skilyrði skal slá inn gildi.
10. Smellið á „Í lagi“.
11. Smellið á „Í lagi“.

> [!NOTE]
> Mælt er með því að keyra hermingu í lotu ef þú býst við að leita að fjölda vara. Gakktu einnig úr skugga um að hermingin sé ekki keyrð á virkasta vinnutíma fyrirtækisins.  

## <a name="review-the-simulation-results"></a>Skoða niðurstöðuna fyrir herminguna
1. Farið í Afurðarupplýsingastjórnun > Fyrirspurnir og skýrslur > Ferill lífferils- og viðhaldsstöðu afurðar.
   
> [!NOTE]
> Á þessari síðu er hægt að sjá herminiðurstöðurnar og meta hversu margar vörur og afurðaafbrigði verða tengd nýrri lífferilsstöðu afurðar þegar uppfærslan er keyrð án hermunar.  

## <a name="run-the-update-of-the-product-lifecycle-state-for-obsolete-products"></a>Keyra skal uppfærslu Lífferlisstaða afurðar fyrir úreltar vörur
1. Lokið síðunni.
2. Fara í Afurðaupplýsingastjórnun > Reglubundin verk > Breyta lífferilsstöðu fyrir úreltar vörur.
3. Útvíkka Færslur til að taka hluta.

> [!NOTE]
> Athugið að síðasta val hefur verið vistað.  

4. Velja skal Nei í Keyra hermun án þess að uppfæra afurðagagnareit.
5. Stækka útvíkkun á liðnum Keyra í bakgrunni.

> [!NOTE]
> Íhuga ætti að keyra þessa vinnslu í lotu, eftir því hversu margar vörur og afurðarafbrigði eru valin. Gangið úr skugga um að keyra ekki stórt uppfærsluverk á virkasta vinnutíma fyrirtækisins.  

6. Smellið á „Í lagi“.
7. Farið í Afurðarupplýsingastjórnun > Fyrirspurnir og skýrslur > Ferill lífferils- og viðhaldsstöðu afurðar.

> [!NOTE]
> Skoða breyttar útgefnar vörur og vöruafbrigði.  

8. Í listanum skal finna og velja þá skráningu sem óskað er eftir.

