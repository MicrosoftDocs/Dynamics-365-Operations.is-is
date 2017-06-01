---
title: "Fylgjast með nákvæmni spár"
description: "Þessi skrá lýsir gerðum nákvæmnispáa sem Microsoft Microsoft Dynamics 365 for Operations reiknar, og útskýrir hvernig hægt er að skoða nákvæmnigildin."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72863
ms.assetid: 810a0d63-f4c6-4167-b2b3-a178b74ead89
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 580b45263b45e6ef730b0fac32575fcdd9c358b6
ms.contentlocale: is-is
ms.lasthandoff: 05/25/2017


---

# <a name="monitor-forecast-accuracy"></a>Fylgjast með nákvæmni spár

[!include[banner](../includes/banner.md)]


Þessi skrá lýsir gerðum nákvæmnispáa sem Microsoft Microsoft Dynamics 365 for Operations reiknar, og útskýrir hvernig hægt er að skoða nákvæmnigildin.

Dynamics 365 for Operations reiknar eftirfarandi gerðir af nákvæmni spár:

-   Söguleg nákvæmni spár, með því að bera saman sögulega spá sem notar Aðaláætlanagerð með sögulega eftirspurn. Til að skoða gildi (bæði raungildi og prósentugildi) fyrir sögulega nákvæmni spár er smellt á **Sýna nákvæmni** á **Upplýsingar eftirspurnarspár** síðunni.
-   Áætlaðuð nákvæmni spárlíkans sem er notað til að mynda spár. Hægt er að skoða nákvæmnihlutfall undir **Líkan upplýsingar - MAPE** á **Upplýsingar eftirspurnarspár** síðunni. 

**Ábending:** Ef eftirspurnarspár Dynamics 365 for Operations Microsoft Azure Vél Nám þjónustan byggist útreikningur á nákvæmni innri líkans á prófunargagnasafni. Til að tilgreina stærð prófunargagnasafns er stillt á **TEST\_SET\_ SIZE\_ PERCENT** færibreyta á **Færibreytur eftirspurnarspár síðu**. Til dæmis, ef virðið er stillt á **20**, munu síðustu 20°prósent sögulegra gagna verða notuð til að reikna út nákvæmni innra líkans.


<a name="see-also"></a>Sjá einnig
--------

[Heimila leiðrétta spá](authorize-adjusted-forecast.md)

[Fjarlægja frávik úr sögulegum færslugögn við útreikning á eftirspurnarspá](remove-historical-outliers-calculating-demand-forecast.md)




