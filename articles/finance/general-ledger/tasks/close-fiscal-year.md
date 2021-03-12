---
title: Loka fjárhagsári
description: Þetta ferli fara í gegnum árslokaferli sem flytja stöður yfir á nýtt fjárhagsár.
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b82cc7e4077a1bd50eab30f234c2f63c79e81d84
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994691"
---
# <a name="close-the-fiscal-year"></a><span data-ttu-id="7539c-103">Loka fjárhagsári</span><span class="sxs-lookup"><span data-stu-id="7539c-103">Close the fiscal year</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7539c-104">Þetta ferli fara í gegnum árslokaferli sem flytja stöður yfir á nýtt fjárhagsár.</span><span class="sxs-lookup"><span data-stu-id="7539c-104">This procedure steps through the year end close process that transfers balances to a new fiscal year.</span></span>


## <a name="validate-year-end-close-parameters"></a><span data-ttu-id="7539c-105">Villuleita færibreytur árslokalokunar</span><span class="sxs-lookup"><span data-stu-id="7539c-105">Validate year-end close parameters</span></span>
1. <span data-ttu-id="7539c-106">Farðu í **Skoðunarrúðu > Kerfi > Fjárhagur > Fjárhagsuppsetning > Fjárhagsfæribreytur**.</span><span class="sxs-lookup"><span data-stu-id="7539c-106">Go to **Navigation pane > Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="7539c-107">Víkkaðu út hlutann **Lokun fjárhagsárs**.</span><span class="sxs-lookup"><span data-stu-id="7539c-107">Expand the **Fiscal year close** section.</span></span>
3. <span data-ttu-id="7539c-108">Veldu „Já“ eða „Nei“ fyrir valkostinn **Eyða lokunarfærslum árs í millifærslu**.</span><span class="sxs-lookup"><span data-stu-id="7539c-108">Select 'Yes' or 'No' for the **Delete close-of-year transactions during transfer** option.</span></span>
    
    <span data-ttu-id="7539c-109">Ef fjárhagsári hefur verið lokað og lokun ársloka er keyrt aftur, er þessa stillingu mikilvæg.</span><span class="sxs-lookup"><span data-stu-id="7539c-109">If the fiscal year has already been closed and the year-end close is being run again, this setting is important.</span></span> <span data-ttu-id="7539c-110">Ef stillt á Já, verður fylgiskjali fyrir lok fyrra árs eytt, og nýtt fylgiskjali verða stofnaðar fyrir allar upphafsstöður lykla.</span><span class="sxs-lookup"><span data-stu-id="7539c-110">If set to Yes, the voucher for the previous year-end close will be deleted, and a new voucher will be created for all accounts beginning balances.</span></span> <span data-ttu-id="7539c-111">Ef stillt á Nei, helst fyrri fylgiskjal og nýju fylgiskjali aðeins verður stofnuð til að leiðrétta færslur sem voru bókaðar eftir síðustu lokun ársloka.</span><span class="sxs-lookup"><span data-stu-id="7539c-111">If set to No, the previous voucher will remain and a new voucher will only be created for adjusting entries that were posted after the last year-end close.</span></span>

4. <span data-ttu-id="7539c-112">Veldu „Já“ eða „Nei“ fyrir valkostinn **Stofna lokunarfærslur í millifærslu**.</span><span class="sxs-lookup"><span data-stu-id="7539c-112">Select 'Yes' or 'No' for the **Create closing transactions during transfer** option.</span></span>

    <span data-ttu-id="7539c-113">Ef setja á Já tvær færslur eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="7539c-113">If set to Yes, two transactions are created.</span></span> <span data-ttu-id="7539c-114">Eitt fylgiskjal er stofnað í fjárhagsárinu sem verið er að loka til að færa stöður í P&L fjárhagslykla niður í núll og önnur fylgiskjal eru stofnuð á næsta fjárhagsári fyrir upphafsstöður.</span><span class="sxs-lookup"><span data-stu-id="7539c-114">One voucher is created in the fiscal year being closed to bring the balances of the P&L ledger accounts down to zero and a second voucher is created in the next fiscal year for the beginning balances.</span></span> <span data-ttu-id="7539c-115">Ef stillt á Nei, eitt fylgiskjal er stofnuð á næsta fjárhagsári fyrir upphafsstöður.</span><span class="sxs-lookup"><span data-stu-id="7539c-115">If set to No, a single voucher is created in the next fiscal year for the beginning balances.</span></span>  

