---
title: Birgðastaðsetningar
description: Birgðastaðsetningar eru notaðar með grunnvöruhúsi (WMS I) til að ákveða hvar geyma skuli vörur og hvar vörur eru teknar til í WMS I vöruhúsi.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSLocation, WMSBlockingCause
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 009106327db971a7fc43a2a3ad233f16eb7ff620
ms.sourcegitcommit: 8cbaeb6443ce47a4c4bc02b5e1a1212eb0056b38
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 09/22/2020
ms.locfileid: "3829730"
---
# <a name="inventory-locations"></a><span data-ttu-id="93edb-103">Birgðastaðsetningar</span><span class="sxs-lookup"><span data-stu-id="93edb-103">Inventory locations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93edb-104">Birgðastaðsetningar eru notaðar með grunnvöruhúsi (WMS I) til að ákveða hvar geyma skuli vörur og hvar vörur eru teknar til í WMS I vöruhúsi.</span><span class="sxs-lookup"><span data-stu-id="93edb-104">Inventory locations are used with basic warehousing (WMS I) to determine where items are stored and where items are picked from in a WMS I warehouse.</span></span>

<span data-ttu-id="93edb-105">Athugasemd: Þetta efni á við aðgerðir í kerfiseiningu vöruhúsastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="93edb-105">This topic applies to features in the Inventory management module.</span></span> <span data-ttu-id="93edb-106">Það á ekki við um aðgerðir í kerfiseiningu vöruhúsastjórnunar.</span><span class="sxs-lookup"><span data-stu-id="93edb-106">It does not apply to features in the Warehouse management module.</span></span>

<span data-ttu-id="93edb-107">Hugtakið staðsetning vísar til staðurinn sem vörur eru geymdar og gefnar út úr.</span><span class="sxs-lookup"><span data-stu-id="93edb-107">The term location refers to the place that items are stored and drawn from.</span></span>

<span data-ttu-id="93edb-108">Fyrir hverja staðsetningu, staðurinn þar sem varan er sett inn einnig er hægt að tilgreina.</span><span class="sxs-lookup"><span data-stu-id="93edb-108">For each location, the place where the item is inserted can also be specified.</span></span> <span data-ttu-id="93edb-109">Að sjálfgefnu þær eru þær sömu.</span><span class="sxs-lookup"><span data-stu-id="93edb-109">By default, they are the same.</span></span> <span data-ttu-id="93edb-110">Vörur eru yfirleitt settar í og dregnar úr sömu hlið í staðsetningu, en ekki alltaf.</span><span class="sxs-lookup"><span data-stu-id="93edb-110">Items are usually inserted and drawn from the same side of a location, but not always.</span></span> <span data-ttu-id="93edb-111">Til dæmis vörur sem eru vistaðar í virku geymslu rekka eru sett inn úr einum gangi og gefnir út frá öðru.</span><span class="sxs-lookup"><span data-stu-id="93edb-111">For example, items that are stored in live storage racks are inserted from one aisle and drawn from another.</span></span> <span data-ttu-id="93edb-112">Aðalinntakið er frá heiti staðsetningar sem er yfirleitt ákveðin af hnitum hennar: vöruhús, gangur, rekki, hillu og körfu.</span><span class="sxs-lookup"><span data-stu-id="93edb-112">The main input is given by a location name, which is usually determined by its coordinates: warehouse, aisle, rack, shelf, and bin.</span></span> <span data-ttu-id="93edb-113">Þetta heiti eða kenni er fært inn handvirkt eða myndar úr stasetningarhnitum - til dæmis 01-02-03-4 fyrir gang 1, rekki 2, hilla 3, karfa 4 í  síðunni birgðastaðsetningar.</span><span class="sxs-lookup"><span data-stu-id="93edb-113">This name or ID can be entered manually or generated from the location coordinates—for example, 01-02-03-4 for aisle 1, rack 2, shelf 3, bin 4 in the Inventory locations page.</span></span>
<span data-ttu-id="93edb-114">Eiginleikar staðsetningar</span><span class="sxs-lookup"><span data-stu-id="93edb-114">Location properties</span></span>

<span data-ttu-id="93edb-115">Staðsetning hefur eftirfarandi eiginleika:</span><span class="sxs-lookup"><span data-stu-id="93edb-115">A location has the following characteristics:</span></span>
-   <span data-ttu-id="93edb-116">Stærð (hæð, breidd, dýpt, og þar með rúmmál)</span><span class="sxs-lookup"><span data-stu-id="93edb-116">Size (height, width, depth, and thereby volume)</span></span>
-   <span data-ttu-id="93edb-117">Vöruhús, rekka, hillu og körfustöðu.</span><span class="sxs-lookup"><span data-stu-id="93edb-117">Warehouse, aisle, rack, shelf, and bin position</span></span>
-   <span data-ttu-id="93edb-118">Gerð staðsetningar (biðstaðsetningu, tiltektarstaðsetning, inn-hlið, út-hlið, staðsetning framleiðsluinntaks, eftirlitsstaðsetning eða kanban-geymslusvæði)</span><span class="sxs-lookup"><span data-stu-id="93edb-118">Location type (bulk location, picking location, inbound dock, outbound dock, production input location, inspection location, or kanban supermarket)</span></span>

