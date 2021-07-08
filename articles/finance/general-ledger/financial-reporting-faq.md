---
title: Algengar spurningar um fjárhagsskýrslugerð
description: Þetta efnisatriði veitir svör við nokkrum algengum spurningum um fjárhagsskýrslugerð.
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
ms.openlocfilehash: e1b67f86446403933005008a9a1e2cc6739dc516
ms.sourcegitcommit: ecabf43282a3e55f1db40341aa3f3c7950b9e94c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/16/2021
ms.locfileid: "6266634"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="d502f-103">Algengar spurningar um fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="d502f-103">Financial reporting FAQ</span></span>

<span data-ttu-id="d502f-104">Þetta efnisatriði veitir svör við algengum spurningum um fjárhagsskýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="d502f-104">This topic provides answers to frequently asked questions about Financial reporting.</span></span>

## <a name="how-do-i-restrict-access-to-a-report-by-using-tree-security"></a><span data-ttu-id="d502f-105">Hvernig takmarka ég aðgang að skýrslu með öryggistré?</span><span class="sxs-lookup"><span data-stu-id="d502f-105">How do I restrict access to a report by using tree security?</span></span>

<span data-ttu-id="d502f-106">Eftirfarandi dæmi sýnir hvernig hægt er að takmarka aðgang að skýrslu með öryggistré.</span><span class="sxs-lookup"><span data-stu-id="d502f-106">The following example shows how to restrict access to a report by using tree security.</span></span>

<span data-ttu-id="d502f-107">USMF-sýnifyrirtækið er með **efnahagsreikningsskýrslu** sem það vill ekki að allir notendur fjárhagsskýrslugerðar hafi aðgang að.</span><span class="sxs-lookup"><span data-stu-id="d502f-107">The USMF demo company has a **Balance sheet** report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="d502f-108">Hægt er að nota öryggistré til að takmarka aðgang að einni skýrslu þannig að aðeins tilteknir notendur hafi aðgang að henni.</span><span class="sxs-lookup"><span data-stu-id="d502f-108">You can use tree security to restrict access to a single report so that only specific users can access it.</span></span>

1. <span data-ttu-id="d502f-109">Skráðu þig inn á Financial Reporter Report Designer.</span><span class="sxs-lookup"><span data-stu-id="d502f-109">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="d502f-110">Veldu **Skrá \> Ný \> Trjáskilgreining** til að búa til nýja trjáskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="d502f-110">Select **File \> New \> Tree Definition** to create a new tree definition.</span></span>
3. <span data-ttu-id="d502f-111">Pikkaðu tvisvar (eða tvísmelltu) á línuna **Samantekt** í dálknum **Einingaröryggi**.</span><span class="sxs-lookup"><span data-stu-id="d502f-111">Double-tap (or double-click) the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="d502f-112">Veldu **Notendur og hópar**.</span><span class="sxs-lookup"><span data-stu-id="d502f-112">Select **Users and Groups**.</span></span>
5. <span data-ttu-id="d502f-113">Veldu notendur eða hópa sem þurfa aðgang að skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="d502f-113">Select the users or groups that require access to the report.</span></span>
6. <span data-ttu-id="d502f-114">Veldu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="d502f-114">Select **Save**.</span></span>
7. <span data-ttu-id="d502f-115">Í skýrsluskilgreiningu skal bæta við nýrri trjáskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="d502f-115">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="d502f-116">Í trjáskilgreiningunni skal velja **Stilling**.</span><span class="sxs-lookup"><span data-stu-id="d502f-116">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="d502f-117">Síðan undir **Einingaval skipurits** skal velja **taka allar einingar með**.</span><span class="sxs-lookup"><span data-stu-id="d502f-117">Then, under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-dont-match-my-balances"></a><span data-ttu-id="d502f-118">Hvernig auðkenni ég hvaða lyklar passa ekki við stöður mínar?</span><span class="sxs-lookup"><span data-stu-id="d502f-118">How do I identify which accounts don't match my balances?</span></span>

