---
title: Handvirkt stofnaðar verkbeiðnir
description: Þetta efni útskýrir hvernig á að stofna verkbeiðnir handvirkt í eignastýringu.
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
ms.openlocfilehash: 261448a134a7c1aacfbb4ea6f954ce03a63c23e2
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875713"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="e9446-103">Handvirkt stofnaðar verkbeiðnir</span><span class="sxs-lookup"><span data-stu-id="e9446-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="e9446-104">Hægt er að stofna verkbeiðnir handvirkt á tvo vegu:</span><span class="sxs-lookup"><span data-stu-id="e9446-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="e9446-105">í **Öllum verkbeiðnum** eða **Virkum verkbeiðnum**</span><span class="sxs-lookup"><span data-stu-id="e9446-105">in **All work orders** or **Active work orders**</span></span>  
- <span data-ttu-id="e9446-106">í **Öllum viðhaldsbeiðnum** eða **Virkum viðhaldsbeiðnum** eða **Mínum viðhaldsbeiðnum á virkri staðsetningu**.</span><span class="sxs-lookup"><span data-stu-id="e9446-106">in **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests**</span></span>  

## <a name="create-work-order"></a><span data-ttu-id="e9446-107">Stofna verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="e9446-107">Create work order</span></span>

1. <span data-ttu-id="e9446-108">Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="e9446-108">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e9446-109">Smellið á hnappinn **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="e9446-109">Click the **New** button.</span></span>

3. <span data-ttu-id="e9446-110">Í fellivalmyndinni **Stofna verkbeiðni** velurðu gerð verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="e9446-110">In the **Create work order** drop-down, select a work order type.</span></span>

4. <span data-ttu-id="e9446-111">Ef þess er krafist skal velja lýsingu.</span><span class="sxs-lookup"><span data-stu-id="e9446-111">If required, select a description.</span></span>

5. <span data-ttu-id="e9446-112">Veldu eignina fyrir verkbeiðnina sem og gerð viðhaldsstarfa.</span><span class="sxs-lookup"><span data-stu-id="e9446-112">Select the asset for the work order as well as a maintenance job type.</span></span>

>[!NOTE]
><span data-ttu-id="e9446-113">Þegar þú velur eign kunna þrír flipar að vera tiltækir: Flipinn **Mínar eignir** inniheldur eignir sem tengjast virkum staðsetningum sem þú (viðhaldsstarfsmaðurinn sem er skráður inn í kerfið) getur fengið úthlutað (sett upp í [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md)).</span><span class="sxs-lookup"><span data-stu-id="e9446-113">When you select an asset, three tabs may be available: The **My assets** tab contains assets related to the functional locations to which you (the worker who is logged on the system) may be allocated (set up in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md)).</span></span> <span data-ttu-id="e9446-114">Ef engar virkar staðsetningar eru settar upp á viðhaldsstarfsmanni í [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md) verður flipinn **Mínar eignir** ekki sýnilegur.</span><span class="sxs-lookup"><span data-stu-id="e9446-114">If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab will not be visible.</span></span> <span data-ttu-id="e9446-115">Flipinn **Virkar eignir** hefur að geyma lista yfir allar eignir með eignalíftímastöðuna „Virkt“.</span><span class="sxs-lookup"><span data-stu-id="e9446-115">The **Active assets** tab contains a list of all assets with asset lifecycle state "Active".</span></span> <span data-ttu-id="e9446-116">Flipinn **Eignayfirlit** sýnir trjáyfirlit yfir virkar staðseningar og eignir sem eru settar upp á þessum stöðum.</span><span class="sxs-lookup"><span data-stu-id="e9446-116">The **Asset view** tab displays a tree view of functional locations and assets installed on those locations.</span></span>

6. <span data-ttu-id="e9446-117">Ef þörf krefur skaltu velja **Afbrigði af gerð viðhaldsstarfa** og **Viðskipti**.</span><span class="sxs-lookup"><span data-stu-id="e9446-117">If required, select **Maintenance job type variant** and **Trade**.</span></span>

7. <span data-ttu-id="e9446-118">Ef þess er krafist geturðu breytt þjónustustigi verkbeiðni í reitnum **Þjónustustig**.</span><span class="sxs-lookup"><span data-stu-id="e9446-118">If required, you can change the work order service level in the **Service level** field.</span></span>

8. <span data-ttu-id="e9446-119">Veldu áætlaðar upphafs- og lokadagsetningar í tengdum reitum.</span><span class="sxs-lookup"><span data-stu-id="e9446-119">Select expected start and end dates in the related fields.</span></span>

