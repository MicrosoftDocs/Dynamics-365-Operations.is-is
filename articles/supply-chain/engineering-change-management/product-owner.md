---
title: Eigendur afurða
description: Þetta efnisatriði gefur upplýsingar um eigendur afurða. Eigendur afurða er hópur notenda sem ber ábyrgð á tilteknum afurðum. Aðeins meðlimir í hópnum geta losað þessar afurðir. Einnig er hægt að nota Eigendur afurða í samþykktarverkflæðinu.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgProductOwner
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 90f5596f9b5fc45e78cc49a3309c45864e07e70b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967334"
---
# <a name="product-owners"></a><span data-ttu-id="d3398-106">Eigendur afurða</span><span class="sxs-lookup"><span data-stu-id="d3398-106">Product owners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3398-107">Eigendur afurðanna er hópur notenda sem ber ábyrgð á tilteknum afurðum.</span><span class="sxs-lookup"><span data-stu-id="d3398-107">The product owner is a group of users who are responsible for specific products.</span></span> <span data-ttu-id="d3398-108">Þegar hóp fyrir Eigendur afurða er úthlutað á afurð geta aðeins meðlimir þess hóps losað afurðina.</span><span class="sxs-lookup"><span data-stu-id="d3398-108">When a product owner group is assigned to a product, only the members of that group can release the product.</span></span> <span data-ttu-id="d3398-109">Einnig er hægt að nota eiganda afurðarinnar í samþykktarverkflæði í umsjón hönnunarbreytinga.</span><span class="sxs-lookup"><span data-stu-id="d3398-109">The product owner can also be used in the approval workflow in engineering change management.</span></span>

<span data-ttu-id="d3398-110">Eigendur afurðar eru Altækar stillingar.</span><span class="sxs-lookup"><span data-stu-id="d3398-110">Product owners are global settings.</span></span> <span data-ttu-id="d3398-111">Þar af leiðandi eru þeir tiltækir öllum lögaðilum.</span><span class="sxs-lookup"><span data-stu-id="d3398-111">Therefore, they are available to all legal entities.</span></span>

## <a name="create-a-product-owner-group"></a><span data-ttu-id="d3398-112">Stofna hóp fyrir Eigendur afurða</span><span class="sxs-lookup"><span data-stu-id="d3398-112">Create a product owner group</span></span>

<span data-ttu-id="d3398-113">Til að stofna hóp fyrir Eigendur afurða og bæta meðlimum við hann skal fylgja þessum skrefum.</span><span class="sxs-lookup"><span data-stu-id="d3398-113">To create a product owner group and add members to it, follow these steps.</span></span>

1. <span data-ttu-id="d3398-114">Farið í **Umsjón hönnunarbreytinga \> Uppsetning \> hóp fyrir Eigendur afurða**.</span><span class="sxs-lookup"><span data-stu-id="d3398-114">Go to **Engineering change management \> Setup \> Product owners**.</span></span>
2. <span data-ttu-id="d3398-115">Í aðgerðarúðunni velurðu **Nýtt**.</span><span class="sxs-lookup"><span data-stu-id="d3398-115">On the Action Pane, select **New**.</span></span>
3. <span data-ttu-id="d3398-116">Í reitnum **Eigandi afurðar** er fært inn heiti fyrir flokkinn.</span><span class="sxs-lookup"><span data-stu-id="d3398-116">In the **Product owner** field, enter a name for the group.</span></span>
4. <span data-ttu-id="d3398-117">Í reitnum **Heiti** skal slá inn lýsingu á hópnum.</span><span class="sxs-lookup"><span data-stu-id="d3398-117">In the **Name** field, enter a description of the group.</span></span>
5. <span data-ttu-id="d3398-118">Í flýtiflipanum **Meðlimir** skal bæta við starfsmönnum sem eiga að vera meðlimir í hópnum.</span><span class="sxs-lookup"><span data-stu-id="d3398-118">On the **Members** FastTab, add the workers who should be members of the group.</span></span>

## <a name="assign-a-product-owner-to-a-product"></a><span data-ttu-id="d3398-119">Úthluta eiganda afurðar á afurð</span><span class="sxs-lookup"><span data-stu-id="d3398-119">Assign a product owner to a product</span></span>

<span data-ttu-id="d3398-120">Til að úthluta eiganda afurðar á afurð, skal fylgja þessum skrefum:</span><span class="sxs-lookup"><span data-stu-id="d3398-120">To assign a product owner to a product, follow these steps.</span></span>

1. <span data-ttu-id="d3398-121">Opnið **Upplýsingar um afurð** síðuna fyrir viðkomandi afurð eða umsjónarmann afurðar.</span><span class="sxs-lookup"><span data-stu-id="d3398-121">Open the **Product details** page for the relevant product or product master.</span></span>
1. <span data-ttu-id="d3398-122">Í flýtiflipanum **Almenn atriði** er reiturinn **Eigandi afurðar** stilltur á heiti viðkomandi hóps fyrir eigendur afurða.</span><span class="sxs-lookup"><span data-stu-id="d3398-122">On the **General** FastTab, set the **Product owner** field to the name of the relevant product owner group.</span></span>

