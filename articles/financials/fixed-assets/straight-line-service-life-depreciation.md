---
title: "Línulegar líftímaafskriftir"
description: "Þessi grein gefur yfirlit yfir afskriftaaðferðina Línulegar líftímaafskriftir."
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
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3341
ms.assetid: ae5ceaeb-aeb7-45cd-b835-23cf9c5cf95a
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 2b8c078841ca2e4bd994bbfbbe2abb130a4cf6fa
ms.contentlocale: is-is
ms.lasthandoff: 09/29/2017

---

# <a name="straight-line-service-life-depreciation"></a><span data-ttu-id="44c4b-103">Línulegar líftímaafskriftir</span><span class="sxs-lookup"><span data-stu-id="44c4b-103">Straight line service life depreciation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="44c4b-104">Þessi grein gefur yfirlit yfir afskriftaaðferðina Línulegar líftímaafskriftir.</span><span class="sxs-lookup"><span data-stu-id="44c4b-104">This article gives an overview of the Straight line service life method of depreciation.</span></span>

<span data-ttu-id="44c4b-105">Þegar afskriftaregla fyrir eignir er sett upp og velur og línulegur líftími í reitnum Aðferð í síðunni afskriftareglu, eru eignirnar sem hafa þessa afskriftarreglu úthlutaða á sig afskrifaðar byggt á heildar líftíma eignar.</span><span class="sxs-lookup"><span data-stu-id="44c4b-105">When you set up a fixed asset depreciation profile and select Straight line service life in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated based on the total service life of the asset.</span></span> <span data-ttu-id="44c4b-106">Þetta er að öllu jöfnu sama afskriftarupphæðin á hverju afskriftatímabili.</span><span class="sxs-lookup"><span data-stu-id="44c4b-106">This generally is the same depreciation amount in each depreciation period.</span></span> 

<span data-ttu-id="44c4b-107">munurinn á afskriftarupphæðinni sem er reiknuð milli eftirstöðva beinlínulíftíma og beinlínu líftíma er þegar leiðrétting er bókuð á eignina.</span><span class="sxs-lookup"><span data-stu-id="44c4b-107">The difference in the depreciation amount that is calculated between straight line service life remaining and straight line service life is when there is an adjustment posted to the asset.</span></span> 

<span data-ttu-id="44c4b-108">Til að setja upp afskriftir fyrir beinlínu líftíma, verður einnig að velja valkosti á svæðinu afskriftarár og reitum tímabilstíðni á síðunni afskriftareglur.</span><span class="sxs-lookup"><span data-stu-id="44c4b-108">To set up straight line service life depreciation, you must also select options in the Depreciation year and Period frequency fields in the Depreciation profiles page.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="44c4b-109">Velja afskriftaár</span><span class="sxs-lookup"><span data-stu-id="44c4b-109">Select a depreciation year</span></span>
<span data-ttu-id="44c4b-110">Hægt er að velja annað hvort Dagatal eða Fjárhagsár á svæði fyrir afskriftarár á síðunni afskriftareglur.</span><span class="sxs-lookup"><span data-stu-id="44c4b-110">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="44c4b-111">Valið skilgreinir valmöguleikana sem í boði eru á svæðinu tímabilstíðni.</span><span class="sxs-lookup"><span data-stu-id="44c4b-111">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="44c4b-112">Sjálfgefinn kostur er dagatal.</span><span class="sxs-lookup"><span data-stu-id="44c4b-112">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="44c4b-113">Dagatal</span><span class="sxs-lookup"><span data-stu-id="44c4b-113">Calendar</span></span>

<span data-ttu-id="44c4b-114">Ef Dagatal er valið er gert ráð fyrir ári sem er 1. Janúar til 31. Desember , jafnvel ef fjárhagsdagatalið hefur verið skilgreint annan hátt.</span><span class="sxs-lookup"><span data-stu-id="44c4b-114">If you select Calendar, a year of January 1 to December 31 is assumed, even if you have defined the fiscal calendar differently.</span></span> 

