---
title: Ekki er hægt að staðfesta sendingu vegna þess að magnið er hærra en hlutfall vanafhendingar
description: Ekki er hægt að staðfesta sendingu vegna þess að magnið er hærra en hlutfall vanafhendingar
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm,WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 625003731485329b93f5f9454ccece580c889613
ms.sourcegitcommit: c2c6d687a89bc1534c029109315c23e92865b63b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/31/2021
ms.locfileid: "6123820"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a><span data-ttu-id="e4a99-103">Ekki er hægt að staðfesta sendingu vegna þess að magnið er hærra en hlutfall vanafhendingar</span><span class="sxs-lookup"><span data-stu-id="e4a99-103">You can't confirm a shipment because the quantity exceeds the underdelivery percentage</span></span>

<span data-ttu-id="e4a99-104">Villukóði WAX1686</span><span class="sxs-lookup"><span data-stu-id="e4a99-104">Error code: WAX1686</span></span>

## <a name="symptoms"></a><span data-ttu-id="e4a99-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="e4a99-105">Symptoms</span></span>

<span data-ttu-id="e4a99-106">Þegar reynt er að staðfesta sendingu sýnir kerfið eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="e4a99-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="e4a99-107">Ekki var hægt að staðfesta sendinguna fyrir farm %1 vegna þess að magnið fyrir vöru %2 fer yfir þá prósentu sem skilgreind er fyrir vanafhendingu.</span><span class="sxs-lookup"><span data-stu-id="e4a99-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for underdelivery.</span></span>

<span data-ttu-id="e4a99-108">Því er ekki hægt að staðfesta sendinguna fyrir farminn.</span><span class="sxs-lookup"><span data-stu-id="e4a99-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="e4a99-109">Orsök</span><span class="sxs-lookup"><span data-stu-id="e4a99-109">Cause</span></span>

<span data-ttu-id="e4a99-110">Magn hleðslunnar eða sendingarinnar hefur aðeins verið tínd að hluta til.</span><span class="sxs-lookup"><span data-stu-id="e4a99-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="e4a99-111">Magnið er í augnablikinu minna en tiltektarmagn um prósentu sem er utan við leyfða vanafhendingu.</span><span class="sxs-lookup"><span data-stu-id="e4a99-111">The quantity is currently less than the picked quantity by a percentage that is outside the allowed underdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="e4a99-112">Upplausn</span><span class="sxs-lookup"><span data-stu-id="e4a99-112">Resolution</span></span>

<span data-ttu-id="e4a99-113">Til að leysa þetta vandamál þarf að ljúka við eitt af eftirfarandi verkum:</span><span class="sxs-lookup"><span data-stu-id="e4a99-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="e4a99-114">Stillið magn hleðslulínunnar.</span><span class="sxs-lookup"><span data-stu-id="e4a99-114">Set the load line quantity.</span></span>
- <span data-ttu-id="e4a99-115">Stillið prósentu vanafhendingar.</span><span class="sxs-lookup"><span data-stu-id="e4a99-115">Set the underdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="e4a99-116">Stilla magn hleðslulínunnar</span><span class="sxs-lookup"><span data-stu-id="e4a99-116">Set the load line quantity</span></span>

<span data-ttu-id="e4a99-117">Til að stilla magn hleðslulínu skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="e4a99-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="e4a99-118">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="e4a99-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e4a99-119">Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.</span><span class="sxs-lookup"><span data-stu-id="e4a99-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="e4a99-120">Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu fyrir vöruna sem fer umfram prósentu vanafhendingar.</span><span class="sxs-lookup"><span data-stu-id="e4a99-120">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="e4a99-121">Á flipanum **Línuupplýsingar** skal velja **Pöntun**.</span><span class="sxs-lookup"><span data-stu-id="e4a99-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="e4a99-122">Í reitnum **Magn** skal stilla gildið á tiltektarmagnið (þ.e. á gildið í **Magn stofnaðs verks**) þannig að staðfesta megi sendingu.</span><span class="sxs-lookup"><span data-stu-id="e4a99-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-underdelivery-percentage"></a><span data-ttu-id="e4a99-123">Stilla prósentu vanafhendingar</span><span class="sxs-lookup"><span data-stu-id="e4a99-123">Set the underdelivery percentage</span></span>

<span data-ttu-id="e4a99-124">Til að stilla vanafhendingarhlutfall skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="e4a99-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="e4a99-125">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="e4a99-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="e4a99-126">Veljið hleðsluna sem ekki er hægt að staðfesta sendinguna fyrir.</span><span class="sxs-lookup"><span data-stu-id="e4a99-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="e4a99-127">Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu fyrir vöruna sem fer umfram prósentu vanafhendingar.</span><span class="sxs-lookup"><span data-stu-id="e4a99-127">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="e4a99-128">Á flýtiflipanum **Línuupplýsingar** skal velja **Almennt**.</span><span class="sxs-lookup"><span data-stu-id="e4a99-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="e4a99-129">Í reitnum **Vanafhending** skal stilla gildið á hærri prósentu sem nær utan um magnið sem er tínt gagnvart hleðslumagninu, þannig að staðfesting sendingar geti átt sér stað.</span><span class="sxs-lookup"><span data-stu-id="e4a99-129">In the **Underdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
