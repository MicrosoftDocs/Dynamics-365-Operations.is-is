---
title: Línuskilgreiningar í fjárhagsskýrsluhönnuði
description: Línuskilgreining er skýrsluhluti, eða eining sem tilgreinir efni hverrar raðar í fjárhagsskýrslu. Línuskilgreiningu er hægt að sameina með dálkaskilgreiningum, skipuritsskilgreiningum og skýrsluskilgreiningum til að stofna einingahóp sem mörg fyrirtæki geta notað.
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
ms.search.scope: Core, Operations
ms.custom: 68873
ms.assetid: 2fd7b5da-700f-48cb-9003-90c0d82f818f
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8cc7de1473ed6ec9b93bd880b47b0c25ec5a7262
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185199"
---
# <a name="row-definitions-in-financial-report-designer"></a><span data-ttu-id="7a7c8-104">Línuskilgreiningar í fjárhagsskýrsluhönnuði</span><span class="sxs-lookup"><span data-stu-id="7a7c8-104">Row definitions in financial report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a7c8-105">Línuskilgreining er skýrsluhluti, eða eining sem tilgreinir efni hverrar raðar í fjárhagsskýrslu.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-105">A row definition is a report component, or building block, that specifies the contents of each row on a financial report.</span></span> <span data-ttu-id="7a7c8-106">Línuskilgreiningu er hægt að sameina með dálkaskilgreiningum, skipuritsskilgreiningum og skýrsluskilgreiningum til að stofna einingahóp sem mörg fyrirtæki geta notað.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-106">A row definition can be combined with column definitions, reporting tree definitions, and report definitions to create a building block group that can be used by multiple companies.</span></span>

## <a name="create-a-row-definition"></a><span data-ttu-id="7a7c8-107">Línuskilgreining stofnuð</span><span class="sxs-lookup"><span data-stu-id="7a7c8-107">Create a row definition</span></span>

