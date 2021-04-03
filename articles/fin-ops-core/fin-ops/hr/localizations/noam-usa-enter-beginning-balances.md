---
title: Innskráning á upphafsstöðu launa
description: Þetta efnisatriði lýsir skrefum fyrir innskráningu á upphafsstöðu fyrir tekjukóða, frádrátt, fríðindi og skatta. Þessar upplýsingar eru mikilvægar fyrir samstarfsaðila til að yfirfæra eða flytja gögn fyrir nýja launainnleiðingu úr öðru kerfi.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 209636d6416a784d298bcfb134f5486c1f5cf202
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568546"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="56614-104">Innskráning á upphafsstöðu launa</span><span class="sxs-lookup"><span data-stu-id="56614-104">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="56614-105">Þetta efnisatriði lýsir skrefum fyrir innskráningu á upphafsstöðu fyrir tekjukóða, frádrátt, fríðindi og skatta.</span><span class="sxs-lookup"><span data-stu-id="56614-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="56614-106">Þessar upplýsingar eru mikilvægar fyrir samstarfsaðila sem flytja gögn fyrir nýja launainnleiðingu úr öðru kerfi.</span><span class="sxs-lookup"><span data-stu-id="56614-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="56614-107">Til að undirbúa innskráningu launastöðu, staðfestum við eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="56614-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="56614-108">Starfsmannafærslur eru innskráðar og tiltækar í kerfinu</span><span class="sxs-lookup"><span data-stu-id="56614-108">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="56614-109">Eftirfarandi gögn eru sett upp og úthlutuð starfsmönnum:</span><span class="sxs-lookup"><span data-stu-id="56614-109">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="56614-110">Greiðsluferli og launatímabil</span><span class="sxs-lookup"><span data-stu-id="56614-110">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="56614-111">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="56614-111">Earning codes</span></span>
    - <span data-ttu-id="56614-112">Skattar</span><span class="sxs-lookup"><span data-stu-id="56614-112">Taxes</span></span>
    - <span data-ttu-id="56614-113">Hlunnindi og frádráttur</span><span class="sxs-lookup"><span data-stu-id="56614-113">Benefits and deductions</span></span>

