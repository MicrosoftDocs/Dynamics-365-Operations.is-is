---
title: Fartækjavinnusvæði fyrir samþykkt innkaupapöntunar
description: Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæði fyrir samþykkt innkaupapöntunar, sem gerir kleift að skoða innkaupapantanir og bregðast við þeim með aðgerðum. Til dæmis er hægt að samþykkja eða hafna innkaupapöntun.
author: mkirknel
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 30211
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 75a38b99fe0aee7d4dd386191be236e54097e867
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561268"
---
# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="7ce6e-104">Fartækjavinnusvæði fyrir samþykkt innkaupapöntunar</span><span class="sxs-lookup"><span data-stu-id="7ce6e-104">Purchase order approval mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="7ce6e-105">Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið **Samþykkt innkaupapöntunar**.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="7ce6e-106">Þetta vinnusvæði gerir kleift að skoða innkaupapantanir og bregðast við þeim með aðgerðum.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="7ce6e-107">Til dæmis er hægt að samþykkja eða hafna innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="7ce6e-108">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="7ce6e-108">Overview</span></span> 
<span data-ttu-id="7ce6e-109">Innkaupapantanir sem þarfnast samþykkis fara í gegnum samþykktarverkflæði.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="7ce6e-110">Verkflæðið getur innihaldið ýmis þrep sem krefjast þess að einn eða fleiri einstaklingar grípi til aðgerða.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="7ce6e-111">Til dæmis gæti einstaklingur þurft að ljúka við verk eða samþykkja innkaupapöntunina.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="7ce6e-112">Vinnusvæðið **Samþykkt innkaupapöntunar** gerir kleift að skoða á auðveldan hátt og bregðast við innkaupapöntunum úr fartækinu.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="7ce6e-113">Þetta vinnusvæði leyfir þér einnig að grípa til sömu verkflæðisaðgerða sem þú getur gripið til í vefbiðlara Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-113">This workspace also lets you take the same workflow actions that you can take from the Microsoft Dynamics 365 for Finance and Operations, web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7ce6e-114">Forkröfur</span><span class="sxs-lookup"><span data-stu-id="7ce6e-114">Prerequisites</span></span>
<span data-ttu-id="7ce6e-115">Forkröfur eru mismunandi eftir þeirri útgáfu Finance and Operations sem hefur verið innleidd í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-115">The prerequisites vary, depending on the version of Finance and Operations that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-finance-and-operations"></a><span data-ttu-id="7ce6e-116">Skilyrði ef þú notar Microsoft Dynamics 365 for Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7ce6e-116">Prerequisites if you use Microsoft Dynamics 365 for Finance and Operations</span></span> 
<span data-ttu-id="7ce6e-117">Ef Microsoft Dynamics 365 for Finance and Operations hefur verið innleitt í fyrirtækinu verður kerfisstjóri að birta fartækjavinnusvæðið **Samþykkt innkaupapöntunar**.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-117">If Microsoft Dynamics 365 for Finance and Operations has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="7ce6e-118">Leiðbeiningar er að finna í [Fartækjavinnusvæði birt](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="7ce6e-118">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="7ce6e-119">Skilyrði ef þú notar Microsoft Dynamics 365 for Operations útgáfu 1611 með verkvangsuppfærslu 3 eða nýrri</span><span class="sxs-lookup"><span data-stu-id="7ce6e-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="7ce6e-120">Ef Microsoft Dynamics 365 for Operations útgáfa 1611 með verkvangsuppfærslu 3 eða síðar hefur verið sett upp fyrir fyrirtækið þitt, verður kerfisstjórinn að ljúka eftirfarandi skilyrðum.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7ce6e-121">Skilyrði</span><span class="sxs-lookup"><span data-stu-id="7ce6e-121">Prerequisite</span></span></th>
<th><span data-ttu-id="7ce6e-122">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="7ce6e-122">Role</span></span></th>
<th><span data-ttu-id="7ce6e-123">lýsing</span><span class="sxs-lookup"><span data-stu-id="7ce6e-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ce6e-124">Innleiða KB 4017918.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="7ce6e-125">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="7ce6e-125">System administrator</span></span></td>
<td><span data-ttu-id="7ce6e-126">KB 4017918 er X++ uppfærsla eða lýsigagnabráðabót sem inniheldur fartækjavinnusvæðið <strong>Samþykkt innkaupapöntunar</strong>.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="7ce6e-127">Til að setja upp KB 4017918 verður kerfisstjóri að fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="7ce6e-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Sækja bráðabót lýsigagna frá Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="7ce6e-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Setja upp bráðabót lýsigagna</a>.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="7ce6e-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Stofna virkjanlegan pakka</a> sem inniheldur <strong>SCMMobile</strong> líkanið og hlaða síðan virkjanlega pakkann í LCS.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="7ce6e-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Notaðu virkjanlega pakkann</a>.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ce6e-132">Útgáfa fartækjavinnusvæðisins <strong>Samþykkt innkaupapöntunar</strong></span><span class="sxs-lookup"><span data-stu-id="7ce6e-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="7ce6e-133">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="7ce6e-133">System administrator</span></span></td>
<td><span data-ttu-id="7ce6e-134">Sjáið <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Fartækjavinnusvæði birt</a>.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-134">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="7ce6e-135">Sæktu og settu upp fartækjaforritið</span><span class="sxs-lookup"><span data-stu-id="7ce6e-135">Download and install the mobile app</span></span>
<span data-ttu-id="7ce6e-136">Sæktu og settu upp Microsoft Dynamics 365 for Unified Operations Mobile forritið:</span><span class="sxs-lookup"><span data-stu-id="7ce6e-136">Download and install the Microsoft Dynamics 365 for Unified Operations mobile app:</span></span>

