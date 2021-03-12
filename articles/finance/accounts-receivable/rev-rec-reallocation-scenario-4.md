---
title: Endurúthlutun tekjuskráningar – Aðstæður 4
description: Þetta efnisatriði fer í gegnum aðstæður endurúthlutunar þar sem lína er fjarlægð úr fyrirliggjandi sölupöntun sem er reikningsfærð að hluta til. Þessar aðstæður leiða til sömu niðurstöðu burtséð frá því hvort línan er fjarlægð úr sölupöntuninni eða fær stöðu afturköllunar.
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 500c7817795448d7d9759c4ad7a1842df0a9bdc5
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003281"
---
# <a name="revenue-recognition-reallocation--scenario-4"></a><span data-ttu-id="aed8d-104">Endurúthlutun tekjuskráningar – Aðstæður 4</span><span class="sxs-lookup"><span data-stu-id="aed8d-104">Revenue recognition reallocation – Scenario 4</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aed8d-105">Þetta efnisatriði fer í gegnum aðstæður endurúthlutunar þar sem lína er fjarlægð úr fyrirliggjandi sölupöntun sem er reikningsfærð að hluta til.</span><span class="sxs-lookup"><span data-stu-id="aed8d-105">This topic goes through a reallocation scenario where a line is removed from an existing, partially invoiced sales order.</span></span> <span data-ttu-id="aed8d-106">Þessar aðstæður leiða til sömu niðurstöðu burtséð frá því hvort línan er fjarlægð úr sölupöntuninni eða fær stöðu afturköllunar.</span><span class="sxs-lookup"><span data-stu-id="aed8d-106">This scenario produces the same result, regardless of whether the line is removed from the sales order or set to a canceled status.</span></span>

<span data-ttu-id="aed8d-107">Í þessum aðstæðum er valkosturinn **Bóka leiðréttingar reiknings á viðskiptakröfur** stilltur á **Nei** í flipanum **Tekjuskráning** á síðunni **Fjárhagsfæribreytur** (**Tekjuskráning \> Uppsetning \> Fjárhagsfæribreytur**).</span><span class="sxs-lookup"><span data-stu-id="aed8d-107">For this scenario, the **Post invoice corrections to Accounts receivable** option is set to **No** on the **Revenue recognition** tab of the **General ledger parameters** page (**Revenue recognition \> Setup \> General ledger parameters**).</span></span>

