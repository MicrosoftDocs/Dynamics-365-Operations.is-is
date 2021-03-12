---
title: Setja upp eldsneytisvísi flutningsaðila
description: Þessari handbók sýnir hvernig stofna á eldsneytisvísasvæði, eldsneytisvísi og eldsneytisvísi flutningsaðila.
author: ShylaThompson
manager: tfehr
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSFuelIndexRegion,TMSCarrierFuelIndexTable,TMSFuelIndex
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 772468fa73e18a02331f877a375a5bd089ece6be
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004928"
---
# <a name="set-up-a-carrier-fuel-index"></a>Setja upp eldsneytisvísi flutningsaðila

[!include [banner](../../includes/banner.md)]

Þessari handbók sýnir hvernig stofna á eldsneytisvísasvæði, eldsneytisvísi og eldsneytisvísi flutningsaðila. Eldsneytisvísasvæði tilgreinir á hvaða svæðum eldsneytisvísi gilda, og eldsneytisvísir tilgreinir eldsneytisverð á tilteknu tímabili. Til að endurspegla breytingarnar í verði eldsneytis yfir tíma, er hægt að tengja marga eldsneytisvísa við flutningsaðila.  Þessi verk eru yfirleitt gert með af samræmingaraðila flutninga. Hægt er að nota þessa aðgerð í fyrirtæki gögn sýnigögn USMF eða með því að nota eigin gögn.


## <a name="create-a-fuel-index-region"></a>Stofna svæði eldsneytisvísis.
1. Fara í flutningsstjórnun > Uppsetning >Eldsneytisvísa > Svæði eldsneytisvísis.
    * Fyrst þarf að stofna mismunandi svæðum, þar sem starfa og reikna út mismunandi eldsneytisálag.  
2. Smellið á „Nýtt“.
3. Í reitnum Svæði skal færa inn gildi.
4. Í reitinn Heiti skal slá inn gildi.
5. Smellið á „Vista“.

## <a name="create-a-fuel-index"></a>Búa til eldsneytisvísi
1. Fara í flutningsstjórnun > Uppsetning >Eldsneytisvísa > Eldsneytisvísa.
    * Fyrir svæði sem hefur verið sett upp þarf að færa núgildandi verð fyrir eldsneytisálag á.  
2. Smellið á „Nýtt“.
3. Í reitnum Svæði skal smella á fellilistahnappinn til að opna leitina.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Í svæðinu Verð á gallon , færið inn tölu.
6. Færa inn dagsetningu og tíma í reitnum Raunveruleg upphafsdagsetning og -tími.
7. Smellið á „Vista“.

## <a name="create-a-carrier-fuel-index"></a>Setja upp Eldsneytisvísi fyrir flutningsaðila
1. Fara í flutningsstjórnun > Uppsetning >Eldsneytisvísa > Eldsneytisvísir flutningsaðila.
2. Smellið á „Nýtt“.
3. Færa inn gildi í reitnum eldsneytisvísir Flutningsaðila.
4. Sláið inn gildi í reitnum „Lýsing“.
5. Smellt er á Nýtt.
6. Færa inn dagsetningu og tíma í reitnum Raunveruleg upphafsdagsetning og -tími.
7. Í reitinn PPG Úr skal slá inn númer.
    * Í þessu dæmi er hægt að stilla PPG Frá svæðið sem 1.95.  
8. Í reitinn PPG í skal slá inn númer.
    * Í þessu dæmi er hægt að stilla svæðið PPG Til á 2.  
9. Færið inn tölu í svæðinu prósenta.
    * Hægt er að setja prósentu til 3 í þessu dæmi.  
10. Í reitnum gjaldmiðill skal smella á fellilistahnappinn til að opna leitina.
11. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
12. Í listanum skal smella á tengilinn í valinni línu.
13. Smellið á „Vista“.

