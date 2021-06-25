---
title: Setja upp vaxtastig fyrir vaxtakóða
description: Vaxtakóðar innihalda stillingar sem ákveða hvenær vextir eru gjaldfærðir og hvernig það er reiknað á gjaldfallna reikninga.
author: ShivamPandey-msft
ms.date: 02/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Interest
audience: Application User
ms.reviewer: roschlom
ms.custom: 59402
ms.assetid: 3b945333-1eaf-4658-ab5a-1a7791a7eb40
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc986ea752d1482f618401058f7a0b18f13efd5f
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188711"
---
# <a name="set-up-interest-rates-for-an-interest-code"></a><span data-ttu-id="ecf2c-103">Setja upp vaxtastig fyrir vaxtakóða</span><span class="sxs-lookup"><span data-stu-id="ecf2c-103">Set up interest rates for an interest code</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecf2c-104">Vaxtakóðar innihalda stillingar sem ákveða hvenær vextir eru gjaldfærðir og hvernig það er reiknað á gjaldfallna reikninga.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-104">Interest codes contain settings that determine when interest is charged and how it is calculated on overdue accounts.</span></span>

<span data-ttu-id="ecf2c-105">Hægt er að setja upp staka vaxtakóða og jafna hann við margar bókunarreglur viðskiptavina, innheimtukóða, eða tilteknar reikningslínur.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-105">You can set up a single interest code and apply it to multiple customer posting profiles, billing codes, or to specific invoice lines.</span></span> <span data-ttu-id="ecf2c-106">Þegar upplýsingum vaxtakóða er breytt, munu allar aðgerðir sem nota kóðann sjálfkrafa innleiða breytingarnar í nýju færslunum.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-106">When the interest code details are changed, all features that use the code will automatically implement the changes on new transactions.</span></span> <span data-ttu-id="ecf2c-107">Fyrir hvern vaxtakóða er hægt að setja upp tvær gerðir taxta:</span><span class="sxs-lookup"><span data-stu-id="ecf2c-107">For each interest code, you can set up two types of rates:</span></span>
-   <span data-ttu-id="ecf2c-108">Taxtar fyrir vaxtatekjur− þeir tákna tekjur sem eru áunnar með því að skuldfæra vexti á reikninga eða vaxtanótur.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-108">Rates for interest earnings − These represent revenue that is earned by charging interest on invoices or interest notes.</span></span>
-   <span data-ttu-id="ecf2c-109">Taxtar fyrir vaxtagreiðslur − Þeir standa fyrir kostnað sem er greiddur fyrir vexti á kreditnótum.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-109">Rates for interest payments − These represent a cost that is paid for interest on credit notes.</span></span>

<span data-ttu-id="ecf2c-110">Báðar þessar taxtategundir geta verið til á sama tíma og í sama vaxtakóða.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-110">Both of these rate types can exist at the same time and in the same interest code.</span></span> <span data-ttu-id="ecf2c-111">Vextir geta byggst á þremur gerðum útreikninga:</span><span class="sxs-lookup"><span data-stu-id="ecf2c-111">Interest rates can be based on three calculation types:</span></span>
-   <span data-ttu-id="ecf2c-112">Vextir Eftir prósentu</span><span class="sxs-lookup"><span data-stu-id="ecf2c-112">Interest by percentage.</span></span>
-   <span data-ttu-id="ecf2c-113">Vextir eftir upphæð</span><span class="sxs-lookup"><span data-stu-id="ecf2c-113">Interest by amount.</span></span>
-   <span data-ttu-id="ecf2c-114">Vextir eftir sviði, sem leiðir til einnar prósentu eða upphæðar</span><span class="sxs-lookup"><span data-stu-id="ecf2c-114">Interest by range, which results in a single percentage or amount.</span></span>

