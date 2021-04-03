---
title: Línuskilgreiningar í fjárhagsskýrsluhönnuði
description: Línuskilgreining er skýrsluhluti, eða eining sem tilgreinir efni hverrar raðar í fjárhagsskýrslu.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: dfce0f1622d45dcf77d91b71abbe9e33e8c91ad0
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564032"
---
# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="b0db9-103">Línuskilgreiningar í fjárhagsskýrsluhönnuði</span><span class="sxs-lookup"><span data-stu-id="b0db9-103">Row definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b0db9-104">Línuskilgreining er skýrsluhluti, eða eining sem tilgreinir efni hverrar raðar í fjárhagsskýrslu.</span><span class="sxs-lookup"><span data-stu-id="b0db9-104">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="b0db9-105">Línuskilgreiningu er hægt að sameina með dálkaskilgreiningum, skipuritsskilgreiningum og skýrsluskilgreiningum til að stofna einingahóp sem mörg fyrirtæki geta notað.</span><span class="sxs-lookup"><span data-stu-id="b0db9-105">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

## <a name="create-a-row-definition"></a><span data-ttu-id="b0db9-106">Línuskilgreining stofnuð</span><span class="sxs-lookup"><span data-stu-id="b0db9-106">Create a row definition</span></span>

1. <span data-ttu-id="b0db9-107">Í Report Designer á yfirlitssvæðinu skal smella á **Línuskilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="b0db9-107">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="b0db9-108">Á **Skrá** smellið á **Nýtt** og síðan **Línuskilgreining**.</span><span class="sxs-lookup"><span data-stu-id="b0db9-108">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="b0db9-109">Frekari upplýsingar um innihald hvers hólfs eru í [Breyta hólfum línuskilgreiningar](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="b0db9-109">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="b0db9-110">Línuskilgreining opnuð</span><span class="sxs-lookup"><span data-stu-id="b0db9-110">Open a row definition</span></span>
1. <span data-ttu-id="b0db9-111">Í Report Designer á yfirlitssvæðinu skal smella á **Línuskilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="b0db9-111">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="b0db9-112">Tvísmellið á heiti línuskilgreiningarinnar sem á að opna.</span><span class="sxs-lookup"><span data-stu-id="b0db9-112">Double-click the name of the row definition to open.</span></span>
3. <span data-ttu-id="b0db9-113">Hægrismellið á línuskilgreiningu og veljið **Tengingar** til að skoða allar einingar sem tengjast línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="b0db9-113">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="b0db9-114">Innihald línuskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="b0db9-114">Contents of a row definition</span></span>
<span data-ttu-id="b0db9-115">Línuskilgreining getur innihaldið allt að 20.000 fjárhagsvíddaarlínur og haft eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="b0db9-115">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

- <span data-ttu-id="b0db9-116">Lýsandi texti sem bætir merkingu við skýrsluna með því að stofna hlutafyrirsagnir, línur og bil, s.s. **Reiðufé** eða **Heildartekjur**</span><span class="sxs-lookup"><span data-stu-id="b0db9-116">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
- <span data-ttu-id="b0db9-117">Tenglar í fjárhagsgögn, sem geta innihaldið víddargildi í Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="b0db9-117">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 Finance</span></span>

    > [!NOTE]
    > <span data-ttu-id="b0db9-118">Setja má upp línuskilgreiningu til að sækja gögn úr fjárhagsvíddarkerfinu í hvert sinn sem skýrslan er mynduð.</span><span class="sxs-lookup"><span data-stu-id="b0db9-118">You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>

- <span data-ttu-id="b0db9-119">Samtölur línu og formúlur eru byggð á tengdum fjárhagsgögnum</span><span class="sxs-lookup"><span data-stu-id="b0db9-119">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="b0db9-120">Yfirleitt inniheldur hver lína í línuskilgreiningu eina af eftirfarandi tegundum upplýsinga:</span><span class="sxs-lookup"><span data-stu-id="b0db9-120">Usually, each row in a row definition contains one of the following types of information:</span></span>

- <span data-ttu-id="b0db9-121">Tilvísanir í fjárhagsvíddarkerfinu</span><span class="sxs-lookup"><span data-stu-id="b0db9-121">References to the financial dimensions system</span></span>
- <span data-ttu-id="b0db9-122">Samtölur eða útreikningar sem byggjast á gögnunum</span><span class="sxs-lookup"><span data-stu-id="b0db9-122">Totals or calculations that are based on the data</span></span>
- <span data-ttu-id="b0db9-123">Sníða</span><span class="sxs-lookup"><span data-stu-id="b0db9-123">Formatting</span></span>

<span data-ttu-id="b0db9-124">Tvær leiðir eru til að slá inn upplýsingar í línuskilgreiningu:</span><span class="sxs-lookup"><span data-stu-id="b0db9-124">There are two methods for entering information in a row definition:</span></span>

- <span data-ttu-id="b0db9-125">Færa handvirkt inn upplýsingar um línu í nýju línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="b0db9-125">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="b0db9-126">Frekari upplýsingar sjá [Breyta hólfum línuskilgreiningar](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="b0db9-126">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
- <span data-ttu-id="b0db9-127">Nota Report Designer til að sækja línuupplýsingar beint úr fjárhagsvíddum.</span><span class="sxs-lookup"><span data-stu-id="b0db9-127">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="b0db9-128">Nánari upplýsingar er að finna í hlutanum "Tengdar línur/formúlur/einingar" í [Breyta reitum skilgreiningar línu](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="b0db9-128">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="b0db9-129">Víddum bætt við línuskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="b0db9-129">Add dimensions in a row definition</span></span>
<span data-ttu-id="b0db9-130">Vídd er skurðpunktur gagna og gilda.</span><span class="sxs-lookup"><span data-stu-id="b0db9-130">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="b0db9-131">Hægt er að taka saman gögn og gildi í Report Designer.</span><span class="sxs-lookup"><span data-stu-id="b0db9-131">You can group data and values in report designer.</span></span> <span data-ttu-id="b0db9-132">Svo er hægt að flokka og greina færslur nánar.</span><span class="sxs-lookup"><span data-stu-id="b0db9-132">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="b0db9-133">Hægt er að nota svargluggann **Setja inn línur úr víddum** til að bæta mörgum línuskilgreiningum við samtímis.</span><span class="sxs-lookup"><span data-stu-id="b0db9-133">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="b0db9-134">Svarglugginn birtir einn dálk fyrir hverja vídd.</span><span class="sxs-lookup"><span data-stu-id="b0db9-134">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="b0db9-135">Eftirfarandi tafla lýsir upplýsingunum sem hægt er að tilgreina fyrir hverja vídd.</span><span class="sxs-lookup"><span data-stu-id="b0db9-135">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="b0db9-136">Valkostur</span><span class="sxs-lookup"><span data-stu-id="b0db9-136">Option</span></span>                | <span data-ttu-id="b0db9-137">Lýsing</span><span class="sxs-lookup"><span data-stu-id="b0db9-137">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="b0db9-138">Vídd</span><span class="sxs-lookup"><span data-stu-id="b0db9-138">Dimension</span></span>             | <span data-ttu-id="b0db9-139">Mynstrið sem auðkennir víddina sem bæta á við línuskilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="b0db9-139">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="b0db9-140">Þetta mynstur inniheldur eitt og-merki (&) eða númeratákn (\#) fyrir hverja stöðu í víddunum.</span><span class="sxs-lookup"><span data-stu-id="b0db9-140">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="b0db9-141">Almennt skal nota allar gæsalappir fyrir víddir aðallykils og öll tákn fyrir aðrar víddir.</span><span class="sxs-lookup"><span data-stu-id="b0db9-141">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="b0db9-142">Upphaf víddasviðs</span><span class="sxs-lookup"><span data-stu-id="b0db9-142">Dimension Range Start</span></span> | <span data-ttu-id="b0db9-143">Fyrsta gildið fyrir þessa vídd sem bæta á við línuskilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="b0db9-143">The first value for this dimension to add to the row definition.</span></span> |
| <span data-ttu-id="b0db9-144">Lok víddasviðs</span><span class="sxs-lookup"><span data-stu-id="b0db9-144">Dimension Range End</span></span>   | <span data-ttu-id="b0db9-145">Síðasta gildið fyrir þessa vídd sem bæta á við línuskilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="b0db9-145">The last value for this dimension to add to the row definition.</span></span> |

<span data-ttu-id="b0db9-146">Til að bæta víddum við línuskilgreiningu skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="b0db9-146">To add dimensions to a row definition, follow these steps.</span></span>

1. <span data-ttu-id="b0db9-147">Report Designer smellt **Línuskilgreiningar**, og opnið síðan línuskilgreiningu til að breyta.</span><span class="sxs-lookup"><span data-stu-id="b0db9-147">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="b0db9-148">Á valmyndinni **Breyta** er smellt á **Setja inn línur úr víddum**.</span><span class="sxs-lookup"><span data-stu-id="b0db9-148">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="b0db9-149">Í **Setja inn Línur úr Víddir** í svarglugganum, í **Víddir** línunni skal velja hólfið fyrir víddina sem á að flytja í línuskilgreininguna og smella síðan á **Öll &&&**.</span><span class="sxs-lookup"><span data-stu-id="b0db9-149">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4. <span data-ttu-id="b0db9-150">Til að takmarka línuskilgreiningar við ákveðin víddargildi skal slá inn upphafsvíddargildi í **Upphafs víddarsviðs** reitinn og slá svo inn lokavíddargildið í **Lok víddarsviðs** reitinn.</span><span class="sxs-lookup"><span data-stu-id="b0db9-150">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="b0db9-151">Ef taka á öll gildi fyrir völdu víddirnar með skal hafa þessi hólf auð.</span><span class="sxs-lookup"><span data-stu-id="b0db9-151">To include all values for the selected dimension, leave these cells empty.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b0db9-152">Algildisstafir (\* eða ?) í víddarsviðum skila ekki endilega öllum niðurstöðum sem óskað er, eftir því hvernig ERP gagnagrunnurinn safnar gögnum.</span><span class="sxs-lookup"><span data-stu-id="b0db9-152">Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>

5. <span data-ttu-id="b0db9-153">Í **Kóði upphafslínu** svæðið skal tilgreina línukóða fyrir fyrsta víddargildi sem á að bæta við línuskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="b0db9-153">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6. <span data-ttu-id="b0db9-154">Í **Auka stig hverrar línu með** svæðið skal tilgreina bilið á milli samfelldra línukóða.</span><span class="sxs-lookup"><span data-stu-id="b0db9-154">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="b0db9-155">Til dæmis, ef kóði fyrstu línu er 100 og stigvaxandi gildi er 30, hafa fyrstu nýju línurnar kóðana 100 130, 160, 190 og 220.</span><span class="sxs-lookup"><span data-stu-id="b0db9-155">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="b0db9-156">Notið stigvaxandi gildi sem veitir nægt bil fyrir innsetningu nýs sniðs og formúlulínur.</span><span class="sxs-lookup"><span data-stu-id="b0db9-156">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7. <span data-ttu-id="b0db9-157">Smelltu á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b0db9-157">Click **OK**.</span></span> <span data-ttu-id="b0db9-158">Einni línu er bætt við línuskilgreininguna fyrir hvert valið víddargildi.</span><span class="sxs-lookup"><span data-stu-id="b0db9-158">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="b0db9-159">Sléttun stillt í línuskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="b0db9-159">Adjust rounding in a row definition</span></span>
<span data-ttu-id="b0db9-160">Fyrir efnahagsreikninga þar sem upphæðir eru sléttaðar er ekki víst að samtölur stemmi.</span><span class="sxs-lookup"><span data-stu-id="b0db9-160">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="b0db9-161">Þetta getur t.d. átt sér stað þegar sléttunarvalkosturinn er notaður efnahagsreikningsskýrslu og skýrsluskilgreining tilgreinir einnig sléttun.</span><span class="sxs-lookup"><span data-stu-id="b0db9-161">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="b0db9-162">Hægt er að nota **Sléttunarleiðrétting** valkostinn í línuskilgreiningu til að leiðrétta upphæðir í efnahagsreikningnum.</span><span class="sxs-lookup"><span data-stu-id="b0db9-162">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="b0db9-163">Hægt er að slökkva á sléttun eða breyta henni í flipanum **Stillingar** í skýrsluskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="b0db9-163">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="b0db9-164">Eftirfarandi tafla sýnir hvernig upphæðirnar eru sléttaðar.</span><span class="sxs-lookup"><span data-stu-id="b0db9-164">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="b0db9-165">Í þessari töflu eru samtölur línanna 100 og 200 mismunandi þegar kveikt er á sléttun.</span><span class="sxs-lookup"><span data-stu-id="b0db9-165">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="b0db9-166">Línukóði</span><span class="sxs-lookup"><span data-stu-id="b0db9-166">Row code</span></span> | <span data-ttu-id="b0db9-167">Upphæðir án sléttunar</span><span class="sxs-lookup"><span data-stu-id="b0db9-167">Amounts without rounding</span></span> | <span data-ttu-id="b0db9-168">Upphæð með sléttun að heilum þúsundum</span><span class="sxs-lookup"><span data-stu-id="b0db9-168">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="b0db9-169">100</span><span class="sxs-lookup"><span data-stu-id="b0db9-169">100</span></span>      | <span data-ttu-id="b0db9-170">3,600</span><span class="sxs-lookup"><span data-stu-id="b0db9-170">3,600</span></span>                    | <span data-ttu-id="b0db9-171">4</span><span class="sxs-lookup"><span data-stu-id="b0db9-171">4</span></span>                                       |
| <span data-ttu-id="b0db9-172">200</span><span class="sxs-lookup"><span data-stu-id="b0db9-172">200</span></span>      | <span data-ttu-id="b0db9-173">3,700</span><span class="sxs-lookup"><span data-stu-id="b0db9-173">3,700</span></span>                    | <span data-ttu-id="b0db9-174">4</span><span class="sxs-lookup"><span data-stu-id="b0db9-174">4</span></span>                                       |
| <span data-ttu-id="b0db9-175">Samtals</span><span class="sxs-lookup"><span data-stu-id="b0db9-175">Total</span></span>    | <span data-ttu-id="b0db9-176">7,300</span><span class="sxs-lookup"><span data-stu-id="b0db9-176">7,300</span></span>                    | <span data-ttu-id="b0db9-177">8</span><span class="sxs-lookup"><span data-stu-id="b0db9-177">8</span></span>                                       |

<span data-ttu-id="b0db9-178">Til að leiðrétta sléttun í efnahagsreikningi skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="b0db9-178">To adjust rounding in a balance sheet, follow these steps.</span></span>

1. <span data-ttu-id="b0db9-179">Smellið á **Línuskilgreiningar** í Skýrsluhönnun og opnið svo línuskilgreininguna sem á að breyta.</span><span class="sxs-lookup"><span data-stu-id="b0db9-179">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="b0db9-180">Á valmyndinni **Breyta** er smellt á **Sléttunarleiðrétting**.</span><span class="sxs-lookup"><span data-stu-id="b0db9-180">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3. <span data-ttu-id="b0db9-181">Í svarglugganum **Sléttunarleiðréttingar** eru eftirfarandi gildi færð inn:</span><span class="sxs-lookup"><span data-stu-id="b0db9-181">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>

    - <span data-ttu-id="b0db9-182">**Sléttunarleiðréttingarlína** – Línukóðinn fyrir línuna sem ætti að leiðrétta til að jafna efnahagsreikninginn.</span><span class="sxs-lookup"><span data-stu-id="b0db9-182">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    - <span data-ttu-id="b0db9-183">**Samtölulína eigna** – Línukóðinn fyrir línuna í efnahagsreikningnum sem inniheldur heildareignir.</span><span class="sxs-lookup"><span data-stu-id="b0db9-183">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    - <span data-ttu-id="b0db9-184">**Samtölulína skulda og eigin fjár** – Línukóðinn fyrir línuna í efnahagsreikningnum sem inniheldur skuldir og eigið fé samtals.</span><span class="sxs-lookup"><span data-stu-id="b0db9-184">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    - <span data-ttu-id="b0db9-185">**Takmörk leiðréttingarupphæðar** – Jákvæð, heiltala sem tilgreinir takmörkun sjálfvirkrar leiðréttingar.</span><span class="sxs-lookup"><span data-stu-id="b0db9-185">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="b0db9-186">Þessi upphæð er borin saman við raungildi raunverulegs sléttunarmismunar.</span><span class="sxs-lookup"><span data-stu-id="b0db9-186">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b0db9-187">Tengja verður þessa línukóða við fjárhagsgögn notanda.</span><span class="sxs-lookup"><span data-stu-id="b0db9-187">These row codes must be linked to your financial data.</span></span> <span data-ttu-id="b0db9-188">Með öðrum orðum, línan verður að hafa víddargildi í hólfinu **Tengill í fjárhagsvíddir**.</span><span class="sxs-lookup"><span data-stu-id="b0db9-188">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="b0db9-189">**Ekki** vísa til lýsingar (**DESC**), reiknaðrar (**CALC**), eða samtölulínu (**TOT**).</span><span class="sxs-lookup"><span data-stu-id="b0db9-189">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="b0db9-190">Upphæðir í efnahagsreikningi verða nú jafnaðar jafnt þegar kveikt er á sléttun.</span><span class="sxs-lookup"><span data-stu-id="b0db9-190">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="b0db9-191">Takmörkun leiðréttingar er beitt út frá valkostinum **Sléttunarnákvæmni** sem er tilgreindur fyrir skýrsluskilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="b0db9-191">The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="b0db9-192">Til dæmis, ef að slétta á skýrsluna í þúsundum og færa inn **2** í **Takmörk leiðréttingarupphæðar** reitnum birtist viðvörun þegar gildið í **Sléttunarleiðréttingarlína** reitnum hækkar eða lækkar um meira en 2.000.</span><span class="sxs-lookup"><span data-stu-id="b0db9-192">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="b0db9-193">Lína og dálktexti sniðin</span><span class="sxs-lookup"><span data-stu-id="b0db9-193">Format row and column text</span></span>
<span data-ttu-id="b0db9-194">Breyta má útliti skýrslna með því að breyta leturgerðum og sníða texta.</span><span class="sxs-lookup"><span data-stu-id="b0db9-194">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="b0db9-195">Eftirfarandi hlutar útskýra hvernig á að sníða útliti lína og dálka í skýrslum.</span><span class="sxs-lookup"><span data-stu-id="b0db9-195">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="b0db9-196">Vinna með leturstíla</span><span class="sxs-lookup"><span data-stu-id="b0db9-196">Manage font styles</span></span>

<span data-ttu-id="b0db9-197">Hægt er að stofna og breyta leturstílum fyrir skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b0db9-197">You can create and modify font styles for your report.</span></span> <span data-ttu-id="b0db9-198">Svo er hægt að nota þá stíla í skjalinu, eða á tiltekna röð eða dálki í skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b0db9-198">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="b0db9-199"><strong>Leturstíll stofnaður</strong></span><span class="sxs-lookup"><span data-stu-id="b0db9-199"><strong>Create a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="b0db9-200">Á valmyndinni <strong>Snið</strong> í Skýrsluhönnun er smellt á <strong>Stílar og snið</strong>.</span><span class="sxs-lookup"><span data-stu-id="b0db9-200">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="b0db9-201">Í <strong>Stílar og snið</strong> svarglugganum skal smella á <strong>Nýtt</strong> og færa inn einkvæmt heiti fyrir nýja stílinn.</span><span class="sxs-lookup"><span data-stu-id="b0db9-201">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="b0db9-202">Veljið leturgerðir og smellið síðan á <strong>Í lagi</strong>.</span><span class="sxs-lookup"><span data-stu-id="b0db9-202">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="b0db9-203"><strong>Leturstíl breytt</strong></span><span class="sxs-lookup"><span data-stu-id="b0db9-203"><strong>Modify a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="b0db9-204">Á valmyndinni <strong>Snið</strong> í Skýrsluhönnun er smellt á <strong>Stílar og snið</strong>.</span><span class="sxs-lookup"><span data-stu-id="b0db9-204">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="b0db9-205">Í <strong>Stílar og snið</strong> svarglugganum skal velja stíl sem á að breyta og smella svo á <strong>Breyta</strong>.</span><span class="sxs-lookup"><span data-stu-id="b0db9-205">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="b0db9-206">Veljið leturgerðir og smellið síðan á <strong>Í lagi</strong>.</span><span class="sxs-lookup"><span data-stu-id="b0db9-206">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="b0db9-207"><strong>Leturstíll notaður</strong></span><span class="sxs-lookup"><span data-stu-id="b0db9-207"><strong>Apply a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="b0db9-208">Í Report Designer, í skilgreiningu eða dálkskilgreining eða í hausum og fótum, skal velja einn eða fleiri reit.</span><span class="sxs-lookup"><span data-stu-id="b0db9-208">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="b0db9-209">Í listanum <strong>Stíll</strong> á tækjastikunni er valinn leturstíll.</span><span class="sxs-lookup"><span data-stu-id="b0db9-209">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="b0db9-210">Snið texta í línum</span><span class="sxs-lookup"><span data-stu-id="b0db9-210">Format row text</span></span>

<span data-ttu-id="b0db9-211">Sniðið sem er tilgreint í línuskilgreiningunni hnekkir öllum sniðum sem eru tilgreind í dálkskilgreiningu og skýrsluskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="b0db9-211">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="b0db9-212">Hægt er að breyta textasniðinu með því að nota stýringarnar á sniðstikunni.</span><span class="sxs-lookup"><span data-stu-id="b0db9-212">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="b0db9-213">Stýringarnar eru hefðbundnar Microsoft Windows stýringar.</span><span class="sxs-lookup"><span data-stu-id="b0db9-213">These controls are standard Microsoft Windows controls.</span></span>

1. <span data-ttu-id="b0db9-214">Opnið skilgreiningu raðar í Report Designer til að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="b0db9-214">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="b0db9-215">Veljið hólfin sem á að sníða.</span><span class="sxs-lookup"><span data-stu-id="b0db9-215">Select the cells to format.</span></span> <span data-ttu-id="b0db9-216">Til að velja fleiri en eitt hólf skal halda Ctrl-lyklinum niðri um leið og hólfin eru valin.</span><span class="sxs-lookup"><span data-stu-id="b0db9-216">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3. <span data-ttu-id="b0db9-217">Smellið á tækjastikuhnapp sniðsins sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="b0db9-217">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="b0db9-218">Til að draga t.d. inn línu skal velja línuna og smella á **Auka inndrátt** ![Auka inndrátt](media/indent.gif "Auka inndrátt") á tækjastikunni.</span><span class="sxs-lookup"><span data-stu-id="b0db9-218">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](media/indent.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="b0db9-219">Stilling dálka við hönnun skýrslna</span><span class="sxs-lookup"><span data-stu-id="b0db9-219">Adjust columns while you design reports</span></span>

<span data-ttu-id="b0db9-220">Til að auðvelda að skoða dálka sem er unnið er með í línuskilgreiningu er hægt að stilla breidd dálks og fela (minnka) eða sýna dálka á skoðunarsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="b0db9-220">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="b0db9-221">Allar breytingar sem gerðar hafa aðeins áhrif á útliti dálkanna á skjánum.</span><span class="sxs-lookup"><span data-stu-id="b0db9-221">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="b0db9-222">Þær hafa ekki áhrif á snið dálkanna í skýrslum.</span><span class="sxs-lookup"><span data-stu-id="b0db9-222">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="b0db9-223">Breidd dálks á skoðunarsvæði breytt</span><span class="sxs-lookup"><span data-stu-id="b0db9-223">Change the width of a column in the view pane</span></span>

1. <span data-ttu-id="b0db9-224">Opnið skilgreiningu raðar í Skýrsluhönnun til að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="b0db9-224">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="b0db9-225">Á valmyndinni **Snið** skal velja **Dálkbreidd**.</span><span class="sxs-lookup"><span data-stu-id="b0db9-225">On the **Format** menu, select **Column Width**.</span></span>
3. <span data-ttu-id="b0db9-226">Í svarglugganum **Dálkbreidd** skal slá inn gildi og smella á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b0db9-226">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="b0db9-227">Einnig er hægt að draga hægri brún hauss á dálkreit til að breyta breidd dálksins.</span><span class="sxs-lookup"><span data-stu-id="b0db9-227">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="b0db9-228">Dálkar á skoðunarsvæði faldir</span><span class="sxs-lookup"><span data-stu-id="b0db9-228">Hide columns in the view pane</span></span>

1. <span data-ttu-id="b0db9-229">Opnið skilgreiningu raðar í Skýrsluhönnun til að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="b0db9-229">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="b0db9-230">Veljið dálk eða dálka sem á að minnka.</span><span class="sxs-lookup"><span data-stu-id="b0db9-230">Select the column or columns to minimize.</span></span>
3. <span data-ttu-id="b0db9-231">Þá er hægrismellt og smellt á **Fela**.</span><span class="sxs-lookup"><span data-stu-id="b0db9-231">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="b0db9-232">Allir faldir dálkar sýndir á skoðunarsvæði</span><span class="sxs-lookup"><span data-stu-id="b0db9-232">Show all hidden columns in the view pane</span></span>

1. <span data-ttu-id="b0db9-233">Opnið skilgreiningu raðar í Skýrsluhönnun til að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="b0db9-233">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="b0db9-234">Hægrismellið á minnkaða dálkinn sem á að birta og smellið á **Sýna**.</span><span class="sxs-lookup"><span data-stu-id="b0db9-234">Right-click the minimized column to display, and then click **Unhide**.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="b0db9-235">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b0db9-235">Additional resources</span></span>

[<span data-ttu-id="b0db9-236">Fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="b0db9-236">Financial reporting</span></span>](financial-reporting-intro.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]