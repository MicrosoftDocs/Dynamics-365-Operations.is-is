---
title: "Setja upp forsendur fyrir stjórnun"
description: "Notið þetta ferli til að virkja sjórnunarferli ósamkvæmni."
author: perlynne
manager: AnnBe
ms.date: 06/07/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0e7f66cccd76e5326fce75d1a13aff294c16fb9b
ms.openlocfilehash: 842a9441158defca74d1b203a1b2509773ba8919
ms.contentlocale: is-is
ms.lasthandoff: 09/12/2017

---
# <a name="set-up-prerequisites-for-management"></a><span data-ttu-id="7cbf3-103">Setja upp forsendur fyrir stjórnun</span><span class="sxs-lookup"><span data-stu-id="7cbf3-103">Set up prerequisites for management</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7cbf3-104">Notið þetta ferli til að virkja sjórnunarferli ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-104">Use this procedure to enable nonconformance management processes.</span></span> <span data-ttu-id="7cbf3-105">Ósamkvæmni lýsir ferli eða vöru sem uppfyllir ekki gæðastaðla, þar sem uppruni og gerð vandamálsins eru í lýsandi upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-105">A nonconformance describes a procedure or item that has a quality problem, where the descriptive information includes the source and type of problem.</span></span> <span data-ttu-id="7cbf3-106">Þessi aðferð notar sýnifyrirtækið USMF.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-106">This procedure uses the USMF demo data company.</span></span> <span data-ttu-id="7cbf3-107">Þetta ferli er yfirleitt framkvæmt af starfsmanni á sviði gæða.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-107">This procedure is typically performed by a quality manager.</span></span>


## <a name="enable-quality-management-processes-within-the-company"></a><span data-ttu-id="7cbf3-108">Virkja ferli gæðastjórnunar innan fyrirtækisins:</span><span class="sxs-lookup"><span data-stu-id="7cbf3-108">Enable quality management processes within the company</span></span>
1. <span data-ttu-id="7cbf3-109">Fara í Birgðastjórnun > Uppsetning > Birgðir og færibreytur vöruhúsakerfis.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="7cbf3-110">Smellið á flipann gæðastjórnun.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="7cbf3-111">Velja skal Já í svæðinu á Notkun gæðastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-111">Select Yes in the Use quality management field.</span></span>
    * <span data-ttu-id="7cbf3-112">Veljið þessa færibreytu til að virkja ferli gæðastjórnunar fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-112">Select this parameter to enable quality management processes for the company.</span></span>  
4. <span data-ttu-id="7cbf3-113">Í reitinn Tímagjald skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-113">In the Hourly rate field, enter a number.</span></span>
    * <span data-ttu-id="7cbf3-114">Nota skal reitinn tímagjald til að færa inn tímagjald fyrir vinnu í gjaldmiðli landsins.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-114">Use the Hourly rate field to enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="7cbf3-115">Tímagjaldið er notuð til að reikna kostnað fyrir aðgerðir sem tengjast ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-115">The hourly rate is used for calculating costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="7cbf3-116">Tímagjaldið og reiknaður kostnaður veita tilvísunarupplýsingar fyrir ósamkvæmni og hafa ekki samskipti við aðrar aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-116">The hourly rate and calculated costs provide reference information for a nonconformance, and they do not interact with other functionality.</span></span>  
5. <span data-ttu-id="7cbf3-117">Smellt er á uppsetningu Skýrslu.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-117">Click Report setup.</span></span>
    * <span data-ttu-id="7cbf3-118">Þessi síða gerir þér kleift að skilgreina gerð athugasemdar fyrir gæðapöntun sem verða notaðir fyrir mismunandi gerðir gæðastjórnunarskýrslurnar.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-118">This page allows you define the quality report note types that will be used on different kinds of quality management reports.</span></span>  
6. <span data-ttu-id="7cbf3-119">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-119">Close the page.</span></span>
7. <span data-ttu-id="7cbf3-120">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-120">Close the page.</span></span>

## <a name="enable-user-for-nonconformance-processing"></a><span data-ttu-id="7cbf3-121">Virkja notenda fyrir ósamkvæmnivinnslu.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-121">Enable user for nonconformance processing</span></span>
1. <span data-ttu-id="7cbf3-122">Farið í Kerfisstjórnun > Notendur > Notendur.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-122">Go to System administration > Users > Users.</span></span>
    * <span data-ttu-id="7cbf3-123">Til að keyra samþykki á ósamkvæmi verður notandi sem samþykkir eða hafnar ósamkvæmi að hafa „Heiti“ úthlutað á síðunni Notendur.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-123">To process the approval of a nonconformance the user who  approves or rejects nonconformances must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="7cbf3-124">Til að nota athugasemdir skjals verður notandinn einnig að hafa skjalaafgreiðslu virkjaða í valkostum notanda.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-124">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
