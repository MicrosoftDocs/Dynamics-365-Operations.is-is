---
title: "Bókunarreglur viðskiptavina"
description: "Bókunarreglur viðskiptavina stýra bókun á viðskiptavinafærslum í fjárhag."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: da750645612c2a0a7650edfd933d707618d9f9ce
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---

# <a name="customer-posting-profiles"></a><span data-ttu-id="16bdc-103">Bókunarreglur viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="16bdc-103">Customer posting profiles</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="16bdc-104">Bókunarreglur viðskiptavina stýra bókun á viðskiptavinafærslum í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="16bdc-104">Customer posting profiles control the posting of customer transactions to the general ledger.</span></span>

<a name="customer-posting-profiles"></a><span data-ttu-id="16bdc-105">Bókunarreglur viðskiptavina</span><span class="sxs-lookup"><span data-stu-id="16bdc-105">Customer posting profiles</span></span>
-------------------------

<span data-ttu-id="16bdc-106">Bókunarreglur viðskiptavina gera það mögulegt að úthluta fjárhagslykla og skjalastillingar fyrir alla viðskiptavini, hóp af viðskiptavinum eða einn viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="16bdc-106">Customer posting profiles enable you to assign general ledger accounts and document settings to all customers, a group of customers or a single customer.</span></span> <span data-ttu-id="16bdc-107">Þessar stillingar verður notuð þegar stofnaðar eru sölupantanir, reikningur með frjálsum texta, staðgreiðslur, innheimtubréf og vaxtanótur.</span><span class="sxs-lookup"><span data-stu-id="16bdc-107">These settings will be used when you create sales orders, free text invoices, cash payments, collection letters, and interest notes.</span></span> <span data-ttu-id="16bdc-108">Fyrir sumar færslur geturðu valið bókunarreglu sem er frábrugðin og sem hefur forgang fram yfir bókunarregluna sem er sett upp fyrir færslur í þessar skjámynd.</span><span class="sxs-lookup"><span data-stu-id="16bdc-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> 

<span data-ttu-id="16bdc-109">Sjálfgefin bókunarregla er skilgreint í flýtiflipanum Fjárhagur og Virðisaukaskattir á síðunni Færibreytur viðskiptaskulda.</span><span class="sxs-lookup"><span data-stu-id="16bdc-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts receivable parameters page.</span></span> <span data-ttu-id="16bdc-110">Sjálfgefin bókunarregla er síðan tekin með sjálfkrafa í haus nýrra skjala þar sem hægt er að breyta henni í aðra bókunarreglu ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="16bdc-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="16bdc-111">Einnig er hægt að tengja bókunarskilgreiningar við færslubókunargerð í síðu skilgreining færslubókunar.</span><span class="sxs-lookup"><span data-stu-id="16bdc-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="16bdc-112">Bókunarskilgreiningar stýra bókun á viðskiptavinafærslum í fjárhag í stað bókunarskilgreininga.</span><span class="sxs-lookup"><span data-stu-id="16bdc-112">Posting definitions control the posting of customer transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="16bdc-113">Stofnun Bókunarregla</span><span class="sxs-lookup"><span data-stu-id="16bdc-113">Creating a posting profile</span></span>
<span data-ttu-id="16bdc-114">Tilgreinið fjárhagslyklana sem eru notaðir við bókun færsla sem nota valda bókunarreglunni.</span><span class="sxs-lookup"><span data-stu-id="16bdc-114">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="16bdc-115">Veljið reikningskóða og þegar hægt er reiknings- eða flokkanúmer fyrir valda bókunarfærslu.</span><span class="sxs-lookup"><span data-stu-id="16bdc-115">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="16bdc-116">Við bókunarferli er sú bókunarregla sem er mest viðeigandi fyrir hverja færslu fundin með því að leita að afmörkuðustu reikningskóða-, reikningsnúmera- eða flokkanúmerasamsetningu í eftirfarandi forgangi:</span><span class="sxs-lookup"><span data-stu-id="16bdc-116">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="16bdc-117">**Lykilkóði** svæðisgildið</span><span class="sxs-lookup"><span data-stu-id="16bdc-117">**Account code** field value</span></span> | <span data-ttu-id="16bdc-118">**Númer lykils/Flokks** svæðisgildið</span><span class="sxs-lookup"><span data-stu-id="16bdc-118">**Account/Group number** field value</span></span>            | <span data-ttu-id="16bdc-119">Forgangsröðun leitar</span><span class="sxs-lookup"><span data-stu-id="16bdc-119">Search priority</span></span> |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="16bdc-120">**Tafla**</span><span class="sxs-lookup"><span data-stu-id="16bdc-120">**Table**</span></span>                    | <span data-ttu-id="16bdc-121">Tiltekinn viðskiptavinareikningur.</span><span class="sxs-lookup"><span data-stu-id="16bdc-121">Specific customer account</span></span>                       | <span data-ttu-id="16bdc-122">1</span><span class="sxs-lookup"><span data-stu-id="16bdc-122">1</span></span>               |
| <span data-ttu-id="16bdc-123">**Flokkur**</span><span class="sxs-lookup"><span data-stu-id="16bdc-123">**Group**</span></span>                    | <span data-ttu-id="16bdc-124">Viðskiptavinarflokkur sem er úthlutað á viðskiptavininn</span><span class="sxs-lookup"><span data-stu-id="16bdc-124">Customer group that is assigned to the customer</span></span> | <span data-ttu-id="16bdc-125">2</span><span class="sxs-lookup"><span data-stu-id="16bdc-125">2</span></span>               |
| <span data-ttu-id="16bdc-126">**Allt**</span><span class="sxs-lookup"><span data-stu-id="16bdc-126">**All**</span></span>                      | <span data-ttu-id="16bdc-127">Autt</span><span class="sxs-lookup"><span data-stu-id="16bdc-127">Blank</span></span>                                           | <span data-ttu-id="16bdc-128">3</span><span class="sxs-lookup"><span data-stu-id="16bdc-128">3</span></span>               |

