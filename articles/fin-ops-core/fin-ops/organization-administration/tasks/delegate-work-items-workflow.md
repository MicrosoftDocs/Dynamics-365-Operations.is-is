---
title: Úthluta vinnuliðir í verkflæði
description: Ef þú verður ekki á skrifstofunni í einhvern tíma eða munt ekki vera tiltækur til að bregðast við vinnulið getur þú úthlutað, eða endurúthlutað vinnuliðunum, til annars notanda.
author: ChrisGarty
ms.date: 07/07/2020
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed21f6d32cdcf74eb153daba32c20b7cef94d4e4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747370"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="202b1-103">Úthluta vinnuliðum í verkflæði</span><span class="sxs-lookup"><span data-stu-id="202b1-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="202b1-104">Úthluta vinnulið handvirkt</span><span class="sxs-lookup"><span data-stu-id="202b1-104">Manually delegate a work item</span></span>

<span data-ttu-id="202b1-105">Til að úthluta einstökum vinnulið skal velja valkostinn **Úthluta** í valmyndinni **Verkflæði** og síðan færa inn notandann sem úthluta á til ásamt athugasemd.</span><span class="sxs-lookup"><span data-stu-id="202b1-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="202b1-106">Þetta mun endurúthluta vinnuliðnum á þann notanda svo hann geti lokið vinnunni.</span><span class="sxs-lookup"><span data-stu-id="202b1-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="manually-delegate-multiple-work-items"></a><span data-ttu-id="202b1-107">Úthluta mörgum vinnuliðum handvirkt</span><span class="sxs-lookup"><span data-stu-id="202b1-107">Manually delegate multiple work items</span></span>

<span data-ttu-id="202b1-108">Hægt er að úthluta mörgum vinnuliðum saman á síðunni **Vinnuliðum sem mér er úthlutað**.</span><span class="sxs-lookup"><span data-stu-id="202b1-108">Multiple work items can be delegated together from the **Work items assigned to me** page.</span></span> <span data-ttu-id="202b1-109">Eftirfarandi verkflæðisgerðir er hægt að fjöldaúthluta: innkaupasamningur, samþykktarverkflæði, verkflæði innkaupapöntunar, yfirferð innkaupabeiðni og verkflæði lánardrottnareiknings.</span><span class="sxs-lookup"><span data-stu-id="202b1-109">The following workflow types are eligible for mass delegation: Purchase agreement approval workflow, Purchase order workflow, Purchase requisition review, and Vendor invoice workflow.</span></span> <span data-ttu-id="202b1-110">Slökkt er á eiginleikanum **Úthluta mörgum vinnuliðum** að sjálfgefnu og hægt er að virkja hann í **Vinnusvæði > Eiginleikastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="202b1-110">The **Delegate multiple work items** feature is disabled by default and can be enabled in **Workspaces > Feature management**.</span></span> <span data-ttu-id="202b1-111">Hafið samband við kerfisstjóra til að fá aðstoð við að kveikja á eiginleikanum.</span><span class="sxs-lookup"><span data-stu-id="202b1-111">Contact your system administrator for help with enabling this feature.</span></span>
1.  <span data-ttu-id="202b1-112">Farið á **Algengt > Algengt > Vinnuliðir > Vinnuliðir sem úthlutað er á mig**.</span><span class="sxs-lookup"><span data-stu-id="202b1-112">Go to **Common > Common > Work items > Work items assigned to me**.</span></span>
2.  <span data-ttu-id="202b1-113">Veljið vinnuliði sem verður úthlutað.</span><span class="sxs-lookup"><span data-stu-id="202b1-113">Select the work items that will be delegated.</span></span>
3.  <span data-ttu-id="202b1-114">Smellið á valmyndina **Úthluta vinnuliðum**.</span><span class="sxs-lookup"><span data-stu-id="202b1-114">Click the **Delegate work items** menu.</span></span>
4.  <span data-ttu-id="202b1-115">Í reitnum **Notandi** skal velja notandann sem á að úthluta vinnuliði á.</span><span class="sxs-lookup"><span data-stu-id="202b1-115">In the **User** field, select the user to delegate the work items to.</span></span>
5.  <span data-ttu-id="202b1-116">Í reitnum **Athugasemd** skal færa inn athugasemd og útskýra hvers vegna vinnuliðum er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="202b1-116">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>
6.  <span data-ttu-id="202b1-117">Smellið á hnappinn **Úthluta vinnuliðum** til að ljúka úthlutun vinnuliðar.</span><span class="sxs-lookup"><span data-stu-id="202b1-117">Click the **Delegate work items** button to complete the work item delegation.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="202b1-118">Úthluta vinnuliðum sjálfvirkt</span><span class="sxs-lookup"><span data-stu-id="202b1-118">Automatically delegate work items</span></span>

