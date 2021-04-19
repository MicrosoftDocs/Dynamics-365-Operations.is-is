---
title: Stofna yfirlitsstigveldi rásar
description: Þetta efnisatriði lýsir hvernig á að stofna yfirlitsstigveldi rásar í Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 01/27/2020
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
ms.openlocfilehash: 358f3d40c7a21184c20da342d6b2bf72dd4e7bbd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795836"
---
# <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="ce6b3-103">Búa til skoðunarstigveldi rásar</span><span class="sxs-lookup"><span data-stu-id="ce6b3-103">Create a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="ce6b3-104">Þetta efnisatriði lýsir hvernig á að stofna yfirlitsstigveldi rásar í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-104">This topic describes how to create a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="ce6b3-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="ce6b3-105">Overview</span></span>

<span data-ttu-id="ce6b3-106">Yfirlitsstigveldi rásar er notað til að flokka og skipuleggja afurðir í flokka svo hægt sé að skoða afurðirnar á netinu eða á sölustöðum (POS).</span><span class="sxs-lookup"><span data-stu-id="ce6b3-106">A channel navigation hierarchy is used to group and organize products into categories so that the products can be browsed online or in point of sale (POS).</span></span>

## <a name="create-a-channel-navigation-hierarchy"></a><span data-ttu-id="ce6b3-107">Stofna yfirlitsstigveldi rásar</span><span class="sxs-lookup"><span data-stu-id="ce6b3-107">Create a channel navigation hierarchy</span></span>

<span data-ttu-id="ce6b3-108">Fylgdu þessum skrefum til að stofna yfirlitsstigveldi rásar.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-108">To create a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="ce6b3-109">Í Skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Afurðir og flokkar \> Yfirlitsflokkar rásar**.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-109">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Channel navigation categories**.</span></span>
1. <span data-ttu-id="ce6b3-110">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="ce6b3-111">Í reitnum **Heiti** færirðu inn heiti.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-111">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="ce6b3-112">Í reitinn **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-112">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="ce6b3-113">Velja **Stofna**.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-113">Select **Create**.</span></span>
1. <span data-ttu-id="ce6b3-114">Í aðgerðarglugganum skal velja **Nýr tegundarhnútur** til að búa til rótarhnút.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-114">On the action pane, select **New category node** to create a root node.</span></span>
1. <span data-ttu-id="ce6b3-115">Í reitnum **Heiti** færirðu inn heiti.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-115">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="ce6b3-116">Í reitinn **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-116">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="ce6b3-117">Í reitinn **Stutt heiti** slærðu inn stutt heiti.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-117">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="ce6b3-118">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="ce6b3-118">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ce6b3-119">Eftirfarandi mynd sýnir dæmi um rótarhnút.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-119">The following image shows a example root node.</span></span>

