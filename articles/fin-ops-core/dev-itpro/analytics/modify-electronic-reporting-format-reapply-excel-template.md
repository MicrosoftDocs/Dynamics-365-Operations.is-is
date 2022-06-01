---
title: Breyta rafrænum skýrslugerðarsniðum með því að endurnýta Excel-sniðmát
description: Þetta efnisatriði lýsir hvernig á að breyta sniði rafrænnar skýrslugerðar (ER) sem er notað til að búa til viðskiptaskjöl með því að endurnota breytt Excel-sniðmát.
author: NickSelin
ms.date: 05/18/2022
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
ms.openlocfilehash: 626450b05789c93f63675a55e050649c862c86f6
ms.sourcegitcommit: 336a0ad772fb55d52b4dcf2fafaa853632373820
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 05/28/2022
ms.locfileid: "8811393"
---
# <a name="modify-electronic-reporting-formats-by-reapplying-excel-templates"></a>Breyta rafrænu skýrslugerðarsniðum með því að endurnýta Excel-sniðmát

[!include [banner](../includes/banner.md)]

Rafræn skýrslugerð (ER) tólið er notað til að búa til viðskiptaskjöl á rafrænu formi. Til að búa til viðskiptaskjöl verður að búa til ER-snið og nota síðan ER-hönnuður til að skilgreina útlit viðskiptaskjalsins og tilgreina þau gögn sem eiga að vera með í því. Þú getur þá keyrt ER-sniðið til að búa til viðskiptaskjalið.

ER tólið er hægt að nota til að búa til viðskiptaskjöl í formi Microsoft Excel skráa. Hægt er að nota Excel-skjal sem sniðmát fyrir þessi skjöl. Til að skilgreina útlit skjalsins í ER hönnuður, er hægt að flytja efni Excel-skjalsins sem þú vilt nota sem sniðmát inn í skilgreint ER sniðið. Fyrir frekari upplýsingar og til að æfa þig í þessum aðstæðum, skaltu spila verkleiðbeiningarnar **ER Hanna skilgreiningu fyrir myndun skýrslna í OPENXML-sniði** (hluti af 7.5.4.3 Acquire/Develop IT service/solution components (10677) viðskiptaferli). Í verkefnaleiðbeiningarskrefinu þar sem þú flytur inn Excel sniðmát skaltu nota upphafssniðmátið í Excel skránni fyrir greiðsluskýrslu, [SampleVendPaymWsReport](https://download.microsoft.com/download/e/6/b/e6bb79f0-cc08-44af-96fa-49c7929d4fb8/SampleVendPaymWsReport.xlsx).

Ef þú breytir Excel-skjalinu sem er notað sem sniðmát fyrir viðskiptaskjal, gerir ný ER-virkni þér kleift að endurnota uppfært sniðmátið á ER-sniðið. ER-sniðið er síðan uppfært þannig að það fylgir uppfærða sniðmátinu. Til að fá frekari upplýsingar um þessa virkni, skaltu spila verkleiðbeiningarnar **ER Hanna snið með því að endurnota Excel-sniðmát** (hluti af 7.5.5.3 Acquire/Develop IT service/solution components (10683) viðskiptaferli). Í verkefnaleiðbeiningarskrefinu þar sem þú flytur inn uppfært sniðmát, notaðu breytta sniðmátið í Excel-skjal greiðsluskýrslu, [SampleVendPaymWsReport2](https://download.microsoft.com/download/3/1/0/3104d397-c9c5-4227-b68e-f98625313801/SampleVendPaymWsReport2.xlsx).

## <a name="additional-resources"></a>Frekari upplýsingar

[Uppfæra sniðmát](er-fillable-excel.md#update-a-template)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
