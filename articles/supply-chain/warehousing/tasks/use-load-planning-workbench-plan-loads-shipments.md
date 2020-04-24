---
title: Áætla farm og sendingar með vinnusvæðinu Farmáætlun
description: Þessi efni sýnir hvernig á að nota vinnusvæði farmáætlunar til að stofna hleðslu fyrir sölupöntun.
author: ShylaThompson
manager: tfehr
ms.date: 07/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6a6af2f0623744f2cddf46c0310231afb0870fd7
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3216736"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="b051e-103">Áætla farm og sendingar með vinnusvæðinu Farmáætlun</span><span class="sxs-lookup"><span data-stu-id="b051e-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b051e-104">Þessi efni sýnir hvernig á að nota vinnusvæði farmáætlunar til að stofna hleðslu fyrir sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="b051e-104">This topic shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="b051e-105">Sem frumskilyrði stofnum við sölupöntunina fyrst.</span><span class="sxs-lookup"><span data-stu-id="b051e-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="b051e-106">Þetta ferli er hluti af daglega vinnu fyrir samræmingaraðili flutninga.</span><span class="sxs-lookup"><span data-stu-id="b051e-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="b051e-107">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="b051e-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="b051e-108">Stofna sölupöntun</span><span class="sxs-lookup"><span data-stu-id="b051e-108">Create a sales order</span></span>
1. <span data-ttu-id="b051e-109">Farðu í **Sloðunarrúða > Kerfiseiningar > viðskiptakröfur > Pantanir > Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="b051e-109">Go to the **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="b051e-110">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="b051e-110">Select **New**.</span></span>
3. <span data-ttu-id="b051e-111">Í reitnum **Viðskiptavinalykill** velurðu fellilistahnappinn til að opna uppflettinguna.</span><span class="sxs-lookup"><span data-stu-id="b051e-111">In the **Customer account** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b051e-112">Veldu lykilinn **US-004.**</span><span class="sxs-lookup"><span data-stu-id="b051e-112">Select account **US-004**.</span></span>
5. <span data-ttu-id="b051e-113">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b051e-113">Select **OK**.</span></span>
6. <span data-ttu-id="b051e-114">Í reitnum **Vörunúmer** velurðu fellilistahnappinn til að opna uppflettinguna.</span><span class="sxs-lookup"><span data-stu-id="b051e-114">In the **Item number** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="b051e-115">Velja vöru **A0001**.</span><span class="sxs-lookup"><span data-stu-id="b051e-115">Select item **A0001**.</span></span> <span data-ttu-id="b051e-116">**A0001** er virkt fyrir flutningsstjórnun.</span><span class="sxs-lookup"><span data-stu-id="b051e-116">**A0001** is enabled for transportation management.</span></span>  
8. <span data-ttu-id="b051e-117">Í reitnum **Svæði** velurðu fellilistahnappinn til að opna leitina og velur síðan vöruna.</span><span class="sxs-lookup"><span data-stu-id="b051e-117">In the **Site** field, select the drop-down button to open the lookup, then select an item.</span></span>
9. <span data-ttu-id="b051e-118">Í reitnum **Magn** slærðu inn tölu.</span><span class="sxs-lookup"><span data-stu-id="b051e-118">In the **Quantity** field, enter a number.</span></span>
10. <span data-ttu-id="b051e-119">Í **Vöruhús** reitinn, sláðu inn '24' fyrir þetta dæmi.</span><span class="sxs-lookup"><span data-stu-id="b051e-119">In the **Warehouse** field, type '24' for this example.</span></span> <span data-ttu-id="b051e-120">Þetta vöruhús er virkr fyrir ítarlegt vöruhúsakerfi og flutningsstjórnun.</span><span class="sxs-lookup"><span data-stu-id="b051e-120">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="b051e-121">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b051e-121">Select **Save**.</span></span>
12. <span data-ttu-id="b051e-122">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b051e-122">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="b051e-123">Stofna nýja hleðslu</span><span class="sxs-lookup"><span data-stu-id="b051e-123">Create a new load</span></span>
1. <span data-ttu-id="b051e-124">Fara í **Skoðunarrúðu > Kerfiseiningar > Flutningsstýring > Áætlanagerð > Vinnusvæði hleðsluáætlunar**.</span><span class="sxs-lookup"><span data-stu-id="b051e-124">Go to the **Navigation pane > Modules > Transportation management > Planning > Load planning workbench**.</span></span>
2. <span data-ttu-id="b051e-125">Veldu flipann **Sölulínur**. Nú byggirðu hleðslu fyrir sölupöntunina sem var nýverið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="b051e-125">Select the **Sales lines** tab. Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="b051e-126">Hægt er að byggja upp hleðslur á grundvelli framboðs og eftirspurnar úr innkaupapöntunum, flutningspöntunum og sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="b051e-126">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="b051e-127">Í aðgerðasvæðinu er smellt á **Framboð og eftirspurn**.</span><span class="sxs-lookup"><span data-stu-id="b051e-127">On the Action Pane, select **Supply and demand**.</span></span>
4. <span data-ttu-id="b051e-128">Veldu **Í nýja hleðslu**.</span><span class="sxs-lookup"><span data-stu-id="b051e-128">Select **To new load**.</span></span>
5. <span data-ttu-id="b051e-129">Í reitnum **Auðkenni hleðslusniðmáts** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="b051e-129">In the **Load template ID** field, select the drop-down button to open the lookup.</span></span> <span data-ttu-id="b051e-130">Sniðmát Hleðslu skilgreinir hámarks mælieiningar fyrir þyngd og rúmmál allrar hleðslunnar.</span><span class="sxs-lookup"><span data-stu-id="b051e-130">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="b051e-131">Til dæmis gæti hleðslusniðmátsins staðið fyrir stærð vörubíls eða gáms.</span><span class="sxs-lookup"><span data-stu-id="b051e-131">For example, the load template might represent the size of a container or truck.</span></span> <span data-ttu-id="b051e-132">Veljið vöru.</span><span class="sxs-lookup"><span data-stu-id="b051e-132">Select an item.</span></span>
6. <span data-ttu-id="b051e-133">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b051e-133">Select **OK**.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="b051e-134">Taxta og leið á hleðslu</span><span class="sxs-lookup"><span data-stu-id="b051e-134">Rate and route the load</span></span>
1. <span data-ttu-id="b051e-135">Veldu **Mat og leiðir**.</span><span class="sxs-lookup"><span data-stu-id="b051e-135">Select **Rating and routing**.</span></span>
2. <span data-ttu-id="b051e-136">Veldu **Taxti vinnusvæðis leiðar**.</span><span class="sxs-lookup"><span data-stu-id="b051e-136">Select **Rate route workbench**.</span></span>
3. <span data-ttu-id="b051e-137">Veldu **Meta verslun**.</span><span class="sxs-lookup"><span data-stu-id="b051e-137">Select **Rate shop**.</span></span>
4. <span data-ttu-id="b051e-138">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="b051e-138">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b051e-139">Velja **Úthluta**.</span><span class="sxs-lookup"><span data-stu-id="b051e-139">Select **Assign**.</span></span>
6. <span data-ttu-id="b051e-140">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b051e-140">Close the page.</span></span>

