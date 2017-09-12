---
title: "Sniðmát fjárhagsáætlunargerðar fyrir Excel"
description: "Þetta efnisatriði lýsir hvernig stofna á sniðmát í Microsoft Excel sem hægt er að nota með fjárhagsáætlununum."
author: ryansandness
manager: AnnBe
ms.date: 07/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 1945d137b337508a1850e3e679a60487aecb6b84
ms.openlocfilehash: 7cec40859a8c68cb8a9751c5531c67cef7706258
ms.contentlocale: is-is
ms.lasthandoff: 07/27/2017

---

# <a name="budget-planning-templates-for-excel"></a><span data-ttu-id="0ad1c-103">Sniðmát fjárhagsáætlunargerðar fyrir Excel</span><span class="sxs-lookup"><span data-stu-id="0ad1c-103">Budget planning templates for Excel</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="0ad1c-104">Þetta efnisatriði lýsir hvernig stofna á sniðmát í Microsoft Excel sem hægt er að nota með fjárhagsáætlununum.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-104">This topic describes how to create Microsoft Excel templates that can be used with budget plans.</span></span>

<span data-ttu-id="0ad1c-105">Þetta efnisatriði sýnir hvernig stofna á sniðmát í Excel sem verða notuð með fjárhagsáætlununum sem nota stöðluð sýnigögn og innskráningu kerfisstjóranotanda.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-105">This topic shows how to create Excel templates that will be used with budget plans using the standard demo data set and the Admin user login.</span></span> <span data-ttu-id="0ad1c-106">Nánari upplýsingar um fjárhagsáætlunargerð eru í [Yfirlit fjárhagsáætlunargerðar](budget-planning-overview-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="0ad1c-106">For more information about budget planning, see [Budget planning overview.](budget-planning-overview-configuration.md)</span></span> <span data-ttu-id="0ad1c-107">Einnig er hægt að fylgja sýnidæminu [Fjárhagsáætlunargerð 101](budget-plan.md) til að læra skilgreiningu og notkunarreglur grunneininda.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-107">You can also follow the [Budget planning 101](budget-plan.md) tutorial to learn basic module configuration and usage principles.</span></span>

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a><span data-ttu-id="0ad1c-108">Mynda vinnublað með útliti fjárhagsáætlunarskjals</span><span class="sxs-lookup"><span data-stu-id="0ad1c-108">Generate a worksheet using budget plan document layout</span></span>

<span data-ttu-id="0ad1c-109">Fjárhagsáætlunarskjal má skoða og breyta með einu eða fleiri útlitum.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-109">Budget plan documents can be viewed and edited using one or more layouts.</span></span> <span data-ttu-id="0ad1c-110">Hvert útlit getur haft an tengdar fjárhagsáætlunarskjal sniðmát til að skoða og breyta fjárhagsáætlungögnum í Excel vinnublað.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-110">Each layout can have an associated budget plan document template to view and edit the budget plan data in an Excel worksheet.</span></span> <span data-ttu-id="0ad1c-111">Í þessu efnisatriði verður sniðmát fjárhagsáætlunarskjals myndað með fyrirliggjandi útlitsskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-111">In this topic, a budget plan document template will be generated using an existing layout configuration.</span></span> 

1. <span data-ttu-id="0ad1c-112">Opnaðu **Fjárhagsáætlunarlista** (**Fjárhagsáætlun** &gt; **Fjárhagsáætlunargerðir**).</span><span class="sxs-lookup"><span data-stu-id="0ad1c-112">Open the **Budget plans list** (**Budgeting** &gt; **Budget plans**).</span></span> 
2. <span data-ttu-id="0ad1c-113">Smellt er á **Ný** til að búa til nýtt fjárhagsáætlunarskjal.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-113">Click **New** to create a new budget plan document.</span></span> 

  <span data-ttu-id="0ad1c-114">[![Fjárhagsáætlanalisti](./media/bpt11-1024x552.png)](./media/bpt11.png)</span><span class="sxs-lookup"><span data-stu-id="0ad1c-114">[![Budget plans list](./media/bpt11-1024x552.png)](./media/bpt11.png)</span></span> 

