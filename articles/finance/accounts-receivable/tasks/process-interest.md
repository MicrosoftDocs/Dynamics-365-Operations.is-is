---
title: Reikna vexti
description: Þessi verklýsing sýnir hvernig á að stofna, prenta og bóka vaxtanótur.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 093fbd23f9fcaf62db9988a98a94b8cebf582768
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444402"
---
# <a name="process-interest"></a><span data-ttu-id="1ef16-103">Reikna vexti</span><span class="sxs-lookup"><span data-stu-id="1ef16-103">Process interest</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1ef16-104">Þessi verklýsing sýnir hvernig á að stofna, prenta og bóka vaxtanótur.</span><span class="sxs-lookup"><span data-stu-id="1ef16-104">This procedure shows how to create, print, and post interest notes.</span></span> <span data-ttu-id="1ef16-105">Þetta verkefni notar USMF-sýnifyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="1ef16-105">This task uses the USMF demo company.</span></span>


## <a name="set-up-interest-on-the-posting-profile"></a><span data-ttu-id="1ef16-106">Setja upp vexti fyrir bókunarregluna</span><span class="sxs-lookup"><span data-stu-id="1ef16-106">Set up interest on the posting profile</span></span>
1. <span data-ttu-id="1ef16-107">Í **Skoðunarrúðu** ferðu í **Kerfiseiningar > Skuldir og innheimta > Uppsetning > Bókunarreglur viðskiptavina**.</span><span class="sxs-lookup"><span data-stu-id="1ef16-107">In the **Navigation pane**, go to **Modules > Credit and collections > Setup > Customer posting profiles**.</span></span>
2. <span data-ttu-id="1ef16-108">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="1ef16-108">Click **Edit**.</span></span>
3. <span data-ttu-id="1ef16-109">Í **Setja upp flýtiflipa**, í reitnum **Vaxtakóði** skaltu velja vaxtakóða úr fellivalmyndinni.</span><span class="sxs-lookup"><span data-stu-id="1ef16-109">In the **Setup fastTab**, in the **Interest code** field, select an interest code from the drop-down list.</span></span> <span data-ttu-id="1ef16-110">Ef ekki á að reikna vexti fyrir færslur með þessari bókunarreglu, skilið eftir autt.</span><span class="sxs-lookup"><span data-stu-id="1ef16-110">If you do not want interest calculated for transactions using this posting profile, leave the field blank.</span></span> <span data-ttu-id="1ef16-111">Flýtiflipinn **Töflutakmarkanir** gerir þér kleift að breyta hvernig vextir eru unnir.</span><span class="sxs-lookup"><span data-stu-id="1ef16-111">The **Table restriction** fastTab allows you to change the way that interest is processed.</span></span> <span data-ttu-id="1ef16-112">Ef þetta svæði er stillt á Já eru vextir reiknast fyrir þessa bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="1ef16-112">If this field is set to Yes, then interest will be calculated for this posting profile.</span></span>  

