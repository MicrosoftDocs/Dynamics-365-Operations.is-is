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
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923026"
---
# <a name="financial-reporting-faq"></a><span data-ttu-id="b4699-103">Algengar spurningar um fjárhagsskýrslugerð</span><span class="sxs-lookup"><span data-stu-id="b4699-103">Financial reporting FAQ</span></span> 

<span data-ttu-id="b4699-104">Þetta efnisatriði veitir svör við algengum spurningum um fjárhagsskýrslugerð.</span><span class="sxs-lookup"><span data-stu-id="b4699-104">This topic provides answers to frequently asked questions about financial reporting.</span></span> 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a><span data-ttu-id="b4699-105">Hvernig takmarka ég aðgang að skýrslu með öryggistré?</span><span class="sxs-lookup"><span data-stu-id="b4699-105">How do I restrict access to a report using tree security?</span></span>

<span data-ttu-id="b4699-106">Eftirfarandi dæmi sýnir hvernig hægt er að takmarka aðgang að skýrslu með öryggistré.</span><span class="sxs-lookup"><span data-stu-id="b4699-106">The following example shows how to restrict access to a report using tree security.</span></span>

<span data-ttu-id="b4699-107">USMF-sýnifyrirtækið er með skýrslu efnahagsreiknings sem það vill ekki að allir notendur fjárhagsskýrslugerðar geti skoðað.</span><span class="sxs-lookup"><span data-stu-id="b4699-107">The USMF demo company has a Balance sheet report that not all Financial reporting users should have access to.</span></span> <span data-ttu-id="b4699-108">Hægt er að nota öryggistré til að takmarka aðgang að einni skýrslu þannig að aðeins tilteknir notendur geti nálgast skýrsluna.</span><span class="sxs-lookup"><span data-stu-id="b4699-108">To restrict access, you can use tree security to restrict access to a single report so that only certain users can access the report.</span></span> <span data-ttu-id="b4699-109">Fylgdu eftirfarandi leiðbeiningum til að takmarka aðgang:</span><span class="sxs-lookup"><span data-stu-id="b4699-109">Follow these steps to restrict access:</span></span> 

1. <span data-ttu-id="b4699-110">Skráðu þig inn í skýrsluhönnun fjárhagsskýrslna.</span><span class="sxs-lookup"><span data-stu-id="b4699-110">Sign in to Financial Reporter Report Designer.</span></span>
2. <span data-ttu-id="b4699-111">Stofnaðu nýja trésskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="b4699-111">Create a new tree definition.</span></span> <span data-ttu-id="b4699-112">Opnaðu **Skrá > Nýtt > Trésskilgreining**.</span><span class="sxs-lookup"><span data-stu-id="b4699-112">Go to **File > New > Tree Definition**.</span></span>
3. <span data-ttu-id="b4699-113">Tvísmellið á línuna **Samantekt** í dálknum **Einingaröryggi**.</span><span class="sxs-lookup"><span data-stu-id="b4699-113">Double-click the **Summary** line in the **Unit Security** column.</span></span>
4. <span data-ttu-id="b4699-114">Veldu **Notendur og hópar**.</span><span class="sxs-lookup"><span data-stu-id="b4699-114">Select **Users and Groups**.</span></span>  
5. <span data-ttu-id="b4699-115">Veldu notendur eða hópa sem þurfa aðgang að þessari skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b4699-115">Select the users or groups that need access to this report.</span></span> 
6. <span data-ttu-id="b4699-116">Veldu **Vista**.</span><span class="sxs-lookup"><span data-stu-id="b4699-116">Select **Save**.</span></span>
7. <span data-ttu-id="b4699-117">Í skýrsluskilgreiningu skal bæta við nýrri trésskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="b4699-117">In the report definition, add your new tree definition.</span></span>
8. <span data-ttu-id="b4699-118">Í trésskilgreiningunni skal velja **Stilling**.</span><span class="sxs-lookup"><span data-stu-id="b4699-118">In the tree definition, select **Setting**.</span></span> <span data-ttu-id="b4699-119">Undir **Einingaval skipurits** skal velja **taka allar einingar með**.</span><span class="sxs-lookup"><span data-stu-id="b4699-119">Under **Reporting unit selection**, select **Include all units**.</span></span>

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a><span data-ttu-id="b4699-120">Hvernig auðkenni ég lykla sem passa ekki við stöður?</span><span class="sxs-lookup"><span data-stu-id="b4699-120">How do I identify which accounts do not match my balances?</span></span>

