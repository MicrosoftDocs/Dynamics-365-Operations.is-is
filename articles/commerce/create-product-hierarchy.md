---
title: Stofna nýtt afurðastigveldi
description: Í þessu efnisatriði er lýst hvernig eigi að stofna nýtt afurðastigveldi í Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 8aef33a501f43105730eaa21a9159eb1398a1b36
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799566"
---
# <a name="create-a-new-product-hierarchy"></a><span data-ttu-id="b293b-103">Stofna nýtt afurðastigveldi</span><span class="sxs-lookup"><span data-stu-id="b293b-103">Create a new product hierarchy</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b293b-104">Í þessu efnisatriði er lýst hvernig eigi að stofna nýtt afurðastigveldi í Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b293b-104">This topic describes how to create a new product hierarchy in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b293b-105">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="b293b-105">Overview</span></span>

<span data-ttu-id="b293b-106">Dynamics 365 Commerce styður margar smásölurásir.</span><span class="sxs-lookup"><span data-stu-id="b293b-106">Dynamics 365 Commerce supports multiple retail channels.</span></span> <span data-ttu-id="b293b-107">Meðal þessara smásölurásir eru netverslanir, símaver, og smásöluverslanir (einnig kallað hefðbundnar verslanir).</span><span class="sxs-lookup"><span data-stu-id="b293b-107">These retail channels include online stores, call centers, and retail stores (also known as brick-and-mortar stores).</span></span> <span data-ttu-id="b293b-108">Hvert smásöluverslunarrás getur haft sína eigin greiðsluhætti, verðflokka, sölustað (POS) afgreiðslukassa, tekjulykla og kostnaðarlykla og starfsfólk.</span><span class="sxs-lookup"><span data-stu-id="b293b-108">Each retail store channel can have its own payment methods, price groups, point of sale (POS) registers, income accounts and expense accounts, and staff.</span></span> <span data-ttu-id="b293b-109">Setja verður upp allar þessar einingar áður en hægt er að stofna smásöluverslunarrás.</span><span class="sxs-lookup"><span data-stu-id="b293b-109">You must set up all of these elements before you can create a retail store channel.</span></span> 

<span data-ttu-id="b293b-110">Afurðastigveldi Commercer er notað til að skilgreina aðalstigveldi smásöluafurða fyrir fyrirtækið.</span><span class="sxs-lookup"><span data-stu-id="b293b-110">A Commerce product hierarchy is used to define the overall product hierarchy for your organization.</span></span> <span data-ttu-id="b293b-111">Hægt er að nota afurðastigveldi Commerce fyrir smásölu, verðlagningu og kynningartilboð, skýrslugerð og skipulagningu úrvals.</span><span class="sxs-lookup"><span data-stu-id="b293b-111">You can use a Commerce product hierarchy for merchandising, pricing and promotions, reporting, and assortment planning.</span></span> <span data-ttu-id="b293b-112">Aðeins er hægt að úthluta einum afurðastigveldi Commerce á hvert fyrirtæki.</span><span class="sxs-lookup"><span data-stu-id="b293b-112">Only one Commerce product hierarchy can be assigned per organization.</span></span>

## <a name="create-and-configure-a-product-hierarchy"></a><span data-ttu-id="b293b-113">Stofna og stilla afurðastigveldi</span><span class="sxs-lookup"><span data-stu-id="b293b-113">Create and configure a product hierarchy</span></span>

<span data-ttu-id="b293b-114">Til að stofna og stilla afurðastigveldi Commerce fylgirðu þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="b293b-114">To create and configure a Commerce product hierarchy, follow these steps.</span></span>

1. <span data-ttu-id="b293b-115">Í Skoðunarrúðunni ferðu í **Einingar \> Retail og Commerce \> Afurðir og flokkar \> Afurðastigveldi Commerce**.</span><span class="sxs-lookup"><span data-stu-id="b293b-115">In the navigation pane, go to **Modules \> Retail and commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
1. <span data-ttu-id="b293b-116">Ef ekkert stigveldi er til ennþá, í **aðgerðaglugganum** veldu **Nýtt** til að búa til rót stigveldisins.</span><span class="sxs-lookup"><span data-stu-id="b293b-116">If no hierachy exists yet, on the **Action pane**, select **New** to create the root of the hierarchy.</span></span>
1. <span data-ttu-id="b293b-117">Undir **Almennt**:</span><span class="sxs-lookup"><span data-stu-id="b293b-117">Under **General**:</span></span>
    1. <span data-ttu-id="b293b-118">Í reitnum **Heiti** færirðu inn heiti.</span><span class="sxs-lookup"><span data-stu-id="b293b-118">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="b293b-119">Í reitinn **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="b293b-119">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="b293b-120">Í reitinn **Stutt heiti** slærðu inn stutt heiti.</span><span class="sxs-lookup"><span data-stu-id="b293b-120">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="b293b-121">Stilltu **Virkt** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="b293b-121">Set **Active** to **Yes**.</span></span>

