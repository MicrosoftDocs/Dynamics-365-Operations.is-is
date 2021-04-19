---
title: Handvirkt stofnaðar verkbeiðnir
description: Þetta efni útskýrir hvernig á að stofna verkbeiðnir handvirkt í eignastýringu.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderTableCreateRelated, EntAssetWorkOrderTableCreate, EntAssetWorkOrderTableCopy
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8962cbbc8f413093eef0fb3783aa6ced22f7bc2d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839560"
---
# <a name="manually-created-work-orders"></a><span data-ttu-id="23f87-103">Handvirkt stofnaðar verkbeiðnir</span><span class="sxs-lookup"><span data-stu-id="23f87-103">Manually created work orders</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="23f87-104">Hægt er að stofna verkbeiðnir handvirkt á tvo vegu:</span><span class="sxs-lookup"><span data-stu-id="23f87-104">You can create work orders manually in two ways:</span></span>

- <span data-ttu-id="23f87-105">Á síðunni **Allar verkbeiðnir** eða **Virkar verkbeiðnir**</span><span class="sxs-lookup"><span data-stu-id="23f87-105">On the **All work orders** or **Active work orders** page</span></span> 
- <span data-ttu-id="23f87-106">Á síðunni **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir** eða **Mínar viðhaldsbeiðnir á virkri staðsetningu**.</span><span class="sxs-lookup"><span data-stu-id="23f87-106">On the **All maintenance requests** or **Active maintenance requests** or **My functional location maintenance requests** page</span></span> 

## <a name="create-work-order"></a><span data-ttu-id="23f87-107">Stofna verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="23f87-107">Create work order</span></span>

1. <span data-ttu-id="23f87-108">Veldu **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="23f87-108">Selece **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="23f87-109">Veljið **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="23f87-109">Select **New**.</span></span>

3. <span data-ttu-id="23f87-110">Í glugganum **Stofna verkbeiðni** velurðu gerð verkbeiðni í reitnum **Gerð verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="23f87-110">In the **Create work order** dialog, select a work order type in the **Work order type** field.</span></span>

4. <span data-ttu-id="23f87-111">Ef þess er krafist skal velja **Lýsingu**.</span><span class="sxs-lookup"><span data-stu-id="23f87-111">If required, select a **Description**.</span></span>

5. <span data-ttu-id="23f87-112">Í reitnum **Eign** velurðu eignina.</span><span class="sxs-lookup"><span data-stu-id="23f87-112">In the **Asset** field, select the asset.</span></span>

>[!NOTE]
><span data-ttu-id="23f87-113">Þegar þú velur eign gætu þrír flipar verið tiltækir í fellivalmyndinni **Eignir**:</span><span class="sxs-lookup"><span data-stu-id="23f87-113">When you select an asset, three tabs might be available in the **Asset** drop-down:</span></span> 

- <span data-ttu-id="23f87-114">**Virkar eignir** - Þessi flipi inniheldur lista yfir allar eignir sem hafa eignalíftímastöðuna „Virkt“.</span><span class="sxs-lookup"><span data-stu-id="23f87-114">**Active assets** - This tab contains a list of all assets that have an "Active" asset lifecycle state.</span></span> 
- <span data-ttu-id="23f87-115">**Eignayfirlit** - Þessi flipi sýnir trjáyfirlit yfir virkar staðseningar og eignirnar sem eru settar upp á þeim.</span><span class="sxs-lookup"><span data-stu-id="23f87-115">**Asset view** - This tab displays a tree view of functional locations and the assets installed on them.</span></span>
- <span data-ttu-id="23f87-116">**Mínar eignir** - Þessi flipi inniheldur eignir sem tengjast virkum staðsetningum sem þú (starfsmaðurinn sem er skráður inn í kerfið) getur verið úthlutað á.</span><span class="sxs-lookup"><span data-stu-id="23f87-116">**My assets** - This tab contains assets that are related to the functional locations that you (the worker who is signed in to the system) may be allocated to.</span></span> <span data-ttu-id="23f87-117">(Sjá upplýsingar um uppsetninguna í [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md).) Ef engar virkar staðsetningar eru settar upp á starfskrafti í [Viðhaldsstarfsmenn og starfsmannahópar](../setup-for-objects/workers-and-worker-groups.md) er flipinn **Mínar eignir** ekki tiltækur.</span><span class="sxs-lookup"><span data-stu-id="23f87-117">(For information about the setup, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).) If no functional locations are set up on a worker in [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md), the **My assets** tab isn't available.</span></span> 

