---
title: Bakfæra greiðslu lánardrottins
description: Þessi grein lýsir muninum á að bakfæra, eyða, ógilda og hafna greiðslu. Einnig útskýrir hún aðferðirnar tvær við að bakfæra ávísun lánardrottins.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankChequeTable, LedgerJournalTransBankChequeReversal, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14361
ms.assetid: 9f0a1883-cbe0-4cc7-b9f3-dd12fb85ebe8
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db9208c8e76d963d5b8f6bee6b7c73268af68734
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178354"
---
# <a name="reverse-a-vendor-payment"></a><span data-ttu-id="634c2-104">Bakfæra greiðslu lánardrottins</span><span class="sxs-lookup"><span data-stu-id="634c2-104">Reverse a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="634c2-105">Þessi grein lýsir muninum á að bakfæra, eyða, ógilda og hafna greiðslu.</span><span class="sxs-lookup"><span data-stu-id="634c2-105">This article describes the differences between reversing, deleting, voiding, and rejecting a payment.</span></span> <span data-ttu-id="634c2-106">Einnig útskýrir hún aðferðirnar tvær við að bakfæra ávísun lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="634c2-106">Additionally, it explains the two methods for reversing a vendor check.</span></span> 

<span data-ttu-id="634c2-107">Einstaka sinnum, eftir að greiðsla lánardrottins hefur verið bókuð, verður að bakfæra greiðsluna.</span><span class="sxs-lookup"><span data-stu-id="634c2-107">Occasionally, after a vendor payment has been posted, the payment must be reversed.</span></span> <span data-ttu-id="634c2-108">Bakfærsla er ólík eyðingu, ógildingu eða höfnun greiðslu.</span><span class="sxs-lookup"><span data-stu-id="634c2-108">Reversal differs from deleting, voiding, or rejecting a payment.</span></span> <span data-ttu-id="634c2-109">Aðeins er hægt að eyða greiðslu ef staða hennar er **Stofnað**.</span><span class="sxs-lookup"><span data-stu-id="634c2-109">You can delete a payment only if its status is **Created**.</span></span> <span data-ttu-id="634c2-110">Þessi staða tilgreinir að greiðslan hefur verið stofnuð en hefur ekki enn verið mynduð.</span><span class="sxs-lookup"><span data-stu-id="634c2-110">This status indicates that the payment has been created but hasn't yet been generated.</span></span> <span data-ttu-id="634c2-111">Þessi takmörkun gildir alltaf, óháð greiðsluaðferð.</span><span class="sxs-lookup"><span data-stu-id="634c2-111">This limitation always applies, regardless of the method of payment.</span></span> <span data-ttu-id="634c2-112">Hægt er að ógilda óbókaðar ávísanir eftir að þær hafa verið myndaðar en áður en þær hafa verið bókaðar.</span><span class="sxs-lookup"><span data-stu-id="634c2-112">You can void unposted checks after they have been generated but before they have been posted.</span></span> <span data-ttu-id="634c2-113">Ef mynduð greiðsla er gerð sem rafræn sjóðamillifærsla (EFT) er hægt að hafna greiðslu áður en hún er bókuð.</span><span class="sxs-lookup"><span data-stu-id="634c2-113">If the generated payment is done as an electronic fund transfer (EFT), you can reject the payment before it's posted.</span></span> <span data-ttu-id="634c2-114">Til að hafna greiðslu þarf að breyta gildinu **Greiðslustaða**.</span><span class="sxs-lookup"><span data-stu-id="634c2-114">To reject a payment, change the **Payment status** value.</span></span> <span data-ttu-id="634c2-115">Hægt er að endurmynda greiðslu sem hefur verið ógild eða hafnað eftir að gildinu **Greiðslustaða** er breytt til baka í **Ekkert**.</span><span class="sxs-lookup"><span data-stu-id="634c2-115">A payment that has been voided or rejected can be regenerated after the **Payment status** value is changed back to **None**.</span></span> 

