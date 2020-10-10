---
title: Staðfesta sölupantanir
description: Þetta ferli sýnir hvernig á að staðfesta sölupantanir.
author: omulvad
manager: tfehr
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, CustConfirmJournal, SysQueryForm, SysQueryFieldLookUp, SysLookup, SalesParmIdLookup, SalesUnconfirmedOrdersPart
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7dcb60b524d375cbb533e88ea456eaa2c7ca6316
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830429"
---
# <a name="confirm-sales-orders"></a><span data-ttu-id="c26f9-103">Staðfesta sölupantanir</span><span class="sxs-lookup"><span data-stu-id="c26f9-103">Confirm sales orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c26f9-104">Þetta ferli sýnir hvernig á að staðfesta sölupantanir.</span><span class="sxs-lookup"><span data-stu-id="c26f9-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="c26f9-105">Þér verður sýnt hvernig á að staðfesta eina pöntun og hvernig staðfesta á margar pantanir í einu.</span><span class="sxs-lookup"><span data-stu-id="c26f9-105">You'll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="c26f9-106">Þessi verkefni eru yfirleitt framkvæmd af sölupantanavinnslu.</span><span class="sxs-lookup"><span data-stu-id="c26f9-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="c26f9-107">Þú getur farið í gegnum þetta ferli í sýnigögn fyrirtækisins USMF eða með því að nota eigin gögn.</span><span class="sxs-lookup"><span data-stu-id="c26f9-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="c26f9-108">Áður en byrjað er, gangið úr skugga um að það eru nokkrar opnar sölupantanir fyrir sama viðskiptavininn.</span><span class="sxs-lookup"><span data-stu-id="c26f9-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="c26f9-109">Ef verið er að nota USMF er hægt að velja lykil US-027.</span><span class="sxs-lookup"><span data-stu-id="c26f9-109">If you're using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="c26f9-110">Staðfesta eina sölupöntun.</span><span class="sxs-lookup"><span data-stu-id="c26f9-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="c26f9-111">Farðu í **Skoðunarrúðu > Kerfiseiningar > Sala og markaðssetning > Sölupantanir > Allar sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-111">Go to **Navigation pane > Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="c26f9-112">Finna og velja pöntunina sem á að staðfesta á listanum.</span><span class="sxs-lookup"><span data-stu-id="c26f9-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="c26f9-113">Smelltu á tengil á sölupöntun til að opna valda pöntun.</span><span class="sxs-lookup"><span data-stu-id="c26f9-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="c26f9-114">Í **Aðgerðasvæðinu** smellirðu á **Selja**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-114">On the **Action Pane**, click **Sell**.</span></span>
5. <span data-ttu-id="c26f9-115">Smellt er á **Staðfesta sölupantanir**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-115">Click **Confirm sales order**.</span></span>
6. <span data-ttu-id="c26f9-116">Útvíkkaðu hlutann **Færibreytur**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-116">Expand the **Parameters** section.</span></span> <span data-ttu-id="c26f9-117">Passaðu að valkosturinn **Bókun** sé stilltur á Já.</span><span class="sxs-lookup"><span data-stu-id="c26f9-117">Make sure that the **Posting** option is set to 'Yes'.</span></span>  
7. <span data-ttu-id="c26f9-118">Stilltu valkostinn **Prenta staðfestingu** á Já.</span><span class="sxs-lookup"><span data-stu-id="c26f9-118">Set the **Print confirmation option** to 'Yes'.</span></span> <span data-ttu-id="c26f9-119">Reiturinn **Athuga lánamark** tilgreinir aðferðina sem er notuð til að reikna út eftirstandandi lánsheimild viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="c26f9-119">The **Check credit limit** field specifies the method that's used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="c26f9-120">Sjálfgefið er að hún sé afrituð af síðunni Færibreytur viðskiptakrafna.</span><span class="sxs-lookup"><span data-stu-id="c26f9-120">By default, it's copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="c26f9-121">Ef sleppa á athugun á lánamörkum þegar tiltekinni sölupöntun er staðfest skal stilla **Athuga lánamark** á Engin.</span><span class="sxs-lookup"><span data-stu-id="c26f9-121">If you want to skip the credit limit check when confirming a specific sales order, set the **Check credit limit** to 'None'.</span></span> <span data-ttu-id="c26f9-122">Hins vegar ætti að hafa í huga að jafnvel með ef þetta svæði er stillt á Ekkert, verða athugun á lánamörkum samt framkvæmd ef valkosturinn **Áskilið lánamark** er valinn á aðalgögnum viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="c26f9-122">However, you should be aware that even with if this field is set to 'None', the credit limit check will still be performed if the **Mandatory credit limit** option is selected on the customer master data.</span></span> 
8. <span data-ttu-id="c26f9-123">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-123">Click **OK**.</span></span>
9. <span data-ttu-id="c26f9-124">Smellið á **Já**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-124">Click **Yes**.</span></span>
10. <span data-ttu-id="c26f9-125">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c26f9-125">Close the page.</span></span>
11. <span data-ttu-id="c26f9-126">Á **aðgerðasvæðinu** er smellt á **Valkosti**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-126">On the **Action Pane**, click **Options**.</span></span>
12. <span data-ttu-id="c26f9-127">Smelltu á **Skoða breytingu**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-127">Click **Change view**.</span></span>
13. <span data-ttu-id="c26f9-128">Smelltu á **Skoða haus**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-128">Click **Header view**.</span></span> <span data-ttu-id="c26f9-129">Þegar pöntun er staðfest, er **Staða skjals** stillt á Staðfestingu.</span><span class="sxs-lookup"><span data-stu-id="c26f9-129">When an order is confirmed, the **Document status** is set to 'Confirmation'.</span></span> 
14. <span data-ttu-id="c26f9-130">Í **Aðgerðasvæðinu** smellirðu á **Selja**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-130">On the **Action Pane**, click **Sell**.</span></span>
15. <span data-ttu-id="c26f9-131">Smellt er á **Staðfesting sölupöntunar**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-131">Click **Sales order confirmation**.</span></span>
16. <span data-ttu-id="c26f9-132">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="c26f9-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="c26f9-133">Staðfesta margar sölupantanir í einu</span><span class="sxs-lookup"><span data-stu-id="c26f9-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="c26f9-134">Farðu í **Sölu og markaðssetningu > Sölupantanir > Staðfesting á pöntun > Staðfesta sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-134">Go to **Sales and marketing > Sales orders > Order confirmation > Confirm sales order**.</span></span>
2. <span data-ttu-id="c26f9-135">Smellið á **Velja**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-135">Click **Select**.</span></span>
3. <span data-ttu-id="c26f9-136">í listanum á flipanum **Afmörkun** skaltu finna og velja færsluna sem vísar í reitinn **Viðskiptavinalykill**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-136">In the list on the **Range** tab, find and select the record that references the **Customer account** field.</span></span>
4. <span data-ttu-id="c26f9-137">Í reitnum **Skilyrði** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c26f9-137">In the **Criteria** field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c26f9-138">Finna og veljið lykil viðskiptavinar sem er með margar pantanir sem óskað er að staðfesta margar í einu, af listanum.</span><span class="sxs-lookup"><span data-stu-id="c26f9-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span> <span data-ttu-id="c26f9-139">Ef verið er að nota USMF er hægt að velja lykil US-027.</span><span class="sxs-lookup"><span data-stu-id="c26f9-139">If you're using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="c26f9-140">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-140">Click **OK**.</span></span>
    - <span data-ttu-id="c26f9-141">Flipinn **Yfirlit** sýnir lista yfir pantanir sem uppfylla skilyrði fyrirspurnar.</span><span class="sxs-lookup"><span data-stu-id="c26f9-141">The **Overview** tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="c26f9-142">Þær verða teknar með í staðfestingu.</span><span class="sxs-lookup"><span data-stu-id="c26f9-142">These will be included in the confirmation.</span></span>  
    - <span data-ttu-id="c26f9-143">Reiturinn **Safnuppfærsla fyrir** í hlutanum **Færibreytur** tilgreinir færibreytu sem farið er eftir þegar margar pantanir eru teknar saman í eina staðfestingarskjal.</span><span class="sxs-lookup"><span data-stu-id="c26f9-143">The **Summary update for** field in the **Parameters** section specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="c26f9-144">Að sjálfgefnu er valkosturinn afritaður úr **Sjálfgildum fyrir stillingu safnuppfærslu** á síðunni **Færibreytur viðskiptakrafna**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-144">By default, the option is copied from the D**efault values for summary update setting** on the **Accounts receivable parameters** page.</span></span>  
