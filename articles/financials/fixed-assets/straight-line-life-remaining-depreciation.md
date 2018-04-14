---
title: "Línuleg afskrift eftirstandandi líftíma"
description: "Þessi grein gefur yfirlit yfir afskriftaaðferðina Línuleg afskrift eftirstandandi líftíma."
author: twheeloc
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
ms.custom: 13851
ms.assetid: 0fa2f71a-596c-414c-a6e6-8f7405a0bf81
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 9b49f8ae3a2afc236aef622438ae1a0b575600bf
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="straight-line-life-remaining-depreciation"></a><span data-ttu-id="ff660-103">Línuleg afskrift eftirstandandi líftíma</span><span class="sxs-lookup"><span data-stu-id="ff660-103">Straight line life remaining depreciation</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="ff660-104">Þessi grein gefur yfirlit yfir afskriftaaðferðina Línuleg afskrift eftirstandandi líftíma.</span><span class="sxs-lookup"><span data-stu-id="ff660-104">This article gives an overview of the Straight line life remaining method of depreciation.</span></span>

<span data-ttu-id="ff660-105">Þegar afskriftarregla fyrir eignir er sett upp og valið er **Línuleg á eftirstöðvum líftíma** í svæðinu **aðferð** í síðunni **afskriftarregla** ráðast afskriftir eignasem heyra undir þá afskriftarreglu er byggð á eftirstandandi líftíma eignarinnar.</span><span class="sxs-lookup"><span data-stu-id="ff660-105">When you set up a fixed asset depreciation profile and select **Straight line life remaining** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is based on the remaining service life of the asset.</span></span> <span data-ttu-id="ff660-106">Þetta er að öllu jöfnu sama afskriftarupphæðin á hverju afskriftatímabili.</span><span class="sxs-lookup"><span data-stu-id="ff660-106">The depreciation amount is generally the same in each depreciation period.</span></span> <span data-ttu-id="ff660-107">Til að setja upp afskriftir fyrir Línuleg á eftirstöðvum líftíma, verður einnig að velja valkosti á svæðinu **afskriftarár** og **tímabilstíðni** á síðunni **afskriftareglur**.</span><span class="sxs-lookup"><span data-stu-id="ff660-107">To set up straight line life remaining depreciation, you also must select options in the **Depreciation year** field and the **Period frequency** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="ff660-108">Valkostirnir sem eru tiltækir á svæðinu**tímabilstíðni** eru mismunandi eftir því sem valið er á svæðinu **afskriftarár**.</span><span class="sxs-lookup"><span data-stu-id="ff660-108">The options that are available in the **Period frequency** field vary, depending on the value that is selected in the **Depreciation year** field.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="ff660-109">Velja afskriftaár</span><span class="sxs-lookup"><span data-stu-id="ff660-109">Select a depreciation year</span></span>
<span data-ttu-id="ff660-110">Hægt er að velja annað hvort **Dagatal** eða **reikningsár** í svæðinu **afskriftarár** á **afskriftareglu** síðunni.</span><span class="sxs-lookup"><span data-stu-id="ff660-110">You can select either **Calendar** or **Fiscal** in the **Depreciation year** field on the **Depreciation profiles** page.</span></span> <span data-ttu-id="ff660-111">Sjálfgefið gildi er **Dagatal**.</span><span class="sxs-lookup"><span data-stu-id="ff660-111">The default value is **Calendar**.</span></span> <span data-ttu-id="ff660-112">Valið skilgreinir valmöguleikana sem í boði eru á svæðinu **tímabilstíðni**.</span><span class="sxs-lookup"><span data-stu-id="ff660-112">Your selection determines the options that are available in the **Period frequency** field.</span></span> <span data-ttu-id="ff660-113">Þetta svæði skilgreinir bókunardagsetningar uppsafnaðra afskrifta og magn þeirra yfir almanaksárið.</span><span class="sxs-lookup"><span data-stu-id="ff660-113">This field defines the depreciation accrual posting dates and amounts throughout the calendar year.</span></span>

