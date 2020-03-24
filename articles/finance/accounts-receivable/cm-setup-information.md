---
title: Uppsetning á lánastýringu
description: Þetta efni lýsir uppsetningunni sem krafist er fyrir lánamálastjórnun.
author: mikefalkner
manager: AnnBe
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 65b1d1a232558efbe05e83d51706a78b12439e47
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124140"
---
# <a name="credit-management-setup"></a><span data-ttu-id="165a9-103">Uppsetning á lánastýringu</span><span class="sxs-lookup"><span data-stu-id="165a9-103">Credit management setup</span></span> 

[!include [banner](../includes/banner.md)]

## <a name="credit-management-workflows"></a><span data-ttu-id="165a9-104">Verkflæði lánastýringar</span><span class="sxs-lookup"><span data-stu-id="165a9-104">Credit management workflows</span></span>

<span data-ttu-id="165a9-105">Fara til **Skuldir og innheimta \> Uppsetning \> Verkflæði lánaumsýslu** til að skilgreina verkflæði sem eru notuð til að stjórna leiðréttingum á lánamörkum.</span><span class="sxs-lookup"><span data-stu-id="165a9-105">Go to **Credit and collections \> Setup \> Credit management workflows** to define the workflows that are used to manage credit limit adjustments.</span></span>

- <span data-ttu-id="165a9-106">Þú getur búið til verkflæði sem gerir þér kleift að samþykkja runu af leiðréttingum á lánamörkum með einu samþykki.</span><span class="sxs-lookup"><span data-stu-id="165a9-106">You can create a workflow that lets you approve a batch of credit limits adjustments through a single approval.</span></span>
- <span data-ttu-id="165a9-107">Þú getur bætt við verkflæði á línustigi, svo að hægt sé að samþykkja leiðréttingar á lánamörkum hver fyrir sig.</span><span class="sxs-lookup"><span data-stu-id="165a9-107">You can add a workflow at the line level, so that credit limit adjustments can be approved individually.</span></span>
- <span data-ttu-id="165a9-108">Þú getur búið til verkflæði sem beinir biðum sjálfkrafa að verkflæðisferli.</span><span class="sxs-lookup"><span data-stu-id="165a9-108">You can create a release workflow that automatically routes holds to a workflow process.</span></span>

## <a name="blocking-rules"></a><span data-ttu-id="165a9-109">Lokunarreglur</span><span class="sxs-lookup"><span data-stu-id="165a9-109">Blocking rules</span></span>

### <a name="ranking-payment-terms"></a><span data-ttu-id="165a9-110">Greiðsluskilmálar röðunar</span><span class="sxs-lookup"><span data-stu-id="165a9-110">Ranking payment terms</span></span>

<span data-ttu-id="165a9-111">Þú getur sett sölupöntun í bið ef greiðsluskilmálar pöntunarinnar passa ekki við sjálfgefna greiðsluskilmála viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="165a9-111">You can put a sales order on hold if the payment terms on the order don't match the default payment terms for the customer.</span></span> <span data-ttu-id="165a9-112">Hins vegar eru greiðsluskilmálar stundum ólíkir en eru nógu líkir til að þú viljir ekki setja pöntunina í bið.</span><span class="sxs-lookup"><span data-stu-id="165a9-112">However, sometimes the payment terms differ but are similar enough that you don't want to put the order on hold.</span></span> <span data-ttu-id="165a9-113">Þú getur raðað greiðsluskilmálum þannig að sumir þeirra séu með sömu stöðu en aðrir hærri eða lægri.</span><span class="sxs-lookup"><span data-stu-id="165a9-113">You can rank payment terms so that some of them have the same rank, whereas others have a higher or lower rank.</span></span>

<span data-ttu-id="165a9-114">Ef röðun greiðsluskilmála er virk verða sölupantanir settar í bið ef greiðsluskilmálar pöntunarinnar eru hærri en sjálfgefnir greiðsluskilmálar viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="165a9-114">If the rankings for payment terms are active, the sales orders will be put on hold if the payment terms on the order have a higher rank than the default payment terms for the customer.</span></span>

