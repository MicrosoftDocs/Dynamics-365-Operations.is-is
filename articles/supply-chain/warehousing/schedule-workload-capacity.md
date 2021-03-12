---
title: Tímasetja afkastagetu vinnuálags
description: Í þessu efnisatriði er útskýrt hvernig á að setja upp og raða vinnuálagsgetu starfsfólks í vöruhúsi eða fyrir heilt vöruhús.
author: MarkusFogelberg
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSWorkloadCapacity
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8db243949b2aeee0a8263276234d439652905449
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965578"
---
# <a name="schedule-workload-capacity"></a><span data-ttu-id="ea0bd-103">Tímasetja afkastagetu vinnuálags</span><span class="sxs-lookup"><span data-stu-id="ea0bd-103">Schedule workload capacity</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ea0bd-104">Hægt er að spá fyrir um vinnuálagsgetu fyrir vöruhús og einnig er hægt að spá fyrir um núverandi og framtíðarvinnuálag fyrir starfsfólkið í einstökum vöruhúsum.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-104">You can schedule workload capacity for warehouses, and you can also project the current and future workloads for the workers in individual warehouses.</span></span> <span data-ttu-id="ea0bd-105">Hægt er að spá fyrir um vinnuálag fyrir allt vöruhúsið eða spá fyrir um vinnuálagið aðskilið fyrir vinnuálag bæði á innleið og útleið.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-105">You can project the workload for the whole warehouse, or you can project the workload separately for incoming and outgoing workloads.</span></span>

<span data-ttu-id="ea0bd-106">Til að spá fyrir um vinnuálagsframleiðslu fyrir valin vöruhús, verða gögn aðalröðunar að vera tiltæk fyrir þessi vöruhús.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-106">To project workload output for selected warehouses, master scheduling data must be available for those warehouses.</span></span> <span data-ttu-id="ea0bd-107">Fyrir frekari upplýsingar, sjá [Yfirlit yfir aðaláætlanir](../master-planning/master-plans.md).</span><span class="sxs-lookup"><span data-stu-id="ea0bd-107">For more information, see [Master plans overview](../master-planning/master-plans.md).</span></span>

## <a name="schedule-and-view-workloads-for-a-warehouse"></a><span data-ttu-id="ea0bd-108">Raða og skoða vinnuálag fyrir vöruhús</span><span class="sxs-lookup"><span data-stu-id="ea0bd-108">Schedule and view workloads for a warehouse</span></span>

<span data-ttu-id="ea0bd-109">Til að raða vinnuálagsgetu fyrir vöruhús er stofnuð uppsetning vinnuálags fyrir eitt eða fleiri vöruhús og uppsetningin svo tengd við aðaláætlunina.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-109">To schedule workload capacity for a warehouse, you create a workload setup for one or more warehouses, and then associate the workload setup with a master plan.</span></span> <span data-ttu-id="ea0bd-110">Í uppsetningu vinnuálagsgetu geturðu skilgreint mörk fyrir þyngd eða rúmmál fyrir færslur á inn- og útleið.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-110">In the workload capacity setup, you can define limits for the weight or volume for incoming and outgoing transactions.</span></span> <span data-ttu-id="ea0bd-111">Þú getur einnig búið til fleiri en eina uppsetningu fyrir hvert vöruhús og síðan tengt uppsetninguna við einstakar aðaláætlanir.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-111">You can also create more than one setup for each warehouse and then associate the setup with individual master plans.</span></span> <span data-ttu-id="ea0bd-112">Til dæmis gætirðu notað þessa aðferð til að mæta árstíðabundnum breytingum á vinnuafli.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-112">For example, you might use this approach to accommodate seasonal changes in the workforce.</span></span>

<span data-ttu-id="ea0bd-113">Ef starfsfólk í vöruhúsi vinnur með færslur fyrir vinnuálag bæði á inn- og útleið getur þú stillt uppsetningu á afkastagetu vöruhúss þannig að vinnuálaginu er varpað í sameiginlegt yfirlit.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-113">If the workers for a warehouse work with transactions for both incoming and outgoing workloads, you can configure the warehouse capacity setup so that the workload is projected in a combined view.</span></span>

<span data-ttu-id="ea0bd-114">Til að tímasetja og skoða vinnuálag fyrir vöruhús verður þú að ljúka eftirfarandi verkum:</span><span class="sxs-lookup"><span data-stu-id="ea0bd-114">To schedule and view workloads for warehouses, you must complete the following tasks:</span></span>

