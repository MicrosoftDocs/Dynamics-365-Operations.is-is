---
title: "Skipuleggja skýrsluhluta í skýrsluhönnun"
description: "Eftir hannað höfum einingar og mynduðum skýrslum, það er gagnlegt að skipuleggja þessum hlutum þannig að þeir verði auðveldara fyrir notendum að staðsetja. Þessi skrá er útskýrt hvernig raða fyrirliggjandi skýrslur einingar og hlutum í skýrsluhönnun."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Management Reporter, UnifiedOperations, Core
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: fade9e2acdb94daa6a908d949c578fd7ed439882
ms.contentlocale: is-is
ms.lasthandoff: 07/18/2017

---

# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="84983-104">Skipuleggja skýrsluhluta í skýrsluhönnun</span><span class="sxs-lookup"><span data-stu-id="84983-104">Organize report components in report designer</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="84983-105">Eftir hannað höfum einingar og mynduðum skýrslum, það er gagnlegt að skipuleggja þessum hlutum þannig að þeir verði auðveldara fyrir notendum að staðsetja.</span><span class="sxs-lookup"><span data-stu-id="84983-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="84983-106">Þessi skrá er útskýrt hvernig raða fyrirliggjandi skýrslur einingar og hlutum í skýrsluhönnun.</span><span class="sxs-lookup"><span data-stu-id="84983-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="84983-107">Hægt að endurnefna möppur, skýrslur, einingar og aðra hluti í skýrsluhönnun til að auðvelda röðun skráa.</span><span class="sxs-lookup"><span data-stu-id="84983-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="84983-108">Hugsanlega þarf að uppfæra tengingar við þá hluti, allt eftir gerð hlutarins sem var endurnefndur.</span><span class="sxs-lookup"><span data-stu-id="84983-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="84983-109">Mappa eða eining endurnefnd í Skýrsluhönnun</span><span class="sxs-lookup"><span data-stu-id="84983-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="84983-110">Í Skýrsluhönnun er hægt að endurnefna möppur, skýrsluskilgreiningar, línuskilgreiningar, dálkskilgreiningar og skipuritsskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="84983-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span> <span data-ttu-id="84983-111">**Athugasemd:** Þegar eining endurnefna þarf að uppfæra skýrslugerð skilgreiningar sem nota eininguna.</span><span class="sxs-lookup"><span data-stu-id="84983-111">**Note:** When you rename a building block, you must update any reporting definitions that use the building block.</span></span> <span data-ttu-id="84983-112">Annars er ekki hægt að mynda nýja skýrslu.</span><span class="sxs-lookup"><span data-stu-id="84983-112">Otherwise, a new report can't be generated.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="84983-113">Mappa eða eining endurnefnd í Skýrsluhönnun</span><span class="sxs-lookup"><span data-stu-id="84983-113">Rename a folder or building block in Report Designer</span></span>

1.  <span data-ttu-id="84983-114">Í Skýrsluhönnun er yfirlitssvæðið notað til að finna möppuna eða hlutinn sem á að endurnefna.</span><span class="sxs-lookup"><span data-stu-id="84983-114">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2.  <span data-ttu-id="84983-115">Hægrismellið á möppuna eða hlutinn og smellið síðan á **Endurnefna**.</span><span class="sxs-lookup"><span data-stu-id="84983-115">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="84983-116">Reiturinn **Heiti** á yfirlitssvæðinu verður virkur.</span><span class="sxs-lookup"><span data-stu-id="84983-116">The **Name** field in the navigation pane becomes available.</span></span>
3.  <span data-ttu-id="84983-117">Nýja heitið er fært inn og ýtt á færslulykilinn.</span><span class="sxs-lookup"><span data-stu-id="84983-117">Type a new name, and then press Enter.</span></span>
4.  <span data-ttu-id="84983-118">Ef einingin er línuskilgreining, dálkskilgreining eða skipuritsskilgreiningu verður að uppfæra aðrar einingar sem tengjast því.</span><span class="sxs-lookup"><span data-stu-id="84983-118">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="84983-119">Hægrismellið á eininguna sem var endurnefnt í skrefi 3, veljið **Tengingar** og veljið svo atriði af listanum til að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="84983-119">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5.  <span data-ttu-id="84983-120">Endurtakið skref 4 þar til öll tengd atriði hafa verið uppfærð.</span><span class="sxs-lookup"><span data-stu-id="84983-120">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="84983-121">Stofnun og stjórnun skýrsluhópa</span><span class="sxs-lookup"><span data-stu-id="84983-121">Create and manage report groups</span></span>
<span data-ttu-id="84983-122">Setja má skýrsluskilgreiningar saman í hóp til að mynda margar skýrslur samtímis.</span><span class="sxs-lookup"><span data-stu-id="84983-122">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="84983-123">Til að stofna, breyta, eyða og mynda skýrsluhópa þarf að hafa hlutverk hönnuðar eða stjórnanda.</span><span class="sxs-lookup"><span data-stu-id="84983-123">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="84983-124">Notendur með hlutverk stofnanda geta myndað skýrsluhópa og geta einnig breytt stillingum skýrsluskilgreininga notanda fyrir skýrsluhópa.</span><span class="sxs-lookup"><span data-stu-id="84983-124">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="84983-125">Skýrsluhópur stofnaður</span><span class="sxs-lookup"><span data-stu-id="84983-125">Create a report group</span></span>

