---
title: Reikna út uppskrift og nota uppbygging með einu stigi (febrúar 2016)
description: Þetta ferli sýnir hvernig reikna út kostnað fullunnin vara með því að nota niðurbrot á einu stigi sem er í kostnaðarskjali.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, InventItemPrice, BOMCalcDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c1968703c7e9662b5cccdb71d049010bb4bd4534
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1836505"
---
# <a name="calculate-a-bom-by-using-a-single-level-structure-february-2016"></a>Reikna út uppskrift og nota uppbygging með einu stigi (febrúar 2016)

[!include [task guide banner](../../includes/task-guide-banner.md)]

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
    * Gæti þurft að smella á þrípunkt (...) til að sjá þennan valkostur í efsta valmynd.    Hér er samsetning kostnaðarins:  •    10 kemur úr ITEM_A, 10 úr ITEM_B, 10 úr BOM_2. Í þessu tilfelli eru engar upplýsingar fyrir BOM_2 því að fært inn sem staðalkostnaður af 10 en ekki gert í gegnum útreikningur.  •  7 kemur úr uppsetningartíma, sem er fastur kostnaður, og 7 til viðbótar kemur úr keyrsluaaðgerð (Vinnsla).  •  Einnig eru aðrar upphæðir sem samsvara óbeinum kostnaði.  
9. @SysTaskRecorder:_RequestClose

