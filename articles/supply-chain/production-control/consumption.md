---
title: Reikna út efnisnotkunina
description: Þessi grein gefur upplýsingar um ýmsa valkosti sem tengjast útreikningi á efnisnotkun.
author: johanhoffmann
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMDesignerEditBOM, BOMTable, ProdBOM
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53401
ms.assetid: 9cff88e4-0425-4707-9178-3c2cb10df7c2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc39df69a22b90a805aa9967d52dafea27c78c2b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246334"
---
# <a name="calculate-material-consumption"></a><span data-ttu-id="00f75-103">Reikna út efnisnotkunina</span><span class="sxs-lookup"><span data-stu-id="00f75-103">Calculate material consumption</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00f75-104">Þessi grein gefur upplýsingar um ýmsa valkosti sem tengjast útreikningi á efnisnotkun.</span><span class="sxs-lookup"><span data-stu-id="00f75-104">This article provides information about various options that are related to the calculation of material consumption.</span></span> 

<span data-ttu-id="00f75-105">eftirfarandi valkosti sem tengjast útreikningi á hráefnisnotkun eri tiltækir í **Uppsetningu** og **Skrefanotkun** flipana í á **Línuupplýsingar** flýtiflipa í **Uppskrift** síðu.</span><span class="sxs-lookup"><span data-stu-id="00f75-105">The following options that are related to the calculation of material consumption are available on the **Setup** and **Step consumption** tabs on the **Line details** FastTab of the **Bill of materials** page.</span></span>

## <a name="variable-and-constant-consumption"></a><span data-ttu-id="00f75-106">Breytileg og föst notkun</span><span class="sxs-lookup"><span data-stu-id="00f75-106">Variable and constant consumption</span></span>
<span data-ttu-id="00f75-107">Í **Notkun er** reit er hægt að velja hvort eigi að reikna notkun út sem fast magn eða breytilegt magn.</span><span class="sxs-lookup"><span data-stu-id="00f75-107">In the **Consumption is** field, you can select whether consumption should be calculated as a constant quantity or a variable quantity.</span></span> <span data-ttu-id="00f75-108">Velja **Fast** ef fast magn eða rúmmál er nauðsynleg fyrir framleiðsluna, óháð því magni sem er framleitt.</span><span class="sxs-lookup"><span data-stu-id="00f75-108">Select **Constant** if a fixed quantity or volume is required for the production, regardless of the quantity that is produced.</span></span> <span data-ttu-id="00f75-109">Velja **Breytilegt**, sem er sjálfgefna stillingin, sé áskilin upphæð efnis í fullbúnu vörunum í hlutfalli við fjölda fullbúnar vörur sem eru framleiddar.</span><span class="sxs-lookup"><span data-stu-id="00f75-109">Select **Variable**, which is the default setting, if the required amount of material in the finished goods is proportional to the number of finished goods that are produced.</span></span>

## <a name="calculating-consumption-from-a-formula"></a><span data-ttu-id="00f75-110">Formúla notuð við útreikning notkunar</span><span class="sxs-lookup"><span data-stu-id="00f75-110">Calculating consumption from a formula</span></span>
<span data-ttu-id="00f75-111">Í **Formúlu** svæði er hægt að setja upp mismunandi formúlur til að reikna út efnisnotkunina.</span><span class="sxs-lookup"><span data-stu-id="00f75-111">In the **Formula** field, you can set up various formulas for calculating material consumption.</span></span> <span data-ttu-id="00f75-112">Ef nota á sjálfgefna gildið **Staðlaða**, notkun er ekki reiknað út frá formúlu.</span><span class="sxs-lookup"><span data-stu-id="00f75-112">If you use the default value, **Standard**, the consumption isn't calculated from a formula.</span></span> <span data-ttu-id="00f75-113">Eftirfarandi formúlur vinna ásamt **Hæð**, **Breidd**, **Dýpt**, **Þéttleiki**, og **Fast** svæði:</span><span class="sxs-lookup"><span data-stu-id="00f75-113">The following formulas work together with the **Height**, **Width**, **Depth**, **Density**, and **Constant** fields:</span></span>

