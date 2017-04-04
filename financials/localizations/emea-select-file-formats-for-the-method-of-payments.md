---
title: "Skrársnið fyrir greiðsluhátt"
description: "Þetta efnisatriði lýsir tvær aðferðir til að sækja skráarsnið sem hægt er að nota fyrir greiðsluhátt."
author: ShylaThompson
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustPaymMode, VendPaymMode
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 262514
ms.assetid: 72ea2018-5a49-419c-93d0-755e5ff2722f
ms.search.region: Belgium, France, Germany, Norway, Spain, Sweden, Switzerland
ms.author: v-lenest
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 54af22f1f2ec779bf947ae584a3ae09c20e6a364
ms.lasthandoff: 03/31/2017


---

# <a name="file-formats-for-methods-of-payment"></a>Skrársnið fyrir greiðsluhátt

Þetta efnisatriði lýsir tvær aðferðir til að sækja skráarsnið sem hægt er að nota fyrir greiðsluhátt.

Það eru tvær aðferðir sem nota má til að sækja skrársnið fyrir notkun með greiðsluhætti, rafrænnar skýrslugerðar (ER) skrársnið eða X ++ skrársnið. Þegar sett er upp greiðsluhátt fyrir viðskiptavin eða lánardrottin, er að tilgreina hvaða skrársnið og stöðlum ætti að nota fyrir greiðslur og hvernig verður að vinna greiðslur. Hægt er að velja úr eftirfarandi sniðum:

-   Flytja út
-   Flytja inn
-   Vöruskil
-   Greiðsla

### <a name="method-1-electronic-reporting-file-formats"></a>Aðferð 1: Rafræna skýrslugerð skráasnið

Fyrir skráarsnið sem byggir á skilgreiningar ER, þarf að flytja inn afbrigði úr Lifecycle Services (LCS). Nánari upplýsingar, sjá [Sækja Rafræna skilgreiningar frá Lifecycle Services reporting](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs). Þegar búið er að flytja inn skilgreiningar fjárhagsskýrslna fyrir þær skráasnið, innfluttu snið verður tiltæk til að velja á fyrir **Greiðsluhættir** síðu. Ferlið við að flytja inn og velja skrársnið fyrir Europe er svipað og ferlið Japan. <!---For more details, see [Enable the JBA payment file format](https://ax.help.dynamics.com/en/wiki/enable-the-jba-payment-file-format/).-->

### <a name="method-2-x-file-formats"></a>Aðferð 2: X ++ skráasnið

Ljúkið eftirfarandi skrefum til að velja skrársnið sem eru byggðar á X ++ kóða sem er.

1.  Farið í **Greiðsluhættir** síðu.
2.  Á við **Skráasnið** FastTab, smellið á **Uppsetningu**.
3.  Veljið flipann sem samsvarar snið skráargerð með.
4.  Velja skrársnið úr á **Tiltækt** listanum og færa það yfir í **Valið** lista með stýringu örina.
5.  Loka skal **Skráasnið fyrir greiðsluhætti** síðu.
6.  Á við **Skráasnið** FastTab, velja skrársnið fyrir greiðsluhátt úr viðeigandi skrársvæði sniði. Almennar rafrænar skýrsluvalkostir ætti að vera stillt á **Nei** fyrir X ++ skráasniða.



