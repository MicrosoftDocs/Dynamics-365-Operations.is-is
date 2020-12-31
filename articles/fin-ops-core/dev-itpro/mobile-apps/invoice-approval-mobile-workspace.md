---
title: Reikningssamþykktir á fartækjavinnusvæðum
description: Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið Reikningssamþykktir. Þessi vinnusvæði gefur lista yfir reikninga sem hafa verið úthlutaðir þér í gegnum verkflæði reikningshauss lánardrottins.
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 8d4b40c7ce8939248e85b6b6f3d359bd16e35b0d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683409"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="606d3-104">Reikningssamþykktir á fartækjavinnusvæðum</span><span class="sxs-lookup"><span data-stu-id="606d3-104">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="606d3-105">Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið **Reikningsssamþykktir**.</span><span class="sxs-lookup"><span data-stu-id="606d3-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="606d3-106">Þessi vinnusvæði gefur lista yfir reikninga sem hafa verið úthlutaðir þér í gegnum verkflæði reikningshauss lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="606d3-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="606d3-107">Þetta fartækjavinnusvæði er ætlað til að nota með farsímaforritið Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="606d3-107">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="606d3-108">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="606d3-108">Overview</span></span>

<span data-ttu-id="606d3-109">Fartækjavinnusvæðið **Reikningssamþykktir** gerir gjaldkerum og stjórnendum í viðskiptaskuldum kleift að skoða reikninga sem hafa verið úthlutaðir þeim sem hluti af verkflæði reikningshauss lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="606d3-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="606d3-110">Hægt er að skoða reikningsupplýsingar, jafnvel línur og skiptingu, til að hjálpa þér að taka upplýstar ákvarðanir við samþykktir.</span><span class="sxs-lookup"><span data-stu-id="606d3-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="606d3-111">Úr vinnusvæðinu getur þú hreyft reikninginn í gegnum verkflæðisferlið.</span><span class="sxs-lookup"><span data-stu-id="606d3-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="606d3-112">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="606d3-112">Prerequisites</span></span>

<span data-ttu-id="606d3-113">Áður en hægt er að nota þetta fartækjavinnusvæði, verður að uppfylla eftirtaldar forsendur.</span><span class="sxs-lookup"><span data-stu-id="606d3-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="606d3-114">Skilyrði</span><span class="sxs-lookup"><span data-stu-id="606d3-114">Prerequisite</span></span></th>
<th><span data-ttu-id="606d3-115">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="606d3-115">Role</span></span></th>
<th><span data-ttu-id="606d3-116">Lýsing</span><span class="sxs-lookup"><span data-stu-id="606d3-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="606d3-117">Microsoft Dynamics 365 Finance verður að vera innleitt í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="606d3-117">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="606d3-118">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="606d3-118">System administrator</span></span></td>
<td><span data-ttu-id="606d3-119">Sjá <a href="../deployment/deploy-demo-environment.md">Uppsetning sýniútgáfuumhverfis</a>.</span><span class="sxs-lookup"><span data-stu-id="606d3-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="606d3-120">Það verður að birta fartækjavinnusvæðið <strong>Reikningssamþykktir</strong>.</span><span class="sxs-lookup"><span data-stu-id="606d3-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="606d3-121">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="606d3-121">System administrator</span></span></td>
<td><span data-ttu-id="606d3-122">Sjáið <a href="publish-mobile-workspace.md">Fartækjavinnusvæði birt</a>.</span><span class="sxs-lookup"><span data-stu-id="606d3-122">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="606d3-123">Sæktu og settu upp fartækjaforritið</span><span class="sxs-lookup"><span data-stu-id="606d3-123">Download and install the mobile app</span></span>

<span data-ttu-id="606d3-124">Sæktu og settu upp fartækjaforritið Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="606d3-124">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="606d3-125">Fyrir Android síma</span><span class="sxs-lookup"><span data-stu-id="606d3-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="606d3-126">Fyrir iPhone síma</span><span class="sxs-lookup"><span data-stu-id="606d3-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="606d3-127">Innskráning í fartækjaforritið</span><span class="sxs-lookup"><span data-stu-id="606d3-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="606d3-128">Ræstu forritið í fartækinu þínu.</span><span class="sxs-lookup"><span data-stu-id="606d3-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="606d3-129">Færðu inn vefslóð þína fyrir Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="606d3-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="606d3-130">Í fyrsta sinn sem þú skráir þig inn, er beðið um notandanafn og aðgangsorð þitt.</span><span class="sxs-lookup"><span data-stu-id="606d3-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="606d3-131">Færðu inn skilríki</span><span class="sxs-lookup"><span data-stu-id="606d3-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="606d3-132">Eftir að þú hefur skráð þig inn, birtast tiltæk vinnusvæði fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="606d3-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="606d3-133">Athugið að ef kerfisstjóri gefur út nýtt vinnusvæði síðar, verður að endurræsa listann yfir fartækjavinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="606d3-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="606d3-134">[![Togið upp til að uppfæra](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="606d3-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="606d3-135">Samþykkja reikninga með því að nota fartækjavinnusvæðið Reikningssamþykktir</span><span class="sxs-lookup"><span data-stu-id="606d3-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="606d3-136">Í fartækinu velurðu vinnusvæðið **Reikningssamþykktir**.</span><span class="sxs-lookup"><span data-stu-id="606d3-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="606d3-137">Veldu þann reikning sem þér hefur verið úthlutaður af verkflæði reikningshauss lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="606d3-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="606d3-138">Skoðaðu hausupplýsingar reikningsins á síðunni **Reikningsupplýsingar**, eins og upplýsingar um lánardrottinn og dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="606d3-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="606d3-139">Veldu línu á reikningi til að skoða nákvæmari upplýsingar um hann í yfirlitinu **Upplýsingar um reikningslínur**.</span><span class="sxs-lookup"><span data-stu-id="606d3-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="606d3-140">Í yfirlitinu **Upplýsingar um reikningslínur** skaltu velja **Skiptingu** til að sýna línuskiptingar.</span><span class="sxs-lookup"><span data-stu-id="606d3-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="606d3-141">Hérna getur þú skoðað bókhald fyrir reikningslínuna.</span><span class="sxs-lookup"><span data-stu-id="606d3-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="606d3-142">Á meðal upplýsinga sem eru sýndar eru fjárhagsvíddir og aðallykill.</span><span class="sxs-lookup"><span data-stu-id="606d3-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="606d3-143">Á síðunni **Reikningsupplýsingar** skaltu velja **Skiptingu** til að sýna allar línuskiptingar.</span><span class="sxs-lookup"><span data-stu-id="606d3-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="606d3-144">Hérna getur þú skoðað bókhald fyrir allan reikninginn.</span><span class="sxs-lookup"><span data-stu-id="606d3-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="606d3-145">Á meðal upplýsinga sem eru sýndar eru fjárhagsvíddir og aðallyklar.</span><span class="sxs-lookup"><span data-stu-id="606d3-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="606d3-146">Veldu **Viðhengi** til að skoða athugasemdir eða skrár sem tengjast reikningnum.</span><span class="sxs-lookup"><span data-stu-id="606d3-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="606d3-147">Á síðunni **Reikningsupplýsingar** velurðu viðeigandi verkflæðisaðgerð til að ljúka við endurskoðunarferli þitt.</span><span class="sxs-lookup"><span data-stu-id="606d3-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="606d3-148">Velja **Ekkert**.</span><span class="sxs-lookup"><span data-stu-id="606d3-148">Select **Done**.</span></span>
