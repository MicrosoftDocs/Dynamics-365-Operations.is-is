---
title: Hefja framleiðslupöntun
description: Þessi verklýsing sýnir hvernig framleiðslupöntun er hafin í vinnslusal.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f83091a9f3e96a9176860bd16fa5969507488a25
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547469"
---
# <a name="start-a-production-order"></a>Hefja framleiðslupöntun

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig framleiðslupöntun er hafin í vinnslusal. Tíma- og efnisnotkun er skráð í þessa vinnslu. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta er fimmta ferlið af sjö sem útskýrir lífsferil pöntunar í framleiðslu.


## <a name="start-a-production-order"></a>Hefja framleiðslupöntun
1. Fara í Framleiðslustýringar > Framleiðslupantanir > Allar framleiðslupantanir.
    * Veljið framleiðslupöntun sem hefur stöðuna Losað.  
2. Smellið á „Framleiðslupöntun“ á aðgerðarúðunni.
3. Smellið á „Byrja“.
    * Á þessari síðu er hægt að staðfesta upphaf framleiðslupöntunarinnar.  
4. Smellið á flipann „Almennt“.
5. Í af rekstri. Nei. skal færa inn ‚10‘.
6. Veljið ‚Alltaf‘ í reitnum Sjálfvirk leiðarnotkun.
7. Smellt er á gátreitinn Bóka leiðarspjald núna.
8. Veljið ‚Alltaf‘ í reitnum Sjálfvirk uppskriftarnotkun.
9. Smellt er í gátreitinn Bóka tiltektarlista núna.
10. Smellt er í gátreitinn Prenta tiltektarlista.
11. Smellið á „Í lagi“.
    * Þetta er prentaði tiltektarlistinn sem sýnir efni sem notað er fyrir framleiðslupöntunina.  
12. Lokið síðunni.

## <a name="validate-the-picking-list"></a>Sannprófa tiltektarlistann
1. Smellið á „Skoða“ á aðgerðarúðunni.
2. Smellt er á tiltektarlista.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Smellið á „Breyta“.
6. Í reitnum Notkun skal slá inn númer.
7. Smellið á „Bóka“.
8. Smellið á „Í lagi“.
    * Í færslubók tiltektarlista er efni sem er notað í framleiðslupöntuninni bókað. Áður en færslubókin er bókuð er hægt að gera leiðréttingar ef munur er á áætluðu magni og raunverulega notuðu magni.  
9. Smellt er á flipann GridPanel.
10. Lokið síðunni.

## <a name="verify-the-route-card-journal"></a>Sannprófa færslubók leiðarspjalda
1. Smellið á „Skoða“ á aðgerðarúðunni.
2. Smellt er á Leiðarspjald.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
4. Í listanum skal smella á tengilinn í valinni línu.
5. Smellið á „Breyta“.
6. Í reitnum Vinnustundir skal slá inn tölu.
7. Smellið á „Bóka“.
8. Smellið á „Í lagi“.
    * Í færslubók leiðarspjalda er tími sem er eytt í staðar aðgerðir skráður. Einnig er hægt að tilkynna gallað og ógallað magn.  
