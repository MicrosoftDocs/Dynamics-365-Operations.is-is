--- 
title: "Vinna úr innheimtubréfum"
description: "Þessi verklýsing sýnir hvernig á að stofna, prenta og bóka innheimtubréf."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, SysQueryForm, CustCollectionLetterNote
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: fe76f2934360580c4015ea13225b9228cc2780b9
ms.contentlocale: is-is
ms.lasthandoff: 09/11/2018

---
# <a name="process-collection-letters"></a><span data-ttu-id="c6e28-103">Vinna úr innheimtubréfum</span><span class="sxs-lookup"><span data-stu-id="c6e28-103">Process collection letters</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c6e28-104">Þessi verklýsing sýnir hvernig á að stofna, prenta og bóka innheimtubréf.</span><span class="sxs-lookup"><span data-stu-id="c6e28-104">This procedure shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="c6e28-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="c6e28-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="c6e28-106">Setja upp röð innheimtubréfa á bókunarreglu</span><span class="sxs-lookup"><span data-stu-id="c6e28-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="c6e28-107">Farið í Skuldir og innheimta > Uppsetning > Bókunarreglur viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="c6e28-107">Go to Credit and collections > Setup > Customer posting profiles.</span></span>
2. <span data-ttu-id="c6e28-108">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="c6e28-108">Click Edit.</span></span>
    * <span data-ttu-id="c6e28-109">Veljið innheimtubréfaröð úr í fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="c6e28-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="c6e28-110">Ef ekki á að mynda innheimtubréf fyrir færslur með þessari bókunarreglu, skilið eftir autt.</span><span class="sxs-lookup"><span data-stu-id="c6e28-110">If you do not want generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
    * <span data-ttu-id="c6e28-111">Flipanum takmarkanir fyrir Taflan gerir kleift að breyta hvernig innheimtubréf eru unnin.</span><span class="sxs-lookup"><span data-stu-id="c6e28-111">The table restriction tab allows you to change the way that collection letters are processed.</span></span> <span data-ttu-id="c6e28-112">Ef þetta svæði er stillt á Já, þá mun það verða að stofna innheimtubréf fyrir þessa bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="c6e28-112">If this field is set to Yes, then collection letters will be created for this posting profile.</span></span>  
3. <span data-ttu-id="c6e28-113">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c6e28-113">Close the page.</span></span>

## <a name="create-collection-letters"></a><span data-ttu-id="c6e28-114">Búa til innheimtubréf</span><span class="sxs-lookup"><span data-stu-id="c6e28-114">Create collection letters</span></span>
1. <span data-ttu-id="c6e28-115">Fara í Skuldir og innheimta > Innheimtubréf > Stofna innheimtubréf.</span><span class="sxs-lookup"><span data-stu-id="c6e28-115">Go to Credit and collections > Collection letter > Create collection letters.</span></span>
    * <span data-ttu-id="c6e28-116">Velja verður færslugerðir sem innheimta á bréf fyrir.</span><span class="sxs-lookup"><span data-stu-id="c6e28-116">You must select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="c6e28-117">Allar opnar færslur fyrir þessar gerðir verða teknar með í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="c6e28-117">All of the open transactions for these types will be included in the calculation.</span></span>  
2. <span data-ttu-id="c6e28-118">Í reitnum innheimtubréf skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="c6e28-118">In the Collection letter field, select an option.</span></span>
3. <span data-ttu-id="c6e28-119">Færðu inn dagsetningu innheimtubréfs.</span><span class="sxs-lookup"><span data-stu-id="c6e28-119">Enter the date of the collection letter.</span></span>
    * <span data-ttu-id="c6e28-120">Það eru tveir valkostir bókunarreglu: Reiknings – Notið bókunarreglu sem er úthlutað á reikning viðskiptavina fyrir hverja vaxtanótu.</span><span class="sxs-lookup"><span data-stu-id="c6e28-120">There are two posting profile options:   Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   <span data-ttu-id="c6e28-121">Velja – Notið bókunarregluna sem valin var á svæðinu .</span><span class="sxs-lookup"><span data-stu-id="c6e28-121">Select – Use the posting profile that you select in the Posting profile field.</span></span>  
    * <span data-ttu-id="c6e28-122">Veljið bókunarreglu hafi verið breytt "Nota bókunarreglu úr" á "Velja".</span><span class="sxs-lookup"><span data-stu-id="c6e28-122">Select a posting profile if you changed "Use posting profile from" to "Select".</span></span>  