2. <span data-ttu-id="7cbf3-125">Nota flýtiafmörkun til að finna færslur</span><span class="sxs-lookup"><span data-stu-id="7cbf3-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="7cbf3-126">Til dæmis, sía svæðið Heiti með gildinu ‚Ricardo'.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-126">For example, filter on the Name field with a value of 'Ricardo'.</span></span>
    * <span data-ttu-id="7cbf3-127">Notið síuna til að finna notandinn sem verður að samþykkja eða hafna færslum ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-127">Use the filter to find the user who will be approving or rejecting the nonconformance records.</span></span>  
3. <span data-ttu-id="7cbf3-128">Í listanum skal smella á tengilinn í valinni línu.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7cbf3-129">Til að keyra samþykki á ósamkvæmi skal ganga úr skugga um að notandi sem samþykkir eða hafnar ósamkvæmi að hafi „Heiti“ úthlutað á síðunni Notendur.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-129">To process the approval of a nonconformance, make sure the user who approves or rejects nonconformances has a “Name” value assigned on the Users page.</span></span>  
4. <span data-ttu-id="7cbf3-130">Smelltu á Notandastillingar</span><span class="sxs-lookup"><span data-stu-id="7cbf3-130">Click User options.</span></span>
5. <span data-ttu-id="7cbf3-131">Smellið á flipann fríðindi.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-131">Click the Preferences tab.</span></span>
6. <span data-ttu-id="7cbf3-132">Velja skal Já í svæðinu virkja skjalastjórnun.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-132">Select Yes in the Enable document handling field.</span></span>
    * <span data-ttu-id="7cbf3-133">Til að nota athugasemdir skjals verður notandinn einnig að hafa skjalaafgreiðslu virkjaða í valkostum notanda.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-133">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
7. <span data-ttu-id="7cbf3-134">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-134">Close the page.</span></span>
8. <span data-ttu-id="7cbf3-135">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-135">Close the page.</span></span>
9. <span data-ttu-id="7cbf3-136">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-136">Close the page.</span></span>

## <a name="define-diagnostic-types-for-nonconformance-processing"></a><span data-ttu-id="7cbf3-137">Skilgreina gerðir greininga fyrir ósamkvæmnivinnslu.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-137">Define diagnostic types for nonconformance processing</span></span>
1. <span data-ttu-id="7cbf3-138">Fara í birgðastjórnun > Uppsetningu >gæðastjórnun > gerðir Greininga.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-138">Go to Inventory management > Setup > Quality management > Diagnostic types.</span></span>
    * <span data-ttu-id="7cbf3-139">Notaðu greiningargerðir  síðuna til að skilgreina flokkun greiningaraðgerða.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-139">Use the Diagnostic types page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="7cbf3-140">Leiðrétting auðkennir hvers konar greiningaraðgerð á að framkvæma á samþykktri ósamkvæmni, hver á að framkvæma hana og umbeðna eða áætlaða dagsetningu þegar henni á að vera lokið.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-140">A correction identifies what type of diagnostic action should be taken on an approved nonconformance, who should perform it, and the requested and planned completion date.</span></span>  
2. <span data-ttu-id="7cbf3-141">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-141">Click New.</span></span>
3. <span data-ttu-id="7cbf3-142">Í reitinn GREINING skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-142">In the Diagnostic field, type a value.</span></span>
4. <span data-ttu-id="7cbf3-143">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-143">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7cbf3-144">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-144">Close the page.</span></span>

## <a name="define-quality-charges-for-nonconformance-processing"></a><span data-ttu-id="7cbf3-145">Skilgreina gæðastjórnunargjöld fyrir ósamkvæmnivinnslu.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-145">Define quality charges for nonconformance processing</span></span>
1. <span data-ttu-id="7cbf3-146">Fara í birgðastjórnun > Uppsetning > Gæðaeftirlit > Gæðastjórnunargjöld.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-146">Go to Inventory management > Setup > Quality management > Quality charges.</span></span>
    * <span data-ttu-id="7cbf3-147">Nota síðu Gæðastjórnunargjöld til að skilgreina flokkun á gjöldum sem verður notuð í aðgerðir sem tengjast ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-147">Use the Quality charges page to define a classification of charges that will used in operations related to nonconformances.</span></span>  
2. <span data-ttu-id="7cbf3-148">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-148">Click New.</span></span>
3. <span data-ttu-id="7cbf3-149">Í reitnum Gjaldakóði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-149">In the Charges code field, type a value.</span></span>
4. <span data-ttu-id="7cbf3-150">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-150">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7cbf3-151">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-151">Close the page.</span></span>

## <a name="define-the-operations-for-nonconformance-processing"></a><span data-ttu-id="7cbf3-152">Skilgreinið starfsemi fyrir ósamkvæmivinnslu</span><span class="sxs-lookup"><span data-stu-id="7cbf3-152">Define the operations for nonconformance processing</span></span>
1. <span data-ttu-id="7cbf3-153">Fara í birgðastjórnun > Uppsetning > Gæðastjórnun > Aðgerðir.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-153">Go to Inventory management > Setup > Quality management > Operations.</span></span>
    * <span data-ttu-id="7cbf3-154">Notið síðuna aðgerðir til þess að skilgreina flokkun á vinnu sem gætu verið að framkvæmda fyrir samþykkta ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-154">Use the Operations page to define a classification of the work that may be performed for an approved nonconformance.</span></span> <span data-ttu-id="7cbf3-155">Þegar aðgerð er tengd við ósamkvæmni, er hægt að skilgreina upplýsingar um tengt efni, vinnustundir og ýmis gjöld sem eru nauðsynleg til þess að framkvæma aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-155">When you relate an operation to a nonconformance, you can define information about the associated material, labor hours, and miscellaneous charges that are required to perform the operation.</span></span> <span data-ttu-id="7cbf3-156">Þessar upplýsingar eru grunnurinn fyrir útreikninga á áætluðum kostnaði við að framkvæma aðgerðina.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-156">This information provides the basis for calculating an estimated cost for performing the operation.</span></span>  