- [<span data-ttu-id="7ce6e-137">Fyrir Android síma</span><span class="sxs-lookup"><span data-stu-id="7ce6e-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="7ce6e-138">Fyrir iPhone síma</span><span class="sxs-lookup"><span data-stu-id="7ce6e-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="7ce6e-139">Innskráning í fartækjaforritið</span><span class="sxs-lookup"><span data-stu-id="7ce6e-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="7ce6e-140">Ræstu forritið í fartækinu þínu.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="7ce6e-141">Færðu inn vefslóð þína fyrir Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="7ce6e-142">Í fyrsta sinn sem þú skráir þig inn, er beðið um notandanafn og aðgangsorð þitt.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="7ce6e-143">Færðu inn skilríki</span><span class="sxs-lookup"><span data-stu-id="7ce6e-143">Enter your credentials.</span></span>
4. <span data-ttu-id="7ce6e-144">Eftir að þú hefur skráð þig inn, birtast tiltæk vinnusvæði fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="7ce6e-145">Athugið að ef kerfisstjóri gefur út nýtt vinnusvæði síðar, verður að endurræsa listann yfir fartækjavinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![Vinnusvæði fyrir samþykkt innkaupapöntunar á listanum yfir tiltæk vinnusvæði](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="7ce6e-147">Skoða pantanir sem þér hefur verið úthlutað</span><span class="sxs-lookup"><span data-stu-id="7ce6e-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="7ce6e-148">Veldu vinnusvæðið **Samþykkt innkaupapöntunar** í fartækinu.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="7ce6e-149">Veldu **Pantanir úthlutaðar á mig** til að skoða allar innkaupapantanir þar sem þú hefur verið beðin(n) um að grípa til aðgerða í verkflæði samþykktar á innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="7ce6e-150">Veldu pöntun.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-150">Select an order.</span></span> <span data-ttu-id="7ce6e-151">Á síðunni **Upplýsingar um pöntun** sjást hausupplýsingar og línur pöntunar.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="7ce6e-152">Einnig er hægt að finna leiðbeiningar í verkflæðisverkinu.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="7ce6e-153">Veldu **Dreifing á fjárhagsupphæð** til að opna síðuna **Dreifing á fjárhagsupphæð hauss**.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="7ce6e-154">Farðu aftur á síðuna **Upplýsingar um pöntun** og veldu línu.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="7ce6e-155">Úr upplýsingum um pöntunarlínu er einnig hægt að skoða línutengda dreifingu á fjárhagsupphæð.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="7ce6e-156">Ljúka við aðgerð í innkaupapöntun</span><span class="sxs-lookup"><span data-stu-id="7ce6e-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="7ce6e-157">Þegar þú hefur skoðað innkaupapöntunina sem þér hefur verið úthlutað og þú hefur lesið verkflæðisfyrirmæli ættir þú að vera tilbúin(n) til aðgerða.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="7ce6e-158">Veldu vinnusvæðið **Samþykkt innkaupapöntunar** í fartækinu.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="7ce6e-159">Veldu **Pantanir úthlutaðar á mig** til að skoða allar innkaupapantanir þar sem þú hefur verið beðin(n) um að grípa til aðgerða í verkflæði samþykktar á innkaupapöntun.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="7ce6e-160">Veldu pöntun og skoðaðu upplýsingasíðuna.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="7ce6e-161">Veldu **Aðgerðir** til að sýna tiltækar aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="7ce6e-162">Aðgerðir sem eru tiltækar fara eftir verkinu sem þér hefur verið úthlutað.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="7ce6e-163">Verkaðgerð</span><span class="sxs-lookup"><span data-stu-id="7ce6e-163">Task action</span></span>    | <span data-ttu-id="7ce6e-164">Samþykktaraðgerð</span><span class="sxs-lookup"><span data-stu-id="7ce6e-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="7ce6e-165">Tilbúið</span><span class="sxs-lookup"><span data-stu-id="7ce6e-165">Complete</span></span>       | <span data-ttu-id="7ce6e-166">Samþykkja</span><span class="sxs-lookup"><span data-stu-id="7ce6e-166">Approve</span></span>          |
    | <span data-ttu-id="7ce6e-167">Vöruskil</span><span class="sxs-lookup"><span data-stu-id="7ce6e-167">Return</span></span>         | <span data-ttu-id="7ce6e-168">Hafna</span><span class="sxs-lookup"><span data-stu-id="7ce6e-168">Reject</span></span>           |
    | <span data-ttu-id="7ce6e-169">Biðja um breytingu</span><span class="sxs-lookup"><span data-stu-id="7ce6e-169">Request change</span></span> | <span data-ttu-id="7ce6e-170">Biðja um breytingu</span><span class="sxs-lookup"><span data-stu-id="7ce6e-170">Request change</span></span>   |
    | <span data-ttu-id="7ce6e-171">Úthluta</span><span class="sxs-lookup"><span data-stu-id="7ce6e-171">Delegate</span></span>       | <span data-ttu-id="7ce6e-172">Úthluta</span><span class="sxs-lookup"><span data-stu-id="7ce6e-172">Delegate</span></span>         |

5. <span data-ttu-id="7ce6e-173">Velja viðeigandi aðgerð.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="7ce6e-174">Færðu inn athugasemd á síðunni **Ljúka verki**.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="7ce6e-175">Athugaðu að ef þú velur aðgerðina **Úthluta**, verður þú að velja notanda til að úthluta verkinu.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="7ce6e-176">Velja **Ekkert**.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-176">Select **Done**.</span></span> <span data-ttu-id="7ce6e-177">Þegar þú endurnýjar vinnusvæðið hverfur innkaupapöntunin af listanum.</span><span class="sxs-lookup"><span data-stu-id="7ce6e-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 
