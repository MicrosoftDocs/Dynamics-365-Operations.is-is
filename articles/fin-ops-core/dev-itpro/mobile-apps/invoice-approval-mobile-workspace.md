---
title: Reikningssamþykktir á fartækjavinnusvæðum
description: Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið Reikningssamþykktir.
author: abruer
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: c3414d6ef5f2df62f37f1ef2e7e2ff43ce040e5e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752251"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="bbf6b-103">Reikningssamþykktir á fartækjavinnusvæðum</span><span class="sxs-lookup"><span data-stu-id="bbf6b-103">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bbf6b-104">Þetta efnisatriði veitir upplýsingar um fartækjavinnusvæðið **Reikningsssamþykktir**.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-104">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="bbf6b-105">Þessi vinnusvæði gefur lista yfir reikninga sem hafa verið úthlutaðir þér í gegnum verkflæði reikningshauss lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-105">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="bbf6b-106">Þetta fartækjavinnusvæði er ætlað til að nota með farsímaforritið Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-106">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="bbf6b-107">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="bbf6b-107">Overview</span></span>

<span data-ttu-id="bbf6b-108">Fartækjavinnusvæðið **Reikningssamþykktir** gerir gjaldkerum og stjórnendum í viðskiptaskuldum kleift að skoða reikninga sem hafa verið úthlutaðir þeim sem hluti af verkflæði reikningshauss lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-108">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="bbf6b-109">Hægt er að skoða reikningsupplýsingar, jafnvel línur og skiptingu, til að hjálpa þér að taka upplýstar ákvarðanir við samþykktir.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-109">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="bbf6b-110">Úr vinnusvæðinu getur þú hreyft reikninginn í gegnum verkflæðisferlið.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-110">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="bbf6b-111">Frumskilyrði</span><span class="sxs-lookup"><span data-stu-id="bbf6b-111">Prerequisites</span></span>

<span data-ttu-id="bbf6b-112">Áður en hægt er að nota þetta fartækjavinnusvæði, verður að uppfylla eftirtaldar forsendur.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-112">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="bbf6b-113">Skilyrði</span><span class="sxs-lookup"><span data-stu-id="bbf6b-113">Prerequisite</span></span></th>
<th><span data-ttu-id="bbf6b-114">Hlutverk</span><span class="sxs-lookup"><span data-stu-id="bbf6b-114">Role</span></span></th>
<th><span data-ttu-id="bbf6b-115">Lýsing</span><span class="sxs-lookup"><span data-stu-id="bbf6b-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bbf6b-116">Microsoft Dynamics 365 Finance verður að vera innleitt í fyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-116">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="bbf6b-117">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="bbf6b-117">System administrator</span></span></td>
<td><span data-ttu-id="bbf6b-118">Sjá <a href="../deployment/deploy-demo-environment.md">Uppsetning sýniútgáfuumhverfis</a>.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-118">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="bbf6b-119">Það verður að birta fartækjavinnusvæðið <strong>Reikningssamþykktir</strong>.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-119">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="bbf6b-120">Kerfisstjóri</span><span class="sxs-lookup"><span data-stu-id="bbf6b-120">System administrator</span></span></td>
<td><span data-ttu-id="bbf6b-121">Sjáið <a href="publish-mobile-workspace.md">Fartækjavinnusvæði birt</a>.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-121">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="bbf6b-122">Sæktu og settu upp fartækjaforritið</span><span class="sxs-lookup"><span data-stu-id="bbf6b-122">Download and install the mobile app</span></span>

<span data-ttu-id="bbf6b-123">Sæktu og settu upp fartækjaforritið Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="bbf6b-123">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="bbf6b-124">Fyrir Android síma</span><span class="sxs-lookup"><span data-stu-id="bbf6b-124">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="bbf6b-125">Fyrir iPhone síma</span><span class="sxs-lookup"><span data-stu-id="bbf6b-125">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="bbf6b-126">Innskráning í fartækjaforritið</span><span class="sxs-lookup"><span data-stu-id="bbf6b-126">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="bbf6b-127">Ræstu forritið í fartækinu þínu.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-127">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="bbf6b-128">Færðu inn vefslóð þína fyrir Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-128">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="bbf6b-129">Í fyrsta sinn sem þú skráir þig inn, er beðið um notandanafn og aðgangsorð þitt.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-129">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="bbf6b-130">Færðu inn skilríki</span><span class="sxs-lookup"><span data-stu-id="bbf6b-130">Enter your credentials.</span></span>
4.  <span data-ttu-id="bbf6b-131">Eftir að þú hefur skráð þig inn, birtast tiltæk vinnusvæði fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-131">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="bbf6b-132">Athugið að ef kerfisstjóri gefur út nýtt vinnusvæði síðar, verður að endurræsa listann yfir fartækjavinnusvæði.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-132">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="bbf6b-133">[![Togið upp til að uppfæra](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="bbf6b-133">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="bbf6b-134">Samþykkja reikninga með því að nota fartækjavinnusvæðið Reikningssamþykktir</span><span class="sxs-lookup"><span data-stu-id="bbf6b-134">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="bbf6b-135">Í fartækinu velurðu vinnusvæðið **Reikningssamþykktir**.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-135">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="bbf6b-136">Veldu þann reikning sem þér hefur verið úthlutaður af verkflæði reikningshauss lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-136">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="bbf6b-137">Skoðaðu hausupplýsingar reikningsins á síðunni **Reikningsupplýsingar**, eins og upplýsingar um lánardrottinn og dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-137">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="bbf6b-138">Veldu línu á reikningi til að skoða nákvæmari upplýsingar um hann í yfirlitinu **Upplýsingar um reikningslínur**.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-138">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="bbf6b-139">Í yfirlitinu **Upplýsingar um reikningslínur** skaltu velja **Skiptingu** til að sýna línuskiptingar.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-139">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="bbf6b-140">Hérna getur þú skoðað bókhald fyrir reikningslínuna.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-140">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="bbf6b-141">Á meðal upplýsinga sem eru sýndar eru fjárhagsvíddir og aðallykill.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-141">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="bbf6b-142">Á síðunni **Reikningsupplýsingar** skaltu velja **Skiptingu** til að sýna allar línuskiptingar.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-142">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="bbf6b-143">Hérna getur þú skoðað bókhald fyrir allan reikninginn.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-143">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="bbf6b-144">Á meðal upplýsinga sem eru sýndar eru fjárhagsvíddir og aðallyklar.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-144">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="bbf6b-145">Veldu **Viðhengi** til að skoða athugasemdir eða skrár sem tengjast reikningnum.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-145">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="bbf6b-146">Á síðunni **Reikningsupplýsingar** velurðu viðeigandi verkflæðisaðgerð til að ljúka við endurskoðunarferli þitt.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-146">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="bbf6b-147">Velja **Ekkert**.</span><span class="sxs-lookup"><span data-stu-id="bbf6b-147">Select **Done**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]