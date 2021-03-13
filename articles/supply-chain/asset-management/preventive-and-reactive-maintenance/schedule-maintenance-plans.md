---
title: Tímasetja viðhaldsáætlanir
description: Þetta efni skýrir tímasetningu viðhaldsáætlana í eignastýringu.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 9c215417eacb8a0e1ec0a8324fe35fc053089afb
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/16/2021
ms.locfileid: "5016907"
---
# <a name="schedule-maintenance-plans"></a><span data-ttu-id="00f11-103">Tímasetja viðhaldsáætlanir</span><span class="sxs-lookup"><span data-stu-id="00f11-103">Schedule maintenance plans</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="00f11-104">Skipulagning forvirks viðhalds býr til dagatalsfærslur á eignum, byggt á viðhaldsáætlunum sem settar eru upp á eignunum.</span><span class="sxs-lookup"><span data-stu-id="00f11-104">Preventive maintenance scheduling generates calendar entries on assets, based on the maintenance plans set up on the assets.</span></span> <span data-ttu-id="00f11-105">Þú getur skipulagt dagatalfærslur út frá völdum viðhaldsáætlunum, eignategundum og eignum.</span><span class="sxs-lookup"><span data-stu-id="00f11-105">You can schedule calendar entries based on selected maintenance plans, asset types, and assets.</span></span>

1. <span data-ttu-id="00f11-106">Smelltu á **Eignastjórnun** > **Reglubundið** > **Forvirkt viðhald** > **Skipuleggja viðhaldsáætlanir**.</span><span class="sxs-lookup"><span data-stu-id="00f11-106">Click **Asset management** > **Periodic** > **Preventive maintenance** > **Schedule maintenance plans**.</span></span>

2. <span data-ttu-id="00f11-107">Þú getur valið tímabil í reitunum **Tímabil** og **Tímabilstíðni**.</span><span class="sxs-lookup"><span data-stu-id="00f11-107">You can select a time interval in the **Period** and **Period frequency** fields.</span></span>

>[!NOTE]
><span data-ttu-id="00f11-108">Reitirnir **Tímabil** og **Tímabilstíðni** gefa til kynna hversu langt fram í tímann þú vilt að viðhaldsáætlunarlínur séu búnar til, byggt á viðhaldsáætlunum sem þú hefur búið til (tímabyggðum eða teljarabyggðum).</span><span class="sxs-lookup"><span data-stu-id="00f11-108">The **Period** and **Period frequencey** fields indicate how far ahead in time you want maintenance schedule lines to be created, based on the maintenance plans you have created (time-based or counter-based).</span></span> <span data-ttu-id="00f11-109">Á myndinni hér að neðan eru viðhaldsskemalínur (= tillögur um verkbeiðnir) búnar til frá núverandi degi og þrjá mánuði fram í tímann.</span><span class="sxs-lookup"><span data-stu-id="00f11-109">In the figure below, maintenance schedule lines (= work order proposals) are created from the current date and three months onwards.</span></span>

3. <span data-ttu-id="00f11-110">Veldu „Já“ á skiptihnappnum **Stofna sjálfkrafa ef tilgreint í línunni** ef verkbeiðnir eiga að vera sjálfkrafa stofnaðar í samræmi við viðhaldsáætlunarlínuna.</span><span class="sxs-lookup"><span data-stu-id="00f11-110">Select "Yes" on the **Auto create if specified in the line** toggle button if work orders should automatically be created according to the maintenance plan line.</span></span>

