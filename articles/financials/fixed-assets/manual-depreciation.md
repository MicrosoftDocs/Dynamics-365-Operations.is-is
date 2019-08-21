---
title: Handvirkar afskriftir
description: Þessi grein veitir yfirlit yfir handvirka afskriftaraðferð.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13811
ms.assetid: b0e837c9-515a-4aed-9060-5ec94f37edeb
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84cde511ab0b5cbe4b99e72832bf548336b6b28c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840314"
---
# <a name="manual-depreciation"></a><span data-ttu-id="4faec-103">Handvirkar afskriftir</span><span class="sxs-lookup"><span data-stu-id="4faec-103">Manual depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4faec-104">Þessi grein veitir yfirlit yfir handvirka afskriftaraðferð.</span><span class="sxs-lookup"><span data-stu-id="4faec-104">This article gives an overview of the manual depreciation method.</span></span>

<span data-ttu-id="4faec-105">Þegar afskriftarregla fyrir eignir er sett upp og valið er **handvirkt** í svæðinu **aðferð** í síðunni **afskriftarregla** ráðast afskriftir eignasem heyra undir þá afskriftarreglu af prósentunni sem færð er inn fyrir hvert bil í almanaksárinu.</span><span class="sxs-lookup"><span data-stu-id="4faec-105">When you set up a fixed asset depreciation profile and select **Manual** in the **Method** field on the **Depreciation profiles** page, the depreciation of fixed assets that are assigned to the depreciation profile is determined by the percentage that you enter for each interval in the calendar year.</span></span> <span data-ttu-id="4faec-106">Bilin sem sett eru upp sem prósentur fyrir, eru bókuð samkvæmt gildinu sem valið er í á **tímabilstíðni** reit á **Almennt** flýtiflipa í **afskriftareglur** síðu.</span><span class="sxs-lookup"><span data-stu-id="4faec-106">The intervals that you set up percentages for are posted according to the value that you select in the **Period frequency** field on the **General** FastTab of the **Depreciation profiles** page.</span></span> <span data-ttu-id="4faec-107">Hér er gildin sem hægt er að velja:</span><span class="sxs-lookup"><span data-stu-id="4faec-107">Here are the values that you can select:</span></span>

-   <span data-ttu-id="4faec-108">Árlega</span><span class="sxs-lookup"><span data-stu-id="4faec-108">Yearly</span></span>
-   <span data-ttu-id="4faec-109">Mánaðarlega</span><span class="sxs-lookup"><span data-stu-id="4faec-109">Monthly</span></span>
-   <span data-ttu-id="4faec-110">Ársfjórðungslega</span><span class="sxs-lookup"><span data-stu-id="4faec-110">Quarterly</span></span>
-   <span data-ttu-id="4faec-111">Tvisvar á ári</span><span class="sxs-lookup"><span data-stu-id="4faec-111">Half-Yearly</span></span>
-   <span data-ttu-id="4faec-112">Daglega</span><span class="sxs-lookup"><span data-stu-id="4faec-112">Daily</span></span>

<span data-ttu-id="4faec-113">Þegar bókunarbil eru valin, smellið á **handvirk röðun** og stillið prósentur fyrir hvert bókunarbil.</span><span class="sxs-lookup"><span data-stu-id="4faec-113">After you select the period frequency, click **Manual schedules**, and set up percentages for each posting interval.</span></span> <span data-ttu-id="4faec-114">Saman skilgreina handvirka röðunin og bókunarbilin afskriftarmagnið, eins og sýnt er í dæmunum hér að neðan.</span><span class="sxs-lookup"><span data-stu-id="4faec-114">Together, the manual schedules and the posting intervals define the depreciation amount, as shown in the examples later in this article.</span></span> <span data-ttu-id="4faec-115">Handvirkar afskriftir eru alltaf reiknaðar sem prósenta af kaupverði.</span><span class="sxs-lookup"><span data-stu-id="4faec-115">Manual depreciation is always calculated as a percentage of the acquisition price.</span></span> <span data-ttu-id="4faec-116">Handvirkar afskriftir fyrir prósentutölurnar sem færðar eru inn í bilin fyrir afskriftir þurfa ekki að vera samanlagt 100 prósent.</span><span class="sxs-lookup"><span data-stu-id="4faec-116">For manual depreciation, the percentages that you enter in the intervals of the depreciation don't have to add up to 100 percent.</span></span> <span data-ttu-id="4faec-117">Handvirkar afskriftir eru sveigjanlega afskriftaraðferð sem oft er notuð til að skilgreina óregluleg afskriftaregla í á **bækur** síða, eins og óreglubundnar afskriftir fyrir sérstakan tilgang (t.d. skattur).</span><span class="sxs-lookup"><span data-stu-id="4faec-117">Manual depreciation is a flexible depreciation method that is often used to define an extraordinary depreciation profile on the **Books** page, such as a non-periodic depreciation for special purposes (for example, tax).</span></span>

