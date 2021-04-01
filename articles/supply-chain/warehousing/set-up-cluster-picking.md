---
title: Setja upp klasatiltekt
description: Í þessu efnisatriði er því lýst hvernig á að setja upp klasatiltekt og hvernig á að nota vörustaðfestingu með klasatiltekt.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm, WHSWorkCluster
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2b3df8cf5e63fe97925f17001e836a41c703dfc9
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/15/2021
ms.locfileid: "5239231"
---
# <a name="set-up-cluster-picking"></a><span data-ttu-id="3f7fc-103">Setja upp klasatiltekt</span><span class="sxs-lookup"><span data-stu-id="3f7fc-103">Set up cluster picking</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3f7fc-104">Þetta efnisatriði lýsir því hvernig starfsmenn til að nota þeirra fartæki við tiltekt vinnu í klasa, þannig að þær hægt að taka vörur frá einum stað fyrir margar pantanir vinnu á sama tíma.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-104">This topic describes how to enable workers to use their mobile devices to group picking work into clusters, so that they can pick items from a single location for multiple work orders at the same time.</span></span> <span data-ttu-id="3f7fc-105">Þetta er kallað *klasatínslu*.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-105">This is called *cluster picking*.</span></span>

## <a name="about-cluster-picking"></a><span data-ttu-id="3f7fc-106">Um klasatiltekt</span><span class="sxs-lookup"><span data-stu-id="3f7fc-106">About cluster picking</span></span>

<span data-ttu-id="3f7fc-107">Eftir að verkpantanir eru gefnar út á vöruhús getur starfsmaður notað farsímann til að úthluta pöntunum í klasa.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-107">After work orders are released to the warehouse, the worker can use a mobile device to assign the orders to a cluster.</span></span> <span data-ttu-id="3f7fc-108">Klasa verður að skipuleggja tiltektarvinnu fyrir starfsmann.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-108">The cluster will organize the picking work for the worker.</span></span> <span data-ttu-id="3f7fc-109">Vinna pöntun er tengdur við klasa, starfsmaður verður að nota klasa tiltektarlista til að framkvæma vinnu við tiltekt pöntunarinnar.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-109">When a work order is assigned to a cluster, the worker must use cluster picking to perform the picking work for the order.</span></span> <span data-ttu-id="3f7fc-110">Starfsmaðurinn getur ekki notað annarri tiltektaraðferð.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-110">The worker cannot use other picking methods.</span></span> <span data-ttu-id="3f7fc-111">Ef vinnu pöntun er úthlutað á klasa mistök, verður starfsmaðurinn skipta klasanum sem og síðan búðu það aftur.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-111">If a work order is assigned to a cluster by mistake, the worker must break the cluster and then re-create it.</span></span>

<span data-ttu-id="3f7fc-112">Ef þörf krefur, getur starfsmaður látið klasa ganga til annan starfsmann.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-112">If needed, a worker can pass a cluster to another worker.</span></span> <span data-ttu-id="3f7fc-113">Þetta breytir stöðunni í klasa Skilað.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-113">This changes the cluster status to Passed.</span></span> <span data-ttu-id="3f7fc-114">Þegar starfsmaður notar fartæki til að tilgreina að lokið er við tiltektar- og frágangsvinnu, verður að staðfesta sendinguna eða farminn í biðlara.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-114">When the worker uses a mobile device to indicate that the picking and put away work is completed, the shipment or load must be confirmed in the client.</span></span>

## <a name="enable-cluster-picking"></a><span data-ttu-id="3f7fc-115">Virkja klasatiltekt</span><span class="sxs-lookup"><span data-stu-id="3f7fc-115">Enable cluster picking</span></span>

<span data-ttu-id="3f7fc-116">Til að virkja klasatínslu, verður að setja upp eftirfarandi:</span><span class="sxs-lookup"><span data-stu-id="3f7fc-116">To enable cluster picking, you must set up the following:</span></span>

