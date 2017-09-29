---
title: "Afskriftir fyrir 175% bókfært virði"
description: "Þessi grein gefur yfirlit yfir afskriftaraðferðina 175 prósent bókfært virði."
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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 318e111f784157666c2853bcd6d5b3af2c9ffdc5
ms.contentlocale: is-is
ms.lasthandoff: 08/29/2017

---

# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="a1926-103">Afskriftir fyrir 175% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a1926-103">175 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="a1926-104">Þessi grein gefur yfirlit yfir afskriftaraðferðina 175 prósent bókfært virði.</span><span class="sxs-lookup"><span data-stu-id="a1926-104">This article gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="a1926-105">Þegar afskriftaregla fyrir eignir er sett upp og gildið **175% bókfært virði** í reitnum **Aðferð** reitnum á **Afskriftarreglur** síðunni eru eignir sem er úthlutað á þessa afskriftareglu afskrifaðar með sömu prósentu á hverju afskriftatímabili.</span><span class="sxs-lookup"><span data-stu-id="a1926-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="a1926-106">Til að setja upp afskriftir fyrir 175% bókfært virði, verður einnig að velja valkosti í á **afskriftarár** svæði og **tímabilstíðni** á í **afskriftareglur** síðu.</span><span class="sxs-lookup"><span data-stu-id="a1926-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="a1926-107">Valkostirnir sem eru tiltækir á svæðinu**tímabilstíðni** eru mismunandi eftir því sem valið er á svæðinu **afskriftarár**.</span><span class="sxs-lookup"><span data-stu-id="a1926-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="a1926-108">Velja afskriftaár</span><span class="sxs-lookup"><span data-stu-id="a1926-108">Select a depreciation year</span></span>
<span data-ttu-id="a1926-109">Hægt er að velja annað hvort **Dagatal** eða **reikningsár** í svæðinu **afskriftarár** á **afskriftareglu** síðunni.</span><span class="sxs-lookup"><span data-stu-id="a1926-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="a1926-110">Sjálfgefið gildi er **Dagatal**.</span><span class="sxs-lookup"><span data-stu-id="a1926-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="a1926-111">Valið skilgreinir valmöguleikana sem í boði eru á svæðinu **tímabilstíðni**.</span><span class="sxs-lookup"><span data-stu-id="a1926-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="a1926-112">Þetta svæði skilgreinir bókunardagsetningar uppsafnaðra afskrifta og magn þeirra yfir almanaksárið.</span><span class="sxs-lookup"><span data-stu-id="a1926-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="a1926-113">Dagatal</span><span class="sxs-lookup"><span data-stu-id="a1926-113">Calendar</span></span>