5. <span data-ttu-id="7539c-116">Veldu „Já“ eða „Nei“ fyrir valkostinn **Stilla stöðu fjárhagsárs á lokað fyrir fullt og allt**.</span><span class="sxs-lookup"><span data-stu-id="7539c-116">Select 'Yes' or 'No' for the **Set fiscal year status to permanently closed** option.</span></span>

    <span data-ttu-id="7539c-117">Ef stillt á Já verður staða fjárhagsárs stillt á Endanlega lokað.</span><span class="sxs-lookup"><span data-stu-id="7539c-117">If set to Yes, the fiscal year status will be set to Permanently closed.</span></span>  <span data-ttu-id="7539c-118">Þar sem ekki er hægt að enduropna varanlega lokað ár, væri bestu venju að þessi valkostur er stilltur á nei.</span><span class="sxs-lookup"><span data-stu-id="7539c-118">Because a permanently closed year cannot be reopened, it would be a best practice to set this option to No.</span></span>  

6. <span data-ttu-id="7539c-119">Veldu „Já“ eða „Nei“ fyrir valkostinn **Rita þarf fylgiskjalsnúmer á meðan á lokun árs stendur**.</span><span class="sxs-lookup"><span data-stu-id="7539c-119">Select 'Yes' or 'No' for the **Voucher number must be filled in during the year end close** option.</span></span>

    <span data-ttu-id="7539c-120">Ef stillt á Já, verður að færa inn númer fylgiskjals handvirkt í árslokaferlinu.</span><span class="sxs-lookup"><span data-stu-id="7539c-120">If set to Yes, a voucher number must be manually entered during the year end close process.</span></span> <span data-ttu-id="7539c-121">Númeraröð er ekki notuð til að mynda þetta fylgiskjalsnúmer.</span><span class="sxs-lookup"><span data-stu-id="7539c-121">A number sequence is not used to generate this voucher number.</span></span> <span data-ttu-id="7539c-122">Bestu starfsvenjur er að setja þetta á Já.</span><span class="sxs-lookup"><span data-stu-id="7539c-122">It's a best practice to set this to Yes.</span></span>  

7. <span data-ttu-id="7539c-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="7539c-123">Close the page.</span></span>
8. <span data-ttu-id="7539c-124">Farðu í **Fjárhagur > Tímabil er lokað > Árslokalokun**.</span><span class="sxs-lookup"><span data-stu-id="7539c-124">Go to **General ledger > Period close > Year end close**.</span></span>
9. <span data-ttu-id="7539c-125">Smelltu á **Nýtt** til að stofna sniðmát árslokalokunar.</span><span class="sxs-lookup"><span data-stu-id="7539c-125">Click **New** to create a year-end close template.</span></span>

    <span data-ttu-id="7539c-126">Hægt er ða stofna sniðmát fyrir hóp lögaðila sem á að keyra árslokalokun fyrir.</span><span class="sxs-lookup"><span data-stu-id="7539c-126">A template can be created for a group of legal entities for which to run the year-end close.</span></span> <span data-ttu-id="7539c-127">Hægt er að endurnota þetta sniðmát ár eftir ár.</span><span class="sxs-lookup"><span data-stu-id="7539c-127">This template can be reused year after year.</span></span>  