<span data-ttu-id="16bdc-129">Ef óskað er eftir að allar færsla viðskiptavinar hafi sömu bókunarregluna setjið þá einungis upp eina bókunarreglu með gildinu  Allt í svæðið lykilkóði.</span><span class="sxs-lookup"><span data-stu-id="16bdc-129">If you want all customer transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="16bdc-130">Tilgreina eftirfarandi gildum til að setja upp bókunarreglunni :</span><span class="sxs-lookup"><span data-stu-id="16bdc-130">Specify the following values to set up your posting profile:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="16bdc-131">Reitur</span><span class="sxs-lookup"><span data-stu-id="16bdc-131">Field</span></span></th>
<th><span data-ttu-id="16bdc-132">Lýsing</span><span class="sxs-lookup"><span data-stu-id="16bdc-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="16bdc-133"><strong>Bókunarregla</strong></span><span class="sxs-lookup"><span data-stu-id="16bdc-133"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="16bdc-134">Færið inn kóða fyrir bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="16bdc-134">Enter a code for the posting profile.</span></span> <span data-ttu-id="16bdc-135">T.d. væri hægt að útbúa tvær bókunarreglur til að fá einn lykil fyrir viðskiptavinastöður í landsgjaldmiðlinum og annan fyrir viðskiptavinastöður í erlendum gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="16bdc-135">For example, you could create two posting profiles to obtain one account for customer balances in the national currency and another for customer balances in a foreign currency.</span></span> <span data-ttu-id="16bdc-136">Hægt væri að kalla annan lykilinn „Lands“ og hinn „Erlendur“.</span><span class="sxs-lookup"><span data-stu-id="16bdc-136">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16bdc-137"><strong>Lýsing</strong></span><span class="sxs-lookup"><span data-stu-id="16bdc-137"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="16bdc-138">Færa skal inn lýsingu á bókunarregla.</span><span class="sxs-lookup"><span data-stu-id="16bdc-138">Enter a description of the posting profile.</span></span> <span data-ttu-id="16bdc-139">Þetta er einungis notað til að auðkenna betur bókunarregla þegar það er skoða í þessa síðu.</span><span class="sxs-lookup"><span data-stu-id="16bdc-139">This is only used to better identify the posting profile when you view it in this page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16bdc-140"><strong>Kóði lykils</strong></span><span class="sxs-lookup"><span data-stu-id="16bdc-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="16bdc-141">Tilgreinið hvort bókunarreglan eigi við um einstakan viðskiptavin, flokk af viðskiptavinum eða alla viðskiptavini:</span><span class="sxs-lookup"><span data-stu-id="16bdc-141">Specify whether the posting profile applies to a single customer, a group of customers, or all customers:</span></span>
<ul>
<li><span data-ttu-id="16bdc-142"><strong>Taflan</strong> – bókunarregla á við einn viðskiptamaður.</span><span class="sxs-lookup"><span data-stu-id="16bdc-142"><strong>Table</strong> – The posting profile applies to a single customer.</span></span> <span data-ttu-id="16bdc-143">Veljið viðskiptavinalykil í númerareit lykils/flokks.</span><span class="sxs-lookup"><span data-stu-id="16bdc-143">Select the customer account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="16bdc-144"><strong>Taflan</strong> – bókunarregla á við einn viðskiptavinaflokk.</span><span class="sxs-lookup"><span data-stu-id="16bdc-144"><strong>Group</strong> – The posting profile applies to a customer group.</span></span> <span data-ttu-id="16bdc-145">Veljið viðskiptavinaflokk í númerareit lykils/flokks.</span><span class="sxs-lookup"><span data-stu-id="16bdc-145">Select the customer group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="16bdc-146"><strong>Allt</strong> – bókunarregla á við alla viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="16bdc-146"><strong>All</strong> – The posting profile applies to all customers.</span></span> <span data-ttu-id="16bdc-147">Látið Númer lykils/Flokks svæðisgildið vera autt.</span><span class="sxs-lookup"><span data-stu-id="16bdc-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16bdc-148"><strong>Númer lykils/flokks</strong></span><span class="sxs-lookup"><span data-stu-id="16bdc-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="16bdc-149">Ef tafla er valin í svæðinu lykilkóði veljið þá lykilnúmer viðskiptavinar sem er tengdur við bókunarregluna.</span><span class="sxs-lookup"><span data-stu-id="16bdc-149">If Table is selected in the Account code field, select the account number of the customer who is associated with the posting profile.</span></span> <span data-ttu-id="16bdc-150">Ef valinn er Flokkur, veljið þá flokk viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="16bdc-150">If Group is selected, select the customer group.</span></span> <span data-ttu-id="16bdc-151">Ef allt er valið skal skilja þetta svæði eftir autt.</span><span class="sxs-lookup"><span data-stu-id="16bdc-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16bdc-152"><strong>Safnlykill</strong></span><span class="sxs-lookup"><span data-stu-id="16bdc-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="16bdc-153">Veljið fjárhagslykilinn sem nota á sem safnlykil viðskiptavina fyrir viðskiptavini sem bókunarreglan er úthlutuð á.</span><span class="sxs-lookup"><span data-stu-id="16bdc-153">Select the ledger account that will be used as the customer summary account for the customers who are associated with the posting profile.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16bdc-154"><strong>Jafna lykil</strong></span><span class="sxs-lookup"><span data-stu-id="16bdc-154"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="16bdc-155">Veldu fjárhagslykill greiðslugetu sem er notaður fyrir sjóðsstreymisspá.</span><span class="sxs-lookup"><span data-stu-id="16bdc-155">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="16bdc-156">Þetta svæði birtast aðeins ef sjóðstreymisspár eru virkjuð.</span><span class="sxs-lookup"><span data-stu-id="16bdc-156">This field will only appear if cash flow forecasts are enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16bdc-157"><strong>Fyrirframgreiðslur virðisaukaskatts</strong></span><span class="sxs-lookup"><span data-stu-id="16bdc-157"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="16bdc-158">Færið inn lykil fyrir virðisaukaskatt fyrir fyrirframgreiðslur.</span><span class="sxs-lookup"><span data-stu-id="16bdc-158">Select the account for sales tax for payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="16bdc-159"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Ábending</span><span class="sxs-lookup"><span data-stu-id="16bdc-159"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="16bdc-160"><strong>Athugið</strong></span><span class="sxs-lookup"><span data-stu-id="16bdc-160"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="16bdc-161">Síðunni færibreytur viðskiptakrafna er notuð til að tilgreina bókunarreglu sem nota á þegar greiðsla er merkt sem fyrirframgreiðsla.</span><span class="sxs-lookup"><span data-stu-id="16bdc-161">Use the Accounts receivable parameters page to specify the posting profile to use when a payment is marked as a prepayment.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16bdc-162"><strong>Skuldbindingar vegna afsláttarlykils</strong></span><span class="sxs-lookup"><span data-stu-id="16bdc-162"><strong>Liabilities for discount account</strong></span></span></td>
<td><span data-ttu-id="16bdc-163">Veljið Fjárhagslyklar fyrir afsláttarskuldbindingar.</span><span class="sxs-lookup"><span data-stu-id="16bdc-163">Select the ledger account for liabilities of discount.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="16bdc-164"><strong>Innheimtubréfaröð</strong></span><span class="sxs-lookup"><span data-stu-id="16bdc-164"><strong>Collection letter sequence</strong></span></span></td>
<td><span data-ttu-id="16bdc-165">Veljið kennimerki innheimtubréfaraðar fyrir viðskiptavini sem bókunarreglan tengist.</span><span class="sxs-lookup"><span data-stu-id="16bdc-165">Select the identifier of the collection letter sequence to use for customers to whom the posting profile is assigned.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="16bdc-166"><strong>Vaxtakóði</strong></span><span class="sxs-lookup"><span data-stu-id="16bdc-166"><strong>Interest code</strong></span></span></td>
<td><span data-ttu-id="16bdc-167">Veljið vaxtakóði til að nota fyrir útreikninga vaxta fyrir viðskiptavini sem bókunarreglan tengist.</span><span class="sxs-lookup"><span data-stu-id="16bdc-167">Select the interest code to use for the calculation of interest for customers to whom the posting profile is assigned.</span></span></td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a><span data-ttu-id="16bdc-168">**Töfluskorður**</span><span class="sxs-lookup"><span data-stu-id="16bdc-168">**Table restrictions**</span></span>