>[!NOTE]
><span data-ttu-id="00f11-111">Ef þessi rofahnappur er stilltur á „Já“ *og* gátreiturinn **Stofna sjálfvirkt** er einnig valinn í viðhaldsáætlunarlínum í skjámyndinni **Viðhaldsáætlanir** eru verkbeiðnir búnar til út frá viðhaldsáætlunarlínum og viðhaldsskemalínur með stöðuna „Verkbeiðni stofnuð“ eru einnig stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="00f11-111">If this toggle button is set to "Yes", *and* the **Auto create** check box is also selected on maintenance plan lines in **Maintenance plans**, work orders are created based on the maintenance plan lines, and maintenance schedule lines with status "Work order created" are also created.</span></span> <span data-ttu-id="00f11-112">Ef aðeins einn valkostur er valinn (**Stofna sjálfkrafa ef tilgreint í línunni** rofahnappinn í þessum glugga eða gátreitnum **Stofna sjálfkrafa** í skjámyndinni **Viðhaldsáætlanir**) eru aðeins viðhaldsskemalínur búnar til með stöðuna „Stofnað“.</span><span class="sxs-lookup"><span data-stu-id="00f11-112">If only one option is selected (**Auto create if specified in the line** toggle button in this dialog or **Auto create** check box in **Maintenance plans** form), only maintenance schedule lines are created with status "Created".</span></span> <span data-ttu-id="00f11-113">Þá eru engar verkbeiðnir stofnaðar.</span><span class="sxs-lookup"><span data-stu-id="00f11-113">In that case, no work orders are created.</span></span>

4. <span data-ttu-id="00f11-114">Það er hægt að búa til dagatalsfærslur byggðar á viðhaldsáætlunum (tíma eða teljara), eignum, eignategundum, virkum stöðum og virkum staðartegundum.</span><span class="sxs-lookup"><span data-stu-id="00f11-114">It is possible to generate calendar entries based on maintenance plans (time or counter), assets, asset types, functional locations, and functional location types.</span></span> <span data-ttu-id="00f11-115">Smelltu á hnappinn **Sía** og gerðu val þitt ef þess er krafist.</span><span class="sxs-lookup"><span data-stu-id="00f11-115">Click the **Filter** button and make your selections, if required.</span></span>

- <span data-ttu-id="00f11-116">Varðandi röðun á viðhaldsáætlunum á virkum staðsetningum: Ef þú uppfærir uppsetningu á eignategundum, framleiðendum og tegundum í viðhaldsáætlunum í flýtiflipanum **Allar virkar staðsetningar** > **Viðhaldsáætlanir** eftir að þú hefur skipulagt viðhaldsáætlanir, verður núverandi viðhaldsskemafærslum sem tengjast þeirri virku staðsetningu sjálfkrafa eytt.</span><span class="sxs-lookup"><span data-stu-id="00f11-116">Regarding scheduling of maintenance plans on functional locations: If you update the setup of asset types, manufacturers, and models on maintenance plans in **All functional locations** > **Maintenance plans** FastTab after you have scheduled maintenance plans, existing maintenance schedule entries related to that functional location are automatically deleted.</span></span> <span data-ttu-id="00f11-117">Til að stofna nýjar dagatalsfærslur sem samsvara uppfærðri viðhaldsáætlunaruppsetningu á virkri staðsetningu verður þú að keyra nýja viðhaldsáætlun fyrir þá virku staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="00f11-117">In order to create new calendar entries, which correspond with the updated maintenance plan setup on the functional location, you must run a new maintenance plan schedule for that functional location.</span></span> <span data-ttu-id="00f11-118">Lestu meira um uppsetningu á eignategundum, framleiðendum og tegundum um virkar staðsetningar í [Stofna virkar staðsetningar](../functional-locations/create-functional-locations.md).</span><span class="sxs-lookup"><span data-stu-id="00f11-118">Read more about the setup of asset types, manufacturers, and models on functional locations in [Create functional locations](../functional-locations/create-functional-locations.md).</span></span>