### <a name="ranking-settlement-discounts"></a><span data-ttu-id="165a9-115">Röðun uppgjörsafsláttar</span><span class="sxs-lookup"><span data-stu-id="165a9-115">Ranking settlement discounts</span></span>

<span data-ttu-id="165a9-116">Þú getur sett sölupöntun í bið ef staðgreiðsluafsláttur pöntunarinnar passar ekki við sjálfgefinn staðgreiðsluafslátt viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="165a9-116">You can put a sales order on hold if the cash discount on the order doesn't match the default cash discount for the customer.</span></span> <span data-ttu-id="165a9-117">Hins vegar er staðgreiðsluafsláttur stundum ólíkur en nógu líkur til að þú viljir ekki setja pöntunina í bið.</span><span class="sxs-lookup"><span data-stu-id="165a9-117">However, sometimes the cash discounts differ but are similar enough that you don't want to put the order on hold.</span></span> <span data-ttu-id="165a9-118">Þú getur raðað staðgreiðsluafsláttum þannig að sumir þeirra séu með sömu stöðu en aðrir hærri eða lægri.</span><span class="sxs-lookup"><span data-stu-id="165a9-118">You can rank cash discounts so that some of them have the same rank, whereas others have a higher or lower rank.</span></span>

<span data-ttu-id="165a9-119">Ef röðun uppgjörsafsláttar er virk verða sölupantanir settar í bið ef staðgreiðsluafsláttur pöntunarinnar er hærri en sjálfgefnir staðgreiðsluafsláttur viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="165a9-119">If rankings for settlement discounts are active, the sales orders will be put on hold if the cash discount on the order has a higher rank than the default cash discount for the customer.</span></span>

## <a name="reasons"></a><span data-ttu-id="165a9-120">Ástæður</span><span class="sxs-lookup"><span data-stu-id="165a9-120">Reasons</span></span>

<span data-ttu-id="165a9-121">Margvíslegar ástæður eru notaðar í lánamálum:</span><span class="sxs-lookup"><span data-stu-id="165a9-121">Several types of reasons are used in Credit management:</span></span>

- <span data-ttu-id="165a9-122">Ástæður bið eru af hverju sölupöntun var sett í bið.</span><span class="sxs-lookup"><span data-stu-id="165a9-122">Hold reasons indicate why a sales order was put on hold.</span></span>
- <span data-ttu-id="165a9-123">Sleppingarástæðum er úthlutað til pöntunar þegar henni er sleppt úr bið.</span><span class="sxs-lookup"><span data-stu-id="165a9-123">Release reasons are assigned to an order when it's released from hold.</span></span>
- <span data-ttu-id="165a9-124">Stöðuástæður segja til um hvers vegna lykilstöðu var úthlutað til viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="165a9-124">Status reasons indicate why an account status was assigned to a customer.</span></span>

<span data-ttu-id="165a9-125">Þú getur sett upp ástæður á síðunni **Ástæður lánaumsýslu** (**Lánastjórnun \> Uppsetning \> Lánastjórnun \> Ástæður lánaumsýslu**).</span><span class="sxs-lookup"><span data-stu-id="165a9-125">You can set up reasons on the **Credit management reasons** page (**Credit management \> Setup \> Credit management \> Credit management reasons**).</span></span>

1. <span data-ttu-id="165a9-126">Í reitnum **Ástæðugerð** velurðu gerð ástæðunnar: **Bið**, **Losun** eða **Staða**.</span><span class="sxs-lookup"><span data-stu-id="165a9-126">In the **Reason type** field, select the type of reason: **Hold**, **Release**, or **Status**.</span></span>
2. <span data-ttu-id="165a9-127">Í svæðið **Ástæða** er fært inn nafn fyrir ástæðuna.</span><span class="sxs-lookup"><span data-stu-id="165a9-127">In the **Reason** field, enter a name for the reason.</span></span>
3. <span data-ttu-id="165a9-128">Í reitnum **Lýsing** skal slá inn lýsingu á ástæðukóðanum.</span><span class="sxs-lookup"><span data-stu-id="165a9-128">In the **Description** field, enter a description of the reason code.</span></span>

