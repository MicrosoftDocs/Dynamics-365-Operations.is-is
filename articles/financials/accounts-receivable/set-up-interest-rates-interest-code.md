---
title: Setja upp vaxtastig fyrir vaxtakóða
description: Vaxtakóðar innihalda stillingar sem ákveða hvenær vextir eru gjaldfærðir og hvernig það er reiknað á gjaldfallna reikninga.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 665c58fd29fb986bf51e10f5814c4793940c0a47
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545579"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="dff24-103">Setja upp vaxtastig fyrir vaxtakóða</span><span class="sxs-lookup"><span data-stu-id="dff24-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dff24-104">Vaxtakóðar innihalda stillingar sem ákveða hvenær vextir eru gjaldfærðir og hvernig það er reiknað á gjaldfallna reikninga.</span><span class="sxs-lookup"><span data-stu-id="dff24-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="dff24-105">Hægt er að setja upp staka vaxtakóða og jafna hann við margar bókunarreglur viðskiptavina, innheimtukóða, eða tilteknar reikningslínur.</span><span class="sxs-lookup"><span data-stu-id="dff24-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="dff24-106">Þegar upplýsingum vaxtakóða er breytt, munu allar aðgerðir sem nota kóðann sjálfkrafa innleiða breytingarnar í nýju færslunum.</span><span class="sxs-lookup"><span data-stu-id="dff24-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="dff24-107">Fyrir hvern vaxtakóða er hægt að setja upp tvær gerðir taxta:</span><span class="sxs-lookup"><span data-stu-id="dff24-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="dff24-108">Taxtar fyrir vaxtatekjur− þeir tákna tekjur sem eru áunnar með því að skuldfæra vexti á reikninga eða vaxtanótur.</span><span class="sxs-lookup"><span data-stu-id="dff24-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="dff24-109">Taxtar fyrir vaxtagreiðslur − Þeir standa fyrir kostnað sem er greiddur fyrir vexti á kreditnótum.</span><span class="sxs-lookup"><span data-stu-id="dff24-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="dff24-110">Báðar þessar taxtategundir geta verið til á sama tíma og í sama vaxtakóða.</span><span class="sxs-lookup"><span data-stu-id="dff24-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="dff24-111">Vextir geta byggst á þremur gerðum útreikninga:</span><span class="sxs-lookup"><span data-stu-id="dff24-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="dff24-112">Vextir Eftir prósentu</span><span class="sxs-lookup"><span data-stu-id="dff24-112">Interest by percentage.</span></span>
-   <span data-ttu-id="dff24-113">Vextir eftir upphæð</span><span class="sxs-lookup"><span data-stu-id="dff24-113">Interest by amount.</span></span>
-   <span data-ttu-id="dff24-114">Vextir eftir sviði, sem leiðir til einnar prósentu eða upphæðar</span><span class="sxs-lookup"><span data-stu-id="dff24-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="dff24-115">Þegar vaxtakóði er notaður til að reikna vexti, er sérstök vaxtanóta stofnuð fyrir hvert vaxtastig sem er í gildi á þeim tíma er greiðsla hefur farið framyfir gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="dff24-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="dff24-116">Nota skal **hagnaður** flipanum á **Vaxtakóði** síðunni til að setja upp vexti fyrir vexti sem þú vinnur þér inn með því að rukka vexti..</span><span class="sxs-lookup"><span data-stu-id="dff24-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="dff24-117">Til að setja upp vaxtastig fyrir vexti sem greiddir eru skal nota **greiðslur** flipann.</span><span class="sxs-lookup"><span data-stu-id="dff24-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="dff24-118">Setja upp vexti á grundvelli prósenta</span><span class="sxs-lookup"><span data-stu-id="dff24-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="dff24-119">Hægt er að setja upp vaxtastig sem reiknar út tilgreinda prósentu.</span><span class="sxs-lookup"><span data-stu-id="dff24-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="dff24-120">Upphæð vaxta gildir um alla gjaldmiðla.</span><span class="sxs-lookup"><span data-stu-id="dff24-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="dff24-121">Hægt er að færa inn valfrjáls takmörk upphæðar fyrir vexti.</span><span class="sxs-lookup"><span data-stu-id="dff24-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="dff24-122"><strong>Prósenta</strong> er valinn\*\* <strong>í \*\*Reikna út vexti á grundvelli</strong> reitnum á síðunni <strong>Setja upp vaxtakóða</strong>.</span><span class="sxs-lookup"><span data-stu-id="dff24-122"><strong>Percentage</strong> is selected\*\* <strong>in the \*\*Calculate interest based on</strong> field on the <strong>Set up Interest codes</strong> page.</span></span>

