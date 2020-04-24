---
title: Hlutaafhending á flutningsfarmi
description: Þetta efnisatriði útskýrir hvernig hægt er að afhenda hluta úr farmi og fresta áætlun um afkastagetu farmsins.
author: Mirzaab
manager: tfehr
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: e92a15cf4e2694eba1804184a02a7fd13159799e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215655"
---
# <a name="partial-shipment-of-a-transport-load"></a><span data-ttu-id="13e1b-103">Hlutaafhending á flutningsfarmi</span><span class="sxs-lookup"><span data-stu-id="13e1b-103">Partial shipment of a transport load</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="13e1b-104">Með því að setja upp hlutaafhendingu á farmi er hægt að meðhöndla farm þar sem ekki er hægt að ákvarða afkastagetu fyrr en öllum sölulínum hefur verið bætt við farm.</span><span class="sxs-lookup"><span data-stu-id="13e1b-104">By setting up partial shipment of loads, you can handle loads where the capacity can't be determined until all the sales lines have been added to a load.</span></span> <span data-ttu-id="13e1b-105">Þá er hægt að ljúka ferlinu þegar nákvæm brettatalning er þekkt.</span><span class="sxs-lookup"><span data-stu-id="13e1b-105">The process can then be finalized when the exact pallet count is known.</span></span> <span data-ttu-id="13e1b-106">Þess vegna þarf ekki að ákveða hvaða brettum verður úthlutað á hvaða flutning fyrr en á augnablikinu sem verið er að hlaða flutning úr uppsettum birgðum.</span><span class="sxs-lookup"><span data-stu-id="13e1b-106">Therefore, you don't have to decide which pallets will be assigned to which transport until the moment when a transport is being physically loaded out of the staged inventory.</span></span>

<span data-ttu-id="13e1b-107">Þessi eiginleiki býður upp á annan valkost við framfylgni á stífara skipulagi þar sem þarf að ákveða hvaða brettum verður úthlutað á hvaða flutning áður en hægt er að búa til tiltekt eða hleðsluvinnu.</span><span class="sxs-lookup"><span data-stu-id="13e1b-107">This feature offers an alternative to the enforcement of a more rigid structure, where you must determine which pallets will be assigned to which transport before picking work or loading work can be created.</span></span> <span data-ttu-id="13e1b-108">Í staðinn geta notendur stillt einstakar hleðslur fyrir staðfesta hlutaafhendingu.</span><span class="sxs-lookup"><span data-stu-id="13e1b-108">Instead, users can configure individual loads for a partial shipment confirmation.</span></span> <span data-ttu-id="13e1b-109">Flutningshleðsluferli fyrir þessar hleðslur getur þá átt sér stað.</span><span class="sxs-lookup"><span data-stu-id="13e1b-109">The transport loading processes for those loads can then occur.</span></span> <span data-ttu-id="13e1b-110">Þess vegna getur flutningsáætlunardeildin skipulagt farma án þess að þurfa að íhuga getu einstakra flutninga.</span><span class="sxs-lookup"><span data-stu-id="13e1b-110">Therefore, the transportation planning department can plan loads without having to consider the capacity of individual transports.</span></span>

<span data-ttu-id="13e1b-111">Við hleðslu geta starfskraftar skilgreint nýjan flutningsfarm sem hægt er að hlaða bretti á.</span><span class="sxs-lookup"><span data-stu-id="13e1b-111">At the time of loading, workers can define a new transport load that a pallet can be loaded to.</span></span> <span data-ttu-id="13e1b-112">Að öðrum kosti geta þeir borið kennsl á flutningsfarm sem er til staðar.</span><span class="sxs-lookup"><span data-stu-id="13e1b-112">Alternatively, they can identify an existing transport load.</span></span> <span data-ttu-id="13e1b-113">Hægt er að skrá þessi gögn í gegnum fartæki.</span><span class="sxs-lookup"><span data-stu-id="13e1b-113">This data can be recorded via a mobile device.</span></span> <span data-ttu-id="13e1b-114">Þess vegna geta nokkrir starfskraftar í vöruhúsi hlaðið birgðum frá sömu hleðslu yfir á aðra hleðslu á sama vörubílnum.</span><span class="sxs-lookup"><span data-stu-id="13e1b-114">Therefore, several warehouse workers can load inventory from the same loads or different loads onto the same truck.</span></span> <span data-ttu-id="13e1b-115">Síðan er hægt að afhenda farminn að fullu eða að hluta til.</span><span class="sxs-lookup"><span data-stu-id="13e1b-115">The loads can then be fully or partially shipped.</span></span>

> [!NOTE] 
> <span data-ttu-id="13e1b-116">Til að hlaða birgðum frá farmi yfir á sérstakan flutningsfarm og afhenda farminn að hluta til, þarf að búa til vinnu með hleðsluflokki í vinnusniðmáti.</span><span class="sxs-lookup"><span data-stu-id="13e1b-116">In order to load inventory from a load to a specific transport load and partially ship the load, work must be generated by using a loading class in a work template.</span></span> <span data-ttu-id="13e1b-117">Ekki er hægt að hlaða venjulega tiltekt af gerðinni **Tiltekt** á flutningsfarm eins og vörubíl.</span><span class="sxs-lookup"><span data-stu-id="13e1b-117">Ordinary picking work of the **Picking** type can't be loaded to a transport load such as a truck.</span></span>

## <a name="set-up-transport-loads-for-partial-shipment"></a><span data-ttu-id="13e1b-118">Setja upp flutningsfarma fyrir hlutaafhendingu</span><span class="sxs-lookup"><span data-stu-id="13e1b-118">Set up transport loads for partial shipment</span></span>

