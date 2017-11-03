---
title: Losunarreglur
description: "Þetta efnisatriði veitir upplýsingar um losunarreglur og mismunandi valkosti fyrir skýrslugerð um losanir."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 818572a8d1f790aaa7c6e4befc1d2222a1c35c50
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="elimination-rules"></a><span data-ttu-id="0b7f1-103">Losunarreglur</span><span class="sxs-lookup"><span data-stu-id="0b7f1-103">Elimination rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0b7f1-104">Þetta efnisatriði veitir upplýsingar um losunarreglur og mismunandi valkosti fyrir skýrslugerð um losanir.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-104">This topic provides information about elimination rules and the various options for reporting about eliminations.</span></span>

<span data-ttu-id="0b7f1-105">Útilokunarfærslna er krafist þegar yfirlögaðili stundar viðskipti við einn eða fleiri undirlögaðila og notar sameinaðar fjárhagsskýrslur.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-105">Elimination transactions are required when a parent legal entity does business with one or more subsidiary legal entities and uses consolidated financial reporting.</span></span> <span data-ttu-id="0b7f1-106">Samstæðureikningsskil verða að innihalda eingöngu færslur sem verða á milli sameinaðs fyrirtækis og annarra eininga utan þess fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-106">Consolidated financial statements must include only transactions that occur between the consolidated organization and other entities outside that organizations.</span></span> <span data-ttu-id="0b7f1-107">Þess vegna verður að fjarlægja færslur á milli lögaðila sem eru hluti af sömu samstæðu eða sleppa þeim úr fjárhag svo að þær birtist ekki í fjárhagsskýrslum.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-107">Therefore, transactions between legal entities that are part of the same organization must be removed, or eliminated, from the general ledger, so they don't appear on financial reports.</span></span> <span data-ttu-id="0b7f1-108">Það eru margar leiðir til að tilkynna um losun:</span><span class="sxs-lookup"><span data-stu-id="0b7f1-108">There are multiple ways to report about eliminations:</span></span>

-   <span data-ttu-id="0b7f1-109">Hægt er að stofna losunarreglu og keyra á samstæðu- eða losunarfyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-109">An elimination rule can be created and processed in a consolidation or elimination company.</span></span>
-   <span data-ttu-id="0b7f1-110">Fjárhagsskýrslu má nota til að sýna útilokunarlykla og víddir á tiltekinni röð eða dálki.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-110">Financial reporting can be used to show the eliminations accounts and dimensions on a specific row or column.</span></span>
-   <span data-ttu-id="0b7f1-111">Sérstakan lögaðila má nota til að bóka færslur handvirkt til að rekja losun.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-111">A separate legal entity can be used to post manual transaction entries to track eliminations.</span></span>

<span data-ttu-id="0b7f1-112">Þetta viðfangsefni leggur áherslu á losunarreglur sem eru myndaðar í samstæðu- eða losunarfyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-112">This topic focuses on elimination rules that are processed in a consolidation or elimination company.</span></span> <span data-ttu-id="0b7f1-113">Þú getur sett upp losunarreglur til að búa til losunarfærslur í lögaðila sem er tilgreindur sem ákvörðunarlögaðili fyrir losun.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-113">You can set up elimination rules to create elimination transactions in a legal entity that is specified as the destination legal entity for eliminations.</span></span> <span data-ttu-id="0b7f1-114">Viðtökulögaðilann er einnig þekktur sem losunarlögaðili.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-114">This destination legal entity is known as the elimination legal entity.</span></span> <span data-ttu-id="0b7f1-115">Hægt er að mynda útilokunarbækur annaðhvort í samstæðuferlinu eða með því að nota tillögu útilokunarbókar.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-115">Elimination journals can be generated either during the consolidation process or by using an elimination journal proposal.</span></span> <span data-ttu-id="0b7f1-116">Áður en losunarreglur eru settar upp er gott að þekkja eftirfarandi hugtök:</span><span class="sxs-lookup"><span data-stu-id="0b7f1-116">Before you set up elimination rules, you should become familiar with the following terms:</span></span>

