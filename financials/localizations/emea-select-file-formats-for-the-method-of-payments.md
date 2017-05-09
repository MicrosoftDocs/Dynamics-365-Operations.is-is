---
title: "Skrársnið fyrir greiðsluhátt"
description: "Þetta efnisatriði lýsir tveimur aðferðum til að sækja skráarsnið sem hægt er að nota fyrir greiðslumáta."
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

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir tveimur aðferðum til að sækja skráarsnið sem hægt er að nota fyrir greiðslumáta.

Hægt er að nota tvenns konar aðferðir til að sækja skráarsnið til að nota með greiðslumátum, skráarsnið fyrir rafræna skýrslugerð eða X++ skráarsnið. Þegar þú setur upp greiðslumáta fyrir viðskiptavin eða lánardrottinn tekurðu fram hvaða skráarsnið og staðla skal nota fyrir greiðslur og hvernig greiðslur verða afgreiddar. Hægt er að velja um eftirfarandi snið:

-   Flytja út
-   Flytja inn
-   Vöruskil
-   Greiðsla

### <a name="method-1-electronic-reporting-file-formats"></a>Aðferð 1: Skráarsnið fyrir rafræna skýrslugerð

Fyrir skráarsnið sem byggjast á skilgreiningum rafrænnar skýrslugerðar verður að flytja inn skilgreiningar frá Lifecycle Services (LCS). Frekari upplýsingar eru í [Niðurhal skilgreininga fyrir rafræna skýrslugerð af Lifecycle Services](/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs) Eftir að þú flytur inn skilgreiningar skýrslugerðar fyrir þessi skráarsnið er hægt að velja innfluttu sniðin á síðunni **Greiðslumáta**. Ferlið fyrir innflutning og val á skráarsniðum fyrir Evrópu er svipað og í Japan. <!---For more details, see [Enable the JBA payment file format](https://ax.help.dynamics.com/en/wiki/enable-the-jba-payment-file-format/).-->

### <a name="method-2-x-file-formats"></a>Aðferð 2: X++ skráarsnið

Til að velja skráarsnið sem byggjast á X++ kóða skal ljúka eftirfarandi skrefum.

1.  Farðu á síðuna **Greiðslumátar**.
2.  Á flýtiflipanum **Skráarsnið** er smellt á **Uppsetning**.
3.  Veldu flipann sem samsvarar gerð skráarsniðsins.
4.  Veldu skráarsnið úr listanum **Tiltækt** og færðu það í listann **Valið** með örvahnappi.
5.  Lokaðu síðunni **Skráarsnið fyrir greiðslumáta**.
6.  Á flýtiflipanum **Skráarsnið** skal velja skráarsniðið sem á að nota fyrir greiðslumátann úr viðeigandi reit fyrir skráarsnið. Almennir valkostir fyrir rafræna skýrslugerð eiga að vera stilltir á **Nei** X++ skráarsnið.





