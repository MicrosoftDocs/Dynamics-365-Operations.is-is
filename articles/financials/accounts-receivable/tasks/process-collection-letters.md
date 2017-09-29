--- 
title: "Vinna úr innheimtubréfum"
description: "Þessi verklýsing sýnir hvernig á að stofna, prenta og bóka innheimtubréf."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
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
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---
# <a name="process-collection-letters"></a><span data-ttu-id="b7958-103">Vinna úr innheimtubréfum</span><span class="sxs-lookup"><span data-stu-id="b7958-103">Process collection letters</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b7958-104">Þessi verklýsing sýnir hvernig á að stofna, prenta og bóka innheimtubréf.</span><span class="sxs-lookup"><span data-stu-id="b7958-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="b7958-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="b7958-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="b7958-106">Setja upp röð innheimtubréfa á bókunarreglu</span><span class="sxs-lookup"><span data-stu-id="b7958-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="b7958-107">Farið í Skuldir og innheimta > Uppsetning > Bókunarreglur viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="b7958-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="b7958-108">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="b7958-108">Click Edit.</span></span>
    * <span data-ttu-id="b7958-109">Veljið innheimtubréfaröð úr í fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="b7958-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="b7958-110">Ef ekki á að mynda innheimtubréf fyrir færslur með þessari bókunarreglu, skilið eftir autt.</span><span class="sxs-lookup"><span data-stu-id="b7958-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="b7958-111">Flipanum takmarkanir fyrir Taflan gerir kleift að breyta hvernig innheimtubréf eru unnin.</span><span class="sxs-lookup"><span data-stu-id="b7958-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="b7958-112">Ef þetta svæði er stillt á Já, þá mun það verða að stofna innheimtubréf fyrir þessa bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="b7958-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="b7958-113">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="b7958-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="b7958-114">Búa til innheimtubréf</span><span class="sxs-lookup"><span data-stu-id="b7958-114">Create collection letters</span></span>
1. <span data-ttu-id="b7958-115">Fara í Skuldir og innheimta > Innheimtubréf > Stofna innheimtubréf.</span><span class="sxs-lookup"><span data-stu-id="b7958-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="b7958-116">Velja verður færslugerðir sem innheimta á bréf fyrir.</span><span class="sxs-lookup"><span data-stu-id="b7958-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="b7958-117">Allar opnar færslur fyrir þessar gerðir verða teknar með í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="b7958-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="b7958-118">Í reitnum innheimtubréf skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="b7958-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="b7958-119">Færðu inn dagsetningu innheimtubréfs.</span><span class="sxs-lookup"><span data-stu-id="b7958-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="b7958-120">Það eru tveir valkostir bókunarreglu: Reiknings – Notið bókunarreglu sem er úthlutað á reikning viðskiptavina fyrir hverja vaxtanótu.</span><span class="sxs-lookup"><span data-stu-id="b7958-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="b7958-121">Velja – Notið bókunarregluna sem valin var á svæðinu .</span><span class="sxs-lookup"><span data-stu-id="b7958-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="b7958-122">Veljið bókunarreglu hafi verið breytt "Nota bókunarreglu úr" á "Velja".</span><span class="sxs-lookup"><span data-stu-id="b7958-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="b7958-123">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="b7958-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="b7958-124">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="b7958-124">Click Filter.</span></span>
6. <span data-ttu-id="b7958-125">Í svæðið Skilyrði, í svæðið Skilyrði er fært inn kenni Viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="b7958-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="b7958-126">Til dæmis færið inn ‚US-001‘..</span><span class="sxs-lookup"><span data-stu-id="b7958-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="b7958-127">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b7958-127">Click OK.</span></span>
8. <span data-ttu-id="b7958-128">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b7958-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="b7958-129">Prenta innheimtubréf</span><span class="sxs-lookup"><span data-stu-id="b7958-129">Print collection letters</span></span>
1. <span data-ttu-id="b7958-130">Fara í Skuldir og innheimta > Innheimtubréf > Fara yfir og vinna innheimtubréf.</span><span class="sxs-lookup"><span data-stu-id="b7958-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="b7958-131">Í reitnum Staða er ‚Stofnað' valin.</span><span class="sxs-lookup"><span data-stu-id="b7958-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="b7958-132">Veljið í svæðinu Prentað 'Ekki prentað'.</span><span class="sxs-lookup"><span data-stu-id="b7958-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="b7958-133">Smelltu á Prenta.</span><span class="sxs-lookup"><span data-stu-id="b7958-133">Click Print.</span></span>
5. <span data-ttu-id="b7958-134">Smellt er á athugasemd innheimtubréfs</span><span class="sxs-lookup"><span data-stu-id="b7958-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="b7958-135">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="b7958-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="b7958-136">Færa inn lokadagsetningu fyrir bókanir</span><span class="sxs-lookup"><span data-stu-id="b7958-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="b7958-137">Smellt er á í lagi til að prenta innheimtubréfið.</span><span class="sxs-lookup"><span data-stu-id="b7958-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="b7958-138">Bóka innheimtubréf</span><span class="sxs-lookup"><span data-stu-id="b7958-138">Post the collection letter</span></span>
1. <span data-ttu-id="b7958-139">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="b7958-139">Click Post.</span></span>
2. <span data-ttu-id="b7958-140">Færð er inn bókunardagsetning fyrir innheimtubréf.</span><span class="sxs-lookup"><span data-stu-id="b7958-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="b7958-141">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="b7958-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="b7958-142">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="b7958-142">Click OK.</span></span>
5. <span data-ttu-id="b7958-143">Í reitnum Staða er ‚bókað' valin.</span><span class="sxs-lookup"><span data-stu-id="b7958-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="b7958-144">Prenta svæði, velja valkostur.</span><span class="sxs-lookup"><span data-stu-id="b7958-144">In the Printed field, select an option.</span></span>


