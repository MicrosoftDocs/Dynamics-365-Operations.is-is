---
title: Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Finance
description: Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir úr Dynamics 365 Finance.
author: roschlom
manager: AnnBe
ms.date: 02/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 14428491383883c1fc2a8cdcd1975e1f1cb71b40
ms.sourcegitcommit: e9d19f25e64cf4d1c1d07c8031a7081454a6f79e
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/18/2021
ms.locfileid: "5474064"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða sem verða fjarlægðir úr Dynamics 365 Finance.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Þessi listi er ætlað að hjálpa þér að íhuga þessar fjarlægingar og úreldingar fyrir eigin áætlanagerð. 

> [!NOTE]
> Ítarlegar upplýsingar um hluti í forritum Finance and Operations má finna í [Tæknilegum tilvísunarskýrslum](https://docs.microsoft.com/dynamics/s-e/global/axtechrefrep_61). Hægt er að bera saman mismunandi útgáfur þessara skýrslna til að fá upplýsingar um hluti sem hefur verið breytt eða hafa verið fjarlægðir í hverri útgáfu forrita Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Eiginleikar sem voru fjarlægðir eða úreltir í Finance 10.0.17 útgáfu

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>LCS-geymsla sem geymsluvalkostur fyrir skilgreiningar rafrænnar skýrslugerðar

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir nýja Regulatory Configuration Service (RCS) altæka geymslu |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Dynamics 365 Finance, Supply Chain Management og Project Operations vörur|
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Frá 1. apríl, 2022, hyggjumst við hætta stuðningi við Microsoft Dynamics Lifecycle Services (LCS) gagnageymslu sem geymsluvalkost fyrir stillingar rafrænnar skýrslugerðar. Nýjar Microsoft skilgreiningar rafrænnar skýrslugerðar verða aðeins birtar fyrir niðurhal úr altæku geymslunni. Hægt er að opna altæku geymsluna úr Dynamics 365 og RCS. Frekari upplýsingar er að finna í [Flytja inn skilgreiningar rafrænnar skýrslugerðar úr RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Eiginleikar sem voru fjarlægðir eða úreltir í Finance 10.0.16 útgáfu

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a>„VSK-skýrsla (CZ)“ og „Control statement export (CZ)“ Snið rafrænnar skýrslugerðar fyrir Tékkland

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir nýrri snið |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Forskráð: Frá 22. janúar 2022 er „VSK-skýrsla (CZ)“, „Útflutningur stýriskýrslu (CZ)“ snið rafrænnar skýrslugerðar (ER). Ný Vsk-skýrsla XML (CZ), Vsk-skýrsla Excel (CZ), VSK-yfirlitsskýrsla XML (CZ) snið eru ti staðar í stað þess að vera undir „Skattskýrsla“. |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>Rafræna skýrslugerðarsniðið „Útflutningssnið fjárhagsfærslu (BE)“ og samsvarandi gerð „Útflutningur fjárhagsáætlunar (BE)“ fyrir Belgíu

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir nýtt snið rafrænnar skýrslugerðar undir gerðinni „Stöðluð endurskoðunarskrá (SAF-T)“.  |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: 1. desember, 2021 munum við ekki lengur styðja rafræna skýrslugerðarsniðið „Útflutningssnið fjárhagsfærslu (BE)“ og samsvarandi gerð „Útflutningur fjárhagsfærslu (BE)“. Nýtt snið „Útflutningur fjárhagsgagna“ ásamt „Vörpun fjárhagsgagnalíkans“ koma í staðinn undir gerðinni „Stöðluð endurskoðunarskrá (SAF-T)“. |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>„VSK 100“-skýrsla fyrir Bretland á SSRS-sniði

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir nýtt snið rafrænnar skýrslugerðar – sniðið „VSK-skýrsla á Excel (UK)“ undir „Skattframtalslíkan“.  |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: 1. desember, 2021 munum við ekki lengur styðja „VSK 100-skýrsla“ á SSRS-sniði. Nýtt snið „VSK-skýrsla á Excel (UK)“ undir „Skattframtalslíkan“ var kynnt með [MTD VSK-eiginleikanum](../localizations/emea-gbr-mtd-vat-integration.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Eiginleikar sem voru fjarlægðir eða úreltir í Finance 10.0.15 útgáfu

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 stuðningi við Dynamics 365 hefur verið hætt

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Frá desember 2020, er Microsoft Internet Explorer 11 stuðningi fyrir allar Dynamics 365 vörur hætt og Internet Explorer 11 verða ekki stutt eftir ágúst 2021.<br><br>Þetta mun hafa áhrif á viðskiptavini sem nota Dynamics 365 vörur sem eru hannaðar til að nota með Internet Explorer 11 viðmóti. Eftir ágúst 2021 er Internet Explorer 11 ekki stutt fyrir þessar Dynamics 365 vörur. |
| **Skipt út fyrir aðra eiginleika?**   | Við mælum með því að viðskiptavinir skipti yfir í Microsoft Edge.|
| **Afurðasvæði sem haft er áhrif á**         | Allar Dynamics 365 vörur |
| **Dreifingarvalkostur**              | Allir|
| **Staða**                         | Úrelt. Internet Explorer 11 verður ekki stutt eftir ágúst 2021.|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Eiginleikar sem voru fjarlægðir eða úreltir í Finance 10.0.12 útgáfu

### <a name="polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Pólska SSRS skýrslur: VSK skrá yfir sölu, virðisaukaskattsskrá, ESB yfirlit virðisaukaskattsskrá - Tilvísun eiginleika PL-00014

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Ekki krafist lagalega.  |
| **Skipt út fyrir aðra eiginleika?**   | Já (Excel snið fyrir venjulega endurskoðunarskrá með virðisaukaskattsyfirlýsingu - JPK_VDEK) |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Hætt við: Fyrir 1. júlí 2021, ætlum við að styðja ekki lengur SSRS skýrslurnar: **Velta VSK skrá, Kaup VSK skrá, ESB yfirlit VSK skrá - Tilvísun eiginleika PL-00014**. Dæmi um Excel snið fyrir venjulega endurskoðunarskrá með virðisaukaskattsyfirlýsingu (JPK_VDEK) verður kynnt í staðinn. |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Eiginleikar sem voru fjarlægðir eða úreltir í Finance 10.0.11 útgáfu

### <a name="norwegian-standard-main-accounts"></a>Aðallyklar Norwegian Standard

|   |  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Endurhönnun  |
| **Skipt út fyrir aðra eiginleika?**   | Já (Skipt út fyrir forritssértækar færibreytur ER-sniðs) |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Útfært: Fyrir 1. apríl 2021, stefnum við að því að styðja ekki lengur virkni sem tengist stöðluðum aðalreikningum: Tilvísunarreitur, tengd tafla, gagnaeining. |

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
