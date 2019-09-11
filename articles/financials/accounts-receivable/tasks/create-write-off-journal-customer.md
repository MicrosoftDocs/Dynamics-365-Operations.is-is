---
title: Stofna afskriftabók fyrir viðskiptavin
description: Þessi leiðarvísi fyrir verk sýnir hvernig á að setja upp færibreytur fyrir afskriftir og síðan að afskrifa færslur frá síðu Innheimtu, á listasíðu Opna reikninga viðskiptavina og síðu Viðskiptavinar.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, CustPosting, DefaultDashboard, CustCollectionsPoolsListPage, CustWriteOff, LedgerJournalTable, LedgerJournalTransDaily, CustCollections, CustOpenInvoicesListPage, CustTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2422f0a9d168daa76d105099c8b7455c97f92125
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916324"
---
# <a name="create-a-write-off-journal-for-a-customer"></a><span data-ttu-id="09f2c-103">Stofna afskriftabók fyrir viðskiptavin</span><span class="sxs-lookup"><span data-stu-id="09f2c-103">Create a write-off journal for a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="09f2c-104">Þessi leiðarvísi fyrir verk sýnir hvernig á að setja upp færibreytur fyrir afskriftir og síðan að afskrifa færslur frá síðu Innheimtu, á listasíðu Opna reikninga viðskiptavina og síðu Viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="09f2c-104">This task guide will show you how to set up the parameters for write-offs and then write off transactions from the Collections page, the Open customer invoices page, and the Customer page.</span></span> <span data-ttu-id="09f2c-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="09f2c-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-the-write-off-parameters"></a><span data-ttu-id="09f2c-106">Setja upp færibreytur afskriftar</span><span class="sxs-lookup"><span data-stu-id="09f2c-106">Set up the write off parameters</span></span>
1. <span data-ttu-id="09f2c-107">Farðu í **Skoðunarrúða > Kerfi > Skuldir og innheimta > Uppsetning > Færibreytur viðskiptakrafna**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-107">Go to **Navigation pane > Modules > Credit and collections > Setup > Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="09f2c-108">Smelltu á flipann **Innheimta**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-108">Click the **Collections** tab.</span></span>
3. <span data-ttu-id="09f2c-109">Stækka eða fella saman hlutann **afskriftir**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-109">Expand or collapse the **Write-off** section.</span></span>
    - <span data-ttu-id="09f2c-110">**Afskriftabók** er almenn færslubók sem mun innihalda afskriftafærslur sem eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="09f2c-110">The **Write-off journal** is the general journal that will hold the write-off transactions that you create.</span></span>  
    - <span data-ttu-id="09f2c-111">Hægt er að tengja ástæðukóða við hvert afskrift.</span><span class="sxs-lookup"><span data-stu-id="09f2c-111">You can attach a reason code to every write-off.</span></span> <span data-ttu-id="09f2c-112">Hægt er að hnekkja þessari sjálfgefnu gildi við sjálfa afskriftina.</span><span class="sxs-lookup"><span data-stu-id="09f2c-112">You can override this default at the time of the write-off.</span></span>  
    - <span data-ttu-id="09f2c-113">Stilltu **Virðisaukaskattur aðskilinn** á Já ef óskað er að aðskilja virðisaukaskatt úr upphaflegri færslu í afskriftum.</span><span class="sxs-lookup"><span data-stu-id="09f2c-113">Set the **Separate sales tax** to Yes if you want to separate the sales tax from the original transaction in the write-off.</span></span>  
