---
title: "Bókunarreglur lánardrottna"
description: "Bókunarreglur lánardrottins stýra bókun á færslum lánardrottins í fjárhag."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 10e6e88ca8e03c75896d0b9d43afad129d2cb1c8
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="vendor-posting-profiles"></a><span data-ttu-id="7ab80-103">Bókunarreglur lánardrottna</span><span class="sxs-lookup"><span data-stu-id="7ab80-103">Vendor posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7ab80-104">Bókunarreglur lánardrottins stýra bókun á færslum lánardrottins í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="7ab80-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

<a name="vendor-posting-profiles"></a><span data-ttu-id="7ab80-105">Bókunarreglur lánardrottna</span><span class="sxs-lookup"><span data-stu-id="7ab80-105">Vendor posting profiles</span></span>
-----------------------

<span data-ttu-id="7ab80-106">Bókunarreglur lánardrottina gera það mögulegt að úthluta fjárhagslykla og skjalastillingar fyrir alla lánardrottna, hóp af lánardrottna eða einn lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="7ab80-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors or a single vendor.</span></span> <span data-ttu-id="7ab80-107">Þessar stillingar verður notuð þegar stofna innkaupapöntun, reikningur lánardrottins og  staðgreiðsla.</span><span class="sxs-lookup"><span data-stu-id="7ab80-107">These settings will be used when you create purchase orders, vendor invoices and cash payments.</span></span> <span data-ttu-id="7ab80-108">Fyrir sumar færslur geturðu vaæo‘ bókunarreglu sem er frábrugðin og sem hefur forgang fram yfir bókunarregluna sem er sett upp fyrir færslur í þessar skjámynd.</span><span class="sxs-lookup"><span data-stu-id="7ab80-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> <span data-ttu-id="7ab80-109">Sjálfgefin bókunarregla er skilgreint í flýtiflipanum Fjárhagur og Virðisaukaskattur á síðunni Færibreytur viðskiptaskulda.</span><span class="sxs-lookup"><span data-stu-id="7ab80-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts payable parameters page.</span></span> <span data-ttu-id="7ab80-110">Sjálfgefin bókunarregla er síðan tekin með sjálfkrafa í haus ný skjöl þar sem hægt er að breyta henni í aðra bókunarreglu ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="7ab80-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="7ab80-111">Einnig er hægt að tengja bókunarskilgreiningar við færslubókunargerð í síðu skilgreining færslubókunar.</span><span class="sxs-lookup"><span data-stu-id="7ab80-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="7ab80-112">Bókunarskilgreining stýra bókun á lánardrottnafærslum í fjárhag í stað bókunarskilgreininga.</span><span class="sxs-lookup"><span data-stu-id="7ab80-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="7ab80-113">Stofnun Bókunarregla</span><span class="sxs-lookup"><span data-stu-id="7ab80-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="7ab80-114">**Uppsetning**</span><span class="sxs-lookup"><span data-stu-id="7ab80-114">**Setup**</span></span>