## <a name="credit-management-groups"></a><span data-ttu-id="165a9-129">Lánastýringarflokkar</span><span class="sxs-lookup"><span data-stu-id="165a9-129">Credit management groups</span></span>

<span data-ttu-id="165a9-130">Lánastjórnunarhópar eru notaðir til að bera kennsl á viðskiptavini eða hópa viðskiptavina sem hafa sömu lánstrausteiginleika.</span><span class="sxs-lookup"><span data-stu-id="165a9-130">Credit management groups are used to identify customers or groups of customers that have the same credit management properties.</span></span> <span data-ttu-id="165a9-131">Til dæmis er hægt að nota lánastjórnunarhópa til að ákvarða reglur um útilokun og útilokun lána fyrir viðskiptavini.</span><span class="sxs-lookup"><span data-stu-id="165a9-131">For example, credit management groups can be used to determine the blocking and exclusion credit management rules for customers.</span></span>

<span data-ttu-id="165a9-132">Þú getur stofnað kreditstjórnunarhópa á síðunni **Kreditstjórnunarhópar** (**Lánastjórnun \> Uppsetning \> Lánastjórnun> Hópauppsetning**).</span><span class="sxs-lookup"><span data-stu-id="165a9-132">You can create credit management groups on the **Credit management groups** page (**Credit management \> Setup> Groups setup \> Credit management groups**).</span></span>

1. <span data-ttu-id="165a9-133">Veldu **Nýtt** til að búa til nýja línu.</span><span class="sxs-lookup"><span data-stu-id="165a9-133">Select **New** to create a line.</span></span>
2. <span data-ttu-id="165a9-134">Færið inn kenni fyrir hópinn.</span><span class="sxs-lookup"><span data-stu-id="165a9-134">Enter an ID for the group.</span></span> <span data-ttu-id="165a9-135">Kennið getur haft allt að 10 stafi.</span><span class="sxs-lookup"><span data-stu-id="165a9-135">The ID can have up to 10 characters.</span></span>
3. <span data-ttu-id="165a9-136">Í reitinn **Lýsing** skal færa inn heiti á hópnum.</span><span class="sxs-lookup"><span data-stu-id="165a9-136">In the **Description** field, enter a name for the group.</span></span> <span data-ttu-id="165a9-137">Heitið getur haft allt að 60 stafi.</span><span class="sxs-lookup"><span data-stu-id="165a9-137">The name can have up to 60 characters.</span></span>

<span data-ttu-id="165a9-138">Kreditstjórnunarhópurinn er úthlutaður á viðskiptavin á flýtiflipanum **Skuldir og innheimta** af síðunni **Allir viðskiptavinir** (**Viðskiptakröfur \> Viðskiptavinir \> Allir viðskiptavinir**).</span><span class="sxs-lookup"><span data-stu-id="165a9-138">The credit management group is assigned to a customer on the **Credit and collections** FastTab of the **All customers** page (**Account receivable \> Customers \> All customers**).</span></span>

## <a name="account-statuses"></a><span data-ttu-id="165a9-139">Stöður reikninga</span><span class="sxs-lookup"><span data-stu-id="165a9-139">Account statuses</span></span>

<span data-ttu-id="165a9-140">Þú getur búið til stöðu reikninga til að bera kennsl á lánstraust viðskiptavinarreiknings.</span><span class="sxs-lookup"><span data-stu-id="165a9-140">You can create account statuses to identify the credit standing of a customer account.</span></span> <span data-ttu-id="165a9-141">Þú getur skilgreint stöðu og áhrif hennar á reikninga og afhendingar í biðferlum.</span><span class="sxs-lookup"><span data-stu-id="165a9-141">You can define a status and its effect on the invoicing and delivery on-hold processes.</span></span> <span data-ttu-id="165a9-142">Einnig er hægt að nota stöðu reikninga til að ákvarða útilokunarreglur fyrir viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="165a9-142">Account statuses can also be used to determine blocking rules for a customer.</span></span>