6. <span data-ttu-id="23f87-118">Í reitnum **Tegund viðhaldsverka** velurðu gerð viðhaldsverka fyrir verkbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="23f87-118">In the **Maintenance job type** field, select a maintenance job type for the work order.</span></span>

7. <span data-ttu-id="23f87-119">Ef þörf krefur skaltu velja **Afbrigði af gerð viðhaldsstarfa** og **Viðskipti**.</span><span class="sxs-lookup"><span data-stu-id="23f87-119">If required, select **Maintenance job type variant** and **Trade**.</span></span>

8. <span data-ttu-id="23f87-120">Ef þess er krafist geturðu breytt þjónustustigi verkbeiðni í reitnum **Þjónustustig**.</span><span class="sxs-lookup"><span data-stu-id="23f87-120">If required, you can change the work order service level in the **Service level** field.</span></span>

9. <span data-ttu-id="23f87-121">Veldu dagsetningarnar **Væntanlegt upphaf** og **Væntanleg lok** í tengdum reitum.</span><span class="sxs-lookup"><span data-stu-id="23f87-121">Select **Expected start** and **Expected end** dates in the related fields.</span></span>

10. <span data-ttu-id="23f87-122">Smelltu á **Í lagi** til að stofna verkbeiðnina.</span><span class="sxs-lookup"><span data-stu-id="23f87-122">Click **OK** to create the work order.</span></span>

11. <span data-ttu-id="23f87-123">Á listasíðunni **Allar verkbeiðnir** er hægt að breyta verkbeiðninni eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="23f87-123">On the **All work orders** list page, you can edit the work order as you require.</span></span>

<span data-ttu-id="23f87-124">Athugið eftirfarandi stig:</span><span class="sxs-lookup"><span data-stu-id="23f87-124">Note the following points:</span></span>

- <span data-ttu-id="23f87-125">Á listasíðunni **Allar verkbeiðnir** er hægt að bæta nokkrum eignum við verkbeiðni í smáatriðum með því að bæta við línum á flýtiflipanum **Viðhaldsverk verkbeiðna**.</span><span class="sxs-lookup"><span data-stu-id="23f87-125">In the details view on the **All work orders** list page, you can add several assets to a work order by adding lines on the **Work order maintenance jobs** FastTab.</span></span> <span data-ttu-id="23f87-126">Á eign er aðeins hægt að velja gerðir viðhaldsverka sem eru skilgreindar á eignategundinni sem er valin á eigninni.</span><span class="sxs-lookup"><span data-stu-id="23f87-126">On an asset, you can select only the maintenance job types that are defined on the asset type that is selected on the asset.</span></span>  

- <span data-ttu-id="23f87-127">Ef þú breytir þjónustustigi eigna eða mikilvægi eigna eftir að þú hefur notað eignina í verkbeiðni, er þjónustustigið eða mikilvægi á verkbeiðninnar ekki uppfært til samræmis.</span><span class="sxs-lookup"><span data-stu-id="23f87-127">If you change an asset service level or an asset criticality after you've used the asset on a work order, the service level or criticality on the work order isn't updated accordingly.</span></span> <span data-ttu-id="23f87-128">Fyrir frekari upplýsingar um þjónustustig og mikilvægi, sjá [Þjónustustig eigna](../setup-for-objects/object-priorities.md) og [Mikilvægisgerðir eigna](../setup-for-objects/object-criticalities.md).</span><span class="sxs-lookup"><span data-stu-id="23f87-128">For more information about service levels and criticalities, see [Asset service levels](../setup-for-objects/object-priorities.md) and [Asset criticality types](../setup-for-objects/object-criticalities.md).</span></span>

