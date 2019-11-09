---
title: Samþætting fjárhagsáætlunargerðar við aðrar einingar
description: Hægt er að gera fjárhagsáætlanir úr mörgum mismunandi tilföngum. Grunneiningar reglubundinnar vinnslu eru þær sömu fyrir öll tilföng.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanGenerate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 64443
ms.assetid: f9a94db5-906c-404a-9ca5-91528d67c490
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7456d0c6a9114fae71aff7b4070d86090e2c7c9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/27/2019
ms.locfileid: "2178320"
---
# <a name="budget-planning-integration-with-other-modules"></a><span data-ttu-id="d8b46-104">Samþætting fjárhagsáætlunargerðar við aðrar einingar</span><span class="sxs-lookup"><span data-stu-id="d8b46-104">Budget planning integration with other modules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d8b46-105">Hægt er að mynda fjárhagsáætlanir úr nokkrum mismunandi tilföngum.</span><span class="sxs-lookup"><span data-stu-id="d8b46-105">Budget plans can be generated from several, different resources.</span></span> <span data-ttu-id="d8b46-106">Grunneiningar reglubundinnar vinnslu eru þær sömu fyrir öll tilföng.</span><span class="sxs-lookup"><span data-stu-id="d8b46-106">The basic elements of the periodic process is the same for all resources.</span></span> 



<a name="periodic-processes-for-generating-budget-plans"></a><span data-ttu-id="d8b46-107">Reglubundnar vinnslur til að mynda fjárhagsáætlanir</span><span class="sxs-lookup"><span data-stu-id="d8b46-107">Periodic processes for generating budget plans</span></span>
----------------------------------------------

<span data-ttu-id="d8b46-108">Hægt er að mynda fjárhagsáætlanir úr eftirfarandi tilföngum:</span><span class="sxs-lookup"><span data-stu-id="d8b46-108">Budget plans can be generated from the following resources:</span></span>

-   <span data-ttu-id="d8b46-109">Fjárhagsfærslur</span><span class="sxs-lookup"><span data-stu-id="d8b46-109">General ledger transactions</span></span>
-   <span data-ttu-id="d8b46-110">Eignir</span><span class="sxs-lookup"><span data-stu-id="d8b46-110">Fixed assets</span></span>
-   <span data-ttu-id="d8b46-111">Spástöður</span><span class="sxs-lookup"><span data-stu-id="d8b46-111">Forecast positions</span></span>
-   <span data-ttu-id="d8b46-112">Áætlanir verka</span><span class="sxs-lookup"><span data-stu-id="d8b46-112">Project forecasts</span></span>
-   <span data-ttu-id="d8b46-113">Birgðaspár</span><span class="sxs-lookup"><span data-stu-id="d8b46-113">Supply forecasts</span></span>
-   <span data-ttu-id="d8b46-114">Eftirspurnarspár</span><span class="sxs-lookup"><span data-stu-id="d8b46-114">Demand forecasts</span></span>
-   <span data-ttu-id="d8b46-115">Færslur í fjárhagsáætlunarskrá</span><span class="sxs-lookup"><span data-stu-id="d8b46-115">Budget register entries</span></span>
-   <span data-ttu-id="d8b46-116">Aðrar fjárhagsáætlanir</span><span class="sxs-lookup"><span data-stu-id="d8b46-116">Other budget plans</span></span>

<span data-ttu-id="d8b46-117">Grunneiningar reglubundins ferlis eru þau sömu fyrir öll ferli.</span><span class="sxs-lookup"><span data-stu-id="d8b46-117">The basic elements of the periodic process are the same for all the processes.</span></span> <span data-ttu-id="d8b46-118">Flipar leyfa skilgreiningu á uppruna gagna, markeiginda (fjárhagsáætlunargerð) og valkosti til að keyra ferlið í bakgrunni sem runuvinnslu.</span><span class="sxs-lookup"><span data-stu-id="d8b46-118">Tabs let you define the source of the data, the target (budget plan) attributes, and options to run the process in the background as a batch process.</span></span> <span data-ttu-id="d8b46-119">Síðari hlutunum þessa þekkingarskráar lýsa vörur sem gætu verið óljósar í hverri vinnslu.</span><span class="sxs-lookup"><span data-stu-id="d8b46-119">Later sections of this article describe items that might not be apparent in each process.</span></span>

### <a name="actions"></a><span data-ttu-id="d8b46-120">Aðgerðir</span><span class="sxs-lookup"><span data-stu-id="d8b46-120">Actions</span></span>

<span data-ttu-id="d8b46-121">Fyrir hvert myndunarferli eru þrjár aðgerðir í boði:</span><span class="sxs-lookup"><span data-stu-id="d8b46-121">For each generation process, three actions are available:</span></span>

