---
title: Skilgreina staðalkostnað fyrir útgjöld og laun
description: Þetta ferli sýnir hvernig á að setja upp staðalkostnaður fyrir vinnuafl og útgjöld í verkefni.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f89590c87aec1a7200e95aeac6b2765fc64bb623
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572397"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="82778-103">Skilgreina staðalkostnað fyrir útgjöld og laun</span><span class="sxs-lookup"><span data-stu-id="82778-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82778-104">Þetta ferli sýnir hvernig á að setja upp staðalkostnaður fyrir vinnuafl og útgjöld í verkefni.</span><span class="sxs-lookup"><span data-stu-id="82778-104">This procedure shows you how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="82778-105">Þetta verkefni notar USSI-gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="82778-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="82778-106">Farið er í Verkefnastjórnun og bókhald > Uppsetning > Verð > Kostnaðarverð (klukkustund).</span><span class="sxs-lookup"><span data-stu-id="82778-106">Go to Project management and accounting > Setup > Prices > Cost price (hour).</span></span>
2. <span data-ttu-id="82778-107">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="82778-107">Click New.</span></span>
3. <span data-ttu-id="82778-108">Í reitnum Gildisdagsetning skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="82778-108">In the Effective date field, enter a date.</span></span>
4. <span data-ttu-id="82778-109">Í reitinn kostnaðarverð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="82778-109">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="82778-110">Hægt er að setja upp staðlað kostnaðarverð fyrir verktegund, eða setja upp kostnaðarverð eftir starfsmannanúmeri, verknúmeri, tegund, dagsetningu eða blöndu af þessu.</span><span class="sxs-lookup"><span data-stu-id="82778-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="82778-111">Hið raunverulega kostnaðarverð sem er notað er kostnaðarverðið með hæsta stig upplýsinga.</span><span class="sxs-lookup"><span data-stu-id="82778-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="82778-112">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="82778-112">Click Save.</span></span>
6. <span data-ttu-id="82778-113">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="82778-113">Close the page.</span></span>
7. <span data-ttu-id="82778-114">Farið er í Verkefnastjórnun Og bókhald > Uppsetning > Verð > Söluverð (klukkustund).</span><span class="sxs-lookup"><span data-stu-id="82778-114">Go to Project management and accounting > Setup > Prices > Sales price (hour).</span></span>
8. <span data-ttu-id="82778-115">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="82778-115">Click New.</span></span>
9. <span data-ttu-id="82778-116">Í reitnum Gildisdagsetning skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="82778-116">In the Effective date field, enter a date.</span></span>
10. <span data-ttu-id="82778-117">Í reitnum Gildir fyrir skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="82778-117">In the Valid for field, select an option.</span></span>
11. <span data-ttu-id="82778-118">Sláðu inn tölu í svæði Verðlagning.</span><span class="sxs-lookup"><span data-stu-id="82778-118">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="82778-119">Hægt er að setja upp staðlað söluverð fyrir klukkustundafærslur eða verktegund.</span><span class="sxs-lookup"><span data-stu-id="82778-119">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="82778-120">Einnig er hægt að setja upp söluverð eftir starfsmannanúmeri, verknúmeri, tegund, færsludagsetningu eða hvers konar samsetningum þessara atriða.</span><span class="sxs-lookup"><span data-stu-id="82778-120">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="82778-121">Raunsöluverð, sem er beitt þegar starfsmaður slær færslu inn i færslubókina Þóknun, er það söluverð með hæst upplýsingastig.</span><span class="sxs-lookup"><span data-stu-id="82778-121">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="82778-122">Til dæmis, ef bæði almennt söluverð og söluverð háð tilteknum starfsmanni eru sett upp velur kerfið söluverð háð tilteknum starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="82778-122">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
12. <span data-ttu-id="82778-123">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="82778-123">Click Save.</span></span>
13. <span data-ttu-id="82778-124">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="82778-124">Close the page.</span></span>
14. <span data-ttu-id="82778-125">Farið er í Verkefnastjórnun Og bókhald > Uppsetning > Verð > Kostnaðarverð (útgjöld).</span><span class="sxs-lookup"><span data-stu-id="82778-125">Go to Project management and accounting > Setup > Prices > Cost price (expense).</span></span>
15. <span data-ttu-id="82778-126">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="82778-126">Click New.</span></span>
16. <span data-ttu-id="82778-127">Í reitnum Gildisdagsetning skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="82778-127">In the Effective date field, enter a date.</span></span>
17. <span data-ttu-id="82778-128">Í reitinn kostnaðarverð skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="82778-128">In the Cost price field, enter a number.</span></span>
    * <span data-ttu-id="82778-129">Hægt er að fylla út í mörg svæði en þetta er lágmark til að geta vista færslu.</span><span class="sxs-lookup"><span data-stu-id="82778-129">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
18. <span data-ttu-id="82778-130">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="82778-130">Click Save.</span></span>
19. <span data-ttu-id="82778-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="82778-131">Close the page.</span></span>
20. <span data-ttu-id="82778-132">Farið er í Verkefnastjórnun Og bókhald > Uppsetning > Verð > Söluverð (útgjöld).</span><span class="sxs-lookup"><span data-stu-id="82778-132">Go to Project management and accounting > Setup > Prices > Sales price (expense).</span></span>
21. <span data-ttu-id="82778-133">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="82778-133">Click New.</span></span>
22. <span data-ttu-id="82778-134">Í reitnum Gildisdagsetning skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="82778-134">In the Effective date field, enter a date.</span></span>
23. <span data-ttu-id="82778-135">Í reitnum Gildir fyrir skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="82778-135">In the Valid for field, select an option.</span></span>
24. <span data-ttu-id="82778-136">Sláðu inn tölu í svæði Verðlagning.</span><span class="sxs-lookup"><span data-stu-id="82778-136">In the Pricing field, enter a number.</span></span>
    * <span data-ttu-id="82778-137">Raunsöluverð, sem er notað þegar starfsmaður færir færslur inn í kostnaðarbók er söluverðið með hæst upplýsingastig.</span><span class="sxs-lookup"><span data-stu-id="82778-137">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="82778-138">Til dæmis, ef bæði almennt söluverð og söluverð háð tilteknum starfsmanni eru sett upp velur kerfið söluverð háð tilteknum starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="82778-138">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
25. <span data-ttu-id="82778-139">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="82778-139">Click Save.</span></span>