<span data-ttu-id="202b1-119">Ef þú verður ekki á skrifstofunni í einhvern tíma eða munt ekki vera tiltækur til að bregðast við vinnuliðum yfir eitthvert tímabil getur þú úthlutað nýjum vinnuliðum sjálfvirkt á aðra notendur með því að nota síðuna **Valkostir notanda**.</span><span class="sxs-lookup"><span data-stu-id="202b1-119">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="202b1-120">Setja upp sjálfvirka úthlutun</span><span class="sxs-lookup"><span data-stu-id="202b1-120">Set up automatic delegation</span></span>
1. <span data-ttu-id="202b1-121">Farðu í **Algengt > Uppsetning > Notandavalkostir**.</span><span class="sxs-lookup"><span data-stu-id="202b1-121">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="202b1-122">Smelltu á flipann **Verkflæði**. Gakktu úr skugga um að hlutinn Úthlutun sé stækkaður.</span><span class="sxs-lookup"><span data-stu-id="202b1-122">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="202b1-123">Til að grunnstilla kerfi til að sjálfkrafa úthluta vinnuliðum á annan notandi, verður að stofna úthlutunarreglur sem tilgreina hvenær ákveðnar gerðir vinnuliða er úthluta.</span><span class="sxs-lookup"><span data-stu-id="202b1-123">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="202b1-124">Fylgið þessum skrefum til að stofna úthlutunarreglu.</span><span class="sxs-lookup"><span data-stu-id="202b1-124">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="202b1-125">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="202b1-125">Click **Add**.</span></span>
4. <span data-ttu-id="202b1-126">Í svæðinu **Umfang** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="202b1-126">In the **Scope** field, select an option:</span></span>
    - <span data-ttu-id="202b1-127">Allt - Úthluta öllum vinnuliðum sem úthlutað á þig.</span><span class="sxs-lookup"><span data-stu-id="202b1-127">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="202b1-128">Eining - Úthluta aðeins vinnuliðum sem tengjast tilgreindri gerð verkflæði.</span><span class="sxs-lookup"><span data-stu-id="202b1-128">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="202b1-129">Ef þessi valkostur valinn, verður að velja gerð verkflæðis í svæðinu **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="202b1-129">If you select this option, you must select the type of workflow in the **Name** field.</span></span>
    - <span data-ttu-id="202b1-130">Verkflæði - Úthluta aðeins vinnuliðum sem tengjast tilgreindu verkflæði.</span><span class="sxs-lookup"><span data-stu-id="202b1-130">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="202b1-131">Ef þessi valkostur valinn, verður að velja verkflæði í svæðinu **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="202b1-131">If you select this option, you must select the workflow in the **Name** field.</span></span>  
5. <span data-ttu-id="202b1-132">Í svæðið **Heiti**:</span><span class="sxs-lookup"><span data-stu-id="202b1-132">In the **Name** field:</span></span>
    - <span data-ttu-id="202b1-133">Fyrir **Eining** umfangið skal velja markeininguna.</span><span class="sxs-lookup"><span data-stu-id="202b1-133">For **Module** scope, select the target module.</span></span>
    - <span data-ttu-id="202b1-134">Fyrir **Verkflæði** eininguna skal velja markverkflæðið.</span><span class="sxs-lookup"><span data-stu-id="202b1-134">For **Workflow** scope, select the target workflow.</span></span>
6. <span data-ttu-id="202b1-135">Í reitnum **Úthluta** skal velja notanda sem úthluta skal vinnuliðum á.</span><span class="sxs-lookup"><span data-stu-id="202b1-135">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="202b1-136">Notið svæðin **Upphafsdagsetning/-tími** og **Lokadagsetning/-tími** til að tilgreina hvenær á sjálfkrafa að úthluta vinnuliður.</span><span class="sxs-lookup"><span data-stu-id="202b1-136">Use the **Start date/time** and **End date/time** fields to specify when you want the work items to be automatically delegated.</span></span>  
7. <span data-ttu-id="202b1-137">Í reitnum **Upphafsdagsetning/-tími** skal slá inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="202b1-137">In the **Start date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="202b1-138">Í reitnum **Lokadagsetning/-tími** skal slá inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="202b1-138">In the **End date/time** field, enter a date and time.</span></span>
9. <span data-ttu-id="202b1-139">Veljið gátreitinn **Virkjað** til að gera úthlutunarregluna virka.</span><span class="sxs-lookup"><span data-stu-id="202b1-139">Select the **Enabled** check box to activate the delegation rule.</span></span> 
10. <span data-ttu-id="202b1-140">Í reitnum **Athugasemd** skal færa inn athugasemd og útskýra hvers vegna vinnuliðum er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="202b1-140">In the **Comment** field, enter a comment that explains why you're delegating the work items.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]