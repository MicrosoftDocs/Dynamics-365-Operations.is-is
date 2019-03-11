---
title: Stofna kanban-regla sölutilviks
description: Þetta ferli leggur áherslu á uppsetningu sem þarf til að stofna kanban-reglu sem er ræst við stofnun sölupöntunar.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, SalesTableListPage, SalesCreateOrder, SalesTable, LeanPeggingTree
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d2bee6e81acd029406c95237f0b4ba4ab2565ea1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "342018"
---
# <a name="create-a-sales-event-kanban-rule"></a>Stofna kanban-regla sölutilviks

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli leggur áherslu á uppsetningu sem þarf til að stofna kanban-reglu sem er ræst við stofnun sölupöntunar. Tilviksreglur kanbans fylla á kröfur sem eiga upphaf sitt í sölupöntunarlínum. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Það er ætlað fyrir ferlishönnuð eða virðisstraumsstjóra þegar þeir undirbúa framleiðslu nýrrar eða breyttrar afurðar.




## <a name="create-a-new-kanban-rule"></a>Stofna nýja kanban-reglu
1. Fara á kanban-reglur.
2. Smellið á „Nýtt“.
3. Velja 'Tilvik' í reitnum Áfyllingaráætlun.
    * Velja Tilvik þýðir kanban-reglan er ræst með tilviki, til dæmis stofnun sölupöntunarlínu.   Þessu er beitt á svæðum þar sem hvert kanban á að ná yfir tiltekna eftirspurn.  
4. Færa inn eða velja gildi í reitnum Fyrsta áætlun verkþáttarins.
    * Velja Lokasamsetningu.  
5. Útvíkka hlutann Upplýsingar.
6. Sláðu inn eða veldu gildi í reitnum Afurð.
    * Veldu L0050.  

## <a name="define-an-event"></a>Skilgreina tilvik
1. Útvíkka hlutann Tilvik.
2. Í reitnum Sölutilvik skal velja ‚Sjálfvirkt‘.
    * Með því að velja sölutilvikið Sjálfvirkt verður þessi kanban-regla ræst sjálfkrafa þegar sölulína samræmist staðsetningu afurðar og móttöku. Í þessu ferli er afurð L0050 í vöruhúsi 13.  
3. Stilla lágmarksmagn tilviks á ‚50‘.
    * Með lágmarksmagni tilviks upp á 50 verður kanban-reglan aðeins ræst af tilvikum með magninu 50 eða meira.  
4. Útvíkka hlutann Framleiðsluflæði.
    * Athugaðu að staðsetning Innhreyfinga er vöruhús 13. Þetta þýðir að þessi kanban-regla verður ræst fyrir þessa staðsetningu.  
    * Í þessu dæmi mun sölulína fyrir afurð L0050, með magni 50 eða fleiri á vöruhúsi 13, virkja þessa kanban-reglu.  

## <a name="create-sales-line-to-trigger-event-kanban-rule"></a>Stofna sölulínur til að kveikja tilviksreglur kanbans
1. Fara í Allar sölupantanir.
    * Viðvörun birtist þegar kanban-reglan er vistuð, sem þýðir að það verður að stofna kanban í rauntíma við stofnun sölupöntunar.  
2. Smellið á „Nýtt“.
3. Færa inn eða veljið gildi í svæðinu Reikningur viðskiptavinar.
    * Veljið til dæmis US-003.  
4. Smellið á „Í lagi“.
5. Sláið inn „L0050“ á svæðinu „Vörunúmer“.
6. Ritað er ‚1‘ í reitnum Svæði.
    * Veljið Svæði 1 þar sem Vöruhús 13 er á Svæði 1.  
7. Sláðu inn eða veldu gildi í reitnum Vöruhús.
    * Stilltu Vöruhús á 13.  
8. Stillið magn á „75“.
    * Færið inn magn 50 eða hærri til að virkja stofnaða kanban-reglu.  

## <a name="verify-that-kanban-is-created"></a>Staðfestið að kanban sé stofnað
1. Smellt er á Afurð og framboð.
2. Smellt er á Skoða þarfarakningartré.
    * Athugið að kanban með sama magni og sölulínan var stofnað. Einnig er hægt að skoða efni sem þarf til að framleiða L0050. Þetta er síðasta skrefið í þessu ferli.  

