--- 
title: "Stofna kanban í föstu magni fyrir framleiðslu"
description: "Þetta ferli leggur áherslu á uppsetningu sem þarf til að stofna fasta kanban-reglu framleiðslu til að kveikja umbreytingarverkþætti, á vinnuflokk, í lean-umhverfi."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8020a37bf0c725fc260574cfe87861aeb017519e
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-fixed-quantity-kanban-rule-for-manufacturing"></a>Stofna kanban í föstu magni fyrir framleiðslu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli leggur áherslu á uppsetningu sem þarf til að stofna fasta kanban-reglu framleiðslu til að kveikja umbreytingarverkþætti, á vinnuflokk, í lean-umhverfi. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta ferli er ætlað fyrir Ferlishönnuð eða Virðisstraumsstjóra, þar sem þau undirbúa framleiðslu nýja eða breytta afurðar.


## <a name="create-new-kanban-rule"></a>Stofna nýja kanban-reglu
1. Fara á kanban-reglur.
2. Smellið á „Nýtt“.
    * Athugaðu að sjálfgefin gerð er Framleiðsla og Áfyllingaráætlun er Fast. Ekki þarf að breyta þessum færibreytum.  
3. Færa inn eða velja gildi í reitnum Fyrsta áætlun verkþáttarins.
    * Þetta er verkþátturinn sem verður að framkvæma fyrir kanbön stofnuð byggt á þessari kanban-reglu.  Veljið 'SpeakerTestAndPackaging'.  
4. Útvíkka hlutann Upplýsingar.
5. Sláðu inn eða veldu gildi í reitnum Afurð.
    * Veldu L0050.  
6. Færðu inn eða veldu gildi í reitnum Mælieining.
    * Veljið mínútur.  
7. Í reitinn Afhendingartími skal slá inn númer.
    * Færðu inn 5.  

## <a name="set-quantities"></a>Stilla magn
1. Útvíkka hlutann Magn.
2. Stilla Sjálfgefið magn á '10'.
    * Þetta er magnið sem verður flutt fyrir hverja kanban.  
3. Veldu gátreitinn Frávik afurðarmagns.
    * Með þessu er hægt að ljúka völdum kanbönum með frávik úr sjálfgefnu magni.  Til að leyfa að kanbönum sé lokið með magn frá 8 til 12 þarf að stilla bæði frávik á 2.  
4. Stilla frávik fyrir neðan á ‚2‘.
    * Þetta leyfir að lokið sé niður að 10 - 2 = 8  
5. Stilla frávik að ofan á ‚2‘.
    * Þetta leyfir að lokið sé allt að 10 + 2 = 12  
6. Færið inn tölu í reitnum Kanban í Föstu magni.
    * Þetta er upphæð kanbana sem á að vera virk. Í þessu tilfelli vinna 5 kanban 10 hvert um sig.  
7. Í reitnum Lágmark viðvörunarmarka skal færa inn ‚2‘.
    * Notað til að fylgjast með lágmarksupphæð fullra kanbana sem eiga að vera á ákvörðunarstað. Þetta er til dæmis notað á yfirlit yfir magn kanbans.  
8. Í reitnum Hámark viðvörunarmarka skal færa inn ‚4‘.
    * Notað til að fylgjast með hámarksupphæð fullra kanbana sem eiga að vera á ákvörðunarstað. Þetta er til dæmis notað á yfirlit yfir magn kanbans.  
9. Í reitnum Sjálfvirkt áætlunarmagn skal færa inn ‚1‘.
    * Ef þetta er stillt á 1 þýðir það að hvert kanban verður sjálfkrafa áætlað.   Ef 3 var fært inn verða kanban ekki áætluð fyrr en 3 tóm kanban eru tilbúin til áætlunar. Þetta er gagnlegt fyrir flokkunarvinnu og til að forðast of mikla uppsetningu.  

## <a name="create-kanbans"></a>Stofna kanban
1. Útvíkkar kanban-hlutann.
2. Smellið á „Vista“.
    * Vista þarf kanban-regluna vista áður en hægt er að stofna kanban.  
3. Smelltu á Bæta við.
    * Athugaðu að það eru engin virk kanban, þess vegna er ráðlagður „Fjöldi nýrra kanbana“ 5. Þetta er jafnt og „Fast kanban-magn“.  
4. Smellið á „Stofna“.
    * Þetta stofnar 5 kanbana.  
    * Athugið að 5 kanbön, fyrir hver 10, voru stofnuð fyrir þessa kanban-reglu framleiðslu. Þetta er síðasta skrefið í þessu ferli.  