<span data-ttu-id="7ab80-115">Tilgreinið fjárhagslyklana sem eru notaðir við bókun færsla sem nota valda bókunarreglunni.</span><span class="sxs-lookup"><span data-stu-id="7ab80-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="7ab80-116">Veljið reikningskóða og þegar hægt er reiknings- eða flokkanúmer fyrir valda bókunarfærslu.</span><span class="sxs-lookup"><span data-stu-id="7ab80-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="7ab80-117">Við bókunarferli er sú bókunarregla sem er mest viðeigandi fyrir hverja færslu fundin með því að leita að afmörkuðustu reikningskóða-, reikningsnúmera- eða flokkanúmerasamsetningu í eftirfarandi forgangi:</span><span class="sxs-lookup"><span data-stu-id="7ab80-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="7ab80-118">**Lykilkóði** svæðisgildið</span><span class="sxs-lookup"><span data-stu-id="7ab80-118">**Account code** field value</span></span> | <span data-ttu-id="7ab80-119">**Númer lykils/Flokks** svæðisgildið</span><span class="sxs-lookup"><span data-stu-id="7ab80-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="7ab80-120">Forgangsröðun leitar</span><span class="sxs-lookup"><span data-stu-id="7ab80-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="7ab80-121">**Tafla**</span><span class="sxs-lookup"><span data-stu-id="7ab80-121">**Table**</span></span>                    | <span data-ttu-id="7ab80-122">Tilgreindur lánardrottnareikningur</span><span class="sxs-lookup"><span data-stu-id="7ab80-122">Specific vendor account</span></span>                     | <span data-ttu-id="7ab80-123">1</span><span class="sxs-lookup"><span data-stu-id="7ab80-123">1</span></span>               |
| <span data-ttu-id="7ab80-124">**Flokkur**</span><span class="sxs-lookup"><span data-stu-id="7ab80-124">**Group**</span></span>                    | <span data-ttu-id="7ab80-125">Lánardrottnahópur sem lánardrottinn tengist</span><span class="sxs-lookup"><span data-stu-id="7ab80-125">vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="7ab80-126">2</span><span class="sxs-lookup"><span data-stu-id="7ab80-126">2</span></span>               |
| <span data-ttu-id="7ab80-127">**Allt**</span><span class="sxs-lookup"><span data-stu-id="7ab80-127">**All**</span></span>                      | <span data-ttu-id="7ab80-128">Autt</span><span class="sxs-lookup"><span data-stu-id="7ab80-128">Blank</span></span>                                       | <span data-ttu-id="7ab80-129">3</span><span class="sxs-lookup"><span data-stu-id="7ab80-129">3</span></span>               |