- <span data-ttu-id="56614-114">Fyrirtækið ætti að hafa valið dagsetningu sem stilla á upphafsstöðu launa eftir.</span><span class="sxs-lookup"><span data-stu-id="56614-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="56614-115">Upplýsingum var safnað um allar tekjur, fríðindi/frádrátt, fríðindaframlög, starfsmannaskatt og vinnuveitendaskatt og upphæðir á árinu úr eldra kerfi.</span><span class="sxs-lookup"><span data-stu-id="56614-115">Information was gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="56614-116">Þar sem ætlunin er að skrá inn upphafsstöður skal hafa í huga hversu ítarleg gögnin þurfa að vera.</span><span class="sxs-lookup"><span data-stu-id="56614-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="56614-117">Flest fyrirtæki skrá eina, sameinaða upphæð það sem af er ári.</span><span class="sxs-lookup"><span data-stu-id="56614-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="56614-118">Hins vegar má skrá uppsafnaðar upphæðir ársfjórðungslega ef þörf er á ítarlegri upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="56614-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="56614-119">Það hversu ítarlegar upplýsingarnar þurfa að vera sker úr um hversu mörg handvirk launayfirlit þarf að stofna fyrir hvern starfsmann.</span><span class="sxs-lookup"><span data-stu-id="56614-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="56614-120">Ef um er að ræða eina upphæð fyrir það sem af er ári, þarf aðeins eitt handvirkt yfirlit fyrir hvern starfsmann.</span><span class="sxs-lookup"><span data-stu-id="56614-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="56614-121">Til að gera þetta skal nota upphæðir það sem af er ári úr endanlegu launayfirliti úr fyrra kerfi sem upphæðina sem er færð inn í nýja launakerfið.</span><span class="sxs-lookup"><span data-stu-id="56614-121">To do this, use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="56614-122">Eftirfarandi dæmi sýnir hvernig hægt er að færa upphafsstöðu launa fyrir starfsmanninn, þar á meðal tekjukóða, fríðindi/frádrátt og skatta.</span><span class="sxs-lookup"><span data-stu-id="56614-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="56614-123">Í raunverulegu dæmi myndir þú hafa línuatriði fyrir hvern tekjukóða, frádrátt fríðinda, fríðindaframlag, skatta starfsmanns og skatta vinnuveitanda með upphæðinni sem skráð er sem upphæð það sem af er ári.</span><span class="sxs-lookup"><span data-stu-id="56614-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="56614-124">Notaðu þann lista yfir kóða og upphæðir og fylgdu skrefunum fyrir stofnun handvirkra tekju- og launayfirlita með bókhald afvirkjað, til að flytja yfir upphafsstöður fyrir laun.</span><span class="sxs-lookup"><span data-stu-id="56614-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="56614-125">Bókhald er afvirkjað þar sem þú vilt ekki bóka þessa upphafsstöðu launayfirlits í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="56614-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="56614-126">Það var gert í eldra kerfinu og kemur yfir í nýja kerfið þegar upphafsstöður eru settar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="56614-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="56614-127">A.</span><span class="sxs-lookup"><span data-stu-id="56614-127">A.</span></span> <span data-ttu-id="56614-128">Uppsetning tekjukóða sem nota á í upphafsstöðu launa</span><span class="sxs-lookup"><span data-stu-id="56614-128">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="56614-129">Þegar upphafsstöður launa eru slegnar inn, gakktu þá úr skugga um að tekjukóðarnir sem þú notar séu skilgreindir með valkostinn „Leyfa breytingar á töxtum í tekjuyfirliti“ virkjaðan.</span><span class="sxs-lookup"><span data-stu-id="56614-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="56614-130">Það gerir þér kleift að lykla upphæðina handvirkt úr eldra kerfinu.</span><span class="sxs-lookup"><span data-stu-id="56614-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="56614-131">B.</span><span class="sxs-lookup"><span data-stu-id="56614-131">B.</span></span> <span data-ttu-id="56614-132">Stofna tekjuyfirlit svo starfsmaður fái upphafsstöðu</span><span class="sxs-lookup"><span data-stu-id="56614-132">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="56614-133">Þetta skref stofnar tekjuyfirlit handvirkt fyrir hvern starfsmann fyrir síðasta launatímabil eldra kerfisins, sem stofnar launayfirlitslínur í nýja launakerfinu.</span><span class="sxs-lookup"><span data-stu-id="56614-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="56614-134">Færðu inn eina línu fyrir hvern tekjukóða og upphæðir og tíma fyrir það sem af er ári.</span><span class="sxs-lookup"><span data-stu-id="56614-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="56614-135">Sýnisskrefin eru sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="56614-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="56614-136">Opnaðu síðuna **Öll tekjuyfirlit** og smelltu á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="56614-136">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="56614-137">Færa inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="56614-137">Enter the following:</span></span> 

    | <span data-ttu-id="56614-138">Svæði</span><span class="sxs-lookup"><span data-stu-id="56614-138">Field</span></span>      | <span data-ttu-id="56614-139">Virði</span><span class="sxs-lookup"><span data-stu-id="56614-139">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="56614-140">Starfskraftur</span><span class="sxs-lookup"><span data-stu-id="56614-140">Worker</span></span>     | <span data-ttu-id="56614-141">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="56614-141">Michael Redmond</span></span>       |
    | <span data-ttu-id="56614-142">Greiðsluferli</span><span class="sxs-lookup"><span data-stu-id="56614-142">Pay cycle</span></span>  | <span data-ttu-id="56614-143">sm</span><span class="sxs-lookup"><span data-stu-id="56614-143">sm</span></span>                    |
    | <span data-ttu-id="56614-144">Launatímabil</span><span class="sxs-lookup"><span data-stu-id="56614-144">Pay period</span></span> | <span data-ttu-id="56614-145">6/16/2017 - 6/30/2017</span><span class="sxs-lookup"><span data-stu-id="56614-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="56614-146">Á flipanum **Tekjuyfirlitslínur** færirðu inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="56614-146">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="56614-147">Lína 1: Flipinn **Tekjuyfirlitslína**</span><span class="sxs-lookup"><span data-stu-id="56614-147">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="56614-148">Svæði</span><span class="sxs-lookup"><span data-stu-id="56614-148">Field</span></span>            | <span data-ttu-id="56614-149">Virði</span><span class="sxs-lookup"><span data-stu-id="56614-149">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="56614-150">Tekjukóði</span><span class="sxs-lookup"><span data-stu-id="56614-150">Earnings code</span></span>    | <span data-ttu-id="56614-151">Regluleg laun</span><span class="sxs-lookup"><span data-stu-id="56614-151">Regular pay</span></span> |
    | <span data-ttu-id="56614-152">Magn</span><span class="sxs-lookup"><span data-stu-id="56614-152">Quantity</span></span>         | <span data-ttu-id="56614-153">1.00</span><span class="sxs-lookup"><span data-stu-id="56614-153">1.00</span></span>        |
    | <span data-ttu-id="56614-154">Taxti</span><span class="sxs-lookup"><span data-stu-id="56614-154">Rate</span></span>             | <span data-ttu-id="56614-155">30,000</span><span class="sxs-lookup"><span data-stu-id="56614-155">30,000</span></span>      |
    | <span data-ttu-id="56614-156">Flipi fyrir línuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="56614-156">Line details tab</span></span> |             |
    | <span data-ttu-id="56614-157">Handbók</span><span class="sxs-lookup"><span data-stu-id="56614-157">Manual</span></span>           | <span data-ttu-id="56614-158">(merkt)</span><span class="sxs-lookup"><span data-stu-id="56614-158">(marked)</span></span>    |

    <span data-ttu-id="56614-159">Lína 2: Flipinn **Tekjuyfirlitslína**</span><span class="sxs-lookup"><span data-stu-id="56614-159">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="56614-160">Svæði</span><span class="sxs-lookup"><span data-stu-id="56614-160">Field</span></span>            | <span data-ttu-id="56614-161">Virði</span><span class="sxs-lookup"><span data-stu-id="56614-161">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="56614-162">Tekjukóði</span><span class="sxs-lookup"><span data-stu-id="56614-162">Earnings code</span></span>    | <span data-ttu-id="56614-163">Kaupauki</span><span class="sxs-lookup"><span data-stu-id="56614-163">Bonus</span></span>    |
    | <span data-ttu-id="56614-164">Magn</span><span class="sxs-lookup"><span data-stu-id="56614-164">Quantity</span></span>         | <span data-ttu-id="56614-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="56614-165">1.0000</span></span>   |
    | <span data-ttu-id="56614-166">Taxti</span><span class="sxs-lookup"><span data-stu-id="56614-166">Rate</span></span>             | <span data-ttu-id="56614-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="56614-167">4250.00</span></span>  |
    | <span data-ttu-id="56614-168">Flipi fyrir línuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="56614-168">Line details tab</span></span> |          |
    | <span data-ttu-id="56614-169">Handvirkt</span><span class="sxs-lookup"><span data-stu-id="56614-169">Manual</span></span>           | <span data-ttu-id="56614-170">(merkt)</span><span class="sxs-lookup"><span data-stu-id="56614-170">(marked)</span></span> |

    <span data-ttu-id="56614-171">Lína 3: Flipinn **Tekjuyfirlitslína**</span><span class="sxs-lookup"><span data-stu-id="56614-171">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="56614-172">Svæði</span><span class="sxs-lookup"><span data-stu-id="56614-172">Field</span></span>           | <span data-ttu-id="56614-173">Virði</span><span class="sxs-lookup"><span data-stu-id="56614-173">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="56614-174">Tekjukóði</span><span class="sxs-lookup"><span data-stu-id="56614-174">Earnings code</span></span>   | <span data-ttu-id="56614-175">Þóknun</span><span class="sxs-lookup"><span data-stu-id="56614-175">Commission</span></span> |
    | <span data-ttu-id="56614-176">Magn</span><span class="sxs-lookup"><span data-stu-id="56614-176">Quantity</span></span>        | <span data-ttu-id="56614-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="56614-177">1.0000</span></span>     |
    | <span data-ttu-id="56614-178">Taxti</span><span class="sxs-lookup"><span data-stu-id="56614-178">Rate</span></span>            | <span data-ttu-id="56614-179">!,299.00</span><span class="sxs-lookup"><span data-stu-id="56614-179">!,299.00</span></span>   |
    | <span data-ttu-id="56614-180">Taxti</span><span class="sxs-lookup"><span data-stu-id="56614-180">Rate</span></span>            | <span data-ttu-id="56614-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="56614-181">1,299.00</span></span>   |
    | <span data-ttu-id="56614-182">Flipi fyrir línuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="56614-182">Line detail tab</span></span> |            |
    | <span data-ttu-id="56614-183">Handvirkt</span><span class="sxs-lookup"><span data-stu-id="56614-183">Manual</span></span>          | <span data-ttu-id="56614-184">(merkt)</span><span class="sxs-lookup"><span data-stu-id="56614-184">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="56614-185">Það að stilla sleðann **Handvirkt** á **Já** á flipanum **Línuupplýsingar** fyrir hverja tekjuyfirlitslínu er lykillinn að því að láta skrá inn upphafsstöðu launa fyrir hvern starfsmann.</span><span class="sxs-lookup"><span data-stu-id="56614-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="56614-186">Á rúðunni **Aðgerð** smellirðu á **Birta tekjuyfirlit** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="56614-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="56614-187">Á rúðunni **Aðgerð** smellirðu á **Launayfirlit** til að opna síðuna **Búa til launayfirlit** og stillir eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="56614-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="56614-188">Svæði</span><span class="sxs-lookup"><span data-stu-id="56614-188">Field</span></span>              | <span data-ttu-id="56614-189">Virði</span><span class="sxs-lookup"><span data-stu-id="56614-189">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="56614-190">Dagsetning greiðslu</span><span class="sxs-lookup"><span data-stu-id="56614-190">Payment date</span></span>       | <span data-ttu-id="56614-191">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="56614-191">6/30/2017</span></span> |
    | <span data-ttu-id="56614-192">Keyrslugerð greiðslu</span><span class="sxs-lookup"><span data-stu-id="56614-192">Payment run type</span></span>   | <span data-ttu-id="56614-193">Handvirkt</span><span class="sxs-lookup"><span data-stu-id="56614-193">Manual</span></span>    |
    | <span data-ttu-id="56614-194">Gera bókhald óvirkt</span><span class="sxs-lookup"><span data-stu-id="56614-194">Disable accounting</span></span> |   <span data-ttu-id="56614-195">Já</span><span class="sxs-lookup"><span data-stu-id="56614-195">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="56614-196">Þetta er aðeins í boði þegar keyrslugerð launa er handvirk og þar sem notandinn vill afvirkja bókhald í launakeyrslu.</span><span class="sxs-lookup"><span data-stu-id="56614-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="56614-197">Smelltu á **Í lagi** og lokaðu **Athugasemdum**.</span><span class="sxs-lookup"><span data-stu-id="56614-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="56614-198">Af hverju þarf að setja sleðann Gera bókhald óvirkt á Já þegar launayfirlit eru búin til?</span><span class="sxs-lookup"><span data-stu-id="56614-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="56614-199">Ef sleðinn er stilltur á **Já** kemur hann í veg fyrir að línum í launayfirliti sé dreift í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="56614-199">Setting the slider to **Yes** prevents lines in the pay statement from being distributed to General ledger.</span></span> <span data-ttu-id="56614-200">Fjárhagsupphæðir voru í uppfærslu áður þegar lykilstöður úr eldra kerfinu voru færðar inn.</span><span class="sxs-lookup"><span data-stu-id="56614-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="56614-201">Ef færðar eru inn upphafsstöður fyrir Laun er hægt að búa til skýrslur sem innihalda upplýsingar frá fyrri árum, sem og að auðkenna mörk fyrir fríðindi og skatta.</span><span class="sxs-lookup"><span data-stu-id="56614-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="56614-202">C.</span><span class="sxs-lookup"><span data-stu-id="56614-202">C.</span></span> <span data-ttu-id="56614-203">Stofna launayfirlit fyrir starfsmenn</span><span class="sxs-lookup"><span data-stu-id="56614-203">Create pay statements for employees</span></span>

