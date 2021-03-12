---
title: Grunnstilla rás til að nota skoðunarstigveldi rásar
description: Þetta efnisatriði lýsir hvernig á að stilla rás til að nota stigveldi rásar í Microsoft Dynamics 365 Commerce.
author: samjarawan
manager: annbe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3dcba743e6557b1bd366ac79ecb49ead831dceb4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "5001026"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a><span data-ttu-id="89426-103">Grunnstilla rás til að nota skoðunarstigveldi rásar</span><span class="sxs-lookup"><span data-stu-id="89426-103">Configure a channel to use a channel navigation hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="89426-104">Þetta efnisatriði lýsir hvernig á að stilla rás til að nota stigveldi rásar í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="89426-104">This topic describes how to configure a channel to use a channel navigation hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="89426-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="89426-105">Overview</span></span>

<span data-ttu-id="89426-106">Stigaleiðir rásarinnar skipuleggja vörur í flokka svo hægt sé að vafra um vörurnar á e-verslunarsíðu eða á sölustöðum (POS).</span><span class="sxs-lookup"><span data-stu-id="89426-106">Channel navigation hierarchies organize products into categories so that the products can be browsed on an e-Commerce site or at points of sale (POS).</span></span> <span data-ttu-id="89426-107">Smásölu- og netrásir verða að vera stilltar með stigveldi rásar.</span><span class="sxs-lookup"><span data-stu-id="89426-107">Retail and online channels must be configured with channel navigation hierarchies.</span></span>

## <a name="configure-the-channel"></a><span data-ttu-id="89426-108">Stilltu rásina</span><span class="sxs-lookup"><span data-stu-id="89426-108">Configure the channel</span></span>

<span data-ttu-id="89426-109">Fylgdu þessum skrefum til að stilla rásina til að nota stigveldi rásarinnar.</span><span class="sxs-lookup"><span data-stu-id="89426-109">To configure a channel to use a channel navigation hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="89426-110">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Rásarflokkar og afurðareigindir**.</span><span class="sxs-lookup"><span data-stu-id="89426-110">In the navigation pane, go to **Modules \> Retail and commerce \> Channel setup \> Channel categories and product attributes**.</span></span>
1. <span data-ttu-id="89426-111">Velja skal rásina sem á að skilgreina.</span><span class="sxs-lookup"><span data-stu-id="89426-111">Select the channel to configure.</span></span>
1. <span data-ttu-id="89426-112">Í aðgerðarúðunni skal velja **Stilla eigind lýsigagna**.</span><span class="sxs-lookup"><span data-stu-id="89426-112">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="89426-113">Í fellilistanum **Tegundastigveldi** velurðu viðeigandi yfirlitsstigveldi rásarinnar.</span><span class="sxs-lookup"><span data-stu-id="89426-113">In the **Category hierarchy** drop-down list, select the appropriate channel navigation hierarchy.</span></span>
1. <span data-ttu-id="89426-114">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="89426-114">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="89426-115">Undir **Eiginleikahópur** bætirðu við hvaða eigindahópum sem verða hnattrænir eiginleikar fyrir alla hnúta.</span><span class="sxs-lookup"><span data-stu-id="89426-115">Under **Attribute group**, add any attribute groups that will be global attributes for all nodes.</span></span>

<span data-ttu-id="89426-116">Eftirfarandi myndi sýnir hvernig stilla skuli rás til að nota stigveldi rásarinnar.</span><span class="sxs-lookup"><span data-stu-id="89426-116">The following image shows how to configure a channel to use a channel navigation hierarchy.</span></span>

![Dæmi um rásaskilgreiningu](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a><span data-ttu-id="89426-118">Stilla eigind lýsigagna</span><span class="sxs-lookup"><span data-stu-id="89426-118">Set attribute metadata</span></span>

<span data-ttu-id="89426-119">Ef þú setur lýsigögn eigindisins gerir það kleift að stilla eiginleika á hverjum hnút.</span><span class="sxs-lookup"><span data-stu-id="89426-119">Setting the attribute metadata will allow configuration of attributes on each node.</span></span>

<span data-ttu-id="89426-120">Til að stilla lýsigögn eigindar skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="89426-120">To set attribute metadata, follow these steps.</span></span>

1. <span data-ttu-id="89426-121">Í aðgerðarúðunni skal velja **Stilla eigind lýsigagna**.</span><span class="sxs-lookup"><span data-stu-id="89426-121">On the action pane, select **Set attribute metadata**.</span></span>
1. <span data-ttu-id="89426-122">Fyrir hvern hnút velurðu **Afurðareigindir rásarinnar**.</span><span class="sxs-lookup"><span data-stu-id="89426-122">For each node select **Channel product attributes**.</span></span>
1. <span data-ttu-id="89426-123">Stilltu **Sýna eigindi á rás** á **Já** og **Hægt að fínpússa** að **Já**, til að gera fágunaraðilum kleift á þeirri rás.</span><span class="sxs-lookup"><span data-stu-id="89426-123">Set **Show attribute on channel** to **Yes** and **Can be refined** to **Yes**, to enable refiners on that channel.</span></span>
1. <span data-ttu-id="89426-124">Eftir að hafa stillt hvern hnút eins og óskað er, í **Aðgerðaglugganum** velurðu hnappinn **Vista** til að vista.</span><span class="sxs-lookup"><span data-stu-id="89426-124">After configuring each node as desired, on the **Action pane**, select the **Save** button to save.</span></span>
1. <span data-ttu-id="89426-125">Veldu **X** efst í hægra horninu til að loka þessum skjá aftur á síðunni **Rásarflokkar og afurðareigindir**.</span><span class="sxs-lookup"><span data-stu-id="89426-125">Select the **X** in the top right corner to exit this screen back to the **Channel categories and product attributes** page.</span></span>

<span data-ttu-id="89426-126">Eftirfarandi mynd sýnir dæmi um eiginleika rásafurða sem eru stilltir á hnút rásaflokks.</span><span class="sxs-lookup"><span data-stu-id="89426-126">The following image shows an example set of channel product attributes configured on a channel category node.</span></span>

![Rásareigindir á hnút rásaflokks](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a><span data-ttu-id="89426-128">Birta breytingar</span><span class="sxs-lookup"><span data-stu-id="89426-128">Publish changes</span></span>

<span data-ttu-id="89426-129">Eigi breytingarnar að öðlast gildi verður að birta breytingarnar.</span><span class="sxs-lookup"><span data-stu-id="89426-129">For changes to take effect, you will need to publish the changes.</span></span>

<span data-ttu-id="89426-130">Til að birta breytingar skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="89426-130">To publish changes, follow these steps.</span></span>

1. <span data-ttu-id="89426-131">Veldu aðgerðarrúðuna **Birta uppfærslur rásar**.</span><span class="sxs-lookup"><span data-stu-id="89426-131">On the action pane, select **Publish channel updates**.</span></span>
1. <span data-ttu-id="89426-132">Í glugganum **Birta rásaruppfærslur** velurðu **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="89426-132">In the **Publish channel updates** pane, select **OK**.</span></span>

<span data-ttu-id="89426-133">Eftirfarandi mynd sýnir hvernig á að birta uppfærslur á rásum.</span><span class="sxs-lookup"><span data-stu-id="89426-133">The following image shows how to publish channel updates.</span></span>

![Birta uppfærslur rásar](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="89426-135">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="89426-135">Additional resources</span></span>

[<span data-ttu-id="89426-136">Stofna yfirlitsstigveldi rásar</span><span class="sxs-lookup"><span data-stu-id="89426-136">Create a channel navigation hierarchy</span></span>](create-channel-hierarchy.md)


