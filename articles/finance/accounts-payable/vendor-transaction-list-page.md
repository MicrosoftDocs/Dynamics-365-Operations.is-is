---
title: Listasíða með lánardrottnafærslum
description: Þetta efnisatriði veitir upplýsingar um listasíðu með lánardrottnafærslum fyrir Microsoft Dynamics 365 Finance.
author: mikefalkner
manager: aolson
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mikefalkner
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 6008a968568806bdf2c3194d32aecf9f67dbce2b
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178341"
---
# <a name="vendor-transactions-list-page"></a><span data-ttu-id="6fa36-103">Listasíða með lánardrottnafærslum</span><span class="sxs-lookup"><span data-stu-id="6fa36-103">Vendor transactions list page</span></span>

[!include [banner](../includes/banner.md)]

## <a name="view-settlements"></a><span data-ttu-id="6fa36-104">Skoða uppgjör</span><span class="sxs-lookup"><span data-stu-id="6fa36-104">View settlements</span></span>

<span data-ttu-id="6fa36-105">**Skoða uppgjör** hnappinn á aðgerðarsvæðinu veitir skjótan aðgang að uppgjörsferlinu og nákvæmar upplýsingar um uppgjörsfærsluna.</span><span class="sxs-lookup"><span data-stu-id="6fa36-105">The **View settlements** button on the Action Pane provides quick access to the settlement history and detailed information about the settlement transaction.</span></span> <span data-ttu-id="6fa36-106">Þú getur einnig sýnt fleiri færslur sem tengjast valdri færslu, annaðhvort vegna þess að þær voru hluti af sama uppgjörinu eða vegna þess að þær eru greiðslur sem voru búnar til í sömu greiðslubókinni.</span><span class="sxs-lookup"><span data-stu-id="6fa36-106">You can also show additional transactions that are related to the selected transaction, either because they were part of the same settlement or because they are payments that were created in the same payment journal.</span></span>

1. <span data-ttu-id="6fa36-107">Veldu **Viðskiptaskuldir \> Allir lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="6fa36-107">Select **Accounts payable \> All vendors**.</span></span>
2. <span data-ttu-id="6fa36-108">Veldu lánardrottin sem er með færslur og síðan á aðgerðasvæðinu í flipanum **Lánardrottinn** skaltu smella á **Færslur**.</span><span class="sxs-lookup"><span data-stu-id="6fa36-108">Select a vendor that has transactions, and then, on the Action Pane, on the **Vendor** tab, select **Transactions**.</span></span>
3. <span data-ttu-id="6fa36-109">Veldu færslu til að kanna og síðan á aðgerðasvæðinu skaltu smella á **Skoða uppgjör**.</span><span class="sxs-lookup"><span data-stu-id="6fa36-109">Select a transaction to research, and then, on the Action Pane, select **View settlements**.</span></span>

    <span data-ttu-id="6fa36-110">Svarglugginn **Skoða uppgjör** birtist og sýnir valda færslu og öll skjöl sem hafa verið jöfnuð á móti henni.</span><span class="sxs-lookup"><span data-stu-id="6fa36-110">The **View settlements** dialog box appears, and shows the selected transaction and all documents that have been settled against it.</span></span> <span data-ttu-id="6fa36-111">Þessi svargluggi líkist yfirliti uppgjörsferils, en hann inniheldur öll tengd skjöl.</span><span class="sxs-lookup"><span data-stu-id="6fa36-111">This dialog box resembles the settlement history view, but it includes all related documents.</span></span>

