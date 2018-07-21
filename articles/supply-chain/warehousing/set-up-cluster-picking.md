---
title: Setja upp klasatiltekt
description: "Í þessu efnisatriði er því lýst hvernig á að setja upp klasatiltekt og hvernig á að nota vörustaðfestingu með klasatiltekt."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 52750321588d69483439873861682636c13a4936
ms.contentlocale: is-is
ms.lasthandoff: 07/21/2018

---

[!include[banner](../includes/banner.md)]

# <a name="set-up-cluster-picking"></a><span data-ttu-id="a7f37-103">Setja upp klasatiltekt</span><span class="sxs-lookup"><span data-stu-id="a7f37-103">Set up cluster picking</span></span>

<span data-ttu-id="a7f37-104">Þetta efnisatriði lýsir því hvernig starfsmenn til að nota þeirra fartæki við tiltekt vinnu í klasa, þannig að þær hægt að taka vörur frá einum stað fyrir margar pantanir vinnu á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="a7f37-104">This topic describes how to enable workers to use their mobile devices to group picking work into clusters, so that they can pick items from a single location for multiple work orders at the same time.</span></span> <span data-ttu-id="a7f37-105">Þetta er kallað *klasatínslu*.</span><span class="sxs-lookup"><span data-stu-id="a7f37-105">This is called *cluster picking*.</span></span>

## <a name="about-cluster-picking"></a><span data-ttu-id="a7f37-106">Um klasatiltekt</span><span class="sxs-lookup"><span data-stu-id="a7f37-106">About cluster picking</span></span>

<span data-ttu-id="a7f37-107">Eftir að verkpantanir eru gefnar út á vöruhús getur starfsmaður notað farsímann til að úthluta pöntunum í klasa.</span><span class="sxs-lookup"><span data-stu-id="a7f37-107">After work orders are released to the warehouse, the worker can use a mobile device to assign the orders to a cluster.</span></span> <span data-ttu-id="a7f37-108">Klasa verður að skipuleggja tiltektarvinnu fyrir starfsmann.</span><span class="sxs-lookup"><span data-stu-id="a7f37-108">The cluster will organize the picking work for the worker.</span></span> <span data-ttu-id="a7f37-109">Vinna pöntun er tengdur við klasa, starfsmaður verður að nota klasa tiltektarlista til að framkvæma vinnu við tiltekt pöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="a7f37-109">When a work order is assigned to a cluster, the worker must use cluster picking to perform the picking work for the order.</span></span> <span data-ttu-id="a7f37-110">Starfsmaðurinn getur ekki notað annarri tiltektaraðferð.</span><span class="sxs-lookup"><span data-stu-id="a7f37-110">The worker cannot use other picking methods.</span></span> <span data-ttu-id="a7f37-111">Ef vinnu pöntun er úthlutað á klasa mistök, verður starfsmaðurinn skipta klasanum sem og síðan búðu það aftur.</span><span class="sxs-lookup"><span data-stu-id="a7f37-111">If a work order is assigned to a cluster by mistake, the worker must break the cluster and then re-create it.</span></span>

<span data-ttu-id="a7f37-112">Ef þörf krefur, getur starfsmaður látið klasa ganga til  annan starfsmann.</span><span class="sxs-lookup"><span data-stu-id="a7f37-112">If needed, a worker can pass a cluster to another worker.</span></span> <span data-ttu-id="a7f37-113">Þetta breytir stöðunni í klasa Skilað.</span><span class="sxs-lookup"><span data-stu-id="a7f37-113">This changes the cluster status to Passed.</span></span> <span data-ttu-id="a7f37-114">Þegar starfskraftur notar fartæki til að tilgreina að lokið er við tiltektar- og frágangsvinnu, verður að staðfesta sendinguna eða farminn í biðlara Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a7f37-114">When the worker uses a mobile device to indicate that the picking and put away work is completed, the shipment or load must be confirmed in the Dynamics 365 for Finance and Operations client.</span></span>

## <a name="set-up-cluster-picking"></a><span data-ttu-id="a7f37-115">Setja upp klasatiltekt</span><span class="sxs-lookup"><span data-stu-id="a7f37-115">Set up cluster picking</span></span>

<span data-ttu-id="a7f37-116">Til að virkja klasatínslu, verður að setja upp eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="a7f37-116">To enable cluster picking, you must set up the following:</span></span>