## <a name="add-hierarchy-nodes"></a><span data-ttu-id="b293b-122">Bæta við stigveldishnút</span><span class="sxs-lookup"><span data-stu-id="b293b-122">Add hierarchy nodes</span></span>

<span data-ttu-id="b293b-123">Fylgdu þessum skrefum til að bæta við stigveldishnútum.</span><span class="sxs-lookup"><span data-stu-id="b293b-123">To add hierarchy nodes, follow these steps.</span></span>

1. <span data-ttu-id="b293b-124">Í aðgerðarúðunni velurðu **Breyta tegundastigveldi**.</span><span class="sxs-lookup"><span data-stu-id="b293b-124">On the action pane, select **Edit category hierarchy**.</span></span>
1. <span data-ttu-id="b293b-125">Veldu yfirhnútinn sem þú vilt bæta nýjum hnút við og veldu síðan **Nýr flokkshnútur**.</span><span class="sxs-lookup"><span data-stu-id="b293b-125">Select the parent node you want to add a new node to, and then select **New category node**.</span></span>
1. <span data-ttu-id="b293b-126">Í kaflanum **Almennt** veitirðu **Heiti**, **Lýsingu**, **Stutt heiti** og **Lykilorð**.</span><span class="sxs-lookup"><span data-stu-id="b293b-126">In the **General** section provide a **Name**, **Description**, **Friendly name** and **Keywords**.</span></span>
1. <span data-ttu-id="b293b-127">Undir **Almennt**:</span><span class="sxs-lookup"><span data-stu-id="b293b-127">Under **General**:</span></span>
    1. <span data-ttu-id="b293b-128">Í reitnum **Heiti** færirðu inn heiti.</span><span class="sxs-lookup"><span data-stu-id="b293b-128">In the **Name** box, enter a name.</span></span>
    1. <span data-ttu-id="b293b-129">Í reitinn **Lýsing** skal færa inn lýsingu.</span><span class="sxs-lookup"><span data-stu-id="b293b-129">In the **Description** box, enter a description.</span></span>
    1. <span data-ttu-id="b293b-130">Í reitinn **Stutt heiti** slærðu inn stutt heiti.</span><span class="sxs-lookup"><span data-stu-id="b293b-130">In the **Friendly name** box, enter a friendly name.</span></span>
    1. <span data-ttu-id="b293b-131">Í reitinn **Lykilorð** slærðu inn viðeigandi lykilorð.</span><span class="sxs-lookup"><span data-stu-id="b293b-131">In the **Keywords** box, enter relevant keywords.</span></span>
    1. <span data-ttu-id="b293b-132">Í reitinn **Sýna röð** slærðu inn númer fyrir skjápöntunina (valfrjálst).</span><span class="sxs-lookup"><span data-stu-id="b293b-132">In the **Display order** box, enter a number for the display order (optional).</span></span>
1. <span data-ttu-id="b293b-133">Í aðgerðaglugganum velurðu **Vista.**</span><span class="sxs-lookup"><span data-stu-id="b293b-133">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="b293b-134">Endurtaktu skrefin hér að ofan til að bæta við fleiri hnútum.</span><span class="sxs-lookup"><span data-stu-id="b293b-134">Repeat the steps above to add additional nodes.</span></span>

<span data-ttu-id="b293b-135">Eftirfarandi mynd sýnir stofnun nýs afurðastigveldishnúts.</span><span class="sxs-lookup"><span data-stu-id="b293b-135">The following image shows the creation of a new product hierarchy node.</span></span>

![Stofna afurðastigveldi](media/create-product-hierarchy.png)

## <a name="other-settings"></a><span data-ttu-id="b293b-137">Aðrar stillingar</span><span class="sxs-lookup"><span data-stu-id="b293b-137">Other settings</span></span>

<span data-ttu-id="b293b-138">Einnig er hægt að úthluta flokknum eigindahópa eftir þörfum.</span><span class="sxs-lookup"><span data-stu-id="b293b-138">Category attribute groups can also be assigned to each group as required.</span></span>  

## <a name="additional-resources"></a><span data-ttu-id="b293b-139">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="b293b-139">Additional resources</span></span>

[<span data-ttu-id="b293b-140">stigveldi verslunar</span><span class="sxs-lookup"><span data-stu-id="b293b-140">commerce hierarchies</span></span>](retail-hierarchies.md)

[<span data-ttu-id="b293b-141">Stjórna afurðaflokkum og afurðum </span><span class="sxs-lookup"><span data-stu-id="b293b-141">Manage product categories and products </span></span>](category-management-product-creation.md)

[<span data-ttu-id="b293b-142">Breyta röðun eininga markaðssetningar</span><span class="sxs-lookup"><span data-stu-id="b293b-142">Change the sort order for merchandizing entities</span></span>](custom-order-categories-nav-retail-prod-hierarchy.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]