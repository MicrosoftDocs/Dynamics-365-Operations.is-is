---
title: Lífsferilsstöður viðhaldsbeiðni
description: Þetta efnisatriði lýsir því hvernig á að setja upp líftímastöður viðhaldsbeiðna í eignastjórnun.
author: josaw1
manager: tfehr
ms.date: 07/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9d1e4412af0619b57467b5bcba75ea7259604d1d
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209008"
---
# <a name="maintenance-request-lifecycle-states"></a><span data-ttu-id="e09b4-103">Lífsferilsstöður viðhaldsbeiðni</span><span class="sxs-lookup"><span data-stu-id="e09b4-103">Maintenance request lifecycle states</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="e09b4-104">Líftímastöður viðhaldsbeiðna skilgreinir stigin sem beiðni getur farið í gegnum.</span><span class="sxs-lookup"><span data-stu-id="e09b4-104">Maintenance request lifecycle states define the stages that a request can go through.</span></span> <span data-ttu-id="e09b4-105">Sem dæmi má nefna **Stofnað**, **Virkur**, og **Kláraði**.</span><span class="sxs-lookup"><span data-stu-id="e09b4-105">Examples include **Created**, **Active**, and **Ended**.</span></span> <span data-ttu-id="e09b4-106">Þegar viðhaldsbeiðni er breytt í verkbeiðni skal uppfæra ástand líftíma viðhaldsbeiðninnar til **Kláraði** eða **Lokað** til að gefa til kynna að viðhaldsbeiðnin sé ekki lengur virk.</span><span class="sxs-lookup"><span data-stu-id="e09b4-106">When a maintenance request is converted to a work order, the maintenance request lifecycle state should be updated to **Ended** or **Closed** to indicate that the maintenance request is no longer active.</span></span> <span data-ttu-id="e09b4-107">Á listasíðunni **Allar viðhaldsbeiðnir** er hægt að skoða allar viðhaldsbeiðnir, óháð líftímastöðu þeirra.</span><span class="sxs-lookup"><span data-stu-id="e09b4-107">On the **All maintenance requests** list page, you can view all maintenance requests, regardless of their lifecycle state.</span></span>

## <a name="set-up-maintenance-request-lifecycle-states"></a><span data-ttu-id="e09b4-108">Setja upp líftímastöður viðhaldsbeiðni</span><span class="sxs-lookup"><span data-stu-id="e09b4-108">Set up maintenance request lifecycle states</span></span>

1. <span data-ttu-id="e09b4-109">Veldu **Eignastýring** \> **Uppsetning** \> **Viðhaldsbeiðnir** \> **Líftímastöður**.</span><span class="sxs-lookup"><span data-stu-id="e09b4-109">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle states**.</span></span>
2. <span data-ttu-id="e09b4-110">Veldu **Nýr** til að stofna líftímastöðu viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="e09b4-110">Select **New** to create a maintenance request lifecycle state.</span></span>
3. <span data-ttu-id="e09b4-111">Í reitinn **Líftímastöðu** slærðu inn kenni líftímastöðunnar.</span><span class="sxs-lookup"><span data-stu-id="e09b4-111">In the **Lifecycle state** field, enter an ID for the lifecycle state.</span></span>
4. <span data-ttu-id="e09b4-112">Færið inn lýsandi nafn í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="e09b4-112">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="e09b4-113">Á flýtiflipanum **Upplýsingar** sýnir reiturinn **Líftímalíkön** fjölda líftímalíkana viðhaldsbeiðna sem nota þessa líftímastöðu.</span><span class="sxs-lookup"><span data-stu-id="e09b4-113">On the **Details** FastTab, the **Lifecycle models** field shows the number of maintenance request lifecycle models that use this lifecycle state.</span></span>