9. <span data-ttu-id="e9446-120">Smelltu á **Í lagi** til að stofna nýja verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="e9446-120">Click **OK** to create a new work order.</span></span>

10. <span data-ttu-id="e9446-121">Breytu verkbeiðninni í **Allar verkbeiðnir**, ef nauðsyn krefur.</span><span class="sxs-lookup"><span data-stu-id="e9446-121">Edit the work order in **All work orders**, if required.</span></span>

- <span data-ttu-id="e9446-122">Í **Öllum verkbeiðnum** er hægt að bæta nokkrum eignum við verkbeiðni í smáatriðum með því að bæta við línum á flýtiflipanum **Viðhaldsverk verkbeiðna**.</span><span class="sxs-lookup"><span data-stu-id="e9446-122">In **All work orders**, You can add several assets to a work order in Details view by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="e9446-123">Á eign er aðeins hægt að velja gerðir viðhaldsverka sem eru skilgreindar á eignategundinni sem var valin fyrir eignina.</span><span class="sxs-lookup"><span data-stu-id="e9446-123">On an asset, you can only select the maintenance job types that are defined on the asset type selected for the asset.</span></span>  
- <span data-ttu-id="e9446-124">Ef þú hefur breytt þjónustustigi eigna eða mikilvægi eigna eftir að þú hefur notað þær í verkbeiðni (sjá [Þjónustustig](../setup-for-objects/object-priorities.md) og [Mikilvægi eigna](../setup-for-objects/object-criticalities.md)) er þjónustustig eða gagnrýni á vinnuskipunina ekki uppfærð til samræmis.</span><span class="sxs-lookup"><span data-stu-id="e9446-124">If you have changed an asset service level or an asset criticality after you have used them on a work order (refer to [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticalities](../setup-for-objects/object-criticalities.md)), the service level or criticality on the work order is not updated accordingly.</span></span>
- <span data-ttu-id="e9446-125">Mikilvægi á verkbeiðni er endurútreiknuð í hvert skipti sem verkbeiðnilínu er bætt við eða henni eytt á verkbeiðninni.</span><span class="sxs-lookup"><span data-stu-id="e9446-125">Criticality on a work order is re-calculated each time a work order line is added or deleted on the work order.</span></span>
- <span data-ttu-id="e9446-126">Í upplýsingaglugganum **Allar verkbeiðnir** > glugganum **Haus** > flýtiflipanum **Tímasetja** geturðu valið ábyrgan starfsmannahóp eða ábyrgan viðhaldsstarfsmann í reitunum **Ábyrgur hópur** eða **Ábyrgðarmaður**.</span><span class="sxs-lookup"><span data-stu-id="e9446-126">In **All work orders** Details view > **Header** view > **Schedule** FastTab, you can select a responsible maintenance worker group or a responsible maintenance worker in the **Responsible group** or **Responsible** fields.</span></span> <span data-ttu-id="e9446-127">Þessum stillingum er hægt að breyta eins lengi sem verkbeiðnin er virk, t.d. þegar líftímastaða verkbeiðninnar breytist.</span><span class="sxs-lookup"><span data-stu-id="e9446-127">These settings can be changed as long as the work order is active, for example, when the work order lifecycle state changes.</span></span> <span data-ttu-id="e9446-128">Sjálfvirka valið sem gert var við stofnun verkbeiðni er byggt á uppsetningunni í **Ábyrgir viðhaldsstarfsmenn**.</span><span class="sxs-lookup"><span data-stu-id="e9446-128">The automatic selection made during work order creation is based on the setup in **Responsible maintenance workers**.</span></span> <span data-ttu-id="e9446-129">Ef þú bætir við eða fjarlægir verkbeiðniverk eftir að þú hefur búið til verkbeiðni og reiturinn **Ábyrgur hópur** og reiturinn **Ábyrgðarmaður** eru auðir þegar þú uppfærir verkbeiðnina leitar Eignastjórnun að mögulegri samsvörun í uppsetningarforminu fyrir ábyrgan viðhaldsstarfsmannahóp eða ábyrgan viðhaldsstarfsmann.</span><span class="sxs-lookup"><span data-stu-id="e9446-129">If you add or remove work order jobs after you have created a work order, and the **Responsible group** field and the **Responsible** field are blank when you update the work order, Asset Management searches for a possible match in the setup form for a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="e9446-130">Ef reiturinn **Ábyrgur hópur** eða reiturinn **Ábyrgðarmaður** eru þegar fylltir út þegar þú uppfærir verkbeiðnina verða engar breytingar gerðar.</span><span class="sxs-lookup"><span data-stu-id="e9446-130">If the **Responsible group** field or the **Responsible** field is already filled out when you update the work order, no changes are made.</span></span> 

