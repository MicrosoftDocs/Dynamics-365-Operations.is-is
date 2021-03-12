---
title: Leiðrétta leigusamninga
description: Þetta efnisatriði útskýrir hvernig á að leiðrétta leigusamning. Leiðrétting gæti verið nauðsynleg ef leiguskilmálum er breytt, leigan framlengd eða aðrar aðstæður breytast.
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
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9d1c6e20e72fb2816c32e71e8921a94724ae5656
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/28/2020
ms.locfileid: "4444593"
---
# <a name="adjust-leases"></a><span data-ttu-id="dc4be-104">Leiðrétta leigusamninga</span><span class="sxs-lookup"><span data-stu-id="dc4be-104">Adjust leases</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc4be-105">Þetta efnisatriði útskýrir hvernig á að leiðrétta leigusamning.</span><span class="sxs-lookup"><span data-stu-id="dc4be-105">The topic explains how to adjust a lease.</span></span> <span data-ttu-id="dc4be-106">Leiðrétting gæti verið nauðsynleg ef leiguskilmálum er breytt, leigan framlengd eða aðrar aðstæður breytast.</span><span class="sxs-lookup"><span data-stu-id="dc4be-106">Adjustment might be required if the lease terms are modified, the lease is extended, or other circumstances change.</span></span> <span data-ttu-id="dc4be-107">Eignarleiga uppfyllir leiðbeiningar sem efnisatriði um skráningarkerfi reikningsskilastaðla 842 (ASC 842) og alþjóðlegan reikningsskilastaðal 16 (IFRS 16) kveður á um varðandi breytingar á leigusamningum.</span><span class="sxs-lookup"><span data-stu-id="dc4be-107">Asset leasing complies with the guidance that Accounting Standards Codification Topic 842 (ASC 842) and International Financial Reporting Standard 16 (IFRS 16) provide about lease modifications.</span></span> <span data-ttu-id="dc4be-108">ASC 842-20-15-1 skilgreinir breytingar á leigusamningi sem allar breytingar á skilmálum samnings sem valda breytingu á umfangi, eða meðferð á leigusamningi.</span><span class="sxs-lookup"><span data-stu-id="dc4be-108">ASC 842-20-15-1 defines a lease modification as any change to the terms and conditions of a contract that causes a change in the scope of, or the consideration for, a lease.</span></span> <span data-ttu-id="dc4be-109">Málsgrein 39 í IFRS 16 segir að leigjandi þurfi að endurmeta leiguskuldbindingu þannig að hún endurspegli breytingar á leigugreiðslum.</span><span class="sxs-lookup"><span data-stu-id="dc4be-109">Paragraph 39 of IFRS 16 states that a lessee must revalue the lease liability so that it reflects changes to the lease payments.</span></span>

<span data-ttu-id="dc4be-110">Fyrir fyrirtæki sem fylgja ASC 842 eða IFRS 16 er leigusamningur endurmetinn aftur til að endurspegla breytingu á núvirði á lágmarksgreiðslum á leigu í framtíðinni (PVFMLP).</span><span class="sxs-lookup"><span data-stu-id="dc4be-110">For organizations that adhere to ASC 842 or IFRS 16, a lease is remeasured to reflect a change in the present value of the future minimum lease payments (PVFMLP).</span></span> <span data-ttu-id="dc4be-111">Þegar PVFMLP-aukning er til staðar mun bókarfærslan sem er stofnuð vera debetfærsla afnotaréttar af eign og kreditfærsla leiguskuldbindingarinnar á milli nýja PVFMLP og eldri PVFMLP.</span><span class="sxs-lookup"><span data-stu-id="dc4be-111">If the PVFMLP increases, the journal entry that is created will be a debit to the right-of-use (ROU) asset and a credit to the lease liability for the difference between the new PVFMLP and the previous PVFMLP.</span></span> <span data-ttu-id="dc4be-112">Ef PVFMLP lækkar verður bókarfærslan debetfærsla leiguskuldbindingar og kreditfærsla afnotaréttar af eign fyrir mismuninum.</span><span class="sxs-lookup"><span data-stu-id="dc4be-112">If the PVFMLP decreases, the journal entry will be a debit to the lease liability and a credit to the ROU asset for the difference.</span></span>

