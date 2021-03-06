---
title: Breyta rafrænum skýrslugerðarsniðum með því að endurnýta Excel-sniðmát
description: Þetta efnisatriði lýsir hvernig á að breyta sniði rafrænnar skýrslugerðar (ER) sem er notað til að búa til viðskiptaskjöl með því að endurnota breytt Excel-sniðmát.
author: NickSelin
ms.date: 06/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.custom: 27621
ms.assetid: e3f7960d-2e01-46a7-9ac8-c355ac933cd6
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0ab7686ac0aba982fd44195214df878ba3ede446
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748718"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>Breyta rafrænu skýrslugerðarsniðum með því að endurnýta Excel-sniðmát

[!include [banner](../includes/banner.md)]

Rafræn skýrslugerð (ER) tólið er notað til að búa til viðskiptaskjöl á rafrænu formi. Til að búa til viðskiptaskjöl verður að búa til ER-snið og nota síðan ER-hönnuður til að skilgreina útlit viðskiptaskjalsins og tilgreina þau gögn sem eiga að vera með í því. Þú getur þá keyrt ER-sniðið til að búa til viðskiptaskjalið.

ER tólið er hægt að nota til að búa til viðskiptaskjöl í formi Microsoft Excel skráa. Hægt er að nota Excel-skjal sem sniðmát fyrir þessi skjöl. Til að skilgreina útlit skjalsins í ER hönnuður, er hægt að flytja efni Excel-skjalsins sem þú vilt nota sem sniðmát inn í skilgreint ER sniðið. Fyrir frekari upplýsingar og til að æfa þig í þessum aðstæðum, skaltu spila verkleiðbeiningarnar **ER Hanna skilgreiningu fyrir myndun skýrslna í OPENXML-sniði** (hluti af 7.5.4.3 Acquire/Develop IT service/solution components (10677) viðskiptaferli).

Ef þú breytir Excel-skjalinu sem er notað sem sniðmát fyrir viðskiptaskjal, gerir ný ER-virkni þér kleift að endurnota uppfært sniðmátið á ER-sniðið. ER-sniðið er síðan uppfært þannig að það fylgir uppfærða sniðmátinu. Til að fá frekari upplýsingar um þessa virkni, skaltu spila verkleiðbeiningarnar **ER Hanna snið með því að endurnota Excel-sniðmát** (hluti af 7.5.5.3 Acquire/Develop IT service/solution components (10683) viðskiptaferli). Í skrefinu í verkleiðbeiningunum þar sem þú flytur inn uppfært sniðmát, skaltu nota breytt sniðmát Greiðsluskýrsla Excel-skrárinnar, SampleVendPaymWsReport2, sem sniðmát.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]