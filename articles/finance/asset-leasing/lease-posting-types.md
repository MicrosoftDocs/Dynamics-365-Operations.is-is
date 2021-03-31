---
title: Bókunargerðir leigusamnings
description: Þetta efnisatriði lýsir bókunargerðunum sem eru notaðar fyrir eignaleigufærslur.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9b7d8c545c1addaa570d54855bbad6c576783007
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5229503"
---
# <a name="lease-posting-types"></a><span data-ttu-id="7e238-103">Bókunargerðir leigusamnings</span><span class="sxs-lookup"><span data-stu-id="7e238-103">Lease posting types</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7e238-104">Þetta efnisatriði lýsir bókunargerðunum sem eru notaðar fyrir eignaleigufærslur.</span><span class="sxs-lookup"><span data-stu-id="7e238-104">This topic describes the posting types that are used for asset leasing transactions.</span></span>

## <a name="lease-asset"></a><span data-ttu-id="7e238-105">Leigja eign</span><span class="sxs-lookup"><span data-stu-id="7e238-105">Lease asset</span></span>

<span data-ttu-id="7e238-106">Lykillinn er tengdur við afnotaréttinn af eign.</span><span class="sxs-lookup"><span data-stu-id="7e238-106">The account is associated with the right-of-use (ROU) asset.</span></span> <span data-ttu-id="7e238-107">Þessi lykill er debetfærður þegar leigusamningur er skráður upphaflega samkvæmt nýjum bókhaldsreglum um leigusamninga, efnisatriði um skráningarkerfi reikningsskilastaðla 842 (ASC 842) og alþjóðlegan reikningsskilastaðal 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="7e238-107">This account is debited when a lease is initially recognized under the new lease accounting standards, Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16).</span></span> <span data-ttu-id="7e238-108">Fyrir breyttan leigusamning kann þessi lykill að vera debet- eða kreditfærður, allt eftir því hvort breytingin hækkar eða lækkar leiguskuldbindinguna.</span><span class="sxs-lookup"><span data-stu-id="7e238-108">For a modified lease, this account might be either debited or credited, depending on whether the modification increases or decreases the lease liability.</span></span>

<span data-ttu-id="7e238-109">**Dæmi um bókarfærslur:** Upphafleg viðurkenning</span><span class="sxs-lookup"><span data-stu-id="7e238-109">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="7e238-110">**Debet:** Leigueign XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-110">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="7e238-111">**Kredit:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-111">**Credit:** Lease liability XXX</span></span>

## <a name="lease-liability"></a><span data-ttu-id="7e238-112">Leiguskuldbinding</span><span class="sxs-lookup"><span data-stu-id="7e238-112">Lease liability</span></span>

<span data-ttu-id="7e238-113">Lykilinn tengist leiguskuldbindingu sem verður til þegar veittur er afsláttur af greiðslum samkvæmt hinum nýju IFRS 16 og ASC 842-stöðlunum.</span><span class="sxs-lookup"><span data-stu-id="7e238-113">The account is associated with the lease liability that occurs when payments are discounted under the new IFRS 16 and ASC 842 standards.</span></span> <span data-ttu-id="7e238-114">Þessi lykill er kreditfærður þegar leigusamningurinn er viðurkenndur upphaflega samkvæmt nýja staðlinum.</span><span class="sxs-lookup"><span data-stu-id="7e238-114">This account is credited when a lease is initially recognized under the new standards.</span></span> <span data-ttu-id="7e238-115">Hann er debetfærðu fyrir leigugreiðslum og kreditfærður fyrir uppsöfnun vaxta.</span><span class="sxs-lookup"><span data-stu-id="7e238-115">It's debited for lease payments and credited for interest accruals.</span></span>

<span data-ttu-id="7e238-116">**Dæmi um bókarfærslur:** Upphafleg viðurkenning</span><span class="sxs-lookup"><span data-stu-id="7e238-116">**Example journal entries:** Initial recognition</span></span><br>
<span data-ttu-id="7e238-117">**Debet:** Leigueign XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-117">**Debit:** Lease asset XXX</span></span><br>
<span data-ttu-id="7e238-118">**Kredit:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-118">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="7e238-119">**Dæmi um bókarfærslur:** Uppsöfnun vaxta</span><span class="sxs-lookup"><span data-stu-id="7e238-119">**Example journal entries:** Interest accrual</span></span><br>
<span data-ttu-id="7e238-120">**Debet:** Vaxtarkostnaður XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-120">**Debit:** Interest expense XXX</span></span><br>
<span data-ttu-id="7e238-121">**Kredit:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-121">**Credit:** Lease liability XXX</span></span>

