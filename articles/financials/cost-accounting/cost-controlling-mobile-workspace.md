---
title: "Fartækjavinnusvæði kostnaðarstýringar"
description: "Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið Kostnaðarstýring. Þetta vinnusvæði gerir kleift kostnaðarstaðar stjórnendur að skoða upplýsingar um kostnað vinnustöðvar afköst hvar og hvenær sem er."
author: AndersGirke
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 267114
ms.assetid: 612f2988-b2b9-420d-9825-40b99dc0e204
ms.search.region: global
ms.author: aevengir
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: e4c9b62456253d0d1710168d8aac1ac20e70e425
ms.contentlocale: is-is
ms.lasthandoff: 01/17/2018

---

# <a name="cost-controlling-mobile-workspace"></a><span data-ttu-id="8235b-104">Fartækjavinnusvæði kostnaðarstýringar</span><span class="sxs-lookup"><span data-stu-id="8235b-104">Cost controlling mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="8235b-105">Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið **Kostnaðarstýring**.</span><span class="sxs-lookup"><span data-stu-id="8235b-105">This topic provides information about the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="8235b-106">Þetta vinnusvæði gerir kleift kostnaðarstaðar stjórnendur að skoða upplýsingar um kostnað vinnustöðvar afköst hvar og hvenær sem er.</span><span class="sxs-lookup"><span data-stu-id="8235b-106">This workspace lets cost center managers view information about cost center performance anytime and anywhere.</span></span>

<span data-ttu-id="8235b-107">Þetta fartækjavinnusvæði er ætlað til notkunar með fartækjaforritinu Microsoft Dynamics 365 for Unified Operations.</span><span class="sxs-lookup"><span data-stu-id="8235b-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="8235b-108">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="8235b-108">Overview</span></span>
<span data-ttu-id="8235b-109">Fartækjavinnusvæði **kostnaðarstýringar** veitir skjótt yfirlit yfir núgildandi afköst kostnaðarstaðar með samanburði á raunverulegum kostnaði og kostnaði fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="8235b-109">The **Cost controlling** mobile workspace provides an instant view of the current performance of cost centers by comparing actual costs against the budgeted costs.</span></span> <span data-ttu-id="8235b-110">Hægt er að kafa niður í stöðu stakra kostnaðareininga.</span><span class="sxs-lookup"><span data-stu-id="8235b-110">You can drill down to the status of individual cost elements.</span></span>

<span data-ttu-id="8235b-111">Til dæmis er starfsmaður fær boð um að koma á erlendar ráðstefna, en fyrirtæki verða að borga öll ferðakostnaður.</span><span class="sxs-lookup"><span data-stu-id="8235b-111">For example, an employee receives an invitation to an international conference, but the organization must cover all the travel expenses.</span></span> <span data-ttu-id="8235b-112">Starfsmaðurinn spyr yfirmann sinn hvort að hann geti farið á ráðstefnuna.</span><span class="sxs-lookup"><span data-stu-id="8235b-112">The employee asks his manager whether he can attend the conference.</span></span> <span data-ttu-id="8235b-113">Stjórnandinn opnar fartækjavinnusvæði **kostnaðarstýringar** í farsímanum sínum til að sjá hvort að til sé fjárhagsáætlun fyrir því að starfsmaðurinn fari á ráðstefnuna.</span><span class="sxs-lookup"><span data-stu-id="8235b-113">The manager opens the **Cost controlling** mobile workspace on her mobile device to see whether she has budget for the employee to attend the conference.</span></span>