-   <span data-ttu-id="a7f37-117">**Klasaforstillingar** - Tilgreindu hvort á að sjálfkrafa búa til auðkenni klasa, fjölda stöðugilda til að nota, hvenær á að brjóta upp klasa, og hvernig á að raða og staðfesta tiltekt.</span><span class="sxs-lookup"><span data-stu-id="a7f37-117">**Cluster profiles** – Specify whether to automatically generate cluster IDs, the number of positions to use, when to break clusters, and how to sequence and verify the picking work.</span></span>

-   <span data-ttu-id="a7f37-118">**Vinnusniðmát** - Tilgreindu hvernig á að búa til tiltekt fyrir klasatiltekt.</span><span class="sxs-lookup"><span data-stu-id="a7f37-118">**Work templates** – Define how to create the picking work for cluster picking.</span></span>

-   <span data-ttu-id="a7f37-119">**Staðsetningarleiðbeiningar** - Tilgreindu hvar á að taka til vörur og hvar á að setja þær.</span><span class="sxs-lookup"><span data-stu-id="a7f37-119">**Location directives** – Specify where to pick items from, and where to put them.</span></span>

-   <span data-ttu-id="a7f37-120">**Valmyndaratriði fartækis** - Stilla valmyndaratriði fartækis til að nota fyrirliggjandi verk sem er stjórnað af klasatiltekt.</span><span class="sxs-lookup"><span data-stu-id="a7f37-120">**Mobile device menu items** – Configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="a7f37-121">Þú verður að bæta valmyndaratriði valmynd fartækis þannig að það birtist í fartækjum.</span><span class="sxs-lookup"><span data-stu-id="a7f37-121">You must then add the menu item to a mobile device menu so that it is displayed on mobile devices.</span></span>

-   <span data-ttu-id="a7f37-122">**Færibreytur vöruhúsakerfis** - Tilgreindu talnarunu til að nota ef þú vilt búa til auðkenni fyrir klasa.</span><span class="sxs-lookup"><span data-stu-id="a7f37-122">**Warehouse management parameters** – Specify the number sequence to use if you want to generate identifiers for clusters.</span></span>

## <a name="set-up-a-cluster-profile"></a><span data-ttu-id="a7f37-123">Setja upp klasaforstillingu</span><span class="sxs-lookup"><span data-stu-id="a7f37-123">Set up a cluster profile</span></span>

<span data-ttu-id="a7f37-124">Til að setja upp forstillingu sem klasa, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="a7f37-124">To set up a cluster profile, follow these steps:</span></span>

1.  <span data-ttu-id="a7f37-125">Smelltu á **Vöruhúsakerfi** \> **Uppsetning** \> **Fartæki** \> **Klasaforstillingar**.</span><span class="sxs-lookup"><span data-stu-id="a7f37-125">Click **Warehouse management** \> **Setup** \> **Mobile device** \> **Cluster profiles**.</span></span>

2.  <span data-ttu-id="a7f37-126">Smelltu á **Nýtt** til að stofna nýja forstillingu.</span><span class="sxs-lookup"><span data-stu-id="a7f37-126">Click **New** to create a new profile.</span></span>

3.  <span data-ttu-id="a7f37-127">Smelltu á **Stofna klasa** og, undir **Klasaröðun**, skal smella á **Nýtt** til að setja upp röðunarforsendur fyrir klasann.</span><span class="sxs-lookup"><span data-stu-id="a7f37-127">Click **Create cluster** and, under **Cluster sorting**, click **New** to set up the sorting criteria for the cluster.</span></span> <span data-ttu-id="a7f37-128">Röðunarforsendur að stýra röðinni sem starfsmaðurinn mun framkvæma tiltekt vinnu.</span><span class="sxs-lookup"><span data-stu-id="a7f37-128">The sorting criteria control the order in which the worker will perform the picking work.</span></span> <span data-ttu-id="a7f37-129">Hægt er að bæta við eins mörgum skilyrðum og þarf.</span><span class="sxs-lookup"><span data-stu-id="a7f37-129">You can add as many criteria as needed.</span></span>

4.  <span data-ttu-id="a7f37-130">Í reitnum **Númeraröð** skal slá inn númer til að skilgreina röðina sem unnið er úr röðunarforsendum.</span><span class="sxs-lookup"><span data-stu-id="a7f37-130">In the **Sequence number** field, enter a number to define the order in which the sorting criteria are processed.</span></span>

5.  <span data-ttu-id="a7f37-131">Í reitnum **Reitarheiti** velurðu reitinn sem mun ákvarða flokkun.</span><span class="sxs-lookup"><span data-stu-id="a7f37-131">In the **Field name** field, select the field that will determine the sorting.</span></span> <span data-ttu-id="a7f37-132">Til dæmis, ef þú velur **WMSLocationId** svæðinu vinnu verður raðað eftir staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="a7f37-132">For example, if you select the **WMSLocationId** field, the work will be sorted by location.</span></span>

