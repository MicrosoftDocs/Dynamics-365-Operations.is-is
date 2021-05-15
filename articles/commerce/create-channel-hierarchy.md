---
title: Stofna yfirlitsstigveldi rásar
description: Þetta efnisatriði lýsir hvernig á að stofna yfirlitsstigveldi rásar í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5df46de9dadfa0b7160a9b340ef36fdf963a0ad3
ms.sourcegitcommit: 6c2f5c3b038f696532c335e20b0fbafa155d6858
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951909"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="cc05c-103">Búa til skoðunarstigveldi rásar</span><span class="sxs-lookup"><span data-stu-id="cc05c-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="cc05c-104">Þetta efnisatriði lýsir hvernig á að stofna yfirlitsstigveldi rásar í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cc05c-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cc05c-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="cc05c-105">Overview</span></span>

<span data-ttu-id="cc05c-106">Yfirlitsstigveldi rásar er notað til að flokka og skipuleggja afurðir í flokka svo hægt sé að skoða afurðirnar á netinu eða á sölustöðum (POS).</span><span class="sxs-lookup"><span data-stu-id="cc05c-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="cc05c-107">Stofna yfirlitsstigveldi rásar</span><span class="sxs-lookup"><span data-stu-id="cc05c-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="cc05c-108">Fylgdu þessum skrefum til að stofna yfirlitsstigveldi rásar.</span><span class="sxs-lookup"><span data-stu-id="cc05c-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="cc05c-109">Í Skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Afurðir og flokkar \> Yfirlitsflokkar rásar**.</span><span class="sxs-lookup"><span data-stu-id="cc05c-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="cc05c-110">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="cc05c-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="cc05c-111">Í reitnum **Heiti** færirðu inn heiti.</span><span class="sxs-lookup"><span data-stu-id="cc05c-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="cc05c-112">Í reitinn **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="cc05c-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="cc05c-113">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="cc05c-113">Select **Create**.</span></span>
1. <span data-ttu-id="cc05c-114">Í aðgerðarglugganum skal velja **Nýr tegundarhnútur** til að búa til rótarhnút.</span><span class="sxs-lookup"><span data-stu-id="cc05c-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="cc05c-115">Í reitnum **Heiti** færirðu inn heiti.</span><span class="sxs-lookup"><span data-stu-id="cc05c-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="cc05c-116">Í reitinn **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="cc05c-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="cc05c-117">Í reitinn **Stutt heiti** slærðu inn stutt heiti.</span><span class="sxs-lookup"><span data-stu-id="cc05c-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="cc05c-118">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="cc05c-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="cc05c-119">Eftirfarandi mynd sýnir dæmi um rótarhnút.</span><span class="sxs-lookup"><span data-stu-id="cc05c-119">The following image shows a example root node.</span></span>

