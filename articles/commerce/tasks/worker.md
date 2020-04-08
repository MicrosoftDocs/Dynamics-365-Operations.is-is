---
title: Skilgreina starfsmann
description: Þetta ferli sýnir hvernig á að skilgreina starfsmaður sem sölufulltrúa sem er hæfur fyrir sölulaun fyrir sölu á Sölustað.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aee84f2dc39d2225985992fac0f9c20985ed9804
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022884"
---
# <a name="configure-a-worker"></a><span data-ttu-id="a5d3a-103">Skilgreina starfsmann</span><span class="sxs-lookup"><span data-stu-id="a5d3a-103">Configure a worker</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="a5d3a-104">Þetta ferli sýnir hvernig á að skilgreina starfsmaður sem sölufulltrúa sem er hæfur fyrir sölulaun fyrir sölu á Sölustað.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-104">This procedure demonstrates how to configure a worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="a5d3a-105">Þessi aðferð notar USRT sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="a5d3a-106">Stofna söluflokk sölulauna fyrir starfsmann.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="a5d3a-107">Fara í Sölu og markaðssetningu > Þóknanir > Söluflokkar.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="a5d3a-108">Hægt er að úthluta starfsmenn á eina eða fleiri söluflokka.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="a5d3a-109">Í POS, er hægt að velja alla söluflokka sem inniheldur starfskrafta úr aðsetursbók verslunarinnar.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="a5d3a-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-110">Click New.</span></span>
3. <span data-ttu-id="a5d3a-111">Í reitinn Hópur skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="a5d3a-112">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a5d3a-113">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-113">Click Save.</span></span>
6. <span data-ttu-id="a5d3a-114">Smellið á „Almennt“ á aðgerðarúðunni.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="a5d3a-115">Smellt er á Sölufulltrúa.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-115">Click Sales rep.</span></span>
    * <span data-ttu-id="a5d3a-116">Söluflokkur getur innihaldið fleiri en einn starfsmann.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="a5d3a-117">Sölulaun má skipta á milli starfsmenn byggt á því hvernig þú skilgreina hluta sölulauna.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="a5d3a-118">Sláið inn eða veldu gildi í reitnum heiti.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="a5d3a-119">Færið númer inn í svæðið hlutur sölulauna.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="a5d3a-120">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-120">Click Save.</span></span>
11. <span data-ttu-id="a5d3a-121">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-121">Close the page.</span></span>
12. <span data-ttu-id="a5d3a-122">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="a5d3a-123">Úthluta sjálfgefnum söluflokki starfsmanns</span><span class="sxs-lookup"><span data-stu-id="a5d3a-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="a5d3a-124">Fara í Retail og Commerce > Starfsmenn > Starfsfólk.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-124">Go to Retail and Commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="a5d3a-125">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="a5d3a-126">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="a5d3a-127">Smellið á flipann Commerce.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-127">Click the Commerce tab.</span></span>
    * <span data-ttu-id="a5d3a-128">Hægt er að úthluta starfsmanni á sjálfgefinn söluflokkur.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="a5d3a-129">Sjálfgefinn Söluflokkur verður sjálfkrafa bætt við sölulínur í Sölustað ef valkosturinn er virkjaður í virknireglu fyrir verslunina.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="a5d3a-130">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-130">Click Edit.</span></span>
6. <span data-ttu-id="a5d3a-131">Færa inn eða veljið gildi í reitnum Sjálfgefinn flokkur.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="a5d3a-132">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a5d3a-132">Click Save.</span></span>
