--- 
title: "Fylgjast með keyrslu áætlanagerðar"
description: "Framleiðslustjóri vill sjá hvort keyrslu áætlunargerðar sé í gangi."
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1e08d9fd3388561563e6fb982416186a652b4ce2
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="fa6e3-103">Fylgjast með keyrslu áætlanagerðar</span><span class="sxs-lookup"><span data-stu-id="fa6e3-103">Monitor a master planning run</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fa6e3-104">Framleiðslustjóri vill sjá hvort keyrslu áætlunargerðar sé í gangi.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="fa6e3-105">Nota Sýnifyrirtækið USMF til að ljúka þetta ferli.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="fa6e3-106">Keyra aðaláætlanagerð</span><span class="sxs-lookup"><span data-stu-id="fa6e3-106">Run master planning</span></span>
1. <span data-ttu-id="fa6e3-107">Smellt er á aðaláætlanagerð.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-107">Click Master planning.</span></span>
    * <span data-ttu-id="fa6e3-108">Það er að finna á sjálfgefið mælaborð.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="fa6e3-109">Í reitinn áætlun skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="fa6e3-110">Dæmi: StaticPlan</span><span class="sxs-lookup"><span data-stu-id="fa6e3-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="fa6e3-111">Smellið á „Keyra“.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-111">Click Run.</span></span>
4. <span data-ttu-id="fa6e3-112">Velja skal Já í svæðisins rekja vinnslutíma.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="fa6e3-113">Sé þetta svæði valið. sleppa skrefinu.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="fa6e3-114">Í svæðinu Fjölda þráða skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="fa6e3-115">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="fa6e3-116">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-116">Click Filter.</span></span>
8. <span data-ttu-id="fa6e3-117">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="fa6e3-118">Merktu línuna þar sem reiturinn er = vörunúmer.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="fa6e3-119">Í reitinn Skilyrði skal slá inn eða veldu gildi.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="fa6e3-120">Til dæmis: T0001</span><span class="sxs-lookup"><span data-stu-id="fa6e3-120">Example: T0001</span></span>  
10. <span data-ttu-id="fa6e3-121">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-121">Click OK.</span></span>
11. <span data-ttu-id="fa6e3-122">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="fa6e3-123">Fylgjast með áætlanagerð keyra</span><span class="sxs-lookup"><span data-stu-id="fa6e3-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="fa6e3-124">Smellt er á ferill.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-124">Click History.</span></span>
2. <span data-ttu-id="fa6e3-125">Smellt er á Fyrirspurnir.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-125">Click Inquiries.</span></span>
3. <span data-ttu-id="fa6e3-126">Smella á lengd vinnsluverka</span><span class="sxs-lookup"><span data-stu-id="fa6e3-126">Click Process task duration.</span></span>
4. <span data-ttu-id="fa6e3-127">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="fa6e3-128">Fyrir hverja vöru er hægt að fá yfirlit yfir hve lengi það tók að klára hvert skref áætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="fa6e3-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  


