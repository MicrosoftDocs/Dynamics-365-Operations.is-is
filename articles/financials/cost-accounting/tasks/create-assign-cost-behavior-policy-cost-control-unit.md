---
title: Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu
description: Kostnaður er flokkaður út frá kostnaðarhegðun sem annað hvort fastur eða breytilegur.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c7b39b7649aaef0d354b61e3d70b6cac887282ed
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543888"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Kostnaður er flokkaður út frá kostnaðarhegðun sem annað hvort fastur eða breytilegur. Stefna og samsvarandi reglur er úthlutað til kostnaðarstýringareiningar svo stefnan taki gildi. Nota þetta ferli til að stofna stefnu og síðan úthluta stefnunni til kostnaðarstýringareiningar


## <a name="create-a-cost-behavior-hierarchy"></a>Stofna Stigveldi kostnaðarhegðunar
1. Fara í kostnaðarbókhald > Víddir > Stigveldi vídda.
2. Smellið á „Nýtt“.
3. Smellið á „Stofna“.
4. Í reitinn Heiti stigveldi víddar skal slá inn „Stigveldi kostnaðarhegðunar“.
5. Sláið inn eða veljið gildi í reitnum Vídd.
    * Velja kostnaðareiningar  
6. Smellið á „Vista“.
7. Smella á Skoða stigveldi
8. Smellið á „Nýtt“.
9. Í svæðið Heiti hnútar, færðu inn gildi.
    * Færa inn Fastan kostnað.  
10. Í trénu skal velja „Stigveldi kostnaðarhegðunar“.
11. Smellið á „Nýtt“.
12. Í svæðið Heiti hnútar, færðu inn gildi.
    * Færa inn breytilegur kostnaður.  
13. Smellið á „Vista“.
14. Í trénu skal velja „stigveldi kostnaðarhegðunar\Fastur kostnaður“.
15. Smellið á „Nýtt“.
16. Í listanum skal merkja valda línu.
17. Sláið inn eða veldu gildi í reitnum Frá víddarstak.
    * Afmörkun víddarstaks getur innihaldið gloppur, en stökin geta ekki skarast.  
18. Sláið inn eða veldu gildi í reitnum í Til víddarstak.
    * Afmörkun víddarstaks getur innihaldið gloppur, en stökin geta ekki skarast.  
19. Í trénu skal velja „stigveldi kostnaðarhegðunar\Breytilegur kostnaður“.
20. Smellið á „Nýtt“.
21. Í listanum skal merkja valda línu.
22. Sláið inn eða veldu gildi í reitnum Frá víddarstak.
    * Afmörkun víddarstaks getur innihaldið gloppur, en stökin geta ekki skarast.  
23. Sláið inn eða veldu gildi í reitnum í Til víddarstak.
    * Afmörkun víddarstaks getur innihaldið gloppur, en stökin geta ekki skarast.  
24. Smellið á „Vista“.

## <a name="create-the-policy-and-rules"></a>Stofna stefnu og reglur
1. Fara í Kostnaðarbókhald > Stefnur > Stefnur fyrir kostnaðarhegðun.
2. Smellið á „Nýtt“.
3. Sláið inn gildi í reitinn Stefnuheiti.
4. Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðareiningar.
    * Velja stigveldi stefnunnar sem nýverið var stofnuð.  
5. Sláið inn eða veljið gildi í reitnum Stigveldi víddar kostnaðarhlutar.
    * Velja Fyrirtæki  
6. Smellið á „Vista“.
7. Smellið á „Nýtt“.
8. Í listanum skal merkja valda línu.
9. Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðareiningar.
    * Útvíkka stigveldið til að velja Breytilegur kostnaður.  
10. Sláið inn eða veljið gildi í reitnum Stigveldishnútur víddar kostnaðarhlutar.
    * Að sjálfgefnu er prósentan í breytilegu 100 prósent.  
11. Smella á Regluúthlutanir fyrir kostnaðarstýringareiningu.
12. Smellið á „Nýtt“.
13. Í listanum skal merkja valda línu.
14. Færa skal inn dagsetningu í reitinn Gildir frá dagsetningu reikningsskila.
    * Reglurnar stjórnast af dagsetningum, og getur notandi eða kerfið látið reglurnar renna út ef nýrri útgáfa er stofnuð.  
15. Í reitinn Kostnaðarstýringareining skal slá inn eða velja gildi.
16. Smellið á „Vista“.