<span data-ttu-id="dff24-123">Til dæmis til að setja upp vaxtakóða sem metur 5 prósent vexti fyrir hverja tvo mánuði sem reikningurinn fer umfram gjalddaga færslunnar, þá væri fært inn 2 í svæðið **reikna vexti fyrir hvern** og velja **Mánuður**.</span><span class="sxs-lookup"><span data-stu-id="dff24-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="dff24-124">Vextir á grundvelli upphæða</span><span class="sxs-lookup"><span data-stu-id="dff24-124">Interest rates based on amounts</span></span>
<span data-ttu-id="dff24-125">Hægt er að setja upp vaxtastig sem reiknar út tilgreinda upphæð fyrir hvern gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="dff24-125">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="dff24-126">Vaxtaupphæð er tilgreind fyrir hvern gjaldmiðil í vaxtakóða.</span><span class="sxs-lookup"><span data-stu-id="dff24-126">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="dff24-127">Hægt er að færa inn valfrjáls takmörk upphæðar fyrir vexti.</span><span class="sxs-lookup"><span data-stu-id="dff24-127">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="dff24-128">**Upphæð** er valinn í **Reikna út vexti á grundvelli**svæði á **Setja upp Vaxtakóði** síða.</span><span class="sxs-lookup"><span data-stu-id="dff24-128">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="dff24-129">Til dæmis til að setja upp vaxtakóða sem metur 25,00 prósent vexti fyrir hverja 20 daga sem reikningurinn fer umfram gjalddaga færslunnar, þá væri fært inn 20 í svæðið **reikna vexti fyrir hvern** og velja **Dagur**.</span><span class="sxs-lookup"><span data-stu-id="dff24-129">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="dff24-130">Vextir á grundvelli sviða</span><span class="sxs-lookup"><span data-stu-id="dff24-130">Interest rates based on ranges</span></span>
<span data-ttu-id="dff24-131">Hægt er að setja upp vaxtastig sem eru mismunandi eftir því hvaða upphæð fallin í gjalddaga, fjölda þeirra daga sem upphæðin er komin fram yfir, eða fjölda mánaða sem upphæðin komin fram yfir.</span><span class="sxs-lookup"><span data-stu-id="dff24-131">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="dff24-132">Hægt er að nota **Hagnaður eftir Gjaldmiðli** flipa til að skilgreina stillingar fyrir ákveðna vexti fyrir hvern gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="dff24-132">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="dff24-133">Þetta er einnig þar sem verður að skilgreina svið.</span><span class="sxs-lookup"><span data-stu-id="dff24-133">This is also where you will define the range.</span></span>
-   <span data-ttu-id="dff24-134">Nota skal **svið** hnappinn til að bæta við línum sem tákna svið sem á að setja upp.</span><span class="sxs-lookup"><span data-stu-id="dff24-134">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="dff24-135">**Frá** gildi stendur fyrir upphaf sviðsins og **Vaxtagildi** númer stendur fyrir annað hvort hlutfall eða upphæð, eftir því sem valið er í **Reikna vexti á grundvelli** í **Setja upp vaxtakóða** síðu.</span><span class="sxs-lookup"><span data-stu-id="dff24-135">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="dff24-136">Dæmi 1: Vextir eftir afmörkun = upphæð</span><span class="sxs-lookup"><span data-stu-id="dff24-136">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="dff24-137">Hægt er að setja upp vaxtakóðann sem metur vexti einu sinni fyrir þriðja hvern mánuð sem reikningurinn er umfram gjalddaga færslunnar.</span><span class="sxs-lookup"><span data-stu-id="dff24-137">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="dff24-138">Óskað er eftir að byggja útreikning á prósentugildi vaxta, samkvæmt skrefskiptum upphæðarbilum.</span><span class="sxs-lookup"><span data-stu-id="dff24-138">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="dff24-139">Vaxtagildið verður 1 prósent fyrir reikningsupphæðir allt að 1.000,00, 2 prósent fyrir upphæðir frá 1.001,00 til 5.000,00 og 3 prósent fyrir upphæðir hærri en 5.000,00.</span><span class="sxs-lookup"><span data-stu-id="dff24-139">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="dff24-140">Gildi svæða fyrir vaxtakóða eru sett upp á eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="dff24-140">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="dff24-141">**Nafn svæðis**</span><span class="sxs-lookup"><span data-stu-id="dff24-141">**Field name**</span></span>                  | <span data-ttu-id="dff24-142">**Svæðisgildi**</span><span class="sxs-lookup"><span data-stu-id="dff24-142">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="dff24-143">**Vaxtakóði**</span><span class="sxs-lookup"><span data-stu-id="dff24-143">**Interest code**</span></span>               | <span data-ttu-id="dff24-144">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="dff24-144">3M%ByAmt</span></span>        |
| <span data-ttu-id="dff24-145">**Reikna vexti hverja**</span><span class="sxs-lookup"><span data-stu-id="dff24-145">**Calculate interest every**</span></span>    | <span data-ttu-id="dff24-146">3/Mánuður</span><span class="sxs-lookup"><span data-stu-id="dff24-146">3/Month</span></span>         |
| <span data-ttu-id="dff24-147">**Vextir eftir afmörkun**</span><span class="sxs-lookup"><span data-stu-id="dff24-147">**Interest by range**</span></span>           | <span data-ttu-id="dff24-148">Upphæð</span><span class="sxs-lookup"><span data-stu-id="dff24-148">Amount</span></span>          |
| <span data-ttu-id="dff24-149">**Reikna vexti út frá**</span><span class="sxs-lookup"><span data-stu-id="dff24-149">**Calculate interest based on**</span></span> | <span data-ttu-id="dff24-150">Prósenta</span><span class="sxs-lookup"><span data-stu-id="dff24-150">Percentage</span></span>      |