- <span data-ttu-id="e9446-131">Í **Viðhaldsstöðu** geturðu gert útreikning til að fá yfirlit yfir vinnuálag varðandi komandi og loknar verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="e9446-131">In **Maintenance status**, you can make a calculation to get an overview of workload regarding incoming and completed work orders.</span></span>  

- <span data-ttu-id="e9446-132">Á flýtiflipanum **Línulýsing** skaltu nota reitina **Breiddargráða** og **Lengdargráða** til að bæta við landfræðilegum hnitum fyrir þá eign sem valin var í verkbeiðnivinnslunni.</span><span class="sxs-lookup"><span data-stu-id="e9446-132">On the **Line details** FastTab, use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset selected on the work order job.</span></span>  

## <a name="create-related-work-order"></a><span data-ttu-id="e9446-133">Stofna tengda verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="e9446-133">Create related work order</span></span>

<span data-ttu-id="e9446-134">Þú getur búið til tengda verkbeiðni við núverandi verkbeiðni ef þú vilt til dæmis vinna með aðal- og annars flokks verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="e9446-134">You can create a related work order to an existing work order if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="e9446-135">Ný verkbeiðni er byggð á verkbeiðnivinnslu úr fyrirliggjandi verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="e9446-135">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="e9446-136">Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="e9446-136">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e9446-137">Veldu verkbeiðnina sem þú vilt búa til tengda verkbeiðni fyrir.</span><span class="sxs-lookup"><span data-stu-id="e9446-137">Select the work order for which you want to make a related work order.</span></span>

3. <span data-ttu-id="e9446-138">Smelltu á **Tengd verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="e9446-138">Click **Related work order**.</span></span>

4. <span data-ttu-id="e9446-139">Í felliglugganum **Stofna tengda verkbeiðni** velurðu verkbeiðnivinnsluna sem þú vilt búa til tengda verkbeiðni fyrir í reitnum **Verkbeiðnivinnsla**.</span><span class="sxs-lookup"><span data-stu-id="e9446-139">In the **Create related work order** drop-down dialog, select the work order job for which you want to create a related work order in the **Work order job** field.</span></span>

5. <span data-ttu-id="e9446-140">Veldu gerð viðhaldsverks í reitnum **Gerð viðhaldsverks** og, ef þess er krafist, tengt viðhaldsverkategundafbrigði og viðskipti í reitunum **Tegundaafbrigði viðhaldsverka** og **Viðskipti**.</span><span class="sxs-lookup"><span data-stu-id="e9446-140">Select a maintenance job type in the **Maintenance job type** field and, if required, a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields.</span></span>

6. <span data-ttu-id="e9446-141">Ef þetta er fyrsta tengda verkbeiðnin sem þú gerir skaltu smella á valhringinn **Ný verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="e9446-141">If this is the first related work order you make, click the **New work order** radio button.</span></span>

7. <span data-ttu-id="e9446-142">Veldu **Gerð verkbeiðni** og **Lýsingu** í tengdum reitum.</span><span class="sxs-lookup"><span data-stu-id="e9446-142">Select a **Work order type** and a **Description** in the related fields.</span></span>

8. <span data-ttu-id="e9446-143">Ef þess er krafist skaltu breyta þjónustustigi verkbeiðni í reitnum **Þjónustustig**.</span><span class="sxs-lookup"><span data-stu-id="e9446-143">If required, change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="e9446-144">Settu inn áætlaðar upphafs- og lokadagsetningar í tengdum reitum.</span><span class="sxs-lookup"><span data-stu-id="e9446-144">Insert expected start and end dates in the related fields.</span></span>

10. <span data-ttu-id="e9446-145">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9446-145">Click **OK**.</span></span> <span data-ttu-id="e9446-146">Nýja tengda verkbeiðnin er sýnd í listanum **Allar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="e9446-146">The new related work order is shown in the **All work orders** list.</span></span>

