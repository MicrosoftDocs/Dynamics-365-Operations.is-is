---
title: Viðhaldsspár
description: Þetta efni skýrir viðhaldsspár í eignastýringu.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderForecastToJournals, EntAssetWorkOrderForecast
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dd652af3100f8de59e06490443baeebca58a4dd3
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838539"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="bb62c-103">Viðhaldsspár</span><span class="sxs-lookup"><span data-stu-id="bb62c-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="bb62c-104">Þegar þú býrð til verkbeiðni býrðu til verkbeiðnivinnslur sem hafa tengdar eignir og tegundir viðhaldsverka.</span><span class="sxs-lookup"><span data-stu-id="bb62c-104">When you create a work order, you create work order jobs that have related assets and maintenance job types.</span></span> <span data-ttu-id="bb62c-105">Þegar þú velur tegund viðhaldsverks sem inniheldur viðhaldsspár eru spárnar afritaðar sjálfkrafa í verkbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="bb62c-105">When you select a maintenance job type that contains maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="bb62c-106">Hugsanlega er hægt að bæta spálínum við verkbeiðni eða eyða þeim úr verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="bb62c-106">You might be able to add forecast lines to a work order or delete them from a work order.</span></span> <span data-ttu-id="bb62c-107">Uppsetning á líftímastöðu verkbeiðni, tengdri verkefnisgerð og stigareglum sem tengjast verkgerðinni ákvarðar hvort þú getur bætt við eða breytt spárlínum.</span><span class="sxs-lookup"><span data-stu-id="bb62c-107">The setup of the work order lifecycle state, the related project type, and the stage rules that are related to the project type determine whether you can add or edit forecast lines.</span></span> <span data-ttu-id="bb62c-108">Nánari upplýsingar um líftímastöður verkbeiðna og tengd verkefnastig, sjá [Spár, verkbeiðnir og verk](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span><span class="sxs-lookup"><span data-stu-id="bb62c-108">For more information about work order lifecycle states and related project stages, see [Forecasts, work orders, and projects](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).</span></span>

1. <span data-ttu-id="bb62c-109">Veldu **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="bb62c-109">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="bb62c-110">Veldu verkbeiðni á listanum og síðan á aðgerðarrúðunni > flipanmu **Verkbeiðni** > hópnum **Verk**, velurðu **Spá**.</span><span class="sxs-lookup"><span data-stu-id="bb62c-110">Select the work order in the list, and then, on the Action Pane > **Work order** tab > the **Project** group, select **Forecast**.</span></span> <span data-ttu-id="bb62c-111">Síðan **Viðhaldsspá verkbeiðni** sýnir spálínur úr gerð viðhaldsverks sem er valið í verkbeiðnivinnslunni.</span><span class="sxs-lookup"><span data-stu-id="bb62c-111">The **Work order maintenance forecast** page shows forecast lines from the maintenance job type that is selected on the work order job.</span></span>


## <a name="add-an-hours-forecast-to-a-work-order"></a><span data-ttu-id="bb62c-112">Bættu tímaspá við verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="bb62c-112">Add an hours forecast to a work order</span></span>

1. <span data-ttu-id="bb62c-113">Á síðunni **Viðhaldsspá verkbeiðni** velurðu vinnslu verkbeiðni til að bæta spá við.</span><span class="sxs-lookup"><span data-stu-id="bb62c-113">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="bb62c-114">Á flýtiflipanum **Klukkustundir** skaltu velja **Bæta við** til að búa til nýja línu.</span><span class="sxs-lookup"><span data-stu-id="bb62c-114">On the **Hours** FastTab, select **Add** to create a new line.</span></span>

3. <span data-ttu-id="bb62c-115">Í reitnum **Flokkur** velurðu flokk.</span><span class="sxs-lookup"><span data-stu-id="bb62c-115">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="bb62c-116">Settu fjölda spáðra tíma inn í reitinn **Klukkutímar**.</span><span class="sxs-lookup"><span data-stu-id="bb62c-116">In the **Hours** field, enter the number of forecasted hours.</span></span>

5. <span data-ttu-id="bb62c-117">Í reitnum **Línueign** skaltu velja tegund gjalds sem á að nota á línunni.</span><span class="sxs-lookup"><span data-stu-id="bb62c-117">In the **Line property** field, select the type of charge that should be used on the line.</span></span>


## <a name="add-an-items-forecast-to-a-work-order"></a><span data-ttu-id="bb62c-118">Bættu vöruspá við verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="bb62c-118">Add an items forecast to a work order</span></span>

<span data-ttu-id="bb62c-119">Það eru þrjár leiðir til að bæta hlutum við viðhaldsspá fyrir verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="bb62c-119">There are three ways to add items to a work order maintenance forecast.</span></span> <span data-ttu-id="bb62c-120">Þú getur búið til línur fyrir vörur (varahluti) sem eru ekki með í varahlutalistanum eða uppskrift eignar (BOM), þú getur valið varahluti af samþykktum varahlutalista og þú getur valið vörur úr uppskrift eignar.</span><span class="sxs-lookup"><span data-stu-id="bb62c-120">You can create lines for items (spare parts) that aren't included on the spare parts list or the asset bill of materials (BOM), you can select spare parts from the approved spare parts list, or you can select items from the asset BOM.</span></span>

- <span data-ttu-id="bb62c-121">Á síðunni **Viðhaldsspá verkbeiðni** velurðu vinnslu verkbeiðni til að bæta spá við.</span><span class="sxs-lookup"><span data-stu-id="bb62c-121">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

- <span data-ttu-id="bb62c-122">Á flýtiflipanum **Atriði** bætirðu atriðum við viðhaldsspá með því að nota viðeigandi aðferð.</span><span class="sxs-lookup"><span data-stu-id="bb62c-122">On the **Items** FastTab, add items to the maintenance forecast by using the appropriate method.</span></span>

<span data-ttu-id="bb62c-123">Til að stofna línu fyrir varahlut sem er ekki á varahlutalistanum eða lista yfir uppskriftir eigna fylgirðu þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="bb62c-123">To create a line for a spare part that isn't on the spare parts list or the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="bb62c-124">Veljið **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="bb62c-124">Select **Add**.</span></span>
2. <span data-ttu-id="bb62c-125">Veldu vöru í reitnum **Vörunúmer**.</span><span class="sxs-lookup"><span data-stu-id="bb62c-125">In the **Item number** field, select the item.</span></span>
3. <span data-ttu-id="bb62c-126">Inn í reitinn **Sölumagn** skal slá inn magnið.</span><span class="sxs-lookup"><span data-stu-id="bb62c-126">In the **Sales quantity** field, enter the quantity.</span></span>
4. <span data-ttu-id="bb62c-127">Í reitnum **Einingu** velurðu mælieiningu fyrir magnið.</span><span class="sxs-lookup"><span data-stu-id="bb62c-127">In the **Unit** field, select the unit of measure for the quantity.</span></span>
5. <span data-ttu-id="bb62c-128">Í reitunum **Kostnaðarverð** og **Gjaldmiðill** slærðu inn viðeigandi gildi.</span><span class="sxs-lookup"><span data-stu-id="bb62c-128">In the **Cost price** and **Currency** fields, enter appropriate values.</span></span>
6. <span data-ttu-id="bb62c-129">Í reitnum **Línueign** velurðu línueign.</span><span class="sxs-lookup"><span data-stu-id="bb62c-129">In the **Line property** field, select a line property.</span></span>
7. <span data-ttu-id="bb62c-130">Til að breyta lista yfir víddir sem eur sýndar í vörulínunum velurðu **Birgðir** > **Sýna víddir**, velur víddirnar og stillir síðan valkostinn **Vista uppsetningu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="bb62c-130">To change the list of dimensions that is shown on the item lines, select **Inventory** > **Display dimensions**, select the dimensions, and then set the **Save setup** option to **Yes**.</span></span>

<span data-ttu-id="bb62c-131">Fylgdu þessum skrefum til að bæta við varahlutum úr viðurkenndum varahlutalista:</span><span class="sxs-lookup"><span data-stu-id="bb62c-131">To add a spare part from an approved spare parts list, follow these steps:</span></span>

1. <span data-ttu-id="bb62c-132">Veldu **Bæta við varahlutum**.</span><span class="sxs-lookup"><span data-stu-id="bb62c-132">Select **Add spare parts**.</span></span>
2. <span data-ttu-id="bb62c-133">Veldu varahlutinn og breyttu tengdum upplýsingum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="bb62c-133">Select the spare part, and edit the related information as you require.</span></span>
3. <span data-ttu-id="bb62c-134">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="bb62c-134">Select **OK**.</span></span>

<span data-ttu-id="bb62c-135">Fylgdu þessum skrefum til að bæta við vöru úr uppskrift eignar:</span><span class="sxs-lookup"><span data-stu-id="bb62c-135">To add an item from the asset BOM, follow these steps:</span></span>

1. <span data-ttu-id="bb62c-136">Veldu **Bæta uppskriftarhlutum við**.</span><span class="sxs-lookup"><span data-stu-id="bb62c-136">Select **Add BOM items**.</span></span>
2. <span data-ttu-id="bb62c-137">Veldu vöru og breyttu tengdum upplýsingum eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="bb62c-137">Select the item, and edit the related information as you require.</span></span>
3. <span data-ttu-id="bb62c-138">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="bb62c-138">Select **OK**.</span></span>

<span data-ttu-id="bb62c-139">Til að fá yfirlit sem sýnir hvar hluturinn á völdum línum er notaður í tengslum við eignir, vanskil tegunda viðhaldsverka, varahluti og verkbeiðnir í eignastýringu velurðu **Notkunarstaður vöru**.</span><span class="sxs-lookup"><span data-stu-id="bb62c-139">To get an overview that shows where the item on the selected line is used in relation to assets, maintenance job type defaults, spare parts, and work orders in Asset Management, select **Item where used**.</span></span> <span data-ttu-id="bb62c-140">Fyrir frekari upplýsingar um þetta yfirlit, sjá [Notkunarstaður vöru](../controlling-and-reporting/item-where-used.md).</span><span class="sxs-lookup"><span data-stu-id="bb62c-140">For more information about this overview, see [Item where used](../controlling-and-reporting/item-where-used.md).</span></span>


## <a name="add-an-expense-forecast-to-a-work-order"></a><span data-ttu-id="bb62c-141">Bættu kostnaðarspá við verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="bb62c-141">Add an expense forecast to a work order</span></span>

1. <span data-ttu-id="bb62c-142">Á síðunni **Viðhaldsspá verkbeiðni** velurðu vinnslu verkbeiðni til að bæta spá við.</span><span class="sxs-lookup"><span data-stu-id="bb62c-142">On the **Work order maintenance forecast** page, select the work order job to add a forecast to.</span></span>

2. <span data-ttu-id="bb62c-143">Á flýtiflipanum **Kostnaður** skaltu velja **Bæta við** til að búa til línu.</span><span class="sxs-lookup"><span data-stu-id="bb62c-143">On the **Expense** FastTab, select **Add** to create a line.</span></span>

3. <span data-ttu-id="bb62c-144">Í reitnum **Flokkur** velurðu flokk.</span><span class="sxs-lookup"><span data-stu-id="bb62c-144">In the **Category** field, select a category.</span></span>

4. <span data-ttu-id="bb62c-145">Inn í reitinn **Magn** skal slá inn magnið.</span><span class="sxs-lookup"><span data-stu-id="bb62c-145">In the **Quantity** field, enter the quantity.</span></span>

5. <span data-ttu-id="bb62c-146">Í reitina **Kostnaðarverð**, **Sölugjaldmiðill** og **Söluverð** skaltu rita viðeigandi gildi.</span><span class="sxs-lookup"><span data-stu-id="bb62c-146">In the **Cost price**, **Sales currency**, and **Sales price** fields, enter appropriate values.</span></span>

6. <span data-ttu-id="bb62c-147">Í reitnum **Línueign** skaltu velja tegund gjalds sem á að nota á línunni.</span><span class="sxs-lookup"><span data-stu-id="bb62c-147">In the **Line property** field, select the type of charge that should be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="bb62c-148">Flýtiflipinn **Viðhaldsspá samtals** sýnir yfirlit yfir fjölda lína sem hafa verið stofnaðar fyrir valið verk í pöntun og fyrir verkbeiðni á hverjum flýtiflipa.</span><span class="sxs-lookup"><span data-stu-id="bb62c-148">The **Maintenance forecast totals** FastTab shows an overview of the number of lines that have been created, for the selected work order job and for the work order, on each FastTab.</span></span> <span data-ttu-id="bb62c-149">Hann sýnir einnig samtölu af spáðum vinnutíma fyrir verkbeiðnivinnsluna og verkbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="bb62c-149">It also shows the total forecasted work hours for the work order job and the work order.</span></span>

<span data-ttu-id="bb62c-150">Skýringarmyndin hér að neðan sýnir dæmi um síðuna **Viðhaldsspá verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="bb62c-150">The illustration below shows an example of the **Work order maintenance forecast** page.</span></span>

![Mynd 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="bb62c-152">Sjálfvirk uppfærsla á spám um verkbeiðnir</span><span class="sxs-lookup"><span data-stu-id="bb62c-152">Automatic update of work order forecasts</span></span>

<span data-ttu-id="bb62c-153">Ef kostnaður á klukkustund, vörukostnaður og útgjöld eru uppfærð í öðrum kerfiseiningum í Microsoft Dynamics 365 for Finance and Operations, er hægt að uppfæra verkbeiðnispár í eignastýringu sjálfkrafa til að endurspegla þessar breytingar.</span><span class="sxs-lookup"><span data-stu-id="bb62c-153">If hour costs, item costs, and expenses are updated in other modules in Microsoft Dynamics 365 for Finance and Operations, work order forecasts in Asset Management can automatically be updated to reflect those changes.</span></span> <span data-ttu-id="bb62c-154">Þessi afkastageta tryggir að nýjustu kostnaðarverðin séu ávallt notuð í spám þínum um verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="bb62c-154">This capability helps guarantee that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="bb62c-155">Einnig er hægt að gera svipaðar uppfærslur fyrir [spár um viðhaldverk](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="bb62c-155">You can also do similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="bb62c-156">Veldu **Eignastjórnun** > **Reglubundið** > **Spá** > **Uppfæra spá um verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="bb62c-156">Select **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="bb62c-157">Í glugganum **Uppfæra spá um verkbeiðni** á flýtiflipanum **Færslur til að taka með** er hægt að bæta við vali varðandi sérstakar verkbeiðnir eða verkbeiðnivinnslur, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="bb62c-157">In the **Update work order forecast** dialog, on the **Records to include** FastTab, you can add selections regarding specific work orders or work order jobs, as you require.</span></span> <span data-ttu-id="bb62c-158">Smelltu á **Sía** til að gera viðeigandi val.</span><span class="sxs-lookup"><span data-stu-id="bb62c-158">Click **Filter** to make the relevant selections.</span></span>

3. <span data-ttu-id="bb62c-159">Á flýtiflipanum **Keyra í bakgrunni** geturðu sett upp sjálfvirka uppfærslu sem runuvinnslu, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="bb62c-159">On the **Run in the background** FastTab, you can set up the automatic update as a batch job, as you require.</span></span>

4. <span data-ttu-id="bb62c-160">Veldu **Í lagi** til að hefja uppfærslu á spá.</span><span class="sxs-lookup"><span data-stu-id="bb62c-160">Select **OK** to start the forecast update.</span></span>


<span data-ttu-id="bb62c-161">Skýringarmyndin hér að neðan sýnir dæmi um gluggann **Uppfæra verkbeiðnispá**.</span><span class="sxs-lookup"><span data-stu-id="bb62c-161">The illustration below shows an example of the **Update work order forecast** dialog.</span></span>

![Mynd 2](media/07-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]