<span data-ttu-id="7e238-122">**Dæmi um bókarfærslur:** Leigugreiðsla</span><span class="sxs-lookup"><span data-stu-id="7e238-122">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="7e238-123">**Debet:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-123">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="7e238-124">**Kredit:** Skuldastaða lánardrottins/leigugreiðsla XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-124">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="short-term-lease-liability"></a><span data-ttu-id="7e238-125">Skuldbinding skammtímaleigu</span><span class="sxs-lookup"><span data-stu-id="7e238-125">Short-term lease liability</span></span>

<span data-ttu-id="7e238-126">Lykilinn er tengdur við skuldbindingu skammtímaleigu þegar bókarfærsla endurflokkunar fyrir skuldbiningu skammtímaleigu er bókað.</span><span class="sxs-lookup"><span data-stu-id="7e238-126">The account is associated with the short-term lease liability when the short-term lease liability reclass journal entry is posted.</span></span> <span data-ttu-id="7e238-127">Lykillinn er kreditfærður fyrir skuldbindingu skammtímaleigu frá afskriftaráætlun á síðasta degi mánaðarins.</span><span class="sxs-lookup"><span data-stu-id="7e238-127">This account is credited for the short-term liability from the amortization schedule on the last day of the month.</span></span> <span data-ttu-id="7e238-128">Sama upphæð er hins vegar debetfærð á fyrsta degi næsta mánaðar.</span><span class="sxs-lookup"><span data-stu-id="7e238-128">However, the same amount is debited on the first day of the next month.</span></span>

<span data-ttu-id="7e238-129">**Dæmi um bókarfærslur:** Endurflokkun skuldbindingar skammtímaleigu</span><span class="sxs-lookup"><span data-stu-id="7e238-129">**Example journal entries:** Short-term lease liability reclass</span></span><br>
<span data-ttu-id="7e238-130">**Debet:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-130">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="7e238-131">**Kredit:** Skuldbinding skammtímaleigu XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-131">**Credit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="7e238-132">**Debet:** Skuldbinding skammtímaleigu XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-132">**Debit:** Short-term lease liability XXX</span></span><br>
<span data-ttu-id="7e238-133">**Kredit:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-133">**Credit:** Lease liability XXX</span></span>

## <a name="depreciation-expense"></a><span data-ttu-id="7e238-134">Afskriftakostnaður</span><span class="sxs-lookup"><span data-stu-id="7e238-134">Depreciation expense</span></span>

<span data-ttu-id="7e238-135">Lykillinn er tengdur við kostnaðinn sem tengist afskriftum á afnotarétti af eign samkvæmt IFRS 16, ASC 842 og fjármögnunarleigusamningum samkvæmt IAS 17 og ASC 840.</span><span class="sxs-lookup"><span data-stu-id="7e238-135">The account is associated with the expense that is related to the depreciation of the ROU asset under IFRS 16, ASC 842, and finance leases under IAS 17 and ASC 840.</span></span> <span data-ttu-id="7e238-136">Þessi lykill er skuldfærður þegar afnotaréttur af eign er afskrifaður í hverjum mánuði.</span><span class="sxs-lookup"><span data-stu-id="7e238-136">This account is debited when an ROU asset is depreciated each month.</span></span>

<span data-ttu-id="7e238-137">**Dæmi um færslubókarfærslur:** Afskriftauppsöfnun</span><span class="sxs-lookup"><span data-stu-id="7e238-137">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="7e238-138">**Debet:** Afskriftakostnaður XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-138">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="7e238-139">**Kredit:** Uppsafnaðar afskriftir XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-139">**Credit:** Accumulated Depreciation XXX</span></span>

## <a name="gainloss-on-lease-modification"></a><span data-ttu-id="7e238-140">Hagnaður/tap vegna breytinga á leigusamningi</span><span class="sxs-lookup"><span data-stu-id="7e238-140">Gain/loss on lease modification</span></span>

