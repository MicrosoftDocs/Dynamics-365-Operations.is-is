---
title: Úthluta vinnuliðir í verkflæði
description: Ef þú verður ekki á skrifstofunni í einhvern tíma eða munt ekki vera tiltækur til að bregðast við vinnulið getur þú úthlutað, eða endurúthlutað vinnuliðunum, til annars notanda.
author: jasongre
manager: AnnBe
ms.date: 04/09/2019
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
ms.openlocfilehash: feace647d7acef6abf86b13fcb8019c622c55ff6
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/12/2019
ms.locfileid: "976782"
---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="747fd-103">Úthluta vinnuliðum í verkflæði</span><span class="sxs-lookup"><span data-stu-id="747fd-103">Delegate work items in a workflow</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

## <a name="manually-delegate-a-work-item"></a><span data-ttu-id="747fd-104">Úthluta vinnulið handvirkt</span><span class="sxs-lookup"><span data-stu-id="747fd-104">Manually delegate a work item</span></span>

<span data-ttu-id="747fd-105">Til að úthluta einstökum vinnulið skal velja valkostinn **Úthluta** í valmyndinni **Verkflæði** og síðan færa inn notandann sem úthluta á til ásamt athugasemd.</span><span class="sxs-lookup"><span data-stu-id="747fd-105">To delegate an individual work item, select the **Delegate** option in the **Workflow** menu and then enter the user to be delegated to along with a comment.</span></span> <span data-ttu-id="747fd-106">Þetta mun endurúthluta vinnuliðnum á þann notanda svo hann geti lokið vinnunni.</span><span class="sxs-lookup"><span data-stu-id="747fd-106">This will reassign the work item to that user so they can complete it.</span></span>

## <a name="automatically-delegate-work-items"></a><span data-ttu-id="747fd-107">Úthluta vinnuliðum sjálfvirkt</span><span class="sxs-lookup"><span data-stu-id="747fd-107">Automatically delegate work items</span></span>

<span data-ttu-id="747fd-108">Ef þú verður ekki á skrifstofunni í einhvern tíma eða munt ekki vera tiltækur til að bregðast við vinnuliðum yfir eitthvert tímabil getur þú úthlutað nýjum vinnuliðum sjálfvirkt á aðra notendur með því að nota síðuna **Valkostir notanda**.</span><span class="sxs-lookup"><span data-stu-id="747fd-108">If you plan to be out of the office or otherwise unavailable to act on work items for a period of time, you can automatically delegate new work items to other users using the **User options** page.</span></span>

### <a name="set-up-automatic-delegation"></a><span data-ttu-id="747fd-109">Setja upp sjálfvirka úthlutun</span><span class="sxs-lookup"><span data-stu-id="747fd-109">Set up automatic delegation</span></span>
1. <span data-ttu-id="747fd-110">Fara í Algengt > Uppsetning > Notandavalkostir.</span><span class="sxs-lookup"><span data-stu-id="747fd-110">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="747fd-111">Smellt er á flipann Verkflæði.</span><span class="sxs-lookup"><span data-stu-id="747fd-111">Click the Workflow tab.</span></span>
    * <span data-ttu-id="747fd-112">Gangið úr skugga um að hlutinn Úthlutun sé stækkaður.</span><span class="sxs-lookup"><span data-stu-id="747fd-112">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="747fd-113">Til að grunnstilla kerfi til að sjálfkrafa úthluta vinnuliðum á annan notandi, verður að stofna úthlutunarreglur sem tilgreina hvenær ákveðnar gerðir vinnuliða er úthluta.</span><span class="sxs-lookup"><span data-stu-id="747fd-113">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="747fd-114">Fylgið þessum skrefum til að stofna úthlutunarreglu.</span><span class="sxs-lookup"><span data-stu-id="747fd-114">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="747fd-115">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="747fd-115">Click Add.</span></span>
4. <span data-ttu-id="747fd-116">Í svæði Umfang, velja valkostur.</span><span class="sxs-lookup"><span data-stu-id="747fd-116">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="747fd-117">Allt - Úthluta öllum vinnuliðum sem úthlutað á þig.</span><span class="sxs-lookup"><span data-stu-id="747fd-117">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="747fd-118">Eining - Úthluta aðeins vinnuliðum sem tengjast tilgreindri gerð verkflæði.</span><span class="sxs-lookup"><span data-stu-id="747fd-118">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="747fd-119">Ef þessi valkostur valinn, verður að velja gerð verkflæðis í svæði Heiti.</span><span class="sxs-lookup"><span data-stu-id="747fd-119">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="747fd-120">Verkflæði - Úthluta aðeins vinnuliðum sem tengjast tilgreindu verkflæði.</span><span class="sxs-lookup"><span data-stu-id="747fd-120">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="747fd-121">Ef þessi valkostur valinn, verður að velja verkflæði í svæði Heiti.</span><span class="sxs-lookup"><span data-stu-id="747fd-121">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="747fd-122">Í svæði Úthluta, velja notandi sem á að úthluta vinnuliðir á.</span><span class="sxs-lookup"><span data-stu-id="747fd-122">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="747fd-123">Notið svæði Upphafsdagsetning/-tími og Lokadagsetning/-tími til að tilgreina hvenær á sjálfkrafa að úthluta vinnuliður.</span><span class="sxs-lookup"><span data-stu-id="747fd-123">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="747fd-124">Í svæði Upphafsdagsetning/-tími, slá inn dagsetning og tími.</span><span class="sxs-lookup"><span data-stu-id="747fd-124">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="747fd-125">Í svæði Lokadagsetning/-tími, slá inn dagsetning og tími.</span><span class="sxs-lookup"><span data-stu-id="747fd-125">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="747fd-126">Veljið gátreitinn Virkt til að gera úthlutunarregluna virka.</span><span class="sxs-lookup"><span data-stu-id="747fd-126">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="747fd-127">Ef Eining er valið sem umfang, verður að velja einingu í svæði Heiti.</span><span class="sxs-lookup"><span data-stu-id="747fd-127">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="747fd-128">Ef Verkflæði er valið sem umfang, verður að velja sérstakt verkflæði sem á að úthluta í svæði Heiti.</span><span class="sxs-lookup"><span data-stu-id="747fd-128">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="747fd-129">Í svæði Athugasemd skal færa inn athugasemd og útskýra hvers vegna vinnuliðir eru úthlutað.</span><span class="sxs-lookup"><span data-stu-id="747fd-129">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>

