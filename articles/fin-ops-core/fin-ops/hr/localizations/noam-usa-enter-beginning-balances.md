---
title: Innskráning á upphafsstöðu launa
description: Þetta efnisatriði lýsir skrefum fyrir innskráningu á upphafsstöðu fyrir tekjukóða, frádrátt, fríðindi og skatta.
author: andreabichsel
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
ms.openlocfilehash: 9272828fe5d6e0bf131ea66353a0d5c3c7b1c4bd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752151"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="d146e-103">Slá inn upphafsstöður launa</span><span class="sxs-lookup"><span data-stu-id="d146e-103">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d146e-104">Þetta efnisatriði lýsir skrefum fyrir innskráningu á upphafsstöðu fyrir tekjukóða, frádrátt, fríðindi og skatta.</span><span class="sxs-lookup"><span data-stu-id="d146e-104">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="d146e-105">Þessar upplýsingar eru mikilvægar fyrir samstarfsaðila sem flytja gögn fyrir nýja launainnleiðingu úr öðru kerfi.</span><span class="sxs-lookup"><span data-stu-id="d146e-105">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="d146e-106">Til að undirbúa innskráningu launastöðu, staðfestum við eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="d146e-106">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="d146e-107">Starfsmannafærslur eru innskráðar og tiltækar í kerfinu</span><span class="sxs-lookup"><span data-stu-id="d146e-107">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="d146e-108">Eftirfarandi gögn eru sett upp og úthlutuð starfsmönnum:</span><span class="sxs-lookup"><span data-stu-id="d146e-108">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="d146e-109">Greiðsluferli og launatímabil</span><span class="sxs-lookup"><span data-stu-id="d146e-109">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="d146e-110">Tekjukóðar</span><span class="sxs-lookup"><span data-stu-id="d146e-110">Earning codes</span></span>
    - <span data-ttu-id="d146e-111">Skattar</span><span class="sxs-lookup"><span data-stu-id="d146e-111">Taxes</span></span>
    - <span data-ttu-id="d146e-112">Hlunnindi og frádráttur</span><span class="sxs-lookup"><span data-stu-id="d146e-112">Benefits and deductions</span></span>

