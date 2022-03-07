---
title: Finna úrelt afurðarafbrigði
description: Þetta ferli sýnir hvernig á að finna úreltar afurðir eða afurðaafbrigði og hvernig á að tengja lífferilsstöðu afurðar við úreltar afurðir.
author: t-benebo
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13db6620575b4c97b3f8079ac94f5231a2fd9c1b
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7577241"
---
# <a name="find-obsolete-product-variants"></a>Finna úrelt afurðarafbrigði 

[!include [banner](../../includes/banner.md)]

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



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]