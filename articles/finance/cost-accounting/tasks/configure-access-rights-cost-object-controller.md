---
title: Skilgreina aðgangsréttindi stjórnborðs kostnaðarhlutar
description: Nota þetta ferli til að skilgreina aðgangsréttindi eftirlitsmanns kostnaðarhlutar.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4b50782c7a1b69b6953c65d6df155f003028333
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444530"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a>Skilgreina aðgangsréttindi stjórnborðs kostnaðarhlutar

[!include [banner](../../includes/banner.md)]

Nota þetta ferli til að skilgreina aðgangsréttindi eftirlitsmanns kostnaðarhlutar. Þessi skráning notar USP2-sýnigagnafyrirtæki.


## <a name="assign-the-cost-object-controller-role"></a>Úthluta hlutverkinu Eftirlitsmaður kostnaðarhlutar
1. Farið í Kerfisstjórnun > Notendur > Notendur.
2. Nota flýtiafmörkun til að finna færslur Til dæmis, sía á svæðið Notendanafn með gildinu „Alicia“.
3. Í listanum skal smella á tengilinn í valinni línu.
4. Smellt er á Úthluta hlutverkum.
5. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
6. Smellið á „Í lagi“.

## <a name="enable-access-list-security"></a>Virkja öryggisatriði aðgangslista
1. Fara í kostnaðarbókhald > Víddir > Stigveldi vídda.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Velja Fyrirtæki  
3. Smellið á „Breyta“.
4. Veljið Já í svæðinu Stigveldi aðgangslista
5. Smella á Skoða stigveldi

## <a name="assign-access-rights-to-user"></a>Úthluta Aðgangsréttindum til notanda
1. Smellið á „Nýtt“.
2. Í listanum skal merkja valda línu.
3. Í reitinn Kenni notanda skal slá inn eða velja gildi.
    * Velja Stjórn.  
4. Í trénu skal velja „Fyrirtæki\CEO\CFO\FIM“.
5. Smellið á „Nýtt“.
6. Í listanum skal merkja valda línu.
7. Í reitinn Kenni notanda skal slá inn eða velja gildi.
    * Velja Alicia.  
8. Smellið á „Vista“.

## <a name="enable-access-rights-in-cost-accounting"></a>Virkja Aðgangsréttindi í kostnaðarbókhaldi
1. Fara í kostnaðarbókhald > Uppsetning > Færibreytur.
2. Smellið á flipann „Almennt“.
3. Velja Já í reitnum Virkja skoðunaraðgang fyrir víddarstök kostnaðarhlutar.
4. Smellið á „Vista“.
5. Lokið síðunni.
6. Fara í kostnaðarbókhald > Uppsetning > kostnaðarstýring vinnusvæði skilgreining.
7. Smellið á „Breyta“.
8. Veljið Já í svæðinu Útgefið.
    * Ef þú velur Já, getur notandi sem er úthlutað einu af fjórum eftirfarandi hlutverkum séð skýrslur í Vinnusvæði kostnaðarstýringar: Stjórnandi kostnaðarbókhalds, endurskoðandi kostnaðar, afgreiðslustarfsmaður endurskoðanda kostnaðar, og eftirlitsmaður kostnaðarhluta. Ef þú velur Nei, getur aðeins notandi sem er úthlutað einu af fjórum eftirfarandi hlutverkum séð skýrslurnar: Stjórnandi kostnaðarbókhalds, endurskoðandi kostnaðar, og afgreiðslustarfsmaður endurskoðanda kostnaðar.    
9. Smellið á „Vista“.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]