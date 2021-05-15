---
title: Breyta röðun fyrir smásölueiningar
description: Þetta efni útskýrir hugtök sem tengjast stjórnun birtingarraðar fyrir ýmsar smásölueiningar í Dynamics 365 Commerce.
author: josaw1
ms.date: 08/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: Category, Retail product hierarchy, Navigation hierarchy
audience: Application User, Merchandising manager, Catalog manager
ms.reviewer: josaw
ms.custom: 268444
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 31798508e4cc71e31a30dc91acebfdde8226b16c
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 04/22/2021
ms.locfileid: "5937063"
---
# <a name="change-the-sort-order-for-merchandising-entities"></a><span data-ttu-id="52624-103">Breyta röðun fyrir smásölueiningar</span><span class="sxs-lookup"><span data-stu-id="52624-103">Change the sort order for merchandising entities</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="52624-104">Smásalar líta á vöruuppgötvun sem aðalverkfæri til að hafa samskipti við viðskiptavini á öllum rásum.</span><span class="sxs-lookup"><span data-stu-id="52624-104">Retailers consider product discovery a primary tool for customer interaction across all channels.</span></span> <span data-ttu-id="52624-105">Ýmis virkni geta hjálpað viðskiptavinum að uppgötva vörur á auðveldan hátt.</span><span class="sxs-lookup"><span data-stu-id="52624-105">Various functionality can help customers easily discover products.</span></span> <span data-ttu-id="52624-106">Til dæmis geta þeir skoðað flokka, leitað og síað.</span><span class="sxs-lookup"><span data-stu-id="52624-106">For example, they can browse categories, search, and filter.</span></span>

<span data-ttu-id="52624-107">Þetta efni útskýrir hugtök sem tengjast stjórnun birtingarraðar fyrir ýmsar smásölueiningar.</span><span class="sxs-lookup"><span data-stu-id="52624-107">This topic explains the concepts that are related to controlling the display order for various merchandising-related entities.</span></span> <span data-ttu-id="52624-108">Það útskýrir einnig hvernig á að breyta röðuninni.</span><span class="sxs-lookup"><span data-stu-id="52624-108">It also explains how to change the sort order.</span></span>

## <a name="overview"></a><span data-ttu-id="52624-109">Yfirlit</span><span class="sxs-lookup"><span data-stu-id="52624-109">Overview</span></span>

<span data-ttu-id="52624-110">Stuðningur við röðun ýmissa smásöluaðila hefur verið aukinn.</span><span class="sxs-lookup"><span data-stu-id="52624-110">The support for sorting various merchandising-related entities has been enhanced.</span></span> <span data-ttu-id="52624-111">Þessi stuðningur er nú betur í takt við núverandi viðskiptavinasviðsmyndir sem áður kröfðust viðbóta frá framkvæmdaraðilum.</span><span class="sxs-lookup"><span data-stu-id="52624-111">This support is now better aligned with existing customer scenarios that previously required extensions from implementation partners.</span></span>

<span data-ttu-id="52624-112">Í útgáfum af Retail sem eru eldri en útgáfa 10.0.5 var röðunin fyrir flokka í yfirlitsstigveldinu í stafrófsröð.</span><span class="sxs-lookup"><span data-stu-id="52624-112">In versions of Retail that are earlier than version 10.0.5, the sort order for categories in the navigation hierarchy was alphabetical.</span></span> <span data-ttu-id="52624-113">Nýja sérsniðna röðunaraðgerðin gerir kleift vörustjórum smásölu að stilla röðunina fyrir ýmsar smásölueiningar á milli allra viðskiptavina.</span><span class="sxs-lookup"><span data-stu-id="52624-113">The new custom sort order functionality lets merchandising managers configure the sort order for various merchandising-related entities across all end-user clients.</span></span> <span data-ttu-id="52624-114">Þessir viðskiptavinir eru með höfuðstöðvar (HQ) og símaver.</span><span class="sxs-lookup"><span data-stu-id="52624-114">These clients include headquarters (HQ) and call centers.</span></span>

