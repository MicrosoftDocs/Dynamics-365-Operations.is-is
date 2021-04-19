---
title: Hlutaafhending á flutningsfarmi
description: Þetta efnisatriði útskýrir hvernig hægt er að afhenda hluta úr farmi og fresta áætlun um afkastagetu farmsins.
author: Mirzaab
ms.date: 03/15/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSTransportLoad
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.assetid: 427e01b3-4968-4cff-9b85-1717530f72e4
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 179a784f1f02ed0840ba5219c350e274272b59eb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818945"
---
# <a name="partial-shipment-of-a-transport-load"></a><span data-ttu-id="f48c7-103">Hlutaafhending á flutningsfarmi</span><span class="sxs-lookup"><span data-stu-id="f48c7-103">Partial shipment of a transport load</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f48c7-104">Með því að setja upp hlutaafhendingu á farmi er hægt að meðhöndla farm þar sem ekki er hægt að ákvarða afkastagetu fyrr en öllum sölulínum hefur verið bætt við farm.</span><span class="sxs-lookup"><span data-stu-id="f48c7-104">By setting up partial shipment of loads, you can handle loads where the capacity can't be determined until all the sales lines have been added to a load.</span></span> <span data-ttu-id="f48c7-105">Þá er hægt að ljúka ferlinu þegar nákvæm brettatalning er þekkt.</span><span class="sxs-lookup"><span data-stu-id="f48c7-105">The process can then be finalized when the exact pallet count is known.</span></span> <span data-ttu-id="f48c7-106">Þess vegna þarf ekki að ákveða hvaða brettum verður úthlutað á hvaða flutning fyrr en á augnablikinu sem verið er að hlaða flutning úr uppsettum birgðum.</span><span class="sxs-lookup"><span data-stu-id="f48c7-106">Therefore, you don't have to decide which pallets will be assigned to which transport until the moment when a transport is being physically loaded out of the staged inventory.</span></span>

<span data-ttu-id="f48c7-107">Þessi eiginleiki býður upp á annan valkost við framfylgni á stífara skipulagi þar sem þarf að ákveða hvaða brettum verður úthlutað á hvaða flutning áður en hægt er að búa til tiltekt eða hleðsluvinnu.</span><span class="sxs-lookup"><span data-stu-id="f48c7-107">This feature offers an alternative to the enforcement of a more rigid structure, where you must determine which pallets will be assigned to which transport before picking work or loading work can be created.</span></span> <span data-ttu-id="f48c7-108">Í staðinn geta notendur stillt einstakar hleðslur fyrir staðfesta hlutaafhendingu.</span><span class="sxs-lookup"><span data-stu-id="f48c7-108">Instead, users can configure individual loads for a partial shipment confirmation.</span></span> <span data-ttu-id="f48c7-109">Flutningshleðsluferli fyrir þessar hleðslur getur þá átt sér stað.</span><span class="sxs-lookup"><span data-stu-id="f48c7-109">The transport loading processes for those loads can then occur.</span></span> <span data-ttu-id="f48c7-110">Þess vegna getur flutningsáætlunardeildin skipulagt farma án þess að þurfa að íhuga getu einstakra flutninga.</span><span class="sxs-lookup"><span data-stu-id="f48c7-110">Therefore, the transportation planning department can plan loads without having to consider the capacity of individual transports.</span></span>

