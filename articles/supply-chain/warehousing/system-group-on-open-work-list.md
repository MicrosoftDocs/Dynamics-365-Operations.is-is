---
title: "Kerfisflokkun á opnum verkefnalista"
description: "Í þessu efnisatriði er lýst hvernig eigi að sía opna vinnu í fartæki."
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d9ca6b0d4a9909d419d6241a044336d7a02aea02
ms.contentlocale: is-is
ms.lasthandoff: 04/13/2018

---

# <a name="system-grouping-on-an-open-work-list"></a><span data-ttu-id="a7459-103">Kerfisflokkun á opnum verkefnalista</span><span class="sxs-lookup"><span data-stu-id="a7459-103">System grouping on an open work list</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="a7459-104">Með því að nota kerfið flokkunarsvæði, er hægt að sía opna verkefnalistinn án þess að þurfa til þess að breyta fartæki valmyndaratriði.</span><span class="sxs-lookup"><span data-stu-id="a7459-104">By using a system grouping field, you can filter an open work list without having to edit the mobile device menu item.</span></span>
<span data-ttu-id="a7459-105">Þar sem það á við um flokkun kerfið vinnur síun verkefnalista á haussvæðið einni vinnustöð.</span><span class="sxs-lookup"><span data-stu-id="a7459-105">Where it applies, system grouping works for filtering a work list on a single work header field.</span></span> <span data-ttu-id="a7459-106">Ekki er hægt að nota kerfið flokkun á netinu stigasvæðum síu.</span><span class="sxs-lookup"><span data-stu-id="a7459-106">You cannot use system grouping to filter on line level fields.</span></span>

## <a name="set-up-system-grouping-on-an-open-work-list"></a><span data-ttu-id="a7459-107">Settu upp kerfisflokkun í opinn verkefnalista</span><span class="sxs-lookup"><span data-stu-id="a7459-107">Set up system grouping on an open work list</span></span>
<span data-ttu-id="a7459-108">Notið eftirfarandi skrefum til að setja upp kerfi flokkun á opnu verkefnalista.</span><span class="sxs-lookup"><span data-stu-id="a7459-108">Use these steps to set up system grouping on an open work list.</span></span>

-   <span data-ttu-id="a7459-109">Úr valmyndaratriði fartæki, veljið **Greiðslumáta: Óbeina** og **Kóða Verkþættinum: Birtingu opinna verkefnalistinn**.</span><span class="sxs-lookup"><span data-stu-id="a7459-109">From a mobile device menu item, select **Mode: Indirect** and **Activity Code: Display open work list**.</span></span> <span data-ttu-id="a7459-110">Eftirtaldir valkostir verða í boði.</span><span class="sxs-lookup"><span data-stu-id="a7459-110">The following options become available.</span></span> <span data-ttu-id="a7459-111">Þessir valkostir eru nauðsynleg fyrir flokkun á opnu verkefnalistinn kerfið.</span><span class="sxs-lookup"><span data-stu-id="a7459-111">These options are required for system grouping on an open work list.</span></span> 

|        <span data-ttu-id="a7459-112">Valkostur</span><span class="sxs-lookup"><span data-stu-id="a7459-112">Option</span></span>         |                                                                                                                                                                                                                                                                         <span data-ttu-id="a7459-113">lýsing</span><span class="sxs-lookup"><span data-stu-id="a7459-113">Description</span></span>                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7459-114">Leyfa flokkun kerfi</span><span class="sxs-lookup"><span data-stu-id="a7459-114">Allow system grouping</span></span> |                                                                                                                                                                                                                                                 <span data-ttu-id="a7459-115">Gerir kerfið groping fyrir vinnustöðina valmyndaratriði listann.</span><span class="sxs-lookup"><span data-stu-id="a7459-115">Enables system groping for a selected work list menu item.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="a7459-116">Kerfisflokkunarsvæði</span><span class="sxs-lookup"><span data-stu-id="a7459-116">System grouping field</span></span> | <span data-ttu-id="a7459-117">Aðeins tiltækt ef <strong>Leyfa kerfið vinnu</strong> er stillt á <strong>Já</strong>.</span><span class="sxs-lookup"><span data-stu-id="a7459-117">Available only if <strong>Allow system work</strong> is set to <strong>Yes</strong>.</span></span> <span data-ttu-id="a7459-118">Velja svæðið sem ákvarða hvernig tiltektarvinna verður flokkuð fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="a7459-118">Select the field that determines how picking work will be grouped for workers.</span></span> <span data-ttu-id="a7459-119">Til dæmis, ef þú velur <strong>ShipmentId</strong> svæðinu starfsmaður verður skanna Sendingarkennið til að flokka vinnuna tiltekt.</span><span class="sxs-lookup"><span data-stu-id="a7459-119">For example, if you select the <strong>ShipmentId</strong> field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="a7459-120">Öll vinna fyrir sendingunni er síðan úthlutað til starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="a7459-120">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="a7459-121">Þessi reitur krefst þess að stofnað sé valmyndaratriði til að nota fyrirliggjandi vinnu sem er flokkuð af kerfinu.</span><span class="sxs-lookup"><span data-stu-id="a7459-121">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="a7459-122">Notkun á <strong>Kerfið flokkun merki</strong> til að upplýsa viðkomandi hvað skanna.</span><span class="sxs-lookup"><span data-stu-id="a7459-122">Use the <strong>System grouping label</strong> field to inform the worker what to scan.</span></span> |
| <span data-ttu-id="a7459-123">Kerfisflokkunarmerki</span><span class="sxs-lookup"><span data-stu-id="a7459-123">System grouping label</span></span> |                       <span data-ttu-id="a7459-124">Aðeins tiltækt ef <strong>Leyfa kerfið vinnu</strong> er stillt á <strong>Já</strong>.</span><span class="sxs-lookup"><span data-stu-id="a7459-124">Available only if <strong>Allow system work</strong> is set to <strong>Yes</strong>.</span></span> <span data-ttu-id="a7459-125">Færið inn upplýsingar um starfsmann um hvað á að skanna þegar tiltekt vinnu er flokkuð.</span><span class="sxs-lookup"><span data-stu-id="a7459-125">Enter information for the worker about what to scan when picking work is grouped.</span></span> <span data-ttu-id="a7459-126">Til dæmis, ef verið er að nota reitinn <strong>ShipmentId</strong> til að flokka tiltektarvinnu eftir sendingu væri hægt að færa inn Sendingarkenni í reitinn.</span><span class="sxs-lookup"><span data-stu-id="a7459-126">For example, if you use the <strong>ShipmentId</strong> field to group picking work by shipment, you might enter Shipment ID in the field.</span></span> <span data-ttu-id="a7459-127">Þessi reitur krefst þess að stofnað sé valmyndaratriði til að nota fyrirliggjandi vinnu sem er flokkuð af kerfinu.</span><span class="sxs-lookup"><span data-stu-id="a7459-127">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="a7459-128">Einnig verður að velja reitinn til að flokka eftir í reitnum <strong>Kerfisflokkunarsvæði</strong>.</span><span class="sxs-lookup"><span data-stu-id="a7459-128">You must also select the field to group by in the <strong>System grouping</strong> field.</span></span>                       |