4. <span data-ttu-id="09f2c-114">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09f2c-114">Close the page.</span></span>
5. <span data-ttu-id="09f2c-115">Farið í **Skuldir og innheimta > Uppsetning > Bókunarreglur viðskiptavina**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-115">Go to **Credit and collections > Setup > Customer posting profiles**.</span></span> <span data-ttu-id="09f2c-116">Afskriftalykill verður notað sem kostnaðarlykill eða öfug leiðrétting í almennu færslubókinni.</span><span class="sxs-lookup"><span data-stu-id="09f2c-116">The write-off account will be used as the expense account or reserve adjustment in the general journal.</span></span>
6. <span data-ttu-id="09f2c-117">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09f2c-117">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-aged-balances-page"></a><span data-ttu-id="09f2c-118">Afskrifa stöðu viðskiptavina af síðunni aldursgreindar stöður</span><span class="sxs-lookup"><span data-stu-id="09f2c-118">Write off a customer balance from the aged balances page</span></span>
1. <span data-ttu-id="09f2c-119">Fara í **skuldir og innheimta > Innheimta > Aldursgreindar stöður**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-119">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="09f2c-120">Merkja línuna fyrir viðskiptavin sem á að afskrifa.</span><span class="sxs-lookup"><span data-stu-id="09f2c-120">Mark the row for the customer that you want to write off.</span></span> <span data-ttu-id="09f2c-121">Til dæmis að merkja línuna með Birch Fyrirtækisins á því.</span><span class="sxs-lookup"><span data-stu-id="09f2c-121">For example, mark the line with Birch Company on it.</span></span>
3. <span data-ttu-id="09f2c-122">Í **aðgerðasvæðinu** er smellt á **Innheimta**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-122">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="09f2c-123">Smellt er á **Afskrifa**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-123">Click **Write off**.</span></span>
5. <span data-ttu-id="09f2c-124">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-124">Click **OK**.</span></span>
6. <span data-ttu-id="09f2c-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09f2c-125">Close the page.</span></span>
7. <span data-ttu-id="09f2c-126">Farðu í **skoðunarrúðuna > Kerfiseiningar > Fjárhagur > Bókarfærslur > Almennar færslubækur**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-126">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
8. <span data-ttu-id="09f2c-127">Veljið rununúmer færslubókar fyrir færslubók sem inniheldur afskrift.</span><span class="sxs-lookup"><span data-stu-id="09f2c-127">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="09f2c-128">Ein lína er stofnuð til að snúa við stöðu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="09f2c-128">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="09f2c-129">Ein eða fleiri línur eru stofnaðar til að bóka afskriftir í afskriftarlykil.</span><span class="sxs-lookup"><span data-stu-id="09f2c-129">One or more lines are created to post the write-off to the write-off account.</span></span>  
9. <span data-ttu-id="09f2c-130">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09f2c-130">Close the page.</span></span>
10. <span data-ttu-id="09f2c-131">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09f2c-131">Close the page.</span></span>

## <a name="write-off-transactions-from-the-collections-form"></a><span data-ttu-id="09f2c-132">Afskrifa færslur úr skjámyndinni innheimta.</span><span class="sxs-lookup"><span data-stu-id="09f2c-132">Write off transactions from the collections form.</span></span>
1. <span data-ttu-id="09f2c-133">Fara í **skuldir og innheimta > Innheimta > Aldursgreindar stöður**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-133">Go to **Credit and collections > Collections > Aged balances**.</span></span>
2. <span data-ttu-id="09f2c-134">Velja nafn viðskiptavinar sem hefur færslur sem á að afskrifa.</span><span class="sxs-lookup"><span data-stu-id="09f2c-134">Select the name of the customer that has the transactions that you want to write off.</span></span> <span data-ttu-id="09f2c-135">Veljið til dæmis Cave Wholesales (U.S.-004).</span><span class="sxs-lookup"><span data-stu-id="09f2c-135">For example, select Cave Wholesales (US-004).</span></span>
3. <span data-ttu-id="09f2c-136">Merkja línuna fyrir fyrstu færsluna.</span><span class="sxs-lookup"><span data-stu-id="09f2c-136">Mark the row for the first transaction.</span></span>
4. <span data-ttu-id="09f2c-137">Merkja línu fyrir aðra færslu.</span><span class="sxs-lookup"><span data-stu-id="09f2c-137">Mark the row for the second transaction.</span></span>
5. <span data-ttu-id="09f2c-138">Smellt er á **Afskrifa**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-138">Click **Write off**.</span></span>
6. <span data-ttu-id="09f2c-139">Færðu inn 'Lélegar skuldir' í svæði **Ástæðuathugasemd**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-139">In the **Reason comment** field, type 'Bad debts'.</span></span>
7. <span data-ttu-id="09f2c-140">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-140">Click **OK**.</span></span>
8. <span data-ttu-id="09f2c-141">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09f2c-141">Close the page.</span></span>
9. <span data-ttu-id="09f2c-142">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09f2c-142">Close the page.</span></span>
10. <span data-ttu-id="09f2c-143">Farðu í **Fjárhag > Færslubókarfærslur > Almennar færslubækur**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-143">Go to **General ledger > Journal entries > General journals**.</span></span>
11. <span data-ttu-id="09f2c-144">Veljið rununúmer færslubókar fyrir færslubók sem inniheldur afskrift.</span><span class="sxs-lookup"><span data-stu-id="09f2c-144">Select the journal batch number for the journal that contains your write-off.</span></span> <span data-ttu-id="09f2c-145">Ein lína er stofnuð til að snúa við stöðu viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="09f2c-145">One line is created to reverse the customer balance.</span></span> <span data-ttu-id="09f2c-146">Ein eða fleiri línur eru stofnaðar til að bóka afskriftir í afskriftarlykil.</span><span class="sxs-lookup"><span data-stu-id="09f2c-146">One or more lines are created to post the write-off to the write-off account.</span></span>  
12. <span data-ttu-id="09f2c-147">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09f2c-147">Close the page.</span></span>
13. <span data-ttu-id="09f2c-148">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09f2c-148">Close the page.</span></span>

