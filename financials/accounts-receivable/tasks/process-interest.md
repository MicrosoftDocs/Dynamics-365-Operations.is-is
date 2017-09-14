--- 
title: Reikna vexti
description: "Þessi verklýsing sýnir hvernig á að stofna, prenta og bóka vaxtanótur."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 543ac29ac1b1cbad52f1c155ac90b04d0c122a1f
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="process-interest"></a><span data-ttu-id="93490-103">Reikna vexti</span><span class="sxs-lookup"><span data-stu-id="93490-103">Process interest</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="93490-104">Þessi verklýsing sýnir hvernig á að stofna, prenta og bóka vaxtanótur.</span><span class="sxs-lookup"><span data-stu-id="93490-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="93490-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="93490-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="93490-106">Setja upp vexti fyrir bókunarregluna</span><span class="sxs-lookup"><span data-stu-id="93490-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="93490-107">Farið í Skuldir og innheimta > Uppsetning > Bókunarreglur viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="93490-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="93490-108">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="93490-108">Click Edit.</span></span>
    * <span data-ttu-id="93490-109">Veldu vaxtakóða úr fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="93490-109">Select an interest code from the drop-down list.</span></span> <span data-ttu-id="93490-110">Ef ekki á að reikna vexti fyrir færslur með þessari bókunarreglu, skilið eftir autt.</span><span class="sxs-lookup"><span data-stu-id="93490-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="93490-111">Takmarkanaflipi fyrir Taflan leyfir þér að breyta hvernig vextir eru unnir.</span><span class="sxs-lookup"><span data-stu-id="93490-111">The Table restriction tab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="93490-112">Ef þetta svæði er stillt á Já eru vextir reiknast fyrir þessa bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="93490-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="93490-113">Reikna út vexti</span><span class="sxs-lookup"><span data-stu-id="93490-113">Calculate interest</span></span>
1. <span data-ttu-id="93490-114">Fara í Skuldir og innheimta > Vextir > Stofna vaxtanótur.</span><span class="sxs-lookup"><span data-stu-id="93490-114">Go to Credit and collections > Interest > Create interest notes.</span></span>
    * <span data-ttu-id="93490-115">Velja færslugerðir sem verður að reikna út vexti fyrir.</span><span class="sxs-lookup"><span data-stu-id="93490-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="93490-116">Allar opnar færslur fyrir þessar gerðir verða teknar með í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="93490-116">All of the open transactions for these types will be included in the calculation.</span></span>  
    * <span data-ttu-id="93490-117">Ef Vaxta er valið, muntu reikna vaxtavexti.</span><span class="sxs-lookup"><span data-stu-id="93490-117">If you select Interest, you will calculate interest on interest.</span></span> <span data-ttu-id="93490-118">Hægt er að athuga lög um útreikningi á vaxtavöxtum áður en þessar færslur eru hafðar með.</span><span class="sxs-lookup"><span data-stu-id="93490-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
    * <span data-ttu-id="93490-119">Vextir reiknast úr þessari dagsetning sem „Til dagsetningar".</span><span class="sxs-lookup"><span data-stu-id="93490-119">Interest will be calculated from this date to the "To date".</span></span> <span data-ttu-id="93490-120">Ef ekki er tiltekin á "Frá dagsetningu', þá allir óbókaðir vaxtanóta verður hætt við og vextir verða endurreiknuð frá færsludagsetning.</span><span class="sxs-lookup"><span data-stu-id="93490-120">If you do not specific a "From date", then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>  
2. <span data-ttu-id="93490-121">Færið inn dagsetningu vaxtanótunnar.</span><span class="sxs-lookup"><span data-stu-id="93490-121">Enter the date of the interest note.</span></span>
    * <span data-ttu-id="93490-122">Það eru þrír möguleikar fyrir bókunarreglu: Reikningur - Nota bókunareglu sem er úthlutað til reikning viðskiptavinar fyrir hverja vaxtanótu.</span><span class="sxs-lookup"><span data-stu-id="93490-122">There are three posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="93490-123">Velja – Notið bókunarregluna sem valin var á svæðinu .</span><span class="sxs-lookup"><span data-stu-id="93490-123">Select – Use the posting profile that you select in the Posting profile field.</span></span>   <span data-ttu-id="93490-124">Færsla – Notið einstaka bókunarreglu úr færslum þar sem vextir eru reiknaðir fyrir hverja vaxtanótu.</span><span class="sxs-lookup"><span data-stu-id="93490-124">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="93490-125">Færslur sem hafa ekki úthlutaða bókunarreglu nota bókunarreglu sem er tilgreind á svæðinu Fjárhagur og virðisaukaskattur í skjámyndinni Færibreytur viðskiptakrafna.</span><span class="sxs-lookup"><span data-stu-id="93490-125">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
    * <span data-ttu-id="93490-126">Veljið bókunarreglu hér ef "Nota bókunarreglu úr" er breytt í "Velja".</span><span class="sxs-lookup"><span data-stu-id="93490-126">Select a posting profile here if you changed "Use posting profile from" to "Select".</span></span>  
