--- 
title: "Reikna uppskrift á mörgum stigum (aðeins febrúar 2016)"
description: "Þetta ferli sýnir hvernig reikna út kostnað fullunnin vara með því að nota niðurbrot á mörgum stigum sem er í kostnaðarskjali."
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 16c2cacaf70df5455c3ed49b8dcb5756e89f8cb8
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-a-bom-by-using-a-multilevel-structure-february-2016-only"></a>Reikna uppskrift á mörgum stigum (aðeins febrúar 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli sýnir hvernig reikna út kostnað fullunnin vara með því að nota niðurbrot á mörgum stigum sem er í kostnaðarskjali. Þetta er sjöunda verkið í línunni Útreikningur uppskrifta. Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.

1. Fara í upplýsingar um afurðastjórnun > Afurðir > Útgefnar afurðir.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Velja vöru BOM_1.  
3. Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.
4. Smellt er á Verð vöru.
5. Smellt er á Reikna vörukostnað.
    * Gæti þurft að smella á þrípunkt (...) til að sjá þennan valkostur í efsta valmynd.  
6. Í svæði Kostnaðarútgáfa, slá inn eða velja gildi.
    * Velja kostnaðarútgáfa 20, því að áætlaður kostnaður og niðurbrot eru með mörgum stigum.   Niðurbrot á mörgum stigum er fyrir áætlaður kostnaður og hermun. Það er ekki notað fyrir staðalkostnaður.  
7. Smellið á „Í lagi“.
8. Smellt er á Skoða útreikningsupplýsingar.
    * Gæti þurft að smella á þrípunkt (...) til að sjá þennan valkostur í efsta valmynd.  Í þessu tilfelli skal athuga hvernig BOM_2 hefur verið reiknað út með tilliti til hráefni, vinnsla og sameiginlegur kostnaður með samtals 29,40 í staðinn fyrir staðalkostnaðurinn 10, sem var virkjaður í upprunalega verkefnaleiðbeiningar í þessari línur.  
9. Smellt er á flipann Kostnaðarskjal.
    * Þegar litið er á flipinn Kostnaðarskjal eru samtölur á hvern kostnaðarflokkur ólíkur miðað við útreikningur sem gerður var í fyrri verkefnaleiðbeiningar.  
10. Á svæðinu Stig skal velja „Mörg stig“.
    * Þegar „Mörg stig“ eru valin eru kostnaður flokkaður samkvæmt samsetningu BOM_2, þar sem 10 kemur úr kostnaðarflokkur M1 (ITEM_C) og 15,60 kemur úr framleiðslu þar sem kostnaðarflokkur er L2. Óbeinn kostnaður er einnig mismunandi.  
11. Lokið síðunni.
12. Lokið síðunni.


