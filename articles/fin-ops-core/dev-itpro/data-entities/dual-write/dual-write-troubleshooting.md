---
title: Almenn úrræðaleit
description: Þetta efni veitir upplýsingar um almenna úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: f7ee0b5aa4e72614205e129acd986376b33efc70
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172692"
---
# <a name="general-troubleshooting"></a><span data-ttu-id="063a9-103">Almenn úrræðaleit</span><span class="sxs-lookup"><span data-stu-id="063a9-103">General troubleshooting</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="063a9-104">Þetta efni veitir upplýsingar um almenna úrræðaleit um samþættingu á tvöföldum skrifum á milli forrita Finance and Operations og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="063a9-104">This topic provides general troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="063a9-105">Nokkur þeirra atriða sem þetta efni fjallar um geta krafist annað hvort kerfisstjórans eða Microsoft Azure Active Directory (Azure AD) Leyfisupplýsingar leigjanda.</span><span class="sxs-lookup"><span data-stu-id="063a9-105">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="063a9-106">Hlutinn fyrir hvert vandamál útskýrir hvort krafist sé sérstaks hlutverks eða skilríkja.</span><span class="sxs-lookup"><span data-stu-id="063a9-106">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a><span data-ttu-id="063a9-107">Þegar þú reynir að setja upp pakka fyrir tvöföld skrif með því að nota verkfærið Package Deployer eru engar fáanlegar lausnir sýndar</span><span class="sxs-lookup"><span data-stu-id="063a9-107">When you try to install the dual-write package by using the package deployer tool, no available solutions are shown</span></span>

<span data-ttu-id="063a9-108">Sumar útgáfur af verkfærinu Package Deployer eru ósamrýmanlegar með tvískiptu lausnarpakkanum.</span><span class="sxs-lookup"><span data-stu-id="063a9-108">Some versions of the package deployer tool are incompatible with the dual-write solution package.</span></span> <span data-ttu-id="063a9-109">Til að setja upp pakkann svo vel sé skaltu passa að nota [útgáfu 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) eða nýrri af verkfærinu Package Deployer.</span><span class="sxs-lookup"><span data-stu-id="063a9-109">To successfully install the package, be sure to use [version 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) or later of the package deployer tool.</span></span>

<span data-ttu-id="063a9-110">Eftir að þú hefur sett upp verkfærið Package Deployer skaltu setja upp lausnarpakkann með því að fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="063a9-110">After you install the package deployer tool, install the solution package by following these steps.</span></span>

1. <span data-ttu-id="063a9-111">Sæktu nýjustu pakkaskrá lausnarinnar af Yammer.com.</span><span class="sxs-lookup"><span data-stu-id="063a9-111">Download the latest solution package file from Yammer.com.</span></span> <span data-ttu-id="063a9-112">Eftir að zip-skráin hefur verið sótt skaltu hægrismella á hana og velja **Eiginleikar**.</span><span class="sxs-lookup"><span data-stu-id="063a9-112">After the package zip file is downloaded, right-click it, and select **Properties**.</span></span> <span data-ttu-id="063a9-113">Veldu gátreitinn **Opna fyrir** og veldu síðan **Beita**.</span><span class="sxs-lookup"><span data-stu-id="063a9-113">Select the **Unblock** check box, and then select **Apply**.</span></span> <span data-ttu-id="063a9-114">Ef þú sérð ekki gátreitinn **Opna fyrir** er zip-skráin þegar aflæst og þú getur sleppt þessu skrefi.</span><span class="sxs-lookup"><span data-stu-id="063a9-114">If you don't see the **Unblock** check box, the zip file is already unblocked, and you can skip this step.</span></span>

    ![Svargluggi eiginleika](media/unblock_option.png)