<span data-ttu-id="56614-204">Eftir að þú hefur búið til launayfirlit sem hafa upphafsstöður verður þú að sannreyna að launayfirlit endurspegli launagögn réttilega.</span><span class="sxs-lookup"><span data-stu-id="56614-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="56614-205">Þú verður einnig að uppfæra upplýsingar um fríðindi og skatta handvirkt þannig að þær passi við gildin í fyrra launakerfi.</span><span class="sxs-lookup"><span data-stu-id="56614-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="56614-206">Þegar búið er að sannreyna að upphæðir úr fyrra launakerfi séu þær sömu og á núverandi launayfirlitum, verður þú að leggja lokahönd á launayfirlitin.</span><span class="sxs-lookup"><span data-stu-id="56614-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="56614-207">Opnaðu síðuna **Öll launayfirlit**.</span><span class="sxs-lookup"><span data-stu-id="56614-207">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="56614-208">Merktu síðasta launayfirlit fyrir Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="56614-208">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="56614-209">Smelltu á **Breyta** til að opna síðuna **Launayfirlit**.</span><span class="sxs-lookup"><span data-stu-id="56614-209">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="56614-210">Opnaðu flipann **Frádráttur fríðinda** og sláðu inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="56614-210">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="56614-211">Svæði</span><span class="sxs-lookup"><span data-stu-id="56614-211">Field</span></span>             | <span data-ttu-id="56614-212">Virði</span><span class="sxs-lookup"><span data-stu-id="56614-212">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="56614-213">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="56614-213">Benefit</span></span>           | <span data-ttu-id="56614-214">Upphæð frádráttar</span><span class="sxs-lookup"><span data-stu-id="56614-214">Deduction amount</span></span> |
    | <span data-ttu-id="56614-215">401K</span><span class="sxs-lookup"><span data-stu-id="56614-215">401K</span></span>              | <span data-ttu-id="56614-216">Þátttaka</span><span class="sxs-lookup"><span data-stu-id="56614-216">Participate</span></span>      |
    | <span data-ttu-id="56614-217">Tannlæknistrygging</span><span class="sxs-lookup"><span data-stu-id="56614-217">Dental</span></span>            | <span data-ttu-id="56614-218">SubSp</span><span class="sxs-lookup"><span data-stu-id="56614-218">SubSp</span></span>            |
    | <span data-ttu-id="56614-219">Kostnaður við tryggingar skjólstæðinga</span><span class="sxs-lookup"><span data-stu-id="56614-219">Dep care spending</span></span> | <span data-ttu-id="56614-220">Þátttaka</span><span class="sxs-lookup"><span data-stu-id="56614-220">Participate</span></span>      |
    | <span data-ttu-id="56614-221">Framtíðarsýn</span><span class="sxs-lookup"><span data-stu-id="56614-221">Vision</span></span>            | <span data-ttu-id="56614-222">SupSp</span><span class="sxs-lookup"><span data-stu-id="56614-222">SupSp</span></span>            |

