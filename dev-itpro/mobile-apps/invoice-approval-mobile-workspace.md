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
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 24818afbbdf328c8fd3eea691634db24e443b07b
ms.contentlocale: is-is
ms.lasthandoff: 07/18/2017

---

# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="0d2f6-104">Reikningssamþykktir á fartækjavinnusvæðum</span><span class="sxs-lookup"><span data-stu-id="0d2f6-104">Invoice approvals mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0d2f6-105">Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið **Reikningsssamþykktir**.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="0d2f6-106">Þessi vinnusvæði gefur lista yfir reikninga sem hafa verið úthlutaðir þér í gegnum verkflæði reikningshauss lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="0d2f6-107">Þetta fartækjavinnusvæði er ætlað til notkunar með fartækjaforritinu Microsoft Dynamics 365 for Unified Operations.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="0d2f6-108">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="0d2f6-108">Overview</span></span>

<span data-ttu-id="0d2f6-109">Fartækjavinnusvæðið **Reikningssamþykktir** gerir gjaldkerum og stjórnendum í viðskiptaskuldum kleift að skoða reikninga sem hafa verið úthlutaðir þeim sem hluti af verkflæði reikningshauss lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="0d2f6-110">Hægt er að skoða reikningsupplýsingar, jafnvel línur og skiptingu, til að hjálpa þér að taka upplýstar ákvarðanir við samþykktir.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="0d2f6-111">Úr vinnusvæðinu getur þú hreyft reikninginn í gegnum verkflæðisferlið.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="0d2f6-112">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="0d2f6-112">Prerequisites</span></span>

<span data-ttu-id="0d2f6-113">Áður en hægt er að nota þetta fartækjavinnusvæði, verður að uppfylla eftirtaldar forsendur.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="0d2f6-114">Skilyrði</span><span class="sxs-lookup"><span data-stu-id="0d2f6-114">Prerequisite</span></span></th>
<th><span data-ttu-id="0d2f6-115">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="0d2f6-115">Role</span></span></th>
<th><span data-ttu-id="0d2f6-116">lýsing</span><span class="sxs-lookup"><span data-stu-id="0d2f6-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0d2f6-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise útgáfa, uppfærsla í júlí 2017, verður að vera í notkun í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition July 2017 update must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="0d2f6-118">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="0d2f6-118">System administrator</span></span></td>
<td><span data-ttu-id="0d2f6-119">Sjá <a href="../deployment/deploy-demo-environment.md">Uppsetning sýniútgáfuumhverfis</a>.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="0d2f6-120">Það verður að birta fartækjavinnusvæðið <strong>Reikningssamþykktir</strong>.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="0d2f6-121">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="0d2f6-121">System administrator</span></span></td>
<td><span data-ttu-id="0d2f6-122">Sjáið <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Fartækjavinnusvæði birt</a>.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-122">See <a href="/dynamics365/unified-operations/dev-itpro/mobile-apps/publish-mobile-workspace">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="0d2f6-123">Sæktu og settu upp fartækjaforritið</span><span class="sxs-lookup"><span data-stu-id="0d2f6-123">Download and install the mobile app</span></span>

<span data-ttu-id="0d2f6-124">Sæktu og settu upp fartækjaforritið Dynamics 365 for Unified Operations:</span><span class="sxs-lookup"><span data-stu-id="0d2f6-124">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="0d2f6-125">Fyrir Android síma</span><span class="sxs-lookup"><span data-stu-id="0d2f6-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="0d2f6-126">Fyrir iPhone síma</span><span class="sxs-lookup"><span data-stu-id="0d2f6-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="0d2f6-127">Innskráning í fartækjaforritið</span><span class="sxs-lookup"><span data-stu-id="0d2f6-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="0d2f6-128">Ræstu forritið í fartækinu þínu.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="0d2f6-129">Færðu inn vefslóð þína fyrir Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="0d2f6-130">Í fyrsta sinn sem þú skráir þig inn, er beðið um notandanafn og aðgangsorð þitt.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="0d2f6-131">Færðu inn skilríki</span><span class="sxs-lookup"><span data-stu-id="0d2f6-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="0d2f6-132">Eftir að þú hefur skráð þig inn, birtast tiltæk vinnusvæði fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="0d2f6-133">Athugið að ef kerfisstjóri gefur út nýtt vinnusvæði síðar, verður að endurræsa listann yfir fartækjavinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="0d2f6-134">[![Togið upp til að uppfæra](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="0d2f6-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="0d2f6-135">Samþykkja reikninga með því að nota fartækjavinnusvæðið Reikningssamþykktir</span><span class="sxs-lookup"><span data-stu-id="0d2f6-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="0d2f6-136">Í fartækinu velurðu vinnusvæðið **Reikningssamþykktir**.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="0d2f6-137">Veldu þann reikning sem þér hefur verið úthlutaður af verkflæði reikningshauss lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="0d2f6-138">Skoðaðu hausupplýsingar reikningsins á síðunni **Reikningsupplýsingar**, eins og upplýsingar um lánardrottinn og dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="0d2f6-139">Veldu línu á reikningi til að skoða nákvæmari upplýsingar um hann í yfirlitinu **Upplýsingar um reikningslínur**.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="0d2f6-140">Í yfirlitinu **Upplýsingar um reikningslínur** skaltu velja **Skiptingu** til að sýna línuskiptingar.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="0d2f6-141">Hérna getur þú skoðað bókhald fyrir reikningslínuna.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="0d2f6-142">Á meðal upplýsinga sem eru sýndar eru fjárhagsvíddir og aðallykill.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="0d2f6-143">Á síðunni **Reikningsupplýsingar** skaltu velja **Skiptingu** til að sýna allar línuskiptingar.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="0d2f6-144">Hérna getur þú skoðað bókhald fyrir allan reikninginn.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="0d2f6-145">Á meðal upplýsinga sem eru sýndar eru fjárhagsvíddir og aðallyklar.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="0d2f6-146">Veldu **Viðhengi** til að skoða athugasemdir eða skrár sem tengjast reikningnum.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="0d2f6-147">Á síðunni **Reikningsupplýsingar** velurðu viðeigandi verkflæðisaðgerð til að ljúka við endurskoðunarferli þitt.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="0d2f6-148">Velja **Ekkert**.</span><span class="sxs-lookup"><span data-stu-id="0d2f6-148">Select **Done**.</span></span>

