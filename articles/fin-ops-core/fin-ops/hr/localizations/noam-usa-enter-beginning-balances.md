---
title: Innskráning á upphafsstöðu launa
description: Þetta efnisatriði lýsir skrefum fyrir innskráningu á upphafsstöðu fyrir tekjukóða, frádrátt, fríðindi og skatta. Þessar upplýsingar eru mikilvægar fyrir samstarfsaðila til að yfirfæra eða flytja gögn fyrir nýja launainnleiðingu úr öðru kerfi.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8443bc5c63a90d80757ab4b7507502497c2aaa69
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 12/19/2020
ms.locfileid: "4797785"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="e853b-104">Innskráning á upphafsstöðu launa</span><span class="sxs-lookup"><span data-stu-id="e853b-104">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e853b-105">Þetta efnisatriði lýsir skrefum fyrir innskráningu á upphafsstöðu fyrir tekjukóða, frádrátt, fríðindi og skatta.</span><span class="sxs-lookup"><span data-stu-id="e853b-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="e853b-106">Þessar upplýsingar eru mikilvægar fyrir samstarfsaðila sem flytja gögn fyrir nýja launainnleiðingu úr öðru kerfi.</span><span class="sxs-lookup"><span data-stu-id="e853b-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="e853b-107">Til að undirbúa innskráningu launastöðu, staðfestum við eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="e853b-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="e853b-108">Starfsmannafærslur eru innskráðar og tiltækar í kerfinu</span><span class="sxs-lookup"><span data-stu-id="e853b-108">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="e853b-109">Eftirfarandi gögn eru sett upp og úthlutuð starfsmönnum:</span><span class="sxs-lookup"><span data-stu-id="e853b-109">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="e853b-110">Greiðsluferli og launatímabil</span><span class="sxs-lookup"><span data-stu-id="e853b-110">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="e853b-111">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="e853b-111">Earning codes</span></span>
    - <span data-ttu-id="e853b-112">Skattar</span><span class="sxs-lookup"><span data-stu-id="e853b-112">Taxes</span></span>
    - <span data-ttu-id="e853b-113">Hlunnindi og frádráttur</span><span class="sxs-lookup"><span data-stu-id="e853b-113">Benefits and deductions</span></span>