3. <span data-ttu-id="0ad1c-115">Notaðu **Bæta við** línuaðgerðna til að bæta við línum.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-115">Use the **Add** line option to add lines.</span></span> <span data-ttu-id="0ad1c-116">Smellt er á **Útlit** til að skoða útlit skilgreining fjárhagsáætlunarskjals.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-116">Click **Layouts** to view the budget plan document layout configuration.</span></span> 

  <span data-ttu-id="0ad1c-117">[![Fjárhagsáætlanir bæta við](./media/bpt2-1024x274.png)](./media/bpt2.png)</span><span class="sxs-lookup"><span data-stu-id="0ad1c-117">[![Budget plans add](./media/bpt2-1024x274.png)](./media/bpt2.png)</span></span> 

<span data-ttu-id="0ad1c-118">Hægt er að yfirfara grunnstillingu útlits og leiðrétta hana eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-118">You can review the layout configuration and adjust it as needed.</span></span> 
1. <span data-ttu-id="0ad1c-119">Farðu í **Sniðmát** &gt; **Mynda** til að stofna Excel-skrá fyrir þetta útlit.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-119">Go to **Template** &gt; **Generate** to create an Excel file for this layout.</span></span> 
2. <span data-ttu-id="0ad1c-120">Eftir að sniðmát er myndað, skal fara í **Sniðmát** &gt; **Skoða** til að opna og yfirfara sniðmát fjárhagsáætlunarskjals.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-120">After the template is generated, go to **Template** &gt; **View** to open and review the budget plan document template.</span></span> <span data-ttu-id="0ad1c-121">Hægt er að vista Excel-skrána á staðbundnu drifi.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-121">You can save the Excel file to your local drive.</span></span> 