4. <span data-ttu-id="6fa36-112">Í svarglugganum er hægt að framkvæma ýmis verk.</span><span class="sxs-lookup"><span data-stu-id="6fa36-112">In the dialog box, you can perform various tasks.</span></span> <span data-ttu-id="6fa36-113">Veldu eitt eða fleiri fylgiskjöl og veldu síðan einn af eftirfarandi hnöppum:</span><span class="sxs-lookup"><span data-stu-id="6fa36-113">Select one or more vouchers, and then select one of the following buttons:</span></span>

    - <span data-ttu-id="6fa36-114">**Skoða tengt** - Sýna allar greiðslubókarfærslur og færslubókarfærslur fyrir lánardrottin sem var búinn til í færslubókunum þar sem skjölin sem sýnd eru í listanum voru búin til.</span><span class="sxs-lookup"><span data-stu-id="6fa36-114">**View related** – Show all the payment journal transactions and general journal tranactions for the vendor that were created in the journals in which the documents shown in the list were created.</span></span> <span data-ttu-id="6fa36-115">Til dæmis, ef greiðsla er sýnd, birtast allar greiðslur í greiðslubókinni þar sem hún var búin til.</span><span class="sxs-lookup"><span data-stu-id="6fa36-115">For example, if a payment is shown, then all of the payments in the payment journal in which it was created will be shown.</span></span> <span data-ttu-id="6fa36-116">Ef reikningur eða greiðsla er sýnd og hún var búin til í almennri færslubók, þá birtast öll skjölin í almennu færslubókinni þar sem hún var búin til.</span><span class="sxs-lookup"><span data-stu-id="6fa36-116">If an invoice or payment is shown and it was created in a general journal, then all of the documents in the general journal in which it was created will be shown.</span></span> <span data-ttu-id="6fa36-117">Öll uppgjör sem tengjast skjalalista eru einnig sýnd.</span><span class="sxs-lookup"><span data-stu-id="6fa36-117">All the settlements that are related to list of documents are also shown.</span></span> <span data-ttu-id="6fa36-118">Við skoðun á tengdum greiðslum breytist merkið á þessum hnappi í **Skoða uppgjör**.</span><span class="sxs-lookup"><span data-stu-id="6fa36-118">While you're viewing related payments, the label of this button changes to **View settlements**.</span></span> <span data-ttu-id="6fa36-119">Veldu **Skoða uppgjör** til að sýna aðeins færslurnar sem sýndar voru þegar þú opnaðir fyrst svargluggann **Skoða uppgjör**.</span><span class="sxs-lookup"><span data-stu-id="6fa36-119">Select **View settlements** to show only the transactions that were shown when you first opened the **View settlements** dialog box.</span></span>
    - <span data-ttu-id="6fa36-120">**Skoða feril** - Skoða uppgjörsferli fyrir fylgiskjölin.</span><span class="sxs-lookup"><span data-stu-id="6fa36-120">**View history** – Show the settlement history for the vouchers.</span></span> <span data-ttu-id="6fa36-121">Veldu **Loka** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="6fa36-121">Select **Close** to close the dialog box.</span></span>
    - <span data-ttu-id="6fa36-122">**Skoða bókhald** - Sýna öll fylgiskjöl sem tengjast völdum skjölum.</span><span class="sxs-lookup"><span data-stu-id="6fa36-122">**View accounting** – Show all vouchers that are related to the selected documents.</span></span> <span data-ttu-id="6fa36-123">Veldu **Loka** til að loka svarglugganum.</span><span class="sxs-lookup"><span data-stu-id="6fa36-123">Select **Close** to close the dialog box.</span></span>
    - <span data-ttu-id="6fa36-124">**Flytja út** - Flyttu út valin fylgiskjöl í Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="6fa36-124">**Export** – Export the selected vouchers to Microsoft Excel.</span></span>
    - <span data-ttu-id="6fa36-125">**Gera upp færslur** - Þessi hnappur birtist aðeins ef upprunalega skjalið sem var valið var ekki að gert upp að fullu.</span><span class="sxs-lookup"><span data-stu-id="6fa36-125">**Settle transactions** – This button appears only if the original document that was selected wasn't fully settled.</span></span> <span data-ttu-id="6fa36-126">Þegar þú velur þennan hnapp birtist svarglugginn **Gera upp færslur** þar sem þú getur valið færslur til að gera upp.</span><span class="sxs-lookup"><span data-stu-id="6fa36-126">When you select this button, the **Settle transactions** dialog box appears, where you can select transactions for settlement.</span></span>
    - <span data-ttu-id="6fa36-127">**Afturkalla uppgjör** - Þessi hnappur birtist aðeins ef upprunalega skjalið sem var valið var gert upp að fullu.</span><span class="sxs-lookup"><span data-stu-id="6fa36-127">**Undo settlements** – This button appears only if the original document that was selected was fully settled.</span></span> <span data-ttu-id="6fa36-128">Þegar þú velur þennan hnapp birtist svarglugginn **Afturkalla uppgjör** þar sem þú getur afturkallað uppgjör sem voru gerð á skjalinu.</span><span class="sxs-lookup"><span data-stu-id="6fa36-128">When you select this button, the **Undo settlements** dialog box appears, where you can undo the settlements that were done for that document.</span></span>

