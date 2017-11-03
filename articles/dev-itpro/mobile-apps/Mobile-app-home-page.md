---
title: "Heimasíða fartækjaforrits"
description: "Þetta efnisatriði lýsir Microsoft Dynamics 365 for Unified Operations fartækjaforritinu og veitir tengla á tilföng sem geta hjálpað til við að taka það upp í fyrirtæki."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Platform
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 25aad52e2640b671a1c30e42a59516293a2f98e1
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="mobile-app-home-page"></a><span data-ttu-id="a8e22-103">Heimasíða fartækjaforrits</span><span class="sxs-lookup"><span data-stu-id="a8e22-103">Mobile app home page</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a8e22-104">Þetta efnisatriði lýsir Microsoft Dynamics 365 for Unified Operations fartækjaforritinu og veitir tengla á tilföng sem geta hjálpað til við að taka það upp í fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="a8e22-104">This topic describes the Microsoft Dynamics 365 for Unified Operations mobile app and provides links to resources that can help you implement it in your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="a8e22-105">Fartækjaforritið hét áður *Microsoft Dynamics 365 for Finance and Operations*.</span><span class="sxs-lookup"><span data-stu-id="a8e22-105">The mobile app was previously named *Microsoft Dynamics 365 for Finance and Operations*.</span></span>

<a name="overview"></a><span data-ttu-id="a8e22-106">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="a8e22-106">Overview</span></span>
--------

