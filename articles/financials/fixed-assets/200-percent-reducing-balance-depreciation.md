---
title: "Afskriftir fyrir 200% bókfært virði"
description: "Þessi grein gefur yfirlit yfir afskriftaraðferðina 200 prósent bókfært virði."
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
ms.custom: 13951
ms.assetid: 69b4e010-7683-4dc2-8a06-6d572f37e903
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 46afd002a370a43c9e1d2fb7cc5e61ece9033be9
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="200-percent-reducing-balance-depreciation"></a><span data-ttu-id="4e074-103">Afskriftir fyrir 200% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="4e074-103">200 percent reducing balance depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="4e074-104">Þessi grein gefur yfirlit yfir afskriftaraðferðina 200 prósent bókfært virði.</span><span class="sxs-lookup"><span data-stu-id="4e074-104">This article gives an overview of the 200 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="4e074-105">Þegar afskriftarregla fyrir eignir er sett upp og gildið **200% bókfært virði** er valið í reitnum **Aðferð** á **Afskriftarreglur** eru eignaafskriftir, sem eru tengdar þessari afskriftareglu, með sama hlutfall af hundraði á hverju afskriftatímabili.</span><span class="sxs-lookup"><span data-stu-id="4e074-105">When you set up a fixed asset depreciation profile and select **200% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="4e074-106">Þessi prósenta er byggist á líftíma eignarinnar.</span><span class="sxs-lookup"><span data-stu-id="4e074-106">The percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="4e074-107">Til dæmis, ef eign er með líftíma fimm ár, er prósenta reiknuð sem 40 prósent (200% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="4e074-107">For example, if an asset has a service life of five years, the percentage is calculated as 40 percent (200% ÷ 5).</span></span> 

<span data-ttu-id="4e074-108">Þessi aðferð er einnig þekkt sem stiglækkandi afskrift .</span><span class="sxs-lookup"><span data-stu-id="4e074-108">This method is also known as double declining balance.</span></span>

<span data-ttu-id="4e074-109">Til að setja upp afskriftir fyrir 200% bókfært virði, verður einnig að velja valkosti á svæðinu **Afskriftarár** og á svæðinu **Tímabilstíðni** á síðunni **Afskriftareglur** síðu.</span><span class="sxs-lookup"><span data-stu-id="4e074-109">To set up 200% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="4e074-110">Valkostirnir sem eru tiltækar á svæðinu **Tímabilstíðni** eru mismunandi eftir því gildi sem valið er á svæðinu **Afskriftarár**.</span><span class="sxs-lookup"><span data-stu-id="4e074-110">The options that are available in the **Period frequency** field vary, depending on the value that you select in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="4e074-111">Velja afskriftaár</span><span class="sxs-lookup"><span data-stu-id="4e074-111">Select a depreciation year</span></span>
<span data-ttu-id="4e074-112">Hægt er að velja annað hvort **Dagatal** eða **reikningsár** í svæðinu **afskriftarár** á **afskriftareglu** síðunni.</span><span class="sxs-lookup"><span data-stu-id="4e074-112">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="4e074-113">Sjálfgefið gildi er **Dagatal**.</span><span class="sxs-lookup"><span data-stu-id="4e074-113">The default value is **Calendar**.</span></span> 

<span data-ttu-id="4e074-114">Valið skilgreinir valmöguleikana sem í boði eru á svæðinu **tímabilstíðni**.</span><span class="sxs-lookup"><span data-stu-id="4e074-114">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="4e074-115">Þetta svæði skilgreinir bókunardagsetningar uppsafnaðra afskrifta og magn þeirra yfir almanaksárið.</span><span class="sxs-lookup"><span data-stu-id="4e074-115">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="4e074-116">Dagatal</span><span class="sxs-lookup"><span data-stu-id="4e074-116">Calendar</span></span>

<span data-ttu-id="4e074-117">Það er hægt að velja að halda sjálfgefnum gildum í svæðinu **afskriftarár,****dagatal**.</span><span class="sxs-lookup"><span data-stu-id="4e074-117">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="4e074-118">**Dagatal** uppfærir afskriftargrundvöllinn 1. Janúar ár hvert.</span><span class="sxs-lookup"><span data-stu-id="4e074-118">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="4e074-119">Yfirleitt eru afskriftir bókað nettóvirði mínus hrakvirði.</span><span class="sxs-lookup"><span data-stu-id="4e074-119">Typically, the depreciation is the net book value minus the scrap value.</span></span> <span data-ttu-id="4e074-120">Í dæmunum hér að neðan er afskriftagrunnurinn deilistofninn í fyrstu segðinni í útreikningum í útreikningsdálkinum.</span><span class="sxs-lookup"><span data-stu-id="4e074-120">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="4e074-121">Ef valið er **Dagatal** sem afskriftaár eru eftirfarandi valkostir tiltækir á svæðinu **tímabilstíðni**:</span><span class="sxs-lookup"><span data-stu-id="4e074-121">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="4e074-122">**Árleg** upphæð bókar 31. Desember.</span><span class="sxs-lookup"><span data-stu-id="4e074-122">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="4e074-123">**Mánaðarlega**bókar mánaðarlega upphæð við lok hvers almanaks mánaðar.</span><span class="sxs-lookup"><span data-stu-id="4e074-123">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="4e074-124">**Ársfjórðungslega**bókar upphæð ársfjórðungslega við lok hvers almanaksfjórðungs (31. mars, 30. júní, 30. september og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="4e074-124">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="4e074-125">**Tvisvar á ári**bókar upphæð á hálfs árs fresti miðað við hálft almanaksár (30. júní og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="4e074-125">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="4e074-126">Með **Daglega** er afskriftarupphæð fyrir afskriftaraðferðina daglega bókuð með einni færslu daglega.</span><span class="sxs-lookup"><span data-stu-id="4e074-126">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="4e074-127">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="4e074-127">Fiscal</span></span>

<span data-ttu-id="4e074-128">Ef valið er **Fjárhagsárs** á svæðinu **Afskriftarár** er 200% afskrift af bókfærðu virði reiknað á grundvelli fjárhagsárs fyrir fjárhagsdagatalið sem tilgreint er fyrir bókina eða fyrir fjárhagsdagatalið sem valin er á síðunni **Fjárhagur**.</span><span class="sxs-lookup"><span data-stu-id="4e074-128">If you select **Fiscal** in the **Depreciation** year field, 200% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="4e074-129">Fjárhagsdagatöl eru sett upp á síðunni **fjárhagsdagatöl**.</span><span class="sxs-lookup"><span data-stu-id="4e074-129">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="4e074-130">Fyrir fjárhagsárið 1. júlí til 30. júní, byrjar útreikningur afskrifta til dæmis þann 1. júlí.</span><span class="sxs-lookup"><span data-stu-id="4e074-130">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="4e074-131">Fjárhagsár getur verið lengra eða styttra en 12 mánuðir.</span><span class="sxs-lookup"><span data-stu-id="4e074-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="4e074-132">Afskriftirnar eru leiðréttar fyrir hvert tímabil.</span><span class="sxs-lookup"><span data-stu-id="4e074-132">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="4e074-133">Lengd næsta fjárhagsárs ákvarðast af uppsetning tímabila á síðunni**fjárhagsdagatöl**.</span><span class="sxs-lookup"><span data-stu-id="4e074-133">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="4e074-134">Ef **Fjárhags** er valið sem afskriftaár eru eftirfarandi valkostir tiltækir á svæðinu **Tímabilstíðni**:</span><span class="sxs-lookup"><span data-stu-id="4e074-134">When **Fiscal** is selected as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="4e074-135">**Árlega**bókar heildarupphæð reiknaðra afskrifta°fyrir fjárhagsárið sem eina upphæð á síðasta degi fjárhagsársins.</span><span class="sxs-lookup"><span data-stu-id="4e074-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="4e074-136">**Reikningstímabil** bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið.</span><span class="sxs-lookup"><span data-stu-id="4e074-136">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="4e074-137">Þessari upphæð er safnað upp í fjárhagstímabilin sem skilgreind eru á síðunni**fjárhagsdagatöl**.</span><span class="sxs-lookup"><span data-stu-id="4e074-137">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-200-reducing-balance-depreciation"></a><span data-ttu-id="4e074-138">Dæmi um afskriftir fyrir 200% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="4e074-138">Example of 200% reducing balance depreciation</span></span>
|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="4e074-139">Kaupverð</span><span class="sxs-lookup"><span data-stu-id="4e074-139">Acquisition cost</span></span>               | <span data-ttu-id="4e074-140">11.000</span><span class="sxs-lookup"><span data-stu-id="4e074-140">11,000</span></span> |
| <span data-ttu-id="4e074-141">Hrakvirði</span><span class="sxs-lookup"><span data-stu-id="4e074-141">Salvage value</span></span>                  | <span data-ttu-id="4e074-142">1, 000</span><span class="sxs-lookup"><span data-stu-id="4e074-142">1, 000</span></span> |
| <span data-ttu-id="4e074-143">Afskriftargrundvöllur</span><span class="sxs-lookup"><span data-stu-id="4e074-143">Depreciation base</span></span>              | <span data-ttu-id="4e074-144">10.000</span><span class="sxs-lookup"><span data-stu-id="4e074-144">10,000</span></span> |
| <span data-ttu-id="4e074-145">Líftími í árum</span><span class="sxs-lookup"><span data-stu-id="4e074-145">Service life years</span></span>             | <span data-ttu-id="4e074-146">5</span><span class="sxs-lookup"><span data-stu-id="4e074-146">5</span></span>      |
| <span data-ttu-id="4e074-147">Föst árleg afskriftaprósenta</span><span class="sxs-lookup"><span data-stu-id="4e074-147">Yearly depreciation percentage</span></span> | <span data-ttu-id="4e074-148">40%</span><span class="sxs-lookup"><span data-stu-id="4e074-148">40%</span></span>    |

<span data-ttu-id="4e074-149">Afskriftir fyrir 200% bókfært virði stöðu aðferð deilir 200% með líftíma í árum.</span><span class="sxs-lookup"><span data-stu-id="4e074-149">The 200% reducing balance method divides 200 percent by the service life years.</span></span> <span data-ttu-id="4e074-150">Það hlutfall af hundraði er margfaldað með bókuðu nettóvirði eignarinnar til að ákvarða afskriftarupphæð ársins.</span><span class="sxs-lookup"><span data-stu-id="4e074-150">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="4e074-151">Tímabil</span><span class="sxs-lookup"><span data-stu-id="4e074-151">Period</span></span> | <span data-ttu-id="4e074-152">Reiknuð upphæð árlegra afskrifta</span><span class="sxs-lookup"><span data-stu-id="4e074-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="4e074-153">Bókfært verð</span><span class="sxs-lookup"><span data-stu-id="4e074-153">Book value</span></span>             | <span data-ttu-id="4e074-154">Nettó bókfært verð við lok árs</span><span class="sxs-lookup"><span data-stu-id="4e074-154">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="4e074-155">1. ár</span><span class="sxs-lookup"><span data-stu-id="4e074-155">Year 1</span></span> | <span data-ttu-id="4e074-156">(11.000 – 1.000) × 40% = 4.000</span><span class="sxs-lookup"><span data-stu-id="4e074-156">(11,000 – 1,000) × 40% = 4,000</span></span>                | <span data-ttu-id="4e074-157">11.000 – 4.000 = 7.000</span><span class="sxs-lookup"><span data-stu-id="4e074-157">11,000 – 4,000 = 7,000</span></span> | <span data-ttu-id="4e074-158">11.000 – 1.000 – 4.000 = 6.000</span><span class="sxs-lookup"><span data-stu-id="4e074-158">11,000 – 1,000 – 4,000 = 6,000</span></span>        |
| <span data-ttu-id="4e074-159">2. ár</span><span class="sxs-lookup"><span data-stu-id="4e074-159">Year 2</span></span> | <span data-ttu-id="4e074-160">6.000 × 40% = 2.,400</span><span class="sxs-lookup"><span data-stu-id="4e074-160">6,000 × 40% = 2,400</span></span>                           | <span data-ttu-id="4e074-161">7.000 – 2.400 = 4.600</span><span class="sxs-lookup"><span data-stu-id="4e074-161">7,000 – 2,400 = 4,600</span></span>  | <span data-ttu-id="4e074-162">6.000 – 2.400 = 3.600</span><span class="sxs-lookup"><span data-stu-id="4e074-162">6,000 – 2,400 = 3,600</span></span>                 |
| <span data-ttu-id="4e074-163">3. ár</span><span class="sxs-lookup"><span data-stu-id="4e074-163">Year 3</span></span> | <span data-ttu-id="4e074-164">3.600 × 40% = 1.440</span><span class="sxs-lookup"><span data-stu-id="4e074-164">3,600 × 40% = 1,440</span></span>                           | <span data-ttu-id="4e074-165">4.600 – 1.440 = 3.160</span><span class="sxs-lookup"><span data-stu-id="4e074-165">4,600 – 1,440 = 3,160</span></span>  | <span data-ttu-id="4e074-166">3.600 – 1.440 = 2.160</span><span class="sxs-lookup"><span data-stu-id="4e074-166">3,600 – 1,440 = 2,160</span></span>                 |

> [!NOTE] 
> <span data-ttu-id="4e074-167">Yfirleitt þegar upphæðin sem er reiknuð með því að nota 200% bókfært virði verður afskriftaraðferð lægri en upphæðin sem yrði reiknuð með því að nota línulega afskriftaaðferð er umbreyting yfir í línulega aðferð fyrir eftirstandandi líftíma.</span><span class="sxs-lookup"><span data-stu-id="4e074-167">Typically, when the amount that is calculated by using the 200% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>




