--- 
title: "Úthluta vinnuliðir í verkflæði"
description: "Ef þú verður ekki á skrifstofunni í einhvern tíma eða munt ekki vera tiltækur til að bregðast við vinnulið getur þú úthlutað, eða endurúthlutað vinnuliðunum, til annars notanda."
author: jasongre
manager: AnnBe
ms.date: 02/21/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 4765fec0cdce0e2f8859c979ff97d20aa6b20bfa
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="delegate-work-items-in-a-workflow"></a><span data-ttu-id="44dd4-103">Úthluta vinnuliðir í verkflæði</span><span class="sxs-lookup"><span data-stu-id="44dd4-103">Delegate work items in a workflow</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="44dd4-104">Ef þú verður ekki á skrifstofunni í einhvern tíma eða munt ekki vera tiltækur til að bregðast við vinnulið getur þú úthlutað, eða endurúthlutað vinnuliðunum, til annars notanda.</span><span class="sxs-lookup"><span data-stu-id="44dd4-104">If you plan to be out of the office or otherwise unavailable to act on work items, you can delegate, or reassign, your work items to other users.</span></span> <span data-ttu-id="44dd4-105">Þetta ferli hjálpar að grunnstilla kerfi til að sjálfkrafa úthluta vinnuliðum á annan notandi.</span><span class="sxs-lookup"><span data-stu-id="44dd4-105">This procedure helps you configure the system to automatically delegate your work items to another user.</span></span>



<span data-ttu-id="44dd4-106">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="44dd4-106">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-automatic-delegation"></a><span data-ttu-id="44dd4-107">Setja upp sjálfvirka úthlutun</span><span class="sxs-lookup"><span data-stu-id="44dd4-107">Set up automatic delegation</span></span>
1. <span data-ttu-id="44dd4-108">Fara í Algengt > Uppsetning > Notandavalkostir.</span><span class="sxs-lookup"><span data-stu-id="44dd4-108">Go to Common > Setup > User options.</span></span>
2. <span data-ttu-id="44dd4-109">Smellt er á flipann Verkflæði.</span><span class="sxs-lookup"><span data-stu-id="44dd4-109">Click the Workflow tab.</span></span>
    * <span data-ttu-id="44dd4-110">Gangið úr skugga um að hlutinn Úthlutun sé stækkaður.</span><span class="sxs-lookup"><span data-stu-id="44dd4-110">Make sure the Delegation section is expanded.</span></span>    <span data-ttu-id="44dd4-111">Til að grunnstilla kerfi til að sjálfkrafa úthluta vinnuliðum á annan notandi, verður að stofna úthlutunarreglur sem tilgreina hvenær ákveðnar gerðir vinnuliða er úthluta.</span><span class="sxs-lookup"><span data-stu-id="44dd4-111">To configure the system to automatically delegate your work items to other users, you must create delegation rules, which specify when certain types of work items are delegated.</span></span> <span data-ttu-id="44dd4-112">Fylgið þessum skrefum til að stofna úthlutunarreglu.</span><span class="sxs-lookup"><span data-stu-id="44dd4-112">Follow these steps to create a delegation rule.</span></span>  
3. <span data-ttu-id="44dd4-113">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="44dd4-113">Click Add.</span></span>
4. <span data-ttu-id="44dd4-114">Í svæði Umfang, velja valkostur.</span><span class="sxs-lookup"><span data-stu-id="44dd4-114">In the Scope field, select an option.</span></span>
    * <span data-ttu-id="44dd4-115">Allt - Úthluta öllum vinnuliðum sem úthlutað á þig.</span><span class="sxs-lookup"><span data-stu-id="44dd4-115">All – Delegate all work items that are assigned to you.</span></span>    <span data-ttu-id="44dd4-116">Eining - Úthluta aðeins vinnuliðum sem tengjast tilgreindri gerð verkflæði.</span><span class="sxs-lookup"><span data-stu-id="44dd4-116">Module – Delegate only the work items that are related to a specific type of workflow.</span></span> <span data-ttu-id="44dd4-117">Ef þessi valkostur valinn, verður að velja gerð verkflæðis í svæði Heiti.</span><span class="sxs-lookup"><span data-stu-id="44dd4-117">If you select this option, you must select the type of workflow in the Name field.</span></span>    <span data-ttu-id="44dd4-118">Verkflæði - Úthluta aðeins vinnuliðum sem tengjast tilgreindu verkflæði.</span><span class="sxs-lookup"><span data-stu-id="44dd4-118">Workflow – Delegate only the work items that are related to a specific workflow.</span></span> <span data-ttu-id="44dd4-119">Ef þessi valkostur valinn, verður að velja verkflæði í svæði Heiti.</span><span class="sxs-lookup"><span data-stu-id="44dd4-119">If you select this option, you must select the workflow in the Name field.</span></span>  
5. <span data-ttu-id="44dd4-120">Í svæði Úthluta, velja notandi sem á að úthluta vinnuliðir á.</span><span class="sxs-lookup"><span data-stu-id="44dd4-120">In the Delegate field, select the user to delegate the work items to.</span></span>
    * <span data-ttu-id="44dd4-121">Notið svæði Upphafsdagsetning/-tími og Lokadagsetning/-tími til að tilgreina hvenær á sjálfkrafa að úthluta vinnuliður.</span><span class="sxs-lookup"><span data-stu-id="44dd4-121">Use the Start date/time and End date/time fields to specify when you want the work items to be automatically delegated.</span></span>  
6. <span data-ttu-id="44dd4-122">Í svæði Upphafsdagsetning/-tími, slá inn dagsetning og tími.</span><span class="sxs-lookup"><span data-stu-id="44dd4-122">In the Start date/time field, enter a date and time.</span></span>
7. <span data-ttu-id="44dd4-123">Í svæði Lokadagsetning/-tími, slá inn dagsetning og tími.</span><span class="sxs-lookup"><span data-stu-id="44dd4-123">In the End date/time field, enter a date and time.</span></span>
8. <span data-ttu-id="44dd4-124">Veljið gátreitinn Virkt til að gera úthlutunarregluna virka.</span><span class="sxs-lookup"><span data-stu-id="44dd4-124">Select the Enabled check box to activate the delegation rule.</span></span>
    * <span data-ttu-id="44dd4-125">Ef Eining er valið sem umfang, verður að velja einingu í svæði Heiti.</span><span class="sxs-lookup"><span data-stu-id="44dd4-125">If you selected Module as the Scope, then you must select the module in the Name field.</span></span>    <span data-ttu-id="44dd4-126">Ef Verkflæði er valið sem umfang, verður að velja sérstakt verkflæði sem á að úthluta í svæði Heiti.</span><span class="sxs-lookup"><span data-stu-id="44dd4-126">If you selected Workflow as the Scope, then you must select the specific workflow to delegate in the Name field.</span></span>  
9. <span data-ttu-id="44dd4-127">Í svæði Athugasemd skal færa inn athugasemd og útskýra hvers vegna vinnuliðir eru úthlutað.</span><span class="sxs-lookup"><span data-stu-id="44dd4-127">In the Comment field, enter a comment that explains why you are delegating the work items.</span></span>


