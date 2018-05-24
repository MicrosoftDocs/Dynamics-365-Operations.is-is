---
title: "Útreikningsaðferðir virðisaukaskatts í reitnum Uppruni"
description: "Þessi grein útskýrir valkosti á svæðinu Uppruni á síðunni vsk-kóðar og hvernig virðisaukaskattur er reiknaður á grundvelli þeirra valkosta sem ákveðnir eru fyrir virðisaukaskattskóða."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1473eeb2950296f5ae6250d7a53794af3d9cba81
ms.contentlocale: is-is
ms.lasthandoff: 05/08/2018

---

# <a name="sales-tax-calculation-methods-in-the-origin-field"></a><span data-ttu-id="4a772-103">Útreikningsaðferðir virðisaukaskatts í reitnum Uppruni</span><span class="sxs-lookup"><span data-stu-id="4a772-103">Sales tax calculation methods in the Origin field</span></span>

[!include [banner](../includes/banner.md)]

[!include [retail name](../includes/retail-name.md)]

<span data-ttu-id="4a772-104">Þessi grein útskýrir valkosti á svæðinu Uppruni á síðunni vsk-kóðar og hvernig virðisaukaskattur er reiknaður á grundvelli þeirra valkosta sem ákveðnir eru fyrir virðisaukaskattskóða.</span><span class="sxs-lookup"><span data-stu-id="4a772-104">This article explains the options in the Origin field on the sales tax codes page and how sales tax is calculated based on the selected option for a sales tax code.</span></span>

<span data-ttu-id="4a772-105">Fyrir hvern VSK-kóða sem stofnaður er á síðunni VSK-kóðar þarf að velja útreikningsaðferð sem notuð er á upphæð VSK-stofns í reitnum Uppruni.</span><span class="sxs-lookup"><span data-stu-id="4a772-105">For each sales tax code that you create in the Sales tax codes page, you must select the method of calculation to apply to the tax base amount in the Origin field.</span></span>

## <a name="percentage-of-net-amount"></a><span data-ttu-id="4a772-106">Prósenta af nettóupphæð</span><span class="sxs-lookup"><span data-stu-id="4a772-106">Percentage of net amount</span></span>
<span data-ttu-id="4a772-107">Prósenta af útreikningsaðferð nettóupphæðar er sjálfgefna gildið í reitnum Uppruna.</span><span class="sxs-lookup"><span data-stu-id="4a772-107">The Percentage of net amount calculation method is the default value in the Origin field.</span></span> <span data-ttu-id="4a772-108">Virðisaukaskatturinn er reiknaður sem prósenta af innkaupa- eða söluupphæð, án annarra virðisaukaskatta.</span><span class="sxs-lookup"><span data-stu-id="4a772-108">The sales tax is calculated as a percentage of the purchase or sales amount, excluding any other sales taxes.</span></span>
### <a name="example"></a><span data-ttu-id="4a772-109">Dæmi</span><span class="sxs-lookup"><span data-stu-id="4a772-109">Example</span></span>

<span data-ttu-id="4a772-110">Skatthlutfallið er 25%.</span><span class="sxs-lookup"><span data-stu-id="4a772-110">The tax rate is 25%.</span></span> <span data-ttu-id="4a772-111">Reikningslínan sýnir magn 10 vara sem kosta 1,00 hver og viðskiptavinurinn fær 10% línuafslátt.</span><span class="sxs-lookup"><span data-stu-id="4a772-111">The invoice line shows a quantity of 10 items at 1.00 each, and the customer is allowed a 10% line discount.</span></span> <span data-ttu-id="4a772-112">Nettóupphæð: (10 x 1,00) -10% = 9,00 VSK: 9,00 x 25% = Heildarupphæð 2,25: 9,00 + 2,25 = 11,25</span><span class="sxs-lookup"><span data-stu-id="4a772-112">Net amount: (10 x 1.00) -10% = 9.00 Sales tax: 9.00 x 25% = 2.25 Total amount: 9.00 + 2.25 = 11.25</span></span>