## <a name="configure-the-display-order-for-categories-in-the-product-hierarchy"></a><span data-ttu-id="52624-115">Skilgreindu birtingarröð fyrir flokka í afurðastigveldi</span><span class="sxs-lookup"><span data-stu-id="52624-115">Configure the display order for categories in the product hierarchy</span></span>

<span data-ttu-id="52624-116">Áður en þú getur klárað þetta ferli verður að setja upp kynningargögn í umhverfi þínu.</span><span class="sxs-lookup"><span data-stu-id="52624-116">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="52624-117">Farðu í **Retail og Commerce \> Afurðir og tegundir \> Afurðastigveldi Commerce**.</span><span class="sxs-lookup"><span data-stu-id="52624-117">Go to **Retail and Commerce \> Products and categories \> Commerce product hierarchy**.</span></span>
2. <span data-ttu-id="52624-118">Smelltu á **Breyta tegundastigveldi**.</span><span class="sxs-lookup"><span data-stu-id="52624-118">Click **Edit category hierarchy**.</span></span>
3. <span data-ttu-id="52624-119">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="52624-119">Click **Edit**.</span></span>
4. <span data-ttu-id="52624-120">Í trénu stækkarðu **ALL \> Action Sports**.</span><span class="sxs-lookup"><span data-stu-id="52624-120">In the tree, expand **ALL \> Action Sports**.</span></span>
5. <span data-ttu-id="52624-121">Í trénu stækkarðu **ALL \> Hópíþróttir**.</span><span class="sxs-lookup"><span data-stu-id="52624-121">In the tree, expand **ALL \> Team Sports**.</span></span>
6. <span data-ttu-id="52624-122">Í reitinn **Sýna röðun** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="52624-122">In the **Display order** field, enter a number.</span></span> <span data-ttu-id="52624-123">(Talan getur verið neikvæð.)</span><span class="sxs-lookup"><span data-stu-id="52624-123">(The number can be negative.)</span></span>
7. <span data-ttu-id="52624-124">Endurtaktu skref 4 til 6 fyrir fleiri flokka sem þú vilt breyta röðinni á.</span><span class="sxs-lookup"><span data-stu-id="52624-124">Repeat steps 4 through 6 for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="52624-125">Skjápöntunin fyrir yfirlitsstigveldi rásar mun endurspeglast í aðalstöðvum fyrir stigveldi afurðar netverslunar og losaðar afurðir eftir flokkum.</span><span class="sxs-lookup"><span data-stu-id="52624-125">The display order for the channel navigation hierarchy will be reflected in HQ for the commerce product hierarchy and released products by category.</span></span>

![Sérsniðin afurðastigveldi flokkuð með neikvæðum gildum](./media/RetailProductHierarchyCustomSortedWithNegativeValues.png)

![Losaðar afurðir eftir flokkum sérraðað eftir afurðastigveldi](./media/ReleasedProductsByCategoryCustomSortedBasedOnRetailProductHierarchy.png)

## <a name="configure-the-display-order-for-categories-in-the-channel-navigation-hierarchy"></a><span data-ttu-id="52624-128">Skilgreindu birtingarröð fyrir flokka í yfirlitsstigveldi rásar</span><span class="sxs-lookup"><span data-stu-id="52624-128">Configure the display order for categories in the channel navigation hierarchy</span></span>

<span data-ttu-id="52624-129">Áður en þú getur klárað þetta ferli verður að setja upp kynningargögn í umhverfi þínu.</span><span class="sxs-lookup"><span data-stu-id="52624-129">Before you can complete this procedure, demo data must be installed in your environment.</span></span>

