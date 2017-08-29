--- 
title: "Skilgreina starfsmann með fartæki"
description: "Þessi verklýsing sýnir hvernig á að úthluta rétt hlutverk notandareikningurinn starfsmanns og virkja síðan starfsmanns til að gera skráningu í vinnslusalarstjórnun."
author: YuyuScheller
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 7da224809946d90387668d25c5aed5b61f6a7b72
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Skilgreina starfsmann með fartæki

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þessi verklýsing sýnir hvernig á að úthluta rétt hlutverk notandareikningurinn starfsmanns og virkja síðan starfsmanns til að gera skráningu í vinnslusalarstjórnun.


## <a name="assign-roles-to-user-account"></a>Bæta hlutverkum við notanda
1. Farið í Kerfisstjórnun > Notendur > Notendur.
2. Nota Síu á Flýtiræsistikunni til að sía á nafn starfsmanns þar sem notandareikningurinn tengist hlutverki starfsmaður á vél. Heiti væri Shannon í sýnigögn.
3. Auðkennið skráningu notandareikningur.
4. Á listanum, smella á tengilinn "Heiti" í völdu línunni til að skoða upplýsingar um lykil notanda.
5. Veljið ‚Roles\Stjórnanda á vél', í trénu.
6. Loka upplýsingasíðunni lykil notanda.
7. Lokið síðunni.

## <a name="configure-worker-account"></a>Skilgreina notandareikning starfsmanns.
1. Farið í Mannauður > Starfsfólk > Starfsfólk.
2. Nota Síu á Flýtiræsistikunni til að sía á nafn starfsmanns þar sem notandareikningurinn tengist hlutverki starfsmaður á vél. Heiti væri Shannon í sýnigögn.
3. Auðkennið skráningu notandareikningur.
4. Á listanum, smella á tengilinn "Heiti" í völdu línunni til að skoða upplýsingar um lykil notanda.
5. Smellið á flipann Ráðningar.
6. Útvíkka tímaskráningu flýtiflipi og smella á Virkja á skráningarstöðvum.
7. Smella á Virkja á skráningarstöðvum.
8. Í reitinn reikniflokkur skal slá inn eða velja gildi.
9. Færa inn eða veljið gildi í reitnum Sjálfgefinn reikniflokkur.
10. Í reitinn samþykkisflokkur skal slá inn eða velja gildi.
11. Færa inn eða veljið gildi í reit fyrir staðlaða forstillingu
12. Færa inn eða veljið gildi í svæðinu forstillingarflokkur.
13. Smellt er á Í lagi.
14. Smella á Breyta til að færa inn númer korti fyrir nýja starfsmaður sem sinnir tímaskráningu.
15. Færa inn gildi í svæðið Kenni korts.
16. Smelltu á Vista.
17. Notaðu flýtileiðina SaveRecord (vista skrá)
18. Loka upplýsingasíðunni starfsmanns.
19. Lokið síðunni.

## <a name="assign-worker-to-device-group"></a>Úthluta starfsmanns á tækjaflokk.
1. Fara í Framleiðslustýringar > Uppsetning > Framkvæmd framleiðslu > Skilgreina verkspjald fyrir tæki.
2. Smelltu á Bæta við.
3. Í listanum skal merkja valda línu.
4. Smellið á „Í lagi“.
5. Smellið á „Breyta“.
6. Í svæðið eining Framleiðslu er hægt að setja síu sjálfgefið fyrir starfsmann. Þetta mun tryggja að eingöngu vinnslur fyrir valda framleiðslueiningu eru birtar þegar starfsmaður skráir sig inn á tækinu.
7. Lokið síðunni.