1. <span data-ttu-id="ea0bd-115">Stofna uppsetningu á afkastagetu vinnuálags og skilgreina mörk afkastagetu vinnuálags fyrir eitt eða fleiri vöruhús.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-115">Create a workload capacity setup and define workload capacity limits for one or more warehouses.</span></span>
2. <span data-ttu-id="ea0bd-116">Tengja uppsetningu á afkastagetu vinnuálags við aðaláætlun til að búa til áætlun vinnuálags og tilgreina hversu lengi þessar áætlanir eiga við.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-116">Associate the workload capacity setup with a master plan to create workload projections and specify how long those projections will apply.</span></span>

### <a name="create-a-workload-capacity-setup-for-a-warehouse"></a><span data-ttu-id="ea0bd-117">Búa til uppsetningu á afkastagetu vinnuálags fyrir vöruhús</span><span class="sxs-lookup"><span data-stu-id="ea0bd-117">Create a workload capacity setup for a warehouse</span></span>

1. <span data-ttu-id="ea0bd-118">Veldu **Birgðastjórnun** \> **Uppsetning** \> **Vöktun vöruhúss** \> **Afkastageta vinnuálags**.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-118">Select **Inventory management** \> **Setup** \> **Warehouse monitoring** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="ea0bd-119">Í aðgerðarglugganum skal velja **Nýtt** til að búa til uppsetningu á afkastagetu vinnuálags.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-119">On the Action Pane, select **New** to create a workload capacity setup.</span></span>
3. <span data-ttu-id="ea0bd-120">Á flýtiflipanum **Vöruhús** skal velja **Nýtt** og slá síðan inn gildi á línunni til að tengja vöruhúsi uppsetningu á afkastagetu vinnuálags.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-120">On the **Warehouses** FastTab, select **New**, and then enter values on the line to associate a warehouse with the workload capacity setup.</span></span>
4. <span data-ttu-id="ea0bd-121">Veldu gátreitinn **Sameinað vinnuálag fyrir inn- og útleið** ef skýrslan **Afkastageta vinnuálags** skyldi sýna heildarvinnuálag fyrir færslur á inn- og útleið í einu yfirliti.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-121">Select the **Combined inbound and outbound workload** check box if the **Workload capacity** report should show the total workload for incoming and outgoing transactions in one view.</span></span>
5. <span data-ttu-id="ea0bd-122">Á flýtiflipanum **Færslugerðir** skal velja gerðir af færslum á inn- og útleið sem mörk vinnuálags eiga við um.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-122">On the **Transaction types** FastTab, select the types of incoming and outgoing transactions that the workload limits will apply to.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ea0bd-123">Þú verður að velja að minnsta kosti eina færslugerð fyrir bæði vinnuálag á inn- og útleið.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-123">You must select at least one transaction type for both the incoming workload and the outgoing workload.</span></span>

#### <a name="define-limits-for-volume-or-weight"></a><span data-ttu-id="ea0bd-124">Skilgreina mörk fyrir rúmmál eða þyngd</span><span class="sxs-lookup"><span data-stu-id="ea0bd-124">Define limits for volume or weight</span></span>

<span data-ttu-id="ea0bd-125">Þú getur sett upp mörk fyrir rúmmál eða þyngd, fer eftir takmörkuninni sem á við um mannafla vöruhússins.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-125">You can set up limits for volume or weight, depending on the limitation that is relevant for the warehouse workforce.</span></span> <span data-ttu-id="ea0bd-126">Mörkin sem þú tilgreinir eru tekin með í áætlun á afkastagetu vinnuálags sem hægt er að skoða í skýrslunni **Afkastageta vinnuálags**.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-126">The limits that you specify are included in the workload capacity projection that you can view on the **Workload capacity** report.</span></span>

<span data-ttu-id="ea0bd-127">Til að spá fyrir um upplýsingar varðandi rúmmál og þyngd á vörum, verður að tilgreina staðalrúmmál og þyngd á einni birgðavöru fyrir allar afurðir.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-127">To project information about volume and weight for items, the standard volume of one inventory item and the weight of one inventory item must be specified for all products.</span></span> <span data-ttu-id="ea0bd-128">Nauðsynlegir reitir eru í boði í eftirfarandi reitaflokkum á flýtiflipanum **Stjórna birgðum** á síðunni **Upplýsingar um losaðar afurðir**:</span><span class="sxs-lookup"><span data-stu-id="ea0bd-128">The fields that are required are available in the following field groups on the **Manage inventory** FastTab of the **Released product details** page:</span></span>

