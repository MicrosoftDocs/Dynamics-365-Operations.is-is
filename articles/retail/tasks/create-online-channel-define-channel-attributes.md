---
title: Stofna netrás og skilgreina eigindi rásar
description: Þetta ferli fer með þig í gegnum til að stofna nýja netrás og henni er bætt við stigveldi fyrirtækisins.
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4547731d7e3bc56b1ba5e0a35ff4746c6c0e9863
ms.sourcegitcommit: 901ec3b360303bb8b4d9a9dcfecc6d75d7f844a0
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/05/2019
ms.locfileid: "1618297"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="509f6-103">Stofna netrás og skilgreina eigindi rásar</span><span class="sxs-lookup"><span data-stu-id="509f6-103">Create online channel and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="509f6-104">Þetta ferli fer með þig í gegnum til að stofna nýja netrás og henni er bætt við stigveldi fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="509f6-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="509f6-105">Þú verður að Stofna stigveldi fyrirtækis áður en hægt er að stofna nýja netrás.</span><span class="sxs-lookup"><span data-stu-id="509f6-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="509f6-106">Þessi aðferð notar USRT sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="509f6-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="509f6-107">Stofna nýjan rás á netinu</span><span class="sxs-lookup"><span data-stu-id="509f6-107">Create a new online channel</span></span>
1. <span data-ttu-id="509f6-108">Fara í Smásölu og viðskipti > rásir > Netverslanir.</span><span class="sxs-lookup"><span data-stu-id="509f6-108">Go to Retail and commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="509f6-109">Smellið á „Nýtt“.</span><span class="sxs-lookup"><span data-stu-id="509f6-109">Click New.</span></span>
3. <span data-ttu-id="509f6-110">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="509f6-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="509f6-111">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="509f6-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="509f6-112">Veljið valkost í svæðinu tímabelti Verslunar.</span><span class="sxs-lookup"><span data-stu-id="509f6-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="509f6-113">Færa inn eða velja gildi í svæðinu Sjálfgefinn viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="509f6-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="509f6-114">Færa inn eða veljið gildi í aðsetursbók viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="509f6-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="509f6-115">Færa inn eða velja gildi í reitnum greiðsluskilmálar.</span><span class="sxs-lookup"><span data-stu-id="509f6-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="509f6-116">Færa inn eða velja gildi í reitnum greiðsluaðferð.</span><span class="sxs-lookup"><span data-stu-id="509f6-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="509f6-117">Færa inn eða veljið gildi í reit fyrir forstillingu tilkynninga Tölvupósts.</span><span class="sxs-lookup"><span data-stu-id="509f6-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="509f6-118">Útvíkka hlutann fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="509f6-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="509f6-119">Færa inn eða veljið gildi í svæðinu BusinessUnit.</span><span class="sxs-lookup"><span data-stu-id="509f6-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="509f6-120">Stilla gildi fyrir allar aðrar sjálfgefnar víddir svipaðan hátt.</span><span class="sxs-lookup"><span data-stu-id="509f6-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="509f6-121">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="509f6-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="509f6-122">Bæta við netrás í stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="509f6-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="509f6-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="509f6-123">Close the page.</span></span>
2. <span data-ttu-id="509f6-124">Fara á fyrirtækisstjórnun > Fyrirtæki > stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="509f6-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="509f6-125">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="509f6-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="509f6-126">Smellið á Skoða.</span><span class="sxs-lookup"><span data-stu-id="509f6-126">Click View.</span></span>
5. <span data-ttu-id="509f6-127">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="509f6-127">Click Edit.</span></span>
    * <span data-ttu-id="509f6-128">Hægt er að velja hvaða stigveldishnút undir sem óskað er að setja inn nýja leið.</span><span class="sxs-lookup"><span data-stu-id="509f6-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="509f6-129">Smellt er á Setja inn.</span><span class="sxs-lookup"><span data-stu-id="509f6-129">Click Insert.</span></span>
7. <span data-ttu-id="509f6-130">Smellt er á smásölurás.</span><span class="sxs-lookup"><span data-stu-id="509f6-130">Click Retail channel.</span></span>
8. <span data-ttu-id="509f6-131">Smellið á „Í lagi“.</span><span class="sxs-lookup"><span data-stu-id="509f6-131">Click OK.</span></span>
9. <span data-ttu-id="509f6-132">Smellt er á Birta til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="509f6-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="509f6-133">Færa inn dagsetningu og tíma í svæðinu gildisdagsetningu.</span><span class="sxs-lookup"><span data-stu-id="509f6-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="509f6-134">Smelltu á Birta.</span><span class="sxs-lookup"><span data-stu-id="509f6-134">Click Publish.</span></span>

## <a name="configure-orders-for-near-realtime-notification"></a><span data-ttu-id="509f6-135">Stilla pantanir fyrir tilkynningu nálægt rauntíma</span><span class="sxs-lookup"><span data-stu-id="509f6-135">Configure orders for near realtime notification</span></span>
1. <span data-ttu-id="509f6-136">Farið í Smásala > Uppsetning höfuðstöðva > Færibreytur > Smásölufæribreytur.</span><span class="sxs-lookup"><span data-stu-id="509f6-136">Go to Retail  > Headquarters setup > Parameters > Retail parameters.</span></span>
2. <span data-ttu-id="509f6-137">Stilla rauntímaþjónustu fyrir stofnun eCommerce pöntunar á „Já“.</span><span class="sxs-lookup"><span data-stu-id="509f6-137">Set Use realtime service for eCommerce order creation to "Yes".</span></span>
3. <span data-ttu-id="509f6-138">Keyra 1070 dreifingaráætlun til að samstilla breytingar við gagnagrunn rásar.</span><span class="sxs-lookup"><span data-stu-id="509f6-138">Run the 1070 distribution schedule to sync changes to the channel database.</span></span> 