-   <span data-ttu-id="0b7f1-117">**Upprunalegur lögaðili** - Lögaðili þar sem upphæðir sem á að eyða voru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-117">**Source legal entity** – The legal entity where the amounts that are being eliminated were posted.</span></span>
-   <span data-ttu-id="0b7f1-118">**Viðtökulögaðili** – Lögaðili þar sem losunarreglur eru bókaðar.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-118">**Destination legal entity** – The legal entity where elimination rules are posted.</span></span>
-   <span data-ttu-id="0b7f1-119">**Losunarlögaðili** – Lögaðili sem er tilgreindur sem viðtökulögaðili fyrir losun.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-119">**Elimination legal entity** – The legal entity that is specified as the destination legal entity for eliminations.</span></span>
-   <span data-ttu-id="0b7f1-120">**Sameinaður lögaðili** – Lögaðili sem er stofnaður til að skrá fjárhagsniðurstöður fyrir hóp lögaðila.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-120">**Consolidated legal entity** – The legal entity that is created to report financial results for a group of legal entities.</span></span> <span data-ttu-id="0b7f1-121">Fjárhagsgögnin frá lögaðilar eru tekin saman inn í þennan lögaðila og fjárhagsskýrsla er stofnuð með sameinuðu gögnunum.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-121">The financial data from the legal entities is consolidated into this legal entity, and then a financial report is created by using the combined data.</span></span>

