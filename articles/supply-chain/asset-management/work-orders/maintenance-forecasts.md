---
title: Viðhaldsspár
description: Þetta efni skýrir viðhaldsspár í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 383c910b40199f2da863144c6dc85a579d0091e9
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024500"
---
# <a name="maintenance-forecasts"></a><span data-ttu-id="3cb51-103">Viðhaldsspár</span><span class="sxs-lookup"><span data-stu-id="3cb51-103">Maintenance forecasts</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="3cb51-104">Þegar þú býrð til verkbeiðni býrðu til verkbeiðnivinnslur með tengdar eignir og tegundir viðhaldsverka.</span><span class="sxs-lookup"><span data-stu-id="3cb51-104">When you create a work order, you create work order jobs with related assets and maintenance job types.</span></span> <span data-ttu-id="3cb51-105">Þegar þú velur tegund viðhaldsverks sem inniheldur viðhaldsspár eru spárnar afritaðar sjálfkrafa í verkbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="3cb51-105">When you select a maintenance job type containing maintenance forecasts, the forecasts are automatically copied to the work order.</span></span>

<span data-ttu-id="3cb51-106">Þú gætir verið fær um að bæta við eða eyða spálínum í verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="3cb51-106">You may be able to add or delete forecast lines on a work order.</span></span> <span data-ttu-id="3cb51-107">Uppsetning á líftímastöðu verkbeiðni, tengdri verkefnisgerð og stigareglum sem tengjast verkgerðinni ákvarðar hvort þú getur bætt við eða breytt spálínum.</span><span class="sxs-lookup"><span data-stu-id="3cb51-107">The setup of a work order lifecycle state, the related project type, and the stage rules related to the project type determines if you are able to add or edit forecast lines.</span></span> 

1. <span data-ttu-id="3cb51-108">Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="3cb51-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="3cb51-109">Veldu verkbeiðnina á listanum og smelltu á **Spá**.</span><span class="sxs-lookup"><span data-stu-id="3cb51-109">Select the work order in the list, and click **Forecast**.</span></span> <span data-ttu-id="3cb51-110">Í **Viðhaldsspá verkbeiðni** birtast spálínur úr gerð viðhaldsverks sem var valin í verkbeiðnivinnslunni.</span><span class="sxs-lookup"><span data-stu-id="3cb51-110">In **Work order maintenance forecast**, forecast lines from the maintenance job type selected on the work order job are displayed.</span></span>


## <a name="add-hours-forecast-to-a-work-order"></a><span data-ttu-id="3cb51-111">Bættu tímaspá við verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="3cb51-111">Add hours forecast to a work order</span></span>

1. <span data-ttu-id="3cb51-112">Veldu vinnslu verkbeiðni sem þú vilt bæta við spá.</span><span class="sxs-lookup"><span data-stu-id="3cb51-112">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="3cb51-113">Á flýtiflipanum **Klukkustundir** skaltu smella á **Bæta við** til að búa til nýja línu.</span><span class="sxs-lookup"><span data-stu-id="3cb51-113">On the **Hours** FastTab, click **Add** to create a new line.</span></span>

3. <span data-ttu-id="3cb51-114">Veljið flokk í reitnum **Flokkur**.</span><span class="sxs-lookup"><span data-stu-id="3cb51-114">Select a category in the **Category** field.</span></span>

4. <span data-ttu-id="3cb51-115">Settu fjölda spáðra tíma inn í reitinn **Klukkutímar**.</span><span class="sxs-lookup"><span data-stu-id="3cb51-115">Insert number of forecasted hours in the **Hours** field.</span></span>

5. <span data-ttu-id="3cb51-116">Í reitnum **Línueign** skaltu velja gjaldtegundina sem á að nota á línunni.</span><span class="sxs-lookup"><span data-stu-id="3cb51-116">In the **Line property** field, select the charge type to be used on the line.</span></span>


## <a name="add-items-forecast-to-a-work-order"></a><span data-ttu-id="3cb51-117">Bættu vöruspá við verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="3cb51-117">Add items forecast to a work order</span></span>

<span data-ttu-id="3cb51-118">Það eru þrjár leiðir til að bæta vörum við viðhaldsspá fyrir verkbeiðni: Þú getur búið til línur fyrir vörur (varahluti) sem eru ekki með í varahlutalistanum eða uppskrift eignar, þú getur valið varahluti af samþykktum varahlutalista og þú getur valið vörur úr uppskrift eignar.</span><span class="sxs-lookup"><span data-stu-id="3cb51-118">There are three ways to add items to a work order maintenance forecast: You can create lines for items (spare parts) that are not included in the spare parts list or asset BOM, you can select spare parts from the approved spare parts list, and you can select items from the asset BOM.</span></span>