<span data-ttu-id="634c2-116">Bakfærslur eru notaðar eftir að greiðsla er bókuð.</span><span class="sxs-lookup"><span data-stu-id="634c2-116">After a payment is posted, reversals are used.</span></span> <span data-ttu-id="634c2-117">Ekki er hægt að bakfæra rafrænar greiðslur eftir að þær hafa verið bókaðar.</span><span class="sxs-lookup"><span data-stu-id="634c2-117">Payments that are made electronically can't be reversed after they have been posted.</span></span> <span data-ttu-id="634c2-118">Í staðinn, verður að stofna nýja færslu fyrir upphæð greiðslu til að fá skuld aftur á reikning lánardrottins.</span><span class="sxs-lookup"><span data-stu-id="634c2-118">Instead, a new transaction must be created for the amount of the payment to get the liability back on the vendor's account.</span></span> <span data-ttu-id="634c2-119">Það eru tvær aðferðir til þess að bakfæra ávísanir.</span><span class="sxs-lookup"><span data-stu-id="634c2-119">There are two methods for reversing posted checks.</span></span> <span data-ttu-id="634c2-120">Í einni aðferð eru bakfærslur bókaðar strax þegar smellt er á **Greiðslubakfærsla** á síðunni **Ávísun**.</span><span class="sxs-lookup"><span data-stu-id="634c2-120">In one method, reversals are posted immediately when you click **Payment reversal** on the **Check** page.</span></span> <span data-ttu-id="634c2-121">Hin aðferðin er þannig að þegar smellt er á hnappinn **Greiðslubakfærsla** á síðunni **Ávísun** er bakfærslan fyrst send í færslubókina Reiðufjár- og bankastjórnun þar sem skoðunarmaður getur bókað eða hafnað bakfærslunni.</span><span class="sxs-lookup"><span data-stu-id="634c2-121">In the other method, when you click **Payment reversal** on the **Check** page, the reversal is sent to the check reversal journal in Cash and bank management, where a reviewer can then post or reject the reversal.</span></span> 

<span data-ttu-id="634c2-122">Til að fræðast um hvaða aðferð fyrirtækið notar skal skoða síðuna **Færibreytur reiðufjár- og bankastjórnunar**.</span><span class="sxs-lookup"><span data-stu-id="634c2-122">To learn which method your organization uses, view the **Cash and bank management parameters** page.</span></span> <span data-ttu-id="634c2-123">Ef valkosturinn **Nota endurskoðunarferlið fyrir greiðslubakfærslur** er stilltur á **Já** eru bakfærslur sendar í bakfærslubók til skoðunar.</span><span class="sxs-lookup"><span data-stu-id="634c2-123">If the **Use review process for payment reversals** option is set to **Yes**, reversals are sent to the check reversal journal for review.</span></span> <span data-ttu-id="634c2-124">Eftirfarandi tafla lýsir því hvernig mismunandi aðferðir til bakfærslu.</span><span class="sxs-lookup"><span data-stu-id="634c2-124">The following table describes how the check reversal methods differ.</span></span>

