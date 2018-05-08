--- 
title: Skipta eign
description: "Þessi leiðarvísi fyrir verk mun skipta hlutfall eitt eignabók á nýtt eignabók."
author: saraschi2
manager: AnnBe
ms.date: 10/19/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b4c1b39bcae1fa3830f3a217d1ad89e84cd72134
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="split-a-fixed-asset"></a>Skipta eign

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi leiðarvísi fyrir verk mun skipta hlutfall eitt eignabók á nýtt eignabók.  Það notar hlutverk Bókhaldara og sýnigögn USMF.


## <a name="create-a-new-fixed-asset"></a>Búa til nýja eign
1. Fara í Eignir > Eignir > Eignir.
2. Smellið á „Nýtt“.
3. Færa inn eða veljið gildi í svæðinu eignaflokkur.
4. Athugið númer eignar til að nota seinna í ferlinu skipta.
5. Í reitinn Heiti skal slá inn gildi.
6. Lokaðu skjámyndinni.

## <a name="split-a-fixed-asset"></a>Skipta eign
1. Finna og veljið eignir sem skipta á í listanum.
2. Í listanum skal smella á tengilinn í valinni línu.
3. Smelltu á bækur.
    * Veljið bók til að skipta á nýju eignina.  
4. Smellið á Aðgerðir.
5. Smellt er á skipta Eign.
6. Sláðu inn eða veldu gildi í reitnum Á eign.
7. Í reitnum Á bók skal smella á fellilistahnappinn til að opna leitina.
8. Færa inn dagsetningu í dagsetningarsvæði Færslunnar.
9. Færið inn tölu í svæðinu prósenta.
10. Sláið inn eða veljið gildi í reitnum heiti færslubókar.
11. Smellið á „Í lagi“.

## <a name="post-the-journal-transaction"></a>Bókið færslubókarfærsla.
1. Fara í Eignir >°Færslubókarfærslur°> Eignabók.
2. Veljið færslubók sem er stofnuð með skipta ferlinu á listanum.
3. Smellið á „Línur“.
    * Staðfestið stofnaðar færslubókarlínur .  Leiðrétting kaupvirðisfærsla er stofnuð fyrir upprunalegu eignina til að minnka virði eftir prósentu sem tilgreind er við að skipta ferlinu.  Kaupfærsla er stofnuð fyrir nýju eignina fyrir sömu upphæð.  
4. Smellið á „Bóka“.


