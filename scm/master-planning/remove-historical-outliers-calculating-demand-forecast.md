---
title: "Fjarlægja frávik úr sögulegum færslugögn við útreikning á eftirspurnarspá"
description: "Þessi grein lýsir hvernig á að útiloka frávik frá sögulegum gögnum sem eru notuð við útreikning á eftirspurnarspá. Með því útiloka einfara er hægt að auka nákvæmni eftirspurnarspár."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ReqDemPlanForecastParameters, ReqDemPlanOutlierQuerySetup
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 72621
ms.assetid: 88a964af-14eb-4c5c-945b-388e5908362c
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: 6f44e1ce566781f1586203528d55b13b28001a2c
ms.lasthandoff: 03/31/2017


---

# <a name="remove-outliers-from-historical-transaction-data-when-calculating-a-demand-forecast"></a>Fjarlægja frávik úr sögulegum færslugögn við útreikning á eftirspurnarspá

Þessi grein lýsir hvernig á að útiloka frávik frá sögulegum gögnum sem eru notuð við útreikning á eftirspurnarspá. Með því útiloka einfara er hægt að auka nákvæmni eftirspurnarspár.

Hægt er að útiloka outliers til að auka nákvæmni eftirspurnarspár. Þetta verk er valfrjálst. Hér er yfirlit yfir ferlið:

1.  Smellið á **Sniðmát fjárhagsáætlunargerðar**&gt;**Uppsetningu**&gt;**eftirspurnarspár**&gt;**Einfari fjarlægður** til að opna í **Einfari fjarlægður** síðuna þar sem hægt er að nota fyrirspurn til að velja færslur til að útiloka.
2.  Veljið fyrirtækið sem fyrirspurnin á við og færið svo inn nafn og lýsingu. Reiturinn **Dagsetning fyrirspurnar** er sjálfkrafa stilltur á Virkt.
3.  Velja skal gátreitinn **Virkur** gátreit til að útiloka færslur sem fyrirspurnin finnur í sögulegum gögnum. Þessi stilling tekur gildi þegar grunnlínuspá er stofnuð.
4.  Á síðunni **Fjarlægingarfyrirspurn fyrir einfara** er hægt að bæta við, fjarlægja og velja skilyrði sem skilgreina hvaða færslur verða útilokaðar þegar grunnspá er reiknuð. Til dæmis, veljið tiltekna vöru eða pöntunarfærslu sem á að útiloka.
5.  Smellt er á **Birta færslur**. Skjámyndin **Færslur einfara** listar færslur sem uppfylla þau skilyrði sem er skilgreind í fyrirspurninni og mun vera útilokuð frá rannsóknarsöguleg gögn þegar eftirspurnarspá er reiknað.

**Ábending:** Einnig er hægt að stofna fyrirspurn sem er byggð á fyrirliggjandi fyrirspurn. Velja skal fyrirspurn sem á að afrita og smella á **Afrita**. Reiturinn **Dagsetning fyrirspurnar** auðkennir útgáfunar. Hægt er að nota fyrirspurnina eins og hún er eða smella á **Breyta fyrirspurn** til að breyta skilyrðum. Einnig er hægt að breyta heiti og lýsingu á nýrri fyrirspurn.

<a name="see-also"></a>Sjá einnig
--------

[Introduction to demand forecasting](introduction-demand-forecasting.md)

[Monitoring forecast accuracy](monitor-forecast-accuracy.md)