| <span data-ttu-id="634c2-125">Ef fyrirtækið fer ekki yfir bakfærslur ávísana áður en bókað er</span><span class="sxs-lookup"><span data-stu-id="634c2-125">If your organization doesn't review check reversals before posting</span></span>                                                                                                                                  | <span data-ttu-id="634c2-126">Ef fyrirtækið fer yfir bakfærslur ávísana áður en bókað er</span><span class="sxs-lookup"><span data-stu-id="634c2-126">If your organization reviews check reversals before posting</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="634c2-127">Ávísunin er bakfærð strax þegar smellt er á **Í lagi** á síðunni **Ávísun**.</span><span class="sxs-lookup"><span data-stu-id="634c2-127">The check is reversed immediately when you click **OK** on the **Check** page.</span></span>                                                                                                                      | <span data-ttu-id="634c2-128">Ávísunin er ekki strax bakfærð.</span><span class="sxs-lookup"><span data-stu-id="634c2-128">The check isn't immediately reversed.</span></span> <span data-ttu-id="634c2-129">Færslubók fyrir bakfærslu ávísana er stofnuð fyrir endurskoðun.</span><span class="sxs-lookup"><span data-stu-id="634c2-129">A check reversal journal is created for review.</span></span> <span data-ttu-id="634c2-130">Ef bakfærslubók er eytt er hægt að bakfæra ávísun aftur.</span><span class="sxs-lookup"><span data-stu-id="634c2-130">If the check reversal journal is deleted, the check can be reversed again.</span></span>                                                                                                                                                                                                                                                                |
| <span data-ttu-id="634c2-131">Bókhaldsfærslur fyrir upphaflega ávísunin er bakfærð.</span><span class="sxs-lookup"><span data-stu-id="634c2-131">The accounting entries for the original check are reversed.</span></span>                                                                                                                                         | <span data-ttu-id="634c2-132">Fjárhagslykillinn úr bókhaldsfærslu upprunalegrar ávísunar er hugsanlega ekki bókaður.</span><span class="sxs-lookup"><span data-stu-id="634c2-132">The ledger account from the original check's accounting entry might not be posted.</span></span> <span data-ttu-id="634c2-133">Fjárhagsvíddir úr færslubók upphaflegrar ávísuninar eru notaðar sem sjálfgefnar fjárhagsvíddir í færslubók fyrir bakfærslu ávísana.</span><span class="sxs-lookup"><span data-stu-id="634c2-133">The financial dimensions from the original check’s journal are used as the default financial dimensions on the check reversal journal.</span></span> <span data-ttu-id="634c2-134">Hægt er að breyta þessum sjálfgefnu gildum.</span><span class="sxs-lookup"><span data-stu-id="634c2-134">You can change these default values.</span></span> <span data-ttu-id="634c2-135">Þegar bakfærslubók er bókuð eru aðallyklar fyrir Viðskiptaskuldir færðir inn sjálfkrafa af bókunarreglunum, sem gætu hafa breyst.</span><span class="sxs-lookup"><span data-stu-id="634c2-135">When the check reversal journal is posted, the main accounts for Accounts payable are entered automatically from the posting profiles, which might have changed.</span></span> |
| <span data-ttu-id="634c2-136">Skipan bókhald sem var notaður þegar upprunalega ávísunin var bókuð er notuð til að bakfæra ávísun, jafnvel þótt lykilskipulagi hefur verið breytt.</span><span class="sxs-lookup"><span data-stu-id="634c2-136">The accounting structures that were used when the original check was posted are used to reverse the check, even if the account structure has been changed.</span></span> <span data-ttu-id="634c2-137">Lyklasamsetningin er ógild.</span><span class="sxs-lookup"><span data-stu-id="634c2-137">The account combination isn't validated.</span></span> | <span data-ttu-id="634c2-138">Ef lykilskipulagi breytt eftir að upphaflega ávísunin var bókaður, þarf hugsanlega nýja fjárhagsvídd fyrir bakfærslu ávísunar.</span><span class="sxs-lookup"><span data-stu-id="634c2-138">If an account structure changed after the original check was posted, a new financial dimension might be required for the reversal of the check.</span></span> <span data-ttu-id="634c2-139">Þessi fjárhagsvídd er hugsanlega ekki færð sjálfvirkt inn úr upphaflegri greiðslubók.</span><span class="sxs-lookup"><span data-stu-id="634c2-139">This financial dimension might not be entered automatically from the original payment's journal.</span></span> <span data-ttu-id="634c2-140">Samsetning lykils er villuleitað þegar bakfærsla ávísunar er bókuð.</span><span class="sxs-lookup"><span data-stu-id="634c2-140">The account combination is validated when the check reversal is posted.</span></span>                                                                                                        |
| <span data-ttu-id="634c2-141">Fastar víddir eru ekki notaðar á bakfærsluna til að aðstoða við að tryggja að sömu fjárhagslyklar séu bakfærðir.</span><span class="sxs-lookup"><span data-stu-id="634c2-141">Fixed dimensions aren't applied to the reversal, to help guarantee that the same ledger accounts are reversed.</span></span>                                                                                      | <span data-ttu-id="634c2-142">Fastar víddir notaðar bakfærslubók við bókun.</span><span class="sxs-lookup"><span data-stu-id="634c2-142">Fixed dimensions are applied to the check reversal journal during posting.</span></span> <span data-ttu-id="634c2-143">Fjárhagsvíddargildið hugsanlega ekki í lykilfærslu fyrir upprunaleg ávísun, eftir því hvenær föst vídd var skilgreind.</span><span class="sxs-lookup"><span data-stu-id="634c2-143">The financial dimension value might not exist in the accounting entry for the original check, depending on when the fixed dimension was defined.</span></span>                                                                                                                                                                                                     |