<span data-ttu-id="13e1b-119">Uppsetning á hlutaafhendingu farma samanstendur af eftirfarandi tveimur ferlum.</span><span class="sxs-lookup"><span data-stu-id="13e1b-119">The setup for partial shipment of loads consists of the following two procedures.</span></span>

### <a name="set-the-loading-strategy"></a><span data-ttu-id="13e1b-120">Stilltu hleðsluáætlunina</span><span class="sxs-lookup"><span data-stu-id="13e1b-120">Set the loading strategy</span></span>

<span data-ttu-id="13e1b-121">Þú verður að virkja að hlutahleðslu með því að stilla hleðsluáætlunina.</span><span class="sxs-lookup"><span data-stu-id="13e1b-121">You must enable partial loading by setting the loading strategy.</span></span> <span data-ttu-id="13e1b-122">Þú getur stillt hleðsluáætlunina eftir að þú hefur búið til hleðslu.</span><span class="sxs-lookup"><span data-stu-id="13e1b-122">You can set the loading strategy after you've created a load.</span></span>

1. <span data-ttu-id="13e1b-123">Veldu **Vöruhúsakerfi** \> **Hleðslur** \> **Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="13e1b-123">Select **Warehouse management** \> **Loads** \> **All loads**.</span></span>
2. <span data-ttu-id="13e1b-124">Veldu hleðslu og smelltu síðan á **Haus**.</span><span class="sxs-lookup"><span data-stu-id="13e1b-124">Select a load, and then click **Header**.</span></span>
3. <span data-ttu-id="13e1b-125">Í reitnum **Hleðsluáætlun** skal velja **Afhending hlutahleðsla leyfð**.</span><span class="sxs-lookup"><span data-stu-id="13e1b-125">In the **Loading strategy** field, select **Partial load shipping allowed**.</span></span>

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a><span data-ttu-id="13e1b-126">Búðu til valmyndaratriði fyrir hleðslu flutningsfarms</span><span class="sxs-lookup"><span data-stu-id="13e1b-126">Create a menu item for loading of transport loads</span></span>

<span data-ttu-id="13e1b-127">Þú verður að búa til nýtt valmyndaratriði sem gerir kleift að hlaða flutningsfarmi.</span><span class="sxs-lookup"><span data-stu-id="13e1b-127">You must create a new menu item that enables transport loads to be loaded.</span></span> <span data-ttu-id="13e1b-128">Flutningsfarmur gerir þér kleift að flokka vinnulínur frá einni hleðslu eða mörgum hleðslum.</span><span class="sxs-lookup"><span data-stu-id="13e1b-128">A transport load lets you group work lines from one load or multiple loads.</span></span> <span data-ttu-id="13e1b-129">Allt sem er bætt við flutningsfarminn getur síðan verið afhent með því að nota farsímaskanna.</span><span class="sxs-lookup"><span data-stu-id="13e1b-129">Everything that is added to the transport load can then be shipped by using a mobile scanner.</span></span>

1. <span data-ttu-id="13e1b-130">Veldu **Vöruhúsakerfi** \> **Uppsetning** \> **Fartæki** \> **Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="13e1b-130">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="13e1b-131">Veldu **Nýtt** og síðan í reitnum **Snið** skal velja **Vinna**.</span><span class="sxs-lookup"><span data-stu-id="13e1b-131">Select **New**, and then, in the **Mode** field, select **Work**.</span></span>
3. <span data-ttu-id="13e1b-132">Stilltu valkostinn **Nota fyrirliggjandi vinnu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="13e1b-132">Set the **Use existing work** option to **Yes**.</span></span>
4. <span data-ttu-id="13e1b-133">Í flipanum **Almennt**, í reitnum **Stýrt af** skal velja **Flutningshleðsla**.</span><span class="sxs-lookup"><span data-stu-id="13e1b-133">On the **General** tab, in the **Directed by** field, select **Transport loading**.</span></span>
5. <span data-ttu-id="13e1b-134">Til að virkja staðfestingu á afhendingu á farsímaskanna skal í reitnum **Leyfð gerð á staðfestingu afhendingar** velja **Flutningsfarmur**.</span><span class="sxs-lookup"><span data-stu-id="13e1b-134">To enable shipment confirmation on a mobile scanner, in the **Allowed ship confirmation type** field, select **Transport load**.</span></span>

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a><span data-ttu-id="13e1b-135">Staðfestu afhendingu á flutningsfarmi frá viðskiptavininum</span><span class="sxs-lookup"><span data-stu-id="13e1b-135">Confirm shipment of a transport load from the client</span></span>

<span data-ttu-id="13e1b-136">Þessi uppsetning gerir þér kleift að staðfesta flutningsfarm sem inniheldur fulla hleðslu eða hlutahleðslu sem á að afhenda.</span><span class="sxs-lookup"><span data-stu-id="13e1b-136">This setup lets you confirm a transport load that includes a full load or a partially loaded load to be shipped.</span></span>

1. <span data-ttu-id="13e1b-137">Veldu **Vöruhúsakerfi** \> **Hleðslur** \> **Flutningshleðslur**.</span><span class="sxs-lookup"><span data-stu-id="13e1b-137">Select **Warehouse management** \> **Loads** \> **Transport loads**.</span></span>
2. <span data-ttu-id="13e1b-138">Í aðgerðasvæðinu, í flipanum **Afhenda og móttaka** í flokknum **Staðfesta** skal velja **Flutningur**.</span><span class="sxs-lookup"><span data-stu-id="13e1b-138">On the Action Pane, on the **Ship and receive** tab, in the **Confirm** group, select **Transport**.</span></span>