## <a name="percentage-of-gross-amount"></a><span data-ttu-id="4a772-113"> Prósenta af brúttó upphæð</span><span class="sxs-lookup"><span data-stu-id="4a772-113">Percentage of gross amount</span></span>
<span data-ttu-id="4a772-114">Ef valin er aðferðin Prósenta af brúttóupphæð er VSK reiknaður sem prósenta af brúttósöluupphæð.</span><span class="sxs-lookup"><span data-stu-id="4a772-114">If you select the Percentage of gross amount method, the sales tax is calculated as a percentage of the gross sales amount.</span></span> <span data-ttu-id="4a772-115">Brúttóupphæð er nettólínuupphæð plús allir skattar og gjöld línunnar, nema einn skattur með Uppruna = Prósenta af brúttóupphæð.</span><span class="sxs-lookup"><span data-stu-id="4a772-115">The gross amount is the line net amount plus all taxes and fees for the line except the one tax with Origin = Percentage of gross amount.</span></span>
### <a name="example"></a><span data-ttu-id="4a772-116">Dæmi</span><span class="sxs-lookup"><span data-stu-id="4a772-116">Example</span></span>

<span data-ttu-id="4a772-117">Skattyfirvöld hafa lagt sérstök gjöld á vöru.</span><span class="sxs-lookup"><span data-stu-id="4a772-117">The tax authority has imposed special duties on an item.</span></span> <span data-ttu-id="4a772-118">Upphæð gjaldanna er bætt við nettóupphæðina áður en virðisaukaskattur er reiknaður út.</span><span class="sxs-lookup"><span data-stu-id="4a772-118">The duty amounts are added to the net amount before sales tax is calculated.</span></span> <span data-ttu-id="4a772-119">Eftirfarandi VSK-kóðar eru gefnir:</span><span class="sxs-lookup"><span data-stu-id="4a772-119">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="4a772-120">Gjald 1 = 10%, notar útreikningsaðferð fyrir prósentu af nettóupphæð</span><span class="sxs-lookup"><span data-stu-id="4a772-120">DUTY 1 = 10%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="4a772-121">Gjald 2 = 20%, notar útreikningsaðferð fyrir prósentu af nettóupphæð</span><span class="sxs-lookup"><span data-stu-id="4a772-121">DUTY 2 = 20%, using the Percentage of net amount calculation method</span></span>
-   <span data-ttu-id="4a772-122">VSK = 25%, notar útreikningsaðferð fyrir prósentu af brúttóupphæð</span><span class="sxs-lookup"><span data-stu-id="4a772-122">SALESTAX = 25%, using the Percentage of gross amount calculation method</span></span>

<span data-ttu-id="4a772-123">Ef nettóupphæðin er 10,00 þá er Gjald 1 1,00 (10,00 x 10%) og Gjald 2 2,00 ( 10,00 x 20%).</span><span class="sxs-lookup"><span data-stu-id="4a772-123">If the net amount is 10.00, then DUTY 1 is 1.00 (10.00 x 10%) and DUTY 2 = 2.00 (10.00 x 20%).</span></span> <span data-ttu-id="4a772-124">Upphæðirnar yrðu eftirfarandi: Brúttóupphæð: Nettóupphæð + upphæð GJALD 1 + upphæð GJALD 2 (10,00 + 1,00 + 2,00) = 13,00 VSK = 13,00 x 25% = 3,25 Samtals GJÖLD og VSK: 1,00 + 2,00 + 3,25 = 6,25 Heildarupphæð: 10,00 + 6,25 = 16,25</span><span class="sxs-lookup"><span data-stu-id="4a772-124">The amounts would be as follows: Gross amount: Net amount + DUTY 1 amount + DUTY 2 amount (10.00 + 1.00 + 2.00) = 13.00 SALESTAX = 13.00 x 25% = 3.25 Total DUTIES and SALESTAX: 1.00 + 2.00 + 3.25 = 6.25 Total amount: 10.00 + 6.25 = 16.25</span></span>