## <a name="reverse-posted-checks-without-reviewing-them"></a><span data-ttu-id="634c2-144">Bakfæra bókaðar ávísanir án þess að endurskoða þær</span><span class="sxs-lookup"><span data-stu-id="634c2-144">Reverse posted checks without reviewing them</span></span>
<span data-ttu-id="634c2-145">Ef fyrirtækið vill bóka bakfærslur ávísana strax þegar smellt er á **Greiðslubakfærsla** á síðunni **Ávísanir**.</span><span class="sxs-lookup"><span data-stu-id="634c2-145">If your organization wants to post check reversals immediately when you click **Payment reversal** on the **Checks** page.</span></span> <span data-ttu-id="634c2-146">Á síðunni **Færibreytur reiðufjár- og bankastjórnunar** skal stilla valkostinn **Nota endurskoðunarferlið fyrir greiðslubakfærslur** á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="634c2-146">On the **Cash and bank management parameters** page, set the **Use review process for payment reversals** option to **No**.</span></span> <span data-ttu-id="634c2-147">Á síðunni **Ávísanir** er hægt að velja ávísun til að bakfæra og velja **Greiðslubakfærsla**.</span><span class="sxs-lookup"><span data-stu-id="634c2-147">On the **Checks** page, you can select the check to reverse and select **Payment reversal**.</span></span> <span data-ttu-id="634c2-148">Síðan er hægt að færa inn dagsetninguna og ástæðu bakfærslunnar.</span><span class="sxs-lookup"><span data-stu-id="634c2-148">You can then enter the date, and select a reason for the reversal.</span></span>

## <a name="reverse-posted-checks-after-they-are-reviewed-in-the-check-reversal-journal"></a><span data-ttu-id="634c2-149">Bakfæra bókaðar ávísanir eftir að þær eru endurskoðaðar í bakfærslubók ávísana</span><span class="sxs-lookup"><span data-stu-id="634c2-149">Reverse posted checks after they are reviewed in the check reversal journal</span></span>
<span data-ttu-id="634c2-150">Ef fyrirtækið vill að fara yfir bakfærslur ávísana áður en þær eru bókaðar skal stofna í bakfærslubók fyrir yfirferð og á síðunni **Færibreytur reiðufjár- og bankastjórnunar** og stilla valkostinn **Nota endurskoðunarferlið fyrir greiðslubakfærslur** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="634c2-150">If your organization wants to review check reversals before they are posted, create a check reversal journal for review and on the **Cash and bank management parameters** page, set the **Use review process for payment reversals** option to **Yes**.</span></span> <span data-ttu-id="634c2-151">Á síðunni **Ávísanir** er hægt að velja ávísun til að bakfæra og velja **Greiðslubakfærsla**.</span><span class="sxs-lookup"><span data-stu-id="634c2-151">On the **Checks** page, you can select check to reverse, select **Payment reversal**.</span></span> <span data-ttu-id="634c2-152">Síðan er hægt að færa inn dagsetninguna og ástæðu bakfærslunnar.</span><span class="sxs-lookup"><span data-stu-id="634c2-152">You can then enter the date, and select a reason for the reversal.</span></span> <span data-ttu-id="634c2-153">Setja verður upp fjárhagsástæðuna fyrir bæði banka- og lánardrottnaaðila.</span><span class="sxs-lookup"><span data-stu-id="634c2-153">The financial reason must be set up for both Bank and Vendor types.</span></span> <span data-ttu-id="634c2-154">Einnig verður að velja færslubókarheiti til að stofna færslubók í færslubók fyrir bakfærslu ávísana.</span><span class="sxs-lookup"><span data-stu-id="634c2-154">You must also select a journal name to create a journal in the check reversal journal.</span></span>

