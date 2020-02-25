---
title: Stofna afbrigðaflokk
description: Þetta efni lýsir því hvernig á að búa til stærð, stíl eða litafbrigði fyrir vöru í Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: b9acd41c000b22e6c74b0d636a7f58917e4b5ac5
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001876"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="4d6da-103">Stofna afbrigðaflokk</span><span class="sxs-lookup"><span data-stu-id="4d6da-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4d6da-104">Þetta efni lýsir því hvernig á að búa til stærð, stíl eða litafbrigði fyrir vöru í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4d6da-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4d6da-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="4d6da-105">Overview</span></span>

<span data-ttu-id="4d6da-106">Dynamics 365 Commerce styður mörg afbrigði fyrir vörur.</span><span class="sxs-lookup"><span data-stu-id="4d6da-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="4d6da-107">Það er kjörið að setja upp afbrigðishópa fyrir mismunandi vöruflokka.</span><span class="sxs-lookup"><span data-stu-id="4d6da-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="4d6da-108">Til dæmis er hægt að búa til stærðarhóp fyrir stuttermaboli með stærðunum extra small, small, medium, large og extra large, eða búa til litahóp til að innihalda alla tiltæka liti á vöru.</span><span class="sxs-lookup"><span data-stu-id="4d6da-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="4d6da-109">Bæta skal við afbrigðishópum áður en afurðum er bætt við.</span><span class="sxs-lookup"><span data-stu-id="4d6da-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="4d6da-110">Í þessu efni verður stærðarhópur búinn til og stilltur.</span><span class="sxs-lookup"><span data-stu-id="4d6da-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="4d6da-111">Hægt er að nota svipaðar aðferðir til að bæta við og stilla stílahópa og litahópa.</span><span class="sxs-lookup"><span data-stu-id="4d6da-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="4d6da-112">Stofna stærðarflokk</span><span class="sxs-lookup"><span data-stu-id="4d6da-112">Create a size group</span></span>

<span data-ttu-id="4d6da-113">Til að stofna stærðarflokk, skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="4d6da-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="4d6da-114">Í Skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Afurðir og flokkar \> Afbrigðishópar \> Stærðarflokkar**.</span><span class="sxs-lookup"><span data-stu-id="4d6da-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="4d6da-115">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="4d6da-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="4d6da-116">Í reitinn **Stærðarflokkur** færirðu inn heiti fyrir stærðarflokkinn.</span><span class="sxs-lookup"><span data-stu-id="4d6da-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="4d6da-117">Í reitinn **Lýsing** ritarðu viðeigandi lýsingu.</span><span class="sxs-lookup"><span data-stu-id="4d6da-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="4d6da-118">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="4d6da-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="4d6da-119">Bættu eigindum við stærðarhópinn</span><span class="sxs-lookup"><span data-stu-id="4d6da-119">Add attributes to the size group</span></span>

<span data-ttu-id="4d6da-120">Fylgið eftirfarandi skrefum til að bæta eigindum við stærðarflokk.</span><span class="sxs-lookup"><span data-stu-id="4d6da-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="4d6da-121">Í Skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Afurðir og flokkar \> Afbrigðishópar \> Stærðarflokkar**</span><span class="sxs-lookup"><span data-stu-id="4d6da-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="4d6da-122">Í yfirlitssvæðinu velurðu stærðarflokk.</span><span class="sxs-lookup"><span data-stu-id="4d6da-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="4d6da-123">Undir **Línur stærðarflokks** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="4d6da-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="4d6da-124">Í reitinn **Stærð** færirðu inn streng sem sýnir stærð (til dæmis, „XL“).</span><span class="sxs-lookup"><span data-stu-id="4d6da-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="4d6da-125">Í reitinn **Stærðarheiti** slærðu inn heiti fyrir stærðina (til dæmis „Extra Large“).</span><span class="sxs-lookup"><span data-stu-id="4d6da-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="4d6da-126">Í reitinn **Áfyllingarþyngd** slærðu inn tölu sem sýnir áfyllingarþyngdina.</span><span class="sxs-lookup"><span data-stu-id="4d6da-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="4d6da-127">Í reitinn **Númer í strikamerki** slærðu inn númer sem táknar strikamerkið.</span><span class="sxs-lookup"><span data-stu-id="4d6da-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="4d6da-128">Í reitinn **Sýna röð** slærðu inn númer sem sýnir skjáröðunina.</span><span class="sxs-lookup"><span data-stu-id="4d6da-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="4d6da-129">Þegar þú hefur bætt við stærðum skaltu velja **Vista** á aðgerðarrúðunni.</span><span class="sxs-lookup"><span data-stu-id="4d6da-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="4d6da-130">Eftirfarandi mynd sýnir dæmi um stærðarhóp fyrir „stærðir á hversdagsskyrtum“.</span><span class="sxs-lookup"><span data-stu-id="4d6da-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![Stofna stærðarflokk](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="4d6da-132">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="4d6da-132">Additional resources</span></span>

[<span data-ttu-id="4d6da-133">Yfirlit afurðarupplýsinga</span><span class="sxs-lookup"><span data-stu-id="4d6da-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="4d6da-134">Setja upp smásöluafurðir</span><span class="sxs-lookup"><span data-stu-id="4d6da-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="4d6da-135">Afurðarvíddir</span><span class="sxs-lookup"><span data-stu-id="4d6da-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)
