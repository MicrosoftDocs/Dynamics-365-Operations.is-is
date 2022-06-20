---
title: Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Finance
description: Þessi grein lýsir eiginleikum sem hafa verið fjarlægðir, eða sem fyrirhugað er að fjarlægja úr Dynamics 365 Finance.
author: kfend
ms.date: 03/21/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: kfend
ms.search.validFrom: 2020-03-02
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 0278b57ccfa2da9dba6b5ea77821fdc47ad2d078
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846655"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-finance"></a>Eiginleikar sem hafa verið fjarlægðir eða eru úreltir í Dynamics 365 Finance

[!include [banner](../includes/banner.md)]

Þessi grein lýsir eiginleikum sem hafa verið fjarlægðir, eða sem fyrirhugað er að fjarlægja úr Dynamics 365 Finance.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Þessi listi er ætlað að hjálpa þér að íhuga þessar fjarlægingar og úreldingar fyrir eigin áætlanagerð. 

> [!NOTE]
> Ítarlegar upplýsingar um hluti í Finance and Operations öppum er að finna í [Tæknilegar tilvísunarskýrslur](/dynamics/s-e/global/axtechrefrep_61). Þú getur borið saman mismunandi útgáfur þessara skýrslna til að fræðast um hluti sem hafa breyst eða verið fjarlægðir í hverri útgáfu af Finance and Operations forritum.

## <a name="features-removed-or-deprecated-in-the-finance-10026-release"></a>Eiginleikar sem voru fjarlægðir eða úreltir í Finance 10.0.26 útgáfu

### <a name="sales-tax-report-for-finland-design-based-on-reporting-codes"></a>Vöruskattsskýrsla fyrir Finnland (hönnun byggð á skýrslukóðum)