<span data-ttu-id="7e238-141">Lykillinn tengist öllum hagnaði eða tapi sem hlýst af breytingum á leigusamningi.</span><span class="sxs-lookup"><span data-stu-id="7e238-141">The account is associated with any gains or losses that arise from lease modifications.</span></span> <span data-ttu-id="7e238-142">Hagnaður gæti orðið vegna breytinga á leigusamningi ef breytingin fæli í sér lægri leiguskuldbindingu sem nemur upphæð sem er hærri en bókfært virði afnotaréttar af eign.</span><span class="sxs-lookup"><span data-stu-id="7e238-142">A gain might arise during a lease modification if the modification decreases the lease liability by an amount that exceeds the carrying value of the ROU asset.</span></span>

<span data-ttu-id="7e238-143">Sem dæmi má nefna að leigusamningur er með núverandi bókfært virði leiguskuldbindingar upp á $150.000 og bókfært virði afnotaréttar af eign upp á $100.000.</span><span class="sxs-lookup"><span data-stu-id="7e238-143">For example, a lease has a current carrying value of the lease liability of $150,000 and a carrying value of the ROU asset of $100,000.</span></span> <span data-ttu-id="7e238-144">Leigusamningnum er breytt og þessar breytingar mynda nýtt núverandi virði á lágmarksleigugreiðslum (PVFMLP) upp á $40.000.</span><span class="sxs-lookup"><span data-stu-id="7e238-144">The lease is modified, and this modification produces a new present value of the future minimum lease payments (PVFMLP) of $40,000.</span></span> <span data-ttu-id="7e238-145">Af þeim sökum verður leiguskuldbindingin debetfærð upp á $110.000 ($150.000 – $40.000).</span><span class="sxs-lookup"><span data-stu-id="7e238-145">Therefore, the lease liability will be debited by $110,000 ($150,000 – $40,000).</span></span> <span data-ttu-id="7e238-146">Þar sem afnotaréttur af eign er aðeins $100.000 mun minnkun upp á $110.000 lækka eignina umfram 0 (núll).</span><span class="sxs-lookup"><span data-stu-id="7e238-146">Because the ROU asset is only $100,000, the decrease of $110,000 will decrease the asset past 0 (zero).</span></span> <span data-ttu-id="7e238-147">Þess vegna segir í leiðbeiningum um bókhald að eftirstöðvar eigi að vera bókaðar á hagnaðarlykil.</span><span class="sxs-lookup"><span data-stu-id="7e238-147">Therefore, the accounting guidance states that the remainder should be booked to a gain account.</span></span> <span data-ttu-id="7e238-148">Hér verður endanleg færsla í færslubók því debetfærð á leiguskuldbindingu upp á $110.000, kreditfærð á leigueignina upp á $100.000 og kreditfærð á hagnaðarlykilinn upp á $10.000.</span><span class="sxs-lookup"><span data-stu-id="7e238-148">In this case, the final journal entry will be a debit to the lease liability for $110,000, a credit to the lease asset for $100,000, and a credit to the gain account for $10,000.</span></span>

<span data-ttu-id="7e238-149">**Dæmi um bókarfærslur:** Breyting á leigusamningi</span><span class="sxs-lookup"><span data-stu-id="7e238-149">**Example journal entries:** Lease modification</span></span><br>
<span data-ttu-id="7e238-150">**Debet:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-150">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="7e238-151">**Kredit:** Leigueign XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-151">**Credit:** Lease Asset XXX</span></span><br>
<span data-ttu-id="7e238-152">**Kredit:** Hagnaður XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-152">**Credit:** Gain XXX</span></span>

## <a name="accumulated-depreciation"></a><span data-ttu-id="7e238-153">Uppsöfnuð afskrift</span><span class="sxs-lookup"><span data-stu-id="7e238-153">Accumulated depreciation</span></span>

<span data-ttu-id="7e238-154">Lykillinn er tengdur við andstæðan eignalykil fyrir afnotarétt af eign.</span><span class="sxs-lookup"><span data-stu-id="7e238-154">The account is associated with the contra-asset account of the ROU asset.</span></span> <span data-ttu-id="7e238-155">Þessi lykill er kreditfærður þegar afskriftarkostnaður er bókaður.</span><span class="sxs-lookup"><span data-stu-id="7e238-155">This account is credited when a depreciation expense is posted.</span></span>