<span data-ttu-id="dc4be-113">Ef leiðréttingin lækkar afnotarétt af eign 0 (núll) verður afgangurinn kreditfærður á bókunarlykil hagnaðar vegna breytinga á leigusamningi sem tilgreindur er á síðunni **Bókunarlyklar leigu**.</span><span class="sxs-lookup"><span data-stu-id="dc4be-113">If the adjustment decreases the ROU asset past 0 (zero), the remainder will be credited to the gain on lease modification posting account that is specified on the **Lease posting accounts** page.</span></span> <span data-ttu-id="dc4be-114">Kerfisreikningar fyrir þessar færslur og aðrar leiðréttingarfærslur, svo sem breytingar á flokkun, ógreiddur stofnkostnaður, leiguhvatar, fyrirframgreiðslur og kostnaður sundurhlutunar sem hlýst af breytingum á leigusamningi.</span><span class="sxs-lookup"><span data-stu-id="dc4be-114">The system accounts for these transactions and other adjustment entries, such as classification changes, initial direct costs, lease incentives, prepayments, and dismantling costs that arise from lease modifications.</span></span>

<span data-ttu-id="dc4be-115">Til að fá sérstaka leiðsögn varðandi leiðréttingarfærslur leigusamnings er mælt með því að skoða IFRS 16 og ASC 842.</span><span class="sxs-lookup"><span data-stu-id="dc4be-115">For specific guidance about lease adjustment transactions, we recommend that you see IFRS 16 and ASC 842.</span></span>

<span data-ttu-id="dc4be-116">Gerðu eftirfarandi til að breyta leigusamningi.</span><span class="sxs-lookup"><span data-stu-id="dc4be-116">To adjust a lease, follow these steps.</span></span> <span data-ttu-id="dc4be-117">Breyttu gögnin uppfæra leiguáætlun þegar keyrslu á ferli áætlunarinnar er lokið.</span><span class="sxs-lookup"><span data-stu-id="dc4be-117">The modified data will update lease schedules after the Create schedule process is run.</span></span>

