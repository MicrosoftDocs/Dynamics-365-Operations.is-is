---
title: Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Finance
description: Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir úr Dynamics 365 Finance.
author: roschlom
manager: AnnBe
ms.date: 03/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: ec13076e6a05c3402af566487f7921f6971da215
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127978"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir úr Dynamics 365 Finance.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Þessi listi er ætlað að hjálpa þér að íhuga þessar fjarlægingar og úreldingar fyrir eigin áætlanagerð. 

> [!NOTE]
> Ítarlegar upplýsingar um hluti í forritum Finance and Operations má finna í [Tæknilegum tilvísunarskýrslum](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Hægt er að bera saman mismunandi útgáfur þessara skýrslna til að fá upplýsingar um hluti sem hefur verið breytt eða hafa verið fjarlægðir í hverri útgáfu forrita Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Eiginleikar sem voru fjarlægðir eða úreltir í Finance 10.0.12 útgáfu

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Pólska SSRS skýrslur: VSK skrá yfir sölu, virðisaukaskattsskrá, ESB yfirlit virðisaukaskattsskrá - Tilvísun eiginleika PL-00014

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Ekki krafist lagalega.  |
| **Skipt út fyrir aðra eiginleika?**   | Já (Excel snið fyrir venjulega endurskoðunarskrá með virðisaukaskattsyfirlýsingu - JPK_VDEK) |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Hætt við: Fyrir 1. júlí 2021, ætlum við að styðja ekki lengur SSRS skýrslurnar: **Velta VSK skrá, Kaup VSK skrá, ESB yfirlit VSK skrá - Tilvísun eiginleika PL-00014**. Dæmi um Excel snið fyrir venjulega endurskoðunarskrá með virðisaukaskattsyfirlýsingu (JPK_VDEK) verður kynnt í staðinn. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Eiginleikar sem voru fjarlægðir eða úreltir í Finance 10.0.7 útgáfu

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Gluggi fyrir breytingu á verkflæðisbeiðni inniheldur ekki lengur fellivalmynd fyrir val á notendum
|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt í aðgerðina með vali á lyklahópum.  |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Verkflæði |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Þann 1. desember 2020 munum við að ekki lengur styðja uppsetningu kínverskra fylgiskjala án vals á lyklahópum. Nánari upplýsingar um nýja hönnun er að finna í [Nýjungar í 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Fyrri tilkynningar um eiginleika sem voru fjarlægðir eða úreltir
Til að læra meira um eiginleika sem hafa verið fjarlægðir eða úreltir í fyrri útgáfum, sjá [Fjarlægir eða úreltir eiginleikar í fyrri útgáfum](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).