- <span data-ttu-id="23f87-129">Mikilvægi á verkbeiðni er endurútreiknað í hvert skipti sem vinnslu verkbeiðni er bætt við eða henni eytt úr verkbeiðninni.</span><span class="sxs-lookup"><span data-stu-id="23f87-129">Criticality on a work order is recalculated every time a work order job is added to or deleted from the work order.</span></span>

- <span data-ttu-id="23f87-130">Í upplýsingaglugganum **Allar verkbeiðnir** > flipanum **Haus** > flýtiflipanum **Áætlun** í reitunum **Ábyrgur hópur** eða **Ábyrgðarmaður** geturðu valið ábyrgan starfsmanahóp eða ábyrgan viðhaldsstarfsmann.</span><span class="sxs-lookup"><span data-stu-id="23f87-130">In the **All work orders** details view > **Header** tab > **Schedule** FastTab, in the **Responsible group** or **Responsible** field, you can select a responsible maintenance worker group or a responsible maintenance worker.</span></span> <span data-ttu-id="23f87-131">Þessum stillingum er hægt að breyta meðan verkbeiðnin er virk.</span><span class="sxs-lookup"><span data-stu-id="23f87-131">These settings can be changed while the work order is active.</span></span> <span data-ttu-id="23f87-132">Til dæmis er hægt að breyta þeim þegar ástand líftíma verkbeiðni breytist.</span><span class="sxs-lookup"><span data-stu-id="23f87-132">For example, they can be changed when the work order lifecycle state changes.</span></span> <span data-ttu-id="23f87-133">Sjálfvirka valið sem gert var við stofnun verkbeiðni er byggt á uppsetningunni á síðunni **Ábyrgir viðhaldsstarfsmenn**.</span><span class="sxs-lookup"><span data-stu-id="23f87-133">The automatic selection that is made during work order creation is based on the setup on the **Responsible maintenance workers** page.</span></span> <span data-ttu-id="23f87-134">Ef þú bætir við eða fjarlægir verkbeiðniverk eftir að þú hefur búið til verkbeiðni og ef reiturinn **Ábyrgur hópur** og reiturinn **Ábyrgðarmaður** eru auðir þegar þú uppfærir verkbeiðnina reynir Eignastjórnun að finna ábyrgan viðhaldsstarfsmannahóp eða ábyrgan viðhaldsstarfsmann fyrir hugsanlega samsvörun á uppsetningarsíðunni.</span><span class="sxs-lookup"><span data-stu-id="23f87-134">If you add or remove work order jobs after you've created a work order, and if the **Responsible group** and **Responsible** fields are blank when you update the work order, Asset Management tries to find a responsible maintenance worker group or a responsible maintenance worker for a possible match on the setup page.</span></span> <span data-ttu-id="23f87-135">Ef reiturinn **Ábyrgur hópur** eða reiturinn **Ábyrgðarmaður** eru þegar stilltir þegar þú uppfærir verkbeiðnina verða engar breytingar gerðar.</span><span class="sxs-lookup"><span data-stu-id="23f87-135">If the **Responsible group** or **Responsible** field is already set when you update the work order, no changes are made.</span></span> <span data-ttu-id="23f87-136">Nánari upplýsingar um hvernig á að setja upp starfskrafta og viðhaldsstarfsmannahóps er að finna í [Ábyrgir viðhaldsstarfskraftar](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="23f87-136">For more information about responsible maintenance workers and worker groups, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>

- <span data-ttu-id="23f87-137">Af síðunni [Viðhaldsstaða](../controlling-and-reporting/maintenance-status.md) er hægt að gera útreikning til að fá yfirlit yfir vinnuálag varðandi komandi og loknar verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="23f87-137">From the [Maintenance status](../controlling-and-reporting/maintenance-status.md) page, you can do a calculation to get an overview of the workload for incoming and completed work orders.</span></span>  

- <span data-ttu-id="23f87-138">Í upplýsingayfirlitinu á síðunni **Allar verkbeiðnir**, á flýtiflipanum **Línulýsing**, er hægt að nota reitina **Breidd** og **Lengdargráða** til að bæta við landfræðilegum hnitum fyrir eignina sem er valin í vinnslu verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="23f87-138">In the details view of the **All work orders** page, on the **Line details** FastTab, you can use the **Latitude** and **Longitude** fields to add geographic coordinates for the asset that is selected on the work order job.</span></span>  