1. <span data-ttu-id="7a7c8-108">Í Report Designer á yfirlitssvæðinu skal smella á **Línuskilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-108">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="7a7c8-109">Á **Skrá** smellið á **Nýtt** og síðan **Línuskilgreining**.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-109">On the **File** menu, click **New**, and then click **Row Definition**.</span></span> <span data-ttu-id="7a7c8-110">Frekari upplýsingar um innihald hvers hólfs eru í [Breyta hólfum línuskilgreiningar](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="7a7c8-110">For more information about the content of each cell, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="open-a-row-definition"></a><span data-ttu-id="7a7c8-111">Línuskilgreining opnuð</span><span class="sxs-lookup"><span data-stu-id="7a7c8-111">Open a row definition</span></span>
1. <span data-ttu-id="7a7c8-112">Í Report Designer á yfirlitssvæðinu skal smella á **Línuskilgreiningar**.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-112">In Report Designer, in the navigation pane, click **Row Definitions**.</span></span>
2. <span data-ttu-id="7a7c8-113">Tvísmellið á heiti línuskilgreiningarinnar sem á að opna.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-113">Double-click the name of the row definition to open.</span></span>
3. <span data-ttu-id="7a7c8-114">Hægrismellið á línuskilgreiningu og veljið **Tengingar** til að skoða allar einingar sem tengjast línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-114">To view any building blocks that are associated with the row definition, right-click the row definition, and then select **Associations**.</span></span>

## <a name="contents-of-a-row-definition"></a><span data-ttu-id="7a7c8-115">Innihald línuskilgreiningar</span><span class="sxs-lookup"><span data-stu-id="7a7c8-115">Contents of a row definition</span></span>
<span data-ttu-id="7a7c8-116">Línuskilgreining getur innihaldið allt að 20.000 fjárhagsvíddaarlínur og haft eftirfarandi upplýsingar:</span><span class="sxs-lookup"><span data-stu-id="7a7c8-116">A row definition can contain up to 20,000 financial dimension rows and can include the following information:</span></span>

- <span data-ttu-id="7a7c8-117">Lýsandi texti sem bætir merkingu við skýrsluna með því að stofna hlutafyrirsagnir, línur og bil, s.s. **Reiðufé** eða **Heildartekjur**</span><span class="sxs-lookup"><span data-stu-id="7a7c8-117">Descriptive text that adds meaning to the report by creating section headings, lines, and spaces, such as **Cash** or **Total Revenue**</span></span>
- <span data-ttu-id="7a7c8-118">Tenglar í fjárhagsgögn, sem geta innihaldið víddargildi í Microsoft Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="7a7c8-118">Links to financial data, which can include dimension values in the Microsoft Dynamics 365 Finance</span></span>

    > [!NOTE]
    > <span data-ttu-id="7a7c8-119">Setja má upp línuskilgreiningu til að sækja gögn úr fjárhagsvíddarkerfinu í hvert sinn sem skýrslan er mynduð.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-119">You can set up a row definition to pull data from the financial dimensions system every time that the report is generated.</span></span>

- <span data-ttu-id="7a7c8-120">Samtölur línu og formúlur eru byggð á tengdum fjárhagsgögnum</span><span class="sxs-lookup"><span data-stu-id="7a7c8-120">Row totals and formulas that are based on the linked financial data</span></span>

<span data-ttu-id="7a7c8-121">Yfirleitt inniheldur hver lína í línuskilgreiningu eina af eftirfarandi tegundum upplýsinga:</span><span class="sxs-lookup"><span data-stu-id="7a7c8-121">Usually, each row in a row definition contains one of the following types of information:</span></span>

- <span data-ttu-id="7a7c8-122">Tilvísanir í fjárhagsvíddarkerfinu</span><span class="sxs-lookup"><span data-stu-id="7a7c8-122">References to the financial dimensions system</span></span>
- <span data-ttu-id="7a7c8-123">Samtölur eða útreikningar sem byggjast á gögnunum</span><span class="sxs-lookup"><span data-stu-id="7a7c8-123">Totals or calculations that are based on the data</span></span>
- <span data-ttu-id="7a7c8-124">Sníða</span><span class="sxs-lookup"><span data-stu-id="7a7c8-124">Formatting</span></span>

<span data-ttu-id="7a7c8-125">Tvær leiðir eru til að slá inn upplýsingar í línuskilgreiningu:</span><span class="sxs-lookup"><span data-stu-id="7a7c8-125">There are two methods for entering information in a row definition:</span></span>

- <span data-ttu-id="7a7c8-126">Færa handvirkt inn upplýsingar um línu í nýju línuskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-126">Manually enter row information in a new row definition.</span></span> <span data-ttu-id="7a7c8-127">Frekari upplýsingar sjá [Breyta hólfum línuskilgreiningar](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="7a7c8-127">For more information, see [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>
- <span data-ttu-id="7a7c8-128">Nota Report Designer til að sækja línuupplýsingar beint úr fjárhagsvíddum.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-128">Use report designer to pull row information directly from the financial dimensions.</span></span> <span data-ttu-id="7a7c8-129">Nánari upplýsingar er að finna í hlutanum "Tengdar línur/formúlur/einingar" í [Breyta reitum skilgreiningar línu](modify-row-definition-cells-financial-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="7a7c8-129">For more information, see the "Related formulas/rows/units" section in [Modify row definition cells](modify-row-definition-cells-financial-reporting.md).</span></span>

## <a name="add-dimensions-in-a-row-definition"></a><span data-ttu-id="7a7c8-130">Víddum bætt við línuskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="7a7c8-130">Add dimensions in a row definition</span></span>
<span data-ttu-id="7a7c8-131">Vídd er skurðpunktur gagna og gilda.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-131">A dimension is an intersection of data and values.</span></span> <span data-ttu-id="7a7c8-132">Hægt er að taka saman gögn og gildi í Report Designer.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-132">You can group data and values in report designer.</span></span> <span data-ttu-id="7a7c8-133">Svo er hægt að flokka og greina færslur nánar.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-133">You can then classify and analyze transactions in more detail.</span></span> <span data-ttu-id="7a7c8-134">Hægt er að nota svargluggann **Setja inn línur úr víddum** til að bæta mörgum línuskilgreiningum við samtímis.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-134">You can use the **Insert Rows from Dimensions** dialog box to add multiple rows to a row definition at the same time.</span></span> <span data-ttu-id="7a7c8-135">Svarglugginn birtir einn dálk fyrir hverja vídd.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-135">The dialog box displays one column for each dimension.</span></span> <span data-ttu-id="7a7c8-136">Eftirfarandi tafla lýsir upplýsingunum sem hægt er að tilgreina fyrir hverja vídd.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-136">The following table describes the information that you can specify for each dimension.</span></span>

| <span data-ttu-id="7a7c8-137">Valkostur</span><span class="sxs-lookup"><span data-stu-id="7a7c8-137">Option</span></span>                | <span data-ttu-id="7a7c8-138">Lýsing</span><span class="sxs-lookup"><span data-stu-id="7a7c8-138">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="7a7c8-139">Vídd</span><span class="sxs-lookup"><span data-stu-id="7a7c8-139">Dimension</span></span>             | <span data-ttu-id="7a7c8-140">Mynstrið sem auðkennir víddina sem bæta á við línuskilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-140">The pattern that identifies the dimension to add to the row definition.</span></span> <span data-ttu-id="7a7c8-141">Þetta mynstur inniheldur eitt og-merki (&) eða númeratákn (\#) fyrir hverja stöðu í víddunum.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-141">This pattern contains one ampersand (&) or number sign (\#) for each position in the dimensions.</span></span> <span data-ttu-id="7a7c8-142">Almennt skal nota allar gæsalappir fyrir víddir aðallykils og öll tákn fyrir aðrar víddir.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-142">Generally, use all ampersands for the Main Account dimension and all number signs for other dimensions.</span></span> |
| <span data-ttu-id="7a7c8-143">Upphaf víddasviðs</span><span class="sxs-lookup"><span data-stu-id="7a7c8-143">Dimension Range Start</span></span> | <span data-ttu-id="7a7c8-144">Fyrsta gildið fyrir þessa vídd sem bæta á við línuskilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-144">The first value for this dimension to add to the row definition.</span></span> |
| <span data-ttu-id="7a7c8-145">Lok víddasviðs</span><span class="sxs-lookup"><span data-stu-id="7a7c8-145">Dimension Range End</span></span>   | <span data-ttu-id="7a7c8-146">Síðasta gildið fyrir þessa vídd sem bæta á við línuskilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-146">The last value for this dimension to add to the row definition.</span></span> |

<span data-ttu-id="7a7c8-147">Til að bæta víddum við línuskilgreiningu skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-147">To add dimensions to a row definition, follow these steps.</span></span>

1. <span data-ttu-id="7a7c8-148">Report Designer smellt **Línuskilgreiningar**, og opnið síðan línuskilgreiningu til að breyta.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-148">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="7a7c8-149">Á valmyndinni **Breyta** er smellt á **Setja inn línur úr víddum**.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-149">On the **Edit** menu, click **Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="7a7c8-150">Í **Setja inn Línur úr Víddir** í svarglugganum, í **Víddir** línunni skal velja hólfið fyrir víddina sem á að flytja í línuskilgreininguna og smella síðan á **Öll &&&**.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-150">In the **Insert Rows from Dimensions** dialog box, in the **Dimensions** row, select the cell for the dimension to transfer to the row definition, and then click **All &&&**.</span></span>
4. <span data-ttu-id="7a7c8-151">Til að takmarka línuskilgreiningar við ákveðin víddargildi skal slá inn upphafsvíddargildi í **Upphafs víddarsviðs** reitinn og slá svo inn lokavíddargildið í **Lok víddarsviðs** reitinn.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-151">To limit the row definition to a specific range of dimension values, enter the starting dimension value in the **Dimension Range Start** cell, and then enter the ending dimension value in the **Dimension Range End** cell.</span></span> <span data-ttu-id="7a7c8-152">Ef taka á öll gildi fyrir völdu víddirnar með skal hafa þessi hólf auð.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-152">To include all values for the selected dimension, leave these cells empty.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7a7c8-153">Algildisstafir (\* eða ?) í víddarsviðum skila ekki endilega öllum niðurstöðum sem óskað er, eftir því hvernig ERP gagnagrunnurinn safnar gögnum.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-153">Wildcard characters (\* or ?) in dimension ranges might not return all the results that you want, depending on how the ERP database collates data.</span></span>

5. <span data-ttu-id="7a7c8-154">Í **Kóði upphafslínu** svæðið skal tilgreina línukóða fyrir fyrsta víddargildi sem á að bæta við línuskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-154">In the **Starting row code** field, specify the row code for the first dimension value to add to the row definition.</span></span>
6. <span data-ttu-id="7a7c8-155">Í **Auka stig hverrar línu með** svæðið skal tilgreina bilið á milli samfelldra línukóða.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-155">In the **Increment each row by** field, specify the gap between consecutive row codes.</span></span> <span data-ttu-id="7a7c8-156">Til dæmis, ef kóði fyrstu línu er 100 og stigvaxandi gildi er 30, hafa fyrstu nýju línurnar kóðana 100 130, 160, 190 og 220.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-156">For example, if the first row code is 100, and the increment value is 30, the first new rows have the codes 100, 130, 160, 190, and 220.</span></span> <span data-ttu-id="7a7c8-157">Notið stigvaxandi gildi sem veitir nægt bil fyrir innsetningu nýs sniðs og formúlulínur.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-157">Use an increment value that provides enough space to insert new format and formula rows.</span></span>
7. <span data-ttu-id="7a7c8-158">Smelltu á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-158">Click **OK**.</span></span> <span data-ttu-id="7a7c8-159">Einni línu er bætt við línuskilgreininguna fyrir hvert valið víddargildi.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-159">For each of the selected dimension values, one line is added to the row definition.</span></span>

## <a name="adjust-rounding-in-a-row-definition"></a><span data-ttu-id="7a7c8-160">Sléttun stillt í línuskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="7a7c8-160">Adjust rounding in a row definition</span></span>
<span data-ttu-id="7a7c8-161">Fyrir efnahagsreikninga þar sem upphæðir eru sléttaðar er ekki víst að samtölur stemmi.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-161">If you have a balance sheet where the amounts are rounded, the totals might not balance.</span></span> <span data-ttu-id="7a7c8-162">Þetta getur t.d. átt sér stað þegar sléttunarvalkosturinn er notaður efnahagsreikningsskýrslu og skýrsluskilgreining tilgreinir einnig sléttun.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-162">This issue can occur if, for example, you use the rounding option on a balance sheet report and the report definition also specifies rounding.</span></span> <span data-ttu-id="7a7c8-163">Hægt er að nota **Sléttunarleiðrétting** valkostinn í línuskilgreiningu til að leiðrétta upphæðir í efnahagsreikningnum.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-163">You can use the **Rounding adjustment** option in the row definition to balance the amounts in the balance sheets.</span></span> <span data-ttu-id="7a7c8-164">Hægt er að slökkva á sléttun eða breyta henni í flipanum **Stillingar** í skýrsluskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-164">You can turn rounding off or modify it on the **Settings** tab of the report definition.</span></span> <span data-ttu-id="7a7c8-165">Eftirfarandi tafla sýnir hvernig upphæðirnar eru sléttaðar.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-165">The following table shows how amounts are rounded.</span></span> <span data-ttu-id="7a7c8-166">Í þessari töflu eru samtölur línanna 100 og 200 mismunandi þegar kveikt er á sléttun.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-166">In this table, the totals of rows 100 and 200 differ when rounding is turned on.</span></span>

| <span data-ttu-id="7a7c8-167">Línukóði</span><span class="sxs-lookup"><span data-stu-id="7a7c8-167">Row code</span></span> | <span data-ttu-id="7a7c8-168">Upphæðir án sléttunar</span><span class="sxs-lookup"><span data-stu-id="7a7c8-168">Amounts without rounding</span></span> | <span data-ttu-id="7a7c8-169">Upphæð með sléttun að heilum þúsundum</span><span class="sxs-lookup"><span data-stu-id="7a7c8-169">Amount with rounding to whole thousands</span></span> |
|----------|--------------------------|-----------------------------------------|
| <span data-ttu-id="7a7c8-170">100</span><span class="sxs-lookup"><span data-stu-id="7a7c8-170">100</span></span>      | <span data-ttu-id="7a7c8-171">3,600</span><span class="sxs-lookup"><span data-stu-id="7a7c8-171">3,600</span></span>                    | <span data-ttu-id="7a7c8-172">4</span><span class="sxs-lookup"><span data-stu-id="7a7c8-172">4</span></span>                                       |
| <span data-ttu-id="7a7c8-173">200</span><span class="sxs-lookup"><span data-stu-id="7a7c8-173">200</span></span>      | <span data-ttu-id="7a7c8-174">3,700</span><span class="sxs-lookup"><span data-stu-id="7a7c8-174">3,700</span></span>                    | <span data-ttu-id="7a7c8-175">4</span><span class="sxs-lookup"><span data-stu-id="7a7c8-175">4</span></span>                                       |
| <span data-ttu-id="7a7c8-176">Samtals</span><span class="sxs-lookup"><span data-stu-id="7a7c8-176">Total</span></span>    | <span data-ttu-id="7a7c8-177">7,300</span><span class="sxs-lookup"><span data-stu-id="7a7c8-177">7,300</span></span>                    | <span data-ttu-id="7a7c8-178">8</span><span class="sxs-lookup"><span data-stu-id="7a7c8-178">8</span></span>                                       |

<span data-ttu-id="7a7c8-179">Til að leiðrétta sléttun í efnahagsreikningi skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-179">To adjust rounding in a balance sheet, follow these steps.</span></span>

1. <span data-ttu-id="7a7c8-180">Smellið á **Línuskilgreiningar** í Skýrsluhönnun og opnið svo línuskilgreininguna sem á að breyta.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-180">In Report Designer, click **Row Definitions**, and then open the row definition to modify.</span></span>
2. <span data-ttu-id="7a7c8-181">Á valmyndinni **Breyta** er smellt á **Sléttunarleiðrétting**.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-181">On the **Edit** menu, click **Rounding Adjustment**.</span></span>
3. <span data-ttu-id="7a7c8-182">Í svarglugganum **Sléttunarleiðréttingar** eru eftirfarandi gildi færð inn:</span><span class="sxs-lookup"><span data-stu-id="7a7c8-182">In the **Rounding Adjustments** dialog box, enter the following values:</span></span>

    - <span data-ttu-id="7a7c8-183">**Sléttunarleiðréttingarlína** – Línukóðinn fyrir línuna sem ætti að leiðrétta til að jafna efnahagsreikninginn.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-183">**Rounding adjustment row** – The row code for the row that should be adjusted to balance the balance sheet.</span></span>
    - <span data-ttu-id="7a7c8-184">**Samtölulína eigna** – Línukóðinn fyrir línuna í efnahagsreikningnum sem inniheldur heildareignir.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-184">**Total assets row** – The row code for the row in the balance sheet that contains the total assets.</span></span>
    - <span data-ttu-id="7a7c8-185">**Samtölulína skulda og eigin fjár** – Línukóðinn fyrir línuna í efnahagsreikningnum sem inniheldur skuldir og eigið fé samtals.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-185">**Total liabilities and equity row** – The row code for the row in the balance sheet that contains the total liabilities and equity.</span></span>
    - <span data-ttu-id="7a7c8-186">**Takmörk leiðréttingarupphæðar** – Jákvæð, heiltala sem tilgreinir takmörkun sjálfvirkrar leiðréttingar.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-186">**Adjustment amount limit** – A positive whole number that specifies the limit on automatic adjustments.</span></span> <span data-ttu-id="7a7c8-187">Þessi upphæð er borin saman við raungildi raunverulegs sléttunarmismunar.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-187">This amount is compared with the absolute value of the actual rounding difference.</span></span>

    > [!NOTE]
    > <span data-ttu-id="7a7c8-188">Tengja verður þessa línukóða við fjárhagsgögn notanda.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-188">These row codes must be linked to your financial data.</span></span> <span data-ttu-id="7a7c8-189">Með öðrum orðum, línan verður að hafa víddargildi í hólfinu **Tengill í fjárhagsvíddir**.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-189">In other words, the row must have a dimension value in its **Link to Financial Dimensions** cell.</span></span> <span data-ttu-id="7a7c8-190">**Ekki** vísa til lýsingar (**DESC**), reiknaðrar (**CALC**), eða samtölulínu (**TOT**).</span><span class="sxs-lookup"><span data-stu-id="7a7c8-190">Do **not** reference a description (**DESC**), calculated (**CALC**), or totaled (**TOT**) row.</span></span>

<span data-ttu-id="7a7c8-191">Upphæðir í efnahagsreikningi verða nú jafnaðar jafnt þegar kveikt er á sléttun.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-191">The amounts in your balance sheet will now balance evenly when rounding is turned on.</span></span>

> [!NOTE]
> <span data-ttu-id="7a7c8-192">Takmörkun leiðréttingar er beitt út frá valkostinum **Sléttunarnákvæmni** sem er tilgreindur fyrir skýrsluskilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-192">The adjustment limit is applied based on the **Rounding precision** option that is specified for the report definition.</span></span> <span data-ttu-id="7a7c8-193">Til dæmis, ef að slétta á skýrsluna í þúsundum og færa inn **2** í **Takmörk leiðréttingarupphæðar** reitnum birtist viðvörun þegar gildið í **Sléttunarleiðréttingarlína** reitnum hækkar eða lækkar um meira en 2.000.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-193">For example, if you round your report to thousands and enter **2** in the **Adjustment amount limit** field, you receive a warning message when the value in the **Rounding adjustment row** field increases or decreases by more than 2,000.</span></span>

## <a name="format-row-and-column-text"></a><span data-ttu-id="7a7c8-194">Lína og dálktexti sniðin</span><span class="sxs-lookup"><span data-stu-id="7a7c8-194">Format row and column text</span></span>
<span data-ttu-id="7a7c8-195">Breyta má útliti skýrslna með því að breyta leturgerðum og sníða texta.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-195">You can customize the appearance of your reports by changing fonts and formatting text.</span></span> <span data-ttu-id="7a7c8-196">Eftirfarandi hlutar útskýra hvernig á að sníða útliti lína og dálka í skýrslum.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-196">The following sections explain how to format the appearance of rows and columns on reports.</span></span>

### <a name="manage-font-styles"></a><span data-ttu-id="7a7c8-197">Vinna með leturstíla</span><span class="sxs-lookup"><span data-stu-id="7a7c8-197">Manage font styles</span></span>

<span data-ttu-id="7a7c8-198">Hægt er að stofna og breyta leturstílum fyrir skýrslu.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-198">You can create and modify font styles for your report.</span></span> <span data-ttu-id="7a7c8-199">Svo er hægt að nota þá stíla í skjalinu, eða á tiltekna röð eða dálki í skýrslu.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-199">You can then apply those styles to the document, or to a specific row or column on a report.</span></span>

<table>
<tbody>
<tr>
<td><span data-ttu-id="7a7c8-200"><strong>Leturstíll stofnaður</strong></span><span class="sxs-lookup"><span data-stu-id="7a7c8-200"><strong>Create a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="7a7c8-201">Á valmyndinni <strong>Snið</strong> í Skýrsluhönnun er smellt á <strong>Stílar og snið</strong>.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-201">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="7a7c8-202">Í <strong>Stílar og snið</strong> svarglugganum skal smella á <strong>Nýtt</strong> og færa inn einkvæmt heiti fyrir nýja stílinn.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-202">In the <strong>Styles and Formatting</strong> dialog box, click <strong>New</strong>, and then enter a unique name for the new style.</span></span></li>
<li><span data-ttu-id="7a7c8-203">Veljið leturgerðir og smellið síðan á <strong>Í lagi</strong>.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-203">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="7a7c8-204"><strong>Leturstíl breytt</strong></span><span class="sxs-lookup"><span data-stu-id="7a7c8-204"><strong>Modify a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="7a7c8-205">Á valmyndinni <strong>Snið</strong> í Skýrsluhönnun er smellt á <strong>Stílar og snið</strong>.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-205">In Report Designer, on the <strong>Format</strong> menu, click <strong>Styles and Formatting</strong>.</span></span></li>
<li><span data-ttu-id="7a7c8-206">Í <strong>Stílar og snið</strong> svarglugganum skal velja stíl sem á að breyta og smella svo á <strong>Breyta</strong>.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-206">In the <strong>Styles and Formatting</strong> dialog box, select a style to modify, and then click <strong>Modify</strong>.</span></span></li>
<li><span data-ttu-id="7a7c8-207">Veljið leturgerðir og smellið síðan á <strong>Í lagi</strong>.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-207">Make your font selections, and then click <strong>OK</strong>.</span></span></li>
</ol>
</td>
</tr>
<tr>
<td><span data-ttu-id="7a7c8-208"><strong>Leturstíll notaður</strong></span><span class="sxs-lookup"><span data-stu-id="7a7c8-208"><strong>Apply a font style</strong></span></span></td>
<td>
<ol>
<li><span data-ttu-id="7a7c8-209">Í Report Designer, í skilgreiningu eða dálkskilgreining eða í hausum og fótum, skal velja einn eða fleiri reit.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-209">In Report Designer, in a definition or column definition, or in headers and footers, select one or more cells.</span></span></li>
<li><span data-ttu-id="7a7c8-210">Í listanum <strong>Stíll</strong> á tækjastikunni er valinn leturstíll.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-210">In the <strong>Style</strong> list on the toolbar, select a font style.</span></span></li>
</ol>
</td>
</tr>
</tbody>
</table>

### <a name="format-row-text"></a><span data-ttu-id="7a7c8-211">Snið texta í línum</span><span class="sxs-lookup"><span data-stu-id="7a7c8-211">Format row text</span></span>

<span data-ttu-id="7a7c8-212">Sniðið sem er tilgreint í línuskilgreiningunni hnekkir öllum sniðum sem eru tilgreind í dálkskilgreiningu og skýrsluskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-212">The formatting that is specified in the row definition overrides any formatting that is specified in the column definition and the report definition.</span></span> <span data-ttu-id="7a7c8-213">Hægt er að breyta textasniðinu með því að nota stýringarnar á sniðstikunni.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-213">You can modify the text format by using the controls on the formatting toolbar.</span></span> <span data-ttu-id="7a7c8-214">Stýringarnar eru hefðbundnar Microsoft Windows stýringar.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-214">These controls are standard Microsoft Windows controls.</span></span>

1. <span data-ttu-id="7a7c8-215">Opnið skilgreiningu raðar í Report Designer til að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-215">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="7a7c8-216">Veljið hólfin sem á að sníða.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-216">Select the cells to format.</span></span> <span data-ttu-id="7a7c8-217">Til að velja fleiri en eitt hólf skal halda Ctrl-lyklinum niðri um leið og hólfin eru valin.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-217">To select multiple cells, hold down the Ctrl key while you select the cell.</span></span>
3. <span data-ttu-id="7a7c8-218">Smellið á tækjastikuhnapp sniðsins sem á að nota.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-218">Click the toolbar button of the format to apply.</span></span> <span data-ttu-id="7a7c8-219">Til að draga t.d. inn línu skal velja línuna og smella á **Auka inndrátt** ![Auka inndrátt](media/indent.gif "Auka inndrátt") á tækjastikunni.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-219">For example, to indent a row, select the row, and then click **Increase Indent** ![Increase Indent](media/indent.gif "Increase Indent") on the toolbar.</span></span>

### <a name="adjust-columns-while-you-design-reports"></a><span data-ttu-id="7a7c8-220">Stilling dálka við hönnun skýrslna</span><span class="sxs-lookup"><span data-stu-id="7a7c8-220">Adjust columns while you design reports</span></span>

<span data-ttu-id="7a7c8-221">Til að auðvelda að skoða dálka sem er unnið er með í línuskilgreiningu er hægt að stilla breidd dálks og fela (minnka) eða sýna dálka á skoðunarsvæðinu.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-221">To make it easier to view the columns that you're working on in the row definition, you can adjust the width of a column, and can also hide (minimize) or show columns in the view pane.</span></span> <span data-ttu-id="7a7c8-222">Allar breytingar sem gerðar hafa aðeins áhrif á útliti dálkanna á skjánum.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-222">The modifications that you make affect only the on-screen appearance of the columns.</span></span> <span data-ttu-id="7a7c8-223">Þær hafa ekki áhrif á snið dálkanna í skýrslum.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-223">They don't affect the column formatting on reports.</span></span>

### <a name="change-the-width-of-a-column-in-the-view-pane"></a><span data-ttu-id="7a7c8-224">Breidd dálks á skoðunarsvæði breytt</span><span class="sxs-lookup"><span data-stu-id="7a7c8-224">Change the width of a column in the view pane</span></span>

1. <span data-ttu-id="7a7c8-225">Opnið skilgreiningu raðar í Skýrsluhönnun til að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-225">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="7a7c8-226">Á valmyndinni **Snið** skal velja **Dálkbreidd**.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-226">On the **Format** menu, select **Column Width**.</span></span>
3. <span data-ttu-id="7a7c8-227">Í svarglugganum **Dálkbreidd** skal slá inn gildi og smella á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-227">In the **Column Width** dialog box, enter a value, and then click **OK**.</span></span> <span data-ttu-id="7a7c8-228">Einnig er hægt að draga hægri brún hauss á dálkreit til að breyta breidd dálksins.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-228">Alternatively, you can drag the right boundary of a column heading cell to change the width of the column.</span></span>

### <a name="hide-columns-in-the-view-pane"></a><span data-ttu-id="7a7c8-229">Dálkar á skoðunarsvæði faldir</span><span class="sxs-lookup"><span data-stu-id="7a7c8-229">Hide columns in the view pane</span></span>

1. <span data-ttu-id="7a7c8-230">Opnið skilgreiningu raðar í Skýrsluhönnun til að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-230">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="7a7c8-231">Veljið dálk eða dálka sem á að minnka.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-231">Select the column or columns to minimize.</span></span>
3. <span data-ttu-id="7a7c8-232">Þá er hægrismellt og smellt á **Fela**.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-232">Right-click, and then click **Hide**.</span></span>

### <a name="show-all-hidden-columns-in-the-view-pane"></a><span data-ttu-id="7a7c8-233">Allir faldir dálkar sýndir á skoðunarsvæði</span><span class="sxs-lookup"><span data-stu-id="7a7c8-233">Show all hidden columns in the view pane</span></span>

1. <span data-ttu-id="7a7c8-234">Opnið skilgreiningu raðar í Skýrsluhönnun til að gera breytingar.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-234">In Report Designer, open the row definition to modify.</span></span>
2. <span data-ttu-id="7a7c8-235">Hægrismellið á minnkaða dálkinn sem á að birta og smellið á **Sýna**.</span><span class="sxs-lookup"><span data-stu-id="7a7c8-235">Right-click the minimized column to display, and then click **Unhide**.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="7a7c8-236">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="7a7c8-236">Additional resources</span></span>

[<span data-ttu-id="7a7c8-237">Fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="7a7c8-237">Financial reporting</span></span>](financial-reporting-intro.md)
