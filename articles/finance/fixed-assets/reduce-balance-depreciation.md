---
title: Minnka bókfært virði
description: Þessi grein gefur yfirlit yfir afskriftaraðferðina bókfært virði.
author: ShylaThompson
manager: AnnBe
ms.date: 04/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.custom: 3281
ms.assetid: 1b86763d-d47c-4a6a-a9a6-d97a736750da
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 69228aec217826780ceb91771028a6a5a180d037
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220986"
---
# <a name="reduce-balance-depreciation"></a><span data-ttu-id="990fa-103">Minnka bókfært virði</span><span class="sxs-lookup"><span data-stu-id="990fa-103">Reduce balance depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="990fa-104">Þessi grein gefur yfirlit yfir afskriftaraðferðina bókfært virði.</span><span class="sxs-lookup"><span data-stu-id="990fa-104">This article gives an overview of the Reducing balance method of depreciation.</span></span>

<span data-ttu-id="990fa-105">Þegar afskriftaregla fyrir eignir er sett upp og bókfært virði er valið í skjámyndinni um afskriftir verða eignir sem hafa þessa afskriftareglu afskrifaðar um sama hlutfall af hundraði á hverju afskriftatímabili.</span><span class="sxs-lookup"><span data-stu-id="990fa-105">When you set up a fixed asset depreciation profile and select Reducing balance in the Method field in the Depreciation profiles page, the assets that have this depreciation profile assigned to them are depreciated by the same percentage in each depreciation period.</span></span>

<span data-ttu-id="990fa-106">Til að setja upp afskriftir fyrir bókfært virði verður einnig að velja í svæðunum á flýtiflipanum "almennt" í skjámyndinni fyrir afskriftarregluna.</span><span class="sxs-lookup"><span data-stu-id="990fa-106">To set up reducing balance depreciation, you must also make selections in fields on the General FastTab of the Depreciation profiles page.</span></span> <span data-ttu-id="990fa-107">Fyrst skal velja ár í afskriftasvæðinu fyrir ár.</span><span class="sxs-lookup"><span data-stu-id="990fa-107">First, select a year in the Depreciation year field.</span></span> <span data-ttu-id="990fa-108">Mismunandi valmöguleikar birtast á svæðinu "tímabilstíðni" eftir því hvað valið er, svo sem útskýrt er í eftirfarandi köflum.</span><span class="sxs-lookup"><span data-stu-id="990fa-108">Depending on the selection, different options appear in the Period frequency field, as explained in the following sections.</span></span> 

<span data-ttu-id="990fa-109">Einnig verður að færa gildi í hlutfallssvæðið fyrir afskriftarregluna.</span><span class="sxs-lookup"><span data-stu-id="990fa-109">You must also enter a value in the Percentage field for the depreciation profile.</span></span> <span data-ttu-id="990fa-110">Ef kosturinn "full afskrift" er valinn er eftirstandandi afskriftagrunnur tekinn á síðasta afskriftatímabili, sem gæti verið há upphæð.</span><span class="sxs-lookup"><span data-stu-id="990fa-110">If you select the Full depreciation option, the remaining depreciation basis is taken in the last depreciation period and could be a large amount.</span></span> <span data-ttu-id="990fa-111">Sum lönd/svæði nota ekki umskipti yfir í línulega afskriftaaðferð.</span><span class="sxs-lookup"><span data-stu-id="990fa-111">Some countries/regions do not use a switchover to a straight line method.</span></span> <span data-ttu-id="990fa-112">Umskipti eiga sér stað þegar upphæð auka afskriftaraðferðar er hærri eða jöfn og upphæð aðalafskriftarreglunnar, þá verður afskriftarupphæðin sem er tekin upphæðin sem fengin er með aukaaðferðinni.</span><span class="sxs-lookup"><span data-stu-id="990fa-112">Switchover occurs when the alternative depreciation method amount is greater than or equal to the primary depreciation profile amount, and the depreciation amount taken is the alternative method amount.</span></span> 