| <span data-ttu-id="4a772-125">**Ábending**</span><span class="sxs-lookup"><span data-stu-id="4a772-125">**Note**</span></span>                                                                                                                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a772-126">Aðeins er hægt að nota einn VSK-kóða með Uppruna = Prósenta af brúttóupphæð fyrir færslu.</span><span class="sxs-lookup"><span data-stu-id="4a772-126">Only one tax code with Origin = Percentage of gross amount can be used for a transaction.</span></span> <span data-ttu-id="4a772-127">Ef fleiri en einn slíkur skattkóði er ákvarðaður fyrir færslu birtist villa um að ekki sé hægt að reikna út virðisaukaskatt.</span><span class="sxs-lookup"><span data-stu-id="4a772-127">If more than one such tax code is determined for a transaction an error will be displayed that sales tax cannot be calculated.</span></span> |


<a name="percentage-of-sales-tax"></a><span data-ttu-id="4a772-128">Prósenta af VSK</span><span class="sxs-lookup"><span data-stu-id="4a772-128">Percentage of sales tax</span></span>
-----------------------

<span data-ttu-id="4a772-129">Þegar Prósenta af virðisaukaskatti er valin í reitnum Uppruni er virðisaukaskattur reiknaður sem prósenta af virðisaukaskatti sem valinn er í reitnum VSK á VSK.</span><span class="sxs-lookup"><span data-stu-id="4a772-129">When you select Percentage of sales tax in the Origin field, sales tax is calculated as a percentage of the sales tax that is selected in the Sales tax on sales tax field.</span></span> <span data-ttu-id="4a772-130">Virðisaukaskattur sem er valinn í reitnum VSK á VSK er reiknaður fyrst.</span><span class="sxs-lookup"><span data-stu-id="4a772-130">The sales tax that is selected in the Sales tax on sales tax field is calculated first.</span></span> <span data-ttu-id="4a772-131">Seinni virðisaukaskatturinn er síðan reiknaður á grunni fyrri virðisaukaskattsins.</span><span class="sxs-lookup"><span data-stu-id="4a772-131">The second sales tax is then calculated based on the first sales tax amount.</span></span>
### <a name="example"></a><span data-ttu-id="4a772-132">Dæmi</span><span class="sxs-lookup"><span data-stu-id="4a772-132">Example</span></span>

<span data-ttu-id="4a772-133">Eftirfarandi VSK-kóðar eru gefnir:</span><span class="sxs-lookup"><span data-stu-id="4a772-133">Given the following sales tax codes:</span></span>
-   <span data-ttu-id="4a772-134">Gjald 1 = 10%, notar aðferð fyrir prósentu af nettóupphæð</span><span class="sxs-lookup"><span data-stu-id="4a772-134">DUTY 1 = 10%, using the Percentage of net amount method</span></span>
-   <span data-ttu-id="4a772-135">GJALD 2 = 20%, notar aðferð prósentu af vsk, með Gjald 1 í reitnum VSK á VSK</span><span class="sxs-lookup"><span data-stu-id="4a772-135">DUTY 2 = 20%, using the Percentage of sales tax method, with Duty 1 in the Sales tax on sales tax field</span></span>
-   <span data-ttu-id="4a772-136">VSK = 25%, notar aðferð fyrir prósentu af brúttóupphæð</span><span class="sxs-lookup"><span data-stu-id="4a772-136">SALESTAX = 25%, using the Percentage of gross amount method</span></span>