1.  <span data-ttu-id="84983-126">Í Skýrsluhönnun er smellt á **Skýrsluhópar** á yfirlitssvæðinu.</span><span class="sxs-lookup"><span data-stu-id="84983-126">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="84983-127">Á **Skrá** valmyndinni, smellið á **Nýtt** &gt; **Skilgreining skýrsluhóps** til að opna nýjan flokk skýrslu í vafra.</span><span class="sxs-lookup"><span data-stu-id="84983-127">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="84983-128">Einnig er hægt að smella á **Skýrsluhópur** hnappinn ![Skýrsluhópur](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Skýrsluhópur") á tækjastikunni.</span><span class="sxs-lookup"><span data-stu-id="84983-128">Alternatively, click the **Report Group** button ![Report Group](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Report Group") on the toolbar.</span></span>
3.  <span data-ttu-id="84983-129">Smellið á flipann **Skýrsluhópur**.</span><span class="sxs-lookup"><span data-stu-id="84983-129">Click the **Report Group** tab.</span></span> <span data-ttu-id="84983-130">Til að hnekkja upplýsingum úr stökum skýrsluskilgreiningum fyrir myndun þessarar skýrslu skal velja gátreitinn **Hnekkja stillingum fyrirtækis, upplýsinga og dagsetningar úr stökum skýrsluskilgreiningum**.</span><span class="sxs-lookup"><span data-stu-id="84983-130">To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="84983-131">Heiti fyrirtækis, upplýsingastig, tímabundnar stillingar og dagsetning eru fyllt inn sjálfkrafa en er hægt að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="84983-131">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4.  <span data-ttu-id="84983-132">Veljið gátreitinn **Taka með alla skýrslugjaldmiðla** ef búa á til margar skýrslur með skýrslugjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="84983-132">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="84983-133">Skoðun í mörgum gluggum má fá með því að smella á hnappinn **Gjaldmiðill** í Vefskoðun þegar skýrslan er skoðuð.</span><span class="sxs-lookup"><span data-stu-id="84983-133">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5.  <span data-ttu-id="84983-134">Í reitnum **Skýrslur í hóp** skal smella á **Bæta við** til að velja skýrslurnar sem eiga að vera í skýrsluhópnum.</span><span class="sxs-lookup"><span data-stu-id="84983-134">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="84983-135">Til að velja margar skýrslur í svarglugganum **Bæta við** skal halda Ctrl-lyklinum niðri á meðan skýrslur eru valdar.</span><span class="sxs-lookup"><span data-stu-id="84983-135">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="84983-136">Þegar lokið hefur verið val skýrslur, smellið á **í lagi**.</span><span class="sxs-lookup"><span data-stu-id="84983-136">When you've finished selecting reports, click **OK**.</span></span>
6.  <span data-ttu-id="84983-137">Smellið á **Skrá** &gt; **Vista** til að vista nýjan skýrsluhóp.</span><span class="sxs-lookup"><span data-stu-id="84983-137">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="84983-138">Skýrsluhópi breytt</span><span class="sxs-lookup"><span data-stu-id="84983-138">Modify a report group</span></span>

1.  <span data-ttu-id="84983-139">Í Skýrsluhönnun er smellt á **Skýrsluhópar** á yfirlitssvæðinu.</span><span class="sxs-lookup"><span data-stu-id="84983-139">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="84983-140">Tvísmellið á skýrsluhóp til að breyta.</span><span class="sxs-lookup"><span data-stu-id="84983-140">Double-click the report group to modify.</span></span>
3.  <span data-ttu-id="84983-141">Smellið á flipann **Skýrsluhópur** og breytið því sem þarf.</span><span class="sxs-lookup"><span data-stu-id="84983-141">On the **Report Group** tab, make the changes that you want.</span></span>
4.  <span data-ttu-id="84983-142">Í valmyndinni **Skrá** skal smella á **Vista** til að vista breyttan skýrsluhóp. Einnig er hægt að smella á **Vista** hnappinn ![Vista](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Vista") á tækjastikunni.</span><span class="sxs-lookup"><span data-stu-id="84983-142">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Save") on the toolbar.</span></span>