## <a name="create-related-work-order"></a><span data-ttu-id="23f87-139">Stofna tengda verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="23f87-139">Create related work order</span></span>

<span data-ttu-id="23f87-140">Hægt er að stofna verkbeiðni sem tengist fyrirliggjandi verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="23f87-140">You can create a work order that is related to an existing work order.</span></span> <span data-ttu-id="23f87-141">Þessi afkastageta er gagnleg ef þú vilt til dæmis vinna með aðal- og annars flokks verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="23f87-141">This capability is useful if, for example, you want to work with primary and secondary work orders.</span></span> <span data-ttu-id="23f87-142">Ný verkbeiðni er byggð á verkbeiðnivinnslu úr fyrirliggjandi verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="23f87-142">A new work order is based on a work order job from an existing work order.</span></span>

1. <span data-ttu-id="23f87-143">Veldu **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="23f87-143">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="23f87-144">Veldu verkbeiðnina til að stofna tengda verkbeiðni fyrir.</span><span class="sxs-lookup"><span data-stu-id="23f87-144">Select the work order to create a related work order for.</span></span>

3. <span data-ttu-id="23f87-145">Á aðgerðarrúðunni, á flipanum **Verkbeiðni**, í hópnum **Nýtt** skaltu velja **Tengd verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="23f87-145">On the Action Pane, on the **Work order** tab, in the **New** group, select **Related work order**.</span></span>

4. <span data-ttu-id="23f87-146">Í glugganum **Stofna tengda verkbeiðni**, í reitnum **Verkbeiðnivinnsla**, velurðu verkbeiðnivinnsluna sem þú vilt búa til tengda verkbeiðni fyrir.</span><span class="sxs-lookup"><span data-stu-id="23f87-146">In the **Create related work order** dialog, in the **Work order job** field, select the work order job to create a related work order for.</span></span>

5. <span data-ttu-id="23f87-147">Veldu gerð viðhaldsverka í reitnum **Tegund viðhaldsverka**.</span><span class="sxs-lookup"><span data-stu-id="23f87-147">Select a maintenance job type in the **Maintenance job type** field.</span></span>

6. <span data-ttu-id="23f87-148">Veldu tengt afbrigði og viðskipti viðhaldsverks í reitunum **Afbrigði af gerð viðhaldsverka** og **Viðskipti**, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="23f87-148">Select a related maintenance job type variant and trade in the **Maintenance job type variant** and **Trade** fields, as you require.</span></span>

7. <span data-ttu-id="23f87-149">Ef þessi verkbeiðni er fyrsta tengda verkbeiðnin sem hefur verið búin til fyrir valda verkbeiðni, fylgdu þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="23f87-149">If this work order is the first related work order that has been created for the selected work order, follow these steps:</span></span>
    1. <span data-ttu-id="23f87-150">Veldu valkostinn **Ný verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="23f87-150">Select the **New work order** option.</span></span>
    2. <span data-ttu-id="23f87-151">Í reitnum **Verkbeiðni** velurðu gerð verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="23f87-151">In  the **Work order type** field, select a work order type.</span></span>
    3. <span data-ttu-id="23f87-152">Í **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="23f87-152">In the **Description**, enter a description.</span></span>
    4. <span data-ttu-id="23f87-153">Í reitnum **Þjónustustig** skaltu breyta þjónustustigi verkbeiðna eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="23f87-153">In the **Service level** field, change the work order service level as you require.</span></span>
    5. <span data-ttu-id="23f87-154">Í reitunum **Væntanlegt upphaf** og **Væntanleg lok** velurðu væntar upphafs- og lokadagsetningar.</span><span class="sxs-lookup"><span data-stu-id="23f87-154">In the **Expected start** and **Expected end** fields, select the expected start and end dates.</span></span>
    6. <span data-ttu-id="23f87-155">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="23f87-155">Select **OK**.</span></span> <span data-ttu-id="23f87-156">Nýja tengda verkbeiðnin er sýnd á listasíðunni **Allar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="23f87-156">The new related work order is shown on the **All work orders** list page.</span></span>  

