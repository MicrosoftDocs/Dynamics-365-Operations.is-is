--- 
title: "Stofna kanban-reglu til að koma í staðinn"
description: "Þetta ferli leggur áherslu á kanban-regla er skipt út nýja kanban-reglu á tiltekinni dagsetningu."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e5b27200a8d56192d473887f01076eced0f92e4c
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-replacement-kanban-rule"></a>Stofna kanban-reglu til að koma í staðinn

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli leggur áherslu á kanban-regla er skipt út nýja kanban-reglu á tiltekinni dagsetningu. Þetta er gagnlegt þegar breytingar í framleiðsluflæðis eða áfylling reglur þarf að samræmdur og raða. Sýnifyrirtæki til að stofna þetta ferli er USMF. Þetta ferli er ætluð fyrir ferlishönnuð eða virðisstraumsstjóra þegar þeir undirbúa framleiðslu fyrir breytt framleiðsluflæði eða nýja áfyllingarreglu. Þetta verk kemur í stað 000022 kanban-reglu með nýja reglu og eykur hámarksmagn úr 48 í 100 fyrir nýju reglunnar.


## <a name="select-a-kanban-rule-to-replace"></a>Veljið kanban-regluna til að skipta út.
1. Fara á kanban-reglur.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Velja kanban-reglu 000022.  

## <a name="create-a-replacement-kanban-rule"></a>Stofna kanban-reglu til að koma í staðinn
1. Smella á Skipta út kanban-reglu
2. Færa inn dagsetningu og tíma í svæðinu gildisdagsetningu.
    * Veldu dagsetningu í framtíðinni, eins og eina viku frá núna. Þetta er dagsetning og tími þegar nýja kanban-regla verður virk og kemur í stað gömlu kanban-regla.  
    * Ef kanban-reglu breytir slóðina í framleiðsluflæði er hægt að velja annan verkþátt.  Í þessu ferli munu verkþætti helst óbreytt.  
3. Smellið á „Í lagi“.
    * Athugaðu að nýja kanban-regla er stofnuð til að koma í stað kanban-regla 000022.  
    * Gildisdagsetning er stillt samkvæmt dagsetningu sem valin er þegar þú skiptir um kanban-regla.  
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Veljið 000022 útskipt kanban-regluna.  
    * Athugaðu að útskipta kanban-regla hefur sama dagsetning og lokadagsetning vegna þess að þetta er dagsetningin þegar hún mun renna út.  
5. Í listanum skal velja línu 1.
    * Veljið nýja kanban-reglu efst á listann. Þetta er kanban-regla með hæsta kanban-reglunúmer.  
6. Í listanum skal smella á tengilinn í valinni línu.
    * Smellið á númer kanban-reglu sem opna kanban-reglu.  

## <a name="modify-maximum-quantity-for-the-replacement-kanban-rule"></a>Breyta hámarksmagn fyrir staðgengil kanban-reglu
1. Setja hámarksmagn á "100".
    * Útvíkka flýtiflipann Magn til að sjá svæðið Hámarksmagn. Hámarksmagni breytt í 100 leyfir allt að 100 kanbans að vera vinna.    Þetta er síðasta skrefið í þessu verkefni.  


