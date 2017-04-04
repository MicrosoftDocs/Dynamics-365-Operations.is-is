---
title: "Ákvarða hvaða uppskriftarútgáfu"
description: "Meðan á niðurbroti eftirspurnar stendur ef vara hefur sjálfgefna gerð pöntunar framleiðslu, finnur áætlunarforritið gilda uppskriftarútgáfu byggða á svæði."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, InventItemOrderSetup
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 4e4f5f02dfa986669decbc8854148b5eff928c2a
ms.lasthandoff: 03/31/2017


---

# <a name="determine-the-bom-version"></a>Ákvarða hvaða uppskriftarútgáfu

Meðan á niðurbroti eftirspurnar stendur ef vara hefur sjálfgefna gerð pöntunar framleiðslu, finnur áætlunarforritið gilda uppskriftarútgáfu byggða á svæði. 

Svæðavíddin er alltaf þekkt og er tilgreind í eftirspurnarfærslu. Aðferðin við að ákvarða hvaða uppskriftarútgáfu á að nota er sem hér segir:

-   Ef uppskriftarútgáfa hefur verið skilgreind fyrir vöruna í eftirspurnarsvæðinu, notar forritið þessa svæðistengdu uppskrift.
-   Ef svæðistengd uppskriftarútgáfa hefur ekki verið skilgreind fyrir vöruna í eftirspurnarsvæðinu, notar forritið almenna uppskriftarútgáfu. Almenn uppskrift tilgreinir ekki svæði og gildir um mörg svæði. Ef til er almenn uppskrift, notar forritið hana.
-   Ef engin almenn uppskrift er fyrir hendi, stöðvast niðurbrot eftirspurnar á þessum tímapunkti.

Gild uppskriftarútgáfa, hvort sem hún er svæðistengd eða almenn, verður að uppfylla nauðsynlegar kröfur varðandi dagsetningu og magn.




