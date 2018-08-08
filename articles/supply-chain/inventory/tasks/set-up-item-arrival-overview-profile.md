---
title: "Setja upp komuyfirlitsreglu fyrir vöru"
description: "Þetta verk áherslu á uppsetningu komuyfirlitsregla."
author: perlynne
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 4b4b89f39008218721ef092ee01a93522d1461b1
ms.contentlocale: is-is
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-an-item-arrival-overview-profile"></a><span data-ttu-id="a63bb-103">Setja upp komuyfirlitsreglu fyrir vöru</span><span class="sxs-lookup"><span data-stu-id="a63bb-103">Set up an item arrival overview profile</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a63bb-104">Þetta verk áherslu á uppsetningu komuyfirlitsregla.</span><span class="sxs-lookup"><span data-stu-id="a63bb-104">This task focuses on the setup of an arrival overview profile.</span></span> <span data-ttu-id="a63bb-105">Komuyfirlitsreglu er safn reglna sem verður notað þegar síðan Komuyfirlit er opnað af notanda.</span><span class="sxs-lookup"><span data-stu-id="a63bb-105">The arrival overview profile is a collection of rules that will be applied when the Arrival overview page is opened by a user.</span></span> <span data-ttu-id="a63bb-106">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF.</span><span class="sxs-lookup"><span data-stu-id="a63bb-106">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="a63bb-107">Þetta verk myndi venjulega vera framkvæmt af starfsmanni í móttöku.</span><span class="sxs-lookup"><span data-stu-id="a63bb-107">This procedure would typically be carried out by a receiving clerk.</span></span>





1. <span data-ttu-id="a63bb-108">Fara í birgðastjórnun > Uppsetning > Dreifing > Komuyfirlitsreglur.</span><span class="sxs-lookup"><span data-stu-id="a63bb-108">Go to Inventory management > Setup > Distribution > Arrival overview profiles.</span></span>
2. <span data-ttu-id="a63bb-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="a63bb-109">Click New.</span></span>
    * <span data-ttu-id="a63bb-110">Þar er þú vinnur nánast alltaf í sama vöruhús við hlaða af fullhlöðnum vörubíl , ætti að stofna komuyfirlitsregla til að auðvelda ferlið við að skrá mótteknar vörur.</span><span class="sxs-lookup"><span data-stu-id="a63bb-110">Because you will almost always work in the same warehouse offloading full truck loads, you should create an arrival overview profile to simplify the process of registering received items.</span></span>  
3. <span data-ttu-id="a63bb-111">Færa inn gildi í reitnum heiti Komuyfirlitsregla .</span><span class="sxs-lookup"><span data-stu-id="a63bb-111">In the Arrival overview profile name field, type a value.</span></span>
4. <span data-ttu-id="a63bb-112">Í reitnum Sýna línur skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="a63bb-112">In the Show lines field, select an option.</span></span>
    * <span data-ttu-id="a63bb-113">Velja hvaða línur á að sýna fyrir innhreyfingarnar: Allar – Sýna allar línur óháð stöðu.</span><span class="sxs-lookup"><span data-stu-id="a63bb-113">Select which lines to show for the receipts:   All – Show all lines, regardless of status.</span></span>   <span data-ttu-id="a63bb-114">Í vinnslu -Sýna línur fyrir innhreyfingar þar sem vinnslu er Lokið eða lokið að Hluta.</span><span class="sxs-lookup"><span data-stu-id="a63bb-114">In progress – Show lines for receipts in which the progress is Complete or Partly.</span></span> <span data-ttu-id="a63bb-115">Það þýðir að fyrir hverja línu hefur annaðhvort fullt magn eða hluti magns verið skráð í komubók.</span><span class="sxs-lookup"><span data-stu-id="a63bb-115">This means that for each line, either the full quantity or part of the quantity has been registered in an arrival journal.</span></span>   <span data-ttu-id="a63bb-116">Ekki lokið -Sýna línur fyrir innhreyfingar þar sem vinnslustaða er Ekkert eða að Hluta.</span><span class="sxs-lookup"><span data-stu-id="a63bb-116">Not complete – Show lines for receipts in which the progress is None or Partly.</span></span> <span data-ttu-id="a63bb-117">Þetta þýðir að ekkert magn eða aðeins hluti þess hefur verið skráður í komubók, fyrir hverja línu.</span><span class="sxs-lookup"><span data-stu-id="a63bb-117">This means that for each line, nothing or only part of the quantity has been registered in an arrival journal.</span></span>  
5. <span data-ttu-id="a63bb-118">Útvíkka eða draga saman hlutann komutímavalkostir.</span><span class="sxs-lookup"><span data-stu-id="a63bb-118">Expand or collapse the Arrival options section.</span></span>
6. <span data-ttu-id="a63bb-119">Í reitinn Dagar frá og með skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a63bb-119">In the Days forward field, type a value.</span></span>
    * <span data-ttu-id="a63bb-120">Þetta stillir síu til að sýna línur innhreyfingar sem búist við að taka á móti innan nokkra daga (eftir því hvaða númer sett).</span><span class="sxs-lookup"><span data-stu-id="a63bb-120">This sets a filter to show the receipt lines expected to be received within the next few days (depending on the number you set).</span></span>  