[Söluskattsskýrsla fyrir Finnland](../localizations/emea-fin-sales-tax-payment-report-finland.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir nýja hönnun virðisaukaskattsskýrslu, [VSK yfirlýsing fyrir Finnland](../localizations/emea-fin-vat-declaration.md). |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Fyrir 1. mars 2023 ætlum við að styðja ekki lengur söluskattsskýrsluna fyrir Finnland (finnsk skýrsluútlit). Nýtt **VSK yfirlýsing TXT (FI**) og **VSK yfirlýsing Excel (FI)** Rafræn skýrslugerð (ER) snið eru kynnt undir **Skattskýrsla** fyrirmynd. |

## <a name="features-removed-or-deprecated-in-the-finance-10024-release"></a>Eiginleikar sem voru fjarlægðir eða úreltir í Finance 10.0.24 útgáfu

### <a name="sales-tax-report-for-sweden-design-based-on-reporting-codes"></a>Vöruskattsskýrsla fyrir Svíþjóð (hönnun byggð á skýrslukóðum)

[Söluskattsskýrsla fyrir Svíþjóð](../localizations/emea-swe-sales-tax-payment-report-sweden.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir nýja hönnun virðisaukaskattsskýrslu, [VSK yfirlýsing fyrir Svíþjóð](../localizations/emea-swe-vat-declaration-sweden.md) |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Fyrir 1. desember 2022 ætlum við að styðja ekki lengur söluskattsskýrslu fyrir Svíþjóð (sænsk skýrsluútlit). Nýtt **VSK yfirlýsing XML (SE**) og **VSK yfirlýsing Excel (SE)** Rafræn skýrslugerð (ER) snið eru kynnt undir **Skattskýrsla** fyrirmynd. |

### <a name="vat-statement-for-austria-design-based-on-reporting-codes"></a>VSK yfirlit fyrir Austurríki (hönnun byggð á skýrslukóðum)

[Upplýsingar um VSK yfirlit fyrir Austurríki](../localizations/emea-aut-vat-statement-details.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir nýja hönnun virðisaukaskattsskýrslu, [VSK yfirlýsing fyrir Austurríki](../localizations/emea-aut-vat-declaration-austria.md) |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Fyrir 1. desember 2022 ætlum við að styðja ekki lengur **VSK yfirlýsing (AT)** Rafræn skýrslugerð (ER) snið undir **VSK framtalslíkan**. Nýtt **VSK yfirlýsing XML (AT)** og **VSK yfirlýsing Excel (AT)** snið eru kynnt undir **Skattskýrsla** fyrirmynd. |

### <a name="elster-declaration-for-germany-design-based-on-reporting-codes"></a>ELSTER yfirlýsing fyrir Þýskaland (hönnun byggð á skýrslukóðum)

[VSK-yfirlit](../localizations/emea-de-vat-declaration.md)</br>
[Settu upp rafræna skattskýrslu fyrir Þýskaland](../../fin-ops-core/dev-itpro/analytics/tasks/setup-electronic-tax-declaration-germany.md)</br>
[Rafræn innsending VSK-skýrslu (ELSTER)](../localizations/tasks/de-00003-electronic-transmission-elster.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir nýja hönnun virðisaukaskattsskýrslu, [VSK yfirlýsing fyrir Þýskaland](../localizations/emea-deu-vat-declaration-germany.md) |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Fyrir 1. desember 2022 ætlum við að styðja ekki lengur **Elster (DE)** og **Elster módel** Rafræn skýrslugerð (ER) snið. Nýtt **VSK yfirlýsing XML (DE)** og **VSK yfirlýsing Excel (DE)** snið eru kynnt undir **Skattskýrsla** fyrirmynd. |

### <a name="ob-declaration-for-netherlands-design-based-on-reporting-codes"></a>OB yfirlýsing fyrir Holland (hönnun byggð á tilkynningarkóðum)

[OB yfirlýsing](../localizations/emea-nl-vat-declaration.md)

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir nýja hönnun virðisaukaskattsskýrslu, [VSK yfirlýsing fyrir Holland](../localizations/emea-nl-vat-declaration-netherlands.md) |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Fyrir 1. desember 2022 ætlum við að styðja ekki lengur **OB yfirlýsing (NL)** og **OB yfirlýsingalíkan** Rafræn skýrslugerð (ER) snið. Nýtt **VSK yfirlýsing XML (NL)** og **VSK yfirlýsing Excel (NL)** snið eru kynnt undir **Skattskýrsla** fyrirmynd. |

## <a name="features-removed-or-deprecated-in-the-finance-10020-release"></a>Eiginleikar sem voru fjarlægðir eða úreltir í Finance 10.0.20 útgáfu

### <a name="rtir-query-invoice-data-request-hu-electronic-reporting-er-format-configuration"></a>RTIR Query Invoice Data Request (HU) sniðsstilling rafrænnar skýrslugerðar

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Ekki tekið með í meðhöndlun rafrænna skilaboða samaðgerðar með Ungverskt reikningskerfi á netinu |
| **Skipt út fyrir aðra eiginleika?**   | Nei |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: frá 15. apríl 2022 hyggjumst við ekki lengur styðja „RTIR Query Invoice Data Request (HU)“ sniðsstillingu. |

### <a name="french-fec-audit-file-electronic-reporting-er-format-for-france-under-german-audit-file-output-format"></a>„Frönsk FEC-endurskoðunarskrá“ snið rafrænnar skýrslugerðar fyrir Frakkland undir skilgreiningarsniðinu „Þýsk endurskoðunarskrá“.

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir nýtt snið „FEC endurskoðunarskrá (FR)“ |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Niðurfelling: 1. maí 2022 styðjum við ekki lengur skilgreiningarsnið „Frönsk FEC-endurskoðunarskrá“ snið rafrænnar skýrslugerðar fyrir Frakkland undir skilgreiningarsniðinu „Þýsk endurskoðunarskrá“. Nýtt snið FEC endurskoðunarskráar (FR) er kynnt í staðinn undir „Gagnaútflutningslíkan“. |

## <a name="features-removed-or-deprecated-in-the-finance-10017-release"></a>Eiginleikar sem voru fjarlægðir eða úreltir í Finance 10.0.17 útgáfu

### <a name="lcs-repository-as-a-storage-option-for-electronic-reporting-configurations"></a>LCS-geymsla sem geymsluvalkostur fyrir skilgreiningar rafrænnar skýrslugerðar

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir nýja Regulatory Configuration Service (RCS) altæka geymslu |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Dynamics 365 Finance, Supply Chain Management og Project Operations vörur|
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Frá 1. apríl, 2022, hyggjumst við hætta stuðningi við Microsoft Dynamics Lifecycle Services (LCS) gagnageymslu sem geymsluvalkost fyrir stillingar rafrænnar skýrslugerðar. Nýjar Microsoft skilgreiningar rafrænnar skýrslugerðar verða aðeins birtar fyrir niðurhal úr altæku geymslunni. Hægt er að opna altæku geymsluna úr Dynamics 365 og RCS. Frekari upplýsingar er að finna í [Flytja inn skilgreiningar rafrænnar skýrslugerðar úr RCS](../../fin-ops-core/dev-itpro/analytics/tasks/import-configuration-rcs.md) og [Regulatory Configuration Service – geymsluafskrift Lifecycle Services](../localizations/rcs-lcs-repo-dep-faq.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10016-release"></a>Eiginleikar sem voru fjarlægðir eða úreltir í Finance 10.0.16 útgáfu

### <a name="vat-declaration-cz-and-control-statement-export-cz-electronic-reporting-formats-for-czech-republic"></a>„VSK-skýrsla (CZ)“ og „Control statement export (CZ)“ Snið rafrænnar skýrslugerðar fyrir Tékkland

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir nýrri snið |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Forskráð: Frá 22. janúar 2022 er „VSK-skýrsla (CZ)“, „Útflutningur stýriskýrslu (CZ)“ snið rafrænnar skýrslugerðar (ER). Ný Vsk-skýrsla XML (CZ), Vsk-skýrsla Excel (CZ), VSK-yfirlitsskýrsla XML (CZ) snið eru ti staðar í stað þess að vera undir „Skattskýrsla“. |

### <a name="ledger-transaction-export-format-be-electronic-reporting-format-and-respective-ledger-transaction-export-be-model-for-belgium"></a>Rafræna skýrslugerðarsniðið „Útflutningssnið fjárhagsfærslu (BE)“ og samsvarandi gerð „Útflutningur fjárhagsáætlunar (BE)“ fyrir Belgíu

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir nýtt snið rafrænnar skýrslugerðar undir gerðinni „Stöðluð endurskoðunarskrá (SAF-T)“.  |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: 1. desember, 2021 munum við ekki lengur styðja rafræna skýrslugerðarsniðið „Útflutningssnið fjárhagsfærslu (BE)“ og samsvarandi gerð „Útflutningur fjárhagsfærslu (BE)“. Nýtt snið „Útflutningur fjárhagsgagna“ ásamt „Vörpun fjárhagsgagnalíkans“ koma í staðinn undir gerðinni „Stöðluð endurskoðunarskrá (SAF-T)“. |

### <a name="vat-100-report-for-the-united-kingdom-in-ssrs-format"></a>„VSK 100“-skýrsla fyrir Bretland á SSRS-sniði

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir nýtt snið rafrænnar skýrslugerðar – sniðið „VSK-skýrsla á Excel (UK)“ undir „Skattframtalslíkan“.  |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: 1. desember, 2021 munum við ekki lengur styðja „VSK 100-skýrsla“ á SSRS-sniði. Nýtt snið „VSK-skýrsla á Excel (UK)“ undir „Skattframtalslíkan“ var kynnt með [MTD VSK-eiginleikanum](../localizations/emea-gbr-mtd-vat-integration.md). |

## <a name="features-removed-or-deprecated-in-the-finance-10015-release"></a>Eiginleikar sem voru fjarlægðir eða úreltir í Finance 10.0.15 útgáfu

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 stuðningi við Dynamics 365 hefur verið hætt

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Frá desember 2020, er Microsoft Internet Explorer 11 stuðningi fyrir allar Dynamics 365 vörur hætt og Internet Explorer 11 verða ekki stutt eftir ágúst 2021.<br><br>Þetta mun hafa áhrif á viðskiptavini sem nota Dynamics 365 vörur sem eru hannaðar til að nota með Internet Explorer 11 viðmóti. Eftir ágúst 2021 er Internet Explorer 11 ekki stutt fyrir þessar Dynamics 365 vörur. |
| **Skipt út fyrir aðra eiginleika?**   | Við mælum með því að viðskiptavinir skipti yfir í Microsoft Edge.|
| **Afurðasvæði sem haft er áhrif á**         | Allar Dynamics 365 vörur |
| **Dreifingarvalkostur**              | Allir|
| **Staða**                         | Úrelt. Internet Explorer 11 verður ekki stutt eftir ágúst 2021.|

## <a name="features-removed-or-deprecated-in-the-finance-10012-release"></a>Eiginleikar sem voru fjarlægðir eða úreltir í Finance 10.0.12 útgáfu

### <a name="not-deprecated-polish-ssrs-reports-sales-vat-register-purchase-vat-register-eu-summary-vat-register--feature-reference-pl-00014"></a>Ekki úrelt: Pólskar SSRS skýrslur: VSK skrá yfir sölu, virðisaukaskattsskrá, ESB yfirlit virðisaukaskattsskrá - Tilvísun eiginleika PL-00014

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Ekki krafist lagalega.  |
| **Skipt út fyrir aðra eiginleika?**   | Já (Excel snið fyrir venjulega endurskoðunarskrá með virðisaukaskattsyfirlýsingu - JPK_VDEK) |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Ekki úrelt: Frá og með 27. apríl 2021 ætlum við að halda áfram að styðja SSRS-skýrslur: **Skrá yfir útskatt, skrá yfir innskatt, VSK-skrá samantektar ESB – Tilvísun eiginleika PL-00014**. Dæmi um Excel-snið fyrir venjulega endurskoðunarskrá með virðisaukaskattsyfirlýsingu (JPK_VDEK) hefur einnig verið kynnt. |

## <a name="features-removed-or-deprecated-in-the-finance-10011-release"></a>Eiginleikar sem voru fjarlægðir eða úreltir í Finance 10.0.11 útgáfu

### <a name="norwegian-standard-main-accounts"></a>Aðallyklar Norwegian Standard

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Endurhönnun  |
| **Skipt út fyrir aðra eiginleika?**   | Já (Skipt út fyrir forritssértækar færibreytur ER-sniðs) |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Útfært: Fyrir 1. apríl 2021, stefnum við að því að styðja ekki lengur virkni sem tengist stöðluðum aðalreikningum: Tilvísunarreitur, tengd tafla, gagnaeining. |

## <a name="features-removed-or-deprecated-in-the-finance-1007-release"></a>Eiginleikar sem voru fjarlægðir eða úreltir í Finance 10.0.7 útgáfu

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Gluggi fyrir breytingu á verkflæðisbeiðni inniheldur ekki lengur fellivalmynd fyrir val á notendum

| &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt í aðgerðina með vali á lyklahópum.  |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Verkflæði |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Þann 1. desember 2020 munum við að ekki lengur styðja uppsetningu kínverskra fylgiskjala án vals á lyklahópum. Nánari upplýsingar um nýja hönnun er að finna í [Nýjungar í 10.0.7](whats-new-changed-10-0-7.md). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Fyrri tilkynningar um eiginleika sem voru fjarlægðir eða úreltir
Til að læra meira um eiginleika sem hafa verið fjarlægðir eða úreltir í fyrri útgáfum, sjá [Fjarlægir eða úreltir eiginleikar í fyrri útgáfum](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