## <a name="global-transactions"></a><span data-ttu-id="6fa36-129">Alþjóðlegar færslur</span><span class="sxs-lookup"><span data-stu-id="6fa36-129">Global transactions</span></span>

<span data-ttu-id="6fa36-130">Hnappurinn **Alþjóðlegar færslur** birtist einnig á listasíðunni **Lánardrottnafærslur**.</span><span class="sxs-lookup"><span data-stu-id="6fa36-130">The **Global transactions** button also displays on the **Vendor transactions** list page.</span></span> <span data-ttu-id="6fa36-131">Þessi hnappur gerir þér kleift að skoða allar færslur fyrir lánardrottin yfir alla lögaðila.</span><span class="sxs-lookup"><span data-stu-id="6fa36-131">This button lets you view all transactions for a vendor across all legal entities.</span></span> <span data-ttu-id="6fa36-132">Listasíðan **Lánardrottnafærslur** sýnir færslur aðeins fyrir lögaðila sem notandinn hefur aðgang að, byggt á öryggisstillingum notanda.</span><span class="sxs-lookup"><span data-stu-id="6fa36-132">The **Vendor transactions** list page shows transactions only for the legal entities that the user has access to, based on his or her security settings.</span></span>

<span data-ttu-id="6fa36-133">Listasíðan sýnir allar færslur fyrir lánardrottna sem hafa sama auðkenni aðila eins og lánardrottin sem þú byrjaðir með.</span><span class="sxs-lookup"><span data-stu-id="6fa36-133">The list page will show all transactions for vendors that have the same party ID as the vendor that you started with.</span></span> <span data-ttu-id="6fa36-134">Til dæmis, ef lánardrottinn US-001 í einum lögaðila hefur sama auðkenni aðila og lánardrottinn DE-001 í öðrum lögaðila, eru allar færslur fyrir bæði auðkenni lánardrottins sýndar.</span><span class="sxs-lookup"><span data-stu-id="6fa36-134">For example, if vendor US-001 in one legal entity has the same party ID as vendor DE-001 in another legal entity, all transactions for both vendor IDs are shown.</span></span>

<span data-ttu-id="6fa36-135">Valmyndirnar á listasíðunni **Lánardrottnafærslur** eru breytilegar, fer eftir lögaðila færslunnar.</span><span class="sxs-lookup"><span data-stu-id="6fa36-135">The menus on the **Vendor transactions** list page vary, depending on the legal entity for the transaction.</span></span> <span data-ttu-id="6fa36-136">Til dæmis, ef eiginleiki er aðeins í boði fyrir svissneska lögaðila, birtast aðeins valkostir valmyndarinnar fyrir þá eiginleika þegar svissnesk færsla er valin.</span><span class="sxs-lookup"><span data-stu-id="6fa36-136">For example, if a feature is available only for Swiss legal entities, the menu options for that feature appear only when a Swiss transaction is selected.</span></span>

<span data-ttu-id="6fa36-137">Fylgið eftirfarandi skrefum til að fá aðgang að eiginleikanum.</span><span class="sxs-lookup"><span data-stu-id="6fa36-137">To access the feature, follow these steps.</span></span>

1. <span data-ttu-id="6fa36-138">Veldu **Viðskiptaskuldir** \> **Allir lánardrottnar**.</span><span class="sxs-lookup"><span data-stu-id="6fa36-138">Select **Accounts payable** \> **All vendors**.</span></span>
2. <span data-ttu-id="6fa36-139">Veldu lánardrottin og síðan á aðgerðasvæðinu í flipanum **Lánardrottinn** í flokknum **Færslur** skal velja **Alþjóðlegar færslur**.</span><span class="sxs-lookup"><span data-stu-id="6fa36-139">Select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Global transactions**.</span></span>