1. <span data-ttu-id="dc4be-118">Opnaðu **Eignarleiga \> Leigusamningar \> Samantekt leigusamnings**.</span><span class="sxs-lookup"><span data-stu-id="dc4be-118">Go to **Asset leasing \> Leases \> Lease summary**.</span></span>
2. <span data-ttu-id="dc4be-119">Á síðunni **Samantekt leigusamnings** skaltu velja leigusamning til að leiðrétta og veldu síðan **Breyta leigusamningi**.</span><span class="sxs-lookup"><span data-stu-id="dc4be-119">On the **Lease summary** page, select the lease to adjust, and then select **Adjust lease**.</span></span>
3. <span data-ttu-id="dc4be-120">Á síðunni **Breyta leigusamningi** skaltu færa inn nýjar upplýsingar fyrir leiðréttan leigusamning.</span><span class="sxs-lookup"><span data-stu-id="dc4be-120">On the **Adjust lease** page, enter the new information for the adjusted lease.</span></span>

    <span data-ttu-id="dc4be-121">Taktu eftir því að síðan **Breyta leigusamningi** líkist síðunni **Bæta við leigusamningi**.</span><span class="sxs-lookup"><span data-stu-id="dc4be-121">Notice that the **Adjust lease** page resembles the **Add lease** page.</span></span> <span data-ttu-id="dc4be-122">Að auki, rétt eins og upphafsdagsetningin sem þú tilgreinir þegar leigusamningi er bætt við sker úr um hvenær leigusamningurinn hefst, sker svæðið **Breytingardagsetning** á síðunni **Breyta leigusamningi** úr um hvenær breytti leigusamningurinn hefst.</span><span class="sxs-lookup"><span data-stu-id="dc4be-122">Additionally, just as the commencement date that you specify when you add a lease determines when the new lease starts, the **Modification date** field on the **Adjust lease** page determines when the modified lease starts.</span></span> <span data-ttu-id="dc4be-123">Þessi dagsetning getur ekki verið eftir upphafsdagsetninguna í greiðsluáætlunarlínunum.</span><span class="sxs-lookup"><span data-stu-id="dc4be-123">This date can't be after the start date on the payment schedule lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="dc4be-124">Svæðin **Atriði varðandi afnotarétt af eign** eiga við um breytinguna á leigusamningnum.</span><span class="sxs-lookup"><span data-stu-id="dc4be-124">The **ROU considerations** fields apply to the lease adjustment.</span></span> <span data-ttu-id="dc4be-125">Þegar enginn stofnkostnaður, leiguhvatar, fyrirframgreiðslur eða kostnaður sundurhluunar er tengdur við breyttan leigusamning skal skilja þessi svæði eftir auð.</span><span class="sxs-lookup"><span data-stu-id="dc4be-125">If no initial direct costs, lease incentives, prepayments, or dismantling costs are associated with the modified lease, you should leave these fields blank.</span></span> <span data-ttu-id="dc4be-126">Upprunalegu upphæðirnar eiga ekki við um uppfærða leigusamninginn.</span><span class="sxs-lookup"><span data-stu-id="dc4be-126">The original amounts won't apply to the updated lease.</span></span> <span data-ttu-id="dc4be-127">Allur viðbótarkostnaður sem myndast þegar leigusamningnum er breytt ætti að færa inn á síðuna **Breyta leigusamningi**.</span><span class="sxs-lookup"><span data-stu-id="dc4be-127">Any additional costs that are incurred when the lease is modified should be entered on the **Adjust lease** page.</span></span>
    > 
    > <span data-ttu-id="dc4be-128">Leigusali veitir t.d. 1000 USD hvata til að samþykkja framlengingu á leigusamningi.</span><span class="sxs-lookup"><span data-stu-id="dc4be-128">For example, a lessor provides a $1,000 incentive for agreeing to a lease extension.</span></span> <span data-ttu-id="dc4be-129">Í þessu tilviki þegar þú breytir leigusamningnum til að gera ráð fyrir framlengingunni færir þú **1000** inn í svæðið **Leiguhvatar**.</span><span class="sxs-lookup"><span data-stu-id="dc4be-129">In this case, when you adjust the lease to account for the extension, you enter **1,000** in the **Lease incentives** field.</span></span> <span data-ttu-id="dc4be-130">Ef engir hvatar eru tengdir við breytingar á leigusamningi skal hreinsa út öll gildi sem áður voru færð inn í þetta svæði.</span><span class="sxs-lookup"><span data-stu-id="dc4be-130">If no incentives are associated with the lease adjustment, you should clear any value that was previously entered in this field.</span></span> <span data-ttu-id="dc4be-131">Sömu rökin eru notuð fyrir önnur atriði varðandi afnotarétt af eign.</span><span class="sxs-lookup"><span data-stu-id="dc4be-131">The same logic is applied to other ROU considerations.</span></span>

    <span data-ttu-id="dc4be-132">Greiðsluáætlunarlínur leiðrétta leigusamningsins ætti að stofna á væntanlegum grunni.</span><span class="sxs-lookup"><span data-stu-id="dc4be-132">The payment schedule lines of the adjusted lease should be created on a prospective basis.</span></span> <span data-ttu-id="dc4be-133">Greiðsluáætlunarlínur sem eru stofnaðar á væntanlegan grunni geta ekki hafist áður en breytingar á leigusamningnum taka gildi.</span><span class="sxs-lookup"><span data-stu-id="dc4be-133">Payment schedule lines that are created on a prospective basis can't start before the lease modifications take effect.</span></span>

    <span data-ttu-id="dc4be-134">Eftirfarandi skref eru nánast hin sömu og upphafsskrefin við að viðurkenna leigusamning.</span><span class="sxs-lookup"><span data-stu-id="dc4be-134">The following steps are almost identical to the steps for initially recognizing a lease.</span></span>