<span data-ttu-id="dff24-151">Settar eru upp upplýsingar um afmörkun sem hér segir.</span><span class="sxs-lookup"><span data-stu-id="dff24-151">You set up the range information as follows.</span></span>

| <span data-ttu-id="dff24-152">**Frá gildi**</span><span class="sxs-lookup"><span data-stu-id="dff24-152">**From value**</span></span> | <span data-ttu-id="dff24-153">**Vaxtagildi**</span><span class="sxs-lookup"><span data-stu-id="dff24-153">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="dff24-154">0</span><span class="sxs-lookup"><span data-stu-id="dff24-154">0</span></span>              | <span data-ttu-id="dff24-155">1</span><span class="sxs-lookup"><span data-stu-id="dff24-155">1</span></span>                  |
| <span data-ttu-id="dff24-156">1,001</span><span class="sxs-lookup"><span data-stu-id="dff24-156">1,001</span></span>          | <span data-ttu-id="dff24-157">2</span><span class="sxs-lookup"><span data-stu-id="dff24-157">2</span></span>                  |
| <span data-ttu-id="dff24-158">5,001</span><span class="sxs-lookup"><span data-stu-id="dff24-158">5,001</span></span>          | <span data-ttu-id="dff24-159">3</span><span class="sxs-lookup"><span data-stu-id="dff24-159">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="dff24-160">Dæmi 2: Vextir eftir afmörkun = Dagar</span><span class="sxs-lookup"><span data-stu-id="dff24-160">Example 2: Interest by range = Days</span></span>
--------------------------------------------------

