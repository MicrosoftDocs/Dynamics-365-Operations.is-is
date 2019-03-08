---
title: Staðfesting einingartiltektar
description: Í þessu efnisatriði er því lýst hvernig eigi að setja upp og nota staðfestingu einingartiltektar úr fartæki.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b85414dd1385dc3d8c97632eaaeb252759590ff
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/29/2019
ms.locfileid: "349631"
---
# <a name="piece-picking-confirmation"></a><span data-ttu-id="3b123-103">Staðfesting einingartiltektar</span><span class="sxs-lookup"><span data-stu-id="3b123-103">Piece picking confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b123-104">Einingatiltekt gerir þér kleift að staðfesta hverja birgðaeiningu í tiltektar- eða talningarvinnu í fartæki.</span><span class="sxs-lookup"><span data-stu-id="3b123-104">Piece picking allows you to confirm each piece of inventory through picking or counting work on a mobile device.</span></span> <span data-ttu-id="3b123-105">Í tiltekt er hægt að staðfesta verkmagn sem fara þarf fram upp að því marki sem tilgreint er í tiltektarverki.</span><span class="sxs-lookup"><span data-stu-id="3b123-105">For picks, you can confirm the quantity of work to be processed up to the quantity that is specified on work to be picked.</span></span> <span data-ttu-id="3b123-106">Í talningarvinnu geturðu skannað birgðirnar sem þú ert að telja og fylgst með heildarmagninu.</span><span class="sxs-lookup"><span data-stu-id="3b123-106">For counting work, you can scan the inventory that you are counting and track the total amount.</span></span>

<span data-ttu-id="3b123-107">Þegar einingatiltekt er virkjuð er staðfesting afurðar sjálfkrafa valin.</span><span class="sxs-lookup"><span data-stu-id="3b123-107">When you enable piece picking, product confirmation is automatically selected.</span></span> <span data-ttu-id="3b123-108">Fyrir verktegundina tiltekt er hámarksfjöldi eininga virkjaður.</span><span class="sxs-lookup"><span data-stu-id="3b123-108">For work-type picks, a maximum number of pieces is enabled.</span></span> <span data-ttu-id="3b123-109">Það gerir þér kleift að setja hámark á fjölda eininga sem þarf að staðfesta í verkferlinu.</span><span class="sxs-lookup"><span data-stu-id="3b123-109">This allows you to set a maximum to the number of pieces that must be confirmed during the work process.</span></span> <span data-ttu-id="3b123-110">Hámarksmagnið byggist á núverandi verkeiningu sem verið er að vinna.</span><span class="sxs-lookup"><span data-stu-id="3b123-110">The maximum quantity is based on the current work unit that is being processed.</span></span> <span data-ttu-id="3b123-111">Verk af gerðinni talning leyfir ekki hámark.</span><span class="sxs-lookup"><span data-stu-id="3b123-111">The counting work type does not allow a maximum.</span></span>

<span data-ttu-id="3b123-112">Einnig er hægt að nota magn og mælieiningu (UOM) sem tengist skönnuðu strikamerki.</span><span class="sxs-lookup"><span data-stu-id="3b123-112">You can also use the quantity and unit of measure (UOM) that is associated with a scanned bar code.</span></span> <span data-ttu-id="3b123-113">Þetta virkar fyrir móttöku á innflæði, þar á meðal móttöku á blandaðri númeraplötu, vöru í innkaupapöntun, vöru í flutningspöntun og hleðsluvöru.</span><span class="sxs-lookup"><span data-stu-id="3b123-113">This will work for receiving on inbound flows including mixed license plate receiving, purchase order item, transfer order item, and load item.</span></span> <span data-ttu-id="3b123-114">Þetta virkar einnig fyrir einingatiltekt þar sem skönnun á strikamerki bætir magninu við heildarfjölda staðfestra eining sem fara úr mælieiningu á strikamerkinu í verkeininguna.</span><span class="sxs-lookup"><span data-stu-id="3b123-114">It also works for piece picking where scanning the bar code will add the quantity to the total number of confirmed pieces converting between the UOM on the bar code and the work unit.</span></span> <span data-ttu-id="3b123-115">Ef talning á mælieiningu á strikamerki staðfestir að magnið er leyfilegt fyrir talningu á röðunarflokknum, er magninu bætt við heildarfjölda.</span><span class="sxs-lookup"><span data-stu-id="3b123-115">If, when counting the UOM on the bar code, it is confirmed that the quantity is allowed for counting on the sequence group, the quantity will be added to the total count.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="3b123-116">Þar sem það á við</span><span class="sxs-lookup"><span data-stu-id="3b123-116">Where it applies</span></span>

