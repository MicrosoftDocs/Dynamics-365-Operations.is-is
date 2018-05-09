--- 
title: "Stofna útgáfu framleiðsluflæðis"
description: "Þetta ferli sýnir hvernig ný útgáfa framleiðsluflæðis er stofnuð."
author: cvocph
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0a241ba056051eccb168b5aa9bfd437b519b2bd9
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-production-flow-version"></a><span data-ttu-id="9e79b-103">Stofna útgáfu framleiðsluflæðis</span><span class="sxs-lookup"><span data-stu-id="9e79b-103">Create a production flow version</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9e79b-104">Þetta ferli sýnir hvernig ný útgáfa framleiðsluflæðis er stofnuð.</span><span class="sxs-lookup"><span data-stu-id="9e79b-104">This procedure focuses on creating a new production flow version.</span></span> <span data-ttu-id="9e79b-105">Fyrir þetta ferli verður að skilgreina framleiðslufæribreytur fyrir lean-framleiðslu og mælieiningar fyrir klasatíma.</span><span class="sxs-lookup"><span data-stu-id="9e79b-105">For this procedure, the production parameters for lean manufacturing and the units of measurement for class time must be defined.</span></span> <span data-ttu-id="9e79b-106">Einnig þarf að skilgreina virðisstraum og framleiðsluflokk.</span><span class="sxs-lookup"><span data-stu-id="9e79b-106">You also need to define a value stream and a production group.</span></span> <span data-ttu-id="9e79b-107">Frekari upplýsingar um framleiðsluflæði og aðgerðir í lean-framleiðslu má sjá í hvítblöð um Lean-framleiðslu í Microsoft Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="9e79b-107">To learn more about production flows and activities in lean manufacturing, see the white papers on Lean manufacturing for Microsoft Dynamics AX.</span></span> <span data-ttu-id="9e79b-108">Sýnigögn fyrirtækisins til að stofna þetta ferli er USMF.</span><span class="sxs-lookup"><span data-stu-id="9e79b-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-production-flow"></a><span data-ttu-id="9e79b-109">Stofna framleiðsluflæði</span><span class="sxs-lookup"><span data-stu-id="9e79b-109">Create a production flow</span></span>
1. <span data-ttu-id="9e79b-110">Fara í Framleiðslustýringar > Uppsetning > Framleiðsluflæði fyrir lean > Framleiðsluflæði.</span><span class="sxs-lookup"><span data-stu-id="9e79b-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="9e79b-111">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="9e79b-111">Click New.</span></span>
3. <span data-ttu-id="9e79b-112">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9e79b-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="9e79b-113">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="9e79b-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9e79b-114">Í reitnum Heiti skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9e79b-114">In the Name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9e79b-115">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9e79b-115">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9e79b-116">Veljið rekstrareiningu af gerðinni virðisstraumur.</span><span class="sxs-lookup"><span data-stu-id="9e79b-116">Select an operating unit of type value stream.</span></span> <span data-ttu-id="9e79b-117">Virðisstraumur er rekstrareining sem nær yfir allar aðgerðir og flæði virðisstraumsins.</span><span class="sxs-lookup"><span data-stu-id="9e79b-117">A value stream is an operating unit that spans all activities and flows of the value stream.</span></span> <span data-ttu-id="9e79b-118">Á þessu stigi takmarkast rekstrareiningar við lögaðila og hafa engin frekari aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="9e79b-118">At this stage, operating units are limited to a legal entity and have no further functionality.</span></span>  
7. <span data-ttu-id="9e79b-119">Í reitnum Framleiðsluflokkur skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="9e79b-119">In the Production group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="9e79b-120">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="9e79b-120">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="9e79b-121">Veljið framleiðsluflokk fyrir framleiðsluflæðið.</span><span class="sxs-lookup"><span data-stu-id="9e79b-121">Select a production group for the production flow.</span></span> <span data-ttu-id="9e79b-122">Framleiðsluflokkar leyfa skilgreiningu á efni, vinnu og vív-lyklum fyrir framleiðsluferli.</span><span class="sxs-lookup"><span data-stu-id="9e79b-122">Production groups allow the definition of material, labor, and WIP accounts for a production process.</span></span> <span data-ttu-id="9e79b-123">Til að tengja bókhaldssamhengi við framleiðsluflæði verður að velja framleiðsluflokk.</span><span class="sxs-lookup"><span data-stu-id="9e79b-123">To associate the accounting context to a production flow, a production group must be selected.</span></span>  
9. <span data-ttu-id="9e79b-124">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9e79b-124">Click Save.</span></span>

## <a name="create-a-production-flow-version"></a><span data-ttu-id="9e79b-125">Stofna útgáfu framleiðsluflæðis</span><span class="sxs-lookup"><span data-stu-id="9e79b-125">Create a production flow version</span></span>
1. <span data-ttu-id="9e79b-126">Smelltu á Bæta við.</span><span class="sxs-lookup"><span data-stu-id="9e79b-126">Click Add.</span></span>
2. <span data-ttu-id="9e79b-127">Færa inn dagsetningu og tíma í dagsetningarsvæði Gildistíma.</span><span class="sxs-lookup"><span data-stu-id="9e79b-127">In the Expiration date field, enter a date and time.</span></span>
    * <span data-ttu-id="9e79b-128">Ef þörf er hægt að skilgreina lokadag fyrir útgáfu.</span><span class="sxs-lookup"><span data-stu-id="9e79b-128">If required, define an Expiration date for the version.</span></span> <span data-ttu-id="9e79b-129">Hægt er að uppfæra hvenær sem er, jafnvel fyrir virkar útgáfur.</span><span class="sxs-lookup"><span data-stu-id="9e79b-129">You can update it at any given time, even for active versions.</span></span> <span data-ttu-id="9e79b-130">Hægt er að nota hana til að áætla að draga smám saman úr útgáfu.</span><span class="sxs-lookup"><span data-stu-id="9e79b-130">You can use it to plan to phase out a version.</span></span>  
