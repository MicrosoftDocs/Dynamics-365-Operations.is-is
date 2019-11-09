---
title: Heimasíða fartækjaforrits
description: Þessi efnisgrein lýsir Finance and Operations fartækjaforritinu og veitir tengla á tilföng sem geta hjálpað til við að taka það upp í fyrirtæki þínu.
author: sericks007
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: 219bb1b5ac8360acf267fb792b8e23f961096abc
ms.sourcegitcommit: bbb64b3475eef155b3f9d1bdc440545da8a7182f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/04/2019
ms.locfileid: "2553069"
---
# <a name="mobile-app-home-page"></a><span data-ttu-id="f197b-103">Heimasíða fartækjaforrits</span><span class="sxs-lookup"><span data-stu-id="f197b-103">Mobile app home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f197b-104">Þessi efnisgrein lýsir Finance and Operations fartækjaforritinu og veitir tengla á tilföng sem geta hjálpað til við að taka það upp í fyrirtæki þínu.</span><span class="sxs-lookup"><span data-stu-id="f197b-104">This topic describes the Finance and Operations Operations mobile app and provides links to resources that can help you implement it in your organization.</span></span>

<a name="overview"></a><span data-ttu-id="f197b-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="f197b-105">Overview</span></span>
--------

<span data-ttu-id="f197b-106">Fartækjaforritið gerir fyrirtæki þínu kleift að gera viðskiptaferla aðgengilega á fartækjum.</span><span class="sxs-lookup"><span data-stu-id="f197b-106">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="f197b-107">Eftir að upplýsingatæknistjóri þinn opnar vinnusvæði á fartækjum fyrir fyrirtækið, geta notendur skráð sig inn í forritið og strax byrjað að keyra viðskiptaferli úr þeirra fartækjum.</span><span class="sxs-lookup"><span data-stu-id="f197b-107">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="f197b-108">Fartækjaforritið er með eftirfarandi eiginleika, sem geta hjálpað við að auka framleiðni:</span><span class="sxs-lookup"><span data-stu-id="f197b-108">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="f197b-109">Notendur geta skoðað, breytt og brugðist við viðskiptagögnin, jafnvel þótt netsamband fartækja þeirra sé óreglulegt eða ekkert.</span><span class="sxs-lookup"><span data-stu-id="f197b-109">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="f197b-110">Þegar tæki tengist neti á ný hlaðast upplýsingar um aðgerðir, sem gerðar voru utan nets, upp sjálfvirkt.</span><span class="sxs-lookup"><span data-stu-id="f197b-110">When a device reestablishes a network connection, offline data operations are automatically synchronized.</span></span>
- <span data-ttu-id="f197b-111">Upplýsingatæknistjóri eða forritarar geta byggja og birtið fartækja vinnusvæði sem hefur verið sniðið að þeirra fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="f197b-111">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="f197b-112">Farsímaforritið notar fyrirliggjandi kóða eigna þinna.</span><span class="sxs-lookup"><span data-stu-id="f197b-112">The app uses your existing code assets.</span></span> <span data-ttu-id="f197b-113">Þess vegna þarf ekki að færa aftur inn villuleitaraðferðir, viðskiptagrunninn eða öryggis samskipan.</span><span class="sxs-lookup"><span data-stu-id="f197b-113">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="f197b-114">Upplýsingatæknistjórar eða forritarar geta auðveldlega hannað fartækjavinnusvæði með því að nota benda-og-smella verkfærið sem er í vefbiðlaranum.</span><span class="sxs-lookup"><span data-stu-id="f197b-114">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="f197b-115">Upplýsingatæknistjórar eða forritarar geta einnig hámarka notkun vinnusvæða utan nets með því að nota Business viðskiptagrunn umgjörðina.</span><span class="sxs-lookup"><span data-stu-id="f197b-115">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="f197b-116">Þar sem gögn heldur áfram að vinna þegar tæki er utan nets, eru þín farsímaforrit áfram virk og auðug, jafnvel þó ekki tæki hafa tengingu við fasta net.</span><span class="sxs-lookup"><span data-stu-id="f197b-116">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="f197b-117">Einingar farsímaforritsins</span><span class="sxs-lookup"><span data-stu-id="f197b-117">Elements of the mobile app</span></span>
<span data-ttu-id="f197b-118">Fletting í fartækjaforritinu byggist á fjórum meginhugtökum: mælaborði, vinnusvæðum, síðum og aðgerðum.</span><span class="sxs-lookup"><span data-stu-id="f197b-118">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="f197b-119">[![Notkunarhugtök í farsímaforritinu](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="f197b-119">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="f197b-120">Þegar þú ræsir smáforritið, er farið í **Yfirlitið**.</span><span class="sxs-lookup"><span data-stu-id="f197b-120">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="f197b-121">Á mælaborðinu getur þú séð lista yfir **vinnusvæði** sem hafa verið gefin út.</span><span class="sxs-lookup"><span data-stu-id="f197b-121">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="f197b-122">Í hverri vinnusvæði getur séð lista yfir **síður** sem eru tiltæk fyrir það vinnusvæðisins.</span><span class="sxs-lookup"><span data-stu-id="f197b-122">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="f197b-123">Hægt er að framkvæma ýmsar aðgerðir á síðu.</span><span class="sxs-lookup"><span data-stu-id="f197b-123">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="f197b-124">Hér eru nokkur dæmi:</span><span class="sxs-lookup"><span data-stu-id="f197b-124">Here are some examples:</span></span>

    - <span data-ttu-id="f197b-125">Skoða ítarleg gögn.</span><span class="sxs-lookup"><span data-stu-id="f197b-125">View detailed data.</span></span>
    - <span data-ttu-id="f197b-126">Fletta á aðrar síður fyrir tengd gögn, eins og einingaupplýsingar eða línur.</span><span class="sxs-lookup"><span data-stu-id="f197b-126">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="f197b-127">Sjá lista yfir **aðgerðir** sem eru tiltækar fyrir þá síðu.</span><span class="sxs-lookup"><span data-stu-id="f197b-127">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="f197b-128">Aðgerðir gera það mögulegt að stofna eða breyta fyrirliggjandi gögnum.</span><span class="sxs-lookup"><span data-stu-id="f197b-128">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="f197b-129">Innleiðingarverk</span><span class="sxs-lookup"><span data-stu-id="f197b-129">Implementation process</span></span>
<span data-ttu-id="f197b-130">Eftirfarandi skýringarmynd sýnir ferlið fyrir innleiðingu á bæði fartækjavinnusvæðum frá Microsoft og sérsniðnum fartækjavinnusvæðum.</span><span class="sxs-lookup"><span data-stu-id="f197b-130">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

<span data-ttu-id="f197b-131">[![Innleiðingarferli farsímaforrita](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span><span class="sxs-lookup"><span data-stu-id="f197b-131">[![Mobile apps implementation process](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span></span>

<span data-ttu-id="f197b-132">Eftirfarandi tafla inniheldur tengla á tilföng sem geta hjálpað til við að innleiða bæði fartækjavinnusvæði frá Microsoft og sérsniðin fartækjavinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="f197b-132">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="f197b-133">Tölurnar í fyrsta dálkinum samsvara tölusettu skrefin í síðustu skýringarmynd.</span><span class="sxs-lookup"><span data-stu-id="f197b-133">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f197b-134">Þrep</span><span class="sxs-lookup"><span data-stu-id="f197b-134">Step</span></span></th>
<th><span data-ttu-id="f197b-135">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="f197b-135">Role</span></span></th>
<th><span data-ttu-id="f197b-136">Aðgerð</span><span class="sxs-lookup"><span data-stu-id="f197b-136">Action</span></span></th>
<th><span data-ttu-id="f197b-137">Tilföng til að hjálpa til við að ljúka aðgerð</span><span class="sxs-lookup"><span data-stu-id="f197b-137">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f197b-138">1</span><span class="sxs-lookup"><span data-stu-id="f197b-138">1</span></span></td>
<td><span data-ttu-id="f197b-139">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="f197b-139">System administrator</span></span></td>
<td><span data-ttu-id="f197b-140">Innleiða forrit Finance and Operations í þitt fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="f197b-140">Implement Finance and Operations apps in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="f197b-141">Ef þú hefur ekki enn notað útgáfu af &#39;Microsoft Dynamics 365 skaltu sjá <a href="../deployment/deploy-demo-environment.md">Virkja sýniútgáfuumhverfi</a>.</span><span class="sxs-lookup"><span data-stu-id="f197b-141">If you haven&#39;t yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="f197b-142">Lista yfir fartækjavinnusvæði sem hægt er að nota má sjá á <a href="mobile-workspaces-released.md">Fartækjavinnusvæði, nýlega útgefin</a>.</span><span class="sxs-lookup"><span data-stu-id="f197b-142">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f197b-143">2</span><span class="sxs-lookup"><span data-stu-id="f197b-143">2</span></span></td>
<td><span data-ttu-id="f197b-144">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="f197b-144">System administrator</span></span></td>
<td><span data-ttu-id="f197b-145"><strong>Ef þú &#39; ert að nota Microsoft Dynamics 365 for Operations útgáfu 1611:</strong> Sæktu og settu upp KBs sem gera kleift að nota fartækja vinnusvæði sem eru veitt af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f197b-145"><strong>If you&#39;re using Microsoft Dynamics 365 for Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="f197b-146">Sjáðu eftirfarandi efnisatriði til að fá frekari upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="f197b-146">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="f197b-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Fartækjavinnusvæði kostnaðarstýringar</a></span><span class="sxs-lookup"><span data-stu-id="f197b-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="f197b-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Birgðir á lager eftir fartækjavinnusvæði</a></span><span class="sxs-lookup"><span data-stu-id="f197b-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="f197b-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sölupantanir fartækjavinnusvæði</a></span><span class="sxs-lookup"><span data-stu-id="f197b-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="f197b-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Fartækjavinnusvæði samstarfs lánardrottna</a></span><span class="sxs-lookup"><span data-stu-id="f197b-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="f197b-151"><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">Vinnustundafærsla verks á fartækjavinnusvæði</a></span><span class="sxs-lookup"><span data-stu-id="f197b-151"><a href="../../../finance/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="f197b-152"><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">Fartækjavinnusvæði útgjaldastýringar</a></span><span class="sxs-lookup"><span data-stu-id="f197b-152"><a href="../../../finance/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f197b-153">3</span><span class="sxs-lookup"><span data-stu-id="f197b-153">3</span></span></td>
<td><span data-ttu-id="f197b-154">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="f197b-154">System administrator</span></span></td>
<td><span data-ttu-id="f197b-155">Gefa út fartækja vinnusvæði sem eru veitt af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="f197b-155">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="f197b-156"><a href="publish-mobile-workspace.md">Birta fartækjavinnusvæði</a>
</span><span class="sxs-lookup"><span data-stu-id="f197b-156"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f197b-157">4</span><span class="sxs-lookup"><span data-stu-id="f197b-157">4</span></span></td>
<td><span data-ttu-id="f197b-158">Forritari eða óháður hugbúnaðarsali (ÓHS)</span><span class="sxs-lookup"><span data-stu-id="f197b-158">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="f197b-159">Nota fartækja umgjörðina til að stofna sérsniðin fartækja vinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="f197b-159">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="f197b-160"><a href="platform/mobile-platform-home-page.md">Fartækjaverkvangur</a></span><span class="sxs-lookup"><span data-stu-id="f197b-160"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f197b-161">5</span><span class="sxs-lookup"><span data-stu-id="f197b-161">5</span></span></td>
<td><span data-ttu-id="f197b-162">ÓHS</span><span class="sxs-lookup"><span data-stu-id="f197b-162">ISV</span></span></td>
<td><span data-ttu-id="f197b-163">Stofna virkjanlegan pakka sem inniheldur sérsniðin fartækja vinnusvæði og hala pakkanum upp í Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="f197b-163">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="f197b-164"><a href="../deployment/create-apply-deployable-package.md">Virkjanlegur pakki búinn til</a></span><span class="sxs-lookup"><span data-stu-id="f197b-164"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f197b-165">6</span><span class="sxs-lookup"><span data-stu-id="f197b-165">6</span></span></td>
<td><span data-ttu-id="f197b-166">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="f197b-166">System administrator</span></span></td>
<td><span data-ttu-id="f197b-167">Notaðu virkjanlega pakkann sem inniheldur sérsniðin vinnusvæði frá óháðum hugbúnaðarsala (ISV).</span><span class="sxs-lookup"><span data-stu-id="f197b-167">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="f197b-168"><a href="../deployment/apply-deployable-package-system.md">Virkjanlegur pakki notaður</a></span><span class="sxs-lookup"><span data-stu-id="f197b-168"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f197b-169">7</span><span class="sxs-lookup"><span data-stu-id="f197b-169">7</span></span></td>
<td><span data-ttu-id="f197b-170">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="f197b-170">System administrator</span></span></td>
<td><span data-ttu-id="f197b-171">Gefa út sérsniðið fartækja vinnusvæði sem veitt eru af ISV.</span><span class="sxs-lookup"><span data-stu-id="f197b-171">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="f197b-172"><a href="publish-mobile-workspace.md">Birta fartækjavinnusvæði</a></span><span class="sxs-lookup"><span data-stu-id="f197b-172"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f197b-173">8</span><span class="sxs-lookup"><span data-stu-id="f197b-173">8</span></span></td>
<td><span data-ttu-id="f197b-174">Notandi</span><span class="sxs-lookup"><span data-stu-id="f197b-174">User</span></span></td>
<td><span data-ttu-id="f197b-175">Sæktu og settu upp fartækjaforritið.</span><span class="sxs-lookup"><span data-stu-id="f197b-175">Download and install the mobile app.</span></span></td>
<td><span data-ttu-id="f197b-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Forrit Finance and Operations fyrir Android</a></span><span class="sxs-lookup"><span data-stu-id="f197b-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations app for Android</a></span></span><BR/><span data-ttu-id="f197b-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Forrit Finance and Operations fyrir iOS</a></span><span class="sxs-lookup"><span data-stu-id="f197b-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations app for iOS</a></span></span><BR/>
<span data-ttu-id="f197b-178">(Styður ekki Windows Phone)</span><span class="sxs-lookup"><span data-stu-id="f197b-178">(Windows Phone unsupported)</span></span>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f197b-179">9</span><span class="sxs-lookup"><span data-stu-id="f197b-179">9</span></span></td>
<td><span data-ttu-id="f197b-180">Notandi</span><span class="sxs-lookup"><span data-stu-id="f197b-180">User</span></span></td>
<td><span data-ttu-id="f197b-181">Innskráning og notkun fartækjaforritsins.</span><span class="sxs-lookup"><span data-stu-id="f197b-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="f197b-182">Forritið hefur að geyma fartækjavinnusvæði sem hafa verið gefin út af kerfisstjóra.</span><span class="sxs-lookup"><span data-stu-id="f197b-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="f197b-183">Lista yfir fartækjavinnusvæði frá Microsoft má sjá á <a href="mobile-workspaces-released.md">Fartækjavinnusvæði, nýlega útgefin</a>.</span><span class="sxs-lookup"><span data-stu-id="f197b-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>