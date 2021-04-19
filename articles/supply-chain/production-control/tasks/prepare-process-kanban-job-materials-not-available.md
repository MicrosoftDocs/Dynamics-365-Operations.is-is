---
title: Undirbúa kanban-vinnslu ferlis þegar efni er ekki tiltækt fyrir vinnuflokk
description: Þetta ferli leggur áherslu á undirbúning kanban-vinnslu þegar einhver hráefni eru ekki tiltækar fyrir vinnuflokkur, þar af leiðandi nauðsynlegt er að taka til efni úr vöruhúsi.
author: ChristianRytt
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72fd083edc48504b35f540ea7bdc8c8c736418f3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828635"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-not-available-for-the-work-cell"></a>Undirbúa kanban-vinnslu ferlis þegar efni er ekki tiltækt fyrir vinnuflokk

[!include [banner](../../includes/banner.md)]

Þetta ferli leggur áherslu á undirbúning kanban-vinnslu þegar einhver hráefni eru ekki tiltækar fyrir vinnuflokkur, þar af leiðandi nauðsynlegt er að taka til efni úr vöruhúsi. Ferli "Undirbúa á kanban-vinnslu þegar efni er tiltækt" er skilyrði fyrir stofnun þetta ferli. Þetta ferli er ætluð fyrir á starfsmaður á vél. Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.

1. Fara í Framleiðslustýring > Kanban > Kanban-spjald fyrir ferlisvinnslur.
2. Í reitnum vinnuflokkur skal smella á fellilistahnappinn til að opna leitina.
3. Í listanum skal smella á tengilinn í valinni línu.
    * Velja vinnuflokkur 1250.  
4. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Velja Kanban 000356.  
5. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Í listanum skal afvelja línu 4. eða Velja línu 4 ef þú hefur ekki lokið verkefninu "Undirbúa á kanban-vinnslu þegar efni er tiltækt."  
6. Víxla útvíkkun á liðnum tiltektarlisti.
    * Táknið Engin færsla í birgðastaða gefir til kynna að 48 ea fyrir vöru P0002 vantar fyrir vinnuflokkur.  

## <a name="transfer-materials-to-work-cell"></a>Flytja efni til vinnuflokkur
1. Víxla útvíkkun á liðnum millifærsla vinnslu.
2. Notið flýtiafmörkun til að sía á vörunúmerasvæðinu með gildinu „P0002“.
3. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
4. Smellið á „Byrja“.
    * Flutningur er í gangi.  
5. Smelltu á Ljúka.
    * Nú er tiltækur á tiltektarlista kanban-vinnslu P0002 vöru. Þetta þýðir að við getum undirbúa kanban með öllum nauðsynlegum efni.  
6. Smellt er á Undirbúa.
    * Athugið að tákn í vinnslustöðu tilgreinir vinnslan er nú tilbúið.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]