<span data-ttu-id="0b7f1-122">Eftirfarandi tafla sýnir gerðir færslna gæti þurft að losa.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-122">The following table shows the types of transactions that might have to be eliminated.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0b7f1-123">Færslugerð</span><span class="sxs-lookup"><span data-stu-id="0b7f1-123">Transaction type</span></span></th>
<th><span data-ttu-id="0b7f1-124">Dæmi</span><span class="sxs-lookup"><span data-stu-id="0b7f1-124">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0b7f1-125">Sölupöntunarfærsla og reikningsfærsla (miðstýrð vinnsla)</span><span class="sxs-lookup"><span data-stu-id="0b7f1-125">Sales order entry and invoicing (centralized processing)</span></span></td>
<td><span data-ttu-id="0b7f1-126">Að selja vöru viðskiptavina fyrir hönd annars lögaðila í þínu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-126">You sell a product to a customer on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b7f1-127">Sölupöntunarfærsla (innan samstæðu/innan fyrirtækis) og reikningsgerð</span><span class="sxs-lookup"><span data-stu-id="0b7f1-127">Sales order entry (intercompany/intracompany) and invoicing</span></span></td>
<td><span data-ttu-id="0b7f1-128">Að selja afurðir á milli lögaðila í þínu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-128">You sell products between legal entities in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b7f1-129">Innkaupapantanir (miðstýrð vinnsla)</span><span class="sxs-lookup"><span data-stu-id="0b7f1-129">Purchase orders (centralized processing)</span></span></td>
<td><span data-ttu-id="0b7f1-130">Þú kaupir birgðir, þjónustu, eignir, og aðrar vörur frá lánardrottni fyrir hönd annars lögaðila í þínu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-130">You purchase inventory, supplies, services, fixed assets, and other products from a vendor on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b7f1-131">Birgðastjórnun (innan samstæðu/innan fyrirtækis)</span><span class="sxs-lookup"><span data-stu-id="0b7f1-131">Inventory management (intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="0b7f1-132">Er að flytja einum lögaðila birgðir í eignir annars lögaðila í þínu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-132">You transfer one legal entity’s inventory to the fixed assets of another legal entity in your organization.</span></span></li>
<li><span data-ttu-id="0b7f1-133">Er að flytja birgðir einum lögaðila á aðra lögaðila í þínu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-133">You transfer one legal entity’s inventory to the inventory of another legal entity in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b7f1-134">Birgðarakning í flutningum</span><span class="sxs-lookup"><span data-stu-id="0b7f1-134">In-transit inventory tracking</span></span></td>
<td><span data-ttu-id="0b7f1-135">Flytja vörur milli vöruhúsa sama lögaðila, en milli mismunandi staða landfræðilega.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-135">You transfer items between warehouses in the same legal entity, but across different geographical sites.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b7f1-136">Miðstýrð reikningavinnsla lánadrottna</span><span class="sxs-lookup"><span data-stu-id="0b7f1-136">Accounts payable centralized invoice processing</span></span></td>
<td><span data-ttu-id="0b7f1-137">Skrá reikning fyrir hönd annars lögaðila í þínu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-137">You record an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b7f1-138">Miðstýrð greiðsluvinnsla lánadrottna</span><span class="sxs-lookup"><span data-stu-id="0b7f1-138">Accounts payable centralized payment processing</span></span></td>
<td><span data-ttu-id="0b7f1-139">Greiða reikning fyrir hönd annars lögaðila í þínu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-139">You pay an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b7f1-140">Reiðufjárstjórnun og fjárstýring (miðstýrð vinnsla)</span><span class="sxs-lookup"><span data-stu-id="0b7f1-140">Cash management and treasury (centralized processing)</span></span></td>
<td><ul>
<li><span data-ttu-id="0b7f1-141">Þú vinnur skattagreiðslur, skattaendurgreiðslur, vaxtagjöld, lán, fyrirgramgreiðslur, arðgreiðslur, og fyrirframgreiddar afnotagreiðslur eða sölulaun.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-141">You process tax payments, tax refunds, interest charges, loans, advances, dividend payments, and prepaid royalties or commissions.</span></span></li>
<li><span data-ttu-id="0b7f1-142">Borga kostnað fyrir hönd annars lögaðila í þínu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-142">You pay an expense on behalf of another legal entity in your organization.</span></span> <span data-ttu-id="0b7f1-143">Reikningurinn er færður inn í bækur á ákvörðunarstað lögaðila og hægt að jafna á milli lögaðila.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-143">The invoice is entered in the destination legal entity’s books, and you must cross-settle between legal entities.</span></span> <span data-ttu-id="0b7f1-144">Til dæmis, einn lögaðila greiðir kostnaðarskýrslu starfsmanns í annan lögaðila.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-144">For example, one legal entity pays the expense report of an employee in another legal entity.</span></span> <span data-ttu-id="0b7f1-145">Í þessu tilfelli hefur kostnaðarskýrsla starfsmanns útgjöld sem tengjast öðrum lögaðila.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-145">In this case, the employee’s expense report has expenses that are related to another legal entity.</span></span></li>
<li><span data-ttu-id="0b7f1-146">Að færa reiðufé frá einn lögaðila í annað í þínu fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-146">You transfer cash from one legal entity to another in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b7f1-147">Viðskiptavinir (miðstýrð vinnsla)</span><span class="sxs-lookup"><span data-stu-id="0b7f1-147">Accounts receivable (centralized processing)</span></span></td>
<td><span data-ttu-id="0b7f1-148">Þú færð reiðufé fyrir reikning viðskiptavinar annars lögaðila, og þú leggur þá ávísun inn á bankareikning þess lögaðila.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-148">You receive cash for another legal entity’s customer invoice, and you deposit the check into that legal entity’s bank account.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b7f1-149">Laun (miðstýrð vinnsla, innan samstæðu/innan fyrirtækis)</span><span class="sxs-lookup"><span data-stu-id="0b7f1-149">Payroll (centralized processing, intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="0b7f1-150">Greidd laun annan lögaðila.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-150">You pay another legal entity’s payroll.</span></span> <span data-ttu-id="0b7f1-151">Til dæmis greiðir lögaðili eigin laun fyrir starfsmenn sína en rukkar fyrir þá vinnu sem starfsmaður vann fyrir annan lögaðila þann mánuðinn.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-151">For example, a legal entity pays its own payroll for its employees but charges back work that an employee did for another legal entity during that pay run.</span></span> <span data-ttu-id="0b7f1-152">Eða, starfsmaður ynni hálfan vinnudag fyrir lögaðilann A og hálfan vinnudag fyrir lögaðilann B og fríðindin næðu yfir öll laun.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-152">Or, an employee worked half-time for legal entity A and half-time for legal entity B, and the benefits are across all pay.</span></span> <span data-ttu-id="0b7f1-153">Í þessum tilvikum innihalda laun starfsmanns laun frá báðum lögaðilum.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-153">In these cases, the employee’s pay includes pay from both legal entities.</span></span> <span data-ttu-id="0b7f1-154">Ekki aðeins laun eru bókuð, heldur einnig skattar, fríðindi, frádráttur og áfallin gjöld fyrir laun.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-154">Not only are the salaries posted, but taxes, benefits, deductions, and accruals for salaries are also posted.</span></span></li>
<li><span data-ttu-id="0b7f1-155">Þú flytur laun frá einni deild í annað svið eða annað.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-155">You transfer labor from one department or division to another.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0b7f1-156">Eignir (innan samstæðu/innan fyrirtækis)</span><span class="sxs-lookup"><span data-stu-id="0b7f1-156">Fixed assets (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="0b7f1-157">Flytja eignir í eignir eða birgðir annars lögaðila.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-157">You transfer fixed assets to another legal entity’s fixed assets or inventory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0b7f1-158">Úthlutanir (innan samstæðu/innan fyrirtækis)</span><span class="sxs-lookup"><span data-stu-id="0b7f1-158">Allocations (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="0b7f1-159">Er að vinna úthlutanir fyrirtækja.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-159">You process corporate allocations.</span></span> <span data-ttu-id="0b7f1-160">Úthlutanir sem eru aðgerðir fyrir hvern úthlutaðan lykil, óháð upprunalegri kerfiseiningu.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-160">Allocations are activities to any account that is allocated, regardless of the originating module.</span></span></td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="0b7f1-161">Dæmi</span><span class="sxs-lookup"><span data-stu-id="0b7f1-161">Example</span></span>
<span data-ttu-id="0b7f1-162">Við lögaðila, lögaðila A, selur búnað til annars lögaðila í þínu fyrirtæki B. lögaðila Eftirfarandi dæmi sýnir hvernig færslur á milli tveggja lögaðila gæti verið að losa:</span><span class="sxs-lookup"><span data-stu-id="0b7f1-162">Your legal entity, legal entity A, sells widgets to another legal entity in your organization, legal entity B. The following example shows how transactions that occur between the two legal entities might have to be eliminated:</span></span>

-   <span data-ttu-id="0b7f1-163">Lögaðili A selur búnaður sem kostar 10,00 til lögaðila B fyrir 10.00.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-163">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00.</span></span>
-   <span data-ttu-id="0b7f1-164">Lögaðili A selur búnaður sem kostar 10,00 til lögaðila B fyrir 10,00, auk 2,00 í raunsendingarkostnað.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-164">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00, plus 2.00 in actual shipping costs.</span></span>
-   <span data-ttu-id="0b7f1-165">Lögaðili A selur búnaður sem kostar 10,00 til lögaðila B fyrir 15,00 og viðurkennir framlegð á sölu.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-165">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes a margin on the sale.</span></span>
-   <span data-ttu-id="0b7f1-166">Lögaðili A selur búnað sem kostar 10,00 til lögaðila B fyrir 15,00 og viðurkennir helming framlegðar á sölu.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-166">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes half the margin on the sale.</span></span> <span data-ttu-id="0b7f1-167">Lögaðili B viðurkennir hinn helming framlegðar í sölu.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-167">Legal entity B recognizes the other half of the margin on the sale.</span></span> <span data-ttu-id="0b7f1-168">Þess vegna er tekjunum skipt.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-168">Therefore, the revenue is split.</span></span> <span data-ttu-id="0b7f1-169">Skiptar tekjur veitir hvata til að panta frá öðrum lögaðila í fyrirtækinu í stað þess að panta frá utanaðkomandi fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-169">Split revenue provides an incentive to order from another legal entity in the organization instead of an external organization.</span></span>

<span data-ttu-id="0b7f1-170">Allar þessar færslur stofna færslur innan samstæðu sem verða bókaðar á vostro- og nostro-lykla.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-170">All these transactions create intercompany transactions that are posted to due-to and due-from accounts.</span></span> <span data-ttu-id="0b7f1-171">Þar að auki gætu þessar færslur innihaldið upphæðir álagningar eða afsláttar þegar upphæð sölu innan fyrirtækis er ekki jöfn kostnaði varanna sem verið er að selja.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-171">In addition, these transactions might include markup and markdown amounts when the amount of the intercompany sale doesn't equal the cost of the goods that were sold.</span></span>

## <a name="set-up-elimination-rules"></a><span data-ttu-id="0b7f1-172">Setja upp losunarreglur</span><span class="sxs-lookup"><span data-stu-id="0b7f1-172">Set up elimination rules</span></span>
<span data-ttu-id="0b7f1-173">Þegar losunarreglur eru settar upp í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, er mælt með því að búin sé til fjárhagsvídd sérstaklega fyrir losun.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-173">When setting up elimination rules in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, we recommend that you create a financial dimension specifically for elimination purposes.</span></span> <span data-ttu-id="0b7f1-174">Flestir viðskiptavinir kalla hana Viðskiptamaður eða eitthvað svipað.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-174">Most customers name it Trading Partner or something similar.</span></span> <span data-ttu-id="0b7f1-175">Ef þú ákveður að nota ekki fjárhagsvídd skaltu gæta þess að hafa aðallykla sem eru sértækir fyrir viðskipti innan samstæðu.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-175">If you decide not to use a financial dimension, then be sure to have main accounts that are specific for intercompany transactions only.</span></span> 

<span data-ttu-id="0b7f1-176">Uppsetningu fyrir losun er að finna á svæðinu Setja upp í einingunni Samstæður.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-176">The setup for eliminations is found in the Setup area of the Consolidations module.</span></span> <span data-ttu-id="0b7f1-177">Eftir að þú slærð inn lýsingu fyrir regluna þarftu að velja fyrirtækið sem losunarbókin bókar í.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-177">After you enter a description for the rule, you must pick the company that the elimination journal will post to.</span></span> <span data-ttu-id="0b7f1-178">Þetta ætti að vera fyrirtæki sem hefur **Nota fyrir losunarferli fjárhags** valið í uppsetningu lögaðila.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-178">This should be a company that has **Use for financial elimination process** selected in the Legal entity setup.</span></span> 

<span data-ttu-id="0b7f1-179">Hægt er að velja dagsetninguna þegar losunarregla tekur gildi og þegar hún rennur út, ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-179">You can set a date on which the elimination rule becomes effective and when it is expired, if needed.</span></span> <span data-ttu-id="0b7f1-180">Stilla verður **Virk** á **Já** ef þú vilt að hún verði í boði í losunartillöguferlinu.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-180">You must set **Active** to **Yes** if you want it to be available in the elimination proposal process.</span></span> <span data-ttu-id="0b7f1-181">Veldu heiti færslubókar sem er með færslubókargerðina **Losun**.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-181">Select a journal name that has a type of **Elimination**.</span></span>

<span data-ttu-id="0b7f1-182">Eftir að þú hefur skilgreint grunnatriði er hægt að skilgreina raunverulegar úrvinnslureglur með því að smella á **Línur**.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-182">After you have defined the basics, you can define the actual processing rules by clicking **Lines**.</span></span> <span data-ttu-id="0b7f1-183">Tveir kostir eru í boði fyrir losun, að losa upphæð nettóbreytingar eða skilgreina fasta upphæð.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-183">There are two options for eliminations, eliminating the net change amount or defining a fixed amount.</span></span> 

<span data-ttu-id="0b7f1-184">Veldu upprunareikning.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-184">Select your source account.</span></span> <span data-ttu-id="0b7f1-185">Hægt er að nota stjörnu (\*) sem algildistákn.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-185">You can use an asterisk (\*) as a wild card.</span></span> <span data-ttu-id="0b7f1-186">Til dæmis myndi 1\* velja alla lykla sem byrja á 1 sem uppruna gagna fyrir úthlutunina.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-186">For example, 1\* would select all accounts that start with a 1 as a source of data for the allocation.</span></span> 

<span data-ttu-id="0b7f1-187">Þegar þú hefur valið upprunareikninga ákvarðar **Reikningslýsing** reikning viðtökufyrirtækis sem er notaður.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-187">After you have selected your source accounts, the **Account specification** determines the account from the destination company that is used.</span></span> <span data-ttu-id="0b7f1-188">Veldu **Uppruni** ef þú vilt nota sama aðalreikning og er skilgreindur í **Upprunareikningur**.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-188">Select **Source** if you want to use the same main account defined in the **Source** account.</span></span> <span data-ttu-id="0b7f1-189">Ef þú velur **Skilgreint af notanda** þarftu að tilgreina viðtökureikning.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-189">If you select **User defined**, then you must specify a destination account.</span></span> 

<span data-ttu-id="0b7f1-190">Víddarskilgreiningin virkar með sama hætti.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-190">The dimension specification acts in the same way.</span></span> <span data-ttu-id="0b7f1-191">Ef þú velur **Uppruni** notar það sömu víddir í viðtökufyrirtækinu og í upprunafyrirtækinu.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-191">If you select **Source**, it will use the same dimensions in the destination company as the source company.</span></span> <span data-ttu-id="0b7f1-192">Ef þú velur **Skilgreint af notanda** þarftu að tilgreina víddir í viðtökufyrirtæki með því að smella á valmyndaratriðið **Víddir viðtökustaðar**.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-192">If you select **User defined**, you will need to specify the dimensions in the destination company by clicking the **Destination dimensions** menu item.</span></span> 

<span data-ttu-id="0b7f1-193">Veldu upprunavíddir og fjárhagsvíddir og gildi sem eru notuð sem uppruni fyrir losunina.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-193">Select source dimensions and the financial dimensions and values that are used as a source of the elimination.</span></span>

## <a name="process-elimination-transactions"></a><span data-ttu-id="0b7f1-194">Vinna Losunarfærslur</span><span class="sxs-lookup"><span data-stu-id="0b7f1-194">Process elimination transactions</span></span>
<span data-ttu-id="0b7f1-195">Tvær leiðir eru til að vinna losunarfærslur, meðan á sameiningu á netinu stendur eða með því að stofna losunarbók og keyra losunartillöguferlið.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-195">There are two ways to process elimination transactions, during the consolidate online process or by creating an elimination journal and running the elimination proposal process.</span></span> <span data-ttu-id="0b7f1-196">Í þessum kafla er áherslan á stofnun færslubókar og að keyra losunarferlið.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-196">This section focuses on creating the journal and running the elimination process.</span></span> 

<span data-ttu-id="0b7f1-197">Í fyrirtæki sem er skilgreint sem losunarfyrirtæki skal velja **Losunarbók** í einingunni Samstæður.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-197">In a company defined as an elimination company, select **Elimination journal** in the Consolidations module.</span></span> <span data-ttu-id="0b7f1-198">Þegar þú hefur valið heiti færslubókar smellirðu á **Línur**.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-198">After you have selected the journal name, click **Lines**.</span></span> <span data-ttu-id="0b7f1-199">Þú getur keyrt tillöguna með því að velja valmyndina **Tillögur** og velja **Losunartillaga**.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-199">You can run the proposal by selecting the **Proposals** menu and then selecting **Elimination proposal**.</span></span>

<span data-ttu-id="0b7f1-200">Veldu fyrirtækið sem er uppruni sameinuðu gagnanna og veldu svo regluna sem þú vilt vinna með.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-200">Select the company that is the source of the consolidated data, and then choose the rule that you want to process.</span></span> <span data-ttu-id="0b7f1-201">Færðu inn upphafsdag til að hefja leit að losunarupphæðum, og lokadag til að ljúka leit að losunarupphæðum.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-201">Enter a start date to begin the search for elimination amounts, and an end date to end the search date for elimination amounts.</span></span> <span data-ttu-id="0b7f1-202">Í reitnum **Bókunardagsetning fjárhags** er dagsetningin sem er notuð til að bóka færslubókina í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-202">The **GL posting date** field is the date used for posting the journal to the general ledger.</span></span> <span data-ttu-id="0b7f1-203">Þegar smellt er á **Í lagi** er hægt að endurskoða upphæðirnar og bóka færslubókina.</span><span class="sxs-lookup"><span data-stu-id="0b7f1-203">After you click **OK**, you can review the amounts and post the journal.</span></span>