- <span data-ttu-id="e853b-114">Fyrirtækið ætti að hafa valið dagsetningu sem stilla á upphafsstöðu launa eftir.</span><span class="sxs-lookup"><span data-stu-id="e853b-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="e853b-115">Upplýsingum var safnað um allar tekjur, fríðindi/frádrátt, fríðindaframlög, starfsmannaskatt og vinnuveitendaskatt og upphæðir á árinu úr eldra kerfi.</span><span class="sxs-lookup"><span data-stu-id="e853b-115">Information was gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="e853b-116">Þar sem ætlunin er að skrá inn upphafsstöður skal hafa í huga hversu ítarleg gögnin þurfa að vera.</span><span class="sxs-lookup"><span data-stu-id="e853b-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="e853b-117">Flest fyrirtæki skrá eina, sameinaða upphæð það sem af er ári.</span><span class="sxs-lookup"><span data-stu-id="e853b-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="e853b-118">Hins vegar má skrá uppsafnaðar upphæðir ársfjórðungslega ef þörf er á ítarlegri upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="e853b-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="e853b-119">Það hversu ítarlegar upplýsingarnar þurfa að vera sker úr um hversu mörg handvirk launayfirlit þarf að stofna fyrir hvern starfsmann.</span><span class="sxs-lookup"><span data-stu-id="e853b-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="e853b-120">Ef um er að ræða eina upphæð fyrir það sem af er ári, þarf aðeins eitt handvirkt yfirlit fyrir hvern starfsmann.</span><span class="sxs-lookup"><span data-stu-id="e853b-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="e853b-121">Til að gera þetta skal nota upphæðir það sem af er ári úr endanlegu launayfirliti úr fyrra kerfi sem upphæðina sem er færð inn í nýja launakerfið.</span><span class="sxs-lookup"><span data-stu-id="e853b-121">To do this, use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="e853b-122">Eftirfarandi dæmi sýnir hvernig hægt er að færa upphafsstöðu launa fyrir starfsmanninn, þar á meðal tekjukóða, fríðindi/frádrátt og skatta.</span><span class="sxs-lookup"><span data-stu-id="e853b-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="e853b-123">Í raunverulegu dæmi myndir þú hafa línuatriði fyrir hvern tekjukóða, frádrátt fríðinda, fríðindaframlag, skatta starfsmanns og skatta vinnuveitanda með upphæðinni sem skráð er sem upphæð það sem af er ári.</span><span class="sxs-lookup"><span data-stu-id="e853b-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="e853b-124">Notaðu þann lista yfir kóða og upphæðir og fylgdu skrefunum fyrir stofnun handvirkra tekju- og launayfirlita með bókhald afvirkjað, til að flytja yfir upphafsstöður fyrir laun.</span><span class="sxs-lookup"><span data-stu-id="e853b-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="e853b-125">Bókhald er afvirkjað þar sem þú vilt ekki bóka þessa upphafsstöðu launayfirlits í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="e853b-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="e853b-126">Það var gert í eldra kerfinu og kemur yfir í nýja kerfið þegar upphafsstöður eru settar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="e853b-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="e853b-127">A.</span><span class="sxs-lookup"><span data-stu-id="e853b-127">A.</span></span> <span data-ttu-id="e853b-128">Uppsetning tekjukóða sem nota á í upphafsstöðu launa</span><span class="sxs-lookup"><span data-stu-id="e853b-128">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="e853b-129">Þegar upphafsstöður launa eru slegnar inn, gakktu þá úr skugga um að tekjukóðarnir sem þú notar séu skilgreindir með valkostinn „Leyfa breytingar á töxtum í tekjuyfirliti“ virkjaðan.</span><span class="sxs-lookup"><span data-stu-id="e853b-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="e853b-130">Það gerir þér kleift að lykla upphæðina handvirkt úr eldra kerfinu.</span><span class="sxs-lookup"><span data-stu-id="e853b-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="e853b-131">B.</span><span class="sxs-lookup"><span data-stu-id="e853b-131">B.</span></span> <span data-ttu-id="e853b-132">Stofna tekjuyfirlit svo starfsmaður fái upphafsstöðu</span><span class="sxs-lookup"><span data-stu-id="e853b-132">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="e853b-133">Þetta skref stofnar tekjuyfirlit handvirkt fyrir hvern starfsmann fyrir síðasta launatímabil eldra kerfisins, sem stofnar launayfirlitslínur í nýja launakerfinu.</span><span class="sxs-lookup"><span data-stu-id="e853b-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="e853b-134">Færðu inn eina línu fyrir hvern tekjukóða og upphæðir og tíma fyrir það sem af er ári.</span><span class="sxs-lookup"><span data-stu-id="e853b-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="e853b-135">Sýnisskrefin eru sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="e853b-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="e853b-136">Opnaðu síðuna **Öll tekjuyfirlit** og smelltu á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e853b-136">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="e853b-137">Færa inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="e853b-137">Enter the following:</span></span> 

    | <span data-ttu-id="e853b-138">Svæði</span><span class="sxs-lookup"><span data-stu-id="e853b-138">Field</span></span>      | <span data-ttu-id="e853b-139">Virði</span><span class="sxs-lookup"><span data-stu-id="e853b-139">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="e853b-140">Starfskraftur</span><span class="sxs-lookup"><span data-stu-id="e853b-140">Worker</span></span>     | <span data-ttu-id="e853b-141">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="e853b-141">Michael Redmond</span></span>       |
    | <span data-ttu-id="e853b-142">Greiðsluferli</span><span class="sxs-lookup"><span data-stu-id="e853b-142">Pay cycle</span></span>  | <span data-ttu-id="e853b-143">sm</span><span class="sxs-lookup"><span data-stu-id="e853b-143">sm</span></span>                    |
    | <span data-ttu-id="e853b-144">Launatímabil</span><span class="sxs-lookup"><span data-stu-id="e853b-144">Pay period</span></span> | <span data-ttu-id="e853b-145">6/16/2017 - 6/30/2017</span><span class="sxs-lookup"><span data-stu-id="e853b-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="e853b-146">Á flipanum **Tekjuyfirlitslínur** færirðu inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="e853b-146">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="e853b-147">Lína 1: Flipinn **Tekjuyfirlitslína**</span><span class="sxs-lookup"><span data-stu-id="e853b-147">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="e853b-148">Svæði</span><span class="sxs-lookup"><span data-stu-id="e853b-148">Field</span></span>            | <span data-ttu-id="e853b-149">Virði</span><span class="sxs-lookup"><span data-stu-id="e853b-149">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="e853b-150">Tekjukóði</span><span class="sxs-lookup"><span data-stu-id="e853b-150">Earnings code</span></span>    | <span data-ttu-id="e853b-151">Regluleg laun</span><span class="sxs-lookup"><span data-stu-id="e853b-151">Regular pay</span></span> |
    | <span data-ttu-id="e853b-152">Magn</span><span class="sxs-lookup"><span data-stu-id="e853b-152">Quantity</span></span>         | <span data-ttu-id="e853b-153">1.00</span><span class="sxs-lookup"><span data-stu-id="e853b-153">1.00</span></span>        |
    | <span data-ttu-id="e853b-154">Taxti</span><span class="sxs-lookup"><span data-stu-id="e853b-154">Rate</span></span>             | <span data-ttu-id="e853b-155">30,000</span><span class="sxs-lookup"><span data-stu-id="e853b-155">30,000</span></span>      |
    | <span data-ttu-id="e853b-156">Flipi fyrir línuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="e853b-156">Line details tab</span></span> |             |
    | <span data-ttu-id="e853b-157">Handbók</span><span class="sxs-lookup"><span data-stu-id="e853b-157">Manual</span></span>           | <span data-ttu-id="e853b-158">(merkt)</span><span class="sxs-lookup"><span data-stu-id="e853b-158">(marked)</span></span>    |

    <span data-ttu-id="e853b-159">Lína 2: Flipinn **Tekjuyfirlitslína**</span><span class="sxs-lookup"><span data-stu-id="e853b-159">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="e853b-160">Svæði</span><span class="sxs-lookup"><span data-stu-id="e853b-160">Field</span></span>            | <span data-ttu-id="e853b-161">Virði</span><span class="sxs-lookup"><span data-stu-id="e853b-161">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="e853b-162">Tekjukóði</span><span class="sxs-lookup"><span data-stu-id="e853b-162">Earnings code</span></span>    | <span data-ttu-id="e853b-163">Kaupauki</span><span class="sxs-lookup"><span data-stu-id="e853b-163">Bonus</span></span>    |
    | <span data-ttu-id="e853b-164">Magn</span><span class="sxs-lookup"><span data-stu-id="e853b-164">Quantity</span></span>         | <span data-ttu-id="e853b-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="e853b-165">1.0000</span></span>   |
    | <span data-ttu-id="e853b-166">Taxti</span><span class="sxs-lookup"><span data-stu-id="e853b-166">Rate</span></span>             | <span data-ttu-id="e853b-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="e853b-167">4250.00</span></span>  |
    | <span data-ttu-id="e853b-168">Flipi fyrir línuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="e853b-168">Line details tab</span></span> |          |
    | <span data-ttu-id="e853b-169">Handvirkt</span><span class="sxs-lookup"><span data-stu-id="e853b-169">Manual</span></span>           | <span data-ttu-id="e853b-170">(merkt)</span><span class="sxs-lookup"><span data-stu-id="e853b-170">(marked)</span></span> |

    <span data-ttu-id="e853b-171">Lína 3: Flipinn **Tekjuyfirlitslína**</span><span class="sxs-lookup"><span data-stu-id="e853b-171">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="e853b-172">Svæði</span><span class="sxs-lookup"><span data-stu-id="e853b-172">Field</span></span>           | <span data-ttu-id="e853b-173">Virði</span><span class="sxs-lookup"><span data-stu-id="e853b-173">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="e853b-174">Tekjukóði</span><span class="sxs-lookup"><span data-stu-id="e853b-174">Earnings code</span></span>   | <span data-ttu-id="e853b-175">Þóknun</span><span class="sxs-lookup"><span data-stu-id="e853b-175">Commission</span></span> |
    | <span data-ttu-id="e853b-176">Magn</span><span class="sxs-lookup"><span data-stu-id="e853b-176">Quantity</span></span>        | <span data-ttu-id="e853b-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="e853b-177">1.0000</span></span>     |
    | <span data-ttu-id="e853b-178">Taxti</span><span class="sxs-lookup"><span data-stu-id="e853b-178">Rate</span></span>            | <span data-ttu-id="e853b-179">!,299.00</span><span class="sxs-lookup"><span data-stu-id="e853b-179">!,299.00</span></span>   |
    | <span data-ttu-id="e853b-180">Taxti</span><span class="sxs-lookup"><span data-stu-id="e853b-180">Rate</span></span>            | <span data-ttu-id="e853b-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="e853b-181">1,299.00</span></span>   |
    | <span data-ttu-id="e853b-182">Flipi fyrir línuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="e853b-182">Line detail tab</span></span> |            |
    | <span data-ttu-id="e853b-183">Handvirkt</span><span class="sxs-lookup"><span data-stu-id="e853b-183">Manual</span></span>          | <span data-ttu-id="e853b-184">(merkt)</span><span class="sxs-lookup"><span data-stu-id="e853b-184">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="e853b-185">Það að stilla sleðann **Handvirkt** á **Já** á flipanum **Línuupplýsingar** fyrir hverja tekjuyfirlitslínu er lykillinn að því að láta skrá inn upphafsstöðu launa fyrir hvern starfsmann.</span><span class="sxs-lookup"><span data-stu-id="e853b-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="e853b-186">Á rúðunni **Aðgerð** smellirðu á **Birta tekjuyfirlit** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="e853b-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="e853b-187">Á rúðunni **Aðgerð** smellirðu á **Launayfirlit** til að opna síðuna **Búa til launayfirlit** og stillir eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="e853b-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="e853b-188">Svæði</span><span class="sxs-lookup"><span data-stu-id="e853b-188">Field</span></span>              | <span data-ttu-id="e853b-189">Virði</span><span class="sxs-lookup"><span data-stu-id="e853b-189">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="e853b-190">Dagsetning greiðslu</span><span class="sxs-lookup"><span data-stu-id="e853b-190">Payment date</span></span>       | <span data-ttu-id="e853b-191">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="e853b-191">6/30/2017</span></span> |
    | <span data-ttu-id="e853b-192">Keyrslugerð greiðslu</span><span class="sxs-lookup"><span data-stu-id="e853b-192">Payment run type</span></span>   | <span data-ttu-id="e853b-193">Handvirkt</span><span class="sxs-lookup"><span data-stu-id="e853b-193">Manual</span></span>    |
    | <span data-ttu-id="e853b-194">Gera bókhald óvirkt</span><span class="sxs-lookup"><span data-stu-id="e853b-194">Disable accounting</span></span> |   <span data-ttu-id="e853b-195">Já</span><span class="sxs-lookup"><span data-stu-id="e853b-195">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="e853b-196">Þetta er aðeins í boði þegar keyrslugerð launa er handvirk og þar sem notandinn vill afvirkja bókhald í launakeyrslu.</span><span class="sxs-lookup"><span data-stu-id="e853b-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="e853b-197">Smelltu á **Í lagi** og lokaðu **Athugasemdum**.</span><span class="sxs-lookup"><span data-stu-id="e853b-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="e853b-198">Af hverju þarf að setja sleðann Gera bókhald óvirkt á Já þegar launayfirlit eru búin til?</span><span class="sxs-lookup"><span data-stu-id="e853b-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="e853b-199">Ef sleðinn er stilltur á **Já** kemur hann í veg fyrir að línum í launayfirliti sé dreift í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="e853b-199">Setting the slider to **Yes** prevents lines in the pay statement from being distributed to General ledger.</span></span> <span data-ttu-id="e853b-200">Fjárhagsupphæðir voru í uppfærslu áður þegar lykilstöður úr eldra kerfinu voru færðar inn.</span><span class="sxs-lookup"><span data-stu-id="e853b-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="e853b-201">Ef færðar eru inn upphafsstöður fyrir Laun er hægt að búa til skýrslur sem innihalda upplýsingar frá fyrri árum, sem og að auðkenna mörk fyrir fríðindi og skatta.</span><span class="sxs-lookup"><span data-stu-id="e853b-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="e853b-202">C.</span><span class="sxs-lookup"><span data-stu-id="e853b-202">C.</span></span> <span data-ttu-id="e853b-203">Stofna launayfirlit fyrir starfsmenn</span><span class="sxs-lookup"><span data-stu-id="e853b-203">Create pay statements for employees</span></span>