## <a name="examples"></a><span data-ttu-id="4faec-118">Dæmi</span><span class="sxs-lookup"><span data-stu-id="4faec-118">Examples</span></span>
<span data-ttu-id="4faec-119">Kaupverð: 11.000,00 Væntanlegt rýrnunarvirði: 1.000,00 eftirfarandi tafla sýnir bilin og prósentutölurnar sem settar eru upp á í **Afskriftaregluáætlanir eigna** síðu.</span><span class="sxs-lookup"><span data-stu-id="4faec-119">Acquisition price: 11,000.00 Expected scrap value: 1,000.00 The following table shows the intervals and percentages that you set up on the **Fixed asset depreciation profile schedules** page.</span></span>

| <span data-ttu-id="4faec-120">Númerabil</span><span class="sxs-lookup"><span data-stu-id="4faec-120">Interval number</span></span> | <span data-ttu-id="4faec-121">Prósenta</span><span class="sxs-lookup"><span data-stu-id="4faec-121">Percentage</span></span> |
|-----------------|------------|
| <span data-ttu-id="4faec-122">1</span><span class="sxs-lookup"><span data-stu-id="4faec-122">1</span></span>               | <span data-ttu-id="4faec-123">10,00</span><span class="sxs-lookup"><span data-stu-id="4faec-123">10.00</span></span>      |
| <span data-ttu-id="4faec-124">2</span><span class="sxs-lookup"><span data-stu-id="4faec-124">2</span></span>               | <span data-ttu-id="4faec-125">50,00</span><span class="sxs-lookup"><span data-stu-id="4faec-125">50.00</span></span>      |
| <span data-ttu-id="4faec-126">3</span><span class="sxs-lookup"><span data-stu-id="4faec-126">3</span></span>               | <span data-ttu-id="4faec-127">8,00</span><span class="sxs-lookup"><span data-stu-id="4faec-127">8.00</span></span>       |

<span data-ttu-id="4faec-128">Afskriftirnar eftir tímabilum eru reiknaðar eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="4faec-128">The following table shows how the depreciation for each interval is calculated.</span></span>

|  <span data-ttu-id="4faec-129">Númerabil</span><span class="sxs-lookup"><span data-stu-id="4faec-129">Interval number</span></span> | <span data-ttu-id="4faec-130">Reiknuð upphæð árlegra afskrifta</span><span class="sxs-lookup"><span data-stu-id="4faec-130">Calculation of the yearly depreciation amount</span></span> | <span data-ttu-id="4faec-131">Nettó bókfært verð við lok árs</span><span class="sxs-lookup"><span data-stu-id="4faec-131">Net book value at the end of the interval</span></span> |
|------------------|-----------------------------------------------|-------------------------------------------|
| <span data-ttu-id="4faec-132">1</span><span class="sxs-lookup"><span data-stu-id="4faec-132">1</span></span>                | <span data-ttu-id="4faec-133">(11.000 – 1.000) × 10% = 1.000</span><span class="sxs-lookup"><span data-stu-id="4faec-133">(11,000 – 1,000) × 10% = 1,000</span></span>                | <span data-ttu-id="4faec-134">10.000 (11.000 – 1.000)</span><span class="sxs-lookup"><span data-stu-id="4faec-134">10,000 (11,000 – 1,000)</span></span>                   |
| <span data-ttu-id="4faec-135">2</span><span class="sxs-lookup"><span data-stu-id="4faec-135">2</span></span>                | <span data-ttu-id="4faec-136">(11.000 – 1.000) × 50% = 5.000</span><span class="sxs-lookup"><span data-stu-id="4faec-136">(11,000 – 1,000) × 50% = 5,000</span></span>                | <span data-ttu-id="4faec-137">5.000 (10.000 – 5.000)</span><span class="sxs-lookup"><span data-stu-id="4faec-137">5,000 (10,000 – 5,000)</span></span>                    |
| <span data-ttu-id="4faec-138">3</span><span class="sxs-lookup"><span data-stu-id="4faec-138">3</span></span>                | <span data-ttu-id="4faec-139">(11.000 – 1.000) × 8% = 800</span><span class="sxs-lookup"><span data-stu-id="4faec-139">(11,000 – 1,000) × 8% = 800</span></span>                   | <span data-ttu-id="4faec-140">4.200 (5.000 – 800)</span><span class="sxs-lookup"><span data-stu-id="4faec-140">4,200 (5,000 – 800)</span></span>                       |

