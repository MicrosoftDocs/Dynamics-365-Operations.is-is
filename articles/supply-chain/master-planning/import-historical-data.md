---
title: Gögn flutt út fyrir eftirspurnarspár
description: Til að fá nákvæmar spár um eftirspurn þarf að hafa söguleg eftirspurnargögn fyrir hverja vöru eða vöruúthlutunarlykil. Þetta efnisatriði útskýrir hvernig á að nota gagnaeiningar til að flytja inn söguleg eftirspurnargögn úr hvaða kerfi sem er þannig að notandi hafi lengri sögu yfir eftirspurnargögn.
author: roxanadiaconu
manager: AnnBe
ms.date: 05/10/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanCreateForecastDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.assetid: 59c0d269-9db0-48e7-b8c7-9a388781a9ca
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 018694c79c6dd64e19b010848aad8acd36b0a9a8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "328609"
---
# <a name="import-historical-data-for-demand-forecasts"></a>Gögn flutt út fyrir eftirspurnarspár

[!include [banner](../includes/banner.md)]

Til að tryggja aukna nákvæmni spár um eftirspurn þarf að hafa eins mikið af sögulegum eftirspurnargögnum og hægt er að fá fyrir hverja vöru eða hvern vöruúthlutunarlykil. Ef söguleg eftirspurnargögn hafa ekki þegar verið flutt inn skal nota gagnaeininguna **Söguleg ytri eftirspurn** (ReqDemPlanHistoricalExternalDemandEntity) í Microsoft Dynamics 365 for Finance and Operations til að flytja þau inn.

Á vinnusvæðinu **Gagnastjórnun** er hægt að sjá yfirlit yfir alla reiti í einingunni.

1. Opnaðu vinnusvæðið **Gagnastjórnun**.
2. Smellið á reitinn **Gagnaeiningar**.
3. Leitið í einingalistanum fyrir **Söguleg ytri eftirspurn**.
4. Smellið á **Markreitir**. Eftirfarandi einingareitir eru áskildir: vefsvæði (**DeliveringSiteId**), dagsetning (**DemandDate**), magn (**DemandQuantity**) og annað hvort vörunúmer (**ItemNumber**) eða úthlutunarlykill vöru (**ProductAllocationKeyId**).

Til að nota gagnaeininguna verður að hafa annað hvort Microsoft Excel-skrá eða skrá með gildum aðgreindum með kommum (CSV) sem inniheldur sögulegu eftirspurnargögnin. Eftirfarandi dæmi sýnir hvernig á að flytja gögn úr CSV-skrá.

## <a name="example"></a>Dæmi

Hægt er að nota eftirfarandi skrá sem dæmi. Sæktu [HistoricalDemandData](https://mbs.microsoft.com/customersource/northamerica/AX/learning/documentation/how-to-articles/365OperationsDemandForecast). Þessi skrá inniheldur gögn sögulegar eftirspurnar vöru D0001. Hún inniheldur aðeins fyrir eftirfarandi skyldusvæði: svæði, magn og dagsetningu eftirspurnar.

1. Velja fyrirtæki til að flytja söguleg eftirspurnargögn inn í.
2. Opnaðu vinnusvæðið **Gagnastjórnun**.
3. Smellið á reitinn **Flytja inn**.
4. Færið inn heiti fyrir innflutningsverkið, t.d. **Flytja inn sögulega eftirspurn fyrir vöruna D0001**.
5. Í reitinn **Snið upprunagagna** skal velja skráarsnið skráarinnar sem þú ert að flytja inn. Til þess að flytja inn skrána HistoricalDemandData í þessu dæmi skal velja **CSV**.
6. Í reitinn **Heiti Einingar** skal velja **Söguleg ytri eftirspurn**.
7. Vistaðu skrána í tölvunni og hladdu henni svo upp.
8. Smelltu á **Flytja inn**.
9. Síðan **Samantekt framkvæmdar** opnast sjálfkrafa. Sannprófaðu innfluttu gögnin á síðunni.

Eftir að söguleg eftirspurnargögn hafa verið flutt inn er hægt að mynda eftirspurnarspá.

## <a name="additional-resources"></a>Frekari upplýsingar

[Myndun tölfræðilegrar grunnlínuspár](generate-statistical-baseline-forecast.md)
