---
title: Bókunargerðir leigusamnings
description: Þetta efnisatriði lýsir bókunargerðunum sem eru notaðar fyrir eignaleigufærslur.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 1d76c7ea72346c432db04bbe7947dea0c2911ea8
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/13/2021
ms.locfileid: "5881133"
---
# <a name="lease-posting-types"></a><span data-ttu-id="b2ff8-103">Bókunargerðir leigusamnings</span><span class="sxs-lookup"><span data-stu-id="b2ff8-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2ff8-104">Þetta efnisatriði lýsir bókunargerðunum sem eru notaðar fyrir eignaleigufærslur.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="b2ff8-105">Leigja eign</span><span class="sxs-lookup"><span data-stu-id="b2ff8-105">Lease asset</span></span>

<span data-ttu-id="b2ff8-106">Lykillinn er tengdur við afnotaréttinn af eign.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="b2ff8-107">Þessi lykill er debetfærður þegar leigusamningur er skráður upphaflega samkvæmt nýjum bókhaldsreglum um leigusamninga, efnisatriði um skráningarkerfi reikningsskilastaðla 842 (ASC 842) og alþjóðlegan reikningsskilastaðal 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="b2ff8-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="b2ff8-108">Fyrir breyttan leigusamning kann þessi lykill að vera debet- eða kreditfærður, allt eftir því hvort breytingin hækkar eða lækkar leiguskuldbindinguna.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="b2ff8-109">**Dæmi um bókarfærslur:** Upphafleg viðurkenning</span><span class="sxs-lookup"><span data-stu-id="b2ff8-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="b2ff8-110">**Debet:** Leigueign XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="b2ff8-111">**Kredit:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="b2ff8-112">Leiguskuldbinding</span><span class="sxs-lookup"><span data-stu-id="b2ff8-112">Lease liability</span></span>

<span data-ttu-id="b2ff8-113">Lykilinn tengist leiguskuldbindingu sem verður til þegar veittur er afsláttur af greiðslum samkvæmt hinum nýju IFRS 16 og ASC 842-stöðlunum.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="b2ff8-114">Þessi lykill er kreditfærður þegar leigusamningurinn er viðurkenndur upphaflega samkvæmt nýja staðlinum.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="b2ff8-115">Hann er debetfærðu fyrir leigugreiðslum og kreditfærður fyrir uppsöfnun vaxta.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="b2ff8-116">**Dæmi um bókarfærslur:** Upphafleg viðurkenning</span><span class="sxs-lookup"><span data-stu-id="b2ff8-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="b2ff8-117">**Debet:** Leigueign XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="b2ff8-118">**Kredit:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="b2ff8-119">**Dæmi um bókarfærslur:** Uppsöfnun vaxta</span><span class="sxs-lookup"><span data-stu-id="b2ff8-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="b2ff8-120">**Debet:** Vaxtarkostnaður XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="b2ff8-121">**Kredit:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="b2ff8-122">**Dæmi um bókarfærslur:** Leigugreiðsla</span><span class="sxs-lookup"><span data-stu-id="b2ff8-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="b2ff8-123">**Debet:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="b2ff8-124">**Kredit:** Skuldastaða lánardrottins/leigugreiðsla XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="b2ff8-125">Skuldbinding skammtímaleigu</span><span class="sxs-lookup"><span data-stu-id="b2ff8-125">Short-term lease liability</span></span>

<span data-ttu-id="b2ff8-126">Lykilinn er tengdur við skuldbindingu skammtímaleigu þegar bókarfærsla endurflokkunar fyrir skuldbiningu skammtímaleigu er bókað.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="b2ff8-127">Lykillinn er kreditfærður fyrir skuldbindingu skammtímaleigu frá afskriftaráætlun á síðasta degi mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="b2ff8-128">Sama upphæð er hins vegar debetfærð á fyrsta degi næsta mánaðar.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="b2ff8-129">**Dæmi um bókarfærslur:** Endurflokkun skuldbindingar skammtímaleigu</span><span class="sxs-lookup"><span data-stu-id="b2ff8-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="b2ff8-130">**Debet:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="b2ff8-131">**Kredit:** Skuldbinding skammtímaleigu XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="b2ff8-132">**Debet:** Skuldbinding skammtímaleigu XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="b2ff8-133">**Kredit:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="b2ff8-134">Afskriftakostnaður</span><span class="sxs-lookup"><span data-stu-id="b2ff8-134">Depreciation expense</span></span>