## <a name="calculate-interest"></a><span data-ttu-id="1ef16-113">Reikna út vexti</span><span class="sxs-lookup"><span data-stu-id="1ef16-113">Calculate interest</span></span>
1. <span data-ttu-id="1ef16-114">Í **Skoðunarrúðu** ferðu í **Kerfiseiningar > Skuldir og innheimta > Vextir > Stofna vaxtanótur**.</span><span class="sxs-lookup"><span data-stu-id="1ef16-114">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Create interest notes**.</span></span>
2. <span data-ttu-id="1ef16-115">Velja færslugerðir sem verður að reikna út vexti fyrir.</span><span class="sxs-lookup"><span data-stu-id="1ef16-115">You must select the transaction types for which you will calculate interest.</span></span> <span data-ttu-id="1ef16-116">Allar opnar færslur fyrir þessar gerðir verða teknar með í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="1ef16-116">All of the open transactions for these types will be included in the calculation.</span></span>  
3. <span data-ttu-id="1ef16-117">Ef þú stillir **Vexti** á Já muntu reikna vaxtavexti.</span><span class="sxs-lookup"><span data-stu-id="1ef16-117">If you set **Interest** to 'Yes', you will calculate interest on interest.</span></span> <span data-ttu-id="1ef16-118">Hægt er að athuga lög um útreikningi á vaxtavöxtum áður en þessar færslur eru hafðar með.</span><span class="sxs-lookup"><span data-stu-id="1ef16-118">You may want to check the laws governing the calculation of interest on interest before including these transactions.</span></span>  
4. <span data-ttu-id="1ef16-119">Í reitinn **Frá dagsetningu** skal færa inn dagsetningu sem vextirnir verða reiknaðir frá.</span><span class="sxs-lookup"><span data-stu-id="1ef16-119">In the **From date** field, enter a date from which the interest will be calculated.</span></span> <span data-ttu-id="1ef16-120">Ef ekki er tiltekin **Frá dagsetningu** verður hætt við allar óbókaðar vaxtanótur og vextir verða endurreiknaðir frá færsludagsetningu.</span><span class="sxs-lookup"><span data-stu-id="1ef16-120">If you do not specific a **From date**, then all unposted interest notes will be canceled and interest will be recalculated from the transaction date.</span></span>
5. <span data-ttu-id="1ef16-121">Í reitinn **Til dagsetningar** skal færa inn dagsetningu sem vextirnir verða reiknaðir til.</span><span class="sxs-lookup"><span data-stu-id="1ef16-121">In the **To date** field, enter a date to which the interest would be calculated.</span></span>
6. <span data-ttu-id="1ef16-122">Í reitnum **Nota virði frá** skal velja valkost.</span><span class="sxs-lookup"><span data-stu-id="1ef16-122">In the **Use posting profile from** field, select an option.</span></span> <span data-ttu-id="1ef16-123">Í boði eru þrír valkostir fyrir bókunarreglu:</span><span class="sxs-lookup"><span data-stu-id="1ef16-123">There are three posting profile options:</span></span>
    - <span data-ttu-id="1ef16-124">Reikningur – Nota bókunarreglu sem er úthlutað til reikning viðskiptavinar fyrir hverja vaxtanótu.</span><span class="sxs-lookup"><span data-stu-id="1ef16-124">Account – Use the posting profile that is assigned to the customer account for each interest note.</span></span> 
    - <span data-ttu-id="1ef16-125">Velja – Notið bókunarregluna sem valin var á svæðinu .</span><span class="sxs-lookup"><span data-stu-id="1ef16-125">Select – Use the posting profile that you select in the Posting profile field.</span></span>
    - <span data-ttu-id="1ef16-126">Færsla – Notið einstaka bókunarreglu úr færslum þar sem vextir eru reiknaðir fyrir hverja vaxtanótu.</span><span class="sxs-lookup"><span data-stu-id="1ef16-126">Transaction – Use the individual posting profile from transactions on which interest is calculated for each interest note.</span></span> <span data-ttu-id="1ef16-127">Færslur sem hafa ekki úthlutaða bókunarreglu nota bókunarreglu sem er tilgreind á svæðinu Fjárhagur og virðisaukaskattur í skjámyndinni Færibreytur viðskiptakrafna.</span><span class="sxs-lookup"><span data-stu-id="1ef16-127">Transactions that do not have an assigned posting profile will use the posting profile that is specified in the Ledger and sales tax area of the Accounts receivable parameters form.</span></span>  
7. <span data-ttu-id="1ef16-128">Útvíkkaðu flýtiflipann **Færslur til að taka með**.</span><span class="sxs-lookup"><span data-stu-id="1ef16-128">Expand the **Records to include** fastTab.</span></span>
8. <span data-ttu-id="1ef16-129">Smella á **Sía**.</span><span class="sxs-lookup"><span data-stu-id="1ef16-129">Click **Filter**.</span></span>
9. <span data-ttu-id="1ef16-130">Í svæðinu **Skilyrði** skal færa inn auðkenni viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="1ef16-130">In the **Criteria** field, enter a Customer ID.</span></span> <span data-ttu-id="1ef16-131">Til dæmis, færið inn ‚US-001'.</span><span class="sxs-lookup"><span data-stu-id="1ef16-131">For example, enter 'US-001'.</span></span>
6. <span data-ttu-id="1ef16-132">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ef16-132">Click **OK**.</span></span>
7. <span data-ttu-id="1ef16-133">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ef16-133">Click **OK**.</span></span>