<span data-ttu-id="3b123-117">Einingatiltekt gengur fyrir alla talningavinnu og fyrir fyrstu tiltekt í öllum tegundum vinnu.</span><span class="sxs-lookup"><span data-stu-id="3b123-117">Piece picking works for all counting work and for the initial pick for any type of work.</span></span> <span data-ttu-id="3b123-118">Einingatiltekt á ekki við ef vörunni er stjórnað af raðnúmerum eða ef um er að ræða framleiðslutiltekt eða kanban-tiltekt úr númeraplötustaðsetningu og varan er stillt á millistigsvigtun.</span><span class="sxs-lookup"><span data-stu-id="3b123-118">Piece picking does not apply if the item is controlled by serial numbers or if it is a production or kanban pick from a license plate (LP) location and the item is set to staging.</span></span>

## <a name="set-up-piece-picking"></a><span data-ttu-id="3b123-119">Uppsetning einingatiltektar</span><span class="sxs-lookup"><span data-stu-id="3b123-119">Set up piece picking</span></span>

1.  <span data-ttu-id="3b123-120">Í valmyndaratriði fartækis skaltu opna uppsetningarskjámyndina fyrir vinnustaðfestingu: Vöruhúsakerfi > **Vöruhúsakerfi** > **Uppsetning** > **Fartæki** > **Valmyndaratriði fartækis**.</span><span class="sxs-lookup"><span data-stu-id="3b123-120">On a mobile device menu item, open the setup form for work confirmation: Warehouse management > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span> 
2. <span data-ttu-id="3b123-121">Opnaðu Uppsetning vinnustaðfestingar í valmyndaratriði fartækis.</span><span class="sxs-lookup"><span data-stu-id="3b123-121">From the mobile device menu item, open Work confirmation setup.</span></span>

<span data-ttu-id="3b123-122">Eftirfarandi valkostir verða tiltækar til vals þegar gerð vinnu er tiltekt eða talning.</span><span class="sxs-lookup"><span data-stu-id="3b123-122">The following options become available for selection when the work type is pick or counting.</span></span>


|           <span data-ttu-id="3b123-123">Valkostur</span><span class="sxs-lookup"><span data-stu-id="3b123-123">Option</span></span>           |                                                                            <span data-ttu-id="3b123-124">lýsing</span><span class="sxs-lookup"><span data-stu-id="3b123-124">Description</span></span>                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b123-125">Staðfesting einingartiltektar</span><span class="sxs-lookup"><span data-stu-id="3b123-125">Piece picking confirmation</span></span> | <span data-ttu-id="3b123-126">Tiltækt fyrir tínslu og talningu.</span><span class="sxs-lookup"><span data-stu-id="3b123-126">Available for pick and counting work types.</span></span> <span data-ttu-id="3b123-127">Staðfesting vöru er sjálfkrafa valin.</span><span class="sxs-lookup"><span data-stu-id="3b123-127">Product confirmation is automatically selected.</span></span> <span data-ttu-id="3b123-128">Gerir kleift að staðfesta hverja birgðaeiningu úr fartækinu.</span><span class="sxs-lookup"><span data-stu-id="3b123-128">Allows you to confirm each piece of inventory from the mobile device.</span></span> |
|  <span data-ttu-id="3b123-129">Hámarksfjöldi eininga</span><span class="sxs-lookup"><span data-stu-id="3b123-129">Maximum number of pieces</span></span>  |                   <span data-ttu-id="3b123-130">Tiltækt fyrir tiltektarvinnu ef staðfesting einingatiltektar er virkjuð.</span><span class="sxs-lookup"><span data-stu-id="3b123-130">Available for pick work if piece picking confirmation is enabled.</span></span> <span data-ttu-id="3b123-131">Stillir takmörkun á fjölda eininga sem þarf að staðfesta.</span><span class="sxs-lookup"><span data-stu-id="3b123-131">Sets a limit to the number of pieces that you must confirm.</span></span>                   |

