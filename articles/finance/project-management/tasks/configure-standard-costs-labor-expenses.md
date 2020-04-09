---
title: Skilgreina staðalkostnað fyrir útgjöld og laun
description: Þetta efni útskýrir hvernig á að setja upp staðalkostnaður fyrir vinnuafl og útgjöld í verkefni.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 51bbe52d70bae11cb0c95e9544f951f0fcc605f5
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140094"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="f58bb-103">Skilgreina staðalkostnað fyrir útgjöld og laun</span><span class="sxs-lookup"><span data-stu-id="f58bb-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f58bb-104">Þetta efni útskýrir hvernig á að setja upp staðalkostnaður fyrir vinnuafl og útgjöld í verkefni.</span><span class="sxs-lookup"><span data-stu-id="f58bb-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="f58bb-105">Þetta verkefni notar USSI-gagnasafn.</span><span class="sxs-lookup"><span data-stu-id="f58bb-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="f58bb-106">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Verkefnastjórnun og bókhald > Uppsetning > Verð > Kostnaðarverð (klukkustund)**.</span><span class="sxs-lookup"><span data-stu-id="f58bb-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="f58bb-107">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f58bb-107">Select **New**.</span></span>
3. <span data-ttu-id="f58bb-108">Í reitnum **Gildisdagsetning** skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="f58bb-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="f58bb-109">Í reitinn **Kostnaðarverð** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f58bb-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="f58bb-110">Hægt er að setja upp staðlað kostnaðarverð fyrir verktegund, eða setja upp kostnaðarverð eftir starfsmannanúmeri, verknúmeri, tegund, dagsetningu eða blöndu af þessu.</span><span class="sxs-lookup"><span data-stu-id="f58bb-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="f58bb-111">Hið raunverulega kostnaðarverð sem er notað er kostnaðarverðið með hæsta stig upplýsinga.</span><span class="sxs-lookup"><span data-stu-id="f58bb-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="f58bb-112">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f58bb-112">Select **Save**.</span></span>
6. <span data-ttu-id="f58bb-113">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Verkefnastjórnun og bókhald > Uppsetning > Verð > Söluverð (klukkustund)**.</span><span class="sxs-lookup"><span data-stu-id="f58bb-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="f58bb-114">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f58bb-114">Select **New**.</span></span>
8. <span data-ttu-id="f58bb-115">Í reitnum **Gildisdagsetning** skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="f58bb-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="f58bb-116">Í reitnum **Gildir fyrir** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="f58bb-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="f58bb-117">Sláðu inn tölu í retinn **Verðlagning**.</span><span class="sxs-lookup"><span data-stu-id="f58bb-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="f58bb-118">Hægt er að setja upp staðlað söluverð fyrir klukkustundafærslur eða verktegund.</span><span class="sxs-lookup"><span data-stu-id="f58bb-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="f58bb-119">Einnig er hægt að setja upp söluverð eftir starfsmannanúmeri, verknúmeri, tegund, færsludagsetningu eða hvers konar samsetningum þessara atriða.</span><span class="sxs-lookup"><span data-stu-id="f58bb-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="f58bb-120">Raunsöluverð, sem er beitt þegar starfsmaður slær færslu inn i færslubókina Þóknun, er það söluverð með hæst upplýsingastig.</span><span class="sxs-lookup"><span data-stu-id="f58bb-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="f58bb-121">Til dæmis, ef bæði almennt söluverð og söluverð háð tilteknum starfsmanni eru sett upp velur kerfið söluverð háð tilteknum starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="f58bb-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="f58bb-122">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f58bb-122">Select **Save**.</span></span>
12. <span data-ttu-id="f58bb-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="f58bb-123">Close the page.</span></span>
13. <span data-ttu-id="f58bb-124">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Verkefnastjórnun og bókhald > Uppsetning > Verð > Kostnaðarverð (kostnaður)**.</span><span class="sxs-lookup"><span data-stu-id="f58bb-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="f58bb-125">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f58bb-125">Select **New**.</span></span>
15. <span data-ttu-id="f58bb-126">Í reitnum **Gildisdagsetning** skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="f58bb-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="f58bb-127">Í reitinn **Kostnaðarverð** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="f58bb-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="f58bb-128">Hægt er að fylla út í mörg svæði en þetta er lágmark til að geta vista færslu.</span><span class="sxs-lookup"><span data-stu-id="f58bb-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="f58bb-129">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f58bb-129">Select **Save**.</span></span>
18. <span data-ttu-id="f58bb-130">Í skoðunarrúðunni ferðu í **Kerfiseiningar > Verkefnastjórnun og bókhald > Uppsetning > Verð > Söluverð (kostnaður)**.</span><span class="sxs-lookup"><span data-stu-id="f58bb-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="f58bb-131">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="f58bb-131">Select **New**.</span></span>
20. <span data-ttu-id="f58bb-132">Í reitnum **Gildisdagsetning** skal slá inn dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="f58bb-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="f58bb-133">Í reitnum **Gildir fyrir** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="f58bb-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="f58bb-134">Sláðu inn tölu í retinn **Verðlagning**.</span><span class="sxs-lookup"><span data-stu-id="f58bb-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="f58bb-135">Raunsöluverð, sem er notað þegar starfsmaður færir færslur inn í kostnaðarbók er söluverðið með hæst upplýsingastig.</span><span class="sxs-lookup"><span data-stu-id="f58bb-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="f58bb-136">Til dæmis, ef bæði almennt söluverð og söluverð háð tilteknum starfsmanni eru sett upp velur kerfið söluverð háð tilteknum starfsmanni.</span><span class="sxs-lookup"><span data-stu-id="f58bb-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="f58bb-137">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="f58bb-137">Select **Save**.</span></span>

