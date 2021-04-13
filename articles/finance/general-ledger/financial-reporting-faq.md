---
title: Algengar spurningar um fjárhagsskýrslugerð
description: Þetta efnisatriði sýnir spurningar sem tengjast fjárhagsskýrslugerð sem aðrir notendur hafa lagt fram.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: a0718db77399901acc8c88278c5b373b77b3cb16
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5811311"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="386c7-103">Algengar spurningar um fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="386c7-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="386c7-104">Þetta efnisatriði sýnir spurningar sem tengjast fjárhagsskýrslugerð sem aðrir notendur hafa lagt fram.</span><span class="sxs-lookup"><span data-stu-id="386c7-104">This topic lists questions related to financial reporting that other users have had.</span></span> 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="386c7-105">Hvernig takmarka ég aðgang að skýrslu með tréöryggi?</span><span class="sxs-lookup"><span data-stu-id="386c7-105">How do I restrict access to a report using Tree security?</span></span>

<span data-ttu-id="386c7-106">Aðstæður: USMF-sýnifyrirtækið er með skýrslu efnahagsreiknings sem það vill ekki að allir notendur fjárhagsskýrslugerðar geti skoðað í D365.</span><span class="sxs-lookup"><span data-stu-id="386c7-106">Scenario: The USMF demo company has a Balance sheet report that it doesn’t want all Financial reporting users to be able to view in D365.</span></span> <span data-ttu-id="386c7-107">Lausn: Hægt er að nýta sér tréöryggi til að takmarka aðgang að einni skýrslu þannig að aðeins tilteknir notendur geti nálgast skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="386c7-107">Solution: You can utilize Tree security to restrict access to a single report so that only certain users can access the report.</span></span> 

1.  <span data-ttu-id="386c7-108">Skrá inn í skýrsluhönnun fjárhagsskýrslna</span><span class="sxs-lookup"><span data-stu-id="386c7-108">Log into Financial Reporter Report Designer</span></span>

2.  <span data-ttu-id="386c7-109">Stofna nýja Trjáskilgreiningu (Skrá | Nýtt | Trjáskilgreining) a.</span><span class="sxs-lookup"><span data-stu-id="386c7-109">Create a new Tree Definition (File | New | Tree Definition) a.</span></span>    <span data-ttu-id="386c7-110">Tvísmellið á línu **Samantektar** í dálknum **Einingaröryggi**.</span><span class="sxs-lookup"><span data-stu-id="386c7-110">Double-click the **Summary** line in the **Unit Security** column.</span></span>
  <span data-ttu-id="386c7-111">i.</span><span class="sxs-lookup"><span data-stu-id="386c7-111">i.</span></span>    <span data-ttu-id="386c7-112">Smellið á Notendur og hópar.</span><span class="sxs-lookup"><span data-stu-id="386c7-112">Click Users and Groups.</span></span>  
          <span data-ttu-id="386c7-113">1. Veljið notanda/notendur eða hóp sem vill fá aðgang að þessari skýrslu.</span><span class="sxs-lookup"><span data-stu-id="386c7-113">1.    Select the User(s) or Group that would like to access this report.</span></span> 
          