<span data-ttu-id="f48c7-111">Við hleðslu geta starfskraftar skilgreint nýjan flutningsfarm sem hægt er að hlaða bretti á.</span><span class="sxs-lookup"><span data-stu-id="f48c7-111">At the time of loading, workers can define a new transport load that a pallet can be loaded to.</span></span> <span data-ttu-id="f48c7-112">Að öðrum kosti geta þeir borið kennsl á flutningsfarm sem er til staðar.</span><span class="sxs-lookup"><span data-stu-id="f48c7-112">Alternatively, they can identify an existing transport load.</span></span> <span data-ttu-id="f48c7-113">Hægt er að skrá þessi gögn í gegnum fartæki.</span><span class="sxs-lookup"><span data-stu-id="f48c7-113">This data can be recorded via a mobile device.</span></span> <span data-ttu-id="f48c7-114">Þess vegna geta nokkrir starfskraftar í vöruhúsi hlaðið birgðum frá sömu hleðslu yfir á aðra hleðslu á sama vörubílnum.</span><span class="sxs-lookup"><span data-stu-id="f48c7-114">Therefore, several warehouse workers can load inventory from the same loads or different loads onto the same truck.</span></span> <span data-ttu-id="f48c7-115">Síðan er hægt að afhenda farminn að fullu eða að hluta til.</span><span class="sxs-lookup"><span data-stu-id="f48c7-115">The loads can then be fully or partially shipped.</span></span>

> [!NOTE] 
> <span data-ttu-id="f48c7-116">Til að hlaða birgðum frá farmi yfir á sérstakan flutningsfarm og afhenda farminn að hluta til, þarf að búa til vinnu með hleðsluflokki í vinnusniðmáti.</span><span class="sxs-lookup"><span data-stu-id="f48c7-116">In order to load inventory from a load to a specific transport load and partially ship the load, work must be generated by using a loading class in a work template.</span></span> <span data-ttu-id="f48c7-117">Ekki er hægt að hlaða venjulega tiltekt af gerðinni **Tiltekt** á flutningsfarm eins og vörubíl.</span><span class="sxs-lookup"><span data-stu-id="f48c7-117">Ordinary picking work of the **Picking** type can't be loaded to a transport load such as a truck.</span></span>

## <a name="set-up-transport-loads-for-partial-shipment"></a><span data-ttu-id="f48c7-118">Setja upp flutningsfarma fyrir hlutaafhendingu</span><span class="sxs-lookup"><span data-stu-id="f48c7-118">Set up transport loads for partial shipment</span></span>

<span data-ttu-id="f48c7-119">Uppsetning á hlutaafhendingu farma samanstendur af eftirfarandi tveimur ferlum.</span><span class="sxs-lookup"><span data-stu-id="f48c7-119">The setup for partial shipment of loads consists of the following two procedures.</span></span>

### <a name="set-the-loading-strategy"></a><span data-ttu-id="f48c7-120">Stilltu hleðsluáætlunina</span><span class="sxs-lookup"><span data-stu-id="f48c7-120">Set the loading strategy</span></span>

<span data-ttu-id="f48c7-121">Þú verður að virkja að hlutahleðslu með því að stilla hleðsluáætlunina.</span><span class="sxs-lookup"><span data-stu-id="f48c7-121">You must enable partial loading by setting the loading strategy.</span></span> <span data-ttu-id="f48c7-122">Þú getur stillt hleðsluáætlunina eftir að þú hefur búið til hleðslu.</span><span class="sxs-lookup"><span data-stu-id="f48c7-122">You can set the loading strategy after you've created a load.</span></span>

1. <span data-ttu-id="f48c7-123">Veldu **Vöruhúsakerfi** \> **Hleðslur** \> **Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="f48c7-123">Select **Warehouse management** \> **Loads** \> **All loads**.</span></span>
2. <span data-ttu-id="f48c7-124">Veldu hleðslu og smelltu síðan á **Haus**.</span><span class="sxs-lookup"><span data-stu-id="f48c7-124">Select a load, and then click **Header**.</span></span>
3. <span data-ttu-id="f48c7-125">Í reitnum **Hleðsluáætlun** skal velja **Afhending hlutahleðsla leyfð**.</span><span class="sxs-lookup"><span data-stu-id="f48c7-125">In the **Loading strategy** field, select **Partial load shipping allowed**.</span></span>

