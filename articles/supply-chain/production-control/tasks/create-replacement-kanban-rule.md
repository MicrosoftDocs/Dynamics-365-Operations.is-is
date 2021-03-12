---
title: Stofna kanban-reglu til að koma í staðinn
description: Þetta ferli leggur áherslu á kanban-regla er skipt út nýja kanban-reglu á tiltekinni dagsetningu.
author: ChristianRytt
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d68087afd1a0c9b675e4ac1ef2118e6aab5213d9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4998654"
---
# <a name="create-a-replacement-kanban-rule"></a>Stofna kanban-reglu til að koma í staðinn

[!include [banner](../../includes/banner.md)]

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