5. <span data-ttu-id="56614-223">Á flipanum **Fríðindaframlög** slærðu inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="56614-223">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="56614-224">Svæði</span><span class="sxs-lookup"><span data-stu-id="56614-224">Field</span></span>   | <span data-ttu-id="56614-225">Virði</span><span class="sxs-lookup"><span data-stu-id="56614-225">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="56614-226">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="56614-226">Benefit</span></span> | <span data-ttu-id="56614-227">Upphæð framlags</span><span class="sxs-lookup"><span data-stu-id="56614-227">Contribution amount</span></span> |
    | <span data-ttu-id="56614-228">401K</span><span class="sxs-lookup"><span data-stu-id="56614-228">401K</span></span>    | <span data-ttu-id="56614-229">Þátttaka</span><span class="sxs-lookup"><span data-stu-id="56614-229">Participate</span></span>         |
    | <span data-ttu-id="56614-230">Tannlæknistrygging</span><span class="sxs-lookup"><span data-stu-id="56614-230">Dental</span></span>  | <span data-ttu-id="56614-231">SubSp</span><span class="sxs-lookup"><span data-stu-id="56614-231">SubSp</span></span>               |
    | <span data-ttu-id="56614-232">Framtíðarsýn</span><span class="sxs-lookup"><span data-stu-id="56614-232">Vision</span></span>  | <span data-ttu-id="56614-233">SubSp</span><span class="sxs-lookup"><span data-stu-id="56614-233">SubSp</span></span>               |