<span data-ttu-id="165a9-143">Þú getur búið til stöðu reikninga á síðunni **Lykilstöður** (**Lánastjórnun \> Uppsetning> Uppsetning hópa \> Lykilstöður**).</span><span class="sxs-lookup"><span data-stu-id="165a9-143">You can create account statuses on the **Account statuses** page (**Credit management \> Setup> Groups setup \> Account statuses**).</span></span>

1. <span data-ttu-id="165a9-144">Bættu við stöðu reiknings og sláðu inn lýsingu sem táknar lánstraust viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="165a9-144">Add an account status, and enter a description that represents the credit standing for a customer.</span></span> <span data-ttu-id="165a9-145">Notaðu til dæmis **Venjulegt** til að gefa til kynna að viðskiptavinur sé í góðu ástandi og opnar pantanir eru háðar stöðluðu vinnslu lánamála.</span><span class="sxs-lookup"><span data-stu-id="165a9-145">For example, use **Normal** to indicate that a customer is in good standing and open orders are subject to standard credit management processing.</span></span>
2. <span data-ttu-id="165a9-146">Í reitunum **Reikningsfærsla** og **Afhending í bið** velurðu þá tegund bið sem ætti að eiga sér stað fyrir viðskiptavini sem hafa þessa reikningsstöðu.</span><span class="sxs-lookup"><span data-stu-id="165a9-146">In the **Invoicing** and **Delivery on Hold** fields, select the type of hold that should occur for customers who have this account status.</span></span> <span data-ttu-id="165a9-147">Þú getur haldið allri vinnslu, haldið aðeins á reikningsvinnslu eða ekki haft neina vinnslu þegar lánamörkunarreglunum er beitt.</span><span class="sxs-lookup"><span data-stu-id="165a9-147">You can hold all processing, hold only invoice processing, or hold no processing when the credit limit rules are applied.</span></span>

## <a name="scoring-groups"></a><span data-ttu-id="165a9-148">Einkunnaflokkar</span><span class="sxs-lookup"><span data-stu-id="165a9-148">Scoring groups</span></span>

<span data-ttu-id="165a9-149">Þú getur sett upp stigahópa til að skilgreina áhættuþætti og viðmið sem eru notuð til að mæla þá.</span><span class="sxs-lookup"><span data-stu-id="165a9-149">You can set up scoring groups to define risk factors and the criteria that are used to measure them.</span></span> <span data-ttu-id="165a9-150">Þegar upplýsingum um viðskiptavin er beitt á stigahóp er stig reiknað fyrir hvern áhættuþátt og notaður til að setja viðskiptavininn í áhættuhóp.</span><span class="sxs-lookup"><span data-stu-id="165a9-150">When information about a customer is applied to a scoring group, a score is calculated for each risk factor and used to put the customer in a risk group.</span></span> <span data-ttu-id="165a9-151">Hægt er að nota áhættuhópinn til að bera kennsl á lánstraust og reikna sjálfvirk lánamörk.</span><span class="sxs-lookup"><span data-stu-id="165a9-151">The risk group can be used to identify credit worthiness and calculate automatic credit limits.</span></span>

<span data-ttu-id="165a9-152">Þú getur búið til stigahópa á síðunni **Stigahópar** (**Lánastjórnun \> Uppsetning \> Uppsetning áhættu \> Stigahópar**).</span><span class="sxs-lookup"><span data-stu-id="165a9-152">You can create scoring groups on the **Scoring groups** page (**Credit management \> Setup \> Risk setup \> Scoring groups**).</span></span>