4. <span data-ttu-id="dc4be-135">Veldu **Stofna áætlanir** til að mynda leiðrétta greiðsluáætlun.</span><span class="sxs-lookup"><span data-stu-id="dc4be-135">Select **Create schedules** to generate the adjusted payment schedule.</span></span> <span data-ttu-id="dc4be-136">Þú færð skilaboð sem tilgreinir að greiðsluáætlun hafi verið stofnuð fyrir leigusamninginn.</span><span class="sxs-lookup"><span data-stu-id="dc4be-136">You receive a message that states that the payment schedule has been created for the lease.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="dc4be-137">Áður en hægt er að velja **Stofna áætlanir** skal ganga úr skugga um að breytingadagsetningin og greiðsluáætlunarlínur séu réttar.</span><span class="sxs-lookup"><span data-stu-id="dc4be-137">Before you select **Create schedules**, make sure that the modification date and payment schedule lines are accurate.</span></span> <span data-ttu-id="dc4be-138">Gangið einnig úr skugga um að allur stofnkostnaður, leiguhvatar, fyrirframgreiðslur eða kostnaður sundurhlutunar samsvari aðeins kostnaði sem hlýst af leiðréttingunni.</span><span class="sxs-lookup"><span data-stu-id="dc4be-138">Also make sure that all initial direct costs, lease incentives, prepayments, or dismantling costs correspond only to those costs that arise from the adjustment.</span></span>

5. <span data-ttu-id="dc4be-139">Til að skoða nýstofnaða greiðsluáætlun skal velja **Bækur** og opna síðuna **Greiðsluáætlun**.</span><span class="sxs-lookup"><span data-stu-id="dc4be-139">To view the newly created payment schedule, select **Books**, and open the **Payment schedule** page.</span></span>
6. <span data-ttu-id="dc4be-140">Á síðunni **Greiðsluáætlun** er hægt að breyta leiðréttum greiðsluupphæðum áður en greiðsluáætlun er staðfest.</span><span class="sxs-lookup"><span data-stu-id="dc4be-140">On the **Payment schedule** page, you can edit the adjusted payment amounts before you confirm the payment schedule.</span></span> <span data-ttu-id="dc4be-141">Til að staðfesta áætlunina skal velja **Staðfesta áætlun**.</span><span class="sxs-lookup"><span data-stu-id="dc4be-141">To confirm the schedule, select **Confirm schedule**.</span></span>

    <span data-ttu-id="dc4be-142">Þegar greiðsluáætlun er staðfest er búið að stofna nýjar afskriftir eigna og nýjar áætlanir um leiguskuldbindingar.</span><span class="sxs-lookup"><span data-stu-id="dc4be-142">When the payment schedule is confirmed, the new asset depreciation and new lease liability schedules are created.</span></span>

7. <span data-ttu-id="dc4be-143">Til að skoða nýju afskriftaráætlun leiguskuldbindingar sem er mynduð úr nýja innslættinum skal loka síðunni **Greiðsluáætlun** og opna síðan síðuna **Afskriftaráætlun leiguskuldbindingar**.</span><span class="sxs-lookup"><span data-stu-id="dc4be-143">To view the new lease liability amortization schedule that is generated from the new inputs, close the **Payment schedule** page, and open the **Liability amortization schedule** page.</span></span>
8. <span data-ttu-id="dc4be-144">Til að skoða nýmyndaða afskriftaráætlun eigna skal opna síðuna **Afskriftaráætlun eigna** á síðunni **Upplýsingar um bók**.</span><span class="sxs-lookup"><span data-stu-id="dc4be-144">To view the newly generated asset depreciation schedule, open the **Asset depreciation schedule** page from the **Book details** page.</span></span>
9. <span data-ttu-id="dc4be-145">Til að mynda leiðréttingarbókarfærslu skal velja **Aðgerð \> Leiðrétting leigusamnings**.</span><span class="sxs-lookup"><span data-stu-id="dc4be-145">To generate the adjustment journal entry, select **Function \> Lease adjustment**.</span></span> <span data-ttu-id="dc4be-146">Þú færð skilaboð sem segir til um að leiðréttingabókarfærsla hafi verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="dc4be-146">You receive a message that states that the adjustment journal entry has been created.</span></span> 
10. <span data-ttu-id="dc4be-147">Til að skoða bókarfærsluna skal velja **Færslubækur \> Færslubók eignarleigu**.</span><span class="sxs-lookup"><span data-stu-id="dc4be-147">To view the journal entry, select **Journals \> Asset leasing journal**.</span></span>
11. <span data-ttu-id="dc4be-148">Til að bóka bókarfærsluna skal velja línuna og velja síðan **Bóka**.</span><span class="sxs-lookup"><span data-stu-id="dc4be-148">To post the journal entry, select the line, and then select **Post**.</span></span>