-   <span data-ttu-id="00f75-114">Hæð \* Fasti</span><span class="sxs-lookup"><span data-stu-id="00f75-114">Height \* Constant</span></span>
-   <span data-ttu-id="00f75-115">Hæð \* Breidd \* Fasti</span><span class="sxs-lookup"><span data-stu-id="00f75-115">Height \* Width \* Constant</span></span>
-   <span data-ttu-id="00f75-116">Hæð \* Breidd \* Dýpt \* Fasti</span><span class="sxs-lookup"><span data-stu-id="00f75-116">Height \* Width \* Depth \* Constant</span></span>
-   <span data-ttu-id="00f75-117">(Hæð \* Breidd \* Dýpt / Þéttleiki) \* Fasti</span><span class="sxs-lookup"><span data-stu-id="00f75-117">(Height \* Width \* Depth / Density) \* Constant</span></span>

## <a name="rounding-up-and-multiples"></a><span data-ttu-id="00f75-118">Sléttun og margfeldi</span><span class="sxs-lookup"><span data-stu-id="00f75-118">Rounding up and multiples</span></span>
<span data-ttu-id="00f75-119">Saman leyfa reitirnir **Sléttun** og **Margfeldi** þér að slétta gildi efnisnotkunar .</span><span class="sxs-lookup"><span data-stu-id="00f75-119">Together, the **Rounding up** and **Multiples** fields let you round up the material consumption value.</span></span> <span data-ttu-id="00f75-120">Til dæmis er hægt að slétta gildinu samkvæmt afgreiðslueiningu sem hráefni er tekin til fyrir framleiðslu.</span><span class="sxs-lookup"><span data-stu-id="00f75-120">For example, you can round up the value according to the handling unit in which the raw material is picked for production.</span></span> <span data-ttu-id="00f75-121">Eftirtaldir valkostir eru tiltækir í **Sléttun** svæði: **Magn**, **Mælingu**, og **Notkun**.</span><span class="sxs-lookup"><span data-stu-id="00f75-121">The following options are available in the **Rounding up** field: **Quantity**, **Measurement**, and **Consumption**.</span></span>

### <a name="quantity"></a><span data-ttu-id="00f75-122">Magn</span><span class="sxs-lookup"><span data-stu-id="00f75-122">Quantity</span></span>

<span data-ttu-id="00f75-123">Ef **Magn** er valið sem sléttunar mekanismi, verður magn að vera margfeldi af tilgreindu magni.</span><span class="sxs-lookup"><span data-stu-id="00f75-123">If you select **Quantity** as the rounding-up mechanism, the quantity must be a multiple of the specified quantity.</span></span> <span data-ttu-id="00f75-124">Til dæmis ef þörf er á heiltölum er **1** tilgreint í svæðinu **Margfeldi**.</span><span class="sxs-lookup"><span data-stu-id="00f75-124">For example, if whole numbers are required, select **1** in the **Multiples** field.</span></span> <span data-ttu-id="00f75-125">Tölur eru svo sléttað í magn sem má deila með 1.</span><span class="sxs-lookup"><span data-stu-id="00f75-125">Numbers are then rounded up to a quantity that is divisible by 1.</span></span>

### <a name="measurement"></a><span data-ttu-id="00f75-126">Mæling</span><span class="sxs-lookup"><span data-stu-id="00f75-126">Measurement</span></span>

