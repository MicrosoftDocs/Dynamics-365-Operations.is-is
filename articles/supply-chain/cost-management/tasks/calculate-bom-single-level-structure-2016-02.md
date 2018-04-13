--- 
title: "Reikna uppskrift á einu stigi (aðeins febrúar 2016)"
description: "Þetta ferli sýnir hvernig reikna út kostnað fullunnin vara með því að nota niðurbrot á einu stigi sem er í kostnaðarskjali."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 0e6829238b244cc01b070fde6acdf37bdaeb9670
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016-only"></a>Reikna uppskrift á einu stigi (aðeins febrúar 2016)

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

Þetta ferli sýnir hvernig reikna út kostnað fullunnin vara með því að nota niðurbrot á einu stigi sem er í kostnaðarskjali. Þetta er sjötta verkið í línunni Útreikningur uppskrifta. Sýnigögn gögn fyrirtækisins til að stofna verkið er USMF.

1. Farðu í Losaðar afurðir.
2. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
    * Velja vöru BOM_1.  
3. Á Aðgerðasvæðinu skal smella á Stjórna kostnaði.
4. Smellt er á Verð vöru.
5. Smellt er á Reikna vörukostnað.
    * Gæti þurft að smella á þrípunkt (...) til að sjá þennan valkostur í efsta valmynd.  
6. Í svæði Kostnaðarútgáfa, smella á fellilistahnapp til að opna uppflettingu.
    * Í þessu sýnishorni, velja 10. Þetta er sama kostnaðarútgáfa notuð til að bæta kostnaðarverði við íhluti.  
7. Smellið á „Í lagi“.
8. Smellt er á Skoða útreikningsupplýsingar.
    * Gæti þurft að smella á þrípunkt (...) til að sjá þennan valkostur í efsta valmynd.    Hér er samsetning kostnaðarins:  •    10 kemur úr ITEM_A, 10 úr ITEM_B, 10 úr BOM_2. Í þessu tilfelli eru engar upplýsingar fyrir BOM_2 því að fært inn sem staðalkostnaður af 10 en ekki gert í gegnum útreikningur.  •  7 kemur úr uppsetningartími, sem er fastur kostnaður, og viðbótar 7 kemur úr keyrsluaaðgerð (Vinnsla).  •  Einnig eru aðrar upphæðir sem samsvara óbeinum kostnaði.  
9. @SysTaskRecorder:_RequestClose


