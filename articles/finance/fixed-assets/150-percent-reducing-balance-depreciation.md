---
title: Afskriftir fyrir 150% bókfært virði
description: Þessi grein gefur yfirlit yfir afskriftaraðferðina 150 prósent bókfært virði.
author: saraschi2
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4edc868b76d466c41be8036b962730db90eeb68a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249438"
---
# <a name="150-percent-reducing-balance-depreciation"></a><span data-ttu-id="ce90d-103">Afskriftir fyrir 150% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="ce90d-103">150 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce90d-104">Þessi grein gefur yfirlit yfir afskriftaraðferðina 150 prósent bókfært virði.</span><span class="sxs-lookup"><span data-stu-id="ce90d-104">This article gives an overview of the 150 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="ce90d-105">Þegar afskriftaregla fyrir eignir er sett upp og gildið **150% af bókfærðu virði** er valið í reitnum **Aðferð** á skjámyndinni **Afskriftaraðferðir** eru eignaafskriftir, sem eru tengdar þessari afskriftareglu, með sama hlutfall af hundraði á hverju afskriftatímabili.</span><span class="sxs-lookup"><span data-stu-id="ce90d-105">When you set up a fixed asset depreciation profile and select **150% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> <span data-ttu-id="ce90d-106">Þessi prósenta er reiknuð á grundvelli líftíma eignarinnar.</span><span class="sxs-lookup"><span data-stu-id="ce90d-106">This percentage is calculated based on the service life of the asset.</span></span> <span data-ttu-id="ce90d-107">Til dæmis, ef eign hefur líftíminn fimm ár, er prósenta reiknuð sem 30 prósent (150% ÷ 5).</span><span class="sxs-lookup"><span data-stu-id="ce90d-107">For example, if an asset has a service life of five years, the percentage is calculated as 30 percent (150% ÷ 5).</span></span> 

<span data-ttu-id="ce90d-108">Til að setja upp afskriftir fyrir 150% bókfært virði, verður einnig að velja valkosti á svæðinu **afskriftarár** og **tímabilstíðni** á síðunni **afskriftareglur**.</span><span class="sxs-lookup"><span data-stu-id="ce90d-108">To set up 150% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="ce90d-109">Valkostirnir sem eru tiltækir í reitnum **Tímabilstíðni** eru mismunandi eftir því sem valið er í reitnum **Afskriftarár**.</span><span class="sxs-lookup"><span data-stu-id="ce90d-109">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="selection-of-depreciation-year"></a><span data-ttu-id="ce90d-110">Val afskriftarárs</span><span class="sxs-lookup"><span data-stu-id="ce90d-110">Selection of depreciation year</span></span>
<span data-ttu-id="ce90d-111">Hægt er að velja annað hvort **Dagatal** eða **reikningsár** í svæðinu **afskriftarár** á **afskriftareglu** síðunni.</span><span class="sxs-lookup"><span data-stu-id="ce90d-111">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> 

<span data-ttu-id="ce90d-112">Sjálfgefið gildi er **Dagatal**.</span><span class="sxs-lookup"><span data-stu-id="ce90d-112">The default value is **Calendar**.</span></span> <span data-ttu-id="ce90d-113">Valið skilgreinir valmöguleikana sem í boði eru á svæðinu **tímabilstíðni**.</span><span class="sxs-lookup"><span data-stu-id="ce90d-113">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="ce90d-114">Þetta svæði skilgreinir bókunardagsetningar uppsafnaðra afskrifta og magn þeirra yfir almanaksárið.</span><span class="sxs-lookup"><span data-stu-id="ce90d-114">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="ce90d-115">Dagatal</span><span class="sxs-lookup"><span data-stu-id="ce90d-115">Calendar</span></span>