-   <span data-ttu-id="d8b46-122">**Búa til nýja fjárhagsáætlun** – Stofna nýja áætlun hefur eigindir sem eru valdar í á **Mark** hluta.</span><span class="sxs-lookup"><span data-stu-id="d8b46-122">**Create a new budget plan** creates a new plan that has the attributes that are selected in the **Target** section.</span></span> <span data-ttu-id="d8b46-123">Þessar eigindir þurfa ekki að vera einkvæmar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-123">These attributes don't have to be unique.</span></span> <span data-ttu-id="d8b46-124">Þess vegna geta tvær áætlanir haft sama heiti og önnur gildi.</span><span class="sxs-lookup"><span data-stu-id="d8b46-124">Therefore, two plans can have the same name and other values.</span></span>
-   <span data-ttu-id="d8b46-125">**Skipta út fyrirliggjandi aðstæðum fjárhagsáætlunargerðar** eyðir öllum gögnum í fjárhagsáætlun marks í völdum aðstæðum fjárhagsáætlunargerðar og stofnar nýjar línur sem nota gögn valinnar upprunastöðu.</span><span class="sxs-lookup"><span data-stu-id="d8b46-125">**Replace the existing budget plan scenario** deletes all data in the target budget plan in the selected budget plan scenario and creates new lines that use the selected source data.</span></span>
-   <span data-ttu-id="d8b46-126">**Uppfæra fyrirliggjandi aðstæður fjárhagsáætlunargerðar og bæta nýjum gögnum við** uppfærir fyrirliggjandi línur í markáætlun sem samsvarar upprunalínum og bætir við nýjum línum fyrir ný gögn.</span><span class="sxs-lookup"><span data-stu-id="d8b46-126">**Update the existing budget plan scenario, and append new data** updates existing lines in the target plan that match the source lines and adds new lines for new data.</span></span> <span data-ttu-id="d8b46-127">Samsvörunin er byggð á fjárhagslykli, dagsetningu, fjárhagsáætlunarklasa og ýmsum öðrum reitum.</span><span class="sxs-lookup"><span data-stu-id="d8b46-127">The matching is based on the ledger account, date, budget class, and various other fields.</span></span> <span data-ttu-id="d8b46-128">Til dæmis þegar fjárhagsáætlanir eru myndaðar úr spástöðum er staðsetningarnúmer mikilvægur reitur.</span><span class="sxs-lookup"><span data-stu-id="d8b46-128">For example, when you generate budget plans from forecast positions, the position number is an important field.</span></span> <span data-ttu-id="d8b46-129">Allar línur sem hafa staðsetningarnúmer sem samsvarar stöðu uppruna er skipt út fyrir nýjar línur úr frumkóða.</span><span class="sxs-lookup"><span data-stu-id="d8b46-129">All lines that have a position number that matches the source position number are replaced with the new lines from the source.</span></span>

### <a name="source"></a><span data-ttu-id="d8b46-130">Uppruni</span><span class="sxs-lookup"><span data-stu-id="d8b46-130">Source</span></span>

<span data-ttu-id="d8b46-131">Fyrir öll ferli sem **Uppruna** flipanum gerir kleift að sía gögn við **Síu** hnappinn.</span><span class="sxs-lookup"><span data-stu-id="d8b46-131">For all processes, the **Source** tab lets you filter data by using the **Filter** button.</span></span> <span data-ttu-id="d8b46-132">Að sjálfgefnu tiltekin svæði er bætt við síu fyrir hverju ferli.</span><span class="sxs-lookup"><span data-stu-id="d8b46-132">By default, specific fields are added to the filter for each process.</span></span> <span data-ttu-id="d8b46-133">Til dæmis, fyrir í **Mynda fjárhagsáætlun úr fjárhag** ferlið í **fjárhagslykil** og **aðallykils** tegundir eru tiltækar og birtast á síðu myndun.</span><span class="sxs-lookup"><span data-stu-id="d8b46-133">For example, for the **Generate budget plan from general ledger** process, the **Ledger account** and **Main account** categories are available, and appear on the generation page.</span></span> <span data-ttu-id="d8b46-134">Öllum reitum sem er bætt við síuna er einnig bætt við síðuna, ásamt öllum skilyrðum sem er bætt við.</span><span class="sxs-lookup"><span data-stu-id="d8b46-134">Any fields that you add to the filter are also added to the page, together with any criteria that you add.</span></span>

### <a name="target"></a><span data-ttu-id="d8b46-135">Mark</span><span class="sxs-lookup"><span data-stu-id="d8b46-135">Target</span></span>

