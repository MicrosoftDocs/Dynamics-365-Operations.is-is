---
title: "Afskriftir fyrir 125% bókfært virði"
description: "Þessi grein gefur yfirlit yfir afskriftaraðferðina 125 prósent bókfært virði."
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 13871
ms.assetid: 3abc263e-59d6-4f1a-986d-1be388948bd3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8ec88d799c44e035b6490861383557f8c3beda41
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="125-percent-reducing-balance-depreciation"></a><span data-ttu-id="80a9b-103">Afskriftir fyrir 125% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="80a9b-103">125 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="80a9b-104">Þessi grein gefur yfirlit yfir afskriftaraðferðina 125 prósent bókfært virði.</span><span class="sxs-lookup"><span data-stu-id="80a9b-104">This article gives an overview of the 125 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="80a9b-105">Þegar afskriftaregla fyrir eignir er sett upp og valið er **125% bókfært virði** í skjámyndinni **Aðferð** á síðunni **Afskriftarreglur**eru eignir sem eru tengdar þessari afskriftareglu, afskrifaðar með sama hlutfall af hundraði á hverju afskriftatímabili.</span><span class="sxs-lookup"><span data-stu-id="80a9b-105">When you set up a fixed asset depreciation profile and select **125% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned to the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="80a9b-106">Þessi prósenta er reiknuð á grundvelli líftíma eignarinnar.</span><span class="sxs-lookup"><span data-stu-id="80a9b-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="80a9b-107">Til dæmis, ef eign hefur líftímann fimm ár, er prósentan reiknuð sem 25 prósent°(125% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="80a9b-107">For example, if an asset has a service life of five years, the percentage is calculated as 25 percent (125% ÷ 5).</span></span>

<span data-ttu-id="80a9b-108">Til að setja upp afskriftir fyrir 125% bókfært virði, verður einnig að velja valkosti á svæðinu **Afskriftarár** og svæðið **Tímabilstíðni** á síðunni **Afskriftareglur**.</span><span class="sxs-lookup"><span data-stu-id="80a9b-108">To set up 125% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="80a9b-109">Valkostirnir sem eru tiltækir á svæðinu**tímabilstíðni** eru mismunandi eftir því sem valið er á svæðinu **afskriftarár**.</span><span class="sxs-lookup"><span data-stu-id="80a9b-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="80a9b-110">Velja afskriftaár</span><span class="sxs-lookup"><span data-stu-id="80a9b-110">Select a depreciation year</span></span>
<span data-ttu-id="80a9b-111">Hægt er að velja annað hvort **Dagatal** eða **reikningsár** í svæðinu **afskriftarár** á **afskriftareglu** síðunni.</span><span class="sxs-lookup"><span data-stu-id="80a9b-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="80a9b-112">Sjálfgefið gildi er **Dagatal**.</span><span class="sxs-lookup"><span data-stu-id="80a9b-112">The default value is **Calendar**.</span></span> 

<span data-ttu-id="80a9b-113">Valið skilgreinir valmöguleikana sem í boði eru á svæðinu **tímabilstíðni**.</span><span class="sxs-lookup"><span data-stu-id="80a9b-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="80a9b-114">Þetta svæði skilgreinir bókunardagsetningar uppsafnaðra afskrifta og magn þeirra yfir almanaksárið.</span><span class="sxs-lookup"><span data-stu-id="80a9b-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="80a9b-115">Dagatal</span><span class="sxs-lookup"><span data-stu-id="80a9b-115">Calendar</span></span>