## <a name="more-transaction-filters"></a><span data-ttu-id="6fa36-140">Fleiri færslusíur</span><span class="sxs-lookup"><span data-stu-id="6fa36-140">More transaction filters</span></span>

<span data-ttu-id="6fa36-141">Sían til að sýna opnar færslur hefur verið skipt út fyrir nýja síu sem leyfir þér að skoða fleiri samsetningar af færslum.</span><span class="sxs-lookup"><span data-stu-id="6fa36-141">The filter for showing open transactions has been replaced with a new filter that lets you view more combinations of transactions.</span></span> <span data-ttu-id="6fa36-142">Eftirfarandi valkostir eru í boði í reitnum **Sýna**:</span><span class="sxs-lookup"><span data-stu-id="6fa36-142">The following options are available in the **Show** field:</span></span>

- <span data-ttu-id="6fa36-143">**Allar** - Sýna allar færslur fyrir valinn lánardrottin (opnar og lokaðar).</span><span class="sxs-lookup"><span data-stu-id="6fa36-143">**All** – Show all transactions for the selected vendors (open and closed).</span></span>
- <span data-ttu-id="6fa36-144">**Lokaðar** - Sýna aðeins færslur sem hafa verið gerðar upp að fullu og lokaðar.</span><span class="sxs-lookup"><span data-stu-id="6fa36-144">**Closed** – Show only transactions that have been fully settled and closed.</span></span>
- <span data-ttu-id="6fa36-145">**Opnar** - Sýna aðeins færslur sem ekki hafa verið gerðar upp að fullu.</span><span class="sxs-lookup"><span data-stu-id="6fa36-145">**Open** – Show only transactions that haven't been fully settled.</span></span>
- <span data-ttu-id="6fa36-146">**Opið þ.m.t. lokað á eða eftir dagsetninguna** - Sýna aðeins færslur sem ekki hafa verið gerðar upp að fullu á eða eftir dagsetningu sem þú tilgreinir.</span><span class="sxs-lookup"><span data-stu-id="6fa36-146">**Open including closed on or after date** – Show only transactions that haven't been fully settled on or after a date that you specify.</span></span> <span data-ttu-id="6fa36-147">Þegar þessi valkostur er valinn er hægt að breyta dagsetningunni sem er sýnd við hliðina á síunni.</span><span class="sxs-lookup"><span data-stu-id="6fa36-147">When you select this option, you can change the date that is shown next to the filter.</span></span> <span data-ttu-id="6fa36-148">Færslur sem eru með gildi fyrir **Síðustu uppgjörsdagsetningu** eða eftir dagsetningunni sem þú tilgreinir eru sýndar í listanum, ef þessar færslur eru gerðar upp að fullu frá og með núverandi dagsetningu.</span><span class="sxs-lookup"><span data-stu-id="6fa36-148">Transactions that have a **Last settlement date** value on or after the date that you specify are shown in the list, even if those transactions are fully settled as of the current date.</span></span> <span data-ttu-id="6fa36-149">Hins vegar sýnir staðan stöðurnar frá og með núverandi degi, ekki frá þeim degi sem valinn er.</span><span class="sxs-lookup"><span data-stu-id="6fa36-149">However, the balance represents the balances as of the current date, not as of the selected date.</span></span>

<span data-ttu-id="6fa36-150">Veldu **Fela endurmat á gjaldmiðli** gátreitinn til að fela færslur fyrir umreikning gjaldmiðils.</span><span class="sxs-lookup"><span data-stu-id="6fa36-150">Select the **Hide currency revaluations** check box to hide currency translation transactions.</span></span>

## <a name="modify-due-dates-and-discount-dates"></a><span data-ttu-id="6fa36-151">Breyta gjalddögum og afsláttardagsetningum</span><span class="sxs-lookup"><span data-stu-id="6fa36-151">Modify due dates and discount dates</span></span>