<span data-ttu-id="dff24-161">Hægt er að setja upp vaxtakóðann sem metur vexti einu sinni fyrir 15. hvern dag sem reikningurinn er umfram gjalddaga færslunnar.</span><span class="sxs-lookup"><span data-stu-id="dff24-161">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="dff24-162">Óskað er eftir að byggja útreikning á upphæðargildi vaxta, samkvæmt skrefskiptum dagabilum.</span><span class="sxs-lookup"><span data-stu-id="dff24-162">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="dff24-163">Gildi vaxta verður 10,00 á 15 daga á fyrstu 60 dögunum, 15,00 á 15 daga á dögum 61 til 90 og 20,00 á 15 daga frá deginum 91 og síðar.</span><span class="sxs-lookup"><span data-stu-id="dff24-163">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="dff24-164">Gildi svæða fyrir vaxtakóða eru sett upp á eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="dff24-164">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="dff24-165">**Nafn svæðis**</span><span class="sxs-lookup"><span data-stu-id="dff24-165">**Field name**</span></span>                  | <span data-ttu-id="dff24-166">**Svæðisgildi**</span><span class="sxs-lookup"><span data-stu-id="dff24-166">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="dff24-167">**Vaxtakóði**</span><span class="sxs-lookup"><span data-stu-id="dff24-167">**Interest code**</span></span>               | <span data-ttu-id="dff24-168">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="dff24-168">15DAmtXDay</span></span>      |
| <span data-ttu-id="dff24-169">**Reikna vexti hverja**</span><span class="sxs-lookup"><span data-stu-id="dff24-169">**Calculate interest every**</span></span>    | <span data-ttu-id="dff24-170">15/Dagur</span><span class="sxs-lookup"><span data-stu-id="dff24-170">15/Day</span></span>          |
| <span data-ttu-id="dff24-171">**Vextir eftir afmörkun**</span><span class="sxs-lookup"><span data-stu-id="dff24-171">**Interest by range**</span></span>           | <span data-ttu-id="dff24-172">Dagar</span><span class="sxs-lookup"><span data-stu-id="dff24-172">Days</span></span>            |
| <span data-ttu-id="dff24-173">**Reikna vexti út frá**</span><span class="sxs-lookup"><span data-stu-id="dff24-173">**Calculate interest based on**</span></span> | <span data-ttu-id="dff24-174">Upphæð</span><span class="sxs-lookup"><span data-stu-id="dff24-174">Amount</span></span>          |

<span data-ttu-id="dff24-175">Settar eru upp upplýsingar um afmörkun sem hér segir.</span><span class="sxs-lookup"><span data-stu-id="dff24-175">You set up the range information as follows.</span></span>

| <span data-ttu-id="dff24-176">**Frá gildi**</span><span class="sxs-lookup"><span data-stu-id="dff24-176">**From value**</span></span> | <span data-ttu-id="dff24-177">**Vaxtagildi**</span><span class="sxs-lookup"><span data-stu-id="dff24-177">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="dff24-178">0</span><span class="sxs-lookup"><span data-stu-id="dff24-178">0</span></span>              | <span data-ttu-id="dff24-179">10</span><span class="sxs-lookup"><span data-stu-id="dff24-179">10</span></span>                 |
| <span data-ttu-id="dff24-180">61</span><span class="sxs-lookup"><span data-stu-id="dff24-180">61</span></span>             | <span data-ttu-id="dff24-181">15</span><span class="sxs-lookup"><span data-stu-id="dff24-181">15</span></span>                 |
| <span data-ttu-id="dff24-182">91</span><span class="sxs-lookup"><span data-stu-id="dff24-182">91</span></span>             | <span data-ttu-id="dff24-183">20</span><span class="sxs-lookup"><span data-stu-id="dff24-183">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="dff24-184">Dæmi 3: Vextir eftir afmörkun = mánuðir</span><span class="sxs-lookup"><span data-stu-id="dff24-184">Example 3: Interest by range = Months</span></span>
----------------------------------------------------