### <a name="data-security"></a><span data-ttu-id="8235b-114">Öryggi gagna</span><span class="sxs-lookup"><span data-stu-id="8235b-114">Data security</span></span>
<span data-ttu-id="8235b-115">Gögnin í fartækjavinnusvæði **Kostnaðarstýring** eru tryggð með notandaskilríkjum.</span><span class="sxs-lookup"><span data-stu-id="8235b-115">The data in the **Cost controlling** mobile workspace is secured through user credentials.</span></span> <span data-ttu-id="8235b-116">Stjórnendur kostnaðarstaðar hafa aðeins leyfi til að skoða gögn fyrir eigin kostnaðarstað.</span><span class="sxs-lookup"><span data-stu-id="8235b-116">Cost center managers are allowed to see data only for their own cost center.</span></span> <span data-ttu-id="8235b-117">Aðgangsstigs örygginu er stjórnað innan einingarinnar **Kostnaðarbókhald**.</span><span class="sxs-lookup"><span data-stu-id="8235b-117">The access-level security is managed in the **Cost accounting** module.</span></span>

<span data-ttu-id="8235b-118">Kostnaðarbókarar skilgreina grunnstillingar fartækjavinnusvæðis **Kostnaðarstýringar** í einingunni **Kostnaðarbókhald**.</span><span class="sxs-lookup"><span data-stu-id="8235b-118">Cost accountants define the configuration of the **Cost controlling** mobile workspace in the **Cost accounting** module.</span></span> <span data-ttu-id="8235b-119">Þegar vinnusvæðið hefur verið sett í fartækjaforritið er það tiltækt í forritinu.</span><span class="sxs-lookup"><span data-stu-id="8235b-119">After the workspace is published to the mobile app, it's available in the app.</span></span> <span data-ttu-id="8235b-120">Þannig geta allir stjórnendur kostnaðarstaða í fyrirtækinu skoðað gögn á sama sniði.</span><span class="sxs-lookup"><span data-stu-id="8235b-120">Therefore, all cost center managers in the organization can view data in the same format.</span></span>

### <a name="actions-views-and-links"></a><span data-ttu-id="8235b-121">Aðgerðir, yfirlit og tenglar</span><span class="sxs-lookup"><span data-stu-id="8235b-121">Actions, views, and links</span></span>
<span data-ttu-id="8235b-122">Fartækjavinnusvæðið **Kostnaðarstýring** býður upp á eftirfarandi aðgerðir, yfirlit og tengla:</span><span class="sxs-lookup"><span data-stu-id="8235b-122">The **Cost controlling** mobile workspace provides the following actions, views, and links:</span></span>

-   <span data-ttu-id="8235b-123">**Aðgerðir:**</span><span class="sxs-lookup"><span data-stu-id="8235b-123">**Actions:**</span></span>

    -   <span data-ttu-id="8235b-124">Notið **Velja skilgreiningu** til að velja útlit.</span><span class="sxs-lookup"><span data-stu-id="8235b-124">Use **Select configuration** to select a layout.</span></span>
    -   <span data-ttu-id="8235b-125">Notið **Valin Hluturinn kostnaður** til að velja kostnaðarstaði til að sía gögnin á.</span><span class="sxs-lookup"><span data-stu-id="8235b-125">Use **Select cost object** to select the cost centers to filter data on.</span></span>
    
        > [!NOTE]
        > <span data-ttu-id="8235b-126">Þeir kostnaðarstaðir sem birtast á listanum eru háðir aðgangi sem er veittur í einingunni **Kostnaðarbókhald**.</span><span class="sxs-lookup"><span data-stu-id="8235b-126">The cost centers that appear in the list depend on the access that is granted in the **Cost accounting** module.</span></span>