8. <span data-ttu-id="23f87-157">Ef verkbeiðnin sem þú ert að stofna þessa skyldu verkbeiðni fyrir er þegar með tengdar verkbeiðnir, fylgdu þessum skrefum til að bæta nýrri vinnslu verkbeiðni við fyrirliggjandi tengda verkbeiðni:</span><span class="sxs-lookup"><span data-stu-id="23f87-157">If the work order that you're creating this related work order for already has related work orders, follow these steps to add a new work order job to an existing related work order:</span></span>
    1. <span data-ttu-id="23f87-158">Veldu valkostinn **Bæta við tengdri verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="23f87-158">Select the **Add to related work order** option.</span></span>
    2. <span data-ttu-id="23f87-159">Í reitnum **Verkbeiðni** velurðu tengda verkbeiðni sem þú vilt bæta nýju verkbeiðniverki við.</span><span class="sxs-lookup"><span data-stu-id="23f87-159">In the **Work order** field, select the related work order to add a new work order job to.</span></span>
    3. <span data-ttu-id="23f87-160">Í reitnum **Þjónustustig** skaltu breyta þjónustustigi verkbeiðna eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="23f87-160">In the **Service level** field, change the work order service level as you require.</span></span>
    4. <span data-ttu-id="23f87-161">Í reitunum **Væntanlegt upphaf** og **Væntanleg lok** breytirðu væntum upphafs- og lokadagsetningum, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="23f87-161">In the **Expected start** and **Expected end** fields, change the expected start and end dates as you require.</span></span>
    5. <span data-ttu-id="23f87-162">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="23f87-162">Select **OK**.</span></span> <span data-ttu-id="23f87-163">Verkbeiðnivinnslunni er bætt við fyrirliggjandi tengda verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="23f87-163">The work order job is added to the existing related work order.</span></span>

<span data-ttu-id="23f87-164">Skýringarmyndin hér að neðan sýnir dæmi um gluggann **Stofna tengda verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="23f87-164">The illustration below shows an example of the **Create related work order** dialog.</span></span>

![Mynd 1](media/03-work-orders.png)

>[!NOTE]
><span data-ttu-id="23f87-166">Athugasemd: Ef þú hefur sett upp tengda verkbeiðnisíu á flipanum **Færibreytur eignastýringar** > **Verkbeiðnir** > reitnum **Tengd verkbeiðnisía** verða kenni verkbeiðna stofnuð í samræmi við uppsetningu síunnar.</span><span class="sxs-lookup"><span data-stu-id="23f87-166">If you've set up a related work order mask in **Asset management parameters** > **Work orders** tab > **Related work order mask** field, work order IDs are created according to the mask setup.</span></span> <span data-ttu-id="23f87-167">Ef engin tengd verkbeiðnisía er sett upp er næsta tiltæka kenni verkbeiðni notað fyrir tengdar verkbeiðnir.</span><span class="sxs-lookup"><span data-stu-id="23f87-167">If no related work order mask is set up, the next available work order ID is used for related work orders.</span></span>

## <a name="copy-a-work-order"></a><span data-ttu-id="23f87-168">Afrita verkbeiðni</span><span class="sxs-lookup"><span data-stu-id="23f87-168">Copy a work order</span></span>

<span data-ttu-id="23f87-169">Það er mögulegt að fljótt búa til nýja verkbeiðni úr núverandi verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="23f87-169">You can quickly create a new work order from an existing work order.</span></span> <span data-ttu-id="23f87-170">Þessi leið til að vinna með verkbeiðnir er frábrugðin stofnun verkbeiðna samkvæmt [viðhaldsáætlunum](../preventive-and-reactive-maintenance/maintenance-plans.md).</span><span class="sxs-lookup"><span data-stu-id="23f87-170">This way of working with work orders differs from the creation of work orders based on [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md).</span></span> <span data-ttu-id="23f87-171">Það er gagnlegt ef þú hefur til dæmis verkbeiðni sem inniheldur margar verkbeiðnavinnslur og ljúka skal ýmsum vinnslum á mismunandi eignum með reglulegu millibili.</span><span class="sxs-lookup"><span data-stu-id="23f87-171">It's useful if, for example, a work order contains many work order jobs, and the various jobs should be completed on different assets at regular intervals.</span></span>