- <span data-ttu-id="3f7fc-117">**Klasaforstillingar** - Tilgreindu hvort á að sjálfkrafa búa til auðkenni klasa, fjölda stöðugilda til að nota, hvenær á að brjóta upp klasa, og hvernig á að raða og staðfesta tiltekt.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-117">**Cluster profiles** – Specify whether to automatically generate cluster   IDs, the number of positions to use, when to break clusters, and how to   sequence and verify the picking work.</span></span>

- <span data-ttu-id="3f7fc-118">**Vinnusniðmát** - Tilgreindu hvernig á að búa til tiltekt fyrir klasatiltekt.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-118">**Work templates** – Define how to create the picking work for cluster   picking.</span></span>

- <span data-ttu-id="3f7fc-119">**Staðsetningarleiðbeiningar** - Tilgreindu hvar á að taka til vörur og hvar á að setja þær.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-119">**Location directives** – Specify where to pick items from, and where to put   them.</span></span>

- <span data-ttu-id="3f7fc-120">**Valmyndaratriði fartækis** - Stilla valmyndaratriði fartækis til að nota fyrirliggjandi verk sem er stjórnað af klasatiltekt.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-120">**Mobile device menu items** – Configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="3f7fc-121">Þú verður að bæta valmyndaratriði valmynd fartækis þannig að það birtist í fartækjum.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-121">You must then add the menu item to a mobile device menu so that it is displayed on mobile devices.</span></span>

- <span data-ttu-id="3f7fc-122">**Færibreytur vöruhúsakerfis** - Tilgreindu talnarunu til að nota ef þú vilt búa til auðkenni fyrir klasa.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-122">**Warehouse management parameters** – Specify the number sequence to use if   you want to generate identifiers for clusters.</span></span>

## <a name="set-up-a-cluster-profile"></a><span data-ttu-id="3f7fc-123">Setja upp klasaforstillingu</span><span class="sxs-lookup"><span data-stu-id="3f7fc-123">Set up a cluster profile</span></span>

<span data-ttu-id="3f7fc-124">Til að setja upp forstillingu sem klasa, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="3f7fc-124">To set up a cluster profile, follow these steps:</span></span>

1. <span data-ttu-id="3f7fc-125">Smelltu á **Vöruhúsakerfi** \> **Uppsetning** \> **Fartæki** \> **Klasaforstillingar**.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-125">Click **Warehouse management** \> **Setup** \> **Mobile device** \>  **Cluster profiles**.</span></span>

1. <span data-ttu-id="3f7fc-126">Smelltu á **Nýtt** til að stofna nýja forstillingu.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-126">Click **New** to create a new profile.</span></span>

1. <span data-ttu-id="3f7fc-127">Smelltu á **Stofna klasa** og, undir **Klasaröðun**, skal smella á **Nýtt** til að setja upp röðunarforsendur fyrir klasann.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-127">Click **Create cluster** and, under **Cluster sorting**, click **New** to set up the sorting criteria for the cluster.</span></span> <span data-ttu-id="3f7fc-128">Röðunarforsendur að stýra röðinni sem starfsmaðurinn mun framkvæma tiltekt vinnu.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-128">The sorting criteria control the order in which the worker will perform the picking work.</span></span> <span data-ttu-id="3f7fc-129">Hægt er að bæta við eins mörgum skilyrðum og þarf.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-129">You can add as many criteria as needed.</span></span>

1. <span data-ttu-id="3f7fc-130">Í reitnum **Númeraröð** skal slá inn númer til að skilgreina röðina sem unnið er úr röðunarforsendum.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-130">In the **Sequence number** field, enter a number to define the order in  which the sorting criteria are processed.</span></span>

1. <span data-ttu-id="3f7fc-131">Í reitnum **Reitarheiti** velurðu reitinn sem mun ákvarða flokkun.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-131">In the **Field name** field, select the field that will determine the sorting.</span></span> <span data-ttu-id="3f7fc-132">Til dæmis, ef þú velur **WMSLocationId** svæðinu vinnu verður raðað eftir staðsetningu.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-132">For example, if you select the **WMSLocationId** field, the work will be sorted by location.</span></span>