><span data-ttu-id="00f11-119">*Dæmi:* Þú vilt búa til viðhaldsáætlun fyrir tiltekna virka staðsetningu, sem þýðir að allar eignir sem settar eru upp á þeirri virku staðsetningu á hverjum tíma verða með þegar þú áætlar viðhaldsáætlun.</span><span class="sxs-lookup"><span data-stu-id="00f11-119">*Example:* You want to create a maintenance plan for a specific functional location, meaning all assets set up on that functional location at any given time will be included when you schedule the maintenance plan.</span></span> <span data-ttu-id="00f11-120">Í því tilfelli býrðu til viðhaldsáætlun og velur sérstaka virka staðsetningu en bætir EKKI við neinum eignum í viðhaldsáætluninni.</span><span class="sxs-lookup"><span data-stu-id="00f11-120">In that case, you create a maintenance plan and select the specific functional location, but you do NOT add any assets in the maintenance plan.</span></span> <span data-ttu-id="00f11-121">Niðurstaðan er sú að þegar þú áætlar þá viðhaldsáætlun verða línur um viðhaldsskema stofnaðar fyrir allar eignir sem tengjast virkri staðsetningu á þeim tíma.</span><span class="sxs-lookup"><span data-stu-id="00f11-121">The result is that when you schedule that maintenance plan, maintenance schedule lines will be created for all the assets related to the functional location at that time.</span></span>

- <span data-ttu-id="00f11-122">Ef þú gerir breytingar á eignategundum, framleiðendum og tegundum í **Gerðir eigna** hafa þessar breytingar aðeins áhrif á nýjar eignir sem nota uppfærðu eignategundina.</span><span class="sxs-lookup"><span data-stu-id="00f11-122">If you make changes to asset types, manufacturers and models in **Asset types**, those changes only affect new assets that use the updated asset type.</span></span> <span data-ttu-id="00f11-123">Lestu meira um uppsetningargerð eigna í [Gerðir eigna](../setup-for-objects/object-types.md).</span><span class="sxs-lookup"><span data-stu-id="00f11-123">Read more about asset type setup in [Asset types](../setup-for-objects/object-types.md).</span></span>  

5. <span data-ttu-id="00f11-124">Smelltu á **Í lagi** til að hefja myndun á viðhaldsskemafærslum á eignum.</span><span class="sxs-lookup"><span data-stu-id="00f11-124">Click **OK** to start the generation of maintenance schedule entries on assets.</span></span> <span data-ttu-id="00f11-125">Myndaðar færslur verða sýndar á listasíðunni **Öll viðhaldsskemu**.</span><span class="sxs-lookup"><span data-stu-id="00f11-125">The generated entries will be shown in the **All maintenance schedule** list page.</span></span> <span data-ttu-id="00f11-126">Eftirfarandi mynd sýnir dæmi um gluggann **Tímasetja viðhaldsáætlanir**.</span><span class="sxs-lookup"><span data-stu-id="00f11-126">The following illustration shows an example of the **Schedule maintenance plans** dialog.</span></span>

![Mynd 1](media/09-preventive-maintenance.png)

- <span data-ttu-id="00f11-128">Í glugganum **Skipuleggja viðhaldsáætlanir** er hægt að setja upp runuvinnslur á flýtiflipanum **Keyra í bakgrunni** til að mynda sjálfkrafa dagatalsfærslur með reglulegu millibili.</span><span class="sxs-lookup"><span data-stu-id="00f11-128">In the **Schedule maintenance plans** dialog, you can set up batch jobs on the **Run in the background** FastTab to automatically generate calendar entries at regular intervals.</span></span>  
- <span data-ttu-id="00f11-129">Þegar þú áætlar fyrirbyggjandi viðhald verða viðhaldsskemalínur með áætluðum upphafsdegi og tíma sem er á undan dagsetningu og tíma kerfisins ekki búin til.</span><span class="sxs-lookup"><span data-stu-id="00f11-129">When you schedule preventive maintenance, maintenance schedule lines with expected start date and time earlier than the system date and time will not be created.</span></span>  

<span data-ttu-id="00f11-130">Myndin hér að neðan gefur myndræna mynd af tímabyggðum útreikningi á viðhaldsáætlun.</span><span class="sxs-lookup"><span data-stu-id="00f11-130">The figure below provides a graphic illustration of a time-based maintenance plan calculation.</span></span>  

![Mynd 2](media/10-preventive-maintenance.jpg)