<span data-ttu-id="d8b46-136">Valkosturinn **Sögulegt** valkostinn á flipanum **Mark** gerir það mögulegt að nota dagsetningar úr upprunagögnum sem gildisdagsetningu í fjárhagsáætlun.</span><span class="sxs-lookup"><span data-stu-id="d8b46-136">The **Historical** option on the **Target** tab lets you use the dates from the source data as the effective date in the budget plan.</span></span> <span data-ttu-id="d8b46-137">Yfirleitt verður gildisdagsetningin að vera innan fjárhagsáætlunarferlis áætlunarinnar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-137">Typically, the effective date must be within the plan’s budget cycle.</span></span> <span data-ttu-id="d8b46-138">Þegar valkosturinn **Sögulegt** er stilltur á **Já** er dagsetning (jafnvel árið) uppruna notuð, þannig að hægt er að nota fyrri gögn sem grunnur fyrir samanburð.</span><span class="sxs-lookup"><span data-stu-id="d8b46-138">When you set the **Historical** option to **Yes**, the date (even the year) of the source is used, so that you can use past data as a basis for comparison.</span></span> <span data-ttu-id="d8b46-139">Ekki er hægt að breyta sögulegum gögn í fjárhagsáætlunargerð og áætlun er stillt á stöðuna samþykkt í verkflæði.</span><span class="sxs-lookup"><span data-stu-id="d8b46-139">You can't modify historical data in the budget plan, and the plan is set to an approved workflow status.</span></span> <span data-ttu-id="d8b46-140">Hins vegar er hægt að endurstilla stöðu ef aðrar aðstæður í áætluninni krefjast breytinga.</span><span class="sxs-lookup"><span data-stu-id="d8b46-140">However, you can reset the status if you must other scenarios in the plan require changes.</span></span>

<span data-ttu-id="d8b46-141">Reiturinn **Steypa saman samtölu eftir** efst á síðunni ákvarðar einnig dagsetninguna sem er notuð.</span><span class="sxs-lookup"><span data-stu-id="d8b46-141">The **Aggregate total by** field at the top of the page also determines the date that is used.</span></span> <span data-ttu-id="d8b46-142">Þessi reitur leggur saman upphæðir og stillir einnig gildisdagsetningu á fyrsta dag fjárhagsársins eða fjárhagstímabili.</span><span class="sxs-lookup"><span data-stu-id="d8b46-142">This field totals amounts, and optionally sets the effective date to the first day of the fiscal year or fiscal period.</span></span> 

<span data-ttu-id="d8b46-143">Margir reitir á flipanum <strong>Mark</strong> verða breytanlegir eða aðeins til lestrar, eftir hvaða aðgerð er valin á flipanum.</span><span class="sxs-lookup"><span data-stu-id="d8b46-143">Many of the fields on the <strong>Target</strong> tab become editable or read-only, depending on the action that you select.</span></span> <span data-ttu-id="d8b46-144">Þegar er breytt úr stofnun nýrrar fjárhagsáætlunar í uppfærslu fyrirliggjandi áætlunar verður reiturinn **Heiti fjárhagsáætlunar** óvirkur og reitir sem eru tengdir vali á fyrirliggjandi áætlun verða tiltækir.</span><span class="sxs-lookup"><span data-stu-id="d8b46-144">When you change from creating a new budget plan to updating an existing plan, the **Budget plan name** field becomes unavailable, and the fields that are related to selecting an existing plan become available.</span></span> <span data-ttu-id="d8b46-145">Bæði á flipanum **Mark** og flipanum **Uppruni**, er reiturinn **Fjárhagur** alltaf óvirkur, þar sem gildið er ákvarðað af valið ferli fjárhagsáætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-145">On both the **Target** tab and the **Source** tab, the **Ledger** field is always unavailable, because the value is determined by the selected budget planning process.</span></span> 

<span data-ttu-id="d8b46-146">Reiturinn **Fjárhagsáætlunarklasi** gerir kleift að stilla línur fjárhagsáætlunar sem annaðhvort kostnaðarfærslur eða tekjufærslur.</span><span class="sxs-lookup"><span data-stu-id="d8b46-146">The **Budget class** field lets you set the budget plan lines as either expense transactions or revenue transactions.</span></span> <span data-ttu-id="d8b46-147">Yfirleitt eru tekjufærslur kreditfærslur í fjárhagslykil og eru þar af leiðandi geymd sem neikvæðar upphæðir.</span><span class="sxs-lookup"><span data-stu-id="d8b46-147">Usually, revenue transactions are credits to a ledger account and are therefore stored as negative amounts.</span></span> <span data-ttu-id="d8b46-148">Yfirleitt birtast þessar færslur einnig sem neikvæðar upphæðir í fjárhagsáætlun.</span><span class="sxs-lookup"><span data-stu-id="d8b46-148">Typically, these transactions also appear as negative amounts in the budget plan.</span></span> <span data-ttu-id="d8b46-149">Hins vegar, með því að bæta við fjárhagsáætlunarklasanum sem reit í útliti áætlunar, er hægt að virkja tekjur birtist sem upphæðir í jákvætt.</span><span class="sxs-lookup"><span data-stu-id="d8b46-149">However, by adding the budget class as a field in the plan layout, you can enable revenue to appear as positive amounts.</span></span>

### <a name="generation-rules"></a><span data-ttu-id="d8b46-150">Myndunarreglur</span><span class="sxs-lookup"><span data-stu-id="d8b46-150">Generation rules</span></span>