<span data-ttu-id="990fa-113">Af því að eign afskrifast aldrei að fullu ef prósentureikningur er notaður verður að velja kostinn "full afskrift" til að afskrifa eign að fullu.</span><span class="sxs-lookup"><span data-stu-id="990fa-113">Because an asset will never be fully depreciated based on a percentage calculation, you must select the Full depreciation option to fully depreciate an asset.</span></span>

## <a name="select-a-depreciation-year"></a><span data-ttu-id="990fa-114">Velja afskriftaár</span><span class="sxs-lookup"><span data-stu-id="990fa-114">Select a depreciation year</span></span>
<span data-ttu-id="990fa-115">Hægt er að velja annað hvort Dagatal eða Fjárhagsár á svæði fyrir afskriftarár á síðunni afskriftareglur.</span><span class="sxs-lookup"><span data-stu-id="990fa-115">You can select either Calendar or Fiscal in the Depreciation year field in the Depreciation profiles page.</span></span> <span data-ttu-id="990fa-116">Valið skilgreinir valmöguleikana sem í boði eru á svæðinu tímabilstíðni.</span><span class="sxs-lookup"><span data-stu-id="990fa-116">The selection defines the options that are available in the Period frequency field.</span></span> <span data-ttu-id="990fa-117">Sjálfgefinn kostur er dagatal.</span><span class="sxs-lookup"><span data-stu-id="990fa-117">The default option is Calendar.</span></span>

### <a name="calendar"></a><span data-ttu-id="990fa-118">Dagatal</span><span class="sxs-lookup"><span data-stu-id="990fa-118">Calendar</span></span>

<span data-ttu-id="990fa-119">Valmöguleikinn dagatal uppfærir afskriftagrunninn (vanalega bókað nettóverð að frádregnu hrakvirði ) þann 1. janúar ár hvert.</span><span class="sxs-lookup"><span data-stu-id="990fa-119">The Calendar option updates the depreciation base, which is typically the net book value minus the scrap value, on January 1 of each year.</span></span> <span data-ttu-id="990fa-120">Í dæminu um afskriftir fyrir bókfært virði hér að neðan er afskriftargrunnurinn deilistofninn í fyrstu segðinni í útreikningsdálkinum.</span><span class="sxs-lookup"><span data-stu-id="990fa-120">In the reducing balance depreciation example later in this topic, the depreciation base is the numerator in the first expression in the calculations column.</span></span> 

<span data-ttu-id="990fa-121">Ef dagatal er valið eru eftirfarandi valkostir á svæðinu tímabilstíðni, sem skilgreinir bókunardagsetningar uppsafnaðra afskrifta og upphæðir yfir allt almanaksárið:</span><span class="sxs-lookup"><span data-stu-id="990fa-121">If you select Calendar, the following options are available in the Period frequency field, which defines the depreciation accrual posting dates and amounts throughout the calendar year:</span></span>

