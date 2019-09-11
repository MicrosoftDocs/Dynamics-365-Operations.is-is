---
title: Kostnaðar- og dagsetningarstýring
description: Þetta efni skýrir kostnaðar- og dagsetningastýringu í eignastýringu.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2bcd1584f6a858f7589387fbfe96267b7c16176a
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918396"
---
# <a name="cost-and-date-control"></a><span data-ttu-id="aa18c-103">Kostnaðar- og dagsetningarstýring</span><span class="sxs-lookup"><span data-stu-id="aa18c-103">Cost and date control</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="aa18c-104">Í eignastýringu er hægt að reikna út kostnað til að fá yfirlit yfir raunkostnað miðað við kostnað fjárhagsáætlunar á eignum, virkum staðsetningum og verkbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="aa18c-104">In Asset Management, you can calculate costs to get an overview of actual costs compared to budget costs on assets, functional locations, and work orders.</span></span> <span data-ttu-id="aa18c-105">Raunkostnaður byggist á bókfærðum færslum.</span><span class="sxs-lookup"><span data-stu-id="aa18c-105">Actual costs are based on posted transactions.</span></span> <span data-ttu-id="aa18c-106">Þú getur líka gert útreikning á dagsetningum ef þú vilt bera saman áætlaðar upphafs- og lokadagsetningar við raunverulegar upphafs- og lokadagsetningar á verkbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="aa18c-106">You can also make a date calculation if you want to compare scheduled start and end dates to actual start and end dates on work orders.</span></span>

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a><span data-ttu-id="aa18c-107">Kostnaðarstýring á eignum, virkum staðssetningum og verkbeiðnum</span><span class="sxs-lookup"><span data-stu-id="aa18c-107">Cost control for assets, functional locations, and work orders</span></span>

<span data-ttu-id="aa18c-108">Útreikningar á eignum, starfrænum stöðum og vinnupöntunum eru nánast eins.</span><span class="sxs-lookup"><span data-stu-id="aa18c-108">The calculations made for assets, functional locations, and work orders are almost identical.</span></span> <span data-ttu-id="aa18c-109">Eini munurinn er sá að fyrir eignir og virkar staðsetningar geturðu einnig haft undireignir og undirstaði með í útreikningum.</span><span class="sxs-lookup"><span data-stu-id="aa18c-109">Only difference is that for assets and functional locations, you can also include sub assets and sub locations in your calculation.</span></span> <span data-ttu-id="aa18c-110">Dagsetningin er færsludagsetningin þegar skráningin var skráð.</span><span class="sxs-lookup"><span data-stu-id="aa18c-110">The date is the transaction date when the registration was recorded.</span></span>

1. <span data-ttu-id="aa18c-111">Smelltu á **Eignastýringu** > **Fyrirspurnir** > **Eignir** > **Stýring eignakostnaðar** eða **Kostnaðarstýring virkra staðsetninga**, eða **Eignastýring** > **Fyrirspurnir** > **Verkbeiðnir** > **Kostnaðarstýring verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="aa18c-111">Click **Asset management** > **Inquiries** > **Assets** > **Asset cost control** or **Functional location cost control**, or **Asset management** > **Inquiries** > **Work orders** > **Work order cost control**.</span></span>

2. <span data-ttu-id="aa18c-112">Í glugganum **Stýring eignakostnaðar** / **Kostnaðarstýring virkra staðsetninga** / **Kostnaðarstýring verkbeiðni** velurðu tímabil sem á að reikna út.</span><span class="sxs-lookup"><span data-stu-id="aa18c-112">In the **Asset cost control** / **Functional location cost control** / **Work order cost control** dialog, select a period to be calculated.</span></span>

3. <span data-ttu-id="aa18c-113">Ef þörf krefur velurðu fjárhagsvídd sem sett er inn í útreikninginn.</span><span class="sxs-lookup"><span data-stu-id="aa18c-113">If required, select a financial dimension set to be included in the calculation.</span></span>

4. <span data-ttu-id="aa18c-114">Veldu „Já“ á skiptihnappnum **Sleppa núlli** ef þú vilt ekki sýna niðurstöður með kostnað við núll.</span><span class="sxs-lookup"><span data-stu-id="aa18c-114">Select "Yes" on the **Skip zero** toggle button if you don't want to show results with a cost of zero.</span></span>