<span data-ttu-id="00f75-127">Yfirleitt, veljið **Mælingu** sem mekanisma sléttunar þegar hráefni kemur í ákveðnum stærðum.</span><span class="sxs-lookup"><span data-stu-id="00f75-127">Typically, you select **Measurement** as the rounding-up mechanism when the raw material comes in specific dimensions.</span></span> <span data-ttu-id="00f75-128">Til dæmis er stykki af 2 metra málmröri krafist fyrir fullbúin framleiðsluvara og málmrörið er geymt í 4.5 metra lengdum.</span><span class="sxs-lookup"><span data-stu-id="00f75-128">For example, a piece of 2-meter metal tube is required for a finished good, and the metal tube is stored in 4.5-meter lengths.</span></span> <span data-ttu-id="00f75-129">Í þessu tilfelli má nota **Mælingu** mekanisma sléttunar til að reikna út hversu mörg málmrör þarf til að framleiða tiltekinn fjölda stykkja fullbúinnar framleiðsluvara.</span><span class="sxs-lookup"><span data-stu-id="00f75-129">In this case, the **Measurement** rounding-up mechanism can be used to calculate how many metal tubes are required to produce a specific number of pieces of the finished good.</span></span> <span data-ttu-id="00f75-130">Til dæmis hér, í **Formúlu** er stillt á **Hæð \* Fasti**.</span><span class="sxs-lookup"><span data-stu-id="00f75-130">For this example, the **Formula** field is set to **Height \* Constant**.</span></span> <span data-ttu-id="00f75-131">Í **Hæð** er stillt á **2** til að tilgreina lengd rörs sem er krafist fyrir fullbúin framleiðsluvara.</span><span class="sxs-lookup"><span data-stu-id="00f75-131">The **Height** field is set to **2** to indicate the length of the tube that is required for the finished good.</span></span> <span data-ttu-id="00f75-132">Í **margfeldi** er stillt á **4.5** til að tilgreina í rör er tekið til í lengdir 4.5 metra.</span><span class="sxs-lookup"><span data-stu-id="00f75-132">The **Multiple** field is set to **4.5** to indicate that the tube is picked in lengths of 4.5 meters.</span></span> <span data-ttu-id="00f75-133">Útreikningurinn er:</span><span class="sxs-lookup"><span data-stu-id="00f75-133">Here is the calculation:</span></span>

1.  <span data-ttu-id="00f75-134">Fjöldi margfelda sem er krafist fyrir 10 stykki af fullbúin framleiðsluvara: 10 ÷ 2 = 5 stykki</span><span class="sxs-lookup"><span data-stu-id="00f75-134">Number of multiples that are required for 10 pieces of the finished good: 10 ÷ 2 = 5 pieces</span></span>
2.  <span data-ttu-id="00f75-135">Samtals notkun:  4,5 × 5 = 22.5 metrar af málmröri</span><span class="sxs-lookup"><span data-stu-id="00f75-135">Total consumption:  4.5 × 5 = 22.5 meters of metal tube</span></span>

<span data-ttu-id="00f75-136">Gert er ráð fyrir að 0.5 metra af röri sé sett í rýrnun fyrir hver fimm stykki af rörum sem eru notaðar.</span><span class="sxs-lookup"><span data-stu-id="00f75-136">It's assumed that 0.5 meter of tube is scrapped for every five pieces of tube that are consumed.</span></span>

### <a name="consumption"></a><span data-ttu-id="00f75-137">Notkun</span><span class="sxs-lookup"><span data-stu-id="00f75-137">Consumption</span></span>

<span data-ttu-id="00f75-138">Yfirleitt, veljið **Notkun** sem mekanisma sléttunar þegar hráefni verður að vera tekið til í heilu magni tiltekinnar afgreiðslueiningar vöru.</span><span class="sxs-lookup"><span data-stu-id="00f75-138">Typically, you select **Consumption** as the rounding-up mechanism when raw material must be picked in whole quantities of a specific handling unit of the product.</span></span> <span data-ttu-id="00f75-139">Til dæmis er 2 fjórðungar af málningu notaðir til að framleiða einu stykki hinnar fullbúnu framleiðsluvara, og málning er tekið til í 25 fjórðungsdollum.</span><span class="sxs-lookup"><span data-stu-id="00f75-139">For example, 2 quarts of paint are used to produce one piece of a finished good, and the paint is picked in 25-quart cans.</span></span> <span data-ttu-id="00f75-140">Í þessu tilfelli er hægt að nota **Notkun** mekanisma sléttunar til að slétta notkun á heilar tölur fyrir 25 fjórðungsdollum.</span><span class="sxs-lookup"><span data-stu-id="00f75-140">In this case, the **Consumption** rounding-up mechanism can be used to round up consumption to whole numbers of 25-quart cans.</span></span> <span data-ttu-id="00f75-141">Hér er útreikningur fyrir magn málningar sem er krafist ef framleiða þarf 180 stykki fullbúinnar framleiðsluvara:</span><span class="sxs-lookup"><span data-stu-id="00f75-141">Here is the calculation for the amount of paint that is required if 180 pieces of the finished good must be produced:</span></span>

