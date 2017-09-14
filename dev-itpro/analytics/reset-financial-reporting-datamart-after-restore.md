---
title: "Endurstilla fjárhagslegar skýrslugerð gagnatorgs eftir endurheimt gagnagrunns"
description: "Þetta efnisatriði lýsir hvernig á að endurstilla gagnaskemmu fyrir fjárhagsskýrslugerð eftir endurheimt Microsoft Dynamics 365 Finance and Operations gagnagrunns."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261824
ms.assetid: d0784b2c-fe10-428d-8d07-fd474ca50fcc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 9953d2f29a67b35f4bb43f577df1c4d910e379a1
ms.openlocfilehash: 08a420a776f47119a5dc47f9119545aa448ffdbd
ms.contentlocale: is-is
ms.lasthandoff: 08/03/2017

---

# <a name="reset-the-financial-reporting-data-mart-after-restoring-a-database"></a><span data-ttu-id="9e70b-103">Endurstilla fjárhagslegar skýrslugerð gagnatorgs eftir endurheimt gagnagrunns</span><span class="sxs-lookup"><span data-stu-id="9e70b-103">Reset the financial reporting data mart after restoring a database</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="9e70b-104">Þetta efnisatriði lýsir hvernig á að endurstilla gagnaskemmu fyrir fjárhagsskýrslugerð eftir endurheimt Microsoft Dynamics 365 Finance and Operations gagnagrunns.</span><span class="sxs-lookup"><span data-stu-id="9e70b-104">This topic describes how to reset the financial reporting data mart after restoring a Microsoft Dynamics 365 for Finance and Operations database.</span></span>