- <span data-ttu-id="ea0bd-129">Afgreiðsla</span><span class="sxs-lookup"><span data-stu-id="ea0bd-129">Handling</span></span>
- <span data-ttu-id="ea0bd-130">Efnislegar víddir</span><span class="sxs-lookup"><span data-stu-id="ea0bd-130">Physical dimensions</span></span>
- <span data-ttu-id="ea0bd-131">Vægi mælinga</span><span class="sxs-lookup"><span data-stu-id="ea0bd-131">Weight measurements</span></span>

<span data-ttu-id="ea0bd-132">Ef þessar upplýsingar eru ekki tilgreindar á réttan hátt, færðu skilaboð þegar þú býrð til skýrsluna **Afkastageta vinnuálags**.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-132">If this information isn't specified correctly, you receive a message when you generate the **Workload capacity** report.</span></span> <span data-ttu-id="ea0bd-133">Frá skýrslunni er hægt að bora niður til að bera kennsl á upplýsingar sem vantar sem þarf til að geta spáð fyrir um framtíðarvinnuálag.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-133">From the report, you can then drill down to identify the missing information that is required in order to project the future workload.</span></span>

### <a name="associate-a-workload-capacity-setup-with-a-master-plan"></a><span data-ttu-id="ea0bd-134">Tengja uppsetningu á afkastagetu vinnuálags við aðaláætlun</span><span class="sxs-lookup"><span data-stu-id="ea0bd-134">Associate a workload capacity setup with a master plan</span></span>

1. <span data-ttu-id="ea0bd-135">Veldu **Birgðastjórnun** \> **Reglubundin** \> **Raða vinnuálagi**.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-135">Select **Inventory management** \> **Periodic** \> **Schedule workload**.</span></span>
2. <span data-ttu-id="ea0bd-136">Í reitnum **Aðaláætlun** skal velja aðaláætlun til að nota fyrir áætlanir um vinnuálag.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-136">In the **Master plan** field, select the master plan to use for workload projections.</span></span>
3. <span data-ttu-id="ea0bd-137">Í reitnum **Fjöldi daga** skal tilgreina fjölda daga sem áætlun vinnuálags nær yfir.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-137">In the **Number of days** field, specify the number of days that the workload projection covers.</span></span>
4. <span data-ttu-id="ea0bd-138">Í reitnum **Vinnuálag** skal velja uppsetningu vinnuálags sem tengja á við aðaláætlun.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-138">In the **Workload** field, select the workload setup to associate with the master plan.</span></span>

### <a name="view-workload-capacity"></a><span data-ttu-id="ea0bd-139">Skoða afkastagetu vinnuálags</span><span class="sxs-lookup"><span data-stu-id="ea0bd-139">View workload capacity</span></span>

1. <span data-ttu-id="ea0bd-140">Veldu **Birgðastjórnun** \> **Fyrirspurnir og skýrslur** \> **Efnislegar birgðarskýrslur** \> **Afkastageta vinnuálags**.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-140">Select **Inventory management** \> **Inquiries and reports** \> **Physical inventory reports** \> **Workload capacity**.</span></span>
2. <span data-ttu-id="ea0bd-141">Í reitnum **Fjöldi dálka** skal tilgreina fjölda dálka sem birta á í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-141">In the **Number of columns** field, specify the number of columns to show on the report.</span></span>
3. <span data-ttu-id="ea0bd-142">Í reitnum **Gerð pöntunar** skal velja **Áætlað og staðfest**, **Áætlað** eða **Staðfest** til að tilgreina gerð pantana sem á að spá fyrir í skýrslunni.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-142">In the **Order type** field, select **Planned and confirmed**, **Planned**, or **Confirmed** to indicate the type of orders to project on the report.</span></span>
4. <span data-ttu-id="ea0bd-143">Í reitnum **Álagsgerðir** skal velja álagsgerð til að tilgreina hvort spá ætti fyrir um afkastagetu vinnuálags fyrir rúmmál og þyngd.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-143">In the **Load type** field, select a load type to specify whether the workload capacity should be projected for volume or weight.</span></span>
5. <span data-ttu-id="ea0bd-144">Í reitnum **Afkastageta vinnuálags** skal velja uppsetningu á afkastagetu vinnuálags.</span><span class="sxs-lookup"><span data-stu-id="ea0bd-144">In the **Workload capacity** field, select a workload capacity setup.</span></span>
