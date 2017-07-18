---
title: "Ákvarða uppskriftarútgáfu"
description: "Á meðan á niðurbroti eftirspurnar stendur, ef vara hefur gerð sjálfgefinnar vöru stillta á framleiðslu finnur áætlunarforritið gilda uppskriftarútgáfu byggða á svæði."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConsistOf, BOMDesigner, BOMTable, InventItemOrderSetup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: ee265d0ab7807cd92c70096111ffb3dbec11ad62
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017

---

# <a name="determine-the-bom-version"></a>Ákvarða uppskriftarútgáfu

[!include[banner](../includes/banner.md)]


Á meðan á niðurbroti eftirspurnar stendur, ef vara hefur gerð sjálfgefinnar vöru stillta á framleiðslu finnur áætlunarforritið gilda uppskriftarútgáfu byggða á svæði. 

Svæðavíddin er alltaf þekkt og er tilgreind í eftirspurnarfærslu. Aðferðin við að ákvarða hvaða uppskriftarútgáfu á að nota er sem hér segir:

-   Ef uppskriftarútgáfa hefur verið skilgreind fyrir vöruna í eftirspurnarsvæðinu, notar forritið þessa svæðistengdu uppskrift.
-   Ef svæðistengd uppskriftarútgáfa hefur ekki verið skilgreind fyrir vöruna í eftirspurnarsvæðinu, notar forritið almenna uppskriftarútgáfu. Almenn uppskrift tilgreinir ekki svæði og gildir um mörg svæði. Ef til er almenn uppskrift, notar forritið hana.
-   Ef engin almenn uppskrift er fyrir hendi, stöðvast niðurbrot eftirspurnar á þessum tímapunkti.

Gild uppskriftarútgáfa, hvort sem hún er svæðistengd eða almenn, verður að uppfylla nauðsynlegar kröfur varðandi dagsetningu og magn.