<span data-ttu-id="e853b-204">Eftir að þú hefur búið til launayfirlit sem hafa upphafsstöður verður þú að sannreyna að launayfirlit endurspegli launagögn réttilega.</span><span class="sxs-lookup"><span data-stu-id="e853b-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="e853b-205">Þú verður einnig að uppfæra upplýsingar um fríðindi og skatta handvirkt þannig að þær passi við gildin í fyrra launakerfi.</span><span class="sxs-lookup"><span data-stu-id="e853b-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="e853b-206">Þegar búið er að sannreyna að upphæðir úr fyrra launakerfi séu þær sömu og á núverandi launayfirlitum, verður þú að leggja lokahönd á launayfirlitin.</span><span class="sxs-lookup"><span data-stu-id="e853b-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="e853b-207">Opnaðu síðuna **Öll launayfirlit**.</span><span class="sxs-lookup"><span data-stu-id="e853b-207">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="e853b-208">Merktu síðasta launayfirlit fyrir Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="e853b-208">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="e853b-209">Smelltu á **Breyta** til að opna síðuna **Launayfirlit**.</span><span class="sxs-lookup"><span data-stu-id="e853b-209">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="e853b-210">Opnaðu flipann **Frádráttur fríðinda** og sláðu inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="e853b-210">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="e853b-211">Svæði</span><span class="sxs-lookup"><span data-stu-id="e853b-211">Field</span></span>             | <span data-ttu-id="e853b-212">Virði</span><span class="sxs-lookup"><span data-stu-id="e853b-212">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="e853b-213">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="e853b-213">Benefit</span></span>           | <span data-ttu-id="e853b-214">Upphæð frádráttar</span><span class="sxs-lookup"><span data-stu-id="e853b-214">Deduction amount</span></span> |
    | <span data-ttu-id="e853b-215">401K</span><span class="sxs-lookup"><span data-stu-id="e853b-215">401K</span></span>              | <span data-ttu-id="e853b-216">Þátttaka</span><span class="sxs-lookup"><span data-stu-id="e853b-216">Participate</span></span>      |
    | <span data-ttu-id="e853b-217">Tannlæknistrygging</span><span class="sxs-lookup"><span data-stu-id="e853b-217">Dental</span></span>            | <span data-ttu-id="e853b-218">SubSp</span><span class="sxs-lookup"><span data-stu-id="e853b-218">SubSp</span></span>            |
    | <span data-ttu-id="e853b-219">Kostnaður við tryggingar skjólstæðinga</span><span class="sxs-lookup"><span data-stu-id="e853b-219">Dep care spending</span></span> | <span data-ttu-id="e853b-220">Þátttaka</span><span class="sxs-lookup"><span data-stu-id="e853b-220">Participate</span></span>      |
    | <span data-ttu-id="e853b-221">Framtíðarsýn</span><span class="sxs-lookup"><span data-stu-id="e853b-221">Vision</span></span>            | <span data-ttu-id="e853b-222">SupSp</span><span class="sxs-lookup"><span data-stu-id="e853b-222">SupSp</span></span>            |

