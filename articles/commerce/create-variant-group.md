---
title: Stofna afbrigðaflokk
description: Þetta efnisatriði lýsir því hvernig á að stofna stærð, stíl eða litaafbrigðaflokk fyrir afurð í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailSizeGroupTable, ConfigGroupIdLookup, RetailStyleGroupTable
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 0462958d8225de145a8d886b096f96cd3f2cb5c5
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799542"
---
# <a name="create-a-variant-group"></a><span data-ttu-id="eb2b0-103">Búa til afbrigðaflokk</span><span class="sxs-lookup"><span data-stu-id="eb2b0-103">Create a variant group</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="eb2b0-104">Þetta efnisatriði lýsir því hvernig á að stofna stærð, stíl eða litaafbrigðaflokk fyrir afurð í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-104">This topic describes how to create a size, style, or color variant group for a product in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="eb2b0-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="eb2b0-105">Overview</span></span>

<span data-ttu-id="eb2b0-106">Dynamics 365 Commerce styður mörg afbrigði fyrir vörur.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-106">Dynamics 365 Commerce supports multiple variants for products.</span></span> <span data-ttu-id="eb2b0-107">Það er kjörið að setja upp afbrigðishópa fyrir mismunandi vöruflokka.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-107">It is ideal to set up variant groups for different product categories.</span></span> <span data-ttu-id="eb2b0-108">Til dæmis er hægt að búa til stærðarhóp fyrir stuttermaboli með stærðunum extra small, small, medium, large og extra large, eða búa til litahóp til að innihalda alla tiltæka liti á vöru.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-108">For example, a size group can be created for t-shirts with sizes extra small, small, medium, large, and extra large, or a color group could be created to include all available colors of a product.</span></span> <span data-ttu-id="eb2b0-109">Bæta skal við afbrigðishópum áður en afurðum er bætt við.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-109">Variant groups should be added before products are added.</span></span>

<span data-ttu-id="eb2b0-110">Í þessu efni verður stærðarhópur búinn til og stilltur.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-110">In this topic, a size group will be created and configured.</span></span> <span data-ttu-id="eb2b0-111">Hægt er að nota svipaðar aðferðir til að bæta við og stilla stílahópa og litahópa.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-111">Similar procedures can be used for adding and configuring style groups and color groups.</span></span>

## <a name="create-a-size-group"></a><span data-ttu-id="eb2b0-112">Stofna stærðarflokk</span><span class="sxs-lookup"><span data-stu-id="eb2b0-112">Create a size group</span></span>

<span data-ttu-id="eb2b0-113">Til að stofna stærðarflokk, skal fylgja eftirfarandi skrefum.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-113">To create a size group, follow these steps.</span></span>
 
1. <span data-ttu-id="eb2b0-114">Í Skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Afurðir og flokkar \> Afbrigðishópar \> Stærðarflokkar**.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-114">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**.</span></span>
1. <span data-ttu-id="eb2b0-115">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-115">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="eb2b0-116">Í reitinn **Stærðarflokkur** færirðu inn heiti fyrir stærðarflokkinn.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-116">In the **Size group** box, enter a name for the size group.</span></span>
1. <span data-ttu-id="eb2b0-117">Í reitinn **Lýsing** ritarðu viðeigandi lýsingu.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-117">In the **Description** box, enter an appropriate description.</span></span>
1. <span data-ttu-id="eb2b0-118">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="eb2b0-118">On the action pane, select **Save**.</span></span>

## <a name="add-attributes-to-the-size-group"></a><span data-ttu-id="eb2b0-119">Bættu eigindum við stærðarhópinn</span><span class="sxs-lookup"><span data-stu-id="eb2b0-119">Add attributes to the size group</span></span>

<span data-ttu-id="eb2b0-120">Fylgið eftirfarandi skrefum til að bæta eigindum við stærðarflokk.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-120">To add attributes to a size group, follow these steps.</span></span>

1. <span data-ttu-id="eb2b0-121">Í Skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Afurðir og flokkar \> Afbrigðishópar \> Stærðarflokkar**</span><span class="sxs-lookup"><span data-stu-id="eb2b0-121">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Variant groups \> Size groups**</span></span>
1. <span data-ttu-id="eb2b0-122">Í yfirlitssvæðinu velurðu stærðarflokk.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-122">In the navigation pane, select a size group.</span></span>
1. <span data-ttu-id="eb2b0-123">Undir **Línur stærðarflokks** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-123">Under **Size group lines**, select **Add**.</span></span>
1. <span data-ttu-id="eb2b0-124">Í reitinn **Stærð** færirðu inn streng sem sýnir stærð (til dæmis, „XL“).</span><span class="sxs-lookup"><span data-stu-id="eb2b0-124">In the **Size** box, enter a string representing the size (for example, "XL").</span></span>
1. <span data-ttu-id="eb2b0-125">Í reitinn **Stærðarheiti** slærðu inn heiti fyrir stærðina (til dæmis „Extra Large“).</span><span class="sxs-lookup"><span data-stu-id="eb2b0-125">In the **Size name** box, enter a name for the size (for example, "Extra Large").</span></span>
1. <span data-ttu-id="eb2b0-126">Í reitinn **Áfyllingarþyngd** slærðu inn tölu sem sýnir áfyllingarþyngdina.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-126">In the **Replenishment weight** box, enter a number representing the replenishment weight.</span></span>
1. <span data-ttu-id="eb2b0-127">Í reitinn **Númer í strikamerki** slærðu inn númer sem táknar strikamerkið.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-127">In the **Number in bar code** box, enter a number representing the bar code.</span></span>
1. <span data-ttu-id="eb2b0-128">Í reitinn **Sýna röð** slærðu inn númer sem sýnir skjáröðunina.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-128">In the **Display order** box, enter a number representing the display order.</span></span>
1. <span data-ttu-id="eb2b0-129">Þegar þú hefur bætt við stærðum skaltu velja **Vista** á aðgerðarrúðunni.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-129">When finished adding sizes, select **Save** on the action pane.</span></span>

<span data-ttu-id="eb2b0-130">Eftirfarandi mynd sýnir dæmi um stærðarhóp fyrir „stærðir á hversdagsskyrtum“.</span><span class="sxs-lookup"><span data-stu-id="eb2b0-130">The following image shows an example of a size group for "casual shirt sizes".</span></span>

![Stofna stærðarflokk](media/create-variant-group.png)

## <a name="additional-resources"></a><span data-ttu-id="eb2b0-132">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="eb2b0-132">Additional resources</span></span>

[<span data-ttu-id="eb2b0-133">Yfirlit afurðarupplýsinga</span><span class="sxs-lookup"><span data-stu-id="eb2b0-133">Product information overview</span></span>](../supply-chain/pim/product-information.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="eb2b0-134">Setja upp smásöluafurðir</span><span class="sxs-lookup"><span data-stu-id="eb2b0-134">Set up retail products</span></span>](set-up-retail-products.md)

[<span data-ttu-id="eb2b0-135">Afurðarvíddir</span><span class="sxs-lookup"><span data-stu-id="eb2b0-135">Product dimensions</span></span>](../supply-chain/pim/product-dimensions.md?toc=/dynamics365/commerce/toc.json)


[!INCLUDE[footer-include](../includes/footer-banner.md)]