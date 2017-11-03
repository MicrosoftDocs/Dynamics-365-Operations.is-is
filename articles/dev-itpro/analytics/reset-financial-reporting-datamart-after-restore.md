---
title: "Endurstilla fjárhagslegar skýrslugerð gagnatorgs eftir endurheimt gagnagrunns"
description: "Þetta efnisatriði lýsir hvernig á að endurstilla gagnaskemmu fyrir fjárhagsskýrslugerð eftir endurheimt Microsoft Dynamics 365 Finance and Operations gagnagrunns."
author: ShylaThompson
manager: AnnBe
ms.date: 08/15/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261824
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 200b1a03a0ea95ec2d75850f9a8aebda966e38d6
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Endurstilla fjárhagslegar skýrslugerð gagnatorgs eftir endurheimt gagnagrunns

[!include[banner](../includes/banner.md)]


Þetta efnisatriði lýsir hvernig á að endurstilla gagnaskemmu fyrir fjárhagsskýrslugerð eftir endurheimt Microsoft Dynamics 365 Finance and Operations gagnagrunns.

Ef þú endurheimtir Finance and Operations gagnagrunninn úr öryggisafritum eða afritar gagnagrunninn úr öðru umhverfi, er nauðsynlegt að fylgja skrefunum í þessu efnisatriði til að tryggja að gagnaskemma fjárhagsskýrslugerðarinnar sé að nota endurheimtan gagnagrunn Finance and Operations á réttan hátt. 
> [!Note] 
> Skrefin í þessu ferli eru studd fyrir Dynamics 365 for Operation útgáfu í maí 2016 (Forritsútgáfa 7.0.1265.23014 og fjárhagsleg skýrslugerð útgáfa 7.0.10000.4) og nýrri útgáfur. Ef þú er með eldri útgáfu af Finance and Operations skaltu hafa samband við þjónustuver okkar til að fá aðstoð.

## <a name="export-report-definitions"></a>Flytja út skilgreiningu á skýrslum
Fyrst skal flytja út skýrsluhönnun sem er staðsett í Skýrsluhönnuðinum með eftirfarandi skrefum:

1.  Í Skýrsluhönnun ferðu í **Fyrirtæki** &gt; **Einingahópar**.
2.  Veldu einingahópinn sem á að flytja út og síðan er smellt á **Flytja út**. 

    > [!Note] 
    > Í Finance and Operations er aðeins einn einingahópur studdur, **Sjálfgefið**.
    
3.  Veldu skýrsluskilgreiningar til að flytja út:
    -   Til að flytja út allar skýrsluskilgreiningar og tengdar einingar er smellt á **Velja allt**.
    -   Til að flytja út tilteknar skýrslur, línur, dálka, skipurit eða víddasamstæður er smellt á viðeigandi flipa og svo valin atriði til að flytja út. Haldið inni Ctrl-lyklinum til að velja mörg atriði á flipa. Þegar valdar eru skýrslur til að flytja út eru einnig valdar tengdar línur, dálkar, skipurit og víddasamstæður.

4.  Smellt er á **Útflutning**.
5.  Færið inn skráarnafn og veljið öruggum stað þar sem á að vista útfluttar skýrsluskilgreiningar.
6.  Smellið á **Vista**.