5. <span data-ttu-id="e853b-223">Á flipanum **Fríðindaframlög** slærðu inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="e853b-223">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="e853b-224">Svæði</span><span class="sxs-lookup"><span data-stu-id="e853b-224">Field</span></span>   | <span data-ttu-id="e853b-225">Virði</span><span class="sxs-lookup"><span data-stu-id="e853b-225">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="e853b-226">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="e853b-226">Benefit</span></span> | <span data-ttu-id="e853b-227">Upphæð framlags</span><span class="sxs-lookup"><span data-stu-id="e853b-227">Contribution amount</span></span> |
    | <span data-ttu-id="e853b-228">401K</span><span class="sxs-lookup"><span data-stu-id="e853b-228">401K</span></span>    | <span data-ttu-id="e853b-229">Þátttaka</span><span class="sxs-lookup"><span data-stu-id="e853b-229">Participate</span></span>         |
    | <span data-ttu-id="e853b-230">Tannlæknistrygging</span><span class="sxs-lookup"><span data-stu-id="e853b-230">Dental</span></span>  | <span data-ttu-id="e853b-231">SubSp</span><span class="sxs-lookup"><span data-stu-id="e853b-231">SubSp</span></span>               |
    | <span data-ttu-id="e853b-232">Framtíðarsýn</span><span class="sxs-lookup"><span data-stu-id="e853b-232">Vision</span></span>  | <span data-ttu-id="e853b-233">SubSp</span><span class="sxs-lookup"><span data-stu-id="e853b-233">SubSp</span></span>               |