<span data-ttu-id="d8b46-151">Þrjú svæði veita viðbótaraðgerðir: **Stuðull**, **Lágmarks**, og **Sléttun** **reglu**.</span><span class="sxs-lookup"><span data-stu-id="d8b46-151">Three fields provide additional functionality: **Factor**, **Minimum**, and **Rounding** **rule**.</span></span> 

<span data-ttu-id="d8b46-152">Gildið í reitnum **Stuðull** er margfaldað með upprunaupphæð til að stilla upphæð í fjárhagsáætlun.</span><span class="sxs-lookup"><span data-stu-id="d8b46-152">The value in the **Factor** field is multiplied by the source amount to set the amount in the budget plan.</span></span> <span data-ttu-id="d8b46-153">Síðan er hægt að gera leiðréttingar þegar línur fjárhagsáætlunar eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-153">You can then make adjustments when you create budget plan lines.</span></span> <span data-ttu-id="d8b46-154">Til dæmis er hægt að færa inn **1,03** fyrir 3 prósent hækkun.</span><span class="sxs-lookup"><span data-stu-id="d8b46-154">For example, you can enter **1.03** for a 3 percent increase.</span></span> <span data-ttu-id="d8b46-155">Stuðullinn verður að vera jákvæð tala.</span><span class="sxs-lookup"><span data-stu-id="d8b46-155">The factor must be a positive number.</span></span> 

<span data-ttu-id="d8b46-156">Reiturinn **Lágmark** gerir kleift að stilla þröskuldsupphæð til að stofna línu fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-156">The **Minimum** field lets you set the threshold amount for creating a budget plan line.</span></span> <span data-ttu-id="d8b46-157">Ef upprunaupphæðin er lægri en þessi tala er fjárhagsáætlunarlína ekki stofnuð.</span><span class="sxs-lookup"><span data-stu-id="d8b46-157">If the source amount is less than this number, the budget plan line isn't created.</span></span> <span data-ttu-id="d8b46-158">Virði upp á **0,00** leyfir allar upphæðir en takmarkar ekki línur við jákvæðar upphæðir.</span><span class="sxs-lookup"><span data-stu-id="d8b46-158">A value of **0.00** allows all amounts but doesn't limit lines to positive amounts.</span></span> <span data-ttu-id="d8b46-159">(Ekkert gildi takmarkar línur við jákvæðar upphæðir.</span><span class="sxs-lookup"><span data-stu-id="d8b46-159">(No value limits lines to positive amounts.</span></span> <span data-ttu-id="d8b46-160">Neikvæðar upphæðir eru alltaf með og standa yfirleitt fyrir kreditfærslur.)</span><span class="sxs-lookup"><span data-stu-id="d8b46-160">Negative amounts are always included and usually represent credit entries.)</span></span>

<span data-ttu-id="d8b46-161">Reiturinn **Sléttunarregla** gerir kleift að stilla nákvæmni fjárhagsáætlunarlínanna sem eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-161">The **Rounding rule** field lets you set the precision of the budget plan lines that are created.</span></span> <span data-ttu-id="d8b46-162">Hægt er að slétta upphæðir í næstu 1,00, 10,00, 100,00 og svo framvegis, í gjaldmiðli.</span><span class="sxs-lookup"><span data-stu-id="d8b46-162">You can round amounts to the nearest 1.00, 10.00, 100.00, and so on, of currency.</span></span>

## <a name="notes-for-specific-processes"></a><span data-ttu-id="d8b46-163">Athugasemdir fyrir tilteknar vinnslur</span><span class="sxs-lookup"><span data-stu-id="d8b46-163">Notes for specific processes</span></span>
### <a name="generate-budget-plan-from-general-ledger"></a><span data-ttu-id="d8b46-164">Mynda fjárhagsáætlun úr fjárhag</span><span class="sxs-lookup"><span data-stu-id="d8b46-164">Generate budget plan from general ledger</span></span>

<span data-ttu-id="d8b46-165">Þegar stofnaðar eru fjárhagsáætlanir úr fjárhagsgögnum verður að stilla reitinn **Steypa saman samtölu eftir** á **Fjárhagsár** ef valkosturinn **Sögulegt** er stilltur á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="d8b46-165">When you create a budget plan from general ledger data, you must set the **Aggregate total by** field to **Fiscal year** if the **Historical** option is set to **No**.</span></span> <span data-ttu-id="d8b46-166">Tímabil og dagsetningar í uppruna gæti passa ekki við tímabilin í dagsetningar í marki.</span><span class="sxs-lookup"><span data-stu-id="d8b46-166">The periods and dates in the source might not match the periods in dates in the target.</span></span> <span data-ttu-id="d8b46-167">Þar sem ferlið hefur engar áreiðanlega leið til að varpa þessi gildi, verður að takmarka það ferli að fyrsta ársins.</span><span class="sxs-lookup"><span data-stu-id="d8b46-167">Because the process has no reliable way to map these values, you must limit the process to the first of the year.</span></span> 