2. <span data-ttu-id="7cbf3-157">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-157">Click New.</span></span>
3. <span data-ttu-id="7cbf3-158">Í reitinn Starfsemi skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-158">In the Operation field, type a value.</span></span>
4. <span data-ttu-id="7cbf3-159">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7cbf3-160">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-160">Close the page.</span></span>

## <a name="define-problem-types-for-nonconformance-processing"></a><span data-ttu-id="7cbf3-161">Skilgreina gerðir vandamála fyrir ósamkvæmnivinnslu.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-161">Define problem types for nonconformance processing</span></span>
1. <span data-ttu-id="7cbf3-162">Fara í birgðastjórnun > Uppsetningu > gæðastjórnun > gerðir vandamála.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-162">Go to Inventory management > Setup > Quality management > Problem types.</span></span>
    * <span data-ttu-id="7cbf3-163">Nota skal vandamálagerðir síðu til að skilgreina flokkun gæðavanda sem kemur fyrir í ýmsum ósamkvæmnigerðum.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-163">Use the Problem types page to define a classification of quality problems that are encountered in the various nonconformance types.</span></span> <span data-ttu-id="7cbf3-164">Gerðir ósamkvæmi innihalda: Viðskiptavinur, Innra, Framleiðsla, Þjónustubeiðni  eða Lánardrottinn og framleiðsla aukaafurða</span><span class="sxs-lookup"><span data-stu-id="7cbf3-164">The nonconformance types include Internal, Customer, Vendor, Service request, Production, and Co-product production.</span></span> <span data-ttu-id="7cbf3-165">Ein Gerð vandamáls eina hægt að tengja við margar gerðir ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-165">A single problem type can be associated with multiple nonconformance types.</span></span>  
2. <span data-ttu-id="7cbf3-166">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-166">Click New.</span></span>
3. <span data-ttu-id="7cbf3-167">Í reitinn gerð VANDAMÁLs skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-167">In the Problem type field, type a value.</span></span>
4. <span data-ttu-id="7cbf3-168">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-168">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7cbf3-169">Smelltu á Gerðir ósamkvæmnitilvika.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-169">Click Non conformance types.</span></span>
    * <span data-ttu-id="7cbf3-170">Notaðu síðuna gerðir ósamkvæmni til að heimila notkun á vandamálagerð í einni eða fleiri gerðum ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-170">Use the Non conformance types page to authorize the use of a problem type for one or more of the nonconformance types.</span></span> <span data-ttu-id="7cbf3-171">Til dæmis getur vandamálagerð sem tengist gallakóða átt við um allar gerðir ósamkvæmni, en aftur á móti getur vandamálagerð um kvartanir viðskiptamanna aðeins átt við um viðskiptavininn og gerðir ósamkvæmni í þjónustubeiðnum.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-171">For example, a problem type regarding a defect code could apply to all nonconformance types, whereas a problem type about customer complaints may only apply to the customer and service request nonconformance types.</span></span>  
6. <span data-ttu-id="7cbf3-172">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-172">Click New.</span></span>
7. <span data-ttu-id="7cbf3-173">Í listanum skal merkja valda línu.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-173">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="7cbf3-174">Veljið valkost í svæðinu tegund ósamkvæmni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-174">In the Non conformance type field, select an option.</span></span>
9. <span data-ttu-id="7cbf3-175">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-175">Close the page.</span></span>
10. <span data-ttu-id="7cbf3-176">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-176">Close the page.</span></span>

## <a name="define-quarantine-zones-for-nonconformance-processing"></a><span data-ttu-id="7cbf3-177">Virkja biðgeymslusæði fyrir ósamkvæmnivinnslu.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-177">Define quarantine zones for nonconformance processing</span></span>
1. <span data-ttu-id="7cbf3-178">Fara í birgðastjórnun > Uppsetning > Gæðastjórnun > Biðgeymslusvæði.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-178">Go to Inventory management > Setup > Quality management > Quarantine zones.</span></span>
2. <span data-ttu-id="7cbf3-179">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-179">Click New.</span></span>
3. <span data-ttu-id="7cbf3-180">Í reitinn biðgeymslusvæði skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-180">In the Quarantine zone field, type a value.</span></span>
4. <span data-ttu-id="7cbf3-181">Sláið inn gildi í reitnum „Lýsing“.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-181">In the Description field, type a value.</span></span>
5. <span data-ttu-id="7cbf3-182">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7cbf3-182">Close the page.</span></span>

