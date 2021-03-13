---
title: Línuskilgreiningar í fjárhagsskýrsluhönnuði
description: Línuskilgreining er skýrsluhluti, eða eining sem tilgreinir efni hverrar raðar í fjárhagsskýrslu.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: kfend
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 274fa4bd137407c504f74335291e4c8e7999625b
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093266"
---
# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="b1a0d-103">Línuskilgreiningar í fjárhagsskýrsluhönnuði</span><span class="sxs-lookup"><span data-stu-id="b1a0d-103">Row definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1a0d-104">Línuskilgreining er skýrsluhluti, eða eining sem tilgreinir efni hverrar raðar í fjárhagsskýrslu.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-104">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="b1a0d-105">Línuskilgreiningu er hægt að sameina með dálkaskilgreiningum, skipuritsskilgreiningum og skýrsluskilgreiningum til að stofna einingahóp sem mörg fyrirtæki geta notað.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-105">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

## <a name="create-a-row-definition"></a><span data-ttu-id="b1a0d-106">Línuskilgreining stofnuð</span><span class="sxs-lookup"><span data-stu-id="b1a0d-106">Create a row definition</span></span>

1. <span data-ttu-id="b1a0d-107">Í Report Designer á yfirlitssvæðinu skal smella á **Línuskilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-107">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="b1a0d-108">Á **Skrá** smellið á **Nýtt** og síðan **Línuskilgreining**.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-108">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="b1a0d-109">Frekari upplýsingar um innihald hvers hólfs eru í [Breyta hólfum línuskilgreiningar](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="b1a0d-109">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="b1a0d-110">Línuskilgreining opnuð</span><span class="sxs-lookup"><span data-stu-id="b1a0d-110">Open a row definition</span></span>
1. <span data-ttu-id="b1a0d-111">Í Report Designer á yfirlitssvæðinu skal smella á **Línuskilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-111">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="b1a0d-112">Tvísmellið á heiti línuskilgreiningarinnar sem á að opna.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-112">Double-click the name of the row definition to open.</span></span>
3. <span data-ttu-id="b1a0d-113">Hægrismellið á línuskilgreiningu og veljið **Tengingar** til að skoða allar einingar sem tengjast línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-113">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="b1a0d-114">Innihald línuskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="b1a0d-114">Contents of a row definition</span></span>
<span data-ttu-id="b1a0d-115">Línuskilgreining getur innihaldið allt að 20.000 fjárhagsvíddaarlínur og haft eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="b1a0d-115">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

- <span data-ttu-id="b1a0d-116">Lýsandi texti sem bætir merkingu við skýrsluna með því að stofna hlutafyrirsagnir, línur og bil, s.s. **Reiðufé** eða **Heildartekjur**</span><span class="sxs-lookup"><span data-stu-id="b1a0d-116">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
- <span data-ttu-id="b1a0d-117">Tenglar í fjárhagsgögn, sem geta innihaldið víddargildi í Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="b1a0d-117">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 Finance</span></span>

    > [!NOTE]
    > <span data-ttu-id="b1a0d-118">Setja má upp línuskilgreiningu til að sækja gögn úr fjárhagsvíddarkerfinu í hvert sinn sem skýrslan er mynduð.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-118">You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>

- <span data-ttu-id="b1a0d-119">Samtölur línu og formúlur eru byggð á tengdum fjárhagsgögnum</span><span class="sxs-lookup"><span data-stu-id="b1a0d-119">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="b1a0d-120">Yfirleitt inniheldur hver lína í línuskilgreiningu eina af eftirfarandi tegundum upplýsinga:</span><span class="sxs-lookup"><span data-stu-id="b1a0d-120">Usually, each row in a row definition contains one of the following types of information:</span></span>

- <span data-ttu-id="b1a0d-121">Tilvísanir í fjárhagsvíddarkerfinu</span><span class="sxs-lookup"><span data-stu-id="b1a0d-121">References to the financial dimensions system</span></span>
- <span data-ttu-id="b1a0d-122">Samtölur eða útreikningar sem byggjast á gögnunum</span><span class="sxs-lookup"><span data-stu-id="b1a0d-122">Totals or calculations that are based on the data</span></span>
- <span data-ttu-id="b1a0d-123">Sníða</span><span class="sxs-lookup"><span data-stu-id="b1a0d-123">Formatting</span></span>

<span data-ttu-id="b1a0d-124">Tvær leiðir eru til að slá inn upplýsingar í línuskilgreiningu:</span><span class="sxs-lookup"><span data-stu-id="b1a0d-124">There are two methods for entering information in a row definition:</span></span>

- <span data-ttu-id="b1a0d-125">Færa handvirkt inn upplýsingar um línu í nýju línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-125">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="b1a0d-126">Frekari upplýsingar sjá [Breyta hólfum línuskilgreiningar](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="b1a0d-126">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
- <span data-ttu-id="b1a0d-127">Nota Report Designer til að sækja línuupplýsingar beint úr fjárhagsvíddum.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-127">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="b1a0d-128">Nánari upplýsingar er að finna í hlutanum "Tengdar línur/formúlur/einingar" í [Breyta reitum skilgreiningar línu](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="b1a0d-128">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="b1a0d-129">Víddum bætt við línuskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="b1a0d-129">Add dimensions in a row definition</span></span>
<span data-ttu-id="b1a0d-130">Vídd er skurðpunktur gagna og gilda.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-130">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="b1a0d-131">Hægt er að taka saman gögn og gildi í Report Designer.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-131">You can group data and values in report designer.</span></span> <span data-ttu-id="b1a0d-132">Svo er hægt að flokka og greina færslur nánar.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-132">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="b1a0d-133">Hægt er að nota svargluggann **Setja inn línur úr víddum** til að bæta mörgum línuskilgreiningum við samtímis.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-133">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="b1a0d-134">Svarglugginn birtir einn dálk fyrir hverja vídd.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-134">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="b1a0d-135">Eftirfarandi tafla lýsir upplýsingunum sem hægt er að tilgreina fyrir hverja vídd.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-135">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="b1a0d-136">Valkostur</span><span class="sxs-lookup"><span data-stu-id="b1a0d-136">Option</span></span>                | <span data-ttu-id="b1a0d-137">Lýsing</span><span class="sxs-lookup"><span data-stu-id="b1a0d-137">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="b1a0d-138">Vídd</span><span class="sxs-lookup"><span data-stu-id="b1a0d-138">Dimension</span></span>             | <span data-ttu-id="b1a0d-139">Mynstrið sem auðkennir víddina sem bæta á við línuskilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-139">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="b1a0d-140">Þetta mynstur inniheldur eitt og-merki (&) eða númeratákn (\#) fyrir hverja stöðu í víddunum.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-140">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="b1a0d-141">Almennt skal nota allar gæsalappir fyrir víddir aðallykils og öll tákn fyrir aðrar víddir.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-141">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="b1a0d-142">Upphaf víddasviðs</span><span class="sxs-lookup"><span data-stu-id="b1a0d-142">Dimension Range Start</span></span> | <span data-ttu-id="b1a0d-143">Fyrsta gildið fyrir þessa vídd sem bæta á við línuskilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-143">The first value for this dimension to add to the row definition.</span></span> |
| <span data-ttu-id="b1a0d-144">Lok víddasviðs</span><span class="sxs-lookup"><span data-stu-id="b1a0d-144">Dimension Range End</span></span>   | <span data-ttu-id="b1a0d-145">Síðasta gildið fyrir þessa vídd sem bæta á við línuskilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-145">The last value for this dimension to add to the row definition.</span></span> |

<span data-ttu-id="b1a0d-146">Til að bæta víddum við línuskilgreiningu skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-146">To add dimensions to a row definition, follow these steps.</span></span>

1. <span data-ttu-id="b1a0d-147">Report Designer smellt **Línuskilgreiningar**, og opnið síðan línuskilgreiningu til að breyta.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-147">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="b1a0d-148">Á valmyndinni **Breyta** er smellt á **Setja inn línur úr víddum**.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-148">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="b1a0d-149">Í **Setja inn Línur úr Víddir** í svarglugganum, í **Víddir** línunni skal velja hólfið fyrir víddina sem á að flytja í línuskilgreininguna og smella síðan á **Öll &&&**.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-149">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4. <span data-ttu-id="b1a0d-150">Til að takmarka línuskilgreiningar við ákveðin víddargildi skal slá inn upphafsvíddargildi í **Upphafs víddarsviðs** reitinn og slá svo inn lokavíddargildið í **Lok víddarsviðs** reitinn.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-150">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="b1a0d-151">Ef taka á öll gildi fyrir völdu víddirnar með skal hafa þessi hólf auð.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-151">To include all values for the selected dimension, leave these cells empty.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b1a0d-152">Algildisstafir (\* eða ?) í víddarsviðum skila ekki endilega öllum niðurstöðum sem óskað er, eftir því hvernig ERP gagnagrunnurinn safnar gögnum.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-152">Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>

5. <span data-ttu-id="b1a0d-153">Í **Kóði upphafslínu** svæðið skal tilgreina línukóða fyrir fyrsta víddargildi sem á að bæta við línuskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-153">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6. <span data-ttu-id="b1a0d-154">Í **Auka stig hverrar línu með** svæðið skal tilgreina bilið á milli samfelldra línukóða.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-154">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="b1a0d-155">Til dæmis, ef kóði fyrstu línu er 100 og stigvaxandi gildi er 30, hafa fyrstu nýju línurnar kóðana 100 130, 160, 190 og 220.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-155">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="b1a0d-156">Notið stigvaxandi gildi sem veitir nægt bil fyrir innsetningu nýs sniðs og formúlulínur.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-156">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7. <span data-ttu-id="b1a0d-157">Smelltu á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-157">Click **OK**.</span></span> <span data-ttu-id="b1a0d-158">Einni línu er bætt við línuskilgreininguna fyrir hvert valið víddargildi.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-158">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="b1a0d-159">Sléttun stillt í línuskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="b1a0d-159">Adjust rounding in a row definition</span></span>
<span data-ttu-id="b1a0d-160">Fyrir efnahagsreikninga þar sem upphæðir eru sléttaðar er ekki víst að samtölur stemmi.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-160">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="b1a0d-161">Þetta getur t.d. átt sér stað þegar sléttunarvalkosturinn er notaður efnahagsreikningsskýrslu og skýrsluskilgreining tilgreinir einnig sléttun.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-161">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="b1a0d-162">Hægt er að nota **Sléttunarleiðrétting** valkostinn í línuskilgreiningu til að leiðrétta upphæðir í efnahagsreikningnum.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-162">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="b1a0d-163">Hægt er að slökkva á sléttun eða breyta henni í flipanum **Stillingar** í skýrsluskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-163">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="b1a0d-164">Eftirfarandi tafla sýnir hvernig upphæðirnar eru sléttaðar.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-164">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="b1a0d-165">Í þessari töflu eru samtölur línanna 100 og 200 mismunandi þegar kveikt er á sléttun.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-165">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="b1a0d-166">Línukóði</span><span class="sxs-lookup"><span data-stu-id="b1a0d-166">Row code</span></span> | <span data-ttu-id="b1a0d-167">Upphæðir án sléttunar</span><span class="sxs-lookup"><span data-stu-id="b1a0d-167">Amounts without rounding</span></span> | <span data-ttu-id="b1a0d-168">Upphæð með sléttun að heilum þúsundum</span><span class="sxs-lookup"><span data-stu-id="b1a0d-168">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="b1a0d-169">100</span><span class="sxs-lookup"><span data-stu-id="b1a0d-169">100</span></span>      | <span data-ttu-id="b1a0d-170">3,600</span><span class="sxs-lookup"><span data-stu-id="b1a0d-170">3,600</span></span>                    | <span data-ttu-id="b1a0d-171">4</span><span class="sxs-lookup"><span data-stu-id="b1a0d-171">4</span></span>                                       |
| <span data-ttu-id="b1a0d-172">200</span><span class="sxs-lookup"><span data-stu-id="b1a0d-172">200</span></span>      | <span data-ttu-id="b1a0d-173">3,700</span><span class="sxs-lookup"><span data-stu-id="b1a0d-173">3,700</span></span>                    | <span data-ttu-id="b1a0d-174">4</span><span class="sxs-lookup"><span data-stu-id="b1a0d-174">4</span></span>                                       |
| <span data-ttu-id="b1a0d-175">Samtals</span><span class="sxs-lookup"><span data-stu-id="b1a0d-175">Total</span></span>    | <span data-ttu-id="b1a0d-176">7,300</span><span class="sxs-lookup"><span data-stu-id="b1a0d-176">7,300</span></span>                    | <span data-ttu-id="b1a0d-177">8</span><span class="sxs-lookup"><span data-stu-id="b1a0d-177">8</span></span>                                       |

<span data-ttu-id="b1a0d-178">Til að leiðrétta sléttun í efnahagsreikningi skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-178">To adjust rounding in a balance sheet, follow these steps.</span></span>

1. <span data-ttu-id="b1a0d-179">Smellið á **Línuskilgreiningar** í Skýrsluhönnun og opnið svo línuskilgreininguna sem á að breyta.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-179">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="b1a0d-180">Á valmyndinni **Breyta** er smellt á **Sléttunarleiðrétting**.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-180">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3. <span data-ttu-id="b1a0d-181">Í svarglugganum **Sléttunarleiðréttingar** eru eftirfarandi gildi færð inn:</span><span class="sxs-lookup"><span data-stu-id="b1a0d-181">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>

    - <span data-ttu-id="b1a0d-182">**Sléttunarleiðréttingarlína** – Línukóðinn fyrir línuna sem ætti að leiðrétta til að jafna efnahagsreikninginn.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-182">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    - <span data-ttu-id="b1a0d-183">**Samtölulína eigna** – Línukóðinn fyrir línuna í efnahagsreikningnum sem inniheldur heildareignir.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-183">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    - <span data-ttu-id="b1a0d-184">**Samtölulína skulda og eigin fjár** – Línukóðinn fyrir línuna í efnahagsreikningnum sem inniheldur skuldir og eigið fé samtals.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-184">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    - <span data-ttu-id="b1a0d-185">**Takmörk leiðréttingarupphæðar** – Jákvæð, heiltala sem tilgreinir takmörkun sjálfvirkrar leiðréttingar.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-185">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="b1a0d-186">Þessi upphæð er borin saman við raungildi raunverulegs sléttunarmismunar.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-186">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b1a0d-187">Tengja verður þessa línukóða við fjárhagsgögn notanda.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-187">These row codes must be linked to your financial data.</span></span> <span data-ttu-id="b1a0d-188">Með öðrum orðum, línan verður að hafa víddargildi í hólfinu **Tengill í fjárhagsvíddir**.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-188">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="b1a0d-189">**Ekki** vísa til lýsingar (**DESC**), reiknaðrar (**CALC**), eða samtölulínu (**TOT**).</span><span class="sxs-lookup"><span data-stu-id="b1a0d-189">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="b1a0d-190">Upphæðir í efnahagsreikningi verða nú jafnaðar jafnt þegar kveikt er á sléttun.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-190">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="b1a0d-191">Takmörkun leiðréttingar er beitt út frá valkostinum **Sléttunarnákvæmni** sem er tilgreindur fyrir skýrsluskilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-191">The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="b1a0d-192">Til dæmis, ef að slétta á skýrsluna í þúsundum og færa inn **2** í **Takmörk leiðréttingarupphæðar** reitnum birtist viðvörun þegar gildið í **Sléttunarleiðréttingarlína** reitnum hækkar eða lækkar um meira en 2.000.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-192">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="b1a0d-193">Lína og dálktexti sniðin</span><span class="sxs-lookup"><span data-stu-id="b1a0d-193">Format row and column text</span></span>
<span data-ttu-id="b1a0d-194">Breyta má útliti skýrslna með því að breyta leturgerðum og sníða texta.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-194">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="b1a0d-195">Eftirfarandi hlutar útskýra hvernig á að sníða útliti lína og dálka í skýrslum.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-195">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="b1a0d-196">Vinna með leturstíla</span><span class="sxs-lookup"><span data-stu-id="b1a0d-196">Manage font styles</span></span>

<span data-ttu-id="b1a0d-197">Hægt er að stofna og breyta leturstílum fyrir skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-197">You can create and modify font styles for your report.</span></span> <span data-ttu-id="b1a0d-198">Svo er hægt að nota þá stíla í skjalinu, eða á tiltekna röð eða dálki í skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-198">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="b1a0d-199"><strong>Leturstíll stofnaður</strong></span><span class="sxs-lookup"><span data-stu-id="b1a0d-199"><strong>Create a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="b1a0d-200">Á valmyndinni <strong>Snið</strong> í Skýrsluhönnun er smellt á <strong>Stílar og snið</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-200">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="b1a0d-201">Í <strong>Stílar og snið</strong> svarglugganum skal smella á <strong>Nýtt</strong> og færa inn einkvæmt heiti fyrir nýja stílinn.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-201">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="b1a0d-202">Veljið leturgerðir og smellið síðan á <strong>Í lagi</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-202">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="b1a0d-203"><strong>Leturstíl breytt</strong></span><span class="sxs-lookup"><span data-stu-id="b1a0d-203"><strong>Modify a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="b1a0d-204">Á valmyndinni <strong>Snið</strong> í Skýrsluhönnun er smellt á <strong>Stílar og snið</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-204">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="b1a0d-205">Í <strong>Stílar og snið</strong> svarglugganum skal velja stíl sem á að breyta og smella svo á <strong>Breyta</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-205">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="b1a0d-206">Veljið leturgerðir og smellið síðan á <strong>Í lagi</strong>.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-206">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="b1a0d-207"><strong>Leturstíll notaður</strong></span><span class="sxs-lookup"><span data-stu-id="b1a0d-207"><strong>Apply a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="b1a0d-208">Í Report Designer, í skilgreiningu eða dálkskilgreining eða í hausum og fótum, skal velja einn eða fleiri reit.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-208">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="b1a0d-209">Í listanum <strong>Stíll</strong> á tækjastikunni er valinn leturstíll.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-209">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="b1a0d-210">Snið texta í línum</span><span class="sxs-lookup"><span data-stu-id="b1a0d-210">Format row text</span></span>

<span data-ttu-id="b1a0d-211">Sniðið sem er tilgreint í línuskilgreiningunni hnekkir öllum sniðum sem eru tilgreind í dálkskilgreiningu og skýrsluskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-211">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="b1a0d-212">Hægt er að breyta textasniðinu með því að nota stýringarnar á sniðstikunni.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-212">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="b1a0d-213">Stýringarnar eru hefðbundnar Microsoft Windows stýringar.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-213">These controls are standard Microsoft Windows controls.</span></span>

1. <span data-ttu-id="b1a0d-214">Opnið skilgreiningu raðar í Report Designer til að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-214">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="b1a0d-215">Veljið hólfin sem á að sníða.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-215">Select the cells to format.</span></span> <span data-ttu-id="b1a0d-216">Til að velja fleiri en eitt hólf skal halda Ctrl-lyklinum niðri um leið og hólfin eru valin.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-216">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3. <span data-ttu-id="b1a0d-217">Smellið á tækjastikuhnapp sniðsins sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-217">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="b1a0d-218">Til að draga t.d. inn línu skal velja línuna og smella á **Auka inndrátt** ![Auka inndrátt](media/indent.gif "Auka inndrátt") á tækjastikunni.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-218">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](media/indent.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="b1a0d-219">Stilling dálka við hönnun skýrslna</span><span class="sxs-lookup"><span data-stu-id="b1a0d-219">Adjust columns while you design reports</span></span>

<span data-ttu-id="b1a0d-220">Til að auðvelda að skoða dálka sem er unnið er með í línuskilgreiningu er hægt að stilla breidd dálks og fela (minnka) eða sýna dálka á skoðunarsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-220">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="b1a0d-221">Allar breytingar sem gerðar hafa aðeins áhrif á útliti dálkanna á skjánum.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-221">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="b1a0d-222">Þær hafa ekki áhrif á snið dálkanna í skýrslum.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-222">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="b1a0d-223">Breidd dálks á skoðunarsvæði breytt</span><span class="sxs-lookup"><span data-stu-id="b1a0d-223">Change the width of a column in the view pane</span></span>

1. <span data-ttu-id="b1a0d-224">Opnið skilgreiningu raðar í Skýrsluhönnun til að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-224">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="b1a0d-225">Á valmyndinni **Snið** skal velja **Dálkbreidd**.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-225">On the **Format** menu, select **Column Width**.</span></span>
3. <span data-ttu-id="b1a0d-226">Í svarglugganum **Dálkbreidd** skal slá inn gildi og smella á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-226">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="b1a0d-227">Einnig er hægt að draga hægri brún hauss á dálkreit til að breyta breidd dálksins.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-227">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="b1a0d-228">Dálkar á skoðunarsvæði faldir</span><span class="sxs-lookup"><span data-stu-id="b1a0d-228">Hide columns in the view pane</span></span>

1. <span data-ttu-id="b1a0d-229">Opnið skilgreiningu raðar í Skýrsluhönnun til að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-229">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="b1a0d-230">Veljið dálk eða dálka sem á að minnka.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-230">Select the column or columns to minimize.</span></span>
3. <span data-ttu-id="b1a0d-231">Þá er hægrismellt og smellt á **Fela**.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-231">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="b1a0d-232">Allir faldir dálkar sýndir á skoðunarsvæði</span><span class="sxs-lookup"><span data-stu-id="b1a0d-232">Show all hidden columns in the view pane</span></span>

1. <span data-ttu-id="b1a0d-233">Opnið skilgreiningu raðar í Skýrsluhönnun til að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-233">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="b1a0d-234">Hægrismellið á minnkaða dálkinn sem á að birta og smellið á **Sýna**.</span><span class="sxs-lookup"><span data-stu-id="b1a0d-234">Right-click the minimized column to display, and then click **Unhide**.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="b1a0d-235">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b1a0d-235">Additional resources</span></span>

[<span data-ttu-id="b1a0d-236">Fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="b1a0d-236">Financial reporting</span></span>](financial-reporting-intro.md)
