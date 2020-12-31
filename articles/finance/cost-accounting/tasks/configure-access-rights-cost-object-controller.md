---
title: Skilgreina aðgangsréttindi stjórnborðs kostnaðarhlutar
description: Nota þetta ferli til að skilgreina aðgangsréttindi eftirlitsmanns kostnaðarhlutar.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4b50782c7a1b69b6953c65d6df155f003028333
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444530"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="3cb0b-103">Skilgreina aðgangsréttindi stjórnborðs kostnaðarhlutar</span><span class="sxs-lookup"><span data-stu-id="3cb0b-103">Configure access rights for a cost object controller</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3cb0b-104">Nota þetta ferli til að skilgreina aðgangsréttindi eftirlitsmanns kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="3cb0b-105">Þessi skráning notar USP2-sýnigagnafyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="3cb0b-106">Úthluta hlutverkinu Eftirlitsmaður kostnaðarhlutar</span><span class="sxs-lookup"><span data-stu-id="3cb0b-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="3cb0b-107">Farið í Kerfisstjórnun > Notendur > Notendur.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="3cb0b-108">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="3cb0b-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3cb0b-109">Til dæmis, sía á svæðið Notendanafn með gildinu „Alicia“.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="3cb0b-110">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3cb0b-111">Smellt er á Úthluta hlutverkum.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-111">Click Assign roles.</span></span>
5. <span data-ttu-id="3cb0b-112">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="3cb0b-113">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="3cb0b-114">Virkja öryggisatriði aðgangslista</span><span class="sxs-lookup"><span data-stu-id="3cb0b-114">Enable access list security</span></span>
1. <span data-ttu-id="3cb0b-115">Fara í kostnaðarbókhald > Víddir > Stigveldi vídda.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="3cb0b-116">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="3cb0b-117">Velja Fyrirtæki</span><span class="sxs-lookup"><span data-stu-id="3cb0b-117">Select Organization.</span></span>  
3. <span data-ttu-id="3cb0b-118">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-118">Click Edit.</span></span>
4. <span data-ttu-id="3cb0b-119">Veljið Já í svæðinu Stigveldi aðgangslista</span><span class="sxs-lookup"><span data-stu-id="3cb0b-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="3cb0b-120">Smella á Skoða stigveldi</span><span class="sxs-lookup"><span data-stu-id="3cb0b-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="3cb0b-121">Úthluta Aðgangsréttindum til notanda</span><span class="sxs-lookup"><span data-stu-id="3cb0b-121">Assign access rights to user</span></span>
1. <span data-ttu-id="3cb0b-122">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-122">Click New.</span></span>
2. <span data-ttu-id="3cb0b-123">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="3cb0b-124">Í reitinn Kenni notanda skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="3cb0b-125">Velja Stjórn.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-125">Select Admin.</span></span>  
4. <span data-ttu-id="3cb0b-126">Í trénu skal velja „Fyrirtæki\CEO\CFO\FIM“.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="3cb0b-127">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-127">Click New.</span></span>
6. <span data-ttu-id="3cb0b-128">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="3cb0b-129">Í reitinn Kenni notanda skal slá inn eða velja gildi.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="3cb0b-130">Velja Alicia.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-130">Select Alicia.</span></span>  
8. <span data-ttu-id="3cb0b-131">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="3cb0b-132">Virkja Aðgangsréttindi í kostnaðarbókhaldi</span><span class="sxs-lookup"><span data-stu-id="3cb0b-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="3cb0b-133">Fara í kostnaðarbókhald > Uppsetning > Færibreytur.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="3cb0b-134">Smellið á flipann „Almennt“.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-134">Click the General tab.</span></span>
3. <span data-ttu-id="3cb0b-135">Velja Já í reitnum Virkja skoðunaraðgang fyrir víddarstök kostnaðarhlutar.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="3cb0b-136">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-136">Click Save.</span></span>
5. <span data-ttu-id="3cb0b-137">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-137">Close the page.</span></span>
6. <span data-ttu-id="3cb0b-138">Fara í kostnaðarbókhald > Uppsetning > kostnaðarstýring vinnusvæði skilgreining.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="3cb0b-139">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-139">Click Edit.</span></span>
8. <span data-ttu-id="3cb0b-140">Veljið Já í svæðinu Útgefið.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="3cb0b-141">Ef þú velur Já, getur notandi sem er úthlutað einu af fjórum eftirfarandi hlutverkum séð skýrslur í Vinnusvæði kostnaðarstýringar: Stjórnandi kostnaðarbókhalds, endurskoðandi kostnaðar, afgreiðslustarfsmaður endurskoðanda kostnaðar, og eftirlitsmaður kostnaðarhluta.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="3cb0b-142">Ef þú velur Nei, getur aðeins notandi sem er úthlutað einu af fjórum eftirfarandi hlutverkum séð skýrslurnar: Stjórnandi kostnaðarbókhalds, endurskoðandi kostnaðar, og afgreiðslustarfsmaður endurskoðanda kostnaðar.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="3cb0b-143">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="3cb0b-143">Click Save.</span></span>