<span data-ttu-id="80a9b-116">Það er hægt að velja að halda sjálfgefnum gildum í svæðinu **afskriftarár,****dagatal**.</span><span class="sxs-lookup"><span data-stu-id="80a9b-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="80a9b-117">**Dagatal** uppfærir afskriftargrundvöllinn 1. Janúar ár hvert.</span><span class="sxs-lookup"><span data-stu-id="80a9b-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="80a9b-118">Yfirleitt er afskriftagrundvöllurinn bókað nettóvirði mínus hrakvirði.</span><span class="sxs-lookup"><span data-stu-id="80a9b-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="80a9b-119">Í dæmunum hér að neðan er afskriftagrunnurinn deilistofninn í fyrstu segðinni í útreikningum í útreikningsdálkinum.</span><span class="sxs-lookup"><span data-stu-id="80a9b-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="80a9b-120">Ef valið er **Dagatal** sem afskriftaár eru eftirfarandi valkostir tiltækir á svæðinu **tímabilstíðni**:</span><span class="sxs-lookup"><span data-stu-id="80a9b-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="80a9b-121">**Árleg** upphæð bókar 31. Desember.</span><span class="sxs-lookup"><span data-stu-id="80a9b-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="80a9b-122">**Mánaðarlega**bókar mánaðarlega upphæð við lok hvers almanaks mánaðar.</span><span class="sxs-lookup"><span data-stu-id="80a9b-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="80a9b-123">**Ársfjórðungslega**bókar upphæð ársfjórðungslega við lok hvers almanaksfjórðungs (31. mars, 30. júní, 30. september og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="80a9b-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="80a9b-124">**Tvisvar á ári**bókar upphæð á hálfs árs fresti miðað við hálft almanaksár (30. júní og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="80a9b-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="80a9b-125">Með **Daglega** er afskriftarupphæð fyrir afskriftaraðferðina daglega bókuð með einni færslu daglega.</span><span class="sxs-lookup"><span data-stu-id="80a9b-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="80a9b-126">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="80a9b-126">Fiscal</span></span>

<span data-ttu-id="80a9b-127">Ef valið er **Fjárhagsárs** á svæðinu **Afskriftarár** er 125% afskrift af bókfærðu virði reiknað á grundvelli fjárhagsárs fyrir fjárhagsdagatalið sem tilgreint er fyrir bókina eða fyrir fjárhagsdagatalið sem valin er á síðunni **Fjárhagur**.</span><span class="sxs-lookup"><span data-stu-id="80a9b-127">If you select **Fiscal** in the **Depreciation year** field, 125% reducing depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="80a9b-128">Fjárhagsdagatöl eru sett upp á síðunni **fjárhagsdagatöl**.</span><span class="sxs-lookup"><span data-stu-id="80a9b-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="80a9b-129">Fyrir fjárhagsárið 1. júlí til 30. júní, byrjar útreikningur afskrifta til dæmis þann 1. júlí.</span><span class="sxs-lookup"><span data-stu-id="80a9b-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="80a9b-130">Fjárhagsár getur verið lengra eða styttra en 12 mánuðir.</span><span class="sxs-lookup"><span data-stu-id="80a9b-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="80a9b-131">Afskriftirnar eru leiðréttar sjálfkrafa fyrir hvert tímabil og lengd næsta fjárhagsárs ákvarðast af uppsetningu tímabila á síðunni **Fjárhagsdagatöl**.</span><span class="sxs-lookup"><span data-stu-id="80a9b-131">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="80a9b-132">Ef **reikningsár** er valið sem afskriftaár eru eftirfarandi valkostir tiltækir í svæðinu **tímabilstíðni**:</span><span class="sxs-lookup"><span data-stu-id="80a9b-132">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="80a9b-133">**Árlega**bókar heildarupphæð reiknaðra afskrifta°fyrir fjárhagsárið sem eina upphæð á síðasta degi fjárhagsársins.</span><span class="sxs-lookup"><span data-stu-id="80a9b-133">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="80a9b-134">**Reikningstímabil** bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið.</span><span class="sxs-lookup"><span data-stu-id="80a9b-134">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="80a9b-135">Þessari upphæð er safnað upp í fjárhagstímabilin sem skilgreind eru á síðunni**fjárhagsdagatöl**.</span><span class="sxs-lookup"><span data-stu-id="80a9b-135">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-125-reducing-balance-depreciation"></a><span data-ttu-id="80a9b-136">Dæmi um afskriftir fyrir 125% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="80a9b-136">Example of 125% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="80a9b-137">Kaupverð</span><span class="sxs-lookup"><span data-stu-id="80a9b-137">Acquisition cost</span></span>               | <span data-ttu-id="80a9b-138">11.000</span><span class="sxs-lookup"><span data-stu-id="80a9b-138">11,000</span></span> |
| <span data-ttu-id="80a9b-139">Hrakvirði</span><span class="sxs-lookup"><span data-stu-id="80a9b-139">Salvage value</span></span>                  | <span data-ttu-id="80a9b-140">1.000</span><span class="sxs-lookup"><span data-stu-id="80a9b-140">1,000</span></span>  |
| <span data-ttu-id="80a9b-141">Afskriftargrundvöllur</span><span class="sxs-lookup"><span data-stu-id="80a9b-141">Depreciation base</span></span>              | <span data-ttu-id="80a9b-142">10.000</span><span class="sxs-lookup"><span data-stu-id="80a9b-142">10,000</span></span> |
| <span data-ttu-id="80a9b-143">Líftími í árum</span><span class="sxs-lookup"><span data-stu-id="80a9b-143">Service life years</span></span>             | <span data-ttu-id="80a9b-144">5</span><span class="sxs-lookup"><span data-stu-id="80a9b-144">5</span></span>      |
| <span data-ttu-id="80a9b-145">Föst árleg afskriftaprósenta</span><span class="sxs-lookup"><span data-stu-id="80a9b-145">Yearly depreciation percentage</span></span> | <span data-ttu-id="80a9b-146">25%</span><span class="sxs-lookup"><span data-stu-id="80a9b-146">25%</span></span>    |

<span data-ttu-id="80a9b-147">Aðferðin afskriftir fyrir 125% bókfært virði deilir 125% með líftíma í árum.</span><span class="sxs-lookup"><span data-stu-id="80a9b-147">The 125% reducing balance method divides 125 percent by the service life years.</span></span> <span data-ttu-id="80a9b-148">Það hlutfall af hundraði er margfaldað með bókuðu nettóvirði eignarinnar til að ákvarða afskriftarupphæð ársins.</span><span class="sxs-lookup"><span data-stu-id="80a9b-148">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="80a9b-149">Tímabil</span><span class="sxs-lookup"><span data-stu-id="80a9b-149">Period</span></span> | <span data-ttu-id="80a9b-150">Reiknuð upphæð árlegra afskrifta</span><span class="sxs-lookup"><span data-stu-id="80a9b-150">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="80a9b-151">Bókfært verð</span><span class="sxs-lookup"><span data-stu-id="80a9b-151">Book value</span></span>                    | <span data-ttu-id="80a9b-152">Nettó bókfært verð við lok árs</span><span class="sxs-lookup"><span data-stu-id="80a9b-152">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-------------------------------|---------------------------------------|
| <span data-ttu-id="80a9b-153">1. ár</span><span class="sxs-lookup"><span data-stu-id="80a9b-153">Year 1</span></span> | <span data-ttu-id="80a9b-154">(11.000 – 1.000) × 25% = 2.500</span><span class="sxs-lookup"><span data-stu-id="80a9b-154">(11,000 – 1,000) × 25% = 2,500</span></span>                | <span data-ttu-id="80a9b-155">(11.000 – 2.500) = 8.500</span><span class="sxs-lookup"><span data-stu-id="80a9b-155">(11,000 – 2,500) = 8,500</span></span>      | <span data-ttu-id="80a9b-156">(11.000 – 1.000 – 2.500) = 7.500</span><span class="sxs-lookup"><span data-stu-id="80a9b-156">(11,000 – 1,000 – 2,500) = 7,500</span></span>      |
| <span data-ttu-id="80a9b-157">2. ár</span><span class="sxs-lookup"><span data-stu-id="80a9b-157">Year 2</span></span> | <span data-ttu-id="80a9b-158">7.500 × 25% = 1.875</span><span class="sxs-lookup"><span data-stu-id="80a9b-158">7,500 × 25% = 1,875</span></span>                           | <span data-ttu-id="80a9b-159">(8.500 – 1.875) = 6.625</span><span class="sxs-lookup"><span data-stu-id="80a9b-159">(8,500 – 1,875) = 6,625</span></span>       | <span data-ttu-id="80a9b-160">(7.500 – 1.875) = 5.625</span><span class="sxs-lookup"><span data-stu-id="80a9b-160">(7,500 – 1,875) = 5,625</span></span>               |
| <span data-ttu-id="80a9b-161">3. ár</span><span class="sxs-lookup"><span data-stu-id="80a9b-161">Year 3</span></span> | <span data-ttu-id="80a9b-162">5.625 × 25% = 1.406,25</span><span class="sxs-lookup"><span data-stu-id="80a9b-162">5,625 × 25% = 1,406.25</span></span>                        | <span data-ttu-id="80a9b-163">(6.625 – 1.406.25) = 5.218.75</span><span class="sxs-lookup"><span data-stu-id="80a9b-163">(6,625 – 1,406.25) = 5,218.75</span></span> | <span data-ttu-id="80a9b-164">(5.625 – 1.406.25) = 4.218.75</span><span class="sxs-lookup"><span data-stu-id="80a9b-164">(5,625 – 1,406.25) = 4,218.75</span></span>         |

> [!NOTE] 
> <span data-ttu-id="80a9b-165">Yfirleitt þegar upphæðin sem er reiknuð með því að nota 125% bókfært virði verður afskriftaraðferð lægri en upphæðin sem yrði reiknuð með því að nota línulega afskriftaaðferð er umbreyting yfir í línulega aðferð fyrir eftirstandandi líftíma.</span><span class="sxs-lookup"><span data-stu-id="80a9b-165">Typically, when the amount that is calculated by using the 125% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