### <a name="calendar"></a><span data-ttu-id="ff660-114">Dagatal</span><span class="sxs-lookup"><span data-stu-id="ff660-114">Calendar</span></span>

<span data-ttu-id="ff660-115">Ef **Dagatal** er valið í ***Afskriftarár*** reitnum, er gert ráðyrir ári sem er 1. Janúar til og með  31. Desember , jafnvel ef fjárhagsdagatalið hefur verið skilgreint annan hátt.</span><span class="sxs-lookup"><span data-stu-id="ff660-115">If you select **Calendar** in the ***Depreciation year*** field, a year of January 1 through December 31 is assumed, even if you've defined the fiscal calendar differently.</span></span> <span data-ttu-id="ff660-116">**Dagatal** uppfærir afskriftargrundvöllinn 1. Janúar ár hvert.</span><span class="sxs-lookup"><span data-stu-id="ff660-116">The **Calendar** option updates the depreciation base on January 1 of each year.</span></span> <span data-ttu-id="ff660-117">Yfirleitt er afskriftagrundvöllurinn bókað nettóvirði mínus hrakvirði.</span><span class="sxs-lookup"><span data-stu-id="ff660-117">Typically, the depreciation base is the net book value minus the salvage value.</span></span> <span data-ttu-id="ff660-118">Í dæmunum hér að neðan er afskriftagrunnurinn deilistofninn í fyrstu segðinni í útreikningum í útreikningsdálkinum.</span><span class="sxs-lookup"><span data-stu-id="ff660-118">In the example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> <span data-ttu-id="ff660-119">Ef valið er **Dagatal** sem afskriftaár eru eftirfarandi valkostir tiltækir á svæðinu **tímabilstíðni**:</span><span class="sxs-lookup"><span data-stu-id="ff660-119">If you select **Calendar** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="ff660-120">**Árleg** upphæð bókar 31. Desember.</span><span class="sxs-lookup"><span data-stu-id="ff660-120">**Yearly** posts an amount on December 31.</span></span>
-   <span data-ttu-id="ff660-121">**Mánaðarlega**bókar mánaðarlega upphæð við lok hvers almanaks mánaðar.</span><span class="sxs-lookup"><span data-stu-id="ff660-121">**Monthly** posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="ff660-122">**Ársfjórðungslega**bókar upphæð ársfjórðungslega við lok hvers almanaksfjórðungs (31. mars, 30. júní, 30. september og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="ff660-122">**Quarterly** posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="ff660-123">Valkosturinn **tvisvar á ári** bókar upphæð á hálfs árs fresti miðað við hálft almanaksár (30. júní og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="ff660-123">**Half-Yearly** posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="ff660-124">Með **daglega** er afskriftarupphæð fyrir afskriftaraðferðina daglega bókuð með einni færslu daglega.</span><span class="sxs-lookup"><span data-stu-id="ff660-124">**Daily** posts the depreciation amount for the daily depreciation method by using one transaction for each day.</span></span>

<span data-ttu-id="ff660-125">Til dæmis, ef valið er **Árlega**, eru árlegar afskriftir bókaðar aðeins einu sinni, 31. Desember ár hvert.</span><span class="sxs-lookup"><span data-stu-id="ff660-125">For example, if you select **Yearly**, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="ff660-126">Ef valið er **mánaðarlega** bókast afskriftirnar sem einn tólfta árlegrar afskriftaupphæðar mánaðarlega.</span><span class="sxs-lookup"><span data-stu-id="ff660-126">If you select **Monthly**, the monthly depreciation is posted each month, as one-twelfth of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="ff660-127">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="ff660-127">Fiscal</span></span>

<span data-ttu-id="ff660-128">Ef valið er **reikningsár**á svæðinu **afskriftarár** er línuleg afskrift eftirstandandi líftíma notuð.</span><span class="sxs-lookup"><span data-stu-id="ff660-128">If you select **Fiscal** in the **Depreciation year** field, straight line life remaining depreciation is used.</span></span> <span data-ttu-id="ff660-129">Afskrift er reiknuð á grundvelli fjárhagsára sem eftir eru.</span><span class="sxs-lookup"><span data-stu-id="ff660-129">Depreciation is calculated based on the fiscal years remaining.</span></span> <span data-ttu-id="ff660-130">Til dæmis, fyrir fjárhagsárið 1. Júlí 2015 gegnum 30. Júní, 2016 byrjar útreikningur afskrifta þann 1. Júlí.</span><span class="sxs-lookup"><span data-stu-id="ff660-130">For example, for the fiscal year July 1, 2015, through June 30, 2016, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="ff660-131">Fjárhagsár getur verið lengra eða styttra en 12 mánuðir.</span><span class="sxs-lookup"><span data-stu-id="ff660-131">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="ff660-132">Afskriftirnar eru leiðréttar fyrir hvert fjárhagstímabil.</span><span class="sxs-lookup"><span data-stu-id="ff660-132">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="ff660-133">Lengd næsta fjárhagsárs ákvarðast af uppsetning fjárhagstímabila á síðunni**fjárhagsdagatöl**.</span><span class="sxs-lookup"><span data-stu-id="ff660-133">The length of the next fiscal year is determined by the fiscal periods that are set up on the **Fiscal calendars** page.</span></span> <span data-ttu-id="ff660-134">Ef **reikningsár** er valið sem afskriftaár eru eftirfarandi valkostir tiltækir í svæðinu **tímabilstíðni**:</span><span class="sxs-lookup"><span data-stu-id="ff660-134">If you select **Fiscal** as the depreciation year, the following options are available in the **Period frequency** field:</span></span>

-   <span data-ttu-id="ff660-135">**Árlega** bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið sem eina upphæð á síðasta degi fjárhagsársins.</span><span class="sxs-lookup"><span data-stu-id="ff660-135">**Yearly** posts the total amount of the depreciation that is calculated for the fiscal year as one amount, on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="ff660-136">**Fjárhagstímabil** reiknar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið.</span><span class="sxs-lookup"><span data-stu-id="ff660-136">**Fiscal period** calculates the total amount of the depreciation for the fiscal year.</span></span> <span data-ttu-id="ff660-137">Þessari upphæð er safnað upp í fjárhagstímabilin sem skilgreind eru á síðunni**fjárhagsdagatöl** fyrir fjárhagstímabilin sem eru skilgreind í fyrir bókina.</span><span class="sxs-lookup"><span data-stu-id="ff660-137">This amount is then accrued into the fiscal periods that are defined on the **Fiscal calendars** page for the fiscal calendar that is specified for the book.</span></span>

## <a name="example-of-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="ff660-138">Dæmi um Línuleg afskrift af óbreytt eign</span><span class="sxs-lookup"><span data-stu-id="ff660-138">Example of straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="ff660-139">eignin hefur eftirfarandi eiginleika:</span><span class="sxs-lookup"><span data-stu-id="ff660-139">A fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="ff660-140">Kaupverð</span><span class="sxs-lookup"><span data-stu-id="ff660-140">Acquisition cost</span></span>    | <span data-ttu-id="ff660-141">11.000</span><span class="sxs-lookup"><span data-stu-id="ff660-141">11,000</span></span> |
| <span data-ttu-id="ff660-142">Hrakvirði</span><span class="sxs-lookup"><span data-stu-id="ff660-142">Salvage value</span></span>       | <span data-ttu-id="ff660-143">1.000</span><span class="sxs-lookup"><span data-stu-id="ff660-143">1,000</span></span>  |
| <span data-ttu-id="ff660-144">Afskriftargrundvöllur</span><span class="sxs-lookup"><span data-stu-id="ff660-144">Depreciation base</span></span>   | <span data-ttu-id="ff660-145">10.000</span><span class="sxs-lookup"><span data-stu-id="ff660-145">10,000</span></span> |
| <span data-ttu-id="ff660-146">Líftími í árum</span><span class="sxs-lookup"><span data-stu-id="ff660-146">Service life years</span></span>  | <span data-ttu-id="ff660-147">5</span><span class="sxs-lookup"><span data-stu-id="ff660-147">5</span></span>      |
| <span data-ttu-id="ff660-148">Árleg afskrift</span><span class="sxs-lookup"><span data-stu-id="ff660-148">Yearly depreciation</span></span> | <span data-ttu-id="ff660-149">2.000</span><span class="sxs-lookup"><span data-stu-id="ff660-149">2,000</span></span>  |

<span data-ttu-id="ff660-150">Afskriftarupphæðin er sama ár hvert: (Kaupverð - hrakvirði) ÷ líftíma í árum</span><span class="sxs-lookup"><span data-stu-id="ff660-150">The depreciation amount is the same every year: (Acquisition cost – Salvage value) ÷ Service life years</span></span>

| <span data-ttu-id="ff660-151">Tímabil</span><span class="sxs-lookup"><span data-stu-id="ff660-151">Period</span></span> | <span data-ttu-id="ff660-152">Reiknuð upphæð árlegra afskrifta</span><span class="sxs-lookup"><span data-stu-id="ff660-152">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="ff660-153">Nettó bókfært verð við lok árs</span><span class="sxs-lookup"><span data-stu-id="ff660-153">Net book value at the end of the year</span></span> |
|--------|-----------------------------------------------|---------------------------------------|
| <span data-ttu-id="ff660-154">1. ár</span><span class="sxs-lookup"><span data-stu-id="ff660-154">Year 1</span></span> | <span data-ttu-id="ff660-155">(11.000 – 1.000) ÷ 5 = 2.000</span><span class="sxs-lookup"><span data-stu-id="ff660-155">(11,000 – 1,000) ÷ 5 = 2,000</span></span>                  | <span data-ttu-id="ff660-156">9.000</span><span class="sxs-lookup"><span data-stu-id="ff660-156">9,000</span></span>                                 |
| <span data-ttu-id="ff660-157">2. ár</span><span class="sxs-lookup"><span data-stu-id="ff660-157">Year 2</span></span> | <span data-ttu-id="ff660-158">(9.000 – 1.000) ÷ 4 = 2.000</span><span class="sxs-lookup"><span data-stu-id="ff660-158">(9,000 – 1,000) ÷ 4 = 2,000</span></span>                   | <span data-ttu-id="ff660-159">7.000</span><span class="sxs-lookup"><span data-stu-id="ff660-159">7,000</span></span>                                 |
| <span data-ttu-id="ff660-160">3. ár</span><span class="sxs-lookup"><span data-stu-id="ff660-160">Year 3</span></span> | <span data-ttu-id="ff660-161">(7.000 – 1.000) ÷ 3 = 2.000</span><span class="sxs-lookup"><span data-stu-id="ff660-161">(7,000 – 1,000) ÷ 3 = 2,000</span></span>                   | <span data-ttu-id="ff660-162">5.000</span><span class="sxs-lookup"><span data-stu-id="ff660-162">5,000</span></span>                                 |
| <span data-ttu-id="ff660-163">4. ár</span><span class="sxs-lookup"><span data-stu-id="ff660-163">Year 4</span></span> | <span data-ttu-id="ff660-164">(5.000 – 1.000) ÷ 2 = 2.000</span><span class="sxs-lookup"><span data-stu-id="ff660-164">(5,000 – 1,000) ÷ 2 = 2,000</span></span>                   | <span data-ttu-id="ff660-165">3.000</span><span class="sxs-lookup"><span data-stu-id="ff660-165">3,000</span></span>                                 |
| <span data-ttu-id="ff660-166">5. ár</span><span class="sxs-lookup"><span data-stu-id="ff660-166">Year 5</span></span> | <span data-ttu-id="ff660-167">(3.000 – 1.000) ÷ 1 = 2.000</span><span class="sxs-lookup"><span data-stu-id="ff660-167">(3,000 – 1,000) ÷ 1 = 2,000</span></span>                   | <span data-ttu-id="ff660-168">1.000</span><span class="sxs-lookup"><span data-stu-id="ff660-168">1,000</span></span>                                 |