3. <span data-ttu-id="93490-127">Útvíkka eða draga saman Færslur sem á að taka með hluta.</span><span class="sxs-lookup"><span data-stu-id="93490-127">Expand or collapse the Records to include section.</span></span>
4. <span data-ttu-id="93490-128">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="93490-128">Click Filter.</span></span>
5. <span data-ttu-id="93490-129">Í forsendusvæðinu, færið inn kenni viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="93490-129">In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="93490-130">Til dæmis færið inn ‚US-001‘..</span><span class="sxs-lookup"><span data-stu-id="93490-130">For example, enter 'US-001'..</span></span>
6. <span data-ttu-id="93490-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="93490-131">Click OK.</span></span>
7. <span data-ttu-id="93490-132">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="93490-132">Click OK.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="93490-133">Prenta vaxtanótur</span><span class="sxs-lookup"><span data-stu-id="93490-133">Print interest notes</span></span>
1. <span data-ttu-id="93490-134">Fara í Skuldir og innheimta > Vextir > Endurskoða og vinna vaxtanótur.</span><span class="sxs-lookup"><span data-stu-id="93490-134">Go to Credit and collections > Interest > Review and process interest notes.</span></span>
2. <span data-ttu-id="93490-135">Í reitnum Staða er ‚Stofnað' valin.</span><span class="sxs-lookup"><span data-stu-id="93490-135">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="93490-136">Veljið í svæðinu Prentað 'Ekki prentað'.</span><span class="sxs-lookup"><span data-stu-id="93490-136">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="93490-137">Smelltu á Prenta.</span><span class="sxs-lookup"><span data-stu-id="93490-137">Click Print.</span></span>
5. <span data-ttu-id="93490-138">Útvíkka eða draga saman Færslur sem á að taka með hluta.</span><span class="sxs-lookup"><span data-stu-id="93490-138">Expand or collapse the Records to include section.</span></span>
6. <span data-ttu-id="93490-139">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="93490-139">Click OK.</span></span>
7. <span data-ttu-id="93490-140">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="93490-140">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="93490-141">Bóka vaxtanótu</span><span class="sxs-lookup"><span data-stu-id="93490-141">Post the interest note</span></span>
1. <span data-ttu-id="93490-142">Velja vaxtanótu sem er að tilbúin til bókunar (staða er stofnuð).</span><span class="sxs-lookup"><span data-stu-id="93490-142">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="93490-143">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="93490-143">Click Post.</span></span>
3. <span data-ttu-id="93490-144">Færð er inn bókunardagsetning fyrir vaxtanóta.</span><span class="sxs-lookup"><span data-stu-id="93490-144">Enter the posting date for the interest note.</span></span>
    * <span data-ttu-id="93490-145">Skal velja Já í stofna fjárhagsfærsla fyrir hverja vaxtanóta.</span><span class="sxs-lookup"><span data-stu-id="93490-145">Select Yes to create a general ledger transaction for each interest note.</span></span>     <span data-ttu-id="93490-146">Ef þú velur ekki já, safnast upp allir vextir á vaxtanóta til viðskiptavinarins og eru bókaðar á fjárhag í einni færslu.</span><span class="sxs-lookup"><span data-stu-id="93490-146">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="93490-147">Útvíkka eða draga saman Færslur sem á að taka með hluta.</span><span class="sxs-lookup"><span data-stu-id="93490-147">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="93490-148">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="93490-148">Click OK.</span></span>
6. <span data-ttu-id="93490-149">Í reitnum Staða er ‚bókað' valin.</span><span class="sxs-lookup"><span data-stu-id="93490-149">In the Status field, select 'Posted'.</span></span>