1. <span data-ttu-id="3f7fc-133">Í reitnum **Röðun** skal velja einn af eftirfarandi valkostum.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-133">In the **Sorting** field, select one of the following options.</span></span>

| <span data-ttu-id="3f7fc-134">**Valkostur**</span><span class="sxs-lookup"><span data-stu-id="3f7fc-134">**Option**</span></span>     | <span data-ttu-id="3f7fc-135">**Lýsing**</span><span class="sxs-lookup"><span data-stu-id="3f7fc-135">**Description**</span></span>                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f7fc-136">**Hækkandi**</span><span class="sxs-lookup"><span data-stu-id="3f7fc-136">**Ascending**</span></span>  | <span data-ttu-id="3f7fc-137">Tiltektarvinnu er raðað í hækkandi röð samkvæmt röðunarforsendunni.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-137">Picking work is sequenced in ascending order based on the sorting criteria.</span></span> <span data-ttu-id="3f7fc-138">Til dæmis, ef nota á **WMSLocationId** eru svæði sem á að raða skilyrðum og Kenni skal staðsetningu 1, 2, 3 og 4, er verður að taka frá staðsetningu 4 fyrst.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-138">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 4 first.</span></span> |
| <span data-ttu-id="3f7fc-139">**Í lækkandi röð**</span><span class="sxs-lookup"><span data-stu-id="3f7fc-139">**Descending**</span></span> | <span data-ttu-id="3f7fc-140">Tiltektarvinnu er raðað í lækkandi röð samkvæmt röðunarforsendunni.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-140">Picking work is sequenced in descending order based on the sorting criteria.</span></span> <span data-ttu-id="3f7fc-141">Til dæmis, ef nota á **WMSLocationId** eru svæði sem á að raða skilyrðum og Kenni skal staðsetningu 1, 2, 3 og 4, er verður að taka frá staðsetningu 1 fyrst.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-141">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 1 first.</span></span> |

## <a name="item-confirmation"></a><span data-ttu-id="3f7fc-142">Vörustaðfesting</span><span class="sxs-lookup"><span data-stu-id="3f7fc-142">Item confirmation</span></span>

<span data-ttu-id="3f7fc-143">Þegar klasatiltekt er notuð, er vörustaðfesting nauðsynleg svo hægt sé að staðfesta þær vörur sem bætt er við klasa.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-143">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="3f7fc-144">Hægt er að staðfesta vörur í klasatiltekt á meðan klasatiltekt stendur yfir.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-144">You can verify items in cluster picking during the cluster picking process.</span></span> <span data-ttu-id="3f7fc-145">Uppsetning byggist á strikamerkjauppsetningu vöru.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-145">The setup is based on the product bar code setup.</span></span>

### <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="3f7fc-146">Setja upp vörustaðfestingu með klasatiltekt</span><span class="sxs-lookup"><span data-stu-id="3f7fc-146">Set up item verification with cluster picking</span></span>

1. <span data-ttu-id="3f7fc-147">Í valmyndaratriði fartækis skal opna eyðublað uppsetningar fyrir vinnustaðfestingu: **Vöruhúsakerfi** \> **Vöruhúsakerfi** \> **Uppsetning** \> **Fartæki** \> **Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-147">On a mobile device menu item, open the setup form for work confirmation:  **Warehouse management** \> **Warehouse management** \> **Setup** \>  **Mobile device** \> **Mobile device menu items**.</span></span>

1. <span data-ttu-id="3f7fc-148">Opna **Uppsetning vinnustaðfestingar** í valmyndaratriði fartækis.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-148">From the mobile device menu item, open **Work confirmation setup**.</span></span> <span data-ttu-id="3f7fc-149">Valkosturinn **Afurðarstaðfesting** leyfir þér að staðfesta hvert stykki af birgðum úr fartæki þegar það er skannað.</span><span class="sxs-lookup"><span data-stu-id="3f7fc-149">The **Product confirmation** option allows you to verify each piece of inventory from the mobile device when scanned.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]