<span data-ttu-id="aed8d-108">[![Bóka leiðréttingar reikningum á valkostinn viðskiptakröfur stillt á Nei](./media/37_rev-rec-scenarios.png)](./media/37_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="aed8d-108">[![Post invoice corrections to Accounts receivable option set to No](./media/37_rev-rec-scenarios.png)](./media/37_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="aed8d-109">Sölupöntun er stofnuð fyrir viðskiptavin US\_SI\_0003.</span><span class="sxs-lookup"><span data-stu-id="aed8d-109">A sales order is created for customer US\_SI\_0003.</span></span> <span data-ttu-id="aed8d-110">Viðskiptavinurinn er að kaupa fartölvu (vörunúmer S0012), uppsetningarþjónustu (vörunúmer S0001) og þjónustuáætlun fyrir fartölvuna (vörunúmer 0008, „Viðvarandi tækniþjónustu“).</span><span class="sxs-lookup"><span data-stu-id="aed8d-110">The customer is purchasing a laptop (item number S0012), installation services (item number S0001), and a support plan for the laptop (item number S0008, "Sustained Engineering Service").</span></span> <span data-ttu-id="aed8d-111">Tekjur fyrir fartölvuna og uppsetningarþjónustuna eru skráðar um leið.</span><span class="sxs-lookup"><span data-stu-id="aed8d-111">The revenue for the laptop and installation services is immediately recognized.</span></span> <span data-ttu-id="aed8d-112">Tekjum fyrir þjónustuáætlunina verður seinkað og þær skráðar yfir 12 mánaða eins og það er skilgreint af tímabilinu í samningnum.</span><span class="sxs-lookup"><span data-stu-id="aed8d-112">The revenue for the support plan will be deferred and recognized over 12 months, as defined by the date range in the contract.</span></span>

<span data-ttu-id="aed8d-113">[![Sölupöntunarlínur fyrir fartölvu, uppsetningarþjónustu og þjónustuáætlun](./media/38_rev-rec-scenarios.png)](./media/38_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="aed8d-113">[![Sales order lines for the laptop, installation services, and support plan](./media/38_rev-rec-scenarios.png)](./media/38_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="aed8d-114">Sölupöntunin er staðfest.</span><span class="sxs-lookup"><span data-stu-id="aed8d-114">The sales order is confirmed.</span></span> <span data-ttu-id="aed8d-115">Þar sem öll þrjú atriðin voru sett upp fyrir endurúthlutun tekjuupphæðar er tekjuupphæð reiknuð þegar sölupöntun er staðfest.</span><span class="sxs-lookup"><span data-stu-id="aed8d-115">Because all three items are set up for revenue price allocation, the revenue price is calculated when the sales order is confirmed.</span></span> <span data-ttu-id="aed8d-116">Hægt er að skoða tekjurnar sem verða skráðar á síðunni **Úthlutun á tekjuupphæð** (á síðunni **Sölupöntun**, í aðgerðasvæðinu, í flipanum **Stjórna**, í flokknum **Tekjuskráning** skal velja **Úthlutun á tekjuupphæð**).</span><span class="sxs-lookup"><span data-stu-id="aed8d-116">You can view the revenue that will be recognized on the **Revenue price allocation** page (on the **Sales order** page, on the Action Pane, on the **Manage** tab, in the **Revenue recognition** group, select **Revenue price allocation**).</span></span> <span data-ttu-id="aed8d-117">Tekjur fyrir fartölvuna verða bókaðar á tekjulykil að upphæð $995,84.</span><span class="sxs-lookup"><span data-stu-id="aed8d-117">The revenue for the laptop will be posted to the Revenue account in the amount of $995.84.</span></span> <span data-ttu-id="aed8d-118">Tekjur fyrir uppsetningarþjónustuna verða einnig bókaðar á tekjulykil að upphæð $314,47.</span><span class="sxs-lookup"><span data-stu-id="aed8d-118">The revenue for the installation services will also be posted to the Revenue account, in the amount of $314.47.</span></span> <span data-ttu-id="aed8d-119">Tekjur fyrir þjónustuáætlunina verða bókaðar á frestaðan tekjulykil í upphæð $188,69.</span><span class="sxs-lookup"><span data-stu-id="aed8d-119">The revenue for the support plan will be posted to a Deferred revenue account in the amount of $188.69.</span></span> <span data-ttu-id="aed8d-120">Samtala tekjuupphæða verður að vera jöfn samtölu línanna sem voru settar upp til að sækja úthlutun tekjuupphæðar ($1.499,00).</span><span class="sxs-lookup"><span data-stu-id="aed8d-120">The sum of the revenue prices must equal the sum of the lines that were set up to capture revenue price allocation ($1,499.00).</span></span>

<span data-ttu-id="aed8d-121">[![Síða úthlutunar á tekjuupphæð](./media/39_rev-rec-scenarios.png)](./media/39_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="aed8d-121">[![Revenue price allocation page](./media/39_rev-rec-scenarios.png)](./media/39_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="aed8d-122">Viðskiptavinurinn er reikningsfærður fyrir fartölvunni og þjónustuáætluninni, en ekki fyrir uppsetningarþjónustunni.</span><span class="sxs-lookup"><span data-stu-id="aed8d-122">The customer is invoiced for the laptop and support plan, but not for the installation services.</span></span> <span data-ttu-id="aed8d-123">Eftirfarandi mynd sýnir bókhaldsfærsluna sem er bókuð fyrir reikninginn.</span><span class="sxs-lookup"><span data-stu-id="aed8d-123">The following illustration shows the accounting entry that is posted for the invoice.</span></span>

<span data-ttu-id="aed8d-124">[![Bókhaldsfærsla fyrir sölupöntunina sem er reikningsfærð](./media/40_rev-rec-scenarios.png)](./media/40_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="aed8d-124">[![Accounting entry for the invoiced sales order](./media/40_rev-rec-scenarios.png)](./media/40_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="aed8d-125">Færslur bókhaldsfærslna $1.276,94 til viðskiptakrafna.</span><span class="sxs-lookup"><span data-stu-id="aed8d-125">The accounting entry posts $1,276.94 to Accounts receivable.</span></span> <span data-ttu-id="aed8d-126">Þar sem þessi reikningur er hins vegar hlutareikningur, eru tekjurnar eða frestuðu tekjurnar auk skatts ekki sömu og upphæð viðskiptakrafa.</span><span class="sxs-lookup"><span data-stu-id="aed8d-126">However, because this invoice is a partial invoice, the revenue or deferred revenue plus the tax doesn't equal the Accounts receivable amount.</span></span> <span data-ttu-id="aed8d-127">Mismunur upp á $14,47 er bókaður á millireikning fyrir tekjur hlutareiknings.</span><span class="sxs-lookup"><span data-stu-id="aed8d-127">The difference of -$14.47 is posted to the Partial invoice revenue clearing account.</span></span>

<span data-ttu-id="aed8d-128">Tekjuskráningaráætlun er einnig búin til.</span><span class="sxs-lookup"><span data-stu-id="aed8d-128">The revenue recognition schedule is also created.</span></span>

<span data-ttu-id="aed8d-129">[![Síða tekjuskráningaráætlunar fyrir hlutareikning](./media/41_rev-rec-scenarios.png)](./media/41_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="aed8d-129">[![Revenue recognition schedule page for the partial invoice](./media/41_rev-rec-scenarios.png)](./media/41_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="aed8d-130">Síðar ákveður viðskiptavinurinn að kaupa ekki uppsetningarþjónustu.</span><span class="sxs-lookup"><span data-stu-id="aed8d-130">Later, the customer decides not to purchase installation services.</span></span> <span data-ttu-id="aed8d-131">Þessi lína er þar af leiðandi fjarlægð úr sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="aed8d-131">Therefore, that line is removed from the sales order.</span></span> <span data-ttu-id="aed8d-132">Athugið að ekki er hægt að staðfesta sölupöntunina aftur, þar sem aðeins reikningsfærðar línur eru eftir á sölupöntuninni.</span><span class="sxs-lookup"><span data-stu-id="aed8d-132">Note that the sales order can't be confirmed again, because only invoiced lines remain on the sales order.</span></span>

<span data-ttu-id="aed8d-133">[![Sölupöntun eftir að lína fyrir uppsetningarþjónustuna er fjarlægð](./media/42_rev-rec-scenarios.png)](./media/42_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="aed8d-133">[![Sales order after the line for installation services is removed](./media/42_rev-rec-scenarios.png)](./media/42_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="aed8d-134">Þótt ekki sé hægt að staðfesta sölupöntunina er samt sem áður hægt að endurúthluta henni.</span><span class="sxs-lookup"><span data-stu-id="aed8d-134">Even though the sales order can't be confirmed, it can be reallocated.</span></span> <span data-ttu-id="aed8d-135">Í sölupöntuninni skal velja **Endurúthluta verði með nýjum pöntunarlínum** til að opna síðuna **Endurúthluta verði með nýjum pöntunarlínum**.</span><span class="sxs-lookup"><span data-stu-id="aed8d-135">In the sales order, select **Reallocate price with new order lines** to open the **Reallocate price with new order lines** page.</span></span> <span data-ttu-id="aed8d-136">Veljið tvær eftirstandandi sölupöntunarlínur og veljið svo **Uppfæra endurúthlutun**.</span><span class="sxs-lookup"><span data-stu-id="aed8d-136">Select the two remaining sales order lines, and then select **Update reallocation**.</span></span> <span data-ttu-id="aed8d-137">Dálkurinn **Endurúthlutuð upphæð** sýnir nýja tekjuupphæð fyrir hverja eftirstandandi sölupöntunarlínu.</span><span class="sxs-lookup"><span data-stu-id="aed8d-137">The **Reallocated amount** column shows the new revenue price for each remaining sales order line.</span></span>

<span data-ttu-id="aed8d-138">[![Nýjar tekjuupphæðir á endurúthlutun verðs með nýrri síðu pöntunarlínu](./media/43_rev-rec-scenarios.png)](./media/43_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="aed8d-138">[![New revenue prices on the Reallocate price with new order lines page](./media/43_rev-rec-scenarios.png)](./media/43_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="aed8d-139">Næst skal velja **Væntanlegt fylgiskjal** til að skoða bókhaldsfærslurnar.</span><span class="sxs-lookup"><span data-stu-id="aed8d-139">Next, select **Expected voucher** to view the accounting entries.</span></span>

<span data-ttu-id="aed8d-140">[![Bókhaldsfærslur á síðu Væntanlegs fylgiskjals](./media/44_rev-rec-scenarios.png)](./media/44_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="aed8d-140">[![Accounting entries on the Expected voucher page](./media/44_rev-rec-scenarios.png)](./media/44_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="aed8d-141">Á síðunni **Væntanlegt fylgiskjal** bakfæra fimm síðustu línurnar upprunalegri bókhaldsfærslu úr bókuðum reikningi.</span><span class="sxs-lookup"><span data-stu-id="aed8d-141">On the **Expected voucher** page, the last five lines reverse the original accounting entry from the posted invoice.</span></span> <span data-ttu-id="aed8d-142">Fyrstu fjórar línurnar eru nýju bókhaldsfærslurnar sem eru bókaðar fyrir reikninginn.</span><span class="sxs-lookup"><span data-stu-id="aed8d-142">The first four lines are the new accounting entries that are posted for the invoice.</span></span> <span data-ttu-id="aed8d-143">Mikilvægt er að skilja að viðskiptavinurinn fær ekki sendan nýja reikninginn.</span><span class="sxs-lookup"><span data-stu-id="aed8d-143">It's important that you understand that a new invoice isn't presented to the customer.</span></span> <span data-ttu-id="aed8d-144">Eftir Endurúthlutun, skuldar viðskiptavinur enn $1.276,94, sem er upphæðin sem verður að bóka á viðskiptakröfur í nýju bókhaldsfærslunni.</span><span class="sxs-lookup"><span data-stu-id="aed8d-144">After the reallocation, the customer still owes $1,276.94, which is the amount that must be posted to Accounts receivable in the new accounting entry.</span></span> <span data-ttu-id="aed8d-145">Nýju tekjurnar eða frestuðu tekjurnar auk skatts jafngilda $1.276,94.</span><span class="sxs-lookup"><span data-stu-id="aed8d-145">The new revenue or deferred revenue plus tax equals $1,276.94.</span></span> <span data-ttu-id="aed8d-146">Þar af leiðandi þarf ekki að bóka á millireikning fyrir tekjur hlutareiknings.</span><span class="sxs-lookup"><span data-stu-id="aed8d-146">Therefore, you don't have to post to the Partial invoice revenue clearing account.</span></span>

<span data-ttu-id="aed8d-147">Til að ljúka endurúthlutuninni skal velja **Vinna úr**.</span><span class="sxs-lookup"><span data-stu-id="aed8d-147">To complete the reallocation, select **Process**.</span></span> <span data-ttu-id="aed8d-148">Bókunardagsetning er færð inn.</span><span class="sxs-lookup"><span data-stu-id="aed8d-148">A posting date is entered.</span></span> <span data-ttu-id="aed8d-149">Eftir að Endurúthlutun er lokið sýnir síðan **Úthlutunar á tekjuupphæð** endurúthlutun verðs fyrir vörurnar tvær sem eru eftir.</span><span class="sxs-lookup"><span data-stu-id="aed8d-149">After the reallocation is completed, the **Revenue price allocation** page shows the price reallocation for the two remaining items.</span></span>

<span data-ttu-id="aed8d-150">[![Verðúthlutun fyrir eftirstandandi vörur á úthlutunarsíðu tekjuupphæðar](./media/45_rev-rec-scenarios.png)](./media/45_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="aed8d-150">[![Price reallocation for the remaining items on the Revenue price allocation page](./media/45_rev-rec-scenarios.png)](./media/45_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="aed8d-151">Tekjuskráningaráætlunin var einnig uppfærð á grunni nýrrar endurúthlutunar á tekjuupphæð.</span><span class="sxs-lookup"><span data-stu-id="aed8d-151">The revenue recognition schedule was also updated, based on the new revenue reallocation price.</span></span> <span data-ttu-id="aed8d-152">Á sölupöntuninni skal opna síðuna **Tekjuskráningaráætlun**.</span><span class="sxs-lookup"><span data-stu-id="aed8d-152">From the sales order, open the **Revenue recognition schedule** page.</span></span> <span data-ttu-id="aed8d-153">Áður voru 13 línur fyrir vöru S0008 (12 mánaða áætlun var úthlutað á þessa vöru).</span><span class="sxs-lookup"><span data-stu-id="aed8d-153">Previously, there were 13 lines for item S0008 (a 12-month schedule was assigned to this item).</span></span> <span data-ttu-id="aed8d-154">Nú eru 39 línur: 13 upprunalegar áætlunarlínur, 13 áætlunarlínur bakfærslu og 13 línur sem byggja á nýju tekjuupphæðinni.</span><span class="sxs-lookup"><span data-stu-id="aed8d-154">There are now 39 lines: the 13 original schedule lines, 13 reversal schedule lines, and 13 lines that are based on the new revenue price.</span></span>

<span data-ttu-id="aed8d-155">[![Síða uppfærslu tekjuskráningaráætlunar með 39 línum fyrir vöru S0008](./media/46_rev-rec-scenarios.png)](./media/46_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="aed8d-155">[![Updated Revenue recognition schedule page with 39 lines for item S0008](./media/46_rev-rec-scenarios.png)](./media/46_rev-rec-scenarios.png)</span></span>

<span data-ttu-id="aed8d-156">Þegar **Fylgiskjal** er valið sýnir reikningabókin upprunalega bókhaldsfærsluna.</span><span class="sxs-lookup"><span data-stu-id="aed8d-156">When you select **Voucher**, the invoice journal shows the original accounting entry.</span></span> <span data-ttu-id="aed8d-157">Til að skoða bakfærsluna og nýju bókhaldsfærsluna úr sölupöntuninni skal velja **Leiðréttingar á tekjum** í aðgerðasvæðinu og síðan velja **Fylgiskjal**.</span><span class="sxs-lookup"><span data-stu-id="aed8d-157">To view the reversing entry and the new accounting entry from the sales order, select **Revenue adjustments** on the Action Pane, and then select **Voucher**.</span></span>

<span data-ttu-id="aed8d-158">Næst skal opna síðuna **Allir viðskiptavinir** (**Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir**), velja viðskiptavin **US\_SI\_0003** og svo **Færslur**.</span><span class="sxs-lookup"><span data-stu-id="aed8d-158">Next, open the **All customers** page (**Accounts receivable \> Customers \> All customers**), select customer **US\_SI\_0003**, and then select **Transactions**.</span></span> <span data-ttu-id="aed8d-159">Síðan **Færslur viðskiptavinar** sýnir aðeins upprunalegan reikning (000008) ásamt upprunalegri bókhaldsfærslu.</span><span class="sxs-lookup"><span data-stu-id="aed8d-159">The **Customer transactions** page shows only the original invoice (000008), together with the original accounting entry.</span></span> <span data-ttu-id="aed8d-160">Þar sem valkosturinn **Bóka leiðréttingar reiknings á viðskiptakröfur** er stilltur á **Nei** á síðunni **Fjárhagsfæribreytur** er aðeins fjárhagur uppfærður.</span><span class="sxs-lookup"><span data-stu-id="aed8d-160">Because the **Post invoice corrections to Accounts receivable** option is set to **No** on the **General ledger parameters** page, only General ledger is updated.</span></span> <span data-ttu-id="aed8d-161">Þess vegna eru bakfærðu og uppfærðu bókhaldsfærslurnar ekki sýndar.</span><span class="sxs-lookup"><span data-stu-id="aed8d-161">Therefore, the reversing and updated accounting entries aren't shown.</span></span> <span data-ttu-id="aed8d-162">Athugið að leiðréttar tekjufærslur sem voru stofnaðar í [aðstæðum 3](rev-rec-reallocation-scenario-3.md) eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="aed8d-162">Note that the revenue adjustment transactions that were created in [scenario 3](rev-rec-reallocation-scenario-3.md) are shown.</span></span>

<span data-ttu-id="aed8d-163">[![Upprunaleg bókhaldsfærsla á síðunni viðskiptavinafærslur](./media/47_rev-rec-scenarios.png)](./media/47_rev-rec-scenarios.png)</span><span class="sxs-lookup"><span data-stu-id="aed8d-163">[![Original accounting entry on the Customer transactions page](./media/47_rev-rec-scenarios.png)](./media/47_rev-rec-scenarios.png)</span></span>