<span data-ttu-id="d502f-119">Ef þú ert með skýrslu sem er ekki með samsvarandi stöðu skaltu nota eftirfarandi ferli til að auðkenna hvern lykil og hvert frávik.</span><span class="sxs-lookup"><span data-stu-id="d502f-119">If you have a report that doesn't have matching balances, use the following procedures to identify each account and variance.</span></span>

### <a name="in-financial-reporter-report-designer"></a><span data-ttu-id="d502f-120">Í Financial Reporter Report Designer</span><span class="sxs-lookup"><span data-stu-id="d502f-120">In Financial Reporter Report Designer</span></span>

1. <span data-ttu-id="d502f-121">Búa til nýja línuskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="d502f-121">Create a new row definition.</span></span>
2. <span data-ttu-id="d502f-122">Veldu **Breyta \> Setja inn línur úr víddum**.</span><span class="sxs-lookup"><span data-stu-id="d502f-122">Select **Edit \> Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="d502f-123">Veldu **MainAccount**.</span><span class="sxs-lookup"><span data-stu-id="d502f-123">Select **MainAccount**.</span></span>
4. <span data-ttu-id="d502f-124">Veldu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="d502f-124">Select **OK**.</span></span>
5. <span data-ttu-id="d502f-125">Vista línuskilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="d502f-125">Save the row definition.</span></span>
6. <span data-ttu-id="d502f-126">Stofna nýja dálkskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="d502f-126">Create a new column definition.</span></span>
7. <span data-ttu-id="d502f-127">Stofna nýja skýrsluskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="d502f-127">Create a new report definition.</span></span>
8. <span data-ttu-id="d502f-128">Veldu **Stillingar** og afveldu þennan valkost.</span><span class="sxs-lookup"><span data-stu-id="d502f-128">Select **Settings** and unmark this option.</span></span>
9. <span data-ttu-id="d502f-129">Mynda skýrslu.</span><span class="sxs-lookup"><span data-stu-id="d502f-129">Generate the report.</span></span> 
10. <span data-ttu-id="d502f-130">Flytja skýrsluna út í Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="d502f-130">Export the report to Microsoft Excel.</span></span>

### <a name="in-dynamics-365-finance"></a><span data-ttu-id="d502f-131">Í Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="d502f-131">In Dynamics 365 Finance</span></span>

1. <span data-ttu-id="d502f-132">Opnaðu **Fjárhagur \> Fyrirspurnir og skýrslur \> Prófjöfnuður**.</span><span class="sxs-lookup"><span data-stu-id="d502f-132">Go to **General ledger \> Inquiries and reports \> Trial balance**.</span></span>
2. <span data-ttu-id="d502f-133">Stilltu eftirfarandi svæði:</span><span class="sxs-lookup"><span data-stu-id="d502f-133">Set the following fields:</span></span>

    - <span data-ttu-id="d502f-134">**Frá dagsetningu** – Færðu inn upphafsdag fjárhagsárs.</span><span class="sxs-lookup"><span data-stu-id="d502f-134">**From Date** – Enter the start date of the fiscal year.</span></span>
    - <span data-ttu-id="d502f-135">**Að dagsetningu** – Færðu inn dagsetninguna sem skýrslan er mynduð fyrir.</span><span class="sxs-lookup"><span data-stu-id="d502f-135">**To Date** – Enter the date that you're generating the report for.</span></span>
    - <span data-ttu-id="d502f-136">**Fjárhagsvídd** – Stilltu þetta svæði á **Aðallykill stilltur**.</span><span class="sxs-lookup"><span data-stu-id="d502f-136">**Financial Dimension** – Set this field to **Main Account set**.</span></span>

