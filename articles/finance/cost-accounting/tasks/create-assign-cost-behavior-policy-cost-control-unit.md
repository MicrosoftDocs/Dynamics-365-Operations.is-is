---
title: Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu
description: Kostnaður er flokkaður út frá kostnaðarhegðun sem annað hvort fastur eða breytilegur.
author: twheeloc
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMCostBehaviorRule
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 653bfb69c4ca118c700755cb95a6b349d2c6bbad
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735143"
---
# <a name="create-and-assign-a-cost-behavior-policy-to-a-cost-control-unit"></a>Stofna og úthluta kostnaðarhegðunarreglu fyrir kostnaðarstýringareiningu

[!include [banner](../../includes/banner.md)]

Kostnaður er flokkaður út frá kostnaðarhegðun sem annað hvort fastur eða breytilegur. Stefna og samsvarandi reglur er úthlutað til kostnaðarstýringareiningar svo stefnan taki gildi. Nota þetta ferli til að stofna stefnu og síðan úthluta stefnunni til kostnaðarstýringareiningar


## <a name="create-a-cost-behavior-hierarchy"></a>Stofna Stigveldi kostnaðarhegðunar
1. Fara í **Kostnaðarbókhald > Víddir > Stigveldi vídda**.
2. Smellt er á **Nýtt**.
3. Smellið á **Stofna**.
4. Í reitinn **Heiti víddarstigveldis** skal slá inn „Stigveldi kostnaðarhegðunar“.
5. Sláið inn eða veljið gildi í reitnum **Vídd**.
    * Velja kostnaðareiningar  
6. Smelltu á **Vista**.
7. Smelltu á **Skoða stigveldi**.
8. Smellt er á **Nýtt**.
9. Í svæðið **Heiti hnútar**, færðu inn gildi.
    * Færa inn Fastan kostnað.  
10. Í trénu skal velja „Stigveldi kostnaðarhegðunar“.
11. Smellt er á **Nýtt**.
12. Í svæðið **Heiti hnútar**, færðu inn gildi.
    * Færa inn breytilegur kostnaður.  
13. Smelltu á **Vista**.
14. Í trénu skal velja „stigveldi kostnaðarhegðunar\Fastur kostnaður“.
15. Smellt er á **Nýtt**.
16. Í listanum skal merkja valda línu.
17. Sláið inn eða veldu gildi í reitnum **Frá víddarstak**.
    * Afmörkun víddarstaks getur innihaldið gloppur, en stökin geta ekki skarast.  
18. Sláið inn eða veldu gildi í reitnum í **Til víddarstaks**.
    * Afmörkun víddarstaks getur innihaldið gloppur, en stökin geta ekki skarast.  
19. Í trénu skal velja „stigveldi kostnaðarhegðunar\Breytilegur kostnaður“.
20. Smellt er á **Nýtt**.
21. Í listanum skal merkja valda línu.
22. Sláið inn eða veldu gildi í reitnum **Frá víddarstak**.
    * Afmörkun víddarstaks getur innihaldið gloppur, en stökin geta ekki skarast.  
23. Sláið inn eða veldu gildi í reitnum í **Til víddarstaks**.
    * Afmörkun víddarstaks getur innihaldið gloppur, en stökin geta ekki skarast.  
24. Smelltu á **Vista**.

## <a name="create-the-policy-and-rules"></a>Stofna stefnu og reglur
1. Fara í **Kostnaðarbókhald > Stefnur > Stefnur fyrir kostnaðarhegðun**.
2. Smellt er á **Nýtt**.
3. Sláið inn gildi í reitinn **Stefnuheiti**.
4. Sláið inn eða veljið gildi í reitnum **Víddarstigveldi kostnaðareiningar**.
    * Velja stigveldi stefnunnar sem nýverið var stofnuð.  
5. Sláið inn eða veljið gildi í reitnum **Stigveldi víddar kostnaðarhlutar**.
    * Velja Fyrirtæki  
6. Smelltu á **Vista**.
7. Smellt er á **Nýtt**.
8. Í listanum skal merkja valda línu.
9. Sláið inn eða veljið gildi í reitnum **Hnútur á víddarstigveldi kostnaðareiningar**.
    * Útvíkka stigveldið til að velja Breytilegur kostnaður.  
10. Sláið inn eða veljið gildi í reitnum **Stigveldishnútur víddar kostnaðarhlutar**.
    * Að sjálfgefnu er prósentan í breytilegu 100 prósent.  
11. Smella á **Regluúthlutanir fyrir kostnaðarstýringareining** u.
12. Smellt er á **Nýtt**.
13. Í listanum skal merkja valda línu.
14. Færa skal inn dagsetningu í reitinn **Gildir frá dagsetningu reikningsskila**.
    * Reglurnar stjórnast af dagsetningum, og getur notandi eða kerfið látið reglurnar renna út ef nýrri útgáfa er stofnuð.  
15. Í reitinn **Kostnaðarstýringareining** skal slá inn eða velja gildi.
16. Smelltu á **Vista**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