5. <span data-ttu-id="e09b4-114">Á flýtiflipanum **Almennt**, stilltu **Virkur** kostur á **Já** ef viðhaldsbeiðni ætti að vera virk meðan hún er í þessari líftímastöðu.</span><span class="sxs-lookup"><span data-stu-id="e09b4-114">On the **General** FastTab, set the **Active** option to **Yes** if a maintenance request should be active while it's in this lifecycle state.</span></span>
6. <span data-ttu-id="e09b4-115">Stilltu valkostinn **Setja raunverulegan endi** á **Já** ef sjálfkrafa ætti að slá inn raunverulegan lokadag og tíma í viðhaldsbeiðni sem er í þessu líftímastöðu.</span><span class="sxs-lookup"><span data-stu-id="e09b4-115">Set he **Set actual end** option to **Yes** if an actual end date and time should automatically be entered on a maintenance request that is in this lifecycle state.</span></span>
7. <span data-ttu-id="e09b4-116">Stilltu valkostinn **Stofna verkbeiðni** á **Já** ef hægt er að búa til verkbeiðni út frá viðhaldsbeiðni sem er í þessu líftíma ástand.</span><span class="sxs-lookup"><span data-stu-id="e09b4-116">Set the **Create work order** option to **Yes** if a work order can be created from a maintenance request that is in this lifecycle state.</span></span>
8. <span data-ttu-id="e09b4-117">Stilltu **Eyða** kostur á **Já** ef hægt er að eyða viðhaldsbeiðni meðan hún er í þessu líftíma ástand.</span><span class="sxs-lookup"><span data-stu-id="e09b4-117">Set the **Delete** option to **Yes** if a maintenance request can be deleted while it's in this lifecycle state.</span></span>
9. <span data-ttu-id="e09b4-118">Á flýtiflipanum **Uppfæra** eru valkostirnir **Á innleið** og **Á útleið** í hlutanum **Eignir** eru viðeigandi ef þú notar Depot Repair.cSetjið viðeigandi valkost til **Já** ef sjálfstætt líftíma eigna sem eru valdar í viðhaldsbeiðni ætti sjálfkrafa að uppfæra í **Á innleið** eða **Á útleið** þegar líftíma viðhaldsbeiðni vegna viðhaldsbeiðninnar er stillt á **Á innleið** eða **Á útleið**.</span><span class="sxs-lookup"><span data-stu-id="e09b4-118">On the **Update** FastTab, the **Inbound** and **Outbound** options in the **Asset** section are relevant if you use depot repair.cSet the appropriate option to **Yes** if the asset lifecycle state of assets that are selected on a maintenance request should automatically be updated to **Inbound** or **Outbound** when the maintenance request lifecycle state of that maintenance request is set to **Inbound** or **Outbound**.</span></span>

<span data-ttu-id="e09b4-119">Eftirfarandi mynd sýnir dæmi um síðuna **Líftímastöður viðhaldsbeiðna**.</span><span class="sxs-lookup"><span data-stu-id="e09b4-119">The follow illustration shows an example of the **Maintenance request lifecycle states** page.</span></span>

![Síðan Lífsferilsstöður viðhaldsbeiðni](media/02-setup-for-requests.png)

> [!NOTE]
> <span data-ttu-id="e09b4-121">Líftímastöður viðhaldsbeiðna, líftímastöðuhópar og tegundir eru tengdar og notaðar á sama hátt og líftímastöður verkbeiðni, líftímastöðuhópar og tegundir.</span><span class="sxs-lookup"><span data-stu-id="e09b4-121">Maintenance request lifecycle states, lifecycle state groups, and types are related to, and used in the same way as, work order lifecycle states, lifecycle state groups, and types.</span></span> 

## <a name="set-up-maintenance-request-lifecycle-models"></a><span data-ttu-id="e09b4-122">Setja upp líftímalíkön viðhaldsbeiðni</span><span class="sxs-lookup"><span data-stu-id="e09b4-122">Set up maintenance request lifecycle models</span></span>

<span data-ttu-id="e09b4-123">Eftir að þú ert búinn að búa til lífsferilstig sem nauðsynleg eru fyrir viðhaldsbeiðnir þínar er hægt að skipta þeim í líftíma hópa eða líftíma líkana.</span><span class="sxs-lookup"><span data-stu-id="e09b4-123">After you've created the lifecycle states that are required for your maintenance requests, they can be divided into lifecycle state groups, or lifecycle models.</span></span> <span data-ttu-id="e09b4-124">Lífsferilslíkön viðhaldsbeiðna eru notuð til að búa til flæði sem hægt er að nota fyrir mismunandi gerðir af viðhaldsbeiðnum.</span><span class="sxs-lookup"><span data-stu-id="e09b4-124">Maintenance request lifecycle models are used to create the flow that can be used for different types of maintenance requests.</span></span> <span data-ttu-id="e09b4-125">Að lágmarki ætti að búa til eitt staðlað líftímalíkan viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="e09b4-125">At a minimum, one standard maintenance request lifecycle model should be created.</span></span>

1. <span data-ttu-id="e09b4-126">Veldu **Eignastýring** \> **Uppsetning** \> **Viðhaldsbeiðnir** \> **Líftímalíkön**.</span><span class="sxs-lookup"><span data-stu-id="e09b4-126">Select **Asset management** \> **Setup** \> **Maintenance requests** \> **Lifecycle models**.</span></span>
2. <span data-ttu-id="e09b4-127">Veldu **Nýr** til að stofna líftímalíkan viðhaldsbeiðni.</span><span class="sxs-lookup"><span data-stu-id="e09b4-127">Select **New** to create a maintenance request lifecycle model.</span></span>
3. <span data-ttu-id="e09b4-128">Í **Líftímalíkan** reitinn, sláðu inn kenni líftímalíkansins.</span><span class="sxs-lookup"><span data-stu-id="e09b4-128">In the **Lifecycle model** field, enter an ID for the lifecycle model.</span></span>
4. <span data-ttu-id="e09b4-129">Færið inn lýsandi nafn í reitinn **Heiti**.</span><span class="sxs-lookup"><span data-stu-id="e09b4-129">In the **Name** field, enter a name.</span></span>

    <span data-ttu-id="e09b4-130">Á flýtiflipanum **Upplýsingar** sýnir **Líftímastöður** fjölda líftímastaða eigna sem eru valin í þessu líftímalíkani eigna.</span><span class="sxs-lookup"><span data-stu-id="e09b4-130">On the **Details** FastTab, the **Lifecycle states** shows the number of lifecycle states that are selected in this lifecycle model.</span></span> <span data-ttu-id="e09b4-131">Reiturinn **Gerðir viðhaldsbeiðna** sýnir fjölda gerða viðhaldsbeiðna sem nota líftímalíkanið.</span><span class="sxs-lookup"><span data-stu-id="e09b4-131">The **Maintenance request types** field shows the number of maintenance request types that use this lifecycle model.</span></span>