![Dæmi um rótarhnút](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="cc05c-121">Stofnun yfirlitsflokkahnúta</span><span class="sxs-lookup"><span data-stu-id="cc05c-121">Create navigation category nodes</span></span>

<span data-ttu-id="cc05c-122">Fylgdu þessum skrefum til að búa til fleiri yfirlitsflokkahnúta til að tákna afurðaflokka á rásinni.</span><span class="sxs-lookup"><span data-stu-id="cc05c-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="cc05c-123">Í yfirlitsglugganum velurðu yfirhnútinn sem þú vilt bæta flokknum við.</span><span class="sxs-lookup"><span data-stu-id="cc05c-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="cc05c-124">Í aðgerðarúðunni velurðu **Nýr tegundahnútur**.</span><span class="sxs-lookup"><span data-stu-id="cc05c-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="cc05c-125">Í reitnum **Heiti** færirðu inn heiti.</span><span class="sxs-lookup"><span data-stu-id="cc05c-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="cc05c-126">Í reitinn **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="cc05c-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="cc05c-127">Í reitinn **Stutt heiti** slærðu inn stutt heiti.</span><span class="sxs-lookup"><span data-stu-id="cc05c-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="cc05c-128">Í reitinn **Sýna röð** slærðu inn röð birtingar (valfrjálst).</span><span class="sxs-lookup"><span data-stu-id="cc05c-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="cc05c-129">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="cc05c-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="cc05c-130">Eftirfarandi mynd sýnir dæmi um yfirlitsstigveldi rásar sem er lokið.</span><span class="sxs-lookup"><span data-stu-id="cc05c-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Dæmi um rásarstigveldi](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="cc05c-132">Bæta afurðum við flokkshnúta</span><span class="sxs-lookup"><span data-stu-id="cc05c-132">Add products to category nodes</span></span>

<span data-ttu-id="cc05c-133">Fylgdu þessum skrefum til að bæta afurðum við flokkahnúta.</span><span class="sxs-lookup"><span data-stu-id="cc05c-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="cc05c-134">Velja flokkshnút.</span><span class="sxs-lookup"><span data-stu-id="cc05c-134">Select a category node.</span></span>
1. <span data-ttu-id="cc05c-135">Undir **Afurðir** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="cc05c-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="cc05c-136">Finndu nýju afurðirnar sem þú vilt bæta við með afurðarnúmeri eða afurðarheiti og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cc05c-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="cc05c-137">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="cc05c-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="cc05c-138">Að bæta afurðum við hnút inni í stigveldi rásarinnar dugar ekki til þess að afurðirnar birtist á valinni rás, einnig verður að tengja afurðirnar við rás.</span><span class="sxs-lookup"><span data-stu-id="cc05c-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a channel.</span></span> <span data-ttu-id="cc05c-139">Frekari upplýsingar um vöruúrval er að finna í [Stjórnun vöruúrvals](assortments.md).</span><span class="sxs-lookup"><span data-stu-id="cc05c-139">For more information on assortments, see [Assortment management](assortments.md).</span></span>

<span data-ttu-id="cc05c-140">Eftirfarandi mynd sýnir dæmi um hnút með afurðum sem er bætt við.</span><span class="sxs-lookup"><span data-stu-id="cc05c-140">The following image shows an example node with products added.</span></span>

![Afurðum bætt við flokkshnút](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="cc05c-142">Bættu afurðareigindahópum við flokkshnúta</span><span class="sxs-lookup"><span data-stu-id="cc05c-142">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="cc05c-143">Það verður að búa til eigindahópa áður en þú getur bætt þeim við hnút innan yfirlitsstigveldi rásar.</span><span class="sxs-lookup"><span data-stu-id="cc05c-143">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="cc05c-144">Til að bæta afurð og eigindahóp við flokkshnút skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="cc05c-144">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="cc05c-145">Velja flokkshnút.</span><span class="sxs-lookup"><span data-stu-id="cc05c-145">Select a category node.</span></span>
1. <span data-ttu-id="cc05c-146">Undir **Afurðaeigindahópur** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="cc05c-146">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="cc05c-147">Finndu eigindahópa sem þú vilt bæta við og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="cc05c-147">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="cc05c-148">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="cc05c-148">On the action pane, select **Save**.</span></span>

<span data-ttu-id="cc05c-149">Eftirfarandi mynd sýnir dæmi um hnút með afurðareigindir sem er bætt við.</span><span class="sxs-lookup"><span data-stu-id="cc05c-149">The following image shows a sample node with product attribute groups added.</span></span>

![Eigindaflokkar afurðar á hnút](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="cc05c-151">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="cc05c-151">Additional resources</span></span>

[<span data-ttu-id="cc05c-152">Setja upp úrval</span><span class="sxs-lookup"><span data-stu-id="cc05c-152">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="cc05c-153">Stjórna eigindum og eigindahópum</span><span class="sxs-lookup"><span data-stu-id="cc05c-153">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