-   <span data-ttu-id="990fa-122">Valkosturinn árlega bókar 31. desember.</span><span class="sxs-lookup"><span data-stu-id="990fa-122">Yearly posts on December 31.</span></span>
-   <span data-ttu-id="990fa-123">Valkosturinn mánaðarlega bókar mánaðarlega upphæð við lok hvers almanaksmánaðar</span><span class="sxs-lookup"><span data-stu-id="990fa-123">Monthly posts a monthly amount at the end of each calendar month.</span></span>
-   <span data-ttu-id="990fa-124">Valkosturinn ársfjórðungslega bókar upphæð ársfjórðungslega við lok hvers almanaksfjórðungs (31. mars, 30. júní, 30. september og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="990fa-124">Quarterly posts a quarterly amount at the end of each calendar quarter (March 31, June 30, September 30, and December 31).</span></span>
-   <span data-ttu-id="990fa-125">Valkosturinn tvisvar á ári bókar upphæð á hálfs árs fresti miðað við hálft almanaksár (30. júní og 31. desember).</span><span class="sxs-lookup"><span data-stu-id="990fa-125">Half-Yearly posts a half-yearly amount at the end of each calendar half-year (June 30 and December 31).</span></span>
-   <span data-ttu-id="990fa-126">Með valkostinum daglega er afskriftarupphæð fyrir afskriftaraðferðina daglega bókuð með einni færslu daglega.</span><span class="sxs-lookup"><span data-stu-id="990fa-126">Daily posts the depreciation amount for the daily depreciation method using one transaction for each day.</span></span>

<span data-ttu-id="990fa-127">Til dæmis, ef valið er Árlega, eru árlegar afskriftir bókaðar aðeins einu sinni, 31. Desember ár hvert.</span><span class="sxs-lookup"><span data-stu-id="990fa-127">For example, if you select Yearly, the yearly depreciation is posted only one time, on December 31 of each year.</span></span> <span data-ttu-id="990fa-128">Ef valið er mánaðarlega bókast afskriftirnar sem 1/12 árlegrar afskriftaupphæðar mánaðarlega.</span><span class="sxs-lookup"><span data-stu-id="990fa-128">If you select Monthly, the monthly depreciation is posted each month as 1/12 of the yearly depreciation amount.</span></span>

### <a name="fiscal"></a><span data-ttu-id="990fa-129">Fjárhagur</span><span class="sxs-lookup"><span data-stu-id="990fa-129">Fiscal</span></span>

<span data-ttu-id="990fa-130">Ef valið er reikningsár á svæðinu afskriftarár er línulega afskriftaraðferðin notuð.</span><span class="sxs-lookup"><span data-stu-id="990fa-130">If you select Fiscal in the Depreciation year field, the straight line depreciation method is used.</span></span> <span data-ttu-id="990fa-131">Það er reiknað á grundvelli fjárhagsársins sem er sett upp á síðunni fjárhagsdagatöl fyrir fjárhagsdagatalið sem valinn er á síðunni höfuðbók.</span><span class="sxs-lookup"><span data-stu-id="990fa-131">It is calculated based on the fiscal year, which is set up in the Fiscal calendars page for the fiscal calendar that is selected in the Ledger page.</span></span> <span data-ttu-id="990fa-132">Fyrir fjárhagsárið 1. júlí til 30. júní, byrjar útreikningur afskrifta til dæmis þann 1. júlí.</span><span class="sxs-lookup"><span data-stu-id="990fa-132">For example, for fiscal year July 1 through June 30, the depreciation calculation starts on July 1.</span></span> <span data-ttu-id="990fa-133">Fjárhagsár getur verið lengra eða styttra en 12 mánuðir.</span><span class="sxs-lookup"><span data-stu-id="990fa-133">The fiscal year can be longer or shorter than 12 months.</span></span> <span data-ttu-id="990fa-134">Afskriftirnar eru leiðréttar fyrir hvert fjárhagstímabil.</span><span class="sxs-lookup"><span data-stu-id="990fa-134">The depreciation is adjusted for each fiscal period.</span></span> <span data-ttu-id="990fa-135">Lengd næsta fjárhagsárs er byggt á fjárhagstímabilum sem sett eru upp þegar nýtt fjárhagsár er stofnað á síðunni fjárhagsdagatöl.</span><span class="sxs-lookup"><span data-stu-id="990fa-135">The length of the next fiscal year is based on the fiscal periods that you set up when you create a new fiscal year in the Fiscal calendars page.</span></span>


<span data-ttu-id="990fa-136">Ef fjárhagsár er valið eru eftirfarandi valkostir tiltækir á svæðinu tímabilstíðni:</span><span class="sxs-lookup"><span data-stu-id="990fa-136">If you select Fiscal, the following options are available in the Period frequency field:</span></span>

-   <span data-ttu-id="990fa-137">Árlega bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið sem eina upphæð á síðasta degi fjárhagsársins.</span><span class="sxs-lookup"><span data-stu-id="990fa-137">Yearly posts the total amount of the depreciation calculated for the fiscal year as one amount on the last day of the fiscal year.</span></span>
-   <span data-ttu-id="990fa-138">Fjárhagstímabil bókar heildarupphæð reiknaðra afskrifta fyrir fjárhagsárið, sem er safnað upp í fjárhagstímabilin sem skilgreind eru fyrir fjárhagsdagatalið sem valið er á síðunni höfuðbók, eða fyrir fjárhagsdagatalið sem valið er fyrir bók fyrir eign.</span><span class="sxs-lookup"><span data-stu-id="990fa-138">Fiscal period posts the total amount of the depreciation calculated for the fiscal year, which is accrued into the fiscal periods that are defined for the fiscal calendar that is selected in the Ledger page, or for the fiscal calendar that is selected for the book for a fixed asset.</span></span>

## <a name="example-of-reducing-balance-depreciation"></a><span data-ttu-id="990fa-139">Dæmi um afskriftir fyrir bókfært virði</span><span class="sxs-lookup"><span data-stu-id="990fa-139">Example of reducing balance depreciation</span></span>

<span data-ttu-id="990fa-140">Segjum að kaupverð eignarinnar sé 11.000, rýrnunarvirðið sé 1.000 og prósentustuðull afskriftanna sé 30.</span><span class="sxs-lookup"><span data-stu-id="990fa-140">Suppose that the fixed asset acquisition price is 11,000, the scrap value is 1,000, and the depreciation percentage factor is 30.</span></span> 

<span data-ttu-id="990fa-141">Með því að nota aðferðina lækkandi afskrift eru 30 prósent af afskriftagrunninum (nettóvirði mínus rýrnunarvirði) reiknuð í lok fyrra afskriftatímabils.</span><span class="sxs-lookup"><span data-stu-id="990fa-141">Using the Reducing balance method, 30 percent of the depreciation base (net book value minus scrap value) is calculated at the end of the previous depreciation period.</span></span> <span data-ttu-id="990fa-142">Afskriftir fyrstu þriggja áranna eru sýndar í eftirfarandi töflu:</span><span class="sxs-lookup"><span data-stu-id="990fa-142">Depreciation for the first three years is shown in the following table.</span></span>

| <span data-ttu-id="990fa-143">Tímabil</span><span class="sxs-lookup"><span data-stu-id="990fa-143">Period</span></span> | <span data-ttu-id="990fa-144">Reiknuð upphæð árlegra afskrifta</span><span class="sxs-lookup"><span data-stu-id="990fa-144">Calculation of yearly depreciation amount</span></span> | <span data-ttu-id="990fa-145">Nettó bókfært verð við lok árs</span><span class="sxs-lookup"><span data-stu-id="990fa-145">Net book value at the end of the year</span></span> |
|--------|-------------------------------------------|---------------------------------------|
| <span data-ttu-id="990fa-146">1. ár</span><span class="sxs-lookup"><span data-stu-id="990fa-146">Year 1</span></span> | <span data-ttu-id="990fa-147">(11.000 - 1.000) \* 30% = 3.000</span><span class="sxs-lookup"><span data-stu-id="990fa-147">(11,000 - 1,000) \* 30% = 3,000</span></span>           | <span data-ttu-id="990fa-148">(11,000 - 1,000) - 3,000 = 7,000</span><span class="sxs-lookup"><span data-stu-id="990fa-148">(11,000 - 1,000) - 3,000 = 7,000</span></span>      |
| <span data-ttu-id="990fa-149">2. ár</span><span class="sxs-lookup"><span data-stu-id="990fa-149">Year 2</span></span> | <span data-ttu-id="990fa-150">(7.000 - 1.000) \* 30% = 1.800</span><span class="sxs-lookup"><span data-stu-id="990fa-150">(7,000 - 1,000) \* 30% = 1,800</span></span>            | <span data-ttu-id="990fa-151">(7,000 -1,800) = 5,200</span><span class="sxs-lookup"><span data-stu-id="990fa-151">(7,000 -1,800) = 5,200</span></span>                |
| <span data-ttu-id="990fa-152">3. ár</span><span class="sxs-lookup"><span data-stu-id="990fa-152">Year 3</span></span> | <span data-ttu-id="990fa-153">(5.200 - 1.000) \* 30% = 1.260</span><span class="sxs-lookup"><span data-stu-id="990fa-153">(5,200 - 1,000) \* 30% = 1,260</span></span>            | <span data-ttu-id="990fa-154">(5,200 - 1,260) = 3,940</span><span class="sxs-lookup"><span data-stu-id="990fa-154">(5,200 - 1,260) = 3,940</span></span>               |


-







[!INCLUDE[footer-include](../../includes/footer-banner.md)]