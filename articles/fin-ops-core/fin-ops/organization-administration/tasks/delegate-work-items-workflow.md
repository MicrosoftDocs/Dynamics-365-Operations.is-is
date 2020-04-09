---
title: Úthluta vinnuliðir í verkflæði
description: Ef þú verður ekki á skrifstofunni í einhvern tíma eða munt ekki vera tiltækur til að bregðast við vinnulið getur þú úthlutað, eða endurúthlutað vinnuliðunum, til annars notanda.
author: jasongre
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysUserSetup, WorkflowDelegationUserListLookup
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aceafbe8dfcdac2ac7b97a4f77a9a30599c60c51
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140583"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="1cfa3-103">Úthluta vinnuliðum í verkflæði</span><span class="sxs-lookup"><span data-stu-id="1cfa3-103">Delegate work items in a workflow</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="1cfa3-104">Úthluta vinnulið handvirkt</span><span class="sxs-lookup"><span data-stu-id="1cfa3-104">Manually delegate a work item</span></span>

<span data-ttu-id="1cfa3-105">Til að úthluta einstökum vinnulið skal velja valkostinn **Úthluta** í valmyndinni **Verkflæði** og síðan færa inn notandann sem úthluta á til ásamt athugasemd.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="1cfa3-106">Þetta mun endurúthluta vinnuliðnum á þann notanda svo hann geti lokið vinnunni.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="1cfa3-107">Úthluta vinnuliðum sjálfvirkt</span><span class="sxs-lookup"><span data-stu-id="1cfa3-107">Automatically delegate work items</span></span>

<span data-ttu-id="1cfa3-108">Ef þú verður ekki á skrifstofunni í einhvern tíma eða munt ekki vera tiltækur til að bregðast við vinnuliðum yfir eitthvert tímabil getur þú úthlutað nýjum vinnuliðum sjálfvirkt á aðra notendur með því að nota síðuna **Valkostir notanda**.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="1cfa3-109">Setja upp sjálfvirka úthlutun</span><span class="sxs-lookup"><span data-stu-id="1cfa3-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="1cfa3-110">Farðu í **Algengt > Uppsetning > Notandavalkostir**.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-110">Go to **Common > Setup > User options**.</span></span>
2. <span data-ttu-id="1cfa3-111">Smelltu á flipann **Verkflæði**. Gakktu úr skugga um að hlutinn Úthlutun sé stækkaður.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-111">Click the **Workflow** tab. Make sure the Delegation section is expanded.</span></span> <span data-ttu-id="1cfa3-112">Til að grunnstilla kerfi til að sjálfkrafa úthluta vinnuliðum á annan notandi, verður að stofna úthlutunarreglur sem tilgreina hvenær ákveðnar gerðir vinnuliða er úthluta.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-112">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="1cfa3-113">Fylgið þessum skrefum til að stofna úthlutunarreglu.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-113">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="1cfa3-114">Smelltu á **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-114">Click **Add**.</span></span>
4. <span data-ttu-id="1cfa3-115">Í svæði **Umfang** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-115">In the **Scope** field, select an option.</span></span>
    - <span data-ttu-id="1cfa3-116">Allt - Úthluta öllum vinnuliðum sem úthlutað á þig.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-116">All – Delegate all work items that are assigned to you.</span></span>
    - <span data-ttu-id="1cfa3-117">Eining - Úthluta aðeins vinnuliðum sem tengjast tilgreindri gerð verkflæði.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-117">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="1cfa3-118">Ef þessi valkostur valinn, verður að velja gerð verkflæðis í svæði Heiti.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-118">If you select this option, you must select the type of workflow in the Name field.</span></span>
    - <span data-ttu-id="1cfa3-119">Verkflæði - Úthluta aðeins vinnuliðum sem tengjast tilgreindu verkflæði.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-119">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="1cfa3-120">Ef þessi valkostur valinn, verður að velja verkflæði í svæði Heiti.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-120">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="1cfa3-121">Í reitnum **Úthluta** skal velja notanda sem úthluta skal vinnuliðum á.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-121">In the **Delegate** field, select the user to delegate the work items to.</span></span> <span data-ttu-id="1cfa3-122">Notið svæði Upphafsdagsetning/-tími og Lokadagsetning/-tími til að tilgreina hvenær á sjálfkrafa að úthluta vinnuliður.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-122">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="1cfa3-123">Í reitnum **Upphafsdagsetning/-tími** skal slá inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-123">In the **Start date/time** field, enter a date and time.</span></span>
7. <span data-ttu-id="1cfa3-124">Í reitnum **Lokadagsetning/-tími** skal slá inn dagsetningu og tíma.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-124">In the **End date/time** field, enter a date and time.</span></span>
8. <span data-ttu-id="1cfa3-125">Veljið gátreitinn **Virkjað** til að gera úthlutunarregluna virka.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-125">Select the **Enabled** check box to activate the delegation rule.</span></span> <span data-ttu-id="1cfa3-126">Ef **Eining** er valið sem umfang verður að velja einingu í reitnum Heiti.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-126">If you selected **Module** as the Scope, then you must select the module in the Name field.</span></span> <span data-ttu-id="1cfa3-127">Ef **Verkflæði** er valið sem umfang verður að velja sérstakt verkflæði til að úthluta í reitinn Heiti.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-127">If you selected **Workflow** as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="1cfa3-128">Í reitinn **Athugasemd** skal færa inn athugasemd og útskýra hvers vegna vinnuliðum er úthlutað.</span><span class="sxs-lookup"><span data-stu-id="1cfa3-128">In the **Comment** field, enter a comment that explains why you are delegating the work items.</span></span>

