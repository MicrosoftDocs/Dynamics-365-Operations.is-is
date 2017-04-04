---
title: "Fylgjast með nákvæmni spár"
description: "Þessi skrá lýsir gerðir nákvæmni eftirspurnarspár Microsoft Dynamics 365 fyrir Aðgerðir á reiknar og útskýrir hvernig hægt er að skoða gildi nákvæmni."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
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
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: d3f88a4fa54217cea909c54955de05e2175db0cd
ms.lasthandoff: 03/29/2017


---

# <a name="monitor-forecast-accuracy"></a>Fylgjast með nákvæmni spár

Þessi skrá lýsir gerðir nákvæmni eftirspurnarspár Microsoft Dynamics 365 fyrir Aðgerðir á reiknar og útskýrir hvernig hægt er að skoða gildi nákvæmni.

Dynamics 365 aðgerða reiknar eftirfarandi gerðir af nákvæmni eftirspurnarspár:

-   Söguleg nákvæmni spár, með því að bera saman sögulega spá sem notar Aðaláætlanagerð með sögulega eftirspurn. Til að skoða gildi (bæði raungildi og prósentugildi) fyrir sögulega nákvæmni spár er smellt á **Sýna nákvæmni** á **Upplýsingar eftirspurnarspár** síðunni.
-   Áætlaðuð nákvæmni spárlíkans sem er notað til að mynda spár. Hægt er að skoða nákvæmnihlutfall undir **Líkan upplýsingar - MAPE** á **Upplýsingar eftirspurnarspár** síðunni. 

**Athugasemd:** Ef Dynamics 365 nota Aðgerðir Microsoft Azure Vél Nám þjónusta Eftirspurnarspár fyrir útreikning á nákvæmni innri líkan byggð á gagnasafn prófun. Til að tilgreina stærð gagnasafn prófun er stillt á **PRÓFA\_SETJA\_STÆRÐ\_PRÓSENT** færibreyta á á **færibreytur Eftirspurnarspár** síðu. Til dæmis, ef virðið er stillt á **20**, munu síðustu 20°prósent sögulegra gagna verða notuð til að reikna út nákvæmni innra líkans.


<a name="see-also"></a>Sjá einnig
--------

[Authorizing the adjusted forecast](authorize-adjusted-forecast.md)

[Remove outliers from historical transaction data when calculating a demand forecast](remove-historical-outliers-calculating-demand-forecast.md)