![Dæmi um rótarhnút](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a><span data-ttu-id="ce6b3-121">Stofnun yfirlitsflokkahnúta</span><span class="sxs-lookup"><span data-stu-id="ce6b3-121">Create navigation category nodes</span></span>

<span data-ttu-id="ce6b3-122">Fylgdu þessum skrefum til að búa til fleiri yfirlitsflokkahnúta til að tákna afurðaflokka á rásinni.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-122">To create any additional navigation category nodes to represent the product categories on the channel, follow these steps.</span></span>

1. <span data-ttu-id="ce6b3-123">Í yfirlitsglugganum velurðu yfirhnútinn sem þú vilt bæta flokknum við.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-123">In the navigation pane, select the parent node to add a category to.</span></span>
1. <span data-ttu-id="ce6b3-124">Í aðgerðarúðunni velurðu **Nýr tegundahnútur**.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-124">On the action pane, select **New category node**.</span></span>
1. <span data-ttu-id="ce6b3-125">Í reitnum **Heiti** færirðu inn heiti.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-125">In the **Name** box, enter a name.</span></span>
1. <span data-ttu-id="ce6b3-126">Í reitinn **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-126">In the **Description** box, enter a description.</span></span>
1. <span data-ttu-id="ce6b3-127">Í reitinn **Stutt heiti** slærðu inn stutt heiti.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-127">In the **Friendly name** box, enter a friendly name.</span></span>
1. <span data-ttu-id="ce6b3-128">Í reitinn **Sýna röð** slærðu inn röð birtingar (valfrjálst).</span><span class="sxs-lookup"><span data-stu-id="ce6b3-128">In the **Display order** box, enter a display order (optional).</span></span>
1. <span data-ttu-id="ce6b3-129">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="ce6b3-129">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ce6b3-130">Eftirfarandi mynd sýnir dæmi um yfirlitsstigveldi rásar sem er lokið.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-130">The following image shows an example of a completed channel navigation hierarchy.</span></span>

![Dæmi um rásarstigveldi](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a><span data-ttu-id="ce6b3-132">Bæta afurðum við flokkshnúta</span><span class="sxs-lookup"><span data-stu-id="ce6b3-132">Add products to category nodes</span></span>

<span data-ttu-id="ce6b3-133">Fylgdu þessum skrefum til að bæta afurðum við flokkahnúta.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-133">To add products to category nodes, follow these steps.</span></span>

1. <span data-ttu-id="ce6b3-134">Velja flokkshnút.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-134">Select a category node.</span></span>
1. <span data-ttu-id="ce6b3-135">Undir **Afurðir** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-135">Under **Products**, select **Add**.</span></span>
1. <span data-ttu-id="ce6b3-136">Finndu nýju afurðirnar sem þú vilt bæta við með afurðarnúmeri eða afurðarheiti og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-136">Find the new product(s) you want to add using product number or product name, and then select **OK**.</span></span>
1. <span data-ttu-id="ce6b3-137">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="ce6b3-137">On the action pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="ce6b3-138">Að bæta afurðum við hnút inni í stigveldi rásarinnar dugar ekki til þess að afurðirnar birtist á valinni rás, einnig verður að tengja afurðirnar við afurð.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-138">Adding products to a node inside the channel navigation hierarchy is not sufficient for the products to show up on a selected channel, the products must also be assorted to a product.</span></span>

<span data-ttu-id="ce6b3-139">Eftirfarandi mynd sýnir dæmi um hnút með afurðum sem er bætt við.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-139">The following image shows an example node with products added.</span></span>

![Afurðum bætt við flokkshnút](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a><span data-ttu-id="ce6b3-141">Bættu afurðareigindahópum við flokkshnúta</span><span class="sxs-lookup"><span data-stu-id="ce6b3-141">Add product attribute groups to category nodes</span></span>

> [!NOTE]
> <span data-ttu-id="ce6b3-142">Það verður að búa til eigindahópa áður en þú getur bætt þeim við hnút innan yfirlitsstigveldi rásar.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-142">Attribute groups must be created before you can add them to a node inside the channel navigation hierarchy.</span></span>

<span data-ttu-id="ce6b3-143">Til að bæta afurð og eigindahóp við flokkshnút skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-143">To add product an attribute group to a category node, follow these steps.</span></span>

1. <span data-ttu-id="ce6b3-144">Velja flokkshnút.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-144">Select a category node.</span></span>
1. <span data-ttu-id="ce6b3-145">Undir **Afurðaeigindahópur** velurðu **Bæta við**.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-145">Under **Product attribute group**, select **Add**.</span></span>
1. <span data-ttu-id="ce6b3-146">Finndu eigindahópa sem þú vilt bæta við og veldu síðan **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-146">Find the attribute group(s) you would like to add, and then select **OK**.</span></span>
1. <span data-ttu-id="ce6b3-147">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="ce6b3-147">On the action pane, select **Save**.</span></span>

<span data-ttu-id="ce6b3-148">Eftirfarandi mynd sýnir dæmi um hnút með afurðareigindir sem er bætt við.</span><span class="sxs-lookup"><span data-stu-id="ce6b3-148">The following image shows a sample node with product attribute groups added.</span></span>

![Eigindaflokkar afurðar á hnút](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a><span data-ttu-id="ce6b3-150">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="ce6b3-150">Additional resources</span></span>

[<span data-ttu-id="ce6b3-151">Setja upp úrval</span><span class="sxs-lookup"><span data-stu-id="ce6b3-151">Set up assortments</span></span>](set-up-assortments.md)

[<span data-ttu-id="ce6b3-152">Stjórna eigindum og eigindahópum</span><span class="sxs-lookup"><span data-stu-id="ce6b3-152">Manage attributes and attribute groups</span></span>](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]