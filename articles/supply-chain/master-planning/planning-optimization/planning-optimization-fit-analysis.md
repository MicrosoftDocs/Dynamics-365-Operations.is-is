---
title: Greining á samsvörun áætlunarfínstillingar
description: Þetta efni útskýrir hvernig á að sannreyna núverandi uppsetningu og gögn gagnvart getu virkni fínstillingar skipulagningar.
author: ChristianRytt
manager: AnnBe
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a61529da63bc20fdd591afc94db960b05c284bb9
ms.sourcegitcommit: b806f0c94d703bec39680fead827733361d47045
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/07/2020
ms.locfileid: "2935876"
---
[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

# <a name="planning-optimization-fit-analysis"></a>Greining á samsvörun áætlunarfínstillingar

Til að sjá hversu samhæf núverandi uppsetning og gögn eru við virkni fínstillingar áætlunarinnar ferðu í **Aðaláætlunargerð** \> **Uppsetning** \> **Greining á samsvörun áætlunarfínstillingar** og veldu síðan **Keyra greiningu**. Ef greiningin finnur fyrir ósamræmi eru þau skráð á sömu síðu. (Greiningin getur tekið nokkrar mínútur í keyrslu.)

> [!NOTE]
> Ef ósamræmi finnst, getur þú samt notað fínstillingu skipulagsins. Niðurstöður samsvörunargreiningar sýna bara staði þar sem skipulagsþjónustan mun ekki heiðra núverandi uppsetningu. Með öðrum orðum sýna þær staði þar sem einhver ferli kunna að vera hunsuð eða ekki studd.

## <a name="analysis-results-example-1"></a>Niðurstöður greiningar: Dæmi 1

- **Eiginleiki:** Framleiðsla
- **Mál:** Vörur með BOM-stig sem eru hærri en núll: 56
- **Útskýring:** Í samsvörunargreiningunni fundust 56 vörur sem eru með uppsetningu uppskriftar (BOM) fyrir framleiðslu. Vegna þess að núverandi útgáfa af fínstillingu áætlunargerðar styður ekki framleiðslu mun fínstilling áætlunarinnar búa til innkaupatillögur í stað framleiðslutillaga. Hún mun einnig sýna viðvörun sem sýnir vörurnar sem varða fyrir áhrifum.

### <a name="analysis-results-example-2"></a>Niðurstöður greiningar: Dæmi 2

- **Eiginleiki:** Aðgerðir
- **Mál:** Þekjuhópar með útreikninga á aðgerðum virkjaða: 6
- **Útskýring:** Samsvörunargreiningin fann sex þekjuhópa þar sem kveikt er á útreikningi á aðgerðum. Þar sem núverandi útgáfa af fínstillingu áætlunarinnar styður ekki aðgerðir verða engar aðgerðir myndaðar við aðalskipulagningu.

## <a name="related-resources"></a>Tengd tilföng

[Yfirlit yfir fínstillingu skipulagningar](planning-optimization-overview.md)

[Byrjaðu með hagræðingu skipulags](get-started.md)

[Skoða áætlunarsögu og skipulagsskrár](plan-history-logs.md)

[Nota síur á áætlun](plan-filters.md)

[Hætta við áætlunarvinnslu](cancel-planning-job.md)