## <a name="print-interest-notes"></a><span data-ttu-id="1ef16-134">Prenta vaxtanótur</span><span class="sxs-lookup"><span data-stu-id="1ef16-134">Print interest notes</span></span>
1. <span data-ttu-id="1ef16-135">Í **Skoðunarrúðu** ferðu í **Kerfiseiningar > Skuldir og innheimta > Vextir > Endurskoða og vinna vaxtanótur**.</span><span class="sxs-lookup"><span data-stu-id="1ef16-135">In the **Navigation pane**, go to **Modules > Credit and collections > Interest > Review and process interest notes**.</span></span>
2. <span data-ttu-id="1ef16-136">Í reitnum **Staða** er ‚Stofnað' valið.</span><span class="sxs-lookup"><span data-stu-id="1ef16-136">In the **Status** field, select 'Created'.</span></span>
3. <span data-ttu-id="1ef16-137">Í reitnum **Prentað** skal velja 'Ekki prentað'.</span><span class="sxs-lookup"><span data-stu-id="1ef16-137">In the **Printed** field, select 'Not printed'.</span></span>
4. <span data-ttu-id="1ef16-138">Smelltu á **Prenta**.</span><span class="sxs-lookup"><span data-stu-id="1ef16-138">Click **Print**.</span></span>
5. <span data-ttu-id="1ef16-139">Útvíkkaðu flýtiflipann **Færslur til að taka með**.</span><span class="sxs-lookup"><span data-stu-id="1ef16-139">Expand the **Records to include** fastTab.</span></span>
6. <span data-ttu-id="1ef16-140">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ef16-140">Click **OK**.</span></span>
7. <span data-ttu-id="1ef16-141">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="1ef16-141">Close the page.</span></span>

## <a name="post-the-interest-note"></a><span data-ttu-id="1ef16-142">Bóka vaxtanótu</span><span class="sxs-lookup"><span data-stu-id="1ef16-142">Post the interest note</span></span>
1. <span data-ttu-id="1ef16-143">Velja vaxtanótu sem er að tilbúin til bókunar (staða er stofnuð).</span><span class="sxs-lookup"><span data-stu-id="1ef16-143">Select an interest note that is ready to post (status is created).</span></span>
2. <span data-ttu-id="1ef16-144">Smelltu á **bóka.**</span><span class="sxs-lookup"><span data-stu-id="1ef16-144">Click **Post**.</span></span>
3. <span data-ttu-id="1ef16-145">Færð er inn bókunardagsetning fyrir vaxtanóta.</span><span class="sxs-lookup"><span data-stu-id="1ef16-145">Enter the posting date for the interest note.</span></span> <span data-ttu-id="1ef16-146">Skal velja Já í stofna fjárhagsfærsla fyrir hverja vaxtanóta.</span><span class="sxs-lookup"><span data-stu-id="1ef16-146">Select Yes to create a general ledger transaction for each interest note.</span></span> <span data-ttu-id="1ef16-147">Ef þú velur ekki já, safnast upp allir vextir á vaxtanóta til viðskiptavinarins og eru bókaðar á fjárhag í einni færslu.</span><span class="sxs-lookup"><span data-stu-id="1ef16-147">If you do not select Yes, the interest on all interest notes to the customer is accumulated and posted to the general ledger in one transaction.</span></span>  
4. <span data-ttu-id="1ef16-148">Útvíkkaðu flýtiflipann **Færslur til að taka með**.</span><span class="sxs-lookup"><span data-stu-id="1ef16-148">Expand the **Records to include** fastTab.</span></span>
5. <span data-ttu-id="1ef16-149">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="1ef16-149">Click **OK**.</span></span>
6. <span data-ttu-id="1ef16-150">Í reitnum **Staða** er ‚bókað' valið.</span><span class="sxs-lookup"><span data-stu-id="1ef16-150">In the **Status** field, select 'Posted'.</span></span>