<span data-ttu-id="4a772-137">Nettóupphæð: 10,00 GJALD 1: 10,00 x 10% = 1,00 GJALDI 2: 1,00 x 20% = 0.20 Brúttóupphæð: 10,00 + 1,00 + 0,20 = 11,20 VSK: 11,20 x 25% = 2.80 Samtals GJÖLD og VSK: 1,00 + 0,20 + 2,80 = 4,00 Heildarupphæð: 10,00 + 4,00 = 14,00</span><span class="sxs-lookup"><span data-stu-id="4a772-137">Net amount: 10.00 DUTY 1: 10.00 x 10% = 1.00 DUTY 2: 1.00 x 20% = 0.20 Gross amount: 10.00 + 1.00 + 0.20 = 11.20 SALESTAX: 11.20 x 25% = 2.80 Total DUTIES and SALESTAX: 1.00 + 0.20 + 2.80 = 4.00 Total amount: 10.00 + 4.00 = 14.00</span></span>

| <span data-ttu-id="4a772-138">**Ábending**</span><span class="sxs-lookup"><span data-stu-id="4a772-138">**Note**</span></span>                                                                                                                                                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a772-139">Margstiga skattur í skattaútreikningum er ekki mögulegur.</span><span class="sxs-lookup"><span data-stu-id="4a772-139">Multilevel tax on tax calculations are not possible.</span></span> <span data-ttu-id="4a772-140">Ekki er hægt að reikna út skatt á grundvelli skatts sem þegar er reiknaður út frá öðrum skatti.</span><span class="sxs-lookup"><span data-stu-id="4a772-140">A tax cannot be calculated based on a tax which already is calculated based on another tax.</span></span> <span data-ttu-id="4a772-141">Hægt er að reikna marga eins stigs skatta í skattkóðum í færslu.</span><span class="sxs-lookup"><span data-stu-id="4a772-141">Multiple single level tax on tax codes can be calculated on a transaction.</span></span> |

## <a name="amount-per-unit"></a><span data-ttu-id="4a772-142"> Upphæð á einingu</span><span class="sxs-lookup"><span data-stu-id="4a772-142">Amount per unit</span></span>
<span data-ttu-id="4a772-143">Þegar Upphæð á einingu í er valin í reitnum Uppruni er virðisaukaskattur reiknaður sem föst upphæð á einingu margfaldað með magninu sem fært er inn í línuna.</span><span class="sxs-lookup"><span data-stu-id="4a772-143">When you select Amount per unit in the Origin field, sales tax is calculated as a fixed amount per unit multiplied with the quantity entered on the document line.</span></span> <span data-ttu-id="4a772-144">Velja skal einingu í reitnum Eining.</span><span class="sxs-lookup"><span data-stu-id="4a772-144">A unit has to be selected in the Unit field.</span></span> <span data-ttu-id="4a772-145">Upphæð á einingu er tilgreind á síðunni Gildi VSK-kóða.</span><span class="sxs-lookup"><span data-stu-id="4a772-145">The amount per unit is specified in the Sales tax code values page.</span></span>
### <a name="example"></a><span data-ttu-id="4a772-146">Dæmi</span><span class="sxs-lookup"><span data-stu-id="4a772-146">Example</span></span>

<span data-ttu-id="4a772-147">Vsk-kóðinn er settur upp sem: 1,20 USD á hverja einingu = kassi Á sölureikningslínu 25 kassar af vöru eru seldir VSK er reiknaður sem 25 x 1,20 = 30,00</span><span class="sxs-lookup"><span data-stu-id="4a772-147">Sales tax code is set up as: USD 1.20 per unit = box On a sales invoice line 25 boxes of an item are sold Sales tax is calculated as 25 x 1.20 = 30.00</span></span>

| <span data-ttu-id="4a772-148">**Ábending**</span><span class="sxs-lookup"><span data-stu-id="4a772-148">**Note**</span></span>                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a772-149">Ef færslan er færð inn í aðra einingu en einingu sem er tilgreind á VSK-kóða, umreiknast hún sjálfkrafa á grundvelli einingaumreikninga sem eru settir upp á síðunni Umreikningur eininga.</span><span class="sxs-lookup"><span data-stu-id="4a772-149">If the transaction is entered in different unit than the unit specified on the sales tax code, it is converted automatically based on the unit conversions that are set up in the Unit conversions page.</span></span> |