- <span data-ttu-id="d146e-113">Fyrirtækið ætti að hafa valið dagsetningu sem stilla á upphafsstöðu launa eftir.</span><span class="sxs-lookup"><span data-stu-id="d146e-113">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="d146e-114">Upplýsingum var safnað um allar tekjur, fríðindi/frádrátt, fríðindaframlög, starfsmannaskatt og vinnuveitendaskatt og upphæðir á árinu úr eldra kerfi.</span><span class="sxs-lookup"><span data-stu-id="d146e-114">Information was gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="d146e-115">Þar sem ætlunin er að skrá inn upphafsstöður skal hafa í huga hversu ítarleg gögnin þurfa að vera.</span><span class="sxs-lookup"><span data-stu-id="d146e-115">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="d146e-116">Flest fyrirtæki skrá eina, sameinaða upphæð það sem af er ári.</span><span class="sxs-lookup"><span data-stu-id="d146e-116">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="d146e-117">Hins vegar má skrá uppsafnaðar upphæðir ársfjórðungslega ef þörf er á ítarlegri upplýsingum.</span><span class="sxs-lookup"><span data-stu-id="d146e-117">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="d146e-118">Það hversu ítarlegar upplýsingarnar þurfa að vera sker úr um hversu mörg handvirk launayfirlit þarf að stofna fyrir hvern starfsmann.</span><span class="sxs-lookup"><span data-stu-id="d146e-118">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="d146e-119">Ef um er að ræða eina upphæð fyrir það sem af er ári, þarf aðeins eitt handvirkt yfirlit fyrir hvern starfsmann.</span><span class="sxs-lookup"><span data-stu-id="d146e-119">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="d146e-120">Til að gera þetta skal nota upphæðir það sem af er ári úr endanlegu launayfirliti úr fyrra kerfi sem upphæðina sem er færð inn í nýja launakerfið.</span><span class="sxs-lookup"><span data-stu-id="d146e-120">To do this, use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="d146e-121">Eftirfarandi dæmi sýnir hvernig hægt er að færa upphafsstöðu launa fyrir starfsmanninn, þar á meðal tekjukóða, fríðindi/frádrátt og skatta.</span><span class="sxs-lookup"><span data-stu-id="d146e-121">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="d146e-122">Í raunverulegu dæmi myndir þú hafa línuatriði fyrir hvern tekjukóða, frádrátt fríðinda, fríðindaframlag, skatta starfsmanns og skatta vinnuveitanda með upphæðinni sem skráð er sem upphæð það sem af er ári.</span><span class="sxs-lookup"><span data-stu-id="d146e-122">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="d146e-123">Notaðu þann lista yfir kóða og upphæðir og fylgdu skrefunum fyrir stofnun handvirkra tekju- og launayfirlita með bókhald afvirkjað, til að flytja yfir upphafsstöður fyrir laun.</span><span class="sxs-lookup"><span data-stu-id="d146e-123">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="d146e-124">Bókhald er afvirkjað þar sem þú vilt ekki bóka þessa upphafsstöðu launayfirlits í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="d146e-124">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="d146e-125">Það var gert í eldra kerfinu og kemur yfir í nýja kerfið þegar upphafsstöður eru settar í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="d146e-125">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="d146e-126">A.</span><span class="sxs-lookup"><span data-stu-id="d146e-126">A.</span></span> <span data-ttu-id="d146e-127">Uppsetning tekjukóða sem nota á í upphafsstöðu launa</span><span class="sxs-lookup"><span data-stu-id="d146e-127">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="d146e-128">Þegar upphafsstöður launa eru slegnar inn, gakktu þá úr skugga um að tekjukóðarnir sem þú notar séu skilgreindir með valkostinn „Leyfa breytingar á töxtum í tekjuyfirliti“ virkjaðan.</span><span class="sxs-lookup"><span data-stu-id="d146e-128">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="d146e-129">Það gerir þér kleift að lykla upphæðina handvirkt úr eldra kerfinu.</span><span class="sxs-lookup"><span data-stu-id="d146e-129">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="d146e-130">B.</span><span class="sxs-lookup"><span data-stu-id="d146e-130">B.</span></span> <span data-ttu-id="d146e-131">Stofna tekjuyfirlit svo starfsmaður fái upphafsstöðu</span><span class="sxs-lookup"><span data-stu-id="d146e-131">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="d146e-132">Þetta skref stofnar tekjuyfirlit handvirkt fyrir hvern starfsmann fyrir síðasta launatímabil eldra kerfisins, sem stofnar launayfirlitslínur í nýja launakerfinu.</span><span class="sxs-lookup"><span data-stu-id="d146e-132">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="d146e-133">Færðu inn eina línu fyrir hvern tekjukóða og upphæðir og tíma fyrir það sem af er ári.</span><span class="sxs-lookup"><span data-stu-id="d146e-133">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="d146e-134">Sýnisskrefin eru sem hér segir:</span><span class="sxs-lookup"><span data-stu-id="d146e-134">The sample steps are as follows:</span></span>

