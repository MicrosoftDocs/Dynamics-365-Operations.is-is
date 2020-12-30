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
ms.openlocfilehash: f15b035c01801041d637a2d315d8a3ddcc9d6540
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413212"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="fa3de-103">Stofna netrás og skilgreina eigindi rásar</span><span class="sxs-lookup"><span data-stu-id="fa3de-103">Create online channel and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fa3de-104">Þetta ferli fer með þig í gegnum til að stofna nýja netrás og henni er bætt við stigveldi fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="fa3de-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="fa3de-105">Þú verður að Stofna stigveldi fyrirtækis áður en hægt er að stofna nýja netrás.</span><span class="sxs-lookup"><span data-stu-id="fa3de-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="fa3de-106">Þessi aðferð notar USRT sýnigögn fyrirtækisins.</span><span class="sxs-lookup"><span data-stu-id="fa3de-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="fa3de-107">Stofna nýjan rás á netinu</span><span class="sxs-lookup"><span data-stu-id="fa3de-107">Create a new online channel</span></span>
1. <span data-ttu-id="fa3de-108">Fara í Retail og Commerce > rásir > Netverslanir.</span><span class="sxs-lookup"><span data-stu-id="fa3de-108">Go to Retail and Commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="fa3de-109">Smellið á Nýtt.</span><span class="sxs-lookup"><span data-stu-id="fa3de-109">Click New.</span></span>
3. <span data-ttu-id="fa3de-110">Í reitinn Heiti skal slá inn gildi.</span><span class="sxs-lookup"><span data-stu-id="fa3de-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="fa3de-111">Sláðu inn eða veldu gildi í reitnum Vöruhús.</span><span class="sxs-lookup"><span data-stu-id="fa3de-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="fa3de-112">Veljið valkost í svæðinu tímabelti Verslunar.</span><span class="sxs-lookup"><span data-stu-id="fa3de-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="fa3de-113">Færa inn eða velja gildi í svæðinu Sjálfgefinn viðskiptavin.</span><span class="sxs-lookup"><span data-stu-id="fa3de-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="fa3de-114">Færa inn eða veljið gildi í aðsetursbók viðskiptavinar.</span><span class="sxs-lookup"><span data-stu-id="fa3de-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="fa3de-115">Færa inn eða velja gildi í reitnum greiðsluskilmálar.</span><span class="sxs-lookup"><span data-stu-id="fa3de-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="fa3de-116">Færa inn eða velja gildi í reitnum greiðsluaðferð.</span><span class="sxs-lookup"><span data-stu-id="fa3de-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="fa3de-117">Færa inn eða veljið gildi í reit fyrir forstillingu tilkynninga Tölvupósts.</span><span class="sxs-lookup"><span data-stu-id="fa3de-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="fa3de-118">Útvíkka hlutann fjárhagsvíddir.</span><span class="sxs-lookup"><span data-stu-id="fa3de-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="fa3de-119">Færa inn eða veljið gildi í svæðinu BusinessUnit.</span><span class="sxs-lookup"><span data-stu-id="fa3de-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="fa3de-120">Stilla gildi fyrir allar aðrar sjálfgefnar víddir svipaðan hátt.</span><span class="sxs-lookup"><span data-stu-id="fa3de-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="fa3de-121">Smellið á „Vista“.</span><span class="sxs-lookup"><span data-stu-id="fa3de-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="fa3de-122">Bæta við netrás í stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="fa3de-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="fa3de-123">Lokið síðunni.</span><span class="sxs-lookup"><span data-stu-id="fa3de-123">Close the page.</span></span>
2. <span data-ttu-id="fa3de-124">Fara á fyrirtækisstjórnun > Fyrirtæki > stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="fa3de-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="fa3de-125">Í listanum skal finna og velja þá skráningu sem óskað er eftir.</span><span class="sxs-lookup"><span data-stu-id="fa3de-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="fa3de-126">Smellið á Skoða.</span><span class="sxs-lookup"><span data-stu-id="fa3de-126">Click View.</span></span>
5. <span data-ttu-id="fa3de-127">Smellið á „Breyta“.</span><span class="sxs-lookup"><span data-stu-id="fa3de-127">Click Edit.</span></span>
    * <span data-ttu-id="fa3de-128">Hægt er að velja hvaða stigveldishnút undir sem óskað er að setja inn nýja leið.</span><span class="sxs-lookup"><span data-stu-id="fa3de-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="fa3de-129">Smellt er á Setja inn.</span><span class="sxs-lookup"><span data-stu-id="fa3de-129">Click Insert.</span></span>
7. <span data-ttu-id="fa3de-130">Smelltu á Commerce-rás.</span><span class="sxs-lookup"><span data-stu-id="fa3de-130">Click Commerce channel.</span></span>
8. <span data-ttu-id="fa3de-131">Smellt er á Í lagi.</span><span class="sxs-lookup"><span data-stu-id="fa3de-131">Click OK.</span></span>
9. <span data-ttu-id="fa3de-132">Smellt er á Birta til að opna felligluggann.</span><span class="sxs-lookup"><span data-stu-id="fa3de-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="fa3de-133">Færa inn dagsetningu og tíma í svæðinu gildisdagsetningu.</span><span class="sxs-lookup"><span data-stu-id="fa3de-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="fa3de-134">Smelltu á Birta.</span><span class="sxs-lookup"><span data-stu-id="fa3de-134">Click Publish.</span></span>

## <a name="configure-orders-for-near-real-time-notification"></a><span data-ttu-id="fa3de-135">Stilla pantanir fyrir tilkynningu nálægt rauntíma</span><span class="sxs-lookup"><span data-stu-id="fa3de-135">Configure orders for near real-time notification</span></span>
1. <span data-ttu-id="fa3de-136">Farið í Retail og Commerce > Uppsetning höfuðstöðva > Færibreytur > Commerce-færibreytur.</span><span class="sxs-lookup"><span data-stu-id="fa3de-136">Go to Retail and Commerce  > Headquarters setup > Parameters > Commerce parameters.</span></span>
2. <span data-ttu-id="fa3de-137">Stilla rauntímaþjónustu fyrir stofnun eCommerce pöntunar á „Já“.</span><span class="sxs-lookup"><span data-stu-id="fa3de-137">Set Use realtime service for eCommerce order creation to "Yes".</span></span>
3. <span data-ttu-id="fa3de-138">Keyra 1070 dreifingaráætlun til að samstilla breytingar við gagnagrunn rásar.</span><span class="sxs-lookup"><span data-stu-id="fa3de-138">Run the 1070 distribution schedule to sync changes to the channel database.</span></span> 


