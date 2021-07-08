---
title: Sléttun aukastafa á uppfærslu efnislegs magns er röng
description: Þegar fylgiseðill er búinn til inniheldur hleðslan á útleið magn sem passar ekki við nákvæmni aukastafa sem er skilgreind í einingunni.
author: GalynaFedorova
ms.date: 5/31/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadPlanningListPage_WHSSalesPackingSlipPost, WHSLoadTable_WHSSalesPackingSlipPost
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 1e63440834f516879aa8ad711bd789e62b0ee993
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248787"
---
# <a name="decimal-rounding-of-the-physical-updating-quantity-is-incorrect"></a><span data-ttu-id="8fd83-103">Sléttun aukastafa á uppfærslu efnislegs magns er röng</span><span class="sxs-lookup"><span data-stu-id="8fd83-103">Decimal rounding of the physical updating quantity is incorrect</span></span>

<span data-ttu-id="8fd83-104">Villukóði SYS19589</span><span class="sxs-lookup"><span data-stu-id="8fd83-104">Error code: SYS19589</span></span>

## <a name="symptoms"></a><span data-ttu-id="8fd83-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="8fd83-105">Symptoms</span></span>

<span data-ttu-id="8fd83-106">Þegar fylgiseðill er búinn til inniheldur hleðslan á útleið magn sem passar ekki við nákvæmni aukastafa sem er skilgreind í einingunni.</span><span class="sxs-lookup"><span data-stu-id="8fd83-106">When you generate a packing slip, the outbound load contains a quantity that doesn't match the decimal precision that is defined in the unit.</span></span>

<span data-ttu-id="8fd83-107">Þegar reynt er að búa til fylgiseðil sýnir kerfið eftirfarandi villuboð:</span><span class="sxs-lookup"><span data-stu-id="8fd83-107">When you try to generate a packing slip, the system shows the following error message:</span></span>

> <span data-ttu-id="8fd83-108">Sléttun aukastafa á efnislegu uppfærslumagni í einingu %1 er röng.</span><span class="sxs-lookup"><span data-stu-id="8fd83-108">Decimal rounding of the physical updating quantity in the unit %1 is incorrect.</span></span>

<span data-ttu-id="8fd83-109">Því er ekki hægt að búa til fylgiseðil fyrir hleðsluna.</span><span class="sxs-lookup"><span data-stu-id="8fd83-109">Therefore, you can't generate the packing slip for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="8fd83-110">Orsök</span><span class="sxs-lookup"><span data-stu-id="8fd83-110">Cause</span></span>

<span data-ttu-id="8fd83-111">Kerfið metur hvort sléttun aukastafa á magni sendingar samsvari nákvæmni aukastafa sem er skilgreind fyrir sendingareininguna.</span><span class="sxs-lookup"><span data-stu-id="8fd83-111">The system evaluates whether the decimal rounding of the shipping quantity corresponds to the decimal precision that is defined for the shipping unit.</span></span> <span data-ttu-id="8fd83-112">Þegar kerfið sléttar magn sendingar í tiltekinn fjölda aukastafa, ef það finnur út að sléttað magn sendingar passar ekki við raunverulegt magn sendingar, er ekki hægt að búa til fylgiseðil.</span><span class="sxs-lookup"><span data-stu-id="8fd83-112">When the system rounds the shipping quantity to the specified number of decimal places, if it finds that the rounded shipping quantity doesn't match the actual shipping quantity, you can't generate the packing slip.</span></span> <span data-ttu-id="8fd83-113">Þetta vandamál gæti til dæmis komið upp ef sölumagnið er 1,75 kíló (kg) en nákvæmni aukastafa er stillt á *1*.</span><span class="sxs-lookup"><span data-stu-id="8fd83-113">For example, this issue might occur if the sales quantity is 1.75 kilograms (kg), but the decimal precision is set to *1*.</span></span>

## <a name="resolution"></a><span data-ttu-id="8fd83-114">Lausn</span><span class="sxs-lookup"><span data-stu-id="8fd83-114">Resolution</span></span>

<span data-ttu-id="8fd83-115">Hleðslan eða sendingin er sem stendur í stöðu þar sem myndun fylgiseðils mistekst.</span><span class="sxs-lookup"><span data-stu-id="8fd83-115">The load or shipment is currently in a state where packing slip generation fails.</span></span> <span data-ttu-id="8fd83-116">Til að leysa þetta vandamál þarf að ljúka við eitt af eftirfarandi verkum:</span><span class="sxs-lookup"><span data-stu-id="8fd83-116">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="8fd83-117">Farið yfir hleðslulínurnar og gerið leiðréttingar til að tryggja að hægt sé að umreikna magnið án aukastafa og annarra sléttunarvandamála.</span><span class="sxs-lookup"><span data-stu-id="8fd83-117">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>
- <span data-ttu-id="8fd83-118">Farið yfir hleðslulínurnar og gerið leiðréttingar til að tryggja að einingin og magnið séu í takt við nákvæmni aukastafa í einingunni.</span><span class="sxs-lookup"><span data-stu-id="8fd83-118">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-quantity-can-be-cleanly-converted-without-decimal-numbers-and-any-other-rounding-issues"></a><span data-ttu-id="8fd83-119">Farið yfir hleðslulínurnar og gerið leiðréttingar til að tryggja að hægt sé að umreikna magnið án aukastafa og annarra sléttunarvandamála</span><span class="sxs-lookup"><span data-stu-id="8fd83-119">Review your load lines, and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues</span></span>