7. <span data-ttu-id="c26f9-145">Í reitnum **Safnuppfærsla fyrir** skaltu velja 'Pöntun'.</span><span class="sxs-lookup"><span data-stu-id="c26f9-145">In the **Summary update for** field, select 'Order'.</span></span> <span data-ttu-id="c26f9-146">Þær lágmarksfæribreytur sem er krafist til að stofna samantekt eru **Reikningslykill** og **Gjaldmiðill**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-146">The minimum parameters that are required to create summary updates are **Invoice account** and **Currency**.</span></span> <span data-ttu-id="c26f9-147">Þetta þýðir að safnuppfærslur með mismunandi reikningslykla og mismunandi gjaldmiðla eru ekki leyfðar.</span><span class="sxs-lookup"><span data-stu-id="c26f9-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="c26f9-148">Hægt er að setja upp viðbótarfæribreytur á síðunni **Færibreytur safnuppfærslu** sem er aðgengileg af síðunni **Færibreytur viðskiptakrafna**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-148">Additional parameters can be set up in the **Summary update parameters** page which is accessible from the **Accounts receivable parameters** page.</span></span> 
8. <span data-ttu-id="c26f9-149">Í reitnum **Sölupöntun** skal smella á fellilistahnappinn til að opna leitina.</span><span class="sxs-lookup"><span data-stu-id="c26f9-149">In the **Sales order** field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="c26f9-150">Á listanum, veljið pöntunarnúmer sem á að verða safnpöntunin.</span><span class="sxs-lookup"><span data-stu-id="c26f9-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="c26f9-151">Smellið á **Raða**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-151">Click **Arrange**.</span></span>
11. <span data-ttu-id="c26f9-152">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-152">Click **OK**.</span></span>
12. <span data-ttu-id="c26f9-153">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="c26f9-153">Click **OK**.</span></span>

