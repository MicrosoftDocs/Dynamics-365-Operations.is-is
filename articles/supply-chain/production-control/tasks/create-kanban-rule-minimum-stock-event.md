---
title: Stofna kanban-reglu með lágmarksbirgðatilviki
description: Þetta ferli leggur áherslu á uppsetningu sem þarf til að stofna kanban-regla með því að nota tilvik lágmarksbirgða til að tryggja að tiltekinni vöru sé alltaf tiltækt á tiltekinn stað.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanRules, LeanProductionFlowActivityLookup, InventItemIdLookupSimple, EcoResProductInformationDialog, EcoResProductDetailsExtended, ReqItemTable, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bd7e02a8a3bf62606c680dad91d46658775138df
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/29/2021
ms.locfileid: "7566624"
---
# <a name="create-a-kanban-rule-using-a-minimum-stock-event"></a>Stofna kanban-reglu með lágmarksbirgðatilviki

[!include [banner](../../includes/banner.md)]

Þetta ferli leggur áherslu á uppsetningu sem þarf til að stofna kanban-regla með því að nota tilvik lágmarksbirgða til að tryggja að tiltekinni vöru sé alltaf tiltækt á tiltekinn stað. Kanban-regla er stofnuð til að flytja efni til staðsetningar þegar birgðastigið fer niður fyrir 200 stykki. Með því að keyra vinnslu þarfarakningartilviks, eru nauðsynleg kanbön stofnaðar. Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF. Þetta verkefni er ætlað fyrir Ferlishönnuð eða Virðisstraumsstjóra, þar sem þau undirbúa framleiðslu nýja eða breytta afurðar í lean-umhverfi.


## <a name="create-a-new-kanban-rule"></a>Stofna nýja kanban-reglu
1. Farið í upplýsingar um afurðarstjórnun > Lean-framleiðsla > Kanban-reglur.
2. Smellið á „Nýtt“.
3. Veljið í svæðinu gerð „afturköllun".
    * Þessi gerð er notuð til að stofna flutnings kanban.  
4. Velja 'Tilvik' í reitnum Áfyllingaráætlun.
    * Tilviksáætlunin er notuð til að stofna flutnings kanban byggt á tilviki. Seinna í ferlinu, muntu virkja flytnings kanban með því að nota birgðaáfyllingar.  
5. Færa inn eða velja gildi í reitnum Fyrsta áætlun verkþáttarins.
    * Sláið inn eða Veljið ReplenishSpeakerComponents. Þessi flutningsverkþátt hefur innhreyfingar (úttak) vöruhús og staðsetning 12, sem þýðir að efni verður að flytja staðsetning 12 í vöruhúsi 12.  
6. Útvíkka hlutann Upplýsingar.
7. Sláðu inn eða veldu gildi í reitnum Afurð.
    * Veldu M0007.  
8. Útvíkka hlutann Tilvik.
9. Í reitnum tilvik birgðaáfyllingar, skal velja ‚runa.
    * Þetta stofnar Kanban til að uppfylla efnisþörfum tengdri staðsetningu meðan stendur á vinnsla Þarfarakningartilvika.  

## <a name="set-the-minimum-quantity-for-the-item"></a>Stilltu Lágmarksmagn vöru
1. Smellið til að elta tengilinn í reitnum afurð.
2. Smellið til að elta tengilinn í reitnum vörunúmer.
3. Útvíkka Upplýsingakassa mynd Afurðar.
4. Smellið á „Áætlun“ á aðgerðarúðunni.
5. Smellt er á vöruþekju.
6. Smellið á „Nýtt“.
7. Í listanum skal merkja valda línu.
8. Sláðu inn eða veldu gildi í reitnum Vöruhús.
    * Stilltu Vöruhús á 12.  
9. Lágmark er stillt á "200".

## <a name="run-the-batch-event-creation-job"></a>Keyra vinnsluna stofnun runutilviks
1. Fara í Framleiðslustýringar > Reglubundin verkefni > Runuvinnsla Kanban-vinnslu > Vinnsla þarfarakningartilvika.
2. Smellið á „Í lagi“.
3. Farið í upplýsingar um afurðarstjórnun > Lean-framleiðsla > Kanban-reglur.
4. Í listanum skal smella á tengilinn í valinni línu.
    * Velja kanban-reglu sem áður var stofnuð.  
5. Útvíkkar kanban-hlutann.
    * Athugið að búinn var til kanban til að flytja nauðsynlegt efni í vöruhús 12 .  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]