###  <a name="amount-per-unit-additional-option"></a><span data-ttu-id="4a772-150"> Upphæð á einingu, viðbótarvalkostur</span><span class="sxs-lookup"><span data-stu-id="4a772-150">Amount per unit, additional option</span></span>

<span data-ttu-id="4a772-151">Á flipanum Útreikningur er hægt að velja hvort reiknaður skattur á upphæð á einingu er reiknaður út á undan öðrum vsk-kóða og bætt við nettóupphæðina áður en aðrir VSK-kóðar með Uppruna = Prósenta af nettóupphæð eru reiknaðir.</span><span class="sxs-lookup"><span data-stu-id="4a772-151">On the Calculation tab, you can select whether an amount per unit calculated tax is calculated before other tax codes and added to the net amount before other tax codes with Origin = Percentage of net amount are calculated.</span></span>

### <a name="examples"></a><span data-ttu-id="4a772-152">Dæmi</span><span class="sxs-lookup"><span data-stu-id="4a772-152">Examples</span></span>

<span data-ttu-id="4a772-153">Gerum ráð fyrir að við reiknum 2 skattkóða á færslu:</span><span class="sxs-lookup"><span data-stu-id="4a772-153">Assume we calculate 2 tax codes on a transaction:</span></span>

-   <span data-ttu-id="4a772-154">GJALD: Uppruni = Upphæð á einingu og virðisaukaskatt, gildi er stillt á 5,00 á einingu = stykki</span><span class="sxs-lookup"><span data-stu-id="4a772-154">DUTY: Origin = Amount per unit and a sales tax, the value is set to 5.00 per unit = pcs</span></span>
-   <span data-ttu-id="4a772-155">VSK: Uppruni = eins og sýnt er í dæmunum hér að neðan, gildi er stillt á 25%</span><span class="sxs-lookup"><span data-stu-id="4a772-155">SALESTAX: Origin = as shown in the examples below, the value is set to 25%</span></span>

<span data-ttu-id="4a772-156">Við seljum 1 stykki af vöru á einingaverðinu 10,00</span><span class="sxs-lookup"><span data-stu-id="4a772-156">We sell 1 piece of an item at a unit price of 10.00</span></span>
#### <a name="example-1"></a><span data-ttu-id="4a772-157">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="4a772-157">Example 1</span></span>

<span data-ttu-id="4a772-158">VSK: Uppruni = Prósenta af brúttóupphæð aðferð Valkosturinn Reikna út á undan VSK hefur engin áhrif, þar sem VSK er reiknaður sem prósenta af brúttóupphæð.</span><span class="sxs-lookup"><span data-stu-id="4a772-158">SALESTAX: Origin = Percentage of gross amount method The Calculate before sales tax option has no effect, because SALESTAX is calculated as a percentage of the gross amount.</span></span> <span data-ttu-id="4a772-159">GJALD: 1 x 5,00 = 5,00 brúttóupphæð: 10,00 + 5,00 = 15,00 VSK: 15,00 x 25% = 3,75 Heildarupphæð virðisaukaskatts: 5,00 + 3,75 = 8,75 Heildarupphæð: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="4a772-159">DUTY: 1 x 5.00 = 5.00 Gross amount: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-2"></a><span data-ttu-id="4a772-160">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="4a772-160">Example 2</span></span>

<span data-ttu-id="4a772-161">VSK: Uppruni = Prósenta af nettóupphæð Valkosturinn Reikna út á undan VSK er ekki valinn fyrir útreikning á GJALDI.</span><span class="sxs-lookup"><span data-stu-id="4a772-161">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is not selected for the DUTY calculation.</span></span> <span data-ttu-id="4a772-162">Nettóupphæð: 10,00 GJALD: 1 x 5,00 = 5,00 VSK: 10,00 x 25% = 2,50 Heildarupphæð virðisaukaskatts: 5,00 + 2,50 = 7,50 Heildarupphæð: 10,00 + 7,50 = 17,50</span><span class="sxs-lookup"><span data-stu-id="4a772-162">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: 10.00 x 25% = 2.50 Total sales tax: 5.00 + 2.50 = 7.50 Total amount: 10.00 + 7.50 = 17.50</span></span>