<span data-ttu-id="7ab80-130">Ef óskað er eftir að allar lánardrottnafærslur hafi sömu bókunarregluna, setjið þá einungis upp eina bókunarreglu með gildinu Allt í svæðið lykilkóði.</span><span class="sxs-lookup"><span data-stu-id="7ab80-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="7ab80-131">Tilgreina eftirfarandi gildum til að setja upp bókunarreglunni :</span><span class="sxs-lookup"><span data-stu-id="7ab80-131">Specify the following values to set up your posting profile:</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="7ab80-132">Reitur</span><span class="sxs-lookup"><span data-stu-id="7ab80-132">Field</span></span></th>
<th><span data-ttu-id="7ab80-133">Lýsing</span><span class="sxs-lookup"><span data-stu-id="7ab80-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ab80-134"><strong>Bókunarregla</strong></span><span class="sxs-lookup"><span data-stu-id="7ab80-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="7ab80-135">Færið inn kóða fyrir bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="7ab80-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="7ab80-136">T.d. væri hægt að útbúa tvær bókunarreglur til að fá einn lykil fyrir lánardrottnastöður í landsgjaldmiðlinum og annan fyrir lánardrottnastöður í erlendum gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="7ab80-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="7ab80-137">Hægt væri að kalla annan lykilinn „Lands“ og hinn „Erlendur“.</span><span class="sxs-lookup"><span data-stu-id="7ab80-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ab80-138"><strong>Lýsing</strong></span><span class="sxs-lookup"><span data-stu-id="7ab80-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="7ab80-139">Færa skal inn lýsingu á bókunarregla.</span><span class="sxs-lookup"><span data-stu-id="7ab80-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ab80-140"><strong>Kóði lykils</strong></span><span class="sxs-lookup"><span data-stu-id="7ab80-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="7ab80-141">Tilgreinið hvort bókunarreglan eigi við um einstakan lánardrottinn, flokk af lánardrottnum eða alla lánardrottna:</span><span class="sxs-lookup"><span data-stu-id="7ab80-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="7ab80-142"><strong>Taflan</strong> – bókunarregla við einn lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="7ab80-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="7ab80-143">Veljið lánardrottnalykill í númerareit lykils/flokks.</span><span class="sxs-lookup"><span data-stu-id="7ab80-143">Select the vendor account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="7ab80-144"><strong>Taflan</strong> – bókunarregla á við einn lánardrottnaflokk.</span><span class="sxs-lookup"><span data-stu-id="7ab80-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="7ab80-145">Veljið lánardrottnaflokkur í númerareit lykils/flokks.</span><span class="sxs-lookup"><span data-stu-id="7ab80-145">Select the vendor group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="7ab80-146"><strong>Allt</strong> – bókunarregla á við alla lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="7ab80-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="7ab80-147">Látið Númer lykils/Flokks svæðisgildið vera autt.</span><span class="sxs-lookup"><span data-stu-id="7ab80-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ab80-148"><strong>Númer lykils/flokks</strong></span><span class="sxs-lookup"><span data-stu-id="7ab80-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="7ab80-149">Ef tafla er valin í svæðinu lykilkóði veljið þá lykilnúmer lánardrottins sem er tengdur við bókunarregluna.</span><span class="sxs-lookup"><span data-stu-id="7ab80-149">If Table is selected in the Account code field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="7ab80-150">Ef valinn er Flokkur, veljið þá flokk lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="7ab80-150">If Group is selected, select a vendor group.</span></span> <span data-ttu-id="7ab80-151">Ef allt er valið skal skilja þetta svæði eftir autt.</span><span class="sxs-lookup"><span data-stu-id="7ab80-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ab80-152"><strong>Safnlykill</strong></span><span class="sxs-lookup"><span data-stu-id="7ab80-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="7ab80-153">Veljið fjárhagslykilinn sem nota á sem safnlykil fyrir lánardrottna sem bókunarreglan er tengd.</span><span class="sxs-lookup"><span data-stu-id="7ab80-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Athugið" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="7ab80-155"><strong>Athugaðu</strong></span><span class="sxs-lookup"><span data-stu-id="7ab80-155"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ab80-156">Ef víxlunin Nota bókunarskilgreiningar er valinn á síðunni Færibreytur fjárhags er færslubókunarskilgreining fyrir reikningur lánardrottins notað í stað samantektarlykils.</span><span class="sxs-lookup"><span data-stu-id="7ab80-156">If the Use posting definitions toggle is selected in the General ledger parameters page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ab80-157"><strong>Jafna lykil</strong></span><span class="sxs-lookup"><span data-stu-id="7ab80-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="7ab80-158">Veldu fjárhagslykill greiðslugetu sem er notaður fyrir sjóðsstreymisspá.</span><span class="sxs-lookup"><span data-stu-id="7ab80-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="7ab80-159">Þetta svæði er aðeins tiltækur þegar sjóðstreymisspá er virkjaður.</span><span class="sxs-lookup"><span data-stu-id="7ab80-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ab80-160"><strong>Fyrirframgreiðslur virðisaukaskatts</strong></span><span class="sxs-lookup"><span data-stu-id="7ab80-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="7ab80-161">Færið inn lykil fyrir virðisaukaskatt fyrir fyrirframgreiðslur.</span><span class="sxs-lookup"><span data-stu-id="7ab80-161">Select the account for sales tax payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Athugið" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="7ab80-163"><strong>Athugaðu</strong></span><span class="sxs-lookup"><span data-stu-id="7ab80-163"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7ab80-164">Bókunarreglan sem er notað þegar greiðslan er merkt sem fyrirframgreiðsla er valinn í reitnum fylgiskjal fyrirframgreiðslubókar í svæðinu Fjárhags og söluskattur á síðunni færibreytum viðskiptaskulda.</span><span class="sxs-lookup"><span data-stu-id="7ab80-164">The posting profile that is used when the payment is marked as a prepayment is selected in the Posting profile with prepayment journal voucher field in the Ledger and sales tax area of the Accounts payable parameters page.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7ab80-165"><strong>Koma</strong></span><span class="sxs-lookup"><span data-stu-id="7ab80-165"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="7ab80-166">Veldu fjárhagslykilsins sem upplýsingar um ósamþykkta reikningur lánardrottins er bókað í.</span><span class="sxs-lookup"><span data-stu-id="7ab80-166">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="7ab80-167">Upplýsingarnar eru færðar inn í komubók Reikninga.</span><span class="sxs-lookup"><span data-stu-id="7ab80-167">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="7ab80-168">Til dæmis, færir notandi grunnupplýsingar um lánardrottnareikninga þegar þær eru mótteknar í komubók.</span><span class="sxs-lookup"><span data-stu-id="7ab80-168">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="7ab80-169">Þegar komubókin er bókuð eru færslurnar bókaðar á lykil sem færður er inn hér og í svæðinu Mótlykill.</span><span class="sxs-lookup"><span data-stu-id="7ab80-169">When the invoice register is posted, the transactions are posted to the account that is entered here and in the Offset account field.</span></span> <span data-ttu-id="7ab80-170">Þegar reikningarnir eru samþykktir er skuldin flutt úr komulykillinn í safnlykil lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="7ab80-170">When the invoices are approved, the debt is transferred from the Arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7ab80-171"><strong>Mótlykill</strong></span><span class="sxs-lookup"><span data-stu-id="7ab80-171"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="7ab80-172">Veljið fjárhagslykilsins sem er notaður fyrir mótfærslu ósamþykktra lánardrottnareikninga sem eru uppfærðir í gegnum komubókina.</span><span class="sxs-lookup"><span data-stu-id="7ab80-172">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="7ab80-173">Mótfærslulykillinn virkar sem mótlykill fyrir færslur sem eru bókaðar í vörukomubók.</span><span class="sxs-lookup"><span data-stu-id="7ab80-173">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="7ab80-174">Þess vegna er inniheldur lykillinn innkaup lánardrottins sem hafa ekki verið samþykkt enn.</span><span class="sxs-lookup"><span data-stu-id="7ab80-174">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="7ab80-175">**Töflutakmarkanir**</span><span class="sxs-lookup"><span data-stu-id="7ab80-175">**Table restrictions**</span></span>

