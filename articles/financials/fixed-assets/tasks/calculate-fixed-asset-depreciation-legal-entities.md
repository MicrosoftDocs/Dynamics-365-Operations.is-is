--- 
title: "Reikna afskriftir eigna milli lögaðila"
description: "Þessi aðferð sýnir hvernig skal setja upp og keyra afskriftarferlið fyrir marga lögaðila."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d804480167414cd038f8229db312dc9c52d131f8
ms.openlocfilehash: 4c45da124136b7fecb916d2ff9098c8ffeff6cb1
ms.contentlocale: is-is
ms.lasthandoff: 11/02/2017

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a>Reikna afskriftir eigna milli lögaðila

[!include[task guide banner](../../includes/task-guide-banner.md)]

Hægt er að keyra eignaafskriftir á milli lögaðila í einu skrefi. Þessi aðferð sýnir hvernig skal setja upp og keyra ferlið fyrir marga lögaðila. Það notar hlutverk Bókhaldara.  

Þessi skráning notar sýnigögn USMF fyrirtækis


Skref (16) Undirverkefni: Setja upp færslubókakeyrslu afskrifta á milli fyrirtækja. 

1. Í fyrsta lagi verður þú að setja upp færslubækurnar sem nota í keyrslu afskrifta milli fyrirtækja hjá sérhverjum lögaðila. Fara í Eignir > Uppsetning > Færibreytur eigna. 
2. Útvíkka eignatillagnahlutann. 
3. Búðu til skrá með færslubókarheitinu sem á að nota fyrir hvert bókunarlag í lögaðilanum. Ef bækur bóka ekki í fjárhag, ætti að velja bókunarlagið Engin með tengdu færslubókinni. Smelltu á Bæta við. 
4. Sláið inn eða veldu gildi í reitnum bókunarlag. 
5. Sláið inn eða veljið gildi í reitnum heiti færslubókar. 
6. Endurtaka uppsetning færslubókar á síðunni Færibreytur eigna fyrir hverjum lögaðila. 

Undirverkefni: Reikna út afskriftir

1. Notaðu síðuna Stofna afskriftartillögu til að hefja afskriftakeyrslu þína á milli lögaðila. Fara í Eignir > Færslubókarfærslur > Stofna afskriftartillögu. 
2. Sláið inn eða veldu gildi í reitnum bókunarlag. 
3. Færslubókarnafnið mun verða sjálfgefið úr Færibreytum eigna. Því er hægt að breyta hér fyrir núgildandi lögaðila. 
4. Í reitinn Til dagsetningar skal slá inn dagsetningu. 
5. Veljið lögaðilana sem á að hafa með í afskriftarkeyrslunni. Aðeins lögaðilar með uppsettar færslubækur fyrir Eignatillögur á síðunni Færibreytur eigna verða sýndir á listanum. 
6. Þegar Bóka færslubækur valkosturinn er virkjaður, mun hann sjálfkrafa bóka færslubækur afskriftar þegar þær eru stofnaðar. Þegar hann er ekki valinn, verða færslubækur búnar til en ekki bókaðar, svo þú getir skoðað upplýsingarnar fyrir bókun. Veljið Já í reitnum bóka færslubækur. 
7. Síureitir ná yfir allar eignir, hópa og bækur fyrir lögaðila sem valdir eru fyrir þessa afskriftakeyrslu. 
8. Runuvinnsluvalkosturinn er virkjaður að sjálfgefnu. Þegar þessi valkostur er virkjaður, mun stofnun og bókun færslubókar afskrifta keyrast í bakgrunni. 
9. Smella skal Stofna færslubók. 
10. Þú verður að skoða færslubækur afskrifta sem eru búnar til í viðkomandi lögaðilum. Fara í Eignir >°Færslubókarfærslur°> Eignabók.