1. <span data-ttu-id="165a9-153">Stofnaðu stigahóp og skráðu heiti fyrir hann.</span><span class="sxs-lookup"><span data-stu-id="165a9-153">Create a scoring group, and enter a name for it.</span></span>
2. <span data-ttu-id="165a9-154">Sláðu inn lýsingu til að lýsa stigahópnum frekar.</span><span class="sxs-lookup"><span data-stu-id="165a9-154">Enter a description to further describe the scoring group.</span></span>
3. <span data-ttu-id="165a9-155">Veldu hópgerð.</span><span class="sxs-lookup"><span data-stu-id="165a9-155">Select a group type.</span></span> <span data-ttu-id="165a9-156">Það eru átta fyrirframskilgreindar gerðir.</span><span class="sxs-lookup"><span data-stu-id="165a9-156">There are eight predefined types.</span></span> <span data-ttu-id="165a9-157">Þú getur líka valið **Notandaskilgreint** til að skilgreina hópgerð sem hentar betur fyrirtækinu þínu.</span><span class="sxs-lookup"><span data-stu-id="165a9-157">You can also select **User defined** to define a group type that's better suited to your organization.</span></span>
4. <span data-ttu-id="165a9-158">Veldu stigagjöf til að skilgreina hvernig stigahópurinn reiknar út áhættustigið.</span><span class="sxs-lookup"><span data-stu-id="165a9-158">Select a score type to define how the scoring group calculates the risk score.</span></span> <span data-ttu-id="165a9-159">Eftirtaldir valkostir eru í boði:</span><span class="sxs-lookup"><span data-stu-id="165a9-159">The following options are available:</span></span>

    - <span data-ttu-id="165a9-160">**Svið** - Notaðu þennan valkost til að skilgreina svið gildi sem ætti að nota til að reikna stig.</span><span class="sxs-lookup"><span data-stu-id="165a9-160">**Range** – Use this option to define a range of values that should be used to calculate a score.</span></span>
    - <span data-ttu-id="165a9-161">**Notandaskilgreint** - Notaðu þennan valkost til að skilgreina handvirkt lista yfir gildi sem ætti að nota fyrir stigagjöfina.</span><span class="sxs-lookup"><span data-stu-id="165a9-161">**User defined** – Use this option to manually define a list of values that should be used for the score.</span></span>

5. <span data-ttu-id="165a9-162">Ef þú valdir **Svið** sem stigagjöf, bættu við línum til að skilgreina gildissviðið og samsvarandi stig.</span><span class="sxs-lookup"><span data-stu-id="165a9-162">If you selected **Range** as the score type, add lines to define the range of values and the corresponding scores.</span></span>

    1. <span data-ttu-id="165a9-163">Í reitnum **Frá gildi** tilgreindu lægsta gildi á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="165a9-163">In the **From value** field, specify the lowest value in the range.</span></span>
    2. <span data-ttu-id="165a9-164">Í reitnum **Til gildis** tilgreindu hæsta gildi á sviðinu.</span><span class="sxs-lookup"><span data-stu-id="165a9-164">In the **To value** field, specify the highest value in the range.</span></span>
    3. <span data-ttu-id="165a9-165">Í reitinn **Stig** sláðu inn stig sem ætti að vera úthlutað þegar gildið sem er gefið er í sviðinu "frá" / "til".</span><span class="sxs-lookup"><span data-stu-id="165a9-165">In the **Score** field, enter the score that should be assigned when the value that is provided is in the "from"/"to" range.</span></span>

    <span data-ttu-id="165a9-166">Ef þú valdir **Notendaskilgreint** sem stigagjöf, bættu við línum til að skilgreina notendaskilgreind gildi og samsvarandi stig.</span><span class="sxs-lookup"><span data-stu-id="165a9-166">If you selected **User defined** as the score type, add lines to define the user-defined values and the corresponding scores.</span></span>

    1. <span data-ttu-id="165a9-167">Í reitnum **Gildi** sláðu inn notendaskilgreint gildi sem ætti að vera veitt frá upplýsingum viðskiptavinarins.</span><span class="sxs-lookup"><span data-stu-id="165a9-167">In the **Value** field, enter the user-defined value that should be provided from the customer information.</span></span>
    2. <span data-ttu-id="165a9-168">Í reitinn **Stig** sláðu inn stig sem ætti að vera úthlutað þegar gildið sem er gefið er í sviðinu "frá" / "til".</span><span class="sxs-lookup"><span data-stu-id="165a9-168">In the **Score** field, enter the score that should be assigned when the value that is provided is in the "from"/"to" range.</span></span>