<span data-ttu-id="9e70b-105">Ef þú endurheimtir Finance and Operations gagnagrunninn úr öryggisafritum eða afritar gagnagrunninn úr öðru umhverfi, er nauðsynlegt að fylgja skrefunum í þessu efnisatriði til að tryggja að gagnaskemma fjárhagsskýrslugerðarinnar sé að nota endurheimtan gagnagrunn Finance and Operations á réttan hátt.</span><span class="sxs-lookup"><span data-stu-id="9e70b-105">If you ever restore your Finance and Operations database from a backup or copy the database from another environment, you must follow the steps in this topic to ensure that the financial reporting data mart is correctly using the restored Finance and Operations database.</span></span> 
<!--If you have questions about resetting the financial reporting data mart for a reason outside of restoring a Finance and Operations database, refer to the [Resetting the Management Reporter data mart](https://blogs.msdn.microsoft.com/dynamics_financial_reporting/2016/06/28/resetting-the-management-reporter-data-mart/) for more information. -->
> [!Note] 
> <span data-ttu-id="9e70b-106">Skrefin í þessu ferli eru studd fyrir Dynamics 365 for Operation útgáfu í maí 2016 (Forritsútgáfa 7.0.1265.23014 og fjárhagsleg skýrslugerð útgáfa 7.0.10000.4) og nýrri útgáfur.</span><span class="sxs-lookup"><span data-stu-id="9e70b-106">The steps in this process are supported for Dynamics 365 for Operation May 2016 release (App build 7.0.1265.23014 and financial reporting build 7.0.10000.4) and newer releases.</span></span> <span data-ttu-id="9e70b-107">Ef þú er með eldri útgáfu af Finance and Operations skaltu hafa samband við þjónustuver okkar til að fá aðstoð.</span><span class="sxs-lookup"><span data-stu-id="9e70b-107">If you have an earlier release of Finance and Operations, contact our Support team for assistance.</span></span>

## <a name="export-report-definitions"></a><span data-ttu-id="9e70b-108">Flytja út skilgreiningu á skýrslum</span><span class="sxs-lookup"><span data-stu-id="9e70b-108">Export report definitions</span></span>
<span data-ttu-id="9e70b-109">Fyrst skal flytja út skýrsluhönnun sem er staðsett í Skýrsluhönnuðinum með eftirfarandi skrefum:</span><span class="sxs-lookup"><span data-stu-id="9e70b-109">First, export the report designs located in the Report Designer, using the following steps:</span></span>

1.  <span data-ttu-id="9e70b-110">Í Skýrsluhönnun ferðu í **Fyrirtæki** &gt; **Einingahópar**.</span><span class="sxs-lookup"><span data-stu-id="9e70b-110">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="9e70b-111">Veldu einingahópinn sem á að flytja út og síðan er smellt á **Flytja út**.</span><span class="sxs-lookup"><span data-stu-id="9e70b-111">Select the building block group to export, and click **Export**.</span></span> 
    > [!Note] 
    > <span data-ttu-id="9e70b-112">Í Finance and Operations er aðeins einn einingahópur studdur, **Sjálfgefið**.</span><span class="sxs-lookup"><span data-stu-id="9e70b-112">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
3.  <span data-ttu-id="9e70b-113">Veldu skýrsluskilgreiningar til að flytja út:</span><span class="sxs-lookup"><span data-stu-id="9e70b-113">Select the report definitions to export:</span></span>
    -   <span data-ttu-id="9e70b-114">Til að flytja út allar skýrsluskilgreiningar og tengdar einingar er smellt á **Velja allt**.</span><span class="sxs-lookup"><span data-stu-id="9e70b-114">To export all your report definitions and the associated building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="9e70b-115">Til að flytja út tilteknar skýrslur, línur, dálka, skipurit eða víddasamstæður er smellt á viðeigandi flipa og svo valin atriði til að flytja út.</span><span class="sxs-lookup"><span data-stu-id="9e70b-115">To export specific reports, rows, columns, trees, or dimension sets, click the appropriate tab, and then select the items to export.</span></span> <span data-ttu-id="9e70b-116">Haldið inni Ctrl-lyklinum til að velja mörg atriði á flipa.</span><span class="sxs-lookup"><span data-stu-id="9e70b-116">Press and hold the Ctrl key to select multiple items in a tab.</span></span> <span data-ttu-id="9e70b-117">Þegar valdar eru skýrslur til að flytja út eru einnig valdar tengdar línur, dálkar, skipurit og víddasamstæður.</span><span class="sxs-lookup"><span data-stu-id="9e70b-117">When you select reports to export, the associated rows, columns, trees, and dimension sets are selected.</span></span>

4.  <span data-ttu-id="9e70b-118">Smellt er á **Útflutning**.</span><span class="sxs-lookup"><span data-stu-id="9e70b-118">Click **Export**.</span></span>
5.  <span data-ttu-id="9e70b-119">Færið inn skráarnafn og veljið öruggum stað þar sem á að vista útfluttar skýrsluskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="9e70b-119">Enter a file name and select a secure location where you want to save the exported report definitions.</span></span>
6.  <span data-ttu-id="9e70b-120">Smellið á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="9e70b-120">Click **Save**.</span></span>

<span data-ttu-id="9e70b-121">Skrána má afrita eða hlaða upp á öruggan stað, þar sem flytja á hana inn í annað umhverfi seinna.</span><span class="sxs-lookup"><span data-stu-id="9e70b-121">The file can be copied or uploaded to a secure location, allowing it to be imported into a different environment at another time.</span></span> <span data-ttu-id="9e70b-122">Hægt er að finna upplýsingar um notkun í geymslulykils Microsoft Azure í [Flytja gögn með AzCopy Command-Line Utility](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span><span class="sxs-lookup"><span data-stu-id="9e70b-122">Information about using a Microsoft Azure storage account can be found in [Transfer data with the AzCopy Command-Line Utility](https://docs.microsoft.com/en-gb/azure/storage/storage-use-azcopy).</span></span> 
> [!NOTE]
> <span data-ttu-id="9e70b-123">Microsoft veitir ekki geymslulykil sem hluta af samningi þínum um Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9e70b-123">Microsoft doesn’t provide a storage account as part of your Finance and Operations agreement.</span></span> <span data-ttu-id="9e70b-124">Annaðhvort verður að kaupa geymslulykil eða nota geymslulykil úr aðskilinni Azure-áskrift.</span><span class="sxs-lookup"><span data-stu-id="9e70b-124">You must either purchase a storage account or use a storage account from a separate Azure subscription.</span></span> 
> [!WARNING]
> <span data-ttu-id="9e70b-125">Huga að hegðun á D-drifi á sýndarvélum Azure.</span><span class="sxs-lookup"><span data-stu-id="9e70b-125">Be aware of the behavior of the D drive on Azure Virtual Machines.</span></span> <span data-ttu-id="9e70b-126">Ekki geyma útflutta einingahópa hér varanlega.</span><span class="sxs-lookup"><span data-stu-id="9e70b-126">Do not keep your exported building block groups here permanently.</span></span> <span data-ttu-id="9e70b-127">Sjá frekari upplýsingar um tímabundin drif á [Skilningur á tímabundnum drifum í sýndarvélum Windows Azure](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span><span class="sxs-lookup"><span data-stu-id="9e70b-127">For more information about temporary drives, see [Understanding the temporary drive on Windows Azure Virtual Machines](https://blogs.msdn.microsoft.com/mast/2013/12/06/understanding-the-temporary-drive-on-windows-azure-virtual-machines/).</span></span>

## <a name="stop-services"></a><span data-ttu-id="9e70b-128">Stöðvunarþjónusta</span><span class="sxs-lookup"><span data-stu-id="9e70b-128">Stop services</span></span>
<span data-ttu-id="9e70b-129">Remote Desktop er notuð til að tengjast öllum tölvum í umhverfinu og stöðva eftirfarandi Windows þjónustu með því að nota services.msc:</span><span class="sxs-lookup"><span data-stu-id="9e70b-129">Use Remote Desktop to connect to all the computers in the environment and stop the following Windows services by using services.msc:</span></span>

-   <span data-ttu-id="9e70b-130">Birtingarþjónusta á vefnum (á allar AOS tölvur)</span><span class="sxs-lookup"><span data-stu-id="9e70b-130">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="9e70b-131">Runustjórnunarþjónusta Finance and Operations (aðeins í AOS-tölvum sem ekki eru einkatölvur)</span><span class="sxs-lookup"><span data-stu-id="9e70b-131">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="9e70b-132">Ferlaþjónusta Management Reporter 2012 (aðeins á BI tölvum)</span><span class="sxs-lookup"><span data-stu-id="9e70b-132">Management Reporter 2012 Process Service (on BI computers only)</span></span>

<span data-ttu-id="9e70b-133">Þessar þjónustur hafa opna tengingar við gagnagrunn Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9e70b-133">These services will have open connections to the Finance and Operations database.</span></span>

## <a name="reset"></a><span data-ttu-id="9e70b-134">Endurstilla</span><span class="sxs-lookup"><span data-stu-id="9e70b-134">Reset</span></span>
#### <a name="locate-and-download-the-latest-minorversiondataupgradezip-package"></a><span data-ttu-id="9e70b-135">Finna og hlaða niður síðasta MinorVersionDataUpgrade.zip pakkanum</span><span class="sxs-lookup"><span data-stu-id="9e70b-135">Locate and download the latest MinorVersionDataUpgrade.zip package</span></span>

<span data-ttu-id="9e70b-136">Finna síðasta pakka MinorVersionDataUpgrade.zip með stefnum sem fundust í [Hlaða niður síðasta virkjanlega gagnauppfærslupakkanum](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span><span class="sxs-lookup"><span data-stu-id="9e70b-136">Locate the latest MinorVersionDataUpgrade.zip package using the directions found in [Download the latest data upgrade deployable package](..\migration-upgrade\upgrade-data-to-latest-update.md#download-the-latest-data-upgrade-deployable-package).</span></span> <span data-ttu-id="9e70b-137">Stefnurnar útskýra hvernig á að finna og hlaða niður rétta útgáfu af gagnauppfærslupakka.</span><span class="sxs-lookup"><span data-stu-id="9e70b-137">The directions explain how to locate and download the correct version of the data upgrade package.</span></span> <span data-ttu-id="9e70b-138">Uppfærslu er ekki krafist til að hlaða niður MinorVersionDataUpgrade.zip pakkanum.</span><span class="sxs-lookup"><span data-stu-id="9e70b-138">An upgrade is not required to download the MinorVersionDataUpgrade.zip package.</span></span> <span data-ttu-id="9e70b-139">Þú þarft einungis að ljúka skrefunum í „Hlaða niður síðasta virkjanlega gagnauppfærslupakkanum“ hlutanum án þess að framkvæma neitt af hinum skrefunum í greininni til að sækja afrit af MinorVersionDataUpgrade.zip pakkanum.</span><span class="sxs-lookup"><span data-stu-id="9e70b-139">You only need to complete the steps in the “Download the latest data upgrade deployable package” section without performing any of the other steps in the article to retrieve a copy of the MinorVersionDataUpgrade.zip package.</span></span>

#### <a name="execute-scripts-against-finance-and-operations-database"></a><span data-ttu-id="9e70b-140">Keyra forskriftir á gagnagrunn Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9e70b-140">Execute scripts against Finance and Operations database</span></span>

<span data-ttu-id="9e70b-141">Keyra eftirfarandi forskriftir á gagnagrunn Finance and Operations (ekki á gagnagrunn fjárhagsskýrslna).</span><span class="sxs-lookup"><span data-stu-id="9e70b-141">Run the following scripts against the Finance and Operations database (not against the financial reporting database).</span></span>

-   <span data-ttu-id="9e70b-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span><span class="sxs-lookup"><span data-stu-id="9e70b-142">DataUpgrade.zip\\AosService\\Scripts\\ConfigureAxReportingIntegration.sql</span></span>
-   <span data-ttu-id="9e70b-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span><span class="sxs-lookup"><span data-stu-id="9e70b-143">DataUpgrade.zip\\AosService\\Scripts\\GrantAzViewChangeTracking.sql</span></span>

<span data-ttu-id="9e70b-144">Þessar forskriftir tryggja að notendur, hlutverk og stillingar á breytingarakningu séu réttar.</span><span class="sxs-lookup"><span data-stu-id="9e70b-144">These scripts ensure that the users, roles, and change tracking settings are correct.</span></span>

#### <a name="execute-powershell-command-to-reset-database"></a><span data-ttu-id="9e70b-145">Keyra PowerShell-skipun til að endurstilla gagnagrunn</span><span class="sxs-lookup"><span data-stu-id="9e70b-145">Execute PowerShell command to reset database</span></span>

<span data-ttu-id="9e70b-146">Keyra eftirfarandi skipun beint á AOS-tölvunni til að endurstilla samþættingu á milli Finance and Operations og fjárhagsskýrslugerðar:</span><span class="sxs-lookup"><span data-stu-id="9e70b-146">Execute the following command, directly on the AOS computer, to reset the integration between Finance and Operations and financial reporting:</span></span>

1.  <span data-ttu-id="9e70b-147">Opna Windows PowerShell sem Kerfisstjóri.</span><span class="sxs-lookup"><span data-stu-id="9e70b-147">Open Windows PowerShell as Administrator.</span></span>
2.  <span data-ttu-id="9e70b-148">Framkvæma: F:</span><span class="sxs-lookup"><span data-stu-id="9e70b-148">Execute: F:</span></span>
3.  <span data-ttu-id="9e70b-149">Keyra: cd F:\\MRApplicationService\\MRInstallDirectory</span><span class="sxs-lookup"><span data-stu-id="9e70b-149">Execute: cd F:\\MRApplicationService\\MRInstallDirectory</span></span>
4.  <span data-ttu-id="9e70b-150">Keyra: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span><span class="sxs-lookup"><span data-stu-id="9e70b-150">Execute: Import-Module .\\Server\\MRDeploy\\MRDeploy.psd1</span></span>
5.  <span data-ttu-id="9e70b-151">Keyra: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;ástæða mín fyrir endurstillingu&gt;”</span><span class="sxs-lookup"><span data-stu-id="9e70b-151">Execute: Reset-DatamartIntegration -Reason OTHER -ReasonDetail “&lt;my reason for resetting&gt;”</span></span>
    -   <span data-ttu-id="9e70b-152">Beðið verður um að fært sé inn "Y" til að staðfesta.</span><span class="sxs-lookup"><span data-stu-id="9e70b-152">You will be asked to enter “Y” to confirm.</span></span>

<span data-ttu-id="9e70b-153">Útskýring á færibreytum:</span><span class="sxs-lookup"><span data-stu-id="9e70b-153">Explanation of parameters:</span></span>

-   <span data-ttu-id="9e70b-154">Gild gildi fyrir - Ástæða eru: SERVICING, BADDATA, OTHER.</span><span class="sxs-lookup"><span data-stu-id="9e70b-154">The valid values for -Reason are: SERVICING, BADDATA, OTHER.</span></span>
-   <span data-ttu-id="9e70b-155">ReasonDetail færibreytan er fyrir valkvæman texta.</span><span class="sxs-lookup"><span data-stu-id="9e70b-155">The -ReasonDetail parameter is free text.</span></span>
-   <span data-ttu-id="9e70b-156">Ástæða og reasonDetail verða skráð í eftirlita fjarmælingu/umhverfis.</span><span class="sxs-lookup"><span data-stu-id="9e70b-156">The reason and reasonDetail will be recorded in telemetry/environment monitoring.</span></span>

## <a name="start-services"></a><span data-ttu-id="9e70b-157">Ræsiþjónusta</span><span class="sxs-lookup"><span data-stu-id="9e70b-157">Start services</span></span>
<span data-ttu-id="9e70b-158">Nota services.msc að endurræsa þjónustuna sem þú hættir áður:</span><span class="sxs-lookup"><span data-stu-id="9e70b-158">Use services.msc to restart the services that you stopped earlier:</span></span>

-   <span data-ttu-id="9e70b-159">Birtingarþjónusta á vefnum (á allar AOS tölvur)</span><span class="sxs-lookup"><span data-stu-id="9e70b-159">World wide web publishing service (on all AOS computers)</span></span>
-   <span data-ttu-id="9e70b-160">Runustjórnunarþjónusta Finance and Operations (aðeins í AOS-tölvum sem ekki eru einkatölvur)</span><span class="sxs-lookup"><span data-stu-id="9e70b-160">Microsoft Dynamics 365 for Finance and Operations Batch Management Service (on non-private AOS computers only)</span></span>
-   <span data-ttu-id="9e70b-161">Ferlaþjónusta Management Reporter 2012 (aðeins á BI tölvum)</span><span class="sxs-lookup"><span data-stu-id="9e70b-161">Management Reporter 2012 Process Service (on BI computers only)</span></span>

## <a name="import-report-definitions"></a><span data-ttu-id="9e70b-162">Flytja inn skýrsluskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="9e70b-162">Import report definitions</span></span>
<span data-ttu-id="9e70b-163">Flytja inn skýrsluhönnun notanda úr Skýrsluhönnuðinum með skránni sem var búin til við útflutninginn:</span><span class="sxs-lookup"><span data-stu-id="9e70b-163">Import your report designs from the Report Designer, using the file created during the export:</span></span>

1.  <span data-ttu-id="9e70b-164">Í Skýrsluhönnun ferðu í **Fyrirtæki** &gt; **Einingahópar**.</span><span class="sxs-lookup"><span data-stu-id="9e70b-164">In the Report Designer, go to **Company** &gt; **Building Block Groups**.</span></span>
2.  <span data-ttu-id="9e70b-165">Veldu einingahópinn sem á að flytja út og síðan er smellt á **Flytja út**.</span><span class="sxs-lookup"><span data-stu-id="9e70b-165">Select the building block group to export, and click **Export**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="9e70b-166">Í Finance and Operations er aðeins einn einingahópur studdur, **Sjálfgefið**.</span><span class="sxs-lookup"><span data-stu-id="9e70b-166">For Finance and Operations, only one building block group is supported, **Default**.</span></span>
    
3.  <span data-ttu-id="9e70b-167">Veldu eininguna **Vanskil** og smelltu á **Innflutning**.</span><span class="sxs-lookup"><span data-stu-id="9e70b-167">Select the **Default** building block and click **Import**.</span></span>
4.  <span data-ttu-id="9e70b-168">Veldu skrána með útfluttum skýrsluskilgreiningum og smelltu á **Opna**.</span><span class="sxs-lookup"><span data-stu-id="9e70b-168">Select the file containing the exported report definitions and click **Open**.</span></span>
5.  <span data-ttu-id="9e70b-169">Smellið á skýrsluskilgreiningarnar í svarglugganum Flytja inn til að flytja inn:</span><span class="sxs-lookup"><span data-stu-id="9e70b-169">In the Import dialog box, select the report definitions to import:</span></span>
    -   <span data-ttu-id="9e70b-170">Til að flytja inn allar skýrsluskilgreiningar og tengdar einingar er smellt á **Velja allt**.</span><span class="sxs-lookup"><span data-stu-id="9e70b-170">To import all the report definitions and the supporting building blocks, click **Select All**.</span></span>
    -   <span data-ttu-id="9e70b-171">Til að flytja inn tilteknar skýrslur, línur, dálka, skipurit eða víddasamstæður skal velja skýrslur, línur, dálka, skipurit eða víddasamstæður sem á að flytja inn.</span><span class="sxs-lookup"><span data-stu-id="9e70b-171">To import specific reports, rows, columns, trees, or dimension sets, select the reports, rows, columns, trees, or dimension sets to import.</span></span>

6.  <span data-ttu-id="9e70b-172">Smelltu á **Flytja inn**.</span><span class="sxs-lookup"><span data-stu-id="9e70b-172">Click **Import**.</span></span>