1. <span data-ttu-id="d146e-135">Opnaðu síðuna **Öll tekjuyfirlit** og smelltu á **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d146e-135">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="d146e-136">Færa inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="d146e-136">Enter the following:</span></span> 

    | <span data-ttu-id="d146e-137">Svæði</span><span class="sxs-lookup"><span data-stu-id="d146e-137">Field</span></span>      | <span data-ttu-id="d146e-138">Virði</span><span class="sxs-lookup"><span data-stu-id="d146e-138">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="d146e-139">Starfskraftur</span><span class="sxs-lookup"><span data-stu-id="d146e-139">Worker</span></span>     | <span data-ttu-id="d146e-140">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="d146e-140">Michael Redmond</span></span>       |
    | <span data-ttu-id="d146e-141">Greiðsluferli</span><span class="sxs-lookup"><span data-stu-id="d146e-141">Pay cycle</span></span>  | <span data-ttu-id="d146e-142">sm</span><span class="sxs-lookup"><span data-stu-id="d146e-142">sm</span></span>                    |
    | <span data-ttu-id="d146e-143">Launatímabil</span><span class="sxs-lookup"><span data-stu-id="d146e-143">Pay period</span></span> | <span data-ttu-id="d146e-144">6/16/2017 - 6/30/2017</span><span class="sxs-lookup"><span data-stu-id="d146e-144">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="d146e-145">Á flipanum **Tekjuyfirlitslínur** færirðu inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="d146e-145">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="d146e-146">Lína 1: Flipinn **Tekjuyfirlitslína**</span><span class="sxs-lookup"><span data-stu-id="d146e-146">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="d146e-147">Svæði</span><span class="sxs-lookup"><span data-stu-id="d146e-147">Field</span></span>            | <span data-ttu-id="d146e-148">Virði</span><span class="sxs-lookup"><span data-stu-id="d146e-148">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="d146e-149">Tekjukóði</span><span class="sxs-lookup"><span data-stu-id="d146e-149">Earnings code</span></span>    | <span data-ttu-id="d146e-150">Regluleg laun</span><span class="sxs-lookup"><span data-stu-id="d146e-150">Regular pay</span></span> |
    | <span data-ttu-id="d146e-151">Magn</span><span class="sxs-lookup"><span data-stu-id="d146e-151">Quantity</span></span>         | <span data-ttu-id="d146e-152">1.00</span><span class="sxs-lookup"><span data-stu-id="d146e-152">1.00</span></span>        |
    | <span data-ttu-id="d146e-153">Taxti</span><span class="sxs-lookup"><span data-stu-id="d146e-153">Rate</span></span>             | <span data-ttu-id="d146e-154">30,000</span><span class="sxs-lookup"><span data-stu-id="d146e-154">30,000</span></span>      |
    | <span data-ttu-id="d146e-155">Flipi fyrir línuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="d146e-155">Line details tab</span></span> |             |
    | <span data-ttu-id="d146e-156">Handbók</span><span class="sxs-lookup"><span data-stu-id="d146e-156">Manual</span></span>           | <span data-ttu-id="d146e-157">(merkt)</span><span class="sxs-lookup"><span data-stu-id="d146e-157">(marked)</span></span>    |

    <span data-ttu-id="d146e-158">Lína 2: Flipinn **Tekjuyfirlitslína**</span><span class="sxs-lookup"><span data-stu-id="d146e-158">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="d146e-159">Svæði</span><span class="sxs-lookup"><span data-stu-id="d146e-159">Field</span></span>            | <span data-ttu-id="d146e-160">Virði</span><span class="sxs-lookup"><span data-stu-id="d146e-160">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="d146e-161">Tekjukóði</span><span class="sxs-lookup"><span data-stu-id="d146e-161">Earnings code</span></span>    | <span data-ttu-id="d146e-162">Kaupauki</span><span class="sxs-lookup"><span data-stu-id="d146e-162">Bonus</span></span>    |
    | <span data-ttu-id="d146e-163">Magn</span><span class="sxs-lookup"><span data-stu-id="d146e-163">Quantity</span></span>         | <span data-ttu-id="d146e-164">1.0000</span><span class="sxs-lookup"><span data-stu-id="d146e-164">1.0000</span></span>   |
    | <span data-ttu-id="d146e-165">Taxti</span><span class="sxs-lookup"><span data-stu-id="d146e-165">Rate</span></span>             | <span data-ttu-id="d146e-166">4250.00</span><span class="sxs-lookup"><span data-stu-id="d146e-166">4250.00</span></span>  |
    | <span data-ttu-id="d146e-167">Flipi fyrir línuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="d146e-167">Line details tab</span></span> |          |
    | <span data-ttu-id="d146e-168">Handvirkt</span><span class="sxs-lookup"><span data-stu-id="d146e-168">Manual</span></span>           | <span data-ttu-id="d146e-169">(merkt)</span><span class="sxs-lookup"><span data-stu-id="d146e-169">(marked)</span></span> |

    <span data-ttu-id="d146e-170">Lína 3: Flipinn **Tekjuyfirlitslína**</span><span class="sxs-lookup"><span data-stu-id="d146e-170">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="d146e-171">Svæði</span><span class="sxs-lookup"><span data-stu-id="d146e-171">Field</span></span>           | <span data-ttu-id="d146e-172">Virði</span><span class="sxs-lookup"><span data-stu-id="d146e-172">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="d146e-173">Tekjukóði</span><span class="sxs-lookup"><span data-stu-id="d146e-173">Earnings code</span></span>   | <span data-ttu-id="d146e-174">Þóknun</span><span class="sxs-lookup"><span data-stu-id="d146e-174">Commission</span></span> |
    | <span data-ttu-id="d146e-175">Magn</span><span class="sxs-lookup"><span data-stu-id="d146e-175">Quantity</span></span>        | <span data-ttu-id="d146e-176">1.0000</span><span class="sxs-lookup"><span data-stu-id="d146e-176">1.0000</span></span>     |
    | <span data-ttu-id="d146e-177">Taxti</span><span class="sxs-lookup"><span data-stu-id="d146e-177">Rate</span></span>            | <span data-ttu-id="d146e-178">!,299.00</span><span class="sxs-lookup"><span data-stu-id="d146e-178">!,299.00</span></span>   |
    | <span data-ttu-id="d146e-179">Taxti</span><span class="sxs-lookup"><span data-stu-id="d146e-179">Rate</span></span>            | <span data-ttu-id="d146e-180">1,299.00</span><span class="sxs-lookup"><span data-stu-id="d146e-180">1,299.00</span></span>   |
    | <span data-ttu-id="d146e-181">Flipi fyrir línuupplýsingar</span><span class="sxs-lookup"><span data-stu-id="d146e-181">Line detail tab</span></span> |            |
    | <span data-ttu-id="d146e-182">Handvirkt</span><span class="sxs-lookup"><span data-stu-id="d146e-182">Manual</span></span>          | <span data-ttu-id="d146e-183">(merkt)</span><span class="sxs-lookup"><span data-stu-id="d146e-183">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="d146e-184">Það að stilla sleðann **Handvirkt** á **Já** á flipanum **Línuupplýsingar** fyrir hverja tekjuyfirlitslínu er lykillinn að því að láta skrá inn upphafsstöðu launa fyrir hvern starfsmann.</span><span class="sxs-lookup"><span data-stu-id="d146e-184">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="d146e-185">Á rúðunni **Aðgerð** smellirðu á **Birta tekjuyfirlit** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="d146e-185">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="d146e-186">Á rúðunni **Aðgerð** smellirðu á **Launayfirlit** til að opna síðuna **Búa til launayfirlit** og stillir eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="d146e-186">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="d146e-187">Svæði</span><span class="sxs-lookup"><span data-stu-id="d146e-187">Field</span></span>              | <span data-ttu-id="d146e-188">Virði</span><span class="sxs-lookup"><span data-stu-id="d146e-188">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="d146e-189">Dagsetning greiðslu</span><span class="sxs-lookup"><span data-stu-id="d146e-189">Payment date</span></span>       | <span data-ttu-id="d146e-190">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="d146e-190">6/30/2017</span></span> |
    | <span data-ttu-id="d146e-191">Keyrslugerð greiðslu</span><span class="sxs-lookup"><span data-stu-id="d146e-191">Payment run type</span></span>   | <span data-ttu-id="d146e-192">Handvirkt</span><span class="sxs-lookup"><span data-stu-id="d146e-192">Manual</span></span>    |
    | <span data-ttu-id="d146e-193">Gera bókhald óvirkt</span><span class="sxs-lookup"><span data-stu-id="d146e-193">Disable accounting</span></span> |   <span data-ttu-id="d146e-194">Já</span><span class="sxs-lookup"><span data-stu-id="d146e-194">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="d146e-195">Þetta er aðeins í boði þegar keyrslugerð launa er handvirk og þar sem notandinn vill afvirkja bókhald í launakeyrslu.</span><span class="sxs-lookup"><span data-stu-id="d146e-195">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="d146e-196">Smelltu á **Í lagi** og lokaðu **Athugasemdum**.</span><span class="sxs-lookup"><span data-stu-id="d146e-196">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="d146e-197">Af hverju þarf að setja sleðann Gera bókhald óvirkt á Já þegar launayfirlit eru búin til?</span><span class="sxs-lookup"><span data-stu-id="d146e-197">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="d146e-198">Ef sleðinn er stilltur á **Já** kemur hann í veg fyrir að línum í launayfirliti sé dreift í fjárhag.</span><span class="sxs-lookup"><span data-stu-id="d146e-198">Setting the slider to **Yes** prevents lines in the pay statement from being distributed to General ledger.</span></span> <span data-ttu-id="d146e-199">Fjárhagsupphæðir voru í uppfærslu áður þegar lykilstöður úr eldra kerfinu voru færðar inn.</span><span class="sxs-lookup"><span data-stu-id="d146e-199">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="d146e-200">Ef færðar eru inn upphafsstöður fyrir Laun er hægt að búa til skýrslur sem innihalda upplýsingar frá fyrri árum, sem og að auðkenna mörk fyrir fríðindi og skatta.</span><span class="sxs-lookup"><span data-stu-id="d146e-200">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="d146e-201">C.</span><span class="sxs-lookup"><span data-stu-id="d146e-201">C.</span></span> <span data-ttu-id="d146e-202">Stofna launayfirlit fyrir starfsmenn</span><span class="sxs-lookup"><span data-stu-id="d146e-202">Create pay statements for employees</span></span>