## <a name="risk-assessments"></a><span data-ttu-id="165a9-169">Áhættumat</span><span class="sxs-lookup"><span data-stu-id="165a9-169">Risk assessments</span></span>

<span data-ttu-id="165a9-170">Þú getur skilgreint áhættumat sem hægt er að úthluta viðskiptavinum, út frá áhættustiginu.</span><span class="sxs-lookup"><span data-stu-id="165a9-170">You can define risk assessments that can be assigned to customers, based on their risk score.</span></span> <span data-ttu-id="165a9-171">Áhættustig er reiknað með því að bera saman upplýsingar viðskiptavina við hvern stigahóp.</span><span class="sxs-lookup"><span data-stu-id="165a9-171">A risk score is calculated by comparing customer information to each scoring group.</span></span> <span data-ttu-id="165a9-172">Stigin eru dregin saman og heildarstigið er borið saman við gildin í uppstillingu áhættuhópsins til að bera kennsl á áhættuhópinn sem viðskiptavinurinn tilheyrir.</span><span class="sxs-lookup"><span data-stu-id="165a9-172">The scores are summed, and the total score is compared to the values in the risk group setup to identify the risk group that the customer belongs to.</span></span> <span data-ttu-id="165a9-173">Stig áhættuhópsins er síðan notað til að skilgreina útilokunar- og útilokunarreglur fyrir lánastjórnun fyrir viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="165a9-173">The risk group score is then used to define credit management blocking and exclusion rules for the customer.</span></span>

<span data-ttu-id="165a9-174">Þú getur sett upp áhættuhópa á síðunni **Áhættumat** (**Lánastjórnun \> Uppsetning \> Uppsetning áhættu \> Áhættumat**).</span><span class="sxs-lookup"><span data-stu-id="165a9-174">You can set up risk groups on the **Risk assessments** page (**Credit management \> Setup \> Risk setup \> Risk assessments**).</span></span>

1. <span data-ttu-id="165a9-175">Sláðu inn auðkenni áhættuhóps.</span><span class="sxs-lookup"><span data-stu-id="165a9-175">Enter a risk group ID.</span></span>
2. <span data-ttu-id="165a9-176">Sláðu inn lýsingu til að útskýrir áhættuhópinn frekar.</span><span class="sxs-lookup"><span data-stu-id="165a9-176">Enter a description to further explain the risk group.</span></span>
3. <span data-ttu-id="165a9-177">Sláðu inn svið skora sem er notað til að ákvarða hvaða viðskiptavinir tilheyra áhættuhópnum.</span><span class="sxs-lookup"><span data-stu-id="165a9-177">Enter a range of scores that is used to determine which customers belong to the risk group.</span></span>
4. <span data-ttu-id="165a9-178">Veldu áhættuhóp til að tilgreina táknið sem táknar áhættuhópinn.</span><span class="sxs-lookup"><span data-stu-id="165a9-178">Select a risk group indicator to specify the symbol that represents the risk group.</span></span>

## <a name="guaranteeinsurance-types"></a><span data-ttu-id="165a9-179">Gerðir ábyrgða/trygginga</span><span class="sxs-lookup"><span data-stu-id="165a9-179">Guarantee/insurance types</span></span>

<span data-ttu-id="165a9-180">Þú getur sett upp gerðir ábyrgða/trygginga á síðunni **Gerðir ábyrgða/trygginga** (**Lánastjórnun \> Uppsetning \> Uppsetning á ábyrgð/tryggingu \> Gerðir ábyrgða/trygginga**).</span><span class="sxs-lookup"><span data-stu-id="165a9-180">You can set up guarantee/insurance types on the **Guarantee/insurance types** page (**Credit management \> Setup \> Guarantee/insurance setup \> Guarantee/insurance types**).</span></span>

