---
title: Vinna úr innheimtubréfum
description: Þetta efni sýnir hvernig á að stofna, prenta og bóka innheimtubréf.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: 326d9375670cb4f4990a4f7070bf923a28b2c025
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178323"
---
# <a name="process-collection-letters"></a><span data-ttu-id="f8fb3-103">Vinna úr innheimtubréfum</span><span class="sxs-lookup"><span data-stu-id="f8fb3-103">Process collection letters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f8fb3-104">Þetta efni sýnir hvernig á að stofna, prenta og bóka innheimtubréf.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-104">This topic shows how to create, print, and post collection letters.</span></span> <span data-ttu-id="f8fb3-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-105">This task uses the USMF demo company.</span></span>

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a><span data-ttu-id="f8fb3-106">Setja upp röð innheimtubréfa á bókunarreglu</span><span class="sxs-lookup"><span data-stu-id="f8fb3-106">Set up a collection letter sequence on the posting profile</span></span>
1. <span data-ttu-id="f8fb3-107">Farðu í **Skoðunarrúðu > Kerfiseiningar > Skuldir og innheimta > Uppsetning > Bókunarreglur viðskiptavina**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="f8fb3-108">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-108">Click **Edit**.</span></span>
3. <span data-ttu-id="f8fb3-109">Veljið innheimtubréfaröð úr í fellilistanum.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-109">Select a collection letter sequence from the drop-down list.</span></span> <span data-ttu-id="f8fb3-110">Ef ekki á að mynda innheimtubréf fyrir færslur með þessari bókunarreglu skal skilja svæðið eftir autt.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-110">If you do not want to generate collection letters for transactions using this posting profile, leave the field blank.</span></span>  
4. <span data-ttu-id="f8fb3-111">Víkkaðu út flipann **Töflutakmarkanir** til að breyta því hvernig innheimtubréf eru unnin.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-111">Expand the **Table restrictions** tab to change the way that collection letters are processed.</span></span> <span data-ttu-id="f8fb3-112">Ef þetta svæði er stillt á **Já**, þá verða stofnuð innheimtubréf fyrir þessa bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-112">If this field is set to **Yes**, then collection letters will be created for this posting profile.</span></span>  

## <a name="create-collection-letters"></a><span data-ttu-id="f8fb3-113">Búa til innheimtubréf</span><span class="sxs-lookup"><span data-stu-id="f8fb3-113">Create collection letters</span></span>
1. <span data-ttu-id="f8fb3-114">Farðu í **Skoðunarrúða > Kerfiseiningar > Skuldir og innheimta > Innheimtubréf > Stofna innheimtubréf**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-114">Go to **Navigation pane > Modules > Credit and collections > Collection letter > Create collection letters**.</span></span>
2. <span data-ttu-id="f8fb3-115">Velja færslugerðir sem innheimta á bréf fyrir.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-115">Select the transaction types for which you will collect letters.</span></span> <span data-ttu-id="f8fb3-116">Allar opnar færslur fyrir þessar gerðir verða teknar með í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="f8fb3-117">Í reitnum **Innheimtubréf** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-117">In the **Collection letter** field, select an option.</span></span>
4. <span data-ttu-id="f8fb3-118">Í reitinn **Dagsetning innheimtubréfs** skaltu slá inn dagsetningu innheimtubréfsins.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-118">In the **Collection letter date** field, enter the date of the collection letter.</span></span>
5. <span data-ttu-id="f8fb3-119">Veljið bókunarreglu ef þú breyttir **Nota bókunarreglu úr** í **Velja**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-119">Select a posting profile if you changed **Use posting profile from** to **Select**.</span></span> <span data-ttu-id="f8fb3-120">Í boði eru tveir valmöguleikar fyrir bókunarreglu:</span><span class="sxs-lookup"><span data-stu-id="f8fb3-120">There are two posting profile options:</span></span>   

   - <span data-ttu-id="f8fb3-121">**Reikningur** – Nota bókunarreglu sem er úthlutað til reikning viðskiptavinar fyrir hverja vaxtanótu.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-121">**Account** – Use the posting profile that is assigned to the customer account for each interest note.</span></span>   
   - <span data-ttu-id="f8fb3-122">**Velja** – Notið bókunarregluna sem valin var á svæðinu **Bókunarregla**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-122">**Select** – Use the posting profile that you select in the **Posting profile** field.</span></span>  

