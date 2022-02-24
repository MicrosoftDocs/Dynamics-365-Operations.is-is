---
title: Eiginleikar úr fyrri útgáfum sem hafa verið fjarlægðir eða eru úreltir
description: Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða áætlað að fjarlægja úr Dynamics 365 for Finance and Operations og fyrri útgáfum þeirrar vöru.
author: sericks007
manager: AnnBe
ms.date: 09/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7ce6b3fb5217ad5d5228841a91d0b0406c305969
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679957"
---
# <a name="removed-or-deprecated-features-in-previous-releases"></a>Eiginleikar úr fyrri útgáfum sem hafa verið fjarlægðir eða eru úreltir

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!IMPORTANT]
> Þetta efni er ekki lengur uppfært. Til að sjá núverandi lista yfir eiginleika sem hafa verið fjarlægðir eða úreltir úr forriti Finance and Operations, leitaðu að efni **„Fjarlægðir eða úreltir eiginleikar“** sem tengist forritinu sem þú notar.

Þetta efnisatriði lýsir eiginleikum sem hafa verið fjarlægðir eða úreltir úr Dynamics 365 for Finance and Operations og fyrri útgáfum þeirrar vöru.

- *Fjarlægður* eiginleiki er ekki lengur tiltækur í vörunni.
- *Úreltur* eiginleiki er ekki í virkri þróun og getur verið fjarlægður úr uppfærslum í framtíðinni.

Þessi listi er ætlað að hjálpa þér að íhuga þessar fjarlægingar og úreldingar fyrir eigin áætlanagerð. 