### <a name="review-a-reversal"></a><span data-ttu-id="634c2-155">Skoða bakfærslu</span><span class="sxs-lookup"><span data-stu-id="634c2-155">Review a reversal</span></span>

<span data-ttu-id="634c2-156">Ef þú ert notandi sem á að skoða bakfærslur geturðu annaðhvort samþykkt og bókað færslubókina eða hafnað bakfærslunni með því að eyða færslubókinni.</span><span class="sxs-lookup"><span data-stu-id="634c2-156">If you're a user who must review reversals, You can either approve and post the journal, or reject the reversal by deleting the journal.</span></span> <span data-ttu-id="634c2-157">Á síðunni **Færslubók fyrir bakfærslu ávísana** er hægt að velja bakfærslubókina sem á að endurskoða og smellið síðan á **Línur**.</span><span class="sxs-lookup"><span data-stu-id="634c2-157">On the **Check reversals journal** page, you can select the reversal journal to review, and then click **Lines**.</span></span> <span data-ttu-id="634c2-158">Hægt er að skoða bakfærða ávísun og velja síðan einn af eftirfarandi samþykktarkostum:</span><span class="sxs-lookup"><span data-stu-id="634c2-158">You can review the reversed check, and then select one of the following approval options:</span></span>

-   <span data-ttu-id="634c2-159">Til að samþykkja og bóka bakfærslubókina er smellt á **Bóka** eða **Bóka og millifæra**.</span><span class="sxs-lookup"><span data-stu-id="634c2-159">To approve and post the reversal journal, click **Post** or **Post and transfer**.</span></span>
-   <span data-ttu-id="634c2-160">Ef hafna á bakfærslu er bakfærslulínunni eytt.</span><span class="sxs-lookup"><span data-stu-id="634c2-160">To reject the reversal, delete the reversal check journal.</span></span>

> [!NOTE]
> <span data-ttu-id="634c2-161">Ef færslubókinni er eytt er bakfærslan fjarlægð úr kerfinu en upphaflega ávísunin er áfram í skjámyndinni **Ávísun**.</span><span class="sxs-lookup"><span data-stu-id="634c2-161">If you delete the journal, the reversal is removed from the system, but the original check remains on the **Check** page.</span></span> <span data-ttu-id="634c2-162">Staða ávísunarinnar er ekki lengur **Bíður afturköllunar**.</span><span class="sxs-lookup"><span data-stu-id="634c2-162">The status of the check is no longer **Pending cancellation**.</span></span>

## <a name="results-of-posting-a-reversal"></a><span data-ttu-id="634c2-163">Niðurstaða af bókun bakfærslu</span><span class="sxs-lookup"><span data-stu-id="634c2-163">Results of posting a reversal</span></span>
<span data-ttu-id="634c2-164">Þegar bakfærsla ávísunar er bókuð gerist eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="634c2-164">When you post a check reversal, the following events occur:</span></span>

-   <span data-ttu-id="634c2-165">Staða ávísunarinnar er uppfærð í **Afturköllun**.</span><span class="sxs-lookup"><span data-stu-id="634c2-165">The check status is updated to **Cancellation**.</span></span>
-   <span data-ttu-id="634c2-166">Ef gátreiturinn **Afstemma** var valinn í bakfærsluskjámyndinni við bakfærsluna er ávísunin stemmd af (gátreiturinn **Afstemmt** er valinn) og verður ekki birt í skjámyndinni **Lykilafstemming**.</span><span class="sxs-lookup"><span data-stu-id="634c2-166">If the **Reconcile** option was selected on the reversal page during the reversal, the check is reconciled (the **Reconciled** option is selected) and doesn't appear on the **Account reconciliation** page.</span></span>
-   <span data-ttu-id="634c2-167">Fylgiskjal bakfærslunnar er bókað á móti bankareikningnum sem ávísunin var gefin út af, til að hækka stöðu bankareikningsins.</span><span class="sxs-lookup"><span data-stu-id="634c2-167">The reversal voucher is posted against the bank account that the check was issued from, to increase the bank account balance.</span></span>
-   <span data-ttu-id="634c2-168">Fylgiskjalið er bókað í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="634c2-168">The voucher is posted to General ledger.</span></span>
-   <span data-ttu-id="634c2-169">Breytingarupplýsingarnar eru uppfærðar í reitaflokknum **Saga** á síðunni **Ávísun**.</span><span class="sxs-lookup"><span data-stu-id="634c2-169">The modification details are updated in the **History** field group on the **Check** page.</span></span>

