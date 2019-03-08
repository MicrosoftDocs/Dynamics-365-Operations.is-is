---
title: 175 prósenta lækkandi afskrift
description: Þetta efnisatriði gefur yfirlit yfir 175 prósent afskriftaraðferðina bókfært virði.
author: saraschi2
manager: AnnBe
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 13911
ms.assetid: cc5d001f-bcfe-4602-9ec1-9e265e9fd188
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a63293dbf24c27733f8013947aeab5792fa0db9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "320168"
---
# <a name="175-percent-reducing-balance-depreciation"></a><span data-ttu-id="2a98f-103">175 prósenta lækkandi afskrift</span><span class="sxs-lookup"><span data-stu-id="2a98f-103">175 percent reducing balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2a98f-104">Þetta efnisatriði gefur yfirlit yfir 175 prósent afskriftaraðferðina bókfært virði.</span><span class="sxs-lookup"><span data-stu-id="2a98f-104">This topic gives an overview of the 175 percent reducing balance method of depreciation.</span></span>

<span data-ttu-id="2a98f-105">Þegar afskriftaregla fyrir eignir er sett upp og gildið **175% bókfært virði** í reitnum **Aðferð** reitnum á **Afskriftarreglur** síðunni eru eignir sem er úthlutað á þessa afskriftareglu afskrifaðar með sömu prósentu á hverju afskriftatímabili.</span><span class="sxs-lookup"><span data-stu-id="2a98f-105">When you set up a fixed asset depreciation profile and select **175% reducing balance** in the **Method** field on the **Depreciation profiles** page, fixed assets that are assigned the depreciation profile are depreciated by the same percentage in each depreciation period.</span></span> 

<span data-ttu-id="2a98f-106">Til að setja upp afskriftir fyrir 175% bókfært virði, verður einnig að velja valkosti í á **afskriftarár** svæði og **tímabilstíðni** á í **afskriftareglur** síðu.</span><span class="sxs-lookup"><span data-stu-id="2a98f-106">To set up 175% reducing balance depreciation, you must also select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="2a98f-107">Valkostirnir sem eru tiltækir á svæðinu**tímabilstíðni** eru mismunandi eftir því sem valið er á svæðinu **afskriftarár**.</span><span class="sxs-lookup"><span data-stu-id="2a98f-107">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="2a98f-108">Velja afskriftaár</span><span class="sxs-lookup"><span data-stu-id="2a98f-108">Select a depreciation year</span></span>
<span data-ttu-id="2a98f-109">Hægt er að velja annað hvort **Dagatal** eða **reikningsár** í svæðinu **afskriftarár** á **afskriftareglu** síðunni.</span><span class="sxs-lookup"><span data-stu-id="2a98f-109">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="2a98f-110">Sjálfgefið gildi er **Dagatal**.</span><span class="sxs-lookup"><span data-stu-id="2a98f-110">The default value is **Calendar**.</span></span> 

<span data-ttu-id="2a98f-111">Valið skilgreinir valmöguleikana sem í boði eru á svæðinu **tímabilstíðni**.</span><span class="sxs-lookup"><span data-stu-id="2a98f-111">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="2a98f-112">Þetta svæði skilgreinir bókunardagsetningar uppsafnaðra afskrifta og magn þeirra yfir almanaksárið.</span><span class="sxs-lookup"><span data-stu-id="2a98f-112">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="2a98f-113">Dagatal</span><span class="sxs-lookup"><span data-stu-id="2a98f-113">Calendar</span></span>

<span data-ttu-id="2a98f-114">Það er hægt að velja að halda sjálfgefnum gildum í svæðinu **afskriftarár**,**dagatal**.</span><span class="sxs-lookup"><span data-stu-id="2a98f-114">You can keep the default value in the **Depreciation year** field, **Calendar**.</span></span> 