<span data-ttu-id="dff24-185">Hægt er að setja upp vaxtakóðann sem metur vexti einu sinni fyrir hvern mánuð sem reikningurinn er umfram gjalddaga færslunnar.</span><span class="sxs-lookup"><span data-stu-id="dff24-185">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="dff24-186">Óskað er eftir að byggja útreikning á prósentugildi vaxta, samkvæmt skrefskiptum mánaðarbilum.</span><span class="sxs-lookup"><span data-stu-id="dff24-186">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="dff24-187">Vaxta gildi verður 1,5 prósent hvern mánuð fyrir fyrstu þrjá gjaldfallna mánuðina, 2,0 prósent fyrir næstu þrjá mánuði og 2,5 prósent á mánuði fyrir hvern mánuð umfram fyrstu sex mánuði.</span><span class="sxs-lookup"><span data-stu-id="dff24-187">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="dff24-188">Gildi svæða fyrir vaxtakóða eru sett upp á eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="dff24-188">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="dff24-189">**Nafn svæðis**</span><span class="sxs-lookup"><span data-stu-id="dff24-189">**Field name**</span></span>                  | <span data-ttu-id="dff24-190">**Svæðisgildi**</span><span class="sxs-lookup"><span data-stu-id="dff24-190">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="dff24-191">**Vaxtakóði**</span><span class="sxs-lookup"><span data-stu-id="dff24-191">**Interest code**</span></span>               | <span data-ttu-id="dff24-192">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="dff24-192">1M%ByMth</span></span>        |
| <span data-ttu-id="dff24-193">**Reikna vexti hverja**</span><span class="sxs-lookup"><span data-stu-id="dff24-193">**Calculate interest every**</span></span>    | <span data-ttu-id="dff24-194">1/mánuður</span><span class="sxs-lookup"><span data-stu-id="dff24-194">1/Month</span></span>         |
| <span data-ttu-id="dff24-195">**Vextir eftir afmörkun**</span><span class="sxs-lookup"><span data-stu-id="dff24-195">**Interest by range**</span></span>           | <span data-ttu-id="dff24-196">Mánuðir</span><span class="sxs-lookup"><span data-stu-id="dff24-196">Months</span></span>          |
| <span data-ttu-id="dff24-197">**Reikna vexti út frá**</span><span class="sxs-lookup"><span data-stu-id="dff24-197">**Calculate interest based on**</span></span> | <span data-ttu-id="dff24-198">Prósenta</span><span class="sxs-lookup"><span data-stu-id="dff24-198">Percentage</span></span>      |

<span data-ttu-id="dff24-199">Settar eru upp upplýsingar um afmörkun sem hér segir.</span><span class="sxs-lookup"><span data-stu-id="dff24-199">You set up the range information as follows.</span></span>

| <span data-ttu-id="dff24-200">**Frá gildi**</span><span class="sxs-lookup"><span data-stu-id="dff24-200">**From value**</span></span> | <span data-ttu-id="dff24-201">**Vaxtagildi**</span><span class="sxs-lookup"><span data-stu-id="dff24-201">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="dff24-202">0</span><span class="sxs-lookup"><span data-stu-id="dff24-202">0</span></span>              | <span data-ttu-id="dff24-203">1.5</span><span class="sxs-lookup"><span data-stu-id="dff24-203">1.5</span></span>                |
| <span data-ttu-id="dff24-204">4</span><span class="sxs-lookup"><span data-stu-id="dff24-204">4</span></span>              | <span data-ttu-id="dff24-205">2</span><span class="sxs-lookup"><span data-stu-id="dff24-205">2</span></span>                  |
| <span data-ttu-id="dff24-206">7</span><span class="sxs-lookup"><span data-stu-id="dff24-206">7</span></span>              | <span data-ttu-id="dff24-207">2,5</span><span class="sxs-lookup"><span data-stu-id="dff24-207">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="dff24-208">Nýjar útgáfur</span><span class="sxs-lookup"><span data-stu-id="dff24-208">New versions</span></span>
<span data-ttu-id="dff24-209">Vaxtakóðar eru gildir eftir dagsetningum.</span><span class="sxs-lookup"><span data-stu-id="dff24-209">Interest codes are date effective.</span></span> <span data-ttu-id="dff24-210">Ef þú vilt breyta vöxtum, geturðu stofnað **nýja útgáfu** sem tekur gildi frá og með framtíðardagsetningu.</span><span class="sxs-lookup"><span data-stu-id="dff24-210">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="dff24-211">Til að skoða mismunandi útgáfur er hægt að nota í **frá og með** val til að velja lokadagsetninguna.</span><span class="sxs-lookup"><span data-stu-id="dff24-211">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="dff24-212">Einnig er hægt að velja **Birta allar færslur** til að skoða allar vaxtakóðum á síðunni.</span><span class="sxs-lookup"><span data-stu-id="dff24-212">You can also select the **Display all records** to view all interest codes in the page.</span></span>



