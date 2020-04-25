---
title: Ákvarða uppskriftarútgáfu
description: Á meðan á niðurbroti eftirspurnar stendur, ef vara hefur gerð sjálfgefinnar vöru stillta á framleiðslu finnur áætlunarforritið gilda uppskriftarútgáfu byggða á svæði.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, BOMDesigner, InventItemOrderSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2534
ms.assetid: a5b64301-a011-4469-afaf-e4c9164ef9c6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efc980e3a3dfff6d163812396613a1493f4428a4
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3213792"
---
# <a name="determine-the-bom-version"></a>Ákvarða uppskriftarútgáfu

[!include [banner](../includes/banner.md)]

Á meðan á niðurbroti eftirspurnar stendur, ef vara hefur gerð sjálfgefinnar vöru stillta á framleiðslu finnur áætlunarforritið gilda uppskriftarútgáfu byggða á svæði. 

Svæðavíddin er alltaf þekkt og er tilgreind í eftirspurnarfærslu. Aðferðin við að ákvarða hvaða uppskriftarútgáfu á að nota er sem hér segir:

-   Ef uppskriftarútgáfa hefur verið skilgreind fyrir vöruna í eftirspurnarsvæðinu, notar forritið þessa svæðistengdu uppskrift.
-   Ef svæðistengd uppskriftarútgáfa hefur ekki verið skilgreind fyrir vöruna í eftirspurnarsvæðinu, notar forritið almenna uppskriftarútgáfu. Almenn uppskrift tilgreinir ekki svæði og gildir um mörg svæði. Ef til er almenn uppskrift, notar forritið hana.
-   Ef engin almenn uppskrift er fyrir hendi, stöðvast niðurbrot eftirspurnar á þessum tímapunkti.

Gild uppskriftarútgáfa, hvort sem hún er svæðistengd eða almenn, verður að uppfylla nauðsynlegar kröfur varðandi dagsetningu og magn.