1.  <span data-ttu-id="00f75-142">Málning þarf án rýrnunar: 180 × 2 = 360 fjórðungar</span><span class="sxs-lookup"><span data-stu-id="00f75-142">Paint that is required, excluding scrap: 180 × 2 = 360 quarts</span></span>
2.  <span data-ttu-id="00f75-143">Fjöldi dósa: 360 ÷ 25 = 14.4 sem er sléttað að 15</span><span class="sxs-lookup"><span data-stu-id="00f75-143">Number of cans: 360 ÷ 25 = 14.4, which is rounded up to 15</span></span>
3.  <span data-ttu-id="00f75-144">Málning sem þarf án rýrnunar: 15 × 25 = 375 fjórðungar</span><span class="sxs-lookup"><span data-stu-id="00f75-144">Paint that is required, including scrap: 15 × 25 = 375 quarts</span></span>

## <a name="step-consumption"></a><span data-ttu-id="00f75-145">Skrefanotkun</span><span class="sxs-lookup"><span data-stu-id="00f75-145">Step consumption</span></span>
<span data-ttu-id="00f75-146">Skrefanotkun er notuð til að reikna út fastanotkun í magntímabilum.</span><span class="sxs-lookup"><span data-stu-id="00f75-146">Step consumption is used to calculate constant consumption in quantity intervals.</span></span> <span data-ttu-id="00f75-147">Ef þú velur **Skrefi notkun** í á **Formúlu** reit á í **Uppsetningu** flipa, er hægt að bæta upplýsingar um skref á í **Skrefanotkun** flipa. Fast notað magn er hægt að stilla í timabilum fyrir framleitt magn.</span><span class="sxs-lookup"><span data-stu-id="00f75-147">If you select **Step consumption** in the **Formula** field on the **Setup** tab, you can add information about the steps on the **Step consumption** tab. The fixed consumed quantity can be set up in intervals of the produced quantity.</span></span> <span data-ttu-id="00f75-148">Til dæmis er skrefanotkun sett upp eins og sýnt er í eftirfarandi töflu.</span><span class="sxs-lookup"><span data-stu-id="00f75-148">For example, step consumption is set up as shown in the following table.</span></span>

| <span data-ttu-id="00f75-149">Frá-röð</span><span class="sxs-lookup"><span data-stu-id="00f75-149">From series</span></span> | <span data-ttu-id="00f75-150">Magn</span><span class="sxs-lookup"><span data-stu-id="00f75-150">Quantity</span></span> |
|-------------|----------|
| <span data-ttu-id="00f75-151">0,00</span><span class="sxs-lookup"><span data-stu-id="00f75-151">0.00</span></span>        | <span data-ttu-id="00f75-152">10.0000</span><span class="sxs-lookup"><span data-stu-id="00f75-152">10.0000</span></span>  |
| <span data-ttu-id="00f75-153">100,00</span><span class="sxs-lookup"><span data-stu-id="00f75-153">100.00</span></span>      | <span data-ttu-id="00f75-154">20.0000</span><span class="sxs-lookup"><span data-stu-id="00f75-154">20.0000</span></span>  |
| <span data-ttu-id="00f75-155">200,00</span><span class="sxs-lookup"><span data-stu-id="00f75-155">200.00</span></span>      | <span data-ttu-id="00f75-156">40.0000</span><span class="sxs-lookup"><span data-stu-id="00f75-156">40.0000</span></span>  |

<span data-ttu-id="00f75-157">Magn uppskriftar (BOM) er 1 og framleiðslumagnið er 110.</span><span class="sxs-lookup"><span data-stu-id="00f75-157">The bill of materials (BOM) quantity is 1, and the production quantity is 110.</span></span> <span data-ttu-id="00f75-158">Formúla fyrir notkun er Úr röð (Magn) = Notkun.</span><span class="sxs-lookup"><span data-stu-id="00f75-158">The formula for the consumption is From series (Quantity) = Consumption.</span></span> <span data-ttu-id="00f75-159">Þar sem framleiðslumagns er 110 fellur það í "Úr 100 röð."</span><span class="sxs-lookup"><span data-stu-id="00f75-159">Because the production quantity is 110, it falls into the "From 100 series."</span></span> <span data-ttu-id="00f75-160">Þessvegna er magnið 20.</span><span class="sxs-lookup"><span data-stu-id="00f75-160">Therefore, the quantity is 20.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]