<span data-ttu-id="d146e-203">Eftir að þú hefur búið til launayfirlit sem hafa upphafsstöður verður þú að sannreyna að launayfirlit endurspegli launagögn réttilega.</span><span class="sxs-lookup"><span data-stu-id="d146e-203">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="d146e-204">Þú verður einnig að uppfæra upplýsingar um fríðindi og skatta handvirkt þannig að þær passi við gildin í fyrra launakerfi.</span><span class="sxs-lookup"><span data-stu-id="d146e-204">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="d146e-205">Þegar búið er að sannreyna að upphæðir úr fyrra launakerfi séu þær sömu og á núverandi launayfirlitum, verður þú að leggja lokahönd á launayfirlitin.</span><span class="sxs-lookup"><span data-stu-id="d146e-205">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="d146e-206">Opnaðu síðuna **Öll launayfirlit**.</span><span class="sxs-lookup"><span data-stu-id="d146e-206">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="d146e-207">Merktu síðasta launayfirlit fyrir Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="d146e-207">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="d146e-208">Smelltu á **Breyta** til að opna síðuna **Launayfirlit**.</span><span class="sxs-lookup"><span data-stu-id="d146e-208">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="d146e-209">Opnaðu flipann **Frádráttur fríðinda** og sláðu inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="d146e-209">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="d146e-210">Svæði</span><span class="sxs-lookup"><span data-stu-id="d146e-210">Field</span></span>             | <span data-ttu-id="d146e-211">Virði</span><span class="sxs-lookup"><span data-stu-id="d146e-211">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="d146e-212">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="d146e-212">Benefit</span></span>           | <span data-ttu-id="d146e-213">Upphæð frádráttar</span><span class="sxs-lookup"><span data-stu-id="d146e-213">Deduction amount</span></span> |
    | <span data-ttu-id="d146e-214">401K</span><span class="sxs-lookup"><span data-stu-id="d146e-214">401K</span></span>              | <span data-ttu-id="d146e-215">Þátttaka</span><span class="sxs-lookup"><span data-stu-id="d146e-215">Participate</span></span>      |
    | <span data-ttu-id="d146e-216">Tannlæknistrygging</span><span class="sxs-lookup"><span data-stu-id="d146e-216">Dental</span></span>            | <span data-ttu-id="d146e-217">SubSp</span><span class="sxs-lookup"><span data-stu-id="d146e-217">SubSp</span></span>            |
    | <span data-ttu-id="d146e-218">Kostnaður við tryggingar skjólstæðinga</span><span class="sxs-lookup"><span data-stu-id="d146e-218">Dep care spending</span></span> | <span data-ttu-id="d146e-219">Þátttaka</span><span class="sxs-lookup"><span data-stu-id="d146e-219">Participate</span></span>      |
    | <span data-ttu-id="d146e-220">Framtíðarsýn</span><span class="sxs-lookup"><span data-stu-id="d146e-220">Vision</span></span>            | <span data-ttu-id="d146e-221">SupSp</span><span class="sxs-lookup"><span data-stu-id="d146e-221">SupSp</span></span>            |