6. <span data-ttu-id="f8fb3-123">Útvíkka **Færslur til að taka með** hlutann.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-123">Expand the **Records to include** section.</span></span>
7. <span data-ttu-id="f8fb3-124">Velja **Síu**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-124">Select **Filter**.</span></span>
8. <span data-ttu-id="f8fb3-125">Í svæðinu **Skilyrði** skal færa inn auðkenni viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-125">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="f8fb3-126">Til dæmis, færið inn ‚US-001'.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-126">For example, enter 'US-001'.</span></span>
9. <span data-ttu-id="f8fb3-127">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-127">Select **OK**.</span></span>
10. <span data-ttu-id="f8fb3-128">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-128">Select **OK**.</span></span>

## <a name="print-collection-letters"></a><span data-ttu-id="f8fb3-129">Prenta innheimtubréf</span><span class="sxs-lookup"><span data-stu-id="f8fb3-129">Print collection letters</span></span>
1. <span data-ttu-id="f8fb3-130">Farðu í **Skoðunarrúða > Kerfiseiningar > Skuldir og innheimta > Innheimtubréf > Endurskoða og vinna innheimtubréf**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-130">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span>
2. <span data-ttu-id="f8fb3-131">Í reitnum **Staða** skal velja **Stofnað**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-131">In the **Status** field, select **Created**.</span></span>
3. <span data-ttu-id="f8fb3-132">Í reitnum **Prentað** skal velja **Ekki prentað**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-132">In the **Printed** field, select **Not printed**.</span></span>
4. <span data-ttu-id="f8fb3-133">Velsu **Prenta**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-133">Select **Print**.</span></span>
5. <span data-ttu-id="f8fb3-134">Veldu **Innheimtubréfsnóta**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-134">Select **Collection letter note**.</span></span>
6. <span data-ttu-id="f8fb3-135">Í kaflanum **Færibreytur** skaltu slá inn lokadagsetningu fyrir bréf.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-135">In the **Parameters** section, enter the cutoff date for postings.</span></span>
7. <span data-ttu-id="f8fb3-136">Stækkaðu kaflann **Færslur til að hafa með** og sláðu inn upplýsingar um innheimtubréfsnótuna.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-136">Expand the **Records to include** section and enter the details of the Collection letter note.</span></span>
8. <span data-ttu-id="f8fb3-137">Veldu **Í lagi** til að prenta innheimtubréfið.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-137">Select **OK** to print the collection letter.</span></span>
9. <span data-ttu-id="f8fb3-138">Bóka innheimtubréfið.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-138">Post the collection letter.</span></span>

    1. <span data-ttu-id="f8fb3-139">Veldu **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-139">Select **Post**.</span></span>
    1. <span data-ttu-id="f8fb3-140">Færð er inn bókunardagsetning fyrir innheimtubréf.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-140">Enter the posting date for the collection letter.</span></span>
    1. <span data-ttu-id="f8fb3-141">Útvíkka **Færslur til að taka með** hlutann.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-141">Expand the **Records to include** section.</span></span>
    1. <span data-ttu-id="f8fb3-142">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-142">Select **OK**.</span></span>
    1. <span data-ttu-id="f8fb3-143">Í reitnum **Staða** skal velja **Bókað**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-143">In the **Status** field, select **Posted**.</span></span>
    1. <span data-ttu-id="f8fb3-144">Í reitnum **Prentað** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-144">In the **Printed** field, select an option.</span></span>

