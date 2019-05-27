---
title: Skipuleggja skýrsluhluta í skýrsluhönnun
description: Eftir hannað höfum einingar og mynduðum skýrslum, það er gagnlegt að skipuleggja þessum hlutum þannig að þeir verði auðveldara fyrir notendum að staðsetja. Þessi skrá er útskýrt hvernig raða fyrirliggjandi skýrslur einingar og hlutum í skýrsluhönnun.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 59161
ms.assetid: 32e728c5-3b06-4049-8070-ade01e951d49
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 3f2b34cccfd84a9e4bb76e7a1da64e5cefa9982e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/15/2019
ms.locfileid: "1551744"
---
# <a name="organize-report-components-in-report-designer"></a><span data-ttu-id="bc98f-104">Skipuleggja skýrsluhluta í skýrsluhönnun</span><span class="sxs-lookup"><span data-stu-id="bc98f-104">Organize report components in report designer</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bc98f-105">Eftir hannað höfum einingar og mynduðum skýrslum, það er gagnlegt að skipuleggja þessum hlutum þannig að þeir verði auðveldara fyrir notendum að staðsetja.</span><span class="sxs-lookup"><span data-stu-id="bc98f-105">After you've designed building blocks and generated reports, it's helpful to organize these objects so that they are easier for users to locate.</span></span> <span data-ttu-id="bc98f-106">Þessi skrá er útskýrt hvernig raða fyrirliggjandi skýrslur einingar og hlutum í skýrsluhönnun.</span><span class="sxs-lookup"><span data-stu-id="bc98f-106">This article explains how to organize existing reports, building blocks, and objects in report designer.</span></span>

<span data-ttu-id="bc98f-107">Hægt að endurnefna möppur, skýrslur, einingar og aðra hluti í skýrsluhönnun til að auðvelda röðun skráa.</span><span class="sxs-lookup"><span data-stu-id="bc98f-107">You can rename folders, reports, building blocks, and other objects in report designer to help organize your files.</span></span> <span data-ttu-id="bc98f-108">Hugsanlega þarf að uppfæra tengingar við þá hluti, allt eftir gerð hlutarins sem var endurnefndur.</span><span class="sxs-lookup"><span data-stu-id="bc98f-108">Depending on the type of object that you rename, you might have to update associations with that object.</span></span>

## <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="bc98f-109">Mappa eða eining endurnefnd í Skýrsluhönnun</span><span class="sxs-lookup"><span data-stu-id="bc98f-109">Rename a folder or building block in Report Designer</span></span>
<span data-ttu-id="bc98f-110">Í Report Designer er hægt að endurnefna möppur, skýrsluskilgreiningar, línuskilgreiningar, dálkskilgreiningar og skipuritsskilgreiningar.</span><span class="sxs-lookup"><span data-stu-id="bc98f-110">In Report Designer, you can rename folders, report definitions, row definitions, column definitions, and reporting tree definitions.</span></span>

### <a name="rename-a-folder-or-building-block-in-report-designer"></a><span data-ttu-id="bc98f-111">Mappa eða eining endurnefnd í Report Designer</span><span class="sxs-lookup"><span data-stu-id="bc98f-111">Rename a folder or building block in Report Designer</span></span>