5. <span data-ttu-id="d146e-222">Á flipanum **Fríðindaframlög** slærðu inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="d146e-222">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="d146e-223">Svæði</span><span class="sxs-lookup"><span data-stu-id="d146e-223">Field</span></span>   | <span data-ttu-id="d146e-224">Virði</span><span class="sxs-lookup"><span data-stu-id="d146e-224">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="d146e-225">Fríðindi</span><span class="sxs-lookup"><span data-stu-id="d146e-225">Benefit</span></span> | <span data-ttu-id="d146e-226">Upphæð framlags</span><span class="sxs-lookup"><span data-stu-id="d146e-226">Contribution amount</span></span> |
    | <span data-ttu-id="d146e-227">401K</span><span class="sxs-lookup"><span data-stu-id="d146e-227">401K</span></span>    | <span data-ttu-id="d146e-228">Þátttaka</span><span class="sxs-lookup"><span data-stu-id="d146e-228">Participate</span></span>         |
    | <span data-ttu-id="d146e-229">Tannlæknistrygging</span><span class="sxs-lookup"><span data-stu-id="d146e-229">Dental</span></span>  | <span data-ttu-id="d146e-230">SubSp</span><span class="sxs-lookup"><span data-stu-id="d146e-230">SubSp</span></span>               |
    | <span data-ttu-id="d146e-231">Framtíðarsýn</span><span class="sxs-lookup"><span data-stu-id="d146e-231">Vision</span></span>  | <span data-ttu-id="d146e-232">SubSp</span><span class="sxs-lookup"><span data-stu-id="d146e-232">SubSp</span></span>               |

