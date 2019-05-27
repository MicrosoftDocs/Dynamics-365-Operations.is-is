---
title: Reikna afskriftir eigna milli lögaðila
description: Hægt er að keyra eignaafskriftir á milli lögaðila í einu skrefi.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetParameters, AssetProposalDepreciation, DefaultDashboard, LedgerJournalTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b2575354af322827972ffa650e9c732170c5a6eb
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566544"
---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Reikna afskriftir eigna milli lögaðila

[!include [task guide banner](../../includes/task-guide-banner.md)]

Hægt er að keyra eignaafskriftir á milli lögaðila í einu skrefi. Þessi aðferð sýnir hvernig skal setja upp og keyra ferlið fyrir marga lögaðila. Það notar Bókari hlutverk og sýnigögn fyrir USMF lögaðila.


## <a name="set-up-cross-company-depreciation-run-journals"></a>Setja upp færslubókakeyrslu afskrifta á milli fyrirtækja
1. Fara í Eignir > Uppsetning > Færibreytur eigna.
2. Útvíkka eignatillagnahlutann.
3. Smelltu á Bæta við.
4. Sláið inn eða veldu gildi í reitnum bókunarlag.
5. Sláið inn eða veljið gildi í reitnum heiti færslubókar.
    * Endurtaka uppsetning færslubókar á síðunni Færibreytur eigna fyrir hverjum lögaðila.  

## <a name="depreciation-run"></a>Afskriftarkeyrsla
1. Fara í Eignir > Færslubókarfærslur > Stofna afskriftartillögu.
2. Sláið inn eða veldu gildi í reitnum bókunarlag.
    * Færslubókarnafnið mun verða sjálfgefið úr Færibreytum eigna. Því er hægt að breyta hér fyrir núgildandi lögaðila.  
3. Í reitinn Til dagsetningar skal slá inn dagsetningu.
    * Veljið lögaðilana sem á að hafa með í afskriftarkeyrslunni.  
    * Aðeins lögaðilar með uppsettar færslubækur fyrir Eignatillögur á síðunni Færibreytur eigna verða sýndir á listanum.  
4. Veljið Já í reitnum bóka færslubækur.
    * Síureitir ná yfir allar eignir, hópa og bækur fyrir lögaðila sem valdir eru fyrir þessa afskriftakeyrslu.  
    * Runuvinnsluvalkosturinn er virkjaður að sjálfgefnu. Þegar þessi valkostur er virkjaður, mun stofnun og bókun færslubókar afskrifta keyrast í bakgrunni.  
5. Smella skal Stofna færslubók.
6. Fara í Eignir >°Færslubókarfærslur°> Eignabók.