-   <span data-ttu-id="8235b-127">**Yfirlit:** Á grundvelli aðgerða sem eru valdar og skilgreiningar í einingunni **Kostnaðarbókhald** er hægt að skoða eftirfarandi upplýsingar á spjöldunum:</span><span class="sxs-lookup"><span data-stu-id="8235b-127">**Views:** Based on the actions that are selected and the configuration in the **Cost accounting** module, you can view the following information on the cards:</span></span>

    -   <span data-ttu-id="8235b-128">Raunverulegt samanb. v. fjárhagsáætlun (núgildandi tímabil)</span><span class="sxs-lookup"><span data-stu-id="8235b-128">Actual vs budget (current period)</span></span>
    -   <span data-ttu-id="8235b-129">Raunverulegt samanb. v. endurskoðaða fjárhagsáætlun (núgildandi tímabil)</span><span class="sxs-lookup"><span data-stu-id="8235b-129">Actual vs revised budget (current period)</span></span>
    -   <span data-ttu-id="8235b-130">Raunverulegt samanb. v. fjárhagsáætlun (fyrra tímabil)</span><span class="sxs-lookup"><span data-stu-id="8235b-130">Actual vs budget (previous period)</span></span>
    -   <span data-ttu-id="8235b-131">Raunverulegt samanb. v. endurskoðaða fjárhagsáætlun (fyrra tímabil)</span><span class="sxs-lookup"><span data-stu-id="8235b-131">Actual vs revised budget (previous period)</span></span>
    -   <span data-ttu-id="8235b-132">Raunverulegt samanb. v. fjárhagsáætlun (það sem af er ári)</span><span class="sxs-lookup"><span data-stu-id="8235b-132">Actual vs budget (year to date)</span></span>
    -   <span data-ttu-id="8235b-133">Raunverulegt samanb. v. endurskoðaða fjárhagsáætlun (á árinu)</span><span class="sxs-lookup"><span data-stu-id="8235b-133">Actual vs revised budget (year to date)</span></span>

    <span data-ttu-id="8235b-134">Eftirfarandi upphæðir eru sýndar á hverju spjaldi: Raunverulegar, fjárhagsáætlun, frávik og frávik %.</span><span class="sxs-lookup"><span data-stu-id="8235b-134">The following amounts are shown on every card: Actual, Budget, Variance, and Variance %.</span></span>