<span data-ttu-id="7e238-156">**Dæmi um færslubókarfærslur:** Afskriftauppsöfnun</span><span class="sxs-lookup"><span data-stu-id="7e238-156">**Example journal entries:** Depreciation accrual</span></span><br>
<span data-ttu-id="7e238-157">**Debet:** Afskriftakostnaður XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-157">**Debit:** Depreciation expense XXX</span></span><br>
<span data-ttu-id="7e238-158">**Kredit:** Uppsafnaðar afskriftir XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-158">**Credit:** Accumulated depreciation XXX</span></span>

## <a name="retained-earnings"></a><span data-ttu-id="7e238-159">Óráðstafað eigið fé</span><span class="sxs-lookup"><span data-stu-id="7e238-159">Retained earnings</span></span>

<span data-ttu-id="7e238-160">Lykillinn er tengdur óráðstöfuðum tekjum.</span><span class="sxs-lookup"><span data-stu-id="7e238-160">The account is associated with retained earnings.</span></span> <span data-ttu-id="7e238-161">Þennan lykil má annaðhvort debetfæra eða kreditfæra í bókarfærslu leiðréttingar umbreytingar með því að nota fulla afturvirka aðferð eða uppsafnaða A-tiltektarvalkostinn.</span><span class="sxs-lookup"><span data-stu-id="7e238-161">This account might be either debited or credited in a transition adjustment journal entry by using the full retrospective method or the cumulative catch-up option A method.</span></span> <span data-ttu-id="7e238-162">Mismunurinn milli upphaflegs afnotaréttar af eign og leiguskuldbindingar er bókaður í óráðstafaðar tekjur.</span><span class="sxs-lookup"><span data-stu-id="7e238-162">The difference between the initial ROU asset and lease liability is booked to retained earnings.</span></span> <span data-ttu-id="7e238-163">Í örfáum tilvikum gætu óráðstafaðar tekjur einnig orðið fyrir áhrifum við breytingar á leigusamningi, ef flokkun leigusamnings er breytt úr fjármálum í rekstur við uppgjör eða niðurfærslu afnotaréttar af eign til að hann sé jafngildur leiguskuldbindingu.</span><span class="sxs-lookup"><span data-stu-id="7e238-163">In rare cases, the retained earnings might also be affected during lease modification, if the classification of a lease is changed from finance to operating to write the ROU asset up or down so that it equals the lease liability.</span></span>

<span data-ttu-id="7e238-164">**Dæmi um bókarfærslur:** Leiðrétting umbreytingar (fullur afturkræfur eða uppsafnaður A-tiltektarvalkostur)</span><span class="sxs-lookup"><span data-stu-id="7e238-164">**Example journal entries:** Transition adjustment (full retrospective or cumulative catch-up option A method)</span></span><br>
<span data-ttu-id="7e238-165">**Debet:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-165">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="7e238-166">**Kredit:** Leigueign xxx</span><span class="sxs-lookup"><span data-stu-id="7e238-166">**Credit:** Lease asset XXX</span></span><br>
<span data-ttu-id="7e238-167">**Kredit:** Óráðstafaðar tekjur</span><span class="sxs-lookup"><span data-stu-id="7e238-167">**Credit:** Retained earnings XXX</span></span>

## <a name="variable-payment"></a><span data-ttu-id="7e238-168">Breytileg greiðsla</span><span class="sxs-lookup"><span data-stu-id="7e238-168">Variable payment</span></span>

<span data-ttu-id="7e238-169">Lykillinn tengist breytilegum leigugreiðslum sem eru myndaðar af endurmatsferli vísitölu samkvæmt ASC 842-, ASC 840- og IAS 17-leigusamningum.</span><span class="sxs-lookup"><span data-stu-id="7e238-169">The account is associated with variable lease payments that are produced by an index revaluation under ASC 842, ASC 840, and IAS 17 leases.</span></span> <span data-ttu-id="7e238-170">Í greiðsluáætlun leigusamnings eru breytilegar greiðslur innifaldar í dálknum **Breytileg greiðsla**.</span><span class="sxs-lookup"><span data-stu-id="7e238-170">In the lease payment schedule, variable payments are included in the **Variable payment** column.</span></span> <span data-ttu-id="7e238-171">Þessi lykill er skuldfærður þegar reikningur er stofnaður gegn greiðsluáætlunarlínu sem inniheldur breytilega greiðslu.</span><span class="sxs-lookup"><span data-stu-id="7e238-171">This account is debited when an invoice is created against a payment schedule line that contains a variable payment.</span></span>