1. <span data-ttu-id="52624-130">Farðu í **Retail og Commerce \> Afurðir og flokkar \> Yfirlitsflokkar rásar**.</span><span class="sxs-lookup"><span data-stu-id="52624-130">Go to **Retail and Commerce \> Products and categories \> Channel navigation categories**.</span></span>
2. <span data-ttu-id="52624-131">Af listanum velurðu stigveldið **Tískuyfirlit**.</span><span class="sxs-lookup"><span data-stu-id="52624-131">In the list, select the **Fashion navigation** hierarchy.</span></span>
3. <span data-ttu-id="52624-132">Smelltu á **Breyta tegundastigveldi**.</span><span class="sxs-lookup"><span data-stu-id="52624-132">Click **Edit category hierarchy**.</span></span>
4. <span data-ttu-id="52624-133">Smellið á **Breyta**.</span><span class="sxs-lookup"><span data-stu-id="52624-133">Click **Edit**.</span></span>
5. <span data-ttu-id="52624-134">Í trénu velurðu **Tíska \> Kvenfatnaður \> Dömuskór**.</span><span class="sxs-lookup"><span data-stu-id="52624-134">In the tree, select **Fashion \> Womenswear \> Womens Shoes**.</span></span>
6. <span data-ttu-id="52624-135">Í reitinn **Sýna röðun** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="52624-135">In the **Display order** field, enter a number.</span></span>
7. <span data-ttu-id="52624-136">Í trénu velurðu **Tíska \> Kvenfatnaður \> Toppar**.</span><span class="sxs-lookup"><span data-stu-id="52624-136">In the tree, select **Fashion \> Womenswear \> Tops**.</span></span>

    <span data-ttu-id="52624-137">Sömuleiðis er hægt að skilgreina röðun fyrir undirflokka.</span><span class="sxs-lookup"><span data-stu-id="52624-137">Likewise, you can define the sort order for the sub-categories.</span></span>

8. <span data-ttu-id="52624-138">Í trénu velurðu **Tíska \> Herrafatnaður \> Óformlegar skyrtur**.</span><span class="sxs-lookup"><span data-stu-id="52624-138">In the tree, select **Fashion \> Menswear \> Casual Shirts**.</span></span>
9. <span data-ttu-id="52624-139">Í reitinn **Sýna röðun** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="52624-139">In the **Display order** field, enter a number.</span></span>
10. <span data-ttu-id="52624-140">Í trénu velurðu **Tíska \> Herrafatnaður \> Frakkar og jakkar**.</span><span class="sxs-lookup"><span data-stu-id="52624-140">In the tree, select **Fashion \> Menswear \> Coats & Jackets**.</span></span>
11. <span data-ttu-id="52624-141">Í reitinn **Sýna röðun** skal slá inn númer.</span><span class="sxs-lookup"><span data-stu-id="52624-141">In the **Display order** field, enter a number.</span></span>
12. <span data-ttu-id="52624-142">Endurtaktu fyrir fleiri flokka sem þú vilt breyta röðinni á.</span><span class="sxs-lookup"><span data-stu-id="52624-142">Repeat for any additional categories that you want to change the order of.</span></span>

<span data-ttu-id="52624-143">Birtingarröð fyrir yfirlitsstigveldi rásarinnar endurspeglast í aðalstöðvum, vörulista og rásum.</span><span class="sxs-lookup"><span data-stu-id="52624-143">The display order for the channel navigation hierarchy is reflected in HQ, catalog, and channels.</span></span>

![Sérröðun yfirlitsstigveldis rásar](./media/ChannelNavCustomSorted.png)

![Yfirlitsstigveldi vörulista sérflokkuð eftir yfirlitsstigveldi rásarinnar](./media/CatalogNavHierarchyCustomSortedBasedOnChannelNav.png)

![Sölustaður með sérsniðnum flokkum](./media/POSChannelCategoriesCustomSorted.png)

> [!NOTE]
> <span data-ttu-id="52624-147">Sjálfgefið er að slökkt sé á sérröðunarstillingunni.</span><span class="sxs-lookup"><span data-stu-id="52624-147">By default the custom sort order feature is turned off.</span></span> <span data-ttu-id="52624-148">Til að læra hvernig á að kveikja á þessum eiginleika og öðrum eiginleikum skal sjá [Eiginleikastjórnun](/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="52624-148">To learn how to turn on this feature and other features, see [Feature management](/dynamics365/unified-operations/fin-and-ops/get-started/feature-management/feature-management-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]