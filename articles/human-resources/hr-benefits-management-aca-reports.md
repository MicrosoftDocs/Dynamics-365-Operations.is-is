---
title: Búa til tilkynningar um Affordable Care Act í fríðindastjórnun
description: Þetta efnisatriði lýsir því hvernig fríðindastjórnun hjálpar til við að rekja upplýsingar sem er greint frá á eyðublaði 1095-B og eyðublaði 1095-C fyrir vinnuveitandaumboð Affordable Care Act (ACA).
author: andreabichsel
manager: tfehr
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 24df18f428e4ca14859bc34048a6bda5e03d1b2f
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464375"
---
# <a name="generate-aca-reports-in-benefits-management"></a><span data-ttu-id="60eed-103">Búa til ACA-tilkynningar í fríðindastjórnun</span><span class="sxs-lookup"><span data-stu-id="60eed-103">Generate ACA reports in Benefits management</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="60eed-104">Fríðindastjórnun hjálpar til við að rekja upplýsingar sem er greint frá á eyðublaði 1095-B og eyðublaði 1095-C fyrir vinnuveitandaumboð Affordable Care Act (ACA).</span><span class="sxs-lookup"><span data-stu-id="60eed-104">Benefits management helps you track information that is reported on Form 1095-B and Form 1095-C for the Affordable Care Act (ACA) employer mandate.</span></span> <span data-ttu-id="60eed-105">Rétt eins og möguleiki ACA-skýrslugerðar í gamla vinnusvæðinu **Fríðindi**, á þessi virkni aðeins við um lögaðila í Bandaríkjunum.</span><span class="sxs-lookup"><span data-stu-id="60eed-105">Like the ACA reporting capability in the old **Benefits** workspace, this functionality applies only to legal entities in the United States.</span></span>

