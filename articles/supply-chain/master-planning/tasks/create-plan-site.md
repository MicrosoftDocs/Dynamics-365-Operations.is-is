---
title: Stofna áætlun fyrir svæði
description: Framleiðslustjóri reiknar efnis- og afkastakröfur fyrir framleiðslu á tiltekinnar vöru.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqTransPOUrgentFormPart, SysQueryForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: daa185864052849b2c78d975a7eb02e9697cb618
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845172"
---
# <a name="create-a-plan-for-a-site"></a><span data-ttu-id="604e6-103">Stofna áætlun fyrir svæði</span><span class="sxs-lookup"><span data-stu-id="604e6-103">Create a plan for a site</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="604e6-104">Framleiðslustjóri reiknar efnis- og afkastakröfur fyrir framleiðslu á tiltekinnar vöru.</span><span class="sxs-lookup"><span data-stu-id="604e6-104">The production planner calculates the material and capacity requirements for the production of a specific item.</span></span> <span data-ttu-id="604e6-105">Eftir að tillögur um uppruna eru stofnaðar finnur hann pantanirnar á svæði sem hann er að gera áætlun fyrir og staðfestir pantanir, byrjar á þeim sem eru mest áríðandi.</span><span class="sxs-lookup"><span data-stu-id="604e6-105">After the sourcing suggestions are created, he finds the orders at the site for which he is planning and firms the orders, starting from the urgent ones.</span></span> <span data-ttu-id="604e6-106">Mest áríðandi pantanir eru þær sem þarf að staðfesta á gildandi dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="604e6-106">The most urgent orders are the ones that need to be firmed on the current date.</span></span> <span data-ttu-id="604e6-107">Nota Sýnifyrirtækið USMF til að ljúka við þessi verk.</span><span class="sxs-lookup"><span data-stu-id="604e6-107">Use the demo data company USMF to perform these tasks.</span></span>


## <a name="create-a-materials-and-capacity-plan-for-an-item"></a><span data-ttu-id="604e6-108">Stofna efnis- og afkastaáætlun fyrir vöru</span><span class="sxs-lookup"><span data-stu-id="604e6-108">Create a materials and capacity plan for an item</span></span>
1. <span data-ttu-id="604e6-109">Smellt er á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="604e6-109">Click Master planning.</span></span>
    * <span data-ttu-id="604e6-110">Þarf að fara á sjálfgefið yfirlit.</span><span class="sxs-lookup"><span data-stu-id="604e6-110">You need to navigate to the default Dashboard.</span></span>  
2. <span data-ttu-id="604e6-111">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="604e6-111">Click Run.</span></span>
3. <span data-ttu-id="604e6-112">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="604e6-112">Expand the Records to include section.</span></span>
4. <span data-ttu-id="604e6-113">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="604e6-113">Click Filter.</span></span>
5. <span data-ttu-id="604e6-114">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="604e6-114">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="604e6-115">Í reitinn Skilyrði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="604e6-115">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="604e6-116">Til dæmis: D0001</span><span class="sxs-lookup"><span data-stu-id="604e6-116">Example: D0001</span></span>  
7. <span data-ttu-id="604e6-117">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="604e6-117">Click OK.</span></span>
8. <span data-ttu-id="604e6-118">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="604e6-118">Click OK.</span></span>
    * <span data-ttu-id="604e6-119">Þetta getur tekið nokkrar mínútur...</span><span class="sxs-lookup"><span data-stu-id="604e6-119">This may take a few minutes.</span></span>  
9. <span data-ttu-id="604e6-120">Endurhlaðið síðuna.</span><span class="sxs-lookup"><span data-stu-id="604e6-120">Refresh the page.</span></span>

## <a name="identify-the-urgent-planned-orders-for-the-item"></a><span data-ttu-id="604e6-121">Auðkenna áríðandi áætlaðar pantanir fyrir vöru</span><span class="sxs-lookup"><span data-stu-id="604e6-121">Identify the urgent planned orders for the item</span></span>
1. <span data-ttu-id="604e6-122">Opna vörunúmerasíu fyrir dálkur.</span><span class="sxs-lookup"><span data-stu-id="604e6-122">Open Item number column filter.</span></span>
2. <span data-ttu-id="604e6-123">Notið síu í reitnum „vörunúmer“ með gildinu „D0001“ og notið til þess „byrjar á“ síu virknitákn</span><span class="sxs-lookup"><span data-stu-id="604e6-123">Apply a filter on the "Item number" field, with a value of "D0001", using the "begins with" filter operator.</span></span>
3. <span data-ttu-id="604e6-124">Opnið dálkasíu pöntunardagsetningar.</span><span class="sxs-lookup"><span data-stu-id="604e6-124">Open Order date column filter.</span></span>
4. <span data-ttu-id="604e6-125">Nota síu á "Pöntunardagsetningu" svæðið, með gildandi dagsetningu, með síuvirkjanum "er nákvæmlega".</span><span class="sxs-lookup"><span data-stu-id="604e6-125">Apply a filter on the "Order date" field, with a value of current date, using the "is exactly" filter operator.</span></span>

## <a name="firm-all-the-urgent-orders-for-the-item"></a><span data-ttu-id="604e6-126">Staðfesta áríðandi pantanir fyrir vöru</span><span class="sxs-lookup"><span data-stu-id="604e6-126">Firm all the urgent orders for the item</span></span>
1. <span data-ttu-id="604e6-127">Merkið eða afmerkið allar línur í listanum.</span><span class="sxs-lookup"><span data-stu-id="604e6-127">In the list, mark or unmark all rows.</span></span>
2. <span data-ttu-id="604e6-128">Smellið á „Fastáætla“.</span><span class="sxs-lookup"><span data-stu-id="604e6-128">Click Firm.</span></span>
3. <span data-ttu-id="604e6-129">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="604e6-129">Click OK.</span></span>