1. <span data-ttu-id="3cb51-119">Veldu vinnslu verkbeiðni sem þú vilt bæta við spá.</span><span class="sxs-lookup"><span data-stu-id="3cb51-119">Select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="3cb51-120">Velja skal flýtiflipann **Vörur**.</span><span class="sxs-lookup"><span data-stu-id="3cb51-120">Select the **Items** FastTab.</span></span>

3. <span data-ttu-id="3cb51-121">Smelltu á **Bæta við** til að búa til nýja línu fyrir varahluti sem er ekki á varahlutalistanum eða lista yfir uppskriftir eigna.</span><span class="sxs-lookup"><span data-stu-id="3cb51-121">Click **Add** to create a new line for a spare part that is not on the spare parts list or the asset BOM list.</span></span>

4. <span data-ttu-id="3cb51-122">Veldu vöru í reitnum **Vörunúmer**.</span><span class="sxs-lookup"><span data-stu-id="3cb51-122">Select the item in the **Item number** field.</span></span>

5. <span data-ttu-id="3cb51-123">Settu magn inn í reitinn **Sölumagn** og veldu magneiningu í reitnum **Eining**.</span><span class="sxs-lookup"><span data-stu-id="3cb51-123">Insert quantity in the **Sales quantity** field, and select a quantity unit in the **Unit** field.</span></span>

6. <span data-ttu-id="3cb51-124">Settu inn kostnaðarverð og gjaldmiðil í viðkomandi reiti og veldu **Línueiginleiki**.</span><span class="sxs-lookup"><span data-stu-id="3cb51-124">Insert cost price and currency in the relevant fields, and select a **Line property**.</span></span>

7. <span data-ttu-id="3cb51-125">Ef þú vilt breyta lista yfir víddir sem birtast í vörulínunum smellirðu á **Birgðir** > **Sýna víddir**, velur víddirnar og velur „Já“ á skiptihnappnum **Vista uppsetningu**.</span><span class="sxs-lookup"><span data-stu-id="3cb51-125">If you want to change the list of dimensions displayed on the item lines, click **Inventory** > **Display dimensions**, select the dimensions, and select "Yes" on the **Save setup** toggle button.</span></span>

8. <span data-ttu-id="3cb51-126">Ef þú vilt bæta viðurkenndum varahlutum við viðhaldsspá smellirðu á **Bæta við varahlutum**, velur varahlutinn, breytir tengdum upplýsingum ef þörf krefur og smellir á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3cb51-126">If you want to add an approved spare part to the maintenance forecast, click **Add spare parts**, select the spare part, edit related information if required, and click **OK**.</span></span>

9. <span data-ttu-id="3cb51-127">Ef þú vilt bæta uppskriftahlutum eigna við spána smellirðu á **Bæta uppskriftarhlutum við**, velur hlutinn, breytir upplýsingum ef þörf krefur og smellir á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3cb51-127">If you want to add asset BOM items to the forecast, click **Add BOM items**, select the item, edit related information if required, and click **OK**.</span></span>

10. <span data-ttu-id="3cb51-128">Smelltu á **Notkunarstaður vöru** ef þú vilt fá yfirlit yfir hvar vara í valinni línu er notuð í eignastjórnun í tengslum við eignir, tegundasjálfgildi viðhaldsverka, varahluti og verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="3cb51-128">Click **Item where used** if you want to get an overview of where the item on the selected line is used in Asset Management in relation to assets, maintenance job type defaults, spare parts, and work orders.</span></span> 



## <a name="add-expense-forecast-to-a-work-order"></a><span data-ttu-id="3cb51-129">Bættu kostnaðarspá við verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="3cb51-129">Add expense forecast to a work order</span></span>

1. <span data-ttu-id="3cb51-130">Þetta efni útskýrir hvernig á að bæta kostnaðarspá við kostnaður.</span><span class="sxs-lookup"><span data-stu-id="3cb51-130">This topic explains how to add an expense forecast to a work order.</span></span> <span data-ttu-id="3cb51-131">Veldu vinstra megin í skjámyndinni þá verkbeiðni sem þú vilt bæta spá við.</span><span class="sxs-lookup"><span data-stu-id="3cb51-131">In the left-hand side of the form, select the work order job to which you want to add a forecast.</span></span>

2. <span data-ttu-id="3cb51-132">Velja skal flýtiflipann **Kostnaður**.</span><span class="sxs-lookup"><span data-stu-id="3cb51-132">Select the **Expense** FastTab.</span></span>

3. <span data-ttu-id="3cb51-133">Smellt er á **Bæta við** til að búa til nýja línu.</span><span class="sxs-lookup"><span data-stu-id="3cb51-133">Click **Add** to create a new line.</span></span>