3. <span data-ttu-id="d502f-137">Veldu **Reikna út**.</span><span class="sxs-lookup"><span data-stu-id="d502f-137">Select **Calculate**.</span></span>
4. <span data-ttu-id="d502f-138">Flytja út skýrslu í Excel.</span><span class="sxs-lookup"><span data-stu-id="d502f-138">Export the report to Excel.</span></span>

<span data-ttu-id="d502f-139">Nú ætti að vera hægt að afrita gögnin úr Excel-skýrslu Financial Reporter yfir í **prófjafnaðarskýrslu** til að bera saman dálkana **Lokastaða**.</span><span class="sxs-lookup"><span data-stu-id="d502f-139">You should now be able to copy the data from the Financial Reporter Excel report to the **Trial Balance** report, so that you can compare the **Closing Balance** columns.</span></span>

## <a name="when-i-design-a-report-in-report-designer-or-when-i-generate-a-financial-report-i-received-the-following-message-the-operation-could-not-be-completed-due-to-a-problem-in-the-data-provider-framework-how-should-i-respond"></a><span data-ttu-id="d502f-140">Þegar ég hanna skýrslu í Report Designer, eða þegar ég mynda fjárhagsskýrslu, fékk ég eftirfarandi skilaboð: „Ekki var hægt að ljúka við aðgerðina vegna bilunar í gagnaveitukerfi.“</span><span class="sxs-lookup"><span data-stu-id="d502f-140">When I design a report in Report Designer, or when I generate a financial report, I received the following message: "The operation could not be completed due to a problem in the data provider framework."</span></span> <span data-ttu-id="d502f-141">Hvernig ætti ég að svara?</span><span class="sxs-lookup"><span data-stu-id="d502f-141">How should I respond?</span></span>

<span data-ttu-id="d502f-142">Skilaboðin gefa til kynna að vandamál hafi komið upp þegar kerfið reyndi að sækja fjárhagsleg lýsigögn úr gagnaskemmunni á meðan þú notaðir fjárhagsskýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="d502f-142">The message indicates that an issue occurred when the system tried to retrieve financial metadata from the data mart while you were using Financial reporting.</span></span> <span data-ttu-id="d502f-143">Hægt er að leysa úr þessu á tvo vegu:</span><span class="sxs-lookup"><span data-stu-id="d502f-143">There are two ways to respond to this issue:</span></span>

- <span data-ttu-id="d502f-144">Farðu yfir samþættingarstöðu gagnanna með því að fara í **Verkfæri \> Samþættingarstaða** í Report Designer.</span><span class="sxs-lookup"><span data-stu-id="d502f-144">Review the integration status of the data by going to **Tools \> Integration status** in Report Designer.</span></span> <span data-ttu-id="d502f-145">Ef samþættingunni er ekki lokið skaltu bíða þar til henni líkur.</span><span class="sxs-lookup"><span data-stu-id="d502f-145">If the integration is incomplete, wait for it to be completed.</span></span> <span data-ttu-id="d502f-146">Reyndu svo að gera það aftur sem þú varst að gera þegar skilaboðin birtust.</span><span class="sxs-lookup"><span data-stu-id="d502f-146">Then retry what you were doing when you received the message.</span></span>
- <span data-ttu-id="d502f-147">Hafðu samband við notendaþjónustu til að finna vandamálið og lagfæra það.</span><span class="sxs-lookup"><span data-stu-id="d502f-147">Contact Support to identify and work through the issue.</span></span> <span data-ttu-id="d502f-148">Það kann að vera ósamræmi í gögnum í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="d502f-148">There might be inconsistent data in the system.</span></span> <span data-ttu-id="d502f-149">Tæknimenn hjá notendaþjónustu geta aðstoðað þig við að finna vandamálið á þjóninum og þau tilgreindu gögn sem kunna að þarfnast uppfærslu.</span><span class="sxs-lookup"><span data-stu-id="d502f-149">Support engineers can help you identify that issue on the server and find the specific data that might require an update.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