<span data-ttu-id="a8e22-107">Fartækjaforritið gerir fyrirtæki þínu kleift að gera viðskiptaferla aðgengilega á fartækjum.</span><span class="sxs-lookup"><span data-stu-id="a8e22-107">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="a8e22-108">Eftir að upplýsingatæknistjóri þinn opnar vinnusvæði á fartækjum fyrir fyrirtækið, geta notendur skráð sig inn í forritið og strax byrjað að keyra viðskiptaferli úr þeirra fartækjum.</span><span class="sxs-lookup"><span data-stu-id="a8e22-108">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="a8e22-109">Fartækjaforritið er með eftirfarandi eiginleika, sem geta hjálpað við að auka framleiðni:</span><span class="sxs-lookup"><span data-stu-id="a8e22-109">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="a8e22-110">Notendur geta skoðað, breytt og brugðist við viðskiptagögnin, jafnvel þótt netsamband fartækja þeirra sé óreglulegt eða ekkert.</span><span class="sxs-lookup"><span data-stu-id="a8e22-110">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="a8e22-111">Þegar tæki tengist neti á ný, eru gagnaaðgerðir sem gerðar voru utan nets sjálfkrafa samstilltar við Dynamics 365 for Finance and Operations, Enterprise útgáfu eða Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a8e22-111">When a device reestablishes a network connection, offline data operations are automatically synchronized with Dynamics 365 for Finance and Operations, Enterprise edition, or Microsoft Dynamics 365 for Finance and Operations.</span></span>
- <span data-ttu-id="a8e22-112">Upplýsingatæknistjóri eða forritarar geta byggja og birtið fartækja vinnusvæði sem hefur verið sniðið að þeirra fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="a8e22-112">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="a8e22-113">Farsímaforritið notar fyrirliggjandi kóða eigna þinna.</span><span class="sxs-lookup"><span data-stu-id="a8e22-113">The app uses your existing code assets.</span></span> <span data-ttu-id="a8e22-114">Þess vegna þarf ekki að færa aftur inn villuleitaraðferðir, viðskiptagrunninn eða öryggis samskipan.</span><span class="sxs-lookup"><span data-stu-id="a8e22-114">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="a8e22-115">Upplýsingatæknistjórar eða forritarar geta auðveldlega hannað fartækjavinnusvæði með því að nota benda-og-smella verkfærið sem er í vefbiðlaranum.</span><span class="sxs-lookup"><span data-stu-id="a8e22-115">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="a8e22-116">Upplýsingatæknistjórar eða forritarar geta einnig hámarka notkun vinnusvæða utan nets með því að nota Business viðskiptagrunn umgjörðina.</span><span class="sxs-lookup"><span data-stu-id="a8e22-116">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="a8e22-117">Þar sem gögn heldur áfram að vinna þegar tæki er utan nets, eru þín farsímaforrit áfram virk og auðug, jafnvel þó ekki tæki hafa tengingu við fasta net.</span><span class="sxs-lookup"><span data-stu-id="a8e22-117">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="a8e22-118">Einingar farsímaforritsins</span><span class="sxs-lookup"><span data-stu-id="a8e22-118">Elements of the mobile app</span></span>
<span data-ttu-id="a8e22-119">Fletting í fartækjaforritinu byggist á fjórum meginhugtökum: mælaborði, vinnusvæðum, síðum og aðgerðum.</span><span class="sxs-lookup"><span data-stu-id="a8e22-119">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="a8e22-120">[![Notkunarhugtök í farsímaforritinu](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="a8e22-120">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="a8e22-121">Þegar þú ræsir smáforritið, er farið í **Yfirlitið**.</span><span class="sxs-lookup"><span data-stu-id="a8e22-121">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="a8e22-122">Á mælaborðinu getur þú séð lista yfir **vinnusvæði** sem hafa verið gefin út.</span><span class="sxs-lookup"><span data-stu-id="a8e22-122">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="a8e22-123">Í hverri vinnusvæði getur séð lista yfir **síður** sem eru tiltæk fyrir það vinnusvæðisins.</span><span class="sxs-lookup"><span data-stu-id="a8e22-123">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="a8e22-124">Hægt er að framkvæma ýmsar aðgerðir á síðu.</span><span class="sxs-lookup"><span data-stu-id="a8e22-124">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="a8e22-125">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="a8e22-125">Here are some examples:</span></span>

    - <span data-ttu-id="a8e22-126">Skoða ítarleg gögn.</span><span class="sxs-lookup"><span data-stu-id="a8e22-126">View detailed data.</span></span>
    - <span data-ttu-id="a8e22-127">Fletta á aðrar síður fyrir tengd gögn, eins og einingaupplýsingar eða línur.</span><span class="sxs-lookup"><span data-stu-id="a8e22-127">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="a8e22-128">Sjá lista yfir **aðgerðir** sem eru tiltækar fyrir þá síðu.</span><span class="sxs-lookup"><span data-stu-id="a8e22-128">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="a8e22-129">Aðgerðir gera það mögulegt að stofna eða breyta fyrirliggjandi gögnum.</span><span class="sxs-lookup"><span data-stu-id="a8e22-129">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="a8e22-130">Innleiðingarverk</span><span class="sxs-lookup"><span data-stu-id="a8e22-130">Implementation process</span></span>
<span data-ttu-id="a8e22-131">Eftirfarandi skýringarmynd sýnir ferlið fyrir innleiðingu á bæði fartækjavinnusvæðum frá Microsoft og sérsniðnum fartækjavinnusvæðum.</span><span class="sxs-lookup"><span data-stu-id="a8e22-131">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

![Innleiðingarferli farsímaforrita](./media/Mobile-implementation-process-5.png)

<span data-ttu-id="a8e22-133">Eftirfarandi tafla inniheldur tengla á tilföng sem geta hjálpað til við að innleiða bæði fartækjavinnusvæði frá Microsoft og sérsniðin fartækjavinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="a8e22-133">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="a8e22-134">Tölurnar í fyrsta dálkinum samsvara tölusettu skrefin í síðustu skýringarmynd.</span><span class="sxs-lookup"><span data-stu-id="a8e22-134">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a8e22-135">Þrep</span><span class="sxs-lookup"><span data-stu-id="a8e22-135">Step</span></span></th>
<th><span data-ttu-id="a8e22-136">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="a8e22-136">Role</span></span></th>
<th><span data-ttu-id="a8e22-137">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="a8e22-137">Action</span></span></th>
<th><span data-ttu-id="a8e22-138">Tilföng til að hjálpa til við að ljúka aðgerð</span><span class="sxs-lookup"><span data-stu-id="a8e22-138">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a8e22-139">1</span><span class="sxs-lookup"><span data-stu-id="a8e22-139">1</span></span></td>
<td><span data-ttu-id="a8e22-140">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="a8e22-140">System administrator</span></span></td>
<td><span data-ttu-id="a8e22-141">Innleiðing Finance and Operations eða Finance and Operations í fyrirtæki þínu.</span><span class="sxs-lookup"><span data-stu-id="a8e22-141">Implement Finance and Operations or Finance and Operations in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="a8e22-142">Hafir þú enn ekki tekið í notkun útgáfu af Microsoft Dynamics 365, sjá <a href="../deployment/deploy-demo-environment.md">Uppsetning sýniútgáfuumhverfis</a>.</span><span class="sxs-lookup"><span data-stu-id="a8e22-142">If you haven't yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="a8e22-143">Lista yfir fartækjavinnusvæði sem hægt er að nota má sjá á <a href="mobile-workspaces-released.md">Fartækjavinnusvæði, nýlega útgefin</a>.</span><span class="sxs-lookup"><span data-stu-id="a8e22-143">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8e22-144">2</span><span class="sxs-lookup"><span data-stu-id="a8e22-144">2</span></span></td>
<td><span data-ttu-id="a8e22-145">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="a8e22-145">System administrator</span></span></td>
<td><span data-ttu-id="a8e22-146"><strong>Ef verið er að nota Microsoft Dynamics 365 for Finance and Operations útgáfu 1611:</strong> skaltu sækja og setja upp KB sem virkja fartækjavinnusvæðin frá Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a8e22-146"><strong>If you're using Microsoft Dynamics 365 for Finance and Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="a8e22-147">Sjáðu eftirfarandi efnisatriði til að fá frekari upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="a8e22-147">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="a8e22-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Fartækjavinnusvæði kostnaðarstýringar</a></span><span class="sxs-lookup"><span data-stu-id="a8e22-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="a8e22-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Birgðir á lager eftir fartækjavinnusvæði</a></span><span class="sxs-lookup"><span data-stu-id="a8e22-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="a8e22-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sölupantanir fartækjavinnusvæði</a></span><span class="sxs-lookup"><span data-stu-id="a8e22-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="a8e22-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Fartækjavinnusvæði samstarfs lánardrottna</a></span><span class="sxs-lookup"><span data-stu-id="a8e22-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="a8e22-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Vinnustundafærsla verks á fartækjavinnusvæði</a></span><span class="sxs-lookup"><span data-stu-id="a8e22-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="a8e22-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Fartækjavinnusvæði útgjaldastýringar</a></span><span class="sxs-lookup"><span data-stu-id="a8e22-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8e22-154">3</span><span class="sxs-lookup"><span data-stu-id="a8e22-154">3</span></span></td>
<td><span data-ttu-id="a8e22-155">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="a8e22-155">System administrator</span></span></td>
<td><span data-ttu-id="a8e22-156">Gefa út fartækja vinnusvæði sem eru veitt af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a8e22-156">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="a8e22-157"><a href="publish-mobile-workspace.md">Birta fartækjavinnusvæði</a>
</span><span class="sxs-lookup"><span data-stu-id="a8e22-157"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8e22-158">4</span><span class="sxs-lookup"><span data-stu-id="a8e22-158">4</span></span></td>
<td><span data-ttu-id="a8e22-159">Forritari eða óháður hugbúnaðarsali (ÓHS)</span><span class="sxs-lookup"><span data-stu-id="a8e22-159">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="a8e22-160">Nota fartækja umgjörðina til að stofna sérsniðin fartækja vinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="a8e22-160">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="a8e22-161"><a href="platform/mobile-platform-home-page.md">Fartækjaverkvangur</a></span><span class="sxs-lookup"><span data-stu-id="a8e22-161"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8e22-162">5</span><span class="sxs-lookup"><span data-stu-id="a8e22-162">5</span></span></td>
<td><span data-ttu-id="a8e22-163">ÓHS</span><span class="sxs-lookup"><span data-stu-id="a8e22-163">ISV</span></span></td>
<td><span data-ttu-id="a8e22-164">Stofna virkjanlegan pakka sem inniheldur sérsniðin fartækja vinnusvæði og hala pakkanum upp í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="a8e22-164">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="a8e22-165"><a href="../deployment/create-apply-deployable-package.md">Mynda virkjanlegan pakka</a></span><span class="sxs-lookup"><span data-stu-id="a8e22-165"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8e22-166">6</span><span class="sxs-lookup"><span data-stu-id="a8e22-166">6</span></span></td>
<td><span data-ttu-id="a8e22-167">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="a8e22-167">System administrator</span></span></td>
<td><span data-ttu-id="a8e22-168">Notaðu virkjanlega pakkann sem inniheldur sérsniðin vinnusvæði frá óháðum hugbúnaðarsala (ISV).</span><span class="sxs-lookup"><span data-stu-id="a8e22-168">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="a8e22-169"><a href="../deployment/apply-deployable-package-system.md">Virkjanlegur pakki notaður</a></span><span class="sxs-lookup"><span data-stu-id="a8e22-169"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8e22-170">7</span><span class="sxs-lookup"><span data-stu-id="a8e22-170">7</span></span></td>
<td><span data-ttu-id="a8e22-171">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="a8e22-171">System administrator</span></span></td>
<td><span data-ttu-id="a8e22-172">Gefa út sérsniðið fartækja vinnusvæði sem veitt eru af ISV.</span><span class="sxs-lookup"><span data-stu-id="a8e22-172">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="a8e22-173"><a href="publish-mobile-workspace.md">Fartækjavinnusvæði birt</a></span><span class="sxs-lookup"><span data-stu-id="a8e22-173"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a8e22-174">8</span><span class="sxs-lookup"><span data-stu-id="a8e22-174">8</span></span></td>
<td><span data-ttu-id="a8e22-175">Notandi</span><span class="sxs-lookup"><span data-stu-id="a8e22-175">User</span></span></td>
<td><span data-ttu-id="a8e22-176">Sæktu og settu upp fartækjaforritið.</span><span class="sxs-lookup"><span data-stu-id="a8e22-176">Download and install the mobile app.</span></span></td>
<td><ul>
<li><span data-ttu-id="a8e22-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">Fyrir Android síma</a></span><span class="sxs-lookup"><span data-stu-id="a8e22-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">For Android phones</a></span></span></li>
<li><span data-ttu-id="a8e22-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">Fyrir iPhone síma</a></span><span class="sxs-lookup"><span data-stu-id="a8e22-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">For iPhones</a></span></span></li></ul>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a8e22-179">9</span><span class="sxs-lookup"><span data-stu-id="a8e22-179">9</span></span></td>
<td><span data-ttu-id="a8e22-180">Notandi</span><span class="sxs-lookup"><span data-stu-id="a8e22-180">User</span></span></td>
<td><span data-ttu-id="a8e22-181">Innskráning og notkun fartækjaforritsins.</span><span class="sxs-lookup"><span data-stu-id="a8e22-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="a8e22-182">Forritið hefur að geyma fartækjavinnusvæði sem hafa verið gefin út af kerfisstjóra.</span><span class="sxs-lookup"><span data-stu-id="a8e22-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="a8e22-183">Lista yfir fartækjavinnusvæði frá Microsoft má sjá á <a href="mobile-workspaces-released.md">Fartækjavinnusvæði, nýlega útgefin</a>.</span><span class="sxs-lookup"><span data-stu-id="a8e22-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