#### <a name="example-3"></a><span data-ttu-id="4a772-163">Dæmi 3</span><span class="sxs-lookup"><span data-stu-id="4a772-163">Example 3</span></span>

<span data-ttu-id="4a772-164">VSK: Uppruni = Prósenta af nettóupphæð Valkosturinn Reikna út á undan VSK er ekki valinn fyrir útreikning á GJALDI.</span><span class="sxs-lookup"><span data-stu-id="4a772-164">SALESTAX: Origin = Percentage of net amount The Calculate before sales tax option is selected for the DUTY calculation.</span></span> <span data-ttu-id="4a772-165">Nettóupphæð: 10,00 GJALD: 1 x 5,00 = 5,00 VSK: (10,00 + 5,00) x 25% = 3,75 Heildarupphæð virðisaukaskatts: 5,00 + 3,75 = 8,75 Heildarupphæð: 10,00 + 8,75 = 18,75</span><span class="sxs-lookup"><span data-stu-id="4a772-165">Net amount: 10.00 DUTY: 1 x 5.00 = 5.00 SALESTAX: (10.00 + 5.00) x 25% = 3.75 Total sales tax: 5.00 + 3.75 = 8.75 Total amount: 10.00 + 8.75 = 18.75</span></span>

#### <a name="example-4"></a><span data-ttu-id="4a772-166">Dæmi 4</span><span class="sxs-lookup"><span data-stu-id="4a772-166">Example 4</span></span>

<span data-ttu-id="4a772-167">Niðurstaðan úr dæmi 3 og dæmi 1 er sú sama, þar sem aðeins er um eitt gjald að ræða.</span><span class="sxs-lookup"><span data-stu-id="4a772-167">The result of Example 3 and Example 1 is the same, because there is only one duty.</span></span> <span data-ttu-id="4a772-168">Gefum okkur að greiða þurfi tvenns konar GJÖLD og aðeins önnur þeirra eru með í nettóupphæð fyrir útreikning vsk: GJALD 1: 5,00 með Upphæð á hverja einingu aðferð og reikna það Út áður en vsk-valkosturinn er valinn GJALDI 2: 2,50 með Upphæð á hverja einingu aðferð og reikna það Út áður en vsk-valkosturinn er ekki valinn vsk : 25%, með því að nota Prósentu af nettó upphæð nettóupphæð aðferð: 10,00 GJALD 1: 1 x 5,00 = 5,00 GJALD 2: 1 x 2,50 = 2,50 nettóupphæð skatts: 10,00 + 5,00 = 15,00 SALESTAX: 15,00 x 25% = 3.75 Samtals virðisaukaskatt, þ.m.t. gjöld: 5,00 + 2,50 + 3,75 = 11,25 heildarupphæð: 10,00 + 11,25 = 21,25 25% SALESTAX er reiknað út fyrir samtöluna af nettóupphæðinni (10,00) + GJALD 1 (5,00) = 15,00.</span><span class="sxs-lookup"><span data-stu-id="4a772-168">Assume that you have two DUTIES, and only one of them is included in the net amount for the sales tax calculation: DUTY 1: 5.00, using the Amount per unit method, and the Calculate before sales tax option is selected DUTY 2: 2.50, using the Amount per unit method, and the Calculate before sales tax option is not selected Sales tax: 25%, using the Percentage of net amount method Net amount: 10.00 DUTY 1: 1 x 5.00 = 5.00 DUTY 2: 1 x 2.50 = 2.50 Net amount subject to sales tax: 10.00 + 5.00 = 15.00 SALESTAX: 15.00 x 25% = 3.75 Total sales taxes, including duties: 5.00 + 2.50 + 3.75 = 11.25 Total amount: 10.00 + 11.25 = 21.25 The 25% SALESTAX is calculated for the sum of the net amount (10.00) + DUTY 1 (5.00) = 15.00.</span></span> <span data-ttu-id="4a772-169">Gjaldi 2 er bætt við skattupphæðina eftir að virðisaukaskatturinn hefur verið reiknaður út.</span><span class="sxs-lookup"><span data-stu-id="4a772-169">DUTY 2 is added to the tax amount after the sales tax is calculated.</span></span>