<span data-ttu-id="44c4b-115">Valmöguleikinn dagatal uppfærir afskriftagrunninn (vanalega bókað nettóverð að frádregnu hrakvirði) þann 1. janúar ár hvert.</span><span class="sxs-lookup"><span data-stu-id="44c4b-115">The Calendar option updates the depreciation base, which is typically the net book value minus the salvage value, on January 1 of each year.</span></span> <span data-ttu-id="44c4b-116">Í dæmunum hér að neðan er afskriftagrunnurinn deilistofninn í fyrstu segðinni í útreikningum í útreikningsdálkinum.</span><span class="sxs-lookup"><span data-stu-id="44c4b-116">In the examples later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="44c4b-117">Ef dagatal er valið eru eftirfarandi valkostir á svæðinu tímabilstíðni, sem skilgreinir bókunardagsetningar uppsafnaðra afskrifta og upphæðir yfir allt almanaksárið:</span><span class="sxs-lookup"><span data-stu-id="44c4b-117">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>
-   <span data-ttu-id="44c4b-118">Árleg upphæð bókar 31. Desember.</span><span class="sxs-lookup"><span data-stu-id="44c4b-118">Yearly posts an amount on December 31.</span></span>
-   <span data-ttu-id="44c4b-119">Valkosturinn mánaðarlega bókar mánaðarlega upphæð við lok hvers almanaksmánaðar</span><span class="sxs-lookup"><span data-stu-id="44c4b-119">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="44c4b-120">Valkosturinn ársfjórðungslega bókar upphæð ársfjórðungslega við lok hvers almanaksfjórðungs (31. mars, 30. júní, 30. september og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="44c4b-120">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="44c4b-121">Valkosturinn tvisvar á ári bókar upphæð á hálfs árs fresti miðað við hálft almanaksár (30. júní og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="44c4b-121">Half-Yearly posts a half-yearly amount at the end of each calendar half year (June 30 and December 31).</span></span>
-   <span data-ttu-id="44c4b-122">Með valkostinum daglega er afskriftarupphæð fyrir afskriftaraðferðina daglega bókuð með einni færslu daglega.</span><span class="sxs-lookup"><span data-stu-id="44c4b-122">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="44c4b-123">Til dæmis, ef valið er Árlega, eru árlegar afskriftir bókaðar aðeins einu sinni, 31. Desember ár hvert.</span><span class="sxs-lookup"><span data-stu-id="44c4b-123">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="44c4b-124">Ef valið er mánaðarlega bókast afskriftirnar sem 1/12 árlegrar afskriftaupphæðar mánaðarlega.</span><span class="sxs-lookup"><span data-stu-id="44c4b-124">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="44c4b-125">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="44c4b-125">Fiscal</span></span>

<span data-ttu-id="44c4b-126">Ef valið er reikningsár á svæðinu afskriftarár er afskrift línulegs líftíma notuð.</span><span class="sxs-lookup"><span data-stu-id="44c4b-126">If you select Fiscal in the Depreciation year field, the straight line service life depreciation is used.</span></span> <span data-ttu-id="44c4b-127">Það reiknuð á grundvelli fjárhagsársins sem er skilgreindur eftir fjárhagsdagatalið sem tilgreindur er fyrir bók eða fjárhagsdagatal sem valinn er í Fjárhagssíðu.</span><span class="sxs-lookup"><span data-stu-id="44c4b-127">It is calculated based on the fiscal year, which is defined by the fiscal calendar that is specified for the book, or by the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="44c4b-128">Fjárhagsdagatöl eru sett upp á síðunni fjárhagsdagatöl.</span><span class="sxs-lookup"><span data-stu-id="44c4b-128">Fiscal calendars are set up in the Fiscal calendars page.</span></span>

<span data-ttu-id="44c4b-129">Fyrir fjárhagsárið 1. júlí til 30. júní, byrjar útreikningur afskrifta til dæmis þann 1. júlí.</span><span class="sxs-lookup"><span data-stu-id="44c4b-129">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="44c4b-130">Fjárhagsár getur verið lengra eða styttra en 12 mánuðir.</span><span class="sxs-lookup"><span data-stu-id="44c4b-130">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="44c4b-131">Afskriftirnar eru leiðréttar sjálfkrafa fyrir hvert fjárhagstímabil.</span><span class="sxs-lookup"><span data-stu-id="44c4b-131">The depreciation automatically is adjusted for each fiscal period.</span></span> <span data-ttu-id="44c4b-132">Lengd næsta fjárhagsárs er byggt á fjárhagstímabilum sem sett eru upp þegar nýtt fjárhagsár er stofnað á skjámyndinni fjárhagsdagatöl.</span><span class="sxs-lookup"><span data-stu-id="44c4b-132">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars form.</span></span> 

<span data-ttu-id="44c4b-133">Ef fjárhagsár er valið eru eftirfarandi valkostir tiltækir á svæðinu tímabilstíðni:</span><span class="sxs-lookup"><span data-stu-id="44c4b-133">If you select Fiscal, the following options are available in the Period frequency field:</span></span>
-   <span data-ttu-id="44c4b-134">Árlega bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið sem eina upphæð á síðasta degi fjárhagsársins.</span><span class="sxs-lookup"><span data-stu-id="44c4b-134">Yearly posts the total amount of the depreciation that is calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="44c4b-135">Fjárhagstímabil reiknar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið sem er safnað upp í tímabilin sem eru skilgreind í skjámynd fjárhagsdagatals fyrir fjárhagsdagatal.</span><span class="sxs-lookup"><span data-stu-id="44c4b-135">Fiscal period calculates the total amount of the depreciation for the fiscal year, which is accrued into the periods that are defined in the Fiscal calendars form for the fiscal calendar.</span></span>

## <a name="example-straight-line-depreciation-of-an-unchanged-fixed-asset"></a><span data-ttu-id="44c4b-136">Dæmi: Línuleg afskrift af óbreytt eign</span><span class="sxs-lookup"><span data-stu-id="44c4b-136">Example: Straight line depreciation of an unchanged fixed asset</span></span>
<span data-ttu-id="44c4b-137">Segjum sem svo að eignin hafi eftirfarandi eiginleika:</span><span class="sxs-lookup"><span data-stu-id="44c4b-137">Suppose that a fixed asset has the following characteristics.</span></span>

|                     |        |
|---------------------|--------|
| <span data-ttu-id="44c4b-138">Kaupverð</span><span class="sxs-lookup"><span data-stu-id="44c4b-138">Acquisition cost</span></span>    | <span data-ttu-id="44c4b-139">11.000</span><span class="sxs-lookup"><span data-stu-id="44c4b-139">11,000</span></span> |
| <span data-ttu-id="44c4b-140">Hrakvirði</span><span class="sxs-lookup"><span data-stu-id="44c4b-140">Salvage value</span></span>       | <span data-ttu-id="44c4b-141">1.000</span><span class="sxs-lookup"><span data-stu-id="44c4b-141">1,000</span></span>  |
| <span data-ttu-id="44c4b-142">Afskriftargrundvöllur</span><span class="sxs-lookup"><span data-stu-id="44c4b-142">Depreciation base</span></span>   | <span data-ttu-id="44c4b-143">10.000</span><span class="sxs-lookup"><span data-stu-id="44c4b-143">10,000</span></span> |
| <span data-ttu-id="44c4b-144">Líftími í árum</span><span class="sxs-lookup"><span data-stu-id="44c4b-144">Service life years</span></span>  | <span data-ttu-id="44c4b-145">5</span><span class="sxs-lookup"><span data-stu-id="44c4b-145">5</span></span>      |
| <span data-ttu-id="44c4b-146">Árleg afskrift</span><span class="sxs-lookup"><span data-stu-id="44c4b-146">Yearly depreciation</span></span> | <span data-ttu-id="44c4b-147">2.000</span><span class="sxs-lookup"><span data-stu-id="44c4b-147">2,000</span></span>  |

<span data-ttu-id="44c4b-148">Sama afskriftarupphæð á hverju ári.</span><span class="sxs-lookup"><span data-stu-id="44c4b-148">You get the same depreciation amount each year.</span></span> <span data-ttu-id="44c4b-149">(Kaupverð - Hrakvirði / Líftími í árum</span><span class="sxs-lookup"><span data-stu-id="44c4b-149">(Acquisition cost - Salvage value) / Service life years</span></span>

| <span data-ttu-id="44c4b-150">Tímabil</span><span class="sxs-lookup"><span data-stu-id="44c4b-150">Period</span></span> | <span data-ttu-id="44c4b-151">Reiknuð árleg upphæð afskrifta</span><span class="sxs-lookup"><span data-stu-id="44c4b-151">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="44c4b-152">Nettó bókfært verð við lok árs</span><span class="sxs-lookup"><span data-stu-id="44c4b-152">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="44c4b-153">1. ár</span><span class="sxs-lookup"><span data-stu-id="44c4b-153">Year 1</span></span> | <span data-ttu-id="44c4b-154">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="44c4b-154">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="44c4b-155">9.000</span><span class="sxs-lookup"><span data-stu-id="44c4b-155">9,000</span></span>                                 |
| <span data-ttu-id="44c4b-156">2. ár</span><span class="sxs-lookup"><span data-stu-id="44c4b-156">Year 2</span></span> | <span data-ttu-id="44c4b-157">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="44c4b-157">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="44c4b-158">7.000</span><span class="sxs-lookup"><span data-stu-id="44c4b-158">7,000</span></span>                                 |
| <span data-ttu-id="44c4b-159">3. ár</span><span class="sxs-lookup"><span data-stu-id="44c4b-159">Year 3</span></span> | <span data-ttu-id="44c4b-160">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="44c4b-160">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="44c4b-161">5.000</span><span class="sxs-lookup"><span data-stu-id="44c4b-161">5,000</span></span>                                 |
| <span data-ttu-id="44c4b-162">4. ár</span><span class="sxs-lookup"><span data-stu-id="44c4b-162">Year 4</span></span> | <span data-ttu-id="44c4b-163">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="44c4b-163">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="44c4b-164">3.000</span><span class="sxs-lookup"><span data-stu-id="44c4b-164">3,000</span></span>                                 |
| <span data-ttu-id="44c4b-165">5. ár</span><span class="sxs-lookup"><span data-stu-id="44c4b-165">Year 5</span></span> | <span data-ttu-id="44c4b-166">(11,000 - 1,000) / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="44c4b-166">(11,000 - 1,000) / 5 = 2,000</span></span>              | <span data-ttu-id="44c4b-167">1.000</span><span class="sxs-lookup"><span data-stu-id="44c4b-167">1,000</span></span>                                 |

## <a name="example-straight-line-depreciation-of-a-modified-fixed-asset"></a><span data-ttu-id="44c4b-168">Dæmi: Línuleg afskrift af breyttri eign</span><span class="sxs-lookup"><span data-stu-id="44c4b-168">Example: Straight line depreciation of a modified fixed asset</span></span>

<span data-ttu-id="44c4b-169">Segjum sem svo að bætt sé við  leiðrétting kaupa upp á 4,000 á 2. ári við sömu eignina.</span><span class="sxs-lookup"><span data-stu-id="44c4b-169">Suppose that you add an acquisition adjustment of 4,000 in year 2 to the same fixed asset.</span></span> 

<span data-ttu-id="44c4b-170">Líftími leiðréttingar kaupa er sú sama og eignarinnar og hefst við kaup þess.</span><span class="sxs-lookup"><span data-stu-id="44c4b-170">The service life of the acquisition adjustment is the same as that of the fixed asset and starts at the time of its acquisition.</span></span> <span data-ttu-id="44c4b-171">Nettó bókfært verð stendur eftir við lok 5. árs, sem samsvarar nettó bókfært verð kaupverðsbreytingarinnar.</span><span class="sxs-lookup"><span data-stu-id="44c4b-171">A net book value remains at the end of year 5, corresponding to the net book value of the acquisition adjustment.</span></span> <span data-ttu-id="44c4b-172">Afskriftirnar eftir tímabilum eru reiknaðar eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="44c4b-172">The depreciation by period is calculated as shown in the following table.</span></span>

| <span data-ttu-id="44c4b-173">Tímabil</span><span class="sxs-lookup"><span data-stu-id="44c4b-173">Period</span></span> | <span data-ttu-id="44c4b-174">Reiknuð upphæð árlegra afskrifta</span><span class="sxs-lookup"><span data-stu-id="44c4b-174">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="44c4b-175">Nettó bókfært verð við lok árs</span><span class="sxs-lookup"><span data-stu-id="44c4b-175">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="44c4b-176">1. ár</span><span class="sxs-lookup"><span data-stu-id="44c4b-176">Year 1</span></span> | <span data-ttu-id="44c4b-177">10,000 / 5 = 2,000</span><span class="sxs-lookup"><span data-stu-id="44c4b-177">10,000 / 5 = 2,000</span></span>                        | <span data-ttu-id="44c4b-178">11.000 - 2.000 = 9.000</span><span class="sxs-lookup"><span data-stu-id="44c4b-178">11,000 - 2,000 = 9,000</span></span>                |
| <span data-ttu-id="44c4b-179">2. ár</span><span class="sxs-lookup"><span data-stu-id="44c4b-179">Year 2</span></span> | <span data-ttu-id="44c4b-180">4.000 ( – Leiðrétting kaupa</span><span class="sxs-lookup"><span data-stu-id="44c4b-180">4,000 (acquisition adjustment)</span></span>            | <span data-ttu-id="44c4b-181">9,000 + 4,000 =13,000</span><span class="sxs-lookup"><span data-stu-id="44c4b-181">9,000 + 4,000 =13,000</span></span>                 |
| <span data-ttu-id="44c4b-182">2. ár</span><span class="sxs-lookup"><span data-stu-id="44c4b-182">Year 2</span></span> | <span data-ttu-id="44c4b-183">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="44c4b-183">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="44c4b-184">13.000 - 2.800 = 10.200</span><span class="sxs-lookup"><span data-stu-id="44c4b-184">13,000 - 2,800 = 10,200</span></span>               |
| <span data-ttu-id="44c4b-185">3. ár</span><span class="sxs-lookup"><span data-stu-id="44c4b-185">Year 3</span></span> | <span data-ttu-id="44c4b-186">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="44c4b-186">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="44c4b-187">10,200 - 2,800 = 7,400</span><span class="sxs-lookup"><span data-stu-id="44c4b-187">10,200 - 2,800 = 7,400</span></span>                |
| <span data-ttu-id="44c4b-188">4. ár</span><span class="sxs-lookup"><span data-stu-id="44c4b-188">Year 4</span></span> | <span data-ttu-id="44c4b-189">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="44c4b-189">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="44c4b-190">7,400 - 2,800 = 4,600</span><span class="sxs-lookup"><span data-stu-id="44c4b-190">7,400 - 2,800 = 4,600</span></span>                 |
| <span data-ttu-id="44c4b-191">5. ár</span><span class="sxs-lookup"><span data-stu-id="44c4b-191">Year 5</span></span> | <span data-ttu-id="44c4b-192">14,000 / 5 = 2,800</span><span class="sxs-lookup"><span data-stu-id="44c4b-192">14,000 / 5 = 2,800</span></span>                        | <span data-ttu-id="44c4b-193">4,600 - 2,800 = 1,800</span><span class="sxs-lookup"><span data-stu-id="44c4b-193">4,600 - 2,800 = 1,800</span></span>                 |
| <span data-ttu-id="44c4b-194">6. ár</span><span class="sxs-lookup"><span data-stu-id="44c4b-194">Year 6</span></span> | <span data-ttu-id="44c4b-195">Eftirstöðvar 800\*</span><span class="sxs-lookup"><span data-stu-id="44c4b-195">Remaining 800\*</span></span>                           | <span data-ttu-id="44c4b-196">1,800 – 800 = 1,000</span><span class="sxs-lookup"><span data-stu-id="44c4b-196">1,800 – 800 = 1,000</span></span>                   |

<span data-ttu-id="44c4b-197">\*Þar sem eftirstandandi upphæð eru lægri en afskriftarupphæðin eru aðeins eftirstöðvarnar, að frádregnu hrakvirði, teknar.</span><span class="sxs-lookup"><span data-stu-id="44c4b-197">\*Because the remaining amount is less than the depreciation amount, only the remaining amount minus the salvage value is taken.</span></span>






