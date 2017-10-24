---
title: "Reikningssamþykktir á fartækjavinnusvæðum"
description: "Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið Reikningssamþykktir. Þessi vinnusvæði gefur lista yfir reikninga sem hafa verið úthlutaðir þér í gegnum verkflæði reikningshauss lánardrottins."
author: abruer
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: c73eeaaf28df8db720431d4bcd317c9721baa99d
ms.openlocfilehash: 190f48f4d5e304902b701f74f2cbefcbe7b36b15
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="6189c-104">Reikningssamþykktir á fartækjavinnusvæðum</span><span class="sxs-lookup"><span data-stu-id="6189c-104">Invoice approvals mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6189c-105">Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið **Reikningsssamþykktir**.</span><span class="sxs-lookup"><span data-stu-id="6189c-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="6189c-106">Þessi vinnusvæði gefur lista yfir reikninga sem hafa verið úthlutaðir þér í gegnum verkflæði reikningshauss lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="6189c-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="6189c-107">Þetta fartækjavinnusvæði er ætlað til notkunar með fartækjaforritinu Microsoft Dynamics 365 for Unified Operations.</span><span class="sxs-lookup"><span data-stu-id="6189c-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="6189c-108">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="6189c-108">Overview</span></span>

<span data-ttu-id="6189c-109">Fartækjavinnusvæðið **Reikningssamþykktir** gerir gjaldkerum og stjórnendum í viðskiptaskuldum kleift að skoða reikninga sem hafa verið úthlutaðir þeim sem hluti af verkflæði reikningshauss lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="6189c-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="6189c-110">Hægt er að skoða reikningsupplýsingar, jafnvel línur og skiptingu, til að hjálpa þér að taka upplýstar ákvarðanir við samþykktir.</span><span class="sxs-lookup"><span data-stu-id="6189c-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="6189c-111">Úr vinnusvæðinu getur þú hreyft reikninginn í gegnum verkflæðisferlið.</span><span class="sxs-lookup"><span data-stu-id="6189c-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="6189c-112">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="6189c-112">Prerequisites</span></span>

<span data-ttu-id="6189c-113">Áður en hægt er að nota þetta fartækjavinnusvæði, verður að uppfylla eftirtaldar forsendur.</span><span class="sxs-lookup"><span data-stu-id="6189c-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6189c-114">Skilyrði</span><span class="sxs-lookup"><span data-stu-id="6189c-114">Prerequisite</span></span></th>
<th><span data-ttu-id="6189c-115">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="6189c-115">Role</span></span></th>
<th><span data-ttu-id="6189c-116">lýsing</span><span class="sxs-lookup"><span data-stu-id="6189c-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6189c-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (júlí 2017) verður að vera virkt í fyrirtækinu þínu.</span><span class="sxs-lookup"><span data-stu-id="6189c-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="6189c-118">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="6189c-118">System administrator</span></span></td>
<td><span data-ttu-id="6189c-119">Sjá <a href="../deployment/deploy-demo-environment.md">Uppsetning sýniútgáfuumhverfis</a>.</span><span class="sxs-lookup"><span data-stu-id="6189c-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="6189c-120">Það verður að birta fartækjavinnusvæðið <strong>Reikningssamþykktir</strong>.</span><span class="sxs-lookup"><span data-stu-id="6189c-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="6189c-121">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="6189c-121">System administrator</span></span></td>
<td><span data-ttu-id="6189c-122">Sjáið <a href="publish-mobile-workspace.md">Fartækjavinnusvæði birt</a>.</span><span class="sxs-lookup"><span data-stu-id="6189c-122">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="6189c-123">Sæktu og settu upp fartækjaforritið</span><span class="sxs-lookup"><span data-stu-id="6189c-123">Download and install the mobile app</span></span>

