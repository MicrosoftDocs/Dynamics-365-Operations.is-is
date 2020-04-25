---
title: Bakfæra stöðu kanban-vinnslu
description: Þetta ferli leggur áherslu á skipti aftur rangt staða kanban-vinnsla.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell, KanbanJobStatusUpdate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: adf65175669d4cd5ec4cb431a7e1436ea3da83ed
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3210507"
---
# <a name="revert-kanban-job-status"></a>Bakfæra stöðu kanban-vinnslu

[!include [banner](../../includes/banner.md)]

Þetta ferli leggur áherslu á skipti aftur rangt staða kanban-vinnsla. Þetta er gagnlegt í tilfellum starfsmaður á vél uppfærir röng vinnslu eða stillir ranga stöðu fyrir mistök. Í þessu ferli kanban-vinnsla er skráð sem undirbjó fyrir mistök og stöðu hefur verið snúa aftur. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF. Þetta ferli er ætluð fyrir verkstæðisstjóri eða starfsmaður á vél í lean-framleiðsla fyrirtæki.


## <a name="open-process-board-for-the-work-cell"></a>Opna ferilspjald fyrir vinnuflokki
1. Fara í Kanban-spjald fyrir vinnslukenni verks
2. Sláið inn eða veldu gildi í reitnum vinnuflokkur.
    * Velja vinnuflokkur 1260.  

## <a name="prepare-kanban-job"></a>Undirbúa kanban-vinnslu
1. Smellt er á Undirbúa.
    * Ef ekki er hægt að smella á Undirbúa þar sem hún er grátóna, ganga úr skugga um að valin kanban-vinnsla hefur stöðuna Áætlaðar, sem er tilgreind með því tóma kanban-tákn. Ef ekki tekst að Undirbúa, ganga úr skugga um að allt efni í tiltektarlistanum eru tiltækar.  
2. Á listanum, veljið undirbúin vinnslu.
    * Veljið vinnsluna sem hefur nýlega verið undirbúið.  
    * Athugið að staða vinnslur er undirbúin, sem er tilgreint með þríhyrningur innan kanban-tákn.  

## <a name="revert-the-status-of-the-prepared-kanban-job"></a>Snúa aftur stöðu undirbúin kanban-vinnslu
1. Í listanum skal merkja valda línu.
    * Veljið fyrsta vinnslan sem var undirbúin.  
2. Í aðgerðasvæðinu er smellt á framleiðsla
3. Smellt er á stöðu snúa aftur.
    * Hægt er að nota annarri kanban-reglu þegar eftirfarandi skilyrði eru sönn:-áfyllingaráætlun er sama fyrir bæði reglur.  - Útgáfa framleiðsluflæði er það sama fyrir bæði reglur.  - Afurð sem er uppgefið er það sama fyrir bæði reglur.  - Niður á við verkþætti sem eru skilgreind fyrir síðustu aðgerð kanban-reglur verður að vera það sama fyrir bæði reglur.  - Skilgreina verður sama uppgefin birgðavíddir fyrir báðar reglurnar.  - Staða afgreiðslueiningar verður að vera Ekki úthlutað.  - Skilgreining fyrir tilvikskanbön verður að vera það sama.  
    * Tryggja skal að nýja staðan er Áætluð.  
4. Smellið á „Í lagi“.
5. Í listanum skal afmerkja valda línu.
    * Velja sömu vinnslu.  
    * Athugið staða vinnslu fyrir kanban-vinnsla hefur verið breytt í áætlað, sem er tilgreind með tómu kanban tákn.  