<span data-ttu-id="2a98f-115">**Dagatal** uppfærir afskriftargrundvöllinn 1. Janúar ár hvert.</span><span class="sxs-lookup"><span data-stu-id="2a98f-115">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="2a98f-116">Yfirleitt er afskriftagrundvöllurinn bókað nettóvirði mínus hrakvirði.</span><span class="sxs-lookup"><span data-stu-id="2a98f-116">Typically, the depreciation base is the net book value minus the scrap value.</span></span> <span data-ttu-id="2a98f-117">Í dæmunum hér að neðan er afskriftagrunnurinn deilistofninn í fyrstu segðinni í útreikningum í útreikningsdálkinum.</span><span class="sxs-lookup"><span data-stu-id="2a98f-117">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="2a98f-118">Ef valið er **Dagatal** sem afskriftaár eru eftirfarandi valkostir tiltækir á svæðinu **tímabilstíðni**:</span><span class="sxs-lookup"><span data-stu-id="2a98f-118">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="2a98f-119">**Árleg** upphæð bókar 31. Desember.</span><span class="sxs-lookup"><span data-stu-id="2a98f-119">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="2a98f-120">**Mánaðarlega**bókar mánaðarlega upphæð við lok hvers almanaks mánaðar.</span><span class="sxs-lookup"><span data-stu-id="2a98f-120">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="2a98f-121">**Ársfjórðungslega**bókar upphæð ársfjórðungslega við lok hvers almanaksfjórðungs (31. mars, 30. júní, 30. september og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="2a98f-121">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="2a98f-122">**Tvisvar á ári**bókar upphæð á hálfs árs fresti miðað við hálft almanaksár (30. júní og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="2a98f-122">**Half-Yearly** posts a half-yearly amount at the calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="2a98f-123">Með **Daglega** er afskriftarupphæð fyrir afskriftaraðferðina daglega bókuð með einni færslu daglega.</span><span class="sxs-lookup"><span data-stu-id="2a98f-123">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

### <a name="fiscal"></a><span data-ttu-id="2a98f-124">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="2a98f-124">Fiscal</span></span>

<span data-ttu-id="2a98f-125">Ef valið er **Fjárhagsárs** á svæðinu **Afskriftarár** er 175% afskrift af bókfærðu virði reiknað á grundvelli fjárhagsárs fyrir fjárhagsdagatalið sem tilgreint er fyrir bókina eða fyrir fjárhagsdagatalið sem valin er á síðunni **Fjárhagur**.</span><span class="sxs-lookup"><span data-stu-id="2a98f-125">If you select **Fiscal** in the **Depreciation year** field, 175% reducing balance depreciation is calculated based on the fiscal year for the fiscal calendar that is specified for the book, or for the fiscal calendar that is selected on the **Ledger** page.</span></span> <span data-ttu-id="2a98f-126">Fjárhagsdagatöl eru sett upp á síðunni **fjárhagsdagatöl**.</span><span class="sxs-lookup"><span data-stu-id="2a98f-126">Fiscal calendars are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="2a98f-127">Fyrir nánari upplýsingar, sjá [Fjárhagsdagatöl, fjárhagsár, og tímabil.](../budgeting/fiscal-calendars-fiscal-years-periods.md)</span><span class="sxs-lookup"><span data-stu-id="2a98f-127">For more information, see [Fiscal calendars, fiscal years, and periods](../budgeting/fiscal-calendars-fiscal-years-periods.md).</span></span>

<span data-ttu-id="2a98f-128">Fyrir fjárhagsárið 1. júlí til 30. júní, byrjar útreikningur afskrifta til dæmis þann 1. júlí.</span><span class="sxs-lookup"><span data-stu-id="2a98f-128">For example, for the fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="2a98f-129">Fjárhagsár getur verið lengra eða styttra en 12 mánuðir.</span><span class="sxs-lookup"><span data-stu-id="2a98f-129">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="2a98f-130">Afskriftirnar eru leiðréttar sjálfkrafa fyrir hvert tímabil og lengd næsta fjárhagsárs ákvarðast af uppsetningu tímabila á síðunni **Fjárhagsdagatöl**.</span><span class="sxs-lookup"><span data-stu-id="2a98f-130">The depreciation is automatically adjusted for each period, and the length of the next fiscal year is determined by the setup of periods on the **Fiscal calendars** page.</span></span> 

<span data-ttu-id="2a98f-131">Ef **reikningsár** er valið sem afskriftaár eru eftirfarandi valkostir tiltækir í svæðinu **tímabilstíðni**:</span><span class="sxs-lookup"><span data-stu-id="2a98f-131">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="2a98f-132">**Árlega** bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið sem eina upphæð á síðasta degi fjárhagsársins.</span><span class="sxs-lookup"><span data-stu-id="2a98f-132">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="2a98f-133">**Fjárhagstímabil** reiknar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið.</span><span class="sxs-lookup"><span data-stu-id="2a98f-133">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="2a98f-134">Þessari upphæð er safnað upp í fjárhagstímabilin sem skilgreind eru á síðunni**fjárhagsdagatöl**.</span><span class="sxs-lookup"><span data-stu-id="2a98f-134">This amount is accrued into the fiscal periods that are defined on the **Fiscal calendars** page.</span></span>

## <a name="example-of-175-reducing-balance-depreciation"></a><span data-ttu-id="2a98f-135">Dæmi um afskriftir fyrir 175% bókfært virði</span><span class="sxs-lookup"><span data-stu-id="2a98f-135">Example of 175% reducing balance depreciation</span></span>

|                                |        |
|--------------------------------|--------|
| <span data-ttu-id="2a98f-136">Kaupverð</span><span class="sxs-lookup"><span data-stu-id="2a98f-136">Acquisition cost</span></span>               | <span data-ttu-id="2a98f-137">11.000</span><span class="sxs-lookup"><span data-stu-id="2a98f-137">11,000</span></span> |
| <span data-ttu-id="2a98f-138">Hrakvirði</span><span class="sxs-lookup"><span data-stu-id="2a98f-138">Salvage value</span></span>                  | <span data-ttu-id="2a98f-139">1.000</span><span class="sxs-lookup"><span data-stu-id="2a98f-139">1,000</span></span>  |
| <span data-ttu-id="2a98f-140">Afskriftargrundvöllur</span><span class="sxs-lookup"><span data-stu-id="2a98f-140">Depreciation base</span></span>              | <span data-ttu-id="2a98f-141">10.000</span><span class="sxs-lookup"><span data-stu-id="2a98f-141">10,000</span></span> |
| <span data-ttu-id="2a98f-142">Líftími í árum</span><span class="sxs-lookup"><span data-stu-id="2a98f-142">Service life years</span></span>             | <span data-ttu-id="2a98f-143">5</span><span class="sxs-lookup"><span data-stu-id="2a98f-143">5</span></span>      |
| <span data-ttu-id="2a98f-144">Föst árleg afskriftaprósenta</span><span class="sxs-lookup"><span data-stu-id="2a98f-144">Yearly depreciation percentage</span></span> | <span data-ttu-id="2a98f-145">35%</span><span class="sxs-lookup"><span data-stu-id="2a98f-145">35%</span></span>    |

<span data-ttu-id="2a98f-146">Aðferðin afskriftir fyrir 175% bókfært virði stöðu deilir 175% með líftíma í árum.</span><span class="sxs-lookup"><span data-stu-id="2a98f-146">The 175% reducing balance depreciation method divides 175 percent by the service life years.</span></span> <span data-ttu-id="2a98f-147">Það hlutfall af hundraði er margfaldað með bókuðu nettóvirði eignarinnar til að ákvarða afskriftarupphæð ársins.</span><span class="sxs-lookup"><span data-stu-id="2a98f-147">That percentage will be multiplied by the net book value of the asset to determine the depreciation amount for the year.</span></span>

| <span data-ttu-id="2a98f-148">Tímabil</span><span class="sxs-lookup"><span data-stu-id="2a98f-148">Period</span></span> | <span data-ttu-id="2a98f-149">Reiknuð upphæð árlegra afskrifta</span><span class="sxs-lookup"><span data-stu-id="2a98f-149">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="2a98f-150">Bókfært verð</span><span class="sxs-lookup"><span data-stu-id="2a98f-150">Book value</span></span>                  | <span data-ttu-id="2a98f-151">Nettó bókfært verð við lok árs</span><span class="sxs-lookup"><span data-stu-id="2a98f-151">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|-----------------------------|---------------------------------------|
| <span data-ttu-id="2a98f-152">1. ár</span><span class="sxs-lookup"><span data-stu-id="2a98f-152">Year 1</span></span> | <span data-ttu-id="2a98f-153">(11,000 – 1,000) × 35% = 3,500</span><span class="sxs-lookup"><span data-stu-id="2a98f-153">(11,000 – 1,000) × 35% = 3,500</span></span>                | <span data-ttu-id="2a98f-154">11.000 – 3.500 = 7.500</span><span class="sxs-lookup"><span data-stu-id="2a98f-154">11,000 – 3,500 = 7,500</span></span>      | <span data-ttu-id="2a98f-155">11.000 – 1.000 – 3.500 = 6.500</span><span class="sxs-lookup"><span data-stu-id="2a98f-155">11,000 – 1,000 – 3,500 = 6,500</span></span>        |
| <span data-ttu-id="2a98f-156">2. ár</span><span class="sxs-lookup"><span data-stu-id="2a98f-156">Year 2</span></span> | <span data-ttu-id="2a98f-157">6,500 × 35% = 2,275</span><span class="sxs-lookup"><span data-stu-id="2a98f-157">6,500 × 35% = 2,275</span></span>                           | <span data-ttu-id="2a98f-158">7,500 – 2,275 = 5,225</span><span class="sxs-lookup"><span data-stu-id="2a98f-158">7,500 – 2,275 = 5,225</span></span>       | <span data-ttu-id="2a98f-159">6,500 – 2,275 = 4,225</span><span class="sxs-lookup"><span data-stu-id="2a98f-159">6,500 – 2,275 = 4,225</span></span>                 |
| <span data-ttu-id="2a98f-160">3. ár</span><span class="sxs-lookup"><span data-stu-id="2a98f-160">Year 3</span></span> | <span data-ttu-id="2a98f-161">4,225 × 35% = 1,478.75</span><span class="sxs-lookup"><span data-stu-id="2a98f-161">4,225 × 35% = 1,478.75</span></span>                        | <span data-ttu-id="2a98f-162">5.225 – 1.478,75 = 3.746,25</span><span class="sxs-lookup"><span data-stu-id="2a98f-162">5,225 – 1,478.75 = 3,746.25</span></span> | <span data-ttu-id="2a98f-163">4,225 – 1,478.75 = 2,746.25</span><span class="sxs-lookup"><span data-stu-id="2a98f-163">4,225 – 1,478.75 = 2,746.25</span></span>           |

> [!NOTE] 
> <span data-ttu-id="2a98f-164">Yfirleitt þegar upphæðin sem er reiknuð með því að nota 175% bókfært virði verður afskriftaraðferð lægri en upphæðin sem yrði reiknuð með því að nota línulega afskriftaaðferð er umbreyting yfir í línulega aðferð fyrir eftirstandandi líftíma.</span><span class="sxs-lookup"><span data-stu-id="2a98f-164">Typically, when the amount that is calculated by using the 175% reducing balance depreciation method becomes less than the amount that would be calculated by using the straight line method, there is a conversion to the straight line method for the remaining life.</span></span>