1. <span data-ttu-id="23f87-172">Veldu **Eignastýringu** > **Sameiginlegt** > **Verkbeiðnir** > **Allar verkbeiðnir** eða **Virkar verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="23f87-172">Select **Asset management** > **Common** > **Work orders** > **All work orders** or **Active work orders**.</span></span>

2. <span data-ttu-id="23f87-173">Veldu verkbeiðnina til að afrita efni úr.</span><span class="sxs-lookup"><span data-stu-id="23f87-173">Select the work order to copy content from.</span></span>

3. <span data-ttu-id="23f87-174">Á aðgerðarrúðunni > flipanum **Verkbeiðni** > hópnum **Nýtt** skaltu velja **Afrita verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="23f87-174">On the Action Pane > **Work order** tab > **New** group, select **Copy work order**.</span></span>

4. <span data-ttu-id="23f87-175">Uppsetning verkbeiðninnar úr valinni verkbeiðni er sýnd.</span><span class="sxs-lookup"><span data-stu-id="23f87-175">The work order setup from the selected work order is shown.</span></span> <span data-ttu-id="23f87-176">Hægt er að breyta nokkrum reitanna, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="23f87-176">You can edit some of the fields as you require.</span></span>

5. <span data-ttu-id="23f87-177">Veldu **Í lagi** til að stofna nýja verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="23f87-177">Select **OK** to create the new work order.</span></span>

6. <span data-ttu-id="23f87-178">Á listasíðunni **Allar verkbeiðnir** er hægt að breyta verkbeiðninni eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="23f87-178">On the **All work orders** list page, you can edit the work order as you require.</span></span>

>[!NOTE]
><span data-ttu-id="23f87-179">Þegar nýja verkbeiðnin er búin til eru sumar upplýsingar afritaðar beint úr fyrirliggjandi verkbeiðni.</span><span class="sxs-lookup"><span data-stu-id="23f87-179">When the new work order is created, some information is copied directly from the existing work order.</span></span> <span data-ttu-id="23f87-180">Upplýsingar um spár, verkfæri, viðhaldsgátlista, virka staðsetningu, heimilisföng og tímasetningar eru ekki afritaðar.</span><span class="sxs-lookup"><span data-stu-id="23f87-180">Information about forecasts, tools, maintenance checklists, functional location, addresses, and scheduling isn't copied.</span></span> <span data-ttu-id="23f87-181">Í staðinn eru þær frumstilltar úr núverandi uppsetningu í Eignastjórnun.</span><span class="sxs-lookup"><span data-stu-id="23f87-181">Instead, it's initialized from the current setup in Asset Management.</span></span> <span data-ttu-id="23f87-182">Þess vegna, ef þeim upplýsingum var breytt á milli tímabilsins þegar fyrsta verkbeiðnin var búin til og þess tíma þegar þú bjóst til afrit af verkbeiðninni, eru breytingarnar með í nýju verkbeiðninni.</span><span class="sxs-lookup"><span data-stu-id="23f87-182">Therefore, if that information was changed between the time when the first work order was created and the time when you made a copy of the work order, the changes are included in the new work order.</span></span> <span data-ttu-id="23f87-183">Dæmi um það eru breytingar á spám og uppfærslur á viðhaldsgátlistum.</span><span class="sxs-lookup"><span data-stu-id="23f87-183">Examples include changes to forecasts and updates to maintenance checklists.</span></span>

<span data-ttu-id="23f87-184">Myndin hér að neðan sýnir dæmi um gluggann **Afrita verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="23f87-184">The illustration below shows an example of the **Copy work order** dialog.</span></span>

![Mynd 2](media/04-work-orders.png)


## <a name="create-a-work-order-based-on-a-maintenance-request"></a><span data-ttu-id="23f87-186">Stofna verkbeiðni sem byggist á viðhaldsbeiðni</span><span class="sxs-lookup"><span data-stu-id="23f87-186">Create a work order based on a maintenance request</span></span>