## <a name="calculated-percentage-of-net-amount"></a><span data-ttu-id="4a772-170"> Reiknuð prósenta af nettóupphæð</span><span class="sxs-lookup"><span data-stu-id="4a772-170">Calculated percentage of net amount</span></span>
<span data-ttu-id="4a772-171">Reiknuð prósenta af nettóupphæð meðhöndlar skattaútreikninga á annan hátt allt eftir stillingu færibreytunnar Upphæðir innihalda vsk fyrir skjalið eða færslubókina.</span><span class="sxs-lookup"><span data-stu-id="4a772-171">The Calculated percentage of net amount handles tax calculation differently depending on the setting of the Amounts include sales tax parameter for the document or journal.</span></span>
### <a name="example-1"></a><span data-ttu-id="4a772-172">Dæmi 1</span><span class="sxs-lookup"><span data-stu-id="4a772-172">Example 1</span></span>

<span data-ttu-id="4a772-173">Skjal / færslubók er stillt á Upphæðir með virðisaukaskatti = Já Færslulínuupphæð: 10,00 Skatthlutfall: 25% Virðisaukaskattur: færslulínuupphæðin x skatthlutf (10,00 x 25%) = 2,50 Grunnupphæð (upphæð uppruna): Færslulínuupphæð - Vsk (10,00-2,50) = 7,50</span><span class="sxs-lookup"><span data-stu-id="4a772-173">Document / journal is set to Amounts include sales tax = Yes Transaction line amount: 10.00 Tax rate: 25% Sales tax: Transaction line amount x tax rate (10.00 x 25%) = 2.50 Tax base amount (origin amount): Transaction line amount - Sales tax (10.00 - 2.50) = 7.50</span></span>

### <a name="example-2"></a><span data-ttu-id="4a772-174">Dæmi 2</span><span class="sxs-lookup"><span data-stu-id="4a772-174">Example 2</span></span>

<span data-ttu-id="4a772-175">Skjal / færslubók er stillt á Upphæðir með virðisaukaskatti = Nei Færslulínuupphæð: 10,00 Skatthlutfall: 25% Virðisaukaskattur: (Færslulínuupphæð x Skatthlutf) / (100 - skatthlutfall) (10,00 x 25%) / (100% - 25%) = 3,33 Grunnupphæð (upphæð uppruna): færslulínuupphæð = 10,00</span><span class="sxs-lookup"><span data-stu-id="4a772-175">Document / journal is set to Amounts include sales tax = No Transaction line amount: 10.00 Tax rate: 25% Sales tax: (Transaction line amount x tax rate) / (100 - tax rate) (10.00 x 25%) / (100% - 25%) = 3.33 Tax base amount (origin amount): Transaction line amount = 10.00</span></span>



<a name="additional-resources"></a><span data-ttu-id="4a772-176">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4a772-176">Additional resources</span></span>
--------

[<span data-ttu-id="4a772-177">Ákvarða skatthlutfall virðisaukaskatts á grundvelli reitanna Jaðargrunnur og Útreikningsaðferð</span><span class="sxs-lookup"><span data-stu-id="4a772-177">Determining sale tax rates based on the Marginal base and Calculation method fields</span></span>](marginal-base-field.md)

[<span data-ttu-id="4a772-178">Útreikningsaðferð heildarupphæðar og tímabils fyrir vsk-kóða</span><span class="sxs-lookup"><span data-stu-id="4a772-178">Whole amount and Interval calculation options for sales tax codes</span></span>](whole-amount-interval-options-sales-tax-codes.md)