10. <span data-ttu-id="7539c-128">Í reitnum **Heiti hóps** færirðu inn sniðmátsheiti árslokalokunar.</span><span class="sxs-lookup"><span data-stu-id="7539c-128">In the **Group name** field, enter a year-end close template name..</span></span>
11. <span data-ttu-id="7539c-129">Í reitnum **Fjárhagsdagatal** velurðu fjárhagsárið sem sniðmátið verður stofnað fyrir.</span><span class="sxs-lookup"><span data-stu-id="7539c-129">In the **Fiscal calendar** field, select the fiscal year for which the template will be created.</span></span>

    <span data-ttu-id="7539c-130">Aðeins er hægt að flokka lögaðila sem nota sama fjárhagsárið saman í sniðmáti árslokalokunar .</span><span class="sxs-lookup"><span data-stu-id="7539c-130">Only legal entities which use the same fiscal year can be grouped together in the year-end close template.</span></span> <span data-ttu-id="7539c-131">Þetta er vegna þess að árslokalokun er gerð með því að velja fjárhagsár, en ekki dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="7539c-131">This is because the year end close is done by selecting a fiscal year, not a date.</span></span>  

12. <span data-ttu-id="7539c-132">Í **Aðgerðasvæðinu** smellirðu á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="7539c-132">On the **Action pane**, click **Save**.</span></span>
13. <span data-ttu-id="7539c-133">Í hlutanum **Lögaðilar** smellirðu á **Bæta við** til að velja lögaðila fyrir þetta sniðmát.</span><span class="sxs-lookup"><span data-stu-id="7539c-133">In the **Legal entities** section, click **Add** to select the legal entities for this template.</span></span>
    
    <span data-ttu-id="7539c-134">Hægt er að bæta lögaðilar við með því að velja annað hvort lögaðila eða með því að velja stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="7539c-134">Legal entities can be added by either selecting the legal entities or by selecting an organizational hierarchy.</span></span>  <span data-ttu-id="7539c-135">Aðeins verður bætt við lögaðilum sem eru með stigveldi fyrirtækis með sama fjárhagsdagatal valið.</span><span class="sxs-lookup"><span data-stu-id="7539c-135">Only legal entities with the organizational hierarchy with the same fiscal calendar selected will be added.</span></span>  

14. <span data-ttu-id="7539c-136">Velja annaðhvort lögaðila eða stigveldisskipan.</span><span class="sxs-lookup"><span data-stu-id="7539c-136">Select either the legal entities or the organizational hierarchy.</span></span>
15. <span data-ttu-id="7539c-137">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="7539c-137">Click **OK**.</span></span>
16. <span data-ttu-id="7539c-138">Veldu „Já“ eða „Nei“ í **Flytja víddir efnahagsreiknings**.</span><span class="sxs-lookup"><span data-stu-id="7539c-138">Select 'Yes' or 'No' in the **Transfer balance sheet dimension**.</span></span>

    <span data-ttu-id="7539c-139">Bestu starfsvenjur eru að stilla þennan valkost á Já fyrir efnahagslykla.</span><span class="sxs-lookup"><span data-stu-id="7539c-139">It's best practice to set this option to Yes for Balance sheet accounts.</span></span> <span data-ttu-id="7539c-140">Þetta viðheldur fjárhagsvíddum á bókaðar færslur þegar stofnaðir eru upphafsstöður fyrir efnahagslykla.</span><span class="sxs-lookup"><span data-stu-id="7539c-140">This will maintain the financial dimensions on posted transactions when creating the beginning balances for the balance sheet accounts.</span></span> <span data-ttu-id="7539c-141">Fyrir rekstrarlykla, er hægt að velja að vinna með fjárhagsvíddir (Loka öllum) þegar stöður eru fluttar yfir á óráðstafað eigið fé eða þú getur valið að hafa fjárhagsvíddir skipt út fyrir annað víddargildi (Loka einum).</span><span class="sxs-lookup"><span data-stu-id="7539c-141">For profit and loss accounts, you can select to maintain the financial dimensions (Close all) when the balances are moved to Retained earnings or you can select to have the financial dimensions replaced with a different dimension value (Close single).</span></span> <span data-ttu-id="7539c-142">Ef þú velur Loka einum, geturðu skilgreint tiltekið víddargildi fyrir hverja vídd eða jafnvel valið að skilja eftir autt.</span><span class="sxs-lookup"><span data-stu-id="7539c-142">If you choose Close single, you can define a specific dimension value for each dimension or even choose to leave it blank.</span></span>  

