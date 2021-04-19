---
title: Eftirlit með nákvæmni spár
description: Þetta efni lýsir gerðum nákvæmnispáa sem Dynamics 365 Supply Chain Management reiknar, og útskýrir hvernig hægt er að skoða nákvæmnigildin.
author: roxanadiaconu
ms.date: 01/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db8b9fdaf05f58d1386513348c11fcc54887d9c8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826468"
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





[!INCLUDE[footer-include](../../includes/footer-banner.md)]