2. <span data-ttu-id="063a9-116">Opnaðu zip-skrána með pakkanum og afritaðu allar skrárnar í möppuna **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**.</span><span class="sxs-lookup"><span data-stu-id="063a9-116">Extract the package zip file, and copy all the files in the **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438** folder.</span></span>

    ![Innihald möppunnar Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. <span data-ttu-id="063a9-118">Límdu allar afritaðar skrár í möppuna **Verkfæri** í verkfærinu Package Deployer.</span><span class="sxs-lookup"><span data-stu-id="063a9-118">Paste all the copied files into the **Tools** folder of the package deployer tool.</span></span> 
4. <span data-ttu-id="063a9-119">Keyrðu **PackageDeployer.exe** til að velja Common Data Service umhverfið og setja upp lausnirnar.</span><span class="sxs-lookup"><span data-stu-id="063a9-119">Run **PackageDeployer.exe** to select the Common Data Service environment and install the solutions.</span></span>

    ![Innihald möppunnar Verkfæri](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-common-data-service-to-view-error-details"></a><span data-ttu-id="063a9-121">Kveiktu á og skoðaðu rakningarkladda viðbótar í Common Data Service til að skoða villuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="063a9-121">Enable and view the plug-in trace log in Common Data Service to view error details</span></span>

<span data-ttu-id="063a9-122">**Nauðsynlegt hlutverk til að kveikja á rakningarkladda og skoða villur:** Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="063a9-122">**Required role to turn on the trace log and view errors:** System admin</span></span>

<span data-ttu-id="063a9-123">Fylgdu þessum skrefum til að kveikja á rakningarkladda.</span><span class="sxs-lookup"><span data-stu-id="063a9-123">To turn on the trace log, follow these steps.</span></span>

1. <span data-ttu-id="063a9-124">Skráðu þig inn í forrit Finance and Operations, opnaðu síðuna **Stillingar** og síðan, undir **Kerfi**, velurðu **Stjórnun**.</span><span class="sxs-lookup"><span data-stu-id="063a9-124">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **System**, select **Administration**.</span></span>
2. <span data-ttu-id="063a9-125">Á síðunni **Stjórnun** skal velja **Kerfisstillingar**.</span><span class="sxs-lookup"><span data-stu-id="063a9-125">On the **Administration** page, select **System Settings**.</span></span>
3. <span data-ttu-id="063a9-126">Á flipanum **Sérsnið**, í reitnum **Viðbóð og sérsniðnar rakningaraðgerðir verkflæðis**, velurðu **Allt** til að virkja rakningarkladda viðbótar.</span><span class="sxs-lookup"><span data-stu-id="063a9-126">On the **Customization** tab, in the **Plug-in and custom workflow activity tracing** field, select **All** to enable the plug-in trace log.</span></span> <span data-ttu-id="063a9-127">Ef þú vilt skrá rakningarkladda aðeins þegar undantekningar eiga sér stað, geturðu valið **Undantekning** í staðinn.</span><span class="sxs-lookup"><span data-stu-id="063a9-127">If you want to log trace logs only when exceptions occur, you can select **Exception** instead.</span></span>


<span data-ttu-id="063a9-128">Fylgdu þessum skrefum til að skoða rakningarkladdann.</span><span class="sxs-lookup"><span data-stu-id="063a9-128">To view the trace log, follow these steps.</span></span>

1. <span data-ttu-id="063a9-129">Skráðu þig inn í forrit Finance and Operations, opnaðu síðuna **Stillingar** og síðan, undir **Sérsnið**, velurðu **Rakningarkladdi viðbótar**.</span><span class="sxs-lookup"><span data-stu-id="063a9-129">Sign in to the Finance and Operations app, open the **Settings** page, and then, under **Customization**, select **Plug-in Trace Log**.</span></span>
2. <span data-ttu-id="063a9-130">Finndu rakningarkladdana þar sem reiturinn **Heiti gerðar** er stilltur á **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span><span class="sxs-lookup"><span data-stu-id="063a9-130">Find the trace logs where the **Type Name** field is set to **Microsoft.Dynamics.Integrator.CrmPlugins.Plugin**.</span></span>
3. <span data-ttu-id="063a9-131">Tvísmelltu á hlut til að skoða alla skrána og síðan á flýtiflipanum **Framkvæmd**, skoðarðu textann **Skilaboðablokk**.</span><span class="sxs-lookup"><span data-stu-id="063a9-131">Double-click an item to view the full log, and then, on the **Execution** FastTab, review the **Message Block** text.</span></span>

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a><span data-ttu-id="063a9-132">Kveiktu á kembiforriti til að leysa vandamál samstillingar í beinni í forritum Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="063a9-132">Enable debug mode to troubleshoot live synchronization issues in Finance and Operations apps</span></span>

<span data-ttu-id="063a9-133">**Nauðsynlegt hlutverk til að skoða villurnar:** Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="063a9-133">**Required role to view the errors:** System admin</span></span>

<span data-ttu-id="063a9-134">Tvíritunarvillur sem eiga uppruna sinn í Common Data Service geta komið fram í forriti Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="063a9-134">Dual-write errors that originate in Common Data Service can appear in the Finance and Operations app.</span></span> <span data-ttu-id="063a9-135">Í sumum tilvikum er allur texti villuboðanna ekki tiltækur vegna þess að skeytið er of langt eða inniheldur persónugreinanlegar upplýsingar (PII).</span><span class="sxs-lookup"><span data-stu-id="063a9-135">In some cases, the full text of the error message isn't available because the message is too long or contains personally identifying information (PII).</span></span> <span data-ttu-id="063a9-136">Þú getur kveikt á fjölorðri skráningu á villum með því að fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="063a9-136">You can turn on verbose logging for errors by following these steps.</span></span>

1. <span data-ttu-id="063a9-137">Allar verkefnisstillingar í forritum Finance and Operations eru með eiginleikann **IsDebugMode** í eingunni **DualWriteProjectConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="063a9-137">All project configurations in Finance and Operations apps have an **IsDebugMode** property in the **DualWriteProjectConfiguration** entity.</span></span> <span data-ttu-id="063a9-138">Opnaðu eininguna **DualWriteProjectConfiguration** með því að nota Excel-viðbótina.</span><span class="sxs-lookup"><span data-stu-id="063a9-138">Open the **DualWriteProjectConfiguration** entity by using the Excel add-in.</span></span>

    > [!TIP]
    > <span data-ttu-id="063a9-139">Auðveld leið til að opna eininguna er að kveikja á stillingunni **Hönnun** í Excel-viðbótinni og síðan bætt við **DualWriteProjectConfigurationEntity** í vinnublaðið.</span><span class="sxs-lookup"><span data-stu-id="063a9-139">An easy way to open the entity is to turn on **Design** mode in the Excel add-in and then add **DualWriteProjectConfigurationEntity** to the worksheet.</span></span> <span data-ttu-id="063a9-140">Nánari upplýsingar eru í [Opna einingagögn í Excel og uppfæra þau með Excel-innbót](../../office-integration/use-excel-add-in.md).</span><span class="sxs-lookup"><span data-stu-id="063a9-140">For more information, see [Open entity data in Excel and update it by using the Excel add-in](../../office-integration/use-excel-add-in.md).</span></span>

2. <span data-ttu-id="063a9-141">Stilltu eiginleikann **IsDebugMode** á **Já** fyrir verkið.</span><span class="sxs-lookup"><span data-stu-id="063a9-141">Set the **IsDebugMode** property to **Yes** for the project.</span></span>
3. <span data-ttu-id="063a9-142">Keyrðu atburðarásina sem er að búa til villur.</span><span class="sxs-lookup"><span data-stu-id="063a9-142">Run the scenario that is generating errors.</span></span>
4. <span data-ttu-id="063a9-143">Fjölorðir kladdar eru fáanlegir í töflunni DualWriteErrorLog.</span><span class="sxs-lookup"><span data-stu-id="063a9-143">The verbose logs are available in the DualWriteErrorLog table.</span></span> <span data-ttu-id="063a9-144">Notaðu eftirfarandi slóð til að fletta upp gögnum í vafra töflunnar (skipta út **XXX** eftir atvikum):</span><span class="sxs-lookup"><span data-stu-id="063a9-144">To look up data in the table browser, use the following URL (replace **XXX** as appropriate):</span></span>

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=>DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a><span data-ttu-id="063a9-145">Athugaðu samstillingarvillur á sýndarvélinni fyrir forritið Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="063a9-145">Check synchronization errors on the virtual machine for the Finance and Operations app</span></span>

<span data-ttu-id="063a9-146">**Nauðsynlegt hlutverk til að skoða villurnar:** Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="063a9-146">**Required role to view the errors:** System admin</span></span>

1. <span data-ttu-id="063a9-147">Skráðu þig inn í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="063a9-147">Sign in to Microsoft Dynamics Lifecycle Services (LCS).</span></span>
2. <span data-ttu-id="063a9-148">Opnaðu LCS-verkið sem þú valdir til að gera tvískriftaprófun fyrir.</span><span class="sxs-lookup"><span data-stu-id="063a9-148">Open the LCS project that you chose to do the dual-write testing for.</span></span>
3. <span data-ttu-id="063a9-149">Veldu reitinn **Umhverfi í skýi**.</span><span class="sxs-lookup"><span data-stu-id="063a9-149">Select the **Cloud-hosted environments** tile.</span></span>
4. <span data-ttu-id="063a9-150">Notaðu Remote Desktop til að skrá þig inn á sýndarvélina (VM) fyrir forrit Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="063a9-150">Use Remote Desktop to sign in to the virtual machine (VM) for the Finance and Operations app.</span></span> <span data-ttu-id="063a9-151">Notaðu staðbundna reikninginn sem er sýndur í LCS.</span><span class="sxs-lookup"><span data-stu-id="063a9-151">Use the local account that is shown in LCS.</span></span>
5. <span data-ttu-id="063a9-152">Opnaðu tilvikayfirlit.</span><span class="sxs-lookup"><span data-stu-id="063a9-152">Open Event viewer.</span></span>
6. <span data-ttu-id="063a9-153">Veldu **Forrit og þjónustukladdar \> Microsoft \> Dynamics \> AX -DualWriteSync \> Virkt**.</span><span class="sxs-lookup"><span data-stu-id="063a9-153">Select **Applications and Services Logs \> Microsoft \> Dynamics \> AX-DualWriteSync \> Operational**.</span></span>
7. <span data-ttu-id="063a9-154">Farðu yfir listann yfir nýlegar villur.</span><span class="sxs-lookup"><span data-stu-id="063a9-154">Review the list of recent errors.</span></span>

## <a name="unlink-and-link-another-common-data-service-environment-from-a-finance-and-operations-app"></a><span data-ttu-id="063a9-155">Taktu af og tengdu annað Common Data Service umhverfi úr forrit Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="063a9-155">Unlink and link another Common Data Service environment from a Finance and Operations app</span></span>

<span data-ttu-id="063a9-156">**Nauðsynleg skilríki til að aftengja umhverfið:** Azure AD leigjandastjóri</span><span class="sxs-lookup"><span data-stu-id="063a9-156">**Required credentials to unlink the environment:** Azure AD tenant admin</span></span>

1. <span data-ttu-id="063a9-157">Innskráning í forritið Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="063a9-157">Sign in to the Finance and Operations app.</span></span>
2. <span data-ttu-id="063a9-158">Farðu í **Vinnusvæði \> Gagnastjórnun** og veldu reitinn **Tvöfalt skrif**.</span><span class="sxs-lookup"><span data-stu-id="063a9-158">Go to **Workspaces \> Data management**, and select the **Dual Write** tile.</span></span>
3. <span data-ttu-id="063a9-159">Veldu allar keyrandi kortlagningar og veldu síðan **Hætta**.</span><span class="sxs-lookup"><span data-stu-id="063a9-159">Select all running mappings, and then select **Stop**.</span></span>
4. <span data-ttu-id="063a9-160">Veldu **Aftengja umhverfi**.</span><span class="sxs-lookup"><span data-stu-id="063a9-160">Select **Unlink environment**.</span></span>
5. <span data-ttu-id="063a9-161">Veldu **Já** til að staðfesta aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="063a9-161">Select **Yes** to confirm the operation.</span></span>

<span data-ttu-id="063a9-162">Þú getur nú tengt nýtt umhverfi.</span><span class="sxs-lookup"><span data-stu-id="063a9-162">You can now link a new environment.</span></span>