<span data-ttu-id="b2ff8-135">Lykillinn er tengdur við kostnaðinn sem tengist afskriftum á afnotarétti af eign samkvæmt IFRS 16, ASC 842 og fjármögnunarleigusamningum samkvæmt IAS 17 og ASC 840.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="b2ff8-136">Þessi lykill er skuldfærður þegar afnotaréttur af eign er afskrifaður í hverjum mánuði.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="b2ff8-137">**Dæmi um færslubókarfærslur:** Afskriftauppsöfnun</span><span class="sxs-lookup"><span data-stu-id="b2ff8-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="b2ff8-138">**Debet:** Afskriftakostnaður XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="b2ff8-139">**Kredit:** Uppsafnaðar afskriftir XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="b2ff8-140">Hagnaður/tap vegna breytinga á leigusamningi</span><span class="sxs-lookup"><span data-stu-id="b2ff8-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="b2ff8-141">Lykillinn tengist öllum hagnaði eða tapi sem hlýst af breytingum á leigusamningi.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="b2ff8-142">Hagnaður gæti orðið vegna breytinga á leigusamningi ef breytingin fæli í sér lægri leiguskuldbindingu sem nemur upphæð sem er hærri en bókfært virði afnotaréttar af eign.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="b2ff8-143">Sem dæmi má nefna að leigusamningur er með núverandi bókfært virði leiguskuldbindingar upp á $150.000 og bókfært virði afnotaréttar af eign upp á $100.000.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="b2ff8-144">Leigusamningnum er breytt og þessar breytingar mynda nýtt núverandi virði á lágmarksleigugreiðslum (PVFMLP) upp á $40.000.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="b2ff8-145">Af þeim sökum verður leiguskuldbindingin debetfærð upp á $110.000 ($150.000 – $40.000).</span><span class="sxs-lookup"><span data-stu-id="b2ff8-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="b2ff8-146">Þar sem afnotaréttur af eign er aðeins $100.000 mun minnkun upp á $110.000 lækka eignina umfram 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="b2ff8-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="b2ff8-147">Þess vegna segir í leiðbeiningum um bókhald að eftirstöðvar eigi að vera bókaðar á hagnaðarlykil.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="b2ff8-148">Hér verður endanleg færsla í færslubók því debetfærð á leiguskuldbindingu upp á $110.000, kreditfærð á leigueignina upp á $100.000 og kreditfærð á hagnaðarlykilinn upp á $10.000.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="b2ff8-149">**Dæmi um bókarfærslur:** Breyting á leigusamningi</span><span class="sxs-lookup"><span data-stu-id="b2ff8-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="b2ff8-150">**Debet:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="b2ff8-151">**Kredit:** Leigueign XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="b2ff8-152">**Kredit:** Hagnaður XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="b2ff8-153">Uppsöfnuð afskrift</span><span class="sxs-lookup"><span data-stu-id="b2ff8-153">Accumulated depreciation</span></span>

<span data-ttu-id="b2ff8-154">Lykillinn er tengdur við andstæðan eignalykil fyrir afnotarétt af eign.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="b2ff8-155">Þessi lykill er kreditfærður þegar afskriftarkostnaður er bókaður.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="b2ff8-156">**Dæmi um færslubókarfærslur:** Afskriftauppsöfnun</span><span class="sxs-lookup"><span data-stu-id="b2ff8-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="b2ff8-157">**Debet:** Afskriftakostnaður XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="b2ff8-158">**Kredit:** Uppsafnaðar afskriftir XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="b2ff8-159">Breytileg greiðsla</span><span class="sxs-lookup"><span data-stu-id="b2ff8-159">Variable payment</span></span>

<span data-ttu-id="b2ff8-160">Lykillinn tengist breytilegum leigugreiðslum sem eru myndaðar af endurmatsferli vísitölu samkvæmt ASC 842-, ASC 840- og IAS 17-leigusamningum.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-160">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="b2ff8-161">Í greiðsluáætlun leigusamnings eru breytilegar greiðslur innifaldar í dálknum **Breytileg greiðsla**.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-161">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="b2ff8-162">Þessi lykill er skuldfærður þegar reikningur er stofnaður gegn greiðsluáætlunarlínu sem inniheldur breytilega greiðslu.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-162">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="b2ff8-163">**Dæmi um bókarfærslur:** Leigugreiðsla</span><span class="sxs-lookup"><span data-stu-id="b2ff8-163">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="b2ff8-164">**Debet:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-164">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="b2ff8-165">**Skuldfærsla:** Breytileg greiðsla XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-165">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="b2ff8-166">**Kredit:** Skuldastaða lánardrottins/leigugreiðsla XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-166">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="b2ff8-167">Frestaðar leigugreiðslur eignar (skuld)</span><span class="sxs-lookup"><span data-stu-id="b2ff8-167">Deferred rent asset (liability)</span></span>

