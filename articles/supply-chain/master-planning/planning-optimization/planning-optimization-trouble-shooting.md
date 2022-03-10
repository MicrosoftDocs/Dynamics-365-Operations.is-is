---
title: Úrræðaleit fínstillingar áætlanagerðar
description: Þetta efnisatriði lýsir því hvernig á að leysa vandamál sem kunna að koma upp á meðan unnið er með fínstillingu áætlanagerðar.
author: ChristianRytt
ms.date: 05/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-5-7
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: bbf21abae60d4adee5a23a8405d14907b91724fa2cbf31c901bb46c589b2ea49
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/05/2021
ms.locfileid: "6768096"
---
# <a name="troubleshoot-planning-optimization"></a>Úrræðaleit fínstillingar áætlanagerðar 

[!include [banner](../../includes/banner.md)]

Þetta efnisatriði lýsir því hvernig á að laga almenn vandamál sem kunna að koma upp þegar unnið er með fínstillingu áætlanagerðar.

## <a name="installation-of-the-planning-optimization-add-in-doesnt-complete"></a>Uppsetningu á innbót fínstilling áætlanagerðar er ekki lokið

Fínstilling áætlanagerðar krefst þess að kveikt sé á Lifecycle Services (LCS), virkt umhverfi, á stigi 2 eða hærra (ekki OneBox-umhverfi), með Dynamics 365 Supply Chain Management-útgáfu 10.0.7 eða nýrri. Ef reynt er að setja upp innbótina í OneBox-umhverfi verður uppsetningunni ekki lokið.

**Lagfæra**: hætta við uppsetninguna og nota umhverfi með miklum tiltækileika, lag 2 eða hærra (ekki OneBox-umhverfi).

## <a name="planning-of-batch-jobs-fails-when-planning-optimization-is-enabled"></a>Áætlun um runuvinnslur mistekst þegar fínstilling áætlanagerðar er virk

Þegar fínstilling áætlanagerðar er gerð virk er innbyggð aðaláætlunargerðarkerfi sjálfkrafa gerð óvirk. Runuvinnslur aðaláætlanagerðar sem voru búnar til fyrir innbyggt áætlunarkerfi Supply Chain Management mistekst ef þær eru ræstar þegar fínstilling áætlanagerðar er virk. Hugsanlega birtast villuboð á borð við *Þessi aðgerð ræsti aðaláætlanagerð sem er ekki studd þegar fínstilling áætlunar er virk*.

**Lagfæra**: hætta við allar runuvinnslur Supply Chain Management sem voru stofnaðar fyrir innbyggt áætlunarkerfi aðfangakeðjustjórnunar.

## <a name="planning-optimization-results-are-different-from-earlier-results"></a>Niðurstöður fínstillingar áætlunargerðar eru frábrugðnar fyrri niðurstöðum

Fínstilling áætlanagerðar er frábrugðin hönnun innbyggðar aðaláætlanagerðar á sumum svæðum. Þetta getur einnig stafað af eiginleikum í bið.

**Lagfæra**: keyra samræmisgreiningu á fínstillingu áætlanagerðar og greina síðan niðurstöðurnar þegar vísað er í tengd fylgiskjöl til að skilja áhrifin. Frekari upplýsingar er að finna í [Greining á samsvörun áætlunarfínstillingar](planning-optimization-fit-analysis.md).

## <a name="cant-enable-planning-optimization"></a>Ekki hægt að virkja fínstillingu áætlanagerðar

**Tengingarstaðan** verður að vera **Tengdur** áður en hægt er að stilla **Nota fínstillingu áætlanagerðar** á **Já**. Frekari upplýsingar er að finna í [Hafist handa með fínstillingu skipulags](get-started.md).

**Lagfæra**: Gangið úr skugga um að innbót fínstillingar áætlanagerðar hafi verið uppsett.

## <a name="error-message-is-shown-during-ctp"></a>Villuboð eru sýnd í CTP

Ef reynt er að keyra afhendingargetu (CTP) frá sölupöntun þegar fínstilling áætlanagerðar er virk birtast eftirfarandi villuboð: *Þessi aðgerð ræsti aðaláætlanagerð sem er ekki studd þegar fínstilling áætlanagerðar er virk*.

Þetta tengist eiginleika í bið sem er áætlaður sem hluti af stuðningi við framleiðslupantanir.

**Lagfæra:** forðast CTP-útreikninga þegar fínstilling áætlanagerðar er virk þar til stuðningur við CTP er tiltækur.

## <a name="additional-resources"></a>Frekari upplýsingar

[Hafist handa með fínstillingu áætlanagerðar](get-started.md)

[Samræmisgreining á fínstillingu áætlanagerðar](planning-optimization-fit-analysis.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]