<span data-ttu-id="b4699-121">Ef þú ert með skýrslu sem er ekki með samsvarandi stöðu geturðu gert eftirfarandi til að auðkenna hvern lykil og hvert frávik.</span><span class="sxs-lookup"><span data-stu-id="b4699-121">If you have a report that doesn't have matching balances, here are some steps you can take to identify each of the accounts and variances.</span></span> 

<span data-ttu-id="b4699-122">**Skýrsluhönnun fjárhagsskýrslna**</span><span class="sxs-lookup"><span data-stu-id="b4699-122">**Financial Reporter Report Designer**</span></span>
1. <span data-ttu-id="b4699-123">Í skýrsluhönnun fjárhagsskýrslna skal stofna nýja línuskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="b4699-123">In Financial Reporter Report Designer, create a new row definition.</span></span> 
2. <span data-ttu-id="b4699-124">Veljið **Breyta > Setja inn línur úr víddum**.</span><span class="sxs-lookup"><span data-stu-id="b4699-124">Select **Edit > Insert Rows from Dimensions**.</span></span>
3. <span data-ttu-id="b4699-125">Veljið **Aðallykill**.</span><span class="sxs-lookup"><span data-stu-id="b4699-125">Select **MainAccount**.</span></span>  
4. <span data-ttu-id="b4699-126">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="b4699-126">Select **OK**.</span></span>
5. <span data-ttu-id="b4699-127">Vistið línuskilgreininguna.</span><span class="sxs-lookup"><span data-stu-id="b4699-127">Save the row definition.</span></span>
6. <span data-ttu-id="b4699-128">Stofna nýja dálkskilgreiningu</span><span class="sxs-lookup"><span data-stu-id="b4699-128">Create a new column definition</span></span>
7. <span data-ttu-id="b4699-129">Stofna nýja skýrsluskilgreiningu.</span><span class="sxs-lookup"><span data-stu-id="b4699-129">Create a new report definition.</span></span>
8. <span data-ttu-id="b4699-130">Veljið **Stillingar** og afveljið þennan valkost.</span><span class="sxs-lookup"><span data-stu-id="b4699-130">Select **Settings** and unmark this option.</span></span>  
9. <span data-ttu-id="b4699-131">Mynda skýrslu.</span><span class="sxs-lookup"><span data-stu-id="b4699-131">Generate the report.</span></span> 
10. <span data-ttu-id="b4699-132">Flytja skýrsluna út í Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="b4699-132">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="b4699-133">**Dynamics 365 Finance**</span><span class="sxs-lookup"><span data-stu-id="b4699-133">**Dynamics 365 Finance**</span></span> 
1. <span data-ttu-id="b4699-134">Í Dynamics 365 Finance skal opna **Fjárhagur > Fyrirspurnir og skýrslur > Prófjöfnuður**.</span><span class="sxs-lookup"><span data-stu-id="b4699-134">In Dynamics 365 Finance, go to **General Ledger > Inquiries and Reports > Trial Balance**.</span></span>
2. <span data-ttu-id="b4699-135">Stillið eftirfarandi færibreytur:</span><span class="sxs-lookup"><span data-stu-id="b4699-135">Set the following parameters:</span></span>
   - <span data-ttu-id="b4699-136">**Frá dagsetningu** – Færið inn upphaf fjárhagsárs.</span><span class="sxs-lookup"><span data-stu-id="b4699-136">**From Date** - Enter the start of the fiscal year.</span></span>
   - <span data-ttu-id="b4699-137">**Að dagsetningu** – Færið inn dagsetninguna sem skýrslan er mynduð fyrir.</span><span class="sxs-lookup"><span data-stu-id="b4699-137">**To Date** - Enter the date you are generating the report for.</span></span>
   - <span data-ttu-id="b4699-138">**Fjárhagsvídd** – Stillið þetta svæði á **Aðallykill stilltur**.</span><span class="sxs-lookup"><span data-stu-id="b4699-138">**Financial Dimension** - Set this field to **Main Account set**.</span></span>
 3. <span data-ttu-id="b4699-139">Veljið **Reikna út**.</span><span class="sxs-lookup"><span data-stu-id="b4699-139">Select **Calculate**.</span></span>
 4. <span data-ttu-id="b4699-140">Flytja skýrsluna út í Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="b4699-140">Export the report to Microsoft Excel.</span></span>

<span data-ttu-id="b4699-141">Nú ætti að vera hægt að afrita gögnin úr Excel-skýrslu fjárhagsskýrslugerðar yfir í prófjafnaðarskýrslu til að bera saman dálkana **Lokastaða**.</span><span class="sxs-lookup"><span data-stu-id="b4699-141">You should now be able to copy the data from the Financial Reporter Excel report to the Trial Balance report, so you can compare the **Closing Balance** columns.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]