<span data-ttu-id="a1926-114">Það er hægt að velja að halda sjálfgefnum gildum í svæðinu **afskriftarár,****dagatal**.</span><span class="sxs-lookup"><span data-stu-id="a1926-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="a1926-115">**Dagatal** uppfærir afskriftargrundvöllinn 1. Janúar ár hvert.</span><span class="sxs-lookup"><span data-stu-id="a1926-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="a1926-116">Yfirleitt er afskriftagrundvöllurinn bókað nettóvirði mínus hrakvirði.</span><span class="sxs-lookup"><span data-stu-id="a1926-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="a1926-117">Í dæmunum hér að neðan er afskriftagrunnurinn deilistofninn í fyrstu segðinni í útreikningum í útreikningsdálkinum.</span><span class="sxs-lookup"><span data-stu-id="a1926-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="a1926-118">Ef valið er **Dagatal** sem afskriftaár eru eftirfarandi valkostir tiltækir á svæðinu **tímabilstíðni**:</span><span class="sxs-lookup"><span data-stu-id="a1926-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="a1926-119">**Árleg** upphæð bókar 31. Desember.</span><span class="sxs-lookup"><span data-stu-id="a1926-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="a1926-120">**Mánaðarlega**bókar mánaðarlega upphæð við lok hvers almanaks mánaðar.</span><span class="sxs-lookup"><span data-stu-id="a1926-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="a1926-121">**Ársfjórðungslega**bókar upphæð ársfjórðungslega við lok hvers almanaksfjórðungs (31. mars, 30. júní, 30. september og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="a1926-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="a1926-122">**Tvisvar á ári**bókar upphæð á hálfs árs fresti miðað við hálft almanaksár (30. júní og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="a1926-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="a1926-123">Með **Daglega** er afskriftarupphæð fyrir afskriftaraðferðina daglega bókuð með einni færslu daglega.</span><span class="sxs-lookup"><span data-stu-id="a1926-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="a1926-124">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="a1926-124">Fiscal</span></span>

<span data-ttu-id="a1926-125">Ef valið er **Fjárhagsárs** á svæðinu **Afskriftarár** er 175% afskrift af bókfærðu virði reiknað á grundvelli fjárhagsárs fyrir fjárhagsdagatalið sem tilgreint er fyrir bókina eða fyrir fjárhagsdagatalið sem valin er á síðunni **Fjárhagur**.</span><span class="sxs-lookup"><span data-stu-id="a1926-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="a1926-126">Fjárhagsdagatöl eru sett upp á síðunni **fjárhagsdagatöl**.</span><span class="sxs-lookup"><span data-stu-id="a1926-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="a1926-127">Fyrir nánari upplýsingar, sjá [járhagsdagatöl, fjárhagsár, og tímabil.](..\budgeting\fiscal-calendars-fiscal-years-periods.md)</span><span class="sxs-lookup"><span data-stu-id="a1926-127">For more information, see [Fiscal calendars, fiscal years, and periods.](..\budgeting\fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="a1926-128">Fyrir fjárhagsárið 1. júlí til 30. júní, byrjar útreikningur afskrifta til dæmis þann 1. júlí.</span><span class="sxs-lookup"><span data-stu-id="a1926-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="a1926-129">Fjárhagsár getur verið lengra eða styttra en 12 mánuðir.</span><span class="sxs-lookup"><span data-stu-id="a1926-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="a1926-130">Afskriftirnar eru leiðréttar sjálfkrafa fyrir hvert tímabil og lengd næsta fjárhagsárs ákvarðast af uppsetningu tímabila á síðunni **Fjárhagsdagatöl**.</span><span class="sxs-lookup"><span data-stu-id="a1926-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="a1926-131">Ef **reikningsár** er valið sem afskriftaár eru eftirfarandi valkostir tiltækir í svæðinu **tímabilstíðni**:</span><span class="sxs-lookup"><span data-stu-id="a1926-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="a1926-132">**Árlega** bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið sem eina upphæð á síðasta degi fjárhagsársins.</span><span class="sxs-lookup"><span data-stu-id="a1926-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="a1926-133">**Fjárhagstímabil** reiknar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið.</span><span class="sxs-lookup"><span data-stu-id="a1926-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="a1926-134">Þessari upphæð er safnað upp í fjárhagstímabilin sem skilgreind eru á síðunni**fjárhagsdagatöl**.</span><span class="sxs-lookup"><span data-stu-id="a1926-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="a1926-135">Dæmi um afskriftir fyrir 175% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="a1926-135">Example of 175% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="a1926-136">Kaupverð</span><span class="sxs-lookup"><span data-stu-id="a1926-136">Acquisition cost</span></span>               | <span data-ttu-id="a1926-137">11.000</span><span class="sxs-lookup"><span data-stu-id="a1926-137">11,000</span></span> |
| <span data-ttu-id="a1926-138">Hrakvirði</span><span class="sxs-lookup"><span data-stu-id="a1926-138">Salvage value</span></span>                  | <span data-ttu-id="a1926-139">1.000</span><span class="sxs-lookup"><span data-stu-id="a1926-139">1,000</span></span>  |
| <span data-ttu-id="a1926-140">Afskriftargrundvöllur</span><span class="sxs-lookup"><span data-stu-id="a1926-140">Depreciation base</span></span>              | <span data-ttu-id="a1926-141">10.000</span><span class="sxs-lookup"><span data-stu-id="a1926-141">10,000</span></span> |
| <span data-ttu-id="a1926-142">Líftími í árum</span><span class="sxs-lookup"><span data-stu-id="a1926-142">Service life years</span></span>             | <span data-ttu-id="a1926-143">5</span><span class="sxs-lookup"><span data-stu-id="a1926-143">5</span></span>      |
| <span data-ttu-id="a1926-144">Föst árleg afskriftaprósenta</span><span class="sxs-lookup"><span data-stu-id="a1926-144">Yearly depreciation percentage</span></span> | <span data-ttu-id="a1926-145">35%</span><span class="sxs-lookup"><span data-stu-id="a1926-145">35%</span></span>    |

<span data-ttu-id="a1926-146">Aðferðin afskriftir fyrir 175% bókfært virði stöðu deilir 175% með líftíma í árum.</span><span class="sxs-lookup"><span data-stu-id="a1926-146">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="a1926-147">Það hlutfall af hundraði er margfaldað með bókuðu nettóvirði eignarinnar til að ákvarða afskriftarupphæð ársins.</span><span class="sxs-lookup"><span data-stu-id="a1926-147">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="a1926-148">Tímabil</span><span class="sxs-lookup"><span data-stu-id="a1926-148">Period</span></span> | <span data-ttu-id="a1926-149">Reiknuð upphæð árlegra afskrifta</span><span class="sxs-lookup"><span data-stu-id="a1926-149">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="a1926-150">Bókfært verð</span><span class="sxs-lookup"><span data-stu-id="a1926-150">Book value</span></span>                  | <span data-ttu-id="a1926-151">Nettó bókfært verð við lok árs</span><span class="sxs-lookup"><span data-stu-id="a1926-151">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="a1926-152">1. ár</span><span class="sxs-lookup"><span data-stu-id="a1926-152">Year 1</span></span> | <span data-ttu-id="a1926-153">(11,000 – 1,000) × 35% = 3,500</span><span class="sxs-lookup"><span data-stu-id="a1926-153">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="a1926-154">11.000 – 3.500 = 7.500</span><span class="sxs-lookup"><span data-stu-id="a1926-154">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="a1926-155">11.000 – 1.000 – 3.500 = 6.500</span><span class="sxs-lookup"><span data-stu-id="a1926-155">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="a1926-156">2. ár</span><span class="sxs-lookup"><span data-stu-id="a1926-156">Year 2</span></span> | <span data-ttu-id="a1926-157">6,500 × 35% = 2,275</span><span class="sxs-lookup"><span data-stu-id="a1926-157">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="a1926-158">7,500 – 2,275 = 5,225</span><span class="sxs-lookup"><span data-stu-id="a1926-158">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="a1926-159">6,500 – 2,275 = 4,225</span><span class="sxs-lookup"><span data-stu-id="a1926-159">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="a1926-160">3. ár</span><span class="sxs-lookup"><span data-stu-id="a1926-160">Year 3</span></span> | <span data-ttu-id="a1926-161">4,225 × 35% = 1,478.75</span><span class="sxs-lookup"><span data-stu-id="a1926-161">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="a1926-162">5.225 – 1.478,75 = 3.746,25</span><span class="sxs-lookup"><span data-stu-id="a1926-162">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="a1926-163">4,225 – 1,478.75 = 2,746.25</span><span class="sxs-lookup"><span data-stu-id="a1926-163">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="a1926-164">Yfirleitt þegar upphæðin sem er reiknuð með því að nota 175% bókfært virði verður afskriftaraðferð lægri en upphæðin sem yrði reiknuð með því að nota línulega afskriftaaðferð er umbreyting yfir í línulega aðferð fyrir eftirstandandi líftíma.</span><span class="sxs-lookup"><span data-stu-id="a1926-164">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