<span data-ttu-id="7ab80-176">Tilgreinið fyrir færslurnar með völdu bókunarreglunni hvort færslur verða jafnaðar sjálfkrafa, vexti reikna út og innheimtubréf gefin út.</span><span class="sxs-lookup"><span data-stu-id="7ab80-176">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="7ab80-177">Þú getur einnig valið reikning sem notaður er þegar færslur með valdri bókunarreglu er lokað.</span><span class="sxs-lookup"><span data-stu-id="7ab80-177">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="7ab80-178">Tilgreina eftirfarandi gildum til að setja upp bókunarreglunni :</span><span class="sxs-lookup"><span data-stu-id="7ab80-178">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="7ab80-179">Reitur</span><span class="sxs-lookup"><span data-stu-id="7ab80-179">Field</span></span>          | <span data-ttu-id="7ab80-180">Lýsing</span><span class="sxs-lookup"><span data-stu-id="7ab80-180">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ab80-181">**Uppgjör**</span><span class="sxs-lookup"><span data-stu-id="7ab80-181">**Settlement**</span></span> | <span data-ttu-id="7ab80-182">Veljið þennan valkost til að virkja sjálfvirka jöfnun fyrir færslur sem eru með þessari bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="7ab80-182">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="7ab80-183">Ef þessi valkostur er tóm þarftu að jafna færslur handvirkt með því að nota Jafna opnar færslur síðuna.</span><span class="sxs-lookup"><span data-stu-id="7ab80-183">If this option is cleared, you must manually settle transactions by using the Settle open transactions page.</span></span> |
| <span data-ttu-id="7ab80-184">**Hætta við**</span><span class="sxs-lookup"><span data-stu-id="7ab80-184">**Cancel**</span></span>     | <span data-ttu-id="7ab80-185">Veljið þennan valkost ef þú vilt geta hætt við færslur sem eru með þessari bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="7ab80-185">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="7ab80-186">**Loka**</span><span class="sxs-lookup"><span data-stu-id="7ab80-186">**Close**</span></span>      | <span data-ttu-id="7ab80-187">Tilgreinið bókunarreglu sem óskað er eftir að verði breytt yfir í þegar færslur með þessari bókunarreglu eru lokaðar.</span><span class="sxs-lookup"><span data-stu-id="7ab80-187">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="7ab80-188">Litið er á færslu sem lokaða þegar hún hefur verið jöfnuð að fullu.</span><span class="sxs-lookup"><span data-stu-id="7ab80-188">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |






