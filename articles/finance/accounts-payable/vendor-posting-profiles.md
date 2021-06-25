---
title: Bókunarreglur lánardrottna
description: Bókunarreglur lánardrottins stýra bókun á færslum lánardrottins í fjárhag.
author: abruer
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4b38fd137e6479493da79d4b62d0111b502a632
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189494"
---
# <a name="vendor-posting-profiles"></a><span data-ttu-id="be8b0-103">Bókunarreglur lánardrottna</span><span class="sxs-lookup"><span data-stu-id="be8b0-103">Vendor posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be8b0-104">Bókunarreglur lánardrottins stýra bókun á færslum lánardrottins í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="be8b0-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

## <a name="vendor-posting-profiles"></a><span data-ttu-id="be8b0-105">Bókunarreglur lánardrottna</span><span class="sxs-lookup"><span data-stu-id="be8b0-105">Vendor posting profiles</span></span>

<span data-ttu-id="be8b0-106">Bókunarreglur lánardrottina gera þér kleift að úthluta fjárhagslyklum og skjalastillingum á alla lánardrottna, hóp af lánardrottnum eða einn lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="be8b0-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors, or a single vendor.</span></span> <span data-ttu-id="be8b0-107">Þessar stillingar verður notaðar þegar þú stofnar innkaupapantanir, lánardrottnalykla og staðgreiðslur.</span><span class="sxs-lookup"><span data-stu-id="be8b0-107">These settings will be used when you create purchase orders, vendor invoices, and cash payments.</span></span> <span data-ttu-id="be8b0-108">Fyrir sumar færslur geturðu valið bókunarreglu sem er frábrugðin og sem hefur forgang fram yfir bókunarregluna sem er sett upp fyrir færslur í þessar skjámynd.</span><span class="sxs-lookup"><span data-stu-id="be8b0-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions on this page.</span></span> <span data-ttu-id="be8b0-109">Sjálfgefin bókunarregla er skilgreind á flýtiflipanum **Fjárhagur og Virðisaukaskattur** á síðunni **Færibreytur viðskiptaskulda**.</span><span class="sxs-lookup"><span data-stu-id="be8b0-109">The default posting profile is defined on the **Ledger and Sales Tax** FastTab on the **Accounts payable parameters** page.</span></span> <span data-ttu-id="be8b0-110">Sjálfgefin bókunarregla er síðan sjálfvirkt tekin með í haus nýrra skjala þar sem hægt er að breyta henni í aðra bókunarreglu ef þörf krefur.</span><span class="sxs-lookup"><span data-stu-id="be8b0-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile, if needed.</span></span>

<span data-ttu-id="be8b0-111">Einnig er hægt að tengja bókunarskilgreiningar við færslubókunargerð á síðunni **Skilgreiningar færslubókana**.</span><span class="sxs-lookup"><span data-stu-id="be8b0-111">You can also associate posting definitions with transaction posting types on the **Transaction posting definitions** page.</span></span> <span data-ttu-id="be8b0-112">Bókunarskilgreining stýra bókun á lánardrottnafærslum í fjárhag í stað bókunarskilgreininga.</span><span class="sxs-lookup"><span data-stu-id="be8b0-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="be8b0-113">Stofnun Bókunarregla</span><span class="sxs-lookup"><span data-stu-id="be8b0-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="be8b0-114">**Uppsetning**</span><span class="sxs-lookup"><span data-stu-id="be8b0-114">**Setup**</span></span>

<span data-ttu-id="be8b0-115">Tilgreinið fjárhagslyklana sem eru notaðir við bókun færsla sem nota valda bókunarreglunni.</span><span class="sxs-lookup"><span data-stu-id="be8b0-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="be8b0-116">Veljið reikningskóða og þegar hægt er reiknings- eða flokkanúmer fyrir valda bókunarfærslu.</span><span class="sxs-lookup"><span data-stu-id="be8b0-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="be8b0-117">Í bókunarferlinu er sú bókunarregla sem er mest viðeigandi fyrir hverja færslu fundin með því að leita að afmörkuðustu reikningskóða-, reikningsnúmera- eða flokkanúmerasamsetningu í eftirfarandi forgangi.</span><span class="sxs-lookup"><span data-stu-id="be8b0-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority.</span></span>

| <span data-ttu-id="be8b0-118">**Lykilkóði** svæðisgildið</span><span class="sxs-lookup"><span data-stu-id="be8b0-118">**Account code** field value</span></span> | <span data-ttu-id="be8b0-119">**Númer lykils/Flokks** svæðisgildið</span><span class="sxs-lookup"><span data-stu-id="be8b0-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="be8b0-120">Forgangsröðun leitar</span><span class="sxs-lookup"><span data-stu-id="be8b0-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="be8b0-121">**Tafla**</span><span class="sxs-lookup"><span data-stu-id="be8b0-121">**Table**</span></span>                    | <span data-ttu-id="be8b0-122">Tilgreindur lánardrottnareikningur</span><span class="sxs-lookup"><span data-stu-id="be8b0-122">Specific vendor account</span></span>                     | <span data-ttu-id="be8b0-123">1</span><span class="sxs-lookup"><span data-stu-id="be8b0-123">1</span></span>               |
| <span data-ttu-id="be8b0-124">**Hópur**</span><span class="sxs-lookup"><span data-stu-id="be8b0-124">**Group**</span></span>                    | <span data-ttu-id="be8b0-125">Lánardrottnahópur sem er úthlutað á lánardrottinn</span><span class="sxs-lookup"><span data-stu-id="be8b0-125">Vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="be8b0-126">2</span><span class="sxs-lookup"><span data-stu-id="be8b0-126">2</span></span>               |
| <span data-ttu-id="be8b0-127">**Öll**</span><span class="sxs-lookup"><span data-stu-id="be8b0-127">**All**</span></span>                      | <span data-ttu-id="be8b0-128">Autt</span><span class="sxs-lookup"><span data-stu-id="be8b0-128">Blank</span></span>                                       | <span data-ttu-id="be8b0-129">3</span><span class="sxs-lookup"><span data-stu-id="be8b0-129">3</span></span>               |

<span data-ttu-id="be8b0-130">Ef þú vilt að allar lánardrottnafærslur hafi sömu bókunarregluna skaltu aðeins setja upp eina bókunarreglu með **Allt** í reitinn **Reikningskóði**.</span><span class="sxs-lookup"><span data-stu-id="be8b0-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with **All** in the **Account code** field.</span></span> <span data-ttu-id="be8b0-131">Tilgreindu eftirfarandi gildi til að setja upp bókunarregluna.</span><span class="sxs-lookup"><span data-stu-id="be8b0-131">Specify the following values to set up your posting profile.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="be8b0-132">Svæði</span><span class="sxs-lookup"><span data-stu-id="be8b0-132">Field</span></span></th>
<th><span data-ttu-id="be8b0-133">Lýsing</span><span class="sxs-lookup"><span data-stu-id="be8b0-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="be8b0-134"><strong>Bókunarregla</strong></span><span class="sxs-lookup"><span data-stu-id="be8b0-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="be8b0-135">Færið inn kóða fyrir bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="be8b0-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="be8b0-136">T.d. væri hægt að útbúa tvær bókunarreglur til að fá einn lykil fyrir lánardrottnastöður í landsgjaldmiðlinum og annan fyrir lánardrottnastöður í erlendum gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="be8b0-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="be8b0-137">Hægt væri að kalla annan lykilinn „Lands“ og hinn „Erlendur“.</span><span class="sxs-lookup"><span data-stu-id="be8b0-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be8b0-138"><strong>Lýsing</strong></span><span class="sxs-lookup"><span data-stu-id="be8b0-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="be8b0-139">Færa skal inn lýsingu á bókunarregla.</span><span class="sxs-lookup"><span data-stu-id="be8b0-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be8b0-140"><strong>Kóði lykils</strong></span><span class="sxs-lookup"><span data-stu-id="be8b0-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="be8b0-141">Tilgreinið hvort bókunarreglan eigi við um einstakan lánardrottinn, flokk af lánardrottnum eða alla lánardrottna:</span><span class="sxs-lookup"><span data-stu-id="be8b0-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="be8b0-142"><strong>Taflan</strong> – bókunarregla við einn lánardrottinn.</span><span class="sxs-lookup"><span data-stu-id="be8b0-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="be8b0-143">Veldu lánardrottnalykil í reitnum <strong>Númer lykils/flokks</strong>.</span><span class="sxs-lookup"><span data-stu-id="be8b0-143">Select the vendor account in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="be8b0-144"><strong>Taflan</strong> – bókunarregla á við einn lánardrottnaflokk.</span><span class="sxs-lookup"><span data-stu-id="be8b0-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="be8b0-145">Veljið lánardrottnaflokkur í reitnum <strong>Númer lykils/flokks</strong>.</span><span class="sxs-lookup"><span data-stu-id="be8b0-145">Select the vendor group in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="be8b0-146"><strong>Allt</strong> – bókunarregla á við alla lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="be8b0-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="be8b0-147">Látið reitinn <strong>Númer lykils/flokks</strong> vera autt.</span><span class="sxs-lookup"><span data-stu-id="be8b0-147">Leave the <strong>Account/Group number</strong> field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="be8b0-148"><strong>Númer lykils/flokks</strong></span><span class="sxs-lookup"><span data-stu-id="be8b0-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="be8b0-149">Ef <strong>Tafla</strong> er valin í reitnum <strong>Lykilkóði</strong> veljið þá lykilnúmer lánardrottins sem er tengdur við bókunarregluna.</span><span class="sxs-lookup"><span data-stu-id="be8b0-149">If <strong>Table</strong> is selected in the <strong>Account code</strong> field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="be8b0-150">Ef valinn er <strong>Flokkur</strong> skaltu velja flokk lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="be8b0-150">If <strong>Group</strong> is selected, select a vendor group.</span></span> <span data-ttu-id="be8b0-151">Ef <strong>Allt</strong> er valið skal skilja þenan reit eftir auðan.</span><span class="sxs-lookup"><span data-stu-id="be8b0-151">If <strong>All</strong> is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be8b0-152"><strong>Safnlykill</strong></span><span class="sxs-lookup"><span data-stu-id="be8b0-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="be8b0-153">Veljið fjárhagslykilinn sem nota á sem safnlykil fyrir lánardrottna sem bókunarreglan er tengd.</span><span class="sxs-lookup"><span data-stu-id="be8b0-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span> <span data-ttu-id="be8b0-154">Færibreytan <strong>Ekki leyfa handvirka færslu</strong> fyrir þennan aðalreikning verður merkt.</span><span class="sxs-lookup"><span data-stu-id="be8b0-154">The <strong>Do not allow manual entry</strong> parameter for this main account will be marked.</span></span> <span data-ttu-id="be8b0-155">Ef þú fjarlægir síðan þennan reikning úr pósti skaltu staðfesta stillinguna <strong>Ekki leyfa handvirka færslu</strong> á síðunni <strong>Aðalreikningar</strong>.</span><span class="sxs-lookup"><span data-stu-id="be8b0-155">If you subsequently remove this account from the posting profile, validate the <strong>Do not allow manual entry</strong> setting on the <strong>Main accounts</strong> page.</span></span> 
<p><span data-ttu-id="be8b0-156"><strong>Ath.:</strong> Ef valkosturinn <strong>Nota bókunarskilgreiningar</strong> er valinn á síðunni <strong>Færibreytur fjárhags</strong> er færslubókunarskilgreining fyrir reikningur lánardrottins notað í stað samantektarlykils.</span><span class="sxs-lookup"><span data-stu-id="be8b0-156"><strong>Note:</strong> If the <strong>Use posting definitions</strong> option is selected on the <strong>General ledger parameters</strong> page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="be8b0-157"><strong>Jafna lykil</strong></span><span class="sxs-lookup"><span data-stu-id="be8b0-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="be8b0-158">Veldu fjárhagslykill greiðslugetu sem er notaður fyrir sjóðsstreymisspá.</span><span class="sxs-lookup"><span data-stu-id="be8b0-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="be8b0-159">Þetta svæði er aðeins tiltækur þegar sjóðstreymisspá er virkjaður.</span><span class="sxs-lookup"><span data-stu-id="be8b0-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be8b0-160"><strong>Fyrirframgreiðslur virðisaukaskatts</strong></span><span class="sxs-lookup"><span data-stu-id="be8b0-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="be8b0-161">Færið inn lykil fyrir virðisaukaskatt fyrir fyrirframgreiðslur.</span><span class="sxs-lookup"><span data-stu-id="be8b0-161">Select the account for sales tax payments that are received in advance.</span></span>
<p><span data-ttu-id="be8b0-162"><strong>Ath.:</strong> Bókunarreglan sem er notuð þegar greiðslan er merkt sem fyrirframgreiðsla er valin í reitnum <strong>Bókun</strong> með reitnum <strong>Fylgiskjal fyrirframgreiðslubókar</strong> á svæðinu <strong>Fjárhags og söluskattur</strong> á síðunni <strong>Færibreytur viðskiptaskulda</strong>.</span><span class="sxs-lookup"><span data-stu-id="be8b0-162"><strong>Note:</strong> The posting profile that is used when the payment is marked as a prepayment is selected in the <strong>Posting</strong> profile with <strong>Prepayment journal voucher</strong> field in the <strong>Ledger and sales tax</strong> area on the <strong>Accounts payable parameters</strong> page.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="be8b0-163"><strong>Koma</strong></span><span class="sxs-lookup"><span data-stu-id="be8b0-163"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="be8b0-164">Veldu fjárhagslykilsins sem upplýsingar um ósamþykkta reikningur lánardrottins er bókað í.</span><span class="sxs-lookup"><span data-stu-id="be8b0-164">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="be8b0-165">Upplýsingarnar eru færðar inn í komubók Reikninga.</span><span class="sxs-lookup"><span data-stu-id="be8b0-165">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="be8b0-166">Til dæmis, færir notandi grunnupplýsingar um lánardrottnareikninga þegar þær eru mótteknar í komubók.</span><span class="sxs-lookup"><span data-stu-id="be8b0-166">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="be8b0-167">Þegar komubókin er bókuð eru færslurnar bókaðar á lykil sem færður er inn hér og í reitnum <strong>Mótlykill</strong>.</span><span class="sxs-lookup"><span data-stu-id="be8b0-167">When the invoice register is posted, the transactions are posted to the account that is entered here and in the <strong>Offset account</strong> field.</span></span> <span data-ttu-id="be8b0-168">Þegar reikningarnir eru samþykktir er skuldin flutt úr komulykillinn í safnlykil lánardrottna.</span><span class="sxs-lookup"><span data-stu-id="be8b0-168">When the invoices are approved, the debt is transferred from the arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="be8b0-169"><strong>Mótlykill</strong></span><span class="sxs-lookup"><span data-stu-id="be8b0-169"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="be8b0-170">Veljið fjárhagslykilsins sem er notaður fyrir mótfærslu ósamþykktra lánardrottnareikninga sem eru uppfærðir í gegnum komubókina.</span><span class="sxs-lookup"><span data-stu-id="be8b0-170">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="be8b0-171">Mótfærslulykillinn virkar sem mótlykill fyrir færslur sem eru bókaðar í vörukomubók.</span><span class="sxs-lookup"><span data-stu-id="be8b0-171">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="be8b0-172">Þess vegna er inniheldur lykillinn innkaup lánardrottins sem hafa ekki verið samþykkt enn.</span><span class="sxs-lookup"><span data-stu-id="be8b0-172">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="be8b0-173">**Töflutakmarkanir**</span><span class="sxs-lookup"><span data-stu-id="be8b0-173">**Table restrictions**</span></span>

<span data-ttu-id="be8b0-174">Tilgreinið fyrir færslurnar með völdu bókunarreglunni hvort færslur verða jafnaðar sjálfkrafa, vexti reikna út og innheimtubréf gefin út.</span><span class="sxs-lookup"><span data-stu-id="be8b0-174">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="be8b0-175">Þú getur einnig valið reikning sem notaður er þegar færslur með valdri bókunarreglu er lokað.</span><span class="sxs-lookup"><span data-stu-id="be8b0-175">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="be8b0-176">Tilgreindu eftirfarandi gildi til að setja upp bókunarregluna</span><span class="sxs-lookup"><span data-stu-id="be8b0-176">Specify the following values to set up your posting profile</span></span>

| <span data-ttu-id="be8b0-177">Svæði</span><span class="sxs-lookup"><span data-stu-id="be8b0-177">Field</span></span>          | <span data-ttu-id="be8b0-178">Lýsing</span><span class="sxs-lookup"><span data-stu-id="be8b0-178">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be8b0-179">**Jöfnun**</span><span class="sxs-lookup"><span data-stu-id="be8b0-179">**Settlement**</span></span> | <span data-ttu-id="be8b0-180">Veljið þennan valkost til að virkja sjálfvirka jöfnun fyrir færslur sem eru með þessari bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="be8b0-180">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="be8b0-181">Ef þessi valkostur er tómur þarftu að jafna færslur handvirkt með því að nota síðuna **Jafna opnar færslur**.</span><span class="sxs-lookup"><span data-stu-id="be8b0-181">If this option is cleared, you must manually settle transactions by using the **Settle open transactions** page.</span></span> |
| <span data-ttu-id="be8b0-182">**Hætta við**</span><span class="sxs-lookup"><span data-stu-id="be8b0-182">**Cancel**</span></span>     | <span data-ttu-id="be8b0-183">Veljið þennan valkost ef þú vilt geta hætt við færslur sem eru með þessari bókunarreglu.</span><span class="sxs-lookup"><span data-stu-id="be8b0-183">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="be8b0-184">**Loka**</span><span class="sxs-lookup"><span data-stu-id="be8b0-184">**Close**</span></span>      | <span data-ttu-id="be8b0-185">Tilgreinið bókunarreglu sem óskað er eftir að verði breytt yfir í þegar færslur með þessari bókunarreglu eru lokaðar.</span><span class="sxs-lookup"><span data-stu-id="be8b0-185">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="be8b0-186">Litið er á færslu sem lokaða þegar hún hefur verið jöfnuð að fullu.</span><span class="sxs-lookup"><span data-stu-id="be8b0-186">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]