---
title: Kostnaðar- og dagsetningarstýring
description: Þetta efni skýrir kostnaðar- og dagsetningastýringu í eignastýringu.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetBICostControlWorkspace, EntAssetWorkOrderDateControl, EntAssetWorkOrderForecastCostInfoPart, EntAssetMaintenanceCostTrans, EntAssetWorkOrderDateControlCalcDialog, EntAssetCostControl, EntAssetCostObjectCalendar, EntAssetWorkOrderCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c09dee94891fb78c22e8cf9f203cb7f5531bb968
ms.sourcegitcommit: 51cad1ce3ed44ebf7eb9bdf553ee2df4c1f03135
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/10/2021
ms.locfileid: "6016134"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="23c0d-103">Kostnaðar- og dagsetningarstýring</span><span class="sxs-lookup"><span data-stu-id="23c0d-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23c0d-104">Í eignastýringu er hægt að reikna út kostnað til að fá yfirlit yfir raunkostnað miðað við kostnað fjárhagsáætlunar á eignum, virkum staðsetningum og verkbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="23c0d-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="23c0d-105">Raunkostnaður byggist á bókfærðum færslum.</span><span class="sxs-lookup"><span data-stu-id="23c0d-105">Actual costs are based on posted transactions.</span></span>

<span data-ttu-id="23c0d-106">Þú getur líka gert útreikning á dagsetningum ef þú vilt bera saman áætlaðar upphafs- og lokadagsetningar við raunverulegar upphafs- og lokadagsetningar á verkbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="23c0d-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="23c0d-107">Kostnaðarstýring á eignum, virkum staðssetningum og verkbeiðnum</span><span class="sxs-lookup"><span data-stu-id="23c0d-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="23c0d-108">Útreikningar á eignum, starfrænum stöðum og vinnupöntunum eru nánast eins.</span><span class="sxs-lookup"><span data-stu-id="23c0d-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="23c0d-109">Eini munurinn er sá að fyrir eignir og virkar staðsetningar geturðu einnig haft undireignir og undirstaði með í útreikningum.</span><span class="sxs-lookup"><span data-stu-id="23c0d-109">The only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="23c0d-110">Dagsetningin er færsludagsetningin þegar skráningin var skráð.</span><span class="sxs-lookup"><span data-stu-id="23c0d-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="23c0d-111">Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Eignir** > **Stýring eignakostnaðar** eða **Kostnaðarstýring virkra staðsetninga**, eða **Eignastýring** > **Fyrirspurnir** > **Verkbeiðnir** > **Kostnaðarstýring verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="23c0d-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="23c0d-112">Í glugganum **Stýring eignakostnaðar** / **Kostnaðarstýring virkra staðsetninga** / **Kostnaðarstýring verkbeiðni** velurðu tímabil sem á að reikna út.</span><span class="sxs-lookup"><span data-stu-id="23c0d-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a time range to be calculated.</span></span>