6. <span data-ttu-id="d146e-233">Á flipanum **Skattafrádráttur** slærðu inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="d146e-233">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="d146e-234">Svæði</span><span class="sxs-lookup"><span data-stu-id="d146e-234">Field</span></span>           | <span data-ttu-id="d146e-235">Virði</span><span class="sxs-lookup"><span data-stu-id="d146e-235">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="d146e-236">Skattkóði</span><span class="sxs-lookup"><span data-stu-id="d146e-236">Tax code</span></span>        | <span data-ttu-id="d146e-237">Upphæð frádráttar</span><span class="sxs-lookup"><span data-stu-id="d146e-237">Deduction amount</span></span> |
    | <span data-ttu-id="d146e-238">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="d146e-238">USA-FED-ER-FICA</span></span> | <span data-ttu-id="d146e-239">1600.00</span><span class="sxs-lookup"><span data-stu-id="d146e-239">1600.00</span></span>          |
    | <span data-ttu-id="d146e-240">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="d146e-240">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="d146e-241">825.75</span><span class="sxs-lookup"><span data-stu-id="d146e-241">825.75</span></span>           |

7. <span data-ttu-id="d146e-242">Á flipanum **Skattaframlög** slærðu inn eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="d146e-242">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="d146e-243">Smelltu á **Reikna út**.</span><span class="sxs-lookup"><span data-stu-id="d146e-243">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="d146e-244">Villuleitaðu samtölur launayfirlita þannig að þær passi við tölur það sem af er ári úr eldra kerfi fyrir starfsmanninn.</span><span class="sxs-lookup"><span data-stu-id="d146e-244">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="d146e-245">Það gæti verið ráðlegt að bíða með að ljúka við næsta skref, til að villuleita öll launayfirlit saman.</span><span class="sxs-lookup"><span data-stu-id="d146e-245">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="d146e-246">Þegar öll launayfirlit hafa verið villuleituð ferðu í gegnum þau og leggur lokahönd á þau.</span><span class="sxs-lookup"><span data-stu-id="d146e-246">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="d146e-247">Hægt er að framkvæma sama ferlið uppsafnað ársfjórðungslega ef það er nauðsynlegt fyrir alla fyrri fjórðunga hvert ár.</span><span class="sxs-lookup"><span data-stu-id="d146e-247">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="d146e-248">Þetta er aðeins nauðsynlegt ef viðskiptavinurinn þarf að skoða gögnin eftir ársfjórðungum án þess að fara aftur í eldra kerfið.</span><span class="sxs-lookup"><span data-stu-id="d146e-248">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="d146e-249">Ef þú gerir mistök við skráningu upphafsstöðu fyrir starfsmann</span><span class="sxs-lookup"><span data-stu-id="d146e-249">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="d146e-250">Er mögulegt að bakfæra og endurskrá færslur.</span><span class="sxs-lookup"><span data-stu-id="d146e-250">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="d146e-251">Til að bakfæra færsluna þarftu bara að ljúka við eftirfarandi skref á síðunni **Öll launayfirlit**.</span><span class="sxs-lookup"><span data-stu-id="d146e-251">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="d146e-252">Smelltu á **Bakfæra**.</span><span class="sxs-lookup"><span data-stu-id="d146e-252">Click **Reverse**.</span></span>
2. <span data-ttu-id="d146e-253">Smelltu á **Já** þegar skilaboðin „Þegar þetta launayfirlit er bakfært verður launayfirlit bakfærslu stofnað fyrir mótbókun á þessu launayfirliti.</span><span class="sxs-lookup"><span data-stu-id="d146e-253">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="d146e-254">Hvorugu launayfirlitinu er hægt að breyta.</span><span class="sxs-lookup"><span data-stu-id="d146e-254">Neither pay statement can be edited.</span></span> <span data-ttu-id="d146e-255">Á að bakfæra þetta launayfirlit?“</span><span class="sxs-lookup"><span data-stu-id="d146e-255">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="d146e-256">birtast.</span><span class="sxs-lookup"><span data-stu-id="d146e-256">displays.</span></span> 

<span data-ttu-id="d146e-257">Eftir að launayfirlitið hefur verið bakfært geturðu búið til nýtt launayfirlit fyrir starfsmanninn úr tekjuyfirlitinu sem þú bjóst til áður.</span><span class="sxs-lookup"><span data-stu-id="d146e-257">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="d146e-258">Gættu þess að lagfæra allar rangar línur á tekjuyfirlitinu áður en þú býrð til nýtt launauppgjör, og búðu svo til ný launayfirlit með réttum upphæðum.</span><span class="sxs-lookup"><span data-stu-id="d146e-258">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]