<span data-ttu-id="16bdc-169">Tilgreinið fyrir færslurnar með völdu bókunarreglunni hvort færslur verða jafnaðar sjálfkrafa, vexti reikna út og innheimtubréf gefin út.</span><span class="sxs-lookup"><span data-stu-id="16bdc-169">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="16bdc-170">Þú getur einnig valið reikning sem notaður er þegar færslur með valdri bókunarreglu er lokað.</span><span class="sxs-lookup"><span data-stu-id="16bdc-170">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="16bdc-171">Tilgreina eftirfarandi gildum til að setja upp bókunarreglunni :</span><span class="sxs-lookup"><span data-stu-id="16bdc-171">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="16bdc-172">Reitur</span><span class="sxs-lookup"><span data-stu-id="16bdc-172">Field</span></span>                 | <span data-ttu-id="16bdc-173">Lýsing</span><span class="sxs-lookup"><span data-stu-id="16bdc-173">Description</span></span>                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16bdc-174">**Uppgjör**</span><span class="sxs-lookup"><span data-stu-id="16bdc-174">**Settlement**</span></span>        | <span data-ttu-id="16bdc-175">Veljið þessa víxlun til að virkja sjálfvirka jöfnun fyrir færslur sem eru með þessari bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="16bdc-175">Select this toggle to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="16bdc-176">Ef þessi víxlun er tóm þarftu að jafna færslur handvirkt með því að nota Jafna opnar færslur síðuna eða síðuna færa inn greiðsla viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="16bdc-176">If this toggle is cleared, you must manually settle transactions by using the Settle open transactions page or the Enter customer payments page.</span></span> |
| <span data-ttu-id="16bdc-177">**Áhugasvið**</span><span class="sxs-lookup"><span data-stu-id="16bdc-177">**Interest**</span></span>          | <span data-ttu-id="16bdc-178">Veldu þessa víxlun eigi að reikna vexti á útistandandi skuldum fyrir viðskiptavinalykill  með þessa forstillingum.</span><span class="sxs-lookup"><span data-stu-id="16bdc-178">Select this toggle if interest should be calculated on outstanding balances for customer accounts that use this profile.</span></span> <span data-ttu-id="16bdc-179">Ef víxlunin er hreinsaður, munu vextir ekki vera reiknaðir fyrir þessa viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="16bdc-179">If this toggle is cleared, interest will not be calculated for these customers.</span></span>                                           |
| <span data-ttu-id="16bdc-180">**Innheimtubréf**</span><span class="sxs-lookup"><span data-stu-id="16bdc-180">**Collection letter**</span></span> | <span data-ttu-id="16bdc-181">Veldu þessa víxlun eigi innheimtubréf að vera myndað fyrir viðskiptavinalykill  með þessa forstillingum.</span><span class="sxs-lookup"><span data-stu-id="16bdc-181">Select this toggle if collection letters should be generated for customer accounts that use this profile.</span></span> <span data-ttu-id="16bdc-182">Ef víxlunin er hreinsaður, munu innheimtubréf ekki vera mynduð fyrir þessa viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="16bdc-182">If this toggle is cleared, collection letters will not be generated for these customers.</span></span>                                                 |
| <span data-ttu-id="16bdc-183">**Loka**</span><span class="sxs-lookup"><span data-stu-id="16bdc-183">**Close**</span></span>             | <span data-ttu-id="16bdc-184">Tilgreinið bókunarreglu sem óskað er eftir að verði breytt yfir í þegar færslur með þessari bókunarreglu eru lokaðar.</span><span class="sxs-lookup"><span data-stu-id="16bdc-184">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="16bdc-185">Litið er á færslu sem lokaða þegar hún hefur verið jöfnuð að fullu.</span><span class="sxs-lookup"><span data-stu-id="16bdc-185">A transaction is regarded as closed when it has been settled in full.</span></span>                                                                           |



<span data-ttu-id="16bdc-186">Frekari upplýsingar, sjá [Yfirlit yfir greiðslur viðskiptavinar](../cash-bank-management/tasks/customer-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="16bdc-186">For more information, see [Customer payment overview](../cash-bank-management/tasks/customer-payment-overview.md).</span></span>