<span data-ttu-id="84983-143">**athugasemd:** Ef gerð hefur verið áætlun um myndun skýrslna með tilteknu millibili í stillingum skýrsluskilgreiningar er hægt að hnekkja þeim stillingum og mynda skýrslu strax.</span><span class="sxs-lookup"><span data-stu-id="84983-143">**Note:** If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="84983-144">Myndun skýrslu í skýrsluhóp</span><span class="sxs-lookup"><span data-stu-id="84983-144">Generate a report group report</span></span>

1.  <span data-ttu-id="84983-145">Í Skýrsluhönnun er smellt á **Skýrsluhópar** á yfirlitssvæðinu.</span><span class="sxs-lookup"><span data-stu-id="84983-145">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="84983-146">Opnið skýrsluhópinn sem á að mynda.</span><span class="sxs-lookup"><span data-stu-id="84983-146">Open the report group to generate.</span></span>
3.  <span data-ttu-id="84983-147">Smellið á hnappinn **Búa til skýrslu** ![Búa til skýrslu](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Búa til skýrslu") til að búa til skýrslur.</span><span class="sxs-lookup"><span data-stu-id="84983-147">Click the **Generate Report** button ![Generate Report](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="84983-148">Skýrsluhópi eytt</span><span class="sxs-lookup"><span data-stu-id="84983-148">Delete a report group</span></span>

1.  <span data-ttu-id="84983-149">Í Skýrsluhönnun er smellt á **Skýrsluhópar** á yfirlitssvæðinu.</span><span class="sxs-lookup"><span data-stu-id="84983-149">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2.  <span data-ttu-id="84983-150">Hægrismellið á skýrsluhópinn til að eyða og veljið **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="84983-150">Right-click the report group to delete, and then select **Delete**.</span></span>
3.  <span data-ttu-id="84983-151">Þegar staðfestingarskilaboð birtast skal smella á **Já**.</span><span class="sxs-lookup"><span data-stu-id="84983-151">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="84983-152">Stýringar flipa skýrsluhóps</span><span class="sxs-lookup"><span data-stu-id="84983-152">Report Group tab controls</span></span>
<span data-ttu-id="84983-153">Eftirfarandi tafla lýsir stýringum í á **Skýrslu Flokkur** flipa.</span><span class="sxs-lookup"><span data-stu-id="84983-153">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="84983-154">Eftirlit</span><span class="sxs-lookup"><span data-stu-id="84983-154">Control</span></span></th>
<th><span data-ttu-id="84983-155">Lýsing</span><span class="sxs-lookup"><span data-stu-id="84983-155">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84983-156">Hnekkja stillingum fyrirtækis, upplýsinga og dagsetningar úr stökum skýrsluskilgreiningum</span><span class="sxs-lookup"><span data-stu-id="84983-156">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="84983-157">Veljið þennan gátreit til að hnekkja stökum skýrsluskilgreiningum skýrslna í þessum skýrsluhópi fyrir myndun þessara skýrslna eingöngu.</span><span class="sxs-lookup"><span data-stu-id="84983-157">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84983-158">Nafn fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="84983-158">Company name</span></span></td>
<td><span data-ttu-id="84983-159">Veljið fyrirtækið sem nota á í skýrslunum.</span><span class="sxs-lookup"><span data-stu-id="84983-159">Select the company to use for the reports.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84983-160">Lýsing á stigi</span><span class="sxs-lookup"><span data-stu-id="84983-160">Detail level</span></span></td>
<td><span data-ttu-id="84983-161">Tilgreinið hvaða upplýsingar eiga að vera í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="84983-161">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="84983-162"><strong>Fjárhagur</strong>− Samantektarskýrsla á háu stigi.</span><span class="sxs-lookup"><span data-stu-id="84983-162"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="84983-163">Ekki er hægt að kafa niður í reikninga og víddir nema þeim sé bætt við í gegnum skipurit.</span><span class="sxs-lookup"><span data-stu-id="84983-163">You can't drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="84983-164"><strong>Fjárhagur &amp; reikningur</strong> − Skýrsla sem inniheldur samantekt á háu stigi með ítarupplýsingum um reikning.</span><span class="sxs-lookup"><span data-stu-id="84983-164"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="84983-165"><strong>Fjárhagsreikningur &amp; færsla</strong> − Skýrsla sem inniheldur samantekt á háu stigi með ítarupplýsingum um færslur.</span><span class="sxs-lookup"><span data-stu-id="84983-165"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84983-166">Tímabundið</span><span class="sxs-lookup"><span data-stu-id="84983-166">Provisional</span></span></td>
<td><span data-ttu-id="84983-167">Tilgreinið hvaða verkþættir eiga að vera í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="84983-167">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="84983-168"><strong>Aðeins bókaðar aðgerðir</strong>− Inniheldur aðeins færslur og innistæður sem eru bókaðar í fjárhagsgögnunum.</span><span class="sxs-lookup"><span data-stu-id="84983-168"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="84983-169"><strong>Bókaðar og óbókaðar aðgerðir</strong>− Inniheldur allar færslur og innistæður sem eru færðar inn og bókaðar í fjárhagsgögnunum.</span><span class="sxs-lookup"><span data-stu-id="84983-169"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="84983-170"><strong>Aðeins óbókaðar aðgerðir</strong>− Inniheldur aðeins færslur sem eru færðar inn en eru ekki enn bókaðar í fjárhagsgögnunum.</span><span class="sxs-lookup"><span data-stu-id="84983-170"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84983-171">Taka með alla skýrslugjaldmiðla</span><span class="sxs-lookup"><span data-stu-id="84983-171">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="84983-172">Ef aðrir skýrslugjaldmiðlar eru grunnstilltir í ERP-kerfi Microsoft Dynamics eru þeir taldir upp hér.</span><span class="sxs-lookup"><span data-stu-id="84983-172">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="84983-173">Veljið gátreit til að mynda viðbótarskýrslur í tilgreindum gjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="84983-173">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="84983-174">Hægt er að skoða skýrslurnar í Vefskoðun með því að smella á hnappinn <strong>Gjaldmiðill</strong> og velja gjaldmiðil.</span><span class="sxs-lookup"><span data-stu-id="84983-174">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84983-175">Upplýsingar um dagsetningu ekki vistaðar með skýrsluskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="84983-175">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="84983-176">Grunntímabil</span><span class="sxs-lookup"><span data-stu-id="84983-176">Base period</span></span></li>
<li><span data-ttu-id="84983-177">Grunnár</span><span class="sxs-lookup"><span data-stu-id="84983-177">Base year</span></span></li>
<li><span data-ttu-id="84983-178">Tímabil</span><span class="sxs-lookup"><span data-stu-id="84983-178">Period covered</span></span></li>
</ul>
<span data-ttu-id="84983-179">Aðeins stillingar sjálfgefins grunntímabils eru vistaðar með skýrsluskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="84983-179">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84983-180">Upplýsingar um dagsetningu vistaðar með skýrsluskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="84983-180">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="84983-181">Dagsetning skýrslu</span><span class="sxs-lookup"><span data-stu-id="84983-181">Report date</span></span></li>
<li><span data-ttu-id="84983-182">Sjálfgefið grunntímabil</span><span class="sxs-lookup"><span data-stu-id="84983-182">Default base period</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84983-183">Skýrslur í hóp</span><span class="sxs-lookup"><span data-stu-id="84983-183">Reports in group</span></span></td>
<td><span data-ttu-id="84983-184">Bæta við, fjarlægja og endurpanta skýrslur í skýrsluhópnum.</span><span class="sxs-lookup"><span data-stu-id="84983-184">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="84983-185">Til að bæta skýrsluskilgreiningum við skýrsluhóp er tvísmellt á skýrsluhópinn til að opna hann og svo smellt á <strong>Bæta við</strong>.</span><span class="sxs-lookup"><span data-stu-id="84983-185">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="84983-186">Veljið skýrslurnar sem á að hafa með í skýrsluhópnum og smellið svo á <strong>Í lagi</strong>.</span><span class="sxs-lookup"><span data-stu-id="84983-186">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="84983-187">Til að fjarlægja skýrslu úr skýrsluhópi er skýrslan valin og smellt á <strong>Fjarlægja</strong>.</span><span class="sxs-lookup"><span data-stu-id="84983-187">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="84983-188">Til að breyta því í hvaða röð skýrslurnar eru myndaðar er skýrsla valin á listanum og síðan smellt á <strong>Flytja upp</strong> eða <strong>Flytja niður</strong>.</span><span class="sxs-lookup"><span data-stu-id="84983-188">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



<a name="see-also"></a><span data-ttu-id="84983-189">Sjá einnig</span><span class="sxs-lookup"><span data-stu-id="84983-189">See also</span></span>
--------

[<span data-ttu-id="84983-190">Fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="84983-190">Financial reporting</span></span>](financial-reporting-intro.md)