5. <span data-ttu-id="aa18c-115">Þú getur notað reitinn **Stig** til að gefa til kynna hversu ítarlegar þú vilt að kostnaðarstýringarlínur séu varðandi virkar staðsetningar.</span><span class="sxs-lookup"><span data-stu-id="aa18c-115">You can use the **Level** field to indicate how detailed you want the cost control lines to be regarding functional locations.</span></span> <span data-ttu-id="aa18c-116">Til dæmis, ef þú setur inn töluna "1" í reitinn, og þú ert með fjölþrepa skipulag virkrar staðsetningar, verða allar kostnaðarstýringarlínur fyrir virka staðsetningu sýndar á efsta stigi og því er hægt að leggja saman klukkustundirnar á línu frá virkum staðsetningum á lægra stigi.</span><span class="sxs-lookup"><span data-stu-id="aa18c-116">For example, if you insert the number "1" in the field, and you have a multi-level functional location hierarchy, all cost control lines for a functional location will be shown on the top level, and therefore the hours on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="aa18c-117">Ef þú setur töluna „0“ inn í reitinn **Stig** muntu sjá ítarlega niðurstöður sem sýna allar kostnaðarstýringarlínur á öllum virkum staðsetningarstigum sem þær tengjast.</span><span class="sxs-lookup"><span data-stu-id="aa18c-117">If you insert the number "0" in the **Level** field, you will see a detailed result showing all cost control lines on all the functional location level to which they are related.</span></span>

6. <span data-ttu-id="aa18c-118">Veldu „Já“ á skiptihnappnum **Sýna opinn ráðstafaðan kostnað** ef þú vilt láta dálkinn fylgja með í útreikningnum.</span><span class="sxs-lookup"><span data-stu-id="aa18c-118">Select "Yes" on the **Show open committed cost** toggle button if you want to include that column in the calculation.</span></span>

7. <span data-ttu-id="aa18c-119">Veldu „Já“ á skiptihnappnuum **Hafa undireignir með** til að sýna kostnað sem tengist undireignum sem aðskildar línur.</span><span class="sxs-lookup"><span data-stu-id="aa18c-119">Select "Yes" on the **Include sub assets** toggle button to show costs related to sub assets as separate lines.</span></span>

8. <span data-ttu-id="aa18c-120">Ef þú vilt takmarka leitina geturðu valið sérstakar eignir / virkar staðsetningar / verkbeiðnum á flýtiflipanum **Færslur til að taka með**.</span><span class="sxs-lookup"><span data-stu-id="aa18c-120">If you want to limit the search, you can select specific assets / functional locations / work orders on the **Records to include** FastTab.</span></span>

9. <span data-ttu-id="aa18c-121">Smellið á **Í lagi** til að byrja að reikna.</span><span class="sxs-lookup"><span data-stu-id="aa18c-121">Click **OK** to start the calculation.</span></span>

<span data-ttu-id="aa18c-122">Myndin hér að neðan sýnir dæmi um gluggann **Stýring eignakostnaðar**.</span><span class="sxs-lookup"><span data-stu-id="aa18c-122">The figure below shows an example of the **Asset cost control** dialog.</span></span>

![Mynd 1](media/01-controlling-and-reporting.png)

10. <span data-ttu-id="aa18c-124">Í aðgerðarrúðahópunum **Flokka eftir...** á síðunni **Stýring eignakostnaðar** smellirðu á viðeigandi hnappa til að sýna nauðsynleg smáatriði við útreikninginn.</span><span class="sxs-lookup"><span data-stu-id="aa18c-124">In the **Group by...** action pane groups on the **Asset cost control** page, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="aa18c-125">Valdir aðgerðarrúðahnappar eru auðkenndir.</span><span class="sxs-lookup"><span data-stu-id="aa18c-125">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="aa18c-126">Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.</span><span class="sxs-lookup"><span data-stu-id="aa18c-126">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="aa18c-127">Myndin hér að neðan sýnir dæmi um niðurstöður útreiknings í **Stýringu eignakostnaðar**.</span><span class="sxs-lookup"><span data-stu-id="aa18c-127">The figure below shows an example of calculation results in **Asset cost control**.</span></span>

