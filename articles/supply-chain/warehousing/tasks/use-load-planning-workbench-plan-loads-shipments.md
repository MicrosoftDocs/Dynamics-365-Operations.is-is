---
title: Áætla farm og sendingar með vinnusvæðinu Farmáætlun
description: Þessi gerli sýnir hvernig á að nota vinnusvæði farmáætlunar til að stofna hleðslu fyrir sölupöntun.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1927cff48beb30f934bd066c32ab48dfb9d06f74
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "343904"
---
# <a name="plan-loads-and-shipments-using-the-load-planning-workbench"></a><span data-ttu-id="a5277-103">Áætla farm og sendingar með vinnusvæðinu Farmáætlun</span><span class="sxs-lookup"><span data-stu-id="a5277-103">Plan loads and shipments using the Load planning workbench</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a5277-104">Þessi gerli sýnir hvernig á að nota vinnusvæði farmáætlunar til að stofna hleðslu fyrir sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="a5277-104">This procedure shows how to use the load planning workbench to create a load for a sales order.</span></span> <span data-ttu-id="a5277-105">Sem frumskilyrði stofnum við sölupöntunina fyrst.</span><span class="sxs-lookup"><span data-stu-id="a5277-105">As a prerequisite we'll create the sales order first.</span></span> <span data-ttu-id="a5277-106">Þetta ferli er hluti af daglega vinnu fyrir samræmingaraðili flutninga.</span><span class="sxs-lookup"><span data-stu-id="a5277-106">This procedure is part of the daily work for the transportation coordinator.</span></span> <span data-ttu-id="a5277-107">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="a5277-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-sales-order"></a><span data-ttu-id="a5277-108">Stofna sölupöntun</span><span class="sxs-lookup"><span data-stu-id="a5277-108">Create a sales order</span></span>
1. <span data-ttu-id="a5277-109">Farið í Viðskiptakröfur > Pantanir > Allar sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="a5277-109">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="a5277-110">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a5277-110">Click New.</span></span>
3. <span data-ttu-id="a5277-111">Í reitnum Reikningur viðskiptavina skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="a5277-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a5277-112">Velja lykilinn US-004.</span><span class="sxs-lookup"><span data-stu-id="a5277-112">Select account US-004.</span></span>
5. <span data-ttu-id="a5277-113">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="a5277-113">Click OK.</span></span>
6. <span data-ttu-id="a5277-114">Í reitnum Vörunúmer skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="a5277-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a5277-115">Velja vöru A0001.</span><span class="sxs-lookup"><span data-stu-id="a5277-115">Select item A0001.</span></span>
    * <span data-ttu-id="a5277-116">A0001 er virkt fyrir flutningsstjórnun.</span><span class="sxs-lookup"><span data-stu-id="a5277-116">A0001 is enabled for transportation management.</span></span>  
8. <span data-ttu-id="a5277-117">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a5277-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="a5277-118">Færið inn númer í reitnum „Magn“.</span><span class="sxs-lookup"><span data-stu-id="a5277-118">In the Quantity field, enter a number.</span></span>
10. <span data-ttu-id="a5277-119">Í reitnum Vöruhús skal færa inn ‚24‘.</span><span class="sxs-lookup"><span data-stu-id="a5277-119">In the Warehouse field, type '24'.</span></span>
    * <span data-ttu-id="a5277-120">Í þessu dæmi skal velja vöruhúsið 24.</span><span class="sxs-lookup"><span data-stu-id="a5277-120">In this example select warehouse 24.</span></span> <span data-ttu-id="a5277-121">Þetta vöruhús er virkr fyrir ítarlegt vöruhúsakerfi og flutningsstjórnun.</span><span class="sxs-lookup"><span data-stu-id="a5277-121">This warehouse is enabled for transportation management and advanced warehouse management.</span></span>  