<span data-ttu-id="4faec-141">Ef valið er **mánaðarlega** í svæðinu **tímabilstíðni** seturðu upp 12 handvirk röðunarbil.</span><span class="sxs-lookup"><span data-stu-id="4faec-141">If you select **Monthly** in the **Period frequency** field, you set up 12 manual schedule intervals.</span></span> <span data-ttu-id="4faec-142">Eftirfarandi tafla sýnir afskriftarupphæðir fyrir fyrstu tveggja tímabila.</span><span class="sxs-lookup"><span data-stu-id="4faec-142">The following table shows the depreciation amounts for the first two intervals.</span></span>

| <span data-ttu-id="4faec-143">Bil</span><span class="sxs-lookup"><span data-stu-id="4faec-143">Interval</span></span> | <span data-ttu-id="4faec-144">Afskriftarupphæð</span><span class="sxs-lookup"><span data-stu-id="4faec-144">Depreciation amount</span></span>            |
|----------|--------------------------------|
| <span data-ttu-id="4faec-145">janúar</span><span class="sxs-lookup"><span data-stu-id="4faec-145">January</span></span>  | <span data-ttu-id="4faec-146">(11.000 – 1.000) × 10% = 1.000</span><span class="sxs-lookup"><span data-stu-id="4faec-146">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="4faec-147">febrúar</span><span class="sxs-lookup"><span data-stu-id="4faec-147">February</span></span> | <span data-ttu-id="4faec-148">(11.000 – 1.000) × 50% = 5.000</span><span class="sxs-lookup"><span data-stu-id="4faec-148">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="4faec-149">Ef valið er <strong>Tvisvar á ári</strong> í *<strong><em>Tímabilstíðni</em>* reitnum</strong> eru tvö handvirk röðunarbil sett upp.</span><span class="sxs-lookup"><span data-stu-id="4faec-149">If you select <strong>Half-Yearly</strong> in the *<strong><em>Period frequency</em>* field</strong>, you set up two manual schedule intervals.</span></span> <span data-ttu-id="4faec-150">Eftirfarandi tafla sýnir afskriftarupphæðir fyrir þessi tvö tímabila.</span><span class="sxs-lookup"><span data-stu-id="4faec-150">The following table shows the depreciation amounts for those two intervals.</span></span>

| <span data-ttu-id="4faec-151">Bil</span><span class="sxs-lookup"><span data-stu-id="4faec-151">Interval</span></span>    | <span data-ttu-id="4faec-152">Afskriftarupphæð</span><span class="sxs-lookup"><span data-stu-id="4faec-152">Depreciation amount</span></span>            |
|-------------|--------------------------------|
| <span data-ttu-id="4faec-153">30. júní</span><span class="sxs-lookup"><span data-stu-id="4faec-153">June 30</span></span>     | <span data-ttu-id="4faec-154">(11.000 – 1.000) × 10% = 1.000</span><span class="sxs-lookup"><span data-stu-id="4faec-154">(11,000 – 1,000) × 10% = 1,000</span></span> |
| <span data-ttu-id="4faec-155">31. desember</span><span class="sxs-lookup"><span data-stu-id="4faec-155">December 31</span></span> | <span data-ttu-id="4faec-156">(11.000 – 1.000) × 50% = 5.000</span><span class="sxs-lookup"><span data-stu-id="4faec-156">(11,000 – 1,000) × 50% = 5,000</span></span> |

<span data-ttu-id="4faec-157">Samtala fyrir prósentutölurnar fyrir öll bilin þurfa ekki að vera 100.</span><span class="sxs-lookup"><span data-stu-id="4faec-157">The total of percentages for all intervals doesn't have to be 100.</span></span> <span data-ttu-id="4faec-158">Hins vegar munu berast skilaboð ef gildið í **heildarprósenta** á síðunni **Afskriftaregluáætlanir eigna** er ekki **100**.</span><span class="sxs-lookup"><span data-stu-id="4faec-158">However, you receive a message if the value in the **Cumulative percentage** field on the **Fixed asset depreciation profile schedules** page isn't **100**.</span></span>



