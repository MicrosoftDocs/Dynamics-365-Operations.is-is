---
title: Búa til virkniforstillingu á netinu
description: Þetta efnisatriði lýsir því hvernig á að búa til virkniforstillingar í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 5ecbfcf3fa78ad2909a7cc9988ab1edaf2b98376
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4413281"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="27993-103">Búa til virkniforstillingu á netinu</span><span class="sxs-lookup"><span data-stu-id="27993-103">Create an online functionality profile</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="27993-104">Þetta efni birtir yfirlit yfir að setja upp netsniðsforrit fyrir Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="27993-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="27993-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="27993-105">Overview</span></span>

<span data-ttu-id="27993-106">Online virkni sniðið veitir ýmsar stillingar sem notaðar eru fyrir netrásir.</span><span class="sxs-lookup"><span data-stu-id="27993-106">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="27993-107">Hver rás á netinu verður að tilgreina prófíl á netinu.</span><span class="sxs-lookup"><span data-stu-id="27993-107">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="27993-108">Búa til virkniforstillingu á netinu</span><span class="sxs-lookup"><span data-stu-id="27993-108">Create an online functionality profile</span></span>

<span data-ttu-id="27993-109">Eftirfarandi aðferð útskýrir hvernig á að búa til netvirkni snið úr forritinu Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="27993-109">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="27993-110">Farðu í **Einingar \> Uppsetning rásar \> Uppsetning netverslunar \> Virknireglur**.</span><span class="sxs-lookup"><span data-stu-id="27993-110">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="27993-111">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="27993-111">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="27993-112">Í svæðið **Forstilling** skal færa inn kenni fyrir forstillinguna.</span><span class="sxs-lookup"><span data-stu-id="27993-112">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="27993-113">Í reitinn **Lýsing**, slærðu inn gildi („Adventure Works Profile“ í myndinni hér að neðan).</span><span class="sxs-lookup"><span data-stu-id="27993-113">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="27993-114">Í **Aðgerðir** kafla, breyttu **CART**, **RETAIL CUSTOMERS** eða **CHECKOUT** stillingar, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="27993-114">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="27993-115">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="27993-115">On the action pane, select **Save**.</span></span>

<span data-ttu-id="27993-116">Eftirfarandi mynd sýnir dæmi um netvirknireglu.</span><span class="sxs-lookup"><span data-stu-id="27993-116">The following image shows an example online functionality profile.</span></span>
  
![Netvirknireglur fyrir forstillingu](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="27993-118">Aðgerðir</span><span class="sxs-lookup"><span data-stu-id="27993-118">Functions</span></span>

- <span data-ttu-id="27993-119">**Samanlagðar vörur**: Þegar þetta er virkt gerir þessi aðgerð körfunni kleift að uppfæra magn þegar sama hlut er bætt við mörgum sinnum.</span><span class="sxs-lookup"><span data-stu-id="27993-119">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="27993-120">**Leyfa afgreiðslu án greiðslna**: Þegar þetta er virkt annast þessi aðgerð atburðarás þegar hlutir sem bætt er við í körfu hafa verð $0.00.</span><span class="sxs-lookup"><span data-stu-id="27993-120">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="27993-121">**Búðu til viðskiptavini í ósamstillta stillingu**: Þetta er eldri stilling sem gildir um þriðja aðila rafræn viðskipti og á ekki við Dynamics 365 netverslunarsíðuna.</span><span class="sxs-lookup"><span data-stu-id="27993-121">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="27993-122">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="27993-122">Additional resources</span></span>

[<span data-ttu-id="27993-123">Yfirlit rása</span><span class="sxs-lookup"><span data-stu-id="27993-123">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="27993-124">Skilyrði fyrir uppsetningu rásar</span><span class="sxs-lookup"><span data-stu-id="27993-124">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="27993-125">Setja upp netrás</span><span class="sxs-lookup"><span data-stu-id="27993-125">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="27993-126">Setja upp smásölurás</span><span class="sxs-lookup"><span data-stu-id="27993-126">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="27993-127">Setja upp rás símavers</span><span class="sxs-lookup"><span data-stu-id="27993-127">Set up a call center channel</span></span>](channel-setup-callcenter.md)