<span data-ttu-id="8fd83-120">Notið eftirfarandi leið til að fara yfir hleðslulínurnar og gera leiðréttingar til að tryggja að hægt sé að umreikna magnið án aukastafa og annarra sléttunarvandamála.</span><span class="sxs-lookup"><span data-stu-id="8fd83-120">Use the following procedure to review your load lines and make adjustments to ensure that the quantity can be cleanly converted without decimal numbers and any other rounding issues.</span></span>

1. <span data-ttu-id="8fd83-121">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="8fd83-121">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="8fd83-122">Veljið hleðsluna sem ekki er hægt að mynda fylgiseðilinn fyrir.</span><span class="sxs-lookup"><span data-stu-id="8fd83-122">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="8fd83-123">Á aðgerðasvæðinu, í flipanum  **Senda og móttaka**, í flokknum  **Bakfæra**, skal velja  **Bakfæra staðfestingu sendingar**.</span><span class="sxs-lookup"><span data-stu-id="8fd83-123">On the Action Pane, on the **Ship and receive** tab, in the **Reverse** group, select **Reverse shipment confirmation**.</span></span>
1. <span data-ttu-id="8fd83-124">Í flipanum  **Hleðslulínur** skal velja hleðslulínu fyrir vöruna þar sem vandamál kemur upp.</span><span class="sxs-lookup"><span data-stu-id="8fd83-124">On the **Load lines** tab, select the load line for the item that causes an issue.</span></span>
1. <span data-ttu-id="8fd83-125">Veljið **Minnka tiltektarmagn** til að laga tiltektarmagnið.</span><span class="sxs-lookup"><span data-stu-id="8fd83-125">Select **Reduce picked quantity** to adjust the picked quantity.</span></span>
1. <span data-ttu-id="8fd83-126">Í flipanum  **Línuupplýsingar** skal velja **Pöntun**.</span><span class="sxs-lookup"><span data-stu-id="8fd83-126">On the  **Line details** tab, select **Order**.</span></span>
1. <span data-ttu-id="8fd83-127">Stillið reitinn **Magn** á tiltektarmagnið (þ.e. gildið í reitnum **Magn stofnaðs verks**) svo hægt sé að halda áfram með myndun fylgiseðils.</span><span class="sxs-lookup"><span data-stu-id="8fd83-127">Set the **Quantity** field to the picked quantity (that is, the value of the **Work created quantity** field), so that packing slip generation can proceed.</span></span>

### <a name="review-your-load-lines-and-make-adjustments-to-ensure-that-the-unit-and-quantity-are-aligned-with-the-decimal-precision-of-the-unit"></a><span data-ttu-id="8fd83-128">Farið yfir hleðslulínurnar og gerið leiðréttingar til að tryggja að einingin og magnið séu í takt við nákvæmni aukastafa í einingunni</span><span class="sxs-lookup"><span data-stu-id="8fd83-128">Review your load lines, and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit</span></span>

<span data-ttu-id="8fd83-129">Notið eftirfarandi aðferðir til að fara yfir hleðslulínurnar og gera leiðréttingar til að tryggja að einingin og magnið séu í takt við nákvæmni aukastafa í einingunni.</span><span class="sxs-lookup"><span data-stu-id="8fd83-129">Use the following procedure to review your load lines and make adjustments to ensure that the unit and quantity are aligned with the decimal precision of the unit.</span></span>

1. <span data-ttu-id="8fd83-130">Farðu í **Vöruhúsakerfi \> Hleðslur \> Allar hleðslur**.</span><span class="sxs-lookup"><span data-stu-id="8fd83-130">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="8fd83-131">Veljið hleðsluna sem ekki er hægt að mynda fylgiseðilinn fyrir.</span><span class="sxs-lookup"><span data-stu-id="8fd83-131">Select the load that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="8fd83-132">Í flýtiflipanum **Hleðslulínur** skal velja hleðslulínu fyrir vöruna þar sem vandamál kemur upp.</span><span class="sxs-lookup"><span data-stu-id="8fd83-132">On the **Load lines** FastTab, select the load line for the item that causes an issue.</span></span> <span data-ttu-id="8fd83-133">Gera skal athugasemd um gildið í reitunum **Magn** og **Eining**.</span><span class="sxs-lookup"><span data-stu-id="8fd83-133">Make a note of the value of the **Quantity** and **Unit** fields.</span></span>
1. <span data-ttu-id="8fd83-134">Farið í **Fyrirtækisstjórnun \> Einingar \> Einingar**.</span><span class="sxs-lookup"><span data-stu-id="8fd83-134">Go to **Organization administration \> Units \> Units**.</span></span>
1. <span data-ttu-id="8fd83-135">Veljið eininguna sem ekki er hægt að búa til fylgiseðil fyrir.</span><span class="sxs-lookup"><span data-stu-id="8fd83-135">Select the unit that the packing slip can't be generated for.</span></span>
1. <span data-ttu-id="8fd83-136">Stillið gildið í reitnum **Nákvæmni aukastafa** eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="8fd83-136">Adjust the value of the **Decimal precision** field as required.</span></span>