![Mynd 2](media/02-controlling-and-reporting.png)

<span data-ttu-id="aa18c-129">Önnur leið til að gera kostnaðarútreikning er að velja margar eignir í **Allar eignir** eða **Virkar eignir**.</span><span class="sxs-lookup"><span data-stu-id="aa18c-129">Another way of making a cost calculation is to multi-select assets in **All assets** or **Active assets**.</span></span> <span data-ttu-id="aa18c-130">Smelltu síðan á hnappinn **Kostnaðarstýring** á flipnanum **Almennt**. Í glugganum **Stýring eignakostnaðar** eru valdar eignir sjálfkrafa settar inn í reitinn **Eignir** á flýtiflipanum **Færslur til að hafa með**.</span><span class="sxs-lookup"><span data-stu-id="aa18c-130">Then, you click the **Cost control** button on the **General** tab. In the **Asset cost control** dialog, the selected assets are automatically inserted in the **Asset** field on the **Records to include** FastTab.</span></span> <span data-ttu-id="aa18c-131">Smelltu á **Í lagi** og kostnaðarútreikningur fyrir valdar eignir er sýndur.</span><span class="sxs-lookup"><span data-stu-id="aa18c-131">Click **OK**, and a cost calculation for the selected assets is shown.</span></span> <span data-ttu-id="aa18c-132">Sama ferli er hægt að gera fyrir virkar staðsetningar í **Allar virkar staðsetningar** eða **Virkar virkar staðsetningar**, og vegna verkbeiðna í **Allar verkbeiðnir** eða **Virkar vinnupantanir**.</span><span class="sxs-lookup"><span data-stu-id="aa18c-132">The same procedure can be done for functional locations in **All functional locations** or **Active functional locations**, and for work orders in **All work orders** or **Active work orders**.</span></span>

>[!NOTE]
><span data-ttu-id="aa18c-133">Reiturinn **Upprunaleg fjárhagsáætlun** sýnir fjárhagsáætlunarkostnað vegna kostnaðar við spá um verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="aa18c-133">The **Original budget** field shows budget costs from the work order forecast.</span></span> <span data-ttu-id="aa18c-134">Reiturinn **Ráðstafaður kostnaður** sýnir heildarupphæð kostnaðar sem lögaðili hefur skuldbundið sig til að greiða.</span><span class="sxs-lookup"><span data-stu-id="aa18c-134">The **Committed cost** field shows the total amount of expenses that a legal entity has committed itself to pay.</span></span> <span data-ttu-id="aa18c-135">Reiturinn **Opinn ráðstafaður kostnaður** sýnir skuldbindingar um greiðslu fyrir vörur, tíma og þjónustu sem þú hefur pantað eða fengið en hefur ekki enn borgað fyrir.</span><span class="sxs-lookup"><span data-stu-id="aa18c-135">The **Open committed cost** field shows commitments to pay for items, hours, and services you have ordered or received but not yet paid for.</span></span> <span data-ttu-id="aa18c-136">Þegar allar notkunarskráningar hafa verið bókaðar er tengdur kostnaður talinn með í reitnum **Raunkostnaður**.</span><span class="sxs-lookup"><span data-stu-id="aa18c-136">When all consumption registrations have been posted, the related costs are included in the **Actual cost** field.</span></span>

## <a name="work-order-date-control"></a><span data-ttu-id="aa18c-137">Dagsetningastjórnun verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="aa18c-137">Work order date control</span></span>

<span data-ttu-id="aa18c-138">Notaðu þessa síðu til að fá yfirlit yfir væntanlegar upphafs- og lokadagsetningar samanborið við raunverulega upphafs- og lokadagsetningar á verkbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="aa18c-138">Use this page to get an overview of expected start and end dates compared to actual start and end dates on work orders.</span></span>

1. <span data-ttu-id="aa18c-139">Smelltu á **Eignastýring** > **Fyrirspurnir** > **Verkbeiðnir** > **Dagsetningarstýring verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="aa18c-139">Click **Asset management** > **Inquiries** > **Work orders** > **Work order date control**.</span></span>