Ítarlegar upplýsingar um hluti í forritum Finance and Operations má finna í [Tæknilegum tilvísunarskýrslum](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Hægt er að bera saman mismunandi útgáfur þessara skýrslna til að fá upplýsingar um hluti sem hefur verið breytt eða hafa verið fjarlægðir í hverri útgáfu forrita Finance and Operations.

## <a name="finance-1007-with-platform-update-31"></a>Finance 10.0.7 með verkvangsuppfærslu 31

### <a name="chinese-voucher-types-without-account-groups-selection"></a>Kínverskar fylgiskjalsgerðir án vals á lyklahópum
|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt í aðgerðina með vali á lyklahópum. |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Öll |
| **Staða**                         | Úrelt: Þann 1. desember 2020 munum við að ekki lengur styðja uppsetningu kínverskra fylgiskjala án vals á lyklahópum. Nánari upplýsingar um nýjar aðgerðir er að finna í Nýjungar í 10.0.7 |

## <a name="finance-and-operations-1006-with-platform-update-30"></a>Finance and Operations 10.0.6 með verkvangsuppfærslu 30


### <a name="dimensionhashgethashstr-_message"></a>DimensionHash.getHash(str _message)

|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Windows afskrifar notkun á SHA1, eins og skjalfest er í [Windows Enforcement of SHA1 Certificates](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx).  |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Forrit |
| **Dreifingarvalkostur**              | Öll |
| **Staða**                         | Úrelt: Frá og með 1. apríl 2020 verða þróunaraðilar að nota API-verkvangana sem er að finna í klasanum **HasFunction**. |

### <a name="hashcomputesha1hashstring-message"></a>Hash.ComputeSHA1Hash(strengjaboð)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Windows afskrifar notkun á SHA1, eins og skjalfest er í [Windows Enforcement of SHA1 Certificates](https://social.technet.microsoft.com/wiki/contents/articles/32288.windows-enforcement-of-sha1-certificates.aspx).  |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Kerfi |
| **Dreifingarvalkostur**              | Öll |
| **Staða**                         | Úrelt: Frá og með 1. apríl 2020 verða þróunaraðilar að nota API-verkvangana sem er að finna í klasanum **HasFunction**. |


### <a name="formdatetimecontrolsetutcstring"></a>FormDateTimeControl.setUtcString()

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Við erum að leggja niður aðferðina **setUtcString()**, vegna þess að betri endurnýjunaraðferð er fáanleg. |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Kerfi |
| **Dreifingarvalkostur**              | Öll |
| **Staða**                         | Úrelt: Fyrir 1. október 2020, stefnum við að því að styðja ekki lengur við aðferðina **setUtcString()**. Verktaki ætti að nota aðferðina **setUtcDateTime()** í staðinn. |

### <a name="blacklist-report-it--feature-reference-it-00001"></a>Bannskýrsla (IT) - Tilvísun eiginleika IT-00001

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Ekki krafist lagalega. |
| **Skipt út fyrir aðra eiginleika?**   | Nr |
| **Afurðasvæði sem haft er áhrif á**         | Ítölsk staðsetning |
| **Dreifingarvalkostur**              | Öll |
| **Staða**                         | Úrelt: Þann 1. október 2020, stefnum við að því að styðja ekki lengur við **Bannskýrslu (IT) - Tilvísun eiginleika IT-00001**. |

### <a name="domestic-tax-report--feature-reference-it-00003"></a>Innlend skattaskýrsla - Tilvísunar eiginleika IT-00003

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Ekki krafist lagalega. |
| **Skipt út fyrir aðra eiginleika?**   | Nr |
| **Afurðasvæði sem haft er áhrif á**         | Ítölsk staðsetning |
| **Dreifingarvalkostur**              | Öll |
| **Staða**                         | Úrelt: Þann 1. október 2020, stefnum við að því að styðja ekki lengur við **Innlenda skattaskýrslu - Tilvísun eiginleika IT-00003**. |


## <a name="finance-and-operations-1005-with-platform-update-29"></a>Finance and Operations 10.0.5 með verkvangsuppfærslu 29

### <a name="us-payroll-tax-updates"></a>Uppfærslur á launaskatti í Bandaríkjunum

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Við erum að hætta við skattauppfærslur vegna bandarískra launatengdra aðgerða vegna lítillar notkunar og aukinnar virkni sem nú er boðið upp á með stefnumótandi samþættingum.  |
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Payroll |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Afskrifað: frá 31. júlí 2024 veitum við ekki lengur skattauppfærslur til US viðskiptavina. Virknin verður áfram í vörunni, en aukning uppfærir ekki virkni og allir gallar verða metnir á í hverju tilviki fyrir sig. |

>[!NOTE]
> Þetta táknar breytingu frá upphaflegri lokadagsetningu 1. október 2021. Sjá frekari upplýsingar [Skattauppfærslur tekin úr notkun vegna launagreiðslu í Bandaríkjunum í Microsoft Dynamics 365 for Finance and Operations](https://aka.ms/financepayrollfaq).


### <a name="data-management-staging-clean-up"></a>Hreinsun á sviðssetningu gagnastjórnunar
|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Uppfyllir ekki grunnkröfurnar sem þarf til að tímasetja reglulega hreinsun. |
| **Skipt út fyrir aðra eiginleika?**   | Já, verkreinsunaraðgerðinni er bætt við til að uppfylla atburðarásina á heildrænan hátt. |
| **Afurðasvæði sem haft er áhrif á**         | Gagnastjórnun |
| **Dreifingarvalkostur**              | Öll  |
| **Staða**                         | Úrelt: Stefnt er að því að fjarlægja virknina í desember 2020. |

## <a name="finance-and-operations-1004-with-platform-update-28"></a>Finance and Operations 10.0.4 með verkvangsuppfærslu 28

### <a name="france-fec-accounting-data-export-in-xml"></a>Frakkland: Útflutningur FEC-bókhaldsgagna í XML

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út með TXT-sniði, **Frönsk FEC-endurskoðunarskrá** er í boði í gegnum **Fjárhagur** \> **Reglubundin verkefni** \> **Útflutningur gagna**.
| **Skipt út fyrir aðra eiginleika?**   | Já |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt. Stefnt er að því að fjarlægja virknina í júlí 2020. |


### <a name="legacy-navigation-bar"></a>Eldri yfirlitsstika

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Stilling á haus með öðrum Dynamics- og Office-vörum. Nánari upplýsingar er að finna í [Uppfæra yfirlitsstiku sem er samstillt við Office-hausinn](https://docs.microsoft.com/business-applications-release-notes/April19/dynamics365-finance-operations/updatednavbar).
| **Skipt út fyrir aðra eiginleika?**   | Í verkvangsuppfærslu 24 var fyrst kynnt til sögunnar endurhönnuð yfirlitsstika sem býður upp á leit. |
| **Afurðasvæði sem haft er áhrif á**         | Vefbiðlari |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Frá og með apríl 2020 mun eldri yfirlitsstika ekki lengur vera í boði. Fram að því geta viðskiptavinir farið aftur í eldri yfirlitsstiku í gegnum síðuna **Valkostir afkastagetu biðlara**. |


## <a name="finance-and-operations-1002-with-platform-update-26"></a>Finance and Operations 10.0.2 með verkvangsuppfærslu 26


### <a name="legacy-default-action-behavior"></a>Eldri hegðun á sjálfvirkri aðgerð

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Eldri hegðun á sjálfvirkum aðgerðum í hnitanetum leiðir til óvænts dálks sem er með sjálfgefinn aðgerðartengil eftir að dálkar hnitanets hafa verið endurraðaðir með sérstillingum. Nýi eiginleikinn fyrir fasta sjálfgefna aðgerð leiðréttir þetta. Frekari upplýsingar er að finna í [Fastar sjálfgefnar aðgerðir í hnitanetum](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/sticky-default-action). |
| **Skipt út fyrir aðra eiginleika?**   | Fyrst í verkvangsuppfærslu 21 var eiginleikinn „fastar sjálfgefnar aðgerðir“ kynntur til sögunnar. Hægt er að virkja þennan eiginleika á síðunni **Valkostir afkastagetu biðlara**. |
| **Afurðasvæði sem haft er áhrif á**         | Hnitanet í vefbiðlaranum |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Frá og með apríl 2020 verða fastar sjálfgefnar aðgerðir sjálfgefin hegðun, án úrræða til að fara aftur í eldri hegðun. |

### <a name="legacy-is-one-of-filtering-experience"></a>Eldri „er einn af“ síunarupplifun

|&nbsp;   | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Síunarmöguleikinn „er einn af“ var endurhannaður í verkvangsuppfærslu 22 með það í huga að hann yrði eini „er einn af“ síunarmöguleikinn. |
| **Skipt út fyrir aðra eiginleika?**   | Í verkvangsuppfærslu 22 var fyrst boðið upp á endurbætur á síunarmöguleikanum „er einn af“ á síðunni **Valkostir afkastagetu biðlara**. Frekari upplýsingar er að finna í [Fínstillt „er ein af“ upplifun með síu](https://docs.microsoft.com/business-applications-release-notes/October18/dynamics365-finance-operations/improved-isoneof-filtering). |
| **Afurðasvæði sem haft er áhrif á**         | Vefbiðlari |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Frá og með apríl 2020 verður upplifunin „er ein af“ sjálfgefin hegðun, án úrræða til að fara aftur í eldri hegðun. |

### <a name="parameter-to-enable-sales-orders-with-multiple-project-contract-funding-sources"></a>Færibreyta til að virkja sölupantanir með marga uppruna fjármögnunar fyrir verksamninga
Stuðningur fyrir stofnun á verkmiðuðum sölupöntunum þar sem verksamningurinn er með marga uppruna fjármögnunar virka með stillingunni **Færibreytur verkefnastjórnunar** í **Leyfa sölupantanir fyrir verk með marga uppruna fjármögnunar**. Sjálfgefið er að þessi færibreyta er ekki virk. 

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Virknin verður alltaf virk eftir að færibreytan hefur verið fjarlægð. |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Virknin til að styðja verkmiðaðar sölupantanir með marga uppruna fjármögnunar verður alltaf virk.   |
| **Afurðasvæði sem haft er áhrif á**         |Færibreytan **Leyfa sölupantanir fyrir verk með mörgum fjármögnunaraðilum** verður fjarlægð. Eftirfarandi aðferðum verður breytt þegar færibreytan er fjarlægð: aðferðin **ctrlSalesOrderTable** í klasanum **ProjStatusType**, aðferðin **sannprófa** fyrir reitinn **ProjId** og aðferðin **keyra** í skjámyndinni **SalescreateOrder**. Eftirfarandi aðferðir verða úreltar þegar færibreytan er fjarlægð: **IsSalesOrderAllowedForMultipleFundingSources** í töfluskránni **ProjTable**, aðferðin **IsAllowSalesOrdersForMultipleFundingSourcesParamEnabled** í töfluskránni **ProjTable**, gagnareiturinn **AllowSalesOrdersForMultipleFundingSources** í skjámyndinni **ProjParameters** og skrárnar **ProjParameterEntity**, einkaaðferðin **IsAssociatedToMultipleFundingSourcesContract** í töfluskránni **ProjTable**. |
| **Dreifingarvalkostur**              | Allir  |
| **Staða**                         | Úrelding er fyrirhuguð fyrir útgáfulotu í apríl 2020. |

### <a name="legacy-workflow-reports-for-tracking-and-instance-status"></a>Eldri skýrslur verkflæðis fyrir stöðu rakningar og tilvika

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Eldri skýrslur verkflæðis fyrir stöðu rakningar og tilvika verða úreltar vegna þess að ekki er lengur vísað í þær úr flettingunni. Skýrsluheitin eru WorkflowWorkflowInstanceByStatusReport og WorkflowWorkflowTrackingReport. |
| **Skipt út fyrir aðra eiginleika?**   | Í staðinn er hægt að nota skjámyndina fyrir verkflæðissögu. |
| **Afurðasvæði sem haft er áhrif á**         | Vefbiðlari |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Stefnt er að því að fjarlægja virknina í apríl 2020. |

## <a name="finance-and-operations-1001-with-platform-update-25"></a>Finance and Operations 10.0.1 með verkvangsuppfærslu 25

### <a name="deprecated-apis-and-potential-breaking-changes"></a>Úrelt API og mögulegar skiptingar breytinga


#### <a name="deriving-from-internal-classes-is-deprecated"></a>Afleiðing frá innri klösum er úrelt

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Á undan verkvangsuppfærslu 25 var hægt að búa til klasa eða töflu sem kemur út frá innri klasa/töflu sem er skilgreind í öðrum pakka/einingu. Þetta er ekki starfsvenja öryggiskóðunar. Frá og með verkvangsuppfærslu 25 mun þýðandinn birta viðvörun. |
| **Skipt út fyrir aðra eiginleika?**   | Viðvörun þýðanda verður skipt út fyrir villu í verkvangsuppfærslu 26. Þessi breyting er samhæf afturvirk við keyrslu, sem þýðir að hægt er að nota verkvangsuppfærslu 25 eða nýrri á hvaða sandkassa- eða framleiðsluumhverfi sem er án þess að þurfa að breyta sérsniðnum kóða. Þessi breyting hefur aðeins áhrif á þróunar- og þýðingartíma.|
| **Afurðasvæði sem haft er áhrif á**         | Visual Studio þróunarverkfæri |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Viðvörunin verður að þýðingarvillu í verkvangsuppfærslu 26. |

#### <a name="overriding-internal-methods-is-deprecated"></a>Hnekking innri aðferða er úrelt

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Á undan verkvangsuppfærslu 25 var hægt að hnekkja innri aðferð í afleiddum klasa sem er skilgreindur í öðrum pakka/einingu. Þetta er ekki starfsvenja öryggiskóðunar. Frá og með verkvangsuppfærslu 25 mun þýðandinn birta viðvörun. |
| **Skipt út fyrir aðra eiginleika?**   | Þessi viðvörun verður skipt út fyrir þýðingarvillu í verkvangsuppfærslu 26. Þessi breyting er samhæf afturvirk við keyrslu, sem þýðir að hægt er að nota verkvangsuppfærslu 25 eða nýrri á hvaða sandkassa- eða framleiðsluumhverfi sem er án þess að þurfa að breyta sérsniðnum kóða. Þessi breyting hefur aðeins áhrif á þróunar- og þýðingartíma. |
| **Afurðasvæði sem haft er áhrif á**         | Visual Studio þróunarverkfæri |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Viðvörunin verður að þýðingarvillu í verkvangsuppfærslu 26. |

## <a name="finance-and-operations-1000-with-platform-update-24"></a>Finance and Operations 10.0.0 með verkvangsuppfærslu 24

### <a name="renaming-released-products"></a>Losuðum afurðum gefið nýtt heiti 
| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þegar þú notar aðgerðina **Endurnefna aðallykil** til að breyta vörukenni losaðrar vöru eru aðeins beinar tilvísanir framandlykla uppfærðar. Allar aðrar tilvísanir í útgefna vöru, svo sem frá framleiðslupöntunum, geymir gamla vörukennið. Fyrir vikið gætu verið ósamkvæm gögn sem munu á endanum loka fyrir viðskiptaferla. |
| **Skipt út fyrir aðra eiginleika?**   | Nei. |
| **Afurðasvæði sem haft er áhrif á**         | Vöruupplýsingastjórnun |
| **Dreifingarvalkostur**              | Allir  |
| **Staða**                         | Fjarlægt frá og með Finance and Operations 10.0.0. með verkvangsuppfærslu 24.|


## <a name="finance-and-operations-813-with-platform-update-23"></a>Finance and Operations 8.1.3 með verkvangsuppfærslu 23

### <a name="sql-server-reporting-services-reportviewer-control"></a>Stjórntæki fyrir ReportViewer SQL Server Reporting Services
Viðskiptavinir geta notað aðgerðina **Útflutningur** sem innfellt stjórntæki ReportViewer fyrir SQL Server Reporting Services (SSRS) býður upp á til að sækja skjöl sem forrit Finance and Operations búa til. Þessi HTML-kynning á skýrslunni býður notendum upp á forskoðun á skjalinu án blaðsíðutals.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Forskoðun á HTML-kynningunni án blaðsíðutals er **ekki** í fullu samræmi við raunverulegu skjölin sem Finance and Operations búa til að lokum. Með því að samþykkja að fullu PDF sem staðlað snið fyrir viðskiptaskjöl geta notendur nýtt sér nútímalega skoðun með endurbættum afköstum þegar skýrslur forrits eru búnar til. |
| **Skipt út fyrir aðra eiginleika?**   | Að halda áfram, PDF skjöl verða sjálfgefið snið fyrir skýrslur sem Finance and Operations búa til.   |
| **Afurðasvæði sem haft er áhrif á**         | Þessi breyting hefur **ekki** áhrif á atburðarásir viðskiptavinar þar sem skýrslum er dreift rafrænt eða sendar beint til prentara.    |
| **Dreifingarvalkostur**              | Allir  |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. Virknin til að forskoða sjálfkrafa skýrslur forrits með því að nota innfelldan PDF-lesara er á dagskrá fyrir verkvangsuppfærslu í maí 2019. |

### <a name="client-kpi-controls"></a>KPI-stýring biðlara
Innfellda afkastavísa (KPI) er hægt að þróa í Visual Studio af þróunaraðila og sérsniðið enn frekar af notanda.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Staðbundin biðlarastýring sem er notuð til að skilgreina afkastavísa er með lága upptöku viðskiptavinar og treystir á að þróunaraðili bæti við rekjanlegum mælingum. |
| **Skipt út fyrir aðra eiginleika?**   | PowerBI.com þjónusta býður upp á heimsklassa tól til að skilgreina og stjórna afkastavísum sem byggist á gögnum frá utanaðkomandi aðilum.  Í væntanlegri útgáfu er áformað að gera þér kleift að fella inn lausnir sem eru hýstar á PowerBI.com í vinnusvæðum forrits.   |
| **Afurðasvæði sem haft er áhrif á**         | Þessi uppfærsla kemur í veg fyrir að þróunaraðilar kynni nýjar stýringar afkastavísa í Visual Studio hönnuði.    |
| **Dreifingarvalkostur**              | Allir  |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="deprecated-apis-and-future-breaking-changes"></a>Úrelt API og framtíðarskiptingar breytinga

#### <a name="field-groups-containing-invalid-field-references"></a>Reitahópar sem innihalda ógilda tilvísanareiti

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Mögulegt er fyrir skilgreiningar á lýsigögnum töflu að hafa reitahópa sem innihalda ógilda tilvísanareiti. Ef sett upp getur það leitt til keyrsluvillu í Fjárhagsskýrslugerð og SQL Server Reporting Services (SSRS). Þetta vandamál er sem stendur flokkað sem *viðvörun þýðanda* frekar en *villa* sem þýðir að stofnun virkjanlegs pakka og uppsetning geti haldið áfram án þess að laga vandamálið. Til að leysa þennan vanda þarf að:<br><br>1. Fjarlægja ógilda tilvísunarreitinn úr skilgreiningu töflureitahópsins.<br><br>2. Endurþýða.<br><br>3. Tryggja að tekið sé á öllum viðvörunum og villum. |
| **Skipt út fyrir aðra eiginleika?**   | Þessi viðvörun verður skipt út fyrir þýðingarvillu í framtíðinni. |
| **Afurðasvæði sem haft er áhrif á**         | Visual Studio þróunarverkfæri |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Úrelt: Viðvörunin er þýðingartímavilla í framtíðinni með uppfærslum á verkvangi fyrir útgáfu 10.0.11 af Finance and Operations forritum. |

#### <a name="complete-list"></a>Heildarlisti
Til að fá aðgang að heildarlista afkastavísa sem verið er að úrelda skal sjá [Úrelding á aðferðum og einingum lýsigagna](deprecation-deletion-apis.md).

## <a name="finance-and-operations-81-with-platform-update-20"></a>Finance and Operations 8.1 með verkvangsuppfærslu 20

### <a name="batch-transfer-rules-for-subledger-journal-account-entries"></a>Runuflutningsreglur fyrir lyklafærslur undirbókar
Samstillta flutningsstillingin er felld úr gildi í færibreytum fjárhags.  Þessari stillingu er aðeins skipt út fyrir ósamstillta og áætlaða runu, sem þegar er til staðar sem valkostir fyrir flutning. Frekari upplýsingar er að finna á blogginu [Færibreytur fjárhags - Reglur fyrir runuflutning](https://community.dynamics.com/365/financeandoperations/b/financials/archive/2019/03/15/general-ledger-parameters-batch-transfer-rules).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Við fjarlægjum samstillingarvalkostinn vegna þess að hann hefur áhrif á frammistöðu kerfisins. |
| **Skipt út fyrir aðra eiginleika?**   | Ósamstillt og áætluð runa eru valkostir til að nota í stað samstilltrar.   |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur, Viðskiptaskuldir, Viðskiptakröfur, Innkaup, Kostnaður    |
| **Dreifingarvalkostur**              | Allir  |
| **Staða**                         | Úrelt: Tímarammi markmiðs um fjarlægingu á virkni er útgáfa 10.0.|

### <a name="electronic-reporting-for-russia"></a>Rafræn skýrslugerð fyrir Rússland
Eiginleiki til að stilla .txt- og .xml-skráarsnið yfirlýsinga. 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir rafræna skýrslugerð. |
| **Skipt út fyrir aðra eiginleika?**   | Já. |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Fjarlægt frá og með Finance and Operations 8.1. með verkvangsuppfærslu 20. |

### <a name="financial-reports-generator-for-russia"></a>Fjárhagsskýrslugerðarforrit fyrir Rússland
Verkfæri til að setja upp gagnasöfnun fyrir bókhald og skattaskýrslur og flytja út gögn í XLS- og DOC-skýrslusniðmát. Virkir hlutar: Flytja út gögn í XLS- og DOC-skýrslusniðmát, fyrirspurnir, föst skilyrði eru fjarlægð. 

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Fjarlægðum hlutum er skipt út fyrir rafræna skýrslugerð. |
| **Skipt út fyrir aðra eiginleika?**   | Já. Notandaviðmót fyrir uppsetningu á fjárhagsskýrslum ætti að nota til að setja upp gagnasöfnunarreglur með fjárhagslyklum eða skattskrám. Flytja út gögn í ýmisar skáargerðir, föst skilyrði og fyrirspurnir eins og gagnasöfnunarreglur ættu að vera stilltar í rafrænni skýrslugerð. |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur. |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Fjarlægt frá og með Finance and Operations 8.1. með verkvangsuppfærslu 20. |

### <a name="integration-with-external-providers-for-sending-electronic-reporting-through-communication-channels-for-russia"></a>Samþætting við ytri þjónustuveitendur við að senda rafræna skýrslugerð í gegnum samskiptarásir fyrir Rússland
Eiginleiki flytur út myndaðar rafrænar skrár yfirlýsinga í möppu til frekari sendingar til opinberra veitenda rafrænna skýrslugerða auk þess að flytja inn stöðu til baka.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir stillanlega eiginleika rafrænna skilaboða. |
| **Skipt út fyrir aðra eiginleika?**   | Já.  |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur, Skattur |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Fjarlægt frá og með Finance and Operations 8.1. með verkvangsuppfærslu 20. |


### <a name="profit-tax-register-wizard"></a>Leiðsagnarforrit fyrir skattskrá hagnaðar
Eiginleiki til að búa til sniðmát fyrir nýjar skattskrár hagnaðar. Þessi eiginleiki býr til X++ hluti fyrir nýjar skrár, sem eru síðan búnar til sem sniðmát þar sem viðeigandi reiknireglum er bætt við.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Eiginleiki er ekki samhæfur við stækkunarhæfnislíkan Finance and Operations. |
| **Skipt út fyrir aðra eiginleika?**   | Ekkert |
| **Afurðasvæði sem haft er áhrif á**         | Skattur |
| **Dreifingarvalkostur**              | Allir |
| **Staða**                         | Fjarlægt frá og með Finance and Operations 8.1. með verkvangsuppfærslu 20. |


## <a name="finance-and-operations-80-with-platform-update-15"></a>Finance and Operations 8.0 með verkvangsuppfærslu 15
Engir eiginleikar hafa verið fjarlægðir eða úreltir með þessari útgáfu. Verkvangsuppfærsla 15 er uppsöfnuð og inniheldur nýja eða breytta eiginleika frá verkvangsuppfærslu 13, verkvangsuppfærslu 14 og verkvangsuppfærslu 15.

## <a name="finance-and-operations-enterprise-edition-73-with-platform-update-12"></a>Finance and Operations, Enterprise Edition 7.3 með verkvangsuppfærslu 12

### <a name="personalized-product-recommendations"></a>Sérsniðnar afurðaráðleggingar 
Frá og með 15. febrúar, 2018, munu smásalar ekki lengur geta birt sérsniðnar vöruráðleggingar á sölustaðartæki. Frekari upplýsingar eru í [Yfirlit afurðarráðlegginga](../../../commerce/product-recommendations.md).  

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Núverandi útgáfa af ráðleggingaþjónustu vörunnar verður fjarlægð og eiginleikinn endurhannaður með betra reikniriti og nýrri smásölumiðuðum möguleikum.  |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Þó eru áform um að fá þennan eiginleika aftur inn sem vægi við nýja ráðleggingarþjónustu eftir haustið 2018.   |
| **Afurðasvæði sem haft er áhrif á**         | Sérsniðnar vöruráðleggingar á sölustað.                                                    |
| **Dreifingarvalkostur**              | Allir                                                                                      |
| **Staða**                         |Fjarlægt þann 15. febrúar, 2018. Þetta hefur áhrif á viðskiptavini sem keyra Dynamics 365 for Operations 1611 og eldri útgáfur.  |

### <a name="extension-of-the-list-of-electronic-reporting-er-functions"></a>Útvíkkun listans yfir aðgerðir Rafrænnar skýrslugerðar
Möguleikinn á að kynna sérsniðnar aðgerðir sem notaðar eru í ER-tjáningarbyggingu (til að fá frekari upplýsingar, sjá [Útvíkka lista yfir aðgerðir Rafrænnar skýrslugerðar (ER)](../../dev-itpro/analytics/general-electronic-reporting-formulas-list-extension.md)) er ekki studdur lengur. Vegna breytinga á ER API, varð API til að kalla innbyggðar aðgerðir frá ER tjáningarbyggingu innra API og ekki hægt að útvíkka lengur.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Frumkvæðis innsiglun kóða  |
| **Skipt út fyrir aðra eiginleika?**   | Ekkert. Í hvert skipti sem þörf er á nýrri innbyggðu aðgerð verður að senda nýtt framlengingarbeiðni til ER rammahópsins.<br><br>Sem tímabundið verk um það leyti sem umbeðin aðgerð er í þróun hjá ER teyminu er hægt að forrita nauðsynlega rökfræði sem aðferð sérsniðins umsóknarflokks. Þessa aðferð er hægt að nálgast í ER-tjáningu sem eiginleika viðbætts ER-gagnasafns af **Umsókn/Flokkur** gerðinni sem vísar til þessa sérsniðna umsóknarflokks.  |
| **Afurðasvæði sem haft er áhrif á**         | Umgjörð rafrænnar skýrslugerðar                                                      |
| **Dreifingarvalkostur**              | Allir                                                                                      |
| **Staða**                         | Fjarlægt frá og með Finance and Operations, Enterprise Edition 7.3.    |

### <a name="inventory-by-item-group-and-inventory-by-inventory-dimension-aging-reports"></a>Birgðir eftir vöruflokki og birgðir eftir aldursskýrslum birgðavídda

Þessar tvær skýrslur eru ekki lengur studdar í Finance and Operations. Í staðinn er hægt að nota skýrslu **Aldur birgða** til að bæta notandaupplifunina.

| &nbsp;  | &nbsp; |
|--------------|-----------------------|
| **Ástæða afskrifta**       | Afrituð virkni  |
| **Skipt út fyrir aðra eiginleika?** | Já. Þessar skýrslur hafa verið skipt út fyrir skýrslu **Aldur birgða**.     |
| **Afurðasvæði sem haft er áhrif á**       | Birgðastjórnun, Kostnaðarstjórnun        |
| **Dreifingarvalkostur**        | Allir|
| **Staða**                       | Úrelt: Valmyndaratriði þessara tveggja skýrslna hafa verið fjarlægðar í útgáfu 7.3. Kóðann fyrir skýrslurnar er samt sem áður enn að finna í afurðinni. Áætlað er að fjarlægja kóðann í framtíðarútgáfu. |

### <a name="power-bi-content-packs-available-on-appsource"></a>Power BI efnispakkar eru tiltækar á AppSource
Efnispakkarnir **Kostnaðarstjórnun**, **Fjárhagsleg frammistaða** og **Retail Channel Performance** sem eru í boði á [Microsoft AppSource](https://appsource.microsoft.com) síunni , eru úreltir vegna uppfærslur á vöru í Microsoft Power BI. Kerfisstjórnunareyðublöð sem notuð eru til að dreifa þessum efnispökkum til PowerBI.com eru einnig úreltir í Finance and Operations.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Vöruuppfærslur í Microsoft Power BI. |
| **Skipt út fyrir aðra eiginleika?**   | Efnispakkarnir **Kostnaðarstjórnun**, **Fjárhagsleg frammistaða** og **Afköst smásölurásar**, sem eru í boði á [AppSource](https://appsource.microsoft.com) síða, er skipt út fyrir greiningarforrit sem leyfa lausnasamþættingu á gagnagrunni stigi. Frekari upplýsingar um greiningarforrit, sjá [Innfellt Power BI í vinnusvæði](../../dev-itpro/analytics/embed-power-bi-workspaces.md).    |
| **Afurðasvæði sem haft er áhrif á**         | Kostnaðarstjórnun, Fjármál og Smásala                                                                                               |
| **Dreifingarvalkostur**              | Einungis ský (Samþætting við PowerBI.com er ekki studd við dreifingu á staðnum.)                                                                                                            |
| **Staða**                         | Úrelt: Tímarammi markmiðs um að fjarlægja virknina er Q2 2018.    |

### <a name="standard-ui-in-data-management-workspace"></a>Staðlað Notendaviðmót í vinnusvæði gagnastjórnunar

Staðlað notendaviðmót í gagnastjórnun er Legacy-UI, sem er sjálfgefna notendaviðmótið sem birtist notendum þegar þeir heimsækja vinnusvæði gagnastjórnunar.

| &nbsp;  | &nbsp; |
|------------------|-------------------------|
| **Ástæða úreldingar/fjarlægingar** | Við erum að fjárfesta í veitingu nýrrar notendaupplifunar í nýja notendaviðmótinu.             |
| **Skipt út fyrir aðra eiginleika?**   | Nýja notendaviðmótið, sem kallast *Aukið yfirlit*, kemur í stað gamla notendaviðmótsins.            |
| **Afurðasvæði sem haft er áhrif á**         | Vinnusvæði gagnastjórnunar                                                     |
| **Dreifingarvalkostur**              | Allir                                                                           |
| **Staða**                         | Úrelt: Tímarammi markmiðs um að fjarlægja virknina er Q2 2018. |

### <a name="excise-sales-tax-service-tax-for-india"></a>Vörugjald, Virðisaukaskattur, Þjónustuskattur fyrir Indland

Þessar skattar hafa verið felldar inn í Vöru- og þjónustuskatt á Indlandi.

|  &nbsp;                                           |      &nbsp;                                                                   |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Ástæða úreldingar eða fjarlægingar**       | Þessar skattar hafa verið felldar inn í Vöru- og þjónustuskatt á Indlandi.                          |
| **Skipt út fyrir aðra eiginleika?**            | Indverskur vöru- og þjónustuskattur                                                              |
| **Afurðasvæði sem haft er áhrif á**                  | Skattur                                                                     |
| **Dreifingarvalkostur**                       | Allar einingar                                                   |
| **Staða**                                  | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |    

### <a name="file-validation-utility-fvu-for-india"></a>Villuleitarhjálparforrit (FVU) fyrir Indland

|              &nbsp;                               |      &nbsp;                                                                   |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Ástæða úreldingar eða fjarlægingar**       | Of lítil notkun viðskiptavina.                                                  |
| **Skipt út fyrir aðra eiginleika?**            | Númer                                                                      |
| **Afurðasvæði sem haft er áhrif á**                  | Staðgreiðsluskattur á Indlandi                                                  |
| **Dreifingarvalkostur**                       | Allar einingar                                                                    |
| **Staða**                                  | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.   |        

### <a name="tdstcs-certificate-for-india"></a>TDS/TCS vottorð fyrir Indland

Notendur geta sótt þetta frá ríkisstjórnargáttinni.

|             &nbsp;                                |    &nbsp;                                                                     |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Ástæða úreldingar eða fjarlægingar**       | Of lítil notkun viðskiptavina.                                                  |
| **Skipt út fyrir aðra eiginleika?**            | Númer                                                                      |
| **Afurðasvæði sem haft er áhrif á**                  | Staðgreiðsluskattur á Indlandi                                                  |
| **Dreifingarvalkostur**                       | Allar einingar                                                                   |
| **Staða**                                  | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.     |    

### <a name="exportimport-exim-incentive-scheme-for-india"></a>Útflutningur/Innflutningur (EXIM) hvatningarkerfi fyrir Indland


|              &nbsp;                               |        &nbsp;                                                                 |
|---------------------------------------------|-------------------------------------------------------------------------|
| **Ástæða úreldingar eða fjarlægingar**       | Of lítil notkun viðskiptavina.                                                  |
| **Skipt út fyrir aðra eiginleika?**            | Númer                                                                      |
| **Afurðasvæði sem haft er áhrif á**                  | Flytja inn og flytja út                                                       |
| **Dreifingarvalkostur**                       | Allar einingar                                                                    |
| **Staða**                                  | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.  |    


## <a name="dynamics-365-for-retail-72"></a>Dynamics 365 for Retail 7.2

### <a name="personalized-product-recommendations"></a>Sérsniðnar afurðaráðleggingar 
Frá og með 15. febrúar, 2018, munu smásalar ekki lengur geta birt sérsniðnar vöruráðleggingar á sölustaðartæki. Frekari upplýsingar eru í [Yfirlit afurðarráðlegginga](../../../commerce/product-recommendations.md).  

|  &nbsp; |  &nbsp;|
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Núverandi útgáfa af ráðleggingaþjónustu vörunnar verður fjarlægð og eiginleikinn endurhannaður með betra reikniriti og nýrri smásölumiðuðum möguleikum.  |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Þó eru áform um að fá þennan eiginleika aftur inn sem vægi við nýja ráðleggingarþjónustu eftir haustið 2018.   |
| **Afurðasvæði sem haft er áhrif á**         | Sérsniðnar vöruráðleggingar á sölustað.                                                    |
| **Dreifingarvalkostur**              | Allir                                                                                      |
| **Staða**                         |Fjarlægt þann 15. febrúar, 2018. Þetta hefur áhrif á viðskiptavini sem keyra Dynamics 365 for Retail 7.2 og eldri útgáfur. |


## <a name="finance-and-operations-enterprise-edition-july-2017-with-platform-update-8"></a>Finance and Operations, Enterprise Edition júlí 2017 með verkvangsuppfærslu 8

### <a name="currency-conversion-for-accounting-and-reporting-currencies"></a>Umreikningur gjaldmiðils fyrir bókhald og skýrslugjaldmiðla

Umreikningur gjaldmiðils fyrir bókhald og skýrslugjaldmiðla var kynntur þegar evran var kynnt.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Takmarkaður notkun og viðbót við afrita lögaðila sem virkni í staðinn.      |
| **Skipt út fyrir aðra eiginleika?**   | Nei, en eiginleikunum „Afrita lögaðila“ og „Skilgreiningar“ var bætt við til að auðvelda flutning til fyrirtækis sem hefur breyttar grunnkröfur. |
| **Afurðasvæði sem haft er áhrif á**         | Fjármálastjórnun     |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.   |


### <a name="warehouse-mobile-devices-portal"></a>Gátt fyrir fartæki vöruhúss

Vöruhús fjarskiptatæki portal (WMDP) var sjálfstæður þáttur sem var gert ráð fyrir verslunarsvæðis á sjálfnýtingu. Þessi hluti er ekki lengur studdur í Finance and Operations. Upprunalegt smáforrit sem bætir notandaupplifunina hefur komið í stað virkni WMDP.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Afrituð virkni.       |
| **Skipt út fyrir aðra eiginleika?**   | Já. Eiginleikanum hefur verið skipt út fyrir Finance and Operations - Warehousing. Nánari upplýsingar um uppsetningu og skilyrði er að finna í [Setja upp og skilgreina yfirlit yfir forritið Warehousing](../../../supply-chain/warehousing/install-configure-warehousing-app.md). |
| **Afurðasvæði sem haft er áhrif á**         | Vöruhúsastjórnun, flutningsstjórnun     |
| **Dreifingarvalkostur**              | Vöruhús fjarskiptatæki portal (WMDP) var sjálfstæður þáttur sem var gert ráð fyrir verslunarsvæðis á sjálfnýtingu.               |
| **Staða**                         | Úrelt: Tímarammi markmiðs um að fjarlægja virknina er Q4 2019.   |

### <a name="advanced-bank-reconciliation-matching-rule-for-manual-matching"></a>Jöfnunarregla ítarlegrar afstemmingar banka fyrir handvirka jöfnun

Jöfnunarregla var notuð til að velja og merkja bankaskjal við handvirka jöfnun skjala í afstemmingarvinnublaðinu

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Takmörkuð notkun.                                                                         |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Síunarskilyrði dálka ætti að nota til að finna skjöl fyrir afstemmingu. |
| **Afurðasvæði sem haft er áhrif á**         | Reiðufjár- og bankastjórnun                                                               |
| **Dreifingarvalkostur**              | Öll                                                                                    |
| **Staða**                         | Fjarlægt frá og með júlí 2017.                                                               |

## <a name="dynamics-365-for-operations-1611-with-platform-update-3"></a>Dynamics 365 for Operations 1611 með verkvangsuppfærslu 3

### <a name="aeb-payment-formats-for-spain"></a>AEB-greiðslusnið fyrir Spán

Consejo Superior Bancario-greiðslusnið voru notuð til að senda greiðsluskrár til bankans fyrir viðskiptavina- og lánardrottnagreiðslur. Innihald þessara sniða var ákvarðað af Asociación Española de Banca. Það tekur á Cuaderno 19, 32, 58, 34.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                                  |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO20022 millifærsla fjármuna og snið beingreiðslu fyrir Spán |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur, viðskiptaskuldir                                    |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.           |

### <a name="bank-payments-transfer-for-lithuania"></a>Flutningar bankagreiðslur fyrir Litháen

Greiðslufærslur banka voru prentaðar og myndaðar með útflutningssniði greiðslufærslna (LT) fyrir Litháen. Litháíska markaðinn hóf að nota LITAS, sameinuðum rafræna bankakerfinu, 2005.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                        |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Litháen     |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir                                               |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>BBS Direkte Remittering greiðslusnið fyrir Noreg

Greiðslusnið BBS Direkte Remittering innihalda útflutning innheimtu fyrir greiðsla viðskiptavinar (beingreiðsla) og innflutning svarskilaboða.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.  |
| **Skipt út fyrir aðra eiginleika?**   | Greiðslusnið viðskiptavinar AvtaleGiro fyrir noregs má nota til að mynda skilaboð beingreiðslu. Innflutningur svarskilaboða verða innleidd í síðari útgáfum. |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur, viðskiptaskuldir   |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                                                                                                 |

### <a name="chart-of-accounts-tool-for-spain"></a>Bókhaldslykill fyrir Spán

Þessa verkfæris er notaður þegar bókhaldslyklum á Spáni krefst meiriháttar breytingar. Notendur geta flytja nýja bókhaldslykla í Microsoft Excel eða textasnið og einnig er hægt að flytja inn fjárhagsskýrslur.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Takmörkuð notkun                                                  |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                                             |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur                                                 |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="dom80-payment-format-for-belgium"></a>Dom80 greiðslusnið fyrir Belgíu

Eldra belgískt Greiðslusnið fyrir innheimtu (beingreiðsla).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                          |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO 20022 beingreiðslusnið fyrir Belgíu.         |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur                                            |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG greiðslusnið fyrir Sviss

DTA/EZAG snið eru samþætta í ESR-kerfinu því þeau geta borið áfram tilvísunarnúmer. Þar sem tilvísunarnúmerið er ekki tilskilinn, má nota sniðin til að vinna allar lánardrottnagreiðslur. Þessara sniða eru notaður af fyrirtækjum sem hafa á bankareikning í staðsetningu annars staðar en “Postfinance”.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                        |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Sviss   |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir                                               |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>EDIFACT-DIRDEB greiðslusnið fyrir Austurríki

EDIFACT-DIRDEB Greiðslusnið innheimtu (beingreiðsla).

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                          |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO 20022 beingreiðslusnið fyrir Austurríki.         |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur                                            |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="edivat-for-belgium"></a>EDIVAT fyrir Belgíu

EDIVAT er úreltum Belgískar staðal fyrir rafræna skattskýrslu sent með öruggum pósti. Dynamics AX 2012 heldur áfram skrifvarið lausn til að virkja aðgang að söguleg gögn.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau eiginleiki eru ekki lengur notaður.                           |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                                             |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur                                                 |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>innflutningssnið greiðslu eGiro EDIFACT fyrir Noreg

eGiro byggir á alþjóðlegum staðli Sameinuðu þjóðanna EDIFACT CREMUL, (Multiple Credit Advice Message), notaður fyrir sjálfvirka bókun á greiðslum viðskiptavina. Í Dynamics AX er eGiro er innleitt sem innflutningssnið greiðslu viðskiptavinar.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                                                     |
| **Skipt út fyrir aðra eiginleika?**   | Já, innflutningstilkynning ISO20022 Camt. 054. |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur                                                                       |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                            |

### <a name="external-inventory-for-poland"></a>Ytri birgðir fyrir Pólland

Sönnun um að vörur teknar frá lánardrottni fyrir sölur án kaupa. Vörur sem eru meðhöndlaðar í ytri birgðir hafa ekki áhrif á staðalaðar birgðir, og má selja þær og síðan kaupa sjálfkrafa. Ferlið stofnar raunverulegum birgðahreyfingar.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir aðra eiginleika                                    |
| **Skipt út fyrir aðra eiginleika?**   | Já, kjarnaaðgerðir vörusendingar á Innleið                |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir, birgðastjórnun                         |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="financial-reports-generator-for-eastern-europe"></a>Myndun fjárhagsskýrslna fyrir austur-Evrópa

Verkfæri er notað til að setja upp gagnasöfnun fyrir bókhald og skattaskýrslur og flytja út gögn í sniðmát skýrslu XLS og DOC.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Takmörkuð notkun                                                                            |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Forritið verður skipt út af skilgreiningar Rafræna skýrslugerð í framtíðinni. |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur                                                                           |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Flytja inn greiðslufærslur viðskiptavinar fyrir Finnland

Hægt er að velja innflutningssnið fyrir finnskar greiðslur sem flytur inn greiðslufærslur viðskiptavinar úr ytri skrá frá bankanum.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                                                     |
| **Skipt út fyrir aðra eiginleika?**   | Já, innflutningstilkynning ISO20022 Camt. 054. |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur                                                                       |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                            |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Innflutningur greiðslufærsla í færslubók fjárhags fyrir Finnland

Sniðið sem er tiltekið fyrir Finnland er notað til að flytja inn bókhaldsfærslur í fjárhag.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                                                     |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO20022 Camt. 053-innflutningur bankayfirlits með ítarlegri bankaafstemmingu. |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur                                                                       |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                            |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Samþætting við Isabel samstillt (CIS) fyrir Belgíu

Isabel er ramma fyrir rafræn bankaviðskipti í Evrópu og de-facto staðall í Belgíu.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Hætt hefur verið samþætting við Isabel-biðlara.   |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Greiðslusnið sem eru ekki lengur notaður er skipt fyrir ISO20022 greiðslusnið millifærsla fjármuna fyrir Belgíu. |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir     |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.    |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Breytingar á bókhaldslykill og bókhaldsreglur fyrir Spán

Þessir eiginleikar eru notaðir fyrir Breytingar á bókhaldslykill og bókhaldsreglur fyrir Spán Það varpar lyklum til að aðstoða við að umbreyta gamla bókhaldslykilinn í nýja bókhaldslykil og ber saman fyrra fjárhagsárið með nýja fjárhagsárið, jafnvel þó þær voru bókaðar á mismunandi lykilnúmer.

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Takmörkuð notkun                                                  |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                                             |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur                                                 |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="pagamento-fornittori-vendor-payment-format"></a>Greiðslusnið lánardrottins Pagamento Fornittori

Eldri Ítölsk greiðslusnið fyrir millifærsla fjármuna.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                          |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Ítalía         |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir                                               |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="payment-export-formats-for-estonia"></a>Greiðsluútflutningssnið fyrir Eistland

Telehansa og Teleservice-snið notuð til að flytja út greiðslu banka.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                        |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Eistland       |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir                                               |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="payment-file-archive-for-norway"></a>Greiðsluskrársafn fyrir Noreg

Þegar greiðsluskrár eru myndaðar, geymir í skráasafn sjálfkrafa allar skrár sem eru stofnaðar, jafnvel skrár sem voru áður skrifuð eða lesa.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir aðra eiginleika                                        |
| **Skipt út fyrir aðra eiginleika?**   | Já, Safnvistaðar vinnslur í Rafrænni skýrslugerð                            |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur, viðskiptaskuldir, fyrirtækisstjórnun |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.     |

### <a name="payment-import-formats-for-estonia"></a>Greiðsluinnflutningssnið fyrir Eistland

Telehansa og TeleTeenus-snið notuð til að flytja inn greiðslu banka.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                                                    |
| **Skipt út fyrir aðra eiginleika?**   | Já, bankainnflutningstilkynning ISO20022 Camt. 054. |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur                                                                        |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                             |

### <a name="payroll-information-in-human-resources"></a>Launaupplýsingar í Mannauði

Mannauður, launaupplýsingar

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þessi aðgerð hefur verið skipt fyrir síðurnar Laun og Mannauður.  |
| **Skipt út fyrir aðra eiginleika?**   | **Fríðindi**, **Tekjur**, og aðrar tengdar síður sem voru áður í BNA Laun hafa verið endurskilgreind, og eru nú hluti kjarnauppsetning Mannauðs til að styðja við ytri launavinnslu. Þessi virkni er opnuð með því að nota **Mannauður 1** \> **Laun** skilgreiningarlykillinn. |
| **Afurðasvæði sem haft er áhrif á**         | Mannauður, Laun   |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Operations útgáfu 1611.    |

### <a name="performance-management-goal-workflow"></a>Verkflæði markmiðs frammistöðustjórnunar

Frammistöðustjórnun inniheldur markmiðastjórnun og samþættingu við yfirferðir frammistöðu.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Frammistöðustjórnun var endurhönnuð og blaðsíðufjöldi var minnkað til að einfalda ferlið.                 |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Markmið eru sýnileg stjórnendum gegnum gátt fyrir Sjálfsafgreiðsla stjórnanda og hægt er að breyta og skoða af stjórnanda. |
| **Afurðasvæði sem haft er áhrif á**         | Mannauðsstjórnun       |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Operations útgáfu 1611.    |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>Postgirot og Postgirot Utland greiðslusnið fyrir Svíþjóð

Postgirot og Postgirot Utland greiðslusnið fyrir Svíþjóð

|&nbsp;   |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                        |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Svíþjóð        |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir                                               |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="radio-frequency-identifier"></a>Rafmerki

Rafmerki (RFID) er gagnasöfnunartækni sem notar Rafræn tög til að geyma auðkennisgögn og no-line-of-sight requirement reader til að grípa auðkenni gögn.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Lítil notkun viðskiptavina og takmörkuðum eiginleikum.   |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                              |
| **Afurðasvæði sem haft er áhrif á**         | Birgðir                            |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Operations 1611. |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Skýrsla um opinbera tölusetningu reikninga í Lettlandi.

Lettneskt löggjöf veitir tilteknar reglur um hvernig sölureikninga skulu númeraðir. Eiginleikinn leyfir þér að úthluta tilteknum númer á sölureikninga, byggt á notanda eða notendaflokk. Síðan er hægt að mynda skýrslu eða xml-skrá. Einnig er hægt að prenta skýrslu um reikningsnúmera sem eru notaðar.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Í opinber tölusetning reikninga þarf ekki lengur að halda við. Skýrslu um notuð reikningsnúmer er ekki lengur þörf. |
| **Skipt út fyrir aðra eiginleika?**   | Númer       |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur    |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.  |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>Setja upp nöfn stjórnanda og aðalbókari fyrirtækis fyrir Litháen

Nöfn stjórnanda og aðalbókari fyrirtækis má tilgreina í upplýsingar um fyrirtækið og notaðar í útprentunum mismunandi staðbundna skýrslu.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skipt út fyrir aðra eiginleika                                     |
| **Skipt út fyrir aðra eiginleika?**   | Já, er hægt að nota uppsetningu embættismanna í sama tilgangi.   |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir, viðskiptakröfur, reiðufjár- og bankastjórnunar |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.  |

### <a name="shipping-carrier-interface"></a>Viðmót farmflytjanda

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Afrituð virkni   |
| **Skipt út fyrir aðra eiginleika?**   | Að hluta til skipt út fyrir Flutningsstjórnun |
| **Afurðasvæði sem haft er áhrif á**         | Sala og markaðssetning, Birgðastjórnun  |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Operations útgáfu 1611.  |

### <a name="telepay-payment-formats-for-norway"></a>Telepay greiðslusnið fyrir Noreg

Greiðslusnið Telepay innihalda útflutning greiðsla lánardrottins (millifærsla fjármuna) og innheimtubréf (beingreiðsla) til viðskiptavina.

|&nbsp;   |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                                                        |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO20022 greiðslusnið kreditfærslu og AvtaleGiro-greiðslusnið viðskiptavinar fyrir Noreg, ásamt innflutningi á skilaskrám banka pain.002 og camt.054. |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur, viðskiptaskuldir                                                          |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                                 |

### <a name="vendor-payment-export-formats-for-finland"></a>Útflutningssnið lánardrottnagreiðslu fyrir Finnland

Tvö snið fyrir útflutning á greiðslum eru tiltækar fyrir Finnland. LM02 (FI) er notuð fyrir innanlandsgreiðslur og LUM2 (FI) er notað fyrir erlendar greiðslur.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þau greiðslusnið eru ekki lengur notaður.                        |
| **Skipt út fyrir aðra eiginleika?**   | Já, ISO20022 greiðslusnið millifærsla fjármuna fyrir Finnland       |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir                                               |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="warehouse-management-ii"></a>Vöruhúsakerfi II

|  &nbsp; |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Vöruhúsakerfi II-lausn (WMS II) sem var tiltæk í virkni tvíteknu kerfiseininga **Birgðastjórnunar** sem er í einingunni **Vöruhúsakerfi** sem var gefin út í Dynamics AX 2012 R3.                                                                         |
| **Skipt út fyrir aðra eiginleika?**   | Einingin **Vöruhúsakerfi** sem var gefin út í AX 2012 R3, Dynamics AX 2012, R3 CU8 og Dynamics AX 2012 R3 CU9 kemur í stað eiginleika vöruhúsakerfis II. Nýja kerfið hefur fleiri ítarlegar aðgerðir og sveigjanlegri vöruhúsakerfisferli en vöruhúsakerfi II. |
| **Afurðasvæði sem haft er áhrif á**         | Birgðastjórnun, sölu og markaðssetningu, innkaup og uppruni   |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Operations útgáfu 1611.    |

### <a name="worker-reminders-in-human-resources"></a>Áminningar starfsmanna í mannauði

Mannauður, launaupplýsingar

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Lítil notkun                                                           |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                                                  |
| **Afurðasvæði sem haft er áhrif á**         | Mannauður                                                     |
| **Staða**                         | Fjarlægð frá og með Dynamics 365 for Operations útgáfu 1611 |

### <a name="workflow-for-creating-goals"></a>Verkflæði til að stofna markmið

Verkflæði til að stjórna stofnun starfsmannamarkmiða er eitt af nokkrum verkflæði sem voru tiltæk til að auðvelda skipulag fyrir ferlið við frammistöðustjórnun.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Frammistöðustjórnun hefur verið algerlega endurhönnuð í Finance and Operations.     |
| **Skipt út fyrir aðra eiginleika?**   | Endurhannaður Eiginleiki frammistöðustjórnunar gefur meiri stjórn yfir markmið, mælingar sem notaðar eru til að rekja framvindu, og að hengja við frekari gögn. Markmið má geyma sem sniðmát og síðan endurnotuð. Þessi eiginleiki getur hjálpað við að setja upp viðbótar markmið fyrir starfsmennina fljótlegri hátt. |
| **Afurðasvæði sem haft er áhrif á**         | Mannauðsstjórnun                 |
| **Staða**                         | Fjarlægt frá og með Dynamics 365 for Operations útgáfu 1611. |

## <a name="dynamics-ax-70"></a>Dynamics AX 7.0 


### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Möguleika á að hætta við breytingar á reikningi lánardrottins

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Bætt frammistaða.        |
| **Skipt út fyrir aðra eiginleika?**   | Númer                             |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir               |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0. |

### <a name="aif-axd-and-axbc-integrations"></a>AIF AxD og AxBC samþættingar

Í samþættingarramma Kerfa (AIF), er hægt að skiptast á gögnum við ytri kerfi gegnum viðskiptagrunninn með viðskiptagrunn sem er sem þjónustu. Dynamics AX felur í sér þjónustu sem byggir á skjölum og .NET Business Connector (AxBC). Skjal er stofnað með notkun XML. XML inniheldur hausupplýsingar sem bætt er við til að stofna *skilaboð* sem hægt er að flytja inn eða út úr Dynamics AX. Dæmi um skjöl fela í sér sölupantanir og innkaupapantanir. Hins vegar getur skjal staðið fyrir nánast hvaða einingu sem er, eins og viðskiptavin. Þjónustur sem byggja á skjölum nota **Axd \<Document\>** klasana.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Ekki tókst að laga uppbyggingu AIF og AxDs að skýjaþjónustu. Upp komu afkastavandamálí tengslum við fjöldainnflutning.                                        |
| **Skipt út fyrir aðra eiginleika?**   | Þessum eiginleika er skipt út fyrir ramma innflutning/útflutning gagna, sem styður endurtekinn magninnflutning/útflutning gagna. Mælt er með því að raunverulegar töflur sé notað AxBC. |
| **Afurðasvæði sem haft er áhrif á**         | AxD AxBC og AIF   |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.   |

### <a name="billing-code-rate-scripts"></a>Forskriftartaxtar innheimtukóða

Innheimtuforskriftir voru notaðar til að reikna út innheimtuverð fyrir innheimtukóða. Þessar forskriftir þurftu sérsniðna forritun í C Sharp eða Visual Basic forritunarmálinu. Í núverandi útgáfu af Dynamics AX er **forskriftarkóði innheimtukóða** ekki studdur.

| &nbsp;  |&nbsp;  |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Stuðningur við sérsniðna C Sharp eða forskriftir Visual Basic var ekki bætt við í Dynamics AX 7.0. |
| **Skipt út fyrir aðra eiginleika?**   | Nei                                                                                      |
| **Afurðasvæði sem haft er áhrif á**         | Hið opinbera, viðskiptakröfur                                    |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.                                                          |

### <a name="boms-without-bom-versions"></a>Uppskriftir án uppskriftaútgáfa

Þegar á skilgreiningarlykill **uppskriftaútgáfur** var gerður óvirkur voru uppskriftarútgáfur falin í öllum skjámyndum og kerfið þvingaði fram 1:1 vensl milli útgefnar afurðir og Uppskrifta. Skilgreiningarlykillinn **Uppskriftaútgáfur** má ekki vera óvirkur í þessari útgáfu af Dynamics AX.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Notkun skilgreiningarlykils til að stjórna uppskriftaútgáfur lagast ekki að skýjaumhverfi. |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                                                                      |
| **Afurðasvæði sem haft er áhrif á**         | Upplýsingar um afurðarstjórnun, Birgðastjórnun                                    |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.                                                          |

### <a name="brazilian-bordero"></a>Brazilian Bordero

Tiltekin greiðsluhátt fyrir Brasilískt fyrirtæki

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Stuðning fyrir greiðsluaðferð Brasilískt Bordero Hefur verið lagðar af úr Brasilískt staðfærslu |
| **Skipt út fyrir aðra eiginleika?**   | Númer   |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir   |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="brazilian-sintegra-statement"></a>Brasilískt Sintegra yfirlit

Alríkisskattframtal fyrir ICMS-skatt

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þetta yfirlit á ekki lengur við sum Brasilískt fylki. |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Notendur geta notað verkfærið Almennan Rafræna skýrslugerð til að skilgreina uppgjör ef nauðsynlegt við tilteknar aðstæður. |
| **Afurðasvæði sem haft er áhrif á**         | Skattabækur    |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.   |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Brasilísk SCAN viðbúnaðarstilling fyrir NF-e

(SCAN) aðstæður viðbúnaðar er notað til að mynda, flytja út og inn stöðu á Nota Fiscal eletrônica (NF-e) þegar aðstæður Secretaria da Fazenda (SEFAZ) er ekki tiltækt.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Viðbúnaðarháttur er á ekki lengur við í öllum brasilískum fylkjum |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                                                          |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur                                                         |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.              |

### <a name="business-analyzer"></a>Viðskiptagreining

Þessi fartækjaforrit leyfa notendum að yfirfara lykil viðskiptaviðmið.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Aðgerðinni hefur verið skipt út fyrir aðra eiginleika.   |
| **Skipt út fyrir aðra eiginleika?**   | Fylgjast með fjárhagslegri frammistöðu efnispakki fyrir Microsoft Power BI mun innihalda lykil viðskiptaviðmiða sem voru áður tiltæk í Viðskiptagreiningu. |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur      |
| **Staða**                         | Úrelt: Notkun Viðskiptagreiningar hefur verið gerð úrelt.    |

### <a name="business-statistics"></a>Viðskiptatalnagögn

Uppsetning fyrirspurnir um viðskiptatalnagögn sem geta auðveldað greiningu á afköstum í fyrirtækinu

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Eldri nálgun á viðskiptagreind (BI), Lítil notkun viðskiptavina og takmörkuðum eiginleikum. |
| **Skipt út fyrir aðra eiginleika?**   | Ný Lausnir fyrir BI fyrir þessa útgáfu af Dynamics AX                                      |
| **Afurðasvæði sem haft er áhrif á**         | Innkaup og uppruni, viðskiptaskuldir, sala og markaðssetning, viðskiptakröfur         |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.                                                               |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Breyta virkni dagsetningu skjals í færslubókarsamþykkt reiknings

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Lítil notkun                                                               |
| **Skipt út fyrir aðra eiginleika?**   | Já. Hægt er að breyta dagsetningu skjals á bókuðum lánardrottnafærslu. |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir                                                        |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.                                          |

### <a name="clieop03-payment-format-for-the-netherlands"></a>ClieOp03 greiðslusnið fyrir holland

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Snið gildir ekki lengur í Hollandi, þar sem því hefur verið skipt út fyrir SEPA-virkni. |
| **Skipt út fyrir aðra eiginleika?**   | SEPA greiðsluútflutningur  |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar     |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.   |

### <a name="compliance-center"></a>Samræmismiðstöð

Samræmismiðstöðinni var Enterprise Portal-setur til að hafa umsjón með kröfum um fylgiskjöl fyrir vegna samræmis við framtaksverkefni í tengslum við Sarbanes Oxley lög.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Of lítil notkun viðskiptavina. Microsoft SharePoint inniheldur sömu getu sem voru tiltæk í Samræmismiðstöð. |
| **Skipt út fyrir aðra eiginleika?**   | Númer   |
| **Afurðasvæði sem haft er áhrif á**         | Samræmi og innra eftirlit  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.    |

### <a name="connector-for-microsoft-dynamics"></a>Tengill fyrir Microsoft Dynamics

Þetta verkfæri var notað til að samþætta lykilgögn úr Microsoft Dynamics CRM í Dynamics ERP forritin.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Aðgerðinni hefur verið skipt út fyrir aðra eiginleika. |
| **Skipt út fyrir aðra eiginleika?**   | Common data service                                      |
| **Afurðasvæði sem haft er áhrif á**         | Tengill fyrir Dynamics                         |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.                           |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Geymslueining og fjölvídd á lager

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Afrituð virkni |
| **Skipt út fyrir aðra eiginleika?**   | Já. Síðan AX 2012 hefur þessi virkni verið skipt út fyrir eiginleikasetti sameinuðum runupöntunum. Þetta eiginleikasett er með samantekið yfirlit á lager. |
| **Afurðasvæði sem haft er áhrif á**         | Stjórnun á upplýsingum um afurðir, framleiðslustýring, Birgðastjórnun, Sölu og markaðssetning  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0. |

### <a name="cue-group-metadata"></a>Bunkaflokkar Lýsigagna

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Bunkaflokkar voru notaðar til að birta eina eða fleiri bunka í svæði Upplýsingakassa . Takmörkuð geta til að meðtaka hlutina einnig komu upp vandamál hvað varðar afköst, vegna þess að breyting á skrá í yfirskjámyndar orsökuðu að ein fyrirspurnin varð til fyrir bunka í bunkaflokknum. |
| **Skipt út fyrir aðra eiginleika?**   | Númer      |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar    |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.  |

### <a name="cue-metadata"></a>Bunka Lýsigögn

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Bunka lýsigögn hafa verið takmarkað til að telja eða taka saman upplýsingar.    |
| **Skipt út fyrir aðra eiginleika?**   | Reitar Lýsigögn var kynnt til sögunnar til að veita sveigjanlegri fyrir líkön. Til dæmis, er hægt að breyta gildandi talningar, flettingum og afkastavísar (KPI). Reitar Lýsigögn Talningar er bein útskipting bunka lýsigagna. |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar           |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0      |

### <a name="danish-check-format"></a>Danskt ávísunarsnið

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Stuðningur við danskt snið ávísana hefur verið lagður af og skýrslan hefur verið fjarlægð úr DK staðfærslu. |
| **Skipt út fyrir aðra eiginleika?**   | Númer    |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar    |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.  |

### <a name="data-partitions"></a>Deildaskiptingar gagna

Deildaskiptingar gagna veita rökréttan aðskilnað gagna í Dynamics AX gagnagrunninum.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Gögn deildaskiptingar voru kynnt í Dynamics AX 2012 R2 til að virkja einangrun gagna. Í almennum aðstæðum, er Fyrirtæki með dótturfyrirtæki og gögn úr eitt dótturfyrirtæki ætti ekki að vera sýnileg fyrir aðra dótturfyrirtæki, jafnvel þótt bæði dótturfyrirtækjum er stjórnað af sömu tæknideild. Hins vegar var þörf á aukalegar forskriftir og sameiginlegur kostnaður í forritinu til að stofna nýja deildaskiptingar og færa inn í þær gög, og afrita deildaskiptingar gagna. Í skýið, þar sem við höfum aðgang að verkvangur sem þjónusta (PaaS) gagnagrunnsþjónustu (Microsoft Azure SQL Gagnagrunnur), er mikið áhrifaríkara að nota í gagnagrunninn sem einangrunargeymi en að framkvæma einangrunina í forritinu. Óháð því hvort deildaskipting gagna er krafist fyrir dótturfyrirtæki, fyrir marga leigjendur, eða einfaldlega fyrir kvörðun, trúum við því að aðstæður megi meðhöndla betur með mörgum tilvikum af Finance and Operations. |
| **Skipt út fyrir aðra eiginleika?**   | Viðskiptavinir sem nota deildaskiptingu gagna verða að nota mörg tilvik af Finance and Operations ef aðskilnaður gagnasafnsstiga er mikilvægt mál.    |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.  |


### <a name="database-and-file-share-storage-for-attachments"></a>Gagnagrunnur og geymsla fyrir samnýttar skár fyrir viðhengi

Dynamics AX 2012 leyfði geymslu á viðhengjum í gagnagrunninum og í skráasamnýtingu. Báðir valkostirnir eru ekki lengur studdir.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Geymsla samnýttra skráa er ekki lengur studd því umhverfi í skýi geta ekki átt samskipti við staðbundnar samnýttar skrár. Gagnagrunnsgeymsla hefur verið gerð úrelt og í staðinn er komin Azure Blob geymsla. Azure Blob-geymsla jafngildir geymslu í gagnagrunninum, úr því að aðeins er hægt að nálgast skjöl í gegnum Finance and Operations eyðublöð viðskiptavinar. Þessu fylgir sá viðbótarkostur að bjóða upp á geymslu sem hefur ekki neikvæð áhrif á afköst gagnagrunnsins. Blob geymsla er sjálfgefið geymslukerfi fyrir Skjalastjórnum og virkar tafarlaust. |
| **Skipt út fyrir aðra eiginleika?**   | Gagnagrunnsgeymsla hefur verið gerð úrelt og í staðinn er komin Azure Blob geymsla.   |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.   |

### <a name="delimitation"></a>Afmörkun

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Engin Notkun á þessari virkni fannst. |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                     |
| **Afurðasvæði sem haft er áhrif á**         | Tími og viðvera                    |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.         |

### <a name="desktop-client"></a>Fjartengingarforrit

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Dynamics AX biðlarinn hefur verið endurhannaður til að auka notkunargetu yfir marga verkvanga og tæki.                      |
| **Skipt út fyrir aðra eiginleika?**   | Nýr vefbiðlari er byggð á lýsigögnum skjáborðsmyndar og forritunarlíkans sem hefur verið breytt til að veita ríkulegan vefvettvang. |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.   |

### <a name="direct-database-connection"></a>Bein gagnagrunnstenging

Í Dynamics AX 2012 R3, getur Retail Modern POS tengst beint í Channel DB á svipaðan hátt og við Enterprise POS. Það var auk staðlaðar samskiptaaðferðar Retail Modern POS sem átti samskipti í gegnum Retail-þjón.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Bein gagnagrunns tengingarnar krefst minna öryggis samskiptareglu og var fyrst og fremst notuð til að ná hæsta stig afköst. Vegna frammistöðu og öryggi endurbætur sem hafa orðið í Finance and Operations, býr aðgerðin nú til fleiri vandamál en lausnir. |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Aðeins stöðluðum Retail-þjónn samskipti eru studd núna.  |
| **Afurðasvæði sem haft er áhrif á**         | Gagnagrunnur rásarRetail Modern POS   |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.  |

### <a name="dutch-swift-mt940"></a>Hollenska SWIFT MT940

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Almenn virkni er nú notaðar í stað staðfært virkni.                    |
| **Skipt út fyrir aðra eiginleika?**   | Já, þessum eiginleika hefur verið skipt út af ítarlega virkni fyrir bankaafstemmingu. |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar                                                                              |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                           |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL fyrir Þýskaland)

Þessi virkni veitti úttak fyrir eXtensible Business Reporting Language (XBRL) sem er sérstaklega ætlað fyrir Þýska eBilanz-flokkunina.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Of lítil notkun viðskiptavina.  |
| **Skipt út fyrir aðra eiginleika?**   | Þessum eiginleika hefur ekki verið skipt út fyrir annan eiginleika, en marga sérhæfða XBRL-pakka sem veita ríkulega xbrl-virkni eru tiltækar fyrir Þýsk markaði. |
| **Afurðasvæði sem haft er áhrif á**         | Management Reporter      |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.  |

### <a name="enterprise-portal-client"></a>Enterprise Portal biðlari

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Eins biðlaravettvangur hefur verið stofnað.  |
| **Skipt út fyrir aðra eiginleika?**   | Nýr vefbiðlari er byggð á lýsigögnum skjáborðsmyndar og forritunarlíkans sem hefur verið breytt til að veita ríkulegan vefvettvang. |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.   |

### <a name="environmental-sustainability"></a>Sjálfbær þróun

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Lítil notkun viðskiptavina og takmörkuðum eiginleikum.  |
| **Skipt út fyrir aðra eiginleika?**   | Númer              |
| **Afurðasvæði sem haft er áhrif á**         | Samræmi og innra eftirlit, viðskiptaskuldir  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0. |

### <a name="form-activex-and-managed-host-controls"></a>Skjámynd ActiveX og stjórntæki hýsils með umsjón

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skjámynd ActiveX og stjórntæki hýsils með umsjón byggjast á afskrifaða fjartengiforritinu. |
| **Skipt út fyrir aðra eiginleika?**   | Umfangsmikill Rammi fjárhagsáætlunarstýringar styður uppbyggingu nýja stýringar sem er byggt á HTML, CSS og JavaScript og er fyrsta flokks stýring í Microsoft Visual Studio Tooling umhverfinu. |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar     |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.       |

### <a name="generate-prenotes-by-using-a-batch"></a>Mynda fyrirframkvittanir með runu

Myndun fyrirframkvittunar er ekki hægt að gera með því að nota runu en samt er hægt að gera af notanda.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Engin skjámynd er til staðar til að staðfesta og birta fyrirframkvittunarskrá sem verður til þegar hún er mynduð með því að nota runuvinnslu. |
| **Skipt út fyrir aðra eiginleika?**   | Enn er hægt að mynda fyrirframkvittanir og notandi hefur stjórn á staðsetningunni þar sem skráin er vistuð.   |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir, viðskiptakröfur, reiðufjár- og bankastjórnunar  |
| **Staða**                         | Fjarlægð frá og með AX 7.0.    |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Þýska DTAUS útflutningur og greiðslu og innflutningur lyklayfirlits (samtölur og færslur)

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Snið gildir ekki lengur í Þýskalandi, þar sem því hefur verið skipt út fyrir virkni sameiginlegs evrópsks greiðslusvæðis (SEPA).                    |
| **Skipt út fyrir aðra eiginleika?**   | Já, þessum eiginleika hefur verið skipt út af greiðsluútflutningur SEPA og ítarlega virkni fyrir bankaafstemming fyrir innflutning reikningsyfirlita. |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar  |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="german-dtazv-payment-format-in-domestic-currency"></a>Þýska DTAZV-greiðslusniðið í innlendum gjaldmiðli

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Snið gildir ekki lengur í þýskalandi, þar sem því hefur verið skipt út fyrir SEPA-virkni. |
| **Skipt út fyrir aðra eiginleika?**   | SEPA greiðsluútflutningur    |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir   |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.    |

### <a name="german-mt940-import"></a>Flytja inn Þýska MT940

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Almenn virkni er nú notaðar í stað staðfært virkni.                    |
| **Skipt út fyrir aðra eiginleika?**   | Já, þessum eiginleika hefur verið skipt út af ítarlega virkni fyrir bankaafstemmingu. |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar                                                                              |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.                           |

### <a name="german-xml-eu-sales-list"></a>Þýskur XML ESB-sölulisti

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Xml-snið fyrir þýska skýrslugerð esb-Sölulista er ekki studd lengur. Hægt er að nota aðeins ELMA5 Snið textaskrár til að senda skýrslu esb-Sölulista til þýska skattstjórans. |
| **Skipt út fyrir aðra eiginleika?**   | Númer         |
| **Afurðasvæði sem haft er áhrif á**         | Skattur        |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.   |

### <a name="gl-ssrs-reports"></a>GL SSRS-skýrslur

Skýrslur sem innihalda eftirfarandi valmyndaratriði hafa verið fjarlægð: **Samantekt á prófjöfnuði**, **Ítarlegur prófjöfnuður**, **Bókhaldslykil**, **Endurskoðunarslóð**, **Stöður**, og **stöðulisti**.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Skýrslur fyrir Financial Microsoft SQL Server Reporting Services (SSRS) hefur verið skipt út fyrir eiginleika Management Reporter og sjálfgefnar skýrslur. |
| **Skipt út fyrir aðra eiginleika?**   | Management Reporter (merktur **Fjárhagsskýrslugerð** í núverandi útgáfu af Dynamics AX)    |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur   |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.   |

### <a name="infopart-and-formpart-metadata"></a>InfoPart og FormPart lýsigögn

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | InfoPart og FormPart lýsigögn virkja stofnun upplýsingareita fyrir tvo mismunandi biðlara. |
| **Skipt út fyrir aðra eiginleika?**   | InfoPart lýsigögn sem var einfaldaður skilgreining skjámyndar, er breytt í Skjámynd með uppfærsluverkfærum. FormPart lýsigögn sem vísaí Skjámynd, er skipt út fyrir beinni tilvísun sem er stofnað af uppfærsluverkfærum. |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar    |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.        |

### <a name="main-account-list-page"></a>Listasíða Aðallykils

Listi yfir lykla fyrir lögaðilann og tengdar stöðuupplýsingar

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Upplýsingar um Stöðu er tiltæk á í **prófjöfnuð** listasíðu eftir lykils og víddar.  |
| **Skipt út fyrir aðra eiginleika?**   | **Aðallyklar** inniheldur sömu lista með lyklum sem listasíðu **aðallykils** innihélt . Sýn hnitanets í **aðallykla** sýnir einnig enn minni, yfirlit í hnitaneti . |
| **Afurðasvæði sem haft er áhrif á**         | Fjárhagur      |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.    |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Malasíu og Singapúr sjóðstreymiskýrsla banka

Þessi eiginleiki gefur notanda kost á að Prenta sjóðstreymisskýrslu sem sýnir færslur og upplýsingar sjóðinnstreymis og útstreymis fyrir tilteknar dagsetningar á völdum bankareikningum.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Hægt er að fá sömu upplýsingar úr fyrirspurn Um bankafærslu. |
| **Skipt út fyrir aðra eiginleika?**   | Fyrirspurn Um bankafærslu.                                            |
| **Afurðasvæði sem haft er áhrif á**         | Reiðufjár- og bankastjórnun                                                |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika.          |

### <a name="mexican-cfd-electronic-invoice"></a>Mexíkóskur CFD rafrænn reikningur

Þessi eiginleiki virkjaði myndun Mexíkósk rafræna reikninga með því að nota aðferðina Comprobante Fiscal Digital (CFD), þar sem fyrirtækið skrifar undir reikninginn með því að biðja um viðkomandi heimild frá yfirvalda. Þessi eiginleiki veitir einnig mánaðarleg skýrsla sem inniheldur alla rafræna reikninga sem voru gefnir út á tímabilinu.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Aðferð er ekki lengur gild. Myndun rafrænna reikninga með því að nota aðferðina CFD var afskrifuð af skattyfirvöldum og skipt út fyrir Comprobante Fiscal Digital a través de Internet (CFDI) -aðferð, þar sem undirritun er framvísað til þriðja aðila þjónustuaðila (PAC). Mánaðarleg skýrsla hefur verið fjarlægt og fyrirspurnarvalkostur gerir notendum kleift að spyrjast fyrir um sögulegar færslur. |
| **Skipt út fyrir aðra eiginleika?**   | Númer    |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptakröfur, verk   |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="mexico-realized-and-unrealized-vat"></a>Mexíkó innleyst og óinnleystur VSK

Dynamics AX 2012 vann úr óinnleysta virðisaukaskattinum (VSK) með því að nota aðgerðir sem eru sérstaklega notaðar fyrir Mexíkó fyrir óinnleystan skatt.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Afrituð virkni  |
| **Skipt út fyrir aðra eiginleika?**   | Já, þessari virkni hefur verið skipt út fyrir virkni staðlaðs skilyrts söluskatts sem Core veitir. |
| **Afurðasvæði sem haft er áhrif á**         | Skattur   |
| **Staða**                         | Úrelt: Fjarlægingardagsetning hefur ekki verið stilltur fyrir þennan eiginleika. |

### <a name="microsoft-outlook-integration"></a>Samþætting Microsoft Outlook


| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Aðgerðinni hefur verið skipt út fyrir Microsoft Exchange Server samþættingu. |
| **Skipt út fyrir aðra eiginleika?**   | Já                                                                            |
| **Afurðasvæði sem haft er áhrif á**         | Sala og markaðsstarf                                                            |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.                                                 |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Einka lokun á færslubókum birgða- og vöruhúsastjórnunar

Færslubók birgða og vöruhúss hafa ekki lengur möguleikann á að merkja færslubók sem einka fyrir valinn notanda. Aðeins ferlið við lokun færslubóka sem einka fyrir notendaflokka og lokunar við breytingar er studd.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Engin Notkun á þessari virkni fannst. |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                     |
| **Afurðasvæði sem haft er áhrif á**         | Birgðir                   |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.         |

### <a name="product-builder"></a>Vörusamsetning

Vörusamsetning (Product builder) var notaður til að setja saman á lifandi hátt vörur úr sölupöntun, innkaupapöntun, framleiðslupöntun, sölutilboð, verktilboð eða vöruþörf. Samkvæmt vörulíkani sem var með líkanabreytum gat notandinn velja gildi til að uppfylla kröfur viðskiptavinar og sækja einkvæmt afurðarafbrigði sem höfðu Uppskrift og leið.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Product builder birti X ++ kóða til að endanotenda og er ekki studdur í þessari útgáfu af Dynamics AX. Það hefur verið fjarlægð til að koma í veg fyrir tvíteknar viðhaldsvinnu á kóðagrunnum sem skarast.  |
| **Skipt út fyrir aðra eiginleika?**   | Já. Skorðuskilgreiningin var kynnt í Dynamics AX 2012 þar sem úrelding Vörusamsetningar í framtíðarútgáfum var þegar tilkynnt. Skorðuskilgreiningartæknin valin á vörustjórunum til að virkja grunnstillingarnar. Frekari upplýsingar, sjá [Yfirlit afurðarafbrigða](../../../supply-chain/pim/build-product-configuration-model.md). |
| **Afurðasvæði sem haft er áhrif á**         | Stjórnun á upplýsingum um afurðir, Sölu og markaðssetningu  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.      |

### <a name="production-floor-app"></a>Forrit framleiðslugólfs
Þetta er forritið fyrir spjaldtölvur sem keyra Windows 8.1 RT og Windows 8.1 Pro.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Með breytingunni á biðlara á netinu er hægt að skila svipaðri virkni í gegnum biðlara Dynamics AX 7.0 á staðnum. Verkspjaldstækið býður upp á notandaviðmót fyrir framleiðslugólf sem er fínstillt inn á snertieiginleika og skjámynd spjaldtölvu. |
| **Skipt út fyrir aðra eiginleika?**   | Já. Verkspjaldstækið, sem er staðbundinn hluti Dynamics AX 7.0.                                                                           |
| **Afurðasvæði sem haft er áhrif á**         | Framleiðslustýring                                                |
| **Staða**                         | Úrelt: Fjarlægingardagsetning frá verslun Microsoft hefur enn ekki verið stillt fyrir þennan eiginleika.                                                |


### <a name="rename-product-dimension"></a>Endurnefna afurðarvídd

Þessi eiginleiki leyfði þér að breyta heiti á einn af þremur staðlaða afurðarvíddum (stærð, lit eða stíl) í nafn sem hentaði betur þínu fyrirtæki. Endurnefning innifalið allar merki þar sem nöfn afurðarvídda voru notuð.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Þessi útgáfu af Dynamics AX styður ekki merkingabreytingar á keyrslutíma. |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                                                            |
| **Afurðasvæði sem haft er áhrif á**         | Vöruupplýsingastjórnun                                                |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.                                                |

### <a name="retail-server-connectivity-using-http"></a>Tengigeta Retail-þjóns athuguð

Í Dynamics AX 2012 R3, gæti Retail-þjónn virkað með HTTP samskiptaaðferðar (ekki-öryggisvörðum). Þetta var til viðbótar við stöðluð samskipti með HTTPS.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Vegna nýrra öryggisþarfa, aðeins öryggisvörðum samskipti með TLS 1,2 (eða ofan, sé það til staðar) er nú studd. Sjálfsafgreiðslu uppsetningarforritið mun sjálfkrafa skilgreina tölvunni þessu samskiptaaðferðar. |
| **Skipt út fyrir aðra eiginleika?**   | Nei. Aðeins stöðluðum HTTPS samskipti eru studd núna. |
| **Afurðasvæði sem haft er áhrif á**         | Retail-þjónn  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0. |

### <a name="role-center-pages"></a>Hlutverkamiðstöðvarsíður

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Síður hlutverkamiðstöðvar voru byggðar á afskrifuðum Enterprise Portal verkvangi, sem hefur verið skipt út fyrir nýtt vefbiðlaravettvang í þessari útgáfu af Dynamics AX. |
| **Skipt út fyrir aðra eiginleika?**   | Nýtt skjámyndarmynstur Vinnusvæðis veitir notendum hönnun sem er vinnslumiðuð og veitir auðveldan aðgang að almennum verkum innan þessu ferli.                       |
| **Afurðasvæði sem haft er áhrif á**         | Allar einingar    |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0   |

### <a name="sales-tax-jurisdictions"></a>Skattaumdæmi

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Lítil notkun viðskiptavina og takmörkuðum eiginleikum. |
| **Skipt út fyrir aðra eiginleika?**   | Númer                                           |
| **Afurðasvæði sem haft er áhrif á**         | Bandarískur virðisaukaskattur                                 |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.               |

### <a name="sites-services"></a>Svæðaþjónusta

Sites Services gerir þér kleift að búa til vefsíður sem framlengja viðskiptaferlum þínum til internetsins án stuðnings við upplýsingatækni.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Grunngerð Microsoft Azure sem notað er í Dynamics AX hefur nýja getu sem hægt er að nota í staðinn (til dæmis Azure setur). |
| **Skipt út fyrir aðra eiginleika?**   | Númer   |
| **Afurðasvæði sem haft er áhrif á**         | Ráðningaferli tengd mannauði, Málastjórnun, Tilboðsbeiðnir, Skráning lánardrottins, Sameiginleg vinnusvæði fyrir tækifæri og herferðir  |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.    |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS stefna eftirspurnarspár

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Hönnun á eiginleikanum getur ekki verið studd í nýrri skýjahögun. |
| **Skipt út fyrir aðra eiginleika?**   | Azure Machine Learning stefna eftirspurnarspár                           |
| **Afurðasvæði sem haft er áhrif á**         | Áætlanagerð                                                              |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.                                               |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Reikningahópur lánardrottins án bókunarupplýsinga

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Lítil notkun. Aðgerðinni hefur verið skipt út af reikningabók sem hefur virknina verkflæði. |
| **Skipt út fyrir aðra eiginleika?**   | Verkflæðigeta reikningsbókar.     |
| **Afurðasvæði sem haft er áhrif á**         | Viðskiptaskuldir |
| **Staða**                         | Fjarlægt frá og með Dynamics AX 7.0.    |


### <a name="virtual-company-accounts"></a>Sýndarreikningsskil

Sýndarfyrirtækjaeiginleiki er ekki lengur studd í Dynamics AX. Eiginleikinn sýndarfyrirtæki gerði notendum mögulegt að setja upp töflur sem mátti deila með hóp fyrirtækja. Fyrir lýsingu á aðgerðinni sjá [reikningsskil og sýndarreikningsskil](https://msdn.microsoft.com/library/aa834382(v=ax.10).aspx). Eiginleikinn vinnur með því að flokka töflur í söfn sem tilheyra sýndarfyrirtæki, sem eru hópar af fyrirliggjandi "raunverulegum" fyrirtæki. Fyrirspurnir eru stofnaðar svo að öll fyrirtæki í sýndarfyrirtækinu hafi aðgang að gögnum í töflum tengdra töflusafna.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | - Sýndarfyrirtæki verður að vera uppsett áður en gögn eru geymd í töflum. Að bæta sýndarfyrirtæki eftirá við yfir fyrirliggjandi framkvæmd er mjög erfitt.<br><br>- Þar sem hefur verið svo mikið um stöðlun gagna í gildandi útgáfu af Dynamics AX, er orðið mjög erfitt að vita hvað skuli bæta við töflusöfn. Til dæmis er erfitt að vita hvaða töflum eigi að deila. Allar töflur sem vísað er til úr töflum sem eru í sýndarfyrirtæki verður að bæta við. Vegna Stöðlun Tafla verða jafnvel einfalt aðalgögn sem er dreift yfir margar töflur að vera hluti af sýndarfyrirtækinu. Öll mistök sem gerð eru hér munu valda virknivandamálum.<br><br>- Þegar tafla er hluti af sýndarfyrirtæki, tapar það upplýsingar um uppruna gagnanna, og aðeins sýndarfyrirtæki er skráð.   |
| **Skipt út fyrir aðra eiginleika?** | Altækar töflur er hægt að nota til að gera töflur aðgengilegar frá öllum fyrirtækjum. Það er engin útskipting sem stendur. |   
| **Afurðasvæði sem haft er áhrif á**       | Allar einingar |   
| **Staða**                       | Fjarlægt frá og með Dynamics AX 7.0.   |   

### <a name="windows-8-tablet-app"></a>Windows 8 spjaldtölvuforrit

Windows 8 spjaldtölvuforrit veittu aðgerðir fyrir kostnaðarfærslu og -samþykkt.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Finance and Operations er samhæft við töflur. Spjaldtölvuforrita er ekki lengur þörf.    |
| **Skipt út fyrir aðra eiginleika?**   | Nei.          |
| **Afurðasvæði sem haft er áhrif á**         | Útgjaldastýring   |
| **Staða**                         | Fjarlægt: Þessi virkni er aðeins tiltækur fyrir Dynamics AX 2012 R3. |

### <a name="workplanner"></a>Vinnuáætlun

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Ástæða úreldingar/fjarlægingar** | Lítil notkun |
| **Skipt út fyrir aðra eiginleika?**   | Nei, en **Forstillingarvensl** síðu sem er opnuð á **forstillingarflokks** síðu, styður sömu viðskiptaaðstæður og í hinu úrelta **vinnuáætlun** síðu. |
| **Afurðasvæði sem haft er áhrif á**         | Tími og mæting     |
| **Staða**                         | Kóðinn hefur ekki verið fjarlægður. Hins vegar var formið JmgWorkPlanner ekki flutt.    |

### <a name="x-financial-statements"></a>X++ fjárhagsskýrslur

| &nbsp;  | &nbsp; |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <strong>Ástæða úreldingar/fjarlægingar</strong> |                         Aðgerðinni hefur verið skipt út fyrir aðra eiginleika.                         |
|  <strong>Skipt út fyrir aðra eiginleika?</strong>  | Management Reporter (merktur <strong>Fjárhagsskýrslugerð</strong> í núverandi útgáfu af Dynamics AX) |
|     <strong>Afurðasvæði sem haft er áhrif á</strong>     |                                              Fjárhagur                                              |
|             <strong>Staða</strong>             |                                      Fjarlægt frá og með Dynamics AX 2012                                      |

