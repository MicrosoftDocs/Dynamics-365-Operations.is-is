---
title: "Endurstilla fjárhagslegar skýrslugerð gögn mart eftir endurheimt gagnagrunn"
description: "Þetta efnisatriði lýsir hvernig á að endurstilla fjárhagslegar skýrslugerð gögn mart eftir endurheimt Microsoft Dynamics 365 fyrir Aðgerðir í gagnagrunni."
author: twheeloc
manager: AnnBe
ms.date: 2016-12-08 16 - 20 - 13
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 3967cbb869fbb23d5d7716f619e4c22b4a273921
ms.lasthandoff: 03/29/2017


---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a>Endurstilla fjárhagslegar skýrslugerð gögn mart eftir endurheimt gagnagrunn

Þetta efnisatriði lýsir hvernig á að endurstilla fjárhagslegar skýrslugerð gögn mart eftir endurheimt Microsoft Dynamics 365 fyrir Aðgerðir í gagnagrunni. 

Það eru nokkrar kringumstæður þar sem þú gætir þurft að endurheimta skal Dynamics 365 fyrir gagnagrunn Aðgerðir úr öryggisafrit eða afrita annað umhverfi gagnagrunninum. Þegar þetta gerist einnig verður að fylgja eftirfarandi skrefum við að tryggja að fjárhagslegar skýrslugerð gögn mart er rétt með endurheimti Dynamics 365 Aðgerðir gagnagrunns. Ef þú hefur spurningar um endurstillingu fjárhagslegar skýrslugerð gögn mart ástæðu utan endurheimt Dynamics 365 Aðgerðir gagnagrunn, vísa í [Endurstillingu mart data Management Reporter](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) frekari upplýsingar. Athugið skrefin í þessu ferli eru studd fyrir Dynamics 365 aðgerð Maí 2016 losun (Forrits byggingu 7.0.1265.23014 og fjárhagsleg skýrslugerð byggingu 7.0.10000.4) og nýrri útgáfum. Ef eldri útgáfu af Dynamics 365 aðgerða, hafa skal samband við þjónustuver okkar til að fá aðstoð.

## <a name="export-report-definitions"></a>Flytja út skýrslu skilgreiningar
Fyrst að flytja út skýrsluhannana sem er staðsett í Skýrsluhönnuðinum með eftirfarandi skrefum:

1.  Í Report Designer fara **Fyrirtæki**&gt;**Bygging Loka Flokka**.
2.  Velja flokk bygging loka til að flytja og smellið á **Út**. **Athugasemd:** Fyrir Dynamics 365 fyrir Aðgerðir, eina bygging loka flokkinn studd, **Sjálfgefin**.
3.  Veljið skilgreiningar til að flytja út skýrslu:
    -   Til að flytja út allar skýrsluskilgreiningar og tengdar einingar er smellt á **Velja allt**.
    -   Til að flytja út tilteknar skýrslur, línur, dálka, skipurit eða víddasamstæður er smellt á viðeigandi flipa og svo valin atriði til að flytja út. Haldið inni Ctrl-lyklinum til að velja mörg atriði á flipa. Þegar velja skýrslur til að flytja út tengdar línur, dálka, trees og víddasamstæður valin.

4.  Smellt er á **Flytja**.
5.  Færið inn skráarnafn og velja á öruggum stað þar sem á að vista útfluttar skýrsluskilgreiningar.
6.  Click **Save**.

Skráin er hægt að afrita eða hlaða upp á öruggan stað, þar sem það á að flytja inn í öðru umhverfi á öðrum tíma. Hægt er að finna upplýsingar um notkun í lykil Microsoft Azure geymslu í [Flytja gögn með í AzCopy Command-Line Utility](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy). **Athugasemd:** Microsoft ekki veita geymslu lykill sem hluti af notanda Dynamics 365 fyrir Aðgerðir innkaupasamnings. Annaðhvort verður innkaupalykill til geymslu eða nota lykil geymslu úr aðskildum Azure áskrift. **Mikilvægt:** Huga hegðun drifi D á Azure Hýsilsheiti Vélar. Ekki geyma útfluttar bygging loka flokka hér varanlega. Sjá frekari upplýsingar um tímabundna keyrir [Skilningur tímabundin drif í Windows Azure Hýsilsheiti Vélar](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).

## <a name="stop-services"></a>Stöðva þjónustu
Remote Desktop er notuð til að tengjast öllum tölvum í umhverfinu og stöðva eftirfarandi Windows þjónustu með því að nota services.msc:

-   Vefnum birtingu þjónustu (á allar AOS tölvur)
-   Microsoft Dynamics 365 Aðgerðir Runu Stjórnun þjónustu (í ekki-einka aos-tölvum aðeins)
-   Management Reporter 2012 Ferli Þjónustu (á BI tölvum aðeins)

Þessar services hafa opna tengingar við Dynamics 365 fyrir Aðgerðir í gagnagrunni.

## <a name="reset"></a>Endurstilla
#### <a name="locate-the-latest-dataupgradezip-package"></a>Finna síðasta DataUpgrade.zip pakka

Finna síðasta pakka DataUpgrade.zip með stefnur fannst í [Sækja forskrift DataUpgrade.zip](..\migration-upgrade\upgrade-data-to-latest-update.md). Stefnur fyrir útskýra hvernig á að finna rétta útgáfan af uppfærslu gagnapakka fyrir tölvuumhverfið.

#### <a name="execute-scripts-against-dynamics-365-for-operations-database"></a>Keyra forskriftir gagnvart Dynamics 365 Aðgerðir gagnagrunns

Keyra forskriftir eftirfarandi gagnvart Dynamics 365 fyrir gagnagrunn Aðgerðir (ekki gagnvart fjárhagslegar skýrslugagnagrunns).

-   DataUpgrade.zip\\AosService\\Forskriftum\\ConfigureAxReportingIntegration.sql
-   DataUpgrade.zip\\AosService\\Forskriftum\\GrantAzViewChangeTracking.sql

Þessar forskriftir tryggja að notendur, hlutverk og stillingar á breytingarakningu séu réttar.

#### <a name="execute-powershell-command-to-reset-database"></a>Keyra PowerShell-skipun til að endurstilla gagnagrunns

Keyra eftirfarandi skipun beint á aos-tölvunni til að endurstilla samþættingu á milli Dynamics 365 aðgerða og fjárhagsskýrslugerð:

1.  Opna Windows PowerShell sem Kerfisstjóri.
2.  Keyra: F:
3.  Keyra: cd F:\\MRApplicationService\\MRInstallDirectory
4.  Keyra: Import-Module. \\Server\\MRDeploy\\MRDeploy.psd1
5.  Keyra: Endurstilla-DatamartIntegration-ÖNNUR Ástæða - ReasonDetail "&lt;mínar ástæða endurstillingu&gt;"
    -   Spurt verður að færa inn "Y" til að staðfesta.

Útskýring á færibreytur:

-   Gild gildi fyrir - Ástæða eru: VIÐSKIPTAVINASETRI, BADDATA, OTHER.
-   -ReasonDetail færibreytan er textareikninga.
-   Ástæða og reasonDetail skráð í telemetry/umhverfi eftirlit.

## <a name="start-services"></a>Ræsa þjónustu
Nota services.msc að endurræsa þjónustuna sem þú hættir fyrr:

-   Vefnum birtingu þjónustu (á allar AOS tölvur)
-   Microsoft Dynamics 365 Aðgerðir Runu Stjórnun þjónustu (í ekki-einka aos-tölvum aðeins)
-   Management Reporter 2012 Ferli Þjónustu (á BI tölvum aðeins)

## <a name="import-report-definitions"></a>Flytja skilgreiningar á skýrslu
Flytja inn notanda skýrsluhannana úr Skýrsluhönnuðinum með búin til við að flytja skrána:

1.  Í Report Designer fara **Fyrirtæki**&gt;**Bygging Loka Flokka**.
2.  Velja flokk bygging loka til að flytja og smellið á **Út**. **Athugasemd:** Fyrir Dynamics 365 fyrir Aðgerðir, eina bygging loka flokkinn studd, **Sjálfgefin**.
3.  Velja á **Sjálfgefin** byggja loka og smella á **Innflutning**.
4.  Veljið skrána sem inniheldur skilgreiningar fluttar út skýrslu og smellið á **Opna**.
5.  Smellið á skýrsluskilgreiningarnar í svarglugganum Flytja inn til að flytja inn:
    -   Til að flytja inn allar skýrsluskilgreiningar og tengdar einingar er smellt á **Velja allt**.
    -   Til að flytja inn tilteknar skýrslur, línur, dálka, skipurit eða víddasamstæður skal velja skýrslur, línur, dálka, skipurit eða víddasamstæður sem á að flytja inn.

6.  Click **Import**.