1. <span data-ttu-id="165a9-181">Sláðu inn ábyrgð eða tryggingategund sem auðkennir nafn ábyrgðaraðila eða vátryggingamiðlara.</span><span class="sxs-lookup"><span data-stu-id="165a9-181">Enter a guarantee or insurance type that identifies the name of the guarantor or insurance broker.</span></span>
2. <span data-ttu-id="165a9-182">Sláðu inn lýsingu til að lýsa ábyrgðarmanni / vátryggingamiðlara.</span><span class="sxs-lookup"><span data-stu-id="165a9-182">Enter a description to describe the guarantor/insurance broker.</span></span>

## <a name="coverage-types"></a><span data-ttu-id="165a9-183">Tegundir trygginga</span><span class="sxs-lookup"><span data-stu-id="165a9-183">Coverage types</span></span>

<span data-ttu-id="165a9-184">Hægt er að nota umfjöllunargerðir til að flokka tryggingar frekar.</span><span class="sxs-lookup"><span data-stu-id="165a9-184">Coverage types can be used to further classify insurance policies.</span></span> <span data-ttu-id="165a9-185">Þeir geta ekki verið notaðir með ábyrgðir.</span><span class="sxs-lookup"><span data-stu-id="165a9-185">They can't be used with guarantees.</span></span>

<span data-ttu-id="165a9-186">Þú getur bætt við vátryggingagerðum á síðunni **Gerðir vátrygginga** (**Lánastjórnun \> Uppsetning \> Uppsetning á ábyrgð/tryggingu \> Gerðir vátrygginga**).</span><span class="sxs-lookup"><span data-stu-id="165a9-186">You can add coverage types on the **Coverage types** page (**Credit management \> Setup \> Guarantee/insurance setup \> Coverage types**).</span></span>

1. <span data-ttu-id="165a9-187">Sláðu inn gerð vátryggingar til að bera kennsl á gerð vátryggingar sem ætti að bæta við sem tryggingu eða ábyrgð.</span><span class="sxs-lookup"><span data-stu-id="165a9-187">Enter a coverage type to identify the type of coverage that should be added as insurance or a guarantee.</span></span>
2. <span data-ttu-id="165a9-188">Færa inn lýsingu til að lýsa gerð vátryggingar.</span><span class="sxs-lookup"><span data-stu-id="165a9-188">Enter a description to describe of the coverage type.</span></span>

## <a name="automatic-credit-limits"></a><span data-ttu-id="165a9-189">Sjálfvirk lánamörk</span><span class="sxs-lookup"><span data-stu-id="165a9-189">Automatic credit limits</span></span>

<span data-ttu-id="165a9-190">Þú getur búið til viðmið fyrir sjálfvirk lánamörk á síðunni **Sjálfvirk lánamörk** (**Lánastjórnun \> Uppsetning \> Uppsetning áhættu \> Sjálfvirk lánamörk**).</span><span class="sxs-lookup"><span data-stu-id="165a9-190">You can create criteria for automatic credit limits on the **Automatic credit limits** page (**Credit management \> Setup \> Risk setup \> Automatic credit limits**).</span></span>