## <a name="view-lease-versions"></a><span data-ttu-id="dc4be-149">Skoða útgáfur leigusamnings</span><span class="sxs-lookup"><span data-stu-id="dc4be-149">View lease versions</span></span>

<span data-ttu-id="dc4be-150">Ef leigusamningi hefur verið breytt er hægt að skoða mismunandi útgáfur af honum.</span><span class="sxs-lookup"><span data-stu-id="dc4be-150">If a lease has been modified, you can view the different versions of it.</span></span> <span data-ttu-id="dc4be-151">Einnig er hægt að skoða eldri áætlanir og eldri upplýsingar um leigusamning.</span><span class="sxs-lookup"><span data-stu-id="dc4be-151">You can also view the historical schedules and past lease details.</span></span>

1. <span data-ttu-id="dc4be-152">Á síðunni **Samantekt leigusamnings** skal velja leigusamning og velja síðan á aðgerðasvæðinu **Útgáfuferill leigusamnings**.</span><span class="sxs-lookup"><span data-stu-id="dc4be-152">On the **Lease summary** page, select the lease, and then, on the Action Pane, select **Lease version history**.</span></span>

    <span data-ttu-id="dc4be-153">Þegar breytingar hafa verið gerðar á völdum leigusamningi birtast ólíkar útgáfur af samningnum á síðunni **Útgáfuferill leigusamnings**.</span><span class="sxs-lookup"><span data-stu-id="dc4be-153">If the selected lease has been adjusted, the **Lease version history** page shows the different versions of it.</span></span> <span data-ttu-id="dc4be-154">Upprunalegi leigusamningurinn er merktur með **1** og útgáfurnar þar á eftir með hækkandi númeraröð.</span><span class="sxs-lookup"><span data-stu-id="dc4be-154">The original lease is labeled **1**, and subsequent versions have ascending numerical order.</span></span>

    <span data-ttu-id="dc4be-155">Fyrir valda útgáfu leigusamnings er hægt að skoða fjárhagsvíddirnar, frekari upplýsingar um samninginn, staðsetningu og greiðsluáætlunarlínur.</span><span class="sxs-lookup"><span data-stu-id="dc4be-155">For a selected lease version, you can view the financial dimensions, contract details, location, and payment schedule lines.</span></span>

2. <span data-ttu-id="dc4be-156">Til að skoða eldri áætlanir skal opna breyttan leigusamning á síðunni **Samantekt leigusamnings** velja viðeigandi bók og velja síðan **Útgáfuferill bókar** á aðgerðasvæðinu.</span><span class="sxs-lookup"><span data-stu-id="dc4be-156">To view historical schedules, open the modified lease from the **Lease summary** page, select the desired book, and then, on the Action Pane, select **Book version history**.</span></span>
3. <span data-ttu-id="dc4be-157">Á síðunni **Bókaútgáfa** skal velja æskilega útgáfu og æskilega áætlun til skoðunar.</span><span class="sxs-lookup"><span data-stu-id="dc4be-157">On the **Book version** page, select the desired version and the desired schedule to view.</span></span>