<span data-ttu-id="7e238-172">**Dæmi um bókarfærslur:** Leigugreiðsla</span><span class="sxs-lookup"><span data-stu-id="7e238-172">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="7e238-173">**Debet:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-173">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="7e238-174">**Skuldfærsla:** Breytileg greiðsla XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-174">**Debit:** Variable payment XXX</span></span><br>
<span data-ttu-id="7e238-175">**Kredit:** Skuldastaða lánardrottins/leigugreiðsla XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-175">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="deferred-rent-asset-liability"></a><span data-ttu-id="7e238-176">Frestaðar leigugreiðslur eignar (skuld)</span><span class="sxs-lookup"><span data-stu-id="7e238-176">Deferred rent asset (liability)</span></span>

<span data-ttu-id="7e238-177">Lykillinn er tengdur við frestaðar leigugreiðslur eignar eða skuldar sem er mynduð af frestuðum leigugreiðslum leigusamnings.</span><span class="sxs-lookup"><span data-stu-id="7e238-177">The account is associated with the deferred rent asset or liability that is produced by a deferred rent treatment lease.</span></span> <span data-ttu-id="7e238-178">Þessi lykill er debetfærður þegar reikningur er bókaður á móti frestuðum leigugreiðslum leigusamnings ef upphæð leigugreiðslu er hærri en línulegur leigukostnaður tímabilsins.</span><span class="sxs-lookup"><span data-stu-id="7e238-178">This account is debited when an invoice is posted against a deferred rent treatment lease, if the lease payment amount is more than the period's straight-line rent expense.</span></span> <span data-ttu-id="7e238-179">Hann er kreditfærður ef leigugreiðslan er lægri en línulegur leigukostnaður tímabilsins.</span><span class="sxs-lookup"><span data-stu-id="7e238-179">It's credited if the lease payment is less than the period's straight-line rent expense.</span></span>

<span data-ttu-id="7e238-180">**Dæmi um bókarfærslur:** Leigugreiðsla (frestaðar leigugreiðslur leigusamnings)</span><span class="sxs-lookup"><span data-stu-id="7e238-180">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="7e238-181">**Debet:** Leigukostnaður XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-181">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="7e238-182">**Kredit:** Skuldbinding vegna frestaðra leigugreiðslna XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-182">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="7e238-183">**Kredit:** Skuldastaða lánardrottins/leigugreiðsla XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-183">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="lease-expense"></a><span data-ttu-id="7e238-184">Leigukostnaður</span><span class="sxs-lookup"><span data-stu-id="7e238-184">Lease expense</span></span>

<span data-ttu-id="7e238-185">Lykillinn tengist leigukostnaðinum ef leigan er flokkuð sem frestaðar leigugreiðslur leigusamnings.</span><span class="sxs-lookup"><span data-stu-id="7e238-185">The account is associated with the lease expense if the lease is classified as a deferred rent treatment lease.</span></span> <span data-ttu-id="7e238-186">Þessi lykill er debetfærður þegar reikningur er bókaður á móti frestuðum leigugreiðslum leigusamnings.</span><span class="sxs-lookup"><span data-stu-id="7e238-186">This account is debited when an invoice is posted against a deferred rent treatment lease.</span></span>

<span data-ttu-id="7e238-187">**Dæmi um bókarfærslur:** Leigugreiðsla (frestaðar leigugreiðslur leigusamnings)</span><span class="sxs-lookup"><span data-stu-id="7e238-187">**Example journal entries:** Lease payment (deferred rent treatment lease)</span></span><br>
<span data-ttu-id="7e238-188">**Debet:** Leigukostnaður XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-188">**Debit:** Lease expense XXX</span></span><br>
<span data-ttu-id="7e238-189">**Kredit:** Skuldbinding vegna frestaðra leigugreiðslna XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-189">**Credit:** Deferred rent liability XXX</span></span><br>
<span data-ttu-id="7e238-190">**Kredit:** Skuldastaða lánardrottins/leigugreiðsla XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-190">**Credit:** Vendor payable/lease payment XXX</span></span>

## <a name="impairment-expense"></a><span data-ttu-id="7e238-191">Kostnaður virðisrýrnunar</span><span class="sxs-lookup"><span data-stu-id="7e238-191">Impairment expense</span></span>

