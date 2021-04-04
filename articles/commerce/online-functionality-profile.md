---
title: Búa til virkniforstillingu á netinu
description: Þetta efnisatriði lýsir hvernig á að stofna virkniforstillingu í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: cb9d78a945132c913dcb8a5d5b41eaacd1a6db3b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477733"
---
# <a name="create-an-online-functionality-profile"></a><span data-ttu-id="8c033-103">Búa til virkniforstillingu á netinu</span><span class="sxs-lookup"><span data-stu-id="8c033-103">Create an online functionality profile</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8c033-104">Þetta efnisatriði sýnir yfirlit yfir uppsetningu á virkniforstillingu fyrir Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8c033-104">This topic presents an overview of setting up an online functionality profile for Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8c033-105">Online virkni sniðið veitir ýmsar stillingar sem notaðar eru fyrir netrásir.</span><span class="sxs-lookup"><span data-stu-id="8c033-105">The online functionality profile provides various settings used for online channels.</span></span> <span data-ttu-id="8c033-106">Hver rás á netinu verður að tilgreina prófíl á netinu.</span><span class="sxs-lookup"><span data-stu-id="8c033-106">Each online channel must specify an online functionality profile.</span></span>

## <a name="create-an-online-functionality-profile"></a><span data-ttu-id="8c033-107">Búa til virkniforstillingu á netinu</span><span class="sxs-lookup"><span data-stu-id="8c033-107">Create an online functionality profile</span></span>

<span data-ttu-id="8c033-108">Eftirfarandi aðferð útskýrir hvernig á að búa til netvirkni snið úr forritinu Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="8c033-108">The following procedure explains how to create an online functionality profile from within Commerce Headquarters app.</span></span>

1. <span data-ttu-id="8c033-109">Farðu í **Einingar \> Uppsetning rásar \> Uppsetning netverslunar \> Virknireglur**.</span><span class="sxs-lookup"><span data-stu-id="8c033-109">In the navigation pane, go to **Modules \> Channel setup \> Online store setup \> Functionality profiles**.</span></span>
1. <span data-ttu-id="8c033-110">Í aðgerðaglugganum velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="8c033-110">On the action pane, select **New**.</span></span>
1. <span data-ttu-id="8c033-111">Í svæðið **Forstilling** skal færa inn kenni fyrir forstillinguna.</span><span class="sxs-lookup"><span data-stu-id="8c033-111">In the **Profile** field, enter an ID for the profile.</span></span>
1. <span data-ttu-id="8c033-112">Í reitinn **Lýsing**, slærðu inn gildi („Adventure Works Profile“ í myndinni hér að neðan).</span><span class="sxs-lookup"><span data-stu-id="8c033-112">In the **Description** field, enter a value ("Adventure Works Profile" in the example image below).</span></span>
1. <span data-ttu-id="8c033-113">Í **Aðgerðir** kafla, breyttu **CART**, **RETAIL CUSTOMERS** eða **CHECKOUT** stillingar, eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="8c033-113">In the **Functions** section, modify the **CART**, **RETAIL CUSTOMERS**, or **CHECKOUT** settings, as needed.</span></span>
1. <span data-ttu-id="8c033-114">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="8c033-114">On the action pane, select **Save**.</span></span>

<span data-ttu-id="8c033-115">Eftirfarandi mynd sýnir dæmi um netvirknireglu.</span><span class="sxs-lookup"><span data-stu-id="8c033-115">The following image shows an example online functionality profile.</span></span>
  
![Netvirknireglur fyrir forstillingu](media/online-functionality-profile.png)

## <a name="functions"></a><span data-ttu-id="8c033-117">Aðgerðir</span><span class="sxs-lookup"><span data-stu-id="8c033-117">Functions</span></span>

- <span data-ttu-id="8c033-118">**Samanlagðar vörur**: Þegar þetta er virkt gerir þessi aðgerð körfunni kleift að uppfæra magn þegar sama hlut er bætt við mörgum sinnum.</span><span class="sxs-lookup"><span data-stu-id="8c033-118">**Aggregate products**: When enabled, this function allows the cart to update quantity when the same item is added multiple times.</span></span>
- <span data-ttu-id="8c033-119">**Leyfa afgreiðslu án greiðslna**: Þegar þetta er virkt annast þessi aðgerð atburðarás þegar hlutir sem bætt er við í körfu hafa verð $0.00.</span><span class="sxs-lookup"><span data-stu-id="8c033-119">**Allow checkout with no payments**: When enabled, this function handles the scenario when items added to cart have a price $0.00.</span></span>
- <span data-ttu-id="8c033-120">**Búðu til viðskiptavini í ósamstillta stillingu**: Þetta er eldri stilling sem gildir um þriðja aðila rafræn viðskipti og á ekki við Dynamics 365 netverslunarsíðuna.</span><span class="sxs-lookup"><span data-stu-id="8c033-120">**Create customer in async mode**: This is a legacy setting applicable to third-party e-Commerce channels and is not applicable to the Dynamics 365 e-Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8c033-121">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="8c033-121">Additional resources</span></span>

[<span data-ttu-id="8c033-122">Yfirlit rása</span><span class="sxs-lookup"><span data-stu-id="8c033-122">Channels overview</span></span>](channels-overview.md)

[<span data-ttu-id="8c033-123">Skilyrði fyrir uppsetningu rásar</span><span class="sxs-lookup"><span data-stu-id="8c033-123">Channel setup prerequisites</span></span>](channels-prerequisites.md)

[<span data-ttu-id="8c033-124">Setja upp netrás</span><span class="sxs-lookup"><span data-stu-id="8c033-124">Set up an online channel</span></span>](channel-setup-online.md)

[<span data-ttu-id="8c033-125">Setja upp smásölurás</span><span class="sxs-lookup"><span data-stu-id="8c033-125">Set up a retail channel</span></span>](channel-setup-retail.md)

[<span data-ttu-id="8c033-126">Setja upp rás símavers</span><span class="sxs-lookup"><span data-stu-id="8c033-126">Set up a call center channel</span></span>](channel-setup-callcenter.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