<span data-ttu-id="60eed-106">Til að nota þessa virkni þarf fyrst að kveikja á **Ítarleg fríðindastjórnun**.</span><span class="sxs-lookup"><span data-stu-id="60eed-106">To use this functionality, you must first turn on **Advanced Benefits Management**.</span></span> <span data-ttu-id="60eed-107">Frekari upplýsingar, þar á meðal mikilvæg skilyrði fríðindastjórnunar, er að finna í [Virkja eða óvirkja fríðindastjórnun](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span><span class="sxs-lookup"><span data-stu-id="60eed-107">For more information, including important caveats about Benefits management, see [Enable or disable Benefits management](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="60eed-108">Aðeins er hægt að nota ACA-tilkynningu frá annaðhvort vinnusvæðinu **Fríðindastjórnun** eða gamla vinnusvæðinu **Fríðindi**, en ekki báðum.</span><span class="sxs-lookup"><span data-stu-id="60eed-108">You can use ACA reporting only from either the **Benefits management** workspace or the old **Benefits** workspace, not from both.</span></span> <span data-ttu-id="60eed-109">Til dæmis ef skipt er yfir í fríðindastjórnun er ACA-tilkynning aðeins í boði á vinnusvæðinu **Fríðindastjórnun**, en ekki gamla vinnusvæðinu **Fríðindi**.</span><span class="sxs-lookup"><span data-stu-id="60eed-109">For example, if you switched to Benefits management, ACA reporting is available only from the **Benefits management** workspace, not from the old **Benefits** workspace.</span></span>
>
> <span data-ttu-id="60eed-110">Ef skipt er í fríðindastjórnun á miðju skráningarári verður að skilgreina á réttan hátt starfsmannagögn fyrir allt árið í fríðindastjórnun.</span><span class="sxs-lookup"><span data-stu-id="60eed-110">If you switch to Benefits management in the middle of an enrollment year, you must correctly configure employee data for the whole year in Benefits management.</span></span> <span data-ttu-id="60eed-111">Þannig er gengið úr skugga um að nákvæmar upplýsingar tilkynningar komi fram fyrir allt árið.</span><span class="sxs-lookup"><span data-stu-id="60eed-111">In this way, you ensure that you will receive accurate reporting information for the whole year.</span></span>

## <a name="getting-started"></a><span data-ttu-id="60eed-112">Hafist handa</span><span class="sxs-lookup"><span data-stu-id="60eed-112">Getting started</span></span>

<span data-ttu-id="60eed-113">Til að rekja upplýsingar fyrir 1095-eyðublöð skal fyrst stofna einn eða fleiri Affordable Care-tryggingaflokka.</span><span class="sxs-lookup"><span data-stu-id="60eed-113">To track information for 1095 forms, first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="60eed-114">Þessir flokkar sýna eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="60eed-114">These groups indicate the following information:</span></span>

- <span data-ttu-id="60eed-115">Tryggingatilboð sem starfsmanni var útvegað</span><span class="sxs-lookup"><span data-stu-id="60eed-115">The offer of coverage that was provided to an employee</span></span>
- <span data-ttu-id="60eed-116">Hlutdeild starfsmanns í lægstu mánaðarlegu greiðslu iðgjalds, ef kostnaðurinn er fyrir ofan fátæktarmörk</span><span class="sxs-lookup"><span data-stu-id="60eed-116">The employee's share of the lowest-cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="60eed-117">Örugga höfnin sem er notuð af starfsmanni, ef á við</span><span class="sxs-lookup"><span data-stu-id="60eed-117">The safe harbor that is used by the employer, if applicable</span></span>

<span data-ttu-id="60eed-118">Affordable Care-tryggingaflokkar auðvelda þér að stjórna þessum upplýsingum fyrir margar starfsmannsfærslur sem eru með sömu skilyrðin.</span><span class="sxs-lookup"><span data-stu-id="60eed-118">Affordable Care coverage groups help you manage this information for multiple employee records that have the same conditions.</span></span> <span data-ttu-id="60eed-119">Auðveldlega er hægt að úthluta flokkum á einn eða fleiri starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="60eed-119">You can easily assign groups to one or more employees.</span></span>

### <a name="create-or-edit-an-affordable-care-coverage-group"></a><span data-ttu-id="60eed-120">Búa til eða breyta Affordable Care-tryggingaflokk</span><span class="sxs-lookup"><span data-stu-id="60eed-120">Create or edit an Affordable Care coverage group</span></span>

1. <span data-ttu-id="60eed-121">Á vinnusvæðinu **Fríðindastjórnun** skal velja **Affordable Care-tryggingaflokk**.</span><span class="sxs-lookup"><span data-stu-id="60eed-121">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>

    ![Val á Affordable Care-tryggingaflokk](./media/hr-benefits-management-aca-coverage-group.png)

2. <span data-ttu-id="60eed-123">Velja skal **Nýr** til að stofna nýjan Affordable Care-tryggingaflokk eða **Breyta** til að breyta fyrirliggjandi flokki.</span><span class="sxs-lookup"><span data-stu-id="60eed-123">Select **New** to create a new Affordable Care coverage group or **Edit** to change an existing group.</span></span>

    ![Að velja nýjan eða breyta](./media/hr-benefits-management-aca-new.png)

3. <span data-ttu-id="60eed-125">Stilltu eftirfarandi reiti.</span><span class="sxs-lookup"><span data-stu-id="60eed-125">Set the following fields.</span></span>

    | <span data-ttu-id="60eed-126">Svæði</span><span class="sxs-lookup"><span data-stu-id="60eed-126">Field</span></span> | <span data-ttu-id="60eed-127">lýsing</span><span class="sxs-lookup"><span data-stu-id="60eed-127">Description</span></span> |
    |---|---|
    | <span data-ttu-id="60eed-128">Nafn</span><span class="sxs-lookup"><span data-stu-id="60eed-128">Name</span></span> | <span data-ttu-id="60eed-129">Færa inn heiti fyrir hópinn.</span><span class="sxs-lookup"><span data-stu-id="60eed-129">Enter a name for the group.</span></span> |
    | <span data-ttu-id="60eed-130">lýsing</span><span class="sxs-lookup"><span data-stu-id="60eed-130">Description</span></span> | <span data-ttu-id="60eed-131">Færa inn lýsingu á flokknum.</span><span class="sxs-lookup"><span data-stu-id="60eed-131">Enter a description of the group.</span></span> |
    | <span data-ttu-id="60eed-132">Tryggingatilboð</span><span class="sxs-lookup"><span data-stu-id="60eed-132">Offer of coverage</span></span> | <span data-ttu-id="60eed-133">Tryggingin sem boðin er starfsmanni, maka og skjólstæðinga.</span><span class="sxs-lookup"><span data-stu-id="60eed-133">The coverage that is offered to employees, their spouse or partner, and their dependents.</span></span> |
    | <span data-ttu-id="60eed-134">Kostnaðarhlutdeild starfsmanns</span><span class="sxs-lookup"><span data-stu-id="60eed-134">Employee share of cost</span></span> | <span data-ttu-id="60eed-135">Upphæðin sem starfsmaður ber ábyrgð á.</span><span class="sxs-lookup"><span data-stu-id="60eed-135">The amount that the employee is responsible for.</span></span> |
    | <span data-ttu-id="60eed-136">Viðeigandi hluti 4980H um örugga höfn</span><span class="sxs-lookup"><span data-stu-id="60eed-136">Applicable section 4980H safe harbor</span></span> | <span data-ttu-id="60eed-137">4980H fyrir örugga höfn eða afléttingarkóði umbreytingar.</span><span class="sxs-lookup"><span data-stu-id="60eed-137">The 4980H safe harbor or transition relief code.</span></span> |
    | <span data-ttu-id="60eed-138">Upphafsmánuður áætlunar</span><span class="sxs-lookup"><span data-stu-id="60eed-138">Plan start month</span></span> | <span data-ttu-id="60eed-139">Veljið almanaksmánuðinn þegar ár fríðindaáætlunar hefst.</span><span class="sxs-lookup"><span data-stu-id="60eed-139">Select the calendar month when your benefit plan year begins.</span></span> |
    | <span data-ttu-id="60eed-140">Flokkur gildir frá</span><span class="sxs-lookup"><span data-stu-id="60eed-140">Group valid from</span></span> | <span data-ttu-id="60eed-141">Fyrsta gilda dagsetning þessarar færslu.</span><span class="sxs-lookup"><span data-stu-id="60eed-141">The first date when this record is valid.</span></span> |
    | <span data-ttu-id="60eed-142">Flokkur gildir</span><span class="sxs-lookup"><span data-stu-id="60eed-142">Group valid through</span></span> | <span data-ttu-id="60eed-143">Síðasta gilda dagsetning þessarar færslu.</span><span class="sxs-lookup"><span data-stu-id="60eed-143">The last date when this record is valid.</span></span> <span data-ttu-id="60eed-144">Ef engin lokadagsetning er til staðar skal slá inn **Aldrei**.</span><span class="sxs-lookup"><span data-stu-id="60eed-144">If there is no expiration date, enter **Never**.</span></span> |

    ![Stofnun þekjuflokks](./media/hr-benefits-management-aca-new-group.png)

4. <span data-ttu-id="60eed-146">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="60eed-146">Select **Save**.</span></span>

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a><span data-ttu-id="60eed-147">Úthluta mörgum starfsmönnum á Affordable Care-tryggingaflokk</span><span class="sxs-lookup"><span data-stu-id="60eed-147">Assign multiple employees to an Affordable Care coverage group</span></span>

1. <span data-ttu-id="60eed-148">Á vinnusvæðinu **Fríðindastjórnun** skal velja **Affordable Care-tryggingaflokk**.</span><span class="sxs-lookup"><span data-stu-id="60eed-148">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>
2. <span data-ttu-id="60eed-149">Veljið flokkinn sem úthluta á starfsmönnum í.</span><span class="sxs-lookup"><span data-stu-id="60eed-149">Select the group to assign employees to.</span></span>
3. <span data-ttu-id="60eed-150">Veljið **Fjöldaúthlutun**.</span><span class="sxs-lookup"><span data-stu-id="60eed-150">Select **Mass assignment**.</span></span>

    ![Fjöldaúthlutun valin](./media/hr-benefits-management-aca-mass-assignment.png)

4. <span data-ttu-id="60eed-152">Veljið starfsmenn af listanum og veljið síðan **Úthluta**.</span><span class="sxs-lookup"><span data-stu-id="60eed-152">Select employees in the list, and then select **Assign**.</span></span>

    ![Völdum starfsmönnum úthlutað í flokkinn](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a><span data-ttu-id="60eed-154">Vinna með margar útgáfur af tryggingarmöguleikum</span><span class="sxs-lookup"><span data-stu-id="60eed-154">Maintain multiple versions of coverage options</span></span>

<span data-ttu-id="60eed-155">Hægt er að viðhalda mörgum útgáfum í hvaða tryggingaflokki sem er.</span><span class="sxs-lookup"><span data-stu-id="60eed-155">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="60eed-156">Þegar eitthvað breytist í fyrirtækinu eða fríðindin sem boðið er upp á er hægt að halda upplýsingum um flokkinn uppfærðum án þess að þurfa að stofna nýjan flokk og endurúthluta starfsmönnum í hann.</span><span class="sxs-lookup"><span data-stu-id="60eed-156">When something changes in your organization or the benefits that are offered, you can keep the group's information up to date without having to create a new group and reassign employees to it.</span></span>

<span data-ttu-id="60eed-157">Þegar búið er að stofna Affordable Care-tryggingaflokka er hægt að úthluta mörgum starfsmönnum í hann í einu.</span><span class="sxs-lookup"><span data-stu-id="60eed-157">After you've created Affordable Care coverage groups, you can mass-assign employees to them.</span></span> <span data-ttu-id="60eed-158">Einnig er hægt að úthluta einum starfsmanni í einu í flokkana og gefa upp hvort ACA-upplýsingar eru raktar og tilkynntar.</span><span class="sxs-lookup"><span data-stu-id="60eed-158">You can also individually assign employees to groups, and indicate whether ACA information is tracked and reported.</span></span>

<span data-ttu-id="60eed-159">Ef ekki þarf að rekja og tilkynna ACA-upplýsingar fyrir starfsmann, er hægt að stilla valkostinn **Tilkynna tryggingu** á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="60eed-159">If you don't have to track and report ACA information for an employee, you can set the **Report coverage** option to **No**.</span></span> <span data-ttu-id="60eed-160">Til dæmis gætu verið starfsmenn í hlutastarfi sem þurfa ekki ACA-tilkynningu.</span><span class="sxs-lookup"><span data-stu-id="60eed-160">For example, you might have part-time employees who don't require ACA reporting.</span></span>

### <a name="override-default-values-for-an-employee"></a><span data-ttu-id="60eed-161">Hnekkja sjálfgefnum gildum fyrir starfsmann</span><span class="sxs-lookup"><span data-stu-id="60eed-161">Override default values for an employee</span></span>

<span data-ttu-id="60eed-162">Fyrir starfsmenn sem er úthlutað í Affordable Care-tryggingaflokk er hægt að breyta eftirfarandi valkostum fyrir hvaða mánuð sem er sem þarf önnur gildi:</span><span class="sxs-lookup"><span data-stu-id="60eed-162">For employees who are assigned to an Affordable Care coverage group, you can change the following options for any months that require different values:</span></span>

- <span data-ttu-id="60eed-163">Tryggingatilboð</span><span class="sxs-lookup"><span data-stu-id="60eed-163">Offer of coverage</span></span>
- <span data-ttu-id="60eed-164">Kostnaðarhlutdeild starfsmanns</span><span class="sxs-lookup"><span data-stu-id="60eed-164">Employee share of cost</span></span>
- <span data-ttu-id="60eed-165">Viðeigandi hluti 4980H um örugga höfn</span><span class="sxs-lookup"><span data-stu-id="60eed-165">Applicable section 4980H safe harbor</span></span>

> [!NOTE]
> <span data-ttu-id="60eed-166">Fyrir ACA-tilkynningar 2020 þarf að tilkynna bæði póstnúmer vinnustaðar og heimilis á eyðublað 1095-C.</span><span class="sxs-lookup"><span data-stu-id="60eed-166">For 2020 ACA reports, you must report both work and home ZIP Codes on Form 1095-C.</span></span> <span data-ttu-id="60eed-167">Gildin eru sjálfkrafa fyllt út í samræmi við núgildandi virkar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="60eed-167">Values are automatically filled in, based on current active locations.</span></span> <span data-ttu-id="60eed-168">Ef önnur hvor staðsetningin var önnur einhvern hluta ársins þarf að hnekkja gildinu.</span><span class="sxs-lookup"><span data-stu-id="60eed-168">If either location was different during any part of the year, you must override the value.</span></span> <span data-ttu-id="60eed-169">Aðeins er fyllt út í reitinn **Póstnúmer** (lína 17) á tilkynningu 1095-C ef kóðinn **Tryggingatilboð** inniheldur **1L** til **1Q** eins og eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="60eed-169">The **ZIP Code** field (line 17) of the 1095-C report is filled in only if the **Offer of coverage** code contains **1L** through **1Q**, as follows:</span></span>
>
> - <span data-ttu-id="60eed-170">**1L, 1M eða 1N:** Póstnúmer aðalaðseturs</span><span class="sxs-lookup"><span data-stu-id="60eed-170">**1L, 1M, or 1N:** The primary residence ZIP Code</span></span>
> - <span data-ttu-id="60eed-171">**1O, 1P, 1Q:** Póstnúmer aðalvinnustaðar</span><span class="sxs-lookup"><span data-stu-id="60eed-171">**1O, 1P, 1Q:** The primary work ZIP Code</span></span>

<span data-ttu-id="60eed-172">Til að færa inn undantekningar fyrir gildi Affordable Care-tryggingaflokks skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="60eed-172">To enter exceptions for any values of an Affordable Care coverage group, follow these steps.</span></span>

1. <span data-ttu-id="60eed-173">Á vinnusvæðinu **Starfsmannastjórnun** skal velja **Tenglar** og síðan velja **Starfsmenn**.</span><span class="sxs-lookup"><span data-stu-id="60eed-173">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>
2. <span data-ttu-id="60eed-174">Veljið starfsmanninn í listanum.</span><span class="sxs-lookup"><span data-stu-id="60eed-174">Select the employee in the list.</span></span>
3. <span data-ttu-id="60eed-175">Í flipanum **Starf**, í hlutanum **Frekari upplýsingar**, skal velja **Affordable Care-trygging**.</span><span class="sxs-lookup"><span data-stu-id="60eed-175">On the **Employment** tab, in the **More information** section, select **Affordable Care coverage**.</span></span>

    ![Valkostum breytt fyrir einn starfsmann](./media/hr-benefits-management-aca-change-single-employee.png)

4. <span data-ttu-id="60eed-177">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="60eed-177">Select **Edit**.</span></span>
5. <span data-ttu-id="60eed-178">Fyrir hvern mánuð sem krefst breytinga skal velja gátreitinn **Hnekkja sjálfgildi** og síðan breyta hinum gildunum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="60eed-178">For each month that requires changes, select the **Override default** check box, and then change the other values as required.</span></span>

    ![Sjálfgefnum gildum hnekkt](./media/hr-benefits-management-aca-override-default.png)

6. <span data-ttu-id="60eed-180">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="60eed-180">Select **Save**.</span></span>

## <a name="report-health-care-coverage"></a><span data-ttu-id="60eed-181">Tilkynna heilbrigðistryggingu</span><span class="sxs-lookup"><span data-stu-id="60eed-181">Report health care coverage</span></span>

<span data-ttu-id="60eed-182">Fylgjast verður með sjálftryggðri heilbrigðistryggingu sem vinnuveitandi greiðir fyrir starfsmenn í fullu starfi og hlutastarfi.</span><span class="sxs-lookup"><span data-stu-id="60eed-182">You must track any employer-sponsored, self-insured health care coverage for full-time and part-time employees.</span></span> <span data-ttu-id="60eed-183">Hafið með hvern starfsmann auk skjólstæðinga hans á eyðublaði 1095-C fyrir mánuðina sem þeir eru tryggðir.</span><span class="sxs-lookup"><span data-stu-id="60eed-183">Include each employee, together with their dependents, on the 1095-C report for the months when they were covered.</span></span>

<span data-ttu-id="60eed-184">Til að gefa til kynna hvort tilkynna verður fríðindaáætlun skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="60eed-184">To indicate whether a benefit plan must be reported, follow these steps.</span></span>

1. <span data-ttu-id="60eed-185">Á vinnusvæðinu **Fríðindastjórnun** skal velja **Fríðindaáætlanir**.</span><span class="sxs-lookup"><span data-stu-id="60eed-185">In the **Benefits management** workspace, select **Benefit plans**.</span></span>
2. <span data-ttu-id="60eed-186">Veljið fríðindaáætlunina sem á að tilkynna.</span><span class="sxs-lookup"><span data-stu-id="60eed-186">Select the benefit plan to report.</span></span>
3. <span data-ttu-id="60eed-187">Veljið **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="60eed-187">Select **Edit**.</span></span>
4. <span data-ttu-id="60eed-188">Stillið valkostinn **Tilkynningarskylt samkvæmt Affordable Care Act** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="60eed-188">Set the **Reported under the Affordable Care Act** option to **Yes**.</span></span>

    ![Skráning sjúkratrygginga](./media/hr-benefits-management-aca-report-coverage.png)

5. <span data-ttu-id="60eed-190">Veljið **Vista**.</span><span class="sxs-lookup"><span data-stu-id="60eed-190">Select **Save**.</span></span>

<span data-ttu-id="60eed-191">Ef starfsmaður velur heilbrigðistryggingu fyrir skjólstæðing er tryggingartímabil skjólstæðingsins ákvarðað af dagsetningunni þegar hann var skráður eða fjarlægður.</span><span class="sxs-lookup"><span data-stu-id="60eed-191">If an employee chooses health care coverage for a dependent, the dependent's coverage period is determined by the date when the dependent was enrolled or removed.</span></span> <span data-ttu-id="60eed-192">Tryggingadagsetningar fyrir skjólstæðing eru sjálfkrafa reiknaðar út frá tímabilinu þegar skjólstæðingurinn var tryggður og virkur í áætlun á skráningarárinu.</span><span class="sxs-lookup"><span data-stu-id="60eed-192">Coverage dates for dependents are automatically calculated based on the period when the dependent was eligible and active in a plan during the enrollment year.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="60eed-193">Búa til eyðublöð 1095-B og 1095-C</span><span class="sxs-lookup"><span data-stu-id="60eed-193">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="60eed-194">Hægt er að búa til eyðublöðin ACA 1095-B og 1095-C og síðan dreifa þeim til allra starfsmanna þinna.</span><span class="sxs-lookup"><span data-stu-id="60eed-194">You can generate ACA 1095-B and 1095-C forms, and then distribute them to each of your employees.</span></span> <span data-ttu-id="60eed-195">Einnig er hægt að búa rafrænt til eyðublöð 1095-C og samsvarandi 1094-C skilaskrár til að senda á bandarísk skattyfirvöld (IRS).</span><span class="sxs-lookup"><span data-stu-id="60eed-195">You can also electronically generate Form 1095-C and the corresponding 1094-C transmittal files to send to the Internal Revenue Service (IRS).</span></span>

1. <span data-ttu-id="60eed-196">Á vinnusvæðinu **Fríðindastjórnun** skal velja **Eyðublað ACA 1095-B** eða **Eyðublað ACA 1095-C**.</span><span class="sxs-lookup"><span data-stu-id="60eed-196">In the **Benefits management** workspace, select **ACA 1095-B form** or **ACA 1095-C form**.</span></span>
2. <span data-ttu-id="60eed-197">Breytið færibreytum eins og krafist er og veljið svo **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="60eed-197">Change the parameters as required, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="60eed-198">Ef eyðublað 1095-C er prentað fyrir fleiri en 500 starfsmenn, færðu fleiri en eina PDF-skrá afhenta.</span><span class="sxs-lookup"><span data-stu-id="60eed-198">If you're printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="60eed-199">Mælt er með því að auka gildið í reitnum **Hámarksstærð skráar í megabætum** á síðunni **Færibreytur skjalastjórnunar** í **150**.</span><span class="sxs-lookup"><span data-stu-id="60eed-199">We recommend that you increase the value of the **Maximum file size in megabytes** field on the **Document management parameters** page to **150**.</span></span> <span data-ttu-id="60eed-200">(Til að opna þessa síðu á fljótlegan hátt er hægt að nota leitarsvæðið á yfirlitsstikunni.)</span><span class="sxs-lookup"><span data-stu-id="60eed-200">(To quickly open that page, you can use the search field on the navigation bar.)</span></span>
    >
    > ![Hámarksstærð skráar breytt](./media/hr-benefits-management-aca-maximum-file-size.png)

3. <span data-ttu-id="60eed-202">Til að athuga stöðu skýrslnanna og skoða þær skal nota leitarsvæðið á yfirlitsstikunni til að opna síðuna **Rafræn skýrslugerðarvinnsla**.</span><span class="sxs-lookup"><span data-stu-id="60eed-202">To check the status of your reports and view them, use the search field on the navigation bar to open the **Electronic reporting jobs** page.</span></span>

    ![Leitað að síðu rafrænnar skýrslugerðarvinnslu](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. <span data-ttu-id="60eed-204">Veljið skýrslurnar sem á að skoða og veljið síðan **Sýna skrár**.</span><span class="sxs-lookup"><span data-stu-id="60eed-204">Select the report to view, and then select **Show files**.</span></span>

    ![Skrár sýndar](./media/hr-benefits-management-aca-show-files.png)

5. <span data-ttu-id="60eed-206">Veljið **Opna**.</span><span class="sxs-lookup"><span data-stu-id="60eed-206">Select **Open**.</span></span>

    ![Skrá opnuð](./media/hr-benefits-management-aca-open-file.png)

6. <span data-ttu-id="60eed-208">Úr tilkynningastikunni sem birtist neðst í vafraglugganum skal opna zip-skrána og síðan velja skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="60eed-208">From the Notification bar that appears at the bottom of the browser window, open the zip file, and then select the report.</span></span> <span data-ttu-id="60eed-209">Hægt er að skoða eða prenta út PDF-skrána.</span><span class="sxs-lookup"><span data-stu-id="60eed-209">You can view or print the PDF file.</span></span>

    ![Sýnishorn af eyðublaði 1095-C](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a><span data-ttu-id="60eed-211">Skoða upplýsingar um ACA-tryggingu</span><span class="sxs-lookup"><span data-stu-id="60eed-211">View ACA coverage information</span></span>

<span data-ttu-id="60eed-212">Síðan **Affordable Care-trygging fyrir starfsmann** sýnir eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="60eed-212">The **Worker Affordable Care coverage** page shows the following information:</span></span>

- <span data-ttu-id="60eed-213">Starfsmenn sem úthlutað er í hvern tryggingaflokk</span><span class="sxs-lookup"><span data-stu-id="60eed-213">Employees who are assigned to each coverage group</span></span>
- <span data-ttu-id="60eed-214">Starfsmenn sem þurfa ekki að vera í skýrslu</span><span class="sxs-lookup"><span data-stu-id="60eed-214">Employees who don't have to be included on a report</span></span>
- <span data-ttu-id="60eed-215">Óúthlutaða starfsmenn</span><span class="sxs-lookup"><span data-stu-id="60eed-215">Unassigned employees</span></span>

<span data-ttu-id="60eed-216">Til að skoða þessar upplýsingar skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="60eed-216">To view this information, follow these steps.</span></span>

1. <span data-ttu-id="60eed-217">Á vinnusvæðinu **Fríðindastjórnun** skal velja **Affordable Care-trygging fyrir starfsmann**.</span><span class="sxs-lookup"><span data-stu-id="60eed-217">In the **Benefits management** workspace, select **Worker Affordable Care coverage**.</span></span>
2. <span data-ttu-id="60eed-218">Í reitnum **Heiti flokks** skal velja flokk.</span><span class="sxs-lookup"><span data-stu-id="60eed-218">In the **Group name** field, select a group.</span></span>

    ![ACA-trygging skoðuð](./media/hr-benefits-management-aca-view-coverage.png)

<span data-ttu-id="60eed-220">Ef einhverjum sjálfgefnum gildum úr Affordable Care-tryggingaflokknum hefur verið hnekkt, birtist stjarna við hliðina á gildinu sem var breytt.</span><span class="sxs-lookup"><span data-stu-id="60eed-220">If any default values from the Affordable Care coverage group have been overridden, an asterisk appears next to the value that was changed.</span></span> <span data-ttu-id="60eed-221">Ef gildin fyrir alla 12 mánuðina eru þau sömu og hefur ekki verið hnekkt birtist gildið í dálknum **Allir 12 mánuðirnir**.</span><span class="sxs-lookup"><span data-stu-id="60eed-221">If the values for all 12 months are the same and haven't been overridden, the value appears in the **All 12 months** column.</span></span>

<span data-ttu-id="60eed-222">Hægt er að skoða starfsmenn sem eru merktir sem ekki ACA-tilkynningaskyldir og þurfa ekki eyðublað 1095-C.</span><span class="sxs-lookup"><span data-stu-id="60eed-222">You can view employees who are marked as not ACA-reportable, and who won't require a Form 1095-C.</span></span> <span data-ttu-id="60eed-223">Í reitnum **Sía eftir** skal velja **Er ekki ACA-tilkynningaskylt**.</span><span class="sxs-lookup"><span data-stu-id="60eed-223">In the **Filter by** field, select **Not ACA reportable**.</span></span>

<span data-ttu-id="60eed-224">Hægt er að skoða starfsmenn sem ekki er búið að úthluta í flokk eða er úthlutað í útrunninn flokk.</span><span class="sxs-lookup"><span data-stu-id="60eed-224">You can view employees who aren't assigned to a group, or who are assigned to an expired group.</span></span> <span data-ttu-id="60eed-225">Í **Sía eftir** skal velja **Óúthlutaður eða útrunninn flokkur**.</span><span class="sxs-lookup"><span data-stu-id="60eed-225">In the **Filter by** field, select **Unassigned or expired group**.</span></span>

### <a name="export-to-excel"></a><span data-ttu-id="60eed-226">Flytja út í Excel</span><span class="sxs-lookup"><span data-stu-id="60eed-226">Export to Excel</span></span>

<span data-ttu-id="60eed-227">Til að flytja út einhvern listanna í Microsoft Excel skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="60eed-227">To export any of the lists to Microsoft Excel, follow these steps.</span></span>

1. <span data-ttu-id="60eed-228">Veljið hnappinn **Opna í Microsoft Office**.</span><span class="sxs-lookup"><span data-stu-id="60eed-228">Select the **Open in Microsoft Office** button.</span></span>
2. <span data-ttu-id="60eed-229">Veljið **Bráðabirgðatafla HCM Human Resources til notkunar innanhúss**.</span><span class="sxs-lookup"><span data-stu-id="60eed-229">Select **HCM Human Resources temporary table for internal use**.</span></span>
3. <span data-ttu-id="60eed-230">Veljið **Hlaða niður**.</span><span class="sxs-lookup"><span data-stu-id="60eed-230">Select **Download**.</span></span>

### <a name="view-aca-reportable-dependents"></a><span data-ttu-id="60eed-231">Skoða skjólstæðinga sem eru ACA-tilkynningaskyldir</span><span class="sxs-lookup"><span data-stu-id="60eed-231">View ACA-reportable dependents</span></span>

<span data-ttu-id="60eed-232">Ef þarf að tilkynna tryggða einstaklinga vegna þess að þú býður upp á sjálfstryggða tryggingu, er hægt að skoða skjólstæðinga sem eru tryggðir undir fríðindaáætlunum sem eru merktar sem **ACA-tilkynningaskylt**.</span><span class="sxs-lookup"><span data-stu-id="60eed-232">If you must report covered individuals because you provide self-insured coverage, you can view dependents who are covered under benefit plans that are marked as **ACA reportable**.</span></span> <span data-ttu-id="60eed-233">Á aðgerðasvæðinu skal velja **Skoða tryggingar skjólstæðinga**.</span><span class="sxs-lookup"><span data-stu-id="60eed-233">On the Action Pane, select **View Dependent coverage**.</span></span>

![Tryggingar skjólstæðinga skoðaðar](./media/hr-benefits-management-aca-view-dependent-coverage.png)

<span data-ttu-id="60eed-235">Upplýsingar um tryggingu skjólstæðinga starfsmanns eru sýndar.</span><span class="sxs-lookup"><span data-stu-id="60eed-235">Coverage information for the employee's dependents is shown.</span></span>

![Tryggingar skjólstæðinga](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> <span data-ttu-id="60eed-237">Síðan sýnir aðeins fríðindaáætlanir sem eru merktar sem **ACA-tilkynningaskyldar**.</span><span class="sxs-lookup"><span data-stu-id="60eed-237">The page shows only benefits plans that are marked as **ACA reportable**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]