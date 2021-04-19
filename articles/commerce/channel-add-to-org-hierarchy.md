---
title: Bæta rás við stigveldi fyrirtækis
description: Þetta efnisatriði lýsir hvernig á að bæta rás við stigveldi fyrirtækis í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: c7ff6d8ee7e526e45975cfa500b5e6d6079054dc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800688"
---
# <a name="add-a-channel-to-an-organizational-hierarchy"></a><span data-ttu-id="3552e-103">Bæta rás við stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="3552e-103">Add a channel to an organizational hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3552e-104">Þetta efnisatriði lýsir hvernig á að bæta rás við stigveldi fyrirtækis í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3552e-104">This topic describes how to add a channel to an organizational hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3552e-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="3552e-105">Overview</span></span>

<span data-ttu-id="3552e-106">Rásir þurfa að vera tengdar við eitt eða fleiri stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="3552e-106">Channels need to be associated with one or more organizational hierarchies.</span></span> <span data-ttu-id="3552e-107">Áður en þú býrð til rásir þarftu að staðfesta að stigveldi fyrirtækis hafi verið sett upp.</span><span class="sxs-lookup"><span data-stu-id="3552e-107">Before creating channels, you need to confirm that your organizational hierarchies have been set up.</span></span>  

<span data-ttu-id="3552e-108">Sjá [Stigveldi fyrirtækis](channels-org-hierarchies.md) fyrir nánari upplýsingar um hvernig stofna skuli stigveldi fyrirtækis.</span><span class="sxs-lookup"><span data-stu-id="3552e-108">See [Organizational hierarchies](channels-org-hierarchies.md) for more details on how to create organizational hierarchies.</span></span>

## <a name="select-a-hierarchy"></a><span data-ttu-id="3552e-109">Velja stigveldi</span><span class="sxs-lookup"><span data-stu-id="3552e-109">Select a hierarchy</span></span>

<span data-ttu-id="3552e-110">Fylgdu þessum skrefum til að velja stigveldi.</span><span class="sxs-lookup"><span data-stu-id="3552e-110">To select a hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="3552e-111">Í yfirlitsglugganum ferðu í **Einingar \> Retail og Commerce \> Uppsetning rásar \> Stigveldi fyrirtækis**.</span><span class="sxs-lookup"><span data-stu-id="3552e-111">In the navigation pane, go to **Modules \> Retail and commerce \> Channel Setup \> Organization hierarchies**.</span></span>
1. <span data-ttu-id="3552e-112">Af listanum velurðu það stigveldi fyrirtækis sem þú ætlar að bæta rásinni við.</span><span class="sxs-lookup"><span data-stu-id="3552e-112">From the list, select the organization hierarchy that you'll be adding the channel to.</span></span>
1. <span data-ttu-id="3552e-113">Í aðgerðaglugganum velurðu **Skoða** til að skoða stigveldisupplýsingar.</span><span class="sxs-lookup"><span data-stu-id="3552e-113">On the action pane, select **View** to view hierarchy details.</span></span>

<span data-ttu-id="3552e-114">Eftirfarandi mynd sýnir upplýsingar um stigveldi fyrirtækis fyrir valið stigveldi.</span><span class="sxs-lookup"><span data-stu-id="3552e-114">The following image shows organizational hierarchy details for the selected hierarchy.</span></span>

![Upplýsingar um stigveldi fyrirtækis fyrir valið stigveldi](media/channel-add-to-org-hierarchy-1.png)

## <a name="add-a-channel-to-a-hierachy-node"></a><span data-ttu-id="3552e-116">Bæta rás við stigveldishnút</span><span class="sxs-lookup"><span data-stu-id="3552e-116">Add a channel to a hierachy node</span></span>

<span data-ttu-id="3552e-117">Til að bæta rás við stigveldishnút skaltu fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="3552e-117">To add a channel to a hierachy node, follow these steps.</span></span>

1. <span data-ttu-id="3552e-118">Í aðgerðaglugganum velurðu **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="3552e-118">On the action pane, select **Edit**.</span></span>
1. <span data-ttu-id="3552e-119">Veldu stigveldishnútinn sem þú vilt að rásinni verði bætt við og síðan í fellivalmyndinni **Setja inn** skaltu velja **Smásölurás**.</span><span class="sxs-lookup"><span data-stu-id="3552e-119">Select the hierachy node you want the channel added to, then from the **Insert** drop-down list, select **Retail Channel**.</span></span> 
1. <span data-ttu-id="3552e-120">Veldu rásina sem á að bæta við og veldu síðan hnappinn **Í lagi**.</span><span class="sxs-lookup"><span data-stu-id="3552e-120">Select the channel to add, then select the **OK** button.</span></span>
1. <span data-ttu-id="3552e-121">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="3552e-121">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="3552e-122">Í aðgerðaglugganum velurðu **Birta** og gefur upp liðna **Gildisdagsetningu** til að þessi aðgerð taki strax gildi.</span><span class="sxs-lookup"><span data-stu-id="3552e-122">On the action pane, select **Publish** and provide an **Effective date** in the past to have this action go into effect immediately.</span></span>

<span data-ttu-id="3552e-123">Eftirfarandi mynd sýnir hvernig á að velja rás til að bæta við stigveldishnút.</span><span class="sxs-lookup"><span data-stu-id="3552e-123">The following image shows how to select a channel to add to a hierarchy node.</span></span>

![Veldu rás til að bæta við stigveldishnút](media/channel-add-to-org-hierarchy-2.png)

<span data-ttu-id="3552e-125">Eftirfarandi mynd sýnir stigveldi með ýmsum rásum bætt við.</span><span class="sxs-lookup"><span data-stu-id="3552e-125">The following image shows a hierarchy with various channels added.</span></span>

![Stigveldi með ýmsum rásum bætt við](media/channel-add-to-org-hierarchy-3.png)

## <a name="additional-resources"></a><span data-ttu-id="3552e-127">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="3552e-127">Additional resources</span></span>

[<span data-ttu-id="3552e-128">Yfirlit yfir rásir</span><span class="sxs-lookup"><span data-stu-id="3552e-128">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="3552e-129">Skilyrði fyrir rásauppsetningu</span><span class="sxs-lookup"><span data-stu-id="3552e-129">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="3552e-130">Yfirlit yfir fyrirtæki og fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="3552e-130">Organizations and organizational hierarchies overview</span></span>](../fin-ops-core/fin-ops/organization-administration/organizations-organizational-hierarchies.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="3552e-131">Skipuleggja fyrirtækjastigveldi</span><span class="sxs-lookup"><span data-stu-id="3552e-131">Plan your organizational hierarchy</span></span>](../fin-ops-core/fin-ops/organization-administration/plan-organizational-hierarchy.md?toc=/dynamics365/commerce/toc.json)

[<span data-ttu-id="3552e-132">Stigveldi fyrirtækis</span><span class="sxs-lookup"><span data-stu-id="3552e-132">Organization hierarchies</span></span>](channels-org-hierarchies.md)

[<span data-ttu-id="3552e-133">Setja upp smásölurás</span><span class="sxs-lookup"><span data-stu-id="3552e-133">Set up a retail channel</span></span>](channel-setup-retail.md)
    
[<span data-ttu-id="3552e-134">Setja upp netrás</span><span class="sxs-lookup"><span data-stu-id="3552e-134">Set up an online channel</span></span>](channel-setup-online.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]