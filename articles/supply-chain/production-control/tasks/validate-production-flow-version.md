--- 
title: "Villuleita í framleiðsluflæði og útgáfu"
description: "Þessi verklýsing sýnir hvernig á að stofna nýtt framleiðsluflæði og fyrstu útgáfu fyrir lean-framleiðslu."
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LeanProductionFlow
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 4ae4c5f55d317a99e23ba6e76fc50ddece1e55a1
ms.contentlocale: is-is
ms.lasthandoff: 09/14/2018

---
# <a name="validate-a-production-flow-and-version"></a><span data-ttu-id="4550b-103">Villuleita í framleiðsluflæði og útgáfu</span><span class="sxs-lookup"><span data-stu-id="4550b-103">Validate a production flow and version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4550b-104">Þessi verklýsing sýnir hvernig á að stofna nýtt framleiðsluflæði og fyrstu útgáfu fyrir lean-framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="4550b-104">This procedure shows how to create a new production flow and a first version for lean manufacturing.</span></span> <span data-ttu-id="4550b-105">Frumskilyrði: Skilgreina þarf framleiðslufæribreytur fyrir Lean-framleiðslu og mælieiningar fyrir klasatíma.</span><span class="sxs-lookup"><span data-stu-id="4550b-105">Prerequisites: The production parameters for Lean manufacturing and the units of measure for class time must be defined.</span></span> <span data-ttu-id="4550b-106">Það þarf að skilgreina virðisstraum og framleiðsluflokk.</span><span class="sxs-lookup"><span data-stu-id="4550b-106">You need to define a Value stream and a Production group.</span></span> <span data-ttu-id="4550b-107">Skoðið hvítblöð í Lean-framleiðslu til að kynna þér hugtökin framleiðsluflæði og verkþætti.</span><span class="sxs-lookup"><span data-stu-id="4550b-107">Refer to the white papers on Lean manufacturing to familiarize yourself with the concepts of production flows and activities.</span></span> <span data-ttu-id="4550b-108">Þetta ferli vísar í lögaðilinn USMF í sýnigögnum.</span><span class="sxs-lookup"><span data-stu-id="4550b-108">This procedure refers to the legal entity USMF in demo data.</span></span> <span data-ttu-id="4550b-109">Hins vegar, ef við gerum ráð fyrir að lögaðilinn sé skilgreindur fyrir Lean-framleiðslu, er hægt að nota aðra lögaðila.</span><span class="sxs-lookup"><span data-stu-id="4550b-109">However, assuming that the legal entity is configured for Lean manufacturing, other legal entities can be used.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="4550b-110">Stofna framleiðsluflæði</span><span class="sxs-lookup"><span data-stu-id="4550b-110">Create a production flow</span></span>
1. <span data-ttu-id="4550b-111">Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.</span><span class="sxs-lookup"><span data-stu-id="4550b-111">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="4550b-112">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="4550b-112">Click New.</span></span>
3. <span data-ttu-id="4550b-113">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="4550b-113">In the Name field, type a value.</span></span>
4. <span data-ttu-id="4550b-114">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="4550b-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4550b-115">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="4550b-115">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="4550b-116">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="4550b-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4550b-117">Virðisstraumur er rekstrareining sem nær yfir alla verkþætti og flæði virðisstraumsins.</span><span class="sxs-lookup"><span data-stu-id="4550b-117">A value stream is an operating unit that spans over all activities and flows of the value stream.</span></span>   <span data-ttu-id="4550b-118">Á þessu stigi takmarkast rekstrareiningar við lögaðila og hafa engin frekari aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="4550b-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="4550b-119">Í reitnum Framleiðsluflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="4550b-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="4550b-120">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="4550b-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4550b-121">Framleiðsluflokkar leyfa skilgreiningu á efni, vinnu og vív-lyklum fyrir framleiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="4550b-121">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="4550b-122">Til að tengja bókhaldssamhengi við framleiðsluflæði verður að velja framleiðsluflokk.</span><span class="sxs-lookup"><span data-stu-id="4550b-122">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="4550b-123">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="4550b-123">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="4550b-124">Stofna útgáfu framleiðsluflæðis</span><span class="sxs-lookup"><span data-stu-id="4550b-124">Create a production flow version</span></span>
1. <span data-ttu-id="4550b-125">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="4550b-125">Click Add.</span></span>
2. <span data-ttu-id="4550b-126">Færa inn dagsetningu og tíma í dagsetningarsvæði Gildistíma.</span><span class="sxs-lookup"><span data-stu-id="4550b-126">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="4550b-127">Hægt er að uppfæra lokadag útgáfu hvenær sem er, jafnvel fyrir virkar útgáfur.</span><span class="sxs-lookup"><span data-stu-id="4550b-127">You can update the Expiration date of the version at any given time, even for active versions.</span></span> <span data-ttu-id="4550b-128">Notaðu gildistíma útgáfu til að áætla áfanga úr útgáfu.</span><span class="sxs-lookup"><span data-stu-id="4550b-128">Use the expiration of the version to plan for a phase out of a version.</span></span>  
3. <span data-ttu-id="4550b-129">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="4550b-129">Click OK.</span></span>
4. <span data-ttu-id="4550b-130">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="4550b-130">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="4550b-131">Í reitnum Eining skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="4550b-131">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="4550b-132">Velja verkeiningu.</span><span class="sxs-lookup"><span data-stu-id="4550b-132">Select the Takt unit.</span></span>
7. <span data-ttu-id="4550b-133">Færið inn tölu í reitnum Framleiðslutími á einingu.</span><span class="sxs-lookup"><span data-stu-id="4550b-133">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="4550b-134">Skilgreina valinn framleiðslutíma á einingu fyrir verkstýringu á útgáfu framleiðsluflæðisins.</span><span class="sxs-lookup"><span data-stu-id="4550b-134">For the takt control of the production flow version, define a targeted average takt time.</span></span>   <span data-ttu-id="4550b-135">Framleiðslutími er skilgreindur sem magn á hvert tímabil.</span><span class="sxs-lookup"><span data-stu-id="4550b-135">The takt is defined as quantity  per time period.</span></span>  <span data-ttu-id="4550b-136">Í gefnu dæmi er framleiðslutíminn 0,2 klukkustundir á 10 stykki.</span><span class="sxs-lookup"><span data-stu-id="4550b-136">In the given example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="4550b-137">Fyrir vinnutíma upp á 8 klukkustundir samsvarar þetta daglegri afkastagetu fyrir 400 stykki.</span><span class="sxs-lookup"><span data-stu-id="4550b-137">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="4550b-138">Í reitinn Magn á talningu skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="4550b-138">In the Quantity per cycle field, enter a number.</span></span>
9. <span data-ttu-id="4550b-139">Útvíkka eða draga saman Útgáfu upplýsingahluta.</span><span class="sxs-lookup"><span data-stu-id="4550b-139">Expand or collapse the Version details section.</span></span>
10. <span data-ttu-id="4550b-140">Í reitnum Lágmark framleiðslutíma á einingu skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="4550b-140">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="4550b-141">Lágmarksframleiðslutími á einingu verður að vera lægri en eða jafnt og meðalframleiðslutími á einingu.</span><span class="sxs-lookup"><span data-stu-id="4550b-141">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="4550b-142">Í reitnum Hámark framleiðslutíma á einingu skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="4550b-142">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="4550b-143">Hámarksframleiðslutími á einingu verður að vera hærri en eða jafnt og meðalframleiðslutími á einingu.</span><span class="sxs-lookup"><span data-stu-id="4550b-143">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="4550b-144">Færið inn fjölda daga á tímabili fyrir raunferlistíma</span><span class="sxs-lookup"><span data-stu-id="4550b-144">Enter a number of days in the Period for actual cycle time</span></span>
    * <span data-ttu-id="4550b-145">Tímabil fyrir raunferlistíma er sá fjöldi daga sem vinnslum er safnað saman úr raunverulega mínútu til baka til að reikna raunferlistíma.</span><span class="sxs-lookup"><span data-stu-id="4550b-145">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="4550b-146">Gildinu er hægt að breyta hvenær sem er og er aðeins notað fyrir útreikning á tímum raunferlistíma.</span><span class="sxs-lookup"><span data-stu-id="4550b-146">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="4550b-147">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="4550b-147">Click Save.</span></span>


