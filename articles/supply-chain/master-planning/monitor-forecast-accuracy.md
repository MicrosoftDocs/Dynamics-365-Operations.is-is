---
title: "Fylgjast með nákvæmni spár"
description: "Þessi grein lýsir gerðum nákvæmnispáa sem Microsoft Microsoft Dynamics 365 for Finance and Operations reiknar, og útskýrir hvernig hægt er að skoða nákvæmnigildin."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqDemPlanForecastDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1f54251b6f6937c59293bd44a0fc27272ffd3d55
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="monitor-forecast-accuracy"></a>Fylgjast með nákvæmni spár

[!include [banner](../includes/banner.md)]

Þessi grein lýsir gerðum nákvæmnispáa sem Microsoft Microsoft Dynamics 365 for Finance and Operations reiknar, og útskýrir hvernig hægt er að skoða nákvæmnigildin.

Finance and Operations reiknar eftirfarandi gerðir af nákvæmnispám:

-   Söguleg nákvæmni spár, með því að bera saman sögulega spá sem notar Aðaláætlanagerð með sögulega eftirspurn. Til að skoða gildi (bæði raungildi og prósentugildi) fyrir sögulega nákvæmni spár er smellt á **Sýna nákvæmni** á **Upplýsingar eftirspurnarspár** síðunni.
-   Áætlaðuð nákvæmni spárlíkans sem er notað til að mynda spár. Hægt er að skoða nákvæmnihlutfall undir **Líkan upplýsingar - MAPE** á **Upplýsingar eftirspurnarspár** síðunni. 

**Athugaðu:** Ef þú notar eftirspurnarspár í Finance and Operations Microsoft Azure Machine Learning þjónustu, byggist útreikningur á nákvæmni innra líkans á prófunargagnsafni. Til að tilgreina stærð prófunargagnasafns er stillt á **TEST\_SET\_ SIZE\_ PERCENT** færibreyta á **Færibreytur eftirspurnarspár síðu**. Til dæmis, ef virðið er stillt á **20**, munu síðustu 20°prósent sögulegra gagna verða notuð til að reikna út nákvæmni innra líkans.


<a name="additional-resources"></a>Frekari upplýsingar
--------

[Heimila leiðrétta spá](authorize-adjusted-forecast.md)

[Fjarlægja einfara úr sögulegum færslugögnum við útreikning á eftirspurnarspá](remove-historical-outliers-calculating-demand-forecast.md)