<span data-ttu-id="d8b46-168">Í markinu er reiturinn **Fjárhagsáætlunarklasi** stilltur á annaðhvort **Kostnaður** eða **Tekjur**.</span><span class="sxs-lookup"><span data-stu-id="d8b46-168">In the target, the **Budget class** field is set to either **Expense** or **Revenue**.</span></span> <span data-ttu-id="d8b46-169">Þessi stilling er notuð til að velja eigindina **Fjárhagsáætlunargerð** fyrir línur sem eru stofnaðar þegar aðallykillinn í línu er ekki með í **Tekjur** eða **Kostnaðarskýrslu** gerð.</span><span class="sxs-lookup"><span data-stu-id="d8b46-169">This setting is used to select the **Budget type** attribute for lines that are created, when the main account on a line isn't of the **Revenue** or **Expense** type.</span></span>

### <a name="generate-budget-plan-from-fixed-assets"></a><span data-ttu-id="d8b46-170">Mynda fjárhagsáætlun úr eignum</span><span class="sxs-lookup"><span data-stu-id="d8b46-170">Generate budget plan from fixed assets</span></span>

<span data-ttu-id="d8b46-171">Ferlið **Mynda fjárhagsáætlun úr eignum** hefur engan valkost fyrir söfnun eftir degi eða tímabili.</span><span class="sxs-lookup"><span data-stu-id="d8b46-171">The **Generate budget plan from fixed assets** process has no option for aggregating by period or day.</span></span> <span data-ttu-id="d8b46-172">Einnig er enginn valkostur til að stilla áætlunina sem sögulega.</span><span class="sxs-lookup"><span data-stu-id="d8b46-172">There is also no option for setting the plan as historical.</span></span> <span data-ttu-id="d8b46-173">Hægt er að nota reglubundna ferlið með áætlaðar færslur fyrir eignir í þínu fjárhagsáætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-173">You can use this periodic process to include projected transactions for fixed assets in your budget planning.</span></span>

### <a name="generate-budget-plan-from-forecast-positions"></a><span data-ttu-id="d8b46-174">Mynda fjárhagsáætlun úr spástöðum</span><span class="sxs-lookup"><span data-stu-id="d8b46-174">Generate budget plan from forecast positions</span></span>

<span data-ttu-id="d8b46-175">Ferlið **Mynda fjárhagsáætlun úr spástöðum** úthlutar spástöðu uppruna á línu fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-175">The **Generate budget plan from forecast positions** process assigns the source forecast position to the budget plan line.</span></span> <span data-ttu-id="d8b46-176">Hægt er að skoða stöðuna með því að bæta spástöðu við sem línu í fjárhagsáætlunarútlit eða nota fyrirspurnina **Fjárhagsáætlunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="d8b46-176">You can view the position by adding the forecast position as a row in the budget plan layout or by using the **Budget plan lines** inquiry.</span></span> <span data-ttu-id="d8b46-177">Ef þú vilt ekki að spárstöðunni sé úthlutað á fjárhagsáætlunarlínu, skal stilla valkostinn **Hafa stöðu í línu fjárhagsáætlunargerðar** á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="d8b46-177">If you don't want the forecast position to be assigned to budget plan lines, set the **Include position in budget plan line** option to **No**.</span></span>

<span data-ttu-id="d8b46-178">Línur í fjárhagsáætlunargerð eru lagðar saman eftir fjárhagslykli og stöðu.</span><span class="sxs-lookup"><span data-stu-id="d8b46-178">Lines in the budget plan are aggregated by ledger account and position.</span></span> <span data-ttu-id="d8b46-179">Hins vegar er hægt að útiloka staðsetningarnúmer, svo sem línur eru lagðar saman eftir fjárhagslyklum eingöngu.</span><span class="sxs-lookup"><span data-stu-id="d8b46-179">However, you can exclude the position number, so that lines are aggregated by ledger account only.</span></span> <span data-ttu-id="d8b46-180">Á flipanum **Mark** skal stilla valkostinn **Hafa stöðu í línu fjárhagsáætlunargerðar** á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="d8b46-180">On the **Target** tab, set the **Include position in budget plan** option to **No**.</span></span>

<span data-ttu-id="d8b46-181">Í reitnum **FTE-aðstæður fjárhagsáætlunar** er hægt að velja aðstæður sem fela í sér fjölda fullt ígildi þess (starfsmanna í fullu starfi) í fjárhagsáætlun.</span><span class="sxs-lookup"><span data-stu-id="d8b46-181">In the **Budget plan FTE scenario** field, you can select a scenario to include the number of full-time equivalents (FTEs) in the budget plan.</span></span> <span data-ttu-id="d8b46-182">Þessi reitur takmarkast við áætlanir af gerðinni magn sem eru innifaldar í útliti markfjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-182">This field is limited to quantity-type scenarios that are included in the layout of the target budget plan.</span></span> <span data-ttu-id="d8b46-183">Ef FTE-aðstæður eru valdar verður einnig að tilgreina aðallykil FTE.</span><span class="sxs-lookup"><span data-stu-id="d8b46-183">If you select an FTE scenario, you must also select an FTE main account.</span></span> <span data-ttu-id="d8b46-184">Þessi lykill er notaður til að stofna fjárhagsáætlunarlínur fyrir magn.</span><span class="sxs-lookup"><span data-stu-id="d8b46-184">This account is used to create the quantity budget plan lines.</span></span> 