> [!NOTE] 
> <span data-ttu-id="634c2-170">Þegar ávísun sem var gefin út vegna samstæðuviðskiptafærslu er bakfærð koma mótfærslurnar úr bókhaldsuppsetningu fyrir samstæðuviðskiptin, ekki úr upphaflegu færslunni.</span><span class="sxs-lookup"><span data-stu-id="634c2-170">When you reverse a check that was issued for an intercompany trade transaction, the offsetting entries come from the accounting setup for intercompany trade, not from the original transaction.</span></span> <span data-ttu-id="634c2-171">Ef ávísunin sem var bakfærð var gefin út vegna greiðslu til lánardrottins gerist einnig eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="634c2-171">If the check that was reversed was issued for a vendor payment, the following events also occur:</span></span>

-   <span data-ttu-id="634c2-172">Upphaflega greiðslan úr reikningnum sem greiðslan var jöfnuð á móti er ófærð (jöfnunin er bakfærð).</span><span class="sxs-lookup"><span data-stu-id="634c2-172">The original payment from the invoice that the payment was settled against is unapplied (the settlement is reversed).</span></span>
-   <span data-ttu-id="634c2-173">Færsla er bókuð á lánardrottnalykill vegna greiðslubakfærslunnar og bakfærða greiðslan er jöfnuð á móti upphaflegu greiðslunni.</span><span class="sxs-lookup"><span data-stu-id="634c2-173">A transaction is posted against the vendor account for the payment reversal, and the reversed payment is settled against the original payment.</span></span> <span data-ttu-id="634c2-174">Reiturinn **Síðasta uppgjörsfylgiskjal** í skjámyndinni **Lánardrottnafærslur** fyrir upphaflegu lánardrottinsgreiðsluna er uppfærður svo að hann sýni fylgiskjalsnúmer bakfærðu færslunnar.</span><span class="sxs-lookup"><span data-stu-id="634c2-174">The **Last settlement voucher** field on the **Vendor transactions** page for the original vendor disbursement is updated to reflect the voucher number of the reversed transaction.</span></span>

<span data-ttu-id="634c2-175">Ef ávísunin sem var bakfærð var gefin út vegna endurgreiðslu viðskiptavinar gerist einnig eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="634c2-175">If the check that was reversed was issued for a customer refund, the following events also occur:</span></span>

-   <span data-ttu-id="634c2-176">Færsla er bókuð á mótiviðskiptavinalykill vegna greiðslubakfærslunnar og jöfnunin milli upphaflegu greiðslunnar og skjalsins sem greiðslan var upphaflega jöfnuð á móti er bakfærð (neikvæð greiðsla er stofnuð).</span><span class="sxs-lookup"><span data-stu-id="634c2-176">A transaction is posted against the customer account for the payment reversal, and the settlement between the original payment and the document that the payment was originally settled against is reversed (a negative payment is created).</span></span>
-   <span data-ttu-id="634c2-177">Bakfærslu á greiðslu er jafnað við upphaflegu greiðsluna.</span><span class="sxs-lookup"><span data-stu-id="634c2-177">A payment reversal is applied to the original payment.</span></span> <span data-ttu-id="634c2-178">Reiturinn **Síðasta uppgjörsfylgiskjal** á síðunni **Færslur viðskiptavina** fyrir upphaflegu lánardrottinsgreiðsluna er uppfærður svo að hann sýni fylgiskjalsnúmer bakfærðu færslunnar.</span><span class="sxs-lookup"><span data-stu-id="634c2-178">The **Last settlement voucher** field on the **Customer transactions** page for the original customer payment is updated to reflect the voucher number of the reversed transaction.</span></span>