4. <span data-ttu-id="3cb51-134">Veljið flokk í reitnum **Flokkur**.</span><span class="sxs-lookup"><span data-stu-id="3cb51-134">Select a category in the **Category** field.</span></span>

5. <span data-ttu-id="3cb51-135">Settu magn inn í reitinn **Magn**.</span><span class="sxs-lookup"><span data-stu-id="3cb51-135">Insert quantity in the **Quantity** field.</span></span>

6. <span data-ttu-id="3cb51-136">Settu inn kostnaðarverð, sölugjaldmiðil og söluverð í viðkomandi reiti.</span><span class="sxs-lookup"><span data-stu-id="3cb51-136">Insert cost price, sales currency, and sales price in the relevant fields.</span></span>

7. <span data-ttu-id="3cb51-137">Í reitnum **Línueign** skaltu velja gjaldtegundina sem á að nota á línunni.</span><span class="sxs-lookup"><span data-stu-id="3cb51-137">In the **Line property** field, select the charge type to be used on the line.</span></span>

>[!NOTE]
><span data-ttu-id="3cb51-138">Á flýtiflipanum **Viðhaldsspá samtals** geturðu séð yfirlit yfir fjölda lína sem eru búnar til á hverjum flipa, fyrir valið verk í pöntun og fyrir verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="3cb51-138">On the **Maintenance forecast totals** FastTab, you can see an overview of the number of lines created on each tab, for the selected work order job and for the work order.</span></span> <span data-ttu-id="3cb51-139">Einnig er hægt að sjá summu af spáðum vinnutíma fyrir verkbeiðnivinnsluna og fyrir verkbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="3cb51-139">Also, you can see a sum of forecasted work hours for the work order job and for the work order.</span></span>

![Mynd 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a><span data-ttu-id="3cb51-141">Sjálfvirk uppfærsla á spám um verkbeiðnir</span><span class="sxs-lookup"><span data-stu-id="3cb51-141">Automatic update of work order forecasts</span></span>

<span data-ttu-id="3cb51-142">Í eignastjórnun geturðu sjálfkrafa uppfært allar breytingar á spám um verkbeiðnir varðandi kostnað á klukkustund, vörukostnað og útgjöld sem hafa verið uppfærð í öðrum einingum.</span><span class="sxs-lookup"><span data-stu-id="3cb51-142">In Asset Management, you can automatically update any changes in work order forecasts regarding hour costs, item costs, and expenses, which have been updated in other modules.</span></span> <span data-ttu-id="3cb51-143">Þetta er gert til að tryggja að nýjustu kostnaðarverðin séu ávallt notuð í spám þínum um verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="3cb51-143">This is done to ensure that the latest cost prices are always used in your work order forecasts.</span></span> <span data-ttu-id="3cb51-144">Það er líka mögulegt að gera svipaðar uppfærslur fyrir [spár um viðhaldverk](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span><span class="sxs-lookup"><span data-stu-id="3cb51-144">It is also possible to make similar updates for [maintenance job type forecasts](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).</span></span>

1. <span data-ttu-id="3cb51-145">Smelltu á **Eignastjórnun** > **Reglubundið** > **Spá** > **Uppfæra spá um verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="3cb51-145">Click **Asset management** > **Periodic** > **Forecast** > **Update work order forecast**.</span></span>

2. <span data-ttu-id="3cb51-146">Í fellivalmyndinni **Uppfæra spá um verkbeiðni** er hægt að bæta við vali varðandi sérstakar verkbeiðnir eða verkbeiðnivinnslur, ef þess er krafist.</span><span class="sxs-lookup"><span data-stu-id="3cb51-146">In the **Update work order forecast** drop-down dialog, you can add selections regarding specific work orders or work order jobs, if required.</span></span> <span data-ttu-id="3cb51-147">Smelltu á **Sía** til að gera það val.</span><span class="sxs-lookup"><span data-stu-id="3cb51-147">Click **Filter** to make those selections.</span></span>

3. <span data-ttu-id="3cb51-148">Ef með þarf er hægt að setja upp sjálfvirka uppfærslu sem runuvinnslu á flýtiflipanum **Keyra í bakgrunni**.</span><span class="sxs-lookup"><span data-stu-id="3cb51-148">If required, you can set up the automatic update as a batch job on the **Run in the background** FastTab.</span></span>

4. <span data-ttu-id="3cb51-149">Smelltu á **Í lagi** til að hefja uppfærslu á spá.</span><span class="sxs-lookup"><span data-stu-id="3cb51-149">Click **OK** to start the forecast update.</span></span>


![Mynd 2](media/07-work-orders.png)