<span data-ttu-id="6fa36-152">Þú getur uppfært gjalddaga og afsláttardagsetningar fyrir opnar færslur viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="6fa36-152">You can update due dates and discount dates for open customer transactions.</span></span> <span data-ttu-id="6fa36-153">Í útgáfu 8.1 er nú hægt að bæta við gjalddögum á listasíðuna **Lánardrottnafærslur**.</span><span class="sxs-lookup"><span data-stu-id="6fa36-153">In release 8.1, you can now add due dates to the **Vendor transactions** list page.</span></span> <span data-ttu-id="6fa36-154">Með því að smella á gjalddaga á listasíðunni **Lánardrottnafærslur** getur þú líka breytt gjalddögum, afsláttardagsetningum, greiðsluskilmálum og skilmálum staðgreiðsluafsláttar í svarglugganum **Uppfæra gjalddaga og dagsetningar staðgreiðsluafsláttar**.</span><span class="sxs-lookup"><span data-stu-id="6fa36-154">By clicking on the due date in the **Vendor transactions** list page, you can also change due dates, discount dates, payment terms, and cash discount terms in the **Update due date and cash discount dates**  dialog box.</span></span>

### <a name="activate-the-feature"></a><span data-ttu-id="6fa36-155">Virkja eiginleikann</span><span class="sxs-lookup"><span data-stu-id="6fa36-155">Activate the feature</span></span>

<span data-ttu-id="6fa36-156">Til að bæta gjalddögum við listasíðuna **Lánardrottnafærslur** og breyta greiðslustillingum fyrir færslu með því að nota svargluggann **Uppfæra gjalddaga og dagsetningar staðgreiðsluafsláttar** skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="6fa36-156">To add due dates to the **Vendor transactions** list page and change payment settings for a transaction by using the **Update due date and cash discount dates** dialog box, follow these steps.</span></span>

1. <span data-ttu-id="6fa36-157">Veldu **Viðskiptaskuldir \> Uppsetning \> Færibreytur viðskiptaskulda**.</span><span class="sxs-lookup"><span data-stu-id="6fa36-157">Select **Accounts payable \> Setup \> Accounts payable parameters**.</span></span>
2. <span data-ttu-id="6fa36-158">Í flipanum **Uppgjör** skal setja valkostinn **Sýna gjalddaga og leyfa breytingar** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="6fa36-158">On the **Settlements** tab, set the **Show due date and allow edit** option to **Yes**.</span></span>
3. <span data-ttu-id="6fa36-159">Til að virkja þennan valkost hefur nýjum reitum verið bætt við lánardrottnafærslur.</span><span class="sxs-lookup"><span data-stu-id="6fa36-159">To enable this feature, new fields have been added to vendor transactions.</span></span> <span data-ttu-id="6fa36-160">Fylltu verður í þessa reiti þegar ný færsla klárast.</span><span class="sxs-lookup"><span data-stu-id="6fa36-160">Those fields will be filled in when a new transaction is completed.</span></span> <span data-ttu-id="6fa36-161">Þeir verða einnig útfylltir þegar þú opnar svargluggann **Uppfæra gjalddaga og dagsetningar staðgreiðsluafsláttar**.</span><span class="sxs-lookup"><span data-stu-id="6fa36-161">They will also be filled in when you open the **Update due date and cash discount dates** dialog box.</span></span> <span data-ttu-id="6fa36-162">Þegar þú stillir valkostinn **Sýna gjalddaga og leyfa breytingar** á **Já** munt þú sjá svargluggann **Uppfæra greiðsluupplýsingar**.</span><span class="sxs-lookup"><span data-stu-id="6fa36-162">When you set the **Show due date and allow edit** option to **Yes**, you will see the **Update payment information** dialog box.</span></span>  <span data-ttu-id="6fa36-163">Til að uppfæra fyrirliggjandi færslur strax skaltu velja **Uppfæra allar fyrirliggjandi færslur**.</span><span class="sxs-lookup"><span data-stu-id="6fa36-163">To update existing transactions immediately, select **Update all existing transactions**.</span></span> <span data-ttu-id="6fa36-164">Að öðrum kosti, til að fylla út reitina aðeins fyrir nýjar færslur, skaltu velja **Halda áfram án uppfærslu**.</span><span class="sxs-lookup"><span data-stu-id="6fa36-164">Alternatively, to fill in the fields only for new transactions, select **Continue without update**.</span></span>