1. <span data-ttu-id="bc98f-112">Í Report Designer er yfirlitssvæðið notað til að finna möppuna eða hlutinn sem á að endurnefna.</span><span class="sxs-lookup"><span data-stu-id="bc98f-112">In Report Designer, use the navigation pane to locate the folder or object to rename.</span></span>
2. <span data-ttu-id="bc98f-113">Hægrismellið á möppuna eða hlutinn og smellið síðan á **Endurnefna**.</span><span class="sxs-lookup"><span data-stu-id="bc98f-113">Right-click the folder or object, and then click **Rename**.</span></span> <span data-ttu-id="bc98f-114">Reiturinn **Heiti** á yfirlitssvæðinu verður virkur.</span><span class="sxs-lookup"><span data-stu-id="bc98f-114">The **Name** field in the navigation pane becomes available.</span></span>
3. <span data-ttu-id="bc98f-115">Nýja heitið er fært inn og ýtt á færslulykilinn.</span><span class="sxs-lookup"><span data-stu-id="bc98f-115">Type a new name, and then press Enter.</span></span>
4. <span data-ttu-id="bc98f-116">Ef einingin er línuskilgreining, dálkskilgreining eða skipuritsskilgreiningu verður að uppfæra aðrar einingar sem tengjast því.</span><span class="sxs-lookup"><span data-stu-id="bc98f-116">If the building block is a row definition, column definition, or reporting tree definition, you must update other building blocks that are associated with it.</span></span> <span data-ttu-id="bc98f-117">Hægrismellið á eininguna sem var endurnefnt í skrefi 3, veljið **Tengingar** og veljið svo atriði af listanum til að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="bc98f-117">Right-click the building block that you renamed in step 3, select **Associations**, and then select an item in the list to update it.</span></span>
5. <span data-ttu-id="bc98f-118">Endurtakið skref 4 þar til öll tengd atriði hafa verið uppfærð.</span><span class="sxs-lookup"><span data-stu-id="bc98f-118">Repeat step 4 until all associated items are updated.</span></span>

## <a name="create-and-manage-report-groups"></a><span data-ttu-id="bc98f-119">Stofnun og stjórnun skýrsluhópa</span><span class="sxs-lookup"><span data-stu-id="bc98f-119">Create and manage report groups</span></span>
<span data-ttu-id="bc98f-120">Setja má skýrsluskilgreiningar saman í hóp til að mynda margar skýrslur samtímis.</span><span class="sxs-lookup"><span data-stu-id="bc98f-120">You can group report definitions to generate multiple reports at the same time.</span></span> <span data-ttu-id="bc98f-121">Til að stofna, breyta, eyða og mynda skýrsluhópa þarf að hafa hlutverk hönnuðar eða stjórnanda.</span><span class="sxs-lookup"><span data-stu-id="bc98f-121">To create, modify, delete, and generate report groups, you must have the designer or administrator role.</span></span> <span data-ttu-id="bc98f-122">Notendur með hlutverk stofnanda geta myndað skýrsluhópa og geta einnig breytt stillingum skýrsluskilgreininga notanda fyrir skýrsluhópa.</span><span class="sxs-lookup"><span data-stu-id="bc98f-122">Users who have the generator role can generate report groups and can also modify the user report definitions setting for report groups.</span></span>

### <a name="create-a-report-group"></a><span data-ttu-id="bc98f-123">Skýrsluhópur stofnaður</span><span class="sxs-lookup"><span data-stu-id="bc98f-123">Create a report group</span></span>