4. <span data-ttu-id="c6e28-123">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="c6e28-123">Expand the Records to include section.</span></span>
5. <span data-ttu-id="c6e28-124">Smellt er á Síu.</span><span class="sxs-lookup"><span data-stu-id="c6e28-124">Click Filter.</span></span>
6. <span data-ttu-id="c6e28-125">Í svæðið Skilyrði, í svæðið Skilyrði er fært inn kenni Viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="c6e28-125">In the Criteria field, In the Criteria field, enter a Customer ID.</span></span> <span data-ttu-id="c6e28-126">Til dæmis færið inn ‚US-001‘..</span><span class="sxs-lookup"><span data-stu-id="c6e28-126">For example, enter 'US-001'..</span></span>
7. <span data-ttu-id="c6e28-127">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c6e28-127">Click OK.</span></span>
8. <span data-ttu-id="c6e28-128">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c6e28-128">Click OK.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="c6e28-129">Prenta innheimtubréf</span><span class="sxs-lookup"><span data-stu-id="c6e28-129">Print collection letters</span></span>
1. <span data-ttu-id="c6e28-130">Fara í Skuldir og innheimta > Innheimtubréf > Fara yfir og vinna innheimtubréf.</span><span class="sxs-lookup"><span data-stu-id="c6e28-130">Go to Credit and collections > Collection letter > Review and process collection letters.</span></span>
2. <span data-ttu-id="c6e28-131">Í reitnum Staða er ‚Stofnað' valin.</span><span class="sxs-lookup"><span data-stu-id="c6e28-131">In the Status field, select 'Created'.</span></span>
3. <span data-ttu-id="c6e28-132">Veljið í svæðinu Prentað 'Ekki prentað'.</span><span class="sxs-lookup"><span data-stu-id="c6e28-132">In the Printed field, select 'Not printed'.</span></span>
4. <span data-ttu-id="c6e28-133">Smelltu á Prenta.</span><span class="sxs-lookup"><span data-stu-id="c6e28-133">Click Print.</span></span>
5. <span data-ttu-id="c6e28-134">Smellt er á athugasemd innheimtubréfs</span><span class="sxs-lookup"><span data-stu-id="c6e28-134">Click Collection letter note.</span></span>
6. <span data-ttu-id="c6e28-135">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="c6e28-135">Expand the Records to include section.</span></span>
7. <span data-ttu-id="c6e28-136">Færa inn lokadagsetningu fyrir bókanir</span><span class="sxs-lookup"><span data-stu-id="c6e28-136">Enter the cutoff date for postings</span></span>
8. <span data-ttu-id="c6e28-137">Smellt er á í lagi til að prenta innheimtubréfið.</span><span class="sxs-lookup"><span data-stu-id="c6e28-137">Click OK to print the collection letter.</span></span>

## <a name="post-the-collection-letter"></a><span data-ttu-id="c6e28-138">Bóka innheimtubréf</span><span class="sxs-lookup"><span data-stu-id="c6e28-138">Post the collection letter</span></span>
1. <span data-ttu-id="c6e28-139">Smellið á „Bóka“.</span><span class="sxs-lookup"><span data-stu-id="c6e28-139">Click Post.</span></span>
2. <span data-ttu-id="c6e28-140">Færð er inn bókunardagsetning fyrir innheimtubréf.</span><span class="sxs-lookup"><span data-stu-id="c6e28-140">Enter the posting date for the collection letter.</span></span>
3. <span data-ttu-id="c6e28-141">Útvíkka Færslur til að taka hluta.</span><span class="sxs-lookup"><span data-stu-id="c6e28-141">Expand the Records to include section.</span></span>
4. <span data-ttu-id="c6e28-142">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="c6e28-142">Click OK.</span></span>
5. <span data-ttu-id="c6e28-143">Í reitnum Staða er ‚bókað' valin.</span><span class="sxs-lookup"><span data-stu-id="c6e28-143">In the Status field, select 'Posted'.</span></span>
6. <span data-ttu-id="c6e28-144">Prenta svæði, velja valkostur.</span><span class="sxs-lookup"><span data-stu-id="c6e28-144">In the Printed field, select an option.</span></span>