## <a name="control-collection-letters-at-the-customer-level"></a><span data-ttu-id="f8fb3-145">Stjórna innheimtubréfum á stigi viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="f8fb3-145">Control collection letters at the customer level</span></span>
<span data-ttu-id="f8fb3-146">Einnig er hægt að að setja upp innheimtubréf á stigi viðskiptavinar þannig að kóði innheimtubréfs fyrir hverja færslu sé rakinn, en úrvinnsla innheimtubréfs mun byggjast á einu stigi innheimtubréfs sem er geymt fyrir viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-146">You can also set up collection letters at the customer level so that the collection letter code for each transaction is tracked, but the collection letter processing will be based on a single collection letter level that is stored for the customer.</span></span> <span data-ttu-id="f8fb3-147">Eitt stakt innheimtubréf mun innihalda allar færslur sem eru gjaldfallnar fyrir viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-147">The single collection letter will contain all transactions that are overdue for the customer.</span></span> <span data-ttu-id="f8fb3-148">Vegna þess að biðdagar eru nú raktir á stigi viðskiptavinar verður næsta innheimtubréf ekki sent fyrr en fjöldi biðdaga er liðinn fyrir næsta innheimtubréf í röðinni, jafnvel þótt færslur falla á gjalddaga eftir að síðasta innheimtubréf var sent.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-148">Because the grace days are now tracked on the customer level, the next collection letter will not be sent until the number of grace days has passed for the next collection letter in the sequence, even though transactions become overdue after the last collection letter was sent.</span></span> <span data-ttu-id="f8fb3-149">Þessi valkostur dregur úr fjölda innheimtubréfa sem þú sendir á hvern viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-149">This option reduces the number of collection letters you will send per customer.</span></span> 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a><span data-ttu-id="f8fb3-150">Setja upp viðskiptavininn til að stjórna innheimtubréfum á stigi viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="f8fb3-150">Set up the customer to control collection letters at the customer level</span></span>
1.  <span data-ttu-id="f8fb3-151">Farðu í **Skoðunarrúða > Kerfiseiningar > Skuldir og innheimta > Uppsetning > Færibreytur viðskiptakrafna** og veldu flipann **Innheimtur**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-151">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and select the **Collections** tab.</span></span> 
2.  <span data-ttu-id="f8fb3-152">Breyta gildinu á **Stofna innheimtubréf eftir** í **Viðskiptavinur**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-152">Change the value of **Create collection letter per** to **Customer**.</span></span> 
3.  <span data-ttu-id="f8fb3-153">Farðu í **Skoðunarrúða > Kerfiseiningar > Skuldir og innheimta > Innheimtubréf > Endurskoða og vinna innheimtubréf**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-153">Go to **navigation pane > Modules > Credit and collections > Collection letter > Review and process collection letters**.</span></span> <span data-ttu-id="f8fb3-154">Aðeins eitt innheimtubréf verður búið til fyrir viðskiptavin með öllum gjaldföllnum færslum.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-154">Only one collection letter will be generated for a customer with all the overdue transactions.</span></span>

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a><span data-ttu-id="f8fb3-155">Hunsa greiðslur og kreditreikninga við útreikning á innheimtubréfskóða</span><span class="sxs-lookup"><span data-stu-id="f8fb3-155">Ignore payments and credit memos when calculating the collection letter code</span></span>
<span data-ttu-id="f8fb3-156">Ef þú hefur með greiðslur og kreditreikninga í færslunum sem verða hafðar með í innheimtubréfum, kann að vera að greiðslur eða kreditreikningar setji innheimtubréf af stað.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-156">If you include payments and credit memos in the transactions that will be included in the collection letters, you may have payments or credit memos that will trigger a collection letter.</span></span> <span data-ttu-id="f8fb3-157">Hægt er að stjórna því hvernig greiðslur og kreditreikningar stýra innheimtubréfakóðanum með því að breyta gildinu á færibreytunni **Hunsa greiðslur og kreditreikninga við útreikning á innheimtubréfskóða**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-157">You can control how payments and credit memos control the collection letter code by changing the value of the **Ignore payments and credit memos when calculating the collection letter code** parameter.</span></span> 

<span data-ttu-id="f8fb3-158">Til að hunsa greiðslur og kreditreikninga við útreikning á innheimtubréfakóðanum skal gera eftirfarandi.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-158">To ignore payments and credit memos when calculating the collection letter code, do the following.</span></span>

1. <span data-ttu-id="f8fb3-159">Farðu í **Skoðunarrúða > Kerfiseiningar > Skuldir og innheimta > Uppsetning > Færibreytur viðskiptakrafna** og smelltu á flipann **Innheimtur**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-159">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters** and click the **Collections** tab.</span></span> 
2. <span data-ttu-id="f8fb3-160">Breyta gildinu á **Hunsa greiðslur og kreditreikninga við útreikning á innheimtubréfskóða** í **Já**.</span><span class="sxs-lookup"><span data-stu-id="f8fb3-160">Change the value of **Ignore payments and credit memos when calculating the collection letter code** to **Yes**.</span></span>