<span data-ttu-id="d3398-123">Þegar eiganda afurðar er úthlutað á afurð geta aðeins meðlimir í hóp fyrir eigendur afurða breytt stillingunni **Eigandi afurðar**.</span><span class="sxs-lookup"><span data-stu-id="d3398-123">While a product owner is assigned to a product, only the members of the product owner group can edit the **Product owner** setting.</span></span>

<span data-ttu-id="d3398-124">Eigandi afurðar er einnig sýnilegur á síðunni **Losaðar afurðir**.</span><span class="sxs-lookup"><span data-stu-id="d3398-124">The product owner is also visible on the **Released products** page.</span></span>

## <a name="product-owners-and-product-releases"></a><span data-ttu-id="d3398-125">Eigendur afurða og afurðarlosun</span><span class="sxs-lookup"><span data-stu-id="d3398-125">Product owners and product releases</span></span>

<span data-ttu-id="d3398-126">Aðeins notendur úr hópi fyrir eigendur afurða geta losað afurðina.</span><span class="sxs-lookup"><span data-stu-id="d3398-126">Only users from a product's product owner group can release that product.</span></span> <span data-ttu-id="d3398-127">Hins vegar er undantekning þegar afurðin er undireining og yfireining hennar er losuð af eiganda yfireiningarinnar.</span><span class="sxs-lookup"><span data-stu-id="d3398-127">However, there is an exception when the product is a child item, and its parent is released by the parent's owner.</span></span> <span data-ttu-id="d3398-128">Ef afurðin er hluti af UPPSKRIFT annarrar afurðar, kannar kerfið ekki eiganda hverrar afurðar í UPPSKRIFTINNI.</span><span class="sxs-lookup"><span data-stu-id="d3398-128">In other words, if the product is part of the BOM of another product, the system doesn't check the product owner of each item in the BOM.</span></span> <span data-ttu-id="d3398-129">Það athugar aðeins eiganda afurðar fyrir yfirafurðina.</span><span class="sxs-lookup"><span data-stu-id="d3398-129">It checks only the product owner of the parent item.</span></span>

<span data-ttu-id="d3398-130">Til dæmis er afurð X úthlutað á afurðareigendahópinn *Hanna skápa*.</span><span class="sxs-lookup"><span data-stu-id="d3398-130">For example, product X is assigned to the *Design cabinets* product owner group.</span></span> <span data-ttu-id="d3398-131">Afurð X er einnig hluti af UPPSKRIFT afurðar Y, sem er úthlutað á afurðareigendahópinn *Hanna hátalara*.</span><span class="sxs-lookup"><span data-stu-id="d3398-131">Product X is also part of the BOM of product Y, which is assigned to the *Design Speakers* product owner group.</span></span> <span data-ttu-id="d3398-132">Ef notandi úr afurðareigendahópnum *Hanna hátalara* losar afurð Y og uppskrift hennar verður afurð X losuð saman um leið og afurð Y.</span><span class="sxs-lookup"><span data-stu-id="d3398-132">If a user from the *Design Speakers* product owner group releases product Y and its BOM, product X will be released together with product Y.</span></span>

## <a name="product-owners-and-approvals"></a><span data-ttu-id="d3398-133">Eigendur afurða og samþykktir</span><span class="sxs-lookup"><span data-stu-id="d3398-133">Product owners and approvals</span></span>

<span data-ttu-id="d3398-134">Vegna þess að afurðareigendur vita hvort tilteknar hönnunarbreytingar muni koma sér vel fyrir þeirra afurð er oft skynsamlegt að taka þær með sem hluta af samþykktarferlinu í umsjón hönnunarbreytinga.</span><span class="sxs-lookup"><span data-stu-id="d3398-134">Because product owners know whether specific engineering changes will benefit their products, it often makes sense to include them as part of the approval process in engineering change management.</span></span> <span data-ttu-id="d3398-135">Hægt er að innleiða þessa nálgun með því að setja upp vörueigendur sem þátttakanda í verkflæðinu sem er notað fyrir umsjón hönnunarbreytinga.</span><span class="sxs-lookup"><span data-stu-id="d3398-135">You can implement this approach by setting up the product owners as participant providers in the workflows that are used for engineering change management.</span></span> <span data-ttu-id="d3398-136">Kerfið mun þá úthluta samþykktarverkefnum í verkflæði, byggt á þeim afurðum sem eru í stjórnunarbeiðnum og beiðnum um hönnunarbreytingar.</span><span class="sxs-lookup"><span data-stu-id="d3398-136">The system will then assign approval tasks in the workflows, based on the products that are in engineering change requests and engineering change orders.</span></span> <span data-ttu-id="d3398-137">Frekari upplýsingar eru í [Umsjón hönnunarbreytinga](engineering-change-management.md).</span><span class="sxs-lookup"><span data-stu-id="d3398-137">For more information, see [Manage changes to engineering products](engineering-change-management.md).</span></span>