17. <span data-ttu-id="7539c-143">Smellt er á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="7539c-143">Click **Save**.</span></span>
18. <span data-ttu-id="7539c-144">Hefja árslokalokun með því að velja **Keyra fjárhagslokun** á **Aðgerðarúðunni**.</span><span class="sxs-lookup"><span data-stu-id="7539c-144">Start the year-end close by choosing **Run fiscal close** on the **Action Pane**.</span></span> <span data-ttu-id="7539c-145">Árslokalokun verður keyrt fyrir valið sniðmát.</span><span class="sxs-lookup"><span data-stu-id="7539c-145">The year-end close will be run for the selected template.</span></span>  
19. <span data-ttu-id="7539c-146">Veldu allt eða hlutmengi lögaðila úr sniðmátinu úr hverju á að keyra árslokalokunina.</span><span class="sxs-lookup"><span data-stu-id="7539c-146">Select all or a subset of legal entities from the template for which to run the year-end close.</span></span>

    <span data-ttu-id="7539c-147">Þegar fyrst er keyrt árslokalokun, þá gætu flest fyrirtæki valið að keyra árslokalokun fyrir alla lögaðila innan þess sniðmáts til að fá upphafsstöður.</span><span class="sxs-lookup"><span data-stu-id="7539c-147">When first running the year-end close, to get beginning balance,s most organizations may choose to run the year-end close for all legal entities within the template.</span></span> <span data-ttu-id="7539c-148">Ef leiðréttingarfærslur eru gerðar eftir það, geturðu valið að keyra árslokalokun fyrir aðeins þeirra lögaðila sem hafa leiðréttingar.</span><span class="sxs-lookup"><span data-stu-id="7539c-148">If adjusting entries are made after that, you may choose to run the year-end close for only the legal entities that have adjustments.</span></span>  

20. <span data-ttu-id="7539c-149">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="7539c-149">Click **OK**.</span></span>
21. <span data-ttu-id="7539c-150">Velja fjárhagsár sem árslokalokun verður keyrð fyrir.</span><span class="sxs-lookup"><span data-stu-id="7539c-150">Select the fiscal year for which to run the year-end close.</span></span>
22. <span data-ttu-id="7539c-151">Í reitinn **Fylgiskjal** skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="7539c-151">In the **Voucher field**, type a value.</span></span> <span data-ttu-id="7539c-152">Bestu starfsvenjur eru að hafa fjárhagsár í fylgiskjalsnúmerinu, til að auðvelda að finna fylgiskjal árslokalokunar sem er stofnaður.</span><span class="sxs-lookup"><span data-stu-id="7539c-152">It's best practice to include the fiscal year in the voucher number, to make it easier to find the year-end close voucher that is created.</span></span>  
23. <span data-ttu-id="7539c-153">Árslokalokunin er sjálfgefið keyrt í runu.</span><span class="sxs-lookup"><span data-stu-id="7539c-153">The year-end close defaults to run in batch.</span></span> <span data-ttu-id="7539c-154">Það eru bestu starfsvenjur fyrir langtímaferli til að keyra í runuhætti.</span><span class="sxs-lookup"><span data-stu-id="7539c-154">It's best practice for long-running processes to run in batch mode.</span></span> <span data-ttu-id="7539c-155">Þetta er yfirleitt eitt af þessum ferlum, og er það ástæðan fyrir því að sjálfgefið er að nota runuhátt.</span><span class="sxs-lookup"><span data-stu-id="7539c-155">This is typically one of those processes, which is why the default is to use batch mode.</span></span>  
24. <span data-ttu-id="7539c-156">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="7539c-156">Click **OK**.</span></span>

