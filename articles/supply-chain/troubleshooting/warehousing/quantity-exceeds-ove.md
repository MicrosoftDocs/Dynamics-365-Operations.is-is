---
title: Ekki er hægt að staðfesta sendingu vegna þess að magnið er hærra en hlutfall ofafhendingar
description: Ekki er hægt að staðfesta sendingu vegna þess að magnið er hærra en hlutfall ofafhendingar
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c9b5ba8dedb927ee049d7e53e9a666902f563f49
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938493"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a><span data-ttu-id="f32b5-103">Ekki er hægt að staðfesta sendingu vegna þess að magnið er hærra en hlutfall ofafhendingar</span><span class="sxs-lookup"><span data-stu-id="f32b5-103">You can't confirm a shipment because the quantity exceeds the overdelivery percentage</span></span>

<span data-ttu-id="f32b5-104">Villukóði WAX1687</span><span class="sxs-lookup"><span data-stu-id="f32b5-104">Error code: WAX1687</span></span>

## <a name="symptoms"></a><span data-ttu-id="f32b5-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="f32b5-105">Symptoms</span></span>

<span data-ttu-id="f32b5-106">Þegar reynt er að staðfesta sendingu sýnir kerfið eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="f32b5-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="f32b5-107">Ekki var hægt að staðfesta sendinguna fyrir farm %1 vegna þess að magnið fyrir vöru %2 fer yfir þá prósentu sem skilgreind er fyrir ofafhendingu.</span><span class="sxs-lookup"><span data-stu-id="f32b5-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for overdelivery.</span></span>

<span data-ttu-id="f32b5-108">Því er ekki hægt að staðfesta sendinguna fyrir farminn.</span><span class="sxs-lookup"><span data-stu-id="f32b5-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="f32b5-109">Orsök</span><span class="sxs-lookup"><span data-stu-id="f32b5-109">Cause</span></span>

<span data-ttu-id="f32b5-110">Magn hleðslunnar eða sendingarinnar hefur aðeins verið tínd að hluta til.</span><span class="sxs-lookup"><span data-stu-id="f32b5-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="f32b5-111">Magnið er í augnablikinu hærra en tiltektarmagn um prósentu sem er utan við leyfða ofafhendingu.</span><span class="sxs-lookup"><span data-stu-id="f32b5-111">The quantity currently exceeds the picked quantity by a percentage that is outside the allowed overdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="f32b5-112">Upplausn</span><span class="sxs-lookup"><span data-stu-id="f32b5-112">Resolution</span></span>

<span data-ttu-id="f32b5-113">Til að leysa þetta vandamál þarf að ljúka við eitt af eftirfarandi verkum:</span><span class="sxs-lookup"><span data-stu-id="f32b5-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="f32b5-114">Stillið magn hleðslulínunnar.</span><span class="sxs-lookup"><span data-stu-id="f32b5-114">Set the load line quantity.</span></span>
- <span data-ttu-id="f32b5-115">Stillið prósentu ofafhendingar.</span><span class="sxs-lookup"><span data-stu-id="f32b5-115">Set the overdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="f32b5-116">Stilla magn hleðslulínunnar</span><span class="sxs-lookup"><span data-stu-id="f32b5-116">Set the load line quantity</span></span>

<span data-ttu-id="f32b5-117">Til að stilla magn hleðslulínu skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="f32b5-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="f32b5-118">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="f32b5-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="f32b5-119">Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.</span><span class="sxs-lookup"><span data-stu-id="f32b5-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="f32b5-120">Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu fyrir vöruna sem fer umfram prósentu ofafhendingar.</span><span class="sxs-lookup"><span data-stu-id="f32b5-120">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="f32b5-121">Á flipanum **Línuupplýsingar** skal velja **Pöntun**.</span><span class="sxs-lookup"><span data-stu-id="f32b5-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="f32b5-122">Í reitnum **Magn** skal stilla gildið á tiltektarmagnið (þ.e. á gildið í **Magn stofnaðs verks**) þannig að staðfesta megi sendingu.</span><span class="sxs-lookup"><span data-stu-id="f32b5-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-overdelivery-percentage"></a><span data-ttu-id="f32b5-123">Stilla prósentu ofafhendingar</span><span class="sxs-lookup"><span data-stu-id="f32b5-123">Set the overdelivery percentage</span></span>

<span data-ttu-id="f32b5-124">Til að stilla vanafhendingarhlutfall skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="f32b5-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="f32b5-125">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="f32b5-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="f32b5-126">Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.</span><span class="sxs-lookup"><span data-stu-id="f32b5-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="f32b5-127">Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu fyrir vöruna sem fer umfram prósentu ofafhendingar.</span><span class="sxs-lookup"><span data-stu-id="f32b5-127">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="f32b5-128">Á flýtiflipanum **Línuupplýsingar** skal velja **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="f32b5-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="f32b5-129">Í reitnum **Ofafhending** skal stilla gildið á hærri prósentu sem nær utan um magnið sem er tínt gagnvart hleðslumagninu, þannig að staðfesting sendingar geti átt sér stað.</span><span class="sxs-lookup"><span data-stu-id="f32b5-129">In the **Overdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