2. <span data-ttu-id="aa18c-140">Smelltu á **Reikna út**.</span><span class="sxs-lookup"><span data-stu-id="aa18c-140">Click **Calculate**.</span></span>

3. <span data-ttu-id="aa18c-141">Veldu virka staðsetningu í reitnum **Virk staðsetning**.</span><span class="sxs-lookup"><span data-stu-id="aa18c-141">Select a functional location in the **Functional location** field.</span></span>

4. <span data-ttu-id="aa18c-142">Settu tímabilið sem þú vilt gera útreikninginn fyrir í reitunum **Frá dagsetningu** og **Til dagsetningar**.</span><span class="sxs-lookup"><span data-stu-id="aa18c-142">Insert the period for which you want to make the calculation in the **From date** and **To date** fields.</span></span> <span data-ttu-id="aa18c-143">Allar verkbeiðnir með áætlaða byrjun innan tímabilsins verða með.</span><span class="sxs-lookup"><span data-stu-id="aa18c-143">All work orders with expected start within the period will be included.</span></span>

5. <span data-ttu-id="aa18c-144">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="aa18c-144">Click **OK**.</span></span>

6. <span data-ttu-id="aa18c-145">Í aðgerðarrúðahópunum **Flokka eftir...** smellirðu á viðeigandi hnappa til að sýna nauðsynleg smáatriði við útreikninginn.</span><span class="sxs-lookup"><span data-stu-id="aa18c-145">In the **Group by...** action pane groups, click the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="aa18c-146">Valdir aðgerðarrúðahnappar eru auðkenndir.</span><span class="sxs-lookup"><span data-stu-id="aa18c-146">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="aa18c-147">Smelltu á hnappinn til að virkjaðu eða afvirkjaðu hann.</span><span class="sxs-lookup"><span data-stu-id="aa18c-147">Click on a button to activate or deactivate it.</span></span>

<span data-ttu-id="aa18c-148">Myndin hér að neðan sýnir dæmi um niðurstöður útreiknings í **Dagsetningastýringu verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="aa18c-148">The figure below shows an example of calculation results in **Work order date control**.</span></span>

![Mynd 3](media/03-controlling-and-reporting.png)

- <span data-ttu-id="aa18c-150">Reiturinn **Meðalseinkun upphafs** sýnir mismuninn í dögum milli áætlaðs upphafsdags fyrir verkbeiðni miðað við raunverulegan upphafsdag.</span><span class="sxs-lookup"><span data-stu-id="aa18c-150">The **Avg. start delay** field shows the difference in days between scheduled start date for a work order compared to actual start date.</span></span> <span data-ttu-id="aa18c-151">Ef til dæmis raunupphafsdagsetningin var tveimur dögum fyrir áætlaðan upphafsdag birtist „-2“ í þessum reit.</span><span class="sxs-lookup"><span data-stu-id="aa18c-151">If, for example, the actual start date was two days before the scheduled start date, "-2" will be displayed in this field.</span></span>  
- <span data-ttu-id="aa18c-152">Reiturinn **Meðalseinkun loka** sýnir mismuninn í dögum milli áætlaðs lokadags fyrir verkbeiðni miðað við raunverulegan lokadag.</span><span class="sxs-lookup"><span data-stu-id="aa18c-152">The **Avg. end delay** field shows the difference in days between scheduled end date for a work order compared to actual end date.</span></span> <span data-ttu-id="aa18c-153">Ef til dæmis raunlokadagsetningin var þremur dögum eftir áætlaðan lokadag birtist „-3“ í þessum reit.</span><span class="sxs-lookup"><span data-stu-id="aa18c-153">If, for example, the actual end date was three days after the scheduled end date, "3" will be displayed in this field.</span></span>  
- <span data-ttu-id="aa18c-154">Reitirnir **Tilvik** sýna fjölda skipta sem frávik eiga sér stað í tengslum við áætlaða og raunverulega upphafsdagsetningu og áætlaða og raunverulega lokadagsetningu í verkbeiðninni.</span><span class="sxs-lookup"><span data-stu-id="aa18c-154">The **Occurrences** fields show the number of times deviations occur in relation to scheduled and actual start date, and scheduled and actual end date on the work order.</span></span>