11. <span data-ttu-id="e9446-147">Ef þú býrð til tengda verkbeiðni í verkbeiðni sem er þegar með tengdar verkbeiðnir geturðu bætt verkbeiðni vinnslunni við þegar tengda verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="e9446-147">If you create a related work order on a work order that already has related work orders, you can add the work order job to an already related work order.</span></span> <span data-ttu-id="e9446-148">Þetta er gert með því að smella á valhringinn **Bæta við tengda verkbeiðni** í 6. þrepi.</span><span class="sxs-lookup"><span data-stu-id="e9446-148">This is done by clicking the **Add to related work order** radio button in step 6.</span></span> <span data-ttu-id="e9446-149">Síðan velurðu tengda verkbeiðni sem þú vilt bæta nýju verkbeiðniverki við.</span><span class="sxs-lookup"><span data-stu-id="e9446-149">Then you select the related work order to which you want to add a new work order job.</span></span> <span data-ttu-id="e9446-150">Breyttu reitunum **Þjónustustig**, **Áætluð byrjun** og **Áætluð lok** eftir þörfum og smelltu á **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="e9446-150">Edit the **Service level**, **Expected start**, and **Expected end** fields, as required, and click **OK**.</span></span> <span data-ttu-id="e9446-151">Verkbeiðnivinnslunni er bætt við fyrirliggjandi tengda verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="e9446-151">The work order job is added to the existing related work order.</span></span>


![Mynd 1](media/03-work-orders.png)

<span data-ttu-id="e9446-153">**Athugasemd:** Ef þú hefur sett upp tengda verkbeiðnisíu í tenglinum **Færibreytur eignastýringar** > **Verkbeiðnir** > reitinn **Tengd verkbeiðnisía** verða kenni verkbeiðna stofnuð í samræmi við uppsetningu síunnar.</span><span class="sxs-lookup"><span data-stu-id="e9446-153">**Note:** If you have set up a related work order mask in **Asset management parameters** > **Work orders** link > **Related work order mask** field, work order IDs will be created in accordance with the mask setup.</span></span> <span data-ttu-id="e9446-154">Ef engin tengd verkbeiðnisía er sett upp verður næsta tiltæka kenni verkbeiðni notað fyrir tengdar verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="e9446-154">If no related work order mask is set up, the next available work order ID will be used for related work orders.</span></span>

## <a name="copy-work-order"></a><span data-ttu-id="e9446-155">Afrita verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="e9446-155">Copy work order</span></span>

<span data-ttu-id="e9446-156">Það er mögulegt að fljótt búa til nýja verkbeiðni úr núverandi verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="e9446-156">It is possible to quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="e9446-157">Þessi leið til að vinna með verkbeiðnir er frábrugðin því að búa til verkbeiðnir byggðar á viðhaldsáætlunum.</span><span class="sxs-lookup"><span data-stu-id="e9446-157">This way of working with work orders is different from creating work orders based on maintenance plans.</span></span> <span data-ttu-id="e9446-158">Það er gagnlegt ef þú hefur til dæmis verkbeiðni sem inniheldur margar verkbeiðnavinnslur með ýmsar vinnslur á mismunandi eignum sem á að ljúka með reglulegu millibili.</span><span class="sxs-lookup"><span data-stu-id="e9446-158">It is useful if, for example, you have a work order containing many work order jobs with various jobs on different assets that should be completed at regular intervals.</span></span>

1. <span data-ttu-id="e9446-159">Smelltu á **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="e9446-159">Click **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="e9446-160">Veldu verkbeiðnina sem þú vilt afrita efni úr.</span><span class="sxs-lookup"><span data-stu-id="e9446-160">Select the work order from which you want to copy content.</span></span>

3. <span data-ttu-id="e9446-161">Smelltu á **Afrita verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="e9446-161">Click **Copy work order**.</span></span> <span data-ttu-id="e9446-162">Uppsetning verkbeiðninnar úr valinni verkbeiðni er sýnd.</span><span class="sxs-lookup"><span data-stu-id="e9446-162">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="e9446-163">Ef þess er krafist geturðu breytt nokkrum reitum.</span><span class="sxs-lookup"><span data-stu-id="e9446-163">If required, you can edit some of the fields.</span></span>

4. <span data-ttu-id="e9446-164">Smelltu á **Í lagi** til að stofna nýja verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="e9446-164">Click **OK** to create the new work order.</span></span>

5. <span data-ttu-id="e9446-165">Breytu verkbeiðninni í **Allar verkbeiðnir**, ef nauðsyn krefur.</span><span class="sxs-lookup"><span data-stu-id="e9446-165">Edit the work order in **All work orders**, if required.</span></span>

