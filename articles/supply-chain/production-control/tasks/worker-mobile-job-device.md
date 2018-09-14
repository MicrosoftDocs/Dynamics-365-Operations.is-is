--- 
title: "Skilgreina starfsmann með fartæki"
description: "Þessi verklýsing sýnir hvernig á að úthluta rétt hlutverk notandareikningurinn starfsmanns og virkja síðan starfsmanns til að gera skráningu í vinnslusalarstjórnun."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 1bb4d806810660e55ef13a9ff21c07e0ce194496
ms.contentlocale: is-is
ms.lasthandoff: 09/14/2018

---
# <a name="configure-a-worker-using-the-mobile-job-device"></a><span data-ttu-id="d2b0f-103">Skilgreina starfsmann með fartæki</span><span class="sxs-lookup"><span data-stu-id="d2b0f-103">Configure a worker using the mobile job device</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d2b0f-104">Þessi verklýsing sýnir hvernig á að úthluta rétt hlutverk notandareikningurinn starfsmanns og virkja síðan starfsmanns til að gera skráningu í vinnslusalarstjórnun.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-104">This procedure shows you how to assign the correct roles to the user account of a worker, and then enable the worker to do shop floor registrations.</span></span>


## <a name="assign-roles-to-user-account"></a><span data-ttu-id="d2b0f-105">Bæta hlutverkum við notanda</span><span class="sxs-lookup"><span data-stu-id="d2b0f-105">Assign roles to user account</span></span>
1. <span data-ttu-id="d2b0f-106">Farið í Kerfisstjórnun > Notendur > Notendur.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="d2b0f-107">Nota Síu á Flýtiræsistikunni til að sía á nafn starfsmanns þar sem notandareikningurinn tengist hlutverki starfsmaður á vél.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-107">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="d2b0f-108">Heiti væri Shannon í sýnigögn.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-108">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="d2b0f-109">Auðkennið skráningu notandareikningur.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-109">Highlight the user account record.</span></span>
4. <span data-ttu-id="d2b0f-110">Á listanum, smella á tengilinn "Heiti" í völdu línunni til að skoða upplýsingar um lykil notanda.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-110">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="d2b0f-111">Veljið ‚Roles\Stjórnanda á vél', í trénu.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-111">In the tree, select 'Roles\Machine operator'.</span></span>
6. <span data-ttu-id="d2b0f-112">Loka upplýsingasíðunni lykil notanda.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-112">Close the user account details page.</span></span>
7. <span data-ttu-id="d2b0f-113">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-113">Close the page.</span></span>

## <a name="configure-worker-account"></a><span data-ttu-id="d2b0f-114">Skilgreina notandareikning starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-114">Configure worker account.</span></span>
1. <span data-ttu-id="d2b0f-115">Farið í Mannauður > Starfsfólk > Starfsfólk.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-115">Go to Human resources > Workers > Workers.</span></span>
2. <span data-ttu-id="d2b0f-116">Nota Síu á Flýtiræsistikunni til að sía á nafn starfsmanns þar sem notandareikningurinn tengist hlutverki starfsmaður á vél.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-116">Use the Quick Filter to filter on the name of a worker where the user account is associated with the machine operator role.</span></span> <span data-ttu-id="d2b0f-117">Heiti væri Shannon í sýnigögn.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-117">In the sample data, the name would be Shannon.</span></span>
3. <span data-ttu-id="d2b0f-118">Auðkennið skráningu notandareikningur.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-118">Highlight the user account record.</span></span>
4. <span data-ttu-id="d2b0f-119">Á listanum, smella á tengilinn "Heiti" í völdu línunni til að skoða upplýsingar um lykil notanda.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-119">In the list, click the "Name" link in the selected row to view the details of the user account.</span></span>
5. <span data-ttu-id="d2b0f-120">Smellið á flipann Ráðningar.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-120">Click the Employment tab.</span></span>
6. <span data-ttu-id="d2b0f-121">Útvíkka tímaskráningu flýtiflipi og smella á Virkja á skráningarstöðvum.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-121">Expand the Time registration FastTab and click Activate on registration terminals.</span></span>
7. <span data-ttu-id="d2b0f-122">Smella á Virkja á skráningarstöðvum.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-122">Click Activate on registration terminals.</span></span>
8. <span data-ttu-id="d2b0f-123">Í reitinn reikniflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-123">In the Calculation group field, enter or select a value.</span></span>
9. <span data-ttu-id="d2b0f-124">Færa inn eða veljið gildi í reitnum Sjálfgefinn reikniflokkur.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-124">In the Default calculation group field, enter or select a value.</span></span>
10. <span data-ttu-id="d2b0f-125">Í reitinn samþykkisflokkur skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-125">In the Approval group field, enter or select a value.</span></span>
11. <span data-ttu-id="d2b0f-126">Færa inn eða veljið gildi í reit fyrir staðlaða forstillingu</span><span class="sxs-lookup"><span data-stu-id="d2b0f-126">In the Standard profile field, enter or select a value.</span></span>
12. <span data-ttu-id="d2b0f-127">Færa inn eða veljið gildi í svæðinu forstillingarflokkur.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-127">In the Profile group field, enter or select a value.</span></span>
13. <span data-ttu-id="d2b0f-128">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-128">Click OK.</span></span>
14. <span data-ttu-id="d2b0f-129">Smella á Breyta til að færa inn númer korti fyrir nýja starfsmaður sem sinnir tímaskráningu.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-129">Click Edit to enter a badge number for the new time registration worker.</span></span>
15. <span data-ttu-id="d2b0f-130">Færa inn gildi í svæðið Kenni korts.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-130">In the Badge ID field, type a value.</span></span>
16. <span data-ttu-id="d2b0f-131">Smelltu á Vista.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-131">Click Save.</span></span>
17. <span data-ttu-id="d2b0f-132">Notaðu flýtileiðina SaveRecord (vista skrá)</span><span class="sxs-lookup"><span data-stu-id="d2b0f-132">Use the SaveRecord shortcut.</span></span>
18. <span data-ttu-id="d2b0f-133">Loka upplýsingasíðunni starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-133">Close the worker details page.</span></span>
19. <span data-ttu-id="d2b0f-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-134">Close the page.</span></span>

## <a name="assign-worker-to-device-group"></a><span data-ttu-id="d2b0f-135">Úthluta starfsmanns á tækjaflokk.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-135">Assign worker to device group.</span></span>
1. <span data-ttu-id="d2b0f-136">Fara í Framleiðslustýringar > Uppsetning > Framkvæmd framleiðslu > Skilgreina verkspjald fyrir tæki.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-136">Go to Production control > Setup > Manufacturing execution > Configure job card for devices.</span></span>
2. <span data-ttu-id="d2b0f-137">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-137">Click Add.</span></span>
3. <span data-ttu-id="d2b0f-138">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="d2b0f-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-139">Click OK.</span></span>
5. <span data-ttu-id="d2b0f-140">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-140">Click Edit.</span></span>
6. <span data-ttu-id="d2b0f-141">Í svæðið eining Framleiðslu er hægt að setja síu sjálfgefið fyrir starfsmann.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-141">In the Production unit field, you can set the default filter for the worker.</span></span> <span data-ttu-id="d2b0f-142">Þetta mun tryggja að eingöngu vinnslur fyrir valda framleiðslueiningu eru birtar þegar starfsmaður skráir sig inn á tækinu.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-142">This will ensure that only production jobs for the selected production unit are shown when the worker logs on to the device.</span></span>
7. <span data-ttu-id="d2b0f-143">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="d2b0f-143">Close the page.</span></span>