<span data-ttu-id="00f11-132">Varðandi teljarabyggðar viðhaldsáætlanir: Á myndunum hér að neðan eru sýndar tvær mismunandi teljaraskráningarlotur.</span><span class="sxs-lookup"><span data-stu-id="00f11-132">Regarding counter-based maintenance plans: In the figures below, two different counter registration cycles are shown.</span></span> <span data-ttu-id="00f11-133">Þær eru byggðar á viðhaldsáætlun sem sett var upp fyrir eignina „V0001“ og búist við að eignin (bíll) gangi u.þ.b. 2.000 km í hverjum mánuði.</span><span class="sxs-lookup"><span data-stu-id="00f11-133">They are based on a maintenance plan set up for asset "V0001", expecting the asset (a car) to run approx. 2,000 km every month.</span></span>

<span data-ttu-id="00f11-134">Í fyrra dæminu næst ekki 2.000 km sem búist er við í hverjum mánuði.</span><span class="sxs-lookup"><span data-stu-id="00f11-134">In the first example, the expected 2,000 km are not reached every month.</span></span> <span data-ttu-id="00f11-135">Samkvæmt teljarabyggðu viðhaldsáætluninni er þröskuldurinn 2.000 km, sem þýðir að þegar þú keyrir tímasetningu viðhaldsáætlunar ætti að búa til viðhaldsskemalínu í hvert skipti sem 2.000 kílómetra þröskuldinum er náð.</span><span class="sxs-lookup"><span data-stu-id="00f11-135">According to the counter-based maintenance plan, the threshold is 2,000 km, meaning when you run a maintenance plan scheduling, a maintenance schedule line should be created each time the 2,000-kilometer threshold is reached.</span></span> <span data-ttu-id="00f11-136">Í dæmi 1 eru 4 skráningarlínur en 2.000 kílómetra þröskuldinum er aðeins náð einu sinni.</span><span class="sxs-lookup"><span data-stu-id="00f11-136">In example 1, there are 4 registration lines, but the 2,000-kilometer threshold is only reached once.</span></span> <span data-ttu-id="00f11-137">Þetta þýðir að þegar þú keyrir áætlun um viðhaldsáætlun fyrir þessa eign, til dæmis í 3 mánaða tímabil, verður aðeins ein viðhaldsskemalína búin til.</span><span class="sxs-lookup"><span data-stu-id="00f11-137">This means that when you run schedule maintenance plans this asset, for example for a 3-month period, only one maintenance schedule line will be created.</span></span>

<span data-ttu-id="00f11-138">Í næstu mynd eru 2.000 km eða meira skráðir í hverjum mánuði.</span><span class="sxs-lookup"><span data-stu-id="00f11-138">In the next figure, 2,000 km or more are registered every month.</span></span> <span data-ttu-id="00f11-139">Þess vegna yrðu búnar til þrjár viðhaldslínur ef þú áætlar viðhaldsáætlanir fyrir þessa eign í 3 mánuði.</span><span class="sxs-lookup"><span data-stu-id="00f11-139">Therefore, three maintenance lines would be created if you schedule maintenance plans for this asset for a 3-month period.</span></span> 

<span data-ttu-id="00f11-140">Dæmin sem lýst er hér sýna að allar gagnaskráningar sem gerðar hafa verið á eign sýna þróun sem lýsir sliti á eigninni.</span><span class="sxs-lookup"><span data-stu-id="00f11-140">The examples described here show that all counter registrations made on an asset show a trend describing wear and tear on the asset.</span></span> <span data-ttu-id="00f11-141">Sú þróun er notuð sem útreikningsgrundvöllur þegar áætlun um viðhaldsáætlun er gerð.</span><span class="sxs-lookup"><span data-stu-id="00f11-141">That trend is used as calculation basis at the time of maintenance plan scheduling.</span></span>

![Mynd 3](media/11-preventive-maintenance.png)

![Mynd 4](media/12-preventive-maintenance.png)