1. <span data-ttu-id="bc98f-124">Í Skýrsluhönnun er smellt á **Skýrsluhópar** á yfirlitssvæðinu.</span><span class="sxs-lookup"><span data-stu-id="bc98f-124">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="bc98f-125">Á **Skrá** valmyndinni, smellið á **Nýtt** &gt; **Skilgreining skýrsluhóps** til að opna nýjan flokk skýrslu í vafra.</span><span class="sxs-lookup"><span data-stu-id="bc98f-125">On the **File** menu, click **New** &gt; **Report Group Definition** to open a new report group in the viewer window.</span></span> <span data-ttu-id="bc98f-126">Einnig er hægt að smella á **Skýrsluhópur** hnappinn ![Skýrsluhópur](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Skýrsluhópur") á tækjastikunni.</span><span class="sxs-lookup"><span data-stu-id="bc98f-126">Alternatively, click the **Report Group** button ![Report Group](https://i-technet.sec.s-msft.com/dynimg/IC679515.gif "Report Group") on the toolbar.</span></span>
3. <span data-ttu-id="bc98f-127">Smellið á flipann **Skýrsluhópur**. Til að hnekkja upplýsingum úr stökum skýrsluskilgreiningum fyrir myndun þessarar skýrslu skal velja gátreitinn **Hnekkja stillingum fyrirtækis, upplýsinga og dagsetningar úr stökum skýrsluskilgreiningum**.</span><span class="sxs-lookup"><span data-stu-id="bc98f-127">Click the **Report Group** tab. To override the information on the individual report definitions for the generation of this report, select the **Override company, detail, and date settings from individual report definitions** check box.</span></span> <span data-ttu-id="bc98f-128">Heiti fyrirtækis, upplýsingastig, tímabundnar stillingar og dagsetning eru fyllt inn sjálfkrafa en er hægt að uppfæra.</span><span class="sxs-lookup"><span data-stu-id="bc98f-128">The company name, detail level, provisional setting, and date information are entered automatically, but you can make updates.</span></span>
4. <span data-ttu-id="bc98f-129">Veljið gátreitinn **Taka með alla skýrslugjaldmiðla** ef búa á til margar skýrslur með skýrslugjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="bc98f-129">To generate multiple reports that show the reporting currencies, select the **Include all reporting currencies** check box.</span></span> <span data-ttu-id="bc98f-130">Skoðun í mörgum gluggum má fá með því að smella á hnappinn **Gjaldmiðill** í Vefskoðun þegar skýrslan er skoðuð.</span><span class="sxs-lookup"><span data-stu-id="bc98f-130">You can then access multiple views by clicking the **Currency** button in the Web Viewer when you view the report.</span></span>
5. <span data-ttu-id="bc98f-131">Í reitnum **Skýrslur í hóp** skal smella á **Bæta við** til að velja skýrslurnar sem eiga að vera í skýrsluhópnum.</span><span class="sxs-lookup"><span data-stu-id="bc98f-131">In the **Reports in group** field, click **Add** to select the reports to include in the report group.</span></span> <span data-ttu-id="bc98f-132">Til að velja margar skýrslur í svarglugganum **Bæta við** skal halda Ctrl-lyklinum niðri á meðan skýrslur eru valdar.</span><span class="sxs-lookup"><span data-stu-id="bc98f-132">To select multiple reports in the **Add** dialog box, hold down the Ctrl key while you select reports.</span></span> <span data-ttu-id="bc98f-133">Þegar lokið hefur verið val skýrslur, smellið á **í lagi**.</span><span class="sxs-lookup"><span data-stu-id="bc98f-133">When you've finished selecting reports, click **OK**.</span></span>
6. <span data-ttu-id="bc98f-134">Smellið á **Skrá** &gt; **Vista** til að vista nýjan skýrsluhóp.</span><span class="sxs-lookup"><span data-stu-id="bc98f-134">Click **File** &gt; **Save** to save the new report group.</span></span>

### <a name="modify-a-report-group"></a><span data-ttu-id="bc98f-135">Skýrsluhópi breytt</span><span class="sxs-lookup"><span data-stu-id="bc98f-135">Modify a report group</span></span>

1. <span data-ttu-id="bc98f-136">Í Skýrsluhönnun er smellt á **Skýrsluhópar** á yfirlitssvæðinu.</span><span class="sxs-lookup"><span data-stu-id="bc98f-136">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="bc98f-137">Tvísmellið á skýrsluhóp til að breyta.</span><span class="sxs-lookup"><span data-stu-id="bc98f-137">Double-click the report group to modify.</span></span>
3. <span data-ttu-id="bc98f-138">Smellið á flipann **Skýrsluhópur** og breytið því sem þarf.</span><span class="sxs-lookup"><span data-stu-id="bc98f-138">On the **Report Group** tab, make the changes that you want.</span></span>
4. <span data-ttu-id="bc98f-139">Í valmyndinni **Skrá** skal smella á **Vista** til að vista breyttan skýrsluhóp. Einnig er hægt að smella á **Vista** hnappinn ![Vista](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Vista") á tækjastikunni.</span><span class="sxs-lookup"><span data-stu-id="bc98f-139">On the **File** menu, click **Save** to save the modified report group, Alternatively, click the **Save** button ![Save](https://i-technet.sec.s-msft.com/dynimg/IC679516.gif "Save") on the toolbar.</span></span>

> <span data-ttu-id="bc98f-140">[ATHUGASEMD] Ef gerð hefur verið áætlun um myndun skýrslna með tilteknu millibili er hægt að hnekkja þeim stillingum og mynda skýrslu strax.</span><span class="sxs-lookup"><span data-stu-id="bc98f-140">[NOTE] If you've scheduled reports so that they are generated at set intervals, you can override those settings and generate a report immediately.</span></span>

### <a name="generate-a-report-group-report"></a><span data-ttu-id="bc98f-141">Myndun skýrslu í skýrsluhóp</span><span class="sxs-lookup"><span data-stu-id="bc98f-141">Generate a report group report</span></span>

1. <span data-ttu-id="bc98f-142">Í Skýrsluhönnun er smellt á **Skýrsluhópar** á yfirlitssvæðinu.</span><span class="sxs-lookup"><span data-stu-id="bc98f-142">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="bc98f-143">Opnið skýrsluhópinn sem á að mynda.</span><span class="sxs-lookup"><span data-stu-id="bc98f-143">Open the report group to generate.</span></span>
3. <span data-ttu-id="bc98f-144">Smellið á hnappinn **Búa til skýrslu** ![Búa til skýrslu](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Búa til skýrslu") til að búa til skýrslur.</span><span class="sxs-lookup"><span data-stu-id="bc98f-144">Click the **Generate Report** button ![Generate Report](https://i-technet.sec.s-msft.com/dynimg/IC679517.gif "Generate Report") to generate reports.</span></span>

### <a name="delete-a-report-group"></a><span data-ttu-id="bc98f-145">Skýrsluhópi eytt</span><span class="sxs-lookup"><span data-stu-id="bc98f-145">Delete a report group</span></span>

1. <span data-ttu-id="bc98f-146">Í Skýrsluhönnun er smellt á **Skýrsluhópar** á yfirlitssvæðinu.</span><span class="sxs-lookup"><span data-stu-id="bc98f-146">In Report Designer, in the navigation pane, click **Report Groups**.</span></span>
2. <span data-ttu-id="bc98f-147">Hægrismellið á skýrsluhópinn til að eyða og veljið **Eyða**.</span><span class="sxs-lookup"><span data-stu-id="bc98f-147">Right-click the report group to delete, and then select **Delete**.</span></span>
3. <span data-ttu-id="bc98f-148">Þegar staðfestingarskilaboð birtast skal smella á **Já**.</span><span class="sxs-lookup"><span data-stu-id="bc98f-148">When a confirmation message appears, click **Yes**.</span></span>

## <a name="report-group-tab-controls"></a><span data-ttu-id="bc98f-149">Stýringar flipa skýrsluhóps</span><span class="sxs-lookup"><span data-stu-id="bc98f-149">Report Group tab controls</span></span>
<span data-ttu-id="bc98f-150">Eftirfarandi tafla lýsir stýringum í á **Skýrslu Flokkur** flipa.</span><span class="sxs-lookup"><span data-stu-id="bc98f-150">The following table describes the controls on the **Report Group** tab.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="bc98f-151">Eftirlit</span><span class="sxs-lookup"><span data-stu-id="bc98f-151">Control</span></span></th>
<th><span data-ttu-id="bc98f-152">Lýsing</span><span class="sxs-lookup"><span data-stu-id="bc98f-152">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="bc98f-153">Hnekkja stillingum fyrirtækis, upplýsinga og dagsetningar úr stökum skýrsluskilgreiningum</span><span class="sxs-lookup"><span data-stu-id="bc98f-153">Override company, detail, and date settings from individual report definitions</span></span></td>
<td><span data-ttu-id="bc98f-154">Veljið þennan gátreit til að hnekkja stökum skýrsluskilgreiningum skýrslna í þessum skýrsluhópi fyrir myndun þessara skýrslna eingöngu.</span><span class="sxs-lookup"><span data-stu-id="bc98f-154">Select this check box to override individual report definitions of the reports in this report group for the generation of these reports only.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc98f-155">Nafn fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="bc98f-155">Company name</span></span></td>
<td><span data-ttu-id="bc98f-156">Veljið fyrirtækið sem nota á í skýrslunum.</span><span class="sxs-lookup"><span data-stu-id="bc98f-156">Select the company to use for the reports.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc98f-157">Lýsing á stigi</span><span class="sxs-lookup"><span data-stu-id="bc98f-157">Detail level</span></span></td>
<td><span data-ttu-id="bc98f-158">Tilgreinið hvaða upplýsingar eiga að vera í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="bc98f-158">Specify the level of detail that the reports include.</span></span>
<ul>
<li><span data-ttu-id="bc98f-159"><strong>Fjárhagur</strong>− Samantektarskýrsla á háu stigi.</span><span class="sxs-lookup"><span data-stu-id="bc98f-159"><strong>Financial</strong> − A high-level summary report.</span></span> <span data-ttu-id="bc98f-160">Ekki er hægt að kafa niður í reikninga og víddir nema þeim sé bætt við í gegnum skipurit.&#39;</span><span class="sxs-lookup"><span data-stu-id="bc98f-160">You can&#39;t drill down to accounts and dimensions, except for those accounts and dimensions that have been added through a reporting tree.</span></span></li>
<li><span data-ttu-id="bc98f-161"><strong>Fjárhagur &amp; reikningur</strong> − Skýrsla sem inniheldur samantekt á háu stigi með ítarupplýsingum um reikning.</span><span class="sxs-lookup"><span data-stu-id="bc98f-161"><strong>Financial &amp; Account</strong> − A report that contains a high-level summary and account details.</span></span></li>
<li><span data-ttu-id="bc98f-162"><strong>Fjárhagsreikningur &amp; færsla</strong> − Skýrsla sem inniheldur samantekt á háu stigi með ítarupplýsingum um færslur.</span><span class="sxs-lookup"><span data-stu-id="bc98f-162"><strong>Financial, Account, &amp; Transaction</strong> − A report that contains a high-level summary and transaction details.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="bc98f-163">Tímabundið</span><span class="sxs-lookup"><span data-stu-id="bc98f-163">Provisional</span></span></td>
<td><span data-ttu-id="bc98f-164">Tilgreinið hvaða verkþættir eiga að vera í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="bc98f-164">Specify the types of activity that the reports include.</span></span>
<ul>
<li><span data-ttu-id="bc98f-165"><strong>Aðeins bókaðir verkþættir</strong> − Inniheldur aðeins færslur og stöðu sem eru bókaðar í fjárhagsgögnum.</span><span class="sxs-lookup"><span data-stu-id="bc98f-165"><strong>Posted activity only</strong> − Include only the transactions and balances that are posted in your financial data.</span></span></li>
<li><span data-ttu-id="bc98f-166"><strong>Bókaðir og óbókaðir verkþættir</strong>− Inniheldur allar færslur og stöðu sem eru slegin inn og bókað í fjárhagsgögnum.</span><span class="sxs-lookup"><span data-stu-id="bc98f-166"><strong>Posted and unposted activity</strong> − Include all the transactions and balances that are entered and posted in your financial data.</span></span></li>
<li><span data-ttu-id="bc98f-167"><strong>Aðeins óbókaðir verkþættir</strong> − Inniheldur aðeins færslur sem hefur veriðs legin inn, en sem hefur ekki verið bókuð í fjárhagsgögn.</span><span class="sxs-lookup"><span data-stu-id="bc98f-167"><strong>Unposted activity only</strong> − Include only the transactions that are entered, but not yet posted, in your financial data.</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="bc98f-168">Taka með alla skýrslugjaldmiðla</span><span class="sxs-lookup"><span data-stu-id="bc98f-168">Include all reporting currencies</span></span></td>
<td><span data-ttu-id="bc98f-169">Ef aðrir skýrslugjaldmiðlar eru grunnstilltir í ERP-kerfi Microsoft Dynamics eru þeir taldir upp hér.</span><span class="sxs-lookup"><span data-stu-id="bc98f-169">Any additional reporting currencies that are configured in your Microsoft Dynamics ERP system are listed here.</span></span> <span data-ttu-id="bc98f-170">Veljið gátreit til að mynda viðbótarskýrslur í tilgreindum gjaldmiðlum.</span><span class="sxs-lookup"><span data-stu-id="bc98f-170">Select this check box to generate additional reports in the currencies that are indicated.</span></span> <span data-ttu-id="bc98f-171">Til að skoða þessar skýrslur í Web Viewer er smellt á <strong>Gjaldmiðill</strong> hnappinn og svo valinn gjaldmiðill.</span><span class="sxs-lookup"><span data-stu-id="bc98f-171">To view these reports in the Web Viewer, click the <strong>Currency</strong> button, and then select a currency.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc98f-172">Upplýsingar um dagsetningu ekki vistaðar með skýrsluskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="bc98f-172">Date information not saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="bc98f-173">Grunntímabil</span><span class="sxs-lookup"><span data-stu-id="bc98f-173">Base period</span></span></li>
<li><span data-ttu-id="bc98f-174">Grunnár</span><span class="sxs-lookup"><span data-stu-id="bc98f-174">Base year</span></span></li>
<li><span data-ttu-id="bc98f-175">Tímabil</span><span class="sxs-lookup"><span data-stu-id="bc98f-175">Period covered</span></span></li>
</ul>
<span data-ttu-id="bc98f-176">Aðeins stillingar sjálfgefins grunntímabils eru vistaðar með skýrsluskilgreiningunni.</span><span class="sxs-lookup"><span data-stu-id="bc98f-176">Only default base period settings are saved with the report definition.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="bc98f-177">Upplýsingar um dagsetningu vistaðar með skýrsluskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="bc98f-177">Date information saved with report definition</span></span></td>
<td><ul>
<li><span data-ttu-id="bc98f-178">Dagsetning skýrslu</span><span class="sxs-lookup"><span data-stu-id="bc98f-178">Report date</span></span></li>
<li><span data-ttu-id="bc98f-179">Sjálfgefið grunntímabil</span><span class="sxs-lookup"><span data-stu-id="bc98f-179">Default base period</span></span></li>
</ul></td>
</tr>
<tr>
<td><span data-ttu-id="bc98f-180">Skýrslur í hóp</span><span class="sxs-lookup"><span data-stu-id="bc98f-180">Reports in group</span></span></td>
<td><span data-ttu-id="bc98f-181">Bæta við, fjarlægja og endurpanta skýrslur í skýrsluhópnum.</span><span class="sxs-lookup"><span data-stu-id="bc98f-181">Add, remove, and re-order reports in the report group.</span></span>
<ul>
<li><span data-ttu-id="bc98f-182">Til að bæta skýrsluskilgreiningum við skýrsluhóp er tvísmellt á skýrsluhópinn til að opna hann og svo smellt á <strong>Bæta við</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc98f-182">To add report definitions to the report group, double-click the report group to open it, and then click <strong>Add</strong>.</span></span> <span data-ttu-id="bc98f-183">Veljið skýrslurnar sem á að hafa með í skýrsluhópnum og smellið svo á <strong>Í lagi</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc98f-183">Select the reports to include in the report group, and then click <strong>OK</strong>.</span></span></li>
<li><span data-ttu-id="bc98f-184">Til að fjarlægja skýrslu úr skýrsluhópi er skýrslan valin og smellt á <strong>Fjarlægja</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc98f-184">To remove a report from the report group, select it, and then click <strong>Remove</strong>.</span></span></li>
<li><span data-ttu-id="bc98f-185">Til að breyta því í hvaða röð skýrslurnar eru myndaðar er skýrsla valin á listanum og síðan smellt á <strong>Flytja upp</strong> eða <strong>Flytja niður</strong>.</span><span class="sxs-lookup"><span data-stu-id="bc98f-185">To modify the order that the reports are generated in, select a report in the list, and then click <strong>Move up</strong> or <strong>Move down</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="bc98f-186">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="bc98f-186">Additional resources</span></span>

[<span data-ttu-id="bc98f-187">Fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="bc98f-187">Financial reporting</span></span>](financial-reporting-intro.md)