<span data-ttu-id="ecf2c-115">Þegar vaxtakóði er notaður til að reikna vexti, er sérstök vaxtanóta stofnuð fyrir hvert vaxtastig sem er í gildi á þeim tíma er greiðsla hefur farið framyfir gjalddaga.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-115">When an interest code is used to calculate interest, a separate interest note is created for each interest rate that is in effect during the time that the payment has exceeded the transaction due date.</span></span> <span data-ttu-id="ecf2c-116">Nota skal **hagnaður** flipanum á **Vaxtakóði** síðunni til að setja upp vexti fyrir vexti sem þú vinnur þér inn með því að rukka vexti..</span><span class="sxs-lookup"><span data-stu-id="ecf2c-116">You use the **Earnings** tab on the **Interest code** page to set up interest rates for interest that you earn by charging interest.</span></span> <span data-ttu-id="ecf2c-117">Til að setja upp vaxtastig fyrir vexti sem greiddir eru skal nota **greiðslur** flipann.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-117">Use the **Payments** tab to set up interest rates for interest that you pay.</span></span>

## <a name="interest-rates-based-on-a-percentage"></a><span data-ttu-id="ecf2c-118">Setja upp vexti á grundvelli prósenta</span><span class="sxs-lookup"><span data-stu-id="ecf2c-118">Interest rates based on a percentage</span></span>
<span data-ttu-id="ecf2c-119">Hægt er að setja upp vaxtastig sem reiknar út tilgreinda prósentu.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-119">You can set up interest rates that calculate a specified percentage.</span></span>

- <span data-ttu-id="ecf2c-120">Upphæð vaxta gildir um alla gjaldmiðla.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-120">Interest amount applies to all currencies.</span></span>
- <span data-ttu-id="ecf2c-121">Hægt er að færa inn valfrjáls takmörk upphæðar fyrir vexti.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-121">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="ecf2c-122">**Prósenta** er valinn í **Reikna út vexti á grundvelli** reitnum á síðöunni **Setja upp vaxtakóða**.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-122">**Percentage** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="ecf2c-123">Til dæmis til að setja upp vaxtakóða sem metur 5 prósent vexti fyrir hverja tvo mánuði sem reikningurinn fer umfram gjalddaga færslunnar, þá væri fært inn 2 í svæðið **reikna vexti fyrir hvern** og velja **Mánuður**.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-123">For example, to set up an interest code that assesses 5 percent interest for every two months that the invoice payment exceeds the transaction due date, you would enter 2 in the **Calculate interest every** field and select **Month**.</span></span>