6.  <span data-ttu-id="a7f37-133">Í reitnum **Röðun** skal velja einn af eftirfarandi valkostum.</span><span class="sxs-lookup"><span data-stu-id="a7f37-133">In the **Sorting** field, select one of the following options.</span></span>

| <span data-ttu-id="a7f37-134">**Valkostur**</span><span class="sxs-lookup"><span data-stu-id="a7f37-134">**Option**</span></span>     | <span data-ttu-id="a7f37-135">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="a7f37-135">**Description**</span></span>                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7f37-136">**Hækkandi**</span><span class="sxs-lookup"><span data-stu-id="a7f37-136">**Ascending**</span></span>  | <span data-ttu-id="a7f37-137">Tiltektarvinnu er raðað í hækkandi röð samkvæmt röðunarforsendunni.</span><span class="sxs-lookup"><span data-stu-id="a7f37-137">Picking work is sequenced in ascending order based on the sorting criteria.</span></span> <span data-ttu-id="a7f37-138">Til dæmis, ef nota á **WMSLocationId** eru svæði sem á að raða skilyrðum og Kenni skal staðsetningu 1, 2, 3 og 4, er verður að taka frá staðsetningu 4 fyrst.</span><span class="sxs-lookup"><span data-stu-id="a7f37-138">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 4 first.</span></span> |
| <span data-ttu-id="a7f37-139">**Í lækkandi röð**</span><span class="sxs-lookup"><span data-stu-id="a7f37-139">**Descending**</span></span> | <span data-ttu-id="a7f37-140">Tiltektarvinnu er raðað í lækkandi röð samkvæmt röðunarforsendunni.</span><span class="sxs-lookup"><span data-stu-id="a7f37-140">Picking work is sequenced in descending order based on the sorting criteria.</span></span> <span data-ttu-id="a7f37-141">Til dæmis, ef nota á **WMSLocationId** eru svæði sem á að raða skilyrðum og Kenni skal staðsetningu 1, 2, 3 og 4, er verður að taka frá staðsetningu 1 fyrst.</span><span class="sxs-lookup"><span data-stu-id="a7f37-141">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 1 first.</span></span> |

## <a name="item-confirmation"></a><span data-ttu-id="a7f37-142">Vörustaðfesting</span><span class="sxs-lookup"><span data-stu-id="a7f37-142">Item confirmation</span></span>

<span data-ttu-id="a7f37-143">Þegar klasatiltekt er notuð, er vörustaðfesting nauðsynleg svo hægt sé að staðfesta þær vörur sem bætt er við klasa.</span><span class="sxs-lookup"><span data-stu-id="a7f37-143">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="a7f37-144">Hægt er að staðfesta vörur í klasatiltekt á meðan klasatiltekt stendur yfir.</span><span class="sxs-lookup"><span data-stu-id="a7f37-144">You can verify items in cluster picking during the cluster picking process.</span></span> <span data-ttu-id="a7f37-145">Uppsetning byggist á strikamerkjauppsetningu vöru.</span><span class="sxs-lookup"><span data-stu-id="a7f37-145">The setup is based on the product bar code setup.</span></span>

### <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="a7f37-146">Setja upp vörustaðfestingu með klasatiltekt</span><span class="sxs-lookup"><span data-stu-id="a7f37-146">Set up item verification with cluster picking</span></span>

1.  <span data-ttu-id="a7f37-147">Í valmyndaratriði fartækis skal opna eyðublað uppsetningar fyrir vinnustaðfestingu: **Vöruhúsakerfi** \> **Vöruhúsakerfi** \> **Uppsetning** \> **Fartæki** \> **Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="a7f37-147">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** \> **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>

2.  <span data-ttu-id="a7f37-148">Opna **Uppsetning vinnustaðfestingar** í valmyndaratriði fartækis.</span><span class="sxs-lookup"><span data-stu-id="a7f37-148">From the mobile device menu item, open **Work confirmation setup**.</span></span> <span data-ttu-id="a7f37-149">Valkosturinn **Afurðarstaðfesting** leyfir þér að staðfesta hvert stykki af birgðum úr fartæki þegar það er skannað.</span><span class="sxs-lookup"><span data-stu-id="a7f37-149">The **Product confirmation** option allows you to verify each piece of inventory from the mobile device when scanned.</span></span>