>[!NOTE]
><span data-ttu-id="e9446-166">Þegar nýja verkbeiðnin er búin til eru sumar upplýsingar afritaðar beint úr fyrirliggjandi verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="e9446-166">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="e9446-167">Upplýsingar varðandi spár, verkfæri, viðhaldsgátlista, virka staðsetningu, netföng og tímasetningar eru ekki afritaðar heldur frumstilltar úr núverandi uppsetningu í Eignastjórnun.</span><span class="sxs-lookup"><span data-stu-id="e9446-167">Information regarding forecasts, tools, maintenance checklists, functional location, addresses, and scheduling is not copied, but initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="e9446-168">Þetta þýðir að ef breytingar voru gerðar í þessum gögnum frá stofnun fyrstu verkbeiðninnar þar til þú gerðir afrit af verkbeiðninni, þá eru þessar breytingar með í nýju verkbeiðninni sem þú bjóst til.</span><span class="sxs-lookup"><span data-stu-id="e9446-168">This means that if changes were made in those data from the time of creation of the first work order until the time you made a copy of the work order, those changes are included in the new work order you have created.</span></span> <span data-ttu-id="e9446-169">Dæmi um það eru breytingar á spám eða uppfærðir viðhaldsgátlistar.</span><span class="sxs-lookup"><span data-stu-id="e9446-169">Examples are changes in forecasts or updated maintenance checklists.</span></span>


![Mynd 2](media/04-work-orders.png)


## <a name="create-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="e9446-171">Stofna verkbeiðni sem byggist á viðhaldsbeiðni</span><span class="sxs-lookup"><span data-stu-id="e9446-171">Create work order based on a maintenance request</span></span>

1. <span data-ttu-id="e9446-172">Smelltu á **Eignastýring** > **Sameiginlegt** > **Viðhaldsbeiðnir** > **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="e9446-172">Click **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="e9446-173">Veldu viðhaldsbeiðni sem þú vilt búa til verkbeiðni fyrir og smelltu á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="e9446-173">Select the maintenance request for which you want to create a work order, and click **Edit**.</span></span>

3. <span data-ttu-id="e9446-174">Í **Öllum beiðnum** smellirðu á **Verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="e9446-174">In **All requests**, click **Work order**.</span></span>

4. <span data-ttu-id="e9446-175">Fylltu út fellivalmyndina **Verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="e9446-175">Fill out the **Work order** drop-down.</span></span> <span data-ttu-id="e9446-176">Ef gerð viðhaldsverks hefur verið valin í viðhaldsbeiðninni geturðu valið aðra tegund viðhaldsverka, ef þörf krefur, þegar þú stofnar verkbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="e9446-176">If a maintenance job type has been selected in the maintenance request, you are able to select another maintenance job type, if required, when you create the work order.</span></span>

5. <span data-ttu-id="e9446-177">Smellt er á **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9446-177">Click **OK**.</span></span> <span data-ttu-id="e9446-178">Þú munt sjá skilaboð sem segja þér að verkbeiðnin hafi verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="e9446-178">You will see a message informing you that the work order has been created.</span></span>

6. <span data-ttu-id="e9446-179">Ef þú vilt sjá hvaða verkbeiðnir tengjast viðhaldsbeiðni skaltu velja viðhaldsbeiðnina í listunum **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir** og smella á hnappinn **Verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="e9446-179">If you want to see which work orders are connected to a maintenance request, select the maintenance request in the **All maintenance requests** or **Active maintenance requests** lists, and click the **Work orders** button.</span></span>


![Mynd 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="e9446-181">Verkbeiðnir geta einnig verið stofnaðar sjálfkrafa með því að tímasetja vinnslur viðhaldsáætlana, eða með því að setja upp „Stofna sjálfkrafa“ viðhaldsáætlanir eða viðhaldslotur á eign.</span><span class="sxs-lookup"><span data-stu-id="e9446-181">Work orders can also be created automatically by scheduling maintenance plan jobs, or by setting up "Auto create" maintenance plans or maintenance rounds on an asset.</span></span> <span data-ttu-id="e9446-182">Verkbeiðnir stofnaðar úr viðhaldsbeiðnum í **Viðhaldsáætlun** eru stofnaðar með þeim gerðum viðhaldsverka sem valdar eru í viðhaldsbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="e9446-182">Work orders created from maintenance requests in **Maintenance schedule** are created with the maintenance job types selected in the maintenance requests.</span></span>