<span data-ttu-id="7e238-192">Lykillinn er mótbókaður þegar leigusamningur skerðist.</span><span class="sxs-lookup"><span data-stu-id="7e238-192">The account is posted against when a lease is impaired.</span></span> <span data-ttu-id="7e238-193">Þessi lykill er debetfærður á meðan lykill afnotaréttar af eign er kreditfærður beint.</span><span class="sxs-lookup"><span data-stu-id="7e238-193">This account is debited, whereas the ROU asset account is directly credited.</span></span>

<span data-ttu-id="7e238-194">**Dæmi um bókarfærslur:** Leigugreiðsla</span><span class="sxs-lookup"><span data-stu-id="7e238-194">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="7e238-195">**Debet:** Kostnaður virðisrýrnunar XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-195">**Debit:** Impairment expense XXX</span></span><br>
<span data-ttu-id="7e238-196">**Kredit:** Afnotaréttur af eign XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-196">**Credit:** ROU asset XXX</span></span>

## <a name="lease-payment"></a><span data-ttu-id="7e238-197">Leigugreiðsla</span><span class="sxs-lookup"><span data-stu-id="7e238-197">Lease payment</span></span>

<span data-ttu-id="7e238-198">Lykillinn er mótbókaður ef slökkt er á færibreytunni **Greiða lánardrottni**.</span><span class="sxs-lookup"><span data-stu-id="7e238-198">The account is posted against if the **Pay to Vendor** parameter is turned off.</span></span> <span data-ttu-id="7e238-199">Lykillinn er kreditfærður í stað lánardrottnaskuldar ef slökkt er á færibreytunni.</span><span class="sxs-lookup"><span data-stu-id="7e238-199">This account is credited instead of the vendor payable if the parameter is turned off.</span></span>

<span data-ttu-id="7e238-200">**Dæmi um bókarfærslur:** Leigugreiðsla</span><span class="sxs-lookup"><span data-stu-id="7e238-200">**Example journal entries:** Lease payment</span></span><br>
<span data-ttu-id="7e238-201">**Debet:** Leiguskuldbinding XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-201">**Debit:** Lease liability XXX</span></span><br>
<span data-ttu-id="7e238-202">**Kredit:** Leigugreiðsla XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-202">**Credit:** Lease payment XXX</span></span>

## <a name="expense-type-postings"></a><span data-ttu-id="7e238-203">Bókun kostnaðargerðar</span><span class="sxs-lookup"><span data-stu-id="7e238-203">Expense type postings</span></span>

<span data-ttu-id="7e238-204">Lykillinn sem er valinn fyrir hverja kostnaðargerð er debetfærður þegar greiðsla fyrir þá kostnaðargerð er mynduð.</span><span class="sxs-lookup"><span data-stu-id="7e238-204">The account that is selected for each expense type is debited when a payment for that expense type is generated.</span></span> <span data-ttu-id="7e238-205">Til dæmis er lykillinn sem er tilgreindur fyrir kostnaðargerðina **Trygging** debetfærður í hvert sinn sem reikningur eða greiðslubókarfærsla er stofnuð úr rekstrarkostnaðaráætlun vegna tryggingakostnaðar.</span><span class="sxs-lookup"><span data-stu-id="7e238-205">For example, the account that is specified for the **Insurance** expense type is debited whenever an invoice or payment journal entry is created from the executory cost schedule for insurance expense.</span></span>

<span data-ttu-id="7e238-206">**Dæmi um bókarfærslur:** Tryggingagreiðsla</span><span class="sxs-lookup"><span data-stu-id="7e238-206">**Example journal entries:** Insurance payment</span></span><br>
<span data-ttu-id="7e238-207">**Debet:** Tryggingakostnaðarlykill XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-207">**Debit:** Insurance expense type account XXX</span></span><br>
<span data-ttu-id="7e238-208">**Kredit:** Mótlykill XXX</span><span class="sxs-lookup"><span data-stu-id="7e238-208">**Credit:** Offset account XXX</span></span>

> [!NOTE]
> <span data-ttu-id="7e238-209">Mótlykill er valinn á leigustigi á línunum fyrir greiðsluáætlun rekstrarkostnaðar.</span><span class="sxs-lookup"><span data-stu-id="7e238-209">The offset account is selected at the lease level on the lines for the executory cost payment schedule.</span></span> <span data-ttu-id="7e238-210">Þessi mótlykill getur tengst lánardrottni eða með fjárhagslykli.</span><span class="sxs-lookup"><span data-stu-id="7e238-210">This offset account can associated with the vendor, or with a ledger account.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]