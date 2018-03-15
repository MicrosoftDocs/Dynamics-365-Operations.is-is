---
title: "Rafrænu skýrslugerðarsniði breytt með því að endurnýta Microsoft Excel-sniðmát"
description: "Þetta umræðuefni veitir upplýsingar um hvernig hægt er að breyta sniði rafrænnar skýrslugerðar (ER) sem er notað til að búa til viðskiptaskjöl með því að endurnota breytt Excel-sniðmát."
author: NickSelin
manager: AnnBe
ms.date: 06/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: af7f9a373496eee4df354d5dd9e5a25c51317c43
ms.openlocfilehash: fca7fb75b965886c2ebc06b12940434f2ffc2543
ms.contentlocale: is-is
ms.lasthandoff: 02/27/2018

---
# <a name="modify-an-electronic-reporting-format-by-reapplying-a-microsoft-excel-template"></a>Rafrænu skýrslugerðarsniði breytt með því að endurnýta Microsoft Excel-sniðmát

[!include[banner](../includes/banner.md)]

Rafræn skýrslugerð (ER) tólið er notað til að búa til viðskiptaskjöl á rafrænu formi. Til að búa til viðskiptaskjöl verður að búa til ER-snið og nota síðan ER-hönnuður til að skilgreina útlit viðskiptaskjalsins og tilgreina þau gögn sem eiga að vera með í því. Þú getur þá keyrt ER-sniðið til að búa til viðskiptaskjalið.

ER tólið er hægt að nota til að búa til viðskiptaskjöl í formi Microsoft Excel-skráa. Hægt er að nota Excel-skjal sem sniðmát fyrir þessi skjöl. Til að skilgreina útlit skjalsins í ER hönnuður, er hægt að flytja efni Excel-skjalsins sem þú vilt nota sem sniðmát inn í skilgreint ER sniðið. Fyrir frekari upplýsingar og til að æfa þig í þessum aðstæðum,  skaltu spila verkleiðbeiningarnar **ER Hanna skilgreiningu fyrir myndun skýrslna í OPENXML-sniði** (hluti af 7.5.4.3 Acquire/Develop IT service/solution components (10677) viðskiptaferli).

Ef þú breytir Excel-skjalinu sem er notað sem sniðmát fyrir viðskiptaskjal, gerir ný ER-virkni þér kleift að endurnota uppfært sniðmátið á ER-sniðið. ER-sniðið er síðan uppfært þannig að það fylgir uppfærða sniðmátinu. Til að fá frekari upplýsingar um þessa virkni, skaltu spila verkleiðbeiningarnar **ER Hanna snið með því að endurnota Excel-sniðmát** (hluti af 7.5.5.3 Acquire/Develop IT service/solution components (10683) viðskiptaferli). Í skrefinu í verkleiðbeiningunum þar sem þú flytur inn uppfært sniðmát, skaltu nota breytt sniðmát Greiðsluskýrsla Excel-skrárinnar, SampleVendPaymWsReport2, sem sniðmát.