1. <span data-ttu-id="165a9-191">Veldu áhættuhóp sem sjálfvirka lánsfjárhæðinni skal úthlutað til.</span><span class="sxs-lookup"><span data-stu-id="165a9-191">Select a risk group that the automatic credit limit should be assigned to.</span></span>
2. <span data-ttu-id="165a9-192">Veldu gjaldmiðil fyrir sjálfvirka lánamörk.</span><span class="sxs-lookup"><span data-stu-id="165a9-192">Select the currency for the automatic credit limit.</span></span> <span data-ttu-id="165a9-193">Þú getur búið til mörg sjálfvirk lánamörk í mismunandi gjaldmiðlum fyrir sama áhættuhóp.</span><span class="sxs-lookup"><span data-stu-id="165a9-193">You can create multiple automatic credit limits in different currencies for the same risk group.</span></span>
3. <span data-ttu-id="165a9-194">Sláðu inn tekjuupphæðina sem táknar hámarks tekjur fyrirtækisins sem hægt er að nota fyrir þetta sjálfvirka lánamörk.</span><span class="sxs-lookup"><span data-stu-id="165a9-194">Enter the revenue amount that represents the maximum company revenue that can be used for this automatic credit limit.</span></span> <span data-ttu-id="165a9-195">Þegar lánamörk eru búin til er tekjufjárhæðin borin saman við tekjuvirði sem er að finna á síðunni **Fjármál** (**Viðskiptakröfur \> Allir viðskiptavinir \> Veldu viðskiptavin \> Almennt \> Talnagögn \> Fjármál**).</span><span class="sxs-lookup"><span data-stu-id="165a9-195">When credit limits are created, the revenue amount is compared to a revenue value that is found on the **Financials** page (**Accounts receivable \> All customers \> Select a customer \> General \> Statistics \> Financial**).</span></span> <span data-ttu-id="165a9-196">Kerfið notar nýjasta gildi í kaflanum **Yfirlit**.</span><span class="sxs-lookup"><span data-stu-id="165a9-196">The system uses the latest value in the **Overview** section.</span></span>

<span data-ttu-id="165a9-197">Fylgdu þessum skrefum til að bæta við línum sem tákna lánamörk sem verða til miðað við valin viðmið.</span><span class="sxs-lookup"><span data-stu-id="165a9-197">Follow these steps to add lines that represent the credit limit that will be generated based on the selected criteria.</span></span>

1. <span data-ttu-id="165a9-198">Veldu stigahópinn sem skilgreinir viðskiptavinaupplýsingarnar sem ætti að nota til að reikna út lánamörkin.</span><span class="sxs-lookup"><span data-stu-id="165a9-198">Select the scoring group that defines the customer information that should be used to calculate the credit limit.</span></span>
2. <span data-ttu-id="165a9-199">Veldu samanburðarstjórann sem skilgreinir hvernig meta skal upplýsingar um stigahópinn.</span><span class="sxs-lookup"><span data-stu-id="165a9-199">Select the comparison operator that defines how the scoring group information should be evaluated.</span></span>
3. <span data-ttu-id="165a9-200">Sláðu inn gildi sem ber að bera saman við gildi sem er tilgreint fyrir stigahópinn.</span><span class="sxs-lookup"><span data-stu-id="165a9-200">Enter the value that should be compared to the value that is specified for the scoring group.</span></span>
4. <span data-ttu-id="165a9-201">Sláðu inn lánsfjárhæðina sem ætti að vera úthlutað ef viðskiptavinaupplýsingin samsvarar gildinu sem er tilgreint fyrir stigahópinn.</span><span class="sxs-lookup"><span data-stu-id="165a9-201">Enter the credit limit that should be assigned if the customer information matches the value that is specified for the scoring group.</span></span> <span data-ttu-id="165a9-202">Til dæmis stofnarðu sjálfvirka lánamörk fyrir stigahópinn **Lágt**.</span><span class="sxs-lookup"><span data-stu-id="165a9-202">For example, you create an automatic credit limit for the **Low** scoring group.</span></span> <span data-ttu-id="165a9-203">Ef árin í viðskiptum eru einn af stigahópunum geturðu skilgreint eina línu sem úthlutar 100.000 lánamörkum ef viðskiptavinurinn hefur verið í viðskiptum í fimm ár og önnur lína sem úthlutar 200.000 kreditmörkum ef viðskiptavinurinn hefur verið í viðskiptum í 10 ár.</span><span class="sxs-lookup"><span data-stu-id="165a9-203">If the years in business is one of the scoring groups, you can define one line that assigns a 100,000 credit limit if the customer has been in business five years and another line that assigns a 200,000 credit limit if the customer has been in business for 10 years.</span></span>