11. <span data-ttu-id="a5277-122">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a5277-122">Click Save.</span></span>
12. <span data-ttu-id="a5277-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a5277-123">Close the page.</span></span>

## <a name="create-a-new-load"></a><span data-ttu-id="a5277-124">Stofna nýja hleðslu</span><span class="sxs-lookup"><span data-stu-id="a5277-124">Create a new load</span></span>
1. <span data-ttu-id="a5277-125">Fara í flutningsstjórnun > Áætlanagerð > Vinnusvæði hleðsluáætlunar.</span><span class="sxs-lookup"><span data-stu-id="a5277-125">Go to Transportation management > Planning > Load planning workbench.</span></span>
2. <span data-ttu-id="a5277-126">Smellt er á flipanum sölulína.</span><span class="sxs-lookup"><span data-stu-id="a5277-126">Click the Sales lines tab.</span></span>
    * <span data-ttu-id="a5277-127">Nú byggirðu hleðslu fyrir sölupöntunina sem var nýverið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="a5277-127">Now you'll build the load for the sales order that you just created.</span></span> <span data-ttu-id="a5277-128">Hægt er að byggja upp hleðslur á grundvelli framboðs og eftirspurnar úr innkaupapöntunum, flutningspöntunum og sölupöntunum.</span><span class="sxs-lookup"><span data-stu-id="a5277-128">Loads can be built based on supply and demand from purchase orders, transfer orders, and sales orders.</span></span>  
3. <span data-ttu-id="a5277-129">Í aðgerðasvæðinu er smellt á Framboð og eftirspurn.</span><span class="sxs-lookup"><span data-stu-id="a5277-129">On the Action Pane, click Supply and demand.</span></span>
4. <span data-ttu-id="a5277-130">Smellt er á Í nýja hleðslu.</span><span class="sxs-lookup"><span data-stu-id="a5277-130">Click To new load.</span></span>
5. <span data-ttu-id="a5277-131">Í reitnum Auðkenni hleðslusniðmáts skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="a5277-131">In the Load template ID field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="a5277-132">Sniðmát Hleðslu skilgreinir hámarks mælieiningar fyrir þyngd og rúmmál allrar hleðslunnar.</span><span class="sxs-lookup"><span data-stu-id="a5277-132">The Load template defines maximum measurements for weight and volume of the entire load.</span></span> <span data-ttu-id="a5277-133">Til dæmis gæti hleðslusniðmátsins staðið fyrir stærð vörubíls eða gáms.</span><span class="sxs-lookup"><span data-stu-id="a5277-133">For example, the load template might represent the size of a container or truck.</span></span>  
6. <span data-ttu-id="a5277-134">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="a5277-134">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="a5277-135">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="a5277-135">Click OK.</span></span>

## <a name="rate-and-route-the-load"></a><span data-ttu-id="a5277-136">Taxta og leið á hleðslu</span><span class="sxs-lookup"><span data-stu-id="a5277-136">Rate and route the load</span></span>
1. <span data-ttu-id="a5277-137">Smellt er á Mat og leið.</span><span class="sxs-lookup"><span data-stu-id="a5277-137">Click Rating and routing.</span></span>
2. <span data-ttu-id="a5277-138">Smellt er á Taxti vinnusvæðis leiðar.</span><span class="sxs-lookup"><span data-stu-id="a5277-138">Click Rate route workbench.</span></span>
3. <span data-ttu-id="a5277-139">Smellt er á Taxti verslunar.</span><span class="sxs-lookup"><span data-stu-id="a5277-139">Click Rate shop.</span></span>
4. <span data-ttu-id="a5277-140">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="a5277-140">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a5277-141">Smellið á úthluta.</span><span class="sxs-lookup"><span data-stu-id="a5277-141">Click Assign.</span></span>
6. <span data-ttu-id="a5277-142">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a5277-142">Close the page.</span></span>
7. <span data-ttu-id="a5277-143">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a5277-143">Close the page.</span></span>

