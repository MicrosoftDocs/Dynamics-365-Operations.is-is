--- 
title: " Skilgreina starfsmann"
description: "Þetta ferli sýnir hvernig á að skilgreina starfsmaður í smásölu sem sölufulltrúa sem er hæfur fyrir sölulaun fyrir sölu á Sölustað."
author: jblucher
manager: AnnBe
ms.date: 02/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 27b075cf1152f16fc4726b224e877eacb2f2572c
ms.contentlocale: is-is
ms.lasthandoff: 02/07/2018

---
# <a name="configure-a-worker"></a><span data-ttu-id="0d35e-103"> Skilgreina starfsmann</span><span class="sxs-lookup"><span data-stu-id="0d35e-103">Configure a worker</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="0d35e-104">Þetta ferli sýnir hvernig á að skilgreina starfsmaður í smásölu sem sölufulltrúa sem er hæfur fyrir sölulaun fyrir sölu á Sölustað.</span><span class="sxs-lookup"><span data-stu-id="0d35e-104">This procedure demonstrates how to configure a retail worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="0d35e-105">Þessi aðferð notar USRT sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="0d35e-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="0d35e-106">Stofna söluflokk sölulauna fyrir starfsmann.</span><span class="sxs-lookup"><span data-stu-id="0d35e-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="0d35e-107">Fara í Sölu og markaðssetningu > Þóknanir > Söluflokkar.</span><span class="sxs-lookup"><span data-stu-id="0d35e-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="0d35e-108">Hægt er að úthluta starfsmenn á eina eða fleiri söluflokka.</span><span class="sxs-lookup"><span data-stu-id="0d35e-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="0d35e-109">Í POS, er hægt að velja alla söluflokka sem inniheldur starfskrafta úr aðsetursbók verslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="0d35e-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="0d35e-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="0d35e-110">Click New.</span></span>
3. <span data-ttu-id="0d35e-111">Í reitinn Hópur skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="0d35e-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="0d35e-112">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="0d35e-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0d35e-113">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0d35e-113">Click Save.</span></span>
6. <span data-ttu-id="0d35e-114">Smellið á „Almennt“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="0d35e-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="0d35e-115">Smellt er á Sölufulltrúa.</span><span class="sxs-lookup"><span data-stu-id="0d35e-115">Click Sales rep.</span></span>
    * <span data-ttu-id="0d35e-116">Söluflokkur getur innihaldið fleiri en einn starfsmann.</span><span class="sxs-lookup"><span data-stu-id="0d35e-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="0d35e-117">Sölulaun má skipta á milli starfsmenn byggt á því hvernig þú skilgreina hluta sölulauna.</span><span class="sxs-lookup"><span data-stu-id="0d35e-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="0d35e-118">Sláið inn eða veldu gildi í reitnum heiti.</span><span class="sxs-lookup"><span data-stu-id="0d35e-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="0d35e-119">Færið númer inn í svæðið hlutur sölulauna.</span><span class="sxs-lookup"><span data-stu-id="0d35e-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="0d35e-120">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0d35e-120">Click Save.</span></span>
11. <span data-ttu-id="0d35e-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0d35e-121">Close the page.</span></span>
12. <span data-ttu-id="0d35e-122">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="0d35e-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="0d35e-123">Úthluta sjálfgefnum söluflokki starfsmanns</span><span class="sxs-lookup"><span data-stu-id="0d35e-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="0d35e-124">Fara í Smásölu og viðskipti > Starfsmenn > Starfsfólk.</span><span class="sxs-lookup"><span data-stu-id="0d35e-124">Go to Retail and commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="0d35e-125">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="0d35e-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0d35e-126">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="0d35e-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0d35e-127">Smellið á flipann Smásala.</span><span class="sxs-lookup"><span data-stu-id="0d35e-127">Click the Retail tab.</span></span>
    * <span data-ttu-id="0d35e-128">Hægt er að úthluta starfsmanni á sjálfgefinn söluflokkur.</span><span class="sxs-lookup"><span data-stu-id="0d35e-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="0d35e-129">Sjálfgefinn Söluflokkur verður sjálfkrafa bætt við sölulínur í Sölustað ef valkosturinn er virkjaður í virknireglu fyrir verslunina.</span><span class="sxs-lookup"><span data-stu-id="0d35e-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="0d35e-130">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="0d35e-130">Click Edit.</span></span>
6. <span data-ttu-id="0d35e-131">Færa inn eða veljið gildi í reitnum Sjálfgefinn flokkur.</span><span class="sxs-lookup"><span data-stu-id="0d35e-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="0d35e-132">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="0d35e-132">Click Save.</span></span>


