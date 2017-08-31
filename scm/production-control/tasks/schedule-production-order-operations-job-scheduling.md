--- 
title: "Áætla framleiðslupöntun með rekstrar- og vinnuröðun"
description: "Þetta ferli áherslu á röðun á framleiðslupöntun með aðgerðaröðun og vinnsluröðun."
author: ChristianRytt
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 10ccb4ac1088e27f3f5771bcb964bf3cc0a509ab
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="schedule-a-production-order-with-operations-and-job-scheduling"></a>Áætla framleiðslupöntun með rekstrar- og vinnuröðun

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli áherslu á röðun á framleiðslupöntun með aðgerðaröðun og vinnsluröðun. Engar vinnslur eru stofnaðar með aðgerðaröðun meðan störf eru stofnuð með vinnsluröðun. Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF. Þetta ferli er ætluð fyrir framleiðslustjóri skipuleggjandi framleiðslu eða vinnusalarstjórnun yfirmaður sem unnið er í framleiðsluumhverfi afmörkuð.


## <a name="create-a-production-order"></a>Stofna framleiðslupöntun
1. Fara í Framleiðslustýringar > Framleiðslupantanir > Allar framleiðslupantanir.
2. Smella á Ný framleiðslupöntun.
3. Í reitinn Vörunúmer skal slá inn eða veldu gildi.
    * Veldu vörunúmer D0001.  
4. Smellið á „Stofna“.

## <a name="schedule-operations-for-the-production-order"></a>Ef framkvæma á aðgerðaröðun fyrir framleiðslupöntun.
1. Í listanum skal merkja valda línu.
    * Veljið framleiðslupöntun sem hefur verið rétt stofnuð. Það ætti að vera efst á listanum.      
2. Í Aðgerðarrúðunni er smellt á Áætlun.
3. smella Raða aðgerðum
4. Í reitnum röðunarstefna er valið „áfram frá röðunardagsetningu“.
5. Dagsetning er rituð í reitinn röðunardagsetning.
    * Velja dagsetningu í framtíðinni, til dæmis í dag plús ein vika. Með valda Röðun stefnu framleiðslupöntun verður raðað áfram frá þessari dagsetningu.  
6. Smellið á „Í lagi“.
7. Í listanum skal merkja valda línu.
    * Athugið Stöðu framleiðslu er breytt í áætlað  
8. Í listanum skal smella á tengilinn í valinni línu.
9. Smellt er á Allar vinnslur.
    * Athugið að engar vinnslur eru stofnaðar með aðgerðaröðun.  
10. Lokið síðunni.

## <a name="schedule-jobs-for-the-production-order"></a>Ef framkvæma á aðgerðaröðun fyrir framleiðslupöntun.
1. Í Aðgerðarrúðunni er smellt á Áætlun.
2. Smella á Áætla verk.
3. Í reitnum röðunarstefna er valið „áfram frá röðunardagsetningu“.
4. Dagsetning er rituð í reitinn röðunardagsetning.
    * Velja dagsetningu í framtíðinni, til dæmis í dag plús ein vika. Með valda Röðun stefnu framleiðslupöntun verður raðað áfram frá þessari dagsetningu.  
5. Smellið á „Í lagi“.
6. Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.
7. Smellt er á Allar vinnslur.
    * Athugið samkvæmt virk leið 5 störf eru stofnuð með vinnsluröðun.  