5. <span data-ttu-id="e09b4-132">Á flýtiflipanum **Líftímastöður** velurðu þær líftímastöður sem ætti að vera með í líftímalíkani:</span><span class="sxs-lookup"><span data-stu-id="e09b4-132">On the **Lifecycle states** FastTab, select the lifecycle states that should be included in the lifecycle model:</span></span>

    - <span data-ttu-id="e09b4-133">Til að hafa líftímastöðu með fyrir líftímalíkanið skaltu velja það í **Eftirstandandi líftímastöður** kafla og veldu síðan hægri örvarhnappinn ![Hægri ör](media/03-setup-for-requests.png) til að færa það til **Valdar líftímastöður**.</span><span class="sxs-lookup"><span data-stu-id="e09b4-133">To include a lifecycle state in the lifecycle model, select it in the **Lifecycle states remaining** section, and then select the right arrow button ![Right arrow](media/03-setup-for-requests.png) to move it to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="e09b4-134">Til að hafa allar tiltækar líftímastöður með fyrir líftímalíkanið velurðu hnappinn **Velja allar tiltækar stöður** ![Velja allar tiltækar stöður](media/04-setup-for-requests.png).</span><span class="sxs-lookup"><span data-stu-id="e09b4-134">To include all the available lifecycle states in the lifecycle model, select the **Select all available states** button ![Select all available states](media/04-setup-for-requests.png).</span></span> <span data-ttu-id="e09b4-135">Allar líftímastöður eru fluttar í hlutann **Valdar líftímastöður**.</span><span class="sxs-lookup"><span data-stu-id="e09b4-135">All lifecycle states are moved to the **Lifecycle states selected** section.</span></span>
    - <span data-ttu-id="e09b4-136">Til að fjarlægja líftímastöðu úr líftímalíkani skaltu velja það í **Valdar líftímastöður** kafla og veldu síðan vinstri örvarhnappinn ![Vinstri ör](media/05-setup-for-requests.png) til að færa það til **Eftirstandandi líftímastöður**.</span><span class="sxs-lookup"><span data-stu-id="e09b4-136">To remove a lifecycle state from the lifecycle model, select it in the **Lifecycle states selected** section, and then select the left arrow button ![Left arrow](media/05-setup-for-requests.png) to move it to the **Lifecycle states remaining** section.</span></span>

6. <span data-ttu-id="e09b4-137">Á flýtiflipanum **Almennt**, reitirnir í **Uppfærslur** kaflinn skiptir máli ef þú notar viðgerð á geymslu.</span><span class="sxs-lookup"><span data-stu-id="e09b4-137">On the **General** FastTab, the fields in the **Updates** section are relevant if you use depot repair.</span></span>

    - <span data-ttu-id="e09b4-138">Í reitnum **Líftímastaða fyrir móttekna eign** skaltu velja ástand líftíma eigna að eignir sem eru valdar í viðhaldsbeiðni ættu sjálfkrafa að vera uppfærðar til þegar þær eru mótteknar til lagfæringar á geymslu.</span><span class="sxs-lookup"><span data-stu-id="e09b4-138">In the **Lifecycle state for asset received** field, select the asset lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are received for depot repair.</span></span>
    - <span data-ttu-id="e09b4-139">Í reitnum **Líftímastaða fyrir afhenta eign** skaltu velja ástand líftíma eigna að eignir sem eru valdar í viðhaldsbeiðni ættu sjálfkrafa að vera uppfærðar til þegar þeim er skilað eftir lagfæringu.</span><span class="sxs-lookup"><span data-stu-id="e09b4-139">In the **Lifecycle state for asset delivered** field, select the lifecycle state that assets that are selected on a maintenance request should automatically be updated to when they are returned after repair.</span></span>

<span data-ttu-id="e09b4-140">Eftirfarandi mynd sýnir dæmi um síðuna **Líftímalíkön viðhaldsbeiðna**.</span><span class="sxs-lookup"><span data-stu-id="e09b4-140">The following illustration shows an example of the **Maintenance request lifecycle models** page.</span></span>

![Síðan Líftímalíkön viðhaldsbeiðni](media/06-setup-for-requests.png)
