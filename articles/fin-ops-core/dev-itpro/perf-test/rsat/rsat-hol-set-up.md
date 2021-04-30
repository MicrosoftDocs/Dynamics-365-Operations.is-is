---
title: Setja upp kennslu fyrir Regression Suite Automation Tool
description: Þetta efni er kennsluefni sem sýnir hvernig á að setja upp Regression Suite Automation Tool (RSAT).
author: robinarh
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: 7c6e4dcbd854cfadbc34f0040dcffd277d32a8d9
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/16/2021
ms.locfileid: "5909035"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a><span data-ttu-id="e18fe-103">Setja upp kennslu fyrir Regression Suite Automation Tool</span><span class="sxs-lookup"><span data-stu-id="e18fe-103">Set up and install Regression suite automation tool tutorial</span></span>

<span data-ttu-id="e18fe-104">Þetta efnisatriði er kennsla sem hjálpar þér að fá skipulag og byrja með RSAT og verkfærin sem tengjast því að nota RSAT.</span><span class="sxs-lookup"><span data-stu-id="e18fe-104">This topic is a tutorial that helps you get setup and get started with RSAT and the tools associated with using RSAT.</span></span>

[!include [banner](../../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="e18fe-105">Notaðu verkfæri þín í internetvafranum til að sækja niður og vista þessa síðu á PDF-sniði.</span><span class="sxs-lookup"><span data-stu-id="e18fe-105">Use your internet browser tools to download and save this page in PDF format.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="e18fe-106">Lykilhugtök</span><span class="sxs-lookup"><span data-stu-id="e18fe-106">Key concepts</span></span>

- <span data-ttu-id="e18fe-107">Kynntu þér uppsetningu og forsendur sem þarf fyrir þau mismunandi forrit sem styðja Regression Suite Automation Tool (RSAT).</span><span class="sxs-lookup"><span data-stu-id="e18fe-107">Understand the installation and prerequisite setup that are required for the various applications that support Regression suite automation tool (RSAT).</span></span>
- <span data-ttu-id="e18fe-108">Kynntu þér hvernig eiginleikinn verkskráning, ásamt Microsoft Dynamics Lifecycle Services (LCS) og Microsoft Azure DevOps, gerir þér kleift að stofna, skilgreina, keyra, rannsaka og tilkynna um prófunaratriði.</span><span class="sxs-lookup"><span data-stu-id="e18fe-108">Understand how the Task recorder feature, together with Microsoft Dynamics Lifecycle Services (LCS) and Microsoft Azure DevOps, let you create, configure, run, investigate, and report on test cases.</span></span>
- <span data-ttu-id="e18fe-109">Styrktu starfandi notendur til að skrá viðskiptaverkefni með því að nota verkskráningu og breyttu síðan verkskráningunum í pakka með sjálfvirkum prófum, án þess að þurfa að skrifa frumkóða.</span><span class="sxs-lookup"><span data-stu-id="e18fe-109">Empower functional users to record business tasks by using Task recorder, and then convert the task recordings into a suite of automated tests, without having to write source code.</span></span>

## <a name="before-you-begin"></a><span data-ttu-id="e18fe-110">Áður en hafist er handa</span><span class="sxs-lookup"><span data-stu-id="e18fe-110">Before you begin</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e18fe-111">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="e18fe-111">Prerequisites</span></span>

- <span data-ttu-id="e18fe-112">Umhverfi sem keyrir Microsoft Dynamics 365 for Finance and Operations útgáfu 10.0 (apríl, 2019) eða síðar fyrir þetta kennsluefni.</span><span class="sxs-lookup"><span data-stu-id="e18fe-112">An environment that runs Microsoft Dynamics 365 for Finance and Operations version 10.0 (April 2019) or later is required for this tutorial.</span></span> <span data-ttu-id="e18fe-113">Fyrir viðskiptavini sem eru að nota Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3 er verkvangsuppfærsla 20 (PU20) eða nýrri einnig studd.</span><span class="sxs-lookup"><span data-stu-id="e18fe-113">For customers who are using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3, Platform update 20 (PU20) or later is also supported.</span></span>
- <span data-ttu-id="e18fe-114">Notandinn verður að hafa stjórnandaréttindi á umhverfið.</span><span class="sxs-lookup"><span data-stu-id="e18fe-114">The user must have admin rights to the environment.</span></span>
- <span data-ttu-id="e18fe-115">Þú verður að hafa aðgang að leigjanda viðskiptavinar í LCS og Azure DevOps (áður þekkt sem Microsoft Visual Studio Team Services \[VSTS\]).</span><span class="sxs-lookup"><span data-stu-id="e18fe-115">You must have access to the customer tenant LCS and Azure DevOps (previously known as Microsoft Visual Studio Team Services \[VSTS\]).</span></span>
- <span data-ttu-id="e18fe-116">Notandinn sem er að stofna og stjórna prófunarpökkum verður að hafa Azure DevOps prófunaráætlanir eða prófunarstjóraleyfi.</span><span class="sxs-lookup"><span data-stu-id="e18fe-116">The user that is creating and managing tests suites must have an Azure DevOps Test Plans or Test Manager license.</span></span> <span data-ttu-id="e18fe-117">Eftirfarandi heimildir veita þér einnig aðgang að prófunaráætlunum:</span><span class="sxs-lookup"><span data-stu-id="e18fe-117">The following licenses will also give you access to Test Plans:</span></span>
    - <span data-ttu-id="e18fe-118">Visual Studio Enterprise-leyfi</span><span class="sxs-lookup"><span data-stu-id="e18fe-118">Visual Studio Enterprise license</span></span>
    - <span data-ttu-id="e18fe-119">Visual Studio Test Professional-leyfi</span><span class="sxs-lookup"><span data-stu-id="e18fe-119">Visual Studio Test Professional license</span></span>
    - <span data-ttu-id="e18fe-120">MSDN Platforms-áskrifandaleyfi</span><span class="sxs-lookup"><span data-stu-id="e18fe-120">MSDN Platforms subscriber license</span></span>
- <span data-ttu-id="e18fe-121">RSAT verður að hafa aðgang að prófunarumhverfi í gegnum vafra.</span><span class="sxs-lookup"><span data-stu-id="e18fe-121">RSAT must have access to the test environment via a web browser.</span></span>
- <span data-ttu-id="e18fe-122">Til að mynda og breyta prófunarbreytum verður þú að vera með Microsoft Excel uppsett.</span><span class="sxs-lookup"><span data-stu-id="e18fe-122">To generate and edit test parameters, you must have Microsoft Excel installed.</span></span>

## <a name="configure-azure-devops"></a><span data-ttu-id="e18fe-123">Skilgreina Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="e18fe-123">Configure Azure DevOps</span></span>

### <a name="user-eligibility"></a><span data-ttu-id="e18fe-124">Hæfni notanda</span><span class="sxs-lookup"><span data-stu-id="e18fe-124">User eligibility</span></span>

<span data-ttu-id="e18fe-125">Gakktu úr skugga um að notandinn sé stofnaður í Azure DevOps og hafi áskriftarstig sem veitir aðgang að prófunaráætlunum í Azure.</span><span class="sxs-lookup"><span data-stu-id="e18fe-125">Make sure that the user is created in Azure DevOps and has a subscription level that provides access to Azure Test Plans.</span></span> <span data-ttu-id="e18fe-126">Leyfis fyrir prófunaráætlanir Azure DevOps er aðeins krafist ef notandinn mun stofna og stjórna prófunartilvikum (þ.e.a.s., ekki allir RSAT-notendur þurfa þetta leyfi).</span><span class="sxs-lookup"><span data-stu-id="e18fe-126">An Azure DevOps Test Plans license is required only if the user will create and manage test cases (that is, not all RSAT users require this license).</span></span> <span data-ttu-id="e18fe-127">Upplýsingar um leyfiskröfur er að finna í [Leyfisskilyrði](/azure/devops/test/manual-test-permissions#license-requirements).</span><span class="sxs-lookup"><span data-stu-id="e18fe-127">For information about the license requirements, see [License requirements](/azure/devops/test/manual-test-permissions#license-requirements).</span></span>

### <a name="create-a-new-azure-devops-project"></a><span data-ttu-id="e18fe-128">Stofna nýtt Azure DevOps-verk</span><span class="sxs-lookup"><span data-stu-id="e18fe-128">Create a new Azure DevOps project</span></span>

<span data-ttu-id="e18fe-129">RSAT notar Azure Devops fyrir prófunartilvikið og stjórnun prófunarpakkans, skýrslugerð og könnun á niðurstöðum prófanakeyrslna.</span><span class="sxs-lookup"><span data-stu-id="e18fe-129">RSAT uses Azure Devops for test case and test suite management, reporting, and investigating test run results.</span></span>

> [!NOTE]
> <span data-ttu-id="e18fe-130">Þú getur notað núverandi Azure DevOps-verk.</span><span class="sxs-lookup"><span data-stu-id="e18fe-130">You can use an existing Azure DevOps project.</span></span> <span data-ttu-id="e18fe-131">En ef núverandi Azure DevOps-verkið er sett upp þannig að það hafi sérsniðið sniðmát muntu fá villuna „VSTS-samstillingarvillu“ þegar þú samstillir prófunartilvik frá Viðskiptaferlavinnslu (BPM) til Azure DevOps (sjá kaflann [Prófa samstillingu frá BPM til Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops)).</span><span class="sxs-lookup"><span data-stu-id="e18fe-131">However, if your existing Azure DevOps project is set up so that it has a custom template, you will receive a "VSTS Sync Failure" error when you sync test cases from Business process modeler (BPM) to Azure DevOps (see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section).</span></span> <span data-ttu-id="e18fe-132">Ef eftirfarandi bestu venjur hefur verið fylgt fyrir sérsniðið sniðmát, munt þú geta samstillt prófunardæmin við Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="e18fe-132">If the following best practices have been followed for the custom template, you will be able to sync the test cases to Azure DevOps.</span></span> <span data-ttu-id="e18fe-133">(Þessar bestu venjur eru skráðar í villuboðunum.)</span><span class="sxs-lookup"><span data-stu-id="e18fe-133">(These best practices are listed in the error message.)</span></span>

- <span data-ttu-id="e18fe-134">Ekki eyða neinum gerðum vinnuliða eða tilbúnum reitum.</span><span class="sxs-lookup"><span data-stu-id="e18fe-134">Do not delete any work item types or out-of-the-box fields.</span></span>
- <span data-ttu-id="e18fe-135">Ekki eyða neinni stöðu í gerð vinnuliðar.</span><span class="sxs-lookup"><span data-stu-id="e18fe-135">Do not delete any state of a work item type.</span></span>
- <span data-ttu-id="e18fe-136">Ekki bæta neinum skyldusvæðum við gerð vinnuliðar.</span><span class="sxs-lookup"><span data-stu-id="e18fe-136">Do not add any required fields to a work item type.</span></span>

![Villuboð með lista yfir bestu starfsvenjur](./media/setup_rsa_tool_02.png)

<span data-ttu-id="e18fe-138">Að öðrum kosti mælum við með því að þú stofnir nýtt Azure DevOps-verk fyrir þetta kennsluefni.</span><span class="sxs-lookup"><span data-stu-id="e18fe-138">Otherwise, for this tutorial, we recommend that you create a new Azure DevOps project.</span></span> <span data-ttu-id="e18fe-139">Nánari upplýsingar er að finna í [Vandamál við samstillingu við BPM með sérsniðnu Azure DevOps (VSTS) ferlissniði](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span><span class="sxs-lookup"><span data-stu-id="e18fe-139">For more information, see [Issues when syncing to BPM using a custom Azure DevOps (VSTS) process template](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).</span></span>

1. <span data-ttu-id="e18fe-140">Opnaðu Azure DevOps-slóðina (`https://dev.azure.com/<Azure DevOps Name>`).</span><span class="sxs-lookup"><span data-stu-id="e18fe-140">Open the Azure DevOps URL (`https://dev.azure.com/<Azure DevOps Name>`).</span></span>
2. <span data-ttu-id="e18fe-141">Veldu **Stofna verk** efst í hægra horninu á síðunni Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="e18fe-141">Select **Create project** in the upper-right corner of the Azure DevOps page.</span></span>

    ![Stofna verkhnapp](./media/setup_rsa_tool_03.png)

3. <span data-ttu-id="e18fe-143">Fylltu út í eftirfarandi reiti og veldu síðan **Stofna**:</span><span class="sxs-lookup"><span data-stu-id="e18fe-143">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="e18fe-144">**Verknafn**</span><span class="sxs-lookup"><span data-stu-id="e18fe-144">**Project name**</span></span>
    - <span data-ttu-id="e18fe-145">**Útgáfustjórnun** - Veldu **Team Foundation útgáfustjórnun**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-145">**Version control** – Select **Team Foundation Version Control**.</span></span> <span data-ttu-id="e18fe-146">Athugaðu að sjálfgefinn valkostur, **Git**, er ekki studdur.</span><span class="sxs-lookup"><span data-stu-id="e18fe-146">Note that the default option, **Git**, isn't supported.</span></span>
    - <span data-ttu-id="e18fe-147">**Ferli vinnuliða**</span><span class="sxs-lookup"><span data-stu-id="e18fe-147">**Work item process**</span></span>

    ![Stofnaðu nýjan svarglugga verks](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a><span data-ttu-id="e18fe-149">Stofna aðgangsmerki notanda</span><span class="sxs-lookup"><span data-stu-id="e18fe-149">Create a personal access token</span></span>

<span data-ttu-id="e18fe-150">Í þessu kennsluefni notar þú LCS Viðskiptaferlavinnslu (BPM) til að búa til prófunarsafn og samstilla prófunaratriði þín við Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="e18fe-150">In this tutorial, you will use the LCS Business Process Modeler (BPM) to create a test case library and synchronize your test cases with Azure DevOps.</span></span> <span data-ttu-id="e18fe-151">Þú þarft aðgangsmerki notanda til að samstilla BPM við Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="e18fe-151">You will need a personal access token to sync BPM with Azure DevOps.</span></span>

1. <span data-ttu-id="e18fe-152">Veldu notandasíðutáknið efst í hægra horni síðunnar fyrir Azure DevOps verkið og veldu síðan **Öryggi**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-152">Select the profile icon in the upper-right corner of the page for your Azure DevOps project, and then select **Security**.</span></span>

    ![Öryggisskipun](./media/setup_rsa_tool_05.png)

2. <span data-ttu-id="e18fe-154">Í vinstri glugganum, undir **Öryggi** velurðu **Aðgangsmerki notanda**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-154">In the left pane, under **Security**, select **Personal access tokens**.</span></span> <span data-ttu-id="e18fe-155">Veldu síðan **Nýtt tákn**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-155">Then select **New Token**.</span></span>

    ![Hnappurinn Nýtt tákn á flipanum Aðgangsmerki í Notendastillingum](./media/setup_rsa_tool_06.png)

3. <span data-ttu-id="e18fe-157">Fylltu út í eftirfarandi reiti og veldu síðan **Stofna**:</span><span class="sxs-lookup"><span data-stu-id="e18fe-157">Fill in the following fields, and then select **Create**:</span></span>

    - <span data-ttu-id="e18fe-158">**Nafn**</span><span class="sxs-lookup"><span data-stu-id="e18fe-158">**Name**</span></span>
    - <span data-ttu-id="e18fe-159">**Gildistími (UTC)** – Veldu **Sérskilgreint** og notaðu síðan dagsetningavalið til að velja síðustu tiltæku dags.</span><span class="sxs-lookup"><span data-stu-id="e18fe-159">**Expiration (UTC)** – Select **Custom defined**, and then use the date picker to select the last available date.</span></span>
    - <span data-ttu-id="e18fe-160">**Umfang** - Veldu valkostinn **Ótakmarkaður aðgangur**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-160">**Scopes** – Select the **Full access** option.</span></span>

    ![Stofnaðu nýjan svarglugga aðgangsmerkis notanda](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > <span data-ttu-id="e18fe-162">Skráðu niður aðgangsmerkið sem er stofnað.</span><span class="sxs-lookup"><span data-stu-id="e18fe-162">Make a note of the personal access token that is created.</span></span> <span data-ttu-id="e18fe-163">Þú þarft það síðar þegar þú setur upp RSAT-skilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="e18fe-163">You will need it later when you set up the RSAT configuration.</span></span>

    ![Aðgangsmerki notanda](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a><span data-ttu-id="e18fe-165">Skilgreina LCS-verk</span><span class="sxs-lookup"><span data-stu-id="e18fe-165">Configure the LCS project</span></span>

<span data-ttu-id="e18fe-166">Þú þarft Lifecycle Services (LCS)-verkefni fyrir aðalprófunarsafnið þitt.</span><span class="sxs-lookup"><span data-stu-id="e18fe-166">You need a Lifecycle Services (LCS) project for your master test library.</span></span> <span data-ttu-id="e18fe-167">LCS Viðskiptaferlavinnsla (BPM) er notuð sem aðalsafn fyrir prófunardæmin þín.</span><span class="sxs-lookup"><span data-stu-id="e18fe-167">The LCS Business Process Modeler (BPM) is used as the master library for your test cases.</span></span> <span data-ttu-id="e18fe-168">BPM er notað til að stjórna og dreifa prófunarsöfnum yfir LCS-verk.</span><span class="sxs-lookup"><span data-stu-id="e18fe-168">BPM is used to manage and distribute test libraries across LCS projects.</span></span> <span data-ttu-id="e18fe-169">Til dæmis mun Microsoft-samstarfsaðili eða sjálfstæður smásali hugbúnaðar (ISV) sem er að byggja prófunarsöfn gefa út prófunardæmi á formi BPM-safna.</span><span class="sxs-lookup"><span data-stu-id="e18fe-169">For example, a Microsoft partner or independent software vendor (ISV) building test libraries will release test cases in the form of BPM libraries.</span></span> <span data-ttu-id="e18fe-170">Í BPM eru prófunardæmin skipulögð af viðskiptaferli.</span><span class="sxs-lookup"><span data-stu-id="e18fe-170">In BPM, test cases are organized by business process.</span></span> <span data-ttu-id="e18fe-171">BPM skilgreinir ekki framkvæmdaröð eða -tíðni staðinna prófana.</span><span class="sxs-lookup"><span data-stu-id="e18fe-171">BPM doesn't define the execution order or frequency of your test pass.</span></span> <span data-ttu-id="e18fe-172">Þessum aðgerðum er stjórnað í Azure DevOps, eins og er lýst síðar í þessu efnisatriði.</span><span class="sxs-lookup"><span data-stu-id="e18fe-172">These details are managed in Azure DevOps, as described later in this topic.</span></span>  

<span data-ttu-id="e18fe-173">Fyrir LCS-verkefnið er hægt að nota núverandi innleiðingu viðskiptavina eða samstarfsverkefni.</span><span class="sxs-lookup"><span data-stu-id="e18fe-173">For your LCS project, you can use an existing customer implementation or partner project.</span></span>

### <a name="update-the-lcs-language"></a><span data-ttu-id="e18fe-174">Uppfæra LCS-tungumál</span><span class="sxs-lookup"><span data-stu-id="e18fe-174">Update the LCS language</span></span>

> [!NOTE]
> <span data-ttu-id="e18fe-175">Svo að notendaviðmótið (UI) geti sýnt viðskiptaferli á réttan hátt verður valið tungumál LCS að vera stillt á **Enska (Bandaríkin)**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-175">For the user interface (UI) to correctly show business processes, the LCS preferred language must be set to **English (United States)**.</span></span>

1. <span data-ttu-id="e18fe-176">Farðu í LCS-innleiðingarverk.</span><span class="sxs-lookup"><span data-stu-id="e18fe-176">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="e18fe-177">Veldu hnappinn **Stillingar** (gírtáknið) efst í hægra horni síðunnar og veldu síðan **Tungumálaval**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-177">Select the **Settings** button (the gear symbol) in the upper-right corner, and then select **Language preference**.</span></span>

    ![Uppfæra stillingar tungumáls](./media/setup_rsa_tool_09.png)

3. <span data-ttu-id="e18fe-179">Í reitnum **Valið tungumál** velurðu **Enska (Bandaríkin)** og síðan velurðu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-179">In the **Preferred language** field, select **English (United States)**, and then select **Save**.</span></span>

    ![Flipinn Tungumálaval í Notendastillingum](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a><span data-ttu-id="e18fe-181">Skilgreina LCS til að tengjast við Azure DevOps-verk</span><span class="sxs-lookup"><span data-stu-id="e18fe-181">Configure LCS to connect to the Azure DevOps project</span></span>

<span data-ttu-id="e18fe-182">Ef þú stofnaðir nýtt Azure DevOps-verk áður skaltu skilgreina LCS-verkið þannig að það tengist því.</span><span class="sxs-lookup"><span data-stu-id="e18fe-182">If you created a new Azure DevOps project earlier, configure the LCS project to connect to it.</span></span> <span data-ttu-id="e18fe-183">Að öðrum kosti geturðu haldið áfram í næsta kafla, ef LCS-verkið þitt er þegar tengt við Azure DevOps-verkið.</span><span class="sxs-lookup"><span data-stu-id="e18fe-183">Otherwise, if your LCS project is already connected to your Azure DevOps project, you can continue to the next section.</span></span>

1. <span data-ttu-id="e18fe-184">Farðu í LCS-innleiðingarverk.</span><span class="sxs-lookup"><span data-stu-id="e18fe-184">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="e18fe-185">Veldu hnappinn **Valmynd** og veldu síðan **Verkefnisstillingar**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-185">Select the **Menu** button, and then select **Project settings**.</span></span>

    ![Skipun fyrir verkstillingar](./media/setup_rsa_tool_11.png)

3. <span data-ttu-id="e18fe-187">Í vinstri glugganum skaltu velja **Visual Studio Team Services** og síðan **Setja upp Visual Studio Team Services**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-187">In the left pane, select **Visual Studio Team Services**, and then select **Setup Visual Studio Team Services**.</span></span>

    ![Flipinn Visual Studio Team Services í verkstillingum](./media/setup_rsa_tool_12.png)

4. <span data-ttu-id="e18fe-189">Í reitnum **Azure DevOps vefslóð vefsvæðis** skaltu slá inn slóðina að vefsvæði Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="e18fe-189">In the **Azure DevOps site URL** field, enter the URL of the Azure DevOps site.</span></span> <span data-ttu-id="e18fe-190">Í reitnum **Aðgangsmerki notanda** skaltu slá inn aðgangsmerki notanda sem var stofnað áður.</span><span class="sxs-lookup"><span data-stu-id="e18fe-190">In the **Personal access token** field, enter the personal access token that was created earlier.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e18fe-191">Þótt VSTS sé núna þekkt sem Azure DevOps skaltu nota gömlu vefslóðina til að tengja LCS við Azure DevOps-verkið.</span><span class="sxs-lookup"><span data-stu-id="e18fe-191">Although VSTS is now known as Azure DevOps, to connect LCS to your Azure DevOps project, use the old URL.</span></span> <span data-ttu-id="e18fe-192">Til dæmis er Azure DevOps-vefslóðin sem er notuð í þessu kennsluatriði `https://dev.azure.com/D365FOFastTrack/`.</span><span class="sxs-lookup"><span data-stu-id="e18fe-192">For example, the Azure DevOps URL that is used in this tutorial is `https://dev.azure.com/D365FOFastTrack/`.</span></span> <span data-ttu-id="e18fe-193">En í eftirfarandi skýringarmynd er hún slegin inn sem `https://D365FOFastTrack.visualstudio.com/`.</span><span class="sxs-lookup"><span data-stu-id="e18fe-193">However, in the following illustration, it's entered as `https://D365FOFastTrack.visualstudio.com/`.</span></span>

    ![Skref 1 í uppsetningu á Visual Studio Team Services](./media/setup_rsa_tool_13.png)

5. <span data-ttu-id="e18fe-195">Veldu **Haltu áfram**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-195">Select **Continue**.</span></span>
6. <span data-ttu-id="e18fe-196">Í reitnum **Visual Studio Team Services-verk** velurðu VSTS-verk á valinni vefslóð til að tengja við LCS-verkið.</span><span class="sxs-lookup"><span data-stu-id="e18fe-196">In the **Visual Studio Team Services project** field, select the VSTS project on the selected site to link with the LCS project.</span></span> <span data-ttu-id="e18fe-197">Reiturinn **Vinna úr sniðmáti** er sjálfgefið stilltur á **Agile**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-197">The **Process template** field is set to **Agile** by default.</span></span> <span data-ttu-id="e18fe-198">Fyrir sérsniðið sniðmát skaltu fara yfir leiðbeiningar á bestu venjum í kaflanum [Stofna nýtt Azure DevOps-verk](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="e18fe-198">For a custom template, review the best practice guidance in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span> <span data-ttu-id="e18fe-199">Veldu síðan **Halda áfram**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-199">Then select **Continue**.</span></span>

    ![Skref 2 í uppsetningu á Visual Studio Team Services](./media/setup_rsa_tool_14.png)

7. <span data-ttu-id="e18fe-201">Farðu yfir stillingar þínar og veldu síðan **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-201">Review your settings, and then select **Save**.</span></span>

    ![Skref 3 í uppsetningu á Visual Studio Team Services](./media/setup_rsa_tool_15.png)

8. <span data-ttu-id="e18fe-203">Veldu **Heimila** til að heimila LCS að aðgang að skilgreindu svæði Azure DevOps fyrir þína hönd og til að kveikja á eiginleikum sem samþættast VSTS.</span><span class="sxs-lookup"><span data-stu-id="e18fe-203">Select **Authorize** to authorize LCS to access the configured Azure DevOps site on your behalf and to turn on features that integrate with VSTS.</span></span>

    ![Hnappurinn Heimila](./media/setup_rsa_tool_16.png)

9. <span data-ttu-id="e18fe-205">Skilaboðagluggi birtist og þar stendur, „Þér verður beint yfir á ytra svæði til að heimila LCS að tengja við Visual Studio Team Services fyrir hönd notanda.</span><span class="sxs-lookup"><span data-stu-id="e18fe-205">A message box appears that states, "You are about to be redirected to an eternal site to authorize LCS to connect to Visual Studio Team Services on your behalf.</span></span> <span data-ttu-id="e18fe-206">Á að halda áfram?“</span><span class="sxs-lookup"><span data-stu-id="e18fe-206">Proceed?"</span></span> <span data-ttu-id="e18fe-207">Velja skal **Já**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-207">Select **Yes**.</span></span>

    ![Skilaboðagluggi](./media/setup_rsa_tool_17.png)

10. <span data-ttu-id="e18fe-209">Veljið **Samþykkja**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-209">Select **Accept**.</span></span>

    ![Heimila aðgang](./media/setup_rsa_tool_18.png)

11. <span data-ttu-id="e18fe-211">Ef þú ert hefur heimild sem notandi ættir notandaviðmótið að skila þér aftur á síðuna LCS-verkefnastillingar.</span><span class="sxs-lookup"><span data-stu-id="e18fe-211">If you're authorized as a user, the UI should you return to the LCS project settings page.</span></span>

    ![Heimilaður notandi](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a><span data-ttu-id="e18fe-213">Stofna nýtt BPM-safn</span><span class="sxs-lookup"><span data-stu-id="e18fe-213">Create a new BPM library</span></span>

1. <span data-ttu-id="e18fe-214">Farðu í LCS-innleiðingarverk.</span><span class="sxs-lookup"><span data-stu-id="e18fe-214">Go to the LCS implementation project.</span></span>
2. <span data-ttu-id="e18fe-215">Veldu hnappinn **Valmynd** og veldu síðan **Viðskiptaferlavinnsla**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-215">Select the **Menu** button, and then select **Business process modeler**.</span></span>

    ![Skipun Viðskiptaferlavinnslu](./media/setup_rsa_tool_20.png)

3. <span data-ttu-id="e18fe-217">Veldu **Nýtt safn**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-217">Select **New library**.</span></span>

    ![Hnappurinn Nýtt safn](./media/setup_rsa_tool_21.png)

4. <span data-ttu-id="e18fe-219">Í reitnum **Heiti safns** slærðu inn heiti og velur síðan **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-219">In the **Library name** field, enter a name, and then select **Create**.</span></span> <span data-ttu-id="e18fe-220">Fyrir þetta kennsluefni skaltu nefna BPM-safnið **RSAT**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-220">For this tutorial, name the BPM library **RSAT**.</span></span>

    ![Stofnaðu nýjan svarglugga safns](./media/setup_rsa_tool_22.png)

5. <span data-ttu-id="e18fe-222">Opnaðu nýtt **RSAT** BPM-safn.</span><span class="sxs-lookup"><span data-stu-id="e18fe-222">Open the new **RSAT** BPM library.</span></span>
6. <span data-ttu-id="e18fe-223">Veldu ferlið **Sýnisviðskiptaferli** og síðan velurðu til hægri **Breyta ham**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-223">Select the **Sample Core Business Process** process, and then, on the right, select **Edit mode**.</span></span>

    ![Hnappurinn Breyta ham](./media/setup_rsa_tool_23.png)

7. <span data-ttu-id="e18fe-225">Breyttu gildi bæði reitarins **Heiti** og reitarins **Lýsing** í **Stofna afurð**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-225">Change the value of both the **Name** field and the **Description** field to **Create a product**.</span></span> <span data-ttu-id="e18fe-226">Veldu síðan **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-226">Then select **Save**.</span></span>

    ![Reitirnir Heiti og Lýsing](./media/setup_rsa_tool_24.png)

## <a name="environment"></a><span data-ttu-id="e18fe-228">Umhverfi</span><span class="sxs-lookup"><span data-stu-id="e18fe-228">Environment</span></span>

### <a name="version-requirement"></a><span data-ttu-id="e18fe-229">Þörf skv. útgáfu</span><span class="sxs-lookup"><span data-stu-id="e18fe-229">Version requirement</span></span>

<span data-ttu-id="e18fe-230">Prófunar- eða sandkassaumhverfis sem keyrir útgáfu 10 er krafist.</span><span class="sxs-lookup"><span data-stu-id="e18fe-230">A test or sandbox environment that runs version 10 is required.</span></span> <span data-ttu-id="e18fe-231">Fyrir viðskiptavini sem eru að nota útgáfu 7.3 er verkvangsuppfærsla 20 eða nýrri einnig studd.</span><span class="sxs-lookup"><span data-stu-id="e18fe-231">For customers that are using version 7.3, Platform update 20 or later is also supported.</span></span>

> [!NOTE]
> <span data-ttu-id="e18fe-232">RSAT verður að hafa aðgang að prófunarumhverfinu í gegnum vafra.</span><span class="sxs-lookup"><span data-stu-id="e18fe-232">RSAT must have access to your test environment via a web browser.</span></span>

### <a name="user-criteria"></a><span data-ttu-id="e18fe-233">Notandaskilyrði</span><span class="sxs-lookup"><span data-stu-id="e18fe-233">User criteria</span></span>

<span data-ttu-id="e18fe-234">Notandinn verður að hafa stjórnandaréttindi á þessu umhverfi.</span><span class="sxs-lookup"><span data-stu-id="e18fe-234">The user must have admin rights to this environment.</span></span>

### <a name="set-up-help-settings-to-connect-with-lcs"></a><span data-ttu-id="e18fe-235">Stilltu hjálparstillingar til að tengjast LCS</span><span class="sxs-lookup"><span data-stu-id="e18fe-235">Set up Help settings to connect with LCS</span></span>

<span data-ttu-id="e18fe-236">Þetta skref er nauðsynlegt til að tengjast LCS þannig að hægt sé að vista verkskráningu í viðeigandi BPM-safn í LCS í gegnum biðlarann.</span><span class="sxs-lookup"><span data-stu-id="e18fe-236">This step is required in order to connect with LCS so that task recordings can be saved to the appropriate BPM library in LCS through the client.</span></span>

1. <span data-ttu-id="e18fe-237">Opna á biðlarann.</span><span class="sxs-lookup"><span data-stu-id="e18fe-237">Open the client.</span></span>
2. <span data-ttu-id="e18fe-238">Farðu í **Kerfisstjórnun \> Uppsetning \> Kerfisfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-238">Go to **System Administration \> Setup \> System parameters**.</span></span>
3. <span data-ttu-id="e18fe-239">Á flipanum **Hjálp**, í reitnum **Hjálparskilgreiningar Lifecycle Services** velurðu viðkomandi LCS-verk (**RSAT** fyrir þetta kennsluefni).</span><span class="sxs-lookup"><span data-stu-id="e18fe-239">On the **Help** tab, in the **Lifecycle Services help configuration** field, select the relevant LCS project (**RSAT** for this tutorial).</span></span>

    ![Reiturinn Hjálparskilgreiningar Lifecycle Services á flipanum Hjálp](./media/setup_rsa_tool_25.png)

    <span data-ttu-id="e18fe-241">BPM-söfn eru fyllt út undir viðeigandi LCS-verki.</span><span class="sxs-lookup"><span data-stu-id="e18fe-241">BPM libraries are filled in under the appropriate LCS project.</span></span>

4. <span data-ttu-id="e18fe-242">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-242">Select **Save**.</span></span>
5. <span data-ttu-id="e18fe-243">Þú gætir þurft að endurræsa vafrann til að sjá uppfært hjálparefni.</span><span class="sxs-lookup"><span data-stu-id="e18fe-243">You might have to refresh the browser to see the updated Help content.</span></span>

    ![Tilkynning um að endurræsingu á vafranum](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a><span data-ttu-id="e18fe-245">Verkskráning</span><span class="sxs-lookup"><span data-stu-id="e18fe-245">Task recordings</span></span>

> [!NOTE]
> <span data-ttu-id="e18fe-246">Gakktu úr skugga um að allar verkskráningar þínar hefjist aðalyfirlitinu.</span><span class="sxs-lookup"><span data-stu-id="e18fe-246">Make sure that all your task recordings start on the main dashboard.</span></span> <span data-ttu-id="e18fe-247">Haltu stökum skráningum stuttum og leggðu áherslu á eitt viðskiptaverk, eins og að stofna sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="e18fe-247">Keep individual recordings short, and focus on one business task, such as creating a sales order.</span></span>

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a><span data-ttu-id="e18fe-248">Stofnaðu verkskráningu og vistaðu hana í BPM-safnið</span><span class="sxs-lookup"><span data-stu-id="e18fe-248">Create a task recording and save it to the BPM library</span></span>

<span data-ttu-id="e18fe-249">Stofnaðu samsvarandi verkskráningu sem hægt er að festa við hið einfaldaða viðskiptaferli sem var stofnað í nýja BPM-safninu.</span><span class="sxs-lookup"><span data-stu-id="e18fe-249">Create a corresponding task recording that you can attach to the simple business process that was created in the new BPM library.</span></span>

1. <span data-ttu-id="e18fe-250">Opna á biðlarann.</span><span class="sxs-lookup"><span data-stu-id="e18fe-250">Open the client.</span></span>
2. <span data-ttu-id="e18fe-251">Í aðalyfirlitinu skaltu velja hnappinn **Stillingar** (gírtáknið) og síðan **Verkskráningu**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-251">On the main dashboard, select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>

    ![Velja Verkskráningu á stillingavalmynd](./media/setup_rsa_tool_27.png)

3. <span data-ttu-id="e18fe-253">Veldu **Stofna skráningu**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-253">Select **Create recording**.</span></span>

    ![Hnappurinn Stofna skráningu](./media/setup_rsa_tool_28.png)

4. <span data-ttu-id="e18fe-255">Fylltu út reitina **Heiti skráningar** og **Lýsing skráningar** og veldu síðan **Ræsa**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-255">Fill in the **Recording name** and **Recording description** fields, and then select **Start**.</span></span>

    ![Reitirnir Heiti skráningar og Lýsing skráningar.](./media/setup_rsa_tool_29.png)

5. <span data-ttu-id="e18fe-257">Skráðu skrefin til að stofna afurð.</span><span class="sxs-lookup"><span data-stu-id="e18fe-257">Record the steps for creating a product.</span></span> <span data-ttu-id="e18fe-258">Þegar því er lokið skaltu velja **Hættu** til að stöðva skráningu.</span><span class="sxs-lookup"><span data-stu-id="e18fe-258">When you've finished, select **Stop** to stop recording.</span></span>

    ![Skref til að stofna afurð](./media/setup_rsa_tool_30.png)

6. <span data-ttu-id="e18fe-260">Veldu **Vista í Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-260">Select **Save to Lifecycle Services**.</span></span>

    ![Vista færsluskráningu í Lifecycle Services](./media/setup_rsa_tool_31.png)

    <span data-ttu-id="e18fe-262">Upplýsingar um söfn er hlaðið úr LCS.</span><span class="sxs-lookup"><span data-stu-id="e18fe-262">Library information is loaded from LCS.</span></span>

    ![Hleður safnupplýsingum](./media/setup_rsa_tool_32.png)

7. <span data-ttu-id="e18fe-264">Veldu BPM-safn til að tengja við verkskráninguna.</span><span class="sxs-lookup"><span data-stu-id="e18fe-264">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="e18fe-265">Fyrir þetta kennsluefni skaltu velja BPM-safnið **RSAT** sem var stofnað áður og síðan viðskiptaferlið **Stofna afurð** undir því.</span><span class="sxs-lookup"><span data-stu-id="e18fe-265">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Create a product** business process under it.</span></span> <span data-ttu-id="e18fe-266">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-266">Then select **OK**.</span></span>

    ![Tengja verkskráningu við BPM-safn og viðskiptaferli](./media/setup_rsa_tool_33.png)

    <span data-ttu-id="e18fe-268">Skilaboðin „Vistað í Lifecycle Services“ birtast.</span><span class="sxs-lookup"><span data-stu-id="e18fe-268">A "Saving to Lifecycle Services was successful" message appears.</span></span>

    ![Skilaboð um árangursríka vistun í LCS](./media/setup_rsa_tool_34.png)

8. <span data-ttu-id="e18fe-270">Ef þú vilt vista verkskráningu á staðnum og hlaða henni síðan inn í BPM í gegnum LCS skaltu fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="e18fe-270">If you want to save the task recording locally and then upload it to BPM through LCS, follow these steps:</span></span>

    1. <span data-ttu-id="e18fe-271">Þegar skáningu er lokið skaltu velja **Vista á þessa tölvu**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-271">After the recording is completed, select **Save to this PC**.</span></span>

        ![Vista í þessari tölvu](./media/setup_rsa_tool_35.png)

    2. <span data-ttu-id="e18fe-273">Í tilkynningastiku vafrans skaltu velja **Vista** eða **Vista sem** til að vista skrána staðbundið á tölvuna.</span><span class="sxs-lookup"><span data-stu-id="e18fe-273">In the browser's Notification bar, select **Save** or **Save As** to save the file on your local computer.</span></span>

        ![Tilkynningastika](./media/setup_rsa_tool_36.png)

    3. <span data-ttu-id="e18fe-275">Farðu í BPM-safnið **RSAT** og veldu viðskiptaferlið sem á að vista verkskráninguna gegn.</span><span class="sxs-lookup"><span data-stu-id="e18fe-275">Go to the **RSAT** BPM library, and select the business process to save the task recording against.</span></span>
    4. <span data-ttu-id="e18fe-276">Á flipanum **Yfirlit** velurðu **Hlaða upp**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-276">On the **Overview** tab, select **Upload**.</span></span>

        ![Hnappurinn Hlaða upp](./media/setup_rsa_tool_37.png)

    5. <span data-ttu-id="e18fe-278">Veldu **Fletta** og veldu .axtr skrána sem þú vistaðir áður.</span><span class="sxs-lookup"><span data-stu-id="e18fe-278">Select **Browse**, and select the .axtr file that you saved earlier.</span></span> <span data-ttu-id="e18fe-279">Veldu síðan **Hlaða upp**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-279">Then select **Upload**.</span></span>

        ![Veldu .axtr skrá til að hlaða upp](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a><span data-ttu-id="e18fe-281">Prófaðu samstillingu úr BPM við Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="e18fe-281">Test the synchronization from BPM to Azure DevOps</span></span>

<span data-ttu-id="e18fe-282">Núna þegar verkskráning er tengd viðskiptaferlinu verður þú að sannreyna að hægt sé að samstilla viðskiptaferlið og tengda verkskráningu við Azure DevOps sem eiginleika og prófunardæmi (í þessari röð) með því að nota VSTS-samstillingu í LCS.</span><span class="sxs-lookup"><span data-stu-id="e18fe-282">Now that a task recording is attached to the business process, you must validate that the business process and the associated task recording can be synced to Azure DevOps as a feature and a test case (respectively) by using the VSTS sync feature in LCS.</span></span>

> [!NOTE]
> <span data-ttu-id="e18fe-283">Samsvarandi gerð vinnuliðar sem er stofnaður í Azure DevOps verður breytileg eftir því ferlissniði sem þú valdir við skilgreiningu á LCS-verkinu með Azure DevOps, eins og lýst er í kaflanum [Stofna nýtt Azure DevOps-verk](#create-a-new-azure-devops-project).</span><span class="sxs-lookup"><span data-stu-id="e18fe-283">The corresponding work item type that is created in Azure DevOps will vary, depending on the process template that you selected when you configured the LCS project with Azure DevOps, as described in the [Create a new Azure DevOps project](#create-a-new-azure-devops-project) section.</span></span>

1. <span data-ttu-id="e18fe-284">Farðu í BPM-safnið og opnaðu **RSAT**-safnið sem var áður stofnað.</span><span class="sxs-lookup"><span data-stu-id="e18fe-284">Go to the BPM library, and open the **RSAT** library that you created earlier.</span></span>
2. <span data-ttu-id="e18fe-285">Veldu úrfellingarhnappinn (**...**) og veldu **VSTS-samstillingu**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-285">Select the ellipsis button (**...**), and select **VSTS sync**.</span></span>

    ![VSTS-samstillingarskipun í úrfellingarvalmyndinni](./media/setup_rsa_tool_39.png)

    <span data-ttu-id="e18fe-287">Eftir að VSTS-samstillingu er lokið birtist flipinn **Þarfir** vinstra megin og inniheldur samsvarandi Azure DevOps-vinnulið.</span><span class="sxs-lookup"><span data-stu-id="e18fe-287">After VSTS sync is completed, a **Requirements** tab appears on the left side and includes the corresponding Azure DevOps work item.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e18fe-288">Vinnuliðurinn sem er stofnaður í Azure DevOps mun hafa heiti BPM-safnsins sem titilforskeyti.</span><span class="sxs-lookup"><span data-stu-id="e18fe-288">The work item that is created in Azure DevOps will have the BPM library name as the title prefix.</span></span>

    ![Flipinn Þarfir](./media/setup_rsa_tool_40.png)

3. <span data-ttu-id="e18fe-290">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="e18fe-290">Refresh the page.</span></span>
4. <span data-ttu-id="e18fe-291">Veldu úrfellingarhnappinn (**...**). Þú munt sjá viðbótarvalkost, **Samstilla prófunartilvik**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-291">Select the ellipsis button (**...**). You will see an additional option, **Sync test cases**.</span></span> <span data-ttu-id="e18fe-292">Veldu þennan valkost.</span><span class="sxs-lookup"><span data-stu-id="e18fe-292">Select this option.</span></span>

    ![Dæmi um samstillingarskipun í úrfellingarvalmyndinni](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > <span data-ttu-id="e18fe-294">Ef valkosturinn **Samstilla prófunartilvik** er ekki tiltækur eftir að endurhleðslu síðunnar skaltu fara á heimasíðuna fyrir BPM og velja **Samstilla prófunartilvik** fyrir allt safnið.</span><span class="sxs-lookup"><span data-stu-id="e18fe-294">If the **Sync test cases** option isn't available after you refresh the page, go to main page for BPM, and select **Sync test cases** for the whole library itself.</span></span> <span data-ttu-id="e18fe-295">Þannig þvingar þú í raun samstillingu á allt safnið.</span><span class="sxs-lookup"><span data-stu-id="e18fe-295">In this way, you effectively force a synchronization for the whole library.</span></span>
    >
    > ![Valið Samstillt prófunardæmi fyrir allt safnið](./media/setup_rsa_tool_42.png)

    <span data-ttu-id="e18fe-297">Þegar samstillinu prófunardæma er lokið er nýtt prófunardæmi stofnað á flipanum **Þarfir**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-297">After Sync test cases is completed, a new test case is created on the **Requirements** tab.</span></span>

    ![Nýtt prófunardæmi á flipanum Þarfir](./media/setup_rsa_tool_43.png)

5. <span data-ttu-id="e18fe-299">Farðu í Azure DevOps-verkið og veldu **Spjöld \> Vinnuliðir**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-299">Go to your Azure DevOps project, and select **Boards \> Work Items**.</span></span>

    ![Vinnuliðaskipun undir Spjöldum](./media/setup_rsa_tool_44.png)

6. <span data-ttu-id="e18fe-301">Staðfestu að vinnuliðurinn og prófunardæmin sem þú voru stofnuð með BPM-samstillingu séu til.</span><span class="sxs-lookup"><span data-stu-id="e18fe-301">Validate that the work item and test case that you created through BPM synchronization exist.</span></span>

    ![Vinnuliður og prófunardæmi](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a><span data-ttu-id="e18fe-303">Setja upp og skilgreina RSAT</span><span class="sxs-lookup"><span data-stu-id="e18fe-303">Install and Configure RSAT</span></span>

<span data-ttu-id="e18fe-304">Hægt er að setja upp RSAT á allar tölvur sem keyra Windows 10 og geta tengst umhverfi í gegnum vafra (Internet Explorer eða Google Chrome).</span><span class="sxs-lookup"><span data-stu-id="e18fe-304">RSAT can be installed on any computer that runs Windows 10 and that can connect to the environment via a web browser (Internet Explorer or Google Chrome).</span></span>

> [!NOTE]
> <span data-ttu-id="e18fe-305">Við mælum með því að þú fjarlægir fyrri útgáfuna áður en þú setur upp nýja útgáfu af verkfærinu.</span><span class="sxs-lookup"><span data-stu-id="e18fe-305">Before you install a new version of the tool, we recommend that you uninstall the previous version.</span></span>

### <a name="install-an-authentication-certificate"></a><span data-ttu-id="e18fe-306">Settu upp sannvottunarvottorð</span><span class="sxs-lookup"><span data-stu-id="e18fe-306">Install an authentication certificate</span></span>

<span data-ttu-id="e18fe-307">Til að virkja sannvottun verðurðu að mynda og setja upp vottorð á sömu tölvu og RSAT keyrir á.</span><span class="sxs-lookup"><span data-stu-id="e18fe-307">To enable authentication, you must generate and install a certificate on the same computer that RSAT is running on.</span></span>

#### <a name="generate-a-certificate"></a><span data-ttu-id="e18fe-308">Mynda skírteini</span><span class="sxs-lookup"><span data-stu-id="e18fe-308">Generate a certificate</span></span>

1. <span data-ttu-id="e18fe-309">Til að mynda vottorðaskrá skaltu opna Microsoft Windows PowerShell-glugga sem stjórnandi og keyra eftirfarandi skipun.</span><span class="sxs-lookup"><span data-stu-id="e18fe-309">To generate a certificate file, open a Microsoft Windows PowerShell window as an admin, and run the following command.</span></span>

    ```powershell
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. <span data-ttu-id="e18fe-310">Opnaðu vottorðsstjóra með því að slá inn **certlm.msc** í svargluggann **Keyra** og staðfesta að vottorðið **D365 Sjálfvirkt prófunarvottorð** sé myndað undir **Persónulegt \> Vottorð**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-310">Open certificate manager by entering **certlm.msc** in the **Run** dialog box, and confirm that the **D365 Automated testing certificate** certificate is created under **Personal \> Certificates**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e18fe-311">Passaðu að slá inn **certlm.msc**, ekki **certmgr.msc**, vegna þess að vottorðin eru geymd á tölvunni þinni.</span><span class="sxs-lookup"><span data-stu-id="e18fe-311">Be sure to enter **certlm.msc**, not **certmgr.msc**, because the certificates are stored on the local computer.</span></span>

    ![D365 Sjálfvirkt vottorð prófunarvottorðs](./media/setup_rsa_tool_46.png)

3. <span data-ttu-id="e18fe-313">Hægri-smelltu á vottorðið og veldu síðan **Afrita**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-313">Right-click the certificate, and then select **Copy**.</span></span>
4. <span data-ttu-id="e18fe-314">Farðu í **Trusted Root Certification Authorities \> Vottorð**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-314">Go to **Trusted Root Certification Authorities \> Certificates**.</span></span>

    ![Vottorðamappa undir möppunni Trusted Root Certification Authorities](./media/setup_rsa_tool_47.png)

5. <span data-ttu-id="e18fe-316">Í valmyndinni **Aðgerð** velurðu **Líma** til að afrita vottorðið á staðsetninguna **Trusted Root Certification Authorities**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-316">On the **Action** menu, select **Paste** to copy the certificate to the **Trusted Root Certification Authorities** location.</span></span>

    ![Líma-skipun í aðgerðavalmyndinni](./media/setup_rsa_tool_48.png)

6. <span data-ttu-id="e18fe-318">Til að fá fingrafar af uppsettu vottorði, en án bila eða sérstafa, skaltu opna gluggann Windows PowerShell sem stjórnandi og keyra eftirfarandi skipanir.</span><span class="sxs-lookup"><span data-stu-id="e18fe-318">To get the thumbprint of the installed certificate, but without spaces or special characters, open a Windows PowerShell window as an admin, and run the following commands.</span></span>

    ```powershell
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > <span data-ttu-id="e18fe-319">Vistaðu fingrafarið því þú þarft það síðar þegar þú uppfærir .wif-skrárnar fyrir Application Object Server (AOS) og setur upp RSAT-stillingar.</span><span class="sxs-lookup"><span data-stu-id="e18fe-319">Save the thumbprint, because you will need it later when you update the .wif files for Application Object Server (AOS) and set up the RSAT configuration.</span></span>

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a><span data-ttu-id="e18fe-320">Skilgreina AOS-tölvuna til að treysta tengingunni</span><span class="sxs-lookup"><span data-stu-id="e18fe-320">Configure the AOS computer to trust the connection</span></span>

> [!NOTE]
> <span data-ttu-id="e18fe-321">Ef umhverfið er Lag 2+ verður fingrafar vottorðs að vera uppfært í wif.config skránni fyrir **allar** AOS-tölvur fyrir umhverfið.</span><span class="sxs-lookup"><span data-stu-id="e18fe-321">If the environment is a Tier 2+ environment, the certificate thumbprint must be updated in the wif.config file for **all** AOS computers for the environment.</span></span>

1. <span data-ttu-id="e18fe-322">Stofnaðu Remote Desktop Protocol (RDP)-tengingu við AOS-tölvuna.</span><span class="sxs-lookup"><span data-stu-id="e18fe-322">Establish a Remote Desktop Protocol (RDP) connection to the AOS computer.</span></span> <span data-ttu-id="e18fe-323">Skráningarupplýsingar eru tiltækar á umhverfisupplýsingasíðunni í LCS.</span><span class="sxs-lookup"><span data-stu-id="e18fe-323">Sign-in details are available on the environment details page in LCS.</span></span>
2. <span data-ttu-id="e18fe-324">Opnaðu Microsoft Internet Information Services (IIS) og finndu **AOSService** á listanum yfir vefsvæði.</span><span class="sxs-lookup"><span data-stu-id="e18fe-324">Open Microsoft Internet Information Services (IIS), and find **AOSService** in the list of sites.</span></span>

    ![AOSService á lista yfir vefsvæði](./media/setup_rsa_tool_49.png)

3. <span data-ttu-id="e18fe-326">Hægrismellið á **Skoða** til að opna möppuna **\<Drive\>: \\AosService\\WebRoot**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-326">Right-click **Explore** to open the **\<Drive\>: \\AosService\\WebRoot** folder.</span></span> <span data-ttu-id="e18fe-327">Finndu skrána **wif.config**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-327">Find the **wif.config** file.</span></span>

    ![Skráin Wif.config í möppunni WebRoot](./media/setup_rsa_tool_50.png)

4. <span data-ttu-id="e18fe-329">Uppfærðu skrána **wif.config** með því að bæta við nýrri heimildarfærslu fyrir vottorðið og heiti heimildar, eins og sýnt er í eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="e18fe-329">Update the **wif.config** file by adding a new authority entry for your certificate and authority name, as shown in the following example.</span></span>

    ```Xml
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > <span data-ttu-id="e18fe-330">Ef margir notendur eru að nota sama forritið verður hver notandi að búa til aðskild fingraför og bæta verður hverju fingrafari við **\<keys\>** hlutann.</span><span class="sxs-lookup"><span data-stu-id="e18fe-330">If multiple users are using the same application, each user must generate separate thumbprints, and each of those thumbprints must be added in the **\<keys\>** section.</span></span>

5. <span data-ttu-id="e18fe-331">Ef fleiri en ein AOS-tölva er til staðar skaltu endurtaka skref 3 til 4 fyrir hverja viðbótartölvu.</span><span class="sxs-lookup"><span data-stu-id="e18fe-331">If there is more than one AOS computer, repeat steps 3 through 4 for each additional computer.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e18fe-332">Ólíkt eldri umhverfum á lagi 2 er nýju umhverfi beitt á lagi 2 umhverfi með tveimur AOS-tilvikum.</span><span class="sxs-lookup"><span data-stu-id="e18fe-332">Unlike older Tier 2 environments, new Tier 2 environments are deployed with two AOS instances.</span></span>

6. <span data-ttu-id="e18fe-333">Hlaupa **iisreset** á öllum AOS-tölvum.</span><span class="sxs-lookup"><span data-stu-id="e18fe-333">Run **iisreset** on all the AOS computers.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e18fe-334">Ef þú hefur ekki stjórnandaréttindi til að keyra **iisreset** á tölvu á lagi 1 skaltu síðunni Umhverfisupplýsingar í LCS velja Viðhalda > Endurræsa þjónustu.</span><span class="sxs-lookup"><span data-stu-id="e18fe-334">If you don't have admin rights to run **iisreset** on a Tier 1 computer, on the Environment details page in LCS, select Maintain > Restart services.</span></span>

#### <a name="tier-2-environment"></a><span data-ttu-id="e18fe-335">Umhverfi lags 2+</span><span class="sxs-lookup"><span data-stu-id="e18fe-335">Tier 2+ environment</span></span>

<span data-ttu-id="e18fe-336">Ef notast er við umhverfi á lagi 2+ (Sandbox: stöðluð samþykktarprófun eða nýrra) skaltu staðfesta eða stilla eftirfarandi stýriskráarstillingar á tölvunni þar sem RSAT er sett upp.</span><span class="sxs-lookup"><span data-stu-id="e18fe-336">If a Tier 2+ (Standard Acceptance Test sandbox or higher) environment is used, verify or set the following registry setting on the computer where RSAT is installed.</span></span> <span data-ttu-id="e18fe-337">Þetta skref er nauðsynlegt vegna þess að það hjálpar þér að koma í veg fyrir villur í sannprófun eða RSAT-tengingu.</span><span class="sxs-lookup"><span data-stu-id="e18fe-337">This step is required because it helps you avoid authentication or RSAT connection errors.</span></span>

```PowerShell
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a><span data-ttu-id="e18fe-338">Setja upp RSAT</span><span class="sxs-lookup"><span data-stu-id="e18fe-338">Install RSAT</span></span>

1. <span data-ttu-id="e18fe-339">Farðu á <https://www.microsoft.com/download/details.aspx?id=57357> og veldu **Sækja**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-339">Go to <https://www.microsoft.com/download/details.aspx?id=57357>, and select **Download**.</span></span>
2. <span data-ttu-id="e18fe-340">Veldu allar skrárnar og veldu síðan **Næst**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-340">Select all the files, and then select **Next**.</span></span>

    ![Val á öllum skrám](./media/setup_rsa_tool_51.png)

3. <span data-ttu-id="e18fe-342">Tvísmelltu á .msi-pakkann til að keyra uppsetningarforritið.</span><span class="sxs-lookup"><span data-stu-id="e18fe-342">Double-click the .msi package to run the installer.</span></span> <span data-ttu-id="e18fe-343">Þegar uppsetningu er lokið skaltu síðan velja **Ljúka**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-343">Then, when the installation is completed, select **Finish**.</span></span>

    ![RSAT Installer-skrá](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a><span data-ttu-id="e18fe-345">Settu upp Selenium og vafradrif</span><span class="sxs-lookup"><span data-stu-id="e18fe-345">Install Selenium and browser drivers</span></span>

<span data-ttu-id="e18fe-346">Í eldri útgáfum af RSAT þurfti að setja upp Selenium og vafradrif.</span><span class="sxs-lookup"><span data-stu-id="e18fe-346">In older versions of RSAT, you had to install Selenium and browser drivers.</span></span> <span data-ttu-id="e18fe-347">Það þarf ekki lengur að setja upp þessi drif vegna þess að þau eru sjálfkrafa sett upp.</span><span class="sxs-lookup"><span data-stu-id="e18fe-347">You no longer have to install these drivers because they are automatically installed.</span></span>

1. <span data-ttu-id="e18fe-348">Í fyrsta skipti sem þú opnar RSAT færðu kvaðiningum um að sækja sjálfkrafa og setja Selenium upp.</span><span class="sxs-lookup"><span data-stu-id="e18fe-348">The first time that you open RSAT, you're prompted to automatically download and install Selenium.</span></span> <span data-ttu-id="e18fe-349">Nánari upplýsingar er að finna í kaflanum [Skilgreina RSAT](#configure-rsat).</span><span class="sxs-lookup"><span data-stu-id="e18fe-349">For more information, see the [Configure RSAT](#configure-rsat) section.</span></span>
2. <span data-ttu-id="e18fe-350">Áður en þú getur keyrt prófunardæmi færðu kvaðningu um að sækja sjálfvirkt og setja upp vafradrifið sem samsvarar sjálfgefna vafranum sem er valinn í RSAT-stillingu.</span><span class="sxs-lookup"><span data-stu-id="e18fe-350">Before you can run a test case, you're prompted to automatically download and install the browser driver that corresponds to the default browser that is selected in the RSAT configuration.</span></span> <span data-ttu-id="e18fe-351">Nánari upplýsingar er að finna í kaflanum [Sækja og keyra prófunardæmi](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="e18fe-351">For more information, see the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

## <a name="get-started-with-rsat"></a><span data-ttu-id="e18fe-352">Hafist handa með RSAT</span><span class="sxs-lookup"><span data-stu-id="e18fe-352">Get started with RSAT</span></span>

### <a name="create-a-test-plan-and-test-suites"></a><span data-ttu-id="e18fe-353">Stofna prófunaráætlun og prófunarpakka</span><span class="sxs-lookup"><span data-stu-id="e18fe-353">Create a test plan and test suites</span></span>

1. <span data-ttu-id="e18fe-354">Farðu í Azure DevOps-verkið og veldu **Prófunaráætlanir**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-354">Go to the Azure DevOps project, and select **Test Plans**.</span></span>

    ![Skipunin Prófunaráætlanir](./media/setup_rsa_tool_53.png)

2. <span data-ttu-id="e18fe-356">Veldu **Ný prófunaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-356">Select **New Test Plan**.</span></span>

    ![Hnappurinn Ný prófunaráætlun](./media/setup_rsa_tool_54.png)

3. <span data-ttu-id="e18fe-358">Fylltu út reitinn **Heiti** og veldu síðan **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-358">Fill in the **Name** field, and then select **Create**.</span></span> <span data-ttu-id="e18fe-359">Fyrir þetta kennsluefni skaltu nefna prófunaráætlunina **RSAT-prófunaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-359">For this tutorial, name the test plan **RSAT Test Plan**.</span></span>

    ![Svarglugginn Ný prófunaráætlun](./media/setup_rsa_tool_55.png)

4. <span data-ttu-id="e18fe-361">Veldu plústáknið (**+**) og veldu síðan **Fast safn** til að stofna fast safn undir nýrri prófunaráætlun.</span><span class="sxs-lookup"><span data-stu-id="e18fe-361">Select the plus sign (**+**), and then select **Static suite** to create a static suite under the new test plan.</span></span> <span data-ttu-id="e18fe-362">Nefndu nýja prófunarsafnið **T01 - Gera á lager**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-362">Name the new test suite **T01 – Make to Stock**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e18fe-363">Einnig er hægt að stofna safn byggt á fyrirspurnum, ef þú vilt að nýju prófunardæmin úr BPM verði sjálfkrafa dregin inn í RSAT-prófunarpakka.</span><span class="sxs-lookup"><span data-stu-id="e18fe-363">You can also create a query-based suite, if you want the new test cases from BPM to be automatically pulled into the RSAT test suite.</span></span>

    ![Stofna fast safn](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a><span data-ttu-id="e18fe-365">Hengdu prófunardæmi við prófunarpakka</span><span class="sxs-lookup"><span data-stu-id="e18fe-365">Attach test cases to test suites</span></span>

1. <span data-ttu-id="e18fe-366">Veldu **Bæta við núverandi** hægra megin til að bæta núverandi prófunardæmum við prófunarpakkann.</span><span class="sxs-lookup"><span data-stu-id="e18fe-366">Select **Add existing** on the right side to add existing test cases to the test suite.</span></span>

    ![Bæta fyrirliggjandi hnappi við](./media/setup_rsa_tool_57.png)

2. <span data-ttu-id="e18fe-368">Á síðunni **Bæta prófunardæmum við safn** velurðu **Keyra fyrirspurn** og síðan velurðu prófunardæmi til að bæta við prófunarpakkann.</span><span class="sxs-lookup"><span data-stu-id="e18fe-368">On the **Add test cases to suite** page, select **Run query**, and then select the test case to add to the test suite.</span></span> <span data-ttu-id="e18fe-369">Fyrir þetta kennsluefni skaltu velja prófunardæmið **Stofna nýja vöru**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-369">For this tutorial, select the **Create a new product** test case.</span></span> <span data-ttu-id="e18fe-370">Veldu síðan **Bæta við prófunardæmum** í neðra hægra horninu á síðunni (þessi hnappur er ekki sýndur í eftirfarandi mynd).</span><span class="sxs-lookup"><span data-stu-id="e18fe-370">Then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Hnappurinn Keyra fyrirspurn](./media/setup_rsa_tool_58.png)

    <span data-ttu-id="e18fe-372">Prófunardæminu er bætt við prófunarpakkann **T01-Gera í lager**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-372">The test case is added to the **T01-Make to Stock** test suite.</span></span>

    ![Prófunardæmi bætt við prófunarpakkann](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a><span data-ttu-id="e18fe-374">Stilla RSAT</span><span class="sxs-lookup"><span data-stu-id="e18fe-374">Configure RSAT</span></span>

1. <span data-ttu-id="e18fe-375">Opnaðu RSAT.</span><span class="sxs-lookup"><span data-stu-id="e18fe-375">Open RSAT.</span></span>

    ![RSAT-tákn](./media/setup_rsa_tool_60.png)

2. <span data-ttu-id="e18fe-377">Þú færð viðvörunarskilaboð þar sem stendur „Regression Suite Automation Tool krefst Selenium, viltu sækja það sjálfvirkt og setja upp núna?“</span><span class="sxs-lookup"><span data-stu-id="e18fe-377">You receive a warning message that states, "The Regression Suite Automation Tool requires Selenium, do you want to automatically download and install it now?"</span></span> <span data-ttu-id="e18fe-378">Velja skal **Já**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-378">Select **Yes**.</span></span>

    ![Viðvörunarskilaboð um að Regression Suite Automation Tool krefjist Selenium](./media/setup_rsa_tool_61.png)

3. <span data-ttu-id="e18fe-380">Veldu hnappinn **Stillingar** (gírtáknið) efst í hægra horninu og fylltu síðan út eftirfarandi reiti í valmyndinni sem birtist:</span><span class="sxs-lookup"><span data-stu-id="e18fe-380">Select the **Settings** button (the gear symbol) in the upper-right corner, and then, in the dialog box that appears, fill in the following fields:</span></span>

    - <span data-ttu-id="e18fe-381">**Azure DevOps-slóð** – Sláðu inn vefslóð Azure DevOps-verksins, eins og `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span><span class="sxs-lookup"><span data-stu-id="e18fe-381">**Azure DevOps Url** – Enter the URL of your Azure DevOps project, such as `https://yourAzureDevOpsUrlHere.visualStudio.com`.</span></span>
    - <span data-ttu-id="e18fe-382">**Aðgangsmerki** - Sláðu inn aðgangsmerkið sem leyfir verkfærinu að tengjast Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="e18fe-382">**Access Token** – Enter the access token that lets the tool connect to Azure DevOps.</span></span> <span data-ttu-id="e18fe-383">Notaðu aðgangsmerki notanda sem þú bjóst til fyrr í þessari kennsluefni.</span><span class="sxs-lookup"><span data-stu-id="e18fe-383">Use the personal access token that you created earlier in this tutorial.</span></span> <span data-ttu-id="e18fe-384">Nánari upplýsingar er að finna í [Sannvotta aðgang með aðgangsmerkjum notenda](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span><span class="sxs-lookup"><span data-stu-id="e18fe-384">For more information, see [Authenticate access with personal access tokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).</span></span>
    - <span data-ttu-id="e18fe-385">**Heiti verkefnis** - Veldu heiti fyrir Azure DevOps-verkið.</span><span class="sxs-lookup"><span data-stu-id="e18fe-385">**Project Name** – Select the name of your Azure DevOps project.</span></span>
    - <span data-ttu-id="e18fe-386">**Prófunaráætlun** - Veldu Azure DevOps-prófunaráætlunina sem inniheldur prófunardæmin.</span><span class="sxs-lookup"><span data-stu-id="e18fe-386">**Test Plan** – Select the Azure DevOps test plan that contains your test cases.</span></span> <span data-ttu-id="e18fe-387">Nánari upplýsingar er að finna í [Stofna prófunaráætlanir og prófunarpakka](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span><span class="sxs-lookup"><span data-stu-id="e18fe-387">For more information, see [Create test plans and test suites](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan).</span></span> <span data-ttu-id="e18fe-388">Þegar þú hefur valið prófunaráætlun skaltu velja **Prófa tengingu** til að prófa tengingu þína við Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="e18fe-388">After you select a test plan, select **Test Connection** to test your connection to Azure DevOps.</span></span>
    - <span data-ttu-id="e18fe-389">**Hýsilheiti** – Sláið inn hýsiheiti prófunarumhverfa á borð við **\<myaos\>. cloudax.Dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-389">**Hostname** – Enter the host name of the test environment, such as **\<myaos\>.cloudax.dynamics.com**.</span></span> <span data-ttu-id="e18fe-390">Hafðu ekki forskeytin **https://** eða **http://** með.</span><span class="sxs-lookup"><span data-stu-id="e18fe-390">Don't include the **https://** or **http://** prefix.</span></span>
    - <span data-ttu-id="e18fe-391">**SOAP-hýsilheiti** – Skráðu SOAP-hýsilheiti prófunarumhverfis.</span><span class="sxs-lookup"><span data-stu-id="e18fe-391">**SOAP Hostname** – Enter the SOAP host name of the test environment.</span></span> <span data-ttu-id="e18fe-392">Yfirleitt er heiti SOAP-hýsils það sama og hýsilheitið en með viðskeytið **soap**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-392">Typically, the SOAP host name is the same as the host name, but it has a **soap** suffix.</span></span> <span data-ttu-id="e18fe-393">Eftirfarandi er dæmi: **\<myaos\>soap.cloudax.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-393">Here is an example: **\<myaos\>soap.cloudax.dynamics.com**.</span></span> <span data-ttu-id="e18fe-394">Hafðu ekki forskeytin **https://** eða **http://** með.</span><span class="sxs-lookup"><span data-stu-id="e18fe-394">Don't include the **https://** or **http://** prefix.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e18fe-395">Til að finna hýsilheiti og heiti SOAP-hýsils skaltu opna IIS Manager, hægri-smella á **Vefsvæði \> AOSService** og velja síðan **Breyta bindingum**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-395">To find the host name and SOAP host name, open IIS Manager, right-click **Sites \> AOSService**, and then select **Edit bindings**.</span></span> <span data-ttu-id="e18fe-396">Gildin í dálknum **Heiti hýsils** veita þér hýsilheitið og heiti SOAP-hýsils (heiti SOAP-hýsils er með viðskeytið **soap** í vefslóðinni).</span><span class="sxs-lookup"><span data-stu-id="e18fe-396">The values in the **Host Name** column give you the host name and SOAP host name (the SOAP host name has the suffix **soap** in the URL).</span></span>

        ![Hýsilheiti og heiti SOAP-hýsils í dálkinum Heiti hýsils](./media/setup_rsa_tool_63.png)

    - <span data-ttu-id="e18fe-398">**Notandaheiti stjórnanda** – Skráðu netfang stjórnanda í prófunarumhverfi.</span><span class="sxs-lookup"><span data-stu-id="e18fe-398">**Admin user name** – Enter the email address of an admin user in the test environment.</span></span>
    - <span data-ttu-id="e18fe-399">**Fingrafar** - Sláðu inn fingrafar auðkenningarvottorðsins, eins og lýst er hér að framan í þessu kennsluefni.</span><span class="sxs-lookup"><span data-stu-id="e18fe-399">**Thumbprint** – Enter the thumbprint of the authentication certificate, as described earlier in this tutorial.</span></span>
    - <span data-ttu-id="e18fe-400">**Vinnuskráarsafn** – Tilgreindu staðsetningu möppu til að geyma sjálfvirkniskrár prófunar, eins og Excel-prófunargagnaskrár.</span><span class="sxs-lookup"><span data-stu-id="e18fe-400">**Working directory** – Specify the folder location for storing test automation files, such as Excel test data files.</span></span> <span data-ttu-id="e18fe-401">Til dæmis, sláðu inn eða veldu **C:\\Temp\\RegressionTool**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-401">For example, enter or select **C:\\Temp\\RegressionTool**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e18fe-402">Ef nafnið á möppunni er með bilum mun framkvæmdin mistakast þar sem ekki verður hægt að finna möppuna.</span><span class="sxs-lookup"><span data-stu-id="e18fe-402">If the name of the folder has spaces, execution will fail because the folder can't be found.</span></span> <span data-ttu-id="e18fe-403">Þetta vandamál er þekkt og ætti að vera leiðrétt í nýjustu útgáfunni af verkfærinu.</span><span class="sxs-lookup"><span data-stu-id="e18fe-403">This issue is a known issue and should be fixed in the latest version of the tool.</span></span>

    - <span data-ttu-id="e18fe-404">**Sjálfgefinn vafri** – Veldu annaðhvort **Internet Explorer** eða **Google Chrome**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-404">**Default browser** – Select either **Internet Explorer** or **Google Chrome**.</span></span> <span data-ttu-id="e18fe-405">Gakktu úr skugga um að viðeigandi vafradrif hafi verið sett upp.</span><span class="sxs-lookup"><span data-stu-id="e18fe-405">Make sure that the appropriate browser drivers have been installed.</span></span>
    - <span data-ttu-id="e18fe-406">**Tímamörk prófunar** – Tilgreindu tímamörk í mínútum fyrir prófanir.</span><span class="sxs-lookup"><span data-stu-id="e18fe-406">**Test run timeout** – Specify the time-out period, in minutes, for test runs.</span></span> <span data-ttu-id="e18fe-407">Þegar tímalokin renna út er öllum virkum gluggum lokað og prófanir í bið takast ekki.</span><span class="sxs-lookup"><span data-stu-id="e18fe-407">When the time-out period elapses, all active windows are closed, and pending test cases fail.</span></span>
    - <span data-ttu-id="e18fe-408">**Tímalok prófunaraðgerða** – Þessi reitur stýrir tímalokum í mínútum fyrir biðlarabeiðnir í umhverfi Finance and Operation.</span><span class="sxs-lookup"><span data-stu-id="e18fe-408">**Test action timeout** – This field controls the time-out period, in minutes, for Finance and Operation environment server requests.</span></span> <span data-ttu-id="e18fe-409">Yfirleitt ætti sjálfgefið gildi (2 mínútur) að vera nóg.</span><span class="sxs-lookup"><span data-stu-id="e18fe-409">Usually, the default value (2 minutes) should be enough.</span></span> <span data-ttu-id="e18fe-410">Hinsvegar þegar um er að ræða hægari umhverfi gætirðu viljað hækka gildið ef villur sem tengjast tímalokum eiga sér stað.</span><span class="sxs-lookup"><span data-stu-id="e18fe-410">However, for slower environments, you might want to increase the value if errors that are related to time-outs occur.</span></span>
    - <span data-ttu-id="e18fe-411">**Heiti fyrirtækis** – Skráðu heiti fyrirtækis sem á að nota sem sjálfgefið fyrirtæki þegar Excel-færibreytuskrár eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="e18fe-411">**Company name** – Enter the company name to use as your default company when Excel parameter files are created.</span></span> <span data-ttu-id="e18fe-412">Þú getur breytt fyrirtækinu seinna með því að breyta Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="e18fe-412">You can change the company later by editing the Excel parameter file.</span></span>

    ![Svargluggi stillinga](./media/setup_rsa_tool_62.png)

4. <span data-ttu-id="e18fe-414">Veldu **Nota** til að nota og vista stillingarnar.</span><span class="sxs-lookup"><span data-stu-id="e18fe-414">Select **Apply** to apply and save your settings.</span></span>

    <span data-ttu-id="e18fe-415">Til að vista núverandi stillingar í skilgreiningaskrá á tölvunni skaltu velja **Vista sem**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-415">To save your current settings to a configuration file on your computer, select **Save as**.</span></span> <span data-ttu-id="e18fe-416">Til að endurheimta stillingarnar úr skilgreiningaskrá á tölvunni skaltu velja **Opna**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-416">To restore your settings from a configuration file on your computer, select **Open**.</span></span>

5. <span data-ttu-id="e18fe-417">Veldu **Loka** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="e18fe-417">Select **Close** to close the dialog box.</span></span>

### <a name="load-and-run-test-cases"></a><span data-ttu-id="e18fe-418">Sækja og keyra prófunardæmi</span><span class="sxs-lookup"><span data-stu-id="e18fe-418">Load and run test cases</span></span>

1. <span data-ttu-id="e18fe-419">Veldu **Sækja** til að sækja prófunaráætlunina **RSAT-prófunaráætlun** úr Azure DevOps-verkinu.</span><span class="sxs-lookup"><span data-stu-id="e18fe-419">Select **Load** to load the **RSAT Test Plan** test plan from the Azure DevOps project.</span></span>

    ![Hnappurinn Sækja](./media/setup_rsa_tool_64.png)

2. <span data-ttu-id="e18fe-421">Veldu prófunardæmið **Stofna nýja vöru** úr prófunarpakkanum og veldu síðan **Nýtt \> Mynda prófunarkeyrslu- og færibreytuskrár**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-421">Select the **Create a new product** test case from the test suite, and then select **New \> Generate Test Execution and Parameter files**.</span></span>

    ![Skipunin Mynda prófunarkeyrslu og færibreytuskrár í nýju valmyndinni](./media/setup_rsa_tool_65.png)

    <span data-ttu-id="e18fe-423">Excel-færibreytuskráin er stofnuð í staðbundnu möppunni sem þú tilgreindir í RSAT-skilgreiningunni (til dæmis, **C:\\Temp\\RegressionTool**).</span><span class="sxs-lookup"><span data-stu-id="e18fe-423">The Excel parameter file is created in the local folder that you specified in the RSAT configuration (for example, **C:\\Temp\\RegressionTool**).</span></span>

    ![Excel-færibreytuskrá stofnuð](./media/setup_rsa_tool_66.png)

3. <span data-ttu-id="e18fe-425">Ef þú vilt vista breytuskrár skaltu velja **Hlaða upp**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-425">If you want to save the parameter files, select **Upload**.</span></span> <span data-ttu-id="e18fe-426">Sjálfvirkniskrám prófunar allra valda prófana er hlaðið upp á Azure DevOps fyrir seinni tíma notkun.</span><span class="sxs-lookup"><span data-stu-id="e18fe-426">Test automation files of all selected test cases are uploaded to Azure DevOps for future use.</span></span> <span data-ttu-id="e18fe-427">(Þessar skrár innihalda Excel-færibreytuskrár prófana.)</span><span class="sxs-lookup"><span data-stu-id="e18fe-427">(These files include Excel test parameter files.)</span></span>

    <span data-ttu-id="e18fe-428">Á þennan hátt geturðu valið **Sækja** til að sækja færibreytuskrár (og sjálfvirkniskrár) úr prófunardæminu beint af Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="e18fe-428">In this way, you can select **Load** to load the parameter files (and automation files) from the test case directly from Azure DevOps.</span></span> <span data-ttu-id="e18fe-429">Þú þarft ekki að endurnýja færibreytuskrárnar.</span><span class="sxs-lookup"><span data-stu-id="e18fe-429">You don't have to regenerate the parameter files.</span></span> <span data-ttu-id="e18fe-430">Þessi nálgun verður mikilvæg seinna þegar þú vilt halda breytingum í færibreytuskránni og vilt ekki að skrifað verði yfir þær.</span><span class="sxs-lookup"><span data-stu-id="e18fe-430">This approach will become important later, when you want to keep the modifications in the parameter file and don't want them to be overwritten.</span></span>

4. <span data-ttu-id="e18fe-431">Til að staðfesta að sjálfvirkniskrár og færibreytuskrár séu vistaðar á Azure DevOps skaltu fara í Azure DevOps-verkið, velja **Spjald \> Vinnuliður** og síðan prófunardæmið **Stofna nýja vöru**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-431">To verify that the automation files and parameter files are saved to Azure DevOps, go to the Azure DevOps project, select **Boards \> Work Items**, and select the **Create a new product** test case.</span></span> <span data-ttu-id="e18fe-432">Á flipanum **Viðhengi** ættirðu að sjá fjórar skrár:</span><span class="sxs-lookup"><span data-stu-id="e18fe-432">On the **Attachments** tab, you should see four files:</span></span>

    - <span data-ttu-id="e18fe-433">**.cs** – C\# sjálfvirkniskrá</span><span class="sxs-lookup"><span data-stu-id="e18fe-433">**.cs** – C\# automation file</span></span>
    - <span data-ttu-id="e18fe-434">**.dll** – Þýdd sjálfvirkniskrá sem samsetning</span><span class="sxs-lookup"><span data-stu-id="e18fe-434">**.dll** – Compiled automation file as an assembly</span></span>
    - <span data-ttu-id="e18fe-435">**.xlsx** – Excel-færibreytuskrá</span><span class="sxs-lookup"><span data-stu-id="e18fe-435">**.xlsx** – Excel parameter file</span></span>
    - <span data-ttu-id="e18fe-436">**.xml** – Skráningarskrá</span><span class="sxs-lookup"><span data-stu-id="e18fe-436">**.xml** – Recording file</span></span>

    ![Skrár á flipanum Viðhengi](./media/setup_rsa_tool_67.png)

5. <span data-ttu-id="e18fe-438">Veldu prófunardæmið sem á að keyra og veldu síðan **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-438">Select the test case to run, and then select **Run**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e18fe-439">Áður en þú keyrir prófunardæmi og ef þú ert að nota Internet Explorer sem vafra, skaltu passa að skjáborðsupplausn þín sé stillt á **100%** í **Windows skjástillingar \> Kvarði og útlit**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-439">Before you run test cases, if you're using Internet Explorer as the browser, make sure that your desktop resolution is set to **100%** at **Windows Display settings \> Scale and layout**.</span></span> <span data-ttu-id="e18fe-440">Ef þú getur ekki breytt þessari stillingu á sýndarvél (VM) skaltu breyta henni á biðlaranum (fartölvu) sem þú ert að reyna að komast í VM af.</span><span class="sxs-lookup"><span data-stu-id="e18fe-440">If you can't change this setting on a virtual machine (VM), change it on the client (laptop) that you're trying to access the VM from.</span></span> <span data-ttu-id="e18fe-441">Upplausnarstillingarnar erfast síðan með stillingum VM-skjásins.</span><span class="sxs-lookup"><span data-stu-id="e18fe-441">The resolution settings will then be inherited by the VM display settings.</span></span>

    ![Skjáborðsupplausn stillt á 100%](./media/setup_rsa_tool_68.png)

6. <span data-ttu-id="e18fe-443">Ef vafrareklarnir eru ekki settir upp í kerfinu birtast viðvörunarskilaboðin „Þessi aðgerð krefst \<browser name\>-rekils.</span><span class="sxs-lookup"><span data-stu-id="e18fe-443">If the browser drivers aren't installed in the system, you receive a warning message that states, "This operation requires the \<browser name\> driver.</span></span> <span data-ttu-id="e18fe-444">Viltu sækja hann sjálfvirkt og setja upp núna?“</span><span class="sxs-lookup"><span data-stu-id="e18fe-444">Do you want to automatically downloads and install it now?"</span></span> <span data-ttu-id="e18fe-445">Velja skal **Já**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-445">Select **Yes**.</span></span>

    ![Viðvörunarboð fyrir Internet Explorer](./media/setup_rsa_tool_69.png)

    ![Viðvörunarboð fyrir Chrome](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > <span data-ttu-id="e18fe-448">Ef þú er að nota Chrome sem vafra og færð villuboð sem segir að setan hafi ekki verið stofnuð vegna þess að útgáfan Chrome sé ekki rétt skaltu sækja nýjasta Chrome-drifið frá <http://chromedriver.chromium.org/downloads> í möppuna **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Almennt\\Ytra\\Selenium**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-448">If you're using Chrome as the browser and receive an error message that states that the session wasn't created because the Chrome version isn't correct, download the latest Chrome driver from <http://chromedriver.chromium.org/downloads> to the **C:\\Program Files (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium** folder.</span></span>

    ![Villuboð fyrir Chrome](./media/setup_rsa_tool_71.png)

    <span data-ttu-id="e18fe-450">Prófunardæmið er keyrt og reiturinn **Niðurstaða** er uppfærður.</span><span class="sxs-lookup"><span data-stu-id="e18fe-450">The test case is run, and the **Result** field is updated.</span></span>

    ![Uppfæra niðurstöðusvæðið](./media/setup_rsa_tool_72.png)

    <span data-ttu-id="e18fe-452">Ef þú hefur fylgt þessu kennsluefni eins og það er skrifað, þá mun prófunardæmið **Stofna nýja vöru** ekki takast, vegna þess að það verkskráningin fyrir stofnun vöru vistaði vöruheitið sem harðkóðað gildi.</span><span class="sxs-lookup"><span data-stu-id="e18fe-452">If you've followed this tutorial as it's written, the **Create a new product** test case will fail, because the task recording for creating a product saved the product name as a hard-coded value.</span></span> <span data-ttu-id="e18fe-453">Ef þú endurkeyrir sama prófunardæmið ættirðu að fá villuskilaboð vegna þess að varan er þegar til.</span><span class="sxs-lookup"><span data-stu-id="e18fe-453">If you rerun the same test case, you should receive an error message, because the product already exists.</span></span>

    ![Niðurstöðureitur stilltur á Stóðst ekki](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a><span data-ttu-id="e18fe-455">Skoða prófunarniðurstöður</span><span class="sxs-lookup"><span data-stu-id="e18fe-455">View the test results</span></span>

1. <span data-ttu-id="e18fe-456">Tvísmelltu á prófunardæmið sem tókst ekki.</span><span class="sxs-lookup"><span data-stu-id="e18fe-456">Double-click the failed test case.</span></span>

    <span data-ttu-id="e18fe-457">Þú fékkst villuboð.</span><span class="sxs-lookup"><span data-stu-id="e18fe-457">You receive an error message.</span></span>

    ![Villuboð](./media/setup_rsa_tool_73.png)

2. <span data-ttu-id="e18fe-459">Veldu **Upplýsingar** til að skoða öll villuboðin.</span><span class="sxs-lookup"><span data-stu-id="e18fe-459">Select **Details** to view the whole error message.</span></span>

    ![Öll villuboðin](./media/setup_rsa_tool_74.png)

3. <span data-ttu-id="e18fe-461">Til að skoða nákvæma útgáfu af villuskilaboðum í Azure DevOps skaltu velja **Opna í Azure DevOps**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-461">To view a detailed version of the error message in Azure DevOps, select **Open in Azure DevOps**.</span></span> <span data-ttu-id="e18fe-462">Í Azure DevOps geturðu skoðað stöðu prófunardæmisins og upplýsingar villuboða.</span><span class="sxs-lookup"><span data-stu-id="e18fe-462">In Azure DevOps, you can view the status of the test case and the detailed error message.</span></span>

    ![Upplýsingar villuboða í Azure DevOps](./media/setup_rsa_tool_75.png)

4. <span data-ttu-id="e18fe-464">Til að skoða niðurstöðurnar beint í Azure DevOps-verkinu skaltu fara í **Prófunaráætlanir \> Prófunaráætlanir \> Keyrslur**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-464">To view the test results directly in the Azure DevOps project, go to **Test Plans \> Test Plans \> Runs**.</span></span> <span data-ttu-id="e18fe-465">Tvísmelltu á prófunarkeyrsluna sem þú vilt sjá meiri upplýsingar um.</span><span class="sxs-lookup"><span data-stu-id="e18fe-465">Double-click the test run that you want to see more details for.</span></span>

    ![Listi yfir prófanir í Azure DevOps](./media/setup_rsa_tool_76.png)

5. <span data-ttu-id="e18fe-467">Flipinn **Keyra samantekt** gefur til kynna að prófunardæmið hafi ekki tekist en hann veitir ekki raunverulegu villuboðin.</span><span class="sxs-lookup"><span data-stu-id="e18fe-467">The **Run summary** tab indicates that the test case failed, but it doesn't provide the actual error message.</span></span> <span data-ttu-id="e18fe-468">Til að skoða sundurliðuð villuboð velurðu flipann **Prófunarniðurstöður**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-468">To view the detailed error message, select the **Test results** tab.</span></span>

    ![Flipinn Keyra samantekt](./media/setup_rsa_tool_77.png)

    <span data-ttu-id="e18fe-470">Flipinn **Prófunarniðurstöður** veitir upplýsingar um prófunardæmið, ásamt útkomunni og villuboðunum.</span><span class="sxs-lookup"><span data-stu-id="e18fe-470">The **Test results** tab provides the test case information, together with the outcome and the error message.</span></span>

    ![Flipinn Niðurstöður prófunar](./media/setup_rsa_tool_78.png)

6. <span data-ttu-id="e18fe-472">Tvísmelltu á viðeigandi skrá til að skoða upplýsingar villuboða.</span><span class="sxs-lookup"><span data-stu-id="e18fe-472">Double-click the relevant record to view the detailed error message.</span></span>

    ![Upplýsingar villuboða](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > <span data-ttu-id="e18fe-474">Öll villuskilaboð eru einnig tiltæk staðbundið í **C:\\Notendur\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-474">All error messages are also available locally in **C:\\Users\\\$YourUserName\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.</span></span>

7. <span data-ttu-id="e18fe-475">Þú getur einnig flutt út niðurstöður prófunarkeyrslu úr prófunaráætlunarstiginu með því að velja **Flytja út**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-475">You can also export the test run results from the test plan level by selecting **Export**.</span></span>

    ![Flytur út prófunaráætlun](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a><span data-ttu-id="e18fe-477">Breyta Excel-færibreytuskrá</span><span class="sxs-lookup"><span data-stu-id="e18fe-477">Modify the Excel parameter file</span></span>

1. <span data-ttu-id="e18fe-478">Opnaðu RSAT.</span><span class="sxs-lookup"><span data-stu-id="e18fe-478">Open RSAT.</span></span>
2. <span data-ttu-id="e18fe-479">Veldu prófdæmið og veldu síðan **Breyta** til að opna Excel-færibreytuskrána.</span><span class="sxs-lookup"><span data-stu-id="e18fe-479">Select the test case, and then select **Edit** to open the Excel parameter file.</span></span>

    <span data-ttu-id="e18fe-480">Á blaðinu **EcoResProductCreate** skaltu athuga að gildið í reinum **Afurðarnúmer** er harðkóðað.</span><span class="sxs-lookup"><span data-stu-id="e18fe-480">On the **EcoResProductCreate** sheet, notice that the value of the **Product number** field is hard-coded.</span></span> <span data-ttu-id="e18fe-481">Þú verður að uppfæra þennan reit í nýtt afurðarnúmer áður en prófunardæmið er keyrt aftur.</span><span class="sxs-lookup"><span data-stu-id="e18fe-481">You must update this field to a new product number before you run the test case again.</span></span>

3. <span data-ttu-id="e18fe-482">Til að mynda einkvæmt afurðarnúmer fyrir hverja keyrslu án þess að þurfa að enduropna Excel-færibreytuskrána og uppfæra afurðarnúmerið handvirkt í hvert skipti skaltu nota eftirfarandi Excel-formúlu.</span><span class="sxs-lookup"><span data-stu-id="e18fe-482">To generate a unique product number for each run without having to reopen the Excel parameter file and manually update the product number every time, use the following Excel formula.</span></span>

    ```vba
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > <span data-ttu-id="e18fe-483">Í viðbót við flipann **Almennt** inniheldur Excel-færibreytuskráin gagnaflipa fyrir hverja síðu sem prófið heimsækir.</span><span class="sxs-lookup"><span data-stu-id="e18fe-483">In addition to the **General** tab, the Excel parameter file contains a data tab for every form page the test case visits.</span></span>

    ![Reiturinn Afurðarnúmer](./media/setup_rsa_tool_81.png)

4. <span data-ttu-id="e18fe-485">Veldu **Vista** og lokaðu síðan Excel-skjalinu.</span><span class="sxs-lookup"><span data-stu-id="e18fe-485">Select **Save**, and then close the Excel workbook.</span></span>
5. <span data-ttu-id="e18fe-486">Veldu **Hlaða upp** til að vista Excel-færibreytuskrá á Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="e18fe-486">Select **Upload** to save the Excel parameter file to Azure DevOps.</span></span>

    ![Upphleðsla skráar tókst](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > <span data-ttu-id="e18fe-488">Til að keyra prófdæmi í tilteknu notendasamhengi skaltu slá inn netfang notanda í reitnum **Prófa notanda** á flipnum **Almennt** í Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="e18fe-488">To run test cases in a specific user context, enter the user's email ID in the **Test User** field on the **General** tab of the Excel parameter file.</span></span> <span data-ttu-id="e18fe-489">Í nýjustu útgáfunni af RSAT hefur útlit reitanna í Excel-færibreytuskránni verið uppfærð, en hugtakið er enn það sama.</span><span class="sxs-lookup"><span data-stu-id="e18fe-489">In the latest version of RSAT, the layout of the fields in the Excel parameter file has been updated, but the concept remains the same.</span></span>
    >
    > ![Reiturinn Prófa notanda](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a><span data-ttu-id="e18fe-491">Sannprófa niðurstöður</span><span class="sxs-lookup"><span data-stu-id="e18fe-491">Validate the results</span></span>

- <span data-ttu-id="e18fe-492">Veldu **Keyra** til að endurkeyra prófunardæmið og sannprófa að prófunardæmið hafi staðist.</span><span class="sxs-lookup"><span data-stu-id="e18fe-492">Select **Run** to rerun the test case, and verify that the test case has passed.</span></span> <span data-ttu-id="e18fe-493">Þú getur skoðað niðurstöðurnar eins og lýst er í kaflanum [Skoða prófunarniðurstöður](#view-the-test-results).</span><span class="sxs-lookup"><span data-stu-id="e18fe-493">You can view the test results as described in the [View the test results](#view-the-test-results) section.</span></span>

    ![Niðurstöðureitur stilltur á Stóðst](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a><span data-ttu-id="e18fe-495">Keðja prófunardæma</span><span class="sxs-lookup"><span data-stu-id="e18fe-495">Chaining of test cases</span></span>

<span data-ttu-id="e18fe-496">Eitt lykilatriði í RSAT er keðja prófunardæma (það er að segja, geta prófunar til að gefa gildi til annarra prófana).</span><span class="sxs-lookup"><span data-stu-id="e18fe-496">One key feature of RSAT is the chaining of test cases (that is, the capability of a test to pass values to other tests).</span></span> <span data-ttu-id="e18fe-497">Prófunardæmi eru keyrð í samræmi við skilgreinda röð þeirra í Azure DevOps-prófunaráætlun.</span><span class="sxs-lookup"><span data-stu-id="e18fe-497">Test cases are run according to their defined order in the Azure DevOps test plan.</span></span> <span data-ttu-id="e18fe-498">(Þessa röð er einnig hægt að uppfæra í prófunarverkfærinu sjálfu.) Ef þú vilt framsenda breytur úr einni prófun í aðra er afar mikilvægt að prófanirnar séu í réttri röð.</span><span class="sxs-lookup"><span data-stu-id="e18fe-498">(This order can also be updated in the test tool itself.) Therefore, if you want to pass variables from one test case to another, it's very important that the tests be in the correct order.</span></span>

<span data-ttu-id="e18fe-499">Í þessum kafla muntu stofna vistaða breytu í fyrsta prófunardæminu, stofna annað prófunardæmi og senda vistaða breytu úr fyrsta prófunardæminu í annað prófunardæmi.</span><span class="sxs-lookup"><span data-stu-id="e18fe-499">In this section, you will create a saved variable in the first test case, create a second test case, and pass the saved variable from the first test case to the second test case.</span></span> <span data-ttu-id="e18fe-500">Síðan muntu keyra prófunardæmin sem keðju af prófunardæmum í RSAT.</span><span class="sxs-lookup"><span data-stu-id="e18fe-500">You will then run the test cases as a chained test case in RSAT.</span></span>

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a><span data-ttu-id="e18fe-501">Breyta núverandi verkskráningu til að stofna vistaða breytu</span><span class="sxs-lookup"><span data-stu-id="e18fe-501">Modify an existing task recording to create a saved variable</span></span>

1. <span data-ttu-id="e18fe-502">Opna á biðlarann.</span><span class="sxs-lookup"><span data-stu-id="e18fe-502">Open the client.</span></span>
2. <span data-ttu-id="e18fe-503">Veldu hnappinn **Stillingar** (gírtáknið) og síðan **Verkskráningu**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-503">Select the **Settings** button (the gear symbol), and then select **Task recorder**.</span></span>
3. <span data-ttu-id="e18fe-504">Veldu **Breyta skráningu**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-504">Select **Edit Recording**.</span></span>

    ![Hnappurinn Breyta skráningu](./media/setup_rsa_tool_85.png)

4. <span data-ttu-id="e18fe-506">Veldu **Opna úr Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-506">Select **Open from Lifecycle Services**.</span></span>

    ![Opna úr hnappnum Lifecycle Services](./media/setup_rsa_tool_86.png)

5. <span data-ttu-id="e18fe-508">Veldu **Velja Lifecycle Services-safnið**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-508">Select **Select the Lifecycle Services library**.</span></span>

    ![Veldu hnappinn Lifecycle Services-safnið](./media/setup_rsa_tool_87.png)

    <span data-ttu-id="e18fe-510">BPM-söfn eru sótt úr LCS.</span><span class="sxs-lookup"><span data-stu-id="e18fe-510">BPM libraries are loaded from LCS.</span></span>

    ![Hleður BPM-söfnum](./media/setup_rsa_tool_88.png)

6. <span data-ttu-id="e18fe-512">Eftir að BPM-söfn hafa verið sótt úr LCS skaltu velja **RSAT** BPM-safnið og viðskiptaferlið **Stofna nýja vöru** sem verkskráningin var tengd við.</span><span class="sxs-lookup"><span data-stu-id="e18fe-512">After the BPM libraries are loaded from LCS, select the **RSAT** BPM library and the **Create a new product** business process that the task recording was associated with.</span></span> <span data-ttu-id="e18fe-513">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-513">Then select **OK**.</span></span>

    ![Val á BPM-safn og viðskiptaferli](./media/setup_rsa_tool_89.png)

7. <span data-ttu-id="e18fe-515">Heiti viðeigandi verkskráningar er slegið inn í reitinn **Heiti skráningar**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-515">The name of the appropriate task recording is entered in the **Recording name** field.</span></span> <span data-ttu-id="e18fe-516">Velja **Ræsa**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-516">Select **Start**.</span></span>

    ![Heiti verkskáningarinnar í reitnum Heiti skráningar](./media/setup_rsa_tool_90.png)

8. <span data-ttu-id="e18fe-518">Farðu í **Afurðaupplýsingastjórnun \> Afurðir** og veldu **Nýtt** til að opna síðuna þar sem upphafleg verkskráning, **Stofna afurð**, var skráð.</span><span class="sxs-lookup"><span data-stu-id="e18fe-518">Go to **Product information management \> Products**, and select **New** to open the page where the original task recording, **Create a product**, was recorded.</span></span>
9. <span data-ttu-id="e18fe-519">Veldu **Setja inn skref**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-519">Select **Insert step**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e18fe-520">Nýja skrefið er sett inn á **eftir** skrefinu sem þú valdir í glugganum.</span><span class="sxs-lookup"><span data-stu-id="e18fe-520">The new step is inserted **after** the step that you selected in the pane.</span></span>

    ![Hnappurinn Setja inn skref](./media/setup_rsa_tool_91.png)

10. <span data-ttu-id="e18fe-522">Hægrismelltu á reitinn **Afurðarnúmer** og veldu síðan **Verkskráning \> Afrita**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-522">Right-click the **Product number** field, and then select **Task recorder \> Copy**.</span></span>

    ![Afrita skipun](./media/setup_rsa_tool_92.png)

11. <span data-ttu-id="e18fe-524">Nýju skrefi er bætt í glugganum.</span><span class="sxs-lookup"><span data-stu-id="e18fe-524">A new step is added in the pane.</span></span> <span data-ttu-id="e18fe-525">Skráðu niður gildið í reitnum **Afurðarnúmer** vegna þess að þú þarft það síðar.</span><span class="sxs-lookup"><span data-stu-id="e18fe-525">Make a note of the value in the **Product number** field, because you will need it later.</span></span>

    ![Nýju skrefi bætt við](./media/setup_rsa_tool_93.png)

12. <span data-ttu-id="e18fe-527">Veldu **Breytingum lokið**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-527">Select **Done editing**.</span></span>
13. <span data-ttu-id="e18fe-528">Veldu **Vista í Lifecycle Services** og tengdu nýja verkskráningu við sama BPM-safnið og viðskiptaferlið sem upphafleg verkskráning var tengd við.</span><span class="sxs-lookup"><span data-stu-id="e18fe-528">Select **Save to Lifecycle Services**, and associate the new task recording with the same BPM library and business process that the original task recording was associated with.</span></span> <span data-ttu-id="e18fe-529">Nánari upplýsingar er að finna í kaflanum [Stofna verkskráningu og vista hana í BPM-safnið](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="e18fe-529">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>
14. <span data-ttu-id="e18fe-530">Farðu í BPM-safnið og veldu **Samstilla prófunardæmi** til að yfirskrifa þá verkskráningu sem fylgir prófunardæminu í Azure DevOps, eins og lýst er í kaflanum [Prófa samstillingu úr BPM við Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="e18fe-530">Go to the BPM library, and select **Sync testcases** to overwrite the task recording that is attached to the test case in Azure DevOps, as described in the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>
15. <span data-ttu-id="e18fe-531">Opnaðu RSAT og veldu **Sækja** til að endursækja öll prófunardæmin í prófunarpakkanum.</span><span class="sxs-lookup"><span data-stu-id="e18fe-531">Open RSAT, and select **Load** to reload all the test cases in the test suite.</span></span> <span data-ttu-id="e18fe-532">Það verður að endurnýja sjálfvirkni- og færibreytuskrár fyrir viðeigandi prófunardæmi með því að velja prófunardæmið og velja síðan **Nýtt \> Mynda prófunarkeyrslu- og færibreytuskrár**, eins og lýst er í kaflanum [Sækja og keyra prófunardæmi](#load-and-run-test-cases).</span><span class="sxs-lookup"><span data-stu-id="e18fe-532">You must regenerate the automation and parameter files for the appropriate test case by selecting the test case and then selecting **New \> Generate Test Execution and Parameter files**, as described in the [Load and run test cases](#load-and-run-test-cases) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e18fe-533">Ef Excel-færibreytuskráin var skilin eftir opnuð mun endurnýjun ekki takast.</span><span class="sxs-lookup"><span data-stu-id="e18fe-533">If the Excel parameter file was left open, regeneration will fail.</span></span> <span data-ttu-id="e18fe-534">Passaðu þess vegna að Excel-færibreytuskráin fyrir prófunardæmið sé lokuð áður en þú myndar nýja Excel-færibreytuskrá.</span><span class="sxs-lookup"><span data-stu-id="e18fe-534">Therefore, make sure that the Excel parameter file for the test case is closed before you generate the new Excel parameter file.</span></span>

16. <span data-ttu-id="e18fe-535">Veldu **Breyta** til að opna nýja Excel-færibreytuskrána.</span><span class="sxs-lookup"><span data-stu-id="e18fe-535">Select **Edit** to open the new Excel parameter file.</span></span> <span data-ttu-id="e18fe-536">Þú munt sjá nýja færslu **Vistuð breyta** í línu 9.</span><span class="sxs-lookup"><span data-stu-id="e18fe-536">You will see a new **Saved variable** entry on line 9.</span></span> <span data-ttu-id="e18fe-537">Þessi breyta, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, er vistuð í XML-skrá verkskráningarinnar og hana má nota í síðari prófanir.</span><span class="sxs-lookup"><span data-stu-id="e18fe-537">This variable, **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}**, is saved in the task recording's XML file and can be used in subsequent tests.</span></span>

    ![Vistuð breytufærsla](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a><span data-ttu-id="e18fe-539">Stofna nýtt prófunardæmi</span><span class="sxs-lookup"><span data-stu-id="e18fe-539">Create a new test case</span></span>

1. <span data-ttu-id="e18fe-540">Farðu í **RSAT** BPM-safnð.</span><span class="sxs-lookup"><span data-stu-id="e18fe-540">Go to the **RSAT** BPM library.</span></span>
2. <span data-ttu-id="e18fe-541">Veldu ferlið **Sýnisstuðningsviðskiptaferli** og síðan velurðu til hægri **Breyta ham**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-541">Select the **Sample Support Business Process** process, and then, on the right, select **Edit mode**.</span></span>
3. <span data-ttu-id="e18fe-542">Breyttu gildi bæði reitarins **Heiti** og reitarins **Lýsing** í **Losa afurð**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-542">Change the value of both the **Name** field and the **Description** field to **Release a product**.</span></span> <span data-ttu-id="e18fe-543">Veldu síðan **Vista**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-543">Then select **Save**.</span></span>

    ![Heiti og lýsingu breytt í Losa afurð](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a><span data-ttu-id="e18fe-545">Stofna nýja verkskráningu sem er með staðfestingaraðgerð</span><span class="sxs-lookup"><span data-stu-id="e18fe-545">Create a new task recording that has a Validate function</span></span>

- <span data-ttu-id="e18fe-546">Stofnaðu verkskráningu til að losa afurðina sem var stofnuð áður til lögaðila í Bandaríkjunum.</span><span class="sxs-lookup"><span data-stu-id="e18fe-546">Create a task recording to release the product that was created earlier to the USRT legal entity.</span></span> <span data-ttu-id="e18fe-547">Nánari upplýsingar er að finna í kaflanum [Stofna verkskráningu og vista hana í BPM-safnið](#create-a-task-recording-and-save-it-to-the-bpm-library).</span><span class="sxs-lookup"><span data-stu-id="e18fe-547">For more information, see the [Create a task recording and save it to the BPM library](#create-a-task-recording-and-save-it-to-the-bpm-library) section.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e18fe-548">Fyrir keðjuð prófunardæmi mælum við alltaf með að þú finnir eða síir fyrir skrána sem þú þarfnast með því að *rita gildið handvirkt inn í reitinn*.</span><span class="sxs-lookup"><span data-stu-id="e18fe-548">For chained test cases, we always recommend that you find or filter for the record that you require by *manually typing the value of the field*.</span></span> <span data-ttu-id="e18fe-549">Þannig getur verkfærið ákvarðað skrána sem nota verður aðgerðin við í síðara prófunardæminu.</span><span class="sxs-lookup"><span data-stu-id="e18fe-549">In that way, the tool can determine the record that the action must be taken against in the subsequent test case.</span></span>

    ![Ný verkskráning sem er með staðfestingaraðgerð](./media/setup_rsa_tool_96.png)

    <span data-ttu-id="e18fe-551">Þegar afurðin er fundin með því að nota flýtiafmörkun, en áður en þú velur **Losa afurðir**, staðfestirðu gildi reitsins **Afurðarnúmer** til að ganga úr skugga um að afurðakennið sé það afurðakenni sem var búið til áður, eins og skýringarmyndin á undan sýnir.</span><span class="sxs-lookup"><span data-stu-id="e18fe-551">As the preceding illustration shows, after the product is found by using the Quick Filter, but before you select **Release products**, you validate the value of the **Product number** field to make sure that the product ID is the product ID that was created earlier.</span></span> <span data-ttu-id="e18fe-552">Til að staðfesta gildi skaltu hægrismella á reitinn **Afurðarnúmer** og velja síðan **Verkskráning \> Staðfesta \> Núverandi gildi**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-552">To validate the value, right-click the **Product number** field, and then select **Task recorder \> Validate \> Current Value**.</span></span>

    ![Staðfesting á núvarndi gildi](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a><span data-ttu-id="e18fe-554">Vistaðu verkskráninguna í BPM</span><span class="sxs-lookup"><span data-stu-id="e18fe-554">Save the task recording to BPM</span></span>

1. <span data-ttu-id="e18fe-555">Þegar verkskráningunni er lokið skaltu velja **Vista í Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-555">After the task recording is completed, select **Save to Lifecycle Services**.</span></span>

    ![Vista lokna verkskráningu í Lifecycle Services](./media/setup_rsa_tool_98.png)

2. <span data-ttu-id="e18fe-557">Upplýsingar um söfn er hlaðið úr LCS.</span><span class="sxs-lookup"><span data-stu-id="e18fe-557">Library information is loaded from LCS.</span></span>

    ![Hleður safnsupplýsingum úr LCS](./media/setup_rsa_tool_99.png)

3. <span data-ttu-id="e18fe-559">Veldu BPM-safn til að tengja við verkskráninguna.</span><span class="sxs-lookup"><span data-stu-id="e18fe-559">Select the BPM library to associate the task recording with.</span></span> <span data-ttu-id="e18fe-560">Fyrir þetta kennsluefni skaltu velja BPM-safnið **RSAT** sem var stofnað áður og síðan viðskiptaferlið **Losa afurð** undir því.</span><span class="sxs-lookup"><span data-stu-id="e18fe-560">For this tutorial, select the **RSAT** BPM library that was created earlier and the **Release a product** business process under it.</span></span> <span data-ttu-id="e18fe-561">Veljið síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-561">Then select **OK**.</span></span>

#### <a name="sync-bpm-to-azure-devops"></a><span data-ttu-id="e18fe-562">Samstilla BPM við Azure DevOps</span><span class="sxs-lookup"><span data-stu-id="e18fe-562">Sync BPM to Azure DevOps</span></span>

1. <span data-ttu-id="e18fe-563">Farðu í BPM-safnið og opnaðu **RSAT**-safnið.</span><span class="sxs-lookup"><span data-stu-id="e18fe-563">Go to the BPM library, and open the **RSAT** library.</span></span>
2. <span data-ttu-id="e18fe-564">Veldu **VSTS-samstilling** og síðan **Samstilla prófunardæmi**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-564">Select **VSTS sync** and then **Sync test cases**.</span></span> <span data-ttu-id="e18fe-565">Nánari upplýsingar er að finna í kaflanum [Prófa samstillingu úr BPM við Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).</span><span class="sxs-lookup"><span data-stu-id="e18fe-565">For more information, see the [Test the synchronization from BPM to Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops) section.</span></span>

    <span data-ttu-id="e18fe-566">Þegar samstillingunni er lokið, verður nýr vinnuliður og samsvarandi prófdæmi fyrir viðskiptaferlið **Losa afurð** birtist í Azure DevOps á **Spjald \> Vinnuliðir**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-566">After the synchronization is completed, the new work item and the corresponding test case for the **Release a product** business process appear in Azure DevOps at **Boards \> Work Items**.</span></span>

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a><span data-ttu-id="e18fe-567">Bættu nýjum prófunardæmum við núverandi prófunarpakka</span><span class="sxs-lookup"><span data-stu-id="e18fe-567">Add the new test case to the existing test suite</span></span>

1. <span data-ttu-id="e18fe-568">Farðu í **Prófunaráætlanir \> Prófunaráætlanir** og veldu áætlunina **RSAT-prófunaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-568">Go to **Test plans \> Test plans**, and select the **RSAT Test Plan** plan.</span></span>
2. <span data-ttu-id="e18fe-569">Veldu **Bæta við fyrirliggjandi**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-569">Select **Add existing**.</span></span>
3. <span data-ttu-id="e18fe-570">Á síðunni **Bæta prófunardæmum við í safn** velurðu **Keyra fyrirspurn**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-570">On the **Add test cases to suite** page, select **Run query**.</span></span>
4. <span data-ttu-id="e18fe-571">Veldu nýja prófunardæmið sem var búið til fyrir **Losa afurð** og veldu síðan **Bæta við prófunardæmum** neðst í hægra horni síðunnar (þessi hnappur er ekki sýndur á eftirfarandi mynd).</span><span class="sxs-lookup"><span data-stu-id="e18fe-571">Select the new test case that was created for **Release a product**, and then select **Add test cases** in the lower-right corner of the page (this button isn't shown in the following illustration).</span></span>

    ![Síðan Bæta prófunardæmum við safn](./media/setup_rsa_tool_100.png)

    <span data-ttu-id="e18fe-573">Núna er prófunarsafnið með tvö prófunardæmi.</span><span class="sxs-lookup"><span data-stu-id="e18fe-573">The test suite now has two test cases.</span></span>

    ![Tvö prófunardæmi í prófunarpakkanum](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a><span data-ttu-id="e18fe-575">Hlaða prófunardæmum í RSAT</span><span class="sxs-lookup"><span data-stu-id="e18fe-575">Load test cases into RSAT</span></span>

1. <span data-ttu-id="e18fe-576">Opnaðu RSAT og veldu **Sækja**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-576">Open RSAT, and select **Load**.</span></span>
2. <span data-ttu-id="e18fe-577">Prófunardæmunum hefur verið hlaðið og þú færð viðvörun sem segir: „Þessi aðgerð mun skrifa yfir Excel-prófgagnaskrár, staðbundnar breytingar munu glatast.</span><span class="sxs-lookup"><span data-stu-id="e18fe-577">The test cases are loaded, and you receive a warning that states, "This action will overwrite Excel test data files, local changes will be lost.</span></span> <span data-ttu-id="e18fe-578">Á að halda áfram?“</span><span class="sxs-lookup"><span data-stu-id="e18fe-578">Do you want to proceed?"</span></span> <span data-ttu-id="e18fe-579">Veldu **Já** til að uppfæra Excel-færibreytuskrár í staðbundna kerfinu en ekki Excel-færibreytuskrár sem var hlaðið upp í Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="e18fe-579">Select **Yes** to update the Excel parameter files in the local system but not the Excel parameter files that were uploaded to Azure DevOps.</span></span>

    ![Þessi aðgerð mun skrifa yfir Excel-prófunargagnaskrár](./media/setup_rsa_tool_102.png)

    <span data-ttu-id="e18fe-581">Báðum prófunardæmunum hefur verið hlaðið, ásamt Excel-færibreytuskránni fyrir fyrsta prófunardæmið.</span><span class="sxs-lookup"><span data-stu-id="e18fe-581">Both the test cases are loaded, together with the Excel parameter file for the first test case.</span></span> <span data-ttu-id="e18fe-582">Þar sem þú valdir **Hlaða upp** í síðustu keyrslunni eru færibreytuskrárnar dregnar úr Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="e18fe-582">Because you selected **Upload** in the last run, the parameter files are pulled from Azure DevOps.</span></span>

    ![Prófunardæmum hlaðið](./media/setup_rsa_tool_103.png)

3. <span data-ttu-id="e18fe-584">Veldu aðeins annað prófunardæmið og veldu síðan **Nýtt \> Mynda prófunarkeyrslu og færibreytuskrár**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-584">Select only the second test case, and then select **New \> Generate test execution and parameter files**.</span></span>

#### <a name="edit-the-excel-parameter-file"></a><span data-ttu-id="e18fe-585">Breyta Excel-færibreytuskránni</span><span class="sxs-lookup"><span data-stu-id="e18fe-585">Edit the Excel parameter file</span></span>

1. <span data-ttu-id="e18fe-586">Veldu aðeins annað prófdæmið og veldu síðan **Breyta** til að opna samsvarandi Excel-færibreytuskrá.</span><span class="sxs-lookup"><span data-stu-id="e18fe-586">Select only the second test case, and then select **Edit** to open the corresponding Excel parameter file.</span></span>
2. <span data-ttu-id="e18fe-587">Afritaðu vistaða breytu **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** (sjá kaflann [Breyta núverandi verkskráningu til að stofna vistaða breytu](#modify-an-existing-task-recording-to-create-a-saved-variable)) úr fyrsta prófunardæminu inn í alla reiti þar sem afurðarnúmerið er notað.</span><span class="sxs-lookup"><span data-stu-id="e18fe-587">Copy the **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** saved variable (see the [Modify an existing task recording to create a saved variable](#modify-an-existing-task-recording-to-create-a-saved-variable) section) from the first test case into all the fields where the product number is used.</span></span> <span data-ttu-id="e18fe-588">Í þessu dæmi afritar þú breytu inn í reitina **Afurðarnúmer** og **Staðfesta afurðarnúmer** á blaðinu **EcoResProductListPage**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-588">In this case, you copy the variable into the **Product number** and **Validate Product number** fields on the **EcoResProductListPage** sheet.</span></span>

    ![Reitirnir Afurðarnúmer og Staðfesta afurðarnúmer](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > <span data-ttu-id="e18fe-590">Aðeins er hægt að láta breytur ganga áfram á milli prófana í sömu prófunarkeyrslu.</span><span class="sxs-lookup"><span data-stu-id="e18fe-590">Variables can be passed between tests only during the same test run.</span></span> <span data-ttu-id="e18fe-591">Heiti breytanna verða að stemma nákvæmlega.</span><span class="sxs-lookup"><span data-stu-id="e18fe-591">The names of the variables must match exactly.</span></span>

3. <span data-ttu-id="e18fe-592">Veldu **Vista** og lokaðu síðan Excel-skjalinu.</span><span class="sxs-lookup"><span data-stu-id="e18fe-592">Select **Save**, and then close the Excel workbook.</span></span>
4. <span data-ttu-id="e18fe-593">Veldu **Hlaða upp** til að vista breytingarnar sem þú gerðir í Excel-færibreytuskránni.</span><span class="sxs-lookup"><span data-stu-id="e18fe-593">Select **Upload** to save the changes that you made to the Excel parameter file.</span></span>

#### <a name="run-the-chained-test-cases"></a><span data-ttu-id="e18fe-594">Keyrðu keðjuð prófunardæmi</span><span class="sxs-lookup"><span data-stu-id="e18fe-594">Run the chained test cases</span></span>

1. <span data-ttu-id="e18fe-595">Veldu bæði prófunardæmin og veldu síðan **Keyra**.</span><span class="sxs-lookup"><span data-stu-id="e18fe-595">Select both the test cases, and then select **Run**.</span></span>
2. <span data-ttu-id="e18fe-596">Staðfestu að bæði prófunardæmin hafi staðist.</span><span class="sxs-lookup"><span data-stu-id="e18fe-596">Verify that both test cases have passed.</span></span>

    ![Niðurstöðureiturinn stilltur á staðist fyrir bæði prófunardæmin](./media/setup_rsa_tool_105.png)


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]