<span data-ttu-id="b2ff8-168">Lykillinn er tengdur við frestaðar leigugreiðslur eignar eða skuldar sem er mynduð af frestuðum leigugreiðslum leigusamnings.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-168">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="b2ff8-169">Þessi lykill er debetfærður þegar reikningur er bókaður á móti frestuðum leigugreiðslum leigusamnings ef upphæð leigugreiðslu er hærri en línulegur leigukostnaður tímabilsins.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-169">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="b2ff8-170">Hann er kreditfærður ef leigugreiðslan er lægri en línulegur leigukostnaður tímabilsins.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-170">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="b2ff8-171">**Dæmi um bókarfærslur:** Leigugreiðsla (frestaðar leigugreiðslur leigusamnings)</span><span class="sxs-lookup"><span data-stu-id="b2ff8-171">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="b2ff8-172">**Debet:** Leigukostnaður XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-172">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="b2ff8-173">**Kredit:** Skuldbinding vegna frestaðra leigugreiðslna XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-173">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="b2ff8-174">**Kredit:** Skuldastaða lánardrottins/leigugreiðsla XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-174">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="b2ff8-175">Leigukostnaður</span><span class="sxs-lookup"><span data-stu-id="b2ff8-175">Lease expense</span></span>

<span data-ttu-id="b2ff8-176">Lykillinn tengist leigukostnaðinum ef leigan er flokkuð sem frestaðar leigugreiðslur leigusamnings.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-176">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="b2ff8-177">Þessi lykill er debetfærður þegar reikningur er bókaður á móti frestuðum leigugreiðslum leigusamnings.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-177">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="b2ff8-178">**Dæmi um bókarfærslur:** Leigugreiðsla (frestaðar leigugreiðslur leigusamnings)</span><span class="sxs-lookup"><span data-stu-id="b2ff8-178">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="b2ff8-179">**Debet:** Leigukostnaður XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-179">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="b2ff8-180">**Kredit:** Skuldbinding vegna frestaðra leigugreiðslna XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-180">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="b2ff8-181">**Kredit:** Skuldastaða lánardrottins/leigugreiðsla XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-181">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="b2ff8-182">Kostnaður virðisrýrnunar</span><span class="sxs-lookup"><span data-stu-id="b2ff8-182">Impairment expense</span></span>

<span data-ttu-id="b2ff8-183">Lykillinn er mótbókaður þegar leigusamningur skerðist.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-183">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="b2ff8-184">Þessi lykill er debetfærður á meðan lykill afnotaréttar af eign er kreditfærður beint.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-184">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="b2ff8-185">**Dæmi um bókarfærslur:** Leigugreiðsla</span><span class="sxs-lookup"><span data-stu-id="b2ff8-185">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="b2ff8-186">**Debet:** Kostnaður virðisrýrnunar XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-186">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="b2ff8-187">**Kredit:** Afnotaréttur af eign XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-187">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="b2ff8-188">Leigugreiðsla</span><span class="sxs-lookup"><span data-stu-id="b2ff8-188">Lease payment</span></span>

<span data-ttu-id="b2ff8-189">Lykillinn er mótbókaður ef slökkt er á færibreytunni **Greiða lánardrottni**.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-189">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="b2ff8-190">Lykillinn er kreditfærður í stað lánardrottnaskuldar ef slökkt er á færibreytunni.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-190">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="b2ff8-191">**Dæmi um bókarfærslur:** Leigugreiðsla</span><span class="sxs-lookup"><span data-stu-id="b2ff8-191">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="b2ff8-192">**Debet:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-192">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="b2ff8-193">**Kredit:** Leigugreiðsla XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-193">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="b2ff8-194">Bókun kostnaðargerðar</span><span class="sxs-lookup"><span data-stu-id="b2ff8-194">Expense type postings</span></span>

<span data-ttu-id="b2ff8-195">Lykillinn sem er valinn fyrir hverja kostnaðargerð er debetfærður þegar greiðsla fyrir þá kostnaðargerð er mynduð.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-195">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="b2ff8-196">Til dæmis er lykillinn sem er tilgreindur fyrir kostnaðargerðina **Trygging** debetfærður í hvert sinn sem reikningur eða greiðslubókarfærsla er stofnuð úr rekstrarkostnaðaráætlun vegna tryggingakostnaðar.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-196">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="b2ff8-197">**Dæmi um bókarfærslur:** Tryggingagreiðsla</span><span class="sxs-lookup"><span data-stu-id="b2ff8-197">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="b2ff8-198">**Debet:** Tryggingakostnaðarlykill XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-198">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="b2ff8-199">**Kredit:** Mótlykill XXX</span><span class="sxs-lookup"><span data-stu-id="b2ff8-199">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="b2ff8-200">Mótlykill er valinn á leigustigi á línunum fyrir greiðsluáætlun rekstrarkostnaðar.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-200">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="b2ff8-201">Þessi mótlykill getur tengst lánardrottni eða með fjárhagslykli.</span><span class="sxs-lookup"><span data-stu-id="b2ff8-201">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
