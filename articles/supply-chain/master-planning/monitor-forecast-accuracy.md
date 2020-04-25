---
title: Eftirlit með nákvæmni spár
description: Þetta efni lýsir gerðum nákvæmnispáa sem Dynamics 365 Supply Chain Management reiknar, og útskýrir hvernig hægt er að skoða nákvæmnigildin.
author: roxanadiaconu
manager: tfehr
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab74ba88ba9eb683107ef82bc105f5a3ed8fac08
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209813"
---
# <a name="monitor-forecast-accuracy"></a>Eftirlit með nákvæmni spár

[!include [banner](../includes/banner.md)]

Þetta efni lýsir gerðum nákvæmnispáa sem Microsoft Dynamics 365 Supply Chain Management reiknar, og útskýrir hvernig hægt er að skoða nákvæmnigildin.

Supply Chain Management reiknar eftirfarandi gerðir af nákvæmnispám:

-   Söguleg nákvæmni spár, með því að bera saman sögulega spá sem notar Aðaláætlanagerð með sögulega eftirspurn. Til að skoða gildi (bæði raungildi og prósentugildi) fyrir sögulega nákvæmni spár er smellt á **Sýna nákvæmni** á **Upplýsingar eftirspurnarspár** síðunni.
-   Áætlaðuð nákvæmni spárlíkans sem er notað til að mynda spár. Hægt er að skoða nákvæmnihlutfall undir **Líkan upplýsingar - MAPE** á **Upplýsingar eftirspurnarspár** síðunni. 

> [!NOTE]
> Ef þú notar eftirspurnarspár Microsoft Azure Machine Learning byggist útreikningur á nákvæmni innri líkans á prófunargagnasafni. Til að tilgreina stærð prófunargagnasafns er stillt á **TEST\_SET\_SIZE\_PERCENT** færibreyta á **Færibreytur eftirspurnarspár síðu**. Til dæmis, ef virðið er stillt á **20**, munu síðustu 20°prósent sögulegra gagna verða notuð til að reikna út nákvæmni innra líkans.


<a name="additional-resources"></a>Frekari upplýsingar
--------

[Leiðrétt spá heimiluð](authorize-adjusted-forecast.md)

[Fjarlægja einfara úr sögulegum færslugögnum við útreikning á eftirspurnarspá](remove-historical-outliers-calculating-demand-forecast.md)



