--- 
title: "Stofna áætlun fyrir svæði"
description: "Framleiðslustjóri reiknar efnis- og afkastakröfur fyrir framleiðslu á tiltekinnar vöru."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1452c5d6f5dd8d0dd4cb08eb5cc9a48fd8f875f9
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="c96f7-103">Stofna áætlun fyrir svæði</span><span class="sxs-lookup"><span data-stu-id="c96f7-103">Create a plan for a site</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c96f7-104">Framleiðslustjóri reiknar efnis- og afkastakröfur fyrir framleiðslu á tiltekinnar vöru.</span><span class="sxs-lookup"><span data-stu-id="c96f7-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="c96f7-105">Eftir að tillögur um uppruna eru stofnaðar finnur hann pantanirnar á svæði sem hann er að gera áætlun fyrir og staðfestir pantanir, byrjar á þeim sem eru mest áríðandi.</span><span class="sxs-lookup"><span data-stu-id="c96f7-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="c96f7-106">Mest áríðandi pantanir eru þær sem þarf að staðfesta á gildandi dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="c96f7-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="c96f7-107">Nota Sýnifyrirtækið USMF til að ljúka við þessi verk.</span><span class="sxs-lookup"><span data-stu-id="c96f7-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="c96f7-108">Stofna efnis- og afkastaáætlun fyrir vöru</span><span class="sxs-lookup"><span data-stu-id="c96f7-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="c96f7-109">Smellt er á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="c96f7-109">Click Master planning.</span></span>
    * <span data-ttu-id="c96f7-110">Þarf að fara á sjálfgefið yfirlit.</span><span class="sxs-lookup"><span data-stu-id="c96f7-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="c96f7-111">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="c96f7-111">Click Run.</span></span>
3. <span data-ttu-id="c96f7-112">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="c96f7-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="c96f7-113">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="c96f7-113">Click Filter.</span></span>
5. <span data-ttu-id="c96f7-114">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="c96f7-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="c96f7-115">Í reitinn Skilyrði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="c96f7-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="c96f7-116">Til dæmis: D0001</span><span class="sxs-lookup"><span data-stu-id="c96f7-116">Example: D0001</span></span>  
7. <span data-ttu-id="c96f7-117">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c96f7-117">Click OK.</span></span>
8. <span data-ttu-id="c96f7-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c96f7-118">Click OK.</span></span>
    * <span data-ttu-id="c96f7-119">Þetta getur tekið nokkrar mínútur...</span><span class="sxs-lookup"><span data-stu-id="c96f7-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="c96f7-120">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="c96f7-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="c96f7-121">Auðkenna áríðandi áætlaðar pantanir fyrir vöru</span><span class="sxs-lookup"><span data-stu-id="c96f7-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="c96f7-122">Opna vörunúmerasíu fyrir dálkur.</span><span class="sxs-lookup"><span data-stu-id="c96f7-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="c96f7-123">Notið síu í reitnum „vörunúmer“ með gildinu „D0001“ og notið til þess „byrjar á“ síu virknitákn</span><span class="sxs-lookup"><span data-stu-id="c96f7-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="c96f7-124">Opnið dálkasíu pöntunardagsetningar.</span><span class="sxs-lookup"><span data-stu-id="c96f7-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="c96f7-125">Nota síu á "Pöntunardagsetningu" svæðið, með gildandi dagsetningu, með síuvirkjanum "er nákvæmlega".</span><span class="sxs-lookup"><span data-stu-id="c96f7-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="c96f7-126">Staðfesta áríðandi pantanir fyrir vöru</span><span class="sxs-lookup"><span data-stu-id="c96f7-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="c96f7-127">Merkið eða afmerkið allar línur í listanum.</span><span class="sxs-lookup"><span data-stu-id="c96f7-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="c96f7-128">Smellið á „Fastáætla“.</span><span class="sxs-lookup"><span data-stu-id="c96f7-128">Click Firm.</span></span>
3. <span data-ttu-id="c96f7-129">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c96f7-129">Click OK.</span></span>