### <a name="create-a-menu-item-for-loading-of-transport-loads"></a><span data-ttu-id="f48c7-126">Búðu til valmyndaratriði fyrir hleðslu flutningsfarms</span><span class="sxs-lookup"><span data-stu-id="f48c7-126">Create a menu item for loading of transport loads</span></span>

<span data-ttu-id="f48c7-127">Þú verður að búa til nýtt valmyndaratriði sem gerir kleift að hlaða flutningsfarmi.</span><span class="sxs-lookup"><span data-stu-id="f48c7-127">You must create a new menu item that enables transport loads to be loaded.</span></span> <span data-ttu-id="f48c7-128">Flutningsfarmur gerir þér kleift að flokka vinnulínur frá einni hleðslu eða mörgum hleðslum.</span><span class="sxs-lookup"><span data-stu-id="f48c7-128">A transport load lets you group work lines from one load or multiple loads.</span></span> <span data-ttu-id="f48c7-129">Allt sem er bætt við flutningsfarminn getur síðan verið afhent með því að nota farsímaskanna.</span><span class="sxs-lookup"><span data-stu-id="f48c7-129">Everything that is added to the transport load can then be shipped by using a mobile scanner.</span></span>

1. <span data-ttu-id="f48c7-130">Veldu **Vöruhúsakerfi** \> **Uppsetning** \> **Fartæki** \> **Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="f48c7-130">Select **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>
2. <span data-ttu-id="f48c7-131">Veldu **Nýtt** og síðan í reitnum **Snið** skal velja **Vinna**.</span><span class="sxs-lookup"><span data-stu-id="f48c7-131">Select **New**, and then, in the **Mode** field, select **Work**.</span></span>
3. <span data-ttu-id="f48c7-132">Stilltu valkostinn **Nota fyrirliggjandi vinnu** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="f48c7-132">Set the **Use existing work** option to **Yes**.</span></span>
4. <span data-ttu-id="f48c7-133">Í flipanum **Almennt**, í reitnum **Stýrt af** skal velja **Flutningshleðsla**.</span><span class="sxs-lookup"><span data-stu-id="f48c7-133">On the **General** tab, in the **Directed by** field, select **Transport loading**.</span></span>
5. <span data-ttu-id="f48c7-134">Til að virkja staðfestingu á afhendingu á farsímaskanna skal í reitnum **Leyfð gerð á staðfestingu afhendingar** velja **Flutningsfarmur**.</span><span class="sxs-lookup"><span data-stu-id="f48c7-134">To enable shipment confirmation on a mobile scanner, in the **Allowed ship confirmation type** field, select **Transport load**.</span></span>

## <a name="confirm-shipment-of-a-transport-load-from-the-client"></a><span data-ttu-id="f48c7-135">Staðfestu afhendingu á flutningsfarmi frá viðskiptavininum</span><span class="sxs-lookup"><span data-stu-id="f48c7-135">Confirm shipment of a transport load from the client</span></span>

<span data-ttu-id="f48c7-136">Þessi uppsetning gerir þér kleift að staðfesta flutningsfarm sem inniheldur fulla hleðslu eða hlutahleðslu sem á að afhenda.</span><span class="sxs-lookup"><span data-stu-id="f48c7-136">This setup lets you confirm a transport load that includes a full load or a partially loaded load to be shipped.</span></span>

1. <span data-ttu-id="f48c7-137">Veldu **Vöruhúsakerfi** \> **Hleðslur** \> **Flutningshleðslur**.</span><span class="sxs-lookup"><span data-stu-id="f48c7-137">Select **Warehouse management** \> **Loads** \> **Transport loads**.</span></span>
2. <span data-ttu-id="f48c7-138">Í aðgerðasvæðinu, í flipanum **Afhenda og móttaka** í flokknum **Staðfesta** skal velja **Flutningur**.</span><span class="sxs-lookup"><span data-stu-id="f48c7-138">On the Action Pane, on the **Ship and receive** tab, in the **Confirm** group, select **Transport**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]