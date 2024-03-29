---
title: Bæta útreikningsreglu kanban-magns við kanban-reglu
description: Þetta ferli leggur áherslu á stofnun útreikningsstefnu kanban-magns og henni er bætt við kanban-reglu til að besta stærðar og magn kanban.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanQuantityPolicy, KanbanRules, KanbanQuantityCalculation
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a844d455b1e583f234ddc47280f5cac8ee0ab852
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579281"
---
# <a name="add-a-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Bæta útreikningsreglu kanban-magns við kanban-reglu

[!include [banner](../../includes/banner.md)]

Þetta ferli leggur áherslu á stofnun útreikningsstefnu kanban-magns og henni er bætt við kanban-reglu til að besta stærðar og magn kanban. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta ferli er ætlað fyrir virðisstraumsstjóra. Þetta ferli er skilyrði til að stofna ferlið Reikna tillögur kanban-magns. 


## <a name="create-a-kanban-quantity-calculation-policy"></a>Stofna útreikningsreglu fyrir kanban-magn
1. Fara í Framleiðslustýringar > Reglubundin verkefni > Útreikning kanban-magns > Útreikningsreglur kanban-magns.
2. Smellið á „Nýtt“.
3. Í reitinn Heiti skal slá inn gildi.
    * Til dæmis, skráið Speaker2016.  
4. Í aðaláætlunarreitnum skal smella á fellilistahnappinn til að opna leitina.
5. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Veljið StaticPlan til að reikna út eftirspurn.  
6. Í listanum skal smella á tengilinn í valinni línu.
7. Smellið á „Vista“.
8. Í svæðinu Lágmarks kanban-magn, færið inn '1'.
    * Þetta er aukanúmer kanbana sem er innifalið í útreikningi kanban-magns.  
9. Setja öryggisstuðull á "1".
    * Þetta er the stuðull sem er notað í a‘ reikna út aukalegt magn öryggisbirgða.  
10. Í dagar fram í tímann svæðinu, færið inn '30'.
    * Þetta er fjöldi daga fyrir dagsetningu útreiknings fyrir kanban-magn sem er innifalið í útreikningi eftirspurnar.  
11. Færið inn '30' í Dagar aftur í tímann.
    * Þetta er fjöldi daga eftir dagsetningu útreiknings fyrir kanban-magn sem er innifalið í útreikningi eftirspurnar.  Formúla notuð við útreikning er sýnd með raungildin. Fyrir dæmi, Kanban-magn = ((meðaltals dagleg eftirspurn x afhendingartími x 2,00) / Afurðarmagn per efnismeðhöndlunareining) + 1  
12. Lokið síðunni.

## <a name="add-the-kanban-quantity-calculation-policy-to-a-kanban-rule"></a>Bæta útreikningsreglu kanban-magns við kanban-reglu
1. Farið í upplýsingar um afurðarstjórnun > Lean-framleiðsla > Kanban-reglur.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Velja kanban-reglu 000020 fyrir þetta ferli.  
3. Í listanum skal smella á tengilinn í valinni línu.
4. Víxla útvíkkun á hluta útreikningsreglur um kanban-magn.
5. Smelltu á Bæta við.
    * Bæta við útreikningsstefnu kanban-magns sem stofnuð hefur verið nýlega í fyrra undirverki.  
6. Í listanum skal merkja valda línu.
7. Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.
8. Í listanum skal smella á tengilinn í valinni línu.
    * Velja reglu fyrir Speaker2016 hafa nýverið var stofnuð í fyrri undirverki.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]