<span data-ttu-id="0ad1c-122">[![Vista sem](./media/bpt3-1024x545.png)](./media/bpt3.png)</span><span class="sxs-lookup"><span data-stu-id="0ad1c-122">[![Save as](./media/bpt3-1024x545.png)](./media/bpt3.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="0ad1c-123">Útlit fjárhagsáætlunarskjals getur ekki verið breytt eftir að Excel-sniðmát er tengt því.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-123">The Budget plan document layout cannot be edited after an Excel template is associated with it.</span></span> <span data-ttu-id="0ad1c-124">Til að breyta útlitinu þarf að eyða tengdri skrá Excel-sniðmáts og endurgera það.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-124">To modify the layout, delete the associated Excel template file and regenerate it.</span></span> <span data-ttu-id="0ad1c-125">Þetta er áskilið til að halda svæðum í útliti og vinnublaði samstilltum.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-125">This is required to keep the fields in the layout and the worksheet synchronized.</span></span> 

<span data-ttu-id="0ad1c-126">Excel-sniðmátið mun innihalda allar einingar úr útliti fjárhagsáætlunarskjals, þar sem dálkurinn **Tiltækt í Vinnublað** dálkur er stilltur á rétt.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-126">The Excel template will contain all of the elements from the budget plan document layout, where the **Available in Worksheet** column is set to True.</span></span> <span data-ttu-id="0ad1c-127">Einingar sem skarast eru ekki leyfðar í Excel-sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-127">Overlapping elements are not allowed in the Excel template.</span></span> <span data-ttu-id="0ad1c-128">Til dæmis, ef útlitið inniheldur dálkana Request Q1, Request Q2, Request Q3, og Request Q4, og samtölubeiðnadálk sem sýnir samtölu allra 4 ársfjórðungslegra dálka, er aðeins ársfjórðungslegur dálkur eða samtöludálkur tiltækur til notkunar í Excel-sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-128">For example, if the layout contains Request Q1, Request Q2, Request Q3, and Request Q4 columns, and a total request column that represents a sum of all 4 quarterly columns, only the quarterly columns or total column is available to be used in the Excel template.</span></span> <span data-ttu-id="0ad1c-129">Excel-skráin getur ekki uppfært dálka sem skarast á meðan uppfærslu stendur, þar sem gögn í töflunni gætu úrelst og orðið ónákvæm.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-129">The Excel file cannot update overlapping columns during the update because data in the table could become out of date and inaccurate.</span></span>

<span data-ttu-id="0ad1c-130">[![Dæmi](./media/bpt4-1024x615.png)](./media/bpt4.png)</span><span class="sxs-lookup"><span data-stu-id="0ad1c-130">[![Example](./media/bpt4-1024x615.png)](./media/bpt4.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="0ad1c-131">Til að forðast möguleg vandamál við skoðun og breytingar á fjárhagsáætlunargögnum með Excel ætti sami notandi að vera skráður bæði inn í Microsoft Dynamics 365 for Finance and Operations, Enterprise edition og Microsoft Dynamics Office Add-in Data Connector.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-131">To avoid potential issues with viewing and editing budget plan data using Excel, the same user should be logged into both Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and the Microsoft Dynamics Office Add-in Data Connector.</span></span>

## <a name="add-a-header-to-budget-plan-document-template"></a><span data-ttu-id="0ad1c-132">Bæta haus við sniðmát fjárhagsáætlunarskjals.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-132">Add a header to budget plan document template</span></span>
<span data-ttu-id="0ad1c-133">Til að bæta við upplýsingum úr haus velurðu efstu línuna í Excel-skránni og setur inn auðar línur.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-133">To add header information, select the top row in the Excel file and insert empty rows.</span></span> <span data-ttu-id="0ad1c-134">Smellið á **Hönnun** í **Gagnatengli** til að bæta við haussvæðum í Excel-skrá.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-134">Click **Design** in the **Data Connector** to add header fields to the Excel file.</span></span>

<span data-ttu-id="0ad1c-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span><span class="sxs-lookup"><span data-stu-id="0ad1c-135">[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png)</span></span> 

<span data-ttu-id="0ad1c-136">Í flipanum **Hönnun** er smellt á svæðið **Bæta við** og svo valið **BudgetPlanHeader** sem gagnaveita einingar.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-136">In the **Design** tab, click **Add** fields, and then select **BudgetPlanHeader** as the entity data source.</span></span>

<span data-ttu-id="0ad1c-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span><span class="sxs-lookup"><span data-stu-id="0ad1c-137">[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)</span></span>

<span data-ttu-id="0ad1c-138">Settu bendilinn á óskaða staðsetningu í Excel-skránni.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-138">Point the cursor to the desired location in the Excel file.</span></span> <span data-ttu-id="0ad1c-139">Smellt er á **Bæta við merki** til að bæta við svæðidmerki á valda staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-139">Click **Add label** to add the field label to the selected location.</span></span> <span data-ttu-id="0ad1c-140">Veldu **Bæta við gildi** til bæta gildissvæði í valinn svæði.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-140">Select **Add Value** to add the value field to the selected place.</span></span> <span data-ttu-id="0ad1c-141">Smellið síðan á **Gert** til að loka hönnuði.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-141">Click **Done** to close the designer.</span></span>

## <a name="bpt7mediabpt7pngmediabpt7png"></a><span data-ttu-id="0ad1c-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span><span class="sxs-lookup"><span data-stu-id="0ad1c-142">[![bpt7](./media/bpt7.png)](./media/bpt7.png)</span></span>

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a><span data-ttu-id="0ad1c-143">Bæta reiknuðum dálki við sniðmátstöflu fjárhagsáætlunarskjals</span><span class="sxs-lookup"><span data-stu-id="0ad1c-143">Add a calculated column to budget plan document template table</span></span>
--------------------------------------------------------------

<span data-ttu-id="0ad1c-144">Næst verður reiknuðum dálki bætt við myndað sniðmát fjárhagsáætlunarskjals.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-144">Next, calculated columns will be added to generated budget plan document template.</span></span> <span data-ttu-id="0ad1c-145">Dálkur með **samtala beiðni**, sem tekur saman dálkana Beiðni Q1: Beiðni Q4 og dálkur **Leiðrétting**, sem endurreiknar dálk **Samtals Beiðni** með fyrirframskilgreindum þætti.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-145">A **Total request** column, which summarizes Request Q1: Request Q4 columns, and an **Adjustment** column, which recalculates the **Total Request** column by a predefined factor.</span></span>

<span data-ttu-id="0ad1c-146">Smellið á **Hönnun** í **Gagnatengli** til að bæta dálkum við í töfluna.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-146">Click **Design** in the **Data connector** to add columns to the table.</span></span> <span data-ttu-id="0ad1c-147">Smellt er á **Breyta** við hliðina á **BudgetPlanWorksheet** gagnaveita til að byrja að bæta við dálkur.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-147">Click **Edit** next to **BudgetPlanWorksheet** data source to start adding columns.</span></span>

<span data-ttu-id="0ad1c-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span><span class="sxs-lookup"><span data-stu-id="0ad1c-148">[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png)</span></span> 

<span data-ttu-id="0ad1c-149">Valinn svæðaflokkur sýnir þá dálka sem eru í boði í sniðmátinu.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-149">The selected field group displays the columns that are available in the template.</span></span> <span data-ttu-id="0ad1c-150">Smellt er á **Formúla** til að bæta við nýjum dálki við.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-150">Click **Formula** to add a new column.</span></span> <span data-ttu-id="0ad1c-151">Nefndu nýja dálkinn og límdu formúluna síðan inn í svæðið **Formúla**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-151">Name the new column and then paste the formula into the **Formula** field.</span></span> <span data-ttu-id="0ad1c-152">Smellt er á **Uppfæra** til setja dálkinn inn.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-152">Click **Update** to insert the column.</span></span>

<span data-ttu-id="0ad1c-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span><span class="sxs-lookup"><span data-stu-id="0ad1c-153">[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)</span></span>

> [!NOTE] 
> <span data-ttu-id="0ad1c-154">Til að skilgreina formúluna þarf að stofna formúluna í vinnublaðinu og afrita hana síðan í gluggann **Hönnun**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-154">To define the formula, create the formula in the spreadsheet, and then copy it to the **Design** window.</span></span> <span data-ttu-id="0ad1c-155">Bundin tafla í Finance and Operations fær yfirleitt heitið „AXTable1“.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-155">A Finance and Operations bound table will typically be named "AXTable1".</span></span> <span data-ttu-id="0ad1c-156">Til dæmis, til að draga saman dálkana Request Q1 : Request Q4 í vinnubókinni er formúlan = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].</span><span class="sxs-lookup"><span data-stu-id="0ad1c-156">For example, to summarize Request Q1 : Request Q4 columns in the spreadsheet, the formula = AxTable1\[Request Q1\]+AxTable1\[Request Q2\]+AxTable1\[Request Q3\]+AxTable1\[Request Q4\].</span></span>

<span data-ttu-id="0ad1c-157">Endurtaktu þessi skref til að setja inn dálkinn **leiðrétting**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-157">Repeat these steps to insert the **Adjustment** column.</span></span> <span data-ttu-id="0ad1c-158">Notaðu formúla = AxTable1\[Samtals beiðni\]\*$I$1 fyrir þennan dálkur.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-158">Use formula = AxTable1\[Total request\]\*$I$1 for this column.</span></span> <span data-ttu-id="0ad1c-159">Þetta mun taka gildið í hólfi I1 og margfalda gildin í dálknum **Samtals beiðni** til að reikna út leiðréttingarupphæðir.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-159">This will take the value in cell I1 and multiply the values in the **Total request** column to calculate adjustment amounts.</span></span>

<span data-ttu-id="0ad1c-160">Vistaðu og lokaðu Excel-skránni.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-160">Save and close the Excel file.</span></span> <span data-ttu-id="0ad1c-161">Farðu aftur í Finance and Operations og í **Útlit** og smelltu á **Sniðmát &gt; Hlaða upp** til að hlaða upp vistuðu Excel-sniðmáti til að nota fyrir fjárhagsáætlun.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-161">Return to Finance and Operations, and in **Layouts**, click **Template &gt; Upload** to upload the saved Excel template to be used for the budget plan.</span></span> 

<span data-ttu-id="0ad1c-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span><span class="sxs-lookup"><span data-stu-id="0ad1c-162">[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png)</span></span> 

<span data-ttu-id="0ad1c-163">Lokaðu sleðanum **Útlit**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-163">Close the **Layouts** slider.</span></span> <span data-ttu-id="0ad1c-164">Í skjalinu **Fjárhagsáætlun** er smellt á **Vinnublað** til að skoða og breyta fylgiskjali í Excel.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-164">In **Budget plan** document, click **Worksheet** to view and edit the document in Excel.</span></span> <span data-ttu-id="0ad1c-165">Athugaðu að leiðrétta Excel-sniðmát var notað til að stofna þetta vinnublað fjárhagsáætlunar og reiknaðir dálkar eru uppfærðir með formúlunum sem voru skilgreindar í fyrra skrefi.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-165">Note that the adjusted Excel template was used to create this budget plan worksheet and calculated columns are updated using the formulas that were defined in the previous steps.</span></span> 

<span data-ttu-id="0ad1c-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span><span class="sxs-lookup"><span data-stu-id="0ad1c-166">[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)</span></span>

## <a name="tips--tricks-for-creating-budget-plan-templates"></a><span data-ttu-id="0ad1c-167">Ábendingar og ráð fyrir stofnun sniðmáta fjárhagsáætlunargerðar</span><span class="sxs-lookup"><span data-stu-id="0ad1c-167">Tips & tricks for creating budget plan templates</span></span>
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a><span data-ttu-id="0ad1c-168">Get ég bætt viðbótargagnaveitum við sniðmát fjárhagsáætlunar?</span><span class="sxs-lookup"><span data-stu-id="0ad1c-168">Can I add and use additional data sources to a budget plan template?</span></span>

<span data-ttu-id="0ad1c-169">Já, þú getur notað valmyndina **Hönnun** til að bæta við viðbótareiningum við sama eða önnur vinnublöð í Excel-sniðmáti.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-169">Yes, you can use the **Design** menu to add additional entities to the same or other sheets in the Excel template.</span></span> <span data-ttu-id="0ad1c-170">Til dæmis er hægt að bæta við gagnaveitunni **BudgetPlanProposedProject** til að stofna og viðhalda lista yfir fyrirhuguð verk um leið og unnið er með gögn fjárhagsáætlunar í Excel.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-170">For example, you can add the **BudgetPlanProposedProject** data source to create and maintain a list of proposed projects at the same time when working with budget plan data in Excel.</span></span> <span data-ttu-id="0ad1c-171">Athugaðu að ef gagnaveita með miklu magni er notuð getur það haft áhrif á afköst Excel-vinnubókar.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-171">Note that including high-volume data sources might impact performance of the Excel workbook.</span></span> 

<span data-ttu-id="0ad1c-172">Hægt er að nota valkostinn **Sía** í **Gagnatengi** til að bæta við óskuðum síum í viðbættar gagnaveitur.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-172">You can use the **Filter** option in the **Data Connector** to add desired filters to additional data sources.</span></span>

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a><span data-ttu-id="0ad1c-173">Get ég falið valkostinn Hönnun í Gagnatengi fyrir öðrum notendum?</span><span class="sxs-lookup"><span data-stu-id="0ad1c-173">Can I hide the Design option in the Data connector for other users?</span></span>

<span data-ttu-id="0ad1c-174">Já, opnaðu valkosti **Gagnatengis** til að fela valkostinn **Hönnun** fyrir öðrum notendum.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-174">Yes, open the **Data Connector** options to hide the **Design** option from other users.</span></span>

<span data-ttu-id="0ad1c-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span><span class="sxs-lookup"><span data-stu-id="0ad1c-175">[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)</span></span>

<span data-ttu-id="0ad1c-176">Stækka **Valkosti gagnatengis** og hreinsa gátreitinn **Kveikja á hönnun**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-176">Expand **Data connector options** and clear the **Enable design** check box.</span></span> <span data-ttu-id="0ad1c-177">Þetta mun fela valkostinn **Hönnun** úr **Gagnatengi**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-177">This will hide the **Design** option from the **Data connector**.</span></span>

<span data-ttu-id="0ad1c-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span><span class="sxs-lookup"><span data-stu-id="0ad1c-178">[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)</span></span>

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a><span data-ttu-id="0ad1c-179">Get ég hindrað notendur í því að loka gagnatenglinum óvart á meðan unnið er með gögn?</span><span class="sxs-lookup"><span data-stu-id="0ad1c-179">Can I prevent users from accidently closing the Data connector while working with data?</span></span>

<span data-ttu-id="0ad1c-180">Við mælum með því að læsa sniðmátinu til að hindra notendur í að loka því.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-180">We recommend locking the template to prevent users from closing it.</span></span> <span data-ttu-id="0ad1c-181">Til að kveikja á læsingu er smellt á **Gagnatengi**, efst í hægra horninu birtist ör.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-181">To turn on the lock, click the **Data connector**, in the top right corner an arrow appears.</span></span> 

<span data-ttu-id="0ad1c-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span><span class="sxs-lookup"><span data-stu-id="0ad1c-182">[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png)</span></span> 

<span data-ttu-id="0ad1c-183">Smellt er á örina fyrir auka valmynd.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-183">Click the arrow for an additional menu.</span></span> <span data-ttu-id="0ad1c-184">Veldu **Læsa**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-184">Select **Lock**.</span></span>

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a><span data-ttu-id="0ad1c-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span><span class="sxs-lookup"><span data-stu-id="0ad1c-185">[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)</span></span>

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a><span data-ttu-id="0ad1c-186">Get ég notað aðra Excel-eiginleika, eins og hólfasnið, liti, skilyrðisbundin snið, og gröf með sniðmátum fjárhagsáætlunar?</span><span class="sxs-lookup"><span data-stu-id="0ad1c-186">Can I use other Excel features, like cell formatting, colors, conditional formatting, and charts with my budget plan templates?</span></span>

<span data-ttu-id="0ad1c-187">Já, flestir hefðbundir Excel-eiginleikar munu virka í sniðmátum fjárhagsáætlunar.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-187">Yes, most of the standard Excel capabilities will work in budget plan templates.</span></span> <span data-ttu-id="0ad1c-188">Við mælum með því að nota litakóðun fyrir notendur til að gera greinarmun á milli skrifvarinna og breytanlegra dálka.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-188">We recommend using color-coding for users to distinguish between read-only and editable columns.</span></span> <span data-ttu-id="0ad1c-189">Skilyrðisbundin snið má nota til að auðkenna vandamálasvæði í áætluninni.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-189">Conditional formatting can be used to highlight problematic areas of the budget.</span></span> <span data-ttu-id="0ad1c-190">Dálkasamtölur er auðveldlega hægt að sýna með því að nota hefðbundnar Excel-formúlur fyrir ofan töfluna.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-190">Column totals can easily be presented by using standard Excel formulas above the table.</span></span>

<span data-ttu-id="0ad1c-191">Einnig er hægt að stofna og nota snúningstöflur og myndrit fyrir viðbótarflokkaa og myndbirtingar á fjárhagsáætlunargögnum.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-191">You can also create and use pivot tables and charts for additional groupings and visualizations of budget data.</span></span> <span data-ttu-id="0ad1c-192">Á flipanum **Gögn**, í flokknum **Tengingar**, er smellt á **Endurnýja allt**, og síðan er smellt á **Eiginleikar tengingar**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-192">On the **Data** tab, in the **Connections** group, click **Refresh All**, and then click **Connection Properties**.</span></span> <span data-ttu-id="0ad1c-193">Smellt er á flipann **Notkun**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-193">Click the **Usage** tab.</span></span> <span data-ttu-id="0ad1c-194">Undir **Endurhlaða**, velurðu gátreitinn **Endurhlaða gögnum þegar skráin er opnuð**.</span><span class="sxs-lookup"><span data-stu-id="0ad1c-194">Under **Refresh**, select the **Refresh data when opening the file** check box.</span></span> 

<span data-ttu-id="0ad1c-195">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span><span class="sxs-lookup"><span data-stu-id="0ad1c-195">[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)</span></span>