<span data-ttu-id="93edb-119">Ekki er hægt að notag ávísunartexta í netkerfum til að staðfesta að virknitáknið hafi valið rétta staðsetningu fyrir tilgreint vara.</span><span class="sxs-lookup"><span data-stu-id="93edb-119">Check text can be used in online systems to verify that the operator has selected the correct location for a specific item.</span></span> <span data-ttu-id="93edb-120">Þennan stýritexta er hægt að stofna handvirkt eða sjálfkrafa.</span><span class="sxs-lookup"><span data-stu-id="93edb-120">This check text can be created manually or by default.</span></span>

## <a name="sort-codes"></a><span data-ttu-id="93edb-121">Raðkóðar</span><span class="sxs-lookup"><span data-stu-id="93edb-121">Sort codes</span></span>
<span data-ttu-id="93edb-122">Notaðu röðunarkóða til að hámarka meðferð tiltektarlína, sem lýsa upplýsingunum sem er krafist fyrir tiltektarvörur úr birgðum, þar með talið tiltektarröðun.</span><span class="sxs-lookup"><span data-stu-id="93edb-122">Use sort codes to optimize the handling of picking lines, which describe the information that is required for picking items from inventory, including the picking order.</span></span> <span data-ttu-id="93edb-123">Það er hægt að tilgreina raðkóða eftir ganginum og öðrum hnitum eða með því að úthluta þeim handvirkt fyrir staðsetninguna.</span><span class="sxs-lookup"><span data-stu-id="93edb-123">Sort codes can be specified by the aisle and other coordinates, or assigned manually for the location.</span></span>

## <a name="blocked-locations"></a><span data-ttu-id="93edb-124">Lokaðar staðsetningar</span><span class="sxs-lookup"><span data-stu-id="93edb-124">Blocked locations</span></span>
<span data-ttu-id="93edb-125">Stundum gæti þurft að gefa til kynna að staðsetning verði læst um ákveðinn tíma, til dæmis til að framkvæma viðgerðir.</span><span class="sxs-lookup"><span data-stu-id="93edb-125">Occasionally, you might want to indicate that a location is blocked for a period of time, for example, to allow for repairs.</span></span> <span data-ttu-id="93edb-126">Á öðrum tímum er hugsanlegt að læsa aðeins ílag eða aðeins frálag.</span><span class="sxs-lookup"><span data-stu-id="93edb-126">At other times, you may want to indicate blocking of only the input or only output.</span></span>

## <a name="tree-structure"></a><span data-ttu-id="93edb-127">Trjáskipulag</span><span class="sxs-lookup"><span data-stu-id="93edb-127">Tree structure</span></span>

<span data-ttu-id="93edb-128">Í síðu birgðastaðsetning er hægt að skoða útlit vöruhúss í tréskipulagi eftir hnitum birgðastaðsetninga í skilgreindu skjásniði.</span><span class="sxs-lookup"><span data-stu-id="93edb-128">In the Inventory locations page, you can view the warehouse layout in a tree structure based on the coordinates of inventory locations, in a defined display format.</span></span>

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a><span data-ttu-id="93edb-129">Viðhalda birgðastaðsetning í skjámyndinni vöruhús</span><span class="sxs-lookup"><span data-stu-id="93edb-129">Maintain inventory locations via the warehouse form</span></span>

<span data-ttu-id="93edb-130">Mögulegt er að afrita staðsetningar úr einu vöruhúsi í annað og til að stofna staðsetningar með leiðsagnarforriti.</span><span class="sxs-lookup"><span data-stu-id="93edb-130">It is possible to copy locations from one warehouse to another and to create locations via a wizard.</span></span> <span data-ttu-id="93edb-131">Áður en leiðsagnarforritið keyrt skal ganga úr skugga sem um að þú hefur skilgreint heiti fyrir sjálfgefin staðsetning síðu Vöruhúss.</span><span class="sxs-lookup"><span data-stu-id="93edb-131">Before you run the wizard you should make sure that you have defined the default location names on the Warehouse page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="93edb-132">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="93edb-132">Additional resources</span></span>
--------

[<span data-ttu-id="93edb-133">Búa til nýtt vöruhúsaútlit</span><span class="sxs-lookup"><span data-stu-id="93edb-133">Create a new warehouse layout</span></span>](tasks/create-new-warehouse-layout.md)