<span data-ttu-id="386c7-114">[![skjár notanda](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span><span class="sxs-lookup"><span data-stu-id="386c7-114">[![user screen](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)</span></span>

<span data-ttu-id="386c7-115">[![öryggisskjár](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span><span class="sxs-lookup"><span data-stu-id="386c7-115">[![security screen](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)</span></span>

  <span data-ttu-id="386c7-116">b.</span><span class="sxs-lookup"><span data-stu-id="386c7-116">b.</span></span>    <span data-ttu-id="386c7-117">Smelltu á **Vista**.</span><span class="sxs-lookup"><span data-stu-id="386c7-117">Click **Save**.</span></span>
  
<span data-ttu-id="386c7-118">[![hnappur til að vista](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span><span class="sxs-lookup"><span data-stu-id="386c7-118">[![save button](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)</span></span>

3.  <span data-ttu-id="386c7-119">Í skýrsluskilgreiningu skal bæta við nýrri trjáskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="386c7-119">In your Report Definition add your new Tree Definition</span></span>

<span data-ttu-id="386c7-120">[![trjáskilgreiningarsnið](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span><span class="sxs-lookup"><span data-stu-id="386c7-120">[![tree definition form](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)</span></span>

<span data-ttu-id="386c7-121">Svar.</span><span class="sxs-lookup"><span data-stu-id="386c7-121">A.</span></span>  <span data-ttu-id="386c7-122">Í trjáskilgreiningunni skal smella á stillingu og undir „Einingaval skipurits“ skal haka í „Taka allar einingar með“</span><span class="sxs-lookup"><span data-stu-id="386c7-122">While in the Tree Definition click on Setting and under “Reporting unit selection” check “Include all units”</span></span>

<span data-ttu-id="386c7-123">[![skjámynd einingavals skipurits](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span><span class="sxs-lookup"><span data-stu-id="386c7-123">[![reporting unit selection form](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)</span></span>

<span data-ttu-id="386c7-124">**Fyrir:** [![fyrir skjáskot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span><span class="sxs-lookup"><span data-stu-id="386c7-124">**Before:** [![before screenshot](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)</span></span>

<span data-ttu-id="386c7-125">**Eftir:** [![eftir skjámynd](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span><span class="sxs-lookup"><span data-stu-id="386c7-125">**After:** [![after screenshot](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)</span></span>

<span data-ttu-id="386c7-126">Athugasemd: Ástæða ofangreindra skilaboða er að notandinn minn hefur ekki aðgang að þessari skýrslu eftir notkun Einingaröryggis</span><span class="sxs-lookup"><span data-stu-id="386c7-126">Note: Reason for the above message is my user does not have access to that report after applying Unit Security</span></span>



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a><span data-ttu-id="386c7-127">Hvernig ákvarða ég hvaða reikningur/reikningar samsvara ekki stöðu minni í D365?</span><span class="sxs-lookup"><span data-stu-id="386c7-127">How do I determine which account(s) do not matching my balances in D365?</span></span>

<span data-ttu-id="386c7-128">Þegar þú ert með skýrslu sem passar ekki við það sem þú ættir að gera ráð fyrir í D365, þá eru hér nokkur skref sem þú gætir tekið til að bera kennsl á þessa reikninga og frávik.</span><span class="sxs-lookup"><span data-stu-id="386c7-128">When you have a report that doesn't match what you would expect in D365, here are some steps you could take to identify those accounts and the variances.</span></span> 

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="386c7-129">Í skýrsluhönnun fjárhagsskýrslna</span><span class="sxs-lookup"><span data-stu-id="386c7-129">In Financial Reporter Report Designer</span></span>

1.  <span data-ttu-id="386c7-130">Búa til nýja línuskilgreiningu a.</span><span class="sxs-lookup"><span data-stu-id="386c7-130">Create a new Row Definition a.</span></span>    <span data-ttu-id="386c7-131">Smella á Breyta | Setja inn línur úr víddum i.</span><span class="sxs-lookup"><span data-stu-id="386c7-131">Click Edit | Insert Rows from Dimensions i.</span></span>  <span data-ttu-id="386c7-132">Veljið MainAccount [![Veljið Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span><span class="sxs-lookup"><span data-stu-id="386c7-132">Select MainAccount [![Select Main screen_](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)</span></span>
    
    <span data-ttu-id="386c7-133">ii.</span><span class="sxs-lookup"><span data-stu-id="386c7-133">ii.</span></span> <span data-ttu-id="386c7-134">Smellið á „Í lagi“ b.</span><span class="sxs-lookup"><span data-stu-id="386c7-134">Click Ok b.</span></span>    <span data-ttu-id="386c7-135">Vista línuskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="386c7-135">Save the Row Definition</span></span>

2.  <span data-ttu-id="386c7-136">Búa til nýja dálkskilgreiningu     [![Búa til nýja dálkskilgreiningu](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span><span class="sxs-lookup"><span data-stu-id="386c7-136">Create a new Column Definition     [![Create a new column definition](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)</span></span>

3.  <span data-ttu-id="386c7-137">Búa til nýja skýrsluskilgreiningu a.</span><span class="sxs-lookup"><span data-stu-id="386c7-137">Create a new Report Definition a.</span></span>    <span data-ttu-id="386c7-138">Smellið á Stillingar og takið hak af [![Stillingagluggi](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span><span class="sxs-lookup"><span data-stu-id="386c7-138">Click Settings and uncheck [![Settings form](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)</span></span>
   
4.  <span data-ttu-id="386c7-139">Mynda skýrslu</span><span class="sxs-lookup"><span data-stu-id="386c7-139">Generate the Report.</span></span> 

5.  <span data-ttu-id="386c7-140">Flytja út skýrslu í Excel.</span><span class="sxs-lookup"><span data-stu-id="386c7-140">Export the Report to Excel.</span></span>

### <a name="in-d365"></a><span data-ttu-id="386c7-141">Í D365:</span><span class="sxs-lookup"><span data-stu-id="386c7-141">In D365:</span></span> 
1.  <span data-ttu-id="386c7-142">Smellið á Fjárhagur | Fyrirspurnir og skýrslur | Prófjöfnuður a.</span><span class="sxs-lookup"><span data-stu-id="386c7-142">Click General Ledger | Inquiries and Reports | Trial Balance a.</span></span>    <span data-ttu-id="386c7-143">Færibreytur i.</span><span class="sxs-lookup"><span data-stu-id="386c7-143">Parameters i.</span></span>  <span data-ttu-id="386c7-144">Frá dagsetningu: upphaf fjárhagsárs ii.</span><span class="sxs-lookup"><span data-stu-id="386c7-144">From Date: Start of Fiscal Year ii.</span></span> <span data-ttu-id="386c7-145">Til dagsetningar: Dagsetning þar sem skýrslan var mynduð fyrir iii.</span><span class="sxs-lookup"><span data-stu-id="386c7-145">To Date: Date you generated the report for iii.</span></span>    <span data-ttu-id="386c7-146">Fjárhagsvíddasamstæðan „Aðallyklasafn“ [![Skjámynd aðallykils](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span><span class="sxs-lookup"><span data-stu-id="386c7-146">Financial Dimension Set “Main Account set” [![Main Account Form](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)</span></span>
      
  <span data-ttu-id="386c7-147">b.</span><span class="sxs-lookup"><span data-stu-id="386c7-147">b.</span></span>    <span data-ttu-id="386c7-148">Smellið á Reikna</span><span class="sxs-lookup"><span data-stu-id="386c7-148">Click Calculate</span></span>

2.  <span data-ttu-id="386c7-149">Flytja út skýrslu í Excel</span><span class="sxs-lookup"><span data-stu-id="386c7-149">Export the report to Excel</span></span>

<span data-ttu-id="386c7-150">Nú ætti að vera hægt að afrita gögnin úr Excel-skýrslu fjárhagsskýrslugerðar yfir í prófjafnaðarskýrslu D365 og bera saman dálka „Lokunarstöðu“.</span><span class="sxs-lookup"><span data-stu-id="386c7-150">You should now be able to copy the data from the FR Excel Report and to the D365 Trial Balance report and compare the “Closing Balance” columns.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]