Skrána má afrita eða hlaða upp á öruggan stað, þar sem flytja á hana inn í annað umhverfi seinna. Hægt er að finna upplýsingar um notkun í geymslulykils Microsoft Azure í [Flytja gögn með AzCopy Command-Line Utility](/azure/storage/storage-use-azcopy). 
> [!NOTE]
> Microsoft veitir ekki geymslulykil sem hluta af samningi þínum um Finance and Operations. Annaðhvort verður að kaupa geymslulykil eða nota geymslulykil úr aðskilinni Azure-áskrift. 
> [!WARNING]
> Huga að hegðun á D-drifi á sýndarvélum Azure. Ekki geyma útflutta einingahópa hér varanlega. Sjá frekari upplýsingar um tímabundin drif á [Skilningur á tímabundnum drifum í sýndarvélum Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Stöðvunarþjónusta
Remote Desktop er notuð til að tengjast öllum tölvum í umhverfinu og stöðva eftirfarandi Windows þjónustu með því að nota services.msc:

-   Birtingarþjónusta á vefnum (á allar AOS tölvur)
-   Runustjórnunarþjónusta Finance and Operations (aðeins í AOS-tölvum sem ekki eru einkatölvur)
-   Ferlaþjónusta Management Reporter 2012 (aðeins á BI tölvum)

Þessar þjónustur hafa opna tengingar við gagnagrunn Finance and Operations.

## <a name="reset"></a>Endurstilla
### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a>Finna og hlaða niður síðasta MinorVersionDataUpgrade.zip pakkanum

Finna síðasta pakka MinorVersionDataUpgrade.zip með stefnum sem fundust í [Hlaða niður síðasta virkjanlega gagnauppfærslupakkanum](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-packages). Stefnurnar útskýra hvernig á að finna og hlaða niður rétta útgáfu af gagnauppfærslupakka. Uppfærslu er ekki krafist til að hlaða niður MinorVersionDataUpgrade.zip pakkanum. Þú þarft einungis að ljúka skrefunum í „Hlaða niður síðasta virkjanlega gagnauppfærslupakkanum“ hlutanum án þess að framkvæma neitt af hinum skrefunum í greininni til að sækja afrit af MinorVersionDataUpgrade.zip pakkanum.

### <a name="execute-scripts-against-finance-and-operations-database"></a>Keyra forskriftir á gagnagrunn Finance and Operations

Keyra eftirfarandi forskriftir á gagnagrunn Finance and Operations (ekki á gagnagrunn fjárhagsskýrslna).

-   DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql

Þessar forskriftir tryggja að notendur, hlutverk og stillingar á breytingarakningu séu réttar.

### <a name="execute-powershell-command-to-reset-database"></a>Keyra PowerShell-skipun til að endurstilla gagnagrunn

Á AOS-tölvunni skal keyra eftirfarandi skipanir í PowerShell sem stjórnandi til að núllstilla samþættingu milli Finance and Operations og fjárhagsskýrslugerðar:

```
F:
cd F:\MRApplicationService\MRInstallDirectory
Import-Module .\Server\MRDeploy\MRDeploy.psd1
Reset-DatamartIntegration -Reason OTHER -ReasonDetail “<my reason for resetting>”

```
> [!NOTE]
> Eftir keyrslu skipananna verður beðið um að fært sé inn "Y" til að staðfesta.

Útskýring á færibreytum:

-   Gild gildi fyrir - Ástæða eru: SERVICING, BADDATA, OTHER.
-   ReasonDetail færibreytan er fyrir valkvæman texta.
-   Ástæða og reasonDetail verða skráð í eftirlita fjarmælingu/umhverfis.

## <a name="start-services"></a>Ræsiþjónusta
Nota services.msc að endurræsa þjónustuna sem þú hættir áður:

-   Birtingarþjónusta á vefnum (á allar AOS tölvur)
-   Runustjórnunarþjónusta Finance and Operations (aðeins í AOS-tölvum sem ekki eru einkatölvur)
-   Ferlaþjónusta Management Reporter 2012 (aðeins á BI tölvum)

## <a name="import-report-definitions"></a>Flytja inn skýrsluskilgreiningu
Flytja inn skýrsluhönnun notanda úr Skýrsluhönnuðinum með skránni sem var búin til við útflutninginn:

1.  Í Skýrsluhönnun ferðu í **Fyrirtæki** &gt; **Einingahópar**.
2.  Veldu einingahópinn sem á að flytja út og síðan er smellt á **Flytja út**. 

    > [!NOTE]
    > Í Finance and Operations er aðeins einn einingahópur studdur, **Sjálfgefið**.
    
3.  Veldu eininguna **Vanskil** og smelltu á **Innflutning**.
4.  Veldu skrána með útfluttum skýrsluskilgreiningum og smelltu á **Opna**.
5.  Smellið á skýrsluskilgreiningarnar í svarglugganum Flytja inn til að flytja inn:
    -   Til að flytja inn allar skýrsluskilgreiningar og tengdar einingar er smellt á **Velja allt**.
    -   Til að flytja inn tilteknar skýrslur, línur, dálka, skipurit eða víddasamstæður skal velja skýrslur, línur, dálka, skipurit eða víddasamstæður sem á að flytja inn.

6.  Smelltu á **Flytja inn**.