-   <span data-ttu-id="8235b-135">**Tenglar:**</span><span class="sxs-lookup"><span data-stu-id="8235b-135">**Links:**</span></span>

    -   <span data-ttu-id="8235b-136">Sundurliðun fyrir núverandi tímabil</span><span class="sxs-lookup"><span data-stu-id="8235b-136">Details for current period</span></span>
    -   <span data-ttu-id="8235b-137">Sundurliðun fyrir fyrra tímabil</span><span class="sxs-lookup"><span data-stu-id="8235b-137">Details for previous period</span></span>
    -   <span data-ttu-id="8235b-138">Sundurliðun fyrir það sem af er árinu</span><span class="sxs-lookup"><span data-stu-id="8235b-138">Details for year to date</span></span>

    <span data-ttu-id="8235b-139">Þegar tengill er valinn, spjald er sýndur fyrir hvern kostnaðarlið.</span><span class="sxs-lookup"><span data-stu-id="8235b-139">When you select a link, a card is shown for each cost element.</span></span> <span data-ttu-id="8235b-140">Eftirfarandi upphæðir eru sýndar á spjöldunum: Raunverulegar, fjárhagsáætlun, Fjárhagsáætlunar Frávik, Fjárhagsáætlunar Frávik %, Endurskoðuð fjárhagsáætlun, Frávik endurskoðaðrar fjárhagsáætlunar og Frávik endurskoðaðrar fjárhagsáætlunar %.</span><span class="sxs-lookup"><span data-stu-id="8235b-140">The following amounts are shown on every card: Actual, Budget, Budget variance, Budget variance %, Revised budget, Revised budget variance, and Revised budget variance %.</span></span>
    
    <span data-ttu-id="8235b-141">[![Spjald fyrir kostnaðareiningu ](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span><span class="sxs-lookup"><span data-stu-id="8235b-141">[![Card for a cost element](./media/Cost-controlling.png)](./media/Cost-controlling.png)</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8235b-142">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="8235b-142">Prerequisites</span></span>
<span data-ttu-id="8235b-143">Forkröfur eru mismunandi eftir þeirri útgáfu Microsoft Dynamics 365 sem hefur verið innleidd í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="8235b-143">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="8235b-144">Forkröfur ef þú notar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="8235b-144">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations, Enterprise edition</span></span>
<span data-ttu-id="8235b-145">Ef Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition hefur verið beitt í þínu fyrirtæki verður kerfisstjóri að birta fartækjavinnusvæðið **Kostnaðarstýring**.</span><span class="sxs-lookup"><span data-stu-id="8235b-145">If Microsoft Dynamics 365 for Finance and Operations, Enterprise edition has been deployed for your organization, the system administrator must publish the **Cost controlling** mobile workspace.</span></span> <span data-ttu-id="8235b-146">Leiðbeiningar er að finna í [Fartækjavinnusvæði birt](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="8235b-146">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="8235b-147">Forkröfur ef verið er að nota Microsoft Dynamics 365 for Operations útgáfu 1611 með svæðisuppfærslu 3 eða síðar</span><span class="sxs-lookup"><span data-stu-id="8235b-147">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later</span></span>
<span data-ttu-id="8235b-148">Ef verið er að nota Microsoft Dynamics 365 for Operations útgáfu 1611 með svæðisuppfærslu 3 eða síðar í fyrirtækinu, verður kerfisstjóri að uppfylla eftirfarandi forkröfur.</span><span class="sxs-lookup"><span data-stu-id="8235b-148">If Microsoft Dynamics 365 for Operations version 1611 with platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8235b-149">Skilyrði</span><span class="sxs-lookup"><span data-stu-id="8235b-149">Prerequisite</span></span></th>
<th><span data-ttu-id="8235b-150">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="8235b-150">Role</span></span></th>
<th><span data-ttu-id="8235b-151">lýsing</span><span class="sxs-lookup"><span data-stu-id="8235b-151">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8235b-152">Innleiða KB 4013633.</span><span class="sxs-lookup"><span data-stu-id="8235b-152">Implement KB 4013633.</span></span></td>
<td><span data-ttu-id="8235b-153">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="8235b-153">System administrator</span></span></td>

<td><span data-ttu-id="8235b-154">KB 4013633 er X++ uppfærsla eða lýsigagnabráðabót sem inniheldur fartækjavinnusvæðið <strong>Kostnaðarstýring</strong>.</span><span class="sxs-lookup"><span data-stu-id="8235b-154">KB 4013633 is an X++ update or metadata hotfix that contains the <strong>Cost controlling</strong> mobile workspace.</span></span> <span data-ttu-id="8235b-155">Til að setja upp KB 4013633 verður kerfisstjóri að fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="8235b-155">To implement KB 4013633, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="8235b-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Sæktu lýsigagnabráðabótina á Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="8235b-156"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="8235b-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Setja upp bráðabót lýsigagna</a>.</span><span class="sxs-lookup"><span data-stu-id="8235b-157"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="8235b-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Stofna virkjanlegan pakka</a> sem inniheldur <strong>SCMMobile</strong> líkanið og hlaða síðan virkjanlega pakkann í LCS.</span><span class="sxs-lookup"><span data-stu-id="8235b-158"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="8235b-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Notaðu virkjanlega pakkann</a>.</span><span class="sxs-lookup"><span data-stu-id="8235b-159"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8235b-160">Gefðu út fartækjavinnusvæðið <strong>Kostnaðarstýring</strong>.</span><span class="sxs-lookup"><span data-stu-id="8235b-160">Publish the <strong>Cost controlling</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="8235b-161">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="8235b-161">System administrator</span></span></td>
<td><span data-ttu-id="8235b-162">Sjáið <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Fartækjavinnusvæði birt</a>.</span><span class="sxs-lookup"><span data-stu-id="8235b-162">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>


## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="8235b-163">Sæktu og settu upp fartækjaforritið</span><span class="sxs-lookup"><span data-stu-id="8235b-163">Download and install the mobile app</span></span>
<span data-ttu-id="8235b-164">Sæktu og settu upp fartækjaforritið Dynamics 365 for Unified Operations:</span><span class="sxs-lookup"><span data-stu-id="8235b-164">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="8235b-165">Fyrir Android síma</span><span class="sxs-lookup"><span data-stu-id="8235b-165">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="8235b-166">Fyrir iPhone síma</span><span class="sxs-lookup"><span data-stu-id="8235b-166">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="8235b-167">Innskráning í fartækjaforritið</span><span class="sxs-lookup"><span data-stu-id="8235b-167">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="8235b-168">Ræstu forritið í fartækinu þínu.</span><span class="sxs-lookup"><span data-stu-id="8235b-168">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="8235b-169">Færðu inn vefslóð þína fyrir Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8235b-169">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="8235b-170">Í fyrsta sinn sem þú skráir þig inn, er beðið um notandanafn og aðgangsorð þitt.</span><span class="sxs-lookup"><span data-stu-id="8235b-170">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="8235b-171">Færðu inn skilríki</span><span class="sxs-lookup"><span data-stu-id="8235b-171">Enter your credentials.</span></span>
4.  <span data-ttu-id="8235b-172">Eftir að þú hefur skráð þig inn, birtast tiltæk vinnusvæði fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="8235b-172">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="8235b-173">Athugið að ef kerfisstjóri gefur út nýtt vinnusvæði síðar, verður að endurræsa listann yfir fartækjavinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="8235b-173">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="8235b-174">[![Togið upp til að uppfæra](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="8235b-174">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-the-performance-of-your-cost-center-by-using-the-cost-controlling-mobile-workspace"></a><span data-ttu-id="8235b-175">Skoða árangur þinn kostnaðarstaður með því að nota Kostnaðarstýra fartækja vinnusvæði</span><span class="sxs-lookup"><span data-stu-id="8235b-175">View the performance of your cost center by using the Cost controlling mobile workspace</span></span>

1.  <span data-ttu-id="8235b-176">Í farsímanum velurðu vinnusvæðið **Kostnaðarstýring**.</span><span class="sxs-lookup"><span data-stu-id="8235b-176">On your mobile device, select the **Cost controlling** workspace.</span></span>
2.  <span data-ttu-id="8235b-177">Veldu **Stjórnborð kostnaðarhlutar**.</span><span class="sxs-lookup"><span data-stu-id="8235b-177">Select **Cost object controlling**.</span></span>
3.  <span data-ttu-id="8235b-178">Velja **Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="8235b-178">Select **Actions**.</span></span>
4.  <span data-ttu-id="8235b-179">Smellið á **Velja grunnstillingu** til að velja útlit kostnaðarstýringar.</span><span class="sxs-lookup"><span data-stu-id="8235b-179">Select **Select configuration** to select a cost controlling layout.</span></span>
5.  <span data-ttu-id="8235b-180">Velja **Ekkert**.</span><span class="sxs-lookup"><span data-stu-id="8235b-180">Select **Done**.</span></span>
6.  <span data-ttu-id="8235b-181">Velja **Aðgerðir**.</span><span class="sxs-lookup"><span data-stu-id="8235b-181">Select **Actions**.</span></span>
7.  <span data-ttu-id="8235b-182">Velja **Velja kostnaðarhlut** til að velja kostnaðarstað sem þú hefur fengið aðgang að.</span><span class="sxs-lookup"><span data-stu-id="8235b-182">Select **Select cost object** to select the cost centers that you've been granted access to.</span></span>
8.  <span data-ttu-id="8235b-183">Velja **Ekkert**.</span><span class="sxs-lookup"><span data-stu-id="8235b-183">Select **Done**.</span></span>
9.  <span data-ttu-id="8235b-184">Skoða heildarafkomu kostnaðarstaðar.</span><span class="sxs-lookup"><span data-stu-id="8235b-184">View the overall performance of your cost center.</span></span>
10. <span data-ttu-id="8235b-185">Veljið **Upplýsingar fyrir núverandi tímabil** tengil.</span><span class="sxs-lookup"><span data-stu-id="8235b-185">Select the **Details for current period** link.</span></span>
11. <span data-ttu-id="8235b-186">Skoða vinnsluhraða stakra kostnaðareininga.</span><span class="sxs-lookup"><span data-stu-id="8235b-186">View the performance of individual cost elements.</span></span>
12. <span data-ttu-id="8235b-187">Einnig má leita að sérstökum kostnaðareiningum.</span><span class="sxs-lookup"><span data-stu-id="8235b-187">You can also search for specific cost elements.</span></span>