6. <span data-ttu-id="e853b-234">Á flipanum **Skattafrádráttur** slærðu inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="e853b-234">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="e853b-235">Svæði</span><span class="sxs-lookup"><span data-stu-id="e853b-235">Field</span></span>           | <span data-ttu-id="e853b-236">Virði</span><span class="sxs-lookup"><span data-stu-id="e853b-236">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="e853b-237">Skattkóði</span><span class="sxs-lookup"><span data-stu-id="e853b-237">Tax code</span></span>        | <span data-ttu-id="e853b-238">Upphæð frádráttar</span><span class="sxs-lookup"><span data-stu-id="e853b-238">Deduction amount</span></span> |
    | <span data-ttu-id="e853b-239">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="e853b-239">USA-FED-ER-FICA</span></span> | <span data-ttu-id="e853b-240">1600.00</span><span class="sxs-lookup"><span data-stu-id="e853b-240">1600.00</span></span>          |
    | <span data-ttu-id="e853b-241">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="e853b-241">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="e853b-242">825.75</span><span class="sxs-lookup"><span data-stu-id="e853b-242">825.75</span></span>           |

7. <span data-ttu-id="e853b-243">Á flipanum **Skattaframlög** slærðu inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="e853b-243">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="e853b-244">Smelltu á **Reikna út**.</span><span class="sxs-lookup"><span data-stu-id="e853b-244">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="e853b-245">Villuleitaðu samtölur launayfirlita þannig að þær passi við tölur það sem af er ári úr eldra kerfi fyrir starfsmanninn.</span><span class="sxs-lookup"><span data-stu-id="e853b-245">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="e853b-246">Það gæti verið ráðlegt að bíða með að ljúka við næsta skref, til að villuleita öll launayfirlit saman.</span><span class="sxs-lookup"><span data-stu-id="e853b-246">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="e853b-247">Þegar öll launayfirlit hafa verið villuleituð ferðu í gegnum þau og leggur lokahönd á þau.</span><span class="sxs-lookup"><span data-stu-id="e853b-247">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="e853b-248">Hægt er að framkvæma sama ferlið uppsafnað ársfjórðungslega ef það er nauðsynlegt fyrir alla fyrri fjórðunga hvert ár.</span><span class="sxs-lookup"><span data-stu-id="e853b-248">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="e853b-249">Þetta er aðeins nauðsynlegt ef viðskiptavinurinn þarf að skoða gögnin eftir ársfjórðungum án þess að fara aftur í eldra kerfið.</span><span class="sxs-lookup"><span data-stu-id="e853b-249">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="e853b-250">Ef þú gerir mistök við skráningu upphafsstöðu fyrir starfsmann</span><span class="sxs-lookup"><span data-stu-id="e853b-250">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="e853b-251">Er mögulegt að bakfæra og endurskrá færslur.</span><span class="sxs-lookup"><span data-stu-id="e853b-251">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="e853b-252">Til að bakfæra færsluna þarftu bara að ljúka við eftirfarandi skref á síðunni **Öll launayfirlit**.</span><span class="sxs-lookup"><span data-stu-id="e853b-252">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="e853b-253">Smelltu á **Bakfæra**.</span><span class="sxs-lookup"><span data-stu-id="e853b-253">Click **Reverse**.</span></span>
2. <span data-ttu-id="e853b-254">Smelltu á **Já** þegar skilaboðin „Þegar þetta launayfirlit er bakfært verður launayfirlit bakfærslu stofnað fyrir mótbókun á þessu launayfirliti.</span><span class="sxs-lookup"><span data-stu-id="e853b-254">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="e853b-255">Hvorugu launayfirlitinu er hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="e853b-255">Neither pay statement can be edited.</span></span> <span data-ttu-id="e853b-256">Á að bakfæra þetta launayfirlit?“</span><span class="sxs-lookup"><span data-stu-id="e853b-256">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="e853b-257">birtast.</span><span class="sxs-lookup"><span data-stu-id="e853b-257">displays.</span></span> 

<span data-ttu-id="e853b-258">Eftir að launayfirlitið hefur verið bakfært geturðu búið til nýtt launayfirlit fyrir starfsmanninn úr tekjuyfirlitinu sem þú bjóst til áður.</span><span class="sxs-lookup"><span data-stu-id="e853b-258">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="e853b-259">Gættu þess að lagfæra allar rangar línur á tekjuyfirlitinu áður en þú býrð til nýtt launauppgjör, og búðu svo til ný launayfirlit með réttum upphæðum.</span><span class="sxs-lookup"><span data-stu-id="e853b-259">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 