3. <span data-ttu-id="9e79b-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="9e79b-131">Click OK.</span></span>
4. <span data-ttu-id="9e79b-132">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="9e79b-132">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="9e79b-133">Í reitnum Eining skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="9e79b-133">In the Unit field, type a value.</span></span>
6. <span data-ttu-id="9e79b-134">Leysa breytir verkeiningu.</span><span class="sxs-lookup"><span data-stu-id="9e79b-134">ResolveChanges the Takt unit.</span></span>
7. <span data-ttu-id="9e79b-135">Færið inn tölu í reitnum Framleiðslutími á einingu.</span><span class="sxs-lookup"><span data-stu-id="9e79b-135">In the Average takt time field, enter a number.</span></span>
    * <span data-ttu-id="9e79b-136">Skilgreina framleiðslutíma á einingu fyrir útgáfuna.</span><span class="sxs-lookup"><span data-stu-id="9e79b-136">Define the Average takt time of the version.</span></span> <span data-ttu-id="9e79b-137">Skilgreina valinn framleiðslutíma á einingu fyrir verkstýringu á útgáfu framleiðsluflæðisins.</span><span class="sxs-lookup"><span data-stu-id="9e79b-137">For the takt control of the production flow version, define a targeted average takt time.</span></span> <span data-ttu-id="9e79b-138">Framleiðslutími er skilgreindur sem magn á hvert tímabil.</span><span class="sxs-lookup"><span data-stu-id="9e79b-138">The takt is defined as quantity per time period.</span></span> <span data-ttu-id="9e79b-139">Í dæminu er framleiðslutíminn 0,2 klukkustundir á 10 stykki.</span><span class="sxs-lookup"><span data-stu-id="9e79b-139">In the example, the takt time is 0.2 hours per 10 pieces.</span></span> <span data-ttu-id="9e79b-140">Fyrir vinnutíma upp á 8 klukkustundir samsvarar þetta daglegri afkastagetu fyrir 400 stykki.</span><span class="sxs-lookup"><span data-stu-id="9e79b-140">For a working time of 8 hours, this corresponds to a daily throughput capacity of 400 pieces.</span></span>  
8. <span data-ttu-id="9e79b-141">Í reitinn Magn á talningu skal slá inn tölu.</span><span class="sxs-lookup"><span data-stu-id="9e79b-141">In the Quantity per cycle field, enter a number.</span></span>
    * <span data-ttu-id="9e79b-142">Skilgreina magn á ferli sem tengist framleiðslutíma á einingu.</span><span class="sxs-lookup"><span data-stu-id="9e79b-142">Define the quantity per cycle related to the Average takt time.</span></span>  
9. <span data-ttu-id="9e79b-143">Víxla útvíkkun á liðnum Útgáfa upplýsinga.</span><span class="sxs-lookup"><span data-stu-id="9e79b-143">Toggle the expansion of the Version details section.</span></span>
10. <span data-ttu-id="9e79b-144">Í reitnum Lágmark framleiðslutíma á einingu skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="9e79b-144">In the Minimum takt time field, enter a number.</span></span>
    * <span data-ttu-id="9e79b-145">Skilgreina lágmarksframleiðslutíma á einingu.</span><span class="sxs-lookup"><span data-stu-id="9e79b-145">Define the minimum takt time.</span></span> <span data-ttu-id="9e79b-146">Lágmarksframleiðslutími á einingu verður að vera lægri en eða jafnt og meðalframleiðslutími á einingu.</span><span class="sxs-lookup"><span data-stu-id="9e79b-146">The minimum takt time must be less than or equal to the average takt time.</span></span>  
11. <span data-ttu-id="9e79b-147">Í reitnum Hámark framleiðslutíma á einingu skal færa inn tölu.</span><span class="sxs-lookup"><span data-stu-id="9e79b-147">In the Maximum takt time field, enter a number.</span></span>
    * <span data-ttu-id="9e79b-148">Hámarksframleiðslutími á einingu verður að vera hærri en eða jafnt og meðalframleiðslutími á einingu.</span><span class="sxs-lookup"><span data-stu-id="9e79b-148">The maximum takt time must be higher than or equal to the Average takt time.</span></span>  
12. <span data-ttu-id="9e79b-149">Í reitinn Tímabil fyrir rauntíma ferlis (dagar) skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="9e79b-149">In the Period for actual cycle time (days) field, enter a number.</span></span>
    * <span data-ttu-id="9e79b-150">Færið inn fjölda daga á tímabili fyrir raunferlistíma.</span><span class="sxs-lookup"><span data-stu-id="9e79b-150">Enter the number of days in the Period for actual cycle time.</span></span> <span data-ttu-id="9e79b-151">Tímabil fyrir raunferlistíma er sá fjöldi daga sem vinnslum er safnað saman úr raunverulega mínútu til baka til að reikna raunferlistíma.</span><span class="sxs-lookup"><span data-stu-id="9e79b-151">The period for actual cycle time is the number of days that jobs are aggregated from the actual minute backwards to calculate the actual cycle time.</span></span> <span data-ttu-id="9e79b-152">Gildinu er hægt að breyta hvenær sem er og er aðeins notað fyrir útreikning á tímum raunferlistíma.</span><span class="sxs-lookup"><span data-stu-id="9e79b-152">The value can be changed at any time and is only used for the calculation of the actual cycle times.</span></span>  
13. <span data-ttu-id="9e79b-153">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="9e79b-153">Click Save.</span></span>