<span data-ttu-id="6fa36-165">Gjalddaga hefur nú verið bætt við listasíðuna **Lánardrottnafærslur** og þú getur á þægilegri hátt breytt gjalddaganum og dagsetningum staðgreiðsluafsláttar fyrir færslur.</span><span class="sxs-lookup"><span data-stu-id="6fa36-165">The due date is now added to the **Vendor transactions** list page, so you can easily modify the due date and cash discount dates for transactions.</span></span>

### <a name="modify-the-payment-settings"></a><span data-ttu-id="6fa36-166">Breyta greiðslustillingum</span><span class="sxs-lookup"><span data-stu-id="6fa36-166">Modify the payment settings</span></span>

<span data-ttu-id="6fa36-167">Listasíðan **Lánardrottnafærslur** sýnir allar færslur fyrir lánardrottin.</span><span class="sxs-lookup"><span data-stu-id="6fa36-167">The **Vendor transactions** list page shows all transactions for a vendor.</span></span> <span data-ttu-id="6fa36-168">Svargluggi birtist þegar þú velur gjalddaga fyrir færslu.</span><span class="sxs-lookup"><span data-stu-id="6fa36-168">When you select the due date for a transaction, a dialog box appears.</span></span> <span data-ttu-id="6fa36-169">Þessi svargluggi sýnir grunndagsetninguna fyrir gjalddaga og afsláttarútreikninga, gjalddaga, greiðsluskilmála, skilmála staðgreiðsluafsláttar og dagsetningu staðgreiðsluafsláttar.</span><span class="sxs-lookup"><span data-stu-id="6fa36-169">This dialog box shows the base date for due date and discount calculations, due date, payment terms, cash discount terms, and cash discount dates.</span></span>

<span data-ttu-id="6fa36-170">Hver reitur hefur mismunandi áhrif á færsluna þegar þú breytir honum:</span><span class="sxs-lookup"><span data-stu-id="6fa36-170">Each field has a different effect on the transaction when you edit it:</span></span>

- <span data-ttu-id="6fa36-171">**Breyta grunndagsetningunni** - Gjalddaga og afsláttardagsetningum er breytt eins og grunndagsetningin sé dagsetning skjalsins.</span><span class="sxs-lookup"><span data-stu-id="6fa36-171">**Edit the base date** - The due date and discount dates are changed as if the base date is the document date.</span></span>
- <span data-ttu-id="6fa36-172">**Breyta gjalddaga** - Aðeins gjalddaganum er breytt</span><span class="sxs-lookup"><span data-stu-id="6fa36-172">**Edit the due date** - Only the due date is changed</span></span>
- <span data-ttu-id="6fa36-173">**Breyta afsláttardagsetningum** - Aðeins afsláttardagsetningum er breytt.</span><span class="sxs-lookup"><span data-stu-id="6fa36-173">**Edit the discount dates** - Only the discount dates are changed.</span></span>
- <span data-ttu-id="6fa36-174">**Breyta greiðsluskilmálum** - Gjalddaga er breytt samkvæmt grunndagsetningu og greiðsluskilmálum.</span><span class="sxs-lookup"><span data-stu-id="6fa36-174">**Edit the payment terms** - The due date is changed, based on the base date and the payment terms.</span></span>
- <span data-ttu-id="6fa36-175">**Breyta skilmálum staðgreiðsluafsláttar** - Staðgreiðsluafsláttum er breytt samkvæmt grunndagsetningu og skilmálum staðgreiðsluafsláttar.</span><span class="sxs-lookup"><span data-stu-id="6fa36-175">**Edit the cash discount terms** - The cash discounts are changed, based on the base date and the cash discount terms.</span></span>

<span data-ttu-id="6fa36-176">Þegar þú hefur lokið við breytingar á greiðslustillingum skaltu velja **Loka** til að vista breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="6fa36-176">When you've finished editing the payment settings, select **Close** to save your changes.</span></span>