7. <span data-ttu-id="a63bb-121">Í reitinn Dagar aftur í tímann skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a63bb-121">In the Days back field, type a value.</span></span>
    * <span data-ttu-id="a63bb-122">Þetta stillir síu til að sýna innhreyfingarlínur sem búist við að tekið sé á móti nokkrum dögum fyrir daginn í dag.</span><span class="sxs-lookup"><span data-stu-id="a63bb-122">This sets a filter to show the receipt lines expected to be received a number of days before today.</span></span>  
8. <span data-ttu-id="a63bb-123">Í reitinn Vöruhús skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a63bb-123">In the Warehouses field, type a value.</span></span>
    * <span data-ttu-id="a63bb-124">Sía á eina eða fleiri vöruhúsum.</span><span class="sxs-lookup"><span data-stu-id="a63bb-124">Filter on one or more warehouses.</span></span>  
9. <span data-ttu-id="a63bb-125">Í reitnum afhendingarmáti, skal færa inn gildi.</span><span class="sxs-lookup"><span data-stu-id="a63bb-125">In the Mode of delivery field, select a value.</span></span>
    * <span data-ttu-id="a63bb-126">Þetta stillir síu til að sýna aðeins innhreyfingarlínur með þennan Afhendingarmáta.</span><span class="sxs-lookup"><span data-stu-id="a63bb-126">This sets a filter to show only the receipt lines with this Mode of delivery.</span></span>  
10. <span data-ttu-id="a63bb-127">Í reitinn Nafn, veldu WHS.</span><span class="sxs-lookup"><span data-stu-id="a63bb-127">In the Name field, select WHS.</span></span>
11. <span data-ttu-id="a63bb-128">Í reitnum vöruhús, veldu vöruhús 24.</span><span class="sxs-lookup"><span data-stu-id="a63bb-128">In the Warehouse field, select warehouse 24.</span></span>
    * <span data-ttu-id="a63bb-129">Þetta er sjálfgefið vöruhús sem verður notað fyrir skráð innhreyfingarlínur sem nota þessa forstillingu.</span><span class="sxs-lookup"><span data-stu-id="a63bb-129">This is the default warehouse that will be used for registered receipt lines that use this profile.</span></span>  
12. <span data-ttu-id="a63bb-130">Í svæðinu Staðsetning skal velja Baydoor.</span><span class="sxs-lookup"><span data-stu-id="a63bb-130">In the Location field, select Baydoor.</span></span>
    * <span data-ttu-id="a63bb-131">Þetta er sjálfgefið staðsetning sem verður notað fyrir skráð innhreyfingarlínur sem nota þessa forstillingu.</span><span class="sxs-lookup"><span data-stu-id="a63bb-131">This is the default location that will be used for registered receipt lines that use this profile.</span></span>  
13. <span data-ttu-id="a63bb-132">Stækka eða fella saman hlutann upplýsingar um komufyrirspurn.</span><span class="sxs-lookup"><span data-stu-id="a63bb-132">Expand or collapse the Arrival query details section.</span></span>
14. <span data-ttu-id="a63bb-133">Í reitnum takmarka við svæði, veldu svæði 2.</span><span class="sxs-lookup"><span data-stu-id="a63bb-133">In the Restrict to site field, select site 2.</span></span>
    * <span data-ttu-id="a63bb-134">Þetta stillir síu til að sýna aðeins innhreyfingarlínur með þennan Stað.</span><span class="sxs-lookup"><span data-stu-id="a63bb-134">This sets a filter to show only the receipt lines with this site.</span></span>  
15. <span data-ttu-id="a63bb-135">Innkaupapantana Valkostinn er stillt á Já.</span><span class="sxs-lookup"><span data-stu-id="a63bb-135">Set the Purchase orders option to Yes.</span></span>
    * <span data-ttu-id="a63bb-136">Veljið innhreyfingarlínur úr innkaupapöntunum.</span><span class="sxs-lookup"><span data-stu-id="a63bb-136">Select receipt lines from purchase orders.</span></span>  
16. <span data-ttu-id="a63bb-137">Flutningspöntun Valkostinn er stillt á Já.</span><span class="sxs-lookup"><span data-stu-id="a63bb-137">Set the Transfer orders option to Yes.</span></span>
    * <span data-ttu-id="a63bb-138">Veljið innhreyfingarlínur úr flutningspöntun.</span><span class="sxs-lookup"><span data-stu-id="a63bb-138">Select receipt lines from transfer orders.</span></span>  
17. <span data-ttu-id="a63bb-139">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="a63bb-139">Click Save.</span></span>
18. <span data-ttu-id="a63bb-140">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="a63bb-140">Close the page.</span></span>