3. <span data-ttu-id="23c0d-113">Ef þörf krefur velurðu fjárhagsvídd sem sett er inn í útreikninginn.</span><span class="sxs-lookup"><span data-stu-id="23c0d-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="23c0d-114">Veldu „Já“ á skiptihnappnum **Sleppa núlli** ef þú vilt ekki sýna niðurstöður með kostnað við núll.</span><span class="sxs-lookup"><span data-stu-id="23c0d-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="23c0d-115">Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að kostnaðarstýringarlínur séu varðandi virkar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="23c0d-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="23c0d-116">Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar kostnaðarstýringarlínur fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi.</span><span class="sxs-lookup"><span data-stu-id="23c0d-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span>

    <span data-ttu-id="23c0d-117">Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar kostnaðarstýringarlínur á öllum virkum staðsetningarstigum sem þær tengjast.</span><span class="sxs-lookup"><span data-stu-id="23c0d-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="23c0d-118">Veldu „Já“ á skiptihnappnum **Sýna opinn ráðstafaðan kostnað** ef þú vilt láta dálkinn fylgja með í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="23c0d-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="23c0d-119">Veldu „Já“ á skiptihnappnuum **Hafa undireignir með** til að sýna kostnað sem tengist undireignum sem aðskildar línur.</span><span class="sxs-lookup"><span data-stu-id="23c0d-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="23c0d-120">Ef þú vilt takmarka leitina geturðu valið sérstakar eignir / virkar staðsetningar / verkbeiðnum á flýtiflipanum **Færslur til að taka með**.</span><span class="sxs-lookup"><span data-stu-id="23c0d-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="23c0d-121">Smellið á **Í lagi** til að byrja að reikna.</span><span class="sxs-lookup"><span data-stu-id="23c0d-121">Click **OK** to start the calculation.</span></span>

    <span data-ttu-id="23c0d-122">Myndin hér að neðan sýnir dæmi um gluggann **Stýring eignakostnaðar**.</span><span class="sxs-lookup"><span data-stu-id="23c0d-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

    ![Valmyndin Stýring eignakostnaðar](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="23c0d-124">Á síðunni **Stýring eignakostnaðar** smellirðu á hnappana **Flokka eftir** til að sýna áskilið upplýsingastig útreikningsins.</span><span class="sxs-lookup"><span data-stu-id="23c0d-124">On the **Asset cost control** page, click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="23c0d-125">Valdir hnappar **Flokka eftir** eru auðkenndir.</span><span class="sxs-lookup"><span data-stu-id="23c0d-125">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="23c0d-126">Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.</span><span class="sxs-lookup"><span data-stu-id="23c0d-126">Click on a button to activate or deactivate it.</span></span>

## <a name="example-of-calculation-results-in-asset-cost-control"></a><span data-ttu-id="23c0d-127">Dæmi um niðurstöður útreiknings í kostnaðarstýringu eignar</span><span class="sxs-lookup"><span data-stu-id="23c0d-127">Example of calculation results in asset cost control</span></span>

<span data-ttu-id="23c0d-128">Skjáskotið hér að neðan sýnir dæmi um niðurstöður útreiknings í **Stýringu eignakostnaðar**.</span><span class="sxs-lookup"><span data-stu-id="23c0d-128">The screenshot below shows an example of calculation results in **Asset cost control**.</span></span>

- <span data-ttu-id="23c0d-129">Reiturinn **Upprunaleg fjárhagsáætlun** sýnir fjárhagsáætlunarkostnað vegna kostnaðar við spá um verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="23c0d-129">The **Original budget** field shows budget costs from the work order forecast.</span></span> 
- <span data-ttu-id="23c0d-130">Reiturinn **Ráðstafaður kostnaður** sýnir heildarupphæð kostnaðar sem lögaðili hefur skuldbundið sig til að greiða.</span><span class="sxs-lookup"><span data-stu-id="23c0d-130">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> 
- <span data-ttu-id="23c0d-131">Reiturinn **Opinn ráðstafaður kostnaður** sýnir skuldbindingar um greiðslu fyrir vörur, tíma og þjónustu sem þú hefur pantað eða fengið en hefur ekki enn borgað fyrir.</span><span class="sxs-lookup"><span data-stu-id="23c0d-131">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> 
- <span data-ttu-id="23c0d-132">Reiturinn **Raunkostnaður** sýnir tengdan kostnað eftir að allar notkunarskráningar hafa verið bókaðar.</span><span class="sxs-lookup"><span data-stu-id="23c0d-132">The **Actual cost** field shows related costs after all consumption registrations have been posted.</span></span>

![Dæmi um niðurstöður útreikninga í Stýringu eignakostnaðar](media/02-controlling-and-reporting.png)

<span data-ttu-id="23c0d-134">Önnur leið til að gera kostnaðarútreikning er að velja margar eignir í **Allar eignir** eða **Virkar eignir**.</span><span class="sxs-lookup"><span data-stu-id="23c0d-134">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="23c0d-135">Smelltu síðan á hnappinn **Kostnaðarstýring** á flipnanum **Almennt**. Í glugganum **Stýring eignakostnaðar** eru valdar eignir sjálfkrafa settar inn í reitinn **Eignir** á flýtiflipanum **Færslur til að hafa með**.</span><span class="sxs-lookup"><span data-stu-id="23c0d-135">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="23c0d-136">Smelltu á **Í lagi** og kostnaðarútreikningur fyrir valdar eignir er sýndur.</span><span class="sxs-lookup"><span data-stu-id="23c0d-136">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="23c0d-137">Sama ferli er hægt að gera fyrir virkar staðsetningar í **Allar virkar staðsetningar** eða **Virkar virkar staðsetningar**, og vegna verkbeiðna í **Allar verkbeiðnir** eða **Virkar vinnupantanir**.</span><span class="sxs-lookup"><span data-stu-id="23c0d-137">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>

## <a name="work-order-date-control"></a><span data-ttu-id="23c0d-138">Dagsetningastjórnun verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="23c0d-138">Work order date control</span></span>

<span data-ttu-id="23c0d-139">Notaðu þessa síðu til að fá yfirlit yfir væntanlegar upphafs- og lokadagsetningar samanborið við raunverulega upphafs- og lokadagsetningar á verkbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="23c0d-139">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="23c0d-140">Smelltu á **Eignastýring** > **Fyrirspurnir** > **Verkbeiðnir** > **Dagsetningarstýring verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="23c0d-140">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="23c0d-141">Smelltu á **Reikna út**.</span><span class="sxs-lookup"><span data-stu-id="23c0d-141">Click **Calculate**.</span></span>

3. <span data-ttu-id="23c0d-142">Veldu virka staðsetningu í reitnum **Virk staðsetning**.</span><span class="sxs-lookup"><span data-stu-id="23c0d-142">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="23c0d-143">Settu tímabilið sem þú vilt gera útreikninginn fyrir í reitunum **Frá dagsetningu** og **Til dagsetningar**.</span><span class="sxs-lookup"><span data-stu-id="23c0d-143">Insert the range for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="23c0d-144">Allar verkbeiðnir með áætlaða byrjunardags. innan tímabilsins verða með.</span><span class="sxs-lookup"><span data-stu-id="23c0d-144">All work orders with expected start date within the range will be included.</span></span>

5. <span data-ttu-id="23c0d-145">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="23c0d-145">Click **OK**.</span></span>

6. <span data-ttu-id="23c0d-146">Smelltu á hnappana **Flokka eftir** til að sýna nauðsynleg smáatriði við útreikninginn.</span><span class="sxs-lookup"><span data-stu-id="23c0d-146">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="23c0d-147">Valdir hnappar **Flokka eftir** eru auðkenndir.</span><span class="sxs-lookup"><span data-stu-id="23c0d-147">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="23c0d-148">Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.</span><span class="sxs-lookup"><span data-stu-id="23c0d-148">Click on a button to activate or deactivate it.</span></span>

## <a name="example-of-calculation-results-in-work-order-date-control"></a><span data-ttu-id="23c0d-149">Dæmi um niðurstöður útreiknings í dagsetningarstýringu verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="23c0d-149">Example of calculation results in work order date control</span></span>

<span data-ttu-id="23c0d-150">Skjáskotið hér að neðan sýnir dæmi um niðurstöður útreiknings í **Dagsetningastýringu verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="23c0d-150">The screenshot below shows an example of calculation results in **Work order date control**.</span></span>

- <span data-ttu-id="23c0d-151">Reiturinn **Meðalseinkun upphafs** sýnir mismuninn í dögum milli áætlaðs upphafsdags fyrir verkbeiðni miðað við raunverulegan upphafsdag.</span><span class="sxs-lookup"><span data-stu-id="23c0d-151">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="23c0d-152">Ef til dæmis raunupphafsdagsetningin var tveimur dögum fyrir áætlaðan upphafsdag birtist „-2“ í þessum reit.</span><span class="sxs-lookup"><span data-stu-id="23c0d-152">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="23c0d-153">Reiturinn **Meðalseinkun loka** sýnir mismuninn í dögum milli áætlaðs lokadags fyrir verkbeiðni miðað við raunverulegan lokadag.</span><span class="sxs-lookup"><span data-stu-id="23c0d-153">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="23c0d-154">Ef til dæmis raunlokadagsetningin var þremur dögum eftir áætlaðan lokadag birtist „-3“ í þessum reit.</span><span class="sxs-lookup"><span data-stu-id="23c0d-154">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="23c0d-155">Reitirnir **Tilvik** sýna fjölda skipta sem frávik eiga sér stað í tengslum við áætlaða og raunverulega upphafsdagsetningu og áætlaða og raunverulega lokadagsetningu í verkbeiðninni.</span><span class="sxs-lookup"><span data-stu-id="23c0d-155">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

![Dæmi um niðurstöður útreikninga í Dagsetningastjórnun verkbeiðni](media/03-controlling-and-reporting.png)




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]