<span data-ttu-id="ce90d-116">Hægt er að velja að halda sjálfgefnum gildum í reitnum **Afskriftarár**, **Dagatal**.</span><span class="sxs-lookup"><span data-stu-id="ce90d-116">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="ce90d-117">**Dagatal** uppfærir afskriftargrundvöllinn 1. Janúar ár hvert.</span><span class="sxs-lookup"><span data-stu-id="ce90d-117">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="ce90d-118">Yfirleitt er afskriftagrundvöllurinn bókað nettóvirði mínus hrakvirði.</span><span class="sxs-lookup"><span data-stu-id="ce90d-118">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="ce90d-119">Í dæmunum hér að neðan er afskriftagrunnurinn deilistofninn í fyrstu segðinni í útreikningum í útreikningsdálkinum.</span><span class="sxs-lookup"><span data-stu-id="ce90d-119">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="ce90d-120">Ef valið er **Dagatal** sem afskriftaár eru eftirfarandi valkostir tiltækir á svæðinu **tímabilstíðni**:</span><span class="sxs-lookup"><span data-stu-id="ce90d-120">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="ce90d-121">**Árleg** upphæð bókar 31. Desember.</span><span class="sxs-lookup"><span data-stu-id="ce90d-121">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="ce90d-122">**Mánaðarlega** bókar mánaðarlega upphæð við lok hvers almanaks mánaðar.</span><span class="sxs-lookup"><span data-stu-id="ce90d-122">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="ce90d-123">**Ársfjórðungslega** bókar upphæð ársfjórðungslega við lok hvers almanaksfjórðungs (31. mars, 30. júní, 30. september og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="ce90d-123">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="ce90d-124">**Tvisvar á ári** bókar upphæð á hálfs árs fresti miðað við hálft almanaksár (30. júní og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="ce90d-124">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="ce90d-125">Með **Daglega** er afskriftarupphæð fyrir afskriftaraðferðina daglega bókuð með einni færslu daglega.</span><span class="sxs-lookup"><span data-stu-id="ce90d-125">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="ce90d-126">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="ce90d-126">Fiscal</span></span>

<span data-ttu-id="ce90d-127">Ef valið er **Fjárhagsárs** á svæðinu **Afskriftarár** er 150% afskrift af bókfærðu virði reiknað á grundvelli fjárhagsárs fyrir fjárhagsdagatalið sem tilgreint er fyrir bókina eða fyrir fjárhagsdagatalið sem valin er á síðunni **Fjárhagur**.</span><span class="sxs-lookup"><span data-stu-id="ce90d-127">If you select **Fiscal** in the **Depreciation year** field, 150% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="ce90d-128">Fjárhagsdagatöl eru sett upp á síðunni **fjárhagsdagatöl**.</span><span class="sxs-lookup"><span data-stu-id="ce90d-128">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="ce90d-129">Fyrir fjárhagsárið 1. júlí til 30. júní, byrjar útreikningur afskrifta til dæmis þann 1. júlí.</span><span class="sxs-lookup"><span data-stu-id="ce90d-129">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="ce90d-130">Fjárhagsár getur verið lengra eða styttra en 12 mánuðir.</span><span class="sxs-lookup"><span data-stu-id="ce90d-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="ce90d-131">Afskriftirnar eru leiðréttar fyrir hvert tímabil.</span><span class="sxs-lookup"><span data-stu-id="ce90d-131">The depreciation is adjusted for each period.</span></span> <span data-ttu-id="ce90d-132">Lengd næsta fjárhagsárs ákvarðast af uppsetning tímabila á síðunni **Fjárhagsdagatöl**.</span><span class="sxs-lookup"><span data-stu-id="ce90d-132">The length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="ce90d-133">Ef **reikningsár** er valið sem afskriftaár eru eftirfarandi valkostir tiltækir í svæðinu **tímabilstíðni**:</span><span class="sxs-lookup"><span data-stu-id="ce90d-133">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="ce90d-134">**Árlega** bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið sem eina upphæð á síðasta degi fjárhagsársins.</span><span class="sxs-lookup"><span data-stu-id="ce90d-134">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="ce90d-135">**Reikningstímabil** bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið.</span><span class="sxs-lookup"><span data-stu-id="ce90d-135">**Fiscal period** posts the total amount of the depreciation that is calculated for the fiscal year.</span></span> <span data-ttu-id="ce90d-136">Þessari upphæð er safnað upp í fjárhagstímabilin sem skilgreind eru á síðunni **Fjárhagsdagatöl**.</span><span class="sxs-lookup"><span data-stu-id="ce90d-136">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-150-reducing-balance-depreciation"></a><span data-ttu-id="ce90d-137">Dæmi um afskriftir fyrir 150% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="ce90d-137">Example of 150% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="ce90d-138">Kaupverð</span><span class="sxs-lookup"><span data-stu-id="ce90d-138">Acquisition cost</span></span>               | <span data-ttu-id="ce90d-139">11.000</span><span class="sxs-lookup"><span data-stu-id="ce90d-139">11,000</span></span> |
| <span data-ttu-id="ce90d-140">Hrakvirði</span><span class="sxs-lookup"><span data-stu-id="ce90d-140">Salvage value</span></span>                  | <span data-ttu-id="ce90d-141">1.000</span><span class="sxs-lookup"><span data-stu-id="ce90d-141">1,000</span></span>  |
| <span data-ttu-id="ce90d-142">Afskriftargrundvöllur</span><span class="sxs-lookup"><span data-stu-id="ce90d-142">Depreciation base</span></span>              | <span data-ttu-id="ce90d-143">10.000</span><span class="sxs-lookup"><span data-stu-id="ce90d-143">10,000</span></span> |
| <span data-ttu-id="ce90d-144">Líftími í árum</span><span class="sxs-lookup"><span data-stu-id="ce90d-144">Service life years</span></span>             | <span data-ttu-id="ce90d-145">5</span><span class="sxs-lookup"><span data-stu-id="ce90d-145">5</span></span>      |
| <span data-ttu-id="ce90d-146">Föst árleg afskriftaprósenta</span><span class="sxs-lookup"><span data-stu-id="ce90d-146">Yearly depreciation percentage</span></span> | <span data-ttu-id="ce90d-147">30%</span><span class="sxs-lookup"><span data-stu-id="ce90d-147">30%</span></span>    |

<span data-ttu-id="ce90d-148">Aðferðin 150% bókfært virði stöðu deilir 150% með líftíma í árum.</span><span class="sxs-lookup"><span data-stu-id="ce90d-148">The 150% reducing balance method divides 150 percent by the service life years.</span></span> <span data-ttu-id="ce90d-149">Það hlutfall af hundraði er margfaldað með bókuðu nettóvirði eignarinnar til að ákvarða afskriftarupphæð ársins.</span><span class="sxs-lookup"><span data-stu-id="ce90d-149">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="ce90d-150">Tímabil</span><span class="sxs-lookup"><span data-stu-id="ce90d-150">Period</span></span> | <span data-ttu-id="ce90d-151">Reiknuð upphæð árlegra afskrifta</span><span class="sxs-lookup"><span data-stu-id="ce90d-151">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="ce90d-152">Bókfært verð</span><span class="sxs-lookup"><span data-stu-id="ce90d-152">Book value</span></span>             | <span data-ttu-id="ce90d-153">Nettó bókfært verð við lok árs</span><span class="sxs-lookup"><span data-stu-id="ce90d-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|------------------------|---------------------------------------|
| <span data-ttu-id="ce90d-154">1. ár</span><span class="sxs-lookup"><span data-stu-id="ce90d-154">Year 1</span></span> | <span data-ttu-id="ce90d-155">(11,000 – 1,000) × 30% = 3,000</span><span class="sxs-lookup"><span data-stu-id="ce90d-155">(11,000 – 1,000) × 30% = 3,000</span></span>                | <span data-ttu-id="ce90d-156">11.000 – 3.000 = 8.000</span><span class="sxs-lookup"><span data-stu-id="ce90d-156">11,000 – 3,000 = 8,000</span></span> | <span data-ttu-id="ce90d-157">11.000 – 1.000 – 3.000 = 7.000</span><span class="sxs-lookup"><span data-stu-id="ce90d-157">11,000 – 1,000 – 3,000 = 7,000</span></span>        |
| <span data-ttu-id="ce90d-158">2. ár</span><span class="sxs-lookup"><span data-stu-id="ce90d-158">Year 2</span></span> | <span data-ttu-id="ce90d-159">7,000 × 30% = 2,100</span><span class="sxs-lookup"><span data-stu-id="ce90d-159">7,000 × 30% = 2,100</span></span>                           | <span data-ttu-id="ce90d-160">8.000 – 2.100 = 5.900</span><span class="sxs-lookup"><span data-stu-id="ce90d-160">8,000 – 2,100 = 5,900</span></span>  | <span data-ttu-id="ce90d-161">7,000 – 2,100 = 4,900</span><span class="sxs-lookup"><span data-stu-id="ce90d-161">7,000 – 2,100 = 4,900</span></span>                 |
| <span data-ttu-id="ce90d-162">3. ár</span><span class="sxs-lookup"><span data-stu-id="ce90d-162">Year 3</span></span> | <span data-ttu-id="ce90d-163">4,900 × 30% = 1,470</span><span class="sxs-lookup"><span data-stu-id="ce90d-163">4,900 × 30% = 1,470</span></span>                           | <span data-ttu-id="ce90d-164">5.900 – 1.470 = 4.430</span><span class="sxs-lookup"><span data-stu-id="ce90d-164">5,900 – 1,470 = 4,430</span></span>  | <span data-ttu-id="ce90d-165">4,900 – 1,470 = 3,430</span><span class="sxs-lookup"><span data-stu-id="ce90d-165">4,900 – 1,470 = 3,430</span></span>                 |

> [!NOTE]
> <span data-ttu-id="ce90d-166">Yfirleitt þegar upphæðin sem er reiknuð með því að nota 150% bókfært virði verður afskriftaraðferð lægri en upphæðin sem yrði reiknuð með því að nota línulega afskriftaaðferð er umbreyting yfir í línulega aðferð fyrir eftirstandandi líftíma.</span><span class="sxs-lookup"><span data-stu-id="ce90d-166">Typically, when the amount that is calculated by using the 150% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]