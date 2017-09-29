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
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 0c68d544fec985f325e6472203533f23948cc9b4
ms.contentlocale: is-is
ms.lasthandoff: 07/18/2017

---

# <a name="system-grouping-on-an-open-work-list"></a><span data-ttu-id="f7f05-103">Kerfisflokkun á opnum verkefnalista</span><span class="sxs-lookup"><span data-stu-id="f7f05-103">System grouping on an open work list</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f7f05-104">Með því að nota kerfið flokkunarsvæði, er hægt að sía opna verkefnalistinn án þess að þurfa til þess að breyta fartæki valmyndaratriði.</span><span class="sxs-lookup"><span data-stu-id="f7f05-104">By using a system grouping field, you can filter an open work list without having to edit the mobile device menu item.</span></span>
<span data-ttu-id="f7f05-105">Þar sem það á við um flokkun kerfið vinnur síun verkefnalista á haussvæðið einni vinnustöð.</span><span class="sxs-lookup"><span data-stu-id="f7f05-105">Where it applies, system grouping works for filtering a work list on a single work header field.</span></span> <span data-ttu-id="f7f05-106">Ekki er hægt að nota kerfið flokkun á netinu stigasvæðum síu.</span><span class="sxs-lookup"><span data-stu-id="f7f05-106">You cannot use system grouping to filter on line level fields.</span></span>

## <a name="set-up-system-grouping-on-an-open-work-list"></a><span data-ttu-id="f7f05-107">Settu upp kerfisflokkun í opinn verkefnalista</span><span class="sxs-lookup"><span data-stu-id="f7f05-107">Set up system grouping on an open work list</span></span>
<span data-ttu-id="f7f05-108">Notið eftirfarandi skrefum til að setja upp kerfi flokkun á opnu verkefnalista.</span><span class="sxs-lookup"><span data-stu-id="f7f05-108">Use these steps to set up system grouping on an open work list.</span></span>

-   <span data-ttu-id="f7f05-109">Úr valmyndaratriði fartæki, veljið **Greiðslumáta: Óbeina** og **Kóða Verkþættinum: Birtingu opinna verkefnalistinn**.</span><span class="sxs-lookup"><span data-stu-id="f7f05-109">From a mobile device menu item, select **Mode: Indirect** and **Activity Code: Display open work list**.</span></span> <span data-ttu-id="f7f05-110">Eftirtaldir valkostir verða í boði.</span><span class="sxs-lookup"><span data-stu-id="f7f05-110">The following options become available.</span></span> <span data-ttu-id="f7f05-111">Þessir valkostir eru nauðsynleg fyrir flokkun á opnu verkefnalistinn kerfið.</span><span class="sxs-lookup"><span data-stu-id="f7f05-111">These options are required for system grouping on an open work list.</span></span> 

| <span data-ttu-id="f7f05-112">Valkostur</span><span class="sxs-lookup"><span data-stu-id="f7f05-112">Option</span></span>        | <span data-ttu-id="f7f05-113">lýsing</span><span class="sxs-lookup"><span data-stu-id="f7f05-113">Description</span></span>   | 
| ------------- | ------------- |
| <span data-ttu-id="f7f05-114">Leyfa flokkun kerfi</span><span class="sxs-lookup"><span data-stu-id="f7f05-114">Allow system grouping</span></span>   | <span data-ttu-id="f7f05-115">Gerir kerfið groping fyrir vinnustöðina valmyndaratriði listann.</span><span class="sxs-lookup"><span data-stu-id="f7f05-115">Enables system groping for a selected work list menu item.</span></span>| 
| <span data-ttu-id="f7f05-116">Kerfisflokkunarsvæði</span><span class="sxs-lookup"><span data-stu-id="f7f05-116">System grouping field</span></span>   | <span data-ttu-id="f7f05-117">Aðeins tiltækt ef **Leyfa kerfið vinnu** er stillt á **Já**.</span><span class="sxs-lookup"><span data-stu-id="f7f05-117">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="f7f05-118">Velja svæðið sem ákvarða hvernig tiltektarvinna verður flokkuð fyrir starfsmenn.</span><span class="sxs-lookup"><span data-stu-id="f7f05-118">Select the field that determines how picking work will be grouped for workers.</span></span> <span data-ttu-id="f7f05-119">Til dæmis, ef þú velur **ShipmentId** svæðinu starfsmaður verður skanna Sendingarkennið til að flokka vinnuna tiltekt.</span><span class="sxs-lookup"><span data-stu-id="f7f05-119">For example, if you select the **ShipmentId** field, the worker will scan the shipment ID to group the picking work.</span></span> <span data-ttu-id="f7f05-120">Öll vinna fyrir sendingunni er síðan úthlutað til starfsmanns.</span><span class="sxs-lookup"><span data-stu-id="f7f05-120">All work for the shipment is then assigned to the worker.</span></span> <span data-ttu-id="f7f05-121">Þessi reitur krefst þess að stofnað sé valmyndaratriði til að nota fyrirliggjandi vinnu sem er flokkuð af kerfinu.</span><span class="sxs-lookup"><span data-stu-id="f7f05-121">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="f7f05-122">Notkun á **Kerfið flokkun merki** til að upplýsa viðkomandi hvað skanna.</span><span class="sxs-lookup"><span data-stu-id="f7f05-122">Use the **System grouping label** field to inform the worker what to scan.</span></span> |
| <span data-ttu-id="f7f05-123">Kerfisflokkunarmerki</span><span class="sxs-lookup"><span data-stu-id="f7f05-123">System grouping label</span></span>   | <span data-ttu-id="f7f05-124">Aðeins tiltækt ef **Leyfa kerfið vinnu** er stillt á **Já**.</span><span class="sxs-lookup"><span data-stu-id="f7f05-124">Available only if **Allow system work** is set to **Yes**.</span></span> <span data-ttu-id="f7f05-125">Færið inn upplýsingar um starfsmann um hvað á að skanna þegar tiltekt vinnu er flokkuð.</span><span class="sxs-lookup"><span data-stu-id="f7f05-125">Enter information for the worker about what to scan when picking work is grouped.</span></span> <span data-ttu-id="f7f05-126">Til dæmis, ef verið er að nota reitinn **ShipmentId** til að flokka tiltektarvinnu eftir sendingu væri hægt að færa inn Sendingarkenni í reitinn.</span><span class="sxs-lookup"><span data-stu-id="f7f05-126">For example, if you use the **ShipmentId** field to group picking work by shipment, you might enter Shipment ID in the field.</span></span> <span data-ttu-id="f7f05-127">Þessi reitur krefst þess að stofnað sé valmyndaratriði til að nota fyrirliggjandi vinnu sem er flokkuð af kerfinu.</span><span class="sxs-lookup"><span data-stu-id="f7f05-127">This field requires that you create a menu item to use existing work that is grouped by the system.</span></span> <span data-ttu-id="f7f05-128">Einnig verður að velja reitinn til að flokka eftir í reitnum **Kerfisflokkunarsvæði**.</span><span class="sxs-lookup"><span data-stu-id="f7f05-128">You must also select the field to group by in the **System grouping** field.</span></span>|