<span data-ttu-id="d8b46-185">Ferli og aðstæður fjárhagsáætlunargerðar sem eru valdar í uppruna ákvarða ferli og aðstæður fjárhagsáætlunargerðar markaðstæðna.</span><span class="sxs-lookup"><span data-stu-id="d8b46-185">The budget planning process and budget plan scenario that are selected in the source set the target scenario budget planning process and scenario.</span></span> <span data-ttu-id="d8b46-186">Þar sem eigindunum er úthlutað á spástöður verða þau að vera samstillt við fjárhagsáætlunina.</span><span class="sxs-lookup"><span data-stu-id="d8b46-186">Because these attributes are assigned to forecast positions, they must match the budget plan.</span></span> <span data-ttu-id="d8b46-187">Þess vegna er ekki hægt að breyta þessum eigindum á markinu.</span><span class="sxs-lookup"><span data-stu-id="d8b46-187">Therefore, these attributes can't be modified on the target.</span></span>

### <a name="generate-budget-plan-from-project-forecasts"></a><span data-ttu-id="d8b46-188">Mynda fjárhagsáætlun úr verkspám</span><span class="sxs-lookup"><span data-stu-id="d8b46-188">Generate budget plan from project forecasts</span></span>

<span data-ttu-id="d8b46-189">Ferlið **Mynda fjárhagsáætlun úr verkspá**, eins og ferlið **Mynda fjárhagsáætlun úr spástöðum**, hefur valkost til að hafa með magn verks (tími, útgjöld og vörur) í magni aðstæðna.</span><span class="sxs-lookup"><span data-stu-id="d8b46-189">The **Generate budget plan from project forecasts** process, like the **Generate budget plan from forecast positions** process, has an option to include project quantities (hours, expenses, and items) in a quantity scenario.</span></span> <span data-ttu-id="d8b46-190">Tvö ferli hafa einnig svipaðar síur fyrir dálka í fjárhagsáætlunarútlit.</span><span class="sxs-lookup"><span data-stu-id="d8b46-190">The two process also have similar filters for the columns in the budget plan layout.</span></span> 

<span data-ttu-id="d8b46-191">Á flipanum **Uppruna** ákvarða þrír valkostir í hlutanum **Taka yfirlit með** hvaða línur fjárhagsáætlunar eru stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-191">On the **Source** tab, three options in the **Include statement** section determine which budget plan lines are created.</span></span> <span data-ttu-id="d8b46-192">Þessir valkostir eru þeir sömu og þeir valkostir sem eru tiltækir þegar færslur fjárhagsáætlunarskrár er stofnuð beint úr verkspá.</span><span class="sxs-lookup"><span data-stu-id="d8b46-192">These options are the same as the options that are available when you create budget register entries directly from project forecasts.</span></span> <span data-ttu-id="d8b46-193">Stilltu valkostinn **Hagnaður og tap** á **Já** til að stofna línur fyrir kostnað og tekjur.</span><span class="sxs-lookup"><span data-stu-id="d8b46-193">Set the **Profit and loss** option to **Yes** to create lines for costs and for revenues.</span></span> <span data-ttu-id="d8b46-194">Setja skal **VÍV** valkosturinn að **Já** til að stofna vinnu í vinnslu á færslum.</span><span class="sxs-lookup"><span data-stu-id="d8b46-194">Set the **WIP** option to **Yes** to create work in process entries.</span></span> <span data-ttu-id="d8b46-195">Stilltu valkostinn **Launaúthlutun** á **Já** til að stofna línur fyrir kostnað og tímafærslur.</span><span class="sxs-lookup"><span data-stu-id="d8b46-195">Set the **Payroll allocation** option to **Yes** to create lines for the payroll offset accounts for hour transactions.</span></span> 

<span data-ttu-id="d8b46-196">Það er enginn reitur **fjárhagsáætlunarklasa** þar sem fjárhagsáætlunarklasinn (**Kostnaður** eða **Tekjur**) er ákvarðaður eftir uppruna.</span><span class="sxs-lookup"><span data-stu-id="d8b46-196">There is no **Budget class** field, because the budget class (**Expense** or **Revenue**) is determined by the source.</span></span> 

<span data-ttu-id="d8b46-197">Hægt er að nota fjárhagsáætlanir verks sem uppruna með því að velja spárlíkanið sem inniheldur upphæðir verkáætlunar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-197">You can use project budgets as a source by selecting the forecast model that contains the project budget amounts.</span></span> <span data-ttu-id="d8b46-198">Munið að fjárhagsáætlanir stofna spárfærslur verks um leið og þær eru samþykktar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-198">Remember that project budgets create project forecast entries as they are approved.</span></span>