<span data-ttu-id="6189c-124">Sæktu og settu upp fartækjaforritið Dynamics 365 for Unified Operations:</span><span class="sxs-lookup"><span data-stu-id="6189c-124">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="6189c-125">Fyrir Android síma</span><span class="sxs-lookup"><span data-stu-id="6189c-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="6189c-126">Fyrir iPhone síma</span><span class="sxs-lookup"><span data-stu-id="6189c-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="6189c-127">Innskráning í fartækjaforritið</span><span class="sxs-lookup"><span data-stu-id="6189c-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="6189c-128">Ræstu forritið í fartækinu þínu.</span><span class="sxs-lookup"><span data-stu-id="6189c-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="6189c-129">Færðu inn vefslóð þína fyrir Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6189c-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="6189c-130">Í fyrsta sinn sem þú skráir þig inn, er beðið um notandanafn og aðgangsorð þitt.</span><span class="sxs-lookup"><span data-stu-id="6189c-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="6189c-131">Færðu inn skilríki</span><span class="sxs-lookup"><span data-stu-id="6189c-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="6189c-132">Eftir að þú hefur skráð þig inn, birtast tiltæk vinnusvæði fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="6189c-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="6189c-133">Athugið að ef kerfisstjóri gefur út nýtt vinnusvæði síðar, verður að endurræsa listann yfir fartækjavinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="6189c-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="6189c-134">[![Togið upp til að uppfæra](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="6189c-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="6189c-135">Samþykkja reikninga með því að nota fartækjavinnusvæðið Reikningssamþykktir</span><span class="sxs-lookup"><span data-stu-id="6189c-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="6189c-136">Í fartækinu velurðu vinnusvæðið **Reikningssamþykktir**.</span><span class="sxs-lookup"><span data-stu-id="6189c-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="6189c-137">Veldu þann reikning sem þér hefur verið úthlutaður af verkflæði reikningshauss lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="6189c-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="6189c-138">Skoðaðu hausupplýsingar reikningsins á síðunni **Reikningsupplýsingar**, eins og upplýsingar um lánardrottinn og dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="6189c-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="6189c-139">Veldu línu á reikningi til að skoða nákvæmari upplýsingar um hann í yfirlitinu **Upplýsingar um reikningslínur**.</span><span class="sxs-lookup"><span data-stu-id="6189c-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="6189c-140">Í yfirlitinu **Upplýsingar um reikningslínur** skaltu velja **Skiptingu** til að sýna línuskiptingar.</span><span class="sxs-lookup"><span data-stu-id="6189c-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="6189c-141">Hérna getur þú skoðað bókhald fyrir reikningslínuna.</span><span class="sxs-lookup"><span data-stu-id="6189c-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="6189c-142">Á meðal upplýsinga sem eru sýndar eru fjárhagsvíddir og aðallykill.</span><span class="sxs-lookup"><span data-stu-id="6189c-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="6189c-143">Á síðunni **Reikningsupplýsingar** skaltu velja **Skiptingu** til að sýna allar línuskiptingar.</span><span class="sxs-lookup"><span data-stu-id="6189c-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="6189c-144">Hérna getur þú skoðað bókhald fyrir allan reikninginn.</span><span class="sxs-lookup"><span data-stu-id="6189c-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="6189c-145">Á meðal upplýsinga sem eru sýndar eru fjárhagsvíddir og aðallyklar.</span><span class="sxs-lookup"><span data-stu-id="6189c-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="6189c-146">Veldu **Viðhengi** til að skoða athugasemdir eða skrár sem tengjast reikningnum.</span><span class="sxs-lookup"><span data-stu-id="6189c-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="6189c-147">Á síðunni **Reikningsupplýsingar** velurðu viðeigandi verkflæðisaðgerð til að ljúka við endurskoðunarferli þitt.</span><span class="sxs-lookup"><span data-stu-id="6189c-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="6189c-148">Velja **Ekkert**.</span><span class="sxs-lookup"><span data-stu-id="6189c-148">Select **Done**.</span></span>