> [!NOTE] 
> <span data-ttu-id="ecf2c-124">Nýja algrímið fyrir útreikning vaxtanótu er bætt við með Eiginleikastjórnun.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-124">The new algorithm for interest note calculation is added using Feature management.</span></span> <span data-ttu-id="ecf2c-125">Til að nota þetta algrím skal virkja eiginleikann **(GBL) Heimila útreikning vaxta á dag sem árlegt prósentuhlutfall deilt með 365**.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-125">To use this algorithm, enable the **(GBL) Allow to calculate interest per day as yearly percent divided by 365** feature.</span></span> <span data-ttu-id="ecf2c-126">Nánari upplýsingar um hvernig á að virkja eiginleikann er að finna í [Yfirlit eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ecf2c-126">For information about how to enable the feature, see [Feature management overview](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>
> 
> <span data-ttu-id="ecf2c-127">Formúla fyrir útreikning fyrir upphæð vaxtanótu er:</span><span class="sxs-lookup"><span data-stu-id="ecf2c-127">The formula for the calculation for the interest note amount is:</span></span> 
>  
> <span data-ttu-id="ecf2c-128">Upphæð vaxtanótu = Upphæð skuldar *Árlegir vextir % / 365* Fjöldi daga framyfir</span><span class="sxs-lookup"><span data-stu-id="ecf2c-128">Interest note amount = Amount owed \* Yearly interest % / 365 \* Number of days late</span></span>
>  
> <span data-ttu-id="ecf2c-129">Þessi eiginleiki er tiltækur í útgáfu 10.0.18 og nýrri.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-129">This feature is available in version 10.0.18 or later.</span></span>    
 
## <a name="interest-rates-based-on-amounts"></a><span data-ttu-id="ecf2c-130">Vextir á grundvelli upphæða</span><span class="sxs-lookup"><span data-stu-id="ecf2c-130">Interest rates based on amounts</span></span>
<span data-ttu-id="ecf2c-131">Hægt er að setja upp vaxtastig sem reiknar út tilgreinda upphæð fyrir hvern gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-131">You can set up interest rates that calculate a specified amount per currency.</span></span>
- <span data-ttu-id="ecf2c-132">Vaxtaupphæð er tilgreind fyrir hvern gjaldmiðil í vaxtakóða.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-132">An interest amount is specified for each currency in the interest code.</span></span>
- <span data-ttu-id="ecf2c-133">Hægt er að færa inn valfrjáls takmörk upphæðar fyrir vexti.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-133">Optional interest amount limits can be entered.</span></span>
- <span data-ttu-id="ecf2c-134">**Upphæð** er valinn í **Reikna út vexti á grundvelli** svæði á **Setja upp Vaxtakóði** síða.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-134">**Amount** is selected in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

<span data-ttu-id="ecf2c-135">Til dæmis til að setja upp vaxtakóða sem metur 25,00 prósent vexti fyrir hverja 20 daga sem reikningurinn fer umfram gjalddaga færslunnar, þá væri fært inn 20 í svæðið **reikna vexti fyrir hvern** og velja **Dagur**.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-135">For example, to set up an interest code that assesses interest of 25.00 for every 20 days that the invoice payment exceeds the transaction due date, you would enter 20 in the **Calculate interest every** field and select **Day**.</span></span>

## <a name="interest-rates-based-on-ranges"></a><span data-ttu-id="ecf2c-136">Vextir á grundvelli sviða</span><span class="sxs-lookup"><span data-stu-id="ecf2c-136">Interest rates based on ranges</span></span>
<span data-ttu-id="ecf2c-137">Hægt er að setja upp vaxtastig sem eru mismunandi eftir því hvaða upphæð fallin í gjalddaga, fjölda þeirra daga sem upphæðin er komin fram yfir, eða fjölda mánaða sem upphæðin komin fram yfir.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-137">You can set up interest rates that vary depending on the overdue amount, the number of days that the amount is late, or the number of months that the amount is late.</span></span>
-   <span data-ttu-id="ecf2c-138">Hægt er að nota **Hagnaður eftir Gjaldmiðli** flipa til að skilgreina stillingar fyrir ákveðna vexti fyrir hvern gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-138">You can use the **Earnings by Currency** tab to define specific interest settings for each currency.</span></span> <span data-ttu-id="ecf2c-139">Þetta er einnig þar sem verður að skilgreina svið.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-139">This is also where you will define the range.</span></span>
-   <span data-ttu-id="ecf2c-140">Nota skal **svið** hnappinn til að bæta við línum sem tákna svið sem á að setja upp.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-140">Use the **Ranges** button to add lines that represent the ranges that you want to set up.</span></span> <span data-ttu-id="ecf2c-141">**Frá** gildi stendur fyrir upphaf sviðsins og **Vaxtagildi** númer stendur fyrir annað hvort hlutfall eða upphæð, eftir því sem valið er í **Reikna vexti á grundvelli** í **Setja upp vaxtakóða** síðu.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-141">The **From** value represents the beginning of the range and the **Interest value** number represents either a percentage or an amount, depending on the selection in the **Calculate interest based on** field on the **Set up Interest codes** page.</span></span>

## <a name="example-1-interest-by-range--amount"></a><span data-ttu-id="ecf2c-142">Dæmi 1: Vextir eftir afmörkun = upphæð</span><span class="sxs-lookup"><span data-stu-id="ecf2c-142">Example 1: Interest by range = Amount</span></span>
<span data-ttu-id="ecf2c-143">Hægt er að setja upp vaxtakóðann sem metur vexti einu sinni fyrir þriðja hvern mánuð sem reikningurinn er umfram gjalddaga færslunnar.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-143">You set up an interest code that assesses interest one time for every three months that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="ecf2c-144">Óskað er eftir að byggja útreikning á prósentugildi vaxta, samkvæmt skrefskiptum upphæðarbilum.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-144">You want to base the calculation on a percentage interest value, according to stepped amount intervals.</span></span> <span data-ttu-id="ecf2c-145">Vaxtagildið verður 1 prósent fyrir reikningsupphæðir allt að 1.000,00, 2 prósent fyrir upphæðir frá 1.001,00 til 5.000,00 og 3 prósent fyrir upphæðir hærri en 5.000,00.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-145">The interest value will be 1 percent for invoice amounts up to 1,000.00, 2 percent for amounts from 1,001.00 to 5,000.00, and 3 percent for amounts larger than 5,000.00.</span></span> <span data-ttu-id="ecf2c-146">Gildi svæða fyrir vaxtakóða eru sett upp á eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-146">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="ecf2c-147">**Nafn svæðis**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-147">**Field name**</span></span>                  | <span data-ttu-id="ecf2c-148">**Svæðisgildi**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-148">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="ecf2c-149">**Vaxtakóði**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-149">**Interest code**</span></span>               | <span data-ttu-id="ecf2c-150">3M%ByAmt</span><span class="sxs-lookup"><span data-stu-id="ecf2c-150">3M%ByAmt</span></span>        |
| <span data-ttu-id="ecf2c-151">**Reikna vexti hverja**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-151">**Calculate interest every**</span></span>    | <span data-ttu-id="ecf2c-152">3/Mánuður</span><span class="sxs-lookup"><span data-stu-id="ecf2c-152">3/Month</span></span>         |
| <span data-ttu-id="ecf2c-153">**Vextir eftir afmörkun**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-153">**Interest by range**</span></span>           | <span data-ttu-id="ecf2c-154">Upphæð</span><span class="sxs-lookup"><span data-stu-id="ecf2c-154">Amount</span></span>          |
| <span data-ttu-id="ecf2c-155">**Reikna vexti út frá**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-155">**Calculate interest based on**</span></span> | <span data-ttu-id="ecf2c-156">Prósenta</span><span class="sxs-lookup"><span data-stu-id="ecf2c-156">Percentage</span></span>      |

<span data-ttu-id="ecf2c-157">Settar eru upp upplýsingar um afmörkun sem hér segir.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-157">You set up the range information as follows.</span></span>

| <span data-ttu-id="ecf2c-158">**Frá gildi**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-158">**From value**</span></span> | <span data-ttu-id="ecf2c-159">**Vaxtagildi**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-159">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="ecf2c-160">0</span><span class="sxs-lookup"><span data-stu-id="ecf2c-160">0</span></span>              | <span data-ttu-id="ecf2c-161">1</span><span class="sxs-lookup"><span data-stu-id="ecf2c-161">1</span></span>                  |
| <span data-ttu-id="ecf2c-162">1,001</span><span class="sxs-lookup"><span data-stu-id="ecf2c-162">1,001</span></span>          | <span data-ttu-id="ecf2c-163">2</span><span class="sxs-lookup"><span data-stu-id="ecf2c-163">2</span></span>                  |
| <span data-ttu-id="ecf2c-164">5,001</span><span class="sxs-lookup"><span data-stu-id="ecf2c-164">5,001</span></span>          | <span data-ttu-id="ecf2c-165">3</span><span class="sxs-lookup"><span data-stu-id="ecf2c-165">3</span></span>                  |


## <a name="example-2-interest-by-range--days"></a><span data-ttu-id="ecf2c-166">Dæmi 2: Vextir eftir afmörkun = Dagar</span><span class="sxs-lookup"><span data-stu-id="ecf2c-166">Example 2: Interest by range = Days</span></span>

<span data-ttu-id="ecf2c-167">Hægt er að setja upp vaxtakóðann sem metur vexti einu sinni fyrir 15. hvern dag sem reikningurinn er umfram gjalddaga færslunnar.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-167">You set up an interest code that assesses interest one time for every 15 days that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="ecf2c-168">Óskað er eftir að byggja útreikning á upphæðargildi vaxta, samkvæmt skrefskiptum dagabilum.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-168">You want to base the calculation on an amount interest value, according to stepped day intervals.</span></span> <span data-ttu-id="ecf2c-169">Gildi vaxta verður 10,00 á 15 daga á fyrstu 60 dögunum, 15,00 á 15 daga á dögum 61 til 90 og 20,00 á 15 daga frá deginum 91 og síðar.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-169">The interest value will be 10.00 per 15 days during the first 60 days, 15.00 per 15 days during days 61 to 90, and 20.00 per 15 days from day 91 and after.</span></span> <span data-ttu-id="ecf2c-170">Gildi svæða fyrir vaxtakóða eru sett upp á eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-170">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="ecf2c-171">**Nafn svæðis**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-171">**Field name**</span></span>                  | <span data-ttu-id="ecf2c-172">**Svæðisgildi**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-172">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="ecf2c-173">**Vaxtakóði**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-173">**Interest code**</span></span>               | <span data-ttu-id="ecf2c-174">15DAmtXDay</span><span class="sxs-lookup"><span data-stu-id="ecf2c-174">15DAmtXDay</span></span>      |
| <span data-ttu-id="ecf2c-175">**Reikna vexti hverja**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-175">**Calculate interest every**</span></span>    | <span data-ttu-id="ecf2c-176">15/Dagur</span><span class="sxs-lookup"><span data-stu-id="ecf2c-176">15/Day</span></span>          |
| <span data-ttu-id="ecf2c-177">**Vextir eftir afmörkun**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-177">**Interest by range**</span></span>           | <span data-ttu-id="ecf2c-178">Dagar</span><span class="sxs-lookup"><span data-stu-id="ecf2c-178">Days</span></span>            |
| <span data-ttu-id="ecf2c-179">**Reikna vexti út frá**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-179">**Calculate interest based on**</span></span> | <span data-ttu-id="ecf2c-180">Upphæð</span><span class="sxs-lookup"><span data-stu-id="ecf2c-180">Amount</span></span>          |

<span data-ttu-id="ecf2c-181">Settar eru upp upplýsingar um afmörkun sem hér segir.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-181">You set up the range information as follows.</span></span>

| <span data-ttu-id="ecf2c-182">**Frá gildi**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-182">**From value**</span></span> | <span data-ttu-id="ecf2c-183">**Vaxtagildi**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-183">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="ecf2c-184">0</span><span class="sxs-lookup"><span data-stu-id="ecf2c-184">0</span></span>              | <span data-ttu-id="ecf2c-185">10</span><span class="sxs-lookup"><span data-stu-id="ecf2c-185">10</span></span>                 |
| <span data-ttu-id="ecf2c-186">61</span><span class="sxs-lookup"><span data-stu-id="ecf2c-186">61</span></span>             | <span data-ttu-id="ecf2c-187">15</span><span class="sxs-lookup"><span data-stu-id="ecf2c-187">15</span></span>                 |
| <span data-ttu-id="ecf2c-188">91</span><span class="sxs-lookup"><span data-stu-id="ecf2c-188">91</span></span>             | <span data-ttu-id="ecf2c-189">20</span><span class="sxs-lookup"><span data-stu-id="ecf2c-189">20</span></span>                 |


## <a name="example-3-interest-by-range--months"></a><span data-ttu-id="ecf2c-190">Dæmi 3: Vextir eftir afmörkun = mánuðir</span><span class="sxs-lookup"><span data-stu-id="ecf2c-190">Example 3: Interest by range = Months</span></span>

<span data-ttu-id="ecf2c-191">Hægt er að setja upp vaxtakóðann sem metur vexti einu sinni fyrir hvern mánuð sem reikningurinn er umfram gjalddaga færslunnar.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-191">You set up an interest code that assesses interest one time for every month that the invoice payment exceeds the transaction due date.</span></span> <span data-ttu-id="ecf2c-192">Óskað er eftir að byggja útreikning á prósentugildi vaxta, samkvæmt skrefskiptum mánaðarbilum.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-192">You want to base the calculation on a percentage interest value, according to stepped month intervals.</span></span> <span data-ttu-id="ecf2c-193">Vaxta gildi verður 1,5 prósent hvern mánuð fyrir fyrstu þrjá gjaldfallna mánuðina, 2,0 prósent fyrir næstu þrjá mánuði og 2,5 prósent á mánuði fyrir hvern mánuð umfram fyrstu sex mánuði.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-193">The interest value will be 1.5 percent per month for the first three overdue months, 2.0 percent per month for the second three months, and 2.5 percent per month for each month beyond the first six months.</span></span> <span data-ttu-id="ecf2c-194">Gildi svæða fyrir vaxtakóða eru sett upp á eftirfarandi hátt.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-194">You set up the interest code field values as follows.</span></span>

| <span data-ttu-id="ecf2c-195">**Nafn svæðis**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-195">**Field name**</span></span>                  | <span data-ttu-id="ecf2c-196">**Svæðisgildi**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-196">**Field value**</span></span> |
|---------------------------------|-----------------|
| <span data-ttu-id="ecf2c-197">**Vaxtakóði**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-197">**Interest code**</span></span>               | <span data-ttu-id="ecf2c-198">1M%ByMth</span><span class="sxs-lookup"><span data-stu-id="ecf2c-198">1M%ByMth</span></span>        |
| <span data-ttu-id="ecf2c-199">**Reikna vexti hverja**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-199">**Calculate interest every**</span></span>    | <span data-ttu-id="ecf2c-200">1/mánuður</span><span class="sxs-lookup"><span data-stu-id="ecf2c-200">1/Month</span></span>         |
| <span data-ttu-id="ecf2c-201">**Vextir eftir afmörkun**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-201">**Interest by range**</span></span>           | <span data-ttu-id="ecf2c-202">Mánuðir</span><span class="sxs-lookup"><span data-stu-id="ecf2c-202">Months</span></span>          |
| <span data-ttu-id="ecf2c-203">**Reikna vexti út frá**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-203">**Calculate interest based on**</span></span> | <span data-ttu-id="ecf2c-204">Prósenta</span><span class="sxs-lookup"><span data-stu-id="ecf2c-204">Percentage</span></span>      |

<span data-ttu-id="ecf2c-205">Settar eru upp upplýsingar um afmörkun sem hér segir.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-205">You set up the range information as follows.</span></span>

| <span data-ttu-id="ecf2c-206">**Frá gildi**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-206">**From value**</span></span> | <span data-ttu-id="ecf2c-207">**Vaxtagildi**</span><span class="sxs-lookup"><span data-stu-id="ecf2c-207">**Interest value**</span></span> |
|----------------|--------------------|
| <span data-ttu-id="ecf2c-208">0</span><span class="sxs-lookup"><span data-stu-id="ecf2c-208">0</span></span>              | <span data-ttu-id="ecf2c-209">1.5</span><span class="sxs-lookup"><span data-stu-id="ecf2c-209">1.5</span></span>                |
| <span data-ttu-id="ecf2c-210">4</span><span class="sxs-lookup"><span data-stu-id="ecf2c-210">4</span></span>              | <span data-ttu-id="ecf2c-211">2</span><span class="sxs-lookup"><span data-stu-id="ecf2c-211">2</span></span>                  |
| <span data-ttu-id="ecf2c-212">7</span><span class="sxs-lookup"><span data-stu-id="ecf2c-212">7</span></span>              | <span data-ttu-id="ecf2c-213">2,5</span><span class="sxs-lookup"><span data-stu-id="ecf2c-213">2.5</span></span>                |

## <a name="new-versions"></a><span data-ttu-id="ecf2c-214">Nýjar útgáfur</span><span class="sxs-lookup"><span data-stu-id="ecf2c-214">New versions</span></span>
<span data-ttu-id="ecf2c-215">Vaxtakóðar eru gildir eftir dagsetningum.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-215">Interest codes are date effective.</span></span> <span data-ttu-id="ecf2c-216">Ef þú vilt breyta vöxtum, geturðu stofnað **nýja útgáfu** sem tekur gildi frá og með framtíðardagsetningu.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-216">If you want to modify the interest rate, you can create a **new version** that is effective as of a future date.</span></span>

<span data-ttu-id="ecf2c-217">Til að skoða mismunandi útgáfur er hægt að nota í **frá og með** val til að velja lokadagsetninguna.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-217">To view different versions, you can use the **As of Date** menu choice to select the cutoff date.</span></span> <span data-ttu-id="ecf2c-218">Einnig er hægt að velja **Birta allar færslur** til að skoða allar vaxtakóðum á síðunni.</span><span class="sxs-lookup"><span data-stu-id="ecf2c-218">You can also select the **Display all records** to view all interest codes in the page.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