<span data-ttu-id="d8b46-199">Til að velja aðeins kostnað eða tekjur fyrir línur fjárhagsáætlunar skal nota síuna til að velja <strong>Áætlunaruppfærslur: gerð upphæðar = Kostnaður</strong>.</span><span class="sxs-lookup"><span data-stu-id="d8b46-199">To select only costs or revenues for budget plan lines, use the filter to select <strong>Budget updates: Amount type = Cost</strong>.</span></span> <span data-ttu-id="d8b46-200">Til að velja aðeins eina gerð spár skal nota síuna til að velja <strong>Áætlunaruppfærslur: Færslugerð = *xxx</strong>*.</span><span class="sxs-lookup"><span data-stu-id="d8b46-200">To select only one type of forecast, use the filter to select <strong>Budget updates: Transaction type = *xxx</strong>*.</span></span> 

<span data-ttu-id="d8b46-201">Hægt er að nota aðeins eitt áætlunarlíkan til að mynda aðstæður fjárhagsáætlunargerðar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-201">Only one forecast model can be used to generate a budget plan scenario.</span></span> <span data-ttu-id="d8b46-202">Ef keyrt er ferli fyrir eitt spálíkan og síðan gerð uppfærsla og reynt að tilgreina annað líkan, verður skrifað yfir fyrsta líkanið ef verið er að nota sama verk og fjárhagslykla.</span><span class="sxs-lookup"><span data-stu-id="d8b46-202">If you run the process for one forecast model, and then do an update and try to specify another model, the first model will be overwritten if the same project and ledger accounts apply.</span></span> <span data-ttu-id="d8b46-203">Til að mynda aðstæður fjárhagsáætlunar úr fleiri en einu spálíkani, mynda í mismunandi aðstæður fjárhagsáætlunargerðar og valkosti fyrir úthlutun er notuð til að bæta við þær saman í öðrum aðstæðum.</span><span class="sxs-lookup"><span data-stu-id="d8b46-203">To generate a budget plan scenario from more than one forecast model, generate into different budget plan scenarios, and use allocation options to add them together in another scenario.</span></span> 

<span data-ttu-id="d8b46-204">Ferlið **Mynda fjárhagsáætlun úr spástöðum** úthlutar einnig upprunaverkefni á línu fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-204">The **Generate budget plan from project forecasts** process also assigns the source project to the budget plan line.</span></span>

### <a name="generate-budget-plan-from-supply-forecast"></a><span data-ttu-id="d8b46-205">Mynda fjárhagsáætlun úr birgðaspá</span><span class="sxs-lookup"><span data-stu-id="d8b46-205">Generate budget plan from supply forecast</span></span>

<span data-ttu-id="d8b46-206">Upprunasíuvalkostirnir í ferlinu **Mynda fjárhagsáætlun úr birgðaspá** voru mótaðir eftir valkostunum í eftir aðgerðinni **Flytja innkaupaáætlun í fjárhag** vegna líkingar milli ferlis og aðgerðinni.</span><span class="sxs-lookup"><span data-stu-id="d8b46-206">The source filter options in the **Generate budget plan from supply forecast** process were modeled after options in the **Transfer purchase budget to ledger** function, because of similarities between the process and the function.</span></span>

### <a name="generate-budget-plan-from-demand-forecast"></a><span data-ttu-id="d8b46-207">Mynda fjárhagsáætlun úr eftirspurnarspám</span><span class="sxs-lookup"><span data-stu-id="d8b46-207">Generate budget plan from demand forecast</span></span>

<span data-ttu-id="d8b46-208">Fyrir ferlið **Mynda fjárhagsáætlun úr eftirspurnarspá** er hægt að stilla valkostinn **Sölupöntun** á **Já** til að mynda tekjulínur í fjárhagsáætlunargerð, stilla **Notkun** á **Já** til að stofna kostnaðarlínur eða stilla báða valkosti á **Já**.</span><span class="sxs-lookup"><span data-stu-id="d8b46-208">For the **Generate budget plan from demand forecast** process, you can set the **Sales order** option to **Yes** to generate revenue lines in the budget plan, set the **Consumption** to **Yes** to create expense lines, or set both options to **Yes**.</span></span>

### <a name="generate-budget-plan-from-budget-register-entries"></a><span data-ttu-id="d8b46-209">Mynda fjárhagsáætlun úr færslum fjárhagsáætlunarskráar</span><span class="sxs-lookup"><span data-stu-id="d8b46-209">Generate budget plan from budget register entries</span></span>