1. <span data-ttu-id="23f87-187">Veldu **Eignastýring** > **Sameiginlegt** > **Viðhaldsbeiðnir** > **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="23f87-187">Select **Asset management** > **Common** > **Maintenance requests** > **All maintenance requests** or **Active maintenance requests**.</span></span>

2. <span data-ttu-id="23f87-188">Veldu viðhaldsbeiðni til að stofna verkbeiðni fyrir og smelltu á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="23f87-188">Select the maintenance request to create a work order for, and click **Edit**.</span></span>

3. <span data-ttu-id="23f87-189">Á aðgerðarrúðunni > flipanum **Viðhaldsbeiðni** > hópnum **Nýtt** skaltu velja **Verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="23f87-189">On the Action Pane > **Maintenance request** tab > **New** group, select **Work order**.</span></span>

4. <span data-ttu-id="23f87-190">Í glugganum **Verkbeiðni** skaltu stilla reitina.</span><span class="sxs-lookup"><span data-stu-id="23f87-190">In the **Work order** dialog, set the fields.</span></span> <span data-ttu-id="23f87-191">Ef gerð viðhaldsverks hefur verið valin í viðhaldsbeiðninni geturðu valið aðra tegund viðhaldsverka, ef þörf krefur, þegar þú stofnar verkbeiðnina, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="23f87-191">If a maintenance job type has been selected in the maintenance request, you can select a different maintenance job type when you create the work order, as you require.</span></span>

5. <span data-ttu-id="23f87-192">Veljið **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="23f87-192">Select **OK**.</span></span> <span data-ttu-id="23f87-193">Skilaboð tilkynna þér að verkbeiðni hefur verið stofnuð.</span><span class="sxs-lookup"><span data-stu-id="23f87-193">A message notifies you that the work order has been created.</span></span>

6. <span data-ttu-id="23f87-194">Til að sjá verkbeiðnirnar sem tengjast viðhaldsbeiðni skaltu velja viðhaldsbeiðnina á listasíðunni **Allar viðhaldsbeiðnir** eða **Virkar viðhaldsbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="23f87-194">To view the work orders that are connected to a maintenance request, on the **All maintenance requests** or **Active maintenance requests** list page, select the maintenance request.</span></span> <span data-ttu-id="23f87-195">Síðan, á aðgerðarrúðunni, á flipanum **Viðhaldsbeiðni**, í hópnum **Skoða**, skaltu velja **Verkbeiðnir**.</span><span class="sxs-lookup"><span data-stu-id="23f87-195">Then, on the Action Pane, on the **Maintenance request** tab, in the **View** group, select **Work orders**.</span></span>


<span data-ttu-id="23f87-196">Myndin hér að neðan sýnir dæmi um gluggann **Stofna verkbeiðni**.</span><span class="sxs-lookup"><span data-stu-id="23f87-196">The illustration below shows an example of the **Create work order** dialog.</span></span>

![Mynd 3](media/05-work-orders.png)


>[!NOTE]
><span data-ttu-id="23f87-198">Ef þú vilt að verkbeiðnir sé sjálfvirkt stofnaðar er hægt að tímastilla vinnslur viðhaldsáætlana eða hægt er að setja upp „Stofna sjálfvirkt“ [viðhaldsáætlanir](../preventive-and-reactive-maintenance/maintenance-plans.md) eða [viðhaldslotur](../preventive-and-reactive-maintenance/maintenance-rounds.md) á eign.</span><span class="sxs-lookup"><span data-stu-id="23f87-198">If you want work orders to be created automatically, you can schedule maintenance plan jobs, or you can set up "Auto create" [maintenance plans](../preventive-and-reactive-maintenance/maintenance-plans.md) or [maintenance rounds](../preventive-and-reactive-maintenance/maintenance-rounds.md) on an asset.</span></span> <span data-ttu-id="23f87-199">Verkbeiðnir sem eru stofnaðar úr viðhaldsbeiðnum á listasíðunni **Öll viðhaldsskemu** eru með þær gerðir viðhaldsverka sem eru valdar í viðhaldsbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="23f87-199">Work orders that are created from maintenance requests on the **All maintenance schedule** list page have the maintenance job types that are selected on the maintenance requests.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]