6. <span data-ttu-id="56614-234">Á flipanum **Skattafrádráttur** slærðu inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="56614-234">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="56614-235">Svæði</span><span class="sxs-lookup"><span data-stu-id="56614-235">Field</span></span>           | <span data-ttu-id="56614-236">Virði</span><span class="sxs-lookup"><span data-stu-id="56614-236">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="56614-237">Skattkóði</span><span class="sxs-lookup"><span data-stu-id="56614-237">Tax code</span></span>        | <span data-ttu-id="56614-238">Upphæð frádráttar</span><span class="sxs-lookup"><span data-stu-id="56614-238">Deduction amount</span></span> |
    | <span data-ttu-id="56614-239">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="56614-239">USA-FED-ER-FICA</span></span> | <span data-ttu-id="56614-240">1600.00</span><span class="sxs-lookup"><span data-stu-id="56614-240">1600.00</span></span>          |
    | <span data-ttu-id="56614-241">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="56614-241">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="56614-242">825.75</span><span class="sxs-lookup"><span data-stu-id="56614-242">825.75</span></span>           |

7. <span data-ttu-id="56614-243">Á flipanum **Skattaframlög** slærðu inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="56614-243">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="56614-244">Smelltu á **Reikna út**.</span><span class="sxs-lookup"><span data-stu-id="56614-244">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="56614-245">Villuleitaðu samtölur launayfirlita þannig að þær passi við tölur það sem af er ári úr eldra kerfi fyrir starfsmanninn.</span><span class="sxs-lookup"><span data-stu-id="56614-245">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="56614-246">Það gæti verið ráðlegt að bíða með að ljúka við næsta skref, til að villuleita öll launayfirlit saman.</span><span class="sxs-lookup"><span data-stu-id="56614-246">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="56614-247">Þegar öll launayfirlit hafa verið villuleituð ferðu í gegnum þau og leggur lokahönd á þau.</span><span class="sxs-lookup"><span data-stu-id="56614-247">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="56614-248">Hægt er að framkvæma sama ferlið uppsafnað ársfjórðungslega ef það er nauðsynlegt fyrir alla fyrri fjórðunga hvert ár.</span><span class="sxs-lookup"><span data-stu-id="56614-248">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="56614-249">Þetta er aðeins nauðsynlegt ef viðskiptavinurinn þarf að skoða gögnin eftir ársfjórðungum án þess að fara aftur í eldra kerfið.</span><span class="sxs-lookup"><span data-stu-id="56614-249">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="56614-250">Ef þú gerir mistök við skráningu upphafsstöðu fyrir starfsmann</span><span class="sxs-lookup"><span data-stu-id="56614-250">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="56614-251">Er mögulegt að bakfæra og endurskrá færslur.</span><span class="sxs-lookup"><span data-stu-id="56614-251">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="56614-252">Til að bakfæra færsluna þarftu bara að ljúka við eftirfarandi skref á síðunni **Öll launayfirlit**.</span><span class="sxs-lookup"><span data-stu-id="56614-252">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="56614-253">Smelltu á **Bakfæra**.</span><span class="sxs-lookup"><span data-stu-id="56614-253">Click **Reverse**.</span></span>
2. <span data-ttu-id="56614-254">Smelltu á **Já** þegar skilaboðin „Þegar þetta launayfirlit er bakfært verður launayfirlit bakfærslu stofnað fyrir mótbókun á þessu launayfirliti.</span><span class="sxs-lookup"><span data-stu-id="56614-254">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="56614-255">Hvorugu launayfirlitinu er hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="56614-255">Neither pay statement can be edited.</span></span> <span data-ttu-id="56614-256">Á að bakfæra þetta launayfirlit?“</span><span class="sxs-lookup"><span data-stu-id="56614-256">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="56614-257">birtast.</span><span class="sxs-lookup"><span data-stu-id="56614-257">displays.</span></span> 

<span data-ttu-id="56614-258">Eftir að launayfirlitið hefur verið bakfært geturðu búið til nýtt launayfirlit fyrir starfsmanninn úr tekjuyfirlitinu sem þú bjóst til áður.</span><span class="sxs-lookup"><span data-stu-id="56614-258">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="56614-259">Gættu þess að lagfæra allar rangar línur á tekjuyfirlitinu áður en þú býrð til nýtt launauppgjör, og búðu svo til ný launayfirlit með réttum upphæðum.</span><span class="sxs-lookup"><span data-stu-id="56614-259">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]