<span data-ttu-id="d8b46-210">Fyrir ferlið **Mynda fjárhagsáætlun úr færslum áætlunarskráar** verður uppruninn að tilgreina eitt undirlíkan, einn fjárhagsáætlunarkóða og eitt færslunúmer.</span><span class="sxs-lookup"><span data-stu-id="d8b46-210">For the **Generate budget plan from budget register entries** process, the source must specify one submodel, one budget code, and one entry number.</span></span> <span data-ttu-id="d8b46-211">Með öðrum orðum er hægt að stofna línur fjárhagsáætlunargerðar fyrir eina færslu fjárhagsáætlunarskrár í einu.</span><span class="sxs-lookup"><span data-stu-id="d8b46-211">In other words, you can create budget plan lines for only one budget register entry at a time.</span></span> <span data-ttu-id="d8b46-212">Hægt er að nota fleiri færslur í sama fjárhagsáætlunargerð með því að keyra einu sinni fyrir hverja færslu uppruna ferlið.</span><span class="sxs-lookup"><span data-stu-id="d8b46-212">You can use additional entries in the same budget plan by running the process one time for each source entry.</span></span>

### <a name="generate-budget-plan-from-budget-plan"></a><span data-ttu-id="d8b46-213">Mynda fjárhagsáætlun úr fjárhagsáætlun</span><span class="sxs-lookup"><span data-stu-id="d8b46-213">Generate budget plan from budget plan</span></span>

<span data-ttu-id="d8b46-214">Fyrir ferlið **Mynda fjárhagsáætlun úr fjárhagsáætlun** gerir aukasafn valkosta á flipanum **Mark** það mögulegt að tengja nýjar fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="d8b46-214">For the **Generate budget plan from budget plan** process, an additional set of options on the **Target** tab lets you assign new financial dimensions.</span></span> <span data-ttu-id="d8b46-215">Ef fjárhagsvídd er valin verður það gildi notað fyrir allar línur fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-215">If a financial dimension is selected, that value will be used for all budget plan lines.</span></span> <span data-ttu-id="d8b46-216">Þess vegna er hægt að nota eina fjárhagsáætlun sem grunn fyrir aðrar fjárhagsáætlanir, en einnig má úthluta, til dæmis, mismunandi deild eða kostnaðarstað á nýjar fjárhagsáætlanir.</span><span class="sxs-lookup"><span data-stu-id="d8b46-216">Therefore, you can use one budget plan as the basis for other budget plans, but can also assign, for example, a different department or cost center to the new budget plans.</span></span>

## <a name="looking-back-from-the-budget-plan"></a><span data-ttu-id="d8b46-217">Flett aftur úr fjárhagsáætlunargerð</span><span class="sxs-lookup"><span data-stu-id="d8b46-217">Looking back from the budget plan</span></span>
### <a name="budget-plans-by-dimension-set-inquiry"></a><span data-ttu-id="d8b46-218">Fjárhagsáætlanir eftir fyrirspurn víddasamstæðu</span><span class="sxs-lookup"><span data-stu-id="d8b46-218">Budget plans by dimension set inquiry</span></span>

<span data-ttu-id="d8b46-219">Fyrirspurnin **Fjárhagsáætlanir eftir víddasamstæðum** inniheldur nokkra valkosti sem gera kleift að keyra fyrirspurn til að finna gögn fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-219">The **Budget plans by dimension set** inquiry includes several options that let you run a query to help identify the source of the budget plan data.</span></span> 

<span data-ttu-id="d8b46-220">Veldu línu og smelltu á hnappinn **Fjárhagsáætlunarlínur** til að keyra fyrirspurnina **Fjárhagsáætlunarlínur**.</span><span class="sxs-lookup"><span data-stu-id="d8b46-220">Select a line and click the **Budget plan lines** button to run the **Budget plan lines** query.</span></span> <span data-ttu-id="d8b46-221">Niðurstöðurnar eru síaðar fyrir víddargildi völdu línunnar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-221">The results are filtered for the dimension values of the selected line.</span></span> <span data-ttu-id="d8b46-222">Síðan er hægt að nota viðbótarfæribreytur.</span><span class="sxs-lookup"><span data-stu-id="d8b46-222">You can then apply additional parameters.</span></span> 

<span data-ttu-id="d8b46-223">Nota skal hnappana **Birgðaspá** og **Eftirspurnarspá** til að keyra þessar fyrirspurnir.</span><span class="sxs-lookup"><span data-stu-id="d8b46-223">Use the **Supply forecast** and **Demand forecast** buttons run these queries.</span></span> <span data-ttu-id="d8b46-224">Í báðum tilvikum leitar fyrirspurnin að spálínum sem gætu hafa stofnað línur fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="d8b46-224">In both cases, the query searches for forecast lines that could have created the budget plan lines.</span></span> 

<span data-ttu-id="d8b46-225">Viðbótarskýrslur sem eru tiltækar innihalda skýrsluna **Spástöður eftir fjárhagsáætlun**.</span><span class="sxs-lookup"><span data-stu-id="d8b46-225">Additional reports that are available include the **Forecast positions by budget plan** report.</span></span> <span data-ttu-id="d8b46-226">Þessi skýrsla er sérlega gagnleg þegar á að ákvarða hvort stöðu hafi verið rétt úthlutað á fjárhagsáætlanir.</span><span class="sxs-lookup"><span data-stu-id="d8b46-226">This report is especially useful when you want to determine whether a position has been correctly allocated to budget plans.</span></span>


