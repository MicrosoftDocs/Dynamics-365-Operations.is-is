--- 
title: "Lean-þarfarakning úr sölupöntun"
description: "Þetta ferli leggur áherslu á villuleit fyrir þarfarakningartré úr sölulínu þar sem varan er framleidd með kanban."
author: ChristianRytt
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: 974dc11c2421f8399efa0ca0e6be53535c10f7fb
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---
# <a name="lean-pegging-from-sales-orders"></a>Lean-þarfarakning úr sölupöntun

[!include[task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli leggur áherslu á villuleit fyrir þarfarakningartré úr sölulínu þar sem varan er framleidd með kanban. Eftir villuleit fyrir þarfarakningartré, eru allar kanban-vinnslur áætlaðar. Þetta er gagnlegt fyrir pöntunaraðstæður þar sem pöntunarviðtaki þarf að tryggja að framleiðslan getur hafist strax. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta ferli er ætluð fyrir þróaðan viðtakanda pöntunar sem vinnur í lean fyrirtæki.


## <a name="create-a-sales-order-for-a-kanban-controlled-item"></a>Stofna sölupöntun fyrir kanban sem er stýrt af vöru
1. Fara í Allar sölupantanir.
2. Smellið á „Nýtt“.
3. Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.
    * Nota US-001.  
4. Smellið á „Í lagi“.
5. Sláið inn „L0001“ á svæðinu „Vörunúmer“.
6. Stillið magn á „30“.
    * Það er mikilvægt að magnið er hærra en 24 til að virkja tilviksreglur kanbans.  

## <a name="open-a-pegging-tree"></a>Opna í þarfarakningartré 
1. Smellt er á Afurð og framboð.
2. Smellt er á Skoða þarfarakningartré.
    * Athugið að fyrir þarfarakningartré sýnir öll þarfarakning þarf fyrir línu í sölupöntun. Í þessu tilfelli eru tveimur stigum kanbana og allir nauðsynlegir íhlutir.  

## <a name="plan-the-pegging-tree"></a>Áætla þarfarakningartré
1. Í trénu, skal velja sölulína ' 000832\Kanban 000558'.
2. Útvíkka hlutann Kanban vinnslur.
    * Athugið að stöðu vinnsla fyrir kanban-vinnsla er Ekki áætluð.  
3. Smellt er á Áætlun alls þarfarakningartré.
    * Þetta mun áætla allar vinnslur kanban í þarfarakningartré, og breytir stöðunni úr er Ekki áætluð í Vinnsla Áætluð.  
4. Endurhlaðið síðuna.
    * Athugið að stöðu kanban var breytt úr Ekki áætluð í áætlað.  
5. Veljið í trénu 'Sölulínu 000832\Kanban 000558\útgáfa fyrir L0001\Kanban 000559'.
    * Vinnslan fyrir kanban-vinnslan númer tvö er líka áætlaðar, þar sem allt þarfarakningartré er áætluð. Athugið að stöðu kanban var breytt úr Ekki áætluð í áætlað.  