## <a name="write-off-an-invoice-from-the-open-customers-invoices-page"></a><span data-ttu-id="09f2c-149">Afskrifa reikning frá síðunni Opna reikninga viðskiptavinir</span><span class="sxs-lookup"><span data-stu-id="09f2c-149">Write off an invoice from the Open customers invoices page</span></span>
1. <span data-ttu-id="09f2c-150">Farðu í **Skoðunarrúðu > Einingar > Viðskiptakröfur > Reikningar > Opnir reikningar viðskiptavina**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-150">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Open customer invoices**.</span></span>
2. <span data-ttu-id="09f2c-151">Merkja línu fyrir reiknings.</span><span class="sxs-lookup"><span data-stu-id="09f2c-151">Mark the line for an invoice.</span></span> <span data-ttu-id="09f2c-152">Til dæmis að merkja línuna fyrir CIV 000667.</span><span class="sxs-lookup"><span data-stu-id="09f2c-152">For example, mark the line for CIV-000667.</span></span>
3. <span data-ttu-id="09f2c-153">Í **aðgerðasvæðinu** er smellt á **Reikningur**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-153">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="09f2c-154">Smellt er á **Afskrifa**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-154">Click **Write off**.</span></span>
5. <span data-ttu-id="09f2c-155">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-155">Click **OK**.</span></span>
6. <span data-ttu-id="09f2c-156">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09f2c-156">Close the page.</span></span>

## <a name="write-off-a-customer-balance-from-the-customer-page"></a><span data-ttu-id="09f2c-157">Afskrifa staða viðskiptavinar á síðu viðskiptavinar</span><span class="sxs-lookup"><span data-stu-id="09f2c-157">Write off a customer balance from the customer page</span></span>
1. <span data-ttu-id="09f2c-158">Farið í **Viðskiptakröfur > Viðskiptavinir > Allir viðskiptavinir**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-158">Go to **Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="09f2c-159">Veljið viðskiptavinalykil.</span><span class="sxs-lookup"><span data-stu-id="09f2c-159">Select a customer account.</span></span> <span data-ttu-id="09f2c-160">Veljið til dæmis U.S.-001 (Contoso Retail San Diego).</span><span class="sxs-lookup"><span data-stu-id="09f2c-160">For example, select US-001 (Contoso Retail San Diego).</span></span>
3. <span data-ttu-id="09f2c-161">Í **aðgerðasvæðinu** er smellt á **Innheimta**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-161">On the **Action Pane**, click **Collect**.</span></span>
4. <span data-ttu-id="09f2c-162">Smellt er á **Afskrifa**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-162">Click **Write off**.</span></span>
5. <span data-ttu-id="09f2c-163">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="09f2c-163">Click **OK**.</span></span>
6. <span data-ttu-id="09f2c-164">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="09f2c-164">Close the page.</span></span>

